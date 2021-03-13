---
title: Üldkulude arvutus
description: Selles teemas kirjeldatakse tüüpilisi üldkulude arvutamise ja eraldamise protsesse.
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: d60248f2bd6774b2e9afdb3632b6eb31d67349ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009514"
---
# <a name="overhead-calculation"></a><span data-ttu-id="24be3-103">Üldkulude arvutus</span><span class="sxs-lookup"><span data-stu-id="24be3-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24be3-104">Selles teemas kirjeldatakse tüüpilisi üldkulude arvutamise ja eraldamise protsesse.</span><span class="sxs-lookup"><span data-stu-id="24be3-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="24be3-105">Mõiste määratlus</span><span class="sxs-lookup"><span data-stu-id="24be3-105">Term definition</span></span>
---------------

<span data-ttu-id="24be3-106">Üldkulud on kulud, mis kaasnevad ettevõtte käitamisega, kuid mida ei saa seostada otseselt ühegi kindla äritegevuse, toote ega teenusega.</span><span class="sxs-lookup"><span data-stu-id="24be3-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="24be3-107">Üldkulud pakuvad kriitilist tuge kasumit andavate tegevuste loomisele.</span><span class="sxs-lookup"><span data-stu-id="24be3-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="24be3-108">Siin on mõned näited üldkuludest.</span><span class="sxs-lookup"><span data-stu-id="24be3-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="24be3-109">Üür</span><span class="sxs-lookup"><span data-stu-id="24be3-109">Rent</span></span>
-   <span data-ttu-id="24be3-110">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-110">Electricity</span></span>
-   <span data-ttu-id="24be3-111">Haldustasud</span><span class="sxs-lookup"><span data-stu-id="24be3-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="24be3-112">Üldkulude arvutuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="24be3-112">Overhead calculation overview</span></span>
<span data-ttu-id="24be3-113">Üldkulude arvutus käitab kuluarvutuse poliitikaid õiges järjekorras.</span><span class="sxs-lookup"><span data-stu-id="24be3-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="24be3-114">Saate käivitada üldkulude arvutuse sama rahandusperioodi kohta mitu korda, kui kuluarvestuse poliitikaid on muudetud või tuvastatud teatud tõrked.</span><span class="sxs-lookup"><span data-stu-id="24be3-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="24be3-115">Iga üldkulude arvutamise käitamine talletatakse ja see saab kordumatu versiooni-ID, mis võimaldab teil arvutuste erinevaid versioone võrrelda.</span><span class="sxs-lookup"><span data-stu-id="24be3-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="24be3-116">Ülekulude arvutusega loodud kulukirjed saavad aruandluskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="24be3-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="24be3-117">See aruandluskuupäev vastab arvutuses kasutatud rahandusperioodi lõppkuupäevale.</span><span class="sxs-lookup"><span data-stu-id="24be3-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="24be3-118">Kordumatu versiooni-ID koosneb järgmistest elementidest.</span><span class="sxs-lookup"><span data-stu-id="24be3-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="24be3-119">Versiooni tüüp</span><span class="sxs-lookup"><span data-stu-id="24be3-119">Version type</span></span>
-   <span data-ttu-id="24be3-120">Kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="24be3-120">Date and time</span></span>
-   <span data-ttu-id="24be3-121">Kuluarvestuse pearaamat</span><span class="sxs-lookup"><span data-stu-id="24be3-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="24be3-122">Finantsaasta</span><span class="sxs-lookup"><span data-stu-id="24be3-122">Fiscal year</span></span>
-   <span data-ttu-id="24be3-123">Rahandusperiood</span><span class="sxs-lookup"><span data-stu-id="24be3-123">Fiscal period</span></span>

<span data-ttu-id="24be3-124">Üldkulude arvutus käivitatakse versioonist sõltumatult.</span><span class="sxs-lookup"><span data-stu-id="24be3-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="24be3-125">Seetõttu saate arvutada eelarveversiooni enne tegelikku versiooni.</span><span class="sxs-lookup"><span data-stu-id="24be3-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="24be3-126">Üldkulude arvutus koosneb neljast etapist, nagu näha alltoodud joonisel.</span><span class="sxs-lookup"><span data-stu-id="24be3-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="24be3-127">Igas etapis luuakse töölehe päis, millel on töölehe kanded.</span><span class="sxs-lookup"><span data-stu-id="24be3-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="24be3-128">See töölehe päis säiiltab sisendandmeid iga arvutusetapi kohta.</span><span class="sxs-lookup"><span data-stu-id="24be3-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="24be3-129">Igale töölehe reale rakendatakse poliitikad ja reeglid ning väljundina luuakse kulukirjed.</span><span class="sxs-lookup"><span data-stu-id="24be3-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="24be3-130">Seega on teil alati olemas põhjalik ülevaade.</span><span class="sxs-lookup"><span data-stu-id="24be3-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="24be3-131">[![Üldkulude arvutus](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="24be3-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="24be3-132">Elektri üldkulude arvutamine ja eraldamine</span><span class="sxs-lookup"><span data-stu-id="24be3-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="24be3-133">Finantsaruandluses on mõned kulud, näiteks elekter, registreeritud põhisummana.</span><span class="sxs-lookup"><span data-stu-id="24be3-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="24be3-134">Seetõttu ei pakuta kuluarvestuseks üksikasjalikku juhtimisülevaadet.</span><span class="sxs-lookup"><span data-stu-id="24be3-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="24be3-135">Kuluarvestuses peavad kulud liikuma läbi organisatsiooniüksuste, et pakkuda korrektset juhtimisülevaadet kõigi organisatsiooniüksuste ja -tasemete kohta.</span><span class="sxs-lookup"><span data-stu-id="24be3-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="24be3-136">See voog peab põhinema tarbimise või õiglase hindamise täpsel kirjendamisel.</span><span class="sxs-lookup"><span data-stu-id="24be3-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="24be3-137">Pearaamatus, saab elektrikulu sisestada nii, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="24be3-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="24be3-138">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="24be3-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="24be3-139">Kulukeskus</span><span class="sxs-lookup"><span data-stu-id="24be3-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="24be3-140">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="24be3-140">Main account</span></span></th>
<th><span data-ttu-id="24be3-141">Summa arvestusvaluutas</span><span class="sxs-lookup"><span data-stu-id="24be3-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-142">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="24be3-143">CC099</span><span class="sxs-lookup"><span data-stu-id="24be3-143">CC099</span></span></td>
<td><span data-ttu-id="24be3-144">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="24be3-144">Default cost center</span></span></td>
<td><span data-ttu-id="24be3-145">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-145">10001</span></span></td>
<td><span data-ttu-id="24be3-146">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-146">Electricity</span></span></td>
<td><span data-ttu-id="24be3-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="24be3-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="24be3-148">1. etapp: kulukäitumise arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="24be3-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="24be3-149">Vaikimisi saavad lähteandmetest imporditud kulukirjed kuluarvestuses kulukäitumise klassifikatsiooniks **Klassifitseerimata**.</span><span class="sxs-lookup"><span data-stu-id="24be3-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="24be3-150">Kulukäitumise poliitikareegleid rakendades saate kulukirjed ümber klassifitseerida kui **Fikseeritud kulu** või **Muutuvkulu**.</span><span class="sxs-lookup"><span data-stu-id="24be3-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="24be3-151">Kulukäitumise reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="24be3-151">Define the cost behavior rule</span></span>

