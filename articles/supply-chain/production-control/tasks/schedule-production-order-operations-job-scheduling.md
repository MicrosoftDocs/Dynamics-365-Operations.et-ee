---
title: Tootmistellimuse plaanimine koos toimingute ja tööde plaanimisega
description: See protseduur keskendub tootmistellimuse planeerimisele koos toimingute ja töö planeerimisega.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 00698e9cd2ed0481e5fed301c8a8c2e98690a5db
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2019
ms.locfileid: "352455"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="65098-103">Tootmistellimuse plaanimine koos toimingute ja tööde plaanimisega</span><span class="sxs-lookup"><span data-stu-id="65098-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="65098-104">See protseduur keskendub tootmistellimuse planeerimisele koos toimingute ja töö planeerimisega.</span><span class="sxs-lookup"><span data-stu-id="65098-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="65098-105">Toimingute planeerimisega ei looda ühtegi tööd, samas kui töö planeerimisega luuakse tööd.</span><span class="sxs-lookup"><span data-stu-id="65098-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="65098-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="65098-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="65098-107">See protseduur on mõeldud diskreetses tootmiskeskkonnas töötavale tootmisjuhile, tootmise planeerijale või tööde järelevaatajale.</span><span class="sxs-lookup"><span data-stu-id="65098-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="65098-108">Tootmistellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="65098-108">Create a production order</span></span>
1. <span data-ttu-id="65098-109">Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="65098-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="65098-110">Klõpsake valikut Uus tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="65098-110">Click New production order.</span></span>
3. <span data-ttu-id="65098-111">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="65098-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="65098-112">Valige kaubakood D0001.</span><span class="sxs-lookup"><span data-stu-id="65098-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="65098-113">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="65098-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="65098-114">Tootmistellimuse toimingute plaanimine</span><span class="sxs-lookup"><span data-stu-id="65098-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="65098-115">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="65098-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="65098-116">Valige tootmistellimus, mille just lõite.</span><span class="sxs-lookup"><span data-stu-id="65098-116">Select the production order that you have just created.</span></span> <span data-ttu-id="65098-117">See peaks olema loendi alguses.</span><span class="sxs-lookup"><span data-stu-id="65098-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="65098-118">Klõpsake tegumiribal valikut Graafik.</span><span class="sxs-lookup"><span data-stu-id="65098-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="65098-119">Klõpsake valikut Planeeri toiminguid.</span><span class="sxs-lookup"><span data-stu-id="65098-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="65098-120">Valige väljal Planeerimissuund üksus Planeerimiskuupäevast edasi.</span><span class="sxs-lookup"><span data-stu-id="65098-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="65098-121">Sisestage kuupäev väljale Plaanimiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="65098-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="65098-122">Valige kuupäev, näiteks täna pluss üks nädal.</span><span class="sxs-lookup"><span data-stu-id="65098-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="65098-123">Kui planeerimissuund on valitud, planeeritakse tootmistellimus sellest kuupäevast edasi.</span><span class="sxs-lookup"><span data-stu-id="65098-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="65098-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="65098-124">Click OK.</span></span>
7. <span data-ttu-id="65098-125">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="65098-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="65098-126">Pange tähele, et olekuks määratakse Planeeritud.</span><span class="sxs-lookup"><span data-stu-id="65098-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="65098-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="65098-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="65098-128">Klõpsake valikut Kõik tööd.</span><span class="sxs-lookup"><span data-stu-id="65098-128">Click All jobs.</span></span>
    * <span data-ttu-id="65098-129">Pange tähele, et operatsioonide planeerimisega ei looda ühtegi tööd.</span><span class="sxs-lookup"><span data-stu-id="65098-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="65098-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="65098-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="65098-131">Tootmistellimuse tööde plaanimine</span><span class="sxs-lookup"><span data-stu-id="65098-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="65098-132">Klõpsake tegumiribal valikut Graafik.</span><span class="sxs-lookup"><span data-stu-id="65098-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="65098-133">Klõpsake valikut Tööde planeerimine.</span><span class="sxs-lookup"><span data-stu-id="65098-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="65098-134">Valige väljal Planeerimissuund üksus Planeerimiskuupäevast edasi.</span><span class="sxs-lookup"><span data-stu-id="65098-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="65098-135">Sisestage kuupäev väljale Plaanimiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="65098-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="65098-136">Valige tuleviku kuupäev, näiteks täna pluss üks nädal.</span><span class="sxs-lookup"><span data-stu-id="65098-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="65098-137">Kui planeerimissuund on valitud, planeeritakse tootmistellimus sellest kuupäevast edasi.</span><span class="sxs-lookup"><span data-stu-id="65098-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="65098-138">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="65098-138">Click OK.</span></span>
6. <span data-ttu-id="65098-139">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="65098-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="65098-140">Klõpsake valikut Kõik tööd.</span><span class="sxs-lookup"><span data-stu-id="65098-140">Click All jobs.</span></span>
    * <span data-ttu-id="65098-141">Pange tähele, et aktiivses protsessis luuakse tööde planeerimisel 5 tööd.</span><span class="sxs-lookup"><span data-stu-id="65098-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

