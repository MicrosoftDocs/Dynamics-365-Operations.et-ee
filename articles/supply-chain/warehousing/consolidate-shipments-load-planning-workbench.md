---
title: Saadetiste konsolideerimine koorma planeerimise töölaua suvandi Lattu väljastamine abil
description: Selles teemas kirjeldatakse stsenaariumi, kus lattu vabastatakse mitu tellimust sama koormuses ja seejärel konsolideeritakse automaatselt saadetisteks.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 30824bf1c8e84bab08b6885ee812ed5e3e9937bb
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117177"
---
# <a name="consolidate-shipments-by-releasing-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="39d7e-103">Saadetiste konsolideerimine koorma planeerimise töölaua suvandi Lattu väljastamine abil</span><span class="sxs-lookup"><span data-stu-id="39d7e-103">Consolidate shipments by releasing to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39d7e-104">Selles teemas kirjeldatakse stsenaariumi, kus lattu vabastatakse mitu tellimust sama koormuses ja seejärel konsolideeritakse automaatselt saadetisteks.</span><span class="sxs-lookup"><span data-stu-id="39d7e-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="39d7e-105">Demoandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="39d7e-105">Make demo data available</span></span>

<span data-ttu-id="39d7e-106">Selle teema stsenaarium viitab väärtustele ja kirjetele, mis kuuluvad Microsoft Dynamics 365 Supply Chain Managementile esitatud standardsete demoandmete hulka.</span><span class="sxs-lookup"><span data-stu-id="39d7e-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="39d7e-107">Kui soovite kasutada siin esitatud väärtusi harjutuste tegemise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks **USMF**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="39d7e-108">Saadetise konsolideerimispoliitikate ja tootefiltrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="39d7e-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="39d7e-109">Siin kirjeldatud stsenaarium eeldab, et olete juba funktsiooni sisse lülitanud, sooritanud [saadetise konsolideerimispoliitikate konfigureerimise](configure-shipment-consolidation-policies.md) harjutused ning loonud poliitikad ja muud seal kirjeldatud kirjed.</span><span class="sxs-lookup"><span data-stu-id="39d7e-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="39d7e-110">Veenduge, et olete enne selle stsenaariumi jätkamist sooritanud need harjutused.</span><span class="sxs-lookup"><span data-stu-id="39d7e-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="39d7e-111">Müügitellimuste loomine selle stsenaariumi jaoks</span><span class="sxs-lookup"><span data-stu-id="39d7e-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="39d7e-112">Alustage müügitellimuste kogumi loomisega, millega saate töötada.</span><span class="sxs-lookup"><span data-stu-id="39d7e-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="39d7e-113">Peate töötama laoga, kus on lubatud täpsema laohalduse (WMS) protsessid.</span><span class="sxs-lookup"><span data-stu-id="39d7e-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="39d7e-114">Kui pole konkreetselt viidatud mõnele muule laole, tuleb kasutada sama ladu kõigi järgmiste tellimuste kogumite puhul.</span><span class="sxs-lookup"><span data-stu-id="39d7e-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="39d7e-115">Avage jaotis **Müügireskontro \> Tellimused \> Kõik müügitellimused** ja looge müügitellimuste kogum, millel on järgmistes alamjaotistes kirjeldatud sätted.</span><span class="sxs-lookup"><span data-stu-id="39d7e-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="39d7e-116">Tellimuse komplekti 1 loomine</span><span class="sxs-lookup"><span data-stu-id="39d7e-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="39d7e-117">Müügitellimus 1-1</span><span class="sxs-lookup"><span data-stu-id="39d7e-117">Sales order 1-1</span></span>

1. <span data-ttu-id="39d7e-118">Looge järgmiste sätetega müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="39d7e-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="39d7e-119">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="39d7e-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="39d7e-120">**Tarneviis:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="39d7e-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="39d7e-121">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="39d7e-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="39d7e-122">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="39d7e-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="39d7e-123">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="39d7e-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="39d7e-124">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="39d7e-125">Müügitellimus 1-2</span><span class="sxs-lookup"><span data-stu-id="39d7e-125">Sales order 1-2</span></span>

