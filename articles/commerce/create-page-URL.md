---
title: Lehe URL-i loomine
description: See teema käsitleb saidil lehe URL-i loomise põhimõisteid ja -toiminguid.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 98743d8948669f32d3c74e1915c7ed53db81141c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795687"
---
# <a name="create-a-page-url"></a><span data-ttu-id="f5238-103">Lehe URL-i loomine</span><span class="sxs-lookup"><span data-stu-id="f5238-103">Create a page URL</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f5238-104">See teema käsitleb saidil lehe URL-i loomise põhimõisteid ja -toiminguid.</span><span class="sxs-lookup"><span data-stu-id="f5238-104">This topic covers the basic concepts and procedures for creating a page URL on your site.</span></span>

<span data-ttu-id="f5238-105">Teie saidi lehele viitav täielik või absoluutne URL koosneb eraldi osadest.</span><span class="sxs-lookup"><span data-stu-id="f5238-105">The full, or absolute, URL that points to a page on your site consists of distinct parts.</span></span> <span data-ttu-id="f5238-106">Näiteks on URL-il `https://www.contoso.com/en-us/contactus` järgmised osad:</span><span class="sxs-lookup"><span data-stu-id="f5238-106">For example, the URL `https://www.contoso.com/en-us/contactus` has the following parts:</span></span>

- <span data-ttu-id="f5238-107">`https://www.contoso.com` – HTTP-protokoll ja saidi domeen.</span><span class="sxs-lookup"><span data-stu-id="f5238-107">`https://www.contoso.com` – The HTTP protocol and the site's domain.</span></span>
- <span data-ttu-id="f5238-108">`/en-us` – saidi keele tee.</span><span class="sxs-lookup"><span data-stu-id="f5238-108">`/en-us` – The site's language path.</span></span>
- <span data-ttu-id="f5238-109">`/contactus` – suhteline URL lehe **Võtke meiega ühendust** jaoks.</span><span class="sxs-lookup"><span data-stu-id="f5238-109">`/contactus` – The relative URL for the **Contact Us** page.</span></span> <span data-ttu-id="f5238-110">Suhteline URL on tuntud ka kui URL-i *komponent*.</span><span class="sxs-lookup"><span data-stu-id="f5238-110">A relative URL is also known as a URL *slug*.</span></span>

<span data-ttu-id="f5238-111">Oma saidi domeeni ja valikulise keele tee loote saidi seadistamisel.</span><span class="sxs-lookup"><span data-stu-id="f5238-111">You establish your site's domain and optional language path when you set up the site.</span></span> <span data-ttu-id="f5238-112">Saate lisada saidile rohkem domeene ja keelte teesid läbi saidi sätete veebipoodide lehe.</span><span class="sxs-lookup"><span data-stu-id="f5238-112">You can add more domains and language paths to your site through the online stores page in the site's settings.</span></span>

<span data-ttu-id="f5238-113">Lehe URL-i komponent on olemas eraldiseisva üksusena saidi autorluse keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="f5238-113">The URL slug for a page exists as a standalone entity in the site authoring environment.</span></span> <span data-ttu-id="f5238-114">Lehe URL koosneb kahest osast: URL-i komponendi esindav nimi ja teie saidil või välisel saidil olevale lehele osutaja.</span><span class="sxs-lookup"><span data-stu-id="f5238-114">A page URL consists of two parts: a name that represents the URL slug, and a pointer to a page on either your site or an external site.</span></span> <span data-ttu-id="f5238-115">Lehe URL-i saab konfigureerida ka käituma teie saidil või välisel saidil olevale teisele lehele suunajana.</span><span class="sxs-lookup"><span data-stu-id="f5238-115">A page URL can also be configured to act as a redirect to another page on either your site or an external site.</span></span>

## <a name="create-a-page-url"></a><span data-ttu-id="f5238-116">Lehe URL-i loomine</span><span class="sxs-lookup"><span data-stu-id="f5238-116">Create a page URL</span></span>

