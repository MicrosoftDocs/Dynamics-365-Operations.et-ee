---
title: Kinkekaardi moodul
description: See teema hõlmab kinkekaardi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a4e4e06ab7032d68fcd36a8e80bc714ebaaac821
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797667"
---
# <a name="gift-card-module"></a><span data-ttu-id="4407f-103">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="4407f-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4407f-104">See teema hõlmab kinkekaardi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="4407f-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4407f-105">Kinkekaardid on levinud makseviis e-Commerce’i tehingute korral ja kinkekaardi moodulit saab kasutada kassa moodulites kinkekaartide vastuvõtmiseks.</span><span class="sxs-lookup"><span data-stu-id="4407f-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="4407f-106">Kinkekaardi moodul toetab Dynamics 365, SVS-i ja Givexi kinkekaarte.</span><span class="sxs-lookup"><span data-stu-id="4407f-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="4407f-107">SVS-i ja Givexi kinkekaarte lunastatakse Adyen maksepakkuja kaudu.</span><span class="sxs-lookup"><span data-stu-id="4407f-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="4407f-108">Lisatebe saamiseks väliste kinkekaartide (nt SVS ja Givex) toe kohta vt [Väliste kinkekaartide tugi](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="4407f-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4407f-109">SVS-i ja Givexi kinkekaartide lunastamise tugi maksmisvoo ajal on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="4407f-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="4407f-110">Saadaval on kaks kinkekaardi moodulit.</span><span class="sxs-lookup"><span data-stu-id="4407f-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="4407f-111">**Kinkekaart** – seda moodulit saab kasutada lehel Kassa, et lunastada kinkekaart maksevahendina.</span><span class="sxs-lookup"><span data-stu-id="4407f-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="4407f-112">**Kinkekaardi saldo vaatamine** – seda moodulit saab kasutada mis tahes leheküljel, et kuvada kinkekaardi saldot.</span><span class="sxs-lookup"><span data-stu-id="4407f-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="4407f-113">See moodul on saadaval Commerce’i väljaandes 10.0.14 ja uuemas.</span><span class="sxs-lookup"><span data-stu-id="4407f-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="4407f-114">Kinkekaardi saldo kontroll-mooduli tugi on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="4407f-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="4407f-115">Järgmisel pildil on näide kinkekaardi moodulist maksmise lehel.</span><span class="sxs-lookup"><span data-stu-id="4407f-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Kinkekaardi mooduli näide](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="4407f-117">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="4407f-117">Module properties</span></span>

- <span data-ttu-id="4407f-118">**Kuva lisaväljad** – see atribuut määratleb, millised kinkekaardi väljad tuleks kuvada peale kinkekaardi numbri, mida kuvatakse vaikimisi alati.</span><span class="sxs-lookup"><span data-stu-id="4407f-118">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="4407f-119">Näiteks osad kinkekaardid toetavad isikliku ID-numbri (PIN-koodi) kuvamist ja osad toetavad PIN-koodi ja aegumiskuupäeva kuvamist.</span><span class="sxs-lookup"><span data-stu-id="4407f-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="4407f-120">Selle atripuudi väärtuseks võib määrata ka „Puudub”, mis tähendab, et kuvatakse ainult kinkekaardi number ilma täiendavate väljadeta.</span><span class="sxs-lookup"><span data-stu-id="4407f-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="4407f-121">Toetatud väärtused.</span><span class="sxs-lookup"><span data-stu-id="4407f-121">Supported values:</span></span>
-   <span data-ttu-id="4407f-122">PIN</span><span class="sxs-lookup"><span data-stu-id="4407f-122">PIN</span></span>
-   <span data-ttu-id="4407f-123">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="4407f-123">Expiration date</span></span>
-   <span data-ttu-id="4407f-124">PIN-kood ja aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="4407f-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="4407f-125">None</span><span class="sxs-lookup"><span data-stu-id="4407f-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="4407f-126">Kinkekaardi moodulite saidisätted</span><span class="sxs-lookup"><span data-stu-id="4407f-126">Site settings for gift card modules</span></span>

<span data-ttu-id="4407f-127">Commerce'i saidiehitaja jaotises **Saidi sätted \> Laiendused** on kinkekaardi mooduli säte nimega **Toetatud kinkekaardi tüüp**.</span><span class="sxs-lookup"><span data-stu-id="4407f-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="4407f-128">See säte toetab kolme väärtust.</span><span class="sxs-lookup"><span data-stu-id="4407f-128">This setting supports three values:</span></span>
- <span data-ttu-id="4407f-129">**Dynamics 365 kinkekaart** – selle sätte rakendamisel lubab kinkekaardi moodul ainult Dynamics 365 kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="4407f-129">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="4407f-130">See säte on toetatud ainult e-kaubanduse saidi sisselogitud kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="4407f-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="4407f-131">**SVS-i ja Givexi kinkekaardid** – selle sätte rakendamisel lubab kinkekaardi moodul ainult Givexi ja SVS-i kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="4407f-131">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="4407f-132">See säte on toetatud e-kaubanduse saidi sisselogitud ja anonüümsete kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="4407f-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="4407f-133">**Dynamics 365, SVS-i ja Givexi kinkekaardid** – selle sätte rakendamisel lubab kinkekaardi moodul Dynamics 365, Givexi ja SVS-i kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="4407f-133">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="4407f-134">See säte on toetatud ainult e-kaubanduse saidi sisselogitud kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="4407f-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4407f-135">Need sätted on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.11 ning on vajalikud ainult juhul, kui vajate tuge SVS-i või Givexi kinkekaartide jaoks.</span><span class="sxs-lookup"><span data-stu-id="4407f-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="4407f-136">Kui värskendate rakenduse Dynamics 365 Commerce varasemast versioonist, peate faili appsettings.json käsitsi värskendama.</span><span class="sxs-lookup"><span data-stu-id="4407f-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="4407f-137">Faili appsettings.json värskendamise juhised leiate teemast [SDK ja mooduliteegi värskendused](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="4407f-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="4407f-138">Lehele kinkekaardi mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="4407f-138">Add a gift card module to a page</span></span>

<span data-ttu-id="4407f-139">Juhiste saamiseks kinkekaardi mooduli lisamiseks kassa lehele ja nõutavate atribuutide määramiseks, vt [Kassa moodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="4407f-139">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4407f-140">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4407f-140">Additional resources</span></span>

[<span data-ttu-id="4407f-141">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="4407f-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4407f-142">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="4407f-142">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="4407f-143">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="4407f-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="4407f-144">Makse moodul</span><span class="sxs-lookup"><span data-stu-id="4407f-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="4407f-145">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="4407f-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="4407f-146">Tarnesuvandite moodul</span><span class="sxs-lookup"><span data-stu-id="4407f-146">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="4407f-147">Järeletulemisteabe moodul</span><span class="sxs-lookup"><span data-stu-id="4407f-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="4407f-148">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="4407f-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="4407f-149">Väliste kinkekaartide tugi</span><span class="sxs-lookup"><span data-stu-id="4407f-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="4407f-150">SDK ja mooduliteegi värskendused</span><span class="sxs-lookup"><span data-stu-id="4407f-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]