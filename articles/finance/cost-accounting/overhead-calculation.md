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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 954e0669c3d24bcc20fe667c22b7dcc367aba1e7
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770800"
---
# <a name="overhead-calculation"></a><span data-ttu-id="ece5c-103">Üldkulude arvutus</span><span class="sxs-lookup"><span data-stu-id="ece5c-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ece5c-104">Selles teemas kirjeldatakse tüüpilisi üldkulude arvutamise ja eraldamise protsesse.</span><span class="sxs-lookup"><span data-stu-id="ece5c-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="ece5c-105">Mõiste määratlus</span><span class="sxs-lookup"><span data-stu-id="ece5c-105">Term definition</span></span>
---------------

<span data-ttu-id="ece5c-106">Üldkulud on kulud, mis kaasnevad ettevõtte käitamisega, kuid mida ei saa seostada otseselt ühegi kindla äritegevuse, toote ega teenusega.</span><span class="sxs-lookup"><span data-stu-id="ece5c-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="ece5c-107">Üldkulud pakuvad kriitilist tuge kasumit andavate tegevuste loomisele.</span><span class="sxs-lookup"><span data-stu-id="ece5c-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="ece5c-108">Siin on mõned näited üldkuludest.</span><span class="sxs-lookup"><span data-stu-id="ece5c-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="ece5c-109">Üür</span><span class="sxs-lookup"><span data-stu-id="ece5c-109">Rent</span></span>
-   <span data-ttu-id="ece5c-110">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-110">Electricity</span></span>
-   <span data-ttu-id="ece5c-111">Haldustasud</span><span class="sxs-lookup"><span data-stu-id="ece5c-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="ece5c-112">Üldkulude arvutuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="ece5c-112">Overhead calculation overview</span></span>
<span data-ttu-id="ece5c-113">Üldkulude arvutus käitab kuluarvutuse poliitikaid õiges järjekorras.</span><span class="sxs-lookup"><span data-stu-id="ece5c-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="ece5c-114">Saate käivitada üldkulude arvutuse sama rahandusperioodi kohta mitu korda, kui kuluarvestuse poliitikaid on muudetud või tuvastatud teatud tõrked.</span><span class="sxs-lookup"><span data-stu-id="ece5c-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="ece5c-115">Iga üldkulude arvutamise käitamine talletatakse ja see saab kordumatu versiooni-ID, mis võimaldab teil arvutuste erinevaid versioone võrrelda.</span><span class="sxs-lookup"><span data-stu-id="ece5c-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="ece5c-116">Ülekulude arvutusega loodud kulukirjed saavad aruandluskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="ece5c-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="ece5c-117">See aruandluskuupäev vastab arvutuses kasutatud rahandusperioodi lõppkuupäevale.</span><span class="sxs-lookup"><span data-stu-id="ece5c-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="ece5c-118">Kordumatu versiooni-ID koosneb järgmistest elementidest.</span><span class="sxs-lookup"><span data-stu-id="ece5c-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="ece5c-119">Versiooni tüüp</span><span class="sxs-lookup"><span data-stu-id="ece5c-119">Version type</span></span>
-   <span data-ttu-id="ece5c-120">Kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="ece5c-120">Date and time</span></span>
-   <span data-ttu-id="ece5c-121">Kuluarvestuse pearaamat</span><span class="sxs-lookup"><span data-stu-id="ece5c-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="ece5c-122">Finantsaasta</span><span class="sxs-lookup"><span data-stu-id="ece5c-122">Fiscal year</span></span>
-   <span data-ttu-id="ece5c-123">Rahandusperiood</span><span class="sxs-lookup"><span data-stu-id="ece5c-123">Fiscal period</span></span>

<span data-ttu-id="ece5c-124">Üldkulude arvutus käivitatakse versioonist sõltumatult.</span><span class="sxs-lookup"><span data-stu-id="ece5c-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="ece5c-125">Seetõttu saate arvutada eelarveversiooni enne tegelikku versiooni.</span><span class="sxs-lookup"><span data-stu-id="ece5c-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="ece5c-126">Üldkulude arvutus koosneb neljast etapist, nagu näha alltoodud joonisel.</span><span class="sxs-lookup"><span data-stu-id="ece5c-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="ece5c-127">Igas etapis luuakse töölehe päis, millel on töölehe kanded.</span><span class="sxs-lookup"><span data-stu-id="ece5c-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="ece5c-128">See töölehe päis säiiltab sisendandmeid iga arvutusetapi kohta.</span><span class="sxs-lookup"><span data-stu-id="ece5c-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="ece5c-129">Igale töölehe reale rakendatakse poliitikad ja reeglid ning väljundina luuakse kulukirjed.</span><span class="sxs-lookup"><span data-stu-id="ece5c-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="ece5c-130">Seega on teil alati olemas põhjalik ülevaade.</span><span class="sxs-lookup"><span data-stu-id="ece5c-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="ece5c-131">[![Üldkulude arvutus](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="ece5c-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="ece5c-132">Elektri üldkulude arvutamine ja eraldamine</span><span class="sxs-lookup"><span data-stu-id="ece5c-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="ece5c-133">Finantsaruandluses on mõned kulud, näiteks elekter, registreeritud põhisummana.</span><span class="sxs-lookup"><span data-stu-id="ece5c-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="ece5c-134">Seetõttu ei pakuta kuluarvestuseks üksikasjalikku juhtimisülevaadet.</span><span class="sxs-lookup"><span data-stu-id="ece5c-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="ece5c-135">Kuluarvestuses peavad kulud liikuma läbi organisatsiooniüksuste, et pakkuda korrektset juhtimisülevaadet kõigi organisatsiooniüksuste ja -tasemete kohta.</span><span class="sxs-lookup"><span data-stu-id="ece5c-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="ece5c-136">See voog peab põhinema tarbimise või õiglase hindamise täpsel kirjendamisel.</span><span class="sxs-lookup"><span data-stu-id="ece5c-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="ece5c-137">Pearaamatus, saab elektrikulu sisestada nii, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="ece5c-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ece5c-138">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="ece5c-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ece5c-139">Kulukeskus</span><span class="sxs-lookup"><span data-stu-id="ece5c-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="ece5c-140">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="ece5c-140">Main account</span></span></th>
<th><span data-ttu-id="ece5c-141">Summa arvestusvaluutas</span><span class="sxs-lookup"><span data-stu-id="ece5c-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-142">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="ece5c-143">CC099</span><span class="sxs-lookup"><span data-stu-id="ece5c-143">CC099</span></span></td>
<td><span data-ttu-id="ece5c-144">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="ece5c-144">Default cost center</span></span></td>
<td><span data-ttu-id="ece5c-145">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-145">10001</span></span></td>
<td><span data-ttu-id="ece5c-146">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-146">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="ece5c-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="ece5c-148">1. etapp: kulukäitumise arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="ece5c-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="ece5c-149">Vaikimisi saavad lähteandmetest imporditud kulukirjed kuluarvestuses kulukäitumise klassifikatsiooniks **Klassifitseerimata**.</span><span class="sxs-lookup"><span data-stu-id="ece5c-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="ece5c-150">Kulukäitumise poliitikareegleid rakendades saate kulukirjed ümber klassifitseerida kui **Fikseeritud kulu** või **Muutuvkulu**.</span><span class="sxs-lookup"><span data-stu-id="ece5c-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="ece5c-151">Kulukäitumise reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="ece5c-151">Define the cost behavior rule</span></span>

