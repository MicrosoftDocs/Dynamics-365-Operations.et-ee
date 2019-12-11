---
title: Jaluse moodul
description: See teema hõlmab jaluse mooduleid ja kuidas neid rakenduses Dynamics 365 Commerce koostada.
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7c253cd9620180b09f2f5cae232e46d236deabdd
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697309"
---
# <a name="footer-module"></a><span data-ttu-id="05e6c-103">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="05e6c-103">Footer module</span></span>  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="05e6c-104">See teema hõlmab jaluse mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce luua.</span><span class="sxs-lookup"><span data-stu-id="05e6c-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="05e6c-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="05e6c-105">Overview</span></span>

<span data-ttu-id="05e6c-106">Jaluse moodul on erikonteiner, mida kasutatakse lehe jaluses kuvatavate moodulite majutamiseks.</span><span class="sxs-lookup"><span data-stu-id="05e6c-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="05e6c-107">Näiteks võib see sisaldada linke saidi erinevatele lehtedele, nagu lehed **Võtke meiega ühendust** ja **Poe eeskirjad**.</span><span class="sxs-lookup"><span data-stu-id="05e6c-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

## <a name="footer-module-properties"></a><span data-ttu-id="05e6c-108">Jaluse mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="05e6c-108">Footer module properties</span></span> 

<span data-ttu-id="05e6c-109">Nagu enamik konteinereid, toetab jaluse moodul pealkirja ja laiuse atribuute.</span><span class="sxs-lookup"><span data-stu-id="05e6c-109">Like most containers, a footer module support properties for the heading and the width.</span></span> <span data-ttu-id="05e6c-110">Samuti toetab mitme jaluse kategooria moodulite lisamist.</span><span class="sxs-lookup"><span data-stu-id="05e6c-110">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="05e6c-111">Iga lisatud jaluse kategooria moodul renderdatakse jaluse mooduli veeruna.</span><span class="sxs-lookup"><span data-stu-id="05e6c-111">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="05e6c-112">Jaluse moodulis saadaolevad moodulid</span><span class="sxs-lookup"><span data-stu-id="05e6c-112">Modules available in a footer module</span></span>

<span data-ttu-id="05e6c-113">**Jaluse üksused** – jaluse üksuste moodul võib sisaldada pealkirja, pilti ja linki.</span><span class="sxs-lookup"><span data-stu-id="05e6c-113">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="05e6c-114">Pealkirja saab kasutada kas eraldi või koos pildi ja lingiga.</span><span class="sxs-lookup"><span data-stu-id="05e6c-114">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="05e6c-115">Iga jaluse linki saab konfigureerida nii, et sellel on ainult tekst (nt lingid „Võtke meiega ühendust” „Privaatsus”), või nii, et sellel on nii tekst kui ka pilt (nt sotsiaalmeedia lingid).</span><span class="sxs-lookup"><span data-stu-id="05e6c-115">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="05e6c-116">**Tagasi üles** – moodul tagasi üles pakub linki kiiresti tagasi lehe ülaossa navigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="05e6c-116">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="05e6c-117">Nõutav on sihtkoht.</span><span class="sxs-lookup"><span data-stu-id="05e6c-117">A destination is required.</span></span> <span data-ttu-id="05e6c-118">Sihtkoha vaikeväärtus on #, mis viib kasutaja lehekülje ülaossa.</span><span class="sxs-lookup"><span data-stu-id="05e6c-118">The default destination value is #, which takes the user to the top of the page.</span></span>

## <a name="author-a-footer-module"></a><span data-ttu-id="05e6c-119">Jaluse mooduli koostamine</span><span class="sxs-lookup"><span data-stu-id="05e6c-119">Author a footer module</span></span>

