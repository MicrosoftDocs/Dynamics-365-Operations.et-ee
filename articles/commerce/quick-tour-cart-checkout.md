---
title: Ostukorvi ja väljaregistreerimise ülevaade
description: See teema annab ülevaate ostukorvi ja kassa lehtedest rakenduses Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: d0b5a74a9880a5cabfdbc124f557998540c94a4d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792239"
---
# <a name="cart-and-checkout-pages-overview"></a><span data-ttu-id="99afa-103">Ostukorvi ja väljaregistreerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="99afa-103">Cart and checkout pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="99afa-104">See teema annab ülevaate ostukorvi ja kassa lehtedest rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="99afa-104">This topic provides an overview of the cart and checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="99afa-105">E-kaubanduse veebisaidi ostukorvi lehel kuvatakse kõik kaubad, mille klient on ostukorvi lisanud.</span><span class="sxs-lookup"><span data-stu-id="99afa-105">The cart page of an e-Commerce website shows all items that a customer has added to the cart.</span></span> <span data-ttu-id="99afa-106">Ostukorvi lehekülg on ehitatud ostukorvi mooduli abil.</span><span class="sxs-lookup"><span data-stu-id="99afa-106">The cart page is built by using the cart module.</span></span> <span data-ttu-id="99afa-107">Ostukorvi moodul on konteiner, mis majutab kõiki mooduleid, mis on vajalikud ostukorvis olevate kaupade esitlemiseks.</span><span class="sxs-lookup"><span data-stu-id="99afa-107">The cart module is a container that hosts all the modules that are required to showcase items in the cart.</span></span> <span data-ttu-id="99afa-108">Ostukorvi moodul saab kasutada ka teisi mooduleid, et näidata tellimuse kokkuvõtet ja kõiki kliendi tellimusele rakendatud kampaania koode.</span><span class="sxs-lookup"><span data-stu-id="99afa-108">The cart module can also use other modules to show the order summary and any promotional codes that have been applied to the customer order.</span></span>

<span data-ttu-id="99afa-109">E-kaubanduse veebisaidi lehe kassas on üksikasjalik voog, mida kliendid järgivad tellimuse esitamiseks vajaliku teabe sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="99afa-109">The checkout page of an e-Commerce website presents a step-by-step flow that customers follow to enter all the information that is required to place an order.</span></span> <span data-ttu-id="99afa-110">Kassa moodul võib sisaldada mooduleid, mis töötlevad kättetoimetamise aadressi, tarne meetodeid, arveldusteavet, tellimuse kokkuvõtet ja muud kliendi tellimustega seotud teavet.</span><span class="sxs-lookup"><span data-stu-id="99afa-110">A checkout module can include modules that handle the shipping address, shipping methods, billing information, order summary, and other information that is related to customer orders.</span></span>

## <a name="cart-page"></a><span data-ttu-id="99afa-111">Ostukorvi leht</span><span class="sxs-lookup"><span data-stu-id="99afa-111">Cart page</span></span>

<span data-ttu-id="99afa-112">Ostukorvi lehekülg toimib ostukorvina ja sisaldab kõiki ostukorvi lisatud kaupu.</span><span class="sxs-lookup"><span data-stu-id="99afa-112">The cart page serves as the shopping bag and includes all the items that have been added to the cart.</span></span>

<span data-ttu-id="99afa-113">Järgmisel joonisel on kujutatud ostukorvi lehe näide, mis loodi mooduliteegi ja kujunduse „Fabrikam” abil.</span><span class="sxs-lookup"><span data-stu-id="99afa-113">The following illustration show an example of a cart page that was built by using the module library and the "Fabrikam" theme.</span></span>

![Ostukorvi lehe näide](./media/cart2.PNG)

