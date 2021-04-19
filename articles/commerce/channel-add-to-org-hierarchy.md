---
title: Kanali lisamine organisatsiooni hierarhiale
description: Selles teemas kirjeldatakse, kuidas lisada rakenduses Microsoft Dynamics 365 Commerce' organisatsiooni hierarhiale kanalit.
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
ms.openlocfilehash: c7ff6d8ee7e526e45975cfa500b5e6d6079054dc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800683"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a><span data-ttu-id="9da6e-103">Kanali lisamine organisatsiooni hierarhiale</span><span class="sxs-lookup"><span data-stu-id="9da6e-103">Add a channel to an organizational hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9da6e-104">Selles teemas kirjeldatakse, kuidas lisada rakenduses Microsoft Dynamics 365 Commerce' organisatsiooni hierarhiale kanalit.</span><span class="sxs-lookup"><span data-stu-id="9da6e-104">This topic describes how to add a channel to an organizational hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9da6e-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="9da6e-105">Overview</span></span>

<span data-ttu-id="9da6e-106">Kanalid peavad olema seotud ühe või mitme organisatsiooni hierarhiaga.</span><span class="sxs-lookup"><span data-stu-id="9da6e-106">Channels need to be associated with one or more organizational hierarchies.</span></span> <span data-ttu-id="9da6e-107">Enne kanalite loomist peate kontrollima, et teie organisatsiooni hierarhiad on seadistatud.</span><span class="sxs-lookup"><span data-stu-id="9da6e-107">Before creating channels, you need to confirm that your organizational hierarchies have been set up.</span></span>  

<span data-ttu-id="9da6e-108">Lisateavet organisatsiooni hierarhiate loomise kohta vt jaotisest [Organisatsiooni hierarhiad](channels-org-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="9da6e-108">See [Organizational hierarchies](channels-org-hierarchies.md) for more details on how to create organizational hierarchies.</span></span>

## <a name="select-a-hierarchy"></a><span data-ttu-id="9da6e-109">Valige hierarhia</span><span class="sxs-lookup"><span data-stu-id="9da6e-109">Select a hierarchy</span></span>

<span data-ttu-id="9da6e-110">Hierarhia valimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="9da6e-110">To select a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="9da6e-111">Avage navigeerimispaanilt **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Organisatsiooni hierarhiad**.</span><span class="sxs-lookup"><span data-stu-id="9da6e-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="9da6e-112">Valige loendist organisatsiooni hierarhia, kuhu te kanali lisate.</span><span class="sxs-lookup"><span data-stu-id="9da6e-112">From the list, select the organization hierarchy that you'll be adding the channel to.</span></span>
1. <span data-ttu-id="9da6e-113">Valige tegevuspaanil hierarhia üksikasjade vaatamiseks **Kuva**.</span><span class="sxs-lookup"><span data-stu-id="9da6e-113">On the action pane, select **View** to view hierarchy details.</span></span>

<span data-ttu-id="9da6e-114">Järgmine pilt näitab organisatsiooni hierarhia üksikasju valitud hierarhia kohta.</span><span class="sxs-lookup"><span data-stu-id="9da6e-114">The following image shows organizational hierarchy details for the selected hierarchy.</span></span>

![Organisatsiooni hierarhia üksikasjad valitud hierarhia kohta](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a><span data-ttu-id="9da6e-116">Kanali lisamine hierarhia sõlmele</span><span class="sxs-lookup"><span data-stu-id="9da6e-116">Add a channel to a hierachy node</span></span>

<span data-ttu-id="9da6e-117">Hierarhia sõlmele kanali lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="9da6e-117">To add a channel to a hierachy node, follow these steps.</span></span>

1. <span data-ttu-id="9da6e-118">Valige tegevuspaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="9da6e-118">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="9da6e-119">Valige hierarhia sõlm, kuhu soovite kanali lisada, seejärel valige ripploendist **Sisesta** valik **Jaemüügikanal**.</span><span class="sxs-lookup"><span data-stu-id="9da6e-119">Select the hierachy node you want the channel added to, then from the **Insert** drop-down list, select **Retail Channel**.</span></span> 
1. <span data-ttu-id="9da6e-120">Valige lisatav kanal ja seejärel klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="9da6e-120">Select the channel to add, then select the **OK** button.</span></span>
1. <span data-ttu-id="9da6e-121">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9da6e-121">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="9da6e-122">Valige tegevuspaanilt **Avalda** ja esitage minevikus olev **Jõustumise kuupäev**, et see tegevus jõustuks kohe.</span><span class="sxs-lookup"><span data-stu-id="9da6e-122">On the action pane, select **Publish** and provide an **Effective date** in the past to have this action go into effect immediately.</span></span>

<span data-ttu-id="9da6e-123">Järgmine pilt näitab, kuidas valida kanalit hierarhia sõlme lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="9da6e-123">The following image shows how to select a channel to add to a hierarchy node.</span></span>

![Kanali valimine hierarhia sõlmele lisamiseks](media/channel-add-to-org-hierarchy-2.png)

<span data-ttu-id="9da6e-125">Järgmine pilt näitab hierarhiat erinevate lisatud kanalitega.</span><span class="sxs-lookup"><span data-stu-id="9da6e-125">The following image shows a hierarchy with various channels added.</span></span>

![Hierarhia erinevate lisatud kanalitega](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="9da6e-127">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="9da6e-127">Additional resources</span></span>

[<span data-ttu-id="9da6e-128">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="9da6e-128">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="9da6e-129">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="9da6e-129">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="9da6e-130">Organisatsioonide ja organisatsioonihierarhiate ülevaade</span><span class="sxs-lookup"><span data-stu-id="9da6e-130">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="9da6e-131">Organisatsioonihierarhia kavandamine</span><span class="sxs-lookup"><span data-stu-id="9da6e-131">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="9da6e-132">Organisatsiooni hierarhiad</span><span class="sxs-lookup"><span data-stu-id="9da6e-132">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="9da6e-133">Jaemüügikanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="9da6e-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="9da6e-134">Veebikanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="9da6e-134">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]