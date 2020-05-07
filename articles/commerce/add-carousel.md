---
title: Karusellmoodul
description: See teema hõlmab karusellmooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: f399e4c5618b65b781fdd3ec835e841614579313
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269724"
---
# <a name="carousel-module"></a><span data-ttu-id="ce433-103">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="ce433-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ce433-104">See teema hõlmab karusellmooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="ce433-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ce433-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="ce433-105">Overview</span></span>

<span data-ttu-id="ce433-106">Karussellmoodulit kasutatakse mitme kampaaniakauba (sealhulgas rikastatud piltide) lisamiseks pöörlevale karussellibännerile, mida kliendid saavad sirvida.</span><span class="sxs-lookup"><span data-stu-id="ce433-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="ce433-107">Näiteks saab jaemüüja kasutada avalehel karussellmoodulit, et tutvustada mitut uut toodet või kampaaniat.</span><span class="sxs-lookup"><span data-stu-id="ce433-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="ce433-108">Saate lisada karusellmooduli sisse sisuploki.</span><span class="sxs-lookup"><span data-stu-id="ce433-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="ce433-109">Karussellmooduli atribuudid määratlevad seejärel, kuidas neid mooduleid renderdatakse.</span><span class="sxs-lookup"><span data-stu-id="ce433-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="ce433-110">E-kaubanduse karusellmoodulite näited</span><span class="sxs-lookup"><span data-stu-id="ce433-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="ce433-111">Karuselli, mille sees on mitu kampaaniamoodulit, saab kasutada kodulehel.</span><span class="sxs-lookup"><span data-stu-id="ce433-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="ce433-112">Karuselli, mille sees on mitu kampaaniamoodulit, saab kasutada toote üksikasjade lehel.</span><span class="sxs-lookup"><span data-stu-id="ce433-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="ce433-113">Karusselli saab kasutada mis tahes turunduse lehel, et reklaamida mitut kampaaniat või toodet.</span><span class="sxs-lookup"><span data-stu-id="ce433-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="ce433-114">Karusellmooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="ce433-114">Carousel module properties</span></span>

| <span data-ttu-id="ce433-115">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="ce433-115">Property name</span></span>             | <span data-ttu-id="ce433-116">Väärtus</span><span class="sxs-lookup"><span data-stu-id="ce433-116">Value</span></span>                 | <span data-ttu-id="ce433-117">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ce433-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="ce433-118">Automaatesitus</span><span class="sxs-lookup"><span data-stu-id="ce433-118">Autoplay</span></span>                  | <span data-ttu-id="ce433-119">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="ce433-119">**True** or **False**</span></span> | <span data-ttu-id="ce433-120">Kui väärtuseks on seatud **Tõene**, toimub karuselli sees üleminek kaupade vahel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="ce433-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="ce433-121">Kui väärtuseks on seatud **Väär**, siis üleminekut ei toimu, kui klient ei kasuta klaviatuuri või hiirt, et liikuda ühelt kaubalt järgmisele kaubale.</span><span class="sxs-lookup"><span data-stu-id="ce433-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="ce433-122">Slaidi ülemineku intervall</span><span class="sxs-lookup"><span data-stu-id="ce433-122">Slide transition interval</span></span> | <span data-ttu-id="ce433-123">Väärtus sekundites</span><span class="sxs-lookup"><span data-stu-id="ce433-123">A value in seconds</span></span>    | <span data-ttu-id="ce433-124">Kaupade vahel üleminekute intervall.</span><span class="sxs-lookup"><span data-stu-id="ce433-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="ce433-125">Siirde tüüp</span><span class="sxs-lookup"><span data-stu-id="ce433-125">Transition type</span></span>           | <span data-ttu-id="ce433-126">**Libisemine** või **Hajumine**</span><span class="sxs-lookup"><span data-stu-id="ce433-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="ce433-127">Ülemineku efekt elementide vahel.</span><span class="sxs-lookup"><span data-stu-id="ce433-127">The transition effect between items.</span></span> |
| <span data-ttu-id="ce433-128">Peida karusselli pöördur</span><span class="sxs-lookup"><span data-stu-id="ce433-128">Hide carousel flipper</span></span>     | <span data-ttu-id="ce433-129">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="ce433-129">**True** or **False**</span></span> | <span data-ttu-id="ce433-130">Kui väärtuseks on seatud **Tõene**, on karusselli keeraja ja indikaator peidetud.</span><span class="sxs-lookup"><span data-stu-id="ce433-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="ce433-131">Luba karusselli hülgamine</span><span class="sxs-lookup"><span data-stu-id="ce433-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="ce433-132">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="ce433-132">**True** or **False**</span></span> | <span data-ttu-id="ce433-133">Kui väärtuseks on seatud **Tõene**, saavad kliendid ise karusselli hüljata.</span><span class="sxs-lookup"><span data-stu-id="ce433-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="ce433-134">Lehele karusellmooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="ce433-134">Add a carousel module to a page</span></span>

