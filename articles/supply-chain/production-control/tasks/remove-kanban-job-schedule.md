---
title: Kanban-töö eemaldamine graafikust
description: See protseduur keskendub plaanitud protsessi kanban-töö eemaldamisele graafikust, taastades töö oleku väärtusele Plaanimata.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e9a512e7f391e08a35fd0eea449af12d81e644
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828582"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="cbe74-103">Kanban-töö eemaldamine graafikust</span><span class="sxs-lookup"><span data-stu-id="cbe74-103">Remove a kanban job from the schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cbe74-104">See protseduur keskendub plaanitud protsessi kanban-töö eemaldamisele graafikust, taastades töö oleku väärtusele Plaanimata.</span><span class="sxs-lookup"><span data-stu-id="cbe74-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="cbe74-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="cbe74-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="cbe74-106">See protseduur on mõeldud tööde järelevaatajale või tootmise planeerijale.</span><span class="sxs-lookup"><span data-stu-id="cbe74-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="cbe74-107">Plaanitud kanban-töö leidmine</span><span class="sxs-lookup"><span data-stu-id="cbe74-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="cbe74-108">Avage Tootmise juhtimine > Kanban > Kanban-tööde plaanimine.</span><span class="sxs-lookup"><span data-stu-id="cbe74-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="cbe74-109">Klõpsake väljal Töörakk otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="cbe74-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="cbe74-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="cbe74-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cbe74-111">Valige töörakk 1250.</span><span class="sxs-lookup"><span data-stu-id="cbe74-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="cbe74-112">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="cbe74-112">Click Select.</span></span>
5. <span data-ttu-id="cbe74-113">Valige väljalt Töö oleku kuvamine suvand Plaanitud.</span><span class="sxs-lookup"><span data-stu-id="cbe74-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="cbe74-114">Plaanitud kanban-töö eemaldamine graafikust</span><span class="sxs-lookup"><span data-stu-id="cbe74-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="cbe74-115">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="cbe74-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cbe74-116">Valige töö, mille olekuks on Plaanitud, näiteks töö 19. detsembrist 2012.</span><span class="sxs-lookup"><span data-stu-id="cbe74-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="cbe74-117">Klõpsake toimingupaanil valikut Plaan.</span><span class="sxs-lookup"><span data-stu-id="cbe74-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="cbe74-118">Klõpsake suvandit Töö oleku taastamine.</span><span class="sxs-lookup"><span data-stu-id="cbe74-118">Click Revert job status.</span></span>
4. <span data-ttu-id="cbe74-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="cbe74-119">Click OK.</span></span>
    * <span data-ttu-id="cbe74-120">See taastab töö praeguse oleku suvandilt Plaanitud suvandile Plaanimata ja eemaldab selle protsessitahvlilt.</span><span class="sxs-lookup"><span data-stu-id="cbe74-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]