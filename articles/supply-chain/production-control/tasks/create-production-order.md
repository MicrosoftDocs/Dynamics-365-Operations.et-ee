---
title: Tootmistellimuse loomine
description: Selles protseduuris näitlikustatakse, kuidas luua tootmistellimust.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdTable, ProdBOM, ProdRoute, ProdJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81caa6693d86c797d8565270094556ae4e103e6a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998674"
---
# <a name="create-a-production-order"></a><span data-ttu-id="c1859-103">Tootmistellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="c1859-103">Create a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1859-104">Selles protseduuris näitlikustatakse, kuidas luua tootmistellimust.</span><span class="sxs-lookup"><span data-stu-id="c1859-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="c1859-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="c1859-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c1859-106">See on esimene protseduur seitsmest, mis selgitab tootmistellimuse elutsüklit.</span><span class="sxs-lookup"><span data-stu-id="c1859-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="c1859-107">Tootmistellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="c1859-107">Create a production order</span></span>
1. <span data-ttu-id="c1859-108">Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="c1859-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="c1859-109">Klõpsake valikut Uus tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="c1859-109">Click New production order.</span></span>
3. <span data-ttu-id="c1859-110">Sisestage väljale Kaubakood tüüp D0001.</span><span class="sxs-lookup"><span data-stu-id="c1859-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="c1859-111">Sisestage tarnekuupäev väljale Tarne.</span><span class="sxs-lookup"><span data-stu-id="c1859-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="c1859-112">Tarnekuupäev näitab, millal peab tootmistellimus lõppema, et tarne toimuks tähtaegselt.</span><span class="sxs-lookup"><span data-stu-id="c1859-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="c1859-113">Seda kuupäeva saab planeerimisprotsessis kasutada.</span><span class="sxs-lookup"><span data-stu-id="c1859-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="c1859-114">Näiteks saate tellimuse planeerida tellimuse jaoks määratud tarnekuupäevast tagasi.</span><span class="sxs-lookup"><span data-stu-id="c1859-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="c1859-115">Määrake koguse väärtuseks 20.</span><span class="sxs-lookup"><span data-stu-id="c1859-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="c1859-116">Märkus: koosluse numbri väljal kuvatakse automaatselt praeguse kauba aktiivse koosluse number, kuid saate tootmistellimuse kooslust muuta, valides aktiivse koosluse kinnitatud koosluse versioonide loendist.</span><span class="sxs-lookup"><span data-stu-id="c1859-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="c1859-117">Märkus: protsessi numbri väljal kuvatakse automaatselt praeguse kauba aktiivse protsessi number, kuid saate tootmistellimuse protsessi muuta, valides aktiivse protsessi kinnitatud protsessi versioonide loendist.</span><span class="sxs-lookup"><span data-stu-id="c1859-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="c1859-118">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="c1859-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="c1859-119">Tootmistellimuse kinnitamine</span><span class="sxs-lookup"><span data-stu-id="c1859-119">Validate the production order</span></span>
1. <span data-ttu-id="c1859-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c1859-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c1859-121">Klõpsake loodud tootmistellimuse numbri linki.</span><span class="sxs-lookup"><span data-stu-id="c1859-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="c1859-122">Avaneb leht tellimuse üksikasjade kohta.</span><span class="sxs-lookup"><span data-stu-id="c1859-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="c1859-123">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="c1859-123">Click Edit.</span></span>
3. <span data-ttu-id="c1859-124">Sisestage tarnekuupäev väljale Tarne.</span><span class="sxs-lookup"><span data-stu-id="c1859-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="c1859-125">Näiteks saate muuta tootmistellimuse tarnekuupäeva.</span><span class="sxs-lookup"><span data-stu-id="c1859-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="c1859-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="c1859-126">Click Save.</span></span>
5. <span data-ttu-id="c1859-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c1859-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="c1859-128">Koosluse värskendus</span><span class="sxs-lookup"><span data-stu-id="c1859-128">Update the BOM</span></span>
1. <span data-ttu-id="c1859-129">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="c1859-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="c1859-130">Klõpsake valikut Kooslus.</span><span class="sxs-lookup"><span data-stu-id="c1859-130">Click BOM.</span></span>
    * <span data-ttu-id="c1859-131">Tootmistellimuse loomisel kopeeritud koosluse vaikeandmete kinnitamiseks avage leht Kooslus.</span><span class="sxs-lookup"><span data-stu-id="c1859-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="c1859-132">Selles protseduuris peate koosluse kogust uuendama.</span><span class="sxs-lookup"><span data-stu-id="c1859-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="c1859-133">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="c1859-133">Click Edit.</span></span>
4. <span data-ttu-id="c1859-134">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="c1859-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="c1859-135">Koguse muutmine koosluse real mõjutab tootmistellimuse materjalitarbimise kuluhinnangut.</span><span class="sxs-lookup"><span data-stu-id="c1859-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="c1859-136">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="c1859-136">Click Save.</span></span>
6. <span data-ttu-id="c1859-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c1859-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="c1859-138">Tootmisprotsessi värskendus</span><span class="sxs-lookup"><span data-stu-id="c1859-138">Update the production route</span></span>
1. <span data-ttu-id="c1859-139">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="c1859-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="c1859-140">Klõpsake valikut Protsess.</span><span class="sxs-lookup"><span data-stu-id="c1859-140">Click Route.</span></span>
    * <span data-ttu-id="c1859-141">Tellimuse loomisel kopeeritud tootmisprotsessi vaikeandmete kinnitamiseks avage leht Protsess.</span><span class="sxs-lookup"><span data-stu-id="c1859-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="c1859-142">Selles protseduuris peaksite uuendama ühe tootmisprotsessi operatsioonide kogust.</span><span class="sxs-lookup"><span data-stu-id="c1859-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="c1859-143">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c1859-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="c1859-144">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="c1859-144">Click Edit.</span></span>
5. <span data-ttu-id="c1859-145">Sisestage arv väljale Protsessi kogus.</span><span class="sxs-lookup"><span data-stu-id="c1859-145">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="c1859-146">Töötlusaja muutmine mõjutab hinnangulist protsessi tarbimist ja tootmistellimuse kulu.</span><span class="sxs-lookup"><span data-stu-id="c1859-146">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="c1859-147">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="c1859-147">Click Save.</span></span>
7. <span data-ttu-id="c1859-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c1859-148">Close the page.</span></span>

