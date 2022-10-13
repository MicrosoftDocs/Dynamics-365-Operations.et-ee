---
title: Bilansi finantsaruanded
description: Selles artiklis kirjeldatakse bilansside vaikearuandeid. Samuti kirjeldatakse nende aruannetega seotud koosteüksusi.
author: jinniew
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: twheeloc
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4aad297f401143388d682da175a6b14727a8f2f0
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643819"
---
# <a name="balance-sheet-financial-reports"></a>Bilansi finantsaruanded

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse bilansside vaikearuandeid. Samuti kirjeldatakse nende aruannetega seotud koosteüksusi. 

## <a name="default-balance-sheet-reports"></a>Bilansi vaikearuanded

Bilansi vaikearuandeid on kaks. Ühes aruandes on jaotised virnastatud. Teises aruandes on jaotised kõrvuti.

| Vaikearuanne                       | Selle funktsioon                                                                                                                           |
|--------------------------------------|--------------------------------------------------------------------------------------|
| Bilanss – vaikimisi              | Annab ülevaate organisatsiooni aasta rahalisest seisust.                    |
| Bilanss ja tuluaruanne perioodide vahel – vaikimisi | Annab vaate organisatsiooni finantspositsioonist aastapoolelt. |

## <a name="building-blocks"></a>Koosteüksused
Bilansi finantsaruanded kasutavad järgmisi koosteüksusi.

| Vaikearuanne                       | Rea definitsioon                       | Veeru määratlus             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Bilanss – vaikimisi              | Bilanss – vaikimisi              | YTD ja hälve – vaikimisi    |
| Bilanss ja tuluaruanne perioodide vahel – vaikimisi | Bilanss ja tuluaruanne perioodide vahel – vaikimisi | Veerg Aasta tänaseni – vaikimisi |

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



## <a name="additional-resources"></a>Lisaressursid

[Finantsaruandluse ülevaade](financial-reporting-getting-started.md)

[Finantsaruannete vaatamine](view-financial-reports.md)

[Dynamicsi finantsaruandluse ajaveeb](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
