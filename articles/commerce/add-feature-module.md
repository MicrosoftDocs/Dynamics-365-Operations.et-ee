---
title: Funktsioonimoodul
description: See teema hõlmab funktsioonimooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785279"
---
# <a name="feature-module"></a><span data-ttu-id="a505d-103">Funktsioonimoodul</span><span class="sxs-lookup"><span data-stu-id="a505d-103">Feature module</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a505d-104">See teema hõlmab funktsioonimooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="a505d-104">This topic covers feature modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a505d-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="a505d-105">Overview</span></span>

<span data-ttu-id="a505d-106">Funktsioonimoodulit kasutatakse toodete või kampaaniate turustamiseks läbi piltide ja teksti kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="a505d-106">A feature module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="a505d-107">Näiteks saab jaemüüja lisada funktsioonimooduli toote üksikasjade lehele, et tuua esile toote omadused.</span><span class="sxs-lookup"><span data-stu-id="a505d-107">For example, a retailer can add a feature module to a product details page to highlight the features of the product.</span></span>

<span data-ttu-id="a505d-108">Funktsioonimoodulit juhivad sisuhaldussüsteemi (CMS) andmed.</span><span class="sxs-lookup"><span data-stu-id="a505d-108">A feature module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="a505d-109">See on eraldiseisev moodul, mis ei sõltu ühestki teisest lehe moodulist.</span><span class="sxs-lookup"><span data-stu-id="a505d-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="a505d-110">Funktsioonimoodulit saab lisada mis tahes saidi lehele, kus jaemüüja soovib midagi turustada või reklaamida (nt tooted, müük või funktsioonid).</span><span class="sxs-lookup"><span data-stu-id="a505d-110">A feature module can be put on any site page where a retailer wants to market or promote something (for example products, sales, or features).</span></span>

## <a name="examples-of-feature-modules-in-e-commerce"></a><span data-ttu-id="a505d-111">E-kaubanduse funktsioonimoodulite näited</span><span class="sxs-lookup"><span data-stu-id="a505d-111">Examples of feature modules in e-Commerce</span></span>

<span data-ttu-id="a505d-112">Funktsioonimoodulit saab kasutada järgmistel lehtedel.</span><span class="sxs-lookup"><span data-stu-id="a505d-112">A feature module can used on the following pages:</span></span>

- <span data-ttu-id="a505d-113">Toote üksikasjade leht, et tutvustada toote funktsioone</span><span class="sxs-lookup"><span data-stu-id="a505d-113">A product details page, to showcase product features</span></span>
- <span data-ttu-id="a505d-114">Avaleht, et tooteid reklaamida</span><span class="sxs-lookup"><span data-stu-id="a505d-114">The home page, to promote products</span></span>
- <span data-ttu-id="a505d-115">Kategooria leht, et tõsta esile toodete kategooria</span><span class="sxs-lookup"><span data-stu-id="a505d-115">A category page, to highlight a category of products</span></span>

## <a name="feature-module-properties"></a><span data-ttu-id="a505d-116">Funktsioonimooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="a505d-116">Feature module properties</span></span>

