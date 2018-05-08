---
title: "Üksik mitme kliendi- või hankijakirjega kanne"
description: "See teema annab ülevaate sellest, mis juhtub, kui sisestate ühe mitme kliendi või hankija kirjega kande. See funktsioon katkestatakse rakenduse Microsoft Dynamics 365 for Finance and Operations tulevastes versioonides, mille tulemusena me ei soovita me kasutada seda sisestamise meetodit raamatupidamise mõju tõttu tasakaalustamisprotsessile."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 222534
ms.assetid: d4df11ce-4d36-4c66-8230-f5fc58e021bc
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 4c499e31fb42a69dff6ac41faac0c78f7f4d1876
ms.contentlocale: et-ee
ms.lasthandoff: 03/26/2018

---

# <a name="single-voucher-with-multiple-customer-or-vendor-records"></a>Üksik mitme kliendi- või hankijakirjega kanne

[!include [banner](../includes/banner.md)]

See teema annab ülevaate sellest, mis juhtub, kui sisestate ühe mitme kliendi või hankija kirjega kande. See funktsioon katkestatakse rakenduse Microsoft Dynamics 365 for Finance and Operations tulevastes versioonides, mille tulemusena me ei soovita me kasutada seda sisestamise meetodit raamatupidamise mõju tõttu tasakaalustamisprotsessile. 

Mõned levinumad süsteemid, kus üht kannet kasutatakse mitme kliendi või hakija jaoks, hõlmavad saldo ülekandeid klientide vahel ja saldode tasaarveldust klientide ja hankijate vahel samas organisatsioonis. 

Rohkem kui üht klienti või hankijat sisaldava kande saab sisestada, kasutades üht järgmistest meetoditest.

-   Sellise töölehe kasutamine, millel on suvand **Ainult üks kande number** valitud, et iga töölehele lisatud rida kaasatakse samasse kandesse.
-   Sellise mitmerealise kande kasutamine, kus puudub pearaamatu vastaskonto, rohkem kui ühe kliendi või hankijaga.
-   Kontoga kande sisestamine ja vastaskonto on hankija/hankija, klient/klient, hankija/klient või klient/hankija.

See teema näitab, kuidas tasakaalustust töödeldakse, kui sisestatakse üks mitme kliendi või hankijaga kanne. Lisaks pakub see teema vastukaale, et aidata teil mõista, kuidas vältida ühe kande kasutamist mitme kliendi või hankijaga. Eelkõige on näiteid, mis kirjeldavad kaht ühist tasakaalustamise stsenaariumit, mida mõjutab ühe kande kasutamine mitme kliendi või hankijaga.

-   Sularaha allahindluse raamatupidamine
-   Ümberhindamise raamatupidamine

## <a name="how-does-settlement-impact-single-voucher-usage"></a>Kuidas tasakaalustus mõjutab ühe kande kasutust
Mitut kliendi- või hankijakirjet sisaldava kande sisestamisel luuakse üks raamatupidamiskanne, mis sisaldab müügireskontro ja ostureskontro saldosid. Tasakaalustamisprotsessi käigus kasutatakse algseid raamatupidamiskirjeid, et luua raamatupidamiskirjed skonto, realiseerimata kasumite ja kahjumite, realiseeritud kasumite ja kahjumite ning algse dokumendi summakonto vabastuse jaoks. Näiteks kui hankijmakse tasakaalustamisel arvele võetakse skonto, peab skonto raamatupidamine sisestama ostureskontro pearaamatukontole algsest arvest. Kui algne arve sisestati kandesse, mis sisaldab mitut hankijakirjet, tehakse algsest raamatupidamisest kokkuvõte. Kuna sel juhul ei ole võimalik juurde pääseda iga hankija kande üksikasjalikule raamatupidamiskirjele ühes kandes, ei ole võimalik kindlaks määrata, kuidas kasutaja kavatses skontot arvestada.

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-cash-discount-accounting"></a>Üks mitme hankijaga kanne ja mõju skonto raamatupidamisele

