--- 
title: "Ajastatud kanban-tööde teisaldamine"
description: "See protseduur keskendub plaanitud protsessi kanban-tööde teise perioodi teisaldamisele."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2a12a6859a3a436706822873bc6fdd781e0ef032
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="26ad2-103">Ajastatud kanban-tööde teisaldamine</span><span class="sxs-lookup"><span data-stu-id="26ad2-103">Move scheduled kanban jobs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="26ad2-104">See protseduur keskendub plaanitud protsessi kanban-tööde teise perioodi teisaldamisele.</span><span class="sxs-lookup"><span data-stu-id="26ad2-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="26ad2-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="26ad2-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="26ad2-106">See protseduur on mõeldud kanbanidega töötavale tööde järelevaatajale või tootmise planeerijale.</span><span class="sxs-lookup"><span data-stu-id="26ad2-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>


## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="26ad2-107">Plaanitud kanban-tööde valimine</span><span class="sxs-lookup"><span data-stu-id="26ad2-107">Select scheduled kanban jobs</span></span>
1. <span data-ttu-id="26ad2-108">Avage Tootmine > Kanban > Kanban-töö planeerimine.</span><span class="sxs-lookup"><span data-stu-id="26ad2-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span></span>
2. <span data-ttu-id="26ad2-109">!MtCMR!Klõpsake väljal Töörakk otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="26ad2-109">!MtCMR!In the Work cell field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="26ad2-110">áçêìõý!</span><span class="sxs-lookup"><span data-stu-id="26ad2-110">áçêìõý !</span></span>
3. <span data-ttu-id="26ad2-111">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="26ad2-111">Markér den valgte række på listen.</span></span>
    * <span data-ttu-id="26ad2-112">Valige töörakk 1250.</span><span class="sxs-lookup"><span data-stu-id="26ad2-112">Select work cell 1250.</span></span>  
4. <span data-ttu-id="26ad2-113">Klõpsake suvandit Vali.</span><span class="sxs-lookup"><span data-stu-id="26ad2-113">Klik på Select.</span></span>
5. <span data-ttu-id="26ad2-114">Valige väljalt Plaanitud suvand Töö oleku kuvamine.</span><span class="sxs-lookup"><span data-stu-id="26ad2-114">Vælg 'Planlagt' i feltet Display job status.</span></span>
    * <span data-ttu-id="26ad2-115">See filtrib tööloendi kuvama ainult plaanitud kanban-töid.</span><span class="sxs-lookup"><span data-stu-id="26ad2-115">This filters the job list to display only the scheduled kanban jobs.</span></span>  

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="26ad2-116">Kanban-tööde teisaldamine teise perioodi</span><span class="sxs-lookup"><span data-stu-id="26ad2-116">Move kanban jobs to a different period</span></span>
1. <span data-ttu-id="26ad2-117">Leidke ja valige loendist vajalik kirje.</span><span class="sxs-lookup"><span data-stu-id="26ad2-117">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="26ad2-118">Valige töö, mille olekuks on Plaanitud, näiteks töö, mis on väljal Plaanitud periood kavandatud 20. detsembrile 2012.</span><span class="sxs-lookup"><span data-stu-id="26ad2-118">Select a job that has the Planned job status, for example, a job scheduled on December 20, 2012  in the Planned period field.</span></span> <span data-ttu-id="26ad2-119">Seejärel teisaldage töö eelmisesse perioodi.</span><span class="sxs-lookup"><span data-stu-id="26ad2-119">Then move the job to the previous period.</span></span>  
2. <span data-ttu-id="26ad2-120">Klõpsake suvandit Eelmine periood.</span><span class="sxs-lookup"><span data-stu-id="26ad2-120">Klik på Previous period.</span></span>
3. <span data-ttu-id="26ad2-121">Klõpsake suvandit Lõpp.</span><span class="sxs-lookup"><span data-stu-id="26ad2-121">Klik på End.</span></span>
    * <span data-ttu-id="26ad2-122">See teisaldab töö tööde loendi lõppu viimase tööna eelmises perioodis.</span><span class="sxs-lookup"><span data-stu-id="26ad2-122">This will move the job to the end of the job list as the last job in the previous period.</span></span>  
4. <span data-ttu-id="26ad2-123">Leidke ja valige loendist vajalik kirje.</span><span class="sxs-lookup"><span data-stu-id="26ad2-123">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="26ad2-124">Valige töö, mille olekuks on Plaanitud, näiteks töö, mis on väljal Plaanitud periood kavandatud 18. detsembrile 2012.</span><span class="sxs-lookup"><span data-stu-id="26ad2-124">Select a job that has the Planned job status, for example, a job scheduled on December 18, 2012 in the Planned period field.</span></span> <span data-ttu-id="26ad2-125">Seejärel teisaldage töö järgmisesse perioodi.</span><span class="sxs-lookup"><span data-stu-id="26ad2-125">Then move the job to the next period.</span></span>  
5. <span data-ttu-id="26ad2-126">Klõpsake suvandit Järgmine periood.</span><span class="sxs-lookup"><span data-stu-id="26ad2-126">Klik på Next period.</span></span>
6. <span data-ttu-id="26ad2-127">Klõpsake suvandit Algus.</span><span class="sxs-lookup"><span data-stu-id="26ad2-127">Klik på Start.</span></span>
    * <span data-ttu-id="26ad2-128">See teisaldab töö tööde loendi algusesse esimese tööna eelmises perioodis.</span><span class="sxs-lookup"><span data-stu-id="26ad2-128">This will move the job to the start of the job list as the first job in the previous period.</span></span>  

## <a name="task-move-a-job-within-a-period"></a><span data-ttu-id="26ad2-129">Ülesanne: perioodi töö teisaldamine</span><span class="sxs-lookup"><span data-stu-id="26ad2-129">Task: Move a job within a period</span></span>
1. <span data-ttu-id="26ad2-130">Leidke ja valige loendist vajalik kirje.</span><span class="sxs-lookup"><span data-stu-id="26ad2-130">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="26ad2-131">Valige töö, mille olekuks on Plaanitud, näiteks teine töö, mis on väljal Plaanitud periood kavandatud 19. detsembrile 2012.</span><span class="sxs-lookup"><span data-stu-id="26ad2-131">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the Planned period field.</span></span> <span data-ttu-id="26ad2-132">Seejärel liigutage tööd plaanitud perioodi sees.</span><span class="sxs-lookup"><span data-stu-id="26ad2-132">Then move the job within the planned period.</span></span>  
2. <span data-ttu-id="26ad2-133">Klõpsake suvandit Edasi.</span><span class="sxs-lookup"><span data-stu-id="26ad2-133">Klik på Forward.</span></span>
    * <span data-ttu-id="26ad2-134">Pange tähele, et tööd teisaldatakse loendis üks rida alla.</span><span class="sxs-lookup"><span data-stu-id="26ad2-134">Notice that the job is moved one line down on the list.</span></span>  
3. <span data-ttu-id="26ad2-135">Klõpsake suvandit Tagasi.</span><span class="sxs-lookup"><span data-stu-id="26ad2-135">Klik på Backward.</span></span>
    * <span data-ttu-id="26ad2-136">Pange tähele, et tööd teisaldatakse loendis üks rida üles.</span><span class="sxs-lookup"><span data-stu-id="26ad2-136">Notice that the job is moved one line up on the list.</span></span>  


