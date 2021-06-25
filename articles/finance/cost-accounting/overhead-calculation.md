---
title: Üldkulude arvutus
description: Selles teemas kirjeldatakse tüüpilisi üldkulude arvutamise ja eraldamise protsesse.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 8dc312e66dc666ac6c23bac6b705ffc7893fd06b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187993"
---
# <a name="overhead-calculation"></a><span data-ttu-id="e4b21-103">Üldkulude arvutus</span><span class="sxs-lookup"><span data-stu-id="e4b21-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4b21-104">Selles teemas kirjeldatakse tüüpilisi üldkulude arvutamise ja eraldamise protsesse.</span><span class="sxs-lookup"><span data-stu-id="e4b21-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

## <a name="term-definition"></a><span data-ttu-id="e4b21-105">Mõiste määratlus</span><span class="sxs-lookup"><span data-stu-id="e4b21-105">Term definition</span></span>

<span data-ttu-id="e4b21-106">Üldkulud on kulud, mis kaasnevad ettevõtte käitamisega, kuid mida ei saa seostada otseselt ühegi kindla äritegevuse, toote ega teenusega.</span><span class="sxs-lookup"><span data-stu-id="e4b21-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="e4b21-107">Üldkulud pakuvad kriitilist tuge kasumit andavate tegevuste loomisele.</span><span class="sxs-lookup"><span data-stu-id="e4b21-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="e4b21-108">Siin on mõned näited üldkuludest.</span><span class="sxs-lookup"><span data-stu-id="e4b21-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="e4b21-109">Üür</span><span class="sxs-lookup"><span data-stu-id="e4b21-109">Rent</span></span>
-   <span data-ttu-id="e4b21-110">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-110">Electricity</span></span>
-   <span data-ttu-id="e4b21-111">Haldustasud</span><span class="sxs-lookup"><span data-stu-id="e4b21-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="e4b21-112">Üldkulude arvutuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="e4b21-112">Overhead calculation overview</span></span>
<span data-ttu-id="e4b21-113">Üldkulude arvutus käitab kuluarvutuse poliitikaid õiges järjekorras.</span><span class="sxs-lookup"><span data-stu-id="e4b21-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="e4b21-114">Saate käivitada üldkulude arvutuse sama rahandusperioodi kohta mitu korda, kui kuluarvestuse poliitikaid on muudetud või tuvastatud teatud tõrked.</span><span class="sxs-lookup"><span data-stu-id="e4b21-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="e4b21-115">Iga üldkulude arvutamise käitamine talletatakse ja see saab kordumatu versiooni-ID, mis võimaldab teil arvutuste erinevaid versioone võrrelda.</span><span class="sxs-lookup"><span data-stu-id="e4b21-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="e4b21-116">Ülekulude arvutusega loodud kulukirjed saavad aruandluskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="e4b21-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="e4b21-117">See aruandluskuupäev vastab arvutuses kasutatud rahandusperioodi lõppkuupäevale.</span><span class="sxs-lookup"><span data-stu-id="e4b21-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="e4b21-118">Kordumatu versiooni-ID koosneb järgmistest elementidest.</span><span class="sxs-lookup"><span data-stu-id="e4b21-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="e4b21-119">Versiooni tüüp</span><span class="sxs-lookup"><span data-stu-id="e4b21-119">Version type</span></span>
-   <span data-ttu-id="e4b21-120">Kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="e4b21-120">Date and time</span></span>
-   <span data-ttu-id="e4b21-121">Kuluarvestuse pearaamat</span><span class="sxs-lookup"><span data-stu-id="e4b21-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="e4b21-122">Finantsaasta</span><span class="sxs-lookup"><span data-stu-id="e4b21-122">Fiscal year</span></span>
-   <span data-ttu-id="e4b21-123">Rahandusperiood</span><span class="sxs-lookup"><span data-stu-id="e4b21-123">Fiscal period</span></span>

<span data-ttu-id="e4b21-124">Üldkulude arvutus käivitatakse versioonist sõltumatult.</span><span class="sxs-lookup"><span data-stu-id="e4b21-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="e4b21-125">Seetõttu saate arvutada eelarveversiooni enne tegelikku versiooni.</span><span class="sxs-lookup"><span data-stu-id="e4b21-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="e4b21-126">Üldkulude arvutus koosneb neljast etapist, nagu näha alltoodud joonisel.</span><span class="sxs-lookup"><span data-stu-id="e4b21-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="e4b21-127">Igas etapis luuakse töölehe päis, millel on töölehe kanded.</span><span class="sxs-lookup"><span data-stu-id="e4b21-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="e4b21-128">See töölehe päis säiiltab sisendandmeid iga arvutusetapi kohta.</span><span class="sxs-lookup"><span data-stu-id="e4b21-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="e4b21-129">Igale töölehe reale rakendatakse poliitikad ja reeglid ning väljundina luuakse kulukirjed.</span><span class="sxs-lookup"><span data-stu-id="e4b21-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="e4b21-130">Seega on teil alati olemas põhjalik ülevaade.</span><span class="sxs-lookup"><span data-stu-id="e4b21-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="e4b21-131">[![Üldkulude arvutus](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="e4b21-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="e4b21-132">Elektri üldkulude arvutamine ja eraldamine</span><span class="sxs-lookup"><span data-stu-id="e4b21-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="e4b21-133">Finantsaruandluses on mõned kulud, näiteks elekter, registreeritud põhisummana.</span><span class="sxs-lookup"><span data-stu-id="e4b21-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="e4b21-134">Seetõttu ei pakuta kuluarvestuseks üksikasjalikku juhtimisülevaadet.</span><span class="sxs-lookup"><span data-stu-id="e4b21-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="e4b21-135">Kuluarvestuses peavad kulud liikuma läbi organisatsiooniüksuste, et pakkuda korrektset juhtimisülevaadet kõigi organisatsiooniüksuste ja -tasemete kohta.</span><span class="sxs-lookup"><span data-stu-id="e4b21-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="e4b21-136">See voog peab põhinema tarbimise või õiglase hindamise täpsel kirjendamisel.</span><span class="sxs-lookup"><span data-stu-id="e4b21-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="e4b21-137">Pearaamatus, saab elektrikulu sisestada nii, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="e4b21-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4b21-138">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="e4b21-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e4b21-139">Kulukeskus</span><span class="sxs-lookup"><span data-stu-id="e4b21-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="e4b21-140">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="e4b21-140">Main account</span></span></th>
<th><span data-ttu-id="e4b21-141">Summa arvestusvaluutas</span><span class="sxs-lookup"><span data-stu-id="e4b21-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-142">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="e4b21-143">CC099</span><span class="sxs-lookup"><span data-stu-id="e4b21-143">CC099</span></span></td>
<td><span data-ttu-id="e4b21-144">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="e4b21-144">Default cost center</span></span></td>
<td><span data-ttu-id="e4b21-145">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-145">10001</span></span></td>
<td><span data-ttu-id="e4b21-146">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-146">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="e4b21-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="e4b21-148">1. etapp: kulukäitumise arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="e4b21-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="e4b21-149">Vaikimisi saavad lähteandmetest imporditud kulukirjed kuluarvestuses kulukäitumise klassifikatsiooniks **Klassifitseerimata**.</span><span class="sxs-lookup"><span data-stu-id="e4b21-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="e4b21-150">Kulukäitumise poliitikareegleid rakendades saate kulukirjed ümber klassifitseerida kui **Fikseeritud kulu** või **Muutuvkulu**.</span><span class="sxs-lookup"><span data-stu-id="e4b21-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="e4b21-151">Kulukäitumise reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="e4b21-151">Define the cost behavior rule</span></span>

