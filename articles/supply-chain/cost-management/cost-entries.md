---
title: Kulukirjed
description: "Sellese artiklis antakse teavet kulukirjete ja nende loomise aja kohta. Kulukirje on kirje, mis registreerib antud sündmuse koguse ja kulu."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a61761a5c9d98befd67682e1790af5377b7a55e1
ms.openlocfilehash: 38fedcb2f482296b1c88dda98d34dd8b7debf555
ms.contentlocale: et-ee
ms.lasthandoff: 10/13/2017

---

# <a name="cost-entries"></a><span data-ttu-id="509fd-104">Kulukirjed</span><span class="sxs-lookup"><span data-stu-id="509fd-104">Cost entries</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="509fd-105">Sellese artiklis antakse teavet kulukirjete ja nende loomise aja kohta.</span><span class="sxs-lookup"><span data-stu-id="509fd-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="509fd-106">Kulukirje on kirje, mis registreerib antud sündmuse koguse ja kulu.</span><span class="sxs-lookup"><span data-stu-id="509fd-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="509fd-107">Kulukanded on laokannete koondsummad, mis salvestatakse aktiivsetel finantsvarude dimensioonidel.</span><span class="sxs-lookup"><span data-stu-id="509fd-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="509fd-108">Näited</span><span class="sxs-lookup"><span data-stu-id="509fd-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="509fd-109">Näide 1: kulukirjeid pole loodud</span><span class="sxs-lookup"><span data-stu-id="509fd-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="509fd-110">Registreeritakse üleviimistöölehe sündmus.</span><span class="sxs-lookup"><span data-stu-id="509fd-110">A transfer journal event is registered.</span></span> <span data-ttu-id="509fd-111">Sündmus edastab ühe kauba A ühiku asukohast A asukohta B. Asukoha varude dimensiooni ei arvestata kuluobjekti osaks.</span><span class="sxs-lookup"><span data-stu-id="509fd-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="509fd-112">Seetõttu loob sündmus kaks laokannet ja mitte ühtegi kulukirjet.</span><span class="sxs-lookup"><span data-stu-id="509fd-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="509fd-113">Näide 2: luuakse kulukirjed</span><span class="sxs-lookup"><span data-stu-id="509fd-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="509fd-114">Registreeritakse üleviimistöölehe sündmus.</span><span class="sxs-lookup"><span data-stu-id="509fd-114">A transfer journal event is registered.</span></span> <span data-ttu-id="509fd-115">Sündmus edastab ühe kauba A ühiku laoalalt 1 laoalale 2.</span><span class="sxs-lookup"><span data-stu-id="509fd-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="509fd-116">Laoala varude dimensioon arvestatakse kuluobjekti osaks.</span><span class="sxs-lookup"><span data-stu-id="509fd-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="509fd-117">Seetõttu loob sündmus kaks laokannet ja kaks kulukirjet.</span><span class="sxs-lookup"><span data-stu-id="509fd-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="509fd-118">Näide 3: luuakse üks kulukirje</span><span class="sxs-lookup"><span data-stu-id="509fd-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="509fd-119">Ostutellimusele registreeritakse toote sissetuleku sündmus.</span><span class="sxs-lookup"><span data-stu-id="509fd-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="509fd-120">Sündmus registreerib 100 kauba A ühikut ühiku hinnaga 10.00 USA dollarit (USD).</span><span class="sxs-lookup"><span data-stu-id="509fd-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="509fd-121">Kuna kaup A kasutab varude halduse eesmärgi jälgimiseks seerianumbrit, luuakse igale vastu võetavale kaubale kordumatu seerianumber.</span><span class="sxs-lookup"><span data-stu-id="509fd-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="509fd-122">Seetõttu loob sündmus 100 laokannet ja ühe kulukirje.</span><span class="sxs-lookup"><span data-stu-id="509fd-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="509fd-123">Kulukirjete leht</span><span class="sxs-lookup"><span data-stu-id="509fd-123">Cost entries page</span></span>
<span data-ttu-id="509fd-124">Uus leht **Kulukirjed** võimaldab vaadata ja juhtida koguste ja kulude registreerimist.</span><span class="sxs-lookup"><span data-stu-id="509fd-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="509fd-125">See leht täiendab lehti **Laokanne** ja **Lao tasakaalustus**.</span><span class="sxs-lookup"><span data-stu-id="509fd-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="509fd-126">Sündmuse kirjed registreeritakse kronoloogilises järjekorras.</span><span class="sxs-lookup"><span data-stu-id="509fd-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="509fd-127">Seetõttu on võimalik konkreetse sündmuse või kõigi dokumendiga seotud sündmuste kogunenud kulusid kiiresti leida ja juhtida.</span><span class="sxs-lookup"><span data-stu-id="509fd-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="509fd-128">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="509fd-128">Here is an example:</span></span>