<span data-ttu-id="ece5c-152">Mõnikord on osa kulust fikseeritud tasu ja järelejäänud kulu põhineb tarbimisel.</span><span class="sxs-lookup"><span data-stu-id="ece5c-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="ece5c-153">Elektriarved vastavad sageli sellele määratlusele.</span><span class="sxs-lookup"><span data-stu-id="ece5c-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="ece5c-154">Pärast kindla fikseeritud tasu maksmist maksate tarbimise eest kilovatt-tunni (Kwh) kohta.</span><span class="sxs-lookup"><span data-stu-id="ece5c-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="ece5c-155">Näiteks kui fikseeritud kulu tasu on 1000,00 eurot, määratletakse kulukäitumise reegel järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ece5c-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="ece5c-156">Fikseeritud summa: 1000,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="ece5c-157">0 &lt;= 1000,00 = fikseeritud</span><span class="sxs-lookup"><span data-stu-id="ece5c-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="ece5c-158">1000,01 &lt; N = muutuja</span><span class="sxs-lookup"><span data-stu-id="ece5c-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="ece5c-159">Tööleht</span><span class="sxs-lookup"><span data-stu-id="ece5c-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ece5c-160">Tööleht</span><span class="sxs-lookup"><span data-stu-id="ece5c-160">Journal</span></span></th>
<th><span data-ttu-id="ece5c-161">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="ece5c-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ece5c-162">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="ece5c-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ece5c-163">Versioon</span><span class="sxs-lookup"><span data-stu-id="ece5c-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-164">00001</span><span class="sxs-lookup"><span data-stu-id="ece5c-164">00001</span></span></td>
<td><span data-ttu-id="ece5c-165">Kulukäitumise arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="ece5c-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="ece5c-166">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="ece5c-166">Fiscal</span></span></td>
<td><span data-ttu-id="ece5c-167">2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-167">2017</span></span></td>
<td><span data-ttu-id="ece5c-168">Periood 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-168">Period 1</span></span></td>
<td><span data-ttu-id="ece5c-169">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="ece5c-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ece5c-170">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="ece5c-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ece5c-171">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="ece5c-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ece5c-172">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ece5c-173">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="ece5c-173">Cost element</span></span></th>
<th><span data-ttu-id="ece5c-174">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="ece5c-174">Cost behavior</span></span></th>
<th><span data-ttu-id="ece5c-175">Summa</span><span class="sxs-lookup"><span data-stu-id="ece5c-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-176">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="ece5c-177">CC099</span><span class="sxs-lookup"><span data-stu-id="ece5c-177">CC099</span></span></td>
<td><span data-ttu-id="ece5c-178">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="ece5c-178">Default cost center</span></span></td>
<td><span data-ttu-id="ece5c-179">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-179">10001</span></span></td>
<td><span data-ttu-id="ece5c-180">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-180">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-181">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="ece5c-181">Unclassified</span></span></td>
<td><span data-ttu-id="ece5c-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="ece5c-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ece5c-183">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="ece5c-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-184">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ece5c-185">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="ece5c-185">Cost element</span></span></th>
<th><span data-ttu-id="ece5c-186">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="ece5c-186">Cost behavior</span></span></th>
<th><span data-ttu-id="ece5c-187">Summa</span><span class="sxs-lookup"><span data-stu-id="ece5c-187">Amount</span></span></th>
<th><span data-ttu-id="ece5c-188">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="ece5c-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-189">CC099</span><span class="sxs-lookup"><span data-stu-id="ece5c-189">CC099</span></span></td>
<td><span data-ttu-id="ece5c-190">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="ece5c-190">Default cost center</span></span></td>
<td><span data-ttu-id="ece5c-191">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-191">10001</span></span></td>
<td><span data-ttu-id="ece5c-192">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-192">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-193">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="ece5c-193">Unclassified</span></span></td>
<td><span data-ttu-id="ece5c-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="ece5c-194">10,000.00</span></span></td>
<td><span data-ttu-id="ece5c-195">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-196">CC099</span><span class="sxs-lookup"><span data-stu-id="ece5c-196">CC099</span></span></td>
<td><span data-ttu-id="ece5c-197">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="ece5c-197">Default cost center</span></span></td>
<td><span data-ttu-id="ece5c-198">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-198">10001</span></span></td>
<td><span data-ttu-id="ece5c-199">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-199">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-200">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="ece5c-200">Unclassified</span></span></td>
<td><span data-ttu-id="ece5c-201">–10 000,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-201">-10,000.00</span></span></td>
<td><span data-ttu-id="ece5c-202">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-203">CC099</span><span class="sxs-lookup"><span data-stu-id="ece5c-203">CC099</span></span></td>
<td><span data-ttu-id="ece5c-204">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="ece5c-204">Default cost center</span></span></td>
<td><span data-ttu-id="ece5c-205">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-205">10001</span></span></td>
<td><span data-ttu-id="ece5c-206">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-206">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-207">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-207">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-208">1,000.00</span></span></td>
<td><span data-ttu-id="ece5c-209">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-210">CC099</span><span class="sxs-lookup"><span data-stu-id="ece5c-210">CC099</span></span></td>
<td><span data-ttu-id="ece5c-211">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="ece5c-211">Default cost center</span></span></td>
<td><span data-ttu-id="ece5c-212">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-212">10001</span></span></td>
<td><span data-ttu-id="ece5c-213">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-213">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-214">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-214">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="ece5c-215">9,000.00</span></span></td>
<td><span data-ttu-id="ece5c-216">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ece5c-217">Lisateavet vt teemast [Kulukäitumise poliitika loomine ja määramine kulujuhtimisüksusele (tegevuse juhis)](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="ece5c-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="ece5c-218">2. etapp: kulujaotuse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="ece5c-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="ece5c-219">Kulujaotust kasutatakse kulu ümberjaotamiseks ühelt kuluobjektilt ühele või mitmele teisele kuluobjektile, rakendades asjakohast eraldusalust.</span><span class="sxs-lookup"><span data-stu-id="ece5c-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="ece5c-220">Kulujaotus ja kulueraldus erinevad selle poolest, et kulujaotus toimub alati algse kulu esmase kuluelemendi tasemel.</span><span class="sxs-lookup"><span data-stu-id="ece5c-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="ece5c-221">Kulujaotuse reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="ece5c-221">Define the cost distribution rule</span></span>

