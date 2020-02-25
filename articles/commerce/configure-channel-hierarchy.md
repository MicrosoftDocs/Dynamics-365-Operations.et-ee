---
title: Kanali konfigureerimine kanali navigeerimishierarhia kasutamiseks
description: Selles teemas kirjeldatakse, kuidas konfigureerida rakenduses Microsoft Dynamics 365 Commerce kanal kasutama kanali navigeerimishierarhiat.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7b5041d35d310125c314ab2cb77d3cc40cdb7113
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002216"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="1f1f3-103">Kanali konfigureerimine kanali navigeerimishierarhia kasutamiseks</span><span class="sxs-lookup"><span data-stu-id="1f1f3-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1f1f3-104">Selles teemas kirjeldatakse, kuidas konfigureerida rakenduses Microsoft Dynamics 365 Commerce kanal kasutama kanali navigeerimishierarhiat.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1f1f3-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="1f1f3-105">Overview</span></span>

<span data-ttu-id="1f1f3-106">Kanali navigeerimishierarhiad korraldavad tooteid kategooriatesse, nii et tooteid saab sirvida e-poes või kassas.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="1f1f3-107">Jaemüügi- ja võrgukanalid peavad olema konfigureeritud kanali navigeerimishierarhiatega.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="1f1f3-108">Kanali konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="1f1f3-108">Configure the channel</span></span>

<span data-ttu-id="1f1f3-109">Kanal konfigureerimiseks kanali navigatsioonihierarhiat kasutama toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="1f1f3-110">Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Kanali kategooriad ja toote atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="1f1f3-111">Valige konfigureerimiseks kanal.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="1f1f3-112">Valige toimingupaanil suvand **Atribuudi metaandmete häälestamine**.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="1f1f3-113">Valige ripploendis **Kategooriahierarhia** sobiv kanali navigeerimishierarhia.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="1f1f3-114">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="1f1f3-115">Lisage jaotisesse **Atribuudigrupp** kõik atribuutide grupid, mis on kõigi sõlmede globaalsed atribuudid.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="1f1f3-116">Järgmine pilt näitab kuidas konfigureerida kanalit kasutama kanali navigatsioonihierarhiat.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![Kanali konfiguratsiooni näide](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="1f1f3-118">Atribuudi metaandmete häälestamine</span><span class="sxs-lookup"><span data-stu-id="1f1f3-118">Set attribute metadata</span></span>

<span data-ttu-id="1f1f3-119">Atribuudi metaandmete häälestamine võimaldab iga sõlme atribuutide konfigureerimist.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="1f1f3-120">Atribuudi metaandmete seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="1f1f3-121">Valige toimingupaanil suvand **Atribuudi metaandmete häälestamine**.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="1f1f3-122">Iga sõlme puhul valige **Kanali toote atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="1f1f3-123">Seadke suvand **Kuva kanalil atribuuti** väärtusele **Jah** ja suvand **Saab täpsustada** väärtusele **Jah**, et lubada sellel kanalil täpsustamisi.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="1f1f3-124">Pärast iga sõlme konfigureerimist vastavalt soovile, valige **Tegevuspaanil** salvestamiseks nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="1f1f3-125">Valige ülevalt parempoolsest nurgast **X**, et väljuda sellelt kuvalt tagasi lehele **Kanali kategooriad ja tooteatribuudid**.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="1f1f3-126">Järgmine pilt näitab näidet kanali tooteatribuutide konfigureerimisest kanali kategooria sõlmel.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![Kanali atribuudid kanali kategooria sõlmel](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="1f1f3-128">Muudatuste avaldamine</span><span class="sxs-lookup"><span data-stu-id="1f1f3-128">Publish changes</span></span>

<span data-ttu-id="1f1f3-129">Muudatuste jõustumiseks tuleb muudatused avaldada.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="1f1f3-130">Muudatuste avaldamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="1f1f3-131">Valige toimingupaanil **Avalda kanali värskendused**.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="1f1f3-132">Valige paanil **Avalda kanali värskendused** nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="1f1f3-133">Järgmine pilt näitab, kuidas kanali värskendusi avaldada.</span><span class="sxs-lookup"><span data-stu-id="1f1f3-133">The following image shows how to publish channel updates.</span></span>

![Kanalivärskenduste avaldamine](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="1f1f3-135">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1f1f3-135">Additional resources</span></span>

[<span data-ttu-id="1f1f3-136">Kanali navigeerimishierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="1f1f3-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)


