--- 
title: "Elektroonilise aruandluse (ER) arvutuste konfigureerimine loendamise ja liitmise väljundi loomiseks"
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 143856f65eaf1d6d667f4f7dfb229807da6f4ad8
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="use-computations-to-make-the-output-for-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="02d1d-103">Elektroonilise aruandluse (ER) arvutuste konfigureerimine loendamise ja liitmise väljundi loomiseks</span><span class="sxs-lookup"><span data-stu-id="02d1d-103">Use computations to make the output for counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="02d1d-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="02d1d-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="02d1d-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="02d1d-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="02d1d-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Vormingu konfigureerimine loendamiseks ja liitmiseks (2. osa: arvutuste konfigureerimine).</span><span class="sxs-lookup"><span data-stu-id="02d1d-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="02d1d-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="02d1d-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="02d1d-108">Selle aruande konfigureerimine loendamise ja liitmise teabe kasutamiseks</span><span class="sxs-lookup"><span data-stu-id="02d1d-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="02d1d-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="02d1d-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="02d1d-110">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="02d1d-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="02d1d-111">Laiendage puul valikut Intrastati mudel.</span><span class="sxs-lookup"><span data-stu-id="02d1d-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="02d1d-112">Laiendage puul valikut Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="02d1d-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="02d1d-113">Valige puult „Intrastati mudel\Intrastat (DE)\Intrastat (DE) koos loendamise ja liitmisega“.</span><span class="sxs-lookup"><span data-stu-id="02d1d-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="02d1d-114">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="02d1d-114">Click Designer.</span></span>
7. <span data-ttu-id="02d1d-115">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="02d1d-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="02d1d-116">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="02d1d-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="02d1d-117">Lisage uus andmeallikas meelde jäetud plokkide loendi saamiseks.</span><span class="sxs-lookup"><span data-stu-id="02d1d-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="02d1d-118">Valige puul suvand Funktsioonid\arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="02d1d-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="02d1d-119">Tippige $BlocksList väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="02d1d-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="02d1d-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="02d1d-120">$BlocksList</span></span>  
11. <span data-ttu-id="02d1d-121">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="02d1d-121">Click Edit formula.</span></span>
12. <span data-ttu-id="02d1d-122">Valige puult Andmekogumi funktsioonid \ COLLECTEDLIST.</span><span class="sxs-lookup"><span data-stu-id="02d1d-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="02d1d-123">Klõpsake suvandit Funktsiooni lisamine.</span><span class="sxs-lookup"><span data-stu-id="02d1d-123">Click Add function.</span></span>
14. <span data-ttu-id="02d1d-124">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="02d1d-124">Click Add data source.</span></span>
15. <span data-ttu-id="02d1d-125">Sisestage väljale Valem COLLECTEDLIST('$BlockName', .</span><span class="sxs-lookup"><span data-stu-id="02d1d-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="02d1d-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="02d1d-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="02d1d-127">Sisestage väljale Valem COLLECTEDLIST('$BlockName', "*").</span><span class="sxs-lookup"><span data-stu-id="02d1d-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "*")'.</span></span>
    * <span data-ttu-id="02d1d-128">COLLECTEDLIST('$BlockName', "*")</span><span class="sxs-lookup"><span data-stu-id="02d1d-128">COLLECTEDLIST('$BlockName', "*")</span></span>  
17. <span data-ttu-id="02d1d-129">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="02d1d-129">Click Save.</span></span>
    * <span data-ttu-id="02d1d-130">Muster „*” tähendab, et kõik plokid lisatakse selle kirje loendisse.</span><span class="sxs-lookup"><span data-stu-id="02d1d-130">The pattern “*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="02d1d-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="02d1d-131">Close the page.</span></span>
