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
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 936e54c0ef1de449afda2392cd1fbb304eed631b
ms.contentlocale: et-ee
ms.lasthandoff: 01/17/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="c1de1-103">Üldkulude arvutus</span><span class="sxs-lookup"><span data-stu-id="c1de1-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c1de1-104">Selles teemas kirjeldatakse tüüpilisi üldkulude arvutamise ja eraldamise protsesse.</span><span class="sxs-lookup"><span data-stu-id="c1de1-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="c1de1-105">Mõiste määratlus</span><span class="sxs-lookup"><span data-stu-id="c1de1-105">Term definition</span></span>
---------------

<span data-ttu-id="c1de1-106">Üldkulud on kulud, mis kaasnevad ettevõtte käitamisega, kuid mida ei saa seostada otseselt ühegi kindla äritegevuse, toote ega teenusega.</span><span class="sxs-lookup"><span data-stu-id="c1de1-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="c1de1-107">Üldkulud pakuvad kriitilist tuge kasumit andavate tegevuste loomisele.</span><span class="sxs-lookup"><span data-stu-id="c1de1-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="c1de1-108">Siin on mõned näited üldkuludest.</span><span class="sxs-lookup"><span data-stu-id="c1de1-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="c1de1-109">Üür</span><span class="sxs-lookup"><span data-stu-id="c1de1-109">Rent</span></span>
-   <span data-ttu-id="c1de1-110">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-110">Electricity</span></span>
-   <span data-ttu-id="c1de1-111">Haldustasud</span><span class="sxs-lookup"><span data-stu-id="c1de1-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="c1de1-112">Üldkulude arvutuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="c1de1-112">Overhead calculation overview</span></span>
<span data-ttu-id="c1de1-113">Üldkulude arvutus käitab kuluarvutuse poliitikaid õiges järjekorras.</span><span class="sxs-lookup"><span data-stu-id="c1de1-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="c1de1-114">Saate käivitada üldkulude arvutuse sama rahandusperioodi kohta mitu korda, kui kuluarvestuse poliitikaid on muudetud või tuvastatud teatud tõrked.</span><span class="sxs-lookup"><span data-stu-id="c1de1-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="c1de1-115">Iga üldkulude arvutamise käitamine talletatakse ja see saab kordumatu versiooni-ID, mis võimaldab teil arvutuste erinevaid versioone võrrelda.</span><span class="sxs-lookup"><span data-stu-id="c1de1-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="c1de1-116">Ülekulude arvutusega loodud kulukirjed saavad aruandluskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="c1de1-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="c1de1-117">See aruandluskuupäev vastab arvutuses kasutatud rahandusperioodi lõppkuupäevale.</span><span class="sxs-lookup"><span data-stu-id="c1de1-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="c1de1-118">Kordumatu versiooni-ID koosneb järgmistest elementidest.</span><span class="sxs-lookup"><span data-stu-id="c1de1-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="c1de1-119">Versiooni tüüp</span><span class="sxs-lookup"><span data-stu-id="c1de1-119">Version type</span></span>
-   <span data-ttu-id="c1de1-120">Kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="c1de1-120">Date and time</span></span>
-   <span data-ttu-id="c1de1-121">Kuluarvestuse pearaamat</span><span class="sxs-lookup"><span data-stu-id="c1de1-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="c1de1-122">Finantsaasta</span><span class="sxs-lookup"><span data-stu-id="c1de1-122">Fiscal year</span></span>
-   <span data-ttu-id="c1de1-123">Rahandusperiood</span><span class="sxs-lookup"><span data-stu-id="c1de1-123">Fiscal period</span></span>

<span data-ttu-id="c1de1-124">Üldkulude arvutus käivitatakse versioonist sõltumatult.</span><span class="sxs-lookup"><span data-stu-id="c1de1-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="c1de1-125">Seetõttu saate arvutada eelarveversiooni enne tegelikku versiooni.</span><span class="sxs-lookup"><span data-stu-id="c1de1-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="c1de1-126">Üldkulude arvutus koosneb neljast etapist, nagu näha alltoodud joonisel.</span><span class="sxs-lookup"><span data-stu-id="c1de1-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="c1de1-127">Igas etapis luuakse töölehe päis, millel on töölehe kanded.</span><span class="sxs-lookup"><span data-stu-id="c1de1-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="c1de1-128">See töölehe päis säiiltab sisendandmeid iga arvutusetapi kohta.</span><span class="sxs-lookup"><span data-stu-id="c1de1-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="c1de1-129">Igale töölehe reale rakendatakse poliitikad ja reeglid ning väljundina luuakse kulukirjed.</span><span class="sxs-lookup"><span data-stu-id="c1de1-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="c1de1-130">Seega on teil alati olemas põhjalik ülevaade.</span><span class="sxs-lookup"><span data-stu-id="c1de1-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="c1de1-131">[![Üldkulude arvutus](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="c1de1-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="c1de1-132">Elektri üldkulude arvutamine ja eraldamine</span><span class="sxs-lookup"><span data-stu-id="c1de1-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="c1de1-133">Finantsaruandluses on mõned kulud, näiteks elekter, registreeritud põhisummana.</span><span class="sxs-lookup"><span data-stu-id="c1de1-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="c1de1-134">Seetõttu ei pakuta kuluarvestuseks üksikasjalikku juhtimisülevaadet.</span><span class="sxs-lookup"><span data-stu-id="c1de1-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="c1de1-135">Kuluarvestuses peavad kulud liikuma läbi organisatsiooniüksuste, et pakkuda korrektset juhtimisülevaadet kõigi organisatsiooniüksuste ja -tasemete kohta.</span><span class="sxs-lookup"><span data-stu-id="c1de1-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="c1de1-136">See voog peab põhinema tarbimise või õiglase hindamise täpsel kirjendamisel.</span><span class="sxs-lookup"><span data-stu-id="c1de1-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="c1de1-137">Pearaamatus, saab elektrikulu sisestada nii, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="c1de1-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c1de1-138">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="c1de1-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c1de1-139">Kulukeskus</span><span class="sxs-lookup"><span data-stu-id="c1de1-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="c1de1-140">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="c1de1-140">Main account</span></span></th>
<th><span data-ttu-id="c1de1-141">Summa arvestusvaluutas</span><span class="sxs-lookup"><span data-stu-id="c1de1-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-142">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="c1de1-143">CC099</span><span class="sxs-lookup"><span data-stu-id="c1de1-143">CC099</span></span></td>
<td><span data-ttu-id="c1de1-144">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="c1de1-144">Default cost center</span></span></td>
<td><span data-ttu-id="c1de1-145">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-145">10001</span></span></td>
<td><span data-ttu-id="c1de1-146">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-146">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c1de1-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="c1de1-148">1. etapp: kulukäitumise arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="c1de1-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="c1de1-149">Vaikimisi saavad lähteandmetest imporditud kulukirjed kuluarvestuses kulukäitumise klassifikatsiooniks **Klassifitseerimata**.</span><span class="sxs-lookup"><span data-stu-id="c1de1-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="c1de1-150">Kulukäitumise poliitikareegleid rakendades saate kulukirjed ümber klassifitseerida kui **Fikseeritud kulu** või **Muutuvkulu**.</span><span class="sxs-lookup"><span data-stu-id="c1de1-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="c1de1-151">Kulukäitumise reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="c1de1-151">Define the cost behavior rule</span></span>

