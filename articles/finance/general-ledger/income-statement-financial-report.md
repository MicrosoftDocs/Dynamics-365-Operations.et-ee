---
title: Kasumiaruande finantsaruanne
description: Selles artiklis kirjeldatakse kasumiaruannete vaikearuannet. Samuti kirjeldatakse selle aruandega seotud koosteüksusi.
author: jcart1106
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9a1f20ed5e2a84e0d18101ede46ffffef4230c7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868456"
---
# <a name="income-statement-financial-report"></a>Kasumiaruande finantsaruanne

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse kasumiaruannete vaikearuannet. Samuti kirjeldatakse selle aruandega seotud koosteüksusi. 

## <a name="default-income-statement-report"></a>Kasumiaruande vaikearuanne

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



## <a name="additional-resources"></a>Lisaressursid

[Finantsaruandluse ülevaade](financial-reporting-getting-started.md)

[Finantsaruannete vaatamine](view-financial-reports.md)

[Dynamicsi finantsaruandluse ajaveeb](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
