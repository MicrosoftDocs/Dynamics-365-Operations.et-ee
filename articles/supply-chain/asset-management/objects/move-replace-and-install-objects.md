---
title: Varade teisaldamine, asendamine ja installimine
description: Selles teemas kirjeldatakse, kuidas varasid moodulis Asset Management teisaldada, asendada ja installida.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0e6306698d351d33cae627e3741ad9a2eb6d893
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783221"
---
# <a name="move-replace-and-install-assets"></a><span data-ttu-id="43e73-103">Varade teisaldamine, asendamine ja installimine</span><span class="sxs-lookup"><span data-stu-id="43e73-103">Move, replace, and install assets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="43e73-104">Selles teemas kirjeldatakse, kuidas varasid moodulis Asset Management teisaldada, asendada ja installida.</span><span class="sxs-lookup"><span data-stu-id="43e73-104">This topic explains how to move, replace, and install assets in Asset Management.</span></span> <span data-ttu-id="43e73-105">Saate luua üksikuid varasid, millel pole seoseid muude varadega või luua vara struktuuri, mis sisaldab emavara (ülataseme vara) ja seotud tütarvarasid (alamvarasid).</span><span class="sxs-lookup"><span data-stu-id="43e73-105">You can create individual assets that have no relations to other assets, or you can create an asset structure that includes a parent asset (top-level asset) and related child assets (sub-assets).</span></span> <span data-ttu-id="43e73-106">Moodulis Asset management on kolm võimalust vara asukoha teisaldamiseks ja muutmiseks.</span><span class="sxs-lookup"><span data-stu-id="43e73-106">In Asset Management, there are three approaches to moving and changing the location of an asset:</span></span>

- <span data-ttu-id="43e73-107">**Teisalda** – saate teisaldada vara kas muusse vara struktuuri või muusse asukohta samas varastruktuuris.</span><span class="sxs-lookup"><span data-stu-id="43e73-107">**Move** – Move an asset either to another asset structure or to another location in the same asset structure.</span></span>
- <span data-ttu-id="43e73-108">**Asenda** – saate vara struktuurist ajutiselt eemaldada, et seda saaks parandada või remontida ja seejärel lisada remonditud vara hiljem tagasi vara struktuuri.</span><span class="sxs-lookup"><span data-stu-id="43e73-108">**Replace** – Temporarily remove an asset from an asset structure so that it can be repaired or refurbished, and then add the refurbished asset back to the asset structure later.</span></span> <span data-ttu-id="43e73-109">Teise võimalusena asendada kasutatud vara püsivalt uue varaga.</span><span class="sxs-lookup"><span data-stu-id="43e73-109">Alternatively, permanently replace a used asset with a new asset.</span></span>
- <span data-ttu-id="43e73-110">**Installi** – saate emavara ja kõik seotud tütarvarad töö asukohta installida.</span><span class="sxs-lookup"><span data-stu-id="43e73-110">**Install** – Install a parent asset and any related child assets on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="43e73-111">Teisaldamisel, asendamisel või installimisel olev vara võib olla seotud mõne muu töö asukohaga.</span><span class="sxs-lookup"><span data-stu-id="43e73-111">The asset that you move, replace, or install might be related to another functional location.</span></span> <span data-ttu-id="43e73-112">Sel juhul võib vara kasutada töö asukoha finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="43e73-112">In that case, the asset might use financial dimensions of the functional location.</span></span> <span data-ttu-id="43e73-113">Lehel **Töö asukoha tüübid** seadistage finantsdimensioonide käsitsemine töö asukohtadele.</span><span class="sxs-lookup"><span data-stu-id="43e73-113">On the **Functional location types** page, you set up the handling of financial dimensions on functional locations.</span></span>

## <a name="move-asset"></a><span data-ttu-id="43e73-114">Vara teisaldamine</span><span class="sxs-lookup"><span data-stu-id="43e73-114">Move asset</span></span>

