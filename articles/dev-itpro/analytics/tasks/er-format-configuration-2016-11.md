--- 
title: Elektrooniline aruandlus. Vormingu konfiguratsiooni loomine (november 2016)
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad vormindada konfiguratsiooni elektroonilise aruandluse (ER) puhul."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 803ed4a1018d344f1b40fa1f2338fc066e784c3c
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="9f192-103">Elektrooniline aruandlus. Vormingu konfiguratsiooni loomine (november 2016)</span><span class="sxs-lookup"><span data-stu-id="9f192-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f192-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad vormindada konfiguratsiooni elektroonilise aruandluse (ER) puhul.</span><span class="sxs-lookup"><span data-stu-id="9f192-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="9f192-105">See vormingu konfiguratsioon määrab elektrooniliste dokumentide vormingu, mida maksete töötlemisel kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="9f192-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="9f192-106">Selles näites loote vormingu konfiguratsiooni näidisettevõtte Litware, Inc. jaoks. Nende etappide lõpuleviimiseks peate kõigepealt läbima etapid protseduuris Andmemudeli vastendamine valitud andmeallikatega.</span><span class="sxs-lookup"><span data-stu-id="9f192-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="9f192-107">Uue vormingu konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="9f192-107">Create a new format configuration</span></span>
1. <span data-ttu-id="9f192-108">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="9f192-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="9f192-109">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="9f192-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="9f192-110">Valige puul suvand Maksed (lihtsustatud mudel).</span><span class="sxs-lookup"><span data-stu-id="9f192-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="9f192-111">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="9f192-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="9f192-112">Sisestage väljale Uus suvand Andmemudelil PaymentModel põhinev vorming.</span><span class="sxs-lookup"><span data-stu-id="9f192-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="9f192-113">Sisestage väljale Nimi suvand BACS (UK fiktiivne).</span><span class="sxs-lookup"><span data-stu-id="9f192-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="9f192-114">BACS (UK fiktiivne)</span><span class="sxs-lookup"><span data-stu-id="9f192-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="9f192-115">Sisestage väljale Kirjeldus suvand BACS-i hankija maksevorming (UK fiktiivne).</span><span class="sxs-lookup"><span data-stu-id="9f192-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="9f192-116">BACS-i hankija maksevorming (UK fiktiivne)</span><span class="sxs-lookup"><span data-stu-id="9f192-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="9f192-117">Aktiivne konfiguratsiooni pakkuja sisestatakse siia automaatselt.</span><span class="sxs-lookup"><span data-stu-id="9f192-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="9f192-118">See pakkuja saab seda konfiguratsiooni hallata.</span><span class="sxs-lookup"><span data-stu-id="9f192-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="9f192-119">Muud pakkujad saavad seda konfiguratsiooni kasutada, kuid ei saa seda hallata.</span><span class="sxs-lookup"><span data-stu-id="9f192-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="9f192-120">Määratleda saab elektroonilise dokumendi kindla vormingu.</span><span class="sxs-lookup"><span data-stu-id="9f192-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="9f192-121">Jätke see väli tühjaks, kui soovite valida vormingu käitusajal.</span><span class="sxs-lookup"><span data-stu-id="9f192-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="9f192-122">Sisestage või valige väärtus väljal Andmemudeli definitsioon.</span><span class="sxs-lookup"><span data-stu-id="9f192-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="9f192-123">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="9f192-123">Click Create configuration.</span></span>
    * <span data-ttu-id="9f192-124">Uus konfiguratsioon on loodud.</span><span class="sxs-lookup"><span data-stu-id="9f192-124">A new configuration has been created.</span></span> <span data-ttu-id="9f192-125">Mustandversiooni saab kasutada vormingu kujunduse salvestamiseks elektrooniliste dokumentide haldamise puhul.</span><span class="sxs-lookup"><span data-stu-id="9f192-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="9f192-126">Elektroonilise dokumendi vormingu kujundus</span><span class="sxs-lookup"><span data-stu-id="9f192-126">Design format of electronic document</span></span>
