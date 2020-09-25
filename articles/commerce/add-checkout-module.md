---
title: Maksmise moodul
description: Selles teemas kirjeldatakse, kuidas lisada lehele maksmise moodul ja määrata vajalikud atribuudid.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 389e3e9d631574eac499f7c6146e2776b8126a52
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761101"
---
# <a name="checkout-module"></a><span data-ttu-id="1e83b-103">Maksmise moodul</span><span class="sxs-lookup"><span data-stu-id="1e83b-103">Checkout module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="1e83b-104">Selles teemas kirjeldatakse, kuidas lisada lehele maksmise moodul ja määrata vajalikud atribuudid.</span><span class="sxs-lookup"><span data-stu-id="1e83b-104">This topic describes how to add a checkout module to a page and set the required properties.</span></span>

## <a name="overview"></a><span data-ttu-id="1e83b-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="1e83b-105">Overview</span></span>

<span data-ttu-id="1e83b-106">Maksmise moodul on spetsiaalne konteiner, mis majutab kõiki tellimuse loomiseks vajalikke mooduleid.</span><span class="sxs-lookup"><span data-stu-id="1e83b-106">A checkout module is a special container that hosts all modules that are required to create an order.</span></span> <span data-ttu-id="1e83b-107">See esitab samm-sammulise voo, mida klient ostu sooritamiseks kogu asjakohase teabe sisestamiseks kasutab.</span><span class="sxs-lookup"><span data-stu-id="1e83b-107">It presents a step-by-step flow that a customer uses to enter all the relevant information to make a purchase.</span></span> <span data-ttu-id="1e83b-108">See hõivab tarneaadressi, tarneviisi ja arveldusteavet.</span><span class="sxs-lookup"><span data-stu-id="1e83b-108">It captures the shipping address, shipping method, and billing information.</span></span> <span data-ttu-id="1e83b-109">Samuti esitatakse tellimuse kokkuvõte ja muud kliendi tellimusega seotud andmed.</span><span class="sxs-lookup"><span data-stu-id="1e83b-109">It also provides an order summary and other information that is related to a customer order.</span></span>

<span data-ttu-id="1e83b-110">Maksmise moodul renderdab andmeid ostukorvi ID põhjal.</span><span class="sxs-lookup"><span data-stu-id="1e83b-110">A checkout module renders data based on the cart ID.</span></span> <span data-ttu-id="1e83b-111">See ostukorvi ID salvestatakse brauseriküpsisena.</span><span class="sxs-lookup"><span data-stu-id="1e83b-111">This cart ID is saved as a browser cookie.</span></span> <span data-ttu-id="1e83b-112">Ostukorvi ID on nõutav, et renderdada maksmise mooduli teavet, nagu tellimuse kaubad, kogusumma ja allahindlused.</span><span class="sxs-lookup"><span data-stu-id="1e83b-112">A cart ID is required to render information in the checkout module, such as the items in the order, the total amount, and discounts.</span></span> 

<span data-ttu-id="1e83b-113">Järgmisel pildil on näide Fabrikami maksmise moodulist maksmise lehel.</span><span class="sxs-lookup"><span data-stu-id="1e83b-113">The following image shows an example of a Fabrikam checkout module on a checkout page.</span></span>