<span data-ttu-id="f5238-117">Lehe URL-ide loomiseks on kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="f5238-117">There are two ways to create page URLs:</span></span>

- <span data-ttu-id="f5238-118">Automaatselt lehe loomisel</span><span class="sxs-lookup"><span data-stu-id="f5238-118">Automatically, when you create a page</span></span>
- <span data-ttu-id="f5238-119">Käsitsi **URL-ide** lehelt</span><span class="sxs-lookup"><span data-stu-id="f5238-119">Manually, from the **URLs** page</span></span>

### <a name="create-a-page-url-when-you-create-a-page"></a><span data-ttu-id="f5238-120">Lehe loomisel lehe URL-i loomine</span><span class="sxs-lookup"><span data-stu-id="f5238-120">Create a page URL when you create a page</span></span>

<span data-ttu-id="f5238-121">Kui sisestate uue lehe loomisel väljale **URL** nime, luuakse **URL-ide** lehel automaatselt lehe URL, mis sellele lehele suunab.</span><span class="sxs-lookup"><span data-stu-id="f5238-121">If you provide a name in the **URL** field when you create a new page, a page URL that points to that page is automatically created on the **URLs** page.</span></span> <span data-ttu-id="f5238-122">Pärast URL-i ja lehe, millele see suunab, avaldamist, pääsevad saidi kasutajad (teie kliendid) URL-iga seostatud lehele ligi.</span><span class="sxs-lookup"><span data-stu-id="f5238-122">After you publish the URL and the page that it points to, site users (your customers) can access the page that is associated with the URL.</span></span>

> [!NOTE]
> <span data-ttu-id="f5238-123">Kui avaldate URL-i ilma, et avaldaksite lehe, millele see osutab, saavad saidi kasutaja lehe avamise proovimisel tõrke 404.</span><span class="sxs-lookup"><span data-stu-id="f5238-123">If you publish a URL without publishing the page that it points to, site users receive a 404 error when they try to access the page.</span></span> <span data-ttu-id="f5238-124">Kui avaldate lehe ilma, et avaldaksite URL-i, mis sellele osutab, ei ole lehele võimalik URL-i kasutades ligi pääseda.</span><span class="sxs-lookup"><span data-stu-id="f5238-124">If you publish a page without publishing the URL that points to it, the page can't be accessed by using a URL.</span></span>

### <a name="manually-create-a-page-url"></a><span data-ttu-id="f5238-125">Lehe URL-i käsitsi loomine</span><span class="sxs-lookup"><span data-stu-id="f5238-125">Manually create a page URL</span></span>

<span data-ttu-id="f5238-126">Uute lehtede loomisel ei ole lehe URL-i määramine nõutud.</span><span class="sxs-lookup"><span data-stu-id="f5238-126">When you create new pages, you aren't required to specify a page URL.</span></span> <span data-ttu-id="f5238-127">Kui jätate URL-i välja tühjaks, luuakse leht seostamata olekus.</span><span class="sxs-lookup"><span data-stu-id="f5238-127">If you leave the URL field blank, the page is created in an unlinked state.</span></span> <span data-ttu-id="f5238-128">Sel juhul ei pääse kliendid lehele ligi, isegi kui see on avaldatud.</span><span class="sxs-lookup"><span data-stu-id="f5238-128">In this case, customers won't be able to access the page, even if it's published.</span></span> <span data-ttu-id="f5238-129">Lehe kättesaadavaks tegemiseks peate käsitsi looma URL-i ja linkima selle lehega.</span><span class="sxs-lookup"><span data-stu-id="f5238-129">To make the page accessible, you must manually create the URL and link it to the page.</span></span>

<span data-ttu-id="f5238-130">Lehe jaoks käsitsi lehe URL-i loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="f5238-130">To manually create the page URL for a page, follow these steps.</span></span>

