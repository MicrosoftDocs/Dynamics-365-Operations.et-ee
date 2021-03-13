---
title: Dünaamiliste e-kaubanduse lehtede loomine URL-i parameetrite põhjal
description: See teema kirjeldab, kuidas seadistada Microsofti Dynamics 365 Commerce e-kaubanduse lehte, mis võib URL-i parameetrite põhjal dünaamilist sisu esitada.
author: StuHarg
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e72b738133b396848848d167cace80fe23694334
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098621"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a><span data-ttu-id="fcfe5-103">Dünaamiliste e-kaubanduse lehtede loomine URL-i parameetrite põhjal</span><span class="sxs-lookup"><span data-stu-id="fcfe5-103">Create dynamic e-commerce pages based on URL parameters</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="fcfe5-104">See teema kirjeldab, kuidas seadistada Microsofti Dynamics 365 Commerce e-kaubanduse lehte, mis võib URL-i parameetrite põhjal dünaamilist sisu esitada.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-104">This topic describes how to set up a Microsoft Dynamics 365 Commerce e-commerce page that can serve dynamic content, based on URL parameters.</span></span>

<span data-ttu-id="fcfe5-105">E-kaubanduse lehte saab konfigureerida URL-i tee segmendi põhjal erinevat sisu esitama.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-105">An e-commerce page can be configured to serve different content, based on a segment in the URL path.</span></span> <span data-ttu-id="fcfe5-106">Seepärast nimetatakse seda lehte dünaamiliseks leheks.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-106">Therefore, the page is known as a dynamic page.</span></span> <span data-ttu-id="fcfe5-107">Segmenti kasutatakse lehe sisu toomise parameetrina.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-107">The segment is used as a parameter to retrieve the page content.</span></span> <span data-ttu-id="fcfe5-108">Näiteks luuakse leht nimega **blogi\_vaatur** ja seostatakse URL-iga `https://fabrikam.com/blog`.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-108">For example, a page that is named **blog\_viewer** is created and associated with the URL `https://fabrikam.com/blog`.</span></span> <span data-ttu-id="fcfe5-109">Seejärel saab seda lehte kasutada URL-i tee viimasel segmendil põhineva erineva sisu näitamiseks.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-109">This page can then be used to show different content, based on the last segment in the URL path.</span></span> <span data-ttu-id="fcfe5-110">URL-i `https://fabrikam.com/blog/article-1` viimane segment on näiteks **artikkel 1**.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-110">For example, the last segment in the URL `https://fabrikam.com/blog/article-1` is **article-1**.</span></span>

<span data-ttu-id="fcfe5-111">Eraldi kohandatud lehed, mis alistavad dünaamilise lehe, saab samuti URL-i tee segmentidega seostada.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-111">Separate custom pages that override the dynamic page can also be associated with segments in the URL path.</span></span> <span data-ttu-id="fcfe5-112">Näiteks luuakse leht nimega **blogi\_kokkuvõte** ja seostatakse URL-iga `https://fabrikam.com/blog/about-this-blog`.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-112">For example, a page that is named **blog\_summary** is created and associated with the URL `https://fabrikam.com/blog/about-this-blog`.</span></span> <span data-ttu-id="fcfe5-113">Kui seda URL-i taotletakse, tagastatakse lehe **blogi\_vaatur** asemel parameetriga **/about-this-blog** seostatud leht **blogi\_kokkuvõte**.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-113">When this URL is requested, the **blog\_summary** page that is associated with the **/about-this-blog** parameter is returned instead of the **blog\_viewer** page.</span></span>

> [!NOTE]
> <span data-ttu-id="fcfe5-114">Dünaamilise lehe sisu hostimise, toomise ja näitamise funktsioon rakendatakse kohandatud mooduli abil.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-114">The functionality for hosting, retrieving, and showing dynamic page content is implemented by using a custom module.</span></span> <span data-ttu-id="fcfe5-115">Lisateavet vt teemast [Võrgukanali laiendatavus](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="fcfe5-115">For more information, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="set-up-a-dynamic-e-commerce-page"></a><span data-ttu-id="fcfe5-116">Dünaamilise e-kaubanduse lehe seadistamine</span><span class="sxs-lookup"><span data-stu-id="fcfe5-116">Set up a dynamic e-commerce page</span></span>

