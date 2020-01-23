---
title: Pannoomoodul
description: See teema hõlmab pannoomooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785383"
---
# <a name="hero-module"></a><span data-ttu-id="1439e-103">Pannoomoodul</span><span class="sxs-lookup"><span data-stu-id="1439e-103">Hero module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="1439e-104">See teema hõlmab pannoomooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="1439e-104">This topic covers hero modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1439e-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="1439e-105">Overview</span></span>

<span data-ttu-id="1439e-106">Pannoomoodulit kasutatakse toodete või kampaaniate turustamiseks läbi piltide ja teksti kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="1439e-106">A hero module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="1439e-107">Näiteks saab jaemüüja lisada pannoomooduli e-kaubanduse saidi avalehele, et reklaamida uut toodet ja tõmmata klientide tähelepanu.</span><span class="sxs-lookup"><span data-stu-id="1439e-107">For example, a retailer can add a hero module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="1439e-108">Pannoomoodulit juhivad sisuhaldussüsteemi (CMS) andmed.</span><span class="sxs-lookup"><span data-stu-id="1439e-108">A hero module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="1439e-109">See on eraldiseisev moodul, mis ei sõltu ühestki teisest lehe moodulist.</span><span class="sxs-lookup"><span data-stu-id="1439e-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="1439e-110">Pannoomoodulit saab lisada mis tahes saidi lehele, kus jaemüüja soovib midagi turustada või reklaamida (nt tooted, müük või funktsioonid).</span><span class="sxs-lookup"><span data-stu-id="1439e-110">A hero module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-hero-module-in-e-commerce"></a><span data-ttu-id="1439e-111">E-kaubanduse pannoomooduli näited</span><span class="sxs-lookup"><span data-stu-id="1439e-111">Examples of hero module in e-Commerce</span></span>

- <span data-ttu-id="1439e-112">Pannoomoodulit saab kasutada e-kaubanduse saidi avalehel kampaaniate ja uute toodete esiletõstmiseks.</span><span class="sxs-lookup"><span data-stu-id="1439e-112">A hero module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="1439e-113">Pannoomoodulit saab kasutada toote üksikasjade lehel, et esitleda toote teavet.</span><span class="sxs-lookup"><span data-stu-id="1439e-113">A hero module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="1439e-114">Karusellmoodulisse saab lisada mitu pannoomoodulit, et tõsta esile mitu toodet või kampaaniat.</span><span class="sxs-lookup"><span data-stu-id="1439e-114">Multiple hero modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="hero-module-properties"></a><span data-ttu-id="1439e-115">Pannoomooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="1439e-115">Hero module properties</span></span>

