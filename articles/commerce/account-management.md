---
title: Kontohalduse lehed ja moodulid
description: See teema käsitleb kontohalduse lehti ja mooduleid rakenduses Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c465b8883438eee886b177274bf89ddb86aa00b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980552"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="24b25-103">Kontohalduse lehed ja moodulid</span><span class="sxs-lookup"><span data-stu-id="24b25-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="24b25-104">See teema käsitleb kontohalduse lehti ja mooduleid rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="24b25-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="24b25-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="24b25-105">Overview</span></span>

<span data-ttu-id="24b25-106">Kontohaldus viitab lehtede grupile, mida kasutatakse kasutajakontoga seotud teabe haldamiseks rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="24b25-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="24b25-107">Kontohalduse lehed hõlmavad kontohalduse sihtlehte, kasutajaprofiili lehte, kasutaja aadressi lehte, tellimuste ajaloo lehte, tellimuste üksikasjade lehte, püsikliendi lehte ja soovinimekirja lehte.</span><span class="sxs-lookup"><span data-stu-id="24b25-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="24b25-108">Kontohalduse sihtleht</span><span class="sxs-lookup"><span data-stu-id="24b25-108">Account management landing page</span></span>

<span data-ttu-id="24b25-109">Kontohalduse sihtleht kasutab järgmisi mooduleid.</span><span class="sxs-lookup"><span data-stu-id="24b25-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="24b25-110">**Konteiner** – kõik kontohalduse sihtlehe moodulid tuleb asetada konteinerisse.</span><span class="sxs-lookup"><span data-stu-id="24b25-110">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="24b25-111">**Konto tervituse paan** – seda moodulit kasutatakse kontohalduse lehe tervitussõnumi esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="24b25-111">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="24b25-112">See sisaldab pealkirja atribuute.</span><span class="sxs-lookup"><span data-stu-id="24b25-112">It includes properties for the heading.</span></span>
- <span data-ttu-id="24b25-113">**Konto üldpaan** – seda moodulit saab kasutada kontohalduse lehtede pealkirjade ja linkide esitamiseks, nt lehed "Tellimuste ajalugu" või "Minu profiil".</span><span class="sxs-lookup"><span data-stu-id="24b25-113">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="24b25-114">Üldpaani moodulit saab kasutada mistahes lehe paani konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="24b25-114">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="24b25-115">Fabrikamis kasutatakse seda moodulit "Tellimuse ajaloo" ja "Minu profiili" lehtede linkideks kontohalduse sihtlehel.</span><span class="sxs-lookup"><span data-stu-id="24b25-115">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="24b25-116">**Konto soovinimekirja paan** – seda moodulit kasutatakse kliendi soovinimekirjas olevate kaupade kokkuvõtte esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="24b25-116">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="24b25-117">Näiteks võib see märkida „Teil on soovinimekirjas 10 eset”.</span><span class="sxs-lookup"><span data-stu-id="24b25-117">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="24b25-118">See hõlmab pealkirja ja lingi "Kuva üksikasjad" atribuute.</span><span class="sxs-lookup"><span data-stu-id="24b25-118">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="24b25-119">Link „Kuva üksikasjad” peaks olema konfigureeritud suunama ümber soovinimekirja lehele.</span><span class="sxs-lookup"><span data-stu-id="24b25-119">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="24b25-120">**Konto aadressi paan** – seda moodulit kasutatakse kasutaja aadressi kokkuvõtte esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="24b25-120">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="24b25-121">Näiteks võib see märkida „Teil on kontole lisatud 2 aadressi”.</span><span class="sxs-lookup"><span data-stu-id="24b25-121">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="24b25-122">See hõlmab pealkirja ja lingi "Kuva üksikasjad" atribuute.</span><span class="sxs-lookup"><span data-stu-id="24b25-122">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="24b25-123">Link „Kuva üksikasjad” peaks olema konfigureeritud suunama ümber kasutaja aadressi lehele.</span><span class="sxs-lookup"><span data-stu-id="24b25-123">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="24b25-124">**Konto püsikliendi paan** – seda moodulit kasutatakse püsikliendiprogrammi teabe kuvamiseks ja linkimiseks.</span><span class="sxs-lookup"><span data-stu-id="24b25-124">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="24b25-125">Sellel paanil on kaks olekut: ühes olekus kuvatakse lingid püsikliendiprogrammiga liitumiseks, kui kasutaja pole juba liige.</span><span class="sxs-lookup"><span data-stu-id="24b25-125">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="24b25-126">Teises olekus kuvatakse lingid, et vaadata püsikliendi üksikasjade lehte, kui kasutaja on juba liige.</span><span class="sxs-lookup"><span data-stu-id="24b25-126">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="24b25-127">Atribuudid sisaldavad pealkirja, linki "Registreeru" ja linki "Kuva püsikliendi infot".</span><span class="sxs-lookup"><span data-stu-id="24b25-127">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="24b25-128">Link „Kuva püsikliendi infot” peaks olema konfigureeritud suunama ümber püsikliendi lehele.</span><span class="sxs-lookup"><span data-stu-id="24b25-128">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="24b25-129">Link „Registreeru” peaks olema konfigureeritud suunama ümber lehele, kus kasutajad saavad püsikliendiprogrammiga liituda.</span><span class="sxs-lookup"><span data-stu-id="24b25-129">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="24b25-130">Tellimuste ajaloo leht</span><span class="sxs-lookup"><span data-stu-id="24b25-130">Order history page</span></span>

