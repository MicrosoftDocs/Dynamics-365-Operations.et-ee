---
title: Varuobjekti väärtused
description: Selles artiklis antakse teavet lao objekti väärtuste arvutamise kohta.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a55b1068835f1e050110c57e6af3340a018ff31
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187766"
---
# <a name="inventory-object-values"></a><span data-ttu-id="d8de9-103">Varuobjekti väärtused</span><span class="sxs-lookup"><span data-stu-id="d8de9-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8de9-104">Selles artiklis antakse teavet lao objekti väärtuste arvutamise kohta.</span><span class="sxs-lookup"><span data-stu-id="d8de9-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="d8de9-105">Uus funktsioon nimega **füüsiline kogus** võimaldab näha konkreetse varuobjekti väärtusi.</span><span class="sxs-lookup"><span data-stu-id="d8de9-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="d8de9-106">Kuluobjekt tähistab üksuse taset, kus laoarvestus toimub.</span><span class="sxs-lookup"><span data-stu-id="d8de9-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="d8de9-107">Lisateavet kuluobjektide kohta leiate jaotisest [Kuluobjektid](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="d8de9-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="d8de9-108">Konkreetse varuobjekti väärtuste vaatamiseks klõpsake lehel **Kuluobjekt** valikut **Füüsiline kogus**.</span><span class="sxs-lookup"><span data-stu-id="d8de9-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="d8de9-109">Varude objekti väärtus arvutatakse järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d8de9-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="d8de9-110">Varude objekt.Väärtus = Kuluobjekt.Keskmine ühikukulu × Varude objekt.Kogus</span><span class="sxs-lookup"><span data-stu-id="d8de9-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="d8de9-111">Järgmises näites kirjeldatakse varude objekti ja kuluobjekti väärtuste arvutamist.</span><span class="sxs-lookup"><span data-stu-id="d8de9-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="d8de9-112">Kaubale A registreeritakse kaks toote sissetuleku sündmust:</span><span class="sxs-lookup"><span data-stu-id="d8de9-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="d8de9-113">Toote sissetulek 1: kogus = 100 tk, summa = 1000.00 $, koht = 1, ladu = 11, partii nr</span><span class="sxs-lookup"><span data-stu-id="d8de9-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="d8de9-114">= B1</span><span class="sxs-lookup"><span data-stu-id="d8de9-114">= B1</span></span>
-   <span data-ttu-id="d8de9-115">Toote sissetulek 2: kogus = 50 tk, summa = 800.00 $, koht = 1, ladu = 11, partii nr</span><span class="sxs-lookup"><span data-stu-id="d8de9-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="d8de9-116">= B2</span><span class="sxs-lookup"><span data-stu-id="d8de9-116">= B2</span></span>

