---
title: Saadetiste konsolideerimine, kui lehel Lattu väljastamine alistatakse saadetise konsolideerimispoliitika
description: Selles teemas kirjeldatakse stsenaariumi, kus tuleb vähemalt üks müügirida väljastada lattu käsitsi lehe Lattu väljastamine kaudu ja enne väljastamist alistada süsteemi määratletud saadetise konsolideerimispoliitika.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 4aaaa7949d988607b38dd6e38a3c3497f227b8af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963331"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a><span data-ttu-id="34e76-103">Saadetiste konsolideerimine, kui lehel Lattu väljastamine alistatakse saadetise konsolideerimispoliitika</span><span class="sxs-lookup"><span data-stu-id="34e76-103">Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34e76-104">Selles teemas kirjeldatakse stsenaariumi, kus tuleb vähemalt üks müügirida väljastada lattu käsitsi lehe **Lattu väljastamine** kaudu ja enne väljastamist alistada süsteemi määratletud saadetise konsolideerimispoliitika.</span><span class="sxs-lookup"><span data-stu-id="34e76-104">This topic presents a scenario where one or more sales lines must be manually released to the warehouse from the **Release to warehouse** page, and the system-defined shipment consolidation policy must be overridden before the release.</span></span> <span data-ttu-id="34e76-105">Saadetiste konsolideerimispoliitika alistamine võib olla nõutav, kui näiteks tellimus, mida tavaliselt ei konsolideerita avatud saadetistega, tuleb konsolideerida avatud saadetistega.</span><span class="sxs-lookup"><span data-stu-id="34e76-105">An override of the shipment consolidation policy might be required if, for example, an order that isn't usually consolidated with open shipments must be consolidated with open shipments.</span></span>

<span data-ttu-id="34e76-106">Selle stsenaariumi käigus loote müügitellimuste komplekti ja seejärel alistate vaikimisi saadetise konsolideerimispoliitika enne tellimuste lattu väljastamist.</span><span class="sxs-lookup"><span data-stu-id="34e76-106">During the scenario, you will create a set of sales orders and then override the default shipment consolidation policy before you release the orders to the warehouse.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="34e76-107">Demoandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="34e76-107">Make demo data available</span></span>

<span data-ttu-id="34e76-108">Selle teema stsenaarium viitab väärtustele ja kirjetele, mis kuuluvad Microsoft Dynamics 365 Supply Chain Managementile esitatud standardsete demoandmete hulka.</span><span class="sxs-lookup"><span data-stu-id="34e76-108">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="34e76-109">Kui soovite kasutada siin esitatud väärtusi harjutuste tegemise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks **USMF**.</span><span class="sxs-lookup"><span data-stu-id="34e76-109">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="34e76-110">Saadetise konsolideerimispoliitikate ja tootefiltrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="34e76-110">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="34e76-111">Siin kirjeldatud stsenaarium eeldab, et olete juba funktsiooni sisse lülitanud, sooritanud [saadetise konsolideerimispoliitikate konfigureerimise](configure-shipment-consolidation-policies.md) harjutused ning loonud poliitikad ja muud seal kirjeldatud kirjed.</span><span class="sxs-lookup"><span data-stu-id="34e76-111">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="34e76-112">Veenduge, et olete enne selle stsenaariumi jätkamist sooritanud need harjutused.</span><span class="sxs-lookup"><span data-stu-id="34e76-112">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="34e76-113">Müügitellimuste loomine selle stsenaariumi jaoks</span><span class="sxs-lookup"><span data-stu-id="34e76-113">Create the sales orders for this scenario</span></span>

1. <span data-ttu-id="34e76-114">Avage jaotis **Müügireskontro \> Tellimused \> Kõik müügitellimused** ja looge kolm identset müügitellimust, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="34e76-114">Go to **Accounts receivable \> Orders \> All sales orders**, and create three identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="34e76-115">**Kliendi konto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="34e76-115">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="34e76-116">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="34e76-116">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="34e76-117">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="34e76-117">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="34e76-118">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="34e76-118">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="34e76-119">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="34e76-119">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a><span data-ttu-id="34e76-120">Müügitellimuste väljastamine lehelt Lattu väljastamine</span><span class="sxs-lookup"><span data-stu-id="34e76-120">Release the sales orders from the Release to warehouse page</span></span>

<span data-ttu-id="34e76-121">Järgige neid juhiseid saadetise konsolideerimispoliitika alistamiseks lattu väljastamise ajal.</span><span class="sxs-lookup"><span data-stu-id="34e76-121">Follow these steps to override the shipment consolidation policy during the release to the warehouse.</span></span>

