---
title: Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (2. osa – arvutuste konfigureerimine)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal.
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
ms.openlocfilehash: 9314a8cd5838333a20dd59dfb52f80a43d89b8c6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684687"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="5a2c6-103">Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (2. osa – arvutuste konfigureerimine)</span><span class="sxs-lookup"><span data-stu-id="5a2c6-103">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5a2c6-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="5a2c6-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="5a2c6-106">Nende etappide lõpule viimiseks peate esmalt viima lõpule etapid protseduuris „Elektrooniline aruandlus Vormingu konfigureerimine loendamiseks ja liitmiseks (1. osa: vormingu loomine)”.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-106">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="5a2c6-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="5a2c6-108">Vormingukonfiguratsiooni loomine loendamise ja liitmise üksikasjade lisamiseks</span><span class="sxs-lookup"><span data-stu-id="5a2c6-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="5a2c6-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="5a2c6-110">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="5a2c6-111">Laiendage puul valikut Intrastati mudel.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="5a2c6-112">Valige puult Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="5a2c6-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="5a2c6-113">Oletame, et teil on vaja kohandada Microsofti antud vormingut, lisades intrastati aruande lõppu ridu kokkuvõtte andmetega.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="5a2c6-114">Muudatuste tegemiseks tuleb seda teha, tuletades oma intrastati konfiguratsiooni eksemplari Microsofti eksemplarist.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="5a2c6-115">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="5a2c6-116">Sisestage väljale Uus üksus Tuleta nimest: intrastat (DE), Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="5a2c6-117">Tippige väljale Nimi tekst „Intrastat (DE) koos loendamise ja liitmisega“.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="5a2c6-118">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="5a2c6-119">Saate konfigureerida selle aruande nii, et loendamine ja liitmine toimub väljundi andmete põhjal</span><span class="sxs-lookup"><span data-stu-id="5a2c6-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="5a2c6-120">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-120">Click Designer.</span></span>
2. <span data-ttu-id="5a2c6-121">Tehke väljal Kogu väljundi üksikasjad valik Jah.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="5a2c6-122">See lipp aktiveerib käitusajal väljundi üksikasjade kogumise protsessi intrastati faili loomiseks.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="5a2c6-123">Loendamine peab toimuma erinevate Intrastati suundade kohta, seega lisage spetsiaalne mudeli loetelu selle vormingukonfiguratsiooni andmeallikate loendile.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="5a2c6-124">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="5a2c6-125">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="5a2c6-126">Valige puul väärtus Andmemudel \ Loetelu.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="5a2c6-127">Tippige Suund väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="5a2c6-128">Sisestage või valige väärtus väljal Mudeli loetelu.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="5a2c6-129">Valige väärtuseks Suund.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="5a2c6-130">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-130">Click OK.</span></span>
9. <span data-ttu-id="5a2c6-131">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="5a2c6-132">Valige puul suvand Funktsioonid\arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="5a2c6-133">Tippige $BlockName väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="5a2c6-134">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-134">Click Edit formula.</span></span>
13. <span data-ttu-id="5a2c6-135">Sisestage „plokk” väljale Valem.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="5a2c6-136">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-136">Click Save.</span></span>
15. <span data-ttu-id="5a2c6-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-137">Close the page.</span></span>
16. <span data-ttu-id="5a2c6-138">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-138">Click OK.</span></span>
17. <span data-ttu-id="5a2c6-139">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="5a2c6-140">Valige puul suvand Funktsioonid\arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="5a2c6-141">Tippige $RecName väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="5a2c6-142">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-142">Click Edit formula.</span></span>
21. <span data-ttu-id="5a2c6-143">Sisestage „kirje” väljale Valem.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="5a2c6-144">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-144">Click Save.</span></span>
23. <span data-ttu-id="5a2c6-145">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-145">Close the page.</span></span>
24. <span data-ttu-id="5a2c6-146">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-146">Click OK.</span></span>
25. <span data-ttu-id="5a2c6-147">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="5a2c6-148">Valige puul suvand Funktsioonid\arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="5a2c6-149">Tippige $InvName väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="5a2c6-150">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-150">Click Edit formula.</span></span>
29. <span data-ttu-id="5a2c6-151">Sisestage „InvoicedAmountEUR” väljale Valem.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="5a2c6-152">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-152">Click Save.</span></span>
31. <span data-ttu-id="5a2c6-153">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-153">Close the page.</span></span>
32. <span data-ttu-id="5a2c6-154">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-154">Click OK.</span></span>
33. <span data-ttu-id="5a2c6-155">Tehke puul valik Intrastat \ Andmed.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="5a2c6-156">Klõpsake välja „Kogutud andmete võtme nimi” nuppu Redigeeri</span><span class="sxs-lookup"><span data-stu-id="5a2c6-156">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="5a2c6-157">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-157">Click Add data source.</span></span>
    * <span data-ttu-id="5a2c6-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="5a2c6-158">$BlockName</span></span>  
