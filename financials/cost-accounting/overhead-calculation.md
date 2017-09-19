---
title: "Üldkulude arvutus"
description: "Selles teemas kirjeldatakse tüüpilisi üldkulude arvutamise ja eraldamise protsesse."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 9e13fc9fa7e51a1299ca8698f581de979b680a7b
ms.openlocfilehash: a8c867ba49b95af2816fe8294059307e974c0a81
ms.contentlocale: et-ee
ms.lasthandoff: 09/18/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="eaa52-103">Üldkulude arvutus</span><span class="sxs-lookup"><span data-stu-id="eaa52-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="eaa52-104">Selles teemas kirjeldatakse tüüpilisi üldkulude arvutamise ja eraldamise protsesse.</span><span class="sxs-lookup"><span data-stu-id="eaa52-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="eaa52-105">Mõiste määratlus</span><span class="sxs-lookup"><span data-stu-id="eaa52-105">Term definition</span></span>
---------------

<span data-ttu-id="eaa52-106">Üldkulud on kulud, mis kaasnevad ettevõtte käitamisega, kuid mida ei saa seostada otseselt ühegi kindla äritegevuse, toote ega teenusega.</span><span class="sxs-lookup"><span data-stu-id="eaa52-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="eaa52-107">Üldkulud pakuvad kriitilist tuge kasumit andavate tegevuste loomisele.</span><span class="sxs-lookup"><span data-stu-id="eaa52-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="eaa52-108">Siin on mõned näited üldkuludest.</span><span class="sxs-lookup"><span data-stu-id="eaa52-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="eaa52-109">Üür</span><span class="sxs-lookup"><span data-stu-id="eaa52-109">Rent</span></span>
-   <span data-ttu-id="eaa52-110">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-110">Electricity</span></span>
-   <span data-ttu-id="eaa52-111">Haldustasud</span><span class="sxs-lookup"><span data-stu-id="eaa52-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="eaa52-112">Üldkulude arvutuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="eaa52-112">Overhead calculation overview</span></span>
<span data-ttu-id="eaa52-113">Üldkulude arvutus käitab kuluarvutuse poliitikaid õiges järjekorras.</span><span class="sxs-lookup"><span data-stu-id="eaa52-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="eaa52-114">Saate käivitada üldkulude arvutuse sama rahandusperioodi kohta mitu korda, kui kuluarvestuse poliitikaid on muudetud või tuvastatud teatud tõrked.</span><span class="sxs-lookup"><span data-stu-id="eaa52-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="eaa52-115">Iga üldkulude arvutamise käitamine talletatakse ja see saab kordumatu versiooni-ID, mis võimaldab teil arvutuste erinevaid versioone võrrelda.</span><span class="sxs-lookup"><span data-stu-id="eaa52-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="eaa52-116">Ülekulude arvutusega loodud kulukirjed saavad aruandluskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="eaa52-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="eaa52-117">See aruandluskuupäev vastab arvutuses kasutatud rahandusperioodi lõppkuupäevale.</span><span class="sxs-lookup"><span data-stu-id="eaa52-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="eaa52-118">Kordumatu versiooni-ID koosneb järgmistest elementidest.</span><span class="sxs-lookup"><span data-stu-id="eaa52-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="eaa52-119">Versiooni tüüp</span><span class="sxs-lookup"><span data-stu-id="eaa52-119">Version type</span></span>
-   <span data-ttu-id="eaa52-120">Kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="eaa52-120">Date and time</span></span>
-   <span data-ttu-id="eaa52-121">Kuluarvestuse pearaamat</span><span class="sxs-lookup"><span data-stu-id="eaa52-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="eaa52-122">Finantsaasta</span><span class="sxs-lookup"><span data-stu-id="eaa52-122">Fiscal year</span></span>
-   <span data-ttu-id="eaa52-123">Rahandusperiood</span><span class="sxs-lookup"><span data-stu-id="eaa52-123">Fiscal period</span></span>

