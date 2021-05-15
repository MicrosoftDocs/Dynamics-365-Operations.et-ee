---
title: Saadetist ei saa kinnitada lõpetamata või puuduva töö tõttu
description: Saadetist ei saa kinnitada lõpetamata või puuduva töö tõttu
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
ms.openlocfilehash: da6388d433d6021a99840ae9781c717db1b540a9
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938456"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a><span data-ttu-id="7b095-103">Saadetist ei saa kinnitada lõpetamata või puuduva töö tõttu</span><span class="sxs-lookup"><span data-stu-id="7b095-103">You can't confirm a shipment because of incomplete or missing work</span></span>

<span data-ttu-id="7b095-104">Tõrkekood: WAX515</span><span class="sxs-lookup"><span data-stu-id="7b095-104">Error code: WAX515</span></span>

## <a name="symptoms"></a><span data-ttu-id="7b095-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="7b095-105">Symptoms</span></span>

<span data-ttu-id="7b095-106">Kui proovite saadetist kinnitada, näitab süsteem järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="7b095-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="7b095-107">Koorma %1 saadetist ei saanud kinnitada, kuna kogu koorma töö peab olema lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="7b095-107">The shipment for load %1 could not be confirmed because all work for the load must be complete.</span></span>

<span data-ttu-id="7b095-108">Seega ei saa te koorma saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="7b095-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="7b095-109">Põhjus</span><span class="sxs-lookup"><span data-stu-id="7b095-109">Cause</span></span>

<span data-ttu-id="7b095-110">Koorem või saadetis on praegu olekus, kus saadetise kinnitamine nurjub.</span><span class="sxs-lookup"><span data-stu-id="7b095-110">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="7b095-111">Enne saadetise kinnitamist peab koorma jaoks olema vähemalt üks töö ja kogu selle töö olek peab olema kas *Suletud* või *Tühistatud*.</span><span class="sxs-lookup"><span data-stu-id="7b095-111">Before you can confirm the shipment, at least some work must exist for the load, and all that work must have a status of *Closed* or *Canceled*.</span></span>

## <a name="resolution"></a><span data-ttu-id="7b095-112">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="7b095-112">Resolution</span></span>

<span data-ttu-id="7b095-113">Kontrollige koorma või saadetisega seotud müügitellimusi või üleviimistellimusi ja veenduge, et kogu seotud töö on lõpule viidud või tühistatud.</span><span class="sxs-lookup"><span data-stu-id="7b095-113">Check the related sales orders or transfer orders for the load or shipment, and make sure that all the related work has been completed or canceled.</span></span>

<span data-ttu-id="7b095-114">Saate töötada saadetiste ja koormatega mitmel lehel.</span><span class="sxs-lookup"><span data-stu-id="7b095-114">You can work with shipments and loads on several pages.</span></span> <span data-ttu-id="7b095-115">Järgmised alamjaotised pakuvad mõnda näidet.</span><span class="sxs-lookup"><span data-stu-id="7b095-115">The following subsections provide a few examples.</span></span>

### <a name="all-loads-page"></a><span data-ttu-id="7b095-116">Kõigi koormate leht</span><span class="sxs-lookup"><span data-stu-id="7b095-116">All loads page</span></span>

1. <span data-ttu-id="7b095-117">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="7b095-117">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="7b095-118">Valige koorem, mille jaoks ei saa saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="7b095-118">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="7b095-119">Toimingupaani vahekaardil **Ladu** grupis **Seotud teave** valige **Töö**.</span><span class="sxs-lookup"><span data-stu-id="7b095-119">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="7b095-120">Kontrollige iga töö ID olekut.</span><span class="sxs-lookup"><span data-stu-id="7b095-120">Inspect the status of each work ID.</span></span> <span data-ttu-id="7b095-121">Jälgige kõiki töö ID-sid, mille olek ei ole *Suletud* või *Tühistatud*.</span><span class="sxs-lookup"><span data-stu-id="7b095-121">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="7b095-122">Kui iga töö ID olek on *Suletud* või *Tühistatud*, proovige saadetist uuesti kinnitada.</span><span class="sxs-lookup"><span data-stu-id="7b095-122">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-shipments-page"></a><span data-ttu-id="7b095-123">Kõigi saadetiste leht</span><span class="sxs-lookup"><span data-stu-id="7b095-123">All shipments page</span></span>

1. <span data-ttu-id="7b095-124">Avage **Laohaldus \> Saadetised \> Kõik saadetised**.</span><span class="sxs-lookup"><span data-stu-id="7b095-124">Go to **Warehouse management \> Shipments\> All shipments**.</span></span>
1. <span data-ttu-id="7b095-125">Valige saadetis, mida ei saa kinnitada.</span><span class="sxs-lookup"><span data-stu-id="7b095-125">Select the shipment that can't be confirmed.</span></span>
1. <span data-ttu-id="7b095-126">Valige toimingupaani vahekaardil **Saadetised** grupis **Töö** üksus **Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="7b095-126">On the Action Pane, on the **Shipments** tab, in the **Work** group, select **Work details**.</span></span>
1. <span data-ttu-id="7b095-127">Kontrollige iga töö ID olekut.</span><span class="sxs-lookup"><span data-stu-id="7b095-127">Inspect the status of each work ID.</span></span> <span data-ttu-id="7b095-128">Jälgige kõiki töö ID-sid, mille olek ei ole *Suletud* või *Tühistatud*.</span><span class="sxs-lookup"><span data-stu-id="7b095-128">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="7b095-129">Kui iga töö ID olek on *Suletud* või *Tühistatud*, proovige saadetist uuesti kinnitada.</span><span class="sxs-lookup"><span data-stu-id="7b095-129">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-work-page"></a><span data-ttu-id="7b095-130">Kõigi tööde leht</span><span class="sxs-lookup"><span data-stu-id="7b095-130">All work page</span></span>

1. <span data-ttu-id="7b095-131">Avage jaotis **Laohaldus \> Töö \> Kõik tööd**.</span><span class="sxs-lookup"><span data-stu-id="7b095-131">Go to **Warehouse management \> Work\> All work**.</span></span>
1. <span data-ttu-id="7b095-132">Valige töö tellimuse numbriga, mille jaoks ei saa saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="7b095-132">Select the work for the order number that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="7b095-133">Paani tegumiriba vahekaardil **Tarne** grupis **tarne** valige suvand **Kinnita tarne**.</span><span class="sxs-lookup"><span data-stu-id="7b095-133">On the Action Pane, on the **Shipment** tab, in the **Shipment** group, select **Confirm shipment**.</span></span>
1. <span data-ttu-id="7b095-134">Kontrollige iga töö ID olekut.</span><span class="sxs-lookup"><span data-stu-id="7b095-134">Inspect the status of each work ID.</span></span> <span data-ttu-id="7b095-135">Jälgige kõiki töö ID-sid, mille olek ei ole *Suletud* või *Tühistatud*.</span><span class="sxs-lookup"><span data-stu-id="7b095-135">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="7b095-136">Kui iga töö ID olek on *Suletud* või *Tühistatud*, proovige saadetist uuesti kinnitada.</span><span class="sxs-lookup"><span data-stu-id="7b095-136">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>
