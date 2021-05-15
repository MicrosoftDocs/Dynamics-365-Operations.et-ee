---
title: Saadetist ei saa kinnitada, kuna kogus ületab alatarne protsendi
description: Saadetist ei saa kinnitada, kuna kogus ületab alatarne protsendi
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
ms.openlocfilehash: 5339b9d800f7454e2a00c230a8d5deca3979c074
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938453"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a><span data-ttu-id="4bfc4-103">Saadetist ei saa kinnitada, kuna kogus ületab alatarne protsendi</span><span class="sxs-lookup"><span data-stu-id="4bfc4-103">You can't confirm a shipment because the quantity exceeds the underdelivery percentage</span></span>

<span data-ttu-id="4bfc4-104">Tõrkekood: WAX1687</span><span class="sxs-lookup"><span data-stu-id="4bfc4-104">Error code: WAX1687</span></span>

## <a name="symptoms"></a><span data-ttu-id="4bfc4-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="4bfc4-105">Symptoms</span></span>

<span data-ttu-id="4bfc4-106">Kui proovite saadetist kinnitada, näitab süsteem järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="4bfc4-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="4bfc4-107">Koorma saadetist %1 ei saanud kinnitada, kuna kauba kogus %2 ületab alatarne jaoks määratletud protsenti.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for underdelivery.</span></span>

<span data-ttu-id="4bfc4-108">Seega ei saa te koorma saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="4bfc4-109">Põhjus</span><span class="sxs-lookup"><span data-stu-id="4bfc4-109">Cause</span></span>

<span data-ttu-id="4bfc4-110">Koorma või saadetise kogus on ainult osaliselt komplekteeritud.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="4bfc4-111">Kogus on praegu valitud kogusest väiksem protsentides, mis jääb väljapoole lubatud alatarnimise protsenti.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-111">The quantity is currently less than the picked quantity by a percentage that is outside the allowed underdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="4bfc4-112">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="4bfc4-112">Resolution</span></span>

<span data-ttu-id="4bfc4-113">Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:</span><span class="sxs-lookup"><span data-stu-id="4bfc4-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="4bfc4-114">Määrake laadimisliini kogus.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-114">Set the load line quantity.</span></span>
- <span data-ttu-id="4bfc4-115">Saate seadistada alatarne protsendi.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-115">Set the underdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="4bfc4-116">Määrake laadimisliini kogus</span><span class="sxs-lookup"><span data-stu-id="4bfc4-116">Set the load line quantity</span></span>

<span data-ttu-id="4bfc4-117">Koguse sätete määratlemiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="4bfc4-118">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="4bfc4-119">Valige koorem, mille jaoks ei saa saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="4bfc4-120">Valige kiirkaardil **Koorma read** koorma rida kauba jaoks, mis ületab alatarne protsendi.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-120">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="4bfc4-121">Kiirkaardil **Liini detailid** valige **Tellimus**.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="4bfc4-122">Seadke väljal **Kogus** väärtus komplekteeritud kogusele (st **Tööga loodud kogus** väärtusele), et saadetise kinnitus saaks toimuda.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-underdelivery-percentage"></a><span data-ttu-id="4bfc4-123">Saate seadistada alatarne protsendi</span><span class="sxs-lookup"><span data-stu-id="4bfc4-123">Set the underdelivery percentage</span></span>

<span data-ttu-id="4bfc4-124">Alatarne protsendi määratlemiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="4bfc4-125">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="4bfc4-126">Valige koorem, mille jaoks ei saa saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="4bfc4-127">Valige kiirkaardil **Koorma read** koorma rida kauba jaoks, mis ületab alatarne protsendi.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-127">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="4bfc4-128">Kiirkaardil **Liini detailid** valige **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="4bfc4-129">Seadke **Alatarne** väljal väärtus suuremale protsendile, mis rahuldab koorma koguse suhtes komplekteeritud kogust, nii et saadetise kinnitus on võimalik.</span><span class="sxs-lookup"><span data-stu-id="4bfc4-129">In the **Underdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
