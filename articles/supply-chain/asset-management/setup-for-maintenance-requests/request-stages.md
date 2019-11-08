---
title: Hooldustaotluse elutsükli olekud
description: See teema kirjeldab, kuidas seadistada hooldustaotluse elutsükli olekuid varahalduses.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 151db9ca8a121759e39b690ec296b36a18dc1729
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571158"
---
# <a name="maintenance-request-lifecycle-states"></a><span data-ttu-id="c45c0-103">Hooldusnõuete töötsükli olek</span><span class="sxs-lookup"><span data-stu-id="c45c0-103">Maintenance request lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="c45c0-104">Hooldustaotluse elutsükli olekud määratlevad etapid, mida taotlus võib läbida.</span><span class="sxs-lookup"><span data-stu-id="c45c0-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="c45c0-105">Näiteks **Loodud**, **Aktiivne** ja **Lõpetatud**.</span><span class="sxs-lookup"><span data-stu-id="c45c0-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="c45c0-106">Kui hooldustaotlus teisendatakse töökäsuks, tuleks hooldustaotluse elutsükli olekut värskendada olekusse **Lõpetatud** või **Suletud**, et see ei oleks enam aktiivne.</span><span class="sxs-lookup"><span data-stu-id="c45c0-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="c45c0-107">Loendileht **Kõik hooldustaotlused** näitab kõiki hooldustaotlusi, olenemata nende elutsükli olekust.</span><span class="sxs-lookup"><span data-stu-id="c45c0-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="c45c0-108">Hooldustaotluse elutsükli olekute sätestamine</span><span class="sxs-lookup"><span data-stu-id="c45c0-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="c45c0-109">Valige **Varahaldus**\>**Häälestus**\>**Hooldustaotlused**\>**Elutsükli olekud**.</span><span class="sxs-lookup"><span data-stu-id="c45c0-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="c45c0-110">Valige uue hooldustaotluse elutsükli oleku loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c45c0-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="c45c0-111">Sisestage väljale **Elutsükli olek** elutsükli olek ID.</span><span class="sxs-lookup"><span data-stu-id="c45c0-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="c45c0-112">Väljale **Nimi** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="c45c0-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="c45c0-113">Kiirkaardi **Üksikasjad** väljal **Elutsükli mudelid** kuvatakse hooldustaotluste elutsükli mudelite arvu, mida selles elutsükli olekus kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="c45c0-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="c45c0-114">Kiirkaardil **Üldine** sätestage suvandi **Aktiivne** väärtuseks **Jah**, kui hooldustaotlus peaks selle elutsükli oleku jooksul aktiivne olema.</span><span class="sxs-lookup"><span data-stu-id="c45c0-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="c45c0-115">Sätestage suvandi **Määra tegelik lõpp** väärtuseks **Jah**, kui tegelik lõppkuupäev ja kellaaeg tuleks automaatselt sisestada hooldustaotlusele, mis on selles elutsükli olekus.</span><span class="sxs-lookup"><span data-stu-id="c45c0-115">Set he **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="c45c0-116">Sätestage suvandi **Loo töökäsk** väärtuseks **Jah**, kui töökäsku saab luua hooldustaotlusest, mis on selles elutsükli olekus.</span><span class="sxs-lookup"><span data-stu-id="c45c0-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="c45c0-117">Seadke suvandi **Kustuta** väärtuseks **Jah**, kui hooldustaotlust saab kustutada, kui see on selles elutsükli olekus.</span><span class="sxs-lookup"><span data-stu-id="c45c0-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="c45c0-118">Kiirkaardi **Värskendamine** suvandid **Sissetulev** ja **Väljaminev** jaotises **Vara** on asjakohased, kui kasutate allikaparandust. Sätestage vastava suvandi väärtuseks **Jah**, kui hooldustaotlusel valitud varade vara elutsükli oleku peaks automaatselt värskendama olekussse **Sissetulev** või **Väljaminev**, kui hooldustaotluse elutsükli olek on sätestatud olekus **Sissetulev** või **Väljaminev**.</span><span class="sxs-lookup"><span data-stu-id="c45c0-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.cSet the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="c45c0-119">Järgnev illustratsioonil kuvatakse lehe **Hooldustaotluse elutsükli olekud** näide.</span><span class="sxs-lookup"><span data-stu-id="c45c0-119">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![Hooldusnõuete töötsükli olekute leht](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="c45c0-121">Hooldustaotluse elutsükli olekud, elutsükli oleku rühmad ja tüübid on seotud ja neid kasutatakse samal viisil nagu töökäsu elutsükli olekud, elutsükli oleku rühmad ja tüübid.</span><span class="sxs-lookup"><span data-stu-id="c45c0-121">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="c45c0-122">Hooldustaotluse elutsükli mudelite sätestamine</span><span class="sxs-lookup"><span data-stu-id="c45c0-122">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="c45c0-123">Pärast seda, kui olete loonud oma hooldustaotluste jaoks nõutavad elutsükli olekud, saab neid jagada elutsükli oleku rühmadeks või elutsükli mudeliteks.</span><span class="sxs-lookup"><span data-stu-id="c45c0-123">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="c45c0-124">Hooldustaotluse elutsükli mudeleid kasutatakse voo loomiseks, mida saab kasutada eri tüüpi hooldustaotluste puhul.</span><span class="sxs-lookup"><span data-stu-id="c45c0-124">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="c45c0-125">Vähemalt üks standardne hooldustaotluse elutsükli mudel tuleks luua.</span><span class="sxs-lookup"><span data-stu-id="c45c0-125">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="c45c0-126">Valige **Varahaldus**\>**Häälestus**\>**Hooldustaotlused**\>**Elutsükli mudelid**.</span><span class="sxs-lookup"><span data-stu-id="c45c0-126">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="c45c0-127">Uue hooldustaotluse elutsükli mudeli loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c45c0-127">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="c45c0-128">Sisestage väljale **Elutsükli mudel** elutsükli mudeli ID.</span><span class="sxs-lookup"><span data-stu-id="c45c0-128">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="c45c0-129">Väljale **Nimi** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="c45c0-129">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="c45c0-130">Kiirkaardil **Üksikasjad** kuvab **Elutsükli olekud** selles elutsükli mudelis valitud elutsükli olekute arvu.</span><span class="sxs-lookup"><span data-stu-id="c45c0-130">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="c45c0-131">Väljal **Hooldustaotluse tüübid** kuvatakse selles elutsükli mudelis kasutavate hooldustaotluse tüüpide arvu.</span><span class="sxs-lookup"><span data-stu-id="c45c0-131">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="c45c0-132">Kiirkaardil **Elutsükli olekud** valige need elutsükli olekud, mis tuleks elutsükli mudelisse kaasata.</span><span class="sxs-lookup"><span data-stu-id="c45c0-132">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="c45c0-133">Elutsükli oleku lisamiseks elutsükli mudelisse, valige see jaotises **Järelejäänud elutsükli olekud** seejärel valige ![paremnool,](media/03-setup-for-requests.png) et teisaldada see jaotisesse **Valitud elutsükli olekud**.</span><span class="sxs-lookup"><span data-stu-id="c45c0-133">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="c45c0-134">Et lisada kõik saadaolevad elutsükli olekud elutsükli mudelisse valige nupp **Vali kõik saadaolevad olekud** ![Vali kõik saadaolevad olekud](media/04-setup-for-requests.png).</span><span class="sxs-lookup"><span data-stu-id="c45c0-134">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="c45c0-135">Kõik elutsükli olekud teisaldatakse jaotisesse **Valitud elutsükli olekud**.</span><span class="sxs-lookup"><span data-stu-id="c45c0-135">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="c45c0-136">Elutsükli oleku eemaldamiseks elutsükli mudelist valige see jaotises **Valitud elutsükli olekud** ja seejärel valige ![vasaknool,](media/05-setup-for-requests.png) et teisaldada see jaotisesse **Järelejäänud elutsükli olekud**.</span><span class="sxs-lookup"><span data-stu-id="c45c0-136">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="c45c0-137">Kiirkaardil **Üldine** väljad jaotises **Värskendused** on asjakohased, kui kasutate depooparandust.</span><span class="sxs-lookup"><span data-stu-id="c45c0-137">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="c45c0-138">Väljal **Vastuvõetud vara elutsükli olek** valige vara elutsükli olek hooldustaotlusel valitud varadele, mida peaks automaatselt värskendama, kui need on vastuvõetud depooparanduseks.</span><span class="sxs-lookup"><span data-stu-id="c45c0-138">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="c45c0-139">Väljal **Kohale toimetatud elutsükli olekud** valige vara elutsükli olek hooldustaotlusel valitud varadele, mida peaks automaatselt värskendama, kui need tagastatakse pärast parandust.</span><span class="sxs-lookup"><span data-stu-id="c45c0-139">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="c45c0-140">Järgnev illustratsioon näitab lehe **Hooldustaotluse elutsükli mudelid** näidet.</span><span class="sxs-lookup"><span data-stu-id="c45c0-140">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![Hooldusnõuete töötsükli mudelite leht](media/06-setup-for-requests.png)
