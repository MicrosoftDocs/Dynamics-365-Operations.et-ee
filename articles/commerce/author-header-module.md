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
ms.openlocfilehash: a5f7ad7d9c5ff63c3c3a8fe38275eec0d138891d
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411198"
---
# <a name="header-module"></a><span data-ttu-id="e9d91-103">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="e9d91-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e9d91-104">See teema hõlmab päise mooduleid ja kirjeldab, kuidas lehe päiseid rakenduses Microsoft Dynamics 365 Commerce luua.</span><span class="sxs-lookup"><span data-stu-id="e9d91-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e9d91-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="e9d91-105">Overview</span></span>

<span data-ttu-id="e9d91-106">Dynamics 365 Commerce'i lehe päis koosneb mitmest moodulist, nagu päis, navigeerimismenüü, otsing, reklaambänner ja küpsistega nõustumise moodulid.</span><span class="sxs-lookup"><span data-stu-id="e9d91-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="e9d91-107">Päise moodul sisaldab saidi logo, linke navigeerimise hierarhiale, linke teistele saidi lehekülgedele, ostukorvi sümbolit, soovinimekirja sümbolit, sisselogimise suvandeid ja otsinguriba.</span><span class="sxs-lookup"><span data-stu-id="e9d91-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="e9d91-108">Päise moodul optimeeritakse automaatselt seadmele, millega saiti vaadatakse (teisisõnu töölauga seade või mobiilne seade).</span><span class="sxs-lookup"><span data-stu-id="e9d91-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="e9d91-109">Näiteks mobiilses seadmes on navigeerimisriba ahendatud nupule **Menüü** (mida nimetatakse mõnikord ka *hamburgerimenüüks*).</span><span class="sxs-lookup"><span data-stu-id="e9d91-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="e9d91-110">Järgmisel pildil on näide päise moodulist avalehel.</span><span class="sxs-lookup"><span data-stu-id="e9d91-110">The following image shows an example of a header module on a home page.</span></span>