1. <span data-ttu-id="39d7e-126">Looge järgmiste sätetega müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="39d7e-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="39d7e-127">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="39d7e-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="39d7e-128">**Tarneviis:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="39d7e-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="39d7e-129">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="39d7e-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="39d7e-130">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="39d7e-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="39d7e-131">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="39d7e-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="39d7e-132">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="39d7e-133">Müügitellimus 1-3</span><span class="sxs-lookup"><span data-stu-id="39d7e-133">Sales order 1-3</span></span>

1. <span data-ttu-id="39d7e-134">Looge järgmiste sätetega müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="39d7e-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="39d7e-135">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="39d7e-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="39d7e-136">**Tarneviis:** *10*</span><span class="sxs-lookup"><span data-stu-id="39d7e-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="39d7e-137">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="39d7e-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="39d7e-138">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="39d7e-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="39d7e-139">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="39d7e-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="39d7e-140">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="39d7e-141">Lisage teine järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="39d7e-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="39d7e-142">**Kaubakood:** *A0002* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="39d7e-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="39d7e-143">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="39d7e-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="39d7e-144">**Tarneviis:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="39d7e-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="39d7e-145">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan teise tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="39d7e-146">Tellimuse komplekti 2 loomine</span><span class="sxs-lookup"><span data-stu-id="39d7e-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="39d7e-147">Müügitellimused 2-1 ja 2-2</span><span class="sxs-lookup"><span data-stu-id="39d7e-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="39d7e-148">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="39d7e-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="39d7e-149">**Kliendi konto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="39d7e-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="39d7e-150">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="39d7e-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="39d7e-151">**Kaubakood:** *M9200* (kaup, kus filtri **Kood 4** väärtuseks on seatud *Kergsüttiv*)</span><span class="sxs-lookup"><span data-stu-id="39d7e-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="39d7e-152">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="39d7e-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="39d7e-153">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="39d7e-154">Lisage teine järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="39d7e-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="39d7e-155">**Kaubakood:** *M9201* (kaup, kus filtri **Kood 4** väärtuseks on seatud *Lõhkeaine*)</span><span class="sxs-lookup"><span data-stu-id="39d7e-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="39d7e-156">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="39d7e-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="39d7e-157">**Tarneviis:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="39d7e-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="39d7e-158">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan teise tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="39d7e-159">Tellimuse komplekti 3 loomine</span><span class="sxs-lookup"><span data-stu-id="39d7e-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="39d7e-160">Müügitellimused 3-1 ja 3-2</span><span class="sxs-lookup"><span data-stu-id="39d7e-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="39d7e-161">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="39d7e-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="39d7e-162">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="39d7e-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="39d7e-163">**Kliendi ostutellimus:** *1*</span><span class="sxs-lookup"><span data-stu-id="39d7e-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="39d7e-164">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="39d7e-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="39d7e-165">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="39d7e-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="39d7e-166">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="39d7e-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="39d7e-167">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="39d7e-168">Müügitellimused 3-3 ja 3-4</span><span class="sxs-lookup"><span data-stu-id="39d7e-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="39d7e-169">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="39d7e-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="39d7e-170">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="39d7e-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="39d7e-171">**Kliendi ostutellimus:** *2*</span><span class="sxs-lookup"><span data-stu-id="39d7e-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="39d7e-172">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="39d7e-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="39d7e-173">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="39d7e-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="39d7e-174">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="39d7e-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="39d7e-175">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="39d7e-176">Tellimuse komplekti 4 loomine</span><span class="sxs-lookup"><span data-stu-id="39d7e-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="39d7e-177">Müügitellimused 4-1 ja 4-2</span><span class="sxs-lookup"><span data-stu-id="39d7e-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="39d7e-178">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="39d7e-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="39d7e-179">**Kliendi konto:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="39d7e-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="39d7e-180">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="39d7e-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="39d7e-181">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="39d7e-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="39d7e-182">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="39d7e-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="39d7e-183">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="39d7e-184">Müügitellimused 4-3 ja 4-4</span><span class="sxs-lookup"><span data-stu-id="39d7e-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="39d7e-185">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="39d7e-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="39d7e-186">**Kliendi konto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="39d7e-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="39d7e-187">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="39d7e-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="39d7e-188">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="39d7e-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="39d7e-189">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="39d7e-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="39d7e-190">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="39d7e-191">Müügitellimused 4-5 ja 4-6</span><span class="sxs-lookup"><span data-stu-id="39d7e-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="39d7e-192">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="39d7e-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="39d7e-193">**Kliendi konto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="39d7e-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="39d7e-194">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="39d7e-194">**Site:** *6*</span></span>
    - <span data-ttu-id="39d7e-195">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="39d7e-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="39d7e-196">**Kaust:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="39d7e-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="39d7e-197">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="39d7e-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="39d7e-198">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="39d7e-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="39d7e-199">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="39d7e-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="39d7e-200">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="39d7e-201">Müügitellimused 4-7 ja 4-8</span><span class="sxs-lookup"><span data-stu-id="39d7e-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="39d7e-202">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="39d7e-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="39d7e-203">**Kliendi konto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="39d7e-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="39d7e-204">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="39d7e-204">**Site:** *6*</span></span>
    - <span data-ttu-id="39d7e-205">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="39d7e-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="39d7e-206">**Kaust:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="39d7e-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="39d7e-207">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="39d7e-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="39d7e-208">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="39d7e-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="39d7e-209">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="39d7e-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="39d7e-210">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="39d7e-211">Koorma planeerimise töölaua kasutamine koormate loomiseks ja lattu vabastamiseks</span><span class="sxs-lookup"><span data-stu-id="39d7e-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="39d7e-212">Järgige neid samme koormuse loomiseks igale selle stsenaariumi jaoks loodud tellimuse komplektile ja seejärel vabastage see lattu.</span><span class="sxs-lookup"><span data-stu-id="39d7e-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="39d7e-213">Avage **Laohaldus \> Koormused \> Koormuse plaanimise töölaud**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="39d7e-214">Otsige üles ja valige vahekaardil **Müügiread** kõik müügitellimuse read ühest selle stsenaariumi jaoks loodud tellimuse komplektist.</span><span class="sxs-lookup"><span data-stu-id="39d7e-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="39d7e-215">Valige tegevusepaani vahekaardil **Pakkumine ja nõudlus** suvand **Lisa \> Uuele koormusele**, et lisada valitud tellimuseread uuele koormusele.</span><span class="sxs-lookup"><span data-stu-id="39d7e-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="39d7e-216">Valige dialoogiboksi **Koormuse malli määramine** väljal **Koormuse malli ID** koormuse mall, näiteks *Stnd koormuse mall*.</span><span class="sxs-lookup"><span data-stu-id="39d7e-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="39d7e-217">Valige dialoogiboksi sulgemiseks suvand **OK**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="39d7e-218">Otsige üles ja valige äsja loodud koormus jaotises **Koormused**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="39d7e-219">Valitud koormuse lattu väljastamiseks valige **Väljasta \> Lattu väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="39d7e-220">Korrake seda protseduuri selle stsenaariumi jaoks loodud ülejäänud kolme tellimuse komplekti puhul.</span><span class="sxs-lookup"><span data-stu-id="39d7e-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="39d7e-221">Saadetiste kontrollimine</span><span class="sxs-lookup"><span data-stu-id="39d7e-221">Verify the shipments</span></span>

