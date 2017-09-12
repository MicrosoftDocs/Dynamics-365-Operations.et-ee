--- 
title: Organisatsiooni aruandehierarhia loomine
description: Selle toimingu abil saate luua aruandehierarhia organisatsiooni aruandluse jaoks.
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f593c59660abcf5b0d5771ddd9daced6ec5fbfb4
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="6edf8-103">Organisatsiooni aruandehierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="6edf8-103">Create an organization report hierarchy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6edf8-104">Selle toimingu abil saate luua aruandehierarhia organisatsiooni aruandluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="6edf8-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="6edf8-105">Salvestise eesmärk on juhendada teid dimensioonihierarhias, et saaksite jätkata seni, kuni kogu organisatsiooni aruandlusstruktuur on loodud.</span><span class="sxs-lookup"><span data-stu-id="6edf8-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="6edf8-106">See salvestis kasutab USP2 demoandmete ettevõtet.</span><span class="sxs-lookup"><span data-stu-id="6edf8-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="6edf8-107">Valige menüü Kuluarvestus jaotis Dimensioonid ja seejärel jaotis Dimensioonihierarhiad.</span><span class="sxs-lookup"><span data-stu-id="6edf8-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="6edf8-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6edf8-108">Click New.</span></span>
3. <span data-ttu-id="6edf8-109">Valige väljal HierarchyTypeComboBox väärtus Dimensiooni klassifitseerimishierarhia.</span><span class="sxs-lookup"><span data-stu-id="6edf8-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="6edf8-110">Valige suvand Dimensiooni klassifitseerimishierarhia.</span><span class="sxs-lookup"><span data-stu-id="6edf8-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="6edf8-111">Tüüpi Dimensiooni klassifitseerimishierarhia kasutatakse reeglite määratlemiseks ja aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="6edf8-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="6edf8-112">See toetab kõiki dimensioone, nt kuluobjekte, kuluelemente ja statistilisi dimensioone.</span><span class="sxs-lookup"><span data-stu-id="6edf8-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="6edf8-113">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="6edf8-113">Click Create.</span></span>
5. <span data-ttu-id="6edf8-114">Tippige väljale Dimensioonihierarhia nimi väärtus Organisatsioon USP2.</span><span class="sxs-lookup"><span data-stu-id="6edf8-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="6edf8-115">Sisestage või valige väärtus väljal Dimensioon.</span><span class="sxs-lookup"><span data-stu-id="6edf8-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="6edf8-116">Valige suvand Kulukeskused.</span><span class="sxs-lookup"><span data-stu-id="6edf8-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="6edf8-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6edf8-117">Click Save.</span></span>
8. <span data-ttu-id="6edf8-118">Klõpsake käsku Kuva hierarhia.</span><span class="sxs-lookup"><span data-stu-id="6edf8-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="6edf8-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6edf8-119">Click New.</span></span>
10. <span data-ttu-id="6edf8-120">Tippige väljale Sõlme nimi väärtus CEO.</span><span class="sxs-lookup"><span data-stu-id="6edf8-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="6edf8-121">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6edf8-121">Click Save.</span></span>
12. <span data-ttu-id="6edf8-122">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6edf8-122">Click New.</span></span>
13. <span data-ttu-id="6edf8-123">Tippige väljale Sõlme nimi väärtus CEO kulukeskused.</span><span class="sxs-lookup"><span data-stu-id="6edf8-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="6edf8-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6edf8-124">Click Save.</span></span>
15. <span data-ttu-id="6edf8-125">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6edf8-125">Click New.</span></span>
16. <span data-ttu-id="6edf8-126">Tippige väljale Sõlme nimi väärtus Piirkond Ida.</span><span class="sxs-lookup"><span data-stu-id="6edf8-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="6edf8-127">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6edf8-127">Click Save.</span></span>
18. <span data-ttu-id="6edf8-128">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6edf8-128">Click New.</span></span>
19. <span data-ttu-id="6edf8-129">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6edf8-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="6edf8-130">Sisestage või valige väärtus väljal Lähtedimensiooni liige.</span><span class="sxs-lookup"><span data-stu-id="6edf8-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6edf8-131">Valige sõlmele vastav dimensiooniliige.</span><span class="sxs-lookup"><span data-stu-id="6edf8-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="6edf8-132">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6edf8-132">Click Save.</span></span>
22. <span data-ttu-id="6edf8-133">Valige puus väärtus Organisatsiooni USP2\CEO\CEO kulukeskused.</span><span class="sxs-lookup"><span data-stu-id="6edf8-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="6edf8-134">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6edf8-134">Click New.</span></span>
24. <span data-ttu-id="6edf8-135">Tippige väljale Sõlme nimi väärtus Piirkond Lääs.</span><span class="sxs-lookup"><span data-stu-id="6edf8-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="6edf8-136">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6edf8-136">Click Save.</span></span>
26. <span data-ttu-id="6edf8-137">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6edf8-137">Click New.</span></span>
27. <span data-ttu-id="6edf8-138">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6edf8-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="6edf8-139">Sisestage või valige väärtus väljal Lähtedimensiooni liige.</span><span class="sxs-lookup"><span data-stu-id="6edf8-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6edf8-140">Valige sõlmele vastav dimensiooniliige.</span><span class="sxs-lookup"><span data-stu-id="6edf8-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="6edf8-141">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6edf8-141">Click Save.</span></span>
30. <span data-ttu-id="6edf8-142">Valige puus väärtus Organisatsiooni USP2\CEO.</span><span class="sxs-lookup"><span data-stu-id="6edf8-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="6edf8-143">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6edf8-143">Click New.</span></span>
32. <span data-ttu-id="6edf8-144">Tippige väljale Sõlme nimi väärtus CFO kulukeskused.</span><span class="sxs-lookup"><span data-stu-id="6edf8-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="6edf8-145">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6edf8-145">Click Save.</span></span>
34. <span data-ttu-id="6edf8-146">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6edf8-146">Click New.</span></span>
35. <span data-ttu-id="6edf8-147">Tippige väljale Sõlme nimi väärtus Turunduskampaania.</span><span class="sxs-lookup"><span data-stu-id="6edf8-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="6edf8-148">Tippige väljale Sõlme nimi väärtus Turunduskampaania.</span><span class="sxs-lookup"><span data-stu-id="6edf8-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="6edf8-149">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6edf8-149">Click Save.</span></span>
38. <span data-ttu-id="6edf8-150">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6edf8-150">Click New.</span></span>
39. <span data-ttu-id="6edf8-151">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6edf8-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="6edf8-152">Sisestage või valige väärtus väljal Lähtedimensiooni liige.</span><span class="sxs-lookup"><span data-stu-id="6edf8-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6edf8-153">Valige sõlmele vastav dimensiooniliige.</span><span class="sxs-lookup"><span data-stu-id="6edf8-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="6edf8-154">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6edf8-154">Click Save.</span></span>
42. <span data-ttu-id="6edf8-155">Valige puus väärtus Organisatsiooni USP2\CEO\CFO kulukeskused.</span><span class="sxs-lookup"><span data-stu-id="6edf8-155">In the tree, select 'Oganization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="6edf8-156">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6edf8-156">Click New.</span></span>
44. <span data-ttu-id="6edf8-157">Tippige väljale Sõlme nimi väärtus Kaubandusnäitused.</span><span class="sxs-lookup"><span data-stu-id="6edf8-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="6edf8-158">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6edf8-158">Click Save.</span></span>
46. <span data-ttu-id="6edf8-159">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6edf8-159">Click New.</span></span>
47. <span data-ttu-id="6edf8-160">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6edf8-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="6edf8-161">Sisestage või valige väärtus väljal Lähtedimensiooni liige.</span><span class="sxs-lookup"><span data-stu-id="6edf8-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6edf8-162">Valige sõlmele vastav dimensiooniliige.</span><span class="sxs-lookup"><span data-stu-id="6edf8-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="6edf8-163">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6edf8-163">Click Save.</span></span>
50. <span data-ttu-id="6edf8-164">Valige puus väärtus Organisatsiooni USP2\CEO.</span><span class="sxs-lookup"><span data-stu-id="6edf8-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="6edf8-165">Tippige väljale Sõlme nimi väärtus CIO kulukeskused.</span><span class="sxs-lookup"><span data-stu-id="6edf8-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="6edf8-166">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6edf8-166">Click Save.</span></span>
53. <span data-ttu-id="6edf8-167">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6edf8-167">Click New.</span></span>
54. <span data-ttu-id="6edf8-168">Tippige väljale Sõlme nimi väärtus Kõnekeskused.</span><span class="sxs-lookup"><span data-stu-id="6edf8-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="6edf8-169">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6edf8-169">Click Save.</span></span>
56. <span data-ttu-id="6edf8-170">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6edf8-170">Click New.</span></span>
57. <span data-ttu-id="6edf8-171">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6edf8-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="6edf8-172">Sisestage või valige väärtus väljal Lähtedimensiooni liige.</span><span class="sxs-lookup"><span data-stu-id="6edf8-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="6edf8-173">Valige sõlmele vastav dimensiooniliige.</span><span class="sxs-lookup"><span data-stu-id="6edf8-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="6edf8-174">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6edf8-174">Click Save.</span></span>


