---
title: "Tööjaotuse struktuurid"
description: "Tööjaotuse struktuur (WBS) on projekti puhul tehtava töö kirjeldus. See on ülesannete hierarhia, mis kajastab projekti töörühma arusaama töö koosseisust ja iga osa või ülesande ulatusest, maksumusest ja kestusest."
author: twheeloc
manager: AnnBe
ms.date: 06/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 6d4391f1a6fa517b447387562fd3216201451316
ms.contentlocale: et-ee
ms.lasthandoff: 06/20/2017

---

# <a name="work-breakdown-structures"></a>Tööjaotuse struktuurid

[!include[banner](../includes/banner.md)]

Tööjaotuse struktuur (WBS) on projekti puhul tehtava töö kirjeldus. See on ülesannete hierarhia, mis kajastab projekti töörühma arusaama töö koosseisust ja iga osa või ülesande ulatusest, maksumusest ja kestusest. WBS-il on kolm suurt eesmärki.

-   Kirjeldada tööjaotust või koosseisu ülesannetes.
-   Plaanida projekti tööd.
-   Prognoosida iga ülesande maksumust.

WBS-i üksikasjalikkuse tase sõltub prognoosides vajalikust täpsuse tasemest ja nende prognooside suhtes vajaliku jälgimise tasemest.. Projektid, mille puhul on lubatud väga väike graafikust või maksumusest kõrvalekalle, nõuavad tavaliselt üksikasjalikumat WBS-i ja hoolikat töö edenemise ning maksumuse jälgimist WBS-i suhtes. Seda tüüpi projekt on tavapärane ehituse ja tehnika valdkondades. 

Vastukaaluks on meedia ja reklaami, tarkvara ja IT-taristu valdkondade projektid pigem ainulaadsed ja produktiivsus sõltub ülesande läbiviija kogemusest ja kompetentsusest. Seetõttu kasutatakse nendes valdkondades WBS-i projekti ulatuse hindamiseks, mitte projekti üksikasjaliku edenemise jälgimiseks. 

WBS-i koostamine on intensiivne protsess, mida tehakse tavaliselt kaua ja mis nõuab koostööd ning teavet väga mitmesugustelt inimestelt. See teema kirjeldab, kuidas saate kasutada WBS-i täiustusi rakenduses Microsoft Dynamics 365 for Finance and Operations teie hinnangutele ja jälgimise nõuetele vastamiseks.

## <a name="prerequisites-for-creating-a-wbs"></a>WBS-i loomise eeltingimused
WBS-i loomiseks tuleb koostada tööplaan ja prognoosida töö maksumust.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Tööplaani loomise eeltingimused

WBS-i funktsioonide täielike plaanimisvõimaluste kasutamiseks tehke järgmine seadistus.

1.  Seadistage vaikekalender ja projekti kalender.
    1.  Klõpsake nuppe **Projektihaldus ja -arvestus** &gt; **Seadistus** &gt; **Planeerimine**. Määrake vaikekalender väljal **Töö vaikekalender**. See on iga uue loodava projekti töö vaikekalender.
    2.  Saate konkreetse projekti vaikekalendrit muuta. Klõpsake projekti üksikasjade lehte ja seejärel uuendage kiirkaardil **Projekti töörühm ja plaanimine** välja **Plaanimiskalender**, valides teise kalendri.

2.  Saate seadistada standardsed tööpäevad ja tööaja. Projekti töökalendriks määratavat kalendrit kasutatakse WBS-is järgmise teabe määratlemiseks.

-   Tööpäevad ja puhkepäevad
-   Päeva töötundide arv

Kalendri tööpäevade ja töötundide seadistamiseks või uue kalendri loomiseks klõpsake valikuid **Organisatsiooni haldus** &gt; **Üldine** &gt; **Kalendrid**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Töö kulude hindamise eeltingimused

WBS-i kulude prognoosimise võimaluste täielikuks kasutamiseks tuleb seadistada kulud ja müügihinnad töötajatele, töö kategooriatele, kuludele ja tasudele ning kaupadele.

