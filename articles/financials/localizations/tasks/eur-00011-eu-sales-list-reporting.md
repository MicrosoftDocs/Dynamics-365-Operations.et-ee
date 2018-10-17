--- 
title: "EUR-00011 EL-i käibearuandluse seadistamine"
description: "See ülesandejuhend selgitab EL-i käibearuande jaoks nõutavate eeltingimuste ülevaadet."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, SysQueryForm, SysQueryFieldLookUp,  TaxTable, TaxGroup, TaxItemGroup, TaxCountryRegionParameters, TaxVATNumTable, IntrastatParameters, CustTable, DirPartyQuickCreateForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: aef1d19aabb7937fcd961a9657b8ca65c064b0b1
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="eur-00011-set-up-eu-sales-list-reporting"></a><span data-ttu-id="cd776-103">EUR-00011 EL-i käibearuandluse seadistamine</span><span class="sxs-lookup"><span data-stu-id="cd776-103">EUR-00011 Set up EU sales list reporting</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd776-104">See ülesandejuhend selgitab EL-i käibearuande jaoks nõutavate eeltingimuste ülevaadet.</span><span class="sxs-lookup"><span data-stu-id="cd776-104">This task walks you through an overview of the prerequisites required for EU sales list reporting.</span></span> <span data-ttu-id="cd776-105">Lisateavet EL-i müügiloendi aruandluse, sh nõutavate eeltingimuste kohta leiate rakenduse Dynamics 365 for Finance and Operations spikrist.</span><span class="sxs-lookup"><span data-stu-id="cd776-105">For more information about EU Sales list reporting, including required prerequisites, refer to the Dynamics 365 for Finance and Operations Help.</span></span>

<span data-ttu-id="cd776-106">See ülesanne kohaldub kõigile Euroopa riikidele/piirkondadele.</span><span class="sxs-lookup"><span data-stu-id="cd776-106">This task applies to all European countries/regions.</span></span> <span data-ttu-id="cd776-107">Juhendi loomisel kasutatakse demoettevõtte DEMF andmeid, seega on kodumaise riigi/piirkonna näiteks Saksamaa.</span><span class="sxs-lookup"><span data-stu-id="cd776-107">The guide was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="cd776-108">Juhend kasutab EL-i riigi/piirkonna näitena ka Portugali.</span><span class="sxs-lookup"><span data-stu-id="cd776-108">The guide also uses Portugal as an exemplar EU country/region.</span></span>

