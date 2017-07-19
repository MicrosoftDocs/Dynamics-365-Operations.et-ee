---
title: "Tellimuse vaikesätted dimensioonide ja tootevariantide puhul"
description: "Tellimuse vaikesätted määratlevad tegevuskoha ja lao, kust kaupu hangitakse või hoitakse, miinimum-, maksimum-, mitmik- ja standardkogused, mida kasutatakse kaubanduse või varude halduse jaoks, täitmisajad, peatamislipu ja tellimuse lubamise meetodi."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventItemOrderSetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations, Retail
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: b4e8ff363a98f8dfc90af0133807373566531568
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017

---

# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Dimensioonide ja tootevariantide tellimuse vaikesätted

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Tellimuse vaikesätted Microsoft Dynamics 365 for Finance and Operations, Enterpise editionis määratlevad tegevuskoha ja lao, kust kaupu hangitakse või hoitakse, miinimum-, maksimum-, mitmik- ja standardkogused, mida kasutatakse kaubanduse või varude halduse jaoks, täitmisajad, peatamislipu ja tellimuse lubamise meetodi. Tellimuse vaikesätteid kasutatakse ostutellimuste, müügitellimuste, üleviimistellimuste, laotöölehtede loomisel ja plaanitud tellimuste loomiseks koondplaanimisega. Tellimuse vaikesätted võivad olla kaubaspetsiifilised, tegevuskohaspetsiifilised, tootevariandispetsiifilised ja või tootedimensiooni-spetsiifilised.

Lehel **Tellimuse vaikesätted** saate määratleda tellimuse vaikesätted. Selle lehe avamiseks minge jaotisse **Tooteteabe haldus** &gt; **Tooted** &gt; **Väljastatud tooted** &gt; valige väljastatud toode &gt; toimingupaanil **Plaan** või ****Varude haldamine**** &gt; **Tellimuse sätted** &gt; **Tellimuse vaikesätted**.

## <a name="default-order-settings"></a>Tellimuse vaikesätted
Ostudele, müügile ja varudele on kolme tüüpi tellimuse vaikesätteid. Ostude tellimuse vaikesätteid kasutatakse, kui luuakse:

-   Ostutellimuse read
-   Ostulepingu read
-   Pakkumiskutse read
-   Ostutaotluse read
-   Saadetise täiendamise read
-   Plaanitud ostutellimused

Müügi tellimuse vaikesätteid kasutatakse, kui luuakse:

-   Müügitellimuse read
-   Müügilepingu read
-   Müügipakkumise read
-   Tagastustellimuse read ja kaubaasenduse read
-   Nõudluse prognoosi read

Vaikimisi müügitellimuse sätted rakenduvad ka siis, kui luuakse:

-   Projekti kaubanõuded
-   Teenuse tellimuse kaubanõuded

Varude tellimuse vaikesätteid kasutatakse, kui luuakse:

-   Laotöölehed
-   Üleviimistellimused
-   Plaanitud üleviimistellimused

Varude tellimuse vaikesätted rakenduvad ka siis, kui luuakse:

-   Vahelaoorderid
-   Kvaliteettellimused
-   Tootmistellimused
-   Koosluseread
-   Plaanitud tootmistellimused

## <a name="full-definition-of-a-released-product"></a>Väljastatud toote täielik määratlus
Kande loomisel peate määrama väljastatud toote täieliku määratluse real enne, kui Finance and Operations proovib tuvastada tellimuse vaikesätted. Väljastatud toote täielik määratlus tähendab, et kauba number ja kõik aktiivsed toote dimensioonid, nagu konfiguratsioon, suurus, laad ja värv, on määratud kandel. Näiteks kui loote käsitsi väljastatud tootevariandile ostutellimuse rea, peate määrama kõik vajalikud toote dimensioonid enne, kui tegevuskoha, lao, koguste ja täitmisaeg kuvatakse vaikimisi tellimusreal. 