Järgmises näites kirjendatakse mitu hankijaarvet pearaamatusse lehe **Päevaraamat** ühes kandes. Need arved jaotatakse mitme konto dimensiooni vahel.

|             |                  |              |                 |           |            |
|-------------|------------------|--------------|-----------------|-----------|------------|
| **Kanne** | **Konto tüüp** | **Konto**  | **Kirjeldus** | **Debiteeri** | **Krediit** |
| GNJL001     | Tarnija           | 1001         | INV1            |           | 100,00     |
| GNJL001     | Tarnija           | 1001         | INV2            |           | 200,00     |
| GNJL001     | Tarnija           | 1001         | INV3            |           | 300.00     |
| GNJL001     | Pearaamat           | 606300-001-- | INV1            |   50,00   |            |
| GNJL001     | Pearaamat           | 606300-002-- | INV1            |   50,00   |            |
| GNJL001     | Pearaamat           | 606300-003-- | INV2            | 200,00    |            |
| GNJL001     | Pearaamat           | 606300-004-- | INV3            | 300.00    |            |

Pärast sisestamist luuakse üks kanne.

|             |              |                  |                                    |
|-------------|--------------|------------------|------------------------------------|
| **Kanne** | **Konto**  | **Sisestamistüüp** | **Summa kandevaluutas** |
| GNJL001     | 606300-001-- | Pearaamatu tööleht   | 50,00                              |
| GNJL001     | 606300-002-- | Pearaamatu tööleht   | 50,00                              |
| GNJL001     | 606300-003-- | Pearaamatu tööleht   | 200,00                             |
| GNJL001     | 606300-004-- | Pearaamatu tööleht   | 300.00                             |
| GNJL001     | 200110-001-  | Hankija saldo   | -100,00                            |
| GNJL001     | 200110-001-  | Hankija saldo   | –200,00                            |
| GNJL001     | 200110-001-  | Hankija saldo   | -300.00                            |

Pange tähele, et kanne sisaldab hankijasaldo sisestamistüübi jaoks ühes kandes kolme kirjet. Puudub viis, kuidas näidata, et deebet 50,00 606300-001-le ja deebet 50,00 606300-002-le on mõeldud tasakaalustama hankija saldo kirjet 200110-001. Seda seetõttu, et kasutaja sisestas mitu hankijakirjet ühte kandesse.

Selle näite abil saame analüüsida, kuidas mõjutab ühe kande kasutamine allavoolu tasakaalustamise raamatupidamist. Oletame, et maksate arvest 197,00/200,00, võttes skonto 3,00. Pange tähele, et skonto kontoväärtus jaotatakse arve kande kulukontodest kõigi dimensioonide vahel. Selle põhjuseks on see, et üht kannet kasutati eespool toodud arve sisestamiseks ilma viitamata, kuidas pidid kulukaotused kasutaja kavatsuse järgi korreleeruma hankijasaldo järgi ühes kandes.

|             |              |                      |           |            |
|-------------|--------------|----------------------|-----------|------------|
| **Kanne** | **Konto**  | **Sisestamistüüp**     | **Debiteeri** | **Krediit** |
| APPAYM001   | 200110-001-  | Hankija saldo       | 197.00    |            |
| APPAYM001   | 110110-001-  | Pank                 |           | 197.00     |
| 14000056    | 520200-001-- | Hankija skonto |           | 0.25       |
| 14000056    | 520200-002-- | Hankija skonto |           | 0.25       |
| 14000056    | 520200-003-- | Hankija skonto |           | 1,00       |
| 14000056    | 520200-004-- | Hankija skonto |           | 1.50       |
| 14000056    | 200110-001-  | Hankija saldo       | 3,00      |            |

Kui kasutaja pole rahul, et skonto jaotatakse ühe kande asemel algse arve kõigi kulujaotuste vahel, tuleb arvete kirjendamiseks kasutada mitut kannet. Siin on näide, kuidas pearaamatusse saab ühe kande kasutamise asemel sisestada mitu kannet, nagu on näidatud selle näite alguses.

