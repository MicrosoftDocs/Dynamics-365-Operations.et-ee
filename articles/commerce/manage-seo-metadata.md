---
title: SEO metaandmete haldamine
description: See teema kirjeldab, kuidas hallata rakenduses Microsoft Dynamics 365 Commerce otsingumootori optimeerimise (SEO) metaandmeid.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 3ea06713af69659c205686a971393892fa584072
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945716"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="17082-103">SEO metaandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="17082-103">Manage SEO metadata</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="17082-104">See teema kirjeldab, kuidas hallata rakenduses Microsoft Dynamics 365 Commerce otsingumootori optimeerimise (SEO) metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="17082-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="17082-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="17082-105">Overview</span></span>

<span data-ttu-id="17082-106">Saidi SEO metaandmeid saab hallata saidikaarte ja lehe metaandmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="17082-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="17082-107">Saidikaardid</span><span class="sxs-lookup"><span data-stu-id="17082-107">Site maps</span></span>

<span data-ttu-id="17082-108">Saidikaart vastendus on teie veebisaidi lehtede (XML-vormingus) masinloetav loend.</span><span class="sxs-lookup"><span data-stu-id="17082-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="17082-109">See on mõeldud otsingumootorite poolt kasutamiseks, et need saaksid teie saidilt paremaid otsingutulemusi pakkuda.</span><span class="sxs-lookup"><span data-stu-id="17082-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="17082-110">Saidikaarte saab otsingumootoritesse käsitsi sisse tuua või avaldada robotite TXT-failis.</span><span class="sxs-lookup"><span data-stu-id="17082-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="17082-111">Dynamics 365 Commerce toetab saidikaartide automaatset loomist.</span><span class="sxs-lookup"><span data-stu-id="17082-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="17082-112">Saidikaarte uuendatakse lehtede avaldamisel ja avaldamise tühistamisel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="17082-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="17082-113">Saidikaardi loomise sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="17082-113">Turn on site map generation</span></span>

1. <span data-ttu-id="17082-114">Logige autorluse tööriista sisse.</span><span class="sxs-lookup"><span data-stu-id="17082-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="17082-115">Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).</span><span class="sxs-lookup"><span data-stu-id="17082-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="17082-116">Valige navigeerimispaanilt vasakult suvand **Saidi haldus**.</span><span class="sxs-lookup"><span data-stu-id="17082-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="17082-117">Veenduge, et suvand **Saidikaardid lubatud** on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="17082-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="17082-118">Lehe metaandmed</span><span class="sxs-lookup"><span data-stu-id="17082-118">Page metadata</span></span>

<span data-ttu-id="17082-119">Dynamics 365 Commerce võimaldab teil hallata individuaalsete lehtede SEO metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="17082-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="17082-120">Saate seda teavet vaadata ja muuta lehe konteineri jaotises **SEO atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="17082-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="17082-121">Praegu toetatakse järgmisi SEO metaandmete atribuute.</span><span class="sxs-lookup"><span data-stu-id="17082-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="17082-122">Tiitel</span><span class="sxs-lookup"><span data-stu-id="17082-122">Title</span></span>
- <span data-ttu-id="17082-123">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="17082-123">Description</span></span>
- <span data-ttu-id="17082-124">SEO märksõnad</span><span class="sxs-lookup"><span data-stu-id="17082-124">SEO keywords</span></span>
- <span data-ttu-id="17082-125">ARIA-sildid</span><span class="sxs-lookup"><span data-stu-id="17082-125">Aria labels</span></span>
- <span data-ttu-id="17082-126">noindex</span><span class="sxs-lookup"><span data-stu-id="17082-126">noindex</span></span>
- <span data-ttu-id="17082-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="17082-127">nofollow</span></span>
- <span data-ttu-id="17082-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="17082-128">noarchive</span></span>
- <span data-ttu-id="17082-129">nocache</span><span class="sxs-lookup"><span data-stu-id="17082-129">nocache</span></span>
- <span data-ttu-id="17082-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="17082-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="17082-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="17082-131">nosnippet</span></span>
- <span data-ttu-id="17082-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="17082-132">noImageIndex</span></span>
- <span data-ttu-id="17082-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="17082-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="17082-134">Lehe metaandmete muutmine</span><span class="sxs-lookup"><span data-stu-id="17082-134">Modify page metadata</span></span>

<span data-ttu-id="17082-135">Lehe metaandmete muutmiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="17082-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="17082-136">Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).</span><span class="sxs-lookup"><span data-stu-id="17082-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="17082-137">Valige navigeerimispaanilt vasakult suvand **Lehed**.</span><span class="sxs-lookup"><span data-stu-id="17082-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="17082-138">Valige avaleht, et avada see lehe redaktoris.</span><span class="sxs-lookup"><span data-stu-id="17082-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="17082-139">Toimingupaanil valige **Registreeri välja**.</span><span class="sxs-lookup"><span data-stu-id="17082-139">On the Action Pane, select **Check Out**.</span></span>
1. <span data-ttu-id="17082-140">Parempoolsel atribuutide paanil laiendage suvandit **Vaikimisi metasildid**.</span><span class="sxs-lookup"><span data-stu-id="17082-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="17082-141">Uue metasildi lisamiseks valige suvand **Lisa**ja sisestage seejärel silt väljale.</span><span class="sxs-lookup"><span data-stu-id="17082-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span>

    <span data-ttu-id="17082-142">Olemasoleva metasildi eemaldamiseks valige selle kõrval paremal prügikasti sümbol.</span><span class="sxs-lookup"><span data-stu-id="17082-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>

1. <span data-ttu-id="17082-143">Valige nupp **Salvesta** ja seejärel suvand **Registreeri**.</span><span class="sxs-lookup"><span data-stu-id="17082-143">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="17082-144">Sisestage väljale **Kommentaarid** suvand **Uuendatud metasildid** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="17082-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="17082-145">Lehe eelvaate kuvamiseks valige suvand **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="17082-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="17082-146">Kui olete lõpetanud, sulgege eelvaate vahekaart, et naasta autorluse tööriista.</span><span class="sxs-lookup"><span data-stu-id="17082-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="17082-147">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="17082-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17082-148">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="17082-148">Additional resources</span></span>

[<span data-ttu-id="17082-149">Olemasoleva saidilehe muutmine</span><span class="sxs-lookup"><span data-stu-id="17082-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="17082-150">Uue saidilehe lisamine</span><span class="sxs-lookup"><span data-stu-id="17082-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="17082-151">Lehepaigutuste valimine</span><span class="sxs-lookup"><span data-stu-id="17082-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="17082-152">Lehe salvestamine, eelvaade ja avaldamine</span><span class="sxs-lookup"><span data-stu-id="17082-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="17082-153">Tootelehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="17082-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="17082-154">Kategooria sihtlehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="17082-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="17082-155">Lehe sisu hõlbustusfunktsioonide kinnitamine</span><span class="sxs-lookup"><span data-stu-id="17082-155">Verify page content accessibility</span></span>](verify-accessibility.md)