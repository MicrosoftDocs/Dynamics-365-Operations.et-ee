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
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885474"
---
# <a name="header-module"></a><span data-ttu-id="897ee-103">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="897ee-103">Header module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="897ee-104">See teema hõlmab pease mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce luua.</span><span class="sxs-lookup"><span data-stu-id="897ee-104">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="897ee-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="897ee-105">Overview</span></span>

<span data-ttu-id="897ee-106">Päise moodul on erikonteiner, mida kasutatakse kõigi lehe päises kuvatavate moodulite majutamiseks.</span><span class="sxs-lookup"><span data-stu-id="897ee-106">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="897ee-107">Näiteks võib see sisaldada saidi logo, navigeerimishierarhia linke, linke saidi teistele lehtedele ja otsinguriba.</span><span class="sxs-lookup"><span data-stu-id="897ee-107">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="897ee-108">Päise moodul optimeeritakse automaatselt seadmele, millega saiti vaadatakse (s.o töölauga seade või mobiilne seade).</span><span class="sxs-lookup"><span data-stu-id="897ee-108">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="897ee-109">Näiteks mobiilses seadmes on navigeerimisriba ahendatud nupule **Menüü** (mida nimetatakse mõnikord ka *hamburgerimenüüks*).</span><span class="sxs-lookup"><span data-stu-id="897ee-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="897ee-110">Päise atribuudid</span><span class="sxs-lookup"><span data-stu-id="897ee-110">Properties of a header</span></span>

<span data-ttu-id="897ee-111">Sarnaselt üldistele konteineritele toetavad päise mooduleid **pealkirja** ja **laiuse** atribuute.</span><span class="sxs-lookup"><span data-stu-id="897ee-111">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="897ee-112">Päise moodulil on mitu pesa.</span><span class="sxs-lookup"><span data-stu-id="897ee-112">A header module has multiple slots.</span></span> <span data-ttu-id="897ee-113">Näiteks on olemas pesad teabesõnumi, navigeerimismenüü, logo, otsinguriba, ostukorvi ikooni, soovinimekirja ikooni ja kontoteabe jaoks.</span><span class="sxs-lookup"><span data-stu-id="897ee-113">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="897ee-114">Iga pesa toetab kindlat moodulite kogumit.</span><span class="sxs-lookup"><span data-stu-id="897ee-114">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="897ee-115">Päise moodulis saadaolevad moodulid</span><span class="sxs-lookup"><span data-stu-id="897ee-115">Modules that are available in a header module</span></span>