-   Tööjõu, kulu ja tasu kategooriatele kulude ja müügihinna seadistamiseks klõpsake valikuid **Projektihaldus ja -arvestus** &gt; **Seadistus** &gt; **Hinnad**.
-   Kaupade maksumuse ja müügihinna seadistamiseks kasutage iga kauba lehte **Kaubanduslepped** mooduli Tooteteabe haldus loendilehel **Väljastatud tooted**.

## <a name="creating-a-wbs"></a>WBS-i loomine
WBS-i loomine hõlmab kolme tegevust.

1.  **Töö eraldamine** – töö eraldatakse hallatavateks tükkideks või ülesanneteks.
2.  **Töögraafik** – saate hinnata aega, mis on vajalik ülesande lõpuleviimiseks, määrata ülesande sõltuvused ja valida ülesande algus- ning lõpukuupäevad.
3.  **Kulu kalkuleerimine** – saate hinnata iga ülesande kulusid.

Järgmistes jaotistes kirjeldatakse, kuidas WBS-i võimalused saavad aidata iga sellist tegevust.

### <a name="work-decomposition"></a>Töö eraldamine

Tööjaotus või töö eraldamine on tavaliselt WBS-i loomise protsessi esimene etapp. WBS-i funktsioon toetab järgmisi tööjaotuse struktuuri või eraldamise põhikonstruktsioone. 

**Projekti juurülesanne** Projekti juurülesanne on projekti ülataseme kokkuvõttev ülesanne. Kõik teised projekti ülesanded luuakse selle alla. Juurülesande nimeks määratakse alati projekti nimi. Panus, kuupäevad ja juursõlme kestus võtavad juurülesande all kokku ülesannete väärtused. Juursõlme atribuute ei saa muuta ning seda ei saa kustutada.

**Kokkuvõtvad või konteinerülesanded** Kokkuvõttev ülesanne on ülesanne, mille all on alam- või koostisülesanded. Kokkuvõtval ülesandel pole oma tööpanust ega maksumust. Selle asemel on kokkuvõtva ülesande tööpanus ja maksumus selle koostisülesannete tööpanuse ja maksumuse summa. Koostisülesannete varaseimat alguskuupäeva kasutatakse kokkuvõtva ülesande alguskuupäevana ja koostisülesannete hiliseimat lõppkuupäeva kasutatakse lõppkuupäevana. Kokkuvõtva ülesande nime saab muuta, kuid panuse, kuupäevade ja kestuse plaanimisatribuute ei saa muuta. Kokkuvõtva ülesande kustutamisel kustutatakse ka kõik selle koostisülesanded. 

**Lehe sõlmülesanded** Lehe sõlmülesanne kajastab projekti kõige detailsemat tööpaketti. Lehel on prognoositav panus, plaanitud ressursside arv, plaanitud algus- ja lõppkuupäev ning kestus. 

Tööhierarhia loomise või projekti lahtikirjutamise lubamiseks saab teha järgmisi hierarhiatoiminguid. 

**Uus ülesanne** Iga uus ülesanne, mille loote, lisatakse automaatselt juursõlme alla ja ülesandele määratakse automaatselt WBS-i number. WBS-i number kajastab ülesande taset hierarhias. Projekti juurülesande all esimesel tasemel olevate ülesannete puhul kasutatakse nummerdamise skeemi 1, 2, 3 jne. Esimese taseme all olevate ülesannete puhul kasutatakse nummerdamise skeemi 1.1, 1.2, 1.3 jne. Iga eelmise taseme alla lisatava taseme puhul lisatakse uus punktiga numbriseeria. 

Praegu ei saa WBS-i nummerdamist kohandada. 

**Ülesande taandamine** Ülesande taandamisel saab sellest sellele eelneva ülesande alamülesanne. Uue alamülesande WBS-i number arvutatakse selle uue põhiüksuse WBS-numbri põhjal automaatselt ümber. Põhiülesanne on nüüd kokkuvõttev või konteinerülesanne ja seetõttu saab sellest koostisülesannete kokkuvõte. 

