---
title: Tellimuse vaikesätted dimensioonide ja tootevariantide puhul
description: Tellimuse vaikesätted määratlevad koha ja lao, kust kaupu hangitakse või hoitakse, miinimum-, maksimum-, mitmik- ja standardkogused, mida kasutatakse kaubanduse või varude halduse jaoks, täitmisajad, peatamislipu ja tellimuse lubamise meetodi.
author: t-benebo
manager: tfehr
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemOrderSetup, InventItemIdLookupByDefaultOrderSetting, EcoResProductReleasedStoppedAllChartPart, UnitTestPartitions
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c3aa800c1a996a062bcb737afa23f00a9e52bb48
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426551"
---
# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Dimensioonide ja tootevariantide tellimuse vaikesätted

[!include [banner](../includes/banner.md)]

Tellimuse vaikesätted Dynamics 365 Supply Chain Managementis määratlevad koha ja lao, kust kaupu hangitakse või hoitakse, miinimum-, maksimum-, mitmik- ning standardkogused, mida kasutatakse kaubanduse või varude halduse jaoks, täitmisajad, peatamislipu ja tellimuse lubamise meetodi. Tellimuse vaikesätteid kasutatakse ostutellimuste, müügitellimuste, üleviimistellimuste, laotöölehtede loomisel ja plaanitud tellimuste loomiseks koondplaanimisega. Tellimuse vaikesätted võivad olla kaubaspetsiifilised, kohaspetsiifilised, tootevariandispetsiifilised ja või tootedimensiooni-spetsiifilised.

Toote jaoks tellimuse vaikesätete määratlemiseks toimige järgmiselt.

1. Avage **Tooteteabe haldus** &gt; **Tooted** &gt; **Väljastatud tooted**.
1. Valige ruudustikust asjakohane toode.
1. Järgige toimingupaanil ühte järgmistest sammudest, et avada valitud toote jaoks leht **Tellimuse vaikesätted**.

    - Valige vahekaardil **Plaan** grupis **Tellimuse sätted** suvand **Tellimuse vaikesätted**.
    - Valige vahekaardil **Varude haldus** grupis **Tellimuse sätted** suvand **Tellimuse vaikesätted**.

1. Konfigureerige sätted nii, nagu selles teemas kirjeldatud.

## <a name="default-order-settings"></a>Tellimuse vaikesätted

Ostudele, müügile ja varudele on kolme tüüpi tellimuse vaikesätteid. Ostude tellimuse vaikesätteid kasutatakse, kui luuakse:

- Ostutellimuse read
- Ostulepingu read
- Pakkumiskutse read
- Ostutaotluse read
- Saadetise täiendamise read (osaliselt toetatud, vt märget)
- Plaanitud ostutellimused

> [!NOTE]
> Saadetise täiendamise tellimuse ridade puhul rakendatakse lehe **Tellimuse vaikesätted** kiirkaardil **Ostutellimuse** olevatest sätetest ainult väljasid **Vaikekoht**, **Vaikeladu** ja märkeruutu **Peatatud**.

Müügi tellimuse vaikesätteid kasutatakse, kui luuakse:

- Müügitellimuse read
- Müügilepingu read
- Müügipakkumise read
- Tagastustellimuse read ja kaubaasenduse read
- Nõudluse prognoosi read

Vaikimisi müügitellimuse sätted rakenduvad ka siis, kui luuakse:

- Projekti kaubanõuded
- Teenuse tellimuse kaubanõuded

Varude tellimuse vaikesätteid kasutatakse, kui luuakse:

- Laotöölehed
- Üleviimistellimused
- Plaanitud üleviimistellimused

Varude tellimuse vaikesätted rakenduvad ka siis, kui luuakse:

- Vahelaoorderid
- Kvaliteettellimused
- Tootmistellimused
- Koosluseread
- Plaanitud tootmistellimused

## <a name="full-definition-of-a-released-product"></a>Väljastatud toote täielik määratlus

Kui loote kande, peate määrama väljastatud toote täieliku määratluse real, et Supply Chain Management saaks proovida tuvastada tellimuse vaikesätted. Väljastatud toote täielik määratlus tähendab, et kaubakood ja kõik aktiivsed tootedimensioonid, nagu konfiguratsioon, suurus, stiil, versioon ja värv, on kandel määratud. Näiteks kui loote käsitsi väljastatud tootevariandile ostutellimuse rea, peate määrama kõik vajalikud tootedimensioonid enne, kui koht, ladu, kogused ja täitmisaeg kuvatakse vaikimisi tellimuse real. 

