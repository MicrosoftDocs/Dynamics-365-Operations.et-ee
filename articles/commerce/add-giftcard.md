---
title: Kinkekaardi moodul
description: See teema hõlmab kinkekaardi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 41f808d671bf5e7425390484ea30470e044899d8
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661238"
---
# <a name="gift-card-module"></a><span data-ttu-id="84e02-103">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="84e02-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="84e02-104">See teema hõlmab kinkekaardi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="84e02-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="84e02-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="84e02-105">Overview</span></span>

<span data-ttu-id="84e02-106">Kinkekaardid on levinud makseviis ja kinkekaardi moodulit saab kasutada kassas kinkekaartide vastuvõtmiseks.</span><span class="sxs-lookup"><span data-stu-id="84e02-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="84e02-107">Kinkekaardi moodul toetab Dynamics 365, SVS-i ja Givexi kinkekaarte.</span><span class="sxs-lookup"><span data-stu-id="84e02-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="84e02-108">SVS-i ja Givexi kinkekaarte lunastatakse Adyen maksepakkuja kaudu.</span><span class="sxs-lookup"><span data-stu-id="84e02-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="84e02-109">Lisatebe saamiseks väliste kinkekaartide (nt SVS ja Givex) toe kohta vt [Väliste kinkekaartide tugi](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="84e02-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

<span data-ttu-id="84e02-110">Järgmisel pildil on näide kinkekaardi moodulist maksmise lehel.</span><span class="sxs-lookup"><span data-stu-id="84e02-110">The following image shows an example of a gift card module on a checkout page.</span></span>

![Kinkekaardi mooduli näide](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="84e02-112">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="84e02-112">Module properties</span></span>

- <span data-ttu-id="84e02-113">**Kuva lisaväljad** – see atribuut määratleb, millised kinkekaardi väljad tuleks kuvada peale kinkekaardi numbri, mida kuvatakse vaikimisi alati.</span><span class="sxs-lookup"><span data-stu-id="84e02-113">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="84e02-114">Näiteks osad kinkekaardid toetavad isikliku ID-numbri (PIN-koodi) kuvamist ja osad toetavad PIN-koodi ja aegumiskuupäeva kuvamist.</span><span class="sxs-lookup"><span data-stu-id="84e02-114">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="84e02-115">Selle atripuudi väärtuseks võib määrata ka „Puudub”, mis tähendab, et kuvatakse ainult kinkekaardi number ilma täiendavate väljadeta.</span><span class="sxs-lookup"><span data-stu-id="84e02-115">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="84e02-116">Toetatud väärtused.</span><span class="sxs-lookup"><span data-stu-id="84e02-116">Supported values:</span></span>
-   <span data-ttu-id="84e02-117">PIN</span><span class="sxs-lookup"><span data-stu-id="84e02-117">PIN</span></span>
-   <span data-ttu-id="84e02-118">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="84e02-118">Expiration date</span></span>
-   <span data-ttu-id="84e02-119">PIN-kood ja aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="84e02-119">PIN and expiration date</span></span> 
-   <span data-ttu-id="84e02-120">None</span><span class="sxs-lookup"><span data-stu-id="84e02-120">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="84e02-121">Kinkekaardi moodulite saidisätted</span><span class="sxs-lookup"><span data-stu-id="84e02-121">Site settings for gift card modules</span></span>

<span data-ttu-id="84e02-122">Commerce'i saidiehitaja jaotises **Saidi sätted \> Laiendused** on kinkekaardi mooduli säte nimega **Toetatud kinkekaardi tüüp**.</span><span class="sxs-lookup"><span data-stu-id="84e02-122">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="84e02-123">See säte toetab kolme väärtust.</span><span class="sxs-lookup"><span data-stu-id="84e02-123">This setting supports three values:</span></span>
- <span data-ttu-id="84e02-124">**Dynamics 365 kinkekaart** – selle sätte rakendamisel lubab kinkekaardi moodul ainult Dynamics 365 kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="84e02-124">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="84e02-125">See säte on toetatud ainult e-kaubanduse saidi sisselogitud kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="84e02-125">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="84e02-126">**SVS-i ja Givexi kinkekaardid** – selle sätte rakendamisel lubab kinkekaardi moodul ainult Givexi ja SVS-i kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="84e02-126">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="84e02-127">See säte on toetatud e-kaubanduse saidi sisselogitud ja anonüümsete kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="84e02-127">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="84e02-128">**Dynamics 365, SVS-i ja Givexi kinkekaardid** – selle sätte rakendamisel lubab kinkekaardi moodul Dynamics 365, Givexi ja SVS-i kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="84e02-128">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="84e02-129">See säte on toetatud ainult e-kaubanduse saidi sisselogitud kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="84e02-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="84e02-130">Lehele kinkekaardi mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="84e02-130">Add a gift card module to a page</span></span>

<span data-ttu-id="84e02-131">Juhiste saamiseks kinkekaardi mooduli lisamiseks kassa lehele ja nõutavate atribuutide määramiseks, vt [Kassa moodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="84e02-131">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="84e02-132">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="84e02-132">Additional resources</span></span>

[<span data-ttu-id="84e02-133">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="84e02-133">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="84e02-134">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="84e02-134">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="84e02-135">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="84e02-135">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="84e02-136">Maksemoodul</span><span class="sxs-lookup"><span data-stu-id="84e02-136">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="84e02-137">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="84e02-137">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="84e02-138">Tarnevalikute moodul</span><span class="sxs-lookup"><span data-stu-id="84e02-138">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="84e02-139">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="84e02-139">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="84e02-140">Väliste kinkekaartide tugi</span><span class="sxs-lookup"><span data-stu-id="84e02-140">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
