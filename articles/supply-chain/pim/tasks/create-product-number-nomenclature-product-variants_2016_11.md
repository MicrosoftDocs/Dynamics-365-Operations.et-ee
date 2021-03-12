---
title: Tootenumbri nomenklatuuri loomine konfigureeritud tootevariantide jaoks
description: See protseduur näitab, kuidas seadistada konfigureeritud tootevariantidele tootenumbri nomenklatuuri ja kuidas selle saab konfigureeritavale tooteetalonile manustada.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e52b7a5aff3e86e845484e1e84b4003cc4a52c95
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992366"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="bedaa-103">Tootenumbri nomenklatuuri loomine konfigureeritud tootevariantide jaoks</span><span class="sxs-lookup"><span data-stu-id="bedaa-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bedaa-104">See protseduur näitab, kuidas seadistada konfigureeritud tootevariantidele tootenumbri nomenklatuuri ja kuidas selle saab konfigureeritavale tooteetalonile manustada.</span><span class="sxs-lookup"><span data-stu-id="bedaa-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="bedaa-105">See protseduur näitab ka, kuidas toote konfiguratsioonimudeli komponendile konfiguratsiooni nomenklatuuri koostada.</span><span class="sxs-lookup"><span data-stu-id="bedaa-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="bedaa-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="bedaa-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="bedaa-107">Uus tootenumbri nomenklatuur määratakse D0004 tooteetalonile.</span><span class="sxs-lookup"><span data-stu-id="bedaa-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="bedaa-108">Enamasti teeb selle toimingu toote koostaja.</span><span class="sxs-lookup"><span data-stu-id="bedaa-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="bedaa-109">Tootenumbri nomenklatuuri loomine</span><span class="sxs-lookup"><span data-stu-id="bedaa-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="bedaa-110">Klõpsake valikut Tootevariandi mudeli määratlus.</span><span class="sxs-lookup"><span data-stu-id="bedaa-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="bedaa-111">Klõpsake valikut Tootenomenklatuur.</span><span class="sxs-lookup"><span data-stu-id="bedaa-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="bedaa-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="bedaa-112">Click New.</span></span>
4. <span data-ttu-id="bedaa-113">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="bedaa-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="bedaa-114">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="bedaa-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="bedaa-115">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="bedaa-115">Click Add.</span></span>
7. <span data-ttu-id="bedaa-116">Klõpsake valikut Tooteetaloni number.</span><span class="sxs-lookup"><span data-stu-id="bedaa-116">Click Product master number.</span></span>
8. <span data-ttu-id="bedaa-117">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="bedaa-117">Click Add.</span></span>
9. <span data-ttu-id="bedaa-118">Klõpsake valikut Tekstikonstant.</span><span class="sxs-lookup"><span data-stu-id="bedaa-118">Click Text constant.</span></span>
10. <span data-ttu-id="bedaa-119">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bedaa-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="bedaa-120">Sisestage väärtus väljale Tekst.</span><span class="sxs-lookup"><span data-stu-id="bedaa-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="bedaa-121">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="bedaa-121">Click Add.</span></span>
13. <span data-ttu-id="bedaa-122">Klõpsake valikut Konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="bedaa-122">Click Configuration.</span></span>
14. <span data-ttu-id="bedaa-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bedaa-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="bedaa-124">Tootenumbri nomenklatuuri määramine tooteetalonile</span><span class="sxs-lookup"><span data-stu-id="bedaa-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="bedaa-125">Klõpsake valikut Tooteetalonid.</span><span class="sxs-lookup"><span data-stu-id="bedaa-125">Click Product masters.</span></span>
2. <span data-ttu-id="bedaa-126">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="bedaa-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="bedaa-127">Näiteks saate filtreerida välja Tootenumber väärtuse D järgi.</span><span class="sxs-lookup"><span data-stu-id="bedaa-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="bedaa-128">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="bedaa-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="bedaa-129">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="bedaa-129">Click Edit.</span></span>
5. <span data-ttu-id="bedaa-130">Tehke väljal Kasuta nomenklatuuri valik Jah.</span><span class="sxs-lookup"><span data-stu-id="bedaa-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="bedaa-131">Sisestage või valige väärtus väljal Tootevariandi numbri nomenklatuur.</span><span class="sxs-lookup"><span data-stu-id="bedaa-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="bedaa-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bedaa-132">Close the page.</span></span>
8. <span data-ttu-id="bedaa-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bedaa-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="bedaa-134">Nomenklatuuri loomine toote konfiguratsioonimudeli komponendile</span><span class="sxs-lookup"><span data-stu-id="bedaa-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="bedaa-135">Klõpsake valikut Toote konfiguratsioonimudelid.</span><span class="sxs-lookup"><span data-stu-id="bedaa-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="bedaa-136">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bedaa-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="bedaa-137">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="bedaa-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="bedaa-138">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="bedaa-138">Click Edit.</span></span>
5. <span data-ttu-id="bedaa-139">Tehke väljal Kasuta konfiguratsiooni nomenklatuuri valik Jah.</span><span class="sxs-lookup"><span data-stu-id="bedaa-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="bedaa-140">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="bedaa-140">Click Add.</span></span>
7. <span data-ttu-id="bedaa-141">Klõpsake valikut Atribuudi väärtus.</span><span class="sxs-lookup"><span data-stu-id="bedaa-141">Click Attribute value.</span></span>
8. <span data-ttu-id="bedaa-142">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bedaa-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="bedaa-143">Valige või sisestage väärtus väljal Atribuut.</span><span class="sxs-lookup"><span data-stu-id="bedaa-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="bedaa-144">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="bedaa-144">Click Add.</span></span>
11. <span data-ttu-id="bedaa-145">Klõpsake valikut Tekstikonstant.</span><span class="sxs-lookup"><span data-stu-id="bedaa-145">Click Text constant.</span></span>
12. <span data-ttu-id="bedaa-146">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bedaa-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="bedaa-147">Sisestage väärtus väljale Tekst.</span><span class="sxs-lookup"><span data-stu-id="bedaa-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="bedaa-148">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="bedaa-148">Click Add.</span></span>
15. <span data-ttu-id="bedaa-149">Klõpsake valikut Atribuudi väärtus.</span><span class="sxs-lookup"><span data-stu-id="bedaa-149">Click Attribute value.</span></span>
16. <span data-ttu-id="bedaa-150">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bedaa-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="bedaa-151">Valige või sisestage väärtus väljal Atribuut.</span><span class="sxs-lookup"><span data-stu-id="bedaa-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="bedaa-152">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="bedaa-152">Click Add.</span></span>
19. <span data-ttu-id="bedaa-153">Klõpsake valikut Tekstikonstant.</span><span class="sxs-lookup"><span data-stu-id="bedaa-153">Click Text constant.</span></span>
20. <span data-ttu-id="bedaa-154">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bedaa-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="bedaa-155">Sisestage väärtus väljale Tekst.</span><span class="sxs-lookup"><span data-stu-id="bedaa-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="bedaa-156">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="bedaa-156">Click Add.</span></span>
23. <span data-ttu-id="bedaa-157">Klõpsake valikut Atribuudi väärtus.</span><span class="sxs-lookup"><span data-stu-id="bedaa-157">Click Attribute value.</span></span>
24. <span data-ttu-id="bedaa-158">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bedaa-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="bedaa-159">Valige või sisestage väärtus väljal Atribuut.</span><span class="sxs-lookup"><span data-stu-id="bedaa-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="bedaa-160">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="bedaa-160">Click Add.</span></span>
27. <span data-ttu-id="bedaa-161">Klõpsake valikut Tekstikonstant.</span><span class="sxs-lookup"><span data-stu-id="bedaa-161">Click Text constant.</span></span>
28. <span data-ttu-id="bedaa-162">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bedaa-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="bedaa-163">Sisestage väärtus väljale Tekst.</span><span class="sxs-lookup"><span data-stu-id="bedaa-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="bedaa-164">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="bedaa-164">Click Add.</span></span>
31. <span data-ttu-id="bedaa-165">Klõpsake valikut Atribuudi väärtus.</span><span class="sxs-lookup"><span data-stu-id="bedaa-165">Click Attribute value.</span></span>
32. <span data-ttu-id="bedaa-166">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bedaa-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="bedaa-167">Valige või sisestage väärtus väljal Atribuut.</span><span class="sxs-lookup"><span data-stu-id="bedaa-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="bedaa-168">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="bedaa-168">Click Add.</span></span>
35. <span data-ttu-id="bedaa-169">Klõpsake valikut Tekstikonstant.</span><span class="sxs-lookup"><span data-stu-id="bedaa-169">Click Text constant.</span></span>
36. <span data-ttu-id="bedaa-170">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bedaa-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="bedaa-171">Sisestage väärtus väljale Tekst.</span><span class="sxs-lookup"><span data-stu-id="bedaa-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="bedaa-172">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="bedaa-172">Click Add.</span></span>
39. <span data-ttu-id="bedaa-173">Klõpsake valikut Numbriseeria väärtus.</span><span class="sxs-lookup"><span data-stu-id="bedaa-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="bedaa-174">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bedaa-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="bedaa-175">Sisestage või valige väärtus väljal Numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="bedaa-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="bedaa-176">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bedaa-176">Close the page.</span></span>
43. <span data-ttu-id="bedaa-177">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bedaa-177">Close the page.</span></span>
44. <span data-ttu-id="bedaa-178">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bedaa-178">Close the page.</span></span>

