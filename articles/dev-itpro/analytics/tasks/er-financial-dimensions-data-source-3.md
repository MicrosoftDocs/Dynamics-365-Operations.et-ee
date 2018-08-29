--- 
title: Aruannete loomine finantsdimensioonide kasutamiseks andmeallikatena
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 055401104ae62c75694dff0b2ee64d12b2621686
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---
# <a name="design-reports-to-use-financial-dimensions-as-data-sources"></a><span data-ttu-id="df6dc-103">Aruannete loomine finantsdimensioonide kasutamiseks andmeallikatena</span><span class="sxs-lookup"><span data-stu-id="df6dc-103">Design reports to use financial dimensions as data sources</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="df6dc-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="df6dc-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="df6dc-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="df6dc-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="df6dc-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (2. osa: mudeli vastendamine).</span><span class="sxs-lookup"><span data-stu-id="df6dc-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="df6dc-107">Aruande koostamine finantsdimensioonide esitamiseks</span><span class="sxs-lookup"><span data-stu-id="df6dc-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="df6dc-108">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="df6dc-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="df6dc-109">Valige puult Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="df6dc-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="df6dc-110">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="df6dc-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="df6dc-111">Sisestage väljale Uus valik Vorming põhineb andmemudelil Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="df6dc-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="df6dc-112">Kasutage oma uue aruande andmeallikana eelnevalt loodud mudelit.</span><span class="sxs-lookup"><span data-stu-id="df6dc-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="df6dc-113">Tippige väljale Nimi tekst Pearaamatu töölehe aruanne.</span><span class="sxs-lookup"><span data-stu-id="df6dc-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="df6dc-114">Tehke väljal Andmemudeli definitsioon valik Kirje.</span><span class="sxs-lookup"><span data-stu-id="df6dc-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="df6dc-115">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="df6dc-115">Click Create configuration.</span></span>
8. <span data-ttu-id="df6dc-116">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="df6dc-116">Click Designer.</span></span>
9. <span data-ttu-id="df6dc-117">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="df6dc-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="df6dc-118">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="df6dc-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="df6dc-119">Tippige Juur väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="df6dc-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="df6dc-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="df6dc-120">Click OK.</span></span>
13. <span data-ttu-id="df6dc-121">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="df6dc-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="df6dc-122">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="df6dc-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="df6dc-123">Sisestage väljale Nimi suvand Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="df6dc-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="df6dc-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="df6dc-124">Click OK.</span></span>
17. <span data-ttu-id="df6dc-125">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="df6dc-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="df6dc-126">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="df6dc-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="df6dc-127">Tippige Tööleht väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="df6dc-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="df6dc-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="df6dc-128">Click OK.</span></span>
21. <span data-ttu-id="df6dc-129">Valige puult Juur: XML-element \ Tööleht: XML-element.</span><span class="sxs-lookup"><span data-stu-id="df6dc-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="df6dc-130">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="df6dc-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="df6dc-131">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="df6dc-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="df6dc-132">Tippige Partii väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="df6dc-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="df6dc-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="df6dc-133">Click OK.</span></span>
26. <span data-ttu-id="df6dc-134">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="df6dc-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="df6dc-135">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="df6dc-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="df6dc-136">Tippige väljale Nimi valik Kanne.</span><span class="sxs-lookup"><span data-stu-id="df6dc-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="df6dc-137">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="df6dc-137">Click OK.</span></span>
30. <span data-ttu-id="df6dc-138">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element.</span><span class="sxs-lookup"><span data-stu-id="df6dc-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="df6dc-139">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="df6dc-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="df6dc-140">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="df6dc-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="df6dc-141">Tippige Kanne väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="df6dc-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="df6dc-142">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="df6dc-142">Click OK.</span></span>
35. <span data-ttu-id="df6dc-143">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="df6dc-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="df6dc-144">Tippige Kuupäev väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="df6dc-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="df6dc-145">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="df6dc-145">Click OK.</span></span>
38. <span data-ttu-id="df6dc-146">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="df6dc-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="df6dc-147">Sisestage väljale Nimi suvand Valuuta.</span><span class="sxs-lookup"><span data-stu-id="df6dc-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="df6dc-148">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="df6dc-148">Click OK.</span></span>
41. <span data-ttu-id="df6dc-149">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="df6dc-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="df6dc-150">Tippige Dt väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="df6dc-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="df6dc-151">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="df6dc-151">Click OK.</span></span>
44. <span data-ttu-id="df6dc-152">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="df6dc-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="df6dc-153">Tippige Ct väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="df6dc-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="df6dc-154">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="df6dc-154">Click OK.</span></span>
47. <span data-ttu-id="df6dc-155">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="df6dc-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="df6dc-156">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="df6dc-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="df6dc-157">Tippige Dimensioonid väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="df6dc-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="df6dc-158">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="df6dc-158">Click OK.</span></span>
51. <span data-ttu-id="df6dc-159">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element.</span><span class="sxs-lookup"><span data-stu-id="df6dc-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="df6dc-160">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="df6dc-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="df6dc-161">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="df6dc-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="df6dc-162">Tippige Kood väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="df6dc-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="df6dc-163">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="df6dc-163">Click OK.</span></span>
56. <span data-ttu-id="df6dc-164">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="df6dc-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="df6dc-165">Tippige Väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="df6dc-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="df6dc-166">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="df6dc-166">Click OK.</span></span>
59. <span data-ttu-id="df6dc-167">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="df6dc-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="df6dc-168">Tippige Desc väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="df6dc-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="df6dc-169">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="df6dc-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="df6dc-170">Aruande elementide vastendamine andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="df6dc-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="df6dc-171">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="df6dc-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="df6dc-172">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="df6dc-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="df6dc-173">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="df6dc-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="df6dc-174">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="df6dc-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="df6dc-175">Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="df6dc-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="df6dc-176">Valige puult Juur: XM-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Desc: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="df6dc-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="df6dc-177">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Kirjeldus: string.</span><span class="sxs-lookup"><span data-stu-id="df6dc-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="df6dc-178">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="df6dc-178">Click Bind.</span></span>
9. <span data-ttu-id="df6dc-179">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Väärtus: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="df6dc-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="df6dc-180">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Kood: string.</span><span class="sxs-lookup"><span data-stu-id="df6dc-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="df6dc-181">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="df6dc-181">Click Bind.</span></span>
12. <span data-ttu-id="df6dc-182">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Kood: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="df6dc-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="df6dc-183">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Nimi: string.</span><span class="sxs-lookup"><span data-stu-id="df6dc-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="df6dc-184">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="df6dc-184">Click Bind.</span></span>
15. <span data-ttu-id="df6dc-185">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="df6dc-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="df6dc-186">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element.</span><span class="sxs-lookup"><span data-stu-id="df6dc-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="df6dc-187">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="df6dc-187">Click Bind.</span></span>
18. <span data-ttu-id="df6dc-188">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Ct: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="df6dc-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="df6dc-189">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kreedit: tegelik.</span><span class="sxs-lookup"><span data-stu-id="df6dc-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="df6dc-190">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="df6dc-190">Click Bind.</span></span>
21. <span data-ttu-id="df6dc-191">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dt: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="df6dc-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="df6dc-192">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Deebet: tegelik.</span><span class="sxs-lookup"><span data-stu-id="df6dc-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="df6dc-193">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="df6dc-193">Click Bind.</span></span>
24. <span data-ttu-id="df6dc-194">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Valuuta: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="df6dc-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="df6dc-195">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Valuuta: string.</span><span class="sxs-lookup"><span data-stu-id="df6dc-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="df6dc-196">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="df6dc-196">Click Bind.</span></span>
27. <span data-ttu-id="df6dc-197">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Kuupäev: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="df6dc-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="df6dc-198">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kuupäev: kuupäev.</span><span class="sxs-lookup"><span data-stu-id="df6dc-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="df6dc-199">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="df6dc-199">Click Bind.</span></span>
30. <span data-ttu-id="df6dc-200">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Kanne: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="df6dc-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="df6dc-201">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kanne: string.</span><span class="sxs-lookup"><span data-stu-id="df6dc-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="df6dc-202">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="df6dc-202">Click Bind.</span></span>
33. <span data-ttu-id="df6dc-203">Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element.</span><span class="sxs-lookup"><span data-stu-id="df6dc-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="df6dc-204">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="df6dc-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="df6dc-205">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="df6dc-205">Click Bind.</span></span>
36. <span data-ttu-id="df6dc-206">Valige puult Juur: XML-element \ Tööleht: XML-element \ Partii: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="df6dc-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="df6dc-207">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Partii: string.</span><span class="sxs-lookup"><span data-stu-id="df6dc-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="df6dc-208">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="df6dc-208">Click Bind.</span></span>
39. <span data-ttu-id="df6dc-209">Valige puult Juur: XML-element \ Tööleht: XML-element.</span><span class="sxs-lookup"><span data-stu-id="df6dc-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="df6dc-210">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="df6dc-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="df6dc-211">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="df6dc-211">Click Bind.</span></span>
42. <span data-ttu-id="df6dc-212">Valige puult Juur: XML-element \ Ettevõte: XML-atribuut.</span><span class="sxs-lookup"><span data-stu-id="df6dc-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="df6dc-213">Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Ettevõte: string.</span><span class="sxs-lookup"><span data-stu-id="df6dc-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="df6dc-214">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="df6dc-214">Click Bind.</span></span>
45. <span data-ttu-id="df6dc-215">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="df6dc-215">Click Save.</span></span>
46. <span data-ttu-id="df6dc-216">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="df6dc-216">Close the page.</span></span>