Mitte kõiki tellimuse vaikesätete parameetreid ei rakendata tellimuse või töölehe ridade loomisel. Kogused ja täitmisajad kuvatakse vaikimisi ainult vastavalt vajadusele. Näiteks töölehe rea loendamisel kuvatakse rea loomisel vaikimisi ainult koht ja ladu. Sellel põhjusel ei tehta rea loomisel või töölehe sisestamisel kordsete või miinimumide puhul koguse vaikeolekusse seadmist ega kontrollimist. 

Süsteem püüab tellimuse ja töölehe rea loomisel leida alati vaikimisi kohta ja ladu. Kohta ei kuvata alati vaikimisi tellimuse sätetest. Näiteks müügitellimuse või ostutellimuse loomisel kasutatakse tellimuse päise kohta automaatselt tellimuse ridadel. Koosluse rea loomisel kasutatakse koosluse päise kohta. Pärast tegevuskoha määramist kasutatakse seda, et leida tegevuskohaga seotud tellimuse sätteid, mida saab seejärel lao jaoks vaikimisi kasutada. 

Lehel **Kauba laovarud** saab tellimuse vaiketüübi, ostu ja varude täitmisajad alistada kauba laovaru reeglitega. Kuigi tellimuse vaikesätted ei luba eristamist toote ja ülekande täitmisaja vahel, siis kauba laovaru reeglid lubavad seda. Siiski kasutatakse kauba laovarude seadistust ainult koondplaneerimise (MRP) abil plaanitud tootmise ja plaanitud üleviimistellimuste loomisel ning see ei rakendu tootmis- ja üleviimistellimuste käsitsi loomisel. 

## <a name="default-order-settings-rules"></a>Tellimuse vaikesätete reeglid

Saate määratleda üldised tellimuse vaikesätted ja mis tahes arvu tellimuse vaikesätete reegleid, mis rakenduvad ainult teatud tingimustele, nagu tegevuskoht või spetsiifiline toote dimensioon või toote dimensioonide kombinatsioon. Te ei saa määratleda laospetsiifilisi tellimuse sätteid.

### <a name="rank-in-default-order-settings"></a>Tellimuse vaikesätete hierarhia

Tellimuse vaikesätetel on hierarhia. Mida kõrgemal hierarhias reegel paikneb, seda olulisem reegel on, mis tähendab, et sellel on kõrgem prioriteetsus ja seda saab kasutada enne hierarhias madalatel positsioonidel olevaid reegleid. Üldistel tellimuse vaikesätetel on nullpositsioon, mida ei saa muuta. Ainult üks reegel saab olla nullpositsiooniga. Reeglitel võib hierarhias olla sama positsioon, tingimusel, et dimensioonid, millele need rakenduvad, on erinevad. See on kasulik tegevuskohaspetsiifiliste tellimuse sätete modelleerimiseks. Uue tellimuse vaikesätete reegli loomisel tellimuse väärtuste väärtused, peatamislipp, jne päritakse nullpositsiooniga reeglist, kuid selle saab alistada.

### <a name="default-order-settings-for-released-products"></a>Väljastatud toodete tellimuse vaikesätted

Eristuvate väljastatud toodete puhul saate määratleda üldised tellimuse sätted või tegevuskohaspetsiifilised tellimuse sätted. Üldistel tellimuse sätetel on alati nullpositsioon. Kui seadistate uued müügi-, ostu- ja varude tellimuse sätted samal ajal, soovitame teil kasutada vaadet **Üksikasjade vaade** lehel **Tellimuse vaikesätted**. Üksikasjade vaatele lülitamiseks valige **Suvandid** &gt; **Lehe suvandid** &gt; **Muuda vaadet** &gt; **Üksikasjade vaade**.

### <a name="site-specific-order-settings"></a>Tegevuskohaspetsiifilised tellimuse sätted

Tegevuskohaspetsiifiliste tellimuse sätete loomiseks valige **Uus**. Sisestage koht vaates **Üksikasjade vaade** väljale **Koht**, mis asub jaotises **Kohalduvad sätted**. Sisestage koht vaates **Ruudustikuvaade** veergu **Koht**. Uuele reeglile määratakse automaatselt uus positsiooni väärtus, mis on suurem kui 0 (null). Saate luua nii palju kohapõhiseid reegleid kui vaja. Et näidata, et need on võrdselt tähtsad, saate määrata kõigile kohapõhistele reeglitele sama positsiooni väärtuse.

Kui asute vaates **Üksikasjade vaade** saate ülevaate kauba jaoks loodud reeglitest. Kasutage nuppu **Kuva/peida loend**, et näha ülevaate teavet. Kui mis tahes tüübi tellimuse rida luuakse ja sellele pole ühtki tegevuskohta antud, otsib Supply Chain Management reeglit, millele pole tegevuskohta määratud. See aitab määrata tellimuse real vaiketegevuskoha. Seda tegevuskohta kasutatakse seejärel tegevuskohaspetsiifilise reegli otsimiseks, kuhu võib olla seatud vaikimisi ladu. See ladu rakendatakse tellimuse reale.

