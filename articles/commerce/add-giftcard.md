---
title: Kinkekaardi moodul
description: See teema hõlmab kinkekaardi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9626f33ced0433bc96ed58429e95d4f75af6508
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980378"
---
# <a name="gift-card-module"></a><span data-ttu-id="d2d85-103">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="d2d85-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d2d85-104">See teema hõlmab kinkekaardi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="d2d85-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d2d85-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="d2d85-105">Overview</span></span>

<span data-ttu-id="d2d85-106">Kinkekaardid on levinud makseviis e-Commerce’i tehingute korral ja kinkekaardi moodulit saab kasutada kassa moodulites kinkekaartide vastuvõtmiseks.</span><span class="sxs-lookup"><span data-stu-id="d2d85-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="d2d85-107">Kinkekaardi moodul toetab Dynamics 365, SVS-i ja Givexi kinkekaarte.</span><span class="sxs-lookup"><span data-stu-id="d2d85-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="d2d85-108">SVS-i ja Givexi kinkekaarte lunastatakse Adyen maksepakkuja kaudu.</span><span class="sxs-lookup"><span data-stu-id="d2d85-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="d2d85-109">Lisatebe saamiseks väliste kinkekaartide (nt SVS ja Givex) toe kohta vt [Väliste kinkekaartide tugi](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="d2d85-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d2d85-110">SVS-i ja Givexi kinkekaartide lunastamise tugi maksmisvoo ajal on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="d2d85-110">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="d2d85-111">Saadaval on kaks kinkekaardi moodulit.</span><span class="sxs-lookup"><span data-stu-id="d2d85-111">There are two gift card modules available:</span></span>

- <span data-ttu-id="d2d85-112">**Kinkekaart** – seda moodulit saab kasutada lehel Kassa, et lunastada kinkekaart maksevahendina.</span><span class="sxs-lookup"><span data-stu-id="d2d85-112">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="d2d85-113">**Kinkekaardi saldo vaatamine** – seda moodulit saab kasutada mis tahes leheküljel, et kuvada kinkekaardi saldot.</span><span class="sxs-lookup"><span data-stu-id="d2d85-113">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="d2d85-114">See moodul on saadaval Commerce’i väljaandes 10.0.14 ja uuemas.</span><span class="sxs-lookup"><span data-stu-id="d2d85-114">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="d2d85-115">Kinkekaardi saldo kontroll-mooduli tugi on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="d2d85-115">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="d2d85-116">Järgmisel pildil on näide kinkekaardi moodulist maksmise lehel.</span><span class="sxs-lookup"><span data-stu-id="d2d85-116">The following image shows an example of a gift card module on a checkout page.</span></span>

