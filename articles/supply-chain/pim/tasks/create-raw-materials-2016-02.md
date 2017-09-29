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
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: f6af7b93d8d1d9a6f7474f24177b16e5295e90d6
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2017

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="205d1-103">Toormaterjalide loomine (ainult veebruar 2016)</span><span class="sxs-lookup"><span data-stu-id="205d1-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="205d1-104">See ülesanne keskendub lõpetatud ja pooleldi lõpetatud komponentide loomisele.</span><span class="sxs-lookup"><span data-stu-id="205d1-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="205d1-105">See on kolmas ülesanne koosluse arvutamise seerias.</span><span class="sxs-lookup"><span data-stu-id="205d1-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="205d1-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="205d1-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="205d1-107">Esimese materjali loomine</span><span class="sxs-lookup"><span data-stu-id="205d1-107">Create the first material</span></span>
1. <span data-ttu-id="205d1-108">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="205d1-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="205d1-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="205d1-109">Click New.</span></span>
3. <span data-ttu-id="205d1-110">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="205d1-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="205d1-111">Selles näites sisestage ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="205d1-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="205d1-112">Sisestage või valige väärtus väljal Kauba mudeligrupp.</span><span class="sxs-lookup"><span data-stu-id="205d1-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-113">Valige suvand STD.</span><span class="sxs-lookup"><span data-stu-id="205d1-113">Select STD.</span></span> <span data-ttu-id="205d1-114">STD tähendab standardset kulu ja on kuluarvestustega töötamisel kõige sagedamini kasutatud mudel.</span><span class="sxs-lookup"><span data-stu-id="205d1-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="205d1-115">Sisestage või valige väärtus väljal Kaubagrupp.</span><span class="sxs-lookup"><span data-stu-id="205d1-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-116">Näiteks valige Heli.</span><span class="sxs-lookup"><span data-stu-id="205d1-116">For example, select Audio.</span></span> <span data-ttu-id="205d1-117">See ei mõjuta kuluarvestusi.</span><span class="sxs-lookup"><span data-stu-id="205d1-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="205d1-118">Sisestage või valige väärtus väljal Laoala dimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="205d1-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-119">Valige SiteWH.</span><span class="sxs-lookup"><span data-stu-id="205d1-119">Select SiteWH.</span></span> <span data-ttu-id="205d1-120">Demonstreerimiseks kasutatakse ainult tegevuskohta ja ladu.</span><span class="sxs-lookup"><span data-stu-id="205d1-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="205d1-121">Sisestage või valige väärtus väljal Jälgimisdimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="205d1-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-122">Selles näites ei kasutata jälgimisdimensioone.</span><span class="sxs-lookup"><span data-stu-id="205d1-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="205d1-123">Valige Pole.</span><span class="sxs-lookup"><span data-stu-id="205d1-123">Select None.</span></span>  
8. <span data-ttu-id="205d1-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="205d1-124">Click OK.</span></span>
9. <span data-ttu-id="205d1-125">Klõpsake toimingupaanil suvandit Halda varusid.</span><span class="sxs-lookup"><span data-stu-id="205d1-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="205d1-126">Klõpsake valikut Tellimuse vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="205d1-126">Click Default order settings.</span></span>
11. <span data-ttu-id="205d1-127">Sisestage või valige väärtus väljal Ostu tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="205d1-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-128">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="205d1-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="205d1-129">Sisestage või valige väärtus väljal Laovarude tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="205d1-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-130">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="205d1-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="205d1-131">Sisestage või valige väärtus väljal Müügi tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="205d1-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-132">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="205d1-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="205d1-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="205d1-133">Close the page.</span></span>
15. <span data-ttu-id="205d1-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="205d1-134">Close the page.</span></span>
16. <span data-ttu-id="205d1-135">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="205d1-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="205d1-136">Klõpsake nuppu ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="205d1-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="205d1-137">Laiendage jaotist Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="205d1-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="205d1-138">Väljale Kulugrupp tippige väärtus.</span><span class="sxs-lookup"><span data-stu-id="205d1-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="205d1-139">Selles näites tippige M2.</span><span class="sxs-lookup"><span data-stu-id="205d1-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="205d1-140">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="205d1-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="205d1-141">Klõpsake nuppu Kauba hind.</span><span class="sxs-lookup"><span data-stu-id="205d1-141">Click Item price.</span></span>
21. <span data-ttu-id="205d1-142">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="205d1-142">Click New.</span></span>
22. <span data-ttu-id="205d1-143">Sisestage või valige väärtus väljal Versioon.</span><span class="sxs-lookup"><span data-stu-id="205d1-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-144">Selles näites valige 10, mis on standardse kulu tüüp.</span><span class="sxs-lookup"><span data-stu-id="205d1-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="205d1-145">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="205d1-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-146">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="205d1-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="205d1-147">Sisestage väljale Price (Hind) number.</span><span class="sxs-lookup"><span data-stu-id="205d1-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="205d1-148">Selles näites tippige 10.</span><span class="sxs-lookup"><span data-stu-id="205d1-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="205d1-149">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="205d1-149">Click Save.</span></span>
26. <span data-ttu-id="205d1-150">Klõpsake nuppu Ootel hinna/hindade aktiveerimine.</span><span class="sxs-lookup"><span data-stu-id="205d1-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="205d1-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="205d1-151">Close the page.</span></span>
28. <span data-ttu-id="205d1-152">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="205d1-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="205d1-153">Teise materjali loomine</span><span class="sxs-lookup"><span data-stu-id="205d1-153">Create the second material</span></span>
1. <span data-ttu-id="205d1-154">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="205d1-154">Click New.</span></span>
2. <span data-ttu-id="205d1-155">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="205d1-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="205d1-156">Selles näites tippige ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="205d1-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="205d1-157">Sisestage või valige väärtus väljal Kauba mudeligrupp.</span><span class="sxs-lookup"><span data-stu-id="205d1-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-158">Valige suvand STD.</span><span class="sxs-lookup"><span data-stu-id="205d1-158">Select STD.</span></span> <span data-ttu-id="205d1-159">STD tähendab standardset kulu ja on kuluarvestustega töötamisel kõige sagedamini kasutatud mudel.</span><span class="sxs-lookup"><span data-stu-id="205d1-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="205d1-160">Sisestage või valige väärtus väljal Kaubagrupp.</span><span class="sxs-lookup"><span data-stu-id="205d1-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-161">Näiteks valige Heli.</span><span class="sxs-lookup"><span data-stu-id="205d1-161">For example, select Audio.</span></span> <span data-ttu-id="205d1-162">See ei mõjuta kuluarvestusi.</span><span class="sxs-lookup"><span data-stu-id="205d1-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="205d1-163">Sisestage või valige väärtus väljal Laoala dimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="205d1-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-164">Valige SiteWH.</span><span class="sxs-lookup"><span data-stu-id="205d1-164">Select SiteWH.</span></span> <span data-ttu-id="205d1-165">Selles näites kasutatakse ainult tegevuskohta ja ladu.</span><span class="sxs-lookup"><span data-stu-id="205d1-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="205d1-166">Sisestage või valige väärtus väljal Jälgimisdimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="205d1-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-167">Selles näites ei kasutata jälgimisdimensioone.</span><span class="sxs-lookup"><span data-stu-id="205d1-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="205d1-168">Valige Pole.</span><span class="sxs-lookup"><span data-stu-id="205d1-168">Select None.</span></span>  
7. <span data-ttu-id="205d1-169">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="205d1-169">Click OK.</span></span>
8. <span data-ttu-id="205d1-170">Klõpsake toimingupaanil suvandit Halda varusid.</span><span class="sxs-lookup"><span data-stu-id="205d1-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="205d1-171">Klõpsake valikut Tellimuse vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="205d1-171">Click Default order settings.</span></span>
10. <span data-ttu-id="205d1-172">Sisestage või valige väärtus väljal Ostu tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="205d1-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-173">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="205d1-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="205d1-174">Sisestage või valige väärtus väljal Laovarude tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="205d1-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-175">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="205d1-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="205d1-176">Sisestage või valige väärtus väljal Müügi tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="205d1-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-177">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="205d1-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="205d1-178">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="205d1-178">Close the page.</span></span>
14. <span data-ttu-id="205d1-179">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="205d1-179">Close the page.</span></span>
15. <span data-ttu-id="205d1-180">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="205d1-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="205d1-181">Klõpsake nuppu ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="205d1-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="205d1-182">Laiendage jaotist Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="205d1-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="205d1-183">Väljale Kulugrupp tippige väärtus.</span><span class="sxs-lookup"><span data-stu-id="205d1-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="205d1-184">Selles näites tippige M2.</span><span class="sxs-lookup"><span data-stu-id="205d1-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="205d1-185">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="205d1-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="205d1-186">Klõpsake nuppu Kauba hind.</span><span class="sxs-lookup"><span data-stu-id="205d1-186">Click Item price.</span></span>
20. <span data-ttu-id="205d1-187">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="205d1-187">Click New.</span></span>
21. <span data-ttu-id="205d1-188">Sisestage või valige väärtus väljal Versioon.</span><span class="sxs-lookup"><span data-stu-id="205d1-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-189">Selles näites valige 10.</span><span class="sxs-lookup"><span data-stu-id="205d1-189">For this example, select 10.</span></span> <span data-ttu-id="205d1-190">See on standardse kulu tüüp.</span><span class="sxs-lookup"><span data-stu-id="205d1-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="205d1-191">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="205d1-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-192">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="205d1-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="205d1-193">Sisestage väljale Price (Hind) number.</span><span class="sxs-lookup"><span data-stu-id="205d1-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="205d1-194">Demonstreerimiseks tippige 10.</span><span class="sxs-lookup"><span data-stu-id="205d1-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="205d1-195">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="205d1-195">Click Save.</span></span>
25. <span data-ttu-id="205d1-196">Klõpsake nuppu Ootel hinna/hindade aktiveerimine.</span><span class="sxs-lookup"><span data-stu-id="205d1-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="205d1-197">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="205d1-197">Close the page.</span></span>
27. <span data-ttu-id="205d1-198">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="205d1-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="205d1-199">Kolmanda materjali loomine</span><span class="sxs-lookup"><span data-stu-id="205d1-199">Create the third material</span></span>
1. <span data-ttu-id="205d1-200">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="205d1-200">Click New.</span></span>
2. <span data-ttu-id="205d1-201">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="205d1-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="205d1-202">Demonstreerimiseks tippige ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="205d1-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="205d1-203">Sisestage või valige väärtus väljal Kauba mudeligrupp.</span><span class="sxs-lookup"><span data-stu-id="205d1-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-204">Valige suvand STD.</span><span class="sxs-lookup"><span data-stu-id="205d1-204">Select STD.</span></span> <span data-ttu-id="205d1-205">STD tähendab standardset kulu ja on kuluarvestustega töötamisel kõige sagedamini kasutatud mudel.</span><span class="sxs-lookup"><span data-stu-id="205d1-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="205d1-206">Sisestage või valige väärtus väljal Kaubagrupp.</span><span class="sxs-lookup"><span data-stu-id="205d1-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-207">Näiteks valige Heli.</span><span class="sxs-lookup"><span data-stu-id="205d1-207">For example, select Audio.</span></span> <span data-ttu-id="205d1-208">See ei mõjuta kuluarvestusi.</span><span class="sxs-lookup"><span data-stu-id="205d1-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="205d1-209">Sisestage või valige väärtus väljal Laoala dimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="205d1-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-210">Valige SiteWH.</span><span class="sxs-lookup"><span data-stu-id="205d1-210">Select SiteWH.</span></span> <span data-ttu-id="205d1-211">Demonstreerimiseks kasutatakse ainult tegevuskohta ja ladu.</span><span class="sxs-lookup"><span data-stu-id="205d1-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="205d1-212">Sisestage või valige väärtus väljal Jälgimisdimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="205d1-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-213">Selles näites ei kasutata jälgimisdimensioone.</span><span class="sxs-lookup"><span data-stu-id="205d1-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="205d1-214">Valige Pole.</span><span class="sxs-lookup"><span data-stu-id="205d1-214">Select None.</span></span>  
7. <span data-ttu-id="205d1-215">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="205d1-215">Click OK.</span></span>
8. <span data-ttu-id="205d1-216">Klõpsake toimingupaanil suvandit Halda varusid.</span><span class="sxs-lookup"><span data-stu-id="205d1-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="205d1-217">Klõpsake valikut Tellimuse vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="205d1-217">Click Default order settings.</span></span>
10. <span data-ttu-id="205d1-218">Sisestage või valige väärtus väljal Ostu tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="205d1-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-219">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="205d1-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="205d1-220">Sisestage või valige väärtus väljal Laovarude tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="205d1-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-221">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="205d1-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="205d1-222">Sisestage või valige väärtus väljal Müügi tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="205d1-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-223">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="205d1-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="205d1-224">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="205d1-224">Close the page.</span></span>
14. <span data-ttu-id="205d1-225">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="205d1-225">Close the page.</span></span>
15. <span data-ttu-id="205d1-226">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="205d1-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="205d1-227">Klõpsake nuppu ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="205d1-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="205d1-228">Laiendage jaotist Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="205d1-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="205d1-229">Väljale Kulugrupp tippige väärtus.</span><span class="sxs-lookup"><span data-stu-id="205d1-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="205d1-230">Selles näites tippige M1.</span><span class="sxs-lookup"><span data-stu-id="205d1-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="205d1-231">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="205d1-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="205d1-232">Klõpsake nuppu Kauba hind.</span><span class="sxs-lookup"><span data-stu-id="205d1-232">Click Item price.</span></span>
20. <span data-ttu-id="205d1-233">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="205d1-233">Click New.</span></span>
21. <span data-ttu-id="205d1-234">Sisestage või valige väärtus väljal Versioon.</span><span class="sxs-lookup"><span data-stu-id="205d1-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-235">Selles näites valige 10.</span><span class="sxs-lookup"><span data-stu-id="205d1-235">For this example, select 10.</span></span> <span data-ttu-id="205d1-236">See on standardse kulu tüüp.</span><span class="sxs-lookup"><span data-stu-id="205d1-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="205d1-237">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="205d1-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="205d1-238">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="205d1-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="205d1-239">Sisestage väljale Price (Hind) number.</span><span class="sxs-lookup"><span data-stu-id="205d1-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="205d1-240">Selles näites tippige 10.</span><span class="sxs-lookup"><span data-stu-id="205d1-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="205d1-241">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="205d1-241">Click Save.</span></span>
25. <span data-ttu-id="205d1-242">Klõpsake nuppu Ootel hinna/hindade aktiveerimine.</span><span class="sxs-lookup"><span data-stu-id="205d1-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="205d1-243">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="205d1-243">Close the page.</span></span>
27. <span data-ttu-id="205d1-244">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="205d1-244">Close the page.</span></span>