![Maksmise mooduli näide](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a><span data-ttu-id="1e83b-115">Maksmise mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="1e83b-115">Checkout module properties</span></span>

<span data-ttu-id="1e83b-116">Kassa moodul näitab tellimuse kokkuvõtet ja pakub tellimuse esitamise funktsionaalsust.</span><span class="sxs-lookup"><span data-stu-id="1e83b-116">A checkout module shows an order summary and provides the functionality for placing an order.</span></span> <span data-ttu-id="1e83b-117">Kõigi tellimuse esitamiseks vajalike kliendi andmete kogumiseks tuleb kassamoodulile lisada täiendavaid mooduleid.</span><span class="sxs-lookup"><span data-stu-id="1e83b-117">To gather all the customer information that is required before an order can be placed, additional modules must be added to the checkout module.</span></span> <span data-ttu-id="1e83b-118">Seetõttu on jaemüüjatel paindlikkus vastavalt oma vajadustele kassavoole kohandatud mooduleid lisada või välistada.</span><span class="sxs-lookup"><span data-stu-id="1e83b-118">Therefore, retailers have the flexibility to add custom modules to the checkout flow, or to exclude modules, based on their requirements.</span></span>

| <span data-ttu-id="1e83b-119">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="1e83b-119">Property name</span></span> | <span data-ttu-id="1e83b-120">Väärtused</span><span class="sxs-lookup"><span data-stu-id="1e83b-120">Values</span></span> | <span data-ttu-id="1e83b-121">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="1e83b-121">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="1e83b-122">Kassa pealkiri</span><span class="sxs-lookup"><span data-stu-id="1e83b-122">Checkout heading</span></span> | <span data-ttu-id="1e83b-123">Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**)</span><span class="sxs-lookup"><span data-stu-id="1e83b-123">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="1e83b-124">Maksmise mooduli pealkiri.</span><span class="sxs-lookup"><span data-stu-id="1e83b-124">A heading for the checkout module.</span></span> |
| <span data-ttu-id="1e83b-125">Tellimuse kokkuvõtte pealkiri</span><span class="sxs-lookup"><span data-stu-id="1e83b-125">Order summary heading</span></span> | <span data-ttu-id="1e83b-126">Pealkirja tekst</span><span class="sxs-lookup"><span data-stu-id="1e83b-126">Heading text</span></span> | <span data-ttu-id="1e83b-127">Mooduli tellimuse kokkuvõtte jaotise pealkiri.</span><span class="sxs-lookup"><span data-stu-id="1e83b-127">A heading for the order summary section of the module.</span></span> |
| <span data-ttu-id="1e83b-128">Ostukorvi reakaupade pealkiri</span><span class="sxs-lookup"><span data-stu-id="1e83b-128">Cart line items heading</span></span> | <span data-ttu-id="1e83b-129">Pealkirja tekst</span><span class="sxs-lookup"><span data-stu-id="1e83b-129">Heading text</span></span> | <span data-ttu-id="1e83b-130">Maksmise moodulis kuvatavate ostukorvi reakaupade pealkiri.</span><span class="sxs-lookup"><span data-stu-id="1e83b-130">A heading for cart line items that are shown in the checkout module.</span></span> |
| <span data-ttu-id="1e83b-131">Kuva reakauba saatekulud</span><span class="sxs-lookup"><span data-stu-id="1e83b-131">Show shipping charges on line item</span></span> | <span data-ttu-id="1e83b-132">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="1e83b-132">**True** or **False**</span></span> | <span data-ttu-id="1e83b-133">Kui selle atribuudi väärtuseks on seatud **Tõene**, kuvatakse reakaupade puhul rakenduvad saatekulud ostukorvi ridadel.</span><span class="sxs-lookup"><span data-stu-id="1e83b-133">If this property is set to **True**, the shipping charges that are applicable for line items will be shown on cart lines.</span></span> <span data-ttu-id="1e83b-134">Kui funktsioon **Päisekulu ilma proportsionaalse jaotamiseta** on Commerce'i peakontoris sisse lülitatud, rakendatakse saatekulu päisetasemel, mitte reatasemel.</span><span class="sxs-lookup"><span data-stu-id="1e83b-134">If the **Header charge with no proration** feature is turned on in Commerce headquarters, the shipping charge will be applied at the header level, not the line level.</span></span> <span data-ttu-id="1e83b-135">See funktsioon lisati Commerce'i versioonis 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="1e83b-135">This feature was added in Commerce version 10.0.13.</span></span> |