1. <span data-ttu-id="05e6c-120">Valige navigeerimispaanil suvand **Fragmendid** ja valige seejärel **Uus lehe fragment**.</span><span class="sxs-lookup"><span data-stu-id="05e6c-120">In the navigation pane, select **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="05e6c-121">Dialoogiaknas **Uus lehe fragment** valige jaluse moodul, sisestage lehe fragmendi nimi ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="05e6c-121">In the **New Page Fragment** dialog box, select the footer module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="05e6c-122">Valige vasakul liigendpuus jaluse mooduli kolmikpunkti nupp (**…**) ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="05e6c-122">In the outline tree on the left, select the ellipsis button (**...**) for the footer module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="05e6c-123">Valige dialoogiaknas **Lisa moodul** jaluse kategooria moodul ja klõpsake seejärel nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="05e6c-123">In the **Add Module** dialog box, select the footer category module, and then select **OK**.</span></span>
1. <span data-ttu-id="05e6c-124">Valige liigendpuus jaluse kategooria mooduli kolmikpunkti nupp ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="05e6c-124">In the outline tree, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="05e6c-125">Valige dialoogiaknas **Lisa moodul** jaluse üksuse moodul ja klõpsake seejärel nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="05e6c-125">In the **Add Module** dialog box, select the footer item module, and then select **OK**.</span></span>
1. <span data-ttu-id="05e6c-126">Valige liigendpuus jaluse üksuse moodul.</span><span class="sxs-lookup"><span data-stu-id="05e6c-126">In the outline tree, select the footer item module.</span></span> <span data-ttu-id="05e6c-127">Seejärel konfigureerige parempoolsel atribuutide paanil pealkiri, link ja lingi tekst ning vastavalt vajadusele pilt.</span><span class="sxs-lookup"><span data-stu-id="05e6c-127">Then, in the properties pane on the right, configure the heading, link and link text, and image as you require.</span></span>
1. <span data-ttu-id="05e6c-128">Rohkemate jaluse üksuste lisamiseks korrake samme 5 kuni 7.</span><span class="sxs-lookup"><span data-stu-id="05e6c-128">To add more footer items, repeat steps 5 through 7.</span></span>
1. <span data-ttu-id="05e6c-129">Jalusele lingi Tagasi üles lisamiseks valige jaluse kategooria mooduli kolmikpunkti nupp ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="05e6c-129">To add a "back to top" link to your footer, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="05e6c-130">Valige dialoogiaknas **Lisa moodul** tagasi üles moodul ja klõpsake seejärel nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="05e6c-130">In the **Add Module** dialog box, select the back to top module, and then select **OK**.</span></span>
1. <span data-ttu-id="05e6c-131">Valige liigendpuus tagasi üles moodul.</span><span class="sxs-lookup"><span data-stu-id="05e6c-131">In the outline tree, select the back to top module.</span></span> <span data-ttu-id="05e6c-132">Seejärel konfigureerige paremal atribuutide paanil vastavalt vajadusele tagasi üles moodul.</span><span class="sxs-lookup"><span data-stu-id="05e6c-132">Then, in the properties pane on the right, configure the back to top module as you require.</span></span>
1. <span data-ttu-id="05e6c-133">Salvestage lehe fragment, kontrollige seda ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="05e6c-133">Save the page fragment, check it in, and publish it.</span></span>

<span data-ttu-id="05e6c-134">Järgige igal saidi jaoks loodud lehe mallil järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="05e6c-134">On every page template that has been created for the site, follow these steps.</span></span>

1. <span data-ttu-id="05e6c-135">Lisage jaluse mooduli vaikelehe pesas **Peamine** jaluse fragment, mille lõite.</span><span class="sxs-lookup"><span data-stu-id="05e6c-135">In the **Main** slot of the default page, in the footer module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="05e6c-136">Salvestage mall, kontrollige seda ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="05e6c-136">Save the template, check it in, and publish it.</span></span>

<span data-ttu-id="05e6c-137">Lisades lehe mallidele lehe fragmendi, aitate tagada, et jalus renderdatakse igal lehel.</span><span class="sxs-lookup"><span data-stu-id="05e6c-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="05e6c-138">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="05e6c-138">Additional resources</span></span>

[<span data-ttu-id="05e6c-139">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="05e6c-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="05e6c-140">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="05e6c-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="05e6c-141">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="05e6c-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="05e6c-142">Ostukorvi moodul</span><span class="sxs-lookup"><span data-stu-id="05e6c-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="05e6c-143">Maksmise moodul</span><span class="sxs-lookup"><span data-stu-id="05e6c-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="05e6c-144">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="05e6c-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="05e6c-145">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="05e6c-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="05e6c-146">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="05e6c-146">Footer module</span></span>](author-footer-module.md)