<span data-ttu-id="cd776-109">Need ülesanded on mõeldud süsteemi administraatoritele.</span><span class="sxs-lookup"><span data-stu-id="cd776-109">These tasks are intended for system administrators.</span></span>


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a><span data-ttu-id="cd776-110">Elektroonilise aruandluse konfiguratsioonide importimine EL-i käibearuandluse jaoks</span><span class="sxs-lookup"><span data-stu-id="cd776-110">Import electronic reporting configurations for EU sales list reporting</span></span>
1. <span data-ttu-id="cd776-111">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="cd776-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="cd776-112">Klõpsake valikut Määra aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="cd776-112">Click Set active.</span></span>
3. <span data-ttu-id="cd776-113">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="cd776-113">Click Repositories.</span></span>
4. <span data-ttu-id="cd776-114">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="cd776-114">Click Open.</span></span>
5. <span data-ttu-id="cd776-115">Klõpsake toimingupaanil valikut Suvandid.</span><span class="sxs-lookup"><span data-stu-id="cd776-115">On the Action Pane, click Options.</span></span>
6. <span data-ttu-id="cd776-116">Klõpsake suvandit Täpsem filter/sortimine.</span><span class="sxs-lookup"><span data-stu-id="cd776-116">Click Advanced Filter/Sort.</span></span>
7. <span data-ttu-id="cd776-117">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="cd776-117">Click Add.</span></span>
8. <span data-ttu-id="cd776-118">Valige väljal Väli suvand Konfiguratsiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="cd776-118">In the Field field, select 'Configuration name'.</span></span>
9. <span data-ttu-id="cd776-119">Sisestage väljale Kriteeriumid tekst „EL-i käibearuanne (DE)”.</span><span class="sxs-lookup"><span data-stu-id="cd776-119">In the Criteria field, type 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="cd776-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="cd776-120">Click OK.</span></span>
11. <span data-ttu-id="cd776-121">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="cd776-121">Click Import.</span></span>
12. <span data-ttu-id="cd776-122">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="cd776-122">Click Yes.</span></span>
13. <span data-ttu-id="cd776-123">Klõpsake toimingupaanil valikut Suvandid.</span><span class="sxs-lookup"><span data-stu-id="cd776-123">On the Action Pane, click Options.</span></span>
14. <span data-ttu-id="cd776-124">Klõpsake suvandit Täpsem filter/sortimine.</span><span class="sxs-lookup"><span data-stu-id="cd776-124">Click Advanced Filter/Sort.</span></span>
15. <span data-ttu-id="cd776-125">Klõpsake nuppu Lähtesta.</span><span class="sxs-lookup"><span data-stu-id="cd776-125">Click Reset.</span></span>
16. <span data-ttu-id="cd776-126">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="cd776-126">Click Add.</span></span>
17. <span data-ttu-id="cd776-127">Valige väljal Väli suvand Konfiguratsiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="cd776-127">In the Field field, select 'Configuration name'.</span></span>
18. <span data-ttu-id="cd776-128">Sisestage väljale Kriteeriumid tekst „EL-i käibearuanne ridade kaupa”.</span><span class="sxs-lookup"><span data-stu-id="cd776-128">In the Criteria field, type 'EU Sales list by rows report'.</span></span>
19. <span data-ttu-id="cd776-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="cd776-129">Click OK.</span></span>
20. <span data-ttu-id="cd776-130">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="cd776-130">Click Import.</span></span>
21. <span data-ttu-id="cd776-131">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="cd776-131">Click Yes.</span></span>

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a><span data-ttu-id="cd776-132">Käibemaksukoodide seadistamine EL-i käibearuandluse jaoks</span><span class="sxs-lookup"><span data-stu-id="cd776-132">Set up sales tax codes for EU sales list reporting</span></span>
1. <span data-ttu-id="cd776-133">Avage Maks > Kaudsed maksud > Käibemaks > Käibemaksukoodid.</span><span class="sxs-lookup"><span data-stu-id="cd776-133">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="cd776-134">Kasutage kiirfiltrit, et filtreerida välja Käibemaksukood väärtuse „KM19” järgi.</span><span class="sxs-lookup"><span data-stu-id="cd776-134">Use the Quick Filter to filter on the Sales tax code field with a value of 'VAT19'.</span></span>
3. <span data-ttu-id="cd776-135">Laiendage jaotist Aruande seadistus.</span><span class="sxs-lookup"><span data-stu-id="cd776-135">Expand the Report setup section.</span></span>
    * <span data-ttu-id="cd776-136">Kontrollige, kas suvandi Välistatud valik sätteks on valitud Ei.</span><span class="sxs-lookup"><span data-stu-id="cd776-136">Verify that the Excluded selection is set to No.</span></span>  
    * <span data-ttu-id="cd776-137">Võib-olla peate selle sätte muutmiseks avama ülesandejuhendi.</span><span class="sxs-lookup"><span data-stu-id="cd776-137">You may need to unlock the task guide to change this setting.</span></span>  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="cd776-138">Käibemaksugruppide seadistamine EL-i käibearuandluse jaoks</span><span class="sxs-lookup"><span data-stu-id="cd776-138">Set up sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="cd776-139">Avage Maks > Kaudsed maksud > Käibemaks > Käibemaksu grupid.</span><span class="sxs-lookup"><span data-stu-id="cd776-139">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="cd776-140">Kasutage kiirfiltrit, et filtreerida välja Käibemaksugrupp väärtuse „AR-DOM” järgi.</span><span class="sxs-lookup"><span data-stu-id="cd776-140">Use the Quick Filter to filter on the Sales tax group field with a value of 'AR-DOM'.</span></span>
