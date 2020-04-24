---
title: Päise moodul
description: See teema hõlmab päise mooduleid ja kirjeldab, kuidas lehe päiseid rakenduses Microsoft Dynamics 365 Commerce luua.
author: anupamar
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261440"
---
# <a name="header-module"></a><span data-ttu-id="fd33d-103">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="fd33d-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fd33d-104">See teema hõlmab päise mooduleid ja kirjeldab, kuidas lehe päiseid rakenduses Microsoft Dynamics 365 Commerce luua.</span><span class="sxs-lookup"><span data-stu-id="fd33d-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fd33d-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="fd33d-105">Overview</span></span>

<span data-ttu-id="fd33d-106">Dynamics 365 Commerce'i lehe päis koosneb mitmest moodulist, nagu päis, navigeerimismenüü, otsing, reklaambänner ja küpsistega nõustumise moodulid.</span><span class="sxs-lookup"><span data-stu-id="fd33d-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="fd33d-107">Päise moodul sisaldab saidi logo, linke navigeerimise hierarhiale, linke teistele saidi lehekülgedele, ostukorvi sümbolit, soovinimekirja sümbolit, sisselogimise suvandeid ja otsinguriba.</span><span class="sxs-lookup"><span data-stu-id="fd33d-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="fd33d-108">Päise moodul optimeeritakse automaatselt seadmele, millega saiti vaadatakse (teisisõnu töölauga seade või mobiilne seade).</span><span class="sxs-lookup"><span data-stu-id="fd33d-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="fd33d-109">Näiteks mobiilses seadmes on navigeerimisriba ahendatud nupule **Menüü** (mida nimetatakse mõnikord ka *hamburgerimenüüks*).</span><span class="sxs-lookup"><span data-stu-id="fd33d-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="fd33d-110">Päise mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="fd33d-110">Properties of a header module</span></span>

