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
ms.openlocfilehash: 6c045f82f3288dba193721dd80c90e68750af9a7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177362"
---
# <a name="overhead-calculation"></a><span data-ttu-id="b6249-103">Üldkulude arvutus</span><span class="sxs-lookup"><span data-stu-id="b6249-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6249-104">Selles teemas kirjeldatakse tüüpilisi üldkulude arvutamise ja eraldamise protsesse.</span><span class="sxs-lookup"><span data-stu-id="b6249-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="b6249-105">Mõiste määratlus</span><span class="sxs-lookup"><span data-stu-id="b6249-105">Term definition</span></span>
---------------

<span data-ttu-id="b6249-106">Üldkulud on kulud, mis kaasnevad ettevõtte käitamisega, kuid mida ei saa seostada otseselt ühegi kindla äritegevuse, toote ega teenusega.</span><span class="sxs-lookup"><span data-stu-id="b6249-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="b6249-107">Üldkulud pakuvad kriitilist tuge kasumit andavate tegevuste loomisele.</span><span class="sxs-lookup"><span data-stu-id="b6249-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="b6249-108">Siin on mõned näited üldkuludest.</span><span class="sxs-lookup"><span data-stu-id="b6249-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="b6249-109">Üür</span><span class="sxs-lookup"><span data-stu-id="b6249-109">Rent</span></span>
-   <span data-ttu-id="b6249-110">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-110">Electricity</span></span>
-   <span data-ttu-id="b6249-111">Haldustasud</span><span class="sxs-lookup"><span data-stu-id="b6249-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="b6249-112">Üldkulude arvutuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="b6249-112">Overhead calculation overview</span></span>
<span data-ttu-id="b6249-113">Üldkulude arvutus käitab kuluarvutuse poliitikaid õiges järjekorras.</span><span class="sxs-lookup"><span data-stu-id="b6249-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="b6249-114">Saate käivitada üldkulude arvutuse sama rahandusperioodi kohta mitu korda, kui kuluarvestuse poliitikaid on muudetud või tuvastatud teatud tõrked.</span><span class="sxs-lookup"><span data-stu-id="b6249-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="b6249-115">Iga üldkulude arvutamise käitamine talletatakse ja see saab kordumatu versiooni-ID, mis võimaldab teil arvutuste erinevaid versioone võrrelda.</span><span class="sxs-lookup"><span data-stu-id="b6249-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="b6249-116">Ülekulude arvutusega loodud kulukirjed saavad aruandluskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="b6249-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="b6249-117">See aruandluskuupäev vastab arvutuses kasutatud rahandusperioodi lõppkuupäevale.</span><span class="sxs-lookup"><span data-stu-id="b6249-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="b6249-118">Kordumatu versiooni-ID koosneb järgmistest elementidest.</span><span class="sxs-lookup"><span data-stu-id="b6249-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="b6249-119">Versiooni tüüp</span><span class="sxs-lookup"><span data-stu-id="b6249-119">Version type</span></span>
-   <span data-ttu-id="b6249-120">Kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="b6249-120">Date and time</span></span>
-   <span data-ttu-id="b6249-121">Kuluarvestuse pearaamat</span><span class="sxs-lookup"><span data-stu-id="b6249-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="b6249-122">Finantsaasta</span><span class="sxs-lookup"><span data-stu-id="b6249-122">Fiscal year</span></span>
-   <span data-ttu-id="b6249-123">Rahandusperiood</span><span class="sxs-lookup"><span data-stu-id="b6249-123">Fiscal period</span></span>

<span data-ttu-id="b6249-124">Üldkulude arvutus käivitatakse versioonist sõltumatult.</span><span class="sxs-lookup"><span data-stu-id="b6249-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="b6249-125">Seetõttu saate arvutada eelarveversiooni enne tegelikku versiooni.</span><span class="sxs-lookup"><span data-stu-id="b6249-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="b6249-126">Üldkulude arvutus koosneb neljast etapist, nagu näha alltoodud joonisel.</span><span class="sxs-lookup"><span data-stu-id="b6249-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="b6249-127">Igas etapis luuakse töölehe päis, millel on töölehe kanded.</span><span class="sxs-lookup"><span data-stu-id="b6249-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="b6249-128">See töölehe päis säiiltab sisendandmeid iga arvutusetapi kohta.</span><span class="sxs-lookup"><span data-stu-id="b6249-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="b6249-129">Igale töölehe reale rakendatakse poliitikad ja reeglid ning väljundina luuakse kulukirjed.</span><span class="sxs-lookup"><span data-stu-id="b6249-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="b6249-130">Seega on teil alati olemas põhjalik ülevaade.</span><span class="sxs-lookup"><span data-stu-id="b6249-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="b6249-131">[![Üldkulude arvutus](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="b6249-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="b6249-132">Elektri üldkulude arvutamine ja eraldamine</span><span class="sxs-lookup"><span data-stu-id="b6249-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="b6249-133">Finantsaruandluses on mõned kulud, näiteks elekter, registreeritud põhisummana.</span><span class="sxs-lookup"><span data-stu-id="b6249-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="b6249-134">Seetõttu ei pakuta kuluarvestuseks üksikasjalikku juhtimisülevaadet.</span><span class="sxs-lookup"><span data-stu-id="b6249-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="b6249-135">Kuluarvestuses peavad kulud liikuma läbi organisatsiooniüksuste, et pakkuda korrektset juhtimisülevaadet kõigi organisatsiooniüksuste ja -tasemete kohta.</span><span class="sxs-lookup"><span data-stu-id="b6249-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="b6249-136">See voog peab põhinema tarbimise või õiglase hindamise täpsel kirjendamisel.</span><span class="sxs-lookup"><span data-stu-id="b6249-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="b6249-137">Pearaamatus, saab elektrikulu sisestada nii, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="b6249-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b6249-138">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b6249-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b6249-139">Kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b6249-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="b6249-140">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="b6249-140">Main account</span></span></th>
<th><span data-ttu-id="b6249-141">Summa arvestusvaluutas</span><span class="sxs-lookup"><span data-stu-id="b6249-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-142">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="b6249-143">CC099</span><span class="sxs-lookup"><span data-stu-id="b6249-143">CC099</span></span></td>
<td><span data-ttu-id="b6249-144">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b6249-144">Default cost center</span></span></td>
<td><span data-ttu-id="b6249-145">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-145">10001</span></span></td>
<td><span data-ttu-id="b6249-146">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-146">Electricity</span></span></td>
<td><span data-ttu-id="b6249-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="b6249-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="b6249-148">1. etapp: kulukäitumise arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="b6249-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="b6249-149">Vaikimisi saavad lähteandmetest imporditud kulukirjed kuluarvestuses kulukäitumise klassifikatsiooniks **Klassifitseerimata**.</span><span class="sxs-lookup"><span data-stu-id="b6249-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="b6249-150">Kulukäitumise poliitikareegleid rakendades saate kulukirjed ümber klassifitseerida kui **Fikseeritud kulu** või **Muutuvkulu**.</span><span class="sxs-lookup"><span data-stu-id="b6249-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="b6249-151">Kulukäitumise reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="b6249-151">Define the cost behavior rule</span></span>

