---
title: Füüsilise värskenduskoguse ümardamine kümnendkohtade kaupa on vale
description: Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ei vasta ühikus määratletud kümnendtäpsusele.
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
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248777"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a><span data-ttu-id="08ec0-103">Füüsilise värskenduskoguse ümardamine kümnendkohtade kaupa on vale</span><span class="sxs-lookup"><span data-stu-id="08ec0-103">Decimal rounding of the physical updating quantity is incorrect</span></span>

<span data-ttu-id="08ec0-104">Tõrkekood: SYS19589</span><span class="sxs-lookup"><span data-stu-id="08ec0-104">Error code: SYS19589</span></span>

## <a name="symptoms"></a><span data-ttu-id="08ec0-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="08ec0-105">Symptoms</span></span>

<span data-ttu-id="08ec0-106">Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ei vasta ühikus määratletud kümnendtäpsusele.</span><span class="sxs-lookup"><span data-stu-id="08ec0-106">When you generate a packing slip, the outbound load contains a quantity that doesn't match the decimal precision that is defined in the unit.</span></span>

<span data-ttu-id="08ec0-107">Kui proovite pakendi silti genereerida, näitab süsteem järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="08ec0-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="08ec0-108">Füüsilise sisestamiskoguse kümnendkoha ümardamine ühikus %1 on vale.</span><span class="sxs-lookup"><span data-stu-id="08ec0-108">Decimal rounding of the physical updating quantity in the unit %1 is incorrect.</span></span>

<span data-ttu-id="08ec0-109">Seega ei saa te koorma pakendi silti genereerida.</span><span class="sxs-lookup"><span data-stu-id="08ec0-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="08ec0-110">Põhjus</span><span class="sxs-lookup"><span data-stu-id="08ec0-110">Cause</span></span>

<span data-ttu-id="08ec0-111">Süsteem hindab, kas lähetuskoguse kümnendkohtade ümardamine vastab saatmisühiku jaoks määratletud kümnendtäpsusele.</span><span class="sxs-lookup"><span data-stu-id="08ec0-111">The system evaluates whether the decimal rounding of the shipping quantity corresponds to the decimal precision that is defined for the shipping unit.</span></span> <span data-ttu-id="08ec0-112">Kui süsteem ümardab lähetuskoguse määratud kümnendkohtade leitud arvuni ja kui ümardatud lähetuskogus ei vasta tegelikule lähetuskogusele, ei saa te saatelehte luua.</span><span class="sxs-lookup"><span data-stu-id="08ec0-112">When the system rounds the shipping quantity to the specified number of decimal places, if it finds that the rounded shipping quantity doesn't match the actual shipping quantity, you can't generate the packing slip.</span></span> <span data-ttu-id="08ec0-113">See probleem võib ilmneda näiteks juhul, kui müügikogus on 1,75 kilogrammi (kg), kuid kümnendtäpsuseks on seatud *1*.</span><span class="sxs-lookup"><span data-stu-id="08ec0-113">For example, this issue might occur if the sales quantity is 1.75 kilograms (kg), but the decimal precision is set to *1*.</span></span>

## <a name="resolution"></a><span data-ttu-id="08ec0-114">Lahendus</span><span class="sxs-lookup"><span data-stu-id="08ec0-114">Resolution</span></span>

<span data-ttu-id="08ec0-115">Koorem või saadetis on praegu olekus, kus saatekirja loomine nurjub.</span><span class="sxs-lookup"><span data-stu-id="08ec0-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="08ec0-116">Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:</span><span class="sxs-lookup"><span data-stu-id="08ec0-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="08ec0-117">Vaadake üle oma koormusread ja tehke kohandusi tagamaks, et kogust saab puhtalt teisendada ilma kümnendkohtade ja muude ümardamisprobleemideta.</span><span class="sxs-lookup"><span data-stu-id="08ec0-117">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>
- <span data-ttu-id="08ec0-118">Vaadake üle oma koormusread ja tehke kohandused, et tagada ühiku ja koguse teisendus kümnendtäpsusega.</span><span class="sxs-lookup"><span data-stu-id="08ec0-118">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a><span data-ttu-id="08ec0-119">Vaadake üle oma koormusread ja tehke kohandusi tagamaks, et kogust saab puhtalt teisendada ilma kümnendkohtade ja muude ümardamisprobleemideta</span><span class="sxs-lookup"><span data-stu-id="08ec0-119">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues</span></span>

