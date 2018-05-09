--- 
title: Elektroonilise aruandluse (ER) vormingukonfiguratsiooni loomine
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad vormindada konfiguratsiooni elektroonilise aruandluse (ER) puhul."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 46c55fe11af3f8a698b55bb80b95d3d14c185c20
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="15c4a-103">Elektroonilise aruandluse (ER) vormingukonfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="15c4a-103">Create a format configuration for electronic reporting (ER)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="15c4a-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad vormindada konfiguratsiooni elektroonilise aruandluse (ER) puhul.</span><span class="sxs-lookup"><span data-stu-id="15c4a-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="15c4a-105">See vormingu konfiguratsioon määrab elektrooniliste dokumentide vormingu, mida maksete töötlemisel kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="15c4a-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="15c4a-106">Selles näites loote vormingu konfiguratsiooni näidisettevõtte Litware, Inc. jaoks. Nende etappide lõpuleviimiseks peate kõigepealt läbima etapid protseduuris Andmemudeli vastendamine valitud andmeallikatega.</span><span class="sxs-lookup"><span data-stu-id="15c4a-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="15c4a-107">Uue vormingu konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="15c4a-107">Create a new format configuration</span></span>
1. <span data-ttu-id="15c4a-108">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="15c4a-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="15c4a-109">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="15c4a-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="15c4a-110">Valige puul suvand Maksed (lihtsustatud mudel).</span><span class="sxs-lookup"><span data-stu-id="15c4a-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="15c4a-111">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="15c4a-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="15c4a-112">Sisestage väljale Uus suvand Andmemudelil PaymentModel põhinev vorming.</span><span class="sxs-lookup"><span data-stu-id="15c4a-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="15c4a-113">Sisestage väljale Nimi suvand BACS (UK fiktiivne).</span><span class="sxs-lookup"><span data-stu-id="15c4a-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="15c4a-114">BACS (UK fiktiivne)</span><span class="sxs-lookup"><span data-stu-id="15c4a-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="15c4a-115">Sisestage väljale Kirjeldus suvand BACS-i hankija maksevorming (UK fiktiivne).</span><span class="sxs-lookup"><span data-stu-id="15c4a-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="15c4a-116">BACS-i hankija maksevorming (UK fiktiivne)</span><span class="sxs-lookup"><span data-stu-id="15c4a-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="15c4a-117">Aktiivne konfiguratsiooni pakkuja sisestatakse siia automaatselt.</span><span class="sxs-lookup"><span data-stu-id="15c4a-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="15c4a-118">See pakkuja saab seda konfiguratsiooni hallata.</span><span class="sxs-lookup"><span data-stu-id="15c4a-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="15c4a-119">Muud pakkujad saavad seda konfiguratsiooni kasutada, kuid ei saa seda hallata.</span><span class="sxs-lookup"><span data-stu-id="15c4a-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="15c4a-120">Määratleda saab elektroonilise dokumendi kindla vormingu.</span><span class="sxs-lookup"><span data-stu-id="15c4a-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="15c4a-121">Jätke see väli tühjaks, kui soovite valida vormingu käitusajal.</span><span class="sxs-lookup"><span data-stu-id="15c4a-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="15c4a-122">Sisestage või valige väärtus väljal Andmemudeli definitsioon.</span><span class="sxs-lookup"><span data-stu-id="15c4a-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="15c4a-123">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="15c4a-123">Click Create configuration.</span></span>
    * <span data-ttu-id="15c4a-124">Uus konfiguratsioon on loodud.</span><span class="sxs-lookup"><span data-stu-id="15c4a-124">A new configuration has been created.</span></span> <span data-ttu-id="15c4a-125">Mustandversiooni saab kasutada vormingu kujunduse salvestamiseks elektrooniliste dokumentide haldamise puhul.</span><span class="sxs-lookup"><span data-stu-id="15c4a-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="15c4a-126">Elektroonilise dokumendi vormingu kujundus</span><span class="sxs-lookup"><span data-stu-id="15c4a-126">Design format of electronic document</span></span>
