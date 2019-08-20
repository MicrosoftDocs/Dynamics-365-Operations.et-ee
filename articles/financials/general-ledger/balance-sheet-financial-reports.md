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
ms.openlocfilehash: d9dcac902118c643b9a9d783c12f02fa5c90827b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839565"
---
# <a name="balance-sheet-financial-reports"></a><span data-ttu-id="4d06b-104">Bilansi finantsaruanded</span><span class="sxs-lookup"><span data-stu-id="4d06b-104">Balance sheet financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d06b-105">Selles artiklis kirjeldatakse bilansside vaikearuandeid.</span><span class="sxs-lookup"><span data-stu-id="4d06b-105">This article describes the default reports for balance sheets.</span></span> <span data-ttu-id="4d06b-106">Samuti kirjeldatakse nende aruannetega seotud koosteüksusi.</span><span class="sxs-lookup"><span data-stu-id="4d06b-106">It also describes the building blocks that are associated with these reports.</span></span> 

<a name="default-balance-sheet-reports"></a><span data-ttu-id="4d06b-107">Bilansi vaikearuanded</span><span class="sxs-lookup"><span data-stu-id="4d06b-107">Default balance sheet reports</span></span>
-----------------------------

<span data-ttu-id="4d06b-108">Bilansi vaikearuandeid on kaks.</span><span class="sxs-lookup"><span data-stu-id="4d06b-108">There are two default balance sheet reports.</span></span> <span data-ttu-id="4d06b-109">Ühes aruandes on jaotised virnastatud.</span><span class="sxs-lookup"><span data-stu-id="4d06b-109">On one report, the sections are stacked.</span></span> <span data-ttu-id="4d06b-110">Teises aruandes on jaotised kõrvuti.</span><span class="sxs-lookup"><span data-stu-id="4d06b-110">On the other report, the sections are side by side.</span></span>

| <span data-ttu-id="4d06b-111">Vaikearuanne</span><span class="sxs-lookup"><span data-stu-id="4d06b-111">Default report</span></span>                       | <span data-ttu-id="4d06b-112">Selle funktsioon</span><span class="sxs-lookup"><span data-stu-id="4d06b-112">What it does</span></span>                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d06b-113">Bilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="4d06b-113">Balance Sheet – Default</span></span>              | <span data-ttu-id="4d06b-114">Annab ülevaate organisatsiooni aasta rahalisest seisust.</span><span class="sxs-lookup"><span data-stu-id="4d06b-114">Provides a view of the organization's financial position for the year.</span></span>                                                                 |
| <span data-ttu-id="4d06b-115">Kõrvuti bilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="4d06b-115">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="4d06b-116">Annab ülevaate organisatsiooni aasta rahalisest seisust.</span><span class="sxs-lookup"><span data-stu-id="4d06b-116">Provides a view of the organization's financial position for the year.</span></span> <span data-ttu-id="4d06b-117">Varad ja kohustused ja omakapital on kõrvuti.</span><span class="sxs-lookup"><span data-stu-id="4d06b-117">Assets and liability and shareholder’s equity are side by side.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="4d06b-118">Koosteüksused</span><span class="sxs-lookup"><span data-stu-id="4d06b-118">Building blocks</span></span>
<span data-ttu-id="4d06b-119">Bilansi finantsaruanded kasutavad järgmisi koosteüksusi.</span><span class="sxs-lookup"><span data-stu-id="4d06b-119">The balance sheet financial reports use the following building blocks.</span></span>

| <span data-ttu-id="4d06b-120">Vaikearuanne</span><span class="sxs-lookup"><span data-stu-id="4d06b-120">Default report</span></span>                       | <span data-ttu-id="4d06b-121">Rea definitsioon</span><span class="sxs-lookup"><span data-stu-id="4d06b-121">Row definition</span></span>                       | <span data-ttu-id="4d06b-122">Veeru määratlus</span><span class="sxs-lookup"><span data-stu-id="4d06b-122">Column definition</span></span>             |
|--------------------------------------|--------------------------------------|-------------------------------|
| <span data-ttu-id="4d06b-123">Bilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="4d06b-123">Balance Sheet - Default</span></span>              | <span data-ttu-id="4d06b-124">Bilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="4d06b-124">Balance Sheet - Default</span></span>              | <span data-ttu-id="4d06b-125">YTD ja hälve – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="4d06b-125">YTD and Variance - Default</span></span>    |
| <span data-ttu-id="4d06b-126">Kõrvuti bilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="4d06b-126">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="4d06b-127">Kõrvuti bilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="4d06b-127">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="4d06b-128">Veerg Aasta tänaseni – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="4d06b-128">Year to Date Column - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="4d06b-129">Rea definitsioon</span><span class="sxs-lookup"><span data-stu-id="4d06b-129">Row definition</span></span>

