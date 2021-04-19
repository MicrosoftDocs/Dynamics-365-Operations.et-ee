---
title: Veebipõhise funktsiooniprofiili loomine
description: See teema kirjeldab, kuidas luua rakenduses Microsoft Dynamics 365 Commerce veebipõhine funktsiooniprofiil.
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
ms.openlocfilehash: be78b92858979b8bb009a4699eff96379ef7cef3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791098"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="6b9c7-103">Funktsiooniprofiili loomine võrgus</span><span class="sxs-lookup"><span data-stu-id="6b9c7-103">Create an online functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6b9c7-104">Selles teemas antakse ülevaade rakenduse Microsoft Dynamics 365 Commerce veebipõhise funktsiooniprofiili seadistamisest.</span><span class="sxs-lookup"><span data-stu-id="6b9c7-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6b9c7-105">Veebipõhine funktsiooniprofiil võimaldab erinevaid võrgukanalites kasutatavaid seadistusi.</span><span class="sxs-lookup"><span data-stu-id="6b9c7-105">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="6b9c7-106">Iga võrgukanal peab määrama veebipõhise funktsiooniprofiili.</span><span class="sxs-lookup"><span data-stu-id="6b9c7-106">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="6b9c7-107">Veebipõhise funktsiooniprofiili loomine</span><span class="sxs-lookup"><span data-stu-id="6b9c7-107">Create an online functionality profile</span></span>

<span data-ttu-id="6b9c7-108">Järgmine protseduur selgitab, kuidas luua rakenduses Commerce Headquarters veebipõhine funktsiooniprofiil.</span><span class="sxs-lookup"><span data-stu-id="6b9c7-108">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="6b9c7-109">Avage navigeerimispaanil **Moodulid \> Kanali seadistus \> Võrgupoe häälestus \> Funktsiooniprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="6b9c7-109">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="6b9c7-110">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6b9c7-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6b9c7-111">Väljale **Profiil** sisestage profiili ID.</span><span class="sxs-lookup"><span data-stu-id="6b9c7-111">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="6b9c7-112">Sisestage väljale **Kirjeldus** väärtus (alumisel pildil oleval näitel „Adventure Worksi profiil”).</span><span class="sxs-lookup"><span data-stu-id="6b9c7-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="6b9c7-113">Jaotises **Funktsioonid** muutke vastavalt vajadusele sätteid **OSTUKORV**, **RETAILI KLIENDID** või **VÄLJAREGISTREERIMINE**.</span><span class="sxs-lookup"><span data-stu-id="6b9c7-113">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="6b9c7-114">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="6b9c7-114">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6b9c7-115">Järgmisel pildil on näidatud veebipõhise funktsiooniprofiili näide.</span><span class="sxs-lookup"><span data-stu-id="6b9c7-115">The following image shows an example online functionality profile.</span></span>
  
![Veebipõhise funktsiooniprofiili näide](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="6b9c7-117">Funktsioonid</span><span class="sxs-lookup"><span data-stu-id="6b9c7-117">Functions</span></span>

- <span data-ttu-id="6b9c7-118">**Ühenda tooted**: kui see on lubatud, võimaldab see funktsioon ostukorvil värskendada kogust, kui sama üksus lisatakse mitu korda.</span><span class="sxs-lookup"><span data-stu-id="6b9c7-118">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="6b9c7-119">**Luba väljaregistreerimine ilma maksmiseta**: kui see on lubatud, käsitleb see funktsioon stsenaariumi, kui ostukorvi lisatud kaupadel on hind 0,00 dollarit.</span><span class="sxs-lookup"><span data-stu-id="6b9c7-119">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="6b9c7-120">**Loo klient asünkroonses režiimis**: see on pärandseadistus, mis on kohaldatav kolmanda poole e-Commerce’i kanalitele ja ei rakendata Dynamics 365 e-Commerce’i saidile.</span><span class="sxs-lookup"><span data-stu-id="6b9c7-120">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6b9c7-121">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6b9c7-121">Additional resources</span></span>

[<span data-ttu-id="6b9c7-122">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="6b9c7-122">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="6b9c7-123">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="6b9c7-123">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="6b9c7-124">Veebikanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="6b9c7-124">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="6b9c7-125">Jaemüügikanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="6b9c7-125">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="6b9c7-126">Kõnekeskuse kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="6b9c7-126">Set up a call center channel</span></span>](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
