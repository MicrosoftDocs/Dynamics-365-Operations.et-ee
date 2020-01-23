---
title: Kategooria sihtlehe rikastamine
description: See teema käsitleb kategoorialehtede rikastamist rakenduses Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4ab152dff0925f9c816419083577b5272ac813be
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945775"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="b5ba1-103">Kategooria sihtlehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="b5ba1-103">Enrich a category landing page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b5ba1-104">See teema käsitleb kategoorialehtede rikastamist rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b5ba1-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="b5ba1-105">Overview</span></span>

<span data-ttu-id="b5ba1-106">Commerce pakub kategooria vaikesihtlehe, mida kasutatakse kategooria andmete kuvamise ajal.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="b5ba1-107">Kategooria vaikeleht sisaldab nõutud elemente, nagu piiritlusatribuudid, kategoriseeritud tootepaigutus, sortimissuvandid, valikute kokkuvõte ja lehejaotuse juhtelemendid.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="b5ba1-108">Samas võite kategooria vaikelehe asemel tahta kasutada nn rikastatud kategooria sihtlehte, kus on rohkem sisu ja palju täpsemad elemendid.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="b5ba1-109">Tüüpiline rikastamine võib hõlmata kategooria lehele kategooriapõhise turundussisu lisamist.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="b5ba1-110">See sisu võib sisaldada kategooriaüleseid tootepaigutusi kaasamüügi eesmärgil, toimetusloendeid, pilte, videoid ja muud teksti.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="b5ba1-111">Võite muuta kas kategooria vaikelehte või määratleda konkreetse kategooria jaoks erineva kategoorialehe.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Rikastatud kategooria sihtleht](./media/CategoryLandingPages.png)

<span data-ttu-id="b5ba1-113">Autorluse tööriistas sisaldab leht **Toode** loendit kategooriatest, mis on pärit saidile määratud kanalist.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-113">In the authoring tool, the **Product** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="b5ba1-114">Kui kategooria lehe jaoks on valitud olek **Rikastatud**, on see kategooria leht rikastatud.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="b5ba1-115">Muul juhul kasutatakse kategooria jaoks kategooria vaikelehte ja sisu.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="b5ba1-116">Võite kuvada kategooria jaoks nii rikastatud kui ka mitte rikastatud kategooria lehtede eelvaate, valides kategooria nime.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="b5ba1-117">Kategooria lehe rikastamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="b5ba1-118">Lehel **Tooted** valige kategooria nimi, mille jaoks soovite kategooria lehte rikastada.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-118">On the **Products** page, select the name of the category that you want to enrich the category page for.</span></span> <span data-ttu-id="b5ba1-119">Lehe redaktoris avatakse valitud kategooria jaoks kategooria vaikeleht.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="b5ba1-120">Valige suvand **Kategooria lehe rikastamine**.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="b5ba1-121">Valige rikastatud kategooria lehele mall.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="b5ba1-122">Kui teete ainult väikeseid muudatusi, saate valida kategooria vaikelehe.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="b5ba1-123">Teise võimalusena saate valida konkreetse kategooria lehe malli.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="b5ba1-124">Malli valimisel avatakse lehe redaktor ja valitud malli kasutatakse valitud kategooria jaoks uue kategooria lehe loomiseks.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="b5ba1-125">Leht registreeritakse teie jaoks välja ja saate nüüd oma muudatused teha.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="b5ba1-126">Kategooria täpsustuse andmeid kasutavad moodulid kasutavad teie valitud kategooria andmeid.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-126">Modules that use category specification data use the data from your selected category.</span></span>
>
> <span data-ttu-id="b5ba1-127">Valitud malli sätted määravad muudatused, mida saate teha.</span><span class="sxs-lookup"><span data-stu-id="b5ba1-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5ba1-128">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b5ba1-128">Additional resources</span></span>

[<span data-ttu-id="b5ba1-129">Olemasoleva saidilehe muutmine</span><span class="sxs-lookup"><span data-stu-id="b5ba1-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="b5ba1-130">Uue saidilehe lisamine</span><span class="sxs-lookup"><span data-stu-id="b5ba1-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="b5ba1-131">Lehepaigutuste valimine</span><span class="sxs-lookup"><span data-stu-id="b5ba1-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="b5ba1-132">SEO metaandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="b5ba1-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="b5ba1-133">Lehe salvestamine, eelvaade ja avaldamine</span><span class="sxs-lookup"><span data-stu-id="b5ba1-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="b5ba1-134">Tootelehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="b5ba1-134">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="b5ba1-135">Lehe sisu hõlbustusfunktsioonide kinnitamine</span><span class="sxs-lookup"><span data-stu-id="b5ba1-135">Verify page content accessibility</span></span>](verify-accessibility.md)
