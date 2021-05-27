---
title: E-kaubanduse digitaalsed kinkekaardid
description: See teema kirjeldab, kuidas digitaalsed kinkekaardid e-kaubanduses teenuse Microsoft Dynamics 365 Commerce juurutamisel töötavad. Samuti antakse ülevaade olulistest konfigureerimisetappidest.
author: anupamar-ms
ms.date: 12/15/2020
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
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 212f425dc3603f838ce030d9ed86f2e418bef29a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019929"
---
# <a name="e-commerce-digital-gift-cards"></a><span data-ttu-id="6a3b6-104">E-kaubanduse digitaalsed kinkekaardid</span><span class="sxs-lookup"><span data-stu-id="6a3b6-104">E-commerce digital gift cards</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="6a3b6-105">See teema kirjeldab, kuidas digitaalsed kinkekaardid e-kaubanduses teenuse Microsoft Dynamics 365 Commerce juurutamisel töötavad.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-105">This topic describes how digital gift cards work in the e-commerce implementation of Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="6a3b6-106">Samuti antakse ülevaade olulistest konfigureerimisetappidest.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-106">It also provides an overview of important configuration steps.</span></span>

<span data-ttu-id="6a3b6-107">Teenuses Dynamics 365 Commerce järgib digitaalsete kinkekaartide ostmine sama voogu mis muude süsteemi toodete ostmine.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-107">In Dynamics 365 Commerce, the purchase of digital gift cards follows the same flow as the purchase of other products in the system.</span></span> <span data-ttu-id="6a3b6-108">Mingeid lisamooduleid ei ole vaja konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-108">No additional modules have to be configured.</span></span> <span data-ttu-id="6a3b6-109">Kui ostukorvi lisatakse mitu kinkekaarti, ei koondata kinkekaardikaubad ühele müügireale.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-109">If multiple gift cards are added to the cart, the gift card items aren't aggregated on a single sales line.</span></span> <span data-ttu-id="6a3b6-110">Selline käitumine on vajalik, kuna iga müügirea arveldamiseks kasutatakse eraldi kinkekaardi numbrit.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-110">This behavior is required because each sales line is invoiced by using a separate gift card number.</span></span>

<span data-ttu-id="6a3b6-111">Digitaalsete kinkekaartide ostmine on toetatud teenuse Dynamics 365 Commerce versioonis 10.0.16 ja uuemas versioonis.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-111">The purchase of digital gift cards is supported in the Dynamics 365 Commerce 10.0.16 release and later.</span></span>

<span data-ttu-id="6a3b6-112">Järgmisel joonisel on toodud näide toote üksikasjade lehest (PDP) digitaalse kinkekaardi puhul Fabrikami e-kaubanduse saidil.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-112">The following illustration shows an example of the product details page (PDP) for a digital gift card on the Fabrikam e-commerce site.</span></span>

