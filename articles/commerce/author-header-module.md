---
title: Päise moodul
description: See teema hõlmab päise mooduleid ja kirjeldab, kuidas lehe päiseid rakenduses Microsoft Dynamics 365 Commerce luua.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 569fb5ac3d30be30044ef9b928ecf1f6dde20aab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211420"
---
# <a name="header-module"></a><span data-ttu-id="86629-103">Päisemoodul</span><span class="sxs-lookup"><span data-stu-id="86629-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="86629-104">See teema hõlmab päise mooduleid ja kirjeldab, kuidas lehe päiseid rakenduses Microsoft Dynamics 365 Commerce luua.</span><span class="sxs-lookup"><span data-stu-id="86629-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="86629-105">Rakenduses Dynamics 365 Commerce konfigureeritakse lehe päis lehe fragmentina, mis sisaldab päise-, reklaambänneri ja küpsistega nõustumise mooduleid.</span><span class="sxs-lookup"><span data-stu-id="86629-105">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="86629-106">Päise moodul sisaldab saidi logo, linke navigeerimise hierarhiale, linke teistele saidi lehekülgedele, ostukorvi ikooni moodulit, soovinimekirja sümbolit, sisselogimise suvandeid ja otsinguriba.</span><span class="sxs-lookup"><span data-stu-id="86629-106">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="86629-107">Päise moodul optimeeritakse automaatselt seadmele, millega saiti vaadatakse (teisisõnu töölauga seade või mobiilne seade).</span><span class="sxs-lookup"><span data-stu-id="86629-107">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="86629-108">Näiteks mobiilses seadmes on navigeerimisriba ahendatud nupule **Menüü** (mida nimetatakse mõnikord ka *hamburgerimenüüks*).</span><span class="sxs-lookup"><span data-stu-id="86629-108">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="86629-109">Järgmisel pildil on näide päise moodulist avalehel.</span><span class="sxs-lookup"><span data-stu-id="86629-109">The following image shows an example of a header module on a home page.</span></span>