<span data-ttu-id="ece5c-222">Finantsaruandluses registreeritakse elektrikulud sageli põhisummana.</span><span class="sxs-lookup"><span data-stu-id="ece5c-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="ece5c-223">Kuluarvestuseses ei ole see lähenemine piisavalt üksikasjalik.</span><span class="sxs-lookup"><span data-stu-id="ece5c-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="ece5c-224">Muutuvkulu tuleb jaotada üksikutele kuluobjektidele õigluse alusel.</span><span class="sxs-lookup"><span data-stu-id="ece5c-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="ece5c-225">Kõige loogilisem eraldamisalus on elektritarbimine (kWh).</span><span class="sxs-lookup"><span data-stu-id="ece5c-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="ece5c-226">Luuakse statistilise dimensiooni liige nimega Elekter ja elektritarbimine on kirjendatakse.</span><span class="sxs-lookup"><span data-stu-id="ece5c-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="ece5c-227">Vaikimisi muutuvad kõik statistilise dimensiooni liikmed eraldamisalusena kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="ece5c-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-228">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-228">Cost object</span></span></th>
<th><span data-ttu-id="ece5c-229">kWh</span><span class="sxs-lookup"><span data-stu-id="ece5c-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-230">CC001</span><span class="sxs-lookup"><span data-stu-id="ece5c-230">CC001</span></span></td>
<td><span data-ttu-id="ece5c-231">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="ece5c-231">HR</span></span></td>
<td><span data-ttu-id="ece5c-232">1000</span><span class="sxs-lookup"><span data-stu-id="ece5c-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-233">CC002</span><span class="sxs-lookup"><span data-stu-id="ece5c-233">CC002</span></span></td>
<td><span data-ttu-id="ece5c-234">Finantsid</span><span class="sxs-lookup"><span data-stu-id="ece5c-234">Finance</span></span></td>
<td><span data-ttu-id="ece5c-235">6,000</span><span class="sxs-lookup"><span data-stu-id="ece5c-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-236">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-236">CC003</span></span></td>
<td><span data-ttu-id="ece5c-237">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-237">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-238">0</span><span class="sxs-lookup"><span data-stu-id="ece5c-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ece5c-239">Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="ece5c-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-240">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-240">Cost object</span></span></th>
<th><span data-ttu-id="ece5c-241">Väärtus</span><span class="sxs-lookup"><span data-stu-id="ece5c-241">Magnitude</span></span></th>
<th><span data-ttu-id="ece5c-242">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="ece5c-242">Allocation factor</span></span></th>
<th><span data-ttu-id="ece5c-243">Summa</span><span class="sxs-lookup"><span data-stu-id="ece5c-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-244">CC001</span><span class="sxs-lookup"><span data-stu-id="ece5c-244">CC001</span></span></td>
<td><span data-ttu-id="ece5c-245">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="ece5c-245">HR</span></span></td>
<td><span data-ttu-id="ece5c-246">1000</span><span class="sxs-lookup"><span data-stu-id="ece5c-246">1,000</span></span></td>
<td><span data-ttu-id="ece5c-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ece5c-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="ece5c-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-249">CC002</span><span class="sxs-lookup"><span data-stu-id="ece5c-249">CC002</span></span></td>
<td><span data-ttu-id="ece5c-250">Finantsid</span><span class="sxs-lookup"><span data-stu-id="ece5c-250">Finance</span></span></td>
<td><span data-ttu-id="ece5c-251">6,000</span><span class="sxs-lookup"><span data-stu-id="ece5c-251">6,000</span></span></td>
<td><span data-ttu-id="ece5c-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ece5c-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="ece5c-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-254">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-254">CC003</span></span></td>
<td><span data-ttu-id="ece5c-255">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-255">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-256">0</span><span class="sxs-lookup"><span data-stu-id="ece5c-256">0</span></span></td>
<td><span data-ttu-id="ece5c-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ece5c-258">0,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ece5c-259">Fikseeritud kulu tuleb jaotada ühtlaselt üksikutele kuluobjektidele, mis on tarbinud elektrit.</span><span class="sxs-lookup"><span data-stu-id="ece5c-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="ece5c-260">Selle tulemuse saate, kasutades valemi eraldamisaluses statistilise dimensiooni liiget Elekter: (Elekter &gt; 0,00). Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="ece5c-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-261">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-261">Cost object</span></span></th>
<th><span data-ttu-id="ece5c-262">Valem</span><span class="sxs-lookup"><span data-stu-id="ece5c-262">Formula</span></span></th>
<th><span data-ttu-id="ece5c-263">Väärtus</span><span class="sxs-lookup"><span data-stu-id="ece5c-263">Magnitude</span></span></th>
<th><span data-ttu-id="ece5c-264">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="ece5c-264">Allocation factor</span></span></th>
<th><span data-ttu-id="ece5c-265">Summa</span><span class="sxs-lookup"><span data-stu-id="ece5c-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-266">CC001</span><span class="sxs-lookup"><span data-stu-id="ece5c-266">CC001</span></span></td>
<td><span data-ttu-id="ece5c-267">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="ece5c-267">HR</span></span></td>
<td><span data-ttu-id="ece5c-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="ece5c-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ece5c-269">1</span><span class="sxs-lookup"><span data-stu-id="ece5c-269">1</span></span></td>
<td><span data-ttu-id="ece5c-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ece5c-271">500,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-272">CC002</span><span class="sxs-lookup"><span data-stu-id="ece5c-272">CC002</span></span></td>
<td><span data-ttu-id="ece5c-273">Finantsid</span><span class="sxs-lookup"><span data-stu-id="ece5c-273">Finance</span></span></td>
<td><span data-ttu-id="ece5c-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="ece5c-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ece5c-275">1</span><span class="sxs-lookup"><span data-stu-id="ece5c-275">1</span></span></td>
<td><span data-ttu-id="ece5c-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ece5c-277">500,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-278">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-278">CC003</span></span></td>
<td><span data-ttu-id="ece5c-279">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-279">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="ece5c-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ece5c-281">0</span><span class="sxs-lookup"><span data-stu-id="ece5c-281">0</span></span></td>
<td><span data-ttu-id="ece5c-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ece5c-283">0,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="ece5c-284">Tööleht</span><span class="sxs-lookup"><span data-stu-id="ece5c-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ece5c-285">Tööleht</span><span class="sxs-lookup"><span data-stu-id="ece5c-285">Journal</span></span></th>
<th><span data-ttu-id="ece5c-286">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="ece5c-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ece5c-287">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="ece5c-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ece5c-288">Versioon</span><span class="sxs-lookup"><span data-stu-id="ece5c-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-289">00002</span><span class="sxs-lookup"><span data-stu-id="ece5c-289">00002</span></span></td>
<td><span data-ttu-id="ece5c-290">Kulujaotuse arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="ece5c-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="ece5c-291">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="ece5c-291">Fiscal</span></span></td>
<td><span data-ttu-id="ece5c-292">2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-292">2017</span></span></td>
<td><span data-ttu-id="ece5c-293">Periood 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-293">Period 1</span></span></td>
<td><span data-ttu-id="ece5c-294">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="ece5c-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ece5c-295">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="ece5c-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ece5c-296">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="ece5c-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ece5c-297">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ece5c-298">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="ece5c-298">Cost element</span></span></th>
<th><span data-ttu-id="ece5c-299">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="ece5c-299">Cost behavior</span></span></th>
<th><span data-ttu-id="ece5c-300">Summa</span><span class="sxs-lookup"><span data-stu-id="ece5c-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-301">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="ece5c-302">CC099</span><span class="sxs-lookup"><span data-stu-id="ece5c-302">CC099</span></span></td>
<td><span data-ttu-id="ece5c-303">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="ece5c-303">Default cost center</span></span></td>
<td><span data-ttu-id="ece5c-304">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-304">10001</span></span></td>
<td><span data-ttu-id="ece5c-305">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-305">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-306">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-306">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-308">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="ece5c-309">CC099</span><span class="sxs-lookup"><span data-stu-id="ece5c-309">CC099</span></span></td>
<td><span data-ttu-id="ece5c-310">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="ece5c-310">Default cost center</span></span></td>
<td><span data-ttu-id="ece5c-311">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-311">10001</span></span></td>
<td><span data-ttu-id="ece5c-312">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-312">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-313">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-313">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="ece5c-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ece5c-315">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="ece5c-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-316">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ece5c-317">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="ece5c-317">Cost element</span></span></th>
<th><span data-ttu-id="ece5c-318">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="ece5c-318">Cost behavior</span></span></th>
<th><span data-ttu-id="ece5c-319">Summa</span><span class="sxs-lookup"><span data-stu-id="ece5c-319">Amount</span></span></th>
<th><span data-ttu-id="ece5c-320">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="ece5c-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-321">CC099</span><span class="sxs-lookup"><span data-stu-id="ece5c-321">CC099</span></span></td>
<td><span data-ttu-id="ece5c-322">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="ece5c-322">Default cost center</span></span></td>
<td><span data-ttu-id="ece5c-323">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-323">10001</span></span></td>
<td><span data-ttu-id="ece5c-324">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-324">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-325">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-325">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-326">–1000,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-326">-1,000.00</span></span></td>
<td><span data-ttu-id="ece5c-327">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-328">CC001</span><span class="sxs-lookup"><span data-stu-id="ece5c-328">CC001</span></span></td>
<td><span data-ttu-id="ece5c-329">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="ece5c-329">HR</span></span></td>
<td><span data-ttu-id="ece5c-330">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-330">10001</span></span></td>
<td><span data-ttu-id="ece5c-331">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-331">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-332">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-332">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-333">500,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-333">500.00</span></span></td>
<td><span data-ttu-id="ece5c-334">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-335">CC002</span><span class="sxs-lookup"><span data-stu-id="ece5c-335">CC002</span></span></td>
<td><span data-ttu-id="ece5c-336">Finantsid</span><span class="sxs-lookup"><span data-stu-id="ece5c-336">Finance</span></span></td>
<td><span data-ttu-id="ece5c-337">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-337">10001</span></span></td>
<td><span data-ttu-id="ece5c-338">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-338">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-339">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-339">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-340">500,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-340">500.00</span></span></td>
<td><span data-ttu-id="ece5c-341">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-342">CC099</span><span class="sxs-lookup"><span data-stu-id="ece5c-342">CC099</span></span></td>
<td><span data-ttu-id="ece5c-343">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="ece5c-343">Default cost center</span></span></td>
<td><span data-ttu-id="ece5c-344">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-344">10001</span></span></td>
<td><span data-ttu-id="ece5c-345">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-345">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-346">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-346">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-347">–9000,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-347">-9,000.00</span></span></td>
<td><span data-ttu-id="ece5c-348">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-349">CC001</span><span class="sxs-lookup"><span data-stu-id="ece5c-349">CC001</span></span></td>
<td><span data-ttu-id="ece5c-350">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="ece5c-350">HR</span></span></td>
<td><span data-ttu-id="ece5c-351">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-351">10001</span></span></td>
<td><span data-ttu-id="ece5c-352">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-352">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-353">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-353">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="ece5c-354">1,285.71</span></span></td>
<td><span data-ttu-id="ece5c-355">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-356">CC002</span><span class="sxs-lookup"><span data-stu-id="ece5c-356">CC002</span></span></td>
<td><span data-ttu-id="ece5c-357">Finantsid</span><span class="sxs-lookup"><span data-stu-id="ece5c-357">Finance</span></span></td>
<td><span data-ttu-id="ece5c-358">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-358">10001</span></span></td>
<td><span data-ttu-id="ece5c-359">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-359">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-360">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-360">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="ece5c-361">7,714.29</span></span></td>
<td><span data-ttu-id="ece5c-362">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ece5c-363">Lisateavet vt teemast [Kulujaotise poliitika loomine ja määramine kulujuhtimisüksusele (tegevuse juhis)](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="ece5c-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="ece5c-364">3. etapp: üldkulude määra arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="ece5c-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="ece5c-365">Üldkulude määra kasutatakse ühe või mitme kindla kuluobjekti debiteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="ece5c-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="ece5c-366">Tasu põhineb eelmääratud kulumääral ja väärtusel määratud eraldamisalusest.</span><span class="sxs-lookup"><span data-stu-id="ece5c-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="ece5c-367">Üldkulu määra määratlemine</span><span class="sxs-lookup"><span data-stu-id="ece5c-367">Define the overhead rate</span></span>

