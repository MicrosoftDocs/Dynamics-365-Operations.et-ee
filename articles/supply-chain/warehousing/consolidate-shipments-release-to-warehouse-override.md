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
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 23379b76367336157edad1bf2e534bf0f10799cb
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383756"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a><span data-ttu-id="e487b-103">Saadetiste konsolideerimine, kui lehel Lattu väljastamine alistatakse saadetise konsolideerimispoliitika</span><span class="sxs-lookup"><span data-stu-id="e487b-103">Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e487b-104">Selles teemas kirjeldatakse stsenaariumi, kus tuleb vähemalt üks müügirida väljastada lattu käsitsi lehe **Lattu väljastamine** kaudu ja enne väljastamist alistada süsteemi määratletud saadetise konsolideerimispoliitika.</span><span class="sxs-lookup"><span data-stu-id="e487b-104">This topic presents a scenario where one or more sales lines must be manually released to the warehouse from the **Release to warehouse** page, and the system-defined shipment consolidation policy must be overridden before the release.</span></span> <span data-ttu-id="e487b-105">Saadetiste konsolideerimispoliitika alistamine võib olla nõutav, kui näiteks tellimus, mida tavaliselt ei konsolideerita avatud saadetistega, tuleb konsolideerida avatud saadetistega.</span><span class="sxs-lookup"><span data-stu-id="e487b-105">An override of the shipment consolidation policy might be required if, for example, an order that isn't usually consolidated with open shipments must be consolidated with open shipments.</span></span>

<span data-ttu-id="e487b-106">Selle stsenaariumi käigus loote müügitellimuste komplekti ja seejärel alistate vaikimisi saadetise konsolideerimispoliitika enne tellimuste lattu väljastamist.</span><span class="sxs-lookup"><span data-stu-id="e487b-106">During the scenario, you will create a set of sales orders and then override the default shipment consolidation policy before you release the orders to the warehouse.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="e487b-107">Demoandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="e487b-107">Make demo data available</span></span>

<span data-ttu-id="e487b-108">Selle teema stsenaarium viitab väärtustele ja kirjetele, mis kuuluvad Microsoft Dynamics 365 Supply Chain Managementile esitatud standardsete demoandmete hulka.</span><span class="sxs-lookup"><span data-stu-id="e487b-108">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e487b-109">Kui soovite kasutada siin esitatud väärtusi harjutuste tegemise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks **USMF**.</span><span class="sxs-lookup"><span data-stu-id="e487b-109">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="e487b-110">Saadetise konsolideerimispoliitikate ja tootefiltrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="e487b-110">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="e487b-111">Siin kirjeldatud stsenaarium eeldab, et olete juba funktsiooni sisse lülitanud, sooritanud [saadetise konsolideerimispoliitikate konfigureerimise](configure-shipment-consolidation-policies.md) harjutused ning loonud poliitikad ja muud seal kirjeldatud kirjed.</span><span class="sxs-lookup"><span data-stu-id="e487b-111">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="e487b-112">Veenduge, et olete enne selle stsenaariumi jätkamist sooritanud need harjutused.</span><span class="sxs-lookup"><span data-stu-id="e487b-112">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="e487b-113">Müügitellimuste loomine selle stsenaariumi jaoks</span><span class="sxs-lookup"><span data-stu-id="e487b-113">Create the sales orders for this scenario</span></span>

1. <span data-ttu-id="e487b-114">Avage jaotis **Müügireskontro \> Tellimused \> Kõik müügitellimused** ja looge kolm identset müügitellimust, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="e487b-114">Go to **Accounts receivable \> Orders \> All sales orders**, and create three identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="e487b-115">**Kliendi konto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="e487b-115">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="e487b-116">Lisage järgmiste sätetega tellimuserida.</span><span class="sxs-lookup"><span data-stu-id="e487b-116">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="e487b-117">**Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)</span><span class="sxs-lookup"><span data-stu-id="e487b-117">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="e487b-118">**Kogus:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="e487b-118">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="e487b-119">Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="e487b-119">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a><span data-ttu-id="e487b-120">Müügitellimuste väljastamine lehelt Lattu väljastamine</span><span class="sxs-lookup"><span data-stu-id="e487b-120">Release the sales orders from the Release to warehouse page</span></span>

<span data-ttu-id="e487b-121">Järgige neid juhiseid saadetise konsolideerimispoliitika alistamiseks lattu väljastamise ajal.</span><span class="sxs-lookup"><span data-stu-id="e487b-121">Follow these steps to override the shipment consolidation policy during the release to the warehouse.</span></span>

