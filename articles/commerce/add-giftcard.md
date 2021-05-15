---
title: Kinkekaardi moodul
description: See teema hõlmab kinkekaardi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
ms.date: 04/29/2021
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
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962759"
---
# <a name="gift-card-module"></a><span data-ttu-id="a3bd2-103">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="a3bd2-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a3bd2-104">See teema hõlmab kinkekaardi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a3bd2-105">Kinkekaardid on levinud makseviis e-Commerce’i tehingute korral ja kinkekaardi moodulit saab kasutada kassa moodulites kinkekaartide vastuvõtmiseks.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="a3bd2-106">Kinkekaardi moodul toetab Dynamics 365, SVS-i ja Givexi kinkekaarte.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="a3bd2-107">SVS-i ja Givexi kinkekaarte lunastatakse Adyen maksepakkuja kaudu.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="a3bd2-108">Lisatebe saamiseks väliste kinkekaartide (nt SVS ja Givex) toe kohta vt [Väliste kinkekaartide tugi](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="a3bd2-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a3bd2-109">SVS-i ja Givexi kinkekaartide lunastamise tugi maksmisvoo ajal on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="a3bd2-110">Saadaval on kaks kinkekaardi moodulit.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="a3bd2-111">**Kinkekaart** – seda moodulit saab kasutada kassalehel, et lunastada kinkekaart maksevahendina.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-111">**Gift card** – This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="a3bd2-112">**Kinkekaardi saldo vaatamine** – seda moodulit saab kasutada mis tahes leheküljel, et kuvada kinkekaardi saldot.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-112">**Gift card balance check** – This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="a3bd2-113">See moodul on saadaval Commerce’i väljaandes 10.0.14 ja uuemas.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="a3bd2-114">Kinkekaardi saldo kontroll-mooduli tugi on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="a3bd2-115">Järgmisel pildil on näide kinkekaardi moodulist maksmise lehel.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Kinkekaardi mooduli näide](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="a3bd2-117">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="a3bd2-117">Module properties</span></span>

- <span data-ttu-id="a3bd2-118">**Kuva lisavälju** – see atribuut määratleb, millised kinkekaardi väljad tuleks kuvada peale kinkekaardi numbri, mida kuvatakse vaikimisi alati.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-118">**Show additional fields** – This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="a3bd2-119">Näiteks osad kinkekaardid toetavad isikliku ID-numbri (PIN-koodi) kuvamist ja osad toetavad PIN-koodi ja aegumiskuupäeva kuvamist.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="a3bd2-120">Selle atripuudi väärtuseks võib määrata ka „Puudub”, mis tähendab, et kuvatakse ainult kinkekaardi number ilma täiendavate väljadeta.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="a3bd2-121">Toetatud väärtused.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-121">Supported values:</span></span>
-   <span data-ttu-id="a3bd2-122">PIN</span><span class="sxs-lookup"><span data-stu-id="a3bd2-122">PIN</span></span>
-   <span data-ttu-id="a3bd2-123">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="a3bd2-123">Expiration date</span></span>
-   <span data-ttu-id="a3bd2-124">PIN-kood ja aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="a3bd2-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="a3bd2-125">None</span><span class="sxs-lookup"><span data-stu-id="a3bd2-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="a3bd2-126">Kinkekaardi moodulite saidisätted</span><span class="sxs-lookup"><span data-stu-id="a3bd2-126">Site settings for gift card modules</span></span>

