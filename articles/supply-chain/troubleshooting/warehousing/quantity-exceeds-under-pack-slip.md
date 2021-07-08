---
title: Kogus ületab saatelehe loomise ajal alatarne protsendi
description: Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ületab alatarne protsendi.
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
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249086"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="6b60c-103">Kogus ületab saatelehe loomise ajal alatarne protsendi</span><span class="sxs-lookup"><span data-stu-id="6b60c-103">Quantity exceeds under-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="6b60c-104">Tõrkekood: SYS24921</span><span class="sxs-lookup"><span data-stu-id="6b60c-104">Error code: SYS24921</span></span>

## <a name="symptoms"></a><span data-ttu-id="6b60c-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="6b60c-105">Symptoms</span></span>

<span data-ttu-id="6b60c-106">Saatelehe loomisel sisaldab väljaminev koormus kogust, mis ületab alatarne protsendi.</span><span class="sxs-lookup"><span data-stu-id="6b60c-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the under-delivery percentage.</span></span>

<span data-ttu-id="6b60c-107">Kui proovite pakendi silti genereerida, näitab süsteem järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="6b60c-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="6b60c-108">Rea alatarne on %1 protsenti, kuid lubatud alatarne on ainult %2 protsenti.</span><span class="sxs-lookup"><span data-stu-id="6b60c-108">Underdelivery of line is %1 percent, but the allowed underdelivery is only %2 percent.</span></span>

<span data-ttu-id="6b60c-109">Seega ei saa te koorma pakendi silti genereerida.</span><span class="sxs-lookup"><span data-stu-id="6b60c-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="6b60c-110">Põhjus</span><span class="sxs-lookup"><span data-stu-id="6b60c-110">Cause</span></span>

<span data-ttu-id="6b60c-111">Koormuse või saadetise komplekteeritud kogus on tellitud kogusest väiksem ja ei kuulu alatarne protsendi vahemikku.</span><span class="sxs-lookup"><span data-stu-id="6b60c-111">The picked quantity for the load or shipment is less than the ordered quantity and isn't within the range of the under-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="6b60c-112">Lahendus</span><span class="sxs-lookup"><span data-stu-id="6b60c-112">Resolution</span></span>

<span data-ttu-id="6b60c-113">Koorem või saadetis on praegu olekus, kus saatekirja loomine nurjub.</span><span class="sxs-lookup"><span data-stu-id="6b60c-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="6b60c-114">Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:</span><span class="sxs-lookup"><span data-stu-id="6b60c-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="6b60c-115">Muutke alatarne protsenti.</span><span class="sxs-lookup"><span data-stu-id="6b60c-115">Adjust the under-delivery percentage.</span></span>
- <span data-ttu-id="6b60c-116">Pöörake ümber ja tehke kohandusi.</span><span class="sxs-lookup"><span data-stu-id="6b60c-116">Reverse and make adjustments.</span></span>

### <a name="adjust-the-under-delivery-percentage"></a><span data-ttu-id="6b60c-117">Muutke alatarne protsenti</span><span class="sxs-lookup"><span data-stu-id="6b60c-117">Adjust the under-delivery percentage</span></span>

<span data-ttu-id="6b60c-118">Alatarne protsendi reguleerimiseks kasutage järgmist toimingut.</span><span class="sxs-lookup"><span data-stu-id="6b60c-118">Use the following procedure to adjust the under-delivery percentage.</span></span>

1. <span data-ttu-id="6b60c-119">Avage jaotis **Müügireskontro \> Tellimused \> Kõik tellimused**.</span><span class="sxs-lookup"><span data-stu-id="6b60c-119">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="6b60c-120">Valige müügitellimus, millele ei saa koormuse jaoks saatelehte sisestada.</span><span class="sxs-lookup"><span data-stu-id="6b60c-120">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="6b60c-121">Valige vahekaardil  **Müügitellimused** müügitellimuse rida kauba jaoks, mis ületab alatarne protsent.</span><span class="sxs-lookup"><span data-stu-id="6b60c-121">On the **Sales order lines** tab, select the sales order line for the item that exceeds the under-delivery percentage.</span></span>
1. <span data-ttu-id="6b60c-122">Vahekaardil  **Liini detailid** valige **Kohaletoimetamine**.</span><span class="sxs-lookup"><span data-stu-id="6b60c-122">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="6b60c-123">Seadke **Alatarne** väljal väärtus suuremale protsendile, mis rahuldab koorma koguse suhtes komplekteeritud kogust, nii et saatelehe loomine on võimalik.</span><span class="sxs-lookup"><span data-stu-id="6b60c-123">Set the **Underdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="6b60c-124">Pöörake ümber ja tehke kohandusi</span><span class="sxs-lookup"><span data-stu-id="6b60c-124">Reverse and make adjustments</span></span>

<span data-ttu-id="6b60c-125">Tühistage kõik koormuse jaoks sisestatud asjad (nt saateleht, lähetuskinnitus ja töö), tehke müügitellimuse täpsustused, väljastage tellimus uuesti lattu ja viige saatmisprotseduur lõpule.</span><span class="sxs-lookup"><span data-stu-id="6b60c-125">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="6b60c-126">Saatelehe tühistamiseks kasutage järgmist toimingut.</span><span class="sxs-lookup"><span data-stu-id="6b60c-126">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="6b60c-127">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="6b60c-127">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="6b60c-128">Valige toimingupaani vahekaardi  **Saatmine ja vastuvõtmine** jaotises  **Ümberpööramine** suvand  **Tühista saatelehed**.</span><span class="sxs-lookup"><span data-stu-id="6b60c-128">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="6b60c-129">Saadetise kinnituse tühistamiseks kasutage järgmist toimingut.</span><span class="sxs-lookup"><span data-stu-id="6b60c-129">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="6b60c-130">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="6b60c-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="6b60c-131">Valige toimingupaani vahekaardi  **Saatmine ja vastuvõtmine** jaotises  **Ümberpööramine** suvand  **Pööra saadetise kinnitus ümber**.</span><span class="sxs-lookup"><span data-stu-id="6b60c-131">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="6b60c-132">Töö pööramiseks tehke järgmised toimingud:</span><span class="sxs-lookup"><span data-stu-id="6b60c-132">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="6b60c-133">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="6b60c-133">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="6b60c-134">Valige toimingupaani vahekaardil  **Koormused** grupis  **Töö** üksus  **Pöördtöö**.</span><span class="sxs-lookup"><span data-stu-id="6b60c-134">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
