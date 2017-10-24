--- 
title: "Kanban-töödega materjalide ülekandmine (ainult veebruar 2016)"
description: "See protseduur keskendub tagastamise kanban-tööle materjalide ülekandeks."
author: ChristianRytt
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c79480d844627a7eed8129515924f1f70ad04f95
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="transfer-materials-with-kanban-jobs-february-2016-only"></a><span data-ttu-id="d6b8b-103">Kanban-töödega materjalide ülekandmine (ainult veebruar 2016)</span><span class="sxs-lookup"><span data-stu-id="d6b8b-103">Transfer materials with kanban jobs (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d6b8b-104">See protseduur keskendub tagastamise kanban-tööle materjalide ülekandeks.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="d6b8b-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d6b8b-106">See protseduur on mõeldud laotöötajale.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="d6b8b-107">Ülekandetööde kuvamine</span><span class="sxs-lookup"><span data-stu-id="d6b8b-107">Display transfer jobs</span></span>
1. <span data-ttu-id="d6b8b-108">Avage Tootmise juhtimine > Kanban > Ülekandetööde kanban-tahvel.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="d6b8b-109">Laiendage või ahendage jaotist Filtrid.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="d6b8b-110">Jaotises Filtrid saate määrata, milliseid töid soovite kuvada, filtrides suvandid Tootmisvoog, Tegevuse nimi, Lähteladu ja -asukoht ning Sihtladu ja -asukoht.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="d6b8b-111">Sisestage väljale Laost väärtus 11.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="d6b8b-112">Sisestage väljale Asukohta väärtus 12.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="d6b8b-113">Käivita ülekandmistöö</span><span class="sxs-lookup"><span data-stu-id="d6b8b-113">Start a transfer job</span></span>
1. <span data-ttu-id="d6b8b-114">Tühistage loendis olemasolul valitud rea valik.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="d6b8b-115">Valige loendist rida 4.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="d6b8b-116">Valige esimene töö, mille olek on Plaanimata.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="d6b8b-117">Veenduge, et valitud on ainult see töö.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="d6b8b-118">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-118">Click Start.</span></span>
    * <span data-ttu-id="d6b8b-119">Pange tähele, et ikoon näitab, et tööd on alustatud.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="d6b8b-120">Teise ülekandetöö valimine ja koguse muutmine</span><span class="sxs-lookup"><span data-stu-id="d6b8b-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="d6b8b-121">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d6b8b-122">Teil võib olla valitud mitu tööd, kuid praegu valige 5. rida.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="d6b8b-123">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d6b8b-124">Veenduge, et valitud oleks ainult eelmises etapis olev töö.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="d6b8b-125">Tühistage kõikide muude tööde valik.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="d6b8b-126">Märkige väljal Töö kogus olev väärtus edasiseks viiteks üles</span><span class="sxs-lookup"><span data-stu-id="d6b8b-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="d6b8b-127">Määrake töö koguseks 30.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="d6b8b-128">Pange tähele hoiatust!</span><span class="sxs-lookup"><span data-stu-id="d6b8b-128">Notice the warning!</span></span> <span data-ttu-id="d6b8b-129">Teil pole lubatud üle kanda rohkem kui 30.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="d6b8b-130">Kanban-reegli seadistuse järgi saate üle kanda ainult algse koguse.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="d6b8b-131">Kasutage varem väljal Töö kogus märgitud väärtust</span><span class="sxs-lookup"><span data-stu-id="d6b8b-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="d6b8b-132">Seadistage Töö kogus eelmisele väärtusele.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="d6b8b-133">Teise ülekandetöö alustamine</span><span class="sxs-lookup"><span data-stu-id="d6b8b-133">Start the second transfer job</span></span>
1. <span data-ttu-id="d6b8b-134">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-134">Click Start.</span></span>
    * <span data-ttu-id="d6b8b-135">See käivitab 5. reas oleva töö ülekande.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="d6b8b-136">Mõlema ülekandetöö lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d6b8b-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="d6b8b-137">Valige loendist rida 4.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="d6b8b-138">Nüüd on 4. ja 5. real valitud kaks ülekandetööd.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="d6b8b-139">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-139">Click Complete.</span></span>
    * <span data-ttu-id="d6b8b-140">See lõpetab mõlema töö ülekande.</span><span class="sxs-lookup"><span data-stu-id="d6b8b-140">This will complete the transfer of both jobs.</span></span>  


