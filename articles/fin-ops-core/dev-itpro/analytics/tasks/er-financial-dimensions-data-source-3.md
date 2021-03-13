---
title: Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (3. osa – aruande koostamine)
description: Selles teemas kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse (ER) mudelit kasutama finantsdimensioone andmeallikana ER-i aruannetele. (3. osa)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0d6da96850e04d5e975b3febbfae2737c8a86af
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092296"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="d5fbc-104">Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (3. osa – aruande koostamine)</span><span class="sxs-lookup"><span data-stu-id="d5fbc-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d5fbc-105">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="d5fbc-106">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="d5fbc-107">Nende etappide lõpule viimiseks peate esmalt viima lõpule etapid protseduuris „Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (2. osa: mudeli vastendamine)”.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="d5fbc-108">Aruande koostamine finantsdimensioonide esitamiseks</span><span class="sxs-lookup"><span data-stu-id="d5fbc-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="d5fbc-109">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d5fbc-110">Valige puult Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="d5fbc-111">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="d5fbc-112">Sisestage väljale Uus valik Vorming põhineb andmemudelil Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="d5fbc-113">Kasutage oma uue aruande andmeallikana eelnevalt loodud mudelit.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="d5fbc-114">Tippige väljale Nimi tekst Pearaamatu töölehe aruanne.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="d5fbc-115">Tehke väljal Andmemudeli definitsioon valik Kirje.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="d5fbc-116">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-116">Click Create configuration.</span></span>
8. <span data-ttu-id="d5fbc-117">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-117">Click Designer.</span></span>
9. <span data-ttu-id="d5fbc-118">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="d5fbc-119">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="d5fbc-120">Tippige Juur väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="d5fbc-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-121">Click OK.</span></span>
13. <span data-ttu-id="d5fbc-122">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="d5fbc-123">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="d5fbc-124">Sisestage väljale Nimi suvand Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="d5fbc-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-125">Click OK.</span></span>
17. <span data-ttu-id="d5fbc-126">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="d5fbc-127">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="d5fbc-128">Tippige Tööleht väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="d5fbc-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-129">Click OK.</span></span>
21. <span data-ttu-id="d5fbc-130">Valige puult Juur: XML-element \ Tööleht: XML-element.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="d5fbc-131">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="d5fbc-132">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="d5fbc-133">Tippige Partii väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="d5fbc-134">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-134">Click OK.</span></span>
26. <span data-ttu-id="d5fbc-135">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="d5fbc-136">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="d5fbc-137">Tippige väljale Nimi valik Kanne.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="d5fbc-138">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-138">Click OK.</span></span>
30. <span data-ttu-id="d5fbc-139">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="d5fbc-140">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="d5fbc-141">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="d5fbc-142">Tippige Kanne väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="d5fbc-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-143">Click OK.</span></span>
35. <span data-ttu-id="d5fbc-144">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="d5fbc-145">Tippige Kuupäev väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="d5fbc-146">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-146">Click OK.</span></span>
38. <span data-ttu-id="d5fbc-147">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="d5fbc-148">Sisestage väljale Nimi suvand Valuuta.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="d5fbc-149">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-149">Click OK.</span></span>
41. <span data-ttu-id="d5fbc-150">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="d5fbc-151">Tippige Dt väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="d5fbc-152">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-152">Click OK.</span></span>
44. <span data-ttu-id="d5fbc-153">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="d5fbc-154">Tippige Ct väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="d5fbc-155">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-155">Click OK.</span></span>
47. <span data-ttu-id="d5fbc-156">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="d5fbc-157">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="d5fbc-158">Tippige Dimensioonid väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="d5fbc-159">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-159">Click OK.</span></span>
51. <span data-ttu-id="d5fbc-160">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="d5fbc-161">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="d5fbc-162">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="d5fbc-163">Tippige Kood väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="d5fbc-164">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-164">Click OK.</span></span>
56. <span data-ttu-id="d5fbc-165">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="d5fbc-166">Tippige Väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="d5fbc-167">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-167">Click OK.</span></span>
59. <span data-ttu-id="d5fbc-168">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="d5fbc-169">Tippige Desc väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="d5fbc-170">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-170">Click OK.</span></span>
<span data-ttu-id="d5fbc-171">![ER-i toimingute koostaja leht](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="d5fbc-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="d5fbc-172">Aruande elementide vastendamine andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="d5fbc-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="d5fbc-173">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="d5fbc-174">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="d5fbc-175">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="d5fbc-176">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="d5fbc-177">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="d5fbc-178">Valige puult Juur: XM-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Desc: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="d5fbc-179">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Kirjeldus: string.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="d5fbc-180">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-180">Click Bind.</span></span>
9. <span data-ttu-id="d5fbc-181">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Väärtus: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="d5fbc-182">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Kood: string.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="d5fbc-183">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-183">Click Bind.</span></span>
12. <span data-ttu-id="d5fbc-184">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Kood: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="d5fbc-185">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Nimi: string.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="d5fbc-186">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-186">Click Bind.</span></span>
15. <span data-ttu-id="d5fbc-187">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="d5fbc-188">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="d5fbc-189">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-189">Click Bind.</span></span>
18. <span data-ttu-id="d5fbc-190">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Ct: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="d5fbc-191">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kreedit: tegelik.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="d5fbc-192">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-192">Click Bind.</span></span>
21. <span data-ttu-id="d5fbc-193">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dt: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="d5fbc-194">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Deebet: tegelik.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="d5fbc-195">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-195">Click Bind.</span></span>
24. <span data-ttu-id="d5fbc-196">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Valuuta: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="d5fbc-197">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Valuuta: string.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="d5fbc-198">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-198">Click Bind.</span></span>
27. <span data-ttu-id="d5fbc-199">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Kuupäev: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="d5fbc-200">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kuupäev: kuupäev.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="d5fbc-201">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-201">Click Bind.</span></span>
30. <span data-ttu-id="d5fbc-202">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Kanne: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="d5fbc-203">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kanne: string.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="d5fbc-204">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-204">Click Bind.</span></span>
33. <span data-ttu-id="d5fbc-205">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="d5fbc-206">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="d5fbc-207">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-207">Click Bind.</span></span>
36. <span data-ttu-id="d5fbc-208">Valige puult Juur: XML-element \ Tööleht: XML-element \ Partii: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="d5fbc-209">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Partii: string.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="d5fbc-210">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-210">Click Bind.</span></span>
39. <span data-ttu-id="d5fbc-211">Valige puult Juur: XML-element \ Tööleht: XML-element.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="d5fbc-212">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="d5fbc-213">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-213">Click Bind.</span></span>
42. <span data-ttu-id="d5fbc-214">Valige puult Juur: XML-element \ Ettevõte: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="d5fbc-215">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Ettevõte: string.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="d5fbc-216">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-216">Click Bind.</span></span>
45. <span data-ttu-id="d5fbc-217">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-217">Click Save.</span></span>
46. <span data-ttu-id="d5fbc-218">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d5fbc-218">Close the page.</span></span>
<span data-ttu-id="d5fbc-219">![ER-i toimingute koostaja leht](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="d5fbc-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