1. <span data-ttu-id="15c4a-127">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="15c4a-127">Click Designer.</span></span>
2. <span data-ttu-id="15c4a-128">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="15c4a-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="15c4a-129">Valige puul suvand Common\File.</span><span class="sxs-lookup"><span data-stu-id="15c4a-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="15c4a-130">Sisestage väljale Nimi suvand XML.</span><span class="sxs-lookup"><span data-stu-id="15c4a-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="15c4a-131">Xml</span><span class="sxs-lookup"><span data-stu-id="15c4a-131">Xml</span></span>  
5. <span data-ttu-id="15c4a-132">Sisestage väljale Kodeerimine suvand UTF-8.</span><span class="sxs-lookup"><span data-stu-id="15c4a-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="15c4a-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="15c4a-133">UTF-8</span></span>  
6. <span data-ttu-id="15c4a-134">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-134">Click OK.</span></span>
7. <span data-ttu-id="15c4a-135">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="15c4a-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="15c4a-136">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="15c4a-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="15c4a-137">Sisestage väljale Nimi suvand Teade.</span><span class="sxs-lookup"><span data-stu-id="15c4a-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="15c4a-138">Teade</span><span class="sxs-lookup"><span data-stu-id="15c4a-138">Message</span></span>  
10. <span data-ttu-id="15c4a-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-139">Click OK.</span></span>
11. <span data-ttu-id="15c4a-140">Puuvaates valige „Xml\Teade”</span><span class="sxs-lookup"><span data-stu-id="15c4a-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="15c4a-141">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="15c4a-141">Click Add Element.</span></span>
13. <span data-ttu-id="15c4a-142">Sisestage väljale Nimi suvand ProcessingDate.</span><span class="sxs-lookup"><span data-stu-id="15c4a-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="15c4a-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="15c4a-143">ProcessingDate</span></span>  
14. <span data-ttu-id="15c4a-144">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-144">Click OK.</span></span>
15. <span data-ttu-id="15c4a-145">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="15c4a-145">Click Add Element.</span></span>
16. <span data-ttu-id="15c4a-146">Sisestage väljale Nimi suvand MessageId.</span><span class="sxs-lookup"><span data-stu-id="15c4a-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="15c4a-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="15c4a-147">MessageId</span></span>  
17. <span data-ttu-id="15c4a-148">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-148">Click OK.</span></span>
18. <span data-ttu-id="15c4a-149">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="15c4a-149">Click Add Element.</span></span>
19. <span data-ttu-id="15c4a-150">Sisestage väljale Nimi suvand Maksed.</span><span class="sxs-lookup"><span data-stu-id="15c4a-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="15c4a-151">Maksed</span><span class="sxs-lookup"><span data-stu-id="15c4a-151">Payments</span></span>  
20. <span data-ttu-id="15c4a-152">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-152">Click OK.</span></span>
21. <span data-ttu-id="15c4a-153">Puuvaates valige „Xml\Teade\Maksed”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="15c4a-154">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="15c4a-154">Click Add Element.</span></span>
23. <span data-ttu-id="15c4a-155">Sisestage väljale Nimi suvand Kaup.</span><span class="sxs-lookup"><span data-stu-id="15c4a-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="15c4a-156">Kaup</span><span class="sxs-lookup"><span data-stu-id="15c4a-156">Item</span></span>  
24. <span data-ttu-id="15c4a-157">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-157">Click OK.</span></span>
25. <span data-ttu-id="15c4a-158">Puuvaates valige „Xml\Teade\Maksed\Kaup”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="15c4a-159">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="15c4a-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="15c4a-160">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="15c4a-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="15c4a-161">Sisestage väljale Nimi suvand Id.</span><span class="sxs-lookup"><span data-stu-id="15c4a-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="15c4a-162">ID</span><span class="sxs-lookup"><span data-stu-id="15c4a-162">Id</span></span>  
29. <span data-ttu-id="15c4a-163">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-163">Click OK.</span></span>
30. <span data-ttu-id="15c4a-164">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="15c4a-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="15c4a-165">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="15c4a-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="15c4a-166">Sisestage väljale Nimi suvand Hankija.</span><span class="sxs-lookup"><span data-stu-id="15c4a-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="15c4a-167">Tarnija</span><span class="sxs-lookup"><span data-stu-id="15c4a-167">Vendor</span></span>  
33. <span data-ttu-id="15c4a-168">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-168">Click OK.</span></span>
34. <span data-ttu-id="15c4a-169">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="15c4a-170">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="15c4a-170">Click Add Element.</span></span>
36. <span data-ttu-id="15c4a-171">Sisestage väljale Nimi suvand Nimi.</span><span class="sxs-lookup"><span data-stu-id="15c4a-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="15c4a-172">Nimi</span><span class="sxs-lookup"><span data-stu-id="15c4a-172">Name</span></span>  
37. <span data-ttu-id="15c4a-173">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-173">Click OK.</span></span>
38. <span data-ttu-id="15c4a-174">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="15c4a-174">Click Add Element.</span></span>
39. <span data-ttu-id="15c4a-175">Sisestage väljale Nimi suvand Pank.</span><span class="sxs-lookup"><span data-stu-id="15c4a-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="15c4a-176">Pank</span><span class="sxs-lookup"><span data-stu-id="15c4a-176">Bank</span></span>  
40. <span data-ttu-id="15c4a-177">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-177">Click OK.</span></span>
41. <span data-ttu-id="15c4a-178">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="15c4a-179">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="15c4a-179">Click Add Element.</span></span>
43. <span data-ttu-id="15c4a-180">Sisestage väljale Nimi suvand RoutingNumber.</span><span class="sxs-lookup"><span data-stu-id="15c4a-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="15c4a-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="15c4a-181">RoutingNumber</span></span>  
44. <span data-ttu-id="15c4a-182">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-182">Click OK.</span></span>
45. <span data-ttu-id="15c4a-183">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="15c4a-183">Click Add Element.</span></span>
46. <span data-ttu-id="15c4a-184">Sisestage väljale Nimi suvand AccountNumber.</span><span class="sxs-lookup"><span data-stu-id="15c4a-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="15c4a-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="15c4a-185">AccountNumber</span></span>  
47. <span data-ttu-id="15c4a-186">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-186">Click OK.</span></span>
48. <span data-ttu-id="15c4a-187">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="15c4a-188">Klõpsake käsku Kopeeri.</span><span class="sxs-lookup"><span data-stu-id="15c4a-188">Click Copy.</span></span>
50. <span data-ttu-id="15c4a-189">Puuvaates valige „Xml\Teade\Maksed\Kaup”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="15c4a-190">Klõpsake käsku Kleebi.</span><span class="sxs-lookup"><span data-stu-id="15c4a-190">Click Paste.</span></span>
52. <span data-ttu-id="15c4a-191">Sisestage väljale Nimi suvand Maksja.</span><span class="sxs-lookup"><span data-stu-id="15c4a-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="15c4a-192">Maksja</span><span class="sxs-lookup"><span data-stu-id="15c4a-192">Payer</span></span>  
53. <span data-ttu-id="15c4a-193">Puuvaates valige „Xml\Teade\Maksed\Kaup”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="15c4a-194">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="15c4a-194">Click Add Element.</span></span>
55. <span data-ttu-id="15c4a-195">Sisestage väljale Nimi suvand Valuuta.</span><span class="sxs-lookup"><span data-stu-id="15c4a-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="15c4a-196">Valuuta</span><span class="sxs-lookup"><span data-stu-id="15c4a-196">Currency</span></span>  
56. <span data-ttu-id="15c4a-197">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-197">Click OK.</span></span>
57. <span data-ttu-id="15c4a-198">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="15c4a-198">Click Add Element.</span></span>
58. <span data-ttu-id="15c4a-199">Sisestage väljale Nimi suvand Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="15c4a-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="15c4a-200">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="15c4a-200">Description</span></span>  
59. <span data-ttu-id="15c4a-201">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-201">Click OK.</span></span>
60. <span data-ttu-id="15c4a-202">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="15c4a-202">Click Add Element.</span></span>
61. <span data-ttu-id="15c4a-203">Sisestage väljale Nimi suvand TransDate.</span><span class="sxs-lookup"><span data-stu-id="15c4a-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="15c4a-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="15c4a-204">TransDate</span></span>  
62. <span data-ttu-id="15c4a-205">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-205">Click OK.</span></span>
63. <span data-ttu-id="15c4a-206">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="15c4a-206">Click Add Element.</span></span>
64. <span data-ttu-id="15c4a-207">Sisestage väljale Nimi suvand Summa.</span><span class="sxs-lookup"><span data-stu-id="15c4a-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="15c4a-208">Summa</span><span class="sxs-lookup"><span data-stu-id="15c4a-208">Amount</span></span>  
65. <span data-ttu-id="15c4a-209">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="15c4a-210">Vormingu komponentide ettevalmistamine andmemudeli elementidega vastendamiseks</span><span class="sxs-lookup"><span data-stu-id="15c4a-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="15c4a-211">Puuvaates valige „Xml\Teade\ProcessingDate”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="15c4a-212">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="15c4a-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="15c4a-213">Puuvaates valige „Tekst\DateTime”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="15c4a-214">Sisestage väljale Vorming suvand aaaa-KK-pp.</span><span class="sxs-lookup"><span data-stu-id="15c4a-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="15c4a-215">aaaa-KK-pp</span><span class="sxs-lookup"><span data-stu-id="15c4a-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="15c4a-216">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-216">Click OK.</span></span>
6. <span data-ttu-id="15c4a-217">Puuvaates valige „Xml\Teade\Maksed\Kaup\TransDate”</span><span class="sxs-lookup"><span data-stu-id="15c4a-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="15c4a-218">Klõpsake valikut Add DateTime.</span><span class="sxs-lookup"><span data-stu-id="15c4a-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="15c4a-219">Sisestage väljale Vorming suvand aaaa-KK-pp.</span><span class="sxs-lookup"><span data-stu-id="15c4a-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="15c4a-220">aaaa-KK-pp</span><span class="sxs-lookup"><span data-stu-id="15c4a-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="15c4a-221">Tüübi väljal DateTime valige „Kuupäev”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="15c4a-222">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-222">Click OK.</span></span>
11. <span data-ttu-id="15c4a-223">Puuvaates valige „Xml\Teade\MessageId”</span><span class="sxs-lookup"><span data-stu-id="15c4a-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="15c4a-224">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="15c4a-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="15c4a-225">Valige puul suvand Tekst\String.</span><span class="sxs-lookup"><span data-stu-id="15c4a-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="15c4a-226">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-226">Click OK.</span></span>
15. <span data-ttu-id="15c4a-227">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Nimi”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="15c4a-228">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="15c4a-228">Click Add String.</span></span>
17. <span data-ttu-id="15c4a-229">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-229">Click OK.</span></span>
18. <span data-ttu-id="15c4a-230">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank\RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="15c4a-231">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="15c4a-231">Click Add String.</span></span>
20. <span data-ttu-id="15c4a-232">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-232">Click OK.</span></span>
21. <span data-ttu-id="15c4a-233">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank\AccountNumber”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="15c4a-234">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="15c4a-234">Click Add String.</span></span>
23. <span data-ttu-id="15c4a-235">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-235">Click OK.</span></span>
24. <span data-ttu-id="15c4a-236">Puuvaates valige „Xml\Teade\Maksed\Kaup\Maksed\Nimi”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="15c4a-237">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="15c4a-237">Click Add String.</span></span>
26. <span data-ttu-id="15c4a-238">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-238">Click OK.</span></span>
27. <span data-ttu-id="15c4a-239">Puuvaates valige „Xml\Teade\Maksed\Kaup\Maksja\Pank\RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="15c4a-240">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="15c4a-240">Click Add String.</span></span>
29. <span data-ttu-id="15c4a-241">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-241">Click OK.</span></span>
30. <span data-ttu-id="15c4a-242">Puuvaates valige „Xml\Teade\Maksed\Kaup\Maksja\Pank\AccountNumber”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="15c4a-243">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="15c4a-243">Click Add String.</span></span>
32. <span data-ttu-id="15c4a-244">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-244">Click OK.</span></span>
33. <span data-ttu-id="15c4a-245">Puuvaates valige „Xml\Teade\Maksed\Kaup\Valuuta”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="15c4a-246">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="15c4a-246">Click Add String.</span></span>
35. <span data-ttu-id="15c4a-247">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-247">Click OK.</span></span>
36. <span data-ttu-id="15c4a-248">Puuvaates valige „Xml\Teade\Maksed\Kaup\Kirjeldus”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="15c4a-249">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="15c4a-249">Click Add String.</span></span>
38. <span data-ttu-id="15c4a-250">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-250">Click OK.</span></span>
39. <span data-ttu-id="15c4a-251">Puuvaates valige „Xml\Teade\Maksed\Kaup\Summa”.</span><span class="sxs-lookup"><span data-stu-id="15c4a-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="15c4a-252">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="15c4a-252">Click Add String.</span></span>
41. <span data-ttu-id="15c4a-253">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15c4a-253">Click OK.</span></span>
42. <span data-ttu-id="15c4a-254">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="15c4a-254">Click Save.</span></span>
43. <span data-ttu-id="15c4a-255">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="15c4a-255">Close the page.</span></span>


