---
title: Ostukorvi ja kassa lehtede ülevaade
description: See teema annab ülevaate ostukorvi ja kassa lehtedest rakenduses Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 07905b9a843eb42d3031dcc80b4e185c122a9e50
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002931"
---
# <a name="overview-of-cart-and-checkout-pages"></a><span data-ttu-id="1f231-103">Ostukorvi ja kassa lehtede ülevaade</span><span class="sxs-lookup"><span data-stu-id="1f231-103">Overview of cart and checkout pages</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1f231-104">See teema annab ülevaate ostukorvi ja kassa lehtedest rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1f231-104">This topic provides an overview of the cart and checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1f231-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="1f231-105">Overview</span></span>

<span data-ttu-id="1f231-106">E-kaubanduse veebisaidi ostukorvi lehel kuvatakse kõik kaubad, mille klient on ostukorvi lisanud.</span><span class="sxs-lookup"><span data-stu-id="1f231-106">The cart page of an e-Commerce website shows all items that a customer has added to the cart.</span></span> <span data-ttu-id="1f231-107">Ostukorvi lehekülg on ehitatud ostukorvi mooduli abil.</span><span class="sxs-lookup"><span data-stu-id="1f231-107">The cart page is built by using the cart module.</span></span> <span data-ttu-id="1f231-108">Ostukorvi moodul on konteiner, mis majutab kõiki mooduleid, mis on vajalikud ostukorvis olevate kaupade esitlemiseks.</span><span class="sxs-lookup"><span data-stu-id="1f231-108">The cart module is a container that hosts all the modules that are required to showcase items in the cart.</span></span> <span data-ttu-id="1f231-109">Ostukorvi moodul saab kasutada ka teisi mooduleid, et näidata tellimuse kokkuvõtet ja kõiki kliendi tellimusele rakendatud kampaania koode.</span><span class="sxs-lookup"><span data-stu-id="1f231-109">The cart module can also use other modules to show the order summary and any promotional codes that have been applied to the customer order.</span></span>

<span data-ttu-id="1f231-110">E-kaubanduse veebisaidi lehe kassas on üksikasjalik voog, mida kliendid järgivad tellimuse esitamiseks vajaliku teabe sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="1f231-110">The checkout page of an e-Commerce website presents a step-by-step flow that customers follow to enter all the information that is required to place an order.</span></span> <span data-ttu-id="1f231-111">Kassa moodul võib sisaldada mooduleid, mis töötlevad kättetoimetamise aadressi, tarne meetodeid, arveldusteavet, tellimuse kokkuvõtet ja muud kliendi tellimustega seotud teavet.</span><span class="sxs-lookup"><span data-stu-id="1f231-111">A checkout module can include modules that handle the shipping address, shipping methods, billing information, order summary, and other information that is related to customer orders.</span></span>

## <a name="cart-page"></a><span data-ttu-id="1f231-112">Ostukorvi leht</span><span class="sxs-lookup"><span data-stu-id="1f231-112">Cart page</span></span>

<span data-ttu-id="1f231-113">Ostukorvi lehekülg toimib ostukorvina ja sisaldab kõiki ostukorvi lisatud kaupu.</span><span class="sxs-lookup"><span data-stu-id="1f231-113">The cart page serves as the shopping bag and includes all the items that have been added to the cart.</span></span>

<span data-ttu-id="1f231-114">Järgmisel joonisel on kujutatud ostukorvi lehe näide, mis loodi veebistardikomplekti ja teema "Fabrikam" abil.</span><span class="sxs-lookup"><span data-stu-id="1f231-114">The following illustration show an example of a cart page that was built by using the online starter kit and the "Fabrikam" theme.</span></span>

![Ostukorvi lehe näide](./media/cart2.PNG)

