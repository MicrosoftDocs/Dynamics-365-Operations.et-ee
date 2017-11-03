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

# <a name="income-statement-financial-report"></a><span data-ttu-id="19174-104">Kasumiaruande finantsaruanne</span><span class="sxs-lookup"><span data-stu-id="19174-104">Income statement financial report</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="19174-105">Selles artiklis kirjeldatakse kasumiaruannete vaikearuannet.</span><span class="sxs-lookup"><span data-stu-id="19174-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="19174-106">Samuti kirjeldatakse selle aruandega seotud koosteüksusi.</span><span class="sxs-lookup"><span data-stu-id="19174-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="19174-107">Kasumiaruande vaikearuanne</span><span class="sxs-lookup"><span data-stu-id="19174-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="19174-108">Vaikearuanne</span><span class="sxs-lookup"><span data-stu-id="19174-108">Default report</span></span>             | <span data-ttu-id="19174-109">Selle funktsioon</span><span class="sxs-lookup"><span data-stu-id="19174-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19174-110">Kasumiaruanne – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="19174-110">Income Statement – Default</span></span> | <span data-ttu-id="19174-111">Annab ülevaate organisatsiooni tulususest praeguse perioodi ja aasta puhul kuni praeguse kuupäevani.</span><span class="sxs-lookup"><span data-stu-id="19174-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="19174-112">Koosteüksused</span><span class="sxs-lookup"><span data-stu-id="19174-112">Building blocks</span></span>
<span data-ttu-id="19174-113">Kasumiaruande finantsaruanne kasutab järgmisi koosteüksusi.</span><span class="sxs-lookup"><span data-stu-id="19174-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="19174-114">Vaikearuanne</span><span class="sxs-lookup"><span data-stu-id="19174-114">Default report</span></span>             | <span data-ttu-id="19174-115">Rea definitsioon</span><span class="sxs-lookup"><span data-stu-id="19174-115">Row definition</span></span>                     | <span data-ttu-id="19174-116">Veeru määratlus</span><span class="sxs-lookup"><span data-stu-id="19174-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="19174-117">Kasumiaruanne – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="19174-117">Income Statement - Default</span></span> | <span data-ttu-id="19174-118">Kasumi koondaruanne – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="19174-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="19174-119">Perioodiline ja YTD – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="19174-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="19174-120">Rea definitsioon</span><span class="sxs-lookup"><span data-stu-id="19174-120">Row definition</span></span>

<span data-ttu-id="19174-121">Readefinitsioon Kasumi koondaruanne – vaikimisi sisaldab jaotist iga tavalise kasumiaruande osa puhul.</span><span class="sxs-lookup"><span data-stu-id="19174-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="19174-122">Põhikonto kategooria dimensiooni kasutatakse selle readefinitsiooni loomiseks.</span><span class="sxs-lookup"><span data-stu-id="19174-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="19174-123">Seega saab igaüks luua aruande ilma muudatusi tegemata.</span><span class="sxs-lookup"><span data-stu-id="19174-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="19174-124">Veeru definitsioon</span><span class="sxs-lookup"><span data-stu-id="19174-124">Column Definition</span></span>

<span data-ttu-id="19174-125">Veeru definitsioonid sisaldavad eri tüüpi veerge üksikasjade ja finantsandmete eri tasemete pakkumiseks.</span><span class="sxs-lookup"><span data-stu-id="19174-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="19174-126">**Perioodiline ja YTD – vaikimisi veerutüübid:**</span><span class="sxs-lookup"><span data-stu-id="19174-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="19174-127">**DESC** – kirjeldus readefinitsioonist</span><span class="sxs-lookup"><span data-stu-id="19174-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="19174-128">**FD** – praeguse perioodi finantsandmed</span><span class="sxs-lookup"><span data-stu-id="19174-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="19174-129">**FD** – finantsandmed aasta algusest praeguse kuupäevani</span><span class="sxs-lookup"><span data-stu-id="19174-129">**FD** – Financial data for the year to date</span></span>

 

<a name="see-also"></a><span data-ttu-id="19174-130">Vt ka</span><span class="sxs-lookup"><span data-stu-id="19174-130">See also</span></span>
--------

[<span data-ttu-id="19174-131">Finantsaruandlus</span><span class="sxs-lookup"><span data-stu-id="19174-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="19174-132">Finantsaruannete vaatamine</span><span class="sxs-lookup"><span data-stu-id="19174-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="19174-133">Dynamicsi finantsaruandluse ajaveeb</span><span class="sxs-lookup"><span data-stu-id="19174-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




