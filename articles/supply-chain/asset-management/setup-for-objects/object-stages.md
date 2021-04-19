---
title: Toote elutsükli olekud
description: Selles teemas selgitatakse vara elutsükli olekuid ja elutsükli mudeleid varahalduses.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 985fedc13e28caee90c9db27b145e415d256208d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808283"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="c477c-103">Toote elutsükli olekud</span><span class="sxs-lookup"><span data-stu-id="c477c-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c477c-104">Selles teemas selgitatakse vara elutsükli olekuid ja elutsükli mudeleid varahalduses.</span><span class="sxs-lookup"><span data-stu-id="c477c-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="c477c-105">Vara elutsükli olekuid kasutatakse määratlemaks, kas vara on aktiivne või passiivne.</span><span class="sxs-lookup"><span data-stu-id="c477c-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="c477c-106">Näiteks saate seadistada vara elutsükli olekud, näiteks **Loodud**, **Aktiivne** ja **Lõpetatud**.</span><span class="sxs-lookup"><span data-stu-id="c477c-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="c477c-107">Taotluse elutsükli olekud on seotud vara elutsükli olekuga.</span><span class="sxs-lookup"><span data-stu-id="c477c-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="c477c-108">Seega, kui taotlus on muudetud uue taotluse elutsükli olekusse, muudetakse taotlusele lisatud vara uue vara elutsükli olekusse.</span><span class="sxs-lookup"><span data-stu-id="c477c-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="c477c-109">Näiteks kui taotluse elutsükli olek muudetakse **Sissetulevaks**, muudetakse manustatud vara elutsükli olekut elutsükli olekusse, mis valitakse väljal **Sissetulev elutsükli olek** kiirkaardil **Vara elutsüklo olek** lehel **Vara elutsükli oleku mudelid**.</span><span class="sxs-lookup"><span data-stu-id="c477c-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="c477c-110">Vara elutsükli olekuid saab seadistada vara elutsükli mudelites, kus saate määratleda nõutavad elutsükli olekud eri liiki varade jaoks.</span><span class="sxs-lookup"><span data-stu-id="c477c-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="c477c-111">Esmalt seadistage elutsükli olekud.</span><span class="sxs-lookup"><span data-stu-id="c477c-111">You first set up lifecycle states.</span></span> <span data-ttu-id="c477c-112">Seejärel looge elutsükli mudel ja valige selle jaoks elutsükli olekud.</span><span class="sxs-lookup"><span data-stu-id="c477c-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="c477c-113">Valige **Varahaldus**\>**Häälestus**\>**Varad**\>**Elutsükli olekud**.</span><span class="sxs-lookup"><span data-stu-id="c477c-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="c477c-114">Valige uue vara elutsükli oleku loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c477c-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="c477c-115">Sisestage väljale **Elutsükli olek** elutsükli oleku ID.</span><span class="sxs-lookup"><span data-stu-id="c477c-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="c477c-116">Väljale **Nimi** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="c477c-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="c477c-117">Väljal **Elutsükli mudelid** kuvatakse vara elutsükli olekut kasutavate varade elutsükli mudelite arv.</span><span class="sxs-lookup"><span data-stu-id="c477c-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="c477c-118">Määrake suvandi **Aktiivne** väärtuseks **Jah**, kui see elutsükli olek peaks olema aktiivne elutsükli olek (teisisõnu, kui töökäske saab luua selle elutsükli olekus olevate varade puhul).</span><span class="sxs-lookup"><span data-stu-id="c477c-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="c477c-119">Seadke suvandi **Kustuta avatud kalendriread** väärtuseks **Jah**, kui avatud vara kalendriread, millel on vara elutsükli olek **Loodud**, tuleks kustutada, kui need on selles elutsükli olekus.</span><span class="sxs-lookup"><span data-stu-id="c477c-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="c477c-120">See säte on kasulik, kui soovite puhastada kõik avatud hooldusajakavad, mis pole vara puhul enam asjakohased (näiteks kui vara pole enam aktiivne).</span><span class="sxs-lookup"><span data-stu-id="c477c-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="c477c-121">Vara elutsükli olekud, vara elutsükli mudelid ja vara tüübid on seotud.</span><span class="sxs-lookup"><span data-stu-id="c477c-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="c477c-122">Neid kasutatakse samamoodi nagu töökäsu elutsükli olekuid, töökäsu elutsükli mudeleid ja töökäsu tüüpe.</span><span class="sxs-lookup"><span data-stu-id="c477c-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="c477c-123">Pärast nõutavate vara elutsükli mudelite loomist saate seadistada elutsükli olekud vara elutsükli mudelites.</span><span class="sxs-lookup"><span data-stu-id="c477c-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="c477c-124">Valige **Varahaldus**\>**Häälestus**\>**Varad**\>**Elutsükli mudelid**.</span><span class="sxs-lookup"><span data-stu-id="c477c-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="c477c-125">Valige uue vara elutsükli mudeli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c477c-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="c477c-126">Sisestage väljale **Elutsükli mudel** elutsükli mudeli ID.</span><span class="sxs-lookup"><span data-stu-id="c477c-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="c477c-127">Väljale **Nimi** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="c477c-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="c477c-128">Väljal **Elutsükli olekud** kuvatakse vara elutsükli mudelit kasutavate varade elutsükli olekut arv.</span><span class="sxs-lookup"><span data-stu-id="c477c-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="c477c-129">Väljal **Vara tüübid** kuvatakse elutsükli mudelit kasutavate vara tüüpide arv.</span><span class="sxs-lookup"><span data-stu-id="c477c-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="c477c-130">Kiirkaardil **Elutsükli olekud**, valige need vara elutsükli olekud, mis peaksid olema kaasatud vara elutsükli mudelis.</span><span class="sxs-lookup"><span data-stu-id="c477c-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="c477c-131">Mudeli elutsükli oleku kasutamiseks valige see jaotises **Järelejäänud elutsükli olekud** ja seejärel valige nupp ![paremnool,](media/15-setup-for-objects.png) et teisaldada see jaotisesse **Valitud elutsükli olekud**.</span><span class="sxs-lookup"><span data-stu-id="c477c-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="c477c-132">Et kasutada kõiki mudeli saadaolevaid elutsükli olekuid, valige nupp **Kõik saadaolevad elutsükli olekud** ![Kõik saadaolevad elutsükli olekud](media/20-setup-for-objects.png).</span><span class="sxs-lookup"><span data-stu-id="c477c-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="c477c-133">Kõik elutsükli olekud viiakse üle jaotisesse **Valitud elutsükli olekud**.</span><span class="sxs-lookup"><span data-stu-id="c477c-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="c477c-134">Elutsükli oleku eemaldamiseks mudelist, valige see jaotises **Valitud elutsükli mudelid** ja seejärel valige nupp ![vasaknool,](media/16-setup-for-objects.png) et teisaldada see jaotisesse **Järelejäänud elutsükli olekud**.</span><span class="sxs-lookup"><span data-stu-id="c477c-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="c477c-135">Valige **Elutsükli oleku värskendused**, et määratleda, millised elutsükli olekud saavad valitud elutsükli olekut järgida.</span><span class="sxs-lookup"><span data-stu-id="c477c-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="c477c-136">Kasutage kiirkaarti **Vara olek**, kui käsitlete remondiks saadud varasid.</span><span class="sxs-lookup"><span data-stu-id="c477c-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="c477c-137">Jaotises **Sissetulev/väljaminev** saate valida vara elutsükli olekud, et näidata vara töövoogu, mille olete paranduseks saanud.</span><span class="sxs-lookup"><span data-stu-id="c477c-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="c477c-138">Kui pakute klientidele või osakondadele laenuvarasid, saate jaotises **Laen** valida laenuvaradele elutsükli olekud.</span><span class="sxs-lookup"><span data-stu-id="c477c-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]