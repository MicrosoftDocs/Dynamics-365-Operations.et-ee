---
title: Eelarve plaanimise täiendamine
description: Selles teemas selgitatakse, mida tuleb ümber konfigureerida, ja kirjeldatakse ka uusi funktsioone, mida tuleb pärast täiendamise lõpulejõudmist arvesse võtta.
author: panolte
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 272923
ms.assetid: 17cdfe74-bdfd-466a-9bdd-c12583f250c7
ms.search.region: Global
ms.author: panolte
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 86c4d83d35c7ca6bd5fe3a9f6c09e0457b40c523
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565060"
---
# <a name="upgrade-budget-planning"></a>Eelarve plaanimise täiendamine

[!include [banner](../includes/banner.md)]

Eelarve planeerimine on rakendustes Microsoft Dynamics AX 2012 ja Dynamics 365 Finance suuresti erinev. Mõnd funktsiooni pole täiendatud ja seetõttu nõuavad need ümberkonfigureerimist. Selles teemas selgitatakse, mida tuleb ümber konfigureerida, ja kirjeldatakse ka uusi funktsioone, mida tuleb pärast täiendamise lõpulejõudmist arvesse võtta.  

Eelarve plaanimisel rakenduses on palju täiustusi, mis ei olnud rakenduses Dynamics AX 2012 saadaval. Selles teemas selgitatakse muudatusi, mida täiendust tegevad kliendid peavad rakendama. Samuti tuuakse välja uued funktsioonid, mida tuleb täiendusprotsessis arvesse võtta. Muudatuste rohkuse tõttu ei saa ühtki olemasolevat eelarveplaani avada, enne kui selles teemas kirjeldatud muudatused on tehtud. Siiski peavad aruanded tööd jätkama ega nõua lisamuudatusi.

## <a name="overview-of-changes"></a>Muudatuste ülevaade
Finance and Operationsi moodulis Eelarvestus on tehtud palju olulisi muudatusi. Need muudatused hõlbustavad eelarve plaanimise konfigureerimist ja korduskasutamist, et vähendada iga-aastast hooldamist ja seadistamist. Finance ei sisalda enam järgmisi AX 2012 valdkondi.

-   Eelarveplaani mallid (eelarve plaanimise konfigureerimine)
-   Eelarveplaani kaustad (eelarve plaanimise konfigureerimine)
-   Stsenaariumipiirangud (eelarve plaanimise konfigureerimine)
-   Mallid eelarve plaanimise etapireeglite ja mallide jaoks (eelarve plaanimise protsess)
-   Töölehe mallide maatriksi väljad
-   Eelarveplaani Microsoft Exceli malli viisard

Mõnd uut põhimõtet ei saa eelmisest funktsionaalsusest otse täiendada. Seetõttu peate nende uute põhimõtete rakendamiseks tegema teatud ümberkonfigureerimised. Järgmistes jaotistes kirjeldatakse põhimõteid, mis asendavad üksusi eelnevas loendis.

### <a name="columns"></a>Veerud

Veerud on uus põhimõte, mis asendab Exceli malli osi ja ka maatriksivälju. Veerud võivad kujutada perioodi, kuud, kvartalit, aastat või kogu aega. Ajaviide on dünaamiline. See osutab eelarveprotsessile viitamisel suhtelisele perioodile või aastale. Näiteks veerg **Eelmise aasta jaanuar** viitab aasta –1 rahandusperioodile 1. Veerg on kohane eelarveplaani stsenaariumile, nagu tegelikud näitajad või eelarvetaotlus.

### <a name="layouts"></a>Paigutused

