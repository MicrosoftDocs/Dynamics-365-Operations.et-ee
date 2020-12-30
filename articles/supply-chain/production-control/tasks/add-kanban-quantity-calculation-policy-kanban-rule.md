---
title: Kanban-koguse arvutuspoliitika lisamine kanban-reeglile
description: See protseduur keskendub kanban-koguse arvutamise poliitika loomisele ja selle lisamisele kanban-reeglisse kanbani suuruse ja koguste optimeerimiseks.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules, KanbanQuantityCalculation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 039c4aaa355cf2b850ded06913e8e39ee8cac543
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425991"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="daec7-103">Kanban-koguse arvutuspoliitika lisamine kanban-reeglile</span><span class="sxs-lookup"><span data-stu-id="daec7-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="daec7-104">See protseduur keskendub kanban-koguse arvutamise poliitika loomisele ja selle lisamisele kanban-reeglisse kanbani suuruse ja koguste optimeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="daec7-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="daec7-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="daec7-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="daec7-106">See protseduur on mõeldud väärtuse voo haldurile.</span><span class="sxs-lookup"><span data-stu-id="daec7-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="daec7-107">See protseduur on eeltingimus protseduuri Kanban koguse soovituste arvutamine loomiseks.</span><span class="sxs-lookup"><span data-stu-id="daec7-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="daec7-108">Kanban-koguse arvutamise poliitika loomine</span><span class="sxs-lookup"><span data-stu-id="daec7-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="daec7-109">Avage Tootmise juhtimine > Perioodilised ülesanded > Kanban-koguse arvutamine > Kanban-koguse arvutamise poliitikad.</span><span class="sxs-lookup"><span data-stu-id="daec7-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="daec7-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="daec7-110">Click New.</span></span>
3. <span data-ttu-id="daec7-111">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="daec7-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="daec7-112">Näiteks sisestage Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="daec7-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="daec7-113">Klõpsake väljal Koondplaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="daec7-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="daec7-114">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="daec7-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="daec7-115">Valige nõudluse arvutamiseks suvand StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="daec7-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="daec7-116">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="daec7-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="daec7-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="daec7-117">Click Save.</span></span>
8. <span data-ttu-id="daec7-118">Sisestage väljale Minimaalne kanban-kogus väärtus 1.</span><span class="sxs-lookup"><span data-stu-id="daec7-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="daec7-119">See on kanban-koguse arvutamisesse kaasatud kanbanide lisaarv.</span><span class="sxs-lookup"><span data-stu-id="daec7-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="daec7-120">Määrake Ohutustegur väärtusele 1.</span><span class="sxs-lookup"><span data-stu-id="daec7-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="daec7-121">See on tegur, mida kasutatakse puhvervaru täiendava koguse arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="daec7-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="daec7-122">Sisestage väljale Päevi enne väärtus 30.</span><span class="sxs-lookup"><span data-stu-id="daec7-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="daec7-123">See on päevade arv enne kanban-koguse arvutamise kuupäeva, mis nõudluse arvutamisse kaasatakse.</span><span class="sxs-lookup"><span data-stu-id="daec7-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="daec7-124">Sisestage väljale Päevi pärast väärtus 30.</span><span class="sxs-lookup"><span data-stu-id="daec7-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="daec7-125">See on päevade arv pärast kanban-koguse arvutamise kuupäeva, mis nõudluse arvutamisse kaasatakse.</span><span class="sxs-lookup"><span data-stu-id="daec7-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="daec7-126">Arvutamiseks kasutatud valemit näidatakse tegelike väärtustega.</span><span class="sxs-lookup"><span data-stu-id="daec7-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="daec7-127">Näiteks Kanban-kogus = ((keskmine igapäevane nõudlus × täitmisaeg × 2,00) / toote kogus materjali käsitlemisühiku kohta) + 1</span><span class="sxs-lookup"><span data-stu-id="daec7-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="daec7-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="daec7-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="daec7-129">Kanban-koguse arvutamise poliitika lisamine kanban-reeglile</span><span class="sxs-lookup"><span data-stu-id="daec7-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="daec7-130">Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="daec7-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="daec7-131">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="daec7-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="daec7-132">Valige selle protseduuri puhul kanban-reegel 000020.</span><span class="sxs-lookup"><span data-stu-id="daec7-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="daec7-133">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="daec7-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="daec7-134">Laiendage jaotist Kanban-koguse arvutamise poliitikad.</span><span class="sxs-lookup"><span data-stu-id="daec7-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="daec7-135">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="daec7-135">Click Add.</span></span>
    * <span data-ttu-id="daec7-136">Lisage kanban-koguse arvutamise poliitika, mille olete eelmises alamülesandes äsja loonud.</span><span class="sxs-lookup"><span data-stu-id="daec7-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="daec7-137">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="daec7-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="daec7-138">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="daec7-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="daec7-139">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="daec7-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="daec7-140">Valige poliitika Speaker2016, mille olete eelmises alamülesandes äsja loonud.</span><span class="sxs-lookup"><span data-stu-id="daec7-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  