<span data-ttu-id="a3bd2-127">Commerce'i saidiehitaja jaotises **Saidi sätted \> Laiendused** on kinkekaardi mooduli säte nimega **Toetatud kinkekaardi tüüp**.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="a3bd2-128">See säte toetab kolme väärtust.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-128">This setting supports three values:</span></span>
- <span data-ttu-id="a3bd2-129">**Dynamics 365 kinkekaart** – selle sätte rakendamisel lubab kinkekaardi moodul ainult Dynamics 365 kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-129">**Dynamics 365 gift card** – When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="a3bd2-130">See säte on toetatud ainult e-kaubanduse saidi sisselogitud kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="a3bd2-131">**SVS-i ja Givexi kinkekaardid** – selle sätte rakendamisel lubab kinkekaardi moodul ainult Givexi ja SVS-i kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-131">**SVS and Givex gift cards** – When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="a3bd2-132">See säte on toetatud e-kaubanduse saidi sisselogitud ja anonüümsete kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="a3bd2-133">**Dynamics 365, SVS-i ja Givexi kinkekaardid** – selle sätte rakendamisel lubab kinkekaardi moodul Dynamics 365, Givexi ja SVS-i kinkekaartide lunastamist.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-133">**Dynamics 365, SVS, and Givex gift cards** – When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="a3bd2-134">See säte on toetatud ainult e-kaubanduse saidi sisselogitud kasutajate puhul.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a3bd2-135">Need sätted on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.11 ning on vajalikud ainult juhul, kui vajate tuge SVS-i või Givexi kinkekaartide jaoks.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="a3bd2-136">Kui värskendate rakenduse Dynamics 365 Commerce varasemast versioonist, peate faili appsettings.json käsitsi värskendama.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="a3bd2-137">Faili appsettings.json värskendamise juhised leiate teemast [SDK ja mooduliteegi värskendused](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="a3bd2-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a><span data-ttu-id="a3bd2-138">Sisemiste kinkekaartide laiendamine e-kaubanduses kasutamiseks</span><span class="sxs-lookup"><span data-stu-id="a3bd2-138">Extend internal gift cards for use in e-commerce storefronts</span></span>

<span data-ttu-id="a3bd2-139">Vaikimisi ei ole sisemised kinkekaardid e-kaubanduses kasutamiseks optimeeritud.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-139">By default, internal gift cards aren't optimized for use in e-commerce storefronts.</span></span> <span data-ttu-id="a3bd2-140">Seetõttu peate enne sisemiste kinkekaartide maksmiseks kasutamiseks lubamist konfigureerima need laienditega, mis aitavad neid turvalisemaks muuta.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-140">Therefore, before you allow internal gift cards to be used for payment, you should configure them with extensions that help make them more secure.</span></span> <span data-ttu-id="a3bd2-141">Siin on kinkekaardi alad, mida peate laiendama enne, kui lubate sisemiste kinkekaartide kasutamist tootmises.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-141">Here are the gift card areas that you should extend before you allow internal gift cards to be used in production:</span></span>

- <span data-ttu-id="a3bd2-142">**Kinkekaardi number** – numbriseeriaid kasutatakse sisemiste kinkekaartide jaoks kinkekaardi numbrite loomiseks.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-142">**Gift card number** – Number sequences are used to generate gift card numbers for internal gift cards.</span></span> <span data-ttu-id="a3bd2-143">Kuna numbriseeriaid on lihtne prognoosida, peaksite laiendama kinkekaardi numbrite genereerimist nii, et väljastatud kinkekaardi numbrite jaoks kasutatakse juhuslikke krüptograafiliselt turvalisi stringe.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-143">Because number sequences can easily be predicted, you should extend the generation of gift card numbers so that random, cryptographically secure strings are used for the gift card numbers that are issued.</span></span>
- <span data-ttu-id="a3bd2-144">**GetBalance** – **GetBalance** API-d kasutatakse kinkekaardi saldode otsimiseks.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-144">**GetBalance** – The **GetBalance** API is used to look up gift card balances.</span></span> <span data-ttu-id="a3bd2-145">Vaikimisi on see API avalik.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-145">By default, this API public.</span></span> <span data-ttu-id="a3bd2-146">Kui PIN-ilt ei nõuta kinkekaardi saldode otsimist, võib brute force-ründed kasutada **GetBalance** API-d saldodega kinkekaardi numbrite otsimiseks.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-146">If a PIN isn't required to look up gift card balances, there is a risk that brute force attacks could use the **GetBalance** API to try to look up gift card numbers that have balances.</span></span> <span data-ttu-id="a3bd2-147">Rakendades nii sisemiste kinkekaartide kui API drosselimise PIN-i nõudeid, saate riski leevendada.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-147">By implementing both PIN requirements for internal gift cards and API throttling, you can help mitigate the risk.</span></span>
- <span data-ttu-id="a3bd2-148">**PIN** – vaikimisi ei toeta sisemised kinkekaardid PIN-e.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-148">**PIN** – By default, internal gift cards don't support PINs.</span></span> <span data-ttu-id="a3bd2-149">Ettevõttesiseseid kinkekaarte tuleb laiendada nii, et saldode otsimiseks on vajalik PIN.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-149">You should extend internal gift cards so that a PIN is required to look up balances.</span></span> <span data-ttu-id="a3bd2-150">Seda funktsiooni saab kasutada ka kinkekaartide lukustamiseks pärast järjestikuste PIN-koodi vale sisestamise katseid.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-150">This functionality can also be used to lock gift cards after consecutive incorrect attempts to enter the PIN.</span></span>

## <a name="enable-gift-card-payments-for-guest-checkout"></a><span data-ttu-id="a3bd2-151">Lubage kinkekaardi maksed külalise väljaregistreerimiseks</span><span class="sxs-lookup"><span data-stu-id="a3bd2-151">Enable gift card payments for guest checkout</span></span>

<span data-ttu-id="a3bd2-152">Vaikimisi ei ole kinkekaardimaksed lubatud külalise (anonüümse) väljaregistreerimise jaoks.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-152">By default, gift card payments aren't enabled for guest (anonymous) checkout.</span></span> <span data-ttu-id="a3bd2-153">Nende lubamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-153">To enable them, follow these steps.</span></span>

1. <span data-ttu-id="a3bd2-154">Commerce'i Headquartersis minge asukohta **Jaemüük ja kaubandus \> Kanali seadistamine \> POSi seadistamine \> POS \> POSi operatsioonid**.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-154">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS Operations**.</span></span>
1. <span data-ttu-id="a3bd2-155">Valige ja hoidke all (või paremklõpsake) ruudustiku päist ning valige käsk **Lisa veerud**.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-155">Select and hold (or right-click) the header of the grid, and then select **Insert columns**.</span></span>
1. <span data-ttu-id="a3bd2-156">Dialoogiaknas **Veergude lisamine** valige märkeruut **AllowAnonymousAccess**.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-156">In the **Insert columns** dialog box, select the **AllowAnonymousAccess** check box.</span></span>
1. <span data-ttu-id="a3bd2-157">Tehke valik **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-157">Select **Update**.</span></span>
1. <span data-ttu-id="a3bd2-158">Toimingute **520** (kinkekaardi saldo) ja **214** puhul seadke välja **AllowAnonymousAccess** väärtuseks **1**.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-158">For operations **520** (Gift card balance) and **214**, set the **AllowAnonymousAccess** value to **1**.</span></span>
1. <span data-ttu-id="a3bd2-159">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-159">Select **Save**.</span></span>
1. <span data-ttu-id="a3bd2-160">Käivitage jaotusgraafik **1090** muudatuste sünkroonimiseks kanali andmebaasiga.</span><span class="sxs-lookup"><span data-stu-id="a3bd2-160">Run the **1090** scheduler job to sync changes to the channel database.</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="a3bd2-161">Lehele kinkekaardi mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="a3bd2-161">Add a gift card module to a page</span></span>

<span data-ttu-id="a3bd2-162">Juhiste saamiseks kinkekaardi mooduli lisamiseks kassa lehele ja nõutavate atribuutide määramiseks, vt [Kassa moodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="a3bd2-162">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a3bd2-163">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a3bd2-163">Additional resources</span></span>

[<span data-ttu-id="a3bd2-164">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="a3bd2-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a3bd2-165">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="a3bd2-165">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="a3bd2-166">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="a3bd2-166">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a3bd2-167">Makse moodul</span><span class="sxs-lookup"><span data-stu-id="a3bd2-167">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="a3bd2-168">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="a3bd2-168">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="a3bd2-169">Tarnesuvandite moodul</span><span class="sxs-lookup"><span data-stu-id="a3bd2-169">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="a3bd2-170">Järeletulemisteabe moodul</span><span class="sxs-lookup"><span data-stu-id="a3bd2-170">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="a3bd2-171">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="a3bd2-171">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a3bd2-172">Väliste kinkekaartide tugi</span><span class="sxs-lookup"><span data-stu-id="a3bd2-172">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="a3bd2-173">SDK ja mooduliteegi värskendused</span><span class="sxs-lookup"><span data-stu-id="a3bd2-173">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
