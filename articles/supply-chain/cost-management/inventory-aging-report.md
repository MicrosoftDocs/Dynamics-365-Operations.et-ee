---
title: Varude ajalise jaotuse aruande näited ja loogika
description: Selles teemas on toodud näited selle kohta, kuidas tõlgendada varude ajalise jaotuse aruande tulemusi.
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: b3822cf4c26d7ef9cd0d062d57fa909140d7e258
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983921"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="aa463-103">Varude ajalise jaotuse aruande näited ja loogika</span><span class="sxs-lookup"><span data-stu-id="aa463-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa463-104">Selles teemas on toodud näited selle kohta, kuidas tõlgendada **varude ajalise jaotuse** aruande tulemusi.</span><span class="sxs-lookup"><span data-stu-id="aa463-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="aa463-105">See aruanne jagab valitud kauba või kaubagrupi laos oleva koguse ja laoväärtused mitmeks perioodiks.</span><span class="sxs-lookup"><span data-stu-id="aa463-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="aa463-106">Teema hõlmab ka aruande sisemist loogikat.</span><span class="sxs-lookup"><span data-stu-id="aa463-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="aa463-107">Selles teemas on toodud näited, mis sisalduvad standardses **varude ajalise jaotuse** aruandes.</span><span class="sxs-lookup"><span data-stu-id="aa463-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="aa463-108">Siiski soovitame üldiselt kasutada selle aruande versiooni [Varude ajalise jaotuse aruande talletamine](inventory-aging-report-storage.md), eriti kui te peate töötlema palju kaupu ja ladusid.</span><span class="sxs-lookup"><span data-stu-id="aa463-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="aa463-109">Varude ajalise jaotuse aruande talletamine salvestab kõik teie loodud aruanded, kuvab tulemused interaktiivse lehena ja diagrammina ning võimaldab teil eksportida kõiki salvestatud aruandeid.</span><span class="sxs-lookup"><span data-stu-id="aa463-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="aa463-110">Näidetes kasutatavad näidisandmed</span><span class="sxs-lookup"><span data-stu-id="aa463-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="aa463-111">Teema näited põhinevad selles jaotises kirjeldatud laokannete näidisandmetel.</span><span class="sxs-lookup"><span data-stu-id="aa463-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="aa463-112">Laoala dimensiooni seadistamine</span><span class="sxs-lookup"><span data-stu-id="aa463-112">Storage dimension setup</span></span>

<span data-ttu-id="aa463-113">Näidissüsteemis on laoala dimensioonid sätestatud järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="aa463-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="aa463-114">Nimi</span><span class="sxs-lookup"><span data-stu-id="aa463-114">Name</span></span>      | <span data-ttu-id="aa463-115">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="aa463-115">Active</span></span> | <span data-ttu-id="aa463-116">Füüsiline ladu</span><span class="sxs-lookup"><span data-stu-id="aa463-116">Physical inventory</span></span> | <span data-ttu-id="aa463-117">Finantsiline laovaru</span><span class="sxs-lookup"><span data-stu-id="aa463-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="aa463-118">Koht</span><span class="sxs-lookup"><span data-stu-id="aa463-118">Site</span></span>      | <span data-ttu-id="aa463-119">Jah</span><span class="sxs-lookup"><span data-stu-id="aa463-119">Yes</span></span>    | <span data-ttu-id="aa463-120">Jah</span><span class="sxs-lookup"><span data-stu-id="aa463-120">Yes</span></span>                | <span data-ttu-id="aa463-121">Jah</span><span class="sxs-lookup"><span data-stu-id="aa463-121">Yes</span></span>                 |
| <span data-ttu-id="aa463-122">Ladu</span><span class="sxs-lookup"><span data-stu-id="aa463-122">Warehouse</span></span> | <span data-ttu-id="aa463-123">Jah</span><span class="sxs-lookup"><span data-stu-id="aa463-123">Yes</span></span>    | <span data-ttu-id="aa463-124">Jah</span><span class="sxs-lookup"><span data-stu-id="aa463-124">Yes</span></span>                | <span data-ttu-id="aa463-125">Ei</span><span class="sxs-lookup"><span data-stu-id="aa463-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="aa463-126">Laomudel</span><span class="sxs-lookup"><span data-stu-id="aa463-126">Inventory model</span></span>

<span data-ttu-id="aa463-127">Näidissüsteemi puhul on väljastatud toodete laomudel *FIFO* ning laomudeli sätte **Omahind** väärtus on *Kaasa füüsiline väärtus*.</span><span class="sxs-lookup"><span data-stu-id="aa463-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="aa463-128">Laokanded</span><span class="sxs-lookup"><span data-stu-id="aa463-128">Inventory transactions</span></span>

