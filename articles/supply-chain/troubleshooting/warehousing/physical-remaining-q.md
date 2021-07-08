---
title: Ühikus olev füüsiline jääkkogus ei tohi olla null
description: Saatelehe loomisel on sellele esitatud andmete laokogus nullist erinev, kuid müügikogus null.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248776"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a><span data-ttu-id="29497-103">Ühikus olev füüsiline jääkkogus ei tohi olla null</span><span class="sxs-lookup"><span data-stu-id="29497-103">Physical remaining quantity in the unit must not be zero</span></span>

<span data-ttu-id="29497-104">Tõrkekood: SYS19591</span><span class="sxs-lookup"><span data-stu-id="29497-104">Error code: SYS19591</span></span>

## <a name="symptoms"></a><span data-ttu-id="29497-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="29497-105">Symptoms</span></span>

<span data-ttu-id="29497-106">Saatelehe loomisel on sellele esitatud andmete laokogus nullist erinev, kuid müügikogus null.</span><span class="sxs-lookup"><span data-stu-id="29497-106">When you generate a packing slip, the data that is supplied to it has a non-zero inventory quantity but a zero sales quantity.</span></span>

<span data-ttu-id="29497-107">Kui proovite pakendi silti genereerida, näitab süsteem järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="29497-107">When you try to generate the packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="29497-108">Füüsiliselt järelejääv kogus ühikus %1 peab nullist erinema.</span><span class="sxs-lookup"><span data-stu-id="29497-108">Physical remaining quantity in the unit %1 must be other than zero.</span></span>

<span data-ttu-id="29497-109">Seega ei saa te koorma pakendi silti genereerida.</span><span class="sxs-lookup"><span data-stu-id="29497-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="29497-110">Põhjus</span><span class="sxs-lookup"><span data-stu-id="29497-110">Cause</span></span>

<span data-ttu-id="29497-111">Süsteem hindab inventuuriühiku füüsilist jääkkogust ja saatmisühikus järelejäänud füüsilist kogust.</span><span class="sxs-lookup"><span data-stu-id="29497-111">The system evaluates the physical remaining quantity in the inventory unit and the physical remaining quantity in the shipping unit.</span></span> <span data-ttu-id="29497-112">Kui süsteem leiab, et saatmisühiku füüsiline jääkkogus on 0 (null), kuid füüsiline jääk laoühikus pole 0, ei saa te saatelehte luua.</span><span class="sxs-lookup"><span data-stu-id="29497-112">If the system finds that the physical remaining quantity in the shipping unit is 0 (zero), but the physical remaining quantity in the inventory unit isn't 0, you can't generate the packing slip.</span></span> <span data-ttu-id="29497-113">See probleem võib ilmneda näiteks juhul, kui kauba müügiühik ja laoühik erinevad ning ühikutevaheline teisendamine pole täpne.</span><span class="sxs-lookup"><span data-stu-id="29497-113">For example, this issue might occur if the sales unit and inventory unit for the item differ, and the conversion between units isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="29497-114">Lahendus</span><span class="sxs-lookup"><span data-stu-id="29497-114">Resolution</span></span>

<span data-ttu-id="29497-115">Koorem või saadetis on praegu olekus, kus saatekirja loomine nurjub.</span><span class="sxs-lookup"><span data-stu-id="29497-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="29497-116">Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:</span><span class="sxs-lookup"><span data-stu-id="29497-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="29497-117">Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.</span><span class="sxs-lookup"><span data-stu-id="29497-117">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="29497-118">Vaadake üle oma koormusread ja tehke kohandusi tagamaks, et kogust saab puhtalt teisendada ilma ümardamisprobleemideta.</span><span class="sxs-lookup"><span data-stu-id="29497-118">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>
- <span data-ttu-id="29497-119">Vaadake üle oma koormusread ja tehke kohandused, et tagada ühiku ja koguse teisendus kümnendtäpsusega.</span><span class="sxs-lookup"><span data-stu-id="29497-119">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>
- <span data-ttu-id="29497-120">Veenduge, et lao mõõtühik oleks müügi mõõtühikust väiksem.</span><span class="sxs-lookup"><span data-stu-id="29497-120">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="29497-121">Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid</span><span class="sxs-lookup"><span data-stu-id="29497-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="29497-122">Kasutage ülevaatuseks järgmist protseduuri ja vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.</span><span class="sxs-lookup"><span data-stu-id="29497-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="29497-123">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="29497-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="29497-124">Valige koorem, mille jaoks ei saa saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="29497-124">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="29497-125">Valige kiirkaardil **Koormaread** koormarida.</span><span class="sxs-lookup"><span data-stu-id="29497-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="29497-126">Tehke märge väärtuse kohta väljal **Loodud töö kogus**.</span><span class="sxs-lookup"><span data-stu-id="29497-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="29497-127">Toimingupaani vahekaardil **Ladu** grupis **Seotud teave** valige **Töö**.</span><span class="sxs-lookup"><span data-stu-id="29497-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="29497-128">Kontrollige, kas töö on saadetise lõppsihtkohas lõpule viidud ja et komplekteeritud töökogus vastab loodud töö kogusele koormareal.</span><span class="sxs-lookup"><span data-stu-id="29497-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="29497-129">Korrake seda protseduuri kõigi koormaridade puhul, et veenduda kõigi kriteeriumide täitmises.</span><span class="sxs-lookup"><span data-stu-id="29497-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a><span data-ttu-id="29497-130">Vaadake üle oma koormusread ja tehke kohandusi tagamaks, et kogust saab puhtalt teisendada ilma ümardamisprobleemideta</span><span class="sxs-lookup"><span data-stu-id="29497-130">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues</span></span>

