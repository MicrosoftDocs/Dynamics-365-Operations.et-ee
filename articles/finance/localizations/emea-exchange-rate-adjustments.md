---
title: Vahetuskursi korrigeerimine
description: Selles teemas antakse teavet vahetuskursi korrigeerimise funktsiooni kohta kasutajatele Eestis, Ungaris, Tšehhi Vabariigis, Lätis, Leedus, Poolas ja Venemaal.
author: ShylaThompson
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 272683
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: bef2f06c9f7252e44037ddbf00b47d53f9af155a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252142"
---
# <a name="exchange-rate-adjustments"></a>Vahetuskursi korrigeerimine

[!include [banner](../includes/banner.md)]

Selles teemas antakse teavet vahetuskursi korrigeerimise funktsiooni kohta kasutajatele Eestis, Ungaris, Tšehhi Vabariigis, Lätis, Leedus, Poolas ja Venemaal.

Vahetuskursi korrigeerimise funktsioon Eesti, Ungari, Tšehhi Vabariigi, Läti, Leedu, Poola ja Venemaa jaoks sisaldab järgmisi müügireskontro ja ostureskontro jaoks asjakohaseid laiendusi.

-   Vahetuskursi korrigeerimise sisestusi saab tühistada algsete korrigeerimiste parandusena (negatiivsed summad).
-   Järjestikuste realiseerimata korrigeerimiste sisestamisel kasutatakse sama pearaamatu sisestuskontot ja kandetüüpi sõltumata sellest, kas korrigeerimised tähistavad kasumit või kahjumit.
-   Arvutatud vahetuskursi kasum sisestatakse alati kasumikontodele ja arvutatud vahetuskursi kahjum sisestatakse alati kulukontodele.

Juriidilised isikud, kelle esmane aadress on Tšehhi Vabariigis, saavad vahetuskursi korrigeerimiseks kasutada erimeetodit. Seda nimetatakse astmeliseks meetodiks. Kui see meetod on sisse lülitatud, ei rakendata praeguses funktsioonis kasutusele võetud muudatusi. Realiseeritud ja realiseerimata kasum või kahjum arvutatakse viimati kasutatud vahetuskursi suhtes. Algse summa asemel kasutatakse arvutamise alusena korrigeeritud summat. Vahetuskursi korrigeerimise astmelisele meetodile lülitumiseks valige lehel **Pearaamatu parameetrid** jaotises **Välisvaluuta ümberarvutamine** väljal **Arvutusmeetod** suvand **Astmeline**. Järgmises näites kirjeldatakse vahetuskursi korrigeerimise funktsiooni toimimise põhimõtet Eesti, Ungari, Tšehhi Vabariigi, Läti Leedu, Poola ja Venemaa puhul. Ettevõtte stsenaarium oleks näiteks järgmine.

-   1. detsembril 2012 on sisestatud välisvaluutas arve.
-   3. jaanuaril 2013 on sisestatud välisvaluutas makse.
-   Makse rakendamiseks arvele tehakse tasakaalustamine.
-   Vahetuskursi korrigeerimine toimub 31. detsembril 2012 (meetod = standardne).
-   Vahetuskursi korrigeerimine toimub 1. jaanuaril 2013 (meetod = arve kuupäev).

Selle näite puhul on Kanada dollari (CAD) ja USA dollari (USD) vahetuskursid järgmised.

-   1. detsember 2012: 400,000
-   31. detsember 2012: 450,0000
-   3. jaanuar 2013: 420,0000

### <a name="invoice"></a>Arve

| Kuupäev                             | Deebet/kreedit | Summad               | Pearaamatukonto    | Kande tüüp             | Sisestamistüüp       | Krediit | Parandus |
|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
| 1-dets-12                         | Debiteeri        | 10 000 CAD / 40 000 USD | MR                             | Arve                      | Kliendi saldo   |        |            |
| 1-dets-12                         | Krediit       | 10 000 CAD / 40 000 USD | Vastas                         | Arve                      | Pearaamatu tööleht     | X      |

### <a name="payment"></a>Makse