<span data-ttu-id="c1de1-152">Mõnikord on osa kulust fikseeritud tasu ja järelejäänud kulu põhineb tarbimisel.</span><span class="sxs-lookup"><span data-stu-id="c1de1-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="c1de1-153">Elektriarved vastavad sageli sellele määratlusele.</span><span class="sxs-lookup"><span data-stu-id="c1de1-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="c1de1-154">Pärast kindla fikseeritud tasu maksmist maksate tarbimise eest kilovatt-tunni (Kwh) kohta.</span><span class="sxs-lookup"><span data-stu-id="c1de1-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="c1de1-155">Näiteks kui fikseeritud kulu tasu on 1000,00 eurot, määratletakse kulukäitumise reegel järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="c1de1-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="c1de1-156">Fikseeritud summa: 1000,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="c1de1-157">0 &lt;= 1000,00 = fikseeritud</span><span class="sxs-lookup"><span data-stu-id="c1de1-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="c1de1-158">1000,01 &lt; N = muutuja</span><span class="sxs-lookup"><span data-stu-id="c1de1-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="c1de1-159">Tööleht</span><span class="sxs-lookup"><span data-stu-id="c1de1-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c1de1-160">Tööleht</span><span class="sxs-lookup"><span data-stu-id="c1de1-160">Journal</span></span></th>
<th><span data-ttu-id="c1de1-161">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="c1de1-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c1de1-162">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="c1de1-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c1de1-163">Versioon</span><span class="sxs-lookup"><span data-stu-id="c1de1-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-164">00001</span><span class="sxs-lookup"><span data-stu-id="c1de1-164">00001</span></span></td>
<td><span data-ttu-id="c1de1-165">Kulukäitumise arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="c1de1-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="c1de1-166">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="c1de1-166">Fiscal</span></span></td>
<td><span data-ttu-id="c1de1-167">2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-167">2017</span></span></td>
<td><span data-ttu-id="c1de1-168">Periood 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-168">Period 1</span></span></td>
<td><span data-ttu-id="c1de1-169">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="c1de1-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c1de1-170">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="c1de1-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c1de1-171">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="c1de1-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c1de1-172">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c1de1-173">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="c1de1-173">Cost element</span></span></th>
<th><span data-ttu-id="c1de1-174">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="c1de1-174">Cost behavior</span></span></th>
<th><span data-ttu-id="c1de1-175">Summa</span><span class="sxs-lookup"><span data-stu-id="c1de1-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-176">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="c1de1-177">CC099</span><span class="sxs-lookup"><span data-stu-id="c1de1-177">CC099</span></span></td>
<td><span data-ttu-id="c1de1-178">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="c1de1-178">Default cost center</span></span></td>
<td><span data-ttu-id="c1de1-179">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-179">10001</span></span></td>
<td><span data-ttu-id="c1de1-180">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-180">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-181">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="c1de1-181">Unclassified</span></span></td>
<td><span data-ttu-id="c1de1-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c1de1-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c1de1-183">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="c1de1-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-184">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c1de1-185">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="c1de1-185">Cost element</span></span></th>
<th><span data-ttu-id="c1de1-186">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="c1de1-186">Cost behavior</span></span></th>
<th><span data-ttu-id="c1de1-187">Summa</span><span class="sxs-lookup"><span data-stu-id="c1de1-187">Amount</span></span></th>
<th><span data-ttu-id="c1de1-188">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="c1de1-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-189">CC099</span><span class="sxs-lookup"><span data-stu-id="c1de1-189">CC099</span></span></td>
<td><span data-ttu-id="c1de1-190">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="c1de1-190">Default cost center</span></span></td>
<td><span data-ttu-id="c1de1-191">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-191">10001</span></span></td>
<td><span data-ttu-id="c1de1-192">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-192">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-193">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="c1de1-193">Unclassified</span></span></td>
<td><span data-ttu-id="c1de1-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c1de1-194">10,000.00</span></span></td>
<td><span data-ttu-id="c1de1-195">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-196">CC099</span><span class="sxs-lookup"><span data-stu-id="c1de1-196">CC099</span></span></td>
<td><span data-ttu-id="c1de1-197">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="c1de1-197">Default cost center</span></span></td>
<td><span data-ttu-id="c1de1-198">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-198">10001</span></span></td>
<td><span data-ttu-id="c1de1-199">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-199">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-200">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="c1de1-200">Unclassified</span></span></td>
<td><span data-ttu-id="c1de1-201">–10 000,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-201">-10,000.00</span></span></td>
<td><span data-ttu-id="c1de1-202">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-203">CC099</span><span class="sxs-lookup"><span data-stu-id="c1de1-203">CC099</span></span></td>
<td><span data-ttu-id="c1de1-204">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="c1de1-204">Default cost center</span></span></td>
<td><span data-ttu-id="c1de1-205">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-205">10001</span></span></td>
<td><span data-ttu-id="c1de1-206">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-206">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-207">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-207">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-208">1,000.00</span></span></td>
<td><span data-ttu-id="c1de1-209">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-210">CC099</span><span class="sxs-lookup"><span data-stu-id="c1de1-210">CC099</span></span></td>
<td><span data-ttu-id="c1de1-211">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="c1de1-211">Default cost center</span></span></td>
<td><span data-ttu-id="c1de1-212">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-212">10001</span></span></td>
<td><span data-ttu-id="c1de1-213">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-213">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-214">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-214">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="c1de1-215">9,000.00</span></span></td>
<td><span data-ttu-id="c1de1-216">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c1de1-217">Üksikasjalikku teavet kulukäitumise kohta vt jaotisest Kulukäitumise poliitika.</span><span class="sxs-lookup"><span data-stu-id="c1de1-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="c1de1-218">(Pange tähele, et see teema pole veel valmis, kuid see tuleb peagi.)</span><span class="sxs-lookup"><span data-stu-id="c1de1-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="c1de1-219">2. etapp: kulujaotuse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="c1de1-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="c1de1-220">Kulujaotust kasutatakse kulu ümberjaotamiseks ühelt kuluobjektilt ühele või mitmele teisele kuluobjektile, rakendades asjakohast eraldusalust.</span><span class="sxs-lookup"><span data-stu-id="c1de1-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="c1de1-221">Kulujaotus ja kulueraldus erinevad selle poolest, et kulujaotus toimub alati algse kulu esmase kuluelemendi tasemel.</span><span class="sxs-lookup"><span data-stu-id="c1de1-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="c1de1-222">Kulujaotuse reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="c1de1-222">Define the cost distribution rule</span></span>

