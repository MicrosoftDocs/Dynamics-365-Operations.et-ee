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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6e708e4dc818f20fc8d835053da75c2fe9c98f6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426239"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="a5b2b-103">Varude ajalise jaotuse aruande näited ja loogika</span><span class="sxs-lookup"><span data-stu-id="a5b2b-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5b2b-104">Selles teemas on toodud näited selle kohta, kuidas tõlgendada **varude ajalise jaotuse** aruande tulemusi.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="a5b2b-105">See aruanne jagab valitud kauba või kaubagrupi laos oleva koguse ja laoväärtused mitmeks perioodiks.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="a5b2b-106">Teema hõlmab ka aruande sisemist loogikat.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="a5b2b-107">Selles teemas on toodud näited, mis sisalduvad standardses **varude ajalise jaotuse** aruandes.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="a5b2b-108">Siiski soovitame üldiselt kasutada selle aruande versiooni [Varude ajalise jaotuse aruande talletamine](inventory-aging-report-storage.md), eriti kui te peate töötlema palju kaupu ja ladusid.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="a5b2b-109">Varude ajalise jaotuse aruande talletamine salvestab kõik teie loodud aruanded, kuvab tulemused interaktiivse lehena ja diagrammina ning võimaldab teil eksportida kõiki salvestatud aruandeid.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="a5b2b-110">Näidetes kasutatavad näidisandmed</span><span class="sxs-lookup"><span data-stu-id="a5b2b-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="a5b2b-111">Teema näited põhinevad selles jaotises kirjeldatud laokannete näidisandmetel.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="a5b2b-112">Laoala dimensiooni seadistamine</span><span class="sxs-lookup"><span data-stu-id="a5b2b-112">Storage dimension setup</span></span>

<span data-ttu-id="a5b2b-113">Näidissüsteemis on laoala dimensioonid sätestatud järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="a5b2b-114">Nimi</span><span class="sxs-lookup"><span data-stu-id="a5b2b-114">Name</span></span>      | <span data-ttu-id="a5b2b-115">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="a5b2b-115">Active</span></span> | <span data-ttu-id="a5b2b-116">Füüsiline ladu</span><span class="sxs-lookup"><span data-stu-id="a5b2b-116">Physical inventory</span></span> | <span data-ttu-id="a5b2b-117">Finantsiline laovaru</span><span class="sxs-lookup"><span data-stu-id="a5b2b-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="a5b2b-118">Koht</span><span class="sxs-lookup"><span data-stu-id="a5b2b-118">Site</span></span>      | <span data-ttu-id="a5b2b-119">Jah</span><span class="sxs-lookup"><span data-stu-id="a5b2b-119">Yes</span></span>    | <span data-ttu-id="a5b2b-120">Jah</span><span class="sxs-lookup"><span data-stu-id="a5b2b-120">Yes</span></span>                | <span data-ttu-id="a5b2b-121">Jah</span><span class="sxs-lookup"><span data-stu-id="a5b2b-121">Yes</span></span>                 |
| <span data-ttu-id="a5b2b-122">Ladu</span><span class="sxs-lookup"><span data-stu-id="a5b2b-122">Warehouse</span></span> | <span data-ttu-id="a5b2b-123">Jah</span><span class="sxs-lookup"><span data-stu-id="a5b2b-123">Yes</span></span>    | <span data-ttu-id="a5b2b-124">Jah</span><span class="sxs-lookup"><span data-stu-id="a5b2b-124">Yes</span></span>                | <span data-ttu-id="a5b2b-125">Ei</span><span class="sxs-lookup"><span data-stu-id="a5b2b-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="a5b2b-126">Laomudel</span><span class="sxs-lookup"><span data-stu-id="a5b2b-126">Inventory model</span></span>

<span data-ttu-id="a5b2b-127">Näidissüsteemi puhul on väljastatud toodete laomudel *FIFO* ning laomudeli sätte **Omahind** väärtus on *Kaasa füüsiline väärtus*.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="a5b2b-128">Laokanded</span><span class="sxs-lookup"><span data-stu-id="a5b2b-128">Inventory transactions</span></span>

