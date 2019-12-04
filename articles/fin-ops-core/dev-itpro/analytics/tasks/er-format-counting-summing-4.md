---
title: Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (4. osa – vormingu käivitamine)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0a80e5b1a79c874ce0a8d24c85be71d0dc5c9c8
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550552"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="2f444-103">Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (4. osa – vormingu käivitamine)</span><span class="sxs-lookup"><span data-stu-id="2f444-103">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2f444-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="2f444-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="2f444-105">Neid toiminguid saab teha DEMF ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="2f444-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="2f444-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Vormingu konfigureerimine loendamiseks ja liitmiseks (3. osa: arvutuste kasutamine väljundi koostamiseks).</span><span class="sxs-lookup"><span data-stu-id="2f444-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="2f444-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="2f444-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="2f444-108">Proovige seda konfiguratsiooni intrastati aruannete koostamiseks</span><span class="sxs-lookup"><span data-stu-id="2f444-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="2f444-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="2f444-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="2f444-110">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="2f444-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="2f444-111">Laiendage puul valikut Intrastati mudel.</span><span class="sxs-lookup"><span data-stu-id="2f444-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="2f444-112">Laiendage puul valikut Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="2f444-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="2f444-113">Valige puult „Intrastati mudel\Intrastat (DE)\Intrastat (DE) koos loendamise ja liitmisega“.</span><span class="sxs-lookup"><span data-stu-id="2f444-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="2f444-114">Klõpsake tegumiribal valikut Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="2f444-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="2f444-115">Klõpsake valikut Kasutaja parameetrid.</span><span class="sxs-lookup"><span data-stu-id="2f444-115">Click User parameters.</span></span>
8. <span data-ttu-id="2f444-116">Tehke väljal Käivita sätted valik Jah.</span><span class="sxs-lookup"><span data-stu-id="2f444-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="2f444-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2f444-117">Click OK.</span></span>
10. <span data-ttu-id="2f444-118">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="2f444-118">Click Edit.</span></span>
11. <span data-ttu-id="2f444-119">Tehke väljal Käivita mustand valik Jah.</span><span class="sxs-lookup"><span data-stu-id="2f444-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="2f444-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2f444-120">Click Save.</span></span>
13. <span data-ttu-id="2f444-121">Minge jaotisse Maks > Seadistus > Väliskaubandus > Väliskaubanduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="2f444-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="2f444-122">Laiendage jaotist Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="2f444-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="2f444-123">Valige konfiguratsioon „Intrastat (DE) koos loendamise ja liitmisega”.</span><span class="sxs-lookup"><span data-stu-id="2f444-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="2f444-124">Valige konfiguratsioon „Intrastat (DE) koos loendamise ja liitmisega”.</span><span class="sxs-lookup"><span data-stu-id="2f444-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="2f444-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2f444-125">Click Save.</span></span>
18. <span data-ttu-id="2f444-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2f444-126">Close the page.</span></span>
19. <span data-ttu-id="2f444-127">Avage Maks > Deklaratsioonid > Väliskaubandus > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="2f444-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="2f444-128">Klõpsake suvandit Väljund.</span><span class="sxs-lookup"><span data-stu-id="2f444-128">Click Output.</span></span>
21. <span data-ttu-id="2f444-129">Klõpsake vahekaarti Aruanne.</span><span class="sxs-lookup"><span data-stu-id="2f444-129">Click Report.</span></span>
    * <span data-ttu-id="2f444-130">Käivitage intrastati aruande koostamise protsess.</span><span class="sxs-lookup"><span data-stu-id="2f444-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="2f444-131">Määrake väljal Alguskuupäev kuupäevaks 2000/01/01.</span><span class="sxs-lookup"><span data-stu-id="2f444-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="2f444-132">Määratlege aruandeperioodi algus- ja lõpukuupäevad, mis hõlmavad vormil olevaid kandeid.</span><span class="sxs-lookup"><span data-stu-id="2f444-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="2f444-133">Määrake väljal Lõppkuupäev kuupäevaks 31.12.2022.</span><span class="sxs-lookup"><span data-stu-id="2f444-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="2f444-134">Määratlege aruandeperioodi algus- ja lõpukuupäevad, mis hõlmavad vormil olevaid kandeid.</span><span class="sxs-lookup"><span data-stu-id="2f444-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="2f444-135">Valige Saabumised väljalt Suund.</span><span class="sxs-lookup"><span data-stu-id="2f444-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="2f444-136">Valige Jah väljal Loo fail.</span><span class="sxs-lookup"><span data-stu-id="2f444-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="2f444-137">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2f444-137">Click OK.</span></span>
    * <span data-ttu-id="2f444-138">Vaadake loodud väljund ja lõpus olevad kokkuvõtteread üle.</span><span class="sxs-lookup"><span data-stu-id="2f444-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="2f444-139">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2f444-139">Click New.</span></span>