<span data-ttu-id="1f231-116">Ostukorvi lehe põhiosas kuvatakse kõik kaubad, mille klient on ostukorvi lisanud.</span><span class="sxs-lookup"><span data-stu-id="1f231-116">The main body of the cart page shows all the items that the customer has added to the cart.</span></span> <span data-ttu-id="1f231-117">Kõik kehtivad allahindlused on esitletud.</span><span class="sxs-lookup"><span data-stu-id="1f231-117">All applicable discounts are showcased.</span></span> <span data-ttu-id="1f231-118">Need allahindlused hõlmavad keerukaid allahindlusi.</span><span class="sxs-lookup"><span data-stu-id="1f231-118">These discounts include complex discounts.</span></span> <span data-ttu-id="1f231-119">Näideteks on "Osta 3 toodet ja saad 10% soodsamalt" või "Osta pudel ja seljakott, et saada 10% soodustust".</span><span class="sxs-lookup"><span data-stu-id="1f231-119">Examples include "Buy 3 items and get 10% off" or "Buy a bottle and a backpack to get 10% off."</span></span> <span data-ttu-id="1f231-120">Tellimuse kokkuvõtte moodul näitab summat, mis kuulub tasumisele pärast allahindluste, tarnekulude, maksude jms rakendamist.</span><span class="sxs-lookup"><span data-stu-id="1f231-120">The order summary module shows the amount that is due after discounts, shipping, taxes, and so on, have been applied.</span></span> <span data-ttu-id="1f231-121">On olemas ka promokoodi moodul, mis võimaldab kliendil rakendada või eemaldada kampaania koode.</span><span class="sxs-lookup"><span data-stu-id="1f231-121">There is also a promo code module that lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="1f231-122">Klient saab sisseoste teha anonüümselt või sisselogitud kasutajana.</span><span class="sxs-lookup"><span data-stu-id="1f231-122">A customer can shop anonymously or as a signed-in user.</span></span> <span data-ttu-id="1f231-123">Kui klient on sisse logitud, säilitatakse ostukorvis olevad kaubad seansside vahel.</span><span class="sxs-lookup"><span data-stu-id="1f231-123">If a customer is signed in, items in the cart are preserved between sessions.</span></span> <span data-ttu-id="1f231-124">Sel viisil saab klient jätkata ostlemist mitmest seadmest.</span><span class="sxs-lookup"><span data-stu-id="1f231-124">In this way, the customer can continue to shop from multiple devices.</span></span>

<span data-ttu-id="1f231-125">Ostukorvist saab klient minna edasi kassasse.</span><span class="sxs-lookup"><span data-stu-id="1f231-125">From the cart, the customer can proceed to checkout.</span></span> <span data-ttu-id="1f231-126">Klient saab käivitada väljaregistreerimise külaliskasutajana või sisselogitud kasutajana.</span><span class="sxs-lookup"><span data-stu-id="1f231-126">A customer can initiate checkout as a guest user or as a signed-in user.</span></span>

<span data-ttu-id="1f231-127">Lisateavet ostukorvi lehe loomise kohta leiate teemast [Ostukorvi mooduli lisamine lehele](add-cart-module.md).</span><span class="sxs-lookup"><span data-stu-id="1f231-127">For information about how to author a cart page, see [Add a cart module to a page](add-cart-module.md).</span></span>

## <a name="checkout-page"></a><span data-ttu-id="1f231-128">Kassa leht</span><span class="sxs-lookup"><span data-stu-id="1f231-128">Checkout page</span></span>

<span data-ttu-id="1f231-129">Kassa leht on koht, kus kliendid sisestavad tellimuse esitamiseks vajaliku teabe.</span><span class="sxs-lookup"><span data-stu-id="1f231-129">The checkout page is where customers enter the information that is required to place an order.</span></span>

<span data-ttu-id="1f231-130">Järgmisel joonisel on kujutatud kassa lehe näide, mis loodi veebistardikomplekti abil.</span><span class="sxs-lookup"><span data-stu-id="1f231-130">The following illustration show an example of a checkout page that was built by using the online starter kit.</span></span>

![Kassa lehe näide](./media/Checkout.PNG)

