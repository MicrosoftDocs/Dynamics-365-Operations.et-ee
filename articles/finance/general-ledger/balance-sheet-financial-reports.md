---
title: Bilansi finantsaruanded
description: Selles artiklis kirjeldatakse bilansside vaikearuandeid. Samuti kirjeldatakse nende aruannetega seotud koosteüksusi.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e96552447182f3692a19d4cfd962afbcb28e5508
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442435"
---
# <a name="balance-sheet-financial-reports"></a>Bilansi finantsaruanded

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse bilansside vaikearuandeid. Samuti kirjeldatakse nende aruannetega seotud koosteüksusi. 

<a name="default-balance-sheet-reports"></a>Bilansi vaikearuanded
-----------------------------

Bilansi vaikearuandeid on kaks. Ühes aruandes on jaotised virnastatud. Teises aruandes on jaotised kõrvuti.

| Vaikearuanne                       | Selle funktsioon                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Bilanss – vaikimisi              | Annab ülevaate organisatsiooni aasta rahalisest seisust.                                                                 |
| Kõrvuti bilanss – vaikimisi | Annab ülevaate organisatsiooni aasta rahalisest seisust. Varad ja kohustused ja omakapital on kõrvuti. |

## <a name="building-blocks"></a>Koosteüksused
Bilansi finantsaruanded kasutavad järgmisi koosteüksusi.

| Vaikearuanne                       | Rea definitsioon                       | Veeru määratlus             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Bilanss – vaikimisi              | Bilanss – vaikimisi              | YTD ja hälve – vaikimisi    |
| Kõrvuti bilanss – vaikimisi | Kõrvuti bilanss – vaikimisi | Veerg Aasta tänaseni – vaikimisi |

### <a name="row-definition"></a>Rea definitsioon

Mõlema bilansiaruande rea definitsioonid sisaldavad jaotisi iga tavalise bilansi osa puhul. Kõrvutiaruanne sisaldab veerupiiri, nii et kohustus ja omakapital kuvatakse varade kõrval. Põhikonto kategooria dimensiooni kasutatakse mõlema readefinitsiooni loomiseks. Seega saab igaüks luua aruanded ilma muudatusi tegemata.

### <a name="column-definition"></a>Veeru määratlus

Veeru definitsioonid sisaldavad eri tüüpi veerge üksikasjade ja finantsandmete eri tasemete pakkumiseks.

-   **YTD ja hälve – vaikimisi veerutüübid:**
    -   **DESC** – kirjeldus readefinitsioonist
    -   **FD** – jooksva aasta finantsandmed aasta algusest praeguse kuupäevani
    -   **FD** – möödunud aasta finantsandmed aasta algusest praeguse kuupäevani
    -   **CALC** – hälve möödunud aasta jooksvast aastast lahutamisest

<!-- -->

-   **Veerg Aasta tänaseni – vaikimisi:**
    -   **DESC** – kirjeldus readefinitsioonist
    -   **FD** – jooksva aasta finantsandmed aasta algusest praeguse kuupäevani



<a name="additional-resources"></a>Lisaressursid
--------

[Finantsaruandluse ülevaade](financial-reporting-getting-started.md)

[Finantsaruannete vaatamine](view-financial-reports.md)

[Dynamicsi finantsaruandluse ajaveeb](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]