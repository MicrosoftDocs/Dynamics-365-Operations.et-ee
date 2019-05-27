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
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544051"
---
# <a name="overhead-calculation"></a><span data-ttu-id="88f84-103">Üldkulude arvutus</span><span class="sxs-lookup"><span data-stu-id="88f84-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88f84-104">Selles teemas kirjeldatakse tüüpilisi üldkulude arvutamise ja eraldamise protsesse.</span><span class="sxs-lookup"><span data-stu-id="88f84-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="88f84-105">Mõiste määratlus</span><span class="sxs-lookup"><span data-stu-id="88f84-105">Term definition</span></span>
---------------

<span data-ttu-id="88f84-106">Üldkulud on kulud, mis kaasnevad ettevõtte käitamisega, kuid mida ei saa seostada otseselt ühegi kindla äritegevuse, toote ega teenusega.</span><span class="sxs-lookup"><span data-stu-id="88f84-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="88f84-107">Üldkulud pakuvad kriitilist tuge kasumit andavate tegevuste loomisele.</span><span class="sxs-lookup"><span data-stu-id="88f84-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="88f84-108">Siin on mõned näited üldkuludest.</span><span class="sxs-lookup"><span data-stu-id="88f84-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="88f84-109">Üür</span><span class="sxs-lookup"><span data-stu-id="88f84-109">Rent</span></span>
-   <span data-ttu-id="88f84-110">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-110">Electricity</span></span>
-   <span data-ttu-id="88f84-111">Haldustasud</span><span class="sxs-lookup"><span data-stu-id="88f84-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="88f84-112">Üldkulude arvutuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="88f84-112">Overhead calculation overview</span></span>
<span data-ttu-id="88f84-113">Üldkulude arvutus käitab kuluarvutuse poliitikaid õiges järjekorras.</span><span class="sxs-lookup"><span data-stu-id="88f84-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="88f84-114">Saate käivitada üldkulude arvutuse sama rahandusperioodi kohta mitu korda, kui kuluarvestuse poliitikaid on muudetud või tuvastatud teatud tõrked.</span><span class="sxs-lookup"><span data-stu-id="88f84-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="88f84-115">Iga üldkulude arvutamise käitamine talletatakse ja see saab kordumatu versiooni-ID, mis võimaldab teil arvutuste erinevaid versioone võrrelda.</span><span class="sxs-lookup"><span data-stu-id="88f84-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="88f84-116">Ülekulude arvutusega loodud kulukirjed saavad aruandluskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="88f84-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="88f84-117">See aruandluskuupäev vastab arvutuses kasutatud rahandusperioodi lõppkuupäevale.</span><span class="sxs-lookup"><span data-stu-id="88f84-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="88f84-118">Kordumatu versiooni-ID koosneb järgmistest elementidest.</span><span class="sxs-lookup"><span data-stu-id="88f84-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="88f84-119">Versiooni tüüp</span><span class="sxs-lookup"><span data-stu-id="88f84-119">Version type</span></span>
-   <span data-ttu-id="88f84-120">Kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="88f84-120">Date and time</span></span>
-   <span data-ttu-id="88f84-121">Kuluarvestuse pearaamat</span><span class="sxs-lookup"><span data-stu-id="88f84-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="88f84-122">Finantsaasta</span><span class="sxs-lookup"><span data-stu-id="88f84-122">Fiscal year</span></span>
-   <span data-ttu-id="88f84-123">Rahandusperiood</span><span class="sxs-lookup"><span data-stu-id="88f84-123">Fiscal period</span></span>

<span data-ttu-id="88f84-124">Üldkulude arvutus käivitatakse versioonist sõltumatult.</span><span class="sxs-lookup"><span data-stu-id="88f84-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="88f84-125">Seetõttu saate arvutada eelarveversiooni enne tegelikku versiooni.</span><span class="sxs-lookup"><span data-stu-id="88f84-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="88f84-126">Üldkulude arvutus koosneb neljast etapist, nagu näha alltoodud joonisel.</span><span class="sxs-lookup"><span data-stu-id="88f84-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="88f84-127">Igas etapis luuakse töölehe päis, millel on töölehe kanded.</span><span class="sxs-lookup"><span data-stu-id="88f84-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="88f84-128">See töölehe päis säiiltab sisendandmeid iga arvutusetapi kohta.</span><span class="sxs-lookup"><span data-stu-id="88f84-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="88f84-129">Igale töölehe reale rakendatakse poliitikad ja reeglid ning väljundina luuakse kulukirjed.</span><span class="sxs-lookup"><span data-stu-id="88f84-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="88f84-130">Seega on teil alati olemas põhjalik ülevaade.</span><span class="sxs-lookup"><span data-stu-id="88f84-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="88f84-131">[![Üldkulude arvutus](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="88f84-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="88f84-132">Elektri üldkulude arvutamine ja eraldamine</span><span class="sxs-lookup"><span data-stu-id="88f84-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="88f84-133">Finantsaruandluses on mõned kulud, näiteks elekter, registreeritud põhisummana.</span><span class="sxs-lookup"><span data-stu-id="88f84-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="88f84-134">Seetõttu ei pakuta kuluarvestuseks üksikasjalikku juhtimisülevaadet.</span><span class="sxs-lookup"><span data-stu-id="88f84-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="88f84-135">Kuluarvestuses peavad kulud liikuma läbi organisatsiooniüksuste, et pakkuda korrektset juhtimisülevaadet kõigi organisatsiooniüksuste ja -tasemete kohta.</span><span class="sxs-lookup"><span data-stu-id="88f84-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="88f84-136">See voog peab põhinema tarbimise või õiglase hindamise täpsel kirjendamisel.</span><span class="sxs-lookup"><span data-stu-id="88f84-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="88f84-137">Pearaamatus, saab elektrikulu sisestada nii, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="88f84-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88f84-138">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="88f84-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="88f84-139">Kulukeskus</span><span class="sxs-lookup"><span data-stu-id="88f84-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="88f84-140">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="88f84-140">Main account</span></span></th>
<th><span data-ttu-id="88f84-141">Summa arvestusvaluutas</span><span class="sxs-lookup"><span data-stu-id="88f84-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-142">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="88f84-143">CC099</span><span class="sxs-lookup"><span data-stu-id="88f84-143">CC099</span></span></td>
<td><span data-ttu-id="88f84-144">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="88f84-144">Default cost center</span></span></td>
<td><span data-ttu-id="88f84-145">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-145">10001</span></span></td>
<td><span data-ttu-id="88f84-146">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-146">Electricity</span></span></td>
<td><span data-ttu-id="88f84-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="88f84-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="88f84-148">1. etapp: kulukäitumise arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="88f84-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="88f84-149">Vaikimisi saavad lähteandmetest imporditud kulukirjed kuluarvestuses kulukäitumise klassifikatsiooniks **Klassifitseerimata**.</span><span class="sxs-lookup"><span data-stu-id="88f84-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="88f84-150">Kulukäitumise poliitikareegleid rakendades saate kulukirjed ümber klassifitseerida kui **Fikseeritud kulu** või **Muutuvkulu**.</span><span class="sxs-lookup"><span data-stu-id="88f84-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="88f84-151">Kulukäitumise reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="88f84-151">Define the cost behavior rule</span></span>