<span data-ttu-id="ece5c-368">Kuluobjekt CC001 inimressursid panustab sisemiste projektide kogumisse.</span><span class="sxs-lookup"><span data-stu-id="ece5c-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="ece5c-369">Luuakse statistilise dimensiooni liige nimega Inimressursside projektid, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="ece5c-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-370">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-370">Cost object</span></span></th>
<th><span data-ttu-id="ece5c-371">Tunnid</span><span class="sxs-lookup"><span data-stu-id="ece5c-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-372">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-372">Proj 1</span></span></td>
<td><span data-ttu-id="ece5c-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-373">Project 1</span></span></td>
<td><span data-ttu-id="ece5c-374">3</span><span class="sxs-lookup"><span data-stu-id="ece5c-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-375">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-375">Proj 2</span></span></td>
<td><span data-ttu-id="ece5c-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-376">Project 2</span></span></td>
<td><span data-ttu-id="ece5c-377">1</span><span class="sxs-lookup"><span data-stu-id="ece5c-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ece5c-378">Määratletud on eelmääratud kulumäär kuluprojektide panusele.</span><span class="sxs-lookup"><span data-stu-id="ece5c-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-379">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-379">Cost object</span></span></th>
<th><span data-ttu-id="ece5c-380">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="ece5c-380">Cost element</span></span></th>
<th><span data-ttu-id="ece5c-381">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="ece5c-381">Cost behavior</span></span></th>
<th><span data-ttu-id="ece5c-382">Ühikud</span><span class="sxs-lookup"><span data-stu-id="ece5c-382">Units</span></span></th>
<th><span data-ttu-id="ece5c-383">Kurss</span><span class="sxs-lookup"><span data-stu-id="ece5c-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-384">CC001</span><span class="sxs-lookup"><span data-stu-id="ece5c-384">CC001</span></span></td>
<td><span data-ttu-id="ece5c-385">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="ece5c-385">HR</span></span></td>
<td><span data-ttu-id="ece5c-386">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-386">10001</span></span></td>
<td><span data-ttu-id="ece5c-387">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-387">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-388">1</span><span class="sxs-lookup"><span data-stu-id="ece5c-388">1</span></span></td>
<td><span data-ttu-id="ece5c-389">10</span><span class="sxs-lookup"><span data-stu-id="ece5c-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ece5c-390">Järgmises tabelis on näidatud tulemus, kui inimressursside projektid on rakendatud eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="ece5c-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-391">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-391">Cost object</span></span></th>
<th><span data-ttu-id="ece5c-392">Väärtus</span><span class="sxs-lookup"><span data-stu-id="ece5c-392">Magnitude</span></span></th>
<th><span data-ttu-id="ece5c-393">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="ece5c-393">Cost element</span></span></th>
<th><span data-ttu-id="ece5c-394">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="ece5c-394">Allocation factor</span></span></th>
<th><span data-ttu-id="ece5c-395">Summa</span><span class="sxs-lookup"><span data-stu-id="ece5c-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-396">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-396">Proj 1</span></span></td>
<td><span data-ttu-id="ece5c-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-397">Project 1</span></span></td>
<td><span data-ttu-id="ece5c-398">3</span><span class="sxs-lookup"><span data-stu-id="ece5c-398">3</span></span></td>
<td><span data-ttu-id="ece5c-399">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-399">10001</span></span></td>
<td><span data-ttu-id="ece5c-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="ece5c-401">30,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-402">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-402">Proj 2</span></span></td>
<td><span data-ttu-id="ece5c-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-403">Project 2</span></span></td>
<td><span data-ttu-id="ece5c-404">1</span><span class="sxs-lookup"><span data-stu-id="ece5c-404">1</span></span></td>
<td><span data-ttu-id="ece5c-405">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-405">10001</span></span></td>
<td><span data-ttu-id="ece5c-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="ece5c-407">10,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="ece5c-408">Tööleht</span><span class="sxs-lookup"><span data-stu-id="ece5c-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ece5c-409">Tööleht</span><span class="sxs-lookup"><span data-stu-id="ece5c-409">Journal</span></span></th>
<th><span data-ttu-id="ece5c-410">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="ece5c-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ece5c-411">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="ece5c-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ece5c-412">Versioon</span><span class="sxs-lookup"><span data-stu-id="ece5c-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-413">00003</span><span class="sxs-lookup"><span data-stu-id="ece5c-413">00003</span></span></td>
<td><span data-ttu-id="ece5c-414">Üldkulu määra arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="ece5c-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="ece5c-415">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="ece5c-415">Fiscal</span></span></td>
<td><span data-ttu-id="ece5c-416">2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-416">2017</span></span></td>
<td><span data-ttu-id="ece5c-417">Periood 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-417">Period 1</span></span></td>
<td><span data-ttu-id="ece5c-418">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="ece5c-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="ece5c-419">Töölehe sisestused (töölehe sisestused üldkulu määra arvutamiseks)</span><span class="sxs-lookup"><span data-stu-id="ece5c-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ece5c-420">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="ece5c-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ece5c-421">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-421">Cost object</span></span></th>
<th><span data-ttu-id="ece5c-422">Väärtus</span><span class="sxs-lookup"><span data-stu-id="ece5c-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-423">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="ece5c-424">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-424">Proj 1</span></span></td>
<td><span data-ttu-id="ece5c-425">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="ece5c-426">3,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-427">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="ece5c-428">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-428">Proj 2</span></span></td>
<td><span data-ttu-id="ece5c-429">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="ece5c-430">1,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ece5c-431">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="ece5c-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-432">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ece5c-433">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="ece5c-433">Cost element</span></span></th>
<th><span data-ttu-id="ece5c-434">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="ece5c-434">Cost behavior</span></span></th>
<th><span data-ttu-id="ece5c-435">Summa</span><span class="sxs-lookup"><span data-stu-id="ece5c-435">Amount</span></span></th>
<th><span data-ttu-id="ece5c-436">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="ece5c-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="ece5c-437">CC0001</span></span></td>
<td><span data-ttu-id="ece5c-438">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="ece5c-438">HR</span></span></td>
<td><span data-ttu-id="ece5c-439">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-439">10001</span></span></td>
<td><span data-ttu-id="ece5c-440">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-440">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-441">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-441">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-442">–30,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-442">-30.00</span></span></td>
<td><span data-ttu-id="ece5c-443">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-444">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-444">Proj 1</span></span></td>
<td><span data-ttu-id="ece5c-445">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="ece5c-446">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-446">10001</span></span></td>
<td><span data-ttu-id="ece5c-447">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-447">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-448">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-448">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-449">30,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-449">30.00</span></span></td>
<td><span data-ttu-id="ece5c-450">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-451">CC001</span><span class="sxs-lookup"><span data-stu-id="ece5c-451">CC001</span></span></td>
<td><span data-ttu-id="ece5c-452">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="ece5c-452">HR</span></span></td>
<td><span data-ttu-id="ece5c-453">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-453">10001</span></span></td>
<td><span data-ttu-id="ece5c-454">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-454">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-455">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-455">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-456">-10.00</span></span></td>
<td><span data-ttu-id="ece5c-457">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-458">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-458">Proj 2</span></span></td>
<td><span data-ttu-id="ece5c-459">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="ece5c-460">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-460">10001</span></span></td>
<td><span data-ttu-id="ece5c-461">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-461">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-462">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-462">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-463">10.00</span><span class="sxs-lookup"><span data-stu-id="ece5c-463">10.00</span></span></td>
<td><span data-ttu-id="ece5c-464">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ece5c-465">Lisateavet vt teemast [Üldkulude arvutamine](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="ece5c-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="ece5c-466">4. etapp: kulueralduse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="ece5c-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="ece5c-467">Eraldamist kasutatakse kuluobjekti saldo eraldamiseks teistele kuluobjektidele, rakendades eraldamisalust.</span><span class="sxs-lookup"><span data-stu-id="ece5c-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="ece5c-468">Finance toetab vastastikuse eraldamise meetodit.</span><span class="sxs-lookup"><span data-stu-id="ece5c-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="ece5c-469">Vastastikuse eraldamise meetodi puhul tuvastatakse täiendavate kuluobjektide vahetatavad vastastikused teenused.</span><span class="sxs-lookup"><span data-stu-id="ece5c-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="ece5c-470">Süsteem määrab automaatselt eraldamiste tegemise õige järjekorra.</span><span class="sxs-lookup"><span data-stu-id="ece5c-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="ece5c-471">Kuluobjekti saldo eraldatakse üksiku eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="ece5c-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="ece5c-472">Toetatakse eraldamisi kuluobjektide dimensioonide ja nende vastavate liikmete seas.</span><span class="sxs-lookup"><span data-stu-id="ece5c-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="ece5c-473">Eraldamisjärjekorda reguleerib kulujuhtseade.</span><span class="sxs-lookup"><span data-stu-id="ece5c-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="ece5c-474">[![Vastastikune meetod](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="ece5c-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="ece5c-475">Kulueraldamise määratlemine</span><span class="sxs-lookup"><span data-stu-id="ece5c-475">Define the cost allocation</span></span>

<span data-ttu-id="ece5c-476">Siin on lihtne näide, mis selgitab, kuidas jälgida kulu liikumist.</span><span class="sxs-lookup"><span data-stu-id="ece5c-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="ece5c-477">Kuluobjekt CC001 inimressursid panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="ece5c-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="ece5c-478">Luuakse statistilise dimensiooni liige nimega Inimressursside teenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="ece5c-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-479">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-479">Cost object</span></span></th>
<th><span data-ttu-id="ece5c-480">Inimressursside teenused</span><span class="sxs-lookup"><span data-stu-id="ece5c-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-481">CC002</span><span class="sxs-lookup"><span data-stu-id="ece5c-481">CC002</span></span></td>
<td><span data-ttu-id="ece5c-482">Finantsid</span><span class="sxs-lookup"><span data-stu-id="ece5c-482">Finance</span></span></td>
<td><span data-ttu-id="ece5c-483">35</span><span class="sxs-lookup"><span data-stu-id="ece5c-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-484">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-484">CC003</span></span></td>
<td><span data-ttu-id="ece5c-485">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-485">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-486">55</span><span class="sxs-lookup"><span data-stu-id="ece5c-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-487">CC004</span><span class="sxs-lookup"><span data-stu-id="ece5c-487">CC004</span></span></td>
<td><span data-ttu-id="ece5c-488">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="ece5c-488">Packaging</span></span></td>
<td><span data-ttu-id="ece5c-489">10</span><span class="sxs-lookup"><span data-stu-id="ece5c-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ece5c-490">Kuluobjekt CC002 rahandus panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="ece5c-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="ece5c-491">Luuakse statistilise dimensiooni liige nimega Rahandusteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="ece5c-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-492">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-492">Cost object</span></span></th>
<th><span data-ttu-id="ece5c-493">Rahandusteenused</span><span class="sxs-lookup"><span data-stu-id="ece5c-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-494">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-494">CC003</span></span></td>
<td><span data-ttu-id="ece5c-495">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-495">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-496">65</span><span class="sxs-lookup"><span data-stu-id="ece5c-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-497">CC004</span><span class="sxs-lookup"><span data-stu-id="ece5c-497">CC004</span></span></td>
<td><span data-ttu-id="ece5c-498">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="ece5c-498">Packaging</span></span></td>
<td><span data-ttu-id="ece5c-499">35</span><span class="sxs-lookup"><span data-stu-id="ece5c-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ece5c-500">Kuluobjekt CC003 assembler panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="ece5c-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="ece5c-501">Luuakse statistilise dimensiooni liige nimega Assembleriteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="ece5c-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-502">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-502">Cost object</span></span></th>
<th><span data-ttu-id="ece5c-503">Assembleriteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="ece5c-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-504">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-504">Prod 1</span></span></td>
<td><span data-ttu-id="ece5c-505">Toode 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-505">Product 1</span></span></td>
<td><span data-ttu-id="ece5c-506">60</span><span class="sxs-lookup"><span data-stu-id="ece5c-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-507">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-507">Prod 2</span></span></td>
<td><span data-ttu-id="ece5c-508">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-508">Product 2</span></span></td>
<td><span data-ttu-id="ece5c-509">20</span><span class="sxs-lookup"><span data-stu-id="ece5c-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ece5c-510">Kuluobjekt CC004 pakendamine panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="ece5c-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="ece5c-511">Luuakse statistilise dimensiooni liige nimega Pakendamisteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="ece5c-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-512">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-512">Cost object</span></span></th>
<th><span data-ttu-id="ece5c-513">Pakendamisteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="ece5c-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-514">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-514">Prod 1</span></span></td>
<td><span data-ttu-id="ece5c-515">Toode 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-515">Product 1</span></span></td>
<td><span data-ttu-id="ece5c-516">80</span><span class="sxs-lookup"><span data-stu-id="ece5c-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-517">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-517">Prod 2</span></span></td>
<td><span data-ttu-id="ece5c-518">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-518">Product 2</span></span></td>
<td><span data-ttu-id="ece5c-519">15</span><span class="sxs-lookup"><span data-stu-id="ece5c-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ece5c-520">Statistilised mõõdud, nagu toote tarbitud tootmistunnid, saab tuletada lähteandmetest.</span><span class="sxs-lookup"><span data-stu-id="ece5c-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="ece5c-521">Lisateavet vt teemast [Statistiliste mõõtude pakkuja mall](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="ece5c-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="ece5c-522">Järgmises tabelis on näidatud tulemus, kui HR-teenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="ece5c-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-523">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-523">Cost object</span></span></th>
<th><span data-ttu-id="ece5c-524">Väärtus</span><span class="sxs-lookup"><span data-stu-id="ece5c-524">Magnitude</span></span></th>
<th><span data-ttu-id="ece5c-525">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="ece5c-525">Allocation factor</span></span></th>
<th><span data-ttu-id="ece5c-526">Summa</span><span class="sxs-lookup"><span data-stu-id="ece5c-526">Amount</span></span></th>
<th><span data-ttu-id="ece5c-527">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="ece5c-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-528">CC002</span><span class="sxs-lookup"><span data-stu-id="ece5c-528">CC002</span></span></td>
<td><span data-ttu-id="ece5c-529">Finantsid</span><span class="sxs-lookup"><span data-stu-id="ece5c-529">Finance</span></span></td>
<td><span data-ttu-id="ece5c-530">35</span><span class="sxs-lookup"><span data-stu-id="ece5c-530">35</span></span></td>
<td><span data-ttu-id="ece5c-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ece5c-532">175.00</span><span class="sxs-lookup"><span data-stu-id="ece5c-532">175.00</span></span></td>
<td><span data-ttu-id="ece5c-533">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-534">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-534">CC003</span></span></td>
<td><span data-ttu-id="ece5c-535">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-535">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-536">55</span><span class="sxs-lookup"><span data-stu-id="ece5c-536">55</span></span></td>
<td><span data-ttu-id="ece5c-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ece5c-538">275.00</span><span class="sxs-lookup"><span data-stu-id="ece5c-538">275.00</span></span></td>
<td><span data-ttu-id="ece5c-539">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-540">CC004</span><span class="sxs-lookup"><span data-stu-id="ece5c-540">CC004</span></span></td>
<td><span data-ttu-id="ece5c-541">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="ece5c-541">Packaging</span></span></td>
<td><span data-ttu-id="ece5c-542">10</span><span class="sxs-lookup"><span data-stu-id="ece5c-542">10</span></span></td>
<td><span data-ttu-id="ece5c-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ece5c-544">50,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-544">50.00</span></span></td>
<td><span data-ttu-id="ece5c-545">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-546">CC002</span><span class="sxs-lookup"><span data-stu-id="ece5c-546">CC002</span></span></td>
<td><span data-ttu-id="ece5c-547">Finantsid</span><span class="sxs-lookup"><span data-stu-id="ece5c-547">Finance</span></span></td>
<td><span data-ttu-id="ece5c-548">35</span><span class="sxs-lookup"><span data-stu-id="ece5c-548">35</span></span></td>
<td><span data-ttu-id="ece5c-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="ece5c-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ece5c-550">436.00</span><span class="sxs-lookup"><span data-stu-id="ece5c-550">436.00</span></span></td>
<td><span data-ttu-id="ece5c-551">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-552">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-552">CC003</span></span></td>
<td><span data-ttu-id="ece5c-553">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-553">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-554">55</span><span class="sxs-lookup"><span data-stu-id="ece5c-554">55</span></span></td>
<td><span data-ttu-id="ece5c-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="ece5c-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ece5c-556">685.14</span><span class="sxs-lookup"><span data-stu-id="ece5c-556">685.14</span></span></td>
<td><span data-ttu-id="ece5c-557">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-558">CC004</span><span class="sxs-lookup"><span data-stu-id="ece5c-558">CC004</span></span></td>
<td><span data-ttu-id="ece5c-559">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="ece5c-559">Packaging</span></span></td>
<td><span data-ttu-id="ece5c-560">10</span><span class="sxs-lookup"><span data-stu-id="ece5c-560">10</span></span></td>
<td><span data-ttu-id="ece5c-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="ece5c-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ece5c-562">124.57</span><span class="sxs-lookup"><span data-stu-id="ece5c-562">124.57</span></span></td>
<td><span data-ttu-id="ece5c-563">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ece5c-564">Järgmises tabelis on näidatud tulemus, kui Rahandusteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="ece5c-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-565">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-565">Cost object</span></span></th>
<th><span data-ttu-id="ece5c-566">Väärtus</span><span class="sxs-lookup"><span data-stu-id="ece5c-566">Magnitude</span></span></th>
<th><span data-ttu-id="ece5c-567">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="ece5c-567">Allocation factor</span></span></th>
<th><span data-ttu-id="ece5c-568">Summa</span><span class="sxs-lookup"><span data-stu-id="ece5c-568">Amount</span></span></th>
<th><span data-ttu-id="ece5c-569">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="ece5c-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-570">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-570">CC003</span></span></td>
<td><span data-ttu-id="ece5c-571">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-571">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-572">65</span><span class="sxs-lookup"><span data-stu-id="ece5c-572">65</span></span></td>
<td><span data-ttu-id="ece5c-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="ece5c-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="ece5c-574">438.75</span><span class="sxs-lookup"><span data-stu-id="ece5c-574">438.75</span></span></td>
<td><span data-ttu-id="ece5c-575">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-576">CC004</span><span class="sxs-lookup"><span data-stu-id="ece5c-576">CC004</span></span></td>
<td><span data-ttu-id="ece5c-577">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="ece5c-577">Packaging</span></span></td>
<td><span data-ttu-id="ece5c-578">35</span><span class="sxs-lookup"><span data-stu-id="ece5c-578">35</span></span></td>
<td><span data-ttu-id="ece5c-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="ece5c-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="ece5c-580">236.25</span><span class="sxs-lookup"><span data-stu-id="ece5c-580">236.25</span></span></td>
<td><span data-ttu-id="ece5c-581">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-582">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-582">CC003</span></span></td>
<td><span data-ttu-id="ece5c-583">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-583">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-584">65</span><span class="sxs-lookup"><span data-stu-id="ece5c-584">65</span></span></td>
<td><span data-ttu-id="ece5c-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="ece5c-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="ece5c-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="ece5c-586">5,297.69</span></span></td>
<td><span data-ttu-id="ece5c-587">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-588">CC004</span><span class="sxs-lookup"><span data-stu-id="ece5c-588">CC004</span></span></td>
<td><span data-ttu-id="ece5c-589">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="ece5c-589">Packaging</span></span></td>
<td><span data-ttu-id="ece5c-590">35</span><span class="sxs-lookup"><span data-stu-id="ece5c-590">35</span></span></td>
<td><span data-ttu-id="ece5c-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="ece5c-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="ece5c-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="ece5c-592">2,852.60</span></span></td>
<td><span data-ttu-id="ece5c-593">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ece5c-594">Järgmises tabelis on näidatud tulemus, kui Assembleriteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="ece5c-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-595">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-595">Cost object</span></span></th>
<th><span data-ttu-id="ece5c-596">Väärtus</span><span class="sxs-lookup"><span data-stu-id="ece5c-596">Magnitude</span></span></th>
<th><span data-ttu-id="ece5c-597">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="ece5c-597">Allocation factor</span></span></th>
<th><span data-ttu-id="ece5c-598">Summa</span><span class="sxs-lookup"><span data-stu-id="ece5c-598">Amount</span></span></th>
<th><span data-ttu-id="ece5c-599">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="ece5c-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-600">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-600">Prod 1</span></span></td>
<td><span data-ttu-id="ece5c-601">Toode 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-601">Product 1</span></span></td>
<td><span data-ttu-id="ece5c-602">60</span><span class="sxs-lookup"><span data-stu-id="ece5c-602">60</span></span></td>
<td><span data-ttu-id="ece5c-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="ece5c-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="ece5c-604">535.31</span><span class="sxs-lookup"><span data-stu-id="ece5c-604">535.31</span></span></td>
<td><span data-ttu-id="ece5c-605">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-606">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-606">Prod 2</span></span></td>
<td><span data-ttu-id="ece5c-607">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-607">Product 2</span></span></td>
<td><span data-ttu-id="ece5c-608">20</span><span class="sxs-lookup"><span data-stu-id="ece5c-608">20</span></span></td>
<td><span data-ttu-id="ece5c-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="ece5c-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="ece5c-610">178.44</span><span class="sxs-lookup"><span data-stu-id="ece5c-610">178.44</span></span></td>
<td><span data-ttu-id="ece5c-611">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-612">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-612">Prod 1</span></span></td>
<td><span data-ttu-id="ece5c-613">Toode 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-613">Product 1</span></span></td>
<td><span data-ttu-id="ece5c-614">60</span><span class="sxs-lookup"><span data-stu-id="ece5c-614">60</span></span></td>
<td><span data-ttu-id="ece5c-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="ece5c-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="ece5c-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="ece5c-616">4,487.12</span></span></td>
<td><span data-ttu-id="ece5c-617">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-618">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-618">Prod 2</span></span></td>
<td><span data-ttu-id="ece5c-619">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-619">Product 2</span></span></td>
<td><span data-ttu-id="ece5c-620">20</span><span class="sxs-lookup"><span data-stu-id="ece5c-620">20</span></span></td>
<td><span data-ttu-id="ece5c-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="ece5c-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="ece5c-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="ece5c-622">1,495.71</span></span></td>
<td><span data-ttu-id="ece5c-623">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ece5c-624">Järgmises tabelis on näidatud tulemus, kui Pakendamisteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="ece5c-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-625">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-625">Cost object</span></span></th>
<th><span data-ttu-id="ece5c-626">Väärtus</span><span class="sxs-lookup"><span data-stu-id="ece5c-626">Magnitude</span></span></th>
<th><span data-ttu-id="ece5c-627">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="ece5c-627">Allocation factor</span></span></th>
<th><span data-ttu-id="ece5c-628">Summa</span><span class="sxs-lookup"><span data-stu-id="ece5c-628">Amount</span></span></th>
<th><span data-ttu-id="ece5c-629">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="ece5c-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-630">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-630">Prod 1</span></span></td>
<td><span data-ttu-id="ece5c-631">Toode 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-631">Product 1</span></span></td>
<td><span data-ttu-id="ece5c-632">80</span><span class="sxs-lookup"><span data-stu-id="ece5c-632">80</span></span></td>
<td><span data-ttu-id="ece5c-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="ece5c-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="ece5c-634">241.05</span><span class="sxs-lookup"><span data-stu-id="ece5c-634">241.05</span></span></td>
<td><span data-ttu-id="ece5c-635">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-636">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-636">Prod 2</span></span></td>
<td><span data-ttu-id="ece5c-637">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-637">Product 2</span></span></td>
<td><span data-ttu-id="ece5c-638">15</span><span class="sxs-lookup"><span data-stu-id="ece5c-638">15</span></span></td>
<td><span data-ttu-id="ece5c-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="ece5c-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="ece5c-640">45.20</span><span class="sxs-lookup"><span data-stu-id="ece5c-640">45.20</span></span></td>
<td><span data-ttu-id="ece5c-641">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-642">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-642">Prod 1</span></span></td>
<td><span data-ttu-id="ece5c-643">Toode 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-643">Product 1</span></span></td>
<td><span data-ttu-id="ece5c-644">80</span><span class="sxs-lookup"><span data-stu-id="ece5c-644">80</span></span></td>
<td><span data-ttu-id="ece5c-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="ece5c-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="ece5c-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="ece5c-646">2,507.09</span></span></td>
<td><span data-ttu-id="ece5c-647">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-648">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-648">Prod 2</span></span></td>
<td><span data-ttu-id="ece5c-649">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-649">Product 2</span></span></td>
<td><span data-ttu-id="ece5c-650">15</span><span class="sxs-lookup"><span data-stu-id="ece5c-650">15</span></span></td>
<td><span data-ttu-id="ece5c-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="ece5c-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="ece5c-652">470.08</span><span class="sxs-lookup"><span data-stu-id="ece5c-652">470.08</span></span></td>
<td><span data-ttu-id="ece5c-653">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ece5c-654">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="ece5c-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ece5c-655">Tööleht</span><span class="sxs-lookup"><span data-stu-id="ece5c-655">Journal</span></span></th>
<th><span data-ttu-id="ece5c-656">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="ece5c-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ece5c-657">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="ece5c-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ece5c-658">Versioon</span><span class="sxs-lookup"><span data-stu-id="ece5c-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-659">00004</span><span class="sxs-lookup"><span data-stu-id="ece5c-659">00004</span></span></td>
<td><span data-ttu-id="ece5c-660">Kulueralduse tööleht</span><span class="sxs-lookup"><span data-stu-id="ece5c-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="ece5c-661">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="ece5c-661">Fiscal</span></span></td>
<td><span data-ttu-id="ece5c-662">2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-662">2017</span></span></td>
<td><span data-ttu-id="ece5c-663">Periood 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-663">Period 1</span></span></td>
<td><span data-ttu-id="ece5c-664">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="ece5c-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="ece5c-665">Töölehe read</span><span class="sxs-lookup"><span data-stu-id="ece5c-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ece5c-666">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="ece5c-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ece5c-667">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ece5c-668">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="ece5c-668">Cost element</span></span></th>
<th><span data-ttu-id="ece5c-669">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="ece5c-669">Cost behavior</span></span></th>
<th><span data-ttu-id="ece5c-670">Summa</span><span class="sxs-lookup"><span data-stu-id="ece5c-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-671">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="ece5c-672">CC001</span><span class="sxs-lookup"><span data-stu-id="ece5c-672">CC001</span></span></td>
<td><span data-ttu-id="ece5c-673">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="ece5c-673">HR</span></span></td>
<td><span data-ttu-id="ece5c-674">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-674">10001</span></span></td>
<td><span data-ttu-id="ece5c-675">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-675">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-676">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-676">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-677">500,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-678">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="ece5c-679">CC001</span><span class="sxs-lookup"><span data-stu-id="ece5c-679">CC001</span></span></td>
<td><span data-ttu-id="ece5c-680">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="ece5c-680">HR</span></span></td>
<td><span data-ttu-id="ece5c-681">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-681">10001</span></span></td>
<td><span data-ttu-id="ece5c-682">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-682">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-683">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-683">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="ece5c-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-685">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="ece5c-686">CC002</span><span class="sxs-lookup"><span data-stu-id="ece5c-686">CC002</span></span></td>
<td><span data-ttu-id="ece5c-687">Finantsid</span><span class="sxs-lookup"><span data-stu-id="ece5c-687">Finance</span></span></td>
<td><span data-ttu-id="ece5c-688">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-688">10001</span></span></td>
<td><span data-ttu-id="ece5c-689">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-689">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-690">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-690">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-691">675.00</span><span class="sxs-lookup"><span data-stu-id="ece5c-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-692">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="ece5c-693">CC002</span><span class="sxs-lookup"><span data-stu-id="ece5c-693">CC002</span></span></td>
<td><span data-ttu-id="ece5c-694">Finantsid</span><span class="sxs-lookup"><span data-stu-id="ece5c-694">Finance</span></span></td>
<td><span data-ttu-id="ece5c-695">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-695">10001</span></span></td>
<td><span data-ttu-id="ece5c-696">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-696">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-697">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-697">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="ece5c-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-699">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="ece5c-700">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-700">CC003</span></span></td>
<td><span data-ttu-id="ece5c-701">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-701">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-702">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-702">10001</span></span></td>
<td><span data-ttu-id="ece5c-703">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-703">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-704">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-704">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-705">713.75</span><span class="sxs-lookup"><span data-stu-id="ece5c-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-706">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="ece5c-707">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-707">CC003</span></span></td>
<td><span data-ttu-id="ece5c-708">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-708">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-709">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-709">10001</span></span></td>
<td><span data-ttu-id="ece5c-710">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-710">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-711">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-711">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="ece5c-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-713">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="ece5c-714">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-714">CC003</span></span></td>
<td><span data-ttu-id="ece5c-715">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="ece5c-715">Packaging</span></span></td>
<td><span data-ttu-id="ece5c-716">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-716">10001</span></span></td>
<td><span data-ttu-id="ece5c-717">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-717">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-718">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-718">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-719">286.25</span><span class="sxs-lookup"><span data-stu-id="ece5c-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-720">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="ece5c-721">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-721">CC003</span></span></td>
<td><span data-ttu-id="ece5c-722">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="ece5c-722">Packaging</span></span></td>
<td><span data-ttu-id="ece5c-723">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-723">10001</span></span></td>
<td><span data-ttu-id="ece5c-724">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-724">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-725">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-725">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="ece5c-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-727">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="ece5c-728">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-728">Prod 1</span></span></td>
<td><span data-ttu-id="ece5c-729">Toode 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-729">Product 1</span></span></td>
<td><span data-ttu-id="ece5c-730">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-730">10001</span></span></td>
<td><span data-ttu-id="ece5c-731">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-731">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-732">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-732">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-733">776.36</span><span class="sxs-lookup"><span data-stu-id="ece5c-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-734">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="ece5c-735">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-735">Prod 1</span></span></td>
<td><span data-ttu-id="ece5c-736">Toode 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-736">Product 1</span></span></td>
<td><span data-ttu-id="ece5c-737">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-737">10001</span></span></td>
<td><span data-ttu-id="ece5c-738">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-738">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-739">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-739">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="ece5c-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-741">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="ece5c-742">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-742">Prod 2</span></span></td>
<td><span data-ttu-id="ece5c-743">Toode 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-743">Product 1</span></span></td>
<td><span data-ttu-id="ece5c-744">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-744">10001</span></span></td>
<td><span data-ttu-id="ece5c-745">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-745">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-746">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-746">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-747">223.64</span><span class="sxs-lookup"><span data-stu-id="ece5c-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-748">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="ece5c-749">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-749">Prod 2</span></span></td>
<td><span data-ttu-id="ece5c-750">Toode 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-750">Product 1</span></span></td>
<td><span data-ttu-id="ece5c-751">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-751">10001</span></span></td>
<td><span data-ttu-id="ece5c-752">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-752">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-753">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-753">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="ece5c-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ece5c-755">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="ece5c-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ece5c-756">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ece5c-757">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="ece5c-757">Cost element</span></span></th>
<th><span data-ttu-id="ece5c-758">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="ece5c-758">Cost behavior</span></span></th>
<th><span data-ttu-id="ece5c-759">Summa</span><span class="sxs-lookup"><span data-stu-id="ece5c-759">Amount</span></span></th>
<th><span data-ttu-id="ece5c-760">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="ece5c-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ece5c-761">CC001</span><span class="sxs-lookup"><span data-stu-id="ece5c-761">CC001</span></span></td>
<td><span data-ttu-id="ece5c-762">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="ece5c-762">HR</span></span></td>
<td><span data-ttu-id="ece5c-763">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-763">10001</span></span></td>
<td><span data-ttu-id="ece5c-764">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-764">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-765">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-765">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-766">‑500,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-766">-500.00</span></span></td>
<td><span data-ttu-id="ece5c-767">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-768">CC002</span><span class="sxs-lookup"><span data-stu-id="ece5c-768">CC002</span></span></td>
<td><span data-ttu-id="ece5c-769">Finantsid</span><span class="sxs-lookup"><span data-stu-id="ece5c-769">Finance</span></span></td>
<td><span data-ttu-id="ece5c-770">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-770">10001</span></span></td>
<td><span data-ttu-id="ece5c-771">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-771">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-772">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-772">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-773">175.00</span><span class="sxs-lookup"><span data-stu-id="ece5c-773">175.00</span></span></td>
<td><span data-ttu-id="ece5c-774">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-775">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-775">CC003</span></span></td>
<td><span data-ttu-id="ece5c-776">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-776">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-777">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-777">10001</span></span></td>
<td><span data-ttu-id="ece5c-778">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-778">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-779">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-779">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-780">275.00</span><span class="sxs-lookup"><span data-stu-id="ece5c-780">275.00</span></span></td>
<td><span data-ttu-id="ece5c-781">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-782">CC004</span><span class="sxs-lookup"><span data-stu-id="ece5c-782">CC004</span></span></td>
<td><span data-ttu-id="ece5c-783">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="ece5c-783">Packaging</span></span></td>
<td><span data-ttu-id="ece5c-784">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-784">10001</span></span></td>
<td><span data-ttu-id="ece5c-785">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-785">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-786">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-786">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-787">50,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-787">50,00</span></span></td>
<td><span data-ttu-id="ece5c-788">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-789">CC001</span><span class="sxs-lookup"><span data-stu-id="ece5c-789">CC001</span></span></td>
<td><span data-ttu-id="ece5c-790">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="ece5c-790">HR</span></span></td>
<td><span data-ttu-id="ece5c-791">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-791">10001</span></span></td>
<td><span data-ttu-id="ece5c-792">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-792">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-793">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-793">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-794">–1245,71</span><span class="sxs-lookup"><span data-stu-id="ece5c-794">-1,245.71</span></span></td>
<td><span data-ttu-id="ece5c-795">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-796">CC002</span><span class="sxs-lookup"><span data-stu-id="ece5c-796">CC002</span></span></td>
<td><span data-ttu-id="ece5c-797">Finantsid</span><span class="sxs-lookup"><span data-stu-id="ece5c-797">Finance</span></span></td>
<td><span data-ttu-id="ece5c-798">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-798">10001</span></span></td>
<td><span data-ttu-id="ece5c-799">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-799">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-800">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-800">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-801">436.00</span><span class="sxs-lookup"><span data-stu-id="ece5c-801">436.00</span></span></td>
<td><span data-ttu-id="ece5c-802">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-803">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-803">CC003</span></span></td>
<td><span data-ttu-id="ece5c-804">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-804">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-805">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-805">10001</span></span></td>
<td><span data-ttu-id="ece5c-806">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-806">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-807">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-807">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-808">685.14</span><span class="sxs-lookup"><span data-stu-id="ece5c-808">685.14</span></span></td>
<td><span data-ttu-id="ece5c-809">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-810">CC004</span><span class="sxs-lookup"><span data-stu-id="ece5c-810">CC004</span></span></td>
<td><span data-ttu-id="ece5c-811">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="ece5c-811">Packaging</span></span></td>
<td><span data-ttu-id="ece5c-812">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-812">10001</span></span></td>
<td><span data-ttu-id="ece5c-813">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-813">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-814">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-814">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-815">124.57</span><span class="sxs-lookup"><span data-stu-id="ece5c-815">124.57</span></span></td>
<td><span data-ttu-id="ece5c-816">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-817">CC002</span><span class="sxs-lookup"><span data-stu-id="ece5c-817">CC002</span></span></td>
<td><span data-ttu-id="ece5c-818">Finantsid</span><span class="sxs-lookup"><span data-stu-id="ece5c-818">Finance</span></span></td>
<td><span data-ttu-id="ece5c-819">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-819">10001</span></span></td>
<td><span data-ttu-id="ece5c-820">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-820">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-821">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-821">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-822">–675,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-822">-675.00</span></span></td>
<td><span data-ttu-id="ece5c-823">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-824">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-824">CC003</span></span></td>
<td><span data-ttu-id="ece5c-825">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-825">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-826">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-826">10001</span></span></td>
<td><span data-ttu-id="ece5c-827">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-827">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-828">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-828">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-829">438.75</span><span class="sxs-lookup"><span data-stu-id="ece5c-829">438.75</span></span></td>
<td><span data-ttu-id="ece5c-830">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-831">CC004</span><span class="sxs-lookup"><span data-stu-id="ece5c-831">CC004</span></span></td>
<td><span data-ttu-id="ece5c-832">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="ece5c-832">Packaging</span></span></td>
<td><span data-ttu-id="ece5c-833">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-833">10001</span></span></td>
<td><span data-ttu-id="ece5c-834">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-834">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-835">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-835">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-836">236.25</span><span class="sxs-lookup"><span data-stu-id="ece5c-836">236.25</span></span></td>
<td><span data-ttu-id="ece5c-837">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-838">CC002</span><span class="sxs-lookup"><span data-stu-id="ece5c-838">CC002</span></span></td>
<td><span data-ttu-id="ece5c-839">Finantsid</span><span class="sxs-lookup"><span data-stu-id="ece5c-839">Finance</span></span></td>
<td><span data-ttu-id="ece5c-840">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-840">10001</span></span></td>
<td><span data-ttu-id="ece5c-841">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-841">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-842">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-842">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-843">–8150,29</span><span class="sxs-lookup"><span data-stu-id="ece5c-843">-8,150.29</span></span></td>
<td><span data-ttu-id="ece5c-844">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-845">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-845">CC003</span></span></td>
<td><span data-ttu-id="ece5c-846">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-846">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-847">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-847">10001</span></span></td>
<td><span data-ttu-id="ece5c-848">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-848">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-849">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-849">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="ece5c-850">5,297.69</span></span></td>
<td><span data-ttu-id="ece5c-851">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-852">CC004</span><span class="sxs-lookup"><span data-stu-id="ece5c-852">CC004</span></span></td>
<td><span data-ttu-id="ece5c-853">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="ece5c-853">Packaging</span></span></td>
<td><span data-ttu-id="ece5c-854">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-854">10001</span></span></td>
<td><span data-ttu-id="ece5c-855">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-855">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-856">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-856">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="ece5c-857">2,852.60</span></span></td>
<td><span data-ttu-id="ece5c-858">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-859">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-859">CC003</span></span></td>
<td><span data-ttu-id="ece5c-860">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-860">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-861">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-861">10001</span></span></td>
<td><span data-ttu-id="ece5c-862">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-862">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-863">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-863">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-864">–713,75</span><span class="sxs-lookup"><span data-stu-id="ece5c-864">-713.75</span></span></td>
<td><span data-ttu-id="ece5c-865">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-866">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-866">Prod 1</span></span></td>
<td><span data-ttu-id="ece5c-867">Toode 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-867">Product 1</span></span></td>
<td><span data-ttu-id="ece5c-868">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-868">10001</span></span></td>
<td><span data-ttu-id="ece5c-869">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-869">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-870">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-870">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-871">535.31</span><span class="sxs-lookup"><span data-stu-id="ece5c-871">535.31</span></span></td>
<td><span data-ttu-id="ece5c-872">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-873">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-873">Prod 2</span></span></td>
<td><span data-ttu-id="ece5c-874">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-874">Product 2</span></span></td>
<td><span data-ttu-id="ece5c-875">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-875">10001</span></span></td>
<td><span data-ttu-id="ece5c-876">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-876">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-877">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-877">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-878">178.44</span><span class="sxs-lookup"><span data-stu-id="ece5c-878">178.44</span></span></td>
<td><span data-ttu-id="ece5c-879">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-880">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-880">CC003</span></span></td>
<td><span data-ttu-id="ece5c-881">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-881">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-882">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-882">10001</span></span></td>
<td><span data-ttu-id="ece5c-883">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-883">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-884">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-884">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-885">–5982,83</span><span class="sxs-lookup"><span data-stu-id="ece5c-885">-5,982.83</span></span></td>
<td><span data-ttu-id="ece5c-886">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-887">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-887">Prod 1</span></span></td>
<td><span data-ttu-id="ece5c-888">Toode 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-888">Product 1</span></span></td>
<td><span data-ttu-id="ece5c-889">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-889">10001</span></span></td>
<td><span data-ttu-id="ece5c-890">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-890">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-891">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-891">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="ece5c-892">4,487.12</span></span></td>
<td><span data-ttu-id="ece5c-893">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-894">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-894">Prod 2</span></span></td>
<td><span data-ttu-id="ece5c-895">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-895">Product 2</span></span></td>
<td><span data-ttu-id="ece5c-896">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-896">10001</span></span></td>
<td><span data-ttu-id="ece5c-897">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-897">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-898">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-898">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="ece5c-899">1,495.71</span></span></td>
<td><span data-ttu-id="ece5c-900">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-901">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-901">CC003</span></span></td>
<td><span data-ttu-id="ece5c-902">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-902">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-903">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-903">10001</span></span></td>
<td><span data-ttu-id="ece5c-904">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-904">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-905">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-905">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-906">–286,25</span><span class="sxs-lookup"><span data-stu-id="ece5c-906">-286.25</span></span></td>
<td><span data-ttu-id="ece5c-907">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-908">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-908">Prod 1</span></span></td>
<td><span data-ttu-id="ece5c-909">Toode 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-909">Product 1</span></span></td>
<td><span data-ttu-id="ece5c-910">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-910">10001</span></span></td>
<td><span data-ttu-id="ece5c-911">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-911">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-912">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-912">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-913">241.05</span><span class="sxs-lookup"><span data-stu-id="ece5c-913">241.05</span></span></td>
<td><span data-ttu-id="ece5c-914">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-915">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-915">Prod 2</span></span></td>
<td><span data-ttu-id="ece5c-916">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-916">Product 2</span></span></td>
<td><span data-ttu-id="ece5c-917">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-917">10001</span></span></td>
<td><span data-ttu-id="ece5c-918">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-918">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-919">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-919">Fixed cost</span></span></td>
<td><span data-ttu-id="ece5c-920">45.20</span><span class="sxs-lookup"><span data-stu-id="ece5c-920">45.20</span></span></td>
<td><span data-ttu-id="ece5c-921">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-922">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-922">CC003</span></span></td>
<td><span data-ttu-id="ece5c-923">Assembler</span><span class="sxs-lookup"><span data-stu-id="ece5c-923">Assembly</span></span></td>
<td><span data-ttu-id="ece5c-924">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-924">10001</span></span></td>
<td><span data-ttu-id="ece5c-925">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-925">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-926">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-926">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-927">–2977,17</span><span class="sxs-lookup"><span data-stu-id="ece5c-927">-2,977.17</span></span></td>
<td><span data-ttu-id="ece5c-928">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-929">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-929">Prod 1</span></span></td>
<td><span data-ttu-id="ece5c-930">Toode 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-930">Product 1</span></span></td>
<td><span data-ttu-id="ece5c-931">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-931">10001</span></span></td>
<td><span data-ttu-id="ece5c-932">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-932">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-933">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-933">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="ece5c-934">2,507.09</span></span></td>
<td><span data-ttu-id="ece5c-935">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ece5c-936">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-936">Prod 2</span></span></td>
<td><span data-ttu-id="ece5c-937">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-937">Product 2</span></span></td>
<td><span data-ttu-id="ece5c-938">10001</span><span class="sxs-lookup"><span data-stu-id="ece5c-938">10001</span></span></td>
<td><span data-ttu-id="ece5c-939">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="ece5c-939">Electricity</span></span></td>
<td><span data-ttu-id="ece5c-940">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-940">Variable cost</span></span></td>
<td><span data-ttu-id="ece5c-941">470.08</span><span class="sxs-lookup"><span data-stu-id="ece5c-941">470.08</span></span></td>
<td><span data-ttu-id="ece5c-942">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="ece5c-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="ece5c-943">Lõppsõna</span><span class="sxs-lookup"><span data-stu-id="ece5c-943">Conclusion</span></span>
<span data-ttu-id="ece5c-944">Finantsaruandluses sisestatakse elektrikulu 10 000,00 fiktiivse kulukeskuse ID-le.</span><span class="sxs-lookup"><span data-stu-id="ece5c-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="ece5c-945">Nii teavad kuluarvestajad, et see kulu tuleb eraldada.</span><span class="sxs-lookup"><span data-stu-id="ece5c-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="ece5c-946">Kuluarvestuses liigub kulu rakendatud poliitikate ja reeglite põhjal läbi organisatsiooniüksuste ja -tasemete.</span><span class="sxs-lookup"><span data-stu-id="ece5c-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="ece5c-947">Iga kulu on seostatud eraldamisalusega, mis pakub kulude eraldamiseks parimat hinnangut.</span><span class="sxs-lookup"><span data-stu-id="ece5c-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="ece5c-948">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="ece5c-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="ece5c-949">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="ece5c-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="ece5c-950">Kokku</span><span class="sxs-lookup"><span data-stu-id="ece5c-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ece5c-951">CC099</span><span class="sxs-lookup"><span data-stu-id="ece5c-951">CC099</span></span></th>
<th><span data-ttu-id="ece5c-952">CC001</span><span class="sxs-lookup"><span data-stu-id="ece5c-952">CC001</span></span></th>
<th><span data-ttu-id="ece5c-953">CC002</span><span class="sxs-lookup"><span data-stu-id="ece5c-953">CC002</span></span></th>
<th><span data-ttu-id="ece5c-954">CC003</span><span class="sxs-lookup"><span data-stu-id="ece5c-954">CC003</span></span></th>
<th><span data-ttu-id="ece5c-955">CC004</span><span class="sxs-lookup"><span data-stu-id="ece5c-955">CC004</span></span></th>
<th><span data-ttu-id="ece5c-956">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-956">Proj 1</span></span></th>
<th><span data-ttu-id="ece5c-957">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-957">Proj 2</span></span></th>
<th><span data-ttu-id="ece5c-958">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="ece5c-958">Prod 1</span></span></th>
<th><span data-ttu-id="ece5c-959">Toode 2</span><span class="sxs-lookup"><span data-stu-id="ece5c-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="ece5c-960">10001 Elekter</span><span class="sxs-lookup"><span data-stu-id="ece5c-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="ece5c-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="ece5c-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="ece5c-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="ece5c-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="ece5c-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="ece5c-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="ece5c-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="ece5c-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="ece5c-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="ece5c-970">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="ece5c-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-971">0,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="ece5c-972">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-973">0,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-974">0,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-975">0,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-976">0,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-977">0,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-978">776.36</span><span class="sxs-lookup"><span data-stu-id="ece5c-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-979">223.64</span><span class="sxs-lookup"><span data-stu-id="ece5c-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="ece5c-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="ece5c-981">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="ece5c-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-982">000</span><span class="sxs-lookup"><span data-stu-id="ece5c-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-983">0,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-984">0,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-985">0,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-986">0,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-987">30,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-988">10,00</span><span class="sxs-lookup"><span data-stu-id="ece5c-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="ece5c-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="ece5c-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ece5c-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="ece5c-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ece5c-992">Selles teemas selgitatakse, kuidas esmane kuluelement, 10001 Eleter, liigub läbi kuluobjektide.</span><span class="sxs-lookup"><span data-stu-id="ece5c-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="ece5c-993">Seega eraldatakse see üldkulu organisatsiooni madalaimale tasemele.</span><span class="sxs-lookup"><span data-stu-id="ece5c-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="ece5c-994">Teisisõnu kannavad kulu madalaimal tasemel olevad kuluobjektid.</span><span class="sxs-lookup"><span data-stu-id="ece5c-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="ece5c-995">Kui soovite saada kuluobjektide vahelisest kuluvoost visuaalset ülevaadet, saate kuluvoo visualiseerimiseks kasutada kulude kokkuvõtte poliitika reegleid.</span><span class="sxs-lookup"><span data-stu-id="ece5c-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="ece5c-996">Lisateavet vt teemast [Kulukomplekti poliitika ja üldkulude arvutus](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="ece5c-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



