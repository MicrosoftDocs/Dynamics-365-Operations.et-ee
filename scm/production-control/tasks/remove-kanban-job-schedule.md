--- 
title: "Kanban-töö eemaldamine graafikust"
description: "See protseduur keskendub plaanitud protsessi kanban-töö eemaldamisele graafikust, taastades töö oleku väärtusele Plaanimata."
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
ms.openlocfilehash: 9a0f246bfe42dde0befdf5c4f01d2ad1e1200b12
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="cdcfc-103">Kanban-töö eemaldamine graafikust</span><span class="sxs-lookup"><span data-stu-id="cdcfc-103">Remove a kanban job from the schedule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cdcfc-104">See protseduur keskendub plaanitud protsessi kanban-töö eemaldamisele graafikust, taastades töö oleku väärtusele Plaanimata.</span><span class="sxs-lookup"><span data-stu-id="cdcfc-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="cdcfc-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="cdcfc-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="cdcfc-106">See protseduur on mõeldud tööde järelevaatajale või tootmise planeerijale.</span><span class="sxs-lookup"><span data-stu-id="cdcfc-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="cdcfc-107">Plaanitud kanban-töö leidmine</span><span class="sxs-lookup"><span data-stu-id="cdcfc-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="cdcfc-108">Avage Tootmise juhtimine > Kanban > Kanban-tööde plaanimine.</span><span class="sxs-lookup"><span data-stu-id="cdcfc-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="cdcfc-109">Klõpsake väljal Töörakk otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="cdcfc-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="cdcfc-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="cdcfc-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cdcfc-111">Valige töörakk 1250.</span><span class="sxs-lookup"><span data-stu-id="cdcfc-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="cdcfc-112">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="cdcfc-112">Click Select.</span></span>
5. <span data-ttu-id="cdcfc-113">Valige väljalt Töö oleku kuvamine suvand Plaanitud.</span><span class="sxs-lookup"><span data-stu-id="cdcfc-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="cdcfc-114">Plaanitud kanban-töö eemaldamine graafikust</span><span class="sxs-lookup"><span data-stu-id="cdcfc-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="cdcfc-115">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="cdcfc-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cdcfc-116">Valige töö, mille olekuks on Plaanitud, näiteks töö 19. detsembrist 2012.</span><span class="sxs-lookup"><span data-stu-id="cdcfc-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="cdcfc-117">Klõpsake toimingupaanil valikut Plaan.</span><span class="sxs-lookup"><span data-stu-id="cdcfc-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="cdcfc-118">Klõpsake suvandit Töö oleku taastamine.</span><span class="sxs-lookup"><span data-stu-id="cdcfc-118">Click Revert job status.</span></span>
4. <span data-ttu-id="cdcfc-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="cdcfc-119">Click OK.</span></span>
    * <span data-ttu-id="cdcfc-120">See taastab töö praeguse oleku suvandilt Plaanitud suvandile Plaanimata ja eemaldab selle protsessitahvlilt.</span><span class="sxs-lookup"><span data-stu-id="cdcfc-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   


