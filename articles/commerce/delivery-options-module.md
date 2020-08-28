---
title: Tarnevalikute moodul
description: See teema hõlmab tarnevalikute mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce konfigureerida.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 60449e9492c8e831b4ec6b2896f1ab471ef9d499
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661198"
---
# <a name="delivery-options-module"></a><span data-ttu-id="ffe4c-103">Tarnevalikute moodul</span><span class="sxs-lookup"><span data-stu-id="ffe4c-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="ffe4c-104">See teema hõlmab tarnevalikute mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ffe4c-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="ffe4c-105">Overview</span></span>

<span data-ttu-id="ffe4c-106">Tarnevalikute moodulid võimaldavad klientidel valida oma veebitellimuse jaoks tarneviisi, nt lähetamise või pealevõtmise.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-106">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="ffe4c-107">Tarneviisi määramiseks on vajalik tarneaadress.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-107">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="ffe4c-108">Kui tarneaadress muutub, tuleb tarnevalikud uuesti hankida.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-108">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="ffe4c-109">Kui tellimus sisaldab ainult kaupu, millele minnakse poodi järele, siis see moodul peidetakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-109">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="ffe4c-110">Lisateavet tarneviiside konfigureerimise kohta leiate teemadest [Võrgukanali seadistamine](channel-setup-online.md) ja [Tarneviiside seadistamine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="ffe4c-110">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="ffe4c-111">Igal tarneviisil võib olla seotud kulu.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-111">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="ffe4c-112">Lisateavet veebipoe jaoks kulude konfigureerimise kohta leiate teemast [Omnikanali täpsemad automaatsed kulud](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="ffe4c-112">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="ffe4c-113">Commerce'i versioonis 10.0.13 värskendati tarnevalikute moodulit, et toetada funktsioone **Päisekulud ilma proportsionaalse jaotamiseta** ja **Lähetamine reakuluna**.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-113">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="ffe4c-114">Kui proportsionaalne jaotamine on välja lülitatud, eeldatakse, et e-kaubanduse töövoog ei luba ostukorvis olevate kaupade jaoks valida erinevat tarneviisi (see tähendab, et mõned kaubad määratakse lähetamiseks, kuid teised pealevõtmiseks).</span><span class="sxs-lookup"><span data-stu-id="ffe4c-114">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="ffe4c-115">Funktsiooni **Päisekulud ilma proportsionaalse jaotamiseta** jaoks on vajalik, et Commerce'i peakontoris oleks sisse lülitatud lipp **Luba kanalis järjekindel tarneviisi käitlemine**.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-115">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="ffe4c-116">Kui see lipp on sisse lülitatud, rakendatakse saatekulusid kas päise- või reatasemel, sõltuvalt Commerce'i peakontori konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-116">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="ffe4c-117">Fabrikami kujundus toetab kombineeritud tarneviisi, kus mõni kaup määratakse lähetamiseks, kuid teised pealevõtmiseks.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-117">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="ffe4c-118">Selle viisi puhul jaotatakse saatekulud proportsionaalselt kõigi kaupade vahel, mille tarneviis on lähetamine.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-118">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="ffe4c-119">Kombineeritud tarneviisi toimimiseks peate Commerce'i peakontoris enne konfigureerima funktsiooni **Päisekulud koos proportsionaalse jaotamisega**.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-119">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="ffe4c-120">Lisateavet selle konfiguratsiooni kohta leiate teemast [Päisekulude proportsionaalselt jaotamine müügiridade järgi](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="ffe4c-120">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="ffe4c-121">Kui reakaupade puhul rakenduvad saatekulud, saab neid kuvada iga kauba ostukorvireal.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-121">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="ffe4c-122">Selle funktsiooni jaoks on vaja, et atribuut **Kuva reakauba saatekulud** oleks nii ostukorvi- kui ka maksmise mooduli puhul sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-122">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="ffe4c-123">Lisateavet leiate teemadest [Ostukorvimoodul](add-cart-module.md) ja [Maksmise moodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="ffe4c-123">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="ffe4c-124">Järgmisel illustratsioonil on näide tarnevalikute moodulist maksmise lehel.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-124">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Tarnevalikute mooduli näide maksmise lehel](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="ffe4c-126">Tarnevalikute mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="ffe4c-126">Delivery options module properties</span></span>

| <span data-ttu-id="ffe4c-127">Atribuut</span><span class="sxs-lookup"><span data-stu-id="ffe4c-127">Property</span></span> | <span data-ttu-id="ffe4c-128">Väärtused</span><span class="sxs-lookup"><span data-stu-id="ffe4c-128">Values</span></span> | <span data-ttu-id="ffe4c-129">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ffe4c-129">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="ffe4c-130">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="ffe4c-130">Heading</span></span> | <span data-ttu-id="ffe4c-131">Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**)</span><span class="sxs-lookup"><span data-stu-id="ffe4c-131">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="ffe4c-132">Tarnevalikute mooduli valikuline pealkiri.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-132">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="ffe4c-133">Kohandatud CSS-i klassinimi</span><span class="sxs-lookup"><span data-stu-id="ffe4c-133">Custom CSS class name</span></span> | <span data-ttu-id="ffe4c-134">Tekst</span><span class="sxs-lookup"><span data-stu-id="ffe4c-134">Text</span></span> | <span data-ttu-id="ffe4c-135">Kaskaadlaadistiku (CSS) kohandatud klassi nimi, mida kasutatakse selle mooduli renderdamiseks, kui seda on vaja.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-135">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="ffe4c-136">Tarneviisi valikute filtreerimine</span><span class="sxs-lookup"><span data-stu-id="ffe4c-136">Filter Delivery Mode Option</span></span> | <span data-ttu-id="ffe4c-137">**Ära filtreeri** või **Lähetusega mitteseotud viisid**</span><span class="sxs-lookup"><span data-stu-id="ffe4c-137">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="ffe4c-138">Väärtus, mis määrab, kas tarnevalikute moodul peaks filtreerima välja kõik tarneviisid, mis pole seotud lähetusega.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-138">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="ffe4c-139">Maksmise lehele tarnevalikute mooduli lisamine ja vajalike atribuutide seadistamine</span><span class="sxs-lookup"><span data-stu-id="ffe4c-139">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="ffe4c-140">Tarnevalikute moodulit saab lisada ainult maksmise moodulisse.</span><span class="sxs-lookup"><span data-stu-id="ffe4c-140">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="ffe4c-141">Lisateavet selle kohta, kuidas konfigureerida tarnevalikute moodulit ja lisada seda maksmise lehele, leiate teemast [Maksmise moodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="ffe4c-141">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ffe4c-142">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ffe4c-142">Additional resources</span></span>

[<span data-ttu-id="ffe4c-143">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="ffe4c-143">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="ffe4c-144">Maksmise moodul</span><span class="sxs-lookup"><span data-stu-id="ffe4c-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="ffe4c-145">Maksemoodul</span><span class="sxs-lookup"><span data-stu-id="ffe4c-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="ffe4c-146">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="ffe4c-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="ffe4c-147">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="ffe4c-147">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="ffe4c-148">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="ffe4c-148">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="ffe4c-149">Võrgukanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="ffe4c-149">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="ffe4c-150">Omnikanali täpsemad automaatsed kulud</span><span class="sxs-lookup"><span data-stu-id="ffe4c-150">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="ffe4c-151">Päisekulude proportsionaalselt jaotamine müügiridade järgi</span><span class="sxs-lookup"><span data-stu-id="ffe4c-151">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="ffe4c-152">Tarneviiside seadistamine</span><span class="sxs-lookup"><span data-stu-id="ffe4c-152">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
