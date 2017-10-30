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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: e57db8f4b692aa9c27916625897e268f63031782
ms.openlocfilehash: 285799d70a945c2dae1e3c65296282d5c432a243
ms.contentlocale: et-ee
ms.lasthandoff: 10/30/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="b7bb2-103">Üldkulude arvutus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b7bb2-104">Selles teemas kirjeldatakse tüüpilisi üldkulude arvutamise ja eraldamise protsesse.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="b7bb2-105">Mõiste määratlus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-105">Term definition</span></span>
---------------

<span data-ttu-id="b7bb2-106">Üldkulud on kulud, mis kaasnevad ettevõtte käitamisega, kuid mida ei saa seostada otseselt ühegi kindla äritegevuse, toote ega teenusega.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="b7bb2-107">Üldkulud pakuvad kriitilist tuge kasumit andavate tegevuste loomisele.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="b7bb2-108">Siin on mõned näited üldkuludest.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="b7bb2-109">Üür</span><span class="sxs-lookup"><span data-stu-id="b7bb2-109">Rent</span></span>
-   <span data-ttu-id="b7bb2-110">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-110">Electricity</span></span>
-   <span data-ttu-id="b7bb2-111">Haldustasud</span><span class="sxs-lookup"><span data-stu-id="b7bb2-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="b7bb2-112">Üldkulude arvutuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="b7bb2-112">Overhead calculation overview</span></span>
<span data-ttu-id="b7bb2-113">Üldkulude arvutus käitab kuluarvutuse poliitikaid õiges järjekorras.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="b7bb2-114">Saate käivitada üldkulude arvutuse sama rahandusperioodi kohta mitu korda, kui kuluarvestuse poliitikaid on muudetud või tuvastatud teatud tõrked.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="b7bb2-115">Iga üldkulude arvutamise käitamine talletatakse ja see saab kordumatu versiooni-ID, mis võimaldab teil arvutuste erinevaid versioone võrrelda.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="b7bb2-116">Ülekulude arvutusega loodud kulukirjed saavad aruandluskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="b7bb2-117">See aruandluskuupäev vastab arvutuses kasutatud rahandusperioodi lõppkuupäevale.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="b7bb2-118">Kordumatu versiooni-ID koosneb järgmistest elementidest.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="b7bb2-119">Versiooni tüüp</span><span class="sxs-lookup"><span data-stu-id="b7bb2-119">Version type</span></span>
-   <span data-ttu-id="b7bb2-120">Kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="b7bb2-120">Date and time</span></span>
-   <span data-ttu-id="b7bb2-121">Kuluarvestuse pearaamat</span><span class="sxs-lookup"><span data-stu-id="b7bb2-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="b7bb2-122">Finantsaasta</span><span class="sxs-lookup"><span data-stu-id="b7bb2-122">Fiscal year</span></span>
-   <span data-ttu-id="b7bb2-123">Rahandusperiood</span><span class="sxs-lookup"><span data-stu-id="b7bb2-123">Fiscal period</span></span>

