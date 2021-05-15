---
title: Saadetist ei saa kinnitada, kuna kogus ületab ületarne protsendi
description: Saadetist ei saa kinnitada, kuna kogus ületab ületarne protsendi
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
ms.openlocfilehash: c9b5ba8dedb927ee049d7e53e9a666902f563f49
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938458"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a><span data-ttu-id="75c33-103">Saadetist ei saa kinnitada, kuna kogus ületab ületarne protsendi</span><span class="sxs-lookup"><span data-stu-id="75c33-103">You can't confirm a shipment because the quantity exceeds the overdelivery percentage</span></span>

<span data-ttu-id="75c33-104">Tõrkekood: WAX1687</span><span class="sxs-lookup"><span data-stu-id="75c33-104">Error code: WAX1687</span></span>

## <a name="symptoms"></a><span data-ttu-id="75c33-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="75c33-105">Symptoms</span></span>

<span data-ttu-id="75c33-106">Kui proovite saadetist kinnitada, näitab süsteem järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="75c33-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="75c33-107">Koorma saadetist %1 ei saanud kinnitada, kuna kauba kogus %2 ületab ületarne jaoks määratletud protsenti.</span><span class="sxs-lookup"><span data-stu-id="75c33-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for overdelivery.</span></span>

<span data-ttu-id="75c33-108">Seega ei saa te koorma saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="75c33-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="75c33-109">Põhjus</span><span class="sxs-lookup"><span data-stu-id="75c33-109">Cause</span></span>

<span data-ttu-id="75c33-110">Koorma või saadetise kogus on ainult osaliselt komplekteeritud.</span><span class="sxs-lookup"><span data-stu-id="75c33-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="75c33-111">Praegu ületab kogus komplekteeritud kogust protsendi võrra, mis on väljaspool lubatud ületarne protsenti.</span><span class="sxs-lookup"><span data-stu-id="75c33-111">The quantity currently exceeds the picked quantity by a percentage that is outside the allowed overdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="75c33-112">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="75c33-112">Resolution</span></span>

<span data-ttu-id="75c33-113">Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:</span><span class="sxs-lookup"><span data-stu-id="75c33-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="75c33-114">Määrake laadimisliini kogus.</span><span class="sxs-lookup"><span data-stu-id="75c33-114">Set the load line quantity.</span></span>
- <span data-ttu-id="75c33-115">Saate seadistada ületarne protsendi.</span><span class="sxs-lookup"><span data-stu-id="75c33-115">Set the overdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="75c33-116">Määrake laadimisliini kogus</span><span class="sxs-lookup"><span data-stu-id="75c33-116">Set the load line quantity</span></span>

<span data-ttu-id="75c33-117">Koguse sätete määratlemiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="75c33-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="75c33-118">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="75c33-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="75c33-119">Valige koorem, mille jaoks ei saa saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="75c33-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="75c33-120">Valige kiirkaardil **Koorma read** koorma rida kauba jaoks, mis ületab ületarne protsendi.</span><span class="sxs-lookup"><span data-stu-id="75c33-120">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="75c33-121">Kiirkaardil **Liini detailid** valige **Tellimus**.</span><span class="sxs-lookup"><span data-stu-id="75c33-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="75c33-122">Seadke väljal **Kogus** väärtus komplekteeritud kogusele (st **Tööga loodud kogus** väärtusele), et saadetise kinnitus saaks toimuda.</span><span class="sxs-lookup"><span data-stu-id="75c33-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-overdelivery-percentage"></a><span data-ttu-id="75c33-123">Saate seadistada ületarne protsendi</span><span class="sxs-lookup"><span data-stu-id="75c33-123">Set the overdelivery percentage</span></span>

<span data-ttu-id="75c33-124">Alatarne protsendi määratlemiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="75c33-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="75c33-125">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="75c33-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="75c33-126">Valige koorem, mille jaoks ei saa saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="75c33-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="75c33-127">Valige kiirkaardil **Koorma read** koorma rida kauba jaoks, mis ületab ületarne protsendi.</span><span class="sxs-lookup"><span data-stu-id="75c33-127">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="75c33-128">Kiirkaardil **Liini detailid** valige **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="75c33-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="75c33-129">Seadke **Ületarne** väljal väärtus suuremale protsendile, mis rahuldab koorma koguse suhtes komplekteeritud kogust, nii et saadetise kinnitus on võimalik.</span><span class="sxs-lookup"><span data-stu-id="75c33-129">In the **Overdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
