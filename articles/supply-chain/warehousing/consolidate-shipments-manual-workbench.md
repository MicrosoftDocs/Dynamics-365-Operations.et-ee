---
title: Saadetiste konsolideerimine saadetise konsolideerimise töölaua abil
description: Selles teemas kirjeldatakse stsenaariumi, kus lattu vabastatakse mitu tellimust ja seejärel konsolideeritakse saadetiseks saadetise konsolideerimise töölaua abil.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 1eec1a8e3a9a2a0f95302e1d6ea68eb90b9a3b93
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016812"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="9d9a3-103">Saadetiste konsolideerimine saadetise konsolideerimise töölaua abil</span><span class="sxs-lookup"><span data-stu-id="9d9a3-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d9a3-104">Selles teemas kirjeldatakse stsenaariumi, kus lattu vabastatakse mitu tellimust ja seejärel konsolideeritakse saadetiseks saadetise konsolideerimise töölaua abil.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="9d9a3-105">Demoandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="9d9a3-105">Make demo data available</span></span>

<span data-ttu-id="9d9a3-106">Selle teema stsenaarium viitab väärtustele ja kirjetele, mis kuuluvad Microsoft Dynamics 365 Supply Chain Managementile esitatud standardsete demoandmete hulka.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="9d9a3-107">Kui soovite kasutada siin esitatud väärtusi harjutuste tegemise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks **USMF**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="9d9a3-108">Saadetise konsolideerimispoliitikate ja tootefiltrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="9d9a3-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="9d9a3-109">Siin kirjeldatud stsenaarium eeldab, et olete juba funktsiooni sisse lülitanud, sooritanud [saadetise konsolideerimispoliitikate konfigureerimise](configure-shipment-consolidation-policies.md) harjutused ning loonud poliitikad ja muud seal kirjeldatud kirjed.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="9d9a3-110">Veenduge, et olete enne selle stsenaariumi jätkamist sooritanud need harjutused.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="9d9a3-111">Saadetise käsitsi konsolideerimise funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="9d9a3-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="9d9a3-112">Enne funktsiooni *Saadetise käsitsi konsolideerimine* kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="9d9a3-113">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="9d9a3-114">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="9d9a3-115">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="9d9a3-116">**Funktsiooni nimi:** *Saadetise käsitsi konsolideerimine*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="9d9a3-117">Vastavalt jaotises [Saadetiste konsolideerimispoliitikate konfigureerimine](configure-shipment-consolidation-policies.md) kirjeldatule, peate enne poliitikate loomist funktsiooni *Saadetise konsolideerimine* sisse lülitamine.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="9d9a3-118">Kuid see etapp peaks olema teil juba lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="9d9a3-119">Müügitellimuste loomine selle stsenaariumi jaoks</span><span class="sxs-lookup"><span data-stu-id="9d9a3-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="9d9a3-120">Alustage müügitellimuste kogumi loomisega, millega saate töötada.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="9d9a3-121">Peate töötama laoga, kus on lubatud täpsema laohalduse (WMS) protsessid.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="9d9a3-122">Kui pole konkreetselt viidatud mõnele muule laole, tuleb kasutada sama ladu kõigi järgmiste tellimuste kogumite puhul.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="9d9a3-123">Avage jaotis **Müügireskontro \> Tellimused \> Kõik müügitellimused** ja looge müügitellimuste kogum, millel on järgmistes alamjaotistes kirjeldatud sätted.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-123">Go to **Accounts receivable \> Orders \> All sales orders** , and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="9d9a3-124">Tellimuse komplekti 1 loomine</span><span class="sxs-lookup"><span data-stu-id="9d9a3-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="9d9a3-125">Müügitellimused 1-1 ja 1-2</span><span class="sxs-lookup"><span data-stu-id="9d9a3-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="9d9a3-126">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9d9a3-127">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9d9a3-128">**Tarneviis:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9d9a3-129">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9d9a3-130">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4** )</span><span class="sxs-lookup"><span data-stu-id="9d9a3-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9d9a3-131">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9d9a3-132">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-132">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="9d9a3-133">Müügitellimus 1-3</span><span class="sxs-lookup"><span data-stu-id="9d9a3-133">Sales order 1-3</span></span>