<span data-ttu-id="29497-131">Kasutage järgmist protseduuri, et vaadata üle oma koormusread ja tehke kohandusi tagamaks, et kogust saab puhtalt teisendada ilma ümardamisprobleemideta.</span><span class="sxs-lookup"><span data-stu-id="29497-131">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>

1. <span data-ttu-id="29497-132">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="29497-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="29497-133">Saate valida koormuse, mille jaoks saatelehte ei saa luua.</span><span class="sxs-lookup"><span data-stu-id="29497-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="29497-134">Valige toimingupaani vahekaardi  **Saatmine ja vastuvõtmine** jaotises  **Ümberpööramine** suvand  **Pööra saadetise kinnitus ümber**.</span><span class="sxs-lookup"><span data-stu-id="29497-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="29497-135">Valige vahekaardil  **Koormaread** koorma rida kauba jaoks, mis ületab ületarnet.</span><span class="sxs-lookup"><span data-stu-id="29497-135">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery.</span></span>
1. <span data-ttu-id="29497-136">Komplekteeritud koguse täpsustamiseks valige **Vähenda komplekteeritud kogust**.</span><span class="sxs-lookup"><span data-stu-id="29497-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="29497-137">Vahekaardil  **Liini detailid** valige **Tellimus**.</span><span class="sxs-lookup"><span data-stu-id="29497-137">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="29497-138">Seadke väljal **Kogus** väärtus komplekteeritud kogusele (st **Tööga loodud kogus** välja väärtusele), et saatelehe loomine saaks toimuda.</span><span class="sxs-lookup"><span data-stu-id="29497-138">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="29497-139">Vaadake üle oma koormusread ja tehke kohandused, et tagada ühiku ja koguse teisendus kümnendtäpsusega</span><span class="sxs-lookup"><span data-stu-id="29497-139">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="29497-140">Kasutage ülevaatuseks järgmist protseduuri ja vaadake üle oma koormusread ja tehke kohandused, et tagada ühiku ja koguse teisendus kümnendtäpsusega.</span><span class="sxs-lookup"><span data-stu-id="29497-140">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="29497-141">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="29497-141">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="29497-142">Saate valida koormuse, mille jaoks saatelehte ei saa luua.</span><span class="sxs-lookup"><span data-stu-id="29497-142">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="29497-143">Kiirkaardil **Koormusread** valige probleemi põhjustava üksuse koormusrida.</span><span class="sxs-lookup"><span data-stu-id="29497-143">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="29497-144">Tehke märge väärtuse kohta väljadel **Kogus** ja **Ühik**.</span><span class="sxs-lookup"><span data-stu-id="29497-144">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="29497-145">Avage **Organisatsiooni haldus \> Seadistus \> Ühikud**.</span><span class="sxs-lookup"><span data-stu-id="29497-145">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="29497-146">Saate valida ühiku, mille jaoks saatelehte ei saa luua.</span><span class="sxs-lookup"><span data-stu-id="29497-146">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="29497-147">Saate välja **Kümnendtäpsus** väärtust vastavalt vajadusele korrigeerida.</span><span class="sxs-lookup"><span data-stu-id="29497-147">Adjust the value of the **Decimal precision** field as required.</span></span>

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a><span data-ttu-id="29497-148">Veenduge, et lao mõõtühik oleks müügi mõõtühikust väiksem</span><span class="sxs-lookup"><span data-stu-id="29497-148">Make sure that the inventory unit of measure is smaller than the sales unit of measure</span></span>

<span data-ttu-id="29497-149">Veenduge, et lao mõõtühik oleks müügi mõõtühikust väiksem.</span><span class="sxs-lookup"><span data-stu-id="29497-149">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span> <span data-ttu-id="29497-150">Kaaluge kauba mõõtühiku ümberkonfigureerimine vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="29497-150">Consider reconfiguring the unit of measure for the item as required.</span></span>
