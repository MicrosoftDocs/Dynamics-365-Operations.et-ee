---
title: Sisupaigutuse moodul
description: See teema hõlmab sisupaigutuse ja sisupaigutuse üksuse mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785296"
---
# <a name="content-placement-module"></a><span data-ttu-id="a6d5a-103">Sisupaigutuse moodul</span><span class="sxs-lookup"><span data-stu-id="a6d5a-103">Content placement module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a6d5a-104">See teema hõlmab sisupaigutuse ja sisupaigutuse üksuse mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-104">This topic covers content placement and content placement item modules, and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a6d5a-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="a6d5a-105">Overview</span></span>

<span data-ttu-id="a6d5a-106">Sisupaigutuse moodul on erikonteiner, kuhu saab lisada teised moodulid konkreetses paigutuses.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-106">A content placement module is a special container that other modules can be put inside in a specific layout.</span></span> <span data-ttu-id="a6d5a-107">Sisupaigutuse moodulid toetavad järgmist tüüpi mooduleid, nagu järgmised alammoodulid: sisupaigutuse üksus, konto tervituse üksus, konto tellimise üksus, konto soovinimekirja üksus ja konto profiili üksus.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-107">Content placement modules support the following types of modules as child modules: content placement item, account welcome item, account order item, account wish list item, and account profile item.</span></span>

<span data-ttu-id="a6d5a-108">Sisupaigutuse moodulid tuletavad andmeid nende toetatud alammoodulitest.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-108">Content placement modules derive data from the child modules that they support.</span></span> <span data-ttu-id="a6d5a-109">Seetõttu saab sisupaigutuse mooduleid kasutada mitmel viisil, olenevalt sellele lisatavatest moodulitest.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-109">Therefore, content placement modules can be used in various ways, depending on the modules that are added to it.</span></span>

<span data-ttu-id="a6d5a-110">Sisupaigutuse üksuse moodulid kasutavad nii pilte kui ka teksti, et tutvustada kampaaniaid, eeskirju ja toote funktsioone.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-110">Content placement item modules use both images and text to showcase promotions, policies, and product features.</span></span> <span data-ttu-id="a6d5a-111">Näiteks saab sisupaigutuse üksuse moodulit kasutada avalehel poe eeskirjade või tarneteabe kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-111">For example, a content placement item module can be used on a home page to show store policies or shipping information.</span></span> <span data-ttu-id="a6d5a-112">Sisupaigutuse üksuse moodulid põhinevad sisuhaldussüsteemi (CMS) andmetel ja neid saab panna igale lehele.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-112">Content placement item modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="a6d5a-113">Samas saab neid kasutada ainult sisupaigutuse mooduli sees.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-113">However, they can be used only inside a content placement module.</span></span>

## <a name="examples-of-content-placement-modules-in-e-commerce"></a><span data-ttu-id="a6d5a-114">E-kaubanduse sisupaigutuse moodulite näited</span><span class="sxs-lookup"><span data-stu-id="a6d5a-114">Examples of content placement modules in e-Commerce</span></span>

* <span data-ttu-id="a6d5a-115">Sisupaigutuse mooduleid, mis sisaldavad sisupaigutuse üksuse mooduleid, saab kasutada avalehel või turunduse lehtedel, et tutvustada nii piltide kui ka teksti kaudu tootefunktsioone, kampaaniaid, poe eeskirju, tarneteavet ja muud teavet.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-115">Content placement modules that contain content placement item modules can be used on a home page or marketing pages to showcase product features, promotions, store policies, shipping information, and other information through both images and text.</span></span>
* <span data-ttu-id="a6d5a-116">Sisupaigutuse mooduleid, mis sisaldavad sisupaigutuse üksuse mooduleid, saab kasutada toote üksikasjade lehtedel, et tutvustada toote omadusi.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-116">Content placement modules that contain content placement item modules can be used on product details pages to showcase product features.</span></span>
* <span data-ttu-id="a6d5a-117">Sisuhalduse moodulid, mis sisaldavad konto tervitamise üksuse või konto tellimise üksuse mooduleid, saab kasutada kontohalduse lehtedel.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-117">Content placement modules that contain account welcome item or account order item modules can be used on account management pages.</span></span>

## <a name="content-placement-module-properties"></a><span data-ttu-id="a6d5a-118">Sisupaigutuse mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="a6d5a-118">Content placement module properties</span></span>

