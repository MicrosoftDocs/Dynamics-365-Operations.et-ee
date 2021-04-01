---
title: Kategooria sihtlehe rikastamine
description: See teema käsitleb kategoorialehtede rikastamist rakenduses Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fbcf6ec60723b726e022b4e17bbde4c903e5cb57
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238771"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="e8b2e-103">Kategooria sihtlehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="e8b2e-103">Enrich a category landing page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e8b2e-104">See teema käsitleb kategoorialehtede rikastamist rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e8b2e-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="e8b2e-105">Overview</span></span>

<span data-ttu-id="e8b2e-106">Commerce pakub kategooria vaikesihtlehe, mida kasutatakse kategooria andmete kuvamise ajal.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="e8b2e-107">Kategooria vaikeleht sisaldab nõutud elemente, nagu piiritlusatribuudid, kategoriseeritud tootepaigutus, sortimissuvandid, valikute kokkuvõte ja lehejaotuse juhtelemendid.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="e8b2e-108">Samas võite kategooria vaikelehe asemel tahta kasutada nn rikastatud kategooria sihtlehte, kus on rohkem sisu ja palju täpsemad elemendid.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="e8b2e-109">Tüüpiline rikastamine võib hõlmata kategooria lehele kategooriapõhise turundussisu lisamist.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="e8b2e-110">See sisu võib sisaldada kategooriaüleseid tootepaigutusi kaasamüügi eesmärgil, toimetusloendeid, pilte, videoid ja muud teksti.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="e8b2e-111">Võite muuta kas kategooria vaikelehte või määratleda konkreetse kategooria jaoks erineva kategoorialehe.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Rikastatud kategooria sihtleht](./media/CategoryLandingPages.png)

<span data-ttu-id="e8b2e-113">Commerce'i saidiehitajas sisaldab leht **Tooted** loendit kategooriatest, mis on pärit saidile määratud kanalist.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-113">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="e8b2e-114">Kui kategooria lehe jaoks on valitud olek **Rikastatud**, on see kategooria leht rikastatud.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="e8b2e-115">Muul juhul kasutatakse kategooria jaoks kategooria vaikelehte ja sisu.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="e8b2e-116">Võite kuvada kategooria jaoks nii rikastatud kui ka mitte rikastatud kategooria lehtede eelvaate, valides kategooria nime.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="e8b2e-117">Kategooria lehe rikastamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="e8b2e-118">Lehel **Tooted** valige kategooria nimi, mille jaoks soovite kategooria lehte rikastada.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-118">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="e8b2e-119">Lehe redaktoris avatakse valitud kategooria jaoks kategooria vaikeleht.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="e8b2e-120">Valige suvand **Kategooria lehe rikastamine**.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="e8b2e-121">Valige rikastatud kategooria lehele mall.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="e8b2e-122">Kui teete ainult väikeseid muudatusi, saate valida kategooria vaikelehe.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="e8b2e-123">Teise võimalusena saate valida konkreetse kategooria lehe malli.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="e8b2e-124">Malli valimisel avatakse lehe redaktor ja valitud malli kasutatakse valitud kategooria jaoks uue kategooria lehe loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="e8b2e-125">Leht registreeritakse teie jaoks välja ja saate nüüd oma muudatused teha.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="e8b2e-126">Kategooria täpsustuse andmeid kasutavad moodulid kasutavad teie valitud kategooria andmeid.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-126">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="e8b2e-127">Valitud malli sätted määravad muudatused, mida saate teha.</span><span class="sxs-lookup"><span data-stu-id="e8b2e-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8b2e-128">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e8b2e-128">Additional resources</span></span>

[<span data-ttu-id="e8b2e-129">Olemasoleva saidilehe muutmine</span><span class="sxs-lookup"><span data-stu-id="e8b2e-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="e8b2e-130">Uue saidilehe lisamine</span><span class="sxs-lookup"><span data-stu-id="e8b2e-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="e8b2e-131">Lehepaigutuste valimine</span><span class="sxs-lookup"><span data-stu-id="e8b2e-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="e8b2e-132">SEO metaandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="e8b2e-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="e8b2e-133">Lehe salvestamine, eelvaade ja avaldamine</span><span class="sxs-lookup"><span data-stu-id="e8b2e-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="e8b2e-134">Tootelehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="e8b2e-134">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="e8b2e-135">Lehe sisu hõlbustusfunktsioonide kinnitamine</span><span class="sxs-lookup"><span data-stu-id="e8b2e-135">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="e8b2e-136">Dünaamiliste e-kaubanduse lehtede loomine URL-parameetrite põhjal</span><span class="sxs-lookup"><span data-stu-id="e8b2e-136">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]