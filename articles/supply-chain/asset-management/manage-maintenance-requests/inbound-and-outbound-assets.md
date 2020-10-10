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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a7239bf5f8e53e61c4259abbcbf2ff740f4cef55
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889933"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="c1b4b-103">Sissetulevad ja väljaminevad varad</span><span class="sxs-lookup"><span data-stu-id="c1b4b-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c1b4b-104">Kui teie ettevõte teeb parandustöid või hooldustöid teistest asukohtadest või klientidelt saadud varadele, saab varahaldus jälgida nii sissetulevaid varasid, mis on teel teie ettevõttesse kui ka tagastatavaid väljaminevaid varasid.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="c1b4b-105">Kui soovite kasutada sissetulevaid ja väljaminevaid elutsükli olekuid, et hallata varasid, mis tulevad sisse ja mis tagastatakse, peate seadistama hoolduse taotluse elutsükli olekud ja elutsükli mudelid nende toimingute toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="c1b4b-106">Lisateavet uute tarnijate nõuete kohta vt [Hooldusnõuded](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="c1b4b-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="c1b4b-107">’Varahalduse häälestus määratleb, kas saate töötada sissetulevate ja väljaminevate põhivaradega.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="c1b4b-108">Registreeri varad sissetulevatena</span><span class="sxs-lookup"><span data-stu-id="c1b4b-108">Register assets as inbound</span></span>

1. <span data-ttu-id="c1b4b-109">Valige **Varahaldus**\>**Ühised**\>**Hooldustaotlused**\>**Aktiivsed hooldustaotlused**.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="c1b4b-110">Valige hooldustaotlus.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="c1b4b-111">Valige **Uuenda hooldustaotluse olekut**.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="c1b4b-112">Valige **Sissetulev** (või mõni muu elutsükli olek, mille olete sissetulevate varade jaoks loonud) ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Registreeri varad sissetulevatena](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="c1b4b-114">Registreeri varad vastuvõetuna</span><span class="sxs-lookup"><span data-stu-id="c1b4b-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="c1b4b-115">Valige **Varahaldus**\>**Ühised**\>**Sissetulevad/väljaminevad**\>**Sissetulevad varad**.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="c1b4b-116">Saate valida vara või hooldustaotluse.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="c1b4b-117">Valige **Varade vastuvõtmine**.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="c1b4b-118">Väljale **Vastuvõetud** sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="c1b4b-119">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-119">Then select **OK**.</span></span> <span data-ttu-id="c1b4b-120">Kirje eemaldatakse loendilehelt **Sissetulevad varad**.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-120">The record is removed from the **Inbound assets** list page.</span></span>

![Registreeri varad vastuvõetuna](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="c1b4b-122">Registreeri varad sissetulekuna</span><span class="sxs-lookup"><span data-stu-id="c1b4b-122">Register assets as outbound</span></span>

<span data-ttu-id="c1b4b-123">Hoolduse või parandustöö lõpule viimise korral saate vara registreerida kui tagastatud.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="c1b4b-124">Valige **Varahaldus**\>**Ühised**\>**Hooldustaotlused**\>**Aktiivsed hooldustaotlused**.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="c1b4b-125">Valige hooldustaotlus.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="c1b4b-126">Valige **Uuenda hooldustaotluse olekut**.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="c1b4b-127">Valige **Väljaminev** (või mõni muu elutsükli olek, mille olete väljaminevate varade jaoks loonud) ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="c1b4b-128">Registreeri varad kui tarnitud.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="c1b4b-129">Valige **Varahaldus**\>**Ühised**\>**Sissetulevad/väljaminevad**\>**Väljaminevad varad**.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="c1b4b-130">Saate valida vara või hooldustaotluse.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="c1b4b-131">Valige **Varade kohaletoimetus**.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="c1b4b-132">Väljale **Kohale toimetatud** sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="c1b4b-133">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-133">Then select **OK**.</span></span> <span data-ttu-id="c1b4b-134">Kirje eemaldatakse loendilehelt **Väljaminev varad**.</span><span class="sxs-lookup"><span data-stu-id="c1b4b-134">The record is removed from the **Outbound assets** list page.</span></span>