<span data-ttu-id="24b25-131">Tellimuste ajaloo leht kasutab tellimuste ajaloo moodulit, et näidata kõiki kasutaja hiljuti esitatud tellimusi.</span><span class="sxs-lookup"><span data-stu-id="24b25-131">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="24b25-132">Tellimuse üksikasjade leht</span><span class="sxs-lookup"><span data-stu-id="24b25-132">Order details page</span></span>

<span data-ttu-id="24b25-133">Tellimuste üksikasjade leht pakub iga tellimuse üksikasjalikku teavet ja sellele pääseb ligi tellimuste ajaloo lehelt.</span><span class="sxs-lookup"><span data-stu-id="24b25-133">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="24b25-134">See kasutab tellimuse üksikasjade moodulit, mis nõuab tellimuse üksikasjade toomiseks müügi ID-d või kande ID-d.</span><span class="sxs-lookup"><span data-stu-id="24b25-134">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="24b25-135">Kasutajaprofiili leht</span><span class="sxs-lookup"><span data-stu-id="24b25-135">User profile page</span></span>

<span data-ttu-id="24b25-136">Kasutajaprofiili leht näitab kasutajakonto üksikasju, nagu kasutajanimi ja meiliaadress.</span><span class="sxs-lookup"><span data-stu-id="24b25-136">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="24b25-137">See kasutab kasutajaprofiili üksikasju ja kasutajaprofiili redigeerimise mooduleid.</span><span class="sxs-lookup"><span data-stu-id="24b25-137">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="24b25-138">Kuigi meiliaadressi ei saa eemaldada, saab seda redigeerida.</span><span class="sxs-lookup"><span data-stu-id="24b25-138">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="24b25-139">Kasutajaprofiili lehel kuvatakse ka kasutaja eelistused, mis võimaldavad kasutajal valida või loobuda teatud funktsioonidest, nt soovituste loendite isikupärastamine.</span><span class="sxs-lookup"><span data-stu-id="24b25-139">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="24b25-140">Kasutaja aadressi leht</span><span class="sxs-lookup"><span data-stu-id="24b25-140">User address page</span></span>

<span data-ttu-id="24b25-141">Kasutaja aadressi leht näitab kasutajakontoga seostadatud aadressite loendit.</span><span class="sxs-lookup"><span data-stu-id="24b25-141">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="24b25-142">Kasutaja kas edastas need aadressid maksmise ajal või lisas need sellel lehel otse.</span><span class="sxs-lookup"><span data-stu-id="24b25-142">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="24b25-143">Kasutaja aadressi moodulit kasutatakse lehel aadresside lisamiseks ja redigeerimiseks, peamise aadressi määramiseks ja olemasolevate aadresside muutmiseks.</span><span class="sxs-lookup"><span data-stu-id="24b25-143">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="24b25-144">Soovinimekirja leht</span><span class="sxs-lookup"><span data-stu-id="24b25-144">Wish list page</span></span>

<span data-ttu-id="24b25-145">Soovinimekirja leht näitab kliendi soovinimekirja lisatud esemeid.</span><span class="sxs-lookup"><span data-stu-id="24b25-145">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="24b25-146">See kasutab soovinimekirja esemete renderdamiseks soovinimekirja moodulit.</span><span class="sxs-lookup"><span data-stu-id="24b25-146">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="24b25-147">Püsikliendi leht</span><span class="sxs-lookup"><span data-stu-id="24b25-147">Loyalty page</span></span>

<span data-ttu-id="24b25-148">Püsikliendi leht võimaldab klientidel vaadata oma püsikliendi infot, kui nad on juba püsikliendi programmi liikmed.</span><span class="sxs-lookup"><span data-stu-id="24b25-148">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="24b25-149">Nad saavad vaadata ka punkte, mille nad on viimaste tehingutega teeninud ja lunastanud.</span><span class="sxs-lookup"><span data-stu-id="24b25-149">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="24b25-150">Leht kasutab püsikliendi üksikasjade moodulit püsikliendi üksikasjade näitamiseks.</span><span class="sxs-lookup"><span data-stu-id="24b25-150">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="24b25-151">Püsikliendiprogrammiga liitumiseks saab luua püsikliendiprogrammi registreerumise ja püsikliendi tingimuste mooduliga turunduslehe.</span><span class="sxs-lookup"><span data-stu-id="24b25-151">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="24b25-152">Kui kasutaja ei ole püsikliendiprogrammi liige, siis võimaldavad need moodulid kasutajal registreeruda.</span><span class="sxs-lookup"><span data-stu-id="24b25-152">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24b25-153">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="24b25-153">Additional resources</span></span>

[<span data-ttu-id="24b25-154">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="24b25-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="24b25-155">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="24b25-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="24b25-156">Ostukastimoodul</span><span class="sxs-lookup"><span data-stu-id="24b25-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="24b25-157">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="24b25-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="24b25-158">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="24b25-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="24b25-159">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="24b25-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="24b25-160">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="24b25-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="24b25-161">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="24b25-161">Footer module</span></span>](author-footer-module.md)