1. <span data-ttu-id="e487b-122">Avage jaotis **Laohaldus \> Lattu väljastamine \> Lattu väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="e487b-122">Go to **Warehouse management \> Release to warehouse \> Release to warehouse**.</span></span>
1. <span data-ttu-id="e487b-123">Valige ülemisel paanil esimene selle stsenaariumi jaoks loodud müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="e487b-123">In the upper pane, select the first sales order that you created for this scenario.</span></span>
1. <span data-ttu-id="e487b-124">Valige **Lisa**, et lisada rida lattu väljastamisele.</span><span class="sxs-lookup"><span data-stu-id="e487b-124">Select **Add** to add the line to the release to the warehouse.</span></span> <span data-ttu-id="e487b-125">Pange tähele, et *Vaikimisi* saadetise konsolideerimispoliitika rakendatakse alumisel paanil.</span><span class="sxs-lookup"><span data-stu-id="e487b-125">Notice that the *Default* shipment consolidation policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="e487b-126">Valige alumisel paanil **Uue saadetise konsolideerimispoliitika valimine**.</span><span class="sxs-lookup"><span data-stu-id="e487b-126">In the bottom pane, select **Select new shipment consolidation policy**.</span></span>
1. <span data-ttu-id="e487b-127">Valige poliitika, mis lubab sama poliitika teiste avatud saadetiste konsolideerimist.</span><span class="sxs-lookup"><span data-stu-id="e487b-127">Select a policy that allows for consolidation with other open shipments of the same policy.</span></span> <span data-ttu-id="e487b-128">Valige näiteks poliitika *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="e487b-128">For example, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="e487b-129">Valige **Lattu väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="e487b-129">Select **Release to warehouse**.</span></span>
1. <span data-ttu-id="e487b-130">Valige selle stsenaariumi jaoks loodud teine ja kolmas müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="e487b-130">Select the second and third sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="e487b-131">Valige **Lisa**, et lisada read lattu väljastamisele.</span><span class="sxs-lookup"><span data-stu-id="e487b-131">Select **Add** to add the lines to the release to the warehouse.</span></span> <span data-ttu-id="e487b-132">Pange tähele, et *Vaikimisi* poliitika rakendatakse alumisel paanil.</span><span class="sxs-lookup"><span data-stu-id="e487b-132">Notice that the *Default* policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="e487b-133">Valige teine rida ja seejärel valige väljal **Uue saadetise konsolideerimispoliitika valimine** poliitika *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="e487b-133">Select the second line, and then, in the **Select new shipment consolidation policy** field, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="e487b-134">Valige mõlemal real **Lattu väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="e487b-134">Select **Release to warehouse** for both lines.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="e487b-135">Saadetiste kontrollimine</span><span class="sxs-lookup"><span data-stu-id="e487b-135">Verify the shipments</span></span>

<span data-ttu-id="e487b-136">Kaks saadetist peaks olema loodud.</span><span class="sxs-lookup"><span data-stu-id="e487b-136">Two shipments should have been created:</span></span>

- <span data-ttu-id="e487b-137">Esimene saadetis sisaldab kahte rida ja loodi saadetise konsolideerimispoliitika *CustomerOrderNo* abil.</span><span class="sxs-lookup"><span data-stu-id="e487b-137">The first shipment contains two lines and was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>
- <span data-ttu-id="e487b-138">Teine saadetis sisaldab ühte rida ja loodi saadetise konsolideerimispoliitika *Vaikimisi* abil.</span><span class="sxs-lookup"><span data-stu-id="e487b-138">The second shipment contains one line and was created by using the *Default* shipment consolidation policy.</span></span>

<span data-ttu-id="e487b-139">Loodud saadetiste ülevaatamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="e487b-139">Follow these steps to review the shipments that were created.</span></span>

1. <span data-ttu-id="e487b-140">Avage **Laohaldus \> Saadetised \> Kõik saadetised**.</span><span class="sxs-lookup"><span data-stu-id="e487b-140">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="e487b-141">Otsige üles ja valige nõutav saadetis.</span><span class="sxs-lookup"><span data-stu-id="e487b-141">Find and select the required shipment.</span></span>
1. <span data-ttu-id="e487b-142">Vaadake väljal **Saadetise konsolideerimispoliitika** üle saadetise loomisel kasutatud konsolideerimispoliitika.</span><span class="sxs-lookup"><span data-stu-id="e487b-142">In the **Shipment consolidation policy** field, review the consolidation policy that was used when the shipment was created.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e487b-143">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e487b-143">Additional resources</span></span>

- [<span data-ttu-id="e487b-144">Saadetise konsolideerimispoliitikad</span><span class="sxs-lookup"><span data-stu-id="e487b-144">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="e487b-145">Saadetise konsolideerimispoliitikate konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e487b-145">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
