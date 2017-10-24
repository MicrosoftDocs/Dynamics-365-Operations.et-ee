--- 
title: "Tootmistööde järjestamine tootmisprotsessiks"
description: "See protseduur kasutab värvitooteid näitena näitamaks, kuidas järjestada plaanitud tellimusi vastavalt värvi ja suuruse prioriteedile."
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
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a25a4575ca1600b07b2dac5949c8775bcd162650
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="e5c60-103">Tootmistööde järjestamine tootmisprotsessiks</span><span class="sxs-lookup"><span data-stu-id="e5c60-103">Sequence production jobs for process manufacturing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e5c60-104">See protseduur kasutab värvitooteid näitena näitamaks, kuidas järjestada plaanitud tellimusi vastavalt värvi ja suuruse prioriteedile.</span><span class="sxs-lookup"><span data-stu-id="e5c60-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="e5c60-105">Selle protseduuri loomiseks kasutati demoettevõtte USPI-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="e5c60-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="e5c60-106">See protseduur on mõeldud tootmisplaanijale.</span><span class="sxs-lookup"><span data-stu-id="e5c60-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="e5c60-107">Koondplaneerimise käitamine USPI jaoks</span><span class="sxs-lookup"><span data-stu-id="e5c60-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="e5c60-108">Avage Koondplaneerimine > Koondplaneerimine > Käivita > Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="e5c60-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="e5c60-109">Klõpsake väljal Koondplaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e5c60-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e5c60-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e5c60-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e5c60-111">Tehke valik MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="e5c60-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="e5c60-112">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e5c60-112">Click OK.</span></span>
    * <span data-ttu-id="e5c60-113">See käivitab koondplaneerimise, sh jada protsessi.</span><span class="sxs-lookup"><span data-stu-id="e5c60-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="e5c60-114">Protsessiks võib kuluda mõni minut.</span><span class="sxs-lookup"><span data-stu-id="e5c60-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="e5c60-115">Värvitoodete plaanitud tellimuste vaatamine</span><span class="sxs-lookup"><span data-stu-id="e5c60-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="e5c60-116">Avage Koondplaneerimine > Koondplaneerimine > Plaanitud tellimused.</span><span class="sxs-lookup"><span data-stu-id="e5c60-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="e5c60-117">Laiendage kiirinfor Kauba üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="e5c60-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="e5c60-118">Laiendage kiirinfot Graafiku üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="e5c60-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="e5c60-119">Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e5c60-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e5c60-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e5c60-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e5c60-121">Tehke valik MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="e5c60-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="e5c60-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e5c60-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e5c60-123">Kasutage kiirfiltrit, et filtreerida väli Kaubakood väärtuse P300 alusel.</span><span class="sxs-lookup"><span data-stu-id="e5c60-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="e5c60-124">Avage ja kerimige paremale, et näha tellimuse kuupäeva ja tarnekuupäeva.</span><span class="sxs-lookup"><span data-stu-id="e5c60-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="e5c60-125">Pange tähele, et nendel kaupadel on tellimuse kuupäev täna ja plaanitud tellimuste tarnekuupäevad ei ole järjestatud värvi ja pakendi suuruse prioriteedi järgi, nagu on näidatud toote nimes.</span><span class="sxs-lookup"><span data-stu-id="e5c60-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="e5c60-126">Toote nime ja prioriteedi nägemiseks hõljutage kursorit kaubakoodil.</span><span class="sxs-lookup"><span data-stu-id="e5c60-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="e5c60-127">Seeria plaanitud tellimused värvi jaoks</span><span class="sxs-lookup"><span data-stu-id="e5c60-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="e5c60-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e5c60-128">Close the page.</span></span>
2. <span data-ttu-id="e5c60-129">Avage Koondplaneerimine > Koondplaneerimine > Järjestatud plaanitud tellimused.</span><span class="sxs-lookup"><span data-stu-id="e5c60-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="e5c60-130">Laiendage kiirinfor Kauba üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="e5c60-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="e5c60-131">Laiendage kiirinfot Graafiku üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="e5c60-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="e5c60-132">Märkus. Siin näete, et plaanitud tellimuste alguskuupäevad/-kellaajad on järjestatud vastavalt värvi ja pakendi suuruse järgi 28-päevase ajavahemiku jooksul.</span><span class="sxs-lookup"><span data-stu-id="e5c60-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="e5c60-133">Need perioodid määratletakse numbriga väljal Kampaania.</span><span class="sxs-lookup"><span data-stu-id="e5c60-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="e5c60-134">Seeria plaanitud tellimuse vorm toimib nagu tavaline plaanitud tellimuse vorm ja tootmise plaanija saab kinnitada siin plaanitud tellimused.</span><span class="sxs-lookup"><span data-stu-id="e5c60-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="e5c60-135">Märkige kõik read.</span><span class="sxs-lookup"><span data-stu-id="e5c60-135">Mark all rows.</span></span>
6. <span data-ttu-id="e5c60-136">Klõpsake suvandit Nõustu.</span><span class="sxs-lookup"><span data-stu-id="e5c60-136">Click Accept.</span></span>
    * <span data-ttu-id="e5c60-137">See värskendab plaanitud tellimused valitud toimingute järjestusega, milleks on kas Edasi lükata või Varasem.</span><span class="sxs-lookup"><span data-stu-id="e5c60-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="e5c60-138">Plaanitud tellimuste seeria kinnitamine</span><span class="sxs-lookup"><span data-stu-id="e5c60-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="e5c60-139">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e5c60-139">Close the page.</span></span>
2. <span data-ttu-id="e5c60-140">Avage Koondplaneerimine > Koondplaneerimine > Plaanitud tellimused.</span><span class="sxs-lookup"><span data-stu-id="e5c60-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="e5c60-141">Laiendage kiirinfor Kauba üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="e5c60-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="e5c60-142">Laiendage kiirinfot Graafiku üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="e5c60-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="e5c60-143">Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e5c60-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e5c60-144">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e5c60-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e5c60-145">Tehke valik MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="e5c60-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="e5c60-146">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e5c60-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e5c60-147">Kasutage kiirfiltrit, et filtreerida väli Kaubakood väärtuse P300 alusel.</span><span class="sxs-lookup"><span data-stu-id="e5c60-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="e5c60-148">Pange tähele, et tellimused on nüüd järjestatud vastavalt värvi ja suuruse prioriteedile ning plaanitud tellimused algavad varaseimal tellimuse kuupäeval ja tarnekuupäeval.</span><span class="sxs-lookup"><span data-stu-id="e5c60-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="e5c60-149">Kinnitage veerg Tellimuse kuupäev või Alguskuupäev kiiinfos Graafiku üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="e5c60-149">Validate the Order date column or the Start date in the Schedule details FactBbox.</span></span>  


