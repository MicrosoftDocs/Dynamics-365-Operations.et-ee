---
title: Saadetiste konsolideerimine, kui need väljastatakse lattu müügitellimuste automaatse väljastamise abil
description: Selles teemas kirjeldatakse stsenaariumi, kus lattu vabastatakse mitu tellimust sama automaatse perioodilise lattu väljastamise protseduuri käigus.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 7102eade4a26f4b4dc08adb395aa7b50a630b9d9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243939"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="b5ac3-103">Saadetiste konsolideerimine, kui need väljastatakse lattu müügitellimuste automaatse väljastamise abil</span><span class="sxs-lookup"><span data-stu-id="b5ac3-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5ac3-104">Selles teemas kirjeldatakse stsenaariumi, kus lattu vabastatakse mitu tellimust sama automaatse perioodilise lattu väljastamise protseduuri käigus.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="b5ac3-105">Tellimused konsolideeritakse saadetisteks automaatselt saadetiste konsolideerimispoliitikatena määratletud reeglite põhjal.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="b5ac3-106">Selle stsenaariumi käigus loote müügitellimuste komplekti ja väljastate kõik komplektid lattu.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="b5ac3-107">Seejärel saate saadetise konsolideerimise käigus loodud või värskendatud saadetised nende konfigureeritud poliitikate põhjal üle vaadata.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="b5ac3-108">Demoandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="b5ac3-108">Make demo data available</span></span>

<span data-ttu-id="b5ac3-109">Selle teema stsenaarium viitab väärtustele ja kirjetele, mis kuuluvad Microsoft Dynamics 365 Supply Chain Managementile esitatud standardsete demoandmete hulka.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="b5ac3-110">Kui soovite kasutada siin esitatud väärtusi harjutuste tegemise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks **USMF**.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="b5ac3-111">Saadetise konsolideerimispoliitikate ja tootefiltrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="b5ac3-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="b5ac3-112">Siin kirjeldatud stsenaarium eeldab, et olete juba funktsiooni sisse lülitanud, sooritanud [saadetise konsolideerimispoliitikate konfigureerimise](configure-shipment-consolidation-policies.md) harjutused ning loonud poliitikad ja muud seal kirjeldatud kirjed.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="b5ac3-113">Veenduge, et olete enne selle stsenaariumi jätkamist sooritanud need harjutused.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="b5ac3-114">Müügitellimuste loomine selle stsenaariumi jaoks</span><span class="sxs-lookup"><span data-stu-id="b5ac3-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="b5ac3-115">Alustage müügitellimuste kogumi loomisega, millega saate töötada.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="b5ac3-116">Peate töötama laoga, kus on lubatud täpsema laohalduse (WMS) protsessid.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="b5ac3-117">Kui pole konkreetselt viidatud mõnele muule laole, tuleb kasutada sama ladu kõigi järgmiste tellimuste kogumite puhul.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="b5ac3-118">Avage jaotis **Müügireskontro \> Tellimused \> Kõik müügitellimused** ja looge müügitellimuste kogum, millel on järgmistes alamjaotistes kirjeldatud sätted.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="b5ac3-119">Tellimuse komplekti 1 loomine</span><span class="sxs-lookup"><span data-stu-id="b5ac3-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="b5ac3-120">Müügitellimus 1-1</span><span class="sxs-lookup"><span data-stu-id="b5ac3-120">Sales order 1-1</span></span>

1. <span data-ttu-id="b5ac3-121">Looge järgmiste sätetega müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-122">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b5ac3-123">**Tarneviis:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="b5ac3-124">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-125">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="b5ac3-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5ac3-126">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="b5ac3-127">Müügitellimus 1-2</span><span class="sxs-lookup"><span data-stu-id="b5ac3-127">Sales order 1-2</span></span>

1. <span data-ttu-id="b5ac3-128">Looge järgmiste sätetega müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-129">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b5ac3-130">**Tarneviis:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="b5ac3-131">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-132">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="b5ac3-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5ac3-133">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="b5ac3-134">Müügitellimus 1-3</span><span class="sxs-lookup"><span data-stu-id="b5ac3-134">Sales order 1-3</span></span>

