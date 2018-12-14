--- 
title: "Ajastatud kanban-tööde teisaldamine"
description: "See protseduur keskendub plaanitud protsessi kanban-tööde teise perioodi teisaldamisele."
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b589a6ce02cdc02436e256f9e81346fe8b766687
ms.openlocfilehash: f791c9048ef6efe1585c991f998099cd1fc12df7
ms.contentlocale: et-ee
ms.lasthandoff: 12/04/2018

---

# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="fb650-103">Ajastatud kanban-tööde teisaldamine</span><span class="sxs-lookup"><span data-stu-id="fb650-103">Move scheduled kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fb650-104">See protseduur keskendub plaanitud protsessi kanban-tööde teise perioodi teisaldamisele.</span><span class="sxs-lookup"><span data-stu-id="fb650-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="fb650-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="fb650-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="fb650-106">See protseduur on mõeldud kanbanidega töötavale tööde järelevaatajale või tootmise planeerijale.</span><span class="sxs-lookup"><span data-stu-id="fb650-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="fb650-107">Valige plaanitud kanban-tööd.</span><span class="sxs-lookup"><span data-stu-id="fb650-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="fb650-108">Minge jaotisse **Tootmise juhtimine > Kanban > Kanban-tööde plaanimine**.</span><span class="sxs-lookup"><span data-stu-id="fb650-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="fb650-109">Klõpsake väljal **Töörakk** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="fb650-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="fb650-110">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="fb650-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="fb650-111">Valige töörakk 1250.</span><span class="sxs-lookup"><span data-stu-id="fb650-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="fb650-112">Klõpsake **Vali**.</span><span class="sxs-lookup"><span data-stu-id="fb650-112">Click **Select**.</span></span> 

5. <span data-ttu-id="fb650-113">Valige väljalt **Töö oleku kuvamine** suvand **Plaanitud**.</span><span class="sxs-lookup"><span data-stu-id="fb650-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="fb650-114">See filtrib tööloendi kuvama ainult plaanitud kanban-töid.</span><span class="sxs-lookup"><span data-stu-id="fb650-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="fb650-115">Teisaldage kanban-tööd teise perioodi.</span><span class="sxs-lookup"><span data-stu-id="fb650-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="fb650-116">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="fb650-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="fb650-117">Valige töö, millel on olek **Plaanitud töö**, näiteks väljal **Plaanitud periood** 20. detsembrile 2012 kavandatud töö.</span><span class="sxs-lookup"><span data-stu-id="fb650-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="fb650-118">Seejärel teisaldage töö eelmisesse perioodi.</span><span class="sxs-lookup"><span data-stu-id="fb650-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="fb650-119">Klõpsake valikut **Eelmine periood**.</span><span class="sxs-lookup"><span data-stu-id="fb650-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="fb650-120">Klõpsake nuppu **Lõpp** töö teisaldamiseks tööde loendi lõppu viimase tööna eelmises perioodis.</span><span class="sxs-lookup"><span data-stu-id="fb650-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="fb650-121">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="fb650-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="fb650-122">Valige töö, millel on olek **Plaanitud töö**, näiteks väljal **Plaanitud periood** 18. detsembrile 2012 kavandatud töö.</span><span class="sxs-lookup"><span data-stu-id="fb650-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="fb650-123">Seejärel teisaldage töö järgmisesse perioodi.</span><span class="sxs-lookup"><span data-stu-id="fb650-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="fb650-124">Klõpsake valikut **Järgmine periood**.</span><span class="sxs-lookup"><span data-stu-id="fb650-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="fb650-125">Klõpsake nuppu **Algus** töö teisaldamiseks tööde loendi algusesse esimese tööna eelmises perioodis.</span><span class="sxs-lookup"><span data-stu-id="fb650-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="fb650-126">Teisaldage töö perioodisiseselt.</span><span class="sxs-lookup"><span data-stu-id="fb650-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="fb650-127">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="fb650-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="fb650-128">Valige töö, millel on olek olekuks on Plaanitud töö, näiteks väljal **Plaanitud periood** 19. detsembrile 2012 kavandatud teine töö.</span><span class="sxs-lookup"><span data-stu-id="fb650-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="fb650-129">Seejärel liigutage tööd plaanitud perioodi sees.</span><span class="sxs-lookup"><span data-stu-id="fb650-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="fb650-130">Klõpsake nuppu **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="fb650-130">Click **Forward**.</span></span> <span data-ttu-id="fb650-131">Pange tähele, et tööd teisaldatakse loendis üks rida alla.</span><span class="sxs-lookup"><span data-stu-id="fb650-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="fb650-132">Klõpsake nuppu **Tagasi**.</span><span class="sxs-lookup"><span data-stu-id="fb650-132">Click **Backward**.</span></span> <span data-ttu-id="fb650-133">Pange tähele, et tööd teisaldatakse loendis üks rida üles.</span><span class="sxs-lookup"><span data-stu-id="fb650-133">Notice that the job is moved one line up on the list.</span></span>