<span data-ttu-id="4d06b-130">Mõlema bilansiaruande rea definitsioonid sisaldavad jaotisi iga tavalise bilansi osa puhul.</span><span class="sxs-lookup"><span data-stu-id="4d06b-130">The row definitions for both balance sheet reports contain sections for each part of a traditional balance sheet.</span></span> <span data-ttu-id="4d06b-131">Kõrvutiaruanne sisaldab veerupiiri, nii et kohustus ja omakapital kuvatakse varade kõrval.</span><span class="sxs-lookup"><span data-stu-id="4d06b-131">The side-by-side report includes a column break, so that liability and the owner’s equity appear next to assets.</span></span> <span data-ttu-id="4d06b-132">Põhikonto kategooria dimensiooni kasutatakse mõlema readefinitsiooni loomiseks.</span><span class="sxs-lookup"><span data-stu-id="4d06b-132">The Main Account Category dimension is used to build both row definitions.</span></span> <span data-ttu-id="4d06b-133">Seega saab igaüks luua aruanded ilma muudatusi tegemata.</span><span class="sxs-lookup"><span data-stu-id="4d06b-133">Therefore, anyone can generate the reports without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="4d06b-134">Veeru määratlus</span><span class="sxs-lookup"><span data-stu-id="4d06b-134">Column definition</span></span>

<span data-ttu-id="4d06b-135">Veeru definitsioonid sisaldavad eri tüüpi veerge üksikasjade ja finantsandmete eri tasemete pakkumiseks.</span><span class="sxs-lookup"><span data-stu-id="4d06b-135">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="4d06b-136">**YTD ja hälve – vaikimisi veerutüübid:**</span><span class="sxs-lookup"><span data-stu-id="4d06b-136">**YTD and Variance – Default column types:**</span></span>
    -   <span data-ttu-id="4d06b-137">**DESC** – kirjeldus readefinitsioonist</span><span class="sxs-lookup"><span data-stu-id="4d06b-137">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="4d06b-138">**FD** – jooksva aasta finantsandmed aasta algusest praeguse kuupäevani</span><span class="sxs-lookup"><span data-stu-id="4d06b-138">**FD** – Year-to-date financial data for the current year</span></span>
    -   <span data-ttu-id="4d06b-139">**FD** – möödunud aasta finantsandmed aasta algusest praeguse kuupäevani</span><span class="sxs-lookup"><span data-stu-id="4d06b-139">**FD** – Year-to-date financial data for the last year</span></span>
    -   <span data-ttu-id="4d06b-140">**CALC** – hälve möödunud aasta jooksvast aastast lahutamisest</span><span class="sxs-lookup"><span data-stu-id="4d06b-140">**CALC** – The variance from subtracting last year from this year</span></span>

<!-- -->

-   <span data-ttu-id="4d06b-141">**Veerg Aasta tänaseni – vaikimisi:**</span><span class="sxs-lookup"><span data-stu-id="4d06b-141">**Year to Date Column – Default:**</span></span>
    -   <span data-ttu-id="4d06b-142">**DESC** – kirjeldus readefinitsioonist</span><span class="sxs-lookup"><span data-stu-id="4d06b-142">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="4d06b-143">**FD** – jooksva aasta finantsandmed aasta algusest praeguse kuupäevani</span><span class="sxs-lookup"><span data-stu-id="4d06b-143">**FD** – Year-to-date financial data for the current year</span></span>



<a name="additional-resources"></a><span data-ttu-id="4d06b-144">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4d06b-144">Additional resources</span></span>
--------

[<span data-ttu-id="4d06b-145">Finantsaruandlus</span><span class="sxs-lookup"><span data-stu-id="4d06b-145">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="4d06b-146">Finantsaruannete vaatamine</span><span class="sxs-lookup"><span data-stu-id="4d06b-146">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="4d06b-147">Dynamicsi finantsaruandluse ajaveeb</span><span class="sxs-lookup"><span data-stu-id="4d06b-147">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