36. <span data-ttu-id="5a2c6-159">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-159">Click Save.</span></span>
37. <span data-ttu-id="5a2c6-160">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-160">Close the page.</span></span>
38. <span data-ttu-id="5a2c6-161">Klõpsake välja Kogutud andmete võtme väärtus nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="5a2c6-162">Sisestage väljale valem IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export").</span><span class="sxs-lookup"><span data-stu-id="5a2c6-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="5a2c6-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="5a2c6-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="5a2c6-164">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-164">Click Save.</span></span>
41. <span data-ttu-id="5a2c6-165">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-165">Close the page.</span></span>
    * <span data-ttu-id="5a2c6-166">Loendage selle järjestuse ridade arv.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-166">Count the lines of this sequence.</span></span> <span data-ttu-id="5a2c6-167">Tulemusi kasutatakse nimega „plokk” erinevate suundade puhul eraldi.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-167">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="5a2c6-168">Väärtust „Import” kasutatakse igasuguste intrastati saabumiskannete puhul.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-168">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="5a2c6-169">Väärtust „Eksport” kasutatakse igasuguste intrastati lähetuskannete puhul.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-169">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="5a2c6-170">Vaadake seda kui virtuaalset Exceli arvutustabelit.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="5a2c6-171">Iga kande puhul täidetakse rida, mille esimene veerg on „plokk”, vastavalt väärtustega „Import” ja „Eksport”.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-171">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="5a2c6-172">Laiendage puul valikut Intrastat \ Andmed: seeria.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="5a2c6-173">Valige puult Intrastat \ Andmed: seeria \ Saabumised?.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="5a2c6-174">Klõpsake välja „Kogutud andmete võtme nimi” nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-174">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="5a2c6-175">Loendage selle järjestuse ridade arv.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-175">Count the lines of this sequence.</span></span> <span data-ttu-id="5a2c6-176">Tulemused jäetakse meelde, kasutades nime „kirje”.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-176">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="5a2c6-177">Valige puul väärtus $RecName.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="5a2c6-178">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-178">Click Add data source.</span></span>
47. <span data-ttu-id="5a2c6-179">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-179">Click Save.</span></span>
48. <span data-ttu-id="5a2c6-180">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-180">Close the page.</span></span>
49. <span data-ttu-id="5a2c6-181">Klõpsake välja „Kogutud andmete võtme väärtus ”nuppu Redigeeri</span><span class="sxs-lookup"><span data-stu-id="5a2c6-181">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="5a2c6-182">Sisestage väljale Valem Intrastat.CommodityRecord.CommodityCode.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="5a2c6-183">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-183">Click Save.</span></span>
52. <span data-ttu-id="5a2c6-184">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-184">Close the page.</span></span>
    * <span data-ttu-id="5a2c6-185">Loendage selle järjestuse ridade arv.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-185">Count the lines of this sequence.</span></span> <span data-ttu-id="5a2c6-186">Tulemusi kasutatakse nimega „kirje” erinevate kaubakoodide puhul eraldi.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-186">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="5a2c6-187">Vaadake seda kui virtuaalset Exceli arvutustabelit.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="5a2c6-188">Iga kande puhul täidetakse rida, mille esimene veerg on „plokk”, vastavalt väärtustega „Import” ja „Eksport” ja teine plokk „kirje” täidetakse kaubakoodi väärtusega.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-188">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="5a2c6-189">Valige puult Intrastat \ Andmed: seeria \ Lähetused?.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="5a2c6-190">Klõpsake välja „Kogutud andmete võtme nimi” nuppu Redigeeri</span><span class="sxs-lookup"><span data-stu-id="5a2c6-190">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="5a2c6-191">Valige puul väärtus $RecName.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="5a2c6-192">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-192">Click Add data source.</span></span>