3. <span data-ttu-id="cd776-141">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="cd776-141">Click Edit.</span></span>
4. <span data-ttu-id="cd776-142">Laiendage jaotist Seadistus.</span><span class="sxs-lookup"><span data-stu-id="cd776-142">Expand the Setup section.</span></span>
5. <span data-ttu-id="cd776-143">Valige loendist esimene rida.</span><span class="sxs-lookup"><span data-stu-id="cd776-143">In the list, select the first row.</span></span>
6. <span data-ttu-id="cd776-144">Märkige ruut Vabastus.</span><span class="sxs-lookup"><span data-stu-id="cd776-144">Select the Exempt check box.</span></span>
7. <span data-ttu-id="cd776-145">Valige loendist teine rida.</span><span class="sxs-lookup"><span data-stu-id="cd776-145">In the list, select the second row.</span></span>
8. <span data-ttu-id="cd776-146">Märkige ruut Vabastus.</span><span class="sxs-lookup"><span data-stu-id="cd776-146">Select the Exempt check box.</span></span>
9. <span data-ttu-id="cd776-147">Valige loendist kolmas rida.</span><span class="sxs-lookup"><span data-stu-id="cd776-147">In the list, select the third row.</span></span>
10. <span data-ttu-id="cd776-148">Märkige ruut Vabastus.</span><span class="sxs-lookup"><span data-stu-id="cd776-148">Select the Exempt check box.</span></span>

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="cd776-149">Kauba käibemaksugruppide seadistamine EL-i käibearuandluse jaoks</span><span class="sxs-lookup"><span data-stu-id="cd776-149">Set up item sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="cd776-150">Avage Maks > Kaudsed maksud > Käibemaks > Käibemaksukoodid.</span><span class="sxs-lookup"><span data-stu-id="cd776-150">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
2. <span data-ttu-id="cd776-151">Kasutage kiirfiltrit, et filtreerida välja Kauba käibemaksugrupp väärtuse „TÄIELIK” järgi.</span><span class="sxs-lookup"><span data-stu-id="cd776-151">Use the Quick Filter to filter on the Item sales tax group field with a value of 'FULL '.</span></span>
    * <span data-ttu-id="cd776-152">Kontrollige, kas suvandi Aruandlustüübi valik sätteks on valitud Kaup.</span><span class="sxs-lookup"><span data-stu-id="cd776-152">Verify that the Reporting type selection is set to 'Item'.</span></span>  
    * <span data-ttu-id="cd776-153">Võib-olla peate selle välja väärtuse muutmiseks avama ülesandejuhendi.</span><span class="sxs-lookup"><span data-stu-id="cd776-153">You may need to unlock the task guide to change the value in this field.</span></span>  
3. <span data-ttu-id="cd776-154">Kasutage kiirfiltrit, et filtreerida välja Kauba käibemaksugrupp väärtuse „PUNANE” järgi.</span><span class="sxs-lookup"><span data-stu-id="cd776-154">Use the Quick Filter to filter on the Item sales tax group field with a value of 'RED '.</span></span>
    * <span data-ttu-id="cd776-155">Kontrollige, kas suvandi Aruandlustüübi valik sätteks on valitud Teenus.</span><span class="sxs-lookup"><span data-stu-id="cd776-155">Verify that the Reporting type selection is set to 'Service'.</span></span>  
    * <span data-ttu-id="cd776-156">Võib-olla peate selle välja väärtuse muutmiseks avama ülesandejuhendi.</span><span class="sxs-lookup"><span data-stu-id="cd776-156">You may need to unlock the task guide to change the value in this field.</span></span>  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a><span data-ttu-id="cd776-157">Riigi/piirkonna parameetrite seadistamine EL-i käibearuandluse jaoks</span><span class="sxs-lookup"><span data-stu-id="cd776-157">Set up country/region parameters for EU sales list reporting</span></span>