<span data-ttu-id="b7bb2-124">Üldkulude arvutus käivitatakse versioonist sõltumatult.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="b7bb2-125">Seetõttu saate arvutada eelarveversiooni enne tegelikku versiooni.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="b7bb2-126">Üldkulude arvutus koosneb neljast etapist, nagu näha alltoodud joonisel.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="b7bb2-127">Igas etapis luuakse töölehe päis, millel on töölehe kanded.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="b7bb2-128">See töölehe päis säiiltab sisendandmeid iga arvutusetapi kohta.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="b7bb2-129">Igale töölehe reale rakendatakse poliitikad ja reeglid ning väljundina luuakse kulukirjed.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="b7bb2-130">Seega on teil alati olemas põhjalik ülevaade.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="b7bb2-131">[![Üldkulude arvutus](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="b7bb2-132">Elektri üldkulude arvutamine ja eraldamine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="b7bb2-133">Finantsaruandluses on mõned kulud, näiteks elekter, registreeritud põhisummana.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="b7bb2-134">Seetõttu ei pakuta kuluarvestuseks üksikasjalikku juhtimisülevaadet.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="b7bb2-135">Kuluarvestuses peavad kulud liikuma läbi organisatsiooniüksuste, et pakkuda korrektset juhtimisülevaadet kõigi organisatsiooniüksuste ja -tasemete kohta.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="b7bb2-136">See voog peab põhinema tarbimise või õiglase hindamise täpsel kirjendamisel.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="b7bb2-137">Pearaamatus, saab elektrikulu sisestada nii, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7bb2-138">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b7bb2-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b7bb2-139">Kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="b7bb2-140">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="b7bb2-140">Main account</span></span></th>
<th><span data-ttu-id="b7bb2-141">Summa arvestusvaluutas</span><span class="sxs-lookup"><span data-stu-id="b7bb2-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-142">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-143">CC099</span><span class="sxs-lookup"><span data-stu-id="b7bb2-143">CC099</span></span></td>
<td><span data-ttu-id="b7bb2-144">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-144">Default cost center</span></span></td>
<td><span data-ttu-id="b7bb2-145">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-145">10001</span></span></td>
<td><span data-ttu-id="b7bb2-146">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-146">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="b7bb2-148">1. etapp: kulukäitumise arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="b7bb2-149">Vaikimisi saavad lähteandmetest imporditud kulukirjed kuluarvestuses kulukäitumise klassifikatsiooniks **Klassifitseerimata**.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="b7bb2-150">Kulukäitumise poliitikareegleid rakendades saate kulukirjed ümber klassifitseerida kui **Fikseeritud kulu** või **Muutuvkulu**.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="b7bb2-151">Kulukäitumise reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-151">Define the cost behavior rule</span></span>

<span data-ttu-id="b7bb2-152">Mõnikord on osa kulust fikseeritud tasu ja järelejäänud kulu põhineb tarbimisel.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="b7bb2-153">Elektriarved vastavad sageli sellele määratlusele.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="b7bb2-154">Pärast kindla fikseeritud tasu maksmist maksate tarbimise eest kilovatt-tunni (Kwh) kohta.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="b7bb2-155">Näiteks kui fikseeritud kulu tasu on 1000,00 eurot, määratletakse kulukäitumise reegel järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="b7bb2-156">Fikseeritud summa: 1000,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="b7bb2-157">0 &lt;= 1000,00 = fikseeritud</span><span class="sxs-lookup"><span data-stu-id="b7bb2-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="b7bb2-158">1000,01 &lt; N = muutuja</span><span class="sxs-lookup"><span data-stu-id="b7bb2-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="b7bb2-159">Tööleht</span><span class="sxs-lookup"><span data-stu-id="b7bb2-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7bb2-160">Tööleht</span><span class="sxs-lookup"><span data-stu-id="b7bb2-160">Journal</span></span></th>
<th><span data-ttu-id="b7bb2-161">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="b7bb2-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b7bb2-162">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="b7bb2-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b7bb2-163">Versioon</span><span class="sxs-lookup"><span data-stu-id="b7bb2-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-164">00001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-164">00001</span></span></td>
<td><span data-ttu-id="b7bb2-165">Kulukäitumise arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="b7bb2-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="b7bb2-166">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="b7bb2-166">Fiscal</span></span></td>
<td><span data-ttu-id="b7bb2-167">2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-167">2017</span></span></td>
<td><span data-ttu-id="b7bb2-168">Periood 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-168">Period 1</span></span></td>
<td><span data-ttu-id="b7bb2-169">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="b7bb2-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b7bb2-170">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7bb2-171">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b7bb2-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b7bb2-172">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b7bb2-173">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b7bb2-173">Cost element</span></span></th>
<th><span data-ttu-id="b7bb2-174">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-174">Cost behavior</span></span></th>
<th><span data-ttu-id="b7bb2-175">Summa</span><span class="sxs-lookup"><span data-stu-id="b7bb2-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-176">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-177">CC099</span><span class="sxs-lookup"><span data-stu-id="b7bb2-177">CC099</span></span></td>
<td><span data-ttu-id="b7bb2-178">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-178">Default cost center</span></span></td>
<td><span data-ttu-id="b7bb2-179">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-179">10001</span></span></td>
<td><span data-ttu-id="b7bb2-180">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-180">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-181">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="b7bb2-181">Unclassified</span></span></td>
<td><span data-ttu-id="b7bb2-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b7bb2-183">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="b7bb2-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-184">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b7bb2-185">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b7bb2-185">Cost element</span></span></th>
<th><span data-ttu-id="b7bb2-186">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-186">Cost behavior</span></span></th>
<th><span data-ttu-id="b7bb2-187">Summa</span><span class="sxs-lookup"><span data-stu-id="b7bb2-187">Amount</span></span></th>
<th><span data-ttu-id="b7bb2-188">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b7bb2-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-189">CC099</span><span class="sxs-lookup"><span data-stu-id="b7bb2-189">CC099</span></span></td>
<td><span data-ttu-id="b7bb2-190">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-190">Default cost center</span></span></td>
<td><span data-ttu-id="b7bb2-191">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-191">10001</span></span></td>
<td><span data-ttu-id="b7bb2-192">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-192">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-193">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="b7bb2-193">Unclassified</span></span></td>
<td><span data-ttu-id="b7bb2-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-194">10,000.00</span></span></td>
<td><span data-ttu-id="b7bb2-195">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-196">CC099</span><span class="sxs-lookup"><span data-stu-id="b7bb2-196">CC099</span></span></td>
<td><span data-ttu-id="b7bb2-197">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-197">Default cost center</span></span></td>
<td><span data-ttu-id="b7bb2-198">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-198">10001</span></span></td>
<td><span data-ttu-id="b7bb2-199">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-199">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-200">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="b7bb2-200">Unclassified</span></span></td>
<td><span data-ttu-id="b7bb2-201">–10 000,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-201">-10,000.00</span></span></td>
<td><span data-ttu-id="b7bb2-202">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-203">CC099</span><span class="sxs-lookup"><span data-stu-id="b7bb2-203">CC099</span></span></td>
<td><span data-ttu-id="b7bb2-204">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-204">Default cost center</span></span></td>
<td><span data-ttu-id="b7bb2-205">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-205">10001</span></span></td>
<td><span data-ttu-id="b7bb2-206">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-206">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-207">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-207">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-208">1,000.00</span></span></td>
<td><span data-ttu-id="b7bb2-209">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-210">CC099</span><span class="sxs-lookup"><span data-stu-id="b7bb2-210">CC099</span></span></td>
<td><span data-ttu-id="b7bb2-211">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-211">Default cost center</span></span></td>
<td><span data-ttu-id="b7bb2-212">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-212">10001</span></span></td>
<td><span data-ttu-id="b7bb2-213">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-213">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-214">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-214">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-215">9,000.00</span></span></td>
<td><span data-ttu-id="b7bb2-216">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7bb2-217">Üksikasjalikku teavet kulukäitumise kohta vt jaotisest Kulukäitumise poliitika.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="b7bb2-218">(Pange tähele, et see teema pole veel valmis, kuid see tuleb peagi.)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="b7bb2-219">2. etapp: kulujaotuse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="b7bb2-220">Kulujaotust kasutatakse kulu ümberjaotamiseks ühelt kuluobjektilt ühele või mitmele teisele kuluobjektile, rakendades asjakohast eraldusalust.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="b7bb2-221">Kulujaotus ja kulueraldus erinevad selle poolest, et kulujaotus toimub alati algse kulu esmase kuluelemendi tasemel.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="b7bb2-222">Kulujaotuse reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-222">Define the cost distribution rule</span></span>

<span data-ttu-id="b7bb2-223">Finantsaruandluses registreeritakse elektrikulud sageli põhisummana.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="b7bb2-224">Kuluarvestuseses ei ole see lähenemine piisavalt üksikasjalik.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="b7bb2-225">Muutuvkulu tuleb jaotada üksikutele kuluobjektidele õigluse alusel.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="b7bb2-226">Kõige loogilisem eraldamisalus on elektritarbimine (kWh).</span><span class="sxs-lookup"><span data-stu-id="b7bb2-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="b7bb2-227">Luuakse statistilise dimensiooni liige nimega Elekter ja elektritarbimine on kirjendatakse.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="b7bb2-228">Vaikimisi muutuvad kõik statistilise dimensiooni liikmed eraldamisalusena kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-229">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-229">Cost object</span></span></th>
<th><span data-ttu-id="b7bb2-230">kWh</span><span class="sxs-lookup"><span data-stu-id="b7bb2-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-231">CC001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-231">CC001</span></span></td>
<td><span data-ttu-id="b7bb2-232">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b7bb2-232">HR</span></span></td>
<td><span data-ttu-id="b7bb2-233">1000</span><span class="sxs-lookup"><span data-stu-id="b7bb2-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-234">CC002</span><span class="sxs-lookup"><span data-stu-id="b7bb2-234">CC002</span></span></td>
<td><span data-ttu-id="b7bb2-235">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b7bb2-235">Finance</span></span></td>
<td><span data-ttu-id="b7bb2-236">6,000</span><span class="sxs-lookup"><span data-stu-id="b7bb2-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-237">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-237">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-238">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-238">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-239">0</span><span class="sxs-lookup"><span data-stu-id="b7bb2-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7bb2-240">Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-241">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-241">Cost object</span></span></th>
<th><span data-ttu-id="b7bb2-242">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-242">Magnitude</span></span></th>
<th><span data-ttu-id="b7bb2-243">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="b7bb2-243">Allocation factor</span></span></th>
<th><span data-ttu-id="b7bb2-244">Summa</span><span class="sxs-lookup"><span data-stu-id="b7bb2-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-245">CC001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-245">CC001</span></span></td>
<td><span data-ttu-id="b7bb2-246">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b7bb2-246">HR</span></span></td>
<td><span data-ttu-id="b7bb2-247">1000</span><span class="sxs-lookup"><span data-stu-id="b7bb2-247">1,000</span></span></td>
<td><span data-ttu-id="b7bb2-248">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b7bb2-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="b7bb2-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-250">CC002</span><span class="sxs-lookup"><span data-stu-id="b7bb2-250">CC002</span></span></td>
<td><span data-ttu-id="b7bb2-251">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b7bb2-251">Finance</span></span></td>
<td><span data-ttu-id="b7bb2-252">6,000</span><span class="sxs-lookup"><span data-stu-id="b7bb2-252">6,000</span></span></td>
<td><span data-ttu-id="b7bb2-253">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b7bb2-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="b7bb2-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-255">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-255">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-256">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-256">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-257">0</span><span class="sxs-lookup"><span data-stu-id="b7bb2-257">0</span></span></td>
<td><span data-ttu-id="b7bb2-258">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b7bb2-259">0,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7bb2-260">Fikseeritud kulu tuleb jaotada ühtlaselt üksikutele kuluobjektidele, mis on tarbinud elektrit.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="b7bb2-261">Selle tulemuse saate, kasutades valemi eraldamisaluses statistilise dimensiooni liiget Elekter: (Elekter &gt; 0,00). Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-262">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-262">Cost object</span></span></th>
<th><span data-ttu-id="b7bb2-263">Valem</span><span class="sxs-lookup"><span data-stu-id="b7bb2-263">Formula</span></span></th>
<th><span data-ttu-id="b7bb2-264">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-264">Magnitude</span></span></th>
<th><span data-ttu-id="b7bb2-265">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="b7bb2-265">Allocation factor</span></span></th>
<th><span data-ttu-id="b7bb2-266">Summa</span><span class="sxs-lookup"><span data-stu-id="b7bb2-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-267">CC001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-267">CC001</span></span></td>
<td><span data-ttu-id="b7bb2-268">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b7bb2-268">HR</span></span></td>
<td><span data-ttu-id="b7bb2-269">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b7bb2-270">1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-270">1</span></span></td>
<td><span data-ttu-id="b7bb2-271">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b7bb2-272">500,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-273">CC002</span><span class="sxs-lookup"><span data-stu-id="b7bb2-273">CC002</span></span></td>
<td><span data-ttu-id="b7bb2-274">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b7bb2-274">Finance</span></span></td>
<td><span data-ttu-id="b7bb2-275">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b7bb2-276">1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-276">1</span></span></td>
<td><span data-ttu-id="b7bb2-277">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b7bb2-278">500,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-279">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-279">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-280">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-280">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b7bb2-282">0</span><span class="sxs-lookup"><span data-stu-id="b7bb2-282">0</span></span></td>
<td><span data-ttu-id="b7bb2-283">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b7bb2-284">0,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="b7bb2-285">Tööleht</span><span class="sxs-lookup"><span data-stu-id="b7bb2-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7bb2-286">Tööleht</span><span class="sxs-lookup"><span data-stu-id="b7bb2-286">Journal</span></span></th>
<th><span data-ttu-id="b7bb2-287">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="b7bb2-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b7bb2-288">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="b7bb2-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b7bb2-289">Versioon</span><span class="sxs-lookup"><span data-stu-id="b7bb2-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-290">00002</span><span class="sxs-lookup"><span data-stu-id="b7bb2-290">00002</span></span></td>
<td><span data-ttu-id="b7bb2-291">Kulujaotuse arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="b7bb2-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="b7bb2-292">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="b7bb2-292">Fiscal</span></span></td>
<td><span data-ttu-id="b7bb2-293">2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-293">2017</span></span></td>
<td><span data-ttu-id="b7bb2-294">Periood 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-294">Period 1</span></span></td>
<td><span data-ttu-id="b7bb2-295">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="b7bb2-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b7bb2-296">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7bb2-297">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b7bb2-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b7bb2-298">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b7bb2-299">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b7bb2-299">Cost element</span></span></th>
<th><span data-ttu-id="b7bb2-300">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-300">Cost behavior</span></span></th>
<th><span data-ttu-id="b7bb2-301">Summa</span><span class="sxs-lookup"><span data-stu-id="b7bb2-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-302">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-303">CC099</span><span class="sxs-lookup"><span data-stu-id="b7bb2-303">CC099</span></span></td>
<td><span data-ttu-id="b7bb2-304">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-304">Default cost center</span></span></td>
<td><span data-ttu-id="b7bb2-305">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-305">10001</span></span></td>
<td><span data-ttu-id="b7bb2-306">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-306">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-307">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-307">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-308">1 000,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-309">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-310">CC099</span><span class="sxs-lookup"><span data-stu-id="b7bb2-310">CC099</span></span></td>
<td><span data-ttu-id="b7bb2-311">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-311">Default cost center</span></span></td>
<td><span data-ttu-id="b7bb2-312">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-312">10001</span></span></td>
<td><span data-ttu-id="b7bb2-313">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-313">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-314">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-314">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b7bb2-316">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="b7bb2-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-317">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b7bb2-318">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b7bb2-318">Cost element</span></span></th>
<th><span data-ttu-id="b7bb2-319">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-319">Cost behavior</span></span></th>
<th><span data-ttu-id="b7bb2-320">Summa</span><span class="sxs-lookup"><span data-stu-id="b7bb2-320">Amount</span></span></th>
<th><span data-ttu-id="b7bb2-321">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b7bb2-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-322">CC099</span><span class="sxs-lookup"><span data-stu-id="b7bb2-322">CC099</span></span></td>
<td><span data-ttu-id="b7bb2-323">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-323">Default cost center</span></span></td>
<td><span data-ttu-id="b7bb2-324">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-324">10001</span></span></td>
<td><span data-ttu-id="b7bb2-325">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-325">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-326">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-326">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-327">–1000,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-327">-1,000.00</span></span></td>
<td><span data-ttu-id="b7bb2-328">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-329">CC001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-329">CC001</span></span></td>
<td><span data-ttu-id="b7bb2-330">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b7bb2-330">HR</span></span></td>
<td><span data-ttu-id="b7bb2-331">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-331">10001</span></span></td>
<td><span data-ttu-id="b7bb2-332">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-332">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-333">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-333">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-334">500,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-334">500.00</span></span></td>
<td><span data-ttu-id="b7bb2-335">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-336">CC002</span><span class="sxs-lookup"><span data-stu-id="b7bb2-336">CC002</span></span></td>
<td><span data-ttu-id="b7bb2-337">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b7bb2-337">Finance</span></span></td>
<td><span data-ttu-id="b7bb2-338">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-338">10001</span></span></td>
<td><span data-ttu-id="b7bb2-339">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-339">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-340">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-340">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-341">500,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-341">500.00</span></span></td>
<td><span data-ttu-id="b7bb2-342">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-343">CC099</span><span class="sxs-lookup"><span data-stu-id="b7bb2-343">CC099</span></span></td>
<td><span data-ttu-id="b7bb2-344">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-344">Default cost center</span></span></td>
<td><span data-ttu-id="b7bb2-345">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-345">10001</span></span></td>
<td><span data-ttu-id="b7bb2-346">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-346">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-347">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-347">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-348">–9000,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-348">-9,000.00</span></span></td>
<td><span data-ttu-id="b7bb2-349">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-350">CC001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-350">CC001</span></span></td>
<td><span data-ttu-id="b7bb2-351">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b7bb2-351">HR</span></span></td>
<td><span data-ttu-id="b7bb2-352">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-352">10001</span></span></td>
<td><span data-ttu-id="b7bb2-353">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-353">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-354">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-354">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="b7bb2-355">1,285.71</span></span></td>
<td><span data-ttu-id="b7bb2-356">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-357">CC002</span><span class="sxs-lookup"><span data-stu-id="b7bb2-357">CC002</span></span></td>
<td><span data-ttu-id="b7bb2-358">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b7bb2-358">Finance</span></span></td>
<td><span data-ttu-id="b7bb2-359">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-359">10001</span></span></td>
<td><span data-ttu-id="b7bb2-360">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-360">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-361">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-361">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="b7bb2-362">7,714.29</span></span></td>
<td><span data-ttu-id="b7bb2-363">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7bb2-364">Üksikasjalikku teavet kulude jaotamise ja eraldamise aluse kohta vt jaotistest Kulujaotuse poliitika ja Eraldamisalused.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="b7bb2-365">(Pange tähele, et see teema pole veel valmis, kuid see tuleb peagi.)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="b7bb2-366">3. etapp: üldkulude määra arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="b7bb2-367">Üldkulude määra kasutatakse ühe või mitme kindla kuluobjekti debiteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="b7bb2-368">Tasu põhineb eelmääratud kulumääral ja väärtusel määratud eraldamisalusest.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="b7bb2-369">Üldkulu määra määratlemine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-369">Define the overhead rate</span></span>

<span data-ttu-id="b7bb2-370">Kuluobjekt CC001 inimressursid panustab sisemiste projektide kogumisse.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="b7bb2-371">Luuakse statistilise dimensiooni liige nimega Inimressursside projektid, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-372">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-372">Cost object</span></span></th>
<th><span data-ttu-id="b7bb2-373">Tunnid</span><span class="sxs-lookup"><span data-stu-id="b7bb2-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-374">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-374">Proj 1</span></span></td>
<td><span data-ttu-id="b7bb2-375">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-375">Project 1</span></span></td>
<td><span data-ttu-id="b7bb2-376">3</span><span class="sxs-lookup"><span data-stu-id="b7bb2-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-377">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-377">Proj 2</span></span></td>
<td><span data-ttu-id="b7bb2-378">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-378">Project 2</span></span></td>
<td><span data-ttu-id="b7bb2-379">1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7bb2-380">Määratletud on eelmääratud kulumäär kuluprojektide panusele.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-381">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-381">Cost object</span></span></th>
<th><span data-ttu-id="b7bb2-382">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b7bb2-382">Cost element</span></span></th>
<th><span data-ttu-id="b7bb2-383">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-383">Cost behavior</span></span></th>
<th><span data-ttu-id="b7bb2-384">Ühikud</span><span class="sxs-lookup"><span data-stu-id="b7bb2-384">Units</span></span></th>
<th><span data-ttu-id="b7bb2-385">Kurss</span><span class="sxs-lookup"><span data-stu-id="b7bb2-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-386">CC001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-386">CC001</span></span></td>
<td><span data-ttu-id="b7bb2-387">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b7bb2-387">HR</span></span></td>
<td><span data-ttu-id="b7bb2-388">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-388">10001</span></span></td>
<td><span data-ttu-id="b7bb2-389">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-389">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-390">1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-390">1</span></span></td>
<td><span data-ttu-id="b7bb2-391">10</span><span class="sxs-lookup"><span data-stu-id="b7bb2-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7bb2-392">Järgmises tabelis on näidatud tulemus, kui inimressursside projektid on rakendatud eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-393">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-393">Cost object</span></span></th>
<th><span data-ttu-id="b7bb2-394">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-394">Magnitude</span></span></th>
<th><span data-ttu-id="b7bb2-395">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b7bb2-395">Cost element</span></span></th>
<th><span data-ttu-id="b7bb2-396">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="b7bb2-396">Allocation factor</span></span></th>
<th><span data-ttu-id="b7bb2-397">Summa</span><span class="sxs-lookup"><span data-stu-id="b7bb2-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-398">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-398">Proj 1</span></span></td>
<td><span data-ttu-id="b7bb2-399">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-399">Project 1</span></span></td>
<td><span data-ttu-id="b7bb2-400">3</span><span class="sxs-lookup"><span data-stu-id="b7bb2-400">3</span></span></td>
<td><span data-ttu-id="b7bb2-401">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-401">10001</span></span></td>
<td><span data-ttu-id="b7bb2-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="b7bb2-403">30,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-404">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-404">Proj 2</span></span></td>
<td><span data-ttu-id="b7bb2-405">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-405">Project 2</span></span></td>
<td><span data-ttu-id="b7bb2-406">1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-406">1</span></span></td>
<td><span data-ttu-id="b7bb2-407">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-407">10001</span></span></td>
<td><span data-ttu-id="b7bb2-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="b7bb2-409">10,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="b7bb2-410">Tööleht</span><span class="sxs-lookup"><span data-stu-id="b7bb2-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7bb2-411">Tööleht</span><span class="sxs-lookup"><span data-stu-id="b7bb2-411">Journal</span></span></th>
<th><span data-ttu-id="b7bb2-412">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="b7bb2-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b7bb2-413">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="b7bb2-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b7bb2-414">Versioon</span><span class="sxs-lookup"><span data-stu-id="b7bb2-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-415">00003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-415">00003</span></span></td>
<td><span data-ttu-id="b7bb2-416">Üldkulu määra arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="b7bb2-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="b7bb2-417">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="b7bb2-417">Fiscal</span></span></td>
<td><span data-ttu-id="b7bb2-418">2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-418">2017</span></span></td>
<td><span data-ttu-id="b7bb2-419">Periood 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-419">Period 1</span></span></td>
<td><span data-ttu-id="b7bb2-420">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="b7bb2-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="b7bb2-421">Töölehe sisestused (töölehe sisestused üldkulu määra arvutamiseks)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7bb2-422">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b7bb2-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b7bb2-423">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-423">Cost object</span></span></th>
<th><span data-ttu-id="b7bb2-424">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-425">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-426">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-426">Proj 1</span></span></td>
<td><span data-ttu-id="b7bb2-427">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="b7bb2-428">3,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-429">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-430">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-430">Proj 2</span></span></td>
<td><span data-ttu-id="b7bb2-431">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="b7bb2-432">1,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b7bb2-433">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="b7bb2-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-434">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b7bb2-435">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b7bb2-435">Cost element</span></span></th>
<th><span data-ttu-id="b7bb2-436">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-436">Cost behavior</span></span></th>
<th><span data-ttu-id="b7bb2-437">Summa</span><span class="sxs-lookup"><span data-stu-id="b7bb2-437">Amount</span></span></th>
<th><span data-ttu-id="b7bb2-438">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b7bb2-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-439">CC0001</span></span></td>
<td><span data-ttu-id="b7bb2-440">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b7bb2-440">HR</span></span></td>
<td><span data-ttu-id="b7bb2-441">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-441">10001</span></span></td>
<td><span data-ttu-id="b7bb2-442">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-442">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-443">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-443">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-444">–30,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-444">-30.00</span></span></td>
<td><span data-ttu-id="b7bb2-445">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-446">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-446">Proj 1</span></span></td>
<td><span data-ttu-id="b7bb2-447">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="b7bb2-448">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-448">10001</span></span></td>
<td><span data-ttu-id="b7bb2-449">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-449">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-450">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-450">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-451">30,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-451">30.00</span></span></td>
<td><span data-ttu-id="b7bb2-452">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-453">CC001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-453">CC001</span></span></td>
<td><span data-ttu-id="b7bb2-454">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b7bb2-454">HR</span></span></td>
<td><span data-ttu-id="b7bb2-455">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-455">10001</span></span></td>
<td><span data-ttu-id="b7bb2-456">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-456">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-457">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-457">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-458">-10.00</span></span></td>
<td><span data-ttu-id="b7bb2-459">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-460">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-460">Proj 2</span></span></td>
<td><span data-ttu-id="b7bb2-461">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="b7bb2-462">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-462">10001</span></span></td>
<td><span data-ttu-id="b7bb2-463">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-463">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-464">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-464">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-465">10,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-465">10.00</span></span></td>
<td><span data-ttu-id="b7bb2-466">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7bb2-467">Üksikasjalikku teavet üldkulu määra poliitika kohta vt jaotistest Üldkulu määra poliitika ja Eraldamisalused.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="b7bb2-468">(Pange tähele, et see teema pole veel valmis, kuid see tuleb peagi.)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="b7bb2-469">4. etapp: kulueralduse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="b7bb2-470">Eraldamist kasutatakse kuluobjekti saldo eraldamiseks teistele kuluobjektidele, rakendades eraldamisalust.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="b7bb2-471">Finance and Operations toetab vastastikuse eraldamise meetodit.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="b7bb2-472">Vastastikuse eraldamise meetodi puhul tuvastatakse täiendavate kuluobjektide vahetatavad vastastikused teenused.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="b7bb2-473">Süsteem määrab automaatselt eraldamiste tegemise õige järjekorra.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="b7bb2-474">Kuluobjekti saldo eraldatakse üksiku eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="b7bb2-475">Toetatakse eraldamisi kuluobjektide dimensioonide ja nende vastavate liikmete seas.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="b7bb2-476">Eraldamisjärjekorda reguleerib kulujuhtseade.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="b7bb2-477">[![Vastastikune meetod](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="b7bb2-478">Kulueraldamise määratlemine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-478">Define the cost allocation</span></span>

<span data-ttu-id="b7bb2-479">Siin on lihtne näide, mis selgitab, kuidas jälgida kulu liikumist.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="b7bb2-480">Kuluobjekt CC001 inimressursid panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="b7bb2-481">Luuakse statistilise dimensiooni liige nimega Inimressursside teenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-482">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-482">Cost object</span></span></th>
<th><span data-ttu-id="b7bb2-483">Inimressursside teenused</span><span class="sxs-lookup"><span data-stu-id="b7bb2-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-484">CC002</span><span class="sxs-lookup"><span data-stu-id="b7bb2-484">CC002</span></span></td>
<td><span data-ttu-id="b7bb2-485">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b7bb2-485">Finance</span></span></td>
<td><span data-ttu-id="b7bb2-486">35</span><span class="sxs-lookup"><span data-stu-id="b7bb2-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-487">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-487">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-488">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-488">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-489">55</span><span class="sxs-lookup"><span data-stu-id="b7bb2-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-490">CC004</span><span class="sxs-lookup"><span data-stu-id="b7bb2-490">CC004</span></span></td>
<td><span data-ttu-id="b7bb2-491">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-491">Packaging</span></span></td>
<td><span data-ttu-id="b7bb2-492">10</span><span class="sxs-lookup"><span data-stu-id="b7bb2-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7bb2-493">Kuluobjekt CC002 rahandus panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="b7bb2-494">Luuakse statistilise dimensiooni liige nimega Rahandusteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-495">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-495">Cost object</span></span></th>
<th><span data-ttu-id="b7bb2-496">Rahandusteenused</span><span class="sxs-lookup"><span data-stu-id="b7bb2-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-497">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-497">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-498">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-498">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-499">65</span><span class="sxs-lookup"><span data-stu-id="b7bb2-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-500">CC004</span><span class="sxs-lookup"><span data-stu-id="b7bb2-500">CC004</span></span></td>
<td><span data-ttu-id="b7bb2-501">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-501">Packaging</span></span></td>
<td><span data-ttu-id="b7bb2-502">35</span><span class="sxs-lookup"><span data-stu-id="b7bb2-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7bb2-503">Kuluobjekt CC003 assembler panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="b7bb2-504">Luuakse statistilise dimensiooni liige nimega Assembleriteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-505">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-505">Cost object</span></span></th>
<th><span data-ttu-id="b7bb2-506">Assembleriteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-507">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-507">Prod 1</span></span></td>
<td><span data-ttu-id="b7bb2-508">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-508">Product 1</span></span></td>
<td><span data-ttu-id="b7bb2-509">60</span><span class="sxs-lookup"><span data-stu-id="b7bb2-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-510">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-510">Prod 2</span></span></td>
<td><span data-ttu-id="b7bb2-511">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-511">Product 2</span></span></td>
<td><span data-ttu-id="b7bb2-512">20</span><span class="sxs-lookup"><span data-stu-id="b7bb2-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7bb2-513">Kuluobjekt CC004 pakendamine panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="b7bb2-514">Luuakse statistilise dimensiooni liige nimega Pakendamisteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-515">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-515">Cost object</span></span></th>
<th><span data-ttu-id="b7bb2-516">Pakendamisteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-517">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-517">Prod 1</span></span></td>
<td><span data-ttu-id="b7bb2-518">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-518">Product 1</span></span></td>
<td><span data-ttu-id="b7bb2-519">80</span><span class="sxs-lookup"><span data-stu-id="b7bb2-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-520">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-520">Prod 2</span></span></td>
<td><span data-ttu-id="b7bb2-521">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-521">Product 2</span></span></td>
<td><span data-ttu-id="b7bb2-522">sept.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7bb2-523">**Märkus.** Finance and Operationsis saab statistilised mõõdud, nagu toote tarbitud tootmistunnid, tuletada lähteandmetest.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="b7bb2-524">Üksikasjalikku teavet statistiliste mõõtude pakkujate kohta vt jaotisest Statistilise mõõdu pakkuja mall.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="b7bb2-525">(Pange tähele, et see teema pole veel valmis, kuid see tuleb peagi.) Järgmises tabelis on näidatud tulemus, kui Inimressursside teenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud kulu ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="b7bb2-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-526">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-526">Cost object</span></span></th>
<th><span data-ttu-id="b7bb2-527">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-527">Magnitude</span></span></th>
<th><span data-ttu-id="b7bb2-528">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="b7bb2-528">Allocation factor</span></span></th>
<th><span data-ttu-id="b7bb2-529">Summa</span><span class="sxs-lookup"><span data-stu-id="b7bb2-529">Amount</span></span></th>
<th><span data-ttu-id="b7bb2-530">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-531">CC002</span><span class="sxs-lookup"><span data-stu-id="b7bb2-531">CC002</span></span></td>
<td><span data-ttu-id="b7bb2-532">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b7bb2-532">Finance</span></span></td>
<td><span data-ttu-id="b7bb2-533">35</span><span class="sxs-lookup"><span data-stu-id="b7bb2-533">35</span></span></td>
<td><span data-ttu-id="b7bb2-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b7bb2-535">175.00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-535">175.00</span></span></td>
<td><span data-ttu-id="b7bb2-536">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-537">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-537">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-538">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-538">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-539">55</span><span class="sxs-lookup"><span data-stu-id="b7bb2-539">55</span></span></td>
<td><span data-ttu-id="b7bb2-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b7bb2-541">275.00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-541">275.00</span></span></td>
<td><span data-ttu-id="b7bb2-542">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-543">CC004</span><span class="sxs-lookup"><span data-stu-id="b7bb2-543">CC004</span></span></td>
<td><span data-ttu-id="b7bb2-544">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-544">Packaging</span></span></td>
<td><span data-ttu-id="b7bb2-545">10</span><span class="sxs-lookup"><span data-stu-id="b7bb2-545">10</span></span></td>
<td><span data-ttu-id="b7bb2-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b7bb2-547">50,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-547">50.00</span></span></td>
<td><span data-ttu-id="b7bb2-548">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-549">CC002</span><span class="sxs-lookup"><span data-stu-id="b7bb2-549">CC002</span></span></td>
<td><span data-ttu-id="b7bb2-550">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b7bb2-550">Finance</span></span></td>
<td><span data-ttu-id="b7bb2-551">35</span><span class="sxs-lookup"><span data-stu-id="b7bb2-551">35</span></span></td>
<td><span data-ttu-id="b7bb2-552">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="b7bb2-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b7bb2-553">436.00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-553">436.00</span></span></td>
<td><span data-ttu-id="b7bb2-554">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-555">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-555">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-556">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-556">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-557">55</span><span class="sxs-lookup"><span data-stu-id="b7bb2-557">55</span></span></td>
<td><span data-ttu-id="b7bb2-558">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="b7bb2-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b7bb2-559">685.14</span><span class="sxs-lookup"><span data-stu-id="b7bb2-559">685.14</span></span></td>
<td><span data-ttu-id="b7bb2-560">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-561">CC004</span><span class="sxs-lookup"><span data-stu-id="b7bb2-561">CC004</span></span></td>
<td><span data-ttu-id="b7bb2-562">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-562">Packaging</span></span></td>
<td><span data-ttu-id="b7bb2-563">10</span><span class="sxs-lookup"><span data-stu-id="b7bb2-563">10</span></span></td>
<td><span data-ttu-id="b7bb2-564">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="b7bb2-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b7bb2-565">124.57</span><span class="sxs-lookup"><span data-stu-id="b7bb2-565">124.57</span></span></td>
<td><span data-ttu-id="b7bb2-566">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7bb2-567">Järgmises tabelis on näidatud tulemus, kui Rahandusteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="b7bb2-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-568">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-568">Cost object</span></span></th>
<th><span data-ttu-id="b7bb2-569">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-569">Magnitude</span></span></th>
<th><span data-ttu-id="b7bb2-570">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="b7bb2-570">Allocation factor</span></span></th>
<th><span data-ttu-id="b7bb2-571">Summa</span><span class="sxs-lookup"><span data-stu-id="b7bb2-571">Amount</span></span></th>
<th><span data-ttu-id="b7bb2-572">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-573">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-573">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-574">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-574">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-575">65</span><span class="sxs-lookup"><span data-stu-id="b7bb2-575">65</span></span></td>
<td><span data-ttu-id="b7bb2-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="b7bb2-577">438.75</span><span class="sxs-lookup"><span data-stu-id="b7bb2-577">438.75</span></span></td>
<td><span data-ttu-id="b7bb2-578">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-579">CC004</span><span class="sxs-lookup"><span data-stu-id="b7bb2-579">CC004</span></span></td>
<td><span data-ttu-id="b7bb2-580">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-580">Packaging</span></span></td>
<td><span data-ttu-id="b7bb2-581">35</span><span class="sxs-lookup"><span data-stu-id="b7bb2-581">35</span></span></td>
<td><span data-ttu-id="b7bb2-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="b7bb2-583">236.25</span><span class="sxs-lookup"><span data-stu-id="b7bb2-583">236.25</span></span></td>
<td><span data-ttu-id="b7bb2-584">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-585">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-585">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-586">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-586">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-587">65</span><span class="sxs-lookup"><span data-stu-id="b7bb2-587">65</span></span></td>
<td><span data-ttu-id="b7bb2-588">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="b7bb2-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="b7bb2-589">5,297.69</span></span></td>
<td><span data-ttu-id="b7bb2-590">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-591">CC004</span><span class="sxs-lookup"><span data-stu-id="b7bb2-591">CC004</span></span></td>
<td><span data-ttu-id="b7bb2-592">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-592">Packaging</span></span></td>
<td><span data-ttu-id="b7bb2-593">35</span><span class="sxs-lookup"><span data-stu-id="b7bb2-593">35</span></span></td>
<td><span data-ttu-id="b7bb2-594">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="b7bb2-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="b7bb2-595">2,852.60</span></span></td>
<td><span data-ttu-id="b7bb2-596">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7bb2-597">Järgmises tabelis on näidatud tulemus, kui Assembleriteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="b7bb2-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-598">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-598">Cost object</span></span></th>
<th><span data-ttu-id="b7bb2-599">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-599">Magnitude</span></span></th>
<th><span data-ttu-id="b7bb2-600">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="b7bb2-600">Allocation factor</span></span></th>
<th><span data-ttu-id="b7bb2-601">Summa</span><span class="sxs-lookup"><span data-stu-id="b7bb2-601">Amount</span></span></th>
<th><span data-ttu-id="b7bb2-602">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-603">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-603">Prod 1</span></span></td>
<td><span data-ttu-id="b7bb2-604">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-604">Product 1</span></span></td>
<td><span data-ttu-id="b7bb2-605">60</span><span class="sxs-lookup"><span data-stu-id="b7bb2-605">60</span></span></td>
<td><span data-ttu-id="b7bb2-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="b7bb2-607">535.31</span><span class="sxs-lookup"><span data-stu-id="b7bb2-607">535.31</span></span></td>
<td><span data-ttu-id="b7bb2-608">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-609">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-609">Prod 2</span></span></td>
<td><span data-ttu-id="b7bb2-610">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-610">Product 2</span></span></td>
<td><span data-ttu-id="b7bb2-611">20</span><span class="sxs-lookup"><span data-stu-id="b7bb2-611">20</span></span></td>
<td><span data-ttu-id="b7bb2-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="b7bb2-613">178.44</span><span class="sxs-lookup"><span data-stu-id="b7bb2-613">178.44</span></span></td>
<td><span data-ttu-id="b7bb2-614">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-615">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-615">Prod 1</span></span></td>
<td><span data-ttu-id="b7bb2-616">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-616">Product 1</span></span></td>
<td><span data-ttu-id="b7bb2-617">60</span><span class="sxs-lookup"><span data-stu-id="b7bb2-617">60</span></span></td>
<td><span data-ttu-id="b7bb2-618">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="b7bb2-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="b7bb2-619">4,487.12</span></span></td>
<td><span data-ttu-id="b7bb2-620">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-621">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-621">Prod 2</span></span></td>
<td><span data-ttu-id="b7bb2-622">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-622">Product 2</span></span></td>
<td><span data-ttu-id="b7bb2-623">20</span><span class="sxs-lookup"><span data-stu-id="b7bb2-623">20</span></span></td>
<td><span data-ttu-id="b7bb2-624">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="b7bb2-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="b7bb2-625">1,495.71</span></span></td>
<td><span data-ttu-id="b7bb2-626">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7bb2-627">Järgmises tabelis on näidatud tulemus, kui Pakendamisteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="b7bb2-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-628">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-628">Cost object</span></span></th>
<th><span data-ttu-id="b7bb2-629">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b7bb2-629">Magnitude</span></span></th>
<th><span data-ttu-id="b7bb2-630">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="b7bb2-630">Allocation factor</span></span></th>
<th><span data-ttu-id="b7bb2-631">Summa</span><span class="sxs-lookup"><span data-stu-id="b7bb2-631">Amount</span></span></th>
<th><span data-ttu-id="b7bb2-632">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-633">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-633">Prod 1</span></span></td>
<td><span data-ttu-id="b7bb2-634">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-634">Product 1</span></span></td>
<td><span data-ttu-id="b7bb2-635">80</span><span class="sxs-lookup"><span data-stu-id="b7bb2-635">80</span></span></td>
<td><span data-ttu-id="b7bb2-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="b7bb2-637">241.05</span><span class="sxs-lookup"><span data-stu-id="b7bb2-637">241.05</span></span></td>
<td><span data-ttu-id="b7bb2-638">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-639">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-639">Prod 2</span></span></td>
<td><span data-ttu-id="b7bb2-640">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-640">Product 2</span></span></td>
<td><span data-ttu-id="b7bb2-641">15</span><span class="sxs-lookup"><span data-stu-id="b7bb2-641">15</span></span></td>
<td><span data-ttu-id="b7bb2-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="b7bb2-643">45.20</span><span class="sxs-lookup"><span data-stu-id="b7bb2-643">45.20</span></span></td>
<td><span data-ttu-id="b7bb2-644">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-645">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-645">Prod 1</span></span></td>
<td><span data-ttu-id="b7bb2-646">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-646">Product 1</span></span></td>
<td><span data-ttu-id="b7bb2-647">80</span><span class="sxs-lookup"><span data-stu-id="b7bb2-647">80</span></span></td>
<td><span data-ttu-id="b7bb2-648">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="b7bb2-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="b7bb2-649">2,507.09</span></span></td>
<td><span data-ttu-id="b7bb2-650">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-651">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-651">Prod 2</span></span></td>
<td><span data-ttu-id="b7bb2-652">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-652">Product 2</span></span></td>
<td><span data-ttu-id="b7bb2-653">15</span><span class="sxs-lookup"><span data-stu-id="b7bb2-653">15</span></span></td>
<td><span data-ttu-id="b7bb2-654">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="b7bb2-655">470.08</span><span class="sxs-lookup"><span data-stu-id="b7bb2-655">470.08</span></span></td>
<td><span data-ttu-id="b7bb2-656">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b7bb2-657">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7bb2-658">Tööleht</span><span class="sxs-lookup"><span data-stu-id="b7bb2-658">Journal</span></span></th>
<th><span data-ttu-id="b7bb2-659">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="b7bb2-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b7bb2-660">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="b7bb2-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b7bb2-661">Versioon</span><span class="sxs-lookup"><span data-stu-id="b7bb2-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-662">00004</span><span class="sxs-lookup"><span data-stu-id="b7bb2-662">00004</span></span></td>
<td><span data-ttu-id="b7bb2-663">Kulueralduse tööleht</span><span class="sxs-lookup"><span data-stu-id="b7bb2-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="b7bb2-664">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="b7bb2-664">Fiscal</span></span></td>
<td><span data-ttu-id="b7bb2-665">2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-665">2017</span></span></td>
<td><span data-ttu-id="b7bb2-666">Periood 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-666">Period 1</span></span></td>
<td><span data-ttu-id="b7bb2-667">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="b7bb2-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="b7bb2-668">Töölehe read</span><span class="sxs-lookup"><span data-stu-id="b7bb2-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7bb2-669">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b7bb2-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b7bb2-670">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b7bb2-671">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b7bb2-671">Cost element</span></span></th>
<th><span data-ttu-id="b7bb2-672">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-672">Cost behavior</span></span></th>
<th><span data-ttu-id="b7bb2-673">Summa</span><span class="sxs-lookup"><span data-stu-id="b7bb2-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-674">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-675">CC001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-675">CC001</span></span></td>
<td><span data-ttu-id="b7bb2-676">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b7bb2-676">HR</span></span></td>
<td><span data-ttu-id="b7bb2-677">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-677">10001</span></span></td>
<td><span data-ttu-id="b7bb2-678">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-678">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-679">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-679">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-680">500,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-681">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-682">CC001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-682">CC001</span></span></td>
<td><span data-ttu-id="b7bb2-683">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b7bb2-683">HR</span></span></td>
<td><span data-ttu-id="b7bb2-684">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-684">10001</span></span></td>
<td><span data-ttu-id="b7bb2-685">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-685">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-686">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-686">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="b7bb2-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-688">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-689">CC002</span><span class="sxs-lookup"><span data-stu-id="b7bb2-689">CC002</span></span></td>
<td><span data-ttu-id="b7bb2-690">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b7bb2-690">Finance</span></span></td>
<td><span data-ttu-id="b7bb2-691">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-691">10001</span></span></td>
<td><span data-ttu-id="b7bb2-692">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-692">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-693">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-693">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-694">675.00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-695">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-696">CC002</span><span class="sxs-lookup"><span data-stu-id="b7bb2-696">CC002</span></span></td>
<td><span data-ttu-id="b7bb2-697">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b7bb2-697">Finance</span></span></td>
<td><span data-ttu-id="b7bb2-698">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-698">10001</span></span></td>
<td><span data-ttu-id="b7bb2-699">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-699">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-700">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-700">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="b7bb2-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-702">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-703">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-703">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-704">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-704">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-705">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-705">10001</span></span></td>
<td><span data-ttu-id="b7bb2-706">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-706">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-707">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-707">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-708">713.75</span><span class="sxs-lookup"><span data-stu-id="b7bb2-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-709">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-710">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-710">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-711">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-711">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-712">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-712">10001</span></span></td>
<td><span data-ttu-id="b7bb2-713">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-713">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-714">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-714">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="b7bb2-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-716">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-717">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-717">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-718">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-718">Packaging</span></span></td>
<td><span data-ttu-id="b7bb2-719">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-719">10001</span></span></td>
<td><span data-ttu-id="b7bb2-720">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-720">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-721">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-721">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-722">286.25</span><span class="sxs-lookup"><span data-stu-id="b7bb2-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-723">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-724">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-724">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-725">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-725">Packaging</span></span></td>
<td><span data-ttu-id="b7bb2-726">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-726">10001</span></span></td>
<td><span data-ttu-id="b7bb2-727">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-727">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-728">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-728">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="b7bb2-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-730">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-731">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-731">Prod 1</span></span></td>
<td><span data-ttu-id="b7bb2-732">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-732">Product 1</span></span></td>
<td><span data-ttu-id="b7bb2-733">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-733">10001</span></span></td>
<td><span data-ttu-id="b7bb2-734">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-734">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-735">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-735">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-736">776.36</span><span class="sxs-lookup"><span data-stu-id="b7bb2-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-737">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-738">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-738">Prod 1</span></span></td>
<td><span data-ttu-id="b7bb2-739">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-739">Product 1</span></span></td>
<td><span data-ttu-id="b7bb2-740">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-740">10001</span></span></td>
<td><span data-ttu-id="b7bb2-741">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-741">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-742">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-742">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="b7bb2-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-744">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-745">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-745">Prod 2</span></span></td>
<td><span data-ttu-id="b7bb2-746">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-746">Product 1</span></span></td>
<td><span data-ttu-id="b7bb2-747">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-747">10001</span></span></td>
<td><span data-ttu-id="b7bb2-748">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-748">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-749">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-749">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-750">223.64</span><span class="sxs-lookup"><span data-stu-id="b7bb2-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-751">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7bb2-752">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-752">Prod 2</span></span></td>
<td><span data-ttu-id="b7bb2-753">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-753">Product 1</span></span></td>
<td><span data-ttu-id="b7bb2-754">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-754">10001</span></span></td>
<td><span data-ttu-id="b7bb2-755">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-755">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-756">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-756">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="b7bb2-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b7bb2-758">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="b7bb2-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7bb2-759">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b7bb2-760">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b7bb2-760">Cost element</span></span></th>
<th><span data-ttu-id="b7bb2-761">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-761">Cost behavior</span></span></th>
<th><span data-ttu-id="b7bb2-762">Summa</span><span class="sxs-lookup"><span data-stu-id="b7bb2-762">Amount</span></span></th>
<th><span data-ttu-id="b7bb2-763">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b7bb2-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7bb2-764">CC001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-764">CC001</span></span></td>
<td><span data-ttu-id="b7bb2-765">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b7bb2-765">HR</span></span></td>
<td><span data-ttu-id="b7bb2-766">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-766">10001</span></span></td>
<td><span data-ttu-id="b7bb2-767">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-767">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-768">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-768">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-769">‑500,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-769">-500.00</span></span></td>
<td><span data-ttu-id="b7bb2-770">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-771">CC002</span><span class="sxs-lookup"><span data-stu-id="b7bb2-771">CC002</span></span></td>
<td><span data-ttu-id="b7bb2-772">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b7bb2-772">Finance</span></span></td>
<td><span data-ttu-id="b7bb2-773">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-773">10001</span></span></td>
<td><span data-ttu-id="b7bb2-774">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-774">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-775">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-775">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-776">175.00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-776">175.00</span></span></td>
<td><span data-ttu-id="b7bb2-777">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-778">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-778">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-779">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-779">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-780">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-780">10001</span></span></td>
<td><span data-ttu-id="b7bb2-781">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-781">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-782">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-782">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-783">275.00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-783">275.00</span></span></td>
<td><span data-ttu-id="b7bb2-784">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-785">CC004</span><span class="sxs-lookup"><span data-stu-id="b7bb2-785">CC004</span></span></td>
<td><span data-ttu-id="b7bb2-786">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-786">Packaging</span></span></td>
<td><span data-ttu-id="b7bb2-787">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-787">10001</span></span></td>
<td><span data-ttu-id="b7bb2-788">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-788">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-789">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-789">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-790">50,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-790">50,00</span></span></td>
<td><span data-ttu-id="b7bb2-791">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-792">CC001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-792">CC001</span></span></td>
<td><span data-ttu-id="b7bb2-793">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b7bb2-793">HR</span></span></td>
<td><span data-ttu-id="b7bb2-794">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-794">10001</span></span></td>
<td><span data-ttu-id="b7bb2-795">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-795">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-796">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-796">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-797">–1245,71</span><span class="sxs-lookup"><span data-stu-id="b7bb2-797">-1,245.71</span></span></td>
<td><span data-ttu-id="b7bb2-798">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-799">CC002</span><span class="sxs-lookup"><span data-stu-id="b7bb2-799">CC002</span></span></td>
<td><span data-ttu-id="b7bb2-800">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b7bb2-800">Finance</span></span></td>
<td><span data-ttu-id="b7bb2-801">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-801">10001</span></span></td>
<td><span data-ttu-id="b7bb2-802">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-802">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-803">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-803">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-804">436.00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-804">436.00</span></span></td>
<td><span data-ttu-id="b7bb2-805">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-806">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-806">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-807">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-807">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-808">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-808">10001</span></span></td>
<td><span data-ttu-id="b7bb2-809">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-809">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-810">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-810">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-811">685.14</span><span class="sxs-lookup"><span data-stu-id="b7bb2-811">685.14</span></span></td>
<td><span data-ttu-id="b7bb2-812">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-813">CC004</span><span class="sxs-lookup"><span data-stu-id="b7bb2-813">CC004</span></span></td>
<td><span data-ttu-id="b7bb2-814">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-814">Packaging</span></span></td>
<td><span data-ttu-id="b7bb2-815">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-815">10001</span></span></td>
<td><span data-ttu-id="b7bb2-816">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-816">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-817">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-817">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-818">124.57</span><span class="sxs-lookup"><span data-stu-id="b7bb2-818">124.57</span></span></td>
<td><span data-ttu-id="b7bb2-819">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-820">CC002</span><span class="sxs-lookup"><span data-stu-id="b7bb2-820">CC002</span></span></td>
<td><span data-ttu-id="b7bb2-821">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b7bb2-821">Finance</span></span></td>
<td><span data-ttu-id="b7bb2-822">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-822">10001</span></span></td>
<td><span data-ttu-id="b7bb2-823">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-823">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-824">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-824">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-825">–675,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-825">-675.00</span></span></td>
<td><span data-ttu-id="b7bb2-826">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-827">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-827">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-828">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-828">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-829">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-829">10001</span></span></td>
<td><span data-ttu-id="b7bb2-830">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-830">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-831">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-831">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-832">438.75</span><span class="sxs-lookup"><span data-stu-id="b7bb2-832">438.75</span></span></td>
<td><span data-ttu-id="b7bb2-833">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-834">CC004</span><span class="sxs-lookup"><span data-stu-id="b7bb2-834">CC004</span></span></td>
<td><span data-ttu-id="b7bb2-835">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-835">Packaging</span></span></td>
<td><span data-ttu-id="b7bb2-836">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-836">10001</span></span></td>
<td><span data-ttu-id="b7bb2-837">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-837">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-838">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-838">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-839">236.25</span><span class="sxs-lookup"><span data-stu-id="b7bb2-839">236.25</span></span></td>
<td><span data-ttu-id="b7bb2-840">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-841">CC002</span><span class="sxs-lookup"><span data-stu-id="b7bb2-841">CC002</span></span></td>
<td><span data-ttu-id="b7bb2-842">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b7bb2-842">Finance</span></span></td>
<td><span data-ttu-id="b7bb2-843">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-843">10001</span></span></td>
<td><span data-ttu-id="b7bb2-844">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-844">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-845">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-845">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-846">–8150,29</span><span class="sxs-lookup"><span data-stu-id="b7bb2-846">-8,150.29</span></span></td>
<td><span data-ttu-id="b7bb2-847">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-848">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-848">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-849">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-849">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-850">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-850">10001</span></span></td>
<td><span data-ttu-id="b7bb2-851">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-851">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-852">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-852">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="b7bb2-853">5,297.69</span></span></td>
<td><span data-ttu-id="b7bb2-854">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-855">CC004</span><span class="sxs-lookup"><span data-stu-id="b7bb2-855">CC004</span></span></td>
<td><span data-ttu-id="b7bb2-856">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b7bb2-856">Packaging</span></span></td>
<td><span data-ttu-id="b7bb2-857">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-857">10001</span></span></td>
<td><span data-ttu-id="b7bb2-858">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-858">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-859">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-859">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="b7bb2-860">2,852.60</span></span></td>
<td><span data-ttu-id="b7bb2-861">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-862">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-862">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-863">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-863">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-864">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-864">10001</span></span></td>
<td><span data-ttu-id="b7bb2-865">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-865">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-866">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-866">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-867">–713,75</span><span class="sxs-lookup"><span data-stu-id="b7bb2-867">-713.75</span></span></td>
<td><span data-ttu-id="b7bb2-868">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-869">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-869">Prod 1</span></span></td>
<td><span data-ttu-id="b7bb2-870">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-870">Product 1</span></span></td>
<td><span data-ttu-id="b7bb2-871">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-871">10001</span></span></td>
<td><span data-ttu-id="b7bb2-872">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-872">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-873">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-873">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-874">535.31</span><span class="sxs-lookup"><span data-stu-id="b7bb2-874">535.31</span></span></td>
<td><span data-ttu-id="b7bb2-875">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-876">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-876">Prod 2</span></span></td>
<td><span data-ttu-id="b7bb2-877">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-877">Product 2</span></span></td>
<td><span data-ttu-id="b7bb2-878">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-878">10001</span></span></td>
<td><span data-ttu-id="b7bb2-879">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-879">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-880">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-880">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-881">178.44</span><span class="sxs-lookup"><span data-stu-id="b7bb2-881">178.44</span></span></td>
<td><span data-ttu-id="b7bb2-882">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-883">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-883">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-884">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-884">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-885">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-885">10001</span></span></td>
<td><span data-ttu-id="b7bb2-886">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-886">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-887">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-887">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-888">–5982,83</span><span class="sxs-lookup"><span data-stu-id="b7bb2-888">-5,982.83</span></span></td>
<td><span data-ttu-id="b7bb2-889">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-890">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-890">Prod 1</span></span></td>
<td><span data-ttu-id="b7bb2-891">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-891">Product 1</span></span></td>
<td><span data-ttu-id="b7bb2-892">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-892">10001</span></span></td>
<td><span data-ttu-id="b7bb2-893">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-893">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-894">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-894">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="b7bb2-895">4,487.12</span></span></td>
<td><span data-ttu-id="b7bb2-896">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-897">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-897">Prod 2</span></span></td>
<td><span data-ttu-id="b7bb2-898">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-898">Product 2</span></span></td>
<td><span data-ttu-id="b7bb2-899">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-899">10001</span></span></td>
<td><span data-ttu-id="b7bb2-900">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-900">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-901">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-901">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="b7bb2-902">1,495.71</span></span></td>
<td><span data-ttu-id="b7bb2-903">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-904">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-904">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-905">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-905">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-906">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-906">10001</span></span></td>
<td><span data-ttu-id="b7bb2-907">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-907">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-908">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-908">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-909">–286,25</span><span class="sxs-lookup"><span data-stu-id="b7bb2-909">-286.25</span></span></td>
<td><span data-ttu-id="b7bb2-910">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-911">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-911">Prod 1</span></span></td>
<td><span data-ttu-id="b7bb2-912">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-912">Product 1</span></span></td>
<td><span data-ttu-id="b7bb2-913">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-913">10001</span></span></td>
<td><span data-ttu-id="b7bb2-914">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-914">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-915">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-915">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-916">241.05</span><span class="sxs-lookup"><span data-stu-id="b7bb2-916">241.05</span></span></td>
<td><span data-ttu-id="b7bb2-917">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-918">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-918">Prod 2</span></span></td>
<td><span data-ttu-id="b7bb2-919">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-919">Product 2</span></span></td>
<td><span data-ttu-id="b7bb2-920">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-920">10001</span></span></td>
<td><span data-ttu-id="b7bb2-921">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-921">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-922">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-922">Fixed cost</span></span></td>
<td><span data-ttu-id="b7bb2-923">45.20</span><span class="sxs-lookup"><span data-stu-id="b7bb2-923">45.20</span></span></td>
<td><span data-ttu-id="b7bb2-924">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-925">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-925">CC003</span></span></td>
<td><span data-ttu-id="b7bb2-926">Assembler</span><span class="sxs-lookup"><span data-stu-id="b7bb2-926">Assembly</span></span></td>
<td><span data-ttu-id="b7bb2-927">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-927">10001</span></span></td>
<td><span data-ttu-id="b7bb2-928">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-928">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-929">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-929">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-930">–2977,17</span><span class="sxs-lookup"><span data-stu-id="b7bb2-930">-2,977.17</span></span></td>
<td><span data-ttu-id="b7bb2-931">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-932">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-932">Prod 1</span></span></td>
<td><span data-ttu-id="b7bb2-933">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-933">Product 1</span></span></td>
<td><span data-ttu-id="b7bb2-934">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-934">10001</span></span></td>
<td><span data-ttu-id="b7bb2-935">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-935">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-936">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-936">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="b7bb2-937">2,507.09</span></span></td>
<td><span data-ttu-id="b7bb2-938">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7bb2-939">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-939">Prod 2</span></span></td>
<td><span data-ttu-id="b7bb2-940">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-940">Product 2</span></span></td>
<td><span data-ttu-id="b7bb2-941">10001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-941">10001</span></span></td>
<td><span data-ttu-id="b7bb2-942">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b7bb2-942">Electricity</span></span></td>
<td><span data-ttu-id="b7bb2-943">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-943">Variable cost</span></span></td>
<td><span data-ttu-id="b7bb2-944">470.08</span><span class="sxs-lookup"><span data-stu-id="b7bb2-944">470.08</span></span></td>
<td><span data-ttu-id="b7bb2-945">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b7bb2-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="b7bb2-946">Lõppsõna</span><span class="sxs-lookup"><span data-stu-id="b7bb2-946">Conclusion</span></span>
<span data-ttu-id="b7bb2-947">Finantsaruandluses sisestatakse elektrikulu 10 000,00 fiktiivse kulukeskuse ID-le.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="b7bb2-948">Nii teavad kuluarvestajad, et see kulu tuleb eraldada.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="b7bb2-949">Kuluarvestuses liigub kulu rakendatud poliitikate ja reeglite põhjal läbi organisatsiooniüksuste ja -tasemete.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="b7bb2-950">Iga kulu on seostatud eraldamisalusega, mis pakub kulude eraldamiseks parimat hinnangut.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="b7bb2-951">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b7bb2-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="b7bb2-952">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b7bb2-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="b7bb2-953">Kokku</span><span class="sxs-lookup"><span data-stu-id="b7bb2-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b7bb2-954">CC099</span><span class="sxs-lookup"><span data-stu-id="b7bb2-954">CC099</span></span></th>
<th><span data-ttu-id="b7bb2-955">CC001</span><span class="sxs-lookup"><span data-stu-id="b7bb2-955">CC001</span></span></th>
<th><span data-ttu-id="b7bb2-956">CC002</span><span class="sxs-lookup"><span data-stu-id="b7bb2-956">CC002</span></span></th>
<th><span data-ttu-id="b7bb2-957">CC003</span><span class="sxs-lookup"><span data-stu-id="b7bb2-957">CC003</span></span></th>
<th><span data-ttu-id="b7bb2-958">CC004</span><span class="sxs-lookup"><span data-stu-id="b7bb2-958">CC004</span></span></th>
<th><span data-ttu-id="b7bb2-959">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-959">Proj 1</span></span></th>
<th><span data-ttu-id="b7bb2-960">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-960">Proj 2</span></span></th>
<th><span data-ttu-id="b7bb2-961">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b7bb2-961">Prod 1</span></span></th>
<th><span data-ttu-id="b7bb2-962">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b7bb2-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="b7bb2-963">10001 Elekter</span><span class="sxs-lookup"><span data-stu-id="b7bb2-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="b7bb2-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-965"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="b7bb2-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-966"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="b7bb2-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-967"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="b7bb2-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-968"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="b7bb2-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-969"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="b7bb2-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-970"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="b7bb2-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-971"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="b7bb2-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-972"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="b7bb2-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="b7bb2-973">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="b7bb2-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-974">0,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="b7bb2-975">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-976">0,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-977">0,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-978">0,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-979">0,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-980">0,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-981">776.36</span><span class="sxs-lookup"><span data-stu-id="b7bb2-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-982">223.64</span><span class="sxs-lookup"><span data-stu-id="b7bb2-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-983"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="b7bb2-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="b7bb2-984">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b7bb2-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-985">000</span><span class="sxs-lookup"><span data-stu-id="b7bb2-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-986">0,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-987">0,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-988">0,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-989">0,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-990">30,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-991">10,00</span><span class="sxs-lookup"><span data-stu-id="b7bb2-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="b7bb2-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="b7bb2-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7bb2-994"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="b7bb2-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b7bb2-995">Selles teemas selgitatakse, kuidas esmane kuluelement, 10001 Eleter, liigub läbi kuluobjektide.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="b7bb2-996">Seega eraldatakse see üldkulu organisatsiooni madalaimale tasemele.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="b7bb2-997">Teisisõnu kannavad kulu madalaimal tasemel olevad kuluobjektid.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="b7bb2-998">Kui soovite saada kuluobjektide vahelisest kuluvoost visuaalset ülevaadet, saate kuluvoo visualiseerimiseks kasutada kulude kokkuvõtte poliitika reegleid.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="b7bb2-999">Täpsemat teavet vaadake jaotisest Kulude kokkuvõtte poliitika.</span><span class="sxs-lookup"><span data-stu-id="b7bb2-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="b7bb2-1000">(Pange tähele, et see teema pole veel valmis, kuid see tuleb peagi.)</span><span class="sxs-lookup"><span data-stu-id="b7bb2-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