Mitte kõiki tellimuse vaikesätete parameetreid ei rakendata tellimuse või töölehe ridade loomisel. Kogused ja täitmisajad kuvatakse vaikimisi ainult vastavalt vajadusele. Näiteks töölehe rea loendamisel kuvatakse rea loomisel vaikimisi ainult tegevuskoht ja ladu. Ilmselgelt ei tehta rea loomisel või töölehe sisestamisel kordsetele või miinimumidele koguse vaikeolekusse seadmist ega kontrolle. 

Süsteem püüab tellimuse ja töölehe rea loomisel leida alati vaikimisi tegevuskohta ja ladu. Tegevuskohta ei kuvata alati vaikimisi tellimuse sätetest. Näiteks müügitellimuse või ostutellimuse loomisel kasutatakse tellimuse päise tegevuskohta automaatselt tellimuse ridadel. Koosluse rea loomisel kasutatakse koosluse päise tegevuskohta. Pärast tegevuskoha määramist kasutatakse seda, et leida mis tahes spetsiifilisi tellimuse sätteid, mida saab seejärel lao jaoks vaikimisi kasutada. 

Lehel **Kauba laovarud** saab tellimuse vaiketüübi, ostu ja varude täitmisajad alistada kauba laovaru reeglitega. Kuigi tellimuse vaikesätted ei luba eristamist toote ja ülekande täitmisaja vahel, siis kauba laovaru reeglid lubavad seda. Siiski kasutatakse kauba laovarude seadistust ainult MRP-ga plaanitud tootmise ja plaanitud üleviimistellimuse loomisel ja see ei rakendu tootmis- ja üleviimistellimuste käsitsi loomisel. 

## <a name="default-order-settings-rules"></a>Tellimuse vaikesätete reeglid
Saate määratleda üldised tellimuse vaikesätted ja mis tahes arvu tellimuse vaikesätete reegleid, mis rakenduvad ainult teatud tingimustele, nagu tegevuskoht või spetsiifiline toote dimensioon või toote dimensioonide kombinatsioon. Te ei saa määratleda laospetsiifilisi tellimuse sätteid.

### <a name="rank-in-default-order-settings"></a>Tellimuse vaikesätete hierarhia

Tellimuse vaikesätetel on hierarhia. Mida kõrgemal hierarhias reegel paikneb, seda olulisem reegel on, mis tähendab, et sellel on kõrgem prioriteetsus ja seda saab kasutada enne hierarhias madalatel positsioonidel olevaid reegleid. Üldistel tellimuse vaikesätetel on nullpositsioon, mida ei saa muuta. Ainult üks reegel saab olla nullpositsiooniga. Reeglitel võib hierarhias olla sama positsioon, tingimusel, et dimensioonid, millele need rakenduvad, on erinevad. See on kasulik tegevuskoha spetsiifiliste tellimuse sätete modelleerimiseks. Uue tellimuse vaikesätete reegli loomisel tellimuse väärtuste väärtused, peatamislipp, jne päritakse nullpositsiooniga reeglist, kuid selle saab alistada.

### <a name="default-order-settings-for-released-products"></a>Väljastatud toodete tellimuse vaikesätted

Eristuvate väljastatud toodete puhul saate määratleda üldised tellimuse sätted või tegevuskoha spetsiifilised tellimuse sätted. Üldistel tellimuse sätetel on alati nullpositsioon. Kui seadistate uued müügi, ostu ja varude tellimuse sätted samaaegselt koos, soovitame teil kasutada vaadet **Üksikasjade vaade** lehel **Tellimuse vaikesätted**. Üksikasjade vaatele lülitamiseks valige toimingupaan **Suvandid** &gt; **Lehe suvandid** &gt; **Muuda vaadet** &gt; **Üksikasjade vaade**.

### <a name="site-specific-order-settings"></a>Tegevuskohaspetsiifilised tellimuse sätted

Tegevuskoha spetsiifiliste tellimuse sätete loomiseks klõpsake valikut **Uus**. Vaates **Üksikasjade vaade** täitke tegevuskoht väljal **Kohalduvad sätted** &gt; **Tegevuskoht**. Vaates **Ruudustikuvaade** täitke tegevuskoht veerus **Tegevuskoht**. Uus reegel saab hierarhias automaatselt uue positsiooni väärtuse, mis on kõrgem kui null. Saate luua nii palju tegevuskohaspetsiifilisi reegleid kui vaja ja saate määrata kõik tegevuskohaspetsiifilised reeglid hierarhias samale positsioonile näitamaks, et need on võrdselt olulised. 