<span data-ttu-id="24be3-152">Mõnikord on osa kulust fikseeritud tasu ja järelejäänud kulu põhineb tarbimisel.</span><span class="sxs-lookup"><span data-stu-id="24be3-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="24be3-153">Elektriarved vastavad sageli sellele määratlusele.</span><span class="sxs-lookup"><span data-stu-id="24be3-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="24be3-154">Pärast kindla fikseeritud tasu maksmist maksate tarbimise eest kilovatt-tunni (Kwh) kohta.</span><span class="sxs-lookup"><span data-stu-id="24be3-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="24be3-155">Näiteks kui fikseeritud kulu tasu on 1000,00 eurot, määratletakse kulukäitumise reegel järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="24be3-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="24be3-156">Fikseeritud summa: 1000,00</span><span class="sxs-lookup"><span data-stu-id="24be3-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="24be3-157">0 &lt;= 1000,00 = fikseeritud</span><span class="sxs-lookup"><span data-stu-id="24be3-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="24be3-158">1000,01 &lt; N = muutuja</span><span class="sxs-lookup"><span data-stu-id="24be3-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="24be3-159">Tööleht</span><span class="sxs-lookup"><span data-stu-id="24be3-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="24be3-160">Tööleht</span><span class="sxs-lookup"><span data-stu-id="24be3-160">Journal</span></span></th>
<th><span data-ttu-id="24be3-161">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="24be3-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="24be3-162">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="24be3-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="24be3-163">Versioon</span><span class="sxs-lookup"><span data-stu-id="24be3-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-164">00001</span><span class="sxs-lookup"><span data-stu-id="24be3-164">00001</span></span></td>
<td><span data-ttu-id="24be3-165">Kulukäitumise arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="24be3-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="24be3-166">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="24be3-166">Fiscal</span></span></td>
<td><span data-ttu-id="24be3-167">2017</span><span class="sxs-lookup"><span data-stu-id="24be3-167">2017</span></span></td>
<td><span data-ttu-id="24be3-168">Periood 1</span><span class="sxs-lookup"><span data-stu-id="24be3-168">Period 1</span></span></td>
<td><span data-ttu-id="24be3-169">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="24be3-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="24be3-170">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="24be3-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="24be3-171">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="24be3-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="24be3-172">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="24be3-173">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="24be3-173">Cost element</span></span></th>
<th><span data-ttu-id="24be3-174">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="24be3-174">Cost behavior</span></span></th>
<th><span data-ttu-id="24be3-175">Summa</span><span class="sxs-lookup"><span data-stu-id="24be3-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-176">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="24be3-177">CC099</span><span class="sxs-lookup"><span data-stu-id="24be3-177">CC099</span></span></td>
<td><span data-ttu-id="24be3-178">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="24be3-178">Default cost center</span></span></td>
<td><span data-ttu-id="24be3-179">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-179">10001</span></span></td>
<td><span data-ttu-id="24be3-180">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-180">Electricity</span></span></td>
<td><span data-ttu-id="24be3-181">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="24be3-181">Unclassified</span></span></td>
<td><span data-ttu-id="24be3-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="24be3-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="24be3-183">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="24be3-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-184">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="24be3-185">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="24be3-185">Cost element</span></span></th>
<th><span data-ttu-id="24be3-186">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="24be3-186">Cost behavior</span></span></th>
<th><span data-ttu-id="24be3-187">Summa</span><span class="sxs-lookup"><span data-stu-id="24be3-187">Amount</span></span></th>
<th><span data-ttu-id="24be3-188">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="24be3-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-189">CC099</span><span class="sxs-lookup"><span data-stu-id="24be3-189">CC099</span></span></td>
<td><span data-ttu-id="24be3-190">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="24be3-190">Default cost center</span></span></td>
<td><span data-ttu-id="24be3-191">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-191">10001</span></span></td>
<td><span data-ttu-id="24be3-192">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-192">Electricity</span></span></td>
<td><span data-ttu-id="24be3-193">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="24be3-193">Unclassified</span></span></td>
<td><span data-ttu-id="24be3-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="24be3-194">10,000.00</span></span></td>
<td><span data-ttu-id="24be3-195">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-196">CC099</span><span class="sxs-lookup"><span data-stu-id="24be3-196">CC099</span></span></td>
<td><span data-ttu-id="24be3-197">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="24be3-197">Default cost center</span></span></td>
<td><span data-ttu-id="24be3-198">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-198">10001</span></span></td>
<td><span data-ttu-id="24be3-199">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-199">Electricity</span></span></td>
<td><span data-ttu-id="24be3-200">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="24be3-200">Unclassified</span></span></td>
<td><span data-ttu-id="24be3-201">–10 000,00</span><span class="sxs-lookup"><span data-stu-id="24be3-201">-10,000.00</span></span></td>
<td><span data-ttu-id="24be3-202">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-203">CC099</span><span class="sxs-lookup"><span data-stu-id="24be3-203">CC099</span></span></td>
<td><span data-ttu-id="24be3-204">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="24be3-204">Default cost center</span></span></td>
<td><span data-ttu-id="24be3-205">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-205">10001</span></span></td>
<td><span data-ttu-id="24be3-206">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-206">Electricity</span></span></td>
<td><span data-ttu-id="24be3-207">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-207">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="24be3-208">1,000.00</span></span></td>
<td><span data-ttu-id="24be3-209">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-210">CC099</span><span class="sxs-lookup"><span data-stu-id="24be3-210">CC099</span></span></td>
<td><span data-ttu-id="24be3-211">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="24be3-211">Default cost center</span></span></td>
<td><span data-ttu-id="24be3-212">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-212">10001</span></span></td>
<td><span data-ttu-id="24be3-213">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-213">Electricity</span></span></td>
<td><span data-ttu-id="24be3-214">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-214">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="24be3-215">9,000.00</span></span></td>
<td><span data-ttu-id="24be3-216">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="24be3-217">Lisateavet vt teemast [Kulukäitumise poliitika loomine ja määramine kulujuhtimisüksusele (tegevuse juhis)](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="24be3-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="24be3-218">2. etapp: kulujaotuse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="24be3-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="24be3-219">Kulujaotust kasutatakse kulu ümberjaotamiseks ühelt kuluobjektilt ühele või mitmele teisele kuluobjektile, rakendades asjakohast eraldusalust.</span><span class="sxs-lookup"><span data-stu-id="24be3-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="24be3-220">Kulujaotus ja kulueraldus erinevad selle poolest, et kulujaotus toimub alati algse kulu esmase kuluelemendi tasemel.</span><span class="sxs-lookup"><span data-stu-id="24be3-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="24be3-221">Kulujaotuse reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="24be3-221">Define the cost distribution rule</span></span>

<span data-ttu-id="24be3-222">Finantsaruandluses registreeritakse elektrikulud sageli põhisummana.</span><span class="sxs-lookup"><span data-stu-id="24be3-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="24be3-223">Kuluarvestuseses ei ole see lähenemine piisavalt üksikasjalik.</span><span class="sxs-lookup"><span data-stu-id="24be3-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="24be3-224">Muutuvkulu tuleb jaotada üksikutele kuluobjektidele õigluse alusel.</span><span class="sxs-lookup"><span data-stu-id="24be3-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="24be3-225">Kõige loogilisem eraldamisalus on elektritarbimine (kWh).</span><span class="sxs-lookup"><span data-stu-id="24be3-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="24be3-226">Luuakse statistilise dimensiooni liige nimega Elekter ja elektritarbimine on kirjendatakse.</span><span class="sxs-lookup"><span data-stu-id="24be3-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="24be3-227">Vaikimisi muutuvad kõik statistilise dimensiooni liikmed eraldamisalusena kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="24be3-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-228">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-228">Cost object</span></span></th>
<th><span data-ttu-id="24be3-229">kWh</span><span class="sxs-lookup"><span data-stu-id="24be3-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-230">CC001</span><span class="sxs-lookup"><span data-stu-id="24be3-230">CC001</span></span></td>
<td><span data-ttu-id="24be3-231">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="24be3-231">HR</span></span></td>
<td><span data-ttu-id="24be3-232">1000</span><span class="sxs-lookup"><span data-stu-id="24be3-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-233">CC002</span><span class="sxs-lookup"><span data-stu-id="24be3-233">CC002</span></span></td>
<td><span data-ttu-id="24be3-234">Finantsid</span><span class="sxs-lookup"><span data-stu-id="24be3-234">Finance</span></span></td>
<td><span data-ttu-id="24be3-235">6,000</span><span class="sxs-lookup"><span data-stu-id="24be3-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-236">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-236">CC003</span></span></td>
<td><span data-ttu-id="24be3-237">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-237">Assembly</span></span></td>
<td><span data-ttu-id="24be3-238">0</span><span class="sxs-lookup"><span data-stu-id="24be3-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="24be3-239">Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="24be3-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-240">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-240">Cost object</span></span></th>
<th><span data-ttu-id="24be3-241">Väärtus</span><span class="sxs-lookup"><span data-stu-id="24be3-241">Magnitude</span></span></th>
<th><span data-ttu-id="24be3-242">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="24be3-242">Allocation factor</span></span></th>
<th><span data-ttu-id="24be3-243">Summa</span><span class="sxs-lookup"><span data-stu-id="24be3-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-244">CC001</span><span class="sxs-lookup"><span data-stu-id="24be3-244">CC001</span></span></td>
<td><span data-ttu-id="24be3-245">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="24be3-245">HR</span></span></td>
<td><span data-ttu-id="24be3-246">1000</span><span class="sxs-lookup"><span data-stu-id="24be3-246">1,000</span></span></td>
<td><span data-ttu-id="24be3-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="24be3-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="24be3-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="24be3-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-249">CC002</span><span class="sxs-lookup"><span data-stu-id="24be3-249">CC002</span></span></td>
<td><span data-ttu-id="24be3-250">Finantsid</span><span class="sxs-lookup"><span data-stu-id="24be3-250">Finance</span></span></td>
<td><span data-ttu-id="24be3-251">6,000</span><span class="sxs-lookup"><span data-stu-id="24be3-251">6,000</span></span></td>
<td><span data-ttu-id="24be3-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="24be3-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="24be3-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="24be3-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-254">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-254">CC003</span></span></td>
<td><span data-ttu-id="24be3-255">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-255">Assembly</span></span></td>
<td><span data-ttu-id="24be3-256">0</span><span class="sxs-lookup"><span data-stu-id="24be3-256">0</span></span></td>
<td><span data-ttu-id="24be3-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="24be3-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="24be3-258">0,00</span><span class="sxs-lookup"><span data-stu-id="24be3-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="24be3-259">Fikseeritud kulu tuleb jaotada ühtlaselt üksikutele kuluobjektidele, mis on tarbinud elektrit.</span><span class="sxs-lookup"><span data-stu-id="24be3-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="24be3-260">Selle tulemuse saate, kasutades valemi eraldamisaluses statistilise dimensiooni liiget Elekter: (Elekter &gt; 0,00). Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="24be3-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-261">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-261">Cost object</span></span></th>
<th><span data-ttu-id="24be3-262">Valem</span><span class="sxs-lookup"><span data-stu-id="24be3-262">Formula</span></span></th>
<th><span data-ttu-id="24be3-263">Väärtus</span><span class="sxs-lookup"><span data-stu-id="24be3-263">Magnitude</span></span></th>
<th><span data-ttu-id="24be3-264">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="24be3-264">Allocation factor</span></span></th>
<th><span data-ttu-id="24be3-265">Summa</span><span class="sxs-lookup"><span data-stu-id="24be3-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-266">CC001</span><span class="sxs-lookup"><span data-stu-id="24be3-266">CC001</span></span></td>
<td><span data-ttu-id="24be3-267">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="24be3-267">HR</span></span></td>
<td><span data-ttu-id="24be3-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="24be3-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="24be3-269">1</span><span class="sxs-lookup"><span data-stu-id="24be3-269">1</span></span></td>
<td><span data-ttu-id="24be3-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="24be3-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="24be3-271">500,00</span><span class="sxs-lookup"><span data-stu-id="24be3-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-272">CC002</span><span class="sxs-lookup"><span data-stu-id="24be3-272">CC002</span></span></td>
<td><span data-ttu-id="24be3-273">Finantsid</span><span class="sxs-lookup"><span data-stu-id="24be3-273">Finance</span></span></td>
<td><span data-ttu-id="24be3-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="24be3-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="24be3-275">1</span><span class="sxs-lookup"><span data-stu-id="24be3-275">1</span></span></td>
<td><span data-ttu-id="24be3-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="24be3-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="24be3-277">500,00</span><span class="sxs-lookup"><span data-stu-id="24be3-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-278">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-278">CC003</span></span></td>
<td><span data-ttu-id="24be3-279">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-279">Assembly</span></span></td>
<td><span data-ttu-id="24be3-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="24be3-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="24be3-281">0</span><span class="sxs-lookup"><span data-stu-id="24be3-281">0</span></span></td>
<td><span data-ttu-id="24be3-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="24be3-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="24be3-283">0,00</span><span class="sxs-lookup"><span data-stu-id="24be3-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="24be3-284">Tööleht</span><span class="sxs-lookup"><span data-stu-id="24be3-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="24be3-285">Tööleht</span><span class="sxs-lookup"><span data-stu-id="24be3-285">Journal</span></span></th>
<th><span data-ttu-id="24be3-286">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="24be3-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="24be3-287">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="24be3-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="24be3-288">Versioon</span><span class="sxs-lookup"><span data-stu-id="24be3-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-289">00002</span><span class="sxs-lookup"><span data-stu-id="24be3-289">00002</span></span></td>
<td><span data-ttu-id="24be3-290">Kulujaotuse arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="24be3-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="24be3-291">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="24be3-291">Fiscal</span></span></td>
<td><span data-ttu-id="24be3-292">2017</span><span class="sxs-lookup"><span data-stu-id="24be3-292">2017</span></span></td>
<td><span data-ttu-id="24be3-293">Periood 1</span><span class="sxs-lookup"><span data-stu-id="24be3-293">Period 1</span></span></td>
<td><span data-ttu-id="24be3-294">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="24be3-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="24be3-295">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="24be3-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="24be3-296">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="24be3-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="24be3-297">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="24be3-298">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="24be3-298">Cost element</span></span></th>
<th><span data-ttu-id="24be3-299">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="24be3-299">Cost behavior</span></span></th>
<th><span data-ttu-id="24be3-300">Summa</span><span class="sxs-lookup"><span data-stu-id="24be3-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-301">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="24be3-302">CC099</span><span class="sxs-lookup"><span data-stu-id="24be3-302">CC099</span></span></td>
<td><span data-ttu-id="24be3-303">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="24be3-303">Default cost center</span></span></td>
<td><span data-ttu-id="24be3-304">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-304">10001</span></span></td>
<td><span data-ttu-id="24be3-305">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-305">Electricity</span></span></td>
<td><span data-ttu-id="24be3-306">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-306">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="24be3-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-308">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="24be3-309">CC099</span><span class="sxs-lookup"><span data-stu-id="24be3-309">CC099</span></span></td>
<td><span data-ttu-id="24be3-310">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="24be3-310">Default cost center</span></span></td>
<td><span data-ttu-id="24be3-311">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-311">10001</span></span></td>
<td><span data-ttu-id="24be3-312">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-312">Electricity</span></span></td>
<td><span data-ttu-id="24be3-313">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-313">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="24be3-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="24be3-315">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="24be3-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-316">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="24be3-317">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="24be3-317">Cost element</span></span></th>
<th><span data-ttu-id="24be3-318">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="24be3-318">Cost behavior</span></span></th>
<th><span data-ttu-id="24be3-319">Summa</span><span class="sxs-lookup"><span data-stu-id="24be3-319">Amount</span></span></th>
<th><span data-ttu-id="24be3-320">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="24be3-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-321">CC099</span><span class="sxs-lookup"><span data-stu-id="24be3-321">CC099</span></span></td>
<td><span data-ttu-id="24be3-322">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="24be3-322">Default cost center</span></span></td>
<td><span data-ttu-id="24be3-323">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-323">10001</span></span></td>
<td><span data-ttu-id="24be3-324">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-324">Electricity</span></span></td>
<td><span data-ttu-id="24be3-325">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-325">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-326">–1000,00</span><span class="sxs-lookup"><span data-stu-id="24be3-326">-1,000.00</span></span></td>
<td><span data-ttu-id="24be3-327">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-328">CC001</span><span class="sxs-lookup"><span data-stu-id="24be3-328">CC001</span></span></td>
<td><span data-ttu-id="24be3-329">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="24be3-329">HR</span></span></td>
<td><span data-ttu-id="24be3-330">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-330">10001</span></span></td>
<td><span data-ttu-id="24be3-331">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-331">Electricity</span></span></td>
<td><span data-ttu-id="24be3-332">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-332">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-333">500,00</span><span class="sxs-lookup"><span data-stu-id="24be3-333">500.00</span></span></td>
<td><span data-ttu-id="24be3-334">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-335">CC002</span><span class="sxs-lookup"><span data-stu-id="24be3-335">CC002</span></span></td>
<td><span data-ttu-id="24be3-336">Finantsid</span><span class="sxs-lookup"><span data-stu-id="24be3-336">Finance</span></span></td>
<td><span data-ttu-id="24be3-337">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-337">10001</span></span></td>
<td><span data-ttu-id="24be3-338">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-338">Electricity</span></span></td>
<td><span data-ttu-id="24be3-339">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-339">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-340">500,00</span><span class="sxs-lookup"><span data-stu-id="24be3-340">500.00</span></span></td>
<td><span data-ttu-id="24be3-341">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-342">CC099</span><span class="sxs-lookup"><span data-stu-id="24be3-342">CC099</span></span></td>
<td><span data-ttu-id="24be3-343">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="24be3-343">Default cost center</span></span></td>
<td><span data-ttu-id="24be3-344">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-344">10001</span></span></td>
<td><span data-ttu-id="24be3-345">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-345">Electricity</span></span></td>
<td><span data-ttu-id="24be3-346">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-346">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-347">–9000,00</span><span class="sxs-lookup"><span data-stu-id="24be3-347">-9,000.00</span></span></td>
<td><span data-ttu-id="24be3-348">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-349">CC001</span><span class="sxs-lookup"><span data-stu-id="24be3-349">CC001</span></span></td>
<td><span data-ttu-id="24be3-350">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="24be3-350">HR</span></span></td>
<td><span data-ttu-id="24be3-351">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-351">10001</span></span></td>
<td><span data-ttu-id="24be3-352">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-352">Electricity</span></span></td>
<td><span data-ttu-id="24be3-353">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-353">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="24be3-354">1,285.71</span></span></td>
<td><span data-ttu-id="24be3-355">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-356">CC002</span><span class="sxs-lookup"><span data-stu-id="24be3-356">CC002</span></span></td>
<td><span data-ttu-id="24be3-357">Finantsid</span><span class="sxs-lookup"><span data-stu-id="24be3-357">Finance</span></span></td>
<td><span data-ttu-id="24be3-358">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-358">10001</span></span></td>
<td><span data-ttu-id="24be3-359">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-359">Electricity</span></span></td>
<td><span data-ttu-id="24be3-360">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-360">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="24be3-361">7,714.29</span></span></td>
<td><span data-ttu-id="24be3-362">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="24be3-363">Lisateavet vt teemast [Kulujaotise poliitika loomine ja määramine kulujuhtimisüksusele (tegevuse juhis)](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="24be3-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="24be3-364">3. etapp: üldkulude määra arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="24be3-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="24be3-365">Üldkulude määra kasutatakse ühe või mitme kindla kuluobjekti debiteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="24be3-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="24be3-366">Tasu põhineb eelmääratud kulumääral ja väärtusel määratud eraldamisalusest.</span><span class="sxs-lookup"><span data-stu-id="24be3-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="24be3-367">Üldkulu määra määratlemine</span><span class="sxs-lookup"><span data-stu-id="24be3-367">Define the overhead rate</span></span>

<span data-ttu-id="24be3-368">Kuluobjekt CC001 inimressursid panustab sisemiste projektide kogumisse.</span><span class="sxs-lookup"><span data-stu-id="24be3-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="24be3-369">Luuakse statistilise dimensiooni liige nimega Inimressursside projektid, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="24be3-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-370">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-370">Cost object</span></span></th>
<th><span data-ttu-id="24be3-371">Tunnid</span><span class="sxs-lookup"><span data-stu-id="24be3-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-372">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="24be3-372">Proj 1</span></span></td>
<td><span data-ttu-id="24be3-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="24be3-373">Project 1</span></span></td>
<td><span data-ttu-id="24be3-374">3</span><span class="sxs-lookup"><span data-stu-id="24be3-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-375">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="24be3-375">Proj 2</span></span></td>
<td><span data-ttu-id="24be3-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="24be3-376">Project 2</span></span></td>
<td><span data-ttu-id="24be3-377">1</span><span class="sxs-lookup"><span data-stu-id="24be3-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="24be3-378">Määratletud on eelmääratud kulumäär kuluprojektide panusele.</span><span class="sxs-lookup"><span data-stu-id="24be3-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-379">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-379">Cost object</span></span></th>
<th><span data-ttu-id="24be3-380">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="24be3-380">Cost element</span></span></th>
<th><span data-ttu-id="24be3-381">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="24be3-381">Cost behavior</span></span></th>
<th><span data-ttu-id="24be3-382">Ühikud</span><span class="sxs-lookup"><span data-stu-id="24be3-382">Units</span></span></th>
<th><span data-ttu-id="24be3-383">Kurss</span><span class="sxs-lookup"><span data-stu-id="24be3-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-384">CC001</span><span class="sxs-lookup"><span data-stu-id="24be3-384">CC001</span></span></td>
<td><span data-ttu-id="24be3-385">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="24be3-385">HR</span></span></td>
<td><span data-ttu-id="24be3-386">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-386">10001</span></span></td>
<td><span data-ttu-id="24be3-387">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-387">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-388">1</span><span class="sxs-lookup"><span data-stu-id="24be3-388">1</span></span></td>
<td><span data-ttu-id="24be3-389">10</span><span class="sxs-lookup"><span data-stu-id="24be3-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="24be3-390">Järgmises tabelis on näidatud tulemus, kui inimressursside projektid on rakendatud eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="24be3-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-391">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-391">Cost object</span></span></th>
<th><span data-ttu-id="24be3-392">Väärtus</span><span class="sxs-lookup"><span data-stu-id="24be3-392">Magnitude</span></span></th>
<th><span data-ttu-id="24be3-393">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="24be3-393">Cost element</span></span></th>
<th><span data-ttu-id="24be3-394">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="24be3-394">Allocation factor</span></span></th>
<th><span data-ttu-id="24be3-395">Summa</span><span class="sxs-lookup"><span data-stu-id="24be3-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-396">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="24be3-396">Proj 1</span></span></td>
<td><span data-ttu-id="24be3-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="24be3-397">Project 1</span></span></td>
<td><span data-ttu-id="24be3-398">3</span><span class="sxs-lookup"><span data-stu-id="24be3-398">3</span></span></td>
<td><span data-ttu-id="24be3-399">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-399">10001</span></span></td>
<td><span data-ttu-id="24be3-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="24be3-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="24be3-401">30,00</span><span class="sxs-lookup"><span data-stu-id="24be3-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-402">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="24be3-402">Proj 2</span></span></td>
<td><span data-ttu-id="24be3-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="24be3-403">Project 2</span></span></td>
<td><span data-ttu-id="24be3-404">1</span><span class="sxs-lookup"><span data-stu-id="24be3-404">1</span></span></td>
<td><span data-ttu-id="24be3-405">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-405">10001</span></span></td>
<td><span data-ttu-id="24be3-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="24be3-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="24be3-407">10,00</span><span class="sxs-lookup"><span data-stu-id="24be3-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="24be3-408">Tööleht</span><span class="sxs-lookup"><span data-stu-id="24be3-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="24be3-409">Tööleht</span><span class="sxs-lookup"><span data-stu-id="24be3-409">Journal</span></span></th>
<th><span data-ttu-id="24be3-410">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="24be3-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="24be3-411">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="24be3-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="24be3-412">Versioon</span><span class="sxs-lookup"><span data-stu-id="24be3-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-413">00003</span><span class="sxs-lookup"><span data-stu-id="24be3-413">00003</span></span></td>
<td><span data-ttu-id="24be3-414">Üldkulu määra arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="24be3-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="24be3-415">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="24be3-415">Fiscal</span></span></td>
<td><span data-ttu-id="24be3-416">2017</span><span class="sxs-lookup"><span data-stu-id="24be3-416">2017</span></span></td>
<td><span data-ttu-id="24be3-417">Periood 1</span><span class="sxs-lookup"><span data-stu-id="24be3-417">Period 1</span></span></td>
<td><span data-ttu-id="24be3-418">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="24be3-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="24be3-419">Töölehe sisestused (töölehe sisestused üldkulu määra arvutamiseks)</span><span class="sxs-lookup"><span data-stu-id="24be3-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="24be3-420">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="24be3-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="24be3-421">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-421">Cost object</span></span></th>
<th><span data-ttu-id="24be3-422">Väärtus</span><span class="sxs-lookup"><span data-stu-id="24be3-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-423">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="24be3-424">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="24be3-424">Proj 1</span></span></td>
<td><span data-ttu-id="24be3-425">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="24be3-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="24be3-426">3,00</span><span class="sxs-lookup"><span data-stu-id="24be3-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-427">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="24be3-428">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="24be3-428">Proj 2</span></span></td>
<td><span data-ttu-id="24be3-429">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="24be3-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="24be3-430">1,00</span><span class="sxs-lookup"><span data-stu-id="24be3-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="24be3-431">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="24be3-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-432">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="24be3-433">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="24be3-433">Cost element</span></span></th>
<th><span data-ttu-id="24be3-434">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="24be3-434">Cost behavior</span></span></th>
<th><span data-ttu-id="24be3-435">Summa</span><span class="sxs-lookup"><span data-stu-id="24be3-435">Amount</span></span></th>
<th><span data-ttu-id="24be3-436">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="24be3-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="24be3-437">CC0001</span></span></td>
<td><span data-ttu-id="24be3-438">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="24be3-438">HR</span></span></td>
<td><span data-ttu-id="24be3-439">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-439">10001</span></span></td>
<td><span data-ttu-id="24be3-440">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-440">Electricity</span></span></td>
<td><span data-ttu-id="24be3-441">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-441">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-442">–30,00</span><span class="sxs-lookup"><span data-stu-id="24be3-442">-30.00</span></span></td>
<td><span data-ttu-id="24be3-443">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-444">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="24be3-444">Proj 1</span></span></td>
<td><span data-ttu-id="24be3-445">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="24be3-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="24be3-446">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-446">10001</span></span></td>
<td><span data-ttu-id="24be3-447">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-447">Electricity</span></span></td>
<td><span data-ttu-id="24be3-448">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-448">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-449">30,00</span><span class="sxs-lookup"><span data-stu-id="24be3-449">30.00</span></span></td>
<td><span data-ttu-id="24be3-450">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-451">CC001</span><span class="sxs-lookup"><span data-stu-id="24be3-451">CC001</span></span></td>
<td><span data-ttu-id="24be3-452">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="24be3-452">HR</span></span></td>
<td><span data-ttu-id="24be3-453">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-453">10001</span></span></td>
<td><span data-ttu-id="24be3-454">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-454">Electricity</span></span></td>
<td><span data-ttu-id="24be3-455">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-455">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="24be3-456">-10.00</span></span></td>
<td><span data-ttu-id="24be3-457">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-458">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="24be3-458">Proj 2</span></span></td>
<td><span data-ttu-id="24be3-459">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="24be3-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="24be3-460">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-460">10001</span></span></td>
<td><span data-ttu-id="24be3-461">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-461">Electricity</span></span></td>
<td><span data-ttu-id="24be3-462">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-462">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-463">10.00</span><span class="sxs-lookup"><span data-stu-id="24be3-463">10.00</span></span></td>
<td><span data-ttu-id="24be3-464">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="24be3-465">Lisateavet vt teemast [Üldkulude arvutamine](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="24be3-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="24be3-466">4. etapp: kulueralduse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="24be3-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="24be3-467">Eraldamist kasutatakse kuluobjekti saldo eraldamiseks teistele kuluobjektidele, rakendades eraldamisalust.</span><span class="sxs-lookup"><span data-stu-id="24be3-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="24be3-468">Finance toetab vastastikuse eraldamise meetodit.</span><span class="sxs-lookup"><span data-stu-id="24be3-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="24be3-469">Vastastikuse eraldamise meetodi puhul tuvastatakse täiendavate kuluobjektide vahetatavad vastastikused teenused.</span><span class="sxs-lookup"><span data-stu-id="24be3-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="24be3-470">Süsteem määrab automaatselt eraldamiste tegemise õige järjekorra.</span><span class="sxs-lookup"><span data-stu-id="24be3-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="24be3-471">Kuluobjekti saldo eraldatakse üksiku eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="24be3-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="24be3-472">Toetatakse eraldamisi kuluobjektide dimensioonide ja nende vastavate liikmete seas.</span><span class="sxs-lookup"><span data-stu-id="24be3-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="24be3-473">Eraldamisjärjekorda reguleerib kulujuhtseade.</span><span class="sxs-lookup"><span data-stu-id="24be3-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="24be3-474">[![Vastastikune meetod](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="24be3-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="24be3-475">Kulueraldamise määratlemine</span><span class="sxs-lookup"><span data-stu-id="24be3-475">Define the cost allocation</span></span>

<span data-ttu-id="24be3-476">Siin on lihtne näide, mis selgitab, kuidas jälgida kulu liikumist.</span><span class="sxs-lookup"><span data-stu-id="24be3-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="24be3-477">Kuluobjekt CC001 inimressursid panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="24be3-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="24be3-478">Luuakse statistilise dimensiooni liige nimega Inimressursside teenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="24be3-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-479">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-479">Cost object</span></span></th>
<th><span data-ttu-id="24be3-480">Inimressursside teenused</span><span class="sxs-lookup"><span data-stu-id="24be3-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-481">CC002</span><span class="sxs-lookup"><span data-stu-id="24be3-481">CC002</span></span></td>
<td><span data-ttu-id="24be3-482">Finantsid</span><span class="sxs-lookup"><span data-stu-id="24be3-482">Finance</span></span></td>
<td><span data-ttu-id="24be3-483">35</span><span class="sxs-lookup"><span data-stu-id="24be3-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-484">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-484">CC003</span></span></td>
<td><span data-ttu-id="24be3-485">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-485">Assembly</span></span></td>
<td><span data-ttu-id="24be3-486">55</span><span class="sxs-lookup"><span data-stu-id="24be3-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-487">CC004</span><span class="sxs-lookup"><span data-stu-id="24be3-487">CC004</span></span></td>
<td><span data-ttu-id="24be3-488">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="24be3-488">Packaging</span></span></td>
<td><span data-ttu-id="24be3-489">10</span><span class="sxs-lookup"><span data-stu-id="24be3-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="24be3-490">Kuluobjekt CC002 rahandus panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="24be3-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="24be3-491">Luuakse statistilise dimensiooni liige nimega Rahandusteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="24be3-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-492">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-492">Cost object</span></span></th>
<th><span data-ttu-id="24be3-493">Rahandusteenused</span><span class="sxs-lookup"><span data-stu-id="24be3-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-494">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-494">CC003</span></span></td>
<td><span data-ttu-id="24be3-495">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-495">Assembly</span></span></td>
<td><span data-ttu-id="24be3-496">65</span><span class="sxs-lookup"><span data-stu-id="24be3-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-497">CC004</span><span class="sxs-lookup"><span data-stu-id="24be3-497">CC004</span></span></td>
<td><span data-ttu-id="24be3-498">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="24be3-498">Packaging</span></span></td>
<td><span data-ttu-id="24be3-499">35</span><span class="sxs-lookup"><span data-stu-id="24be3-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="24be3-500">Kuluobjekt CC003 assembler panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="24be3-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="24be3-501">Luuakse statistilise dimensiooni liige nimega Assembleriteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="24be3-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-502">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-502">Cost object</span></span></th>
<th><span data-ttu-id="24be3-503">Assembleriteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="24be3-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-504">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="24be3-504">Prod 1</span></span></td>
<td><span data-ttu-id="24be3-505">Toode 1</span><span class="sxs-lookup"><span data-stu-id="24be3-505">Product 1</span></span></td>
<td><span data-ttu-id="24be3-506">60</span><span class="sxs-lookup"><span data-stu-id="24be3-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-507">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-507">Prod 2</span></span></td>
<td><span data-ttu-id="24be3-508">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-508">Product 2</span></span></td>
<td><span data-ttu-id="24be3-509">20</span><span class="sxs-lookup"><span data-stu-id="24be3-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="24be3-510">Kuluobjekt CC004 pakendamine panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="24be3-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="24be3-511">Luuakse statistilise dimensiooni liige nimega Pakendamisteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="24be3-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-512">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-512">Cost object</span></span></th>
<th><span data-ttu-id="24be3-513">Pakendamisteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="24be3-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-514">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="24be3-514">Prod 1</span></span></td>
<td><span data-ttu-id="24be3-515">Toode 1</span><span class="sxs-lookup"><span data-stu-id="24be3-515">Product 1</span></span></td>
<td><span data-ttu-id="24be3-516">80</span><span class="sxs-lookup"><span data-stu-id="24be3-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-517">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-517">Prod 2</span></span></td>
<td><span data-ttu-id="24be3-518">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-518">Product 2</span></span></td>
<td><span data-ttu-id="24be3-519">15</span><span class="sxs-lookup"><span data-stu-id="24be3-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="24be3-520">Statistilised mõõdud, nagu toote tarbitud tootmistunnid, saab tuletada lähteandmetest.</span><span class="sxs-lookup"><span data-stu-id="24be3-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="24be3-521">Lisateavet vt teemast [Statistiliste mõõtude pakkuja mall](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="24be3-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="24be3-522">Järgmises tabelis on näidatud tulemus, kui HR-teenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="24be3-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-523">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-523">Cost object</span></span></th>
<th><span data-ttu-id="24be3-524">Väärtus</span><span class="sxs-lookup"><span data-stu-id="24be3-524">Magnitude</span></span></th>
<th><span data-ttu-id="24be3-525">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="24be3-525">Allocation factor</span></span></th>
<th><span data-ttu-id="24be3-526">Summa</span><span class="sxs-lookup"><span data-stu-id="24be3-526">Amount</span></span></th>
<th><span data-ttu-id="24be3-527">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="24be3-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-528">CC002</span><span class="sxs-lookup"><span data-stu-id="24be3-528">CC002</span></span></td>
<td><span data-ttu-id="24be3-529">Finantsid</span><span class="sxs-lookup"><span data-stu-id="24be3-529">Finance</span></span></td>
<td><span data-ttu-id="24be3-530">35</span><span class="sxs-lookup"><span data-stu-id="24be3-530">35</span></span></td>
<td><span data-ttu-id="24be3-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="24be3-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="24be3-532">175.00</span><span class="sxs-lookup"><span data-stu-id="24be3-532">175.00</span></span></td>
<td><span data-ttu-id="24be3-533">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-534">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-534">CC003</span></span></td>
<td><span data-ttu-id="24be3-535">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-535">Assembly</span></span></td>
<td><span data-ttu-id="24be3-536">55</span><span class="sxs-lookup"><span data-stu-id="24be3-536">55</span></span></td>
<td><span data-ttu-id="24be3-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="24be3-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="24be3-538">275.00</span><span class="sxs-lookup"><span data-stu-id="24be3-538">275.00</span></span></td>
<td><span data-ttu-id="24be3-539">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-540">CC004</span><span class="sxs-lookup"><span data-stu-id="24be3-540">CC004</span></span></td>
<td><span data-ttu-id="24be3-541">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="24be3-541">Packaging</span></span></td>
<td><span data-ttu-id="24be3-542">10</span><span class="sxs-lookup"><span data-stu-id="24be3-542">10</span></span></td>
<td><span data-ttu-id="24be3-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="24be3-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="24be3-544">50,00</span><span class="sxs-lookup"><span data-stu-id="24be3-544">50.00</span></span></td>
<td><span data-ttu-id="24be3-545">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-546">CC002</span><span class="sxs-lookup"><span data-stu-id="24be3-546">CC002</span></span></td>
<td><span data-ttu-id="24be3-547">Finantsid</span><span class="sxs-lookup"><span data-stu-id="24be3-547">Finance</span></span></td>
<td><span data-ttu-id="24be3-548">35</span><span class="sxs-lookup"><span data-stu-id="24be3-548">35</span></span></td>
<td><span data-ttu-id="24be3-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="24be3-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="24be3-550">436.00</span><span class="sxs-lookup"><span data-stu-id="24be3-550">436.00</span></span></td>
<td><span data-ttu-id="24be3-551">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-552">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-552">CC003</span></span></td>
<td><span data-ttu-id="24be3-553">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-553">Assembly</span></span></td>
<td><span data-ttu-id="24be3-554">55</span><span class="sxs-lookup"><span data-stu-id="24be3-554">55</span></span></td>
<td><span data-ttu-id="24be3-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="24be3-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="24be3-556">685.14</span><span class="sxs-lookup"><span data-stu-id="24be3-556">685.14</span></span></td>
<td><span data-ttu-id="24be3-557">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-558">CC004</span><span class="sxs-lookup"><span data-stu-id="24be3-558">CC004</span></span></td>
<td><span data-ttu-id="24be3-559">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="24be3-559">Packaging</span></span></td>
<td><span data-ttu-id="24be3-560">10</span><span class="sxs-lookup"><span data-stu-id="24be3-560">10</span></span></td>
<td><span data-ttu-id="24be3-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="24be3-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="24be3-562">124.57</span><span class="sxs-lookup"><span data-stu-id="24be3-562">124.57</span></span></td>
<td><span data-ttu-id="24be3-563">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="24be3-564">Järgmises tabelis on näidatud tulemus, kui Rahandusteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="24be3-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-565">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-565">Cost object</span></span></th>
<th><span data-ttu-id="24be3-566">Väärtus</span><span class="sxs-lookup"><span data-stu-id="24be3-566">Magnitude</span></span></th>
<th><span data-ttu-id="24be3-567">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="24be3-567">Allocation factor</span></span></th>
<th><span data-ttu-id="24be3-568">Summa</span><span class="sxs-lookup"><span data-stu-id="24be3-568">Amount</span></span></th>
<th><span data-ttu-id="24be3-569">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="24be3-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-570">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-570">CC003</span></span></td>
<td><span data-ttu-id="24be3-571">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-571">Assembly</span></span></td>
<td><span data-ttu-id="24be3-572">65</span><span class="sxs-lookup"><span data-stu-id="24be3-572">65</span></span></td>
<td><span data-ttu-id="24be3-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="24be3-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="24be3-574">438.75</span><span class="sxs-lookup"><span data-stu-id="24be3-574">438.75</span></span></td>
<td><span data-ttu-id="24be3-575">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-576">CC004</span><span class="sxs-lookup"><span data-stu-id="24be3-576">CC004</span></span></td>
<td><span data-ttu-id="24be3-577">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="24be3-577">Packaging</span></span></td>
<td><span data-ttu-id="24be3-578">35</span><span class="sxs-lookup"><span data-stu-id="24be3-578">35</span></span></td>
<td><span data-ttu-id="24be3-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="24be3-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="24be3-580">236.25</span><span class="sxs-lookup"><span data-stu-id="24be3-580">236.25</span></span></td>
<td><span data-ttu-id="24be3-581">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-582">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-582">CC003</span></span></td>
<td><span data-ttu-id="24be3-583">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-583">Assembly</span></span></td>
<td><span data-ttu-id="24be3-584">65</span><span class="sxs-lookup"><span data-stu-id="24be3-584">65</span></span></td>
<td><span data-ttu-id="24be3-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="24be3-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="24be3-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="24be3-586">5,297.69</span></span></td>
<td><span data-ttu-id="24be3-587">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-588">CC004</span><span class="sxs-lookup"><span data-stu-id="24be3-588">CC004</span></span></td>
<td><span data-ttu-id="24be3-589">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="24be3-589">Packaging</span></span></td>
<td><span data-ttu-id="24be3-590">35</span><span class="sxs-lookup"><span data-stu-id="24be3-590">35</span></span></td>
<td><span data-ttu-id="24be3-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="24be3-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="24be3-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="24be3-592">2,852.60</span></span></td>
<td><span data-ttu-id="24be3-593">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="24be3-594">Järgmises tabelis on näidatud tulemus, kui Assembleriteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="24be3-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-595">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-595">Cost object</span></span></th>
<th><span data-ttu-id="24be3-596">Väärtus</span><span class="sxs-lookup"><span data-stu-id="24be3-596">Magnitude</span></span></th>
<th><span data-ttu-id="24be3-597">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="24be3-597">Allocation factor</span></span></th>
<th><span data-ttu-id="24be3-598">Summa</span><span class="sxs-lookup"><span data-stu-id="24be3-598">Amount</span></span></th>
<th><span data-ttu-id="24be3-599">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="24be3-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-600">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="24be3-600">Prod 1</span></span></td>
<td><span data-ttu-id="24be3-601">Toode 1</span><span class="sxs-lookup"><span data-stu-id="24be3-601">Product 1</span></span></td>
<td><span data-ttu-id="24be3-602">60</span><span class="sxs-lookup"><span data-stu-id="24be3-602">60</span></span></td>
<td><span data-ttu-id="24be3-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="24be3-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="24be3-604">535.31</span><span class="sxs-lookup"><span data-stu-id="24be3-604">535.31</span></span></td>
<td><span data-ttu-id="24be3-605">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-606">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-606">Prod 2</span></span></td>
<td><span data-ttu-id="24be3-607">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-607">Product 2</span></span></td>
<td><span data-ttu-id="24be3-608">20</span><span class="sxs-lookup"><span data-stu-id="24be3-608">20</span></span></td>
<td><span data-ttu-id="24be3-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="24be3-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="24be3-610">178.44</span><span class="sxs-lookup"><span data-stu-id="24be3-610">178.44</span></span></td>
<td><span data-ttu-id="24be3-611">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-612">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="24be3-612">Prod 1</span></span></td>
<td><span data-ttu-id="24be3-613">Toode 1</span><span class="sxs-lookup"><span data-stu-id="24be3-613">Product 1</span></span></td>
<td><span data-ttu-id="24be3-614">60</span><span class="sxs-lookup"><span data-stu-id="24be3-614">60</span></span></td>
<td><span data-ttu-id="24be3-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="24be3-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="24be3-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="24be3-616">4,487.12</span></span></td>
<td><span data-ttu-id="24be3-617">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-618">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-618">Prod 2</span></span></td>
<td><span data-ttu-id="24be3-619">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-619">Product 2</span></span></td>
<td><span data-ttu-id="24be3-620">20</span><span class="sxs-lookup"><span data-stu-id="24be3-620">20</span></span></td>
<td><span data-ttu-id="24be3-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="24be3-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="24be3-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="24be3-622">1,495.71</span></span></td>
<td><span data-ttu-id="24be3-623">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="24be3-624">Järgmises tabelis on näidatud tulemus, kui Pakendamisteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="24be3-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-625">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-625">Cost object</span></span></th>
<th><span data-ttu-id="24be3-626">Väärtus</span><span class="sxs-lookup"><span data-stu-id="24be3-626">Magnitude</span></span></th>
<th><span data-ttu-id="24be3-627">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="24be3-627">Allocation factor</span></span></th>
<th><span data-ttu-id="24be3-628">Summa</span><span class="sxs-lookup"><span data-stu-id="24be3-628">Amount</span></span></th>
<th><span data-ttu-id="24be3-629">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="24be3-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-630">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="24be3-630">Prod 1</span></span></td>
<td><span data-ttu-id="24be3-631">Toode 1</span><span class="sxs-lookup"><span data-stu-id="24be3-631">Product 1</span></span></td>
<td><span data-ttu-id="24be3-632">80</span><span class="sxs-lookup"><span data-stu-id="24be3-632">80</span></span></td>
<td><span data-ttu-id="24be3-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="24be3-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="24be3-634">241.05</span><span class="sxs-lookup"><span data-stu-id="24be3-634">241.05</span></span></td>
<td><span data-ttu-id="24be3-635">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-636">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-636">Prod 2</span></span></td>
<td><span data-ttu-id="24be3-637">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-637">Product 2</span></span></td>
<td><span data-ttu-id="24be3-638">15</span><span class="sxs-lookup"><span data-stu-id="24be3-638">15</span></span></td>
<td><span data-ttu-id="24be3-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="24be3-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="24be3-640">45.20</span><span class="sxs-lookup"><span data-stu-id="24be3-640">45.20</span></span></td>
<td><span data-ttu-id="24be3-641">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-642">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="24be3-642">Prod 1</span></span></td>
<td><span data-ttu-id="24be3-643">Toode 1</span><span class="sxs-lookup"><span data-stu-id="24be3-643">Product 1</span></span></td>
<td><span data-ttu-id="24be3-644">80</span><span class="sxs-lookup"><span data-stu-id="24be3-644">80</span></span></td>
<td><span data-ttu-id="24be3-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="24be3-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="24be3-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="24be3-646">2,507.09</span></span></td>
<td><span data-ttu-id="24be3-647">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-648">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-648">Prod 2</span></span></td>
<td><span data-ttu-id="24be3-649">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-649">Product 2</span></span></td>
<td><span data-ttu-id="24be3-650">15</span><span class="sxs-lookup"><span data-stu-id="24be3-650">15</span></span></td>
<td><span data-ttu-id="24be3-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="24be3-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="24be3-652">470.08</span><span class="sxs-lookup"><span data-stu-id="24be3-652">470.08</span></span></td>
<td><span data-ttu-id="24be3-653">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="24be3-654">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="24be3-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="24be3-655">Tööleht</span><span class="sxs-lookup"><span data-stu-id="24be3-655">Journal</span></span></th>
<th><span data-ttu-id="24be3-656">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="24be3-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="24be3-657">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="24be3-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="24be3-658">Versioon</span><span class="sxs-lookup"><span data-stu-id="24be3-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-659">00004</span><span class="sxs-lookup"><span data-stu-id="24be3-659">00004</span></span></td>
<td><span data-ttu-id="24be3-660">Kulueralduse tööleht</span><span class="sxs-lookup"><span data-stu-id="24be3-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="24be3-661">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="24be3-661">Fiscal</span></span></td>
<td><span data-ttu-id="24be3-662">2017</span><span class="sxs-lookup"><span data-stu-id="24be3-662">2017</span></span></td>
<td><span data-ttu-id="24be3-663">Periood 1</span><span class="sxs-lookup"><span data-stu-id="24be3-663">Period 1</span></span></td>
<td><span data-ttu-id="24be3-664">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="24be3-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="24be3-665">Töölehe read</span><span class="sxs-lookup"><span data-stu-id="24be3-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="24be3-666">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="24be3-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="24be3-667">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="24be3-668">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="24be3-668">Cost element</span></span></th>
<th><span data-ttu-id="24be3-669">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="24be3-669">Cost behavior</span></span></th>
<th><span data-ttu-id="24be3-670">Summa</span><span class="sxs-lookup"><span data-stu-id="24be3-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-671">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="24be3-672">CC001</span><span class="sxs-lookup"><span data-stu-id="24be3-672">CC001</span></span></td>
<td><span data-ttu-id="24be3-673">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="24be3-673">HR</span></span></td>
<td><span data-ttu-id="24be3-674">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-674">10001</span></span></td>
<td><span data-ttu-id="24be3-675">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-675">Electricity</span></span></td>
<td><span data-ttu-id="24be3-676">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-676">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-677">500,00</span><span class="sxs-lookup"><span data-stu-id="24be3-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-678">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="24be3-679">CC001</span><span class="sxs-lookup"><span data-stu-id="24be3-679">CC001</span></span></td>
<td><span data-ttu-id="24be3-680">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="24be3-680">HR</span></span></td>
<td><span data-ttu-id="24be3-681">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-681">10001</span></span></td>
<td><span data-ttu-id="24be3-682">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-682">Electricity</span></span></td>
<td><span data-ttu-id="24be3-683">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-683">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="24be3-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-685">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="24be3-686">CC002</span><span class="sxs-lookup"><span data-stu-id="24be3-686">CC002</span></span></td>
<td><span data-ttu-id="24be3-687">Finantsid</span><span class="sxs-lookup"><span data-stu-id="24be3-687">Finance</span></span></td>
<td><span data-ttu-id="24be3-688">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-688">10001</span></span></td>
<td><span data-ttu-id="24be3-689">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-689">Electricity</span></span></td>
<td><span data-ttu-id="24be3-690">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-690">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-691">675.00</span><span class="sxs-lookup"><span data-stu-id="24be3-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-692">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="24be3-693">CC002</span><span class="sxs-lookup"><span data-stu-id="24be3-693">CC002</span></span></td>
<td><span data-ttu-id="24be3-694">Finantsid</span><span class="sxs-lookup"><span data-stu-id="24be3-694">Finance</span></span></td>
<td><span data-ttu-id="24be3-695">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-695">10001</span></span></td>
<td><span data-ttu-id="24be3-696">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-696">Electricity</span></span></td>
<td><span data-ttu-id="24be3-697">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-697">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="24be3-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-699">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="24be3-700">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-700">CC003</span></span></td>
<td><span data-ttu-id="24be3-701">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-701">Assembly</span></span></td>
<td><span data-ttu-id="24be3-702">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-702">10001</span></span></td>
<td><span data-ttu-id="24be3-703">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-703">Electricity</span></span></td>
<td><span data-ttu-id="24be3-704">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-704">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-705">713.75</span><span class="sxs-lookup"><span data-stu-id="24be3-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-706">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="24be3-707">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-707">CC003</span></span></td>
<td><span data-ttu-id="24be3-708">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-708">Assembly</span></span></td>
<td><span data-ttu-id="24be3-709">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-709">10001</span></span></td>
<td><span data-ttu-id="24be3-710">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-710">Electricity</span></span></td>
<td><span data-ttu-id="24be3-711">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-711">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="24be3-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-713">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="24be3-714">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-714">CC003</span></span></td>
<td><span data-ttu-id="24be3-715">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="24be3-715">Packaging</span></span></td>
<td><span data-ttu-id="24be3-716">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-716">10001</span></span></td>
<td><span data-ttu-id="24be3-717">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-717">Electricity</span></span></td>
<td><span data-ttu-id="24be3-718">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-718">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-719">286.25</span><span class="sxs-lookup"><span data-stu-id="24be3-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-720">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="24be3-721">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-721">CC003</span></span></td>
<td><span data-ttu-id="24be3-722">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="24be3-722">Packaging</span></span></td>
<td><span data-ttu-id="24be3-723">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-723">10001</span></span></td>
<td><span data-ttu-id="24be3-724">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-724">Electricity</span></span></td>
<td><span data-ttu-id="24be3-725">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-725">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="24be3-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-727">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="24be3-728">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="24be3-728">Prod 1</span></span></td>
<td><span data-ttu-id="24be3-729">Toode 1</span><span class="sxs-lookup"><span data-stu-id="24be3-729">Product 1</span></span></td>
<td><span data-ttu-id="24be3-730">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-730">10001</span></span></td>
<td><span data-ttu-id="24be3-731">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-731">Electricity</span></span></td>
<td><span data-ttu-id="24be3-732">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-732">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-733">776.36</span><span class="sxs-lookup"><span data-stu-id="24be3-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-734">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="24be3-735">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="24be3-735">Prod 1</span></span></td>
<td><span data-ttu-id="24be3-736">Toode 1</span><span class="sxs-lookup"><span data-stu-id="24be3-736">Product 1</span></span></td>
<td><span data-ttu-id="24be3-737">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-737">10001</span></span></td>
<td><span data-ttu-id="24be3-738">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-738">Electricity</span></span></td>
<td><span data-ttu-id="24be3-739">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-739">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="24be3-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-741">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="24be3-742">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-742">Prod 2</span></span></td>
<td><span data-ttu-id="24be3-743">Toode 1</span><span class="sxs-lookup"><span data-stu-id="24be3-743">Product 1</span></span></td>
<td><span data-ttu-id="24be3-744">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-744">10001</span></span></td>
<td><span data-ttu-id="24be3-745">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-745">Electricity</span></span></td>
<td><span data-ttu-id="24be3-746">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-746">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-747">223.64</span><span class="sxs-lookup"><span data-stu-id="24be3-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-748">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="24be3-749">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-749">Prod 2</span></span></td>
<td><span data-ttu-id="24be3-750">Toode 1</span><span class="sxs-lookup"><span data-stu-id="24be3-750">Product 1</span></span></td>
<td><span data-ttu-id="24be3-751">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-751">10001</span></span></td>
<td><span data-ttu-id="24be3-752">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-752">Electricity</span></span></td>
<td><span data-ttu-id="24be3-753">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-753">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="24be3-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="24be3-755">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="24be3-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="24be3-756">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="24be3-757">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="24be3-757">Cost element</span></span></th>
<th><span data-ttu-id="24be3-758">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="24be3-758">Cost behavior</span></span></th>
<th><span data-ttu-id="24be3-759">Summa</span><span class="sxs-lookup"><span data-stu-id="24be3-759">Amount</span></span></th>
<th><span data-ttu-id="24be3-760">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="24be3-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="24be3-761">CC001</span><span class="sxs-lookup"><span data-stu-id="24be3-761">CC001</span></span></td>
<td><span data-ttu-id="24be3-762">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="24be3-762">HR</span></span></td>
<td><span data-ttu-id="24be3-763">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-763">10001</span></span></td>
<td><span data-ttu-id="24be3-764">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-764">Electricity</span></span></td>
<td><span data-ttu-id="24be3-765">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-765">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-766">‑500,00</span><span class="sxs-lookup"><span data-stu-id="24be3-766">-500.00</span></span></td>
<td><span data-ttu-id="24be3-767">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-768">CC002</span><span class="sxs-lookup"><span data-stu-id="24be3-768">CC002</span></span></td>
<td><span data-ttu-id="24be3-769">Finantsid</span><span class="sxs-lookup"><span data-stu-id="24be3-769">Finance</span></span></td>
<td><span data-ttu-id="24be3-770">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-770">10001</span></span></td>
<td><span data-ttu-id="24be3-771">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-771">Electricity</span></span></td>
<td><span data-ttu-id="24be3-772">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-772">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-773">175.00</span><span class="sxs-lookup"><span data-stu-id="24be3-773">175.00</span></span></td>
<td><span data-ttu-id="24be3-774">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-775">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-775">CC003</span></span></td>
<td><span data-ttu-id="24be3-776">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-776">Assembly</span></span></td>
<td><span data-ttu-id="24be3-777">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-777">10001</span></span></td>
<td><span data-ttu-id="24be3-778">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-778">Electricity</span></span></td>
<td><span data-ttu-id="24be3-779">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-779">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-780">275.00</span><span class="sxs-lookup"><span data-stu-id="24be3-780">275.00</span></span></td>
<td><span data-ttu-id="24be3-781">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-782">CC004</span><span class="sxs-lookup"><span data-stu-id="24be3-782">CC004</span></span></td>
<td><span data-ttu-id="24be3-783">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="24be3-783">Packaging</span></span></td>
<td><span data-ttu-id="24be3-784">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-784">10001</span></span></td>
<td><span data-ttu-id="24be3-785">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-785">Electricity</span></span></td>
<td><span data-ttu-id="24be3-786">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-786">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-787">50,00</span><span class="sxs-lookup"><span data-stu-id="24be3-787">50,00</span></span></td>
<td><span data-ttu-id="24be3-788">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-789">CC001</span><span class="sxs-lookup"><span data-stu-id="24be3-789">CC001</span></span></td>
<td><span data-ttu-id="24be3-790">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="24be3-790">HR</span></span></td>
<td><span data-ttu-id="24be3-791">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-791">10001</span></span></td>
<td><span data-ttu-id="24be3-792">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-792">Electricity</span></span></td>
<td><span data-ttu-id="24be3-793">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-793">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-794">–1245,71</span><span class="sxs-lookup"><span data-stu-id="24be3-794">-1,245.71</span></span></td>
<td><span data-ttu-id="24be3-795">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-796">CC002</span><span class="sxs-lookup"><span data-stu-id="24be3-796">CC002</span></span></td>
<td><span data-ttu-id="24be3-797">Finantsid</span><span class="sxs-lookup"><span data-stu-id="24be3-797">Finance</span></span></td>
<td><span data-ttu-id="24be3-798">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-798">10001</span></span></td>
<td><span data-ttu-id="24be3-799">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-799">Electricity</span></span></td>
<td><span data-ttu-id="24be3-800">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-800">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-801">436.00</span><span class="sxs-lookup"><span data-stu-id="24be3-801">436.00</span></span></td>
<td><span data-ttu-id="24be3-802">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-803">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-803">CC003</span></span></td>
<td><span data-ttu-id="24be3-804">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-804">Assembly</span></span></td>
<td><span data-ttu-id="24be3-805">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-805">10001</span></span></td>
<td><span data-ttu-id="24be3-806">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-806">Electricity</span></span></td>
<td><span data-ttu-id="24be3-807">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-807">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-808">685.14</span><span class="sxs-lookup"><span data-stu-id="24be3-808">685.14</span></span></td>
<td><span data-ttu-id="24be3-809">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-810">CC004</span><span class="sxs-lookup"><span data-stu-id="24be3-810">CC004</span></span></td>
<td><span data-ttu-id="24be3-811">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="24be3-811">Packaging</span></span></td>
<td><span data-ttu-id="24be3-812">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-812">10001</span></span></td>
<td><span data-ttu-id="24be3-813">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-813">Electricity</span></span></td>
<td><span data-ttu-id="24be3-814">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-814">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-815">124.57</span><span class="sxs-lookup"><span data-stu-id="24be3-815">124.57</span></span></td>
<td><span data-ttu-id="24be3-816">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-817">CC002</span><span class="sxs-lookup"><span data-stu-id="24be3-817">CC002</span></span></td>
<td><span data-ttu-id="24be3-818">Finantsid</span><span class="sxs-lookup"><span data-stu-id="24be3-818">Finance</span></span></td>
<td><span data-ttu-id="24be3-819">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-819">10001</span></span></td>
<td><span data-ttu-id="24be3-820">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-820">Electricity</span></span></td>
<td><span data-ttu-id="24be3-821">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-821">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-822">–675,00</span><span class="sxs-lookup"><span data-stu-id="24be3-822">-675.00</span></span></td>
<td><span data-ttu-id="24be3-823">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-824">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-824">CC003</span></span></td>
<td><span data-ttu-id="24be3-825">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-825">Assembly</span></span></td>
<td><span data-ttu-id="24be3-826">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-826">10001</span></span></td>
<td><span data-ttu-id="24be3-827">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-827">Electricity</span></span></td>
<td><span data-ttu-id="24be3-828">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-828">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-829">438.75</span><span class="sxs-lookup"><span data-stu-id="24be3-829">438.75</span></span></td>
<td><span data-ttu-id="24be3-830">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-831">CC004</span><span class="sxs-lookup"><span data-stu-id="24be3-831">CC004</span></span></td>
<td><span data-ttu-id="24be3-832">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="24be3-832">Packaging</span></span></td>
<td><span data-ttu-id="24be3-833">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-833">10001</span></span></td>
<td><span data-ttu-id="24be3-834">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-834">Electricity</span></span></td>
<td><span data-ttu-id="24be3-835">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-835">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-836">236.25</span><span class="sxs-lookup"><span data-stu-id="24be3-836">236.25</span></span></td>
<td><span data-ttu-id="24be3-837">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-838">CC002</span><span class="sxs-lookup"><span data-stu-id="24be3-838">CC002</span></span></td>
<td><span data-ttu-id="24be3-839">Finantsid</span><span class="sxs-lookup"><span data-stu-id="24be3-839">Finance</span></span></td>
<td><span data-ttu-id="24be3-840">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-840">10001</span></span></td>
<td><span data-ttu-id="24be3-841">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-841">Electricity</span></span></td>
<td><span data-ttu-id="24be3-842">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-842">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-843">–8150,29</span><span class="sxs-lookup"><span data-stu-id="24be3-843">-8,150.29</span></span></td>
<td><span data-ttu-id="24be3-844">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-845">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-845">CC003</span></span></td>
<td><span data-ttu-id="24be3-846">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-846">Assembly</span></span></td>
<td><span data-ttu-id="24be3-847">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-847">10001</span></span></td>
<td><span data-ttu-id="24be3-848">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-848">Electricity</span></span></td>
<td><span data-ttu-id="24be3-849">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-849">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="24be3-850">5,297.69</span></span></td>
<td><span data-ttu-id="24be3-851">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-852">CC004</span><span class="sxs-lookup"><span data-stu-id="24be3-852">CC004</span></span></td>
<td><span data-ttu-id="24be3-853">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="24be3-853">Packaging</span></span></td>
<td><span data-ttu-id="24be3-854">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-854">10001</span></span></td>
<td><span data-ttu-id="24be3-855">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-855">Electricity</span></span></td>
<td><span data-ttu-id="24be3-856">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-856">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="24be3-857">2,852.60</span></span></td>
<td><span data-ttu-id="24be3-858">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-859">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-859">CC003</span></span></td>
<td><span data-ttu-id="24be3-860">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-860">Assembly</span></span></td>
<td><span data-ttu-id="24be3-861">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-861">10001</span></span></td>
<td><span data-ttu-id="24be3-862">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-862">Electricity</span></span></td>
<td><span data-ttu-id="24be3-863">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-863">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-864">–713,75</span><span class="sxs-lookup"><span data-stu-id="24be3-864">-713.75</span></span></td>
<td><span data-ttu-id="24be3-865">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-866">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="24be3-866">Prod 1</span></span></td>
<td><span data-ttu-id="24be3-867">Toode 1</span><span class="sxs-lookup"><span data-stu-id="24be3-867">Product 1</span></span></td>
<td><span data-ttu-id="24be3-868">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-868">10001</span></span></td>
<td><span data-ttu-id="24be3-869">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-869">Electricity</span></span></td>
<td><span data-ttu-id="24be3-870">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-870">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-871">535.31</span><span class="sxs-lookup"><span data-stu-id="24be3-871">535.31</span></span></td>
<td><span data-ttu-id="24be3-872">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-873">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-873">Prod 2</span></span></td>
<td><span data-ttu-id="24be3-874">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-874">Product 2</span></span></td>
<td><span data-ttu-id="24be3-875">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-875">10001</span></span></td>
<td><span data-ttu-id="24be3-876">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-876">Electricity</span></span></td>
<td><span data-ttu-id="24be3-877">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-877">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-878">178.44</span><span class="sxs-lookup"><span data-stu-id="24be3-878">178.44</span></span></td>
<td><span data-ttu-id="24be3-879">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-880">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-880">CC003</span></span></td>
<td><span data-ttu-id="24be3-881">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-881">Assembly</span></span></td>
<td><span data-ttu-id="24be3-882">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-882">10001</span></span></td>
<td><span data-ttu-id="24be3-883">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-883">Electricity</span></span></td>
<td><span data-ttu-id="24be3-884">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-884">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-885">–5982,83</span><span class="sxs-lookup"><span data-stu-id="24be3-885">-5,982.83</span></span></td>
<td><span data-ttu-id="24be3-886">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-887">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="24be3-887">Prod 1</span></span></td>
<td><span data-ttu-id="24be3-888">Toode 1</span><span class="sxs-lookup"><span data-stu-id="24be3-888">Product 1</span></span></td>
<td><span data-ttu-id="24be3-889">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-889">10001</span></span></td>
<td><span data-ttu-id="24be3-890">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-890">Electricity</span></span></td>
<td><span data-ttu-id="24be3-891">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-891">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="24be3-892">4,487.12</span></span></td>
<td><span data-ttu-id="24be3-893">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-894">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-894">Prod 2</span></span></td>
<td><span data-ttu-id="24be3-895">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-895">Product 2</span></span></td>
<td><span data-ttu-id="24be3-896">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-896">10001</span></span></td>
<td><span data-ttu-id="24be3-897">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-897">Electricity</span></span></td>
<td><span data-ttu-id="24be3-898">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-898">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="24be3-899">1,495.71</span></span></td>
<td><span data-ttu-id="24be3-900">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-901">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-901">CC003</span></span></td>
<td><span data-ttu-id="24be3-902">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-902">Assembly</span></span></td>
<td><span data-ttu-id="24be3-903">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-903">10001</span></span></td>
<td><span data-ttu-id="24be3-904">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-904">Electricity</span></span></td>
<td><span data-ttu-id="24be3-905">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-905">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-906">–286,25</span><span class="sxs-lookup"><span data-stu-id="24be3-906">-286.25</span></span></td>
<td><span data-ttu-id="24be3-907">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-908">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="24be3-908">Prod 1</span></span></td>
<td><span data-ttu-id="24be3-909">Toode 1</span><span class="sxs-lookup"><span data-stu-id="24be3-909">Product 1</span></span></td>
<td><span data-ttu-id="24be3-910">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-910">10001</span></span></td>
<td><span data-ttu-id="24be3-911">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-911">Electricity</span></span></td>
<td><span data-ttu-id="24be3-912">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-912">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-913">241.05</span><span class="sxs-lookup"><span data-stu-id="24be3-913">241.05</span></span></td>
<td><span data-ttu-id="24be3-914">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-915">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-915">Prod 2</span></span></td>
<td><span data-ttu-id="24be3-916">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-916">Product 2</span></span></td>
<td><span data-ttu-id="24be3-917">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-917">10001</span></span></td>
<td><span data-ttu-id="24be3-918">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-918">Electricity</span></span></td>
<td><span data-ttu-id="24be3-919">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-919">Fixed cost</span></span></td>
<td><span data-ttu-id="24be3-920">45.20</span><span class="sxs-lookup"><span data-stu-id="24be3-920">45.20</span></span></td>
<td><span data-ttu-id="24be3-921">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-922">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-922">CC003</span></span></td>
<td><span data-ttu-id="24be3-923">Assembler</span><span class="sxs-lookup"><span data-stu-id="24be3-923">Assembly</span></span></td>
<td><span data-ttu-id="24be3-924">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-924">10001</span></span></td>
<td><span data-ttu-id="24be3-925">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-925">Electricity</span></span></td>
<td><span data-ttu-id="24be3-926">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-926">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-927">–2977,17</span><span class="sxs-lookup"><span data-stu-id="24be3-927">-2,977.17</span></span></td>
<td><span data-ttu-id="24be3-928">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-929">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="24be3-929">Prod 1</span></span></td>
<td><span data-ttu-id="24be3-930">Toode 1</span><span class="sxs-lookup"><span data-stu-id="24be3-930">Product 1</span></span></td>
<td><span data-ttu-id="24be3-931">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-931">10001</span></span></td>
<td><span data-ttu-id="24be3-932">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-932">Electricity</span></span></td>
<td><span data-ttu-id="24be3-933">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-933">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="24be3-934">2,507.09</span></span></td>
<td><span data-ttu-id="24be3-935">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="24be3-936">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-936">Prod 2</span></span></td>
<td><span data-ttu-id="24be3-937">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-937">Product 2</span></span></td>
<td><span data-ttu-id="24be3-938">10001</span><span class="sxs-lookup"><span data-stu-id="24be3-938">10001</span></span></td>
<td><span data-ttu-id="24be3-939">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="24be3-939">Electricity</span></span></td>
<td><span data-ttu-id="24be3-940">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-940">Variable cost</span></span></td>
<td><span data-ttu-id="24be3-941">470.08</span><span class="sxs-lookup"><span data-stu-id="24be3-941">470.08</span></span></td>
<td><span data-ttu-id="24be3-942">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="24be3-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="24be3-943">Lõppsõna</span><span class="sxs-lookup"><span data-stu-id="24be3-943">Conclusion</span></span>
<span data-ttu-id="24be3-944">Finantsaruandluses sisestatakse elektrikulu 10 000,00 fiktiivse kulukeskuse ID-le.</span><span class="sxs-lookup"><span data-stu-id="24be3-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="24be3-945">Nii teavad kuluarvestajad, et see kulu tuleb eraldada.</span><span class="sxs-lookup"><span data-stu-id="24be3-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="24be3-946">Kuluarvestuses liigub kulu rakendatud poliitikate ja reeglite põhjal läbi organisatsiooniüksuste ja -tasemete.</span><span class="sxs-lookup"><span data-stu-id="24be3-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="24be3-947">Iga kulu on seostatud eraldamisalusega, mis pakub kulude eraldamiseks parimat hinnangut.</span><span class="sxs-lookup"><span data-stu-id="24be3-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="24be3-948">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="24be3-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="24be3-949">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="24be3-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="24be3-950">Kokku</span><span class="sxs-lookup"><span data-stu-id="24be3-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="24be3-951">CC099</span><span class="sxs-lookup"><span data-stu-id="24be3-951">CC099</span></span></th>
<th><span data-ttu-id="24be3-952">CC001</span><span class="sxs-lookup"><span data-stu-id="24be3-952">CC001</span></span></th>
<th><span data-ttu-id="24be3-953">CC002</span><span class="sxs-lookup"><span data-stu-id="24be3-953">CC002</span></span></th>
<th><span data-ttu-id="24be3-954">CC003</span><span class="sxs-lookup"><span data-stu-id="24be3-954">CC003</span></span></th>
<th><span data-ttu-id="24be3-955">CC004</span><span class="sxs-lookup"><span data-stu-id="24be3-955">CC004</span></span></th>
<th><span data-ttu-id="24be3-956">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="24be3-956">Proj 1</span></span></th>
<th><span data-ttu-id="24be3-957">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="24be3-957">Proj 2</span></span></th>
<th><span data-ttu-id="24be3-958">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="24be3-958">Prod 1</span></span></th>
<th><span data-ttu-id="24be3-959">Toode 2</span><span class="sxs-lookup"><span data-stu-id="24be3-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="24be3-960">10001 Elekter</span><span class="sxs-lookup"><span data-stu-id="24be3-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="24be3-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="24be3-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="24be3-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="24be3-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="24be3-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="24be3-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="24be3-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="24be3-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="24be3-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="24be3-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="24be3-970">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="24be3-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-971">0,00</span><span class="sxs-lookup"><span data-stu-id="24be3-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="24be3-972">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-973">0,00</span><span class="sxs-lookup"><span data-stu-id="24be3-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-974">0,00</span><span class="sxs-lookup"><span data-stu-id="24be3-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-975">0,00</span><span class="sxs-lookup"><span data-stu-id="24be3-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-976">0,00</span><span class="sxs-lookup"><span data-stu-id="24be3-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-977">0,00</span><span class="sxs-lookup"><span data-stu-id="24be3-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="24be3-978">776.36</span><span class="sxs-lookup"><span data-stu-id="24be3-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-979">223.64</span><span class="sxs-lookup"><span data-stu-id="24be3-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="24be3-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="24be3-981">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="24be3-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-982">000</span><span class="sxs-lookup"><span data-stu-id="24be3-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-983">0,00</span><span class="sxs-lookup"><span data-stu-id="24be3-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-984">0,00</span><span class="sxs-lookup"><span data-stu-id="24be3-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-985">0,00</span><span class="sxs-lookup"><span data-stu-id="24be3-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-986">0,00</span><span class="sxs-lookup"><span data-stu-id="24be3-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-987">30,00</span><span class="sxs-lookup"><span data-stu-id="24be3-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-988">10,00</span><span class="sxs-lookup"><span data-stu-id="24be3-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="24be3-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="24be3-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="24be3-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="24be3-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="24be3-992">Selles teemas selgitatakse, kuidas esmane kuluelement, 10001 Eleter, liigub läbi kuluobjektide.</span><span class="sxs-lookup"><span data-stu-id="24be3-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="24be3-993">Seega eraldatakse see üldkulu organisatsiooni madalaimale tasemele.</span><span class="sxs-lookup"><span data-stu-id="24be3-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="24be3-994">Teisisõnu kannavad kulu madalaimal tasemel olevad kuluobjektid.</span><span class="sxs-lookup"><span data-stu-id="24be3-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="24be3-995">Kui soovite saada kuluobjektide vahelisest kuluvoost visuaalset ülevaadet, saate kuluvoo visualiseerimiseks kasutada kulude kokkuvõtte poliitika reegleid.</span><span class="sxs-lookup"><span data-stu-id="24be3-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="24be3-996">Lisateavet vt teemast [Kulukomplekti poliitika ja üldkulude arvutus](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="24be3-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