Paigutused on uus põhimõte, mis asendab Exceli malli. Paigutused sisaldavad veerge, mis määratlevad, milliseid eelarve või tegelike näitajate andmeid ja perioode tuleb kuvada. Paigutusi kasutavad klientrakendus ja Exceli lisandmoodul ka ühiselt. Seetõttu on kasutajakogemus Finance and Operationsi klientrakenduses andmete sisestamisel või vaatamisel parem kui kasutajakogemus AX 2012-s. Andmete sisestamiseks Finance’i klientrakenduses pole teil enam kandevaates piirangut vaadata ja sisestada ainult üht stsenaariumit. Selle asemel võimaldab võrdlusvaade hõlpsasti vaadata ja sisestada samal ajal mitme perioodi ning konto summasid. Paigutsi saab ka määratleda nii, et saate sisestada ja vaadata valuutat, kommentaare ning muid valikulisi andmeid. Paigutused võimaldavad ka määratleda, milliseid pearaamatu dimensioone ja dimensioonikirjeldusi tuleb kuvada. Ühtlasi sisaldavad paigutused stsenaariumipiiranguid määratlemaks, milliseid malli veerge saab redigeerida ja millised veerud peavad Excelis saadaval olema. Pärast paigutuse määratlemist luuakse selle jaoks mall. See mall omakorda loob vastava Exceli malli. Seejärel saate Exceli malli redigeerida, et kaasata rohkem valemeid ja vorminguid, ning seejärel selle uuesti üles laadida. Pärast seda määratakse paigutused lehel **Eelarve plaanimise protsess** igale etapireeglile. Seega asendavad paigutused malle, mida määrati ja kasutati samal moel.

### <a name="budget-planning-processes"></a>Eelarve planeerimise protsessid

Eelarve plaanimise protsessid on üldjoontes samad mis AX 2012-s. Olulisim muudatus on mallide asendamine paigutustega. Kui AX 2012-s viidi mis tahes protsessid lõpule, seatakse nende olekuks nüüd Pooleli, et oleks võimalik teha muudatusi, Peate määrama iga etapireegli jaoks vajalikud paigutused, et määrata, millised stsenaariumid ja ajaperioodid kuvatakse, kui plaan klientrakenduses avatakse. Paigutused määravad ka selle, milline Exceli mall avatakse väljaspool Dynamic 365 Finance’i, et saaksite eelarvet vaadata. **Konto vaikestruktuur** on eelarve planeerimise protsessi uus kohustuslik väli. Iga eelarve planeerimise protsessi puhul saate määrata eelarvestamisel kasutatava esmase kontostruktuuri.

### <a name="attachments"></a>Manused

AX 2012-s salvestati põhjendusdokumendid manuse kausta. Eelmisi põhjendusdokumente ei täiendata. Põhjendusdokumente talletatakse nüüd andmebaasis. Kui see teave tuleb täiendatud versioonis salvestada, saate iga plaani puhul lõplikud põhjendusdokumendid manusena üles laadida toimingupaani nupuga **Põhjendus**. AX 2012-s loodi Exceli töölehed iga eelarveplaani kohta malli põhjal. Finance’is avavad kõik plaanid paigutuse koopia. Exceli faili muudatusi siiski ei salvestata. Kõik valemid või toetav teave, mida kasutatakse iga plaani alusel eraldi, tuleb lisada kommentaaride, põhjendusdokumendi või mõne muu lisaprotsessi kaudu.

## <a name="configuring-an-upgraded-environment-from-ax-2012"></a>AX 2012-st täiendatud keskkonna konfigureerimine
Järgmine näide aitab teil määrata, kuidas täiendatud süsteemi konfigureerida, kasutades täiendatud eelarve protsessi AX 2012 demoandmete põhjal. Loodi veergude vaikekonfiguratsiooni andmed täiendamisprotsessi abistamiseks. Saate neid vaikeandmeid värskendada või kustutada, kui need ei vasta teie konfigureerimisnõuetele. **Märkus.** Siin on uued kohustuslikud väljad, mida süsteemis ei seadistata. Kui te ei pääse mõnelt lehelt, näiteks **Eelarve plaanimise konfiguratsioon**, edasi ega saa mujale navigeerida, võite brauseri sulgeda ja seejärel selle uuesti avada teisel lehel, et sisestada üksikasjad õiges järjekorras. Siin on kohustuslikud väljad, mis ei ole veel seadistatud. Seetõttu võib esineda probleeme, kuni kõik on konfigureeritud ja kõik kohustuslikud väljad seadistatud. Selles teemas selgitatakse, kuidas neid välju vastavalt vajadusele seadistada. Nõutud väljad on muu hulgas järgmised.

