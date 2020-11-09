---
title: Maksemoodul
description: See teema hõlmab maksemoodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.openlocfilehash: 894ac35973927c193d6e9c54e326daefb8a3f4a5
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055377"
---
# <a name="payment-module"></a><span data-ttu-id="f1e46-103">Maksemoodul</span><span class="sxs-lookup"><span data-stu-id="f1e46-103">Payment module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f1e46-104">See teema hõlmab maksemoodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="f1e46-104">This topic covers the payment module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f1e46-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="f1e46-105">Overview</span></span>

<span data-ttu-id="f1e46-106">Maksemoodul võimaldab klientidel tellimuste eest tasuda krediit-või deebetkaardiga.</span><span class="sxs-lookup"><span data-stu-id="f1e46-106">The payment module lets customers pay for orders by using credit or debit cards.</span></span> <span data-ttu-id="f1e46-107">Selle mooduli puhul võimaldab makseintegratsiooni Dynamics 365 maksekonnektor Adyeni jaoks.</span><span class="sxs-lookup"><span data-stu-id="f1e46-107">Payment integration for this module is provided by the Dynamics 365 Payment Connector for Adyen.</span></span> <span data-ttu-id="f1e46-108">Lisateavet maksekonnektori seadistamise ja konfigureerimise kohta leiate teemast [Dynamics 365 maksekonnektor Adyeni jaoks](dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="f1e46-108">For more information about how to set up and configure the payment connector, see [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).</span></span>

<span data-ttu-id="f1e46-109">Maksemoodul majutab makseteavet, mida edastab Adyen HTML-i tekstisisese raami kaudu (iFrame).</span><span class="sxs-lookup"><span data-stu-id="f1e46-109">The payment module hosts the payment information that is served via Adyen in an HTML inline frame (iframe).</span></span> <span data-ttu-id="f1e46-110">Maksemoodul suhtleb Adyeni makseteabe toomiseks Commerce Scale Unitiga.</span><span class="sxs-lookup"><span data-stu-id="f1e46-110">The payment module interacts with the Commerce Scale Unit to retrieve the Adyen payment information.</span></span> <span data-ttu-id="f1e46-111">Commerce Scale Unitiga suhtlemise tõttu lubab maksemoodul esitada arveaadressi teavet nii iFrame'is kui ka eraldi moodulis.</span><span class="sxs-lookup"><span data-stu-id="f1e46-111">As part of the Commerce Scale Unit interaction, the payment module can allow billing address information to be served either in the iframe or as a separate module.</span></span> <span data-ttu-id="f1e46-112">Fabrikami kujunduses kuvatakse arveaadress eraldi moodulis.</span><span class="sxs-lookup"><span data-stu-id="f1e46-112">In the Fabrikam theme, the billing address is shown in a separate module.</span></span> <span data-ttu-id="f1e46-113">Sellise meetodi puhul on vormindamine paindlikum, sest aadressiridu saab renderdada nii, et need sarnaneksid tarneaadressi ridadega.</span><span class="sxs-lookup"><span data-stu-id="f1e46-113">This approach allows for more formatting flexibility, because the address lines can be rendered so that they resemble the lines of the shipping address.</span></span>

<span data-ttu-id="f1e46-114">Maksemoodul võimaldab ka sisselogitud klientidel oma makseteavet salvestada.</span><span class="sxs-lookup"><span data-stu-id="f1e46-114">The payment module also lets signed-in customers save their payment information.</span></span> <span data-ttu-id="f1e46-115">Makseteavet ja arveaadressi salvestatakse ning hallatakse Adyeni maksekonnektori kaudu.</span><span class="sxs-lookup"><span data-stu-id="f1e46-115">The payment information and billing address are saved and managed via the Adyen payment connector.</span></span>

<span data-ttu-id="f1e46-116">Maksemoodul hõlmab kõiki tellimuse tasusid, mis jäävad pärast boonuspunktide või kinkekaardi kasutamist alles.</span><span class="sxs-lookup"><span data-stu-id="f1e46-116">The payment module covers any order charges that aren't already covered by loyalty points or a gift card.</span></span> <span data-ttu-id="f1e46-117">Kui tellimuse kogusumma eest saab tasuda täielikult boonuspunktide või kinkekaardi abil, siis on maksemoodul peidetud ja klient saab teha tellimuse ilma selleta.</span><span class="sxs-lookup"><span data-stu-id="f1e46-117">If the total for an order is fully covered by loyalty points or gift card credits, the payment module will be hidden, and the customer will be able to place the order without it.</span></span>

<span data-ttu-id="f1e46-118">Adyeni maksekonnektor toetab ka tugevat kliendi autentimist (SCA).</span><span class="sxs-lookup"><span data-stu-id="f1e46-118">The Adyen payment connector also supports strong customer authentication (SCA).</span></span> <span data-ttu-id="f1e46-119">Euroopa Liidu (EL) teise makseteenuste direktiivi (PSD2.0) järgi tuleb veebipoe külastajaid elektroonilise makseviisi kasutamise korral autentida väljaspool veebipoe keskkonda.</span><span class="sxs-lookup"><span data-stu-id="f1e46-119">Part of the European Union (EU) Payment Services Directive 2.0 (PSD2.0) requires that online shoppers be authenticated outside their online shopping experience when they use an electronic payment method.</span></span> <span data-ttu-id="f1e46-120">Maksmisvoo ajal suunatakse kliendid nende pangasaidile.</span><span class="sxs-lookup"><span data-stu-id="f1e46-120">During the checkout flow,  customers are redirected to their banking site.</span></span> <span data-ttu-id="f1e46-121">Seejärel suunatakse nad pärast autentimist tagasi Commerce'i maksmisvoogu.</span><span class="sxs-lookup"><span data-stu-id="f1e46-121">Then, after authentication, they are redirected back to the Commerce checkout flow.</span></span> <span data-ttu-id="f1e46-122">Tagasisuunamise ajal näidatakse teavet, mille klient maksmisvoos sisestas (nt tarneaadress, tarnevalikud, kinkekaardi- ja püsiklienditeave).</span><span class="sxs-lookup"><span data-stu-id="f1e46-122">During this redirection, the information that a customer entered in the checkout flow (for example, the shipping address, delivery options, gift card information, and loyalty information) will persist.</span></span> <span data-ttu-id="f1e46-123">Enne selle funktsiooni sisselülitamist peab maksekonnektor Commerce'i peakontoris SCA jaoks olema konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="f1e46-123">Before you can turn on this feature, the payment connector must be configured for SCA in Commerce headquarters.</span></span> <span data-ttu-id="f1e46-124">Lisateavet leiate teemast [Tugev kliendi autentimine Adyeni kaudu](adyen_redirect.md).</span><span class="sxs-lookup"><span data-stu-id="f1e46-124">For more information, see [Strong Customer Authentication using Adyen](adyen_redirect.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f1e46-125">Adyeni maksekonnektori puhul saab maksemoodulis olevat moodulit iFrame renderdada ainult juhul, kui lisate Adyeni oma saidi lubatud URL-ide loendisse.</span><span class="sxs-lookup"><span data-stu-id="f1e46-125">For the Adyen payment connector, the iframe module in the payment module can be rendered only if you add the Adyen URL to your site's allow list.</span></span> <span data-ttu-id="f1e46-126">Selle etapi lõpule viimiseks lisage **\*.adyen.com** oma saidi sisu turbepoliitika direktiividele **child-src** , **connect-src** , **img-src** , **script-src** ja **style-src**.</span><span class="sxs-lookup"><span data-stu-id="f1e46-126">To complete this step, add **\*.adyen.com** to the **child-src** , **connect-src** , **img-src** , **script-src** , and **style-src** directives of your site's content security policy.</span></span> <span data-ttu-id="f1e46-127">Lisateavet leiate teemast [Sisu turbepoliitika haldamine](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="f1e46-127">For more information, see [Manage Content Security Policy](manage-csp.md).</span></span> 

<span data-ttu-id="f1e46-128">Järgmisel illustratsioonil on näide kinkekaardi, boonuspunktide ja maksemoodulitest maksmise lehel.</span><span class="sxs-lookup"><span data-stu-id="f1e46-128">The following illustration shows an example of gift card, loyalty, and payment modules on a checkout page.</span></span>

![Kinkekaardi, boonuspunktide ja maksemoodulite näide maksmise lehel](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a><span data-ttu-id="f1e46-130">Maksemooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="f1e46-130">Payment module properties</span></span>

| <span data-ttu-id="f1e46-131">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="f1e46-131">Property name</span></span> | <span data-ttu-id="f1e46-132">Väärtused</span><span class="sxs-lookup"><span data-stu-id="f1e46-132">Values</span></span> | <span data-ttu-id="f1e46-133">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="f1e46-133">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="f1e46-134">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="f1e46-134">Heading</span></span> | <span data-ttu-id="f1e46-135">Pealkirja tekst</span><span class="sxs-lookup"><span data-stu-id="f1e46-135">Heading text</span></span> | <span data-ttu-id="f1e46-136">Maksemooduli valikuline pealkiri.</span><span class="sxs-lookup"><span data-stu-id="f1e46-136">An optional heading for the payment module.</span></span> |
| <span data-ttu-id="f1e46-137">IFrame'i kõrgus</span><span class="sxs-lookup"><span data-stu-id="f1e46-137">Height of the iframe</span></span> | <span data-ttu-id="f1e46-138">Pikslid</span><span class="sxs-lookup"><span data-stu-id="f1e46-138">Pixels</span></span> | <span data-ttu-id="f1e46-139">IFrame'i kõrgus pikslites.</span><span class="sxs-lookup"><span data-stu-id="f1e46-139">The iframe height, in pixels.</span></span> <span data-ttu-id="f1e46-140">Kõrgust saab vajaduse järgi reguleerida.</span><span class="sxs-lookup"><span data-stu-id="f1e46-140">The height can be adjusted as required.</span></span> |
| <span data-ttu-id="f1e46-141">Kuva arveaadress</span><span class="sxs-lookup"><span data-stu-id="f1e46-141">Show billing address</span></span> | <span data-ttu-id="f1e46-142">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="f1e46-142">**True** or **False**</span></span> | <span data-ttu-id="f1e46-143">Kui selle atribuudi väärtuseks on seatud **Tõene** , näitab Adyen arveaadressi maksemooduli iFrame'i sees.</span><span class="sxs-lookup"><span data-stu-id="f1e46-143">If this property is set to **True** , the billing address will be served by Adyen inside the payment module iframe.</span></span> <span data-ttu-id="f1e46-144">Kui selle väärtuseks on seatud **Väär** , ei näita Adyen arveaadressi ja Commerce'i kasutaja peab konfigureerima mooduli, et näidata maksmise lehel arveaadressi.</span><span class="sxs-lookup"><span data-stu-id="f1e46-144">If it's set to **False** , the billing address won't be served by Adyen, and a Commerce user will have to configure a module to show the billing address on the checkout page.</span></span> |
| <span data-ttu-id="f1e46-145">Makse stiili tühistamine</span><span class="sxs-lookup"><span data-stu-id="f1e46-145">Payment style override</span></span> | <span data-ttu-id="f1e46-146">Kaskaadlaadistiku (CSS) kood</span><span class="sxs-lookup"><span data-stu-id="f1e46-146">Cascading Style Sheets (CSS) code</span></span> | <span data-ttu-id="f1e46-147">Kuna maksemoodulit majutatakse iFrame'is, on laadi muutmine piiratud.</span><span class="sxs-lookup"><span data-stu-id="f1e46-147">Because the payment module is hosted in an iframe, there is limited styling capability.</span></span> <span data-ttu-id="f1e46-148">Selle atribuudi abil saate laadi veidi muuta.</span><span class="sxs-lookup"><span data-stu-id="f1e46-148">You can achieve some styling by using this property.</span></span> <span data-ttu-id="f1e46-149">Saidi laadide alistamiseks peate kleepima CSS-koodi selle atribuudi väärtusena.</span><span class="sxs-lookup"><span data-stu-id="f1e46-149">To override site styles, you must paste the CSS code as the value of this property.</span></span> <span data-ttu-id="f1e46-150">Selle mooduli puhul ei rakendu saidiehitaja CSS-i alistused ja laadid.</span><span class="sxs-lookup"><span data-stu-id="f1e46-150">Site builder CSS overrides and styles don't apply to this module.</span></span> |

## <a name="billing-address"></a><span data-ttu-id="f1e46-151">Arveaadress</span><span class="sxs-lookup"><span data-stu-id="f1e46-151">Billing address</span></span>

<span data-ttu-id="f1e46-152">Maksemoodul võimaldab klientidel sisestada oma makseteabes arveaadressi.</span><span class="sxs-lookup"><span data-stu-id="f1e46-152">The payment module lets customers provide a billing address for their payment information.</span></span> <span data-ttu-id="f1e46-153">Samuti võimaldab see neil kasutada arveaadressina oma tarneaadressi, et muuta maksmisvoog lihtsamaks ja kiiremaks.</span><span class="sxs-lookup"><span data-stu-id="f1e46-153">It also lets them  use their shipping address as the billing address, to make the checkout flow easier and faster.</span></span> <span data-ttu-id="f1e46-154">Kui atribuudi **Näita arveaadressi** väärtuseks on seatud **Väär** , tuleb maksemoodul konfigureerida maksmise lehel.</span><span class="sxs-lookup"><span data-stu-id="f1e46-154">If the **Show billing address** property is set to **False** , the payment module should be configured on the checkout page.</span></span>

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="f1e46-155">Maksmise lehele maksemooduli lisamine ja vajalike atribuutide seadistamine</span><span class="sxs-lookup"><span data-stu-id="f1e46-155">Add a payment module to a checkout page and set the required properties</span></span>

<span data-ttu-id="f1e46-156">Maksemoodulit saab lisada ainult maksmise moodulisse.</span><span class="sxs-lookup"><span data-stu-id="f1e46-156">A payment module can be added only to a checkout module.</span></span> <span data-ttu-id="f1e46-157">Lisateavet maksmise lehe jaoks maksemooduli konfigureerimise kohta leiate teemast [Maksmise moodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="f1e46-157">For more information about how to configure a payment module for a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1e46-158">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f1e46-158">Additional resources</span></span>

[<span data-ttu-id="f1e46-159">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="f1e46-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f1e46-160">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="f1e46-160">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="f1e46-161">Maksmise moodul</span><span class="sxs-lookup"><span data-stu-id="f1e46-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f1e46-162">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="f1e46-162">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="f1e46-163">Tarnevalikute moodul</span><span class="sxs-lookup"><span data-stu-id="f1e46-163">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="f1e46-164">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="f1e46-164">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f1e46-165">Kinkekaardimoodul</span><span class="sxs-lookup"><span data-stu-id="f1e46-165">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="f1e46-166">Dynamics 365 maksekonnektor Adyeni jaoks</span><span class="sxs-lookup"><span data-stu-id="f1e46-166">Dynamics 365 Payment Connector for Adyen</span></span>](dev-itpro/adyen-connector.md)

[<span data-ttu-id="f1e46-167">Tugev kliendi autentimine Adyeni kaudu</span><span class="sxs-lookup"><span data-stu-id="f1e46-167">Strong Customer Authentication using Adyen</span></span>](adyen_redirect.md)
