---
title: Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (2. osa – arvutuste konfigureerimine)
description: Selles teemas kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse vormingut juba loodud tekstiväljundi andmete põhjal loendama ja liitma. (2. osa)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6215fe1f32bcb4833bd009b7c33e09edbba17817
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092993"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="52deb-104">Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (2. osa – arvutuste konfigureerimine)</span><span class="sxs-lookup"><span data-stu-id="52deb-104">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52deb-105">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="52deb-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="52deb-106">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="52deb-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="52deb-107">Nende etappide lõpule viimiseks peate esmalt viima lõpule etapid protseduuris „Elektrooniline aruandlus Vormingu konfigureerimine loendamiseks ja liitmiseks (1. osa: vormingu loomine)”.</span><span class="sxs-lookup"><span data-stu-id="52deb-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="52deb-108">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="52deb-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="52deb-109">Vormingukonfiguratsiooni loomine loendamise ja liitmise üksikasjade lisamiseks</span><span class="sxs-lookup"><span data-stu-id="52deb-109">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="52deb-110">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="52deb-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="52deb-111">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="52deb-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="52deb-112">Laiendage puul valikut Intrastati mudel.</span><span class="sxs-lookup"><span data-stu-id="52deb-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="52deb-113">Valige puult Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="52deb-113">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="52deb-114">Oletame, et teil on vaja kohandada Microsofti antud vormingut, lisades intrastati aruande lõppu ridu kokkuvõtte andmetega.</span><span class="sxs-lookup"><span data-stu-id="52deb-114">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="52deb-115">Muudatuste tegemiseks tuleb seda teha, tuletades oma intrastati konfiguratsiooni eksemplari Microsofti eksemplarist.</span><span class="sxs-lookup"><span data-stu-id="52deb-115">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="52deb-116">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="52deb-116">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="52deb-117">Sisestage väljale Uus üksus Tuleta nimest: intrastat (DE), Microsoft.</span><span class="sxs-lookup"><span data-stu-id="52deb-117">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="52deb-118">Tippige väljale Nimi tekst „Intrastat (DE) koos loendamise ja liitmisega“.</span><span class="sxs-lookup"><span data-stu-id="52deb-118">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="52deb-119">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="52deb-119">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="52deb-120">Saate konfigureerida selle aruande nii, et loendamine ja liitmine toimub väljundi andmete põhjal</span><span class="sxs-lookup"><span data-stu-id="52deb-120">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="52deb-121">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="52deb-121">Click Designer.</span></span>
2. <span data-ttu-id="52deb-122">Tehke väljal Kogu väljundi üksikasjad valik Jah.</span><span class="sxs-lookup"><span data-stu-id="52deb-122">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="52deb-123">See lipp aktiveerib käitusajal väljundi üksikasjade kogumise protsessi intrastati faili loomiseks.</span><span class="sxs-lookup"><span data-stu-id="52deb-123">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="52deb-124">Loendamine peab toimuma erinevate Intrastati suundade kohta, seega lisage spetsiaalne mudeli loetelu selle vormingukonfiguratsiooni andmeallikate loendile.</span><span class="sxs-lookup"><span data-stu-id="52deb-124">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="52deb-125">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="52deb-125">Click the Mapping tab.</span></span>
4. <span data-ttu-id="52deb-126">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="52deb-126">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="52deb-127">Valige puul väärtus Andmemudel \ Loetelu.</span><span class="sxs-lookup"><span data-stu-id="52deb-127">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="52deb-128">Tippige Suund väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="52deb-128">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="52deb-129">Sisestage või valige väärtus väljal Mudeli loetelu.</span><span class="sxs-lookup"><span data-stu-id="52deb-129">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="52deb-130">Valige väärtuseks Suund.</span><span class="sxs-lookup"><span data-stu-id="52deb-130">Select the value Direction.</span></span>  
8. <span data-ttu-id="52deb-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="52deb-131">Click OK.</span></span>
9. <span data-ttu-id="52deb-132">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="52deb-132">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="52deb-133">Valige puul suvand Funktsioonid\arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="52deb-133">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="52deb-134">Tippige $BlockName väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="52deb-134">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="52deb-135">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="52deb-135">Click Edit formula.</span></span>
13. <span data-ttu-id="52deb-136">Sisestage „plokk” väljale Valem.</span><span class="sxs-lookup"><span data-stu-id="52deb-136">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="52deb-137">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="52deb-137">Click Save.</span></span>
15. <span data-ttu-id="52deb-138">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="52deb-138">Close the page.</span></span>
16. <span data-ttu-id="52deb-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="52deb-139">Click OK.</span></span>
17. <span data-ttu-id="52deb-140">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="52deb-140">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="52deb-141">Valige puul suvand Funktsioonid\arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="52deb-141">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="52deb-142">Tippige $RecName väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="52deb-142">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="52deb-143">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="52deb-143">Click Edit formula.</span></span>
21. <span data-ttu-id="52deb-144">Sisestage „kirje” väljale Valem.</span><span class="sxs-lookup"><span data-stu-id="52deb-144">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="52deb-145">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="52deb-145">Click Save.</span></span>
23. <span data-ttu-id="52deb-146">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="52deb-146">Close the page.</span></span>
24. <span data-ttu-id="52deb-147">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="52deb-147">Click OK.</span></span>
25. <span data-ttu-id="52deb-148">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="52deb-148">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="52deb-149">Valige puul suvand Funktsioonid\arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="52deb-149">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="52deb-150">Tippige $InvName väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="52deb-150">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="52deb-151">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="52deb-151">Click Edit formula.</span></span>
29. <span data-ttu-id="52deb-152">Sisestage „InvoicedAmountEUR” väljale Valem.</span><span class="sxs-lookup"><span data-stu-id="52deb-152">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="52deb-153">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="52deb-153">Click Save.</span></span>
31. <span data-ttu-id="52deb-154">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="52deb-154">Close the page.</span></span>
32. <span data-ttu-id="52deb-155">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="52deb-155">Click OK.</span></span>
33. <span data-ttu-id="52deb-156">Tehke puul valik Intrastat \ Andmed.</span><span class="sxs-lookup"><span data-stu-id="52deb-156">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="52deb-157">Klõpsake välja „Kogutud andmete võtme nimi” nuppu Redigeeri</span><span class="sxs-lookup"><span data-stu-id="52deb-157">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="52deb-158">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="52deb-158">Click Add data source.</span></span>
    * <span data-ttu-id="52deb-159">$BlockName</span><span class="sxs-lookup"><span data-stu-id="52deb-159">$BlockName</span></span>  
