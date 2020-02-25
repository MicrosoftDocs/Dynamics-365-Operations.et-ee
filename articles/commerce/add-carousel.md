---
title: Karusellmoodul
description: See teema hõlmab karusellmooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f279d7db0a92df9e64b1d3f6ca01c65ca1478d79
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025777"
---
# <a name="carousel-module"></a><span data-ttu-id="db40a-103">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="db40a-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="db40a-104">See teema hõlmab karusellmooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="db40a-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="db40a-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="db40a-105">Overview</span></span>

<span data-ttu-id="db40a-106">Karussellmoodulit kasutatakse mitme kampaaniakauba (sealhulgas rikastatud piltide) lisamiseks pöörlevale karussellibännerile, mida kliendid saavad sirvida.</span><span class="sxs-lookup"><span data-stu-id="db40a-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="db40a-107">Näiteks saab jaemüüja kasutada avalehel karussellmoodulit, et tutvustada mitut uut toodet või kampaaniat.</span><span class="sxs-lookup"><span data-stu-id="db40a-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="db40a-108">Saate lisada karusellmooduli sisse sisuploki.</span><span class="sxs-lookup"><span data-stu-id="db40a-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="db40a-109">Karussellmooduli atribuudid määratlevad seejärel, kuidas neid mooduleid renderdatakse.</span><span class="sxs-lookup"><span data-stu-id="db40a-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="db40a-110">E-kaubanduse karusellmoodulite näited</span><span class="sxs-lookup"><span data-stu-id="db40a-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="db40a-111">Karuselli, mille sees on mitu kampaaniamoodulit, saab kasutada kodulehel.</span><span class="sxs-lookup"><span data-stu-id="db40a-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="db40a-112">Karuselli, mille sees on mitu kampaaniamoodulit, saab kasutada toote üksikasjade lehel.</span><span class="sxs-lookup"><span data-stu-id="db40a-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="db40a-113">Karusselli saab kasutada mis tahes turunduse lehel, et reklaamida mitut kampaaniat või toodet.</span><span class="sxs-lookup"><span data-stu-id="db40a-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="db40a-114">Karusellmooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="db40a-114">Carousel module properties</span></span>

| <span data-ttu-id="db40a-115">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="db40a-115">Property name</span></span>             | <span data-ttu-id="db40a-116">Väärtus</span><span class="sxs-lookup"><span data-stu-id="db40a-116">Value</span></span>                 | <span data-ttu-id="db40a-117">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="db40a-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="db40a-118">Automaatesitus</span><span class="sxs-lookup"><span data-stu-id="db40a-118">Autoplay</span></span>                  | <span data-ttu-id="db40a-119">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="db40a-119">**True** or **False**</span></span> | <span data-ttu-id="db40a-120">Kui väärtuseks on seatud **Tõene**, toimub karuselli sees üleminek kaupade vahel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="db40a-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="db40a-121">Kui väärtuseks on seatud **Väär**, siis üleminekut ei toimu, kui klient ei kasuta klaviatuuri või hiirt, et liikuda ühelt kaubalt järgmisele kaubale.</span><span class="sxs-lookup"><span data-stu-id="db40a-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="db40a-122">Slaidi ülemineku intervall</span><span class="sxs-lookup"><span data-stu-id="db40a-122">Slide transition interval</span></span> | <span data-ttu-id="db40a-123">Väärtus sekundites</span><span class="sxs-lookup"><span data-stu-id="db40a-123">A value in seconds</span></span>    | <span data-ttu-id="db40a-124">Kaupade vahel üleminekute intervall.</span><span class="sxs-lookup"><span data-stu-id="db40a-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="db40a-125">Siirde tüüp</span><span class="sxs-lookup"><span data-stu-id="db40a-125">Transition type</span></span>           | <span data-ttu-id="db40a-126">**Libisemine** või **Hajumine**</span><span class="sxs-lookup"><span data-stu-id="db40a-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="db40a-127">Ülemineku efekt elementide vahel.</span><span class="sxs-lookup"><span data-stu-id="db40a-127">The transition effect between items.</span></span> |
| <span data-ttu-id="db40a-128">Peida karusselli pöördur</span><span class="sxs-lookup"><span data-stu-id="db40a-128">Hide carousel flipper</span></span>     | <span data-ttu-id="db40a-129">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="db40a-129">**True** or **False**</span></span> | <span data-ttu-id="db40a-130">Kui väärtuseks on seatud **Tõene**, on karusselli keeraja ja indikaator peidetud.</span><span class="sxs-lookup"><span data-stu-id="db40a-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="db40a-131">Luba karusselli hülgamine</span><span class="sxs-lookup"><span data-stu-id="db40a-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="db40a-132">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="db40a-132">**True** or **False**</span></span> | <span data-ttu-id="db40a-133">Kui väärtuseks on seatud **Tõene**, saavad kliendid ise karusselli hüljata.</span><span class="sxs-lookup"><span data-stu-id="db40a-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="db40a-134">Lehele karusellmooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="db40a-134">Add a carousel module to a page</span></span>