|             |                  |              |                 |           |            |                 |                    |
|-------------|------------------|--------------|-----------------|-----------|------------|-----------------|--------------------|
| **Kanne** | **Konto tüüp** | **Konto**  | **Kirjeldus** | **Debiteeri** | **Krediit** | **Tasakaalustustasu tüüp** | **Vastaskonto** |
| GNJL001     | Tarnija           | 1001         | INV1            |           | 100,00     | Pearaamat          | &lt;tühi&gt;      |
| GNJL001     | Pearaamat           | 606300-001-- | INV1            |   50,00   |            | Pearaamat          | &lt;tühi&gt;      |
| GNJL001     | Pearaamat           | 606300-002-- | INV1            |   50,00   |            | Pearaamat          | &lt;tühi&gt;      |
| GNJL002     | Tarnija           | 1001         | INV2            |           | 200,00     | Pearaamat          | 606300-003--       |
| GNJL003     | Tarnija           | 1001         | INV3            |           | 300.00     | Pearaamat          | 606300-004--       |

Nüüd kui makstakse INV2, tehakse järgmine kirje. Pange tähele, et skonto finantsdimensioonid järgnevad seostatud kulu finantsdimensioonidele.

|             |              |                      |           |            |
|-------------|--------------|----------------------|-----------|------------|
| **Kanne** | **Konto**  | **Sisestamistüüp**     | **Debiteeri** | **Krediit** |
| APPAYM001   | 200110-001-  | Hankija saldo       | 197.00    |            |
| APPAYM001   | 110110-001-  | Pank                 |           | 197.00     |
| 14000056    | 520200-003-- | Hankija skonto |           | 3,00       |
| 14000056    | 200110-001-  | Hankija saldo       | 3,00      |            |

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-realized-gainloss-accounting"></a>Üks mitme hankijaga kanne ja mõju realiseeritud kasumi/kahjumi raamatupidamisele

|             |                  |             |                 |           |            |                  |              |
|-------------|------------------|-------------|-----------------|-----------|------------|------------------|--------------|
| **Kanne** | **Konto tüüp** | **Konto** | **Kirjeldus** | **Debiteeri** | **Krediit** | **Konto tüüp** | **Konto**  |
| GNJL001     | Tarnija           | 1001        | INV1            |           | 100,00     | Pearaamat           | 606300-001-- |
| GNJL001     | Tarnija           | 1001        | INV2            |           | 200,00     | Pearaamat           | 606300-002-- |

Järgmises näites salvestatakse mitu hankijaarvet pearaamatusse lehe **Päevaraamat** ühes kandes. Need arved jaotatakse mitme konto dimensiooni vahel. Pärast sisestamist luuakse üks kanne.

|             |              |                  |                                          |                                         |
|-------------|--------------|------------------|------------------------------------------|-----------------------------------------|
| **Kanne** | **Konto**  | **Sisestamistüüp** | **Summa kandevaluutas (EUR)** | **Summa arvestusvaluutas (USD)** |
| GNJL001     | 606300-001-- | Pearaamatu tööleht   | 100,00                                   | 114.00                                  |
| GNJL001     | 606300-002-- | Pearaamatu tööleht   | 200,00                                   | 228.00                                  |
| GNJL001     | 200110-001-  | Hankija saldo   | -100,00                                  | -114.00                                 |
| GNJL001     | 200110-001-  | Hankija saldo   | –200,00                                  | -228.00                                 |

Pange tähele, et kanne sisaldab hankijasaldo sisestamistüübi jaoks ühes kandes kahte kirjet. Puudub viis, kuidas näidata, et deebet 606300-001 jaoks on mõeldud tasakaalustama hankija saldo kirje 100,00 200110-001-le. Seda seetõttu, et kasutaja sisestas mitu hankijakirjet ühte kandesse. 

