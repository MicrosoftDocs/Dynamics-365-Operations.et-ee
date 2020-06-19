---
title: Tekstiploki moodul
description: See teema hõlmab tekstiploki mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 93ad09a05d188a30b099b9a44c35e15839be80a7
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411131"
---
# <a name="text-block-module"></a><span data-ttu-id="526aa-103">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="526aa-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="526aa-104">See teema hõlmab tekstiploki mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="526aa-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="526aa-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="526aa-105">Overview</span></span>

<span data-ttu-id="526aa-106">Tekstiploki moodul on moodul, mida kasutatakse tekstilise sisu lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="526aa-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="526aa-107">See sisu võib olla kas teavitav või kampaaniaga seotud.</span><span class="sxs-lookup"><span data-stu-id="526aa-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="526aa-108">Tekstiploki moodulid põhinevad sisuhaldussüsteemi (CMS) andmetel ja neid saab panna igale lehele.</span><span class="sxs-lookup"><span data-stu-id="526aa-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="526aa-109">Need on eraldiseisvad moodulid, mis ei sõltu lehekülje kontekstist ega ühestki teisest moodulist.</span><span class="sxs-lookup"><span data-stu-id="526aa-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="526aa-110">E-kaubanduse tekstiploki moodulite näited</span><span class="sxs-lookup"><span data-stu-id="526aa-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="526aa-111">Tekstiploki mooduleid saab kasutada järgmistel viisidel.</span><span class="sxs-lookup"><span data-stu-id="526aa-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="526aa-112">Toote üksikasjade lehel toote funktsioonide tutvustamiseks.</span><span class="sxs-lookup"><span data-stu-id="526aa-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="526aa-113">Teavitamise eesmärgil mis tahes lehel.</span><span class="sxs-lookup"><span data-stu-id="526aa-113">For informational purposes on any page.</span></span> <span data-ttu-id="526aa-114">Näiteks võivad need selgitada püsikliendiprogrammide eeliseid, kirjeldada tarne- ja tagastamispoliitikaid, vastata korduma kippuvatele küsimustele või lisada sisu osale „Tutvustus”.</span><span class="sxs-lookup"><span data-stu-id="526aa-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="526aa-115">Lisada toote üksikasjade lehele kohandatud sõnumeid.</span><span class="sxs-lookup"><span data-stu-id="526aa-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="526aa-116">(nt „Üle 50 euro maksvad tellimused tarnitakse tasuta”).</span><span class="sxs-lookup"><span data-stu-id="526aa-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="526aa-117">Lahtiütluste ja kontaktandmete jaoks toote üksikasjade lehtedel, ostukorvi lehtedel, maksmise lehtedel ja teistel lehtedel (nt „Tarnimisele ja tagastustele kehtivad poe eeskirjad”).</span><span class="sxs-lookup"><span data-stu-id="526aa-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="526aa-118">Järgmisel pildil on näide tekstiploki moodulist, mida kasutatakse avalehel.</span><span class="sxs-lookup"><span data-stu-id="526aa-118">The following image shows an example of a text block module that is used on a home page.</span></span>

