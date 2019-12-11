---
title: Sisurikas plokimoodul
description: See teema hõlmab sisurikkaid plokimooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785417"
---
# <a name="content-rich-block-module"></a><span data-ttu-id="d90d2-103">Sisurikas plokimoodul</span><span class="sxs-lookup"><span data-stu-id="d90d2-103">Content rich block module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d90d2-104">See teema hõlmab sisurikkaid plokimooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="d90d2-104">This topic covers content rich block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d90d2-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="d90d2-105">Overview</span></span>

<span data-ttu-id="d90d2-106">Sisurikas plokimoodul on erikonteiner, kuhu saab lisada ühe või mitu sisurikka ploki üksust.</span><span class="sxs-lookup"><span data-stu-id="d90d2-106">A content rich block module is a special container that one or more content rich block items can be put inside.</span></span> <span data-ttu-id="d90d2-107">Sisurikkaid plokimooduleid kasutatakse lehe tekstiliseks sisuks.</span><span class="sxs-lookup"><span data-stu-id="d90d2-107">Content rich block modules are used for textual content on a page.</span></span> <span data-ttu-id="d90d2-108">See sisu võib olla kas teavitav või kampaaniaga seotud.</span><span class="sxs-lookup"><span data-stu-id="d90d2-108">This content can be either informational or promotional.</span></span>

<span data-ttu-id="d90d2-109">Sisurikkad plokimoodulid põhinevad sisuhaldussüsteemi (CMS) andmetel ja neid saab panna igale lehele.</span><span class="sxs-lookup"><span data-stu-id="d90d2-109">Content rich block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="d90d2-110">Need on eraldiseisvad moodulid, mis ei sõltu lehekülje kontekstist ega ühestki teisest moodulist.</span><span class="sxs-lookup"><span data-stu-id="d90d2-110">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a><span data-ttu-id="d90d2-111">E-kaubanduse sisurikaste plokimoodulite näited</span><span class="sxs-lookup"><span data-stu-id="d90d2-111">Examples of content rich block modules in e-Commerce</span></span>

<span data-ttu-id="d90d2-112">Sisurikkaid plokimooduleid saab kasutada järgmistel viisidel.</span><span class="sxs-lookup"><span data-stu-id="d90d2-112">Content rich block modules can be used in the following ways:</span></span>

* <span data-ttu-id="d90d2-113">Toote üksikasjade lehel toote funktsioonide tutvustamiseks.</span><span class="sxs-lookup"><span data-stu-id="d90d2-113">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="d90d2-114">Teavitamise eesmärgil mis tahes lehel.</span><span class="sxs-lookup"><span data-stu-id="d90d2-114">For informational purposes on any page.</span></span> <span data-ttu-id="d90d2-115">Näiteks võivad need selgitada püsikliendiprogrammide eeliseid, kirjeldada tarne- ja tagastamispoliitikaid, vastata korduma kippuvatele küsimustele või lisada sisu osale „Tutvustus”.</span><span class="sxs-lookup"><span data-stu-id="d90d2-115">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="d90d2-116">Lisada toote üksikasjade lehele kohandatud sõnumeid.</span><span class="sxs-lookup"><span data-stu-id="d90d2-116">To add custom messages on a product details page.</span></span> <span data-ttu-id="d90d2-117">(nt „Üle 50 euro maksvad tellimused tarnitakse tasuta”).</span><span class="sxs-lookup"><span data-stu-id="d90d2-117">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="d90d2-118">Lahtiütluste ja kontaktandmete jaoks toote üksikasjade lehtedel, ostukorvi lehtedel, maksmise lehtedel ja teistel lehtedel (nt „Tarnimisele ja tagastustele kehtivad poe eeskirjad”).</span><span class="sxs-lookup"><span data-stu-id="d90d2-118">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="content-rich-block-module-properties"></a><span data-ttu-id="d90d2-119">Sisurikka plokimooduli atribuutide sisu</span><span class="sxs-lookup"><span data-stu-id="d90d2-119">Content rich block module properties</span></span>

