--- 
title: "EL-i käibearuandluse seadistamine"
description: "See ülesandejuhend selgitab EL-i käibearuande jaoks nõutavate eeltingimuste ülevaadet."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 821b1403da1b4269c01e07c20e82f0de67104d84
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-eu-sales-list-reporting"></a><span data-ttu-id="0cb40-103">EL-i käibearuandluse seadistamine</span><span class="sxs-lookup"><span data-stu-id="0cb40-103">Set up EU sales list reporting</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0cb40-104">See ülesandejuhend selgitab EL-i käibearuande jaoks nõutavate eeltingimuste ülevaadet.</span><span class="sxs-lookup"><span data-stu-id="0cb40-104">This task walks you through an overview of the prerequisites required for EU sales list reporting.</span></span> <span data-ttu-id="0cb40-105">Lisateavet EL-i müügiloendi aruandluse, sh nõutavate eeltingimuste kohta leiate rakenduse Dynamics 365 for Finance and Operations spikrist.</span><span class="sxs-lookup"><span data-stu-id="0cb40-105">For more information about EU Sales list reporting, including required prerequisites, refer to the Dynamics 365 for Finance and Operations Help.</span></span>

<span data-ttu-id="0cb40-106">See ülesanne kohaldub kõigile Euroopa riikidele/piirkondadele.</span><span class="sxs-lookup"><span data-stu-id="0cb40-106">This task applies to all European countries/regions.</span></span> <span data-ttu-id="0cb40-107">Juhendi loomisel kasutatakse demoettevõtte DEMF andmeid, seega on kodumaise riigi/piirkonna näiteks Saksamaa.</span><span class="sxs-lookup"><span data-stu-id="0cb40-107">The guide was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="0cb40-108">Juhend kasutab EL-i riigi/piirkonna näitena ka Portugali.</span><span class="sxs-lookup"><span data-stu-id="0cb40-108">The guide also uses Portugal as an exemplar EU country/region.</span></span>

