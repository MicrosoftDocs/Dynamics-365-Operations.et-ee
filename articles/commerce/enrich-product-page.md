---
title: Tootelehe rikastamine
description: Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Commerce toote lehte rikastada.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6c1a9474ed514426386b1d7b4a72b62129cdb8a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799036"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="8818c-103">Tootelehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="8818c-103">Enrich a product page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8818c-104">Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Commerce toote lehte rikastada.</span><span class="sxs-lookup"><span data-stu-id="8818c-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8818c-105">Vaikimisi kasutab teie sait toote andmete näitamiseks üldist lehte.</span><span class="sxs-lookup"><span data-stu-id="8818c-105">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="8818c-106">See leht sisaldab põhiteavet toote ja selle müümiseks vajalike juhtelementide kohta.</span><span class="sxs-lookup"><span data-stu-id="8818c-106">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="8818c-107">Samas saate täiendada kaubanduse skaala üksusest tulevat teavet konkreetse toote täiendavate piltide või tekstiga.</span><span class="sxs-lookup"><span data-stu-id="8818c-107">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="8818c-108">See protsess on tuntud kui toote lehe rikastamine.</span><span class="sxs-lookup"><span data-stu-id="8818c-108">This process is known as enriching the product page.</span></span>

<span data-ttu-id="8818c-109">Paljudel juhtudel soovite oma toodete jaoks kasutada kindlat täiendavat sisu.</span><span class="sxs-lookup"><span data-stu-id="8818c-109">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="8818c-110">Kui avate autoriseerimise tööriistal suvandi **Jaemüük ja kaubandus**, näete saidile määratud kanalist pärinevate toodete loendit.</span><span class="sxs-lookup"><span data-stu-id="8818c-110">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="8818c-111">Selles loendis näitab veerg **Rikastatud**, kas toote tooteleht on rikastatud.</span><span class="sxs-lookup"><span data-stu-id="8818c-111">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="8818c-112">Kui veerus kuvatakse märge, on toote jaoks olemas rikastatud toote leht.</span><span class="sxs-lookup"><span data-stu-id="8818c-112">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="8818c-113">Kui ühtegi märget ei kuvata, kasutatakse toote jaoks vaikimisi tootelehte ja sisu.</span><span class="sxs-lookup"><span data-stu-id="8818c-113">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="8818c-114">Võite kuvada nii rikastatud kui ka mitte rikastatud toote lehtede eelvaate, valides loendist toote nime.</span><span class="sxs-lookup"><span data-stu-id="8818c-114">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="8818c-115">Tootelehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="8818c-115">Enrich a product page</span></span>

<span data-ttu-id="8818c-116">Tootelehe rikastamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="8818c-116">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="8818c-117">Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).</span><span class="sxs-lookup"><span data-stu-id="8818c-117">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="8818c-118">Valige navigeerimispaanilt vasakult suvand **Tooted**.</span><span class="sxs-lookup"><span data-stu-id="8818c-118">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="8818c-119">Valige toode, millel pole rikastatud tootelehte.</span><span class="sxs-lookup"><span data-stu-id="8818c-119">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="8818c-120">Valige toimingupaanil suvand **Rikastatud tooteleht**.</span><span class="sxs-lookup"><span data-stu-id="8818c-120">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="8818c-121">Valige suvand **PDP mall** ja seejärel nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8818c-121">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="8818c-122">Laiendage vasakul lehe liigendpuus pesa **Peamine**.</span><span class="sxs-lookup"><span data-stu-id="8818c-122">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="8818c-123">Valige pesa **Peamine** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="8818c-123">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="8818c-124">Valige suvand **Konteiner 2** ja seejärel nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8818c-124">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="8818c-125">Valige suvandi **Konteiner 2** kolmikpunkti nupp ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="8818c-125">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="8818c-126">Valige suvand **Funktsioon** ja seejärel nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8818c-126">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="8818c-127">Parempoolsel atribuutide paanil sisestage väljale **Rikastekst** toote värskendatud kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="8818c-127">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="8818c-128">Sisestage väljale **Pealkiri** pealkirja tekst ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="8818c-128">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="8818c-129">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="8818c-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="8818c-130">Sisestage väljale **Kommentaarid** suvand **Rikastatud suvand** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="8818c-130">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="8818c-131">Rikastatud tootelehe eelvaate kuvamiseks valige suvand **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="8818c-131">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="8818c-132">Kui olete lõpetanud, sulgege eelvaate vahekaart, et naasta autorluse tööriista.</span><span class="sxs-lookup"><span data-stu-id="8818c-132">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="8818c-133">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="8818c-133">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8818c-134">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="8818c-134">Additional resources</span></span>

[<span data-ttu-id="8818c-135">Olemasoleva saidilehe muutmine</span><span class="sxs-lookup"><span data-stu-id="8818c-135">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="8818c-136">Uue saidilehe lisamine</span><span class="sxs-lookup"><span data-stu-id="8818c-136">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="8818c-137">Lehepaigutuste valimine</span><span class="sxs-lookup"><span data-stu-id="8818c-137">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="8818c-138">SEO metaandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="8818c-138">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="8818c-139">Lehe salvestamine, eelvaade ja avaldamine</span><span class="sxs-lookup"><span data-stu-id="8818c-139">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="8818c-140">Kategooria sihtlehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="8818c-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="8818c-141">Lehe sisu hõlbustusfunktsioonide kinnitamine</span><span class="sxs-lookup"><span data-stu-id="8818c-141">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="8818c-142">Dünaamiliste e-kaubanduse lehtede loomine URL-parameetrite põhjal</span><span class="sxs-lookup"><span data-stu-id="8818c-142">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