![Digitaalse kinkekaardi PDP näide Fabrikami e-kaubanduse saidil](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a><span data-ttu-id="6a3b6-114">Lülitage Commerce'i peakontoris digitaalse kinkekaardi funktsioon sisse</span><span class="sxs-lookup"><span data-stu-id="6a3b6-114">Turn on the digital gift card feature in Commerce headquarters</span></span>

<span data-ttu-id="6a3b6-115">Selleks et digitaalsete kinkekaartide ostuvoog teenuses Dynamics 365 Commerce töötaks, tuleb Commerce'i peakontoris lülitada sisse funktsioon **E-kaubanduse funktsiooni kaudu kinkekaardi ostmine**.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-115">For the purchase flow for digital gift cards to work in Dynamics 365 Commerce, the **Purchasing gift card on e-Commerce feature** feature must be turned on in Commerce headquarters.</span></span> <span data-ttu-id="6a3b6-116">Funktsioon asub Commerce'i peakontori tööruumis **Funktsionihaldus**, nagu järgmisel joonisel näidatud.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-116">You can find the feature in the **Feature management** workspace in Commerce headquarters, as shown in the following illustration.</span></span>

![Funktsioonihalduse tööruum Commerce'i peakontoris](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a><span data-ttu-id="6a3b6-118">Commerce'i peakontoris digitaalse kinkekaardi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="6a3b6-118">Configure a digital gift card in Commerce headquarters</span></span>

<span data-ttu-id="6a3b6-119">Digitaalsete kinkekaartide tooteid tuleb konfigureerida Commerce'i peakontoris.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-119">Digital gift card products should be configured in Commerce headquarters.</span></span> <span data-ttu-id="6a3b6-120">Protsess sarnaneb muude toodete protsessiga.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-120">The process resembles the process for other products.</span></span> <span data-ttu-id="6a3b6-121">Järgmised olulised etapid käsitlevad konkreetselt ostmiseks kasutatavate kinkekaartide konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-121">However, the following important steps are specific to the configuration of gift cards for purchase.</span></span> <span data-ttu-id="6a3b6-122">Lisateavet toodete loomise ja konfigureerimise kohta vt teemast [Commerce'is uue toote loomine](create-new-product-commerce.md).</span><span class="sxs-lookup"><span data-stu-id="6a3b6-122">For more information about how to create and configure products, see [Create a new product in Commerce](create-new-product-commerce.md).</span></span>

- <span data-ttu-id="6a3b6-123">Kui konfigureerite dialoogiboksis **Uus toode** digitaalsete kinkekaartide tooteid, määrake välja **Toote tüüp** väärtuseks **Teenus**.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-123">When you configure digital gift card products in the **New product** dialog box, set the **Product type** field to **Service**.</span></span> <span data-ttu-id="6a3b6-124">(Dialoogiboksi avamiseks minge lehele **Jaemüügi ja kaubandus \> Tooted ja kategooriad \> Tooted kategooriate alusel** ja valige **Uus**.) Tüübi **Teenus** tooteid ei kontrollita enne tellimuse esitamist saadaolevate varude suhtes.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-124">(To open the dialog box, go to **Retail and commerce \> Products and categories \> Products by category**, and select **New**.) Products of the **Service** type aren't checked for available inventory before an order is placed.</span></span> <span data-ttu-id="6a3b6-125">Lisateavet vt teemast [Uue toote loomine](create-new-product-commerce.md#create-a-new-product).</span><span class="sxs-lookup"><span data-stu-id="6a3b6-125">For more information, see [Create a new product](create-new-product-commerce.md#create-a-new-product).</span></span>
- <span data-ttu-id="6a3b6-126">Lehe **Kaubanduse parameetrid** vahekaardil **Sisestamine** peab väli **Kinkekaarditoode** olema seatud väärtusele **Digitaalne kinkekaart**, nagu järgmisel joonisel näidatud.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-126">On the **Commerce parameters** page, on the **Posting** tab, the **Gift card product** field must be set to **Digital Gift Card**, as shown in the following illustration.</span></span> <span data-ttu-id="6a3b6-127">Kui toode on väline kinkekaart, vaadake lisateavet teemast [Väliste kinkekaartide tugi](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="6a3b6-127">If the product is an external gift card, see [Support for external gift cards](./dev-itpro/gift-card.md) for more information.</span></span>

    ![Kinkekaarditoote väli Commerce'i peakontoris](./media/PostGiftcard.png)

- <span data-ttu-id="6a3b6-129">Kui kinkekaart peab toetama mitmeid eelmääratletud summasid (nt 25, 50 ja 100 $), tuleks nende eelmääratletud summade seadistamiseks kasutada dimensiooni **Suurus**.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-129">If a gift card must support multiple predefined amounts (for example, $25, $50, and $100), the **Size** dimension should be used to set up those predefined amounts.</span></span> <span data-ttu-id="6a3b6-130">Iga eelmääratletud summa on variant.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-130">Each predefined amount will be a variant.</span></span> <span data-ttu-id="6a3b6-131">Lisateavet vt teemast [Toote dimensioonid](../supply-chain/pim/product-dimensions.md?toc=%2fdynamics365%2fretail%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="6a3b6-131">For more information, see [Product dimensions](../supply-chain/pim/product-dimensions.md?toc=%2fdynamics365%2fretail%2ftoc.json).</span></span>
- <span data-ttu-id="6a3b6-132">Kui kliendid peavad saama kinkekaardile kohandatud summat määrata, seadistage esmalt variant, mis lubab kasutada kohandatud summat.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-132">If customers must be able to specify a custom amount for a gift card, first set up a variant that allows for a custom amount.</span></span> <span data-ttu-id="6a3b6-133">Seejärel avage toode lehel **Väljastatud tooted kategooriatena** ja määrake kiirkaardil **Kaubandus** välja **Hinna sisestamine** väärtuseks **Uue hinna sisestamine on kohustuslik**, nagu järgmisel joonisel näidatud.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-133">Next, open the product from the **Released products in category** page, and then, on the **Commerce** FastTab, set the **Key in price** field to **Must key in new price**, as shown in the following illustration.</span></span> <span data-ttu-id="6a3b6-134">See seadistus tagab, et kliendid saavad PDP-s toote sirvimisel hinna sisestada.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-134">This setting ensures that customers can enter a price when they browse the product on a PDP.</span></span>

    ![Hinna sisestamise väli Commerce'i peakontoris](./media/KeyInPrice.png)

- <span data-ttu-id="6a3b6-136">Digitaalse kinkekaardi tarneviisi väärtuseks peab olema määratud **Elektrooniline**.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-136">The mode of delivery for a digital gift card must be set to **Electronic**.</span></span> <span data-ttu-id="6a3b6-137">Valige lehe **Tarneviisid** (**Jaemüük ja kaubandus \> Kanali seadistus \> Tarneviisid**) loendipaanil tarneviis **Elektrooniline** ja seejärel lisage digitaalse kinkekaardi toode kiirkaardi **Tooted** ruudustikku, nagu järgmisel joonisel näidatud.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-137">On the **Modes of delivery** page (**Retail and commerce \> Channel setup \> Modes of delivery**), select the **Electronic** mode of delivery in the list pane, and then add the digital gift card product to the grid on the **Products** FastTab, as shown in the following illustration.</span></span> <span data-ttu-id="6a3b6-138">Lisateavet vt teemast [Tarneviiside seadistamine](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="6a3b6-138">For more information, see [Set up modes of delivery](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

    ![Digitaalsete kinkekaartide tooted Commerce'i peakontori lehel Tarneviisid](./media/ElectronicMode.PNG)

- <span data-ttu-id="6a3b6-140">Veenduge, et Commerce'i peakontoris oleks loodud veebipõhine funktsiooniprofiil ja see oleks teie võrgupoega seostatud.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-140">Make sure that an online functionality profile has been created and associated with your online store in Commerce headquarters.</span></span> <span data-ttu-id="6a3b6-141">Määrake funktsiooniprofiilil suvandi **Liida tooted** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-141">In the functionality profile, set the **Aggregate products** option to **Yes**.</span></span> <span data-ttu-id="6a3b6-142">See seadistus tagab, et kõik kaubad peale kinkekaartide liidetakse.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-142">This setting ensures that all items except gift cards are aggregated.</span></span> <span data-ttu-id="6a3b6-143">Lisateavet vt teemast [Veebipõhise funktsiooniprofiili loomine](online-functionality-profile.md).</span><span class="sxs-lookup"><span data-stu-id="6a3b6-143">For more information, see [Create an online functionality profile](online-functionality-profile.md).</span></span>
- <span data-ttu-id="6a3b6-144">Kui soovite tagada, et kliendid saaksid pärast kinkekaardi arveldamist meili, looge lehel **Meiliteatiste profiilid** uus meiliteatise tüüp ja määrake välja **Meiliteatise tüüp** väärtuseks **Väljasta kinkekaart**.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-144">To ensure that customers receive an email after a gift card is invoiced, create a new email notification type on the **Email notification profiles** page, and set the **Email notification type** field to **Issue gift card**.</span></span> <span data-ttu-id="6a3b6-145">Lisateavet vt teemast [Meiliteatise profiili seadistamine](email-notification-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="6a3b6-145">For more information, see [Set up an email notification profile](email-notification-profiles.md).</span></span>

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a><span data-ttu-id="6a3b6-146">Commerce'i saidiehitaja meediateeki tootepiltide lisamine</span><span class="sxs-lookup"><span data-stu-id="6a3b6-146">Add product images to the Commerce site builder Media library</span></span>

<span data-ttu-id="6a3b6-147">Commerce'i saidiehitaja meediateeki tuleb lisada digitaalsete kinkekaartide toodete jaoks tootepildid.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-147">You must add product images for digital gift card products to the Commerce site builder Media library.</span></span> <span data-ttu-id="6a3b6-148">Veenduge, et kinkekaartide pildifailide failinimed järgiks teie saidi tootepiltide nimemääramisreegleid.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-148">Make sure that the file names of the gift card image files follow your site's naming conventions for product images.</span></span> <span data-ttu-id="6a3b6-149">Lisateavet vt teemast [Piltide üleslaadimine](dam-upload-images.md).</span><span class="sxs-lookup"><span data-stu-id="6a3b6-149">For more information, see [Upload images](dam-upload-images.md).</span></span>

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a><span data-ttu-id="6a3b6-150">Commerce'i saidiehitajas digitaalse kinkekaardi jaoks kohandatud summa konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="6a3b6-150">Configure a custom amount for a digital gift card in Commerce site builder</span></span>

<span data-ttu-id="6a3b6-151">Kui digitaalne kinkekaart on konfigureeritud lubama kohandatud summat, peab see käitumine olema lubatud ka [ostukasti moodulis](add-buy-box.md), mida kasutatakse teie saidi PDP-del.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-151">If a digital gift card is configured to allow for a custom amount, this behavior must also be enabled in the [buy box module](add-buy-box.md) that is used on your site's PDPs.</span></span> <span data-ttu-id="6a3b6-152">Ostukasti moodul toetab mooduli konfiguratsiooni kohandatud summade lubamiseks.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-152">The buy box module supports module configuration to allow for custom amounts.</span></span> <span data-ttu-id="6a3b6-153">Saate määrata ka kohandatud summade puhul lubatud miinimum- ja maksimumsummad.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-153">You can also define the minimum and maximum amounts that are allowed for custom amounts.</span></span>

<span data-ttu-id="6a3b6-154">Commerce'i saidiehitajas digitaalse kinkekaardi jaoks kohandatud summa konfigureerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-154">To configure a custom amount for a digital gift card in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6a3b6-155">Avage teie saidi PDP-del kasutatav ostukasti moodul.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-155">Go to the buy box module that is used on your site's PDPs.</span></span> <span data-ttu-id="6a3b6-156">See ostuboksi moodul võib olla kasutusel fragmendis, mallis või lehel.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-156">This buy box module might be implemented in a fragment, in a template, or on a page.</span></span>
1. <span data-ttu-id="6a3b6-157">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-157">Select **Edit**.</span></span>
1. <span data-ttu-id="6a3b6-158">Valige parempoolsel atribuutide paanil märkeruut **Luba kohandatud hind**.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-158">In the properties pane on the right, select the **Allow custom price** check box.</span></span>
1. <span data-ttu-id="6a3b6-159">Valikuline: kohandatud summade miinimum- ja maksimumsummade määratlemiseks sisestage summad väljale **Miinimumhind** ja **Maksimumhind**.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-159">Optional: To define minimum and maximum amounts for custom amounts, enter amounts under **Minimum price** and **Maximum price**.</span></span>
1. <span data-ttu-id="6a3b6-160">Valige käsk **Lõpeta redigeerimine** ja seejärel käsk **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="6a3b6-160">Select **Finish editing**, and then select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a3b6-161">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6a3b6-161">Additional resources</span></span>

[<span data-ttu-id="6a3b6-162">Ostukastimoodul</span><span class="sxs-lookup"><span data-stu-id="6a3b6-162">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="6a3b6-163">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="6a3b6-163">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="6a3b6-164">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="6a3b6-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="6a3b6-165">Uue toote loomine Commerce'is</span><span class="sxs-lookup"><span data-stu-id="6a3b6-165">Create a new product in Commerce</span></span>](create-new-product-commerce.md)

[<span data-ttu-id="6a3b6-166">Tarneviiside häälestamine</span><span class="sxs-lookup"><span data-stu-id="6a3b6-166">Set up modes of delivery</span></span>](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[<span data-ttu-id="6a3b6-167">Tootedimensioonid</span><span class="sxs-lookup"><span data-stu-id="6a3b6-167">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=%2fdynamics365%2fretail%2ftoc.json)

[<span data-ttu-id="6a3b6-168">Meiliteatise profiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="6a3b6-168">Set up an email notification profile</span></span>](email-notification-profiles.md)

[<span data-ttu-id="6a3b6-169">Funktsiooniprofiili loomine võrgus</span><span class="sxs-lookup"><span data-stu-id="6a3b6-169">Create an online functionality profile</span></span>](online-functionality-profile.md)

[<span data-ttu-id="6a3b6-170">Väliste kinkekaartide tugi</span><span class="sxs-lookup"><span data-stu-id="6a3b6-170">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]