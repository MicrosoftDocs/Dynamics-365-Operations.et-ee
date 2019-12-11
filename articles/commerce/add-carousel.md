---
title: Karusellmoodul
description: See teema hõlmab karusellmooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785233"
---
# <a name="carousel-module"></a><span data-ttu-id="d35c6-103">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="d35c6-103">Carousel module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d35c6-104">See teema hõlmab karusellmooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="d35c6-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d35c6-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="d35c6-105">Overview</span></span>

<span data-ttu-id="d35c6-106">Karussellmoodulit kasutatakse mitme kampaaniakauba lisamiseks karuselli, mida kliendid saavad sirvida.</span><span class="sxs-lookup"><span data-stu-id="d35c6-106">A carousel module is used to put multiple promotional items in a carousel that customers can browse.</span></span> <span data-ttu-id="d35c6-107">See on spetsiaalne konteinermoodul, mis majutab teisi mooduleid.</span><span class="sxs-lookup"><span data-stu-id="d35c6-107">It's a special container module that hosts other modules.</span></span> <span data-ttu-id="d35c6-108">Näiteks saab jaemüüja kasutada avalehel karussellmoodulit, et tutvustada mitut uut toodet või kampaaniat.</span><span class="sxs-lookup"><span data-stu-id="d35c6-108">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="d35c6-109">Saate lisada karusellmooduli sisse pannoo- ja funktsioonimoodulid.</span><span class="sxs-lookup"><span data-stu-id="d35c6-109">You can add hero and feature modules inside a carousel module.</span></span> <span data-ttu-id="d35c6-110">Karussellmooduli atribuudid määratlevad seejärel, kuidas neid mooduleid renderdatakse.</span><span class="sxs-lookup"><span data-stu-id="d35c6-110">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="d35c6-111">E-kaubanduse karusellmoodulite näited</span><span class="sxs-lookup"><span data-stu-id="d35c6-111">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="d35c6-112">Karuselli, mille sees on mitu kampaaniamoodulit, saab kasutada kodulehel.</span><span class="sxs-lookup"><span data-stu-id="d35c6-112">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="d35c6-113">Karuselli, mille sees on mitu kampaaniamoodulit, saab kasutada toote üksikasjade lehel.</span><span class="sxs-lookup"><span data-stu-id="d35c6-113">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="d35c6-114">Karusselli saab kasutada mis tahes turunduse lehel, et reklaamida mitut kampaaniat või toodet.</span><span class="sxs-lookup"><span data-stu-id="d35c6-114">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="d35c6-115">Karusellmooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="d35c6-115">Carousel module properties</span></span>

| <span data-ttu-id="d35c6-116">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="d35c6-116">Property name</span></span>             | <span data-ttu-id="d35c6-117">Väärtus</span><span class="sxs-lookup"><span data-stu-id="d35c6-117">Value</span></span>                                | <span data-ttu-id="d35c6-118">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d35c6-118">Description</span></span> |
|---------------------------|--------------------------------------|-------------|
| <span data-ttu-id="d35c6-119">Automaatesitus</span><span class="sxs-lookup"><span data-stu-id="d35c6-119">Autoplay</span></span>                  | <span data-ttu-id="d35c6-120">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="d35c6-120">**True** or **False**</span></span>                | <span data-ttu-id="d35c6-121">Kui väärtuseks on seatud **Tõene**, toimub karuselli sees üleminek kaupade vahel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="d35c6-121">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="d35c6-122">Kui väärtuseks on seatud **Väär**, siis üleminekut ei toimu, kui klient ei kasuta klaviatuuri või hiirt, et liikuda ühelt kaubalt järgmisele kaubale.</span><span class="sxs-lookup"><span data-stu-id="d35c6-122">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="d35c6-123">Slaidi ülemineku intervall</span><span class="sxs-lookup"><span data-stu-id="d35c6-123">Slide transition interval</span></span> | <span data-ttu-id="d35c6-124">Väärtus sekundites</span><span class="sxs-lookup"><span data-stu-id="d35c6-124">A value in seconds</span></span>                   | <span data-ttu-id="d35c6-125">Kaupade vahel üleminekute intervall.</span><span class="sxs-lookup"><span data-stu-id="d35c6-125">The interval for transitions between items.</span></span> |
| <span data-ttu-id="d35c6-126">Ülemineku animatsioon</span><span class="sxs-lookup"><span data-stu-id="d35c6-126">Transition animation</span></span>      | <span data-ttu-id="d35c6-127">**Libisemine** või **Hajumine**</span><span class="sxs-lookup"><span data-stu-id="d35c6-127">**Slide** or **Fade**</span></span>                | <span data-ttu-id="d35c6-128">Ülemineku efekt.</span><span class="sxs-lookup"><span data-stu-id="d35c6-128">The transition effect.</span></span> |
| <span data-ttu-id="d35c6-129">Laius</span><span class="sxs-lookup"><span data-stu-id="d35c6-129">Width</span></span>                     | <span data-ttu-id="d35c6-130">**Mahuta konteinerisse** või **Täida ekraan**</span><span class="sxs-lookup"><span data-stu-id="d35c6-130">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="d35c6-131">Kui väärtuseks on seatud **Mahuta konteinerisse**, on karussellis olevad kaubad piiratud karusselli laiusega.</span><span class="sxs-lookup"><span data-stu-id="d35c6-131">If the value is set to **Fit container**, the items inside the carousel are restricted to the width of the carousel.</span></span> <span data-ttu-id="d35c6-132">Kui väärtuseks on seatud **Täida ekraan**, ei ole kaubad karusselli laiusega piiratud, vaid võivad minna täisekraani režiimi.</span><span class="sxs-lookup"><span data-stu-id="d35c6-132">If the value is set to **Fill screen**, the items aren't restricted to the carousel width but can go into full-screen mode.</span></span> <span data-ttu-id="d35c6-133">Soovitud paigutuse saavutamiseks saate väärtust muuta.</span><span class="sxs-lookup"><span data-stu-id="d35c6-133">You can change the value to achieve the desired layout.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="d35c6-134">Lehele karusellmooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="d35c6-134">Add a carousel module to a page</span></span>