<span data-ttu-id="43e73-115">Funktsiooni **Vara teisaldamine** saate kasutada vara teisaldamiseks kas muusse vara struktuuri või muusse asukohta samas varastruktuuris.</span><span class="sxs-lookup"><span data-stu-id="43e73-115">Use the **Move asset** function to move an asset either to another asset structure or to another location in the same asset structure.</span></span> <span data-ttu-id="43e73-116">Vara saab teisaldada ka väljapoole vara struktuuris, nii et sellest saab eraldiseisev vara, millel pole seoseid struktuuriga.</span><span class="sxs-lookup"><span data-stu-id="43e73-116">You can also move an asset out of an asset structure so that it becomes a standalone asset that has no structure relations.</span></span>

> [!NOTE]
> <span data-ttu-id="43e73-117">Ärge kasutage seda funktsiooni, kui varasid parandatakse või asendatakse ajutiselt.</span><span class="sxs-lookup"><span data-stu-id="43e73-117">Don't use this function if assets are being repaired or temporarily replaced.</span></span> <span data-ttu-id="43e73-118">Selle asemel kasutage funktsiooni **Vara asendamine**, mida kirjeldatakse hiljem selles teemas.</span><span class="sxs-lookup"><span data-stu-id="43e73-118">Instead, use the **Replace asset** functionality that is described later in this topic.</span></span>

1. <span data-ttu-id="43e73-119">Valige **Varahaldus** \> **Ühine** \> **Varad** \> **Kõik varad** või **Aktiivsed varad**.</span><span class="sxs-lookup"><span data-stu-id="43e73-119">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="43e73-120">Valige loendist teisaldatav vara.</span><span class="sxs-lookup"><span data-stu-id="43e73-120">In the list, select the asset to move.</span></span> <span data-ttu-id="43e73-121">Kui varal on alamarad, teisaldate ka need varad.</span><span class="sxs-lookup"><span data-stu-id="43e73-121">If the asset has child assets, you also move those assets.</span></span>
3. <span data-ttu-id="43e73-122">Valige **Teisalda vara**.</span><span class="sxs-lookup"><span data-stu-id="43e73-122">Select **Move asset**.</span></span>
4. <span data-ttu-id="43e73-123">Vara teisaldamiseks nii, et see muutuks varade struktuuri osaks, valige uus emavara väljal **Emavara**.</span><span class="sxs-lookup"><span data-stu-id="43e73-123">To move the asset so that it becomes part of an asset structure, select the new parent asset in the **Parent asset** field.</span></span> <span data-ttu-id="43e73-124">Kui teisaldate tütarvara ja soovite muuta selle eraldiseisvad põhivarad, millel pole struktuurisuhteid, jätke **emasvara** väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="43e73-124">If you're moving a child asset, and you want to make it a standalone asset that has no structure relations, leave the **Parent asset** field blank.</span></span>
5. <span data-ttu-id="43e73-125">Vaikimisi määratakse väljale **Kehtiv** praegune kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="43e73-125">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="43e73-126">Siiski saate valida mõne muu kuupäeva ja kellaaja, millest alates vara teisaldamine kehtib.</span><span class="sxs-lookup"><span data-stu-id="43e73-126">However, you can select a different date and time that the asset move is valid from.</span></span>
6. <span data-ttu-id="43e73-127">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="43e73-127">Select **OK**.</span></span>

## <a name="replace-asset"></a><span data-ttu-id="43e73-128">Vara asendamine</span><span class="sxs-lookup"><span data-stu-id="43e73-128">Replace asset</span></span>

