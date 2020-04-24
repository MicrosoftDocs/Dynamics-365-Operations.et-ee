---
title: Kinkekaardi moodul
description: See teema hõlmab kinkekaardi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 70047376cec44523cc9cfe4df792bde23c776d8c
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261563"
---
# <a name="gift-card-module"></a><span data-ttu-id="ce3ac-103">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="ce3ac-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ce3ac-104">See teema hõlmab kinkekaardi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ce3ac-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="ce3ac-105">Overview</span></span>

<span data-ttu-id="ce3ac-106">Kinkekaardid on levinud makseviis ja kinkekaardi moodulit saab kasutada kassas kinkekaartide vastuvõtmiseks.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="ce3ac-107">Kinkekaardi moodul toetab Dynamics 365, SVS-i ja Givexi kinkekaarte.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="ce3ac-108">SVS-i ja Givexi kinkekaarte lunastatakse Adyen maksepakkuja kaudu.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="ce3ac-109">Lisatebe saamiseks väliste kinkekaartide (nt SVS ja Givex) toe kohta vt [Väliste kinkekaartide tugi](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="ce3ac-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

## <a name="module-properties"></a><span data-ttu-id="ce3ac-110">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="ce3ac-110">Module properties</span></span>

- <span data-ttu-id="ce3ac-111">**Kuva lisaväljad** – see atribuut määratleb, millised kinkekaardi väljad tuleks kuvada peale kinkekaardi numbri, mida kuvatakse vaikimisi alati.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-111">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="ce3ac-112">Näiteks osad kinkekaardid toetavad isikliku ID-numbri (PIN-koodi) kuvamist ja osad toetavad PIN-koodi ja aegumiskuupäeva kuvamist.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-112">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="ce3ac-113">Selle atripuudi väärtuseks võib määrata ka „Puudub”, mis tähendab, et kuvatakse ainult kinkekaardi number ilma täiendavate väljadeta.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-113">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="ce3ac-114">Toetatud väärtused.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-114">Supported values:</span></span>
-   <span data-ttu-id="ce3ac-115">PIN</span><span class="sxs-lookup"><span data-stu-id="ce3ac-115">PIN</span></span>
-   <span data-ttu-id="ce3ac-116">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="ce3ac-116">Expiration date</span></span>
-   <span data-ttu-id="ce3ac-117">PIN-kood ja aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="ce3ac-117">PIN and expiration date</span></span> 
-   <span data-ttu-id="ce3ac-118">None</span><span class="sxs-lookup"><span data-stu-id="ce3ac-118">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="ce3ac-119">Kinkekaardi moodulite saidisätted</span><span class="sxs-lookup"><span data-stu-id="ce3ac-119">Site settings for gift card modules</span></span>

<span data-ttu-id="ce3ac-120">Commerce'i saidiehitaja jaotises **Saidi sätted \> Laiendused** on kinkekaardi mooduli säte nimega **Toetatud kinkekaardi tüüp**.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-120">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="ce3ac-121">See säte toetab kolme väärtust.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-121">This setting supports three values:</span></span>
- <span data-ttu-id="ce3ac-122">**Dynamics 365 kinkekaart** – selle sätte rakendamisel lubab kinkekaardi moodul ainult Dynamics 365 kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-122">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="ce3ac-123">See säte on toetatud ainult e-kaubanduse saidi sisselogitud kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-123">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="ce3ac-124">**SVS-i ja Givexi kinkekaardid** – selle sätte rakendamisel lubab kinkekaardi moodul ainult Givexi ja SVS-i kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-124">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="ce3ac-125">See säte on toetatud e-kaubanduse saidi sisselogitud ja anonüümsete kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-125">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="ce3ac-126">**Dynamics 365, SVS-i ja Givexi kinkekaardid** – selle sätte rakendamisel lubab kinkekaardi moodul Dynamics 365, Givexi ja SVS-i kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-126">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="ce3ac-127">See säte on toetatud ainult e-kaubanduse saidi sisselogitud kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="ce3ac-127">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="ce3ac-128">Lehele kinkekaardi mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="ce3ac-128">Add a gift card module to a page</span></span>

<span data-ttu-id="ce3ac-129">Juhiste saamiseks kinkekaardi mooduli lisamiseks kassa lehele ja nõutavate atribuutide määramiseks, vt [Kassa moodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="ce3ac-129">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce3ac-130">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ce3ac-130">Additional resources</span></span>

[<span data-ttu-id="ce3ac-131">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="ce3ac-131">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ce3ac-132">Väljaregistreerimismoodul</span><span class="sxs-lookup"><span data-stu-id="ce3ac-132">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="ce3ac-133">Väliste kinkekaartide tugi</span><span class="sxs-lookup"><span data-stu-id="ce3ac-133">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
