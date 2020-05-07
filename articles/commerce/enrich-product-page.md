---
title: Tootelehe rikastamine
description: Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Commerce toote lehte rikastada.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12508a80c440894ec6e2073b5e550846480e6c45
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269816"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="92ca0-103">Tootelehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="92ca0-103">Enrich a product page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="92ca0-104">Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Commerce toote lehte rikastada.</span><span class="sxs-lookup"><span data-stu-id="92ca0-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="92ca0-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="92ca0-105">Overview</span></span>

<span data-ttu-id="92ca0-106">Vaikimisi kasutab teie sait toote andmete näitamiseks üldist lehte.</span><span class="sxs-lookup"><span data-stu-id="92ca0-106">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="92ca0-107">See leht sisaldab põhiteavet toote ja selle müümiseks vajalike juhtelementide kohta.</span><span class="sxs-lookup"><span data-stu-id="92ca0-107">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="92ca0-108">Samas saate täiendada kaubanduse skaala üksusest tulevat teavet konkreetse toote täiendavate piltide või tekstiga.</span><span class="sxs-lookup"><span data-stu-id="92ca0-108">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="92ca0-109">See protsess on tuntud kui toote lehe rikastamine.</span><span class="sxs-lookup"><span data-stu-id="92ca0-109">This process is known as enriching the product page.</span></span>

<span data-ttu-id="92ca0-110">Paljudel juhtudel soovite oma toodete jaoks kasutada kindlat täiendavat sisu.</span><span class="sxs-lookup"><span data-stu-id="92ca0-110">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="92ca0-111">Kui avate autoriseerimise tööriistal suvandi **Jaemüük ja kaubandus**, näete saidile määratud kanalist pärinevate toodete loendit.</span><span class="sxs-lookup"><span data-stu-id="92ca0-111">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="92ca0-112">Selles loendis näitab veerg **Rikastatud**, kas toote tooteleht on rikastatud.</span><span class="sxs-lookup"><span data-stu-id="92ca0-112">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="92ca0-113">Kui veerus kuvatakse märge, on toote jaoks olemas rikastatud toote leht.</span><span class="sxs-lookup"><span data-stu-id="92ca0-113">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="92ca0-114">Kui ühtegi märget ei kuvata, kasutatakse toote jaoks vaikimisi tootelehte ja sisu.</span><span class="sxs-lookup"><span data-stu-id="92ca0-114">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="92ca0-115">Võite kuvada  nii rikastatud kui ka mitte rikastatud toote lehtede eelvaate, valides loendist toote nime.</span><span class="sxs-lookup"><span data-stu-id="92ca0-115">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="92ca0-116">Tootelehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="92ca0-116">Enrich a product page</span></span>

<span data-ttu-id="92ca0-117">Tootelehe rikastamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="92ca0-117">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="92ca0-118">Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).</span><span class="sxs-lookup"><span data-stu-id="92ca0-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="92ca0-119">Valige navigeerimispaanilt vasakult suvand **Tooted**.</span><span class="sxs-lookup"><span data-stu-id="92ca0-119">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="92ca0-120">Valige toode, millel pole rikastatud tootelehte.</span><span class="sxs-lookup"><span data-stu-id="92ca0-120">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="92ca0-121">Valige toimingupaanil suvand **Rikastatud tooteleht**.</span><span class="sxs-lookup"><span data-stu-id="92ca0-121">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="92ca0-122">Valige suvand **PDP mall** ja seejärel nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="92ca0-122">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="92ca0-123">Laiendage vasakul lehe liigendpuus pesa **Peamine**.</span><span class="sxs-lookup"><span data-stu-id="92ca0-123">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="92ca0-124">Valige pesa **Peamine** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="92ca0-124">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="92ca0-125">Valige suvand **Konteiner 2** ja seejärel nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="92ca0-125">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="92ca0-126">Valige suvandi **Konteiner 2** kolmikpunkti nupp ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="92ca0-126">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="92ca0-127">Valige suvand **Funktsioon** ja seejärel nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="92ca0-127">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="92ca0-128">Parempoolsel atribuutide paanil sisestage väljale **Rikastekst** toote värskendatud kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="92ca0-128">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="92ca0-129">Sisestage väljale **Pealkiri** pealkirja tekst ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="92ca0-129">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="92ca0-130">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="92ca0-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="92ca0-131">Sisestage väljale **Kommentaarid** suvand **Rikastatud suvand** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="92ca0-131">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="92ca0-132">Rikastatud tootelehe eelvaate kuvamiseks valige suvand **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="92ca0-132">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="92ca0-133">Kui olete lõpetanud, sulgege eelvaate vahekaart, et naasta autorluse tööriista.</span><span class="sxs-lookup"><span data-stu-id="92ca0-133">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="92ca0-134">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="92ca0-134">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92ca0-135">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="92ca0-135">Additional resources</span></span>

[<span data-ttu-id="92ca0-136">Olemasoleva saidilehe muutmine</span><span class="sxs-lookup"><span data-stu-id="92ca0-136">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="92ca0-137">Uue saidilehe lisamine</span><span class="sxs-lookup"><span data-stu-id="92ca0-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="92ca0-138">Lehepaigutuste valimine</span><span class="sxs-lookup"><span data-stu-id="92ca0-138">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="92ca0-139">SEO metaandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="92ca0-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="92ca0-140">Lehe salvestamine, eelvaade ja avaldamine</span><span class="sxs-lookup"><span data-stu-id="92ca0-140">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="92ca0-141">Kategooria sihtlehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="92ca0-141">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="92ca0-142">Lehe sisu hõlbustusfunktsioonide kinnitamine</span><span class="sxs-lookup"><span data-stu-id="92ca0-142">Verify page content accessibility</span></span>](verify-accessibility.md)
