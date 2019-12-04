---
title: EUR-00002 ELi Intrastati deklaratsiooni loomine
description: Selles protseduuris selgitatakse vajalikke toiminguid Intrastati deklaratsiooni eksportimise kohta elektroonilises failivormingus ja deklaratsiooni andmete eelvaatamist Exceli vormingus.
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, IntrastatParameters, IntrastatCommodityLookup, IntrastatCompressParameters, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d7ab1d274b527bf5071900940bf53a57a88f482
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183598"
---
# <a name="eur-00002-generate-an-eu-intrastat-declaration"></a><span data-ttu-id="d6858-103">EUR-00002 ELi Intrastati deklaratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="d6858-103">EUR-00002 Generate an EU Intrastat declaration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d6858-104">Selles protseduuris selgitatakse vajalikke toiminguid Intrastati deklaratsiooni eksportimise kohta elektroonilises failivormingus ja deklaratsiooni andmete eelvaatamist Exceli vormingus.</span><span class="sxs-lookup"><span data-stu-id="d6858-104">This procedure walks you through the steps required to export the Intrastat declaration in the electronic file format and preview the declaration data in an Excel format.</span></span> 

<span data-ttu-id="d6858-105">Enne kui saate selle protseduuri lõpule viia, peate kandma kanded Intrastati.</span><span class="sxs-lookup"><span data-stu-id="d6858-105">Before you can complete this procedure, you must transfer transactions to the Intrastat.</span></span> 

<span data-ttu-id="d6858-106">Protseduuri loomisel kasutati demoettevõtte DEMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="d6858-106">This procedure was created using the demo data company DEMF.</span></span>


## <a name="import-configurations-with-settings"></a><span data-ttu-id="d6858-107">Konfiguratsioonide importimine sätetega</span><span class="sxs-lookup"><span data-stu-id="d6858-107">Import configurations with settings</span></span>
1. <span data-ttu-id="d6858-108">Avage Tööruumid > Elektrooniline aruandlus</span><span class="sxs-lookup"><span data-stu-id="d6858-108">Go to Workspaces > Electronic reporting</span></span>
2. <span data-ttu-id="d6858-109">Klõpsake valikut Määra aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="d6858-109">Click Set active.</span></span>
3. <span data-ttu-id="d6858-110">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="d6858-110">Click Repositories.</span></span>
4. <span data-ttu-id="d6858-111">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="d6858-111">Click Open.</span></span>
5. <span data-ttu-id="d6858-112">Avage veeru filter Konfiguratsiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="d6858-112">Open Configuration name column filter.</span></span>
6. <span data-ttu-id="d6858-113">Rakendage väljal Konfiguratsiooni nimi filtrit väärtusega Intrastat (DE), kasutades filtri tehtemärki „algab üksusega”.</span><span class="sxs-lookup"><span data-stu-id="d6858-113">Apply a filter on the "Configuration name" field, with a value of "Intrastat (DE)", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="d6858-114">Peate valima konfiguratsiooni nime, mis on rakendatav teie juriidilise isiku riigile.</span><span class="sxs-lookup"><span data-stu-id="d6858-114">You should select the configuration name applicable for the country of your legal entity.</span></span> <span data-ttu-id="d6858-115">Selles protseduuris kasutatakse näitena Saksamaa juriidilist isikut (DEMF), seetõttu tuleks teha valik Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="d6858-115">This procedure uses the German legal entity (DEMF) as an example, therefore "Intrastat (DE)" should be chosen.</span></span>  
    * <span data-ttu-id="d6858-116">Klõpsake nuppu Impordi ja seejärel nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="d6858-116">Click Import and then click Yes.</span></span>  
7. <span data-ttu-id="d6858-117">Avage veeru filter Konfiguratsiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="d6858-117">Open Configuration name column filter.</span></span>
8. <span data-ttu-id="d6858-118">Rakendage väljal Konfiguratsiooni nimi filtrit väärtusega Intrastati aruanne kasutades filtri tehtemärki „algab üksusega”.</span><span class="sxs-lookup"><span data-stu-id="d6858-118">Apply a filter on the "Configuration name" field, with a value of "intrastat report", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="d6858-119">Klõpsake nuppu Impordi ja seejärel nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="d6858-119">Click Import and then click Yes.</span></span>  

## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="d6858-120">Väliskaubanduse parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="d6858-120">Set up Foreign trade parameters</span></span>
1. <span data-ttu-id="d6858-121">Avage Maks > Seadistus > Väliskaubandus > Väliskaubanduse parameetrid</span><span class="sxs-lookup"><span data-stu-id="d6858-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters</span></span>
2. <span data-ttu-id="d6858-122">Laiendage jaotist Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="d6858-122">Expand the Electronic reporting section.</span></span>
3. <span data-ttu-id="d6858-123">Sisestage või valige väärtus Intrastat (DE) väljal Failivormingu vastendamine</span><span class="sxs-lookup"><span data-stu-id="d6858-123">In the File format mapping field, enter or select a value Intrastat (DE)</span></span>
4. <span data-ttu-id="d6858-124">Sisestage või valige väärtus Intrastati aruanne väljal Aruandevormingu vastendamine</span><span class="sxs-lookup"><span data-stu-id="d6858-124">In the Report format mapping field, enter or select a value Intrastat report</span></span>
5. <span data-ttu-id="d6858-125">Laiendage jaotist Ümardamisreeglid.</span><span class="sxs-lookup"><span data-stu-id="d6858-125">Expand the Rounding rules section.</span></span>
    * <span data-ttu-id="d6858-126">Peate seadistama ümardamisreeglid, mis kehtivad teie riigis/regioonis Intrastati aruandluse puhul.</span><span class="sxs-lookup"><span data-stu-id="d6858-126">You should set up rounding rules that are applicable in your country/region for Intrastat reporting.</span></span>  
6. <span data-ttu-id="d6858-127">Sisestage number väljale Ümardamisreegel</span><span class="sxs-lookup"><span data-stu-id="d6858-127">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="d6858-128">Sisestage ümardamistäpsus, näiteks 0,01.</span><span class="sxs-lookup"><span data-stu-id="d6858-128">Enter rounding precision, for example, enter '0.01'.</span></span>  
7. <span data-ttu-id="d6858-129">Sisestage number väljale Summa kümnendkohtade arv.</span><span class="sxs-lookup"><span data-stu-id="d6858-129">In the Number of decimals for amount field, enter a number.</span></span>
    * <span data-ttu-id="d6858-130">Sisestage näiteks 2.</span><span class="sxs-lookup"><span data-stu-id="d6858-130">For example, enter '2'.</span></span>  
8. <span data-ttu-id="d6858-131">Valige suvand väljal Ümardamine alla 1 kg.</span><span class="sxs-lookup"><span data-stu-id="d6858-131">In the Rounding below 1 kg field, select an option.</span></span>
    * <span data-ttu-id="d6858-132">Valige näiteks Ümardamine kuni 1 kg-ni.</span><span class="sxs-lookup"><span data-stu-id="d6858-132">For example, select 'Rounding up to 1 kg'.</span></span>  
9. <span data-ttu-id="d6858-133">Sisestage number väljale Ümardamisreegel</span><span class="sxs-lookup"><span data-stu-id="d6858-133">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="d6858-134">Sisestage näiteks 1 kaalu ümardamise kohta täisarvuni.</span><span class="sxs-lookup"><span data-stu-id="d6858-134">For example, enter '1' for rounding weight to the integer.</span></span>  
10. <span data-ttu-id="d6858-135">Laiendage jaotist Alampiir.</span><span class="sxs-lookup"><span data-stu-id="d6858-135">Expand the Minimum limit section.</span></span>
11. <span data-ttu-id="d6858-136">Sisestage number väljale Kaal.</span><span class="sxs-lookup"><span data-stu-id="d6858-136">In the Weight field, enter a number.</span></span>
    * <span data-ttu-id="d6858-137">Sisestage minimaalseks kaaluks näiteks 10.</span><span class="sxs-lookup"><span data-stu-id="d6858-137">For example, enter '10' as the minimum weight.</span></span>  
