---
title: Kanbani protsessitööde käivitamine
description: See protseduur keskendub kanbani protsessitööde käivitamisele.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62be1f116dfecbc4c6ba11053b94efc874baa3e3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "357423"
---
# <a name="execute-kanban-process-jobs"></a><span data-ttu-id="a6fbd-103">Kanbani protsessitööde käivitamine</span><span class="sxs-lookup"><span data-stu-id="a6fbd-103">Execute kanban process jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a6fbd-104">See protseduur keskendub kanbani protsessitööde käivitamisele.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-104">This procedure focuses on executing kanban process jobs.</span></span> <span data-ttu-id="a6fbd-105">Esimene töö on lõpule viidud eeldatava kogusega ja tõrkeid ei ole.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-105">The first job is completed with the expected quantity and has no errors.</span></span> <span data-ttu-id="a6fbd-106">Teine töö on lõpule viidud tõrgetega.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-106">The second job is completed with errors.</span></span> <span data-ttu-id="a6fbd-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a6fbd-108">See protseduur on mõeldud masinaoperaatorile.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-108">This procedure is intended for the machine operator.</span></span>


## <a name="select-a-kanban-job"></a><span data-ttu-id="a6fbd-109">Kanban-töö valimine</span><span class="sxs-lookup"><span data-stu-id="a6fbd-109">Select a kanban job</span></span>
1. <span data-ttu-id="a6fbd-110">Avage Tootmise juhtimine > Kanban > Protsessitööde kanban-tahvel.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-110">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="a6fbd-111">Klõpsake väljal Töörakk otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-111">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a6fbd-112">Klõpsake rida ressursigrupiga 1250.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-112">Click the row with resource group 1250.</span></span> <span data-ttu-id="a6fbd-113">See filtreerib tööde loendit, nii et see kuvab ainult tööraku 1250 tööd.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-113">This filters the Jobs list to display only the jobs for work cell 1250.</span></span>
    * <span data-ttu-id="a6fbd-114">Märkige rida, millel on olek Plaanitud töö.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-114">Mark the row that has the Planned job status.</span></span>  

## <a name="complete-a-job-with-expected-quantity"></a><span data-ttu-id="a6fbd-115">Töö lõpuleviimine eeldatud kogusega</span><span class="sxs-lookup"><span data-stu-id="a6fbd-115">Complete a job with expected quantity</span></span>
1. <span data-ttu-id="a6fbd-116">Laiendage või ahendage jaotist Üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-116">Expand or collapse the Details section.</span></span>
    * <span data-ttu-id="a6fbd-117">Selles jaotises kuvatakse tähtsat teavet kaardi numbri, kaubakoodi, tellitud koguse ja tegevuse nime kohta.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-117">This section displays important information about card number, item number, quantity ordered, and activity name.</span></span>  
2. <span data-ttu-id="a6fbd-118">Laiendage või ahendage jaotist Tootmisjuhendid.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-118">Expand or collapse the Production instructions section.</span></span>
    * <span data-ttu-id="a6fbd-119">Selles jaotises kuvatakse tegevuse tootmise juhised.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-119">This section displays production instructions for the activity.</span></span> <span data-ttu-id="a6fbd-120">Juhised võivad olla tekst, pildid, joonistused ja muud dokumendid.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-120">The instructions can be text, pictures, drawings, and other documents.</span></span>  
3. <span data-ttu-id="a6fbd-121">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-121">Click Start.</span></span>
    * <span data-ttu-id="a6fbd-122">Valige töö, mis ei ole lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-122">Select a job that is not completed.</span></span> <span data-ttu-id="a6fbd-123">Töö oleku vaatamiseks kasutage väljal Töö olek olevaid olekuikoone.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-123">Use status icons in the Job status field to view job status.</span></span>      
4. <span data-ttu-id="a6fbd-124">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-124">Click Complete.</span></span>
    * <span data-ttu-id="a6fbd-125">Töö on lõpule viidud eeldatud kvaliteediga.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-125">The job is completed with the expected quality.</span></span>  

## <a name="complete-a-job-with-errors"></a><span data-ttu-id="a6fbd-126">Töö lõpuleviimine tõrgetega</span><span class="sxs-lookup"><span data-stu-id="a6fbd-126">Complete a job with errors</span></span>
1. <span data-ttu-id="a6fbd-127">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-127">Click Start.</span></span>
    * <span data-ttu-id="a6fbd-128">Kui töö on lõpule viidud, valitakse automaatselt järgmine töö loendist.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-128">When a job is completed, the next job on the list is selected automatically.</span></span> <span data-ttu-id="a6fbd-129">Sellepärast ei pea te valima tööd enne nupu Start klõpsamist.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-129">This is why you don't need to select a job before you click Start.</span></span>  
2. <span data-ttu-id="a6fbd-130">Klõpsake toimingupaanil suvandit Tootmine.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-130">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="a6fbd-131">Klõpsake käsku Lõpeta (üksikasjad).</span><span class="sxs-lookup"><span data-stu-id="a6fbd-131">Click Complete (details).</span></span>
4. <span data-ttu-id="a6fbd-132">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="a6fbd-133">Sisestage väljale Tõrgete kogus number.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-133">In the Error quantity field, enter a number.</span></span>
6. <span data-ttu-id="a6fbd-134">Sisestage number väljale Hea kogus.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-134">In the Good quantity field, enter a number.</span></span>
7. <span data-ttu-id="a6fbd-135">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a6fbd-135">Click OK.</span></span>