## <a name="modules-that-can-be-used-in-the-checkout-module"></a><span data-ttu-id="1e83b-136">Moodulid, mida saab ostukorvi moodulis kasutada</span><span class="sxs-lookup"><span data-stu-id="1e83b-136">Modules that can be used in the checkout module</span></span>

- <span data-ttu-id="1e83b-137">**Tarneaadress** – see moodul võimaldab kliendil lisada või valida tellimuse tarneaadressi.</span><span class="sxs-lookup"><span data-stu-id="1e83b-137">**Shipping address** – This module lets a customer add or select the shipping address for an order.</span></span> <span data-ttu-id="1e83b-138">Lisateavet selle mooduli kohta leiate teemast [Tarneaadressi moodul](ship-address-module.md).</span><span class="sxs-lookup"><span data-stu-id="1e83b-138">For more information about this module, see [Shipping address module](ship-address-module.md).</span></span>

    <span data-ttu-id="1e83b-139">Järgmisel pildil on näide tarneaadressi moodulist maksmise lehel.</span><span class="sxs-lookup"><span data-stu-id="1e83b-139">The following image shows an example of a shipping address module on a checkout page.</span></span>

    ![Tarneaadressi mooduli näide](./media/ecommerce-shippingaddress.PNG)

- <span data-ttu-id="1e83b-141">**Tarnevalikud** – see moodul võimaldab kliendil valida tellimuse tarneviisi.</span><span class="sxs-lookup"><span data-stu-id="1e83b-141">**Delivery options** – This module lets a customer select a mode of delivery for an order.</span></span> <span data-ttu-id="1e83b-142">Lisateavet selle mooduli kohta leiate teemast [Tarnevalikute moodul](delivery-options-module.md).</span><span class="sxs-lookup"><span data-stu-id="1e83b-142">For more information about this module, see [Delivery options module](delivery-options-module.md).</span></span>

    <span data-ttu-id="1e83b-143">Järgmisel pildil on näide tarnevalikute moodulist maksmise lehel.</span><span class="sxs-lookup"><span data-stu-id="1e83b-143">The following image shows an example of a delivery options module on a checkout page.</span></span>
 
    ![Tarnevalikute mooduli näide](./media/ecommerce-deliveryoptions.PNG)

- <span data-ttu-id="1e83b-145">**Maksmise jaotise konteiner** – see moodul on konteiner, kuhu saate lisada mitu moodulit, et luua jaotis maksmise voo sees.</span><span class="sxs-lookup"><span data-stu-id="1e83b-145">**Checkout section container** – This module is a container that you can put multiple modules inside to create a section within the checkout flow.</span></span> <span data-ttu-id="1e83b-146">Näiteks saate panna sellesse konteinerisse kõik maksmisega seotud moodulid, et need kuvataks ühe jaotisena.</span><span class="sxs-lookup"><span data-stu-id="1e83b-146">For example, you can put all payment-related modules inside this container to make them appear as one section.</span></span> <span data-ttu-id="1e83b-147">See moodul mõjutab ainult voo paigutust.</span><span class="sxs-lookup"><span data-stu-id="1e83b-147">This module affects only the layout of the flow.</span></span>

- <span data-ttu-id="1e83b-148">**Kinkekaart** – see moodul võimaldab kliendil tasuda tellimuse eest kinkekaardiga.</span><span class="sxs-lookup"><span data-stu-id="1e83b-148">**Gift card** – This module lets a customer pay for an order by using a gift card.</span></span> <span data-ttu-id="1e83b-149">Lisateavet selle mooduli kohta leiate teemast [Kinkekaardi moodul](add-giftcard.md).</span><span class="sxs-lookup"><span data-stu-id="1e83b-149">For more information about this module, see [Gift card module](add-giftcard.md).</span></span>