| <span data-ttu-id="d90d2-120">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="d90d2-120">Property name</span></span>     | <span data-ttu-id="d90d2-121">Väärtus</span><span class="sxs-lookup"><span data-stu-id="d90d2-121">Value</span></span>                                 | <span data-ttu-id="d90d2-122">Atribuut</span><span class="sxs-lookup"><span data-stu-id="d90d2-122">Property</span></span> |
|-------------------|---------------------------------------|----------|
| <span data-ttu-id="d90d2-123">Veergude arv</span><span class="sxs-lookup"><span data-stu-id="d90d2-123">Number of columns</span></span> | <span data-ttu-id="d90d2-124">Number vahemikus **1** kuni **4**</span><span class="sxs-lookup"><span data-stu-id="d90d2-124">A number from **1** through **4**</span></span>     | <span data-ttu-id="d90d2-125">Sisurikka ploki veergude arv.</span><span class="sxs-lookup"><span data-stu-id="d90d2-125">The number of columns in the content rich block.</span></span> <span data-ttu-id="d90d2-126">Seal võib olla kuni neli veergu.</span><span class="sxs-lookup"><span data-stu-id="d90d2-126">There can be up to four columns.</span></span> |
| <span data-ttu-id="d90d2-127">Laius</span><span class="sxs-lookup"><span data-stu-id="d90d2-127">Width</span></span>             | <span data-ttu-id="d90d2-128">**Täida konteiner** või **Täida ekraan**</span><span class="sxs-lookup"><span data-stu-id="d90d2-128">**Fill container** or **Fill screen**</span></span> | <span data-ttu-id="d90d2-129">Kui väärtuseks on seatud **Täida konteiner**, on konteineris olevad kaubad piiratud konteineri laiusega.</span><span class="sxs-lookup"><span data-stu-id="d90d2-129">If the value is set to **Fill container**, the items inside the container are restricted to the width of the container.</span></span> <span data-ttu-id="d90d2-130">Kui väärtuseks on seatud **Täida ekraan**, ei ole kaubad konteineri laiusega piiratud, vaid võivad minna täisekraani režiimi.</span><span class="sxs-lookup"><span data-stu-id="d90d2-130">If the value is set to **Fill screen**, the items aren't restricted to the container width but can go into full-screen mode.</span></span> <span data-ttu-id="d90d2-131">Soovitud paigutuse saavutamiseks saate väärtust muuta.</span><span class="sxs-lookup"><span data-stu-id="d90d2-131">You can change the value to achieve the desired layout.</span></span> |

## <a name="content-rich-block-item-module-properties"></a><span data-ttu-id="d90d2-132">Sisurikka ploki kauba mooduli atribuutide sisu</span><span class="sxs-lookup"><span data-stu-id="d90d2-132">Content rich block item module properties</span></span>

| <span data-ttu-id="d90d2-133">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="d90d2-133">Property name</span></span> | <span data-ttu-id="d90d2-134">Väärtus</span><span class="sxs-lookup"><span data-stu-id="d90d2-134">Value</span></span>          | <span data-ttu-id="d90d2-135">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d90d2-135">Description</span></span> |
|---------------|----------------|-------------|
| <span data-ttu-id="d90d2-136">Lõik</span><span class="sxs-lookup"><span data-stu-id="d90d2-136">Paragraph</span></span>     | <span data-ttu-id="d90d2-137">Lõigu tekst</span><span class="sxs-lookup"><span data-stu-id="d90d2-137">Paragraph text</span></span> | <span data-ttu-id="d90d2-138">Iga sisurikka bloki kaupa saatev tekst.</span><span class="sxs-lookup"><span data-stu-id="d90d2-138">The text that accompanies each content rich block item.</span></span> <span data-ttu-id="d90d2-139">Toetatud on mõned põhilised RTF-i võimalused, nagu paks, allajoonitud ja kursiivis tekst.</span><span class="sxs-lookup"><span data-stu-id="d90d2-139">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |

## <a name="add-a-content-rich-block-module-to-a-page"></a><span data-ttu-id="d90d2-140">Sisurikka plokimooduli lehele lisamine</span><span class="sxs-lookup"><span data-stu-id="d90d2-140">Add a content rich block module to a page</span></span>

