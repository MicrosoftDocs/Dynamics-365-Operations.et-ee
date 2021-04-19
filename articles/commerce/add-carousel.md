---
title: Karusellmoodul
description: See teema hõlmab ostukasti mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5bc2227e08dbbf5f76a37180114e5affff131658
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797883"
---
# <a name="carousel-module"></a><span data-ttu-id="2a316-103">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="2a316-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2a316-104">See teema hõlmab ostukasti mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="2a316-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2a316-105">Karussellmoodulit kasutatakse mitme kampaaniakauba (sealhulgas rikastatud piltide) lisamiseks pöörlevale karussellibännerile, mida kliendid saavad sirvida.</span><span class="sxs-lookup"><span data-stu-id="2a316-105">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="2a316-106">Näiteks saab jaemüüja kasutada avalehel karussellmoodulit, et tutvustada mitut uut toodet või kampaaniat.</span><span class="sxs-lookup"><span data-stu-id="2a316-106">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="2a316-107">Saate lisada karusellmooduli sisse sisuploki.</span><span class="sxs-lookup"><span data-stu-id="2a316-107">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="2a316-108">Karussellmooduli atribuudid määratlevad seejärel, kuidas neid mooduleid renderdatakse.</span><span class="sxs-lookup"><span data-stu-id="2a316-108">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="2a316-109">E-kaubanduse karusellmoodulite näited</span><span class="sxs-lookup"><span data-stu-id="2a316-109">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="2a316-110">Karuselli, mille sees on mitu kampaaniamoodulit, saab kasutada kodulehel.</span><span class="sxs-lookup"><span data-stu-id="2a316-110">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="2a316-111">Karuselli, mille sees on mitu kampaaniamoodulit, saab kasutada toote üksikasjade lehel.</span><span class="sxs-lookup"><span data-stu-id="2a316-111">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="2a316-112">Karusselli saab kasutada mis tahes turunduse lehel, et reklaamida mitut kampaaniat või toodet.</span><span class="sxs-lookup"><span data-stu-id="2a316-112">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="2a316-113">Järgmisel pildil on näide karussellmoodulist, mida kasutatakse avalehel.</span><span class="sxs-lookup"><span data-stu-id="2a316-113">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="2a316-114">Karussellmoodul sisaldab mitmeid sisu blokeerimise üksuseid.</span><span class="sxs-lookup"><span data-stu-id="2a316-114">This carousel module contains multiple content block items.</span></span>