> [!NOTE] 
> Kui taandate ülesandeid ülesande all, mis oli enne taandamistoimingut lehe sõlm, kaotab loodud kokkuvõttev ülesanne oma kuupäevad, panuse ja ressursside arvu. Nüüd kasutab see oma uute koostisülesannete väärtusi. 

**Ülesande eendamine** Kui ülesande eendate, pole see enam oma põhiüksuse koostisülesanne. Ülesande WBS-i number arvutatakse automaatselt ümber, et kajastada ülesande uut taset hierarhias. Ülesande eelmise põhiülesande panus, kulu ja kuupäevad arvutatakse ümber, jättes selle ülesande välja. 

**Nihuta üles ja Nihuta alla** Kui klõpsate nuppe **Nihuta üles** ja **Nihuta alla**, muudate ülesande asukohta põhihierarhias. Ülesande asukoht ei mõjuta ülesande panust, maksumust, kuupäevi ega kestust. Kuid ülesande WBS-i number arvutatakse automaatselt ümber, et kajastada ülesande uut asendit.

### <a name="schedule-estimation"></a>Graafiku prognoosimine

Graafiku prognoosimine on tavaliselt WBS-i loomise teine etapp. Graafikut on kõige parem prognoosida pärast ülesannete loomist. Finance and Operationsi lehel **Tööjaotuse struktuur** on kaks osa. Ülemine paan on mõeldud graafiku prognoosimiseks ja alumisel paanil on vahekaart **Eeldatavad kulud ja tulud**, mida saate kasutada kulude prognoosimiseks. 
**Ülesande sõltuvused** WBS-is saab luua ülesannete vahel eelkäija seose. Kui määrate ülesandele eelkäijatest ülesanded, saab ülesanne alata alles siis, kui kõik eelkäijatest ülesanded on lõpetatud. Ülesande plaanitavaks alguskuupäevaks määratakse automaatselt kõigi selle eelkäijate hiliseim kuupäev. 

**Ülesannete plaanimine rakenduses Finance and Operations** Järgmised tegurid määravad lehe sõlme ülesannete ajastamise.

-   Eelkäijad
-   Panus
-   Ressursside arv
-   Algus- ja lõppkuupäevad

Ilma eelkäijateta lehe sõlmülesande alguskuupäevaks määratakse automaatselt projekti plaanimise alguskuupäev. Lehe sõlmülesande kestus arvutatakse alati algus- ja lõppkuupäevade vaheliste tööpäevade arvuna. 

****Plaanimisreeglid**** Kui automaatne plaanimisabi on sisse lülitatud, kehtivad lehe sõlmülesannete plaanimisel järgmised reeglid.

-   Ülesande algus- ja lõppkuupäevad peavad olema projekti planeerimise kalendrile vastavad tööpäevad.
-   Eelkäijatega ülesande alguskuupäevaks määratakse automaatselt selle eelkäijate hiliseim lõppkuupäev.
-   Ülesande panus arvutatakse automaatselt järgmisel viisil.

Inimeste arv × kestus × tundide arv standardsel tööpäeval projektikalendris. 

Mõnikord võite soovida neist reeglitest kõrvale kalduda. Saate lülitada automaatse plaanimise välja, et Finance and Operations ei seadistaks ega korrigeeriks automaatselt lehe sõlmülesannete atribuute. Kui sisestate ülesandele teavet, mis põhjustab mõne plaanimisreegli rikkumise, kuvatakse selle ülesande puhul plaanimisvea ikoon. Kui te ei soovi, et plaanimisvigu kuvatakse, klõpsake funktsiooni väljalülitamiseks valikut **Plaanimisvead on kuvatud**. 

> [!NOTE] 
> Kokkuvõtva või konteinerülesande väärtusi arvutatakse jätkuvalt koostisülesannete väärtuste summana, olenemata sellest, kas automaatne plaanimisabi on sisse või välja lülitatud. 

**Plaanimisvigade parandamine** Kui automaatne plaanimisabi on sisse lülitatud, siis plaanimisvigu tõenäoliselt ei esine. Kuid kui lülitate automaatse plaanimisabilise välja ja siis hiljem uuesti sisse, võidakse WBS-is kuvada plaanimisvea ikoonid. 

