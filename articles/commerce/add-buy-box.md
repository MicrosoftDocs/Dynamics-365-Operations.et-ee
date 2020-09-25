---
title: Ostukasti moodul
description: See teema hõlmab ostukasti mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6556ee8acf1e24a9f6ceddb622960cb3ac891852
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761293"
---
# <a name="buy-box-module"></a><span data-ttu-id="55033-103">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="55033-103">Buy box module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="55033-104">See teema hõlmab ostukasti mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="55033-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="55033-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="55033-105">Overview</span></span>

<span data-ttu-id="55033-106">Mõiste *ostukast* viitab tavaliselt toote üksikasjade lehe alale, mis on lehe kuvatav osa ehk „above the fold” ja mis sisaldab kõige olulisemat teavet, mis on toote ostu tegemiseks vajalik.</span><span class="sxs-lookup"><span data-stu-id="55033-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="55033-107">(Ala, mida nimetatakse inglise keeles „above the fold”, on nähtav, kui leht esmakordselt laeb, ilma et kasutaja peaks hiirega selle nägemiseks kerima.)</span><span class="sxs-lookup"><span data-stu-id="55033-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="55033-108">Ostukasti moodul on spetsiaalne konteiner, mida kasutatakse kõigi moodulite majutamiseks, mis on toote üksikasjade lehe ostukasti alal näidatud.</span><span class="sxs-lookup"><span data-stu-id="55033-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="55033-109">Toote üksikasjade lehe URL sisaldab toote ID-d.</span><span class="sxs-lookup"><span data-stu-id="55033-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="55033-110">Kogu teave, mis on vajalik ostukasti mooduli renderdamiseks, tuletatakse sellest toote ID-st.</span><span class="sxs-lookup"><span data-stu-id="55033-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="55033-111">Kui toote ID-d ei ole, siis ostukasti moodulit ei renderdata lehel õigesti.</span><span class="sxs-lookup"><span data-stu-id="55033-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="55033-112">Seetõttu saab ostukasti moodulit kasutada ainult lehtedel, millel on toote kontekst.</span><span class="sxs-lookup"><span data-stu-id="55033-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="55033-113">Selle kasutamiseks lehel, millel ei ole toote konteksti (nt avaleht või turunduse leht), peate tegema täiendavaid kohandusi.</span><span class="sxs-lookup"><span data-stu-id="55033-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

<span data-ttu-id="55033-114">Järgmisel pildil on näide ostukasti moodulist toote üksikasjade lehel.</span><span class="sxs-lookup"><span data-stu-id="55033-114">The following image shows an example of a buy box module on a product details page.</span></span>