| <span data-ttu-id="a6d5a-119">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="a6d5a-119">Property name</span></span> | <span data-ttu-id="a6d5a-120">Väärtus</span><span class="sxs-lookup"><span data-stu-id="a6d5a-120">Value</span></span> | <span data-ttu-id="a6d5a-121">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a6d5a-121">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="a6d5a-122">Laius</span><span class="sxs-lookup"><span data-stu-id="a6d5a-122">Width</span></span>         | <span data-ttu-id="a6d5a-123">**Mahuta konteinerisse** või **Täida ekraan**</span><span class="sxs-lookup"><span data-stu-id="a6d5a-123">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="a6d5a-124">Kui väärtuseks on seatud **Mahuta konteinerisse**, on sisupaigutuse moodulis olevad kaubad piiratud sisupaigutuse mooduli laiusega.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-124">If the value is set to **Fit container**, the items inside the content placement module are restricted to the width of the content placement module.</span></span> <span data-ttu-id="a6d5a-125">Kui väärtuseks on seatud **Täida ekraan**, ei ole kaubad sisupaigutuse mooduli laiusega piiratud, vaid võivad minna täisekraani režiimi.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-125">If the value is set to **Fill screen**, the items aren't restricted to the width of the content placement module but can go into full-screen mode.</span></span> |

## <a name="content-placement-item-module-properties"></a><span data-ttu-id="a6d5a-126">Sisupaigutuse üksuse mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="a6d5a-126">Content placement item module properties</span></span>

| <span data-ttu-id="a6d5a-127">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="a6d5a-127">Property name</span></span> | <span data-ttu-id="a6d5a-128">Väärtus</span><span class="sxs-lookup"><span data-stu-id="a6d5a-128">Value</span></span> | <span data-ttu-id="a6d5a-129">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a6d5a-129">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="a6d5a-130">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="a6d5a-130">Heading</span></span>       | <span data-ttu-id="a6d5a-131">Pealkirja tekst ja pealkirja sildid (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**)</span><span class="sxs-lookup"><span data-stu-id="a6d5a-131">Heading text and heading tags (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="a6d5a-132">Igal sisupaigutuse üksuse moodulil võib olla pealkiri.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-132">Every content placement item module can have a heading.</span></span> <span data-ttu-id="a6d5a-133">Atribuut **Pealkirja** toetab pealkirja silte.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-133">The **Heading** property supports heading tags.</span></span> <span data-ttu-id="a6d5a-134">Vaikimisi kasutatakse pealkirja silti **H2**, kuid pealkirja silti saab vajadusel muuta juurdepääsu nõuetele vastavaks.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-134">By default, the **H2** heading tag is used, but the heading tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="a6d5a-135">Lõik</span><span class="sxs-lookup"><span data-stu-id="a6d5a-135">Paragraph</span></span>     | <span data-ttu-id="a6d5a-136">Lõigu tekst</span><span class="sxs-lookup"><span data-stu-id="a6d5a-136">Paragraph text</span></span> | <span data-ttu-id="a6d5a-137">Sisupaigutuse üksuse moodulid toetavad RTF-vormingus lõigu teksti.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-137">Content placement item modules support paragraph text in rich text format.</span></span> <span data-ttu-id="a6d5a-138">Toetatud on mõned põhilised RTF-i võimalused, nagu paks, allajoonitud ja kursiivis tekst ning hüperlingid.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-138">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="a6d5a-139">Osasid neid võimalusi saab alistada lehe teema poolt, mis rakendatakse moodulile.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-139">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="a6d5a-140">Pilt</span><span class="sxs-lookup"><span data-stu-id="a6d5a-140">Image</span></span>         | <span data-ttu-id="a6d5a-141">Pildifail</span><span class="sxs-lookup"><span data-stu-id="a6d5a-141">Image file</span></span> | <span data-ttu-id="a6d5a-142">Tekstiga saab seostada pildi.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-142">An image can be associated with the text.</span></span> |
| <span data-ttu-id="a6d5a-143">Seos</span><span class="sxs-lookup"><span data-stu-id="a6d5a-143">Link</span></span>          | <span data-ttu-id="a6d5a-144">Lingi URL ja lingi tekst</span><span class="sxs-lookup"><span data-stu-id="a6d5a-144">Link URL and link text</span></span> | <span data-ttu-id="a6d5a-145">Tekstile saab lisada lingi, et suunata kasutajad ümber kindlale lehele.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-145">A link can be added to the text to redirect users to a specific page.</span></span> |
| <span data-ttu-id="a6d5a-146">Paani suurus</span><span class="sxs-lookup"><span data-stu-id="a6d5a-146">Tile size</span></span>     | <span data-ttu-id="a6d5a-147">Number vahemikus **1** kuni **12**</span><span class="sxs-lookup"><span data-stu-id="a6d5a-147">A number from **1** through **12**</span></span> | <span data-ttu-id="a6d5a-148">Iga sisupaigutuse üksuse puhul määratleb see atribuut pesade arvu, mille üksus peab sisupaigutuse moodulis täitma.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-148">For each content placement item, this property defines the number of slots that the item should fill in the content placement module.</span></span> <span data-ttu-id="a6d5a-149">Sisupaigutuse mooduli maksimaalne suurus on 12 pesa.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-149">The maximum size of the content placement module is 12 slots.</span></span> <span data-ttu-id="a6d5a-150">Kui sisupaigutuse mooduli esimese *n* üksuse paani kogusuurus ületab 12 pesa, murtakse üksuse teksti read järgmisele reale.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-150">If the total tile size for the first *n* items in the content placement module exceeds 12 slots, the items are wrapped to the next row.</span></span> |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a><span data-ttu-id="a6d5a-151">Sisupaigutuse mooduli lisamine, mis sisaldab lehe sisupaigutuse üksuse moodulit</span><span class="sxs-lookup"><span data-stu-id="a6d5a-151">Add a content placement module that contains a content placement item module to a page</span></span>

