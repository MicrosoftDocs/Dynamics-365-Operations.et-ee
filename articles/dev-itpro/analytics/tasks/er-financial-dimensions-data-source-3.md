--- 
title: Elektroonilise aruandluse (ER) aruande koostamine finantsdimensioonide kasutamiseks andmeallikana
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.openlocfilehash: 178deb75bec9ee7c9c355b06850f7f771bac8704
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="design-a-report-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="7296f-103">Elektroonilise aruandluse (ER) aruande koostamine finantsdimensioonide kasutamiseks andmeallikana</span><span class="sxs-lookup"><span data-stu-id="7296f-103">Design a report to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7296f-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="7296f-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="7296f-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="7296f-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="7296f-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (2. osa: mudeli vastendamine).</span><span class="sxs-lookup"><span data-stu-id="7296f-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="7296f-107">Aruande koostamine finantsdimensioonide esitamiseks</span><span class="sxs-lookup"><span data-stu-id="7296f-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="7296f-108">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="7296f-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="7296f-109">Valige puult Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="7296f-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="7296f-110">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="7296f-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="7296f-111">Sisestage väljale Uus valik Vorming põhineb andmemudelil Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="7296f-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="7296f-112">Kasutage oma uue aruande andmeallikana eelnevalt loodud mudelit.</span><span class="sxs-lookup"><span data-stu-id="7296f-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="7296f-113">Tippige väljale Nimi tekst Pearaamatu töölehe aruanne.</span><span class="sxs-lookup"><span data-stu-id="7296f-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="7296f-114">Tehke väljal Andmemudeli definitsioon valik Kirje.</span><span class="sxs-lookup"><span data-stu-id="7296f-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="7296f-115">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="7296f-115">Click Create configuration.</span></span>
8. <span data-ttu-id="7296f-116">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="7296f-116">Click Designer.</span></span>
9. <span data-ttu-id="7296f-117">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="7296f-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="7296f-118">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="7296f-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="7296f-119">Tippige Juur väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="7296f-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="7296f-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7296f-120">Click OK.</span></span>
13. <span data-ttu-id="7296f-121">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="7296f-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="7296f-122">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="7296f-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="7296f-123">Sisestage väljale Nimi suvand Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="7296f-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="7296f-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7296f-124">Click OK.</span></span>
17. <span data-ttu-id="7296f-125">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="7296f-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="7296f-126">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="7296f-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="7296f-127">Tippige Tööleht väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="7296f-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="7296f-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7296f-128">Click OK.</span></span>
21. <span data-ttu-id="7296f-129">Valige puult Juur: XML-element \ Tööleht: XML-element.</span><span class="sxs-lookup"><span data-stu-id="7296f-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="7296f-130">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="7296f-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="7296f-131">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="7296f-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="7296f-132">Tippige Partii väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="7296f-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="7296f-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7296f-133">Click OK.</span></span>
26. <span data-ttu-id="7296f-134">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="7296f-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="7296f-135">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="7296f-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="7296f-136">Tippige väljale Nimi valik Kanne.</span><span class="sxs-lookup"><span data-stu-id="7296f-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="7296f-137">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7296f-137">Click OK.</span></span>
30. <span data-ttu-id="7296f-138">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element.</span><span class="sxs-lookup"><span data-stu-id="7296f-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="7296f-139">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="7296f-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="7296f-140">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="7296f-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="7296f-141">Tippige Kanne väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="7296f-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="7296f-142">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7296f-142">Click OK.</span></span>
35. <span data-ttu-id="7296f-143">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="7296f-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="7296f-144">Tippige Kuupäev väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="7296f-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="7296f-145">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7296f-145">Click OK.</span></span>
38. <span data-ttu-id="7296f-146">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="7296f-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="7296f-147">Sisestage väljale Nimi suvand Valuuta.</span><span class="sxs-lookup"><span data-stu-id="7296f-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="7296f-148">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7296f-148">Click OK.</span></span>
41. <span data-ttu-id="7296f-149">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="7296f-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="7296f-150">Tippige Dt väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="7296f-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="7296f-151">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7296f-151">Click OK.</span></span>
44. <span data-ttu-id="7296f-152">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="7296f-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="7296f-153">Tippige Ct väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="7296f-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="7296f-154">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7296f-154">Click OK.</span></span>
47. <span data-ttu-id="7296f-155">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="7296f-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="7296f-156">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="7296f-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="7296f-157">Tippige Dimensioonid väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="7296f-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="7296f-158">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7296f-158">Click OK.</span></span>
51. <span data-ttu-id="7296f-159">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element.</span><span class="sxs-lookup"><span data-stu-id="7296f-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="7296f-160">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="7296f-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="7296f-161">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="7296f-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="7296f-162">Tippige Kood väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="7296f-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="7296f-163">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7296f-163">Click OK.</span></span>
56. <span data-ttu-id="7296f-164">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="7296f-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="7296f-165">Tippige Väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="7296f-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="7296f-166">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7296f-166">Click OK.</span></span>
59. <span data-ttu-id="7296f-167">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="7296f-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="7296f-168">Tippige Desc väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="7296f-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="7296f-169">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7296f-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="7296f-170">Aruande elementide vastendamine andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="7296f-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="7296f-171">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="7296f-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="7296f-172">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="7296f-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="7296f-173">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="7296f-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="7296f-174">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="7296f-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="7296f-175">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="7296f-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="7296f-176">Valige puult Juur: XM-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Desc: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="7296f-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="7296f-177">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Kirjeldus: string.</span><span class="sxs-lookup"><span data-stu-id="7296f-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="7296f-178">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="7296f-178">Click Bind.</span></span>
9. <span data-ttu-id="7296f-179">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Väärtus: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="7296f-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="7296f-180">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Kood: string.</span><span class="sxs-lookup"><span data-stu-id="7296f-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="7296f-181">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="7296f-181">Click Bind.</span></span>
12. <span data-ttu-id="7296f-182">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Kood: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="7296f-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="7296f-183">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Nimi: string.</span><span class="sxs-lookup"><span data-stu-id="7296f-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="7296f-184">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="7296f-184">Click Bind.</span></span>
15. <span data-ttu-id="7296f-185">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="7296f-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="7296f-186">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element.</span><span class="sxs-lookup"><span data-stu-id="7296f-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="7296f-187">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="7296f-187">Click Bind.</span></span>
18. <span data-ttu-id="7296f-188">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Ct: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="7296f-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="7296f-189">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kreedit: tegelik.</span><span class="sxs-lookup"><span data-stu-id="7296f-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="7296f-190">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="7296f-190">Click Bind.</span></span>
21. <span data-ttu-id="7296f-191">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dt: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="7296f-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="7296f-192">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Deebet: tegelik.</span><span class="sxs-lookup"><span data-stu-id="7296f-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="7296f-193">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="7296f-193">Click Bind.</span></span>
24. <span data-ttu-id="7296f-194">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Valuuta: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="7296f-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="7296f-195">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Valuuta: string.</span><span class="sxs-lookup"><span data-stu-id="7296f-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="7296f-196">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="7296f-196">Click Bind.</span></span>
27. <span data-ttu-id="7296f-197">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Kuupäev: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="7296f-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="7296f-198">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kuupäev: kuupäev.</span><span class="sxs-lookup"><span data-stu-id="7296f-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="7296f-199">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="7296f-199">Click Bind.</span></span>
30. <span data-ttu-id="7296f-200">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Kanne: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="7296f-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="7296f-201">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kanne: string.</span><span class="sxs-lookup"><span data-stu-id="7296f-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="7296f-202">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="7296f-202">Click Bind.</span></span>
33. <span data-ttu-id="7296f-203">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element.</span><span class="sxs-lookup"><span data-stu-id="7296f-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="7296f-204">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="7296f-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="7296f-205">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="7296f-205">Click Bind.</span></span>
36. <span data-ttu-id="7296f-206">Valige puult Juur: XML-element \ Tööleht: XML-element \ Partii: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="7296f-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="7296f-207">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Partii: string.</span><span class="sxs-lookup"><span data-stu-id="7296f-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="7296f-208">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="7296f-208">Click Bind.</span></span>
39. <span data-ttu-id="7296f-209">Valige puult Juur: XML-element \ Tööleht: XML-element.</span><span class="sxs-lookup"><span data-stu-id="7296f-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="7296f-210">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="7296f-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="7296f-211">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="7296f-211">Click Bind.</span></span>
42. <span data-ttu-id="7296f-212">Valige puult Juur: XML-element \ Ettevõte: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="7296f-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="7296f-213">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Ettevõte: string.</span><span class="sxs-lookup"><span data-stu-id="7296f-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="7296f-214">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="7296f-214">Click Bind.</span></span>
45. <span data-ttu-id="7296f-215">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="7296f-215">Click Save.</span></span>
46. <span data-ttu-id="7296f-216">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="7296f-216">Close the page.</span></span>