<span data-ttu-id="0cb40-109">Need ülesanded on mõeldud süsteemi administraatoritele.</span><span class="sxs-lookup"><span data-stu-id="0cb40-109">These tasks are intended for system administrators.</span></span>


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a><span data-ttu-id="0cb40-110">Elektroonilise aruandluse konfiguratsioonide importimine EL-i käibearuandluse jaoks</span><span class="sxs-lookup"><span data-stu-id="0cb40-110">Import electronic reporting configurations for EU sales list reporting</span></span>
1. <span data-ttu-id="0cb40-111">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="0cb40-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="0cb40-112">Klõpsake valikut Määra aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="0cb40-112">Click Set active.</span></span>
3. <span data-ttu-id="0cb40-113">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="0cb40-113">Click Repositories.</span></span>
4. <span data-ttu-id="0cb40-114">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="0cb40-114">Click Open.</span></span>
5. <span data-ttu-id="0cb40-115">Klõpsake toimingupaanil valikut Suvandid.</span><span class="sxs-lookup"><span data-stu-id="0cb40-115">On the Action Pane, click Options.</span></span>
6. <span data-ttu-id="0cb40-116">Klõpsake suvandit Täpsem filter/sortimine.</span><span class="sxs-lookup"><span data-stu-id="0cb40-116">Click Advanced Filter/Sort.</span></span>
7. <span data-ttu-id="0cb40-117">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0cb40-117">Click Add.</span></span>
8. <span data-ttu-id="0cb40-118">Valige väljal Väli suvand Konfiguratsiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="0cb40-118">In the Field field, select 'Configuration name'.</span></span>
9. <span data-ttu-id="0cb40-119">Sisestage väljale Kriteeriumid tekst „EL-i käibearuanne (DE)”.</span><span class="sxs-lookup"><span data-stu-id="0cb40-119">In the Criteria field, type 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="0cb40-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0cb40-120">Click OK.</span></span>
11. <span data-ttu-id="0cb40-121">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="0cb40-121">Click Import.</span></span>
12. <span data-ttu-id="0cb40-122">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="0cb40-122">Click Yes.</span></span>
13. <span data-ttu-id="0cb40-123">Klõpsake toimingupaanil valikut Suvandid.</span><span class="sxs-lookup"><span data-stu-id="0cb40-123">On the Action Pane, click Options.</span></span>
14. <span data-ttu-id="0cb40-124">Klõpsake suvandit Täpsem filter/sortimine.</span><span class="sxs-lookup"><span data-stu-id="0cb40-124">Click Advanced Filter/Sort.</span></span>
15. <span data-ttu-id="0cb40-125">Klõpsake nuppu Lähtesta.</span><span class="sxs-lookup"><span data-stu-id="0cb40-125">Click Reset.</span></span>
16. <span data-ttu-id="0cb40-126">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0cb40-126">Click Add.</span></span>
17. <span data-ttu-id="0cb40-127">Valige väljal Väli suvand Konfiguratsiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="0cb40-127">In the Field field, select 'Configuration name'.</span></span>
18. <span data-ttu-id="0cb40-128">Sisestage väljale Kriteeriumid tekst „EL-i käibearuanne ridade kaupa”.</span><span class="sxs-lookup"><span data-stu-id="0cb40-128">In the Criteria field, type 'EU Sales list by rows report'.</span></span>
19. <span data-ttu-id="0cb40-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0cb40-129">Click OK.</span></span>
20. <span data-ttu-id="0cb40-130">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="0cb40-130">Click Import.</span></span>
21. <span data-ttu-id="0cb40-131">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="0cb40-131">Click Yes.</span></span>

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a><span data-ttu-id="0cb40-132">Käibemaksukoodide seadistamine EL-i käibearuandluse jaoks</span><span class="sxs-lookup"><span data-stu-id="0cb40-132">Set up sales tax codes for EU sales list reporting</span></span>
1. <span data-ttu-id="0cb40-133">Avage Maks > Kaudsed maksud > Käibemaks > Käibemaksukoodid.</span><span class="sxs-lookup"><span data-stu-id="0cb40-133">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="0cb40-134">Kasutage kiirfiltrit, et filtreerida välja Käibemaksukood väärtuse „KM19” järgi.</span><span class="sxs-lookup"><span data-stu-id="0cb40-134">Use the Quick Filter to filter on the Sales tax code field with a value of 'VAT19'.</span></span>
3. <span data-ttu-id="0cb40-135">Laiendage jaotist Aruande seadistus.</span><span class="sxs-lookup"><span data-stu-id="0cb40-135">Expand the Report setup section.</span></span>
    * <span data-ttu-id="0cb40-136">Kontrollige, kas suvandi Välistatud valik sätteks on valitud Ei.</span><span class="sxs-lookup"><span data-stu-id="0cb40-136">Verify that the Excluded selection is set to No.</span></span>  
    * <span data-ttu-id="0cb40-137">Võib-olla peate selle sätte muutmiseks avama ülesandejuhendi.</span><span class="sxs-lookup"><span data-stu-id="0cb40-137">You may need to unlock the task guide to change this setting.</span></span>  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="0cb40-138">Käibemaksugruppide seadistamine EL-i käibearuandluse jaoks</span><span class="sxs-lookup"><span data-stu-id="0cb40-138">Set up sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="0cb40-139">Avage Maks > Kaudsed maksud > Käibemaks > Käibemaksu grupid.</span><span class="sxs-lookup"><span data-stu-id="0cb40-139">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="0cb40-140">Kasutage kiirfiltrit, et filtreerida välja Käibemaksugrupp väärtuse „AR-DOM” järgi.</span><span class="sxs-lookup"><span data-stu-id="0cb40-140">Use the Quick Filter to filter on the Sales tax group field with a value of 'AR-DOM'.</span></span>