1. <span data-ttu-id="b5ac3-135">Looge järgmiste sätetega müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-136">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b5ac3-137">**Tarneviis:** *10*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="b5ac3-138">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-139">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="b5ac3-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5ac3-140">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b5ac3-141">Lisage teine järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-142">**Kaubakood:** *A0002* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="b5ac3-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5ac3-143">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="b5ac3-144">**Tarneviis:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="b5ac3-145">Tellimuse komplekti 2 loomine</span><span class="sxs-lookup"><span data-stu-id="b5ac3-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="b5ac3-146">Müügitellimused 2-1 ja 2-2</span><span class="sxs-lookup"><span data-stu-id="b5ac3-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="b5ac3-147">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b5ac3-148">**Kliendi konto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="b5ac3-149">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-150">**Kaubakood:** *M9200* (kaup, kus filtri **Kood 4** väärtuseks on seatud *Kergsüttiv*)</span><span class="sxs-lookup"><span data-stu-id="b5ac3-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="b5ac3-151">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b5ac3-152">Lisage teine järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-153">**Kaubakood:** *M9201* (kaup, kus filtri **Kood 4** väärtuseks on seatud *Lõhkeaine*)</span><span class="sxs-lookup"><span data-stu-id="b5ac3-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="b5ac3-154">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="b5ac3-155">**Tarneviis:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="b5ac3-156">Tellimuse komplekti 3 loomine</span><span class="sxs-lookup"><span data-stu-id="b5ac3-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="b5ac3-157">Müügitellimus 3-1</span><span class="sxs-lookup"><span data-stu-id="b5ac3-157">Sales order 3-1</span></span>

1. <span data-ttu-id="b5ac3-158">Looge järgmiste sätetega müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-159">**Kliendi konto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="b5ac3-160">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-161">**Kaubakood:** *M9200* (kaup, kus filtri **Kood 4** väärtuseks on seatud *Kergsüttiv*)</span><span class="sxs-lookup"><span data-stu-id="b5ac3-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="b5ac3-162">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="b5ac3-163">Lisage teine järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-164">**Kaubakood:** *M9201* (kaup, kus filtri **Kood 4** väärtuseks on seatud *Lõhkeaine*)</span><span class="sxs-lookup"><span data-stu-id="b5ac3-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="b5ac3-165">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="b5ac3-166">**Tarneviis:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="b5ac3-167">See tellimus on identne kahe tellimusega, mille lõite tellimuse komplekti 2 jaoks.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="b5ac3-168">Kuid see loetletakse eraldi tellimuse komplektina, kuna te väljastate selle hiljem antud stsenaariumi käigus.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="b5ac3-169">Tellimuse komplekti 4 loomine</span><span class="sxs-lookup"><span data-stu-id="b5ac3-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="b5ac3-170">Müügitellimus 4-1</span><span class="sxs-lookup"><span data-stu-id="b5ac3-170">Sales order 4-1</span></span>

1. <span data-ttu-id="b5ac3-171">Looge järgmiste sätetega müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-172">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b5ac3-173">**Kliendi ostutellimus:** *1*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="b5ac3-174">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-175">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="b5ac3-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5ac3-176">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="b5ac3-177">Tellimuse komplekti 5 loomine</span><span class="sxs-lookup"><span data-stu-id="b5ac3-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="b5ac3-178">Müügitellimused 5-1 ja 5-2</span><span class="sxs-lookup"><span data-stu-id="b5ac3-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="b5ac3-179">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b5ac3-180">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b5ac3-181">**Kliendi ostutellimus:** *2*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="b5ac3-182">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-183">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="b5ac3-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5ac3-184">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="b5ac3-185">Müügitellimus 5-3</span><span class="sxs-lookup"><span data-stu-id="b5ac3-185">Sales order 5-3</span></span>

