---
title: Tekstiploki moodul
description: See teema hõlmab tekstiploki mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025593"
---
# <a name="text-block-module"></a><span data-ttu-id="473c9-103">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="473c9-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="473c9-104">See teema hõlmab tekstiploki mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="473c9-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="473c9-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="473c9-105">Overview</span></span>

<span data-ttu-id="473c9-106">Tekstiploki moodul on moodul, mida kasutatakse tekstilise sisu lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="473c9-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="473c9-107">See sisu võib olla kas teavitav või kampaaniaga seotud.</span><span class="sxs-lookup"><span data-stu-id="473c9-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="473c9-108">Tekstiploki moodulid põhinevad sisuhaldussüsteemi (CMS) andmetel ja neid saab panna igale lehele.</span><span class="sxs-lookup"><span data-stu-id="473c9-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="473c9-109">Need on eraldiseisvad moodulid, mis ei sõltu lehekülje kontekstist ega ühestki teisest moodulist.</span><span class="sxs-lookup"><span data-stu-id="473c9-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="473c9-110">E-kaubanduse tekstiploki moodulite näited</span><span class="sxs-lookup"><span data-stu-id="473c9-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="473c9-111">Tekstiploki mooduleid saab kasutada järgmistel viisidel.</span><span class="sxs-lookup"><span data-stu-id="473c9-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="473c9-112">Toote üksikasjade lehel toote funktsioonide tutvustamiseks.</span><span class="sxs-lookup"><span data-stu-id="473c9-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="473c9-113">Teavitamise eesmärgil mis tahes lehel.</span><span class="sxs-lookup"><span data-stu-id="473c9-113">For informational purposes on any page.</span></span> <span data-ttu-id="473c9-114">Näiteks võivad need selgitada püsikliendiprogrammide eeliseid, kirjeldada tarne- ja tagastamispoliitikaid, vastata korduma kippuvatele küsimustele või lisada sisu osale „Tutvustus”.</span><span class="sxs-lookup"><span data-stu-id="473c9-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="473c9-115">Lisada toote üksikasjade lehele kohandatud sõnumeid.</span><span class="sxs-lookup"><span data-stu-id="473c9-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="473c9-116">(nt „Üle 50 euro maksvad tellimused tarnitakse tasuta”).</span><span class="sxs-lookup"><span data-stu-id="473c9-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="473c9-117">Lahtiütluste ja kontaktandmete jaoks toote üksikasjade lehtedel, ostukorvi lehtedel, maksmise lehtedel ja teistel lehtedel (nt „Tarnimisele ja tagastustele kehtivad poe eeskirjad”).</span><span class="sxs-lookup"><span data-stu-id="473c9-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="text-block-module-properties"></a><span data-ttu-id="473c9-118">Tekstiploki mooduli omadused</span><span class="sxs-lookup"><span data-stu-id="473c9-118">Text block module properties</span></span>

| <span data-ttu-id="473c9-119">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="473c9-119">Property name</span></span>     | <span data-ttu-id="473c9-120">Value</span><span class="sxs-lookup"><span data-stu-id="473c9-120">Value</span></span>                                            | <span data-ttu-id="473c9-121">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="473c9-121">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="473c9-122">Rikastekst</span><span class="sxs-lookup"><span data-stu-id="473c9-122">Rich text</span></span>         | <span data-ttu-id="473c9-123">Rikastekst</span><span class="sxs-lookup"><span data-stu-id="473c9-123">Rich text</span></span>                                        | <span data-ttu-id="473c9-124">Lõigu tekst.</span><span class="sxs-lookup"><span data-stu-id="473c9-124">Paragraph text.</span></span> <span data-ttu-id="473c9-125">Toetatud on mõned põhilised RTF-i võimalused, nagu paks, allajoonitud ja kursiivis tekst.</span><span class="sxs-lookup"><span data-stu-id="473c9-125">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="473c9-126">Kohandatud klassinimi</span><span class="sxs-lookup"><span data-stu-id="473c9-126">Custom class name</span></span> | <span data-ttu-id="473c9-127">Kaskaadlaadistiku (CSS) klassi nimi</span><span class="sxs-lookup"><span data-stu-id="473c9-127">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="473c9-128">Kohandatud CSS'i klassi nimi, mille arendaja annab selle mooduli vormindamiseks.</span><span class="sxs-lookup"><span data-stu-id="473c9-128">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="473c9-129">Klassi nimi tuleks määratleda kujundusepaketis.</span><span class="sxs-lookup"><span data-stu-id="473c9-129">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="473c9-130">Fondi suurus</span><span class="sxs-lookup"><span data-stu-id="473c9-130">Font size</span></span>         | <span data-ttu-id="473c9-131">**Väike**, **Keskmine**, **Suur** või **Väga suur**</span><span class="sxs-lookup"><span data-stu-id="473c9-131">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="473c9-132">Sisu fondi suurus.</span><span class="sxs-lookup"><span data-stu-id="473c9-132">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="473c9-133">Tekstiploki mooduli lehele lisamine</span><span class="sxs-lookup"><span data-stu-id="473c9-133">Add a text block module to a page</span></span>

<span data-ttu-id="473c9-134">Uuele lehele tekstiploki mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="473c9-134">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="473c9-135">Looge lehe mall nimega **Sisu mall**.</span><span class="sxs-lookup"><span data-stu-id="473c9-135">Create a page template that is named **Content template**.</span></span> 
1. <span data-ttu-id="473c9-136">Lisage pesasse **Kehatekst** moodul **Vaikeleht**.</span><span class="sxs-lookup"><span data-stu-id="473c9-136">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="473c9-137">Viige lõpuni malli redigeerimine ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="473c9-137">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="473c9-138">Kasutage äsja loodud sisu malli, et luua leht, mille nimi on **Sisu leht**.</span><span class="sxs-lookup"><span data-stu-id="473c9-138">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="473c9-139">Lisage uue lehe pessa **Peamine** konteinermoodul.</span><span class="sxs-lookup"><span data-stu-id="473c9-139">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="473c9-140">Seadistage konteineri mooduli paanil atribuut **Laius** väärtusele **Täida konteiner**.</span><span class="sxs-lookup"><span data-stu-id="473c9-140">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="473c9-141">Lisage konteineri moodulile tekstiploki moodul.</span><span class="sxs-lookup"><span data-stu-id="473c9-141">Add a text block module to the container module.</span></span> 
1. <span data-ttu-id="473c9-142">Lisage tekst tekstiploki mooduli atribuutide paani väljale **Rikastekst**.</span><span class="sxs-lookup"><span data-stu-id="473c9-142">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="473c9-143">Viige lõpuni lehe redigeerimine ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="473c9-143">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="473c9-144">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="473c9-144">Additional resources</span></span>

[<span data-ttu-id="473c9-145">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="473c9-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="473c9-146">Reklaambänneri moodul</span><span class="sxs-lookup"><span data-stu-id="473c9-146">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="473c9-147">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="473c9-147">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="473c9-148">Sisuploki moodul</span><span class="sxs-lookup"><span data-stu-id="473c9-148">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="473c9-149">Videopleierimoodul</span><span class="sxs-lookup"><span data-stu-id="473c9-149">Video player module</span></span>](add-video-player.md)

