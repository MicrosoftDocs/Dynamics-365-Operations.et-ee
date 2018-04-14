--- 
title: "Minimaalsete laovarude sündmuse abil kanban-reegli loomine"
description: "See protseduur keskendub seadistusele, mis on vajalik kanban-reegli loomiseks, kasutades minimaalset laosündmust tagamiseks, et konkreetne toode oleks alati konkreetses asukohas saadaval."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c5f795f8d3c31c9acdbddd94879dbd427145956c
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="8ecb7-103">Minimaalsete laovarude sündmuse abil kanban-reegli loomine</span><span class="sxs-lookup"><span data-stu-id="8ecb7-103">Create a kanban rule using a minimum stock event</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ecb7-104">See protseduur keskendub seadistusele, mis on vajalik kanban-reegli loomiseks, kasutades minimaalset laosündmust tagamiseks, et konkreetne toode oleks alati konkreetses asukohas saadaval.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="8ecb7-105">Luuakse kanban-reegel materjali üleviimiseks asukohta, kui varude tase langeb alla 200 ühiku.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="8ecb7-106">Sidumissündmuse töötlemise käivitamisega luuakse vajalikud kanbanid.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="8ecb7-107">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="8ecb7-108">See toiming on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud toote tootmist säästlikus keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="8ecb7-109">Looge uus kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="8ecb7-110">Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="8ecb7-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-111">Click New.</span></span>
3. <span data-ttu-id="8ecb7-112">Tehke väljal Tüüp vali Tühistamine.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="8ecb7-113">Seda tüüpi kasutatakse ülekande-kanbanide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="8ecb7-114">Valige väljal Täiendusstrateegia suvand Sündmus.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="8ecb7-115">Sündmusel põhinevate kanbanide ülekandmise loomiseks kasutatakse sündmuse strateegiat.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="8ecb7-116">Edaspidi käivitate protseduuris üleviimise kanbanid, kasutades varude täiendamist.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="8ecb7-117">Sisestage või valige väärtus väljal Esimene plaanitegevus.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="8ecb7-118">Sisestage või valige väärtus ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="8ecb7-119">Sellel ülekandmistegevusel on sissetulev (väljund) ladu ja asukoht 12, mis tähendab, et materjalid teisaldatakse asukohta 12 laos 12.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="8ecb7-120">Laiendage jaotist Üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-120">Expand the Details section.</span></span>
7. <span data-ttu-id="8ecb7-121">Sisestage või valige väärtus väljal Toode.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="8ecb7-122">Valige suvand M0007.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-122">Select M0007.</span></span>  
8. <span data-ttu-id="8ecb7-123">Laiendage jaotist Sündmused.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-123">Expand the Events section.</span></span>
9. <span data-ttu-id="8ecb7-124">Valige väljalt Varude täiendamise sündmus väärtus Partii.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="8ecb7-125">See loob kanbanid materjalivajaduste rahuldamiseks seotud asukohas sidumissündmuse töötlemise ajal.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="8ecb7-126">Määrake kauba miinimumkogus</span><span class="sxs-lookup"><span data-stu-id="8ecb7-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="8ecb7-127">Klõpsake, et järgida linki väljal Toode.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="8ecb7-128">Klõpsake, et järgida linki väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="8ecb7-129">Laiendage toote pildi kiirinfot.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="8ecb7-130">Klõpsake toimingupaanil valikut Plaan.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="8ecb7-131">Klõpsake valikut Kauba laovarud.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-131">Click Item coverage.</span></span>
6. <span data-ttu-id="8ecb7-132">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-132">Click New.</span></span>
7. <span data-ttu-id="8ecb7-133">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="8ecb7-134">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="8ecb7-135">Valige välja Ladu väärtuseks 12.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="8ecb7-136">Määra valiku Miinimum väärtuseks 200.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="8ecb7-137">Käivitage pakettsündmuse loomise töö</span><span class="sxs-lookup"><span data-stu-id="8ecb7-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="8ecb7-138">Avage Tootmise juhtimine > Perioodilised ülesanded > Kanban-töö pakktöötlus > Sidumissündmuse töötlemine.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="8ecb7-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-139">Click OK.</span></span>
3. <span data-ttu-id="8ecb7-140">Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="8ecb7-141">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8ecb7-142">Valige varem loodud kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="8ecb7-143">Laiendage jaotist Kanbanid.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="8ecb7-144">Pange tähele, et kanban loodi vajaliku materjali üleviimiseks lattu 12.</span><span class="sxs-lookup"><span data-stu-id="8ecb7-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  


