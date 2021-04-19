---
title: SEO metaandmete haldamine
description: See teema kirjeldab, kuidas hallata rakenduses Microsoft Dynamics 365 Commerce otsingumootori optimeerimise (SEO) metaandmeid.
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
ms.openlocfilehash: 1e03ef346df92a94b0a403f241d0f7d1f64fd210
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794207"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="03e9c-103">SEO metaandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="03e9c-103">Manage SEO metadata</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="03e9c-104">See teema kirjeldab, kuidas hallata rakenduses Microsoft Dynamics 365 Commerce otsingumootori optimeerimise (SEO) metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="03e9c-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="03e9c-105">Saidi SEO metaandmeid saab hallata saidikaarte ja lehe metaandmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="03e9c-105">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="03e9c-106">Saidikaardid</span><span class="sxs-lookup"><span data-stu-id="03e9c-106">Site maps</span></span>

<span data-ttu-id="03e9c-107">Saidikaart vastendus on teie veebisaidi lehtede (XML-vormingus) masinloetav loend.</span><span class="sxs-lookup"><span data-stu-id="03e9c-107">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="03e9c-108">See on mõeldud otsingumootorite poolt kasutamiseks, et need saaksid teie saidilt paremaid otsingutulemusi pakkuda.</span><span class="sxs-lookup"><span data-stu-id="03e9c-108">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="03e9c-109">Saidikaarte saab otsingumootoritesse käsitsi sisse tuua või avaldada robotite TXT-failis.</span><span class="sxs-lookup"><span data-stu-id="03e9c-109">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="03e9c-110">Dynamics 365 Commerce toetab saidikaartide automaatset loomist.</span><span class="sxs-lookup"><span data-stu-id="03e9c-110">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="03e9c-111">Saidikaarte uuendatakse lehtede avaldamisel ja avaldamise tühistamisel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="03e9c-111">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="03e9c-112">Saidikaardi loomise sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="03e9c-112">Turn on site map generation</span></span>

1. <span data-ttu-id="03e9c-113">Logige autorluse tööriista sisse.</span><span class="sxs-lookup"><span data-stu-id="03e9c-113">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="03e9c-114">Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).</span><span class="sxs-lookup"><span data-stu-id="03e9c-114">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="03e9c-115">Valige navigeerimispaanilt vasakult suvand **Saidi haldus**.</span><span class="sxs-lookup"><span data-stu-id="03e9c-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="03e9c-116">Veenduge, et suvand **Saidikaardid lubatud** on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="03e9c-116">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="03e9c-117">Lehe metaandmed</span><span class="sxs-lookup"><span data-stu-id="03e9c-117">Page metadata</span></span>

<span data-ttu-id="03e9c-118">Dynamics 365 Commerce võimaldab teil hallata individuaalsete lehtede SEO metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="03e9c-118">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="03e9c-119">Saate seda teavet vaadata ja muuta lehe konteineri jaotises **SEO atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="03e9c-119">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="03e9c-120">Praegu toetatakse järgmisi SEO metaandmete atribuute.</span><span class="sxs-lookup"><span data-stu-id="03e9c-120">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="03e9c-121">Tiitel</span><span class="sxs-lookup"><span data-stu-id="03e9c-121">Title</span></span>
- <span data-ttu-id="03e9c-122">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="03e9c-122">Description</span></span>
- <span data-ttu-id="03e9c-123">SEO märksõnad</span><span class="sxs-lookup"><span data-stu-id="03e9c-123">SEO keywords</span></span>
- <span data-ttu-id="03e9c-124">ARIA-sildid</span><span class="sxs-lookup"><span data-stu-id="03e9c-124">Aria labels</span></span>
- <span data-ttu-id="03e9c-125">noindex</span><span class="sxs-lookup"><span data-stu-id="03e9c-125">noindex</span></span>
- <span data-ttu-id="03e9c-126">nofollow</span><span class="sxs-lookup"><span data-stu-id="03e9c-126">nofollow</span></span>
- <span data-ttu-id="03e9c-127">noarchive</span><span class="sxs-lookup"><span data-stu-id="03e9c-127">noarchive</span></span>
- <span data-ttu-id="03e9c-128">nocache</span><span class="sxs-lookup"><span data-stu-id="03e9c-128">nocache</span></span>
- <span data-ttu-id="03e9c-129">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="03e9c-129">noOpenDirectoryProject</span></span>
- <span data-ttu-id="03e9c-130">nosnippet</span><span class="sxs-lookup"><span data-stu-id="03e9c-130">nosnippet</span></span>
- <span data-ttu-id="03e9c-131">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="03e9c-131">noImageIndex</span></span>
- <span data-ttu-id="03e9c-132">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="03e9c-132">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="03e9c-133">Lehe metaandmete muutmine</span><span class="sxs-lookup"><span data-stu-id="03e9c-133">Modify page metadata</span></span>

<span data-ttu-id="03e9c-134">Lehe metaandmete muutmiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="03e9c-134">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="03e9c-135">Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).</span><span class="sxs-lookup"><span data-stu-id="03e9c-135">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="03e9c-136">Valige navigeerimispaanilt vasakult suvand **Lehed**.</span><span class="sxs-lookup"><span data-stu-id="03e9c-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="03e9c-137">Valige avaleht, et avada see lehe redaktoris.</span><span class="sxs-lookup"><span data-stu-id="03e9c-137">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="03e9c-138">Klõpsake käsuribal käsku **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="03e9c-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="03e9c-139">Parempoolsel atribuutide paanil laiendage suvandit **Vaikimisi metasildid**.</span><span class="sxs-lookup"><span data-stu-id="03e9c-139">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="03e9c-140">Uue metasildi lisamiseks valige suvand **Lisa** ja sisestage seejärel silt väljale.</span><span class="sxs-lookup"><span data-stu-id="03e9c-140">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="03e9c-141">Olemasoleva metasildi eemaldamiseks valige selle kõrval paremal prügikasti sümbol.</span><span class="sxs-lookup"><span data-stu-id="03e9c-141">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="03e9c-142">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="03e9c-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="03e9c-143">Sisestage väljale **Kommentaarid** suvand **Uuendatud metasildid** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="03e9c-143">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="03e9c-144">Lehe eelvaate kuvamiseks valige suvand **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="03e9c-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="03e9c-145">Kui olete lõpetanud, sulgege eelvaate vahekaart, et naasta autorluse tööriista.</span><span class="sxs-lookup"><span data-stu-id="03e9c-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="03e9c-146">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="03e9c-146">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03e9c-147">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="03e9c-147">Additional resources</span></span>

[<span data-ttu-id="03e9c-148">Olemasoleva saidilehe muutmine</span><span class="sxs-lookup"><span data-stu-id="03e9c-148">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="03e9c-149">Uue saidilehe lisamine</span><span class="sxs-lookup"><span data-stu-id="03e9c-149">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="03e9c-150">Lehepaigutuste valimine</span><span class="sxs-lookup"><span data-stu-id="03e9c-150">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="03e9c-151">Lehe salvestamine, eelvaade ja avaldamine</span><span class="sxs-lookup"><span data-stu-id="03e9c-151">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="03e9c-152">Tootelehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="03e9c-152">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="03e9c-153">Kategooria sihtlehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="03e9c-153">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="03e9c-154">Lehe sisu hõlbustusfunktsioonide kinnitamine</span><span class="sxs-lookup"><span data-stu-id="03e9c-154">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="03e9c-155">Dünaamiliste e-kaubanduse lehtede loomine URL-parameetrite põhjal</span><span class="sxs-lookup"><span data-stu-id="03e9c-155">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
