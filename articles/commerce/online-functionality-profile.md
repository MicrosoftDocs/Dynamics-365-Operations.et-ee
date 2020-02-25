---
title: Veebipõhise funktsiooniprofiili loomine
description: See teema kirjeldab, kuidas luua rakenduses Microsoft Dynamics 365 Commerce veebipõhine funktsiooniprofiil.
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
ms.openlocfilehash: 5ecbfcf3fa78ad2909a7cc9988ab1edaf2b98376
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003368"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="56033-103">Veebipõhise funktsiooniprofiili loomine</span><span class="sxs-lookup"><span data-stu-id="56033-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="56033-104">Selles teemas antakse ülevaade rakenduse Microsoft Dynamics 365 Commerce veebipõhise funktsiooniprofiili seadistamisest.</span><span class="sxs-lookup"><span data-stu-id="56033-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="56033-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="56033-105">Overview</span></span>

<span data-ttu-id="56033-106">Veebipõhine funktsiooniprofiil võimaldab erinevaid võrgukanalites kasutatavaid seadistusi.</span><span class="sxs-lookup"><span data-stu-id="56033-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="56033-107">Iga võrgukanal peab määrama veebipõhise funktsiooniprofiili.</span><span class="sxs-lookup"><span data-stu-id="56033-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="56033-108">Veebipõhise funktsiooniprofiili loomine</span><span class="sxs-lookup"><span data-stu-id="56033-108">Create an online functionality profile</span></span>

<span data-ttu-id="56033-109">Järgmine protseduur selgitab, kuidas luua rakenduses Commerce Headquarters veebipõhine funktsiooniprofiil.</span><span class="sxs-lookup"><span data-stu-id="56033-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="56033-110">Avage navigeerimispaanil **Moodulid \> Kanali seadistus \> Võrgupoe häälestus \> Funktsiooniprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="56033-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="56033-111">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="56033-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="56033-112">Väljale **Profiil** sisestage profiili ID.</span><span class="sxs-lookup"><span data-stu-id="56033-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="56033-113">Sisestage väljale **Kirjeldus** väärtus (alumisel pildil oleval näitel „Adventure Worksi profiil”).</span><span class="sxs-lookup"><span data-stu-id="56033-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="56033-114">Jaotises **Funktsioonid** muutke vastavalt vajadusele sätteid **OSTUKORV**, **RETAILI KLIENDID** või **VÄLJAREGISTREERIMINE**.</span><span class="sxs-lookup"><span data-stu-id="56033-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="56033-115">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="56033-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="56033-116">Järgmisel pildil on näidatud veebipõhise funktsiooniprofiili näide.</span><span class="sxs-lookup"><span data-stu-id="56033-116">The following image shows an example online functionality profile.</span></span>
  
![Veebipõhise funktsiooniprofiili näide](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="56033-118">Funktsioonid</span><span class="sxs-lookup"><span data-stu-id="56033-118">Functions</span></span>

- <span data-ttu-id="56033-119">**Ühenda tooted**: kui see on lubatud, võimaldab see funktsioon ostukorvil värskendada kogust, kui sama üksus lisatakse mitu korda.</span><span class="sxs-lookup"><span data-stu-id="56033-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="56033-120">**Luba väljaregistreerimine ilma maksmiseta**: kui see on lubatud, käsitleb see funktsioon stsenaariumi, kui ostukorvi lisatud kaupadel on hind 0,00 dollarit.</span><span class="sxs-lookup"><span data-stu-id="56033-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="56033-121">**Loo klient asünkroonses režiimis**: see on pärandseadistus, mis on kohaldatav kolmanda poole e-Commerce’i kanalitele ja ei rakendata Dynamics 365 e-Commerce’i saidile.</span><span class="sxs-lookup"><span data-stu-id="56033-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56033-122">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="56033-122">Additional resources</span></span>

[<span data-ttu-id="56033-123">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="56033-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="56033-124">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="56033-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="56033-125">Veebikanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="56033-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="56033-126">Jaemüügikanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="56033-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="56033-127">Kõnekeskuse kanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="56033-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)