**Plaanimisvigade parandamine ülesannete kaupa** Kui teete plaanimisvea ikoonil konkreetse ülesande puhul topeltklõpsu, kuvab dialoogiboks kõik selle ülesande plaanimisvead. Saate valida, milliseid plaanimisvigu selle ülesande puhul parandada. 

**Kõigi plaanimisvigade parandamine** Kui soovite, et Finance and Operations parandaks WBS-is kõik plaanimisvead, klõpsake valikut **Paranda kõik plaanimislahknevused**. 

> [!NOTE] 
> See funktsioon võib põhjustada WBS-ile olulisi muudatusi. Vead parandatakse järgmises järjestuses.

1.  Kõigi ülesannete hinnangulist panust muudetakse nii, et see oleks võrdne projekti kalendris määratud mahuga.
2.  Ülesande alguskuupäeva muudetakse nii, et ülesanne algab pärast selle eelkäijatest ülesannete lõpetamist.
3.  Iga ülesande alguskuupäeva muudetakse, eemaldades vahed eelkäijatest ülesannete alguskuupäevades.

### <a name="cost-estimation"></a>Kuluhinnang

Nagu selles dokumendis eespool mainiti, tuleb iga lehe sõlmülesande kuluprognoos sisestada vahekaardil **Eeldatavad kulud ja tulud** lehe **Tööjaotuse struktuur** alumisel paanil. 

> [!NOTE] 
> Kokkuvõtva või konteinerülesande kuluprognoosi ei saa muuta. Kokkuvõtva ülesande kuluprognoos võrdub selle lehe sõlmülesannete kuluprognoosi summaga. Iga ülesande eeldatav kogukulu arvutatakse eeldatavate kulude summana järgmiste kandetüüpide puhul.

-   Tööjõud
-   Kaup või materjal
-   Kulud

Kandetüüpi **Tasu** kasutatakse tasupõhise tulu prognoosimiseks. Sellel kandetüübil pole kulukomponenti ja seetõttu ei arvestata seda kulude prognoosimisel. 

Kandetüüpi **Ettemaks** kasutatakse lepingu müügiväärtuse kajastamiseks fikseeritud väärtusega projektis. Seda kandetüüpi ei arvestata samuti kulude prognoosimisel. 

Iga toimingu tööjõukulu, materjalikulu ja muude kulude prognoosimisel tuleb määrata eeldatavale kulule projektikategooria. 

**Tööjõukulude prognoosimine** iga lehe sõlmülesande puhul saab määrata tööpanuse tundides ning vaikekategooria. Seetõttu lisatakse ülesande graafiku seadistamisel selle ülesande tööjõukulu prognoos automaatselt tööjõu vaikekategooriasse. See kuluprognoos kuvatakse vahekaardil **Eeldatavad kulud ja tulu** selle ülesande ruudustikus **Rea üksikasjad**. Kui vajate rohkem tööjõukulu prognoose, saate lisada neid sellel vahekaardil. Tööjõukulu prognoosi tundide arvu suurendamisel või vähendamisel arvutatakse ülesande graafik automaatselt ümber. 

**Kulude ja materjali maksumuse prognoosimine** Vahekaardil **Eeldatavad kulud ja tulu** saate prognoosida ka ülesande kulusid ja materjali maksumust, kui prognoosid on vajalikud. 

Iga tööjõu või kuluprognoosi rea kulu ja müügihind põhinevad seadistusel, mis on jaotises **Projektihaldus ja -arvestus** &gt; **Seadistus** &gt; **Hinnakujundus** olevates hinnatabelites igale kategooriale määratletud. Kaupade puhul lisatakse nende maksumus ja müügihind vaikimisi kaubalt või kaubanduslepetest mooduli Tooteteabe haldus loendilehel **Väljastatud tooted**.

## <a name="tracking-progress-on-the-wbs"></a>Edenemise jälgimine WBS-is
Mõnes valdkonnas jälgitakse projekti edenemist WBS-i suhtes väga detailsel tasemel, samas kui teistes jälgitakse edenemist WBS-i kõrgemal tasemel. See jaotis kirjeldab, kuidas WBS-i jälgimist projekti nõuete jaoks kasutada saab. 

