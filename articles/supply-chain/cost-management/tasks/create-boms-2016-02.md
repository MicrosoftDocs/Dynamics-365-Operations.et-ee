---
title: Koosluste loomine (ainult veebruar 2016)
description: See ülesanne keskendub lõpetatud ja pooleldi lõpetatud toote jaoks koosluse struktuuri loomisele.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f132a3865b180a74d328ebc76ca29b2fc8aee85f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563246"
---
# <a name="create-boms-february-2016-only"></a><span data-ttu-id="f6115-103">Koosluste loomine (ainult veebruar 2016)</span><span class="sxs-lookup"><span data-stu-id="f6115-103">Create BOMs (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f6115-104">See ülesanne keskendub lõpetatud ja pooleldi lõpetatud toote jaoks koosluse struktuuri loomisele.</span><span class="sxs-lookup"><span data-stu-id="f6115-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="f6115-105">See on neljas ülesanne koosluse arvutamise seerias.</span><span class="sxs-lookup"><span data-stu-id="f6115-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="f6115-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="f6115-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="f6115-107">Koosluse loomine pooleldi lõpetatud tootele</span><span class="sxs-lookup"><span data-stu-id="f6115-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="f6115-108">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="f6115-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="f6115-109">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f6115-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f6115-110">Valige kaubakood BOM_2.</span><span class="sxs-lookup"><span data-stu-id="f6115-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="f6115-111">Klõpsake toimingupaanil suvandit Projekteeri.</span><span class="sxs-lookup"><span data-stu-id="f6115-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="f6115-112">Klõpsake koosluse versioone.</span><span class="sxs-lookup"><span data-stu-id="f6115-112">Click BOM versions.</span></span>
5. <span data-ttu-id="f6115-113">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f6115-113">Click New.</span></span>
6. <span data-ttu-id="f6115-114">Klõpsake kooslust ja koosluse versiooni.</span><span class="sxs-lookup"><span data-stu-id="f6115-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="f6115-115">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f6115-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f6115-116">Näiteks tippige BOM_2.</span><span class="sxs-lookup"><span data-stu-id="f6115-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="f6115-117">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="f6115-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f6115-118">Selles snäites sisestage või valige Sait 1.</span><span class="sxs-lookup"><span data-stu-id="f6115-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="f6115-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f6115-119">Click OK.</span></span>
10. <span data-ttu-id="f6115-120">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f6115-120">Click New.</span></span>
11. <span data-ttu-id="f6115-121">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="f6115-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f6115-122">Selles näites tippige ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="f6115-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="f6115-123">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="f6115-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f6115-124">Selles näites sisestage või valige 11.</span><span class="sxs-lookup"><span data-stu-id="f6115-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="f6115-125">Klõpsake päist.</span><span class="sxs-lookup"><span data-stu-id="f6115-125">Click Header.</span></span>
14. <span data-ttu-id="f6115-126">Klõpsake koosluste kinnitamiseks nuppu Kinnitus.</span><span class="sxs-lookup"><span data-stu-id="f6115-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="f6115-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f6115-127">Click OK.</span></span>
16. <span data-ttu-id="f6115-128">Klõpsake nuppu Kinnita.</span><span class="sxs-lookup"><span data-stu-id="f6115-128">Click Approve.</span></span>
    * <span data-ttu-id="f6115-129">Nupp Kinnita asub tööriistaribal koosluse versioonide jaotises.</span><span class="sxs-lookup"><span data-stu-id="f6115-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="f6115-130">Kui see on nähtamatu, klõpsake nupu Kinnita kuvamiseks lehekülje Kooslused ülanurgas nuppu Päis.</span><span class="sxs-lookup"><span data-stu-id="f6115-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="f6115-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f6115-131">Click OK.</span></span>