- <span data-ttu-id="1e83b-150">**Püsikliendi punktid** – see moodul võimaldab kliendil tasuda tellimuse eest püsikliendi punktidega.</span><span class="sxs-lookup"><span data-stu-id="1e83b-150">**Loyalty points** – This module lets a customer pay for an order by using loyalty points.</span></span> <span data-ttu-id="1e83b-151">See esitab saadaolevate punktide ja aeguvate punktide kokkuvõtte ja võimaldab klientidel valida lunastamiseks punktide arvu.</span><span class="sxs-lookup"><span data-stu-id="1e83b-151">It provides a summary of available points and expiring points, and lets the customer select the number of points to redeem.</span></span> <span data-ttu-id="1e83b-152">Kui klient ei ole sisse logitud või ei ole püsikliendis programmi liige või kui ostukorvi kogusumma on 0 (null), peidetakse see moodul automaatselt.</span><span class="sxs-lookup"><span data-stu-id="1e83b-152">If the customer isn't signed in or isn't a loyalty member, or if the total amount in the cart is 0 (zero), this module is automatically hidden.</span></span>

- <span data-ttu-id="1e83b-153">**Makse** – see moodul võimaldab kliendil tasuda tellimuse eest krediit- või deebetkaardiga.</span><span class="sxs-lookup"><span data-stu-id="1e83b-153">**Payment** – This module lets a customer pay for an order by using a credit or debit card.</span></span> <span data-ttu-id="1e83b-154">Kliendid saavad sisestada ka valitud makseviisi jaoks arveaadressi.</span><span class="sxs-lookup"><span data-stu-id="1e83b-154">Customers can also provide a billing address for the payment option that they select.</span></span> <span data-ttu-id="1e83b-155">Lisateavet selle mooduli kohta leiate teemast [Maksemoodul](payment-module.md).</span><span class="sxs-lookup"><span data-stu-id="1e83b-155">For more information about this module, see [Payment module](payment-module.md).</span></span>

    <span data-ttu-id="1e83b-156">Järgmisel pildil on näide kinkekaardi, boonuspunktide ja maksemoodulitest maksmise lehel.</span><span class="sxs-lookup"><span data-stu-id="1e83b-156">The following image shows an example of gift card, loyalty points, and payment modules on a checkout page.</span></span>

    ![Kinkekaardi, boonuspunktide ja maksemoodulite näide maksmise lehel](./media/ecommerce-payments.PNG)

- <span data-ttu-id="1e83b-158">**Kontaktteave** – see moodul võimaldab kliendil lisada või muuta tellimuse kontaktandmeid (meiliaadress).</span><span class="sxs-lookup"><span data-stu-id="1e83b-158">**Contact information** – This module lets a customer add or change the contact information (email address) for an order.</span></span>

- <span data-ttu-id="1e83b-159">**Tekstiplokk** – see moodul sisaldab mis tahes teateid, mida juhib sisuhaldussüsteem (CMS).</span><span class="sxs-lookup"><span data-stu-id="1e83b-159">**Text block** – This module contains any messaging that is driven by the content management system (CMS).</span></span> <span data-ttu-id="1e83b-160">Näiteks võib see sisaldada teadet, mis ütleb: „Tellimusega esinevate probleemide osas võtke ühendust numbril 1-800-Fabrikam."</span><span class="sxs-lookup"><span data-stu-id="1e83b-160">For example, it might contain a message that states, "For issues with your order, contact 1-800-Fabrikam."</span></span> 

