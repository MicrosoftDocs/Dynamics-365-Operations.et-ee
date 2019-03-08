---
title: Kanban-töödega materjalide ülekandmine
description: See protseduur keskendub tagastamise kanban-tööle materjalide ülekandeks.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2db7b9fb960beb5b4a851aabb9f28a0f9e3d3da
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "367428"
---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="3e5a7-103">Kanban-töödega materjalide ülekandmine</span><span class="sxs-lookup"><span data-stu-id="3e5a7-103">Transfer materials with kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3e5a7-104">See protseduur keskendub tagastamise kanban-tööle materjalide ülekandeks.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="3e5a7-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3e5a7-106">See protseduur on mõeldud laotöötajale.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="3e5a7-107">Ülekandetööde kuvamine</span><span class="sxs-lookup"><span data-stu-id="3e5a7-107">Display transfer jobs</span></span>
1. <span data-ttu-id="3e5a7-108">Avage Tootmise juhtimine > Kanban > Ülekandetööde kanban-tahvel.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="3e5a7-109">Laiendage või ahendage jaotist Filtrid.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="3e5a7-110">Jaotises Filtrid saate määrata, milliseid töid soovite kuvada, filtrides suvandid Tootmisvoog, Tegevuse nimi, Lähteladu ja -asukoht ning Sihtladu ja -asukoht.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="3e5a7-111">Sisestage väljale Laost väärtus 11.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="3e5a7-112">Sisestage väljale Asukohta väärtus 12.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="3e5a7-113">Käivita ülekandmistöö</span><span class="sxs-lookup"><span data-stu-id="3e5a7-113">Start a transfer job</span></span>
1. <span data-ttu-id="3e5a7-114">Tühistage loendis olemasolul valitud rea valik.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="3e5a7-115">Valige loendist rida 4.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="3e5a7-116">Valige esimene töö, mille olek on Plaanimata.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="3e5a7-117">Veenduge, et valitud on ainult see töö.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="3e5a7-118">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-118">Click Start.</span></span>
    * <span data-ttu-id="3e5a7-119">Pange tähele, et ikoon näitab, et tööd on alustatud.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="3e5a7-120">Teise ülekandetöö valimine ja koguse muutmine</span><span class="sxs-lookup"><span data-stu-id="3e5a7-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="3e5a7-121">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3e5a7-122">Teil võib olla valitud mitu tööd, kuid praegu valige 5. rida.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="3e5a7-123">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3e5a7-124">Veenduge, et valitud oleks ainult eelmises etapis olev töö.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="3e5a7-125">Tühistage kõikide muude tööde valik.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="3e5a7-126">Märkige väljal Töö kogus olev väärtus edasiseks viiteks üles</span><span class="sxs-lookup"><span data-stu-id="3e5a7-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="3e5a7-127">Määrake töö koguseks 30.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="3e5a7-128">Pange tähele hoiatust!</span><span class="sxs-lookup"><span data-stu-id="3e5a7-128">Notice the warning!</span></span> <span data-ttu-id="3e5a7-129">Teil pole lubatud üle kanda rohkem kui 30.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="3e5a7-130">Kanban-reegli seadistuse järgi saate üle kanda ainult algse koguse.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="3e5a7-131">Kasutage varem väljal Töö kogus märgitud väärtust</span><span class="sxs-lookup"><span data-stu-id="3e5a7-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="3e5a7-132">Seadistage Töö kogus eelmisele väärtusele.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="3e5a7-133">Teise ülekandetöö alustamine</span><span class="sxs-lookup"><span data-stu-id="3e5a7-133">Start the second transfer job</span></span>
1. <span data-ttu-id="3e5a7-134">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-134">Click Start.</span></span>
    * <span data-ttu-id="3e5a7-135">See käivitab 5. reas oleva töö ülekande.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="3e5a7-136">Mõlema ülekandetöö lõpetamine</span><span class="sxs-lookup"><span data-stu-id="3e5a7-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="3e5a7-137">Valige loendist rida 4.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="3e5a7-138">Nüüd on 4. ja 5. real valitud kaks ülekandetööd.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="3e5a7-139">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-139">Click Complete.</span></span>
    * <span data-ttu-id="3e5a7-140">See lõpetab mõlema töö ülekande.</span><span class="sxs-lookup"><span data-stu-id="3e5a7-140">This will complete the transfer of both jobs.</span></span>  

