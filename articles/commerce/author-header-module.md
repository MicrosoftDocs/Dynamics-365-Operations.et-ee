---
title: Päise moodul
description: See teema hõlmab päise mooduleid ja kirjeldab, kuidas lehe päiseid rakenduses Microsoft Dynamics 365 Commerce luua.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: efadd19681bbb21ea5b2b469e55bc6f4b0535046
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3025652"
---
# <a name="header-module"></a><span data-ttu-id="0538d-103">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="0538d-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0538d-104">See teema hõlmab päise mooduleid ja kirjeldab, kuidas lehe päiseid rakenduses Microsoft Dynamics 365 Commerce luua.</span><span class="sxs-lookup"><span data-stu-id="0538d-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0538d-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="0538d-105">Overview</span></span>

<span data-ttu-id="0538d-106">Dynamics 365 Commerce'i lehe päis koosneb mitmest moodulist, nagu päis, navigeerimismenüü, otsing, reklaambänner ja küpsistega nõustumise moodulid.</span><span class="sxs-lookup"><span data-stu-id="0538d-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="0538d-107">Päise moodul sisaldab saidi logo, linke navigeerimise hierarhiale, linke teistele saidi lehekülgedele, ostukorvi sümbolit, soovinimekirja sümbolit, sisselogimise suvandeid ja otsinguriba.</span><span class="sxs-lookup"><span data-stu-id="0538d-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="0538d-108">Päise moodul optimeeritakse automaatselt seadmele, millega saiti vaadatakse (teisisõnu töölauga seade või mobiilne seade).</span><span class="sxs-lookup"><span data-stu-id="0538d-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="0538d-109">Näiteks mobiilses seadmes on navigeerimisriba ahendatud nupule **Menüü** (mida nimetatakse mõnikord ka *hamburgerimenüüks*).</span><span class="sxs-lookup"><span data-stu-id="0538d-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="0538d-110">Päise mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="0538d-110">Properties of a header module</span></span>

