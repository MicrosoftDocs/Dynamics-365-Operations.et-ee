---
title: Kanalite ülevaade
description: Selles teemas antakse ülevaade rakenduse Microsoft Dynamics 365 Commerce kanalitest.
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
ms.openlocfilehash: 7f5d527dd14d24c06aef874de0088bb07c49849b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800539"
---
# <a name="channels-overview"></a><span data-ttu-id="46dd3-103">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="46dd3-103">Channels overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="46dd3-104">Selles teemas antakse ülevaade rakenduse Microsoft Dynamics 365 Commerce kanalitest.</span><span class="sxs-lookup"><span data-stu-id="46dd3-104">This topic presents an overview of channels in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="46dd3-105">See sisaldab teavet ülesannete kohta, mis tuleb lõpule viia enne ja pärast iga kanali seadistamist.</span><span class="sxs-lookup"><span data-stu-id="46dd3-105">It includes information about the tasks that you must complete both before and after you set up each channel.</span></span>

## <a name="types-of-channels"></a><span data-ttu-id="46dd3-106">Kanalite tüübid</span><span class="sxs-lookup"><span data-stu-id="46dd3-106">Types of Channels</span></span>

<span data-ttu-id="46dd3-107">Dynamics 365 Commerce toetab kolme erinevat kanali tüüpi: jae-, kõnekeskuse- ja veebikanalid.</span><span class="sxs-lookup"><span data-stu-id="46dd3-107">Dynamics 365 Commerce supports three different channel types: retail, call center, and online channels.</span></span>

### <a name="retail-channels"></a><span data-ttu-id="46dd3-108">Jaemüügikanalid</span><span class="sxs-lookup"><span data-stu-id="46dd3-108">Retail channels</span></span>

<span data-ttu-id="46dd3-109">Jaemüügi kanalid tähistavad standardseid füüsilisi kauplusi.</span><span class="sxs-lookup"><span data-stu-id="46dd3-109">Retail channels represent standard brick-and-mortar stores.</span></span> <span data-ttu-id="46dd3-110">Igal kauplusel võivad olla kassaregistrid, tulu- ja kulukontod ning personal.</span><span class="sxs-lookup"><span data-stu-id="46dd3-110">Each store can have its own point of sale (POS) registers, income and expense accounts, and staff.</span></span> 

### <a name="call-center-channels"></a><span data-ttu-id="46dd3-111">Kõnekeskuse kanalid</span><span class="sxs-lookup"><span data-stu-id="46dd3-111">Call center channels</span></span>

<span data-ttu-id="46dd3-112">Kõnekeskuse kanalid esindavad kõnekeskuse tellimuste ja klientide haldust.</span><span class="sxs-lookup"><span data-stu-id="46dd3-112">Call center channels represent call center order and customer management.</span></span>

### <a name="online-channels"></a><span data-ttu-id="46dd3-113">Võrgukanalid</span><span class="sxs-lookup"><span data-stu-id="46dd3-113">Online channels</span></span>

<span data-ttu-id="46dd3-114">Veebikanalid esindavad e-kaubanduse poode.</span><span class="sxs-lookup"><span data-stu-id="46dd3-114">Online channels represent online e-Commerce storefronts.</span></span> <span data-ttu-id="46dd3-115">Kui veebikanal on loodud, tuleb luua Microsoft Dynamics 365 Commerce'i saidiehitustööriista või kolmanda osapoole e-kaubanduse lahenduse abil sait.</span><span class="sxs-lookup"><span data-stu-id="46dd3-115">Once an online channel is created, a site must be created using the Microsoft Dynamics 365 Commerce Site Builder tool or other third-party e-Commerce solution.</span></span>

## <a name="channel-setup-basics"></a><span data-ttu-id="46dd3-116">Kanali seadistuse põhitõed</span><span class="sxs-lookup"><span data-stu-id="46dd3-116">Channel setup basics</span></span>

<span data-ttu-id="46dd3-117">Kanali seadistus teostatakse tööriistas Commerce.</span><span class="sxs-lookup"><span data-stu-id="46dd3-117">Channel set up is performed in the Commerce tool.</span></span> <span data-ttu-id="46dd3-118">Igal kanalil võivad olla oma makseviisid, hinnagrupid, toote hierarhiad, sortimendid ja toodete kogumid.</span><span class="sxs-lookup"><span data-stu-id="46dd3-118">Each channel can have its own payment methods, price groups, product hierarchies, assortments, and set of products.</span></span> <span data-ttu-id="46dd3-119">Kui olete kanali loonud, saate määrata seal müüdavad tooted.</span><span class="sxs-lookup"><span data-stu-id="46dd3-119">After you create a channel, you assign the products that you want it to carry and sell.</span></span> <span data-ttu-id="46dd3-120">Igal kanali tüübil on ainulaadne funktsioonide kogum, mida võib olla vajalik konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="46dd3-120">Each channel type has a unique set of features that may need to be configured.</span></span> <span data-ttu-id="46dd3-121">Näiteks vajab jaemüügi kanal määratud töötajaid, registreid ja kliente.</span><span class="sxs-lookup"><span data-stu-id="46dd3-121">For example, a retail channel needs assigned employees, registers, and customers.</span></span> <span data-ttu-id="46dd3-122">Kui uus kanal on loodud, tuleb see määrata organisatsiooni hierarhiale.</span><span class="sxs-lookup"><span data-stu-id="46dd3-122">Once a new channel is created, it needs to be assigned to an organization hierarchy.</span></span>

## <a name="channel-setup-prerequisites"></a><span data-ttu-id="46dd3-123">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="46dd3-123">Channel setup prerequisites</span></span>

<span data-ttu-id="46dd3-124">Enne kanali seadistamist peate täitma mõned eeltingimuseks olevad ülesanded, mis põhinevad kanali tüübil.</span><span class="sxs-lookup"><span data-stu-id="46dd3-124">Before you can set up a channel, you must complete some prerequisite tasks based on the channel type.</span></span> <span data-ttu-id="46dd3-125">Lisateavet vaadake jaotisest [Kanali seadistuse eeltingimused](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="46dd3-125">For more information, see [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="set-up-a-channel"></a><span data-ttu-id="46dd3-126">Kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="46dd3-126">Set up a channel</span></span>

<span data-ttu-id="46dd3-127">Pärast eeltingimuseks olevate ülesannete täitmist kasutage järgmisi linke edasiste seadistamise juhiste saamiseks.</span><span class="sxs-lookup"><span data-stu-id="46dd3-127">After you complete the prerequisite tasks, for further setup instructions, use the following links.</span></span>

- [<span data-ttu-id="46dd3-128">Jaemüügikanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="46dd3-128">Set up a retail channel</span></span>](channel-setup-retail.md)
- [<span data-ttu-id="46dd3-129">Kõnekeskuse kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="46dd3-129">Set up a call center channel</span></span>](channel-setup-callcenter.md)
- [<span data-ttu-id="46dd3-130">Veebikanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="46dd3-130">Set up an online channel</span></span>](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a><span data-ttu-id="46dd3-131">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="46dd3-131">Additional resources</span></span>

[<span data-ttu-id="46dd3-132">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="46dd3-132">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="46dd3-133">Jaemüügikanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="46dd3-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="46dd3-134">Veebikanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="46dd3-134">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="46dd3-135">Kõnekeskuse kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="46dd3-135">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="46dd3-136">Organisatsiooni hierarhiate seadistamine</span><span class="sxs-lookup"><span data-stu-id="46dd3-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]