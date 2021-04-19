---
title: Uue saidilehe lisamine
description: Selles teemas kirjeldatakse, kuidas lisada rakenduses Microsoft Microsoft Dynamics 365 Commerce uus saidi leht.
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
ms.openlocfilehash: 4a2ecc3ef3ff3f708cec50e42777b50ec4576e25
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797547"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="0a13b-103">Uue saidilehe lisamine</span><span class="sxs-lookup"><span data-stu-id="0a13b-103">Add a new site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0a13b-104">Selles teemas kirjeldatakse, kuidas lisada rakenduses Microsoft Microsoft Dynamics 365 Commerce uus saidi leht.</span><span class="sxs-lookup"><span data-stu-id="0a13b-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0a13b-105">Pärast saidi mallide ja fragmentide loomist on järgmine etapp lehtede loomise alustamine, mis neid kasutavad.</span><span class="sxs-lookup"><span data-stu-id="0a13b-105">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="0a13b-106">Alustamiseks peate valima malli või paigutuse, lehe nime ja lehe URL-i.</span><span class="sxs-lookup"><span data-stu-id="0a13b-106">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="0a13b-107">Mall või paigutus</span><span class="sxs-lookup"><span data-stu-id="0a13b-107">Template or layout</span></span>

<span data-ttu-id="0a13b-108">Saate kasutada kas oma uue lehe malli või paigutust.</span><span class="sxs-lookup"><span data-stu-id="0a13b-108">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="0a13b-109">Lisateavet vaadake teemast [Mallide ja paigutuste ülevaade](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0a13b-109">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="0a13b-110">Lehe nimi</span><span class="sxs-lookup"><span data-stu-id="0a13b-110">Page name</span></span>

<span data-ttu-id="0a13b-111">Lehe nimi peab olema teie lehe jaoks ainulaadne.</span><span class="sxs-lookup"><span data-stu-id="0a13b-111">The page name must be unique to your page.</span></span> <span data-ttu-id="0a13b-112">See peaks olema kirjeldav, et saaksite selle hõlpsasti leida ja teised inimesed teaksid, milleks leht on mõeldud.</span><span class="sxs-lookup"><span data-stu-id="0a13b-112">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="0a13b-113">Valige lehe nimi hoolikalt, kuna seda ei saa hiljem muuta.</span><span class="sxs-lookup"><span data-stu-id="0a13b-113">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="0a13b-114">Lehe URL</span><span class="sxs-lookup"><span data-stu-id="0a13b-114">Page URL</span></span>

<span data-ttu-id="0a13b-115">Teil võib olla võimalus sisestada uue lehe URL.</span><span class="sxs-lookup"><span data-stu-id="0a13b-115">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="0a13b-116">Lehe loomisel saate sisestada stringi, mida kasutatakse täieliku URL-i moodustamiseks.</span><span class="sxs-lookup"><span data-stu-id="0a13b-116">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="0a13b-117">See string on tuntud kui suhteline URL või URL-i komponent.</span><span class="sxs-lookup"><span data-stu-id="0a13b-117">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="0a13b-118">Seejärel luuakse URL-i komponendi põhjal täielik URL ja sellele määratakse uus leht.</span><span class="sxs-lookup"><span data-stu-id="0a13b-118">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="0a13b-119">Saate URL-i komponenti hiljem muuta, enne kui avaldate lehe.</span><span class="sxs-lookup"><span data-stu-id="0a13b-119">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="0a13b-120">Lisateavet vaadake teemast [Lehe URL-i loomine](create-page-URL.md) .</span><span class="sxs-lookup"><span data-stu-id="0a13b-120">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="0a13b-121">Dynamics 365 Commerce lahutab URL-id ja sisu.</span><span class="sxs-lookup"><span data-stu-id="0a13b-121">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="0a13b-122">Teisisõnu saab luua lehe, mis ei ole URL-iga seotud, ja saab luua URL-i, mis ei ole seotud lehega.</span><span class="sxs-lookup"><span data-stu-id="0a13b-122">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="0a13b-123">Seega saab URL-i sisu ära vahetada ja see ei nõua seisakuid ning ümbersuunamisi on hõlpsam hallata.</span><span class="sxs-lookup"><span data-stu-id="0a13b-123">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="0a13b-124">Uue lehe lisamine</span><span class="sxs-lookup"><span data-stu-id="0a13b-124">Add a new page</span></span>

<span data-ttu-id="0a13b-125">Oma saidile uue saidi lehe lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="0a13b-125">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="0a13b-126">Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).</span><span class="sxs-lookup"><span data-stu-id="0a13b-126">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="0a13b-127">Valige suvand **Uus leht**.</span><span class="sxs-lookup"><span data-stu-id="0a13b-127">Select **New Page**.</span></span>
1. <span data-ttu-id="0a13b-128">Valige dialoogiaknas **Uus leht** mall ja valige seejärel nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a13b-128">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="0a13b-129">Väljale **Lehe nimi** sisestage lehe nimi (näiteks **Minu uus leht**).</span><span class="sxs-lookup"><span data-stu-id="0a13b-129">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="0a13b-130">Väljale **URL** sisestage string (URL-i komponent), et URL lõpetada (näiteks **minuuusleht**).</span><span class="sxs-lookup"><span data-stu-id="0a13b-130">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="0a13b-131">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a13b-131">Select **OK**.</span></span> <span data-ttu-id="0a13b-132">Kuvatakse lehe redaktor.</span><span class="sxs-lookup"><span data-stu-id="0a13b-132">The page editor appears.</span></span> <span data-ttu-id="0a13b-133">Pange tähele, et päis ja jalus lisatakse lehele automaatselt, olenevalt teie valitud mallist.</span><span class="sxs-lookup"><span data-stu-id="0a13b-133">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="0a13b-134">Lehe liigenduses valige pesa **Peamine**, valige kolmikpunkt nupp (**...**) ja seejärel valige suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="0a13b-134">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0a13b-135">Valige suvand **Konteiner** ja seejärel nupp **OK**</span><span class="sxs-lookup"><span data-stu-id="0a13b-135">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="0a13b-136">Valige **Sujuv konteiner**, kolmikpunkti nupp ja seejärel käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="0a13b-136">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="0a13b-137">Valige **Sisurikas plokk** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a13b-137">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="0a13b-138">Valige **Sisurikas plokk**, kolmikpunkti nupp ja seejärel käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="0a13b-138">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="0a13b-139">Valige **Sisurikka ploki üksus** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a13b-139">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="0a13b-140">Parempoolsel atribuutide paanil valige **Lõik** ja seejärel sisestage väljale **Minu katsetekst**.</span><span class="sxs-lookup"><span data-stu-id="0a13b-140">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="0a13b-141">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="0a13b-141">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="0a13b-142">Sisestage väljale **Kommentaarid** suvand **Lisatud uus leht** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a13b-142">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="0a13b-143">Lehe eelvaate kuvamiseks valige suvand **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="0a13b-143">Select **Preview** to preview your page.</span></span> <span data-ttu-id="0a13b-144">Kui olete lõpetanud, sulgege eelvaate vahekaart, et naasta autorluse tööriista.</span><span class="sxs-lookup"><span data-stu-id="0a13b-144">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="0a13b-145">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="0a13b-145">Select **Publish**.</span></span>
1. <span data-ttu-id="0a13b-146">Navigeerimisteel (lingirida) valige **Fabrikam** (või oma saidi nimi).</span><span class="sxs-lookup"><span data-stu-id="0a13b-146">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="0a13b-147">Valige navigeerimispaanilt vasakult suvand **URL-id**.</span><span class="sxs-lookup"><span data-stu-id="0a13b-147">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="0a13b-148">Leidke loendist ja valige oma URL (**minuuusleht**).</span><span class="sxs-lookup"><span data-stu-id="0a13b-148">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="0a13b-149">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="0a13b-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0a13b-150">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0a13b-150">Additional resources</span></span>

[<span data-ttu-id="0a13b-151">Olemasoleva saidilehe muutmine</span><span class="sxs-lookup"><span data-stu-id="0a13b-151">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="0a13b-152">Lehepaigutuste valimine</span><span class="sxs-lookup"><span data-stu-id="0a13b-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="0a13b-153">SEO metaandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="0a13b-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="0a13b-154">Lehe salvestamine, eelvaade ja avaldamine</span><span class="sxs-lookup"><span data-stu-id="0a13b-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="0a13b-155">Tootelehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="0a13b-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="0a13b-156">Kategooria sihtlehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="0a13b-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="0a13b-157">Lehe sisu hõlbustusfunktsioonide kinnitamine</span><span class="sxs-lookup"><span data-stu-id="0a13b-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="0a13b-158">Dünaamiliste e-kaubanduse lehtede loomine URL-parameetrite põhjal</span><span class="sxs-lookup"><span data-stu-id="0a13b-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
