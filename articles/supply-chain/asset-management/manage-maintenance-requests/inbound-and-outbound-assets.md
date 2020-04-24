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
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eb491b1c3eced52f6cfc69e3da028dfed36b823b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205180"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="7ba6e-103">Sissetulevad ja väljaminevad varad</span><span class="sxs-lookup"><span data-stu-id="7ba6e-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="7ba6e-104">Kui teie ettevõte teeb parandustöid või hooldustöid teistest asukohtadest või klientidelt saadud varadele, saab varahaldus jälgida nii sissetulevaid varasid, mis on teel teie ettevõttesse kui ka tagastatavaid väljaminevaid varasid.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="7ba6e-105">Kui soovite kasutada sissetulevaid ja väljaminevaid elutsükli olekuid, et hallata varasid, mis tulevad sisse ja mis tagastatakse, peate seadistama hoolduse taotluse elutsükli olekud ja elutsükli mudelid nende toimingute toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="7ba6e-106">Lisateavet uute tarnijate nõuete kohta vt [Hooldusnõuded](../setup-for-maintenance-requests/requests.md).</span><span class="sxs-lookup"><span data-stu-id="7ba6e-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="7ba6e-107">’Varahalduse häälestus määratleb, kas saate töötada sissetulevate ja väljaminevate põhivaradega.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="7ba6e-108">Registreeri varad sissetulevatena</span><span class="sxs-lookup"><span data-stu-id="7ba6e-108">Register assets as inbound</span></span>

1. <span data-ttu-id="7ba6e-109">Valige **Varahaldus**\>**Ühised**\>**Hooldustaotlused**\>**Aktiivsed hooldustaotlused**.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="7ba6e-110">Valige hooldustaotlus.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="7ba6e-111">Valige **Uuenda hooldustaotluse olekut**.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="7ba6e-112">Valige **Sissetulev** (või mõni muu elutsükli olek, mille olete sissetulevate varade jaoks loonud) ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![Registreeri varad sissetulevatena](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="7ba6e-114">Registreeri varad vastuvõetuna</span><span class="sxs-lookup"><span data-stu-id="7ba6e-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="7ba6e-115">Valige **Varahaldus**\>**Ühised**\>**Sissetulevad/väljaminevad**\>**Sissetulevad varad**.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="7ba6e-116">Saate valida vara või hooldustaotluse.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="7ba6e-117">Valige **Varade vastuvõtmine**.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="7ba6e-118">Väljale **Vastuvõetud** sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="7ba6e-119">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-119">Then select **OK**.</span></span> <span data-ttu-id="7ba6e-120">Kirje eemaldatakse loendilehelt **Sissetulevad varad**.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-120">The record is removed from the **Inbound assets** list page.</span></span>

![Registreeri varad vastuvõetuna](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="7ba6e-122">Registreeri varad sissetulekuna</span><span class="sxs-lookup"><span data-stu-id="7ba6e-122">Register assets as outbound</span></span>

<span data-ttu-id="7ba6e-123">Hoolduse või parandustöö lõpule viimise korral saate vara registreerida kui tagastatud.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="7ba6e-124">Valige **Varahaldus**\>**Ühised**\>**Hooldustaotlused**\>**Aktiivsed hooldustaotlused**.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="7ba6e-125">Valige hooldustaotlus.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="7ba6e-126">Valige **Uuenda hooldustaotluse olekut**.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="7ba6e-127">Valige **Väljaminev** (või mõni muu elutsükli olek, mille olete väljaminevate varade jaoks loonud) ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="7ba6e-128">Registreeri varad kui tarnitud.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="7ba6e-129">Valige **Varahaldus**\>**Ühised**\>**Sissetulevad/väljaminevad**\>**Väljaminevad varad**.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="7ba6e-130">Saate valida vara või hooldustaotluse.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="7ba6e-131">Valige **Varade kohaletoimetus**.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="7ba6e-132">Väljale **Kohale toimetatud** sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="7ba6e-133">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-133">Then select **OK**.</span></span> <span data-ttu-id="7ba6e-134">Kirje eemaldatakse loendilehelt **Väljaminev varad**.</span><span class="sxs-lookup"><span data-stu-id="7ba6e-134">The record is removed from the **Outbound assets** list page.</span></span>
