---
title: Tarnevalikute moodul
description: See teema hõlmab tarnevalikute mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce konfigureerida.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 1e55ce327e2c8ab714eb5e2fa14b3830b9171688
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020675"
---
# <a name="delivery-options-module"></a><span data-ttu-id="0a185-103">Tarnevalikute moodul</span><span class="sxs-lookup"><span data-stu-id="0a185-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="0a185-104">See teema hõlmab tarnevalikute mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="0a185-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0a185-105">Tarnevalikute moodulid võimaldavad klientidel valida oma veebitellimuse jaoks tarneviisi, nt lähetamise või pealevõtmise.</span><span class="sxs-lookup"><span data-stu-id="0a185-105">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="0a185-106">Tarneviisi määramiseks on vajalik tarneaadress.</span><span class="sxs-lookup"><span data-stu-id="0a185-106">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="0a185-107">Kui tarneaadress muutub, tuleb tarnevalikud uuesti hankida.</span><span class="sxs-lookup"><span data-stu-id="0a185-107">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="0a185-108">Kui tellimus sisaldab ainult kaupu, millele minnakse poodi järele, siis see moodul peidetakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="0a185-108">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="0a185-109">Lisateavet tarneviiside konfigureerimise kohta leiate teemadest [Võrgukanali seadistamine](channel-setup-online.md) ja [Tarneviiside seadistamine](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="0a185-109">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="0a185-110">Igal tarneviisil võib olla seotud kulu.</span><span class="sxs-lookup"><span data-stu-id="0a185-110">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="0a185-111">Lisateavet veebipoe jaoks kulude konfigureerimise kohta leiate teemast [Omnikanali täpsemad automaatsed kulud](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="0a185-111">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="0a185-112">Commerce'i versioonis 10.0.13 värskendati tarnevalikute moodulit, et toetada funktsioone **Päisekulud ilma proportsionaalse jaotamiseta** ja **Lähetamine reakuluna**.</span><span class="sxs-lookup"><span data-stu-id="0a185-112">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="0a185-113">Kui proportsionaalne jaotamine on välja lülitatud, eeldatakse, et e-kaubanduse töövoog ei luba ostukorvis olevate kaupade jaoks valida erinevat tarneviisi (see tähendab, et mõned kaubad määratakse lähetamiseks, kuid teised pealevõtmiseks).</span><span class="sxs-lookup"><span data-stu-id="0a185-113">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="0a185-114">Funktsiooni **Päisekulud ilma proportsionaalse jaotamiseta** jaoks on vajalik, et Commerce'i peakontoris oleks sisse lülitatud lipp **Luba kanalis järjekindel tarneviisi käitlemine**.</span><span class="sxs-lookup"><span data-stu-id="0a185-114">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag is turned on in Commerce headquarters.</span></span> <span data-ttu-id="0a185-115">Kui funktsiooni lipp on sisse lülitatud, rakendatakse saatekulusid kas päise- või reatasemel, sõltuvalt Commerce'i peakontori konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="0a185-115">When the feature flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="0a185-116">Fabrikami kujundus toetab kombineeritud tarneviisi, kus mõni kaup määratakse lähetamiseks, kuid teised pealevõtmiseks.</span><span class="sxs-lookup"><span data-stu-id="0a185-116">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="0a185-117">Selle viisi puhul jaotatakse saatekulud proportsionaalselt kõigi kaupade vahel, mille tarneviis on lähetamine.</span><span class="sxs-lookup"><span data-stu-id="0a185-117">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="0a185-118">Kombineeritud tarneviisi toimimiseks peate Commerce'i peakontoris enne konfigureerima funktsiooni **Päisekulud koos proportsionaalse jaotamisega**.</span><span class="sxs-lookup"><span data-stu-id="0a185-118">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="0a185-119">Lisateavet selle konfiguratsiooni kohta leiate teemast [Päisekulude proportsionaalselt jaotamine müügiridade järgi](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="0a185-119">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="0a185-120">Kui reakaupade puhul rakenduvad saatekulud, saab neid kuvada iga kauba ostukorvireal.</span><span class="sxs-lookup"><span data-stu-id="0a185-120">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="0a185-121">Selle funktsiooni jaoks on vaja, et atribuut **Kuva reakauba saatekulud** oleks nii ostukorvi- kui ka maksmise mooduli puhul sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="0a185-121">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="0a185-122">Lisateavet leiate teemadest [Ostukorvimoodul](add-cart-module.md) ja [Maksmise moodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="0a185-122">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="0a185-123">Järgmisel illustratsioonil on näide tarnevalikute moodulist maksmise lehel.</span><span class="sxs-lookup"><span data-stu-id="0a185-123">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Tarnevalikute mooduli näide maksmise lehel](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="0a185-125">Tarnevalikute mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="0a185-125">Delivery options module properties</span></span>