<span data-ttu-id="c1de1-223">Finantsaruandluses registreeritakse elektrikulud sageli põhisummana.</span><span class="sxs-lookup"><span data-stu-id="c1de1-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="c1de1-224">Kuluarvestuseses ei ole see lähenemine piisavalt üksikasjalik.</span><span class="sxs-lookup"><span data-stu-id="c1de1-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="c1de1-225">Muutuvkulu tuleb jaotada üksikutele kuluobjektidele õigluse alusel.</span><span class="sxs-lookup"><span data-stu-id="c1de1-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="c1de1-226">Kõige loogilisem eraldamisalus on elektritarbimine (kWh).</span><span class="sxs-lookup"><span data-stu-id="c1de1-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="c1de1-227">Luuakse statistilise dimensiooni liige nimega Elekter ja elektritarbimine on kirjendatakse.</span><span class="sxs-lookup"><span data-stu-id="c1de1-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="c1de1-228">Vaikimisi muutuvad kõik statistilise dimensiooni liikmed eraldamisalusena kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="c1de1-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-229">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-229">Cost object</span></span></th>
<th><span data-ttu-id="c1de1-230">kWh</span><span class="sxs-lookup"><span data-stu-id="c1de1-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-231">CC001</span><span class="sxs-lookup"><span data-stu-id="c1de1-231">CC001</span></span></td>
<td><span data-ttu-id="c1de1-232">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="c1de1-232">HR</span></span></td>
<td><span data-ttu-id="c1de1-233">1000</span><span class="sxs-lookup"><span data-stu-id="c1de1-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-234">CC002</span><span class="sxs-lookup"><span data-stu-id="c1de1-234">CC002</span></span></td>
<td><span data-ttu-id="c1de1-235">Finantsid</span><span class="sxs-lookup"><span data-stu-id="c1de1-235">Finance</span></span></td>
<td><span data-ttu-id="c1de1-236">6,000</span><span class="sxs-lookup"><span data-stu-id="c1de1-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-237">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-237">CC003</span></span></td>
<td><span data-ttu-id="c1de1-238">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-238">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-239">0</span><span class="sxs-lookup"><span data-stu-id="c1de1-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c1de1-240">Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="c1de1-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-241">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-241">Cost object</span></span></th>
<th><span data-ttu-id="c1de1-242">Väärtus</span><span class="sxs-lookup"><span data-stu-id="c1de1-242">Magnitude</span></span></th>
<th><span data-ttu-id="c1de1-243">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="c1de1-243">Allocation factor</span></span></th>
<th><span data-ttu-id="c1de1-244">Summa</span><span class="sxs-lookup"><span data-stu-id="c1de1-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-245">CC001</span><span class="sxs-lookup"><span data-stu-id="c1de1-245">CC001</span></span></td>
<td><span data-ttu-id="c1de1-246">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="c1de1-246">HR</span></span></td>
<td><span data-ttu-id="c1de1-247">1000</span><span class="sxs-lookup"><span data-stu-id="c1de1-247">1,000</span></span></td>
<td><span data-ttu-id="c1de1-248">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c1de1-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c1de1-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-250">CC002</span><span class="sxs-lookup"><span data-stu-id="c1de1-250">CC002</span></span></td>
<td><span data-ttu-id="c1de1-251">Finantsid</span><span class="sxs-lookup"><span data-stu-id="c1de1-251">Finance</span></span></td>
<td><span data-ttu-id="c1de1-252">6,000</span><span class="sxs-lookup"><span data-stu-id="c1de1-252">6,000</span></span></td>
<td><span data-ttu-id="c1de1-253">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c1de1-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c1de1-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-255">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-255">CC003</span></span></td>
<td><span data-ttu-id="c1de1-256">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-256">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-257">0</span><span class="sxs-lookup"><span data-stu-id="c1de1-257">0</span></span></td>
<td><span data-ttu-id="c1de1-258">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c1de1-259">0,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c1de1-260">Fikseeritud kulu tuleb jaotada ühtlaselt üksikutele kuluobjektidele, mis on tarbinud elektrit.</span><span class="sxs-lookup"><span data-stu-id="c1de1-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="c1de1-261">Selle tulemuse saate, kasutades valemi eraldamisaluses statistilise dimensiooni liiget Elekter: (Elekter &gt; 0,00). Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="c1de1-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-262">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-262">Cost object</span></span></th>
<th><span data-ttu-id="c1de1-263">Valem</span><span class="sxs-lookup"><span data-stu-id="c1de1-263">Formula</span></span></th>
<th><span data-ttu-id="c1de1-264">Väärtus</span><span class="sxs-lookup"><span data-stu-id="c1de1-264">Magnitude</span></span></th>
<th><span data-ttu-id="c1de1-265">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="c1de1-265">Allocation factor</span></span></th>
<th><span data-ttu-id="c1de1-266">Summa</span><span class="sxs-lookup"><span data-stu-id="c1de1-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-267">CC001</span><span class="sxs-lookup"><span data-stu-id="c1de1-267">CC001</span></span></td>
<td><span data-ttu-id="c1de1-268">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="c1de1-268">HR</span></span></td>
<td><span data-ttu-id="c1de1-269">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="c1de1-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c1de1-270">1</span><span class="sxs-lookup"><span data-stu-id="c1de1-270">1</span></span></td>
<td><span data-ttu-id="c1de1-271">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c1de1-272">500,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-273">CC002</span><span class="sxs-lookup"><span data-stu-id="c1de1-273">CC002</span></span></td>
<td><span data-ttu-id="c1de1-274">Finantsid</span><span class="sxs-lookup"><span data-stu-id="c1de1-274">Finance</span></span></td>
<td><span data-ttu-id="c1de1-275">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="c1de1-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c1de1-276">1</span><span class="sxs-lookup"><span data-stu-id="c1de1-276">1</span></span></td>
<td><span data-ttu-id="c1de1-277">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c1de1-278">500,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-279">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-279">CC003</span></span></td>
<td><span data-ttu-id="c1de1-280">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-280">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="c1de1-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c1de1-282">0</span><span class="sxs-lookup"><span data-stu-id="c1de1-282">0</span></span></td>
<td><span data-ttu-id="c1de1-283">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c1de1-284">0,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c1de1-285">Tööleht</span><span class="sxs-lookup"><span data-stu-id="c1de1-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c1de1-286">Tööleht</span><span class="sxs-lookup"><span data-stu-id="c1de1-286">Journal</span></span></th>
<th><span data-ttu-id="c1de1-287">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="c1de1-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c1de1-288">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="c1de1-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c1de1-289">Versioon</span><span class="sxs-lookup"><span data-stu-id="c1de1-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-290">00002</span><span class="sxs-lookup"><span data-stu-id="c1de1-290">00002</span></span></td>
<td><span data-ttu-id="c1de1-291">Kulujaotuse arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="c1de1-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="c1de1-292">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="c1de1-292">Fiscal</span></span></td>
<td><span data-ttu-id="c1de1-293">2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-293">2017</span></span></td>
<td><span data-ttu-id="c1de1-294">Periood 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-294">Period 1</span></span></td>
<td><span data-ttu-id="c1de1-295">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="c1de1-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c1de1-296">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="c1de1-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c1de1-297">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="c1de1-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c1de1-298">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c1de1-299">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="c1de1-299">Cost element</span></span></th>
<th><span data-ttu-id="c1de1-300">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="c1de1-300">Cost behavior</span></span></th>
<th><span data-ttu-id="c1de1-301">Summa</span><span class="sxs-lookup"><span data-stu-id="c1de1-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-302">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="c1de1-303">CC099</span><span class="sxs-lookup"><span data-stu-id="c1de1-303">CC099</span></span></td>
<td><span data-ttu-id="c1de1-304">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="c1de1-304">Default cost center</span></span></td>
<td><span data-ttu-id="c1de1-305">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-305">10001</span></span></td>
<td><span data-ttu-id="c1de1-306">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-306">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-307">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-307">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-308">1 000,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-309">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="c1de1-310">CC099</span><span class="sxs-lookup"><span data-stu-id="c1de1-310">CC099</span></span></td>
<td><span data-ttu-id="c1de1-311">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="c1de1-311">Default cost center</span></span></td>
<td><span data-ttu-id="c1de1-312">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-312">10001</span></span></td>
<td><span data-ttu-id="c1de1-313">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-313">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-314">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-314">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="c1de1-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c1de1-316">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="c1de1-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-317">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c1de1-318">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="c1de1-318">Cost element</span></span></th>
<th><span data-ttu-id="c1de1-319">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="c1de1-319">Cost behavior</span></span></th>
<th><span data-ttu-id="c1de1-320">Summa</span><span class="sxs-lookup"><span data-stu-id="c1de1-320">Amount</span></span></th>
<th><span data-ttu-id="c1de1-321">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="c1de1-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-322">CC099</span><span class="sxs-lookup"><span data-stu-id="c1de1-322">CC099</span></span></td>
<td><span data-ttu-id="c1de1-323">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="c1de1-323">Default cost center</span></span></td>
<td><span data-ttu-id="c1de1-324">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-324">10001</span></span></td>
<td><span data-ttu-id="c1de1-325">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-325">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-326">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-326">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-327">–1000,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-327">-1,000.00</span></span></td>
<td><span data-ttu-id="c1de1-328">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-329">CC001</span><span class="sxs-lookup"><span data-stu-id="c1de1-329">CC001</span></span></td>
<td><span data-ttu-id="c1de1-330">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="c1de1-330">HR</span></span></td>
<td><span data-ttu-id="c1de1-331">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-331">10001</span></span></td>
<td><span data-ttu-id="c1de1-332">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-332">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-333">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-333">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-334">500,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-334">500.00</span></span></td>
<td><span data-ttu-id="c1de1-335">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-336">CC002</span><span class="sxs-lookup"><span data-stu-id="c1de1-336">CC002</span></span></td>
<td><span data-ttu-id="c1de1-337">Finantsid</span><span class="sxs-lookup"><span data-stu-id="c1de1-337">Finance</span></span></td>
<td><span data-ttu-id="c1de1-338">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-338">10001</span></span></td>
<td><span data-ttu-id="c1de1-339">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-339">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-340">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-340">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-341">500,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-341">500.00</span></span></td>
<td><span data-ttu-id="c1de1-342">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-343">CC099</span><span class="sxs-lookup"><span data-stu-id="c1de1-343">CC099</span></span></td>
<td><span data-ttu-id="c1de1-344">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="c1de1-344">Default cost center</span></span></td>
<td><span data-ttu-id="c1de1-345">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-345">10001</span></span></td>
<td><span data-ttu-id="c1de1-346">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-346">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-347">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-347">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-348">–9000,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-348">-9,000.00</span></span></td>
<td><span data-ttu-id="c1de1-349">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-350">CC001</span><span class="sxs-lookup"><span data-stu-id="c1de1-350">CC001</span></span></td>
<td><span data-ttu-id="c1de1-351">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="c1de1-351">HR</span></span></td>
<td><span data-ttu-id="c1de1-352">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-352">10001</span></span></td>
<td><span data-ttu-id="c1de1-353">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-353">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-354">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-354">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c1de1-355">1,285.71</span></span></td>
<td><span data-ttu-id="c1de1-356">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-357">CC002</span><span class="sxs-lookup"><span data-stu-id="c1de1-357">CC002</span></span></td>
<td><span data-ttu-id="c1de1-358">Finantsid</span><span class="sxs-lookup"><span data-stu-id="c1de1-358">Finance</span></span></td>
<td><span data-ttu-id="c1de1-359">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-359">10001</span></span></td>
<td><span data-ttu-id="c1de1-360">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-360">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-361">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-361">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c1de1-362">7,714.29</span></span></td>
<td><span data-ttu-id="c1de1-363">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c1de1-364">Üksikasjalikku teavet kulude jaotamise ja eraldamise aluse kohta vt jaotistest Kulujaotuse poliitika ja Eraldamisalused.</span><span class="sxs-lookup"><span data-stu-id="c1de1-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="c1de1-365">(Pange tähele, et see teema pole veel valmis, kuid see tuleb peagi.)</span><span class="sxs-lookup"><span data-stu-id="c1de1-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="c1de1-366">3. etapp: üldkulude määra arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="c1de1-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="c1de1-367">Üldkulude määra kasutatakse ühe või mitme kindla kuluobjekti debiteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="c1de1-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="c1de1-368">Tasu põhineb eelmääratud kulumääral ja väärtusel määratud eraldamisalusest.</span><span class="sxs-lookup"><span data-stu-id="c1de1-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="c1de1-369">Üldkulu määra määratlemine</span><span class="sxs-lookup"><span data-stu-id="c1de1-369">Define the overhead rate</span></span>