<span data-ttu-id="a6d5a-152">Uuele lehele sisupaigutuse mooduli lisamiseks, mis sisaldab sisupaigutuse üksuse moodulit, ja nõutavate atribuutide määramiseks, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-152">To add a content placement module that contains a content placement item module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a6d5a-153">Looge mall nimega **sisupaigutuse mall**.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-153">Create a template that is named **content placement template**.</span></span>
1. <span data-ttu-id="a6d5a-154">Lisage vaikelehe pessa **Peamine** sisupaigutuse moodul.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-154">In the **Main** slot of the default page, add a content placement module.</span></span>
1. <span data-ttu-id="a6d5a-155">Lisage sisupaigutuse moodulis sisupaigutuse üksuse moodul.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-155">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="a6d5a-156">Registreerige mall ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-156">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="a6d5a-157">Kasutage äsja loodud sisupaigutuse malli, et luua leht, mille nimi on **Sisupaigutuse leht**.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-157">Use the content placement template that you just created to create a page that is named **Content placement page**.</span></span>
1. <span data-ttu-id="a6d5a-158">Lisage uue lehe pessa **Peamine** sisupaigutuse moodul.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-158">In the **Main** slot of the new page, add a content placement module.</span></span>
1. <span data-ttu-id="a6d5a-159">Lisage sisupaigutuse moodulis sisupaigutuse üksuse moodul.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-159">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="a6d5a-160">Sisupaigutuse üksuse mooduli atribuutide paanil valige pilt, lisage pealkiri, lisage lõik, lisage link, määrake lingi URL ja määrake paani suuruseks **6**.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-160">In the property pane for the content placement item module, select an image, add a heading, add a paragraph, add a link, set the link URL, and set the tile size to **6**.</span></span>
1. <span data-ttu-id="a6d5a-161">Korrake samme 7 ja 8, et lisada teine sisupaigutuse üksuse moodul, millel on sama paani suurus.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-161">Repeat steps 7 and 8 to add another content placement item module that has the same tile size.</span></span>
1. <span data-ttu-id="a6d5a-162">Salvestage ja kuvage lehe eelvaade.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-162">Save and preview the page.</span></span> <span data-ttu-id="a6d5a-163">Peaksite nägema kahte sisupaigutamise üksust, mis kuvatakse kõrvuti.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-163">You should see two content placement items that appear side by side.</span></span> <span data-ttu-id="a6d5a-164">Saate kohandada iga sisupaigutuse üksuse mooduli atribuuti **Paani suurus** või lisada rohkem mooduleid, et saavutada soovitud paigutus.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-164">You can adjust the **Tile size** property of each content placement item module or add more modules to achieve the desired layout.</span></span>
1. <span data-ttu-id="a6d5a-165">Registreerige leht ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="a6d5a-165">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6d5a-166">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a6d5a-166">Additional resources</span></span>

[<span data-ttu-id="a6d5a-167">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="a6d5a-167">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a6d5a-168">Teatise moodul</span><span class="sxs-lookup"><span data-stu-id="a6d5a-168">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="a6d5a-169">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="a6d5a-169">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="a6d5a-170">Sisurikas plokimoodul</span><span class="sxs-lookup"><span data-stu-id="a6d5a-170">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="a6d5a-171">Funktsioonimoodul</span><span class="sxs-lookup"><span data-stu-id="a6d5a-171">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="a6d5a-172">Pannoomoodul</span><span class="sxs-lookup"><span data-stu-id="a6d5a-172">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="a6d5a-173">Videopleieri moodul</span><span class="sxs-lookup"><span data-stu-id="a6d5a-173">Video player module</span></span>](add-video-player.md)