36. <span data-ttu-id="52deb-160">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="52deb-160">Click Save.</span></span>
37. <span data-ttu-id="52deb-161">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="52deb-161">Close the page.</span></span>
38. <span data-ttu-id="52deb-162">Klõpsake välja Kogutud andmete võtme väärtus nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="52deb-162">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="52deb-163">Sisestage väljale valem IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export").</span><span class="sxs-lookup"><span data-stu-id="52deb-163">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="52deb-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="52deb-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="52deb-165">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="52deb-165">Click Save.</span></span>
41. <span data-ttu-id="52deb-166">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="52deb-166">Close the page.</span></span>
    * <span data-ttu-id="52deb-167">Loendage selle järjestuse ridade arv.</span><span class="sxs-lookup"><span data-stu-id="52deb-167">Count the lines of this sequence.</span></span> <span data-ttu-id="52deb-168">Tulemusi kasutatakse nimega „plokk” erinevate suundade puhul eraldi.</span><span class="sxs-lookup"><span data-stu-id="52deb-168">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="52deb-169">Väärtust „Import” kasutatakse igasuguste intrastati saabumiskannete puhul.</span><span class="sxs-lookup"><span data-stu-id="52deb-169">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="52deb-170">Väärtust „Eksport” kasutatakse igasuguste intrastati lähetuskannete puhul.</span><span class="sxs-lookup"><span data-stu-id="52deb-170">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="52deb-171">Vaadake seda kui virtuaalset Exceli arvutustabelit.</span><span class="sxs-lookup"><span data-stu-id="52deb-171">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="52deb-172">Iga kande puhul täidetakse rida, mille esimene veerg on „plokk”, vastavalt väärtustega „Import” ja „Eksport”.</span><span class="sxs-lookup"><span data-stu-id="52deb-172">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="52deb-173">Laiendage puul valikut Intrastat \ Andmed: seeria.</span><span class="sxs-lookup"><span data-stu-id="52deb-173">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="52deb-174">Valige puult Intrastat \ Andmed: seeria \ Saabumised?.</span><span class="sxs-lookup"><span data-stu-id="52deb-174">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="52deb-175">Klõpsake välja „Kogutud andmete võtme nimi” nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="52deb-175">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="52deb-176">Loendage selle järjestuse ridade arv.</span><span class="sxs-lookup"><span data-stu-id="52deb-176">Count the lines of this sequence.</span></span> <span data-ttu-id="52deb-177">Tulemused jäetakse meelde, kasutades nime „kirje”.</span><span class="sxs-lookup"><span data-stu-id="52deb-177">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="52deb-178">Valige puul väärtus $RecName.</span><span class="sxs-lookup"><span data-stu-id="52deb-178">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="52deb-179">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="52deb-179">Click Add data source.</span></span>
