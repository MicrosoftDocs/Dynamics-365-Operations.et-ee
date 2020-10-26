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
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 923e6e38a664e17ec3349d839c4b77ec903c5dc2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976471"
---
# <a name="overhead-calculation"></a><span data-ttu-id="35c6e-103">Üldkulude arvutus</span><span class="sxs-lookup"><span data-stu-id="35c6e-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35c6e-104">Selles teemas kirjeldatakse tüüpilisi üldkulude arvutamise ja eraldamise protsesse.</span><span class="sxs-lookup"><span data-stu-id="35c6e-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="35c6e-105">Mõiste määratlus</span><span class="sxs-lookup"><span data-stu-id="35c6e-105">Term definition</span></span>
---------------

<span data-ttu-id="35c6e-106">Üldkulud on kulud, mis kaasnevad ettevõtte käitamisega, kuid mida ei saa seostada otseselt ühegi kindla äritegevuse, toote ega teenusega.</span><span class="sxs-lookup"><span data-stu-id="35c6e-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="35c6e-107">Üldkulud pakuvad kriitilist tuge kasumit andavate tegevuste loomisele.</span><span class="sxs-lookup"><span data-stu-id="35c6e-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="35c6e-108">Siin on mõned näited üldkuludest.</span><span class="sxs-lookup"><span data-stu-id="35c6e-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="35c6e-109">Üür</span><span class="sxs-lookup"><span data-stu-id="35c6e-109">Rent</span></span>
-   <span data-ttu-id="35c6e-110">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-110">Electricity</span></span>
-   <span data-ttu-id="35c6e-111">Haldustasud</span><span class="sxs-lookup"><span data-stu-id="35c6e-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="35c6e-112">Üldkulude arvutuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="35c6e-112">Overhead calculation overview</span></span>
<span data-ttu-id="35c6e-113">Üldkulude arvutus käitab kuluarvutuse poliitikaid õiges järjekorras.</span><span class="sxs-lookup"><span data-stu-id="35c6e-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="35c6e-114">Saate käivitada üldkulude arvutuse sama rahandusperioodi kohta mitu korda, kui kuluarvestuse poliitikaid on muudetud või tuvastatud teatud tõrked.</span><span class="sxs-lookup"><span data-stu-id="35c6e-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="35c6e-115">Iga üldkulude arvutamise käitamine talletatakse ja see saab kordumatu versiooni-ID, mis võimaldab teil arvutuste erinevaid versioone võrrelda.</span><span class="sxs-lookup"><span data-stu-id="35c6e-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="35c6e-116">Ülekulude arvutusega loodud kulukirjed saavad aruandluskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="35c6e-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="35c6e-117">See aruandluskuupäev vastab arvutuses kasutatud rahandusperioodi lõppkuupäevale.</span><span class="sxs-lookup"><span data-stu-id="35c6e-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="35c6e-118">Kordumatu versiooni-ID koosneb järgmistest elementidest.</span><span class="sxs-lookup"><span data-stu-id="35c6e-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="35c6e-119">Versiooni tüüp</span><span class="sxs-lookup"><span data-stu-id="35c6e-119">Version type</span></span>
-   <span data-ttu-id="35c6e-120">Kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="35c6e-120">Date and time</span></span>
-   <span data-ttu-id="35c6e-121">Kuluarvestuse pearaamat</span><span class="sxs-lookup"><span data-stu-id="35c6e-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="35c6e-122">Finantsaasta</span><span class="sxs-lookup"><span data-stu-id="35c6e-122">Fiscal year</span></span>
-   <span data-ttu-id="35c6e-123">Rahandusperiood</span><span class="sxs-lookup"><span data-stu-id="35c6e-123">Fiscal period</span></span>

<span data-ttu-id="35c6e-124">Üldkulude arvutus käivitatakse versioonist sõltumatult.</span><span class="sxs-lookup"><span data-stu-id="35c6e-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="35c6e-125">Seetõttu saate arvutada eelarveversiooni enne tegelikku versiooni.</span><span class="sxs-lookup"><span data-stu-id="35c6e-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="35c6e-126">Üldkulude arvutus koosneb neljast etapist, nagu näha alltoodud joonisel.</span><span class="sxs-lookup"><span data-stu-id="35c6e-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="35c6e-127">Igas etapis luuakse töölehe päis, millel on töölehe kanded.</span><span class="sxs-lookup"><span data-stu-id="35c6e-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="35c6e-128">See töölehe päis säiiltab sisendandmeid iga arvutusetapi kohta.</span><span class="sxs-lookup"><span data-stu-id="35c6e-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="35c6e-129">Igale töölehe reale rakendatakse poliitikad ja reeglid ning väljundina luuakse kulukirjed.</span><span class="sxs-lookup"><span data-stu-id="35c6e-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="35c6e-130">Seega on teil alati olemas põhjalik ülevaade.</span><span class="sxs-lookup"><span data-stu-id="35c6e-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="35c6e-131">[![Üldkulude arvutus](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="35c6e-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="35c6e-132">Elektri üldkulude arvutamine ja eraldamine</span><span class="sxs-lookup"><span data-stu-id="35c6e-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="35c6e-133">Finantsaruandluses on mõned kulud, näiteks elekter, registreeritud põhisummana.</span><span class="sxs-lookup"><span data-stu-id="35c6e-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="35c6e-134">Seetõttu ei pakuta kuluarvestuseks üksikasjalikku juhtimisülevaadet.</span><span class="sxs-lookup"><span data-stu-id="35c6e-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="35c6e-135">Kuluarvestuses peavad kulud liikuma läbi organisatsiooniüksuste, et pakkuda korrektset juhtimisülevaadet kõigi organisatsiooniüksuste ja -tasemete kohta.</span><span class="sxs-lookup"><span data-stu-id="35c6e-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="35c6e-136">See voog peab põhinema tarbimise või õiglase hindamise täpsel kirjendamisel.</span><span class="sxs-lookup"><span data-stu-id="35c6e-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="35c6e-137">Pearaamatus, saab elektrikulu sisestada nii, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="35c6e-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="35c6e-138">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="35c6e-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="35c6e-139">Kulukeskus</span><span class="sxs-lookup"><span data-stu-id="35c6e-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="35c6e-140">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="35c6e-140">Main account</span></span></th>
<th><span data-ttu-id="35c6e-141">Summa arvestusvaluutas</span><span class="sxs-lookup"><span data-stu-id="35c6e-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-142">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="35c6e-143">CC099</span><span class="sxs-lookup"><span data-stu-id="35c6e-143">CC099</span></span></td>
<td><span data-ttu-id="35c6e-144">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="35c6e-144">Default cost center</span></span></td>
<td><span data-ttu-id="35c6e-145">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-145">10001</span></span></td>
<td><span data-ttu-id="35c6e-146">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-146">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="35c6e-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="35c6e-148">1. etapp: kulukäitumise arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="35c6e-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="35c6e-149">Vaikimisi saavad lähteandmetest imporditud kulukirjed kuluarvestuses kulukäitumise klassifikatsiooniks **Klassifitseerimata**.</span><span class="sxs-lookup"><span data-stu-id="35c6e-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="35c6e-150">Kulukäitumise poliitikareegleid rakendades saate kulukirjed ümber klassifitseerida kui **Fikseeritud kulu** või **Muutuvkulu**.</span><span class="sxs-lookup"><span data-stu-id="35c6e-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="35c6e-151">Kulukäitumise reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="35c6e-151">Define the cost behavior rule</span></span>

