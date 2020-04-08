---
title: Tootmistellimuse plaanimine koos toimingute ja tööde plaanimisega
description: Selles teemas keskendutakse tootmistellimuse plaanimisele koos toimingute ja tööde plaanimisega.
author: ChristianRytt
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2181a84aea08aac0ddb202f7211dbda6330a3d49
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148833"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="ec9b2-103">Tootmistellimuse plaanimine koos toimingute ja tööde plaanimisega</span><span class="sxs-lookup"><span data-stu-id="ec9b2-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ec9b2-104">Selles teemas keskendutakse tootmistellimuse plaanimisele koos toimingute ja tööde plaanimisega.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="ec9b2-105">Toimingute planeerimisega ei looda ühtegi tööd, samas kui töö planeerimisega luuakse tööd.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="ec9b2-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="ec9b2-107">See protseduur on mõeldud diskreetses tootmiskeskkonnas töötavale tootmisjuhile, tootmise planeerijale või tööde järelevaatajale.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="ec9b2-108">Tootmistellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="ec9b2-108">Create a production order</span></span>
1. <span data-ttu-id="ec9b2-109">Avage navigeerimispaanil **Moodulid > Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="ec9b2-110">Valige **Uus tootmistellimus**.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-110">Select **New production order**.</span></span>
3. <span data-ttu-id="ec9b2-111">Sisestage või valige väärtus väljale **Kauba kood**.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="ec9b2-112">Valige kaubakood **D0001**.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="ec9b2-113">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="ec9b2-114">Tootmistellimuse toimingute plaanimine</span><span class="sxs-lookup"><span data-stu-id="ec9b2-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="ec9b2-115">Märkige äsja loodud rida.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="ec9b2-116">Toimingupaanil valige **Plaani**.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="ec9b2-117">Valige **Plaani toiming**.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="ec9b2-118">Väljal **Planeerimissuund** valige **Planeerimiskuupäevast edasi**.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="ec9b2-119">Väljale **Planeerimiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="ec9b2-120">Valige kuupäev, näiteks täna pluss üks nädal.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="ec9b2-121">Kui planeerimissuund on valitud, planeeritakse tootmistellimus sellest kuupäevast edasi.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="ec9b2-122">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-122">Select **OK**.</span></span>
7. <span data-ttu-id="ec9b2-123">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-123">In the list, mark the selected row.</span></span> <span data-ttu-id="ec9b2-124">Pange tähele, et olek on muudetud **Plaanitud**.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="ec9b2-125">Valige **Kõik tööd**.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-125">Select **All jobs**.</span></span> <span data-ttu-id="ec9b2-126">Pange tähele, et operatsioonide planeerimisega ei looda ühtegi tööd.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="ec9b2-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="ec9b2-128">Tootmistellimuse tööde plaanimine</span><span class="sxs-lookup"><span data-stu-id="ec9b2-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="ec9b2-129">Toimingupaanil valige **Plaani**.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="ec9b2-130">Valige **Plaani töid**.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="ec9b2-131">Väljal **Planeerimissuund** valige **Planeerimiskuupäevast edasi**.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="ec9b2-132">Väljale **Planeerimiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="ec9b2-133">Valige tuleviku kuupäev, näiteks täna pluss üks nädal.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="ec9b2-134">Kui planeerimissuund on valitud, planeeritakse tootmistellimus sellest kuupäevast edasi.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="ec9b2-135">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-135">Select **OK**.</span></span>
6. <span data-ttu-id="ec9b2-136">Toimingupaanil valige **Tootmistellimus**.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="ec9b2-137">Valige **Kõik tööd**.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-137">Select **All jobs**.</span></span> <span data-ttu-id="ec9b2-138">Pange tähele, et aktiivses protsessis luuakse tööde planeerimisel 5 tööd.</span><span class="sxs-lookup"><span data-stu-id="ec9b2-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

