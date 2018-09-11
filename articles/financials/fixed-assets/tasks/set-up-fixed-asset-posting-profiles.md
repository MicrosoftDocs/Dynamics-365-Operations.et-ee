--- 
title: "Põhivara sisestusreeglite seadistamine"
description: "See ülesande juhend seadistab Põhivara sisestusreeglid."
author: saraschi2
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: b00ad7f8dc77eb80e0ed322c1e09624398cfc4d5
ms.contentlocale: et-ee
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="808df-103">Põhivara sisestusreeglite seadistamine</span><span class="sxs-lookup"><span data-stu-id="808df-103">Set up fixed asset posting profiles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="808df-104">See ülesande juhend seadistab Põhivara sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="808df-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="808df-105">See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="808df-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="808df-106">Ülesande juhendis esitatud näited kehtivad üldiste sisestusreeglite kohta, kuigi sisestusreeglid tuleb luua teie kindla kontoplaani ja finantsaruandluse nõuete puhul.</span><span class="sxs-lookup"><span data-stu-id="808df-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="808df-107">Avage Põhivarad > Seadistus > Põhivara sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="808df-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="808df-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="808df-108">Click New.</span></span>
3. <span data-ttu-id="808df-109">Sisestage väärtus väljale Sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="808df-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="808df-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="808df-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="808df-111">Peate looma sisestusreeglid iga põhivara kandetüübi puhul, mida põhivaradega töötades kasutate.</span><span class="sxs-lookup"><span data-stu-id="808df-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="808df-112">See ülesande juhend algab kandetüübiga Soetus.</span><span class="sxs-lookup"><span data-stu-id="808df-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="808df-113">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-113">Click Add.</span></span>
6. <span data-ttu-id="808df-114">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="808df-115">Väljal Grupeerimised saate määrata sisestusreeglid kuni tabeli (iga põhivara puhul ühe konto) või grupini (iga põhivaragrupi puhul ühe konto).</span><span class="sxs-lookup"><span data-stu-id="808df-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="808df-116">Selle ülesande juhendi puhul jätan väärtuse suvandile „Kõik” kõikide põhivarade rakendamiseks määratud raamatuga.</span><span class="sxs-lookup"><span data-stu-id="808df-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="808df-117">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="808df-118">Soetamiste puhul saate sisestada vastaskonto või jätta selle konkreetse kandega täitmiseks tühjaks.</span><span class="sxs-lookup"><span data-stu-id="808df-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="808df-119">Valige väljal Kande tüüp suvand Soetamise korrigeerimine.</span><span class="sxs-lookup"><span data-stu-id="808df-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="808df-120">Soetamise korrigeerimiskannete puhul kasutame samu kontosid kui soetuskannete puhul.</span><span class="sxs-lookup"><span data-stu-id="808df-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="808df-121">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-121">Click Add.</span></span>
10. <span data-ttu-id="808df-122">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="808df-123">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="808df-124">Soetusmaksumuse korrigeerimiste puhul saate sisestada vastaskonto või jätta selle konkreetse kandega täitmiseks tühjaks.</span><span class="sxs-lookup"><span data-stu-id="808df-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="808df-125">Valige väljal Kande tüüp suvand Kulum.</span><span class="sxs-lookup"><span data-stu-id="808df-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="808df-126">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-126">Click Add.</span></span>
14. <span data-ttu-id="808df-127">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="808df-128">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="808df-129">Täpsustage soovitud väärtusi väljal Vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="808df-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="808df-130">Valige väljal Kande tüüp suvand Kulumi korrigeerimine.</span><span class="sxs-lookup"><span data-stu-id="808df-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="808df-131">Kulumi korrigeerimiskannete puhul kasutame samu kontosid kui kulumikannete puhul.</span><span class="sxs-lookup"><span data-stu-id="808df-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="808df-132">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-132">Click Add.</span></span>
19. <span data-ttu-id="808df-133">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="808df-134">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="808df-135">Täpsustage soovitud väärtusi väljal Vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="808df-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="808df-136">Valige väljal Kande tüüp suvand Likvideerimine – müük.</span><span class="sxs-lookup"><span data-stu-id="808df-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="808df-137">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-137">Click Add.</span></span>
24. <span data-ttu-id="808df-138">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="808df-139">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="808df-140">Likvideerimiste puhul saate sisestada vastaskonto või jätta selle konkreetse kandega täitmiseks tühjaks.</span><span class="sxs-lookup"><span data-stu-id="808df-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="808df-141">Valige väljal Kande tüüp suvand Likvideerimine – mahakandmine.</span><span class="sxs-lookup"><span data-stu-id="808df-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="808df-142">Kasutame samu kontosid likvideerimismüügi ja likvideerimispraagi puhul.</span><span class="sxs-lookup"><span data-stu-id="808df-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="808df-143">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-143">Click Add.</span></span>
28. <span data-ttu-id="808df-144">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="808df-145">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="808df-146">Likvideerimiste puhul saate sisestada vastaskonto või jätta selle konkreetse kandega täitmiseks tühjaks.</span><span class="sxs-lookup"><span data-stu-id="808df-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="808df-147">Laiendage jaotist Likvideerimine.</span><span class="sxs-lookup"><span data-stu-id="808df-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="808df-148">Peate seadistama likvideerimise sisestusreeglid nii müügi kui ka mahakandmise puhul.</span><span class="sxs-lookup"><span data-stu-id="808df-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="808df-149">Alustame likvideerimise müügitehingutest.</span><span class="sxs-lookup"><span data-stu-id="808df-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="808df-150">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-150">Click Add.</span></span>
32. <span data-ttu-id="808df-151">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="808df-152">Valige väljal Järelväärtus suvand Soetusmaksumus.</span><span class="sxs-lookup"><span data-stu-id="808df-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="808df-153">Soetusmaksumus käsitleb väärtusi Soetus ja Soetuse korrigeerimine kõigi aastate puhul.</span><span class="sxs-lookup"><span data-stu-id="808df-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="808df-154">Samuti saate määratleda kontod nende kandetüüpide puhul eraldi.</span><span class="sxs-lookup"><span data-stu-id="808df-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="808df-155">Saate seadistada likvideerimisprotsessi eri kontosid kasutama, olenevalt sellest, kas likvideerimise tulemuseks on kasum või kahjum.</span><span class="sxs-lookup"><span data-stu-id="808df-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="808df-156">Seadistan väärtuse Müük tüübiks „Kõik”, et kasutada samu kontosid igat tüüpi likvideerimiste puhul.</span><span class="sxs-lookup"><span data-stu-id="808df-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="808df-157">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="808df-158">Täpsustage soovitud väärtusi väljal Vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="808df-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="808df-159">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-159">Click Add.</span></span>
37. <span data-ttu-id="808df-160">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="808df-161">Valige väljalt Järelväärtus suvand Kulum eelnenud aastatel.</span><span class="sxs-lookup"><span data-stu-id="808df-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="808df-162">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="808df-163">Täpsustage soovitud väärtusi väljal Vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="808df-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="808df-164">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-164">Click Add.</span></span>
41. <span data-ttu-id="808df-165">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="808df-166">Valige väljal Järelväärtus suvand Käesoleva aasta kulum.</span><span class="sxs-lookup"><span data-stu-id="808df-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="808df-167">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="808df-168">Täpsustage soovitud väärtusi väljal Vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="808df-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="808df-169">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-169">Click Add.</span></span>
46. <span data-ttu-id="808df-170">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="808df-171">Valige väljalt Järelväärtus suvand Kulumi korrigeerimised eelnenud aastatel.</span><span class="sxs-lookup"><span data-stu-id="808df-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="808df-172">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="808df-173">Täpsustage soovitud väärtusi väljal Vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="808df-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="808df-174">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-174">Click Add.</span></span>
51. <span data-ttu-id="808df-175">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="808df-176">Valige väljal Järelväärtus suvand Kulumi korrigeerimised sel aastal.</span><span class="sxs-lookup"><span data-stu-id="808df-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="808df-177">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="808df-178">Täpsustage soovitud väärtusi väljal Vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="808df-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="808df-179">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-179">Click Add.</span></span>
56. <span data-ttu-id="808df-180">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="808df-181">Valige väljalt Järelväärtus suvand Raamatupidamislik jääkväärtus.</span><span class="sxs-lookup"><span data-stu-id="808df-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="808df-182">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="808df-183">Täpsustage soovitud väärtusi väljal Vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="808df-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="808df-184">Valige väljalt Müük või mahakandmine suvand Mahakandmine.</span><span class="sxs-lookup"><span data-stu-id="808df-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="808df-185">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-185">Click Add.</span></span>
62. <span data-ttu-id="808df-186">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="808df-187">Valige väljal Järelväärtus suvand Soetusmaksumus.</span><span class="sxs-lookup"><span data-stu-id="808df-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="808df-188">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="808df-189">Täpsustage soovitud väärtusi väljal Vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="808df-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="808df-190">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-190">Click Add.</span></span>
67. <span data-ttu-id="808df-191">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="808df-192">Valige väljalt Järelväärtus suvand Kulum eelnenud aastatel.</span><span class="sxs-lookup"><span data-stu-id="808df-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="808df-193">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="808df-194">Täpsustage soovitud väärtusi väljal Vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="808df-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="808df-195">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-195">Click Add.</span></span>
71. <span data-ttu-id="808df-196">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="808df-197">Valige väljal Järelväärtus suvand Käesoleva aasta kulum.</span><span class="sxs-lookup"><span data-stu-id="808df-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="808df-198">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="808df-199">Täpsustage soovitud väärtusi väljal Vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="808df-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="808df-200">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-200">Click Add.</span></span>
76. <span data-ttu-id="808df-201">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="808df-202">Valige väljalt Järelväärtus suvand Kulumi korrigeerimised eelnenud aastatel.</span><span class="sxs-lookup"><span data-stu-id="808df-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="808df-203">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="808df-204">Täpsustage soovitud väärtusi väljal Vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="808df-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="808df-205">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-205">Click Add.</span></span>
81. <span data-ttu-id="808df-206">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="808df-207">Valige väljal Järelväärtus suvand Kulumi korrigeerimised sel aastal.</span><span class="sxs-lookup"><span data-stu-id="808df-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="808df-208">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="808df-209">Täpsustage soovitud väärtusi väljal Vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="808df-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="808df-210">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="808df-210">Click Add.</span></span>
86. <span data-ttu-id="808df-211">Valige või sisestage väärtus väljal Raamat.</span><span class="sxs-lookup"><span data-stu-id="808df-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="808df-212">Valige väljalt Järelväärtus suvand Raamatupidamislik jääkväärtus.</span><span class="sxs-lookup"><span data-stu-id="808df-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="808df-213">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="808df-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="808df-214">Täpsustage soovitud väärtusi väljal Vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="808df-214">In the Offset account field, specify the desired values.</span></span>


