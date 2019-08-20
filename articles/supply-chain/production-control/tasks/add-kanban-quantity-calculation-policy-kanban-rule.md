---
title: Kanban-koguse arvutuspoliitika lisamine kanban-reeglile
description: See protseduur keskendub kanban-koguse arvutamise poliitika loomisele ja selle lisamisele kanban-reeglisse kanbani suuruse ja koguste optimeerimiseks.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 401b01a6128babd6ed345342a65705a0262540e8
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837946"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="97d96-103">Kanban-koguse arvutuspoliitika lisamine kanban-reeglile</span><span class="sxs-lookup"><span data-stu-id="97d96-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97d96-104">See protseduur keskendub kanban-koguse arvutamise poliitika loomisele ja selle lisamisele kanban-reeglisse kanbani suuruse ja koguste optimeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="97d96-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="97d96-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="97d96-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="97d96-106">See protseduur on mõeldud väärtuse voo haldurile.</span><span class="sxs-lookup"><span data-stu-id="97d96-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="97d96-107">See protseduur on eeltingimus protseduuri Kanban koguse soovituste arvutamine loomiseks.</span><span class="sxs-lookup"><span data-stu-id="97d96-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="97d96-108">Kanban-koguse arvutamise poliitika loomine</span><span class="sxs-lookup"><span data-stu-id="97d96-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="97d96-109">Avage Tootmise juhtimine > Perioodilised ülesanded > Kanban-koguse arvutamine > Kanban-koguse arvutamise poliitikad.</span><span class="sxs-lookup"><span data-stu-id="97d96-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="97d96-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="97d96-110">Click New.</span></span>
3. <span data-ttu-id="97d96-111">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="97d96-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="97d96-112">Näiteks sisestage Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="97d96-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="97d96-113">Klõpsake väljal Koondplaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="97d96-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="97d96-114">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="97d96-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="97d96-115">Valige nõudluse arvutamiseks suvand StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="97d96-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="97d96-116">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="97d96-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="97d96-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="97d96-117">Click Save.</span></span>
8. <span data-ttu-id="97d96-118">Sisestage väljale Minimaalne kanban-kogus väärtus 1.</span><span class="sxs-lookup"><span data-stu-id="97d96-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="97d96-119">See on kanban-koguse arvutamisesse kaasatud kanbanide lisaarv.</span><span class="sxs-lookup"><span data-stu-id="97d96-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="97d96-120">Määrake Ohutustegur väärtusele 1.</span><span class="sxs-lookup"><span data-stu-id="97d96-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="97d96-121">See on tegur, mida kasutatakse puhvervaru täiendava koguse arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="97d96-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="97d96-122">Sisestage väljale Päevi enne väärtus 30.</span><span class="sxs-lookup"><span data-stu-id="97d96-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="97d96-123">See on päevade arv enne kanban-koguse arvutamise kuupäeva, mis nõudluse arvutamisse kaasatakse.</span><span class="sxs-lookup"><span data-stu-id="97d96-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="97d96-124">Sisestage väljale Päevi pärast väärtus 30.</span><span class="sxs-lookup"><span data-stu-id="97d96-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="97d96-125">See on päevade arv pärast kanban-koguse arvutamise kuupäeva, mis nõudluse arvutamisse kaasatakse.</span><span class="sxs-lookup"><span data-stu-id="97d96-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="97d96-126">Arvutamiseks kasutatud valemit näidatakse tegelike väärtustega.</span><span class="sxs-lookup"><span data-stu-id="97d96-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="97d96-127">Näiteks Kanban-kogus = ((keskmine igapäevane nõudlus × täitmisaeg × 2,00) / toote kogus materjali käsitlemisühiku kohta) + 1</span><span class="sxs-lookup"><span data-stu-id="97d96-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="97d96-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="97d96-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="97d96-129">Kanban-koguse arvutamise poliitika lisamine kanban-reeglile</span><span class="sxs-lookup"><span data-stu-id="97d96-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="97d96-130">Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="97d96-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="97d96-131">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="97d96-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="97d96-132">Valige selle protseduuri puhul kanban-reegel 000020.</span><span class="sxs-lookup"><span data-stu-id="97d96-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="97d96-133">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="97d96-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="97d96-134">Laiendage jaotist Kanban-koguse arvutamise poliitikad.</span><span class="sxs-lookup"><span data-stu-id="97d96-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="97d96-135">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="97d96-135">Click Add.</span></span>
    * <span data-ttu-id="97d96-136">Lisage kanban-koguse arvutamise poliitika, mille olete eelmises alamülesandes äsja loonud.</span><span class="sxs-lookup"><span data-stu-id="97d96-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="97d96-137">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="97d96-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="97d96-138">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="97d96-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="97d96-139">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="97d96-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="97d96-140">Valige poliitika Speaker2016, mille olete eelmises alamülesandes äsja loonud.</span><span class="sxs-lookup"><span data-stu-id="97d96-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  