<span data-ttu-id="fcfe5-117">Dünaamilise e-kaubanduse lehe seadistamiseks peate looma dünaamilise lehe ja baas-URL-i ning konfigureerima marsruudi dünaamilisele lehele.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-117">To set up a dynamic e-commerce page, you must create the dynamic page, create the base URL, and configure the route to the dynamic page.</span></span>

### <a name="create-the-page-that-will-serve-dynamic-content"></a><span data-ttu-id="fcfe5-118">Dünaamilist sisu esitava lehe loomine</span><span class="sxs-lookup"><span data-stu-id="fcfe5-118">Create the page that will serve dynamic content</span></span>

<span data-ttu-id="fcfe5-119">Dünaamilist sisu esitava lehe loomiseks järgige teemas [Uue saidilehe lisamine](add-new-page.md) kirjeldatud etappe.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-119">To create a page that will serve dynamic content, follow the steps in [Add a new site page](add-new-page.md).</span></span> <span data-ttu-id="fcfe5-120">Loodava lehe puhul tuleb rakendada moodul, mis kasutab välisest andmeallikast sisu toomiseks URL-i viimast segmenti.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-120">The page that you create will require implementation of a module that uses the last segment in the URL path to retrieve content from an external data source.</span></span> <span data-ttu-id="fcfe5-121">Lisateavet kohandatud mooduli arenduse kohta vt teemast [Võrgukanali laiendatavus](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="fcfe5-121">For more information about custom module development, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

### <a name="create-the-base-url-for-the-dynamic-page"></a><span data-ttu-id="fcfe5-122">Dünaamilise lehe baas-URL-i loomine</span><span class="sxs-lookup"><span data-stu-id="fcfe5-122">Create the base URL for the dynamic page</span></span>

<span data-ttu-id="fcfe5-123">Commerce'i saidiehitajas dünaamilise lehe baas-URL-i loomiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-123">To create the base URL for the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="fcfe5-124">Avage **URL-id** ja valige **Uus \> Uus URL**.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-124">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="fcfe5-125">Tehke dialoogiboksis **Loo uus URL** valik **Sisemine leht**.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-125">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="fcfe5-126">Sisestage väljale **URL-i tee** tee, mis toimib dünaamilise lehe juurena (selles näites **/blog**).</span><span class="sxs-lookup"><span data-stu-id="fcfe5-126">Under **URL path**, enter the path that will serve as the root for the dynamic page (in this example, **/blog**).</span></span> <span data-ttu-id="fcfe5-127">Seejärel valige **Järgmine**.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-127">Then select **Next**.</span></span>
1. <span data-ttu-id="fcfe5-128">Valige dialoogiboksis **Lehe valimine** dünaamilise lehena kasutamiseks loodud leht ja seejärel valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-128">In the **Select a page** dialog box, select the page that you created to serve as the dynamic page, and then select **Save**.</span></span>
1. <span data-ttu-id="fcfe5-129">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-129">Select **Publish**.</span></span>

### <a name="configure-the-route-to-the-dynamic-page"></a><span data-ttu-id="fcfe5-130">Dünaamilise lehe marsruudi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="fcfe5-130">Configure the route to the dynamic page</span></span>

<span data-ttu-id="fcfe5-131">Commerce'i saidiehitajas dünaamilise lehe marsruudi konfigureerimiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-131">To configure the route to the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="fcfe5-132">Avage **Saidi sätted \> Laiendused**.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-132">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="fcfe5-133">Valige jaotises **Parametriseeritud URL-i teed** käsk **Lisa** ja seejärel sisestage URL-i loomisel sisestatud URL-i tee (selles näites **/blog**).</span><span class="sxs-lookup"><span data-stu-id="fcfe5-133">Under **Parameterized URL paths**, select **Add**, and then enter the URL path that you entered when you created the URL (in this example, **/blog**).</span></span>
1. <span data-ttu-id="fcfe5-134">Valige käsk **Salvesta ja avalda**.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-134">Select **Save and publish**.</span></span>

<span data-ttu-id="fcfe5-135">Kui marsruut on konfigureeritud, tagastavad kõik parametriseeritud URL-i tee taotlused selle URL-iga seotud lehe.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-135">After the route is configured, all requests to the parameterized URL path will return the page that is associated with that URL.</span></span> <span data-ttu-id="fcfe5-136">Kui mõni taotlus hõlmab lisasegmenti, tagastatakse seostatud leht ja lehe sisu toomiseks kasutatakse parameetrina segmenti.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-136">If any requests contain an additional segment, the associated page will be returned, and the page content will be retrieved by using the segment as a parameter.</span></span> <span data-ttu-id="fcfe5-137">Näiteks `https://fabrikam.com/blog/article-1` tagastab lehe **blogi\_kokkuvõte** ja lehe sisu tuuakse parameetriga **/article-1**.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-137">For example, `https://fabrikam.com/blog/article-1` will return the **blog\_summary** page, and the page content will be retrieved by using the **/article-1** parameter.</span></span>

## <a name="override-a-parameterized-url-with-a-custom-page"></a><span data-ttu-id="fcfe5-138">Kohandatud lehega parametriseeritud URL-i alistamine</span><span class="sxs-lookup"><span data-stu-id="fcfe5-138">Override a parameterized URL with a custom page</span></span>

<span data-ttu-id="fcfe5-139">Commerce'i saidiehitajas kohandatud lehega parametriseeritud URL-i alistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-139">To override a parameterized URL with a custom page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="fcfe5-140">Avage **URL-id** ja valige **Uus \> Uus URL**.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-140">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="fcfe5-141">Tehke dialoogiboksis **Loo uus URL** valik **Sisemine leht**.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-141">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="fcfe5-142">Sisestage väljal **URL-i tee** tee, mis hõlmab alistatavat segmenti (selles näites **/blog/about-this-blog**).</span><span class="sxs-lookup"><span data-stu-id="fcfe5-142">Under **URL path**, enter the path that includes the segment to override (in this example, **/blog/about-this-blog**).</span></span> <span data-ttu-id="fcfe5-143">Seejärel valige **Järgmine**.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-143">Then select **Next**.</span></span>
1. <span data-ttu-id="fcfe5-144">Valige dialoogiboksis **Lehe valimine** kohandatud leht ja seejärel valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-144">In the **Select a page** dialog box, select the custom page, and then select **Save**.</span></span>
1. <span data-ttu-id="fcfe5-145">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-145">Select **Publish**.</span></span>
1. <span data-ttu-id="fcfe5-146">Kui kohandatud leht ei ole veel avaldatud, avage jaotis **Lehed**, valige kohandatud leht ja seejärel valige käsk **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-146">If the custom page hasn't yet been published, go to **Pages**, select the custom page, and then select **Publish**.</span></span>

<span data-ttu-id="fcfe5-147">Pärast kohandatud lehe avaldamist esitatakse see parametriseeritud sisuga dünaamilise lehe asemel.</span><span class="sxs-lookup"><span data-stu-id="fcfe5-147">After the custom page is published, it will be served instead of the dynamic page that has parameterized content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fcfe5-148">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="fcfe5-148">Additional resources</span></span>

[<span data-ttu-id="fcfe5-149">Olemasoleva saidilehe muutmine</span><span class="sxs-lookup"><span data-stu-id="fcfe5-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="fcfe5-150">Uue saidilehe lisamine</span><span class="sxs-lookup"><span data-stu-id="fcfe5-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="fcfe5-151">Lehepaigutuste valimine</span><span class="sxs-lookup"><span data-stu-id="fcfe5-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="fcfe5-152">SEO metaandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="fcfe5-152">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="fcfe5-153">Lehe salvestamine, eelvaade ja avaldamine</span><span class="sxs-lookup"><span data-stu-id="fcfe5-153">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="fcfe5-154">Tootelehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="fcfe5-154">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="fcfe5-155">Kategooria sihtlehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="fcfe5-155">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="fcfe5-156">Lehe sisu hõlbustusfunktsioonide kinnitamine</span><span class="sxs-lookup"><span data-stu-id="fcfe5-156">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="fcfe5-157">Võrgukanali laiendatavus</span><span class="sxs-lookup"><span data-stu-id="fcfe5-157">Online channel extensibility</span></span>](e-commerce-extensibility/overview.md)
