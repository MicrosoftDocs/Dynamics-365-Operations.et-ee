---
title: Ostukasti moodul
description: See teema hõlmab ostukasti mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 35b7027e0f0b680dd82ebfcea754fef1617c0163
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261394"
---
# <a name="buy-box-module"></a><span data-ttu-id="b7121-103">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="b7121-103">Buy box module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b7121-104">See teema hõlmab ostukasti mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="b7121-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b7121-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="b7121-105">Overview</span></span>

<span data-ttu-id="b7121-106">Mõiste *ostukast* viitab tavaliselt toote üksikasjade lehe alale, mis on lehe kuvatav osa ehk „above the fold” ja mis sisaldab kõige olulisemat teavet, mis on toote ostu tegemiseks vajalik.</span><span class="sxs-lookup"><span data-stu-id="b7121-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="b7121-107">(Ala, mida nimetatakse inglise keeles „above the fold”, on nähtav, kui leht esmakordselt laeb, ilma et kasutaja peaks hiirega selle nägemiseks kerima.)</span><span class="sxs-lookup"><span data-stu-id="b7121-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="b7121-108">Ostukasti moodul on spetsiaalne konteiner, mida kasutatakse kõigi moodulite majutamiseks, mis on toote üksikasjade lehe ostukasti alal näidatud.</span><span class="sxs-lookup"><span data-stu-id="b7121-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="b7121-109">Toote üksikasjade lehe URL sisaldab toote ID-d.</span><span class="sxs-lookup"><span data-stu-id="b7121-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="b7121-110">Kogu teave, mis on vajalik ostukasti mooduli renderdamiseks, tuletatakse sellest toote ID-st.</span><span class="sxs-lookup"><span data-stu-id="b7121-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="b7121-111">Kui toote ID-d ei ole, siis ostukasti moodulit ei renderdata lehel õigesti.</span><span class="sxs-lookup"><span data-stu-id="b7121-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="b7121-112">Seetõttu saab ostukasti moodulit kasutada ainult lehtedel, millel on toote kontekst.</span><span class="sxs-lookup"><span data-stu-id="b7121-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="b7121-113">Selle kasutamiseks lehel, millel ei ole toote konteksti (nt avaleht või turunduse leht), peate tegema täiendavaid kohandusi.</span><span class="sxs-lookup"><span data-stu-id="b7121-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="b7121-114">Ostukasti mooduli atribuudid ja pesad</span><span class="sxs-lookup"><span data-stu-id="b7121-114">Buy box module properties and slots</span></span> 

<span data-ttu-id="b7121-115">Toote üksikasjade lehel on ostukast jaotatud kaheks piirkonnaks: meediumipiirkond vasakul ja sisupiirkond paremal.</span><span class="sxs-lookup"><span data-stu-id="b7121-115">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="b7121-116">Vaikimisi on meediumipiirkonna veeru ja sisupiirkonna veeru suhe 2:1.</span><span class="sxs-lookup"><span data-stu-id="b7121-116">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="b7121-117">Mobiilsetel seadmetel on kaks piirkonda virnastatud, nii et üks piirkond ilmub teise piirkonna all.</span><span class="sxs-lookup"><span data-stu-id="b7121-117">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="b7121-118">Kujundusi saab kasutada veeru laiuse ja virnastamise astme kohandamiseks.</span><span class="sxs-lookup"><span data-stu-id="b7121-118">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="b7121-119">Ostukasti moodul annab toote pealkirja, kirjelduse, hinna ja hinnangud.</span><span class="sxs-lookup"><span data-stu-id="b7121-119">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="b7121-120">Samuti laseb see klientidel valida toote variante, millel on erinevad toote atribuudid, nagu suurus, stiil ja värv.</span><span class="sxs-lookup"><span data-stu-id="b7121-120">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="b7121-121">Kui tootevariant on valitud, värskendatakse ostukasti teisi atribuute (nt toote kirjeldus ja pildid), et näidata variandi teavet.</span><span class="sxs-lookup"><span data-stu-id="b7121-121">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="b7121-122">Koguse valija on esitatud, et kliendid saaksid määrata ostetavate kaupade koguse.</span><span class="sxs-lookup"><span data-stu-id="b7121-122">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="b7121-123">Maksimaalset kogust, mida saab osta, saab määrata saidi sätetes.</span><span class="sxs-lookup"><span data-stu-id="b7121-123">The maximum quantity that can be purchased can be defined in the site settings.</span></span>