3. <span data-ttu-id="0cb40-141">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="0cb40-141">Click Edit.</span></span>
4. <span data-ttu-id="0cb40-142">Laiendage jaotist Seadistus.</span><span class="sxs-lookup"><span data-stu-id="0cb40-142">Expand the Setup section.</span></span>
5. <span data-ttu-id="0cb40-143">Valige loendist esimene rida.</span><span class="sxs-lookup"><span data-stu-id="0cb40-143">In the list, select the first row.</span></span>
6. <span data-ttu-id="0cb40-144">Märkige ruut Vabastus.</span><span class="sxs-lookup"><span data-stu-id="0cb40-144">Select the Exempt check box.</span></span>
7. <span data-ttu-id="0cb40-145">Valige loendist teine rida.</span><span class="sxs-lookup"><span data-stu-id="0cb40-145">In the list, select the second row.</span></span>
8. <span data-ttu-id="0cb40-146">Märkige ruut Vabastus.</span><span class="sxs-lookup"><span data-stu-id="0cb40-146">Select the Exempt check box.</span></span>
9. <span data-ttu-id="0cb40-147">Valige loendist kolmas rida.</span><span class="sxs-lookup"><span data-stu-id="0cb40-147">In the list, select the third row.</span></span>
10. <span data-ttu-id="0cb40-148">Märkige ruut Vabastus.</span><span class="sxs-lookup"><span data-stu-id="0cb40-148">Select the Exempt check box.</span></span>

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="0cb40-149">Kauba käibemaksugruppide seadistamine EL-i käibearuandluse jaoks</span><span class="sxs-lookup"><span data-stu-id="0cb40-149">Set up item sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="0cb40-150">Avage Maks > Kaudsed maksud > Käibemaks > Käibemaksukoodid.</span><span class="sxs-lookup"><span data-stu-id="0cb40-150">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
2. <span data-ttu-id="0cb40-151">Kasutage kiirfiltrit, et filtreerida välja Kauba käibemaksugrupp väärtuse „TÄIELIK” järgi.</span><span class="sxs-lookup"><span data-stu-id="0cb40-151">Use the Quick Filter to filter on the Item sales tax group field with a value of 'FULL '.</span></span>
    * <span data-ttu-id="0cb40-152">Kontrollige, kas suvandi Aruandlustüübi valik sätteks on valitud Kaup.</span><span class="sxs-lookup"><span data-stu-id="0cb40-152">Verify that the Reporting type selection is set to 'Item'.</span></span>  
    * <span data-ttu-id="0cb40-153">Võib-olla peate selle välja väärtuse muutmiseks avama ülesandejuhendi.</span><span class="sxs-lookup"><span data-stu-id="0cb40-153">You may need to unlock the task guide to change the value in this field.</span></span>  
3. <span data-ttu-id="0cb40-154">Kasutage kiirfiltrit, et filtreerida välja Kauba käibemaksugrupp väärtuse „PUNANE” järgi.</span><span class="sxs-lookup"><span data-stu-id="0cb40-154">Use the Quick Filter to filter on the Item sales tax group field with a value of 'RED '.</span></span>
    * <span data-ttu-id="0cb40-155">Kontrollige, kas suvandi Aruandlustüübi valik sätteks on valitud Teenus.</span><span class="sxs-lookup"><span data-stu-id="0cb40-155">Verify that the Reporting type selection is set to 'Service'.</span></span>  
    * <span data-ttu-id="0cb40-156">Võib-olla peate selle välja väärtuse muutmiseks avama ülesandejuhendi.</span><span class="sxs-lookup"><span data-stu-id="0cb40-156">You may need to unlock the task guide to change the value in this field.</span></span>  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a><span data-ttu-id="0cb40-157">Riigi/piirkonna parameetrite seadistamine EL-i käibearuandluse jaoks</span><span class="sxs-lookup"><span data-stu-id="0cb40-157">Set up country/region parameters for EU sales list reporting</span></span>
