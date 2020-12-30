---
title: Mooduliteegi ülevaade
description: Selles teemas antakse ülevaade rakenduse Microsoft Dynamics 365 Commerce mooduliteegi kohta.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: dfc52dd8e14bb2e9f2f9c026ee0e058aee4cedcb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411746"
---
# <a name="module-library-overview"></a><span data-ttu-id="87aa2-103">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="87aa2-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="87aa2-104">Selles teemas antakse ülevaade rakenduse Microsoft Dynamics 365 Commerce mooduliteegi kohta.</span><span class="sxs-lookup"><span data-stu-id="87aa2-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

## <a name="overview"></a><span data-ttu-id="87aa2-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="87aa2-105">Overview</span></span>

<span data-ttu-id="87aa2-106">Rakenduse Dynamics 365 Commerce mooduliteek on moodulikogum, mida saab kasutada e-kaubanduse veebisaidi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="87aa2-106">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="87aa2-107">Moodulitel on nii kasutajaliidese (UI) kui ka funktsionaalse käitumise aspektid.</span><span class="sxs-lookup"><span data-stu-id="87aa2-107">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="87aa2-108">Mooduliteegis olevatele moodulitele saab rakendada kujundusi, et muuta nende välimust ja olemust.</span><span class="sxs-lookup"><span data-stu-id="87aa2-108">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="87aa2-109">Kujundused kasutavad kaskaadlaadistikke (CSS).</span><span class="sxs-lookup"><span data-stu-id="87aa2-109">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="87aa2-110">Mooduliteegis on fiktiivse e-kaubanduse saidi Fabrikam kujundus, mida võib kasutada mallina.</span><span class="sxs-lookup"><span data-stu-id="87aa2-110">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="87aa2-111">Mooduliteegi moodulid</span><span class="sxs-lookup"><span data-stu-id="87aa2-111">Module library modules</span></span>

