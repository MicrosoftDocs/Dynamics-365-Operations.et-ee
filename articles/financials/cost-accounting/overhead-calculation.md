---
title: "Üldkulude arvutus"
description: "Selles teemas kirjeldatakse tüüpilisi üldkulude arvutamise ja eraldamise protsesse."
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 12ae99c15bafcd9cc08b30903fe3f251f446b17d
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.contentlocale: et-ee
ms.lasthandoff: 10/05/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="6bb5a-103">Üldkulude arvutus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6bb5a-104">Selles teemas kirjeldatakse tüüpilisi üldkulude arvutamise ja eraldamise protsesse.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="6bb5a-105">Mõiste määratlus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-105">Term definition</span></span>
---------------

<span data-ttu-id="6bb5a-106">Üldkulud on kulud, mis kaasnevad ettevõtte käitamisega, kuid mida ei saa seostada otseselt ühegi kindla äritegevuse, toote ega teenusega.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="6bb5a-107">Üldkulud pakuvad kriitilist tuge kasumit andavate tegevuste loomisele.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="6bb5a-108">Siin on mõned näited üldkuludest.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="6bb5a-109">Üür</span><span class="sxs-lookup"><span data-stu-id="6bb5a-109">Rent</span></span>
-   <span data-ttu-id="6bb5a-110">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-110">Electricity</span></span>
-   <span data-ttu-id="6bb5a-111">Haldustasud</span><span class="sxs-lookup"><span data-stu-id="6bb5a-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="6bb5a-112">Üldkulude arvutuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="6bb5a-112">Overhead calculation overview</span></span>
<span data-ttu-id="6bb5a-113">Üldkulude arvutus käitab kuluarvutuse poliitikaid õiges järjekorras.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="6bb5a-114">Saate käivitada üldkulude arvutuse sama rahandusperioodi kohta mitu korda, kui kuluarvestuse poliitikaid on muudetud või tuvastatud teatud tõrked.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="6bb5a-115">Iga üldkulude arvutamise käitamine talletatakse ja see saab kordumatu versiooni-ID, mis võimaldab teil arvutuste erinevaid versioone võrrelda.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="6bb5a-116">Ülekulude arvutusega loodud kulukirjed saavad aruandluskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="6bb5a-117">See aruandluskuupäev vastab arvutuses kasutatud rahandusperioodi lõppkuupäevale.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="6bb5a-118">Kordumatu versiooni-ID koosneb järgmistest elementidest.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="6bb5a-119">Versiooni tüüp</span><span class="sxs-lookup"><span data-stu-id="6bb5a-119">Version type</span></span>
-   <span data-ttu-id="6bb5a-120">Kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="6bb5a-120">Date and time</span></span>
-   <span data-ttu-id="6bb5a-121">Kuluarvestuse pearaamat</span><span class="sxs-lookup"><span data-stu-id="6bb5a-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="6bb5a-122">Finantsaasta</span><span class="sxs-lookup"><span data-stu-id="6bb5a-122">Fiscal year</span></span>
-   <span data-ttu-id="6bb5a-123">Rahandusperiood</span><span class="sxs-lookup"><span data-stu-id="6bb5a-123">Fiscal period</span></span>

