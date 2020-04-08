---
title: Kastiaruannete loomine ja nende lõppemine
description: Kasutage seda tegevuse juhist valmisaruannete käitamiseks Headquartersis erinevatest tööruumidest ja asukohas Päringud ja Müügiaruanded, mis asuvad rakenduses Commerce.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d148fa36a116860af8c44043d90759b8a2d76fb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140757"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="fe0ee-103">Kastiaruannete loomine ja nende lõppemine</span><span class="sxs-lookup"><span data-stu-id="fe0ee-103">Generate and run out of box reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe0ee-104">Kasutage seda tegevuse juhist valmisaruannete käitamiseks Headquartersis erinevatest tööruumidest ja asukohas Päringud ja Müügiaruanded, mis asuvad rakenduses Commerce.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="fe0ee-105">Selle salvestise loomisel kasutati demoettevõtte USRT-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="fe0ee-106">See salvestis on mõeldud süsteemiadministraatori rollile.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="fe0ee-107">Aruannete käivitamine tööruumidest</span><span class="sxs-lookup"><span data-stu-id="fe0ee-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="fe0ee-108">Avage Jaemüük ja kaubandus > Tooted ja kategooriad > Kategooria- ja tootehaldus.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="fe0ee-109">Klõpsake noolt jaotise Aruanded laiendamiseks või ahendamiseks.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="fe0ee-110">Klõpsake suvandit Peamiste toodete aruanne.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-110">Click Top products report.</span></span>
4. <span data-ttu-id="fe0ee-111">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="fe0ee-112">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="fe0ee-113">Klõpsake väljal Kanal otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="fe0ee-114">Valige puul suvand Contoso Retail\Contoso Retail USA\Central\Houston.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="fe0ee-115">See näitab organisatsiooni vaikehierarhiat Commerce’i aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="fe0ee-116">Minge jaotisse Organisatsioonihaldus > Organisatsioonid > Organisatsioonihierarhia eesmärgid, valige suvand Kaubanduse aruandlus ja kontrollige jaotises Määratud hierarhiad hierarhia nime, mille puhul on veerg Vaikimisi märgitud.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="fe0ee-117">Selle tegevuse salvestise jaoks kasutatud demoandmete osana märkate, et aruandluse jaoks on organisatsiooni vaikehierarhiaks valitud Kauplused piirkonniti.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="fe0ee-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-118">Click OK.</span></span>
9. <span data-ttu-id="fe0ee-119">Valige suvand väljal Kuva.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="fe0ee-120">Valige suvand väljal Alus.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="fe0ee-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="fe0ee-122">Aruannete käivitamine päringutest ja müügiaruannetest</span><span class="sxs-lookup"><span data-stu-id="fe0ee-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="fe0ee-123">Avage Jaemüük ja kaubandus > Päringud ja aruanded > Müügiaruanded > Kategooria müügiaruanded.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="fe0ee-124">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="fe0ee-125">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="fe0ee-126">Klõpsake väljal Kanal otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="fe0ee-127">Valige puul suvand Contoso Retail\Contoso Retail USA\West\Seattle.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="fe0ee-128">See näitab organisatsiooni vaikehierarhiat Commerce’i aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="fe0ee-129">Minge jaotisse Organisatsioonihaldus > Organisatsioonid > Organisatsioonihierarhia eesmärgid, valige suvand Kaubanduse aruandlus ja kontrollige jaotises Määratud hierarhiad hierarhia nime, mille puhul on veerg Vaikimisi märgitud.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="fe0ee-130">Selle tegevuse salvestise jaoks kasutatud demoandmete osana märkate, et aruandluse jaoks on organisatsiooni vaikehierarhiaks valitud Kauplused piirkonniti.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="fe0ee-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-131">Click OK.</span></span>
7. <span data-ttu-id="fe0ee-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="fe0ee-133">HQ aruannete eksportimine</span><span class="sxs-lookup"><span data-stu-id="fe0ee-133">Export an HQ reports</span></span>
1. <span data-ttu-id="fe0ee-134">Avage Jaemüük ja kaubandus > Päringud ja aruanded > Müügiaruanded > Organisatsiooni müügiaruanded.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="fe0ee-135">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="fe0ee-136">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="fe0ee-137">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-137">Click OK.</span></span>
5. <span data-ttu-id="fe0ee-138">Klõpsake suvandit Ekspordi.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-138">Click Export.</span></span>
6. <span data-ttu-id="fe0ee-139">Klõpsake suvandit PDF.</span><span class="sxs-lookup"><span data-stu-id="fe0ee-139">Click PDF.</span></span>

