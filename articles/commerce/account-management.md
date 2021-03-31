---
title: Kontohalduse lehed ja moodulid
description: See teema käsitleb kontohalduse lehti ja mooduleid rakenduses Microsoft Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 29523d03fb687684dae7d0ce08208905cce702df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206627"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="17649-103">Kontohalduse lehed ja moodulid</span><span class="sxs-lookup"><span data-stu-id="17649-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="17649-104">See teema käsitleb kontohalduse lehti ja mooduleid rakenduses Microsoft Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="17649-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="17649-105">Kontohaldus viitab lehtede grupile, mida kasutatakse kasutajakontoga seotud teabe haldamiseks rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="17649-105">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="17649-106">Kontohalduse lehed hõlmavad kontohalduse sihtlehte, kasutajaprofiili lehte, kasutaja aadressi lehte, tellimuste ajaloo lehte, tellimuste üksikasjade lehte, püsikliendi lehte ja soovinimekirja lehte.</span><span class="sxs-lookup"><span data-stu-id="17649-106">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="17649-107">Kontohalduse sihtleht</span><span class="sxs-lookup"><span data-stu-id="17649-107">Account management landing page</span></span>

<span data-ttu-id="17649-108">Kontohalduse sihtleht kasutab järgmisi mooduleid.</span><span class="sxs-lookup"><span data-stu-id="17649-108">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="17649-109">**Konteiner** – kõik kontohalduse sihtlehe moodulid tuleb asetada konteinerisse.</span><span class="sxs-lookup"><span data-stu-id="17649-109">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="17649-110">**Konto tervituse paan** – seda moodulit kasutatakse kontohalduse lehe tervitussõnumi esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="17649-110">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="17649-111">See sisaldab pealkirja atribuute.</span><span class="sxs-lookup"><span data-stu-id="17649-111">It includes properties for the heading.</span></span>
- <span data-ttu-id="17649-112">**Konto üldpaan** – seda moodulit saab kasutada kontohalduse lehtede pealkirjade ja linkide esitamiseks, nt lehed "Tellimuste ajalugu" või "Minu profiil".</span><span class="sxs-lookup"><span data-stu-id="17649-112">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="17649-113">Üldpaani moodulit saab kasutada mistahes lehe paani konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="17649-113">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="17649-114">Fabrikamis kasutatakse seda moodulit "Tellimuse ajaloo" ja "Minu profiili" lehtede linkideks kontohalduse sihtlehel.</span><span class="sxs-lookup"><span data-stu-id="17649-114">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="17649-115">**Konto soovinimekirja paan** – seda moodulit kasutatakse kliendi soovinimekirjas olevate kaupade kokkuvõtte esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="17649-115">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="17649-116">Näiteks võib see märkida „Teil on soovinimekirjas 10 eset”.</span><span class="sxs-lookup"><span data-stu-id="17649-116">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="17649-117">See hõlmab pealkirja ja lingi "Kuva üksikasjad" atribuute.</span><span class="sxs-lookup"><span data-stu-id="17649-117">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="17649-118">Link „Kuva üksikasjad” peaks olema konfigureeritud suunama ümber soovinimekirja lehele.</span><span class="sxs-lookup"><span data-stu-id="17649-118">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="17649-119">**Konto aadressi paan** – seda moodulit kasutatakse kasutaja aadressi kokkuvõtte esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="17649-119">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="17649-120">Näiteks võib see märkida „Teil on kontole lisatud 2 aadressi”.</span><span class="sxs-lookup"><span data-stu-id="17649-120">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="17649-121">See hõlmab pealkirja ja lingi "Kuva üksikasjad" atribuute.</span><span class="sxs-lookup"><span data-stu-id="17649-121">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="17649-122">Link „Kuva üksikasjad” peaks olema konfigureeritud suunama ümber kasutaja aadressi lehele.</span><span class="sxs-lookup"><span data-stu-id="17649-122">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="17649-123">**Konto püsikliendi paan** – seda moodulit kasutatakse püsikliendiprogrammi teabe kuvamiseks ja linkimiseks.</span><span class="sxs-lookup"><span data-stu-id="17649-123">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="17649-124">Sellel paanil on kaks olekut: ühes olekus kuvatakse lingid püsikliendiprogrammiga liitumiseks, kui kasutaja pole juba liige.</span><span class="sxs-lookup"><span data-stu-id="17649-124">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="17649-125">Teises olekus kuvatakse lingid, et vaadata püsikliendi üksikasjade lehte, kui kasutaja on juba liige.</span><span class="sxs-lookup"><span data-stu-id="17649-125">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="17649-126">Atribuudid sisaldavad pealkirja, linki "Registreeru" ja linki "Kuva püsikliendi infot".</span><span class="sxs-lookup"><span data-stu-id="17649-126">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="17649-127">Link „Kuva püsikliendi infot” peaks olema konfigureeritud suunama ümber püsikliendi lehele.</span><span class="sxs-lookup"><span data-stu-id="17649-127">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="17649-128">Link „Registreeru” peaks olema konfigureeritud suunama ümber lehele, kus kasutajad saavad püsikliendiprogrammiga liituda.</span><span class="sxs-lookup"><span data-stu-id="17649-128">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="17649-129">Tellimuste ajaloo leht</span><span class="sxs-lookup"><span data-stu-id="17649-129">Order history page</span></span>

