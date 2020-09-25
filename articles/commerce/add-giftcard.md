---
title: Kinkekaardi moodul
description: See teema hõlmab kinkekaardi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 4cc947b9d6f3cfa51bce2155170c49e9529d0f7d
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761077"
---
# <a name="gift-card-module"></a><span data-ttu-id="4a972-103">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="4a972-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="4a972-104">See teema hõlmab kinkekaardi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="4a972-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4a972-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="4a972-105">Overview</span></span>

<span data-ttu-id="4a972-106">Kinkekaardid on levinud makseviis e-Commerce’i tehingute korral ja kinkekaardi moodulit saab kasutada kassa moodulites kinkekaartide vastuvõtmiseks.</span><span class="sxs-lookup"><span data-stu-id="4a972-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="4a972-107">Kinkekaardi moodul toetab Dynamics 365, SVS-i ja Givexi kinkekaarte.</span><span class="sxs-lookup"><span data-stu-id="4a972-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="4a972-108">SVS-i ja Givexi kinkekaarte lunastatakse Adyen maksepakkuja kaudu.</span><span class="sxs-lookup"><span data-stu-id="4a972-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="4a972-109">Lisatebe saamiseks väliste kinkekaartide (nt SVS ja Givex) toe kohta vt [Väliste kinkekaartide tugi](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="4a972-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

<span data-ttu-id="4a972-110">Saadaval on kaks kinkekaardi moodulit.</span><span class="sxs-lookup"><span data-stu-id="4a972-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="4a972-111">**Kinkekaart** – seda moodulit saab kasutada lehel Kassa, et lunastada kinkekaart maksevahendina.</span><span class="sxs-lookup"><span data-stu-id="4a972-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="4a972-112">**Kinkekaardi saldo vaatamine** – seda moodulit saab kasutada mis tahes leheküljel, et kuvada kinkekaardi saldot.</span><span class="sxs-lookup"><span data-stu-id="4a972-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="4a972-113">See moodul on saadaval Commerce’i väljaandes 10.0.14 ja uuemas.</span><span class="sxs-lookup"><span data-stu-id="4a972-113">This module is available in Commerce release 10.0.14 and later.</span></span>

<span data-ttu-id="4a972-114">Järgmisel pildil on näide kinkekaardi moodulist maksmise lehel.</span><span class="sxs-lookup"><span data-stu-id="4a972-114">The following image shows an example of a gift card module on a checkout page.</span></span>

![Kinkekaardi mooduli näide](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="4a972-116">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="4a972-116">Module properties</span></span>

- <span data-ttu-id="4a972-117">**Kuva lisaväljad** – see atribuut määratleb, millised kinkekaardi väljad tuleks kuvada peale kinkekaardi numbri, mida kuvatakse vaikimisi alati.</span><span class="sxs-lookup"><span data-stu-id="4a972-117">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="4a972-118">Näiteks osad kinkekaardid toetavad isikliku ID-numbri (PIN-koodi) kuvamist ja osad toetavad PIN-koodi ja aegumiskuupäeva kuvamist.</span><span class="sxs-lookup"><span data-stu-id="4a972-118">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="4a972-119">Selle atripuudi väärtuseks võib määrata ka „Puudub”, mis tähendab, et kuvatakse ainult kinkekaardi number ilma täiendavate väljadeta.</span><span class="sxs-lookup"><span data-stu-id="4a972-119">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="4a972-120">Toetatud väärtused.</span><span class="sxs-lookup"><span data-stu-id="4a972-120">Supported values:</span></span>
-   <span data-ttu-id="4a972-121">PIN</span><span class="sxs-lookup"><span data-stu-id="4a972-121">PIN</span></span>
-   <span data-ttu-id="4a972-122">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="4a972-122">Expiration date</span></span>
-   <span data-ttu-id="4a972-123">PIN-kood ja aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="4a972-123">PIN and expiration date</span></span> 
-   <span data-ttu-id="4a972-124">None</span><span class="sxs-lookup"><span data-stu-id="4a972-124">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="4a972-125">Kinkekaardi moodulite saidisätted</span><span class="sxs-lookup"><span data-stu-id="4a972-125">Site settings for gift card modules</span></span>

<span data-ttu-id="4a972-126">Commerce'i saidiehitaja jaotises **Saidi sätted \> Laiendused** on kinkekaardi mooduli säte nimega **Toetatud kinkekaardi tüüp**.</span><span class="sxs-lookup"><span data-stu-id="4a972-126">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="4a972-127">See säte toetab kolme väärtust.</span><span class="sxs-lookup"><span data-stu-id="4a972-127">This setting supports three values:</span></span>
- <span data-ttu-id="4a972-128">**Dynamics 365 kinkekaart** – selle sätte rakendamisel lubab kinkekaardi moodul ainult Dynamics 365 kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="4a972-128">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="4a972-129">See säte on toetatud ainult e-kaubanduse saidi sisselogitud kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="4a972-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="4a972-130">**SVS-i ja Givexi kinkekaardid** – selle sätte rakendamisel lubab kinkekaardi moodul ainult Givexi ja SVS-i kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="4a972-130">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="4a972-131">See säte on toetatud e-kaubanduse saidi sisselogitud ja anonüümsete kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="4a972-131">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="4a972-132">**Dynamics 365, SVS-i ja Givexi kinkekaardid** – selle sätte rakendamisel lubab kinkekaardi moodul Dynamics 365, Givexi ja SVS-i kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="4a972-132">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="4a972-133">See säte on toetatud ainult e-kaubanduse saidi sisselogitud kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="4a972-133">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="4a972-134">Lehele kinkekaardi mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="4a972-134">Add a gift card module to a page</span></span>

<span data-ttu-id="4a972-135">Juhiste saamiseks kinkekaardi mooduli lisamiseks kassa lehele ja nõutavate atribuutide määramiseks, vt [Kassa moodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="4a972-135">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4a972-136">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4a972-136">Additional resources</span></span>

[<span data-ttu-id="4a972-137">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="4a972-137">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4a972-138">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="4a972-138">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="4a972-139">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="4a972-139">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="4a972-140">Maksemoodul</span><span class="sxs-lookup"><span data-stu-id="4a972-140">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="4a972-141">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="4a972-141">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="4a972-142">Tarnevalikute moodul</span><span class="sxs-lookup"><span data-stu-id="4a972-142">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="4a972-143">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="4a972-143">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="4a972-144">Väliste kinkekaartide tugi</span><span class="sxs-lookup"><span data-stu-id="4a972-144">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
