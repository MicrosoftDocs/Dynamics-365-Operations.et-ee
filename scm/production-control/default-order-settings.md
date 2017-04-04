---
title: "Vaikimisi tellimuse telefoni mõõtmed ja toote variantide puhul"
description: "Tellimuse vaikesätted määratlevad tegevuskoha ja lao, kust kaupu hangitakse või hoitakse, miinimum-, maksimum-, mitmik- ja standardkogused, mida kasutatakse kaubanduse või varude halduse jaoks, täitmisajad, peatamislipu ja tellimuse lubamise meetodi. Tellimuse vaikesätteid kasutatakse ostutellimuste, müügitellimuste, üleviimistellimuste, laotöölehtede loomisel ja plaanitud tellimuste loomiseks koondplaanimisega. Tellimuse vaikesätted võivad olla kaubaspetsiifilised, tegevuskohaspetsiifilised, tootevariandispetsiifilised ja või tootedimensiooni-spetsiifilised."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventItemOrderSetup
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 60abaa69debd891b2fe2dd98184c0dab50b0bf9f
ms.lasthandoff: 03/29/2017


---

# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Vaikimisi tellimuse telefoni mõõtmed ja toote variantide puhul

Tellimuse vaikesätted määratlevad tegevuskoha ja lao, kust kaupu hangitakse või hoitakse, miinimum-, maksimum-, mitmik- ja standardkogused, mida kasutatakse kaubanduse või varude halduse jaoks, täitmisajad, peatamislipu ja tellimuse lubamise meetodi. Tellimuse vaikesätteid kasutatakse ostutellimuste, müügitellimuste, üleviimistellimuste, laotöölehtede loomisel ja plaanitud tellimuste loomiseks koondplaanimisega. Tellimuse vaikesätted võivad olla kaubaspetsiifilised, tegevuskohaspetsiifilised, tootevariandispetsiifilised ja või tootedimensiooni-spetsiifilised.

Lehel **Tellimuse vaikesätted** saate määratleda tellimuse vaikesätted. Selle lehe avamiseks Mine **toote teabekorraldus**&gt;**toodete**&gt;**vabastatud toodete**&gt; välja antud toodet &gt;kohta on **planeerida** või *** hallata varude *** Updatehagi paani &gt;**Telli seaded**&gt;**vaikimisi tellimuse telefoni**.

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
Kande loomisel peate määratleda täielikku väljalastud toote Real enne Dynamics 365 operatsioonide üritab tuvastada tellimuse vaikesätted. Välja antud toote täielik määratlus tähendab, et kauba kood ja kõik aktiivse toote mõõtmed, konfiguratsiooni, suuruse, stiili ja värvi, nagu on määratud kandel. Näiteks kui loote käsitsi väljastatud tootevariandile ostutellimuse rea, peate määrama kõik vajalikud toote dimensioonid enne, kui tegevuskoha, lao, koguste ja täitmisaeg kuvatakse vaikimisi tellimusreal. 

Mitte kõiki tellimuse vaikesätete parameetreid ei rakendata tellimuse või töölehe ridade loomisel. Vajaduse korral vaikimisi kuvab ainult kogused ja aja. Näiteks žurnaalirealt inventuuride saidi ja ladu kuvab vaikimisi rea loomisel. Ilmselt ükski kogus rikkunud või kontrolli mitu ja miinimummääradeks läbi rea loomisel või töölehe sisestamist. 

Süsteem püüab tellimuse ja töölehe rea loomisel leida alati vaikimisi tegevuskohta ja ladu. Tegevuskohta ei kuvata alati vaikimisi tellimuse sätetest. Näiteks müügitellimuse või ostutellimuse loomisel kasutatakse tellimuse päise tegevuskohta automaatselt tellimuse ridadel. Koosluse rea loomisel kasutatakse saidi Koosluse päisest. Pärast kindlaks ei määrata, kasutatakse see leida meetmeid järjekorraga seaded, mida saab seejärel kasutada vaikimisi lao. 