Finance and Operations on projekti WBS-i jaoks kolm kuva: plaanimiskuva, panuse jälgimise kuva ja kulude jälgimise kuva.

### <a name="planning-view"></a>Plaanimiskuva

Plaanimiskuva näitab graafiku ja kulu teabe plaanitud või alusprognoosi. Kuigi projekti WBS-i versiooni ja aluse jälgimise funktsioonid puuduvad, on selle kuva väärtused mõeldud alusversiooni kajastamiseks. Selle teema jaotistes Graafiku prognoosimine ja Kulude prognoosimine kirjeldavad seda kuva ja selle kasutamist WBS-i loomisel.

### <a name="effort-tracking-view"></a>Panuse jälgimise kuva

Panuse jälgimise kuval näidatakse ülesannete edenemise jälgimist WBS-is. See võrdleb ülesande kogunenud tegeliku panuse tunde plaanitud panuse tundidega. Panuse jälgimise kuva väärtused pärinevad järgmistest valemitest.

-   Edenemise protsent = tegelik panus tänaseni ÷ ülesande plaanitud panus
-   Järelejäänud panus (teisisõnu prognoos lõpetamiseni \[ETC\]) = plaanitud panus – tegelik panus tänaseni
-   Prognoos lõpetamisel (EAC) = järelejäänud panus + tegelik panus tänaseni
-   Kavandatud panuse hälve = kavandatud panus – EAC

Panuse jälgimise kuval on ülesande panuse hälbe eeldus, mis põhineb sellel, kas EAC on suurem või väiksem kui plaanitud panus.

-   Kui EAC on suurem kui plaanitud panus, siis eeldatakse, et ülesanne võtab algselt plaanitust rohkem aega ja on graafikust maas.
-   Kui EAC on väiksem kui plaanitud panus, siis eeldatakse, et ülesanne võtab algselt plaanitust vähem aega ja on graafikust ees.

**Projektijuhi uus hinnang panuse kohta** Mõnikord on projektijuhil või muul isikul, kes projekti edenemist jälgib, vaja ülesande algseid prognoose parandada. Ülesanne võib liikuda mitmesugustel põhjustel kiiremini või aeglasemalt, kui algselt eeldatud. Näiteks võib ulatus väheneda või töötajatel olla algselt plaanitust vähem kogemusi. Eeldused on projektijuhi hinnang prognoosidele, tuginedes projekti praegusele olekule. Üldjuhul ei tohiks alusnumbreid muuta, kuna projekti alus kujutab endast projekti graafiku ja kuluprognoosi avaldatud dokumenti, millega kõik projekti sidusrühmad on nõustunud. 

On kaks viisi, kuidas projektihaldurid saavad muuta ülesannetel olevat panust.

-   Järelejäänud panuse muutmine, mis on määratud automaatselt ülesande järelejäänud panust muutma.
-   Edenemise protsendi muutmine, mis on määratud automaatselt ülesande tegelikku edenemist muutma.

Mõlemad lähenemised põhjustavad ülesande ETC, EAC ja edenemise protsendi ning ülesande eeldatava panuse hälbe ümberarvutamise. Kokkuvõtvate ülesannete EAC, ETC ja edenemise protsent arvutatakse samuti ümber ja nende eeldatavat panuse hälvet muudetakse. 

**Muudetud panus kokkuvõtvate ülesannete puhul** Saate muuta kokkuvõtvate või konteinerülesannete panust. Olenemata sellest, kas muudate neid väärtusi, kasutades kokkuvõtvate ülesannete järelejäänud panust või edenemise protsenti, toimuvad arvutused automaatselt järgmises järjekorras.

1.  Arvutatakse ülesande EAC, ETC ja edenemise protsent.
2.  Uus EAC jaotatakse alamülesannete vahel samas proportsioonis, mis algne EAC summa.
3.  Arvutatakse iga lehe sõlmülesande uus EAC.
4.  Järelejäänud panus ja edenemise protsent arvutatakse EAC uue väärtuse põhjal kõigi mõjutatud alamülesannete puhul ümber. Ümber arvutatakse ka ülesannete panuse hälve.
5.  Kokkuvõtvate ülesannete EAC arvutatakse ümber ka lehe sõlmedelt.