1. <span data-ttu-id="9f192-127">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="9f192-127">Click Designer.</span></span>
2. <span data-ttu-id="9f192-128">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="9f192-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="9f192-129">Valige puul suvand Common\File.</span><span class="sxs-lookup"><span data-stu-id="9f192-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="9f192-130">Sisestage väljale Nimi suvand XML.</span><span class="sxs-lookup"><span data-stu-id="9f192-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="9f192-131">Xml</span><span class="sxs-lookup"><span data-stu-id="9f192-131">Xml</span></span>  
5. <span data-ttu-id="9f192-132">Sisestage väljale Kodeerimine suvand UTF-8.</span><span class="sxs-lookup"><span data-stu-id="9f192-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="9f192-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="9f192-133">UTF-8</span></span>  
6. <span data-ttu-id="9f192-134">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-134">Click OK.</span></span>
7. <span data-ttu-id="9f192-135">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="9f192-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="9f192-136">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="9f192-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="9f192-137">Sisestage väljale Nimi suvand Teade.</span><span class="sxs-lookup"><span data-stu-id="9f192-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="9f192-138">Teade</span><span class="sxs-lookup"><span data-stu-id="9f192-138">Message</span></span>  
10. <span data-ttu-id="9f192-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-139">Click OK.</span></span>
11. <span data-ttu-id="9f192-140">Puuvaates valige „Xml\Teade”</span><span class="sxs-lookup"><span data-stu-id="9f192-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="9f192-141">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="9f192-141">Click Add Element.</span></span>
13. <span data-ttu-id="9f192-142">Sisestage väljale Nimi suvand ProcessingDate.</span><span class="sxs-lookup"><span data-stu-id="9f192-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="9f192-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="9f192-143">ProcessingDate</span></span>  
14. <span data-ttu-id="9f192-144">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-144">Click OK.</span></span>
15. <span data-ttu-id="9f192-145">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="9f192-145">Click Add Element.</span></span>
16. <span data-ttu-id="9f192-146">Sisestage väljale Nimi suvand MessageId.</span><span class="sxs-lookup"><span data-stu-id="9f192-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="9f192-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="9f192-147">MessageId</span></span>  
17. <span data-ttu-id="9f192-148">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-148">Click OK.</span></span>
18. <span data-ttu-id="9f192-149">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="9f192-149">Click Add Element.</span></span>
19. <span data-ttu-id="9f192-150">Sisestage väljale Nimi suvand Maksed.</span><span class="sxs-lookup"><span data-stu-id="9f192-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="9f192-151">Maksed</span><span class="sxs-lookup"><span data-stu-id="9f192-151">Payments</span></span>  
20. <span data-ttu-id="9f192-152">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-152">Click OK.</span></span>
21. <span data-ttu-id="9f192-153">Puuvaates valige „Xml\Teade\Maksed”.</span><span class="sxs-lookup"><span data-stu-id="9f192-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="9f192-154">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="9f192-154">Click Add Element.</span></span>
23. <span data-ttu-id="9f192-155">Sisestage väljale Nimi suvand Kaup.</span><span class="sxs-lookup"><span data-stu-id="9f192-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="9f192-156">Kaup</span><span class="sxs-lookup"><span data-stu-id="9f192-156">Item</span></span>  
24. <span data-ttu-id="9f192-157">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-157">Click OK.</span></span>
25. <span data-ttu-id="9f192-158">Puuvaates valige „Xml\Teade\Maksed\Kaup”.</span><span class="sxs-lookup"><span data-stu-id="9f192-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="9f192-159">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="9f192-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="9f192-160">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="9f192-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="9f192-161">Sisestage väljale Nimi suvand Id.</span><span class="sxs-lookup"><span data-stu-id="9f192-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="9f192-162">ID</span><span class="sxs-lookup"><span data-stu-id="9f192-162">Id</span></span>  
29. <span data-ttu-id="9f192-163">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-163">Click OK.</span></span>
30. <span data-ttu-id="9f192-164">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="9f192-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="9f192-165">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="9f192-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="9f192-166">Sisestage väljale Nimi suvand Hankija.</span><span class="sxs-lookup"><span data-stu-id="9f192-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="9f192-167">Tarnija</span><span class="sxs-lookup"><span data-stu-id="9f192-167">Vendor</span></span>  
33. <span data-ttu-id="9f192-168">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-168">Click OK.</span></span>
34. <span data-ttu-id="9f192-169">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija”.</span><span class="sxs-lookup"><span data-stu-id="9f192-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="9f192-170">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="9f192-170">Click Add Element.</span></span>
36. <span data-ttu-id="9f192-171">Sisestage väljale Nimi suvand Nimi.</span><span class="sxs-lookup"><span data-stu-id="9f192-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="9f192-172">Nimi</span><span class="sxs-lookup"><span data-stu-id="9f192-172">Name</span></span>  
37. <span data-ttu-id="9f192-173">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-173">Click OK.</span></span>
38. <span data-ttu-id="9f192-174">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="9f192-174">Click Add Element.</span></span>
39. <span data-ttu-id="9f192-175">Sisestage väljale Nimi suvand Pank.</span><span class="sxs-lookup"><span data-stu-id="9f192-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="9f192-176">Pank</span><span class="sxs-lookup"><span data-stu-id="9f192-176">Bank</span></span>  
40. <span data-ttu-id="9f192-177">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-177">Click OK.</span></span>
41. <span data-ttu-id="9f192-178">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank”.</span><span class="sxs-lookup"><span data-stu-id="9f192-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="9f192-179">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="9f192-179">Click Add Element.</span></span>
43. <span data-ttu-id="9f192-180">Sisestage väljale Nimi suvand RoutingNumber.</span><span class="sxs-lookup"><span data-stu-id="9f192-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="9f192-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="9f192-181">RoutingNumber</span></span>  
44. <span data-ttu-id="9f192-182">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-182">Click OK.</span></span>
45. <span data-ttu-id="9f192-183">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="9f192-183">Click Add Element.</span></span>
46. <span data-ttu-id="9f192-184">Sisestage väljale Nimi suvand AccountNumber.</span><span class="sxs-lookup"><span data-stu-id="9f192-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="9f192-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="9f192-185">AccountNumber</span></span>  
47. <span data-ttu-id="9f192-186">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-186">Click OK.</span></span>
48. <span data-ttu-id="9f192-187">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija”.</span><span class="sxs-lookup"><span data-stu-id="9f192-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="9f192-188">Klõpsake käsku Kopeeri.</span><span class="sxs-lookup"><span data-stu-id="9f192-188">Click Copy.</span></span>
50. <span data-ttu-id="9f192-189">Puuvaates valige „Xml\Teade\Maksed\Kaup”.</span><span class="sxs-lookup"><span data-stu-id="9f192-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="9f192-190">Klõpsake käsku Kleebi.</span><span class="sxs-lookup"><span data-stu-id="9f192-190">Click Paste.</span></span>
52. <span data-ttu-id="9f192-191">Sisestage väljale Nimi suvand Maksja.</span><span class="sxs-lookup"><span data-stu-id="9f192-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="9f192-192">Maksja</span><span class="sxs-lookup"><span data-stu-id="9f192-192">Payer</span></span>  
53. <span data-ttu-id="9f192-193">Puuvaates valige „Xml\Teade\Maksed\Kaup”.</span><span class="sxs-lookup"><span data-stu-id="9f192-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="9f192-194">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="9f192-194">Click Add Element.</span></span>
55. <span data-ttu-id="9f192-195">Sisestage väljale Nimi suvand Valuuta.</span><span class="sxs-lookup"><span data-stu-id="9f192-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="9f192-196">Valuuta</span><span class="sxs-lookup"><span data-stu-id="9f192-196">Currency</span></span>  
56. <span data-ttu-id="9f192-197">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-197">Click OK.</span></span>
57. <span data-ttu-id="9f192-198">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="9f192-198">Click Add Element.</span></span>
58. <span data-ttu-id="9f192-199">Sisestage väljale Nimi suvand Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9f192-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="9f192-200">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="9f192-200">Description</span></span>  
59. <span data-ttu-id="9f192-201">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-201">Click OK.</span></span>
60. <span data-ttu-id="9f192-202">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="9f192-202">Click Add Element.</span></span>
61. <span data-ttu-id="9f192-203">Sisestage väljale Nimi suvand TransDate.</span><span class="sxs-lookup"><span data-stu-id="9f192-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="9f192-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="9f192-204">TransDate</span></span>  
62. <span data-ttu-id="9f192-205">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-205">Click OK.</span></span>
63. <span data-ttu-id="9f192-206">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="9f192-206">Click Add Element.</span></span>
64. <span data-ttu-id="9f192-207">Sisestage väljale Nimi suvand Summa.</span><span class="sxs-lookup"><span data-stu-id="9f192-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="9f192-208">Summa</span><span class="sxs-lookup"><span data-stu-id="9f192-208">Amount</span></span>  
65. <span data-ttu-id="9f192-209">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="9f192-210">Vormingu komponentide ettevalmistamine andmemudeli elementidega vastendamiseks</span><span class="sxs-lookup"><span data-stu-id="9f192-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="9f192-211">Puuvaates valige „Xml\Teade\ProcessingDate”.</span><span class="sxs-lookup"><span data-stu-id="9f192-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="9f192-212">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="9f192-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="9f192-213">Puuvaates valige „Tekst\DateTime”.</span><span class="sxs-lookup"><span data-stu-id="9f192-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="9f192-214">Sisestage väljale Vorming suvand aaaa-KK-pp.</span><span class="sxs-lookup"><span data-stu-id="9f192-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="9f192-215">aaaa-KK-pp</span><span class="sxs-lookup"><span data-stu-id="9f192-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="9f192-216">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-216">Click OK.</span></span>
6. <span data-ttu-id="9f192-217">Puuvaates valige „Xml\Teade\Maksed\Kaup\TransDate”</span><span class="sxs-lookup"><span data-stu-id="9f192-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="9f192-218">Klõpsake valikut Add DateTime.</span><span class="sxs-lookup"><span data-stu-id="9f192-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="9f192-219">Sisestage väljale Vorming suvand aaaa-KK-pp.</span><span class="sxs-lookup"><span data-stu-id="9f192-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="9f192-220">aaaa-KK-pp</span><span class="sxs-lookup"><span data-stu-id="9f192-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="9f192-221">Tüübi väljal DateTime valige „Kuupäev”.</span><span class="sxs-lookup"><span data-stu-id="9f192-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="9f192-222">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-222">Click OK.</span></span>
11. <span data-ttu-id="9f192-223">Puuvaates valige „Xml\Teade\MessageId”</span><span class="sxs-lookup"><span data-stu-id="9f192-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="9f192-224">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="9f192-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="9f192-225">Valige puul suvand Tekst\String.</span><span class="sxs-lookup"><span data-stu-id="9f192-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="9f192-226">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-226">Click OK.</span></span>
15. <span data-ttu-id="9f192-227">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Nimi”.</span><span class="sxs-lookup"><span data-stu-id="9f192-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="9f192-228">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="9f192-228">Click Add String.</span></span>
17. <span data-ttu-id="9f192-229">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-229">Click OK.</span></span>
18. <span data-ttu-id="9f192-230">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank\RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="9f192-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="9f192-231">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="9f192-231">Click Add String.</span></span>
20. <span data-ttu-id="9f192-232">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-232">Click OK.</span></span>
21. <span data-ttu-id="9f192-233">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank\AccountNumber”.</span><span class="sxs-lookup"><span data-stu-id="9f192-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="9f192-234">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="9f192-234">Click Add String.</span></span>
23. <span data-ttu-id="9f192-235">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-235">Click OK.</span></span>
24. <span data-ttu-id="9f192-236">Puuvaates valige „Xml\Teade\Maksed\Kaup\Maksed\Nimi”.</span><span class="sxs-lookup"><span data-stu-id="9f192-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="9f192-237">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="9f192-237">Click Add String.</span></span>
26. <span data-ttu-id="9f192-238">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-238">Click OK.</span></span>
27. <span data-ttu-id="9f192-239">Puuvaates valige „Xml\Teade\Maksed\Kaup\Maksja\Pank\RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="9f192-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="9f192-240">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="9f192-240">Click Add String.</span></span>
29. <span data-ttu-id="9f192-241">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-241">Click OK.</span></span>
30. <span data-ttu-id="9f192-242">Puuvaates valige „Xml\Teade\Maksed\Kaup\Maksja\Pank\AccountNumber”.</span><span class="sxs-lookup"><span data-stu-id="9f192-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="9f192-243">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="9f192-243">Click Add String.</span></span>
32. <span data-ttu-id="9f192-244">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-244">Click OK.</span></span>
33. <span data-ttu-id="9f192-245">Puuvaates valige „Xml\Teade\Maksed\Kaup\Valuuta”.</span><span class="sxs-lookup"><span data-stu-id="9f192-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="9f192-246">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="9f192-246">Click Add String.</span></span>
35. <span data-ttu-id="9f192-247">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-247">Click OK.</span></span>
36. <span data-ttu-id="9f192-248">Puuvaates valige „Xml\Teade\Maksed\Kaup\Kirjeldus”.</span><span class="sxs-lookup"><span data-stu-id="9f192-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="9f192-249">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="9f192-249">Click Add String.</span></span>
38. <span data-ttu-id="9f192-250">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-250">Click OK.</span></span>
39. <span data-ttu-id="9f192-251">Puuvaates valige „Xml\Teade\Maksed\Kaup\Summa”.</span><span class="sxs-lookup"><span data-stu-id="9f192-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="9f192-252">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="9f192-252">Click Add String.</span></span>
41. <span data-ttu-id="9f192-253">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9f192-253">Click OK.</span></span>
42. <span data-ttu-id="9f192-254">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9f192-254">Click Save.</span></span>
43. <span data-ttu-id="9f192-255">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9f192-255">Close the page.</span></span>