Selle näite abil saame analüüsida, kuidas mõjutab ühe kande kasutamine allavoolu tasakaalustamise raamatupidamist. Oletame, et arvestusvaluuta on USD ja eespool toodud kanded sisestati kandevaluutas EUR. Oletame, et maksate täielikult arve 200,00 EUR, kuid ilmneb realiseeritud kahjum, mis tuleneb arve sisestamise ja selle maksmise aja vahelise vahetuskursi erinevusest. Pange tähele, et realiseeritud kahjumi kontoväärtus jaotatakse arve kande kulukontodest kõigi dimensioonide vahel. Sellisel juhul jaotati mõlemad dimensioonid 001 ja 002, kuigi kasutaja võib tajuda, et ainult 002 kuulub tasakaalustatava arve kulukontole. Selle põhjuseks on see, et üht kannet kasutati eespool toodud arve sisestamiseks jätmata ühtki viisi viitamaks, kuidas pidid kulukaotused kasutaja kavatsuse järgi korreleeruma hankijasaldo järgi ühes kandes.

|             |             |                    |                                          |                                         |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| **Kanne** | **Konto** | **Sisestamistüüp**   | **Summa kandevaluutas (EUR)** | **Summa arvestusvaluutas (USD)** |
| APPAYM001   | 200110-001- | Hankija saldo     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Pank               | –200,00                                  | -230.00                                 |
| 14000056    | 801300-001- | Valuutakursi kahjum | 0,00                                     | 0.67                                    |
| 14000056    | 801300-002- | Valuutakursi kahjum | 0,00                                     | 1.33                                    |
| 14000056    | 200110-001- | Hankija saldo     |                                          | -2.00                                   |

Kui kasutaja pole rahul, et vahetuskursi kahjum jaotatakse ühe kande asemel algse arve kõigi kulujaotuste vahel, tuleb arvete kirjendamiseks kasutada mitut kannet. Siin on näide, kuidas pearaamatusse saab ühe kande kasutamise asemel sisestada mitu kannet, nagu on näidatud selle näite alguses.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Kanne** | **Konto tüüp** | **Konto** | **Kirjeldus** | **Debiteeri** | **Krediit** | **Tasakaalustustasu tüüp** | **Vastaskonto** |
| GNJL002     | Tarnija           | 1001        | INV1            |           | 100,00     | Pearaamat          | 606300-001--       |
| GNJL003     | Tarnija           | 1001        | INV2            |           | 200,00     | Pearaamat          | 606300-002--       |

Nüüd kui makstakse INV2, tehakse järgmine kirje. Pange tähele, et vahetuskursi kahjumi finantsdimensioonid järgnevad seostatud kulu finantsdimensioonidele.

|             |             |                    |                                          |                                         |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| **Kanne** | **Konto** | **Sisestamistüüp**   | **Summa kandevaluutas (EUR)** | **Summa arvestusvaluutas (USD)** |
| APPAYM001   | 200110-001- | Hankija saldo     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Pank               | –200,00                                  | -230.00                                 |
| 14000056    | 801300-002- | Valuutakursi kahjum | 0,00                                     | 2.00                                    |
| 14000056    | 200110-001- | Hankija saldo     |                                          | -2.00                                   |

## <a name="one-voucher-for-balance-transfers-and-netting-scenarios"></a>Üks kanne saldo ülekannete ja tasaarvelduse stsenaariumide jaoks
Kaks levinumalt kasutatud stsenaariumit, mis kasutavad üht mitut klienti või hankijat sisaldavat kannet, hõlmavad saldo ülekandeid ühelt kliendilt/hankijalt teisele kliendile/hankijale ja sama organisatsiooni kliendi ja hankija tasaarveldamist. Kaks järgmist näidet kirjeldavad eelistatud meetodit nende stsenaariumide sisestamiseks rakendusse Dynamics 365 for Finance and Operations, alternatiivina nende sisestamisele ühte kandesse. 

*Saldo ülekanne* on üks mitme kliendiga kanne, mis on sisestatud eesmärgil kanda saldo ühelt kliendilt teisele kliendile üle (sama hankijatele) See stsenaarium võib esineda, kui vastutus arve maksmise eest nihkub teisel osapoolele, näiteks tütarettevõte nihutab vastutuse emaettevõttele. 