<span data-ttu-id="b7121-124">Ostukastist saavad kliendid teha ka selliseid toiminguid nagu toote lisamine ostukorvi, toote lisamine soovinimekirja ja komplekteerimiskoha valimine.</span><span class="sxs-lookup"><span data-stu-id="b7121-124">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="b7121-125">Neid toiminguid saab teha toote või toote variandiga.</span><span class="sxs-lookup"><span data-stu-id="b7121-125">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="b7121-126">Toote lisamiseks soovinimekirja peab klient olema sisse logitud.</span><span class="sxs-lookup"><span data-stu-id="b7121-126">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="b7121-127">Kujundusi saab kasutada ostukasti tooteatribuutide ja tegevuste juhtelementide eemaldamiseks või muutmiseks.</span><span class="sxs-lookup"><span data-stu-id="b7121-127">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="b7121-128">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="b7121-128">Module properties</span></span>

- <span data-ttu-id="b7121-129">**Pealkirja silt** – see atribuut määratleb toote pealkirjale pealkirja sildi.</span><span class="sxs-lookup"><span data-stu-id="b7121-129">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="b7121-130">Kui ostukast on lehe ülaosas, tuleb see atribuut seada väärtusele **h1**, et vastata juurdepääsetavuse standarditele.</span><span class="sxs-lookup"><span data-stu-id="b7121-130">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="b7121-131">Moodulid, mida saab ostukasti moodulis kasutada</span><span class="sxs-lookup"><span data-stu-id="b7121-131">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="b7121-132">**Meediumigalerii** – seda moodulit kasutatakse toote üksikasjade lehel toote piltide näitamiseks.</span><span class="sxs-lookup"><span data-stu-id="b7121-132">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="b7121-133">See võib toetada ühte kuni mitu pilti.</span><span class="sxs-lookup"><span data-stu-id="b7121-133">It can support one to many images.</span></span> <span data-ttu-id="b7121-134">See toetab ka pisipilte.</span><span class="sxs-lookup"><span data-stu-id="b7121-134">It also supports thumbnail images.</span></span> <span data-ttu-id="b7121-135">Pisipildid saab paigutada kas horisontaalselt (reana pildi all) või vertikaalselt (veeruna pildi kõrval).</span><span class="sxs-lookup"><span data-stu-id="b7121-135">The thumbnail images can be arranged either horizontally (as a row below the image) or vertically (as a column next to the image).</span></span> <span data-ttu-id="b7121-136">Meediumigalerii mooduli saab lisada ostukasti mooduli pesale **Meedia**.</span><span class="sxs-lookup"><span data-stu-id="b7121-136">The media gallery module can be added to the **Media** slot in the buy box module.</span></span> <span data-ttu-id="b7121-137">Hetkel toetab see ainult pilte.</span><span class="sxs-lookup"><span data-stu-id="b7121-137">It currently supports only images.</span></span> 
- <span data-ttu-id="b7121-138">**Kaupluse valija** – see moodul kuvab lähedalasuvate poodide loendi, kus kaup on kohapeal olemas.</span><span class="sxs-lookup"><span data-stu-id="b7121-138">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="b7121-139">See võimaldab kasutajatel sisestada asukoha, et leida läheduses asuvad kauplused.</span><span class="sxs-lookup"><span data-stu-id="b7121-139">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="b7121-140">Selle mooduli kohta lisateabe saamiseks vaadake teemat [Poe valija moodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="b7121-140">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="b7121-141">Ostukasti mooduli sätted</span><span class="sxs-lookup"><span data-stu-id="b7121-141">Buy box module settings</span></span>

<span data-ttu-id="b7121-142">Ostukasti moodulitel on kolm seadistust, mida saab konfigureerida jaotises **Saidi sätted \> Laiendused**.</span><span class="sxs-lookup"><span data-stu-id="b7121-142">Buy box modules have three settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="b7121-143">**Maksimaalne kogus** – seda tribuuti kasutatakse iga kauba maksimaalselt ostukorvi lisatava arvu määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="b7121-143">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="b7121-144">Näiteks võib jaemüüja otsustada, et ühe tehinguga saab müüa iga toodet ainult 10 tükki.</span><span class="sxs-lookup"><span data-stu-id="b7121-144">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="b7121-145">**Varude kontroll** – kui väärtus on satud suvandile **Tõene**, saab kauba lisada ostukorvi ainult pärast seda, kui ostukasti moodul on veendunud, et see oleks laos olemas.</span><span class="sxs-lookup"><span data-stu-id="b7121-145">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="b7121-146">See varude kontroll tehakse nii stsenaariumide jaoks, kus kaup saadetakse, kui ka stsenaariumide jaoks, kus sellele tullakse poodi järele.</span><span class="sxs-lookup"><span data-stu-id="b7121-146">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="b7121-147">Kui väärtuseks on seatud suvand **Väär**, siis enne kauba ostukorvi lisamist ja tellimuse esitamist varude kontrolli ei tehta.</span><span class="sxs-lookup"><span data-stu-id="b7121-147">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span> <span data-ttu-id="b7121-148">Lisateavet varude sätete konfigureerimise kohta varukontoris leiate teemast [Jaemüügikanalite varude saadavuse arvutamine](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="b7121-148">For information on how to configure inventory settings in back office, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

- <span data-ttu-id="b7121-149">**Varude puhver** – seda atribuuti kasutatakse varude puhvri arvu määramiseks.</span><span class="sxs-lookup"><span data-stu-id="b7121-149">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="b7121-150">Varusid hallatakse reaalajas ja kui paljud kliendid esitavad tellimusi, võib täpse varude arvu säilitamine olla keeruline.</span><span class="sxs-lookup"><span data-stu-id="b7121-150">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="b7121-151">Kui varude kontroll on tehtud, siis kui varusid on vähem kui puhvri kogus, käsitletakse toodet kui laost otsas.</span><span class="sxs-lookup"><span data-stu-id="b7121-151">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="b7121-152">Seega kui müük toimub kiiresti läbi mitme kanali, nii et varade arv pole täielikult sünkroonitud, on vähem ohtu, et müüakse kaup, mis on laost otsas.</span><span class="sxs-lookup"><span data-stu-id="b7121-152">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="b7121-153">Commerce Scale Unitiga suhtlemine</span><span class="sxs-lookup"><span data-stu-id="b7121-153">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="b7121-154">Ostukasti moodul toob toote teabe välja Commerce Scale Uniti API-de abil.</span><span class="sxs-lookup"><span data-stu-id="b7121-154">The buy box module retrieves product information using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="b7121-155">Kogu teabe toomiseks kasutatakse toote ID-d toote üksikasjade lehel.</span><span class="sxs-lookup"><span data-stu-id="b7121-155">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="b7121-156">Lehele ostukasti mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="b7121-156">Add a buy box module to a page</span></span>

<span data-ttu-id="b7121-157">Uuele lehele ostukasti mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b7121-157">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b7121-158">Looge fragment nimega **ostukasti fragment** ja lisage sellele ostukasti moodul.</span><span class="sxs-lookup"><span data-stu-id="b7121-158">Create a fragment that is named **buy box fragment**, and add a buy box module to it.</span></span>
1. <span data-ttu-id="b7121-159">Lisage ostukasti mooduli pesas **Meedia** meediumigalerii moodul.</span><span class="sxs-lookup"><span data-stu-id="b7121-159">In the **Media** slot of the buy box module, add a media gallery module.</span></span>
1. <span data-ttu-id="b7121-160">Lisage ostukasti mooduli pesasse **Kaupluse valik** kaupluse valija moodul.</span><span class="sxs-lookup"><span data-stu-id="b7121-160">In the **Store selector** slot of the buy box module, add a store selector module.</span></span>
1. <span data-ttu-id="b7121-161">Registreerige leht ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="b7121-161">Check in the page, and publish it.</span></span>
1. <span data-ttu-id="b7121-162">Looge toote üksikasjade lehel jaoks mall ja pange sellele nimeks **PDP mall**.</span><span class="sxs-lookup"><span data-stu-id="b7121-162">Create a template for a product details page, and name it **PDP template**.</span></span>
1. <span data-ttu-id="b7121-163">Lisage vaikeleht.</span><span class="sxs-lookup"><span data-stu-id="b7121-163">Add a default page.</span></span>
1. <span data-ttu-id="b7121-164">Lisage vaikelehe pessa **Peamine** ostukasti fragment.</span><span class="sxs-lookup"><span data-stu-id="b7121-164">In the **Main** slot of the default page, add a buy box fragment.</span></span>
1. <span data-ttu-id="b7121-165">Salvestage mall, lõpetage selle redigeerimine ja seejärel avaldage see.</span><span class="sxs-lookup"><span data-stu-id="b7121-165">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="b7121-166">Kasutage äsja loodud malli, et luua leht, mille nimi on **PDP leht**.</span><span class="sxs-lookup"><span data-stu-id="b7121-166">Use the template that you just created to create a page that is named **PDP page**.</span></span>
1. <span data-ttu-id="b7121-167">Lisage uue lehe pessa **Peamine** ostukasti fragment.</span><span class="sxs-lookup"><span data-stu-id="b7121-167">In the **Main** slot of the new page, add a buy box fragment.</span></span>
1. <span data-ttu-id="b7121-168">Salvestage ja kuvage lehe eelvaade.</span><span class="sxs-lookup"><span data-stu-id="b7121-168">Save and preview the page.</span></span> <span data-ttu-id="b7121-169">Lisage eelvaatelehe URL-ile päringustringi parameeter **?productid=&lt;toote ID&gt;**.</span><span class="sxs-lookup"><span data-stu-id="b7121-169">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="b7121-170">Sel viisil kasutatakse eelvaatelehe laadimiseks ja renderdamiseks toote konteksti.</span><span class="sxs-lookup"><span data-stu-id="b7121-170">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="b7121-171">Salvestage leht, lõpetage selle redigeerimine ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="b7121-171">Save the page, finish editing it, and publish it.</span></span> <span data-ttu-id="b7121-172">Toote üksikasjade lehele peaks ilmuma ostukast.</span><span class="sxs-lookup"><span data-stu-id="b7121-172">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7121-173">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b7121-173">Additional resources</span></span>

[<span data-ttu-id="b7121-174">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="b7121-174">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b7121-175">Kaupluse valimise moodul</span><span class="sxs-lookup"><span data-stu-id="b7121-175">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="b7121-176">Konteineri moodul</span><span class="sxs-lookup"><span data-stu-id="b7121-176">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b7121-177">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="b7121-177">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b7121-178">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="b7121-178">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b7121-179">Väljaregistreerimismoodul</span><span class="sxs-lookup"><span data-stu-id="b7121-179">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b7121-180">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="b7121-180">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b7121-181">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="b7121-181">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b7121-182">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="b7121-182">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="b7121-183">Varude saadavuse arvutamine jaemüügikanalite jaoks</span><span class="sxs-lookup"><span data-stu-id="b7121-183">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