1. <span data-ttu-id="f5238-131">Valige lehel **URL-id** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f5238-131">On the **URLs** page, select **New**.</span></span>
1. <span data-ttu-id="f5238-132">Valige saidi leht,mille URL-iga seostada.</span><span class="sxs-lookup"><span data-stu-id="f5238-132">Select the site page to associate with the URL.</span></span>
1. <span data-ttu-id="f5238-133">Sisestage URL-i komponent ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5238-133">Enter the URL slug, and then select **OK**.</span></span>

<span data-ttu-id="f5238-134">Sel hetkel on URL mustandi olekus.</span><span class="sxs-lookup"><span data-stu-id="f5238-134">At this point, the URL is in a draft state.</span></span> <span data-ttu-id="f5238-135">See tuleb avaldada, enne kui saidi kasutajad pääsevad seotud lehele ligi.</span><span class="sxs-lookup"><span data-stu-id="f5238-135">It must be published before site users can access the associated page.</span></span>

## <a name="update-a-page-url"></a><span data-ttu-id="f5238-136">Lehe URL-i värskendamine</span><span class="sxs-lookup"><span data-stu-id="f5238-136">Update a page URL</span></span>

<span data-ttu-id="f5238-137">Lehe URL-i sihtlehe värskendamiseks järgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="f5238-137">To update the target page of a page URL, follow these steps.</span></span>

1. <span data-ttu-id="f5238-138">Valige lehel **URL-id** värskendamiseks URL.</span><span class="sxs-lookup"><span data-stu-id="f5238-138">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="f5238-139">Valige parempoolsel atribuudipaanil sihtlehe välja kõrval kolmikpunkti nupp (**...**).</span><span class="sxs-lookup"><span data-stu-id="f5238-139">In the property pane on the right, select the ellipsis button (**...**) next to the target page field.</span></span>
1. <span data-ttu-id="f5238-140">Valige dialoogiaknas erinev leht ja valige seejärel nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5238-140">In the dialog box, select a different page, and then select **OK**.</span></span>
1. <span data-ttu-id="f5238-141">Salvestage ja avaldage URL.</span><span class="sxs-lookup"><span data-stu-id="f5238-141">Save and publish the URL.</span></span>

## <a name="redirect-a-page-url"></a><span data-ttu-id="f5238-142">Lehe URL-i ümbersuunamine</span><span class="sxs-lookup"><span data-stu-id="f5238-142">Redirect a page URL</span></span>

<span data-ttu-id="f5238-143">Mõnikord võite soovida, et kliendid näeksid konkreetse URL-i taotlemisel erinevat lehte.</span><span class="sxs-lookup"><span data-stu-id="f5238-143">Sometimes, you might want your customers to view a different page when they request a specific URL.</span></span> <span data-ttu-id="f5238-144">Sellisel juhul on sageli parim ja lihtsaim lahendus muuta lehte, kuhu lehe URL osutab.</span><span class="sxs-lookup"><span data-stu-id="f5238-144">In these cases, the best and easiest approach is often to change the page that the page URL points to.</span></span> <span data-ttu-id="f5238-145">Samas võivad teil olla legaalsed põhjused HTTP 301 või 3023 ümbersuunamiste kasutamiseks, et suunata URLi taotlused erinevale URL-ile.</span><span class="sxs-lookup"><span data-stu-id="f5238-145">However, you might have legitimate reasons for using HTTP 301 or 3023 redirects to redirect requests for a URL to a different URL.</span></span>

<span data-ttu-id="f5238-146">URL-i erinevale URL-i ümbersuunamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="f5238-146">To redirect a URL to a different URL, follow these steps.</span></span>