<span data-ttu-id="88f84-152">Mõnikord on osa kulust fikseeritud tasu ja järelejäänud kulu põhineb tarbimisel.</span><span class="sxs-lookup"><span data-stu-id="88f84-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="88f84-153">Elektriarved vastavad sageli sellele määratlusele.</span><span class="sxs-lookup"><span data-stu-id="88f84-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="88f84-154">Pärast kindla fikseeritud tasu maksmist maksate tarbimise eest kilovatt-tunni (Kwh) kohta.</span><span class="sxs-lookup"><span data-stu-id="88f84-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="88f84-155">Näiteks kui fikseeritud kulu tasu on 1000,00 eurot, määratletakse kulukäitumise reegel järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="88f84-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="88f84-156">Fikseeritud summa: 1000,00</span><span class="sxs-lookup"><span data-stu-id="88f84-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="88f84-157">0 &lt;= 1000,00 = fikseeritud</span><span class="sxs-lookup"><span data-stu-id="88f84-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="88f84-158">1000,01 &lt; N = muutuja</span><span class="sxs-lookup"><span data-stu-id="88f84-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="88f84-159">Tööleht</span><span class="sxs-lookup"><span data-stu-id="88f84-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88f84-160">Tööleht</span><span class="sxs-lookup"><span data-stu-id="88f84-160">Journal</span></span></th>
<th><span data-ttu-id="88f84-161">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="88f84-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="88f84-162">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="88f84-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="88f84-163">Versioon</span><span class="sxs-lookup"><span data-stu-id="88f84-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-164">00001</span><span class="sxs-lookup"><span data-stu-id="88f84-164">00001</span></span></td>
<td><span data-ttu-id="88f84-165">Kulukäitumise arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="88f84-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="88f84-166">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="88f84-166">Fiscal</span></span></td>
<td><span data-ttu-id="88f84-167">2017</span><span class="sxs-lookup"><span data-stu-id="88f84-167">2017</span></span></td>
<td><span data-ttu-id="88f84-168">Periood 1</span><span class="sxs-lookup"><span data-stu-id="88f84-168">Period 1</span></span></td>
<td><span data-ttu-id="88f84-169">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="88f84-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="88f84-170">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="88f84-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88f84-171">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="88f84-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="88f84-172">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="88f84-173">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="88f84-173">Cost element</span></span></th>
<th><span data-ttu-id="88f84-174">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="88f84-174">Cost behavior</span></span></th>
<th><span data-ttu-id="88f84-175">Summa</span><span class="sxs-lookup"><span data-stu-id="88f84-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-176">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="88f84-177">CC099</span><span class="sxs-lookup"><span data-stu-id="88f84-177">CC099</span></span></td>
<td><span data-ttu-id="88f84-178">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="88f84-178">Default cost center</span></span></td>
<td><span data-ttu-id="88f84-179">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-179">10001</span></span></td>
<td><span data-ttu-id="88f84-180">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-180">Electricity</span></span></td>
<td><span data-ttu-id="88f84-181">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="88f84-181">Unclassified</span></span></td>
<td><span data-ttu-id="88f84-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="88f84-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="88f84-183">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="88f84-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-184">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="88f84-185">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="88f84-185">Cost element</span></span></th>
<th><span data-ttu-id="88f84-186">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="88f84-186">Cost behavior</span></span></th>
<th><span data-ttu-id="88f84-187">Summa</span><span class="sxs-lookup"><span data-stu-id="88f84-187">Amount</span></span></th>
<th><span data-ttu-id="88f84-188">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="88f84-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-189">CC099</span><span class="sxs-lookup"><span data-stu-id="88f84-189">CC099</span></span></td>
<td><span data-ttu-id="88f84-190">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="88f84-190">Default cost center</span></span></td>
<td><span data-ttu-id="88f84-191">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-191">10001</span></span></td>
<td><span data-ttu-id="88f84-192">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-192">Electricity</span></span></td>
<td><span data-ttu-id="88f84-193">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="88f84-193">Unclassified</span></span></td>
<td><span data-ttu-id="88f84-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="88f84-194">10,000.00</span></span></td>
<td><span data-ttu-id="88f84-195">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-196">CC099</span><span class="sxs-lookup"><span data-stu-id="88f84-196">CC099</span></span></td>
<td><span data-ttu-id="88f84-197">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="88f84-197">Default cost center</span></span></td>
<td><span data-ttu-id="88f84-198">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-198">10001</span></span></td>
<td><span data-ttu-id="88f84-199">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-199">Electricity</span></span></td>
<td><span data-ttu-id="88f84-200">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="88f84-200">Unclassified</span></span></td>
<td><span data-ttu-id="88f84-201">–10 000,00</span><span class="sxs-lookup"><span data-stu-id="88f84-201">-10,000.00</span></span></td>
<td><span data-ttu-id="88f84-202">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-203">CC099</span><span class="sxs-lookup"><span data-stu-id="88f84-203">CC099</span></span></td>
<td><span data-ttu-id="88f84-204">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="88f84-204">Default cost center</span></span></td>
<td><span data-ttu-id="88f84-205">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-205">10001</span></span></td>
<td><span data-ttu-id="88f84-206">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-206">Electricity</span></span></td>
<td><span data-ttu-id="88f84-207">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-207">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="88f84-208">1,000.00</span></span></td>
<td><span data-ttu-id="88f84-209">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-210">CC099</span><span class="sxs-lookup"><span data-stu-id="88f84-210">CC099</span></span></td>
<td><span data-ttu-id="88f84-211">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="88f84-211">Default cost center</span></span></td>
<td><span data-ttu-id="88f84-212">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-212">10001</span></span></td>
<td><span data-ttu-id="88f84-213">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-213">Electricity</span></span></td>
<td><span data-ttu-id="88f84-214">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-214">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="88f84-215">9,000.00</span></span></td>
<td><span data-ttu-id="88f84-216">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88f84-217">Lisateavet vt teemast [Kulukäitumise poliitika loomine ja määramine kulujuhtimisüksusele (tegevuse juhis)](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="88f84-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="88f84-218">2. etapp: kulujaotuse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="88f84-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="88f84-219">Kulujaotust kasutatakse kulu ümberjaotamiseks ühelt kuluobjektilt ühele või mitmele teisele kuluobjektile, rakendades asjakohast eraldusalust.</span><span class="sxs-lookup"><span data-stu-id="88f84-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="88f84-220">Kulujaotus ja kulueraldus erinevad selle poolest, et kulujaotus toimub alati algse kulu esmase kuluelemendi tasemel.</span><span class="sxs-lookup"><span data-stu-id="88f84-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="88f84-221">Kulujaotuse reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="88f84-221">Define the cost distribution rule</span></span>

