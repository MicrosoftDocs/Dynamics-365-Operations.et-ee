---
title: Tekstiploki moodul
description: See teema hõlmab tekstiploki mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7dbeb8785641960cc2680335436aea10775759d3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797763"
---
# <a name="text-block-module"></a><span data-ttu-id="2db31-103">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="2db31-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2db31-104">See teema hõlmab tekstiploki mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="2db31-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2db31-105">Tekstiploki moodul on moodul, mida kasutatakse tekstilise sisu lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="2db31-105">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="2db31-106">See sisu võib olla kas teavitav või kampaaniaga seotud.</span><span class="sxs-lookup"><span data-stu-id="2db31-106">This content can be informational or promotional.</span></span>

<span data-ttu-id="2db31-107">Tekstiploki moodulid põhinevad sisuhaldussüsteemi (CMS) andmetel ja neid saab panna igale lehele.</span><span class="sxs-lookup"><span data-stu-id="2db31-107">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="2db31-108">Need on eraldiseisvad moodulid, mis ei sõltu lehekülje kontekstist ega ühestki teisest moodulist.</span><span class="sxs-lookup"><span data-stu-id="2db31-108">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="2db31-109">E-kaubanduse tekstiploki moodulite näited</span><span class="sxs-lookup"><span data-stu-id="2db31-109">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="2db31-110">Tekstiploki mooduleid saab kasutada järgmistel viisidel.</span><span class="sxs-lookup"><span data-stu-id="2db31-110">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="2db31-111">Toote üksikasjade lehel toote funktsioonide tutvustamiseks.</span><span class="sxs-lookup"><span data-stu-id="2db31-111">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="2db31-112">Teavitamise eesmärgil mis tahes lehel.</span><span class="sxs-lookup"><span data-stu-id="2db31-112">For informational purposes on any page.</span></span> <span data-ttu-id="2db31-113">Näiteks võivad need selgitada püsikliendiprogrammide eeliseid, kirjeldada tarne- ja tagastamispoliitikaid, vastata korduma kippuvatele küsimustele või lisada sisu osale „Tutvustus”.</span><span class="sxs-lookup"><span data-stu-id="2db31-113">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="2db31-114">Lisada toote üksikasjade lehele kohandatud sõnumeid.</span><span class="sxs-lookup"><span data-stu-id="2db31-114">To add custom messages on a product details page.</span></span> <span data-ttu-id="2db31-115">(nt „Üle 50 euro maksvad tellimused tarnitakse tasuta”).</span><span class="sxs-lookup"><span data-stu-id="2db31-115">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="2db31-116">Lahtiütluste ja kontaktandmete jaoks toote üksikasjade lehtedel, ostukorvi lehtedel, maksmise lehtedel ja teistel lehtedel (nt „Tarnimisele ja tagastustele kehtivad poe eeskirjad”).</span><span class="sxs-lookup"><span data-stu-id="2db31-116">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="2db31-117">Järgmisel pildil on näide tekstiploki moodulist, mida kasutatakse avalehel.</span><span class="sxs-lookup"><span data-stu-id="2db31-117">The following image shows an example of a text block module that is used on a home page.</span></span>

