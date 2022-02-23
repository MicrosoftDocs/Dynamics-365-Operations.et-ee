---
title: Kolmesuunalised vastavusse viimise poliitikad
description: See teema sisaldab näiteid kolmesuunalise vastavusseviimise kohta.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 2761
ms.assetid: 70f3cb1a-18b7-4474-95ec-28b2410dd8f8
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d84e3ed050bacf7632d03cf0123f682c43fd7b58
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442311"
---
# <a name="three-way-matching-policies"></a>Kolmesuunalised vastavusse viimise poliitikad

[!include [banner](../includes/banner.md)]

See teema sisaldab näiteid kolmesuunalise vastavusseviimise kohta.

<a name="example-three-way-matching-for-items"></a>Näide: kaupade kolmesuunaline vastavusse viimine
-------------------------------------

**Kokkuvõte:** Ken on kontroller Fabrikami nimelise juriidilise isiku peakontoris. Ken otsustab, et kõik ostutellimustel põhinevad hankija arved tuleks viia vastavusse ostutellimuse ridadega (kahesuunaline vastavusse viimine). Põhivaradena kasutatavate kaupade ostuarved peaksid aga olema vastavusse viidud nii ostutellimuse kui ka toote sissetuleku ridadega (kolmesuunaline vastavusse viimine).

Fabrikami alla kuulub mitu juriidilist isikut ja ettevõttel on töötajaid üle maailma. Kannete mahu suurenedes kasvavad ka lahknevused sissetulekute ja arvete vahel. Selle tulemuseks vara mahakandmine. Hankijatelt saadud arved makstakse, kuid protsess ei sisalda saadud ja tellitud kaupade koguste lahknevuste tuvastamist ega seda, kas kaubad üldse saadi. Kulutused aga suurenevad, sest töötajad vajavad töö tegemiseks ikkagi tööriistu ja teisi materjale. Ken tahab veenduda, et hankijad tarnivad tellitud tooted ja Fabrikami töötajad võtavad kaubad vastu. Seega nõuab Ken kõigilt organisatsiooni juriidilistelt isikutelt kahe- ja kolmesuunalist vastavusse viimist. Arvete vastavusse viimine aitab tagada, et probleeme kaduma läinud või tarnimata jäänud kaupadega on võimalik jälitada ja lahendada. 

Selles näites toodud arvete vastavusse viimise poliitikad aitavad järgmistes rollides inimestel järgmisi eesmärke täita.

-   Ken on ettevõtte Fabrikam kontroller. Ta saab aidata inimestel oma organisatsioonis hankijatelt kaupade (tooted ja teenused) tellimise, vastuvõtu ja maksmisega seotud probleeme tuvastada ja lahendada.
-   Phyllis ja April on Fabrikami Ameerika Ühendriikide allüksuse arveldusosakonna raamatupidamise juhid. Nemad saavad korporatiivset poliitikat kehtestada ja tagada, et arved makstakse alles pärast seda, kui need on ostutellimuse ning toodete ja teenuste sissetulekuga vastavusse viidud, kui see on vajalik.
-   Tony on Fabrikami Ameerika Ühendriikide allüksuse tootmisjuht. Tema ja ülejäänud tootmistöötajad saavad veenduda, et hankijatelt saadakse tellitud kaubad ja need loetakse, nii et töötajatel on tööde tegemiseks kõik vajalik olemas.

### <a name="prerequisites"></a>Eeltingimused

-   Ken seadistab juriidilise isiku tasemel vastavusse viimise poliitikaks Kolmesuunaline vastavusse viimine.
-   Ken määrab juriidilise isiku jaoks valiku Päise vastavusse viimise oleku automaatne värskendamine suvandiks Jah.
-   Ken määrab juriidilise isiku jaoks välja Hinna kogusumma vastendamine väärtuseks Protsent ja sisestab kõikumise protsendiks 15%.
-   Ken määrab kauba tasemel kaubale 1500 – CNC Milicroni masin vastavusse viimise poliitikaks Kolmesuunaline vastavusse viimine. See kaup on põhivara kaup, mida Fabrikamis tootmiseks kasutatakse. Selle kauba arved vastendatakse ostutellimuse ridade hindade ja toote sissetulekute kogustega.
-   Tony sisestab taotluse viiele CNC Milicroni masinale. Alicia, kes on Fabrikami ostutellimuse ametnik, esitab Contoso nimelisele juriidilisele isikule ostutellimuse kaupade tarnimiseks.

    | Kaubakood                 | Kogus | Ühiku hind | Netosumma | Tasukood        | Tasude väärtus |
    |-----------------------------|----------|------------|------------|---------------------|---------------|
    | 1500 – CNC Milicroni masin | 5        | 8000,00   | 40 000,00  | Saatmine ja käsitsemine | 3000,00      |

-   Arnie, kes on Contoso müügireskontro ametnik, vaatab üle nädala saadetised. Arnie valib Fabrikamile CNC Milicroni masinate tarne eest arve esitamiseks saadetise kanded. Arnie lisab tasu saatmise ja käsitsemise eest. Fabrikam arvestab seda tasu osana vara kulust.

