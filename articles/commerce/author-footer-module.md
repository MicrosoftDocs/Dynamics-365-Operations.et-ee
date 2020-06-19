---
title: Jaluse moodul
description: See teema hõlmab jaluse mooduleid ja kuidas neid rakenduses Dynamics 365 Commerce koostada.
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 87ffc0204019f2f7122c40dc21bdb5de012929d6
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411195"
---
# <a name="footer-module"></a><span data-ttu-id="93648-103">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="93648-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="93648-104">See teema hõlmab jaluse mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce luua.</span><span class="sxs-lookup"><span data-stu-id="93648-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="93648-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="93648-105">Overview</span></span>

<span data-ttu-id="93648-106">Jaluse moodul on erikonteiner, mida kasutatakse lehe jaluses kuvatavate moodulite majutamiseks.</span><span class="sxs-lookup"><span data-stu-id="93648-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="93648-107">Näiteks võib see sisaldada linke saidi erinevatele lehtedele, nagu lehed **Võtke meiega ühendust** ja **Poe eeskirjad**.</span><span class="sxs-lookup"><span data-stu-id="93648-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="93648-108">Järgmisel pildil on näide jaluse moodulist saidi lehel.</span><span class="sxs-lookup"><span data-stu-id="93648-108">The following image shows an example of a footer module on a site page.</span></span>

![Jaluse mooduli näide](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="93648-110">Jaluse mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="93648-110">Footer module properties</span></span> 

<span data-ttu-id="93648-111">Nagu enamik konteinereid, toetab jaluse moodul pealkirja ja laiuse atribuute.</span><span class="sxs-lookup"><span data-stu-id="93648-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="93648-112">Samuti toetab mitme jaluse kategooria moodulite lisamist.</span><span class="sxs-lookup"><span data-stu-id="93648-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="93648-113">Iga lisatud jaluse kategooria moodul renderdatakse jaluse mooduli veeruna.</span><span class="sxs-lookup"><span data-stu-id="93648-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="93648-114">Jaluse moodulis saadaolevad moodulid</span><span class="sxs-lookup"><span data-stu-id="93648-114">Modules available in a footer module</span></span>

<span data-ttu-id="93648-115">**Jaluse üksused** – jaluse üksuste moodul võib sisaldada pealkirja, pilti ja linki.</span><span class="sxs-lookup"><span data-stu-id="93648-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="93648-116">Pealkirja saab kasutada kas eraldi või koos pildi ja lingiga.</span><span class="sxs-lookup"><span data-stu-id="93648-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="93648-117">Iga jaluse linki saab konfigureerida nii, et sellel on ainult tekst (nt lingid „Võtke meiega ühendust” „Privaatsus”), või nii, et sellel on nii tekst kui ka pilt (nt sotsiaalmeedia lingid).</span><span class="sxs-lookup"><span data-stu-id="93648-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="93648-118">**Tagasi üles** – moodul tagasi üles pakub linki kiiresti tagasi lehe ülaossa navigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="93648-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="93648-119">Nõutav on sihtkoht.</span><span class="sxs-lookup"><span data-stu-id="93648-119">A destination is required.</span></span> <span data-ttu-id="93648-120">Sihtkoha vaikeväärtus on \#, mis viib kasutaja lehekülje ülaossa.</span><span class="sxs-lookup"><span data-stu-id="93648-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="93648-121">Jalusemooduli loomine</span><span class="sxs-lookup"><span data-stu-id="93648-121">Create a footer module</span></span>

1. <span data-ttu-id="93648-122">Avage **Lehe fragmendid** ja valige uue fragmendi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="93648-122">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="93648-123">Dialoogiboksis **Uus lehe fragment** valige moodul **Konteiner**, sisestage lehe fragmendi nimi ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="93648-123">In the **New Page Fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="93648-124">Valige pesas **Vaikekonteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="93648-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="93648-125">Valige dialoogiboksis **Lisa moodul** moodul **Jaluse kategooria** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="93648-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="93648-126">Valige pesas **Jaluse kategooria** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="93648-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="93648-127">Valige dialoogiboksis **Lisa moodul** moodul **Jaluse üksus** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="93648-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="93648-128">Valige pesa **Jaluse üksus** ja seejärel konfigureerige parempoolsel atribuutide paanil vajaduse pealkiri, link ja lingi tekst ning vajadusel pilt.</span><span class="sxs-lookup"><span data-stu-id="93648-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="93648-129">Rohkemate jaluse üksuste lisamiseks korrake iga kord samme 5 kuni 7.</span><span class="sxs-lookup"><span data-stu-id="93648-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="93648-130">Jalusele lingi „Tagasi üles“ lisamiseks valige pesas **Jaluse kategooria** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="93648-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="93648-131">Valige dialoogiboksis **Lisa moodul** moodul **Tagasi üles** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="93648-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="93648-132">Valige pesa **Tagasi üles** ja seejärel konfigureerige parempoolsel atribuutide paanil vajaduse järgi tekst ja muud mooduli atribuudid.</span><span class="sxs-lookup"><span data-stu-id="93648-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="93648-133">Valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="93648-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="93648-134">Päise igal lehel kuvamise tagamiseks järgige neid samme iga malli jaoks, mis on saidi jaoks loodud.</span><span class="sxs-lookup"><span data-stu-id="93648-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="93648-135">Lisage mooduli **Vaikeleht** pesas **Jalus** loodud jaluse fragment.</span><span class="sxs-lookup"><span data-stu-id="93648-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="93648-136">Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="93648-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="93648-137">Lisades lehe mallidele lehe fragmendi, aitate tagada, et jalus renderdatakse igal lehel.</span><span class="sxs-lookup"><span data-stu-id="93648-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93648-138">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="93648-138">Additional resources</span></span>

[<span data-ttu-id="93648-139">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="93648-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="93648-140">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="93648-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="93648-141">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="93648-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="93648-142">Ostukorvi moodul</span><span class="sxs-lookup"><span data-stu-id="93648-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="93648-143">Maksmise moodul</span><span class="sxs-lookup"><span data-stu-id="93648-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="93648-144">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="93648-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="93648-145">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="93648-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="93648-146">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="93648-146">Footer module</span></span>](author-footer-module.md)