<span data-ttu-id="a5b2b-129">Väljastatud toote, mille kaubakood on *1000*, puhul on näidissüsteemis järgmised laokanded.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="a5b2b-130">Viide</span><span class="sxs-lookup"><span data-stu-id="a5b2b-130">Reference</span></span>      | <span data-ttu-id="a5b2b-131">Koht</span><span class="sxs-lookup"><span data-stu-id="a5b2b-131">Site</span></span> | <span data-ttu-id="a5b2b-132">Ladu</span><span class="sxs-lookup"><span data-stu-id="a5b2b-132">Warehouse</span></span> | <span data-ttu-id="a5b2b-133">Sissetulek</span><span class="sxs-lookup"><span data-stu-id="a5b2b-133">Receipt</span></span>   | <span data-ttu-id="a5b2b-134">Väljastus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-134">Issue</span></span> | <span data-ttu-id="a5b2b-135">Füüsiline kuupäev</span><span class="sxs-lookup"><span data-stu-id="a5b2b-135">Physical date</span></span> | <span data-ttu-id="a5b2b-136">Finantskuupäev</span><span class="sxs-lookup"><span data-stu-id="a5b2b-136">Financial date</span></span> | <span data-ttu-id="a5b2b-137">Kogus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-137">Quantity</span></span> | <span data-ttu-id="a5b2b-138">Sisseostuhind</span><span class="sxs-lookup"><span data-stu-id="a5b2b-138">Cost amount</span></span> | <span data-ttu-id="a5b2b-139">Füüsiline omahind</span><span class="sxs-lookup"><span data-stu-id="a5b2b-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="a5b2b-140">Ostutellimus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-140">Purchase order</span></span> | <span data-ttu-id="a5b2b-141">1</span><span class="sxs-lookup"><span data-stu-id="a5b2b-141">1</span></span>    | <span data-ttu-id="a5b2b-142">11</span><span class="sxs-lookup"><span data-stu-id="a5b2b-142">11</span></span>        | <span data-ttu-id="a5b2b-143">Ostetud</span><span class="sxs-lookup"><span data-stu-id="a5b2b-143">Purchased</span></span> |       | <span data-ttu-id="a5b2b-144">15. märts</span><span class="sxs-lookup"><span data-stu-id="a5b2b-144">March 15</span></span>      | <span data-ttu-id="a5b2b-145">15. märts</span><span class="sxs-lookup"><span data-stu-id="a5b2b-145">March 15</span></span>       | <span data-ttu-id="a5b2b-146">10</span><span class="sxs-lookup"><span data-stu-id="a5b2b-146">10</span></span>       | <span data-ttu-id="a5b2b-147">1000</span><span class="sxs-lookup"><span data-stu-id="a5b2b-147">1,000</span></span>       | <span data-ttu-id="a5b2b-148">1000</span><span class="sxs-lookup"><span data-stu-id="a5b2b-148">1,000</span></span>                |
| <span data-ttu-id="a5b2b-149">Ostutellimus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-149">Purchase order</span></span> | <span data-ttu-id="a5b2b-150">2</span><span class="sxs-lookup"><span data-stu-id="a5b2b-150">2</span></span>    | <span data-ttu-id="a5b2b-151">21</span><span class="sxs-lookup"><span data-stu-id="a5b2b-151">21</span></span>        | <span data-ttu-id="a5b2b-152">Ostetud</span><span class="sxs-lookup"><span data-stu-id="a5b2b-152">Purchased</span></span> |       | <span data-ttu-id="a5b2b-153">15. märts</span><span class="sxs-lookup"><span data-stu-id="a5b2b-153">March 15</span></span>      | <span data-ttu-id="a5b2b-154">15. märts</span><span class="sxs-lookup"><span data-stu-id="a5b2b-154">March 15</span></span>       | <span data-ttu-id="a5b2b-155">10</span><span class="sxs-lookup"><span data-stu-id="a5b2b-155">10</span></span>       | <span data-ttu-id="a5b2b-156">2,000</span><span class="sxs-lookup"><span data-stu-id="a5b2b-156">2,000</span></span>       | <span data-ttu-id="a5b2b-157">2,000</span><span class="sxs-lookup"><span data-stu-id="a5b2b-157">2,000</span></span>                |
| <span data-ttu-id="a5b2b-158">Ostutellimus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-158">Purchase order</span></span> | <span data-ttu-id="a5b2b-159">1</span><span class="sxs-lookup"><span data-stu-id="a5b2b-159">1</span></span>    | <span data-ttu-id="a5b2b-160">11</span><span class="sxs-lookup"><span data-stu-id="a5b2b-160">11</span></span>        | <span data-ttu-id="a5b2b-161">Vastuvõetud</span><span class="sxs-lookup"><span data-stu-id="a5b2b-161">Received</span></span>  |       | <span data-ttu-id="a5b2b-162">15. aprill</span><span class="sxs-lookup"><span data-stu-id="a5b2b-162">April 15</span></span>      |                | <span data-ttu-id="a5b2b-163">5</span><span class="sxs-lookup"><span data-stu-id="a5b2b-163">5</span></span>        |             | <span data-ttu-id="a5b2b-164">375</span><span class="sxs-lookup"><span data-stu-id="a5b2b-164">375</span></span>                  |
| <span data-ttu-id="a5b2b-165">Üleviimistellimus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-165">Transfer order</span></span> | <span data-ttu-id="a5b2b-166">1</span><span class="sxs-lookup"><span data-stu-id="a5b2b-166">1</span></span>    | <span data-ttu-id="a5b2b-167">11</span><span class="sxs-lookup"><span data-stu-id="a5b2b-167">11</span></span>        |           | <span data-ttu-id="a5b2b-168">Müüdud</span><span class="sxs-lookup"><span data-stu-id="a5b2b-168">Sold</span></span>  | <span data-ttu-id="a5b2b-169">2. mai</span><span class="sxs-lookup"><span data-stu-id="a5b2b-169">May 2</span></span>         | <span data-ttu-id="a5b2b-170">2. mai</span><span class="sxs-lookup"><span data-stu-id="a5b2b-170">May 2</span></span>          | <span data-ttu-id="a5b2b-171">-5</span><span class="sxs-lookup"><span data-stu-id="a5b2b-171">-5</span></span>       | <span data-ttu-id="a5b2b-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="a5b2b-172">-458.33</span></span>     | <span data-ttu-id="a5b2b-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="a5b2b-173">-458.33</span></span>              |
| <span data-ttu-id="a5b2b-174">Üleviimistellimus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-174">Transfer order</span></span> | <span data-ttu-id="a5b2b-175">1</span><span class="sxs-lookup"><span data-stu-id="a5b2b-175">1</span></span>    | <span data-ttu-id="a5b2b-176">12</span><span class="sxs-lookup"><span data-stu-id="a5b2b-176">12</span></span>        | <span data-ttu-id="a5b2b-177">Ostetud</span><span class="sxs-lookup"><span data-stu-id="a5b2b-177">Purchased</span></span> |       | <span data-ttu-id="a5b2b-178">2. mai</span><span class="sxs-lookup"><span data-stu-id="a5b2b-178">May 2</span></span>         | <span data-ttu-id="a5b2b-179">2. mai</span><span class="sxs-lookup"><span data-stu-id="a5b2b-179">May 2</span></span>          | <span data-ttu-id="a5b2b-180">5</span><span class="sxs-lookup"><span data-stu-id="a5b2b-180">5</span></span>        | <span data-ttu-id="a5b2b-181">458.33</span><span class="sxs-lookup"><span data-stu-id="a5b2b-181">458.33</span></span>      | <span data-ttu-id="a5b2b-182">458.33</span><span class="sxs-lookup"><span data-stu-id="a5b2b-182">458.33</span></span>               |
| <span data-ttu-id="a5b2b-183">Müügitellimus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-183">Sales order</span></span>    | <span data-ttu-id="a5b2b-184">1</span><span class="sxs-lookup"><span data-stu-id="a5b2b-184">1</span></span>    | <span data-ttu-id="a5b2b-185">12</span><span class="sxs-lookup"><span data-stu-id="a5b2b-185">12</span></span>        |           | <span data-ttu-id="a5b2b-186">Müüdud</span><span class="sxs-lookup"><span data-stu-id="a5b2b-186">Sold</span></span>  | <span data-ttu-id="a5b2b-187">3. mai</span><span class="sxs-lookup"><span data-stu-id="a5b2b-187">May 3</span></span>         | <span data-ttu-id="a5b2b-188">3. mai</span><span class="sxs-lookup"><span data-stu-id="a5b2b-188">May 3</span></span>          | <span data-ttu-id="a5b2b-189">–1</span><span class="sxs-lookup"><span data-stu-id="a5b2b-189">-1</span></span>       | <span data-ttu-id="a5b2b-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="a5b2b-190">-91.67</span></span>      | <span data-ttu-id="a5b2b-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="a5b2b-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="a5b2b-192">Kuidas arvutatakse igas perioodis koguseid ja summasid?</span><span class="sxs-lookup"><span data-stu-id="a5b2b-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="a5b2b-193">Eelmistes jaotistes kirjeldatud näidisandmete abil saate käivitada **varude ajalise jaotuse** aruande, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="a5b2b-194">**Kuupäevaga:** *9. mai 2020*</span><span class="sxs-lookup"><span data-stu-id="a5b2b-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="a5b2b-195">**Koht:** *Kuva*</span><span class="sxs-lookup"><span data-stu-id="a5b2b-195">**Site:** *View*</span></span>
- <span data-ttu-id="a5b2b-196">**Ladu:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="a5b2b-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="a5b2b-197">**Kaubakood:** *Kokku*</span><span class="sxs-lookup"><span data-stu-id="a5b2b-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="a5b2b-198">**Ajalise jaotuse periood:** määrake see väli, et luua igakuiseid ajavahemikke.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="a5b2b-199">Sellisel juhul sarnaneb loodud aruande sisu järgmise näitega.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="a5b2b-200">Kaubakood</span><span class="sxs-lookup"><span data-stu-id="a5b2b-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-201">Koht</span><span class="sxs-lookup"><span data-stu-id="a5b2b-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-202">Laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-203">Laoseisu väärtus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-204">Laoväärtuse kogus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-205">Laoväärtus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-206">Keskmine ühikukulu</span><span class="sxs-lookup"><span data-stu-id="a5b2b-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="a5b2b-207">01.05.2020–08.05.2020</span><span class="sxs-lookup"><span data-stu-id="a5b2b-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a5b2b-208">01.04.2020–30.04.2020</span><span class="sxs-lookup"><span data-stu-id="a5b2b-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a5b2b-209">01.03.2020–31.03.2020</span><span class="sxs-lookup"><span data-stu-id="a5b2b-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="a5b2b-210">P1: kogus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="a5b2b-211">P1: summa</span><span class="sxs-lookup"><span data-stu-id="a5b2b-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="a5b2b-212">P2: kogus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="a5b2b-213">P2: summa</span><span class="sxs-lookup"><span data-stu-id="a5b2b-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="a5b2b-214">P3: kogus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="a5b2b-215">P3: summa</span><span class="sxs-lookup"><span data-stu-id="a5b2b-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="a5b2b-216">1000</span><span class="sxs-lookup"><span data-stu-id="a5b2b-216">1000</span></span></td>
    <td><span data-ttu-id="a5b2b-217">1</span><span class="sxs-lookup"><span data-stu-id="a5b2b-217">1</span></span></td>
    <td><span data-ttu-id="a5b2b-218">14</span><span class="sxs-lookup"><span data-stu-id="a5b2b-218">14</span></span></td>
    <td><span data-ttu-id="a5b2b-219">1283,33</span><span class="sxs-lookup"><span data-stu-id="a5b2b-219">1,283.33</span></span></td>
    <td><span data-ttu-id="a5b2b-220">14</span><span class="sxs-lookup"><span data-stu-id="a5b2b-220">14</span></span></td>
    <td><span data-ttu-id="a5b2b-221">1283,33</span><span class="sxs-lookup"><span data-stu-id="a5b2b-221">1,283.33</span></span></td>
    <td><span data-ttu-id="a5b2b-222">91,67</span><span class="sxs-lookup"><span data-stu-id="a5b2b-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a5b2b-223">5,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-223">5.00</span></span></td>
    <td><span data-ttu-id="a5b2b-224">458,33</span><span class="sxs-lookup"><span data-stu-id="a5b2b-224">458.33</span></span></td>
    <td><span data-ttu-id="a5b2b-225">9,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-225">9.00</span></span></td>
    <td><span data-ttu-id="a5b2b-226">825,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="a5b2b-227">1000</span><span class="sxs-lookup"><span data-stu-id="a5b2b-227">1000</span></span></td>
    <td><span data-ttu-id="a5b2b-228">2</span><span class="sxs-lookup"><span data-stu-id="a5b2b-228">2</span></span></td>
    <td><span data-ttu-id="a5b2b-229">10</span><span class="sxs-lookup"><span data-stu-id="a5b2b-229">10</span></span></td>
    <td><span data-ttu-id="a5b2b-230">2000,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-230">2,000.00</span></span></td>
    <td><span data-ttu-id="a5b2b-231">10</span><span class="sxs-lookup"><span data-stu-id="a5b2b-231">10</span></span></td>
    <td><span data-ttu-id="a5b2b-232">2000,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-232">2,000.00</span></span></td>
    <td><span data-ttu-id="a5b2b-233">200,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a5b2b-234">10,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-234">10.00</span></span></td>
    <td><span data-ttu-id="a5b2b-235">2000,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="a5b2b-236"><strong>1000 kokku</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="a5b2b-237"><strong>24,00</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="a5b2b-238"><strong>3283,33</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a5b2b-239"><strong>5,00</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="a5b2b-240"><strong>458,33</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="a5b2b-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="a5b2b-242"><strong>2825,00</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="a5b2b-243">Pöörake selles näidisaruandes tähelepanu järgmistele üksikasjadele.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="a5b2b-244">Aruandes toodud väärtused **Laoväärtuse kogus**, **Laoväärtus** ja **Keskmine ühikukulu** on finantsilise varude dimensiooni (praegusel juhul **Koht**) väärtused.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="a5b2b-245">Näiteks kuvatakse koha 1 puhul aruandes järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="a5b2b-246">**Laoväärtuse koguse** väärtus on *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="a5b2b-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="a5b2b-247">**Laoväärtuse** väärtus on *1283,33* (= 1000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="a5b2b-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="a5b2b-248">**Keskmine ühikukulu** on *91,67*.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="a5b2b-249">Igas perioodis arvutatakse väärtused **Laoseisu väärtus** ja **Summa** väärtuse **Keskmine ühikukulu** alusel.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="a5b2b-250">Aruandes määratletakse iga perioodi laos olev kogus sellel perioodil vastuvõetud varude koguste kokkuliitmise kaudu.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="a5b2b-251">Seejärel rakendatakse kogu väljastatud koguse lahutamiseks esimesena sisse, esimesena välja (FIFO) põhimõtet, sõltumata laomudelist, mida kaubad kasutavad.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="a5b2b-252">Kui käivitate sama aruande uuesti, kuid määrate seekord väljade **Koht** ja **Ladu** väärtuseks *Kuva*, sarnaneb uus aruanne järgmise näitega.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="a5b2b-253">Kaubakood</span><span class="sxs-lookup"><span data-stu-id="a5b2b-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-254">Koht</span><span class="sxs-lookup"><span data-stu-id="a5b2b-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-255">Ladu</span><span class="sxs-lookup"><span data-stu-id="a5b2b-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-256">Laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-257">Laoseisu väärtus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-258">Laoväärtuse kogus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-259">Laoväärtus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-260">Keskmine ühikukulu</span><span class="sxs-lookup"><span data-stu-id="a5b2b-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="a5b2b-261">01.05.2020–08.05.2020</span><span class="sxs-lookup"><span data-stu-id="a5b2b-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a5b2b-262">01.04.2020–30.04.2020</span><span class="sxs-lookup"><span data-stu-id="a5b2b-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a5b2b-263">01.03.2020–31.03.2020</span><span class="sxs-lookup"><span data-stu-id="a5b2b-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="a5b2b-264">P1: kogus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="a5b2b-265">P1: summa</span><span class="sxs-lookup"><span data-stu-id="a5b2b-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="a5b2b-266">P2: kogus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="a5b2b-267">P2: summa</span><span class="sxs-lookup"><span data-stu-id="a5b2b-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="a5b2b-268">P3: kogus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="a5b2b-269">P3: summa</span><span class="sxs-lookup"><span data-stu-id="a5b2b-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="a5b2b-270">1000</span><span class="sxs-lookup"><span data-stu-id="a5b2b-270">1000</span></span></td>
    <td><span data-ttu-id="a5b2b-271">1</span><span class="sxs-lookup"><span data-stu-id="a5b2b-271">1</span></span></td>
    <td><span data-ttu-id="a5b2b-272">11</span><span class="sxs-lookup"><span data-stu-id="a5b2b-272">11</span></span></td>
    <td><span data-ttu-id="a5b2b-273">10</span><span class="sxs-lookup"><span data-stu-id="a5b2b-273">10</span></span></td>
    <td><span data-ttu-id="a5b2b-274">916,67</span><span class="sxs-lookup"><span data-stu-id="a5b2b-274">916.67</span></span></td>
    <td><span data-ttu-id="a5b2b-275">14</span><span class="sxs-lookup"><span data-stu-id="a5b2b-275">14</span></span></td>
    <td><span data-ttu-id="a5b2b-276">1283,33</span><span class="sxs-lookup"><span data-stu-id="a5b2b-276">1,283.33</span></span></td>
    <td><span data-ttu-id="a5b2b-277">91,67</span><span class="sxs-lookup"><span data-stu-id="a5b2b-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a5b2b-278">5,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-278">5.00</span></span></td>
    <td><span data-ttu-id="a5b2b-279">458,33</span><span class="sxs-lookup"><span data-stu-id="a5b2b-279">458.33</span></span></td>
    <td><span data-ttu-id="a5b2b-280">5,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-280">5.00</span></span></td>
    <td><span data-ttu-id="a5b2b-281">458,33</span><span class="sxs-lookup"><span data-stu-id="a5b2b-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="a5b2b-282">1000</span><span class="sxs-lookup"><span data-stu-id="a5b2b-282">1000</span></span></td>
    <td><span data-ttu-id="a5b2b-283">1</span><span class="sxs-lookup"><span data-stu-id="a5b2b-283">1</span></span></td>
    <td><span data-ttu-id="a5b2b-284">12</span><span class="sxs-lookup"><span data-stu-id="a5b2b-284">12</span></span></td>
    <td><span data-ttu-id="a5b2b-285">4</span><span class="sxs-lookup"><span data-stu-id="a5b2b-285">4</span></span></td>
    <td><span data-ttu-id="a5b2b-286">366,67</span><span class="sxs-lookup"><span data-stu-id="a5b2b-286">366.67</span></span></td>
    <td><span data-ttu-id="a5b2b-287">14</span><span class="sxs-lookup"><span data-stu-id="a5b2b-287">14</span></span></td>
    <td><span data-ttu-id="a5b2b-288">1283,33</span><span class="sxs-lookup"><span data-stu-id="a5b2b-288">1,283.33</span></span></td>
    <td><span data-ttu-id="a5b2b-289">91,67</span><span class="sxs-lookup"><span data-stu-id="a5b2b-289">91.67</span></span></td>
    <td><span data-ttu-id="a5b2b-290">4,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-290">4.00</span></span></td>
    <td><span data-ttu-id="a5b2b-291">366,67</span><span class="sxs-lookup"><span data-stu-id="a5b2b-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="a5b2b-292">1000</span><span class="sxs-lookup"><span data-stu-id="a5b2b-292">1000</span></span></td>
    <td><span data-ttu-id="a5b2b-293">2</span><span class="sxs-lookup"><span data-stu-id="a5b2b-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="a5b2b-294">10</span><span class="sxs-lookup"><span data-stu-id="a5b2b-294">10</span></span></td>
    <td><span data-ttu-id="a5b2b-295">2000,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-295">2,000.00</span></span></td>
    <td><span data-ttu-id="a5b2b-296">10</span><span class="sxs-lookup"><span data-stu-id="a5b2b-296">10</span></span></td>
    <td><span data-ttu-id="a5b2b-297">2000,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-297">2,000.00</span></span></td>
    <td><span data-ttu-id="a5b2b-298">200,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a5b2b-299">10,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-299">10.00</span></span></td>
    <td><span data-ttu-id="a5b2b-300">2000,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="a5b2b-301"><strong>1000 kokku</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a5b2b-302"><strong>24,00</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="a5b2b-303"><strong>3283,33</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a5b2b-304"><strong>4,00</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="a5b2b-305"><strong>366,67</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="a5b2b-306"><strong>5,00</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="a5b2b-307"><strong>458,33</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="a5b2b-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="a5b2b-309"><strong>2458,33</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="a5b2b-310">Seekord on koht 1 jagatud kaheks reaks: üks lao 11 ja üks lao 12 jaoks.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="a5b2b-311">Kuid väärtused **Laoväärtuse kogus**, **Laoväärtus** ja **Keskmine ühikukulu** on samad, kuna **Ladu** pole finantsiline varude dimensioon.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="a5b2b-312">Lisaks pange tähele, et koha 1 koguse jaotus on erinev.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="a5b2b-313">Esimeses käivitatud aruandes eiras süsteem samas kohas toimunud üleviimistellimust ja lahutas müügiarve koguse koha 1 perioodist **01.03.2020–31.03.2020**.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="a5b2b-314">Kuid uues aruandes lahutab süsteem müügiarve koguse lao 12 perioodist **01.05.2020–08.05.2020**.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="a5b2b-315">Lao sulgemise mõju</span><span class="sxs-lookup"><span data-stu-id="a5b2b-315">Effects of inventory closing</span></span>