<span data-ttu-id="e4b21-152">Mõnikord on osa kulust fikseeritud tasu ja järelejäänud kulu põhineb tarbimisel.</span><span class="sxs-lookup"><span data-stu-id="e4b21-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="e4b21-153">Elektriarved vastavad sageli sellele määratlusele.</span><span class="sxs-lookup"><span data-stu-id="e4b21-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="e4b21-154">Pärast kindla fikseeritud tasu maksmist maksate tarbimise eest kilovatt-tunni (Kwh) kohta.</span><span class="sxs-lookup"><span data-stu-id="e4b21-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="e4b21-155">Näiteks kui fikseeritud kulu tasu on 1000,00 eurot, määratletakse kulukäitumise reegel järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e4b21-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="e4b21-156">Fikseeritud summa: 1000,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="e4b21-157">0 &lt;= 1000,00 = fikseeritud</span><span class="sxs-lookup"><span data-stu-id="e4b21-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="e4b21-158">1000,01 &lt; N = muutuja</span><span class="sxs-lookup"><span data-stu-id="e4b21-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="e4b21-159">Tööleht</span><span class="sxs-lookup"><span data-stu-id="e4b21-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4b21-160">Tööleht</span><span class="sxs-lookup"><span data-stu-id="e4b21-160">Journal</span></span></th>
<th><span data-ttu-id="e4b21-161">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="e4b21-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e4b21-162">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="e4b21-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e4b21-163">Versioon</span><span class="sxs-lookup"><span data-stu-id="e4b21-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-164">00001</span><span class="sxs-lookup"><span data-stu-id="e4b21-164">00001</span></span></td>
<td><span data-ttu-id="e4b21-165">Kulukäitumise arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="e4b21-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="e4b21-166">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="e4b21-166">Fiscal</span></span></td>
<td><span data-ttu-id="e4b21-167">2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-167">2017</span></span></td>
<td><span data-ttu-id="e4b21-168">Periood 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-168">Period 1</span></span></td>
<td><span data-ttu-id="e4b21-169">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="e4b21-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e4b21-170">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="e4b21-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4b21-171">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="e4b21-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e4b21-172">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e4b21-173">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="e4b21-173">Cost element</span></span></th>
<th><span data-ttu-id="e4b21-174">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="e4b21-174">Cost behavior</span></span></th>
<th><span data-ttu-id="e4b21-175">Summa</span><span class="sxs-lookup"><span data-stu-id="e4b21-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-176">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="e4b21-177">CC099</span><span class="sxs-lookup"><span data-stu-id="e4b21-177">CC099</span></span></td>
<td><span data-ttu-id="e4b21-178">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="e4b21-178">Default cost center</span></span></td>
<td><span data-ttu-id="e4b21-179">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-179">10001</span></span></td>
<td><span data-ttu-id="e4b21-180">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-180">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-181">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="e4b21-181">Unclassified</span></span></td>
<td><span data-ttu-id="e4b21-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="e4b21-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e4b21-183">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="e4b21-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-184">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e4b21-185">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="e4b21-185">Cost element</span></span></th>
<th><span data-ttu-id="e4b21-186">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="e4b21-186">Cost behavior</span></span></th>
<th><span data-ttu-id="e4b21-187">Summa</span><span class="sxs-lookup"><span data-stu-id="e4b21-187">Amount</span></span></th>
<th><span data-ttu-id="e4b21-188">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="e4b21-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-189">CC099</span><span class="sxs-lookup"><span data-stu-id="e4b21-189">CC099</span></span></td>
<td><span data-ttu-id="e4b21-190">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="e4b21-190">Default cost center</span></span></td>
<td><span data-ttu-id="e4b21-191">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-191">10001</span></span></td>
<td><span data-ttu-id="e4b21-192">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-192">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-193">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="e4b21-193">Unclassified</span></span></td>
<td><span data-ttu-id="e4b21-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="e4b21-194">10,000.00</span></span></td>
<td><span data-ttu-id="e4b21-195">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-196">CC099</span><span class="sxs-lookup"><span data-stu-id="e4b21-196">CC099</span></span></td>
<td><span data-ttu-id="e4b21-197">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="e4b21-197">Default cost center</span></span></td>
<td><span data-ttu-id="e4b21-198">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-198">10001</span></span></td>
<td><span data-ttu-id="e4b21-199">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-199">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-200">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="e4b21-200">Unclassified</span></span></td>
<td><span data-ttu-id="e4b21-201">–10 000,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-201">-10,000.00</span></span></td>
<td><span data-ttu-id="e4b21-202">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-203">CC099</span><span class="sxs-lookup"><span data-stu-id="e4b21-203">CC099</span></span></td>
<td><span data-ttu-id="e4b21-204">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="e4b21-204">Default cost center</span></span></td>
<td><span data-ttu-id="e4b21-205">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-205">10001</span></span></td>
<td><span data-ttu-id="e4b21-206">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-206">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-207">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-207">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-208">1,000.00</span></span></td>
<td><span data-ttu-id="e4b21-209">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-210">CC099</span><span class="sxs-lookup"><span data-stu-id="e4b21-210">CC099</span></span></td>
<td><span data-ttu-id="e4b21-211">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="e4b21-211">Default cost center</span></span></td>
<td><span data-ttu-id="e4b21-212">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-212">10001</span></span></td>
<td><span data-ttu-id="e4b21-213">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-213">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-214">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-214">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="e4b21-215">9,000.00</span></span></td>
<td><span data-ttu-id="e4b21-216">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4b21-217">Lisateavet vt teemast [Kulukäitumise poliitika loomine ja määramine kulujuhtimisüksusele (tegevuse juhis)](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="e4b21-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="e4b21-218">2. etapp: kulujaotuse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="e4b21-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="e4b21-219">Kulujaotust kasutatakse kulu ümberjaotamiseks ühelt kuluobjektilt ühele või mitmele teisele kuluobjektile, rakendades asjakohast eraldusalust.</span><span class="sxs-lookup"><span data-stu-id="e4b21-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="e4b21-220">Kulujaotus ja kulueraldus erinevad selle poolest, et kulujaotus toimub alati algse kulu esmase kuluelemendi tasemel.</span><span class="sxs-lookup"><span data-stu-id="e4b21-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="e4b21-221">Kulujaotuse reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="e4b21-221">Define the cost distribution rule</span></span>

