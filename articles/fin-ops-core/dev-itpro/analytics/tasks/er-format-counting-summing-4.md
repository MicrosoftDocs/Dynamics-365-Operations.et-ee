---
title: Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (4. osa – vormingu käivitamine)
description: Selles teemas kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse vormingut juba loodud tekstiväljundi andmete põhjal loendama ja liitma. (4. osa)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ca8449581edc06016b6e387880aad91087b67f1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565413"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="a420f-104">Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (4. osa – vormingu käivitamine)</span><span class="sxs-lookup"><span data-stu-id="a420f-104">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a420f-105">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="a420f-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="a420f-106">Neid toiminguid saab teha DEMF ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="a420f-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="a420f-107">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Vormingu konfigureerimine loendamiseks ja liitmiseks (3. osa: arvutuste kasutamine väljundi koostamiseks).</span><span class="sxs-lookup"><span data-stu-id="a420f-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="a420f-108">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="a420f-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="a420f-109">Proovige seda konfiguratsiooni intrastati aruannete koostamiseks</span><span class="sxs-lookup"><span data-stu-id="a420f-109">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="a420f-110">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="a420f-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a420f-111">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="a420f-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="a420f-112">Laiendage puul valikut Intrastati mudel.</span><span class="sxs-lookup"><span data-stu-id="a420f-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="a420f-113">Laiendage puul valikut Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="a420f-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="a420f-114">Valige puult „Intrastati mudel\Intrastat (DE)\Intrastat (DE) koos loendamise ja liitmisega“.</span><span class="sxs-lookup"><span data-stu-id="a420f-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="a420f-115">Klõpsake tegumiribal valikut Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="a420f-115">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="a420f-116">Klõpsake valikut Kasutaja parameetrid.</span><span class="sxs-lookup"><span data-stu-id="a420f-116">Click User parameters.</span></span>
8. <span data-ttu-id="a420f-117">Tehke väljal Käivita sätted valik Jah.</span><span class="sxs-lookup"><span data-stu-id="a420f-117">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="a420f-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a420f-118">Click OK.</span></span>
10. <span data-ttu-id="a420f-119">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="a420f-119">Click Edit.</span></span>
11. <span data-ttu-id="a420f-120">Tehke väljal Käivita mustand valik Jah.</span><span class="sxs-lookup"><span data-stu-id="a420f-120">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="a420f-121">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a420f-121">Click Save.</span></span>
13. <span data-ttu-id="a420f-122">Minge jaotisse Maks > Seadistus > Väliskaubandus > Väliskaubanduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="a420f-122">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="a420f-123">Laiendage jaotist Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="a420f-123">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="a420f-124">Valige konfiguratsioon „Intrastat (DE) koos loendamise ja liitmisega”.</span><span class="sxs-lookup"><span data-stu-id="a420f-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="a420f-125">Valige konfiguratsioon „Intrastat (DE) koos loendamise ja liitmisega”.</span><span class="sxs-lookup"><span data-stu-id="a420f-125">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="a420f-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a420f-126">Click Save.</span></span>
18. <span data-ttu-id="a420f-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a420f-127">Close the page.</span></span>
19. <span data-ttu-id="a420f-128">Avage Maks > Deklaratsioonid > Väliskaubandus > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="a420f-128">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="a420f-129">Klõpsake suvandit Väljund.</span><span class="sxs-lookup"><span data-stu-id="a420f-129">Click Output.</span></span>
21. <span data-ttu-id="a420f-130">Klõpsake vahekaarti Aruanne.</span><span class="sxs-lookup"><span data-stu-id="a420f-130">Click Report.</span></span>
    * <span data-ttu-id="a420f-131">Käivitage intrastati aruande koostamise protsess.</span><span class="sxs-lookup"><span data-stu-id="a420f-131">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="a420f-132">Määrake väljal Alguskuupäev kuupäevaks 2000/01/01.</span><span class="sxs-lookup"><span data-stu-id="a420f-132">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="a420f-133">Määratlege aruandeperioodi algus- ja lõpukuupäevad, mis hõlmavad vormil olevaid kandeid.</span><span class="sxs-lookup"><span data-stu-id="a420f-133">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="a420f-134">Määrake väljal Lõppkuupäev kuupäevaks 31.12.2022.</span><span class="sxs-lookup"><span data-stu-id="a420f-134">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="a420f-135">Määratlege aruandeperioodi algus- ja lõpukuupäevad, mis hõlmavad vormil olevaid kandeid.</span><span class="sxs-lookup"><span data-stu-id="a420f-135">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="a420f-136">Valige Saabumised väljalt Suund.</span><span class="sxs-lookup"><span data-stu-id="a420f-136">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="a420f-137">Valige Jah väljal Loo fail.</span><span class="sxs-lookup"><span data-stu-id="a420f-137">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="a420f-138">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a420f-138">Click OK.</span></span>
    * <span data-ttu-id="a420f-139">Vaadake loodud väljund ja lõpus olevad kokkuvõtteread üle.</span><span class="sxs-lookup"><span data-stu-id="a420f-139">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="a420f-140">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a420f-140">Click New.</span></span>