28. <span data-ttu-id="2f444-140">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="2f444-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="2f444-141">Valige Lähetused väljalt Suund.</span><span class="sxs-lookup"><span data-stu-id="2f444-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="2f444-142">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="2f444-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="2f444-143">Sisestage või valige väärtus väljal Kaup.</span><span class="sxs-lookup"><span data-stu-id="2f444-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="2f444-144">Määrake valiku Kaal väärtuseks 10.</span><span class="sxs-lookup"><span data-stu-id="2f444-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="2f444-145">Määrake valiku Arve summa väärtuseks 10 000.</span><span class="sxs-lookup"><span data-stu-id="2f444-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="2f444-146">Määrake valiku Statistiline summa väärtuseks 10 000.</span><span class="sxs-lookup"><span data-stu-id="2f444-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="2f444-147">Klõpsake suvandit Väljund.</span><span class="sxs-lookup"><span data-stu-id="2f444-147">Click Output.</span></span>
36. <span data-ttu-id="2f444-148">Klõpsake vahekaarti Aruanne.</span><span class="sxs-lookup"><span data-stu-id="2f444-148">Click Report.</span></span>
37. <span data-ttu-id="2f444-149">Valige Lähetused väljalt Suund.</span><span class="sxs-lookup"><span data-stu-id="2f444-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="2f444-150">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2f444-150">Click OK.</span></span>
    * <span data-ttu-id="2f444-151">Vaadake loodud väljund ja lõpus olevad kokkuvõtteread üle.</span><span class="sxs-lookup"><span data-stu-id="2f444-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="2f444-152">Pange tähele, et seda on esimese tsükliga võrreldes muudetud.</span><span class="sxs-lookup"><span data-stu-id="2f444-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="2f444-153">Käivitage konfiguratsioon silumisrežiimis kogutud loendamise ja liitmise andmete ülevaatamiseks</span><span class="sxs-lookup"><span data-stu-id="2f444-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="2f444-154">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="2f444-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="2f444-155">Laiendage puul valikut Intrastati mudel.</span><span class="sxs-lookup"><span data-stu-id="2f444-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="2f444-156">Laiendage puul valikut Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="2f444-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="2f444-157">Valige puult „Intrastati mudel\Intrastat (DE)\Intrastat (DE) koos loendamise ja liitmisega“.</span><span class="sxs-lookup"><span data-stu-id="2f444-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="2f444-158">Klõpsake tegumiribal valikut Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="2f444-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="2f444-159">Klõpsake valikut Kasutaja parameetrid.</span><span class="sxs-lookup"><span data-stu-id="2f444-159">Click User parameters.</span></span>
7. <span data-ttu-id="2f444-160">Valige välja Käivita silumisrežiimis väärtuseks Jah.</span><span class="sxs-lookup"><span data-stu-id="2f444-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="2f444-161">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2f444-161">Click OK.</span></span>
9. <span data-ttu-id="2f444-162">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2f444-162">Close the page.</span></span>
10. <span data-ttu-id="2f444-163">Avage Maks > Deklaratsioonid > Väliskaubandus > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="2f444-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="2f444-164">Klõpsake suvandit Väljund.</span><span class="sxs-lookup"><span data-stu-id="2f444-164">Click Output.</span></span>
12. <span data-ttu-id="2f444-165">Klõpsake vahekaarti Aruanne.</span><span class="sxs-lookup"><span data-stu-id="2f444-165">Click Report.</span></span>
13. <span data-ttu-id="2f444-166">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2f444-166">Click OK.</span></span>
14. <span data-ttu-id="2f444-167">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2f444-167">Close the page.</span></span>
15. <span data-ttu-id="2f444-168">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="2f444-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="2f444-169">Laiendage puul valikut Intrastati mudel.</span><span class="sxs-lookup"><span data-stu-id="2f444-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="2f444-170">Laiendage puul valikut Intrastati mudel \ Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="2f444-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="2f444-171">Valige puult „Intrastati mudel\Intrastat (DE)\Intrastat (DE) koos loendamise ja liitmisega“.</span><span class="sxs-lookup"><span data-stu-id="2f444-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="2f444-172">Klõpsake nuppu Silumislogid.</span><span class="sxs-lookup"><span data-stu-id="2f444-172">Click Debug logs.</span></span>
    * <span data-ttu-id="2f444-173">Pange tähele, et valitud konfiguratsiooni käivitamiseks on loodud siluri logikirje.</span><span class="sxs-lookup"><span data-stu-id="2f444-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="2f444-174">Klõpsake suvandit Manusta.</span><span class="sxs-lookup"><span data-stu-id="2f444-174">Click Attach.</span></span>
21. <span data-ttu-id="2f444-175">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="2f444-175">Click Open.</span></span>
    * <span data-ttu-id="2f444-176">Vaadake üle loodud XML-fail, mis sisaldab valitud konfiguratsiooni käitamise ajal kogutud loendamise ja liitmise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="2f444-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  