1. <span data-ttu-id="0cb40-158">Minge jaotisse Maks > Seadistus > Käibemaks > Riigi/piirkonna parameetrid.</span><span class="sxs-lookup"><span data-stu-id="0cb40-158">Go to Tax > Setup > Sales tax > Country/region parameters.</span></span>
2. <span data-ttu-id="0cb40-159">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0cb40-159">Click New.</span></span>
3. <span data-ttu-id="0cb40-160">Valige väljal Riik/piirkond tüüp PRT.</span><span class="sxs-lookup"><span data-stu-id="0cb40-160">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="0cb40-161">Sisestage väljale Käibemaks tekst „PT”.</span><span class="sxs-lookup"><span data-stu-id="0cb40-161">In the Sales tax field, type 'PT'.</span></span>

## <a name="create-tax-exempt-numbers"></a><span data-ttu-id="0cb40-162">Maksuvabastuse numbrite loomine</span><span class="sxs-lookup"><span data-stu-id="0cb40-162">Create tax exempt numbers</span></span>
1. <span data-ttu-id="0cb40-163">Minge jaotisse Maks > Seadistus > Käibemaks > Maksuvabastuskoodid.</span><span class="sxs-lookup"><span data-stu-id="0cb40-163">Go to Tax > Setup > Sales tax > Tax exempt numbers.</span></span>
2. <span data-ttu-id="0cb40-164">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0cb40-164">Click New.</span></span>
3. <span data-ttu-id="0cb40-165">Valige väljal Riik/piirkond tüüp PRT.</span><span class="sxs-lookup"><span data-stu-id="0cb40-165">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="0cb40-166">Sisestage väljale Maksuvabastuse number tekst „PT12345”.</span><span class="sxs-lookup"><span data-stu-id="0cb40-166">In the Tax exempt number field, type 'PT12345'.</span></span>

## <a name="set-up-eu-sales-list-reporting-parameters"></a><span data-ttu-id="0cb40-167">EL-i käibearuandluse parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="0cb40-167">Set up EU sales list reporting parameters</span></span>
1. <span data-ttu-id="0cb40-168">Minge jaotisse Maks > Seadistus > Väliskaubandus > Väliskaubanduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="0cb40-168">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="0cb40-169">Klõpsake vahekaarti EL-i käibearuanne.</span><span class="sxs-lookup"><span data-stu-id="0cb40-169">Click the EU sales list tab.</span></span>
3. <span data-ttu-id="0cb40-170">Valige väljal Ostude ülekandmine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="0cb40-170">Select Yes in the Transfer purchases field.</span></span>
4. <span data-ttu-id="0cb40-171">Laiendage jaotist Ümardamisreeglid.</span><span class="sxs-lookup"><span data-stu-id="0cb40-171">Expand the Rounding rules section.</span></span>
5. <span data-ttu-id="0cb40-172">Määrake ümardamisreegli väärtuseks „0,1”.</span><span class="sxs-lookup"><span data-stu-id="0cb40-172">Set Rounding rule to '0.1'.</span></span>
6. <span data-ttu-id="0cb40-173">Valige väljal Kasuta miinimumväärtust suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="0cb40-173">Select Yes in the Use minimum value field.</span></span>
7. <span data-ttu-id="0cb40-174">Sisestage väljale Kümnendkohtade arv väärtus „2”..</span><span class="sxs-lookup"><span data-stu-id="0cb40-174">In the Number of decimals field, enter '2'.</span></span>
8. <span data-ttu-id="0cb40-175">Laiendage jaotist Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="0cb40-175">Expand the Electronic reporting section.</span></span>
9. <span data-ttu-id="0cb40-176">Valige väljal Failivormingu vastendus suvand EL-i käibearuanne (DE).</span><span class="sxs-lookup"><span data-stu-id="0cb40-176">In the File format mapping field, select 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="0cb40-177">Valige väljal Aruandevormingu vastendus suvand EL-i käibearuanne ridade kaupa.</span><span class="sxs-lookup"><span data-stu-id="0cb40-177">In the Report format mapping field, select 'EU Sales list by rows report'.</span></span>
11. <span data-ttu-id="0cb40-178">Klõpsake vahekaarti Riigi/regiooni atribuudid.</span><span class="sxs-lookup"><span data-stu-id="0cb40-178">Click the Country/region properties tab.</span></span>
    * <span data-ttu-id="0cb40-179">Kontrollige, kas välja Riigi/piirkonna tüüp sätteks on valitud Kodumaine või Riigi/piirkonna DEU.</span><span class="sxs-lookup"><span data-stu-id="0cb40-179">Verify that the Country/region type field is set to 'Domestic' for Country/region DEU.</span></span>  
    * <span data-ttu-id="0cb40-180">Võib-olla peate selle välja väärtuse muutmiseks avama ülesandejuhendi.</span><span class="sxs-lookup"><span data-stu-id="0cb40-180">You may need to unlock the task guide to change the value in this field.</span></span>  