<span data-ttu-id="eaa52-124">Üldkulude arvutus käivitatakse versioonist sõltumatult.</span><span class="sxs-lookup"><span data-stu-id="eaa52-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="eaa52-125">Seetõttu saate arvutada eelarveversiooni enne tegelikku versiooni.</span><span class="sxs-lookup"><span data-stu-id="eaa52-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="eaa52-126">Üldkulude arvutus koosneb neljast etapist, nagu näha alltoodud joonisel.</span><span class="sxs-lookup"><span data-stu-id="eaa52-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="eaa52-127">Igas etapis luuakse töölehe päis, millel on töölehe kanded.</span><span class="sxs-lookup"><span data-stu-id="eaa52-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="eaa52-128">See töölehe päis säiiltab sisendandmeid iga arvutusetapi kohta.</span><span class="sxs-lookup"><span data-stu-id="eaa52-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="eaa52-129">Igale töölehe reale rakendatakse poliitikad ja reeglid ning väljundina luuakse kulukirjed.</span><span class="sxs-lookup"><span data-stu-id="eaa52-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="eaa52-130">Seega on teil alati olemas põhjalik ülevaade.</span><span class="sxs-lookup"><span data-stu-id="eaa52-130">Therefore, you always have full traceability.</span></span> 
<span data-ttu-id="eaa52-131">[![Üldkulude arvutus](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="eaa52-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="eaa52-132">Elektri üldkulude arvutamine ja eraldamine</span><span class="sxs-lookup"><span data-stu-id="eaa52-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="eaa52-133">Finantsaruandluses on mõned kulud, näiteks elekter, registreeritud põhisummana.</span><span class="sxs-lookup"><span data-stu-id="eaa52-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="eaa52-134">Seetõttu ei pakuta kuluarvestuseks üksikasjalikku juhtimisülevaadet.</span><span class="sxs-lookup"><span data-stu-id="eaa52-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="eaa52-135">Kuluarvestuses peavad kulud liikuma läbi organisatsiooniüksuste, et pakkuda korrektset juhtimisülevaadet kõigi organisatsiooniüksuste ja -tasemete kohta.</span><span class="sxs-lookup"><span data-stu-id="eaa52-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="eaa52-136">See voog peab põhinema tarbimise või õiglase hindamise täpsel kirjendamisel.</span><span class="sxs-lookup"><span data-stu-id="eaa52-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="eaa52-137">Pearaamatus, saab elektrikulu sisestada nii, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="eaa52-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="eaa52-138">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="eaa52-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="eaa52-139">Kulukeskus</span><span class="sxs-lookup"><span data-stu-id="eaa52-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="eaa52-140">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="eaa52-140">Main account</span></span></th>
<th><span data-ttu-id="eaa52-141">Summa arvestusvaluutas</span><span class="sxs-lookup"><span data-stu-id="eaa52-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-142">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="eaa52-143">CC099</span><span class="sxs-lookup"><span data-stu-id="eaa52-143">CC099</span></span></td>
<td><span data-ttu-id="eaa52-144">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="eaa52-144">Default cost center</span></span></td>
<td><span data-ttu-id="eaa52-145">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-145">10001</span></span></td>
<td><span data-ttu-id="eaa52-146">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-146">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="eaa52-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="eaa52-148">1. etapp: kulukäitumise arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="eaa52-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="eaa52-149">Vaikimisi saavad lähteandmetest imporditud kulukirjed kuluarvestuses kulukäitumise klassifikatsiooniks **Klassifitseerimata**.</span><span class="sxs-lookup"><span data-stu-id="eaa52-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="eaa52-150">Kulukäitumise poliitikareegleid rakendades saate kulukirjed ümber klassifitseerida kui **Fikseeritud kulu** või **Muutuvkulu**.</span><span class="sxs-lookup"><span data-stu-id="eaa52-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="eaa52-151">Kulukäitumise reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="eaa52-151">Define the cost behavior rule</span></span>

<span data-ttu-id="eaa52-152">Mõnikord on osa kulust fikseeritud tasu ja järelejäänud kulu põhineb tarbimisel.</span><span class="sxs-lookup"><span data-stu-id="eaa52-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="eaa52-153">Elektriarved vastavad sageli sellele määratlusele.</span><span class="sxs-lookup"><span data-stu-id="eaa52-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="eaa52-154">Pärast kindla fikseeritud tasu maksmist maksate tarbimise eest kilovatt-tunni (Kwh) kohta.</span><span class="sxs-lookup"><span data-stu-id="eaa52-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="eaa52-155">Näiteks kui fikseeritud kulu tasu on 1000,00 eurot, määratletakse kulukäitumise reegel järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="eaa52-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="eaa52-156">Fikseeritud summa: 1000,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="eaa52-157">0 &lt;= 1000,00 = fikseeritud</span><span class="sxs-lookup"><span data-stu-id="eaa52-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="eaa52-158">1000,01 &lt; N = muutuja</span><span class="sxs-lookup"><span data-stu-id="eaa52-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="eaa52-159">Tööleht</span><span class="sxs-lookup"><span data-stu-id="eaa52-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="eaa52-160">Tööleht</span><span class="sxs-lookup"><span data-stu-id="eaa52-160">Journal</span></span></th>
<th><span data-ttu-id="eaa52-161">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="eaa52-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="eaa52-162">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="eaa52-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="eaa52-163">Versioon</span><span class="sxs-lookup"><span data-stu-id="eaa52-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-164">00001</span><span class="sxs-lookup"><span data-stu-id="eaa52-164">00001</span></span></td>
<td><span data-ttu-id="eaa52-165">Kulukäitumise arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="eaa52-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="eaa52-166">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="eaa52-166">Fiscal</span></span></td>
<td><span data-ttu-id="eaa52-167">2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-167">2017</span></span></td>
<td><span data-ttu-id="eaa52-168">Periood 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-168">Period 1</span></span></td>
<td><span data-ttu-id="eaa52-169">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="eaa52-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="eaa52-170">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="eaa52-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="eaa52-171">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="eaa52-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="eaa52-172">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="eaa52-173">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="eaa52-173">Cost element</span></span></th>
<th><span data-ttu-id="eaa52-174">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="eaa52-174">Cost behavior</span></span></th>
<th><span data-ttu-id="eaa52-175">Summa</span><span class="sxs-lookup"><span data-stu-id="eaa52-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-176">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="eaa52-177">CC099</span><span class="sxs-lookup"><span data-stu-id="eaa52-177">CC099</span></span></td>
<td><span data-ttu-id="eaa52-178">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="eaa52-178">Default cost center</span></span></td>
<td><span data-ttu-id="eaa52-179">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-179">10001</span></span></td>
<td><span data-ttu-id="eaa52-180">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-180">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-181">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="eaa52-181">Unclassified</span></span></td>
<td><span data-ttu-id="eaa52-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="eaa52-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="eaa52-183">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="eaa52-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-184">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="eaa52-185">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="eaa52-185">Cost element</span></span></th>
<th><span data-ttu-id="eaa52-186">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="eaa52-186">Cost behavior</span></span></th>
<th><span data-ttu-id="eaa52-187">Summa</span><span class="sxs-lookup"><span data-stu-id="eaa52-187">Amount</span></span></th>
<th><span data-ttu-id="eaa52-188">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="eaa52-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-189">CC099</span><span class="sxs-lookup"><span data-stu-id="eaa52-189">CC099</span></span></td>
<td><span data-ttu-id="eaa52-190">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="eaa52-190">Default cost center</span></span></td>
<td><span data-ttu-id="eaa52-191">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-191">10001</span></span></td>
<td><span data-ttu-id="eaa52-192">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-192">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-193">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="eaa52-193">Unclassified</span></span></td>
<td><span data-ttu-id="eaa52-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="eaa52-194">10,000.00</span></span></td>
<td><span data-ttu-id="eaa52-195">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-196">CC099</span><span class="sxs-lookup"><span data-stu-id="eaa52-196">CC099</span></span></td>
<td><span data-ttu-id="eaa52-197">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="eaa52-197">Default cost center</span></span></td>
<td><span data-ttu-id="eaa52-198">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-198">10001</span></span></td>
<td><span data-ttu-id="eaa52-199">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-199">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-200">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="eaa52-200">Unclassified</span></span></td>
<td><span data-ttu-id="eaa52-201">–10 000,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-201">-10,000.00</span></span></td>
<td><span data-ttu-id="eaa52-202">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-203">CC099</span><span class="sxs-lookup"><span data-stu-id="eaa52-203">CC099</span></span></td>
<td><span data-ttu-id="eaa52-204">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="eaa52-204">Default cost center</span></span></td>
<td><span data-ttu-id="eaa52-205">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-205">10001</span></span></td>
<td><span data-ttu-id="eaa52-206">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-206">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-207">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-207">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-208">1,000.00</span></span></td>
<td><span data-ttu-id="eaa52-209">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-210">CC099</span><span class="sxs-lookup"><span data-stu-id="eaa52-210">CC099</span></span></td>
<td><span data-ttu-id="eaa52-211">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="eaa52-211">Default cost center</span></span></td>
<td><span data-ttu-id="eaa52-212">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-212">10001</span></span></td>
<td><span data-ttu-id="eaa52-213">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-213">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-214">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-214">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="eaa52-215">9,000.00</span></span></td>
<td><span data-ttu-id="eaa52-216">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="eaa52-217">Üksikasjalikku teavet kulukäitumise kohta vt jaotisest Kulukäitumise poliitika.</span><span class="sxs-lookup"><span data-stu-id="eaa52-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="eaa52-218">(Pange tähele, et see teema pole veel valmis, kuid see tuleb peagi.)</span><span class="sxs-lookup"><span data-stu-id="eaa52-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="eaa52-219">2. etapp: kulujaotuse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="eaa52-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="eaa52-220">Kulujaotust kasutatakse kulu ümberjaotamiseks ühelt kuluobjektilt ühele või mitmele teisele kuluobjektile, rakendades asjakohast eraldusalust.</span><span class="sxs-lookup"><span data-stu-id="eaa52-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="eaa52-221">Kulujaotus ja kulueraldus erinevad selle poolest, et kulujaotus toimub alati algse kulu esmase kuluelemendi tasemel.</span><span class="sxs-lookup"><span data-stu-id="eaa52-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="eaa52-222">Kulujaotuse reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="eaa52-222">Define the cost distribution rule</span></span>

<span data-ttu-id="eaa52-223">Finantsaruandluses registreeritakse elektrikulud sageli põhisummana.</span><span class="sxs-lookup"><span data-stu-id="eaa52-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="eaa52-224">Kuluarvestuseses ei ole see lähenemine piisavalt üksikasjalik.</span><span class="sxs-lookup"><span data-stu-id="eaa52-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="eaa52-225">Muutuvkulu tuleb jaotada üksikutele kuluobjektidele õigluse alusel.</span><span class="sxs-lookup"><span data-stu-id="eaa52-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="eaa52-226">Kõige loogilisem eraldamisalus on elektritarbimine (kWh).</span><span class="sxs-lookup"><span data-stu-id="eaa52-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="eaa52-227">Luuakse statistilise dimensiooni liige nimega Elekter ja elektritarbimine on kirjendatakse.</span><span class="sxs-lookup"><span data-stu-id="eaa52-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="eaa52-228">Vaikimisi muutuvad kõik statistilise dimensiooni liikmed eraldamisalusena kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="eaa52-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-229">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-229">Cost object</span></span></th>
<th><span data-ttu-id="eaa52-230">kWh</span><span class="sxs-lookup"><span data-stu-id="eaa52-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-231">CC001</span><span class="sxs-lookup"><span data-stu-id="eaa52-231">CC001</span></span></td>
<td><span data-ttu-id="eaa52-232">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="eaa52-232">HR</span></span></td>
<td><span data-ttu-id="eaa52-233">1000</span><span class="sxs-lookup"><span data-stu-id="eaa52-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-234">CC002</span><span class="sxs-lookup"><span data-stu-id="eaa52-234">CC002</span></span></td>
<td><span data-ttu-id="eaa52-235">Finantsid</span><span class="sxs-lookup"><span data-stu-id="eaa52-235">Finance</span></span></td>
<td><span data-ttu-id="eaa52-236">6,000</span><span class="sxs-lookup"><span data-stu-id="eaa52-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-237">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-237">CC003</span></span></td>
<td><span data-ttu-id="eaa52-238">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-238">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-239">0</span><span class="sxs-lookup"><span data-stu-id="eaa52-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="eaa52-240">Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="eaa52-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-241">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-241">Cost object</span></span></th>
<th><span data-ttu-id="eaa52-242">Väärtus</span><span class="sxs-lookup"><span data-stu-id="eaa52-242">Magnitude</span></span></th>
<th><span data-ttu-id="eaa52-243">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="eaa52-243">Allocation factor</span></span></th>
<th><span data-ttu-id="eaa52-244">Summa</span><span class="sxs-lookup"><span data-stu-id="eaa52-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-245">CC001</span><span class="sxs-lookup"><span data-stu-id="eaa52-245">CC001</span></span></td>
<td><span data-ttu-id="eaa52-246">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="eaa52-246">HR</span></span></td>
<td><span data-ttu-id="eaa52-247">1000</span><span class="sxs-lookup"><span data-stu-id="eaa52-247">1,000</span></span></td>
<td><span data-ttu-id="eaa52-248">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="eaa52-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="eaa52-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-250">CC002</span><span class="sxs-lookup"><span data-stu-id="eaa52-250">CC002</span></span></td>
<td><span data-ttu-id="eaa52-251">Finantsid</span><span class="sxs-lookup"><span data-stu-id="eaa52-251">Finance</span></span></td>
<td><span data-ttu-id="eaa52-252">6,000</span><span class="sxs-lookup"><span data-stu-id="eaa52-252">6,000</span></span></td>
<td><span data-ttu-id="eaa52-253">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="eaa52-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="eaa52-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-255">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-255">CC003</span></span></td>
<td><span data-ttu-id="eaa52-256">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-256">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-257">0</span><span class="sxs-lookup"><span data-stu-id="eaa52-257">0</span></span></td>
<td><span data-ttu-id="eaa52-258">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="eaa52-259">0,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="eaa52-260">Fikseeritud kulu tuleb jaotada ühtlaselt üksikutele kuluobjektidele, mis on tarbinud elektrit.</span><span class="sxs-lookup"><span data-stu-id="eaa52-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="eaa52-261">Selle tulemuse saate, kasutades valemi eraldamisaluses statistilise dimensiooni liiget Elekter: (Elekter &gt; 0,00). Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="eaa52-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-262">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-262">Cost object</span></span></th>
<th><span data-ttu-id="eaa52-263">Valem</span><span class="sxs-lookup"><span data-stu-id="eaa52-263">Formula</span></span></th>
<th><span data-ttu-id="eaa52-264">Väärtus</span><span class="sxs-lookup"><span data-stu-id="eaa52-264">Magnitude</span></span></th>
<th><span data-ttu-id="eaa52-265">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="eaa52-265">Allocation factor</span></span></th>
<th><span data-ttu-id="eaa52-266">Summa</span><span class="sxs-lookup"><span data-stu-id="eaa52-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-267">CC001</span><span class="sxs-lookup"><span data-stu-id="eaa52-267">CC001</span></span></td>
<td><span data-ttu-id="eaa52-268">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="eaa52-268">HR</span></span></td>
<td><span data-ttu-id="eaa52-269">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="eaa52-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="eaa52-270">1</span><span class="sxs-lookup"><span data-stu-id="eaa52-270">1</span></span></td>
<td><span data-ttu-id="eaa52-271">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="eaa52-272">500,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-273">CC002</span><span class="sxs-lookup"><span data-stu-id="eaa52-273">CC002</span></span></td>
<td><span data-ttu-id="eaa52-274">Finantsid</span><span class="sxs-lookup"><span data-stu-id="eaa52-274">Finance</span></span></td>
<td><span data-ttu-id="eaa52-275">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="eaa52-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="eaa52-276">1</span><span class="sxs-lookup"><span data-stu-id="eaa52-276">1</span></span></td>
<td><span data-ttu-id="eaa52-277">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="eaa52-278">500,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-279">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-279">CC003</span></span></td>
<td><span data-ttu-id="eaa52-280">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-280">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="eaa52-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="eaa52-282">0</span><span class="sxs-lookup"><span data-stu-id="eaa52-282">0</span></span></td>
<td><span data-ttu-id="eaa52-283">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="eaa52-284">0,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="eaa52-285">Tööleht</span><span class="sxs-lookup"><span data-stu-id="eaa52-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="eaa52-286">Tööleht</span><span class="sxs-lookup"><span data-stu-id="eaa52-286">Journal</span></span></th>
<th><span data-ttu-id="eaa52-287">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="eaa52-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="eaa52-288">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="eaa52-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="eaa52-289">Versioon</span><span class="sxs-lookup"><span data-stu-id="eaa52-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-290">00002</span><span class="sxs-lookup"><span data-stu-id="eaa52-290">00002</span></span></td>
<td><span data-ttu-id="eaa52-291">Kulujaotuse arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="eaa52-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="eaa52-292">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="eaa52-292">Fiscal</span></span></td>
<td><span data-ttu-id="eaa52-293">2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-293">2017</span></span></td>
<td><span data-ttu-id="eaa52-294">Periood 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-294">Period 1</span></span></td>
<td><span data-ttu-id="eaa52-295">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="eaa52-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="eaa52-296">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="eaa52-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="eaa52-297">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="eaa52-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="eaa52-298">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="eaa52-299">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="eaa52-299">Cost element</span></span></th>
<th><span data-ttu-id="eaa52-300">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="eaa52-300">Cost behavior</span></span></th>
<th><span data-ttu-id="eaa52-301">Summa</span><span class="sxs-lookup"><span data-stu-id="eaa52-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-302">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="eaa52-303">CC099</span><span class="sxs-lookup"><span data-stu-id="eaa52-303">CC099</span></span></td>
<td><span data-ttu-id="eaa52-304">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="eaa52-304">Default cost center</span></span></td>
<td><span data-ttu-id="eaa52-305">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-305">10001</span></span></td>
<td><span data-ttu-id="eaa52-306">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-306">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-307">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-307">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-308">1 000,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-309">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="eaa52-310">CC099</span><span class="sxs-lookup"><span data-stu-id="eaa52-310">CC099</span></span></td>
<td><span data-ttu-id="eaa52-311">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="eaa52-311">Default cost center</span></span></td>
<td><span data-ttu-id="eaa52-312">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-312">10001</span></span></td>
<td><span data-ttu-id="eaa52-313">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-313">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-314">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-314">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="eaa52-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="eaa52-316">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="eaa52-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-317">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="eaa52-318">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="eaa52-318">Cost element</span></span></th>
<th><span data-ttu-id="eaa52-319">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="eaa52-319">Cost behavior</span></span></th>
<th><span data-ttu-id="eaa52-320">Summa</span><span class="sxs-lookup"><span data-stu-id="eaa52-320">Amount</span></span></th>
<th><span data-ttu-id="eaa52-321">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="eaa52-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-322">CC099</span><span class="sxs-lookup"><span data-stu-id="eaa52-322">CC099</span></span></td>
<td><span data-ttu-id="eaa52-323">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="eaa52-323">Default cost center</span></span></td>
<td><span data-ttu-id="eaa52-324">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-324">10001</span></span></td>
<td><span data-ttu-id="eaa52-325">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-325">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-326">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-326">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-327">–1000,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-327">-1,000.00</span></span></td>
<td><span data-ttu-id="eaa52-328">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-329">CC001</span><span class="sxs-lookup"><span data-stu-id="eaa52-329">CC001</span></span></td>
<td><span data-ttu-id="eaa52-330">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="eaa52-330">HR</span></span></td>
<td><span data-ttu-id="eaa52-331">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-331">10001</span></span></td>
<td><span data-ttu-id="eaa52-332">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-332">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-333">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-333">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-334">500,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-334">500.00</span></span></td>
<td><span data-ttu-id="eaa52-335">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-336">CC002</span><span class="sxs-lookup"><span data-stu-id="eaa52-336">CC002</span></span></td>
<td><span data-ttu-id="eaa52-337">Finantsid</span><span class="sxs-lookup"><span data-stu-id="eaa52-337">Finance</span></span></td>
<td><span data-ttu-id="eaa52-338">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-338">10001</span></span></td>
<td><span data-ttu-id="eaa52-339">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-339">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-340">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-340">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-341">500,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-341">500.00</span></span></td>
<td><span data-ttu-id="eaa52-342">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-343">CC099</span><span class="sxs-lookup"><span data-stu-id="eaa52-343">CC099</span></span></td>
<td><span data-ttu-id="eaa52-344">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="eaa52-344">Default cost center</span></span></td>
<td><span data-ttu-id="eaa52-345">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-345">10001</span></span></td>
<td><span data-ttu-id="eaa52-346">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-346">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-347">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-347">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-348">–9000,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-348">-9,000.00</span></span></td>
<td><span data-ttu-id="eaa52-349">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-350">CC001</span><span class="sxs-lookup"><span data-stu-id="eaa52-350">CC001</span></span></td>
<td><span data-ttu-id="eaa52-351">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="eaa52-351">HR</span></span></td>
<td><span data-ttu-id="eaa52-352">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-352">10001</span></span></td>
<td><span data-ttu-id="eaa52-353">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-353">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-354">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-354">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="eaa52-355">1,285.71</span></span></td>
<td><span data-ttu-id="eaa52-356">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-357">CC002</span><span class="sxs-lookup"><span data-stu-id="eaa52-357">CC002</span></span></td>
<td><span data-ttu-id="eaa52-358">Finantsid</span><span class="sxs-lookup"><span data-stu-id="eaa52-358">Finance</span></span></td>
<td><span data-ttu-id="eaa52-359">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-359">10001</span></span></td>
<td><span data-ttu-id="eaa52-360">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-360">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-361">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-361">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="eaa52-362">7,714.29</span></span></td>
<td><span data-ttu-id="eaa52-363">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="eaa52-364">Üksikasjalikku teavet kulude jaotamise ja eraldamise aluse kohta vt jaotistest Kulujaotuse poliitika ja Eraldamisalused.</span><span class="sxs-lookup"><span data-stu-id="eaa52-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="eaa52-365">(Pange tähele, et see teema pole veel valmis, kuid see tuleb peagi.)</span><span class="sxs-lookup"><span data-stu-id="eaa52-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="eaa52-366">3. etapp: üldkulude määra arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="eaa52-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="eaa52-367">Üldkulude määra kasutatakse ühe või mitme kindla kuluobjekti debiteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="eaa52-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="eaa52-368">Tasu põhineb eelmääratud kulumääral ja väärtusel määratud eraldamisalusest.</span><span class="sxs-lookup"><span data-stu-id="eaa52-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="eaa52-369">Üldkulu määra määratlemine</span><span class="sxs-lookup"><span data-stu-id="eaa52-369">Define the overhead rate</span></span>

<span data-ttu-id="eaa52-370">Kuluobjekt CC001 inimressursid panustab sisemiste projektide kogumisse.</span><span class="sxs-lookup"><span data-stu-id="eaa52-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="eaa52-371">Luuakse statistilise dimensiooni liige nimega Inimressursside projektid, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="eaa52-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-372">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-372">Cost object</span></span></th>
<th><span data-ttu-id="eaa52-373">Tunnid</span><span class="sxs-lookup"><span data-stu-id="eaa52-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-374">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-374">Proj 1</span></span></td>
<td><span data-ttu-id="eaa52-375">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-375">Project 1</span></span></td>
<td><span data-ttu-id="eaa52-376">3</span><span class="sxs-lookup"><span data-stu-id="eaa52-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-377">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-377">Proj 2</span></span></td>
<td><span data-ttu-id="eaa52-378">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-378">Project 2</span></span></td>
<td><span data-ttu-id="eaa52-379">1</span><span class="sxs-lookup"><span data-stu-id="eaa52-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="eaa52-380">Määratletud on eelmääratud kulumäär kuluprojektide panusele.</span><span class="sxs-lookup"><span data-stu-id="eaa52-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-381">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-381">Cost object</span></span></th>
<th><span data-ttu-id="eaa52-382">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="eaa52-382">Cost element</span></span></th>
<th><span data-ttu-id="eaa52-383">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="eaa52-383">Cost behavior</span></span></th>
<th><span data-ttu-id="eaa52-384">Ühikud</span><span class="sxs-lookup"><span data-stu-id="eaa52-384">Units</span></span></th>
<th><span data-ttu-id="eaa52-385">Kurss</span><span class="sxs-lookup"><span data-stu-id="eaa52-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-386">CC001</span><span class="sxs-lookup"><span data-stu-id="eaa52-386">CC001</span></span></td>
<td><span data-ttu-id="eaa52-387">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="eaa52-387">HR</span></span></td>
<td><span data-ttu-id="eaa52-388">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-388">10001</span></span></td>
<td><span data-ttu-id="eaa52-389">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-389">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-390">1</span><span class="sxs-lookup"><span data-stu-id="eaa52-390">1</span></span></td>
<td><span data-ttu-id="eaa52-391">10</span><span class="sxs-lookup"><span data-stu-id="eaa52-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="eaa52-392">Järgmises tabelis on näidatud tulemus, kui inimressursside projektid on rakendatud eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="eaa52-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-393">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-393">Cost object</span></span></th>
<th><span data-ttu-id="eaa52-394">Väärtus</span><span class="sxs-lookup"><span data-stu-id="eaa52-394">Magnitude</span></span></th>
<th><span data-ttu-id="eaa52-395">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="eaa52-395">Cost element</span></span></th>
<th><span data-ttu-id="eaa52-396">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="eaa52-396">Allocation factor</span></span></th>
<th><span data-ttu-id="eaa52-397">Summa</span><span class="sxs-lookup"><span data-stu-id="eaa52-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-398">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-398">Proj 1</span></span></td>
<td><span data-ttu-id="eaa52-399">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-399">Project 1</span></span></td>
<td><span data-ttu-id="eaa52-400">3</span><span class="sxs-lookup"><span data-stu-id="eaa52-400">3</span></span></td>
<td><span data-ttu-id="eaa52-401">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-401">10001</span></span></td>
<td><span data-ttu-id="eaa52-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="eaa52-403">30,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-404">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-404">Proj 2</span></span></td>
<td><span data-ttu-id="eaa52-405">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-405">Project 2</span></span></td>
<td><span data-ttu-id="eaa52-406">1</span><span class="sxs-lookup"><span data-stu-id="eaa52-406">1</span></span></td>
<td><span data-ttu-id="eaa52-407">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-407">10001</span></span></td>
<td><span data-ttu-id="eaa52-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="eaa52-409">10,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="eaa52-410">Tööleht</span><span class="sxs-lookup"><span data-stu-id="eaa52-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="eaa52-411">Tööleht</span><span class="sxs-lookup"><span data-stu-id="eaa52-411">Journal</span></span></th>
<th><span data-ttu-id="eaa52-412">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="eaa52-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="eaa52-413">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="eaa52-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="eaa52-414">Versioon</span><span class="sxs-lookup"><span data-stu-id="eaa52-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-415">00003</span><span class="sxs-lookup"><span data-stu-id="eaa52-415">00003</span></span></td>
<td><span data-ttu-id="eaa52-416">Üldkulu määra arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="eaa52-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="eaa52-417">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="eaa52-417">Fiscal</span></span></td>
<td><span data-ttu-id="eaa52-418">2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-418">2017</span></span></td>
<td><span data-ttu-id="eaa52-419">Periood 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-419">Period 1</span></span></td>
<td><span data-ttu-id="eaa52-420">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="eaa52-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="eaa52-421">Töölehe sisestused (töölehe sisestused üldkulu määra arvutamiseks)</span><span class="sxs-lookup"><span data-stu-id="eaa52-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="eaa52-422">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="eaa52-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="eaa52-423">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-423">Cost object</span></span></th>
<th><span data-ttu-id="eaa52-424">Väärtus</span><span class="sxs-lookup"><span data-stu-id="eaa52-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-425">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="eaa52-426">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-426">Proj 1</span></span></td>
<td><span data-ttu-id="eaa52-427">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="eaa52-428">3,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-429">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="eaa52-430">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-430">Proj 2</span></span></td>
<td><span data-ttu-id="eaa52-431">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="eaa52-432">1,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="eaa52-433">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="eaa52-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-434">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="eaa52-435">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="eaa52-435">Cost element</span></span></th>
<th><span data-ttu-id="eaa52-436">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="eaa52-436">Cost behavior</span></span></th>
<th><span data-ttu-id="eaa52-437">Summa</span><span class="sxs-lookup"><span data-stu-id="eaa52-437">Amount</span></span></th>
<th><span data-ttu-id="eaa52-438">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="eaa52-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="eaa52-439">CC0001</span></span></td>
<td><span data-ttu-id="eaa52-440">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="eaa52-440">HR</span></span></td>
<td><span data-ttu-id="eaa52-441">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-441">10001</span></span></td>
<td><span data-ttu-id="eaa52-442">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-442">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-443">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-443">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-444">–30,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-444">-30.00</span></span></td>
<td><span data-ttu-id="eaa52-445">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-446">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-446">Proj 1</span></span></td>
<td><span data-ttu-id="eaa52-447">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="eaa52-448">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-448">10001</span></span></td>
<td><span data-ttu-id="eaa52-449">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-449">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-450">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-450">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-451">30,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-451">30.00</span></span></td>
<td><span data-ttu-id="eaa52-452">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-453">CC001</span><span class="sxs-lookup"><span data-stu-id="eaa52-453">CC001</span></span></td>
<td><span data-ttu-id="eaa52-454">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="eaa52-454">HR</span></span></td>
<td><span data-ttu-id="eaa52-455">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-455">10001</span></span></td>
<td><span data-ttu-id="eaa52-456">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-456">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-457">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-457">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-458">-10.00</span></span></td>
<td><span data-ttu-id="eaa52-459">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-460">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-460">Proj 2</span></span></td>
<td><span data-ttu-id="eaa52-461">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="eaa52-462">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-462">10001</span></span></td>
<td><span data-ttu-id="eaa52-463">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-463">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-464">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-464">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-465">10,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-465">10.00</span></span></td>
<td><span data-ttu-id="eaa52-466">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="eaa52-467">Üksikasjalikku teavet üldkulu määra poliitika kohta vt jaotistest Üldkulu määra poliitika ja Eraldamisalused.</span><span class="sxs-lookup"><span data-stu-id="eaa52-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="eaa52-468">(Pange tähele, et see teema pole veel valmis, kuid see tuleb peagi.)</span><span class="sxs-lookup"><span data-stu-id="eaa52-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="eaa52-469">4. etapp: kulueralduse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="eaa52-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="eaa52-470">Eraldamist kasutatakse kuluobjekti saldo eraldamiseks teistele kuluobjektidele, rakendades eraldamisalust.</span><span class="sxs-lookup"><span data-stu-id="eaa52-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="eaa52-471">Finance and Operations toetab vastastikuse eraldamise meetodit.</span><span class="sxs-lookup"><span data-stu-id="eaa52-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="eaa52-472">Vastastikuse eraldamise meetodi puhul tuvastatakse täiendavate kuluobjektide vahetatavad vastastikused teenused.</span><span class="sxs-lookup"><span data-stu-id="eaa52-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="eaa52-473">Süsteem määrab automaatselt eraldamiste tegemise õige järjekorra.</span><span class="sxs-lookup"><span data-stu-id="eaa52-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="eaa52-474">Kuluobjekti saldo eraldatakse üksiku eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="eaa52-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="eaa52-475">Toetatakse eraldamisi kuluobjektide dimensioonide ja nende vastavate liikmete seas.</span><span class="sxs-lookup"><span data-stu-id="eaa52-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="eaa52-476">Eraldamisjärjekorda reguleerib kulujuhtseade.</span><span class="sxs-lookup"><span data-stu-id="eaa52-476">The allocation order is controlled by the cost control unit.</span></span> <span data-ttu-id="eaa52-477">[![Vastastikune meetod](./media/reciprocal-method.png)]</span><span class="sxs-lookup"><span data-stu-id="eaa52-477">[![Reciprocal method](./media/reciprocal-method.png)]</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="eaa52-478">Kulueraldamise määratlemine</span><span class="sxs-lookup"><span data-stu-id="eaa52-478">Define the cost allocation</span></span>

<span data-ttu-id="eaa52-479">Siin on lihtne näide, mis selgitab, kuidas jälgida kulu liikumist.</span><span class="sxs-lookup"><span data-stu-id="eaa52-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="eaa52-480">Kuluobjekt CC001 inimressursid panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="eaa52-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="eaa52-481">Luuakse statistilise dimensiooni liige nimega Inimressursside teenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="eaa52-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-482">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-482">Cost object</span></span></th>
<th><span data-ttu-id="eaa52-483">Inimressursside teenused</span><span class="sxs-lookup"><span data-stu-id="eaa52-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-484">CC002</span><span class="sxs-lookup"><span data-stu-id="eaa52-484">CC002</span></span></td>
<td><span data-ttu-id="eaa52-485">Finantsid</span><span class="sxs-lookup"><span data-stu-id="eaa52-485">Finance</span></span></td>
<td><span data-ttu-id="eaa52-486">35</span><span class="sxs-lookup"><span data-stu-id="eaa52-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-487">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-487">CC003</span></span></td>
<td><span data-ttu-id="eaa52-488">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-488">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-489">55</span><span class="sxs-lookup"><span data-stu-id="eaa52-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-490">CC004</span><span class="sxs-lookup"><span data-stu-id="eaa52-490">CC004</span></span></td>
<td><span data-ttu-id="eaa52-491">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="eaa52-491">Packaging</span></span></td>
<td><span data-ttu-id="eaa52-492">10</span><span class="sxs-lookup"><span data-stu-id="eaa52-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="eaa52-493">Kuluobjekt CC002 rahandus panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="eaa52-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="eaa52-494">Luuakse statistilise dimensiooni liige nimega Rahandusteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="eaa52-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-495">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-495">Cost object</span></span></th>
<th><span data-ttu-id="eaa52-496">Rahandusteenused</span><span class="sxs-lookup"><span data-stu-id="eaa52-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-497">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-497">CC003</span></span></td>
<td><span data-ttu-id="eaa52-498">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-498">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-499">65</span><span class="sxs-lookup"><span data-stu-id="eaa52-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-500">CC004</span><span class="sxs-lookup"><span data-stu-id="eaa52-500">CC004</span></span></td>
<td><span data-ttu-id="eaa52-501">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="eaa52-501">Packaging</span></span></td>
<td><span data-ttu-id="eaa52-502">35</span><span class="sxs-lookup"><span data-stu-id="eaa52-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="eaa52-503">Kuluobjekt CC003 assembler panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="eaa52-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="eaa52-504">Luuakse statistilise dimensiooni liige nimega Assembleriteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="eaa52-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-505">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-505">Cost object</span></span></th>
<th><span data-ttu-id="eaa52-506">Assembleriteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="eaa52-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-507">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-507">Prod 1</span></span></td>
<td><span data-ttu-id="eaa52-508">Toode 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-508">Product 1</span></span></td>
<td><span data-ttu-id="eaa52-509">60</span><span class="sxs-lookup"><span data-stu-id="eaa52-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-510">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-510">Prod 2</span></span></td>
<td><span data-ttu-id="eaa52-511">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-511">Product 2</span></span></td>
<td><span data-ttu-id="eaa52-512">20</span><span class="sxs-lookup"><span data-stu-id="eaa52-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="eaa52-513">Kuluobjekt CC004 pakendamine panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="eaa52-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="eaa52-514">Luuakse statistilise dimensiooni liige nimega Pakendamisteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="eaa52-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-515">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-515">Cost object</span></span></th>
<th><span data-ttu-id="eaa52-516">Pakendamisteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="eaa52-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-517">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-517">Prod 1</span></span></td>
<td><span data-ttu-id="eaa52-518">Toode 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-518">Product 1</span></span></td>
<td><span data-ttu-id="eaa52-519">80</span><span class="sxs-lookup"><span data-stu-id="eaa52-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-520">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-520">Prod 2</span></span></td>
<td><span data-ttu-id="eaa52-521">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-521">Product 2</span></span></td>
<td><span data-ttu-id="eaa52-522">sept.</span><span class="sxs-lookup"><span data-stu-id="eaa52-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="eaa52-523">**Märkus.** Finance and Operationsis saab statistilised mõõdud, nagu toote tarbitud tootmistunnid, tuletada lähteandmetest.</span><span class="sxs-lookup"><span data-stu-id="eaa52-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="eaa52-524">Üksikasjalikku teavet statistiliste mõõtude pakkujate kohta vt jaotisest Statistilise mõõdu pakkuja mall.</span><span class="sxs-lookup"><span data-stu-id="eaa52-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="eaa52-525">(Pange tähele, et see teema pole veel valmis, kuid see tuleb peagi.) Järgmises tabelis on näidatud tulemus, kui Inimressursside teenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud kulu ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="eaa52-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-526">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-526">Cost object</span></span></th>
<th><span data-ttu-id="eaa52-527">Väärtus</span><span class="sxs-lookup"><span data-stu-id="eaa52-527">Magnitude</span></span></th>
<th><span data-ttu-id="eaa52-528">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="eaa52-528">Allocation factor</span></span></th>
<th><span data-ttu-id="eaa52-529">Summa</span><span class="sxs-lookup"><span data-stu-id="eaa52-529">Amount</span></span></th>
<th><span data-ttu-id="eaa52-530">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="eaa52-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-531">CC002</span><span class="sxs-lookup"><span data-stu-id="eaa52-531">CC002</span></span></td>
<td><span data-ttu-id="eaa52-532">Finantsid</span><span class="sxs-lookup"><span data-stu-id="eaa52-532">Finance</span></span></td>
<td><span data-ttu-id="eaa52-533">35</span><span class="sxs-lookup"><span data-stu-id="eaa52-533">35</span></span></td>
<td><span data-ttu-id="eaa52-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="eaa52-535">175.00</span><span class="sxs-lookup"><span data-stu-id="eaa52-535">175.00</span></span></td>
<td><span data-ttu-id="eaa52-536">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-537">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-537">CC003</span></span></td>
<td><span data-ttu-id="eaa52-538">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-538">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-539">55</span><span class="sxs-lookup"><span data-stu-id="eaa52-539">55</span></span></td>
<td><span data-ttu-id="eaa52-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="eaa52-541">275.00</span><span class="sxs-lookup"><span data-stu-id="eaa52-541">275.00</span></span></td>
<td><span data-ttu-id="eaa52-542">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-543">CC004</span><span class="sxs-lookup"><span data-stu-id="eaa52-543">CC004</span></span></td>
<td><span data-ttu-id="eaa52-544">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="eaa52-544">Packaging</span></span></td>
<td><span data-ttu-id="eaa52-545">10</span><span class="sxs-lookup"><span data-stu-id="eaa52-545">10</span></span></td>
<td><span data-ttu-id="eaa52-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="eaa52-547">50,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-547">50.00</span></span></td>
<td><span data-ttu-id="eaa52-548">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-549">CC002</span><span class="sxs-lookup"><span data-stu-id="eaa52-549">CC002</span></span></td>
<td><span data-ttu-id="eaa52-550">Finantsid</span><span class="sxs-lookup"><span data-stu-id="eaa52-550">Finance</span></span></td>
<td><span data-ttu-id="eaa52-551">35</span><span class="sxs-lookup"><span data-stu-id="eaa52-551">35</span></span></td>
<td><span data-ttu-id="eaa52-552">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="eaa52-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="eaa52-553">436.00</span><span class="sxs-lookup"><span data-stu-id="eaa52-553">436.00</span></span></td>
<td><span data-ttu-id="eaa52-554">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-555">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-555">CC003</span></span></td>
<td><span data-ttu-id="eaa52-556">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-556">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-557">55</span><span class="sxs-lookup"><span data-stu-id="eaa52-557">55</span></span></td>
<td><span data-ttu-id="eaa52-558">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="eaa52-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="eaa52-559">685.14</span><span class="sxs-lookup"><span data-stu-id="eaa52-559">685.14</span></span></td>
<td><span data-ttu-id="eaa52-560">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-561">CC004</span><span class="sxs-lookup"><span data-stu-id="eaa52-561">CC004</span></span></td>
<td><span data-ttu-id="eaa52-562">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="eaa52-562">Packaging</span></span></td>
<td><span data-ttu-id="eaa52-563">10</span><span class="sxs-lookup"><span data-stu-id="eaa52-563">10</span></span></td>
<td><span data-ttu-id="eaa52-564">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="eaa52-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="eaa52-565">124.57</span><span class="sxs-lookup"><span data-stu-id="eaa52-565">124.57</span></span></td>
<td><span data-ttu-id="eaa52-566">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="eaa52-567">Järgmises tabelis on näidatud tulemus, kui Rahandusteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="eaa52-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-568">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-568">Cost object</span></span></th>
<th><span data-ttu-id="eaa52-569">Väärtus</span><span class="sxs-lookup"><span data-stu-id="eaa52-569">Magnitude</span></span></th>
<th><span data-ttu-id="eaa52-570">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="eaa52-570">Allocation factor</span></span></th>
<th><span data-ttu-id="eaa52-571">Summa</span><span class="sxs-lookup"><span data-stu-id="eaa52-571">Amount</span></span></th>
<th><span data-ttu-id="eaa52-572">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="eaa52-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-573">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-573">CC003</span></span></td>
<td><span data-ttu-id="eaa52-574">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-574">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-575">65</span><span class="sxs-lookup"><span data-stu-id="eaa52-575">65</span></span></td>
<td><span data-ttu-id="eaa52-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="eaa52-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="eaa52-577">438.75</span><span class="sxs-lookup"><span data-stu-id="eaa52-577">438.75</span></span></td>
<td><span data-ttu-id="eaa52-578">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-579">CC004</span><span class="sxs-lookup"><span data-stu-id="eaa52-579">CC004</span></span></td>
<td><span data-ttu-id="eaa52-580">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="eaa52-580">Packaging</span></span></td>
<td><span data-ttu-id="eaa52-581">35</span><span class="sxs-lookup"><span data-stu-id="eaa52-581">35</span></span></td>
<td><span data-ttu-id="eaa52-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="eaa52-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="eaa52-583">236.25</span><span class="sxs-lookup"><span data-stu-id="eaa52-583">236.25</span></span></td>
<td><span data-ttu-id="eaa52-584">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-585">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-585">CC003</span></span></td>
<td><span data-ttu-id="eaa52-586">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-586">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-587">65</span><span class="sxs-lookup"><span data-stu-id="eaa52-587">65</span></span></td>
<td><span data-ttu-id="eaa52-588">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="eaa52-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="eaa52-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="eaa52-589">5,297.69</span></span></td>
<td><span data-ttu-id="eaa52-590">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-591">CC004</span><span class="sxs-lookup"><span data-stu-id="eaa52-591">CC004</span></span></td>
<td><span data-ttu-id="eaa52-592">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="eaa52-592">Packaging</span></span></td>
<td><span data-ttu-id="eaa52-593">35</span><span class="sxs-lookup"><span data-stu-id="eaa52-593">35</span></span></td>
<td><span data-ttu-id="eaa52-594">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="eaa52-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="eaa52-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="eaa52-595">2,852.60</span></span></td>
<td><span data-ttu-id="eaa52-596">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="eaa52-597">Järgmises tabelis on näidatud tulemus, kui Assembleriteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="eaa52-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-598">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-598">Cost object</span></span></th>
<th><span data-ttu-id="eaa52-599">Väärtus</span><span class="sxs-lookup"><span data-stu-id="eaa52-599">Magnitude</span></span></th>
<th><span data-ttu-id="eaa52-600">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="eaa52-600">Allocation factor</span></span></th>
<th><span data-ttu-id="eaa52-601">Summa</span><span class="sxs-lookup"><span data-stu-id="eaa52-601">Amount</span></span></th>
<th><span data-ttu-id="eaa52-602">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="eaa52-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-603">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-603">Prod 1</span></span></td>
<td><span data-ttu-id="eaa52-604">Toode 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-604">Product 1</span></span></td>
<td><span data-ttu-id="eaa52-605">60</span><span class="sxs-lookup"><span data-stu-id="eaa52-605">60</span></span></td>
<td><span data-ttu-id="eaa52-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="eaa52-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="eaa52-607">535.31</span><span class="sxs-lookup"><span data-stu-id="eaa52-607">535.31</span></span></td>
<td><span data-ttu-id="eaa52-608">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-609">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-609">Prod 2</span></span></td>
<td><span data-ttu-id="eaa52-610">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-610">Product 2</span></span></td>
<td><span data-ttu-id="eaa52-611">20</span><span class="sxs-lookup"><span data-stu-id="eaa52-611">20</span></span></td>
<td><span data-ttu-id="eaa52-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="eaa52-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="eaa52-613">178.44</span><span class="sxs-lookup"><span data-stu-id="eaa52-613">178.44</span></span></td>
<td><span data-ttu-id="eaa52-614">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-615">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-615">Prod 1</span></span></td>
<td><span data-ttu-id="eaa52-616">Toode 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-616">Product 1</span></span></td>
<td><span data-ttu-id="eaa52-617">60</span><span class="sxs-lookup"><span data-stu-id="eaa52-617">60</span></span></td>
<td><span data-ttu-id="eaa52-618">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="eaa52-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="eaa52-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="eaa52-619">4,487.12</span></span></td>
<td><span data-ttu-id="eaa52-620">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-621">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-621">Prod 2</span></span></td>
<td><span data-ttu-id="eaa52-622">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-622">Product 2</span></span></td>
<td><span data-ttu-id="eaa52-623">20</span><span class="sxs-lookup"><span data-stu-id="eaa52-623">20</span></span></td>
<td><span data-ttu-id="eaa52-624">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="eaa52-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="eaa52-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="eaa52-625">1,495.71</span></span></td>
<td><span data-ttu-id="eaa52-626">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="eaa52-627">Järgmises tabelis on näidatud tulemus, kui Pakendamisteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="eaa52-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-628">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-628">Cost object</span></span></th>
<th><span data-ttu-id="eaa52-629">Väärtus</span><span class="sxs-lookup"><span data-stu-id="eaa52-629">Magnitude</span></span></th>
<th><span data-ttu-id="eaa52-630">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="eaa52-630">Allocation factor</span></span></th>
<th><span data-ttu-id="eaa52-631">Summa</span><span class="sxs-lookup"><span data-stu-id="eaa52-631">Amount</span></span></th>
<th><span data-ttu-id="eaa52-632">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="eaa52-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-633">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-633">Prod 1</span></span></td>
<td><span data-ttu-id="eaa52-634">Toode 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-634">Product 1</span></span></td>
<td><span data-ttu-id="eaa52-635">80</span><span class="sxs-lookup"><span data-stu-id="eaa52-635">80</span></span></td>
<td><span data-ttu-id="eaa52-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="eaa52-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="eaa52-637">241.05</span><span class="sxs-lookup"><span data-stu-id="eaa52-637">241.05</span></span></td>
<td><span data-ttu-id="eaa52-638">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-639">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-639">Prod 2</span></span></td>
<td><span data-ttu-id="eaa52-640">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-640">Product 2</span></span></td>
<td><span data-ttu-id="eaa52-641">15</span><span class="sxs-lookup"><span data-stu-id="eaa52-641">15</span></span></td>
<td><span data-ttu-id="eaa52-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="eaa52-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="eaa52-643">45.20</span><span class="sxs-lookup"><span data-stu-id="eaa52-643">45.20</span></span></td>
<td><span data-ttu-id="eaa52-644">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-645">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-645">Prod 1</span></span></td>
<td><span data-ttu-id="eaa52-646">Toode 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-646">Product 1</span></span></td>
<td><span data-ttu-id="eaa52-647">80</span><span class="sxs-lookup"><span data-stu-id="eaa52-647">80</span></span></td>
<td><span data-ttu-id="eaa52-648">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="eaa52-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="eaa52-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="eaa52-649">2,507.09</span></span></td>
<td><span data-ttu-id="eaa52-650">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-651">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-651">Prod 2</span></span></td>
<td><span data-ttu-id="eaa52-652">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-652">Product 2</span></span></td>
<td><span data-ttu-id="eaa52-653">15</span><span class="sxs-lookup"><span data-stu-id="eaa52-653">15</span></span></td>
<td><span data-ttu-id="eaa52-654">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="eaa52-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="eaa52-655">470.08</span><span class="sxs-lookup"><span data-stu-id="eaa52-655">470.08</span></span></td>
<td><span data-ttu-id="eaa52-656">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="eaa52-657">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="eaa52-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="eaa52-658">Tööleht</span><span class="sxs-lookup"><span data-stu-id="eaa52-658">Journal</span></span></th>
<th><span data-ttu-id="eaa52-659">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="eaa52-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="eaa52-660">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="eaa52-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="eaa52-661">Versioon</span><span class="sxs-lookup"><span data-stu-id="eaa52-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-662">00004</span><span class="sxs-lookup"><span data-stu-id="eaa52-662">00004</span></span></td>
<td><span data-ttu-id="eaa52-663">Kulueralduse tööleht</span><span class="sxs-lookup"><span data-stu-id="eaa52-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="eaa52-664">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="eaa52-664">Fiscal</span></span></td>
<td><span data-ttu-id="eaa52-665">2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-665">2017</span></span></td>
<td><span data-ttu-id="eaa52-666">Periood 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-666">Period 1</span></span></td>
<td><span data-ttu-id="eaa52-667">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="eaa52-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="eaa52-668">Töölehe read</span><span class="sxs-lookup"><span data-stu-id="eaa52-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="eaa52-669">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="eaa52-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="eaa52-670">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="eaa52-671">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="eaa52-671">Cost element</span></span></th>
<th><span data-ttu-id="eaa52-672">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="eaa52-672">Cost behavior</span></span></th>
<th><span data-ttu-id="eaa52-673">Summa</span><span class="sxs-lookup"><span data-stu-id="eaa52-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-674">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="eaa52-675">CC001</span><span class="sxs-lookup"><span data-stu-id="eaa52-675">CC001</span></span></td>
<td><span data-ttu-id="eaa52-676">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="eaa52-676">HR</span></span></td>
<td><span data-ttu-id="eaa52-677">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-677">10001</span></span></td>
<td><span data-ttu-id="eaa52-678">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-678">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-679">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-679">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-680">500,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-681">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="eaa52-682">CC001</span><span class="sxs-lookup"><span data-stu-id="eaa52-682">CC001</span></span></td>
<td><span data-ttu-id="eaa52-683">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="eaa52-683">HR</span></span></td>
<td><span data-ttu-id="eaa52-684">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-684">10001</span></span></td>
<td><span data-ttu-id="eaa52-685">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-685">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-686">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-686">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="eaa52-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-688">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="eaa52-689">CC002</span><span class="sxs-lookup"><span data-stu-id="eaa52-689">CC002</span></span></td>
<td><span data-ttu-id="eaa52-690">Finantsid</span><span class="sxs-lookup"><span data-stu-id="eaa52-690">Finance</span></span></td>
<td><span data-ttu-id="eaa52-691">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-691">10001</span></span></td>
<td><span data-ttu-id="eaa52-692">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-692">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-693">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-693">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-694">675.00</span><span class="sxs-lookup"><span data-stu-id="eaa52-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-695">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="eaa52-696">CC002</span><span class="sxs-lookup"><span data-stu-id="eaa52-696">CC002</span></span></td>
<td><span data-ttu-id="eaa52-697">Finantsid</span><span class="sxs-lookup"><span data-stu-id="eaa52-697">Finance</span></span></td>
<td><span data-ttu-id="eaa52-698">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-698">10001</span></span></td>
<td><span data-ttu-id="eaa52-699">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-699">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-700">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-700">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="eaa52-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-702">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="eaa52-703">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-703">CC003</span></span></td>
<td><span data-ttu-id="eaa52-704">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-704">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-705">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-705">10001</span></span></td>
<td><span data-ttu-id="eaa52-706">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-706">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-707">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-707">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-708">713.75</span><span class="sxs-lookup"><span data-stu-id="eaa52-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-709">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="eaa52-710">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-710">CC003</span></span></td>
<td><span data-ttu-id="eaa52-711">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-711">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-712">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-712">10001</span></span></td>
<td><span data-ttu-id="eaa52-713">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-713">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-714">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-714">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="eaa52-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-716">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="eaa52-717">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-717">CC003</span></span></td>
<td><span data-ttu-id="eaa52-718">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="eaa52-718">Packaging</span></span></td>
<td><span data-ttu-id="eaa52-719">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-719">10001</span></span></td>
<td><span data-ttu-id="eaa52-720">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-720">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-721">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-721">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-722">286.25</span><span class="sxs-lookup"><span data-stu-id="eaa52-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-723">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="eaa52-724">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-724">CC003</span></span></td>
<td><span data-ttu-id="eaa52-725">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="eaa52-725">Packaging</span></span></td>
<td><span data-ttu-id="eaa52-726">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-726">10001</span></span></td>
<td><span data-ttu-id="eaa52-727">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-727">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-728">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-728">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="eaa52-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-730">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="eaa52-731">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-731">Prod 1</span></span></td>
<td><span data-ttu-id="eaa52-732">Toode 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-732">Product 1</span></span></td>
<td><span data-ttu-id="eaa52-733">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-733">10001</span></span></td>
<td><span data-ttu-id="eaa52-734">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-734">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-735">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-735">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-736">776.36</span><span class="sxs-lookup"><span data-stu-id="eaa52-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-737">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="eaa52-738">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-738">Prod 1</span></span></td>
<td><span data-ttu-id="eaa52-739">Toode 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-739">Product 1</span></span></td>
<td><span data-ttu-id="eaa52-740">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-740">10001</span></span></td>
<td><span data-ttu-id="eaa52-741">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-741">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-742">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-742">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="eaa52-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-744">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="eaa52-745">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-745">Prod 2</span></span></td>
<td><span data-ttu-id="eaa52-746">Toode 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-746">Product 1</span></span></td>
<td><span data-ttu-id="eaa52-747">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-747">10001</span></span></td>
<td><span data-ttu-id="eaa52-748">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-748">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-749">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-749">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-750">223.64</span><span class="sxs-lookup"><span data-stu-id="eaa52-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-751">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="eaa52-752">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-752">Prod 2</span></span></td>
<td><span data-ttu-id="eaa52-753">Toode 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-753">Product 1</span></span></td>
<td><span data-ttu-id="eaa52-754">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-754">10001</span></span></td>
<td><span data-ttu-id="eaa52-755">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-755">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-756">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-756">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="eaa52-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="eaa52-758">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="eaa52-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="eaa52-759">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="eaa52-760">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="eaa52-760">Cost element</span></span></th>
<th><span data-ttu-id="eaa52-761">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="eaa52-761">Cost behavior</span></span></th>
<th><span data-ttu-id="eaa52-762">Summa</span><span class="sxs-lookup"><span data-stu-id="eaa52-762">Amount</span></span></th>
<th><span data-ttu-id="eaa52-763">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="eaa52-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="eaa52-764">CC001</span><span class="sxs-lookup"><span data-stu-id="eaa52-764">CC001</span></span></td>
<td><span data-ttu-id="eaa52-765">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="eaa52-765">HR</span></span></td>
<td><span data-ttu-id="eaa52-766">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-766">10001</span></span></td>
<td><span data-ttu-id="eaa52-767">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-767">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-768">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-768">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-769">‑500,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-769">-500.00</span></span></td>
<td><span data-ttu-id="eaa52-770">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-771">CC002</span><span class="sxs-lookup"><span data-stu-id="eaa52-771">CC002</span></span></td>
<td><span data-ttu-id="eaa52-772">Finantsid</span><span class="sxs-lookup"><span data-stu-id="eaa52-772">Finance</span></span></td>
<td><span data-ttu-id="eaa52-773">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-773">10001</span></span></td>
<td><span data-ttu-id="eaa52-774">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-774">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-775">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-775">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-776">175.00</span><span class="sxs-lookup"><span data-stu-id="eaa52-776">175.00</span></span></td>
<td><span data-ttu-id="eaa52-777">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-778">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-778">CC003</span></span></td>
<td><span data-ttu-id="eaa52-779">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-779">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-780">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-780">10001</span></span></td>
<td><span data-ttu-id="eaa52-781">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-781">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-782">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-782">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-783">275.00</span><span class="sxs-lookup"><span data-stu-id="eaa52-783">275.00</span></span></td>
<td><span data-ttu-id="eaa52-784">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-785">CC004</span><span class="sxs-lookup"><span data-stu-id="eaa52-785">CC004</span></span></td>
<td><span data-ttu-id="eaa52-786">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="eaa52-786">Packaging</span></span></td>
<td><span data-ttu-id="eaa52-787">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-787">10001</span></span></td>
<td><span data-ttu-id="eaa52-788">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-788">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-789">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-789">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-790">50,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-790">50,00</span></span></td>
<td><span data-ttu-id="eaa52-791">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-792">CC001</span><span class="sxs-lookup"><span data-stu-id="eaa52-792">CC001</span></span></td>
<td><span data-ttu-id="eaa52-793">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="eaa52-793">HR</span></span></td>
<td><span data-ttu-id="eaa52-794">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-794">10001</span></span></td>
<td><span data-ttu-id="eaa52-795">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-795">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-796">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-796">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-797">–1245,71</span><span class="sxs-lookup"><span data-stu-id="eaa52-797">-1,245.71</span></span></td>
<td><span data-ttu-id="eaa52-798">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-799">CC002</span><span class="sxs-lookup"><span data-stu-id="eaa52-799">CC002</span></span></td>
<td><span data-ttu-id="eaa52-800">Finantsid</span><span class="sxs-lookup"><span data-stu-id="eaa52-800">Finance</span></span></td>
<td><span data-ttu-id="eaa52-801">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-801">10001</span></span></td>
<td><span data-ttu-id="eaa52-802">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-802">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-803">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-803">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-804">436.00</span><span class="sxs-lookup"><span data-stu-id="eaa52-804">436.00</span></span></td>
<td><span data-ttu-id="eaa52-805">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-806">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-806">CC003</span></span></td>
<td><span data-ttu-id="eaa52-807">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-807">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-808">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-808">10001</span></span></td>
<td><span data-ttu-id="eaa52-809">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-809">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-810">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-810">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-811">685.14</span><span class="sxs-lookup"><span data-stu-id="eaa52-811">685.14</span></span></td>
<td><span data-ttu-id="eaa52-812">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-813">CC004</span><span class="sxs-lookup"><span data-stu-id="eaa52-813">CC004</span></span></td>
<td><span data-ttu-id="eaa52-814">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="eaa52-814">Packaging</span></span></td>
<td><span data-ttu-id="eaa52-815">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-815">10001</span></span></td>
<td><span data-ttu-id="eaa52-816">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-816">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-817">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-817">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-818">124.57</span><span class="sxs-lookup"><span data-stu-id="eaa52-818">124.57</span></span></td>
<td><span data-ttu-id="eaa52-819">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-820">CC002</span><span class="sxs-lookup"><span data-stu-id="eaa52-820">CC002</span></span></td>
<td><span data-ttu-id="eaa52-821">Finantsid</span><span class="sxs-lookup"><span data-stu-id="eaa52-821">Finance</span></span></td>
<td><span data-ttu-id="eaa52-822">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-822">10001</span></span></td>
<td><span data-ttu-id="eaa52-823">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-823">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-824">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-824">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-825">–675,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-825">-675.00</span></span></td>
<td><span data-ttu-id="eaa52-826">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-827">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-827">CC003</span></span></td>
<td><span data-ttu-id="eaa52-828">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-828">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-829">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-829">10001</span></span></td>
<td><span data-ttu-id="eaa52-830">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-830">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-831">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-831">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-832">438.75</span><span class="sxs-lookup"><span data-stu-id="eaa52-832">438.75</span></span></td>
<td><span data-ttu-id="eaa52-833">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-834">CC004</span><span class="sxs-lookup"><span data-stu-id="eaa52-834">CC004</span></span></td>
<td><span data-ttu-id="eaa52-835">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="eaa52-835">Packaging</span></span></td>
<td><span data-ttu-id="eaa52-836">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-836">10001</span></span></td>
<td><span data-ttu-id="eaa52-837">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-837">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-838">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-838">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-839">236.25</span><span class="sxs-lookup"><span data-stu-id="eaa52-839">236.25</span></span></td>
<td><span data-ttu-id="eaa52-840">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-841">CC002</span><span class="sxs-lookup"><span data-stu-id="eaa52-841">CC002</span></span></td>
<td><span data-ttu-id="eaa52-842">Finantsid</span><span class="sxs-lookup"><span data-stu-id="eaa52-842">Finance</span></span></td>
<td><span data-ttu-id="eaa52-843">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-843">10001</span></span></td>
<td><span data-ttu-id="eaa52-844">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-844">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-845">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-845">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-846">–8150,29</span><span class="sxs-lookup"><span data-stu-id="eaa52-846">-8,150.29</span></span></td>
<td><span data-ttu-id="eaa52-847">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-848">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-848">CC003</span></span></td>
<td><span data-ttu-id="eaa52-849">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-849">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-850">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-850">10001</span></span></td>
<td><span data-ttu-id="eaa52-851">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-851">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-852">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-852">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="eaa52-853">5,297.69</span></span></td>
<td><span data-ttu-id="eaa52-854">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-855">CC004</span><span class="sxs-lookup"><span data-stu-id="eaa52-855">CC004</span></span></td>
<td><span data-ttu-id="eaa52-856">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="eaa52-856">Packaging</span></span></td>
<td><span data-ttu-id="eaa52-857">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-857">10001</span></span></td>
<td><span data-ttu-id="eaa52-858">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-858">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-859">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-859">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="eaa52-860">2,852.60</span></span></td>
<td><span data-ttu-id="eaa52-861">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-862">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-862">CC003</span></span></td>
<td><span data-ttu-id="eaa52-863">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-863">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-864">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-864">10001</span></span></td>
<td><span data-ttu-id="eaa52-865">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-865">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-866">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-866">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-867">–713,75</span><span class="sxs-lookup"><span data-stu-id="eaa52-867">-713.75</span></span></td>
<td><span data-ttu-id="eaa52-868">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-869">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-869">Prod 1</span></span></td>
<td><span data-ttu-id="eaa52-870">Toode 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-870">Product 1</span></span></td>
<td><span data-ttu-id="eaa52-871">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-871">10001</span></span></td>
<td><span data-ttu-id="eaa52-872">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-872">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-873">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-873">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-874">535.31</span><span class="sxs-lookup"><span data-stu-id="eaa52-874">535.31</span></span></td>
<td><span data-ttu-id="eaa52-875">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-876">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-876">Prod 2</span></span></td>
<td><span data-ttu-id="eaa52-877">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-877">Product 2</span></span></td>
<td><span data-ttu-id="eaa52-878">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-878">10001</span></span></td>
<td><span data-ttu-id="eaa52-879">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-879">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-880">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-880">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-881">178.44</span><span class="sxs-lookup"><span data-stu-id="eaa52-881">178.44</span></span></td>
<td><span data-ttu-id="eaa52-882">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-883">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-883">CC003</span></span></td>
<td><span data-ttu-id="eaa52-884">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-884">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-885">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-885">10001</span></span></td>
<td><span data-ttu-id="eaa52-886">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-886">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-887">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-887">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-888">–5982,83</span><span class="sxs-lookup"><span data-stu-id="eaa52-888">-5,982.83</span></span></td>
<td><span data-ttu-id="eaa52-889">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-890">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-890">Prod 1</span></span></td>
<td><span data-ttu-id="eaa52-891">Toode 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-891">Product 1</span></span></td>
<td><span data-ttu-id="eaa52-892">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-892">10001</span></span></td>
<td><span data-ttu-id="eaa52-893">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-893">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-894">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-894">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="eaa52-895">4,487.12</span></span></td>
<td><span data-ttu-id="eaa52-896">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-897">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-897">Prod 2</span></span></td>
<td><span data-ttu-id="eaa52-898">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-898">Product 2</span></span></td>
<td><span data-ttu-id="eaa52-899">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-899">10001</span></span></td>
<td><span data-ttu-id="eaa52-900">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-900">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-901">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-901">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="eaa52-902">1,495.71</span></span></td>
<td><span data-ttu-id="eaa52-903">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-904">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-904">CC003</span></span></td>
<td><span data-ttu-id="eaa52-905">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-905">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-906">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-906">10001</span></span></td>
<td><span data-ttu-id="eaa52-907">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-907">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-908">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-908">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-909">–286,25</span><span class="sxs-lookup"><span data-stu-id="eaa52-909">-286.25</span></span></td>
<td><span data-ttu-id="eaa52-910">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-911">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-911">Prod 1</span></span></td>
<td><span data-ttu-id="eaa52-912">Toode 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-912">Product 1</span></span></td>
<td><span data-ttu-id="eaa52-913">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-913">10001</span></span></td>
<td><span data-ttu-id="eaa52-914">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-914">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-915">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-915">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-916">241.05</span><span class="sxs-lookup"><span data-stu-id="eaa52-916">241.05</span></span></td>
<td><span data-ttu-id="eaa52-917">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-918">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-918">Prod 2</span></span></td>
<td><span data-ttu-id="eaa52-919">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-919">Product 2</span></span></td>
<td><span data-ttu-id="eaa52-920">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-920">10001</span></span></td>
<td><span data-ttu-id="eaa52-921">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-921">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-922">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-922">Fixed cost</span></span></td>
<td><span data-ttu-id="eaa52-923">45.20</span><span class="sxs-lookup"><span data-stu-id="eaa52-923">45.20</span></span></td>
<td><span data-ttu-id="eaa52-924">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-925">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-925">CC003</span></span></td>
<td><span data-ttu-id="eaa52-926">Assembler</span><span class="sxs-lookup"><span data-stu-id="eaa52-926">Assembly</span></span></td>
<td><span data-ttu-id="eaa52-927">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-927">10001</span></span></td>
<td><span data-ttu-id="eaa52-928">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-928">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-929">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-929">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-930">–2977,17</span><span class="sxs-lookup"><span data-stu-id="eaa52-930">-2,977.17</span></span></td>
<td><span data-ttu-id="eaa52-931">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-932">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-932">Prod 1</span></span></td>
<td><span data-ttu-id="eaa52-933">Toode 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-933">Product 1</span></span></td>
<td><span data-ttu-id="eaa52-934">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-934">10001</span></span></td>
<td><span data-ttu-id="eaa52-935">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-935">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-936">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-936">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="eaa52-937">2,507.09</span></span></td>
<td><span data-ttu-id="eaa52-938">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="eaa52-939">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-939">Prod 2</span></span></td>
<td><span data-ttu-id="eaa52-940">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-940">Product 2</span></span></td>
<td><span data-ttu-id="eaa52-941">10001</span><span class="sxs-lookup"><span data-stu-id="eaa52-941">10001</span></span></td>
<td><span data-ttu-id="eaa52-942">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="eaa52-942">Electricity</span></span></td>
<td><span data-ttu-id="eaa52-943">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-943">Variable cost</span></span></td>
<td><span data-ttu-id="eaa52-944">470.08</span><span class="sxs-lookup"><span data-stu-id="eaa52-944">470.08</span></span></td>
<td><span data-ttu-id="eaa52-945">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="eaa52-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="eaa52-946">Lõppsõna</span><span class="sxs-lookup"><span data-stu-id="eaa52-946">Conclusion</span></span>
<span data-ttu-id="eaa52-947">Finantsaruandluses sisestatakse elektrikulu 10 000,00 fiktiivse kulukeskuse ID-le.</span><span class="sxs-lookup"><span data-stu-id="eaa52-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="eaa52-948">Nii teavad kuluarvestajad, et see kulu tuleb eraldada.</span><span class="sxs-lookup"><span data-stu-id="eaa52-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="eaa52-949">Kuluarvestuses liigub kulu rakendatud poliitikate ja reeglite põhjal läbi organisatsiooniüksuste ja -tasemete.</span><span class="sxs-lookup"><span data-stu-id="eaa52-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="eaa52-950">Iga kulu on seostatud eraldamisalusega, mis pakub kulude eraldamiseks parimat hinnangut.</span><span class="sxs-lookup"><span data-stu-id="eaa52-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="eaa52-951">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="eaa52-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="eaa52-952">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="eaa52-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="eaa52-953">Kokku</span><span class="sxs-lookup"><span data-stu-id="eaa52-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="eaa52-954">CC099</span><span class="sxs-lookup"><span data-stu-id="eaa52-954">CC099</span></span></th>
<th><span data-ttu-id="eaa52-955">CC001</span><span class="sxs-lookup"><span data-stu-id="eaa52-955">CC001</span></span></th>
<th><span data-ttu-id="eaa52-956">CC002</span><span class="sxs-lookup"><span data-stu-id="eaa52-956">CC002</span></span></th>
<th><span data-ttu-id="eaa52-957">CC003</span><span class="sxs-lookup"><span data-stu-id="eaa52-957">CC003</span></span></th>
<th><span data-ttu-id="eaa52-958">CC004</span><span class="sxs-lookup"><span data-stu-id="eaa52-958">CC004</span></span></th>
<th><span data-ttu-id="eaa52-959">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-959">Proj 1</span></span></th>
<th><span data-ttu-id="eaa52-960">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-960">Proj 2</span></span></th>
<th><span data-ttu-id="eaa52-961">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="eaa52-961">Prod 1</span></span></th>
<th><span data-ttu-id="eaa52-962">Toode 2</span><span class="sxs-lookup"><span data-stu-id="eaa52-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="eaa52-963">10001 Elekter</span><span class="sxs-lookup"><span data-stu-id="eaa52-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="eaa52-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-965"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="eaa52-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-966"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="eaa52-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-967"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="eaa52-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-968"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="eaa52-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-969"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="eaa52-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-970"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="eaa52-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-971"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="eaa52-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-972"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="eaa52-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="eaa52-973">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="eaa52-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-974">0,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-974">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="eaa52-975">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-976">0,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-977">0,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-978">0,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-979">0,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-980">0,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-981">776.36</span><span class="sxs-lookup"><span data-stu-id="eaa52-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-982">223.64</span><span class="sxs-lookup"><span data-stu-id="eaa52-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-983"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="eaa52-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="eaa52-984">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="eaa52-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-985">000</span><span class="sxs-lookup"><span data-stu-id="eaa52-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-986">0,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-987">0,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-988">0,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-989">0,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-990">30,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-991">10,00</span><span class="sxs-lookup"><span data-stu-id="eaa52-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="eaa52-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="eaa52-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="eaa52-994"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="eaa52-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="eaa52-995">Selles teemas selgitatakse, kuidas esmane kuluelement, 10001 Eleter, liigub läbi kuluobjektide.</span><span class="sxs-lookup"><span data-stu-id="eaa52-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="eaa52-996">Seega eraldatakse see üldkulu organisatsiooni madalaimale tasemele.</span><span class="sxs-lookup"><span data-stu-id="eaa52-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="eaa52-997">Teisisõnu kannavad kulu madalaimal tasemel olevad kuluobjektid.</span><span class="sxs-lookup"><span data-stu-id="eaa52-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="eaa52-998">Kui soovite saada kuluobjektide vahelisest kuluvoost visuaalset ülevaadet, saate kuluvoo visualiseerimiseks kasutada kulude kokkuvõtte poliitika reegleid.</span><span class="sxs-lookup"><span data-stu-id="eaa52-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="eaa52-999">Täpsemat teavet vaadake jaotisest Kulude kokkuvõtte poliitika.</span><span class="sxs-lookup"><span data-stu-id="eaa52-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="eaa52-1000">(Pange tähele, et see teema pole veel valmis, kuid see tuleb peagi.)</span><span class="sxs-lookup"><span data-stu-id="eaa52-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