1. <span data-ttu-id="9d9a3-134">Looge järgmiste sätetega müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9d9a3-135">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9d9a3-136">**Tarneviis:** *10*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="9d9a3-137">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9d9a3-138">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4** )</span><span class="sxs-lookup"><span data-stu-id="9d9a3-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9d9a3-139">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9d9a3-140">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-140">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="9d9a3-141">Lisage teine järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="9d9a3-142">**Kaubakood:** *A0002* (kaup, millele pole määratud filtrit **Kood 4** )</span><span class="sxs-lookup"><span data-stu-id="9d9a3-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9d9a3-143">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="9d9a3-144">**Tarneviis:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9d9a3-145">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan teise tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-145">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="9d9a3-146">Tellimuse komplekti 2 loomine</span><span class="sxs-lookup"><span data-stu-id="9d9a3-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="9d9a3-147">Müügitellimused 2-1 ja 2-2</span><span class="sxs-lookup"><span data-stu-id="9d9a3-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="9d9a3-148">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9d9a3-149">**Kliendi konto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="9d9a3-150">**Tarneviis:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9d9a3-151">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9d9a3-152">**Kaubakood:** *M9200* (kaup, kus filtri **Kood 4** väärtuseks on seatud *Kergsüttiv* )</span><span class="sxs-lookup"><span data-stu-id="9d9a3-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable* )</span></span>
    - <span data-ttu-id="9d9a3-153">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9d9a3-154">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-154">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="9d9a3-155">Lisage teine järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="9d9a3-156">**Kaubakood:** *M9201* (kaup, kus filtri **Kood 4** väärtuseks on seatud *Lõhkeaine* )</span><span class="sxs-lookup"><span data-stu-id="9d9a3-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive* )</span></span>
    - <span data-ttu-id="9d9a3-157">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="9d9a3-158">**Tarneviis:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="9d9a3-159">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan teise tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-159">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="9d9a3-160">Tellimuse komplekti 3 loomine</span><span class="sxs-lookup"><span data-stu-id="9d9a3-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="9d9a3-161">Müügitellimused 3-1 ja 3-2</span><span class="sxs-lookup"><span data-stu-id="9d9a3-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="9d9a3-162">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9d9a3-163">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9d9a3-164">**Kliendi ostutellimus:** *1*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="9d9a3-165">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9d9a3-166">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4** )</span><span class="sxs-lookup"><span data-stu-id="9d9a3-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9d9a3-167">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9d9a3-168">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-168">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="9d9a3-169">Müügitellimused 3-3 ja 3-4</span><span class="sxs-lookup"><span data-stu-id="9d9a3-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="9d9a3-170">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9d9a3-171">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9d9a3-172">**Kliendi ostutellimus:** *2*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="9d9a3-173">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9d9a3-174">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4** )</span><span class="sxs-lookup"><span data-stu-id="9d9a3-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9d9a3-175">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9d9a3-176">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-176">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="9d9a3-177">Tellimuse komplekti 4 loomine</span><span class="sxs-lookup"><span data-stu-id="9d9a3-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="9d9a3-178">Müügitellimused 4-1 ja 4-2</span><span class="sxs-lookup"><span data-stu-id="9d9a3-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="9d9a3-179">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9d9a3-180">**Kliendi konto:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="9d9a3-181">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9d9a3-182">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4** )</span><span class="sxs-lookup"><span data-stu-id="9d9a3-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9d9a3-183">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9d9a3-184">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-184">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="9d9a3-185">Müügitellimused 4-3 ja 4-4</span><span class="sxs-lookup"><span data-stu-id="9d9a3-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="9d9a3-186">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9d9a3-187">**Kliendi konto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="9d9a3-188">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9d9a3-189">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4** )</span><span class="sxs-lookup"><span data-stu-id="9d9a3-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9d9a3-190">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9d9a3-191">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-191">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="9d9a3-192">Müügitellimused 4-5 ja 4-6</span><span class="sxs-lookup"><span data-stu-id="9d9a3-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="9d9a3-193">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9d9a3-194">**Kliendi konto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="9d9a3-195">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-195">**Site:** *6*</span></span>
    - <span data-ttu-id="9d9a3-196">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="9d9a3-197">**Kaust:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="9d9a3-198">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9d9a3-199">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4** )</span><span class="sxs-lookup"><span data-stu-id="9d9a3-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9d9a3-200">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9d9a3-201">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-201">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="9d9a3-202">Müügitellimused 4-7 ja 4-8</span><span class="sxs-lookup"><span data-stu-id="9d9a3-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="9d9a3-203">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="9d9a3-204">**Kliendi konto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="9d9a3-205">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-205">**Site:** *6*</span></span>
    - <span data-ttu-id="9d9a3-206">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="9d9a3-207">**Kaust:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="9d9a3-208">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="9d9a3-209">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4** )</span><span class="sxs-lookup"><span data-stu-id="9d9a3-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="9d9a3-210">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="9d9a3-211">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-211">Select **Inventory \> Reservation** , and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="9d9a3-212">Väljastage tellimused lattu</span><span class="sxs-lookup"><span data-stu-id="9d9a3-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="9d9a3-213">Järgige neid etappe iga selle stsenaariumi jaoks loodud müügitellimuse väljastamiseks lattu.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="9d9a3-214">Avage jaotis **Müügireskontro \> Tellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="9d9a3-215">Otsige üles ja valige väljastatav müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="9d9a3-216">Tehke Toimingupaani vahekaardil **Ladu** valik **Tegevused \> Vabasta lattu** , et väljastada valitud müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="9d9a3-217">Korrake seda protseduuri kõigi selle stsenaariumi jaoks loodud müügitellimuste puhul.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="9d9a3-218">Saadetiste konsolideerimine saadetise konsolideerimise töölaua abil</span><span class="sxs-lookup"><span data-stu-id="9d9a3-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="9d9a3-219">Avage jaotis **Laohaldus \> Lattu väljastamine \> Saadetise konsoldeerimise töölaud**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="9d9a3-220">Valige Toimingupaanil nupp **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="9d9a3-221">Valige päringu redaktori dialoogiboksis vahekaardil **Vahemik** suvand  **Lisa** , et lisada järgmiste sätetega rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="9d9a3-222">**Tabel:** *Müügitellimused*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="9d9a3-223">**Väli:** *Müügitellimus*</span><span class="sxs-lookup"><span data-stu-id="9d9a3-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="9d9a3-224">**Kriteeriumid:** sisestage iga selle stsenaariumi jaoks loodud tellimusele komaeraldusega müügitellimuse numbrite loend.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="9d9a3-225">Oma päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="9d9a3-226">Valige Toimingupaanil suvand **Saadetise konsolideerimine**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="9d9a3-227">Valige kõik saadetised ja valige Toimingupaanil suvand **Konsolideerimine**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="9d9a3-228">Saadetiste kontrollimine</span><span class="sxs-lookup"><span data-stu-id="9d9a3-228">Verify the shipments</span></span>