![Karussellmooduli näide](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="2a316-116">Karusellmooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="2a316-116">Carousel module properties</span></span>

| <span data-ttu-id="2a316-117">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="2a316-117">Property name</span></span>             | <span data-ttu-id="2a316-118">Väärtus</span><span class="sxs-lookup"><span data-stu-id="2a316-118">Value</span></span>                 | <span data-ttu-id="2a316-119">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2a316-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="2a316-120">Automaatesitus</span><span class="sxs-lookup"><span data-stu-id="2a316-120">Autoplay</span></span>                  | <span data-ttu-id="2a316-121">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="2a316-121">**True** or **False**</span></span> | <span data-ttu-id="2a316-122">Kui väärtuseks on seatud **Tõene**, toimub karuselli sees üleminek kaupade vahel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="2a316-122">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="2a316-123">Kui väärtuseks on seatud **Väär**, siis üleminekut ei toimu, kui klient ei kasuta klaviatuuri või hiirt, et liikuda ühelt kaubalt järgmisele kaubale.</span><span class="sxs-lookup"><span data-stu-id="2a316-123">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="2a316-124">Slaidi ülemineku intervall</span><span class="sxs-lookup"><span data-stu-id="2a316-124">Slide transition interval</span></span> | <span data-ttu-id="2a316-125">Väärtus sekundites</span><span class="sxs-lookup"><span data-stu-id="2a316-125">A value in seconds</span></span>    | <span data-ttu-id="2a316-126">Kaupade vahel üleminekute intervall.</span><span class="sxs-lookup"><span data-stu-id="2a316-126">The interval for transitions between items.</span></span> |
| <span data-ttu-id="2a316-127">Siirde tüüp</span><span class="sxs-lookup"><span data-stu-id="2a316-127">Transition type</span></span>           | <span data-ttu-id="2a316-128">**Libisemine** või **Hajumine**</span><span class="sxs-lookup"><span data-stu-id="2a316-128">**Slide** or **Fade**</span></span> | <span data-ttu-id="2a316-129">Ülemineku efekt elementide vahel.</span><span class="sxs-lookup"><span data-stu-id="2a316-129">The transition effect between items.</span></span> |
| <span data-ttu-id="2a316-130">Peida karusselli pöördur</span><span class="sxs-lookup"><span data-stu-id="2a316-130">Hide carousel flipper</span></span>     | <span data-ttu-id="2a316-131">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="2a316-131">**True** or **False**</span></span> | <span data-ttu-id="2a316-132">Kui väärtuseks on seatud **Tõene**, on karusselli keeraja ja indikaator peidetud.</span><span class="sxs-lookup"><span data-stu-id="2a316-132">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="2a316-133">Luba karusselli hülgamine</span><span class="sxs-lookup"><span data-stu-id="2a316-133">Allow carousel dismiss</span></span>    | <span data-ttu-id="2a316-134">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="2a316-134">**True** or **False**</span></span> | <span data-ttu-id="2a316-135">Kui väärtuseks on seatud **Tõene**, saavad kliendid ise karusselli hüljata.</span><span class="sxs-lookup"><span data-stu-id="2a316-135">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="2a316-136">Lehele karusellmooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="2a316-136">Add a carousel module to a page</span></span>

<span data-ttu-id="2a316-137">Uuele lehele karusellmooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2a316-137">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="2a316-138">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2a316-138">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="2a316-139">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Karusselli mall** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a316-139">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="2a316-140">Lisage pesasse **Kehatekst** moodul **Vaikeleht**.</span><span class="sxs-lookup"><span data-stu-id="2a316-140">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="2a316-141">Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="2a316-141">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="2a316-142">Kasutage äsja loodud karuselli malli, et luua leht, mille nimi on **Karuselli leht**.</span><span class="sxs-lookup"><span data-stu-id="2a316-142">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="2a316-143">Lisage uue lehe pessa **Peamine** konteinermoodul.</span><span class="sxs-lookup"><span data-stu-id="2a316-143">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="2a316-144">Seadistage paremal paanil väärtus **Laius** olekusse **Täida ekraan**.</span><span class="sxs-lookup"><span data-stu-id="2a316-144">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="2a316-145">Lisage jaotises **Lehe liigendus** konteineri moodulile karusselli moodul.</span><span class="sxs-lookup"><span data-stu-id="2a316-145">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="2a316-146">Lisage karusselli moodulile sisuploki moodul.</span><span class="sxs-lookup"><span data-stu-id="2a316-146">Add a content block module to the carousel module.</span></span> <span data-ttu-id="2a316-147">Seadistage sisuploki mooduli atribuudid, täites atribuudid **Pealkiri**, **Link**, **Paigutus** ja muud.</span><span class="sxs-lookup"><span data-stu-id="2a316-147">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="2a316-148">Lisage ja konfigureerige teine sisuploki moodul.</span><span class="sxs-lookup"><span data-stu-id="2a316-148">Add and configure another content block module.</span></span>
1. <span data-ttu-id="2a316-149">Seadistage vajadusel karusselli moodulile täiendavaid atribuute.</span><span class="sxs-lookup"><span data-stu-id="2a316-149">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="2a316-150">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="2a316-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="2a316-151">Lehekülg peaks näitama karusselli, mille sees on kaks moodulit (pannoomoodul ja funktsioonimoodul).</span><span class="sxs-lookup"><span data-stu-id="2a316-151">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="2a316-152">Võite soovitud efekti saavutamiseks muuta karusell-, pannoo- ja funktsioonimoodulite täiendavaid atribuute.</span><span class="sxs-lookup"><span data-stu-id="2a316-152">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="2a316-153">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="2a316-153">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2a316-154">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2a316-154">Additional resources</span></span>

[<span data-ttu-id="2a316-155">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="2a316-155">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2a316-156">Kampaania ribareklaami moodul</span><span class="sxs-lookup"><span data-stu-id="2a316-156">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="2a316-157">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="2a316-157">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="2a316-158">Sisuploki moodul</span><span class="sxs-lookup"><span data-stu-id="2a316-158">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="2a316-159">Videopleierimoodul</span><span class="sxs-lookup"><span data-stu-id="2a316-159">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]