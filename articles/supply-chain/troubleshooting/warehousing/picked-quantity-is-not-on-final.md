---
title: Saadetist ei saa kinnitada, kuna kaubad pole komplekteeritud
description: Saadetist ei saa kinnitada, kuna kaubad pole komplekteeritud
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301301"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="dfa86-103">Saadetist ei saa kinnitada, kuna kaubad pole komplekteeritud</span><span class="sxs-lookup"><span data-stu-id="dfa86-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="dfa86-104">Tõrkekood: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="dfa86-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="dfa86-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="dfa86-105">Symptoms</span></span>

<span data-ttu-id="dfa86-106">Kui proovite saadetist kinnitada, näitab süsteem järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="dfa86-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="dfa86-107">Mõni koorma %1 jaoks vajalik kaup pole veel komplekteeritud ja saadetise lõppsihtkohta teisaldatud.</span><span class="sxs-lookup"><span data-stu-id="dfa86-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="dfa86-108">Seega ei saa te koorma saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="dfa86-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="dfa86-109">Põhjus</span><span class="sxs-lookup"><span data-stu-id="dfa86-109">Cause</span></span>

<span data-ttu-id="dfa86-110">Koormat või saadetist ei saa praeguses olekus kinnitada, kuna võib esineda üht järgmistest tingimustest:</span><span class="sxs-lookup"><span data-stu-id="dfa86-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="dfa86-111">Seotud tööd pole veel komplekteeritud ega teisaldatud saadetise lõppsihtkohta.</span><span class="sxs-lookup"><span data-stu-id="dfa86-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="dfa86-112">Komplekteeritud töö kogus ei vasta loodud töö kogusele koormareal.</span><span class="sxs-lookup"><span data-stu-id="dfa86-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="dfa86-113">Asukoha direktiiv on konfigureeritud pakkimisasukohaga kui saadetise lõppsihtkohaks, kasutades voomalli konteinerit.</span><span class="sxs-lookup"><span data-stu-id="dfa86-113">The location directive has been configured with packing location as the final shipping location while using Wave template containerization.</span></span>

## <a name="resolution"></a><span data-ttu-id="dfa86-114">Lahendus</span><span class="sxs-lookup"><span data-stu-id="dfa86-114">Resolution</span></span>

<span data-ttu-id="dfa86-115">Koorem või saadetis on praegu olekus, kus saadetise kinnitamine nurjub.</span><span class="sxs-lookup"><span data-stu-id="dfa86-115">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="dfa86-116">Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:</span><span class="sxs-lookup"><span data-stu-id="dfa86-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="dfa86-117">Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.</span><span class="sxs-lookup"><span data-stu-id="dfa86-117">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="dfa86-118">Tühistage pakkimisasukohaga loodud töö ID-d saadetise lõppsihtkohana, konfigureerige asukohadirektiivi ümber ja väljastage koorem uuesti.</span><span class="sxs-lookup"><span data-stu-id="dfa86-118">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="dfa86-119">Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid</span><span class="sxs-lookup"><span data-stu-id="dfa86-119">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="dfa86-120">Kasutage ülevaatuseks järgmist protseduuri ja vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.</span><span class="sxs-lookup"><span data-stu-id="dfa86-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="dfa86-121">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="dfa86-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="dfa86-122">Valige koorem, mille jaoks ei saa saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="dfa86-122">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="dfa86-123">Valige kiirkaardil **Koormaread** koormarida.</span><span class="sxs-lookup"><span data-stu-id="dfa86-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="dfa86-124">Tehke märge väärtuse kohta väljal **Loodud töö kogus**.</span><span class="sxs-lookup"><span data-stu-id="dfa86-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="dfa86-125">Toimingupaani vahekaardil **Ladu** grupis **Seotud teave** valige **Töö**.</span><span class="sxs-lookup"><span data-stu-id="dfa86-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="dfa86-126">Kontrollige, kas töö on saadetise lõppsihtkohas lõpule viidud ja et komplekteeritud töökogus vastab loodud töö kogusele koormareal.</span><span class="sxs-lookup"><span data-stu-id="dfa86-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="dfa86-127">Korrake seda protseduuri kõigi koormaridade puhul, et veenduda kõigi kriteeriumide täitmises.</span><span class="sxs-lookup"><span data-stu-id="dfa86-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a><span data-ttu-id="dfa86-128">Tühistage pakkimisasukohaga loodud töö ID-d saadetise lõppsihtkohana, konfigureerige asukohadirektiivi ümber ja väljastage koorem uuesti</span><span class="sxs-lookup"><span data-stu-id="dfa86-128">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load</span></span>

<span data-ttu-id="dfa86-129">Kasutage järgmist protseduuri, et tühistada töö ID-d, mille pakkimise asukoht on lõplik maha panemise asukoht koos automaatse konteinerite paigutamisega.</span><span class="sxs-lookup"><span data-stu-id="dfa86-129">Use the following procedure to cancel the work IDs that have the packing location as the final put location with automated containerization in place.</span></span>