47. <span data-ttu-id="52deb-180">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="52deb-180">Click Save.</span></span>
48. <span data-ttu-id="52deb-181">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="52deb-181">Close the page.</span></span>
49. <span data-ttu-id="52deb-182">Klõpsake välja „Kogutud andmete võtme väärtus ”nuppu Redigeeri</span><span class="sxs-lookup"><span data-stu-id="52deb-182">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="52deb-183">Sisestage väljale Valem Intrastat.CommodityRecord.CommodityCode.</span><span class="sxs-lookup"><span data-stu-id="52deb-183">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="52deb-184">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="52deb-184">Click Save.</span></span>
52. <span data-ttu-id="52deb-185">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="52deb-185">Close the page.</span></span>
    * <span data-ttu-id="52deb-186">Loendage selle järjestuse ridade arv.</span><span class="sxs-lookup"><span data-stu-id="52deb-186">Count the lines of this sequence.</span></span> <span data-ttu-id="52deb-187">Tulemusi kasutatakse nimega „kirje” erinevate kaubakoodide puhul eraldi.</span><span class="sxs-lookup"><span data-stu-id="52deb-187">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="52deb-188">Vaadake seda kui virtuaalset Exceli arvutustabelit.</span><span class="sxs-lookup"><span data-stu-id="52deb-188">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="52deb-189">Iga kande puhul täidetakse rida, mille esimene veerg on „plokk”, vastavalt väärtustega „Import” ja „Eksport” ja teine plokk „kirje” täidetakse kaubakoodi väärtusega.</span><span class="sxs-lookup"><span data-stu-id="52deb-189">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="52deb-190">Valige puult Intrastat \ Andmed: seeria \ Lähetused?.</span><span class="sxs-lookup"><span data-stu-id="52deb-190">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="52deb-191">Klõpsake välja „Kogutud andmete võtme nimi” nuppu Redigeeri</span><span class="sxs-lookup"><span data-stu-id="52deb-191">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="52deb-192">Valige puul väärtus $RecName.</span><span class="sxs-lookup"><span data-stu-id="52deb-192">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="52deb-193">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="52deb-193">Click Add data source.</span></span>