![Tekstiploki mooduli näide](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="2db31-119">Tekstiploki mooduli omadused</span><span class="sxs-lookup"><span data-stu-id="2db31-119">Text block module properties</span></span>

| <span data-ttu-id="2db31-120">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="2db31-120">Property name</span></span>     | <span data-ttu-id="2db31-121">Väärtus</span><span class="sxs-lookup"><span data-stu-id="2db31-121">Value</span></span>                                            | <span data-ttu-id="2db31-122">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2db31-122">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="2db31-123">Rikastekst</span><span class="sxs-lookup"><span data-stu-id="2db31-123">Rich text</span></span>         | <span data-ttu-id="2db31-124">Rikastekst</span><span class="sxs-lookup"><span data-stu-id="2db31-124">Rich text</span></span>                                        | <span data-ttu-id="2db31-125">Lõigu tekst.</span><span class="sxs-lookup"><span data-stu-id="2db31-125">Paragraph text.</span></span> <span data-ttu-id="2db31-126">Toetatud on mõned põhilised RTF-i võimalused, nagu paks, allajoonitud ja kursiivis tekst.</span><span class="sxs-lookup"><span data-stu-id="2db31-126">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="2db31-127">Kohandatud klassinimi</span><span class="sxs-lookup"><span data-stu-id="2db31-127">Custom class name</span></span> | <span data-ttu-id="2db31-128">Kaskaadlaadistiku (CSS) klassi nimi</span><span class="sxs-lookup"><span data-stu-id="2db31-128">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="2db31-129">Kohandatud CSS-i klassi nimi, mille arendaja annab selle mooduli vormindamiseks.</span><span class="sxs-lookup"><span data-stu-id="2db31-129">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="2db31-130">Klassi nimi tuleks määratleda kujundusepaketis.</span><span class="sxs-lookup"><span data-stu-id="2db31-130">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="2db31-131">Fondi suurus</span><span class="sxs-lookup"><span data-stu-id="2db31-131">Font size</span></span>         | <span data-ttu-id="2db31-132">**Väike**, **Keskmine**, **Suur** või **Väga suur**</span><span class="sxs-lookup"><span data-stu-id="2db31-132">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="2db31-133">Sisu fondi suurus.</span><span class="sxs-lookup"><span data-stu-id="2db31-133">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="2db31-134">Tekstiploki mooduli lehele lisamine</span><span class="sxs-lookup"><span data-stu-id="2db31-134">Add a text block module to a page</span></span>

<span data-ttu-id="2db31-135">Uuele lehele tekstiploki mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2db31-135">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="2db31-136">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2db31-136">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="2db31-137">Sisestage dialoogiboksi **Uus mall** jaotises **Malli nimi** **Sisumall**.</span><span class="sxs-lookup"><span data-stu-id="2db31-137">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="2db31-138">Valige pesas **Keha** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="2db31-138">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2db31-139">Valige dialoogiboksis **Lisa moodul** moodul **Vaikeleht** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="2db31-139">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2db31-140">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="2db31-140">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="2db31-141">Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2db31-141">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="2db31-142">Valige dialoogiaknas **Vali mall** **Sisumall**.</span><span class="sxs-lookup"><span data-stu-id="2db31-142">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="2db31-143">Sisestage jaotises **Lehe nimi** väärtus **Sisuleht** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="2db31-143">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="2db31-144">Uue lehe pesas **Peamine** valige kolmikpunkt (**...**) ja seejärel valige suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="2db31-144">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2db31-145">Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="2db31-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2db31-146">Seadistage konteineri mooduli paanil atribuut **Laius** väärtusele **Täida konteiner**.</span><span class="sxs-lookup"><span data-stu-id="2db31-146">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="2db31-147">Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="2db31-147">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2db31-148">Valige dialoogiboksis **Lisa moodul** moodul **Tekstiplokk** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="2db31-148">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="2db31-149">Lisage tekst tekstiploki mooduli atribuutide paani väljale **Rikastekst**.</span><span class="sxs-lookup"><span data-stu-id="2db31-149">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="2db31-150">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="2db31-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="2db31-151">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="2db31-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2db31-152">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2db31-152">Additional resources</span></span>

[<span data-ttu-id="2db31-153">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="2db31-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2db31-154">Kampaania ribareklaami moodul</span><span class="sxs-lookup"><span data-stu-id="2db31-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="2db31-155">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="2db31-155">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="2db31-156">Sisuploki moodul</span><span class="sxs-lookup"><span data-stu-id="2db31-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="2db31-157">Videopleierimoodul</span><span class="sxs-lookup"><span data-stu-id="2db31-157">Video player module</span></span>](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]