---
title: Karusellmoodul
description: See teema hõlmab karusellmooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 10ff0cd566a1a8d89ccadce9571dafc5a592520b
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/27/2020
ms.locfileid: "3620982"
---
# <a name="carousel-module"></a><span data-ttu-id="105f1-103">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="105f1-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="105f1-104">See teema hõlmab karusellmooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="105f1-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="105f1-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="105f1-105">Overview</span></span>

<span data-ttu-id="105f1-106">Karussellmoodulit kasutatakse mitme kampaaniakauba (sealhulgas rikastatud piltide) lisamiseks pöörlevale karussellibännerile, mida kliendid saavad sirvida.</span><span class="sxs-lookup"><span data-stu-id="105f1-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="105f1-107">Näiteks saab jaemüüja kasutada avalehel karussellmoodulit, et tutvustada mitut uut toodet või kampaaniat.</span><span class="sxs-lookup"><span data-stu-id="105f1-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="105f1-108">Saate lisada karusellmooduli sisse sisuploki.</span><span class="sxs-lookup"><span data-stu-id="105f1-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="105f1-109">Karussellmooduli atribuudid määratlevad seejärel, kuidas neid mooduleid renderdatakse.</span><span class="sxs-lookup"><span data-stu-id="105f1-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="105f1-110">E-kaubanduse karusellmoodulite näited</span><span class="sxs-lookup"><span data-stu-id="105f1-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="105f1-111">Karuselli, mille sees on mitu kampaaniamoodulit, saab kasutada kodulehel.</span><span class="sxs-lookup"><span data-stu-id="105f1-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="105f1-112">Karuselli, mille sees on mitu kampaaniamoodulit, saab kasutada toote üksikasjade lehel.</span><span class="sxs-lookup"><span data-stu-id="105f1-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="105f1-113">Karusselli saab kasutada mis tahes turunduse lehel, et reklaamida mitut kampaaniat või toodet.</span><span class="sxs-lookup"><span data-stu-id="105f1-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="105f1-114">Järgmisel pildil on näide karussellmoodulist, mida kasutatakse avalehel.</span><span class="sxs-lookup"><span data-stu-id="105f1-114">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="105f1-115">Karussellmoodul sisaldab mitmeid sisu blokeerimise üksuseid.</span><span class="sxs-lookup"><span data-stu-id="105f1-115">This carousel module contains multiple content block items.</span></span>