| <span data-ttu-id="1439e-116">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="1439e-116">Property name</span></span>  | <span data-ttu-id="1439e-117">Väärtused</span><span class="sxs-lookup"><span data-stu-id="1439e-117">Values</span></span> | <span data-ttu-id="1439e-118">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="1439e-118">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="1439e-119">Pilt</span><span class="sxs-lookup"><span data-stu-id="1439e-119">Image</span></span>          | <span data-ttu-id="1439e-120">Pildifail</span><span class="sxs-lookup"><span data-stu-id="1439e-120">Image file</span></span> | <span data-ttu-id="1439e-121">Toote või kampaania esitlemiseks saab kasutada pilti.</span><span class="sxs-lookup"><span data-stu-id="1439e-121">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="1439e-122">Pildi saab laadida üles pildigaleriisse või kasutada olemasolevat pilti.</span><span class="sxs-lookup"><span data-stu-id="1439e-122">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="1439e-123">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="1439e-123">Heading</span></span>        | <span data-ttu-id="1439e-124">Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**)</span><span class="sxs-lookup"><span data-stu-id="1439e-124">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="1439e-125">Igal pannoomoodulil võib olla pealkiri.</span><span class="sxs-lookup"><span data-stu-id="1439e-125">Every hero module can have a heading.</span></span> <span data-ttu-id="1439e-126">Vaikimisi kasutatakse pealkirja jaks pealkirja silti **H2**.</span><span class="sxs-lookup"><span data-stu-id="1439e-126">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="1439e-127">Samas saab silti muuta, et see vastaks juurdepääsetavuse nõuetele.</span><span class="sxs-lookup"><span data-stu-id="1439e-127">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="1439e-128">Lõik</span><span class="sxs-lookup"><span data-stu-id="1439e-128">Paragraph</span></span>      | <span data-ttu-id="1439e-129">Lõigu tekst</span><span class="sxs-lookup"><span data-stu-id="1439e-129">Paragraph text</span></span> | <span data-ttu-id="1439e-130">Pannoomoodulid toetavad RTF-vormingus lõigu teksti.</span><span class="sxs-lookup"><span data-stu-id="1439e-130">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="1439e-131">Toetatud on mõned põhilised RTF-i võimalused, nagu paks, allajoonitud ja kursiivis tekst ning hüperlingid.</span><span class="sxs-lookup"><span data-stu-id="1439e-131">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="1439e-132">Osasid neid võimalusi saab alistada lehe teema poolt, mis rakendatakse moodulile.</span><span class="sxs-lookup"><span data-stu-id="1439e-132">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="1439e-133">Seos</span><span class="sxs-lookup"><span data-stu-id="1439e-133">Link</span></span>           | <span data-ttu-id="1439e-134">Lingi tekst, lingi URL, silt ARIA (Accessible Rich Internet Applications) ja suvand **Ava link uuel vahekaardil**</span><span class="sxs-lookup"><span data-stu-id="1439e-134">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="1439e-135">Pannoomoodulid toetavad üht või mitut tegutsemiskutse linki.</span><span class="sxs-lookup"><span data-stu-id="1439e-135">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="1439e-136">Lingi lisamisel on nõutavad lingi tekst, URL ja ARIA-silt.</span><span class="sxs-lookup"><span data-stu-id="1439e-136">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="1439e-137">ARIA-sildid peaksid olema kirjeldavad, et vastata juurdepääsetavuse nõuetele.</span><span class="sxs-lookup"><span data-stu-id="1439e-137">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="1439e-138">Linke saab konfigureerida nii, et need avatakse uuel vahekaardil.</span><span class="sxs-lookup"><span data-stu-id="1439e-138">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="1439e-139">Teksti paigutus</span><span class="sxs-lookup"><span data-stu-id="1439e-139">Text placement</span></span> | <span data-ttu-id="1439e-140">**Üleval vasakul**, **üleval paremal**, **üleval keskel**, **all vasakul**, **all paremal**, **all keskel**, **keskel vasakul**, **keskel paremal** või **keskel keskel**</span><span class="sxs-lookup"><span data-stu-id="1439e-140">**Top Left**, **Top Right**, **Top Center**, **Bottom Left**, **Bottom Right**, **Bottom Center**, **Center Left**, **Center Right**, or **Center Center**</span></span> | <span data-ttu-id="1439e-141">See atribuut määratleb pildi asukoha teksti suhtes.</span><span class="sxs-lookup"><span data-stu-id="1439e-141">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="1439e-142">Näiteks kui on valitud suvand **Paremal**, ilmub pilt tekstist paremal.</span><span class="sxs-lookup"><span data-stu-id="1439e-142">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="1439e-143">Teksti teema</span><span class="sxs-lookup"><span data-stu-id="1439e-143">Text theme</span></span>     | <span data-ttu-id="1439e-144">**Hele** või **tume**</span><span class="sxs-lookup"><span data-stu-id="1439e-144">**Light** or **Dark**</span></span> | <span data-ttu-id="1439e-145">Tekstile saab määratleda taustapildi põhjal värviskeemi.</span><span class="sxs-lookup"><span data-stu-id="1439e-145">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="1439e-146">Näiteks kui pildil on tume taust, saab rakendada heledat kujundust, et muuta tekst nähtavamaks ja olla juurdepääsetavuse eesmärgil vastavuses värvide kontrastsuse suhtega.</span><span class="sxs-lookup"><span data-stu-id="1439e-146">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> |
| <span data-ttu-id="1439e-147">Astmik</span><span class="sxs-lookup"><span data-stu-id="1439e-147">Gradient</span></span>       | <span data-ttu-id="1439e-148">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="1439e-148">**True** or **False**</span></span> | <span data-ttu-id="1439e-149">Pildile saab rakendada astmikku, et olla juurdepääsetavuse eesmärgil vastavuses värvide kontrastsuse suhtega.</span><span class="sxs-lookup"><span data-stu-id="1439e-149">A gradient can be applied to the image to meet color contrast ratios for accessibility purposes.</span></span> |

