--- 
title: Koosluste loomine (ainult veebruar 2016)
description: "See ülesanne keskendub lõpetatud ja pooleldi lõpetatud toote jaoks koosluse struktuuri loomisele."
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6c5473a0786ba0348701e8e106de46f811571f07
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="create-boms-february-2016-only"></a><span data-ttu-id="f7afe-103">Koosluste loomine (ainult veebruar 2016)</span><span class="sxs-lookup"><span data-stu-id="f7afe-103">Create BOMs (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f7afe-104">See ülesanne keskendub lõpetatud ja pooleldi lõpetatud toote jaoks koosluse struktuuri loomisele.</span><span class="sxs-lookup"><span data-stu-id="f7afe-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="f7afe-105">See on neljas ülesanne koosluse arvutamise seerias.</span><span class="sxs-lookup"><span data-stu-id="f7afe-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="f7afe-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="f7afe-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="f7afe-107">Koosluse loomine pooleldi lõpetatud tootele</span><span class="sxs-lookup"><span data-stu-id="f7afe-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="f7afe-108">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="f7afe-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="f7afe-109">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f7afe-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f7afe-110">Valige kaubakood BOM_2.</span><span class="sxs-lookup"><span data-stu-id="f7afe-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="f7afe-111">Klõpsake toimingupaanil suvandit Projekteeri.</span><span class="sxs-lookup"><span data-stu-id="f7afe-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="f7afe-112">Klõpsake koosluse versioone.</span><span class="sxs-lookup"><span data-stu-id="f7afe-112">Click BOM versions.</span></span>
5. <span data-ttu-id="f7afe-113">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f7afe-113">Click New.</span></span>
6. <span data-ttu-id="f7afe-114">Klõpsake kooslust ja koosluse versiooni.</span><span class="sxs-lookup"><span data-stu-id="f7afe-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="f7afe-115">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f7afe-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f7afe-116">Näiteks tippige BOM_2.</span><span class="sxs-lookup"><span data-stu-id="f7afe-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="f7afe-117">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="f7afe-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f7afe-118">Selles snäites sisestage või valige Sait 1.</span><span class="sxs-lookup"><span data-stu-id="f7afe-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="f7afe-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f7afe-119">Click OK.</span></span>
10. <span data-ttu-id="f7afe-120">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f7afe-120">Click New.</span></span>
11. <span data-ttu-id="f7afe-121">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="f7afe-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f7afe-122">Selles näites tippige ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="f7afe-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="f7afe-123">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="f7afe-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f7afe-124">Selles näites sisestage või valige 11.</span><span class="sxs-lookup"><span data-stu-id="f7afe-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="f7afe-125">Klõpsake päist.</span><span class="sxs-lookup"><span data-stu-id="f7afe-125">Click Header.</span></span>
14. <span data-ttu-id="f7afe-126">Klõpsake koosluste kinnitamiseks nuppu Kinnitus.</span><span class="sxs-lookup"><span data-stu-id="f7afe-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="f7afe-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f7afe-127">Click OK.</span></span>
16. <span data-ttu-id="f7afe-128">Klõpsake nuppu Kinnita.</span><span class="sxs-lookup"><span data-stu-id="f7afe-128">Click Approve.</span></span>
    * <span data-ttu-id="f7afe-129">Nupp Kinnita asub tööriistaribal koosluse versioonide jaotises.</span><span class="sxs-lookup"><span data-stu-id="f7afe-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="f7afe-130">Kui see on nähtamatu, klõpsake nupu Kinnita kuvamiseks lehekülje Kooslused ülanurgas nuppu Päis.</span><span class="sxs-lookup"><span data-stu-id="f7afe-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="f7afe-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f7afe-131">Click OK.</span></span>
18. <span data-ttu-id="f7afe-132">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="f7afe-132">Click Activate.</span></span>
19. <span data-ttu-id="f7afe-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7afe-133">Close the page.</span></span>
20. <span data-ttu-id="f7afe-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7afe-134">Close the page.</span></span>
21. <span data-ttu-id="f7afe-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7afe-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="f7afe-136">Koosluse loomine lõpetatud tootele</span><span class="sxs-lookup"><span data-stu-id="f7afe-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="f7afe-137">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f7afe-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f7afe-138">Valige kaubakood BOM_1.</span><span class="sxs-lookup"><span data-stu-id="f7afe-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="f7afe-139">Klõpsake toimingupaanil suvandit Projekteeri.</span><span class="sxs-lookup"><span data-stu-id="f7afe-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="f7afe-140">Klõpsake koosluse versioone.</span><span class="sxs-lookup"><span data-stu-id="f7afe-140">Click BOM versions.</span></span>
4. <span data-ttu-id="f7afe-141">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f7afe-141">Click New.</span></span>
5. <span data-ttu-id="f7afe-142">Klõpsake kooslust ja koosluse versiooni.</span><span class="sxs-lookup"><span data-stu-id="f7afe-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="f7afe-143">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f7afe-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f7afe-144">Näiteks tippige BOM_1.</span><span class="sxs-lookup"><span data-stu-id="f7afe-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="f7afe-145">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="f7afe-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f7afe-146">Selles snäites sisestage või valige Sait 1.</span><span class="sxs-lookup"><span data-stu-id="f7afe-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="f7afe-147">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f7afe-147">Click OK.</span></span>
9. <span data-ttu-id="f7afe-148">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f7afe-148">Click New.</span></span>
10. <span data-ttu-id="f7afe-149">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="f7afe-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f7afe-150">Selles näites tippige ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="f7afe-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="f7afe-151">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="f7afe-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f7afe-152">Selles näites valige 11.</span><span class="sxs-lookup"><span data-stu-id="f7afe-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="f7afe-153">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f7afe-153">Click New.</span></span>
13. <span data-ttu-id="f7afe-154">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="f7afe-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f7afe-155">Selles näites tippige ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="f7afe-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="f7afe-156">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="f7afe-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f7afe-157">Selles näites sisestage või valige 11.</span><span class="sxs-lookup"><span data-stu-id="f7afe-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="f7afe-158">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f7afe-158">Click New.</span></span>
16. <span data-ttu-id="f7afe-159">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="f7afe-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f7afe-160">Selles näites tippige BOM_2.</span><span class="sxs-lookup"><span data-stu-id="f7afe-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="f7afe-161">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="f7afe-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="f7afe-162">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="f7afe-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f7afe-163">Selles näites sisestage või valige ladu 11.</span><span class="sxs-lookup"><span data-stu-id="f7afe-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="f7afe-164">Klõpsake päist.</span><span class="sxs-lookup"><span data-stu-id="f7afe-164">Click Header.</span></span>
20. <span data-ttu-id="f7afe-165">Klõpsake koosluste kinnitamiseks nuppu Kinnitus.</span><span class="sxs-lookup"><span data-stu-id="f7afe-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="f7afe-166">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f7afe-166">Click OK.</span></span>
22. <span data-ttu-id="f7afe-167">Klõpsake nuppu Kinnita.</span><span class="sxs-lookup"><span data-stu-id="f7afe-167">Click Approve.</span></span>
    * <span data-ttu-id="f7afe-168">Nupp Kinnita asub tööriistaribal koosluse versioonide jaotises.</span><span class="sxs-lookup"><span data-stu-id="f7afe-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="f7afe-169">Kui see on nähtamatu, klõpsake nupu Kinnita kuvamiseks lehekülje Kooslused ülanurgas nuppu Päis.</span><span class="sxs-lookup"><span data-stu-id="f7afe-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="f7afe-170">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f7afe-170">Click OK.</span></span>
24. <span data-ttu-id="f7afe-171">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="f7afe-171">Click Activate.</span></span>
25. <span data-ttu-id="f7afe-172">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7afe-172">Close the page.</span></span>
26. <span data-ttu-id="f7afe-173">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7afe-173">Close the page.</span></span>
27. <span data-ttu-id="f7afe-174">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7afe-174">Close the page.</span></span>