<span data-ttu-id="d90d2-141">Uuele lehele sisurikka plokimooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d90d2-141">To add a content rich block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d90d2-142">Looge lehe mall nimega **Sisu mall**.</span><span class="sxs-lookup"><span data-stu-id="d90d2-142">Create a page template that is named **Content template**.</span></span>
1. <span data-ttu-id="d90d2-143">Lisage vaikelehe pessa **Peamine** sisurikas plokimoodul.</span><span class="sxs-lookup"><span data-stu-id="d90d2-143">In the **Main** slot of the default page, add a content rich block module.</span></span>
1. <span data-ttu-id="d90d2-144">Registreerige mall ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="d90d2-144">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="d90d2-145">Kasutage äsja loodud sisu malli, et luua leht, mille nimi on **Sisu leht**.</span><span class="sxs-lookup"><span data-stu-id="d90d2-145">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="d90d2-146">Lisage uue lehe pessa **Peamine** sisurikas plokimoodul.</span><span class="sxs-lookup"><span data-stu-id="d90d2-146">In the **Main** slot of the new page, add a content rich block module.</span></span>
1. <span data-ttu-id="d90d2-147">Määrake sisurikka plokimooduli atribuutides veergude arvuks **2**.</span><span class="sxs-lookup"><span data-stu-id="d90d2-147">In the properties of the content rich block module, set number of columns to **2**.</span></span>
1. <span data-ttu-id="d90d2-148">Valige sisurikka plokimooduli sisus suvand **Lisa moodul** ja lisage sisurikka ploki kauba sisu (näiteks **kaup1**).</span><span class="sxs-lookup"><span data-stu-id="d90d2-148">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item1**).</span></span>
1. <span data-ttu-id="d90d2-149">Lisage uues sisurikkas ploki üksuses uus sisu ja paragrahvi tekst.</span><span class="sxs-lookup"><span data-stu-id="d90d2-149">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="d90d2-150">Valige sisurikka plokimooduli sisus suvand **Lisa moodul** ja lisage sisurikka ploki kauba sisu (näiteks **kaup2**).</span><span class="sxs-lookup"><span data-stu-id="d90d2-150">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item2**).</span></span>
1. <span data-ttu-id="d90d2-151">Lisage uues sisurikkas ploki üksuses uus sisu ja paragrahvi tekst.</span><span class="sxs-lookup"><span data-stu-id="d90d2-151">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="d90d2-152">Salvestage leht ja kuvage muudatuste eelvaade.</span><span class="sxs-lookup"><span data-stu-id="d90d2-152">Save the page, and preview the changes.</span></span> <span data-ttu-id="d90d2-153">Peaksite nägema kahte rikasteksti plokki kahe veeruga vaates.</span><span class="sxs-lookup"><span data-stu-id="d90d2-153">You should see two rich text blocks in a two-column view.</span></span>
1. <span data-ttu-id="d90d2-154">Registreerige leht ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="d90d2-154">Check in the page, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="d90d2-155">Kui lisate kolmanda rikasteksti ploki üksuse, virnastatakse see kahe eelnevalt lisatud üksuse alla.</span><span class="sxs-lookup"><span data-stu-id="d90d2-155">If you add a third content rich block item, it will be stacked below the two items that you previously added.</span></span> <span data-ttu-id="d90d2-156">Muutes veergude ja konteineris olevate üksuste arvu, võite saavutada tekstisisu erinevad paigutused.</span><span class="sxs-lookup"><span data-stu-id="d90d2-156">By changing the number of columns and items in the container, you can achieve different layouts for textual content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d90d2-157">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d90d2-157">Additional resources</span></span>

[<span data-ttu-id="d90d2-158">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="d90d2-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d90d2-159">Teatise moodul</span><span class="sxs-lookup"><span data-stu-id="d90d2-159">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="d90d2-160">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="d90d2-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="d90d2-161">Sisupaigutuse moodul</span><span class="sxs-lookup"><span data-stu-id="d90d2-161">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="d90d2-162">Funktsioonimoodul</span><span class="sxs-lookup"><span data-stu-id="d90d2-162">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="d90d2-163">Pannoomoodul</span><span class="sxs-lookup"><span data-stu-id="d90d2-163">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="d90d2-164">Videopleieri moodul</span><span class="sxs-lookup"><span data-stu-id="d90d2-164">Video player module</span></span>](add-video-player.md)