1. <span data-ttu-id="b5ac3-186">Looge järgmiste sätetega müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-187">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="b5ac3-188">**Kliendi ostutellimus:** *1*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="b5ac3-189">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-190">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="b5ac3-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5ac3-191">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="b5ac3-192">Tellimuse komplekti 6 loomine</span><span class="sxs-lookup"><span data-stu-id="b5ac3-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="b5ac3-193">Müügitellimused 6-1 ja 6-2</span><span class="sxs-lookup"><span data-stu-id="b5ac3-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="b5ac3-194">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b5ac3-195">**Kliendi konto:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="b5ac3-196">**Kliendi ostutellimus:** *2*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="b5ac3-197">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-198">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="b5ac3-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5ac3-199">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="b5ac3-200">Müügitellimused 6-3 ja 6-4</span><span class="sxs-lookup"><span data-stu-id="b5ac3-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="b5ac3-201">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b5ac3-202">**Kliendi konto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="b5ac3-203">**Kliendi ostutellimus:** *1*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="b5ac3-204">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-205">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="b5ac3-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5ac3-206">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="b5ac3-207">Müügitellimused 6-5 ja 6-6</span><span class="sxs-lookup"><span data-stu-id="b5ac3-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="b5ac3-208">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b5ac3-209">**Kliendi konto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="b5ac3-210">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-210">**Site:** *6*</span></span>
    - <span data-ttu-id="b5ac3-211">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="b5ac3-212">**Kaust:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="b5ac3-213">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-214">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="b5ac3-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5ac3-215">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="b5ac3-216">Müügitellimused 6-7 ja 6-8</span><span class="sxs-lookup"><span data-stu-id="b5ac3-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="b5ac3-217">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="b5ac3-218">**Kliendi konto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="b5ac3-219">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-219">**Site:** *6*</span></span>
    - <span data-ttu-id="b5ac3-220">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="b5ac3-221">**Kaust:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="b5ac3-222">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="b5ac3-223">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="b5ac3-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="b5ac3-224">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="b5ac3-225">Müügitellimuste automaatne lattu väljastamine</span><span class="sxs-lookup"><span data-stu-id="b5ac3-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="b5ac3-226">Te viite lõpule automaatse lattu väljastamise protseduuri iga eelnevalt loodud müügitellimuste komplekti kohta.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="b5ac3-227">Viite kõigiga neist läbi siin esitatud [üldise lattu väljastamise protseduuri](#release-procedure).</span><span class="sxs-lookup"><span data-stu-id="b5ac3-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="b5ac3-228">Üldine lattu väljastamise protseduur</span><span class="sxs-lookup"><span data-stu-id="b5ac3-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="b5ac3-229">Te viite lõpule kolm järgmistes alamjaotistes kirjeldatud protseduuri iga eelnevalt loodud müügitellimuste komplekti kohta.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="b5ac3-230">Väljastamise ajal kasutatava voo malli värskendamine</span><span class="sxs-lookup"><span data-stu-id="b5ac3-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="b5ac3-231">Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="b5ac3-232">Määrake välja **Voo malli tüüp** väärtuseks *Lähetamine*.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="b5ac3-233">Otsige üles ja valige voo mall, mis on seostatud laoga, mida kasutasite selle stsenaariumi jaoks loodud tellimuse komplektides.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="b5ac3-234">Kui kasutasite näiteks ladu *24*, valige voo mall **24 saadetise vaikemall**.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="b5ac3-235">Kui kasutasite ladu *61*, valige voo mall **61 saatmine**.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="b5ac3-236">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b5ac3-237">Määrake suvandi **Töötle voogu lattu vabastamisel** väärtuseks *Ei*.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="b5ac3-238">Lattu väljastamine</span><span class="sxs-lookup"><span data-stu-id="b5ac3-238">Release to the warehouse</span></span>

1. <span data-ttu-id="b5ac3-239">Avage jaotis **Laohaldus \> Lattu väljastamine \> Müügitellimuste automaatne väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="b5ac3-240">Määrake välja **Väljastatav kogus** väärtuseks *Kõik*.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="b5ac3-241">Päringu dialoogiboksi avamiseks valige kiirkaardil **Kaasatavad kirjed** suvand **Filter**.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="b5ac3-242">Valige vahekaardil **Vahemik** suvand **Lisa**, et lisada ruudustikule järgmiste sätetega rida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="b5ac3-243">**Tabel:** *Müügitellimus*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="b5ac3-244">**Tuletatud tabel:** *Müügitellimus*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="b5ac3-245">**Väli:** *Müügitellimus*</span><span class="sxs-lookup"><span data-stu-id="b5ac3-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="b5ac3-246">**Kriteeriumid:** sisestage soovitud tellimuse komplekti müügitellimuste numbrite komaeraldusega loend.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="b5ac3-247">Päringu salvestamiseks klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="b5ac3-248">Protseduuri *Automaatne lattu väljastamine* käivitamiseks klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="b5ac3-249">Loodud või värskendatud saadetise ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="b5ac3-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="b5ac3-250">Avage **Laohaldus \> Saadetised \> Kõik saadetised**.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="b5ac3-251">Otsige üles ja valige nõutav saadetis.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="b5ac3-252">Kui saadetise loomise või värskendamise ajal kasutati konsolideerimispoliitikat, kasutage välja **Saadetise konsolideerimispoliitika**.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="b5ac3-253">Müügitellimuste väljastamine tellimuse komplektist 1</span><span class="sxs-lookup"><span data-stu-id="b5ac3-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="b5ac3-254">Müügitellimuste väljastamiseks tellimuse komplektist 1, järgige [üldist lattu väljastamise protseduuri](#release-procedure).</span><span class="sxs-lookup"><span data-stu-id="b5ac3-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="b5ac3-255">Kui olete lõpetanud, peaksite nägema, et loodi kaks saadetist.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="b5ac3-256">Esimene saadetis sisaldab kolme rida ja loodi saadetise konsolideerimispoliitika *CustomerMode* abil.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="b5ac3-257">Teine saadetis, mis ei kasuta transportimisel tarneviisi *Lennutransport*, loodi saadetise konsolideerimispoliitika *CustomerOrderNo* abil.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="b5ac3-258">Müügitellimuste väljastamine tellimuse komplektist 2</span><span class="sxs-lookup"><span data-stu-id="b5ac3-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="b5ac3-259">Müügitellimuste väljastamiseks tellimuse komplektist 2, järgige [üldist lattu väljastamise protseduuri](#release-procedure).</span><span class="sxs-lookup"><span data-stu-id="b5ac3-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="b5ac3-260">Kui olete lõpetanud, peaksite nägema, et loodi kolm saadetist.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="b5ac3-261">Esimene saadetis sisaldab *Kergsüttivaid* kaupu.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="b5ac3-262">Ülejäänud kaks saadetist sisaldavad ühte rida, millel on kaup *Lõhkeaine*.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="b5ac3-263">Müügitellimuste väljastamine tellimuse komplektist 3</span><span class="sxs-lookup"><span data-stu-id="b5ac3-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="b5ac3-264">Müügitellimuste väljastamiseks tellimuse komplektist 3, järgige [üldist lattu väljastamise protseduuri](#release-procedure).</span><span class="sxs-lookup"><span data-stu-id="b5ac3-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="b5ac3-265">Kui olete lõpetanud, peaksite nägema, et ilmnesid järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="b5ac3-266">Värskendati üks olemasolev saadetis (saadetis, mis loodi tellimuse komplekti 2 väljastamisel lattu).</span><span class="sxs-lookup"><span data-stu-id="b5ac3-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="b5ac3-267">Lisati rida, millel on *Kergsüttiv* kaup.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="b5ac3-268">Loodi üks uus saadetis, mis sisaldab kaupa *Lõhkeaine*.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="b5ac3-269">Müügitellimuste väljastamine tellimuse komplektist 4</span><span class="sxs-lookup"><span data-stu-id="b5ac3-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="b5ac3-270">Müügitellimuste väljastamiseks tellimuse komplektist 4, järgige [üldist lattu väljastamise protseduuri](#release-procedure).</span><span class="sxs-lookup"><span data-stu-id="b5ac3-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="b5ac3-271">Kui olete lõpetanud, peaksite nägema, et värskendati üks olemasolev saadetis (kus välja **Kliendi ostutellimus** väärtuseks on seatud *1*).</span><span class="sxs-lookup"><span data-stu-id="b5ac3-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="b5ac3-272">Sellele lisati üks uus rida.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="b5ac3-273">Müügitellimuste väljastamine tellimuse komplektist 5</span><span class="sxs-lookup"><span data-stu-id="b5ac3-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="b5ac3-274">Müügitellimuste väljastamiseks tellimuse komplektist 5, järgige [üldist lattu väljastamise protseduuri](#release-procedure).</span><span class="sxs-lookup"><span data-stu-id="b5ac3-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="b5ac3-275">Kui olete lõpetanud, peaksite nägema, et ilmnesid järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="b5ac3-276">Värskendati üks olemasolev saadetis (kus välja **Kliendi ostutellimus** väärtuseks on seatud *1*).</span><span class="sxs-lookup"><span data-stu-id="b5ac3-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="b5ac3-277">Sellele lisati rida müügitellimusest 5-3 (kus välja **Kliendi ostutellimus** väärtuseks on seatud *1*).</span><span class="sxs-lookup"><span data-stu-id="b5ac3-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="b5ac3-278">Loodi üks uus saadetis, kus müügitellimuste 5-1 ja 5-2 read grupeeritakse ühte saadetisse.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="b5ac3-279">Müügitellimuste väljastamine tellimuse komplektist 6</span><span class="sxs-lookup"><span data-stu-id="b5ac3-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="b5ac3-280">Müügitellimuste väljastamiseks tellimuse komplektist 6, järgige [üldist lattu väljastamise protseduuri](#release-procedure).</span><span class="sxs-lookup"><span data-stu-id="b5ac3-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="b5ac3-281">Kui olete lõpetanud, peaksite nägema, et loodi neli saadetist.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="b5ac3-282">Kliendi *USA-003* kahe tellimuse read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="b5ac3-283">Kliendi *USA-004* kahe tellimuse read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="b5ac3-284">Kliendi *USA-007* tellimuste 6-5 ja 6-6 read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="b5ac3-285">Kliendi *USA-007* tellimuste 6-7 ja 6-8 read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *CrossOrder* abil.</span><span class="sxs-lookup"><span data-stu-id="b5ac3-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5ac3-286">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b5ac3-286">Additional resources</span></span>

- [<span data-ttu-id="b5ac3-287">Saadetise konsolideerimispoliitikad</span><span class="sxs-lookup"><span data-stu-id="b5ac3-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="b5ac3-288">Saadetise konsolideerimispoliitikate konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b5ac3-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]