- <span data-ttu-id="1e83b-161">**Maksmise tingimused** – sellest mooduli kuvatakse rikastekst, mis sisaldab tingimusi ja märkeruutu kliendi sisendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="1e83b-161">**Checkout terms and conditions** – This module shows rich text that contains the terms and conditions and a check box for the customer input.</span></span> <span data-ttu-id="1e83b-162">Märkeruut on valikuline ja konfigureeritav.</span><span class="sxs-lookup"><span data-stu-id="1e83b-162">The check box is optional and configurable.</span></span> <span data-ttu-id="1e83b-163">Moodul salvestab sisendi ja seda saab kasutada kontrolliks enne tellimuse esitamise käivitamist, kuid see ei sisaldu tellimuse kokkuvõtte teabes.</span><span class="sxs-lookup"><span data-stu-id="1e83b-163">The input is captured by the module and can be used as a check before order placement is triggered, but it isn't included in the order summary information.</span></span> <span data-ttu-id="1e83b-164">Seda moodulit saab lisada ettevõtte vajaduste järgi tellimuse konteinerisse, maksmise jaotise konteinerisse või tingimuste pessa.</span><span class="sxs-lookup"><span data-stu-id="1e83b-164">This module can be added to the checkout container, checkout section container, or terms and conditions slot, according to business needs.</span></span> <span data-ttu-id="1e83b-165">Kui see lisatakse maksmise konteinerisse või maksmise jaotise konteineri pesasse, kuvatakse see maksmiseprotsessi etapina.</span><span class="sxs-lookup"><span data-stu-id="1e83b-165">If it's added to the checkout container or checkout section container slot, it will appear as a step in the checkout process.</span></span> <span data-ttu-id="1e83b-166">Kui see lisatakse tingimuste pessa, kuvatakse see tellimuse esitamise nupu lähedal.</span><span class="sxs-lookup"><span data-stu-id="1e83b-166">If it's added to the terms and conditions slot, it will appear near the order placement button.</span></span>

    <span data-ttu-id="1e83b-167">Järgmisel pildil on näide tingimustest maksmise lehel.</span><span class="sxs-lookup"><span data-stu-id="1e83b-167">The following image shows an example of terms and conditions on a checkout page.</span></span>

    ![Tingimuste näide maksmise lehel](./media/ecommerce-checkout-terms.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="1e83b-169">Commerce Scale Unitiga suhtlemine</span><span class="sxs-lookup"><span data-stu-id="1e83b-169">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="1e83b-170">Enamik maksmise teabest, näiteks tarneaadress ja tarnemeetod, salvestatakse ostukorvis ja töödeldakse tellimuse osana.</span><span class="sxs-lookup"><span data-stu-id="1e83b-170">Most of the checkout information, such as the shipping address and shipping method, is stored in the cart and processed as part of the order.</span></span> <span data-ttu-id="1e83b-171">Ainus erand on krediitkaardi teave.</span><span class="sxs-lookup"><span data-stu-id="1e83b-171">The only exception is the credit card information.</span></span> <span data-ttu-id="1e83b-172">See teave töödeldakse otse Adyeni makseühenduse abil.</span><span class="sxs-lookup"><span data-stu-id="1e83b-172">This information is processed directly by using the Adyen payment connector.</span></span> <span data-ttu-id="1e83b-173">Makse on autoriseeritud, kuid raha ei võeta enne, kui tellimus on täidetud.</span><span class="sxs-lookup"><span data-stu-id="1e83b-173">The payment is authorized, but it isn't charged until the order is fulfilled.</span></span>

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a><span data-ttu-id="1e83b-174">Lehele maksmise mooduli lisamine ja vajalike atribuutide seadistamine</span><span class="sxs-lookup"><span data-stu-id="1e83b-174">Add a checkout module to a page and set the required properties</span></span>

<span data-ttu-id="1e83b-175">Uuele lehele ostukorvi mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="1e83b-175">To add a checkout module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="1e83b-176">Avage **Fragmendid** ja valige uue fragmendi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1e83b-176">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="1e83b-177">Valige dialoogiboksis **Uus fragment** moodul **Maksma siirdumine**.</span><span class="sxs-lookup"><span data-stu-id="1e83b-177">In the **New fragment** dialog box, select the **Checkout** module.</span></span>
1. <span data-ttu-id="1e83b-178">Avage jaotis **Fragmendi nimi**, sisestage **Maksma siirdumise fragmendi** nimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e83b-178">Under **Fragment name**, enter the name **Checkout fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="1e83b-179">Valige pesa **Maksmise moodul**.</span><span class="sxs-lookup"><span data-stu-id="1e83b-179">Select the **Checkout module** slot.</span></span>
1. <span data-ttu-id="1e83b-180">Valige parempoolsel atribuutide paanil pliiatsisümbol, sisestage väljale pealkirja tekst ja seejärel valige märkesümbol.</span><span class="sxs-lookup"><span data-stu-id="1e83b-180">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="1e83b-181">Valige pesas **Maksmise teave** kolmikpunkt (**...**) ja seejärel valige suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="1e83b-181">In the **Checkout Information** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1e83b-182">Valige dialoogiboksis **Lisamoodul** moodulid **Tarneaadress**, **Tarnevalikud**, **Maksmise jaotise konteiner** ja **Kontaktteave** ning valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e83b-182">In the **Add Module** dialog box, select the **Shipping address**, **Delivery options**, **Checkout section container**, and **Contact information** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="1e83b-183">Valige moodulis **Maksmise jaotise konteiner** kolmikpunkt (**...**) ja seejärel valige suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="1e83b-183">In the **Checkout section container** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1e83b-184">Valige dialoogiboksis **Lisa moodul** moodulid **Kinkekaart**, **Püsiklient** ja **Maksmine** ning seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e83b-184">In the **Add Module** dialog box, select the **Gift card**, **Loyalty**, and **Payment** modules, and then select **OK**.</span></span> <span data-ttu-id="1e83b-185">Sel viisil saate kindlustada, et kõik maksmisviisid ilmuvad jaotises koos.</span><span class="sxs-lookup"><span data-stu-id="1e83b-185">In this way, you make sure that all the payment methods appear together in a section.</span></span>
1. <span data-ttu-id="1e83b-186">Lisage pesas **Tingimused** moodul **Maksmise tingimused**, kui see on vajalik.</span><span class="sxs-lookup"><span data-stu-id="1e83b-186">In the **Terms and conditions** slot, add a **Checkout terms and conditions** module if it's required.</span></span> <span data-ttu-id="1e83b-187">Konfigureerige mooduli atribuutide paanil tingimuste tekst nii nagu vaja.</span><span class="sxs-lookup"><span data-stu-id="1e83b-187">In the module's properties pane, configure the terms and condition text as appropriate.</span></span>
1. <span data-ttu-id="1e83b-188">Valige **Salvesta** ja seejärel fragmendi eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="1e83b-188">Select **Save**, and then select **Preview** to preview the fragment.</span></span> <span data-ttu-id="1e83b-189">Osasid mooduleid, millel ei ole ostukorvi konteksti, ei pruugita eelvaates renderdada.</span><span class="sxs-lookup"><span data-stu-id="1e83b-189">Some modules that don't have a cart context might not be rendered in the preview.</span></span>
1. <span data-ttu-id="1e83b-190">Valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="1e83b-190">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="1e83b-191">Looge mall, mis kasutab uut maksmise fragmenti.</span><span class="sxs-lookup"><span data-stu-id="1e83b-191">Create a template that uses the new checkout fragment.</span></span>
1. <span data-ttu-id="1e83b-192">Looge maksmise leht, mis kasutab uut malli.</span><span class="sxs-lookup"><span data-stu-id="1e83b-192">Create a checkout page that uses the new template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e83b-193">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1e83b-193">Additional resources</span></span>

[<span data-ttu-id="1e83b-194">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="1e83b-194">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1e83b-195">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="1e83b-195">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="1e83b-196">Maksemoodul</span><span class="sxs-lookup"><span data-stu-id="1e83b-196">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="1e83b-197">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="1e83b-197">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="1e83b-198">Tarnevalikute moodul</span><span class="sxs-lookup"><span data-stu-id="1e83b-198">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="1e83b-199">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="1e83b-199">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="1e83b-200">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="1e83b-200">Gift card module</span></span>](add-giftcard.md)
