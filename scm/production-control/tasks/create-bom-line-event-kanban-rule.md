--- 
title: "Koosluserea sündmuse kanban-reegli loomine"
description: "See toiming keskendub seadistusele, mida on vaja sündmuse kanban-reegli loomiseks, et tagada tootmise koosluseridade varud segatud kulusäästlikus ja klassikalises tootmiskeskkonnas."
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 452cc5cf6060b71f91ad43e39e756dc23d759448
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="bac90-103">Koosluserea sündmuse kanban-reegli loomine</span><span class="sxs-lookup"><span data-stu-id="bac90-103">Create a BOM line event kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bac90-104">See toiming keskendub seadistusele, mida on vaja sündmuse kanban-reegli loomiseks, et tagada tootmise koosluseridade varud segatud kulusäästlikus ja klassikalises tootmiskeskkonnas.</span><span class="sxs-lookup"><span data-stu-id="bac90-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="bac90-105">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="bac90-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="bac90-106">See ülesanne on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud toote tootmist.</span><span class="sxs-lookup"><span data-stu-id="bac90-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="bac90-107">Looge uus kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="bac90-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="bac90-108">Avage Tootmise juhtimine > Perioodilised ülesanded > Kanban-koguse arvutamine > Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="bac90-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="bac90-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="bac90-109">Click New.</span></span>
3. <span data-ttu-id="bac90-110">Tehke väljal Tüüp vali Tühistamine.</span><span class="sxs-lookup"><span data-stu-id="bac90-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="bac90-111">Tühistamise tüüpi kasutatakse ülekande-kanbanide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="bac90-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="bac90-112">Valige väljal Täiendusstrateegia suvand Sündmus.</span><span class="sxs-lookup"><span data-stu-id="bac90-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="bac90-113">Sündmuse alusel kanbanide ülekandmise loomiseks valitakse sündmuse strateegia.</span><span class="sxs-lookup"><span data-stu-id="bac90-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="bac90-114">Hiljem käivitame selle ülesande juhendis, hinnates tootmistellimust.</span><span class="sxs-lookup"><span data-stu-id="bac90-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="bac90-115">Sisestage või valige väärtus väljal Esimene plaanitegevus.</span><span class="sxs-lookup"><span data-stu-id="bac90-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="bac90-116">Sisestage või valige väärtus ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="bac90-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="bac90-117">Sellel ülekandmistegevusel on sissetulev (väljund) ladu ja asukoht 12, mis tähendab, et materjal teisaldatakse asukohta 12 laos 12.</span><span class="sxs-lookup"><span data-stu-id="bac90-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="bac90-118">Laiendage jaotist Üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="bac90-118">Expand the Details section.</span></span>
7. <span data-ttu-id="bac90-119">Sisestage või valige väljal Toode väärtus M0001.</span><span class="sxs-lookup"><span data-stu-id="bac90-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="bac90-120">Laiendage jaotist Sündmused.</span><span class="sxs-lookup"><span data-stu-id="bac90-120">Expand the Events section.</span></span>
9. <span data-ttu-id="bac90-121">Valige väljal Koosluse rea sündmus väärtus Automaatne.</span><span class="sxs-lookup"><span data-stu-id="bac90-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="bac90-122">Kui välja Koosluse rea sündmus väärtuseks on Automaatne, luuakse kanban, et täita tootmistellimuse koosluse ridade materjalivajadused.</span><span class="sxs-lookup"><span data-stu-id="bac90-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="bac90-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bac90-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="bac90-124">Uue tootmistellimuse loomine ja muutmine</span><span class="sxs-lookup"><span data-stu-id="bac90-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="bac90-125">Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="bac90-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="bac90-126">Klõpsake valikut Uus tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="bac90-126">Click New production order.</span></span>
3. <span data-ttu-id="bac90-127">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="bac90-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="bac90-128">Sisestage või valige väärtus L0001.</span><span class="sxs-lookup"><span data-stu-id="bac90-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="bac90-129">Kasutame kaupa L0001, sest kaup M0001 on lisatud kooslusse kauba L0001 puhul.</span><span class="sxs-lookup"><span data-stu-id="bac90-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="bac90-130">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="bac90-130">Click Create.</span></span>
5. <span data-ttu-id="bac90-131">Klõpsake loendis linki väärtuse L0001 real</span><span class="sxs-lookup"><span data-stu-id="bac90-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="bac90-132">Klõpsake valikut Kooslus.</span><span class="sxs-lookup"><span data-stu-id="bac90-132">Click BOM.</span></span>
7. <span data-ttu-id="bac90-133">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="bac90-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="bac90-134">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="bac90-134">Click Edit.</span></span>
9. <span data-ttu-id="bac90-135">Valige väljal Rea tüüp väärtus Kinnistatud tarne.</span><span class="sxs-lookup"><span data-stu-id="bac90-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="bac90-136">Kinnistatud tarne on valitud, et käivitada kanbani pakkumise loomine.</span><span class="sxs-lookup"><span data-stu-id="bac90-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="bac90-137">Tehke väljal Ressursi tarbimine valik Ei.</span><span class="sxs-lookup"><span data-stu-id="bac90-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="bac90-138">Märkeruudu Ressursi tarbimine tühjendamist võimaldab meil ladu muuta.</span><span class="sxs-lookup"><span data-stu-id="bac90-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="bac90-139">Laiendage jaotist Varude dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="bac90-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="bac90-140">Sisestage väljale Ladu väärtus 12.</span><span class="sxs-lookup"><span data-stu-id="bac90-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="bac90-141">Ladu on seadistatud režiimile 12, sest see on tühistamistegevuse väljundi ladu.</span><span class="sxs-lookup"><span data-stu-id="bac90-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="bac90-142">Tippige väljale Asukoht väärtus 12.</span><span class="sxs-lookup"><span data-stu-id="bac90-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="bac90-143">Asukohaks on seatud 12, sest see on tühistamistegevuse väljundi asukoht.</span><span class="sxs-lookup"><span data-stu-id="bac90-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="bac90-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bac90-144">Close the page.</span></span>
15. <span data-ttu-id="bac90-145">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bac90-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="bac90-146">Tootmistellimuse hindamine ja loodud kanbani kuvamine</span><span class="sxs-lookup"><span data-stu-id="bac90-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="bac90-147">Klõpsake suvandit Hinnang.</span><span class="sxs-lookup"><span data-stu-id="bac90-147">Click Estimate.</span></span>
    * <span data-ttu-id="bac90-148">Tootmistellimuse hindamine käivitab seostatud kanbani loomise tarnekaubale M0001.</span><span class="sxs-lookup"><span data-stu-id="bac90-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="bac90-149">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="bac90-149">Click OK.</span></span>
3. <span data-ttu-id="bac90-150">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bac90-150">Close the page.</span></span>
4. <span data-ttu-id="bac90-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bac90-151">Close the page.</span></span>
5. <span data-ttu-id="bac90-152">Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="bac90-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="bac90-153">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="bac90-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="bac90-154">Valige sündmuse kanban-reegel, mis on loodud kaubale M0001.</span><span class="sxs-lookup"><span data-stu-id="bac90-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="bac90-155">Laiendage jaotist Kanbanid.</span><span class="sxs-lookup"><span data-stu-id="bac90-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="bac90-156">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bac90-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bac90-157">Pange tähele kanbani, mis on loodud M0001 tarneks hinnangulise tootmistellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="bac90-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="bac90-158">See on viimane etapp!</span><span class="sxs-lookup"><span data-stu-id="bac90-158">This is the last step!</span></span>  