<span data-ttu-id="39d7e-222">Järgmine protseduur võimaldab teil kontrollida saadetise konsolideerimise käigus loodud või värskendatud saadetisi.</span><span class="sxs-lookup"><span data-stu-id="39d7e-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="39d7e-223">Kasutage seda iga selle stsenaariumi jaoks loodud tellimuse komplekti läbivaatamiseks ja vaadake üle järgnevad alamjaotised veendumaks, et saavutasite oodatud tulemused.</span><span class="sxs-lookup"><span data-stu-id="39d7e-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="39d7e-224">Avage **Laohaldus \> Saadetised \> Kõik saadetised**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="39d7e-225">Otsige üles ja valige nõutav saadetis.</span><span class="sxs-lookup"><span data-stu-id="39d7e-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="39d7e-226">Kui saadetise loomise või värskendamise ajal kasutati konsolideerimispoliitikat, kasutage välja **Saadetise konsolideerimispoliitika**.</span><span class="sxs-lookup"><span data-stu-id="39d7e-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="39d7e-227">1. tellimuse komplekti väljastamine ühes koormuses</span><span class="sxs-lookup"><span data-stu-id="39d7e-227">Release order set 1 in one load</span></span>

<span data-ttu-id="39d7e-228">Kaks saadetist peaks olema loodud.</span><span class="sxs-lookup"><span data-stu-id="39d7e-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="39d7e-229">Esimene saadetis sisaldab kolme rida ja loodi saadetise konsolideerimispoliitika *CustomerMode* abil.</span><span class="sxs-lookup"><span data-stu-id="39d7e-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="39d7e-230">Teine saadetis, mis ei kasuta transportimisel tarneviisi *Lennutransport*, loodi saadetise konsolideerimispoliitika *CustomerOrderNo* abil.</span><span class="sxs-lookup"><span data-stu-id="39d7e-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="39d7e-231">2. tellimuse komplekti väljastamine ühes koormuses</span><span class="sxs-lookup"><span data-stu-id="39d7e-231">Release order set 2 in one load</span></span>

