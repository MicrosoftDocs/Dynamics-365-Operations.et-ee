---
title: Kogus ületab saatelehe loomise ajal ületarne protsendi
description: Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ületab ületarne protsendi.
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
ms.openlocfilehash: 1106322cc3772c1b671b7fa82fb74039c028ba35
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249088"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="c1239-103">Kogus ületab saatelehe loomise ajal ületarne protsendi</span><span class="sxs-lookup"><span data-stu-id="c1239-103">Quantity exceeds over-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="c1239-104">Tõrkekood: SYS24920</span><span class="sxs-lookup"><span data-stu-id="c1239-104">Error code: SYS24920</span></span>

## <a name="symptoms"></a><span data-ttu-id="c1239-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="c1239-105">Symptoms</span></span>

<span data-ttu-id="c1239-106">Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ületab ületarne protsendi.</span><span class="sxs-lookup"><span data-stu-id="c1239-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the over-delivery percentage.</span></span>

<span data-ttu-id="c1239-107">Kui proovite pakendi silti genereerida, näitab süsteem järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="c1239-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="c1239-108">Rea ületarne on %1 protsenti, kuid lubatud ületarne on ainult %2 protsenti.</span><span class="sxs-lookup"><span data-stu-id="c1239-108">Overdelivery of line is %1 percent, but the allowed overdelivery is only %2 percent.</span></span>

<span data-ttu-id="c1239-109">Seega ei saa te koorma pakendi silti genereerida.</span><span class="sxs-lookup"><span data-stu-id="c1239-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="c1239-110">Põhjus</span><span class="sxs-lookup"><span data-stu-id="c1239-110">Cause</span></span>

<span data-ttu-id="c1239-111">Koormuse või saadetise komplekteeritud kogus on tellitud kogusest suurem ja ei kuulu ületarne protsendi vahemikku.</span><span class="sxs-lookup"><span data-stu-id="c1239-111">The picked quantity for the load or shipment is more than the ordered quantity and isn't within the range of the over-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="c1239-112">Lahendus</span><span class="sxs-lookup"><span data-stu-id="c1239-112">Resolution</span></span>

<span data-ttu-id="c1239-113">Koorem või saadetis on praegu olekus, kus saatekirja loomine nurjub.</span><span class="sxs-lookup"><span data-stu-id="c1239-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="c1239-114">Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:</span><span class="sxs-lookup"><span data-stu-id="c1239-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="c1239-115">Muutke laadimisliini kogust.</span><span class="sxs-lookup"><span data-stu-id="c1239-115">Adjust the load line quantity.</span></span>
- <span data-ttu-id="c1239-116">Muutke ületarne protsendi.</span><span class="sxs-lookup"><span data-stu-id="c1239-116">Adjust the over-delivery percentage.</span></span>
- <span data-ttu-id="c1239-117">Pöörake ümber ja tehke kohandusi.</span><span class="sxs-lookup"><span data-stu-id="c1239-117">Reverse and make adjustments.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="c1239-118">Muutke laadimisliini kogust</span><span class="sxs-lookup"><span data-stu-id="c1239-118">Adjust the load line quantity</span></span>

<span data-ttu-id="c1239-119">Koormusrea koguse reguleerimiseks kasutage järgmist toimingut.</span><span class="sxs-lookup"><span data-stu-id="c1239-119">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="c1239-120">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="c1239-120">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c1239-121">Saate valida koormuse, mille jaoks saatelehte ei saa luua.</span><span class="sxs-lookup"><span data-stu-id="c1239-121">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="c1239-122">Valige toimingupaani vahekaardi  **Saatmine ja vastuvõtmine** jaotises  **Ümberpööramine** suvand  **Pööra saadetise kinnitus ümber**.</span><span class="sxs-lookup"><span data-stu-id="c1239-122">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="c1239-123">Valige vahekaardil  **Koormaread** koorma rida kauba jaoks, mis ületab ületarne protsent.</span><span class="sxs-lookup"><span data-stu-id="c1239-123">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="c1239-124">Komplekteeritud koguse täpsustamiseks valige **Vähenda komplekteeritud kogust**.</span><span class="sxs-lookup"><span data-stu-id="c1239-124">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="c1239-125">Vahekaardil  **Liini detailid** valige **Tellimus**.</span><span class="sxs-lookup"><span data-stu-id="c1239-125">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="c1239-126">Seadke väljal **Kogus** väärtus komplekteeritud kogusele (st **Tööga loodud kogus** välja väärtusele), et saatelehe loomine saaks toimuda.</span><span class="sxs-lookup"><span data-stu-id="c1239-126">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="adjust-the-over-delivery-percentage"></a><span data-ttu-id="c1239-127">Muutke ületarne protsendi</span><span class="sxs-lookup"><span data-stu-id="c1239-127">Adjust the over-delivery percentage</span></span>

