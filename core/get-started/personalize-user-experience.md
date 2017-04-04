---
title: "Kasutuskogemuse isikupärastamine"
description: Selles artiklis selgitatakse, kuidas teil Microsoft Dynamics 365 toiminguteks.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysUserSetup
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 8965c193839002776b3c61036b23b54625c974a4
ms.lasthandoff: 03/31/2017


---

# <a name="personalize-the-user-experience"></a>Kasutuskogemuse isikupärastamine

Selles artiklis selgitatakse, kuidas teil Microsoft Dynamics 365 toiminguteks.

Seal on palju liike isikupärastamisüksusi Microsoft Dynamics 365 toiminguteks. Mõned isikupärastamised on valikud, mille teete seadistuslehe suvandite loendis. Mõned isikupärastamisüksusi on kaudselt, näiteks Dynamics 365 operatsioonide jälgib võrgu Veergude laiused kui teil kohandada ja laiendada/lagunes riigi FastTabs. Muud isikupärastamised on selgesõnalised. Selgesõnaliste isikupärastamiste puhul sisenete interaktiivsesse isikupärastamise režiimi ja muudate lehe välimust, hallates otse, kuidas elemendid lehel kuvatakse või kuidas need käituvad. 

Kõik isikupärastamisüksusi, mis tahes liiki, mis kasutaja teeb Dynamics 365 toiminguteks on selle kasutaja, olenemata sellest, kui kasutaja seda kasutab ettevõte. Kasutaja lehele tehtud muudatused ei mõjuta süsteemi teisi kasutajaid.

## <a name="systemwide-options-for-the-current-user"></a>Praeguse kasutaja süsteemiga Valikud
Navigeerimisribal leiate hammasrattapildi, mida nimetatakse menüünupuks **Sätted**. Menüü **Sätted** avamisel kuvatakse mitu valikut. Suvandi **Sätted** valimine avab kasutaja lehe **Suvandid**. Sealt leiate neli suvandite vahekaarti: **Visuaalne**, **Eelistused**, **Konto** ja **Töövoog**.

-   **Visuaalne: **kasutage värvikujunduse ja lehtede elementide vaikesuuruste valimiseks.
-   **Eelistused:** siin saate vaikesätted, sest iga kord, kui avate Dynamics 365 koos firma, Avaleht ja Vaata/Muuda vaikere¾iim, (mis määrab kui lehe vaatamiseks lukustatud või avatud redigeerimiseks iga kord, kui avate seda). Samuti leiate keele, ajavööndi ja kuupäeva, kellaaja ning numbrivormingute suvandid. Lisaks sisaldab see leht mitmesuguseid eelistusi, mis erinevat väljaanneti.
-   **Konto: **kasutage oma kasutaja ID ja muude kontoga seotud suvandite jaoks.
-   **Töövoog: **siin saate valida töövooga seotud suvandeid.

## <a name="implicit-personalizations"></a>Varjatud isikupärastamised
Varjatud isikupärastamised on need isikupärastamised, mida teete, suheldes teatud juhtnuppudega, mis jätavad oma praeguse nähtava oleku meelde. 

**Ruudustiku veerud:** saate korrigeerida veeru laiust loendis, valides veerupäisest vasakul või paremal oleva suuruse muutise riba ja libistades seda soovitud laiuse saavutamiseks vasakule või paremale. Dynamics 365 operatsioonide salvestab laius, mis sulle meeldib ja näidata selle veeru see laius iga kord, kui avate lehe loetelu. 

**Kiirkaardid:** mõnel lehel on laiendatavad jaotised, mida nimetatakse kiirkaartideks. Salvesta Dynamics 365 meetmeteks, mille FastTabs on laienenud ja milliseid FastTabs on kokku kukkunud. Iga kord, kui lehele naasete, laiendatakse või ahendatakse neid samu kiirkaarte nende viimase kasutamise alusel. Selles artiklis selgitame, kuidas muuta kiirkaardi jaotiste järjekorda. Mõnel juhul on FastTab kokkuvajumine jõudlust suurendada sest Dynamics 365 operatsioonide vajab teavet alla laadida selle FastTab eest kuni selle FastTab on laiendatud. 

