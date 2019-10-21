---
title: Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (3. osa – aruande koostamine)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 29dcf008f342603615241ab75860893cadc2b69e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182435"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3-design-the-report"></a><span data-ttu-id="2a68a-103">Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (3. osa: aruande koostamine)</span><span class="sxs-lookup"><span data-stu-id="2a68a-103">ER Use financial dimensions as a data source (Part 3: Design the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2a68a-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="2a68a-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="2a68a-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="2a68a-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="2a68a-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (2. osa: mudeli vastendamine).</span><span class="sxs-lookup"><span data-stu-id="2a68a-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="2a68a-107">Aruande koostamine finantsdimensioonide esitamiseks</span><span class="sxs-lookup"><span data-stu-id="2a68a-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="2a68a-108">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="2a68a-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="2a68a-109">Valige puult Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="2a68a-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="2a68a-110">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="2a68a-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="2a68a-111">Sisestage väljale Uus valik Vorming põhineb andmemudelil Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="2a68a-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="2a68a-112">Kasutage oma uue aruande andmeallikana eelnevalt loodud mudelit.</span><span class="sxs-lookup"><span data-stu-id="2a68a-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="2a68a-113">Tippige väljale Nimi tekst Pearaamatu töölehe aruanne.</span><span class="sxs-lookup"><span data-stu-id="2a68a-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="2a68a-114">Tehke väljal Andmemudeli definitsioon valik Kirje.</span><span class="sxs-lookup"><span data-stu-id="2a68a-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="2a68a-115">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="2a68a-115">Click Create configuration.</span></span>
8. <span data-ttu-id="2a68a-116">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="2a68a-116">Click Designer.</span></span>
9. <span data-ttu-id="2a68a-117">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="2a68a-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="2a68a-118">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="2a68a-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="2a68a-119">Tippige Juur väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="2a68a-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="2a68a-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2a68a-120">Click OK.</span></span>
13. <span data-ttu-id="2a68a-121">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="2a68a-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="2a68a-122">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="2a68a-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="2a68a-123">Sisestage väljale Nimi suvand Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="2a68a-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="2a68a-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2a68a-124">Click OK.</span></span>
17. <span data-ttu-id="2a68a-125">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="2a68a-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="2a68a-126">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="2a68a-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="2a68a-127">Tippige Tööleht väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="2a68a-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="2a68a-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2a68a-128">Click OK.</span></span>
21. <span data-ttu-id="2a68a-129">Valige puult Juur: XML-element \ Tööleht: XML-element.</span><span class="sxs-lookup"><span data-stu-id="2a68a-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="2a68a-130">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="2a68a-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="2a68a-131">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="2a68a-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="2a68a-132">Tippige Partii väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="2a68a-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="2a68a-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2a68a-133">Click OK.</span></span>
26. <span data-ttu-id="2a68a-134">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="2a68a-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="2a68a-135">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="2a68a-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="2a68a-136">Tippige väljale Nimi valik Kanne.</span><span class="sxs-lookup"><span data-stu-id="2a68a-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="2a68a-137">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2a68a-137">Click OK.</span></span>
30. <span data-ttu-id="2a68a-138">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element.</span><span class="sxs-lookup"><span data-stu-id="2a68a-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="2a68a-139">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="2a68a-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="2a68a-140">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="2a68a-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="2a68a-141">Tippige Kanne väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="2a68a-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="2a68a-142">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2a68a-142">Click OK.</span></span>
35. <span data-ttu-id="2a68a-143">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="2a68a-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="2a68a-144">Tippige Kuupäev väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="2a68a-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="2a68a-145">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2a68a-145">Click OK.</span></span>
38. <span data-ttu-id="2a68a-146">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="2a68a-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="2a68a-147">Sisestage väljale Nimi suvand Valuuta.</span><span class="sxs-lookup"><span data-stu-id="2a68a-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="2a68a-148">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2a68a-148">Click OK.</span></span>
41. <span data-ttu-id="2a68a-149">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="2a68a-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="2a68a-150">Tippige Dt väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="2a68a-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="2a68a-151">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2a68a-151">Click OK.</span></span>
44. <span data-ttu-id="2a68a-152">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="2a68a-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="2a68a-153">Tippige Ct väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="2a68a-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="2a68a-154">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2a68a-154">Click OK.</span></span>
47. <span data-ttu-id="2a68a-155">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="2a68a-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="2a68a-156">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="2a68a-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="2a68a-157">Tippige Dimensioonid väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="2a68a-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="2a68a-158">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2a68a-158">Click OK.</span></span>
51. <span data-ttu-id="2a68a-159">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element.</span><span class="sxs-lookup"><span data-stu-id="2a68a-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="2a68a-160">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="2a68a-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="2a68a-161">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="2a68a-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="2a68a-162">Tippige Kood väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="2a68a-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="2a68a-163">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2a68a-163">Click OK.</span></span>
56. <span data-ttu-id="2a68a-164">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="2a68a-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="2a68a-165">Tippige Väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="2a68a-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="2a68a-166">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2a68a-166">Click OK.</span></span>
59. <span data-ttu-id="2a68a-167">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="2a68a-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="2a68a-168">Tippige Desc väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="2a68a-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="2a68a-169">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2a68a-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="2a68a-170">Aruande elementide vastendamine andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="2a68a-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="2a68a-171">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="2a68a-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="2a68a-172">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="2a68a-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="2a68a-173">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="2a68a-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="2a68a-174">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="2a68a-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="2a68a-175">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="2a68a-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="2a68a-176">Valige puult Juur: XM-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Desc: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="2a68a-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="2a68a-177">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Kirjeldus: string.</span><span class="sxs-lookup"><span data-stu-id="2a68a-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="2a68a-178">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="2a68a-178">Click Bind.</span></span>
9. <span data-ttu-id="2a68a-179">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Väärtus: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="2a68a-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="2a68a-180">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Kood: string.</span><span class="sxs-lookup"><span data-stu-id="2a68a-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="2a68a-181">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="2a68a-181">Click Bind.</span></span>
12. <span data-ttu-id="2a68a-182">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Kood: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="2a68a-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="2a68a-183">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Nimi: string.</span><span class="sxs-lookup"><span data-stu-id="2a68a-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="2a68a-184">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="2a68a-184">Click Bind.</span></span>
15. <span data-ttu-id="2a68a-185">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="2a68a-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="2a68a-186">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element.</span><span class="sxs-lookup"><span data-stu-id="2a68a-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="2a68a-187">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="2a68a-187">Click Bind.</span></span>
18. <span data-ttu-id="2a68a-188">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Ct: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="2a68a-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="2a68a-189">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kreedit: tegelik.</span><span class="sxs-lookup"><span data-stu-id="2a68a-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="2a68a-190">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="2a68a-190">Click Bind.</span></span>
21. <span data-ttu-id="2a68a-191">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dt: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="2a68a-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="2a68a-192">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Deebet: tegelik.</span><span class="sxs-lookup"><span data-stu-id="2a68a-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="2a68a-193">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="2a68a-193">Click Bind.</span></span>
24. <span data-ttu-id="2a68a-194">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Valuuta: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="2a68a-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="2a68a-195">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Valuuta: string.</span><span class="sxs-lookup"><span data-stu-id="2a68a-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="2a68a-196">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="2a68a-196">Click Bind.</span></span>
27. <span data-ttu-id="2a68a-197">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Kuupäev: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="2a68a-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="2a68a-198">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kuupäev: kuupäev.</span><span class="sxs-lookup"><span data-stu-id="2a68a-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="2a68a-199">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="2a68a-199">Click Bind.</span></span>
30. <span data-ttu-id="2a68a-200">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Kanne: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="2a68a-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="2a68a-201">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kanne: string.</span><span class="sxs-lookup"><span data-stu-id="2a68a-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="2a68a-202">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="2a68a-202">Click Bind.</span></span>
33. <span data-ttu-id="2a68a-203">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element.</span><span class="sxs-lookup"><span data-stu-id="2a68a-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="2a68a-204">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="2a68a-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="2a68a-205">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="2a68a-205">Click Bind.</span></span>
36. <span data-ttu-id="2a68a-206">Valige puult Juur: XML-element \ Tööleht: XML-element \ Partii: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="2a68a-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="2a68a-207">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Partii: string.</span><span class="sxs-lookup"><span data-stu-id="2a68a-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="2a68a-208">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="2a68a-208">Click Bind.</span></span>
39. <span data-ttu-id="2a68a-209">Valige puult Juur: XML-element \ Tööleht: XML-element.</span><span class="sxs-lookup"><span data-stu-id="2a68a-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="2a68a-210">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="2a68a-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="2a68a-211">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="2a68a-211">Click Bind.</span></span>
42. <span data-ttu-id="2a68a-212">Valige puult Juur: XML-element \ Ettevõte: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="2a68a-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="2a68a-213">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Ettevõte: string.</span><span class="sxs-lookup"><span data-stu-id="2a68a-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="2a68a-214">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="2a68a-214">Click Bind.</span></span>
45. <span data-ttu-id="2a68a-215">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2a68a-215">Click Save.</span></span>
46. <span data-ttu-id="2a68a-216">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2a68a-216">Close the page.</span></span>