| <span data-ttu-id="a505d-117">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="a505d-117">Property name</span></span>     | <span data-ttu-id="a505d-118">Väärtused</span><span class="sxs-lookup"><span data-stu-id="a505d-118">Values</span></span> | <span data-ttu-id="a505d-119">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a505d-119">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="a505d-120">Pilt</span><span class="sxs-lookup"><span data-stu-id="a505d-120">Image</span></span>             | <span data-ttu-id="a505d-121">Pildifail</span><span class="sxs-lookup"><span data-stu-id="a505d-121">Image file</span></span> | <span data-ttu-id="a505d-122">Toote või kampaania turustamiseks saab kasutada pilti.</span><span class="sxs-lookup"><span data-stu-id="a505d-122">An image can be used to market the product or promotion.</span></span> <span data-ttu-id="a505d-123">Pildi saab laadida üles pildigaleriisse või kasutada olemasolevat pilti.</span><span class="sxs-lookup"><span data-stu-id="a505d-123">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="a505d-124">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="a505d-124">Heading</span></span>           | <span data-ttu-id="a505d-125">Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**)</span><span class="sxs-lookup"><span data-stu-id="a505d-125">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="a505d-126">Igal funktsioonimoodulil võib olla pealkiri.</span><span class="sxs-lookup"><span data-stu-id="a505d-126">Every feature module can have a heading.</span></span> <span data-ttu-id="a505d-127">Vaikimisi kasutatakse pealkirja jaks pealkirja silti **H2**.</span><span class="sxs-lookup"><span data-stu-id="a505d-127">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="a505d-128">Samas saab silti muuta, et see vastaks juurdepääsetavuse nõuetele.</span><span class="sxs-lookup"><span data-stu-id="a505d-128">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="a505d-129">Lõik</span><span class="sxs-lookup"><span data-stu-id="a505d-129">Paragraph</span></span>         | <span data-ttu-id="a505d-130">Lõigu tekst</span><span class="sxs-lookup"><span data-stu-id="a505d-130">Paragraph text</span></span> | <span data-ttu-id="a505d-131">Funktsioonimoodulid toetavad RTF-vormingus lõigu teksti.</span><span class="sxs-lookup"><span data-stu-id="a505d-131">Feature modules support paragraph text in rich text format.</span></span> <span data-ttu-id="a505d-132">Toetatud on mõned põhilised RTF-i võimalused, nagu paks, allajoonitud ja kursiivis tekst ning hüperlingid.</span><span class="sxs-lookup"><span data-stu-id="a505d-132">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="a505d-133">Osasid neid võimalusi saab alistada lehe teema poolt, mis rakendatakse moodulile.</span><span class="sxs-lookup"><span data-stu-id="a505d-133">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="a505d-134">Seos</span><span class="sxs-lookup"><span data-stu-id="a505d-134">Link</span></span>              | <span data-ttu-id="a505d-135">Lingi tekst, lingi URL, silt ARIA (Accessible Rich Internet Applications) ja suvand **Ava link uuel vahekaardil**</span><span class="sxs-lookup"><span data-stu-id="a505d-135">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="a505d-136">Funktsioonimoodulid toetavad üht või mitut tegutsemiskutse linki.</span><span class="sxs-lookup"><span data-stu-id="a505d-136">Feature modules support one or more "call to action" links.</span></span> <span data-ttu-id="a505d-137">Lingi lisamisel on nõutavad lingi tekst, URL ja ARIA-silt.</span><span class="sxs-lookup"><span data-stu-id="a505d-137">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="a505d-138">ARIA-sildid peaksid olema kirjeldavad, et vastata juurdepääsetavuse nõuetele.</span><span class="sxs-lookup"><span data-stu-id="a505d-138">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="a505d-139">Linke saab konfigureerida nii, et need avatakse uuel vahekaardil.</span><span class="sxs-lookup"><span data-stu-id="a505d-139">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="a505d-140">Pildi paigutus</span><span class="sxs-lookup"><span data-stu-id="a505d-140">Image placement</span></span>   | <span data-ttu-id="a505d-141">**Paremal**, **Vasakul**, **Üleval** või **All**</span><span class="sxs-lookup"><span data-stu-id="a505d-141">**Right**, **Left**, **Top**, or **Bottom**</span></span> | <span data-ttu-id="a505d-142">See atribuut määratleb pildi asukoha teksti suhtes.</span><span class="sxs-lookup"><span data-stu-id="a505d-142">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="a505d-143">Näiteks kui on valitud suvand **Paremal**, ilmub pilt tekstist paremal.</span><span class="sxs-lookup"><span data-stu-id="a505d-143">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="a505d-144">Pildiveeru suurus</span><span class="sxs-lookup"><span data-stu-id="a505d-144">Image column size</span></span> | <span data-ttu-id="a505d-145">Väärtus vahemikus **1** kuni **12**</span><span class="sxs-lookup"><span data-stu-id="a505d-145">A value from **1** through **12**</span></span> | <span data-ttu-id="a505d-146">See atribuut määratleb pildi suuruse teksti suhtes.</span><span class="sxs-lookup"><span data-stu-id="a505d-146">This property defines the size of the image relative to the text.</span></span> <span data-ttu-id="a505d-147">Suurus on väljendatud veergude arvuna lehel.</span><span class="sxs-lookup"><span data-stu-id="a505d-147">Size is expressed as a number of columns on the page.</span></span> <span data-ttu-id="a505d-148">Lehel on 12 veergu.</span><span class="sxs-lookup"><span data-stu-id="a505d-148">There are 12 columns on a page.</span></span> <span data-ttu-id="a505d-149">Vaikimisi on pilt ja tekst võrdse suurusega (kuus veergu).</span><span class="sxs-lookup"><span data-stu-id="a505d-149">By default, the image and text have equal size (six columns each).</span></span> <span data-ttu-id="a505d-150">Samas saab suurust vastavalt vajadusele reguleerida.</span><span class="sxs-lookup"><span data-stu-id="a505d-150">However, the size can be adjusted as required.</span></span> |