-   Leht **Eelarve planeerimise protsess**: väli **Konto vaikestruktuur**
-   Leht **Eelarve planeerimise protsess**: väli **Paigutus** kiirkaardil **Eelarve planeerimise etapireeglid ja paigutused**

### <a name="define-columns-and-layouts"></a>Veergude ja paigutuste määratlemine

1. Klõpsake lehel **Eelarve plaanimise konfiguratsioon** vahekaarti **Veerud**. Täienduse osana luuakse uued veerud automaatselt teie eelarveplaani ridade põhjal. Veerud kasutavad nüüd dünaamilisi kuupäevi, kus aeg ja aasta on nihkes rahandusaasta suhtes, mis on määratletud eelarve plaanimise protsessis. **Märkus.** Täiendamisel jõudluse tagamiseks eeldatakse, et kõik eelarvetsüklid tähistavad kalendriaastaid, mitte rahandusaastaid. Rahandusaastate kasutamisel tuleb teil teha muudatusi veergude rahandusaastaga õigesti vastendamiseks. Näiteks olid AX 2012-s järgmised elemendid.
   -   Eelarveplaani stsenaariumid: Tegelikud näitajad, Algväärtus, Eelarvetaotlus, Kinnitatud eelarve
   -   Eelarveplaani read kõigile stsenaariumitele 2017. aastal ja tegelikud näitajad nii 2017. kui ka 2016. aastal

   Finance and Operationsis luuakse järgmised veerud.

   | Veeru nimi    | Eelarveplaani stsenaarium | Veeru ajaperiood | Aasta nihe |
   |----------------|----------------------|--------------------|-------------|
   | Jaanuaristsenaarium 1 | Tegelikud              | 1                  | 0           |
   | Jaanuaristsenaarium 2 | Alus             | 1                  | 0           |
   | Jaanuaristsenaarium 3 | Eelarvenõue       | 1                  | 0           |
   | Jaanuaristsenaarium 4 | Kinnitatud eelarve      | 1                  | 0           |
   | Jaanuaristsenaarium 5 | Tegelikud              | 1                  | –1          |
   | Veebruarinõue 1 | Tegelikud              | 1                  | 0           |
   | ...            | ...                  | ...                | ...         |

   Selles näites luuakse veerg nimega **Jaanuaristsenaarium 1** viimaste eelarveplaani kandeandmete kohta, mis leitakse, kui jaanuaris on kandeid. Sarnane veerg luuakse iga andmetega stsenaariumi kohta. Kui selle aasta kõigi perioodide kohta on veerud olemas, luuakse veerud eelmiste aastate kohta.
2. Saate veergude nimesid ja kirjeldusi ning muid üksikasju muuta kas käsitsi klientrakenduses või hulgivärskendustega Exceli lisandmooduli kaudu, mis osutab eelarveplaani veergude andmeüksusele. Kõik eelnevalt maatriksiväljadele seatud filtrid seatakse nüüd veergudes.
3. Looge uus eelarveplaani paigutus. Paigutus osutab mitmele veerule, et määratleda Excelis ja klientrakenduses kuvatav vaade. Esmalt nõuab paigutus, et määraksite pearaamatu dimensioonikogumi määramaks, milliseid finantsdimensioonide saab sisestada. Pärast dimensioonikogumi määramist klõpsake valikut **Kirjeldused**, et valida paigutusse kaasatavad dimensioonide kirjeldused.
4. Klõpsake kiirkaardil **Paigutuse elemendid** nuppu **Lisa**, et lisada igale reale metaandmed, nagu valuuta, kommentaar või eelarveklass, mis määrab tulu- ja kuluridade seose. Seejärel lisage veerud ajaperioodi jaoks ning selle eelarve tsüklile ja etaiple rakenduvad stsenaariumid. Saate neid muudatusi teha käsitsi klientrakenduses või Exceli lisandmooduli kaudu, mis osutab eelarveplaani paigutuse elementide andmeüksusele.
5. Valige iga paigutuselemendi puhul, kas veerg peab olema redigeeritav ja kas see tuleb kuvada ka selle paigutuse Exceli töövihikus. **Märkus.** Ajalooliste plaanide puhul soovite võib-olla arvesse võtta paigutust, mis kuvab 12 kuuveergu selle protsessi mis tahes eelarveplaani stsenaariumite puhul.

