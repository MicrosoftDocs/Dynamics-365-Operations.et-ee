---
title: Bilansi finantsaruanded
description: "Selles artiklis kirjeldatakse bilansside vaikearuandeid. Samuti kirjeldatakse nende aruannetega seotud koosteüksusi."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6323a2bf40a853edff4b3cef31eea7e95542a92e
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="balance-sheet-financial-reports"></a>Bilansi finantsaruanded

[!include[banner](../includes/banner.md)]


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

 

<a name="see-also"></a>Vt ka
--------

[Finantsaruandlus](financial-reporting-getting-started.md)

[Finantsaruannete vaatamine](view-financial-reports.md)

[Dynamicsi finantsaruandluse ajaveeb](http://blogs.msdn.com/b/dynamics_financial_reporting/)