![Tekstiploki mooduli näide](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="526aa-120">Tekstiploki mooduli omadused</span><span class="sxs-lookup"><span data-stu-id="526aa-120">Text block module properties</span></span>

| <span data-ttu-id="526aa-121">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="526aa-121">Property name</span></span>     | <span data-ttu-id="526aa-122">Väärtus</span><span class="sxs-lookup"><span data-stu-id="526aa-122">Value</span></span>                                            | <span data-ttu-id="526aa-123">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="526aa-123">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="526aa-124">Rikastekst</span><span class="sxs-lookup"><span data-stu-id="526aa-124">Rich text</span></span>         | <span data-ttu-id="526aa-125">Rikastekst</span><span class="sxs-lookup"><span data-stu-id="526aa-125">Rich text</span></span>                                        | <span data-ttu-id="526aa-126">Lõigu tekst.</span><span class="sxs-lookup"><span data-stu-id="526aa-126">Paragraph text.</span></span> <span data-ttu-id="526aa-127">Toetatud on mõned põhilised RTF-i võimalused, nagu paks, allajoonitud ja kursiivis tekst.</span><span class="sxs-lookup"><span data-stu-id="526aa-127">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="526aa-128">Kohandatud klassinimi</span><span class="sxs-lookup"><span data-stu-id="526aa-128">Custom class name</span></span> | <span data-ttu-id="526aa-129">Kaskaadlaadistiku (CSS) klassi nimi</span><span class="sxs-lookup"><span data-stu-id="526aa-129">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="526aa-130">Kohandatud CSS'i klassi nimi, mille arendaja annab selle mooduli vormindamiseks.</span><span class="sxs-lookup"><span data-stu-id="526aa-130">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="526aa-131">Klassi nimi tuleks määratleda kujundusepaketis.</span><span class="sxs-lookup"><span data-stu-id="526aa-131">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="526aa-132">Fondi suurus</span><span class="sxs-lookup"><span data-stu-id="526aa-132">Font size</span></span>         | <span data-ttu-id="526aa-133">**Väike**, **Keskmine**, **Suur** või **Väga suur**</span><span class="sxs-lookup"><span data-stu-id="526aa-133">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="526aa-134">Sisu fondi suurus.</span><span class="sxs-lookup"><span data-stu-id="526aa-134">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="526aa-135">Tekstiploki mooduli lehele lisamine</span><span class="sxs-lookup"><span data-stu-id="526aa-135">Add a text block module to a page</span></span>

<span data-ttu-id="526aa-136">Uuele lehele tekstiploki mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="526aa-136">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="526aa-137">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="526aa-137">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="526aa-138">Sisestage dialoogiboksi **Uus mall** jaotises **Malli nimi** **Sisumall**.</span><span class="sxs-lookup"><span data-stu-id="526aa-138">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="526aa-139">Valige pesas **Keha** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="526aa-139">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="526aa-140">Valige dialoogiboksis **Lisa moodul** moodul **Vaikeleht** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="526aa-140">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="526aa-141">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="526aa-141">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="526aa-142">Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="526aa-142">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="526aa-143">Valige dialoogiaknas **Vali mall** **Sisumall**.</span><span class="sxs-lookup"><span data-stu-id="526aa-143">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="526aa-144">Sisestage jaotises **Lehe nimi** väärtus **Sisuleht** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="526aa-144">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="526aa-145">Uue lehe pesas **Peamine** valige kolmikpunkt (**...**) ja seejärel valige suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="526aa-145">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="526aa-146">Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="526aa-146">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="526aa-147">Seadistage konteineri mooduli paanil atribuut **Laius** väärtusele **Täida konteiner**.</span><span class="sxs-lookup"><span data-stu-id="526aa-147">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="526aa-148">Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="526aa-148">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="526aa-149">Valige dialoogiboksis **Lisa moodul** moodul **Tekstiplokk** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="526aa-149">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="526aa-150">Lisage tekst tekstiploki mooduli atribuutide paani väljale **Rikastekst**.</span><span class="sxs-lookup"><span data-stu-id="526aa-150">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="526aa-151">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="526aa-151">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="526aa-152">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="526aa-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="526aa-153">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="526aa-153">Additional resources</span></span>

[<span data-ttu-id="526aa-154">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="526aa-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="526aa-155">Kampaania ribareklaami moodul</span><span class="sxs-lookup"><span data-stu-id="526aa-155">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="526aa-156">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="526aa-156">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="526aa-157">Sisuploki moodul</span><span class="sxs-lookup"><span data-stu-id="526aa-157">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="526aa-158">Videopleierimoodul</span><span class="sxs-lookup"><span data-stu-id="526aa-158">Video player module</span></span>](add-video-player.md)

