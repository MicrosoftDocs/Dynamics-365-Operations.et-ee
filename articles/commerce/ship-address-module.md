---
title: Tarneaadressi moodul
description: See teema hõlmab tarneaadressi moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.
author: anupamar-ms
ms.date: 02/11/2021
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
ms.openlocfilehash: fd48a04612159cbe29a2cc7cafea1c9c4c8745b4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795425"
---
# <a name="shipping-address-module"></a><span data-ttu-id="5a0dd-103">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="5a0dd-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5a0dd-104">See teema hõlmab tarneaadressi moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5a0dd-105">Tarneaadressi moodul võimaldab klientidel maksmise voo ajal lisada või valida tellimuse tarneaadressi.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-105">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="5a0dd-106">Kui klient on sisse logitud, kuvatakse aadressid, mis selle kliendi jaoks eelmisel korral salvestati, ja klient saab teha nende seast valiku.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-106">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="5a0dd-107">Klient saab lisada ka uue aadressi.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-107">The customer can also add a new address.</span></span> <span data-ttu-id="5a0dd-108">Tarneaadressi moodulit kasutatakse kõigi kaupade puhul, mis nõuavad tarnet.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-108">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="5a0dd-109">Tarneaadressi vorminguid saab määratleda Commerce'i peakontoris iga riigi või regiooni jaoks ning tarneaadressi moodul täidab seejärel riigi-/regioonipõhiseid reegleid.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-109">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="5a0dd-110">Kui kliendid sisestavad tarneaadressi maksmise voos, on neil võimalus salvestada aadress esmase aadressina.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-110">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="5a0dd-111">See valik kuvatakse ainult siis, kui klient on sisse logitud.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-111">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="5a0dd-112">Kuigi tarneaadressi moodul ei paku aadressi kinnitamist, saab seda funktsiooni rakendada kohandamise kaudu.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-112">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="5a0dd-113">Järgmisel pildil on näide uuest tarneaadressi moodulist maksmise lehel.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-113">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Tarneaadressi mooduli näide maksmise lehel](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="5a0dd-115">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="5a0dd-115">Module properties</span></span>

| <span data-ttu-id="5a0dd-116">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="5a0dd-116">Property name</span></span> | <span data-ttu-id="5a0dd-117">Väärtused</span><span class="sxs-lookup"><span data-stu-id="5a0dd-117">Values</span></span> | <span data-ttu-id="5a0dd-118">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="5a0dd-118">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="5a0dd-119">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="5a0dd-119">Heading</span></span> | <span data-ttu-id="5a0dd-120">Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**)</span><span class="sxs-lookup"><span data-stu-id="5a0dd-120">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="5a0dd-121">Tarneaadressi mooduli valikuline pealkiri.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-121">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="5a0dd-122">Kuva aadressi tüüp</span><span class="sxs-lookup"><span data-stu-id="5a0dd-122">Show address type</span></span> | <span data-ttu-id="5a0dd-123">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="5a0dd-123">**True** or **False**</span></span> | <span data-ttu-id="5a0dd-124">Kui selle valikulise atribuudi väärtuseks on seatud **Tõene**, kuvatakse aadressi tüüp, nt **Kodu** või **Ettevõte**.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-124">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="5a0dd-125">Kui aadressi tüüpi pole määratud, salvestatakse aadress automaatselt nii, et selle **Tüüp**=**Muu**.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-125">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |
| <span data-ttu-id="5a0dd-126">Lubage automaatne soovitus</span><span class="sxs-lookup"><span data-stu-id="5a0dd-126">Enable auto suggestion</span></span>| <span data-ttu-id="5a0dd-127">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="5a0dd-127">**True** or **False**</span></span> | <span data-ttu-id="5a0dd-128">Kui valikuline atribuut on seatud väärtusele **Tõene**, antakse automaatsed aadressisoovitused.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-128">If this optional property is set to **True**, automatic address suggestions will be provided.</span></span> <span data-ttu-id="5a0dd-129">Need soovitused on toetatud Bingi kaartide puhul.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-129">These suggestions are powered by Bing Maps.</span></span> <span data-ttu-id="5a0dd-130">Lisateavet selle kohta, kuidas seadistada oma saidi jaoks Bing Mapsi integratsioon, vt [poe valimise moodulit](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="5a0dd-130">For information about how to set up Bing Maps integration for your site, see [Store selector module](store-selector.md).</span></span> <span data-ttu-id="5a0dd-131">See funktsioon on saadaval Commerce'i versiooni 10.0.15 väljalaskes.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-131">This feature is available as of the Commerce version 10.0.15 release.</span></span>|
|<span data-ttu-id="5a0dd-132">Automaatsed soovitatud valikud</span><span class="sxs-lookup"><span data-stu-id="5a0dd-132">Auto suggest options</span></span>| <span data-ttu-id="5a0dd-133">Number</span><span class="sxs-lookup"><span data-stu-id="5a0dd-133">A number</span></span>| <span data-ttu-id="5a0dd-134">Kui automaatsed aadressisoovitused on lubatud, saate määrata lisavalikud, näiteks maksimaalse soovituste arvu.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-134">If automatic address suggestions are enabled, you can specify additional options, such as the maximum number of suggestions that should be provided.</span></span>|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="5a0dd-135">Maksmise lehele tarneaadressi mooduli lisamine ja vajalike atribuutide seadistamine</span><span class="sxs-lookup"><span data-stu-id="5a0dd-135">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="5a0dd-136">Tarneaadressi moodulit saab lisada ainult maksmise moodulisse.</span><span class="sxs-lookup"><span data-stu-id="5a0dd-136">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="5a0dd-137">Lisateavet selle kohta, kuidas konfigureerida tarneaadressi moodulit ja lisada seda maksmise lehele, leiate teemast [Maksmise moodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="5a0dd-137">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5a0dd-138">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="5a0dd-138">Additional resources</span></span>

[<span data-ttu-id="5a0dd-139">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="5a0dd-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5a0dd-140">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="5a0dd-140">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="5a0dd-141">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="5a0dd-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="5a0dd-142">Makse moodul</span><span class="sxs-lookup"><span data-stu-id="5a0dd-142">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="5a0dd-143">Tarnesuvandite moodul</span><span class="sxs-lookup"><span data-stu-id="5a0dd-143">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="5a0dd-144">Järeletulemise teabe moodul</span><span class="sxs-lookup"><span data-stu-id="5a0dd-144">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="5a0dd-145">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="5a0dd-145">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="5a0dd-146">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="5a0dd-146">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="5a0dd-147">Kaupluse valimise moodul</span><span class="sxs-lookup"><span data-stu-id="5a0dd-147">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]