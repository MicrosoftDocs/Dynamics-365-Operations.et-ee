---
title: Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (3. osa – arvutuste kasutamine väljundi koostamiseks)
description: Selles teemas kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse vormingut juba loodud tekstiväljundi andmete põhjal loendama ja liitma. (3. osa)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af95399118b9059b9bead3a1b84203cf3b6e74c2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567112"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="3e01e-104">Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (3. osa – arvutuste kasutamine väljundi koostamiseks)</span><span class="sxs-lookup"><span data-stu-id="3e01e-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e01e-105">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="3e01e-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="3e01e-106">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="3e01e-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="3e01e-107">Nende etappide lõpule viimiseks peate esmalt viima lõpule etapid protseduuris „Elektrooniline aruandlus Vormingu konfigureerimine loendamiseks ja liitmiseks (2. osa: arvutuste konfigureerimine)”.</span><span class="sxs-lookup"><span data-stu-id="3e01e-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="3e01e-108">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="3e01e-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="3e01e-109">Selle aruande konfigureerimine loendamise ja liitmise teabe kasutamiseks</span><span class="sxs-lookup"><span data-stu-id="3e01e-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="3e01e-110">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="3e01e-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="3e01e-111">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="3e01e-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="3e01e-112">Laiendage puul valikut Intrastati mudel.</span><span class="sxs-lookup"><span data-stu-id="3e01e-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="3e01e-113">Laiendage puul valikut Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="3e01e-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="3e01e-114">Valige puult „Intrastati mudel\Intrastat (DE)\Intrastat (DE) koos loendamise ja liitmisega“.</span><span class="sxs-lookup"><span data-stu-id="3e01e-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="3e01e-115">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="3e01e-115">Click Designer.</span></span>
7. <span data-ttu-id="3e01e-116">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="3e01e-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="3e01e-117">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="3e01e-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="3e01e-118">Lisage uus andmeallikas meelde jäetud plokkide loendi saamiseks.</span><span class="sxs-lookup"><span data-stu-id="3e01e-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="3e01e-119">Valige puul suvand Funktsioonid\arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="3e01e-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="3e01e-120">Tippige $BlocksList väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="3e01e-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="3e01e-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="3e01e-121">$BlocksList</span></span>  
11. <span data-ttu-id="3e01e-122">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="3e01e-122">Click Edit formula.</span></span>
12. <span data-ttu-id="3e01e-123">Valige puult Andmekogumi funktsioonid \ COLLECTEDLIST.</span><span class="sxs-lookup"><span data-stu-id="3e01e-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="3e01e-124">Klõpsake suvandit Funktsiooni lisamine.</span><span class="sxs-lookup"><span data-stu-id="3e01e-124">Click Add function.</span></span>
14. <span data-ttu-id="3e01e-125">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="3e01e-125">Click Add data source.</span></span>
15. <span data-ttu-id="3e01e-126">Sisestage väljale Valem COLLECTEDLIST('$BlockName', .</span><span class="sxs-lookup"><span data-stu-id="3e01e-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="3e01e-127">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="3e01e-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="3e01e-128">Sisestage väljale Valem COLLECTEDLIST('$BlockName', "\*").</span><span class="sxs-lookup"><span data-stu-id="3e01e-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="3e01e-129">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="3e01e-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="3e01e-130">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="3e01e-130">Click Save.</span></span>
    * <span data-ttu-id="3e01e-131">Muster „\*” tähendab, et kõik plokid lisatakse selle kirje loendisse.</span><span class="sxs-lookup"><span data-stu-id="3e01e-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="3e01e-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3e01e-132">Close the page.</span></span>
19. <span data-ttu-id="3e01e-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3e01e-133">Click OK.</span></span>
20. <span data-ttu-id="3e01e-134">Klõpsake vahekaarti Vorming.</span><span class="sxs-lookup"><span data-stu-id="3e01e-134">Click the Format tab.</span></span>
21. <span data-ttu-id="3e01e-135">Tehke puul valik Intrastat \ Andmed.</span><span class="sxs-lookup"><span data-stu-id="3e01e-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="3e01e-136">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="3e01e-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="3e01e-137">Valige puult Tekst \ Seeria.</span><span class="sxs-lookup"><span data-stu-id="3e01e-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="3e01e-138">Tippige väljale Nimi valik Kogusummad plokkide alusel.</span><span class="sxs-lookup"><span data-stu-id="3e01e-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="3e01e-139">Kogusummad plokkide alusel</span><span class="sxs-lookup"><span data-stu-id="3e01e-139">Totals by blocks</span></span>  
25. <span data-ttu-id="3e01e-140">Valige väljal Erimärgid Uus rida – Windows (CR LF).</span><span class="sxs-lookup"><span data-stu-id="3e01e-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="3e01e-141">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3e01e-141">Click OK.</span></span>
27. <span data-ttu-id="3e01e-142">Valige puult Intrastat \ Andmed \ Kogusummad plokkide alusel.</span><span class="sxs-lookup"><span data-stu-id="3e01e-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="3e01e-143">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="3e01e-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="3e01e-144">Valige puul suvand Tekst\String.</span><span class="sxs-lookup"><span data-stu-id="3e01e-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="3e01e-145">Tippige Ploki kood väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="3e01e-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="3e01e-146">Ploki kood</span><span class="sxs-lookup"><span data-stu-id="3e01e-146">Block code</span></span>  
31. <span data-ttu-id="3e01e-147">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3e01e-147">Click OK.</span></span>
32. <span data-ttu-id="3e01e-148">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="3e01e-148">Click Add String.</span></span>
33. <span data-ttu-id="3e01e-149">Tippige väljale Nimi valik Ridade loendamine.</span><span class="sxs-lookup"><span data-stu-id="3e01e-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="3e01e-150">Ridade loendamine</span><span class="sxs-lookup"><span data-stu-id="3e01e-150">Lines counting</span></span>  
34. <span data-ttu-id="3e01e-151">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3e01e-151">Click OK.</span></span>
35. <span data-ttu-id="3e01e-152">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="3e01e-152">Click Add String.</span></span>
36. <span data-ttu-id="3e01e-153">Tippige väljale Nimi valik Kogusumma.</span><span class="sxs-lookup"><span data-stu-id="3e01e-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="3e01e-154">Kogusumma</span><span class="sxs-lookup"><span data-stu-id="3e01e-154">Total amount</span></span>  
37. <span data-ttu-id="3e01e-155">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3e01e-155">Click OK.</span></span>
38. <span data-ttu-id="3e01e-156">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="3e01e-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="3e01e-157">Valige puul väärtus $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="3e01e-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="3e01e-158">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="3e01e-158">Click Bind.</span></span>
    * <span data-ttu-id="3e01e-159">Looge iga meelde jäetud ploki kohta kokkuvõtte rida.</span><span class="sxs-lookup"><span data-stu-id="3e01e-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="3e01e-160">Klõpsake vahekaarti Vorming.</span><span class="sxs-lookup"><span data-stu-id="3e01e-160">Click the Format tab.</span></span>
42. <span data-ttu-id="3e01e-161">Valige puult Intrastat \ Andmed \ Kogusummad plokkide alusel \ Ploki kood.</span><span class="sxs-lookup"><span data-stu-id="3e01e-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="3e01e-162">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="3e01e-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="3e01e-163">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="3e01e-163">Click Edit formula.</span></span>
45. <span data-ttu-id="3e01e-164">Sisestage väljale Valem tekst „"Block id: " & “.</span><span class="sxs-lookup"><span data-stu-id="3e01e-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="3e01e-165">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="3e01e-165">"Block id: " &</span></span>  
46. <span data-ttu-id="3e01e-166">Laiendage puul väärtust $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="3e01e-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="3e01e-167">Valige puult $BlocksList\Väärtus.</span><span class="sxs-lookup"><span data-stu-id="3e01e-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="3e01e-168">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="3e01e-168">Click Add data source.</span></span>
49. <span data-ttu-id="3e01e-169">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="3e01e-169">Click Save.</span></span>
50. <span data-ttu-id="3e01e-170">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3e01e-170">Close the page.</span></span>
51. <span data-ttu-id="3e01e-171">Klõpsake vahekaarti Vorming.</span><span class="sxs-lookup"><span data-stu-id="3e01e-171">Click the Format tab.</span></span>
52. <span data-ttu-id="3e01e-172">Valige puult Intrastat \ Andmed \ Kogusummad plokkide alusel \ Ridade loendamine.</span><span class="sxs-lookup"><span data-stu-id="3e01e-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="3e01e-173">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="3e01e-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="3e01e-174">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="3e01e-174">Click Edit formula.</span></span>
    * <span data-ttu-id="3e01e-175">Looge iga selles aruandes esitatud ploki ridade arvu kohta väljund.</span><span class="sxs-lookup"><span data-stu-id="3e01e-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="3e01e-176">Sisestage väljale Valem „"Number of lines in this block: " & ”.</span><span class="sxs-lookup"><span data-stu-id="3e01e-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="3e01e-177">"Number of lines in this block: " &</span><span class="sxs-lookup"><span data-stu-id="3e01e-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="3e01e-178">Sisestage väljale Valem "Number of lines in this block: " & TEXT(.</span><span class="sxs-lookup"><span data-stu-id="3e01e-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="3e01e-179">"Number of lines in this block: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="3e01e-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="3e01e-180">Valige puult Andmekogumi funktsioonid \ COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="3e01e-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="3e01e-181">Klõpsake suvandit Funktsiooni lisamine.</span><span class="sxs-lookup"><span data-stu-id="3e01e-181">Click Add function.</span></span>
59. <span data-ttu-id="3e01e-182">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="3e01e-182">Click Add data source.</span></span>
60. <span data-ttu-id="3e01e-183">Sisestage väljale Valem "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="3e01e-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="3e01e-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="3e01e-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="3e01e-185">Laiendage puul väärtust $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="3e01e-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="3e01e-186">Valige puult $BlocksList\Väärtus.</span><span class="sxs-lookup"><span data-stu-id="3e01e-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="3e01e-187">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="3e01e-187">Click Add data source.</span></span>
64. <span data-ttu-id="3e01e-188">Sisestage väljale Valem "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="3e01e-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="3e01e-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="3e01e-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="3e01e-190">Valige puul väärtus $RecName.</span><span class="sxs-lookup"><span data-stu-id="3e01e-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="3e01e-191">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="3e01e-191">Click Add data source.</span></span>
67. <span data-ttu-id="3e01e-192">Sisestage väljale Valem "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*")).</span><span class="sxs-lookup"><span data-stu-id="3e01e-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="3e01e-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="3e01e-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="3e01e-194">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="3e01e-194">Click Save.</span></span>
69. <span data-ttu-id="3e01e-195">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3e01e-195">Close the page.</span></span>
70. <span data-ttu-id="3e01e-196">Klõpsake vahekaarti Vorming.</span><span class="sxs-lookup"><span data-stu-id="3e01e-196">Click the Format tab.</span></span>
71. <span data-ttu-id="3e01e-197">Valige puult Intrastat \ Andmed \ Kogusummad plokkide alusel \ Kogusumma.</span><span class="sxs-lookup"><span data-stu-id="3e01e-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="3e01e-198">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="3e01e-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="3e01e-199">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="3e01e-199">Click Edit formula.</span></span>
    * <span data-ttu-id="3e01e-200">Looge väljund, mis on iga selles aruandes esitatud ploki arveldatud summa koguväärtus.</span><span class="sxs-lookup"><span data-stu-id="3e01e-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="3e01e-201">Sisestage väljale Valem "Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*")).</span><span class="sxs-lookup"><span data-stu-id="3e01e-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="3e01e-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="3e01e-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="3e01e-203">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="3e01e-203">Click Save.</span></span>
76. <span data-ttu-id="3e01e-204">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3e01e-204">Close the page.</span></span>
77. <span data-ttu-id="3e01e-205">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="3e01e-205">Click Save.</span></span>
78. <span data-ttu-id="3e01e-206">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3e01e-206">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]