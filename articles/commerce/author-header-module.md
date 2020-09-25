---
title: Päise moodul
description: See teema hõlmab päise mooduleid ja kirjeldab, kuidas lehe päiseid rakenduses Microsoft Dynamics 365 Commerce luua.
author: anupamar
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: eb440a8fb67888c9411ad5998fead4d00982b436
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761220"
---
# <a name="header-module"></a><span data-ttu-id="411f9-103">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="411f9-103">Header module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="411f9-104">See teema hõlmab päise mooduleid ja kirjeldab, kuidas lehe päiseid rakenduses Microsoft Dynamics 365 Commerce luua.</span><span class="sxs-lookup"><span data-stu-id="411f9-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="411f9-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="411f9-105">Overview</span></span>

<span data-ttu-id="411f9-106">Rakenduses Dynamics 365 Commerce konfigureeritakse lehe päis lehe fragmentina, mis sisaldab päise-, reklaambänneri ja küpsistega nõustumise mooduleid.</span><span class="sxs-lookup"><span data-stu-id="411f9-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="411f9-107">Päise moodul sisaldab saidi logo, linke navigeerimise hierarhiale, linke teistele saidi lehekülgedele, ostukorvi ikooni moodulit, soovinimekirja sümbolit, sisselogimise suvandeid ja otsinguriba.</span><span class="sxs-lookup"><span data-stu-id="411f9-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="411f9-108">Päise moodul optimeeritakse automaatselt seadmele, millega saiti vaadatakse (teisisõnu töölauga seade või mobiilne seade).</span><span class="sxs-lookup"><span data-stu-id="411f9-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="411f9-109">Näiteks mobiilses seadmes on navigeerimisriba ahendatud nupule **Menüü** (mida nimetatakse mõnikord ka *hamburgerimenüüks*).</span><span class="sxs-lookup"><span data-stu-id="411f9-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="411f9-110">Järgmisel pildil on näide päise moodulist avalehel.</span><span class="sxs-lookup"><span data-stu-id="411f9-110">The following image shows an example of a header module on a home page.</span></span>