<span data-ttu-id="aa463-129">Väljastatud toote, mille kaubakood on *1000*, puhul on näidissüsteemis järgmised laokanded.</span><span class="sxs-lookup"><span data-stu-id="aa463-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="aa463-130">Viide</span><span class="sxs-lookup"><span data-stu-id="aa463-130">Reference</span></span>      | <span data-ttu-id="aa463-131">Koht</span><span class="sxs-lookup"><span data-stu-id="aa463-131">Site</span></span> | <span data-ttu-id="aa463-132">Ladu</span><span class="sxs-lookup"><span data-stu-id="aa463-132">Warehouse</span></span> | <span data-ttu-id="aa463-133">Sissetulek</span><span class="sxs-lookup"><span data-stu-id="aa463-133">Receipt</span></span>   | <span data-ttu-id="aa463-134">Väljastus</span><span class="sxs-lookup"><span data-stu-id="aa463-134">Issue</span></span> | <span data-ttu-id="aa463-135">Füüsiline kuupäev</span><span class="sxs-lookup"><span data-stu-id="aa463-135">Physical date</span></span> | <span data-ttu-id="aa463-136">Finantskuupäev</span><span class="sxs-lookup"><span data-stu-id="aa463-136">Financial date</span></span> | <span data-ttu-id="aa463-137">Kogus</span><span class="sxs-lookup"><span data-stu-id="aa463-137">Quantity</span></span> | <span data-ttu-id="aa463-138">Sisseostuhind</span><span class="sxs-lookup"><span data-stu-id="aa463-138">Cost amount</span></span> | <span data-ttu-id="aa463-139">Füüsiline omahind</span><span class="sxs-lookup"><span data-stu-id="aa463-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="aa463-140">Ostutellimus</span><span class="sxs-lookup"><span data-stu-id="aa463-140">Purchase order</span></span> | <span data-ttu-id="aa463-141">1</span><span class="sxs-lookup"><span data-stu-id="aa463-141">1</span></span>    | <span data-ttu-id="aa463-142">11</span><span class="sxs-lookup"><span data-stu-id="aa463-142">11</span></span>        | <span data-ttu-id="aa463-143">Ostetud</span><span class="sxs-lookup"><span data-stu-id="aa463-143">Purchased</span></span> |       | <span data-ttu-id="aa463-144">15. märts</span><span class="sxs-lookup"><span data-stu-id="aa463-144">March 15</span></span>      | <span data-ttu-id="aa463-145">15. märts</span><span class="sxs-lookup"><span data-stu-id="aa463-145">March 15</span></span>       | <span data-ttu-id="aa463-146">10</span><span class="sxs-lookup"><span data-stu-id="aa463-146">10</span></span>       | <span data-ttu-id="aa463-147">1000</span><span class="sxs-lookup"><span data-stu-id="aa463-147">1,000</span></span>       | <span data-ttu-id="aa463-148">1000</span><span class="sxs-lookup"><span data-stu-id="aa463-148">1,000</span></span>                |
| <span data-ttu-id="aa463-149">Ostutellimus</span><span class="sxs-lookup"><span data-stu-id="aa463-149">Purchase order</span></span> | <span data-ttu-id="aa463-150">2</span><span class="sxs-lookup"><span data-stu-id="aa463-150">2</span></span>    | <span data-ttu-id="aa463-151">21</span><span class="sxs-lookup"><span data-stu-id="aa463-151">21</span></span>        | <span data-ttu-id="aa463-152">Ostetud</span><span class="sxs-lookup"><span data-stu-id="aa463-152">Purchased</span></span> |       | <span data-ttu-id="aa463-153">15. märts</span><span class="sxs-lookup"><span data-stu-id="aa463-153">March 15</span></span>      | <span data-ttu-id="aa463-154">15. märts</span><span class="sxs-lookup"><span data-stu-id="aa463-154">March 15</span></span>       | <span data-ttu-id="aa463-155">10</span><span class="sxs-lookup"><span data-stu-id="aa463-155">10</span></span>       | <span data-ttu-id="aa463-156">2,000</span><span class="sxs-lookup"><span data-stu-id="aa463-156">2,000</span></span>       | <span data-ttu-id="aa463-157">2,000</span><span class="sxs-lookup"><span data-stu-id="aa463-157">2,000</span></span>                |
| <span data-ttu-id="aa463-158">Ostutellimus</span><span class="sxs-lookup"><span data-stu-id="aa463-158">Purchase order</span></span> | <span data-ttu-id="aa463-159">1</span><span class="sxs-lookup"><span data-stu-id="aa463-159">1</span></span>    | <span data-ttu-id="aa463-160">11</span><span class="sxs-lookup"><span data-stu-id="aa463-160">11</span></span>        | <span data-ttu-id="aa463-161">Vastuvõetud</span><span class="sxs-lookup"><span data-stu-id="aa463-161">Received</span></span>  |       | <span data-ttu-id="aa463-162">15. aprill</span><span class="sxs-lookup"><span data-stu-id="aa463-162">April 15</span></span>      |                | <span data-ttu-id="aa463-163">5</span><span class="sxs-lookup"><span data-stu-id="aa463-163">5</span></span>        |             | <span data-ttu-id="aa463-164">375</span><span class="sxs-lookup"><span data-stu-id="aa463-164">375</span></span>                  |
| <span data-ttu-id="aa463-165">Üleviimistellimus</span><span class="sxs-lookup"><span data-stu-id="aa463-165">Transfer order</span></span> | <span data-ttu-id="aa463-166">1</span><span class="sxs-lookup"><span data-stu-id="aa463-166">1</span></span>    | <span data-ttu-id="aa463-167">11</span><span class="sxs-lookup"><span data-stu-id="aa463-167">11</span></span>        |           | <span data-ttu-id="aa463-168">Müüdud</span><span class="sxs-lookup"><span data-stu-id="aa463-168">Sold</span></span>  | <span data-ttu-id="aa463-169">2. mai</span><span class="sxs-lookup"><span data-stu-id="aa463-169">May 2</span></span>         | <span data-ttu-id="aa463-170">2. mai</span><span class="sxs-lookup"><span data-stu-id="aa463-170">May 2</span></span>          | <span data-ttu-id="aa463-171">-5</span><span class="sxs-lookup"><span data-stu-id="aa463-171">-5</span></span>       | <span data-ttu-id="aa463-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="aa463-172">-458.33</span></span>     | <span data-ttu-id="aa463-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="aa463-173">-458.33</span></span>              |
| <span data-ttu-id="aa463-174">Üleviimistellimus</span><span class="sxs-lookup"><span data-stu-id="aa463-174">Transfer order</span></span> | <span data-ttu-id="aa463-175">1</span><span class="sxs-lookup"><span data-stu-id="aa463-175">1</span></span>    | <span data-ttu-id="aa463-176">12</span><span class="sxs-lookup"><span data-stu-id="aa463-176">12</span></span>        | <span data-ttu-id="aa463-177">Ostetud</span><span class="sxs-lookup"><span data-stu-id="aa463-177">Purchased</span></span> |       | <span data-ttu-id="aa463-178">2. mai</span><span class="sxs-lookup"><span data-stu-id="aa463-178">May 2</span></span>         | <span data-ttu-id="aa463-179">2. mai</span><span class="sxs-lookup"><span data-stu-id="aa463-179">May 2</span></span>          | <span data-ttu-id="aa463-180">5</span><span class="sxs-lookup"><span data-stu-id="aa463-180">5</span></span>        | <span data-ttu-id="aa463-181">458.33</span><span class="sxs-lookup"><span data-stu-id="aa463-181">458.33</span></span>      | <span data-ttu-id="aa463-182">458.33</span><span class="sxs-lookup"><span data-stu-id="aa463-182">458.33</span></span>               |
| <span data-ttu-id="aa463-183">Müügitellimus</span><span class="sxs-lookup"><span data-stu-id="aa463-183">Sales order</span></span>    | <span data-ttu-id="aa463-184">1</span><span class="sxs-lookup"><span data-stu-id="aa463-184">1</span></span>    | <span data-ttu-id="aa463-185">12</span><span class="sxs-lookup"><span data-stu-id="aa463-185">12</span></span>        |           | <span data-ttu-id="aa463-186">Müüdud</span><span class="sxs-lookup"><span data-stu-id="aa463-186">Sold</span></span>  | <span data-ttu-id="aa463-187">3. mai</span><span class="sxs-lookup"><span data-stu-id="aa463-187">May 3</span></span>         | <span data-ttu-id="aa463-188">3. mai</span><span class="sxs-lookup"><span data-stu-id="aa463-188">May 3</span></span>          | <span data-ttu-id="aa463-189">–1</span><span class="sxs-lookup"><span data-stu-id="aa463-189">-1</span></span>       | <span data-ttu-id="aa463-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="aa463-190">-91.67</span></span>      | <span data-ttu-id="aa463-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="aa463-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="aa463-192">Kuidas arvutatakse igas perioodis koguseid ja summasid?</span><span class="sxs-lookup"><span data-stu-id="aa463-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="aa463-193">Eelmistes jaotistes kirjeldatud näidisandmete abil saate käivitada **varude ajalise jaotuse** aruande, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="aa463-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="aa463-194">**Kuupäevaga:** *9. mai 2020*</span><span class="sxs-lookup"><span data-stu-id="aa463-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="aa463-195">**Koht:** *Kuva*</span><span class="sxs-lookup"><span data-stu-id="aa463-195">**Site:** *View*</span></span>
- <span data-ttu-id="aa463-196">**Ladu:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="aa463-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="aa463-197">**Kaubakood:** *Kokku*</span><span class="sxs-lookup"><span data-stu-id="aa463-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="aa463-198">**Ajalise jaotuse periood:** määrake see väli, et luua igakuiseid ajavahemikke.</span><span class="sxs-lookup"><span data-stu-id="aa463-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="aa463-199">Sellisel juhul sarnaneb loodud aruande sisu järgmise näitega.</span><span class="sxs-lookup"><span data-stu-id="aa463-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="aa463-200">Kaubakood</span><span class="sxs-lookup"><span data-stu-id="aa463-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-201">Koht</span><span class="sxs-lookup"><span data-stu-id="aa463-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-202">Laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="aa463-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-203">Laoseisu väärtus</span><span class="sxs-lookup"><span data-stu-id="aa463-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-204">Laoväärtuse kogus</span><span class="sxs-lookup"><span data-stu-id="aa463-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-205">Laoväärtus</span><span class="sxs-lookup"><span data-stu-id="aa463-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-206">Keskmine ühikukulu</span><span class="sxs-lookup"><span data-stu-id="aa463-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="aa463-207">01.05.2020–08.05.2020</span><span class="sxs-lookup"><span data-stu-id="aa463-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="aa463-208">01.04.2020–30.04.2020</span><span class="sxs-lookup"><span data-stu-id="aa463-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="aa463-209">01.03.2020–31.03.2020</span><span class="sxs-lookup"><span data-stu-id="aa463-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="aa463-210">P1: kogus</span><span class="sxs-lookup"><span data-stu-id="aa463-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="aa463-211">P1: summa</span><span class="sxs-lookup"><span data-stu-id="aa463-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="aa463-212">P2: kogus</span><span class="sxs-lookup"><span data-stu-id="aa463-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="aa463-213">P2: summa</span><span class="sxs-lookup"><span data-stu-id="aa463-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="aa463-214">P3: kogus</span><span class="sxs-lookup"><span data-stu-id="aa463-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="aa463-215">P3: summa</span><span class="sxs-lookup"><span data-stu-id="aa463-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="aa463-216">1000</span><span class="sxs-lookup"><span data-stu-id="aa463-216">1000</span></span></td>
    <td><span data-ttu-id="aa463-217">1</span><span class="sxs-lookup"><span data-stu-id="aa463-217">1</span></span></td>
    <td><span data-ttu-id="aa463-218">14</span><span class="sxs-lookup"><span data-stu-id="aa463-218">14</span></span></td>
    <td><span data-ttu-id="aa463-219">1283,33</span><span class="sxs-lookup"><span data-stu-id="aa463-219">1,283.33</span></span></td>
    <td><span data-ttu-id="aa463-220">14</span><span class="sxs-lookup"><span data-stu-id="aa463-220">14</span></span></td>
    <td><span data-ttu-id="aa463-221">1283,33</span><span class="sxs-lookup"><span data-stu-id="aa463-221">1,283.33</span></span></td>
    <td><span data-ttu-id="aa463-222">91,67</span><span class="sxs-lookup"><span data-stu-id="aa463-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="aa463-223">5,00</span><span class="sxs-lookup"><span data-stu-id="aa463-223">5.00</span></span></td>
    <td><span data-ttu-id="aa463-224">458,33</span><span class="sxs-lookup"><span data-stu-id="aa463-224">458.33</span></span></td>
    <td><span data-ttu-id="aa463-225">9,00</span><span class="sxs-lookup"><span data-stu-id="aa463-225">9.00</span></span></td>
    <td><span data-ttu-id="aa463-226">825,00</span><span class="sxs-lookup"><span data-stu-id="aa463-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="aa463-227">1000</span><span class="sxs-lookup"><span data-stu-id="aa463-227">1000</span></span></td>
    <td><span data-ttu-id="aa463-228">2</span><span class="sxs-lookup"><span data-stu-id="aa463-228">2</span></span></td>
    <td><span data-ttu-id="aa463-229">10</span><span class="sxs-lookup"><span data-stu-id="aa463-229">10</span></span></td>
    <td><span data-ttu-id="aa463-230">2000,00</span><span class="sxs-lookup"><span data-stu-id="aa463-230">2,000.00</span></span></td>
    <td><span data-ttu-id="aa463-231">10</span><span class="sxs-lookup"><span data-stu-id="aa463-231">10</span></span></td>
    <td><span data-ttu-id="aa463-232">2000,00</span><span class="sxs-lookup"><span data-stu-id="aa463-232">2,000.00</span></span></td>
    <td><span data-ttu-id="aa463-233">200,00</span><span class="sxs-lookup"><span data-stu-id="aa463-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="aa463-234">10,00</span><span class="sxs-lookup"><span data-stu-id="aa463-234">10.00</span></span></td>
    <td><span data-ttu-id="aa463-235">2000,00</span><span class="sxs-lookup"><span data-stu-id="aa463-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="aa463-236"><strong>1000 kokku</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="aa463-237"><strong>24,00</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="aa463-238"><strong>3283,33</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="aa463-239"><strong>5,00</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="aa463-240"><strong>458,33</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="aa463-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="aa463-242"><strong>2825,00</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="aa463-243">Pöörake selles näidisaruandes tähelepanu järgmistele üksikasjadele.</span><span class="sxs-lookup"><span data-stu-id="aa463-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="aa463-244">Aruandes toodud väärtused **Laoväärtuse kogus**, **Laoväärtus** ja **Keskmine ühikukulu** on finantsilise varude dimensiooni (praegusel juhul **Koht**) väärtused.</span><span class="sxs-lookup"><span data-stu-id="aa463-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="aa463-245">Näiteks kuvatakse koha 1 puhul aruandes järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="aa463-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="aa463-246">**Laoväärtuse koguse** väärtus on *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="aa463-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="aa463-247">**Laoväärtuse** väärtus on *1283,33* (= 1000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="aa463-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="aa463-248">**Keskmine ühikukulu** on *91,67*.</span><span class="sxs-lookup"><span data-stu-id="aa463-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="aa463-249">Igas perioodis arvutatakse väärtused **Laoseisu väärtus** ja **Summa** väärtuse **Keskmine ühikukulu** alusel.</span><span class="sxs-lookup"><span data-stu-id="aa463-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="aa463-250">Aruandes määratletakse iga perioodi laos olev kogus sellel perioodil vastuvõetud varude koguste kokkuliitmise kaudu.</span><span class="sxs-lookup"><span data-stu-id="aa463-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="aa463-251">Seejärel rakendatakse kogu väljastatud koguse lahutamiseks esimesena sisse, esimesena välja (FIFO) põhimõtet, sõltumata laomudelist, mida kaubad kasutavad.</span><span class="sxs-lookup"><span data-stu-id="aa463-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="aa463-252">Kui käivitate sama aruande uuesti, kuid määrate seekord väljade **Koht** ja **Ladu** väärtuseks *Kuva*, sarnaneb uus aruanne järgmise näitega.</span><span class="sxs-lookup"><span data-stu-id="aa463-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="aa463-253">Kaubakood</span><span class="sxs-lookup"><span data-stu-id="aa463-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-254">Koht</span><span class="sxs-lookup"><span data-stu-id="aa463-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-255">Ladu</span><span class="sxs-lookup"><span data-stu-id="aa463-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-256">Laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="aa463-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-257">Laoseisu väärtus</span><span class="sxs-lookup"><span data-stu-id="aa463-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-258">Laoväärtuse kogus</span><span class="sxs-lookup"><span data-stu-id="aa463-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-259">Laoväärtus</span><span class="sxs-lookup"><span data-stu-id="aa463-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-260">Keskmine ühikukulu</span><span class="sxs-lookup"><span data-stu-id="aa463-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="aa463-261">01.05.2020–08.05.2020</span><span class="sxs-lookup"><span data-stu-id="aa463-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="aa463-262">01.04.2020–30.04.2020</span><span class="sxs-lookup"><span data-stu-id="aa463-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="aa463-263">01.03.2020–31.03.2020</span><span class="sxs-lookup"><span data-stu-id="aa463-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="aa463-264">P1: kogus</span><span class="sxs-lookup"><span data-stu-id="aa463-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="aa463-265">P1: summa</span><span class="sxs-lookup"><span data-stu-id="aa463-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="aa463-266">P2: kogus</span><span class="sxs-lookup"><span data-stu-id="aa463-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="aa463-267">P2: summa</span><span class="sxs-lookup"><span data-stu-id="aa463-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="aa463-268">P3: kogus</span><span class="sxs-lookup"><span data-stu-id="aa463-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="aa463-269">P3: summa</span><span class="sxs-lookup"><span data-stu-id="aa463-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="aa463-270">1000</span><span class="sxs-lookup"><span data-stu-id="aa463-270">1000</span></span></td>
    <td><span data-ttu-id="aa463-271">1</span><span class="sxs-lookup"><span data-stu-id="aa463-271">1</span></span></td>
    <td><span data-ttu-id="aa463-272">11</span><span class="sxs-lookup"><span data-stu-id="aa463-272">11</span></span></td>
    <td><span data-ttu-id="aa463-273">10</span><span class="sxs-lookup"><span data-stu-id="aa463-273">10</span></span></td>
    <td><span data-ttu-id="aa463-274">916,67</span><span class="sxs-lookup"><span data-stu-id="aa463-274">916.67</span></span></td>
    <td><span data-ttu-id="aa463-275">14</span><span class="sxs-lookup"><span data-stu-id="aa463-275">14</span></span></td>
    <td><span data-ttu-id="aa463-276">1283,33</span><span class="sxs-lookup"><span data-stu-id="aa463-276">1,283.33</span></span></td>
    <td><span data-ttu-id="aa463-277">91,67</span><span class="sxs-lookup"><span data-stu-id="aa463-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="aa463-278">5,00</span><span class="sxs-lookup"><span data-stu-id="aa463-278">5.00</span></span></td>
    <td><span data-ttu-id="aa463-279">458,33</span><span class="sxs-lookup"><span data-stu-id="aa463-279">458.33</span></span></td>
    <td><span data-ttu-id="aa463-280">5,00</span><span class="sxs-lookup"><span data-stu-id="aa463-280">5.00</span></span></td>
    <td><span data-ttu-id="aa463-281">458,33</span><span class="sxs-lookup"><span data-stu-id="aa463-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="aa463-282">1000</span><span class="sxs-lookup"><span data-stu-id="aa463-282">1000</span></span></td>
    <td><span data-ttu-id="aa463-283">1</span><span class="sxs-lookup"><span data-stu-id="aa463-283">1</span></span></td>
    <td><span data-ttu-id="aa463-284">12</span><span class="sxs-lookup"><span data-stu-id="aa463-284">12</span></span></td>
    <td><span data-ttu-id="aa463-285">4</span><span class="sxs-lookup"><span data-stu-id="aa463-285">4</span></span></td>
    <td><span data-ttu-id="aa463-286">366,67</span><span class="sxs-lookup"><span data-stu-id="aa463-286">366.67</span></span></td>
    <td><span data-ttu-id="aa463-287">14</span><span class="sxs-lookup"><span data-stu-id="aa463-287">14</span></span></td>
    <td><span data-ttu-id="aa463-288">1283,33</span><span class="sxs-lookup"><span data-stu-id="aa463-288">1,283.33</span></span></td>
    <td><span data-ttu-id="aa463-289">91,67</span><span class="sxs-lookup"><span data-stu-id="aa463-289">91.67</span></span></td>
    <td><span data-ttu-id="aa463-290">4,00</span><span class="sxs-lookup"><span data-stu-id="aa463-290">4.00</span></span></td>
    <td><span data-ttu-id="aa463-291">366,67</span><span class="sxs-lookup"><span data-stu-id="aa463-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="aa463-292">1000</span><span class="sxs-lookup"><span data-stu-id="aa463-292">1000</span></span></td>
    <td><span data-ttu-id="aa463-293">2</span><span class="sxs-lookup"><span data-stu-id="aa463-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="aa463-294">10</span><span class="sxs-lookup"><span data-stu-id="aa463-294">10</span></span></td>
    <td><span data-ttu-id="aa463-295">2000,00</span><span class="sxs-lookup"><span data-stu-id="aa463-295">2,000.00</span></span></td>
    <td><span data-ttu-id="aa463-296">10</span><span class="sxs-lookup"><span data-stu-id="aa463-296">10</span></span></td>
    <td><span data-ttu-id="aa463-297">2000,00</span><span class="sxs-lookup"><span data-stu-id="aa463-297">2,000.00</span></span></td>
    <td><span data-ttu-id="aa463-298">200,00</span><span class="sxs-lookup"><span data-stu-id="aa463-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="aa463-299">10,00</span><span class="sxs-lookup"><span data-stu-id="aa463-299">10.00</span></span></td>
    <td><span data-ttu-id="aa463-300">2000,00</span><span class="sxs-lookup"><span data-stu-id="aa463-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="aa463-301"><strong>1000 kokku</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="aa463-302"><strong>24,00</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="aa463-303"><strong>3283,33</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="aa463-304"><strong>4,00</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="aa463-305"><strong>366,67</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="aa463-306"><strong>5,00</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="aa463-307"><strong>458,33</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="aa463-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="aa463-309"><strong>2458,33</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="aa463-310">Seekord on koht 1 jagatud kaheks reaks: üks lao 11 ja üks lao 12 jaoks.</span><span class="sxs-lookup"><span data-stu-id="aa463-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="aa463-311">Kuid väärtused **Laoväärtuse kogus**, **Laoväärtus** ja **Keskmine ühikukulu** on samad, kuna **Ladu** pole finantsiline varude dimensioon.</span><span class="sxs-lookup"><span data-stu-id="aa463-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="aa463-312">Lisaks pange tähele, et koha 1 koguse jaotus on erinev.</span><span class="sxs-lookup"><span data-stu-id="aa463-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="aa463-313">Esimeses käivitatud aruandes eiras süsteem samas kohas toimunud üleviimistellimust ja lahutas müügiarve koguse koha 1 perioodist **01.03.2020–31.03.2020**.</span><span class="sxs-lookup"><span data-stu-id="aa463-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="aa463-314">Kuid uues aruandes lahutab süsteem müügiarve koguse lao 12 perioodist **01.05.2020–08.05.2020**.</span><span class="sxs-lookup"><span data-stu-id="aa463-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="aa463-315">Lao sulgemise mõju</span><span class="sxs-lookup"><span data-stu-id="aa463-315">Effects of inventory closing</span></span>

<span data-ttu-id="aa463-316">Kui käivitate lao sulgemise maikuu jaoks ja käivitate seejärel eelmise aruande uuesti, kuid seadistate välja **Kuupäevaga** väärtuseks *31. mai 2020*, peaksite märkama järgmisi tulemusi.</span><span class="sxs-lookup"><span data-stu-id="aa463-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="aa463-317">Väärtused **Laoväärtus** ja **Keskmine ühikukulu** on uuendatud.</span><span class="sxs-lookup"><span data-stu-id="aa463-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="aa463-318">Iga perioodi puhul on väärtused **Laoseisu väärtus** ja **Summa** samuti vastavalt uuendatud.</span><span class="sxs-lookup"><span data-stu-id="aa463-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="aa463-319">Uus aruanne sarnaneb järgmise näitega.</span><span class="sxs-lookup"><span data-stu-id="aa463-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="aa463-320">Kaubakood</span><span class="sxs-lookup"><span data-stu-id="aa463-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-321">Koht</span><span class="sxs-lookup"><span data-stu-id="aa463-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-322">Ladu</span><span class="sxs-lookup"><span data-stu-id="aa463-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-323">Laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="aa463-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-324">Laoseisu väärtus</span><span class="sxs-lookup"><span data-stu-id="aa463-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-325">Laoväärtuse kogus</span><span class="sxs-lookup"><span data-stu-id="aa463-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-326">Laoväärtus</span><span class="sxs-lookup"><span data-stu-id="aa463-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="aa463-327">Keskmine ühikukulu</span><span class="sxs-lookup"><span data-stu-id="aa463-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="aa463-328">01.05.2020–31.05.2020</span><span class="sxs-lookup"><span data-stu-id="aa463-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="aa463-329">01.04.2020–30.04.2020</span><span class="sxs-lookup"><span data-stu-id="aa463-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="aa463-330">01.03.2020–31.03.2020</span><span class="sxs-lookup"><span data-stu-id="aa463-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="aa463-331">P1: kogus</span><span class="sxs-lookup"><span data-stu-id="aa463-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="aa463-332">P1: summa</span><span class="sxs-lookup"><span data-stu-id="aa463-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="aa463-333">P2: kogus</span><span class="sxs-lookup"><span data-stu-id="aa463-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="aa463-334">P2: summa</span><span class="sxs-lookup"><span data-stu-id="aa463-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="aa463-335">P3: kogus</span><span class="sxs-lookup"><span data-stu-id="aa463-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="aa463-336">P3: summa</span><span class="sxs-lookup"><span data-stu-id="aa463-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="aa463-337">1000</span><span class="sxs-lookup"><span data-stu-id="aa463-337">1000</span></span></td>
    <td><span data-ttu-id="aa463-338">1</span><span class="sxs-lookup"><span data-stu-id="aa463-338">1</span></span></td>
    <td><span data-ttu-id="aa463-339">11</span><span class="sxs-lookup"><span data-stu-id="aa463-339">11</span></span></td>
    <td><span data-ttu-id="aa463-340">10</span><span class="sxs-lookup"><span data-stu-id="aa463-340">10</span></span></td>
    <td><span data-ttu-id="aa463-341">910,70</span><span class="sxs-lookup"><span data-stu-id="aa463-341">910.70</span></span></td>
    <td><span data-ttu-id="aa463-342">14</span><span class="sxs-lookup"><span data-stu-id="aa463-342">14</span></span></td>
    <td><span data-ttu-id="aa463-343">1275,00</span><span class="sxs-lookup"><span data-stu-id="aa463-343">1,275.00</span></span></td>
    <td><span data-ttu-id="aa463-344">91,07</span><span class="sxs-lookup"><span data-stu-id="aa463-344">91.07</span></span></td>
    <td><span data-ttu-id="aa463-345">0,00</span><span class="sxs-lookup"><span data-stu-id="aa463-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="aa463-346">5,00</span><span class="sxs-lookup"><span data-stu-id="aa463-346">5.00</span></span></td>
    <td><span data-ttu-id="aa463-347">455,36</span><span class="sxs-lookup"><span data-stu-id="aa463-347">455.36</span></span></td>
    <td><span data-ttu-id="aa463-348">5,00</span><span class="sxs-lookup"><span data-stu-id="aa463-348">5.00</span></span></td>
    <td><span data-ttu-id="aa463-349">455,36</span><span class="sxs-lookup"><span data-stu-id="aa463-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="aa463-350">1000</span><span class="sxs-lookup"><span data-stu-id="aa463-350">1000</span></span></td>
    <td><span data-ttu-id="aa463-351">1</span><span class="sxs-lookup"><span data-stu-id="aa463-351">1</span></span></td>
    <td><span data-ttu-id="aa463-352">12</span><span class="sxs-lookup"><span data-stu-id="aa463-352">12</span></span></td>
    <td><span data-ttu-id="aa463-353">4</span><span class="sxs-lookup"><span data-stu-id="aa463-353">4</span></span></td>
    <td><span data-ttu-id="aa463-354">364,29</span><span class="sxs-lookup"><span data-stu-id="aa463-354">364.29</span></span></td>
    <td><span data-ttu-id="aa463-355">14</span><span class="sxs-lookup"><span data-stu-id="aa463-355">14</span></span></td>
    <td><span data-ttu-id="aa463-356">1275,00</span><span class="sxs-lookup"><span data-stu-id="aa463-356">1,275.00</span></span></td>
    <td><span data-ttu-id="aa463-357">91,07</span><span class="sxs-lookup"><span data-stu-id="aa463-357">91.07</span></span></td>
    <td><span data-ttu-id="aa463-358">4,00</span><span class="sxs-lookup"><span data-stu-id="aa463-358">4.00</span></span></td>
    <td><span data-ttu-id="aa463-359">364,29</span><span class="sxs-lookup"><span data-stu-id="aa463-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="aa463-360">1000</span><span class="sxs-lookup"><span data-stu-id="aa463-360">1000</span></span></td>
    <td><span data-ttu-id="aa463-361">2</span><span class="sxs-lookup"><span data-stu-id="aa463-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="aa463-362">10</span><span class="sxs-lookup"><span data-stu-id="aa463-362">10</span></span></td>
    <td><span data-ttu-id="aa463-363">2000,00</span><span class="sxs-lookup"><span data-stu-id="aa463-363">2,000.00</span></span></td>
    <td><span data-ttu-id="aa463-364">10</span><span class="sxs-lookup"><span data-stu-id="aa463-364">10</span></span></td>
    <td><span data-ttu-id="aa463-365">2000,00</span><span class="sxs-lookup"><span data-stu-id="aa463-365">2,000.00</span></span></td>
    <td><span data-ttu-id="aa463-366">200,00</span><span class="sxs-lookup"><span data-stu-id="aa463-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="aa463-367">10,00</span><span class="sxs-lookup"><span data-stu-id="aa463-367">10.00</span></span></td>
    <td><span data-ttu-id="aa463-368">2000,00</span><span class="sxs-lookup"><span data-stu-id="aa463-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="aa463-369"><strong>1000 kokku</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="aa463-370"><strong>24,00</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="aa463-371"><strong>3275,00</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="aa463-372"><strong>4,00</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="aa463-373"><strong>364,29</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="aa463-374"><strong>5,00</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="aa463-375"><strong>455,36</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="aa463-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="aa463-377"><strong>2455,36</strong></span><span class="sxs-lookup"><span data-stu-id="aa463-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