<span data-ttu-id="99afa-115">Ostukorvi lehe põhiosas kuvatakse kõik kaubad, mille klient on ostukorvi lisanud.</span><span class="sxs-lookup"><span data-stu-id="99afa-115">The main body of the cart page shows all the items that the customer has added to the cart.</span></span> <span data-ttu-id="99afa-116">Kõik kehtivad allahindlused on esitletud.</span><span class="sxs-lookup"><span data-stu-id="99afa-116">All applicable discounts are showcased.</span></span> <span data-ttu-id="99afa-117">Need allahindlused hõlmavad keerukaid allahindlusi.</span><span class="sxs-lookup"><span data-stu-id="99afa-117">These discounts include complex discounts.</span></span> <span data-ttu-id="99afa-118">Näideteks on "Osta 3 toodet ja saad 10% soodsamalt" või "Osta pudel ja seljakott, et saada 10% soodustust".</span><span class="sxs-lookup"><span data-stu-id="99afa-118">Examples include "Buy 3 items and get 10% off" or "Buy a bottle and a backpack to get 10% off."</span></span> <span data-ttu-id="99afa-119">Tellimuse kokkuvõtte moodul näitab summat, mis kuulub tasumisele pärast allahindluste, tarnekulude, maksude jms rakendamist.</span><span class="sxs-lookup"><span data-stu-id="99afa-119">The order summary module shows the amount that is due after discounts, shipping, taxes, and so on, have been applied.</span></span> <span data-ttu-id="99afa-120">On olemas ka promokoodi moodul, mis võimaldab kliendil rakendada või eemaldada kampaania koode.</span><span class="sxs-lookup"><span data-stu-id="99afa-120">There is also a promo code module that lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="99afa-121">Klient saab sisseoste teha anonüümselt või sisselogitud kasutajana.</span><span class="sxs-lookup"><span data-stu-id="99afa-121">A customer can shop anonymously or as a signed-in user.</span></span> <span data-ttu-id="99afa-122">Kui klient on sisse logitud, säilitatakse ostukorvis olevad kaubad seansside vahel.</span><span class="sxs-lookup"><span data-stu-id="99afa-122">If a customer is signed in, items in the cart are preserved between sessions.</span></span> <span data-ttu-id="99afa-123">Sel viisil saab klient jätkata ostlemist mitmest seadmest.</span><span class="sxs-lookup"><span data-stu-id="99afa-123">In this way, the customer can continue to shop from multiple devices.</span></span>

<span data-ttu-id="99afa-124">Ostukorvist saab klient minna edasi kassasse.</span><span class="sxs-lookup"><span data-stu-id="99afa-124">From the cart, the customer can proceed to checkout.</span></span> <span data-ttu-id="99afa-125">Klient saab käivitada väljaregistreerimise külaliskasutajana või sisselogitud kasutajana.</span><span class="sxs-lookup"><span data-stu-id="99afa-125">A customer can initiate checkout as a guest user or as a signed-in user.</span></span>

<span data-ttu-id="99afa-126">Lisateavet ostukorvi lehe loomise kohta leiate teemast [Ostukorvi mooduli lisamine lehele](add-cart-module.md).</span><span class="sxs-lookup"><span data-stu-id="99afa-126">For information about how to author a cart page, see [Add a cart module to a page](add-cart-module.md).</span></span>

## <a name="checkout-page"></a><span data-ttu-id="99afa-127">Kassa leht</span><span class="sxs-lookup"><span data-stu-id="99afa-127">Checkout page</span></span>

<span data-ttu-id="99afa-128">Kassa leht on koht, kus kliendid sisestavad tellimuse esitamiseks vajaliku teabe.</span><span class="sxs-lookup"><span data-stu-id="99afa-128">The checkout page is where customers enter the information that is required to place an order.</span></span>

<span data-ttu-id="99afa-129">Järgmisel joonisel on kujutatud kassa lehe näide, mis loodi mooduliteegi abil.</span><span class="sxs-lookup"><span data-stu-id="99afa-129">The following illustration show an example of a checkout page that was built by using the module library.</span></span>

![Kassa lehe näide](./media/Checkout.PNG)