1. <span data-ttu-id="34e76-122">Avage jaotis **Laohaldus \> Lattu väljastamine \> Lattu väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="34e76-122">Go to **Warehouse management \> Release to warehouse \> Release to warehouse**.</span></span>
1. <span data-ttu-id="34e76-123">Valige ülemisel paanil esimene selle stsenaariumi jaoks loodud müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="34e76-123">In the upper pane, select the first sales order that you created for this scenario.</span></span>
1. <span data-ttu-id="34e76-124">Valige **Lisa**, et lisada rida lattu väljastamisele.</span><span class="sxs-lookup"><span data-stu-id="34e76-124">Select **Add** to add the line to the release to the warehouse.</span></span> <span data-ttu-id="34e76-125">Pange tähele, et *Vaikimisi* saadetise konsolideerimispoliitika rakendatakse alumisel paanil.</span><span class="sxs-lookup"><span data-stu-id="34e76-125">Notice that the *Default* shipment consolidation policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="34e76-126">Valige alumisel paanil **Uue saadetise konsolideerimispoliitika valimine**.</span><span class="sxs-lookup"><span data-stu-id="34e76-126">In the bottom pane, select **Select new shipment consolidation policy**.</span></span>
1. <span data-ttu-id="34e76-127">Valige poliitika, mis lubab sama poliitika teiste avatud saadetiste konsolideerimist.</span><span class="sxs-lookup"><span data-stu-id="34e76-127">Select a policy that allows for consolidation with other open shipments of the same policy.</span></span> <span data-ttu-id="34e76-128">Valige näiteks poliitika *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="34e76-128">For example, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="34e76-129">Valige **Lattu väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="34e76-129">Select **Release to warehouse**.</span></span>
1. <span data-ttu-id="34e76-130">Valige selle stsenaariumi jaoks loodud teine ja kolmas müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="34e76-130">Select the second and third sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="34e76-131">Valige **Lisa**, et lisada read lattu väljastamisele.</span><span class="sxs-lookup"><span data-stu-id="34e76-131">Select **Add** to add the lines to the release to the warehouse.</span></span> <span data-ttu-id="34e76-132">Pange tähele, et *Vaikimisi* poliitika rakendatakse alumisel paanil.</span><span class="sxs-lookup"><span data-stu-id="34e76-132">Notice that the *Default* policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="34e76-133">Valige teine rida ja seejärel valige väljal **Uue saadetise konsolideerimispoliitika valimine** poliitika *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="34e76-133">Select the second line, and then, in the **Select new shipment consolidation policy** field, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="34e76-134">Valige mõlemal real **Lattu väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="34e76-134">Select **Release to warehouse** for both lines.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="34e76-135">Saadetiste kontrollimine</span><span class="sxs-lookup"><span data-stu-id="34e76-135">Verify the shipments</span></span>

<span data-ttu-id="34e76-136">Kaks saadetist peaks olema loodud.</span><span class="sxs-lookup"><span data-stu-id="34e76-136">Two shipments should have been created:</span></span>

- <span data-ttu-id="34e76-137">Esimene saadetis sisaldab kahte rida ja loodi saadetise konsolideerimispoliitika *CustomerOrderNo* abil.</span><span class="sxs-lookup"><span data-stu-id="34e76-137">The first shipment contains two lines and was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>
- <span data-ttu-id="34e76-138">Teine saadetis sisaldab ühte rida ja loodi saadetise konsolideerimispoliitika *Vaikimisi* abil.</span><span class="sxs-lookup"><span data-stu-id="34e76-138">The second shipment contains one line and was created by using the *Default* shipment consolidation policy.</span></span>

<span data-ttu-id="34e76-139">Loodud saadetiste ülevaatamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="34e76-139">Follow these steps to review the shipments that were created.</span></span>

1. <span data-ttu-id="34e76-140">Avage **Laohaldus \> Saadetised \> Kõik saadetised**.</span><span class="sxs-lookup"><span data-stu-id="34e76-140">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="34e76-141">Otsige üles ja valige nõutav saadetis.</span><span class="sxs-lookup"><span data-stu-id="34e76-141">Find and select the required shipment.</span></span>
1. <span data-ttu-id="34e76-142">Vaadake väljal **Saadetise konsolideerimispoliitika** üle saadetise loomisel kasutatud konsolideerimispoliitika.</span><span class="sxs-lookup"><span data-stu-id="34e76-142">In the **Shipment consolidation policy** field, review the consolidation policy that was used when the shipment was created.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34e76-143">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="34e76-143">Additional resources</span></span>

- [<span data-ttu-id="34e76-144">Saadetise konsolideerimispoliitikad</span><span class="sxs-lookup"><span data-stu-id="34e76-144">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="34e76-145">Saadetise konsolideerimispoliitikate konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="34e76-145">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