![Päise mooduli näide](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="e9d91-112">Päise mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="e9d91-112">Properties of a header module</span></span>

<span data-ttu-id="e9d91-113">Päise moodul toetab atribuute **Logo pilt**, **Logo link** ja **Minu konto lingid**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="e9d91-114">Lehel logo määratlemiseks kasutatakse atribuute **Logo pilt** ja **Logo link**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="e9d91-115">Lisateavet vt jaotisest [Logo lisamine](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="e9d91-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="e9d91-116">Atribuuti **Minu konto lingid** saab kasutada konto lehtede määratlemiseks, millele saidi omanik soovib päises kiirlinke kuvada.</span><span class="sxs-lookup"><span data-stu-id="e9d91-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="e9d91-117">Päise moodulis saadaolevad moodulid</span><span class="sxs-lookup"><span data-stu-id="e9d91-117">Modules that are available in a header module</span></span>

<span data-ttu-id="e9d91-118">Päise moodulis saab kasutada järgmisi mooduleid.</span><span class="sxs-lookup"><span data-stu-id="e9d91-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="e9d91-119">**Navigeerimismenüü** – navigeerimismenüü tähistab kanali navigeerimishierarhiat ja teisi staatilisi navigeerimislinke.</span><span class="sxs-lookup"><span data-stu-id="e9d91-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="e9d91-120">Kanali navigeerimishierarhiat saab konfigureerida rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e9d91-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="e9d91-121">Navigeerimise menüül on atribuut **Navigeerimise allikas**, mida kasutatakse jaemüügi serveri navigatsiooni menüü elementide ja staatilise menüü elementide määramiseks allikana.</span><span class="sxs-lookup"><span data-stu-id="e9d91-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="e9d91-122">Kui allikana on määratud staatilised menüü-elemendid, saab esitada seotud linke teistele saidi lehekülgedele.</span><span class="sxs-lookup"><span data-stu-id="e9d91-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="e9d91-123">Konfigureeritud üksused ilmuvad seejärel päise navigeerimises.</span><span class="sxs-lookup"><span data-stu-id="e9d91-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="e9d91-124">**Otsing** – otsingu moodul võimaldab kasutajatel sisestada otsinguterminid toodete otsimiseks.</span><span class="sxs-lookup"><span data-stu-id="e9d91-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="e9d91-125">Vaikimisi otsingulehe URL ja otsingupäringu parameetrid peavad olema antud jaotises **Saidi sätted \> Laiendused**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="e9d91-126">Otsingu moodulil on atribuudid, mis võimaldavad teil vajadusel otsingunupu peita või soovikohaselt sildistada.</span><span class="sxs-lookup"><span data-stu-id="e9d91-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="e9d91-127">Otsingumoodul toetab ka automaatse soovitamise valikuid, näiteks nagu toote, võtmesõna ja kategooria otsitulemused.</span><span class="sxs-lookup"><span data-stu-id="e9d91-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="e9d91-128">**Ostukorvi ikoon** – ostukorvi ikooni moodul tähistab ostukorvi ikooni, mis näitab ostukorvis olevate kaupade arvu igal ajahetkel.</span><span class="sxs-lookup"><span data-stu-id="e9d91-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="e9d91-129">Lisateavet vt teemast [Ostukorvi ikooni moodul](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="e9d91-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="e9d91-130">Lehele päise mooduli loomine</span><span class="sxs-lookup"><span data-stu-id="e9d91-130">Create a header module for a page</span></span>

<span data-ttu-id="e9d91-131">Päise mooduli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e9d91-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="e9d91-132">Avage **Lehe fragmendid** ja valige uue fragmendi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-132">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="e9d91-133">Dialoogiboksis **Uus lehe fragment** valige moodul **Konteiner**, sisestage lehe fragmendi nimi ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-133">In the **New Page Fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="e9d91-134">Valige pesa **Vaikekonteiner** ja seejärel määrake parempoolsel atribuutide paanil atribuudi **Laius** väärtuseks **Täida konteiner**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="e9d91-135">Valige pesas **Vaikekonteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e9d91-136">Valige dialoogiboksis **Lisa moodul** moodulid **Reklaambänner** ja **Küpsistega nõustumine** ning seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="e9d91-137">Valige pesas **Vaikekonteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e9d91-138">Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e9d91-139">Valige pesa **Konteiner** ja seejärel määrake parempoolsel atribuutide paanil atribuudi **Laius** väärtuseks **Täida konteiner**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="e9d91-140">Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e9d91-141">Valige dialoogiboksis **Lisa moodul** moodul **Päis** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e9d91-142">Valige päise mooduli pesas **Navigeerimismenüü** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e9d91-143">Valige dialoogiboksis **Lisa moodul** moodul **Navigeerimismenüü** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e9d91-144">Konfigureerige navigeerimismenüü atribuutide paanil vajaduse järgi atribuudid.</span><span class="sxs-lookup"><span data-stu-id="e9d91-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="e9d91-145">Valige päise mooduli pesas **Otsing** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e9d91-146">Valige dialoogiboksis **Lisa moodul** moodul **Otsing** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e9d91-147">Konfigureerige otsingumooduli atribuutide paanil vajaduse järgi atribuudid.</span><span class="sxs-lookup"><span data-stu-id="e9d91-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="e9d91-148">Valige päise mooduli pesas **Ostukorvi ikoon** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e9d91-149">Valige dialoogiboksis **Lisa moodul** moodul **Ostukorvi ikoon** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e9d91-150">Konfigureerige ostukorvi ikooni mooduli atribuutide paanil vajaduse järgi atribuudid.</span><span class="sxs-lookup"><span data-stu-id="e9d91-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="e9d91-151">Kui soovite, et ostukorvi ikoon kuvaks ostukorvi kokkuvõtet (tuntud ka kui miniostukorv), kui kasutaja hiirt selle kohal hoiab, siis valige **Kuva miniostukorv**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="e9d91-152">Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="e9d91-153">Päise igal lehel kuvamise tagamiseks järgige neid samme iga malli jaoks, mis on saidi jaoks loodud.</span><span class="sxs-lookup"><span data-stu-id="e9d91-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="e9d91-154">Lisage mooduli **Vaikeleht** pesas **Päis** loodud jaluse fragment.</span><span class="sxs-lookup"><span data-stu-id="e9d91-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="e9d91-155">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="e9d91-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e9d91-156">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e9d91-156">Additional resources</span></span>

[<span data-ttu-id="e9d91-157">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="e9d91-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e9d91-158">Konteineri moodul</span><span class="sxs-lookup"><span data-stu-id="e9d91-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="e9d91-159">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="e9d91-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e9d91-160">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="e9d91-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e9d91-161">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="e9d91-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="e9d91-162">Väljaregistreerimismoodul</span><span class="sxs-lookup"><span data-stu-id="e9d91-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e9d91-163">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="e9d91-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="e9d91-164">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="e9d91-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="e9d91-165">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="e9d91-165">Footer module</span></span>](author-footer-module.md)
