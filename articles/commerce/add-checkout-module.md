---
title: Maksmise moodul
description: Selles teemas kirjeldatakse, kuidas lisada lehele maksmise moodul ja määrata vajalikud atribuudid.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4b810441fd25d41ee0893b119b4f7d91e7435d21
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697079"
---
# <a name="checkout-module"></a><span data-ttu-id="ce605-103">Maksmise moodul</span><span class="sxs-lookup"><span data-stu-id="ce605-103">Checkout module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ce605-104">Selles teemas kirjeldatakse, kuidas lisada lehele maksmise moodul ja määrata vajalikud atribuudid.</span><span class="sxs-lookup"><span data-stu-id="ce605-104">This topic describes how to add a checkout module to a page and set the required properties.</span></span>

## <a name="overview"></a><span data-ttu-id="ce605-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="ce605-105">Overview</span></span>

<span data-ttu-id="ce605-106">Maksmise moodul on spetsiaalne konteiner, mis majutab kõiki tellimuse loomiseks vajalikke mooduleid.</span><span class="sxs-lookup"><span data-stu-id="ce605-106">A checkout module is a special container that hosts all the modules that are required to create an order.</span></span> <span data-ttu-id="ce605-107">Kassa moodul võib sisaldada mooduleid, mis töötlevad kättetoimetamise aadressi, tarne meetodeid, arveldusteavet, tellimuse kokkuvõtet ja muud kliendi tellimusega seotud teavet.</span><span class="sxs-lookup"><span data-stu-id="ce605-107">A checkout module can include modules that handle the shipping address, shipping methods, billing information, order summary, and other information that is related to a customer order.</span></span> <span data-ttu-id="ce605-108">See esitab samm-sammulise voo, mida klient ostu sooritamiseks kogu asjakohase teabe sisestamiseks kasutab.</span><span class="sxs-lookup"><span data-stu-id="ce605-108">It presents a step-by-step flow that a customer uses to enter all the relevant information to make a purchase.</span></span>

<span data-ttu-id="ce605-109">Maksmise moodul renderdab andmeid ostukorvi ID põhjal.</span><span class="sxs-lookup"><span data-stu-id="ce605-109">A checkout module renders data based on the cart ID.</span></span> <span data-ttu-id="ce605-110">See ostukorvi ID salvestatakse brauseriküpsisena.</span><span class="sxs-lookup"><span data-stu-id="ce605-110">This cart ID is saved as a browser cookie.</span></span> <span data-ttu-id="ce605-111">Ostukorvi ID on nõutav, et renderdada maksmise mooduli teavet, nagu tellimuse kaubad, kogusumma ja allahindlused.</span><span class="sxs-lookup"><span data-stu-id="ce605-111">A cart ID is required to render information in the checkout module, such as the items in the order, the total amount, and discounts.</span></span>

## <a name="checkout-module-properties"></a><span data-ttu-id="ce605-112">Maksmise mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="ce605-112">Checkout module properties</span></span>

<span data-ttu-id="ce605-113">Maksmise moodul majutab endas moodulite kogumit.</span><span class="sxs-lookup"><span data-stu-id="ce605-113">A checkout module hosts a set of modules inside it.</span></span> <span data-ttu-id="ce605-114">Laiuse atribuut võimaldab teil määrata, kas maksmise moodulis olevad kaubad peavad mahtuma selle laiusesse või täitma ekraani.</span><span class="sxs-lookup"><span data-stu-id="ce605-114">A width property lets you specify whether the items in the checkout module should fit the width of it or fill the screen.</span></span>