See näide eeldab müüki, kus klient on sobilik skonto jaoks siis, kui makse tehakse 10 päeva jooksul. Klient kasutab selles näites kindlustusettevõtet, kes vastutab arve tasumise eest. Kindlustusettevõte seadistatakse süsteemis teise kliendina. Algne kliendi saldo kantakse üle kindlustusettevõttele, kes tasub arve, võttes 2% skotot allahindlusperioodi siseselt tasumise eest. 

Kirjeldamiseks eeldame, et järgmine müük tehakse kliendile ACME. Järgmised raamatupidamiskirjed tähistavad müüki.

|                    |                  |           |            |
|--------------------|------------------|-----------|------------|
| **Pearaamatukonto** | **Sisestamistüüp** | **Debiteeri** | **Krediit** |
| 401100-002-023-    | Tulu          |           | 100        |
| 130100-002-        | Kliendi saldo | 100       |            |

Järgmisena kannab kasutaja ACME-lt nõutava saldo üle kindlustusettevõttele müügireskontro maksetöölehel ühes kandes. Rakenduses Finance and Operations on kindlustusettevõte seadistatud kui kliendi kindlustus.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Kanne** | **Konto tüüp** | **Konto** | **Kirjeldus** | **Debiteeri** | **Krediit** | **Tasakaalustustasu tüüp** | **Vastaskonto** |
| ARPAYM001   | Klient         | ACME        | Ülekanne        |           | 100,00     | Klient        | Kindlustus          |

Pange tähele, et eespool toodud kirje sisaldub ühes kandes. See kanne sisaldab kaht kliendikirjet. Järgmine kanne luuakse eespool toodud pearaamatu kirje sisestamisel.

|             |             |                  |                                    |
|-------------|-------------|------------------|------------------------------------|
| **Kanne** | **Konto** | **Sisestamistüüp** | **Summa kandevaluutas** |
| ARPAYM001   | 130100-002- | Kliendi saldo | 100,00                             |
| ARPAYM001   | 130100-002- | Kliendi saldo | -100,00                            |

Järgmisena oletame, et saate kindlustuskliendilt makse 98,00 ja valite makse tasakaalustamise saldo ülekandega loodud arvega. See põhjustab järgmise kande sisestamise. Võib olla ootus, et tasakaalustus kasutab finantsdimensioone algsest arvest, kuid see pole võimalik, kuna kindlustuskliendi jaoks puudub arvedokument. Pange tähele, et vaikimisi tulenevad skonto jaotusdimensioonid ülekandest loodud kliendikandest, mitte algse arve tulukontolt. Vaikesäte on saldode ülekandmiseks ühe kande kasutamise tulemus.

|             |             |                  |           |            |
|-------------|-------------|------------------|-----------|------------|
| **Kanne** | **Konto** | **Sisestamistüüp** | **Debiteeri** | **Krediit** |
| ARPAYM002   | 110110-002- | Pank             | 98.00     |            |
| ARPAYM002   | 130100-002- | Kliendi saldo |           | 98.00      |

Skonto jaoks seotud kandel tuleneb finantsdimensiooni vaikesäte ülekandest loodud kliendikandest, kuna ülekandel on rohkem kui üks klient.

|             |             |                        |           |            |
|-------------|-------------|------------------------|-----------|------------|
| **Kanne** | **Konto** | **Sisestamistüüp**       | **Debiteeri** | **Krediit** |
| ARP‑00001   | 403300-002- | Kliendi skonto | 2.00      |            |
| ARP‑00001   | 130100-002- | Kliendi saldo       |           | 2.00       |

