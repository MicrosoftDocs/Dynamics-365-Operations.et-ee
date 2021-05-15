---
title: Kanali navigeerimishierarhia loomine
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce navigatsiooni hierarhia.
author: samjarawan
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5df46de9dadfa0b7160a9b340ef36fdf963a0ad3
ms.sourcegitcommit: 6c2f5c3b038f696532c335e20b0fbafa155d6858
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951904"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="14123-103">Looge kanali navigeerimishierarhia</span><span class="sxs-lookup"><span data-stu-id="14123-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="14123-104">Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce navigatsiooni hierarhia.</span><span class="sxs-lookup"><span data-stu-id="14123-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="14123-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="14123-105">Overview</span></span>

<span data-ttu-id="14123-106">Kanali navigatsiooni hierarhiat kasutatakse toodete grupeerimiseks ja korraldamiseks kategooriatesse, nii et tooteid saab sirvida võrgus või kassas.</span><span class="sxs-lookup"><span data-stu-id="14123-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="14123-107">Kanali navigeerimishierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="14123-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="14123-108">Kanali navigeerimishierarhia loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="14123-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="14123-109">Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Tooted ja kategooriad \> Kanali navigatsiooni kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="14123-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="14123-110">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="14123-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="14123-111">Sisestage nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="14123-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="14123-112">Sisestage kirjeldus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="14123-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="14123-113">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="14123-113">Select **Create**.</span></span>
1. <span data-ttu-id="14123-114">Valige toimingupaanilt suvand **Uus kategooria sõlm**, et luua juursõlm.</span><span class="sxs-lookup"><span data-stu-id="14123-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="14123-115">Sisestage nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="14123-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="14123-116">Sisestage kirjeldus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="14123-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="14123-117">Sisestage hüüdnimi väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="14123-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="14123-118">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="14123-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="14123-119">Järgmine pilt näitab juursõlme näidet.</span><span class="sxs-lookup"><span data-stu-id="14123-119">The following image shows a example root node.</span></span>

![Juursõlme näide](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="14123-121">Navigeerimiskategooria sõlmede loomine</span><span class="sxs-lookup"><span data-stu-id="14123-121">Create navigation category nodes</span></span>

<span data-ttu-id="14123-122">Et luua täiendavaid navigeerimiskategooria sõlmi, mis tähistavad tootekategooriaid kanalis, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="14123-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="14123-123">Valige navigeerimispaanil peamine sõlm, millele kategooria lisada.</span><span class="sxs-lookup"><span data-stu-id="14123-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="14123-124">Valige toimingupaanil nupp **Uus kategooria sõlm**.</span><span class="sxs-lookup"><span data-stu-id="14123-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="14123-125">Sisestage nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="14123-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="14123-126">Sisestage kirjeldus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="14123-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="14123-127">Sisestage hüüdnimi väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="14123-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="14123-128">Sisestage väljale **Kuva järjekord** kuva järjekord (valikuline).</span><span class="sxs-lookup"><span data-stu-id="14123-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="14123-129">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="14123-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="14123-130">Järgmine pilt näitab lõpuleviidud kanali navigeerimishierarhia näidet.</span><span class="sxs-lookup"><span data-stu-id="14123-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Kanali hierarhia näide](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="14123-132">Toodete lisamine kategooria sõlmedesse</span><span class="sxs-lookup"><span data-stu-id="14123-132">Add products to category nodes</span></span>

<span data-ttu-id="14123-133">Toodete lisamiseks kategooria sõlmedesse toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="14123-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="14123-134">Valige kategooria sõlm.</span><span class="sxs-lookup"><span data-stu-id="14123-134">Select a category node.</span></span>
1. <span data-ttu-id="14123-135">Valige jaotises **Tooted** suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="14123-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="14123-136">Leidke uued tooted, mida soovite lisada, kasutades toote numbrit või nime, ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="14123-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="14123-137">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="14123-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="14123-138">Toodete lisamisest sõlmele kanali navigeerimise hierarhia sees ei piisa selleks, et tooted kuvataks valitud kanalis, tooted peavad olema ka kanalile määratud.</span><span class="sxs-lookup"><span data-stu-id="14123-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a channel.</span></span> <span data-ttu-id="14123-139">Sortimentide kohta lisateabe saamiseks vt [sortimendi haldust](assortments.md).</span><span class="sxs-lookup"><span data-stu-id="14123-139">For more information on assortments, see [Assortment management](assortments.md).</span></span>

<span data-ttu-id="14123-140">Järgmine pilt näitab lisatud toodetega sõlme näidet.</span><span class="sxs-lookup"><span data-stu-id="14123-140">The following image shows an example node with products added.</span></span>

![Kategooria sõlme lisatud tooted](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="14123-142">Toote atribuutide gruppide lisamine kategooria sõlmedesse</span><span class="sxs-lookup"><span data-stu-id="14123-142">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="14123-143">Atribuutide grupid tuleb luua enne, kui saate need kanali navigeerimise hierarhias sõlmele lisada.</span><span class="sxs-lookup"><span data-stu-id="14123-143">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="14123-144">Tootele kategooria sõlme atribuudigrupi lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="14123-144">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="14123-145">Valige kategooria sõlm.</span><span class="sxs-lookup"><span data-stu-id="14123-145">Select a category node.</span></span>
1. <span data-ttu-id="14123-146">Valige jaotises **Toote atribuudigrupp** suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="14123-146">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="14123-147">Leidke lisatavad atribuutide grupid ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="14123-147">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="14123-148">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="14123-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="14123-149">Järgmine pilt näitab sõlme näidist koos lisatud toote atribuudigruppidega.</span><span class="sxs-lookup"><span data-stu-id="14123-149">The following image shows a sample node with product attribute groups added.</span></span>

![Sõlme toote atribuudigrupid](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="14123-151">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="14123-151">Additional resources</span></span>

[<span data-ttu-id="14123-152">Sortimentide häälestamine</span><span class="sxs-lookup"><span data-stu-id="14123-152">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="14123-153">Atribuutide ja atribuudigruppide haldamine</span><span class="sxs-lookup"><span data-stu-id="14123-153">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