### <a name="specific-order-settings-for-product-dimension"></a>Tootedimensiooni spetsiifilised tellimused sätted

Saate määratleda tellimuse sätete reeglid mis tahes aktiivsele toote dimensioonile või aktiivsete tootedimensioonide kombinatsioonile. Kui tootedimensiooni väli on tühi, siis rakendub see reegel kõigile tootedimensiooni väärtustele. 

Arvestage järgmist näidistoodet.

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Toote nimi**                                    | Fotoelektriline andur                    |
| **Kaubakood**                                     | XW56                                    |
| **Konfiguratsioon** (kasutatakse valguse tüübi modelleerimiseks) | C1-nähtav punane tuli, C2 infrapunavalgus |
| **Versioon** | V1, V2, V3                              |

Selles näites eeldage, et toode on soetatud ja mitte toodetud. Samuti eeldage, et konfiguratsiooni C1 kasutatakse rohkem üldisemalt, seega on sellel lühemad täitmisajad. 

Looge selle stsenaariumi modelleerimiseks järgmised tellimuse vaikesätted.

| Reiting | Koht | Konfiguratsioon | Versioon | Ost – vaikesätete alistamine | Ostu täitmisaeg | Ost – peatatud | Müük – vaikesätete alistamine | Müük – peatatud |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Jah                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Kui kauba XW56, konfiguratsiooni C1 jaoks luuakse ostutellimuse rida või plaanitud ostutellimus, siis loetakse täitmisajaks 2 hoolimata versioonist või kohast, kus rida ladustatakse. Eeldage, et kõik versioonid peale V3 on peatatud.

Saate luua järgmised tellimuse vaikesätete reeglid.

| Reiting | Koht | Konfiguratsioon | Versioon | Ost – vaikesätete alistamine | Ostu täitmisaeg | Ost – peatatud | Müük – vaikesätete alistamine | Müük – peatatud |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | V2    | Jah                                  |                    | Jah                | Jah                               | Jah             |
| 20   |      |               | V1    | Jah                                  |                    | Jah                | Jah                               | Jah             |
| 10   |      | C1            |       | Jah                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Vanade versioonide peatamise kahel reeglil on sama positsioon. Seetõttu on need võrdselt tähtsad. Kuna mõlemal reeglil on kõrgem positsioon kui konfiguratsiooni C1 reeglil, tähendab see, et need on konfiguratsiooni C1 reegli suhtes ülimuslikud. 

See näide selgitab positsiooni vajadust. Kui konfiguratsiooni C1 ja versiooni V2 jaoks ostutellimuse loomisel ei kasutata positsiooni, on V2 ja C1 jaoks määratletud kaks reeglit ebamäärased. Ebamäärasuse lahendamiseks otsib Supply Chain Management reegleid läbi positsioonide laskuvas järjestuses ja rakendab esimese kohaldatava reegli. Praeguses näites, kui ostutellimuse rida luuakse konfiguratsiooni C1 ja versiooni V2 jaoks, siis saab kasutaja hoiatusteate, millel on kirjas, et kaup on ootel ja seda põhjustab versiooni väärtus. Kui konfiguratsiooni reeglil oli kõrgem positsioon kui versiooni reeglil, siis oleks ostutellimuse rea loomine konfiguratsiooni C1 ja versiooni V2 jaoks olnud edukas ning kasutajale ei kuvataks teadet „kaup ootel”. 

Arvestage järgmiseid tellimuse vaikesätte reegleid.

| Reiting | Koht | Konfiguratsioon | Versioon | Vaiketegevuskoht | Vaikeladu | Ost – laoala vaikedimensioonide alistamine | Ostuladu |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Jah                                            | 22                 |
| 10   |      | C1            |  V2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Süsteem läbib reeglite kogumi tegevuskoha ja lao määramiseks kaks korda. Kui konfiguratsiooni C1, versiooni V2 jaoks luuakse ostutellimuse rida, siis määratakse koht reegli põhjal, mille positsioon on 10. Seejärel otsib süsteem lao määramiseks reeglit koha 2 jaoks. Leitakse reegel 20 ja kuna sellel on kõrgem positsioon, siis on ostutellimuse real olev ladu 22, mitte 21.

Üldiselt saavad spetsiifilised reeglid ja dimensioonide reeglid, mis on olulisemad kui teised dimensioonid, kõrgemaid positsioone, samas kui üldised reeglid saavad madalamaid positsioone. 

Nullpositsiooniga reegel täidab turvavõrgu rolli. Kui ühtki teist reeglit ei tabata, siis kasutatakse tellimuse vaikesätteid nullpositsioonist. 

