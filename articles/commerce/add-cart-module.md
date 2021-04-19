---
title: Ostukorvi moodul
description: See teema hõlmab ostukasti mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ec8e89ed82bcdffdc21e62d24ad8c8a7d939cdf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797859"
---
# <a name="cart-module"></a><span data-ttu-id="c829e-103">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="c829e-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c829e-104">See teema hõlmab ostukasti mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="c829e-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c829e-105">Ostukorvi moodul näitab ostukorvi lisatud kaupasid enne, kui klient on kassasse läinud.</span><span class="sxs-lookup"><span data-stu-id="c829e-105">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="c829e-106">Moodul näitab ka ostu kokkuvõtet ja võimaldab kliendil rakendada või eemaldada kampaaniakoode.</span><span class="sxs-lookup"><span data-stu-id="c829e-106">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="c829e-107">Ostukorvi moodul toetab sisselogitud ostu ja külalisostu.</span><span class="sxs-lookup"><span data-stu-id="c829e-107">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="c829e-108">Samuti toetab see linki **Tagasi ostlema**.</span><span class="sxs-lookup"><span data-stu-id="c829e-108">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="c829e-109">Saate konfigureerida selle lingi marsruudi jaotises **Saidi sätted \> Laiendused \> Marsruudid**.</span><span class="sxs-lookup"><span data-stu-id="c829e-109">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="c829e-110">Ostukorvi moodul renderdab andmed ostukorvi ID põhjal, mis on üle kogu saidi saadaval brauseri küpsis.</span><span class="sxs-lookup"><span data-stu-id="c829e-110">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="c829e-111">Järgmisel pildil on näide Fabrikami saidi ostukorvi lehest.</span><span class="sxs-lookup"><span data-stu-id="c829e-111">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Ostukorvimooduli näide Fabrikami saidil](./media/cart2.PNG)

<span data-ttu-id="c829e-113">Järgmisel pildil on näide Fabrikami saidi ostukorvi lehest.</span><span class="sxs-lookup"><span data-stu-id="c829e-113">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="c829e-114">Selles näites on reakaubal töötluskulu.</span><span class="sxs-lookup"><span data-stu-id="c829e-114">In this example, there is a handling fee for a line item.</span></span>

