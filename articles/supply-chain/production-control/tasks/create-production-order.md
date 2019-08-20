---
title: Tootmistellimuse loomine
description: Selles protseduuris näitlikustatakse, kuidas luua tootmistellimust.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdTable, ProdBOM, ProdRoute
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67a15a5c52bd1032c8bee8652f1f13d1f1a4cb64
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838579"
---
# <a name="create-a-production-order"></a><span data-ttu-id="109cb-103">Tootmistellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="109cb-103">Create a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="109cb-104">Selles protseduuris näitlikustatakse, kuidas luua tootmistellimust.</span><span class="sxs-lookup"><span data-stu-id="109cb-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="109cb-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="109cb-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="109cb-106">See on esimene protseduur seitsmest, mis selgitab tootmistellimuse elutsüklit.</span><span class="sxs-lookup"><span data-stu-id="109cb-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="109cb-107">Tootmistellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="109cb-107">Create a production order</span></span>
1. <span data-ttu-id="109cb-108">Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="109cb-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="109cb-109">Klõpsake valikut Uus tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="109cb-109">Click New production order.</span></span>
3. <span data-ttu-id="109cb-110">Sisestage väljale Kaubakood tüüp D0001.</span><span class="sxs-lookup"><span data-stu-id="109cb-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="109cb-111">Sisestage tarnekuupäev väljale Tarne.</span><span class="sxs-lookup"><span data-stu-id="109cb-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="109cb-112">Tarnekuupäev näitab, millal peab tootmistellimus lõppema, et tarne toimuks tähtaegselt.</span><span class="sxs-lookup"><span data-stu-id="109cb-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="109cb-113">Seda kuupäeva saab planeerimisprotsessis kasutada.</span><span class="sxs-lookup"><span data-stu-id="109cb-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="109cb-114">Näiteks saate tellimuse planeerida tellimuse jaoks määratud tarnekuupäevast tagasi.</span><span class="sxs-lookup"><span data-stu-id="109cb-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="109cb-115">Määrake koguse väärtuseks 20.</span><span class="sxs-lookup"><span data-stu-id="109cb-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="109cb-116">Märkus: koosluse numbri väljal kuvatakse automaatselt praeguse kauba aktiivse koosluse number, kuid saate tootmistellimuse kooslust muuta, valides aktiivse koosluse kinnitatud koosluse versioonide loendist.</span><span class="sxs-lookup"><span data-stu-id="109cb-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="109cb-117">Märkus: protsessi numbri väljal kuvatakse automaatselt praeguse kauba aktiivse protsessi number, kuid saate tootmistellimuse protsessi muuta, valides aktiivse protsessi kinnitatud protsessi versioonide loendist.</span><span class="sxs-lookup"><span data-stu-id="109cb-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="109cb-118">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="109cb-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="109cb-119">Tootmistellimuse kinnitamine</span><span class="sxs-lookup"><span data-stu-id="109cb-119">Validate the production order</span></span>
1. <span data-ttu-id="109cb-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="109cb-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="109cb-121">Klõpsake loodud tootmistellimuse numbri linki.</span><span class="sxs-lookup"><span data-stu-id="109cb-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="109cb-122">Avaneb leht tellimuse üksikasjade kohta.</span><span class="sxs-lookup"><span data-stu-id="109cb-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="109cb-123">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="109cb-123">Click Edit.</span></span>
3. <span data-ttu-id="109cb-124">Sisestage tarnekuupäev väljale Tarne.</span><span class="sxs-lookup"><span data-stu-id="109cb-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="109cb-125">Näiteks saate muuta tootmistellimuse tarnekuupäeva.</span><span class="sxs-lookup"><span data-stu-id="109cb-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="109cb-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="109cb-126">Click Save.</span></span>
5. <span data-ttu-id="109cb-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="109cb-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="109cb-128">Koosluse värskendus</span><span class="sxs-lookup"><span data-stu-id="109cb-128">Update the BOM</span></span>
1. <span data-ttu-id="109cb-129">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="109cb-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="109cb-130">Klõpsake valikut Kooslus.</span><span class="sxs-lookup"><span data-stu-id="109cb-130">Click BOM.</span></span>
    * <span data-ttu-id="109cb-131">Tootmistellimuse loomisel kopeeritud koosluse vaikeandmete kinnitamiseks avage leht Kooslus.</span><span class="sxs-lookup"><span data-stu-id="109cb-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="109cb-132">Selles protseduuris peate koosluse kogust uuendama.</span><span class="sxs-lookup"><span data-stu-id="109cb-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="109cb-133">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="109cb-133">Click Edit.</span></span>
4. <span data-ttu-id="109cb-134">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="109cb-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="109cb-135">Koguse muutmine koosluse real mõjutab tootmistellimuse materjalitarbimise kuluhinnangut.</span><span class="sxs-lookup"><span data-stu-id="109cb-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="109cb-136">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="109cb-136">Click Save.</span></span>
6. <span data-ttu-id="109cb-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="109cb-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="109cb-138">Tootmisprotsessi värskendus</span><span class="sxs-lookup"><span data-stu-id="109cb-138">Update the production route</span></span>
1. <span data-ttu-id="109cb-139">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="109cb-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="109cb-140">Klõpsake valikut Protsess.</span><span class="sxs-lookup"><span data-stu-id="109cb-140">Click Route.</span></span>
    * <span data-ttu-id="109cb-141">Tellimuse loomisel kopeeritud tootmisprotsessi vaikeandmete kinnitamiseks avage leht Protsess.</span><span class="sxs-lookup"><span data-stu-id="109cb-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="109cb-142">Selles protseduuris peaksite uuendama ühe tootmisprotsessi operatsioonide kogust.</span><span class="sxs-lookup"><span data-stu-id="109cb-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="109cb-143">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="109cb-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="109cb-144">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="109cb-144">Click Edit.</span></span>
5. <span data-ttu-id="109cb-145">Sisestage arv väljale Protsessi kogus.</span><span class="sxs-lookup"><span data-stu-id="109cb-145">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="109cb-146">Töötlusaja muutmine mõjutab hinnangulist protsessi tarbimist ja tootmistellimuse kulu.</span><span class="sxs-lookup"><span data-stu-id="109cb-146">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="109cb-147">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="109cb-147">Click Save.</span></span>
7. <span data-ttu-id="109cb-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="109cb-148">Close the page.</span></span>