Kuna positsiooninumber on nii oluline, on toimingupaanil **Tellimuse vaikesätted** funktsioonid reegli üles ja alla liigutamiseks ning reeglite ümbernummerdamiseks, et need suureneksid alati 10 võrra. 

Väljastatud toote jaoks loodud reeglite arv võib olla hulgaline. Saamaks paremat aimu sellest, mida iga reegel alistab ja miks see on vajalik, soovitame kasutada vaadet **Ruudustikuvaade** lehel **Tellimuse vaikesätted**. Saate lubada ruudustikuvaate, valides **Suvandid** &gt; **Lehe suvandid** &gt; **Muuda vaadet** &gt; **Ruudustikuvaade**. Ruudustikus kuvatud veergude arv võib olla üsna märkimisväärne, eriti müügi ja varude vahekaartide puhul Ruudustikus näidatud veergude arvu piiramiseks saab veergude gruppe peita või kuvada, kasutades menüü **Tellimuse vaikesätted** &gt; **Veeru kuvamine** nuppe.

### <a name="specific-order-settings-for-released-product-variant"></a>Väljastatud tootevariandi spetsiifilised tellimuse sätted

Kui tellimuse vaikesätete reeglite süsteem on liiga raskepärane, siis on võimalik määratleda iga tootevariandi jaoks tellimuse vaikesätted. Järgmises näites on näha, kuidas see toote ja eespool toodud juhtumite puhul välja näeb.

| Reiting | Koht | Konfiguratsioon | Versioon | Ost – vaikesätete alistamine | Ostu täitmisaeg | Ost – peatatud | Müük – vaikesätete alistamine | Müük – peatatud |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | V3    | Jah                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | V2    | Jah                                  | 5                  | Jah                | Jah                               | Jah             |
| 10   |      | C2            | V1    | Jah                                  | 5                  | Jah                | Jah                               | Jah             |
| 10   |      | C1            | V3    | Jah                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | V2    | Jah                                  | 2                  | Jah                | Jah                               | Jah             |
| 10   |      | C1            | V1    | Jah                                  | 2                  | Jah                | Jah                               | Jah             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Sellisel juhul ei ole positsioon tegelikult tähtis, seega saate valida selle peitmise. See lahendus tekitab hoolduse probleemi. Siiski võikiste kaaluda selle seadistuse kasutamist, kui kaalute integreerimist toote töötsükli halduse (PLM) süsteemidega.

## <a name="use-strict-or-standard-validation-of-default-order-quantities"></a>Tellimuse vaikekoguste range või standardse kontrollimise kasutamine

Saate valida, kui range peaks süsteem olema, kui kontrollitakse koguseid, mis on toote jaoks **Tellimuse vaikesätetes** sisestatud. Kui kasutate uut ranget suvandit, peab **Standardne tellimuse kogus** olema alati ostutellimustele, varudele ja müügitellimustele määratud väärtuse **Tegur** korrutis. Kui kasutate ranget valideerimist, ei saa te salvestada tellimuse vaikesätteid, mis ei vasta sellele nõudele (ja teateribal kuvatakse tõrge). 

Range kontrollimine rakendub **Standardse tellimuse koguse** väärtustele, mis on määratud kiirkaartidel **Ostutellimus**, **Varud** ja **Müügitellimus** lehel **Tellimuse vaikesätted**. Igal kiirkaardil on oma säte **Tegur**, mida kasutatakse selle kiirkaardi jaoks määratud väärtuse **Standardne tellimuse kogus** kontrollimiseks.

### <a name="enable-the-strict-validation-option"></a>Range kontrollimise suvandi lubamine

Enne range kontrollimise funktsiooni kasutamist peab see teie süsteemis olema sisse lülitatud. Administraatorid saavad kasutada [funktsioonide halduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lehte, et kontrollida funktsiooni olekut ja vajaduse korral see lubada. Siin on funktsioon loetletud järgmiselt.

- **Moodul** - *Tooteteabe haldus*
- **Funktsiooni nimi** - *Tellimuse vaikekoguste range kontrollimine*

### <a name="set-the-validation-option"></a>Kontrollimissuvandi määramine

Kontrollimissuvandi määramiseks tehke järgmist.

1. Avage **Tooteteabe haldus \> Seadistus \> Tooteteabe halduse parameetrid**.
1. Seadke vahekaardil **Üldine** suvandi **Tellimuse vaikekoguste kontrollimine** väärtuseks üks järgmistest.
    - **Range** – valige see suvand, et teha kindlaks, et kõik **Standardse tellimuse koguse** väärtused oleksid iga kiirkaardi puhul (**Ostutellimus**, **Varud** ja **Müügitellimus**) väärtuse **Tegur** korrutised.
    - **Standardne** – valige see suvand standardse kontrollimise kasutamiseks (mis toimib nii, nagu see funktsioon poleks lubatud).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]