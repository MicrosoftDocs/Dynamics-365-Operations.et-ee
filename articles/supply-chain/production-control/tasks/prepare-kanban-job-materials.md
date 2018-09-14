--- 
title: "Protsessi kanban-töö ettevalmistamine, kui materjalid on tööraku jaoks saadaval"
description: "See ülesanne keskendub protsessi kanban-töö ettevalmistamisele, kui kõik materjalid on tööraku puhul saadaval."
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 714196ba92fe3f57c80809930ed54705a4e75078
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="2b0f2-103">Protsessi kanban-töö ettevalmistamine, kui materjalid on tööraku jaoks saadaval</span><span class="sxs-lookup"><span data-stu-id="2b0f2-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2b0f2-104">See ülesanne keskendub protsessi kanban-töö ettevalmistamisele, kui kõik materjalid on tööraku puhul saadaval.</span><span class="sxs-lookup"><span data-stu-id="2b0f2-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="2b0f2-105">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="2b0f2-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="2b0f2-106">See ülesanne on mõeldud masinaoperaatorile.</span><span class="sxs-lookup"><span data-stu-id="2b0f2-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="2b0f2-107">Avage Protsessitööde kanban-tahvel.</span><span class="sxs-lookup"><span data-stu-id="2b0f2-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="2b0f2-108">Klõpsake väljal Töörakk otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="2b0f2-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="2b0f2-109">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="2b0f2-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2b0f2-110">Valige töörakk 1250 ja klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2b0f2-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="2b0f2-111">Valige loendist rida 4.</span><span class="sxs-lookup"><span data-stu-id="2b0f2-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="2b0f2-112">Puhtas demoettevõttes on Kanban 000329 real 4 esimene töö, mis pole veel lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="2b0f2-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="2b0f2-113">Laiendage jaotist Komplekteerimisleht.</span><span class="sxs-lookup"><span data-stu-id="2b0f2-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="2b0f2-114">Kontrollige, kas tarneolek on saadaval kõigi komplekteerimiselehe kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="2b0f2-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="2b0f2-115">Mitme töö valimisel kuvab komplekteerimisleht kõikide valitud tööde puhul vajalike kaupade summa.</span><span class="sxs-lookup"><span data-stu-id="2b0f2-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="2b0f2-116">Klõpsake suvandit Valmista ette.</span><span class="sxs-lookup"><span data-stu-id="2b0f2-116">Click Prepare.</span></span>
    * <span data-ttu-id="2b0f2-117">Ettevalmistamise protsess on nüüd lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="2b0f2-117">The preparation process is now completed.</span></span> <span data-ttu-id="2b0f2-118">Kõigi komplekteerimislehe ridade puhul valitud märkeruut näitab, et tarneolek on komplekteeritud.</span><span class="sxs-lookup"><span data-stu-id="2b0f2-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  


