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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938455"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="c2529-103">Saadetist ei saa kinnitada, kuna kaubad pole komplekteeritud</span><span class="sxs-lookup"><span data-stu-id="c2529-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="c2529-104">Tõrkekood: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="c2529-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="c2529-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="c2529-105">Symptoms</span></span>

<span data-ttu-id="c2529-106">Kui proovite saadetist kinnitada, näitab süsteem järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="c2529-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="c2529-107">Mõni koorma %1 jaoks vajalik kaup pole veel komplekteeritud ja saadetise lõppsihtkohta teisaldatud.</span><span class="sxs-lookup"><span data-stu-id="c2529-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="c2529-108">Seega ei saa te koorma saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="c2529-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="c2529-109">Põhjus</span><span class="sxs-lookup"><span data-stu-id="c2529-109">Cause</span></span>

<span data-ttu-id="c2529-110">Koormat või saadetist ei saa praeguses olekus kinnitada, kuna võib esineda üht järgmistest tingimustest:</span><span class="sxs-lookup"><span data-stu-id="c2529-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="c2529-111">Seotud tööd pole veel komplekteeritud ega teisaldatud saadetise lõppsihtkohta.</span><span class="sxs-lookup"><span data-stu-id="c2529-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="c2529-112">Komplekteeritud töö kogus ei vasta loodud töö kogusele koormareal.</span><span class="sxs-lookup"><span data-stu-id="c2529-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>

## <a name="resolution"></a><span data-ttu-id="c2529-113">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="c2529-113">Resolution</span></span>

<span data-ttu-id="c2529-114">Saate kontrollida seotud müügitellimusi või koorma või saadetise üleviimistellimusi.</span><span class="sxs-lookup"><span data-stu-id="c2529-114">Check the related sales orders or transfer orders for the load or shipment.</span></span> <span data-ttu-id="c2529-115">Kontrollige, et kogu seotud töö oleks saadetise lõppsihtkohas lõpule viidud ja et kogused sobiksid.</span><span class="sxs-lookup"><span data-stu-id="c2529-115">Make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="c2529-116">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="c2529-116">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c2529-117">Valige koorem, mille jaoks ei saa saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="c2529-117">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="c2529-118">Valige kiirkaardil **Koormaread** koormarida.</span><span class="sxs-lookup"><span data-stu-id="c2529-118">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="c2529-119">Tehke märge väärtuse kohta väljal **Loodud töö kogus**.</span><span class="sxs-lookup"><span data-stu-id="c2529-119">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="c2529-120">Toimingupaani vahekaardil **Ladu** grupis **Seotud teave** valige **Töö**.</span><span class="sxs-lookup"><span data-stu-id="c2529-120">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="c2529-121">Kontrollige, kas töö on saadetise lõppsihtkohas lõpule viidud ja et komplekteeritud töökogus vastab loodud töö kogusele koormareal.</span><span class="sxs-lookup"><span data-stu-id="c2529-121">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="c2529-122">Korrake seda protseduuri kõigi koormaridade puhul, et veenduda kõigi kriteeriumide täitmises.</span><span class="sxs-lookup"><span data-stu-id="c2529-122">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>