<span data-ttu-id="d8de9-117">Järgmises tabelis on kuluobjekti arvutuse tulemus.</span><span class="sxs-lookup"><span data-stu-id="d8de9-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="d8de9-118">Tulemust saab vaadata lehel **Kuluobjekt**.</span><span class="sxs-lookup"><span data-stu-id="d8de9-118">You can view the result on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="d8de9-119">Objekti tüüp</span><span class="sxs-lookup"><span data-stu-id="d8de9-119">Object type</span></span></th>
<th><span data-ttu-id="d8de9-120">Kaubakood</span><span class="sxs-lookup"><span data-stu-id="d8de9-120">Item number</span></span></th>
<th><span data-ttu-id="d8de9-121">Laoala</span><span class="sxs-lookup"><span data-stu-id="d8de9-121">Site</span></span></th>
<th><span data-ttu-id="d8de9-122">Kogus</span><span class="sxs-lookup"><span data-stu-id="d8de9-122">Quantity</span></span></th>
<th><span data-ttu-id="d8de9-123">Laoühik</span><span class="sxs-lookup"><span data-stu-id="d8de9-123">Inventory unit</span></span></th>
<th><span data-ttu-id="d8de9-124">Väärtus</span><span class="sxs-lookup"><span data-stu-id="d8de9-124">Value</span></span></th>
<th><span data-ttu-id="d8de9-125">Keskmine ühikukulu</span><span class="sxs-lookup"><span data-stu-id="d8de9-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d8de9-126">Kuluobjekt</span><span class="sxs-lookup"><span data-stu-id="d8de9-126">Cost object</span></span></td>
<td><span data-ttu-id="d8de9-127">A</span><span class="sxs-lookup"><span data-stu-id="d8de9-127">A</span></span></td>
<td><span data-ttu-id="d8de9-128">1</span><span class="sxs-lookup"><span data-stu-id="d8de9-128">1</span></span></td>
<td><span data-ttu-id="d8de9-129">150</span><span class="sxs-lookup"><span data-stu-id="d8de9-129">150</span></span></td>
<td><span data-ttu-id="d8de9-130">Kogus</span><span class="sxs-lookup"><span data-stu-id="d8de9-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="d8de9-131">$1800.00</span><span class="sxs-lookup"><span data-stu-id="d8de9-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="d8de9-132">$12.00</span><span class="sxs-lookup"><span data-stu-id="d8de9-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d8de9-133">Järgmises tabelis on varuobjekti arvutuse tulemus.</span><span class="sxs-lookup"><span data-stu-id="d8de9-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="d8de9-134">Tulemust saab vaadata, klõpsates nuppu **Füüsiline kogus** lehel **Kuluobjekt**.</span><span class="sxs-lookup"><span data-stu-id="d8de9-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="d8de9-135">Objekti tüüp</span><span class="sxs-lookup"><span data-stu-id="d8de9-135">Object type</span></span></th>
<th><span data-ttu-id="d8de9-136">Kaubakood</span><span class="sxs-lookup"><span data-stu-id="d8de9-136">Item number</span></span></th>
<th><span data-ttu-id="d8de9-137">Laoala</span><span class="sxs-lookup"><span data-stu-id="d8de9-137">Site</span></span></th>
<th><span data-ttu-id="d8de9-138">Ladu</span><span class="sxs-lookup"><span data-stu-id="d8de9-138">Warehouse</span></span></th>
<th><span data-ttu-id="d8de9-139">Partii nr</span><span class="sxs-lookup"><span data-stu-id="d8de9-139">Batch No.</span></span></th>
<th><span data-ttu-id="d8de9-140">Kogus</span><span class="sxs-lookup"><span data-stu-id="d8de9-140">Quantity</span></span></th>
<th><span data-ttu-id="d8de9-141">Laoühik</span><span class="sxs-lookup"><span data-stu-id="d8de9-141">Inventory unit</span></span></th>
<th><span data-ttu-id="d8de9-142">Väärtus</span><span class="sxs-lookup"><span data-stu-id="d8de9-142">Value</span></span></th>
<th><span data-ttu-id="d8de9-143">Keskmine ühikukulu</span><span class="sxs-lookup"><span data-stu-id="d8de9-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d8de9-144">Varuobjekt</span><span class="sxs-lookup"><span data-stu-id="d8de9-144">Inventory object</span></span></td>
<td><span data-ttu-id="d8de9-145">A</span><span class="sxs-lookup"><span data-stu-id="d8de9-145">A</span></span></td>
<td><span data-ttu-id="d8de9-146">1</span><span class="sxs-lookup"><span data-stu-id="d8de9-146">1</span></span></td>
<td><span data-ttu-id="d8de9-147">11</span><span class="sxs-lookup"><span data-stu-id="d8de9-147">11</span></span></td>
<td><span data-ttu-id="d8de9-148">B1</span><span class="sxs-lookup"><span data-stu-id="d8de9-148">B1</span></span></td>
<td><span data-ttu-id="d8de9-149">100</span><span class="sxs-lookup"><span data-stu-id="d8de9-149">100</span></span></td>
<td><span data-ttu-id="d8de9-150">Kogus</span><span class="sxs-lookup"><span data-stu-id="d8de9-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="d8de9-151">$1200.00</span><span class="sxs-lookup"><span data-stu-id="d8de9-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="d8de9-152">$12.00</span><span class="sxs-lookup"><span data-stu-id="d8de9-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d8de9-153">Varuobjekt</span><span class="sxs-lookup"><span data-stu-id="d8de9-153">Inventory object</span></span></td>
<td><span data-ttu-id="d8de9-154">A</span><span class="sxs-lookup"><span data-stu-id="d8de9-154">A</span></span></td>
<td><span data-ttu-id="d8de9-155">1</span><span class="sxs-lookup"><span data-stu-id="d8de9-155">1</span></span></td>
<td><span data-ttu-id="d8de9-156">11</span><span class="sxs-lookup"><span data-stu-id="d8de9-156">11</span></span></td>
<td><span data-ttu-id="d8de9-157">B2</span><span class="sxs-lookup"><span data-stu-id="d8de9-157">B2</span></span></td>
<td><span data-ttu-id="d8de9-158">50</span><span class="sxs-lookup"><span data-stu-id="d8de9-158">50</span></span></td>
<td><span data-ttu-id="d8de9-159">Kogus</span><span class="sxs-lookup"><span data-stu-id="d8de9-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="d8de9-160">$600.00</span><span class="sxs-lookup"><span data-stu-id="d8de9-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="d8de9-161">$12.00</span><span class="sxs-lookup"><span data-stu-id="d8de9-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="additional-resources"></a><span data-ttu-id="d8de9-162">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d8de9-162">Additional resources</span></span>

[<span data-ttu-id="d8de9-163">Kuluobjektid</span><span class="sxs-lookup"><span data-stu-id="d8de9-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="d8de9-164">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="d8de9-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="d8de9-165">Mis on uus ja muudetud</span><span class="sxs-lookup"><span data-stu-id="d8de9-165">What's new and changed</span></span>](../../fin-ops-core/fin-ops/get-started/whats-new-changed.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]