57. <span data-ttu-id="5a2c6-193">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-193">Click Save.</span></span>
58. <span data-ttu-id="5a2c6-194">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-194">Close the page.</span></span>
59. <span data-ttu-id="5a2c6-195">Klõpsake välja „Kogutud andmete võtme väärtus” nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-195">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="5a2c6-196">Sisestage väljale Valem Intrastat.CommodityRecord.CommodityCode.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="5a2c6-197">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-197">Click Save.</span></span>
62. <span data-ttu-id="5a2c6-198">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-198">Close the page.</span></span>
63. <span data-ttu-id="5a2c6-199">Laiendage puul valikut Intrastat \ Andmed: seeria \ Lähetused: seeria?.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="5a2c6-200">Laiendage puul valikut Intrastat \ Andmed: seeria \ Lähetused: seeria? \ Kirje =  Intrastat.CommodityRecord.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="5a2c6-201">Klõpsake vahekaarti Vorming.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-201">Click the Format tab.</span></span>
66. <span data-ttu-id="5a2c6-202">Valige puult Intrastat \ Andmed \ Lähetused \ Kirje \ Arve summa EUR.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="5a2c6-203">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="5a2c6-204">Klõpsake välja „Kogutud andmete võtme nimi” nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-204">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="5a2c6-205">Valige puul väärtus $InvName.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="5a2c6-206">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-206">Click Add data source.</span></span>
71. <span data-ttu-id="5a2c6-207">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-207">Click Save.</span></span>
72. <span data-ttu-id="5a2c6-208">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-208">Close the page.</span></span>
    * <span data-ttu-id="5a2c6-209">Liitke selle järjestuse ridade arveldatud summade väärtused.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="5a2c6-210">Tulemusi kasutatakse nimega „InvoicedAmountEUR” erinevate intrastati suundade ja kaubakoodide puhul eraldi.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-210">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="5a2c6-211">Vaadake seda kui virtuaalset loomingut Exceli arvutustabelis.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="5a2c6-212">Iga kande puhul täidetakse rida, mille esimene veerg on „plokk”, vastavalt väärtustega „Import” ja „Eksport”.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-212">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="5a2c6-213">Teine plokk „kirje” täidetakse kaubakoodi väärtusega ja kolmas veerg „InvoicedAmountEUR” täidetakse arve summa väärtusega.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-213">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="5a2c6-214">Laiendage puul valikut Intrastat \ Andmed \ Saabumised?.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="5a2c6-215">Laiendage puul valikut Intrastat \ Andmed \ Saabumised? \ Kirje =  Intrastat.CommodityRecord.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="5a2c6-216">Klõpsake vahekaarti Vorming.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-216">Click the Format tab.</span></span>
76. <span data-ttu-id="5a2c6-217">Valige puult Intrastat \ Andmed \ Saabumised \ Kirje \ Arve summa EUR.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="5a2c6-218">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="5a2c6-219">Klõpsake välja „Kogutud andmete võtme nimi” nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-219">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="5a2c6-220">Valige puul väärtus $InvName.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="5a2c6-221">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-221">Click Add data source.</span></span>
81. <span data-ttu-id="5a2c6-222">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-222">Click Save.</span></span>
82. <span data-ttu-id="5a2c6-223">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-223">Close the page.</span></span>
83. <span data-ttu-id="5a2c6-224">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-224">Click Save.</span></span>
84. <span data-ttu-id="5a2c6-225">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5a2c6-225">Close the page.</span></span>