<span data-ttu-id="ce433-135">Uuele lehele karusellmooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ce433-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="ce433-136">Valige lehe malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ce433-136">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="ce433-137">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Karusselli mall** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce433-137">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="ce433-138">Lisage pesasse **Kehatekst** moodul **Vaikeleht**.</span><span class="sxs-lookup"><span data-stu-id="ce433-138">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="ce433-139">Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="ce433-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="ce433-140">Kasutage äsja loodud karuselli malli, et luua leht, mille nimi on **Karuselli leht**.</span><span class="sxs-lookup"><span data-stu-id="ce433-140">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="ce433-141">Lisage uue lehe pessa **Peamine** konteinermoodul.</span><span class="sxs-lookup"><span data-stu-id="ce433-141">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="ce433-142">Seadistage paremal paanil väärtus **Laius** olekusse **Täida ekraan**.</span><span class="sxs-lookup"><span data-stu-id="ce433-142">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="ce433-143">Lisage jaotises **Lehe liigendus** konteineri moodulile karusselli moodul.</span><span class="sxs-lookup"><span data-stu-id="ce433-143">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="ce433-144">Lisage karusselli moodulile sisuploki moodul.</span><span class="sxs-lookup"><span data-stu-id="ce433-144">Add a content block module to the carousel module.</span></span> <span data-ttu-id="ce433-145">Seadistage sisuploki mooduli atribuudid, täites atribuudid **Pealkiri**, **Link**, **Paigutus** ja muud.</span><span class="sxs-lookup"><span data-stu-id="ce433-145">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="ce433-146">Lisage ja konfigureerige teine sisuploki moodul.</span><span class="sxs-lookup"><span data-stu-id="ce433-146">Add and configure another content block module.</span></span>
1. <span data-ttu-id="ce433-147">Seadistage vajadusel karusselli moodulile täiendavaid atribuute.</span><span class="sxs-lookup"><span data-stu-id="ce433-147">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="ce433-148">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="ce433-148">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="ce433-149">Lehekülg peaks näitama karusselli, mille sees on kaks moodulit (pannoomoodul ja funktsioonimoodul).</span><span class="sxs-lookup"><span data-stu-id="ce433-149">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="ce433-150">Võite soovitud efekti saavutamiseks muuta karusell-, pannoo- ja funktsioonimoodulite täiendavaid atribuute.</span><span class="sxs-lookup"><span data-stu-id="ce433-150">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="ce433-151">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="ce433-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce433-152">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ce433-152">Additional resources</span></span>

[<span data-ttu-id="ce433-153">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="ce433-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ce433-154">Kampaania ribareklaami moodul</span><span class="sxs-lookup"><span data-stu-id="ce433-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="ce433-155">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="ce433-155">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="ce433-156">Sisuploki moodul</span><span class="sxs-lookup"><span data-stu-id="ce433-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="ce433-157">Videopleierimoodul</span><span class="sxs-lookup"><span data-stu-id="ce433-157">Video player module</span></span>](add-video-player.md)