<span data-ttu-id="c1de1-370">Kuluobjekt CC001 inimressursid panustab sisemiste projektide kogumisse.</span><span class="sxs-lookup"><span data-stu-id="c1de1-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="c1de1-371">Luuakse statistilise dimensiooni liige nimega Inimressursside projektid, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="c1de1-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-372">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-372">Cost object</span></span></th>
<th><span data-ttu-id="c1de1-373">Tunnid</span><span class="sxs-lookup"><span data-stu-id="c1de1-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-374">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-374">Proj 1</span></span></td>
<td><span data-ttu-id="c1de1-375">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-375">Project 1</span></span></td>
<td><span data-ttu-id="c1de1-376">3</span><span class="sxs-lookup"><span data-stu-id="c1de1-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-377">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-377">Proj 2</span></span></td>
<td><span data-ttu-id="c1de1-378">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-378">Project 2</span></span></td>
<td><span data-ttu-id="c1de1-379">1</span><span class="sxs-lookup"><span data-stu-id="c1de1-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c1de1-380">Määratletud on eelmääratud kulumäär kuluprojektide panusele.</span><span class="sxs-lookup"><span data-stu-id="c1de1-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-381">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-381">Cost object</span></span></th>
<th><span data-ttu-id="c1de1-382">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="c1de1-382">Cost element</span></span></th>
<th><span data-ttu-id="c1de1-383">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="c1de1-383">Cost behavior</span></span></th>
<th><span data-ttu-id="c1de1-384">Ühikud</span><span class="sxs-lookup"><span data-stu-id="c1de1-384">Units</span></span></th>
<th><span data-ttu-id="c1de1-385">Kurss</span><span class="sxs-lookup"><span data-stu-id="c1de1-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-386">CC001</span><span class="sxs-lookup"><span data-stu-id="c1de1-386">CC001</span></span></td>
<td><span data-ttu-id="c1de1-387">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="c1de1-387">HR</span></span></td>
<td><span data-ttu-id="c1de1-388">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-388">10001</span></span></td>
<td><span data-ttu-id="c1de1-389">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-389">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-390">1</span><span class="sxs-lookup"><span data-stu-id="c1de1-390">1</span></span></td>
<td><span data-ttu-id="c1de1-391">10</span><span class="sxs-lookup"><span data-stu-id="c1de1-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c1de1-392">Järgmises tabelis on näidatud tulemus, kui inimressursside projektid on rakendatud eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="c1de1-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-393">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-393">Cost object</span></span></th>
<th><span data-ttu-id="c1de1-394">Väärtus</span><span class="sxs-lookup"><span data-stu-id="c1de1-394">Magnitude</span></span></th>
<th><span data-ttu-id="c1de1-395">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="c1de1-395">Cost element</span></span></th>
<th><span data-ttu-id="c1de1-396">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="c1de1-396">Allocation factor</span></span></th>
<th><span data-ttu-id="c1de1-397">Summa</span><span class="sxs-lookup"><span data-stu-id="c1de1-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-398">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-398">Proj 1</span></span></td>
<td><span data-ttu-id="c1de1-399">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-399">Project 1</span></span></td>
<td><span data-ttu-id="c1de1-400">3</span><span class="sxs-lookup"><span data-stu-id="c1de1-400">3</span></span></td>
<td><span data-ttu-id="c1de1-401">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-401">10001</span></span></td>
<td><span data-ttu-id="c1de1-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c1de1-403">30,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-404">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-404">Proj 2</span></span></td>
<td><span data-ttu-id="c1de1-405">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-405">Project 2</span></span></td>
<td><span data-ttu-id="c1de1-406">1</span><span class="sxs-lookup"><span data-stu-id="c1de1-406">1</span></span></td>
<td><span data-ttu-id="c1de1-407">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-407">10001</span></span></td>
<td><span data-ttu-id="c1de1-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c1de1-409">10,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c1de1-410">Tööleht</span><span class="sxs-lookup"><span data-stu-id="c1de1-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c1de1-411">Tööleht</span><span class="sxs-lookup"><span data-stu-id="c1de1-411">Journal</span></span></th>
<th><span data-ttu-id="c1de1-412">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="c1de1-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c1de1-413">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="c1de1-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c1de1-414">Versioon</span><span class="sxs-lookup"><span data-stu-id="c1de1-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-415">00003</span><span class="sxs-lookup"><span data-stu-id="c1de1-415">00003</span></span></td>
<td><span data-ttu-id="c1de1-416">Üldkulu määra arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="c1de1-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="c1de1-417">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="c1de1-417">Fiscal</span></span></td>
<td><span data-ttu-id="c1de1-418">2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-418">2017</span></span></td>
<td><span data-ttu-id="c1de1-419">Periood 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-419">Period 1</span></span></td>
<td><span data-ttu-id="c1de1-420">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="c1de1-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="c1de1-421">Töölehe sisestused (töölehe sisestused üldkulu määra arvutamiseks)</span><span class="sxs-lookup"><span data-stu-id="c1de1-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c1de1-422">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="c1de1-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c1de1-423">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-423">Cost object</span></span></th>
<th><span data-ttu-id="c1de1-424">Väärtus</span><span class="sxs-lookup"><span data-stu-id="c1de1-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-425">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="c1de1-426">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-426">Proj 1</span></span></td>
<td><span data-ttu-id="c1de1-427">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c1de1-428">3,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-429">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="c1de1-430">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-430">Proj 2</span></span></td>
<td><span data-ttu-id="c1de1-431">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c1de1-432">1,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c1de1-433">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="c1de1-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-434">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c1de1-435">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="c1de1-435">Cost element</span></span></th>
<th><span data-ttu-id="c1de1-436">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="c1de1-436">Cost behavior</span></span></th>
<th><span data-ttu-id="c1de1-437">Summa</span><span class="sxs-lookup"><span data-stu-id="c1de1-437">Amount</span></span></th>
<th><span data-ttu-id="c1de1-438">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="c1de1-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="c1de1-439">CC0001</span></span></td>
<td><span data-ttu-id="c1de1-440">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="c1de1-440">HR</span></span></td>
<td><span data-ttu-id="c1de1-441">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-441">10001</span></span></td>
<td><span data-ttu-id="c1de1-442">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-442">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-443">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-443">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-444">–30,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-444">-30.00</span></span></td>
<td><span data-ttu-id="c1de1-445">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-446">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-446">Proj 1</span></span></td>
<td><span data-ttu-id="c1de1-447">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c1de1-448">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-448">10001</span></span></td>
<td><span data-ttu-id="c1de1-449">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-449">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-450">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-450">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-451">30,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-451">30.00</span></span></td>
<td><span data-ttu-id="c1de1-452">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-453">CC001</span><span class="sxs-lookup"><span data-stu-id="c1de1-453">CC001</span></span></td>
<td><span data-ttu-id="c1de1-454">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="c1de1-454">HR</span></span></td>
<td><span data-ttu-id="c1de1-455">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-455">10001</span></span></td>
<td><span data-ttu-id="c1de1-456">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-456">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-457">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-457">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-458">-10.00</span></span></td>
<td><span data-ttu-id="c1de1-459">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-460">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-460">Proj 2</span></span></td>
<td><span data-ttu-id="c1de1-461">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c1de1-462">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-462">10001</span></span></td>
<td><span data-ttu-id="c1de1-463">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-463">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-464">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-464">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-465">10,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-465">10.00</span></span></td>
<td><span data-ttu-id="c1de1-466">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c1de1-467">Üksikasjalikku teavet üldkulu määra poliitika kohta vt jaotistest Üldkulu määra poliitika ja Eraldamisalused.</span><span class="sxs-lookup"><span data-stu-id="c1de1-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="c1de1-468">(Pange tähele, et see teema pole veel valmis, kuid see tuleb peagi.)</span><span class="sxs-lookup"><span data-stu-id="c1de1-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="c1de1-469">4. etapp: kulueralduse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="c1de1-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="c1de1-470">Eraldamist kasutatakse kuluobjekti saldo eraldamiseks teistele kuluobjektidele, rakendades eraldamisalust.</span><span class="sxs-lookup"><span data-stu-id="c1de1-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="c1de1-471">Finance and Operations toetab vastastikuse eraldamise meetodit.</span><span class="sxs-lookup"><span data-stu-id="c1de1-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="c1de1-472">Vastastikuse eraldamise meetodi puhul tuvastatakse täiendavate kuluobjektide vahetatavad vastastikused teenused.</span><span class="sxs-lookup"><span data-stu-id="c1de1-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="c1de1-473">Süsteem määrab automaatselt eraldamiste tegemise õige järjekorra.</span><span class="sxs-lookup"><span data-stu-id="c1de1-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="c1de1-474">Kuluobjekti saldo eraldatakse üksiku eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="c1de1-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="c1de1-475">Toetatakse eraldamisi kuluobjektide dimensioonide ja nende vastavate liikmete seas.</span><span class="sxs-lookup"><span data-stu-id="c1de1-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="c1de1-476">Eraldamisjärjekorda reguleerib kulujuhtseade.</span><span class="sxs-lookup"><span data-stu-id="c1de1-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="c1de1-477">[![Vastastikune meetod](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="c1de1-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="c1de1-478">Kulueraldamise määratlemine</span><span class="sxs-lookup"><span data-stu-id="c1de1-478">Define the cost allocation</span></span>