-   <span data-ttu-id="509fd-129">Kaubale A registreeritakse toote sissetuleku sündmus. Vastu võetakse sada ühikut ühiku hinnaga 10.00 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="509fd-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="509fd-130">Mõni päev pärast arvesündmuse registreerimist suureneb kulu 11.00 USA dollarini.</span><span class="sxs-lookup"><span data-stu-id="509fd-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="509fd-131">Seetõttu on kogusumma 1100 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="509fd-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="509fd-132">Luuakse teine kanne, mis kajastab 100 USA dollari suurust vahet.</span><span class="sxs-lookup"><span data-stu-id="509fd-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="509fd-133">Mõni päev hiljem registreeritakse ostutellimusel lisatasu 15.00 USA dollarit transpordikulu katteks.</span><span class="sxs-lookup"><span data-stu-id="509fd-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="509fd-134">Kanne</span><span class="sxs-lookup"><span data-stu-id="509fd-134">Voucher</span></span> | <span data-ttu-id="509fd-135">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="509fd-135">Date</span></span>       | <span data-ttu-id="509fd-136">Viide</span><span class="sxs-lookup"><span data-stu-id="509fd-136">Reference</span></span>      | <span data-ttu-id="509fd-137">Kood</span><span class="sxs-lookup"><span data-stu-id="509fd-137">Number</span></span> | <span data-ttu-id="509fd-138">Saatepartii ID</span><span class="sxs-lookup"><span data-stu-id="509fd-138">Lot ID</span></span>  | <span data-ttu-id="509fd-139">Kogus</span><span class="sxs-lookup"><span data-stu-id="509fd-139">Quantity</span></span> | <span data-ttu-id="509fd-140">Summa</span><span class="sxs-lookup"><span data-stu-id="509fd-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="509fd-141">00001</span><span class="sxs-lookup"><span data-stu-id="509fd-141">00001</span></span>   | <span data-ttu-id="509fd-142">01-01-2015</span><span class="sxs-lookup"><span data-stu-id="509fd-142">01-01-2015</span></span> | <span data-ttu-id="509fd-143">Ostutellimus</span><span class="sxs-lookup"><span data-stu-id="509fd-143">Purchase order</span></span> | <span data-ttu-id="509fd-144">100001</span><span class="sxs-lookup"><span data-stu-id="509fd-144">100001</span></span> | <span data-ttu-id="509fd-145">0000101</span><span class="sxs-lookup"><span data-stu-id="509fd-145">0000101</span></span> | <span data-ttu-id="509fd-146">100,00</span><span class="sxs-lookup"><span data-stu-id="509fd-146">100.00</span></span>   | <span data-ttu-id="509fd-147">1000.00</span><span class="sxs-lookup"><span data-stu-id="509fd-147">1000.00</span></span> |
| <span data-ttu-id="509fd-148">00002</span><span class="sxs-lookup"><span data-stu-id="509fd-148">00002</span></span>   | <span data-ttu-id="509fd-149">20-01-2015</span><span class="sxs-lookup"><span data-stu-id="509fd-149">20-01-2015</span></span> | <span data-ttu-id="509fd-150">Ostutellimus</span><span class="sxs-lookup"><span data-stu-id="509fd-150">Purchase order</span></span> | <span data-ttu-id="509fd-151">100001</span><span class="sxs-lookup"><span data-stu-id="509fd-151">100001</span></span> | <span data-ttu-id="509fd-152">0000101</span><span class="sxs-lookup"><span data-stu-id="509fd-152">0000101</span></span> |          | <span data-ttu-id="509fd-153">100,00</span><span class="sxs-lookup"><span data-stu-id="509fd-153">100.00</span></span>  |
| <span data-ttu-id="509fd-154">00003</span><span class="sxs-lookup"><span data-stu-id="509fd-154">00003</span></span>   | <span data-ttu-id="509fd-155">31-01-2015</span><span class="sxs-lookup"><span data-stu-id="509fd-155">31-01-2015</span></span> | <span data-ttu-id="509fd-156">Korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="509fd-156">Adjustment</span></span>     | <span data-ttu-id="509fd-157">100001</span><span class="sxs-lookup"><span data-stu-id="509fd-157">100001</span></span> | <span data-ttu-id="509fd-158">0000101</span><span class="sxs-lookup"><span data-stu-id="509fd-158">0000101</span></span> |          | <span data-ttu-id="509fd-159">15,00</span><span class="sxs-lookup"><span data-stu-id="509fd-159">15.00</span></span>   |

<span data-ttu-id="509fd-160">Lehel **Kulukirjed** saab filtreerida dokumendi ID ja dokumendi kuupäeva alusel.</span><span class="sxs-lookup"><span data-stu-id="509fd-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="509fd-161">Kulukeskused on saadaval ainult [kuluobjektide](cost-object.md) või väljastatud toodete puhul.</span><span class="sxs-lookup"><span data-stu-id="509fd-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="see-also"></a><span data-ttu-id="509fd-162">Vt ka</span><span class="sxs-lookup"><span data-stu-id="509fd-162">See also</span></span>
--------

[<span data-ttu-id="509fd-163">Kuluobjektid</span><span class="sxs-lookup"><span data-stu-id="509fd-163">Cost objects</span></span>](cost-object.md)