| <span data-ttu-id="0a185-126">Atribuut</span><span class="sxs-lookup"><span data-stu-id="0a185-126">Property</span></span> | <span data-ttu-id="0a185-127">Väärtused</span><span class="sxs-lookup"><span data-stu-id="0a185-127">Values</span></span> | <span data-ttu-id="0a185-128">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0a185-128">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="0a185-129">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="0a185-129">Heading</span></span> | <span data-ttu-id="0a185-130">Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**)</span><span class="sxs-lookup"><span data-stu-id="0a185-130">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="0a185-131">Tarnevalikute mooduli valikuline pealkiri.</span><span class="sxs-lookup"><span data-stu-id="0a185-131">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="0a185-132">Kohandatud CSS-i klassinimi</span><span class="sxs-lookup"><span data-stu-id="0a185-132">Custom CSS class name</span></span> | <span data-ttu-id="0a185-133">Tekst</span><span class="sxs-lookup"><span data-stu-id="0a185-133">Text</span></span> | <span data-ttu-id="0a185-134">Kaskaadlaadistiku (CSS) kohandatud klassi nimi, mida kasutatakse selle mooduli renderdamiseks, kui seda on vaja.</span><span class="sxs-lookup"><span data-stu-id="0a185-134">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="0a185-135">Tarneviisi valikute filtreerimine</span><span class="sxs-lookup"><span data-stu-id="0a185-135">Filter Delivery Mode Option</span></span> | <span data-ttu-id="0a185-136">**Ära filtreeri** või **Lähetusega mitteseotud viisid**</span><span class="sxs-lookup"><span data-stu-id="0a185-136">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="0a185-137">Väärtus, mis määrab, kas tarnevalikute moodul peaks filtreerima välja kõik tarneviisid, mis pole seotud lähetusega.</span><span class="sxs-lookup"><span data-stu-id="0a185-137">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |
| <span data-ttu-id="0a185-138">Tarnesuvandi automaatne valimine</span><span class="sxs-lookup"><span data-stu-id="0a185-138">Auto select a delivery option</span></span> | <span data-ttu-id="0a185-139">**Ära filtreeri**, **vali tarnesuvand automaatselt ja kuva kokkuvõte** või vali tarnesuvand automaatselt ja ära kuva **kokkuvõtet**</span><span class="sxs-lookup"><span data-stu-id="0a185-139">**Do not filter**, **Auto select delivery option and show summary**, or **Auto select delivery option and don't show summary**</span></span> | <span data-ttu-id="0a185-140">See atribuut rakendab automaatselt esimese saadaoleva tarne suvandi väljaregistreerimiseks ilma, et kasutaja seda valik nõuaks.</span><span class="sxs-lookup"><span data-stu-id="0a185-140">This property automatically applies the first available delivery option to checkout without requiring the user to select it.</span></span> <span data-ttu-id="0a185-141">Seda tuleks kasutada ainult juhul, kui tarnevalik on saadaval.</span><span class="sxs-lookup"><span data-stu-id="0a185-141">It should be used only if there is one available delivery option.</span></span> <span data-ttu-id="0a185-142">See atribuut on saadaval alates Commerce'i versiooni 10.0.19 väljalaskest.</span><span class="sxs-lookup"><span data-stu-id="0a185-142">This property is supported as of the Commerce version 10.0.19 release.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="0a185-143">Maksmise lehele tarnevalikute mooduli lisamine ja vajalike atribuutide seadistamine</span><span class="sxs-lookup"><span data-stu-id="0a185-143">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="0a185-144">Tarnevalikute moodulit saab lisada ainult maksmise moodulisse.</span><span class="sxs-lookup"><span data-stu-id="0a185-144">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="0a185-145">Lisateavet selle kohta, kuidas konfigureerida tarnevalikute moodulit ja lisada seda maksmise lehele, leiate teemast [Maksmise moodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="0a185-145">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0a185-146">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0a185-146">Additional resources</span></span>

[<span data-ttu-id="0a185-147">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="0a185-147">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0a185-148">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="0a185-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0a185-149">Makse moodul</span><span class="sxs-lookup"><span data-stu-id="0a185-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="0a185-150">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="0a185-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="0a185-151">Järeletulemisteabe moodul</span><span class="sxs-lookup"><span data-stu-id="0a185-151">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="0a185-152">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="0a185-152">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="0a185-153">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="0a185-153">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="0a185-154">Võrgukanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="0a185-154">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="0a185-155">Omnikanali täpsemad automaatsed kulud</span><span class="sxs-lookup"><span data-stu-id="0a185-155">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="0a185-156">Päisekulude proportsionaalselt jaotamine müügiridade järgi</span><span class="sxs-lookup"><span data-stu-id="0a185-156">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="0a185-157">Tarneviiside seadistamine</span><span class="sxs-lookup"><span data-stu-id="0a185-157">Set up modes of delivery</span></span>](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
