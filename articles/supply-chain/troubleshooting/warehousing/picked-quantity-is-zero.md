---
title: Saadetist ei saa kinnitada, kuna kogus on null
description: Saadetist ei saa kinnitada, kuna kogus on null
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938454"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a><span data-ttu-id="4dad0-103">Saadetist ei saa kinnitada, kuna kogus on null</span><span class="sxs-lookup"><span data-stu-id="4dad0-103">You can't confirm a shipment because there is zero quantity</span></span>

<span data-ttu-id="4dad0-104">Tõrkekood: LoadLineWarningUpdatedToZero</span><span class="sxs-lookup"><span data-stu-id="4dad0-104">Error code: LoadLineWarningUpdatedToZero</span></span>

## <a name="symptoms"></a><span data-ttu-id="4dad0-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="4dad0-105">Symptoms</span></span>

<span data-ttu-id="4dad0-106">Kui proovite saadetist kinnitada, näitab süsteem järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="4dad0-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="4dad0-107">Kauba %1 ja saadetise %2 koormarida on värskendatud nullkogusele, kuna alatarne häälestus ei luba selle kauba jaoks ükskõik millises koguses saadetisi.</span><span class="sxs-lookup"><span data-stu-id="4dad0-107">Load line for item %1 and shipment %2 has been updated to have zero quantity due to underdelivery setup allowing not to ship any quantities for this item.</span></span>

<span data-ttu-id="4dad0-108">Seega ei saa te koorma saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="4dad0-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="4dad0-109">Põhjus</span><span class="sxs-lookup"><span data-stu-id="4dad0-109">Cause</span></span>

<span data-ttu-id="4dad0-110">Süsteem hindab, kas komplekteeritud kogus jääb oodatud piiridesse, võttes aluseks komplekteeritud koguse, koormarea koguse ja alatarne protsendi.</span><span class="sxs-lookup"><span data-stu-id="4dad0-110">The system evaluates whether the picked quantity is within the expected limits, based on the picked quantity, load line quantity, and underdelivery percentage.</span></span> <span data-ttu-id="4dad0-111">Kui süsteem leiab, et komplekteeritud kogus koormareal on 0 (null), ei saa saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="4dad0-111">If the system finds that the picked quantity on the load line is 0 (zero), you can't confirm the shipment.</span></span> <span data-ttu-id="4dad0-112">Näiteks võib see probleem ilmneda, kui töö on tühistatud ja koormarea alatarne protsent on 100 protsenti.</span><span class="sxs-lookup"><span data-stu-id="4dad0-112">For example, this issue might occur if work has been canceled, and the underdelivery percentage on the load line is 100 percent.</span></span>

## <a name="resolution"></a><span data-ttu-id="4dad0-113">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="4dad0-113">Resolution</span></span>

<span data-ttu-id="4dad0-114">Kontrollige koorma ridu veendumaks, et alatarnete protsent ja kogused on joondatud komplekteeritud tööga.</span><span class="sxs-lookup"><span data-stu-id="4dad0-114">Check your load lines to make sure that the underdelivery percentage and quantities are aligned with the picked work.</span></span>

1. <span data-ttu-id="4dad0-115">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="4dad0-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="4dad0-116">Valige koorem, mille jaoks ei saa saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="4dad0-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="4dad0-117">Valige kiirkaardil **Koorma read** koorma rida kauba jaoks, mis ületab alatarne protsendi.</span><span class="sxs-lookup"><span data-stu-id="4dad0-117">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="4dad0-118">Korrigeerige välja **Alatarne** väärtust või välja **Kogus** vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="4dad0-118">Adjust the value of the **Underdelivery** field or the **Quantity** field as required.</span></span>

> [!TIP]
> <span data-ttu-id="4dad0-119">Kui probleem pole ikka veel lahendatud, peate lõpule viima rohkem komplekteerimistööd seotud müügitellimustes või üleviimistellimustes kuni saadav kogus on koorma või saadetisega joondatud.</span><span class="sxs-lookup"><span data-stu-id="4dad0-119">If the issue still isn't fixed, you might have to complete more picking work for the related sales orders or transfer orders until the available quantity is aligned with the load or shipment.</span></span>
