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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0017d13b7f7594462dfff4ef896f4139607d4bc5
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="income-statement-financial-report"></a><span data-ttu-id="b8ae9-104">Kasumiaruande finantsaruanne</span><span class="sxs-lookup"><span data-stu-id="b8ae9-104">Income statement financial report</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b8ae9-105">Selles artiklis kirjeldatakse kasumiaruannete vaikearuannet.</span><span class="sxs-lookup"><span data-stu-id="b8ae9-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="b8ae9-106">Samuti kirjeldatakse selle aruandega seotud koosteüksusi.</span><span class="sxs-lookup"><span data-stu-id="b8ae9-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="b8ae9-107">Kasumiaruande vaikearuanne</span><span class="sxs-lookup"><span data-stu-id="b8ae9-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="b8ae9-108">Vaikearuanne</span><span class="sxs-lookup"><span data-stu-id="b8ae9-108">Default report</span></span>             | <span data-ttu-id="b8ae9-109">Selle funktsioon</span><span class="sxs-lookup"><span data-stu-id="b8ae9-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ae9-110">Kasumiaruanne – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="b8ae9-110">Income Statement – Default</span></span> | <span data-ttu-id="b8ae9-111">Annab ülevaate organisatsiooni tulususest praeguse perioodi ja aasta puhul kuni praeguse kuupäevani.</span><span class="sxs-lookup"><span data-stu-id="b8ae9-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="b8ae9-112">Koosteüksused</span><span class="sxs-lookup"><span data-stu-id="b8ae9-112">Building blocks</span></span>
<span data-ttu-id="b8ae9-113">Kasumiaruande finantsaruanne kasutab järgmisi koosteüksusi.</span><span class="sxs-lookup"><span data-stu-id="b8ae9-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="b8ae9-114">Vaikearuanne</span><span class="sxs-lookup"><span data-stu-id="b8ae9-114">Default report</span></span>             | <span data-ttu-id="b8ae9-115">Rea definitsioon</span><span class="sxs-lookup"><span data-stu-id="b8ae9-115">Row definition</span></span>                     | <span data-ttu-id="b8ae9-116">Veeru määratlus</span><span class="sxs-lookup"><span data-stu-id="b8ae9-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="b8ae9-117">Kasumiaruanne – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="b8ae9-117">Income Statement - Default</span></span> | <span data-ttu-id="b8ae9-118">Kasumi koondaruanne – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="b8ae9-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="b8ae9-119">Perioodiline ja YTD – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="b8ae9-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="b8ae9-120">Rea definitsioon</span><span class="sxs-lookup"><span data-stu-id="b8ae9-120">Row definition</span></span>

<span data-ttu-id="b8ae9-121">Readefinitsioon Kasumi koondaruanne – vaikimisi sisaldab jaotist iga tavalise kasumiaruande osa puhul.</span><span class="sxs-lookup"><span data-stu-id="b8ae9-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="b8ae9-122">Põhikonto kategooria dimensiooni kasutatakse selle readefinitsiooni loomiseks.</span><span class="sxs-lookup"><span data-stu-id="b8ae9-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="b8ae9-123">Seega saab igaüks luua aruande ilma muudatusi tegemata.</span><span class="sxs-lookup"><span data-stu-id="b8ae9-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="b8ae9-124">Veeru definitsioon</span><span class="sxs-lookup"><span data-stu-id="b8ae9-124">Column Definition</span></span>

<span data-ttu-id="b8ae9-125">Veeru definitsioonid sisaldavad eri tüüpi veerge üksikasjade ja finantsandmete eri tasemete pakkumiseks.</span><span class="sxs-lookup"><span data-stu-id="b8ae9-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="b8ae9-126">**Perioodiline ja YTD – vaikimisi veerutüübid:**</span><span class="sxs-lookup"><span data-stu-id="b8ae9-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="b8ae9-127">**DESC** – kirjeldus readefinitsioonist</span><span class="sxs-lookup"><span data-stu-id="b8ae9-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="b8ae9-128">**FD** – praeguse perioodi finantsandmed</span><span class="sxs-lookup"><span data-stu-id="b8ae9-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="b8ae9-129">**FD** – finantsandmed aasta algusest praeguse kuupäevani</span><span class="sxs-lookup"><span data-stu-id="b8ae9-129">**FD** – Financial data for the year to date</span></span>

 

<a name="see-also"></a><span data-ttu-id="b8ae9-130">Vt ka</span><span class="sxs-lookup"><span data-stu-id="b8ae9-130">See also</span></span>
--------

[<span data-ttu-id="b8ae9-131">Finantsaruandlus</span><span class="sxs-lookup"><span data-stu-id="b8ae9-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="b8ae9-132">Finantsaruannete vaatamine</span><span class="sxs-lookup"><span data-stu-id="b8ae9-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="b8ae9-133">Dynamicsi finantsaruandluse ajaveeb</span><span class="sxs-lookup"><span data-stu-id="b8ae9-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