<span data-ttu-id="ce605-115">Maksmise moodulil on mitu pesa, näiteks pesa **Maksmise teave**, pesa **Tellimuse kokkuvõte** ja pesa **Tellimuse esitamine**.</span><span class="sxs-lookup"><span data-stu-id="ce605-115">A checkout module has multiple slots, such as a **Checkout information** slot, an **Order summary** slot, and a **Place order** slot.</span></span> <span data-ttu-id="ce605-116">Iga pesa toetab moodulite kogumit, mis kuvatakse lehel kindlas paigutuses.</span><span class="sxs-lookup"><span data-stu-id="ce605-116">Each slot supports a set of modules that will appear in a specific layout on the page.</span></span> <span data-ttu-id="ce605-117">Näiteks sisaldab pesa **Maksmise teave** kõiki mooduleid, mis on vajalikud maksmise käivitamiseks, nagu saatmise aadressi ja makseviisi moodulid.</span><span class="sxs-lookup"><span data-stu-id="ce605-117">For example, the **Checkout information** slot contains all the modules that are required to trigger a checkout, such as modules for the shipping address and payment method.</span></span> <span data-ttu-id="ce605-118">Pesa **Tellimuse kokkuvõtte** näitab tellimuse kokkuvõtet ja toetab tellimuse esitamise tegevust.</span><span class="sxs-lookup"><span data-stu-id="ce605-118">The **Order summary** slot shows an order summary and supports the action for placing the order.</span></span> <span data-ttu-id="ce605-119">Pesa **Tellimuse esitamine** toetab samuti tellimuse esitamise tegevust.</span><span class="sxs-lookup"><span data-stu-id="ce605-119">The **Place order** slot also supports the action for placing the order.</span></span> <span data-ttu-id="ce605-120">Tellimuse esitamise mooduleid saab erinevatelt platvormidelt tellimuste esitamise protsessi optimeerimiseks määratleda kahes pesas.</span><span class="sxs-lookup"><span data-stu-id="ce605-120">Place order modules can be defined in two slots to optimize the process of placing orders from various platforms.</span></span>

### <a name="modules-that-can-be-used-in-the-checkout-module"></a><span data-ttu-id="ce605-121">Moodulid, mida saab ostukorvi moodulis kasutada</span><span class="sxs-lookup"><span data-stu-id="ce605-121">Modules that can be used in the checkout module</span></span>