<span data-ttu-id="88f84-222">Finantsaruandluses registreeritakse elektrikulud sageli põhisummana.</span><span class="sxs-lookup"><span data-stu-id="88f84-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="88f84-223">Kuluarvestuseses ei ole see lähenemine piisavalt üksikasjalik.</span><span class="sxs-lookup"><span data-stu-id="88f84-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="88f84-224">Muutuvkulu tuleb jaotada üksikutele kuluobjektidele õigluse alusel.</span><span class="sxs-lookup"><span data-stu-id="88f84-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="88f84-225">Kõige loogilisem eraldamisalus on elektritarbimine (kWh).</span><span class="sxs-lookup"><span data-stu-id="88f84-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="88f84-226">Luuakse statistilise dimensiooni liige nimega Elekter ja elektritarbimine on kirjendatakse.</span><span class="sxs-lookup"><span data-stu-id="88f84-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="88f84-227">Vaikimisi muutuvad kõik statistilise dimensiooni liikmed eraldamisalusena kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="88f84-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-228">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-228">Cost object</span></span></th>
<th><span data-ttu-id="88f84-229">kWh</span><span class="sxs-lookup"><span data-stu-id="88f84-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-230">CC001</span><span class="sxs-lookup"><span data-stu-id="88f84-230">CC001</span></span></td>
<td><span data-ttu-id="88f84-231">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="88f84-231">HR</span></span></td>
<td><span data-ttu-id="88f84-232">1000</span><span class="sxs-lookup"><span data-stu-id="88f84-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-233">CC002</span><span class="sxs-lookup"><span data-stu-id="88f84-233">CC002</span></span></td>
<td><span data-ttu-id="88f84-234">Finantsid</span><span class="sxs-lookup"><span data-stu-id="88f84-234">Finance</span></span></td>
<td><span data-ttu-id="88f84-235">6,000</span><span class="sxs-lookup"><span data-stu-id="88f84-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-236">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-236">CC003</span></span></td>
<td><span data-ttu-id="88f84-237">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-237">Assembly</span></span></td>
<td><span data-ttu-id="88f84-238">0</span><span class="sxs-lookup"><span data-stu-id="88f84-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88f84-239">Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="88f84-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-240">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-240">Cost object</span></span></th>
<th><span data-ttu-id="88f84-241">Väärtus</span><span class="sxs-lookup"><span data-stu-id="88f84-241">Magnitude</span></span></th>
<th><span data-ttu-id="88f84-242">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="88f84-242">Allocation factor</span></span></th>
<th><span data-ttu-id="88f84-243">Summa</span><span class="sxs-lookup"><span data-stu-id="88f84-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-244">CC001</span><span class="sxs-lookup"><span data-stu-id="88f84-244">CC001</span></span></td>
<td><span data-ttu-id="88f84-245">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="88f84-245">HR</span></span></td>
<td><span data-ttu-id="88f84-246">1000</span><span class="sxs-lookup"><span data-stu-id="88f84-246">1,000</span></span></td>
<td><span data-ttu-id="88f84-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="88f84-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="88f84-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="88f84-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-249">CC002</span><span class="sxs-lookup"><span data-stu-id="88f84-249">CC002</span></span></td>
<td><span data-ttu-id="88f84-250">Finantsid</span><span class="sxs-lookup"><span data-stu-id="88f84-250">Finance</span></span></td>
<td><span data-ttu-id="88f84-251">6,000</span><span class="sxs-lookup"><span data-stu-id="88f84-251">6,000</span></span></td>
<td><span data-ttu-id="88f84-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="88f84-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="88f84-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="88f84-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-254">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-254">CC003</span></span></td>
<td><span data-ttu-id="88f84-255">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-255">Assembly</span></span></td>
<td><span data-ttu-id="88f84-256">0</span><span class="sxs-lookup"><span data-stu-id="88f84-256">0</span></span></td>
<td><span data-ttu-id="88f84-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="88f84-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="88f84-258">0,00</span><span class="sxs-lookup"><span data-stu-id="88f84-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88f84-259">Fikseeritud kulu tuleb jaotada ühtlaselt üksikutele kuluobjektidele, mis on tarbinud elektrit.</span><span class="sxs-lookup"><span data-stu-id="88f84-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="88f84-260">Selle tulemuse saate, kasutades valemi eraldamisaluses statistilise dimensiooni liiget Elekter: (Elekter &gt; 0,00). Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="88f84-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-261">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-261">Cost object</span></span></th>
<th><span data-ttu-id="88f84-262">Valem</span><span class="sxs-lookup"><span data-stu-id="88f84-262">Formula</span></span></th>
<th><span data-ttu-id="88f84-263">Väärtus</span><span class="sxs-lookup"><span data-stu-id="88f84-263">Magnitude</span></span></th>
<th><span data-ttu-id="88f84-264">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="88f84-264">Allocation factor</span></span></th>
<th><span data-ttu-id="88f84-265">Summa</span><span class="sxs-lookup"><span data-stu-id="88f84-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-266">CC001</span><span class="sxs-lookup"><span data-stu-id="88f84-266">CC001</span></span></td>
<td><span data-ttu-id="88f84-267">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="88f84-267">HR</span></span></td>
<td><span data-ttu-id="88f84-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="88f84-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="88f84-269">1</span><span class="sxs-lookup"><span data-stu-id="88f84-269">1</span></span></td>
<td><span data-ttu-id="88f84-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="88f84-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="88f84-271">500,00</span><span class="sxs-lookup"><span data-stu-id="88f84-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-272">CC002</span><span class="sxs-lookup"><span data-stu-id="88f84-272">CC002</span></span></td>
<td><span data-ttu-id="88f84-273">Finantsid</span><span class="sxs-lookup"><span data-stu-id="88f84-273">Finance</span></span></td>
<td><span data-ttu-id="88f84-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="88f84-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="88f84-275">1</span><span class="sxs-lookup"><span data-stu-id="88f84-275">1</span></span></td>
<td><span data-ttu-id="88f84-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="88f84-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="88f84-277">500,00</span><span class="sxs-lookup"><span data-stu-id="88f84-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-278">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-278">CC003</span></span></td>
<td><span data-ttu-id="88f84-279">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-279">Assembly</span></span></td>
<td><span data-ttu-id="88f84-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="88f84-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="88f84-281">0</span><span class="sxs-lookup"><span data-stu-id="88f84-281">0</span></span></td>
<td><span data-ttu-id="88f84-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="88f84-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="88f84-283">0,00</span><span class="sxs-lookup"><span data-stu-id="88f84-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="88f84-284">Tööleht</span><span class="sxs-lookup"><span data-stu-id="88f84-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88f84-285">Tööleht</span><span class="sxs-lookup"><span data-stu-id="88f84-285">Journal</span></span></th>
<th><span data-ttu-id="88f84-286">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="88f84-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="88f84-287">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="88f84-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="88f84-288">Versioon</span><span class="sxs-lookup"><span data-stu-id="88f84-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-289">00002</span><span class="sxs-lookup"><span data-stu-id="88f84-289">00002</span></span></td>
<td><span data-ttu-id="88f84-290">Kulujaotuse arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="88f84-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="88f84-291">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="88f84-291">Fiscal</span></span></td>
<td><span data-ttu-id="88f84-292">2017</span><span class="sxs-lookup"><span data-stu-id="88f84-292">2017</span></span></td>
<td><span data-ttu-id="88f84-293">Periood 1</span><span class="sxs-lookup"><span data-stu-id="88f84-293">Period 1</span></span></td>
<td><span data-ttu-id="88f84-294">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="88f84-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="88f84-295">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="88f84-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88f84-296">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="88f84-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="88f84-297">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="88f84-298">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="88f84-298">Cost element</span></span></th>
<th><span data-ttu-id="88f84-299">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="88f84-299">Cost behavior</span></span></th>
<th><span data-ttu-id="88f84-300">Summa</span><span class="sxs-lookup"><span data-stu-id="88f84-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-301">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="88f84-302">CC099</span><span class="sxs-lookup"><span data-stu-id="88f84-302">CC099</span></span></td>
<td><span data-ttu-id="88f84-303">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="88f84-303">Default cost center</span></span></td>
<td><span data-ttu-id="88f84-304">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-304">10001</span></span></td>
<td><span data-ttu-id="88f84-305">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-305">Electricity</span></span></td>
<td><span data-ttu-id="88f84-306">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-306">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="88f84-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-308">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="88f84-309">CC099</span><span class="sxs-lookup"><span data-stu-id="88f84-309">CC099</span></span></td>
<td><span data-ttu-id="88f84-310">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="88f84-310">Default cost center</span></span></td>
<td><span data-ttu-id="88f84-311">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-311">10001</span></span></td>
<td><span data-ttu-id="88f84-312">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-312">Electricity</span></span></td>
<td><span data-ttu-id="88f84-313">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-313">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="88f84-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="88f84-315">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="88f84-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-316">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="88f84-317">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="88f84-317">Cost element</span></span></th>
<th><span data-ttu-id="88f84-318">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="88f84-318">Cost behavior</span></span></th>
<th><span data-ttu-id="88f84-319">Summa</span><span class="sxs-lookup"><span data-stu-id="88f84-319">Amount</span></span></th>
<th><span data-ttu-id="88f84-320">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="88f84-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-321">CC099</span><span class="sxs-lookup"><span data-stu-id="88f84-321">CC099</span></span></td>
<td><span data-ttu-id="88f84-322">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="88f84-322">Default cost center</span></span></td>
<td><span data-ttu-id="88f84-323">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-323">10001</span></span></td>
<td><span data-ttu-id="88f84-324">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-324">Electricity</span></span></td>
<td><span data-ttu-id="88f84-325">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-325">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-326">–1000,00</span><span class="sxs-lookup"><span data-stu-id="88f84-326">-1,000.00</span></span></td>
<td><span data-ttu-id="88f84-327">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-328">CC001</span><span class="sxs-lookup"><span data-stu-id="88f84-328">CC001</span></span></td>
<td><span data-ttu-id="88f84-329">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="88f84-329">HR</span></span></td>
<td><span data-ttu-id="88f84-330">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-330">10001</span></span></td>
<td><span data-ttu-id="88f84-331">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-331">Electricity</span></span></td>
<td><span data-ttu-id="88f84-332">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-332">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-333">500,00</span><span class="sxs-lookup"><span data-stu-id="88f84-333">500.00</span></span></td>
<td><span data-ttu-id="88f84-334">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-335">CC002</span><span class="sxs-lookup"><span data-stu-id="88f84-335">CC002</span></span></td>
<td><span data-ttu-id="88f84-336">Finantsid</span><span class="sxs-lookup"><span data-stu-id="88f84-336">Finance</span></span></td>
<td><span data-ttu-id="88f84-337">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-337">10001</span></span></td>
<td><span data-ttu-id="88f84-338">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-338">Electricity</span></span></td>
<td><span data-ttu-id="88f84-339">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-339">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-340">500,00</span><span class="sxs-lookup"><span data-stu-id="88f84-340">500.00</span></span></td>
<td><span data-ttu-id="88f84-341">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-342">CC099</span><span class="sxs-lookup"><span data-stu-id="88f84-342">CC099</span></span></td>
<td><span data-ttu-id="88f84-343">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="88f84-343">Default cost center</span></span></td>
<td><span data-ttu-id="88f84-344">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-344">10001</span></span></td>
<td><span data-ttu-id="88f84-345">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-345">Electricity</span></span></td>
<td><span data-ttu-id="88f84-346">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-346">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-347">–9000,00</span><span class="sxs-lookup"><span data-stu-id="88f84-347">-9,000.00</span></span></td>
<td><span data-ttu-id="88f84-348">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-349">CC001</span><span class="sxs-lookup"><span data-stu-id="88f84-349">CC001</span></span></td>
<td><span data-ttu-id="88f84-350">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="88f84-350">HR</span></span></td>
<td><span data-ttu-id="88f84-351">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-351">10001</span></span></td>
<td><span data-ttu-id="88f84-352">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-352">Electricity</span></span></td>
<td><span data-ttu-id="88f84-353">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-353">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="88f84-354">1,285.71</span></span></td>
<td><span data-ttu-id="88f84-355">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-356">CC002</span><span class="sxs-lookup"><span data-stu-id="88f84-356">CC002</span></span></td>
<td><span data-ttu-id="88f84-357">Finantsid</span><span class="sxs-lookup"><span data-stu-id="88f84-357">Finance</span></span></td>
<td><span data-ttu-id="88f84-358">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-358">10001</span></span></td>
<td><span data-ttu-id="88f84-359">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-359">Electricity</span></span></td>
<td><span data-ttu-id="88f84-360">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-360">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="88f84-361">7,714.29</span></span></td>
<td><span data-ttu-id="88f84-362">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88f84-363">Lisateavet vt teemast [Kulujaotise poliitika loomine ja määramine kulujuhtimisüksusele (tegevuse juhis)](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="88f84-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="88f84-364">3. etapp: üldkulude määra arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="88f84-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="88f84-365">Üldkulude määra kasutatakse ühe või mitme kindla kuluobjekti debiteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="88f84-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="88f84-366">Tasu põhineb eelmääratud kulumääral ja väärtusel määratud eraldamisalusest.</span><span class="sxs-lookup"><span data-stu-id="88f84-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="88f84-367">Üldkulu määra määratlemine</span><span class="sxs-lookup"><span data-stu-id="88f84-367">Define the overhead rate</span></span>

