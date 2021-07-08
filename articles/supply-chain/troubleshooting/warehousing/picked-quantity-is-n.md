---
title: Komplekteeritud kogus pole saatelehe loomise ajal piisav
description: Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ei ühti koormusjoonel loodud töökogusega.
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
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249090"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a><span data-ttu-id="8da10-103">Komplekteeritud kogus pole saatelehe loomise ajal piisav</span><span class="sxs-lookup"><span data-stu-id="8da10-103">Picked quantity isn't sufficient during packing slip generation</span></span>

<span data-ttu-id="8da10-104">Tõrkekood: SYS54073</span><span class="sxs-lookup"><span data-stu-id="8da10-104">Error code: SYS54073</span></span>

## <a name="symptoms"></a><span data-ttu-id="8da10-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="8da10-105">Symptoms</span></span>

<span data-ttu-id="8da10-106">Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ei ühti koormusjoonel loodud töökogusega.</span><span class="sxs-lookup"><span data-stu-id="8da10-106">When you generate a packing slip, the outbound load contains a picked quantity that doesn't match the created work quantity on the load line.</span></span>

<span data-ttu-id="8da10-107">Kui proovite pakendi silti genereerida, näitab süsteem järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="8da10-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="8da10-108">Kuna %1 on komplekteeritud, ei piisa %2 uuendamisest, kui jääk peab olema %3.</span><span class="sxs-lookup"><span data-stu-id="8da10-108">As %1 have been picked, it is not sufficient to update %2, when, subsequently, the remainder must be %3.</span></span>

<span data-ttu-id="8da10-109">Seega ei saa te koorma pakendi silti genereerida.</span><span class="sxs-lookup"><span data-stu-id="8da10-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="8da10-110">Põhjus</span><span class="sxs-lookup"><span data-stu-id="8da10-110">Cause</span></span>

<span data-ttu-id="8da10-111">Saatelehte ei saa praeguses olekus genereerida, kuna võib esineda üht järgmistest tingimustest:</span><span class="sxs-lookup"><span data-stu-id="8da10-111">The packing slip can't be generated in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="8da10-112">Seotud tööd pole veel komplekteeritud ega teisaldatud saadetise lõppsihtkohta.</span><span class="sxs-lookup"><span data-stu-id="8da10-112">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="8da10-113">Komplekteeritud töö kogus ei vasta loodud töö kogusele koormareal.</span><span class="sxs-lookup"><span data-stu-id="8da10-113">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="8da10-114">Koormusjoone kogus, tööga loodud kogus ja valitud kogus ei ühti.</span><span class="sxs-lookup"><span data-stu-id="8da10-114">The load line quantity, work created quantity, and picked quantity don't match.</span></span>

## <a name="resolution"></a><span data-ttu-id="8da10-115">Lahendus</span><span class="sxs-lookup"><span data-stu-id="8da10-115">Resolution</span></span>

<span data-ttu-id="8da10-116">Koorem või saadetis on praegu olekus, kus saatekirja loomine nurjub.</span><span class="sxs-lookup"><span data-stu-id="8da10-116">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="8da10-117">Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:</span><span class="sxs-lookup"><span data-stu-id="8da10-117">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="8da10-118">Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.</span><span class="sxs-lookup"><span data-stu-id="8da10-118">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="8da10-119">Muutke laadimisliini kogust.</span><span class="sxs-lookup"><span data-stu-id="8da10-119">Adjust the load line quantity.</span></span>
- <span data-ttu-id="8da10-120">Tühistage kõik komplekteerimisregistreerimised ja tehke komplekteerimine uuesti.</span><span class="sxs-lookup"><span data-stu-id="8da10-120">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="8da10-121">Vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid</span><span class="sxs-lookup"><span data-stu-id="8da10-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="8da10-122">Kasutage ülevaatuseks järgmist protseduuri ja vaadake üle oma koormusjoones ja kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.</span><span class="sxs-lookup"><span data-stu-id="8da10-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="8da10-123">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="8da10-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="8da10-124">Saate valida koormuse, mille jaoks saatelehte ei saa luua.</span><span class="sxs-lookup"><span data-stu-id="8da10-124">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="8da10-125">Valige kiirkaardil **Koormaread** koormarida.</span><span class="sxs-lookup"><span data-stu-id="8da10-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="8da10-126">Tehke märge väärtuse kohta väljal **Loodud töö kogus**.</span><span class="sxs-lookup"><span data-stu-id="8da10-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="8da10-127">Toimingupaani vahekaardil **Ladu** grupis **Seotud teave** valige **Töö**.</span><span class="sxs-lookup"><span data-stu-id="8da10-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="8da10-128">Kontrollige, kas töö on saadetise lõppsihtkohas lõpule viidud ja et komplekteeritud töökogus vastab loodud töö kogusele koormareal.</span><span class="sxs-lookup"><span data-stu-id="8da10-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="8da10-129">Korrake seda protseduuri kõigi koormaridade puhul, et veenduda kõigi kriteeriumide täitmises.</span><span class="sxs-lookup"><span data-stu-id="8da10-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="8da10-130">Muutke laadimisliini kogust</span><span class="sxs-lookup"><span data-stu-id="8da10-130">Adjust the load line quantity</span></span>

