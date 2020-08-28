---
title: Päise moodul
description: See teema hõlmab päise mooduleid ja kirjeldab, kuidas lehe päiseid rakenduses Microsoft Dynamics 365 Commerce luua.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: e7dde3ba1ad375b309ae66cc6d31ccad85615e45
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686618"
---
# <a name="header-module"></a><span data-ttu-id="0f4ef-103">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="0f4ef-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0f4ef-104">See teema hõlmab päise mooduleid ja kirjeldab, kuidas lehe päiseid rakenduses Microsoft Dynamics 365 Commerce luua.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0f4ef-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="0f4ef-105">Overview</span></span>

<span data-ttu-id="0f4ef-106">Dynamics 365 Commerce'i lehe päis koosneb mitmest moodulist, nagu päis, navigeerimismenüü, otsing, reklaambänner ja küpsistega nõustumise moodulid.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="0f4ef-107">Päise moodul sisaldab saidi logo, linke navigeerimise hierarhiale, linke teistele saidi lehekülgedele, ostukorvi sümbolit, soovinimekirja sümbolit, sisselogimise suvandeid ja otsinguriba.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="0f4ef-108">Päise moodul optimeeritakse automaatselt seadmele, millega saiti vaadatakse (teisisõnu töölauga seade või mobiilne seade).</span><span class="sxs-lookup"><span data-stu-id="0f4ef-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="0f4ef-109">Näiteks mobiilses seadmes on navigeerimisriba ahendatud nupule **Menüü** (mida nimetatakse mõnikord ka *hamburgerimenüüks*).</span><span class="sxs-lookup"><span data-stu-id="0f4ef-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="0f4ef-110">Järgmisel pildil on näide päise moodulist avalehel.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-110">The following image shows an example of a header module on a home page.</span></span>