![Päise mooduli näide](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="411f9-112">Päise mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="411f9-112">Properties of a header module</span></span>

<span data-ttu-id="411f9-113">Päise moodul toetab atribuute **Logo pilt**, **Logo link** ja **Minu konto lingid**.</span><span class="sxs-lookup"><span data-stu-id="411f9-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="411f9-114">Lehel logo määratlemiseks kasutatakse atribuute **Logo pilt** ja **Logo link**.</span><span class="sxs-lookup"><span data-stu-id="411f9-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="411f9-115">Lisateavet vt jaotisest [Logo lisamine](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="411f9-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="411f9-116">Atribuuti **Minu konto lingid** saab kasutada konto lehtede määratlemiseks, millele saidi omanik soovib päises kiirlinke kuvada.</span><span class="sxs-lookup"><span data-stu-id="411f9-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="411f9-117">Päise moodulis saadaolevad moodulid</span><span class="sxs-lookup"><span data-stu-id="411f9-117">Modules that are available within a header module</span></span>

<span data-ttu-id="411f9-118">Päise moodulis saab kasutada järgmisi mooduleid.</span><span class="sxs-lookup"><span data-stu-id="411f9-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="411f9-119">**Navigeerimismenüü** – navigeerimismenüü tähistab kanali navigeerimishierarhiat ja teisi staatilisi navigeerimislinke.</span><span class="sxs-lookup"><span data-stu-id="411f9-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="411f9-120">Lisateavet vt teemast [Navigeerimismenüü moodul](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="411f9-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="411f9-121">**Otsing** – otsingu moodul võimaldab kasutajatel sisestada otsinguterminid toodete otsimiseks.</span><span class="sxs-lookup"><span data-stu-id="411f9-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="411f9-122">Vaikimisi otsingulehe URL ja otsingupäringu parameetrid peavad olema antud jaotises **Saidi sätted \> Laiendused**.</span><span class="sxs-lookup"><span data-stu-id="411f9-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="411f9-123">Otsingu moodulil on atribuudid, mis võimaldavad teil vajadusel otsingunupu peita või soovikohaselt sildistada.</span><span class="sxs-lookup"><span data-stu-id="411f9-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="411f9-124">Otsingumoodul toetab ka automaatse soovitamise valikuid, näiteks nagu toote, võtmesõna ja kategooria otsitulemused.</span><span class="sxs-lookup"><span data-stu-id="411f9-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="411f9-125">**Ostukorvi ikoon** – ostukorvi ikooni moodul tähistab ostukorvi ikooni, mis näitab ostukorvis olevate kaupade arvu igal ajahetkel.</span><span class="sxs-lookup"><span data-stu-id="411f9-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="411f9-126">Lisateavet vt teemast [Ostukorvi ikooni moodul](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="411f9-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="411f9-127">Lehele päise fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="411f9-127">Create a header fragment for a page</span></span>

<span data-ttu-id="411f9-128">Päise fragmendi loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="411f9-128">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="411f9-129">Avage **Fragmendid** ja valige uue fragmendi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="411f9-129">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="411f9-130">Valige dialoogiboksis **Uus fragment** moodul **Konteiner**, sisestage fragmendi nimi ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="411f9-130">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="411f9-131">Valige pesa **Vaikekonteiner** ja seejärel määrake parempoolsel atribuutide paanil atribuudi **Laius** väärtuseks **Täida ekraan**.</span><span class="sxs-lookup"><span data-stu-id="411f9-131">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="411f9-132">Valige pesas **Vaikekonteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="411f9-132">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="411f9-133">Valige dialoogiboksis **Lisa moodul** moodulid **Küpsistega nõustumine**, **Päis** ja **Reklaambänner** ning seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="411f9-133">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="411f9-134">Tehke mooduli **Reklaambänner** atribuutide paanil valikud **Lisa teade** ja **Teade**.</span><span class="sxs-lookup"><span data-stu-id="411f9-134">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="411f9-135">Lisage dialoogiaknas **Teade** reklaami tekst ja lingid ning klõpsake seejärel nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="411f9-135">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="411f9-136">Lisage ja konfigureerige mooduli **Küpsistega nõustumine** atribuutide paanil tekst ja link, mis suunab saidi privaatsuspoliitika lehele.</span><span class="sxs-lookup"><span data-stu-id="411f9-136">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="411f9-137">Valige päise mooduli pesas **Navigeerimismenüü** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="411f9-137">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="411f9-138">Valige dialoogiboksis **Lisa moodul** moodul **Navigeerimismenüü** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="411f9-138">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="411f9-139">Tehke navigeerimismenüü mooduli atribuudipaani jaotises **Navigeerimismenüü allikas** valik **Jaemüügiserver**.</span><span class="sxs-lookup"><span data-stu-id="411f9-139">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="411f9-140">Tehke navigeerimismenüü mooduli atribuudipaani jaotises **Staatilised menüü-üksused** valikud **Lisa menüü-üksus** ja **Menüü-üksus**.</span><span class="sxs-lookup"><span data-stu-id="411f9-140">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="411f9-141">Sisestage dialoogiboksi **Menüü-üksus** jaotisse **Menüü-üksuse tekst** tekst „Kontakt”.</span><span class="sxs-lookup"><span data-stu-id="411f9-141">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="411f9-142">Klõpsake dialoogiboksi **Menüü-üksus** jaotises **Menüü-üksuse lingi sihtkoht** käsku **Lisa link**.</span><span class="sxs-lookup"><span data-stu-id="411f9-142">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="411f9-143">Valige dialoogiaknas **Lisa link** saidi lehe „Kontakt” URL ning seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="411f9-143">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="411f9-144">Tehke dialoogiaknas **Menüü-üksus** valik **OK**.</span><span class="sxs-lookup"><span data-stu-id="411f9-144">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="411f9-145">Valige päise mooduli pesas **Otsing** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="411f9-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="411f9-146">Valige dialoogiboksis **Lisa moodul** moodul **Otsing** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="411f9-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="411f9-147">Konfigureerige otsingumooduli atribuutide paanil vajaduse järgi atribuudid.</span><span class="sxs-lookup"><span data-stu-id="411f9-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="411f9-148">Valige päise mooduli pesas **Ostukorvi ikoon** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="411f9-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="411f9-149">Valige dialoogiboksis **Lisa moodul** moodul **Ostukorvi ikoon** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="411f9-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="411f9-150">Konfigureerige ostukorvi ikooni mooduli atribuutide paanil vajaduse järgi atribuudid.</span><span class="sxs-lookup"><span data-stu-id="411f9-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="411f9-151">Kui soovite, et ostukorvi ikoon kuvaks ostukorvi kokkuvõtet (tuntud ka kui miniostukorv), kui kasutaja hiirt selle kohal hoiab, siis valige **Kuva miniostukorv**.</span><span class="sxs-lookup"><span data-stu-id="411f9-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="411f9-152">Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="411f9-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="411f9-153">Päise igal lehel kuvamise tagamiseks järgige neid samme iga malli jaoks, mis on saidi jaoks loodud.</span><span class="sxs-lookup"><span data-stu-id="411f9-153">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="411f9-154">Lisage mooduli **Vaikeleht** pesas **Päis** loodud jaluse fragment.</span><span class="sxs-lookup"><span data-stu-id="411f9-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="411f9-155">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="411f9-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="411f9-156">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="411f9-156">Additional resources</span></span>

[<span data-ttu-id="411f9-157">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="411f9-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="411f9-158">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="411f9-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="411f9-159">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="411f9-159">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="411f9-160">Kampaania ribareklaami moodul</span><span class="sxs-lookup"><span data-stu-id="411f9-160">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="411f9-161">Navigeerimismenüü moodul</span><span class="sxs-lookup"><span data-stu-id="411f9-161">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="411f9-162">Küpsistega nõustumine</span><span class="sxs-lookup"><span data-stu-id="411f9-162">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="411f9-163">Jalusemoodul</span><span class="sxs-lookup"><span data-stu-id="411f9-163">Footer module</span></span>](author-footer-module.md)
