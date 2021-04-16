---
title: Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (3. osa – aruande koostamine)
description: Selles teemas kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse (ER) mudelit kasutama finantsdimensioone andmeallikana ER-i aruannetele. (3. osa)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a3b9a8b5775d2001f3384480e2f9593f2dfa8b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752408"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="becfb-104">Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (3. osa – aruande koostamine)</span><span class="sxs-lookup"><span data-stu-id="becfb-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="becfb-105">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="becfb-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="becfb-106">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="becfb-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="becfb-107">Nende etappide lõpule viimiseks peate esmalt viima lõpule etapid protseduuris „Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (2. osa: mudeli vastendamine)”.</span><span class="sxs-lookup"><span data-stu-id="becfb-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="becfb-108">Aruande koostamine finantsdimensioonide esitamiseks</span><span class="sxs-lookup"><span data-stu-id="becfb-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="becfb-109">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="becfb-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="becfb-110">Valige puult Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="becfb-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="becfb-111">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="becfb-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="becfb-112">Sisestage väljale Uus valik Vorming põhineb andmemudelil Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="becfb-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="becfb-113">Kasutage oma uue aruande andmeallikana eelnevalt loodud mudelit.</span><span class="sxs-lookup"><span data-stu-id="becfb-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="becfb-114">Tippige väljale Nimi tekst Pearaamatu töölehe aruanne.</span><span class="sxs-lookup"><span data-stu-id="becfb-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="becfb-115">Tehke väljal Andmemudeli definitsioon valik Kirje.</span><span class="sxs-lookup"><span data-stu-id="becfb-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="becfb-116">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="becfb-116">Click Create configuration.</span></span>
8. <span data-ttu-id="becfb-117">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="becfb-117">Click Designer.</span></span>
9. <span data-ttu-id="becfb-118">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="becfb-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="becfb-119">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="becfb-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="becfb-120">Tippige Juur väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="becfb-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="becfb-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="becfb-121">Click OK.</span></span>
13. <span data-ttu-id="becfb-122">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="becfb-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="becfb-123">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="becfb-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="becfb-124">Sisestage väljale Nimi suvand Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="becfb-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="becfb-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="becfb-125">Click OK.</span></span>
17. <span data-ttu-id="becfb-126">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="becfb-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="becfb-127">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="becfb-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="becfb-128">Tippige Tööleht väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="becfb-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="becfb-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="becfb-129">Click OK.</span></span>
21. <span data-ttu-id="becfb-130">Valige puult Juur: XML-element \ Tööleht: XML-element.</span><span class="sxs-lookup"><span data-stu-id="becfb-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="becfb-131">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="becfb-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="becfb-132">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="becfb-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="becfb-133">Tippige Partii väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="becfb-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="becfb-134">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="becfb-134">Click OK.</span></span>
26. <span data-ttu-id="becfb-135">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="becfb-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="becfb-136">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="becfb-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="becfb-137">Tippige väljale Nimi valik Kanne.</span><span class="sxs-lookup"><span data-stu-id="becfb-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="becfb-138">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="becfb-138">Click OK.</span></span>
30. <span data-ttu-id="becfb-139">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element.</span><span class="sxs-lookup"><span data-stu-id="becfb-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="becfb-140">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="becfb-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="becfb-141">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="becfb-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="becfb-142">Tippige Kanne väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="becfb-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="becfb-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="becfb-143">Click OK.</span></span>
35. <span data-ttu-id="becfb-144">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="becfb-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="becfb-145">Tippige Kuupäev väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="becfb-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="becfb-146">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="becfb-146">Click OK.</span></span>
38. <span data-ttu-id="becfb-147">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="becfb-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="becfb-148">Sisestage väljale Nimi suvand Valuuta.</span><span class="sxs-lookup"><span data-stu-id="becfb-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="becfb-149">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="becfb-149">Click OK.</span></span>
41. <span data-ttu-id="becfb-150">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="becfb-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="becfb-151">Tippige Dt väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="becfb-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="becfb-152">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="becfb-152">Click OK.</span></span>
44. <span data-ttu-id="becfb-153">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="becfb-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="becfb-154">Tippige Ct väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="becfb-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="becfb-155">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="becfb-155">Click OK.</span></span>
47. <span data-ttu-id="becfb-156">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="becfb-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="becfb-157">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="becfb-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="becfb-158">Tippige Dimensioonid väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="becfb-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="becfb-159">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="becfb-159">Click OK.</span></span>
51. <span data-ttu-id="becfb-160">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element.</span><span class="sxs-lookup"><span data-stu-id="becfb-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="becfb-161">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="becfb-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="becfb-162">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="becfb-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="becfb-163">Tippige Kood väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="becfb-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="becfb-164">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="becfb-164">Click OK.</span></span>
56. <span data-ttu-id="becfb-165">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="becfb-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="becfb-166">Tippige Väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="becfb-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="becfb-167">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="becfb-167">Click OK.</span></span>
59. <span data-ttu-id="becfb-168">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="becfb-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="becfb-169">Tippige Desc väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="becfb-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="becfb-170">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="becfb-170">Click OK.</span></span>
<span data-ttu-id="becfb-171">![ER-i toimingute koostaja leht](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="becfb-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="becfb-172">Aruande elementide vastendamine andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="becfb-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="becfb-173">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="becfb-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="becfb-174">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="becfb-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="becfb-175">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="becfb-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="becfb-176">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="becfb-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="becfb-177">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="becfb-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="becfb-178">Valige puult Juur: XM-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Desc: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="becfb-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="becfb-179">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Kirjeldus: string.</span><span class="sxs-lookup"><span data-stu-id="becfb-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="becfb-180">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="becfb-180">Click Bind.</span></span>
9. <span data-ttu-id="becfb-181">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Väärtus: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="becfb-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="becfb-182">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Kood: string.</span><span class="sxs-lookup"><span data-stu-id="becfb-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="becfb-183">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="becfb-183">Click Bind.</span></span>
12. <span data-ttu-id="becfb-184">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Kood: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="becfb-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="becfb-185">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Nimi: string.</span><span class="sxs-lookup"><span data-stu-id="becfb-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="becfb-186">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="becfb-186">Click Bind.</span></span>
15. <span data-ttu-id="becfb-187">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="becfb-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="becfb-188">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element.</span><span class="sxs-lookup"><span data-stu-id="becfb-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="becfb-189">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="becfb-189">Click Bind.</span></span>
18. <span data-ttu-id="becfb-190">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Ct: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="becfb-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="becfb-191">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kreedit: tegelik.</span><span class="sxs-lookup"><span data-stu-id="becfb-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="becfb-192">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="becfb-192">Click Bind.</span></span>
21. <span data-ttu-id="becfb-193">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dt: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="becfb-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="becfb-194">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Deebet: tegelik.</span><span class="sxs-lookup"><span data-stu-id="becfb-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="becfb-195">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="becfb-195">Click Bind.</span></span>
24. <span data-ttu-id="becfb-196">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Valuuta: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="becfb-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="becfb-197">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Valuuta: string.</span><span class="sxs-lookup"><span data-stu-id="becfb-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="becfb-198">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="becfb-198">Click Bind.</span></span>
27. <span data-ttu-id="becfb-199">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Kuupäev: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="becfb-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="becfb-200">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kuupäev: kuupäev.</span><span class="sxs-lookup"><span data-stu-id="becfb-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="becfb-201">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="becfb-201">Click Bind.</span></span>
30. <span data-ttu-id="becfb-202">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Kanne: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="becfb-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="becfb-203">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kanne: string.</span><span class="sxs-lookup"><span data-stu-id="becfb-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="becfb-204">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="becfb-204">Click Bind.</span></span>
33. <span data-ttu-id="becfb-205">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element.</span><span class="sxs-lookup"><span data-stu-id="becfb-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="becfb-206">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="becfb-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="becfb-207">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="becfb-207">Click Bind.</span></span>
36. <span data-ttu-id="becfb-208">Valige puult Juur: XML-element \ Tööleht: XML-element \ Partii: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="becfb-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="becfb-209">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Partii: string.</span><span class="sxs-lookup"><span data-stu-id="becfb-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="becfb-210">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="becfb-210">Click Bind.</span></span>
39. <span data-ttu-id="becfb-211">Valige puult Juur: XML-element \ Tööleht: XML-element.</span><span class="sxs-lookup"><span data-stu-id="becfb-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="becfb-212">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="becfb-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="becfb-213">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="becfb-213">Click Bind.</span></span>
42. <span data-ttu-id="becfb-214">Valige puult Juur: XML-element \ Ettevõte: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="becfb-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="becfb-215">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Ettevõte: string.</span><span class="sxs-lookup"><span data-stu-id="becfb-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="becfb-216">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="becfb-216">Click Bind.</span></span>
45. <span data-ttu-id="becfb-217">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="becfb-217">Click Save.</span></span>
46. <span data-ttu-id="becfb-218">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="becfb-218">Close the page.</span></span>
<span data-ttu-id="becfb-219">![ER-i toimingute koostaja leht](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="becfb-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]