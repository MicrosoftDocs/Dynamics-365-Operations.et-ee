---
title: Bilansi finantsaruanded
description: "Selles artiklis kirjeldatakse bilansside vaikearuandeid. Samuti kirjeldatakse nende aruannetega seotud koosteüksusi."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 664d32c2bfecb50e24fd48a66ab5b34cef6c09a3
ms.lasthandoff: 03/31/2017


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