![Ostukasti mooduli näide](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="55033-116">Ostukasti mooduli atribuudid ja pesad</span><span class="sxs-lookup"><span data-stu-id="55033-116">Buy box module properties and slots</span></span> 

<span data-ttu-id="55033-117">Toote üksikasjade lehel on ostukast jaotatud kaheks piirkonnaks: meediumipiirkond vasakul ja sisupiirkond paremal.</span><span class="sxs-lookup"><span data-stu-id="55033-117">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="55033-118">Vaikimisi on meediumipiirkonna veeru ja sisupiirkonna veeru suhe 2:1.</span><span class="sxs-lookup"><span data-stu-id="55033-118">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="55033-119">Mobiilsetel seadmetel on kaks piirkonda virnastatud, nii et üks piirkond ilmub teise piirkonna all.</span><span class="sxs-lookup"><span data-stu-id="55033-119">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="55033-120">Kujundusi saab kasutada veeru laiuse ja virnastamise astme kohandamiseks.</span><span class="sxs-lookup"><span data-stu-id="55033-120">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="55033-121">Ostukasti moodul annab toote pealkirja, kirjelduse, hinna ja hinnangud.</span><span class="sxs-lookup"><span data-stu-id="55033-121">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="55033-122">Samuti laseb see klientidel valida toote variante, millel on erinevad toote atribuudid, nagu suurus, stiil ja värv.</span><span class="sxs-lookup"><span data-stu-id="55033-122">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="55033-123">Kui tootevariant on valitud, värskendatakse ostukasti teisi atribuute (nt toote kirjeldus ja pildid), et näidata variandi teavet.</span><span class="sxs-lookup"><span data-stu-id="55033-123">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="55033-124">Koguse valija on esitatud, et kliendid saaksid määrata ostetavate kaupade koguse.</span><span class="sxs-lookup"><span data-stu-id="55033-124">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="55033-125">Maksimaalset kogust, mida saab osta, saab määrata saidi sätetes.</span><span class="sxs-lookup"><span data-stu-id="55033-125">The maximum quantity that can be purchased can be defined in the site settings.</span></span>

<span data-ttu-id="55033-126">Ostukastist saavad kliendid teha ka selliseid toiminguid nagu toote lisamine ostukorvi, toote lisamine soovinimekirja ja komplekteerimiskoha valimine.</span><span class="sxs-lookup"><span data-stu-id="55033-126">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="55033-127">Neid toiminguid saab teha toote või toote variandiga.</span><span class="sxs-lookup"><span data-stu-id="55033-127">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="55033-128">Toote lisamiseks soovinimekirja peab klient olema sisse logitud.</span><span class="sxs-lookup"><span data-stu-id="55033-128">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="55033-129">Kujundusi saab kasutada ostukasti tooteatribuutide ja tegevuste juhtelementide eemaldamiseks või muutmiseks.</span><span class="sxs-lookup"><span data-stu-id="55033-129">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="55033-130">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="55033-130">Module properties</span></span>

- <span data-ttu-id="55033-131">**Pealkirja silt** – see atribuut määratleb toote pealkirjale pealkirja sildi.</span><span class="sxs-lookup"><span data-stu-id="55033-131">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="55033-132">Kui ostukast on lehe ülaosas, tuleb see atribuut seada väärtusele **h1**, et vastata juurdepääsetavuse standarditele.</span><span class="sxs-lookup"><span data-stu-id="55033-132">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

- <span data-ttu-id="55033-133">**Luba soovitused „osta sarnaseid tooteid”** - See atribuut lubab ostukastis kuvada nende toodete linke, mis sarnanevad praegu kuvatava kaubaga.</span><span class="sxs-lookup"><span data-stu-id="55033-133">**Enable "shop similar looks" recommendations** - This property allows the buy box to show links to products that look similar to the currently viewed item.</span></span> <span data-ttu-id="55033-134">See funktsioon on saadaval kaubanduse väljalaskes 10.0.13 ja uuemas.</span><span class="sxs-lookup"><span data-stu-id="55033-134">This feature is available in Commerce release 10.0.13 and later.</span></span>

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="55033-135">Moodulid, mida saab ostukasti moodulis kasutada</span><span class="sxs-lookup"><span data-stu-id="55033-135">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="55033-136">**Meediumigalerii** – seda moodulit kasutatakse toote üksikasjade lehel toote piltide näitamiseks.</span><span class="sxs-lookup"><span data-stu-id="55033-136">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="55033-137">Selle mooduli kohta lisateabe saamiseks vaadake teemat [Meediumigalerii moodul](media-gallery-module.md).</span><span class="sxs-lookup"><span data-stu-id="55033-137">For more information about this module, see [Media gallery module](media-gallery-module.md).</span></span>
- <span data-ttu-id="55033-138">**Kaupluse valija** – see moodul kuvab lähedalasuvate poodide loendi, kus kaup on kohapeal olemas.</span><span class="sxs-lookup"><span data-stu-id="55033-138">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="55033-139">See võimaldab kasutajatel sisestada asukoha, et leida läheduses asuvad kauplused.</span><span class="sxs-lookup"><span data-stu-id="55033-139">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="55033-140">Selle mooduli kohta lisateabe saamiseks vaadake teemat [Kaupluse valimise moodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="55033-140">For more information about this module, see [Store selector module](store-selector.md).</span></span>
- <span data-ttu-id="55033-141">**Suhtluskanalites jagamine** - Selle mooduli saab lisada ostukasti, et kasutajad saaksid tooteteavet suhtluskanalites jagada.</span><span class="sxs-lookup"><span data-stu-id="55033-141">**Social share** - This module can be added to the buy box to allow users to share product information on social media.</span></span> <span data-ttu-id="55033-142">Lisateabe saamiseks vt [Suhtluskanalites jagamise moodul](social-share-module.md).</span><span class="sxs-lookup"><span data-stu-id="55033-142">For more information, see [Social share module](social-share-module.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="55033-143">Ostukasti mooduli sätted</span><span class="sxs-lookup"><span data-stu-id="55033-143">Buy box module settings</span></span>

<span data-ttu-id="55033-144">Jaotises **Saidi sätted \> Laiendused** saab konfigureerida järgmisi ostukasti mooduli sätteid.</span><span class="sxs-lookup"><span data-stu-id="55033-144">The following buy box module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="55033-145">**Ostukorvi rea koguse piirang** – selle atribuudi abil määratakse, mitu kaubaühikut võib maksimaalselt ostukorvi lisada.</span><span class="sxs-lookup"><span data-stu-id="55033-145">**Cart line quantity limit** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="55033-146">Näiteks võib jaemüüja otsustada, et ühe tehinguga saab müüa iga toodet ainult 10 tükki.</span><span class="sxs-lookup"><span data-stu-id="55033-146">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="55033-147">**Varud** – varude sätete rakendamise kohta lisateabe saamiseks vt teemat [Varude sätete rakendamine](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="55033-147">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="55033-148">**Lisa ostukorvi** – selle atribuudi abil määratakse, mis juhtub pärast kauba lisamist ostukorvi.</span><span class="sxs-lookup"><span data-stu-id="55033-148">**Add to cart** - This property is used to specify the behavior after an item is added to the cart.</span></span> <span data-ttu-id="55033-149">Võimalikud väärtused on **Navigeeri ostukorvi juurde**, **Ära navigeeri ostukorvi juurde** ja **Kuva teatised**.</span><span class="sxs-lookup"><span data-stu-id="55033-149">The possible values are **Navigate to cart**, **Do not navigate to cart**, and **Show notifications**.</span></span> <span data-ttu-id="55033-150">Kui väärtuseks on seatud **Navigeeri ostukorvi juurde**, suunatakse kasutajad pärast kauba lisamist ostukorvi lehele.</span><span class="sxs-lookup"><span data-stu-id="55033-150">When the value is set to **Navigate to cart**, users are sent to the cart page after they add an item.</span></span> <span data-ttu-id="55033-151">Kui väärtuseks on seatud **Ära navigeeri ostukorvi juurde**, ei suunata kasutajaid pärast kauba lisamist ostukorvi lehele.</span><span class="sxs-lookup"><span data-stu-id="55033-151">When the value is set to **Do not navigate to cart**, users aren't sent to the cart page after they add an item.</span></span> <span data-ttu-id="55033-152">Kui väärtuseks on seatud **Kuva teatised**, kuvatakse kasutajatele kinnitusteatis ja nad võivad jätkata toote üksikasjade lehe sirvimist.</span><span class="sxs-lookup"><span data-stu-id="55033-152">When the value is set to **Show notifications**, users are shown a confirmation notification and can continue to browse on the product details page.</span></span> 

    <span data-ttu-id="55033-153">Järgmisel pildil on näide kinnitusteatisest „lisati ostukorvi” Fabrikami saidil.</span><span class="sxs-lookup"><span data-stu-id="55033-153">The following image shows an example of an "added to cart" confirmation notification on the Fabrikam site.</span></span>

    ![Teatise mooduli näide](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="55033-155">Commerce Scale Unitiga suhtlemine</span><span class="sxs-lookup"><span data-stu-id="55033-155">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="55033-156">Ostukasti moodul toob tooteteavet Commerce Scale Uniti rakendusliideste (API-de) abil.</span><span class="sxs-lookup"><span data-stu-id="55033-156">The buy box module retrieves product information by using Commerce Scale Unit application programming interfaces (APIs).</span></span> <span data-ttu-id="55033-157">Kogu teabe toomiseks kasutatakse toote ID-d toote üksikasjade lehel.</span><span class="sxs-lookup"><span data-stu-id="55033-157">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="55033-158">Lehele ostukasti mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="55033-158">Add a buy box module to a page</span></span>

<span data-ttu-id="55033-159">Uuele lehele ostukasti mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="55033-159">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="55033-160">Avage **Fragmendid** ja valige uue fragmendi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="55033-160">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="55033-161">Valige dialoogiboksis **Uus fragment** moodul **Ostukast**.</span><span class="sxs-lookup"><span data-stu-id="55033-161">In the **New fragment** dialog box, select the **Buybox** module.</span></span>
1. <span data-ttu-id="55033-162">Avage jaotis **Fragmendi nimi**, sisestage **Ostukasti fragmendi** nimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="55033-162">Under **Fragment name**, enter the name **Buy box fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="55033-163">Valige ostukasti mooduli pesas **Meediumigalerii** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="55033-163">In the **Media Gallery** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="55033-164">Valige dialoogiboksis **Lisa moodul** moodul **Meediumigalerii** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="55033-164">In the **Add Module** dialog box, select the **Media gallery** module, and then select **OK**.</span></span>
1. <span data-ttu-id="55033-165">Valige ostukasti mooduli pesas **Kaupluse valija** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="55033-165">In the **Store selector** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="55033-166">Valige dialoogiboksis **Lisa moodul** moodul **Kaupluse valija** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="55033-166">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="55033-167">Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="55033-167">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="55033-168">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="55033-168">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="55033-169">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **PDP mall** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="55033-169">In the **New Template** dialog box, under **Template name**, enter **PDP template**, and then select **OK**.</span></span>
1. <span data-ttu-id="55033-170">Valige pesas **Keha** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="55033-170">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="55033-171">Valige dialoogiboksis **Lisa moodul** moodul **Vaikeleht** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="55033-171">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="55033-172">Valige vaikelehe jaotises **Peamine** kolmikpunkt (**...**) ja seejärel valige **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="55033-172">In the **Main** slot of the default page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="55033-173">Valige dialoogiboksis **Vali fragment** varem loodud fragment **Ostukasti fragment** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="55033-173">In the **Select fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="55033-174">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="55033-174">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="55033-175">Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="55033-175">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="55033-176">Valige dialoogiboksis **Vali mall** mall **PDP mall**.</span><span class="sxs-lookup"><span data-stu-id="55033-176">In the **Choose a template** dialog box, select the **PDP template** template.</span></span> <span data-ttu-id="55033-177">Sisestage jaotises **Lehe nimi** väärtus **PDP leht** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="55033-177">Under **Page name**, enter **PDP page**, and then select **OK**.</span></span>
1. <span data-ttu-id="55033-178">Valige uue lehe jaotises **Peamine** kolmikpunkt (**...**) ja seejärel valige **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="55033-178">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="55033-179">Valige dialoogiboksis **Vali fragment** varem loodud fragment **Ostukasti fragment** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="55033-179">In the **Select fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="55033-180">Salvestage ja kuvage lehe eelvaade.</span><span class="sxs-lookup"><span data-stu-id="55033-180">Save and preview the page.</span></span> <span data-ttu-id="55033-181">Lisage eelvaatelehe URL-ile päringustringi parameeter **?productid=&lt;toote ID&gt;**.</span><span class="sxs-lookup"><span data-stu-id="55033-181">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="55033-182">Sel viisil kasutatakse eelvaatelehe laadimiseks ja renderdamiseks toote konteksti.</span><span class="sxs-lookup"><span data-stu-id="55033-182">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="55033-183">Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="55033-183">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="55033-184">Toote üksikasjade lehele peaks ilmuma ostukast.</span><span class="sxs-lookup"><span data-stu-id="55033-184">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="55033-185">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="55033-185">Additional resources</span></span>

[<span data-ttu-id="55033-186">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="55033-186">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="55033-187">Kaupluse valimise moodul</span><span class="sxs-lookup"><span data-stu-id="55033-187">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="55033-188">Meediumigaleriimoodul</span><span class="sxs-lookup"><span data-stu-id="55033-188">Media gallery module</span></span>](media-gallery-module.md)

[<span data-ttu-id="55033-189">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="55033-189">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="55033-190">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="55033-190">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="55033-191">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="55033-191">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="55033-192">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="55033-192">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="55033-193">Päisemoodul</span><span class="sxs-lookup"><span data-stu-id="55033-193">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="55033-194">Jalusemoodul</span><span class="sxs-lookup"><span data-stu-id="55033-194">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="55033-195">Suhtluskanalites jagamise moodul</span><span class="sxs-lookup"><span data-stu-id="55033-195">Social share module</span></span>](social-share-module.md)

[<span data-ttu-id="55033-196">Varude saadavuse arvutamine jaemüügikanalite jaoks</span><span class="sxs-lookup"><span data-stu-id="55033-196">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
