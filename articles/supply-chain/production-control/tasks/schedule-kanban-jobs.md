---
title: Kanban-tööde plaanimine
description: See protseduur keskendub protsessi kanban-tööde plaanimisele kindla tööraku puhul.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a56bca460af229b53d41959d48562ef425c0bf7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843477"
---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="6e427-103">Kanban-tööde plaanimine</span><span class="sxs-lookup"><span data-stu-id="6e427-103">Schedule kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e427-104">See protseduur keskendub protsessi kanban-tööde plaanimisele kindla tööraku puhul.</span><span class="sxs-lookup"><span data-stu-id="6e427-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="6e427-105">Protseduur Protsessi kanban-töö ettevalmistamine materjalide mittesaadavusel tööraku puhul on selle protseduuri loomise eeltingimus.</span><span class="sxs-lookup"><span data-stu-id="6e427-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="6e427-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="6e427-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6e427-107">See ülesanne on mõeldud kanbanidega töötavale tööde järelevaatajale ja tootmise planeerijale.</span><span class="sxs-lookup"><span data-stu-id="6e427-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="6e427-108">Kanban-tööde valimine tööraku puhul</span><span class="sxs-lookup"><span data-stu-id="6e427-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="6e427-109">Avage Tootmise juhtimine > Kanban > Kanban-tööde plaanimine.</span><span class="sxs-lookup"><span data-stu-id="6e427-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="6e427-110">Kiirinfo Perioodi võimsus laiendamine</span><span class="sxs-lookup"><span data-stu-id="6e427-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="6e427-111">Laiendage kiirinfot Kanban.</span><span class="sxs-lookup"><span data-stu-id="6e427-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="6e427-112">Klõpsake väljal Töörakk otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6e427-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6e427-113">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6e427-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6e427-114">Valige töörakk 1250.</span><span class="sxs-lookup"><span data-stu-id="6e427-114">Select work cell 1250.</span></span> <span data-ttu-id="6e427-115">See filtrib vaate kuvama ainult tööraku 1250 töid.</span><span class="sxs-lookup"><span data-stu-id="6e427-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="6e427-116">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6e427-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="6e427-117">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="6e427-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="6e427-118">Kanban-töö plaanimine esimeses saadaolevas perioodis</span><span class="sxs-lookup"><span data-stu-id="6e427-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="6e427-119">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6e427-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6e427-120">Valige esimene rida loendist, mille olek on Plaanimata.</span><span class="sxs-lookup"><span data-stu-id="6e427-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="6e427-121">Punktiirikoon väljal Töö olek näitab plaanimatust.</span><span class="sxs-lookup"><span data-stu-id="6e427-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="6e427-122">Klõpsake suvandit Graafik.</span><span class="sxs-lookup"><span data-stu-id="6e427-122">Click Schedule.</span></span>
    * <span data-ttu-id="6e427-123">See kavandab kanban-töö esimeses saadaolevas perioodis.</span><span class="sxs-lookup"><span data-stu-id="6e427-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="6e427-124">Pange tähele, et kanban-töö teisaldatakse loendi lõppu, kuna see on lisatud perioodi alates tänasest.</span><span class="sxs-lookup"><span data-stu-id="6e427-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="6e427-125">Kui periood alates tänasest on täis, teisaldatakse töö esimesse saadaolevasse perioodi.</span><span class="sxs-lookup"><span data-stu-id="6e427-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="6e427-126">Kahe kanban-töö plaanimine kindlaks päevaks</span><span class="sxs-lookup"><span data-stu-id="6e427-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="6e427-127">Valige loendist rida 1.</span><span class="sxs-lookup"><span data-stu-id="6e427-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="6e427-128">Peaksite nägema, et esimesel real on väljal Töö olek suvandiks Plaanimata.</span><span class="sxs-lookup"><span data-stu-id="6e427-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="6e427-129">Valige loendist rida 2.</span><span class="sxs-lookup"><span data-stu-id="6e427-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="6e427-130">Peaksite nägema, et teisel real on väljal Töö olek suvandiks Plaanimata.</span><span class="sxs-lookup"><span data-stu-id="6e427-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="6e427-131">Nüüd on teil kaks esimest tööd valitud.</span><span class="sxs-lookup"><span data-stu-id="6e427-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="6e427-132">Rippdialoogi avamiseks klõpsake suvandit Plaani alates kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="6e427-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="6e427-133">Märkige või tühjendage ruut Alista mahu puudujäägi reaktsioon.</span><span class="sxs-lookup"><span data-stu-id="6e427-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="6e427-134">See suvand võimaldab teil vaikimisi mahu puudujäägi reaktsiooni alistada.</span><span class="sxs-lookup"><span data-stu-id="6e427-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="6e427-135">Valige väljalt Võimsuse puudujäägi reaktsioon suvand Lisa taotletud perioodile.</span><span class="sxs-lookup"><span data-stu-id="6e427-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="6e427-136">See suvand tagab töö lisamise taotletud perioodi olenemata sellest, kas töörakk võib olla ülekoormatud.</span><span class="sxs-lookup"><span data-stu-id="6e427-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="6e427-137">Klõpsake suvandit Graafik.</span><span class="sxs-lookup"><span data-stu-id="6e427-137">Click Schedule.</span></span>
    * <span data-ttu-id="6e427-138">Pange tähele, et mõlemad tööd lisatakse soovitud perioodi.</span><span class="sxs-lookup"><span data-stu-id="6e427-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="6e427-139">Jaotises Perioodi võimsus saate vaadata iga perioodi koormust.</span><span class="sxs-lookup"><span data-stu-id="6e427-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="6e427-140">Väli Tarbimine kuvab plaanitud tarbimise sellel perioodil.</span><span class="sxs-lookup"><span data-stu-id="6e427-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="6e427-141">Kui plaanitud tarbimine selles perioodis on saadaolevast võimsusest suurem, valitakse ülekoormatud tarbimine.</span><span class="sxs-lookup"><span data-stu-id="6e427-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  