- <span data-ttu-id="ce605-122">**Tarneaadress** – see moodul võimaldab kliendil lisada või valida tellimuse tarneaadressi.</span><span class="sxs-lookup"><span data-stu-id="ce605-122">**Shipping address** – This module lets a customer add or select the shipping address for an order.</span></span> <span data-ttu-id="ce605-123">Kui klient on sisse logitud, kuvatakse aadress, mis selle kliendi jaoks eelmisel korral salvestati.</span><span class="sxs-lookup"><span data-stu-id="ce605-123">If the customer is signed in, any addresses that were previously saved for that customer are shown.</span></span> <span data-ttu-id="ce605-124">Seejärel saab klient valida nende aadresside seast.</span><span class="sxs-lookup"><span data-stu-id="ce605-124">The customer can then select among those addresses.</span></span> <span data-ttu-id="ce605-125">Klient saab lisada ka uue aadressi.</span><span class="sxs-lookup"><span data-stu-id="ce605-125">The customer can also add a new address.</span></span> <span data-ttu-id="ce605-126">Tarneaadressi kasutatakse kõigi kaupade puhul, mis nõuavad tarnet.</span><span class="sxs-lookup"><span data-stu-id="ce605-126">The shipping address is used for all the items in the order that require shipping.</span></span> <span data-ttu-id="ce605-127">Seda ei saa üksikute reakaupade puhul kohandada.</span><span class="sxs-lookup"><span data-stu-id="ce605-127">It can't be customized for individual line items.</span></span> <span data-ttu-id="ce605-128">Tarneaadressi vormingud määratletakse iga riigi või piirkonna kohta ja sellest moodulist tulenevad riigi/piirkonna spetsiifilised reeglid.</span><span class="sxs-lookup"><span data-stu-id="ce605-128">Shipping address formats are defined for each country or region, and the country/region-specific rules are enforced by this module.</span></span> <span data-ttu-id="ce605-129">Kuigi see moodul ei paku aadressi kinnitamist, saab aadressi kinnitamist rakendada kohandamise kaudu.</span><span class="sxs-lookup"><span data-stu-id="ce605-129">Although this module doesn't provide address validation, address validation can be implemented through customization.</span></span> <span data-ttu-id="ce605-130">Kui tellimus sisaldav ainult kaupu, millele minnakse poodi järgi, siis see moodul peidetakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="ce605-130">If the order includes only items that will be picked up in the store, this module is automatically hidden.</span></span>
- <span data-ttu-id="ce605-131">**Tarnevalikud** – see moodul võimaldab kliendil valida tellimuse tarnevaliku.</span><span class="sxs-lookup"><span data-stu-id="ce605-131">**Delivery options** – This module lets a customer select a delivery option for an order.</span></span> <span data-ttu-id="ce605-132">tarnevalikud põhinevad saatmisaadressil.</span><span class="sxs-lookup"><span data-stu-id="ce605-132">Delivery options are based on the shipping address.</span></span> <span data-ttu-id="ce605-133">Kui tarneaadressi muudetakse, tuleb tarnevalikud uuesti hankida.</span><span class="sxs-lookup"><span data-stu-id="ce605-133">If the shipping address is changed, the delivery options must be retrieved again.</span></span> <span data-ttu-id="ce605-134">Kui tellimus sisaldav ainult kaupu, millele minnakse poodi järgi, siis see moodul peidetakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="ce605-134">If the order includes only items that will be picked up in the store, this module is automatically hidden.</span></span>
- <span data-ttu-id="ce605-135">**Maksmise jaotise konteiner** – see moodul on konteiner, kuhu saate lisada mitu moodulit, et luua jaotis maksmise voo sees.</span><span class="sxs-lookup"><span data-stu-id="ce605-135">**Checkout section container** – This module is a container that you can put multiple modules inside to create a section within the checkout flow.</span></span> <span data-ttu-id="ce605-136">Näiteks saate panna sellesse konteinerisse kõik maksmisega seotud moodulid, et need kuvataks ühe jaotisena.</span><span class="sxs-lookup"><span data-stu-id="ce605-136">For example, you can put all payment-related modules inside this container to make them appear as one section.</span></span> <span data-ttu-id="ce605-137">See moodul mõjutab ainult voo paigutust.</span><span class="sxs-lookup"><span data-stu-id="ce605-137">This module affects only the layout of the flow.</span></span>
- <span data-ttu-id="ce605-138">**Kinkekaart** – see moodul võimaldab kliendil tasuda tellimuse eest kinkekaardiga.</span><span class="sxs-lookup"><span data-stu-id="ce605-138">**Gift card** – This module lets a customer pay for an order by using a gift card.</span></span> <span data-ttu-id="ce605-139">See toetab ainult Microsoft Dynamics 365 Commerce’i kinkekaarte.</span><span class="sxs-lookup"><span data-stu-id="ce605-139">It supports only Microsoft Dynamics 365 Commerce gift cards.</span></span> <span data-ttu-id="ce605-140">Tellimusele saab rakendada ühe või mitu kinkekaarti.</span><span class="sxs-lookup"><span data-stu-id="ce605-140">One or more gift cards can be applied to an order.</span></span> <span data-ttu-id="ce605-141">Kui kinkekaardi saldo ei kata ostukorvis olevat summat, saab kinkekaardi kombineerida muu makseviisiga.</span><span class="sxs-lookup"><span data-stu-id="ce605-141">If the balance of the gift card doesn't cover the amount in the cart, the gift card can be combined with another payment method.</span></span> <span data-ttu-id="ce605-142">Kinkekaarte saab lunastada ainult siis, kui klient on sisse logitud.</span><span class="sxs-lookup"><span data-stu-id="ce605-142">Gift cards can be redeemed only if the customer is signed in.</span></span>
- <span data-ttu-id="ce605-143">**Püsikliendi punktid** – see moodul võimaldab kliendil tasuda tellimuse eest püsikliendi punktidega.</span><span class="sxs-lookup"><span data-stu-id="ce605-143">**Loyalty points** – This module lets a customer pay for an order by using loyalty points.</span></span> <span data-ttu-id="ce605-144">See esitab saadaolevate punktide ja aeguvate punktide kokkuvõtte ja võimaldab klientidel valida lunastamiseks punktide arvu.</span><span class="sxs-lookup"><span data-stu-id="ce605-144">It provides a summary of available points and expiring points, and lets the customer select the number of points to redeem.</span></span> <span data-ttu-id="ce605-145">Kui klient ei ole sisse logitud või ei ole püsikliendis programmi liige või kui ostukorvi kogusumma on 0 (null), peidetakse see moodul automaatselt.</span><span class="sxs-lookup"><span data-stu-id="ce605-145">If the customer isn't signed in or isn't a loyalty member, or if the total amount in the cart is 0 (zero), this module is automatically hidden.</span></span>
- <span data-ttu-id="ce605-146">**Krediitkaart** – see moodul võimaldab kliendil tasuda tellimuse eest krediitkaardiga.</span><span class="sxs-lookup"><span data-stu-id="ce605-146">**Credit card** – This module lets a customer pay for an order by using a credit card.</span></span> <span data-ttu-id="ce605-147">Kui püsikliendi punktid või kinkekaart katab ostukorvi kogusumma või kui see on 0 (null), peidetakse see moodul automaatselt.</span><span class="sxs-lookup"><span data-stu-id="ce605-147">If the total amount in the cart is covered by loyalty points or a gift card, or if it's 0 (zero), this module is automatically hidden.</span></span> <span data-ttu-id="ce605-148">Krediitkaardi integratsiooni pakub Adyeni makseühendus.</span><span class="sxs-lookup"><span data-stu-id="ce605-148">Credit card integration is provided by the Adyen payment connector.</span></span> <span data-ttu-id="ce605-149">Lisateavet selle konnektori kasutamise kohta vaadake teemast [Adyeni makseühendus](https://).</span><span class="sxs-lookup"><span data-stu-id="ce605-149">For more information about how to use this connector, see [Adyen payment connector](https://).</span></span>
- <span data-ttu-id="ce605-150">**Arveldusaadress** – see moodul võimaldab kliendil esitada arveldusteavet.</span><span class="sxs-lookup"><span data-stu-id="ce605-150">**Billing address** – This module lets a customer provide billing information.</span></span> <span data-ttu-id="ce605-151">Seda teavet töötleb koos krediitkaardi teabega Adyen.</span><span class="sxs-lookup"><span data-stu-id="ce605-151">This information is processed, together with the credit card information, by Adyen.</span></span> <span data-ttu-id="ce605-152">See moodul sisaldab võimalust, et kliendid kasutavad oma arveldusaadressi tarneaadressina.</span><span class="sxs-lookup"><span data-stu-id="ce605-152">This module includes an option that lets customers use their billing address as the shipping address.</span></span>
- <span data-ttu-id="ce605-153">**Kontaktteave** – see moodul võimaldab kliendil lisada või muuta tellimuse kontaktandmeid (meiliaadress).</span><span class="sxs-lookup"><span data-stu-id="ce605-153">**Contact information** – This module lets a customer add or change the contact information (email address) for an order.</span></span>
- <span data-ttu-id="ce605-154">**Tellimuse esitamine** – see moodul võimaldab kliendil esitada tellimuse.</span><span class="sxs-lookup"><span data-stu-id="ce605-154">**Place order** – This module lets a customer place an order.</span></span>
- <span data-ttu-id="ce605-155">**Sisurikas plokk** – see moodul sisaldab mis tahes teateid, mida juhib sisuhaldussüsteem (CMS).</span><span class="sxs-lookup"><span data-stu-id="ce605-155">**Content rich block** – This module contains any messaging that is driven by the content management system (CMS).</span></span> <span data-ttu-id="ce605-156">Näiteks võib see sisaldada teadet, mis ütleb: „Tellimusega esinevate probleemide osas võtke ühendust numbril 1-800-FABRIKAM”.</span><span class="sxs-lookup"><span data-stu-id="ce605-156">For example, it might contain a message that states, "For issues with your order, please contact 1-800-FABRIKAM."</span></span> 
- <span data-ttu-id="ce605-157">**Tellimuse Kokkuvõte** – selles moodulis kuvatakse tellimuse kulude jaotus.</span><span class="sxs-lookup"><span data-stu-id="ce605-157">**Order summary** – This module shows the cost breakdown of an order.</span></span>
- <span data-ttu-id="ce605-158">**Tellimuserea kaubad** – selles moodulis kuvatakse tellimuses sisalduvate kaupade kokkuvõte.</span><span class="sxs-lookup"><span data-stu-id="ce605-158">**Order line items** – This module shows a summary of the items that will be included in an order.</span></span>