![Karussellmooduli näide](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="105f1-117">Karusellmooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="105f1-117">Carousel module properties</span></span>

| <span data-ttu-id="105f1-118">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="105f1-118">Property name</span></span>             | <span data-ttu-id="105f1-119">Väärtus</span><span class="sxs-lookup"><span data-stu-id="105f1-119">Value</span></span>                 | <span data-ttu-id="105f1-120">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="105f1-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="105f1-121">Automaatesitus</span><span class="sxs-lookup"><span data-stu-id="105f1-121">Autoplay</span></span>                  | <span data-ttu-id="105f1-122">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="105f1-122">**True** or **False**</span></span> | <span data-ttu-id="105f1-123">Kui väärtuseks on seatud **Tõene**, toimub karuselli sees üleminek kaupade vahel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="105f1-123">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="105f1-124">Kui väärtuseks on seatud **Väär**, siis üleminekut ei toimu, kui klient ei kasuta klaviatuuri või hiirt, et liikuda ühelt kaubalt järgmisele kaubale.</span><span class="sxs-lookup"><span data-stu-id="105f1-124">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="105f1-125">Slaidi ülemineku intervall</span><span class="sxs-lookup"><span data-stu-id="105f1-125">Slide transition interval</span></span> | <span data-ttu-id="105f1-126">Väärtus sekundites</span><span class="sxs-lookup"><span data-stu-id="105f1-126">A value in seconds</span></span>    | <span data-ttu-id="105f1-127">Kaupade vahel üleminekute intervall.</span><span class="sxs-lookup"><span data-stu-id="105f1-127">The interval for transitions between items.</span></span> |
| <span data-ttu-id="105f1-128">Siirde tüüp</span><span class="sxs-lookup"><span data-stu-id="105f1-128">Transition type</span></span>           | <span data-ttu-id="105f1-129">**Libisemine** või **Hajumine**</span><span class="sxs-lookup"><span data-stu-id="105f1-129">**Slide** or **Fade**</span></span> | <span data-ttu-id="105f1-130">Ülemineku efekt elementide vahel.</span><span class="sxs-lookup"><span data-stu-id="105f1-130">The transition effect between items.</span></span> |
| <span data-ttu-id="105f1-131">Peida karusselli pöördur</span><span class="sxs-lookup"><span data-stu-id="105f1-131">Hide carousel flipper</span></span>     | <span data-ttu-id="105f1-132">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="105f1-132">**True** or **False**</span></span> | <span data-ttu-id="105f1-133">Kui väärtuseks on seatud **Tõene**, on karusselli keeraja ja indikaator peidetud.</span><span class="sxs-lookup"><span data-stu-id="105f1-133">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="105f1-134">Luba karusselli hülgamine</span><span class="sxs-lookup"><span data-stu-id="105f1-134">Allow carousel dismiss</span></span>    | <span data-ttu-id="105f1-135">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="105f1-135">**True** or **False**</span></span> | <span data-ttu-id="105f1-136">Kui väärtuseks on seatud **Tõene**, saavad kliendid ise karusselli hüljata.</span><span class="sxs-lookup"><span data-stu-id="105f1-136">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="105f1-137">Lehele karusellmooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="105f1-137">Add a carousel module to a page</span></span>

<span data-ttu-id="105f1-138">Uuele lehele karusellmooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="105f1-138">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="105f1-139">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="105f1-139">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="105f1-140">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Karusselli mall** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="105f1-140">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="105f1-141">Lisage pesasse **Kehatekst** moodul **Vaikeleht**.</span><span class="sxs-lookup"><span data-stu-id="105f1-141">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="105f1-142">Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="105f1-142">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="105f1-143">Kasutage äsja loodud karuselli malli, et luua leht, mille nimi on **Karuselli leht**.</span><span class="sxs-lookup"><span data-stu-id="105f1-143">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="105f1-144">Lisage uue lehe pessa **Peamine** konteinermoodul.</span><span class="sxs-lookup"><span data-stu-id="105f1-144">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="105f1-145">Seadistage paremal paanil väärtus **Laius** olekusse **Täida ekraan**.</span><span class="sxs-lookup"><span data-stu-id="105f1-145">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="105f1-146">Lisage jaotises **Lehe liigendus** konteineri moodulile karusselli moodul.</span><span class="sxs-lookup"><span data-stu-id="105f1-146">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="105f1-147">Lisage karusselli moodulile sisuploki moodul.</span><span class="sxs-lookup"><span data-stu-id="105f1-147">Add a content block module to the carousel module.</span></span> <span data-ttu-id="105f1-148">Seadistage sisuploki mooduli atribuudid, täites atribuudid **Pealkiri**, **Link**, **Paigutus** ja muud.</span><span class="sxs-lookup"><span data-stu-id="105f1-148">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="105f1-149">Lisage ja konfigureerige teine sisuploki moodul.</span><span class="sxs-lookup"><span data-stu-id="105f1-149">Add and configure another content block module.</span></span>
1. <span data-ttu-id="105f1-150">Seadistage vajadusel karusselli moodulile täiendavaid atribuute.</span><span class="sxs-lookup"><span data-stu-id="105f1-150">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="105f1-151">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="105f1-151">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="105f1-152">Lehekülg peaks näitama karusselli, mille sees on kaks moodulit (pannoomoodul ja funktsioonimoodul).</span><span class="sxs-lookup"><span data-stu-id="105f1-152">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="105f1-153">Võite soovitud efekti saavutamiseks muuta karusell-, pannoo- ja funktsioonimoodulite täiendavaid atribuute.</span><span class="sxs-lookup"><span data-stu-id="105f1-153">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="105f1-154">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="105f1-154">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="105f1-155">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="105f1-155">Additional resources</span></span>

[<span data-ttu-id="105f1-156">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="105f1-156">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="105f1-157">Kampaania ribareklaami moodul</span><span class="sxs-lookup"><span data-stu-id="105f1-157">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="105f1-158">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="105f1-158">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="105f1-159">Sisuploki moodul</span><span class="sxs-lookup"><span data-stu-id="105f1-159">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="105f1-160">Videopleierimoodul</span><span class="sxs-lookup"><span data-stu-id="105f1-160">Video player module</span></span>](add-video-player.md)