Vaikimisi tellimuse tüüp, ostmist ja varude teostusaega saab overriden kauba laovarude reeglid on **kauba laovarud** lehel. Kuigi vaikimisi sortimisjärjestuse sätted ei võimalda tootmise ja üleandmise aega, kauba laovarude reeglid lubavad seda. Siiski kasutatakse kauba laovarude seadistust ainult MRP-ga plaanitud tootmise ja plaanitud üleviimistellimuse loomisel ja see ei rakendu tootmis- ja üleviimistellimuste käsitsi loomisel. 

## <a name="default-order-settings-rules"></a>Tellimuse vaikesätete reeglid
Saate määratleda üldised tellimuse vaikesätted ja mis tahes arvu tellimuse vaikesätete reegleid, mis rakenduvad ainult teatud tingimustele, nagu tegevuskoht või spetsiifiline toote dimensioon või toote dimensioonide kombinatsioon. Te ei saa määratleda laospetsiifilisi tellimuse sätteid.

### <a name="rank-in-default-order-settings"></a>Tellimuse vaikesätete hierarhia

Tellimuse vaikesätetel on hierarhia. Mida kõrgemal hierarhias reegel paikneb, seda olulisem reegel on, mis tähendab, et sellel on kõrgem prioriteetsus ja seda saab kasutada enne hierarhias madalatel positsioonidel olevaid reegleid. Üldistel tellimuse vaikesätetel on nullpositsioon, mida ei saa muuta. Ainult üks reegel saab olla nullpositsiooniga. Reeglitel võib hierarhias olla sama positsioon, tingimusel, et dimensioonid, millele need rakenduvad, on erinevad. See on kasulik tegevuskoha spetsiifiliste tellimuse sätete modelleerimiseks. Uue tellimuse vaikesätete reegli loomisel tellimuse väärtuste väärtused, peatamislipp, jne päritakse nullpositsiooniga reeglist, kuid selle saab alistada.

### <a name="default-order-settings-for-released-products"></a>Väljastatud toodete tellimuse vaikesätted

Eristuvate väljastatud toodete puhul saate määratleda üldised tellimuse sätted või tegevuskoha spetsiifilised tellimuse sätted. Üldistel tellimuse sätetel on alati nullpositsioon. Kui seadistate uued müügi, ostu ja varude tellimuse sätted samaaegselt koos, soovitame teil kasutada vaadet **Üksikasjade vaade** lehel **Tellimuse vaikesätted **. Kuva üksikasjad aktiveerimiseks minge ning **Valikud** Updatehagi paani &gt;**veebilehe Valikud**&gt;**muuta vaadet**&gt;**üksikasjade vaade**.

### <a name="site-specific-order-settings"></a>Tegevuskohaspetsiifilised tellimuse sätted

Tegevuskoha spetsiifiliste tellimuse sätete loomiseks klõpsake valikut **Uus**. Aastal **üksikasjade vaade**, saidi täita ning **sätted, mis on mõeldud**&gt;**saidi** välja. Vaates **Ruudustikuvaade** täitke tegevuskoht veerus **Tegevuskoht**. Uus reegel saab hierarhias automaatselt uue positsiooni väärtuse, mis on kõrgem kui null. Saate luua nii palju tegevuskohaspetsiifilisi reegleid kui vaja ja saate määrata kõik tegevuskohaspetsiifilised reeglid hierarhias samale positsioonile näitamaks, et need on võrdselt olulised. 

Kui asute vaates **Üksikasjade vaade** saate ülevaate kauba jaoks loodud reeglitest. Lülitage nuppu **Kuva/peida loend**, et näha ülevaate teavet. Kui tellimuse rea pära ning see pole mõõdikutele, Dynamics 365 toimingute puhul otsib reeglina koos määratud sait. See aitaks kindlaks rea vaikesaiti. Seda tegevuskohta kasutatakse seejärel tegevuskohaspetsiifilise reegli otsimiseks, kus võib olla seatud vaikimisi ladu. See ladu rakendatakse tellimuse reale.