<span data-ttu-id="9d9a3-229">Järgmine protseduur võimaldab teil kontrollida saadetise konsolideerimise käigus loodud või värskendatud saadetisi.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="9d9a3-230">Kasutage seda iga selle stsenaariumi jaoks loodud tellimuse komplekti läbivaatamiseks ja vaadake üle järgnevad alamjaotised veendumaks, et saavutasite oodatud tulemused.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="9d9a3-231">Avage **Laohaldus \> Saadetised \> Kõik saadetised**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="9d9a3-232">Otsige üles ja valige nõutav saadetis.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="9d9a3-233">Kui saadetise loomise või värskendamise ajal kasutati konsolideerimispoliitikat, kasutage välja **Saadetise konsolideerimispoliitika**.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="9d9a3-234">Tellimuse komplektiga 1 seostatud saadetised</span><span class="sxs-lookup"><span data-stu-id="9d9a3-234">Related shipments for order set 1</span></span>

<span data-ttu-id="9d9a3-235">Kaks saadetist peaks olema loodud.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="9d9a3-236">Esimene saadetis sisaldab kolme rida ja loodi saadetise konsolideerimispoliitika *CustomerMode* abil.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="9d9a3-237">Teine saadetis, mis ei kasuta transportimisel tarneviisi *Lennutransport* , loodi saadetise konsolideerimispoliitika *CustomerOrderNo* abil.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="9d9a3-238">Tellimuse komplektiga 2 seostatud saadetised</span><span class="sxs-lookup"><span data-stu-id="9d9a3-238">Related shipments for order set 2</span></span>

<span data-ttu-id="9d9a3-239">Kolm saadetist peaks olema loodud.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="9d9a3-240">Esimene saadetis sisaldab *Kergsüttivaid* kaupu.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="9d9a3-241">Ülejäänud kaks saadetist sisaldavad ühte rida, millel on kaup *Lõhkeaine*.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="9d9a3-242">Tellimuse komplektiga 3 seostatud saadetised</span><span class="sxs-lookup"><span data-stu-id="9d9a3-242">Related shipments for order set 3</span></span>

<span data-ttu-id="9d9a3-243">Kaks saadetist peaks olema loodud.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="9d9a3-244">Esimene saadetis sisaldab tellimuse ridu müügitellimuselt, kus välja **Kliendi ostutellimus** väärtuseks on seatud *1*.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="9d9a3-245">Teine saadetis sisaldab tellimuse ridu müügitellimuselt, kus välja **Kliendi ostutellimus** väärtuseks on seatud *2*.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="9d9a3-246">Tellimuse komplektiga 4 seostatud saadetised</span><span class="sxs-lookup"><span data-stu-id="9d9a3-246">Related shipments for order set 4</span></span>

<span data-ttu-id="9d9a3-247">Neli saadetist peaks olema loodud.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="9d9a3-248">Kliendi *USA-003* kahe tellimuse read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="9d9a3-249">Kliendi *USA-004* kahe tellimuse read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="9d9a3-250">Kliendi *USA-007* tellimuste 4-5 ja 4-6 read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="9d9a3-251">Kliendi *USA-007* tellimuste 4-7 ja 4-8 read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *CrossOrder* abil.</span><span class="sxs-lookup"><span data-stu-id="9d9a3-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9d9a3-252">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="9d9a3-252">Additional resources</span></span>

- [<span data-ttu-id="9d9a3-253">Saadetise konsolideerimispoliitikad</span><span class="sxs-lookup"><span data-stu-id="9d9a3-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="9d9a3-254">Saadetise konsolideerimispoliitikate konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="9d9a3-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