18. <span data-ttu-id="f6115-132">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="f6115-132">Click Activate.</span></span>
19. <span data-ttu-id="f6115-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f6115-133">Close the page.</span></span>
20. <span data-ttu-id="f6115-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f6115-134">Close the page.</span></span>
21. <span data-ttu-id="f6115-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f6115-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="f6115-136">Koosluse loomine lõpetatud tootele</span><span class="sxs-lookup"><span data-stu-id="f6115-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="f6115-137">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f6115-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f6115-138">Valige kaubakood BOM_1.</span><span class="sxs-lookup"><span data-stu-id="f6115-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="f6115-139">Klõpsake toimingupaanil suvandit Projekteeri.</span><span class="sxs-lookup"><span data-stu-id="f6115-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="f6115-140">Klõpsake koosluse versioone.</span><span class="sxs-lookup"><span data-stu-id="f6115-140">Click BOM versions.</span></span>
4. <span data-ttu-id="f6115-141">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f6115-141">Click New.</span></span>
5. <span data-ttu-id="f6115-142">Klõpsake kooslust ja koosluse versiooni.</span><span class="sxs-lookup"><span data-stu-id="f6115-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="f6115-143">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f6115-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f6115-144">Näiteks tippige BOM_1.</span><span class="sxs-lookup"><span data-stu-id="f6115-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="f6115-145">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="f6115-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f6115-146">Selles snäites sisestage või valige Sait 1.</span><span class="sxs-lookup"><span data-stu-id="f6115-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="f6115-147">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f6115-147">Click OK.</span></span>
9. <span data-ttu-id="f6115-148">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f6115-148">Click New.</span></span>
10. <span data-ttu-id="f6115-149">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="f6115-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f6115-150">Selles näites tippige ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="f6115-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="f6115-151">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="f6115-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f6115-152">Selles näites valige 11.</span><span class="sxs-lookup"><span data-stu-id="f6115-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="f6115-153">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f6115-153">Click New.</span></span>
13. <span data-ttu-id="f6115-154">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="f6115-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f6115-155">Selles näites tippige ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="f6115-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="f6115-156">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="f6115-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f6115-157">Selles näites sisestage või valige 11.</span><span class="sxs-lookup"><span data-stu-id="f6115-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="f6115-158">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f6115-158">Click New.</span></span>
16. <span data-ttu-id="f6115-159">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="f6115-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f6115-160">Selles näites tippige BOM_2.</span><span class="sxs-lookup"><span data-stu-id="f6115-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="f6115-161">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="f6115-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="f6115-162">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="f6115-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f6115-163">Selles näites sisestage või valige ladu 11.</span><span class="sxs-lookup"><span data-stu-id="f6115-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="f6115-164">Klõpsake päist.</span><span class="sxs-lookup"><span data-stu-id="f6115-164">Click Header.</span></span>
20. <span data-ttu-id="f6115-165">Klõpsake koosluste kinnitamiseks nuppu Kinnitus.</span><span class="sxs-lookup"><span data-stu-id="f6115-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="f6115-166">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f6115-166">Click OK.</span></span>
22. <span data-ttu-id="f6115-167">Klõpsake nuppu Kinnita.</span><span class="sxs-lookup"><span data-stu-id="f6115-167">Click Approve.</span></span>
    * <span data-ttu-id="f6115-168">Nupp Kinnita asub tööriistaribal koosluse versioonide jaotises.</span><span class="sxs-lookup"><span data-stu-id="f6115-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="f6115-169">Kui see on nähtamatu, klõpsake nupu Kinnita kuvamiseks lehekülje Kooslused ülanurgas nuppu Päis.</span><span class="sxs-lookup"><span data-stu-id="f6115-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="f6115-170">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f6115-170">Click OK.</span></span>
24. <span data-ttu-id="f6115-171">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="f6115-171">Click Activate.</span></span>
25. <span data-ttu-id="f6115-172">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f6115-172">Close the page.</span></span>
26. <span data-ttu-id="f6115-173">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f6115-173">Close the page.</span></span>
27. <span data-ttu-id="f6115-174">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f6115-174">Close the page.</span></span>