![Päise mooduli näide](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="0f4ef-112">Päise mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="0f4ef-112">Properties of a header module</span></span>

<span data-ttu-id="0f4ef-113">Päise moodul toetab atribuute **Logo pilt**, **Logo link** ja **Minu konto lingid**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="0f4ef-114">Lehel logo määratlemiseks kasutatakse atribuute **Logo pilt** ja **Logo link**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="0f4ef-115">Lisateavet vt jaotisest [Logo lisamine](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="0f4ef-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="0f4ef-116">Atribuuti **Minu konto lingid** saab kasutada konto lehtede määratlemiseks, millele saidi omanik soovib päises kiirlinke kuvada.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="0f4ef-117">Päise moodulis saadaolevad moodulid</span><span class="sxs-lookup"><span data-stu-id="0f4ef-117">Modules that are available in a header module</span></span>

<span data-ttu-id="0f4ef-118">Päise moodulis saab kasutada järgmisi mooduleid.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="0f4ef-119">**Navigeerimismenüü** – navigeerimismenüü tähistab kanali navigeerimishierarhiat ja teisi staatilisi navigeerimislinke.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="0f4ef-120">Kanali navigeerimishierarhiat saab konfigureerida rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="0f4ef-121">Navigeerimise menüül on atribuut **Navigeerimise allikas**, mida kasutatakse jaemüügi serveri navigatsiooni menüü elementide ja staatilise menüü elementide määramiseks allikana.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="0f4ef-122">Kui allikana on määratud staatilised menüü-elemendid, saab esitada seotud linke teistele saidi lehekülgedele.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="0f4ef-123">Konfigureeritud üksused ilmuvad seejärel päise navigeerimises.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="0f4ef-124">**Otsing** – otsingu moodul võimaldab kasutajatel sisestada otsinguterminid toodete otsimiseks.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="0f4ef-125">Vaikimisi otsingulehe URL ja otsingupäringu parameetrid peavad olema antud jaotises **Saidi sätted \> Laiendused**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="0f4ef-126">Otsingu moodulil on atribuudid, mis võimaldavad teil vajadusel otsingunupu peita või soovikohaselt sildistada.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="0f4ef-127">Otsingumoodul toetab ka automaatse soovitamise valikuid, näiteks nagu toote, võtmesõna ja kategooria otsitulemused.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="0f4ef-128">**Ostukorvi ikoon** – ostukorvi ikooni moodul tähistab ostukorvi ikooni, mis näitab ostukorvis olevate kaupade arvu igal ajahetkel.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="0f4ef-129">Lisateavet vt teemast [Ostukorvi ikooni moodul](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="0f4ef-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="0f4ef-130">Lehele päise mooduli loomine</span><span class="sxs-lookup"><span data-stu-id="0f4ef-130">Create a header module for a page</span></span>

<span data-ttu-id="0f4ef-131">Päise mooduli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="0f4ef-132">Avage **Fragmendid** ja valige uue fragmendi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-132">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="0f4ef-133">Valige dialoogiboksis **Uus lehe fragment** moodul **Konteiner**, sisestage lehe fragmendi nimi ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-133">In the **New page fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="0f4ef-134">Valige pesa **Vaikekonteiner** ja seejärel määrake parempoolsel atribuutide paanil atribuudi **Laius** väärtuseks **Täida konteiner**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="0f4ef-135">Valige pesas **Vaikekonteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0f4ef-136">Valige dialoogiboksis **Lisa moodul** moodulid **Reklaambänner** ja **Küpsistega nõustumine** ning seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="0f4ef-137">Valige pesas **Vaikekonteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0f4ef-138">Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0f4ef-139">Valige pesa **Konteiner** ja seejärel määrake parempoolsel atribuutide paanil atribuudi **Laius** väärtuseks **Täida konteiner**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="0f4ef-140">Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0f4ef-141">Valige dialoogiboksis **Lisa moodul** moodul **Päis** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0f4ef-142">Valige päise mooduli pesas **Navigeerimismenüü** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0f4ef-143">Valige dialoogiboksis **Lisa moodul** moodul **Navigeerimismenüü** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0f4ef-144">Konfigureerige navigeerimismenüü atribuutide paanil vajaduse järgi atribuudid.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="0f4ef-145">Valige päise mooduli pesas **Otsing** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0f4ef-146">Valige dialoogiboksis **Lisa moodul** moodul **Otsing** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0f4ef-147">Konfigureerige otsingumooduli atribuutide paanil vajaduse järgi atribuudid.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="0f4ef-148">Valige päise mooduli pesas **Ostukorvi ikoon** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0f4ef-149">Valige dialoogiboksis **Lisa moodul** moodul **Ostukorvi ikoon** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0f4ef-150">Konfigureerige ostukorvi ikooni mooduli atribuutide paanil vajaduse järgi atribuudid.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="0f4ef-151">Kui soovite, et ostukorvi ikoon kuvaks ostukorvi kokkuvõtet (tuntud ka kui miniostukorv), kui kasutaja hiirt selle kohal hoiab, siis valige **Kuva miniostukorv**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="0f4ef-152">Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="0f4ef-153">Päise igal lehel kuvamise tagamiseks järgige neid samme iga malli jaoks, mis on saidi jaoks loodud.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="0f4ef-154">Lisage mooduli **Vaikeleht** pesas **Päis** loodud jaluse fragment.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="0f4ef-155">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="0f4ef-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f4ef-156">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0f4ef-156">Additional resources</span></span>

[<span data-ttu-id="0f4ef-157">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="0f4ef-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0f4ef-158">Konteineri moodul</span><span class="sxs-lookup"><span data-stu-id="0f4ef-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="0f4ef-159">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="0f4ef-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="0f4ef-160">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="0f4ef-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0f4ef-161">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="0f4ef-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="0f4ef-162">Väljaregistreerimismoodul</span><span class="sxs-lookup"><span data-stu-id="0f4ef-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0f4ef-163">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="0f4ef-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="0f4ef-164">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="0f4ef-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="0f4ef-165">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="0f4ef-165">Footer module</span></span>](author-footer-module.md)
