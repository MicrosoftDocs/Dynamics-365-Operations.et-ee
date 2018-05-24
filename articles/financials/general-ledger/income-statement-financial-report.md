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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9310508082ff710cd040b74519044f5a90c23988
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="income-statement-financial-report"></a><span data-ttu-id="6a79d-104">Kasumiaruande finantsaruanne</span><span class="sxs-lookup"><span data-stu-id="6a79d-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a79d-105">Selles artiklis kirjeldatakse kasumiaruannete vaikearuannet.</span><span class="sxs-lookup"><span data-stu-id="6a79d-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="6a79d-106">Samuti kirjeldatakse selle aruandega seotud koosteüksusi.</span><span class="sxs-lookup"><span data-stu-id="6a79d-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="6a79d-107">Kasumiaruande vaikearuanne</span><span class="sxs-lookup"><span data-stu-id="6a79d-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="6a79d-108">Vaikearuanne</span><span class="sxs-lookup"><span data-stu-id="6a79d-108">Default report</span></span>             | <span data-ttu-id="6a79d-109">Selle funktsioon</span><span class="sxs-lookup"><span data-stu-id="6a79d-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a79d-110">Kasumiaruanne – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="6a79d-110">Income Statement – Default</span></span> | <span data-ttu-id="6a79d-111">Annab ülevaate organisatsiooni tulususest praeguse perioodi ja aasta puhul kuni praeguse kuupäevani.</span><span class="sxs-lookup"><span data-stu-id="6a79d-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="6a79d-112">Koosteüksused</span><span class="sxs-lookup"><span data-stu-id="6a79d-112">Building blocks</span></span>
<span data-ttu-id="6a79d-113">Kasumiaruande finantsaruanne kasutab järgmisi koosteüksusi.</span><span class="sxs-lookup"><span data-stu-id="6a79d-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="6a79d-114">Vaikearuanne</span><span class="sxs-lookup"><span data-stu-id="6a79d-114">Default report</span></span>             | <span data-ttu-id="6a79d-115">Rea definitsioon</span><span class="sxs-lookup"><span data-stu-id="6a79d-115">Row definition</span></span>                     | <span data-ttu-id="6a79d-116">Veeru määratlus</span><span class="sxs-lookup"><span data-stu-id="6a79d-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="6a79d-117">Kasumiaruanne – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="6a79d-117">Income Statement - Default</span></span> | <span data-ttu-id="6a79d-118">Kasumi koondaruanne – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="6a79d-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="6a79d-119">Perioodiline ja YTD – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="6a79d-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="6a79d-120">Rea definitsioon</span><span class="sxs-lookup"><span data-stu-id="6a79d-120">Row definition</span></span>

<span data-ttu-id="6a79d-121">Readefinitsioon Kasumi koondaruanne – vaikimisi sisaldab jaotist iga tavalise kasumiaruande osa puhul.</span><span class="sxs-lookup"><span data-stu-id="6a79d-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="6a79d-122">Põhikonto kategooria dimensiooni kasutatakse selle readefinitsiooni loomiseks.</span><span class="sxs-lookup"><span data-stu-id="6a79d-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="6a79d-123">Seega saab igaüks luua aruande ilma muudatusi tegemata.</span><span class="sxs-lookup"><span data-stu-id="6a79d-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="6a79d-124">Veeru definitsioon</span><span class="sxs-lookup"><span data-stu-id="6a79d-124">Column Definition</span></span>

<span data-ttu-id="6a79d-125">Veeru definitsioonid sisaldavad eri tüüpi veerge üksikasjade ja finantsandmete eri tasemete pakkumiseks.</span><span class="sxs-lookup"><span data-stu-id="6a79d-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="6a79d-126">**Perioodiline ja YTD – vaikimisi veerutüübid:**</span><span class="sxs-lookup"><span data-stu-id="6a79d-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="6a79d-127">**DESC** – kirjeldus readefinitsioonist</span><span class="sxs-lookup"><span data-stu-id="6a79d-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="6a79d-128">**FD** – praeguse perioodi finantsandmed</span><span class="sxs-lookup"><span data-stu-id="6a79d-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="6a79d-129">**FD** – finantsandmed aasta algusest praeguse kuupäevani</span><span class="sxs-lookup"><span data-stu-id="6a79d-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="6a79d-130">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6a79d-130">Additional resources</span></span>
--------

[<span data-ttu-id="6a79d-131">Finantsaruandlus</span><span class="sxs-lookup"><span data-stu-id="6a79d-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="6a79d-132">Finantsaruannete vaatamine</span><span class="sxs-lookup"><span data-stu-id="6a79d-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="6a79d-133">Dynamicsi finantsaruandluse ajaveeb</span><span class="sxs-lookup"><span data-stu-id="6a79d-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