![Ostukorvimooduli näide koos reakauba töötluskuluga](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="c829e-116">Ostukorvi mooduli atribuudid ja pesad</span><span class="sxs-lookup"><span data-stu-id="c829e-116">Cart module properties and slots</span></span>

| <span data-ttu-id="c829e-117">Atribuut</span><span class="sxs-lookup"><span data-stu-id="c829e-117">Property</span></span> | <span data-ttu-id="c829e-118">Väärtused</span><span class="sxs-lookup"><span data-stu-id="c829e-118">Values</span></span> | <span data-ttu-id="c829e-119">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c829e-119">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="c829e-120">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="c829e-120">Heading</span></span> | <span data-ttu-id="c829e-121">Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**)</span><span class="sxs-lookup"><span data-stu-id="c829e-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="c829e-122">Ostukorvi pealkiri, näiteks „Ostukorv” või „Ostukorvis olevad kaubad”.</span><span class="sxs-lookup"><span data-stu-id="c829e-122">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="c829e-123">Kuva laost otsas varude tõrked</span><span class="sxs-lookup"><span data-stu-id="c829e-123">Show out of stock errors</span></span> | <span data-ttu-id="c829e-124">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="c829e-124">**True** or **False**</span></span> | <span data-ttu-id="c829e-125">Kui selle atribuudi väärtuseks on seatud **Tõene**, kuvatakse ostukorvilehel varudega seotud tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="c829e-125">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="c829e-126">Soovitame seada selle atribuudi väärtuseks **Tõene**, kui saidil kontrollitakse varusid.</span><span class="sxs-lookup"><span data-stu-id="c829e-126">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="c829e-127">Kuva reakaupade saatekulud</span><span class="sxs-lookup"><span data-stu-id="c829e-127">Show shipping charges for line items</span></span> | <span data-ttu-id="c829e-128">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="c829e-128">**True** or **False**</span></span> | <span data-ttu-id="c829e-129">Kui selle atribuudi väärtuseks on seatud **Tõene**, kuvatakse ostukorvi reakaupade juures saatekulud, kui see teave on saadaval.</span><span class="sxs-lookup"><span data-stu-id="c829e-129">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="c829e-130">See funktsioon pole Fabrikami kujunduses toetatud, kuna kasutajad valivad tarneviisi alles maksmise voos.</span><span class="sxs-lookup"><span data-stu-id="c829e-130">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="c829e-131">Kuid seda funktsiooni saab sisse lülitada ka teistes töövoogudes, kui see on rakendatav.</span><span class="sxs-lookup"><span data-stu-id="c829e-131">However, this feature can be turned on in other workflows if it's applicable.</span></span> |
| <span data-ttu-id="c829e-132">Kuva saadaolevad kampaaniad</span><span class="sxs-lookup"><span data-stu-id="c829e-132">Show available promotions</span></span>| <span data-ttu-id="c829e-133">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="c829e-133">**True** or **False**</span></span> | <span data-ttu-id="c829e-134">Kui selle atribuudi väärtuseks on määratud **Tõene**, kuvatakse ostukorvis selles olevate kaupade alusel saadaolevad kampaaniad.</span><span class="sxs-lookup"><span data-stu-id="c829e-134">If this property is set to **True**, the cart shows available promotions, based on items in the cart.</span></span> <span data-ttu-id="c829e-135">See funktsioon on saadaval Dynamics 365 Commerce'i versioonis 10.0.16.</span><span class="sxs-lookup"><span data-stu-id="c829e-135">This capability is available in the Dynamics 365 Commerce 10.0.16 release.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="c829e-136">Moodulid, mida saab ostukorvi moodulis kasutada</span><span class="sxs-lookup"><span data-stu-id="c829e-136">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="c829e-137">**Tekstiplokk** – see moodul toetab ostukorvi mooduli kohandatud sõnumeid.</span><span class="sxs-lookup"><span data-stu-id="c829e-137">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="c829e-138">Sõnumeid juhib sisuhaldussüsteem (CMS).</span><span class="sxs-lookup"><span data-stu-id="c829e-138">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="c829e-139">Lisada on võimalik mis tahes sõnum, näiteks „Tellimusega esinevate probleemide osas võtke ühendust numbril 1-800-Fabrikam”.</span><span class="sxs-lookup"><span data-stu-id="c829e-139">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="c829e-140">**Kaupluse valija** – see moodul kuvab lähedalasuvate poodide loendi, kus kaup on kohapeal olemas.</span><span class="sxs-lookup"><span data-stu-id="c829e-140">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="c829e-141">See võimaldab kasutajatel sisestada asukoha, et leida läheduses asuvad kauplused.</span><span class="sxs-lookup"><span data-stu-id="c829e-141">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="c829e-142">Selle mooduli kohta lisateabe saamiseks vaadake teemat [Poe valija moodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="c829e-142">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="c829e-143">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="c829e-143">Module properties</span></span>

<span data-ttu-id="c829e-144">Jaotises **Saidi sätted \> Laiendused** saab konfigureerida järgmisi ostukorvi mooduli sätteid.</span><span class="sxs-lookup"><span data-stu-id="c829e-144">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="c829e-145">**Maksimaalne kogus** – seda tribuuti kasutatakse iga kauba maksimaalselt ostukorvi lisatava arvu määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="c829e-145">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="c829e-146">Näiteks võib jaemüüja otsustada, et ühe tehinguga saab müüa iga toodet ainult 10 tükki.</span><span class="sxs-lookup"><span data-stu-id="c829e-146">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="c829e-147">**Varud** – varude sätete rakendamise kohta lisateabe saamiseks vt teemat [Varude sätete rakendamine](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c829e-147">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="c829e-148">**Tagasi ostukorvi** – seda atribuuti kasutatakse ostukorvi lingi **Tagasi ostlema** marsruudi määramiseks.</span><span class="sxs-lookup"><span data-stu-id="c829e-148">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="c829e-149">Protsessi saab konfigureerida saiditasemel, võimaldades jaemüüjatel viia klient tagasi avalehele või saidi mis tahes teisele lehele.</span><span class="sxs-lookup"><span data-stu-id="c829e-149">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c829e-150">Väljalaskes Dynamics 365 Commerce 10.0.14 ja uuemas koondatakse ostukorvis olevad kaubad vastavalt sätetele, mis määratletakse Commerce'i peakontori võrgupoe veebipõhises funktsiooniprofiilis.</span><span class="sxs-lookup"><span data-stu-id="c829e-150">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="c829e-151">Lisateavet selle kohta, kuidas luua vebipõhist funktsiooniprofiili ja määrata kogumile nõutavad atribuudid, leiate teemast [Veebipõhise funktsiooniprofiili loomine](online-functionality-profile.md).</span><span class="sxs-lookup"><span data-stu-id="c829e-151">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="c829e-152">Commerce Scale Unitiga suhtlemine</span><span class="sxs-lookup"><span data-stu-id="c829e-152">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="c829e-153">Ostukorvi moodul toob toote teabe välja Commerce Scale Uniti API-de abil.</span><span class="sxs-lookup"><span data-stu-id="c829e-153">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="c829e-154">Brauseriküpsise ostukorvi ID-d kasutatakse Commerce Sale Unitist kogu tooteteabe toomiseks.</span><span class="sxs-lookup"><span data-stu-id="c829e-154">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="c829e-155">Lehele ostukorvi mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="c829e-155">Add a cart module to a page</span></span>

<span data-ttu-id="c829e-156">Uuele lehele ostukorvi mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="c829e-156">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c829e-157">Avage **Fragmendid** ja valige uue fragmendi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c829e-157">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="c829e-158">Valige dialoogiboksis **Uus fragment** moodul **Ostukorv**.</span><span class="sxs-lookup"><span data-stu-id="c829e-158">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="c829e-159">Avage jaotis **Fragmendi nimi**, sisestage **Ostukorvi fragmendi** nimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c829e-159">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="c829e-160">Valige pesa **Ostukorv**.</span><span class="sxs-lookup"><span data-stu-id="c829e-160">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="c829e-161">Valige parempoolsel atribuutide paanil pliiatsisümbol, sisestage väljale pealkirja tekst ja seejärel valige märkesümbol.</span><span class="sxs-lookup"><span data-stu-id="c829e-161">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="c829e-162">Valige pesas **Ostukorv** kolmikpunkt (**…**) ja seejärel käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="c829e-162">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c829e-163">Valige dialoogiboksis **Lisa moodul** moodul **Kaupluse valija** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="c829e-163">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c829e-164">Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="c829e-164">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c829e-165">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c829e-165">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="c829e-166">Sisestage dialoogiboksis **Uus mall** jaotises **Malli nimi** mallile nimi.</span><span class="sxs-lookup"><span data-stu-id="c829e-166">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="c829e-167">Valige liigenduspuu jaotises **Sisu** kolmikpunkt (**...**) ja seejärel valige **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="c829e-167">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="c829e-168">Valige dialoogiboksis **Vali fragment** **Ostukorvi fragmendi** fragment ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c829e-168">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="c829e-169">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="c829e-169">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c829e-170">Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c829e-170">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="c829e-171">Valige dialoogiboksis **Malli valimine** varem teie loodud mall, sisestage lehe nimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c829e-171">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="c829e-172">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="c829e-172">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="c829e-173">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="c829e-173">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c829e-174">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c829e-174">Additional resources</span></span>

[<span data-ttu-id="c829e-175">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="c829e-175">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="c829e-176">Maksmise moodul</span><span class="sxs-lookup"><span data-stu-id="c829e-176">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c829e-177">Makse moodul</span><span class="sxs-lookup"><span data-stu-id="c829e-177">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="c829e-178">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="c829e-178">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="c829e-179">Tarnevalikute moodul</span><span class="sxs-lookup"><span data-stu-id="c829e-179">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="c829e-180">Järeletulemisteabe moodul</span><span class="sxs-lookup"><span data-stu-id="c829e-180">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="c829e-181">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="c829e-181">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c829e-182">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="c829e-182">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="c829e-183">Varude saadavuse arvutamine jaemüügikanalite jaoks</span><span class="sxs-lookup"><span data-stu-id="c829e-183">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="c829e-184">Funktsiooniprofiili loomine võrgus</span><span class="sxs-lookup"><span data-stu-id="c829e-184">Create an online functionality profile</span></span>](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]