![Kinkekaardi mooduli näide](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="d2d85-118">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="d2d85-118">Module properties</span></span>

- <span data-ttu-id="d2d85-119">**Kuva lisaväljad** – see atribuut määratleb, millised kinkekaardi väljad tuleks kuvada peale kinkekaardi numbri, mida kuvatakse vaikimisi alati.</span><span class="sxs-lookup"><span data-stu-id="d2d85-119">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="d2d85-120">Näiteks osad kinkekaardid toetavad isikliku ID-numbri (PIN-koodi) kuvamist ja osad toetavad PIN-koodi ja aegumiskuupäeva kuvamist.</span><span class="sxs-lookup"><span data-stu-id="d2d85-120">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="d2d85-121">Selle atripuudi väärtuseks võib määrata ka „Puudub”, mis tähendab, et kuvatakse ainult kinkekaardi number ilma täiendavate väljadeta.</span><span class="sxs-lookup"><span data-stu-id="d2d85-121">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="d2d85-122">Toetatud väärtused.</span><span class="sxs-lookup"><span data-stu-id="d2d85-122">Supported values:</span></span>
-   <span data-ttu-id="d2d85-123">PIN</span><span class="sxs-lookup"><span data-stu-id="d2d85-123">PIN</span></span>
-   <span data-ttu-id="d2d85-124">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="d2d85-124">Expiration date</span></span>
-   <span data-ttu-id="d2d85-125">PIN-kood ja aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="d2d85-125">PIN and expiration date</span></span> 
-   <span data-ttu-id="d2d85-126">None</span><span class="sxs-lookup"><span data-stu-id="d2d85-126">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="d2d85-127">Kinkekaardi moodulite saidisätted</span><span class="sxs-lookup"><span data-stu-id="d2d85-127">Site settings for gift card modules</span></span>

<span data-ttu-id="d2d85-128">Commerce'i saidiehitaja jaotises **Saidi sätted \> Laiendused** on kinkekaardi mooduli säte nimega **Toetatud kinkekaardi tüüp**.</span><span class="sxs-lookup"><span data-stu-id="d2d85-128">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="d2d85-129">See säte toetab kolme väärtust.</span><span class="sxs-lookup"><span data-stu-id="d2d85-129">This setting supports three values:</span></span>
- <span data-ttu-id="d2d85-130">**Dynamics 365 kinkekaart** – selle sätte rakendamisel lubab kinkekaardi moodul ainult Dynamics 365 kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="d2d85-130">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="d2d85-131">See säte on toetatud ainult e-kaubanduse saidi sisselogitud kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="d2d85-131">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="d2d85-132">**SVS-i ja Givexi kinkekaardid** – selle sätte rakendamisel lubab kinkekaardi moodul ainult Givexi ja SVS-i kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="d2d85-132">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="d2d85-133">See säte on toetatud e-kaubanduse saidi sisselogitud ja anonüümsete kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="d2d85-133">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="d2d85-134">**Dynamics 365, SVS-i ja Givexi kinkekaardid** – selle sätte rakendamisel lubab kinkekaardi moodul Dynamics 365, Givexi ja SVS-i kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="d2d85-134">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="d2d85-135">See säte on toetatud ainult e-kaubanduse saidi sisselogitud kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="d2d85-135">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d2d85-136">Need sätted on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.11 ning on vajalikud ainult juhul, kui vajate tuge SVS-i või Givexi kinkekaartide jaoks.</span><span class="sxs-lookup"><span data-stu-id="d2d85-136">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="d2d85-137">Kui värskendate rakenduse Dynamics 365 Commerce varasemast versioonist, peate faili appsettings.json käsitsi värskendama.</span><span class="sxs-lookup"><span data-stu-id="d2d85-137">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="d2d85-138">Faili appsettings.json värskendamise juhised leiate teemast [SDK ja mooduliteegi värskendused](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="d2d85-138">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="d2d85-139">Lehele kinkekaardi mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="d2d85-139">Add a gift card module to a page</span></span>

<span data-ttu-id="d2d85-140">Juhiste saamiseks kinkekaardi mooduli lisamiseks kassa lehele ja nõutavate atribuutide määramiseks, vt [Kassa moodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="d2d85-140">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d2d85-141">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d2d85-141">Additional resources</span></span>

[<span data-ttu-id="d2d85-142">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="d2d85-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d2d85-143">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="d2d85-143">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="d2d85-144">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="d2d85-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d2d85-145">Makse moodul</span><span class="sxs-lookup"><span data-stu-id="d2d85-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="d2d85-146">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="d2d85-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="d2d85-147">Tarnesuvandite moodul</span><span class="sxs-lookup"><span data-stu-id="d2d85-147">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="d2d85-148">Järeletulemisteabe moodul</span><span class="sxs-lookup"><span data-stu-id="d2d85-148">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="d2d85-149">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="d2d85-149">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d2d85-150">Väliste kinkekaartide tugi</span><span class="sxs-lookup"><span data-stu-id="d2d85-150">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="d2d85-151">SDK ja mooduliteegi värskendused</span><span class="sxs-lookup"><span data-stu-id="d2d85-151">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
