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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3dcba743e6557b1bd366ac79ecb49ead831dceb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001021"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="0b1d5-103">Kanali konfigureerimine kanali navigeerimishierarhia kasutamiseks</span><span class="sxs-lookup"><span data-stu-id="0b1d5-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0b1d5-104">Selles teemas kirjeldatakse, kuidas konfigureerida rakenduses Microsoft Dynamics 365 Commerce kanal kasutama kanali navigeerimishierarhiat.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0b1d5-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="0b1d5-105">Overview</span></span>

<span data-ttu-id="0b1d5-106">Kanali navigeerimishierarhiad korraldavad tooteid kategooriatesse, nii et tooteid saab sirvida e-poes või kassas.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="0b1d5-107">Jaemüügi- ja võrgukanalid peavad olema konfigureeritud kanali navigeerimishierarhiatega.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="0b1d5-108">Kanali konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="0b1d5-108">Configure the channel</span></span>

<span data-ttu-id="0b1d5-109">Kanal konfigureerimiseks kanali navigatsioonihierarhiat kasutama toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="0b1d5-110">Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Kanali kategooriad ja toote atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="0b1d5-111">Valige konfigureerimiseks kanal.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="0b1d5-112">Valige toimingupaanil suvand **Atribuudi metaandmete häälestamine**.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="0b1d5-113">Valige ripploendis **Kategooriahierarhia** sobiv kanali navigeerimishierarhia.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="0b1d5-114">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="0b1d5-115">Lisage jaotisesse **Atribuudigrupp** kõik atribuutide grupid, mis on kõigi sõlmede globaalsed atribuudid.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="0b1d5-116">Järgmine pilt näitab kuidas konfigureerida kanalit kasutama kanali navigatsioonihierarhiat.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![Kanali konfiguratsiooni näide](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="0b1d5-118">Atribuudi metaandmete häälestamine</span><span class="sxs-lookup"><span data-stu-id="0b1d5-118">Set attribute metadata</span></span>

<span data-ttu-id="0b1d5-119">Atribuudi metaandmete häälestamine võimaldab iga sõlme atribuutide konfigureerimist.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="0b1d5-120">Atribuudi metaandmete seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="0b1d5-121">Valige toimingupaanil suvand **Atribuudi metaandmete häälestamine**.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="0b1d5-122">Iga sõlme puhul valige **Kanali toote atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="0b1d5-123">Seadke suvand **Kuva kanalil atribuuti** väärtusele **Jah** ja suvand **Saab täpsustada** väärtusele **Jah**, et lubada sellel kanalil täpsustamisi.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="0b1d5-124">Pärast iga sõlme konfigureerimist vastavalt soovile, valige **Tegevuspaanil** salvestamiseks nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="0b1d5-125">Valige ülevalt parempoolsest nurgast **X**, et väljuda sellelt kuvalt tagasi lehele **Kanali kategooriad ja tooteatribuudid**.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="0b1d5-126">Järgmine pilt näitab näidet kanali tooteatribuutide konfigureerimisest kanali kategooria sõlmel.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![Kanali atribuudid kanali kategooria sõlmel](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="0b1d5-128">Muudatuste avaldamine</span><span class="sxs-lookup"><span data-stu-id="0b1d5-128">Publish changes</span></span>

<span data-ttu-id="0b1d5-129">Muudatuste jõustumiseks tuleb muudatused avaldada.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="0b1d5-130">Muudatuste avaldamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="0b1d5-131">Valige toimingupaanil **Avalda kanali värskendused**.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="0b1d5-132">Valige paanil **Avalda kanali värskendused** nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="0b1d5-133">Järgmine pilt näitab, kuidas kanali värskendusi avaldada.</span><span class="sxs-lookup"><span data-stu-id="0b1d5-133">The following image shows how to publish channel updates.</span></span>

![Kanalivärskenduste avaldamine](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="0b1d5-135">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0b1d5-135">Additional resources</span></span>

[<span data-ttu-id="0b1d5-136">Kanali navigeerimishierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="0b1d5-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)