### <a name="update-budget-planning-processes-to-use-the-appropriate-layout-for-each-budget-stage"></a>Eelarve plaanimise protsesside värskendamine iga eelarveetapi jaoks sobiva paigutuse kasutamiseks

1.  Valige lehel **Eelarve plaanimise protsess** konfigureeritav protsess.
2.  Klõpsake toimingupaanil käsku **Redigeeri**.
3.  Määrake selle eelarveprotsessi jaoks konto vaikestruktuur. **Konto vaikestruktuur** on uus kohustuslik väli, mis peab olema määratud.
4.  Valige kiirkaardi **Eelarve plaanimise etapireeglid ja paigutused** väljal **Paigutus** eelnevalt konfigureeritud ja sellele etapile sobiv paigutus.
5.  Jätkake sama või teiste paigutuste valimisega erinevatele eelarve plaanimise etappidele ja seejärel salvestage muudatused.

## <a name="additional-features-to-consider-in-your-budgeting-process"></a>Lisafunktsioonid, mida eelarvestamise protsessis arvesse võtta
### <a name="budget-planning-workspace"></a>Eelarve plaanimise tööruum

See tööruum on mõeldud nii eelarve omanikule kui ka üksikutele eelarve kaastöötajatele. See sisaldab linke kõigile eelarvedokumentidele, mis vajavad teie tähelepanu. Samuti sisaldab see aruandeid ja tulemuslikkuse võtmenäitajaid (KPI) eelarveprotsessi jaoks. Eelarve administraator saab määratleda praeguse eelarve plaanimise protsessi kõigi kasutajate jaoks lehel **Eelarvestamise parameetrid**. Vahekaardi **Tööruumi sätted** kiirkaardil **Eelarve plaanimine** on väli, kus saate valida eelarve plaanimise protsessi.

### <a name="alternate-layouts"></a>Alternatiivsed paigutused

Alternatiivsed paigutused on uus funktsioon, mis võimaldab vaadata plaane erinevates paigutustes. Valikutena saab pakkuda ühe või mitu paigutust. Seejärel saate vaadata eelarveplaani kuupaigutuses või kvartalipaigutuses. Saate määratleda alternatiivsed paigutused lehe **Eelarve plaanimise protsess** kiirkaardil **Eelarve planeerimise etapireeglid ja paigutused**.

### <a name="budget-milestones"></a>Eelarve vahe-eesmärgid

Eelarveprotsessi osana on oluline, et mõistaksite peamisi kuupäevi ja tähtaegu. Nüüd saate kuupäevi konfigureerida nii, et neil on ka kirjeldused. Eelarvestamise kasutajad näevad neid kirjeldusi siis, kui avavad eelarved, et redigeerida või vaadata neile määratud üksusi.

### <a name="copy-from-budget-plan-allocation"></a>Koopia eelarve plaanimise eraldamisest

Uue eraldamismeetodi abil saate jaotada ülemplaanist alamplaanile ilma hierarhia vahetasandeid läbimata. See meetod on eriti kasulik klientidele, kes lõid varem finantsdimensiooni üksnes eelarve jaotuseks ja kinnitusteks.

