---
title: Sissetulevad ja väljaminevad varad
description: Selles teemas kirjeldatakse, kuidas registreerida sissetulevad ja väljaminevad varad varahalduses.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6dfadf6824c6a3df7be9b3b6f3d9f5dd2749e34
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018067"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="475e4-103">Sissetulevad ja väljaminevad varad</span><span class="sxs-lookup"><span data-stu-id="475e4-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="475e4-104">Kui teie ettevõte teeb parandustöid või hooldustöid teistest asukohtadest või klientidelt saadud varadele, saab varahaldus jälgida nii sissetulevaid varasid, mis on teel teie ettevõttesse kui ka tagastatavaid väljaminevaid varasid.</span><span class="sxs-lookup"><span data-stu-id="475e4-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="475e4-105">Kui soovite kasutada sissetulevaid ja väljaminevaid elutsükli olekuid, et hallata varasid, mis tulevad sisse ja mis tagastatakse, peate seadistama hoolduse taotluse elutsükli olekud ja elutsükli mudelid nende toimingute toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="475e4-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="475e4-106">Lisateavet uute tarnijate nõuete kohta vt [Hooldusnõuded](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="475e4-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="475e4-107">’Varahalduse häälestus määratleb, kas saate töötada sissetulevate ja väljaminevate põhivaradega.</span><span class="sxs-lookup"><span data-stu-id="475e4-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="475e4-108">Registreeri varad sissetulevatena</span><span class="sxs-lookup"><span data-stu-id="475e4-108">Register assets as inbound</span></span>

1. <span data-ttu-id="475e4-109">Valige **Varahaldus**\>**Ühised**\>**Hooldustaotlused**\>**Aktiivsed hooldustaotlused**.</span><span class="sxs-lookup"><span data-stu-id="475e4-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="475e4-110">Valige hooldustaotlus.</span><span class="sxs-lookup"><span data-stu-id="475e4-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="475e4-111">Valige **Uuenda hooldustaotluse olekut**.</span><span class="sxs-lookup"><span data-stu-id="475e4-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="475e4-112">Valige **Sissetulev** (või mõni muu elutsükli olek, mille olete sissetulevate varade jaoks loonud) ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="475e4-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Registreeri varad sissetulevatena](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="475e4-114">Registreeri varad vastuvõetuna</span><span class="sxs-lookup"><span data-stu-id="475e4-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="475e4-115">Valige **Varahaldus**\>**Ühised**\>**Sissetulevad/väljaminevad**\>**Sissetulevad varad**.</span><span class="sxs-lookup"><span data-stu-id="475e4-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="475e4-116">Saate valida vara või hooldustaotluse.</span><span class="sxs-lookup"><span data-stu-id="475e4-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="475e4-117">Valige **Varade vastuvõtmine**.</span><span class="sxs-lookup"><span data-stu-id="475e4-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="475e4-118">Väljale **Vastuvõetud** sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="475e4-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="475e4-119">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="475e4-119">Then select **OK**.</span></span> <span data-ttu-id="475e4-120">Kirje eemaldatakse loendilehelt **Sissetulevad varad**.</span><span class="sxs-lookup"><span data-stu-id="475e4-120">The record is removed from the **Inbound assets** list page.</span></span>

![Registreeri varad vastuvõetuna](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="475e4-122">Registreeri varad sissetulekuna</span><span class="sxs-lookup"><span data-stu-id="475e4-122">Register assets as outbound</span></span>

<span data-ttu-id="475e4-123">Hoolduse või parandustöö lõpule viimise korral saate vara registreerida kui tagastatud.</span><span class="sxs-lookup"><span data-stu-id="475e4-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="475e4-124">Valige **Varahaldus**\>**Ühised**\>**Hooldustaotlused**\>**Aktiivsed hooldustaotlused**.</span><span class="sxs-lookup"><span data-stu-id="475e4-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="475e4-125">Valige hooldustaotlus.</span><span class="sxs-lookup"><span data-stu-id="475e4-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="475e4-126">Valige **Uuenda hooldustaotluse olekut**.</span><span class="sxs-lookup"><span data-stu-id="475e4-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="475e4-127">Valige **Väljaminev** (või mõni muu elutsükli olek, mille olete väljaminevate varade jaoks loonud) ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="475e4-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="475e4-128">Registreeri varad kui tarnitud.</span><span class="sxs-lookup"><span data-stu-id="475e4-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="475e4-129">Valige **Varahaldus**\>**Ühised**\>**Sissetulevad/väljaminevad**\>**Väljaminevad varad**.</span><span class="sxs-lookup"><span data-stu-id="475e4-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="475e4-130">Saate valida vara või hooldustaotluse.</span><span class="sxs-lookup"><span data-stu-id="475e4-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="475e4-131">Valige **Varade kohaletoimetus**.</span><span class="sxs-lookup"><span data-stu-id="475e4-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="475e4-132">Väljale **Kohale toimetatud** sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="475e4-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="475e4-133">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="475e4-133">Then select **OK**.</span></span> <span data-ttu-id="475e4-134">Kirje eemaldatakse loendilehelt **Väljaminev varad**.</span><span class="sxs-lookup"><span data-stu-id="475e4-134">The record is removed from the **Outbound assets** list page.</span></span>