<span data-ttu-id="43e73-129">Kasutage funktsiooni **Vara asendamine** seoses remontimise, renoveerimise või kulunud vara püsiva asendamisega uue varaga.</span><span class="sxs-lookup"><span data-stu-id="43e73-129">Use the **Replace asset** function in connection with repairs, refurbishment, or permanent replacement of a worn-out asset by a new asset.</span></span> <span data-ttu-id="43e73-130">Seda funktsiooni kasutatakse alamvarade asendamiseks vara struktuuris.</span><span class="sxs-lookup"><span data-stu-id="43e73-130">This function is used to replace child assets in an asset structure.</span></span> <span data-ttu-id="43e73-131">Emavara jaoks (st varad, millel pole praegu emavara), tehakse see asendamine töö asukohas.</span><span class="sxs-lookup"><span data-stu-id="43e73-131">For parent assets (that is, assets that don't currently have a parent asset), this replacement is done on a functional location.</span></span> <span data-ttu-id="43e73-132">Lisateabe saamiseks emavara asendamiseks töö asukohas lugege teemat [Varade installimine töö asukohtadesse](../functional-locations/install-objects-on-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="43e73-132">For more information about how to replace parent assets on a functional location, see [Install assets on functional locations](../functional-locations/install-objects-on-functional-locations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="43e73-133">Kui tootmisosakonnaga on seotud remonditöökoda, saate luua töö asukohti **(nt Remont**, **Praak**ja **Ladustamine**), et käsitseda vara parandamist ja asendamist.</span><span class="sxs-lookup"><span data-stu-id="43e73-133">If a repair shop is related to your production department, you can create functional locations such as **Repair**, **Scrap**, and **Storage** to handle the repair and replacement of assets.</span></span>

1. <span data-ttu-id="43e73-134">Valige **Varahaldus** \> **Ühine** \> **Varad** \> **Kõik varad** või **Aktiivsed varad**.</span><span class="sxs-lookup"><span data-stu-id="43e73-134">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="43e73-135">Valige loendist asendatav alamvara.</span><span class="sxs-lookup"><span data-stu-id="43e73-135">In the list, select the child asset to replace.</span></span> <span data-ttu-id="43e73-136">Kui varal on alamvarad, asendate ka need varad.</span><span class="sxs-lookup"><span data-stu-id="43e73-136">If the asset has child assets, you also replace those assets.</span></span>
3. <span data-ttu-id="43e73-137">Valige **Asenda vara**.</span><span class="sxs-lookup"><span data-stu-id="43e73-137">Select **Replace asset**.</span></span>

    <span data-ttu-id="43e73-138">Väljal **Struktuuri muutus** kuvatakse viimane kuupäev ja kellaaeg, millal valitud vara ja seotud alamvarad vara struktuuris teisaldati.</span><span class="sxs-lookup"><span data-stu-id="43e73-138">The **Structure change** field shows the last date and time that the selected asset and related child assets were moved in the asset structure.</span></span>

4. <span data-ttu-id="43e73-139">Valige jaotise **Valitud vara** väljal **Töö sihtasukoht** töö asukoht, kuhu vara teisaldada.</span><span class="sxs-lookup"><span data-stu-id="43e73-139">In the **Selected asset** section, in the **Target functional location** field, select the functional location to move the asset to.</span></span> <span data-ttu-id="43e73-140">Näiteks saate valida asukoha **Remont** või **Praak**.</span><span class="sxs-lookup"><span data-stu-id="43e73-140">For example, select the **Repair** or **Scrap** location.</span></span>

    <span data-ttu-id="43e73-141">Jaotises **Emavara** kuvatakse väljal **Kehtiv** viimane kuupäev ja kellaaeg, mil emavara ja sellega seotud tütarvarad on praegusesse töö asukohta installitud või teisaldatud.</span><span class="sxs-lookup"><span data-stu-id="43e73-141">In the **Parent asset** section, the **Effective** field shows the last date and time that the parent asset and related child assets were installed or moved on the current functional location.</span></span>

5. <span data-ttu-id="43e73-142">Valige jaotise **Uus vara** väljal **Vara** valitud vara ajutiseks või püsivaks asendamiseks lisatav vara.</span><span class="sxs-lookup"><span data-stu-id="43e73-142">In the **New asset** section, in the **Asset** field, select the asset to insert as a temporary or permanent replacement for the selected asset.</span></span> <span data-ttu-id="43e73-143">See vara võib praegu asuda mõnes muus töö asukohas (nt **Ladustamine**).</span><span class="sxs-lookup"><span data-stu-id="43e73-143">This asset might currently be located on another functional location, such as **Storage**.</span></span>
7. <span data-ttu-id="43e73-144">Jaotises **Kehtiv alates** on väli **Kehtiv** seadistatud vaikimisi praegusele kuupäevale ja kellaajale.</span><span class="sxs-lookup"><span data-stu-id="43e73-144">In the **Effective from** section, the **Effective** field is set to the current date and time by default.</span></span> <span data-ttu-id="43e73-145">Siiski saate valida mõne muu kuupäeva ja kellaaja, millest alates vara asendamine kehtib.</span><span class="sxs-lookup"><span data-stu-id="43e73-145">However, you can select a different date and time that the asset replacement is valid from.</span></span>
8. <span data-ttu-id="43e73-146">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="43e73-146">Select **OK**.</span></span>

## <a name="install-asset"></a><span data-ttu-id="43e73-147">Vara installimine</span><span class="sxs-lookup"><span data-stu-id="43e73-147">Install asset</span></span>

<span data-ttu-id="43e73-148">Vara struktuuri installimiseks töö asukohta kasutage funktsiooni **Vara installimine**.</span><span class="sxs-lookup"><span data-stu-id="43e73-148">Use the **Install asset** function to install an asset structure on a functional location.</span></span>

> [!NOTE]
> <span data-ttu-id="43e73-149">Valige alati emavara.</span><span class="sxs-lookup"><span data-stu-id="43e73-149">Always select a parent asset.</span></span> <span data-ttu-id="43e73-150">Emavara ja sellega seotud tütarvarad teisaldatakse valitud töö asukohta.</span><span class="sxs-lookup"><span data-stu-id="43e73-150">The parent asset and related child assets will be moved to the selected functional location.</span></span>

1. <span data-ttu-id="43e73-151">Valige **Varahaldus** \> **Ühine** \> **Varad** \> **Kõik varad** või **Aktiivsed varad**.</span><span class="sxs-lookup"><span data-stu-id="43e73-151">Select **Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**.</span></span>
2. <span data-ttu-id="43e73-152">Valige loendist ema vara, mida soovite installida muusse töö asukohta.</span><span class="sxs-lookup"><span data-stu-id="43e73-152">In the list, select the parent asset to install on another functional location.</span></span>
3. <span data-ttu-id="43e73-153">Valige **Installi vara**.</span><span class="sxs-lookup"><span data-stu-id="43e73-153">Select **Install asset**.</span></span>

    <span data-ttu-id="43e73-154">Jaotises **Atribuudid** kuvatakse emavaras seadistatud vara atribuudid.</span><span class="sxs-lookup"><span data-stu-id="43e73-154">The **Attributes** section shows the asset attributes that are set up on the parent asset.</span></span>

4. <span data-ttu-id="43e73-155">Valige väljal **Töö asukoht** uus asukoht.</span><span class="sxs-lookup"><span data-stu-id="43e73-155">In the **Functional location** field, select the new location.</span></span>
5. <span data-ttu-id="43e73-156">Vaikimisi määratakse väljale **Kehtiv** praegune kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="43e73-156">By default, the **Effective** field is set to the current date and time.</span></span> <span data-ttu-id="43e73-157">Siiski saate valida mõne muu kuupäeva ja kellaaja, millest alates vara installimine vara struktuuri kehtib.</span><span class="sxs-lookup"><span data-stu-id="43e73-157">However, you can select a different date and time that the installation on the asset structure is valid from.</span></span>
6. <span data-ttu-id="43e73-158">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="43e73-158">Select **OK**.</span></span>
