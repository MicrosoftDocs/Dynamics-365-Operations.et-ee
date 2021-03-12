---
title: Saadetiste käsitsi konsolideerimine saadetiste konsolideerimise lehe abil
description: Selles teemas kirjeldatakse stsenaariumi, kus lattu vabastatakse mitu tellimust ja seejärel konsolideeritakse saadetiste konsolideerimise lehe abil.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0e580253de0d787b721c2f729ecc96db56b91af0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983011"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="8f2ab-103">Saadetiste käsitsi konsolideerimine saadetiste konsolideerimise lehe abil</span><span class="sxs-lookup"><span data-stu-id="8f2ab-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f2ab-104">Selles teemas kirjeldatakse stsenaariumi, kus lattu vabastatakse mitu tellimust ja seejärel konsolideeritakse lehe **Saadetiste konsolideerimine** abil.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="8f2ab-105">Demoandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="8f2ab-105">Make demo data available</span></span>

<span data-ttu-id="8f2ab-106">Selle teema stsenaarium viitab väärtustele ja kirjetele, mis kuuluvad Microsoft Dynamics 365 Supply Chain Managementile esitatud standardsete demoandmete hulka.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="8f2ab-107">Kui soovite kasutada siin esitatud väärtusi harjutuste tegemise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks **USMF**.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="8f2ab-108">Saadetise konsolideerimispoliitikate ja tootefiltrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="8f2ab-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="8f2ab-109">Siin kirjeldatud stsenaarium eeldab, et olete juba funktsiooni sisse lülitanud, sooritanud [saadetise konsolideerimispoliitikate konfigureerimise](configure-shipment-consolidation-policies.md) harjutused ning loonud poliitikad ja muud seal kirjeldatud kirjed.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="8f2ab-110">Veenduge, et olete enne selle stsenaariumi jätkamist sooritanud need harjutused.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="8f2ab-111">Müügitellimuste loomine selle stsenaariumi jaoks</span><span class="sxs-lookup"><span data-stu-id="8f2ab-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="8f2ab-112">Alustage müügitellimuste kogumi loomisega, millega saate töötada.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="8f2ab-113">Peate töötama laoga, kus on lubatud täpsema laohalduse (WMS) protsessid.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="8f2ab-114">Kui pole konkreetselt viidatud mõnele muule laole, tuleb kasutada sama ladu kõigi järgmiste tellimuste kogumite puhul.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="8f2ab-115">Avage jaotis **Müügireskontro \> Tellimused \> Kõik müügitellimused** ja looge müügitellimuste kogum, millel on järgmistes alamjaotistes kirjeldatud sätted.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="8f2ab-116">Looge müügitellimus 1 ja 2</span><span class="sxs-lookup"><span data-stu-id="8f2ab-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="8f2ab-117">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="8f2ab-118">**Kliendi konto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="8f2ab-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="8f2ab-119">**Kaust:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="8f2ab-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="8f2ab-120">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8f2ab-121">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="8f2ab-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8f2ab-122">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8f2ab-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="8f2ab-123">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="8f2ab-124">Looge müügitellimus 3 ja 4</span><span class="sxs-lookup"><span data-stu-id="8f2ab-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="8f2ab-125">Looge kaks identset müügitellimust järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="8f2ab-126">**Kliendi konto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="8f2ab-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="8f2ab-127">**Kaust:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="8f2ab-128">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="8f2ab-129">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="8f2ab-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="8f2ab-130">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="8f2ab-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="8f2ab-131">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="8f2ab-132">Väljastage tellimused lattu</span><span class="sxs-lookup"><span data-stu-id="8f2ab-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="8f2ab-133">Järgige neid etappe iga selle stsenaariumi jaoks loodud müügitellimuse väljastamiseks lattu.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="8f2ab-134">Avage jaotis **Müügireskontro \> Tellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="8f2ab-135">Otsige üles ja valige väljastatav müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="8f2ab-136">Tehke Toimingupaani vahekaardil **Ladu** valik **Tegevused \> Vabasta lattu**, et väljastada valitud müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="8f2ab-137">Korrake seda protseduuri kõigi selle stsenaariumi jaoks loodud müügitellimuste puhul.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="8f2ab-138">Konsolideeri saadetised</span><span class="sxs-lookup"><span data-stu-id="8f2ab-138">Consolidate shipments</span></span>

1. <span data-ttu-id="8f2ab-139">Avage **Laohaldus \> Saadetised \> Kõik saadetised**.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="8f2ab-140">Otsige üles ja valige saadetis, mis loodi 1. müügitellimuse väljastamisel lattu.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="8f2ab-141">(Selle välja **Saadetise konsolideerimispoliitika** väärtuseks olema seatud *Tellimuse kaust* .)</span><span class="sxs-lookup"><span data-stu-id="8f2ab-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="8f2ab-142">Valige toimingupaani vahekaardil **Saadetised** suvand **Saadetised \> Saadetiste konsolideerimine**.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="8f2ab-143">Kinnitage konsolideerimiseks soovitatud saadetised.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="8f2ab-144">Konsolideerimiseks peaks olema soovitatud ainult üht sama poliitikaga saadetis.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="8f2ab-145">Sulgege leht **Saadetise konsolideerimine**.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="8f2ab-146">Otsige üles ja valige saadetis, mis loodi 3. müügitellimuse väljastamisel lattu.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="8f2ab-147">(Selle välja **Saadetise konsolideerimispoliitika** väärtuseks olema seatud *Vaikimisi* .)</span><span class="sxs-lookup"><span data-stu-id="8f2ab-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="8f2ab-148">Valige toimingupaani vahekaardil **Saadetised** suvand **Saadetised \> Saadetiste konsolideerimine**.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="8f2ab-149">Kinnitage, et konsolideerimiseks pole soovitatud saadetisi.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="8f2ab-150">Valige **Kuva filtrid**.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="8f2ab-151">Eemaldage paanil **Filtrid** filter **Tellimuse number** ja seejärel valige **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="8f2ab-152">Kinnitage konsolideerimiseks soovitatud saadetised.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="8f2ab-153">Konsolideerimiseks peaks olema soovitatud ainult üht sama poliitikaga saadetis.</span><span class="sxs-lookup"><span data-stu-id="8f2ab-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8f2ab-154">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="8f2ab-154">Additional resources</span></span>

- [<span data-ttu-id="8f2ab-155">Saadetise konsolideerimispoliitikad</span><span class="sxs-lookup"><span data-stu-id="8f2ab-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="8f2ab-156">Saadetise konsolideerimispoliitikate konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="8f2ab-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)