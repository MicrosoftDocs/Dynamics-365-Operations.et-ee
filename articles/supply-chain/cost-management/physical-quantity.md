---
title: Varuobjekti väärtused
description: Selles artiklis antakse teavet lao objekti väärtuste arvutamise kohta.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: daa36dad4009cc25b89363dcff6b4496205522e3
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981483"
---
# <a name="inventory-object-values"></a><span data-ttu-id="f0c3f-103">Varuobjekti väärtused</span><span class="sxs-lookup"><span data-stu-id="f0c3f-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0c3f-104">Selles artiklis antakse teavet lao objekti väärtuste arvutamise kohta.</span><span class="sxs-lookup"><span data-stu-id="f0c3f-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="f0c3f-105">Uus funktsioon nimega **füüsiline kogus** võimaldab näha konkreetse varuobjekti väärtusi.</span><span class="sxs-lookup"><span data-stu-id="f0c3f-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="f0c3f-106">Kuluobjekt tähistab üksuse taset, kus laoarvestus toimub.</span><span class="sxs-lookup"><span data-stu-id="f0c3f-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="f0c3f-107">Lisateavet kuluobjektide kohta leiate jaotisest [Kuluobjektid](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="f0c3f-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="f0c3f-108">Konkreetse varuobjekti väärtuste vaatamiseks klõpsake lehel **Kuluobjekt** valikut **Füüsiline kogus**.</span><span class="sxs-lookup"><span data-stu-id="f0c3f-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="f0c3f-109">Varude objekti väärtus arvutatakse järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="f0c3f-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="f0c3f-110">Varude objekt.Väärtus = Kuluobjekt.Keskmine ühikukulu × Varude objekt.Kogus</span><span class="sxs-lookup"><span data-stu-id="f0c3f-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="f0c3f-111">Järgmises näites kirjeldatakse varude objekti ja kuluobjekti väärtuste arvutamist.</span><span class="sxs-lookup"><span data-stu-id="f0c3f-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="f0c3f-112">Kaubale A registreeritakse kaks toote sissetuleku sündmust:</span><span class="sxs-lookup"><span data-stu-id="f0c3f-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="f0c3f-113">Toote sissetulek 1: kogus = 100 tk, summa = 1000.00 $, koht = 1, ladu = 11, partii nr</span><span class="sxs-lookup"><span data-stu-id="f0c3f-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="f0c3f-114">= B1</span><span class="sxs-lookup"><span data-stu-id="f0c3f-114">= B1</span></span>
-   <span data-ttu-id="f0c3f-115">Toote sissetulek 2: kogus = 50 tk, summa = 800.00 $, koht = 1, ladu = 11, partii nr</span><span class="sxs-lookup"><span data-stu-id="f0c3f-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="f0c3f-116">= B2</span><span class="sxs-lookup"><span data-stu-id="f0c3f-116">= B2</span></span>

