---
title: Sisuploki moodul
description: See teema hõlmab sisuploki mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
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
ms.openlocfilehash: f91de93ce5ed4813f9f2adbe7678229189b5af2f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025754"
---
# <a name="content-block-module"></a><span data-ttu-id="de56c-103">Sisuploki moodul</span><span class="sxs-lookup"><span data-stu-id="de56c-103">Content block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="de56c-104">See teema hõlmab sisuploki mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="de56c-104">This topic covers content block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="de56c-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="de56c-105">Overview</span></span>

<span data-ttu-id="de56c-106">Sisuploki moodulit kasutatakse toodete või kampaaniate turustamiseks läbi piltide ja teksti kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="de56c-106">A content block module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="de56c-107">Näiteks saab jaemüüja lisada sisuploki mooduli e-kaubanduse saidi avalehele, et reklaamida uut toodet ja tõmmata klientide tähelepanu.</span><span class="sxs-lookup"><span data-stu-id="de56c-107">For example, a retailer can add a content block module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="de56c-108">Sisuploki moodulit juhivad sisuhaldussüsteemi (CMS) andmed.</span><span class="sxs-lookup"><span data-stu-id="de56c-108">A content block module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="de56c-109">See on eraldiseisev moodul, mis ei sõltu ühestki teisest lehe moodulist.</span><span class="sxs-lookup"><span data-stu-id="de56c-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="de56c-110">Sisuploki moodulit saab lisada mis tahes saidi lehele, kus jaemüüja soovib midagi turustada või reklaamida (nt tooted, müük või funktsioonid).</span><span class="sxs-lookup"><span data-stu-id="de56c-110">A content block module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-content-block-module-in-e-commerce"></a><span data-ttu-id="de56c-111">E-kaubanduse sisuploki moodulite näited</span><span class="sxs-lookup"><span data-stu-id="de56c-111">Examples of content block module in e-Commerce</span></span>

- <span data-ttu-id="de56c-112">Sisuploki moodulit saab kasutada e-kaubanduse saidi avalehel kampaaniate ja uute toodete esiletõstmiseks.</span><span class="sxs-lookup"><span data-stu-id="de56c-112">A content block module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="de56c-113">Sisuploki moodulit saab kasutada toote üksikasjade lehel, et esitleda toote teavet.</span><span class="sxs-lookup"><span data-stu-id="de56c-113">A content block module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="de56c-114">Karusellmoodulisse saab lisada mitu sisuploki moodulit, et tõsta esile mitu toodet või kampaaniat.</span><span class="sxs-lookup"><span data-stu-id="de56c-114">Multiple content block modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="content-block-modules-and-themes"></a><span data-ttu-id="de56c-115">Sisuploki moodulid ja kujundused</span><span class="sxs-lookup"><span data-stu-id="de56c-115">Content block modules and themes</span></span>

<span data-ttu-id="de56c-116">Sisuploki moodulid võivad toetada mitmesuguseid kujundusi ja laade kujunduse alusel.</span><span class="sxs-lookup"><span data-stu-id="de56c-116">Content block modules can support various layouts and styles based on a theme.</span></span> <span data-ttu-id="de56c-117">Näiteks on Fabrikami kujunduses toetatud sisuploki mooduli kolme paigutuse variatsiooni: pannoo, funktsioon ja paan.</span><span class="sxs-lookup"><span data-stu-id="de56c-117">For example, the Fabrikam theme supports three layout variations of a content block module: hero, feature, and tile.</span></span> <span data-ttu-id="de56c-118">Pannoo paigutus näitab pilti taustal koos ülekattetekstiga.</span><span class="sxs-lookup"><span data-stu-id="de56c-118">The hero layout shows an image on the background with text overlay.</span></span> <span data-ttu-id="de56c-119">Funktsiooni paigutus näitab pilti ja teksti kõrvuti.</span><span class="sxs-lookup"><span data-stu-id="de56c-119">The feature layout shows an image and text side by side.</span></span> <span data-ttu-id="de56c-120">Paani paigutus võimaldab mitmeid sisuplokke paanivormingus.</span><span class="sxs-lookup"><span data-stu-id="de56c-120">The tile layout allows multiple content blocks in a tile format.</span></span>