<span data-ttu-id="1f231-132">Kassa lehe põhiosa on see, kus kogutakse kogu tellimuse teave.</span><span class="sxs-lookup"><span data-stu-id="1f231-132">The main body of the checkout page is where all the order information is collected.</span></span> <span data-ttu-id="1f231-133">See teave sisaldab tarneaadressi, kohaletoimetamise valikuid ja makseteavet.</span><span class="sxs-lookup"><span data-stu-id="1f231-133">This information includes the shipping address, delivery options, and payment information.</span></span> <span data-ttu-id="1f231-134">Kassas on samm-sammuline voog, sest teave tuleb töödelda kindlas järjekorras.</span><span class="sxs-lookup"><span data-stu-id="1f231-134">Checkout has a step-by-step flow, because the information must be entered in a specific order to be processed.</span></span> <span data-ttu-id="1f231-135">Näiteks tuleb sisestada tarneaadress, enne kui saab tarnekulud arvutada ja makse autoriseerida.</span><span class="sxs-lookup"><span data-stu-id="1f231-135">For example, the shipping address must be entered before the shipping costs can be calculated and the payment can be authorized.</span></span>

### <a name="shipping-address"></a><span data-ttu-id="1f231-136">Tarneaadress</span><span class="sxs-lookup"><span data-stu-id="1f231-136">Shipping address</span></span>

<span data-ttu-id="1f231-137">Tarneaadress on nõutav, kui kaubad tuleb saata.</span><span class="sxs-lookup"><span data-stu-id="1f231-137">A shipping address is required if items must be shipped.</span></span> <span data-ttu-id="1f231-138">Iga asukoha saatmise aadresside vormingut saab konfigureerida rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1f231-138">The format of shipping addresses for each locale can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="1f231-139">Näiteks kui kaubad saadetakse Ameerika Ühendriikidesse, peab tarneaadress sisaldama tänava aadressi, osariiki ja postiindeksit.</span><span class="sxs-lookup"><span data-stu-id="1f231-139">For example, if the items will be shipped to the United States, the shipping address must include a street address, state, and ZIP Code.</span></span> <span data-ttu-id="1f231-140">Mõned põhilised sisestuse kinnitamised tehakse saatmise aadressi väljade jaoks, nt tähe- ja numbrimärkide, maksimumpikkuse ja numbrite kinnitamine.</span><span class="sxs-lookup"><span data-stu-id="1f231-140">Some basic input validation is done for shipping address fields, such as validation for alphanumeric characters, maximum length, and numbers.</span></span> <span data-ttu-id="1f231-141">Kuigi aadressi enda kehtivust ei kontrollita, saab seda kontrollida kohandatud kolmandate osapoolte teenuste abil.</span><span class="sxs-lookup"><span data-stu-id="1f231-141">Although the validity of the address itself isn't verified, this verification can be done by using customized third-party services.</span></span>

<span data-ttu-id="1f231-142">Tarneaadress rakendatakse kõigile ostukorvi kaupadele, mille jaoks on valitud suvand "tarni".</span><span class="sxs-lookup"><span data-stu-id="1f231-142">The shipping address is applied to all items in the cart that the "ship" option is selected for.</span></span> <span data-ttu-id="1f231-143">Kui kasutate kassa voogu, mille on taganud veebistardikomplekt, ei saa üksikuid ostukorvi tooteid saata erinevatele aadressidele.</span><span class="sxs-lookup"><span data-stu-id="1f231-143">If you use the checkout flow that is provided in the online starter kit, individual cart items can't be shipped to different addresses.</span></span> <span data-ttu-id="1f231-144">Kui vajate seda võimalust, saab seda rakendada kassa moodulite kohandamise kaudu.</span><span class="sxs-lookup"><span data-stu-id="1f231-144">If you require this capability, it can be implemented through customization of the checkout modules.</span></span>

<span data-ttu-id="1f231-145">Kui kättetoimetamise aadress on olemas, kuvatakse rakenduse Dynamics 365 Commerce võrgupoes saadaolevad tarneviisid.</span><span class="sxs-lookup"><span data-stu-id="1f231-145">After the shipping address is provided, the shipping methods that are available from the Dynamics 365 Commerce online store are shown.</span></span> <span data-ttu-id="1f231-146">Kohaletoimetamise meetodeid ja neid toetavaid aadresse saab konfigureerida rakenduses Commerce.</span><span class="sxs-lookup"><span data-stu-id="1f231-146">The shipping methods and the addresses that they support can be configured in Commerce.</span></span>

### <a name="payment"></a><span data-ttu-id="1f231-147">Makse</span><span class="sxs-lookup"><span data-stu-id="1f231-147">Payment</span></span>