<span data-ttu-id="0538d-111">Päise moodul toetab atribuute **Logo pilt**, **Logo link** ja **Minu konto lingid**.</span><span class="sxs-lookup"><span data-stu-id="0538d-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="0538d-112">Lehel logo määratlemiseks kasutatakse atribuute **Logo pilt** ja **Logo link**.</span><span class="sxs-lookup"><span data-stu-id="0538d-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="0538d-113">Lisateavet vt jaotisest [Logo lisamine](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="0538d-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="0538d-114">Atribuuti **Minu konto lingid** saab kasutada konto lehtede määratlemiseks, millele saidi omanik soovib päises kiirlinke kuvada.</span><span class="sxs-lookup"><span data-stu-id="0538d-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="0538d-115">Päise moodulis saadaolevad moodulid</span><span class="sxs-lookup"><span data-stu-id="0538d-115">Modules that are available in a header module</span></span>

<span data-ttu-id="0538d-116">Päise moodulis saab kasutada järgmisi mooduleid.</span><span class="sxs-lookup"><span data-stu-id="0538d-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="0538d-117">**Navigeerimismenüü** – navigeerimismenüü tähistab kanali navigeerimishierarhiat ja teisi staatilisi navigeerimislinke.</span><span class="sxs-lookup"><span data-stu-id="0538d-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="0538d-118">Kanali navigeerimishierarhiat saab konfigureerida rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0538d-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="0538d-119">Navigeerimise menüül on atribuut **Navigeerimise allikas**, mida kasutatakse jaemüügi serveri navigatsiooni menüü elementide ja staatilise menüü elementide määramiseks allikana.</span><span class="sxs-lookup"><span data-stu-id="0538d-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="0538d-120">Kui allikana on määratud staatilised menüü-elemendid, saab esitada seotud linke teistele saidi lehekülgedele.</span><span class="sxs-lookup"><span data-stu-id="0538d-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="0538d-121">Konfigureeritud üksused ilmuvad seejärel päise navigeerimises.</span><span class="sxs-lookup"><span data-stu-id="0538d-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="0538d-122">**Otsing** – otsingu moodul võimaldab kasutajatel sisestada otsinguterminid toodete otsimiseks.</span><span class="sxs-lookup"><span data-stu-id="0538d-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="0538d-123">Vaikimisi otsingulehe URL ja otsingupäringu parameetrid peavad olema antud jaotises **Saidi sätted \> Laiendused**.</span><span class="sxs-lookup"><span data-stu-id="0538d-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="0538d-124">Otsingu moodulil on atribuudid, mis võimaldavad teil vajadusel otsingunupu peita või soovikohaselt sildistada.</span><span class="sxs-lookup"><span data-stu-id="0538d-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="0538d-125">Otsingumoodul toetab ka automaatse soovitamise valikuid, näiteks nagu toote, võtmesõna ja kategooria otsitulemused.</span><span class="sxs-lookup"><span data-stu-id="0538d-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="0538d-126">Lehele päise mooduli loomine</span><span class="sxs-lookup"><span data-stu-id="0538d-126">Create a header module for a page</span></span>

<span data-ttu-id="0538d-127">Päise mooduli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="0538d-127">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="0538d-128">Looge fragment nimega **Päise fragment** ja lisage sellele konteineri moodul.</span><span class="sxs-lookup"><span data-stu-id="0538d-128">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="0538d-129">Seadistage konteineri mooduli paanil atribuut **Laius** väärtusele **Täida konteiner**.</span><span class="sxs-lookup"><span data-stu-id="0538d-129">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="0538d-130">Lisage konteineri moodulile reklaambänner ja küpsistega nõustumise moodulid.</span><span class="sxs-lookup"><span data-stu-id="0538d-130">Add promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="0538d-131">Lisage fragmendile veel üks konteineri moodul ja seadistage atribuudi **Laius** väärtuseks **Täida konteiner**.</span><span class="sxs-lookup"><span data-stu-id="0538d-131">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="0538d-132">Lisage teisele konteineri moodulile päise moodul.</span><span class="sxs-lookup"><span data-stu-id="0538d-132">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="0538d-133">Lisage päise mooduli pesasse **Navigeerimise menüü** navigeerimise menüü moodul.</span><span class="sxs-lookup"><span data-stu-id="0538d-133">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="0538d-134">Konfigureerige navigatsioonimenüü atribuudi paanil navigatsioonimenüü mooduli atribuudid.</span><span class="sxs-lookup"><span data-stu-id="0538d-134">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="0538d-135">Lisage päise mooduli pesasse **Otsing** otsingu moodul.</span><span class="sxs-lookup"><span data-stu-id="0538d-135">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="0538d-136">Konfigureerige otsingumooduli atribuudi paanil otsingumooduli atribuudid.</span><span class="sxs-lookup"><span data-stu-id="0538d-136">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="0538d-137">Salvestage lehe fragment, lõpetage selle redigeerimine ja seejärel avaldage see.</span><span class="sxs-lookup"><span data-stu-id="0538d-137">Save the page fragment, finish editing it, and publish it.</span></span> 

<span data-ttu-id="0538d-138">Päise igal lehel kuvamise tagamiseks järgige neid samme iga malli jaoks, mis on saidi jaoks loodud.</span><span class="sxs-lookup"><span data-stu-id="0538d-138">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="0538d-139">Lisage vaikelehe pesasse **Peamine** päise lehe fragment, mis sisaldab päise päise moodulit.</span><span class="sxs-lookup"><span data-stu-id="0538d-139">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="0538d-140">Salvestage mall, lõpetage selle redigeerimine ja seejärel avaldage see.</span><span class="sxs-lookup"><span data-stu-id="0538d-140">Save the template, finish editing it, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0538d-141">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0538d-141">Additional resources</span></span>

[<span data-ttu-id="0538d-142">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="0538d-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0538d-143">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="0538d-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="0538d-144">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="0538d-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="0538d-145">Ostukorvi moodul</span><span class="sxs-lookup"><span data-stu-id="0538d-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0538d-146">Maksmise moodul</span><span class="sxs-lookup"><span data-stu-id="0538d-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0538d-147">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="0538d-147">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="0538d-148">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="0538d-148">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="0538d-149">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="0538d-149">Footer module</span></span>](author-footer-module.md)
