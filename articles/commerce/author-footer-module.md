---
title: Jaluse moodul
description: See teema hõlmab jaluse mooduleid ja kuidas neid rakenduses Dynamics 365 Commerce koostada.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 16c9ca145aff97f0af242da4cf662367f1f4ca3d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211444"
---
# <a name="footer-module"></a><span data-ttu-id="b7b73-103">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="b7b73-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="b7b73-104">See teema hõlmab jaluse mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce luua.</span><span class="sxs-lookup"><span data-stu-id="b7b73-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b7b73-105">Jaluse moodul on erikonteiner, mida kasutatakse lehe jaluses kuvatavate moodulite majutamiseks.</span><span class="sxs-lookup"><span data-stu-id="b7b73-105">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="b7b73-106">Näiteks võib see sisaldada linke saidi erinevatele lehtedele, nagu lehed **Võtke meiega ühendust** ja **Poe eeskirjad**.</span><span class="sxs-lookup"><span data-stu-id="b7b73-106">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="b7b73-107">Järgmisel pildil on näide jaluse moodulist saidi lehel.</span><span class="sxs-lookup"><span data-stu-id="b7b73-107">The following image shows an example of a footer module on a site page.</span></span>

![Jaluse mooduli näide](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="b7b73-109">Jaluse mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="b7b73-109">Footer module properties</span></span> 

<span data-ttu-id="b7b73-110">Nagu enamik konteinereid, toetab jaluse moodul pealkirja ja laiuse atribuute.</span><span class="sxs-lookup"><span data-stu-id="b7b73-110">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="b7b73-111">Samuti toetab mitme jaluse kategooria moodulite lisamist.</span><span class="sxs-lookup"><span data-stu-id="b7b73-111">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="b7b73-112">Iga lisatud jaluse kategooria moodul renderdatakse jaluse mooduli veeruna.</span><span class="sxs-lookup"><span data-stu-id="b7b73-112">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="b7b73-113">Jaluse moodulis saadaolevad moodulid</span><span class="sxs-lookup"><span data-stu-id="b7b73-113">Modules available in a footer module</span></span>

<span data-ttu-id="b7b73-114">**Jaluse üksused** – jaluse üksuste moodul võib sisaldada pealkirja, pilti ja linki.</span><span class="sxs-lookup"><span data-stu-id="b7b73-114">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="b7b73-115">Pealkirja saab kasutada kas eraldi või koos pildi ja lingiga.</span><span class="sxs-lookup"><span data-stu-id="b7b73-115">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="b7b73-116">Iga jaluse linki saab konfigureerida nii, et sellel on ainult tekst (nt lingid „Võtke meiega ühendust” „Privaatsus”), või nii, et sellel on nii tekst kui ka pilt (nt sotsiaalmeedia lingid).</span><span class="sxs-lookup"><span data-stu-id="b7b73-116">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="b7b73-117">**Tagasi üles** – moodul tagasi üles pakub linki kiiresti tagasi lehe ülaossa navigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="b7b73-117">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="b7b73-118">Nõutav on sihtkoht.</span><span class="sxs-lookup"><span data-stu-id="b7b73-118">A destination is required.</span></span> <span data-ttu-id="b7b73-119">Sihtkoha vaikeväärtus on \#, mis viib kasutaja lehekülje ülaossa.</span><span class="sxs-lookup"><span data-stu-id="b7b73-119">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="b7b73-120">Jalusemooduli loomine</span><span class="sxs-lookup"><span data-stu-id="b7b73-120">Create a footer module</span></span>

1. <span data-ttu-id="b7b73-121">Avage **Fragmendid** ja valige uue fragmendi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b7b73-121">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="b7b73-122">Valige dialoogiboksis **Uus fragment** moodul **Konteiner**, sisestage fragmendi nimi ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7b73-122">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b7b73-123">Valige pesas **Vaikekonteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="b7b73-123">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b7b73-124">Valige dialoogiboksis **Lisa moodul** moodul **Jaluse kategooria** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7b73-124">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b7b73-125">Valige pesas **Jaluse kategooria** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="b7b73-125">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b7b73-126">Valige dialoogiboksis **Lisa moodul** moodul **Jaluse üksus** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7b73-126">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b7b73-127">Valige pesa **Jaluse üksus** ja seejärel konfigureerige parempoolsel atribuutide paanil vajaduse pealkiri, link ja lingi tekst ning vajadusel pilt.</span><span class="sxs-lookup"><span data-stu-id="b7b73-127">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="b7b73-128">Rohkemate jaluse üksuste lisamiseks korrake iga kord samme 5 kuni 7.</span><span class="sxs-lookup"><span data-stu-id="b7b73-128">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="b7b73-129">Jalusele lingi „Tagasi üles“ lisamiseks valige pesas **Jaluse kategooria** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="b7b73-129">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="b7b73-130">Valige dialoogiboksis **Lisa moodul** moodul **Tagasi üles** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7b73-130">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b7b73-131">Valige pesa **Tagasi üles** ja seejärel konfigureerige parempoolsel atribuutide paanil vajaduse järgi tekst ja muud mooduli atribuudid.</span><span class="sxs-lookup"><span data-stu-id="b7b73-131">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="b7b73-132">Valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="b7b73-132">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="b7b73-133">Päise igal lehel kuvamise tagamiseks järgige neid samme iga malli jaoks, mis on saidi jaoks loodud.</span><span class="sxs-lookup"><span data-stu-id="b7b73-133">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="b7b73-134">Lisage mooduli **Vaikeleht** pesas **Jalus** loodud jaluse fragment.</span><span class="sxs-lookup"><span data-stu-id="b7b73-134">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="b7b73-135">Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="b7b73-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="b7b73-136">Lisades lehe mallidele fragmendi, aitate tagada, et jalus renderdatakse igal lehel.</span><span class="sxs-lookup"><span data-stu-id="b7b73-136">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7b73-137">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b7b73-137">Additional resources</span></span>

[<span data-ttu-id="b7b73-138">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="b7b73-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b7b73-139">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="b7b73-139">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b7b73-140">Ostukastimoodul</span><span class="sxs-lookup"><span data-stu-id="b7b73-140">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b7b73-141">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="b7b73-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b7b73-142">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="b7b73-142">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b7b73-143">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="b7b73-143">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b7b73-144">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="b7b73-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b7b73-145">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="b7b73-145">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]