WBS-i jälgimise ja haldamise taseme määramiseks klõpsake panuse jälgimise kuval valikut **Tasemele laiendamine**. WBS-i avamisel panuse jälgimise kuval laiendatakse WBS automaatselt sellele tasemele.

### <a name="cost-tracking-view"></a>Kulude jälgimise kuva

Kulude jälgimise kuval näidatakse ülesande kulu tarbimise jälgimist. Sellel kuval võrreldakse ülesandele tehtud tegelikke kulutusi ülesande plaanitud kuludega. Kulu jälgimise kuva väärtused pärinevad järgmistest valemitest.

-   Tarbitud kulu protsent = tegelik kulu tänaseni ÷ ülesande plaanitud kulu
-   Kulu lõpetamiseks (CTC) = plaanitud kulu – tegelik kulu tänaseni
-   Prognoos lõpetamisel (EAC) = CTC + tegelik kulu tänaseni
-   Eeldatav omahinna hälve = plaanitud kulu – EAC

Kulu jälgimise kuval on ülesande kulu hälbe eeldus, mis põhineb sellel, kas EAC on suurem või väiksem kui plaanitud kulu.

-   Kui EAC on suurem kui plaanitud kulu, siis eeldatakse, et ülesandes kasutatakse algselt plaanitust rohkem raha ja see ületab eelarvet.
-   Kui EAC on väiksem kui plaanitud kulu, siis eeldatakse, et ülesandes kasutatakse algselt plaanitust vähem raha ja see jääb alla eelarve.

**Projektijuhi uus hinnang kulu kohta** Projektijuhid peavad kasutama CTC-d ülesande algse kuluprognoosi parandamiseks. Projektijuht saab CTC väärtust muuta, määrates selleks kulu, mis on ülesande lõpuleviimiseks vajalik. CTC väärtuse muutmisel arvutatakse ülesande CTC, EAC ja tarbitud kulu protsent ning ülesande eeldatav kulu hälve ümber. Kokkuvõtvate ülesannete EAC, ETC ja tarbitud kulu protsent arvutatakse samuti ümber ja nende eeldatavat kulu hälvet muudetakse. 

> [!NOTE] 
> Kui parandate WBS-i ülesande panust panuse jälgimise kuval, arvutatakse ülesande CTC, EAC, tarbitud kulu protsent ja eeldatav kulu hälve kulu jälgimise kuval ümber. Kuid kulu parandused ei mõjuta väärtusi panuse jälgimise kuval, kuna kulu kandetüübi alusel (tööjõud, materjal või kulu) ega projektikategooria alusel ei parandata. 

**Kulude eelduse parandamine kokkuvõtvate ülesannete puhul** Saate parandada kokkuvõtvate ülesannete kulusid ja arvutused toimuvad automaatselt järgmises järjekorras.

1.  EAC, CTC ja ülesandes tarbitud kulu protsent arvutatakse ümber.
2.  Uus EAC jaotatakse alamülesannete vahel samas proportsioonis, mis ülesannete algne EAC.
3.  Iga ülesande puhul arvutatakse uus EAC.
4.  CTS ja tarbitud kulu protsent arvutatakse mõjutatud alamülesannete puhul EAC väärtuse põhjal ümber. Ümber arvutatakse ka ülesannete kulu hälve.
5.  Kõigi kokkuvõtvate ülesannete EAC arvutatakse selle muudatuse põhjal ümber.

WBS-i jälgimise ja haldamise taseme määramiseks klõpsake kulu jälgimise kuval valikut **Tasemele laiendamine**. WBS-i avamisel kulu jälgimise kuval laiendatakse WBS sellele tasemele.

### <a name="earned-value-management"></a>Plaanitud väärtuse haldamine