<span data-ttu-id="c1de1-479">Siin on lihtne näide, mis selgitab, kuidas jälgida kulu liikumist.</span><span class="sxs-lookup"><span data-stu-id="c1de1-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="c1de1-480">Kuluobjekt CC001 inimressursid panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="c1de1-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="c1de1-481">Luuakse statistilise dimensiooni liige nimega Inimressursside teenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="c1de1-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-482">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-482">Cost object</span></span></th>
<th><span data-ttu-id="c1de1-483">Inimressursside teenused</span><span class="sxs-lookup"><span data-stu-id="c1de1-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-484">CC002</span><span class="sxs-lookup"><span data-stu-id="c1de1-484">CC002</span></span></td>
<td><span data-ttu-id="c1de1-485">Finantsid</span><span class="sxs-lookup"><span data-stu-id="c1de1-485">Finance</span></span></td>
<td><span data-ttu-id="c1de1-486">35</span><span class="sxs-lookup"><span data-stu-id="c1de1-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-487">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-487">CC003</span></span></td>
<td><span data-ttu-id="c1de1-488">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-488">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-489">55</span><span class="sxs-lookup"><span data-stu-id="c1de1-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-490">CC004</span><span class="sxs-lookup"><span data-stu-id="c1de1-490">CC004</span></span></td>
<td><span data-ttu-id="c1de1-491">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="c1de1-491">Packaging</span></span></td>
<td><span data-ttu-id="c1de1-492">10</span><span class="sxs-lookup"><span data-stu-id="c1de1-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c1de1-493">Kuluobjekt CC002 rahandus panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="c1de1-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="c1de1-494">Luuakse statistilise dimensiooni liige nimega Rahandusteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="c1de1-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-495">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-495">Cost object</span></span></th>
<th><span data-ttu-id="c1de1-496">Rahandusteenused</span><span class="sxs-lookup"><span data-stu-id="c1de1-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-497">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-497">CC003</span></span></td>
<td><span data-ttu-id="c1de1-498">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-498">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-499">65</span><span class="sxs-lookup"><span data-stu-id="c1de1-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-500">CC004</span><span class="sxs-lookup"><span data-stu-id="c1de1-500">CC004</span></span></td>
<td><span data-ttu-id="c1de1-501">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="c1de1-501">Packaging</span></span></td>
<td><span data-ttu-id="c1de1-502">35</span><span class="sxs-lookup"><span data-stu-id="c1de1-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c1de1-503">Kuluobjekt CC003 assembler panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="c1de1-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="c1de1-504">Luuakse statistilise dimensiooni liige nimega Assembleriteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="c1de1-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-505">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-505">Cost object</span></span></th>
<th><span data-ttu-id="c1de1-506">Assembleriteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="c1de1-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-507">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-507">Prod 1</span></span></td>
<td><span data-ttu-id="c1de1-508">Toode 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-508">Product 1</span></span></td>
<td><span data-ttu-id="c1de1-509">60</span><span class="sxs-lookup"><span data-stu-id="c1de1-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-510">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-510">Prod 2</span></span></td>
<td><span data-ttu-id="c1de1-511">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-511">Product 2</span></span></td>
<td><span data-ttu-id="c1de1-512">20</span><span class="sxs-lookup"><span data-stu-id="c1de1-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c1de1-513">Kuluobjekt CC004 pakendamine panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="c1de1-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="c1de1-514">Luuakse statistilise dimensiooni liige nimega Pakendamisteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="c1de1-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-515">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-515">Cost object</span></span></th>
<th><span data-ttu-id="c1de1-516">Pakendamisteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="c1de1-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-517">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-517">Prod 1</span></span></td>
<td><span data-ttu-id="c1de1-518">Toode 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-518">Product 1</span></span></td>
<td><span data-ttu-id="c1de1-519">80</span><span class="sxs-lookup"><span data-stu-id="c1de1-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-520">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-520">Prod 2</span></span></td>
<td><span data-ttu-id="c1de1-521">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-521">Product 2</span></span></td>
<td><span data-ttu-id="c1de1-522">sept.</span><span class="sxs-lookup"><span data-stu-id="c1de1-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c1de1-523">**Märkus.** Finance and Operationsis saab statistilised mõõdud, nagu toote tarbitud tootmistunnid, tuletada lähteandmetest.</span><span class="sxs-lookup"><span data-stu-id="c1de1-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="c1de1-524">Üksikasjalikku teavet statistiliste mõõtude pakkujate kohta vt jaotisest Statistilise mõõdu pakkuja mall.</span><span class="sxs-lookup"><span data-stu-id="c1de1-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="c1de1-525">(Pange tähele, et see teema pole veel valmis, kuid see tuleb peagi.) Järgmises tabelis on näidatud tulemus, kui Inimressursside teenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud kulu ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="c1de1-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-526">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-526">Cost object</span></span></th>
<th><span data-ttu-id="c1de1-527">Väärtus</span><span class="sxs-lookup"><span data-stu-id="c1de1-527">Magnitude</span></span></th>
<th><span data-ttu-id="c1de1-528">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="c1de1-528">Allocation factor</span></span></th>
<th><span data-ttu-id="c1de1-529">Summa</span><span class="sxs-lookup"><span data-stu-id="c1de1-529">Amount</span></span></th>
<th><span data-ttu-id="c1de1-530">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="c1de1-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-531">CC002</span><span class="sxs-lookup"><span data-stu-id="c1de1-531">CC002</span></span></td>
<td><span data-ttu-id="c1de1-532">Finantsid</span><span class="sxs-lookup"><span data-stu-id="c1de1-532">Finance</span></span></td>
<td><span data-ttu-id="c1de1-533">35</span><span class="sxs-lookup"><span data-stu-id="c1de1-533">35</span></span></td>
<td><span data-ttu-id="c1de1-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c1de1-535">175.00</span><span class="sxs-lookup"><span data-stu-id="c1de1-535">175.00</span></span></td>
<td><span data-ttu-id="c1de1-536">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-537">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-537">CC003</span></span></td>
<td><span data-ttu-id="c1de1-538">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-538">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-539">55</span><span class="sxs-lookup"><span data-stu-id="c1de1-539">55</span></span></td>
<td><span data-ttu-id="c1de1-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c1de1-541">275.00</span><span class="sxs-lookup"><span data-stu-id="c1de1-541">275.00</span></span></td>
<td><span data-ttu-id="c1de1-542">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-543">CC004</span><span class="sxs-lookup"><span data-stu-id="c1de1-543">CC004</span></span></td>
<td><span data-ttu-id="c1de1-544">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="c1de1-544">Packaging</span></span></td>
<td><span data-ttu-id="c1de1-545">10</span><span class="sxs-lookup"><span data-stu-id="c1de1-545">10</span></span></td>
<td><span data-ttu-id="c1de1-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c1de1-547">50,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-547">50.00</span></span></td>
<td><span data-ttu-id="c1de1-548">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-549">CC002</span><span class="sxs-lookup"><span data-stu-id="c1de1-549">CC002</span></span></td>
<td><span data-ttu-id="c1de1-550">Finantsid</span><span class="sxs-lookup"><span data-stu-id="c1de1-550">Finance</span></span></td>
<td><span data-ttu-id="c1de1-551">35</span><span class="sxs-lookup"><span data-stu-id="c1de1-551">35</span></span></td>
<td><span data-ttu-id="c1de1-552">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="c1de1-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c1de1-553">436.00</span><span class="sxs-lookup"><span data-stu-id="c1de1-553">436.00</span></span></td>
<td><span data-ttu-id="c1de1-554">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-555">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-555">CC003</span></span></td>
<td><span data-ttu-id="c1de1-556">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-556">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-557">55</span><span class="sxs-lookup"><span data-stu-id="c1de1-557">55</span></span></td>
<td><span data-ttu-id="c1de1-558">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="c1de1-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c1de1-559">685.14</span><span class="sxs-lookup"><span data-stu-id="c1de1-559">685.14</span></span></td>
<td><span data-ttu-id="c1de1-560">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-561">CC004</span><span class="sxs-lookup"><span data-stu-id="c1de1-561">CC004</span></span></td>
<td><span data-ttu-id="c1de1-562">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="c1de1-562">Packaging</span></span></td>
<td><span data-ttu-id="c1de1-563">10</span><span class="sxs-lookup"><span data-stu-id="c1de1-563">10</span></span></td>
<td><span data-ttu-id="c1de1-564">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="c1de1-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c1de1-565">124.57</span><span class="sxs-lookup"><span data-stu-id="c1de1-565">124.57</span></span></td>
<td><span data-ttu-id="c1de1-566">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c1de1-567">Järgmises tabelis on näidatud tulemus, kui Rahandusteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="c1de1-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-568">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-568">Cost object</span></span></th>
<th><span data-ttu-id="c1de1-569">Väärtus</span><span class="sxs-lookup"><span data-stu-id="c1de1-569">Magnitude</span></span></th>
<th><span data-ttu-id="c1de1-570">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="c1de1-570">Allocation factor</span></span></th>
<th><span data-ttu-id="c1de1-571">Summa</span><span class="sxs-lookup"><span data-stu-id="c1de1-571">Amount</span></span></th>
<th><span data-ttu-id="c1de1-572">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="c1de1-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-573">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-573">CC003</span></span></td>
<td><span data-ttu-id="c1de1-574">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-574">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-575">65</span><span class="sxs-lookup"><span data-stu-id="c1de1-575">65</span></span></td>
<td><span data-ttu-id="c1de1-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="c1de1-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c1de1-577">438.75</span><span class="sxs-lookup"><span data-stu-id="c1de1-577">438.75</span></span></td>
<td><span data-ttu-id="c1de1-578">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-579">CC004</span><span class="sxs-lookup"><span data-stu-id="c1de1-579">CC004</span></span></td>
<td><span data-ttu-id="c1de1-580">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="c1de1-580">Packaging</span></span></td>
<td><span data-ttu-id="c1de1-581">35</span><span class="sxs-lookup"><span data-stu-id="c1de1-581">35</span></span></td>
<td><span data-ttu-id="c1de1-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="c1de1-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c1de1-583">236.25</span><span class="sxs-lookup"><span data-stu-id="c1de1-583">236.25</span></span></td>
<td><span data-ttu-id="c1de1-584">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-585">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-585">CC003</span></span></td>
<td><span data-ttu-id="c1de1-586">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-586">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-587">65</span><span class="sxs-lookup"><span data-stu-id="c1de1-587">65</span></span></td>
<td><span data-ttu-id="c1de1-588">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="c1de1-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c1de1-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c1de1-589">5,297.69</span></span></td>
<td><span data-ttu-id="c1de1-590">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-591">CC004</span><span class="sxs-lookup"><span data-stu-id="c1de1-591">CC004</span></span></td>
<td><span data-ttu-id="c1de1-592">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="c1de1-592">Packaging</span></span></td>
<td><span data-ttu-id="c1de1-593">35</span><span class="sxs-lookup"><span data-stu-id="c1de1-593">35</span></span></td>
<td><span data-ttu-id="c1de1-594">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="c1de1-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c1de1-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c1de1-595">2,852.60</span></span></td>
<td><span data-ttu-id="c1de1-596">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c1de1-597">Järgmises tabelis on näidatud tulemus, kui Assembleriteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="c1de1-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-598">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-598">Cost object</span></span></th>
<th><span data-ttu-id="c1de1-599">Väärtus</span><span class="sxs-lookup"><span data-stu-id="c1de1-599">Magnitude</span></span></th>
<th><span data-ttu-id="c1de1-600">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="c1de1-600">Allocation factor</span></span></th>
<th><span data-ttu-id="c1de1-601">Summa</span><span class="sxs-lookup"><span data-stu-id="c1de1-601">Amount</span></span></th>
<th><span data-ttu-id="c1de1-602">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="c1de1-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-603">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-603">Prod 1</span></span></td>
<td><span data-ttu-id="c1de1-604">Toode 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-604">Product 1</span></span></td>
<td><span data-ttu-id="c1de1-605">60</span><span class="sxs-lookup"><span data-stu-id="c1de1-605">60</span></span></td>
<td><span data-ttu-id="c1de1-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="c1de1-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c1de1-607">535.31</span><span class="sxs-lookup"><span data-stu-id="c1de1-607">535.31</span></span></td>
<td><span data-ttu-id="c1de1-608">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-609">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-609">Prod 2</span></span></td>
<td><span data-ttu-id="c1de1-610">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-610">Product 2</span></span></td>
<td><span data-ttu-id="c1de1-611">20</span><span class="sxs-lookup"><span data-stu-id="c1de1-611">20</span></span></td>
<td><span data-ttu-id="c1de1-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="c1de1-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c1de1-613">178.44</span><span class="sxs-lookup"><span data-stu-id="c1de1-613">178.44</span></span></td>
<td><span data-ttu-id="c1de1-614">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-615">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-615">Prod 1</span></span></td>
<td><span data-ttu-id="c1de1-616">Toode 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-616">Product 1</span></span></td>
<td><span data-ttu-id="c1de1-617">60</span><span class="sxs-lookup"><span data-stu-id="c1de1-617">60</span></span></td>
<td><span data-ttu-id="c1de1-618">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="c1de1-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c1de1-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c1de1-619">4,487.12</span></span></td>
<td><span data-ttu-id="c1de1-620">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-621">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-621">Prod 2</span></span></td>
<td><span data-ttu-id="c1de1-622">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-622">Product 2</span></span></td>
<td><span data-ttu-id="c1de1-623">20</span><span class="sxs-lookup"><span data-stu-id="c1de1-623">20</span></span></td>
<td><span data-ttu-id="c1de1-624">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="c1de1-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c1de1-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c1de1-625">1,495.71</span></span></td>
<td><span data-ttu-id="c1de1-626">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c1de1-627">Järgmises tabelis on näidatud tulemus, kui Pakendamisteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="c1de1-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-628">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-628">Cost object</span></span></th>
<th><span data-ttu-id="c1de1-629">Väärtus</span><span class="sxs-lookup"><span data-stu-id="c1de1-629">Magnitude</span></span></th>
<th><span data-ttu-id="c1de1-630">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="c1de1-630">Allocation factor</span></span></th>
<th><span data-ttu-id="c1de1-631">Summa</span><span class="sxs-lookup"><span data-stu-id="c1de1-631">Amount</span></span></th>
<th><span data-ttu-id="c1de1-632">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="c1de1-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-633">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-633">Prod 1</span></span></td>
<td><span data-ttu-id="c1de1-634">Toode 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-634">Product 1</span></span></td>
<td><span data-ttu-id="c1de1-635">80</span><span class="sxs-lookup"><span data-stu-id="c1de1-635">80</span></span></td>
<td><span data-ttu-id="c1de1-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="c1de1-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c1de1-637">241.05</span><span class="sxs-lookup"><span data-stu-id="c1de1-637">241.05</span></span></td>
<td><span data-ttu-id="c1de1-638">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-639">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-639">Prod 2</span></span></td>
<td><span data-ttu-id="c1de1-640">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-640">Product 2</span></span></td>
<td><span data-ttu-id="c1de1-641">15</span><span class="sxs-lookup"><span data-stu-id="c1de1-641">15</span></span></td>
<td><span data-ttu-id="c1de1-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="c1de1-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c1de1-643">45.20</span><span class="sxs-lookup"><span data-stu-id="c1de1-643">45.20</span></span></td>
<td><span data-ttu-id="c1de1-644">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-645">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-645">Prod 1</span></span></td>
<td><span data-ttu-id="c1de1-646">Toode 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-646">Product 1</span></span></td>
<td><span data-ttu-id="c1de1-647">80</span><span class="sxs-lookup"><span data-stu-id="c1de1-647">80</span></span></td>
<td><span data-ttu-id="c1de1-648">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="c1de1-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c1de1-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c1de1-649">2,507.09</span></span></td>
<td><span data-ttu-id="c1de1-650">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-651">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-651">Prod 2</span></span></td>
<td><span data-ttu-id="c1de1-652">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-652">Product 2</span></span></td>
<td><span data-ttu-id="c1de1-653">15</span><span class="sxs-lookup"><span data-stu-id="c1de1-653">15</span></span></td>
<td><span data-ttu-id="c1de1-654">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="c1de1-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c1de1-655">470.08</span><span class="sxs-lookup"><span data-stu-id="c1de1-655">470.08</span></span></td>
<td><span data-ttu-id="c1de1-656">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c1de1-657">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="c1de1-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c1de1-658">Tööleht</span><span class="sxs-lookup"><span data-stu-id="c1de1-658">Journal</span></span></th>
<th><span data-ttu-id="c1de1-659">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="c1de1-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c1de1-660">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="c1de1-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c1de1-661">Versioon</span><span class="sxs-lookup"><span data-stu-id="c1de1-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-662">00004</span><span class="sxs-lookup"><span data-stu-id="c1de1-662">00004</span></span></td>
<td><span data-ttu-id="c1de1-663">Kulueralduse tööleht</span><span class="sxs-lookup"><span data-stu-id="c1de1-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="c1de1-664">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="c1de1-664">Fiscal</span></span></td>
<td><span data-ttu-id="c1de1-665">2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-665">2017</span></span></td>
<td><span data-ttu-id="c1de1-666">Periood 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-666">Period 1</span></span></td>
<td><span data-ttu-id="c1de1-667">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="c1de1-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="c1de1-668">Töölehe read</span><span class="sxs-lookup"><span data-stu-id="c1de1-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c1de1-669">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="c1de1-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c1de1-670">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c1de1-671">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="c1de1-671">Cost element</span></span></th>
<th><span data-ttu-id="c1de1-672">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="c1de1-672">Cost behavior</span></span></th>
<th><span data-ttu-id="c1de1-673">Summa</span><span class="sxs-lookup"><span data-stu-id="c1de1-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-674">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="c1de1-675">CC001</span><span class="sxs-lookup"><span data-stu-id="c1de1-675">CC001</span></span></td>
<td><span data-ttu-id="c1de1-676">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="c1de1-676">HR</span></span></td>
<td><span data-ttu-id="c1de1-677">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-677">10001</span></span></td>
<td><span data-ttu-id="c1de1-678">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-678">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-679">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-679">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-680">500,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-681">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="c1de1-682">CC001</span><span class="sxs-lookup"><span data-stu-id="c1de1-682">CC001</span></span></td>
<td><span data-ttu-id="c1de1-683">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="c1de1-683">HR</span></span></td>
<td><span data-ttu-id="c1de1-684">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-684">10001</span></span></td>
<td><span data-ttu-id="c1de1-685">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-685">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-686">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-686">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="c1de1-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-688">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="c1de1-689">CC002</span><span class="sxs-lookup"><span data-stu-id="c1de1-689">CC002</span></span></td>
<td><span data-ttu-id="c1de1-690">Finantsid</span><span class="sxs-lookup"><span data-stu-id="c1de1-690">Finance</span></span></td>
<td><span data-ttu-id="c1de1-691">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-691">10001</span></span></td>
<td><span data-ttu-id="c1de1-692">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-692">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-693">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-693">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-694">675.00</span><span class="sxs-lookup"><span data-stu-id="c1de1-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-695">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="c1de1-696">CC002</span><span class="sxs-lookup"><span data-stu-id="c1de1-696">CC002</span></span></td>
<td><span data-ttu-id="c1de1-697">Finantsid</span><span class="sxs-lookup"><span data-stu-id="c1de1-697">Finance</span></span></td>
<td><span data-ttu-id="c1de1-698">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-698">10001</span></span></td>
<td><span data-ttu-id="c1de1-699">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-699">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-700">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-700">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="c1de1-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-702">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="c1de1-703">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-703">CC003</span></span></td>
<td><span data-ttu-id="c1de1-704">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-704">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-705">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-705">10001</span></span></td>
<td><span data-ttu-id="c1de1-706">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-706">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-707">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-707">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-708">713.75</span><span class="sxs-lookup"><span data-stu-id="c1de1-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-709">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="c1de1-710">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-710">CC003</span></span></td>
<td><span data-ttu-id="c1de1-711">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-711">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-712">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-712">10001</span></span></td>
<td><span data-ttu-id="c1de1-713">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-713">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-714">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-714">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="c1de1-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-716">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="c1de1-717">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-717">CC003</span></span></td>
<td><span data-ttu-id="c1de1-718">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="c1de1-718">Packaging</span></span></td>
<td><span data-ttu-id="c1de1-719">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-719">10001</span></span></td>
<td><span data-ttu-id="c1de1-720">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-720">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-721">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-721">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-722">286.25</span><span class="sxs-lookup"><span data-stu-id="c1de1-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-723">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="c1de1-724">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-724">CC003</span></span></td>
<td><span data-ttu-id="c1de1-725">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="c1de1-725">Packaging</span></span></td>
<td><span data-ttu-id="c1de1-726">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-726">10001</span></span></td>
<td><span data-ttu-id="c1de1-727">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-727">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-728">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-728">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="c1de1-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-730">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="c1de1-731">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-731">Prod 1</span></span></td>
<td><span data-ttu-id="c1de1-732">Toode 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-732">Product 1</span></span></td>
<td><span data-ttu-id="c1de1-733">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-733">10001</span></span></td>
<td><span data-ttu-id="c1de1-734">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-734">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-735">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-735">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-736">776.36</span><span class="sxs-lookup"><span data-stu-id="c1de1-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-737">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="c1de1-738">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-738">Prod 1</span></span></td>
<td><span data-ttu-id="c1de1-739">Toode 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-739">Product 1</span></span></td>
<td><span data-ttu-id="c1de1-740">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-740">10001</span></span></td>
<td><span data-ttu-id="c1de1-741">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-741">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-742">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-742">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c1de1-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-744">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="c1de1-745">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-745">Prod 2</span></span></td>
<td><span data-ttu-id="c1de1-746">Toode 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-746">Product 1</span></span></td>
<td><span data-ttu-id="c1de1-747">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-747">10001</span></span></td>
<td><span data-ttu-id="c1de1-748">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-748">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-749">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-749">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-750">223.64</span><span class="sxs-lookup"><span data-stu-id="c1de1-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-751">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="c1de1-752">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-752">Prod 2</span></span></td>
<td><span data-ttu-id="c1de1-753">Toode 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-753">Product 1</span></span></td>
<td><span data-ttu-id="c1de1-754">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-754">10001</span></span></td>
<td><span data-ttu-id="c1de1-755">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-755">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-756">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-756">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c1de1-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c1de1-758">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="c1de1-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c1de1-759">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c1de1-760">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="c1de1-760">Cost element</span></span></th>
<th><span data-ttu-id="c1de1-761">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="c1de1-761">Cost behavior</span></span></th>
<th><span data-ttu-id="c1de1-762">Summa</span><span class="sxs-lookup"><span data-stu-id="c1de1-762">Amount</span></span></th>
<th><span data-ttu-id="c1de1-763">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="c1de1-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c1de1-764">CC001</span><span class="sxs-lookup"><span data-stu-id="c1de1-764">CC001</span></span></td>
<td><span data-ttu-id="c1de1-765">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="c1de1-765">HR</span></span></td>
<td><span data-ttu-id="c1de1-766">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-766">10001</span></span></td>
<td><span data-ttu-id="c1de1-767">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-767">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-768">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-768">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-769">‑500,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-769">-500.00</span></span></td>
<td><span data-ttu-id="c1de1-770">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-771">CC002</span><span class="sxs-lookup"><span data-stu-id="c1de1-771">CC002</span></span></td>
<td><span data-ttu-id="c1de1-772">Finantsid</span><span class="sxs-lookup"><span data-stu-id="c1de1-772">Finance</span></span></td>
<td><span data-ttu-id="c1de1-773">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-773">10001</span></span></td>
<td><span data-ttu-id="c1de1-774">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-774">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-775">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-775">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-776">175.00</span><span class="sxs-lookup"><span data-stu-id="c1de1-776">175.00</span></span></td>
<td><span data-ttu-id="c1de1-777">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-778">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-778">CC003</span></span></td>
<td><span data-ttu-id="c1de1-779">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-779">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-780">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-780">10001</span></span></td>
<td><span data-ttu-id="c1de1-781">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-781">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-782">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-782">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-783">275.00</span><span class="sxs-lookup"><span data-stu-id="c1de1-783">275.00</span></span></td>
<td><span data-ttu-id="c1de1-784">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-785">CC004</span><span class="sxs-lookup"><span data-stu-id="c1de1-785">CC004</span></span></td>
<td><span data-ttu-id="c1de1-786">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="c1de1-786">Packaging</span></span></td>
<td><span data-ttu-id="c1de1-787">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-787">10001</span></span></td>
<td><span data-ttu-id="c1de1-788">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-788">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-789">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-789">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-790">50,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-790">50,00</span></span></td>
<td><span data-ttu-id="c1de1-791">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-792">CC001</span><span class="sxs-lookup"><span data-stu-id="c1de1-792">CC001</span></span></td>
<td><span data-ttu-id="c1de1-793">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="c1de1-793">HR</span></span></td>
<td><span data-ttu-id="c1de1-794">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-794">10001</span></span></td>
<td><span data-ttu-id="c1de1-795">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-795">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-796">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-796">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-797">–1245,71</span><span class="sxs-lookup"><span data-stu-id="c1de1-797">-1,245.71</span></span></td>
<td><span data-ttu-id="c1de1-798">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-799">CC002</span><span class="sxs-lookup"><span data-stu-id="c1de1-799">CC002</span></span></td>
<td><span data-ttu-id="c1de1-800">Finantsid</span><span class="sxs-lookup"><span data-stu-id="c1de1-800">Finance</span></span></td>
<td><span data-ttu-id="c1de1-801">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-801">10001</span></span></td>
<td><span data-ttu-id="c1de1-802">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-802">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-803">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-803">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-804">436.00</span><span class="sxs-lookup"><span data-stu-id="c1de1-804">436.00</span></span></td>
<td><span data-ttu-id="c1de1-805">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-806">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-806">CC003</span></span></td>
<td><span data-ttu-id="c1de1-807">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-807">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-808">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-808">10001</span></span></td>
<td><span data-ttu-id="c1de1-809">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-809">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-810">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-810">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-811">685.14</span><span class="sxs-lookup"><span data-stu-id="c1de1-811">685.14</span></span></td>
<td><span data-ttu-id="c1de1-812">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-813">CC004</span><span class="sxs-lookup"><span data-stu-id="c1de1-813">CC004</span></span></td>
<td><span data-ttu-id="c1de1-814">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="c1de1-814">Packaging</span></span></td>
<td><span data-ttu-id="c1de1-815">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-815">10001</span></span></td>
<td><span data-ttu-id="c1de1-816">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-816">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-817">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-817">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-818">124.57</span><span class="sxs-lookup"><span data-stu-id="c1de1-818">124.57</span></span></td>
<td><span data-ttu-id="c1de1-819">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-820">CC002</span><span class="sxs-lookup"><span data-stu-id="c1de1-820">CC002</span></span></td>
<td><span data-ttu-id="c1de1-821">Finantsid</span><span class="sxs-lookup"><span data-stu-id="c1de1-821">Finance</span></span></td>
<td><span data-ttu-id="c1de1-822">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-822">10001</span></span></td>
<td><span data-ttu-id="c1de1-823">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-823">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-824">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-824">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-825">–675,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-825">-675.00</span></span></td>
<td><span data-ttu-id="c1de1-826">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-827">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-827">CC003</span></span></td>
<td><span data-ttu-id="c1de1-828">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-828">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-829">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-829">10001</span></span></td>
<td><span data-ttu-id="c1de1-830">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-830">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-831">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-831">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-832">438.75</span><span class="sxs-lookup"><span data-stu-id="c1de1-832">438.75</span></span></td>
<td><span data-ttu-id="c1de1-833">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-834">CC004</span><span class="sxs-lookup"><span data-stu-id="c1de1-834">CC004</span></span></td>
<td><span data-ttu-id="c1de1-835">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="c1de1-835">Packaging</span></span></td>
<td><span data-ttu-id="c1de1-836">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-836">10001</span></span></td>
<td><span data-ttu-id="c1de1-837">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-837">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-838">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-838">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-839">236.25</span><span class="sxs-lookup"><span data-stu-id="c1de1-839">236.25</span></span></td>
<td><span data-ttu-id="c1de1-840">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-841">CC002</span><span class="sxs-lookup"><span data-stu-id="c1de1-841">CC002</span></span></td>
<td><span data-ttu-id="c1de1-842">Finantsid</span><span class="sxs-lookup"><span data-stu-id="c1de1-842">Finance</span></span></td>
<td><span data-ttu-id="c1de1-843">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-843">10001</span></span></td>
<td><span data-ttu-id="c1de1-844">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-844">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-845">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-845">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-846">–8150,29</span><span class="sxs-lookup"><span data-stu-id="c1de1-846">-8,150.29</span></span></td>
<td><span data-ttu-id="c1de1-847">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-848">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-848">CC003</span></span></td>
<td><span data-ttu-id="c1de1-849">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-849">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-850">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-850">10001</span></span></td>
<td><span data-ttu-id="c1de1-851">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-851">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-852">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-852">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c1de1-853">5,297.69</span></span></td>
<td><span data-ttu-id="c1de1-854">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-855">CC004</span><span class="sxs-lookup"><span data-stu-id="c1de1-855">CC004</span></span></td>
<td><span data-ttu-id="c1de1-856">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="c1de1-856">Packaging</span></span></td>
<td><span data-ttu-id="c1de1-857">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-857">10001</span></span></td>
<td><span data-ttu-id="c1de1-858">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-858">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-859">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-859">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c1de1-860">2,852.60</span></span></td>
<td><span data-ttu-id="c1de1-861">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-862">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-862">CC003</span></span></td>
<td><span data-ttu-id="c1de1-863">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-863">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-864">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-864">10001</span></span></td>
<td><span data-ttu-id="c1de1-865">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-865">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-866">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-866">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-867">–713,75</span><span class="sxs-lookup"><span data-stu-id="c1de1-867">-713.75</span></span></td>
<td><span data-ttu-id="c1de1-868">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-869">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-869">Prod 1</span></span></td>
<td><span data-ttu-id="c1de1-870">Toode 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-870">Product 1</span></span></td>
<td><span data-ttu-id="c1de1-871">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-871">10001</span></span></td>
<td><span data-ttu-id="c1de1-872">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-872">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-873">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-873">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-874">535.31</span><span class="sxs-lookup"><span data-stu-id="c1de1-874">535.31</span></span></td>
<td><span data-ttu-id="c1de1-875">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-876">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-876">Prod 2</span></span></td>
<td><span data-ttu-id="c1de1-877">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-877">Product 2</span></span></td>
<td><span data-ttu-id="c1de1-878">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-878">10001</span></span></td>
<td><span data-ttu-id="c1de1-879">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-879">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-880">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-880">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-881">178.44</span><span class="sxs-lookup"><span data-stu-id="c1de1-881">178.44</span></span></td>
<td><span data-ttu-id="c1de1-882">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-883">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-883">CC003</span></span></td>
<td><span data-ttu-id="c1de1-884">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-884">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-885">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-885">10001</span></span></td>
<td><span data-ttu-id="c1de1-886">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-886">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-887">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-887">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-888">–5982,83</span><span class="sxs-lookup"><span data-stu-id="c1de1-888">-5,982.83</span></span></td>
<td><span data-ttu-id="c1de1-889">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-890">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-890">Prod 1</span></span></td>
<td><span data-ttu-id="c1de1-891">Toode 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-891">Product 1</span></span></td>
<td><span data-ttu-id="c1de1-892">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-892">10001</span></span></td>
<td><span data-ttu-id="c1de1-893">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-893">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-894">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-894">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c1de1-895">4,487.12</span></span></td>
<td><span data-ttu-id="c1de1-896">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-897">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-897">Prod 2</span></span></td>
<td><span data-ttu-id="c1de1-898">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-898">Product 2</span></span></td>
<td><span data-ttu-id="c1de1-899">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-899">10001</span></span></td>
<td><span data-ttu-id="c1de1-900">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-900">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-901">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-901">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c1de1-902">1,495.71</span></span></td>
<td><span data-ttu-id="c1de1-903">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-904">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-904">CC003</span></span></td>
<td><span data-ttu-id="c1de1-905">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-905">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-906">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-906">10001</span></span></td>
<td><span data-ttu-id="c1de1-907">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-907">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-908">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-908">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-909">–286,25</span><span class="sxs-lookup"><span data-stu-id="c1de1-909">-286.25</span></span></td>
<td><span data-ttu-id="c1de1-910">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-911">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-911">Prod 1</span></span></td>
<td><span data-ttu-id="c1de1-912">Toode 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-912">Product 1</span></span></td>
<td><span data-ttu-id="c1de1-913">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-913">10001</span></span></td>
<td><span data-ttu-id="c1de1-914">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-914">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-915">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-915">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-916">241.05</span><span class="sxs-lookup"><span data-stu-id="c1de1-916">241.05</span></span></td>
<td><span data-ttu-id="c1de1-917">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-918">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-918">Prod 2</span></span></td>
<td><span data-ttu-id="c1de1-919">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-919">Product 2</span></span></td>
<td><span data-ttu-id="c1de1-920">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-920">10001</span></span></td>
<td><span data-ttu-id="c1de1-921">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-921">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-922">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-922">Fixed cost</span></span></td>
<td><span data-ttu-id="c1de1-923">45.20</span><span class="sxs-lookup"><span data-stu-id="c1de1-923">45.20</span></span></td>
<td><span data-ttu-id="c1de1-924">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-925">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-925">CC003</span></span></td>
<td><span data-ttu-id="c1de1-926">Assembler</span><span class="sxs-lookup"><span data-stu-id="c1de1-926">Assembly</span></span></td>
<td><span data-ttu-id="c1de1-927">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-927">10001</span></span></td>
<td><span data-ttu-id="c1de1-928">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-928">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-929">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-929">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-930">–2977,17</span><span class="sxs-lookup"><span data-stu-id="c1de1-930">-2,977.17</span></span></td>
<td><span data-ttu-id="c1de1-931">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-932">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-932">Prod 1</span></span></td>
<td><span data-ttu-id="c1de1-933">Toode 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-933">Product 1</span></span></td>
<td><span data-ttu-id="c1de1-934">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-934">10001</span></span></td>
<td><span data-ttu-id="c1de1-935">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-935">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-936">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-936">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c1de1-937">2,507.09</span></span></td>
<td><span data-ttu-id="c1de1-938">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c1de1-939">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-939">Prod 2</span></span></td>
<td><span data-ttu-id="c1de1-940">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-940">Product 2</span></span></td>
<td><span data-ttu-id="c1de1-941">10001</span><span class="sxs-lookup"><span data-stu-id="c1de1-941">10001</span></span></td>
<td><span data-ttu-id="c1de1-942">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="c1de1-942">Electricity</span></span></td>
<td><span data-ttu-id="c1de1-943">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-943">Variable cost</span></span></td>
<td><span data-ttu-id="c1de1-944">470.08</span><span class="sxs-lookup"><span data-stu-id="c1de1-944">470.08</span></span></td>
<td><span data-ttu-id="c1de1-945">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="c1de1-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="c1de1-946">Lõppsõna</span><span class="sxs-lookup"><span data-stu-id="c1de1-946">Conclusion</span></span>
<span data-ttu-id="c1de1-947">Finantsaruandluses sisestatakse elektrikulu 10 000,00 fiktiivse kulukeskuse ID-le.</span><span class="sxs-lookup"><span data-stu-id="c1de1-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="c1de1-948">Nii teavad kuluarvestajad, et see kulu tuleb eraldada.</span><span class="sxs-lookup"><span data-stu-id="c1de1-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="c1de1-949">Kuluarvestuses liigub kulu rakendatud poliitikate ja reeglite põhjal läbi organisatsiooniüksuste ja -tasemete.</span><span class="sxs-lookup"><span data-stu-id="c1de1-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="c1de1-950">Iga kulu on seostatud eraldamisalusega, mis pakub kulude eraldamiseks parimat hinnangut.</span><span class="sxs-lookup"><span data-stu-id="c1de1-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="c1de1-951">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="c1de1-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="c1de1-952">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="c1de1-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="c1de1-953">Kokku</span><span class="sxs-lookup"><span data-stu-id="c1de1-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c1de1-954">CC099</span><span class="sxs-lookup"><span data-stu-id="c1de1-954">CC099</span></span></th>
<th><span data-ttu-id="c1de1-955">CC001</span><span class="sxs-lookup"><span data-stu-id="c1de1-955">CC001</span></span></th>
<th><span data-ttu-id="c1de1-956">CC002</span><span class="sxs-lookup"><span data-stu-id="c1de1-956">CC002</span></span></th>
<th><span data-ttu-id="c1de1-957">CC003</span><span class="sxs-lookup"><span data-stu-id="c1de1-957">CC003</span></span></th>
<th><span data-ttu-id="c1de1-958">CC004</span><span class="sxs-lookup"><span data-stu-id="c1de1-958">CC004</span></span></th>
<th><span data-ttu-id="c1de1-959">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-959">Proj 1</span></span></th>
<th><span data-ttu-id="c1de1-960">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-960">Proj 2</span></span></th>
<th><span data-ttu-id="c1de1-961">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="c1de1-961">Prod 1</span></span></th>
<th><span data-ttu-id="c1de1-962">Toode 2</span><span class="sxs-lookup"><span data-stu-id="c1de1-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="c1de1-963">10001 Elekter</span><span class="sxs-lookup"><span data-stu-id="c1de1-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="c1de1-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-965"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="c1de1-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-966"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="c1de1-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-967"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="c1de1-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-968"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="c1de1-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-969"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="c1de1-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-970"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="c1de1-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-971"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="c1de1-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-972"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="c1de1-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="c1de1-973">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="c1de1-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-974">0,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="c1de1-975">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-976">0,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-977">0,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-978">0,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-979">0,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-980">0,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-981">776.36</span><span class="sxs-lookup"><span data-stu-id="c1de1-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-982">223.64</span><span class="sxs-lookup"><span data-stu-id="c1de1-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-983"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="c1de1-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="c1de1-984">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="c1de1-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-985">000</span><span class="sxs-lookup"><span data-stu-id="c1de1-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-986">0,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-987">0,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-988">0,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-989">0,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-990">30,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-991">10,00</span><span class="sxs-lookup"><span data-stu-id="c1de1-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c1de1-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c1de1-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c1de1-994"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="c1de1-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c1de1-995">Selles teemas selgitatakse, kuidas esmane kuluelement, 10001 Eleter, liigub läbi kuluobjektide.</span><span class="sxs-lookup"><span data-stu-id="c1de1-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="c1de1-996">Seega eraldatakse see üldkulu organisatsiooni madalaimale tasemele.</span><span class="sxs-lookup"><span data-stu-id="c1de1-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="c1de1-997">Teisisõnu kannavad kulu madalaimal tasemel olevad kuluobjektid.</span><span class="sxs-lookup"><span data-stu-id="c1de1-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="c1de1-998">Kui soovite saada kuluobjektide vahelisest kuluvoost visuaalset ülevaadet, saate kuluvoo visualiseerimiseks kasutada kulude kokkuvõtte poliitika reegleid.</span><span class="sxs-lookup"><span data-stu-id="c1de1-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="c1de1-999">Täpsemat teavet vaadake jaotisest Kulude kokkuvõtte poliitika.</span><span class="sxs-lookup"><span data-stu-id="c1de1-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="c1de1-1000">(Pange tähele, et see teema pole veel valmis, kuid see tuleb peagi.)</span><span class="sxs-lookup"><span data-stu-id="c1de1-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




