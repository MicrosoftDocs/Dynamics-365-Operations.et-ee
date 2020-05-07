---
title: Uue saidilehe lisamine
description: Selles teemas kirjeldatakse, kuidas lisada rakenduses Microsoft Dynamics 365 Commerce uus saidi leht.
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
ms.openlocfilehash: b0f1e290526c25aa6e6300c65e24044a325bee53
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269954"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="da538-103">Uue saidilehe lisamine</span><span class="sxs-lookup"><span data-stu-id="da538-103">Add a new site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="da538-104">Selles teemas kirjeldatakse, kuidas lisada rakenduses Microsoft Dynamics 365 Commerce uus saidi leht.</span><span class="sxs-lookup"><span data-stu-id="da538-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="da538-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="da538-105">Overview</span></span>

<span data-ttu-id="da538-106">Pärast saidi mallide ja fragmentide loomist on järgmine etapp lehtede loomise alustamine, mis neid kasutavad.</span><span class="sxs-lookup"><span data-stu-id="da538-106">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="da538-107">Alustamiseks peate valima malli või paigutuse, lehe nime ja lehe URL-i.</span><span class="sxs-lookup"><span data-stu-id="da538-107">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="da538-108">Mall või paigutus</span><span class="sxs-lookup"><span data-stu-id="da538-108">Template or layout</span></span>