<span data-ttu-id="08ec0-120">Kasutage järgmist protseduuri, et vaadata üle oma koormusread ja tehke kohandusi tagamaks, et kogust saab puhtalt teisendada ilma kümnendkohtade ja muude ümardamisprobleemideta.</span><span class="sxs-lookup"><span data-stu-id="08ec0-120">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>

1. <span data-ttu-id="08ec0-121">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="08ec0-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="08ec0-122">Saate valida koormuse, mille jaoks saatelehte ei saa luua.</span><span class="sxs-lookup"><span data-stu-id="08ec0-122">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="08ec0-123">Valige toimingupaani vahekaardi  **Saatmine ja vastuvõtmine** jaotises  **Ümberpööramine** suvand  **Pööra saadetise kinnitus ümber**.</span><span class="sxs-lookup"><span data-stu-id="08ec0-123">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="08ec0-124">Vahekaardil  **Koormusread** valige probleemi põhjustava üksuse koormusrida.</span><span class="sxs-lookup"><span data-stu-id="08ec0-124">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="08ec0-125">Komplekteeritud koguse täpsustamiseks valige **Vähenda komplekteeritud kogust**.</span><span class="sxs-lookup"><span data-stu-id="08ec0-125">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="08ec0-126">Vahekaardil  **Liini detailid** valige **Tellimus**.</span><span class="sxs-lookup"><span data-stu-id="08ec0-126">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="08ec0-127">Seadke väljal **Kogus** väärtus komplekteeritud kogusele (st **Tööga loodud kogus** välja väärtusele), et saatelehe loomine saaks toimuda.</span><span class="sxs-lookup"><span data-stu-id="08ec0-127">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="08ec0-128">Vaadake üle oma koormusread ja tehke kohandused, et tagada ühiku ja koguse teisendus kümnendtäpsusega</span><span class="sxs-lookup"><span data-stu-id="08ec0-128">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="08ec0-129">Kasutage ülevaatuseks järgmist protseduuri ja vaadake üle oma koormusread ja tehke kohandused, et tagada ühiku ja koguse teisendus kümnendtäpsusega.</span><span class="sxs-lookup"><span data-stu-id="08ec0-129">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="08ec0-130">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="08ec0-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="08ec0-131">Saate valida koormuse, mille jaoks saatelehte ei saa luua.</span><span class="sxs-lookup"><span data-stu-id="08ec0-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="08ec0-132">Kiirkaardil **Koormusread** valige probleemi põhjustava üksuse koormusrida.</span><span class="sxs-lookup"><span data-stu-id="08ec0-132">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="08ec0-133">Tehke märge väärtuse kohta väljadel **Kogus** ja **Ühik**.</span><span class="sxs-lookup"><span data-stu-id="08ec0-133">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="08ec0-134">Avage **Organisatsiooni haldus \> Seadistus \> Ühikud**.</span><span class="sxs-lookup"><span data-stu-id="08ec0-134">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="08ec0-135">Saate valida ühiku, mille jaoks saatelehte ei saa luua.</span><span class="sxs-lookup"><span data-stu-id="08ec0-135">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="08ec0-136">Saate välja **Kümnendtäpsus** väärtust vastavalt vajadusele korrigeerida.</span><span class="sxs-lookup"><span data-stu-id="08ec0-136">Adjust the value of the **Decimal precision** field as required.</span></span>