<span data-ttu-id="17649-130">Tellimuste ajaloo leht kasutab tellimuste ajaloo moodulit, et näidata kõiki kasutaja hiljuti esitatud tellimusi.</span><span class="sxs-lookup"><span data-stu-id="17649-130">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="17649-131">Tellimuse üksikasjade leht</span><span class="sxs-lookup"><span data-stu-id="17649-131">Order details page</span></span>

<span data-ttu-id="17649-132">Tellimuste üksikasjade leht pakub iga tellimuse üksikasjalikku teavet ja sellele pääseb ligi tellimuste ajaloo lehelt.</span><span class="sxs-lookup"><span data-stu-id="17649-132">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="17649-133">See kasutab tellimuse üksikasjade moodulit, mis nõuab tellimuse üksikasjade toomiseks müügi ID-d või kande ID-d.</span><span class="sxs-lookup"><span data-stu-id="17649-133">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="17649-134">Kasutajaprofiili leht</span><span class="sxs-lookup"><span data-stu-id="17649-134">User profile page</span></span>

<span data-ttu-id="17649-135">Kasutajaprofiili leht näitab kasutajakonto üksikasju, nagu kasutajanimi ja meiliaadress.</span><span class="sxs-lookup"><span data-stu-id="17649-135">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="17649-136">See kasutab kasutajaprofiili üksikasju ja kasutajaprofiili redigeerimise mooduleid.</span><span class="sxs-lookup"><span data-stu-id="17649-136">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="17649-137">Kuigi meiliaadressi ei saa eemaldada, saab seda redigeerida.</span><span class="sxs-lookup"><span data-stu-id="17649-137">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="17649-138">Kasutajaprofiili lehel kuvatakse ka kasutaja eelistused, mis võimaldavad kasutajal valida või loobuda teatud funktsioonidest, nt soovituste loendite isikupärastamine.</span><span class="sxs-lookup"><span data-stu-id="17649-138">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="17649-139">Kasutaja aadressi leht</span><span class="sxs-lookup"><span data-stu-id="17649-139">User address page</span></span>

<span data-ttu-id="17649-140">Kasutaja aadressi leht näitab kasutajakontoga seostadatud aadressite loendit.</span><span class="sxs-lookup"><span data-stu-id="17649-140">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="17649-141">Kasutaja kas edastas need aadressid maksmise ajal või lisas need sellel lehel otse.</span><span class="sxs-lookup"><span data-stu-id="17649-141">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="17649-142">Kasutaja aadressi moodulit kasutatakse lehel aadresside lisamiseks ja redigeerimiseks, peamise aadressi määramiseks ja olemasolevate aadresside muutmiseks.</span><span class="sxs-lookup"><span data-stu-id="17649-142">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="17649-143">Soovinimekirja leht</span><span class="sxs-lookup"><span data-stu-id="17649-143">Wish list page</span></span>

<span data-ttu-id="17649-144">Soovinimekirja leht näitab kliendi soovinimekirja lisatud esemeid.</span><span class="sxs-lookup"><span data-stu-id="17649-144">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="17649-145">See kasutab soovinimekirja esemete renderdamiseks soovinimekirja moodulit.</span><span class="sxs-lookup"><span data-stu-id="17649-145">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="17649-146">Püsikliendi leht</span><span class="sxs-lookup"><span data-stu-id="17649-146">Loyalty page</span></span>

<span data-ttu-id="17649-147">Püsikliendi leht võimaldab klientidel vaadata oma püsikliendi infot, kui nad on juba püsikliendi programmi liikmed.</span><span class="sxs-lookup"><span data-stu-id="17649-147">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="17649-148">Nad saavad vaadata ka punkte, mille nad on viimaste tehingutega teeninud ja lunastanud.</span><span class="sxs-lookup"><span data-stu-id="17649-148">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="17649-149">Leht kasutab püsikliendi üksikasjade moodulit püsikliendi üksikasjade näitamiseks.</span><span class="sxs-lookup"><span data-stu-id="17649-149">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="17649-150">Püsikliendiprogrammiga liitumiseks saab luua püsikliendiprogrammi registreerumise ja püsikliendi tingimuste mooduliga turunduslehe.</span><span class="sxs-lookup"><span data-stu-id="17649-150">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="17649-151">Kui kasutaja ei ole püsikliendiprogrammi liige, siis võimaldavad need moodulid kasutajal registreeruda.</span><span class="sxs-lookup"><span data-stu-id="17649-151">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17649-152">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="17649-152">Additional resources</span></span>

[<span data-ttu-id="17649-153">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="17649-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="17649-154">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="17649-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="17649-155">Ostukastimoodul</span><span class="sxs-lookup"><span data-stu-id="17649-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="17649-156">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="17649-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="17649-157">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="17649-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="17649-158">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="17649-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="17649-159">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="17649-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="17649-160">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="17649-160">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]