<span data-ttu-id="99afa-131">Kassa lehe põhiosa on see, kus kogutakse kogu tellimuse teave.</span><span class="sxs-lookup"><span data-stu-id="99afa-131">The main body of the checkout page is where all the order information is collected.</span></span> <span data-ttu-id="99afa-132">See teave sisaldab tarneaadressi, kohaletoimetamise valikuid ja makseteavet.</span><span class="sxs-lookup"><span data-stu-id="99afa-132">This information includes the shipping address, delivery options, and payment information.</span></span> <span data-ttu-id="99afa-133">Kassas on samm-sammuline voog, sest teave tuleb töödelda kindlas järjekorras.</span><span class="sxs-lookup"><span data-stu-id="99afa-133">Checkout has a step-by-step flow, because the information must be entered in a specific order to be processed.</span></span> <span data-ttu-id="99afa-134">Näiteks tuleb sisestada tarneaadress, enne kui saab tarnekulud arvutada ja makse autoriseerida.</span><span class="sxs-lookup"><span data-stu-id="99afa-134">For example, the shipping address must be entered before the shipping costs can be calculated and the payment can be authorized.</span></span>

### <a name="shipping-address"></a><span data-ttu-id="99afa-135">Tarneaadress</span><span class="sxs-lookup"><span data-stu-id="99afa-135">Shipping address</span></span>

<span data-ttu-id="99afa-136">Tarneaadress on nõutav, kui kaubad tuleb saata.</span><span class="sxs-lookup"><span data-stu-id="99afa-136">A shipping address is required if items must be shipped.</span></span> <span data-ttu-id="99afa-137">Iga asukoha saatmise aadresside vormingut saab konfigureerida rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="99afa-137">The format of shipping addresses for each locale can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="99afa-138">Näiteks kui kaubad saadetakse Ameerika Ühendriikidesse, peab tarneaadress sisaldama tänava aadressi, osariiki ja postiindeksit.</span><span class="sxs-lookup"><span data-stu-id="99afa-138">For example, if the items will be shipped to the United States, the shipping address must include a street address, state, and ZIP Code.</span></span> <span data-ttu-id="99afa-139">Mõned põhilised sisestuse kinnitamised tehakse saatmise aadressi väljade jaoks, nt tähe- ja numbrimärkide, maksimumpikkuse ja numbrite kinnitamine.</span><span class="sxs-lookup"><span data-stu-id="99afa-139">Some basic input validation is done for shipping address fields, such as validation for alphanumeric characters, maximum length, and numbers.</span></span> <span data-ttu-id="99afa-140">Kuigi aadressi enda kehtivust ei kontrollita, saab seda kontrollida kohandatud kolmandate osapoolte teenuste abil.</span><span class="sxs-lookup"><span data-stu-id="99afa-140">Although the validity of the address itself isn't verified, this verification can be done by using customized third-party services.</span></span>

<span data-ttu-id="99afa-141">Tarneaadress rakendatakse kõigile ostukorvi kaupadele, mille jaoks on valitud suvand "tarni".</span><span class="sxs-lookup"><span data-stu-id="99afa-141">The shipping address is applied to all items in the cart that the "ship" option is selected for.</span></span> <span data-ttu-id="99afa-142">Kui kasutate kassa voogu, mille on taganud mooduliteek, ei saa üksikuid ostukorvi tooteid saata erinevatele aadressidele.</span><span class="sxs-lookup"><span data-stu-id="99afa-142">If you use the checkout flow that is provided in the module library, individual cart items can't be shipped to different addresses.</span></span> <span data-ttu-id="99afa-143">Kui vajate seda võimalust, saab seda rakendada kassa moodulite kohandamise kaudu.</span><span class="sxs-lookup"><span data-stu-id="99afa-143">If you require this capability, it can be implemented through customization of the checkout modules.</span></span>

<span data-ttu-id="99afa-144">Kui kättetoimetamise aadress on olemas, kuvatakse rakenduse Dynamics 365 Commerce võrgupoes saadaolevad tarneviisid.</span><span class="sxs-lookup"><span data-stu-id="99afa-144">After the shipping address is provided, the shipping methods that are available from the Dynamics 365 Commerce online store are shown.</span></span> <span data-ttu-id="99afa-145">Kohaletoimetamise meetodeid ja neid toetavaid aadresse saab konfigureerida rakenduses Commerce.</span><span class="sxs-lookup"><span data-stu-id="99afa-145">The shipping methods and the addresses that they support can be configured in Commerce.</span></span>

