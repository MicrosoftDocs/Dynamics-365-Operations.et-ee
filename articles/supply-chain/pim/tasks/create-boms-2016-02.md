---
title: Koosluste loomine (veebruar 2016)
description: See ülesanne keskendub lõpetatud ja pooleldi lõpetatud toote jaoks koosluse struktuuri loomisele.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0087c53d9cdc3bb65e6fa446c193c752d0f9b4fc
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845082"
---
# <a name="create-boms-february-2016"></a><span data-ttu-id="fd2ea-103">Koosluste loomine (veebruar 2016)</span><span class="sxs-lookup"><span data-stu-id="fd2ea-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd2ea-104">See ülesanne keskendub lõpetatud ja pooleldi lõpetatud toote jaoks koosluse struktuuri loomisele.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="fd2ea-105">See on neljas ülesanne koosluse arvutamise seerias.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="fd2ea-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="fd2ea-107">Koosluse loomine pooleldi lõpetatud tootele</span><span class="sxs-lookup"><span data-stu-id="fd2ea-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="fd2ea-108">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="fd2ea-109">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fd2ea-110">Valige kaubakood BOM_2.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="fd2ea-111">Klõpsake toimingupaanil suvandit Projekteeri.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="fd2ea-112">Klõpsake koosluse versioone.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-112">Click BOM versions.</span></span>
5. <span data-ttu-id="fd2ea-113">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-113">Click New.</span></span>
6. <span data-ttu-id="fd2ea-114">Klõpsake kooslust ja koosluse versiooni.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="fd2ea-115">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="fd2ea-116">Näiteks tippige BOM_2.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="fd2ea-117">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="fd2ea-118">Selles snäites sisestage või valige Sait 1.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="fd2ea-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-119">Click OK.</span></span>
10. <span data-ttu-id="fd2ea-120">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-120">Click New.</span></span>
11. <span data-ttu-id="fd2ea-121">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="fd2ea-122">Selles näites tippige ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="fd2ea-123">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="fd2ea-124">Selles näites sisestage või valige 11.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="fd2ea-125">Klõpsake päist.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-125">Click Header.</span></span>
14. <span data-ttu-id="fd2ea-126">Klõpsake koosluste kinnitamiseks nuppu Kinnitus.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="fd2ea-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-127">Click OK.</span></span>
16. <span data-ttu-id="fd2ea-128">Klõpsake nuppu Kinnita.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-128">Click Approve.</span></span>
    * <span data-ttu-id="fd2ea-129">Nupp Kinnita asub tööriistaribal koosluse versioonide jaotises.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="fd2ea-130">Kui see on nähtamatu, klõpsake nupu Kinnita kuvamiseks lehekülje Kooslused ülanurgas nuppu Päis.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="fd2ea-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-131">Click OK.</span></span>
18. <span data-ttu-id="fd2ea-132">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-132">Click Activate.</span></span>
19. <span data-ttu-id="fd2ea-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-133">Close the page.</span></span>
20. <span data-ttu-id="fd2ea-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-134">Close the page.</span></span>
21. <span data-ttu-id="fd2ea-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="fd2ea-136">Koosluse loomine lõpetatud tootele</span><span class="sxs-lookup"><span data-stu-id="fd2ea-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="fd2ea-137">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="fd2ea-138">Valige kaubakood BOM_1.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="fd2ea-139">Klõpsake toimingupaanil suvandit Projekteeri.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="fd2ea-140">Klõpsake koosluse versioone.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-140">Click BOM versions.</span></span>
4. <span data-ttu-id="fd2ea-141">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-141">Click New.</span></span>
5. <span data-ttu-id="fd2ea-142">Klõpsake kooslust ja koosluse versiooni.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="fd2ea-143">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="fd2ea-144">Näiteks tippige BOM_1.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="fd2ea-145">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="fd2ea-146">Selles snäites sisestage või valige Sait 1.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="fd2ea-147">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-147">Click OK.</span></span>
9. <span data-ttu-id="fd2ea-148">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-148">Click New.</span></span>
10. <span data-ttu-id="fd2ea-149">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="fd2ea-150">Selles näites tippige ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="fd2ea-151">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="fd2ea-152">Selles näites valige 11.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="fd2ea-153">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-153">Click New.</span></span>
13. <span data-ttu-id="fd2ea-154">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="fd2ea-155">Selles näites tippige ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="fd2ea-156">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="fd2ea-157">Selles näites sisestage või valige 11.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="fd2ea-158">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-158">Click New.</span></span>
16. <span data-ttu-id="fd2ea-159">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="fd2ea-160">Selles näites tippige BOM_2.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="fd2ea-161">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="fd2ea-162">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="fd2ea-163">Selles näites sisestage või valige ladu 11.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="fd2ea-164">Klõpsake päist.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-164">Click Header.</span></span>
20. <span data-ttu-id="fd2ea-165">Klõpsake koosluste kinnitamiseks nuppu Kinnitus.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="fd2ea-166">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-166">Click OK.</span></span>
22. <span data-ttu-id="fd2ea-167">Klõpsake nuppu Kinnita.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-167">Click Approve.</span></span>
    * <span data-ttu-id="fd2ea-168">Nupp Kinnita asub tööriistaribal koosluse versioonide jaotises.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="fd2ea-169">Kui see on nähtamatu, klõpsake nupu Kinnita kuvamiseks lehekülje Kooslused ülanurgas nuppu Päis.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="fd2ea-170">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-170">Click OK.</span></span>
24. <span data-ttu-id="fd2ea-171">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-171">Click Activate.</span></span>
25. <span data-ttu-id="fd2ea-172">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-172">Close the page.</span></span>
26. <span data-ttu-id="fd2ea-173">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-173">Close the page.</span></span>
27. <span data-ttu-id="fd2ea-174">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fd2ea-174">Close the page.</span></span>

