---
title: Ostukorvi moodul
description: See teema hõlmab ostukorvi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: d9a15f85838849796d6ce4674712636251c75bf3
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818271"
---
# <a name="cart-module"></a><span data-ttu-id="d519c-103">Ostukorvi moodul</span><span class="sxs-lookup"><span data-stu-id="d519c-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d519c-104">See teema hõlmab ostukorvi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="d519c-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d519c-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="d519c-105">Overview</span></span>

<span data-ttu-id="d519c-106">Ostukorvi moodul näitab ostukorvi lisatud kaupasid enne, kui klient on kassasse läinud.</span><span class="sxs-lookup"><span data-stu-id="d519c-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="d519c-107">Moodul näitab ka ostu kokkuvõtet ja võimaldab kliendil rakendada või eemaldada kampaaniakoode.</span><span class="sxs-lookup"><span data-stu-id="d519c-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="d519c-108">Ostukorvi moodul toetab sisselogitud ostu ja külalisostu.</span><span class="sxs-lookup"><span data-stu-id="d519c-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="d519c-109">Samuti toetab see linki **Tagasi ostlema**.</span><span class="sxs-lookup"><span data-stu-id="d519c-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="d519c-110">Saate konfigureerida selle lingi marsruudi jaotises **Saidi sätted \> Laiendused \> Marsruudid**.</span><span class="sxs-lookup"><span data-stu-id="d519c-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="d519c-111">Ostukorvi moodul renderdab andmed ostukorvi ID põhjal, mis on üle kogu saidi saadaval brauseri küpsis.</span><span class="sxs-lookup"><span data-stu-id="d519c-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="d519c-112">Järgmisel pildil on näide Fabrikami saidi ostukorvi lehest.</span><span class="sxs-lookup"><span data-stu-id="d519c-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Ostukorvimooduli näide Fabrikami saidil](./media/cart2.PNG)

<span data-ttu-id="d519c-114">Järgmisel pildil on näide Fabrikami saidi ostukorvi lehest.</span><span class="sxs-lookup"><span data-stu-id="d519c-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="d519c-115">Selles näites on reakaubal töötluskulu.</span><span class="sxs-lookup"><span data-stu-id="d519c-115">In this example, there is a handling fee for a line item.</span></span>

![Ostukorvimooduli näide koos reakauba töötluskuluga](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="d519c-117">Ostukorvi mooduli atribuudid ja pesad</span><span class="sxs-lookup"><span data-stu-id="d519c-117">Cart module properties and slots</span></span>

| <span data-ttu-id="d519c-118">Atribuut</span><span class="sxs-lookup"><span data-stu-id="d519c-118">Property</span></span> | <span data-ttu-id="d519c-119">Väärtused</span><span class="sxs-lookup"><span data-stu-id="d519c-119">Values</span></span> | <span data-ttu-id="d519c-120">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d519c-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="d519c-121">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="d519c-121">Heading</span></span> | <span data-ttu-id="d519c-122">Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**)</span><span class="sxs-lookup"><span data-stu-id="d519c-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="d519c-123">Ostukorvi pealkiri, näiteks „Ostukorv” või „Ostukorvis olevad kaubad”.</span><span class="sxs-lookup"><span data-stu-id="d519c-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="d519c-124">Kuva laost otsas varude tõrked</span><span class="sxs-lookup"><span data-stu-id="d519c-124">Show out of stock errors</span></span> | <span data-ttu-id="d519c-125">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="d519c-125">**True** or **False**</span></span> | <span data-ttu-id="d519c-126">Kui selle atribuudi väärtuseks on seatud **Tõene**, kuvatakse ostukorvilehel varudega seotud tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="d519c-126">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="d519c-127">Soovitame seada selle atribuudi väärtuseks **Tõene**, kui saidil kontrollitakse varusid.</span><span class="sxs-lookup"><span data-stu-id="d519c-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="d519c-128">Kuva reakaupade saatekulud</span><span class="sxs-lookup"><span data-stu-id="d519c-128">Show shipping charges for line items</span></span> | <span data-ttu-id="d519c-129">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="d519c-129">**True** or **False**</span></span> | <span data-ttu-id="d519c-130">Kui selle atribuudi väärtuseks on seatud **Tõene**, kuvatakse ostukorvi reakaupade juures saatekulud, kui see teave on saadaval.</span><span class="sxs-lookup"><span data-stu-id="d519c-130">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="d519c-131">See funktsioon pole Fabrikami kujunduses toetatud, kuna kasutajad valivad tarneviisi alles maksmise voos.</span><span class="sxs-lookup"><span data-stu-id="d519c-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="d519c-132">Kuid seda funktsiooni saab sisse lülitada ka teistes töövoogudes, kui see on rakendatav.</span><span class="sxs-lookup"><span data-stu-id="d519c-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="d519c-133">Moodulid, mida saab ostukorvi moodulis kasutada</span><span class="sxs-lookup"><span data-stu-id="d519c-133">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="d519c-134">**Tekstiplokk** – see moodul toetab ostukorvi mooduli kohandatud sõnumeid.</span><span class="sxs-lookup"><span data-stu-id="d519c-134">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="d519c-135">Sõnumeid juhib sisuhaldussüsteem (CMS).</span><span class="sxs-lookup"><span data-stu-id="d519c-135">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="d519c-136">Lisada on võimalik mis tahes sõnum, näiteks „Tellimusega esinevate probleemide osas võtke ühendust numbril 1-800-Fabrikam”.</span><span class="sxs-lookup"><span data-stu-id="d519c-136">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="d519c-137">**Kaupluse valija** – see moodul kuvab lähedalasuvate poodide loendi, kus kaup on kohapeal olemas.</span><span class="sxs-lookup"><span data-stu-id="d519c-137">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="d519c-138">See võimaldab kasutajatel sisestada asukoha, et leida läheduses asuvad kauplused.</span><span class="sxs-lookup"><span data-stu-id="d519c-138">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="d519c-139">Selle mooduli kohta lisateabe saamiseks vaadake teemat [Poe valija moodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="d519c-139">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="d519c-140">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="d519c-140">Module properties</span></span>