<span data-ttu-id="897ee-116">Päise moodulis saab kasutada järgmisi mooduleid.</span><span class="sxs-lookup"><span data-stu-id="897ee-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="897ee-117">**Navigeerimismenüü** – navigeerimismenüü tähistab kanali navigeerimishierarhiat ja teisi staatilisi navigeerimislinke.</span><span class="sxs-lookup"><span data-stu-id="897ee-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="897ee-118">Kanali navigeerimishierarhiat saab konfigureerida rakenduses Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="897ee-118">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="897ee-119">Konfigureeritud üksused ilmuvad seejärel päise navigeerimises.</span><span class="sxs-lookup"><span data-stu-id="897ee-119">Configured items then appear as header navigation.</span></span> <span data-ttu-id="897ee-120">Lisaks on võimalik konfigureerida staatilisi navigeerimislinke ja sisestada suhtelisi linke teistele e-kaubanduse saidi lehtedele.</span><span class="sxs-lookup"><span data-stu-id="897ee-120">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="897ee-121">Päist ennast saab joondada vasakule, paremale või keskele.</span><span class="sxs-lookup"><span data-stu-id="897ee-121">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="897ee-122">**Ostukorvi ikoon** – ostukorvi ikoon on spetsiaalne ikoon, mis tähistab ostukorvi.</span><span class="sxs-lookup"><span data-stu-id="897ee-122">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="897ee-123">See kuvatakse päises ja see näitab ostukorvis olevate kaupade arvu.</span><span class="sxs-lookup"><span data-stu-id="897ee-123">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="897ee-124">Ostukorvi ikooniga peab olema kaasas ostukorvi leht, et kliendid oleks võimalik ikooniga suheldes suunata ümber ostukorvi lehele.</span><span class="sxs-lookup"><span data-stu-id="897ee-124">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="897ee-125">**Soovinimekirja ikoon** – päises kuvatakse soovinimekirja ikoon ja see näitab kliendi soovinimekirja lisatud kaupade arvu.</span><span class="sxs-lookup"><span data-stu-id="897ee-125">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="897ee-126">Selle ikooniga peab olema kaasas soovinimekirja leht, et kliendid oleks võimalik ikooniga suheldes suunata ümber soovinimekirja lehele.</span><span class="sxs-lookup"><span data-stu-id="897ee-126">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="897ee-127">**Sisselogimismoodul** – sisselogimismoodul kuvatakse päises.</span><span class="sxs-lookup"><span data-stu-id="897ee-127">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="897ee-128">See võimaldab klientidel oma kontole sisse logida või registreerida konto.</span><span class="sxs-lookup"><span data-stu-id="897ee-128">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="897ee-129">Kui klient on juba sisse logitud, saab mooduli konfigureerida kuvama linke konto lehele, tellimuse ajaloo lehele või muule lehele.</span><span class="sxs-lookup"><span data-stu-id="897ee-129">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="897ee-130">**Logo moodul** – see moodul kuvab jaemüüjat ja kaubamärki esindava logo.</span><span class="sxs-lookup"><span data-stu-id="897ee-130">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="897ee-131">See on lingiga pilt.</span><span class="sxs-lookup"><span data-stu-id="897ee-131">It's an image that has a link.</span></span> <span data-ttu-id="897ee-132">Link on tavaliselt konfigureeritud nii, et sellel on ümbersuunamine kodulehele, seega saavad kliendid kiiresti naasta avalehele mis tahes lehelt.</span><span class="sxs-lookup"><span data-stu-id="897ee-132">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="897ee-133">**Teatis** – teatis kuvatakse päises ja seda kasutatakse tekstisisese teate kuvamiseks, mis rakendub kõigile saidi lehtedele.</span><span class="sxs-lookup"><span data-stu-id="897ee-133">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="897ee-134">Näiteks võib teatis kuvada sõnumi „Iga-aastane allahindlus lõpeb 2 päeva pärast”.</span><span class="sxs-lookup"><span data-stu-id="897ee-134">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="897ee-135">**Otsinguriba** – otsinguriba võimaldab kasutajatel sisestada otsinguterminid, et otsida tooteid.</span><span class="sxs-lookup"><span data-stu-id="897ee-135">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="897ee-136">Moodul peab olema konfigureeritud otsingutulemuste lehe URL-iga.</span><span class="sxs-lookup"><span data-stu-id="897ee-136">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="897ee-137">Päringustringi parameetrit saab konfigureerida (vaikeväärtus on **„q”**).</span><span class="sxs-lookup"><span data-stu-id="897ee-137">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="897ee-138">Otsinguribal on automaatse soovitamise pesa, kuhu tuleks lisada automaatse soovitamise moodul.</span><span class="sxs-lookup"><span data-stu-id="897ee-138">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="897ee-139">**Automaatne soovitamine** – automaatse soovitamise moodul kuvab automaatselt soovitatud tulemused.</span><span class="sxs-lookup"><span data-stu-id="897ee-139">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="897ee-140">Need tulemused võivad olla võtmesõnad, tooted või kategooriad, kus otsingusõna leitakse.</span><span class="sxs-lookup"><span data-stu-id="897ee-140">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="897ee-141">Päisemooduli loomine</span><span class="sxs-lookup"><span data-stu-id="897ee-141">Create a header module</span></span>

<span data-ttu-id="897ee-142">Päise mooduli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="897ee-142">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="897ee-143">Looge lehekülje fragment, mis sisaldab päise moodulit.</span><span class="sxs-lookup"><span data-stu-id="897ee-143">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="897ee-144">Lisage moodulid päise mooduli pesadesse.</span><span class="sxs-lookup"><span data-stu-id="897ee-144">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="897ee-145">Uuendage iga mooduli sätteid.</span><span class="sxs-lookup"><span data-stu-id="897ee-145">Update the settings for each module.</span></span>
1. <span data-ttu-id="897ee-146">Salvestage lehe fragment.</span><span class="sxs-lookup"><span data-stu-id="897ee-146">Save the page fragment.</span></span> 
1. <span data-ttu-id="897ee-147">Registreerige leht ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="897ee-147">Check in the page, and publish it.</span></span>

<span data-ttu-id="897ee-148">Päise igal lehel kuvamise tagamiseks järgige neid samme iga malli jaoks, mis on saidi jaoks loodud.</span><span class="sxs-lookup"><span data-stu-id="897ee-148">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="897ee-149">Lisage vaikelehel päise moodulit sisaldav lehe fragment peamise pesa päisele.</span><span class="sxs-lookup"><span data-stu-id="897ee-149">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="897ee-150">Salvestage mall</span><span class="sxs-lookup"><span data-stu-id="897ee-150">Save the template.</span></span> 
1. <span data-ttu-id="897ee-151">Registreerige mall ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="897ee-151">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="897ee-152">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="897ee-152">Additional resources</span></span>

[<span data-ttu-id="897ee-153">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="897ee-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="897ee-154">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="897ee-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="897ee-155">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="897ee-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="897ee-156">Ostukorvi moodul</span><span class="sxs-lookup"><span data-stu-id="897ee-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="897ee-157">Maksmise moodul</span><span class="sxs-lookup"><span data-stu-id="897ee-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="897ee-158">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="897ee-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="897ee-159">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="897ee-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="897ee-160">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="897ee-160">Footer module</span></span>](author-footer-module.md)
