---
title: Kontohalduse lehed ja moodulid
description: See teema käsitleb kontohalduse lehti ja mooduleid rakenduses Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f9fc3731cd9d21294b0161e1d419f255096d7790
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885805"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="db2d6-103">Kontohalduse lehed ja moodulid</span><span class="sxs-lookup"><span data-stu-id="db2d6-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="db2d6-104">See teema käsitleb kontohalduse lehti ja mooduleid rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="db2d6-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="db2d6-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="db2d6-105">Overview</span></span>

<span data-ttu-id="db2d6-106">Kontohaldus viitab lehtede grupile, mida kasutatakse kasutajakontoga seotud teabe haldamiseks rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="db2d6-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="db2d6-107">Kontohalduse lehed hõlmavad kontohalduse sihtlehte, kasutajaprofiili lehte, kasutaja aadressi lehte, tellimuste ajaloo lehte, tellimuste üksikasjade lehte, püsikliendi lehte ja soovinimekirja lehte.</span><span class="sxs-lookup"><span data-stu-id="db2d6-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="db2d6-108">Kontohalduse sihtleht</span><span class="sxs-lookup"><span data-stu-id="db2d6-108">Account management landing page</span></span>

<span data-ttu-id="db2d6-109">Kontohalduse sihtleht kasutab järgmisi mooduleid.</span><span class="sxs-lookup"><span data-stu-id="db2d6-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="db2d6-110">**Sisupaigutus** – see moodul on konteinermoodul, mis sisaldab kõiki kontohalduse sihtlehe mooduleid.</span><span class="sxs-lookup"><span data-stu-id="db2d6-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="db2d6-111">**Konto tervituse üksus** – seda moodulit kasutatakse kontohalduse lehe tervitussõnumi esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="db2d6-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="db2d6-112">See hõlmab pealkirja ja paani suuruse atribuute.</span><span class="sxs-lookup"><span data-stu-id="db2d6-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="db2d6-113">Atribuut **Paani suurus** määrab mooduli laiuse sisupaigutuse moodulis.</span><span class="sxs-lookup"><span data-stu-id="db2d6-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="db2d6-114">Väärtused on vahemikus **1** kuni **12**, kus **12** tähistab sisupaigutuse konteineri täielikku laiust.</span><span class="sxs-lookup"><span data-stu-id="db2d6-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="db2d6-115">**Konto tellimuse esitamise üksus** – seda moodulit kasutatakse kasutajakonto esitatud tellimuste koguarvu näitamiseks.</span><span class="sxs-lookup"><span data-stu-id="db2d6-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="db2d6-116">See hõlmab pealkirja, paani suuruse ja üksikasjade kuvamise lingi atribuute.</span><span class="sxs-lookup"><span data-stu-id="db2d6-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="db2d6-117">Link „Kuva üksikasjad” peaks olema konfigureeritud suunama ümber tellimuste ajaloo lehele.</span><span class="sxs-lookup"><span data-stu-id="db2d6-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="db2d6-118">**Kontoprofiili paigutuse üksus** – seda moodulit kasutatakse kasutajaprofiili kokkuvõtte esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="db2d6-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="db2d6-119">See hõlmab pealkirja, paani suuruse ja üksikasjade kuvamise lingi atribuute.</span><span class="sxs-lookup"><span data-stu-id="db2d6-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="db2d6-120">Link „Kuva üksikasjad” peaks olema konfigureeritud suunama ümber kasutajaprofiili lehele.</span><span class="sxs-lookup"><span data-stu-id="db2d6-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="db2d6-121">**Konto soovinimekirja üksus** – seda moodulit kasutatakse kliendi soovinimekirjas olevate kaupade kokkuvõtte esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="db2d6-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="db2d6-122">Näiteks võib see märkida „Teil on soovinimekirjas 10 eset”.</span><span class="sxs-lookup"><span data-stu-id="db2d6-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="db2d6-123">See hõlmab pealkirja, paani suuruse ja üksikasjade kuvamise lingi atribuute.</span><span class="sxs-lookup"><span data-stu-id="db2d6-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="db2d6-124">Link „Kuva üksikasjad” peaks olema konfigureeritud suunama ümber soovinimekirja lehele.</span><span class="sxs-lookup"><span data-stu-id="db2d6-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="db2d6-125">**Konto aadressi üksus** – seda moodulit kasutatakse kasutaja aadressi kokkuvõtte esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="db2d6-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="db2d6-126">Näiteks võib see märkida „Teil on kontole lisatud 2 aadressi”.</span><span class="sxs-lookup"><span data-stu-id="db2d6-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="db2d6-127">See hõlmab pealkirja, paani suuruse ja üksikasjade kuvamise lingi atribuute.</span><span class="sxs-lookup"><span data-stu-id="db2d6-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="db2d6-128">Link „Kuva üksikasjad” peaks olema konfigureeritud suunama ümber kasutaja aadressi lehele.</span><span class="sxs-lookup"><span data-stu-id="db2d6-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="db2d6-129">**Konto püsikliendi üksus** – seda moodulit kasutatakse püsikliendiprogrammi teabe kuvamiseks ja linkimiseks.</span><span class="sxs-lookup"><span data-stu-id="db2d6-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="db2d6-130">See hõlmab pealkirja, paani suuruse, üksikasjade kuvamise lingi ja liikmeks hakkamise lingi atribuute.</span><span class="sxs-lookup"><span data-stu-id="db2d6-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="db2d6-131">Link „Kuva üksikasjad” peaks olema konfigureeritud suunama ümber püsikliendi lehele.</span><span class="sxs-lookup"><span data-stu-id="db2d6-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="db2d6-132">Link „Hakka liikmeks” peaks olema konfigureeritud suunama ümber lehele, kus kasutajad saavad püsikliendiprogrammiga liituda.</span><span class="sxs-lookup"><span data-stu-id="db2d6-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="db2d6-133">Tellimuste ajaloo leht</span><span class="sxs-lookup"><span data-stu-id="db2d6-133">Order history page</span></span>