1. <span data-ttu-id="dfa86-130">Minge **Laohalduse \> Perioodiliste ülesannete juurde \> Puhastamine \>Tühista töö**.</span><span class="sxs-lookup"><span data-stu-id="dfa86-130">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="dfa86-131">Avaneb dialoog **Tühista töö**.</span><span class="sxs-lookup"><span data-stu-id="dfa86-131">The **Cancel work** dialog opens.</span></span> <span data-ttu-id="dfa86-132">Väljal **Töö ID** määrake töö ID, mida soovite tühistada.</span><span class="sxs-lookup"><span data-stu-id="dfa86-132">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span> <span data-ttu-id="dfa86-133">Valitud töö ID **töö oleku** väärtus peab olema *Avatud*, *Pooleli*, *Tühistatud*, *Kombineeritud* või *Suletud*.</span><span class="sxs-lookup"><span data-stu-id="dfa86-133">The selected work ID must have a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="dfa86-134">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfa86-134">Select **OK**.</span></span>
1. <span data-ttu-id="dfa86-135">Valige **Jah**, et kinnitada, et soovite töö tühistada.</span><span class="sxs-lookup"><span data-stu-id="dfa86-135">Select **Yes** to confirm that you want to cancel the work.</span></span>
1. <span data-ttu-id="dfa86-136">Korrake seda protseduuri muude töö ID-de puhul vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="dfa86-136">Repeat this procedure for the other work IDs as needed.</span></span>

<span data-ttu-id="dfa86-137">Lisateabe saamiseks vt [Erandite töötlemise laotöö tühistamine](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="dfa86-137">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

<span data-ttu-id="dfa86-138">Kasutage asukohadirektiivi ümber konfigureerimiseks järgmist protseduuri, et see ei kasutaks voomalli automatiseeritud konteinerite konfigureerimise korral pakkimisasukohta lõppsihtkohana.</span><span class="sxs-lookup"><span data-stu-id="dfa86-138">Use the following procedure to reconfigure the location directive so it won't use the packing location as the final shipping location when automated containerization is set up for the wave template.</span></span>

1. <span data-ttu-id="dfa86-139">Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.</span><span class="sxs-lookup"><span data-stu-id="dfa86-139">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="dfa86-140">Valige väljal **Töökäsu tüüp** suvand *Müügitellimused*.</span><span class="sxs-lookup"><span data-stu-id="dfa86-140">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="dfa86-141">Valige asukohadirektiivid, mida kasutate konteinerite määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="dfa86-141">Select the location directive you are using for automated containerization.</span></span>
1. <span data-ttu-id="dfa86-142">Valige kiirkaardi tööriistaribal **Asukohakorralduse tegevused** suvand **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="dfa86-142">On the **Location Directive Actions** FastTab toolbar, select **Edit query**.</span></span>
1. <span data-ttu-id="dfa86-143">Päringu redaktori dialoogis leidke vahekaardil **Vahemik** rida, kus **Väli** on seatud *asukohaprofiilile*, ja veenduge, et rea väli **Kriteerium** ei ole seadistatud asukohaprofiilile, mille **asukohatüüp** on *Pakkimine*.</span><span class="sxs-lookup"><span data-stu-id="dfa86-143">In the query editor dialog, on the **Range** tab, find the row where **Field** is set to *Location profile*, and verify that the **Criteria** field for that row is not set to a location profile that has a **Location type** of *Packing*.</span></span> <span data-ttu-id="dfa86-144">Korrigeerige välja **Kriteerium**, et parandada lõplik maha panemise asukoht.</span><span class="sxs-lookup"><span data-stu-id="dfa86-144">Adjust the **Criteria** field to correct the final put location.</span></span>

<span data-ttu-id="dfa86-145">Kasutage järgmist protseduuri, et taas väljastada koorem ja luua õige saadetise sihtkohaga töö ID-d.</span><span class="sxs-lookup"><span data-stu-id="dfa86-145">Use the following procedure to rerelease the load and create work IDs with the correct final shipping location.</span></span>

1. <span data-ttu-id="dfa86-146">Avage **Laohaldus \> Koormused \> Koormuse plaanimise töölaud**.</span><span class="sxs-lookup"><span data-stu-id="dfa86-146">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="dfa86-147">Leidke jaotises **Koormad** koorem, mis tuleb vabastada.</span><span class="sxs-lookup"><span data-stu-id="dfa86-147">In the **Loads** section, find the load that needs to be released.</span></span>
1. <span data-ttu-id="dfa86-148">Valige jaotise **Koormused** tööriistaribal koormuse lattu väljastamiseks **Väljasta \> Lattu väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="dfa86-148">On the **Loads** section toolbar, select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="dfa86-149">Korrake seda protseduuri muude koormuste puhul vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="dfa86-149">Repeat this procedure for the other loads as needed.</span></span>
