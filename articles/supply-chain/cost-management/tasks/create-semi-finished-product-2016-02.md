--- 
title: Pooltoote loomine (ainult veebruar 2016)
description: "See ülesanne keskendub pooleldi lõpetatud toote loomisele."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1311e27b4080832c6e1aa2b879308f518d2ab001
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-semi-finished-product-february-2016-only"></a><span data-ttu-id="2bbad-103">Pooltoote loomine (ainult veebruar 2016)</span><span class="sxs-lookup"><span data-stu-id="2bbad-103">Create a semi-finished product (February 2016 only)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2bbad-104">See ülesanne keskendub pooleldi lõpetatud toote loomisele.</span><span class="sxs-lookup"><span data-stu-id="2bbad-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="2bbad-105">See on teine ülesanne koosluse arvutamise seeriates.</span><span class="sxs-lookup"><span data-stu-id="2bbad-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="2bbad-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="2bbad-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="2bbad-107">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="2bbad-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="2bbad-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2bbad-108">Click New.</span></span>
3. <span data-ttu-id="2bbad-109">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="2bbad-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="2bbad-110">Selles näites tippige BOM_2.</span><span class="sxs-lookup"><span data-stu-id="2bbad-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="2bbad-111">Sisestage või valige väärtus väljal Kauba mudeligrupp.</span><span class="sxs-lookup"><span data-stu-id="2bbad-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="2bbad-112">Valige suvand STD.</span><span class="sxs-lookup"><span data-stu-id="2bbad-112">Select STD.</span></span> <span data-ttu-id="2bbad-113">STD tähendab standardset kulu ja on kuluarvestustega töötamisel kõige sagedamini kasutatud mudel.</span><span class="sxs-lookup"><span data-stu-id="2bbad-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="2bbad-114">Sisestage või valige väärtus väljal Kaubagrupp.</span><span class="sxs-lookup"><span data-stu-id="2bbad-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="2bbad-115">Näiteks valige Heli.</span><span class="sxs-lookup"><span data-stu-id="2bbad-115">For example, select Audio.</span></span> <span data-ttu-id="2bbad-116">See ei mõjuta kuluarvestusi.</span><span class="sxs-lookup"><span data-stu-id="2bbad-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="2bbad-117">Sisestage või valige väärtus väljal Laoala dimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="2bbad-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="2bbad-118">Valige SiteWH.</span><span class="sxs-lookup"><span data-stu-id="2bbad-118">Select SiteWH.</span></span> <span data-ttu-id="2bbad-119">Selles näites kasutatakse ainult tegevuskohta ja ladu.</span><span class="sxs-lookup"><span data-stu-id="2bbad-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="2bbad-120">Sisestage või valige väärtus väljal Jälgimisdimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="2bbad-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="2bbad-121">Jälgimisdimensioone ei kasutata selles näites, seega valige Pole.</span><span class="sxs-lookup"><span data-stu-id="2bbad-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="2bbad-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2bbad-122">Click OK.</span></span>
9. <span data-ttu-id="2bbad-123">Klõpsake toimingupaanil suvandit Halda varusid.</span><span class="sxs-lookup"><span data-stu-id="2bbad-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="2bbad-124">Klõpsake valikut Tellimuse vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="2bbad-124">Click Default order settings.</span></span>
11. <span data-ttu-id="2bbad-125">Väljal Vaikimisi tellimusetüüp valige Tootmine.</span><span class="sxs-lookup"><span data-stu-id="2bbad-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="2bbad-126">Kuna see on pooleldi lõpetatud toodetav toode, valige Tootmine.</span><span class="sxs-lookup"><span data-stu-id="2bbad-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="2bbad-127">Sisestage või valige väärtus väljal Ostu tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="2bbad-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="2bbad-128">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="2bbad-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="2bbad-129">Sisestage või valige väärtus väljal Laovarude tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="2bbad-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="2bbad-130">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="2bbad-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="2bbad-131">Sisestage või valige väärtus väljal Müügi tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="2bbad-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="2bbad-132">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="2bbad-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="2bbad-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2bbad-133">Close the page.</span></span>
16. <span data-ttu-id="2bbad-134">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="2bbad-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="2bbad-135">Klõpsake nuppu Kauba hind.</span><span class="sxs-lookup"><span data-stu-id="2bbad-135">Click Item price.</span></span>
18. <span data-ttu-id="2bbad-136">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2bbad-136">Click New.</span></span>
19. <span data-ttu-id="2bbad-137">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="2bbad-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="2bbad-138">Sisestage või valige väärtus väljal Versioon.</span><span class="sxs-lookup"><span data-stu-id="2bbad-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="2bbad-139">Selles näites valige Versioon 10.</span><span class="sxs-lookup"><span data-stu-id="2bbad-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="2bbad-140">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="2bbad-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="2bbad-141">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="2bbad-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="2bbad-142">Määrake suvandi Hind väärtuseks „10”.</span><span class="sxs-lookup"><span data-stu-id="2bbad-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="2bbad-143">Selles näites tippige omahind 10.</span><span class="sxs-lookup"><span data-stu-id="2bbad-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="2bbad-144">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2bbad-144">Click Save.</span></span>
24. <span data-ttu-id="2bbad-145">Klõpsake nuppu Ootel hinna/hindade aktiveerimine.</span><span class="sxs-lookup"><span data-stu-id="2bbad-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="2bbad-146">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2bbad-146">Close the page.</span></span>
26. <span data-ttu-id="2bbad-147">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2bbad-147">Close the page.</span></span>
27. <span data-ttu-id="2bbad-148">Selle avamiseks klõpsake nuppu BOM_2.</span><span class="sxs-lookup"><span data-stu-id="2bbad-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="2bbad-149">Laiendage jaotist Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="2bbad-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="2bbad-150">Sisestage või valige väärtus väljal Kulugrupp.</span><span class="sxs-lookup"><span data-stu-id="2bbad-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="2bbad-151">Selles näites valige Kulugrupp M1.</span><span class="sxs-lookup"><span data-stu-id="2bbad-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="2bbad-152">Kasutage otseteed kirje salvestamiseks.</span><span class="sxs-lookup"><span data-stu-id="2bbad-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="2bbad-153">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2bbad-153">Close the page.</span></span>