19. <span data-ttu-id="02d1d-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="02d1d-132">Click OK.</span></span>
20. <span data-ttu-id="02d1d-133">Klõpsake vahekaarti Vorming.</span><span class="sxs-lookup"><span data-stu-id="02d1d-133">Click the Format tab.</span></span>
21. <span data-ttu-id="02d1d-134">Tehke puul valik Intrastat \ Andmed.</span><span class="sxs-lookup"><span data-stu-id="02d1d-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="02d1d-135">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="02d1d-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="02d1d-136">Valige puult Tekst \ Seeria.</span><span class="sxs-lookup"><span data-stu-id="02d1d-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="02d1d-137">Tippige väljale Nimi valik Kogusummad plokkide alusel.</span><span class="sxs-lookup"><span data-stu-id="02d1d-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="02d1d-138">Kogusummad plokkide alusel</span><span class="sxs-lookup"><span data-stu-id="02d1d-138">Totals by blocks</span></span>  
25. <span data-ttu-id="02d1d-139">Valige väljal Erimärgid Uus rida – Windows (CR LF).</span><span class="sxs-lookup"><span data-stu-id="02d1d-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="02d1d-140">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="02d1d-140">Click OK.</span></span>
27. <span data-ttu-id="02d1d-141">Valige puult Intrastat \ Andmed \ Kogusummad plokkide alusel.</span><span class="sxs-lookup"><span data-stu-id="02d1d-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="02d1d-142">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="02d1d-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="02d1d-143">Valige puul suvand Tekst\String.</span><span class="sxs-lookup"><span data-stu-id="02d1d-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="02d1d-144">Tippige Ploki kood väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="02d1d-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="02d1d-145">Ploki kood</span><span class="sxs-lookup"><span data-stu-id="02d1d-145">Block code</span></span>  
31. <span data-ttu-id="02d1d-146">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="02d1d-146">Click OK.</span></span>
32. <span data-ttu-id="02d1d-147">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="02d1d-147">Click Add String.</span></span>
33. <span data-ttu-id="02d1d-148">Tippige väljale Nimi valik Ridade loendamine.</span><span class="sxs-lookup"><span data-stu-id="02d1d-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="02d1d-149">Ridade loendamine</span><span class="sxs-lookup"><span data-stu-id="02d1d-149">Lines counting</span></span>  
34. <span data-ttu-id="02d1d-150">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="02d1d-150">Click OK.</span></span>
35. <span data-ttu-id="02d1d-151">Klõpsake käsku Lisa string.</span><span class="sxs-lookup"><span data-stu-id="02d1d-151">Click Add String.</span></span>
36. <span data-ttu-id="02d1d-152">Tippige väljale Nimi valik Kogusumma.</span><span class="sxs-lookup"><span data-stu-id="02d1d-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="02d1d-153">Kogusumma</span><span class="sxs-lookup"><span data-stu-id="02d1d-153">Total amount</span></span>  
37. <span data-ttu-id="02d1d-154">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="02d1d-154">Click OK.</span></span>
38. <span data-ttu-id="02d1d-155">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="02d1d-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="02d1d-156">Valige puul väärtus $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="02d1d-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="02d1d-157">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="02d1d-157">Click Bind.</span></span>
    * <span data-ttu-id="02d1d-158">Looge iga meelde jäetud ploki kohta kokkuvõtte rida.</span><span class="sxs-lookup"><span data-stu-id="02d1d-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="02d1d-159">Klõpsake vahekaarti Vorming.</span><span class="sxs-lookup"><span data-stu-id="02d1d-159">Click the Format tab.</span></span>