<span data-ttu-id="1f231-148">Järgmine etapp kassa voos on makse.</span><span class="sxs-lookup"><span data-stu-id="1f231-148">The next step in the checkout flow is payment.</span></span> <span data-ttu-id="1f231-149">E-kaubanduses saab tellimuste täitmiseks kasutada mitut makseviisi, nt krediitkaarte, kinkekaarte ja boonuspunkte.</span><span class="sxs-lookup"><span data-stu-id="1f231-149">In e-Commerce, multiple methods of payment can be used to place orders, such as credit cards, gift cards, and loyalty points.</span></span> <span data-ttu-id="1f231-150">Kasutada saab ka nende makseviiside kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="1f231-150">A combination of these payment methods can also be used.</span></span> <span data-ttu-id="1f231-151">Sõltuvalt kasutatavast makseviisist, võidakse nõuda lisateavet.</span><span class="sxs-lookup"><span data-stu-id="1f231-151">Depending on the payment methods that are used, additional information might be required.</span></span> <span data-ttu-id="1f231-152">Näiteks krediitkaardi makse nõuab arveldamise aadressi.</span><span class="sxs-lookup"><span data-stu-id="1f231-152">For example, a credit card payment requires a billing address.</span></span> <span data-ttu-id="1f231-153">Krediitkaardi makseid töödeldakse Adyen Payment Connectori abil.</span><span class="sxs-lookup"><span data-stu-id="1f231-153">Credit card payments are processed by using the Adyen Payment Connector.</span></span>

#### <a name="loyalty-points"></a><span data-ttu-id="1f231-154">Boonuspunktid</span><span class="sxs-lookup"><span data-stu-id="1f231-154">Loyalty points</span></span>

<span data-ttu-id="1f231-155">Kassas olev klient, kes on püsikliendiprogrammi liige ja kes on kogunud boonuspunkte, saab neid boonuspunkte lunastada tellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="1f231-155">During the checkout flow, a customer who is a member of a loyalty program and who has accrued loyalty points can redeem those loyalty points for an order.</span></span> <span data-ttu-id="1f231-156">Boonuspunktide moodul kuvatakse ainult siis, kui kliendil on olemas püsikliendi liikmelisus.</span><span class="sxs-lookup"><span data-stu-id="1f231-156">The loyalty points module is shown only if the customer has an existing loyalty membership.</span></span> <span data-ttu-id="1f231-157">Mitte-liikmetele ja külaliskasutajatele on see moodul peidetud.</span><span class="sxs-lookup"><span data-stu-id="1f231-157">For non-members and guest users, this module is hidden.</span></span>

#### <a name="gift-cards"></a><span data-ttu-id="1f231-158">Kinkekaardid</span><span class="sxs-lookup"><span data-stu-id="1f231-158">Gift cards</span></span>

<span data-ttu-id="1f231-159">Veebistardikomplekt võimaldab sisemisi kinkekaarte lunastada tellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="1f231-159">The online starter kit lets internal gift cards be redeemed for an order.</span></span> <span data-ttu-id="1f231-160">Sisemise kinkekaardi rakendamiseks peab klient olema sisse logitud.</span><span class="sxs-lookup"><span data-stu-id="1f231-160">To apply an internal gift card, the customer must be signed in.</span></span> <span data-ttu-id="1f231-161">Täiendava turvalisuse tagamiseks soovitame teil voogu kohandada, kasutades sisemiste kinkekaartide jaoks isiklikku tuvastuskoodi (PIN-koodi).</span><span class="sxs-lookup"><span data-stu-id="1f231-161">For additional security, we recommend that you customize the flow by using a personal identification number (PIN) for internal gift cards.</span></span>

### <a name="signed-in-and-guest-users"></a><span data-ttu-id="1f231-162">Sisselogitud ja külaliskasutajad</span><span class="sxs-lookup"><span data-stu-id="1f231-162">Signed-in and guest users</span></span>