<span data-ttu-id="db40a-135">Uuele lehele karusellmooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="db40a-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="db40a-136">Looge lehe mall nimega **karuselli mall**.</span><span class="sxs-lookup"><span data-stu-id="db40a-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="db40a-137">Lisage pesasse **Kehatekst** moodul **Vaikeleht**.</span><span class="sxs-lookup"><span data-stu-id="db40a-137">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="db40a-138">Registreerige mall ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="db40a-138">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="db40a-139">Kasutage äsja loodud karuselli malli, et luua leht, mille nimi on **karuselli leht**.</span><span class="sxs-lookup"><span data-stu-id="db40a-139">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="db40a-140">Lisage uue lehe pessa **Peamine** konteinermoodul.</span><span class="sxs-lookup"><span data-stu-id="db40a-140">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="db40a-141">Seadistage paremal paanil väärtus **Laius** olekusse **Täida ekraan**.</span><span class="sxs-lookup"><span data-stu-id="db40a-141">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="db40a-142">Lisage jaotises **Lehe liigendus** konteineri moodulile karusselli moodul.</span><span class="sxs-lookup"><span data-stu-id="db40a-142">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="db40a-143">Lisage karusselli moodulile sisuploki moodul.</span><span class="sxs-lookup"><span data-stu-id="db40a-143">Add a content block module to the carousel module.</span></span> <span data-ttu-id="db40a-144">Seadistage sisuploki mooduli atribuudid, täites atribuudid **Pealkiri**, **Link**, **Paigutus** ja muud.</span><span class="sxs-lookup"><span data-stu-id="db40a-144">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="db40a-145">Lisage ja konfigureerige teine sisuploki moodul.</span><span class="sxs-lookup"><span data-stu-id="db40a-145">Add and configure another content block module.</span></span>
1. <span data-ttu-id="db40a-146">Seadistage vajadusel karusselli moodulile täiendavaid atribuute.</span><span class="sxs-lookup"><span data-stu-id="db40a-146">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="db40a-147">Salvestage ja kuvage lehe eelvaade.</span><span class="sxs-lookup"><span data-stu-id="db40a-147">Save and preview the page.</span></span> <span data-ttu-id="db40a-148">Lehekülg peaks näitama karusselli, mille sees on kaks moodulit (pannoomoodul ja funktsioonimoodul).</span><span class="sxs-lookup"><span data-stu-id="db40a-148">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="db40a-149">Võite soovitud efekti saavutamiseks muuta karusell-, pannoo- ja funktsioonimoodulite täiendavaid atribuute.</span><span class="sxs-lookup"><span data-stu-id="db40a-149">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="db40a-150">Viige lõpuni lehe redigeerimine ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="db40a-150">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db40a-151">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="db40a-151">Additional resources</span></span>

[<span data-ttu-id="db40a-152">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="db40a-152">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="db40a-153">Reklaambänneri moodul</span><span class="sxs-lookup"><span data-stu-id="db40a-153">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="db40a-154">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="db40a-154">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="db40a-155">Sisuploki moodul</span><span class="sxs-lookup"><span data-stu-id="db40a-155">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="db40a-156">Videopleierimoodul</span><span class="sxs-lookup"><span data-stu-id="db40a-156">Video player module</span></span>](add-video-player.md)