42. <span data-ttu-id="02d1d-160">Valige puult Intrastat \ Andmed \ Kogusummad plokkide alusel \ Ploki kood.</span><span class="sxs-lookup"><span data-stu-id="02d1d-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="02d1d-161">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="02d1d-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="02d1d-162">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="02d1d-162">Click Edit formula.</span></span>
45. <span data-ttu-id="02d1d-163">Sisestage väljale Valem tekst „"Block id: " & “.</span><span class="sxs-lookup"><span data-stu-id="02d1d-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="02d1d-164">"Block id: " &</span><span class="sxs-lookup"><span data-stu-id="02d1d-164">"Block id: " &</span></span>  
46. <span data-ttu-id="02d1d-165">Laiendage puul väärtust $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="02d1d-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="02d1d-166">Valige puult $BlocksList\Väärtus.</span><span class="sxs-lookup"><span data-stu-id="02d1d-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="02d1d-167">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="02d1d-167">Click Add data source.</span></span>
49. <span data-ttu-id="02d1d-168">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="02d1d-168">Click Save.</span></span>
50. <span data-ttu-id="02d1d-169">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="02d1d-169">Close the page.</span></span>
51. <span data-ttu-id="02d1d-170">Klõpsake vahekaarti Vorming.</span><span class="sxs-lookup"><span data-stu-id="02d1d-170">Click the Format tab.</span></span>
52. <span data-ttu-id="02d1d-171">Valige puult Intrastat \ Andmed \ Kogusummad plokkide alusel \ Ridade loendamine.</span><span class="sxs-lookup"><span data-stu-id="02d1d-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="02d1d-172">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="02d1d-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="02d1d-173">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="02d1d-173">Click Edit formula.</span></span>
    * <span data-ttu-id="02d1d-174">Looge iga selles aruandes esitatud ploki ridade arvu kohta väljund.</span><span class="sxs-lookup"><span data-stu-id="02d1d-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="02d1d-175">Sisestage väljale Valem „"Number of lines in this block: " & ”.</span><span class="sxs-lookup"><span data-stu-id="02d1d-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="02d1d-176">"Number of lines in this block: " &</span><span class="sxs-lookup"><span data-stu-id="02d1d-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="02d1d-177">Sisestage väljale Valem "Number of lines in this block: " & TEXT(.</span><span class="sxs-lookup"><span data-stu-id="02d1d-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="02d1d-178">"Number of lines in this block: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="02d1d-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="02d1d-179">Valige puult Andmekogumi funktsioonid \ COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="02d1d-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="02d1d-180">Klõpsake suvandit Funktsiooni lisamine.</span><span class="sxs-lookup"><span data-stu-id="02d1d-180">Click Add function.</span></span>
59. <span data-ttu-id="02d1d-181">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="02d1d-181">Click Add data source.</span></span>
60. <span data-ttu-id="02d1d-182">Sisestage väljale Valem "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="02d1d-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="02d1d-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="02d1d-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="02d1d-184">Laiendage puul väärtust $BlocksList.</span><span class="sxs-lookup"><span data-stu-id="02d1d-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="02d1d-185">Valige puult $BlocksList\Väärtus.</span><span class="sxs-lookup"><span data-stu-id="02d1d-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="02d1d-186">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="02d1d-186">Click Add data source.</span></span>
64. <span data-ttu-id="02d1d-187">Sisestage väljale Valem "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="02d1d-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="02d1d-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="02d1d-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="02d1d-189">Valige puul väärtus $RecName.</span><span class="sxs-lookup"><span data-stu-id="02d1d-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="02d1d-190">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="02d1d-190">Click Add data source.</span></span>
67. <span data-ttu-id="02d1d-191">Sisestage väljale Valem "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*")).</span><span class="sxs-lookup"><span data-stu-id="02d1d-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.</span></span>
    * <span data-ttu-id="02d1d-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span><span class="sxs-lookup"><span data-stu-id="02d1d-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span></span>  
68. <span data-ttu-id="02d1d-193">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="02d1d-193">Click Save.</span></span>
69. <span data-ttu-id="02d1d-194">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="02d1d-194">Close the page.</span></span>
70. <span data-ttu-id="02d1d-195">Klõpsake vahekaarti Vorming.</span><span class="sxs-lookup"><span data-stu-id="02d1d-195">Click the Format tab.</span></span>
71. <span data-ttu-id="02d1d-196">Valige puult Intrastat \ Andmed \ Kogusummad plokkide alusel \ Kogusumma.</span><span class="sxs-lookup"><span data-stu-id="02d1d-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="02d1d-197">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="02d1d-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="02d1d-198">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="02d1d-198">Click Edit formula.</span></span>
    * <span data-ttu-id="02d1d-199">Looge väljund, mis on iga selles aruandes esitatud ploki arveldatud summa koguväärtus.</span><span class="sxs-lookup"><span data-stu-id="02d1d-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="02d1d-200">Sisestage väljale Valem "Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*")).</span><span class="sxs-lookup"><span data-stu-id="02d1d-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.</span></span>
    * <span data-ttu-id="02d1d-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span><span class="sxs-lookup"><span data-stu-id="02d1d-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span></span>  
75. <span data-ttu-id="02d1d-202">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="02d1d-202">Click Save.</span></span>
76. <span data-ttu-id="02d1d-203">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="02d1d-203">Close the page.</span></span>
77. <span data-ttu-id="02d1d-204">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="02d1d-204">Click Save.</span></span>
78. <span data-ttu-id="02d1d-205">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="02d1d-205">Close the page.</span></span>


