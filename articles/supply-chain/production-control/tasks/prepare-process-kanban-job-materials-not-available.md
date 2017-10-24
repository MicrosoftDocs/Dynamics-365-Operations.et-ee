--- 
title: "Protsessi kanban-töö ettevalmistamine, kui materjalid pole tööraku jaoks saadaval"
description: "See protseduur keskendub protsessi kanban-töö ettevalmistamisele, kui mõned materjalid pole tööraku puhul saadaval, mistõttu tuleb materjalid laost komplekteerida."
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
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5a47af6910a9686e74ab6d1069dd02079e60cb8a
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="b8b0e-103">Protsessi kanban-töö ettevalmistamine, kui materjalid pole tööraku jaoks saadaval</span><span class="sxs-lookup"><span data-stu-id="b8b0e-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8b0e-104">See protseduur keskendub protsessi kanban-töö ettevalmistamisele, kui mõned materjalid pole tööraku puhul saadaval, mistõttu tuleb materjalid laost komplekteerida.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="b8b0e-105">Protseduur Protsessi kanban-töö ettevalmistamine materjalide mittesaadavusel on selle protseduuri loomise eeltingimus.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="b8b0e-106">See protseduur on mõeldud masinaoperaatorile.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="b8b0e-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="b8b0e-108">Avage Tootmise juhtimine > Kanban > Protsessitööde kanban-tahvel.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="b8b0e-109">Klõpsake väljal Töörakk otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="b8b0e-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b8b0e-111">Valige töörakk 1250.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="b8b0e-112">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b8b0e-113">Valige Kanban 000356.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="b8b0e-114">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b8b0e-115">Tühistage loendis rea 4 valik.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-115">In the list, deselect row 4.</span></span> <span data-ttu-id="b8b0e-116">või valige rida 4, kui te pole lõpetanud ülesannet „Protsessi kanban-töö ettevalmistamine materjalide saadavusel“.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="b8b0e-117">Laiendage jaotist Komplekteerimisleht.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="b8b0e-118">Kirje puudumise ikoon tarne olekus näitab, et kauba P0002 rida 48 puudub tööraku puhul.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="b8b0e-119">Materjalide ülekanne töörakku</span><span class="sxs-lookup"><span data-stu-id="b8b0e-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="b8b0e-120">Laiendage jaotist Ülekandetööd.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="b8b0e-121">Kasutage kiirfiltrit, et filtreerida väli Kaubakood väärtuse P0002 alusel.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="b8b0e-122">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="b8b0e-123">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-123">Click Start.</span></span>
    * <span data-ttu-id="b8b0e-124">Edastamine on pooleli.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="b8b0e-125">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-125">Click Complete.</span></span>
    * <span data-ttu-id="b8b0e-126">Kaup P0002 on nüüd kanban-töö puhul komplekteerimislehel saadaval.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="b8b0e-127">See tähendab, et saame kanbani koos kõigi vajalike materjalidega ette valmistada.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="b8b0e-128">Klõpsake suvandit Valmista ette.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-128">Click Prepare.</span></span>
    * <span data-ttu-id="b8b0e-129">Pange tähele, et töö oleku ikoon näitab, et töö on nüüd valmis.</span><span class="sxs-lookup"><span data-stu-id="b8b0e-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  


