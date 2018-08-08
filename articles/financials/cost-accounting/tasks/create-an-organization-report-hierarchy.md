--- 
title: Organisatsiooni aruandehierarhia loomine
description: Selle toimingu abil saate luua aruandehierarhia organisatsiooni aruandluse jaoks.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: d9a06a67f851e4a73df90f999683d5ea27f38e66
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="71378-103">Organisatsiooni aruandehierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="71378-103">Create an organization report hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71378-104">Selle toimingu abil saate luua aruandehierarhia organisatsiooni aruandluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="71378-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="71378-105">Salvestise eesmärk on juhendada teid dimensioonihierarhias, et saaksite jätkata seni, kuni kogu organisatsiooni aruandlusstruktuur on loodud.</span><span class="sxs-lookup"><span data-stu-id="71378-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="71378-106">See salvestis kasutab USP2 demoandmete ettevõtet.</span><span class="sxs-lookup"><span data-stu-id="71378-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="71378-107">Valige menüü Kuluarvestus jaotis Dimensioonid ja seejärel jaotis Dimensioonihierarhiad.</span><span class="sxs-lookup"><span data-stu-id="71378-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="71378-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="71378-108">Click New.</span></span>
3. <span data-ttu-id="71378-109">Valige väljal HierarchyTypeComboBox väärtus Dimensiooni klassifitseerimishierarhia.</span><span class="sxs-lookup"><span data-stu-id="71378-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="71378-110">Valige suvand Dimensiooni klassifitseerimishierarhia.</span><span class="sxs-lookup"><span data-stu-id="71378-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="71378-111">Tüüpi Dimensiooni klassifitseerimishierarhia kasutatakse reeglite määratlemiseks ja aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="71378-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="71378-112">See toetab kõiki dimensioone, nt kuluobjekte, kuluelemente ja statistilisi dimensioone.</span><span class="sxs-lookup"><span data-stu-id="71378-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="71378-113">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="71378-113">Click Create.</span></span>
5. <span data-ttu-id="71378-114">Tippige väljale Dimensioonihierarhia nimi väärtus Organisatsioon USP2.</span><span class="sxs-lookup"><span data-stu-id="71378-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="71378-115">Sisestage või valige väärtus väljal Dimensioon.</span><span class="sxs-lookup"><span data-stu-id="71378-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="71378-116">Valige suvand Kulukeskused.</span><span class="sxs-lookup"><span data-stu-id="71378-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="71378-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="71378-117">Click Save.</span></span>
8. <span data-ttu-id="71378-118">Klõpsake käsku Kuva hierarhia.</span><span class="sxs-lookup"><span data-stu-id="71378-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="71378-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="71378-119">Click New.</span></span>
10. <span data-ttu-id="71378-120">Tippige väljale Sõlme nimi väärtus CEO.</span><span class="sxs-lookup"><span data-stu-id="71378-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="71378-121">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="71378-121">Click Save.</span></span>
12. <span data-ttu-id="71378-122">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="71378-122">Click New.</span></span>
13. <span data-ttu-id="71378-123">Tippige väljale Sõlme nimi väärtus CEO kulukeskused.</span><span class="sxs-lookup"><span data-stu-id="71378-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="71378-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="71378-124">Click Save.</span></span>
15. <span data-ttu-id="71378-125">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="71378-125">Click New.</span></span>
16. <span data-ttu-id="71378-126">Tippige väljale Sõlme nimi väärtus Piirkond Ida.</span><span class="sxs-lookup"><span data-stu-id="71378-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="71378-127">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="71378-127">Click Save.</span></span>
18. <span data-ttu-id="71378-128">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="71378-128">Click New.</span></span>
19. <span data-ttu-id="71378-129">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="71378-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="71378-130">Sisestage või valige väärtus väljal Lähtedimensiooni liige.</span><span class="sxs-lookup"><span data-stu-id="71378-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="71378-131">Valige sõlmele vastav dimensiooniliige.</span><span class="sxs-lookup"><span data-stu-id="71378-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="71378-132">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="71378-132">Click Save.</span></span>
22. <span data-ttu-id="71378-133">Valige puus väärtus Organisatsiooni USP2\CEO\CEO kulukeskused.</span><span class="sxs-lookup"><span data-stu-id="71378-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="71378-134">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="71378-134">Click New.</span></span>
24. <span data-ttu-id="71378-135">Tippige väljale Sõlme nimi väärtus Piirkond Lääs.</span><span class="sxs-lookup"><span data-stu-id="71378-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="71378-136">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="71378-136">Click Save.</span></span>
26. <span data-ttu-id="71378-137">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="71378-137">Click New.</span></span>
27. <span data-ttu-id="71378-138">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="71378-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="71378-139">Sisestage või valige väärtus väljal Lähtedimensiooni liige.</span><span class="sxs-lookup"><span data-stu-id="71378-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="71378-140">Valige sõlmele vastav dimensiooniliige.</span><span class="sxs-lookup"><span data-stu-id="71378-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="71378-141">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="71378-141">Click Save.</span></span>
30. <span data-ttu-id="71378-142">Valige puus väärtus Organisatsiooni USP2\CEO.</span><span class="sxs-lookup"><span data-stu-id="71378-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="71378-143">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="71378-143">Click New.</span></span>
32. <span data-ttu-id="71378-144">Tippige väljale Sõlme nimi väärtus CFO kulukeskused.</span><span class="sxs-lookup"><span data-stu-id="71378-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="71378-145">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="71378-145">Click Save.</span></span>
34. <span data-ttu-id="71378-146">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="71378-146">Click New.</span></span>
35. <span data-ttu-id="71378-147">Tippige väljale Sõlme nimi väärtus Turunduskampaania.</span><span class="sxs-lookup"><span data-stu-id="71378-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="71378-148">Tippige väljale Sõlme nimi väärtus Turunduskampaania.</span><span class="sxs-lookup"><span data-stu-id="71378-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="71378-149">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="71378-149">Click Save.</span></span>
38. <span data-ttu-id="71378-150">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="71378-150">Click New.</span></span>
39. <span data-ttu-id="71378-151">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="71378-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="71378-152">Sisestage või valige väärtus väljal Lähtedimensiooni liige.</span><span class="sxs-lookup"><span data-stu-id="71378-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="71378-153">Valige sõlmele vastav dimensiooniliige.</span><span class="sxs-lookup"><span data-stu-id="71378-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="71378-154">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="71378-154">Click Save.</span></span>
42. <span data-ttu-id="71378-155">Valige puus väärtus Organisatsiooni USP2\CEO\CFO kulukeskused.</span><span class="sxs-lookup"><span data-stu-id="71378-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="71378-156">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="71378-156">Click New.</span></span>
44. <span data-ttu-id="71378-157">Tippige väljale Sõlme nimi väärtus Kaubandusnäitused.</span><span class="sxs-lookup"><span data-stu-id="71378-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="71378-158">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="71378-158">Click Save.</span></span>
46. <span data-ttu-id="71378-159">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="71378-159">Click New.</span></span>
47. <span data-ttu-id="71378-160">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="71378-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="71378-161">Sisestage või valige väärtus väljal Lähtedimensiooni liige.</span><span class="sxs-lookup"><span data-stu-id="71378-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="71378-162">Valige sõlmele vastav dimensiooniliige.</span><span class="sxs-lookup"><span data-stu-id="71378-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="71378-163">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="71378-163">Click Save.</span></span>
50. <span data-ttu-id="71378-164">Valige puus väärtus Organisatsiooni USP2\CEO.</span><span class="sxs-lookup"><span data-stu-id="71378-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="71378-165">Tippige väljale Sõlme nimi väärtus CIO kulukeskused.</span><span class="sxs-lookup"><span data-stu-id="71378-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="71378-166">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="71378-166">Click Save.</span></span>
53. <span data-ttu-id="71378-167">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="71378-167">Click New.</span></span>
54. <span data-ttu-id="71378-168">Tippige väljale Sõlme nimi väärtus Kõnekeskused.</span><span class="sxs-lookup"><span data-stu-id="71378-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="71378-169">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="71378-169">Click Save.</span></span>
56. <span data-ttu-id="71378-170">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="71378-170">Click New.</span></span>
57. <span data-ttu-id="71378-171">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="71378-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="71378-172">Sisestage või valige väärtus väljal Lähtedimensiooni liige.</span><span class="sxs-lookup"><span data-stu-id="71378-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="71378-173">Valige sõlmele vastav dimensiooniliige.</span><span class="sxs-lookup"><span data-stu-id="71378-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="71378-174">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="71378-174">Click Save.</span></span>