<span data-ttu-id="8da10-131">Koormusrea koguse reguleerimiseks kasutage järgmist toimingut.</span><span class="sxs-lookup"><span data-stu-id="8da10-131">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="8da10-132">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="8da10-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="8da10-133">Saate valida koormuse, mille jaoks saatelehte ei saa luua.</span><span class="sxs-lookup"><span data-stu-id="8da10-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="8da10-134">Valige toimingupaani vahekaardi  **Saatmine ja vastuvõtmine** jaotises  **Ümberpööramine** suvand  **Pööra saadetise kinnitus ümber**.</span><span class="sxs-lookup"><span data-stu-id="8da10-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="8da10-135">Vahekaardil  **Koormusread** valige probleemi põhjustava üksuse koormusrida.</span><span class="sxs-lookup"><span data-stu-id="8da10-135">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="8da10-136">Komplekteeritud koguse täpsustamiseks valige **Vähenda komplekteeritud kogust**.</span><span class="sxs-lookup"><span data-stu-id="8da10-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="8da10-137">Seadistage väli **Koormarea vähendamine**, et kajastada koormusrea korrigeerimisi.</span><span class="sxs-lookup"><span data-stu-id="8da10-137">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="8da10-138">Tühistage kõik komplekteerimisregistreerimised ja tehke komplekteerimine uuesti</span><span class="sxs-lookup"><span data-stu-id="8da10-138">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="8da10-139">Probleem võib ilmneda, sest keegi kasutab koormuse rea sulgemiseks ilma tööta komplekteeritud registreerimist.</span><span class="sxs-lookup"><span data-stu-id="8da10-139">The issue might occur because someone used pick registration to close a load line without work.</span></span> <span data-ttu-id="8da10-140">Sel juhul tuleb käsitsi komplekteerimise registreerimine tühistada ja komplekteerimine tuleb seejärel Warehouse Management laohalduse mobiilirakenduse abil lõpetada.</span><span class="sxs-lookup"><span data-stu-id="8da10-140">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="8da10-141">Kasutage järgmist protseduuri komplekteeritud registreerimise tühistamiseks.</span><span class="sxs-lookup"><span data-stu-id="8da10-141">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="8da10-142">Avage jaotis **Müügireskontro \> Tellimused \> Kõik tellimused**.</span><span class="sxs-lookup"><span data-stu-id="8da10-142">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="8da10-143">Valige müügitellimus, millele ei saa koormuse jaoks saatelehte sisestada.</span><span class="sxs-lookup"><span data-stu-id="8da10-143">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="8da10-144">Vahekaardil  **Müügitellimuse read** valige müügitellimuse rida, mille jaoks registreerimine komplekteeritud oli.</span><span class="sxs-lookup"><span data-stu-id="8da10-144">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="8da10-145">Valige suvand **Uuenda rida \> Vali**, et kaupade komplekt eemaldada.</span><span class="sxs-lookup"><span data-stu-id="8da10-145">Select **Update line \> Pick** to unpick the items.</span></span>