<span data-ttu-id="39d7e-232">Kolm saadetist peaks olema loodud.</span><span class="sxs-lookup"><span data-stu-id="39d7e-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="39d7e-233">Esimene saadetis sisaldab *kergsüttivaid* kaupu.</span><span class="sxs-lookup"><span data-stu-id="39d7e-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="39d7e-234">Ülejäänud kaks saadetist sisaldavad ühte rida, millel on kaup *Lõhkeaine*.</span><span class="sxs-lookup"><span data-stu-id="39d7e-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="39d7e-235">3. tellimuse komplekti väljastamine ühes koormuses</span><span class="sxs-lookup"><span data-stu-id="39d7e-235">Release order set 3 in one load</span></span>

<span data-ttu-id="39d7e-236">Kaks saadetist peaks olema loodud.</span><span class="sxs-lookup"><span data-stu-id="39d7e-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="39d7e-237">Esimene saadetis sisaldab tellimuse ridu müügitellimuselt, kus välja **Kliendi ostutellimus** väärtuseks on seatud *1*.</span><span class="sxs-lookup"><span data-stu-id="39d7e-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="39d7e-238">Teine saadetis sisaldab tellimuse ridu müügitellimuselt, kus välja **Kliendi ostutellimus** väärtuseks on seatud *2*.</span><span class="sxs-lookup"><span data-stu-id="39d7e-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="39d7e-239">4. tellimuse komplekti väljastamine ühes koormuses</span><span class="sxs-lookup"><span data-stu-id="39d7e-239">Release order set 4 in one load</span></span>

<span data-ttu-id="39d7e-240">Neli saadetist peaks olema loodud.</span><span class="sxs-lookup"><span data-stu-id="39d7e-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="39d7e-241">Kliendi konto *USA-003* kahe tellimuse read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.</span><span class="sxs-lookup"><span data-stu-id="39d7e-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="39d7e-242">Kliendi konto *USA-004* kahe tellimuse read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.</span><span class="sxs-lookup"><span data-stu-id="39d7e-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="39d7e-243">Kliendi konto *USA-007* tellimuste 4–5 ja 4–6 read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.</span><span class="sxs-lookup"><span data-stu-id="39d7e-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="39d7e-244">Kliendi konto *USA-007* tellimuste 4–7 ja 4–8 read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *CrossOrder* abil.</span><span class="sxs-lookup"><span data-stu-id="39d7e-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39d7e-245">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="39d7e-245">Additional resources</span></span>

- [<span data-ttu-id="39d7e-246">Saadetise konsolideerimispoliitikad</span><span class="sxs-lookup"><span data-stu-id="39d7e-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="39d7e-247">Saadetise konsolideerimispoliitikate konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="39d7e-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]