<span data-ttu-id="87aa2-112">Mooduliteegis on järgmist tüüpi moodulid.</span><span class="sxs-lookup"><span data-stu-id="87aa2-112">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="87aa2-113">**Konteineri moodul** – konteineri moodul on lihtne moodul, mis toimib teiste moodulite hostina.</span><span class="sxs-lookup"><span data-stu-id="87aa2-113">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="87aa2-114">See kontrollib selle sees olevate moodulite paigutust.</span><span class="sxs-lookup"><span data-stu-id="87aa2-114">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="87aa2-115">**Turundusmoodulid** – turundusmoodulid sisaldavad sisubloki, tekstibloki, videopleieri ja karusselli mooduleid.</span><span class="sxs-lookup"><span data-stu-id="87aa2-115">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="87aa2-116">Kõiki neid mooduleid võib kasutada sisu tutvustamiseks.</span><span class="sxs-lookup"><span data-stu-id="87aa2-116">All these modules can be used to showcase content.</span></span> <span data-ttu-id="87aa2-117">Neid saab panna igale lehele ja need põhinevad sisuhaldussüsteemi (CMS) andmetel.</span><span class="sxs-lookup"><span data-stu-id="87aa2-117">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="87aa2-118">**Päise ja jaluse moodulid** – päise ja jaluse moodulid ilmuvad kõikide saidi lehtede päistes ja jalustes.</span><span class="sxs-lookup"><span data-stu-id="87aa2-118">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="87aa2-119">Neid mooduleid saab atribuutide kaudu vajaduse järgi konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="87aa2-119">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="87aa2-120">**Otsingumoodulid** – tooteid saab leida, kasutades päises otsingumoodulit.</span><span class="sxs-lookup"><span data-stu-id="87aa2-120">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="87aa2-121">Otsingutulemused kuvatakse otsingutulemuste lehel.</span><span class="sxs-lookup"><span data-stu-id="87aa2-121">Search results appear on the search results page.</span></span> <span data-ttu-id="87aa2-122">Tooteid saab leida ka kategoorialehtedelt, mis on kanali navigeerimishierarhias toetatud iga kategooria erilehed.</span><span class="sxs-lookup"><span data-stu-id="87aa2-122">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="87aa2-123">Peale selle saab kasutada piiritlusmooduleid, et veelgi filtreerida otsingutulemusi otsingutulemuste ja kategoorialehel.</span><span class="sxs-lookup"><span data-stu-id="87aa2-123">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="87aa2-124">**Toote üksikasjade lehe moodulid** – toote üksikasjade lehel kasutatakse mitut moodulit tooteteabe kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="87aa2-124">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="87aa2-125">Ostukastimoodulis saavad kasutajad vaadata tooteid ja lisada neid ostukorvi.</span><span class="sxs-lookup"><span data-stu-id="87aa2-125">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="87aa2-126">Muud moodulid, nt tehniliste andmete moodul, kuvavad toote üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="87aa2-126">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="87aa2-127">Hinnangute ja arvustuste moodulit saab kasutada arvustuste vaatamiseks ja esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="87aa2-127">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="87aa2-128">**Veebist ostmise ja kauplusest kättesaamise moodul** – veebist ostmise ja kauplusest kättesaamise moodul on integreeritud Bingi kaartidesse.</span><span class="sxs-lookup"><span data-stu-id="87aa2-128">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="87aa2-129">Seda saab kasutada lähedalasuvate poodide leidmiseks, kuhu kliendid saavad ostetud toodetele järele minna.</span><span class="sxs-lookup"><span data-stu-id="87aa2-129">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="87aa2-130">**Ostumoodulid** – ostumoodulid sisaldavad ostukorvimoodulit, mida saab kasutada kaupade lisamiseks ostukorvi.</span><span class="sxs-lookup"><span data-stu-id="87aa2-130">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="87aa2-131">Väljaregistreerimismoodul jäädvustab tarneaadressi, tarnevalikud ja kinkekaardi, püsikliendi programmi ning krediitkaardi teabe, et tellimust saaks töödelda.</span><span class="sxs-lookup"><span data-stu-id="87aa2-131">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="87aa2-132">Pärast tellimuse esitamist saab kasutada tellimuse kinnituse moodulit, et kuvada kinnituse üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="87aa2-132">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="87aa2-133">**Kontohaldusmoodulid** – sisselogimismoodul laseb klientidel sisse logida olemasolevale kontole ja registreerimismoodul laseb luua uue konto.</span><span class="sxs-lookup"><span data-stu-id="87aa2-133">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="87aa2-134">Pärast konto loomist saab hiljutiste tellimuste vaatamiseks kasutada tellimuse ajaloo moodulit ja tellimuse üksikasjade moodulit saab kasutada tellimuse üksikasjade vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="87aa2-134">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="87aa2-135">**Soovituste moodul** – soovitused kuvatakse, kasutades toote paigutamise moodulit.</span><span class="sxs-lookup"><span data-stu-id="87aa2-135">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="87aa2-136">See moodul toetab algoritmilisi ja toimetusloendeid, mida saab tutvustada mis tahes lehel.</span><span class="sxs-lookup"><span data-stu-id="87aa2-136">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87aa2-137">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="87aa2-137">Additional resources</span></span>

[<span data-ttu-id="87aa2-138">Konteineri moodul</span><span class="sxs-lookup"><span data-stu-id="87aa2-138">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="87aa2-139">Ostukastimoodul</span><span class="sxs-lookup"><span data-stu-id="87aa2-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="87aa2-140">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="87aa2-140">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="87aa2-141">Väljaregistreerimismoodul</span><span class="sxs-lookup"><span data-stu-id="87aa2-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="87aa2-142">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="87aa2-142">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="87aa2-143">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="87aa2-143">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="87aa2-144">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="87aa2-144">Footer module</span></span>](author-footer-module.md)