## <a name="add-a-feature-module-to-a-new-page"></a><span data-ttu-id="a505d-151">Uuele lehele funktsioonimooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="a505d-151">Add a feature module to a new page</span></span> 

<span data-ttu-id="a505d-152">Uuele lehele funktsioonimooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a505d-152">To add a feature module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a505d-153">Avage **Mallid** ja looge lehe mall nimega **funktsiooni mall**.</span><span class="sxs-lookup"><span data-stu-id="a505d-153">Go to **Templates**, and create a page template that is named **feature template**.</span></span>
1. <span data-ttu-id="a505d-154">Lisage vaikelehe pessa **Peamine** funktsioonimoodul.</span><span class="sxs-lookup"><span data-stu-id="a505d-154">In the **Main** slot of the default page, add a feature module.</span></span>
1. <span data-ttu-id="a505d-155">Registreerige mall ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="a505d-155">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="a505d-156">Kasutage äsja loodud funktsiooni malli, et luua leht, mille nimi on **funktsiooni leht**.</span><span class="sxs-lookup"><span data-stu-id="a505d-156">Use the feature template that you just created to create a page that is named **feature page**.</span></span>
1. <span data-ttu-id="a505d-157">Vaikelehe pesas **Peamine** valige kolmikpunkti nupp (**...**) ja seejärel valige suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="a505d-157">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a505d-158">Dialoogiaknas **Lisa moodul** jaotises **Moodulite valimine** valige funktsioonimoodul ja klõpsake seejärel nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="a505d-158">In the **Add Module** dialog box, under **Select Modules**, select a feature module, and then select **OK**.</span></span>
1. <span data-ttu-id="a505d-159">Valige vasakul liigendpuus funktsioonimoodul.</span><span class="sxs-lookup"><span data-stu-id="a505d-159">In the outline tree on the left, select the feature module.</span></span>
1. <span data-ttu-id="a505d-160">Parempoolsel atribuutide paanil valige suvand **Lisa pilt**.</span><span class="sxs-lookup"><span data-stu-id="a505d-160">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="a505d-161">Seejärel valige kas olemasolev pilt või laadige üles uus pilt.</span><span class="sxs-lookup"><span data-stu-id="a505d-161">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="a505d-162">Valige suvand **Pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="a505d-162">Select **Heading**.</span></span>
1. <span data-ttu-id="a505d-163">Dialoogiaknas **Pealkiri** lisage pealkirja tekst, valige pealkirja tase ja seejärel klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="a505d-163">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="a505d-164">Suvandis **Rikastekst** lisage tekst, mida vajate.</span><span class="sxs-lookup"><span data-stu-id="a505d-164">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="a505d-165">Valige suvand **Lisa tegevuse link**.</span><span class="sxs-lookup"><span data-stu-id="a505d-165">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="a505d-166">Dialoogiaknas **Tegevuse link** lisage lingi tekst, lingi URL ja lingi ARIA-silt ning klõpsake seejärel nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="a505d-166">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="a505d-167">Salvestage muudatused ja kuvage oma muudatuste eelvaade.</span><span class="sxs-lookup"><span data-stu-id="a505d-167">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="a505d-168">Registreerige leht ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="a505d-168">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a505d-169">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a505d-169">Additional resources</span></span>

[<span data-ttu-id="a505d-170">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="a505d-170">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a505d-171">Teatise moodul</span><span class="sxs-lookup"><span data-stu-id="a505d-171">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="a505d-172">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="a505d-172">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="a505d-173">Sisurikas plokimoodul</span><span class="sxs-lookup"><span data-stu-id="a505d-173">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="a505d-174">Sisupaigutuse moodul</span><span class="sxs-lookup"><span data-stu-id="a505d-174">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="a505d-175">Pannoomoodul</span><span class="sxs-lookup"><span data-stu-id="a505d-175">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="a505d-176">Videopleieri moodul</span><span class="sxs-lookup"><span data-stu-id="a505d-176">Video player module</span></span>](add-video-player.md)