### <a name="payment"></a><span data-ttu-id="99afa-146">Makse</span><span class="sxs-lookup"><span data-stu-id="99afa-146">Payment</span></span>

<span data-ttu-id="99afa-147">Järgmine etapp kassa voos on makse.</span><span class="sxs-lookup"><span data-stu-id="99afa-147">The next step in the checkout flow is payment.</span></span> <span data-ttu-id="99afa-148">E-kaubanduses saab tellimuste täitmiseks kasutada mitut makseviisi, nt krediitkaarte, kinkekaarte ja boonuspunkte.</span><span class="sxs-lookup"><span data-stu-id="99afa-148">In e-Commerce, multiple methods of payment can be used to place orders, such as credit cards, gift cards, and loyalty points.</span></span> <span data-ttu-id="99afa-149">Kasutada saab ka nende makseviiside kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="99afa-149">A combination of these payment methods can also be used.</span></span> <span data-ttu-id="99afa-150">Sõltuvalt kasutatavast makseviisist, võidakse nõuda lisateavet.</span><span class="sxs-lookup"><span data-stu-id="99afa-150">Depending on the payment methods that are used, additional information might be required.</span></span> <span data-ttu-id="99afa-151">Näiteks krediitkaardi makse nõuab arveldamise aadressi.</span><span class="sxs-lookup"><span data-stu-id="99afa-151">For example, a credit card payment requires a billing address.</span></span> <span data-ttu-id="99afa-152">Krediitkaardi makseid töödeldakse Adyen Payment Connectori abil.</span><span class="sxs-lookup"><span data-stu-id="99afa-152">Credit card payments are processed by using the Adyen Payment Connector.</span></span>

#### <a name="loyalty-points"></a><span data-ttu-id="99afa-153">Boonuspunktid</span><span class="sxs-lookup"><span data-stu-id="99afa-153">Loyalty points</span></span>

<span data-ttu-id="99afa-154">Kassas olev klient, kes on püsikliendiprogrammi liige ja kes on kogunud boonuspunkte, saab neid boonuspunkte lunastada tellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="99afa-154">During the checkout flow, a customer who is a member of a loyalty program and who has accrued loyalty points can redeem those loyalty points for an order.</span></span> <span data-ttu-id="99afa-155">Boonuspunktide moodul kuvatakse ainult siis, kui kliendil on olemas püsikliendi liikmelisus.</span><span class="sxs-lookup"><span data-stu-id="99afa-155">The loyalty points module is shown only if the customer has an existing loyalty membership.</span></span> <span data-ttu-id="99afa-156">Mitte-liikmetele ja külaliskasutajatele on see moodul peidetud.</span><span class="sxs-lookup"><span data-stu-id="99afa-156">For non-members and guest users, this module is hidden.</span></span>

#### <a name="gift-cards"></a><span data-ttu-id="99afa-157">Kinkekaardid</span><span class="sxs-lookup"><span data-stu-id="99afa-157">Gift cards</span></span>

<span data-ttu-id="99afa-158">Mooduliteek võimaldab sisemisi kinkekaarte lunastada tellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="99afa-158">The module library lets internal gift cards be redeemed for an order.</span></span> <span data-ttu-id="99afa-159">Sisemise kinkekaardi rakendamiseks peab klient olema sisse logitud.</span><span class="sxs-lookup"><span data-stu-id="99afa-159">To apply an internal gift card, the customer must be signed in.</span></span> <span data-ttu-id="99afa-160">Täiendava turvalisuse tagamiseks soovitame teil voogu kohandada, kasutades sisemiste kinkekaartide jaoks isiklikku tuvastuskoodi (PIN-koodi).</span><span class="sxs-lookup"><span data-stu-id="99afa-160">For additional security, we recommend that you customize the flow by using a personal identification number (PIN) for internal gift cards.</span></span>

### <a name="signed-in-and-guest-users"></a><span data-ttu-id="99afa-161">Sisselogitud ja külaliskasutajad</span><span class="sxs-lookup"><span data-stu-id="99afa-161">Signed-in and guest users</span></span>