<span data-ttu-id="de56c-121">Lisaks võib teema paljastada iga paigutuse jaoks erinevaid atribuute.</span><span class="sxs-lookup"><span data-stu-id="de56c-121">In addition, the theme can expose different properties for each layout.</span></span> <span data-ttu-id="de56c-122">Kujunduse arendaja saab luua rohkem kujundusi rohkemate stiilidega, kasutades selleks sisuploki moodulit.</span><span class="sxs-lookup"><span data-stu-id="de56c-122">A theme developer can build more layouts with more styles using the content block module.</span></span>

<span data-ttu-id="de56c-123">Järgmine pilt näitab sisuploki mooduli näidet pannoo paigutusega.</span><span class="sxs-lookup"><span data-stu-id="de56c-123">The following image shows an example of a content block module with a hero layout.</span></span>

![Pannoo mooduli näide](./media/Hero.PNG)

<span data-ttu-id="de56c-125">Järgmine pilt näitab sisuploki mooduli näidet funktsiooni paigutusega.</span><span class="sxs-lookup"><span data-stu-id="de56c-125">The following image shows an example of a content block module with a feature layout.</span></span>

![Funktsiooni moodulite näited](./media/Feature.PNG)

## <a name="content-block-module-properties"></a><span data-ttu-id="de56c-127">Sisuploki mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="de56c-127">Content block module properties</span></span>

| <span data-ttu-id="de56c-128">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="de56c-128">Property name</span></span>  | <span data-ttu-id="de56c-129">Väärtused</span><span class="sxs-lookup"><span data-stu-id="de56c-129">Values</span></span> | <span data-ttu-id="de56c-130">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="de56c-130">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="de56c-131">Pilt</span><span class="sxs-lookup"><span data-stu-id="de56c-131">Image</span></span>          | <span data-ttu-id="de56c-132">Pildifail</span><span class="sxs-lookup"><span data-stu-id="de56c-132">Image file</span></span> | <span data-ttu-id="de56c-133">Toote või kampaania esitlemiseks saab kasutada pilti.</span><span class="sxs-lookup"><span data-stu-id="de56c-133">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="de56c-134">Pildi saab laadida üles pildigaleriisse või kasutada olemasolevat pilti.</span><span class="sxs-lookup"><span data-stu-id="de56c-134">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="de56c-135">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="de56c-135">Heading</span></span>        | <span data-ttu-id="de56c-136">Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**)</span><span class="sxs-lookup"><span data-stu-id="de56c-136">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="de56c-137">Igal pannoomoodulil võib olla pealkiri.</span><span class="sxs-lookup"><span data-stu-id="de56c-137">Every hero module can have a heading.</span></span> <span data-ttu-id="de56c-138">Vaikimisi kasutatakse pealkirja jaks pealkirja silti **H2**.</span><span class="sxs-lookup"><span data-stu-id="de56c-138">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="de56c-139">Samas saab silti muuta, et see vastaks juurdepääsetavuse nõuetele.</span><span class="sxs-lookup"><span data-stu-id="de56c-139">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="de56c-140">Lõik</span><span class="sxs-lookup"><span data-stu-id="de56c-140">Paragraph</span></span>      | <span data-ttu-id="de56c-141">Lõigu tekst</span><span class="sxs-lookup"><span data-stu-id="de56c-141">Paragraph text</span></span> | <span data-ttu-id="de56c-142">Pannoomoodulid toetavad RTF-vormingus lõigu teksti.</span><span class="sxs-lookup"><span data-stu-id="de56c-142">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="de56c-143">Toetatud on mõned põhilised RTF-i võimalused, nagu paks, allajoonitud ja kursiivis tekst ning hüperlingid.</span><span class="sxs-lookup"><span data-stu-id="de56c-143">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="de56c-144">Osasid neid võimalusi saab alistada lehe teema poolt, mis rakendatakse moodulile.</span><span class="sxs-lookup"><span data-stu-id="de56c-144">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="de56c-145">Seos</span><span class="sxs-lookup"><span data-stu-id="de56c-145">Link</span></span>           | <span data-ttu-id="de56c-146">Lingi tekst, lingi URL, silt ARIA (Accessible Rich Internet Applications) ja suvand **Ava link uuel vahekaardil**</span><span class="sxs-lookup"><span data-stu-id="de56c-146">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="de56c-147">Pannoomoodulid toetavad üht või mitut tegutsemiskutse linki.</span><span class="sxs-lookup"><span data-stu-id="de56c-147">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="de56c-148">Lingi lisamisel on nõutavad lingi tekst, URL ja ARIA-silt.</span><span class="sxs-lookup"><span data-stu-id="de56c-148">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="de56c-149">ARIA-sildid peaksid olema kirjeldavad, et vastata juurdepääsetavuse nõuetele.</span><span class="sxs-lookup"><span data-stu-id="de56c-149">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="de56c-150">Linke saab konfigureerida nii, et need avatakse uuel vahekaardil.</span><span class="sxs-lookup"><span data-stu-id="de56c-150">Links can be configured so that they are opened on a new tab.</span></span> |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a><span data-ttu-id="de56c-151">Sisuploki mooduli atribuudid, mis on paljastatud Fabrikami kujundusega</span><span class="sxs-lookup"><span data-stu-id="de56c-151">Content block module properties exposed by the Fabrikam theme</span></span> 