<span data-ttu-id="b6249-152">Mõnikord on osa kulust fikseeritud tasu ja järelejäänud kulu põhineb tarbimisel.</span><span class="sxs-lookup"><span data-stu-id="b6249-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="b6249-153">Elektriarved vastavad sageli sellele määratlusele.</span><span class="sxs-lookup"><span data-stu-id="b6249-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="b6249-154">Pärast kindla fikseeritud tasu maksmist maksate tarbimise eest kilovatt-tunni (Kwh) kohta.</span><span class="sxs-lookup"><span data-stu-id="b6249-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="b6249-155">Näiteks kui fikseeritud kulu tasu on 1000,00 eurot, määratletakse kulukäitumise reegel järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b6249-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="b6249-156">Fikseeritud summa: 1000,00</span><span class="sxs-lookup"><span data-stu-id="b6249-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="b6249-157">0 &lt;= 1000,00 = fikseeritud</span><span class="sxs-lookup"><span data-stu-id="b6249-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="b6249-158">1000,01 &lt; N = muutuja</span><span class="sxs-lookup"><span data-stu-id="b6249-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="b6249-159">Tööleht</span><span class="sxs-lookup"><span data-stu-id="b6249-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b6249-160">Tööleht</span><span class="sxs-lookup"><span data-stu-id="b6249-160">Journal</span></span></th>
<th><span data-ttu-id="b6249-161">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="b6249-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b6249-162">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="b6249-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b6249-163">Versioon</span><span class="sxs-lookup"><span data-stu-id="b6249-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-164">00001</span><span class="sxs-lookup"><span data-stu-id="b6249-164">00001</span></span></td>
<td><span data-ttu-id="b6249-165">Kulukäitumise arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="b6249-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="b6249-166">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="b6249-166">Fiscal</span></span></td>
<td><span data-ttu-id="b6249-167">2017</span><span class="sxs-lookup"><span data-stu-id="b6249-167">2017</span></span></td>
<td><span data-ttu-id="b6249-168">Periood 1</span><span class="sxs-lookup"><span data-stu-id="b6249-168">Period 1</span></span></td>
<td><span data-ttu-id="b6249-169">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="b6249-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b6249-170">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="b6249-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b6249-171">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b6249-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b6249-172">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b6249-173">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b6249-173">Cost element</span></span></th>
<th><span data-ttu-id="b6249-174">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b6249-174">Cost behavior</span></span></th>
<th><span data-ttu-id="b6249-175">Summa</span><span class="sxs-lookup"><span data-stu-id="b6249-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-176">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="b6249-177">CC099</span><span class="sxs-lookup"><span data-stu-id="b6249-177">CC099</span></span></td>
<td><span data-ttu-id="b6249-178">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b6249-178">Default cost center</span></span></td>
<td><span data-ttu-id="b6249-179">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-179">10001</span></span></td>
<td><span data-ttu-id="b6249-180">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-180">Electricity</span></span></td>
<td><span data-ttu-id="b6249-181">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="b6249-181">Unclassified</span></span></td>
<td><span data-ttu-id="b6249-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="b6249-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b6249-183">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="b6249-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-184">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b6249-185">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b6249-185">Cost element</span></span></th>
<th><span data-ttu-id="b6249-186">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b6249-186">Cost behavior</span></span></th>
<th><span data-ttu-id="b6249-187">Summa</span><span class="sxs-lookup"><span data-stu-id="b6249-187">Amount</span></span></th>
<th><span data-ttu-id="b6249-188">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b6249-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-189">CC099</span><span class="sxs-lookup"><span data-stu-id="b6249-189">CC099</span></span></td>
<td><span data-ttu-id="b6249-190">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b6249-190">Default cost center</span></span></td>
<td><span data-ttu-id="b6249-191">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-191">10001</span></span></td>
<td><span data-ttu-id="b6249-192">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-192">Electricity</span></span></td>
<td><span data-ttu-id="b6249-193">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="b6249-193">Unclassified</span></span></td>
<td><span data-ttu-id="b6249-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="b6249-194">10,000.00</span></span></td>
<td><span data-ttu-id="b6249-195">3. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-196">CC099</span><span class="sxs-lookup"><span data-stu-id="b6249-196">CC099</span></span></td>
<td><span data-ttu-id="b6249-197">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b6249-197">Default cost center</span></span></td>
<td><span data-ttu-id="b6249-198">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-198">10001</span></span></td>
<td><span data-ttu-id="b6249-199">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-199">Electricity</span></span></td>
<td><span data-ttu-id="b6249-200">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="b6249-200">Unclassified</span></span></td>
<td><span data-ttu-id="b6249-201">–10 000,00</span><span class="sxs-lookup"><span data-stu-id="b6249-201">-10,000.00</span></span></td>
<td><span data-ttu-id="b6249-202">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-203">CC099</span><span class="sxs-lookup"><span data-stu-id="b6249-203">CC099</span></span></td>
<td><span data-ttu-id="b6249-204">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b6249-204">Default cost center</span></span></td>
<td><span data-ttu-id="b6249-205">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-205">10001</span></span></td>
<td><span data-ttu-id="b6249-206">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-206">Electricity</span></span></td>
<td><span data-ttu-id="b6249-207">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-207">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-208">1 000,00</span><span class="sxs-lookup"><span data-stu-id="b6249-208">1,000.00</span></span></td>
<td><span data-ttu-id="b6249-209">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-210">CC099</span><span class="sxs-lookup"><span data-stu-id="b6249-210">CC099</span></span></td>
<td><span data-ttu-id="b6249-211">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b6249-211">Default cost center</span></span></td>
<td><span data-ttu-id="b6249-212">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-212">10001</span></span></td>
<td><span data-ttu-id="b6249-213">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-213">Electricity</span></span></td>
<td><span data-ttu-id="b6249-214">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-214">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="b6249-215">9,000.00</span></span></td>
<td><span data-ttu-id="b6249-216">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b6249-217">Lisateavet vt teemast [Kulukäitumise poliitika loomine ja määramine kulujuhtimisüksusele (tegevuse juhis)](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="b6249-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="b6249-218">2. etapp: kulujaotuse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="b6249-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="b6249-219">Kulujaotust kasutatakse kulu ümberjaotamiseks ühelt kuluobjektilt ühele või mitmele teisele kuluobjektile, rakendades asjakohast eraldusalust.</span><span class="sxs-lookup"><span data-stu-id="b6249-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="b6249-220">Kulujaotus ja kulueraldus erinevad selle poolest, et kulujaotus toimub alati algse kulu esmase kuluelemendi tasemel.</span><span class="sxs-lookup"><span data-stu-id="b6249-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="b6249-221">Kulujaotuse reegli määratlemine</span><span class="sxs-lookup"><span data-stu-id="b6249-221">Define the cost distribution rule</span></span>