<span data-ttu-id="f0c3f-117">Järgmises tabelis on kuluobjekti arvutuse tulemus.</span><span class="sxs-lookup"><span data-stu-id="f0c3f-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="f0c3f-118">Tulemust saab vaadata lehel **Kuluobjekt**.</span><span class="sxs-lookup"><span data-stu-id="f0c3f-118">You can view the result on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f0c3f-119">Objekti tüüp</span><span class="sxs-lookup"><span data-stu-id="f0c3f-119">Object type</span></span></th>
<th><span data-ttu-id="f0c3f-120">Kaubakood</span><span class="sxs-lookup"><span data-stu-id="f0c3f-120">Item number</span></span></th>
<th><span data-ttu-id="f0c3f-121">Laoala</span><span class="sxs-lookup"><span data-stu-id="f0c3f-121">Site</span></span></th>
<th><span data-ttu-id="f0c3f-122">Kogus</span><span class="sxs-lookup"><span data-stu-id="f0c3f-122">Quantity</span></span></th>
<th><span data-ttu-id="f0c3f-123">Laoühik</span><span class="sxs-lookup"><span data-stu-id="f0c3f-123">Inventory unit</span></span></th>
<th><span data-ttu-id="f0c3f-124">Väärtus</span><span class="sxs-lookup"><span data-stu-id="f0c3f-124">Value</span></span></th>
<th><span data-ttu-id="f0c3f-125">Keskmine ühikukulu</span><span class="sxs-lookup"><span data-stu-id="f0c3f-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f0c3f-126">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="f0c3f-126">Cost object</span></span></td>
<td><span data-ttu-id="f0c3f-127">A</span><span class="sxs-lookup"><span data-stu-id="f0c3f-127">A</span></span></td>
<td><span data-ttu-id="f0c3f-128">1</span><span class="sxs-lookup"><span data-stu-id="f0c3f-128">1</span></span></td>
<td><span data-ttu-id="f0c3f-129">150</span><span class="sxs-lookup"><span data-stu-id="f0c3f-129">150</span></span></td>
<td><span data-ttu-id="f0c3f-130">Kogus</span><span class="sxs-lookup"><span data-stu-id="f0c3f-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="f0c3f-131">$1800.00</span><span class="sxs-lookup"><span data-stu-id="f0c3f-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="f0c3f-132">$12.00</span><span class="sxs-lookup"><span data-stu-id="f0c3f-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f0c3f-133">Järgmises tabelis on varuobjekti arvutuse tulemus.</span><span class="sxs-lookup"><span data-stu-id="f0c3f-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="f0c3f-134">Tulemust saab vaadata, klõpsates nuppu **Füüsiline kogus** lehel **Kuluobjekt**.</span><span class="sxs-lookup"><span data-stu-id="f0c3f-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f0c3f-135">Objekti tüüp</span><span class="sxs-lookup"><span data-stu-id="f0c3f-135">Object type</span></span></th>
<th><span data-ttu-id="f0c3f-136">Kaubakood</span><span class="sxs-lookup"><span data-stu-id="f0c3f-136">Item number</span></span></th>
<th><span data-ttu-id="f0c3f-137">Laoala</span><span class="sxs-lookup"><span data-stu-id="f0c3f-137">Site</span></span></th>
<th><span data-ttu-id="f0c3f-138">Ladu</span><span class="sxs-lookup"><span data-stu-id="f0c3f-138">Warehouse</span></span></th>
<th><span data-ttu-id="f0c3f-139">Partii nr</span><span class="sxs-lookup"><span data-stu-id="f0c3f-139">Batch No.</span></span></th>
<th><span data-ttu-id="f0c3f-140">Kogus</span><span class="sxs-lookup"><span data-stu-id="f0c3f-140">Quantity</span></span></th>
<th><span data-ttu-id="f0c3f-141">Laoühik</span><span class="sxs-lookup"><span data-stu-id="f0c3f-141">Inventory unit</span></span></th>
<th><span data-ttu-id="f0c3f-142">Väärtus</span><span class="sxs-lookup"><span data-stu-id="f0c3f-142">Value</span></span></th>
<th><span data-ttu-id="f0c3f-143">Keskmine ühikukulu</span><span class="sxs-lookup"><span data-stu-id="f0c3f-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f0c3f-144">Varuobjekt</span><span class="sxs-lookup"><span data-stu-id="f0c3f-144">Inventory object</span></span></td>
<td><span data-ttu-id="f0c3f-145">A</span><span class="sxs-lookup"><span data-stu-id="f0c3f-145">A</span></span></td>
<td><span data-ttu-id="f0c3f-146">1</span><span class="sxs-lookup"><span data-stu-id="f0c3f-146">1</span></span></td>
<td><span data-ttu-id="f0c3f-147">11</span><span class="sxs-lookup"><span data-stu-id="f0c3f-147">11</span></span></td>
<td><span data-ttu-id="f0c3f-148">B1</span><span class="sxs-lookup"><span data-stu-id="f0c3f-148">B1</span></span></td>
<td><span data-ttu-id="f0c3f-149">100</span><span class="sxs-lookup"><span data-stu-id="f0c3f-149">100</span></span></td>
<td><span data-ttu-id="f0c3f-150">Kogus</span><span class="sxs-lookup"><span data-stu-id="f0c3f-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="f0c3f-151">$1200.00</span><span class="sxs-lookup"><span data-stu-id="f0c3f-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="f0c3f-152">$12.00</span><span class="sxs-lookup"><span data-stu-id="f0c3f-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f0c3f-153">Varuobjekt</span><span class="sxs-lookup"><span data-stu-id="f0c3f-153">Inventory object</span></span></td>
<td><span data-ttu-id="f0c3f-154">A</span><span class="sxs-lookup"><span data-stu-id="f0c3f-154">A</span></span></td>
<td><span data-ttu-id="f0c3f-155">1</span><span class="sxs-lookup"><span data-stu-id="f0c3f-155">1</span></span></td>
<td><span data-ttu-id="f0c3f-156">11</span><span class="sxs-lookup"><span data-stu-id="f0c3f-156">11</span></span></td>
<td><span data-ttu-id="f0c3f-157">B2</span><span class="sxs-lookup"><span data-stu-id="f0c3f-157">B2</span></span></td>
<td><span data-ttu-id="f0c3f-158">50</span><span class="sxs-lookup"><span data-stu-id="f0c3f-158">50</span></span></td>
<td><span data-ttu-id="f0c3f-159">Kogus</span><span class="sxs-lookup"><span data-stu-id="f0c3f-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="f0c3f-160">$600.00</span><span class="sxs-lookup"><span data-stu-id="f0c3f-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="f0c3f-161">$12.00</span><span class="sxs-lookup"><span data-stu-id="f0c3f-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="f0c3f-162">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f0c3f-162">Additional resources</span></span>
--------

[<span data-ttu-id="f0c3f-163">Kuluobjektid</span><span class="sxs-lookup"><span data-stu-id="f0c3f-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="f0c3f-164">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="f0c3f-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="f0c3f-165">Mis on uus ja muudetud</span><span class="sxs-lookup"><span data-stu-id="f0c3f-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)