### <a name="generating-budget-plans-from-new-budget-sources"></a>Eelarveplaani loomine uute eelarveallikate põhjal

Järgmised valikud on lisatud perioodiliste protsessidena. Nende valikute abil saate luua eelarveplaani, kasutades lähtepunktina olemasolevaid andmeid teisest moodulist.

-   Eelarveplaani loomine nõudluse prognoosist
-   Eelarveplaani loomine tarneprognoosist
-   Eelarveplaani loomine projektist
-   Eelarveplaani loomine eelarve registrist

### <a name="more-complete-tracking-of-amounts"></a>Summade põhjalikum jälgimine

AX 2012-s talletati eelarve planeerimisel iga väärtuse kohta üks plaani summa. Finance’is on andmemudelit laiendatud. Nüüd on iga valuuta jaoks saadaval arvestusvaluuta, kandevaluuta ja aruandlusvaluuta summad. Täiendamise ajal täidetakse need uued veerud olemasolevate andmete puhul automaatselt.

### <a name="do-not-convert-currency-in-aggregation"></a>Ära teisenda kogumis olevat valuutat

Tavaliselt kui alamplaan liidetakse ülemtasemega, teisendatakse summad automaatselt kandevaluutast organisatsiooni arvestusvaluutasse. Kui seate valiku **Ära teisenda valuutat liitmisel** sätteks **Ei**, jäävad liidetud summad algsesse valuutasse. Seetõttu võimaldab see valik täpsemaid korrigeerimisi, mida mõjutavad vahetuskursi kõikumised.

### <a name="looking-back-from-a-budget-plan-to-other-modules-that-contributed-to-the-budget"></a>Tagasivaade eelarveplaanilt teistele moodulitele, mis on eelarvesse panustanud

Eelarveplaane saab luua nõudluse või tarneprognoosist, projektist ja muudest aladest. Päring Eelarveplaanid dimensioonikogumi järgi hõlmab mitut suvandit, mis võimaldavad teil päringu käivitada tuvastamaks eelarveplaani allikaks olevaid andmeid.

### <a name="overwrite-or-append-to-plan-for-allocation-schedules"></a>Plaani ülekirjutamine või plaanile lisamine eraldamisgraafikute jaoks

Kui jaotatavate summade allikaid on mitu, saate määrata, et summad peavad olema täiendavad. Sellisel juhul ei kirjuta summad olemasolevaid summasid üle. Selle asemel lisatakse need olemasolevatele summadele.

### <a name="default-financial-dimension-set-for-budget-planning-configuration"></a>Finantsdimensioonide vaikekogum eelarve plaanimise konfiguratsioonile

Lehel **Eelarve plaanimise konfiguratsioon** on nüüd väli, kus saate määrata finantsdimensioonide vaikekogumi. Ehkki see väli on valikuline, võib see olla teatud päringute puhul vajalik. See võib olla nõutav ka siis, kui soovite aruandegruppe dimensoonikogumi alusel grupeerida või filtreerida.

### <a name="data-entities"></a>Andmeüksused

Lisatud on mitu andmeüksust, et võimaldada eelarve plaanimist kiiresti rakendada. Üksused võimaldavad teha ka Exceli kaudu palju muudatusi. Seetõttu ei pea te looma üksusi klientrakenduse kaudu ükshaaval. Uute andmeüksuste loend on järgmine.

-   Üksuse nimi
-   Eelarve parameetrid
-   Eelarveplaani parameeter
-   Eelarveplaani stsenaariumid
-   Eelarveplaani etapid
-   Eelarveplaani töövoo etapp
-   Eelarveplaani eraldamisgraafikud
-   Eelarveplaani etapi eraldamised
-   Eelarveplaani prioriteedid
-   Eelarveplaani veerud
-   Eelarveplaani paigutuse elemendid






[!INCLUDE[footer-include](../../../includes/footer-banner.md)]