<span data-ttu-id="b6249-222">Finantsaruandluses registreeritakse elektrikulud sageli põhisummana.</span><span class="sxs-lookup"><span data-stu-id="b6249-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="b6249-223">Kuluarvestuseses ei ole see lähenemine piisavalt üksikasjalik.</span><span class="sxs-lookup"><span data-stu-id="b6249-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="b6249-224">Muutuvkulu tuleb jaotada üksikutele kuluobjektidele õigluse alusel.</span><span class="sxs-lookup"><span data-stu-id="b6249-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="b6249-225">Kõige loogilisem eraldamisalus on elektritarbimine (kWh).</span><span class="sxs-lookup"><span data-stu-id="b6249-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="b6249-226">Luuakse statistilise dimensiooni liige nimega Elekter ja elektritarbimine on kirjendatakse.</span><span class="sxs-lookup"><span data-stu-id="b6249-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="b6249-227">Vaikimisi muutuvad kõik statistilise dimensiooni liikmed eraldamisalusena kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="b6249-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-228">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-228">Cost object</span></span></th>
<th><span data-ttu-id="b6249-229">kWh</span><span class="sxs-lookup"><span data-stu-id="b6249-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-230">CC001</span><span class="sxs-lookup"><span data-stu-id="b6249-230">CC001</span></span></td>
<td><span data-ttu-id="b6249-231">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b6249-231">HR</span></span></td>
<td><span data-ttu-id="b6249-232">1000</span><span class="sxs-lookup"><span data-stu-id="b6249-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-233">CC002</span><span class="sxs-lookup"><span data-stu-id="b6249-233">CC002</span></span></td>
<td><span data-ttu-id="b6249-234">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b6249-234">Finance</span></span></td>
<td><span data-ttu-id="b6249-235">6,000</span><span class="sxs-lookup"><span data-stu-id="b6249-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-236">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-236">CC003</span></span></td>
<td><span data-ttu-id="b6249-237">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-237">Assembly</span></span></td>
<td><span data-ttu-id="b6249-238">0</span><span class="sxs-lookup"><span data-stu-id="b6249-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b6249-239">Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="b6249-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-240">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-240">Cost object</span></span></th>
<th><span data-ttu-id="b6249-241">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b6249-241">Magnitude</span></span></th>
<th><span data-ttu-id="b6249-242">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="b6249-242">Allocation factor</span></span></th>
<th><span data-ttu-id="b6249-243">Summa</span><span class="sxs-lookup"><span data-stu-id="b6249-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-244">CC001</span><span class="sxs-lookup"><span data-stu-id="b6249-244">CC001</span></span></td>
<td><span data-ttu-id="b6249-245">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b6249-245">HR</span></span></td>
<td><span data-ttu-id="b6249-246">1000</span><span class="sxs-lookup"><span data-stu-id="b6249-246">1,000</span></span></td>
<td><span data-ttu-id="b6249-247">(1000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="b6249-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b6249-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="b6249-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-249">CC002</span><span class="sxs-lookup"><span data-stu-id="b6249-249">CC002</span></span></td>
<td><span data-ttu-id="b6249-250">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b6249-250">Finance</span></span></td>
<td><span data-ttu-id="b6249-251">6,000</span><span class="sxs-lookup"><span data-stu-id="b6249-251">6,000</span></span></td>
<td><span data-ttu-id="b6249-252">(6000 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="b6249-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b6249-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="b6249-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-254">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-254">CC003</span></span></td>
<td><span data-ttu-id="b6249-255">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-255">Assembly</span></span></td>
<td><span data-ttu-id="b6249-256">0</span><span class="sxs-lookup"><span data-stu-id="b6249-256">0</span></span></td>
<td><span data-ttu-id="b6249-257">(0 ÷ 7000) × 9000,00</span><span class="sxs-lookup"><span data-stu-id="b6249-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b6249-258">0,00</span><span class="sxs-lookup"><span data-stu-id="b6249-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b6249-259">Fikseeritud kulu tuleb jaotada ühtlaselt üksikutele kuluobjektidele, mis on tarbinud elektrit.</span><span class="sxs-lookup"><span data-stu-id="b6249-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="b6249-260">Selle tulemuse saate, kasutades valemi eraldamisaluses statistilise dimensiooni liiget Elekter: (Elekter &gt; 0,00). Järgmises tabelis on näidatud tulemus, kui elektritarbimist rakendatakse muutuvkulude puhul eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="b6249-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-261">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-261">Cost object</span></span></th>
<th><span data-ttu-id="b6249-262">Valem</span><span class="sxs-lookup"><span data-stu-id="b6249-262">Formula</span></span></th>
<th><span data-ttu-id="b6249-263">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b6249-263">Magnitude</span></span></th>
<th><span data-ttu-id="b6249-264">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="b6249-264">Allocation factor</span></span></th>
<th><span data-ttu-id="b6249-265">Summa</span><span class="sxs-lookup"><span data-stu-id="b6249-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-266">CC001</span><span class="sxs-lookup"><span data-stu-id="b6249-266">CC001</span></span></td>
<td><span data-ttu-id="b6249-267">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b6249-267">HR</span></span></td>
<td><span data-ttu-id="b6249-268">(1000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b6249-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b6249-269">1</span><span class="sxs-lookup"><span data-stu-id="b6249-269">1</span></span></td>
<td><span data-ttu-id="b6249-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b6249-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b6249-271">500,00</span><span class="sxs-lookup"><span data-stu-id="b6249-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-272">CC002</span><span class="sxs-lookup"><span data-stu-id="b6249-272">CC002</span></span></td>
<td><span data-ttu-id="b6249-273">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b6249-273">Finance</span></span></td>
<td><span data-ttu-id="b6249-274">(6000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b6249-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b6249-275">1</span><span class="sxs-lookup"><span data-stu-id="b6249-275">1</span></span></td>
<td><span data-ttu-id="b6249-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b6249-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b6249-277">500,00</span><span class="sxs-lookup"><span data-stu-id="b6249-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-278">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-278">CC003</span></span></td>
<td><span data-ttu-id="b6249-279">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-279">Assembly</span></span></td>
<td><span data-ttu-id="b6249-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b6249-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b6249-281">0</span><span class="sxs-lookup"><span data-stu-id="b6249-281">0</span></span></td>
<td><span data-ttu-id="b6249-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b6249-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b6249-283">0,00</span><span class="sxs-lookup"><span data-stu-id="b6249-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="b6249-284">Tööleht</span><span class="sxs-lookup"><span data-stu-id="b6249-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b6249-285">Tööleht</span><span class="sxs-lookup"><span data-stu-id="b6249-285">Journal</span></span></th>
<th><span data-ttu-id="b6249-286">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="b6249-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b6249-287">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="b6249-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b6249-288">Versioon</span><span class="sxs-lookup"><span data-stu-id="b6249-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-289">00002</span><span class="sxs-lookup"><span data-stu-id="b6249-289">00002</span></span></td>
<td><span data-ttu-id="b6249-290">Kulujaotuse arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="b6249-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="b6249-291">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="b6249-291">Fiscal</span></span></td>
<td><span data-ttu-id="b6249-292">2017</span><span class="sxs-lookup"><span data-stu-id="b6249-292">2017</span></span></td>
<td><span data-ttu-id="b6249-293">Periood 1</span><span class="sxs-lookup"><span data-stu-id="b6249-293">Period 1</span></span></td>
<td><span data-ttu-id="b6249-294">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="b6249-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b6249-295">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="b6249-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b6249-296">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b6249-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b6249-297">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b6249-298">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b6249-298">Cost element</span></span></th>
<th><span data-ttu-id="b6249-299">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b6249-299">Cost behavior</span></span></th>
<th><span data-ttu-id="b6249-300">Summa</span><span class="sxs-lookup"><span data-stu-id="b6249-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-301">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="b6249-302">CC099</span><span class="sxs-lookup"><span data-stu-id="b6249-302">CC099</span></span></td>
<td><span data-ttu-id="b6249-303">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b6249-303">Default cost center</span></span></td>
<td><span data-ttu-id="b6249-304">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-304">10001</span></span></td>
<td><span data-ttu-id="b6249-305">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-305">Electricity</span></span></td>
<td><span data-ttu-id="b6249-306">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-306">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-307">1 000,00</span><span class="sxs-lookup"><span data-stu-id="b6249-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-308">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="b6249-309">CC099</span><span class="sxs-lookup"><span data-stu-id="b6249-309">CC099</span></span></td>
<td><span data-ttu-id="b6249-310">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b6249-310">Default cost center</span></span></td>
<td><span data-ttu-id="b6249-311">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-311">10001</span></span></td>
<td><span data-ttu-id="b6249-312">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-312">Electricity</span></span></td>
<td><span data-ttu-id="b6249-313">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-313">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="b6249-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b6249-315">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="b6249-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-316">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b6249-317">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b6249-317">Cost element</span></span></th>
<th><span data-ttu-id="b6249-318">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b6249-318">Cost behavior</span></span></th>
<th><span data-ttu-id="b6249-319">Summa</span><span class="sxs-lookup"><span data-stu-id="b6249-319">Amount</span></span></th>
<th><span data-ttu-id="b6249-320">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b6249-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-321">CC099</span><span class="sxs-lookup"><span data-stu-id="b6249-321">CC099</span></span></td>
<td><span data-ttu-id="b6249-322">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b6249-322">Default cost center</span></span></td>
<td><span data-ttu-id="b6249-323">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-323">10001</span></span></td>
<td><span data-ttu-id="b6249-324">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-324">Electricity</span></span></td>
<td><span data-ttu-id="b6249-325">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-325">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-326">–1000,00</span><span class="sxs-lookup"><span data-stu-id="b6249-326">-1,000.00</span></span></td>
<td><span data-ttu-id="b6249-327">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-328">CC001</span><span class="sxs-lookup"><span data-stu-id="b6249-328">CC001</span></span></td>
<td><span data-ttu-id="b6249-329">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b6249-329">HR</span></span></td>
<td><span data-ttu-id="b6249-330">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-330">10001</span></span></td>
<td><span data-ttu-id="b6249-331">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-331">Electricity</span></span></td>
<td><span data-ttu-id="b6249-332">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-332">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-333">500,00</span><span class="sxs-lookup"><span data-stu-id="b6249-333">500.00</span></span></td>
<td><span data-ttu-id="b6249-334">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-335">CC002</span><span class="sxs-lookup"><span data-stu-id="b6249-335">CC002</span></span></td>
<td><span data-ttu-id="b6249-336">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b6249-336">Finance</span></span></td>
<td><span data-ttu-id="b6249-337">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-337">10001</span></span></td>
<td><span data-ttu-id="b6249-338">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-338">Electricity</span></span></td>
<td><span data-ttu-id="b6249-339">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-339">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-340">500,00</span><span class="sxs-lookup"><span data-stu-id="b6249-340">500.00</span></span></td>
<td><span data-ttu-id="b6249-341">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-342">CC099</span><span class="sxs-lookup"><span data-stu-id="b6249-342">CC099</span></span></td>
<td><span data-ttu-id="b6249-343">Vaike-kulukeskus</span><span class="sxs-lookup"><span data-stu-id="b6249-343">Default cost center</span></span></td>
<td><span data-ttu-id="b6249-344">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-344">10001</span></span></td>
<td><span data-ttu-id="b6249-345">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-345">Electricity</span></span></td>
<td><span data-ttu-id="b6249-346">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-346">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-347">–9000,00</span><span class="sxs-lookup"><span data-stu-id="b6249-347">-9,000.00</span></span></td>
<td><span data-ttu-id="b6249-348">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-349">CC001</span><span class="sxs-lookup"><span data-stu-id="b6249-349">CC001</span></span></td>
<td><span data-ttu-id="b6249-350">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b6249-350">HR</span></span></td>
<td><span data-ttu-id="b6249-351">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-351">10001</span></span></td>
<td><span data-ttu-id="b6249-352">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-352">Electricity</span></span></td>
<td><span data-ttu-id="b6249-353">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-353">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="b6249-354">1,285.71</span></span></td>
<td><span data-ttu-id="b6249-355">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-356">CC002</span><span class="sxs-lookup"><span data-stu-id="b6249-356">CC002</span></span></td>
<td><span data-ttu-id="b6249-357">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b6249-357">Finance</span></span></td>
<td><span data-ttu-id="b6249-358">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-358">10001</span></span></td>
<td><span data-ttu-id="b6249-359">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-359">Electricity</span></span></td>
<td><span data-ttu-id="b6249-360">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-360">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="b6249-361">7,714.29</span></span></td>
<td><span data-ttu-id="b6249-362">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b6249-363">Lisateavet vt teemast [Kulujaotise poliitika loomine ja määramine kulujuhtimisüksusele (tegevuse juhis)](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="b6249-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="b6249-364">3. etapp: üldkulude määra arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="b6249-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="b6249-365">Üldkulude määra kasutatakse ühe või mitme kindla kuluobjekti debiteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="b6249-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="b6249-366">Tasu põhineb eelmääratud kulumääral ja väärtusel määratud eraldamisalusest.</span><span class="sxs-lookup"><span data-stu-id="b6249-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="b6249-367">Üldkulu määra määratlemine</span><span class="sxs-lookup"><span data-stu-id="b6249-367">Define the overhead rate</span></span>

<span data-ttu-id="b6249-368">Kuluobjekt CC001 inimressursid panustab sisemiste projektide kogumisse.</span><span class="sxs-lookup"><span data-stu-id="b6249-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="b6249-369">Luuakse statistilise dimensiooni liige nimega Inimressursside projektid, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="b6249-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-370">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-370">Cost object</span></span></th>
<th><span data-ttu-id="b6249-371">Tunnid</span><span class="sxs-lookup"><span data-stu-id="b6249-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-372">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="b6249-372">Proj 1</span></span></td>
<td><span data-ttu-id="b6249-373">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="b6249-373">Project 1</span></span></td>
<td><span data-ttu-id="b6249-374">3</span><span class="sxs-lookup"><span data-stu-id="b6249-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-375">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="b6249-375">Proj 2</span></span></td>
<td><span data-ttu-id="b6249-376">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="b6249-376">Project 2</span></span></td>
<td><span data-ttu-id="b6249-377">1</span><span class="sxs-lookup"><span data-stu-id="b6249-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b6249-378">Määratletud on eelmääratud kulumäär kuluprojektide panusele.</span><span class="sxs-lookup"><span data-stu-id="b6249-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-379">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-379">Cost object</span></span></th>
<th><span data-ttu-id="b6249-380">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b6249-380">Cost element</span></span></th>
<th><span data-ttu-id="b6249-381">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b6249-381">Cost behavior</span></span></th>
<th><span data-ttu-id="b6249-382">Ühikud</span><span class="sxs-lookup"><span data-stu-id="b6249-382">Units</span></span></th>
<th><span data-ttu-id="b6249-383">Kurss</span><span class="sxs-lookup"><span data-stu-id="b6249-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-384">CC001</span><span class="sxs-lookup"><span data-stu-id="b6249-384">CC001</span></span></td>
<td><span data-ttu-id="b6249-385">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b6249-385">HR</span></span></td>
<td><span data-ttu-id="b6249-386">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-386">10001</span></span></td>
<td><span data-ttu-id="b6249-387">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-387">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-388">1</span><span class="sxs-lookup"><span data-stu-id="b6249-388">1</span></span></td>
<td><span data-ttu-id="b6249-389">10</span><span class="sxs-lookup"><span data-stu-id="b6249-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b6249-390">Järgmises tabelis on näidatud tulemus, kui inimressursside projektid on rakendatud eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="b6249-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-391">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-391">Cost object</span></span></th>
<th><span data-ttu-id="b6249-392">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b6249-392">Magnitude</span></span></th>
<th><span data-ttu-id="b6249-393">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b6249-393">Cost element</span></span></th>
<th><span data-ttu-id="b6249-394">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="b6249-394">Allocation factor</span></span></th>
<th><span data-ttu-id="b6249-395">Summa</span><span class="sxs-lookup"><span data-stu-id="b6249-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-396">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="b6249-396">Proj 1</span></span></td>
<td><span data-ttu-id="b6249-397">Projekt 1</span><span class="sxs-lookup"><span data-stu-id="b6249-397">Project 1</span></span></td>
<td><span data-ttu-id="b6249-398">3</span><span class="sxs-lookup"><span data-stu-id="b6249-398">3</span></span></td>
<td><span data-ttu-id="b6249-399">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-399">10001</span></span></td>
<td><span data-ttu-id="b6249-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="b6249-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="b6249-401">30,00</span><span class="sxs-lookup"><span data-stu-id="b6249-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-402">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="b6249-402">Proj 2</span></span></td>
<td><span data-ttu-id="b6249-403">Projekt 2</span><span class="sxs-lookup"><span data-stu-id="b6249-403">Project 2</span></span></td>
<td><span data-ttu-id="b6249-404">1</span><span class="sxs-lookup"><span data-stu-id="b6249-404">1</span></span></td>
<td><span data-ttu-id="b6249-405">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-405">10001</span></span></td>
<td><span data-ttu-id="b6249-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="b6249-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="b6249-407">10,00</span><span class="sxs-lookup"><span data-stu-id="b6249-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="b6249-408">Tööleht</span><span class="sxs-lookup"><span data-stu-id="b6249-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b6249-409">Tööleht</span><span class="sxs-lookup"><span data-stu-id="b6249-409">Journal</span></span></th>
<th><span data-ttu-id="b6249-410">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="b6249-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b6249-411">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="b6249-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b6249-412">Versioon</span><span class="sxs-lookup"><span data-stu-id="b6249-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-413">00003</span><span class="sxs-lookup"><span data-stu-id="b6249-413">00003</span></span></td>
<td><span data-ttu-id="b6249-414">Üldkulu määra arvutamise tööleht</span><span class="sxs-lookup"><span data-stu-id="b6249-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="b6249-415">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="b6249-415">Fiscal</span></span></td>
<td><span data-ttu-id="b6249-416">2017</span><span class="sxs-lookup"><span data-stu-id="b6249-416">2017</span></span></td>
<td><span data-ttu-id="b6249-417">Periood 1</span><span class="sxs-lookup"><span data-stu-id="b6249-417">Period 1</span></span></td>
<td><span data-ttu-id="b6249-418">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="b6249-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="b6249-419">Töölehe sisestused (töölehe sisestused üldkulu määra arvutamiseks)</span><span class="sxs-lookup"><span data-stu-id="b6249-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b6249-420">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b6249-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b6249-421">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-421">Cost object</span></span></th>
<th><span data-ttu-id="b6249-422">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b6249-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-423">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="b6249-424">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="b6249-424">Proj 1</span></span></td>
<td><span data-ttu-id="b6249-425">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="b6249-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="b6249-426">3,00</span><span class="sxs-lookup"><span data-stu-id="b6249-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-427">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="b6249-428">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="b6249-428">Proj 2</span></span></td>
<td><span data-ttu-id="b6249-429">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="b6249-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="b6249-430">1,00</span><span class="sxs-lookup"><span data-stu-id="b6249-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b6249-431">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="b6249-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-432">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b6249-433">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b6249-433">Cost element</span></span></th>
<th><span data-ttu-id="b6249-434">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b6249-434">Cost behavior</span></span></th>
<th><span data-ttu-id="b6249-435">Summa</span><span class="sxs-lookup"><span data-stu-id="b6249-435">Amount</span></span></th>
<th><span data-ttu-id="b6249-436">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b6249-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="b6249-437">CC0001</span></span></td>
<td><span data-ttu-id="b6249-438">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b6249-438">HR</span></span></td>
<td><span data-ttu-id="b6249-439">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-439">10001</span></span></td>
<td><span data-ttu-id="b6249-440">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-440">Electricity</span></span></td>
<td><span data-ttu-id="b6249-441">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-441">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-442">–30,00</span><span class="sxs-lookup"><span data-stu-id="b6249-442">-30.00</span></span></td>
<td><span data-ttu-id="b6249-443">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-444">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="b6249-444">Proj 1</span></span></td>
<td><span data-ttu-id="b6249-445">Sisemine proj. 1</span><span class="sxs-lookup"><span data-stu-id="b6249-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="b6249-446">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-446">10001</span></span></td>
<td><span data-ttu-id="b6249-447">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-447">Electricity</span></span></td>
<td><span data-ttu-id="b6249-448">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-448">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-449">30,00</span><span class="sxs-lookup"><span data-stu-id="b6249-449">30.00</span></span></td>
<td><span data-ttu-id="b6249-450">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-451">CC001</span><span class="sxs-lookup"><span data-stu-id="b6249-451">CC001</span></span></td>
<td><span data-ttu-id="b6249-452">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b6249-452">HR</span></span></td>
<td><span data-ttu-id="b6249-453">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-453">10001</span></span></td>
<td><span data-ttu-id="b6249-454">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-454">Electricity</span></span></td>
<td><span data-ttu-id="b6249-455">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-455">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="b6249-456">-10.00</span></span></td>
<td><span data-ttu-id="b6249-457">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-458">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="b6249-458">Proj 2</span></span></td>
<td><span data-ttu-id="b6249-459">Sisemine proj. 2</span><span class="sxs-lookup"><span data-stu-id="b6249-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="b6249-460">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-460">10001</span></span></td>
<td><span data-ttu-id="b6249-461">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-461">Electricity</span></span></td>
<td><span data-ttu-id="b6249-462">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-462">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-463">10.00</span><span class="sxs-lookup"><span data-stu-id="b6249-463">10.00</span></span></td>
<td><span data-ttu-id="b6249-464">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b6249-465">Lisateavet vt teemast [Üldkulude arvutamine](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="b6249-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="b6249-466">4. etapp: kulueralduse arvutuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="b6249-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="b6249-467">Eraldamist kasutatakse kuluobjekti saldo eraldamiseks teistele kuluobjektidele, rakendades eraldamisalust.</span><span class="sxs-lookup"><span data-stu-id="b6249-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="b6249-468">Finance toetab vastastikuse eraldamise meetodit.</span><span class="sxs-lookup"><span data-stu-id="b6249-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="b6249-469">Vastastikuse eraldamise meetodi puhul tuvastatakse täiendavate kuluobjektide vahetatavad vastastikused teenused.</span><span class="sxs-lookup"><span data-stu-id="b6249-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="b6249-470">Süsteem määrab automaatselt eraldamiste tegemise õige järjekorra.</span><span class="sxs-lookup"><span data-stu-id="b6249-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="b6249-471">Kuluobjekti saldo eraldatakse üksiku eraldamisalusena.</span><span class="sxs-lookup"><span data-stu-id="b6249-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="b6249-472">Toetatakse eraldamisi kuluobjektide dimensioonide ja nende vastavate liikmete seas.</span><span class="sxs-lookup"><span data-stu-id="b6249-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="b6249-473">Eraldamisjärjekorda reguleerib kulujuhtseade.</span><span class="sxs-lookup"><span data-stu-id="b6249-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="b6249-474">[![Vastastikune meetod](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="b6249-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="b6249-475">Kulueraldamise määratlemine</span><span class="sxs-lookup"><span data-stu-id="b6249-475">Define the cost allocation</span></span>

<span data-ttu-id="b6249-476">Siin on lihtne näide, mis selgitab, kuidas jälgida kulu liikumist.</span><span class="sxs-lookup"><span data-stu-id="b6249-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="b6249-477">Kuluobjekt CC001 inimressursid panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="b6249-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="b6249-478">Luuakse statistilise dimensiooni liige nimega Inimressursside teenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="b6249-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-479">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-479">Cost object</span></span></th>
<th><span data-ttu-id="b6249-480">Inimressursside teenused</span><span class="sxs-lookup"><span data-stu-id="b6249-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-481">CC002</span><span class="sxs-lookup"><span data-stu-id="b6249-481">CC002</span></span></td>
<td><span data-ttu-id="b6249-482">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b6249-482">Finance</span></span></td>
<td><span data-ttu-id="b6249-483">35</span><span class="sxs-lookup"><span data-stu-id="b6249-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-484">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-484">CC003</span></span></td>
<td><span data-ttu-id="b6249-485">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-485">Assembly</span></span></td>
<td><span data-ttu-id="b6249-486">55</span><span class="sxs-lookup"><span data-stu-id="b6249-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-487">CC004</span><span class="sxs-lookup"><span data-stu-id="b6249-487">CC004</span></span></td>
<td><span data-ttu-id="b6249-488">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b6249-488">Packaging</span></span></td>
<td><span data-ttu-id="b6249-489">10</span><span class="sxs-lookup"><span data-stu-id="b6249-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b6249-490">Kuluobjekt CC002 rahandus panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="b6249-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="b6249-491">Luuakse statistilise dimensiooni liige nimega Rahandusteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="b6249-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-492">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-492">Cost object</span></span></th>
<th><span data-ttu-id="b6249-493">Rahandusteenused</span><span class="sxs-lookup"><span data-stu-id="b6249-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-494">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-494">CC003</span></span></td>
<td><span data-ttu-id="b6249-495">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-495">Assembly</span></span></td>
<td><span data-ttu-id="b6249-496">65</span><span class="sxs-lookup"><span data-stu-id="b6249-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-497">CC004</span><span class="sxs-lookup"><span data-stu-id="b6249-497">CC004</span></span></td>
<td><span data-ttu-id="b6249-498">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b6249-498">Packaging</span></span></td>
<td><span data-ttu-id="b6249-499">35</span><span class="sxs-lookup"><span data-stu-id="b6249-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b6249-500">Kuluobjekt CC003 assembler panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="b6249-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="b6249-501">Luuakse statistilise dimensiooni liige nimega Assembleriteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="b6249-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-502">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-502">Cost object</span></span></th>
<th><span data-ttu-id="b6249-503">Assembleriteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="b6249-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-504">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b6249-504">Prod 1</span></span></td>
<td><span data-ttu-id="b6249-505">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b6249-505">Product 1</span></span></td>
<td><span data-ttu-id="b6249-506">60</span><span class="sxs-lookup"><span data-stu-id="b6249-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-507">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-507">Prod 2</span></span></td>
<td><span data-ttu-id="b6249-508">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-508">Product 2</span></span></td>
<td><span data-ttu-id="b6249-509">20</span><span class="sxs-lookup"><span data-stu-id="b6249-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b6249-510">Kuluobjekt CC004 pakendamine panustab mitmele kuluobjektile.</span><span class="sxs-lookup"><span data-stu-id="b6249-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="b6249-511">Luuakse statistilise dimensiooni liige nimega Pakendamisteenused, et mõõta tarbitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="b6249-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-512">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-512">Cost object</span></span></th>
<th><span data-ttu-id="b6249-513">Pakendamisteenused (tundides)</span><span class="sxs-lookup"><span data-stu-id="b6249-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-514">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b6249-514">Prod 1</span></span></td>
<td><span data-ttu-id="b6249-515">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b6249-515">Product 1</span></span></td>
<td><span data-ttu-id="b6249-516">80</span><span class="sxs-lookup"><span data-stu-id="b6249-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-517">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-517">Prod 2</span></span></td>
<td><span data-ttu-id="b6249-518">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-518">Product 2</span></span></td>
<td><span data-ttu-id="b6249-519">15</span><span class="sxs-lookup"><span data-stu-id="b6249-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b6249-520">Statistilised mõõdud, nagu toote tarbitud tootmistunnid, saab tuletada lähteandmetest.</span><span class="sxs-lookup"><span data-stu-id="b6249-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="b6249-521">Lisateavet vt teemast [Statistiliste mõõtude pakkuja mall](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="b6249-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="b6249-522">Järgmises tabelis on näidatud tulemus, kui HR-teenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="b6249-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-523">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-523">Cost object</span></span></th>
<th><span data-ttu-id="b6249-524">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b6249-524">Magnitude</span></span></th>
<th><span data-ttu-id="b6249-525">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="b6249-525">Allocation factor</span></span></th>
<th><span data-ttu-id="b6249-526">Summa</span><span class="sxs-lookup"><span data-stu-id="b6249-526">Amount</span></span></th>
<th><span data-ttu-id="b6249-527">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b6249-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-528">CC002</span><span class="sxs-lookup"><span data-stu-id="b6249-528">CC002</span></span></td>
<td><span data-ttu-id="b6249-529">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b6249-529">Finance</span></span></td>
<td><span data-ttu-id="b6249-530">35</span><span class="sxs-lookup"><span data-stu-id="b6249-530">35</span></span></td>
<td><span data-ttu-id="b6249-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b6249-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b6249-532">175.00</span><span class="sxs-lookup"><span data-stu-id="b6249-532">175.00</span></span></td>
<td><span data-ttu-id="b6249-533">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-534">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-534">CC003</span></span></td>
<td><span data-ttu-id="b6249-535">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-535">Assembly</span></span></td>
<td><span data-ttu-id="b6249-536">55</span><span class="sxs-lookup"><span data-stu-id="b6249-536">55</span></span></td>
<td><span data-ttu-id="b6249-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b6249-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b6249-538">275.00</span><span class="sxs-lookup"><span data-stu-id="b6249-538">275.00</span></span></td>
<td><span data-ttu-id="b6249-539">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-540">CC004</span><span class="sxs-lookup"><span data-stu-id="b6249-540">CC004</span></span></td>
<td><span data-ttu-id="b6249-541">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b6249-541">Packaging</span></span></td>
<td><span data-ttu-id="b6249-542">10</span><span class="sxs-lookup"><span data-stu-id="b6249-542">10</span></span></td>
<td><span data-ttu-id="b6249-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b6249-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b6249-544">50,00</span><span class="sxs-lookup"><span data-stu-id="b6249-544">50.00</span></span></td>
<td><span data-ttu-id="b6249-545">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-546">CC002</span><span class="sxs-lookup"><span data-stu-id="b6249-546">CC002</span></span></td>
<td><span data-ttu-id="b6249-547">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b6249-547">Finance</span></span></td>
<td><span data-ttu-id="b6249-548">35</span><span class="sxs-lookup"><span data-stu-id="b6249-548">35</span></span></td>
<td><span data-ttu-id="b6249-549">(35 ÷ 100) × 1245,71</span><span class="sxs-lookup"><span data-stu-id="b6249-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b6249-550">436.00</span><span class="sxs-lookup"><span data-stu-id="b6249-550">436.00</span></span></td>
<td><span data-ttu-id="b6249-551">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-552">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-552">CC003</span></span></td>
<td><span data-ttu-id="b6249-553">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-553">Assembly</span></span></td>
<td><span data-ttu-id="b6249-554">55</span><span class="sxs-lookup"><span data-stu-id="b6249-554">55</span></span></td>
<td><span data-ttu-id="b6249-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="b6249-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b6249-556">685.14</span><span class="sxs-lookup"><span data-stu-id="b6249-556">685.14</span></span></td>
<td><span data-ttu-id="b6249-557">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-558">CC004</span><span class="sxs-lookup"><span data-stu-id="b6249-558">CC004</span></span></td>
<td><span data-ttu-id="b6249-559">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b6249-559">Packaging</span></span></td>
<td><span data-ttu-id="b6249-560">10</span><span class="sxs-lookup"><span data-stu-id="b6249-560">10</span></span></td>
<td><span data-ttu-id="b6249-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="b6249-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b6249-562">124.57</span><span class="sxs-lookup"><span data-stu-id="b6249-562">124.57</span></span></td>
<td><span data-ttu-id="b6249-563">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b6249-564">Järgmises tabelis on näidatud tulemus, kui Rahandusteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="b6249-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-565">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-565">Cost object</span></span></th>
<th><span data-ttu-id="b6249-566">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b6249-566">Magnitude</span></span></th>
<th><span data-ttu-id="b6249-567">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="b6249-567">Allocation factor</span></span></th>
<th><span data-ttu-id="b6249-568">Summa</span><span class="sxs-lookup"><span data-stu-id="b6249-568">Amount</span></span></th>
<th><span data-ttu-id="b6249-569">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b6249-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-570">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-570">CC003</span></span></td>
<td><span data-ttu-id="b6249-571">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-571">Assembly</span></span></td>
<td><span data-ttu-id="b6249-572">65</span><span class="sxs-lookup"><span data-stu-id="b6249-572">65</span></span></td>
<td><span data-ttu-id="b6249-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="b6249-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="b6249-574">438.75</span><span class="sxs-lookup"><span data-stu-id="b6249-574">438.75</span></span></td>
<td><span data-ttu-id="b6249-575">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-576">CC004</span><span class="sxs-lookup"><span data-stu-id="b6249-576">CC004</span></span></td>
<td><span data-ttu-id="b6249-577">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b6249-577">Packaging</span></span></td>
<td><span data-ttu-id="b6249-578">35</span><span class="sxs-lookup"><span data-stu-id="b6249-578">35</span></span></td>
<td><span data-ttu-id="b6249-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="b6249-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="b6249-580">236.25</span><span class="sxs-lookup"><span data-stu-id="b6249-580">236.25</span></span></td>
<td><span data-ttu-id="b6249-581">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-582">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-582">CC003</span></span></td>
<td><span data-ttu-id="b6249-583">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-583">Assembly</span></span></td>
<td><span data-ttu-id="b6249-584">65</span><span class="sxs-lookup"><span data-stu-id="b6249-584">65</span></span></td>
<td><span data-ttu-id="b6249-585">(65 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="b6249-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="b6249-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="b6249-586">5,297.69</span></span></td>
<td><span data-ttu-id="b6249-587">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-588">CC004</span><span class="sxs-lookup"><span data-stu-id="b6249-588">CC004</span></span></td>
<td><span data-ttu-id="b6249-589">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b6249-589">Packaging</span></span></td>
<td><span data-ttu-id="b6249-590">35</span><span class="sxs-lookup"><span data-stu-id="b6249-590">35</span></span></td>
<td><span data-ttu-id="b6249-591">(35 ÷ 100) × (7714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="b6249-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="b6249-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="b6249-592">2,852.60</span></span></td>
<td><span data-ttu-id="b6249-593">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b6249-594">Järgmises tabelis on näidatud tulemus, kui Assembleriteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="b6249-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-595">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-595">Cost object</span></span></th>
<th><span data-ttu-id="b6249-596">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b6249-596">Magnitude</span></span></th>
<th><span data-ttu-id="b6249-597">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="b6249-597">Allocation factor</span></span></th>
<th><span data-ttu-id="b6249-598">Summa</span><span class="sxs-lookup"><span data-stu-id="b6249-598">Amount</span></span></th>
<th><span data-ttu-id="b6249-599">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b6249-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-600">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b6249-600">Prod 1</span></span></td>
<td><span data-ttu-id="b6249-601">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b6249-601">Product 1</span></span></td>
<td><span data-ttu-id="b6249-602">60</span><span class="sxs-lookup"><span data-stu-id="b6249-602">60</span></span></td>
<td><span data-ttu-id="b6249-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="b6249-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="b6249-604">535.31</span><span class="sxs-lookup"><span data-stu-id="b6249-604">535.31</span></span></td>
<td><span data-ttu-id="b6249-605">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-606">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-606">Prod 2</span></span></td>
<td><span data-ttu-id="b6249-607">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-607">Product 2</span></span></td>
<td><span data-ttu-id="b6249-608">20</span><span class="sxs-lookup"><span data-stu-id="b6249-608">20</span></span></td>
<td><span data-ttu-id="b6249-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="b6249-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="b6249-610">178.44</span><span class="sxs-lookup"><span data-stu-id="b6249-610">178.44</span></span></td>
<td><span data-ttu-id="b6249-611">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-612">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b6249-612">Prod 1</span></span></td>
<td><span data-ttu-id="b6249-613">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b6249-613">Product 1</span></span></td>
<td><span data-ttu-id="b6249-614">60</span><span class="sxs-lookup"><span data-stu-id="b6249-614">60</span></span></td>
<td><span data-ttu-id="b6249-615">(60 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="b6249-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="b6249-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="b6249-616">4,487.12</span></span></td>
<td><span data-ttu-id="b6249-617">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-618">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-618">Prod 2</span></span></td>
<td><span data-ttu-id="b6249-619">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-619">Product 2</span></span></td>
<td><span data-ttu-id="b6249-620">20</span><span class="sxs-lookup"><span data-stu-id="b6249-620">20</span></span></td>
<td><span data-ttu-id="b6249-621">(20 ÷ 80) × (5297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="b6249-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="b6249-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="b6249-622">1,495.71</span></span></td>
<td><span data-ttu-id="b6249-623">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b6249-624">Järgmises tabelis on näidatud tulemus, kui Pakendamisteenused on rakendatud kogukulu puhul eraldamisalusena (fikseeritud ja muutuvkulu).</span><span class="sxs-lookup"><span data-stu-id="b6249-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-625">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-625">Cost object</span></span></th>
<th><span data-ttu-id="b6249-626">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b6249-626">Magnitude</span></span></th>
<th><span data-ttu-id="b6249-627">Eraldamistegur</span><span class="sxs-lookup"><span data-stu-id="b6249-627">Allocation factor</span></span></th>
<th><span data-ttu-id="b6249-628">Summa</span><span class="sxs-lookup"><span data-stu-id="b6249-628">Amount</span></span></th>
<th><span data-ttu-id="b6249-629">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b6249-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-630">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b6249-630">Prod 1</span></span></td>
<td><span data-ttu-id="b6249-631">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b6249-631">Product 1</span></span></td>
<td><span data-ttu-id="b6249-632">80</span><span class="sxs-lookup"><span data-stu-id="b6249-632">80</span></span></td>
<td><span data-ttu-id="b6249-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="b6249-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="b6249-634">241.05</span><span class="sxs-lookup"><span data-stu-id="b6249-634">241.05</span></span></td>
<td><span data-ttu-id="b6249-635">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-636">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-636">Prod 2</span></span></td>
<td><span data-ttu-id="b6249-637">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-637">Product 2</span></span></td>
<td><span data-ttu-id="b6249-638">15</span><span class="sxs-lookup"><span data-stu-id="b6249-638">15</span></span></td>
<td><span data-ttu-id="b6249-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="b6249-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="b6249-640">45.20</span><span class="sxs-lookup"><span data-stu-id="b6249-640">45.20</span></span></td>
<td><span data-ttu-id="b6249-641">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-642">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b6249-642">Prod 1</span></span></td>
<td><span data-ttu-id="b6249-643">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b6249-643">Product 1</span></span></td>
<td><span data-ttu-id="b6249-644">80</span><span class="sxs-lookup"><span data-stu-id="b6249-644">80</span></span></td>
<td><span data-ttu-id="b6249-645">(80 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="b6249-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="b6249-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="b6249-646">2,507.09</span></span></td>
<td><span data-ttu-id="b6249-647">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-648">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-648">Prod 2</span></span></td>
<td><span data-ttu-id="b6249-649">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-649">Product 2</span></span></td>
<td><span data-ttu-id="b6249-650">15</span><span class="sxs-lookup"><span data-stu-id="b6249-650">15</span></span></td>
<td><span data-ttu-id="b6249-651">(15 ÷ 95) × (2852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="b6249-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="b6249-652">470.08</span><span class="sxs-lookup"><span data-stu-id="b6249-652">470.08</span></span></td>
<td><span data-ttu-id="b6249-653">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b6249-654">Töölehe sisestused (kuluobjekti saldo töölehe sisestused)</span><span class="sxs-lookup"><span data-stu-id="b6249-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b6249-655">Tööleht</span><span class="sxs-lookup"><span data-stu-id="b6249-655">Journal</span></span></th>
<th><span data-ttu-id="b6249-656">Töölehe tüüp</span><span class="sxs-lookup"><span data-stu-id="b6249-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b6249-657">Rahanduskalendri periood</span><span class="sxs-lookup"><span data-stu-id="b6249-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b6249-658">Versioon</span><span class="sxs-lookup"><span data-stu-id="b6249-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-659">00004</span><span class="sxs-lookup"><span data-stu-id="b6249-659">00004</span></span></td>
<td><span data-ttu-id="b6249-660">Kulueralduse tööleht</span><span class="sxs-lookup"><span data-stu-id="b6249-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="b6249-661">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="b6249-661">Fiscal</span></span></td>
<td><span data-ttu-id="b6249-662">2017</span><span class="sxs-lookup"><span data-stu-id="b6249-662">2017</span></span></td>
<td><span data-ttu-id="b6249-663">Periood 1</span><span class="sxs-lookup"><span data-stu-id="b6249-663">Period 1</span></span></td>
<td><span data-ttu-id="b6249-664">Üldkulude arvutus / 01-02-2017 23:51:00 / Pearaamat /2017 / 1. periood</span><span class="sxs-lookup"><span data-stu-id="b6249-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="b6249-665">Töölehe read</span><span class="sxs-lookup"><span data-stu-id="b6249-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b6249-666">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b6249-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b6249-667">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b6249-668">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b6249-668">Cost element</span></span></th>
<th><span data-ttu-id="b6249-669">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b6249-669">Cost behavior</span></span></th>
<th><span data-ttu-id="b6249-670">Summa</span><span class="sxs-lookup"><span data-stu-id="b6249-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-671">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="b6249-672">CC001</span><span class="sxs-lookup"><span data-stu-id="b6249-672">CC001</span></span></td>
<td><span data-ttu-id="b6249-673">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b6249-673">HR</span></span></td>
<td><span data-ttu-id="b6249-674">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-674">10001</span></span></td>
<td><span data-ttu-id="b6249-675">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-675">Electricity</span></span></td>
<td><span data-ttu-id="b6249-676">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-676">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-677">500,00</span><span class="sxs-lookup"><span data-stu-id="b6249-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-678">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="b6249-679">CC001</span><span class="sxs-lookup"><span data-stu-id="b6249-679">CC001</span></span></td>
<td><span data-ttu-id="b6249-680">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b6249-680">HR</span></span></td>
<td><span data-ttu-id="b6249-681">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-681">10001</span></span></td>
<td><span data-ttu-id="b6249-682">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-682">Electricity</span></span></td>
<td><span data-ttu-id="b6249-683">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-683">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="b6249-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-685">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="b6249-686">CC002</span><span class="sxs-lookup"><span data-stu-id="b6249-686">CC002</span></span></td>
<td><span data-ttu-id="b6249-687">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b6249-687">Finance</span></span></td>
<td><span data-ttu-id="b6249-688">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-688">10001</span></span></td>
<td><span data-ttu-id="b6249-689">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-689">Electricity</span></span></td>
<td><span data-ttu-id="b6249-690">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-690">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-691">675.00</span><span class="sxs-lookup"><span data-stu-id="b6249-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-692">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="b6249-693">CC002</span><span class="sxs-lookup"><span data-stu-id="b6249-693">CC002</span></span></td>
<td><span data-ttu-id="b6249-694">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b6249-694">Finance</span></span></td>
<td><span data-ttu-id="b6249-695">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-695">10001</span></span></td>
<td><span data-ttu-id="b6249-696">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-696">Electricity</span></span></td>
<td><span data-ttu-id="b6249-697">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-697">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="b6249-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-699">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="b6249-700">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-700">CC003</span></span></td>
<td><span data-ttu-id="b6249-701">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-701">Assembly</span></span></td>
<td><span data-ttu-id="b6249-702">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-702">10001</span></span></td>
<td><span data-ttu-id="b6249-703">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-703">Electricity</span></span></td>
<td><span data-ttu-id="b6249-704">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-704">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-705">713.75</span><span class="sxs-lookup"><span data-stu-id="b6249-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-706">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="b6249-707">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-707">CC003</span></span></td>
<td><span data-ttu-id="b6249-708">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-708">Assembly</span></span></td>
<td><span data-ttu-id="b6249-709">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-709">10001</span></span></td>
<td><span data-ttu-id="b6249-710">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-710">Electricity</span></span></td>
<td><span data-ttu-id="b6249-711">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-711">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="b6249-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-713">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="b6249-714">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-714">CC003</span></span></td>
<td><span data-ttu-id="b6249-715">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b6249-715">Packaging</span></span></td>
<td><span data-ttu-id="b6249-716">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-716">10001</span></span></td>
<td><span data-ttu-id="b6249-717">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-717">Electricity</span></span></td>
<td><span data-ttu-id="b6249-718">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-718">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-719">286.25</span><span class="sxs-lookup"><span data-stu-id="b6249-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-720">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="b6249-721">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-721">CC003</span></span></td>
<td><span data-ttu-id="b6249-722">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b6249-722">Packaging</span></span></td>
<td><span data-ttu-id="b6249-723">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-723">10001</span></span></td>
<td><span data-ttu-id="b6249-724">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-724">Electricity</span></span></td>
<td><span data-ttu-id="b6249-725">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-725">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="b6249-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-727">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="b6249-728">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b6249-728">Prod 1</span></span></td>
<td><span data-ttu-id="b6249-729">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b6249-729">Product 1</span></span></td>
<td><span data-ttu-id="b6249-730">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-730">10001</span></span></td>
<td><span data-ttu-id="b6249-731">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-731">Electricity</span></span></td>
<td><span data-ttu-id="b6249-732">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-732">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-733">776.36</span><span class="sxs-lookup"><span data-stu-id="b6249-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-734">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="b6249-735">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b6249-735">Prod 1</span></span></td>
<td><span data-ttu-id="b6249-736">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b6249-736">Product 1</span></span></td>
<td><span data-ttu-id="b6249-737">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-737">10001</span></span></td>
<td><span data-ttu-id="b6249-738">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-738">Electricity</span></span></td>
<td><span data-ttu-id="b6249-739">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-739">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="b6249-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-741">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="b6249-742">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-742">Prod 2</span></span></td>
<td><span data-ttu-id="b6249-743">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b6249-743">Product 1</span></span></td>
<td><span data-ttu-id="b6249-744">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-744">10001</span></span></td>
<td><span data-ttu-id="b6249-745">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-745">Electricity</span></span></td>
<td><span data-ttu-id="b6249-746">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-746">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-747">223.64</span><span class="sxs-lookup"><span data-stu-id="b6249-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-748">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="b6249-749">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-749">Prod 2</span></span></td>
<td><span data-ttu-id="b6249-750">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b6249-750">Product 1</span></span></td>
<td><span data-ttu-id="b6249-751">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-751">10001</span></span></td>
<td><span data-ttu-id="b6249-752">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-752">Electricity</span></span></td>
<td><span data-ttu-id="b6249-753">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-753">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="b6249-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b6249-755">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="b6249-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b6249-756">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b6249-757">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b6249-757">Cost element</span></span></th>
<th><span data-ttu-id="b6249-758">Kulukäitumine</span><span class="sxs-lookup"><span data-stu-id="b6249-758">Cost behavior</span></span></th>
<th><span data-ttu-id="b6249-759">Summa</span><span class="sxs-lookup"><span data-stu-id="b6249-759">Amount</span></span></th>
<th><span data-ttu-id="b6249-760">Aruandluskuupäev</span><span class="sxs-lookup"><span data-stu-id="b6249-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6249-761">CC001</span><span class="sxs-lookup"><span data-stu-id="b6249-761">CC001</span></span></td>
<td><span data-ttu-id="b6249-762">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b6249-762">HR</span></span></td>
<td><span data-ttu-id="b6249-763">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-763">10001</span></span></td>
<td><span data-ttu-id="b6249-764">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-764">Electricity</span></span></td>
<td><span data-ttu-id="b6249-765">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-765">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-766">‑500,00</span><span class="sxs-lookup"><span data-stu-id="b6249-766">-500.00</span></span></td>
<td><span data-ttu-id="b6249-767">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-768">CC002</span><span class="sxs-lookup"><span data-stu-id="b6249-768">CC002</span></span></td>
<td><span data-ttu-id="b6249-769">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b6249-769">Finance</span></span></td>
<td><span data-ttu-id="b6249-770">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-770">10001</span></span></td>
<td><span data-ttu-id="b6249-771">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-771">Electricity</span></span></td>
<td><span data-ttu-id="b6249-772">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-772">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-773">175.00</span><span class="sxs-lookup"><span data-stu-id="b6249-773">175.00</span></span></td>
<td><span data-ttu-id="b6249-774">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-775">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-775">CC003</span></span></td>
<td><span data-ttu-id="b6249-776">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-776">Assembly</span></span></td>
<td><span data-ttu-id="b6249-777">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-777">10001</span></span></td>
<td><span data-ttu-id="b6249-778">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-778">Electricity</span></span></td>
<td><span data-ttu-id="b6249-779">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-779">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-780">275.00</span><span class="sxs-lookup"><span data-stu-id="b6249-780">275.00</span></span></td>
<td><span data-ttu-id="b6249-781">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-782">CC004</span><span class="sxs-lookup"><span data-stu-id="b6249-782">CC004</span></span></td>
<td><span data-ttu-id="b6249-783">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b6249-783">Packaging</span></span></td>
<td><span data-ttu-id="b6249-784">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-784">10001</span></span></td>
<td><span data-ttu-id="b6249-785">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-785">Electricity</span></span></td>
<td><span data-ttu-id="b6249-786">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-786">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-787">50,00</span><span class="sxs-lookup"><span data-stu-id="b6249-787">50,00</span></span></td>
<td><span data-ttu-id="b6249-788">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-789">CC001</span><span class="sxs-lookup"><span data-stu-id="b6249-789">CC001</span></span></td>
<td><span data-ttu-id="b6249-790">Personaliosakond</span><span class="sxs-lookup"><span data-stu-id="b6249-790">HR</span></span></td>
<td><span data-ttu-id="b6249-791">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-791">10001</span></span></td>
<td><span data-ttu-id="b6249-792">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-792">Electricity</span></span></td>
<td><span data-ttu-id="b6249-793">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-793">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-794">–1245,71</span><span class="sxs-lookup"><span data-stu-id="b6249-794">-1,245.71</span></span></td>
<td><span data-ttu-id="b6249-795">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-796">CC002</span><span class="sxs-lookup"><span data-stu-id="b6249-796">CC002</span></span></td>
<td><span data-ttu-id="b6249-797">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b6249-797">Finance</span></span></td>
<td><span data-ttu-id="b6249-798">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-798">10001</span></span></td>
<td><span data-ttu-id="b6249-799">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-799">Electricity</span></span></td>
<td><span data-ttu-id="b6249-800">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-800">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-801">436.00</span><span class="sxs-lookup"><span data-stu-id="b6249-801">436.00</span></span></td>
<td><span data-ttu-id="b6249-802">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-803">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-803">CC003</span></span></td>
<td><span data-ttu-id="b6249-804">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-804">Assembly</span></span></td>
<td><span data-ttu-id="b6249-805">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-805">10001</span></span></td>
<td><span data-ttu-id="b6249-806">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-806">Electricity</span></span></td>
<td><span data-ttu-id="b6249-807">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-807">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-808">685.14</span><span class="sxs-lookup"><span data-stu-id="b6249-808">685.14</span></span></td>
<td><span data-ttu-id="b6249-809">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-810">CC004</span><span class="sxs-lookup"><span data-stu-id="b6249-810">CC004</span></span></td>
<td><span data-ttu-id="b6249-811">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b6249-811">Packaging</span></span></td>
<td><span data-ttu-id="b6249-812">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-812">10001</span></span></td>
<td><span data-ttu-id="b6249-813">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-813">Electricity</span></span></td>
<td><span data-ttu-id="b6249-814">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-814">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-815">124.57</span><span class="sxs-lookup"><span data-stu-id="b6249-815">124.57</span></span></td>
<td><span data-ttu-id="b6249-816">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-817">CC002</span><span class="sxs-lookup"><span data-stu-id="b6249-817">CC002</span></span></td>
<td><span data-ttu-id="b6249-818">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b6249-818">Finance</span></span></td>
<td><span data-ttu-id="b6249-819">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-819">10001</span></span></td>
<td><span data-ttu-id="b6249-820">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-820">Electricity</span></span></td>
<td><span data-ttu-id="b6249-821">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-821">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-822">–675,00</span><span class="sxs-lookup"><span data-stu-id="b6249-822">-675.00</span></span></td>
<td><span data-ttu-id="b6249-823">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-824">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-824">CC003</span></span></td>
<td><span data-ttu-id="b6249-825">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-825">Assembly</span></span></td>
<td><span data-ttu-id="b6249-826">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-826">10001</span></span></td>
<td><span data-ttu-id="b6249-827">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-827">Electricity</span></span></td>
<td><span data-ttu-id="b6249-828">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-828">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-829">438.75</span><span class="sxs-lookup"><span data-stu-id="b6249-829">438.75</span></span></td>
<td><span data-ttu-id="b6249-830">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-831">CC004</span><span class="sxs-lookup"><span data-stu-id="b6249-831">CC004</span></span></td>
<td><span data-ttu-id="b6249-832">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b6249-832">Packaging</span></span></td>
<td><span data-ttu-id="b6249-833">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-833">10001</span></span></td>
<td><span data-ttu-id="b6249-834">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-834">Electricity</span></span></td>
<td><span data-ttu-id="b6249-835">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-835">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-836">236.25</span><span class="sxs-lookup"><span data-stu-id="b6249-836">236.25</span></span></td>
<td><span data-ttu-id="b6249-837">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-838">CC002</span><span class="sxs-lookup"><span data-stu-id="b6249-838">CC002</span></span></td>
<td><span data-ttu-id="b6249-839">Finantsid</span><span class="sxs-lookup"><span data-stu-id="b6249-839">Finance</span></span></td>
<td><span data-ttu-id="b6249-840">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-840">10001</span></span></td>
<td><span data-ttu-id="b6249-841">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-841">Electricity</span></span></td>
<td><span data-ttu-id="b6249-842">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-842">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-843">–8150,29</span><span class="sxs-lookup"><span data-stu-id="b6249-843">-8,150.29</span></span></td>
<td><span data-ttu-id="b6249-844">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-845">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-845">CC003</span></span></td>
<td><span data-ttu-id="b6249-846">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-846">Assembly</span></span></td>
<td><span data-ttu-id="b6249-847">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-847">10001</span></span></td>
<td><span data-ttu-id="b6249-848">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-848">Electricity</span></span></td>
<td><span data-ttu-id="b6249-849">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-849">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="b6249-850">5,297.69</span></span></td>
<td><span data-ttu-id="b6249-851">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-852">CC004</span><span class="sxs-lookup"><span data-stu-id="b6249-852">CC004</span></span></td>
<td><span data-ttu-id="b6249-853">Pakendamine</span><span class="sxs-lookup"><span data-stu-id="b6249-853">Packaging</span></span></td>
<td><span data-ttu-id="b6249-854">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-854">10001</span></span></td>
<td><span data-ttu-id="b6249-855">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-855">Electricity</span></span></td>
<td><span data-ttu-id="b6249-856">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-856">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="b6249-857">2,852.60</span></span></td>
<td><span data-ttu-id="b6249-858">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-859">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-859">CC003</span></span></td>
<td><span data-ttu-id="b6249-860">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-860">Assembly</span></span></td>
<td><span data-ttu-id="b6249-861">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-861">10001</span></span></td>
<td><span data-ttu-id="b6249-862">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-862">Electricity</span></span></td>
<td><span data-ttu-id="b6249-863">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-863">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-864">–713,75</span><span class="sxs-lookup"><span data-stu-id="b6249-864">-713.75</span></span></td>
<td><span data-ttu-id="b6249-865">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-866">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b6249-866">Prod 1</span></span></td>
<td><span data-ttu-id="b6249-867">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b6249-867">Product 1</span></span></td>
<td><span data-ttu-id="b6249-868">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-868">10001</span></span></td>
<td><span data-ttu-id="b6249-869">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-869">Electricity</span></span></td>
<td><span data-ttu-id="b6249-870">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-870">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-871">535.31</span><span class="sxs-lookup"><span data-stu-id="b6249-871">535.31</span></span></td>
<td><span data-ttu-id="b6249-872">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-873">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-873">Prod 2</span></span></td>
<td><span data-ttu-id="b6249-874">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-874">Product 2</span></span></td>
<td><span data-ttu-id="b6249-875">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-875">10001</span></span></td>
<td><span data-ttu-id="b6249-876">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-876">Electricity</span></span></td>
<td><span data-ttu-id="b6249-877">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-877">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-878">178.44</span><span class="sxs-lookup"><span data-stu-id="b6249-878">178.44</span></span></td>
<td><span data-ttu-id="b6249-879">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-880">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-880">CC003</span></span></td>
<td><span data-ttu-id="b6249-881">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-881">Assembly</span></span></td>
<td><span data-ttu-id="b6249-882">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-882">10001</span></span></td>
<td><span data-ttu-id="b6249-883">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-883">Electricity</span></span></td>
<td><span data-ttu-id="b6249-884">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-884">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-885">–5982,83</span><span class="sxs-lookup"><span data-stu-id="b6249-885">-5,982.83</span></span></td>
<td><span data-ttu-id="b6249-886">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-887">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b6249-887">Prod 1</span></span></td>
<td><span data-ttu-id="b6249-888">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b6249-888">Product 1</span></span></td>
<td><span data-ttu-id="b6249-889">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-889">10001</span></span></td>
<td><span data-ttu-id="b6249-890">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-890">Electricity</span></span></td>
<td><span data-ttu-id="b6249-891">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-891">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="b6249-892">4,487.12</span></span></td>
<td><span data-ttu-id="b6249-893">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-894">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-894">Prod 2</span></span></td>
<td><span data-ttu-id="b6249-895">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-895">Product 2</span></span></td>
<td><span data-ttu-id="b6249-896">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-896">10001</span></span></td>
<td><span data-ttu-id="b6249-897">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-897">Electricity</span></span></td>
<td><span data-ttu-id="b6249-898">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-898">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="b6249-899">1,495.71</span></span></td>
<td><span data-ttu-id="b6249-900">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-901">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-901">CC003</span></span></td>
<td><span data-ttu-id="b6249-902">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-902">Assembly</span></span></td>
<td><span data-ttu-id="b6249-903">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-903">10001</span></span></td>
<td><span data-ttu-id="b6249-904">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-904">Electricity</span></span></td>
<td><span data-ttu-id="b6249-905">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-905">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-906">–286,25</span><span class="sxs-lookup"><span data-stu-id="b6249-906">-286.25</span></span></td>
<td><span data-ttu-id="b6249-907">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-908">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b6249-908">Prod 1</span></span></td>
<td><span data-ttu-id="b6249-909">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b6249-909">Product 1</span></span></td>
<td><span data-ttu-id="b6249-910">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-910">10001</span></span></td>
<td><span data-ttu-id="b6249-911">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-911">Electricity</span></span></td>
<td><span data-ttu-id="b6249-912">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-912">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-913">241.05</span><span class="sxs-lookup"><span data-stu-id="b6249-913">241.05</span></span></td>
<td><span data-ttu-id="b6249-914">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-915">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-915">Prod 2</span></span></td>
<td><span data-ttu-id="b6249-916">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-916">Product 2</span></span></td>
<td><span data-ttu-id="b6249-917">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-917">10001</span></span></td>
<td><span data-ttu-id="b6249-918">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-918">Electricity</span></span></td>
<td><span data-ttu-id="b6249-919">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-919">Fixed cost</span></span></td>
<td><span data-ttu-id="b6249-920">45.20</span><span class="sxs-lookup"><span data-stu-id="b6249-920">45.20</span></span></td>
<td><span data-ttu-id="b6249-921">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-922">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-922">CC003</span></span></td>
<td><span data-ttu-id="b6249-923">Assembler</span><span class="sxs-lookup"><span data-stu-id="b6249-923">Assembly</span></span></td>
<td><span data-ttu-id="b6249-924">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-924">10001</span></span></td>
<td><span data-ttu-id="b6249-925">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-925">Electricity</span></span></td>
<td><span data-ttu-id="b6249-926">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-926">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-927">–2977,17</span><span class="sxs-lookup"><span data-stu-id="b6249-927">-2,977.17</span></span></td>
<td><span data-ttu-id="b6249-928">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-929">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b6249-929">Prod 1</span></span></td>
<td><span data-ttu-id="b6249-930">Toode 1</span><span class="sxs-lookup"><span data-stu-id="b6249-930">Product 1</span></span></td>
<td><span data-ttu-id="b6249-931">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-931">10001</span></span></td>
<td><span data-ttu-id="b6249-932">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-932">Electricity</span></span></td>
<td><span data-ttu-id="b6249-933">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-933">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="b6249-934">2,507.09</span></span></td>
<td><span data-ttu-id="b6249-935">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b6249-936">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-936">Prod 2</span></span></td>
<td><span data-ttu-id="b6249-937">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-937">Product 2</span></span></td>
<td><span data-ttu-id="b6249-938">10001</span><span class="sxs-lookup"><span data-stu-id="b6249-938">10001</span></span></td>
<td><span data-ttu-id="b6249-939">Elektrienergia</span><span class="sxs-lookup"><span data-stu-id="b6249-939">Electricity</span></span></td>
<td><span data-ttu-id="b6249-940">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-940">Variable cost</span></span></td>
<td><span data-ttu-id="b6249-941">470.08</span><span class="sxs-lookup"><span data-stu-id="b6249-941">470.08</span></span></td>
<td><span data-ttu-id="b6249-942">31. jaanuar 2017</span><span class="sxs-lookup"><span data-stu-id="b6249-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="b6249-943">Lõppsõna</span><span class="sxs-lookup"><span data-stu-id="b6249-943">Conclusion</span></span>
<span data-ttu-id="b6249-944">Finantsaruandluses sisestatakse elektrikulu 10 000,00 fiktiivse kulukeskuse ID-le.</span><span class="sxs-lookup"><span data-stu-id="b6249-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="b6249-945">Nii teavad kuluarvestajad, et see kulu tuleb eraldada.</span><span class="sxs-lookup"><span data-stu-id="b6249-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="b6249-946">Kuluarvestuses liigub kulu rakendatud poliitikate ja reeglite põhjal läbi organisatsiooniüksuste ja -tasemete.</span><span class="sxs-lookup"><span data-stu-id="b6249-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="b6249-947">Iga kulu on seostatud eraldamisalusega, mis pakub kulude eraldamiseks parimat hinnangut.</span><span class="sxs-lookup"><span data-stu-id="b6249-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="b6249-948">Kuluelement</span><span class="sxs-lookup"><span data-stu-id="b6249-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="b6249-949">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="b6249-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="b6249-950">Kokku</span><span class="sxs-lookup"><span data-stu-id="b6249-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b6249-951">CC099</span><span class="sxs-lookup"><span data-stu-id="b6249-951">CC099</span></span></th>
<th><span data-ttu-id="b6249-952">CC001</span><span class="sxs-lookup"><span data-stu-id="b6249-952">CC001</span></span></th>
<th><span data-ttu-id="b6249-953">CC002</span><span class="sxs-lookup"><span data-stu-id="b6249-953">CC002</span></span></th>
<th><span data-ttu-id="b6249-954">CC003</span><span class="sxs-lookup"><span data-stu-id="b6249-954">CC003</span></span></th>
<th><span data-ttu-id="b6249-955">CC004</span><span class="sxs-lookup"><span data-stu-id="b6249-955">CC004</span></span></th>
<th><span data-ttu-id="b6249-956">Proj. 1</span><span class="sxs-lookup"><span data-stu-id="b6249-956">Proj 1</span></span></th>
<th><span data-ttu-id="b6249-957">Proj. 2</span><span class="sxs-lookup"><span data-stu-id="b6249-957">Proj 2</span></span></th>
<th><span data-ttu-id="b6249-958">Tooe 1</span><span class="sxs-lookup"><span data-stu-id="b6249-958">Prod 1</span></span></th>
<th><span data-ttu-id="b6249-959">Toode 2</span><span class="sxs-lookup"><span data-stu-id="b6249-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="b6249-960">10001 Elekter</span><span class="sxs-lookup"><span data-stu-id="b6249-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-961"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="b6249-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-962"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="b6249-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-963"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="b6249-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-964"><strong>0,00</strong></span><span class="sxs-lookup"><span data-stu-id="b6249-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="b6249-965"><strong>30,00</strong></span><span class="sxs-lookup"><span data-stu-id="b6249-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-966"><strong>10,00</strong></span><span class="sxs-lookup"><span data-stu-id="b6249-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-967"><strong>7.770,57</strong></span><span class="sxs-lookup"><span data-stu-id="b6249-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-968"><strong>2.189,43</strong></span><span class="sxs-lookup"><span data-stu-id="b6249-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-969"><strong>10.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="b6249-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="b6249-970">Liigitamata</span><span class="sxs-lookup"><span data-stu-id="b6249-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-971">0,00</span><span class="sxs-lookup"><span data-stu-id="b6249-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="b6249-972">Fikseeritud kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-973">0,00</span><span class="sxs-lookup"><span data-stu-id="b6249-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-974">0,00</span><span class="sxs-lookup"><span data-stu-id="b6249-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-975">0,00</span><span class="sxs-lookup"><span data-stu-id="b6249-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-976">0,00</span><span class="sxs-lookup"><span data-stu-id="b6249-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-977">0,00</span><span class="sxs-lookup"><span data-stu-id="b6249-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="b6249-978">776.36</span><span class="sxs-lookup"><span data-stu-id="b6249-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-979">223.64</span><span class="sxs-lookup"><span data-stu-id="b6249-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-980"><strong>1.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="b6249-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="b6249-981">Muutuv kulu</span><span class="sxs-lookup"><span data-stu-id="b6249-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-982">000</span><span class="sxs-lookup"><span data-stu-id="b6249-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-983">0,00</span><span class="sxs-lookup"><span data-stu-id="b6249-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-984">0,00</span><span class="sxs-lookup"><span data-stu-id="b6249-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-985">0,00</span><span class="sxs-lookup"><span data-stu-id="b6249-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-986">0,00</span><span class="sxs-lookup"><span data-stu-id="b6249-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-987">30,00</span><span class="sxs-lookup"><span data-stu-id="b6249-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-988">10,00</span><span class="sxs-lookup"><span data-stu-id="b6249-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="b6249-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="b6249-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b6249-991"><strong>9.000,00</strong></span><span class="sxs-lookup"><span data-stu-id="b6249-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b6249-992">Selles teemas selgitatakse, kuidas esmane kuluelement, 10001 Eleter, liigub läbi kuluobjektide.</span><span class="sxs-lookup"><span data-stu-id="b6249-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="b6249-993">Seega eraldatakse see üldkulu organisatsiooni madalaimale tasemele.</span><span class="sxs-lookup"><span data-stu-id="b6249-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="b6249-994">Teisisõnu kannavad kulu madalaimal tasemel olevad kuluobjektid.</span><span class="sxs-lookup"><span data-stu-id="b6249-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="b6249-995">Kui soovite saada kuluobjektide vahelisest kuluvoost visuaalset ülevaadet, saate kuluvoo visualiseerimiseks kasutada kulude kokkuvõtte poliitika reegleid.</span><span class="sxs-lookup"><span data-stu-id="b6249-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="b6249-996">Täpsemat teavet vt teemast [Kulude kokkuvõte](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="b6249-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



