--- 
title: "Kastiaruannete loomine ja nende lõppemine"
description: "Kasutage seda ülesandejuhendit valmisaruannete käitamiseks halduses erinevatest tööruumidest ning asukohas Päringud ja Müügiaruanded (jaotises Jaemüük ja Kaubandus)."
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: b42f86fc243312d18654b1a048f9dffb29afd187
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="b588d-103">Kastiaruannete loomine ja nende lõppemine</span><span class="sxs-lookup"><span data-stu-id="b588d-103">Generate and run out of box reports</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b588d-104">Kasutage seda ülesandejuhendit valmisaruannete käitamiseks halduses erinevatest tööruumidest ning asukohas Päringud ja Müügiaruanded (jaotises Jaemüük ja Kaubandus).</span><span class="sxs-lookup"><span data-stu-id="b588d-104">Use this task guide to run out of box reports in headquarters from different workspaces and Inquiries & Sales reports located under Retail & Commerce.</span></span>



<span data-ttu-id="b588d-105">Selle salvestise loomisel kasutati demoettevõtte USRT-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="b588d-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="b588d-106">See salvestis on mõeldud süsteemiadministraatori rollile.</span><span class="sxs-lookup"><span data-stu-id="b588d-106">This recording is intended for the System administrator role.</span></span>


## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="b588d-107">Aruannete käivitamine tööruumidest</span><span class="sxs-lookup"><span data-stu-id="b588d-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="b588d-108">Avage Jaemüük ja kaubandus > Tooted ja kategooriad > Kategooria- ja tootehaldus.</span><span class="sxs-lookup"><span data-stu-id="b588d-108">Go to Retail and commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="b588d-109">Klõpsake noolt jaotise Aruanded laiendamiseks või ahendamiseks.</span><span class="sxs-lookup"><span data-stu-id="b588d-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="b588d-110">Klõpsake suvandit Peamiste toodete aruanne.</span><span class="sxs-lookup"><span data-stu-id="b588d-110">Click Top products report.</span></span>
4. <span data-ttu-id="b588d-111">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="b588d-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="b588d-112">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="b588d-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="b588d-113">Klõpsake väljal Kanal otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b588d-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="b588d-114">Valige puul suvand Contoso Retail\Contoso Retail USA\Central\Houston.</span><span class="sxs-lookup"><span data-stu-id="b588d-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="b588d-115">See näitab jaemüügi organisatsiooni vaikehierarhiat jaemüügi aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="b588d-115">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="b588d-116">Minge jaotisse Organisatsioonihaldus >Organisatsioonid > Organisatsioonihierarhia eesmärgid, valige suvand Jaemüügi aruandlus ja kontrollige jaotises Määratud hierarhiad hierarhia nime, mille puhul on veerg Vaikimisi märgitud.</span><span class="sxs-lookup"><span data-stu-id="b588d-116">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="b588d-117">Selle ülesandesalvestise jaoks kasutatud demoandmete osana märkate, et jaemüügi aruandluse jaoks on organisatsiooni vaikehierarhiaks valitud Jaekauplused piirkonniti.</span><span class="sxs-lookup"><span data-stu-id="b588d-117">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
8. <span data-ttu-id="b588d-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b588d-118">Click OK.</span></span>
9. <span data-ttu-id="b588d-119">Valige suvand väljal Kuva.</span><span class="sxs-lookup"><span data-stu-id="b588d-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="b588d-120">Valige suvand väljal Alus.</span><span class="sxs-lookup"><span data-stu-id="b588d-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="b588d-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b588d-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a><span data-ttu-id="b588d-122">Saate käivitada päringute aruanded ja müügiaruanded, mis asuvad rakenduse Jaemüük ja kaubandus lingi all.</span><span class="sxs-lookup"><span data-stu-id="b588d-122">Launch reports from the inquiries and sales reports located under Retail & Commerce app link.</span></span>
1. <span data-ttu-id="b588d-123">Avage Jaemüük ja kaubandus > Päringud ja aruanded > Müügiaruanded > Kategooria müügiaruanded.</span><span class="sxs-lookup"><span data-stu-id="b588d-123">Go to Retail and commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="b588d-124">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="b588d-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="b588d-125">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="b588d-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="b588d-126">Klõpsake väljal Kanal otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b588d-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b588d-127">Valige puul suvand Contoso Retail\Contoso Retail USA\West\Seattle.</span><span class="sxs-lookup"><span data-stu-id="b588d-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="b588d-128">See näitab jaemüügi organisatsiooni vaikehierarhiat jaemüügi aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="b588d-128">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="b588d-129">Minge jaotisse Organisatsioonihaldus >Organisatsioonid > Organisatsioonihierarhia eesmärgid, valige suvand Jaemüügi aruandlus ja kontrollige jaotises Määratud hierarhiad hierarhia nime, mille puhul on veerg Vaikimisi märgitud.</span><span class="sxs-lookup"><span data-stu-id="b588d-129">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="b588d-130">Selle ülesandesalvestise jaoks kasutatud demoandmete osana märkate, et jaemüügi aruandluse jaoks on organisatsiooni vaikehierarhiaks valitud Jaekauplused piirkonniti.</span><span class="sxs-lookup"><span data-stu-id="b588d-130">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
6. <span data-ttu-id="b588d-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b588d-131">Click OK.</span></span>
7. <span data-ttu-id="b588d-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b588d-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="b588d-133">HQ aruannete eksportimine</span><span class="sxs-lookup"><span data-stu-id="b588d-133">Export an HQ reports</span></span>
1. <span data-ttu-id="b588d-134">Avage Jaemüük ja kaubandus > Päringud ja aruanded > Müügiaruanded > Organisatsiooni müügiaruanded.</span><span class="sxs-lookup"><span data-stu-id="b588d-134">Go to Retail and commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="b588d-135">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="b588d-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="b588d-136">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="b588d-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="b588d-137">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b588d-137">Click OK.</span></span>
5. <span data-ttu-id="b588d-138">Klõpsake suvandit Ekspordi.</span><span class="sxs-lookup"><span data-stu-id="b588d-138">Click Export.</span></span>
6. <span data-ttu-id="b588d-139">Klõpsake suvandit PDF.</span><span class="sxs-lookup"><span data-stu-id="b588d-139">Click PDF.</span></span>