## <a name="retail-server-interaction"></a><span data-ttu-id="ce605-159">Jaemüügiserveri suhtlus</span><span class="sxs-lookup"><span data-stu-id="ce605-159">Retail server interaction</span></span>

<span data-ttu-id="ce605-160">Enamik maksmise teabest, näiteks tarneaadress ja tarnemeetod, salvestatakse ostukorvis ja töödeldakse tellimuse osana.</span><span class="sxs-lookup"><span data-stu-id="ce605-160">Most of the checkout information, such as the shipping address and shipping method, is stored in the cart and processed as part of the order.</span></span> <span data-ttu-id="ce605-161">Ainus erand on krediitkaardi teave.</span><span class="sxs-lookup"><span data-stu-id="ce605-161">The only exception is the credit card information.</span></span> <span data-ttu-id="ce605-162">See teave töödeldakse otse Adyeni makseühenduse abil.</span><span class="sxs-lookup"><span data-stu-id="ce605-162">This information is processed directly by using the Adyen payment connector.</span></span> <span data-ttu-id="ce605-163">Makse on autoriseeritakse, kuid seda ei nõuta sisse.</span><span class="sxs-lookup"><span data-stu-id="ce605-163">The payment is authorized but isn't charged.</span></span>

## <a name="add-a-checkout-module-to-a-new-page-and-set-the-required-properties"></a><span data-ttu-id="ce605-164">Uuele lehele maksmise mooduli lisamine ja vajalike atribuutide seadistamine</span><span class="sxs-lookup"><span data-stu-id="ce605-164">Add a checkout module to a new page and set the required properties</span></span>