## <a name="add-a-hero-module-to-a-new-page"></a><span data-ttu-id="1439e-150">Pannoomooduli lisamine uuele lehele</span><span class="sxs-lookup"><span data-stu-id="1439e-150">Add a hero module to a new page</span></span>

<span data-ttu-id="1439e-151">Uuele lehele pannoomooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="1439e-151">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="1439e-152">Avage **Mallid** ja looge lehe mall nimega **pannoo mall**.</span><span class="sxs-lookup"><span data-stu-id="1439e-152">Go to **Templates**, and create a page template that is named **hero template**.</span></span>
1. <span data-ttu-id="1439e-153">Lisage vaikelehe pessa **Peamine** pannoomoodul.</span><span class="sxs-lookup"><span data-stu-id="1439e-153">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="1439e-154">Registreerige mall ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="1439e-154">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="1439e-155">Kasutage äsja loodud pannoo malli, et luua leht, mille nimi on **pannoo leht**.</span><span class="sxs-lookup"><span data-stu-id="1439e-155">Use the hero template that you just created to create a page that is named **hero page**.</span></span>
1. <span data-ttu-id="1439e-156">Vaikelehe pesas **Peamine** valige kolmikpunkti nupp (**...**) ja seejärel valige suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="1439e-156">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1439e-157">Dialoogiaknas **Lisa moodul** jaotises **Moodulite valimine** valige pannoomoodul ja klõpsake seejärel nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="1439e-157">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="1439e-158">Valige vasakul liigendpuus pannoomoodul.</span><span class="sxs-lookup"><span data-stu-id="1439e-158">In the outline tree on the left, select the hero module.</span></span>
1. <span data-ttu-id="1439e-159">Parempoolsel atribuutide paanil valige suvand **Lisa pilt**.</span><span class="sxs-lookup"><span data-stu-id="1439e-159">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="1439e-160">Seejärel valige kas olemasolev pilt või laadige üles uus pilt.</span><span class="sxs-lookup"><span data-stu-id="1439e-160">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="1439e-161">Valige suvand **Pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="1439e-161">Select **Heading**.</span></span>
1. <span data-ttu-id="1439e-162">Dialoogiaknas **Pealkiri** lisage pealkirja tekst, valige pealkirja tase ja seejärel klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="1439e-162">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="1439e-163">Suvandis **Rikastekst** lisage tekst, mida vajate.</span><span class="sxs-lookup"><span data-stu-id="1439e-163">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="1439e-164">Valige suvand **Lisa tegevuse link**.</span><span class="sxs-lookup"><span data-stu-id="1439e-164">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="1439e-165">Dialoogiaknas **Tegevuse link** lisage lingi tekst, lingi URL ja lingi ARIA-silt ning klõpsake seejärel nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="1439e-165">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="1439e-166">Salvestage muudatused ja kuvage oma muudatuste eelvaade.</span><span class="sxs-lookup"><span data-stu-id="1439e-166">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="1439e-167">Registreerige leht ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="1439e-167">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1439e-168">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1439e-168">Additional resources</span></span>

[<span data-ttu-id="1439e-169">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="1439e-169">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1439e-170">Teatise moodul</span><span class="sxs-lookup"><span data-stu-id="1439e-170">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="1439e-171">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="1439e-171">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="1439e-172">Sisurikas plokimoodul</span><span class="sxs-lookup"><span data-stu-id="1439e-172">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="1439e-173">Sisupaigutuse moodul</span><span class="sxs-lookup"><span data-stu-id="1439e-173">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="1439e-174">Funktsioonimoodul</span><span class="sxs-lookup"><span data-stu-id="1439e-174">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="1439e-175">Videopleieri moodul</span><span class="sxs-lookup"><span data-stu-id="1439e-175">Video player module</span></span>](add-video-player.md)