| <span data-ttu-id="de56c-152">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="de56c-152">Property name</span></span>  | <span data-ttu-id="de56c-153">Väärtused</span><span class="sxs-lookup"><span data-stu-id="de56c-153">Values</span></span> | <span data-ttu-id="de56c-154">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="de56c-154">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="de56c-155">Teksti paigutus</span><span class="sxs-lookup"><span data-stu-id="de56c-155">Text placement</span></span> | <span data-ttu-id="de56c-156">**Vasakul**, **Paremal**, **Keskel**</span><span class="sxs-lookup"><span data-stu-id="de56c-156">**Left**, **Right**, **Center**</span></span> | <span data-ttu-id="de56c-157">See atribuut määratleb teksti asukoha pildi peal.</span><span class="sxs-lookup"><span data-stu-id="de56c-157">This property defines the position of the text on the image.</span></span> <span data-ttu-id="de56c-158">See kehtib ainult pannoo paigutuse kohta.</span><span class="sxs-lookup"><span data-stu-id="de56c-158">It only applies to the hero layout.</span></span> |
| <span data-ttu-id="de56c-159">Teksti teema</span><span class="sxs-lookup"><span data-stu-id="de56c-159">Text theme</span></span>     | <span data-ttu-id="de56c-160">**Hele** või **tume**</span><span class="sxs-lookup"><span data-stu-id="de56c-160">**Light** or **Dark**</span></span> | <span data-ttu-id="de56c-161">Tekstile saab määratleda taustapildi põhjal värviskeemi.</span><span class="sxs-lookup"><span data-stu-id="de56c-161">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="de56c-162">Näiteks kui pildil on tume taust, saab rakendada heledat kujundust, et muuta tekst nähtavamaks ja olla juurdepääsetavuse eesmärgil vastavuses värvide kontrastsuse suhtega.</span><span class="sxs-lookup"><span data-stu-id="de56c-162">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> <span data-ttu-id="de56c-163">See kehtib ainult pannoo paigutuse kohta.</span><span class="sxs-lookup"><span data-stu-id="de56c-163">It only applies to the hero layout.</span></span>|
| <span data-ttu-id="de56c-164">Pildi paigutus</span><span class="sxs-lookup"><span data-stu-id="de56c-164">Image placement</span></span>       | <span data-ttu-id="de56c-165">**Vasakul**,  **Paremal**</span><span class="sxs-lookup"><span data-stu-id="de56c-165">**Left**,  **Right**</span></span> | <span data-ttu-id="de56c-166">See atribuut määrab, kas pilt peaks olema tekstist vasakul või paremal.</span><span class="sxs-lookup"><span data-stu-id="de56c-166">This property specifies if the image should be to the left or right of the text.</span></span> <span data-ttu-id="de56c-167">See kehtib ainult funktsiooni paigutuse kohta.</span><span class="sxs-lookup"><span data-stu-id="de56c-167">It only applies to the feature layout.</span></span>  |