### <a name="specific-order-settings-for-product-dimension"></a>Tootedimensiooni spetsiifilised tellimused sätted

Saate määratleda tellimuse sätete reeglid mis tahes aktiivsele toote dimensioonile või aktiivsete tootedimensioonide kombinatsioonile. Kui tootedimensiooni väli jäetakse tühjaks, siis rakendub see reegel kõigile tootedimensiooni väärtustele. 

Arvestage järgmist näidistoodet.

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Product name**                                    | Fotoelektriline andur                    |
| **Item number**                                     | XW56                                    |
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

See näide selgitab positsiooni vajadust. Kui konfiguratsiooni C1 ja revisjoni R2 jaoks luuakse ostutellimus, siis hierarhia positsiooni puudumisel oleks kaks R2 ja C1 jaoks määratletud reeglit ebamäärased. Ebamäärasuse lahendamiseks otsib Dynamics 365 for Operations reegleid läbi positsioonide laskuvas järjestuses ja rakendab esimese kohaldatava reegli. Praeguses näites, kui ostutellimuse rida luuakse konfiguratsiooni C1 ja revisjoni R2 jaoks, siis saab kasutaja hoiatusteate, et kaup on ootel ja et seda põhjustab revisjoni väärtus. Kui konfiguratsiooni reeglil oli kõrgem positsioon kui revisjoni reeglil, siis oleks ostutellimuse rea loomine konfiguratsiooni C1 ja revisjoni R2 jaoks olnud edukas ja kasutajale ei oleks kuvatud teadet „kaup ootel”. 

Arvestage järgmiseid tellimuse vaikesätte reegleid.

| Reiting | Sait | Konfiguratsioon | Laad | Vaiketegevuskoht | Vaikeladu | Ost – laoala vaikedimensioonide alistamine | Ostuladu |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Jah                                            | 22                 |
| 10   |      | C1            |  R2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Süsteem läbib reeglite kogumit tegevuskoha ja lao määramiseks kaks korda. Ostutellimuse rea loomisel Configuration C1, stiilis R2, määratakse saidi auaste 10 põhinevast. Seejärel otsib süsteem reeglina sait 2 ladu kindlaksmääramiseks. Leitakse reegel 20 ja kuna sellel on kõrgem positsioon, siis on ostutellimuse real olev ladu 22 ja mitte 21. 

Üldiste juhistena saavad spetsiifilised reeglid ja dimensioonide reeglid, mis on olulisemad kui teised dimensioonid, kõrgemaid positsioone, samas kui üldised reeglid saavad madalamaid positsioone. 

Nullpositsiooniga reegel täidab turvavõrgu rolli. Kui ühtki teist reeglit ei tabata, siis kasutatakse tellimuse vaikesätteid nullpositsioonist. 

Kuna hierarhia positsiooni number on nii oluline, on tegumiribal **Tellimuse vaikesätted **funktsioonid reegli üles ja alla liigutamiseks ning reeglite ümber nummerdamiseks, et need on alati juurdekasvuga 10. 

Väljastatud toote jaoks loodud reeglite arv võib olla hulgaline. Saamaks paremat aimu sellest, mida iga reegel alistab ja miks see on vajalik, soovitame kasutada vaadet **Ruudustikuvaade** lehel** Tellimuse vaikesätted**. Ruudustiku vaate saate lubada minnes on **Valikud** Updatehagi paani &gt;**veebilehe Valikud**&gt;**muuta vaadet**&gt;**tabelivaate**. Ruudustikus kuvatud veergude arv võib olla üsna märkimisväärne, eriti müügi ja varude vahekaartide puhul Koordinaatvõrgu veerud arvu piiramiseks saab sõprade veerud peidetud ja kuvada nuppude abil ning **vaikimisi tellimuse telefoni**&gt;**veeru Kuva** menüü.

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


