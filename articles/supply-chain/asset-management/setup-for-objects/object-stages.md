---
title: Toote elutsükli olekud
description: Selles teemas selgitatakse vara elutsükli olekuid ja elutsükli mudeleid varahalduses.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 566036c6361194d910a0fc34bd5d72147585ec4f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426164"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="3fa70-103">Toote elutsükli olekud</span><span class="sxs-lookup"><span data-stu-id="3fa70-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="3fa70-104">Selles teemas selgitatakse vara elutsükli olekuid ja elutsükli mudeleid varahalduses.</span><span class="sxs-lookup"><span data-stu-id="3fa70-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="3fa70-105">Vara elutsükli olekuid kasutatakse määratlemaks, kas vara on aktiivne või passiivne.</span><span class="sxs-lookup"><span data-stu-id="3fa70-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="3fa70-106">Näiteks saate seadistada vara elutsükli olekud, näiteks **Loodud**, **Aktiivne** ja **Lõpetatud**.</span><span class="sxs-lookup"><span data-stu-id="3fa70-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="3fa70-107">Taotluse elutsükli olekud on seotud vara elutsükli olekuga.</span><span class="sxs-lookup"><span data-stu-id="3fa70-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="3fa70-108">Seega, kui taotlus on muudetud uue taotluse elutsükli olekusse, muudetakse taotlusele lisatud vara uue vara elutsükli olekusse.</span><span class="sxs-lookup"><span data-stu-id="3fa70-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="3fa70-109">Näiteks kui taotluse elutsükli olek muudetakse **Sissetulevaks**, muudetakse manustatud vara elutsükli olekut elutsükli olekusse, mis valitakse väljal **Sissetulev elutsükli olek** kiirkaardil **Vara elutsüklo olek** lehel **Vara elutsükli oleku mudelid**.</span><span class="sxs-lookup"><span data-stu-id="3fa70-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="3fa70-110">Vara elutsükli olekuid saab seadistada vara elutsükli mudelites, kus saate määratleda nõutavad elutsükli olekud eri liiki varade jaoks.</span><span class="sxs-lookup"><span data-stu-id="3fa70-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="3fa70-111">Esmalt seadistage elutsükli olekud.</span><span class="sxs-lookup"><span data-stu-id="3fa70-111">You first set up lifecycle states.</span></span> <span data-ttu-id="3fa70-112">Seejärel looge elutsükli mudel ja valige selle jaoks elutsükli olekud.</span><span class="sxs-lookup"><span data-stu-id="3fa70-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="3fa70-113">Valige **Varahaldus**\>**Häälestus**\>**Varad**\>**Elutsükli olekud**.</span><span class="sxs-lookup"><span data-stu-id="3fa70-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="3fa70-114">Valige uue vara elutsükli oleku loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="3fa70-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="3fa70-115">Sisestage väljale **Elutsükli olek** elutsükli oleku ID.</span><span class="sxs-lookup"><span data-stu-id="3fa70-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="3fa70-116">Väljale **Nimi** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="3fa70-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="3fa70-117">Väljal **Elutsükli mudelid** kuvatakse vara elutsükli olekut kasutavate varade elutsükli mudelite arv.</span><span class="sxs-lookup"><span data-stu-id="3fa70-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="3fa70-118">Määrake suvandi **Aktiivne** väärtuseks **Jah**, kui see elutsükli olek peaks olema aktiivne elutsükli olek (teisisõnu, kui töökäske saab luua selle elutsükli olekus olevate varade puhul).</span><span class="sxs-lookup"><span data-stu-id="3fa70-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="3fa70-119">Seadke suvandi **Kustuta avatud kalendriread** väärtuseks **Jah**, kui avatud vara kalendriread, millel on vara elutsükli olek **Loodud**, tuleks kustutada, kui need on selles elutsükli olekus.</span><span class="sxs-lookup"><span data-stu-id="3fa70-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="3fa70-120">See säte on kasulik, kui soovite puhastada kõik avatud hooldusajakavad, mis pole vara puhul enam asjakohased (näiteks kui vara pole enam aktiivne).</span><span class="sxs-lookup"><span data-stu-id="3fa70-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="3fa70-121">Vara elutsükli olekud, vara elutsükli mudelid ja vara tüübid on seotud.</span><span class="sxs-lookup"><span data-stu-id="3fa70-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="3fa70-122">Neid kasutatakse samamoodi nagu töökäsu elutsükli olekuid, töökäsu elutsükli mudeleid ja töökäsu tüüpe.</span><span class="sxs-lookup"><span data-stu-id="3fa70-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="3fa70-123">Pärast nõutavate vara elutsükli mudelite loomist saate seadistada elutsükli olekud vara elutsükli mudelites.</span><span class="sxs-lookup"><span data-stu-id="3fa70-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="3fa70-124">Valige **Varahaldus**\>**Häälestus**\>**Varad**\>**Elutsükli mudelid**.</span><span class="sxs-lookup"><span data-stu-id="3fa70-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="3fa70-125">Valige uue vara elutsükli mudeli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="3fa70-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="3fa70-126">Sisestage väljale **Elutsükli mudel** elutsükli mudeli ID.</span><span class="sxs-lookup"><span data-stu-id="3fa70-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="3fa70-127">Väljale **Nimi** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="3fa70-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="3fa70-128">Väljal **Elutsükli olekud** kuvatakse vara elutsükli mudelit kasutavate varade elutsükli olekut arv.</span><span class="sxs-lookup"><span data-stu-id="3fa70-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="3fa70-129">Väljal **Vara tüübid** kuvatakse elutsükli mudelit kasutavate vara tüüpide arv.</span><span class="sxs-lookup"><span data-stu-id="3fa70-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="3fa70-130">Kiirkaardil **Elutsükli olekud**, valige need vara elutsükli olekud, mis peaksid olema kaasatud vara elutsükli mudelis.</span><span class="sxs-lookup"><span data-stu-id="3fa70-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="3fa70-131">Mudeli elutsükli oleku kasutamiseks valige see jaotises **Järelejäänud elutsükli olekud** ja seejärel valige nupp ![paremnool,](media/15-setup-for-objects.png) et teisaldada see jaotisesse **Valitud elutsükli olekud**.</span><span class="sxs-lookup"><span data-stu-id="3fa70-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="3fa70-132">Et kasutada kõiki mudeli saadaolevaid elutsükli olekuid, valige nupp **Kõik saadaolevad elutsükli olekud** ![Kõik saadaolevad elutsükli olekud](media/20-setup-for-objects.png).</span><span class="sxs-lookup"><span data-stu-id="3fa70-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="3fa70-133">Kõik elutsükli olekud viiakse üle jaotisesse **Valitud elutsükli olekud**.</span><span class="sxs-lookup"><span data-stu-id="3fa70-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="3fa70-134">Elutsükli oleku eemaldamiseks mudelist, valige see jaotises **Valitud elutsükli mudelid** ja seejärel valige nupp ![vasaknool,](media/16-setup-for-objects.png) et teisaldada see jaotisesse **Järelejäänud elutsükli olekud**.</span><span class="sxs-lookup"><span data-stu-id="3fa70-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="3fa70-135">Valige **Elutsükli oleku värskendused**, et määratleda, millised elutsükli olekud saavad valitud elutsükli olekut järgida.</span><span class="sxs-lookup"><span data-stu-id="3fa70-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="3fa70-136">Kasutage kiirkaarti **Vara olek**, kui käsitlete remondiks saadud varasid.</span><span class="sxs-lookup"><span data-stu-id="3fa70-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="3fa70-137">Jaotises **Sissetulev/väljaminev** saate valida vara elutsükli olekud, et näidata vara töövoogu, mille olete paranduseks saanud.</span><span class="sxs-lookup"><span data-stu-id="3fa70-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="3fa70-138">Kui pakute klientidele või osakondadele laenuvarasid, saate jaotises **Laen** valida laenuvaradele elutsükli olekud.</span><span class="sxs-lookup"><span data-stu-id="3fa70-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>