| Kuupäev                             | Deebet/kreedit | Summad               | Pearaamatukonto    | Kande tüüp             | Sisestamistüüp       | Krediit | Parandus |
|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
| 3-jaan-13                         | Debiteeri        | 10 000 CAD / 42 000 USD | Vastas                         | Makse                      | Pearaamatu tööleht     |        |            |
| 3-jaan-13                         | Krediit       | 10 000 CAD / 42 000 USD | MR                             | Makse                      | Kliendi saldo   | X      |            |

### <a name="settlement"></a>Tasakaalustus

| Kuupäev                             | Deebet/kreedit | Summad               | Pearaamatukonto    | Kande tüüp             | Sisestamistüüp       | Krediit | Parandus |
|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
|3. jaanuar 2013 (= maksekuupäev) | Debiteeri        | 0 CAD / 2000 USD       | MR                             | Klient                     | Vahetuskursi tulu |        |            |
3. jaanuar 2013 (= maksekuupäev) | Krediit       | 0 CAD / 2000 USD       | Valuuta realiseeritud korrigeeritud kasum   | Klient                     | Vahetuskursi tulu | X      |            |


### <a name="revaluation--standard-method-date--december-31-2012"></a>Ümberarvutamine (standardne meetod; kuupäev = 31. detsember 2012)
Selle ümberarvutamisnäite puhul pange tähele, et kirje 3. jaanuarist 2013 on 31. detsembrist 2012 pärineva kirje otsene tühistamine. Isegi pearaamatukontod ja sisestustüübid on samad. Samuti pange tähele, et seatud on lipp **Parandus**.

| Kuupäev                             | Deebet/kreedit | Summad               | Pearaamatukonto    | Kande tüüp             | Sisestamistüüp       | Krediit | Parandus |
|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
| 31-dets-12           | Debiteeri        | 0 CAD / 5000 USD       | MR                             | Välisvaluuta ümberarvutamine | Vahetuskursi tulu |        |            |
| 31-dets-12           | Krediit       | 0 CAD / 5000 USD       | Valuuta realiseerimata korrigeeritud kasum | Välisvaluuta ümberarvutamine | Vahetuskursi tulu | X      |            |
| 3-jaan-13            | Debiteeri        | 0 CAD / 5000 USD       | MR                             | Välisvaluuta ümberarvutamine | Vahetuskursi tulu |        | X          |
 3-jaan-13            | Krediit       | 0 CAD / 5000 USD       | Valuuta realiseerimata korrigeeritud kasum | Välisvaluuta ümberarvutamine | Vahetuskursi tulu | X      | X          |


### <a name="revaluation-invoice-date-method-date--january-1-2013"></a>Ümberarvutamine (arve kuupäeva meetod; kuupäev = 1. jaanuar 2013)
Selle ümberarvutamisnäite puhul pange tähele, et kirje 1. jaanuarist 2013 on 3. jaanuarist 2013 pärineva kirje otsene tühistamine. Isegi pearaamatukontod ja sisestustüübid on samad. Samuti pange tähele, et seatud on lipp **Parandus**.

| Kuupäev   | Deebet/kreedit | Summad | Pearaamatukonto| Kande tüüp| Sisestamistüüp| Krediit | Parandus |
|--------|--------------|---------|----------------------------|----------------|--------|------------|--------------|
|1-jaan-13 | Debiteeri  | 0 CAD / 5000 USD | MR                             | Välisvaluuta ümberarvutamine | Vahetuskursi tulu |   | X |
|1-jaan-13 | Krediit | 0 CAD / 5000 USD | Valuuta realiseerimata korrigeeritud kasum | Välisvaluuta ümberarvutamine | Vahetuskursi tulu | X | X |
|3-jaan-13 | Debiteeri  | 0 CAD / 5000 USD | MR                             | Välisvaluuta ümberarvutamine | Vahetuskursi tulu |   |   |
|3-jaan-13 | Krediit | 0 CAD / 5000 USD | Valuuta realiseerimata korrigeeritud kasum | Välisvaluuta ümberarvutamine | Vahetuskursi tulu | X |   |

Süsteemi käitumine on sama, olenemata sellest, kas lehe **Pearaamatu parameetrid** jaotises **Pearaamatukanne** jaotises on suvandi **Parandus** sätteks valitud **Jah** või **Ei**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]