<span data-ttu-id="1f231-163">Klient saab lõpetada väljeregistreerimise protsessi külaliskasutajana või sisselogitud kasutajana.</span><span class="sxs-lookup"><span data-stu-id="1f231-163">The customer can complete the checkout process as a guest user or a signed-in user.</span></span> <span data-ttu-id="1f231-164">Kui klient logib sisse, tuuakse automaatselt sisse kontoteave, nt salvestatud tarneaadress ja salvestatud krediitkaardi üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="1f231-164">If the customer signs in, account information such as saved shipping addresses and saved credit card details is automatically retrieved.</span></span>

### <a name="order-summary"></a><span data-ttu-id="1f231-165">Tellimuse kokkuvõte</span><span class="sxs-lookup"><span data-stu-id="1f231-165">Order summary</span></span>

<span data-ttu-id="1f231-166">Kassas kuvatakse ostukorvis reaüksuste kokkuvõte, nii et klient saab tellimuse kinnitada, enne kui ta selle esitab.</span><span class="sxs-lookup"><span data-stu-id="1f231-166">Checkout shows a summary of the line items in the cart, so that the customer can verify the order before he or she places it.</span></span> <span data-ttu-id="1f231-167">Reaüksuseid ei saa kassa voo ajal redigeerida.</span><span class="sxs-lookup"><span data-stu-id="1f231-167">The line items can't be edited during the checkout flow.</span></span> <span data-ttu-id="1f231-168">Siiski on olemas linki ostukorvi, juhul kui kasutaja soovib tagasi minna ja reaüksusi redigeerida.</span><span class="sxs-lookup"><span data-stu-id="1f231-168">However, a link to the cart is provided in case the user wants to go back and edit line items.</span></span>

<span data-ttu-id="1f231-169">Pärast seda, kui klient annab tarne- ja arvelduse teabe, peegeldab tellimuse kokkuvõte summat, mis on tasutud pärast boonuspunktide, kinkekaartide ja muude maksete rakendamist.</span><span class="sxs-lookup"><span data-stu-id="1f231-169">After the customer provides shipping and billing information, the order summary reflects the amount that is due after loyalty points, gift cards, and other payments have been applied.</span></span>

### <a name="order-confirmation-and-email"></a><span data-ttu-id="1f231-170">Tellimuse kinnitus ja meil</span><span class="sxs-lookup"><span data-stu-id="1f231-170">Order confirmation and email</span></span>

<span data-ttu-id="1f231-171">Kui klient esitab tellimuse, esitatakse kinnituse number.</span><span class="sxs-lookup"><span data-stu-id="1f231-171">When the customer places an order, a confirmation number is provided.</span></span> <span data-ttu-id="1f231-172">Sel hetkel on makse autoriseeritud, kuid mitte laekunud.</span><span class="sxs-lookup"><span data-stu-id="1f231-172">At this point, the payment has been authorized but not charged.</span></span> <span data-ttu-id="1f231-173">Makse laekub ainult siis, kui tellimus on täidetud (st kui see on saadetud või komplekteeritud).</span><span class="sxs-lookup"><span data-stu-id="1f231-173">The payment will be charged only when the order is fulfilled (that is, when it's either shipped or picked up).</span></span>

<span data-ttu-id="1f231-174">Pärast tellimuse loomist saadetakse kliendile tellimuse kinnituse meilisõnum.</span><span class="sxs-lookup"><span data-stu-id="1f231-174">After an order is created, an order confirmation email is sent to the customer.</span></span>

<span data-ttu-id="1f231-175">Lisateavet kassa lehe loomise kohta leiate teemast [Kassa mooduli lisamine lehele](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="1f231-175">For more information about how to author a checkout page, see [Add a checkout module to a page](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1f231-176">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1f231-176">Additional resources</span></span>

[<span data-ttu-id="1f231-177">Avalehe ülevaade</span><span class="sxs-lookup"><span data-stu-id="1f231-177">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="1f231-178">Kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade</span><span class="sxs-lookup"><span data-stu-id="1f231-178">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="1f231-179">Toodete üksikasjade lehtede ülevaade</span><span class="sxs-lookup"><span data-stu-id="1f231-179">Overview of product details pages</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="1f231-180">Kontohalduse lehtede ülevaade</span><span class="sxs-lookup"><span data-stu-id="1f231-180">Overview of account management pages</span></span>](quick-tour-account-management.md)