<span data-ttu-id="35c6e-152">Mõnikord on osa kulust fikseeritud tasu ja järelejäänud kulu põhineb tarbimisel.</span><span class="sxs-lookup"><span data-stu-id="35c6e-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="35c6e-153">Elektriarved vastavad sageli sellele määratlusele.</span><span class="sxs-lookup"><span data-stu-id="35c6e-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="35c6e-154">Pärast kindla fikseeritud tasu maksmist maksate tarbimise eest kilovatt-tunni (Kwh) kohta.</span><span class="sxs-lookup"><span data-stu-id="35c6e-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="35c6e-155">Näiteks kui fikseeritud kulu tasu on 1000,00 eurot, määratletakse kulukäitumise reegel järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="35c6e-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="35c6e-156">Fikseeritud summa: 1000,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="35c6e-157">0 &lt;= 1000,00 = fikseeritud</span><span class="sxs-lookup"><span data-stu-id="35c6e-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="35c6e-158">1000,01 &lt; N = muutuja</span><span class="sxs-lookup"><span data-stu-id="35c6e-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="35c6e-159">Tööleht</span><span class="sxs-lookup"><span data-stu-id="35c6e-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="35c6e-160">Tööleht</span><span class="sxs-lookup"><span data-stu-id="35c6e-160">Journal</span></span></th>
<th><span data-ttu-id="35c6e-161">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="35c6e-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="35c6e-162">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="35c6e-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="35c6e-163">Versioon</span><span class="sxs-lookup"><span data-stu-id="35c6e-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-164">00001</span><span class="sxs-lookup"><span data-stu-id="35c6e-164">00001</span></span></td>
<td><span data-ttu-id="35c6e-165">Kulukäitumise arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="35c6e-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="35c6e-166">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="35c6e-166">Fiscal</span></span></td>
<td><span data-ttu-id="35c6e-167">2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-167">2017</span></span></td>
<td><span data-ttu-id="35c6e-168">Periood 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-168">Period 1</span></span></td>
<td><span data-ttu-id="35c6e-169">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="35c6e-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="35c6e-170">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="35c6e-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="35c6e-171">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="35c6e-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="35c6e-172">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="35c6e-173">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="35c6e-173">Cost element</span></span></th>
<th><span data-ttu-id="35c6e-174">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="35c6e-174">Cost behavior</span></span></th>
<th><span data-ttu-id="35c6e-175">Summa</span><span class="sxs-lookup"><span data-stu-id="35c6e-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-176">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="35c6e-177">CC099</span><span class="sxs-lookup"><span data-stu-id="35c6e-177">CC099</span></span></td>
<td><span data-ttu-id="35c6e-178">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="35c6e-178">Default cost center</span></span></td>
<td><span data-ttu-id="35c6e-179">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-179">10001</span></span></td>
<td><span data-ttu-id="35c6e-180">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-180">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-181">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="35c6e-181">Unclassified</span></span></td>
<td><span data-ttu-id="35c6e-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="35c6e-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="35c6e-183">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="35c6e-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-184">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="35c6e-185">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="35c6e-185">Cost element</span></span></th>
<th><span data-ttu-id="35c6e-186">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="35c6e-186">Cost behavior</span></span></th>
<th><span data-ttu-id="35c6e-187">Summa</span><span class="sxs-lookup"><span data-stu-id="35c6e-187">Amount</span></span></th>
<th><span data-ttu-id="35c6e-188">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="35c6e-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-189">CC099</span><span class="sxs-lookup"><span data-stu-id="35c6e-189">CC099</span></span></td>
<td><span data-ttu-id="35c6e-190">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="35c6e-190">Default cost center</span></span></td>
<td><span data-ttu-id="35c6e-191">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-191">10001</span></span></td>
<td><span data-ttu-id="35c6e-192">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-192">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-193">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="35c6e-193">Unclassified</span></span></td>
<td><span data-ttu-id="35c6e-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="35c6e-194">10,000.00</span></span></td>
<td><span data-ttu-id="35c6e-195">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-196">CC099</span><span class="sxs-lookup"><span data-stu-id="35c6e-196">CC099</span></span></td>
<td><span data-ttu-id="35c6e-197">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="35c6e-197">Default cost center</span></span></td>
<td><span data-ttu-id="35c6e-198">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-198">10001</span></span></td>
<td><span data-ttu-id="35c6e-199">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-199">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-200">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="35c6e-200">Unclassified</span></span></td>
<td><span data-ttu-id="35c6e-201">–10 000,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-201">-10,000.00</span></span></td>
<td><span data-ttu-id="35c6e-202">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-203">CC099</span><span class="sxs-lookup"><span data-stu-id="35c6e-203">CC099</span></span></td>
<td><span data-ttu-id="35c6e-204">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="35c6e-204">Default cost center</span></span></td>
<td><span data-ttu-id="35c6e-205">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-205">10001</span></span></td>
<td><span data-ttu-id="35c6e-206">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-206">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-207">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-207">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-208">1,000.00</span></span></td>
<td><span data-ttu-id="35c6e-209">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-210">CC099</span><span class="sxs-lookup"><span data-stu-id="35c6e-210">CC099</span></span></td>
<td><span data-ttu-id="35c6e-211">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="35c6e-211">Default cost center</span></span></td>
<td><span data-ttu-id="35c6e-212">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-212">10001</span></span></td>
<td><span data-ttu-id="35c6e-213">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-213">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-214">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-214">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="35c6e-215">9,000.00</span></span></td>
<td><span data-ttu-id="35c6e-216">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="35c6e-217">Lisateavet vt teemast [Kulukäitumise poliitika loomine ja määramine kulujuhtimisüksusele (tegevuse juhis)](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="35c6e-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="35c6e-218">2. etapp: kulujaotuse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="35c6e-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="35c6e-219">Kulujaotust kasutatakse kulu ümberjaotamiseks ühelt kuluobjektilt ühele või mitmele teisele kuluobjektile, rakendades asjakohast eraldusalust.</span><span class="sxs-lookup"><span data-stu-id="35c6e-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="35c6e-220">Kulujaotus ja kulueraldus erinevad selle poolest, et kulujaotus toimub alati algse kulu esmase kuluelemendi tasemel.</span><span class="sxs-lookup"><span data-stu-id="35c6e-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="35c6e-221">Kulujaotuse reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="35c6e-221">Define the cost distribution rule</span></span>

<span data-ttu-id="35c6e-222">Finantsaruandluses registreeritakse elektrikulud sageli põhisummana.</span><span class="sxs-lookup"><span data-stu-id="35c6e-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="35c6e-223">Kuluarvestuseses ei ole see lähenemine piisavalt üksikasjalik.</span><span class="sxs-lookup"><span data-stu-id="35c6e-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="35c6e-224">Muutuvkulu tuleb jaotada üksikutele kuluobjektidele õigluse alusel.</span><span class="sxs-lookup"><span data-stu-id="35c6e-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="35c6e-225">Kõige loogilisem eraldamisalus on elektritarbimine (kWh).</span><span class="sxs-lookup"><span data-stu-id="35c6e-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="35c6e-226">Luuakse statistilise dimensiooni liige nimega Elekter ja elektritarbimine on kirjendatakse.</span><span class="sxs-lookup"><span data-stu-id="35c6e-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="35c6e-227">Vaikimisi muutuvad kõik statistilise dimensiooni liikmed eraldamisalusena kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="35c6e-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-228">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-228">Cost object</span></span></th>
<th><span data-ttu-id="35c6e-229">kWh</span><span class="sxs-lookup"><span data-stu-id="35c6e-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-230">CC001</span><span class="sxs-lookup"><span data-stu-id="35c6e-230">CC001</span></span></td>
<td><span data-ttu-id="35c6e-231">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="35c6e-231">HR</span></span></td>
<td><span data-ttu-id="35c6e-232">1000</span><span class="sxs-lookup"><span data-stu-id="35c6e-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-233">CC002</span><span class="sxs-lookup"><span data-stu-id="35c6e-233">CC002</span></span></td>
<td><span data-ttu-id="35c6e-234">Finantsid</span><span class="sxs-lookup"><span data-stu-id="35c6e-234">Finance</span></span></td>
<td><span data-ttu-id="35c6e-235">6,000</span><span class="sxs-lookup"><span data-stu-id="35c6e-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-236">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-236">CC003</span></span></td>
<td><span data-ttu-id="35c6e-237">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-237">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-238">0</span><span class="sxs-lookup"><span data-stu-id="35c6e-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="35c6e-239">Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="35c6e-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-240">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-240">Cost object</span></span></th>
<th><span data-ttu-id="35c6e-241">Väärtus</span><span class="sxs-lookup"><span data-stu-id="35c6e-241">Magnitude</span></span></th>
<th><span data-ttu-id="35c6e-242">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="35c6e-242">Allocation factor</span></span></th>
<th><span data-ttu-id="35c6e-243">Summa</span><span class="sxs-lookup"><span data-stu-id="35c6e-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-244">CC001</span><span class="sxs-lookup"><span data-stu-id="35c6e-244">CC001</span></span></td>
<td><span data-ttu-id="35c6e-245">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="35c6e-245">HR</span></span></td>
<td><span data-ttu-id="35c6e-246">1000</span><span class="sxs-lookup"><span data-stu-id="35c6e-246">1,000</span></span></td>
<td><span data-ttu-id="35c6e-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="35c6e-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="35c6e-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-249">CC002</span><span class="sxs-lookup"><span data-stu-id="35c6e-249">CC002</span></span></td>
<td><span data-ttu-id="35c6e-250">Finantsid</span><span class="sxs-lookup"><span data-stu-id="35c6e-250">Finance</span></span></td>
<td><span data-ttu-id="35c6e-251">6,000</span><span class="sxs-lookup"><span data-stu-id="35c6e-251">6,000</span></span></td>
<td><span data-ttu-id="35c6e-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="35c6e-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="35c6e-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-254">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-254">CC003</span></span></td>
<td><span data-ttu-id="35c6e-255">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-255">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-256">0</span><span class="sxs-lookup"><span data-stu-id="35c6e-256">0</span></span></td>
<td><span data-ttu-id="35c6e-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="35c6e-258">0,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="35c6e-259">Fikseeritud kulu tuleb jaotada ühtlaselt üksikutele kuluobjektidele, mis on tarbinud elektrit.</span><span class="sxs-lookup"><span data-stu-id="35c6e-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="35c6e-260">Selle tulemuse saate, kasutades valemi eraldamisaluses statistilise dimensiooni liiget Elekter: (Elekter &gt; 0,00). Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="35c6e-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-261">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-261">Cost object</span></span></th>
<th><span data-ttu-id="35c6e-262">Valem</span><span class="sxs-lookup"><span data-stu-id="35c6e-262">Formula</span></span></th>
<th><span data-ttu-id="35c6e-263">Väärtus</span><span class="sxs-lookup"><span data-stu-id="35c6e-263">Magnitude</span></span></th>
<th><span data-ttu-id="35c6e-264">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="35c6e-264">Allocation factor</span></span></th>
<th><span data-ttu-id="35c6e-265">Summa</span><span class="sxs-lookup"><span data-stu-id="35c6e-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-266">CC001</span><span class="sxs-lookup"><span data-stu-id="35c6e-266">CC001</span></span></td>
<td><span data-ttu-id="35c6e-267">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="35c6e-267">HR</span></span></td>
<td><span data-ttu-id="35c6e-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="35c6e-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="35c6e-269">1</span><span class="sxs-lookup"><span data-stu-id="35c6e-269">1</span></span></td>
<td><span data-ttu-id="35c6e-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="35c6e-271">500,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-272">CC002</span><span class="sxs-lookup"><span data-stu-id="35c6e-272">CC002</span></span></td>
<td><span data-ttu-id="35c6e-273">Finantsid</span><span class="sxs-lookup"><span data-stu-id="35c6e-273">Finance</span></span></td>
<td><span data-ttu-id="35c6e-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="35c6e-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="35c6e-275">1</span><span class="sxs-lookup"><span data-stu-id="35c6e-275">1</span></span></td>
<td><span data-ttu-id="35c6e-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="35c6e-277">500,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-278">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-278">CC003</span></span></td>
<td><span data-ttu-id="35c6e-279">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-279">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="35c6e-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="35c6e-281">0</span><span class="sxs-lookup"><span data-stu-id="35c6e-281">0</span></span></td>
<td><span data-ttu-id="35c6e-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="35c6e-283">0,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="35c6e-284">Tööleht</span><span class="sxs-lookup"><span data-stu-id="35c6e-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="35c6e-285">Tööleht</span><span class="sxs-lookup"><span data-stu-id="35c6e-285">Journal</span></span></th>
<th><span data-ttu-id="35c6e-286">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="35c6e-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="35c6e-287">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="35c6e-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="35c6e-288">Versioon</span><span class="sxs-lookup"><span data-stu-id="35c6e-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-289">00002</span><span class="sxs-lookup"><span data-stu-id="35c6e-289">00002</span></span></td>
<td><span data-ttu-id="35c6e-290">Kulujaotuse arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="35c6e-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="35c6e-291">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="35c6e-291">Fiscal</span></span></td>
<td><span data-ttu-id="35c6e-292">2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-292">2017</span></span></td>
<td><span data-ttu-id="35c6e-293">Periood 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-293">Period 1</span></span></td>
<td><span data-ttu-id="35c6e-294">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="35c6e-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="35c6e-295">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="35c6e-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="35c6e-296">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="35c6e-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="35c6e-297">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="35c6e-298">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="35c6e-298">Cost element</span></span></th>
<th><span data-ttu-id="35c6e-299">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="35c6e-299">Cost behavior</span></span></th>
<th><span data-ttu-id="35c6e-300">Summa</span><span class="sxs-lookup"><span data-stu-id="35c6e-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-301">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="35c6e-302">CC099</span><span class="sxs-lookup"><span data-stu-id="35c6e-302">CC099</span></span></td>
<td><span data-ttu-id="35c6e-303">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="35c6e-303">Default cost center</span></span></td>
<td><span data-ttu-id="35c6e-304">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-304">10001</span></span></td>
<td><span data-ttu-id="35c6e-305">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-305">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-306">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-306">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-308">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="35c6e-309">CC099</span><span class="sxs-lookup"><span data-stu-id="35c6e-309">CC099</span></span></td>
<td><span data-ttu-id="35c6e-310">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="35c6e-310">Default cost center</span></span></td>
<td><span data-ttu-id="35c6e-311">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-311">10001</span></span></td>
<td><span data-ttu-id="35c6e-312">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-312">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-313">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-313">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="35c6e-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="35c6e-315">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="35c6e-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-316">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="35c6e-317">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="35c6e-317">Cost element</span></span></th>
<th><span data-ttu-id="35c6e-318">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="35c6e-318">Cost behavior</span></span></th>
<th><span data-ttu-id="35c6e-319">Summa</span><span class="sxs-lookup"><span data-stu-id="35c6e-319">Amount</span></span></th>
<th><span data-ttu-id="35c6e-320">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="35c6e-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-321">CC099</span><span class="sxs-lookup"><span data-stu-id="35c6e-321">CC099</span></span></td>
<td><span data-ttu-id="35c6e-322">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="35c6e-322">Default cost center</span></span></td>
<td><span data-ttu-id="35c6e-323">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-323">10001</span></span></td>
<td><span data-ttu-id="35c6e-324">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-324">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-325">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-325">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-326">–1000,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-326">-1,000.00</span></span></td>
<td><span data-ttu-id="35c6e-327">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-328">CC001</span><span class="sxs-lookup"><span data-stu-id="35c6e-328">CC001</span></span></td>
<td><span data-ttu-id="35c6e-329">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="35c6e-329">HR</span></span></td>
<td><span data-ttu-id="35c6e-330">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-330">10001</span></span></td>
<td><span data-ttu-id="35c6e-331">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-331">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-332">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-332">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-333">500,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-333">500.00</span></span></td>
<td><span data-ttu-id="35c6e-334">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-335">CC002</span><span class="sxs-lookup"><span data-stu-id="35c6e-335">CC002</span></span></td>
<td><span data-ttu-id="35c6e-336">Finantsid</span><span class="sxs-lookup"><span data-stu-id="35c6e-336">Finance</span></span></td>
<td><span data-ttu-id="35c6e-337">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-337">10001</span></span></td>
<td><span data-ttu-id="35c6e-338">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-338">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-339">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-339">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-340">500,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-340">500.00</span></span></td>
<td><span data-ttu-id="35c6e-341">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-342">CC099</span><span class="sxs-lookup"><span data-stu-id="35c6e-342">CC099</span></span></td>
<td><span data-ttu-id="35c6e-343">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="35c6e-343">Default cost center</span></span></td>
<td><span data-ttu-id="35c6e-344">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-344">10001</span></span></td>
<td><span data-ttu-id="35c6e-345">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-345">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-346">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-346">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-347">–9000,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-347">-9,000.00</span></span></td>
<td><span data-ttu-id="35c6e-348">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-349">CC001</span><span class="sxs-lookup"><span data-stu-id="35c6e-349">CC001</span></span></td>
<td><span data-ttu-id="35c6e-350">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="35c6e-350">HR</span></span></td>
<td><span data-ttu-id="35c6e-351">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-351">10001</span></span></td>
<td><span data-ttu-id="35c6e-352">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-352">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-353">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-353">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="35c6e-354">1,285.71</span></span></td>
<td><span data-ttu-id="35c6e-355">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-356">CC002</span><span class="sxs-lookup"><span data-stu-id="35c6e-356">CC002</span></span></td>
<td><span data-ttu-id="35c6e-357">Finantsid</span><span class="sxs-lookup"><span data-stu-id="35c6e-357">Finance</span></span></td>
<td><span data-ttu-id="35c6e-358">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-358">10001</span></span></td>
<td><span data-ttu-id="35c6e-359">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-359">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-360">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-360">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="35c6e-361">7,714.29</span></span></td>
<td><span data-ttu-id="35c6e-362">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="35c6e-363">Lisateavet vt teemast [Kulujaotise poliitika loomine ja määramine kulujuhtimisüksusele (tegevuse juhis)](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="35c6e-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="35c6e-364">3. etapp: üldkulude määra arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="35c6e-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="35c6e-365">Üldkulude määra kasutatakse ühe või mitme kindla kuluobjekti debiteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="35c6e-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="35c6e-366">Tasu põhineb eelmääratud kulumääral ja väärtusel määratud eraldamisalusest.</span><span class="sxs-lookup"><span data-stu-id="35c6e-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="35c6e-367">Üldkulu määra määratlemine</span><span class="sxs-lookup"><span data-stu-id="35c6e-367">Define the overhead rate</span></span>

<span data-ttu-id="35c6e-368">Kuluobjekt CC001 inimressursid panustab sisemiste projektide kogumisse.</span><span class="sxs-lookup"><span data-stu-id="35c6e-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="35c6e-369">Luuakse statistilise dimensiooni liige nimega Inimressursside projektid, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="35c6e-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-370">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-370">Cost object</span></span></th>
<th><span data-ttu-id="35c6e-371">Tunnid</span><span class="sxs-lookup"><span data-stu-id="35c6e-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-372">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-372">Proj 1</span></span></td>
<td><span data-ttu-id="35c6e-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-373">Project 1</span></span></td>
<td><span data-ttu-id="35c6e-374">3</span><span class="sxs-lookup"><span data-stu-id="35c6e-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-375">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-375">Proj 2</span></span></td>
<td><span data-ttu-id="35c6e-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-376">Project 2</span></span></td>
<td><span data-ttu-id="35c6e-377">1</span><span class="sxs-lookup"><span data-stu-id="35c6e-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="35c6e-378">Määratletud on eelmääratud kulumäär kuluprojektide panusele.</span><span class="sxs-lookup"><span data-stu-id="35c6e-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-379">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-379">Cost object</span></span></th>
<th><span data-ttu-id="35c6e-380">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="35c6e-380">Cost element</span></span></th>
<th><span data-ttu-id="35c6e-381">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="35c6e-381">Cost behavior</span></span></th>
<th><span data-ttu-id="35c6e-382">Ühikud</span><span class="sxs-lookup"><span data-stu-id="35c6e-382">Units</span></span></th>
<th><span data-ttu-id="35c6e-383">Kurss</span><span class="sxs-lookup"><span data-stu-id="35c6e-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-384">CC001</span><span class="sxs-lookup"><span data-stu-id="35c6e-384">CC001</span></span></td>
<td><span data-ttu-id="35c6e-385">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="35c6e-385">HR</span></span></td>
<td><span data-ttu-id="35c6e-386">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-386">10001</span></span></td>
<td><span data-ttu-id="35c6e-387">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-387">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-388">1</span><span class="sxs-lookup"><span data-stu-id="35c6e-388">1</span></span></td>
<td><span data-ttu-id="35c6e-389">10</span><span class="sxs-lookup"><span data-stu-id="35c6e-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="35c6e-390">Järgmises tabelis on näidatud tulemus, kui inimressursside projektid on rakendatud eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="35c6e-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-391">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-391">Cost object</span></span></th>
<th><span data-ttu-id="35c6e-392">Väärtus</span><span class="sxs-lookup"><span data-stu-id="35c6e-392">Magnitude</span></span></th>
<th><span data-ttu-id="35c6e-393">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="35c6e-393">Cost element</span></span></th>
<th><span data-ttu-id="35c6e-394">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="35c6e-394">Allocation factor</span></span></th>
<th><span data-ttu-id="35c6e-395">Summa</span><span class="sxs-lookup"><span data-stu-id="35c6e-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-396">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-396">Proj 1</span></span></td>
<td><span data-ttu-id="35c6e-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-397">Project 1</span></span></td>
<td><span data-ttu-id="35c6e-398">3</span><span class="sxs-lookup"><span data-stu-id="35c6e-398">3</span></span></td>
<td><span data-ttu-id="35c6e-399">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-399">10001</span></span></td>
<td><span data-ttu-id="35c6e-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="35c6e-401">30,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-402">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-402">Proj 2</span></span></td>
<td><span data-ttu-id="35c6e-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-403">Project 2</span></span></td>
<td><span data-ttu-id="35c6e-404">1</span><span class="sxs-lookup"><span data-stu-id="35c6e-404">1</span></span></td>
<td><span data-ttu-id="35c6e-405">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-405">10001</span></span></td>
<td><span data-ttu-id="35c6e-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="35c6e-407">10,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="35c6e-408">Tööleht</span><span class="sxs-lookup"><span data-stu-id="35c6e-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="35c6e-409">Tööleht</span><span class="sxs-lookup"><span data-stu-id="35c6e-409">Journal</span></span></th>
<th><span data-ttu-id="35c6e-410">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="35c6e-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="35c6e-411">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="35c6e-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="35c6e-412">Versioon</span><span class="sxs-lookup"><span data-stu-id="35c6e-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-413">00003</span><span class="sxs-lookup"><span data-stu-id="35c6e-413">00003</span></span></td>
<td><span data-ttu-id="35c6e-414">Üldkulu määra arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="35c6e-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="35c6e-415">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="35c6e-415">Fiscal</span></span></td>
<td><span data-ttu-id="35c6e-416">2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-416">2017</span></span></td>
<td><span data-ttu-id="35c6e-417">Periood 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-417">Period 1</span></span></td>
<td><span data-ttu-id="35c6e-418">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="35c6e-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="35c6e-419">Töölehe sisestused (töölehe sisestused üldkulu määra arvutamiseks)</span><span class="sxs-lookup"><span data-stu-id="35c6e-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="35c6e-420">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="35c6e-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="35c6e-421">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-421">Cost object</span></span></th>
<th><span data-ttu-id="35c6e-422">Väärtus</span><span class="sxs-lookup"><span data-stu-id="35c6e-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-423">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="35c6e-424">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-424">Proj 1</span></span></td>
<td><span data-ttu-id="35c6e-425">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="35c6e-426">3,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-427">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="35c6e-428">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-428">Proj 2</span></span></td>
<td><span data-ttu-id="35c6e-429">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="35c6e-430">1,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="35c6e-431">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="35c6e-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-432">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="35c6e-433">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="35c6e-433">Cost element</span></span></th>
<th><span data-ttu-id="35c6e-434">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="35c6e-434">Cost behavior</span></span></th>
<th><span data-ttu-id="35c6e-435">Summa</span><span class="sxs-lookup"><span data-stu-id="35c6e-435">Amount</span></span></th>
<th><span data-ttu-id="35c6e-436">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="35c6e-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="35c6e-437">CC0001</span></span></td>
<td><span data-ttu-id="35c6e-438">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="35c6e-438">HR</span></span></td>
<td><span data-ttu-id="35c6e-439">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-439">10001</span></span></td>
<td><span data-ttu-id="35c6e-440">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-440">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-441">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-441">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-442">–30,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-442">-30.00</span></span></td>
<td><span data-ttu-id="35c6e-443">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-444">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-444">Proj 1</span></span></td>
<td><span data-ttu-id="35c6e-445">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="35c6e-446">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-446">10001</span></span></td>
<td><span data-ttu-id="35c6e-447">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-447">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-448">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-448">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-449">30,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-449">30.00</span></span></td>
<td><span data-ttu-id="35c6e-450">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-451">CC001</span><span class="sxs-lookup"><span data-stu-id="35c6e-451">CC001</span></span></td>
<td><span data-ttu-id="35c6e-452">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="35c6e-452">HR</span></span></td>
<td><span data-ttu-id="35c6e-453">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-453">10001</span></span></td>
<td><span data-ttu-id="35c6e-454">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-454">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-455">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-455">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-456">-10.00</span></span></td>
<td><span data-ttu-id="35c6e-457">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-458">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-458">Proj 2</span></span></td>
<td><span data-ttu-id="35c6e-459">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="35c6e-460">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-460">10001</span></span></td>
<td><span data-ttu-id="35c6e-461">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-461">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-462">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-462">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-463">10.00</span><span class="sxs-lookup"><span data-stu-id="35c6e-463">10.00</span></span></td>
<td><span data-ttu-id="35c6e-464">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="35c6e-465">Lisateavet vt teemast [Üldkulude arvutamine](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="35c6e-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="35c6e-466">4. etapp: kulueralduse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="35c6e-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="35c6e-467">Eraldamist kasutatakse kuluobjekti saldo eraldamiseks teistele kuluobjektidele, rakendades eraldamisalust.</span><span class="sxs-lookup"><span data-stu-id="35c6e-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="35c6e-468">Finance toetab vastastikuse eraldamise meetodit.</span><span class="sxs-lookup"><span data-stu-id="35c6e-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="35c6e-469">Vastastikuse eraldamise meetodi puhul tuvastatakse täiendavate kuluobjektide vahetatavad vastastikused teenused.</span><span class="sxs-lookup"><span data-stu-id="35c6e-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="35c6e-470">Süsteem määrab automaatselt eraldamiste tegemise õige järjekorra.</span><span class="sxs-lookup"><span data-stu-id="35c6e-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="35c6e-471">Kuluobjekti saldo eraldatakse üksiku eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="35c6e-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="35c6e-472">Toetatakse eraldamisi kuluobjektide dimensioonide ja nende vastavate liikmete seas.</span><span class="sxs-lookup"><span data-stu-id="35c6e-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="35c6e-473">Eraldamisjärjekorda reguleerib kulujuhtseade.</span><span class="sxs-lookup"><span data-stu-id="35c6e-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="35c6e-474">[![Vastastikune meetod](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="35c6e-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="35c6e-475">Kulueraldamise määratlemine</span><span class="sxs-lookup"><span data-stu-id="35c6e-475">Define the cost allocation</span></span>

<span data-ttu-id="35c6e-476">Siin on lihtne näide, mis selgitab, kuidas jälgida kulu liikumist.</span><span class="sxs-lookup"><span data-stu-id="35c6e-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="35c6e-477">Kuluobjekt CC001 inimressursid panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="35c6e-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="35c6e-478">Luuakse statistilise dimensiooni liige nimega Inimressursside teenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="35c6e-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-479">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-479">Cost object</span></span></th>
<th><span data-ttu-id="35c6e-480">Inimressursside teenused</span><span class="sxs-lookup"><span data-stu-id="35c6e-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-481">CC002</span><span class="sxs-lookup"><span data-stu-id="35c6e-481">CC002</span></span></td>
<td><span data-ttu-id="35c6e-482">Finantsid</span><span class="sxs-lookup"><span data-stu-id="35c6e-482">Finance</span></span></td>
<td><span data-ttu-id="35c6e-483">35</span><span class="sxs-lookup"><span data-stu-id="35c6e-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-484">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-484">CC003</span></span></td>
<td><span data-ttu-id="35c6e-485">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-485">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-486">55</span><span class="sxs-lookup"><span data-stu-id="35c6e-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-487">CC004</span><span class="sxs-lookup"><span data-stu-id="35c6e-487">CC004</span></span></td>
<td><span data-ttu-id="35c6e-488">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="35c6e-488">Packaging</span></span></td>
<td><span data-ttu-id="35c6e-489">10</span><span class="sxs-lookup"><span data-stu-id="35c6e-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="35c6e-490">Kuluobjekt CC002 rahandus panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="35c6e-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="35c6e-491">Luuakse statistilise dimensiooni liige nimega Rahandusteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="35c6e-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-492">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-492">Cost object</span></span></th>
<th><span data-ttu-id="35c6e-493">Rahandusteenused</span><span class="sxs-lookup"><span data-stu-id="35c6e-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-494">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-494">CC003</span></span></td>
<td><span data-ttu-id="35c6e-495">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-495">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-496">65</span><span class="sxs-lookup"><span data-stu-id="35c6e-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-497">CC004</span><span class="sxs-lookup"><span data-stu-id="35c6e-497">CC004</span></span></td>
<td><span data-ttu-id="35c6e-498">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="35c6e-498">Packaging</span></span></td>
<td><span data-ttu-id="35c6e-499">35</span><span class="sxs-lookup"><span data-stu-id="35c6e-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="35c6e-500">Kuluobjekt CC003 assembler panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="35c6e-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="35c6e-501">Luuakse statistilise dimensiooni liige nimega Assembleriteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="35c6e-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-502">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-502">Cost object</span></span></th>
<th><span data-ttu-id="35c6e-503">Assembleriteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="35c6e-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-504">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-504">Prod 1</span></span></td>
<td><span data-ttu-id="35c6e-505">Toode 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-505">Product 1</span></span></td>
<td><span data-ttu-id="35c6e-506">60</span><span class="sxs-lookup"><span data-stu-id="35c6e-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-507">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-507">Prod 2</span></span></td>
<td><span data-ttu-id="35c6e-508">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-508">Product 2</span></span></td>
<td><span data-ttu-id="35c6e-509">20</span><span class="sxs-lookup"><span data-stu-id="35c6e-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="35c6e-510">Kuluobjekt CC004 pakendamine panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="35c6e-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="35c6e-511">Luuakse statistilise dimensiooni liige nimega Pakendamisteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="35c6e-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-512">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-512">Cost object</span></span></th>
<th><span data-ttu-id="35c6e-513">Pakendamisteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="35c6e-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-514">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-514">Prod 1</span></span></td>
<td><span data-ttu-id="35c6e-515">Toode 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-515">Product 1</span></span></td>
<td><span data-ttu-id="35c6e-516">80</span><span class="sxs-lookup"><span data-stu-id="35c6e-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-517">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-517">Prod 2</span></span></td>
<td><span data-ttu-id="35c6e-518">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-518">Product 2</span></span></td>
<td><span data-ttu-id="35c6e-519">15</span><span class="sxs-lookup"><span data-stu-id="35c6e-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="35c6e-520">Statistilised mõõdud, nagu toote tarbitud tootmistunnid, saab tuletada lähteandmetest.</span><span class="sxs-lookup"><span data-stu-id="35c6e-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="35c6e-521">Lisateavet vt teemast [Statistiliste mõõtude pakkuja mall](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="35c6e-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="35c6e-522">Järgmises tabelis on näidatud tulemus, kui HR-teenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="35c6e-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-523">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-523">Cost object</span></span></th>
<th><span data-ttu-id="35c6e-524">Väärtus</span><span class="sxs-lookup"><span data-stu-id="35c6e-524">Magnitude</span></span></th>
<th><span data-ttu-id="35c6e-525">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="35c6e-525">Allocation factor</span></span></th>
<th><span data-ttu-id="35c6e-526">Summa</span><span class="sxs-lookup"><span data-stu-id="35c6e-526">Amount</span></span></th>
<th><span data-ttu-id="35c6e-527">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="35c6e-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-528">CC002</span><span class="sxs-lookup"><span data-stu-id="35c6e-528">CC002</span></span></td>
<td><span data-ttu-id="35c6e-529">Finantsid</span><span class="sxs-lookup"><span data-stu-id="35c6e-529">Finance</span></span></td>
<td><span data-ttu-id="35c6e-530">35</span><span class="sxs-lookup"><span data-stu-id="35c6e-530">35</span></span></td>
<td><span data-ttu-id="35c6e-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="35c6e-532">175.00</span><span class="sxs-lookup"><span data-stu-id="35c6e-532">175.00</span></span></td>
<td><span data-ttu-id="35c6e-533">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-534">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-534">CC003</span></span></td>
<td><span data-ttu-id="35c6e-535">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-535">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-536">55</span><span class="sxs-lookup"><span data-stu-id="35c6e-536">55</span></span></td>
<td><span data-ttu-id="35c6e-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="35c6e-538">275.00</span><span class="sxs-lookup"><span data-stu-id="35c6e-538">275.00</span></span></td>
<td><span data-ttu-id="35c6e-539">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-540">CC004</span><span class="sxs-lookup"><span data-stu-id="35c6e-540">CC004</span></span></td>
<td><span data-ttu-id="35c6e-541">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="35c6e-541">Packaging</span></span></td>
<td><span data-ttu-id="35c6e-542">10</span><span class="sxs-lookup"><span data-stu-id="35c6e-542">10</span></span></td>
<td><span data-ttu-id="35c6e-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="35c6e-544">50,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-544">50.00</span></span></td>
<td><span data-ttu-id="35c6e-545">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-546">CC002</span><span class="sxs-lookup"><span data-stu-id="35c6e-546">CC002</span></span></td>
<td><span data-ttu-id="35c6e-547">Finantsid</span><span class="sxs-lookup"><span data-stu-id="35c6e-547">Finance</span></span></td>
<td><span data-ttu-id="35c6e-548">35</span><span class="sxs-lookup"><span data-stu-id="35c6e-548">35</span></span></td>
<td><span data-ttu-id="35c6e-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="35c6e-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="35c6e-550">436.00</span><span class="sxs-lookup"><span data-stu-id="35c6e-550">436.00</span></span></td>
<td><span data-ttu-id="35c6e-551">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-552">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-552">CC003</span></span></td>
<td><span data-ttu-id="35c6e-553">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-553">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-554">55</span><span class="sxs-lookup"><span data-stu-id="35c6e-554">55</span></span></td>
<td><span data-ttu-id="35c6e-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="35c6e-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="35c6e-556">685.14</span><span class="sxs-lookup"><span data-stu-id="35c6e-556">685.14</span></span></td>
<td><span data-ttu-id="35c6e-557">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-558">CC004</span><span class="sxs-lookup"><span data-stu-id="35c6e-558">CC004</span></span></td>
<td><span data-ttu-id="35c6e-559">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="35c6e-559">Packaging</span></span></td>
<td><span data-ttu-id="35c6e-560">10</span><span class="sxs-lookup"><span data-stu-id="35c6e-560">10</span></span></td>
<td><span data-ttu-id="35c6e-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="35c6e-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="35c6e-562">124.57</span><span class="sxs-lookup"><span data-stu-id="35c6e-562">124.57</span></span></td>
<td><span data-ttu-id="35c6e-563">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="35c6e-564">Järgmises tabelis on näidatud tulemus, kui Rahandusteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="35c6e-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-565">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-565">Cost object</span></span></th>
<th><span data-ttu-id="35c6e-566">Väärtus</span><span class="sxs-lookup"><span data-stu-id="35c6e-566">Magnitude</span></span></th>
<th><span data-ttu-id="35c6e-567">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="35c6e-567">Allocation factor</span></span></th>
<th><span data-ttu-id="35c6e-568">Summa</span><span class="sxs-lookup"><span data-stu-id="35c6e-568">Amount</span></span></th>
<th><span data-ttu-id="35c6e-569">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="35c6e-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-570">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-570">CC003</span></span></td>
<td><span data-ttu-id="35c6e-571">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-571">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-572">65</span><span class="sxs-lookup"><span data-stu-id="35c6e-572">65</span></span></td>
<td><span data-ttu-id="35c6e-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="35c6e-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="35c6e-574">438.75</span><span class="sxs-lookup"><span data-stu-id="35c6e-574">438.75</span></span></td>
<td><span data-ttu-id="35c6e-575">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-576">CC004</span><span class="sxs-lookup"><span data-stu-id="35c6e-576">CC004</span></span></td>
<td><span data-ttu-id="35c6e-577">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="35c6e-577">Packaging</span></span></td>
<td><span data-ttu-id="35c6e-578">35</span><span class="sxs-lookup"><span data-stu-id="35c6e-578">35</span></span></td>
<td><span data-ttu-id="35c6e-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="35c6e-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="35c6e-580">236.25</span><span class="sxs-lookup"><span data-stu-id="35c6e-580">236.25</span></span></td>
<td><span data-ttu-id="35c6e-581">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-582">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-582">CC003</span></span></td>
<td><span data-ttu-id="35c6e-583">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-583">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-584">65</span><span class="sxs-lookup"><span data-stu-id="35c6e-584">65</span></span></td>
<td><span data-ttu-id="35c6e-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="35c6e-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="35c6e-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="35c6e-586">5,297.69</span></span></td>
<td><span data-ttu-id="35c6e-587">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-588">CC004</span><span class="sxs-lookup"><span data-stu-id="35c6e-588">CC004</span></span></td>
<td><span data-ttu-id="35c6e-589">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="35c6e-589">Packaging</span></span></td>
<td><span data-ttu-id="35c6e-590">35</span><span class="sxs-lookup"><span data-stu-id="35c6e-590">35</span></span></td>
<td><span data-ttu-id="35c6e-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="35c6e-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="35c6e-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="35c6e-592">2,852.60</span></span></td>
<td><span data-ttu-id="35c6e-593">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="35c6e-594">Järgmises tabelis on näidatud tulemus, kui Assembleriteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="35c6e-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-595">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-595">Cost object</span></span></th>
<th><span data-ttu-id="35c6e-596">Väärtus</span><span class="sxs-lookup"><span data-stu-id="35c6e-596">Magnitude</span></span></th>
<th><span data-ttu-id="35c6e-597">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="35c6e-597">Allocation factor</span></span></th>
<th><span data-ttu-id="35c6e-598">Summa</span><span class="sxs-lookup"><span data-stu-id="35c6e-598">Amount</span></span></th>
<th><span data-ttu-id="35c6e-599">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="35c6e-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-600">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-600">Prod 1</span></span></td>
<td><span data-ttu-id="35c6e-601">Toode 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-601">Product 1</span></span></td>
<td><span data-ttu-id="35c6e-602">60</span><span class="sxs-lookup"><span data-stu-id="35c6e-602">60</span></span></td>
<td><span data-ttu-id="35c6e-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="35c6e-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="35c6e-604">535.31</span><span class="sxs-lookup"><span data-stu-id="35c6e-604">535.31</span></span></td>
<td><span data-ttu-id="35c6e-605">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-606">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-606">Prod 2</span></span></td>
<td><span data-ttu-id="35c6e-607">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-607">Product 2</span></span></td>
<td><span data-ttu-id="35c6e-608">20</span><span class="sxs-lookup"><span data-stu-id="35c6e-608">20</span></span></td>
<td><span data-ttu-id="35c6e-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="35c6e-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="35c6e-610">178.44</span><span class="sxs-lookup"><span data-stu-id="35c6e-610">178.44</span></span></td>
<td><span data-ttu-id="35c6e-611">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-612">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-612">Prod 1</span></span></td>
<td><span data-ttu-id="35c6e-613">Toode 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-613">Product 1</span></span></td>
<td><span data-ttu-id="35c6e-614">60</span><span class="sxs-lookup"><span data-stu-id="35c6e-614">60</span></span></td>
<td><span data-ttu-id="35c6e-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="35c6e-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="35c6e-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="35c6e-616">4,487.12</span></span></td>
<td><span data-ttu-id="35c6e-617">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-618">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-618">Prod 2</span></span></td>
<td><span data-ttu-id="35c6e-619">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-619">Product 2</span></span></td>
<td><span data-ttu-id="35c6e-620">20</span><span class="sxs-lookup"><span data-stu-id="35c6e-620">20</span></span></td>
<td><span data-ttu-id="35c6e-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="35c6e-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="35c6e-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="35c6e-622">1,495.71</span></span></td>
<td><span data-ttu-id="35c6e-623">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="35c6e-624">Järgmises tabelis on näidatud tulemus, kui Pakendamisteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="35c6e-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-625">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-625">Cost object</span></span></th>
<th><span data-ttu-id="35c6e-626">Väärtus</span><span class="sxs-lookup"><span data-stu-id="35c6e-626">Magnitude</span></span></th>
<th><span data-ttu-id="35c6e-627">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="35c6e-627">Allocation factor</span></span></th>
<th><span data-ttu-id="35c6e-628">Summa</span><span class="sxs-lookup"><span data-stu-id="35c6e-628">Amount</span></span></th>
<th><span data-ttu-id="35c6e-629">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="35c6e-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-630">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-630">Prod 1</span></span></td>
<td><span data-ttu-id="35c6e-631">Toode 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-631">Product 1</span></span></td>
<td><span data-ttu-id="35c6e-632">80</span><span class="sxs-lookup"><span data-stu-id="35c6e-632">80</span></span></td>
<td><span data-ttu-id="35c6e-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="35c6e-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="35c6e-634">241.05</span><span class="sxs-lookup"><span data-stu-id="35c6e-634">241.05</span></span></td>
<td><span data-ttu-id="35c6e-635">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-636">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-636">Prod 2</span></span></td>
<td><span data-ttu-id="35c6e-637">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-637">Product 2</span></span></td>
<td><span data-ttu-id="35c6e-638">15</span><span class="sxs-lookup"><span data-stu-id="35c6e-638">15</span></span></td>
<td><span data-ttu-id="35c6e-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="35c6e-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="35c6e-640">45.20</span><span class="sxs-lookup"><span data-stu-id="35c6e-640">45.20</span></span></td>
<td><span data-ttu-id="35c6e-641">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-642">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-642">Prod 1</span></span></td>
<td><span data-ttu-id="35c6e-643">Toode 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-643">Product 1</span></span></td>
<td><span data-ttu-id="35c6e-644">80</span><span class="sxs-lookup"><span data-stu-id="35c6e-644">80</span></span></td>
<td><span data-ttu-id="35c6e-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="35c6e-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="35c6e-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="35c6e-646">2,507.09</span></span></td>
<td><span data-ttu-id="35c6e-647">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-648">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-648">Prod 2</span></span></td>
<td><span data-ttu-id="35c6e-649">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-649">Product 2</span></span></td>
<td><span data-ttu-id="35c6e-650">15</span><span class="sxs-lookup"><span data-stu-id="35c6e-650">15</span></span></td>
<td><span data-ttu-id="35c6e-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="35c6e-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="35c6e-652">470.08</span><span class="sxs-lookup"><span data-stu-id="35c6e-652">470.08</span></span></td>
<td><span data-ttu-id="35c6e-653">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="35c6e-654">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="35c6e-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="35c6e-655">Tööleht</span><span class="sxs-lookup"><span data-stu-id="35c6e-655">Journal</span></span></th>
<th><span data-ttu-id="35c6e-656">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="35c6e-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="35c6e-657">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="35c6e-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="35c6e-658">Versioon</span><span class="sxs-lookup"><span data-stu-id="35c6e-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-659">00004</span><span class="sxs-lookup"><span data-stu-id="35c6e-659">00004</span></span></td>
<td><span data-ttu-id="35c6e-660">Kulueralduse tööleht</span><span class="sxs-lookup"><span data-stu-id="35c6e-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="35c6e-661">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="35c6e-661">Fiscal</span></span></td>
<td><span data-ttu-id="35c6e-662">2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-662">2017</span></span></td>
<td><span data-ttu-id="35c6e-663">Periood 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-663">Period 1</span></span></td>
<td><span data-ttu-id="35c6e-664">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="35c6e-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="35c6e-665">Töölehe read</span><span class="sxs-lookup"><span data-stu-id="35c6e-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="35c6e-666">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="35c6e-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="35c6e-667">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="35c6e-668">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="35c6e-668">Cost element</span></span></th>
<th><span data-ttu-id="35c6e-669">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="35c6e-669">Cost behavior</span></span></th>
<th><span data-ttu-id="35c6e-670">Summa</span><span class="sxs-lookup"><span data-stu-id="35c6e-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-671">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="35c6e-672">CC001</span><span class="sxs-lookup"><span data-stu-id="35c6e-672">CC001</span></span></td>
<td><span data-ttu-id="35c6e-673">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="35c6e-673">HR</span></span></td>
<td><span data-ttu-id="35c6e-674">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-674">10001</span></span></td>
<td><span data-ttu-id="35c6e-675">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-675">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-676">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-676">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-677">500,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-678">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="35c6e-679">CC001</span><span class="sxs-lookup"><span data-stu-id="35c6e-679">CC001</span></span></td>
<td><span data-ttu-id="35c6e-680">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="35c6e-680">HR</span></span></td>
<td><span data-ttu-id="35c6e-681">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-681">10001</span></span></td>
<td><span data-ttu-id="35c6e-682">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-682">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-683">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-683">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="35c6e-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-685">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="35c6e-686">CC002</span><span class="sxs-lookup"><span data-stu-id="35c6e-686">CC002</span></span></td>
<td><span data-ttu-id="35c6e-687">Finantsid</span><span class="sxs-lookup"><span data-stu-id="35c6e-687">Finance</span></span></td>
<td><span data-ttu-id="35c6e-688">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-688">10001</span></span></td>
<td><span data-ttu-id="35c6e-689">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-689">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-690">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-690">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-691">675.00</span><span class="sxs-lookup"><span data-stu-id="35c6e-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-692">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="35c6e-693">CC002</span><span class="sxs-lookup"><span data-stu-id="35c6e-693">CC002</span></span></td>
<td><span data-ttu-id="35c6e-694">Finantsid</span><span class="sxs-lookup"><span data-stu-id="35c6e-694">Finance</span></span></td>
<td><span data-ttu-id="35c6e-695">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-695">10001</span></span></td>
<td><span data-ttu-id="35c6e-696">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-696">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-697">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-697">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="35c6e-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-699">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="35c6e-700">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-700">CC003</span></span></td>
<td><span data-ttu-id="35c6e-701">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-701">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-702">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-702">10001</span></span></td>
<td><span data-ttu-id="35c6e-703">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-703">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-704">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-704">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-705">713.75</span><span class="sxs-lookup"><span data-stu-id="35c6e-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-706">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="35c6e-707">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-707">CC003</span></span></td>
<td><span data-ttu-id="35c6e-708">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-708">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-709">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-709">10001</span></span></td>
<td><span data-ttu-id="35c6e-710">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-710">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-711">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-711">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="35c6e-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-713">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="35c6e-714">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-714">CC003</span></span></td>
<td><span data-ttu-id="35c6e-715">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="35c6e-715">Packaging</span></span></td>
<td><span data-ttu-id="35c6e-716">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-716">10001</span></span></td>
<td><span data-ttu-id="35c6e-717">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-717">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-718">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-718">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-719">286.25</span><span class="sxs-lookup"><span data-stu-id="35c6e-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-720">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="35c6e-721">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-721">CC003</span></span></td>
<td><span data-ttu-id="35c6e-722">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="35c6e-722">Packaging</span></span></td>
<td><span data-ttu-id="35c6e-723">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-723">10001</span></span></td>
<td><span data-ttu-id="35c6e-724">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-724">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-725">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-725">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="35c6e-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-727">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="35c6e-728">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-728">Prod 1</span></span></td>
<td><span data-ttu-id="35c6e-729">Toode 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-729">Product 1</span></span></td>
<td><span data-ttu-id="35c6e-730">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-730">10001</span></span></td>
<td><span data-ttu-id="35c6e-731">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-731">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-732">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-732">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-733">776.36</span><span class="sxs-lookup"><span data-stu-id="35c6e-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-734">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="35c6e-735">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-735">Prod 1</span></span></td>
<td><span data-ttu-id="35c6e-736">Toode 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-736">Product 1</span></span></td>
<td><span data-ttu-id="35c6e-737">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-737">10001</span></span></td>
<td><span data-ttu-id="35c6e-738">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-738">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-739">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-739">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="35c6e-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-741">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="35c6e-742">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-742">Prod 2</span></span></td>
<td><span data-ttu-id="35c6e-743">Toode 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-743">Product 1</span></span></td>
<td><span data-ttu-id="35c6e-744">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-744">10001</span></span></td>
<td><span data-ttu-id="35c6e-745">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-745">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-746">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-746">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-747">223.64</span><span class="sxs-lookup"><span data-stu-id="35c6e-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-748">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="35c6e-749">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-749">Prod 2</span></span></td>
<td><span data-ttu-id="35c6e-750">Toode 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-750">Product 1</span></span></td>
<td><span data-ttu-id="35c6e-751">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-751">10001</span></span></td>
<td><span data-ttu-id="35c6e-752">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-752">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-753">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-753">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="35c6e-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="35c6e-755">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="35c6e-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="35c6e-756">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="35c6e-757">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="35c6e-757">Cost element</span></span></th>
<th><span data-ttu-id="35c6e-758">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="35c6e-758">Cost behavior</span></span></th>
<th><span data-ttu-id="35c6e-759">Summa</span><span class="sxs-lookup"><span data-stu-id="35c6e-759">Amount</span></span></th>
<th><span data-ttu-id="35c6e-760">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="35c6e-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="35c6e-761">CC001</span><span class="sxs-lookup"><span data-stu-id="35c6e-761">CC001</span></span></td>
<td><span data-ttu-id="35c6e-762">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="35c6e-762">HR</span></span></td>
<td><span data-ttu-id="35c6e-763">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-763">10001</span></span></td>
<td><span data-ttu-id="35c6e-764">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-764">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-765">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-765">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-766">‑500,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-766">-500.00</span></span></td>
<td><span data-ttu-id="35c6e-767">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-768">CC002</span><span class="sxs-lookup"><span data-stu-id="35c6e-768">CC002</span></span></td>
<td><span data-ttu-id="35c6e-769">Finantsid</span><span class="sxs-lookup"><span data-stu-id="35c6e-769">Finance</span></span></td>
<td><span data-ttu-id="35c6e-770">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-770">10001</span></span></td>
<td><span data-ttu-id="35c6e-771">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-771">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-772">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-772">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-773">175.00</span><span class="sxs-lookup"><span data-stu-id="35c6e-773">175.00</span></span></td>
<td><span data-ttu-id="35c6e-774">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-775">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-775">CC003</span></span></td>
<td><span data-ttu-id="35c6e-776">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-776">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-777">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-777">10001</span></span></td>
<td><span data-ttu-id="35c6e-778">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-778">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-779">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-779">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-780">275.00</span><span class="sxs-lookup"><span data-stu-id="35c6e-780">275.00</span></span></td>
<td><span data-ttu-id="35c6e-781">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-782">CC004</span><span class="sxs-lookup"><span data-stu-id="35c6e-782">CC004</span></span></td>
<td><span data-ttu-id="35c6e-783">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="35c6e-783">Packaging</span></span></td>
<td><span data-ttu-id="35c6e-784">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-784">10001</span></span></td>
<td><span data-ttu-id="35c6e-785">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-785">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-786">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-786">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-787">50,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-787">50,00</span></span></td>
<td><span data-ttu-id="35c6e-788">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-789">CC001</span><span class="sxs-lookup"><span data-stu-id="35c6e-789">CC001</span></span></td>
<td><span data-ttu-id="35c6e-790">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="35c6e-790">HR</span></span></td>
<td><span data-ttu-id="35c6e-791">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-791">10001</span></span></td>
<td><span data-ttu-id="35c6e-792">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-792">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-793">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-793">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-794">–1245,71</span><span class="sxs-lookup"><span data-stu-id="35c6e-794">-1,245.71</span></span></td>
<td><span data-ttu-id="35c6e-795">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-796">CC002</span><span class="sxs-lookup"><span data-stu-id="35c6e-796">CC002</span></span></td>
<td><span data-ttu-id="35c6e-797">Finantsid</span><span class="sxs-lookup"><span data-stu-id="35c6e-797">Finance</span></span></td>
<td><span data-ttu-id="35c6e-798">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-798">10001</span></span></td>
<td><span data-ttu-id="35c6e-799">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-799">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-800">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-800">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-801">436.00</span><span class="sxs-lookup"><span data-stu-id="35c6e-801">436.00</span></span></td>
<td><span data-ttu-id="35c6e-802">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-803">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-803">CC003</span></span></td>
<td><span data-ttu-id="35c6e-804">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-804">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-805">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-805">10001</span></span></td>
<td><span data-ttu-id="35c6e-806">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-806">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-807">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-807">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-808">685.14</span><span class="sxs-lookup"><span data-stu-id="35c6e-808">685.14</span></span></td>
<td><span data-ttu-id="35c6e-809">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-810">CC004</span><span class="sxs-lookup"><span data-stu-id="35c6e-810">CC004</span></span></td>
<td><span data-ttu-id="35c6e-811">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="35c6e-811">Packaging</span></span></td>
<td><span data-ttu-id="35c6e-812">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-812">10001</span></span></td>
<td><span data-ttu-id="35c6e-813">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-813">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-814">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-814">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-815">124.57</span><span class="sxs-lookup"><span data-stu-id="35c6e-815">124.57</span></span></td>
<td><span data-ttu-id="35c6e-816">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-817">CC002</span><span class="sxs-lookup"><span data-stu-id="35c6e-817">CC002</span></span></td>
<td><span data-ttu-id="35c6e-818">Finantsid</span><span class="sxs-lookup"><span data-stu-id="35c6e-818">Finance</span></span></td>
<td><span data-ttu-id="35c6e-819">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-819">10001</span></span></td>
<td><span data-ttu-id="35c6e-820">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-820">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-821">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-821">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-822">–675,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-822">-675.00</span></span></td>
<td><span data-ttu-id="35c6e-823">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-824">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-824">CC003</span></span></td>
<td><span data-ttu-id="35c6e-825">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-825">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-826">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-826">10001</span></span></td>
<td><span data-ttu-id="35c6e-827">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-827">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-828">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-828">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-829">438.75</span><span class="sxs-lookup"><span data-stu-id="35c6e-829">438.75</span></span></td>
<td><span data-ttu-id="35c6e-830">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-831">CC004</span><span class="sxs-lookup"><span data-stu-id="35c6e-831">CC004</span></span></td>
<td><span data-ttu-id="35c6e-832">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="35c6e-832">Packaging</span></span></td>
<td><span data-ttu-id="35c6e-833">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-833">10001</span></span></td>
<td><span data-ttu-id="35c6e-834">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-834">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-835">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-835">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-836">236.25</span><span class="sxs-lookup"><span data-stu-id="35c6e-836">236.25</span></span></td>
<td><span data-ttu-id="35c6e-837">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-838">CC002</span><span class="sxs-lookup"><span data-stu-id="35c6e-838">CC002</span></span></td>
<td><span data-ttu-id="35c6e-839">Finantsid</span><span class="sxs-lookup"><span data-stu-id="35c6e-839">Finance</span></span></td>
<td><span data-ttu-id="35c6e-840">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-840">10001</span></span></td>
<td><span data-ttu-id="35c6e-841">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-841">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-842">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-842">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-843">–8150,29</span><span class="sxs-lookup"><span data-stu-id="35c6e-843">-8,150.29</span></span></td>
<td><span data-ttu-id="35c6e-844">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-845">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-845">CC003</span></span></td>
<td><span data-ttu-id="35c6e-846">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-846">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-847">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-847">10001</span></span></td>
<td><span data-ttu-id="35c6e-848">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-848">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-849">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-849">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="35c6e-850">5,297.69</span></span></td>
<td><span data-ttu-id="35c6e-851">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-852">CC004</span><span class="sxs-lookup"><span data-stu-id="35c6e-852">CC004</span></span></td>
<td><span data-ttu-id="35c6e-853">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="35c6e-853">Packaging</span></span></td>
<td><span data-ttu-id="35c6e-854">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-854">10001</span></span></td>
<td><span data-ttu-id="35c6e-855">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-855">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-856">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-856">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="35c6e-857">2,852.60</span></span></td>
<td><span data-ttu-id="35c6e-858">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-859">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-859">CC003</span></span></td>
<td><span data-ttu-id="35c6e-860">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-860">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-861">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-861">10001</span></span></td>
<td><span data-ttu-id="35c6e-862">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-862">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-863">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-863">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-864">–713,75</span><span class="sxs-lookup"><span data-stu-id="35c6e-864">-713.75</span></span></td>
<td><span data-ttu-id="35c6e-865">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-866">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-866">Prod 1</span></span></td>
<td><span data-ttu-id="35c6e-867">Toode 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-867">Product 1</span></span></td>
<td><span data-ttu-id="35c6e-868">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-868">10001</span></span></td>
<td><span data-ttu-id="35c6e-869">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-869">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-870">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-870">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-871">535.31</span><span class="sxs-lookup"><span data-stu-id="35c6e-871">535.31</span></span></td>
<td><span data-ttu-id="35c6e-872">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-873">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-873">Prod 2</span></span></td>
<td><span data-ttu-id="35c6e-874">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-874">Product 2</span></span></td>
<td><span data-ttu-id="35c6e-875">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-875">10001</span></span></td>
<td><span data-ttu-id="35c6e-876">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-876">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-877">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-877">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-878">178.44</span><span class="sxs-lookup"><span data-stu-id="35c6e-878">178.44</span></span></td>
<td><span data-ttu-id="35c6e-879">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-880">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-880">CC003</span></span></td>
<td><span data-ttu-id="35c6e-881">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-881">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-882">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-882">10001</span></span></td>
<td><span data-ttu-id="35c6e-883">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-883">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-884">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-884">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-885">–5982,83</span><span class="sxs-lookup"><span data-stu-id="35c6e-885">-5,982.83</span></span></td>
<td><span data-ttu-id="35c6e-886">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-887">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-887">Prod 1</span></span></td>
<td><span data-ttu-id="35c6e-888">Toode 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-888">Product 1</span></span></td>
<td><span data-ttu-id="35c6e-889">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-889">10001</span></span></td>
<td><span data-ttu-id="35c6e-890">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-890">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-891">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-891">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="35c6e-892">4,487.12</span></span></td>
<td><span data-ttu-id="35c6e-893">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-894">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-894">Prod 2</span></span></td>
<td><span data-ttu-id="35c6e-895">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-895">Product 2</span></span></td>
<td><span data-ttu-id="35c6e-896">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-896">10001</span></span></td>
<td><span data-ttu-id="35c6e-897">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-897">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-898">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-898">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="35c6e-899">1,495.71</span></span></td>
<td><span data-ttu-id="35c6e-900">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-901">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-901">CC003</span></span></td>
<td><span data-ttu-id="35c6e-902">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-902">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-903">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-903">10001</span></span></td>
<td><span data-ttu-id="35c6e-904">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-904">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-905">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-905">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-906">–286,25</span><span class="sxs-lookup"><span data-stu-id="35c6e-906">-286.25</span></span></td>
<td><span data-ttu-id="35c6e-907">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-908">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-908">Prod 1</span></span></td>
<td><span data-ttu-id="35c6e-909">Toode 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-909">Product 1</span></span></td>
<td><span data-ttu-id="35c6e-910">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-910">10001</span></span></td>
<td><span data-ttu-id="35c6e-911">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-911">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-912">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-912">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-913">241.05</span><span class="sxs-lookup"><span data-stu-id="35c6e-913">241.05</span></span></td>
<td><span data-ttu-id="35c6e-914">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-915">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-915">Prod 2</span></span></td>
<td><span data-ttu-id="35c6e-916">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-916">Product 2</span></span></td>
<td><span data-ttu-id="35c6e-917">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-917">10001</span></span></td>
<td><span data-ttu-id="35c6e-918">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-918">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-919">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-919">Fixed cost</span></span></td>
<td><span data-ttu-id="35c6e-920">45.20</span><span class="sxs-lookup"><span data-stu-id="35c6e-920">45.20</span></span></td>
<td><span data-ttu-id="35c6e-921">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-922">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-922">CC003</span></span></td>
<td><span data-ttu-id="35c6e-923">Assembler</span><span class="sxs-lookup"><span data-stu-id="35c6e-923">Assembly</span></span></td>
<td><span data-ttu-id="35c6e-924">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-924">10001</span></span></td>
<td><span data-ttu-id="35c6e-925">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-925">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-926">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-926">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-927">–2977,17</span><span class="sxs-lookup"><span data-stu-id="35c6e-927">-2,977.17</span></span></td>
<td><span data-ttu-id="35c6e-928">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-929">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-929">Prod 1</span></span></td>
<td><span data-ttu-id="35c6e-930">Toode 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-930">Product 1</span></span></td>
<td><span data-ttu-id="35c6e-931">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-931">10001</span></span></td>
<td><span data-ttu-id="35c6e-932">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-932">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-933">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-933">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="35c6e-934">2,507.09</span></span></td>
<td><span data-ttu-id="35c6e-935">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="35c6e-936">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-936">Prod 2</span></span></td>
<td><span data-ttu-id="35c6e-937">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-937">Product 2</span></span></td>
<td><span data-ttu-id="35c6e-938">10001</span><span class="sxs-lookup"><span data-stu-id="35c6e-938">10001</span></span></td>
<td><span data-ttu-id="35c6e-939">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="35c6e-939">Electricity</span></span></td>
<td><span data-ttu-id="35c6e-940">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-940">Variable cost</span></span></td>
<td><span data-ttu-id="35c6e-941">470.08</span><span class="sxs-lookup"><span data-stu-id="35c6e-941">470.08</span></span></td>
<td><span data-ttu-id="35c6e-942">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="35c6e-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="35c6e-943">Lõppsõna</span><span class="sxs-lookup"><span data-stu-id="35c6e-943">Conclusion</span></span>
<span data-ttu-id="35c6e-944">Finantsaruandluses sisestatakse elektrikulu 10 000,00 fiktiivse kulukeskuse ID-le.</span><span class="sxs-lookup"><span data-stu-id="35c6e-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="35c6e-945">Nii teavad kuluarvestajad, et see kulu tuleb eraldada.</span><span class="sxs-lookup"><span data-stu-id="35c6e-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="35c6e-946">Kuluarvestuses liigub kulu rakendatud poliitikate ja reeglite põhjal läbi organisatsiooniüksuste ja -tasemete.</span><span class="sxs-lookup"><span data-stu-id="35c6e-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="35c6e-947">Iga kulu on seostatud eraldamisalusega, mis pakub kulude eraldamiseks parimat hinnangut.</span><span class="sxs-lookup"><span data-stu-id="35c6e-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="35c6e-948">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="35c6e-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="35c6e-949">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="35c6e-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="35c6e-950">Kokku</span><span class="sxs-lookup"><span data-stu-id="35c6e-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="35c6e-951">CC099</span><span class="sxs-lookup"><span data-stu-id="35c6e-951">CC099</span></span></th>
<th><span data-ttu-id="35c6e-952">CC001</span><span class="sxs-lookup"><span data-stu-id="35c6e-952">CC001</span></span></th>
<th><span data-ttu-id="35c6e-953">CC002</span><span class="sxs-lookup"><span data-stu-id="35c6e-953">CC002</span></span></th>
<th><span data-ttu-id="35c6e-954">CC003</span><span class="sxs-lookup"><span data-stu-id="35c6e-954">CC003</span></span></th>
<th><span data-ttu-id="35c6e-955">CC004</span><span class="sxs-lookup"><span data-stu-id="35c6e-955">CC004</span></span></th>
<th><span data-ttu-id="35c6e-956">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-956">Proj 1</span></span></th>
<th><span data-ttu-id="35c6e-957">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-957">Proj 2</span></span></th>
<th><span data-ttu-id="35c6e-958">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="35c6e-958">Prod 1</span></span></th>
<th><span data-ttu-id="35c6e-959">Toode 2</span><span class="sxs-lookup"><span data-stu-id="35c6e-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="35c6e-960">10001 Elekter</span><span class="sxs-lookup"><span data-stu-id="35c6e-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="35c6e-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="35c6e-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="35c6e-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="35c6e-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="35c6e-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="35c6e-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="35c6e-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="35c6e-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="35c6e-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="35c6e-970">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="35c6e-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-971">0,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="35c6e-972">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-973">0,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-974">0,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-975">0,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-976">0,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-977">0,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-978">776.36</span><span class="sxs-lookup"><span data-stu-id="35c6e-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-979">223.64</span><span class="sxs-lookup"><span data-stu-id="35c6e-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="35c6e-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="35c6e-981">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="35c6e-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-982">000</span><span class="sxs-lookup"><span data-stu-id="35c6e-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-983">0,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-984">0,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-985">0,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-986">0,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-987">30,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-988">10,00</span><span class="sxs-lookup"><span data-stu-id="35c6e-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="35c6e-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="35c6e-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="35c6e-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="35c6e-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="35c6e-992">Selles teemas selgitatakse, kuidas esmane kuluelement, 10001 Eleter, liigub läbi kuluobjektide.</span><span class="sxs-lookup"><span data-stu-id="35c6e-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="35c6e-993">Seega eraldatakse see üldkulu organisatsiooni madalaimale tasemele.</span><span class="sxs-lookup"><span data-stu-id="35c6e-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="35c6e-994">Teisisõnu kannavad kulu madalaimal tasemel olevad kuluobjektid.</span><span class="sxs-lookup"><span data-stu-id="35c6e-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="35c6e-995">Kui soovite saada kuluobjektide vahelisest kuluvoost visuaalset ülevaadet, saate kuluvoo visualiseerimiseks kasutada kulude kokkuvõtte poliitika reegleid.</span><span class="sxs-lookup"><span data-stu-id="35c6e-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="35c6e-996">Lisateavet vt teemast [Kulukomplekti poliitika ja üldkulude arvutus](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="35c6e-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