Saate kasutada teenitud väärtuse meetodit (EVM) projekti edenemise jälgimiseks. Saate vaadata teenitud väärtuse mõõdikuid projektijuhi rollikeskuses. Teenitud väärtuse diagrammi komponent kuvab teenitud väärtuse ja tegeliku kulu ajafaasi väärtused. Teenitud väärtus tänase kuupäeva seisuga kuvatakse punktina. Teenitud väärtuse ajafaasi andmed pole praegu saadaval. 

Teenitud väärtuse ajafaasi diagramm kuvatakse nädalate või kuude kaupa. Selles jaotises kirjeldatakse EVM-i kolme alustala: plaanitud väärtus, teenitud väärtus ja tegelik kulu. 

**Plaanitud väärtus** EVM-i teooria väidab, et graafiku plaanitud väärtus kajastab määra, mille ulatuses projekti töörühm plaanis projekti puhul väärtust teenida. 

Finance and Operations kasutab plaanitud väärtuse kavandamisel 0:100 teenimise reeglit. Selle reegli kohaselt sisestatakse ülesande väärtus ülesandele selle lõppkuupäeva seisuga. Ühtegi väärtust ei sisestata enne, kui ülesanne on 100 protsenti lõpule viidud. 

Moodulis Projektihaldus ja raamatupidamine sisestatakse lehe sõlmede lõppkuupäev ja plaanitud kulu. Kui plaanitud väärtuse graafik kuvatakse nädalakaupa, summeeritakse plaanitud väärtus nädalakaupa kõigi lehe sõlmülesannete puhul projekti vältel. 

**Teenitud väärtus** EVM-i teooria väidab, et graafiku teenitud väärtus kajastab määra, mille ulatuses projekti töörühm tegelikult väärtust teenib. 

Finance and Operations kasutab teenitud väärtuse kavandamisel 0:100 teenimise reeglit. Selle reegli kohaselt sisestatakse ülesande väärtus ülesandele selle lõppkuupäeva seisuga. Ühtegi väärtust ei sisestata enne, kui ülesanne on 100 protsenti lõpule viidud. 

Teenitud väärtuse arvutamisel arvestatakse iga ülesande edenemise protsenti. 0:100 teenimise reegli alusel arvestatakse teenitud väärtuse arvutuses ainult antud perioodi lõpetatud ülesandeid selle perioodi lõpu seisuga. Projekti teenitud väärtus arvutatakse kõigi selle graafiku loomisel lõpetatud ülesannete kohta. 

> [!NOTE] 
> Praegu pole WBS-i jälgimise süsteemis andmestruktuure iga ülesande varasemate edenemisprotsentide talletamiseks. Seetõttu saab teenitud väärtuse kohta esitada andmeid ainult kuubi töötlemise aja seisuga. Töödelge kuupi regulaarselt rollikeskuses kuvatavate teenitud väärtuse andmete uuendamiseks. 

**Tegelik kulu** EVM-i teooria väidab, et tegeliku kulu graafik kajastab projektis raha kulutamise määra. 

Tegelik kulurea graafiku koostamiseks kasutatakse projekti sisestatud kandeid. Kulude summeeritakse kuupäeva järgi. Neid andmeid kasutatakse tegelike kulude graafiku koostamiseks teenitud väärtuse diagrammil nädalate või kuude kaupa.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Plaanitud väärtuse, teenitud väärtuse ja tegeliku kulu mõistete kasutamine

**Hälbe plaanimine** Plaanimise ajal luuakse töö prognoos ajajoonel. Seega on plaanitud väärtus projekti tööde läbiviimise kiirus projekti plaanijate hinnangu kohaselt. Projekti edenedes tehakse tööd ja projekt teenib väärtust. Võrreldes plaanitud väärtust teenitud väärtusega, saate vaadata, kuidas projekti töö edeneb. Selle võrdluse tulemust nimetatakse graafiku hälbeks. 

Kui perioodi plaanitud väärtus on suurem kui teenitud väärtus, on projektis tehtud töö hulk väiksem kui plaanitud hulk. Seetõttu on projekt graafikust maas. Kuna plaanitud ja teenitud väärtust väljendatakse rahas, antakse ka projekti viivitusajale rahaline väärtus. 

