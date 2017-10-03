---
title: Kasumiaruande finantsaruanne
description: "Selles artiklis kirjeldatakse kasumiaruannete vaikearuannet. Samuti kirjeldatakse selle aruandega seotud koosteüksusi."
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
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: f07aea0b87bc3e09982f9ba248d3c28540fd2dc5
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017

---

# <a name="income-statement-financial-report"></a>Kasumiaruande finantsaruanne

[!include[banner](../includes/banner.md)]


Selles artiklis kirjeldatakse kasumiaruannete vaikearuannet. Samuti kirjeldatakse selle aruandega seotud koosteüksusi. 

<a name="default-income-statement-report"></a>Kasumiaruande vaikearuanne
-------------------------------

| Vaikearuanne             | Selle funktsioon                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| Kasumiaruanne – vaikimisi | Annab ülevaate organisatsiooni tulususest praeguse perioodi ja aasta puhul kuni praeguse kuupäevani. |

## <a name="building-blocks"></a>Koosteüksused
Kasumiaruande finantsaruanne kasutab järgmisi koosteüksusi.

| Vaikearuanne             | Rea definitsioon                     | Veeru määratlus          |
|----------------------------|------------------------------------|----------------------------|
| Kasumiaruanne – vaikimisi | Kasumi koondaruanne – vaikimisi | Perioodiline ja YTD – vaikimisi |

### <a name="row-definition"></a>Rea definitsioon

Readefinitsioon Kasumi koondaruanne – vaikimisi sisaldab jaotist iga tavalise kasumiaruande osa puhul. Põhikonto kategooria dimensiooni kasutatakse selle readefinitsiooni loomiseks. Seega saab igaüks luua aruande ilma muudatusi tegemata.

### <a name="column-definition"></a>Veeru definitsioon

Veeru definitsioonid sisaldavad eri tüüpi veerge üksikasjade ja finantsandmete eri tasemete pakkumiseks.

-   **Perioodiline ja YTD – vaikimisi veerutüübid:**
    -   **DESC** – kirjeldus readefinitsioonist
    -   **FD** – praeguse perioodi finantsandmed
    -   **FD** – finantsandmed aasta algusest praeguse kuupäevani

 

<a name="see-also"></a>Vt ka
--------

[Finantsaruandlus](financial-reporting-getting-started.md)

[Finantsaruannete vaatamine](view-financial-reports.md)

[Dynamicsi finantsaruandluse ajaveeb](http://blogs.msdn.com/b/dynamics_financial_reporting/)