![Päise mooduli näide](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="86629-111">Päise mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="86629-111">Properties of a header module</span></span>

<span data-ttu-id="86629-112">Päise moodul toetab atribuute **Logo pilt**, **Logo link** ja **Minu konto lingid**.</span><span class="sxs-lookup"><span data-stu-id="86629-112">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="86629-113">Lehel logo määratlemiseks kasutatakse atribuute **Logo pilt** ja **Logo link**.</span><span class="sxs-lookup"><span data-stu-id="86629-113">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="86629-114">Lisateavet vt jaotisest [Logo lisamine](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="86629-114">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="86629-115">Atribuuti **Minu konto lingid** saab kasutada konto lehtede määratlemiseks, millele saidi omanik soovib päises kiirlinke kuvada.</span><span class="sxs-lookup"><span data-stu-id="86629-115">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="86629-116">Päise moodulis saadaolevad moodulid</span><span class="sxs-lookup"><span data-stu-id="86629-116">Modules that are available within a header module</span></span>

<span data-ttu-id="86629-117">Päise moodulis saab kasutada järgmisi mooduleid.</span><span class="sxs-lookup"><span data-stu-id="86629-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="86629-118">**Navigeerimismenüü** – navigeerimismenüü tähistab kanali navigeerimishierarhiat ja teisi staatilisi navigeerimislinke.</span><span class="sxs-lookup"><span data-stu-id="86629-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="86629-119">Lisateavet vt teemast [Navigeerimismenüü moodul](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="86629-119">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="86629-120">**Otsing** – otsingu moodul võimaldab kasutajatel sisestada otsinguterminid toodete otsimiseks.</span><span class="sxs-lookup"><span data-stu-id="86629-120">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="86629-121">Vaikimisi otsingulehe URL ja otsingupäringu parameetrid peavad olema antud jaotises **Saidi sätted \> Laiendused**.</span><span class="sxs-lookup"><span data-stu-id="86629-121">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="86629-122">Otsingu moodulil on atribuudid, mis võimaldavad teil vajadusel otsingunupu peita või soovikohaselt sildistada.</span><span class="sxs-lookup"><span data-stu-id="86629-122">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="86629-123">Otsingumoodul toetab ka automaatse soovitamise valikuid, näiteks nagu toote, võtmesõna ja kategooria otsitulemused.</span><span class="sxs-lookup"><span data-stu-id="86629-123">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="86629-124">**Ostukorvi ikoon** – ostukorvi ikooni moodul tähistab ostukorvi ikooni, mis näitab ostukorvis olevate kaupade arvu igal ajahetkel.</span><span class="sxs-lookup"><span data-stu-id="86629-124">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="86629-125">Lisateavet vt teemast [Ostukorvi ikooni moodul](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="86629-125">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

- <span data-ttu-id="86629-126">**Saidi valija** – saidi valija moodul võimaldab kasutajatel sirvida erinevatel eelmääratletud saitidel, mis põhinevad turul, piirkondadel ja lokaatidel.</span><span class="sxs-lookup"><span data-stu-id="86629-126">**Site selector** - The site selector module lets users browse across different predefined sites, based on market, regions, and locales.</span></span> <span data-ttu-id="86629-127">Lisateabe saamiseks vt [Saidi valija moodul](site-selector.md).</span><span class="sxs-lookup"><span data-stu-id="86629-127">For more information, see [Site selector module](site-selector.md).</span></span>

- <span data-ttu-id="86629-128">**Kaupluse valija** – kaupluse valija moodulit saab lisada päise mooduli kaupluse valija pessa.</span><span class="sxs-lookup"><span data-stu-id="86629-128">**Store selector** - The store selector module can be included in a header module's store selector slot.</span></span> <span data-ttu-id="86629-129">Kasutajad saavad selle abil sirvida ja leida lähedalasuvaid kauplusi.</span><span class="sxs-lookup"><span data-stu-id="86629-129">It lets users browse and find nearby stores.</span></span> <span data-ttu-id="86629-130">Kasutajad saavad määrata ka eelistatud kaupluse.</span><span class="sxs-lookup"><span data-stu-id="86629-130">Users can also specify a preferred store.</span></span> <span data-ttu-id="86629-131">See kauplus kuvatakse seejärel päises.</span><span class="sxs-lookup"><span data-stu-id="86629-131">That store will then be shown in the header.</span></span> <span data-ttu-id="86629-132">Kui kaupluse valija moodul on lisatud päise moodulisse, peab selle atribuudi **Režiim** väärtuseks olema seatud **Kaupluste otsimine**.</span><span class="sxs-lookup"><span data-stu-id="86629-132">When the store selector module is included in the header module, its **Mode** property must be set to **Find stores**.</span></span> <span data-ttu-id="86629-133">Lisateabe saamiseks vt [Kaupluse valija moodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="86629-133">For more information, see [Store selector module](store-selector.md).</span></span>

> [!NOTE]
> - <span data-ttu-id="86629-134">Ostukorvi ikooni mooduli kasutamise tugi päise moodulis on saadaval väljalaskes Dynamics 365 Commerce 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="86629-134">Support for using the cart icon module in header modules is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>
> - <span data-ttu-id="86629-135">Saidi valija mooduli kasutamise tugi päise moodulis on saadaval väljalaskes Dynamics 365 Commerce 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="86629-135">Support for using the site selector module in header modules is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>
> - <span data-ttu-id="86629-136">Kaupluse valija mooduli kasutamise tugi päise moodulis on saadaval väljalaskes Dynamics 365 Commerce 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="86629-136">Support for using the store selector module in header modules is available in the Dynamics 365 Commerce 10.0.15 release.</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="86629-137">Lehele päise fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="86629-137">Create a header fragment for a page</span></span>

<span data-ttu-id="86629-138">Päise fragmendi loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="86629-138">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="86629-139">Avage **Fragmendid** ja valige uue fragmendi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="86629-139">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="86629-140">Valige dialoogiboksis **Uus fragment** moodul **Konteiner**, sisestage fragmendi nimi ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="86629-140">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="86629-141">Valige pesa **Vaikekonteiner** ja seejärel määrake parempoolsel atribuutide paanil atribuudi **Laius** väärtuseks **Täida ekraan**.</span><span class="sxs-lookup"><span data-stu-id="86629-141">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="86629-142">Valige pesas **Vaikekonteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="86629-142">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="86629-143">Valige dialoogiboksis **Lisa moodul** moodulid **Küpsistega nõustumine**, **Päis** ja **Reklaambänner** ning seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="86629-143">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="86629-144">Tehke mooduli **Reklaambänner** atribuutide paanil valikud **Lisa teade** ja **Teade**.</span><span class="sxs-lookup"><span data-stu-id="86629-144">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="86629-145">Lisage dialoogiaknas **Teade** reklaami tekst ja lingid ning klõpsake seejärel nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="86629-145">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="86629-146">Lisage ja konfigureerige mooduli **Küpsistega nõustumine** atribuutide paanil tekst ja link, mis suunab saidi privaatsuspoliitika lehele.</span><span class="sxs-lookup"><span data-stu-id="86629-146">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="86629-147">Valige päise mooduli pesas **Navigeerimismenüü** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="86629-147">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="86629-148">Valige dialoogiboksis **Lisa moodul** moodul **Navigeerimismenüü** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="86629-148">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="86629-149">Tehke navigeerimismenüü mooduli atribuudipaani jaotises **Navigeerimismenüü allikas** valik **Jaemüügiserver**.</span><span class="sxs-lookup"><span data-stu-id="86629-149">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="86629-150">Tehke navigeerimismenüü mooduli atribuudipaani jaotises **Staatilised menüü-üksused** valikud **Lisa menüü-üksus** ja **Menüü-üksus**.</span><span class="sxs-lookup"><span data-stu-id="86629-150">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="86629-151">Sisestage dialoogiboksi **Menüü-üksus** jaotisse **Menüü-üksuse tekst** tekst „Kontakt”.</span><span class="sxs-lookup"><span data-stu-id="86629-151">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="86629-152">Klõpsake dialoogiboksi **Menüü-üksus** jaotises **Menüü-üksuse lingi sihtkoht** käsku **Lisa link**.</span><span class="sxs-lookup"><span data-stu-id="86629-152">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="86629-153">Valige dialoogiaknas **Lisa link** saidi lehe „Kontakt” URL ning seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="86629-153">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="86629-154">Tehke dialoogiaknas **Menüü-üksus** valik **OK**.</span><span class="sxs-lookup"><span data-stu-id="86629-154">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="86629-155">Valige päise mooduli pesas **Otsing** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="86629-155">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="86629-156">Valige dialoogiboksis **Lisa moodul** moodul **Otsing** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="86629-156">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="86629-157">Konfigureerige otsingumooduli atribuutide paanil vajaduse järgi atribuudid.</span><span class="sxs-lookup"><span data-stu-id="86629-157">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="86629-158">Valige päise mooduli pesas **Ostukorvi ikoon** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="86629-158">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="86629-159">Valige dialoogiboksis **Lisa moodul** moodul **Ostukorvi ikoon** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="86629-159">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="86629-160">Konfigureerige ostukorvi ikooni mooduli atribuutide paanil vajaduse järgi atribuudid.</span><span class="sxs-lookup"><span data-stu-id="86629-160">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="86629-161">Kui soovite, et ostukorvi ikoon kuvaks ostukorvi kokkuvõtet (tuntud ka kui miniostukorv), kui kasutaja hiirt selle kohal hoiab, siis valige **Kuva miniostukorv**.</span><span class="sxs-lookup"><span data-stu-id="86629-161">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="86629-162">Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="86629-162">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="86629-163">Päise igal lehel kuvamise tagamiseks järgige neid samme iga malli jaoks, mis on saidi jaoks loodud.</span><span class="sxs-lookup"><span data-stu-id="86629-163">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="86629-164">Lisage mooduli **Vaikeleht** pesas **Päis** loodud jaluse fragment.</span><span class="sxs-lookup"><span data-stu-id="86629-164">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="86629-165">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="86629-165">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86629-166">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="86629-166">Additional resources</span></span>

[<span data-ttu-id="86629-167">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="86629-167">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="86629-168">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="86629-168">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="86629-169">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="86629-169">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="86629-170">Kampaania ribareklaami moodul</span><span class="sxs-lookup"><span data-stu-id="86629-170">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="86629-171">Navigeerimismenüü moodul</span><span class="sxs-lookup"><span data-stu-id="86629-171">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="86629-172">Küpsistega nõustumine</span><span class="sxs-lookup"><span data-stu-id="86629-172">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="86629-173">Jalusemoodul</span><span class="sxs-lookup"><span data-stu-id="86629-173">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="86629-174">Saidi valija moodul</span><span class="sxs-lookup"><span data-stu-id="86629-174">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="86629-175">Kaupluse valimise moodul</span><span class="sxs-lookup"><span data-stu-id="86629-175">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]