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
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8ca90b949a1a2b5af4a0fd78ddf80d5add2565b9
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

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