<span data-ttu-id="d519c-141">Jaotises **Saidi sätted \> Laiendused** saab konfigureerida järgmisi ostukorvi mooduli sätteid.</span><span class="sxs-lookup"><span data-stu-id="d519c-141">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="d519c-142">**Maksimaalne kogus** – seda tribuuti kasutatakse iga kauba maksimaalselt ostukorvi lisatava arvu määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="d519c-142">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="d519c-143">Näiteks võib jaemüüja otsustada, et ühe tehinguga saab müüa iga toodet ainult 10 tükki.</span><span class="sxs-lookup"><span data-stu-id="d519c-143">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="d519c-144">**Varud** – varude sätete rakendamise kohta lisateabe saamiseks vt teemat [Varude sätete rakendamine](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="d519c-144">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="d519c-145">**Tagasi ostukorvi** – seda atribuuti kasutatakse ostukorvi lingi **Tagasi ostlema** marsruudi määramiseks.</span><span class="sxs-lookup"><span data-stu-id="d519c-145">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="d519c-146">Protsessi saab konfigureerida saiditasemel, võimaldades jaemüüjatel viia klient tagasi avalehele või saidi mis tahes teisele lehele.</span><span class="sxs-lookup"><span data-stu-id="d519c-146">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="d519c-147">Commerce Scale Unitiga suhtlemine</span><span class="sxs-lookup"><span data-stu-id="d519c-147">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="d519c-148">Ostukorvi moodul toob toote teabe välja Commerce Scale Uniti API-de abil.</span><span class="sxs-lookup"><span data-stu-id="d519c-148">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="d519c-149">Brauseriküpsise ostukorvi ID-d kasutatakse Commerce Sale Unitist kogu tooteteabe toomiseks.</span><span class="sxs-lookup"><span data-stu-id="d519c-149">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="d519c-150">Lehele ostukorvi mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="d519c-150">Add a cart module to a page</span></span>

<span data-ttu-id="d519c-151">Uuele lehele ostukorvi mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d519c-151">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d519c-152">Avage **Fragmendid** ja valige uue fragmendi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d519c-152">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="d519c-153">Valige dialoogiboksis **Uus fragment** moodul **Ostukorv**.</span><span class="sxs-lookup"><span data-stu-id="d519c-153">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="d519c-154">Avage jaotis **Fragmendi nimi**, sisestage **Ostukorvi fragmendi** nimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="d519c-154">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="d519c-155">Valige pesa **Ostukorv**.</span><span class="sxs-lookup"><span data-stu-id="d519c-155">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="d519c-156">Valige parempoolsel atribuutide paanil pliiatsisümbol, sisestage väljale pealkirja tekst ja seejärel valige märkesümbol.</span><span class="sxs-lookup"><span data-stu-id="d519c-156">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="d519c-157">Valige pesas **Ostukorv** kolmikpunkt (**…**) ja seejärel käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="d519c-157">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d519c-158">Valige dialoogiboksis **Lisa moodul** moodul **Kaupluse valija** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="d519c-158">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d519c-159">Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="d519c-159">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="d519c-160">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d519c-160">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="d519c-161">Sisestage dialoogiboksis **Uus mall** jaotises **Malli nimi** mallile nimi.</span><span class="sxs-lookup"><span data-stu-id="d519c-161">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="d519c-162">Valige liigenduspuu jaotises **Sisu** kolmikpunkt (**...**) ja seejärel valige **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="d519c-162">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="d519c-163">Valige dialoogiboksis **Vali fragment** **Ostukorvi fragmendi** fragment ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="d519c-163">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="d519c-164">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="d519c-164">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="d519c-165">Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d519c-165">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="d519c-166">Valige dialoogiboksis **Malli valimine** varem teie loodud mall, sisestage lehe nimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="d519c-166">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="d519c-167">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="d519c-167">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="d519c-168">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="d519c-168">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d519c-169">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d519c-169">Additional resources</span></span>

[<span data-ttu-id="d519c-170">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="d519c-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="d519c-171">Maksmise moodul</span><span class="sxs-lookup"><span data-stu-id="d519c-171">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d519c-172">Maksemoodul</span><span class="sxs-lookup"><span data-stu-id="d519c-172">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="d519c-173">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="d519c-173">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="d519c-174">Tarnevalikute moodul</span><span class="sxs-lookup"><span data-stu-id="d519c-174">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="d519c-175">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="d519c-175">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d519c-176">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="d519c-176">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="d519c-177">Varude saadavuse arvutamine jaemüügikanalite jaoks</span><span class="sxs-lookup"><span data-stu-id="d519c-177">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