**Kiirinfo:** mõnel lehel on jaotis, mida nimetatakse kiirinfo paaniks. See paan sisaldab kirjutuskaitstud teavet, mis on seotud lehe praeguse teemaga. Igat kiirinfo paani jaotist nimetatakse kiirinfoks. Saate laiendada või ahendada asjaolu kasti ja Dynamics 365 operatsioonide salvestab oma eelistuse. Mõnikord kokkuvajumine asjaolu kasti jõudlust suurendada sest Dynamics 365 operatsioonide vajab teavet nimetatud asjaolu kasti tuua kuni asjaolu kast on laiendatud.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Selgesõnalised isikupärastamised tööriistariba Isikupärastamine kasutades
Igal inimesel ja ettevõttel on erinev vaatenurk sellele, milline teave nende jaoks kõige olulisem on või millist teavet ei ole vaja sel moel ettevõtte juhtimisel. Kohandada teie on tellitud, suhelnud või isegi nii peidetud on võtmeelement Dynamics 365 operatsioonide eksklusiivselt kogemus. 

Selgesõnaline isikupärastamisüksusi on isikupärastamisüksusi, mida selgesõnaliselt eesmärgiga muuta välimuse või käitumisega element või lehe, valides menüü isikupärastamine. Kõige elementaarsem selgesõnalise isikupärastamine on kus element paremklõpsake ja valige **isikupärastamine**. (Pange tähele, et kõik elemendid lehel saab isikliku.) Kui valite selle meetodi personaalse, näete elemendi vara akna. 

