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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fcb8eda188a6796282a7a800b87a68dfef9d7d62
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097334"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="65305-103">Tootelehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="65305-103">Enrich a product page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="65305-104">Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Commerce toote lehte rikastada.</span><span class="sxs-lookup"><span data-stu-id="65305-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="65305-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="65305-105">Overview</span></span>

<span data-ttu-id="65305-106">Vaikimisi kasutab teie sait toote andmete näitamiseks üldist lehte.</span><span class="sxs-lookup"><span data-stu-id="65305-106">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="65305-107">See leht sisaldab põhiteavet toote ja selle müümiseks vajalike juhtelementide kohta.</span><span class="sxs-lookup"><span data-stu-id="65305-107">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="65305-108">Samas saate täiendada kaubanduse skaala üksusest tulevat teavet konkreetse toote täiendavate piltide või tekstiga.</span><span class="sxs-lookup"><span data-stu-id="65305-108">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="65305-109">See protsess on tuntud kui toote lehe rikastamine.</span><span class="sxs-lookup"><span data-stu-id="65305-109">This process is known as enriching the product page.</span></span>

<span data-ttu-id="65305-110">Paljudel juhtudel soovite oma toodete jaoks kasutada kindlat täiendavat sisu.</span><span class="sxs-lookup"><span data-stu-id="65305-110">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="65305-111">Kui avate autoriseerimise tööriistal suvandi **Jaemüük ja kaubandus**, näete saidile määratud kanalist pärinevate toodete loendit.</span><span class="sxs-lookup"><span data-stu-id="65305-111">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="65305-112">Selles loendis näitab veerg **Rikastatud**, kas toote tooteleht on rikastatud.</span><span class="sxs-lookup"><span data-stu-id="65305-112">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="65305-113">Kui veerus kuvatakse märge, on toote jaoks olemas rikastatud toote leht.</span><span class="sxs-lookup"><span data-stu-id="65305-113">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="65305-114">Kui ühtegi märget ei kuvata, kasutatakse toote jaoks vaikimisi tootelehte ja sisu.</span><span class="sxs-lookup"><span data-stu-id="65305-114">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="65305-115">Võite kuvada  nii rikastatud kui ka mitte rikastatud toote lehtede eelvaate, valides loendist toote nime.</span><span class="sxs-lookup"><span data-stu-id="65305-115">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="65305-116">Tootelehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="65305-116">Enrich a product page</span></span>

<span data-ttu-id="65305-117">Tootelehe rikastamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="65305-117">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="65305-118">Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).</span><span class="sxs-lookup"><span data-stu-id="65305-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="65305-119">Valige navigeerimispaanilt vasakult suvand **Tooted**.</span><span class="sxs-lookup"><span data-stu-id="65305-119">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="65305-120">Valige toode, millel pole rikastatud tootelehte.</span><span class="sxs-lookup"><span data-stu-id="65305-120">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="65305-121">Valige toimingupaanil suvand **Rikastatud tooteleht**.</span><span class="sxs-lookup"><span data-stu-id="65305-121">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="65305-122">Valige suvand **PDP mall** ja seejärel nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="65305-122">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="65305-123">Laiendage vasakul lehe liigendpuus pesa **Peamine**.</span><span class="sxs-lookup"><span data-stu-id="65305-123">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="65305-124">Valige pesa **Peamine** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="65305-124">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="65305-125">Valige suvand **Konteiner 2** ja seejärel nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="65305-125">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="65305-126">Valige suvandi **Konteiner 2** kolmikpunkti nupp ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="65305-126">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="65305-127">Valige suvand **Funktsioon** ja seejärel nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="65305-127">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="65305-128">Parempoolsel atribuutide paanil sisestage väljale **Rikastekst** toote värskendatud kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="65305-128">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="65305-129">Sisestage väljale **Pealkiri** pealkirja tekst ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="65305-129">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="65305-130">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="65305-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="65305-131">Sisestage väljale **Kommentaarid** suvand **Rikastatud suvand** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="65305-131">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="65305-132">Rikastatud tootelehe eelvaate kuvamiseks valige suvand **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="65305-132">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="65305-133">Kui olete lõpetanud, sulgege eelvaate vahekaart, et naasta autorluse tööriista.</span><span class="sxs-lookup"><span data-stu-id="65305-133">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="65305-134">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="65305-134">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65305-135">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="65305-135">Additional resources</span></span>

[<span data-ttu-id="65305-136">Olemasoleva saidilehe muutmine</span><span class="sxs-lookup"><span data-stu-id="65305-136">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="65305-137">Uue saidilehe lisamine</span><span class="sxs-lookup"><span data-stu-id="65305-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="65305-138">Lehepaigutuste valimine</span><span class="sxs-lookup"><span data-stu-id="65305-138">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="65305-139">SEO metaandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="65305-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="65305-140">Lehe salvestamine, eelvaade ja avaldamine</span><span class="sxs-lookup"><span data-stu-id="65305-140">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="65305-141">Kategooria sihtlehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="65305-141">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="65305-142">Lehe sisu hõlbustusfunktsioonide kinnitamine</span><span class="sxs-lookup"><span data-stu-id="65305-142">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="65305-143">Dünaamiliste e-kaubanduse lehtede loomine URL-parameetrite põhjal</span><span class="sxs-lookup"><span data-stu-id="65305-143">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)