<span data-ttu-id="d35c6-135">Uuele lehele karusellmooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d35c6-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d35c6-136">Looge lehe mall nimega **karuselli mall**.</span><span class="sxs-lookup"><span data-stu-id="d35c6-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="d35c6-137">Lisage vaikelehe pessa **Peamine** karusellmoodul.</span><span class="sxs-lookup"><span data-stu-id="d35c6-137">In the **Main** slot of the default page, add a carousel module.</span></span>
1. <span data-ttu-id="d35c6-138">Lisage karusellmoodulile pannoomoodul.</span><span class="sxs-lookup"><span data-stu-id="d35c6-138">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="d35c6-139">Lisage karusellmoodulile funktsioonimoodul.</span><span class="sxs-lookup"><span data-stu-id="d35c6-139">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="d35c6-140">Registreerige mall ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="d35c6-140">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="d35c6-141">Kasutage äsja loodud karuselli malli, et luua leht, mille nimi on **karuselli leht**.</span><span class="sxs-lookup"><span data-stu-id="d35c6-141">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="d35c6-142">Lisage uue lehe pessa **Peamine** karusellmoodul.</span><span class="sxs-lookup"><span data-stu-id="d35c6-142">In the **Main** slot of the new page, add a carousel module.</span></span>
1. <span data-ttu-id="d35c6-143">Määrake karusellmooduli atribuut **Laius** väärtusele **Täida ekraan**.</span><span class="sxs-lookup"><span data-stu-id="d35c6-143">Set the **Width** property of the carousel module to **Fill screen**.</span></span> 
1. <span data-ttu-id="d35c6-144">Määrake atribuut **Ülemineku animatsioon** väärtusele **Libisemine**.</span><span class="sxs-lookup"><span data-stu-id="d35c6-144">Set the **Transition animation** property to **Slide**.</span></span>
1. <span data-ttu-id="d35c6-145">Lisage karusellmoodulile pannoomoodul.</span><span class="sxs-lookup"><span data-stu-id="d35c6-145">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="d35c6-146">Pannoomoodulis lisage pilt ja pealkiri ning valige seejärel **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d35c6-146">In the hero module, add an image and a heading, and then select **Save**.</span></span>
1. <span data-ttu-id="d35c6-147">Lisage karusellmoodulile funktsioonimoodul.</span><span class="sxs-lookup"><span data-stu-id="d35c6-147">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="d35c6-148">Funktsioonimoodulis lisage pilt, pealkiri ja tekstilõik.</span><span class="sxs-lookup"><span data-stu-id="d35c6-148">In the feature module, add an image, a heading, and a paragraph of text.</span></span>
1. <span data-ttu-id="d35c6-149">Salvestage ja kuvage lehe eelvaade.</span><span class="sxs-lookup"><span data-stu-id="d35c6-149">Save and preview the page.</span></span> <span data-ttu-id="d35c6-150">Lehekülg peaks näitama karusselli, mille sees on kaks moodulit (pannoomoodul ja funktsioonimoodul).</span><span class="sxs-lookup"><span data-stu-id="d35c6-150">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="d35c6-151">Võite soovitud efekti saavutamiseks muuta karusell-, pannoo- ja funktsioonimoodulite täiendavaid atribuute.</span><span class="sxs-lookup"><span data-stu-id="d35c6-151">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="d35c6-152">Registreerige leht ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="d35c6-152">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d35c6-153">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d35c6-153">Additional resources</span></span>

[<span data-ttu-id="d35c6-154">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="d35c6-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d35c6-155">Teatise moodul</span><span class="sxs-lookup"><span data-stu-id="d35c6-155">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="d35c6-156">Sisurikas plokimoodul</span><span class="sxs-lookup"><span data-stu-id="d35c6-156">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="d35c6-157">Sisupaigutuse moodul</span><span class="sxs-lookup"><span data-stu-id="d35c6-157">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="d35c6-158">Funktsioonimoodul</span><span class="sxs-lookup"><span data-stu-id="d35c6-158">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="d35c6-159">Pannoomoodul</span><span class="sxs-lookup"><span data-stu-id="d35c6-159">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="d35c6-160">Videopleieri moodul</span><span class="sxs-lookup"><span data-stu-id="d35c6-160">Video player module</span></span>](add-video-player.md)