12. <span data-ttu-id="d6858-138">Sisestage number väljale Summa.</span><span class="sxs-lookup"><span data-stu-id="d6858-138">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="d6858-139">Sisestage miinimumsummaks näiteks 200.</span><span class="sxs-lookup"><span data-stu-id="d6858-139">For example, enter '200' as the minimum amount.</span></span>  
13. <span data-ttu-id="d6858-140">Sisestage või valige väärtus väljal Kaup.</span><span class="sxs-lookup"><span data-stu-id="d6858-140">In the Commodity field, enter or select a value.</span></span>

## <a name="set-up-compression-of-intrastat"></a><span data-ttu-id="d6858-141">Intrastati tihendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="d6858-141">Set up Compression of Intrastat</span></span>
1. <span data-ttu-id="d6858-142">Avage Maks > Seadistus > Väliskaubandus > Intrastati tihendamine.</span><span class="sxs-lookup"><span data-stu-id="d6858-142">Go to Tax > Setup > Foreign trade > Compression of Intrastat.</span></span>
2. <span data-ttu-id="d6858-143">Klõpsake nuppu Eemalda.</span><span class="sxs-lookup"><span data-stu-id="d6858-143">Click Remove.</span></span>
3. <span data-ttu-id="d6858-144">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d6858-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d6858-145">Valige jaotises Saadaval näiteks Kaup.</span><span class="sxs-lookup"><span data-stu-id="d6858-145">For example, select Commodity in the Available section.</span></span>  
4. <span data-ttu-id="d6858-146">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d6858-146">Click Add.</span></span>

## <a name="generate-intrastat-declaration"></a><span data-ttu-id="d6858-147">Intrastati deklaratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="d6858-147">Generate Intrastat declaration</span></span>
1. <span data-ttu-id="d6858-148">Avage Maks > Deklaratsioonid > Väliskaubandus > Intrastat</span><span class="sxs-lookup"><span data-stu-id="d6858-148">Go to Tax > Declarations > Foreign trade > Intrastat</span></span>
2. <span data-ttu-id="d6858-149">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="d6858-149">Click Validate.</span></span>
    * <span data-ttu-id="d6858-150">Kinnitamine tehakse vastavalt väljale Kontrolli seadistust lehel Väliskaubanduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="d6858-150">The validation is done according to the Check setup field on the Foreign trade parameters page.</span></span>  
3. <span data-ttu-id="d6858-151">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d6858-151">Click OK.</span></span>
4. <span data-ttu-id="d6858-152">Klõpsake käsku Uuenda.</span><span class="sxs-lookup"><span data-stu-id="d6858-152">Click Update.</span></span>
5. <span data-ttu-id="d6858-153">Klõpsake suvandit Alampiir.</span><span class="sxs-lookup"><span data-stu-id="d6858-153">Click Minimum limit.</span></span>
6. <span data-ttu-id="d6858-154">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="d6858-154">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="d6858-155">Sisestage näiteks 1. jaanuar 2015.</span><span class="sxs-lookup"><span data-stu-id="d6858-155">For example, enter January 1, 2015.</span></span>  
7. <span data-ttu-id="d6858-156">Tehke väljal Tihendamine valik Jah.</span><span class="sxs-lookup"><span data-stu-id="d6858-156">Select Yes in the Compress field.</span></span>
8. <span data-ttu-id="d6858-157">Sisestage kuupäev väljale Lõppkuupäev.</span><span class="sxs-lookup"><span data-stu-id="d6858-157">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="d6858-158">Sisestage näiteks 31. jaanuar 2015.</span><span class="sxs-lookup"><span data-stu-id="d6858-158">For example, enter January 31, 2015.</span></span>  
9. <span data-ttu-id="d6858-159">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d6858-159">Click OK.</span></span>
10. <span data-ttu-id="d6858-160">Klõpsake käsku Uuenda.</span><span class="sxs-lookup"><span data-stu-id="d6858-160">Click Update.</span></span>
11. <span data-ttu-id="d6858-161">Klõpsake käsku Tihenda.</span><span class="sxs-lookup"><span data-stu-id="d6858-161">Click Compress.</span></span>
    * <span data-ttu-id="d6858-162">See tihendamine toimub vastavalt sellele, kuidas te seadistate Intrastati tiheduse sätted.</span><span class="sxs-lookup"><span data-stu-id="d6858-162">This compression happens according to how you set the Compression of intrastate settings.</span></span>  
