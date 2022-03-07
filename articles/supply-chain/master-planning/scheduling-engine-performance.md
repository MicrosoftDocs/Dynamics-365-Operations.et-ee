---
title: Ajastamismootori jõudluse parandamine
description: Selles teemas antakse teavet ajastamismootori ja selle jõudluse parandamise kohta.
author: ChristianRytt
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: crytt
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2495339f25469af705cff841f090c5df95b4d996
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578436"
---
# <a name="improve-scheduling-engine-performance"></a>Ajastamismootori jõudluse parandamine

[!include [banner](../includes/banner.md)]

Ressursside ajastamise mootorit kasutatakse plaanitud ja väljastatud tootmistellimuste protsesside ajastamiseks. Mootor anti algselt välja koos rakendusega Dynamics AX 2012 ja seda on pärast väljastamist mitu korda täiustatud.

[Tööde ajastamise probleem](https://en.wikipedia.org/wiki/Job_shop_scheduling) on äärmiselt keerukas kombinatoorikaprobleem, mille puhul kasvab lahendamisaeg muutujate arvu suurenedes eksponentsiaalselt. Sageli seavad kliendid tootmisprotsessid ja seotud andmed üles viisil, mis põhjustab ajastamisprobleemi, mida ei saa mõistliku aja jooksul lahendada isegi kõige moodsam riistvara. See teema aitab teil mõista ajastamismootorit ja seda, kuidas konkreetne seadistus võib jõudlust mõjutada.

Ajastamise jõudluse parandamise puhul soovitatakse üldiselt vähendada mootori lahendatava probleemi keerukust. Jõudlust võivad mõjutada muu hulgas peamiselt järgmised tegurid.

- Paljude toimingutega protsessid
- Paralleelsete toimingutega protsessid
- Toimingud, millel on rohkem kui üks ressurss
- Paljude rakendatavate ressurssidega toimingud
- Püsiseoste kasutamine
- Piiratud võimsuse kasutamine
- Kasutatavate kalendrite arv
- Tööajavahemike arv ühe kalendripäeva kohta
- Protsessi kogukestus
- Mitme ajastamismootori käitamine paralleelselt

## <a name="overview-of-basic-scheduling-flow"></a>Põhilise ajastamisvoo ülevaade

Et mõista, kuidas konkreetne seadistus võib jõudlust mõjutada, on oluline mõista seda, kuidas protsess toimib nii mootori sees kui ka keeles X++ kirjutatud koodis, mis seda ümbritseb.

Tellimuse ajastamise põhiprotsess koosneb kolmest põhietapist.

- **Andmete laadimine** – siin teisendatakse keeles X++ olevad andmemudelid tööde ja piirangute vormis mootori sisemiseks andmemudeliks.
- **Ajastamine** – see on ajastamise peamine allikas, mis töötleb konkreetset mudelit ja piiranguid, ning loob tulemuse. Selle protsessi käigus pärib mootor X++ koodist vajaduse järgi tööajateavet ja olemasolevaid võimsuse reserveeringuid.
- **Andmete salvestamine** – keeles X++ kirjutatud kood töötleb mootori tulemust, mis on töö võimsuse reserveeringute ajavahemike vormis, et salvestada võimuse reserveeringud ning värskendada tööde/toimingu/järjekorra algus- ja lõppaegasid.

## <a name="load-data-into-the-engine"></a>Andmete laadimine mootorisse

Ajastamismootoril on abstraktsem andmemudel kui rakenduse Supply Chain Management andmebaasil, kuna see loodi üldise mootorina, mis suudab töötada eri andmeallikatega. Protsessi, teiseste toimingute ja käitusaja mõisted tuleb „tõlkida” üldiseks töö- ja piirangumudeliks, mida mootor kasutab. Mudeli ehitamise loogika hõlmab üsna palju äriloogikat ja see erineb sõltuvalt lähteandmetest. Vastutav X++ klass on `WrkCtrScheduler` ning sellel on tuletatud klassid plaanitud tootmistellimuste, väljastatud tootmistellimuste ja projektiprognooside jaoks.

Näitena kaaluge järgmises tabelis ja pildil toodud protsessi, mis näib olevat üsna lihtne.

| Toim. nr | Prioriteet | Seadistusaeg | Käitusaeg | Ooteaeg pärast | Ressursside kogus | Järgmine |
| --- | --- | --- | --- | --- | --- | --- |
| 10 | Esmane | 1.00 | 2.00 | | 1 | 20 |
| 10 | Teisene&nbsp;1 | | | | 1 | 20 |
| 20 | Esmane | | 3.00 | 1.00 | 3 | 0 |

![Protsessidiagrammi näidis.](media/scheduling-engine-route.png "Protsessidiagrammi näidis")

Kui see saadetakse mootorisse, jagatakse see kaheksaks tööks, nagu on näidatud järgmisel illustratsioonil (klõpsake pildile, et seda suuremana näha).

[![Ajastamismootori tööd](media/scheduling-engine-jobs.png "Ajastamismootori tööd.")](media/scheduling-engine-jobs-large.png)

Standardne seos nende kahe töö vahel on `FinishStart`, mis tähendab, et ühe töö lõppaeg peab olema enne teise töö algusaega. Kuna seadistuse peab tegema sama ressurss, mis hiljem protsessis osaleb, on nende vahel `OnSameResource`'i piirangud. Number 10 esmase ja teisese toimingu tööde vahel on seosed `StartStart` ning `FinishFinish`, mis tähendab, et tööd peavad algama ja lõppema samal ajal, ning `NotOnSameResource`'i piirangud, mis takistavad sama ressursi kasutamist esmases ja teises toimingus.

Toimingu 20 puhul, kus ressursside kogus on 3, on protsessi töö jaotatud kolmeks eri tööks, mis kõik peavad juhtuma täpselt samal ajal.
Selle jaoks on seadistatud protsessirühm, mis takistab võimsuse reserveerimist pärastiste ooteaegade jaoks, mistõttu on pärastises ooteajas ainult üks töö.

Ajastamismootor mõistab ainult tööde mõistet ning sellel pole toimingutest aimugi. See tähendab, et toimingute ajastamisel jaotatakse toimingud samuti töödeks, kuigi neid ei hoita andmebaasis.

Iga töö jaoks määratleme ka töö võimsuse nõude (vajalike sekundite arv). Sõltuvalt sellest, kuidas ressursinõuded on määratletud, võime iga töö jaoks saata ka kõigi võimalike rakendatavate ressursside loendi, mida töö võib kasutada, ning teabe selle kohta, milline on selle konkreetse ressursi võimsuse nõue. Kuigi rakendatavate ressursside loend saadetakse mudeli ehitamisel, peab mootor ikkagi kindlaks tegema, et ressursi määramine kehtib tegelikult kogu töö jooksul.

## <a name="scheduling-engine-internals"></a>Ajastamismootori sisemised andmed

### <a name="scheduling-engine-interface"></a>Ajastamismootori liides

Et saada aimu, kuidas mootor sisemiselt töötab, on kõige parem vaadata funktsioone, mida see väliselt kasutab. Keeles X++ on peamine liides `WrkCtrSchedulerEngineInterface`. Sellel on järgmistes alajaotistes kirjeldatud meetodid.

#### <a name="general-engine"></a>Üldine mootor

| **Meetod** | **Eesmärk** |
| --- | --- |
| `run` | Ajastab kõik laaditud tööd ja tagastab tõrkekoodi. |
| `getJobSchedulingSequenceResult` | Saab ajastamistulemuse ja esimese tõrketöö kindla töö poolt tuvastatud järjestuse jaoks. |
| `validateJobCapacityReservations` | Kontrollib kõigi mootori salvestatud tööde võimsuse reserveeringud. |
| `setReservationsTimeStamp` | Saadab mootorisse ajatempli, mis hõlmab kõigi mootori vahemälus olevate ajastatud tööde uusi võimsuse reserveeringuid. |
| `addPropertyToGroupAggregation` | Lisab atribuudieesliite atribuutide kogumile, mida kasutatakse võimsuse koondamisel. |
| `addResource` | Lisab ressursi ajastamismootori ressursivarusse. |
| `addResourceGroup` | Lisab ressursirüma ajastamismootori ressursirühmavarusse. |
| `addResourceGroupMembership` | Lisab ressursi ressursirühma liikmena. |
| `addOptimizationGoal` | Lisab asjastamise optimeerimise eesmärgi (kestus või prioriteet). |

#### <a name="individual-jobs"></a>Üksikud tööd

| **Meetod** | **Eesmärk** |
| --- | --- |
| `addJobInfo` | Lisab tööteabe kirje, mis teavitab mootorit tööst, mis tuleb ajastada. |
| `addConstraintJobEndsAt` | Lisab piirangu, et töö peab lõppema määratud kuupäeval ja kellaajal. |
| `addConstraintJobStartsAt` | Lisab piirangu, et töö peab algama määratud kuupäeval ja kellaajal. |
| `addConstraintMaxJobDays` | Määratleb piirangu, et töö võib toimuda määratud maksimaalse päevade arvu jooksul. |
| `addConstraintResourceRequirement` | Lisab piirangu, et töö peab olema ajastatud kindla ressursi alusel. |
| `addJobBindPriority` | Lisab (tööde, piirangutasemete) paarile töö sidumisprioriteedi. Suurem prioriteediväärtus tähendab, et töö muutujad piiritletakse varem. Töö töödeldakse enne töid, millel on samas järjestuses madalam prioriteediväärtus. |
| `addJobCapacity` | Lisab täiskoormuse teabe tööle (nt nõutav töö käitusaeg) sõltumata sellest, millist ressurssi töö kasutab. |
| `addJobResourceCapacity` | Lisab ressursi ressursikogumile, mida saab kasutada töö tegemiseks, ning täpsustab, kui suur on vajalik võimsus selle ressursi kasutamisel. |
| `addJobGoal` | Lisab tööeesmärgi teabe kindlale piirangutasemele (varaseim lõppaeg või hiliseim algusaeg). |
| `addJobResourcePriority` | Lisab prioriteedi, mida kasutada siis, kui töö on ressursi jaoks ajastatud. |
| `addJobResourceRuntime` | Määrab tööaja, mis sõltub ressursist, mille jaoks töö ajastatakse. |
| `addJobRuntime` | Määrab tööaja, mis ei sõltu ressursist, mille jaoks töö ajastatakse. |
| `scheduleJobOnResourceGroup` | Märgib töö ressursirühma tasemel ajastamiseks. |
| `setJobResourcePreemptionAllowed` | Määrab, kas eelnev eraldamine on ressursi töö jaoks lubatud (kas mootoril on lubatud ajastada tööd mittekülgnevates võimsusvahemikes). |
| `setRequiredNumberOfResources` | Määrab töö ajastamiseks vajalike ressursside arvu (ainult toimingute planeerimiseks). |

#### <a name="constraints-between-jobs"></a>Töödevahelised piirangud

| **Meetod** | **Eesmärk** |
| --- | --- |
| `addJobLink` | Lisab kahe töö vahele seose (nt algus\>lõpp). |
| `addConstraintEndsDelayed` | Määratleb piirangu, et töö ei saa lõppeda enne teise töö lõppemist, millele on liidetud viivitusaeg. |
| `addConstraintJobListWorkingTimeIntersect` | Lisab piirangu, et tööde jaoks reserveeritud võimsusvahemikud peavad olema tööaegadel, mis kattuvad tööde kasutatud mõlema ressursi puhul. |
| `addConstraintJobOverlap` | Lisab piirangu, mis määratleb, kuidas töid järjestatakse, kui kindlat kaubakogust saab liigutada kahe ressursi vahel ajal, mil esimese ressursi töötlemine pole veel lõppenud, nii et teise ressursi töötlemine saaks alata. |
| `addConstraintNotOnSameResource` | Lisab piirangu, et kaht tööd ei tohiks sama ressursi jaoks ajastada. |
| `addConstraintOnSameResource` | Lisab piirangu, et kaks tööd peavad kasutama sama ressurssi. |
| `addJobSameReservations` | Lisab piirangu, et tööl peab olema lõpuks võimsuse reserveeringud esmase tööga samade ajavahemike jaoks. |
| `setPrimaryParallelJob` | Lisab teabe selle kohta, milline töö on paralleelsete tööde kogumis peamine töö. |

### <a name="solver"></a>Lahendaja

Mootor ise on põhimõtteliselt spetsialiseerunud piirangulahendaja, millele on lisatud kohandatud heuristikad. Lahendaja põhineb kahel peamisel elemendil: muutujad ja piirangud.

#### <a name="variable"></a>Muutuja

Muutuja tähistab võimalikke väärtusi. Ajastamismootoril on kaht tüüpi muutujaid.

- **Muutuja DateTime** – sisaldab kõiki kuupäevasid ja kellaaegasid ning vahemikku saab piirata, liigutades muutuja alumist ja ülemist piiri üksteisele lähemale.
- **Ressursi muutuja** – sisaldab rakendatavaid ressursse ning vahemikku saab piirata ressursside eemaldamise kaudu loendist.

#### <a name="constraint"></a>Piirang

Piirang mõjutab muutujaid, piirates nende vahemikke, kuid see sõltub ka muutujatest, mistõttu aktiveeritakse see muutujate muutumise korral. „Piirangu edasikandmise” protsess toimib nii, et piirang täidab oma põhifunktsiooni ja annab sellest põhiloogikale teada, kui kõik õnnestus.

Muutuja loetakse piiritletuks, kui seda ei saa enam rohkem piirata, mis tähendab muutuja DateTime puhul, et ülemine ja alumine piir on samad, ning ressursi muutuja puhul, et sellel on ainult üks rakendatav ressurss. Kui kõik muutujad on piiritletud, leitakse lahendus.

### <a name="constraint-levels"></a>Piirangutasemed

Kui ajastamine viiakse läbi materjalivajaduse planeerimise (MRP) katvuse faasi osana, ajastatakse tellimused vajaduse kuupäevast tagasiulatuvalt. Kuid kui sellise graafiku leidmine, mis algab täna või hiljem ja lõpeb enne vajaduse kuupäeva, on võimatu, muutub ajastamise suund tänasest edasiulatuvaks.

Seda põhilist ärireeglit käsitletakse tasemete piirangute organiseerimise kaudu. Kui kõrgeimal tasemel olevate piirangute kasutamisel lahendust ei leita, siis hüljatakse kõik need piirangud ja proovitakse madalamat taset. Praktikas tähendab see seda, et tagasiulatuva ajastamise korral sisaldab mudel taset 1, mille tööeesmärkidel on hilisem algusaeg, arvestades maksimaalse lõpuaja piirangut (vajaduse kuupäev), ja taset 0, mille tööeesmärkidel on varaseim lõppaeg, arvestades minimaalse algusaja piirangut ehk tänast päeva.

### <a name="algorithm"></a>Algoritm

Mootori algoritmi põhietapid on järgmised.

1. Leia järjestused (tööahelad), mida saab eraldi lahendada.
1. Ürita leida kõrgeima piirangutasemega järjestuse jaoks algne lahendus.
    1. Sordi järjestused olevad tööd tööeesmärkide ja prioriteetide alusel, et teha kindlaks algustöö.
    1. Käi tööd järgmises järjestuses läbi.
        1. Leia kõik piirangud, mis tuleb edasi kanda, ja käivita edasikandmine.
        1. Kui kõik töö muutujad on piiritletud, on leitud selle töö lahendus.
        1. Kui mõnda muutujat ei olnud võimalik piiranguid rikkumata piiritleda, siis tühista muutuja piiritlus, proovi muud saadavalolevat väärtust (ressursi muutuja puhul) ja käivita piirangute edasikandmine uuesti.
1. Kui lahendust ei leitud, eemaldatakse kõik praeguse piirangutaseme piirangud, langetatakse piirangutaset (kui leidub madalamaid tasemeid) ja lahendust üritatakse otsida uute piirangute alusel.
1. Kui leiti teostatav lahendus, alustatakse optimeerimisfaasi, mis püüab leida parema lahenduse, kuni jõutakse optimeerimise ajalõpuni või kõik ressursikombinatsioonid on läbi proovitud.

Piirangulahendaja ei tea ajastamisalgoritmi üksikasju. „Ime” sünnib mitmesuguste piirangute määratlemisel ja sobitamisel.

### <a name="determining-working-times"></a>Tööaegade kindlaks määramine

Suur osa mootori (sisemistest) piirangutest kontrollib ressursi tööaega ja võimsust. Sisuliselt on ülesandeks läbida ressursi tööajavahemikud kindlast kohast alates kindlas suunas ja leida piisavalt pikk intervall, millesse mahub töö vajalik võimsus (aeg).

Selleks peab mootor teadma ressursi tööaegu. Vastupidiselt põhiandmemudelile laaditakse tööaegu *laisalt*, mis tähendab, et need laaditakse mootorisse vajaduse järgi. Selle meetodi põhjus on see, et sageli hõlmavad rakenduse Supply Chain Management tööajad kalendris väga pikka perioodi ja tavaliselt leidub palju kalendreid, nii et eellaadida tuleks väga palju andmeid.

Kalendriteavet pärib mootor osadena, tuginedes X++ klassi meetodile `WrkCtrSchedulingInteropDataProvider.getWorkingTimes`. Päring hõlmab kindlat kalendri ID-d kindlas ajavahemikus. Sõltuvalt rakenduse Supply Chain Management serveri vahemälu olekust võidakse selliste päringute puhul teha mitu andmebaasikutset, mis võtab kaua aega (võrreldes puhta arvutusajaga). Kui kalender sisaldab väga keerulisi tööaja definitsioone, millel on päeva jooksul palju tööajaintervalle, pikendab see laadimise aega.

Kui tööaja andmed laaditakse ajastamismootorisse, säilitatakse see kindla kalendri sisemises vahemälus, mis tähendab, et kui sama kalendrit kasutavad teised tööd või ressursid, saab järgmised otsingud teha kiiresti mälust. Kehva jõudluse üks põhilisi põhjuseid on see, kui iga ressursi jaoks kasutatakse eraldi kalendri ID-d, sest sellisel juhul tuleb iga kalendri puhul andmeid uuesti pärida, kuigi kalendrite sisu võib olla sama.

### <a name="finite-capacity"></a>Piiratud võimsus

Kui kasutate piiratud võimsust, jaotatakse ja vähendatakse kalendri tööajavahemikud olemasolevate võimsuse reserveeringute põhjal. Need reserveeringud tuuakse samuti klassi `WrkCtrSchedulingInteropDataProvider` kaudu, nagu kalendrite puhul, kuid selle asemel kasutatakse meetodit `getCapacityReservations`. Koondplaneerimise ajal ajastamisel arvestatakse konkreetse koondplaani reserveeringuid ning kui see on lehel **Koondplaneerimise parameetrid** lubatud, kaasatakse ka kinnitatud tootmistellimuste reserveeringud. Samuti on tootmistellimuse ajastamisel võimalik kaasata olemasolevate plaanitud tellimuste reserveeringuid, kuigi see ei ole nii levinud kui teine valik.

Piiratud võimsuse kasutamine pikendab ajastamist mitme põhjuse tõttu..

- Võimsusteabe toomine andmebaasist on aeglane toiming ja võimsusteabe serveripoolne vahemälu ei ole tavaliselt nii hea kui tööaegade puhul, kuna neid ei jagata ressursside vahel, nagu tavaliselt kalendreid jagatakse.
- Läbitavate tööajavahemike arv suureneb jaotamise tõttu ning pikema perioodi vahemikke tuleb tavaliselt uurida enne lahenduse leidmist.
- Pärast ajastamise lõpetamist tuleb kontrollida vastuolulisi reserveeringuid (üksikasjad leiate jaotisest „Ajastamismootorite käitamine paralleelselt”).

### <a name="examining-the-resource-combinations"></a>Ressursikombinatsioonide uurimine

Kui tööde järjestus sisaldab ainult standardseid `FinishStart` seoseid, mis tähendab, et need moodustavad lihtsa ahela, millel ei ole ühtegi haru, siis on optimaalset tulemust (ühe tellimuse põhjal, mitte kõikide) võimalik saavutada, kui leida esimesele tööle parim lahendus ja seejärel liikuda edasi, et leida parim lahendus järgmisele tööle. Töö parim lahendus tähendab ressursi leidmist, mis võimaldab töö algus- ja lõppkuupäeva saada tööeesmärgile võimalikult lähedale (etteulatuva ajastamise korral tähendab see, et töö lõppkuupäev on võimalikult varajane), arvestades siiski piiranguid.

Paralleelsete tööde korral võib lahenduse leidmine hõlmata ressursside eri kombinatsioonide uurimist. Võimalike ressursikombinatsioonide arv sõltub ühendatud paralleelsete tööde puhul rakenduvate ressursside arvust. Võib võtta päris kaua aega, enne kui loogika taipab, et probleemile ei ole lahendust, mis mahutaks paralleelsed tööd enne tänast kuupäeva (eriti töötlemise ajastamisel vajaduse kuupäevast tagasiulatuvalt), kuna see peab kontrollima kõiki kombinatsioone, kuna võib leiduda mõni tõhusam ressurss või teine, tulemuseni viiv kalender. See tähendab, et kui ajalõpupiiri pole määratud, käitatakse seda pikka aega, enne kui suund edasiulatuvaks muudetakse.

See kombinatoorne loogika tähendab ka, et rakenduvate ressursside lisamine võib muuta mootori aeglasemaks. Kui paralleelsete toimingute ja piiramatu võimsusega ajastamise korral tekivad jõudlusprobleemid, saab seda osaliselt parandada, lastes protsessikujundajal vastu võtta otsus, millist ressurssi tuleks kasutada, ja seejärel määrata ressurss otse toimingule (kuna enamikul juhtudel valib mootor alati sama ressursi, nii et lõpptulemus on sama).

### <a name="hard-links"></a>Püsiseosed

Seosetüübi seadistamine kahe töö vahel püsivaks tagab, et ühe töö lõpu ja järgmise alguse vahel ei ole ajalist lünka. See võib olla väga kasulik sellistel juhtudel, kui metalli kuumutatakse ühes töös ja töödeldakse seejärel järgmises töös, mille korral ei tohiks metall vahepeal maha jahtuda.

Kui protsess moodustab standardsete paindlike seoste ja edasiulatuva ajastamise korral lihtsa ahela ilma harudeta, saab tulemuse saavutada siis, kui leida lahendus esimese töö jaoks, mis vastab omaenda piirangutele, ja seejärel liikuda mööda ahelat, kandes eelmise töö lõppaega edasi järgmisesse töösse. Kui praegune töö ei leia ühtegi võimsust, viiakse selle algusaeg edasi, mis ei mõjuta eelmisi töid, mistõttu võivad tööde vahele tekkida lüngad. Kuid püsiseoste korral (eriti piiratud võimsuse puhul) juhtub samas olukorras see, et kui ahelas hiljem käitatava töö jaoks ei leita võimsust, „lohistatakse” kõik eelmised ajastatud tööd ükshaaval sellega kaasa ja seetõttu ajastatakse mitu korda ümber. Püsiseosed võivad põhjustada ahelreaktsiooni, kus tööd mõjutavad üksteist ning enne tulemuse stabiliseerumist teostatavaks graafikuks tuleb itereerida mitu korda (eriti olukordades, kus mitmel ressursil on suur koormus).

## <a name="running-scheduling-engines-in-parallel"></a>Ajastamismootorite käitamine paralleelselt

Ajastamise korral koondplaneerimise osana, mille puhul kasutatakse abilisi, võivad kõik koondplaneerimise abilõimed samuti tootmistellimuse ajastamise ülesandeid endale võtta. See tähendab, et samal ajal saab käitada mitut ajastamismootorit. Kuigi lõimtöötlusel on üldiselt suur jõudluseelis, on sel ajastamise puhul ka mõni funktsionaalne probleem.

MRP-s ajastatakse kõik kindla koosluse (BOM) taseme tootmistellimused vajaduse kuupäeva järgi, mis tähendab, et varasema vajaduse kuupäevaga tellimused tuleb ajastada esimesena ja seega on neil kõige suurem võimalus kasutada saadaolevaid ressursse. Kuid olukorras, kus ajastamata tellimuste loendist teevad valikuid mitu mootorit, pole järjestus enam tagatud, kuna üks võib lõppeda kiiremini kui teine.

Kui ajastamine toimub piiratud võimsusega ja mitu mootorieksemplari üritavad ajastada tellimusi, mis kasutavad potentsiaalselt samu ressursse samas ajavahemikus, võib tekkida võidujooksu olukord. Võidujooksu tingimuste arv salvestatakse koondplaneerimise ajaloo lehe väljale **Ajastamiskonfliktid**. Konflikti lahendamise loogika on järgmine.

- Ajasta tellimus (lukuvaba) ja hangi võimsuse reserveeringud.
- Võta lukk.
- Kontrolli, kas ajavahemikus ajastatud ressursside jaoks on olemas uuemad võimsuse reserveeringud.
  - Kui ei, kirjutage võimsus üles ja vabasta lukk.
  - Kui jah, vabasta lukk ja ajasta tellimus uuesti algusest peale.

Nii et mitme mootorieksemplariga ajastamise korral ei ole tulemus täielikult deterministlik, kuna see sõltub iga lõime täpsest ajastusest.

## <a name="operation-scheduling-performance"></a>Toimingute ajastamise jõudlus

Kuigi toimingute ajastamist tuntakse ka kui üldise võimsuse plaanimisena, võib mootori vaatenurgast olla raskem probleemi lahendada, kui kasutatakse piiratud võimsust, kuna teostatavuse määramiseks on vaja rohkem andmeid.

Ressursirühma võimsus sõltub sellest, millised ressursid on ressursirühma liikmed ja mitu neid on. Ressursirühmal pole endal üldse võimsust – alles siis, kui rühmal on ressurssidest liikmeid, on sellel võimsus. Kuna ressursirühma liikmed võivad aja jooksul varieeruda, tuleb võimsust hinnata iga päeva kohta.

Toimingute planeerimisel kasutatakse ressursirühma kalendrit iga toimingu algus- ja lõppaja määramiseks. See tähendab, et ressursirühma kalender seab piirangu, kui palju aega saab ühes ressursirühmas ühes päevas ühe toimingu jaoks eraldada. Vastandina kindlate ressursside kalendrile eiratakse ressursirühma puhul kalendri tõhususandmeid, kuna need näitavad ainult avamisaegu ja mitte tegelikku võimsust.

Näiteks kui ühel kindlal kuupäeval on ressursirühma tööaeg alates 8.00 kuni 16.00, ei saa üks toiming ressursirühma koormata rohkem kui 8 tunniks, hoolimata sellest, kui suur võimsus ressursirühmal sellel päeval on. Saadaolev võimsus võib siiski koormust veelgi piirata.

Kui kindlal päeval arvutatakse ressursirühma saadaolevat võimsust, võetakse arvesse sellel päeval ressursirühmas olevate ressursside tööde ajastamise koormust. Iga kuupäeva puhul on arvutus järgmine.

*Saadaolev ressursigrupi võimsus = grupi ressursside võimsus kalendri põhjal &ndash; rühma ressurssidele rakenduv tööde ajastamise koormus &ndash; grupi ressurssidele rakenduv toimingute ajastamise koormus &ndash; ressursirühmale rakenduv toimingute ajastamise koormus*

Protsessitoimingu vahekaardil **Ressursinõuded** saab määratleda ressursinõuded kindla ressursi valimiseks (sel juhul ajastatakse toiming selle ressursi abil) või ressursirühma, ressursi tüübi, ühe või mitme võimekuse, oskuse, kursuse või sertifikaadi jaoks. Kuigi kõikide suvandite kasutamine muudab protsessi kujundamise paindlikuks, raskendab see ka mootori jaoks ajastamist, kuna võimsus peab olema arvestatud „atribuudi” kohta (abstraktne nimi, mida kasutatakse mootoris võimekuste, oskuste jne puhul).

Ressursirühma võimekuse võimsus on kõnealuse võimekusega ressursirühma kõikide ressursside võimsuse summa. Kui rühmas oleval ressursil on võimekus, siis arvestatakse seda sõltumata sellest, mis tasemel võimekus on vajalik.

Toimingute ajastamisel vähendatakse ressursirühma kindla võimekuse saadaolevat võimsust, kui see on koormatud toiminguga, mis vajab kõnealust võimekust. Kui toiminguks on vaja rohkem kui üht võimekust, vähendatakse võimsust kõigi nõutavate võimekuste puhul.

Iga kuupäeva puhul on nõutav arvutus järgmine.

*Võimekuse saadaolev võimsus = võimekuse võimsus &ndash; ressursirühmas sisalduvatele, kindla võimekusega ressurssidele rakenduv tööde ajastamise koormus &ndash; ressursirühmas sisalduvatele, kindla võimekusega ressurssidele rakenduv toimingute ajastamise koormus &ndash; kindlat võimekust vajavale ressursirühmale rakenduv toimingute ajastamise koormus*

See tähendab, et kui kindlale ressursile rakendub koormus, arvestatakse koormust ressursirühma saadaoleva võimsuse arvutamisel võimekuse järgi, sest kindla ressursi koormus vähendab selle panust ressursirühma võimekuse võimsusesse isegi siis, kui kindla ressursi koormus on selle võimekuse jaoks. Kui koormus rakendub ressursirühma tasemel, arvestatakse seda ressursirühma saadaoleva võimsuse arvutamisel võimekuse järgi ainult siis, kui koormus on pärit toimingust, mis vajab kindlat võimekust.

Ülaltoodud loogika on keeruline, kuna see on sama iga „atribuudi” tüübi puhul, nii et kasutades piiratud võimsusega toimingute ajastamist, tuleb laadida palju andmeid.

## <a name="viewing-scheduling-engine-input-and-output"></a>Ajastamismootori sisendi ja väljundi kuvamine

Ajastamisprotsessi sisendi ja väljundi täpsete üksikasjade hankimiseks lubage logimine, avades **Organisatsiooni haldus \> Seadistus \> Ajastamine \> Ajastamise jälgimise kokpit**.

Sellel lehel valige toimingupaanilt esiteks suvand **Luba logimine**. Seejärel käivitage tootmistellimuse ajastamine. Kui see on lõppenud, naaske lehele **Ajastamise jälgimise kokpit** ja valige toimingupaanilt **Keela logimine**. Värskendage lehte ning ruudustikus kuvatakse uus rida. Valige uus rida ja seejärel tegumipaanilt **Laadi alla**. See annab teile tihendatud .zip-kausta, mis sisaldab järgmisi faile.

- **Log.txt** – see on logifail, mis kirjeldab etappe, mida mootor läbib. See on väga keerukas ja võib olla veidi üle mõistuse käiv, kuid kui seda kasutatakse jõudlusprobleemide lahendamise eesmärgil protsessiseadistusega mängimise osana, tuleb esimesena leida üles erinevus esimese ja viimase rea aja vahel, sest see annab teile täpse ajastaja kulutatud aja.
- **XmlModel.xml** – see sisaldab mudelit, mis on loodud keeles X++ ja mida mootor töötades kasutab. Failis kasutatud suvand `JobId` vastab suvandile `RecId`, mis asub allikatabelis, mis sisaldab töid (`ReqRouteJob` või `ProdRouteJob`). Tüüpiline asi, millele selles failis tähelepanu pöörata, on see, et suvandite `ConstraintJobStartsAt` ja `ConstraintJobEndsAt` kuupäevad oleksid ootuspärased, et atribuut `JobGoal` oleks õigesti seadistatud ja et töökohad oleks üksteisega seotud `JobLink` piirangute kaudu.
- **XmlSlots.xml** – see sisaldab kõiki tööaegu ja võimsuse reserveeringuid, mida mootor on pärinud. Kalendri tööaegu ja reserveeringuid pärib mootor ainult ajaperioodide jaoks, millesse see üritab töid (ja lisapuhvrit) paigutada, nii et kui fail sisaldab aegu, mis on kauges tulevikus, võib see tähendada, et seadistus on probleemne. Sõlmedes `ResourceProperty` kuvatakse iga ressursi puhul millise ressursirühma ja võimekustega on see millisel perioodil seotud.
- **Result.xml** – see sisaldab ajastamise käitamise tulemust.

Pidage meeles, et jälgimise funktsioon võib jõudlust oluliselt vähendada, nii et kasutage seda ainult konkreetsete tellimuste ajastamise uurimiseks kontrollitud viisil. Kui see on koondplaneerimise käitamise ajal sisse lülitatud, jõuab see kiiresti oma suuruse piirini ja peatub.

## <a name="troubleshooting-performance"></a>Tõrkeotsingu jõudlus

Nagu eelmiste jaotiste põhjal võib aru saada, võib ajastamismootori seadistamisel ja kasutamisel tekkida vigasid, mis võivad viia jõudlusprobleemideni. Selliste probleemide tõrkeotsinguks saab kasutada järgmist kontroll-loendit. Oluline on kontrollida kõiki punkte, kuna kõige sagedamini põhjustab probleeme mitme teguri kombinatsioon.

### <a name="performing-scheduling-as-part-of-mrp-when-it-is-not-needed"></a>Ajastamine MRP osana, kui seda ei ole vaja

Kuigi protsesse kasutatakse tootmise juhtimise eesmärkidel, näiteks kuluarvutuse ja aruandluse jaoks, ei pruugi nende arvesse võtmine MRP ajal olla vajalik. Mõnel juhul on planeerimiseks piisav, kui kaubale on määratud standardne tootmise täitmisaeg. Protsessi ajastamise väljalülitamiseks seadke võimsuse ajapiir nulliks. Kui ajastamine peaks toimuma, tuleb võimsuse ajapiir määrata hoolikalt, kuna võib juhtuda, et protsesse ei pea arvesse võtma terve MRP katvuse ajapiiri jooksul.

Pidage meeles, et kui tellimust MRP ajal ei ajastada, tuleb see ajastada siis, kui plaanitud tellimus kinnitatakse. See tähendab, et kinnitamise protsess võtab kauem aega, nii et sõltuvalt sellest, kui paljusid soovitatud plaanitud tellimusi kinnitatakse, võib kinnitamine MRP ajal saadud parema jõudluse nullistada.

### <a name="route-with-unnecessary-operations"></a>Tarbetute toimingutega protsess

Protsessi kujundamisel võib tekkida kiusatus jäljendada pärismaailma täpselt koos iga sammuga, mis tootmises läbitakse. Kuigi see võib mõnel juhul kasulik olla, ei ole see jõudlust arvestades hea, sest mootori kasutatav mudel kasvab (nii tööde kui ka piirangute osas) ning tööde ja võimsuse reserveeringute sisestamiseks ja värskendamiseks käitatakse rohkem SQL-lauseid. Samuti tuleb lõpuks tööde edenemise kohta aru anda, mida saab lahendada automaatse sisestamise kaudu. Kui andmeid ei kasutata millekski, tekitab see tarbetut koormust.

Soovitame luua ainult toiminguid, mis on rangelt vajalikud ajastamiseks (mis on tavaliselt kitsaskohtadena toimivad ressursid) ja/või kuluarvutuse eesmärgil. Teise võimalusena peaksite liitma mitu väiksemat eraldiseisvat toimingut üheks suuremaks toiminguks, mis tähistab protsessi suuremat osa.

### <a name="many-applicable-resources-for-an-operation"></a>Toimingu paljud rakendatavad ressursid

Toimingu puhul rakendatavate ressursside arv määratletakse toimingu seoses määratud ressursinõuete alusel. Nõue võib hõlmata kindlat (üksikut) ressursi või põhineda ressursi ressursirühma kuulumisel või võimekusel.

Kui ajastamise puhul ei kasutata piiratud võimsust ja kõikidel rakendatavatel ressurssidel on sama kalender ning tõhusus, valib ajastamismootor toimingu jaoks alati sama ressursi, kuid ainult pärast kõigi rakendatavate ressursside proovimist, et kontrollida, kas on olemas mõni, mis on parem kui teised. Sellisel juhul saab ajastamise koormat oluliselt vähendada, määrates protsessi kujundamise ajal toimingule alati kindla ressursi.

### <a name="route-with-parallel-operations"></a>Paralleelsete toimingutega protsess

Kuigi paralleelsed toimingud (esmane/teisene) moodustavad võimsa tööriista selliste olukordade jäljendamiseks, kui kindlat ülesannet peavad täitma nii masin kui ka operaator, tekitab see samuti palju jõudlusprobleeme. Kui konkreetse üksiku ressursi nõue on määratud nii esmasele kui ka teisesele toimingule, ei ole see tavaliselt probleem. Kuid kui iga toimingu jaoks on olemas mitu võimalikku ressurssi, tõstab see ajastamise arvutamiskeerukust oluliselt.

Paralleelsete toimingute kasutamise alternatiiv on kas jäljendada paare „virtuaalsete” ressurssidena (mis siis esindavad meeskonda, mis on toimingus alati koos) või lihtsalt jätta üks toiming jäljendamata, kui see ei kujuta endast kitsaskohta.

### <a name="route-with-quantity-of-resources-higher-than-1"></a>Protsess, millel on ressursse rohkem kui üks

Kui toimingu jaoks vajalike ressursside kogus seatakse suuremaks kui üks, siis selle tulemuseks on sama, mis esmaste/teiseste toimingute kasutamine, sest mootorile saadetakse mitu paralleelset tööd. Kuid sel juhul ei ole võimalik määrata kindlaid ressursse, sest rohkem kui üht ressurssi nõudva koguse puhul peab toimingu jaoks olema rakendatav rohkem kui üks ressurss.

### <a name="excessive-use-of-finite-capacity"></a>Piiratud võimsuse liigne kasutamine

Piiratud võimsuse kasutamise puhul peab mootor laadima võimsusteavet andmebaasist ja selle arvutusaeg võib pikeneda, kuna lahenduse leidmine on raskem, eriti keskkondades, kus ressursid on reserveeritud lähedal nende maksimaalse võimsuse piirile. Seetõttu on oluline hoolikalt hinnata, kas ressurss peab tõesti piiratud võimsust kasutama või saab neid ülereserveerida. Kuna piiratud võimsusega ressursside puhul võib olla oluline see, milliseid ei tohiks kindlasti ülereserveerida, soovitame kasutada ressursis kitsaskohtade valikut koos plaani eraldi väärtusega suvandis „Võimsuse ajapiir kitsaskohana toimivate ressursside puhul”. Kitsaskohtade kontseptsiooni abil on võimalik lubada üldise piiratud võimsuse ajapiiri vähendamine.

### <a name="setting-hard-links"></a>Püsiseoste seadistamine

Protsessi standardne seosetüüp on *paindlik*, mis tähendab, et ühe toimingu lõpetamise ja teise alustamise vahele võib jääda vahe. Selle lubamise korral võib kahjuks juhtuda nii, et kui ühe toimingu jaoks ei ole materjale või võimsust väga pikka aega saadaval, võib tootmine olla üsna kaua jõudeolekus, mis tähendab poolelioleva töö võimalikku suurenemist. Seda ei juhtu püsiseoste puhul, kuna lõpp ja algus peavad sobima kokku täpselt. Kuid püsiseoste seadistamine muudab ajastamisprobleemi keerulisemaks, kuna tööaja ja võimsuse kattumised tuleb arvutada toimingute kahe ressursi jaoks. Kui sellega on seotud ka paralleelsed toimingud, muutub arvutusaeg oluliselt pikemaks. Kui kahe toimingu ressurssidel on erinevad kalendrid, mis ei kattu üldse, on probleem lahendamatu.

Soovitame kasutada püsiseoseid ainult äärmise vajaduse korral ning kaaluda hoolikalt, kas see on vajalik protsessi iga toimingu jaoks.

Et vähendada pooleliolevaid töid püsiseoseid rakendamata, on üks võimalus ajastada tellimus kaks korda, muutes teisel korral suund vastupidiseks. Kui esimene graafik tehti tarnekuupäevast tagasiulatuvalt, tuleks teine graafik teha ajastatud alguskuupäevast edasiulatuvalt. Selle tulemusena surutakse töid kokku nii palju kui võimalik, et pooleliolevaid töid oleks võimalikult vähe.

### <a name="separate-calendar-for-each-resource"></a>Eraldi kalender iga ressursi jaoks

Ajastamismootori puhul on üks andmete põhiallikaid kalendriteave, mille laadimine võib andmebaasist olla kulukas. Kuna kalendreid luuakse mallide põhjal, võib tekkida kiusatus luua iga ressursi jaoks kalender ja seejärel korrigeerida selles kalendris olevat teavet, kui ressursil on seisakuid ja muid probleeme. Kuid see piirab oluliselt mootori võimet kalendriandmeid vahemälusse salvestada, kuna see peaks iga ressursi puhul uusi andmeid pärima ning see võib olla suur jõudlusprobleemide allikas. Selle asemel soovitame teil taaskasutada ressursside jaoks kalendreid nii palju kui võimalik ja seejärel kontrollida seisakute muudatusi, määrates perioodi jaoks teistsuguse kalendri ID.

### <a name="high-number-of-working-time-slots-per-calendar-day"></a>Tööajavahemike suur arv ühe kalendripäeva kohta

Kuna mootor töötab nii, et uurib ajavahemikke võimsust silmas pidades ükshaaval, on kasulik vähendada ajavahemike arvu kalendripäeva kohta. Seda saab teha näiteks kaaludes, kas lõplikus kalendris on oluline ära märkida, et töötajatel on igas tunnis viieminutiline paus.

### <a name="large-or-none-scheduling-timeouts"></a>Suured (või puuduvad) ajastamise ajalõpud

Ajastamismootori jõudlust saab optimeerida, kasutades lehel **Ajastamise parameetrid** leitavaid parameetreid. Suvandite **Ajastamise ajalõpp on lubatud** ja **Ajastamise optimeerimise ajalõpp on lubatud** väärtus peaks alati olema **Jah**. Kui väärtus on **Ei**, võib ajastamine potentsiaalselt töötada lõpmatult, kui loodud on paljude valikutega teostamatu protsess.

Suvandi **Maksimaalne ajastamisaeg järjestuse kohta** väärtus määrab, mitu sekundit saab kõige rohkem kulutada ühe järjestuse lahenduse leidmisele (enamikul juhtudel vastab järjestus ühele tellimusele). Siin kasutatav väärtus sõltub suuresti protsessi keerukusest ja sätetest, nagu piiratud võimsus, kuigi maksimaalne arv 30 sekundit on hea koht, kust alustada.

Suvandi **Optimeerimiskatsete ajalõpp** väärtus määrab, mitu sekundit saab kõige rohkem kasutada algsest parema lahenduse leidmiseks. See mõjutab ainult paralleelseid toiminguid kasutavaid protsesse, kuna nende puhul on vajalik kontrollida eri kombinatsioone.

> [!NOTE]
> Ajalõppudele määratud väärtusi rakendatakse MRP osana nii väljastatud tootmistellimuste kui ka plaanitud tellimuste ajastamisel. Selle tulemusena võivad väga kõrged väärtused MRP käitusaega oluliselt pikendada, kui käitatakse paljude plaanitud tootmistellimustega plaani.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]