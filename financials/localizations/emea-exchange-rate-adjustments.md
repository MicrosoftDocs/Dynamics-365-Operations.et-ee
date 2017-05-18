---
title: Vahetuskursi korrigeerimine
description: "Selles teemas antakse teavet vahetuskursi korrigeerimise funktsiooni kohta kasutajatele Eestis, Ungaris, Tšehhi Vabariigis, Lätis, Leedus, Poolas ja Venemaal."
author: ShylaThompson
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Operations, Core
ms.custom: 272683
ms.assetid: cd1b9f11-4640-41a1-a114-222483333972
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 5becb8bcc5aa619edfc0ad2fdcd31a483d003f0a
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="exchange-rate-adjustments"></a>Vahetuskursi korrigeerimine

[!include[banner](../includes/banner.md)]


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

| Sündmus                                       | Kuupäev                             | Deebet/kreedit | Summad               | Pearaamatukonto    | Kande tüüp             | Sisestamistüüp       | Krediit | Parandus |
|---------------------------------------------|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
| Arve                                     | 1-dets-12                         | Debiteeri        | 10 000 CAD / 40 000 USD | MR                             | Arve                      | Kliendi saldo   |        |            |
| Arve                                     | 1-dets-12                         | Krediit       | 10 000 CAD / 40 000 USD | Vastas                         | Arve                      | Pearaamatu tööleht     | X      |            |
| Makse                                     | 3-jaan-13                         | Debiteeri        | 10 000 CAD / 42 000 USD | Vastas                         | Makse                      | Pearaamatu tööleht     |        |            |
| Makse                                     | 3-jaan-13                         | Krediit       | 10 000 CAD / 42 000 USD | MR                             | Makse                      | Kliendi saldo   | X      |            |
| Tasakaalustus                                  | 3. jaanuar 2013 (= maksekuupäev) | Debiteeri        | 0 CAD / 2000 USD       | MR                             | Klient                     | Vahetuskursi tulu |        |            |
| Tasakaalustus                                  | 3. jaanuar 2013 (= maksekuupäev) | Krediit       | 0 CAD / 2000 USD       | Valuuta realiseeritud korrigeeritud kasum   | Klient                     | Vahetuskursi tulu | X      |            |
| Ümberarvutamine (standardne meetod; kuupäev = 31. detsember 2012) | 31-dets-12           | Debiteeri        | 0 CAD / 5000 USD       | MR                             | Välisvaluuta ümberarvutamine | Vahetuskursi tulu |        |            |
| Ümberarvutamine (standardne meetod; kuupäev = 31. detsember 2012) | 31-dets-12           | Krediit       | 0 CAD / 5,000 USD       | Valuuta realiseerimata korrigeeritud kasum | Välisvaluuta ümberarvutamine | Vahetuskursi tulu | X      |            |
| Ümberarvutamine (standardne meetod; kuupäev = 31. detsember 2012) | 3-jaan-13            | Debiteeri        | 0 CAD / 5,000 USD       | MR                             | Välisvaluuta ümberarvutamine | Vahetuskursi tulu |        | X          |
| Ümberarvutamine (standardne meetod; kuupäev = 31. detsember 2012) | 3-jaan-13            | Krediit       | 0 CAD / 5000 USD       | Valuuta realiseerimata korrigeeritud kasum | Välisvaluuta ümberarvutamine | Vahetuskursi tulu | X      | X          |



Eelneva ümberarvutamise puhul pange tähele, et kirje 3. jaanuarist 2013 on selle kohal oleva kirje (31. detsembrist 2012) otsene tühistamine. Isegi pearaamatukontod ja sisestustüübid on samad. Samuti pange tähele, et seatud on lipp **Parandus**.
||||||||||
|-----------------------------------------------------------|----------|--------|-----------------|--------------------------------|------------------------------|--------------------|---|---|
|Ümberarvutamine (arve kuupäeva meetod; kuupäev = 1. jaanuar 2013)  | 1-jaan-13 | Debiteeri  | 0 CAD / 5000 USD | MR                             | Välisvaluuta ümberarvutamine | Vahetuskursi tulu |   | X |
| Ümberarvutamine (arve kuupäeva meetod; kuupäev = 1. jaanuar 2013) | 1-jaan-13 | Krediit | 0 CAD / 5000 USD | Valuuta realiseerimata korrigeeritud kasum | Välisvaluuta ümberarvutamine | Vahetuskursi tulu | X | X |
| Ümberarvutamine (arve kuupäeva meetod; kuupäev = 1. jaanuar 2013) | 3-jaan-13 | Debiteeri  | 0 CAD / 5000 USD | MR                             | Välisvaluuta ümberarvutamine | Vahetuskursi tulu |   |   |
| Ümberarvutamine (arve kuupäeva meetod; kuupäev = 1. jaanuar 2013) | 3-jaan-13 | Krediit | 0 CAD / 5000 USD | Valuuta realiseerimata korrigeeritud kasum | Välisvaluuta ümberarvutamine | Vahetuskursi tulu | X |   |

Eelneva ümberarvutamise puhul pange tähele, et kirje 1. jaanuarist 2013 on selle all oleva kirje (3. jaanuarist 2013) otsene tühistamine. Isegi pearaamatukontod ja sisestustüübid on samad. Samuti pange tähele, et seatud on lipp **Parandus**.

Süsteemi käitumine on sama, olenemata sellest, kas lehe **Pearaamatu parameetrid** jaotises **Pearaamatukanne** jaotises on suvandi **Parandus** sätteks valitud **Jah** või **Ei**.