<span data-ttu-id="c1239-128">Ületarne protsendi reguleerimiseks kasutage järgmist toimingut.</span><span class="sxs-lookup"><span data-stu-id="c1239-128">Use the following procedure to adjust the over-delivery percentage.</span></span>

1. <span data-ttu-id="c1239-129">Avage jaotis **Müügireskontro \> Tellimused \> Kõik tellimused**.</span><span class="sxs-lookup"><span data-stu-id="c1239-129">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="c1239-130">Valige müügitellimus, millele ei saa koormuse jaoks saatelehte sisestada.</span><span class="sxs-lookup"><span data-stu-id="c1239-130">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="c1239-131">Valige vahekaardil  **Müügitellimused** müügitellimuse rida kauba jaoks, mis ületab ületarne protsent.</span><span class="sxs-lookup"><span data-stu-id="c1239-131">On the **Sales order lines** tab, select the sales order line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="c1239-132">Vahekaardil  **Liini detailid** valige **Kohaletoimetamine**.</span><span class="sxs-lookup"><span data-stu-id="c1239-132">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="c1239-133">Seadke **Ületarne** väljal väärtus suuremale protsendile, mis rahuldab koorma koguse suhtes komplekteeritud kogust, nii et saatelehe loomine on võimalik.</span><span class="sxs-lookup"><span data-stu-id="c1239-133">Set the **Overdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="c1239-134">Pöörake ümber ja tehke kohandusi</span><span class="sxs-lookup"><span data-stu-id="c1239-134">Reverse and make adjustments</span></span>

<span data-ttu-id="c1239-135">Tühistage kõik koormuse jaoks sisestatud asjad (nt saateleht, lähetuskinnitus ja töö), tehke müügitellimuse täpsustused, väljastage tellimus uuesti lattu ja viige saatmisprotseduur lõpule.</span><span class="sxs-lookup"><span data-stu-id="c1239-135">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="c1239-136">Saatelehe tühistamiseks kasutage järgmist toimingut.</span><span class="sxs-lookup"><span data-stu-id="c1239-136">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="c1239-137">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="c1239-137">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c1239-138">Valige toimingupaani vahekaardi  **Saatmine ja vastuvõtmine** jaotises  **Ümberpööramine** suvand  **Tühista saatelehed**.</span><span class="sxs-lookup"><span data-stu-id="c1239-138">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="c1239-139">Saadetise kinnituse tühistamiseks kasutage järgmist toimingut.</span><span class="sxs-lookup"><span data-stu-id="c1239-139">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="c1239-140">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="c1239-140">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c1239-141">Valige toimingupaani vahekaardi  **Saatmine ja vastuvõtmine** jaotises  **Ümberpööramine** suvand  **Pööra saadetise kinnitus ümber**.</span><span class="sxs-lookup"><span data-stu-id="c1239-141">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="c1239-142">Töö pööramiseks tehke järgmised toimingud:</span><span class="sxs-lookup"><span data-stu-id="c1239-142">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="c1239-143">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="c1239-143">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c1239-144">Valige toimingupaani vahekaardil  **Koormused** grupis  **Töö** üksus  **Pöördtöö**.</span><span class="sxs-lookup"><span data-stu-id="c1239-144">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
