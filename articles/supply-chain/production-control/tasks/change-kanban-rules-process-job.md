--- 
title: "Kanban-reeglite muutmine protsessitöö jaoks"
description: Protseduur keskendub konkreetse kanbani kasutatud kanban-reegli muutmisele.
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 8fc47751534af69300bf8f0bdb7424043cab7b26
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="ac685-103">Kanban-reeglite muutmine protsessitöö jaoks</span><span class="sxs-lookup"><span data-stu-id="ac685-103">Change kanban rules for a process job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ac685-104">Protseduur keskendub konkreetse kanbani kasutatud kanban-reegli muutmisele.</span><span class="sxs-lookup"><span data-stu-id="ac685-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="ac685-105">See on kasulik koormuse ressursside tasakaalustamiseks või katkestuse korral.</span><span class="sxs-lookup"><span data-stu-id="ac685-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="ac685-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="ac685-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ac685-107">Protseduur on mõeldud plaanijale, kes töötab lean manufacturingil põhinevas ettevõttes ja vastutab väärtuse voo eest.</span><span class="sxs-lookup"><span data-stu-id="ac685-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="ac685-108">Kanban-reegli kopeerimine</span><span class="sxs-lookup"><span data-stu-id="ac685-108">Copy kanban rule</span></span>
1. <span data-ttu-id="ac685-109">Minge jaotisse Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="ac685-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="ac685-110">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ac685-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ac685-111">Valige sündmuse kanban-reegel 000022 üksusele L0001.</span><span class="sxs-lookup"><span data-stu-id="ac685-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="ac685-112">Klõpsake suvandit Kanban-reegli dubleerimine.</span><span class="sxs-lookup"><span data-stu-id="ac685-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="ac685-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ac685-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="ac685-114">Kanban-reegli muutmine</span><span class="sxs-lookup"><span data-stu-id="ac685-114">Change kanban rule</span></span>
1. <span data-ttu-id="ac685-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ac685-115">Close the page.</span></span>
2. <span data-ttu-id="ac685-116">Avage kanban-töö plaanimine.</span><span class="sxs-lookup"><span data-stu-id="ac685-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="ac685-117">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="ac685-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ac685-118">Valige rida, millel on Kanban 000177.</span><span class="sxs-lookup"><span data-stu-id="ac685-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="ac685-119">Klõpsake suvandit Alternatiivse kanban-reegli kasutamine.</span><span class="sxs-lookup"><span data-stu-id="ac685-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="ac685-120">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="ac685-120">Click Next.</span></span>
6. <span data-ttu-id="ac685-121">Valige või sisestage väärtus väljal Kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="ac685-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="ac685-122">Valige varem loodud kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="ac685-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="ac685-123">See on suurima numbriga kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="ac685-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="ac685-124">Klõpsake Lõpeta.</span><span class="sxs-lookup"><span data-stu-id="ac685-124">Click Finish.</span></span>
    * <span data-ttu-id="ac685-125">Praegu kasutab kanban-töö muud kanban-reeglit.</span><span class="sxs-lookup"><span data-stu-id="ac685-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="ac685-126">See võib olla kasulik töörakkude koormuse tasakaalustamiseks.</span><span class="sxs-lookup"><span data-stu-id="ac685-126">This can be useful to level load work cells.</span></span>  