Kui asute vaates **Üksikasjade vaade** saate ülevaate kauba jaoks loodud reeglitest. Lülitage nuppu **Kuva/peida loend**, et näha ülevaate teavet. Kui mis tahes tüübi tellimuse rida luuakse ja sellele pole ühtki tegevuskohta antud, otsib Finance and Operations reeglit, millele pole tegevuskohta määratud. See võib aidata määrata tellimuse real vaiketegevuskoha. Seda tegevuskohta kasutatakse seejärel tegevuskohaspetsiifilise reegli otsimiseks, kus võib olla seatud vaikimisi ladu. See ladu rakendatakse tellimuse reale.

### <a name="specific-order-settings-for-product-dimension"></a>Tootedimensiooni spetsiifilised tellimused sätted

Saate määratleda tellimuse sätete reeglid mis tahes aktiivsele toote dimensioonile või aktiivsete tootedimensioonide kombinatsioonile. Kui tootedimensiooni väli jäetakse tühjaks, siis rakendub see reegel kõigile tootedimensiooni väärtustele. 

Arvestage järgmist näidistoodet.

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Toote nimi**                                    | Fotoelektriline andur                    |
| **Kaubakood**                                     | XW56                                    |
| **Konfiguratsioon** (kasutatakse valguse tüübi modelleerimiseks) | C1-nähtav punane tuli, C2 infrapunavalgus |
| **Laad** (kasutatakse konstrueerimise revisjoni modelleerimiseks)  | R1, R2, R3                              |

Selles näites eeldage, et toode on soetatud ja mitte toodetud. Samuti eeldage, et konfiguratsiooni C1 kasutatakse rohkem üldisemalt, seega on sellel lühemad täitmisajad. 

Looge selle stsenaariumi modelleerimiseks järgmised tellimuse vaikesätted.

| Reiting | Sait | Konfiguratsioon | Laad | Ost – vaikesätete alistamine | Ostu täitmisaeg | Ost – peatatud | Müük – vaikesätete alistamine | Müük – peatatud |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Jah                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Kui XW56, konfiguratsiooni C1 jaoks luuakse ostutellimuse rida või plaanitud ostutellimus, siis loetakse täitmisajaks 2 hoolimata revisjonist või tegevuskohast, kuhu rida on paigutatud. Eeldage, et kõik revisjonid peale R3 on peatatud.

Saate luua järgmised tellimuse vaikesätete reeglid.

| Reiting | Sait | Konfiguratsioon | Laad | Ost – vaikesätete alistamine | Ostu täitmisaeg | Ost – peatatud | Müük – vaikesätete alistamine | Müük – peatatud |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | R2    | Jah                                  |                    | Jah                | Jah                               | Jah             |
| 20   |      |               | R1    | Jah                                  |                    | Jah                | Jah                               | Jah             |
| 10   |      | C1            |       | Jah                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Kahel reeglil vanade revisjonide peatamiseks on hierarhias sama positsioon, mis tähendab, et need on võrdselt olulised. Neil mõlemal on kõrgem positsioon kui konfiguratsiooni C1 reeglil, mis tähendab, et need on konfiguratsiooni C1 reegli suhtes ülimuslikud. 

See näide selgitab positsiooni vajadust. Kui konfiguratsiooni C1 ja revisjoni R2 jaoks luuakse ostutellimus, siis hierarhia positsiooni puudumisel oleks kaks R2 ja C1 jaoks määratletud reeglit ebamäärased. Ebamäärasuse lahendamiseks otsib Finance and Operations reegleid läbi positsioonide laskuvas järjestuses ja rakendab esimese kohaldatava reegli. Praeguses näites, kui ostutellimuse rida luuakse konfiguratsiooni C1 ja revisjoni R2 jaoks, siis saab kasutaja hoiatusteate, et kaup on ootel ja et seda põhjustab revisjoni väärtus. Kui konfiguratsiooni reeglil oli kõrgem positsioon kui revisjoni reeglil, siis oleks ostutellimuse rea loomine konfiguratsiooni C1 ja revisjoni R2 jaoks olnud edukas ja kasutajale ei oleks kuvatud teadet „kaup ootel”. 