<span data-ttu-id="88f84-368">Kuluobjekt CC001 inimressursid panustab sisemiste projektide kogumisse.</span><span class="sxs-lookup"><span data-stu-id="88f84-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="88f84-369">Luuakse statistilise dimensiooni liige nimega Inimressursside projektid, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="88f84-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-370">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-370">Cost object</span></span></th>
<th><span data-ttu-id="88f84-371">Tunnid</span><span class="sxs-lookup"><span data-stu-id="88f84-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-372">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="88f84-372">Proj 1</span></span></td>
<td><span data-ttu-id="88f84-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="88f84-373">Project 1</span></span></td>
<td><span data-ttu-id="88f84-374">3</span><span class="sxs-lookup"><span data-stu-id="88f84-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-375">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="88f84-375">Proj 2</span></span></td>
<td><span data-ttu-id="88f84-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="88f84-376">Project 2</span></span></td>
<td><span data-ttu-id="88f84-377">1</span><span class="sxs-lookup"><span data-stu-id="88f84-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88f84-378">Määratletud on eelmääratud kulumäär kuluprojektide panusele.</span><span class="sxs-lookup"><span data-stu-id="88f84-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-379">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-379">Cost object</span></span></th>
<th><span data-ttu-id="88f84-380">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="88f84-380">Cost element</span></span></th>
<th><span data-ttu-id="88f84-381">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="88f84-381">Cost behavior</span></span></th>
<th><span data-ttu-id="88f84-382">Ühikud</span><span class="sxs-lookup"><span data-stu-id="88f84-382">Units</span></span></th>
<th><span data-ttu-id="88f84-383">Kurss</span><span class="sxs-lookup"><span data-stu-id="88f84-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-384">CC001</span><span class="sxs-lookup"><span data-stu-id="88f84-384">CC001</span></span></td>
<td><span data-ttu-id="88f84-385">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="88f84-385">HR</span></span></td>
<td><span data-ttu-id="88f84-386">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-386">10001</span></span></td>
<td><span data-ttu-id="88f84-387">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-387">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-388">1</span><span class="sxs-lookup"><span data-stu-id="88f84-388">1</span></span></td>
<td><span data-ttu-id="88f84-389">10</span><span class="sxs-lookup"><span data-stu-id="88f84-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88f84-390">Järgmises tabelis on näidatud tulemus, kui inimressursside projektid on rakendatud eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="88f84-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-391">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-391">Cost object</span></span></th>
<th><span data-ttu-id="88f84-392">Väärtus</span><span class="sxs-lookup"><span data-stu-id="88f84-392">Magnitude</span></span></th>
<th><span data-ttu-id="88f84-393">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="88f84-393">Cost element</span></span></th>
<th><span data-ttu-id="88f84-394">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="88f84-394">Allocation factor</span></span></th>
<th><span data-ttu-id="88f84-395">Summa</span><span class="sxs-lookup"><span data-stu-id="88f84-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-396">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="88f84-396">Proj 1</span></span></td>
<td><span data-ttu-id="88f84-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="88f84-397">Project 1</span></span></td>
<td><span data-ttu-id="88f84-398">3</span><span class="sxs-lookup"><span data-stu-id="88f84-398">3</span></span></td>
<td><span data-ttu-id="88f84-399">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-399">10001</span></span></td>
<td><span data-ttu-id="88f84-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="88f84-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="88f84-401">30,00</span><span class="sxs-lookup"><span data-stu-id="88f84-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-402">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="88f84-402">Proj 2</span></span></td>
<td><span data-ttu-id="88f84-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="88f84-403">Project 2</span></span></td>
<td><span data-ttu-id="88f84-404">1</span><span class="sxs-lookup"><span data-stu-id="88f84-404">1</span></span></td>
<td><span data-ttu-id="88f84-405">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-405">10001</span></span></td>
<td><span data-ttu-id="88f84-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="88f84-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="88f84-407">10,00</span><span class="sxs-lookup"><span data-stu-id="88f84-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="88f84-408">Tööleht</span><span class="sxs-lookup"><span data-stu-id="88f84-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88f84-409">Tööleht</span><span class="sxs-lookup"><span data-stu-id="88f84-409">Journal</span></span></th>
<th><span data-ttu-id="88f84-410">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="88f84-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="88f84-411">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="88f84-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="88f84-412">Versioon</span><span class="sxs-lookup"><span data-stu-id="88f84-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-413">00003</span><span class="sxs-lookup"><span data-stu-id="88f84-413">00003</span></span></td>
<td><span data-ttu-id="88f84-414">Üldkulu määra arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="88f84-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="88f84-415">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="88f84-415">Fiscal</span></span></td>
<td><span data-ttu-id="88f84-416">2017</span><span class="sxs-lookup"><span data-stu-id="88f84-416">2017</span></span></td>
<td><span data-ttu-id="88f84-417">Periood 1</span><span class="sxs-lookup"><span data-stu-id="88f84-417">Period 1</span></span></td>
<td><span data-ttu-id="88f84-418">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="88f84-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="88f84-419">Töölehe sisestused (töölehe sisestused üldkulu määra arvutamiseks)</span><span class="sxs-lookup"><span data-stu-id="88f84-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88f84-420">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="88f84-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="88f84-421">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-421">Cost object</span></span></th>
<th><span data-ttu-id="88f84-422">Väärtus</span><span class="sxs-lookup"><span data-stu-id="88f84-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-423">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="88f84-424">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="88f84-424">Proj 1</span></span></td>
<td><span data-ttu-id="88f84-425">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="88f84-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="88f84-426">3,00</span><span class="sxs-lookup"><span data-stu-id="88f84-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-427">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="88f84-428">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="88f84-428">Proj 2</span></span></td>
<td><span data-ttu-id="88f84-429">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="88f84-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="88f84-430">1,00</span><span class="sxs-lookup"><span data-stu-id="88f84-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="88f84-431">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="88f84-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-432">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="88f84-433">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="88f84-433">Cost element</span></span></th>
<th><span data-ttu-id="88f84-434">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="88f84-434">Cost behavior</span></span></th>
<th><span data-ttu-id="88f84-435">Summa</span><span class="sxs-lookup"><span data-stu-id="88f84-435">Amount</span></span></th>
<th><span data-ttu-id="88f84-436">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="88f84-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="88f84-437">CC0001</span></span></td>
<td><span data-ttu-id="88f84-438">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="88f84-438">HR</span></span></td>
<td><span data-ttu-id="88f84-439">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-439">10001</span></span></td>
<td><span data-ttu-id="88f84-440">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-440">Electricity</span></span></td>
<td><span data-ttu-id="88f84-441">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-441">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-442">–30,00</span><span class="sxs-lookup"><span data-stu-id="88f84-442">-30.00</span></span></td>
<td><span data-ttu-id="88f84-443">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-444">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="88f84-444">Proj 1</span></span></td>
<td><span data-ttu-id="88f84-445">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="88f84-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="88f84-446">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-446">10001</span></span></td>
<td><span data-ttu-id="88f84-447">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-447">Electricity</span></span></td>
<td><span data-ttu-id="88f84-448">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-448">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-449">30,00</span><span class="sxs-lookup"><span data-stu-id="88f84-449">30.00</span></span></td>
<td><span data-ttu-id="88f84-450">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-451">CC001</span><span class="sxs-lookup"><span data-stu-id="88f84-451">CC001</span></span></td>
<td><span data-ttu-id="88f84-452">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="88f84-452">HR</span></span></td>
<td><span data-ttu-id="88f84-453">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-453">10001</span></span></td>
<td><span data-ttu-id="88f84-454">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-454">Electricity</span></span></td>
<td><span data-ttu-id="88f84-455">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-455">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="88f84-456">-10.00</span></span></td>
<td><span data-ttu-id="88f84-457">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-458">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="88f84-458">Proj 2</span></span></td>
<td><span data-ttu-id="88f84-459">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="88f84-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="88f84-460">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-460">10001</span></span></td>
<td><span data-ttu-id="88f84-461">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-461">Electricity</span></span></td>
<td><span data-ttu-id="88f84-462">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-462">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-463">10.00</span><span class="sxs-lookup"><span data-stu-id="88f84-463">10.00</span></span></td>
<td><span data-ttu-id="88f84-464">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88f84-465">Lisateavet vt teemast [Üldkulude arvutamine](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="88f84-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="88f84-466">4. etapp: kulueralduse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="88f84-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="88f84-467">Eraldamist kasutatakse kuluobjekti saldo eraldamiseks teistele kuluobjektidele, rakendades eraldamisalust.</span><span class="sxs-lookup"><span data-stu-id="88f84-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="88f84-468">Finance and Operations toetab vastastikuse eraldamise meetodit.</span><span class="sxs-lookup"><span data-stu-id="88f84-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="88f84-469">Vastastikuse eraldamise meetodi puhul tuvastatakse täiendavate kuluobjektide vahetatavad vastastikused teenused.</span><span class="sxs-lookup"><span data-stu-id="88f84-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="88f84-470">Süsteem määrab automaatselt eraldamiste tegemise õige järjekorra.</span><span class="sxs-lookup"><span data-stu-id="88f84-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="88f84-471">Kuluobjekti saldo eraldatakse üksiku eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="88f84-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="88f84-472">Toetatakse eraldamisi kuluobjektide dimensioonide ja nende vastavate liikmete seas.</span><span class="sxs-lookup"><span data-stu-id="88f84-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="88f84-473">Eraldamisjärjekorda reguleerib kulujuhtseade.</span><span class="sxs-lookup"><span data-stu-id="88f84-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="88f84-474">[![Vastastikune meetod](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="88f84-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="88f84-475">Kulueraldamise määratlemine</span><span class="sxs-lookup"><span data-stu-id="88f84-475">Define the cost allocation</span></span>

<span data-ttu-id="88f84-476">Siin on lihtne näide, mis selgitab, kuidas jälgida kulu liikumist.</span><span class="sxs-lookup"><span data-stu-id="88f84-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="88f84-477">Kuluobjekt CC001 inimressursid panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="88f84-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="88f84-478">Luuakse statistilise dimensiooni liige nimega Inimressursside teenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="88f84-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-479">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-479">Cost object</span></span></th>
<th><span data-ttu-id="88f84-480">Inimressursside teenused</span><span class="sxs-lookup"><span data-stu-id="88f84-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-481">CC002</span><span class="sxs-lookup"><span data-stu-id="88f84-481">CC002</span></span></td>
<td><span data-ttu-id="88f84-482">Finantsid</span><span class="sxs-lookup"><span data-stu-id="88f84-482">Finance</span></span></td>
<td><span data-ttu-id="88f84-483">35</span><span class="sxs-lookup"><span data-stu-id="88f84-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-484">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-484">CC003</span></span></td>
<td><span data-ttu-id="88f84-485">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-485">Assembly</span></span></td>
<td><span data-ttu-id="88f84-486">55</span><span class="sxs-lookup"><span data-stu-id="88f84-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-487">CC004</span><span class="sxs-lookup"><span data-stu-id="88f84-487">CC004</span></span></td>
<td><span data-ttu-id="88f84-488">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="88f84-488">Packaging</span></span></td>
<td><span data-ttu-id="88f84-489">10</span><span class="sxs-lookup"><span data-stu-id="88f84-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88f84-490">Kuluobjekt CC002 rahandus panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="88f84-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="88f84-491">Luuakse statistilise dimensiooni liige nimega Rahandusteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="88f84-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-492">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-492">Cost object</span></span></th>
<th><span data-ttu-id="88f84-493">Rahandusteenused</span><span class="sxs-lookup"><span data-stu-id="88f84-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-494">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-494">CC003</span></span></td>
<td><span data-ttu-id="88f84-495">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-495">Assembly</span></span></td>
<td><span data-ttu-id="88f84-496">65</span><span class="sxs-lookup"><span data-stu-id="88f84-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-497">CC004</span><span class="sxs-lookup"><span data-stu-id="88f84-497">CC004</span></span></td>
<td><span data-ttu-id="88f84-498">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="88f84-498">Packaging</span></span></td>
<td><span data-ttu-id="88f84-499">35</span><span class="sxs-lookup"><span data-stu-id="88f84-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88f84-500">Kuluobjekt CC003 assembler panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="88f84-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="88f84-501">Luuakse statistilise dimensiooni liige nimega Assembleriteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="88f84-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-502">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-502">Cost object</span></span></th>
<th><span data-ttu-id="88f84-503">Assembleriteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="88f84-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-504">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="88f84-504">Prod 1</span></span></td>
<td><span data-ttu-id="88f84-505">Toode 1</span><span class="sxs-lookup"><span data-stu-id="88f84-505">Product 1</span></span></td>
<td><span data-ttu-id="88f84-506">60</span><span class="sxs-lookup"><span data-stu-id="88f84-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-507">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-507">Prod 2</span></span></td>
<td><span data-ttu-id="88f84-508">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-508">Product 2</span></span></td>
<td><span data-ttu-id="88f84-509">20</span><span class="sxs-lookup"><span data-stu-id="88f84-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88f84-510">Kuluobjekt CC004 pakendamine panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="88f84-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="88f84-511">Luuakse statistilise dimensiooni liige nimega Pakendamisteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="88f84-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-512">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-512">Cost object</span></span></th>
<th><span data-ttu-id="88f84-513">Pakendamisteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="88f84-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-514">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="88f84-514">Prod 1</span></span></td>
<td><span data-ttu-id="88f84-515">Toode 1</span><span class="sxs-lookup"><span data-stu-id="88f84-515">Product 1</span></span></td>
<td><span data-ttu-id="88f84-516">80</span><span class="sxs-lookup"><span data-stu-id="88f84-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-517">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-517">Prod 2</span></span></td>
<td><span data-ttu-id="88f84-518">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-518">Product 2</span></span></td>
<td><span data-ttu-id="88f84-519">sept.</span><span class="sxs-lookup"><span data-stu-id="88f84-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="88f84-520">Finance and Operationsis saab statistilised mõõdud, nagu toote tarbitud tootmistunnid, tuletada lähteandmetest.</span><span class="sxs-lookup"><span data-stu-id="88f84-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="88f84-521">Lisateavet vt teemast [Statistiliste mõõtude pakkuja mall](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="88f84-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="88f84-522">Järgmises tabelis on näidatud tulemus, kui HR-teenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="88f84-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-523">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-523">Cost object</span></span></th>
<th><span data-ttu-id="88f84-524">Väärtus</span><span class="sxs-lookup"><span data-stu-id="88f84-524">Magnitude</span></span></th>
<th><span data-ttu-id="88f84-525">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="88f84-525">Allocation factor</span></span></th>
<th><span data-ttu-id="88f84-526">Summa</span><span class="sxs-lookup"><span data-stu-id="88f84-526">Amount</span></span></th>
<th><span data-ttu-id="88f84-527">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="88f84-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-528">CC002</span><span class="sxs-lookup"><span data-stu-id="88f84-528">CC002</span></span></td>
<td><span data-ttu-id="88f84-529">Finantsid</span><span class="sxs-lookup"><span data-stu-id="88f84-529">Finance</span></span></td>
<td><span data-ttu-id="88f84-530">35</span><span class="sxs-lookup"><span data-stu-id="88f84-530">35</span></span></td>
<td><span data-ttu-id="88f84-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="88f84-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="88f84-532">175.00</span><span class="sxs-lookup"><span data-stu-id="88f84-532">175.00</span></span></td>
<td><span data-ttu-id="88f84-533">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-534">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-534">CC003</span></span></td>
<td><span data-ttu-id="88f84-535">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-535">Assembly</span></span></td>
<td><span data-ttu-id="88f84-536">55</span><span class="sxs-lookup"><span data-stu-id="88f84-536">55</span></span></td>
<td><span data-ttu-id="88f84-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="88f84-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="88f84-538">275.00</span><span class="sxs-lookup"><span data-stu-id="88f84-538">275.00</span></span></td>
<td><span data-ttu-id="88f84-539">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-540">CC004</span><span class="sxs-lookup"><span data-stu-id="88f84-540">CC004</span></span></td>
<td><span data-ttu-id="88f84-541">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="88f84-541">Packaging</span></span></td>
<td><span data-ttu-id="88f84-542">10</span><span class="sxs-lookup"><span data-stu-id="88f84-542">10</span></span></td>
<td><span data-ttu-id="88f84-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="88f84-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="88f84-544">50,00</span><span class="sxs-lookup"><span data-stu-id="88f84-544">50.00</span></span></td>
<td><span data-ttu-id="88f84-545">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-546">CC002</span><span class="sxs-lookup"><span data-stu-id="88f84-546">CC002</span></span></td>
<td><span data-ttu-id="88f84-547">Finantsid</span><span class="sxs-lookup"><span data-stu-id="88f84-547">Finance</span></span></td>
<td><span data-ttu-id="88f84-548">35</span><span class="sxs-lookup"><span data-stu-id="88f84-548">35</span></span></td>
<td><span data-ttu-id="88f84-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="88f84-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="88f84-550">436.00</span><span class="sxs-lookup"><span data-stu-id="88f84-550">436.00</span></span></td>
<td><span data-ttu-id="88f84-551">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-552">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-552">CC003</span></span></td>
<td><span data-ttu-id="88f84-553">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-553">Assembly</span></span></td>
<td><span data-ttu-id="88f84-554">55</span><span class="sxs-lookup"><span data-stu-id="88f84-554">55</span></span></td>
<td><span data-ttu-id="88f84-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="88f84-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="88f84-556">685.14</span><span class="sxs-lookup"><span data-stu-id="88f84-556">685.14</span></span></td>
<td><span data-ttu-id="88f84-557">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-558">CC004</span><span class="sxs-lookup"><span data-stu-id="88f84-558">CC004</span></span></td>
<td><span data-ttu-id="88f84-559">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="88f84-559">Packaging</span></span></td>
<td><span data-ttu-id="88f84-560">10</span><span class="sxs-lookup"><span data-stu-id="88f84-560">10</span></span></td>
<td><span data-ttu-id="88f84-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="88f84-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="88f84-562">124.57</span><span class="sxs-lookup"><span data-stu-id="88f84-562">124.57</span></span></td>
<td><span data-ttu-id="88f84-563">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88f84-564">Järgmises tabelis on näidatud tulemus, kui Rahandusteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="88f84-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-565">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-565">Cost object</span></span></th>
<th><span data-ttu-id="88f84-566">Väärtus</span><span class="sxs-lookup"><span data-stu-id="88f84-566">Magnitude</span></span></th>
<th><span data-ttu-id="88f84-567">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="88f84-567">Allocation factor</span></span></th>
<th><span data-ttu-id="88f84-568">Summa</span><span class="sxs-lookup"><span data-stu-id="88f84-568">Amount</span></span></th>
<th><span data-ttu-id="88f84-569">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="88f84-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-570">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-570">CC003</span></span></td>
<td><span data-ttu-id="88f84-571">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-571">Assembly</span></span></td>
<td><span data-ttu-id="88f84-572">65</span><span class="sxs-lookup"><span data-stu-id="88f84-572">65</span></span></td>
<td><span data-ttu-id="88f84-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="88f84-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="88f84-574">438.75</span><span class="sxs-lookup"><span data-stu-id="88f84-574">438.75</span></span></td>
<td><span data-ttu-id="88f84-575">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-576">CC004</span><span class="sxs-lookup"><span data-stu-id="88f84-576">CC004</span></span></td>
<td><span data-ttu-id="88f84-577">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="88f84-577">Packaging</span></span></td>
<td><span data-ttu-id="88f84-578">35</span><span class="sxs-lookup"><span data-stu-id="88f84-578">35</span></span></td>
<td><span data-ttu-id="88f84-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="88f84-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="88f84-580">236.25</span><span class="sxs-lookup"><span data-stu-id="88f84-580">236.25</span></span></td>
<td><span data-ttu-id="88f84-581">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-582">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-582">CC003</span></span></td>
<td><span data-ttu-id="88f84-583">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-583">Assembly</span></span></td>
<td><span data-ttu-id="88f84-584">65</span><span class="sxs-lookup"><span data-stu-id="88f84-584">65</span></span></td>
<td><span data-ttu-id="88f84-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="88f84-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="88f84-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="88f84-586">5,297.69</span></span></td>
<td><span data-ttu-id="88f84-587">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-588">CC004</span><span class="sxs-lookup"><span data-stu-id="88f84-588">CC004</span></span></td>
<td><span data-ttu-id="88f84-589">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="88f84-589">Packaging</span></span></td>
<td><span data-ttu-id="88f84-590">35</span><span class="sxs-lookup"><span data-stu-id="88f84-590">35</span></span></td>
<td><span data-ttu-id="88f84-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="88f84-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="88f84-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="88f84-592">2,852.60</span></span></td>
<td><span data-ttu-id="88f84-593">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88f84-594">Järgmises tabelis on näidatud tulemus, kui Assembleriteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="88f84-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-595">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-595">Cost object</span></span></th>
<th><span data-ttu-id="88f84-596">Väärtus</span><span class="sxs-lookup"><span data-stu-id="88f84-596">Magnitude</span></span></th>
<th><span data-ttu-id="88f84-597">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="88f84-597">Allocation factor</span></span></th>
<th><span data-ttu-id="88f84-598">Summa</span><span class="sxs-lookup"><span data-stu-id="88f84-598">Amount</span></span></th>
<th><span data-ttu-id="88f84-599">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="88f84-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-600">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="88f84-600">Prod 1</span></span></td>
<td><span data-ttu-id="88f84-601">Toode 1</span><span class="sxs-lookup"><span data-stu-id="88f84-601">Product 1</span></span></td>
<td><span data-ttu-id="88f84-602">60</span><span class="sxs-lookup"><span data-stu-id="88f84-602">60</span></span></td>
<td><span data-ttu-id="88f84-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="88f84-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="88f84-604">535.31</span><span class="sxs-lookup"><span data-stu-id="88f84-604">535.31</span></span></td>
<td><span data-ttu-id="88f84-605">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-606">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-606">Prod 2</span></span></td>
<td><span data-ttu-id="88f84-607">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-607">Product 2</span></span></td>
<td><span data-ttu-id="88f84-608">20</span><span class="sxs-lookup"><span data-stu-id="88f84-608">20</span></span></td>
<td><span data-ttu-id="88f84-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="88f84-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="88f84-610">178.44</span><span class="sxs-lookup"><span data-stu-id="88f84-610">178.44</span></span></td>
<td><span data-ttu-id="88f84-611">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-612">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="88f84-612">Prod 1</span></span></td>
<td><span data-ttu-id="88f84-613">Toode 1</span><span class="sxs-lookup"><span data-stu-id="88f84-613">Product 1</span></span></td>
<td><span data-ttu-id="88f84-614">60</span><span class="sxs-lookup"><span data-stu-id="88f84-614">60</span></span></td>
<td><span data-ttu-id="88f84-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="88f84-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="88f84-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="88f84-616">4,487.12</span></span></td>
<td><span data-ttu-id="88f84-617">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-618">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-618">Prod 2</span></span></td>
<td><span data-ttu-id="88f84-619">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-619">Product 2</span></span></td>
<td><span data-ttu-id="88f84-620">20</span><span class="sxs-lookup"><span data-stu-id="88f84-620">20</span></span></td>
<td><span data-ttu-id="88f84-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="88f84-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="88f84-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="88f84-622">1,495.71</span></span></td>
<td><span data-ttu-id="88f84-623">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="88f84-624">Järgmises tabelis on näidatud tulemus, kui Pakendamisteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="88f84-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-625">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-625">Cost object</span></span></th>
<th><span data-ttu-id="88f84-626">Väärtus</span><span class="sxs-lookup"><span data-stu-id="88f84-626">Magnitude</span></span></th>
<th><span data-ttu-id="88f84-627">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="88f84-627">Allocation factor</span></span></th>
<th><span data-ttu-id="88f84-628">Summa</span><span class="sxs-lookup"><span data-stu-id="88f84-628">Amount</span></span></th>
<th><span data-ttu-id="88f84-629">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="88f84-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-630">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="88f84-630">Prod 1</span></span></td>
<td><span data-ttu-id="88f84-631">Toode 1</span><span class="sxs-lookup"><span data-stu-id="88f84-631">Product 1</span></span></td>
<td><span data-ttu-id="88f84-632">80</span><span class="sxs-lookup"><span data-stu-id="88f84-632">80</span></span></td>
<td><span data-ttu-id="88f84-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="88f84-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="88f84-634">241.05</span><span class="sxs-lookup"><span data-stu-id="88f84-634">241.05</span></span></td>
<td><span data-ttu-id="88f84-635">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-636">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-636">Prod 2</span></span></td>
<td><span data-ttu-id="88f84-637">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-637">Product 2</span></span></td>
<td><span data-ttu-id="88f84-638">15</span><span class="sxs-lookup"><span data-stu-id="88f84-638">15</span></span></td>
<td><span data-ttu-id="88f84-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="88f84-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="88f84-640">45.20</span><span class="sxs-lookup"><span data-stu-id="88f84-640">45.20</span></span></td>
<td><span data-ttu-id="88f84-641">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-642">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="88f84-642">Prod 1</span></span></td>
<td><span data-ttu-id="88f84-643">Toode 1</span><span class="sxs-lookup"><span data-stu-id="88f84-643">Product 1</span></span></td>
<td><span data-ttu-id="88f84-644">80</span><span class="sxs-lookup"><span data-stu-id="88f84-644">80</span></span></td>
<td><span data-ttu-id="88f84-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="88f84-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="88f84-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="88f84-646">2,507.09</span></span></td>
<td><span data-ttu-id="88f84-647">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-648">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-648">Prod 2</span></span></td>
<td><span data-ttu-id="88f84-649">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-649">Product 2</span></span></td>
<td><span data-ttu-id="88f84-650">15</span><span class="sxs-lookup"><span data-stu-id="88f84-650">15</span></span></td>
<td><span data-ttu-id="88f84-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="88f84-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="88f84-652">470.08</span><span class="sxs-lookup"><span data-stu-id="88f84-652">470.08</span></span></td>
<td><span data-ttu-id="88f84-653">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="88f84-654">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="88f84-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88f84-655">Tööleht</span><span class="sxs-lookup"><span data-stu-id="88f84-655">Journal</span></span></th>
<th><span data-ttu-id="88f84-656">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="88f84-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="88f84-657">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="88f84-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="88f84-658">Versioon</span><span class="sxs-lookup"><span data-stu-id="88f84-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-659">00004</span><span class="sxs-lookup"><span data-stu-id="88f84-659">00004</span></span></td>
<td><span data-ttu-id="88f84-660">Kulueralduse tööleht</span><span class="sxs-lookup"><span data-stu-id="88f84-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="88f84-661">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="88f84-661">Fiscal</span></span></td>
<td><span data-ttu-id="88f84-662">2017</span><span class="sxs-lookup"><span data-stu-id="88f84-662">2017</span></span></td>
<td><span data-ttu-id="88f84-663">Periood 1</span><span class="sxs-lookup"><span data-stu-id="88f84-663">Period 1</span></span></td>
<td><span data-ttu-id="88f84-664">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="88f84-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="88f84-665">Töölehe read</span><span class="sxs-lookup"><span data-stu-id="88f84-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="88f84-666">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="88f84-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="88f84-667">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="88f84-668">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="88f84-668">Cost element</span></span></th>
<th><span data-ttu-id="88f84-669">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="88f84-669">Cost behavior</span></span></th>
<th><span data-ttu-id="88f84-670">Summa</span><span class="sxs-lookup"><span data-stu-id="88f84-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-671">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="88f84-672">CC001</span><span class="sxs-lookup"><span data-stu-id="88f84-672">CC001</span></span></td>
<td><span data-ttu-id="88f84-673">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="88f84-673">HR</span></span></td>
<td><span data-ttu-id="88f84-674">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-674">10001</span></span></td>
<td><span data-ttu-id="88f84-675">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-675">Electricity</span></span></td>
<td><span data-ttu-id="88f84-676">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-676">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-677">500,00</span><span class="sxs-lookup"><span data-stu-id="88f84-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-678">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="88f84-679">CC001</span><span class="sxs-lookup"><span data-stu-id="88f84-679">CC001</span></span></td>
<td><span data-ttu-id="88f84-680">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="88f84-680">HR</span></span></td>
<td><span data-ttu-id="88f84-681">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-681">10001</span></span></td>
<td><span data-ttu-id="88f84-682">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-682">Electricity</span></span></td>
<td><span data-ttu-id="88f84-683">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-683">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="88f84-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-685">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="88f84-686">CC002</span><span class="sxs-lookup"><span data-stu-id="88f84-686">CC002</span></span></td>
<td><span data-ttu-id="88f84-687">Finantsid</span><span class="sxs-lookup"><span data-stu-id="88f84-687">Finance</span></span></td>
<td><span data-ttu-id="88f84-688">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-688">10001</span></span></td>
<td><span data-ttu-id="88f84-689">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-689">Electricity</span></span></td>
<td><span data-ttu-id="88f84-690">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-690">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-691">675.00</span><span class="sxs-lookup"><span data-stu-id="88f84-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-692">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="88f84-693">CC002</span><span class="sxs-lookup"><span data-stu-id="88f84-693">CC002</span></span></td>
<td><span data-ttu-id="88f84-694">Finantsid</span><span class="sxs-lookup"><span data-stu-id="88f84-694">Finance</span></span></td>
<td><span data-ttu-id="88f84-695">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-695">10001</span></span></td>
<td><span data-ttu-id="88f84-696">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-696">Electricity</span></span></td>
<td><span data-ttu-id="88f84-697">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-697">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="88f84-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-699">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="88f84-700">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-700">CC003</span></span></td>
<td><span data-ttu-id="88f84-701">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-701">Assembly</span></span></td>
<td><span data-ttu-id="88f84-702">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-702">10001</span></span></td>
<td><span data-ttu-id="88f84-703">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-703">Electricity</span></span></td>
<td><span data-ttu-id="88f84-704">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-704">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-705">713.75</span><span class="sxs-lookup"><span data-stu-id="88f84-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-706">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="88f84-707">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-707">CC003</span></span></td>
<td><span data-ttu-id="88f84-708">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-708">Assembly</span></span></td>
<td><span data-ttu-id="88f84-709">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-709">10001</span></span></td>
<td><span data-ttu-id="88f84-710">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-710">Electricity</span></span></td>
<td><span data-ttu-id="88f84-711">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-711">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="88f84-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-713">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="88f84-714">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-714">CC003</span></span></td>
<td><span data-ttu-id="88f84-715">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="88f84-715">Packaging</span></span></td>
<td><span data-ttu-id="88f84-716">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-716">10001</span></span></td>
<td><span data-ttu-id="88f84-717">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-717">Electricity</span></span></td>
<td><span data-ttu-id="88f84-718">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-718">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-719">286.25</span><span class="sxs-lookup"><span data-stu-id="88f84-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-720">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="88f84-721">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-721">CC003</span></span></td>
<td><span data-ttu-id="88f84-722">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="88f84-722">Packaging</span></span></td>
<td><span data-ttu-id="88f84-723">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-723">10001</span></span></td>
<td><span data-ttu-id="88f84-724">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-724">Electricity</span></span></td>
<td><span data-ttu-id="88f84-725">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-725">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="88f84-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-727">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="88f84-728">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="88f84-728">Prod 1</span></span></td>
<td><span data-ttu-id="88f84-729">Toode 1</span><span class="sxs-lookup"><span data-stu-id="88f84-729">Product 1</span></span></td>
<td><span data-ttu-id="88f84-730">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-730">10001</span></span></td>
<td><span data-ttu-id="88f84-731">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-731">Electricity</span></span></td>
<td><span data-ttu-id="88f84-732">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-732">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-733">776.36</span><span class="sxs-lookup"><span data-stu-id="88f84-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-734">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="88f84-735">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="88f84-735">Prod 1</span></span></td>
<td><span data-ttu-id="88f84-736">Toode 1</span><span class="sxs-lookup"><span data-stu-id="88f84-736">Product 1</span></span></td>
<td><span data-ttu-id="88f84-737">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-737">10001</span></span></td>
<td><span data-ttu-id="88f84-738">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-738">Electricity</span></span></td>
<td><span data-ttu-id="88f84-739">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-739">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="88f84-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-741">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="88f84-742">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-742">Prod 2</span></span></td>
<td><span data-ttu-id="88f84-743">Toode 1</span><span class="sxs-lookup"><span data-stu-id="88f84-743">Product 1</span></span></td>
<td><span data-ttu-id="88f84-744">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-744">10001</span></span></td>
<td><span data-ttu-id="88f84-745">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-745">Electricity</span></span></td>
<td><span data-ttu-id="88f84-746">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-746">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-747">223.64</span><span class="sxs-lookup"><span data-stu-id="88f84-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-748">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="88f84-749">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-749">Prod 2</span></span></td>
<td><span data-ttu-id="88f84-750">Toode 1</span><span class="sxs-lookup"><span data-stu-id="88f84-750">Product 1</span></span></td>
<td><span data-ttu-id="88f84-751">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-751">10001</span></span></td>
<td><span data-ttu-id="88f84-752">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-752">Electricity</span></span></td>
<td><span data-ttu-id="88f84-753">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-753">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="88f84-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="88f84-755">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="88f84-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="88f84-756">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="88f84-757">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="88f84-757">Cost element</span></span></th>
<th><span data-ttu-id="88f84-758">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="88f84-758">Cost behavior</span></span></th>
<th><span data-ttu-id="88f84-759">Summa</span><span class="sxs-lookup"><span data-stu-id="88f84-759">Amount</span></span></th>
<th><span data-ttu-id="88f84-760">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="88f84-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="88f84-761">CC001</span><span class="sxs-lookup"><span data-stu-id="88f84-761">CC001</span></span></td>
<td><span data-ttu-id="88f84-762">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="88f84-762">HR</span></span></td>
<td><span data-ttu-id="88f84-763">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-763">10001</span></span></td>
<td><span data-ttu-id="88f84-764">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-764">Electricity</span></span></td>
<td><span data-ttu-id="88f84-765">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-765">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-766">‑500,00</span><span class="sxs-lookup"><span data-stu-id="88f84-766">-500.00</span></span></td>
<td><span data-ttu-id="88f84-767">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-768">CC002</span><span class="sxs-lookup"><span data-stu-id="88f84-768">CC002</span></span></td>
<td><span data-ttu-id="88f84-769">Finantsid</span><span class="sxs-lookup"><span data-stu-id="88f84-769">Finance</span></span></td>
<td><span data-ttu-id="88f84-770">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-770">10001</span></span></td>
<td><span data-ttu-id="88f84-771">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-771">Electricity</span></span></td>
<td><span data-ttu-id="88f84-772">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-772">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-773">175.00</span><span class="sxs-lookup"><span data-stu-id="88f84-773">175.00</span></span></td>
<td><span data-ttu-id="88f84-774">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-775">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-775">CC003</span></span></td>
<td><span data-ttu-id="88f84-776">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-776">Assembly</span></span></td>
<td><span data-ttu-id="88f84-777">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-777">10001</span></span></td>
<td><span data-ttu-id="88f84-778">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-778">Electricity</span></span></td>
<td><span data-ttu-id="88f84-779">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-779">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-780">275.00</span><span class="sxs-lookup"><span data-stu-id="88f84-780">275.00</span></span></td>
<td><span data-ttu-id="88f84-781">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-782">CC004</span><span class="sxs-lookup"><span data-stu-id="88f84-782">CC004</span></span></td>
<td><span data-ttu-id="88f84-783">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="88f84-783">Packaging</span></span></td>
<td><span data-ttu-id="88f84-784">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-784">10001</span></span></td>
<td><span data-ttu-id="88f84-785">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-785">Electricity</span></span></td>
<td><span data-ttu-id="88f84-786">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-786">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-787">50,00</span><span class="sxs-lookup"><span data-stu-id="88f84-787">50,00</span></span></td>
<td><span data-ttu-id="88f84-788">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-789">CC001</span><span class="sxs-lookup"><span data-stu-id="88f84-789">CC001</span></span></td>
<td><span data-ttu-id="88f84-790">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="88f84-790">HR</span></span></td>
<td><span data-ttu-id="88f84-791">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-791">10001</span></span></td>
<td><span data-ttu-id="88f84-792">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-792">Electricity</span></span></td>
<td><span data-ttu-id="88f84-793">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-793">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-794">–1245,71</span><span class="sxs-lookup"><span data-stu-id="88f84-794">-1,245.71</span></span></td>
<td><span data-ttu-id="88f84-795">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-796">CC002</span><span class="sxs-lookup"><span data-stu-id="88f84-796">CC002</span></span></td>
<td><span data-ttu-id="88f84-797">Finantsid</span><span class="sxs-lookup"><span data-stu-id="88f84-797">Finance</span></span></td>
<td><span data-ttu-id="88f84-798">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-798">10001</span></span></td>
<td><span data-ttu-id="88f84-799">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-799">Electricity</span></span></td>
<td><span data-ttu-id="88f84-800">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-800">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-801">436.00</span><span class="sxs-lookup"><span data-stu-id="88f84-801">436.00</span></span></td>
<td><span data-ttu-id="88f84-802">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-803">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-803">CC003</span></span></td>
<td><span data-ttu-id="88f84-804">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-804">Assembly</span></span></td>
<td><span data-ttu-id="88f84-805">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-805">10001</span></span></td>
<td><span data-ttu-id="88f84-806">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-806">Electricity</span></span></td>
<td><span data-ttu-id="88f84-807">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-807">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-808">685.14</span><span class="sxs-lookup"><span data-stu-id="88f84-808">685.14</span></span></td>
<td><span data-ttu-id="88f84-809">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-810">CC004</span><span class="sxs-lookup"><span data-stu-id="88f84-810">CC004</span></span></td>
<td><span data-ttu-id="88f84-811">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="88f84-811">Packaging</span></span></td>
<td><span data-ttu-id="88f84-812">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-812">10001</span></span></td>
<td><span data-ttu-id="88f84-813">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-813">Electricity</span></span></td>
<td><span data-ttu-id="88f84-814">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-814">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-815">124.57</span><span class="sxs-lookup"><span data-stu-id="88f84-815">124.57</span></span></td>
<td><span data-ttu-id="88f84-816">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-817">CC002</span><span class="sxs-lookup"><span data-stu-id="88f84-817">CC002</span></span></td>
<td><span data-ttu-id="88f84-818">Finantsid</span><span class="sxs-lookup"><span data-stu-id="88f84-818">Finance</span></span></td>
<td><span data-ttu-id="88f84-819">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-819">10001</span></span></td>
<td><span data-ttu-id="88f84-820">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-820">Electricity</span></span></td>
<td><span data-ttu-id="88f84-821">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-821">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-822">–675,00</span><span class="sxs-lookup"><span data-stu-id="88f84-822">-675.00</span></span></td>
<td><span data-ttu-id="88f84-823">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-824">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-824">CC003</span></span></td>
<td><span data-ttu-id="88f84-825">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-825">Assembly</span></span></td>
<td><span data-ttu-id="88f84-826">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-826">10001</span></span></td>
<td><span data-ttu-id="88f84-827">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-827">Electricity</span></span></td>
<td><span data-ttu-id="88f84-828">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-828">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-829">438.75</span><span class="sxs-lookup"><span data-stu-id="88f84-829">438.75</span></span></td>
<td><span data-ttu-id="88f84-830">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-831">CC004</span><span class="sxs-lookup"><span data-stu-id="88f84-831">CC004</span></span></td>
<td><span data-ttu-id="88f84-832">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="88f84-832">Packaging</span></span></td>
<td><span data-ttu-id="88f84-833">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-833">10001</span></span></td>
<td><span data-ttu-id="88f84-834">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-834">Electricity</span></span></td>
<td><span data-ttu-id="88f84-835">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-835">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-836">236.25</span><span class="sxs-lookup"><span data-stu-id="88f84-836">236.25</span></span></td>
<td><span data-ttu-id="88f84-837">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-838">CC002</span><span class="sxs-lookup"><span data-stu-id="88f84-838">CC002</span></span></td>
<td><span data-ttu-id="88f84-839">Finantsid</span><span class="sxs-lookup"><span data-stu-id="88f84-839">Finance</span></span></td>
<td><span data-ttu-id="88f84-840">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-840">10001</span></span></td>
<td><span data-ttu-id="88f84-841">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-841">Electricity</span></span></td>
<td><span data-ttu-id="88f84-842">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-842">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-843">–8150,29</span><span class="sxs-lookup"><span data-stu-id="88f84-843">-8,150.29</span></span></td>
<td><span data-ttu-id="88f84-844">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-845">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-845">CC003</span></span></td>
<td><span data-ttu-id="88f84-846">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-846">Assembly</span></span></td>
<td><span data-ttu-id="88f84-847">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-847">10001</span></span></td>
<td><span data-ttu-id="88f84-848">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-848">Electricity</span></span></td>
<td><span data-ttu-id="88f84-849">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-849">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="88f84-850">5,297.69</span></span></td>
<td><span data-ttu-id="88f84-851">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-852">CC004</span><span class="sxs-lookup"><span data-stu-id="88f84-852">CC004</span></span></td>
<td><span data-ttu-id="88f84-853">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="88f84-853">Packaging</span></span></td>
<td><span data-ttu-id="88f84-854">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-854">10001</span></span></td>
<td><span data-ttu-id="88f84-855">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-855">Electricity</span></span></td>
<td><span data-ttu-id="88f84-856">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-856">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="88f84-857">2,852.60</span></span></td>
<td><span data-ttu-id="88f84-858">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-859">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-859">CC003</span></span></td>
<td><span data-ttu-id="88f84-860">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-860">Assembly</span></span></td>
<td><span data-ttu-id="88f84-861">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-861">10001</span></span></td>
<td><span data-ttu-id="88f84-862">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-862">Electricity</span></span></td>
<td><span data-ttu-id="88f84-863">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-863">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-864">–713,75</span><span class="sxs-lookup"><span data-stu-id="88f84-864">-713.75</span></span></td>
<td><span data-ttu-id="88f84-865">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-866">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="88f84-866">Prod 1</span></span></td>
<td><span data-ttu-id="88f84-867">Toode 1</span><span class="sxs-lookup"><span data-stu-id="88f84-867">Product 1</span></span></td>
<td><span data-ttu-id="88f84-868">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-868">10001</span></span></td>
<td><span data-ttu-id="88f84-869">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-869">Electricity</span></span></td>
<td><span data-ttu-id="88f84-870">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-870">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-871">535.31</span><span class="sxs-lookup"><span data-stu-id="88f84-871">535.31</span></span></td>
<td><span data-ttu-id="88f84-872">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-873">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-873">Prod 2</span></span></td>
<td><span data-ttu-id="88f84-874">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-874">Product 2</span></span></td>
<td><span data-ttu-id="88f84-875">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-875">10001</span></span></td>
<td><span data-ttu-id="88f84-876">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-876">Electricity</span></span></td>
<td><span data-ttu-id="88f84-877">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-877">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-878">178.44</span><span class="sxs-lookup"><span data-stu-id="88f84-878">178.44</span></span></td>
<td><span data-ttu-id="88f84-879">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-880">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-880">CC003</span></span></td>
<td><span data-ttu-id="88f84-881">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-881">Assembly</span></span></td>
<td><span data-ttu-id="88f84-882">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-882">10001</span></span></td>
<td><span data-ttu-id="88f84-883">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-883">Electricity</span></span></td>
<td><span data-ttu-id="88f84-884">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-884">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-885">–5982,83</span><span class="sxs-lookup"><span data-stu-id="88f84-885">-5,982.83</span></span></td>
<td><span data-ttu-id="88f84-886">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-887">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="88f84-887">Prod 1</span></span></td>
<td><span data-ttu-id="88f84-888">Toode 1</span><span class="sxs-lookup"><span data-stu-id="88f84-888">Product 1</span></span></td>
<td><span data-ttu-id="88f84-889">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-889">10001</span></span></td>
<td><span data-ttu-id="88f84-890">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-890">Electricity</span></span></td>
<td><span data-ttu-id="88f84-891">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-891">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="88f84-892">4,487.12</span></span></td>
<td><span data-ttu-id="88f84-893">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-894">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-894">Prod 2</span></span></td>
<td><span data-ttu-id="88f84-895">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-895">Product 2</span></span></td>
<td><span data-ttu-id="88f84-896">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-896">10001</span></span></td>
<td><span data-ttu-id="88f84-897">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-897">Electricity</span></span></td>
<td><span data-ttu-id="88f84-898">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-898">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="88f84-899">1,495.71</span></span></td>
<td><span data-ttu-id="88f84-900">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-901">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-901">CC003</span></span></td>
<td><span data-ttu-id="88f84-902">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-902">Assembly</span></span></td>
<td><span data-ttu-id="88f84-903">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-903">10001</span></span></td>
<td><span data-ttu-id="88f84-904">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-904">Electricity</span></span></td>
<td><span data-ttu-id="88f84-905">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-905">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-906">–286,25</span><span class="sxs-lookup"><span data-stu-id="88f84-906">-286.25</span></span></td>
<td><span data-ttu-id="88f84-907">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-908">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="88f84-908">Prod 1</span></span></td>
<td><span data-ttu-id="88f84-909">Toode 1</span><span class="sxs-lookup"><span data-stu-id="88f84-909">Product 1</span></span></td>
<td><span data-ttu-id="88f84-910">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-910">10001</span></span></td>
<td><span data-ttu-id="88f84-911">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-911">Electricity</span></span></td>
<td><span data-ttu-id="88f84-912">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-912">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-913">241.05</span><span class="sxs-lookup"><span data-stu-id="88f84-913">241.05</span></span></td>
<td><span data-ttu-id="88f84-914">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-915">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-915">Prod 2</span></span></td>
<td><span data-ttu-id="88f84-916">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-916">Product 2</span></span></td>
<td><span data-ttu-id="88f84-917">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-917">10001</span></span></td>
<td><span data-ttu-id="88f84-918">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-918">Electricity</span></span></td>
<td><span data-ttu-id="88f84-919">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-919">Fixed cost</span></span></td>
<td><span data-ttu-id="88f84-920">45.20</span><span class="sxs-lookup"><span data-stu-id="88f84-920">45.20</span></span></td>
<td><span data-ttu-id="88f84-921">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-922">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-922">CC003</span></span></td>
<td><span data-ttu-id="88f84-923">Assembler</span><span class="sxs-lookup"><span data-stu-id="88f84-923">Assembly</span></span></td>
<td><span data-ttu-id="88f84-924">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-924">10001</span></span></td>
<td><span data-ttu-id="88f84-925">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-925">Electricity</span></span></td>
<td><span data-ttu-id="88f84-926">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-926">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-927">–2977,17</span><span class="sxs-lookup"><span data-stu-id="88f84-927">-2,977.17</span></span></td>
<td><span data-ttu-id="88f84-928">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-929">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="88f84-929">Prod 1</span></span></td>
<td><span data-ttu-id="88f84-930">Toode 1</span><span class="sxs-lookup"><span data-stu-id="88f84-930">Product 1</span></span></td>
<td><span data-ttu-id="88f84-931">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-931">10001</span></span></td>
<td><span data-ttu-id="88f84-932">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-932">Electricity</span></span></td>
<td><span data-ttu-id="88f84-933">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-933">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="88f84-934">2,507.09</span></span></td>
<td><span data-ttu-id="88f84-935">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="88f84-936">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-936">Prod 2</span></span></td>
<td><span data-ttu-id="88f84-937">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-937">Product 2</span></span></td>
<td><span data-ttu-id="88f84-938">10001</span><span class="sxs-lookup"><span data-stu-id="88f84-938">10001</span></span></td>
<td><span data-ttu-id="88f84-939">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="88f84-939">Electricity</span></span></td>
<td><span data-ttu-id="88f84-940">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-940">Variable cost</span></span></td>
<td><span data-ttu-id="88f84-941">470.08</span><span class="sxs-lookup"><span data-stu-id="88f84-941">470.08</span></span></td>
<td><span data-ttu-id="88f84-942">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="88f84-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="88f84-943">Lõppsõna</span><span class="sxs-lookup"><span data-stu-id="88f84-943">Conclusion</span></span>
<span data-ttu-id="88f84-944">Finantsaruandluses sisestatakse elektrikulu 10 000,00 fiktiivse kulukeskuse ID-le.</span><span class="sxs-lookup"><span data-stu-id="88f84-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="88f84-945">Nii teavad kuluarvestajad, et see kulu tuleb eraldada.</span><span class="sxs-lookup"><span data-stu-id="88f84-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="88f84-946">Kuluarvestuses liigub kulu rakendatud poliitikate ja reeglite põhjal läbi organisatsiooniüksuste ja -tasemete.</span><span class="sxs-lookup"><span data-stu-id="88f84-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="88f84-947">Iga kulu on seostatud eraldamisalusega, mis pakub kulude eraldamiseks parimat hinnangut.</span><span class="sxs-lookup"><span data-stu-id="88f84-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="88f84-948">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="88f84-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="88f84-949">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="88f84-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="88f84-950">Kokku</span><span class="sxs-lookup"><span data-stu-id="88f84-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="88f84-951">CC099</span><span class="sxs-lookup"><span data-stu-id="88f84-951">CC099</span></span></th>
<th><span data-ttu-id="88f84-952">CC001</span><span class="sxs-lookup"><span data-stu-id="88f84-952">CC001</span></span></th>
<th><span data-ttu-id="88f84-953">CC002</span><span class="sxs-lookup"><span data-stu-id="88f84-953">CC002</span></span></th>
<th><span data-ttu-id="88f84-954">CC003</span><span class="sxs-lookup"><span data-stu-id="88f84-954">CC003</span></span></th>
<th><span data-ttu-id="88f84-955">CC004</span><span class="sxs-lookup"><span data-stu-id="88f84-955">CC004</span></span></th>
<th><span data-ttu-id="88f84-956">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="88f84-956">Proj 1</span></span></th>
<th><span data-ttu-id="88f84-957">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="88f84-957">Proj 2</span></span></th>
<th><span data-ttu-id="88f84-958">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="88f84-958">Prod 1</span></span></th>
<th><span data-ttu-id="88f84-959">Toode 2</span><span class="sxs-lookup"><span data-stu-id="88f84-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="88f84-960">10001 Elekter</span><span class="sxs-lookup"><span data-stu-id="88f84-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="88f84-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="88f84-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="88f84-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="88f84-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="88f84-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="88f84-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="88f84-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="88f84-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="88f84-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="88f84-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="88f84-970">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="88f84-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-971">0,00</span><span class="sxs-lookup"><span data-stu-id="88f84-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="88f84-972">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-973">0,00</span><span class="sxs-lookup"><span data-stu-id="88f84-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-974">0,00</span><span class="sxs-lookup"><span data-stu-id="88f84-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-975">0,00</span><span class="sxs-lookup"><span data-stu-id="88f84-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-976">0,00</span><span class="sxs-lookup"><span data-stu-id="88f84-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-977">0,00</span><span class="sxs-lookup"><span data-stu-id="88f84-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="88f84-978">776.36</span><span class="sxs-lookup"><span data-stu-id="88f84-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-979">223.64</span><span class="sxs-lookup"><span data-stu-id="88f84-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="88f84-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="88f84-981">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="88f84-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-982">000</span><span class="sxs-lookup"><span data-stu-id="88f84-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-983">0,00</span><span class="sxs-lookup"><span data-stu-id="88f84-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-984">0,00</span><span class="sxs-lookup"><span data-stu-id="88f84-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-985">0,00</span><span class="sxs-lookup"><span data-stu-id="88f84-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-986">0,00</span><span class="sxs-lookup"><span data-stu-id="88f84-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-987">30,00</span><span class="sxs-lookup"><span data-stu-id="88f84-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-988">10,00</span><span class="sxs-lookup"><span data-stu-id="88f84-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="88f84-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="88f84-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="88f84-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="88f84-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="88f84-992">Selles teemas selgitatakse, kuidas esmane kuluelement, 10001 Eleter, liigub läbi kuluobjektide.</span><span class="sxs-lookup"><span data-stu-id="88f84-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="88f84-993">Seega eraldatakse see üldkulu organisatsiooni madalaimale tasemele.</span><span class="sxs-lookup"><span data-stu-id="88f84-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="88f84-994">Teisisõnu kannavad kulu madalaimal tasemel olevad kuluobjektid.</span><span class="sxs-lookup"><span data-stu-id="88f84-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="88f84-995">Kui soovite saada kuluobjektide vahelisest kuluvoost visuaalset ülevaadet, saate kuluvoo visualiseerimiseks kasutada kulude kokkuvõtte poliitika reegleid.</span><span class="sxs-lookup"><span data-stu-id="88f84-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="88f84-996">Täpsemat teavet vt teemast [Kulude kokkuvõte](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="88f84-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