Kui perioodi plaanitud väärtus on väiksem kui teenitud väärtus, on projektis tehtud töö hulk suurem kui plaanitud hulk. Seetõttu on projekt graafikust ees. Sellele täitmisajale antakse samuti rahaline väärtus.

**Kulu hälve** Kuna teenitud väärtus kasutab kordajana omahinda, näitab teenitud väärtus projektiga tehtud töö kulu. Projekti edenemise käigus annab kandelogi ülevaate projektis tegelikult kulutatud rahast. Võrreldes teenitud väärtust tegeliku kuluga, saate vaadata kulutatava raha hulka teenitava väärtuse suhtes. Selle võrdluse tulemust nimetatakse kulu hälbeks. 

Kui perioodi tegelik kulu on suurem kui teenitud väärtus, kulutati rohkem raha, kui teeniti. Seetõttu ületab projekt eelarvet. 

Kui perioodi tegelik kulu on väiksem kui teenitud väärtus, teeniti rohkem raha, kui kulutati. Seetõttu on projekt alla eelarve.

## <a name="wbs-templates"></a>WBS mallid
Saate kasutada WBS-i mallide funktsiooni, et projektide jaoks standardseid malle luua. Kui projektides, mida teie ettevõte pakun, on palju korratavat tööd, tuleks kaaluda WBS-i malli loomist. 

Saate luua WBS-i malli olemasoleva projekti WBS-ist, et selle projekti plaanimise käigus kogutus teadmisi ja parimaid praktikaid saaks tulevikus sarnaste projektide puhul uuesti kasutada. Siiski ei pruugi mõnikord olla otstarbekas kogu WBS-i mallina salvestada. Seetõttu saate luua malle ka projekti WBS-i osadest.

### <a name="saving-a-projects-wbs-as-a-template"></a>Projekti WBS-i salvestamine mallina

Pärast malli loomist saate importida selle uue projekti WBS-i juursõlme alla või mõne uue ülesande alla projekti WBS-is.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>WBS-i malli importimine projekti WBS-i

Ülesannete importimisel korraldatakse malli ülesandeid selle ülesande alguskuupäeva alusel, mille all neid imporditakse. Importimise ajal kasutatakse malli ülesannete eelkäijatest seoseid imporditud ülesannete alguskuupäevade arvutamiseks. Imporditud ülesannete lõppkuupäevade arvutamiseks kasutatakse sihtprojekti standardset töökalendrit, et praeguse projekti töökalendris määratletud tööpäevad ja standardtööaeg säiliksid. 

Prognoosi ridadel rakendatakse kulusummasid ja müügihindu, mis tagavad projekti või projektilepingu põhistele hindadele kehtivad kuupäevad.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Projekti WBS-i ja WBS-i malli erinevused

-   WBS-i mallides olevatel ülesannetel pole algus- ja lõppkuupäeva.

WBS-i mallide puhul pole tööpäevi ja puhkepäevi määratud.

-   WBS-i mallid kasutavad alati plaanimiskalendrit, mis on seadistatud kõigi projektide jaoks vaikekalendrina.

Plaanimise vaikekalendrit kasutatakse standardtööpäeva tundide leidmiseks.

-   Eelkäijatest seoseid ei kopeerita WBS-i mallile.

Kuna WBS-i mallidel pole kuupäevi, pole eelkäija lõppkuupäeval põhinev alguskuupäeva loogika vajalik.

-   WBS-i mallis ülesande loomisel luuakse automaatselt tööjõukulu prognoosi rida. Müügihind ja kulusumma kopeeritakse valitud töötajalt.

Kulu ja kauba maksumuse saab luua käsitsi, samamoodi nagu projekti WBS-i puhul.

-   Plaanimistõrked kuvatakse kõrvalekallete korral järgmisest valemist.

Panus = ressursside arv × kestus × standardse tööpäeva tundide arv 

Saate parandada kõik plaanimisvead üheaegselt, klõpsates valikut **Paranda kõik plaanimisvead**. 

Teine võimalus plaanimisvigade parandamiseks on parandada need eraldi, klõpsates iga ülesande puhul hoiatusikooni.