<span data-ttu-id="fd33d-111">Päise moodul toetab atribuute **Logo pilt**, **Logo link** ja **Minu konto lingid**.</span><span class="sxs-lookup"><span data-stu-id="fd33d-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="fd33d-112">Lehel logo määratlemiseks kasutatakse atribuute **Logo pilt** ja **Logo link**.</span><span class="sxs-lookup"><span data-stu-id="fd33d-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="fd33d-113">Lisateavet vt jaotisest [Logo lisamine](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="fd33d-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="fd33d-114">Atribuuti **Minu konto lingid** saab kasutada konto lehtede määratlemiseks, millele saidi omanik soovib päises kiirlinke kuvada.</span><span class="sxs-lookup"><span data-stu-id="fd33d-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="fd33d-115">Päise moodulis saadaolevad moodulid</span><span class="sxs-lookup"><span data-stu-id="fd33d-115">Modules that are available in a header module</span></span>

<span data-ttu-id="fd33d-116">Päise moodulis saab kasutada järgmisi mooduleid.</span><span class="sxs-lookup"><span data-stu-id="fd33d-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="fd33d-117">**Navigeerimismenüü** – navigeerimismenüü tähistab kanali navigeerimishierarhiat ja teisi staatilisi navigeerimislinke.</span><span class="sxs-lookup"><span data-stu-id="fd33d-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="fd33d-118">Kanali navigeerimishierarhiat saab konfigureerida rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fd33d-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="fd33d-119">Navigeerimise menüül on atribuut **Navigeerimise allikas**, mida kasutatakse jaemüügi serveri navigatsiooni menüü elementide ja staatilise menüü elementide määramiseks allikana.</span><span class="sxs-lookup"><span data-stu-id="fd33d-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="fd33d-120">Kui allikana on määratud staatilised menüü-elemendid, saab esitada seotud linke teistele saidi lehekülgedele.</span><span class="sxs-lookup"><span data-stu-id="fd33d-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="fd33d-121">Konfigureeritud üksused ilmuvad seejärel päise navigeerimises.</span><span class="sxs-lookup"><span data-stu-id="fd33d-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="fd33d-122">**Otsing** – otsingu moodul võimaldab kasutajatel sisestada otsinguterminid toodete otsimiseks.</span><span class="sxs-lookup"><span data-stu-id="fd33d-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="fd33d-123">Vaikimisi otsingulehe URL ja otsingupäringu parameetrid peavad olema antud jaotises **Saidi sätted \> Laiendused**.</span><span class="sxs-lookup"><span data-stu-id="fd33d-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="fd33d-124">Otsingu moodulil on atribuudid, mis võimaldavad teil vajadusel otsingunupu peita või soovikohaselt sildistada.</span><span class="sxs-lookup"><span data-stu-id="fd33d-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="fd33d-125">Otsingumoodul toetab ka automaatse soovitamise valikuid, näiteks nagu toote, võtmesõna ja kategooria otsitulemused.</span><span class="sxs-lookup"><span data-stu-id="fd33d-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>
- <span data-ttu-id="fd33d-126">**Ostukorvi ikoon** – ostukorvi ikooni moodul tähistab ostukorvi ikooni, mis näitab ostukorvis olevate kaupade arvu igal ajahetkel.</span><span class="sxs-lookup"><span data-stu-id="fd33d-126">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="fd33d-127">Lisateavet vt teemast [Ostukorvi ikooni moodul](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="fd33d-127">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="fd33d-128">Lehele päise mooduli loomine</span><span class="sxs-lookup"><span data-stu-id="fd33d-128">Create a header module for a page</span></span>

<span data-ttu-id="fd33d-129">Päise mooduli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="fd33d-129">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="fd33d-130">Looge fragment nimega **Päise fragment** ja lisage sellele konteineri moodul.</span><span class="sxs-lookup"><span data-stu-id="fd33d-130">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="fd33d-131">Seadistage konteineri mooduli paanil atribuut **Laius** väärtusele **Täida konteiner**.</span><span class="sxs-lookup"><span data-stu-id="fd33d-131">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="fd33d-132">Lisage konteineri moodulile reklaambänner ja küpsistega nõustumise moodulid.</span><span class="sxs-lookup"><span data-stu-id="fd33d-132">Add a promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="fd33d-133">Lisage fragmendile veel üks konteineri moodul ja seadistage atribuudi **Laius** väärtuseks **Täida konteiner**.</span><span class="sxs-lookup"><span data-stu-id="fd33d-133">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="fd33d-134">Lisage teisele konteineri moodulile päise moodul.</span><span class="sxs-lookup"><span data-stu-id="fd33d-134">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="fd33d-135">Lisage päise mooduli pesasse **Navigeerimise menüü** navigeerimise menüü moodul.</span><span class="sxs-lookup"><span data-stu-id="fd33d-135">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="fd33d-136">Konfigureerige navigatsioonimenüü atribuudi paanil navigatsioonimenüü mooduli atribuudid.</span><span class="sxs-lookup"><span data-stu-id="fd33d-136">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="fd33d-137">Lisage päise mooduli pesasse **Otsing** otsingu moodul.</span><span class="sxs-lookup"><span data-stu-id="fd33d-137">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="fd33d-138">Konfigureerige otsingumooduli atribuudi paanil otsingumooduli atribuudid.</span><span class="sxs-lookup"><span data-stu-id="fd33d-138">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="fd33d-139">Lisage ostukorvi ikooni moodul päisemooduli pesasse **Ostukorvi ikoon**.</span><span class="sxs-lookup"><span data-stu-id="fd33d-139">In the **Cart icon** slot of the header module, add a cart icon module.</span></span> 
1. <span data-ttu-id="fd33d-140">Konfigureerige ostukorvi ikooni mooduli atribuudi paanil ostukorvi ikooni mooduli atribuudid.</span><span class="sxs-lookup"><span data-stu-id="fd33d-140">In the property pane for the cart icon module, configure the properties of the cart icon module.</span></span> <span data-ttu-id="fd33d-141">Kui soovite, et ostukorvi ikoonil hõljutamisel kuvatakse väike ostukorv, valige sätte **Kuva väike ostukorv** jaoks väärtus **Tõene**.</span><span class="sxs-lookup"><span data-stu-id="fd33d-141">If you want the cart icon to display a mini cart when hovered over, select **True** for **Show mini cart**.</span></span>
1. <span data-ttu-id="fd33d-142">Salvestage lehe fragment, lõpetage selle redigeerimine ja seejärel avaldage see.</span><span class="sxs-lookup"><span data-stu-id="fd33d-142">Save the page fragment, finish editing, and publish it.</span></span> 


<span data-ttu-id="fd33d-143">Päise igal lehel kuvamise tagamiseks järgige neid samme iga malli jaoks, mis on saidi jaoks loodud.</span><span class="sxs-lookup"><span data-stu-id="fd33d-143">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="fd33d-144">Lisage vaikelehe pesasse **Peamine** päise lehe fragment, mis sisaldab päise päise moodulit.</span><span class="sxs-lookup"><span data-stu-id="fd33d-144">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="fd33d-145">Salvestage mall, lõpetage selle redigeerimine ja seejärel avaldage see.</span><span class="sxs-lookup"><span data-stu-id="fd33d-145">Save the template, finish editing, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd33d-146">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="fd33d-146">Additional resources</span></span>

[<span data-ttu-id="fd33d-147">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="fd33d-147">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fd33d-148">Konteineri moodul</span><span class="sxs-lookup"><span data-stu-id="fd33d-148">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="fd33d-149">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="fd33d-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="fd33d-150">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="fd33d-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fd33d-151">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="fd33d-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="fd33d-152">Väljaregistreerimismoodul</span><span class="sxs-lookup"><span data-stu-id="fd33d-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fd33d-153">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="fd33d-153">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="fd33d-154">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="fd33d-154">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="fd33d-155">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="fd33d-155">Footer module</span></span>](author-footer-module.md)