<span data-ttu-id="db2d6-134">Tellimuste ajaloo leht kasutab tellimuste ajaloo moodulit, et näidata kõiki kasutaja hiljuti esitatud tellimusi.</span><span class="sxs-lookup"><span data-stu-id="db2d6-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="db2d6-135">Tellimuse üksikasjade leht</span><span class="sxs-lookup"><span data-stu-id="db2d6-135">Order details page</span></span>

<span data-ttu-id="db2d6-136">Tellimuste üksikasjade leht pakub iga tellimuse üksikasjalikku teavet ja sellele pääseb ligi tellimuste ajaloo lehelt.</span><span class="sxs-lookup"><span data-stu-id="db2d6-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="db2d6-137">See kasutab tellimuse üksikasjade moodulit, mis nõuab tellimuse üksikasjade toomiseks müügi ID-d või kande ID-d.</span><span class="sxs-lookup"><span data-stu-id="db2d6-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="db2d6-138">Kasutajaprofiili leht</span><span class="sxs-lookup"><span data-stu-id="db2d6-138">User profile page</span></span>

<span data-ttu-id="db2d6-139">Kasutajaprofiili leht näitab kasutajakonto üksikasju, nagu kasutajanimi ja meiliaadress.</span><span class="sxs-lookup"><span data-stu-id="db2d6-139">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="db2d6-140">See kasutab kasutajaprofiili moodulit.</span><span class="sxs-lookup"><span data-stu-id="db2d6-140">It uses the user profile module.</span></span> <span data-ttu-id="db2d6-141">Kuigi meiliaadressi ei saa eemaldada, saab seda redigeerida.</span><span class="sxs-lookup"><span data-stu-id="db2d6-141">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="db2d6-142">Kasutajaprofiili lehel kuvatakse ka kasutaja eelistused, mis võimaldavad kasutajal valida või loobuda teatud funktsioonidest, nt soovituste loendite isikupärastamine.</span><span class="sxs-lookup"><span data-stu-id="db2d6-142">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="db2d6-143">Kasutaja aadressi leht</span><span class="sxs-lookup"><span data-stu-id="db2d6-143">User address page</span></span>

<span data-ttu-id="db2d6-144">Kasutaja aadressi leht näitab kasutajakontoga seostadatud aadressite loendit.</span><span class="sxs-lookup"><span data-stu-id="db2d6-144">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="db2d6-145">Kasutaja kas edastas need aadressid maksmise ajal või lisas need sellel lehel otse.</span><span class="sxs-lookup"><span data-stu-id="db2d6-145">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="db2d6-146">Kasutaja aadressi moodulit kasutatakse lehel aadresside lisamiseks ja redigeerimiseks, peamise aadressi määramiseks ja olemasolevate aadresside muutmiseks.</span><span class="sxs-lookup"><span data-stu-id="db2d6-146">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="db2d6-147">Soovinimekirja leht</span><span class="sxs-lookup"><span data-stu-id="db2d6-147">Wish list page</span></span>

<span data-ttu-id="db2d6-148">Soovinimekirja leht näitab kliendi soovinimekirja lisatud esemeid.</span><span class="sxs-lookup"><span data-stu-id="db2d6-148">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="db2d6-149">See kasutab soovinimekirja esemete renderdamiseks soovinimekirja moodulit.</span><span class="sxs-lookup"><span data-stu-id="db2d6-149">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="db2d6-150">Püsikliendi leht</span><span class="sxs-lookup"><span data-stu-id="db2d6-150">Loyalty page</span></span>

<span data-ttu-id="db2d6-151">Püsikliendi leht võimaldab klientidel liituda püsikliendi programmiga või kui nad on juba püsikliendi programmi liikmed, vaadata oma programmi üksikasju.</span><span class="sxs-lookup"><span data-stu-id="db2d6-151">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="db2d6-152">Nad saavad vaadata ka punkte, mille nad on viimaste tehingutega teeninud ja lunastanud.</span><span class="sxs-lookup"><span data-stu-id="db2d6-152">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db2d6-153">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="db2d6-153">Additional resources</span></span>

[<span data-ttu-id="db2d6-154">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="db2d6-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="db2d6-155">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="db2d6-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="db2d6-156">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="db2d6-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="db2d6-157">Ostukorvi moodul</span><span class="sxs-lookup"><span data-stu-id="db2d6-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="db2d6-158">Maksmise moodul</span><span class="sxs-lookup"><span data-stu-id="db2d6-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="db2d6-159">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="db2d6-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="db2d6-160">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="db2d6-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="db2d6-161">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="db2d6-161">Footer module</span></span>](author-footer-module.md)