<span data-ttu-id="a5b2b-316">Kui käivitate lao sulgemise maikuu jaoks ja käivitate seejärel eelmise aruande uuesti, kuid seadistate välja **Kuupäevaga** väärtuseks *31. mai 2020*, peaksite märkama järgmisi tulemusi.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="a5b2b-317">Väärtused **Laoväärtus** ja **Keskmine ühikukulu** on uuendatud.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="a5b2b-318">Iga perioodi puhul on väärtused **Laoseisu väärtus** ja **Summa** samuti vastavalt uuendatud.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="a5b2b-319">Uus aruanne sarnaneb järgmise näitega.</span><span class="sxs-lookup"><span data-stu-id="a5b2b-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="a5b2b-320">Kaubakood</span><span class="sxs-lookup"><span data-stu-id="a5b2b-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-321">Koht</span><span class="sxs-lookup"><span data-stu-id="a5b2b-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-322">Ladu</span><span class="sxs-lookup"><span data-stu-id="a5b2b-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-323">Laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-324">Laoseisu väärtus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-325">Laoväärtuse kogus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-326">Laoväärtus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a5b2b-327">Keskmine ühikukulu</span><span class="sxs-lookup"><span data-stu-id="a5b2b-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="a5b2b-328">01.05.2020–31.05.2020</span><span class="sxs-lookup"><span data-stu-id="a5b2b-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a5b2b-329">01.04.2020–30.04.2020</span><span class="sxs-lookup"><span data-stu-id="a5b2b-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a5b2b-330">01.03.2020–31.03.2020</span><span class="sxs-lookup"><span data-stu-id="a5b2b-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="a5b2b-331">P1: kogus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="a5b2b-332">P1: summa</span><span class="sxs-lookup"><span data-stu-id="a5b2b-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="a5b2b-333">P2: kogus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="a5b2b-334">P2: summa</span><span class="sxs-lookup"><span data-stu-id="a5b2b-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="a5b2b-335">P3: kogus</span><span class="sxs-lookup"><span data-stu-id="a5b2b-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="a5b2b-336">P3: summa</span><span class="sxs-lookup"><span data-stu-id="a5b2b-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="a5b2b-337">1000</span><span class="sxs-lookup"><span data-stu-id="a5b2b-337">1000</span></span></td>
    <td><span data-ttu-id="a5b2b-338">1</span><span class="sxs-lookup"><span data-stu-id="a5b2b-338">1</span></span></td>
    <td><span data-ttu-id="a5b2b-339">11</span><span class="sxs-lookup"><span data-stu-id="a5b2b-339">11</span></span></td>
    <td><span data-ttu-id="a5b2b-340">10</span><span class="sxs-lookup"><span data-stu-id="a5b2b-340">10</span></span></td>
    <td><span data-ttu-id="a5b2b-341">910,70</span><span class="sxs-lookup"><span data-stu-id="a5b2b-341">910.70</span></span></td>
    <td><span data-ttu-id="a5b2b-342">14</span><span class="sxs-lookup"><span data-stu-id="a5b2b-342">14</span></span></td>
    <td><span data-ttu-id="a5b2b-343">1275,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-343">1,275.00</span></span></td>
    <td><span data-ttu-id="a5b2b-344">91,07</span><span class="sxs-lookup"><span data-stu-id="a5b2b-344">91.07</span></span></td>
    <td><span data-ttu-id="a5b2b-345">0,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="a5b2b-346">5,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-346">5.00</span></span></td>
    <td><span data-ttu-id="a5b2b-347">455,36</span><span class="sxs-lookup"><span data-stu-id="a5b2b-347">455.36</span></span></td>
    <td><span data-ttu-id="a5b2b-348">5,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-348">5.00</span></span></td>
    <td><span data-ttu-id="a5b2b-349">455,36</span><span class="sxs-lookup"><span data-stu-id="a5b2b-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="a5b2b-350">1000</span><span class="sxs-lookup"><span data-stu-id="a5b2b-350">1000</span></span></td>
    <td><span data-ttu-id="a5b2b-351">1</span><span class="sxs-lookup"><span data-stu-id="a5b2b-351">1</span></span></td>
    <td><span data-ttu-id="a5b2b-352">12</span><span class="sxs-lookup"><span data-stu-id="a5b2b-352">12</span></span></td>
    <td><span data-ttu-id="a5b2b-353">4</span><span class="sxs-lookup"><span data-stu-id="a5b2b-353">4</span></span></td>
    <td><span data-ttu-id="a5b2b-354">364,29</span><span class="sxs-lookup"><span data-stu-id="a5b2b-354">364.29</span></span></td>
    <td><span data-ttu-id="a5b2b-355">14</span><span class="sxs-lookup"><span data-stu-id="a5b2b-355">14</span></span></td>
    <td><span data-ttu-id="a5b2b-356">1275,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-356">1,275.00</span></span></td>
    <td><span data-ttu-id="a5b2b-357">91,07</span><span class="sxs-lookup"><span data-stu-id="a5b2b-357">91.07</span></span></td>
    <td><span data-ttu-id="a5b2b-358">4,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-358">4.00</span></span></td>
    <td><span data-ttu-id="a5b2b-359">364,29</span><span class="sxs-lookup"><span data-stu-id="a5b2b-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="a5b2b-360">1000</span><span class="sxs-lookup"><span data-stu-id="a5b2b-360">1000</span></span></td>
    <td><span data-ttu-id="a5b2b-361">2</span><span class="sxs-lookup"><span data-stu-id="a5b2b-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="a5b2b-362">10</span><span class="sxs-lookup"><span data-stu-id="a5b2b-362">10</span></span></td>
    <td><span data-ttu-id="a5b2b-363">2000,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-363">2,000.00</span></span></td>
    <td><span data-ttu-id="a5b2b-364">10</span><span class="sxs-lookup"><span data-stu-id="a5b2b-364">10</span></span></td>
    <td><span data-ttu-id="a5b2b-365">2000,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-365">2,000.00</span></span></td>
    <td><span data-ttu-id="a5b2b-366">200,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a5b2b-367">10,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-367">10.00</span></span></td>
    <td><span data-ttu-id="a5b2b-368">2000,00</span><span class="sxs-lookup"><span data-stu-id="a5b2b-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="a5b2b-369"><strong>1000 kokku</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a5b2b-370"><strong>24,00</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="a5b2b-371"><strong>3275,00</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a5b2b-372"><strong>4,00</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="a5b2b-373"><strong>364,29</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="a5b2b-374"><strong>5,00</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="a5b2b-375"><strong>455,36</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="a5b2b-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="a5b2b-377"><strong>2455,36</strong></span><span class="sxs-lookup"><span data-stu-id="a5b2b-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