<span data-ttu-id="e4b21-222">Finantsaruandluses registreeritakse elektrikulud sageli põhisummana.</span><span class="sxs-lookup"><span data-stu-id="e4b21-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="e4b21-223">Kuluarvestuseses ei ole see lähenemine piisavalt üksikasjalik.</span><span class="sxs-lookup"><span data-stu-id="e4b21-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="e4b21-224">Muutuvkulu tuleb jaotada üksikutele kuluobjektidele õigluse alusel.</span><span class="sxs-lookup"><span data-stu-id="e4b21-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="e4b21-225">Kõige loogilisem eraldamisalus on elektritarbimine (kWh).</span><span class="sxs-lookup"><span data-stu-id="e4b21-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="e4b21-226">Luuakse statistilise dimensiooni liige nimega Elekter ja elektritarbimine on kirjendatakse.</span><span class="sxs-lookup"><span data-stu-id="e4b21-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="e4b21-227">Vaikimisi muutuvad kõik statistilise dimensiooni liikmed eraldamisalusena kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="e4b21-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-228">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-228">Cost object</span></span></th>
<th><span data-ttu-id="e4b21-229">kWh</span><span class="sxs-lookup"><span data-stu-id="e4b21-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-230">CC001</span><span class="sxs-lookup"><span data-stu-id="e4b21-230">CC001</span></span></td>
<td><span data-ttu-id="e4b21-231">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="e4b21-231">HR</span></span></td>
<td><span data-ttu-id="e4b21-232">1000</span><span class="sxs-lookup"><span data-stu-id="e4b21-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-233">CC002</span><span class="sxs-lookup"><span data-stu-id="e4b21-233">CC002</span></span></td>
<td><span data-ttu-id="e4b21-234">Finantsid</span><span class="sxs-lookup"><span data-stu-id="e4b21-234">Finance</span></span></td>
<td><span data-ttu-id="e4b21-235">6,000</span><span class="sxs-lookup"><span data-stu-id="e4b21-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-236">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-236">CC003</span></span></td>
<td><span data-ttu-id="e4b21-237">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-237">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-238">0</span><span class="sxs-lookup"><span data-stu-id="e4b21-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4b21-239">Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="e4b21-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-240">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-240">Cost object</span></span></th>
<th><span data-ttu-id="e4b21-241">Väärtus</span><span class="sxs-lookup"><span data-stu-id="e4b21-241">Magnitude</span></span></th>
<th><span data-ttu-id="e4b21-242">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="e4b21-242">Allocation factor</span></span></th>
<th><span data-ttu-id="e4b21-243">Summa</span><span class="sxs-lookup"><span data-stu-id="e4b21-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-244">CC001</span><span class="sxs-lookup"><span data-stu-id="e4b21-244">CC001</span></span></td>
<td><span data-ttu-id="e4b21-245">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="e4b21-245">HR</span></span></td>
<td><span data-ttu-id="e4b21-246">1000</span><span class="sxs-lookup"><span data-stu-id="e4b21-246">1,000</span></span></td>
<td><span data-ttu-id="e4b21-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e4b21-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="e4b21-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-249">CC002</span><span class="sxs-lookup"><span data-stu-id="e4b21-249">CC002</span></span></td>
<td><span data-ttu-id="e4b21-250">Finantsid</span><span class="sxs-lookup"><span data-stu-id="e4b21-250">Finance</span></span></td>
<td><span data-ttu-id="e4b21-251">6,000</span><span class="sxs-lookup"><span data-stu-id="e4b21-251">6,000</span></span></td>
<td><span data-ttu-id="e4b21-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e4b21-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="e4b21-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-254">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-254">CC003</span></span></td>
<td><span data-ttu-id="e4b21-255">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-255">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-256">0</span><span class="sxs-lookup"><span data-stu-id="e4b21-256">0</span></span></td>
<td><span data-ttu-id="e4b21-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="e4b21-258">0,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4b21-259">Fikseeritud kulu tuleb jaotada ühtlaselt üksikutele kuluobjektidele, mis on tarbinud elektrit.</span><span class="sxs-lookup"><span data-stu-id="e4b21-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="e4b21-260">Selle tulemuse saate, kasutades valemi eraldamisaluses statistilise dimensiooni liiget Elekter: (Elekter &gt; 0,00). Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="e4b21-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-261">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-261">Cost object</span></span></th>
<th><span data-ttu-id="e4b21-262">Valem</span><span class="sxs-lookup"><span data-stu-id="e4b21-262">Formula</span></span></th>
<th><span data-ttu-id="e4b21-263">Väärtus</span><span class="sxs-lookup"><span data-stu-id="e4b21-263">Magnitude</span></span></th>
<th><span data-ttu-id="e4b21-264">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="e4b21-264">Allocation factor</span></span></th>
<th><span data-ttu-id="e4b21-265">Summa</span><span class="sxs-lookup"><span data-stu-id="e4b21-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-266">CC001</span><span class="sxs-lookup"><span data-stu-id="e4b21-266">CC001</span></span></td>
<td><span data-ttu-id="e4b21-267">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="e4b21-267">HR</span></span></td>
<td><span data-ttu-id="e4b21-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e4b21-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e4b21-269">1</span><span class="sxs-lookup"><span data-stu-id="e4b21-269">1</span></span></td>
<td><span data-ttu-id="e4b21-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e4b21-271">500,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-272">CC002</span><span class="sxs-lookup"><span data-stu-id="e4b21-272">CC002</span></span></td>
<td><span data-ttu-id="e4b21-273">Finantsid</span><span class="sxs-lookup"><span data-stu-id="e4b21-273">Finance</span></span></td>
<td><span data-ttu-id="e4b21-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e4b21-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e4b21-275">1</span><span class="sxs-lookup"><span data-stu-id="e4b21-275">1</span></span></td>
<td><span data-ttu-id="e4b21-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e4b21-277">500,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-278">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-278">CC003</span></span></td>
<td><span data-ttu-id="e4b21-279">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-279">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="e4b21-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="e4b21-281">0</span><span class="sxs-lookup"><span data-stu-id="e4b21-281">0</span></span></td>
<td><span data-ttu-id="e4b21-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="e4b21-283">0,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="e4b21-284">Tööleht</span><span class="sxs-lookup"><span data-stu-id="e4b21-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4b21-285">Tööleht</span><span class="sxs-lookup"><span data-stu-id="e4b21-285">Journal</span></span></th>
<th><span data-ttu-id="e4b21-286">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="e4b21-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e4b21-287">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="e4b21-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e4b21-288">Versioon</span><span class="sxs-lookup"><span data-stu-id="e4b21-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-289">00002</span><span class="sxs-lookup"><span data-stu-id="e4b21-289">00002</span></span></td>
<td><span data-ttu-id="e4b21-290">Kulujaotuse arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="e4b21-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="e4b21-291">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="e4b21-291">Fiscal</span></span></td>
<td><span data-ttu-id="e4b21-292">2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-292">2017</span></span></td>
<td><span data-ttu-id="e4b21-293">Periood 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-293">Period 1</span></span></td>
<td><span data-ttu-id="e4b21-294">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="e4b21-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e4b21-295">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="e4b21-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4b21-296">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="e4b21-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e4b21-297">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e4b21-298">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="e4b21-298">Cost element</span></span></th>
<th><span data-ttu-id="e4b21-299">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="e4b21-299">Cost behavior</span></span></th>
<th><span data-ttu-id="e4b21-300">Summa</span><span class="sxs-lookup"><span data-stu-id="e4b21-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-301">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4b21-302">CC099</span><span class="sxs-lookup"><span data-stu-id="e4b21-302">CC099</span></span></td>
<td><span data-ttu-id="e4b21-303">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="e4b21-303">Default cost center</span></span></td>
<td><span data-ttu-id="e4b21-304">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-304">10001</span></span></td>
<td><span data-ttu-id="e4b21-305">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-305">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-306">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-306">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-308">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4b21-309">CC099</span><span class="sxs-lookup"><span data-stu-id="e4b21-309">CC099</span></span></td>
<td><span data-ttu-id="e4b21-310">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="e4b21-310">Default cost center</span></span></td>
<td><span data-ttu-id="e4b21-311">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-311">10001</span></span></td>
<td><span data-ttu-id="e4b21-312">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-312">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-313">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-313">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="e4b21-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e4b21-315">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="e4b21-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-316">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e4b21-317">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="e4b21-317">Cost element</span></span></th>
<th><span data-ttu-id="e4b21-318">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="e4b21-318">Cost behavior</span></span></th>
<th><span data-ttu-id="e4b21-319">Summa</span><span class="sxs-lookup"><span data-stu-id="e4b21-319">Amount</span></span></th>
<th><span data-ttu-id="e4b21-320">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="e4b21-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-321">CC099</span><span class="sxs-lookup"><span data-stu-id="e4b21-321">CC099</span></span></td>
<td><span data-ttu-id="e4b21-322">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="e4b21-322">Default cost center</span></span></td>
<td><span data-ttu-id="e4b21-323">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-323">10001</span></span></td>
<td><span data-ttu-id="e4b21-324">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-324">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-325">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-325">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-326">–1000,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-326">-1,000.00</span></span></td>
<td><span data-ttu-id="e4b21-327">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-328">CC001</span><span class="sxs-lookup"><span data-stu-id="e4b21-328">CC001</span></span></td>
<td><span data-ttu-id="e4b21-329">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="e4b21-329">HR</span></span></td>
<td><span data-ttu-id="e4b21-330">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-330">10001</span></span></td>
<td><span data-ttu-id="e4b21-331">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-331">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-332">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-332">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-333">500,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-333">500.00</span></span></td>
<td><span data-ttu-id="e4b21-334">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-335">CC002</span><span class="sxs-lookup"><span data-stu-id="e4b21-335">CC002</span></span></td>
<td><span data-ttu-id="e4b21-336">Finantsid</span><span class="sxs-lookup"><span data-stu-id="e4b21-336">Finance</span></span></td>
<td><span data-ttu-id="e4b21-337">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-337">10001</span></span></td>
<td><span data-ttu-id="e4b21-338">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-338">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-339">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-339">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-340">500,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-340">500.00</span></span></td>
<td><span data-ttu-id="e4b21-341">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-342">CC099</span><span class="sxs-lookup"><span data-stu-id="e4b21-342">CC099</span></span></td>
<td><span data-ttu-id="e4b21-343">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="e4b21-343">Default cost center</span></span></td>
<td><span data-ttu-id="e4b21-344">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-344">10001</span></span></td>
<td><span data-ttu-id="e4b21-345">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-345">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-346">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-346">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-347">–9000,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-347">-9,000.00</span></span></td>
<td><span data-ttu-id="e4b21-348">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-349">CC001</span><span class="sxs-lookup"><span data-stu-id="e4b21-349">CC001</span></span></td>
<td><span data-ttu-id="e4b21-350">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="e4b21-350">HR</span></span></td>
<td><span data-ttu-id="e4b21-351">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-351">10001</span></span></td>
<td><span data-ttu-id="e4b21-352">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-352">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-353">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-353">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="e4b21-354">1,285.71</span></span></td>
<td><span data-ttu-id="e4b21-355">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-356">CC002</span><span class="sxs-lookup"><span data-stu-id="e4b21-356">CC002</span></span></td>
<td><span data-ttu-id="e4b21-357">Finantsid</span><span class="sxs-lookup"><span data-stu-id="e4b21-357">Finance</span></span></td>
<td><span data-ttu-id="e4b21-358">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-358">10001</span></span></td>
<td><span data-ttu-id="e4b21-359">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-359">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-360">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-360">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="e4b21-361">7,714.29</span></span></td>
<td><span data-ttu-id="e4b21-362">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4b21-363">Lisateavet vt teemast [Kulujaotise poliitika loomine ja määramine kulujuhtimisüksusele (tegevuse juhis)](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="e4b21-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="e4b21-364">3. etapp: üldkulude määra arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="e4b21-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="e4b21-365">Üldkulude määra kasutatakse ühe või mitme kindla kuluobjekti debiteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="e4b21-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="e4b21-366">Tasu põhineb eelmääratud kulumääral ja väärtusel määratud eraldamisalusest.</span><span class="sxs-lookup"><span data-stu-id="e4b21-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="e4b21-367">Üldkulu määra määratlemine</span><span class="sxs-lookup"><span data-stu-id="e4b21-367">Define the overhead rate</span></span>