<span data-ttu-id="ce605-165">Uuele lehele ostukorvi mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ce605-165">To add a checkout module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="ce605-166">Avage **Fragment \> Uus fragment** ja andke uuele fragmendile nimi **Maksmise fragment**.</span><span class="sxs-lookup"><span data-stu-id="ce605-166">Go to **Fragment \> New Fragment**, and name the new fragment **Checkout fragment**.</span></span>
1. <span data-ttu-id="ce605-167">Lisage fragmendile maksmise moodul.</span><span class="sxs-lookup"><span data-stu-id="ce605-167">Add a checkout module to the fragment.</span></span>
1. <span data-ttu-id="ce605-168">Lisage maksmise moodulile päis.</span><span class="sxs-lookup"><span data-stu-id="ce605-168">Add a heading to the checkout module.</span></span>
1. <span data-ttu-id="ce605-169">Lisage pesas **Maksmise teave** tarneaadressi, tarnevaliku, maksmise jaotise konteineri ja kontaktteabe moodulid.</span><span class="sxs-lookup"><span data-stu-id="ce605-169">In the **Checkout information** slot, add shipping address, delivery options, checkout section container, and contact information modules.</span></span> <span data-ttu-id="ce605-170">Nüüd peaks pesas **Maksmise teave** olema neli jaotist.</span><span class="sxs-lookup"><span data-stu-id="ce605-170">There should now be four sections in the **Checkout information** slot.</span></span>
1. <span data-ttu-id="ce605-171">Lisage maksmise jaotise konteinermoodulis kinkekaardi, püsikliendi punktide ja krediitkaardi moodulid.</span><span class="sxs-lookup"><span data-stu-id="ce605-171">In the checkout section container module, add gift card, loyalty points, and credit card modules.</span></span> <span data-ttu-id="ce605-172">Sel viisil saate kindlustada, et kõik maksmisviisid ilmuvad jaotises koos.</span><span class="sxs-lookup"><span data-stu-id="ce605-172">In this way, you make sure that all the payment methods appear together in a section.</span></span>
1. <span data-ttu-id="ce605-173">Lisage pesas **Tellimuse kokkuvõte** tellimuse kokkuvõtte, tellimuse esitamise ja sisurikas plokimoodul.</span><span class="sxs-lookup"><span data-stu-id="ce605-173">In the **Order summary** slot, add order summary, place order, and content rich block modules.</span></span>
1. <span data-ttu-id="ce605-174">Lisage sisurikkas plokimoodulis järgmine tekst: **Tellimusega seotud küsimuste korral võtke ühendust numbril 1-800-FABRIKAM**.</span><span class="sxs-lookup"><span data-stu-id="ce605-174">In the content rich block module, add the following text: **For questions about your order, contact 1-800-FABRIKAM.**</span></span>
1. <span data-ttu-id="ce605-175">Lisage pesas **Tellimuse esitamine** tellimuse esitamise moodul.</span><span class="sxs-lookup"><span data-stu-id="ce605-175">In the **Place order** slot, add a place order module.</span></span>
1. <span data-ttu-id="ce605-176">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ce605-176">Select **Save**.</span></span> <span data-ttu-id="ce605-177">Osasid mooduleid ei pruugita eelvaates renderdada, kuna nendel puudub kaardi kontekst.</span><span class="sxs-lookup"><span data-stu-id="ce605-177">Some modules might not be rendered in the preview, because they don't have a cart context.</span></span>
1. <span data-ttu-id="ce605-178">Kontrollige selles fragmenti ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="ce605-178">Check the fragment in, and publish it.</span></span>
1. <span data-ttu-id="ce605-179">Looge mall, mis kasutab uut maksmise fragmenti.</span><span class="sxs-lookup"><span data-stu-id="ce605-179">Create a template that uses the new checkout fragment.</span></span>
1. <span data-ttu-id="ce605-180">Looge maksmise leht, mis kasutab uut malli.</span><span class="sxs-lookup"><span data-stu-id="ce605-180">Create a checkout page that uses the new template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce605-181">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ce605-181">Additional resources</span></span>

[<span data-ttu-id="ce605-182">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="ce605-182">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ce605-183">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="ce605-183">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="ce605-184">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="ce605-184">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ce605-185">Ostukorvi moodul</span><span class="sxs-lookup"><span data-stu-id="ce605-185">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="ce605-186">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="ce605-186">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="ce605-187">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="ce605-187">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="ce605-188">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="ce605-188">Footer module</span></span>](author-footer-module.md)