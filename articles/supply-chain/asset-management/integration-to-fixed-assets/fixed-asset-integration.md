---
title: Varahalduse integreerimine põhivaradega
description: Selles teemas selgitatakse, kuidas integreerida varahaldus- ja põhivarade mooduleid, et saaksite ühendada põhivarad varahooldusega.
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: cdda44d361011706fe0ba170309908533aa0c2f7
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276909"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="74f55-103">Varahalduse integreerimine põhivaradega</span><span class="sxs-lookup"><span data-stu-id="74f55-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="74f55-104">Kui integreerite moodulid **Varahaldus** ja **Põhivarad**, saate ühendada põhivarad varahooldusega.</span><span class="sxs-lookup"><span data-stu-id="74f55-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="74f55-105">Põhivarade kasutajad saavad seejärel luua varahoolduse uue või olemasoleva põhivara põhjal ning varahalduse kasutajad saavad seostada varahoolduse olemasoleva põhivaraga.</span><span class="sxs-lookup"><span data-stu-id="74f55-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="74f55-106">See funktsioon muudab ka põhivarade kasutajatel selliste kulude vaatamise lihtsamaks, mis sisestati töökäskude kaudu seotud varahoolduse tööde jaoks.</span><span class="sxs-lookup"><span data-stu-id="74f55-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="74f55-107">Selles teemas viitab termin *varahooldus* mooduli **Varahaldus** varadele ning termin *põhivarad* mooduli **Põhivarad** varadele.</span><span class="sxs-lookup"><span data-stu-id="74f55-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="74f55-108">Põhivaradest loodud varahoolduse töö vaikeasukoha määramine (valikuline)</span><span class="sxs-lookup"><span data-stu-id="74f55-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="74f55-109">See valikuline konfiguratsioon lubab teil määrata põhivaradest loodud varahoolduse töö jaoks vaikeasukoha.</span><span class="sxs-lookup"><span data-stu-id="74f55-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="74f55-110">Tavaliselt viite selle konfiguratsiooni lõpule ainult üks kord, kui üldse.</span><span class="sxs-lookup"><span data-stu-id="74f55-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="74f55-111">Konfiguratsiooni lõpetamiseks järgige järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="74f55-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="74f55-112">Avage **Varahaldus \> Seadistus \> Varahalduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="74f55-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="74f55-113">Valige vaikeasukoht vahekaardi **Põhivarad** väljal **Töö asukoht**.</span><span class="sxs-lookup"><span data-stu-id="74f55-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="74f55-114">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="74f55-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="74f55-115">Integreeritud varahoolduse ja põhivaradega töötamine</span><span class="sxs-lookup"><span data-stu-id="74f55-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="74f55-116">Selles jaotises on toodud tegevuste kogum erinevatest viisidest, kuidas töötada integreeritud varahalduse ja põhivarade funktsioonidega.</span><span class="sxs-lookup"><span data-stu-id="74f55-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="74f55-117">Olemasoleva varahoolduse seostamine põhivaraga</span><span class="sxs-lookup"><span data-stu-id="74f55-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="74f55-118">Olemasoleva varahoolduse seostamiseks põhivaraga toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="74f55-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="74f55-119">Valige **Varahaldus \> Varad \> Kõik varad** (või **Aktiivsed varad**).</span><span class="sxs-lookup"><span data-stu-id="74f55-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="74f55-120">Valige vara.</span><span class="sxs-lookup"><span data-stu-id="74f55-120">Select an asset.</span></span>
1. <span data-ttu-id="74f55-121">Valige kiirkaardi **Põhivara** väljal **Põhivara kood** olemasolev põhivara.</span><span class="sxs-lookup"><span data-stu-id="74f55-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="74f55-122">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="74f55-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="74f55-123">Valitud varahooldusega seotud põhivara kuvamine</span><span class="sxs-lookup"><span data-stu-id="74f55-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="74f55-124">Valitud varahooldusega seotud põhivara kuvamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="74f55-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="74f55-125">Valige **Varahaldus \> Varad \> Kõik varad** (või **Aktiivsed varad**).</span><span class="sxs-lookup"><span data-stu-id="74f55-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="74f55-126">Valige vara.</span><span class="sxs-lookup"><span data-stu-id="74f55-126">Select an asset.</span></span>
1. <span data-ttu-id="74f55-127">Valige link kiirkaardi **Põhivara** väljal **Põhivara kood**.</span><span class="sxs-lookup"><span data-stu-id="74f55-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="74f55-128">Avatakse leht **Põhivara** valitud vara jaoks.</span><span class="sxs-lookup"><span data-stu-id="74f55-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="74f55-129">(Tavaliselt leiate selle lehe siit: **Põhivarad \> Põhivarad \> Põhivarad**.)</span><span class="sxs-lookup"><span data-stu-id="74f55-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="74f55-130">Valitud põhivaraga seotud varahoolduse kuvamine</span><span class="sxs-lookup"><span data-stu-id="74f55-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="74f55-131">Valitud põhivaraga seotud varahoolduse kuvamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="74f55-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="74f55-132">Avage **Põhivarad \> Põhivarad \> Põhivarad**.</span><span class="sxs-lookup"><span data-stu-id="74f55-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="74f55-133">Valige vara.</span><span class="sxs-lookup"><span data-stu-id="74f55-133">Select an asset.</span></span>
1. <span data-ttu-id="74f55-134">Seejärel valige toimingupaanil vahekaardi **Varahaldus** grupis **Kuva** suvand **Varahooldus**.</span><span class="sxs-lookup"><span data-stu-id="74f55-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="74f55-135">Avatakse valitud põhivaraga seotud vara **Varahoolduse** leht.</span><span class="sxs-lookup"><span data-stu-id="74f55-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="74f55-136">(Tavaliselt leiate selle lehe siit: **Varahaldus \> Varad \> Kõik varad**.)</span><span class="sxs-lookup"><span data-stu-id="74f55-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="74f55-137">Põhivaraga seotud hoolduskulude kuvamine</span><span class="sxs-lookup"><span data-stu-id="74f55-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="74f55-138">Varahoolduse jaoks saab sisestada varahalduse töökäske ja neil kõigil on tavaliselt kulu.</span><span class="sxs-lookup"><span data-stu-id="74f55-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="74f55-139">Kui põhivara seostatakse varahooldusega, saate seotud kulusid vaadata otse põhivara kaudu.</span><span class="sxs-lookup"><span data-stu-id="74f55-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="74f55-140">Põhivaraga seotud hoolduskulude kuvamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="74f55-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="74f55-141">Avage **Põhivarad \> Põhivarad \> Põhivarad**.</span><span class="sxs-lookup"><span data-stu-id="74f55-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="74f55-142">Valige vara.</span><span class="sxs-lookup"><span data-stu-id="74f55-142">Select an asset.</span></span>
1. <span data-ttu-id="74f55-143">Seejärel valige toimingupaanil vahekaardi **Varahaldus** grupis **Kuva** suvand **Hoolduskulu**.</span><span class="sxs-lookup"><span data-stu-id="74f55-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="74f55-144">Avatakse **Hoolduskulu** leht, millel kuvatakse seotud kulud.</span><span class="sxs-lookup"><span data-stu-id="74f55-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="74f55-145">Olemasolevale põhivarale uue varahoolduse loomine</span><span class="sxs-lookup"><span data-stu-id="74f55-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="74f55-146">Olemasolevale põhivarale uue varahoolduse loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="74f55-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="74f55-147">Avage **Põhivarad \> Põhivarad \> Põhivarad**.</span><span class="sxs-lookup"><span data-stu-id="74f55-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="74f55-148">Valige vara.</span><span class="sxs-lookup"><span data-stu-id="74f55-148">Select an asset.</span></span>
1. <span data-ttu-id="74f55-149">Seejärel valige toimingupaanil vahekaardi **Varahaldus** grupis **Uus** suvand **Loo varahooldus**.</span><span class="sxs-lookup"><span data-stu-id="74f55-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="74f55-150">(Kui see valik ei ole saadaval, võib varahooldus juba valitud põhivaraga seotud olla.)</span><span class="sxs-lookup"><span data-stu-id="74f55-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="74f55-151">Lõpetage vara loomine, nagu kirjeldatud jaotises [Vara loomine](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="74f55-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="74f55-152">Uue põhivara loomine ja sellele uue varahoolduse lisamine</span><span class="sxs-lookup"><span data-stu-id="74f55-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="74f55-153">Uue põhivara loomiseks ja sellele uue varahoolduse lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="74f55-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="74f55-154">Avage **Põhivarad \> Põhivarad \> Põhivarad**.</span><span class="sxs-lookup"><span data-stu-id="74f55-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="74f55-155">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="74f55-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="74f55-156">Lõpetage põhivara loomine, nagu kirjeldatud jaotises [Põhivara loomine](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="74f55-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="74f55-157">Seejärel valige toimingupaanil vahekaardi **Varahaldus** grupis **Uus** suvand **Loo varahooldus**.</span><span class="sxs-lookup"><span data-stu-id="74f55-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="74f55-158">Lõpetage vara loomine, nagu kirjeldatud jaotises [Vara loomine](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="74f55-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="74f55-159">Seose eemaldamine kahe vara vahelt</span><span class="sxs-lookup"><span data-stu-id="74f55-159">Remove the association between two assets</span></span>

<span data-ttu-id="74f55-160">Mõnel juhul peate eemaldama seose varahoolduse ja selle põhivara vahelt.</span><span class="sxs-lookup"><span data-stu-id="74f55-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="74f55-161">Näiteks kui soovite [luua uue varahoolduse](#new-maintenance-from-fixed) põhivarast, peate esmalt eemaldama kõik olemasolevad seosed.</span><span class="sxs-lookup"><span data-stu-id="74f55-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="74f55-162">Olemasoleva seose eemaldamiseks varahoolduse ja põhivara vahelt toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="74f55-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="74f55-163">Valige **Varahaldus \> Varad \> Kõik varad** (või **Aktiivsed varad**).</span><span class="sxs-lookup"><span data-stu-id="74f55-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="74f55-164">Leidke ja avage põhivara.</span><span class="sxs-lookup"><span data-stu-id="74f55-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="74f55-165">Eemaldage kiirkaardil **Põhivara** välja **Töö asukoht** väärtus.</span><span class="sxs-lookup"><span data-stu-id="74f55-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="74f55-166">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="74f55-166">On the Action Pane, select **Save**.</span></span>
