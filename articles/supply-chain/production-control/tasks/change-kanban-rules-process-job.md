---
title: Kanban-reeglite muutmine protsessitöö jaoks
description: Protseduur keskendub konkreetse kanbani kasutatud kanban-reegli muutmisele.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d4c8fd8251aca2cc53e59afe4c104f2e5198426
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210958"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="625ac-103">Kanban-reeglite muutmine protsessitöö jaoks</span><span class="sxs-lookup"><span data-stu-id="625ac-103">Change kanban rules for a process job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="625ac-104">Protseduur keskendub konkreetse kanbani kasutatud kanban-reegli muutmisele.</span><span class="sxs-lookup"><span data-stu-id="625ac-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="625ac-105">See on kasulik koormuse ressursside tasakaalustamiseks või katkestuse korral.</span><span class="sxs-lookup"><span data-stu-id="625ac-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="625ac-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="625ac-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="625ac-107">Protseduur on mõeldud plaanijale, kes töötab lean manufacturingil põhinevas ettevõttes ja vastutab väärtuse voo eest.</span><span class="sxs-lookup"><span data-stu-id="625ac-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="625ac-108">Kanban-reegli kopeerimine</span><span class="sxs-lookup"><span data-stu-id="625ac-108">Copy kanban rule</span></span>
1. <span data-ttu-id="625ac-109">Minge jaotisse Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="625ac-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="625ac-110">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="625ac-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="625ac-111">Valige sündmuse kanban-reegel 000022 üksusele L0001.</span><span class="sxs-lookup"><span data-stu-id="625ac-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="625ac-112">Klõpsake suvandit Kanban-reegli dubleerimine.</span><span class="sxs-lookup"><span data-stu-id="625ac-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="625ac-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="625ac-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="625ac-114">Kanban-reegli muutmine</span><span class="sxs-lookup"><span data-stu-id="625ac-114">Change kanban rule</span></span>
1. <span data-ttu-id="625ac-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="625ac-115">Close the page.</span></span>
2. <span data-ttu-id="625ac-116">Avage kanban-töö plaanimine.</span><span class="sxs-lookup"><span data-stu-id="625ac-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="625ac-117">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="625ac-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="625ac-118">Valige rida, millel on Kanban 000177.</span><span class="sxs-lookup"><span data-stu-id="625ac-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="625ac-119">Klõpsake suvandit Alternatiivse kanban-reegli kasutamine.</span><span class="sxs-lookup"><span data-stu-id="625ac-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="625ac-120">Klõpsake käsku Edasi.</span><span class="sxs-lookup"><span data-stu-id="625ac-120">Click Next.</span></span>
6. <span data-ttu-id="625ac-121">Valige või sisestage väärtus väljal Kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="625ac-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="625ac-122">Valige varem loodud kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="625ac-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="625ac-123">See on suurima numbriga kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="625ac-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="625ac-124">Klõpsake Lõpeta.</span><span class="sxs-lookup"><span data-stu-id="625ac-124">Click Finish.</span></span>
    * <span data-ttu-id="625ac-125">Praegu kasutab kanban-töö muud kanban-reeglit.</span><span class="sxs-lookup"><span data-stu-id="625ac-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="625ac-126">See võib olla kasulik töörakkude koormuse tasakaalustamiseks.</span><span class="sxs-lookup"><span data-stu-id="625ac-126">This can be useful to level load work cells.</span></span>  