### <a name="scenario"></a>Stsenaarium

1.  Sammy, kes on Fabrikami vastuvõtu osakonna töötaja, saab Contoso saadetud masinate lõpliku koguse. Ta sisestab toote sissetuleku koguseks 5. Kuna ostutellimus on täielikult saadud, muutub ostutellimuse olekuks Saadud.
2.  April, Fabrikami ostureskontro koordinaator, sisestab ja kinnitab Contoso esitatud arve. Ta kontrollib järgmist teavet.
    -   Kolmesuunalist vastavusse viimist vajavate kaupade kogus arve real vastab saadud kogusele. Saadud kogus on näidatud arvega vastendatud toote sissetulekul.
    -   Kahe- või kolmesuunalist vastavusseviimist vajavate kaupade hinnad arve real jäävad Microsoft Dynamics 365 Financeis määratletud kõikumiste piiridesse. See hõlmab järgmisi hindade vastavusseviimise tüüpe.
        -   Ühiku netohinna vastavusse viimine – ühiku netohind arve real vastendub kõikumise protsendi piires ühiku netohinnale ostutellimuse real. Selles näites on lubatud ühiku netohinna kõikumine +8 protsenti.
        -   Koguhindade vastavusse viimine – netosumma arve real vastendub kõikumise protsendi, summa või protsendi ja summa piires netosummale ostutellimuse real. Selles näites on lubatud koguhindade vastavusse viimise kõikumine +15 protsenti.

Contoso paberarve sisaldab järgmist teavet.

| Kaup                        | Kogus | Ühiku hind | Netosumma |
|-----------------------------|----------|------------|------------|
| 1500 – CNC Milicroni masin | 5        | 8100,00   | 40,500.00  |
| Saatmine ja käsitsemine       |          |            | 4,000.00   |
| Maks                         |          |            | 0,00       |
| Kokku                       |          |            | 44,500.00  |

Arve rida sisaldab järgmist teavet.

| Kaubakood                 | Kogus | Ühiku hind | Rea netosumma | Vastavusse viimise poliitika    | Toote sissetuleku koguse vastendamine | Hinna vastendamine | Koguhinna vastendus |
|-----------------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| 1500 – CNC Milicroni masin | 5        | 8100,00   | 40 500,00       | Kolmesuunaline vastavusse viimine | Arvestatud                         | Arvestatud      | Arvestatud            |

Arve saab sisestada, kuna see rida läbib arvete vastavusse viimise protsessi.

## <a name="example-three-way-matching-for-item-and-vendor-combinations"></a> Näide: kauba ja hankija kombinatsioonide kolmesuunaline vastavusse viimine
Kokkuvõte: Ken on kontroller Fabrikami nimelise juriidilise isiku peakontoris. Ken otsustab, et kõik ostutellimustel põhinevad arved tuleks viia vastavusse ostutellimuse ridadega (kahesuunaline vastavusse viimine). Cassie on Fabrikami Malaisia allüksuse raamatupidaja. Ta määrab teatud Malaisia hankijatelt tellitud valitud kaupade vastavusse viimise nii ostutellimuse kui ka toote sissetuleku ridadega (kolmesuunaline vastavusse viimine). Ta saab ka tühistada vastavusse viimise poliitika, et kindlad ostutellimused vastendataks kõrgemal tasemel. 

Maht ja summad on väiksed ning mõne Malaisia hankija tarnega on olnud probleeme. Sellest tulenevalt määrab Cassie teatud Malaisias toodetud kaupade kauba ja hankija kombinatsioonide kontrollitaseme kolmesuunaliseks vastavusse viimiseks. 

Selles näites toodud arvete vastavusse viimise poliitikad aitavad järgmistes rollides inimestel järgmisi eesmärke täita.
-   Ken on ettevõtte Fabrikam kontroller. Ta saab aidata inimestel oma organisatsioonis hankijatelt kaupade (tooted ja teenused) tellimise, vastuvõtu ja maksmisega seotud probleeme tuvastada ja lahendada.
-   Cassie on Fabrikami Malaisia allüksuse raamatupidaja. Tema saab korporatiivset poliitikat kehtestada ja tagada, et arved makstakse alles pärast seda, kui need on ostutellimuse ridade ning tooteid ja teenuseid kajastava sissetulekuga toote sissetulekutel vastavusse viidud. Ta saab ka tegevuskulude kontrollimiseks kindlate kaupade kontrollitaseme kolmesuunaliseks vastavusse viimiseks suurendada.

### <a name="prerequisites"></a>Eeltingimused