<span data-ttu-id="99afa-162">Klient saab lõpetada väljeregistreerimise protsessi külaliskasutajana või sisselogitud kasutajana.</span><span class="sxs-lookup"><span data-stu-id="99afa-162">The customer can complete the checkout process as a guest user or a signed-in user.</span></span> <span data-ttu-id="99afa-163">Kui klient logib sisse, tuuakse automaatselt sisse kontoteave, nt salvestatud tarneaadress ja salvestatud krediitkaardi üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="99afa-163">If the customer signs in, account information such as saved shipping addresses and saved credit card details is automatically retrieved.</span></span>

### <a name="order-summary"></a><span data-ttu-id="99afa-164">Tellimuse kokkuvõte</span><span class="sxs-lookup"><span data-stu-id="99afa-164">Order summary</span></span>

<span data-ttu-id="99afa-165">Kassas kuvatakse ostukorvis reaüksuste kokkuvõte, nii et klient saab tellimuse kinnitada, enne kui ta selle esitab.</span><span class="sxs-lookup"><span data-stu-id="99afa-165">Checkout shows a summary of the line items in the cart, so that the customer can verify the order before he or she places it.</span></span> <span data-ttu-id="99afa-166">Reaüksuseid ei saa kassa voo ajal redigeerida.</span><span class="sxs-lookup"><span data-stu-id="99afa-166">The line items can't be edited during the checkout flow.</span></span> <span data-ttu-id="99afa-167">Siiski on olemas linki ostukorvi, juhul kui kasutaja soovib tagasi minna ja reaüksusi redigeerida.</span><span class="sxs-lookup"><span data-stu-id="99afa-167">However, a link to the cart is provided in case the user wants to go back and edit line items.</span></span>

<span data-ttu-id="99afa-168">Pärast seda, kui klient annab tarne- ja arvelduse teabe, peegeldab tellimuse kokkuvõte summat, mis on tasutud pärast boonuspunktide, kinkekaartide ja muude maksete rakendamist.</span><span class="sxs-lookup"><span data-stu-id="99afa-168">After the customer provides shipping and billing information, the order summary reflects the amount that is due after loyalty points, gift cards, and other payments have been applied.</span></span>

### <a name="order-confirmation-and-email"></a><span data-ttu-id="99afa-169">Tellimuse kinnitus ja meil</span><span class="sxs-lookup"><span data-stu-id="99afa-169">Order confirmation and email</span></span>

<span data-ttu-id="99afa-170">Kui klient esitab tellimuse, esitatakse kinnituse number.</span><span class="sxs-lookup"><span data-stu-id="99afa-170">When the customer places an order, a confirmation number is provided.</span></span> <span data-ttu-id="99afa-171">Sel hetkel on makse autoriseeritud, kuid mitte laekunud.</span><span class="sxs-lookup"><span data-stu-id="99afa-171">At this point, the payment has been authorized but not charged.</span></span> <span data-ttu-id="99afa-172">Makse laekub ainult siis, kui tellimus on täidetud (st kui see on saadetud või komplekteeritud).</span><span class="sxs-lookup"><span data-stu-id="99afa-172">The payment will be charged only when the order is fulfilled (that is, when it's either shipped or picked up).</span></span>

<span data-ttu-id="99afa-173">Pärast tellimuse loomist saadetakse kliendile tellimuse kinnituse meilisõnum.</span><span class="sxs-lookup"><span data-stu-id="99afa-173">After an order is created, an order confirmation email is sent to the customer.</span></span>

<span data-ttu-id="99afa-174">Lisateavet kassa lehe loomise kohta leiate teemast [Kassa mooduli lisamine lehele](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="99afa-174">For more information about how to author a checkout page, see [Add a checkout module to a page](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="99afa-175">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="99afa-175">Additional resources</span></span>

[<span data-ttu-id="99afa-176">Avalehe ülevaade</span><span class="sxs-lookup"><span data-stu-id="99afa-176">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="99afa-177">Toote üksikasjade lehe ülevaade</span><span class="sxs-lookup"><span data-stu-id="99afa-177">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="99afa-178">Kontohalduse lehtede ülevaade</span><span class="sxs-lookup"><span data-stu-id="99afa-178">Account management pages overview</span></span>](quick-tour-account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