1. <span data-ttu-id="f5238-147">Valige lehel **URL-id** värskendamiseks URL.</span><span class="sxs-lookup"><span data-stu-id="f5238-147">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="f5238-148">Valige paremalt atribuutide paanilt suvand **Ümbersuunamine**.</span><span class="sxs-lookup"><span data-stu-id="f5238-148">In the property pane on the right, select **Redirect**.</span></span>
1. <span data-ttu-id="f5238-149">Valige ümbersuunamise sihtkoht.</span><span class="sxs-lookup"><span data-stu-id="f5238-149">Select a destination for the redirect:</span></span>

    - <span data-ttu-id="f5238-150">Saidi teisele leheküljele osutamiseks valige suvand **Sisemine URL**, valige kolmikpunkti nupp (**...**) ja seejärel valige URL, millele ümber suunata.</span><span class="sxs-lookup"><span data-stu-id="f5238-150">To point to another page on your site, select **Internal URL**, select the ellipsis button (**...**), and then select the URL to redirect to.</span></span>
    - <span data-ttu-id="f5238-151">Välisel saidil olevale lehele osutamiseks valige suvand **Väline URL** ja sisestage seejärel tolle lehekülje täielik URL.</span><span class="sxs-lookup"><span data-stu-id="f5238-151">To point to a page on an external site, select **External URL**, and then enter the full URL for that page.</span></span> <span data-ttu-id="f5238-152">Kaasake kindlasti protokoll.</span><span class="sxs-lookup"><span data-stu-id="f5238-152">Be sure to include the protocol.</span></span> <span data-ttu-id="f5238-153">Sisestage näiteks `https://domain.com/new/page`.</span><span class="sxs-lookup"><span data-stu-id="f5238-153">For example, enter `https://domain.com/new/page`.</span></span> <span data-ttu-id="f5238-154">Kui URL juba suunab ümber sisemisele URL-ile, peate enne välise URL-i sisestamist valima suvandi **Tühjenda valik**.</span><span class="sxs-lookup"><span data-stu-id="f5238-154">If the URL already redirects to an internal URL, you must select **Clear selection** before you can enter an external URL.</span></span>

1. <span data-ttu-id="f5238-155">Valige ümbersuunamise tüüp.</span><span class="sxs-lookup"><span data-stu-id="f5238-155">Select a redirect type:</span></span>

    - <span data-ttu-id="f5238-156">**Püsiv ümbersuunamine (301)** – valige see suvand, kui teate, et teie sisu teisaldatakse jäädavalt ja seda ei saa selle eelmisele URL-ile taastada.</span><span class="sxs-lookup"><span data-stu-id="f5238-156">**Permanent redirect (301)** – Select this option when you know that your content is moving permanently and won't revert to its previous URL.</span></span> <span data-ttu-id="f5238-157">Otsimootorid määravad ümbersuunava URL-i otsimootori optimeerimise (SEO) väärtuseks URL-i väärtuse, mis on ümber suunatud ja värskendavad oma kirjet, et uut URL-i näidata.</span><span class="sxs-lookup"><span data-stu-id="f5238-157">Search engines will assign the search engine optimization (SEO) value of the redirecting URL to the URL that is being redirected to and update their record to show the new URL.</span></span> 
    - <span data-ttu-id="f5238-158">**Ajutine ümbersuunamine (302)** – valige see suvand liikluse ümbersuunamiseks otsingumootorit uuendamata.</span><span class="sxs-lookup"><span data-stu-id="f5238-158">**Temporary redirect (302)** – Select this option to redirect traffic without updating search engines.</span></span> <span data-ttu-id="f5238-159">Seda lähenemist kasutatakse tavaliselt siis, kui sisu naaseb peagi eelmisele URL-ile.</span><span class="sxs-lookup"><span data-stu-id="f5238-159">This approach is typically used if the content will soon revert to its previous URL.</span></span>

1. <span data-ttu-id="f5238-160">Kui olete ümbersuunamise juurutamiseks valmis, salvestage ja avaldage URL.</span><span class="sxs-lookup"><span data-stu-id="f5238-160">When you're ready to implement the redirect, save and publish the URL.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5238-161">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f5238-161">Additional resources</span></span>

[<span data-ttu-id="f5238-162">Saidil navigeerimise kohandamine</span><span class="sxs-lookup"><span data-stu-id="f5238-162">Customize site navigation</span></span>](customize-site-navigation.md)

[<span data-ttu-id="f5238-163">Uue saidilehe lisamine</span><span class="sxs-lookup"><span data-stu-id="f5238-163">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="f5238-164">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f5238-164">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="f5238-165">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="f5238-165">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