28. <span data-ttu-id="a420f-141">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="a420f-141">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="a420f-142">Valige Lähetused väljalt Suund.</span><span class="sxs-lookup"><span data-stu-id="a420f-142">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="a420f-143">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="a420f-143">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="a420f-144">Sisestage või valige väärtus väljal Kaup.</span><span class="sxs-lookup"><span data-stu-id="a420f-144">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="a420f-145">Määrake valiku Kaal väärtuseks 10.</span><span class="sxs-lookup"><span data-stu-id="a420f-145">Set Weight to '10'.</span></span>
33. <span data-ttu-id="a420f-146">Määrake valiku Arve summa väärtuseks 10 000.</span><span class="sxs-lookup"><span data-stu-id="a420f-146">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="a420f-147">Määrake valiku Statistiline summa väärtuseks 10 000.</span><span class="sxs-lookup"><span data-stu-id="a420f-147">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="a420f-148">Klõpsake suvandit Väljund.</span><span class="sxs-lookup"><span data-stu-id="a420f-148">Click Output.</span></span>
36. <span data-ttu-id="a420f-149">Klõpsake vahekaarti Aruanne.</span><span class="sxs-lookup"><span data-stu-id="a420f-149">Click Report.</span></span>
37. <span data-ttu-id="a420f-150">Valige Lähetused väljalt Suund.</span><span class="sxs-lookup"><span data-stu-id="a420f-150">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="a420f-151">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a420f-151">Click OK.</span></span>
    * <span data-ttu-id="a420f-152">Vaadake loodud väljund ja lõpus olevad kokkuvõtteread üle.</span><span class="sxs-lookup"><span data-stu-id="a420f-152">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="a420f-153">Pange tähele, et seda on esimese tsükliga võrreldes muudetud.</span><span class="sxs-lookup"><span data-stu-id="a420f-153">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="a420f-154">Käivitage konfiguratsioon silumisrežiimis kogutud loendamise ja liitmise andmete ülevaatamiseks</span><span class="sxs-lookup"><span data-stu-id="a420f-154">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="a420f-155">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="a420f-155">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a420f-156">Laiendage puul valikut Intrastati mudel.</span><span class="sxs-lookup"><span data-stu-id="a420f-156">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="a420f-157">Laiendage puul valikut Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="a420f-157">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="a420f-158">Valige puult „Intrastati mudel\Intrastat (DE)\Intrastat (DE) koos loendamise ja liitmisega“.</span><span class="sxs-lookup"><span data-stu-id="a420f-158">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="a420f-159">Klõpsake tegumiribal valikut Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="a420f-159">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="a420f-160">Klõpsake valikut Kasutaja parameetrid.</span><span class="sxs-lookup"><span data-stu-id="a420f-160">Click User parameters.</span></span>
7. <span data-ttu-id="a420f-161">Valige välja Käivita silumisrežiimis väärtuseks Jah.</span><span class="sxs-lookup"><span data-stu-id="a420f-161">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="a420f-162">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a420f-162">Click OK.</span></span>
9. <span data-ttu-id="a420f-163">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a420f-163">Close the page.</span></span>
10. <span data-ttu-id="a420f-164">Avage Maks > Deklaratsioonid > Väliskaubandus > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="a420f-164">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="a420f-165">Klõpsake suvandit Väljund.</span><span class="sxs-lookup"><span data-stu-id="a420f-165">Click Output.</span></span>
12. <span data-ttu-id="a420f-166">Klõpsake vahekaarti Aruanne.</span><span class="sxs-lookup"><span data-stu-id="a420f-166">Click Report.</span></span>
13. <span data-ttu-id="a420f-167">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a420f-167">Click OK.</span></span>
14. <span data-ttu-id="a420f-168">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a420f-168">Close the page.</span></span>
15. <span data-ttu-id="a420f-169">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="a420f-169">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="a420f-170">Laiendage puul valikut Intrastati mudel.</span><span class="sxs-lookup"><span data-stu-id="a420f-170">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="a420f-171">Laiendage puul valikut Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="a420f-171">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="a420f-172">Valige puult „Intrastati mudel\Intrastat (DE)\Intrastat (DE) koos loendamise ja liitmisega“.</span><span class="sxs-lookup"><span data-stu-id="a420f-172">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="a420f-173">Klõpsake nuppu Silumislogid.</span><span class="sxs-lookup"><span data-stu-id="a420f-173">Click Debug logs.</span></span>
    * <span data-ttu-id="a420f-174">Pange tähele, et valitud konfiguratsiooni käivitamiseks on loodud siluri logikirje.</span><span class="sxs-lookup"><span data-stu-id="a420f-174">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="a420f-175">Klõpsake suvandit Manusta.</span><span class="sxs-lookup"><span data-stu-id="a420f-175">Click Attach.</span></span>
21. <span data-ttu-id="a420f-176">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="a420f-176">Click Open.</span></span>
    * <span data-ttu-id="a420f-177">Vaadake üle loodud XML-fail, mis sisaldab valitud konfiguratsiooni käitamise ajal kogutud loendamise ja liitmise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="a420f-177">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]