-   Ken seadistab juriidilise isiku tasemel vastavusse viimise poliitikaks Kahesuunaline vastavusse viimine.
-   Ken määrab juriidilise isiku jaoks välja Hinna kogusumma vastendamine väärtuseks Protsent ja sisestab kõikumise protsendiks 10 protsenti.
-   Ken määrab kõigi kaupade ühiku hinna kõikumiseks 2 protsenti.
-   Cassie määrab kauba ja hankija kombinatsiooni tasemel kaubale PH2500 – arvuti ja hankija Contoso vastavusse viimise poliitikaks Kolmesuunaline vastavusse viimine.
-   Alicia, kes on Fabrikami Malaisia allüksuse ostutellimuse ametnik, esitab Contosole ostutellimused kolme kauba tarnimiseks, nagu on näidatud järgmises tabelis. Ostutellimust luues tühistab ta juhtmeta hiire puhul vastavusse viimise poliitika ja määrab kahesuunalise vastavusse viimise asemel kolmesuunalise.

    | Kaubakood           | Kogus | Ühiku hind | Netosumma | Vastavusse viimise poliitika (vaikesisestus) | Vastavusse viimise poliitika (ostutellimuse real) |
    |-----------------------|----------|------------|------------|---------------------------------|----------------------------------------------|
    | PH2500 – arvuti     | 2        | 2500,00   | 5000,00   | Kolmesuunaline vastavusse viimine              | Kolmesuunaline vastavusse viimine                           |
    | MM01 – juhtmeta hiir | 2        | 40,00      | 80,00      | Kahesuunaline vastavusse viimine                | Kolmesuunaline vastavusse viimine                           |
    | USB‑draiv             | 200      | 10,00      | 2000,00   | Kahesuunaline vastavusse viimine                | Kahesuunaline vastavusse viimine                             |

### <a name="scenario"></a>Stsenaarium

1.  Kaubad jõuavad kohale. Sammy, kes on Fabrikami Malaisia allüksuse vastuvõtu osakonna töötaja, töö katkestatakse ja ta ei sisesta kohe toote sissetulekut.
2.  April, Fabrikami ostureskontro koordinaator, sisestab ja kinnitab Contoso esitatud arve. Ta kontrollib järgmist teavet.
    -   Kolmesuunalist vastavusse viimist vajavate kaupade kogus arve real vastab saadud kogusele. Saadud kogus on näidatud arvega vastendatud toote sissetulekul.
    -   Kahe- või kolmesuunalist vastavusseviimist vajavate kaupade hinnad arve real jäävad määratletud kõikumiste piiridesse. See hõlmab järgmisi hindade vastavusseviimise tüüpe.
        -   Ühiku netohinna vastavusse viimine – ühiku netohind arve real vastendub kõikumise protsendi piires ühiku netohinnale ostutellimuse real. Selles näites on lubatud ühiku netohinna kõikumine +2 protsenti.
        -   Koguhindade vastavusse viimine – netosumma arve real vastendub kõikumise protsendi, summa või protsendi ja summa piires netosummale ostutellimuse real. Selles näites on lubatud koguhindade vastavusse viimise kõikumine +10 protsenti.

Contoso paberarve sisaldab järgmist teavet.

| Kaup                  | Kogus | Ühiku hind | Netosumma |
|-----------------------|----------|------------|------------|
| PH2500 – arvuti     | 2        | 2500,00   | 5000,00   |
| MM01 – juhtmeta hiir | 2        | 41.00      | 82.00      |
| USB‑draiv             | 200      | 10.05      | 2,010.00   |
| Arve kogusumma         |          |            | 7,092.00   |

Arve rida sisaldab järgmist teavet.

| Kaubakood           | Kogus | Ühiku hind | Rea netosumma | Vastavusse viimise poliitika    | Toote sissetuleku koguse vastendamine | Hinna vastendamine | Koguhinna vastendus |
|-----------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| PH2500 – arvuti     | 2        | 2500,00   | 5000,00        | Kolmesuunaline vastavusse viimine | Nurjunud                         | Arvestatud      | Arvestatud            |
| MM01 – juhtmeta hiir | 2        | 41,00      | 82,00           | Kolmesuunaline vastavusse viimine | Nurjunud                         | Nurjunud      | Arvestatud            |
| USB‑draiv             | 200      | 10,05      | 2010,00         | Kahesuunaline vastavusse viimine   |                                | Arvestatud      | Arvestatud            |

Pange tähele järgmisi kaupu.
-   PH2500 – arvuti rida. Toote sissetuleku koguse vastenduse veerul on hoiatusikoon, kuna arve rida ei ole toote sissetulekuga vastavusse viidud.
-   MM01 – traadita hiire rida. Toote sissetuleku koguse vastenduse veerul on hoiatusikoon, kuna arve rida ei ole toote sissetulekuga vastavusse viidud. Ühiku hinna vastenduse veerul on hoiatusikoon, kuna ühiku hinna kõikumine 2% on ületatud.
-   USB-draivi rea toote sissetuleku koguse vastenduse veerg on tühi, kuna kahesuunaline vastavusse viimine ei vasta arve rea ja toote sissetuleku rea kogustele.

Kui vastendamise lahknevustega arvete sisestamisel on nõutud kinnitus, tuleb enne, kui hinna ja koguse vastendamise vigadega arvet saab sisestada, määrata lehel Arve võrdlemise üksikasjad valik Kinnita ühtivate lahknevustega sisestamine. Kui kinnitamine ei ole kohustuslik, saab arve töötlemist muude sisestusvigade puudumisel jätkata.


Lisateabe saamiseks vaadake teemat [Ostureskontro arvete võrdlemise ülevaade](accounts-payable-invoice-matching.md).



