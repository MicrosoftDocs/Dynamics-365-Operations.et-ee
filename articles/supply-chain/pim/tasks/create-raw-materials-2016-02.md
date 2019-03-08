---
title: Toormaterjalide loomine (veebruar 2016)
description: See ülesanne keskendub lõpetatud ja pooleldi lõpetatud komponentide loomisele.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091b6edaf43e86e6e3665bf79871648473e284c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "351052"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="5f2a8-103">Toormaterjalide loomine (veebruar 2016)</span><span class="sxs-lookup"><span data-stu-id="5f2a8-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5f2a8-104">See ülesanne keskendub lõpetatud ja pooleldi lõpetatud komponentide loomisele.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="5f2a8-105">See on kolmas ülesanne koosluse arvutamise seerias.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="5f2a8-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="5f2a8-107">Esimese materjali loomine</span><span class="sxs-lookup"><span data-stu-id="5f2a8-107">Create the first material</span></span>
1. <span data-ttu-id="5f2a8-108">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="5f2a8-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-109">Click New.</span></span>
3. <span data-ttu-id="5f2a8-110">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="5f2a8-111">Selles näites sisestage ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="5f2a8-112">Sisestage või valige väärtus väljal Kauba mudeligrupp.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-113">Valige suvand STD.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-113">Select STD.</span></span> <span data-ttu-id="5f2a8-114">STD tähendab standardset kulu ja on kuluarvestustega töötamisel kõige sagedamini kasutatud mudel.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="5f2a8-115">Sisestage või valige väärtus väljal Kaubagrupp.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-116">Näiteks valige Heli.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-116">For example, select Audio.</span></span> <span data-ttu-id="5f2a8-117">See ei mõjuta kuluarvestusi.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="5f2a8-118">Sisestage või valige väärtus väljal Laoala dimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-119">Valige SiteWH.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-119">Select SiteWH.</span></span> <span data-ttu-id="5f2a8-120">Demonstreerimiseks kasutatakse ainult tegevuskohta ja ladu.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="5f2a8-121">Sisestage või valige väärtus väljal Jälgimisdimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-122">Selles näites ei kasutata jälgimisdimensioone.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="5f2a8-123">Valige Pole.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-123">Select None.</span></span>  
8. <span data-ttu-id="5f2a8-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-124">Click OK.</span></span>
9. <span data-ttu-id="5f2a8-125">Klõpsake toimingupaanil suvandit Halda varusid.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="5f2a8-126">Klõpsake valikut Tellimuse vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-126">Click Default order settings.</span></span>
11. <span data-ttu-id="5f2a8-127">Sisestage või valige väärtus väljal Ostu tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-128">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="5f2a8-129">Sisestage või valige väärtus väljal Laovarude tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-130">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="5f2a8-131">Sisestage või valige väärtus väljal Müügi tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-132">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="5f2a8-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-133">Close the page.</span></span>
15. <span data-ttu-id="5f2a8-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-134">Close the page.</span></span>
16. <span data-ttu-id="5f2a8-135">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5f2a8-136">Klõpsake nuppu ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="5f2a8-137">Laiendage jaotist Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="5f2a8-138">Väljale Kulugrupp tippige väärtus.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="5f2a8-139">Selles näites tippige M2.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="5f2a8-140">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="5f2a8-141">Klõpsake nuppu Kauba hind.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-141">Click Item price.</span></span>
21. <span data-ttu-id="5f2a8-142">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-142">Click New.</span></span>
22. <span data-ttu-id="5f2a8-143">Sisestage või valige väärtus väljal Versioon.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-144">Selles näites valige 10, mis on standardse kulu tüüp.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="5f2a8-145">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-146">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="5f2a8-147">Sisestage väljale Price (Hind) number.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="5f2a8-148">Selles näites tippige 10.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="5f2a8-149">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-149">Click Save.</span></span>
26. <span data-ttu-id="5f2a8-150">Klõpsake nuppu Ootel hinna/hindade aktiveerimine.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="5f2a8-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-151">Close the page.</span></span>
28. <span data-ttu-id="5f2a8-152">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="5f2a8-153">Teise materjali loomine</span><span class="sxs-lookup"><span data-stu-id="5f2a8-153">Create the second material</span></span>
1. <span data-ttu-id="5f2a8-154">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-154">Click New.</span></span>
2. <span data-ttu-id="5f2a8-155">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="5f2a8-156">Selles näites tippige ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="5f2a8-157">Sisestage või valige väärtus väljal Kauba mudeligrupp.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-158">Valige suvand STD.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-158">Select STD.</span></span> <span data-ttu-id="5f2a8-159">STD tähendab standardset kulu ja on kuluarvestustega töötamisel kõige sagedamini kasutatud mudel.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="5f2a8-160">Sisestage või valige väärtus väljal Kaubagrupp.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-161">Näiteks valige Heli.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-161">For example, select Audio.</span></span> <span data-ttu-id="5f2a8-162">See ei mõjuta kuluarvestusi.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="5f2a8-163">Sisestage või valige väärtus väljal Laoala dimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-164">Valige SiteWH.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-164">Select SiteWH.</span></span> <span data-ttu-id="5f2a8-165">Selles näites kasutatakse ainult tegevuskohta ja ladu.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="5f2a8-166">Sisestage või valige väärtus väljal Jälgimisdimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-167">Selles näites ei kasutata jälgimisdimensioone.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="5f2a8-168">Valige Pole.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-168">Select None.</span></span>  
7. <span data-ttu-id="5f2a8-169">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-169">Click OK.</span></span>
8. <span data-ttu-id="5f2a8-170">Klõpsake toimingupaanil suvandit Halda varusid.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="5f2a8-171">Klõpsake valikut Tellimuse vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-171">Click Default order settings.</span></span>
10. <span data-ttu-id="5f2a8-172">Sisestage või valige väärtus väljal Ostu tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-173">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="5f2a8-174">Sisestage või valige väärtus väljal Laovarude tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-175">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="5f2a8-176">Sisestage või valige väärtus väljal Müügi tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-177">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="5f2a8-178">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-178">Close the page.</span></span>
14. <span data-ttu-id="5f2a8-179">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-179">Close the page.</span></span>
15. <span data-ttu-id="5f2a8-180">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5f2a8-181">Klõpsake nuppu ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="5f2a8-182">Laiendage jaotist Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="5f2a8-183">Väljale Kulugrupp tippige väärtus.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="5f2a8-184">Selles näites tippige M2.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="5f2a8-185">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="5f2a8-186">Klõpsake nuppu Kauba hind.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-186">Click Item price.</span></span>
20. <span data-ttu-id="5f2a8-187">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-187">Click New.</span></span>
21. <span data-ttu-id="5f2a8-188">Sisestage või valige väärtus väljal Versioon.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-189">Selles näites valige 10.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-189">For this example, select 10.</span></span> <span data-ttu-id="5f2a8-190">See on standardse kulu tüüp.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="5f2a8-191">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-192">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="5f2a8-193">Sisestage väljale Price (Hind) number.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="5f2a8-194">Demonstreerimiseks tippige 10.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="5f2a8-195">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-195">Click Save.</span></span>
25. <span data-ttu-id="5f2a8-196">Klõpsake nuppu Ootel hinna/hindade aktiveerimine.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="5f2a8-197">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-197">Close the page.</span></span>
27. <span data-ttu-id="5f2a8-198">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="5f2a8-199">Kolmanda materjali loomine</span><span class="sxs-lookup"><span data-stu-id="5f2a8-199">Create the third material</span></span>
1. <span data-ttu-id="5f2a8-200">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-200">Click New.</span></span>
2. <span data-ttu-id="5f2a8-201">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="5f2a8-202">Demonstreerimiseks tippige ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="5f2a8-203">Sisestage või valige väärtus väljal Kauba mudeligrupp.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-204">Valige suvand STD.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-204">Select STD.</span></span> <span data-ttu-id="5f2a8-205">STD tähendab standardset kulu ja on kuluarvestustega töötamisel kõige sagedamini kasutatud mudel.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="5f2a8-206">Sisestage või valige väärtus väljal Kaubagrupp.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-207">Näiteks valige Heli.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-207">For example, select Audio.</span></span> <span data-ttu-id="5f2a8-208">See ei mõjuta kuluarvestusi.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="5f2a8-209">Sisestage või valige väärtus väljal Laoala dimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-210">Valige SiteWH.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-210">Select SiteWH.</span></span> <span data-ttu-id="5f2a8-211">Demonstreerimiseks kasutatakse ainult tegevuskohta ja ladu.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="5f2a8-212">Sisestage või valige väärtus väljal Jälgimisdimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-213">Selles näites ei kasutata jälgimisdimensioone.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="5f2a8-214">Valige Pole.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-214">Select None.</span></span>  
7. <span data-ttu-id="5f2a8-215">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-215">Click OK.</span></span>
8. <span data-ttu-id="5f2a8-216">Klõpsake toimingupaanil suvandit Halda varusid.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="5f2a8-217">Klõpsake valikut Tellimuse vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-217">Click Default order settings.</span></span>
10. <span data-ttu-id="5f2a8-218">Sisestage või valige väärtus väljal Ostu tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-219">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="5f2a8-220">Sisestage või valige väärtus väljal Laovarude tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-221">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="5f2a8-222">Sisestage või valige väärtus väljal Müügi tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-223">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="5f2a8-224">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-224">Close the page.</span></span>
14. <span data-ttu-id="5f2a8-225">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-225">Close the page.</span></span>
15. <span data-ttu-id="5f2a8-226">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5f2a8-227">Klõpsake nuppu ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="5f2a8-228">Laiendage jaotist Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="5f2a8-229">Väljale Kulugrupp tippige väärtus.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="5f2a8-230">Selles näites tippige M1.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="5f2a8-231">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="5f2a8-232">Klõpsake nuppu Kauba hind.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-232">Click Item price.</span></span>
20. <span data-ttu-id="5f2a8-233">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-233">Click New.</span></span>
21. <span data-ttu-id="5f2a8-234">Sisestage või valige väärtus väljal Versioon.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-235">Selles näites valige 10.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-235">For this example, select 10.</span></span> <span data-ttu-id="5f2a8-236">See on standardse kulu tüüp.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="5f2a8-237">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="5f2a8-238">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="5f2a8-239">Sisestage väljale Price (Hind) number.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="5f2a8-240">Selles näites tippige 10.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="5f2a8-241">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-241">Click Save.</span></span>
25. <span data-ttu-id="5f2a8-242">Klõpsake nuppu Ootel hinna/hindade aktiveerimine.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="5f2a8-243">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-243">Close the page.</span></span>
27. <span data-ttu-id="5f2a8-244">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-244">Close the page.</span></span>

