---
title: Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (3. osa – arvutuste kasutamine väljundi koostamiseks)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7bbef7048488056f50ec8967a9af53d468666856
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550759"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="f7403-103">Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (3. osa – arvutuste kasutamine väljundi koostamiseks)</span><span class="sxs-lookup"><span data-stu-id="f7403-103">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f7403-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="f7403-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="f7403-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="f7403-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="f7403-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Vormingu konfigureerimine loendamiseks ja liitmiseks (2. osa: arvutuste konfigureerimine).</span><span class="sxs-lookup"><span data-stu-id="f7403-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="f7403-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="f7403-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="f7403-108">Selle aruande konfigureerimine loendamise ja liitmise teabe kasutamiseks</span><span class="sxs-lookup"><span data-stu-id="f7403-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="f7403-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="f7403-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f7403-110">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="f7403-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="f7403-111">Laiendage puul valikut Intrastati mudel.</span><span class="sxs-lookup"><span data-stu-id="f7403-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="f7403-112">Laiendage puul valikut Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="f7403-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="f7403-113">Valige puult „Intrastati mudel\Intrastat (DE)\Intrastat (DE) koos loendamise ja liitmisega“.</span><span class="sxs-lookup"><span data-stu-id="f7403-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="f7403-114">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="f7403-114">Click Designer.</span></span>
7. <span data-ttu-id="f7403-115">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="f7403-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="f7403-116">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="f7403-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="f7403-117">Lisage uus andmeallikas meelde jäetud plokkide loendi saamiseks.</span><span class="sxs-lookup"><span data-stu-id="f7403-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="f7403-118">Valige puul suvand Funktsioonid\arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="f7403-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="f7403-119">Tippige $BlocksList väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f7403-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="f7403-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="f7403-120">$BlocksList</span></span>  
11. <span data-ttu-id="f7403-121">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="f7403-121">Click Edit formula.</span></span>
12. <span data-ttu-id="f7403-122">Valige puult Andmekogumi funktsioonid \ COLLECTEDLIST.</span><span class="sxs-lookup"><span data-stu-id="f7403-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="f7403-123">Klõpsake suvandit Funktsiooni lisamine.</span><span class="sxs-lookup"><span data-stu-id="f7403-123">Click Add function.</span></span>
14. <span data-ttu-id="f7403-124">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="f7403-124">Click Add data source.</span></span>
15. <span data-ttu-id="f7403-125">Sisestage väljale Valem COLLECTEDLIST('$BlockName', .</span><span class="sxs-lookup"><span data-stu-id="f7403-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="f7403-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="f7403-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="f7403-127">Sisestage väljale Valem COLLECTEDLIST('$BlockName', "\*").</span><span class="sxs-lookup"><span data-stu-id="f7403-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="f7403-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="f7403-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="f7403-129">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f7403-129">Click Save.</span></span>
    * <span data-ttu-id="f7403-130">Muster „\*” tähendab, et kõik plokid lisatakse selle kirje loendisse.</span><span class="sxs-lookup"><span data-stu-id="f7403-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="f7403-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7403-131">Close the page.</span></span>
19. <span data-ttu-id="f7403-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f7403-132">Click OK.</span></span>
20. <span data-ttu-id="f7403-133">Klõpsake vahekaarti Vorming.</span><span class="sxs-lookup"><span data-stu-id="f7403-133">Click the Format tab.</span></span>
21. <span data-ttu-id="f7403-134">Tehke puul valik Intrastat \ Andmed.</span><span class="sxs-lookup"><span data-stu-id="f7403-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="f7403-135">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="f7403-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="f7403-136">Valige puult Tekst \ Seeria.</span><span class="sxs-lookup"><span data-stu-id="f7403-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="f7403-137">Tippige väljale Nimi valik Kogusummad plokkide alusel.</span><span class="sxs-lookup"><span data-stu-id="f7403-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="f7403-138">Kogusummad plokkide alusel</span><span class="sxs-lookup"><span data-stu-id="f7403-138">Totals by blocks</span></span>  
25. <span data-ttu-id="f7403-139">Valige väljal Erimärgid Uus rida – Windows (CR LF).</span><span class="sxs-lookup"><span data-stu-id="f7403-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="f7403-140">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f7403-140">Click OK.</span></span>
27. <span data-ttu-id="f7403-141">Valige puult Intrastat \ Andmed \ Kogusummad plokkide alusel.</span><span class="sxs-lookup"><span data-stu-id="f7403-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="f7403-142">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="f7403-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="f7403-143">Valige puul suvand Tekst\String.</span><span class="sxs-lookup"><span data-stu-id="f7403-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="f7403-144">Tippige Ploki kood väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f7403-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="f7403-145">Ploki kood</span><span class="sxs-lookup"><span data-stu-id="f7403-145">Block code</span></span>  
31. <span data-ttu-id="f7403-146">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f7403-146">Click OK.</span></span>
32. <span data-ttu-id="f7403-147">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="f7403-147">Click Add String.</span></span>
33. <span data-ttu-id="f7403-148">Tippige väljale Nimi valik Ridade loendamine.</span><span class="sxs-lookup"><span data-stu-id="f7403-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="f7403-149">Ridade loendamine</span><span class="sxs-lookup"><span data-stu-id="f7403-149">Lines counting</span></span>  
34. <span data-ttu-id="f7403-150">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f7403-150">Click OK.</span></span>
35. <span data-ttu-id="f7403-151">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="f7403-151">Click Add String.</span></span>
36. <span data-ttu-id="f7403-152">Tippige väljale Nimi valik Kogusumma.</span><span class="sxs-lookup"><span data-stu-id="f7403-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="f7403-153">Kogusumma</span><span class="sxs-lookup"><span data-stu-id="f7403-153">Total amount</span></span>  
37. <span data-ttu-id="f7403-154">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f7403-154">Click OK.</span></span>
38. <span data-ttu-id="f7403-155">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="f7403-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="f7403-156">Valige puul väärtus $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="f7403-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="f7403-157">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="f7403-157">Click Bind.</span></span>
    * <span data-ttu-id="f7403-158">Looge iga meelde jäetud ploki kohta kokkuvõtte rida.</span><span class="sxs-lookup"><span data-stu-id="f7403-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="f7403-159">Klõpsake vahekaarti Vorming.</span><span class="sxs-lookup"><span data-stu-id="f7403-159">Click the Format tab.</span></span>
42. <span data-ttu-id="f7403-160">Valige puult Intrastat \ Andmed \ Kogusummad plokkide alusel \ Ploki kood.</span><span class="sxs-lookup"><span data-stu-id="f7403-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="f7403-161">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="f7403-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="f7403-162">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="f7403-162">Click Edit formula.</span></span>
45. <span data-ttu-id="f7403-163">Sisestage väljale Valem tekst „"Block id: " & “.</span><span class="sxs-lookup"><span data-stu-id="f7403-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="f7403-164">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="f7403-164">"Block id: " &</span></span>  
46. <span data-ttu-id="f7403-165">Laiendage puul väärtust $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="f7403-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="f7403-166">Valige puult $BlocksList\Väärtus.</span><span class="sxs-lookup"><span data-stu-id="f7403-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="f7403-167">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="f7403-167">Click Add data source.</span></span>
49. <span data-ttu-id="f7403-168">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f7403-168">Click Save.</span></span>
50. <span data-ttu-id="f7403-169">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7403-169">Close the page.</span></span>
51. <span data-ttu-id="f7403-170">Klõpsake vahekaarti Vorming.</span><span class="sxs-lookup"><span data-stu-id="f7403-170">Click the Format tab.</span></span>
52. <span data-ttu-id="f7403-171">Valige puult Intrastat \ Andmed \ Kogusummad plokkide alusel \ Ridade loendamine.</span><span class="sxs-lookup"><span data-stu-id="f7403-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="f7403-172">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="f7403-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="f7403-173">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="f7403-173">Click Edit formula.</span></span>
    * <span data-ttu-id="f7403-174">Looge iga selles aruandes esitatud ploki ridade arvu kohta väljund.</span><span class="sxs-lookup"><span data-stu-id="f7403-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="f7403-175">Sisestage väljale Valem „"Number of lines in this block: " & ”.</span><span class="sxs-lookup"><span data-stu-id="f7403-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="f7403-176">"Number of lines in this block: " &</span><span class="sxs-lookup"><span data-stu-id="f7403-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="f7403-177">Sisestage väljale Valem "Number of lines in this block: " & TEXT(.</span><span class="sxs-lookup"><span data-stu-id="f7403-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="f7403-178">"Number of lines in this block: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="f7403-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="f7403-179">Valige puult Andmekogumi funktsioonid \ COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="f7403-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="f7403-180">Klõpsake suvandit Funktsiooni lisamine.</span><span class="sxs-lookup"><span data-stu-id="f7403-180">Click Add function.</span></span>
59. <span data-ttu-id="f7403-181">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="f7403-181">Click Add data source.</span></span>
60. <span data-ttu-id="f7403-182">Sisestage väljale Valem "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="f7403-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="f7403-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="f7403-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="f7403-184">Laiendage puul väärtust $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="f7403-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="f7403-185">Valige puult $BlocksList\Väärtus.</span><span class="sxs-lookup"><span data-stu-id="f7403-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="f7403-186">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="f7403-186">Click Add data source.</span></span>
64. <span data-ttu-id="f7403-187">Sisestage väljale Valem "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="f7403-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="f7403-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="f7403-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="f7403-189">Valige puul väärtus $RecName.</span><span class="sxs-lookup"><span data-stu-id="f7403-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="f7403-190">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="f7403-190">Click Add data source.</span></span>
67. <span data-ttu-id="f7403-191">Sisestage väljale Valem "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*")).</span><span class="sxs-lookup"><span data-stu-id="f7403-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="f7403-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="f7403-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="f7403-193">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f7403-193">Click Save.</span></span>
69. <span data-ttu-id="f7403-194">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7403-194">Close the page.</span></span>
70. <span data-ttu-id="f7403-195">Klõpsake vahekaarti Vorming.</span><span class="sxs-lookup"><span data-stu-id="f7403-195">Click the Format tab.</span></span>
71. <span data-ttu-id="f7403-196">Valige puult Intrastat \ Andmed \ Kogusummad plokkide alusel \ Kogusumma.</span><span class="sxs-lookup"><span data-stu-id="f7403-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="f7403-197">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="f7403-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="f7403-198">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="f7403-198">Click Edit formula.</span></span>
    * <span data-ttu-id="f7403-199">Looge väljund, mis on iga selles aruandes esitatud ploki arveldatud summa koguväärtus.</span><span class="sxs-lookup"><span data-stu-id="f7403-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="f7403-200">Sisestage väljale Valem "Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*")).</span><span class="sxs-lookup"><span data-stu-id="f7403-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="f7403-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="f7403-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="f7403-202">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f7403-202">Click Save.</span></span>
76. <span data-ttu-id="f7403-203">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7403-203">Close the page.</span></span>
77. <span data-ttu-id="f7403-204">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f7403-204">Click Save.</span></span>
78. <span data-ttu-id="f7403-205">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7403-205">Close the page.</span></span>