Arvestage järgmiseid tellimuse vaikesätte reegleid.

| Reiting | Sait | Konfiguratsioon | Laad | Vaiketegevuskoht | Vaikeladu | Ost – laoala vaikedimensioonide alistamine | Ostuladu |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Jah                                            | 22                 |
| 10   |      | C1            |  R2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Süsteem läbib reeglite kogumit tegevuskoha ja lao määramiseks kaks korda. Kui konfiguratsiooni C1, laadi R2 jaoks luuakse ostutellimuse rida, siis määratakse tegevuskoht positsiooniga 10 reegli põhjal. Seejärel otsib süsteem lao määramiseks reeglit tegevuskoha 2 jaoks. Leitakse reegel 20 ja kuna sellel on kõrgem positsioon, siis on ostutellimuse real olev ladu 22 ja mitte 21. 

Üldiste juhistena saavad spetsiifilised reeglid ja dimensioonide reeglid, mis on olulisemad kui teised dimensioonid, kõrgemaid positsioone, samas kui üldised reeglid saavad madalamaid positsioone. 

Nullpositsiooniga reegel täidab turvavõrgu rolli. Kui ühtki teist reeglit ei tabata, siis kasutatakse tellimuse vaikesätteid nullpositsioonist. 

Kuna hierarhia positsiooni number on nii oluline, on tegumiribal **Tellimuse vaikesätted** funktsioonid reegli üles ja alla liigutamiseks ning reeglite ümber nummerdamiseks, et need on alati juurdekasvuga 10. 

Väljastatud toote jaoks loodud reeglite arv võib olla hulgaline. Saamaks paremat aimu sellest, mida iga reegel alistab ja miks see on vajalik, soovitame kasutada vaadet **Ruudustikuvaade** lehel **Tellimuse vaikesätted**. Saate lubada ruudustikuvaate, valides toimingupaani **Suvandid** &gt; **Lehe suvandid** &gt; **Muuda vaadet** &gt; **Ruudustikuvaade**. Ruudustikus kuvatud veergude arv võib olla üsna märkimisväärne, eriti müügi ja varude vahekaartide puhul Ruudustikus näidatud veergude arvu piiramiseks saab veergude gruppe peita või kuvada, kasutades menüü **Tellimuse vaikesätted** &gt; **Veeru kuvamine** nuppe.

### <a name="specific-order-settings-for-released-product-variant"></a>Väljastatud tootevariandi spetsiifilised tellimuse sätted

Kui tellimuse vaikesätete reeglite süsteem on liiga raskepärane, siis on võimalik lihtsalt määratleda iga tootevariandi jaoks tellimuse vaikesätted. Järgmised näited näitavad, kuidas see toote ja eespool toodud juhtumite puhul välja näeb.

| Reiting | Sait | Konfiguratsioon | Laad | Ost – vaikesätete alistamine | Ostu täitmisaeg | Ost – peatatud | Müük – vaikesätete alistamine | Müük – peatatud |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | R3    | Jah                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | R2    | Jah                                  | 5                  | Jah                | Jah                               | Jah             |
| 10   |      | C2            | R1    | Jah                                  | 5                  | Jah                | Jah                               | Jah             |
| 10   |      | C1            | R3    | Jah                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | R2    | Jah                                  | 2                  | Jah                | Jah                               | Jah             |
| 10   |      | C1            | R1    | Jah                                  | 2                  | Jah                | Jah                               | Jah             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Sellisel juhul ei ole positsioon tegelikult tähtis, seega saate valida selle peitmise. See lahendus tekitab hoolduse probleemi. Siiski võikiste kaaluda selle seadistuse kasutamist, kui kaalute integreerimist toote töötsükli halduse (PLM) süsteemidega.