## <a name="add-a-content-block-module-to-a-new-page"></a><span data-ttu-id="de56c-168">Sisuploki mooduli lisamine uuele lehele</span><span class="sxs-lookup"><span data-stu-id="de56c-168">Add a content block module to a new page</span></span>

<span data-ttu-id="de56c-169">Uuele lehele pannoomooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="de56c-169">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="de56c-170">Avage **Mallid** ja looge lehe mall nimega **sisuploki mall**.</span><span class="sxs-lookup"><span data-stu-id="de56c-170">Go to **Templates**, and create a page template that is named **content block template**.</span></span>
1. <span data-ttu-id="de56c-171">Lisage vaikelehe pessa **Peamine** pannoomoodul.</span><span class="sxs-lookup"><span data-stu-id="de56c-171">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="de56c-172">Registreerige mall ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="de56c-172">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="de56c-173">Kasutage äsja loodud pannoo malli, et luua leht, mille nimi on **sisuploki leht**.</span><span class="sxs-lookup"><span data-stu-id="de56c-173">Use the hero template that you just created to create a page that is named **content block page**.</span></span>
1. <span data-ttu-id="de56c-174">Vaikelehe pesas **Peamine** valige kolmikpunkti nupp (**...**) ja seejärel valige suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="de56c-174">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="de56c-175">Dialoogiaknas **Lisa moodul** jaotises **Moodulite valimine** valige pannoomoodul ja klõpsake seejärel nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="de56c-175">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="de56c-176">Valige vasakul liigendpuus sisuploki moodul.</span><span class="sxs-lookup"><span data-stu-id="de56c-176">In the outline tree on the left, select the content block module.</span></span>
1. <span data-ttu-id="de56c-177">Parempoolsel atribuutide paanil valige suvand **Lisa pilt**.</span><span class="sxs-lookup"><span data-stu-id="de56c-177">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="de56c-178">Seejärel valige kas olemasolev pilt või laadige üles uus pilt.</span><span class="sxs-lookup"><span data-stu-id="de56c-178">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="de56c-179">Valige suvand **Pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="de56c-179">Select **Heading**.</span></span>
1. <span data-ttu-id="de56c-180">Dialoogiaknas **Pealkiri** lisage pealkirja tekst, valige pealkirja tase ja seejärel klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="de56c-180">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="de56c-181">Suvandis **Rikastekst** lisage tekst, mida vajate.</span><span class="sxs-lookup"><span data-stu-id="de56c-181">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="de56c-182">Valige **Lisa link**.</span><span class="sxs-lookup"><span data-stu-id="de56c-182">Select **Add Link**.</span></span>
1. <span data-ttu-id="de56c-183">Lisage dialoogiaknas **Link** lingi tekst, lingi URL ja lingi ARIA-silt ning klõpsake seejärel nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="de56c-183">In the **Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="de56c-184">Valige **Pannoo** paigutus.</span><span class="sxs-lookup"><span data-stu-id="de56c-184">Select the **Hero** layout.</span></span>
1. <span data-ttu-id="de56c-185">Salvestage muudatused ja kuvage oma muudatuste eelvaade.</span><span class="sxs-lookup"><span data-stu-id="de56c-185">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="de56c-186">Registreerige leht ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="de56c-186">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="de56c-187">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="de56c-187">Additional resources</span></span>

[<span data-ttu-id="de56c-188">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="de56c-188">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="de56c-189">Reklaambänneri moodul</span><span class="sxs-lookup"><span data-stu-id="de56c-189">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="de56c-190">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="de56c-190">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="de56c-191">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="de56c-191">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="de56c-192">Videopleierimoodul</span><span class="sxs-lookup"><span data-stu-id="de56c-192">Video player module</span></span>](add-video-player.md)