1. <span data-ttu-id="cd776-158">Minge jaotisse Maks > Seadistus > Käibemaks > Riigi/piirkonna parameetrid.</span><span class="sxs-lookup"><span data-stu-id="cd776-158">Go to Tax > Setup > Sales tax > Country/region parameters.</span></span>
2. <span data-ttu-id="cd776-159">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cd776-159">Click New.</span></span>
3. <span data-ttu-id="cd776-160">Valige väljal Riik/piirkond tüüp PRT.</span><span class="sxs-lookup"><span data-stu-id="cd776-160">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="cd776-161">Sisestage väljale Käibemaks tekst „PT”.</span><span class="sxs-lookup"><span data-stu-id="cd776-161">In the Sales tax field, type 'PT'.</span></span>

## <a name="create-tax-exempt-numbers"></a><span data-ttu-id="cd776-162">Maksuvabastuse numbrite loomine</span><span class="sxs-lookup"><span data-stu-id="cd776-162">Create tax exempt numbers</span></span>
1. <span data-ttu-id="cd776-163">Minge jaotisse Maks > Seadistus > Käibemaks > Maksuvabastuskoodid.</span><span class="sxs-lookup"><span data-stu-id="cd776-163">Go to Tax > Setup > Sales tax > Tax exempt numbers.</span></span>
2. <span data-ttu-id="cd776-164">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cd776-164">Click New.</span></span>
3. <span data-ttu-id="cd776-165">Valige väljal Riik/piirkond tüüp PRT.</span><span class="sxs-lookup"><span data-stu-id="cd776-165">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="cd776-166">Sisestage väljale Maksuvabastuse number tekst „PT12345”.</span><span class="sxs-lookup"><span data-stu-id="cd776-166">In the Tax exempt number field, type 'PT12345'.</span></span>

## <a name="set-up-eu-sales-list-reporting-parameters"></a><span data-ttu-id="cd776-167">EL-i käibearuandluse parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="cd776-167">Set up EU sales list reporting parameters</span></span>
1. <span data-ttu-id="cd776-168">Minge jaotisse Maks > Seadistus > Väliskaubandus > Väliskaubanduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="cd776-168">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="cd776-169">Klõpsake vahekaarti EL-i käibearuanne.</span><span class="sxs-lookup"><span data-stu-id="cd776-169">Click the EU sales list tab.</span></span>
3. <span data-ttu-id="cd776-170">Valige väljal Ostude ülekandmine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="cd776-170">Select Yes in the Transfer purchases field.</span></span>
4. <span data-ttu-id="cd776-171">Laiendage jaotist Ümardamisreeglid.</span><span class="sxs-lookup"><span data-stu-id="cd776-171">Expand the Rounding rules section.</span></span>
5. <span data-ttu-id="cd776-172">Määrake ümardamisreegli väärtuseks „0,1”.</span><span class="sxs-lookup"><span data-stu-id="cd776-172">Set Rounding rule to '0.1'.</span></span>
6. <span data-ttu-id="cd776-173">Valige väljal Kasuta miinimumväärtust suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="cd776-173">Select Yes in the Use minimum value field.</span></span>
7. <span data-ttu-id="cd776-174">Sisestage väljale Kümnendkohtade arv väärtus „2”..</span><span class="sxs-lookup"><span data-stu-id="cd776-174">In the Number of decimals field, enter '2'.</span></span>
8. <span data-ttu-id="cd776-175">Laiendage jaotist Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="cd776-175">Expand the Electronic reporting section.</span></span>
9. <span data-ttu-id="cd776-176">Valige väljal Failivormingu vastendus suvand EL-i käibearuanne (DE).</span><span class="sxs-lookup"><span data-stu-id="cd776-176">In the File format mapping field, select 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="cd776-177">Valige väljal Aruandevormingu vastendus suvand EL-i käibearuanne ridade kaupa.</span><span class="sxs-lookup"><span data-stu-id="cd776-177">In the Report format mapping field, select 'EU Sales list by rows report'.</span></span>
11. <span data-ttu-id="cd776-178">Klõpsake vahekaarti Riigi/regiooni atribuudid.</span><span class="sxs-lookup"><span data-stu-id="cd776-178">Click the Country/region properties tab.</span></span>
    * <span data-ttu-id="cd776-179">Kontrollige, kas välja Riigi/piirkonna tüüp sätteks on valitud Kodumaine või Riigi/piirkonna DEU.</span><span class="sxs-lookup"><span data-stu-id="cd776-179">Verify that the Country/region type field is set to 'Domestic' for Country/region DEU.</span></span>  
    * <span data-ttu-id="cd776-180">Võib-olla peate selle välja väärtuse muutmiseks avama ülesandejuhendi.</span><span class="sxs-lookup"><span data-stu-id="cd776-180">You may need to unlock the task guide to change the value in this field.</span></span>  
