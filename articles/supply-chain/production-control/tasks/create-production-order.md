---
title: Tootmistellimuse loomine
description: "Selles protseduuris näitlikustatakse, kuidas luua tootmistellimust."
author: johanhoffmann
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
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 4db56f76c7f8ce0cccf85ab04024d9a1e88a8822
ms.contentlocale: et-ee
ms.lasthandoff: 02/06/2018

---
# <a name="create-a-production-order"></a><span data-ttu-id="56e32-103">Tootmistellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="56e32-103">Create a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="56e32-104">Selles protseduuris näitlikustatakse, kuidas luua tootmistellimust.</span><span class="sxs-lookup"><span data-stu-id="56e32-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="56e32-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="56e32-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="56e32-106">See on esimene protseduur seitsmest, mis selgitab tootmistellimuse elutsüklit.</span><span class="sxs-lookup"><span data-stu-id="56e32-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="56e32-107">Tootmistellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="56e32-107">Create a production order</span></span>
1. <span data-ttu-id="56e32-108">Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="56e32-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="56e32-109">Klõpsake valikut Uus tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="56e32-109">Click New production order.</span></span>
3. <span data-ttu-id="56e32-110">Sisestage väljale Kaubakood tüüp D0001.</span><span class="sxs-lookup"><span data-stu-id="56e32-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="56e32-111">Sisestage tarnekuupäev väljale Tarne.</span><span class="sxs-lookup"><span data-stu-id="56e32-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="56e32-112">Tarnekuupäev näitab, millal peab tootmistellimus lõppema, et tarne toimuks tähtaegselt.</span><span class="sxs-lookup"><span data-stu-id="56e32-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="56e32-113">Seda kuupäeva saab planeerimisprotsessis kasutada.</span><span class="sxs-lookup"><span data-stu-id="56e32-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="56e32-114">Näiteks saate tellimuse planeerida tellimuse jaoks määratud tarnekuupäevast tagasi.</span><span class="sxs-lookup"><span data-stu-id="56e32-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="56e32-115">Määrake koguse väärtuseks 20.</span><span class="sxs-lookup"><span data-stu-id="56e32-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="56e32-116">Märkus: koosluse numbri väljal kuvatakse automaatselt praeguse kauba aktiivse koosluse number, kuid saate tootmistellimuse kooslust muuta, valides aktiivse koosluse kinnitatud koosluse versioonide loendist.</span><span class="sxs-lookup"><span data-stu-id="56e32-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="56e32-117">Märkus: protsessi numbri väljal kuvatakse automaatselt praeguse kauba aktiivse protsessi number, kuid saate tootmistellimuse protsessi muuta, valides aktiivse protsessi kinnitatud protsessi versioonide loendist.</span><span class="sxs-lookup"><span data-stu-id="56e32-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="56e32-118">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="56e32-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="56e32-119">Tootmistellimuse kinnitamine</span><span class="sxs-lookup"><span data-stu-id="56e32-119">Validate the production order</span></span>
1. <span data-ttu-id="56e32-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="56e32-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="56e32-121">Klõpsake loodud tootmistellimuse numbri linki.</span><span class="sxs-lookup"><span data-stu-id="56e32-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="56e32-122">Avaneb leht tellimuse üksikasjade kohta.</span><span class="sxs-lookup"><span data-stu-id="56e32-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="56e32-123">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="56e32-123">Click Edit.</span></span>
3. <span data-ttu-id="56e32-124">Sisestage tarnekuupäev väljale Tarne.</span><span class="sxs-lookup"><span data-stu-id="56e32-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="56e32-125">Näiteks saate muuta tootmistellimuse tarnekuupäeva.</span><span class="sxs-lookup"><span data-stu-id="56e32-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="56e32-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="56e32-126">Click Save.</span></span>
5. <span data-ttu-id="56e32-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="56e32-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="56e32-128">Koosluse värskendus</span><span class="sxs-lookup"><span data-stu-id="56e32-128">Update the BOM</span></span>
1. <span data-ttu-id="56e32-129">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="56e32-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="56e32-130">Klõpsake valikut Kooslus.</span><span class="sxs-lookup"><span data-stu-id="56e32-130">Click BOM.</span></span>
    * <span data-ttu-id="56e32-131">Tootmistellimuse loomisel kopeeritud koosluse vaikeandmete kinnitamiseks avage leht Kooslus.</span><span class="sxs-lookup"><span data-stu-id="56e32-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="56e32-132">Selles protseduuris peate koosluse kogust uuendama.</span><span class="sxs-lookup"><span data-stu-id="56e32-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="56e32-133">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="56e32-133">Click Edit.</span></span>
4. <span data-ttu-id="56e32-134">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="56e32-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="56e32-135">Koguse muutmine koosluse real mõjutab tootmistellimuse materjalitarbimise kuluhinnangut.</span><span class="sxs-lookup"><span data-stu-id="56e32-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="56e32-136">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="56e32-136">Click Save.</span></span>
6. <span data-ttu-id="56e32-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="56e32-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="56e32-138">Tootmisprotsessi värskendus</span><span class="sxs-lookup"><span data-stu-id="56e32-138">Update the production route</span></span>
1. <span data-ttu-id="56e32-139">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="56e32-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="56e32-140">Klõpsake valikut Protsess.</span><span class="sxs-lookup"><span data-stu-id="56e32-140">Click Route.</span></span>
    * <span data-ttu-id="56e32-141">Tellimuse loomisel kopeeritud tootmisprotsessi vaikeandmete kinnitamiseks avage leht Protsess.</span><span class="sxs-lookup"><span data-stu-id="56e32-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="56e32-142">Selles protseduuris peaksite uuendama ühe tootmisprotsessi operatsioonide kogust.</span><span class="sxs-lookup"><span data-stu-id="56e32-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="56e32-143">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="56e32-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="56e32-144">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="56e32-144">Click Edit.</span></span>
5. <span data-ttu-id="56e32-145">Sisestage arv väljale Protsessi kogus.</span><span class="sxs-lookup"><span data-stu-id="56e32-145">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="56e32-146">Töötlusaja muutmine mõjutab hinnangulist protsessi tarbimist ja tootmistellimuse kulu.</span><span class="sxs-lookup"><span data-stu-id="56e32-146">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="56e32-147">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="56e32-147">Click Save.</span></span>
7. <span data-ttu-id="56e32-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="56e32-148">Close the page.</span></span>