57. <span data-ttu-id="52deb-194">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="52deb-194">Click Save.</span></span>
58. <span data-ttu-id="52deb-195">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="52deb-195">Close the page.</span></span>
59. <span data-ttu-id="52deb-196">Klõpsake välja „Kogutud andmete võtme väärtus” nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="52deb-196">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="52deb-197">Sisestage väljale Valem Intrastat.CommodityRecord.CommodityCode.</span><span class="sxs-lookup"><span data-stu-id="52deb-197">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="52deb-198">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="52deb-198">Click Save.</span></span>
62. <span data-ttu-id="52deb-199">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="52deb-199">Close the page.</span></span>
63. <span data-ttu-id="52deb-200">Laiendage puul valikut Intrastat \ Andmed: seeria \ Lähetused: seeria?.</span><span class="sxs-lookup"><span data-stu-id="52deb-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="52deb-201">Laiendage puul valikut Intrastat \ Andmed: seeria \ Lähetused: seeria? \ Kirje =  Intrastat.CommodityRecord.</span><span class="sxs-lookup"><span data-stu-id="52deb-201">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="52deb-202">Klõpsake vahekaarti Vorming.</span><span class="sxs-lookup"><span data-stu-id="52deb-202">Click the Format tab.</span></span>
66. <span data-ttu-id="52deb-203">Valige puult Intrastat \ Andmed \ Lähetused \ Kirje \ Arve summa EUR.</span><span class="sxs-lookup"><span data-stu-id="52deb-203">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="52deb-204">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="52deb-204">Click the Mapping tab.</span></span>
68. <span data-ttu-id="52deb-205">Klõpsake välja „Kogutud andmete võtme nimi” nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="52deb-205">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="52deb-206">Valige puul väärtus $InvName.</span><span class="sxs-lookup"><span data-stu-id="52deb-206">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="52deb-207">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="52deb-207">Click Add data source.</span></span>
71. <span data-ttu-id="52deb-208">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="52deb-208">Click Save.</span></span>
72. <span data-ttu-id="52deb-209">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="52deb-209">Close the page.</span></span>
    * <span data-ttu-id="52deb-210">Liitke selle järjestuse ridade arveldatud summade väärtused.</span><span class="sxs-lookup"><span data-stu-id="52deb-210">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="52deb-211">Tulemusi kasutatakse nimega „InvoicedAmountEUR” erinevate intrastati suundade ja kaubakoodide puhul eraldi.</span><span class="sxs-lookup"><span data-stu-id="52deb-211">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="52deb-212">Vaadake seda kui virtuaalset loomingut Exceli arvutustabelis.</span><span class="sxs-lookup"><span data-stu-id="52deb-212">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="52deb-213">Iga kande puhul täidetakse rida, mille esimene veerg on „plokk”, vastavalt väärtustega „Import” ja „Eksport”.</span><span class="sxs-lookup"><span data-stu-id="52deb-213">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="52deb-214">Teine plokk „kirje” täidetakse kaubakoodi väärtusega ja kolmas veerg „InvoicedAmountEUR” täidetakse arve summa väärtusega.</span><span class="sxs-lookup"><span data-stu-id="52deb-214">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="52deb-215">Laiendage puul valikut Intrastat \ Andmed \ Saabumised?.</span><span class="sxs-lookup"><span data-stu-id="52deb-215">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="52deb-216">Laiendage puul valikut Intrastat \ Andmed \ Saabumised? \ Kirje =  Intrastat.CommodityRecord.</span><span class="sxs-lookup"><span data-stu-id="52deb-216">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="52deb-217">Klõpsake vahekaarti Vorming.</span><span class="sxs-lookup"><span data-stu-id="52deb-217">Click the Format tab.</span></span>
76. <span data-ttu-id="52deb-218">Valige puult Intrastat \ Andmed \ Saabumised \ Kirje \ Arve summa EUR.</span><span class="sxs-lookup"><span data-stu-id="52deb-218">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="52deb-219">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="52deb-219">Click the Mapping tab.</span></span>
78. <span data-ttu-id="52deb-220">Klõpsake välja „Kogutud andmete võtme nimi” nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="52deb-220">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="52deb-221">Valige puul väärtus $InvName.</span><span class="sxs-lookup"><span data-stu-id="52deb-221">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="52deb-222">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="52deb-222">Click Add data source.</span></span>
81. <span data-ttu-id="52deb-223">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="52deb-223">Click Save.</span></span>
82. <span data-ttu-id="52deb-224">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="52deb-224">Close the page.</span></span>
83. <span data-ttu-id="52deb-225">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="52deb-225">Click Save.</span></span>
84. <span data-ttu-id="52deb-226">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="52deb-226">Close the page.</span></span>