12. <span data-ttu-id="0cb40-181">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0cb40-181">Click New.</span></span>
13. <span data-ttu-id="0cb40-182">Valige väljal Riik/piirkond tüüp PRT.</span><span class="sxs-lookup"><span data-stu-id="0cb40-182">In the Country/region field, type 'PRT'.</span></span>
14. <span data-ttu-id="0cb40-183">Sisestage väljale Intrastati kood tekst „PT”.</span><span class="sxs-lookup"><span data-stu-id="0cb40-183">In the Intrastat code field, type 'PT'.</span></span>
15. <span data-ttu-id="0cb40-184">Valige väljal Riigi/piirkonna tüüp suvand EL.</span><span class="sxs-lookup"><span data-stu-id="0cb40-184">In the Country/region type field, select 'EU'.</span></span>
16. <span data-ttu-id="0cb40-185">Klõpsake vahekaarti Numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="0cb40-185">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="0cb40-186">Kontrollige, kas viitele EL-i käibearuanne on määratud numbriseeria kood.</span><span class="sxs-lookup"><span data-stu-id="0cb40-186">Verify that a Number sequence code is specified for the Reference 'EU sales list'.</span></span>  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a><span data-ttu-id="0cb40-187">Kliendi loomine EL-i käibearuandluse demoeesmärgil</span><span class="sxs-lookup"><span data-stu-id="0cb40-187">Create a customer for EU sales list reporting demo purposes</span></span>
1. <span data-ttu-id="0cb40-188">Avage Müügireskontro > Kliendid > Kõik kliendid.</span><span class="sxs-lookup"><span data-stu-id="0cb40-188">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="0cb40-189">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0cb40-189">Click New.</span></span>
3. <span data-ttu-id="0cb40-190">Sisestage väljale Kliendi konto tekst „PRT-001”.</span><span class="sxs-lookup"><span data-stu-id="0cb40-190">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="0cb40-191">Sisestage väljale Nimi tekst „Klient Portugalist”.</span><span class="sxs-lookup"><span data-stu-id="0cb40-191">In the Name field, type 'A customer from Portugal'.</span></span>
5. <span data-ttu-id="0cb40-192">Valige väljal Kliendigrupp suvand 10.</span><span class="sxs-lookup"><span data-stu-id="0cb40-192">In the Customer group field, select '10'.</span></span>
6. <span data-ttu-id="0cb40-193">Valige väljal Käibemaksugrupp suvand AR-DOM.</span><span class="sxs-lookup"><span data-stu-id="0cb40-193">In the Sales tax group field, select 'AR-DOM'.</span></span>
7. <span data-ttu-id="0cb40-194">Valige väljal Maksuvabastuse number suvand PT12345.</span><span class="sxs-lookup"><span data-stu-id="0cb40-194">In the Tax exempt number field, select 'PT12345'.</span></span>
8. <span data-ttu-id="0cb40-195">Valige väljal Riik/piirkond tüüp PRT.</span><span class="sxs-lookup"><span data-stu-id="0cb40-195">In the Country/region field, type 'PRT'.</span></span>
9. <span data-ttu-id="0cb40-196">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="0cb40-196">Click Save.</span></span>