[![Isikupärastamiseks mõne elemendi atribuudid](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

Saate isikupärastada oma lehel oleva elemendi sel viisil, kui soovite lihtsalt muuta elemendi silti, peita elementi, et seda lehel ei kuvataks (see ei muuda andmeid, teile lihtsalt ei kuvata neid), lisada andmed kirikaardi kokkuvõtte ossa (kui element on kiirkaardil), jätta selle välja tabeldusklahviga vahele või teha nii, et andmeid ei saaks muuta, märkides need valikuga Ära muuda. 

Kui soovite elemente teisaldada või peita või teha mitu muudatust, saate kasutada tööriistariba Isikupärastamine, mis on saadaval elementide aknas Atribuut, kui valite suvandi **Vormi isikupärastamine**. Tööriistariba Isikupärastamine on saadaval ka vormi tegevuspaanil, vahekaardi **Suvandid** jaotises Isikupärastamisgrupp. Valige suvand **Vormi isikupärastamine** ja näete tööriistariba Isikupärastamine. 

[![Isikupärastamise tööriistariba](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Isikupärastamise tööriistaribal on mitmeid isikupärastamine. Valige tööriist **Vali**, kui soovite valida ja muuta korraga mitme elemendi atribuute. Esmalt klõpsake tööriista Vali ja siis elementi, mille atribuute muuta soovite. Elemendi valimisel avaneb elemendi atribuutide aken ja saate muuta selle elemendi mis tahes atribuute. Saate protsessi vormi muude isikupärastatavate elementide jaoks korrata. Mõnel juhul valite elemendi ja näete, et mõned atribuudid ei ole muudetavad. See tähendab, et vastavalt kuidas elemendil kasutatakse, Dynamics 365 toiminguteks ei saa teile seda atribuuti muuta. Näiteks ei saa te peita nõutavat välja. 

Valige tööriist **Teisalda**, kui soovite valida ja teisaldada elementi erinevasse asukohta praeguses elementidegrupis. (Te ei saa teisaldada elementi selle emagrupist väljapoole). Esmalt klõpsake tööriista Teisalda ja siis elementi, mida teisaldada soovite. Soovitud elemendi klõpsamisel Dynamics 365 operatsioonide näidatakse skaneeri vorm mõista, kui selle elemendi teisaldatav ja luua mitmeid "rippmenüüst piirkonnad", et näidata kus element võib langes elemendi ümber praeguse grupi lohistamise ala kõrval värviline, julge joonega. 

Valige tööriist **Peida**, elemendi valimiseks ja peitmiseks. Elemendi peitmiseks valige lihtsalt tööriist Peida ja klõpsake elementi, mida peita soovite. Kui valite tööriista Peida, muudetakse kõik praegu peidetud elemendid nähtavaks ja neid näidatakse varjutatud konteineris, nii et saate valida elemendi selle nähtavaks tegemiseks. Valige tööriist Vali nägemaks, kuidas leht valitud peidetud elementidega välja näeb. Valige tööriist **Kokkuvõte**, kui soovite, et numbrilist või stringivälja näidataks kiirkaardi kokkuvõtte alal. Tööriist Kokkuvõte rakendub ainult väljadele, mis sisalduvad kiirkaardi jaotises. Kokkuvõte tööriista valimisel Dynamics 365 operatsioonide näitab kõik väljad, mida ümbritseb neid varjulises nõus Kokkuvõte väljadena valitud. Saate välju kiirkaardi kokkuvõttesse interaktiivselt lisada ja neid sealt eemaldada, klõpsates välja. 

Valida on **vahele** vahend eemaldada elemendi lehe klaviatuuri järjestuse. Jäta tööriist valimisel kuvatakse varjutatud nõus kõik praegu vahele jäetud elemente nii, et saate neid uuesti teha neid osa vahele elementi valides järjestuse. 

Valige tööriist **Redigeeri**, kui soovite lisada elemendile märke Redigeeritav või Ei ole redigeeritav. Kui valite tööriista Redigeeri, näidatakse kõiki praegu mitteredigeeritavaid elemente varjutatud konteinetis, nii et saate neid valida, et muuta need redigeeritavaks. Arvestage sellega, et mõned väljad on nõutavad ja neid ei saa mitteredigeeritavateks muuta. Nende väljade kõrval kuvatakse tabalukuikoon. 

Valige tööriist **Lisa**, et lisada väli lehele. Tööriistaga Lisa ei saa te luua uut välja, kuid saate lisada välju, mis on osa praeguse lehe määratlusest, kuid mida lehel ei näidata. Kui valite tööriista Lisa, peate esmalt valima grupi või ala, kuhu soovite välja lisada. Dialoogikast kuvab teie valitud jaotisega seotud väljade loendi. Sellest dialoogikastist saate valida lisamiseks ühe või mitu välja ja klõpsata nuppu Lisa. Kui soovite hiljem varem lisatud välja eemaldada, korrake protsessi, kuid lihtsalt kustutage varem lisatud väli. 

Valida on **Halda** nuppu loendi juhtimisotsuste seotud kõik isikupärastamisüksusi praeguse lehe. 

Valige **selge** lehe lähtestamiseks vaikesätetele, paigaldatud riik. Teenin isikupärastamisüksusi praegusel lehel. Võta tagasi toimingust, vaid kasutage seda suvandit, kui olete kindel, et soovite lähtestamine leht. 

Valige suvand **Impordi**, et kasutada isikupärastamist isikupärastamise failist, mille teie või keegi teine on lehele varem loonud. Isikupärastamise importimine kustutab kogu lehel mis tahes isikupärastamised ja kasutab hoopis kõiki valitud faili isikupärastamisi. Kui soovite isikupärastamist salvestada või ühiskasutusse anda, valige suvand **Ekspordi**, et salvestada isikupärastamised faili. 

Valige nupp **Sulge**, et sulgeda tööriistariba ja viia leht uuesti selle eelmisesse interaktiivsesse olekusse. 

Tööriistaribaga Isikupärastamine on salvestamine varjatud. Teie isikupärastamised jõustuvad kohe, kui need teete, ja ei ole vaja klõpsata nuppu **Salvesta**. Mõnel juhul näete tabaluku ikooni kõrval element vahend valimisel. See tähendab, et lehe töötada õigesti et, ei saa muuta atribuudid, mis on seotud valitud tööriista. Kui tööriistariba Isikupärastamine on avatud, muutub leht mitteinteraktiivseks. Te ei saa andmeid sisestada ega jaotisi laiendada või ahendada.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Selgesõnaline isikupärastamine: tööruumile paani või loendi lisamine
Mõnel loenditega lehel on toimingupaanil vahekaardi Suvandid jaotises Isikupärastamisgrupp saadaval täiendav isikupärastamise funktsioon. Valige suvand **Lisa tööruumi**, et avada ripploend, mis annab teile võimaluse näidatata praeguses loendis olevat teavet (filtreeritud ja sorditud või vaikimisi) tööruumis loendi või kokkuvõttepaanina (seda saab kasutada loendis olevate kaupade arvu näitamiseks). 

[![Add to workspace](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Tööruumile loendi lisamiseks sortige või filtreerige esmalt loendi teavet, nagu soovite seda oma tööruumis näha, ja seejärel valige dialoog Lisa tööruumi. Järgmisena valige soovitud tööruum ja valige ripploendit Esitlus suvand **Loend**. Kui valite suvandi **Loend**, avaneb dialoog, mis võimaldab teil valida veerud, mida sooviksite loendis näha, ja loendi silt, nagu see tööruumis kuvatakse. 

Tööruumile paani lisamiseks filtreerige esmalt loendit, et esitada andmed, mida soovite kokku võtta (või millele soovite kiiret juurdepääsu). Seejärel avage rippdialoog Lisa tööruumi. Järgmisena valige soovitud tööruum ja valige ripploendist Esitlus suvand **Paan**. Kui valite suvandi **Paan**, avaneb dialoog, mis võimaldab teil lisada paani sildi ja otsuatada, kas paan näitab loendust. Tööruumi paigutatud paan võimaldab teil avada praegust lehte tööruumist ja näidata paaniga seotud teabe loendit. 

Kui loend või paan on tööruumi lisatud, saate selle tööruumi avada ja loendi või paani uuesti tellida grupist, kuhu see paigutatud oli.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Selgesõnaline isikupärastamine: kokkuvõtte lisamine tööruumist armatuurlauale
Mõnda tööruumi sisaldavad arv plaadid (plaatide numbritega nende kohta), mida soovite ka näha oma armatuurlaud. Tööruum, paremklõpsake arvu ruutu ja valige **isikupärastamine**. Valige suvand **Kinnita armatuurlauale**. Järgmine kord, kui navigeerite valitud armatuurlauale (ja värskendate seda), näete seda arvu selle tööruumi navigeerimispaani all armatuurlaual.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Selgesõnaline isikupärastamine: armatuurlaua isikupärastamine
Juhtpaneel on sageli esilehel näete, kui avate Dynamics 365 toiminguteks. Saate armatuurlauda isikupärastada nimetama ümber tööruumi navigeerimispaane, näitama ainult paane, mida näha soovite, paane pmber nimetama või korraldama paane eelistatud järjekorda. Armatuurlaya isikupärastamiseks valige mis tahes paan ja paremklõpsake kontekstimenüü avamiseks. Valige kontekstimenüüs suvand **Isikupärasta**. Kui valitud paan on see, mida soovite peita või ümbe nimetada või vahele jätta, saate teha selle muudatuse otse kuvatavas aknas Atribuut. Kui soovite paane ümber korraldada, siis valige aknas Atribuut suvand **Vormi isikupärastamine**, et avada tööriistariba Isikupärastamine. Seejärel saate kasutada paanide ümberkorraldamiseks tööriista Teisalda.

## <a name="administration-of-personalization"></a>Isikupärastamise haldamine
On võimalik isikupärastada leht ja ühiskasutada seda teiste kasutajatega, eksportides lihtsalt isikupärastatud leht ja paludes teistel kasutajatel isikupärastatud lehele navigeerida ja importida loodud isikupärastatud fail. Kui kasutajal on administraatori privileegid, saab ta hallata ka teiste kasutajate isikupärastamisi lehel **Isikupärastamise seadistus**. Navigeerige lehele b. Lehel **Isikupärastamine** leiate kaks vahekaarti, üks on tähistatud sildiga **Süsteem** ja teine sildiga** Kasutajad**. 

**Süsteem:** siin saate ajutiselt keelata või välja lülitada kõik süsteemi isikupärastamised. See ei kustuta isikupärastamisi, vaid lähtestab kõik vormid nende vaikeolekusse. Hiljem saate isikupärastamise uuesti lubada, et kõik isikupärastamised igale kasutajate vormile uuesti rakendada. Samuti saate kustutada kõikide kasutajate kõik isikupärastamised. Arvestage sellega, et kui kustutate isikupärastamisi, siis puudub võimalus isikupärastamiste automaatseks uuesti lubamiseks süsteemist. Veendute, et olete eksportinud isikupärastamised, mida soovite võib-olla hiljem importida, enne kui selle toimingu teete. 

**Kasutajad:** siin saate iga kasutaja puhul otsustada, kas ta saab läbi viia selgesõnalist või varjatud isikupärastamist. Samuti saate otsustada, kas iga kasutaja saab läbi viia varjatud või selgesõnalist isikupärastamist kindlas vormis. Lõpuks saate importida või eksportida või kustutada iga kasutaja isikupärastamise. 

**Märkus.** Algses väljaandes võimaldab isikupärastamise haldus kasutaja haldamist ainult kasutaja alusel.