<span data-ttu-id="e4b21-368">Kuluobjekt CC001 inimressursid panustab sisemiste projektide kogumisse.</span><span class="sxs-lookup"><span data-stu-id="e4b21-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="e4b21-369">Luuakse statistilise dimensiooni liige nimega Inimressursside projektid, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="e4b21-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-370">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-370">Cost object</span></span></th>
<th><span data-ttu-id="e4b21-371">Tunnid</span><span class="sxs-lookup"><span data-stu-id="e4b21-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-372">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-372">Proj 1</span></span></td>
<td><span data-ttu-id="e4b21-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-373">Project 1</span></span></td>
<td><span data-ttu-id="e4b21-374">3</span><span class="sxs-lookup"><span data-stu-id="e4b21-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-375">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-375">Proj 2</span></span></td>
<td><span data-ttu-id="e4b21-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-376">Project 2</span></span></td>
<td><span data-ttu-id="e4b21-377">1</span><span class="sxs-lookup"><span data-stu-id="e4b21-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4b21-378">Määratletud on eelmääratud kulumäär kuluprojektide panusele.</span><span class="sxs-lookup"><span data-stu-id="e4b21-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-379">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-379">Cost object</span></span></th>
<th><span data-ttu-id="e4b21-380">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="e4b21-380">Cost element</span></span></th>
<th><span data-ttu-id="e4b21-381">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="e4b21-381">Cost behavior</span></span></th>
<th><span data-ttu-id="e4b21-382">Ühikud</span><span class="sxs-lookup"><span data-stu-id="e4b21-382">Units</span></span></th>
<th><span data-ttu-id="e4b21-383">Kurss</span><span class="sxs-lookup"><span data-stu-id="e4b21-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-384">CC001</span><span class="sxs-lookup"><span data-stu-id="e4b21-384">CC001</span></span></td>
<td><span data-ttu-id="e4b21-385">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="e4b21-385">HR</span></span></td>
<td><span data-ttu-id="e4b21-386">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-386">10001</span></span></td>
<td><span data-ttu-id="e4b21-387">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-387">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-388">1</span><span class="sxs-lookup"><span data-stu-id="e4b21-388">1</span></span></td>
<td><span data-ttu-id="e4b21-389">10</span><span class="sxs-lookup"><span data-stu-id="e4b21-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4b21-390">Järgmises tabelis on näidatud tulemus, kui inimressursside projektid on rakendatud eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="e4b21-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-391">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-391">Cost object</span></span></th>
<th><span data-ttu-id="e4b21-392">Väärtus</span><span class="sxs-lookup"><span data-stu-id="e4b21-392">Magnitude</span></span></th>
<th><span data-ttu-id="e4b21-393">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="e4b21-393">Cost element</span></span></th>
<th><span data-ttu-id="e4b21-394">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="e4b21-394">Allocation factor</span></span></th>
<th><span data-ttu-id="e4b21-395">Summa</span><span class="sxs-lookup"><span data-stu-id="e4b21-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-396">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-396">Proj 1</span></span></td>
<td><span data-ttu-id="e4b21-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-397">Project 1</span></span></td>
<td><span data-ttu-id="e4b21-398">3</span><span class="sxs-lookup"><span data-stu-id="e4b21-398">3</span></span></td>
<td><span data-ttu-id="e4b21-399">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-399">10001</span></span></td>
<td><span data-ttu-id="e4b21-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="e4b21-401">30,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-402">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-402">Proj 2</span></span></td>
<td><span data-ttu-id="e4b21-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-403">Project 2</span></span></td>
<td><span data-ttu-id="e4b21-404">1</span><span class="sxs-lookup"><span data-stu-id="e4b21-404">1</span></span></td>
<td><span data-ttu-id="e4b21-405">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-405">10001</span></span></td>
<td><span data-ttu-id="e4b21-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="e4b21-407">10,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="e4b21-408">Tööleht</span><span class="sxs-lookup"><span data-stu-id="e4b21-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4b21-409">Tööleht</span><span class="sxs-lookup"><span data-stu-id="e4b21-409">Journal</span></span></th>
<th><span data-ttu-id="e4b21-410">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="e4b21-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e4b21-411">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="e4b21-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e4b21-412">Versioon</span><span class="sxs-lookup"><span data-stu-id="e4b21-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-413">00003</span><span class="sxs-lookup"><span data-stu-id="e4b21-413">00003</span></span></td>
<td><span data-ttu-id="e4b21-414">Üldkulu määra arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="e4b21-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="e4b21-415">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="e4b21-415">Fiscal</span></span></td>
<td><span data-ttu-id="e4b21-416">2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-416">2017</span></span></td>
<td><span data-ttu-id="e4b21-417">Periood 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-417">Period 1</span></span></td>
<td><span data-ttu-id="e4b21-418">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="e4b21-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="e4b21-419">Töölehe sisestused (töölehe sisestused üldkulu määra arvutamiseks)</span><span class="sxs-lookup"><span data-stu-id="e4b21-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4b21-420">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="e4b21-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e4b21-421">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-421">Cost object</span></span></th>
<th><span data-ttu-id="e4b21-422">Väärtus</span><span class="sxs-lookup"><span data-stu-id="e4b21-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-423">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4b21-424">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-424">Proj 1</span></span></td>
<td><span data-ttu-id="e4b21-425">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="e4b21-426">3,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-427">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4b21-428">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-428">Proj 2</span></span></td>
<td><span data-ttu-id="e4b21-429">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="e4b21-430">1,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e4b21-431">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="e4b21-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-432">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e4b21-433">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="e4b21-433">Cost element</span></span></th>
<th><span data-ttu-id="e4b21-434">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="e4b21-434">Cost behavior</span></span></th>
<th><span data-ttu-id="e4b21-435">Summa</span><span class="sxs-lookup"><span data-stu-id="e4b21-435">Amount</span></span></th>
<th><span data-ttu-id="e4b21-436">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="e4b21-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="e4b21-437">CC0001</span></span></td>
<td><span data-ttu-id="e4b21-438">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="e4b21-438">HR</span></span></td>
<td><span data-ttu-id="e4b21-439">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-439">10001</span></span></td>
<td><span data-ttu-id="e4b21-440">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-440">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-441">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-441">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-442">–30,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-442">-30.00</span></span></td>
<td><span data-ttu-id="e4b21-443">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-444">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-444">Proj 1</span></span></td>
<td><span data-ttu-id="e4b21-445">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="e4b21-446">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-446">10001</span></span></td>
<td><span data-ttu-id="e4b21-447">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-447">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-448">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-448">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-449">30,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-449">30.00</span></span></td>
<td><span data-ttu-id="e4b21-450">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-451">CC001</span><span class="sxs-lookup"><span data-stu-id="e4b21-451">CC001</span></span></td>
<td><span data-ttu-id="e4b21-452">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="e4b21-452">HR</span></span></td>
<td><span data-ttu-id="e4b21-453">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-453">10001</span></span></td>
<td><span data-ttu-id="e4b21-454">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-454">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-455">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-455">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-456">-10.00</span></span></td>
<td><span data-ttu-id="e4b21-457">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-458">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-458">Proj 2</span></span></td>
<td><span data-ttu-id="e4b21-459">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="e4b21-460">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-460">10001</span></span></td>
<td><span data-ttu-id="e4b21-461">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-461">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-462">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-462">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-463">10.00</span><span class="sxs-lookup"><span data-stu-id="e4b21-463">10.00</span></span></td>
<td><span data-ttu-id="e4b21-464">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4b21-465">Lisateavet vt teemast [Üldkulude arvutamine](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="e4b21-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="e4b21-466">4. etapp: kulueralduse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="e4b21-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="e4b21-467">Eraldamist kasutatakse kuluobjekti saldo eraldamiseks teistele kuluobjektidele, rakendades eraldamisalust.</span><span class="sxs-lookup"><span data-stu-id="e4b21-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="e4b21-468">Finance toetab vastastikuse eraldamise meetodit.</span><span class="sxs-lookup"><span data-stu-id="e4b21-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="e4b21-469">Vastastikuse eraldamise meetodi puhul tuvastatakse täiendavate kuluobjektide vahetatavad vastastikused teenused.</span><span class="sxs-lookup"><span data-stu-id="e4b21-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="e4b21-470">Süsteem määrab automaatselt eraldamiste tegemise õige järjekorra.</span><span class="sxs-lookup"><span data-stu-id="e4b21-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="e4b21-471">Kuluobjekti saldo eraldatakse üksiku eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="e4b21-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="e4b21-472">Toetatakse eraldamisi kuluobjektide dimensioonide ja nende vastavate liikmete seas.</span><span class="sxs-lookup"><span data-stu-id="e4b21-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="e4b21-473">Eraldamisjärjekorda reguleerib kulujuhtseade.</span><span class="sxs-lookup"><span data-stu-id="e4b21-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="e4b21-474">[![Vastastikune meetod](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="e4b21-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="e4b21-475">Kulueraldamise määratlemine</span><span class="sxs-lookup"><span data-stu-id="e4b21-475">Define the cost allocation</span></span>

<span data-ttu-id="e4b21-476">Siin on lihtne näide, mis selgitab, kuidas jälgida kulu liikumist.</span><span class="sxs-lookup"><span data-stu-id="e4b21-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="e4b21-477">Kuluobjekt CC001 inimressursid panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="e4b21-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="e4b21-478">Luuakse statistilise dimensiooni liige nimega Inimressursside teenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="e4b21-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-479">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-479">Cost object</span></span></th>
<th><span data-ttu-id="e4b21-480">Inimressursside teenused</span><span class="sxs-lookup"><span data-stu-id="e4b21-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-481">CC002</span><span class="sxs-lookup"><span data-stu-id="e4b21-481">CC002</span></span></td>
<td><span data-ttu-id="e4b21-482">Finantsid</span><span class="sxs-lookup"><span data-stu-id="e4b21-482">Finance</span></span></td>
<td><span data-ttu-id="e4b21-483">35</span><span class="sxs-lookup"><span data-stu-id="e4b21-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-484">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-484">CC003</span></span></td>
<td><span data-ttu-id="e4b21-485">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-485">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-486">55</span><span class="sxs-lookup"><span data-stu-id="e4b21-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-487">CC004</span><span class="sxs-lookup"><span data-stu-id="e4b21-487">CC004</span></span></td>
<td><span data-ttu-id="e4b21-488">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="e4b21-488">Packaging</span></span></td>
<td><span data-ttu-id="e4b21-489">10</span><span class="sxs-lookup"><span data-stu-id="e4b21-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4b21-490">Kuluobjekt CC002 rahandus panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="e4b21-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="e4b21-491">Luuakse statistilise dimensiooni liige nimega Rahandusteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="e4b21-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-492">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-492">Cost object</span></span></th>
<th><span data-ttu-id="e4b21-493">Rahandusteenused</span><span class="sxs-lookup"><span data-stu-id="e4b21-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-494">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-494">CC003</span></span></td>
<td><span data-ttu-id="e4b21-495">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-495">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-496">65</span><span class="sxs-lookup"><span data-stu-id="e4b21-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-497">CC004</span><span class="sxs-lookup"><span data-stu-id="e4b21-497">CC004</span></span></td>
<td><span data-ttu-id="e4b21-498">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="e4b21-498">Packaging</span></span></td>
<td><span data-ttu-id="e4b21-499">35</span><span class="sxs-lookup"><span data-stu-id="e4b21-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4b21-500">Kuluobjekt CC003 assembler panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="e4b21-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="e4b21-501">Luuakse statistilise dimensiooni liige nimega Assembleriteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="e4b21-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-502">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-502">Cost object</span></span></th>
<th><span data-ttu-id="e4b21-503">Assembleriteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="e4b21-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-504">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-504">Prod 1</span></span></td>
<td><span data-ttu-id="e4b21-505">Toode 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-505">Product 1</span></span></td>
<td><span data-ttu-id="e4b21-506">60</span><span class="sxs-lookup"><span data-stu-id="e4b21-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-507">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-507">Prod 2</span></span></td>
<td><span data-ttu-id="e4b21-508">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-508">Product 2</span></span></td>
<td><span data-ttu-id="e4b21-509">20</span><span class="sxs-lookup"><span data-stu-id="e4b21-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4b21-510">Kuluobjekt CC004 pakendamine panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="e4b21-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="e4b21-511">Luuakse statistilise dimensiooni liige nimega Pakendamisteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="e4b21-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-512">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-512">Cost object</span></span></th>
<th><span data-ttu-id="e4b21-513">Pakendamisteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="e4b21-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-514">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-514">Prod 1</span></span></td>
<td><span data-ttu-id="e4b21-515">Toode 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-515">Product 1</span></span></td>
<td><span data-ttu-id="e4b21-516">80</span><span class="sxs-lookup"><span data-stu-id="e4b21-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-517">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-517">Prod 2</span></span></td>
<td><span data-ttu-id="e4b21-518">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-518">Product 2</span></span></td>
<td><span data-ttu-id="e4b21-519">15</span><span class="sxs-lookup"><span data-stu-id="e4b21-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e4b21-520">Statistilised mõõdud, nagu toote tarbitud tootmistunnid, saab tuletada lähteandmetest.</span><span class="sxs-lookup"><span data-stu-id="e4b21-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="e4b21-521">Lisateavet vt teemast [Statistiliste mõõtude pakkuja mall](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="e4b21-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="e4b21-522">Järgmises tabelis on näidatud tulemus, kui HR-teenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="e4b21-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-523">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-523">Cost object</span></span></th>
<th><span data-ttu-id="e4b21-524">Väärtus</span><span class="sxs-lookup"><span data-stu-id="e4b21-524">Magnitude</span></span></th>
<th><span data-ttu-id="e4b21-525">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="e4b21-525">Allocation factor</span></span></th>
<th><span data-ttu-id="e4b21-526">Summa</span><span class="sxs-lookup"><span data-stu-id="e4b21-526">Amount</span></span></th>
<th><span data-ttu-id="e4b21-527">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="e4b21-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-528">CC002</span><span class="sxs-lookup"><span data-stu-id="e4b21-528">CC002</span></span></td>
<td><span data-ttu-id="e4b21-529">Finantsid</span><span class="sxs-lookup"><span data-stu-id="e4b21-529">Finance</span></span></td>
<td><span data-ttu-id="e4b21-530">35</span><span class="sxs-lookup"><span data-stu-id="e4b21-530">35</span></span></td>
<td><span data-ttu-id="e4b21-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e4b21-532">175.00</span><span class="sxs-lookup"><span data-stu-id="e4b21-532">175.00</span></span></td>
<td><span data-ttu-id="e4b21-533">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-534">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-534">CC003</span></span></td>
<td><span data-ttu-id="e4b21-535">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-535">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-536">55</span><span class="sxs-lookup"><span data-stu-id="e4b21-536">55</span></span></td>
<td><span data-ttu-id="e4b21-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e4b21-538">275.00</span><span class="sxs-lookup"><span data-stu-id="e4b21-538">275.00</span></span></td>
<td><span data-ttu-id="e4b21-539">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-540">CC004</span><span class="sxs-lookup"><span data-stu-id="e4b21-540">CC004</span></span></td>
<td><span data-ttu-id="e4b21-541">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="e4b21-541">Packaging</span></span></td>
<td><span data-ttu-id="e4b21-542">10</span><span class="sxs-lookup"><span data-stu-id="e4b21-542">10</span></span></td>
<td><span data-ttu-id="e4b21-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="e4b21-544">50,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-544">50.00</span></span></td>
<td><span data-ttu-id="e4b21-545">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-546">CC002</span><span class="sxs-lookup"><span data-stu-id="e4b21-546">CC002</span></span></td>
<td><span data-ttu-id="e4b21-547">Finantsid</span><span class="sxs-lookup"><span data-stu-id="e4b21-547">Finance</span></span></td>
<td><span data-ttu-id="e4b21-548">35</span><span class="sxs-lookup"><span data-stu-id="e4b21-548">35</span></span></td>
<td><span data-ttu-id="e4b21-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="e4b21-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e4b21-550">436.00</span><span class="sxs-lookup"><span data-stu-id="e4b21-550">436.00</span></span></td>
<td><span data-ttu-id="e4b21-551">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-552">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-552">CC003</span></span></td>
<td><span data-ttu-id="e4b21-553">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-553">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-554">55</span><span class="sxs-lookup"><span data-stu-id="e4b21-554">55</span></span></td>
<td><span data-ttu-id="e4b21-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="e4b21-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e4b21-556">685.14</span><span class="sxs-lookup"><span data-stu-id="e4b21-556">685.14</span></span></td>
<td><span data-ttu-id="e4b21-557">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-558">CC004</span><span class="sxs-lookup"><span data-stu-id="e4b21-558">CC004</span></span></td>
<td><span data-ttu-id="e4b21-559">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="e4b21-559">Packaging</span></span></td>
<td><span data-ttu-id="e4b21-560">10</span><span class="sxs-lookup"><span data-stu-id="e4b21-560">10</span></span></td>
<td><span data-ttu-id="e4b21-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="e4b21-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="e4b21-562">124.57</span><span class="sxs-lookup"><span data-stu-id="e4b21-562">124.57</span></span></td>
<td><span data-ttu-id="e4b21-563">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4b21-564">Järgmises tabelis on näidatud tulemus, kui Rahandusteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="e4b21-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-565">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-565">Cost object</span></span></th>
<th><span data-ttu-id="e4b21-566">Väärtus</span><span class="sxs-lookup"><span data-stu-id="e4b21-566">Magnitude</span></span></th>
<th><span data-ttu-id="e4b21-567">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="e4b21-567">Allocation factor</span></span></th>
<th><span data-ttu-id="e4b21-568">Summa</span><span class="sxs-lookup"><span data-stu-id="e4b21-568">Amount</span></span></th>
<th><span data-ttu-id="e4b21-569">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="e4b21-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-570">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-570">CC003</span></span></td>
<td><span data-ttu-id="e4b21-571">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-571">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-572">65</span><span class="sxs-lookup"><span data-stu-id="e4b21-572">65</span></span></td>
<td><span data-ttu-id="e4b21-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="e4b21-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="e4b21-574">438.75</span><span class="sxs-lookup"><span data-stu-id="e4b21-574">438.75</span></span></td>
<td><span data-ttu-id="e4b21-575">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-576">CC004</span><span class="sxs-lookup"><span data-stu-id="e4b21-576">CC004</span></span></td>
<td><span data-ttu-id="e4b21-577">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="e4b21-577">Packaging</span></span></td>
<td><span data-ttu-id="e4b21-578">35</span><span class="sxs-lookup"><span data-stu-id="e4b21-578">35</span></span></td>
<td><span data-ttu-id="e4b21-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="e4b21-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="e4b21-580">236.25</span><span class="sxs-lookup"><span data-stu-id="e4b21-580">236.25</span></span></td>
<td><span data-ttu-id="e4b21-581">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-582">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-582">CC003</span></span></td>
<td><span data-ttu-id="e4b21-583">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-583">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-584">65</span><span class="sxs-lookup"><span data-stu-id="e4b21-584">65</span></span></td>
<td><span data-ttu-id="e4b21-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="e4b21-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="e4b21-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="e4b21-586">5,297.69</span></span></td>
<td><span data-ttu-id="e4b21-587">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-588">CC004</span><span class="sxs-lookup"><span data-stu-id="e4b21-588">CC004</span></span></td>
<td><span data-ttu-id="e4b21-589">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="e4b21-589">Packaging</span></span></td>
<td><span data-ttu-id="e4b21-590">35</span><span class="sxs-lookup"><span data-stu-id="e4b21-590">35</span></span></td>
<td><span data-ttu-id="e4b21-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="e4b21-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="e4b21-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="e4b21-592">2,852.60</span></span></td>
<td><span data-ttu-id="e4b21-593">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4b21-594">Järgmises tabelis on näidatud tulemus, kui Assembleriteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="e4b21-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-595">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-595">Cost object</span></span></th>
<th><span data-ttu-id="e4b21-596">Väärtus</span><span class="sxs-lookup"><span data-stu-id="e4b21-596">Magnitude</span></span></th>
<th><span data-ttu-id="e4b21-597">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="e4b21-597">Allocation factor</span></span></th>
<th><span data-ttu-id="e4b21-598">Summa</span><span class="sxs-lookup"><span data-stu-id="e4b21-598">Amount</span></span></th>
<th><span data-ttu-id="e4b21-599">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="e4b21-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-600">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-600">Prod 1</span></span></td>
<td><span data-ttu-id="e4b21-601">Toode 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-601">Product 1</span></span></td>
<td><span data-ttu-id="e4b21-602">60</span><span class="sxs-lookup"><span data-stu-id="e4b21-602">60</span></span></td>
<td><span data-ttu-id="e4b21-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="e4b21-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="e4b21-604">535.31</span><span class="sxs-lookup"><span data-stu-id="e4b21-604">535.31</span></span></td>
<td><span data-ttu-id="e4b21-605">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-606">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-606">Prod 2</span></span></td>
<td><span data-ttu-id="e4b21-607">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-607">Product 2</span></span></td>
<td><span data-ttu-id="e4b21-608">20</span><span class="sxs-lookup"><span data-stu-id="e4b21-608">20</span></span></td>
<td><span data-ttu-id="e4b21-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="e4b21-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="e4b21-610">178.44</span><span class="sxs-lookup"><span data-stu-id="e4b21-610">178.44</span></span></td>
<td><span data-ttu-id="e4b21-611">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-612">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-612">Prod 1</span></span></td>
<td><span data-ttu-id="e4b21-613">Toode 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-613">Product 1</span></span></td>
<td><span data-ttu-id="e4b21-614">60</span><span class="sxs-lookup"><span data-stu-id="e4b21-614">60</span></span></td>
<td><span data-ttu-id="e4b21-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="e4b21-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="e4b21-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="e4b21-616">4,487.12</span></span></td>
<td><span data-ttu-id="e4b21-617">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-618">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-618">Prod 2</span></span></td>
<td><span data-ttu-id="e4b21-619">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-619">Product 2</span></span></td>
<td><span data-ttu-id="e4b21-620">20</span><span class="sxs-lookup"><span data-stu-id="e4b21-620">20</span></span></td>
<td><span data-ttu-id="e4b21-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="e4b21-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="e4b21-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="e4b21-622">1,495.71</span></span></td>
<td><span data-ttu-id="e4b21-623">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4b21-624">Järgmises tabelis on näidatud tulemus, kui Pakendamisteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="e4b21-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-625">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-625">Cost object</span></span></th>
<th><span data-ttu-id="e4b21-626">Väärtus</span><span class="sxs-lookup"><span data-stu-id="e4b21-626">Magnitude</span></span></th>
<th><span data-ttu-id="e4b21-627">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="e4b21-627">Allocation factor</span></span></th>
<th><span data-ttu-id="e4b21-628">Summa</span><span class="sxs-lookup"><span data-stu-id="e4b21-628">Amount</span></span></th>
<th><span data-ttu-id="e4b21-629">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="e4b21-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-630">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-630">Prod 1</span></span></td>
<td><span data-ttu-id="e4b21-631">Toode 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-631">Product 1</span></span></td>
<td><span data-ttu-id="e4b21-632">80</span><span class="sxs-lookup"><span data-stu-id="e4b21-632">80</span></span></td>
<td><span data-ttu-id="e4b21-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="e4b21-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="e4b21-634">241.05</span><span class="sxs-lookup"><span data-stu-id="e4b21-634">241.05</span></span></td>
<td><span data-ttu-id="e4b21-635">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-636">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-636">Prod 2</span></span></td>
<td><span data-ttu-id="e4b21-637">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-637">Product 2</span></span></td>
<td><span data-ttu-id="e4b21-638">15</span><span class="sxs-lookup"><span data-stu-id="e4b21-638">15</span></span></td>
<td><span data-ttu-id="e4b21-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="e4b21-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="e4b21-640">45.20</span><span class="sxs-lookup"><span data-stu-id="e4b21-640">45.20</span></span></td>
<td><span data-ttu-id="e4b21-641">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-642">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-642">Prod 1</span></span></td>
<td><span data-ttu-id="e4b21-643">Toode 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-643">Product 1</span></span></td>
<td><span data-ttu-id="e4b21-644">80</span><span class="sxs-lookup"><span data-stu-id="e4b21-644">80</span></span></td>
<td><span data-ttu-id="e4b21-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="e4b21-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="e4b21-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="e4b21-646">2,507.09</span></span></td>
<td><span data-ttu-id="e4b21-647">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-648">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-648">Prod 2</span></span></td>
<td><span data-ttu-id="e4b21-649">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-649">Product 2</span></span></td>
<td><span data-ttu-id="e4b21-650">15</span><span class="sxs-lookup"><span data-stu-id="e4b21-650">15</span></span></td>
<td><span data-ttu-id="e4b21-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="e4b21-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="e4b21-652">470.08</span><span class="sxs-lookup"><span data-stu-id="e4b21-652">470.08</span></span></td>
<td><span data-ttu-id="e4b21-653">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="e4b21-654">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="e4b21-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4b21-655">Tööleht</span><span class="sxs-lookup"><span data-stu-id="e4b21-655">Journal</span></span></th>
<th><span data-ttu-id="e4b21-656">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="e4b21-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="e4b21-657">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="e4b21-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="e4b21-658">Versioon</span><span class="sxs-lookup"><span data-stu-id="e4b21-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-659">00004</span><span class="sxs-lookup"><span data-stu-id="e4b21-659">00004</span></span></td>
<td><span data-ttu-id="e4b21-660">Kulueralduse tööleht</span><span class="sxs-lookup"><span data-stu-id="e4b21-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="e4b21-661">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="e4b21-661">Fiscal</span></span></td>
<td><span data-ttu-id="e4b21-662">2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-662">2017</span></span></td>
<td><span data-ttu-id="e4b21-663">Periood 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-663">Period 1</span></span></td>
<td><span data-ttu-id="e4b21-664">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="e4b21-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="e4b21-665">Töölehe read</span><span class="sxs-lookup"><span data-stu-id="e4b21-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e4b21-666">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="e4b21-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="e4b21-667">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e4b21-668">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="e4b21-668">Cost element</span></span></th>
<th><span data-ttu-id="e4b21-669">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="e4b21-669">Cost behavior</span></span></th>
<th><span data-ttu-id="e4b21-670">Summa</span><span class="sxs-lookup"><span data-stu-id="e4b21-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-671">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4b21-672">CC001</span><span class="sxs-lookup"><span data-stu-id="e4b21-672">CC001</span></span></td>
<td><span data-ttu-id="e4b21-673">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="e4b21-673">HR</span></span></td>
<td><span data-ttu-id="e4b21-674">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-674">10001</span></span></td>
<td><span data-ttu-id="e4b21-675">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-675">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-676">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-676">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-677">500,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-678">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4b21-679">CC001</span><span class="sxs-lookup"><span data-stu-id="e4b21-679">CC001</span></span></td>
<td><span data-ttu-id="e4b21-680">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="e4b21-680">HR</span></span></td>
<td><span data-ttu-id="e4b21-681">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-681">10001</span></span></td>
<td><span data-ttu-id="e4b21-682">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-682">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-683">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-683">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="e4b21-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-685">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4b21-686">CC002</span><span class="sxs-lookup"><span data-stu-id="e4b21-686">CC002</span></span></td>
<td><span data-ttu-id="e4b21-687">Finantsid</span><span class="sxs-lookup"><span data-stu-id="e4b21-687">Finance</span></span></td>
<td><span data-ttu-id="e4b21-688">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-688">10001</span></span></td>
<td><span data-ttu-id="e4b21-689">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-689">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-690">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-690">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-691">675.00</span><span class="sxs-lookup"><span data-stu-id="e4b21-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-692">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4b21-693">CC002</span><span class="sxs-lookup"><span data-stu-id="e4b21-693">CC002</span></span></td>
<td><span data-ttu-id="e4b21-694">Finantsid</span><span class="sxs-lookup"><span data-stu-id="e4b21-694">Finance</span></span></td>
<td><span data-ttu-id="e4b21-695">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-695">10001</span></span></td>
<td><span data-ttu-id="e4b21-696">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-696">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-697">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-697">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="e4b21-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-699">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4b21-700">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-700">CC003</span></span></td>
<td><span data-ttu-id="e4b21-701">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-701">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-702">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-702">10001</span></span></td>
<td><span data-ttu-id="e4b21-703">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-703">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-704">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-704">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-705">713.75</span><span class="sxs-lookup"><span data-stu-id="e4b21-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-706">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4b21-707">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-707">CC003</span></span></td>
<td><span data-ttu-id="e4b21-708">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-708">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-709">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-709">10001</span></span></td>
<td><span data-ttu-id="e4b21-710">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-710">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-711">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-711">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="e4b21-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-713">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4b21-714">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-714">CC003</span></span></td>
<td><span data-ttu-id="e4b21-715">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="e4b21-715">Packaging</span></span></td>
<td><span data-ttu-id="e4b21-716">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-716">10001</span></span></td>
<td><span data-ttu-id="e4b21-717">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-717">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-718">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-718">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-719">286.25</span><span class="sxs-lookup"><span data-stu-id="e4b21-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-720">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4b21-721">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-721">CC003</span></span></td>
<td><span data-ttu-id="e4b21-722">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="e4b21-722">Packaging</span></span></td>
<td><span data-ttu-id="e4b21-723">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-723">10001</span></span></td>
<td><span data-ttu-id="e4b21-724">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-724">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-725">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-725">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="e4b21-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-727">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4b21-728">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-728">Prod 1</span></span></td>
<td><span data-ttu-id="e4b21-729">Toode 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-729">Product 1</span></span></td>
<td><span data-ttu-id="e4b21-730">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-730">10001</span></span></td>
<td><span data-ttu-id="e4b21-731">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-731">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-732">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-732">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-733">776.36</span><span class="sxs-lookup"><span data-stu-id="e4b21-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-734">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4b21-735">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-735">Prod 1</span></span></td>
<td><span data-ttu-id="e4b21-736">Toode 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-736">Product 1</span></span></td>
<td><span data-ttu-id="e4b21-737">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-737">10001</span></span></td>
<td><span data-ttu-id="e4b21-738">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-738">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-739">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-739">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="e4b21-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-741">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4b21-742">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-742">Prod 2</span></span></td>
<td><span data-ttu-id="e4b21-743">Toode 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-743">Product 1</span></span></td>
<td><span data-ttu-id="e4b21-744">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-744">10001</span></span></td>
<td><span data-ttu-id="e4b21-745">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-745">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-746">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-746">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-747">223.64</span><span class="sxs-lookup"><span data-stu-id="e4b21-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-748">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="e4b21-749">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-749">Prod 2</span></span></td>
<td><span data-ttu-id="e4b21-750">Toode 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-750">Product 1</span></span></td>
<td><span data-ttu-id="e4b21-751">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-751">10001</span></span></td>
<td><span data-ttu-id="e4b21-752">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-752">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-753">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-753">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="e4b21-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="e4b21-755">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="e4b21-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="e4b21-756">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="e4b21-757">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="e4b21-757">Cost element</span></span></th>
<th><span data-ttu-id="e4b21-758">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="e4b21-758">Cost behavior</span></span></th>
<th><span data-ttu-id="e4b21-759">Summa</span><span class="sxs-lookup"><span data-stu-id="e4b21-759">Amount</span></span></th>
<th><span data-ttu-id="e4b21-760">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="e4b21-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4b21-761">CC001</span><span class="sxs-lookup"><span data-stu-id="e4b21-761">CC001</span></span></td>
<td><span data-ttu-id="e4b21-762">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="e4b21-762">HR</span></span></td>
<td><span data-ttu-id="e4b21-763">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-763">10001</span></span></td>
<td><span data-ttu-id="e4b21-764">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-764">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-765">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-765">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-766">‑500,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-766">-500.00</span></span></td>
<td><span data-ttu-id="e4b21-767">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-768">CC002</span><span class="sxs-lookup"><span data-stu-id="e4b21-768">CC002</span></span></td>
<td><span data-ttu-id="e4b21-769">Finantsid</span><span class="sxs-lookup"><span data-stu-id="e4b21-769">Finance</span></span></td>
<td><span data-ttu-id="e4b21-770">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-770">10001</span></span></td>
<td><span data-ttu-id="e4b21-771">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-771">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-772">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-772">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-773">175.00</span><span class="sxs-lookup"><span data-stu-id="e4b21-773">175.00</span></span></td>
<td><span data-ttu-id="e4b21-774">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-775">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-775">CC003</span></span></td>
<td><span data-ttu-id="e4b21-776">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-776">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-777">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-777">10001</span></span></td>
<td><span data-ttu-id="e4b21-778">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-778">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-779">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-779">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-780">275.00</span><span class="sxs-lookup"><span data-stu-id="e4b21-780">275.00</span></span></td>
<td><span data-ttu-id="e4b21-781">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-782">CC004</span><span class="sxs-lookup"><span data-stu-id="e4b21-782">CC004</span></span></td>
<td><span data-ttu-id="e4b21-783">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="e4b21-783">Packaging</span></span></td>
<td><span data-ttu-id="e4b21-784">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-784">10001</span></span></td>
<td><span data-ttu-id="e4b21-785">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-785">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-786">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-786">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-787">50,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-787">50,00</span></span></td>
<td><span data-ttu-id="e4b21-788">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-789">CC001</span><span class="sxs-lookup"><span data-stu-id="e4b21-789">CC001</span></span></td>
<td><span data-ttu-id="e4b21-790">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="e4b21-790">HR</span></span></td>
<td><span data-ttu-id="e4b21-791">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-791">10001</span></span></td>
<td><span data-ttu-id="e4b21-792">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-792">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-793">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-793">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-794">–1245,71</span><span class="sxs-lookup"><span data-stu-id="e4b21-794">-1,245.71</span></span></td>
<td><span data-ttu-id="e4b21-795">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-796">CC002</span><span class="sxs-lookup"><span data-stu-id="e4b21-796">CC002</span></span></td>
<td><span data-ttu-id="e4b21-797">Finantsid</span><span class="sxs-lookup"><span data-stu-id="e4b21-797">Finance</span></span></td>
<td><span data-ttu-id="e4b21-798">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-798">10001</span></span></td>
<td><span data-ttu-id="e4b21-799">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-799">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-800">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-800">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-801">436.00</span><span class="sxs-lookup"><span data-stu-id="e4b21-801">436.00</span></span></td>
<td><span data-ttu-id="e4b21-802">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-803">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-803">CC003</span></span></td>
<td><span data-ttu-id="e4b21-804">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-804">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-805">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-805">10001</span></span></td>
<td><span data-ttu-id="e4b21-806">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-806">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-807">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-807">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-808">685.14</span><span class="sxs-lookup"><span data-stu-id="e4b21-808">685.14</span></span></td>
<td><span data-ttu-id="e4b21-809">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-810">CC004</span><span class="sxs-lookup"><span data-stu-id="e4b21-810">CC004</span></span></td>
<td><span data-ttu-id="e4b21-811">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="e4b21-811">Packaging</span></span></td>
<td><span data-ttu-id="e4b21-812">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-812">10001</span></span></td>
<td><span data-ttu-id="e4b21-813">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-813">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-814">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-814">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-815">124.57</span><span class="sxs-lookup"><span data-stu-id="e4b21-815">124.57</span></span></td>
<td><span data-ttu-id="e4b21-816">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-817">CC002</span><span class="sxs-lookup"><span data-stu-id="e4b21-817">CC002</span></span></td>
<td><span data-ttu-id="e4b21-818">Finantsid</span><span class="sxs-lookup"><span data-stu-id="e4b21-818">Finance</span></span></td>
<td><span data-ttu-id="e4b21-819">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-819">10001</span></span></td>
<td><span data-ttu-id="e4b21-820">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-820">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-821">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-821">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-822">–675,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-822">-675.00</span></span></td>
<td><span data-ttu-id="e4b21-823">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-824">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-824">CC003</span></span></td>
<td><span data-ttu-id="e4b21-825">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-825">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-826">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-826">10001</span></span></td>
<td><span data-ttu-id="e4b21-827">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-827">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-828">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-828">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-829">438.75</span><span class="sxs-lookup"><span data-stu-id="e4b21-829">438.75</span></span></td>
<td><span data-ttu-id="e4b21-830">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-831">CC004</span><span class="sxs-lookup"><span data-stu-id="e4b21-831">CC004</span></span></td>
<td><span data-ttu-id="e4b21-832">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="e4b21-832">Packaging</span></span></td>
<td><span data-ttu-id="e4b21-833">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-833">10001</span></span></td>
<td><span data-ttu-id="e4b21-834">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-834">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-835">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-835">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-836">236.25</span><span class="sxs-lookup"><span data-stu-id="e4b21-836">236.25</span></span></td>
<td><span data-ttu-id="e4b21-837">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-838">CC002</span><span class="sxs-lookup"><span data-stu-id="e4b21-838">CC002</span></span></td>
<td><span data-ttu-id="e4b21-839">Finantsid</span><span class="sxs-lookup"><span data-stu-id="e4b21-839">Finance</span></span></td>
<td><span data-ttu-id="e4b21-840">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-840">10001</span></span></td>
<td><span data-ttu-id="e4b21-841">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-841">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-842">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-842">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-843">–8150,29</span><span class="sxs-lookup"><span data-stu-id="e4b21-843">-8,150.29</span></span></td>
<td><span data-ttu-id="e4b21-844">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-845">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-845">CC003</span></span></td>
<td><span data-ttu-id="e4b21-846">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-846">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-847">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-847">10001</span></span></td>
<td><span data-ttu-id="e4b21-848">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-848">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-849">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-849">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="e4b21-850">5,297.69</span></span></td>
<td><span data-ttu-id="e4b21-851">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-852">CC004</span><span class="sxs-lookup"><span data-stu-id="e4b21-852">CC004</span></span></td>
<td><span data-ttu-id="e4b21-853">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="e4b21-853">Packaging</span></span></td>
<td><span data-ttu-id="e4b21-854">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-854">10001</span></span></td>
<td><span data-ttu-id="e4b21-855">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-855">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-856">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-856">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="e4b21-857">2,852.60</span></span></td>
<td><span data-ttu-id="e4b21-858">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-859">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-859">CC003</span></span></td>
<td><span data-ttu-id="e4b21-860">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-860">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-861">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-861">10001</span></span></td>
<td><span data-ttu-id="e4b21-862">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-862">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-863">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-863">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-864">–713,75</span><span class="sxs-lookup"><span data-stu-id="e4b21-864">-713.75</span></span></td>
<td><span data-ttu-id="e4b21-865">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-866">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-866">Prod 1</span></span></td>
<td><span data-ttu-id="e4b21-867">Toode 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-867">Product 1</span></span></td>
<td><span data-ttu-id="e4b21-868">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-868">10001</span></span></td>
<td><span data-ttu-id="e4b21-869">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-869">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-870">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-870">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-871">535.31</span><span class="sxs-lookup"><span data-stu-id="e4b21-871">535.31</span></span></td>
<td><span data-ttu-id="e4b21-872">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-873">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-873">Prod 2</span></span></td>
<td><span data-ttu-id="e4b21-874">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-874">Product 2</span></span></td>
<td><span data-ttu-id="e4b21-875">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-875">10001</span></span></td>
<td><span data-ttu-id="e4b21-876">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-876">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-877">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-877">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-878">178.44</span><span class="sxs-lookup"><span data-stu-id="e4b21-878">178.44</span></span></td>
<td><span data-ttu-id="e4b21-879">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-880">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-880">CC003</span></span></td>
<td><span data-ttu-id="e4b21-881">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-881">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-882">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-882">10001</span></span></td>
<td><span data-ttu-id="e4b21-883">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-883">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-884">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-884">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-885">–5982,83</span><span class="sxs-lookup"><span data-stu-id="e4b21-885">-5,982.83</span></span></td>
<td><span data-ttu-id="e4b21-886">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-887">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-887">Prod 1</span></span></td>
<td><span data-ttu-id="e4b21-888">Toode 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-888">Product 1</span></span></td>
<td><span data-ttu-id="e4b21-889">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-889">10001</span></span></td>
<td><span data-ttu-id="e4b21-890">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-890">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-891">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-891">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="e4b21-892">4,487.12</span></span></td>
<td><span data-ttu-id="e4b21-893">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-894">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-894">Prod 2</span></span></td>
<td><span data-ttu-id="e4b21-895">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-895">Product 2</span></span></td>
<td><span data-ttu-id="e4b21-896">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-896">10001</span></span></td>
<td><span data-ttu-id="e4b21-897">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-897">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-898">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-898">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="e4b21-899">1,495.71</span></span></td>
<td><span data-ttu-id="e4b21-900">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-901">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-901">CC003</span></span></td>
<td><span data-ttu-id="e4b21-902">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-902">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-903">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-903">10001</span></span></td>
<td><span data-ttu-id="e4b21-904">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-904">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-905">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-905">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-906">–286,25</span><span class="sxs-lookup"><span data-stu-id="e4b21-906">-286.25</span></span></td>
<td><span data-ttu-id="e4b21-907">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-908">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-908">Prod 1</span></span></td>
<td><span data-ttu-id="e4b21-909">Toode 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-909">Product 1</span></span></td>
<td><span data-ttu-id="e4b21-910">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-910">10001</span></span></td>
<td><span data-ttu-id="e4b21-911">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-911">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-912">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-912">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-913">241.05</span><span class="sxs-lookup"><span data-stu-id="e4b21-913">241.05</span></span></td>
<td><span data-ttu-id="e4b21-914">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-915">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-915">Prod 2</span></span></td>
<td><span data-ttu-id="e4b21-916">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-916">Product 2</span></span></td>
<td><span data-ttu-id="e4b21-917">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-917">10001</span></span></td>
<td><span data-ttu-id="e4b21-918">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-918">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-919">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-919">Fixed cost</span></span></td>
<td><span data-ttu-id="e4b21-920">45.20</span><span class="sxs-lookup"><span data-stu-id="e4b21-920">45.20</span></span></td>
<td><span data-ttu-id="e4b21-921">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-922">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-922">CC003</span></span></td>
<td><span data-ttu-id="e4b21-923">Assembler</span><span class="sxs-lookup"><span data-stu-id="e4b21-923">Assembly</span></span></td>
<td><span data-ttu-id="e4b21-924">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-924">10001</span></span></td>
<td><span data-ttu-id="e4b21-925">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-925">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-926">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-926">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-927">–2977,17</span><span class="sxs-lookup"><span data-stu-id="e4b21-927">-2,977.17</span></span></td>
<td><span data-ttu-id="e4b21-928">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-929">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-929">Prod 1</span></span></td>
<td><span data-ttu-id="e4b21-930">Toode 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-930">Product 1</span></span></td>
<td><span data-ttu-id="e4b21-931">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-931">10001</span></span></td>
<td><span data-ttu-id="e4b21-932">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-932">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-933">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-933">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="e4b21-934">2,507.09</span></span></td>
<td><span data-ttu-id="e4b21-935">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4b21-936">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-936">Prod 2</span></span></td>
<td><span data-ttu-id="e4b21-937">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-937">Product 2</span></span></td>
<td><span data-ttu-id="e4b21-938">10001</span><span class="sxs-lookup"><span data-stu-id="e4b21-938">10001</span></span></td>
<td><span data-ttu-id="e4b21-939">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="e4b21-939">Electricity</span></span></td>
<td><span data-ttu-id="e4b21-940">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-940">Variable cost</span></span></td>
<td><span data-ttu-id="e4b21-941">470.08</span><span class="sxs-lookup"><span data-stu-id="e4b21-941">470.08</span></span></td>
<td><span data-ttu-id="e4b21-942">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="e4b21-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="e4b21-943">Lõppsõna</span><span class="sxs-lookup"><span data-stu-id="e4b21-943">Conclusion</span></span>
<span data-ttu-id="e4b21-944">Finantsaruandluses sisestatakse elektrikulu 10 000,00 fiktiivse kulukeskuse ID-le.</span><span class="sxs-lookup"><span data-stu-id="e4b21-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="e4b21-945">Nii teavad kuluarvestajad, et see kulu tuleb eraldada.</span><span class="sxs-lookup"><span data-stu-id="e4b21-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="e4b21-946">Kuluarvestuses liigub kulu rakendatud poliitikate ja reeglite põhjal läbi organisatsiooniüksuste ja -tasemete.</span><span class="sxs-lookup"><span data-stu-id="e4b21-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="e4b21-947">Iga kulu on seostatud eraldamisalusega, mis pakub kulude eraldamiseks parimat hinnangut.</span><span class="sxs-lookup"><span data-stu-id="e4b21-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="e4b21-948">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="e4b21-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="e4b21-949">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="e4b21-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="e4b21-950">Kokku</span><span class="sxs-lookup"><span data-stu-id="e4b21-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e4b21-951">CC099</span><span class="sxs-lookup"><span data-stu-id="e4b21-951">CC099</span></span></th>
<th><span data-ttu-id="e4b21-952">CC001</span><span class="sxs-lookup"><span data-stu-id="e4b21-952">CC001</span></span></th>
<th><span data-ttu-id="e4b21-953">CC002</span><span class="sxs-lookup"><span data-stu-id="e4b21-953">CC002</span></span></th>
<th><span data-ttu-id="e4b21-954">CC003</span><span class="sxs-lookup"><span data-stu-id="e4b21-954">CC003</span></span></th>
<th><span data-ttu-id="e4b21-955">CC004</span><span class="sxs-lookup"><span data-stu-id="e4b21-955">CC004</span></span></th>
<th><span data-ttu-id="e4b21-956">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-956">Proj 1</span></span></th>
<th><span data-ttu-id="e4b21-957">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-957">Proj 2</span></span></th>
<th><span data-ttu-id="e4b21-958">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="e4b21-958">Prod 1</span></span></th>
<th><span data-ttu-id="e4b21-959">Toode 2</span><span class="sxs-lookup"><span data-stu-id="e4b21-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="e4b21-960">10001 Elekter</span><span class="sxs-lookup"><span data-stu-id="e4b21-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4b21-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4b21-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4b21-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4b21-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4b21-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4b21-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="e4b21-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="e4b21-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4b21-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="e4b21-970">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="e4b21-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-971">0,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="e4b21-972">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-973">0,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-974">0,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-975">0,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-976">0,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-977">0,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-978">776.36</span><span class="sxs-lookup"><span data-stu-id="e4b21-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-979">223.64</span><span class="sxs-lookup"><span data-stu-id="e4b21-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4b21-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="e4b21-981">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="e4b21-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-982">000</span><span class="sxs-lookup"><span data-stu-id="e4b21-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-983">0,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-984">0,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-985">0,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-986">0,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-987">30,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-988">10,00</span><span class="sxs-lookup"><span data-stu-id="e4b21-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="e4b21-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="e4b21-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="e4b21-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="e4b21-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e4b21-992">Selles teemas selgitatakse, kuidas esmane kuluelement, 10001 Eleter, liigub läbi kuluobjektide.</span><span class="sxs-lookup"><span data-stu-id="e4b21-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="e4b21-993">Seega eraldatakse see üldkulu organisatsiooni madalaimale tasemele.</span><span class="sxs-lookup"><span data-stu-id="e4b21-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="e4b21-994">Teisisõnu kannavad kulu madalaimal tasemel olevad kuluobjektid.</span><span class="sxs-lookup"><span data-stu-id="e4b21-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="e4b21-995">Kui soovite saada kuluobjektide vahelisest kuluvoost visuaalset ülevaadet, saate kuluvoo visualiseerimiseks kasutada kulude kokkuvõtte poliitika reegleid.</span><span class="sxs-lookup"><span data-stu-id="e4b21-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="e4b21-996">Lisateavet vt teemast [Kulukomplekti poliitika ja üldkulude arvutus](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="e4b21-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]