Kui kasutaja ei ole rahul skonto finantsdimensioonide vaikesättega tuleks ühe kande asemel kasutada saldo ülekande kirjeldamiseks mitut kannet. Selle stsenaariumi saavutamiseks tuleks luua krediiditeatis sellele kliendile, kellelt saldo liigutati, ja deebetiteatis või arve sellele kliendile, kellele saldo liigitatakse. Järgmine näide näitab, kuidas ühe kande kasutamise asemel tuleks saldo ülekandmiseks sisestada müügireskontro makse töölehele mitu kannet, nagu on näidatud varasemalt selles näites.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Kanne** | **Konto tüüp** | **Konto** | **Kirjeldus** | **Debiteeri** | **Krediit** | **Tasakaalustustasu tüüp** | **Vastaskonto** |
| ARPAYM001   | Klient         | ACME        |                 |           | 100,00     | Pearaamat          | 401100-002-023-    |
| ARPAYM002   | Klient         | Kindlustus   |                 | 100,00    |            | Pearaamat          | 401100-002-023-    |

See tähendab, et kui kindlustusklient maksab 98,00 kandega ARPAYM02, kasutatakse õigeid finantsdimensioone kande ARPAYM002 pearaamatukonto kirjest.

|             |             |                  |           |            |
|-------------|-------------|------------------|-----------|------------|
| **Kanne** | **Konto** | **Sisestamistüüp** | **Debiteeri** | **Krediit** |
| ARPAYM003   | 110110-002- | Pank             | 98.00     |            |
| ARPAYM003   | 130100-002  | Kliendi saldo |           | 98.00      |

Seotud skonto kandel kasutatakse finantsdimensioone kandel ARPAYM002 näidatud tasakaalustavalt tulukontolt.

|             |                 |                        |           |            |
|-------------|-----------------|------------------------|-----------|------------|
| **Kanne** | **Konto**     | **Sisestamistüüp**       | **Debiteeri** | **Krediit** |
| ARP‑00001   | 403300-002-023- | Kliendi skonto | 2.00      |            |
| ARP‑00001   | 130100-002-     | Kliendi saldo       |           | 2.00       |

### 

## <a name="one-voucher-with-a-netting-for-multiple-customers-and-vendors"></a>Üks kanne tasaarveldusega mitme kliendi ja hankija jaoks
Tasaarveldus võib olla kasulik, kui organisatsioon ostab ja müüb samale ettevõttele. Hankijaarvete tasumise ja kliendiarvete eest makse ootamise asemel tasaarveldatakse hankija- ja kliendiarved. Tasaarvelduse kanne tasakaalustatakse tähtaja ületanud saldode suhtes. 

Kirjeldamiseks oletame, et hankija 1001 ja klient US-008 on sama üksus, seega teie organisatsioon soovib ostureskontro ja müügireskontro saldod tasaarveldada enne ülejäänud saldo tasumist/vastuvõtmist. Oletame, et kliendi kirje võlgneb 75,00 EUR ja hankija kirje võlgneb 100,00 EUR, mis tähendab, et eelistaksite saldod tasaarveldada ja tasuda ainult hankijale 25,00 EUR. Täiendavalt oletame, et arvestusvaluuta on USD. Sellisel juhul tasaarvelduse kanne sisestatakse ostureskontro maksetöölehel ühesse kandesse.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Kanne** | **Konto tüüp** | **Konto** | **Kirjeldus** | **Debiteeri** | **Krediit** | **Tasakaalustustasu tüüp** | **Vastaskonto** |
| APPAYM001   | Tarnija           | 1001        | Tasaarveldus         |  75,00    |            | Klient        | US-008             |

Vältimaks soovimatuid probleeme tulevaste tasakaalustamistega selle kande puhul tuleb tasaarveldamise kande kirjendamiseks sisestada töölehele ühe kande kasutamise asemel mitu kannet. Pange tähele, et kliendi- ja hankijasaldod tasakaalustatakse ühe kliiringukontoga, et vältida ühe sellise kande kasutamist, mis sisaldab mitut kliendi- ja hankijasaldot.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Kanne** | **Konto tüüp** | **Konto** | **Kirjeldus** | **Debiteeri** | **Krediit** | **Tasakaalustustasu tüüp** | **Vastaskonto** |
| 001         | Klient         | US-008      |                 |           |  75,00     | Pearaamat          | 999999---          |
| 002         | Tarnija           | 1001        |                 |  75,00    |            | Pearaamat          | 999999---          |