<span data-ttu-id="6bb5a-124">Üldkulude arvutus käivitatakse versioonist sõltumatult.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="6bb5a-125">Seetõttu saate arvutada eelarveversiooni enne tegelikku versiooni.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="6bb5a-126">Üldkulude arvutus koosneb neljast etapist, nagu näha alltoodud joonisel.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="6bb5a-127">Igas etapis luuakse töölehe päis, millel on töölehe kanded.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="6bb5a-128">See töölehe päis säiiltab sisendandmeid iga arvutusetapi kohta.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="6bb5a-129">Igale töölehe reale rakendatakse poliitikad ja reeglid ning väljundina luuakse kulukirjed.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="6bb5a-130">Seega on teil alati olemas põhjalik ülevaade.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="6bb5a-131">[![Üldkulude arvutus](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="6bb5a-132">Elektri üldkulude arvutamine ja eraldamine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="6bb5a-133">Finantsaruandluses on mõned kulud, näiteks elekter, registreeritud põhisummana.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="6bb5a-134">Seetõttu ei pakuta kuluarvestuseks üksikasjalikku juhtimisülevaadet.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="6bb5a-135">Kuluarvestuses peavad kulud liikuma läbi organisatsiooniüksuste, et pakkuda korrektset juhtimisülevaadet kõigi organisatsiooniüksuste ja -tasemete kohta.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="6bb5a-136">See voog peab põhinema tarbimise või õiglase hindamise täpsel kirjendamisel.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="6bb5a-137">Pearaamatus, saab elektrikulu sisestada nii, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6bb5a-138">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="6bb5a-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6bb5a-139">Kulukeskus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="6bb5a-140">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="6bb5a-140">Main account</span></span></th>
<th><span data-ttu-id="6bb5a-141">Summa arvestusvaluutas</span><span class="sxs-lookup"><span data-stu-id="6bb5a-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-142">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-143">CC099</span><span class="sxs-lookup"><span data-stu-id="6bb5a-143">CC099</span></span></td>
<td><span data-ttu-id="6bb5a-144">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-144">Default cost center</span></span></td>
<td><span data-ttu-id="6bb5a-145">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-145">10001</span></span></td>
<td><span data-ttu-id="6bb5a-146">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-146">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="6bb5a-148">1. etapp: kulukäitumise arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="6bb5a-149">Vaikimisi saavad lähteandmetest imporditud kulukirjed kuluarvestuses kulukäitumise klassifikatsiooniks **Klassifitseerimata**.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="6bb5a-150">Kulukäitumise poliitikareegleid rakendades saate kulukirjed ümber klassifitseerida kui **Fikseeritud kulu** või **Muutuvkulu**.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="6bb5a-151">Kulukäitumise reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-151">Define the cost behavior rule</span></span>

<span data-ttu-id="6bb5a-152">Mõnikord on osa kulust fikseeritud tasu ja järelejäänud kulu põhineb tarbimisel.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="6bb5a-153">Elektriarved vastavad sageli sellele määratlusele.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="6bb5a-154">Pärast kindla fikseeritud tasu maksmist maksate tarbimise eest kilovatt-tunni (Kwh) kohta.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="6bb5a-155">Näiteks kui fikseeritud kulu tasu on 1000,00 eurot, määratletakse kulukäitumise reegel järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="6bb5a-156">Fikseeritud summa: 1000,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="6bb5a-157">0 &lt;= 1000,00 = fikseeritud</span><span class="sxs-lookup"><span data-stu-id="6bb5a-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="6bb5a-158">1000,01 &lt; N = muutuja</span><span class="sxs-lookup"><span data-stu-id="6bb5a-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="6bb5a-159">Tööleht</span><span class="sxs-lookup"><span data-stu-id="6bb5a-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6bb5a-160">Tööleht</span><span class="sxs-lookup"><span data-stu-id="6bb5a-160">Journal</span></span></th>
<th><span data-ttu-id="6bb5a-161">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="6bb5a-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6bb5a-162">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="6bb5a-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6bb5a-163">Versioon</span><span class="sxs-lookup"><span data-stu-id="6bb5a-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-164">00001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-164">00001</span></span></td>
<td><span data-ttu-id="6bb5a-165">Kulukäitumise arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="6bb5a-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="6bb5a-166">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="6bb5a-166">Fiscal</span></span></td>
<td><span data-ttu-id="6bb5a-167">2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-167">2017</span></span></td>
<td><span data-ttu-id="6bb5a-168">Periood 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-168">Period 1</span></span></td>
<td><span data-ttu-id="6bb5a-169">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="6bb5a-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6bb5a-170">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6bb5a-171">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="6bb5a-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6bb5a-172">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6bb5a-173">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="6bb5a-173">Cost element</span></span></th>
<th><span data-ttu-id="6bb5a-174">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-174">Cost behavior</span></span></th>
<th><span data-ttu-id="6bb5a-175">Summa</span><span class="sxs-lookup"><span data-stu-id="6bb5a-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-176">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-177">CC099</span><span class="sxs-lookup"><span data-stu-id="6bb5a-177">CC099</span></span></td>
<td><span data-ttu-id="6bb5a-178">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-178">Default cost center</span></span></td>
<td><span data-ttu-id="6bb5a-179">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-179">10001</span></span></td>
<td><span data-ttu-id="6bb5a-180">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-180">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-181">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="6bb5a-181">Unclassified</span></span></td>
<td><span data-ttu-id="6bb5a-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6bb5a-183">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="6bb5a-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-184">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6bb5a-185">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="6bb5a-185">Cost element</span></span></th>
<th><span data-ttu-id="6bb5a-186">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-186">Cost behavior</span></span></th>
<th><span data-ttu-id="6bb5a-187">Summa</span><span class="sxs-lookup"><span data-stu-id="6bb5a-187">Amount</span></span></th>
<th><span data-ttu-id="6bb5a-188">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="6bb5a-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-189">CC099</span><span class="sxs-lookup"><span data-stu-id="6bb5a-189">CC099</span></span></td>
<td><span data-ttu-id="6bb5a-190">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-190">Default cost center</span></span></td>
<td><span data-ttu-id="6bb5a-191">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-191">10001</span></span></td>
<td><span data-ttu-id="6bb5a-192">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-192">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-193">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="6bb5a-193">Unclassified</span></span></td>
<td><span data-ttu-id="6bb5a-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-194">10,000.00</span></span></td>
<td><span data-ttu-id="6bb5a-195">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-196">CC099</span><span class="sxs-lookup"><span data-stu-id="6bb5a-196">CC099</span></span></td>
<td><span data-ttu-id="6bb5a-197">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-197">Default cost center</span></span></td>
<td><span data-ttu-id="6bb5a-198">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-198">10001</span></span></td>
<td><span data-ttu-id="6bb5a-199">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-199">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-200">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="6bb5a-200">Unclassified</span></span></td>
<td><span data-ttu-id="6bb5a-201">–10 000,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-201">-10,000.00</span></span></td>
<td><span data-ttu-id="6bb5a-202">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-203">CC099</span><span class="sxs-lookup"><span data-stu-id="6bb5a-203">CC099</span></span></td>
<td><span data-ttu-id="6bb5a-204">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-204">Default cost center</span></span></td>
<td><span data-ttu-id="6bb5a-205">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-205">10001</span></span></td>
<td><span data-ttu-id="6bb5a-206">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-206">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-207">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-207">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-208">1,000.00</span></span></td>
<td><span data-ttu-id="6bb5a-209">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-210">CC099</span><span class="sxs-lookup"><span data-stu-id="6bb5a-210">CC099</span></span></td>
<td><span data-ttu-id="6bb5a-211">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-211">Default cost center</span></span></td>
<td><span data-ttu-id="6bb5a-212">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-212">10001</span></span></td>
<td><span data-ttu-id="6bb5a-213">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-213">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-214">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-214">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-215">9,000.00</span></span></td>
<td><span data-ttu-id="6bb5a-216">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6bb5a-217">Lisateavet vt teemast [Kulukäitumise poliitika loomine ja määramine kulujuhtimisüksusele (tegevuse juhis)](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="6bb5a-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="6bb5a-218">2. etapp: kulujaotuse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="6bb5a-219">Kulujaotust kasutatakse kulu ümberjaotamiseks ühelt kuluobjektilt ühele või mitmele teisele kuluobjektile, rakendades asjakohast eraldusalust.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="6bb5a-220">Kulujaotus ja kulueraldus erinevad selle poolest, et kulujaotus toimub alati algse kulu esmase kuluelemendi tasemel.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="6bb5a-221">Kulujaotuse reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-221">Define the cost distribution rule</span></span>

<span data-ttu-id="6bb5a-222">Finantsaruandluses registreeritakse elektrikulud sageli põhisummana.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="6bb5a-223">Kuluarvestuseses ei ole see lähenemine piisavalt üksikasjalik.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="6bb5a-224">Muutuvkulu tuleb jaotada üksikutele kuluobjektidele õigluse alusel.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="6bb5a-225">Kõige loogilisem eraldamisalus on elektritarbimine (kWh).</span><span class="sxs-lookup"><span data-stu-id="6bb5a-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="6bb5a-226">Luuakse statistilise dimensiooni liige nimega Elekter ja elektritarbimine on kirjendatakse.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="6bb5a-227">Vaikimisi muutuvad kõik statistilise dimensiooni liikmed eraldamisalusena kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-228">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-228">Cost object</span></span></th>
<th><span data-ttu-id="6bb5a-229">kWh</span><span class="sxs-lookup"><span data-stu-id="6bb5a-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-230">CC001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-230">CC001</span></span></td>
<td><span data-ttu-id="6bb5a-231">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="6bb5a-231">HR</span></span></td>
<td><span data-ttu-id="6bb5a-232">1000</span><span class="sxs-lookup"><span data-stu-id="6bb5a-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-233">CC002</span><span class="sxs-lookup"><span data-stu-id="6bb5a-233">CC002</span></span></td>
<td><span data-ttu-id="6bb5a-234">Finantsid</span><span class="sxs-lookup"><span data-stu-id="6bb5a-234">Finance</span></span></td>
<td><span data-ttu-id="6bb5a-235">6,000</span><span class="sxs-lookup"><span data-stu-id="6bb5a-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-236">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-236">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-237">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-237">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-238">0</span><span class="sxs-lookup"><span data-stu-id="6bb5a-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6bb5a-239">Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-240">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-240">Cost object</span></span></th>
<th><span data-ttu-id="6bb5a-241">Väärtus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-241">Magnitude</span></span></th>
<th><span data-ttu-id="6bb5a-242">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="6bb5a-242">Allocation factor</span></span></th>
<th><span data-ttu-id="6bb5a-243">Summa</span><span class="sxs-lookup"><span data-stu-id="6bb5a-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-244">CC001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-244">CC001</span></span></td>
<td><span data-ttu-id="6bb5a-245">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="6bb5a-245">HR</span></span></td>
<td><span data-ttu-id="6bb5a-246">1000</span><span class="sxs-lookup"><span data-stu-id="6bb5a-246">1,000</span></span></td>
<td><span data-ttu-id="6bb5a-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6bb5a-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6bb5a-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-249">CC002</span><span class="sxs-lookup"><span data-stu-id="6bb5a-249">CC002</span></span></td>
<td><span data-ttu-id="6bb5a-250">Finantsid</span><span class="sxs-lookup"><span data-stu-id="6bb5a-250">Finance</span></span></td>
<td><span data-ttu-id="6bb5a-251">6,000</span><span class="sxs-lookup"><span data-stu-id="6bb5a-251">6,000</span></span></td>
<td><span data-ttu-id="6bb5a-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6bb5a-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6bb5a-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-254">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-254">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-255">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-255">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-256">0</span><span class="sxs-lookup"><span data-stu-id="6bb5a-256">0</span></span></td>
<td><span data-ttu-id="6bb5a-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6bb5a-258">0,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6bb5a-259">Fikseeritud kulu tuleb jaotada ühtlaselt üksikutele kuluobjektidele, mis on tarbinud elektrit.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="6bb5a-260">Selle tulemuse saate, kasutades valemi eraldamisaluses statistilise dimensiooni liiget Elekter: (Elekter &gt; 0,00). Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-261">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-261">Cost object</span></span></th>
<th><span data-ttu-id="6bb5a-262">Valem</span><span class="sxs-lookup"><span data-stu-id="6bb5a-262">Formula</span></span></th>
<th><span data-ttu-id="6bb5a-263">Väärtus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-263">Magnitude</span></span></th>
<th><span data-ttu-id="6bb5a-264">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="6bb5a-264">Allocation factor</span></span></th>
<th><span data-ttu-id="6bb5a-265">Summa</span><span class="sxs-lookup"><span data-stu-id="6bb5a-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-266">CC001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-266">CC001</span></span></td>
<td><span data-ttu-id="6bb5a-267">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="6bb5a-267">HR</span></span></td>
<td><span data-ttu-id="6bb5a-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6bb5a-269">1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-269">1</span></span></td>
<td><span data-ttu-id="6bb5a-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6bb5a-271">500,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-272">CC002</span><span class="sxs-lookup"><span data-stu-id="6bb5a-272">CC002</span></span></td>
<td><span data-ttu-id="6bb5a-273">Finantsid</span><span class="sxs-lookup"><span data-stu-id="6bb5a-273">Finance</span></span></td>
<td><span data-ttu-id="6bb5a-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6bb5a-275">1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-275">1</span></span></td>
<td><span data-ttu-id="6bb5a-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6bb5a-277">500,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-278">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-278">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-279">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-279">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6bb5a-281">0</span><span class="sxs-lookup"><span data-stu-id="6bb5a-281">0</span></span></td>
<td><span data-ttu-id="6bb5a-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6bb5a-283">0,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6bb5a-284">Tööleht</span><span class="sxs-lookup"><span data-stu-id="6bb5a-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6bb5a-285">Tööleht</span><span class="sxs-lookup"><span data-stu-id="6bb5a-285">Journal</span></span></th>
<th><span data-ttu-id="6bb5a-286">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="6bb5a-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6bb5a-287">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="6bb5a-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6bb5a-288">Versioon</span><span class="sxs-lookup"><span data-stu-id="6bb5a-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-289">00002</span><span class="sxs-lookup"><span data-stu-id="6bb5a-289">00002</span></span></td>
<td><span data-ttu-id="6bb5a-290">Kulujaotuse arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="6bb5a-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="6bb5a-291">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="6bb5a-291">Fiscal</span></span></td>
<td><span data-ttu-id="6bb5a-292">2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-292">2017</span></span></td>
<td><span data-ttu-id="6bb5a-293">Periood 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-293">Period 1</span></span></td>
<td><span data-ttu-id="6bb5a-294">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="6bb5a-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6bb5a-295">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6bb5a-296">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="6bb5a-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6bb5a-297">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6bb5a-298">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="6bb5a-298">Cost element</span></span></th>
<th><span data-ttu-id="6bb5a-299">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-299">Cost behavior</span></span></th>
<th><span data-ttu-id="6bb5a-300">Summa</span><span class="sxs-lookup"><span data-stu-id="6bb5a-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-301">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-302">CC099</span><span class="sxs-lookup"><span data-stu-id="6bb5a-302">CC099</span></span></td>
<td><span data-ttu-id="6bb5a-303">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-303">Default cost center</span></span></td>
<td><span data-ttu-id="6bb5a-304">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-304">10001</span></span></td>
<td><span data-ttu-id="6bb5a-305">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-305">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-306">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-306">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-308">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-309">CC099</span><span class="sxs-lookup"><span data-stu-id="6bb5a-309">CC099</span></span></td>
<td><span data-ttu-id="6bb5a-310">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-310">Default cost center</span></span></td>
<td><span data-ttu-id="6bb5a-311">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-311">10001</span></span></td>
<td><span data-ttu-id="6bb5a-312">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-312">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-313">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-313">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6bb5a-315">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="6bb5a-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-316">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6bb5a-317">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="6bb5a-317">Cost element</span></span></th>
<th><span data-ttu-id="6bb5a-318">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-318">Cost behavior</span></span></th>
<th><span data-ttu-id="6bb5a-319">Summa</span><span class="sxs-lookup"><span data-stu-id="6bb5a-319">Amount</span></span></th>
<th><span data-ttu-id="6bb5a-320">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="6bb5a-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-321">CC099</span><span class="sxs-lookup"><span data-stu-id="6bb5a-321">CC099</span></span></td>
<td><span data-ttu-id="6bb5a-322">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-322">Default cost center</span></span></td>
<td><span data-ttu-id="6bb5a-323">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-323">10001</span></span></td>
<td><span data-ttu-id="6bb5a-324">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-324">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-325">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-325">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-326">–1000,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-326">-1,000.00</span></span></td>
<td><span data-ttu-id="6bb5a-327">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-328">CC001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-328">CC001</span></span></td>
<td><span data-ttu-id="6bb5a-329">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="6bb5a-329">HR</span></span></td>
<td><span data-ttu-id="6bb5a-330">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-330">10001</span></span></td>
<td><span data-ttu-id="6bb5a-331">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-331">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-332">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-332">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-333">500,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-333">500.00</span></span></td>
<td><span data-ttu-id="6bb5a-334">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-335">CC002</span><span class="sxs-lookup"><span data-stu-id="6bb5a-335">CC002</span></span></td>
<td><span data-ttu-id="6bb5a-336">Finantsid</span><span class="sxs-lookup"><span data-stu-id="6bb5a-336">Finance</span></span></td>
<td><span data-ttu-id="6bb5a-337">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-337">10001</span></span></td>
<td><span data-ttu-id="6bb5a-338">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-338">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-339">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-339">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-340">500,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-340">500.00</span></span></td>
<td><span data-ttu-id="6bb5a-341">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-342">CC099</span><span class="sxs-lookup"><span data-stu-id="6bb5a-342">CC099</span></span></td>
<td><span data-ttu-id="6bb5a-343">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-343">Default cost center</span></span></td>
<td><span data-ttu-id="6bb5a-344">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-344">10001</span></span></td>
<td><span data-ttu-id="6bb5a-345">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-345">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-346">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-346">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-347">–9000,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-347">-9,000.00</span></span></td>
<td><span data-ttu-id="6bb5a-348">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-349">CC001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-349">CC001</span></span></td>
<td><span data-ttu-id="6bb5a-350">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="6bb5a-350">HR</span></span></td>
<td><span data-ttu-id="6bb5a-351">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-351">10001</span></span></td>
<td><span data-ttu-id="6bb5a-352">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-352">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-353">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-353">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6bb5a-354">1,285.71</span></span></td>
<td><span data-ttu-id="6bb5a-355">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-356">CC002</span><span class="sxs-lookup"><span data-stu-id="6bb5a-356">CC002</span></span></td>
<td><span data-ttu-id="6bb5a-357">Finantsid</span><span class="sxs-lookup"><span data-stu-id="6bb5a-357">Finance</span></span></td>
<td><span data-ttu-id="6bb5a-358">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-358">10001</span></span></td>
<td><span data-ttu-id="6bb5a-359">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-359">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-360">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-360">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6bb5a-361">7,714.29</span></span></td>
<td><span data-ttu-id="6bb5a-362">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6bb5a-363">Lisateavet vt teemast [Kulujaotise poliitika loomine ja määramine kulujuhtimisüksusele (tegevuse juhis)](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="6bb5a-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="6bb5a-364">3. etapp: üldkulude määra arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="6bb5a-365">Üldkulude määra kasutatakse ühe või mitme kindla kuluobjekti debiteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="6bb5a-366">Tasu põhineb eelmääratud kulumääral ja väärtusel määratud eraldamisalusest.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="6bb5a-367">Üldkulu määra määratlemine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-367">Define the overhead rate</span></span>

<span data-ttu-id="6bb5a-368">Kuluobjekt CC001 inimressursid panustab sisemiste projektide kogumisse.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="6bb5a-369">Luuakse statistilise dimensiooni liige nimega Inimressursside projektid, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-370">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-370">Cost object</span></span></th>
<th><span data-ttu-id="6bb5a-371">Tunnid</span><span class="sxs-lookup"><span data-stu-id="6bb5a-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-372">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-372">Proj 1</span></span></td>
<td><span data-ttu-id="6bb5a-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-373">Project 1</span></span></td>
<td><span data-ttu-id="6bb5a-374">3</span><span class="sxs-lookup"><span data-stu-id="6bb5a-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-375">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-375">Proj 2</span></span></td>
<td><span data-ttu-id="6bb5a-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-376">Project 2</span></span></td>
<td><span data-ttu-id="6bb5a-377">1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6bb5a-378">Määratletud on eelmääratud kulumäär kuluprojektide panusele.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-379">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-379">Cost object</span></span></th>
<th><span data-ttu-id="6bb5a-380">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="6bb5a-380">Cost element</span></span></th>
<th><span data-ttu-id="6bb5a-381">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-381">Cost behavior</span></span></th>
<th><span data-ttu-id="6bb5a-382">Ühikud</span><span class="sxs-lookup"><span data-stu-id="6bb5a-382">Units</span></span></th>
<th><span data-ttu-id="6bb5a-383">Kurss</span><span class="sxs-lookup"><span data-stu-id="6bb5a-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-384">CC001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-384">CC001</span></span></td>
<td><span data-ttu-id="6bb5a-385">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="6bb5a-385">HR</span></span></td>
<td><span data-ttu-id="6bb5a-386">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-386">10001</span></span></td>
<td><span data-ttu-id="6bb5a-387">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-387">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-388">1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-388">1</span></span></td>
<td><span data-ttu-id="6bb5a-389">10</span><span class="sxs-lookup"><span data-stu-id="6bb5a-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6bb5a-390">Järgmises tabelis on näidatud tulemus, kui inimressursside projektid on rakendatud eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-391">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-391">Cost object</span></span></th>
<th><span data-ttu-id="6bb5a-392">Väärtus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-392">Magnitude</span></span></th>
<th><span data-ttu-id="6bb5a-393">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="6bb5a-393">Cost element</span></span></th>
<th><span data-ttu-id="6bb5a-394">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="6bb5a-394">Allocation factor</span></span></th>
<th><span data-ttu-id="6bb5a-395">Summa</span><span class="sxs-lookup"><span data-stu-id="6bb5a-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-396">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-396">Proj 1</span></span></td>
<td><span data-ttu-id="6bb5a-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-397">Project 1</span></span></td>
<td><span data-ttu-id="6bb5a-398">3</span><span class="sxs-lookup"><span data-stu-id="6bb5a-398">3</span></span></td>
<td><span data-ttu-id="6bb5a-399">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-399">10001</span></span></td>
<td><span data-ttu-id="6bb5a-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6bb5a-401">30,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-402">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-402">Proj 2</span></span></td>
<td><span data-ttu-id="6bb5a-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-403">Project 2</span></span></td>
<td><span data-ttu-id="6bb5a-404">1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-404">1</span></span></td>
<td><span data-ttu-id="6bb5a-405">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-405">10001</span></span></td>
<td><span data-ttu-id="6bb5a-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6bb5a-407">10,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6bb5a-408">Tööleht</span><span class="sxs-lookup"><span data-stu-id="6bb5a-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6bb5a-409">Tööleht</span><span class="sxs-lookup"><span data-stu-id="6bb5a-409">Journal</span></span></th>
<th><span data-ttu-id="6bb5a-410">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="6bb5a-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6bb5a-411">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="6bb5a-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6bb5a-412">Versioon</span><span class="sxs-lookup"><span data-stu-id="6bb5a-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-413">00003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-413">00003</span></span></td>
<td><span data-ttu-id="6bb5a-414">Üldkulu määra arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="6bb5a-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="6bb5a-415">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="6bb5a-415">Fiscal</span></span></td>
<td><span data-ttu-id="6bb5a-416">2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-416">2017</span></span></td>
<td><span data-ttu-id="6bb5a-417">Periood 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-417">Period 1</span></span></td>
<td><span data-ttu-id="6bb5a-418">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="6bb5a-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="6bb5a-419">Töölehe sisestused (töölehe sisestused üldkulu määra arvutamiseks)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6bb5a-420">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="6bb5a-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6bb5a-421">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-421">Cost object</span></span></th>
<th><span data-ttu-id="6bb5a-422">Väärtus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-423">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-424">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-424">Proj 1</span></span></td>
<td><span data-ttu-id="6bb5a-425">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6bb5a-426">3,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-427">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-428">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-428">Proj 2</span></span></td>
<td><span data-ttu-id="6bb5a-429">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6bb5a-430">1,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6bb5a-431">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="6bb5a-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-432">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6bb5a-433">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="6bb5a-433">Cost element</span></span></th>
<th><span data-ttu-id="6bb5a-434">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-434">Cost behavior</span></span></th>
<th><span data-ttu-id="6bb5a-435">Summa</span><span class="sxs-lookup"><span data-stu-id="6bb5a-435">Amount</span></span></th>
<th><span data-ttu-id="6bb5a-436">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="6bb5a-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-437">CC0001</span></span></td>
<td><span data-ttu-id="6bb5a-438">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="6bb5a-438">HR</span></span></td>
<td><span data-ttu-id="6bb5a-439">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-439">10001</span></span></td>
<td><span data-ttu-id="6bb5a-440">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-440">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-441">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-441">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-442">–30,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-442">-30.00</span></span></td>
<td><span data-ttu-id="6bb5a-443">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-444">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-444">Proj 1</span></span></td>
<td><span data-ttu-id="6bb5a-445">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6bb5a-446">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-446">10001</span></span></td>
<td><span data-ttu-id="6bb5a-447">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-447">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-448">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-448">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-449">30,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-449">30.00</span></span></td>
<td><span data-ttu-id="6bb5a-450">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-451">CC001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-451">CC001</span></span></td>
<td><span data-ttu-id="6bb5a-452">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="6bb5a-452">HR</span></span></td>
<td><span data-ttu-id="6bb5a-453">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-453">10001</span></span></td>
<td><span data-ttu-id="6bb5a-454">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-454">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-455">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-455">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-456">-10.00</span></span></td>
<td><span data-ttu-id="6bb5a-457">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-458">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-458">Proj 2</span></span></td>
<td><span data-ttu-id="6bb5a-459">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6bb5a-460">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-460">10001</span></span></td>
<td><span data-ttu-id="6bb5a-461">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-461">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-462">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-462">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-463">10.00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-463">10.00</span></span></td>
<td><span data-ttu-id="6bb5a-464">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6bb5a-465">Lisateavet vt teemast [Üldkulude arvutamine](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="6bb5a-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="6bb5a-466">4. etapp: kulueralduse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="6bb5a-467">Eraldamist kasutatakse kuluobjekti saldo eraldamiseks teistele kuluobjektidele, rakendades eraldamisalust.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="6bb5a-468">Finance and Operations toetab vastastikuse eraldamise meetodit.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="6bb5a-469">Vastastikuse eraldamise meetodi puhul tuvastatakse täiendavate kuluobjektide vahetatavad vastastikused teenused.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="6bb5a-470">Süsteem määrab automaatselt eraldamiste tegemise õige järjekorra.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="6bb5a-471">Kuluobjekti saldo eraldatakse üksiku eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="6bb5a-472">Toetatakse eraldamisi kuluobjektide dimensioonide ja nende vastavate liikmete seas.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="6bb5a-473">Eraldamisjärjekorda reguleerib kulujuhtseade.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="6bb5a-474">[![Vastastikune meetod](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="6bb5a-475">Kulueraldamise määratlemine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-475">Define the cost allocation</span></span>

<span data-ttu-id="6bb5a-476">Siin on lihtne näide, mis selgitab, kuidas jälgida kulu liikumist.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="6bb5a-477">Kuluobjekt CC001 inimressursid panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="6bb5a-478">Luuakse statistilise dimensiooni liige nimega Inimressursside teenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-479">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-479">Cost object</span></span></th>
<th><span data-ttu-id="6bb5a-480">Inimressursside teenused</span><span class="sxs-lookup"><span data-stu-id="6bb5a-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-481">CC002</span><span class="sxs-lookup"><span data-stu-id="6bb5a-481">CC002</span></span></td>
<td><span data-ttu-id="6bb5a-482">Finantsid</span><span class="sxs-lookup"><span data-stu-id="6bb5a-482">Finance</span></span></td>
<td><span data-ttu-id="6bb5a-483">35</span><span class="sxs-lookup"><span data-stu-id="6bb5a-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-484">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-484">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-485">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-485">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-486">55</span><span class="sxs-lookup"><span data-stu-id="6bb5a-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-487">CC004</span><span class="sxs-lookup"><span data-stu-id="6bb5a-487">CC004</span></span></td>
<td><span data-ttu-id="6bb5a-488">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-488">Packaging</span></span></td>
<td><span data-ttu-id="6bb5a-489">10</span><span class="sxs-lookup"><span data-stu-id="6bb5a-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6bb5a-490">Kuluobjekt CC002 rahandus panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="6bb5a-491">Luuakse statistilise dimensiooni liige nimega Rahandusteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-492">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-492">Cost object</span></span></th>
<th><span data-ttu-id="6bb5a-493">Rahandusteenused</span><span class="sxs-lookup"><span data-stu-id="6bb5a-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-494">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-494">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-495">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-495">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-496">65</span><span class="sxs-lookup"><span data-stu-id="6bb5a-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-497">CC004</span><span class="sxs-lookup"><span data-stu-id="6bb5a-497">CC004</span></span></td>
<td><span data-ttu-id="6bb5a-498">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-498">Packaging</span></span></td>
<td><span data-ttu-id="6bb5a-499">35</span><span class="sxs-lookup"><span data-stu-id="6bb5a-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6bb5a-500">Kuluobjekt CC003 assembler panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="6bb5a-501">Luuakse statistilise dimensiooni liige nimega Assembleriteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-502">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-502">Cost object</span></span></th>
<th><span data-ttu-id="6bb5a-503">Assembleriteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-504">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-504">Prod 1</span></span></td>
<td><span data-ttu-id="6bb5a-505">Toode 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-505">Product 1</span></span></td>
<td><span data-ttu-id="6bb5a-506">60</span><span class="sxs-lookup"><span data-stu-id="6bb5a-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-507">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-507">Prod 2</span></span></td>
<td><span data-ttu-id="6bb5a-508">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-508">Product 2</span></span></td>
<td><span data-ttu-id="6bb5a-509">20</span><span class="sxs-lookup"><span data-stu-id="6bb5a-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6bb5a-510">Kuluobjekt CC004 pakendamine panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="6bb5a-511">Luuakse statistilise dimensiooni liige nimega Pakendamisteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-512">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-512">Cost object</span></span></th>
<th><span data-ttu-id="6bb5a-513">Pakendamisteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-514">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-514">Prod 1</span></span></td>
<td><span data-ttu-id="6bb5a-515">Toode 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-515">Product 1</span></span></td>
<td><span data-ttu-id="6bb5a-516">80</span><span class="sxs-lookup"><span data-stu-id="6bb5a-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-517">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-517">Prod 2</span></span></td>
<td><span data-ttu-id="6bb5a-518">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-518">Product 2</span></span></td>
<td><span data-ttu-id="6bb5a-519">sept.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6bb5a-520">Finance and Operationsis saab statistilised mõõdud, nagu toote tarbitud tootmistunnid, tuletada lähteandmetest.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="6bb5a-521">Lisateavet vt teemast [Statistiliste mõõtude pakkuja mall](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="6bb5a-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="6bb5a-522">Järgmises tabelis on näidatud tulemus, kui HR-teenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="6bb5a-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-523">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-523">Cost object</span></span></th>
<th><span data-ttu-id="6bb5a-524">Väärtus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-524">Magnitude</span></span></th>
<th><span data-ttu-id="6bb5a-525">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="6bb5a-525">Allocation factor</span></span></th>
<th><span data-ttu-id="6bb5a-526">Summa</span><span class="sxs-lookup"><span data-stu-id="6bb5a-526">Amount</span></span></th>
<th><span data-ttu-id="6bb5a-527">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-528">CC002</span><span class="sxs-lookup"><span data-stu-id="6bb5a-528">CC002</span></span></td>
<td><span data-ttu-id="6bb5a-529">Finantsid</span><span class="sxs-lookup"><span data-stu-id="6bb5a-529">Finance</span></span></td>
<td><span data-ttu-id="6bb5a-530">35</span><span class="sxs-lookup"><span data-stu-id="6bb5a-530">35</span></span></td>
<td><span data-ttu-id="6bb5a-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6bb5a-532">175.00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-532">175.00</span></span></td>
<td><span data-ttu-id="6bb5a-533">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-534">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-534">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-535">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-535">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-536">55</span><span class="sxs-lookup"><span data-stu-id="6bb5a-536">55</span></span></td>
<td><span data-ttu-id="6bb5a-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6bb5a-538">275.00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-538">275.00</span></span></td>
<td><span data-ttu-id="6bb5a-539">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-540">CC004</span><span class="sxs-lookup"><span data-stu-id="6bb5a-540">CC004</span></span></td>
<td><span data-ttu-id="6bb5a-541">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-541">Packaging</span></span></td>
<td><span data-ttu-id="6bb5a-542">10</span><span class="sxs-lookup"><span data-stu-id="6bb5a-542">10</span></span></td>
<td><span data-ttu-id="6bb5a-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6bb5a-544">50,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-544">50.00</span></span></td>
<td><span data-ttu-id="6bb5a-545">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-546">CC002</span><span class="sxs-lookup"><span data-stu-id="6bb5a-546">CC002</span></span></td>
<td><span data-ttu-id="6bb5a-547">Finantsid</span><span class="sxs-lookup"><span data-stu-id="6bb5a-547">Finance</span></span></td>
<td><span data-ttu-id="6bb5a-548">35</span><span class="sxs-lookup"><span data-stu-id="6bb5a-548">35</span></span></td>
<td><span data-ttu-id="6bb5a-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="6bb5a-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6bb5a-550">436.00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-550">436.00</span></span></td>
<td><span data-ttu-id="6bb5a-551">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-552">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-552">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-553">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-553">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-554">55</span><span class="sxs-lookup"><span data-stu-id="6bb5a-554">55</span></span></td>
<td><span data-ttu-id="6bb5a-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="6bb5a-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6bb5a-556">685.14</span><span class="sxs-lookup"><span data-stu-id="6bb5a-556">685.14</span></span></td>
<td><span data-ttu-id="6bb5a-557">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-558">CC004</span><span class="sxs-lookup"><span data-stu-id="6bb5a-558">CC004</span></span></td>
<td><span data-ttu-id="6bb5a-559">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-559">Packaging</span></span></td>
<td><span data-ttu-id="6bb5a-560">10</span><span class="sxs-lookup"><span data-stu-id="6bb5a-560">10</span></span></td>
<td><span data-ttu-id="6bb5a-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="6bb5a-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6bb5a-562">124.57</span><span class="sxs-lookup"><span data-stu-id="6bb5a-562">124.57</span></span></td>
<td><span data-ttu-id="6bb5a-563">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6bb5a-564">Järgmises tabelis on näidatud tulemus, kui Rahandusteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="6bb5a-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-565">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-565">Cost object</span></span></th>
<th><span data-ttu-id="6bb5a-566">Väärtus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-566">Magnitude</span></span></th>
<th><span data-ttu-id="6bb5a-567">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="6bb5a-567">Allocation factor</span></span></th>
<th><span data-ttu-id="6bb5a-568">Summa</span><span class="sxs-lookup"><span data-stu-id="6bb5a-568">Amount</span></span></th>
<th><span data-ttu-id="6bb5a-569">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-570">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-570">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-571">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-571">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-572">65</span><span class="sxs-lookup"><span data-stu-id="6bb5a-572">65</span></span></td>
<td><span data-ttu-id="6bb5a-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6bb5a-574">438.75</span><span class="sxs-lookup"><span data-stu-id="6bb5a-574">438.75</span></span></td>
<td><span data-ttu-id="6bb5a-575">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-576">CC004</span><span class="sxs-lookup"><span data-stu-id="6bb5a-576">CC004</span></span></td>
<td><span data-ttu-id="6bb5a-577">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-577">Packaging</span></span></td>
<td><span data-ttu-id="6bb5a-578">35</span><span class="sxs-lookup"><span data-stu-id="6bb5a-578">35</span></span></td>
<td><span data-ttu-id="6bb5a-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6bb5a-580">236.25</span><span class="sxs-lookup"><span data-stu-id="6bb5a-580">236.25</span></span></td>
<td><span data-ttu-id="6bb5a-581">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-582">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-582">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-583">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-583">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-584">65</span><span class="sxs-lookup"><span data-stu-id="6bb5a-584">65</span></span></td>
<td><span data-ttu-id="6bb5a-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6bb5a-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6bb5a-586">5,297.69</span></span></td>
<td><span data-ttu-id="6bb5a-587">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-588">CC004</span><span class="sxs-lookup"><span data-stu-id="6bb5a-588">CC004</span></span></td>
<td><span data-ttu-id="6bb5a-589">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-589">Packaging</span></span></td>
<td><span data-ttu-id="6bb5a-590">35</span><span class="sxs-lookup"><span data-stu-id="6bb5a-590">35</span></span></td>
<td><span data-ttu-id="6bb5a-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6bb5a-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6bb5a-592">2,852.60</span></span></td>
<td><span data-ttu-id="6bb5a-593">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6bb5a-594">Järgmises tabelis on näidatud tulemus, kui Assembleriteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="6bb5a-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-595">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-595">Cost object</span></span></th>
<th><span data-ttu-id="6bb5a-596">Väärtus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-596">Magnitude</span></span></th>
<th><span data-ttu-id="6bb5a-597">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="6bb5a-597">Allocation factor</span></span></th>
<th><span data-ttu-id="6bb5a-598">Summa</span><span class="sxs-lookup"><span data-stu-id="6bb5a-598">Amount</span></span></th>
<th><span data-ttu-id="6bb5a-599">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-600">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-600">Prod 1</span></span></td>
<td><span data-ttu-id="6bb5a-601">Toode 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-601">Product 1</span></span></td>
<td><span data-ttu-id="6bb5a-602">60</span><span class="sxs-lookup"><span data-stu-id="6bb5a-602">60</span></span></td>
<td><span data-ttu-id="6bb5a-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6bb5a-604">535.31</span><span class="sxs-lookup"><span data-stu-id="6bb5a-604">535.31</span></span></td>
<td><span data-ttu-id="6bb5a-605">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-606">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-606">Prod 2</span></span></td>
<td><span data-ttu-id="6bb5a-607">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-607">Product 2</span></span></td>
<td><span data-ttu-id="6bb5a-608">20</span><span class="sxs-lookup"><span data-stu-id="6bb5a-608">20</span></span></td>
<td><span data-ttu-id="6bb5a-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6bb5a-610">178.44</span><span class="sxs-lookup"><span data-stu-id="6bb5a-610">178.44</span></span></td>
<td><span data-ttu-id="6bb5a-611">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-612">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-612">Prod 1</span></span></td>
<td><span data-ttu-id="6bb5a-613">Toode 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-613">Product 1</span></span></td>
<td><span data-ttu-id="6bb5a-614">60</span><span class="sxs-lookup"><span data-stu-id="6bb5a-614">60</span></span></td>
<td><span data-ttu-id="6bb5a-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6bb5a-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6bb5a-616">4,487.12</span></span></td>
<td><span data-ttu-id="6bb5a-617">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-618">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-618">Prod 2</span></span></td>
<td><span data-ttu-id="6bb5a-619">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-619">Product 2</span></span></td>
<td><span data-ttu-id="6bb5a-620">20</span><span class="sxs-lookup"><span data-stu-id="6bb5a-620">20</span></span></td>
<td><span data-ttu-id="6bb5a-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6bb5a-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6bb5a-622">1,495.71</span></span></td>
<td><span data-ttu-id="6bb5a-623">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6bb5a-624">Järgmises tabelis on näidatud tulemus, kui Pakendamisteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="6bb5a-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-625">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-625">Cost object</span></span></th>
<th><span data-ttu-id="6bb5a-626">Väärtus</span><span class="sxs-lookup"><span data-stu-id="6bb5a-626">Magnitude</span></span></th>
<th><span data-ttu-id="6bb5a-627">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="6bb5a-627">Allocation factor</span></span></th>
<th><span data-ttu-id="6bb5a-628">Summa</span><span class="sxs-lookup"><span data-stu-id="6bb5a-628">Amount</span></span></th>
<th><span data-ttu-id="6bb5a-629">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-630">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-630">Prod 1</span></span></td>
<td><span data-ttu-id="6bb5a-631">Toode 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-631">Product 1</span></span></td>
<td><span data-ttu-id="6bb5a-632">80</span><span class="sxs-lookup"><span data-stu-id="6bb5a-632">80</span></span></td>
<td><span data-ttu-id="6bb5a-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6bb5a-634">241.05</span><span class="sxs-lookup"><span data-stu-id="6bb5a-634">241.05</span></span></td>
<td><span data-ttu-id="6bb5a-635">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-636">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-636">Prod 2</span></span></td>
<td><span data-ttu-id="6bb5a-637">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-637">Product 2</span></span></td>
<td><span data-ttu-id="6bb5a-638">15</span><span class="sxs-lookup"><span data-stu-id="6bb5a-638">15</span></span></td>
<td><span data-ttu-id="6bb5a-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6bb5a-640">45.20</span><span class="sxs-lookup"><span data-stu-id="6bb5a-640">45.20</span></span></td>
<td><span data-ttu-id="6bb5a-641">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-642">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-642">Prod 1</span></span></td>
<td><span data-ttu-id="6bb5a-643">Toode 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-643">Product 1</span></span></td>
<td><span data-ttu-id="6bb5a-644">80</span><span class="sxs-lookup"><span data-stu-id="6bb5a-644">80</span></span></td>
<td><span data-ttu-id="6bb5a-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6bb5a-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6bb5a-646">2,507.09</span></span></td>
<td><span data-ttu-id="6bb5a-647">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-648">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-648">Prod 2</span></span></td>
<td><span data-ttu-id="6bb5a-649">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-649">Product 2</span></span></td>
<td><span data-ttu-id="6bb5a-650">15</span><span class="sxs-lookup"><span data-stu-id="6bb5a-650">15</span></span></td>
<td><span data-ttu-id="6bb5a-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6bb5a-652">470.08</span><span class="sxs-lookup"><span data-stu-id="6bb5a-652">470.08</span></span></td>
<td><span data-ttu-id="6bb5a-653">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6bb5a-654">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="6bb5a-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6bb5a-655">Tööleht</span><span class="sxs-lookup"><span data-stu-id="6bb5a-655">Journal</span></span></th>
<th><span data-ttu-id="6bb5a-656">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="6bb5a-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6bb5a-657">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="6bb5a-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6bb5a-658">Versioon</span><span class="sxs-lookup"><span data-stu-id="6bb5a-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-659">00004</span><span class="sxs-lookup"><span data-stu-id="6bb5a-659">00004</span></span></td>
<td><span data-ttu-id="6bb5a-660">Kulueralduse tööleht</span><span class="sxs-lookup"><span data-stu-id="6bb5a-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="6bb5a-661">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="6bb5a-661">Fiscal</span></span></td>
<td><span data-ttu-id="6bb5a-662">2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-662">2017</span></span></td>
<td><span data-ttu-id="6bb5a-663">Periood 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-663">Period 1</span></span></td>
<td><span data-ttu-id="6bb5a-664">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="6bb5a-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="6bb5a-665">Töölehe read</span><span class="sxs-lookup"><span data-stu-id="6bb5a-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6bb5a-666">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="6bb5a-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6bb5a-667">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6bb5a-668">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="6bb5a-668">Cost element</span></span></th>
<th><span data-ttu-id="6bb5a-669">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-669">Cost behavior</span></span></th>
<th><span data-ttu-id="6bb5a-670">Summa</span><span class="sxs-lookup"><span data-stu-id="6bb5a-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-671">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-672">CC001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-672">CC001</span></span></td>
<td><span data-ttu-id="6bb5a-673">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="6bb5a-673">HR</span></span></td>
<td><span data-ttu-id="6bb5a-674">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-674">10001</span></span></td>
<td><span data-ttu-id="6bb5a-675">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-675">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-676">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-676">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-677">500,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-678">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-679">CC001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-679">CC001</span></span></td>
<td><span data-ttu-id="6bb5a-680">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="6bb5a-680">HR</span></span></td>
<td><span data-ttu-id="6bb5a-681">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-681">10001</span></span></td>
<td><span data-ttu-id="6bb5a-682">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-682">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-683">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-683">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="6bb5a-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-685">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-686">CC002</span><span class="sxs-lookup"><span data-stu-id="6bb5a-686">CC002</span></span></td>
<td><span data-ttu-id="6bb5a-687">Finantsid</span><span class="sxs-lookup"><span data-stu-id="6bb5a-687">Finance</span></span></td>
<td><span data-ttu-id="6bb5a-688">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-688">10001</span></span></td>
<td><span data-ttu-id="6bb5a-689">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-689">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-690">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-690">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-691">675.00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-692">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-693">CC002</span><span class="sxs-lookup"><span data-stu-id="6bb5a-693">CC002</span></span></td>
<td><span data-ttu-id="6bb5a-694">Finantsid</span><span class="sxs-lookup"><span data-stu-id="6bb5a-694">Finance</span></span></td>
<td><span data-ttu-id="6bb5a-695">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-695">10001</span></span></td>
<td><span data-ttu-id="6bb5a-696">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-696">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-697">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-697">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="6bb5a-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-699">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-700">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-700">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-701">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-701">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-702">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-702">10001</span></span></td>
<td><span data-ttu-id="6bb5a-703">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-703">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-704">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-704">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-705">713.75</span><span class="sxs-lookup"><span data-stu-id="6bb5a-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-706">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-707">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-707">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-708">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-708">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-709">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-709">10001</span></span></td>
<td><span data-ttu-id="6bb5a-710">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-710">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-711">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-711">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="6bb5a-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-713">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-714">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-714">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-715">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-715">Packaging</span></span></td>
<td><span data-ttu-id="6bb5a-716">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-716">10001</span></span></td>
<td><span data-ttu-id="6bb5a-717">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-717">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-718">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-718">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-719">286.25</span><span class="sxs-lookup"><span data-stu-id="6bb5a-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-720">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-721">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-721">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-722">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-722">Packaging</span></span></td>
<td><span data-ttu-id="6bb5a-723">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-723">10001</span></span></td>
<td><span data-ttu-id="6bb5a-724">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-724">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-725">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-725">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="6bb5a-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-727">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-728">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-728">Prod 1</span></span></td>
<td><span data-ttu-id="6bb5a-729">Toode 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-729">Product 1</span></span></td>
<td><span data-ttu-id="6bb5a-730">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-730">10001</span></span></td>
<td><span data-ttu-id="6bb5a-731">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-731">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-732">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-732">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-733">776.36</span><span class="sxs-lookup"><span data-stu-id="6bb5a-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-734">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-735">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-735">Prod 1</span></span></td>
<td><span data-ttu-id="6bb5a-736">Toode 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-736">Product 1</span></span></td>
<td><span data-ttu-id="6bb5a-737">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-737">10001</span></span></td>
<td><span data-ttu-id="6bb5a-738">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-738">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-739">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-739">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6bb5a-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-741">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-742">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-742">Prod 2</span></span></td>
<td><span data-ttu-id="6bb5a-743">Toode 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-743">Product 1</span></span></td>
<td><span data-ttu-id="6bb5a-744">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-744">10001</span></span></td>
<td><span data-ttu-id="6bb5a-745">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-745">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-746">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-746">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-747">223.64</span><span class="sxs-lookup"><span data-stu-id="6bb5a-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-748">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="6bb5a-749">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-749">Prod 2</span></span></td>
<td><span data-ttu-id="6bb5a-750">Toode 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-750">Product 1</span></span></td>
<td><span data-ttu-id="6bb5a-751">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-751">10001</span></span></td>
<td><span data-ttu-id="6bb5a-752">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-752">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-753">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-753">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6bb5a-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6bb5a-755">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="6bb5a-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6bb5a-756">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6bb5a-757">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="6bb5a-757">Cost element</span></span></th>
<th><span data-ttu-id="6bb5a-758">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-758">Cost behavior</span></span></th>
<th><span data-ttu-id="6bb5a-759">Summa</span><span class="sxs-lookup"><span data-stu-id="6bb5a-759">Amount</span></span></th>
<th><span data-ttu-id="6bb5a-760">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="6bb5a-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6bb5a-761">CC001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-761">CC001</span></span></td>
<td><span data-ttu-id="6bb5a-762">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="6bb5a-762">HR</span></span></td>
<td><span data-ttu-id="6bb5a-763">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-763">10001</span></span></td>
<td><span data-ttu-id="6bb5a-764">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-764">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-765">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-765">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-766">‑500,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-766">-500.00</span></span></td>
<td><span data-ttu-id="6bb5a-767">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-768">CC002</span><span class="sxs-lookup"><span data-stu-id="6bb5a-768">CC002</span></span></td>
<td><span data-ttu-id="6bb5a-769">Finantsid</span><span class="sxs-lookup"><span data-stu-id="6bb5a-769">Finance</span></span></td>
<td><span data-ttu-id="6bb5a-770">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-770">10001</span></span></td>
<td><span data-ttu-id="6bb5a-771">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-771">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-772">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-772">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-773">175.00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-773">175.00</span></span></td>
<td><span data-ttu-id="6bb5a-774">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-775">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-775">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-776">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-776">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-777">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-777">10001</span></span></td>
<td><span data-ttu-id="6bb5a-778">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-778">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-779">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-779">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-780">275.00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-780">275.00</span></span></td>
<td><span data-ttu-id="6bb5a-781">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-782">CC004</span><span class="sxs-lookup"><span data-stu-id="6bb5a-782">CC004</span></span></td>
<td><span data-ttu-id="6bb5a-783">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-783">Packaging</span></span></td>
<td><span data-ttu-id="6bb5a-784">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-784">10001</span></span></td>
<td><span data-ttu-id="6bb5a-785">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-785">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-786">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-786">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-787">50,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-787">50,00</span></span></td>
<td><span data-ttu-id="6bb5a-788">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-789">CC001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-789">CC001</span></span></td>
<td><span data-ttu-id="6bb5a-790">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="6bb5a-790">HR</span></span></td>
<td><span data-ttu-id="6bb5a-791">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-791">10001</span></span></td>
<td><span data-ttu-id="6bb5a-792">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-792">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-793">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-793">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-794">–1245,71</span><span class="sxs-lookup"><span data-stu-id="6bb5a-794">-1,245.71</span></span></td>
<td><span data-ttu-id="6bb5a-795">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-796">CC002</span><span class="sxs-lookup"><span data-stu-id="6bb5a-796">CC002</span></span></td>
<td><span data-ttu-id="6bb5a-797">Finantsid</span><span class="sxs-lookup"><span data-stu-id="6bb5a-797">Finance</span></span></td>
<td><span data-ttu-id="6bb5a-798">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-798">10001</span></span></td>
<td><span data-ttu-id="6bb5a-799">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-799">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-800">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-800">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-801">436.00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-801">436.00</span></span></td>
<td><span data-ttu-id="6bb5a-802">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-803">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-803">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-804">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-804">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-805">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-805">10001</span></span></td>
<td><span data-ttu-id="6bb5a-806">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-806">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-807">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-807">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-808">685.14</span><span class="sxs-lookup"><span data-stu-id="6bb5a-808">685.14</span></span></td>
<td><span data-ttu-id="6bb5a-809">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-810">CC004</span><span class="sxs-lookup"><span data-stu-id="6bb5a-810">CC004</span></span></td>
<td><span data-ttu-id="6bb5a-811">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-811">Packaging</span></span></td>
<td><span data-ttu-id="6bb5a-812">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-812">10001</span></span></td>
<td><span data-ttu-id="6bb5a-813">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-813">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-814">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-814">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-815">124.57</span><span class="sxs-lookup"><span data-stu-id="6bb5a-815">124.57</span></span></td>
<td><span data-ttu-id="6bb5a-816">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-817">CC002</span><span class="sxs-lookup"><span data-stu-id="6bb5a-817">CC002</span></span></td>
<td><span data-ttu-id="6bb5a-818">Finantsid</span><span class="sxs-lookup"><span data-stu-id="6bb5a-818">Finance</span></span></td>
<td><span data-ttu-id="6bb5a-819">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-819">10001</span></span></td>
<td><span data-ttu-id="6bb5a-820">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-820">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-821">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-821">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-822">–675,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-822">-675.00</span></span></td>
<td><span data-ttu-id="6bb5a-823">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-824">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-824">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-825">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-825">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-826">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-826">10001</span></span></td>
<td><span data-ttu-id="6bb5a-827">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-827">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-828">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-828">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-829">438.75</span><span class="sxs-lookup"><span data-stu-id="6bb5a-829">438.75</span></span></td>
<td><span data-ttu-id="6bb5a-830">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-831">CC004</span><span class="sxs-lookup"><span data-stu-id="6bb5a-831">CC004</span></span></td>
<td><span data-ttu-id="6bb5a-832">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-832">Packaging</span></span></td>
<td><span data-ttu-id="6bb5a-833">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-833">10001</span></span></td>
<td><span data-ttu-id="6bb5a-834">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-834">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-835">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-835">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-836">236.25</span><span class="sxs-lookup"><span data-stu-id="6bb5a-836">236.25</span></span></td>
<td><span data-ttu-id="6bb5a-837">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-838">CC002</span><span class="sxs-lookup"><span data-stu-id="6bb5a-838">CC002</span></span></td>
<td><span data-ttu-id="6bb5a-839">Finantsid</span><span class="sxs-lookup"><span data-stu-id="6bb5a-839">Finance</span></span></td>
<td><span data-ttu-id="6bb5a-840">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-840">10001</span></span></td>
<td><span data-ttu-id="6bb5a-841">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-841">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-842">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-842">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-843">–8150,29</span><span class="sxs-lookup"><span data-stu-id="6bb5a-843">-8,150.29</span></span></td>
<td><span data-ttu-id="6bb5a-844">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-845">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-845">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-846">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-846">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-847">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-847">10001</span></span></td>
<td><span data-ttu-id="6bb5a-848">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-848">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-849">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-849">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6bb5a-850">5,297.69</span></span></td>
<td><span data-ttu-id="6bb5a-851">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-852">CC004</span><span class="sxs-lookup"><span data-stu-id="6bb5a-852">CC004</span></span></td>
<td><span data-ttu-id="6bb5a-853">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="6bb5a-853">Packaging</span></span></td>
<td><span data-ttu-id="6bb5a-854">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-854">10001</span></span></td>
<td><span data-ttu-id="6bb5a-855">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-855">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-856">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-856">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6bb5a-857">2,852.60</span></span></td>
<td><span data-ttu-id="6bb5a-858">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-859">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-859">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-860">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-860">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-861">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-861">10001</span></span></td>
<td><span data-ttu-id="6bb5a-862">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-862">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-863">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-863">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-864">–713,75</span><span class="sxs-lookup"><span data-stu-id="6bb5a-864">-713.75</span></span></td>
<td><span data-ttu-id="6bb5a-865">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-866">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-866">Prod 1</span></span></td>
<td><span data-ttu-id="6bb5a-867">Toode 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-867">Product 1</span></span></td>
<td><span data-ttu-id="6bb5a-868">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-868">10001</span></span></td>
<td><span data-ttu-id="6bb5a-869">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-869">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-870">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-870">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-871">535.31</span><span class="sxs-lookup"><span data-stu-id="6bb5a-871">535.31</span></span></td>
<td><span data-ttu-id="6bb5a-872">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-873">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-873">Prod 2</span></span></td>
<td><span data-ttu-id="6bb5a-874">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-874">Product 2</span></span></td>
<td><span data-ttu-id="6bb5a-875">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-875">10001</span></span></td>
<td><span data-ttu-id="6bb5a-876">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-876">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-877">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-877">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-878">178.44</span><span class="sxs-lookup"><span data-stu-id="6bb5a-878">178.44</span></span></td>
<td><span data-ttu-id="6bb5a-879">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-880">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-880">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-881">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-881">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-882">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-882">10001</span></span></td>
<td><span data-ttu-id="6bb5a-883">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-883">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-884">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-884">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-885">–5982,83</span><span class="sxs-lookup"><span data-stu-id="6bb5a-885">-5,982.83</span></span></td>
<td><span data-ttu-id="6bb5a-886">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-887">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-887">Prod 1</span></span></td>
<td><span data-ttu-id="6bb5a-888">Toode 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-888">Product 1</span></span></td>
<td><span data-ttu-id="6bb5a-889">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-889">10001</span></span></td>
<td><span data-ttu-id="6bb5a-890">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-890">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-891">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-891">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6bb5a-892">4,487.12</span></span></td>
<td><span data-ttu-id="6bb5a-893">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-894">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-894">Prod 2</span></span></td>
<td><span data-ttu-id="6bb5a-895">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-895">Product 2</span></span></td>
<td><span data-ttu-id="6bb5a-896">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-896">10001</span></span></td>
<td><span data-ttu-id="6bb5a-897">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-897">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-898">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-898">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6bb5a-899">1,495.71</span></span></td>
<td><span data-ttu-id="6bb5a-900">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-901">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-901">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-902">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-902">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-903">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-903">10001</span></span></td>
<td><span data-ttu-id="6bb5a-904">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-904">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-905">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-905">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-906">–286,25</span><span class="sxs-lookup"><span data-stu-id="6bb5a-906">-286.25</span></span></td>
<td><span data-ttu-id="6bb5a-907">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-908">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-908">Prod 1</span></span></td>
<td><span data-ttu-id="6bb5a-909">Toode 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-909">Product 1</span></span></td>
<td><span data-ttu-id="6bb5a-910">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-910">10001</span></span></td>
<td><span data-ttu-id="6bb5a-911">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-911">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-912">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-912">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-913">241.05</span><span class="sxs-lookup"><span data-stu-id="6bb5a-913">241.05</span></span></td>
<td><span data-ttu-id="6bb5a-914">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-915">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-915">Prod 2</span></span></td>
<td><span data-ttu-id="6bb5a-916">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-916">Product 2</span></span></td>
<td><span data-ttu-id="6bb5a-917">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-917">10001</span></span></td>
<td><span data-ttu-id="6bb5a-918">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-918">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-919">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-919">Fixed cost</span></span></td>
<td><span data-ttu-id="6bb5a-920">45.20</span><span class="sxs-lookup"><span data-stu-id="6bb5a-920">45.20</span></span></td>
<td><span data-ttu-id="6bb5a-921">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-922">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-922">CC003</span></span></td>
<td><span data-ttu-id="6bb5a-923">Assembler</span><span class="sxs-lookup"><span data-stu-id="6bb5a-923">Assembly</span></span></td>
<td><span data-ttu-id="6bb5a-924">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-924">10001</span></span></td>
<td><span data-ttu-id="6bb5a-925">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-925">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-926">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-926">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-927">–2977,17</span><span class="sxs-lookup"><span data-stu-id="6bb5a-927">-2,977.17</span></span></td>
<td><span data-ttu-id="6bb5a-928">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-929">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-929">Prod 1</span></span></td>
<td><span data-ttu-id="6bb5a-930">Toode 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-930">Product 1</span></span></td>
<td><span data-ttu-id="6bb5a-931">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-931">10001</span></span></td>
<td><span data-ttu-id="6bb5a-932">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-932">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-933">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-933">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6bb5a-934">2,507.09</span></span></td>
<td><span data-ttu-id="6bb5a-935">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6bb5a-936">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-936">Prod 2</span></span></td>
<td><span data-ttu-id="6bb5a-937">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-937">Product 2</span></span></td>
<td><span data-ttu-id="6bb5a-938">10001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-938">10001</span></span></td>
<td><span data-ttu-id="6bb5a-939">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="6bb5a-939">Electricity</span></span></td>
<td><span data-ttu-id="6bb5a-940">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-940">Variable cost</span></span></td>
<td><span data-ttu-id="6bb5a-941">470.08</span><span class="sxs-lookup"><span data-stu-id="6bb5a-941">470.08</span></span></td>
<td><span data-ttu-id="6bb5a-942">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="6bb5a-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="6bb5a-943">Lõppsõna</span><span class="sxs-lookup"><span data-stu-id="6bb5a-943">Conclusion</span></span>
<span data-ttu-id="6bb5a-944">Finantsaruandluses sisestatakse elektrikulu 10 000,00 fiktiivse kulukeskuse ID-le.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="6bb5a-945">Nii teavad kuluarvestajad, et see kulu tuleb eraldada.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="6bb5a-946">Kuluarvestuses liigub kulu rakendatud poliitikate ja reeglite põhjal läbi organisatsiooniüksuste ja -tasemete.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="6bb5a-947">Iga kulu on seostatud eraldamisalusega, mis pakub kulude eraldamiseks parimat hinnangut.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="6bb5a-948">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="6bb5a-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="6bb5a-949">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="6bb5a-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="6bb5a-950">Kokku</span><span class="sxs-lookup"><span data-stu-id="6bb5a-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6bb5a-951">CC099</span><span class="sxs-lookup"><span data-stu-id="6bb5a-951">CC099</span></span></th>
<th><span data-ttu-id="6bb5a-952">CC001</span><span class="sxs-lookup"><span data-stu-id="6bb5a-952">CC001</span></span></th>
<th><span data-ttu-id="6bb5a-953">CC002</span><span class="sxs-lookup"><span data-stu-id="6bb5a-953">CC002</span></span></th>
<th><span data-ttu-id="6bb5a-954">CC003</span><span class="sxs-lookup"><span data-stu-id="6bb5a-954">CC003</span></span></th>
<th><span data-ttu-id="6bb5a-955">CC004</span><span class="sxs-lookup"><span data-stu-id="6bb5a-955">CC004</span></span></th>
<th><span data-ttu-id="6bb5a-956">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-956">Proj 1</span></span></th>
<th><span data-ttu-id="6bb5a-957">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-957">Proj 2</span></span></th>
<th><span data-ttu-id="6bb5a-958">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="6bb5a-958">Prod 1</span></span></th>
<th><span data-ttu-id="6bb5a-959">Toode 2</span><span class="sxs-lookup"><span data-stu-id="6bb5a-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="6bb5a-960">10001 Elekter</span><span class="sxs-lookup"><span data-stu-id="6bb5a-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="6bb5a-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="6bb5a-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="6bb5a-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="6bb5a-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="6bb5a-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="6bb5a-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="6bb5a-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="6bb5a-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="6bb5a-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="6bb5a-970">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="6bb5a-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-971">0,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="6bb5a-972">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-973">0,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-974">0,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-975">0,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-976">0,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-977">0,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-978">776.36</span><span class="sxs-lookup"><span data-stu-id="6bb5a-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-979">223.64</span><span class="sxs-lookup"><span data-stu-id="6bb5a-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="6bb5a-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="6bb5a-981">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="6bb5a-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-982">000</span><span class="sxs-lookup"><span data-stu-id="6bb5a-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-983">0,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-984">0,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-985">0,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-986">0,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-987">30,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-988">10,00</span><span class="sxs-lookup"><span data-stu-id="6bb5a-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6bb5a-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6bb5a-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6bb5a-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="6bb5a-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6bb5a-992">Selles teemas selgitatakse, kuidas esmane kuluelement, 10001 Eleter, liigub läbi kuluobjektide.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="6bb5a-993">Seega eraldatakse see üldkulu organisatsiooni madalaimale tasemele.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="6bb5a-994">Teisisõnu kannavad kulu madalaimal tasemel olevad kuluobjektid.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="6bb5a-995">Kui soovite saada kuluobjektide vahelisest kuluvoost visuaalset ülevaadet, saate kuluvoo visualiseerimiseks kasutada kulude kokkuvõtte poliitika reegleid.</span><span class="sxs-lookup"><span data-stu-id="6bb5a-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="6bb5a-996">Täpsemat teavet vt teemast [Kulude kokkuvõte](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="6bb5a-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>




