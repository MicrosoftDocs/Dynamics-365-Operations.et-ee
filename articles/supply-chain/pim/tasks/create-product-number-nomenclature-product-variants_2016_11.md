--- 
title: Tootenumbri loomine konfigureeritud tootevariantide jaoks
description: "See protseduur näitab, kuidas seadistada konfigureeritud tootevariantidele tootenumbri nomenklatuuri ja kuidas selle saab konfigureeritavale tooteetalonile manustada."
author: BibiSp
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e70a5f28635e75a69811085637f7e7431c0f1d40
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-product-number-for-configured-product-variants"></a><span data-ttu-id="b4718-103">Tootenumbri loomine konfigureeritud tootevariantide jaoks</span><span class="sxs-lookup"><span data-stu-id="b4718-103">Create a product number for configured product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b4718-104">See protseduur näitab, kuidas seadistada konfigureeritud tootevariantidele tootenumbri nomenklatuuri ja kuidas selle saab konfigureeritavale tooteetalonile manustada.</span><span class="sxs-lookup"><span data-stu-id="b4718-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="b4718-105">See protseduur näitab ka, kuidas toote konfiguratsioonimudeli komponendile konfiguratsiooni nomenklatuuri koostada.</span><span class="sxs-lookup"><span data-stu-id="b4718-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="b4718-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="b4718-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b4718-107">Uus tootenumbri nomenklatuur määratakse D0004 tooteetalonile.</span><span class="sxs-lookup"><span data-stu-id="b4718-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="b4718-108">Enamasti teeb selle toimingu toote koostaja.</span><span class="sxs-lookup"><span data-stu-id="b4718-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="b4718-109">Tootenumbri nomenklatuuri loomine</span><span class="sxs-lookup"><span data-stu-id="b4718-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="b4718-110">Klõpsake valikut Tootevariandi mudeli määratlus.</span><span class="sxs-lookup"><span data-stu-id="b4718-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="b4718-111">Klõpsake valikut Tootenomenklatuur.</span><span class="sxs-lookup"><span data-stu-id="b4718-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="b4718-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b4718-112">Click New.</span></span>
4. <span data-ttu-id="b4718-113">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="b4718-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="b4718-114">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="b4718-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="b4718-115">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b4718-115">Click Add.</span></span>
7. <span data-ttu-id="b4718-116">Klõpsake valikut Tooteetaloni number.</span><span class="sxs-lookup"><span data-stu-id="b4718-116">Click Product master number.</span></span>
8. <span data-ttu-id="b4718-117">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b4718-117">Click Add.</span></span>
9. <span data-ttu-id="b4718-118">Klõpsake valikut Tekstikonstant.</span><span class="sxs-lookup"><span data-stu-id="b4718-118">Click Text constant.</span></span>
10. <span data-ttu-id="b4718-119">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b4718-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="b4718-120">Sisestage väärtus väljale Tekst.</span><span class="sxs-lookup"><span data-stu-id="b4718-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="b4718-121">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b4718-121">Click Add.</span></span>
13. <span data-ttu-id="b4718-122">Klõpsake valikut Konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="b4718-122">Click Configuration.</span></span>
14. <span data-ttu-id="b4718-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b4718-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="b4718-124">Tootenumbri nomenklatuuri määramine tooteetalonile</span><span class="sxs-lookup"><span data-stu-id="b4718-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="b4718-125">Klõpsake valikut Tooteetalonid.</span><span class="sxs-lookup"><span data-stu-id="b4718-125">Click Product masters.</span></span>
2. <span data-ttu-id="b4718-126">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="b4718-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b4718-127">Näiteks saate filtreerida välja Tootenumber väärtuse D järgi.</span><span class="sxs-lookup"><span data-stu-id="b4718-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="b4718-128">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b4718-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b4718-129">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="b4718-129">Click Edit.</span></span>
5. <span data-ttu-id="b4718-130">Tehke väljal Kasuta nomenklatuuri valik Jah.</span><span class="sxs-lookup"><span data-stu-id="b4718-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="b4718-131">Sisestage või valige väärtus väljal Tootevariandi numbri nomenklatuur.</span><span class="sxs-lookup"><span data-stu-id="b4718-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="b4718-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b4718-132">Close the page.</span></span>
8. <span data-ttu-id="b4718-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b4718-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="b4718-134">Nomenklatuuri loomine toote konfiguratsioonimudeli komponendile</span><span class="sxs-lookup"><span data-stu-id="b4718-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="b4718-135">Klõpsake valikut Toote konfiguratsioonimudelid.</span><span class="sxs-lookup"><span data-stu-id="b4718-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="b4718-136">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b4718-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b4718-137">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b4718-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b4718-138">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="b4718-138">Click Edit.</span></span>
5. <span data-ttu-id="b4718-139">Tehke väljal Kasuta konfiguratsiooni nomenklatuuri valik Jah.</span><span class="sxs-lookup"><span data-stu-id="b4718-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="b4718-140">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b4718-140">Click Add.</span></span>
7. <span data-ttu-id="b4718-141">Klõpsake valikut Atribuudi väärtus.</span><span class="sxs-lookup"><span data-stu-id="b4718-141">Click Attribute value.</span></span>
8. <span data-ttu-id="b4718-142">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b4718-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="b4718-143">Valige või sisestage väärtus väljal Atribuut.</span><span class="sxs-lookup"><span data-stu-id="b4718-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="b4718-144">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b4718-144">Click Add.</span></span>
11. <span data-ttu-id="b4718-145">Klõpsake valikut Tekstikonstant.</span><span class="sxs-lookup"><span data-stu-id="b4718-145">Click Text constant.</span></span>
12. <span data-ttu-id="b4718-146">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b4718-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="b4718-147">Sisestage väärtus väljale Tekst.</span><span class="sxs-lookup"><span data-stu-id="b4718-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="b4718-148">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b4718-148">Click Add.</span></span>
15. <span data-ttu-id="b4718-149">Klõpsake valikut Atribuudi väärtus.</span><span class="sxs-lookup"><span data-stu-id="b4718-149">Click Attribute value.</span></span>
16. <span data-ttu-id="b4718-150">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b4718-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="b4718-151">Valige või sisestage väärtus väljal Atribuut.</span><span class="sxs-lookup"><span data-stu-id="b4718-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="b4718-152">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b4718-152">Click Add.</span></span>
19. <span data-ttu-id="b4718-153">Klõpsake valikut Tekstikonstant.</span><span class="sxs-lookup"><span data-stu-id="b4718-153">Click Text constant.</span></span>
20. <span data-ttu-id="b4718-154">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b4718-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="b4718-155">Sisestage väärtus väljale Tekst.</span><span class="sxs-lookup"><span data-stu-id="b4718-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="b4718-156">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b4718-156">Click Add.</span></span>
23. <span data-ttu-id="b4718-157">Klõpsake valikut Atribuudi väärtus.</span><span class="sxs-lookup"><span data-stu-id="b4718-157">Click Attribute value.</span></span>
24. <span data-ttu-id="b4718-158">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b4718-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="b4718-159">Valige või sisestage väärtus väljal Atribuut.</span><span class="sxs-lookup"><span data-stu-id="b4718-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="b4718-160">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b4718-160">Click Add.</span></span>
27. <span data-ttu-id="b4718-161">Klõpsake valikut Tekstikonstant.</span><span class="sxs-lookup"><span data-stu-id="b4718-161">Click Text constant.</span></span>
28. <span data-ttu-id="b4718-162">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b4718-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="b4718-163">Sisestage väärtus väljale Tekst.</span><span class="sxs-lookup"><span data-stu-id="b4718-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="b4718-164">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b4718-164">Click Add.</span></span>
31. <span data-ttu-id="b4718-165">Klõpsake valikut Atribuudi väärtus.</span><span class="sxs-lookup"><span data-stu-id="b4718-165">Click Attribute value.</span></span>
32. <span data-ttu-id="b4718-166">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b4718-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="b4718-167">Valige või sisestage väärtus väljal Atribuut.</span><span class="sxs-lookup"><span data-stu-id="b4718-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="b4718-168">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b4718-168">Click Add.</span></span>
35. <span data-ttu-id="b4718-169">Klõpsake valikut Tekstikonstant.</span><span class="sxs-lookup"><span data-stu-id="b4718-169">Click Text constant.</span></span>
36. <span data-ttu-id="b4718-170">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b4718-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="b4718-171">Sisestage väärtus väljale Tekst.</span><span class="sxs-lookup"><span data-stu-id="b4718-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="b4718-172">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b4718-172">Click Add.</span></span>
39. <span data-ttu-id="b4718-173">Klõpsake valikut Numbriseeria väärtus.</span><span class="sxs-lookup"><span data-stu-id="b4718-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="b4718-174">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b4718-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="b4718-175">Sisestage või valige väärtus väljal Numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="b4718-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="b4718-176">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b4718-176">Close the page.</span></span>
43. <span data-ttu-id="b4718-177">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b4718-177">Close the page.</span></span>
44. <span data-ttu-id="b4718-178">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b4718-178">Close the page.</span></span>