<span data-ttu-id="da538-109">Saate kasutada kas oma uue lehe malli või paigutust.</span><span class="sxs-lookup"><span data-stu-id="da538-109">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="da538-110">Lisateavet vaadake teemast [Mallide ja paigutuste ülevaade](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="da538-110">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="da538-111">Lehe nimi</span><span class="sxs-lookup"><span data-stu-id="da538-111">Page name</span></span>

<span data-ttu-id="da538-112">Lehe nimi peab olema teie lehe jaoks ainulaadne.</span><span class="sxs-lookup"><span data-stu-id="da538-112">The page name must be unique to your page.</span></span> <span data-ttu-id="da538-113">See peaks olema kirjeldav, et saaksite selle hõlpsasti leida ja teised inimesed teaksid, milleks leht on mõeldud.</span><span class="sxs-lookup"><span data-stu-id="da538-113">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="da538-114">Valige lehe nimi hoolikalt, kuna seda ei saa hiljem muuta.</span><span class="sxs-lookup"><span data-stu-id="da538-114">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="da538-115">Lehe URL</span><span class="sxs-lookup"><span data-stu-id="da538-115">Page URL</span></span>

<span data-ttu-id="da538-116">Teil võib olla võimalus sisestada uue lehe URL.</span><span class="sxs-lookup"><span data-stu-id="da538-116">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="da538-117">Lehe loomisel saate sisestada stringi, mida kasutatakse täieliku URL-i moodustamiseks.</span><span class="sxs-lookup"><span data-stu-id="da538-117">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="da538-118">See string on tuntud kui suhteline URL või URL-i komponent.</span><span class="sxs-lookup"><span data-stu-id="da538-118">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="da538-119">Seejärel luuakse URL-i komponendi põhjal täielik URL ja sellele määratakse uus leht.</span><span class="sxs-lookup"><span data-stu-id="da538-119">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="da538-120">Saate URL-i komponenti hiljem muuta, enne kui avaldate lehe.</span><span class="sxs-lookup"><span data-stu-id="da538-120">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="da538-121">Lisateavet vaadake teemast [Lehe URL-i loomine](create-page-URL.md) .</span><span class="sxs-lookup"><span data-stu-id="da538-121">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="da538-122">Dynamics 365 Commerce lahutab URL-id ja sisu.</span><span class="sxs-lookup"><span data-stu-id="da538-122">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="da538-123">Teisisõnu saab luua lehe, mis ei ole URL-iga seotud, ja saab luua URL-i, mis ei ole seotud lehega.</span><span class="sxs-lookup"><span data-stu-id="da538-123">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="da538-124">Seega saab URL-i sisu ära vahetada ja see ei nõua seisakuid ning ümbersuunamisi on hõlpsam hallata.</span><span class="sxs-lookup"><span data-stu-id="da538-124">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="da538-125">Uue lehe lisamine</span><span class="sxs-lookup"><span data-stu-id="da538-125">Add a new page</span></span>

<span data-ttu-id="da538-126">Oma saidile uue saidi lehe lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="da538-126">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="da538-127">Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).</span><span class="sxs-lookup"><span data-stu-id="da538-127">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="da538-128">Valige suvand **Uus leht**.</span><span class="sxs-lookup"><span data-stu-id="da538-128">Select **New Page**.</span></span>
1. <span data-ttu-id="da538-129">Valige dialoogiaknas **Uus leht** mall ja valige seejärel nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="da538-129">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="da538-130">Väljale **Lehe nimi** sisestage lehe nimi (näiteks **Minu uus leht**).</span><span class="sxs-lookup"><span data-stu-id="da538-130">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="da538-131">Väljale **URL** sisestage string (URL-i komponent), et URL lõpetada (näiteks **minuuusleht**).</span><span class="sxs-lookup"><span data-stu-id="da538-131">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="da538-132">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="da538-132">Select **OK**.</span></span> <span data-ttu-id="da538-133">Kuvatakse lehe redaktor.</span><span class="sxs-lookup"><span data-stu-id="da538-133">The page editor appears.</span></span> <span data-ttu-id="da538-134">Pange tähele, et päis ja jalus lisatakse lehele automaatselt, olenevalt teie valitud mallist.</span><span class="sxs-lookup"><span data-stu-id="da538-134">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="da538-135">Lehe liigenduses valige pesa **Peamine**, valige kolmikpunkt nupp (**...**) ja seejärel valige suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="da538-135">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="da538-136">Valige suvand **Konteiner** ja seejärel nupp **OK**</span><span class="sxs-lookup"><span data-stu-id="da538-136">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="da538-137">Valige **Sujuv konteiner**, kolmikpunkti nupp ja seejärel käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="da538-137">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="da538-138">Valige **Sisurikas plokk** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="da538-138">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="da538-139">Valige **Sisurikas plokk**, kolmikpunkti nupp ja seejärel käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="da538-139">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="da538-140">Valige **Sisurikka ploki üksus** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="da538-140">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="da538-141">Parempoolsel atribuutide paanil valige **Lõik** ja seejärel sisestage väljale **Minu katsetekst**.</span><span class="sxs-lookup"><span data-stu-id="da538-141">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="da538-142">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="da538-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="da538-143">Sisestage väljale **Kommentaarid** suvand **Lisatud uus leht** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="da538-143">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="da538-144">Lehe eelvaate kuvamiseks valige suvand **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="da538-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="da538-145">Kui olete lõpetanud, sulgege eelvaate vahekaart, et naasta autorluse tööriista.</span><span class="sxs-lookup"><span data-stu-id="da538-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="da538-146">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="da538-146">Select **Publish**.</span></span>
1. <span data-ttu-id="da538-147">Navigeerimisteel (lingirida) valige **Fabrikam** (või oma saidi nimi).</span><span class="sxs-lookup"><span data-stu-id="da538-147">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="da538-148">Valige navigeerimispaanilt vasakult suvand **URL-id**.</span><span class="sxs-lookup"><span data-stu-id="da538-148">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="da538-149">Leidke loendist ja valige oma URL (**minuuusleht**).</span><span class="sxs-lookup"><span data-stu-id="da538-149">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="da538-150">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="da538-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da538-151">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="da538-151">Additional resources</span></span>

[<span data-ttu-id="da538-152">Olemasoleva saidilehe muutmine</span><span class="sxs-lookup"><span data-stu-id="da538-152">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="da538-153">Lehepaigutuste valimine</span><span class="sxs-lookup"><span data-stu-id="da538-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="da538-154">SEO metaandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="da538-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="da538-155">Lehe salvestamine, eelvaade ja avaldamine</span><span class="sxs-lookup"><span data-stu-id="da538-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="da538-156">Tootelehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="da538-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="da538-157">Kategooria sihtlehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="da538-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="da538-158">Lehe sisu hõlbustusfunktsioonide kinnitamine</span><span class="sxs-lookup"><span data-stu-id="da538-158">Verify page content accessibility</span></span>](verify-accessibility.md)