12. <span data-ttu-id="cd776-181">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cd776-181">Click New.</span></span>
13. <span data-ttu-id="cd776-182">Valige väljal Riik/piirkond tüüp PRT.</span><span class="sxs-lookup"><span data-stu-id="cd776-182">In the Country/region field, type 'PRT'.</span></span>
14. <span data-ttu-id="cd776-183">Sisestage väljale Intrastati kood tekst „PT”.</span><span class="sxs-lookup"><span data-stu-id="cd776-183">In the Intrastat code field, type 'PT'.</span></span>
15. <span data-ttu-id="cd776-184">Valige väljal Riigi/piirkonna tüüp suvand EL.</span><span class="sxs-lookup"><span data-stu-id="cd776-184">In the Country/region type field, select 'EU'.</span></span>
16. <span data-ttu-id="cd776-185">Klõpsake vahekaarti Numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="cd776-185">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="cd776-186">Kontrollige, kas viitele EL-i käibearuanne on määratud numbriseeria kood.</span><span class="sxs-lookup"><span data-stu-id="cd776-186">Verify that a Number sequence code is specified for the Reference 'EU sales list'.</span></span>  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a><span data-ttu-id="cd776-187">Kliendi loomine EL-i käibearuandluse demoeesmärgil</span><span class="sxs-lookup"><span data-stu-id="cd776-187">Create a customer for EU sales list reporting demo purposes</span></span>
1. <span data-ttu-id="cd776-188">Avage Müügireskontro > Kliendid > Kõik kliendid.</span><span class="sxs-lookup"><span data-stu-id="cd776-188">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="cd776-189">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cd776-189">Click New.</span></span>
3. <span data-ttu-id="cd776-190">Sisestage väljale Kliendi konto tekst „PRT-001”.</span><span class="sxs-lookup"><span data-stu-id="cd776-190">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="cd776-191">Sisestage väljale Nimi tekst „Klient Portugalist”.</span><span class="sxs-lookup"><span data-stu-id="cd776-191">In the Name field, type 'A customer from Portugal'.</span></span>
5. <span data-ttu-id="cd776-192">Valige väljal Kliendigrupp suvand 10.</span><span class="sxs-lookup"><span data-stu-id="cd776-192">In the Customer group field, select '10'.</span></span>
6. <span data-ttu-id="cd776-193">Valige väljal Käibemaksugrupp suvand AR-DOM.</span><span class="sxs-lookup"><span data-stu-id="cd776-193">In the Sales tax group field, select 'AR-DOM'.</span></span>
7. <span data-ttu-id="cd776-194">Valige väljal Maksuvabastuse number suvand PT12345.</span><span class="sxs-lookup"><span data-stu-id="cd776-194">In the Tax exempt number field, select 'PT12345'.</span></span>
8. <span data-ttu-id="cd776-195">Valige väljal Riik/piirkond tüüp PRT.</span><span class="sxs-lookup"><span data-stu-id="cd776-195">In the Country/region field, type 'PRT'.</span></span>
9. <span data-ttu-id="cd776-196">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="cd776-196">Click Save.</span></span>


