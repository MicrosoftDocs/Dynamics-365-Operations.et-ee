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
ms.openlocfilehash: 77f1f2d6390a1d99b22d6eab9f0cae30f9760cc8
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550575"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="1d2aa-103">Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (3. osa – aruande koostamine)</span><span class="sxs-lookup"><span data-stu-id="1d2aa-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d2aa-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="1d2aa-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="1d2aa-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (2. osa: mudeli vastendamine).</span><span class="sxs-lookup"><span data-stu-id="1d2aa-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="1d2aa-107">Aruande koostamine finantsdimensioonide esitamiseks</span><span class="sxs-lookup"><span data-stu-id="1d2aa-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="1d2aa-108">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="1d2aa-109">Valige puult Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="1d2aa-110">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="1d2aa-111">Sisestage väljale Uus valik Vorming põhineb andmemudelil Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="1d2aa-112">Kasutage oma uue aruande andmeallikana eelnevalt loodud mudelit.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="1d2aa-113">Tippige väljale Nimi tekst Pearaamatu töölehe aruanne.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="1d2aa-114">Tehke väljal Andmemudeli definitsioon valik Kirje.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="1d2aa-115">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-115">Click Create configuration.</span></span>
8. <span data-ttu-id="1d2aa-116">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-116">Click Designer.</span></span>
9. <span data-ttu-id="1d2aa-117">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="1d2aa-118">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="1d2aa-119">Tippige Juur väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="1d2aa-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-120">Click OK.</span></span>
13. <span data-ttu-id="1d2aa-121">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="1d2aa-122">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="1d2aa-123">Sisestage väljale Nimi suvand Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="1d2aa-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-124">Click OK.</span></span>
17. <span data-ttu-id="1d2aa-125">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="1d2aa-126">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="1d2aa-127">Tippige Tööleht väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="1d2aa-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-128">Click OK.</span></span>
21. <span data-ttu-id="1d2aa-129">Valige puult Juur: XML-element \ Tööleht: XML-element.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="1d2aa-130">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="1d2aa-131">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="1d2aa-132">Tippige Partii väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="1d2aa-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-133">Click OK.</span></span>
26. <span data-ttu-id="1d2aa-134">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="1d2aa-135">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="1d2aa-136">Tippige väljale Nimi valik Kanne.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="1d2aa-137">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-137">Click OK.</span></span>
30. <span data-ttu-id="1d2aa-138">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="1d2aa-139">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="1d2aa-140">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="1d2aa-141">Tippige Kanne väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="1d2aa-142">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-142">Click OK.</span></span>
35. <span data-ttu-id="1d2aa-143">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="1d2aa-144">Tippige Kuupäev väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="1d2aa-145">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-145">Click OK.</span></span>
38. <span data-ttu-id="1d2aa-146">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="1d2aa-147">Sisestage väljale Nimi suvand Valuuta.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="1d2aa-148">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-148">Click OK.</span></span>
41. <span data-ttu-id="1d2aa-149">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="1d2aa-150">Tippige Dt väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="1d2aa-151">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-151">Click OK.</span></span>
44. <span data-ttu-id="1d2aa-152">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="1d2aa-153">Tippige Ct väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="1d2aa-154">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-154">Click OK.</span></span>
47. <span data-ttu-id="1d2aa-155">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="1d2aa-156">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="1d2aa-157">Tippige Dimensioonid väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="1d2aa-158">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-158">Click OK.</span></span>
51. <span data-ttu-id="1d2aa-159">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="1d2aa-160">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="1d2aa-161">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="1d2aa-162">Tippige Kood väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="1d2aa-163">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-163">Click OK.</span></span>
56. <span data-ttu-id="1d2aa-164">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="1d2aa-165">Tippige Väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="1d2aa-166">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-166">Click OK.</span></span>
59. <span data-ttu-id="1d2aa-167">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="1d2aa-168">Tippige Desc väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="1d2aa-169">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="1d2aa-170">Aruande elementide vastendamine andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="1d2aa-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="1d2aa-171">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="1d2aa-172">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="1d2aa-173">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="1d2aa-174">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="1d2aa-175">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="1d2aa-176">Valige puult Juur: XM-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Desc: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="1d2aa-177">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Kirjeldus: string.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="1d2aa-178">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-178">Click Bind.</span></span>
9. <span data-ttu-id="1d2aa-179">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Väärtus: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="1d2aa-180">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Kood: string.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="1d2aa-181">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-181">Click Bind.</span></span>
12. <span data-ttu-id="1d2aa-182">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Kood: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="1d2aa-183">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Nimi: string.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="1d2aa-184">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-184">Click Bind.</span></span>
15. <span data-ttu-id="1d2aa-185">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="1d2aa-186">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="1d2aa-187">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-187">Click Bind.</span></span>
18. <span data-ttu-id="1d2aa-188">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Ct: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="1d2aa-189">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kreedit: tegelik.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="1d2aa-190">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-190">Click Bind.</span></span>
21. <span data-ttu-id="1d2aa-191">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dt: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="1d2aa-192">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Deebet: tegelik.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="1d2aa-193">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-193">Click Bind.</span></span>
24. <span data-ttu-id="1d2aa-194">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Valuuta: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="1d2aa-195">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Valuuta: string.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="1d2aa-196">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-196">Click Bind.</span></span>
27. <span data-ttu-id="1d2aa-197">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Kuupäev: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="1d2aa-198">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kuupäev: kuupäev.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="1d2aa-199">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-199">Click Bind.</span></span>
30. <span data-ttu-id="1d2aa-200">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Kanne: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="1d2aa-201">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kanne: string.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="1d2aa-202">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-202">Click Bind.</span></span>
33. <span data-ttu-id="1d2aa-203">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="1d2aa-204">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="1d2aa-205">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-205">Click Bind.</span></span>
36. <span data-ttu-id="1d2aa-206">Valige puult Juur: XML-element \ Tööleht: XML-element \ Partii: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="1d2aa-207">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Partii: string.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="1d2aa-208">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-208">Click Bind.</span></span>
39. <span data-ttu-id="1d2aa-209">Valige puult Juur: XML-element \ Tööleht: XML-element.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="1d2aa-210">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="1d2aa-211">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-211">Click Bind.</span></span>
42. <span data-ttu-id="1d2aa-212">Valige puult Juur: XML-element \ Ettevõte: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="1d2aa-213">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Ettevõte: string.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="1d2aa-214">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-214">Click Bind.</span></span>
45. <span data-ttu-id="1d2aa-215">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-215">Click Save.</span></span>
46. <span data-ttu-id="1d2aa-216">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1d2aa-216">Close the page.</span></span>

