---
title: Kogus, mida proovite värskendada, ületab vastuvõetud/tarnitud kogust.
description: Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ületab müügitellimuse jaoks korjatud ja reserveeritud töökogust.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249091"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a><span data-ttu-id="bcb4c-103">Kogus, mida proovite värskendada, ületab vastuvõetud/tarnitud kogust</span><span class="sxs-lookup"><span data-stu-id="bcb4c-103">Quantity that you're trying to update exceeds the received/delivered quantity</span></span>

<span data-ttu-id="bcb4c-104">Tõrkekood: SYS7676</span><span class="sxs-lookup"><span data-stu-id="bcb4c-104">Error code: SYS7676</span></span>

## <a name="symptoms"></a><span data-ttu-id="bcb4c-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="bcb4c-105">Symptoms</span></span>

<span data-ttu-id="bcb4c-106">Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ületab müügitellimuse jaoks korjatud ja reserveeritud töökogust.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the work quantity that was picked and reserved for the sales order.</span></span>

<span data-ttu-id="bcb4c-107">Kui proovite pakendi silti genereerida, näitab süsteem järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="bcb4c-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="bcb4c-108">Kogus, mida püüate värskendada, ületab saadud või tarnitud koguse.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-108">The quantity that you are trying to update exceeds the quantity received/delivered.</span></span>

<span data-ttu-id="bcb4c-109">Seega ei saa te koorma pakendi silti genereerida.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="bcb4c-110">Põhjus</span><span class="sxs-lookup"><span data-stu-id="bcb4c-110">Cause</span></span>

<span data-ttu-id="bcb4c-111">Komplekteeritud töö kogus ei vasta loodud töö kogusele koormareal.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-111">The picked work quantity doesn't match the created work quantity on the load line.</span></span> <span data-ttu-id="bcb4c-112">Näiteks võib see probleem ilmneda, kui koormarea kogus, tööga loodud kogus või komplekteeritud kogus ei ole täpne.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-112">For example, this issue might occur if the load line quantity, work created quantity, or picked quantity isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="bcb4c-113">Lahendus</span><span class="sxs-lookup"><span data-stu-id="bcb4c-113">Resolution</span></span>

<span data-ttu-id="bcb4c-114">Koorem või saadetis on praegu olekus, kus saatekirja loomine nurjub.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-114">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="bcb4c-115">Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:</span><span class="sxs-lookup"><span data-stu-id="bcb4c-115">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="bcb4c-116">Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-116">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="bcb4c-117">Muutke laadimisliini kogust.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-117">Adjust the load line quantity.</span></span>
- <span data-ttu-id="bcb4c-118">Tühistage kõik komplekteerimisregistreerimised ja tehke komplekteerimine uuesti.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-118">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="bcb4c-119">Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid</span><span class="sxs-lookup"><span data-stu-id="bcb4c-119">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="bcb4c-120">Kasutage ülevaatuseks järgmist protseduuri ja vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="bcb4c-121">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="bcb4c-122">Valige koorem, mille jaoks ei saa saadetist luua.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-122">Select the load that the shipment can't be generated for.</span></span>
1. <span data-ttu-id="bcb4c-123">Valige kiirkaardil **Koormaread** koormarida.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="bcb4c-124">Tehke märge väärtuse kohta väljal **Loodud töö kogus**.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="bcb4c-125">Toimingupaani vahekaardil **Ladu** grupis **Seotud teave** valige **Töö**.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="bcb4c-126">Kontrollige, kas töö on saadetise lõppsihtkohas lõpule viidud ja et komplekteeritud töökogus vastab loodud töö kogusele koormareal.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="bcb4c-127">Korrake seda protseduuri kõigi koormaridade puhul, et veenduda kõigi kriteeriumide täitmises.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="bcb4c-128">Muutke laadimisliini kogust</span><span class="sxs-lookup"><span data-stu-id="bcb4c-128">Adjust the load line quantity</span></span>

<span data-ttu-id="bcb4c-129">Koormusrea koguse reguleerimiseks kasutage järgmist toimingut.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-129">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="bcb4c-130">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="bcb4c-131">Saate valida koormuse, mille jaoks saatelehte ei saa luua.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="bcb4c-132">Valige toimingupaani vahekaardi  **Saatmine ja vastuvõtmine** jaotises  **Ümberpööramine** suvand  **Pööra saadetise kinnitus ümber**.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-132">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="bcb4c-133">Vahekaardil  **Koormusread** valige probleemi põhjustava üksuse koormusrida.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-133">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="bcb4c-134">Komplekteeritud koguse täpsustamiseks valige **Vähenda komplekteeritud kogust**.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-134">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="bcb4c-135">Seadistage väli **Koormarea vähendamine**, et kajastada koormusrea korrigeerimisi.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-135">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="bcb4c-136">Tühistage kõik komplekteerimisregistreerimised ja tehke komplekteerimine uuesti</span><span class="sxs-lookup"><span data-stu-id="bcb4c-136">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="bcb4c-137">Kui keegi kasutab registreerimise noppimist koormarea sulgemiseks ilma tööta, võib esineda lahknevust koormarea koguse ja komplekteeritud koguse vahel.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-137">If someone used pick registration to close a load line without work, a discrepancy can occur between the load line quantity and the picked quantity.</span></span> <span data-ttu-id="bcb4c-138">Sel juhul tuleb käsitsi komplekteerimise registreerimine tühistada ja komplekteerimine tuleb seejärel Warehouse Management laohalduse mobiilirakenduse abil lõpetada.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-138">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="bcb4c-139">Kasutage järgmist protseduuri komplekteeritud registreerimise tühistamiseks.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-139">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="bcb4c-140">Avage jaotis **Müügireskontro \> Tellimused \> Kõik tellimused**.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-140">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="bcb4c-141">Valige müügitellimus, millele ei saa koormuse jaoks saatelehte sisestada.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-141">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="bcb4c-142">Vahekaardil  **Müügitellimuse read** valige müügitellimuse rida, mille jaoks registreerimine komplekteeritud oli.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-142">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="bcb4c-143">Valige suvand **Uuenda rida \> Vali**, et kaupade komplekt eemaldada.</span><span class="sxs-lookup"><span data-stu-id="bcb4c-143">Select **Update line \> Pick** to unpick the items.</span></span>
