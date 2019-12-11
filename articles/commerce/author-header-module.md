---
title: Päise moodul
description: See teema hõlmab pease mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce luua.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697271"
---
# <a name="header-module"></a><span data-ttu-id="df8b9-103">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="df8b9-103">Header module</span></span>

<span data-ttu-id="df8b9-104">[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span><span class="sxs-lookup"><span data-stu-id="df8b9-104">[!include [banner]includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span></span>

<span data-ttu-id="df8b9-105">See teema hõlmab pease mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce luua.</span><span class="sxs-lookup"><span data-stu-id="df8b9-105">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="df8b9-106">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="df8b9-106">Overview</span></span>

<span data-ttu-id="df8b9-107">Päise moodul on erikonteiner, mida kasutatakse kõigi lehe päises kuvatavate moodulite majutamiseks.</span><span class="sxs-lookup"><span data-stu-id="df8b9-107">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="df8b9-108">Näiteks võib see sisaldada saidi logo, navigeerimishierarhia linke, linke saidi teistele lehtedele ja otsinguriba.</span><span class="sxs-lookup"><span data-stu-id="df8b9-108">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="df8b9-109">Päise moodul optimeeritakse automaatselt seadmele, millega saiti vaadatakse (s.o töölauga seade või mobiilne seade).</span><span class="sxs-lookup"><span data-stu-id="df8b9-109">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="df8b9-110">Näiteks mobiilses seadmes on navigeerimisriba ahendatud nupule **Menüü** (mida nimetatakse mõnikord ka *hamburgerimenüüks*).</span><span class="sxs-lookup"><span data-stu-id="df8b9-110">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="df8b9-111">Päise atribuudid</span><span class="sxs-lookup"><span data-stu-id="df8b9-111">Properties of a header</span></span>

<span data-ttu-id="df8b9-112">Sarnaselt üldistele konteineritele toetavad päise mooduleid **pealkirja** ja **laiuse** atribuute.</span><span class="sxs-lookup"><span data-stu-id="df8b9-112">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="df8b9-113">Päise moodulil on mitu pesa.</span><span class="sxs-lookup"><span data-stu-id="df8b9-113">A header module has multiple slots.</span></span> <span data-ttu-id="df8b9-114">Näiteks on olemas pesad teabesõnumi, navigeerimismenüü, logo, otsinguriba, ostukorvi ikooni, soovinimekirja ikooni ja kontoteabe jaoks.</span><span class="sxs-lookup"><span data-stu-id="df8b9-114">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="df8b9-115">Iga pesa toetab kindlat moodulite kogumit.</span><span class="sxs-lookup"><span data-stu-id="df8b9-115">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="df8b9-116">Päise moodulis saadaolevad moodulid</span><span class="sxs-lookup"><span data-stu-id="df8b9-116">Modules that are available in a header module</span></span>

<span data-ttu-id="df8b9-117">Päise moodulis saab kasutada järgmisi mooduleid.</span><span class="sxs-lookup"><span data-stu-id="df8b9-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="df8b9-118">**Navigeerimismenüü** – navigeerimismenüü tähistab kanali navigeerimishierarhiat ja teisi staatilisi navigeerimislinke.</span><span class="sxs-lookup"><span data-stu-id="df8b9-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="df8b9-119">Kanali navigeerimishierarhiat saab konfigureerida rakenduses Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="df8b9-119">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="df8b9-120">Konfigureeritud üksused ilmuvad seejärel päise navigeerimises.</span><span class="sxs-lookup"><span data-stu-id="df8b9-120">Configured items then appear as header navigation.</span></span> <span data-ttu-id="df8b9-121">Lisaks on võimalik konfigureerida staatilisi navigeerimislinke ja sisestada suhtelisi linke teistele e-kaubanduse saidi lehtedele.</span><span class="sxs-lookup"><span data-stu-id="df8b9-121">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="df8b9-122">Päist ennast saab joondada vasakule, paremale või keskele.</span><span class="sxs-lookup"><span data-stu-id="df8b9-122">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="df8b9-123">**Ostukorvi ikoon** – ostukorvi ikoon on spetsiaalne ikoon, mis tähistab ostukorvi.</span><span class="sxs-lookup"><span data-stu-id="df8b9-123">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="df8b9-124">See kuvatakse päises ja see näitab ostukorvis olevate kaupade arvu.</span><span class="sxs-lookup"><span data-stu-id="df8b9-124">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="df8b9-125">Ostukorvi ikooniga peab olema kaasas ostukorvi leht, et kliendid oleks võimalik ikooniga suheldes suunata ümber ostukorvi lehele.</span><span class="sxs-lookup"><span data-stu-id="df8b9-125">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="df8b9-126">**Soovinimekirja ikoon** – päises kuvatakse soovinimekirja ikoon ja see näitab kliendi soovinimekirja lisatud kaupade arvu.</span><span class="sxs-lookup"><span data-stu-id="df8b9-126">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="df8b9-127">Selle ikooniga peab olema kaasas soovinimekirja leht, et kliendid oleks võimalik ikooniga suheldes suunata ümber soovinimekirja lehele.</span><span class="sxs-lookup"><span data-stu-id="df8b9-127">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="df8b9-128">**Sisselogimismoodul** – sisselogimismoodul kuvatakse päises.</span><span class="sxs-lookup"><span data-stu-id="df8b9-128">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="df8b9-129">See võimaldab klientidel oma kontole sisse logida või registreerida konto.</span><span class="sxs-lookup"><span data-stu-id="df8b9-129">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="df8b9-130">Kui klient on juba sisse logitud, saab mooduli konfigureerida kuvama linke konto lehele, tellimuse ajaloo lehele või muule lehele.</span><span class="sxs-lookup"><span data-stu-id="df8b9-130">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="df8b9-131">**Logo moodul** – see moodul kuvab jaemüüjat ja kaubamärki esindava logo.</span><span class="sxs-lookup"><span data-stu-id="df8b9-131">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="df8b9-132">See on lingiga pilt.</span><span class="sxs-lookup"><span data-stu-id="df8b9-132">It's an image that has a link.</span></span> <span data-ttu-id="df8b9-133">Link on tavaliselt konfigureeritud nii, et sellel on ümbersuunamine kodulehele, seega saavad kliendid kiiresti naasta avalehele mis tahes lehelt.</span><span class="sxs-lookup"><span data-stu-id="df8b9-133">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="df8b9-134">**Teatis** – teatis kuvatakse päises ja seda kasutatakse tekstisisese teate kuvamiseks, mis rakendub kõigile saidi lehtedele.</span><span class="sxs-lookup"><span data-stu-id="df8b9-134">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="df8b9-135">Näiteks võib teatis kuvada sõnumi „Iga-aastane allahindlus lõpeb 2 päeva pärast”.</span><span class="sxs-lookup"><span data-stu-id="df8b9-135">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="df8b9-136">**Otsinguriba** – otsinguriba võimaldab kasutajatel sisestada otsinguterminid, et otsida tooteid.</span><span class="sxs-lookup"><span data-stu-id="df8b9-136">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="df8b9-137">Moodul peab olema konfigureeritud otsingutulemuste lehe URL-iga.</span><span class="sxs-lookup"><span data-stu-id="df8b9-137">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="df8b9-138">Päringustringi parameetrit saab konfigureerida (vaikeväärtus on **„q”**).</span><span class="sxs-lookup"><span data-stu-id="df8b9-138">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="df8b9-139">Otsinguribal on automaatse soovitamise pesa, kuhu tuleks lisada automaatse soovitamise moodul.</span><span class="sxs-lookup"><span data-stu-id="df8b9-139">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="df8b9-140">**Automaatne soovitamine** – automaatse soovitamise moodul kuvab automaatselt soovitatud tulemused.</span><span class="sxs-lookup"><span data-stu-id="df8b9-140">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="df8b9-141">Need tulemused võivad olla võtmesõnad, tooted või kategooriad, kus otsingusõna leitakse.</span><span class="sxs-lookup"><span data-stu-id="df8b9-141">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="df8b9-142">Päisemooduli loomine</span><span class="sxs-lookup"><span data-stu-id="df8b9-142">Create a header module</span></span>

<span data-ttu-id="df8b9-143">Päise mooduli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="df8b9-143">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="df8b9-144">Looge lehekülje fragment, mis sisaldab päise moodulit.</span><span class="sxs-lookup"><span data-stu-id="df8b9-144">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="df8b9-145">Lisage moodulid päise mooduli pesadesse.</span><span class="sxs-lookup"><span data-stu-id="df8b9-145">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="df8b9-146">Uuendage iga mooduli sätteid.</span><span class="sxs-lookup"><span data-stu-id="df8b9-146">Update the settings for each module.</span></span>
1. <span data-ttu-id="df8b9-147">Salvestage lehe fragment.</span><span class="sxs-lookup"><span data-stu-id="df8b9-147">Save the page fragment.</span></span> 
1. <span data-ttu-id="df8b9-148">Registreerige leht ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="df8b9-148">Check in the page, and publish it.</span></span>

<span data-ttu-id="df8b9-149">Päise igal lehel kuvamise tagamiseks järgige neid samme iga malli jaoks, mis on saidi jaoks loodud.</span><span class="sxs-lookup"><span data-stu-id="df8b9-149">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="df8b9-150">Lisage vaikelehel päise moodulit sisaldav lehe fragment peamise pesa päisele.</span><span class="sxs-lookup"><span data-stu-id="df8b9-150">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="df8b9-151">Salvestage mall</span><span class="sxs-lookup"><span data-stu-id="df8b9-151">Save the template.</span></span> 
1. <span data-ttu-id="df8b9-152">Registreerige mall ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="df8b9-152">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df8b9-153">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="df8b9-153">Additional resources</span></span>

[<span data-ttu-id="df8b9-154">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="df8b9-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="df8b9-155">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="df8b9-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="df8b9-156">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="df8b9-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="df8b9-157">Ostukorvi moodul</span><span class="sxs-lookup"><span data-stu-id="df8b9-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="df8b9-158">Maksmise moodul</span><span class="sxs-lookup"><span data-stu-id="df8b9-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="df8b9-159">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="df8b9-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="df8b9-160">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="df8b9-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="df8b9-161">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="df8b9-161">Footer module</span></span>](author-footer-module.md)