12. <span data-ttu-id="d6858-163">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="d6858-163">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="d6858-164">Sisestage näiteks 1. jaanuar 2015.</span><span class="sxs-lookup"><span data-stu-id="d6858-164">For example, enter January 1, 2015.</span></span>  
13. <span data-ttu-id="d6858-165">Sisestage kuupäev väljale Lõppkuupäev.</span><span class="sxs-lookup"><span data-stu-id="d6858-165">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="d6858-166">Sisestage näiteks 31. jaanuar 2015.</span><span class="sxs-lookup"><span data-stu-id="d6858-166">For example, enter 31st January 2015.</span></span>  
14. <span data-ttu-id="d6858-167">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d6858-167">Click OK.</span></span>
15. <span data-ttu-id="d6858-168">Klõpsake käsku Uuenda.</span><span class="sxs-lookup"><span data-stu-id="d6858-168">Click Update.</span></span>
16. <span data-ttu-id="d6858-169">Klõpsake käsku Loo uued järjekorranumbrid.</span><span class="sxs-lookup"><span data-stu-id="d6858-169">Click Regenerate sequence numbers.</span></span>
17. <span data-ttu-id="d6858-170">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d6858-170">Click OK.</span></span>
18. <span data-ttu-id="d6858-171">Klõpsake suvandit Väljund.</span><span class="sxs-lookup"><span data-stu-id="d6858-171">Click Output.</span></span>
19. <span data-ttu-id="d6858-172">Klõpsake vahekaarti Aruanne.</span><span class="sxs-lookup"><span data-stu-id="d6858-172">Click Report.</span></span>
20. <span data-ttu-id="d6858-173">Sisestage väljale Alates kuupäevast aruandlusperioodi esimene kuupäev.</span><span class="sxs-lookup"><span data-stu-id="d6858-173">In the From date field, enter the first date of the reporting period.</span></span>
    * <span data-ttu-id="d6858-174">Määrake kuupäevaks näiteks 1. jaanuar 2015.</span><span class="sxs-lookup"><span data-stu-id="d6858-174">For example, set the date to January 1, 2015.</span></span>  
21. <span data-ttu-id="d6858-175">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="d6858-175">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="d6858-176">Sisestage näiteks 31. jaanuar 2015.</span><span class="sxs-lookup"><span data-stu-id="d6858-176">For example, enter January 31, 2015.</span></span>  
22. <span data-ttu-id="d6858-177">Valige Jah väljal Loo fail.</span><span class="sxs-lookup"><span data-stu-id="d6858-177">Select Yes in the Generate file field.</span></span>
23. <span data-ttu-id="d6858-178">Sisestage väärtus väljale Faili nimi.</span><span class="sxs-lookup"><span data-stu-id="d6858-178">In the File name field, type a value.</span></span>
24. <span data-ttu-id="d6858-179">Valige Jah väljal Loo aruanne.</span><span class="sxs-lookup"><span data-stu-id="d6858-179">Select Yes in the Generate report field.</span></span>
25. <span data-ttu-id="d6858-180">Tippige väärtus väljale Aruandefaili nimi.</span><span class="sxs-lookup"><span data-stu-id="d6858-180">In the Report file name field, type a value.</span></span>
26. <span data-ttu-id="d6858-181">Valige suvand väljal Suund.</span><span class="sxs-lookup"><span data-stu-id="d6858-181">In the Direction field, select an option.</span></span>
    * <span data-ttu-id="d6858-182">Tehke näiteks valik Kauba lähetamine.</span><span class="sxs-lookup"><span data-stu-id="d6858-182">For example, select 'Dispatches'.</span></span>  
27. <span data-ttu-id="d6858-183">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d6858-183">Click OK.</span></span>
