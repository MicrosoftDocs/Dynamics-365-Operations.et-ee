--- 
title: Toormaterjalide loomine (ainult veebruar 2016)
description: "See ülesanne keskendub lõpetatud ja pooleldi lõpetatud komponentide loomisele."
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
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5a31ceacb7037164d35e38fb70a013b33d670d94
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="780c9-103">Toormaterjalide loomine (ainult veebruar 2016)</span><span class="sxs-lookup"><span data-stu-id="780c9-103">Create raw materials (February 2016 only)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="780c9-104">See ülesanne keskendub lõpetatud ja pooleldi lõpetatud komponentide loomisele.</span><span class="sxs-lookup"><span data-stu-id="780c9-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="780c9-105">See on kolmas ülesanne koosluse arvutamise seerias.</span><span class="sxs-lookup"><span data-stu-id="780c9-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="780c9-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="780c9-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="780c9-107">Esimese materjali loomine</span><span class="sxs-lookup"><span data-stu-id="780c9-107">Create the first material</span></span>
1. <span data-ttu-id="780c9-108">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="780c9-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="780c9-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="780c9-109">Click New.</span></span>
3. <span data-ttu-id="780c9-110">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="780c9-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="780c9-111">Selles näites sisestage ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="780c9-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="780c9-112">Sisestage või valige väärtus väljal Kauba mudeligrupp.</span><span class="sxs-lookup"><span data-stu-id="780c9-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-113">Valige suvand STD.</span><span class="sxs-lookup"><span data-stu-id="780c9-113">Select STD.</span></span> <span data-ttu-id="780c9-114">STD tähendab standardset kulu ja on kuluarvestustega töötamisel kõige sagedamini kasutatud mudel.</span><span class="sxs-lookup"><span data-stu-id="780c9-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="780c9-115">Sisestage või valige väärtus väljal Kaubagrupp.</span><span class="sxs-lookup"><span data-stu-id="780c9-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-116">Näiteks valige Heli.</span><span class="sxs-lookup"><span data-stu-id="780c9-116">For example, select Audio.</span></span> <span data-ttu-id="780c9-117">See ei mõjuta kuluarvestusi.</span><span class="sxs-lookup"><span data-stu-id="780c9-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="780c9-118">Sisestage või valige väärtus väljal Laoala dimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="780c9-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-119">Valige SiteWH.</span><span class="sxs-lookup"><span data-stu-id="780c9-119">Select SiteWH.</span></span> <span data-ttu-id="780c9-120">Demonstreerimiseks kasutatakse ainult tegevuskohta ja ladu.</span><span class="sxs-lookup"><span data-stu-id="780c9-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="780c9-121">Sisestage või valige väärtus väljal Jälgimisdimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="780c9-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-122">Selles näites ei kasutata jälgimisdimensioone.</span><span class="sxs-lookup"><span data-stu-id="780c9-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="780c9-123">Valige Pole.</span><span class="sxs-lookup"><span data-stu-id="780c9-123">Select None.</span></span>  
8. <span data-ttu-id="780c9-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="780c9-124">Click OK.</span></span>
9. <span data-ttu-id="780c9-125">Klõpsake toimingupaanil suvandit Halda varusid.</span><span class="sxs-lookup"><span data-stu-id="780c9-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="780c9-126">Klõpsake valikut Tellimuse vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="780c9-126">Click Default order settings.</span></span>
11. <span data-ttu-id="780c9-127">Sisestage või valige väärtus väljal Ostu tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="780c9-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-128">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="780c9-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="780c9-129">Sisestage või valige väärtus väljal Laovarude tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="780c9-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-130">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="780c9-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="780c9-131">Sisestage või valige väärtus väljal Müügi tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="780c9-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-132">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="780c9-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="780c9-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="780c9-133">Close the page.</span></span>
15. <span data-ttu-id="780c9-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="780c9-134">Close the page.</span></span>
16. <span data-ttu-id="780c9-135">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="780c9-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="780c9-136">Klõpsake nuppu ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="780c9-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="780c9-137">Laiendage jaotist Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="780c9-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="780c9-138">Väljale Kulugrupp tippige väärtus.</span><span class="sxs-lookup"><span data-stu-id="780c9-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="780c9-139">Selles näites tippige M2.</span><span class="sxs-lookup"><span data-stu-id="780c9-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="780c9-140">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="780c9-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="780c9-141">Klõpsake nuppu Kauba hind.</span><span class="sxs-lookup"><span data-stu-id="780c9-141">Click Item price.</span></span>
21. <span data-ttu-id="780c9-142">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="780c9-142">Click New.</span></span>
22. <span data-ttu-id="780c9-143">Sisestage või valige väärtus väljal Versioon.</span><span class="sxs-lookup"><span data-stu-id="780c9-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-144">Selles näites valige 10, mis on standardse kulu tüüp.</span><span class="sxs-lookup"><span data-stu-id="780c9-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="780c9-145">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="780c9-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-146">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="780c9-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="780c9-147">Sisestage väljale Price (Hind) number.</span><span class="sxs-lookup"><span data-stu-id="780c9-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="780c9-148">Selles näites tippige 10.</span><span class="sxs-lookup"><span data-stu-id="780c9-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="780c9-149">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="780c9-149">Click Save.</span></span>
26. <span data-ttu-id="780c9-150">Klõpsake nuppu Ootel hinna/hindade aktiveerimine.</span><span class="sxs-lookup"><span data-stu-id="780c9-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="780c9-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="780c9-151">Close the page.</span></span>
28. <span data-ttu-id="780c9-152">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="780c9-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="780c9-153">Teise materjali loomine</span><span class="sxs-lookup"><span data-stu-id="780c9-153">Create the second material</span></span>
1. <span data-ttu-id="780c9-154">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="780c9-154">Click New.</span></span>
2. <span data-ttu-id="780c9-155">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="780c9-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="780c9-156">Selles näites tippige ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="780c9-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="780c9-157">Sisestage või valige väärtus väljal Kauba mudeligrupp.</span><span class="sxs-lookup"><span data-stu-id="780c9-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-158">Valige suvand STD.</span><span class="sxs-lookup"><span data-stu-id="780c9-158">Select STD.</span></span> <span data-ttu-id="780c9-159">STD tähendab standardset kulu ja on kuluarvestustega töötamisel kõige sagedamini kasutatud mudel.</span><span class="sxs-lookup"><span data-stu-id="780c9-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="780c9-160">Sisestage või valige väärtus väljal Kaubagrupp.</span><span class="sxs-lookup"><span data-stu-id="780c9-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-161">Näiteks valige Heli.</span><span class="sxs-lookup"><span data-stu-id="780c9-161">For example, select Audio.</span></span> <span data-ttu-id="780c9-162">See ei mõjuta kuluarvestusi.</span><span class="sxs-lookup"><span data-stu-id="780c9-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="780c9-163">Sisestage või valige väärtus väljal Laoala dimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="780c9-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-164">Valige SiteWH.</span><span class="sxs-lookup"><span data-stu-id="780c9-164">Select SiteWH.</span></span> <span data-ttu-id="780c9-165">Selles näites kasutatakse ainult tegevuskohta ja ladu.</span><span class="sxs-lookup"><span data-stu-id="780c9-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="780c9-166">Sisestage või valige väärtus väljal Jälgimisdimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="780c9-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-167">Selles näites ei kasutata jälgimisdimensioone.</span><span class="sxs-lookup"><span data-stu-id="780c9-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="780c9-168">Valige Pole.</span><span class="sxs-lookup"><span data-stu-id="780c9-168">Select None.</span></span>  
7. <span data-ttu-id="780c9-169">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="780c9-169">Click OK.</span></span>
8. <span data-ttu-id="780c9-170">Klõpsake toimingupaanil suvandit Halda varusid.</span><span class="sxs-lookup"><span data-stu-id="780c9-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="780c9-171">Klõpsake valikut Tellimuse vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="780c9-171">Click Default order settings.</span></span>
10. <span data-ttu-id="780c9-172">Sisestage või valige väärtus väljal Ostu tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="780c9-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-173">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="780c9-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="780c9-174">Sisestage või valige väärtus väljal Laovarude tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="780c9-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-175">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="780c9-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="780c9-176">Sisestage või valige väärtus väljal Müügi tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="780c9-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-177">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="780c9-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="780c9-178">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="780c9-178">Close the page.</span></span>
14. <span data-ttu-id="780c9-179">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="780c9-179">Close the page.</span></span>
15. <span data-ttu-id="780c9-180">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="780c9-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="780c9-181">Klõpsake nuppu ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="780c9-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="780c9-182">Laiendage jaotist Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="780c9-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="780c9-183">Väljale Kulugrupp tippige väärtus.</span><span class="sxs-lookup"><span data-stu-id="780c9-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="780c9-184">Selles näites tippige M2.</span><span class="sxs-lookup"><span data-stu-id="780c9-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="780c9-185">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="780c9-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="780c9-186">Klõpsake nuppu Kauba hind.</span><span class="sxs-lookup"><span data-stu-id="780c9-186">Click Item price.</span></span>
20. <span data-ttu-id="780c9-187">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="780c9-187">Click New.</span></span>
21. <span data-ttu-id="780c9-188">Sisestage või valige väärtus väljal Versioon.</span><span class="sxs-lookup"><span data-stu-id="780c9-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-189">Selles näites valige 10.</span><span class="sxs-lookup"><span data-stu-id="780c9-189">For this example, select 10.</span></span> <span data-ttu-id="780c9-190">See on standardse kulu tüüp.</span><span class="sxs-lookup"><span data-stu-id="780c9-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="780c9-191">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="780c9-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-192">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="780c9-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="780c9-193">Sisestage väljale Price (Hind) number.</span><span class="sxs-lookup"><span data-stu-id="780c9-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="780c9-194">Demonstreerimiseks tippige 10.</span><span class="sxs-lookup"><span data-stu-id="780c9-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="780c9-195">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="780c9-195">Click Save.</span></span>
25. <span data-ttu-id="780c9-196">Klõpsake nuppu Ootel hinna/hindade aktiveerimine.</span><span class="sxs-lookup"><span data-stu-id="780c9-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="780c9-197">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="780c9-197">Close the page.</span></span>
27. <span data-ttu-id="780c9-198">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="780c9-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="780c9-199">Kolmanda materjali loomine</span><span class="sxs-lookup"><span data-stu-id="780c9-199">Create the third material</span></span>
1. <span data-ttu-id="780c9-200">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="780c9-200">Click New.</span></span>
2. <span data-ttu-id="780c9-201">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="780c9-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="780c9-202">Demonstreerimiseks tippige ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="780c9-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="780c9-203">Sisestage või valige väärtus väljal Kauba mudeligrupp.</span><span class="sxs-lookup"><span data-stu-id="780c9-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-204">Valige suvand STD.</span><span class="sxs-lookup"><span data-stu-id="780c9-204">Select STD.</span></span> <span data-ttu-id="780c9-205">STD tähendab standardset kulu ja on kuluarvestustega töötamisel kõige sagedamini kasutatud mudel.</span><span class="sxs-lookup"><span data-stu-id="780c9-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="780c9-206">Sisestage või valige väärtus väljal Kaubagrupp.</span><span class="sxs-lookup"><span data-stu-id="780c9-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-207">Näiteks valige Heli.</span><span class="sxs-lookup"><span data-stu-id="780c9-207">For example, select Audio.</span></span> <span data-ttu-id="780c9-208">See ei mõjuta kuluarvestusi.</span><span class="sxs-lookup"><span data-stu-id="780c9-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="780c9-209">Sisestage või valige väärtus väljal Laoala dimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="780c9-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-210">Valige SiteWH.</span><span class="sxs-lookup"><span data-stu-id="780c9-210">Select SiteWH.</span></span> <span data-ttu-id="780c9-211">Demonstreerimiseks kasutatakse ainult tegevuskohta ja ladu.</span><span class="sxs-lookup"><span data-stu-id="780c9-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="780c9-212">Sisestage või valige väärtus väljal Jälgimisdimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="780c9-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-213">Selles näites ei kasutata jälgimisdimensioone.</span><span class="sxs-lookup"><span data-stu-id="780c9-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="780c9-214">Valige Pole.</span><span class="sxs-lookup"><span data-stu-id="780c9-214">Select None.</span></span>  
7. <span data-ttu-id="780c9-215">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="780c9-215">Click OK.</span></span>
8. <span data-ttu-id="780c9-216">Klõpsake toimingupaanil suvandit Halda varusid.</span><span class="sxs-lookup"><span data-stu-id="780c9-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="780c9-217">Klõpsake valikut Tellimuse vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="780c9-217">Click Default order settings.</span></span>
10. <span data-ttu-id="780c9-218">Sisestage või valige väärtus väljal Ostu tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="780c9-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-219">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="780c9-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="780c9-220">Sisestage või valige väärtus väljal Laovarude tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="780c9-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-221">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="780c9-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="780c9-222">Sisestage või valige väärtus väljal Müügi tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="780c9-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-223">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="780c9-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="780c9-224">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="780c9-224">Close the page.</span></span>
14. <span data-ttu-id="780c9-225">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="780c9-225">Close the page.</span></span>
15. <span data-ttu-id="780c9-226">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="780c9-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="780c9-227">Klõpsake nuppu ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="780c9-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="780c9-228">Laiendage jaotist Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="780c9-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="780c9-229">Väljale Kulugrupp tippige väärtus.</span><span class="sxs-lookup"><span data-stu-id="780c9-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="780c9-230">Selles näites tippige M1.</span><span class="sxs-lookup"><span data-stu-id="780c9-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="780c9-231">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="780c9-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="780c9-232">Klõpsake nuppu Kauba hind.</span><span class="sxs-lookup"><span data-stu-id="780c9-232">Click Item price.</span></span>
20. <span data-ttu-id="780c9-233">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="780c9-233">Click New.</span></span>
21. <span data-ttu-id="780c9-234">Sisestage või valige väärtus väljal Versioon.</span><span class="sxs-lookup"><span data-stu-id="780c9-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-235">Selles näites valige 10.</span><span class="sxs-lookup"><span data-stu-id="780c9-235">For this example, select 10.</span></span> <span data-ttu-id="780c9-236">See on standardse kulu tüüp.</span><span class="sxs-lookup"><span data-stu-id="780c9-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="780c9-237">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="780c9-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="780c9-238">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="780c9-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="780c9-239">Sisestage väljale Price (Hind) number.</span><span class="sxs-lookup"><span data-stu-id="780c9-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="780c9-240">Selles näites tippige 10.</span><span class="sxs-lookup"><span data-stu-id="780c9-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="780c9-241">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="780c9-241">Click Save.</span></span>
25. <span data-ttu-id="780c9-242">Klõpsake nuppu Ootel hinna/hindade aktiveerimine.</span><span class="sxs-lookup"><span data-stu-id="780c9-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="780c9-243">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="780c9-243">Close the page.</span></span>
27. <span data-ttu-id="780c9-244">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="780c9-244">Close the page.</span></span>


