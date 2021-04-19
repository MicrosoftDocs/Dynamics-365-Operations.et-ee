---
title: Kanali navigeerimishierarhia loomine
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce navigatsiooni hierarhia.
author: samjarawan
ms.date: 01/27/2020
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
ms.openlocfilehash: 358f3d40c7a21184c20da342d6b2bf72dd4e7bbd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795831"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="8336a-103">Looge kanali navigeerimishierarhia</span><span class="sxs-lookup"><span data-stu-id="8336a-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8336a-104">Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce navigatsiooni hierarhia.</span><span class="sxs-lookup"><span data-stu-id="8336a-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8336a-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="8336a-105">Overview</span></span>

<span data-ttu-id="8336a-106">Kanali navigatsiooni hierarhiat kasutatakse toodete grupeerimiseks ja korraldamiseks kategooriatesse, nii et tooteid saab sirvida võrgus või kassas.</span><span class="sxs-lookup"><span data-stu-id="8336a-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="8336a-107">Kanali navigeerimishierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="8336a-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="8336a-108">Kanali navigeerimishierarhia loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="8336a-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="8336a-109">Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Tooted ja kategooriad \> Kanali navigatsiooni kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="8336a-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="8336a-110">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="8336a-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="8336a-111">Sisestage nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="8336a-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="8336a-112">Sisestage kirjeldus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="8336a-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="8336a-113">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="8336a-113">Select **Create**.</span></span>
1. <span data-ttu-id="8336a-114">Valige toimingupaanilt suvand **Uus kategooria sõlm**, et luua juursõlm.</span><span class="sxs-lookup"><span data-stu-id="8336a-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="8336a-115">Sisestage nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="8336a-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="8336a-116">Sisestage kirjeldus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="8336a-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="8336a-117">Sisestage hüüdnimi väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="8336a-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="8336a-118">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="8336a-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="8336a-119">Järgmine pilt näitab juursõlme näidet.</span><span class="sxs-lookup"><span data-stu-id="8336a-119">The following image shows a example root node.</span></span>

![Juursõlme näide](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="8336a-121">Navigeerimiskategooria sõlmede loomine</span><span class="sxs-lookup"><span data-stu-id="8336a-121">Create navigation category nodes</span></span>

<span data-ttu-id="8336a-122">Et luua täiendavaid navigeerimiskategooria sõlmi, mis tähistavad tootekategooriaid kanalis, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="8336a-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="8336a-123">Valige navigeerimispaanil peamine sõlm, millele kategooria lisada.</span><span class="sxs-lookup"><span data-stu-id="8336a-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="8336a-124">Valige toimingupaanil nupp **Uus kategooria sõlm**.</span><span class="sxs-lookup"><span data-stu-id="8336a-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="8336a-125">Sisestage nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="8336a-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="8336a-126">Sisestage kirjeldus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="8336a-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="8336a-127">Sisestage hüüdnimi väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="8336a-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="8336a-128">Sisestage väljale **Kuva järjekord** kuva järjekord (valikuline).</span><span class="sxs-lookup"><span data-stu-id="8336a-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="8336a-129">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="8336a-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="8336a-130">Järgmine pilt näitab lõpuleviidud kanali navigeerimishierarhia näidet.</span><span class="sxs-lookup"><span data-stu-id="8336a-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Kanali hierarhia näide](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="8336a-132">Toodete lisamine kategooria sõlmedesse</span><span class="sxs-lookup"><span data-stu-id="8336a-132">Add products to category nodes</span></span>

<span data-ttu-id="8336a-133">Toodete lisamiseks kategooria sõlmedesse toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="8336a-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="8336a-134">Valige kategooria sõlm.</span><span class="sxs-lookup"><span data-stu-id="8336a-134">Select a category node.</span></span>
1. <span data-ttu-id="8336a-135">Valige jaotises **Tooted** suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="8336a-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="8336a-136">Leidke uued tooted, mida soovite lisada, kasutades toote numbrit või nime, ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="8336a-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="8336a-137">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="8336a-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="8336a-138">Toodete lisamine sõlmele kanali navigeerimise hierarhia sees ei ole piisav, et tooted kuvataks valitud kanalis, tooted peavad olema ka tootele erinevad.</span><span class="sxs-lookup"><span data-stu-id="8336a-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a product.</span></span>

<span data-ttu-id="8336a-139">Järgmine pilt näitab lisatud toodetega sõlme näidet.</span><span class="sxs-lookup"><span data-stu-id="8336a-139">The following image shows an example node with products added.</span></span>

![Kategooria sõlme lisatud tooted](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="8336a-141">Toote atribuutide gruppide lisamine kategooria sõlmedesse</span><span class="sxs-lookup"><span data-stu-id="8336a-141">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="8336a-142">Atribuutide grupid tuleb luua enne, kui saate need kanali navigeerimise hierarhias sõlmele lisada.</span><span class="sxs-lookup"><span data-stu-id="8336a-142">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="8336a-143">Tootele kategooria sõlme atribuudigrupi lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="8336a-143">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="8336a-144">Valige kategooria sõlm.</span><span class="sxs-lookup"><span data-stu-id="8336a-144">Select a category node.</span></span>
1. <span data-ttu-id="8336a-145">Valige jaotises **Toote atribuudigrupp** suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="8336a-145">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="8336a-146">Leidke lisatavad atribuutide grupid ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="8336a-146">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="8336a-147">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="8336a-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="8336a-148">Järgmine pilt näitab sõlme näidist koos lisatud toote atribuudigruppidega.</span><span class="sxs-lookup"><span data-stu-id="8336a-148">The following image shows a sample node with product attribute groups added.</span></span>

![Sõlme toote atribuudigrupid](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="8336a-150">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="8336a-150">Additional resources</span></span>

[<span data-ttu-id="8336a-151">Sortimentide häälestamine</span><span class="sxs-lookup"><span data-stu-id="8336a-151">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="8336a-152">Atribuutide ja atribuudigruppide haldamine</span><span class="sxs-lookup"><span data-stu-id="8336a-152">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]