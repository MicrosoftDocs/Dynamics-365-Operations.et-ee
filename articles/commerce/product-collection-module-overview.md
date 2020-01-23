---
title: Tootekogumi moodulid
description: See teema annab ülevaate tootekogumi moodulitest rakenduses Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/07/2020
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
ms.openlocfilehash: 31307035014f2fae6146f33bc23e3e06103f82eb
ms.sourcegitcommit: c237123ad94d9418994ac095fbd8634c05a927b1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943259"
---
# <a name="product-collection-modules"></a><span data-ttu-id="e0313-103">Tootekogumi moodulid</span><span class="sxs-lookup"><span data-stu-id="e0313-103">Product collection modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e0313-104">See teema annab ülevaate tootekogumi moodulitest rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e0313-104">This topic provides an overview of product collection modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e0313-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="e0313-105">Overview</span></span>

<span data-ttu-id="e0313-106">Toote tuvastus on esmane tööriist, mida jaemüüjad kasutavad oma klientidega suhtlemiseks e-kaubanduse veebisaidil.</span><span class="sxs-lookup"><span data-stu-id="e0313-106">Product discovery is a primary tool that retailers use to engage with their customers on an e-Commerce website.</span></span> <span data-ttu-id="e0313-107">Tootekogumi moodulid aitavad jaemüüjatel luua meeldejäävaid ostlemise kogemusi, pakkudes intuitiivset visuaalset liidest, mida saab kasutada tootekogumite kiireks loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e0313-107">Product collection modules help retailers build compelling shopping experiences by providing an intuitive visual interface that can be used to quickly author product collections.</span></span>

<span data-ttu-id="e0313-108">Tootekogumi moodulid esindavad füüsilisi tooteid ja teenuseid veebisaidil.</span><span class="sxs-lookup"><span data-stu-id="e0313-108">Product collection modules represent physical products and services on the website.</span></span> <span data-ttu-id="e0313-109">Tootekogumi moodul on tavaliselt seotud üksikasjade lehega, kus kliendid saavad osta toodet või teenust või selle kohta lisateavet lugeda.</span><span class="sxs-lookup"><span data-stu-id="e0313-109">A product collection module is typically linked to a details page where customers can purchase a product or service, or learn more about it.</span></span> 

<span data-ttu-id="e0313-110">Tootekogumite allikad võivad olla järgmised nelja tüüpi loendid.</span><span class="sxs-lookup"><span data-stu-id="e0313-110">The sources for product collections can be lists of the following four types:</span></span>

- <span data-ttu-id="e0313-111">Toodete toimetusloendid, mis on toote või toote loendite puhul rakenduses Dynamics 365 Retail käsitsi määratletud seotud toodetena.</span><span class="sxs-lookup"><span data-stu-id="e0313-111">Editorial lists of products that are manually defined in Dynamics 365 Retail as related products for a product, or product lists</span></span>
- <span data-ttu-id="e0313-112">Algoritmilised loendid, nt uute, enim müüdud või populaarsete toodete loendid</span><span class="sxs-lookup"><span data-stu-id="e0313-112">Algorithmic lists, such as lists of new, best-selling, or trending products</span></span>
- <span data-ttu-id="e0313-113">Soovituste loendid, mis põhinevad arvuti õppimisel</span><span class="sxs-lookup"><span data-stu-id="e0313-113">Recommendation lists that are based on machine learning</span></span>
- <span data-ttu-id="e0313-114">Isikupärastamise loendid, mis toetavad kliendi isikupärastatud tulemusi.</span><span class="sxs-lookup"><span data-stu-id="e0313-114">Personalization lists that support personalized results for a customer.</span></span> <span data-ttu-id="e0313-115">Isikupärastatud tulemuste nägemiseks peavad kliendid olema e-kaubanduse saidile sisse logitud.</span><span class="sxs-lookup"><span data-stu-id="e0313-115">Customers must be signed in to the e-Commerce site to see personalized results.</span></span> <span data-ttu-id="e0313-116">Külaliskasutajad ei näe isikupärastatud tulemusi.</span><span class="sxs-lookup"><span data-stu-id="e0313-116">Guest users don't see personalized results.</span></span> <span data-ttu-id="e0313-117">Kliendid saavad isikupärastamisest loobuda [kontohalduse lehel](account-management.md).</span><span class="sxs-lookup"><span data-stu-id="e0313-117">Customers can opt out of personalization from the [account management page](account-management.md).</span></span>

<span data-ttu-id="e0313-118">Järgmisel joonisel on kujutatud e-kaubanduse saidil kasutatavat erinevat tüüpi tootekogumeid.</span><span class="sxs-lookup"><span data-stu-id="e0313-118">The following illustration shows the different types of product collections being used on an e-Commerce site.</span></span>

![Näide e-kaubanduse saidi erinevatest tootekogumitest](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> <span data-ttu-id="e0313-120">Kasutage alati tootekogumi mooduleid, et näidata sarnast tüüpi toodete gruppi.</span><span class="sxs-lookup"><span data-stu-id="e0313-120">Always use product collection modules to show a group of products of a similar type.</span></span>

## <a name="product-collection-modules-and-types"></a><span data-ttu-id="e0313-121">Tootekogumi moodulid ja tüübid</span><span class="sxs-lookup"><span data-stu-id="e0313-121">Product collection modules and types</span></span>

<span data-ttu-id="e0313-122">Järgmises tabelis kirjeldatakse erinevate tootekogumi moodulite tüüpe rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e0313-122">The following table describes various types of product collection modules in Dynamics 365 Commerce.</span></span>

| <span data-ttu-id="e0313-123">Tootekogumi moodul</span><span class="sxs-lookup"><span data-stu-id="e0313-123">Product collection module</span></span>  | <span data-ttu-id="e0313-124">Tüüp</span><span class="sxs-lookup"><span data-stu-id="e0313-124">Type</span></span> | <span data-ttu-id="e0313-125">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e0313-125">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="e0313-126">Kategooria</span><span class="sxs-lookup"><span data-stu-id="e0313-126">Category</span></span>                   | <span data-ttu-id="e0313-127">Kategooria</span><span class="sxs-lookup"><span data-stu-id="e0313-127">Category</span></span> | <span data-ttu-id="e0313-128">Selles moodulis kuvatakse kategooria toodete loend, mis on määratletud navigeerimiskategooria hierarhia poolt, mille jaemüüja on jaemüügi kanali jaoks loonud.</span><span class="sxs-lookup"><span data-stu-id="e0313-128">This module shows a list of products in a category, as defined by the navigation category hierarchy that the retailer created for a retail channel.</span></span> |
| <span data-ttu-id="e0313-129">Seotud tooted</span><span class="sxs-lookup"><span data-stu-id="e0313-129">Related products</span></span>           | <span data-ttu-id="e0313-130">Kureeritud</span><span class="sxs-lookup"><span data-stu-id="e0313-130">Editorial</span></span> | <span data-ttu-id="e0313-131">See moodul näitab toodete loendit, mida kauba haldur on konfigureerinud seotud toodetena jaemüügis autori valitud seose tüübi jaoks.</span><span class="sxs-lookup"><span data-stu-id="e0313-131">This module shows a list of products that a merchandising manager has configured as related products in Retail, for the relation type that the author has selected.</span></span> |
| <span data-ttu-id="e0313-132">Kureeritud toodete loend</span><span class="sxs-lookup"><span data-stu-id="e0313-132">Curated product lists</span></span>      | <span data-ttu-id="e0313-133">Kureeritud</span><span class="sxs-lookup"><span data-stu-id="e0313-133">Editorial</span></span> | <span data-ttu-id="e0313-134">See moodul kuvab kohandatud loendi, mille kaupmehed ja toimetajad on jaemüügis loonud.</span><span class="sxs-lookup"><span data-stu-id="e0313-134">This module shows custom lists that merchandisers and editors have created in Retail.</span></span> |
| <span data-ttu-id="e0313-135">Uus</span><span class="sxs-lookup"><span data-stu-id="e0313-135">New</span></span>                        | <span data-ttu-id="e0313-136">Algoritmiline</span><span class="sxs-lookup"><span data-stu-id="e0313-136">Algorithmic</span></span> | <span data-ttu-id="e0313-137">See moodul kuvab uusimate toodete loendi, mis on kanalitele ja kataloogidele valitud.</span><span class="sxs-lookup"><span data-stu-id="e0313-137">This module shows a list of the newest products that have been assorted to channels and catalogs.</span></span> <span data-ttu-id="e0313-138">See loend võib kuvada sisselogitud kasutajale isikupärastatud tulemusi, kui saidi autor valib selle suvandi.</span><span class="sxs-lookup"><span data-stu-id="e0313-138">This list can show personalized results for a signed-in user if the site author chooses that option.</span></span> |
| <span data-ttu-id="e0313-139">Enim müüdud</span><span class="sxs-lookup"><span data-stu-id="e0313-139">Best selling</span></span>               | <span data-ttu-id="e0313-140">Algoritmiline</span><span class="sxs-lookup"><span data-stu-id="e0313-140">Algorithmic</span></span> | <span data-ttu-id="e0313-141">See moodul kuvab toodete loendi, mis on järjestatud kõige suurema müügi arvu alusel.</span><span class="sxs-lookup"><span data-stu-id="e0313-141">This module shows a list of products that are ranked by the highest number of sales.</span></span> <span data-ttu-id="e0313-142">See loend võib kuvada sisselogitud kasutajale isikupärastatud tulemusi, kui saidi autor valib selle suvandi.</span><span class="sxs-lookup"><span data-stu-id="e0313-142">This list can show personalized results for a signed-in user if the site author chooses that option.</span></span> |
| <span data-ttu-id="e0313-143">Populaarsed</span><span class="sxs-lookup"><span data-stu-id="e0313-143">Trending</span></span>                   | <span data-ttu-id="e0313-144">Algoritmiline</span><span class="sxs-lookup"><span data-stu-id="e0313-144">Algorithmic</span></span> | <span data-ttu-id="e0313-145">See moodul kuvab antud perioodi kõrgeima jõudlusega toodete loendi.</span><span class="sxs-lookup"><span data-stu-id="e0313-145">This module shows a list of the highest-performing products for a given period.</span></span> <span data-ttu-id="e0313-146">See loend võib kuvada sisselogitud kasutajale isikupärastatud tulemusi, kui saidi autor valib selle suvandi.</span><span class="sxs-lookup"><span data-stu-id="e0313-146">This list can show personalized results for a signed-in user if the site author chooses that option.</span></span> |
| <span data-ttu-id="e0313-147">Kliendid ostavad sageli koos</span><span class="sxs-lookup"><span data-stu-id="e0313-147">Frequently bought together</span></span> | <span data-ttu-id="e0313-148">Tehisintellekt/masina õppimine</span><span class="sxs-lookup"><span data-stu-id="e0313-148">Artificial intelligence/Machine learning</span></span> | <span data-ttu-id="e0313-149">See moodul kasutab masinõpet, et analüüsida tarbija ostumustreid ja soovitada seotud kaupu, mida sageli ostetakse koos valitud tootega.</span><span class="sxs-lookup"><span data-stu-id="e0313-149">This module uses machine learning to analyze consumer purchase patterns and recommend related items that are frequently bought together with a given product.</span></span> <span data-ttu-id="e0313-150">See loend võib kuvada sisselogitud kasutajale isikupärastatud tulemusi, kui saidi autor valib selle suvandi.</span><span class="sxs-lookup"><span data-stu-id="e0313-150">This list can show personalized results for a signed-in user if the site author chooses that option.</span></span> |
| <span data-ttu-id="e0313-151">Inimestele meeldib ka</span><span class="sxs-lookup"><span data-stu-id="e0313-151">People also like</span></span>           | <span data-ttu-id="e0313-152">Tehisintellekt/masina õppimine</span><span class="sxs-lookup"><span data-stu-id="e0313-152">Artificial intelligence/Machine learning</span></span> | <span data-ttu-id="e0313-153">See moodul kasutab masinõpet, et analüüsida tarbija ostumustreid ja soovitada seotud kaupu, mis on seotud valitud tootega.</span><span class="sxs-lookup"><span data-stu-id="e0313-153">This module uses machine learning to analyze consumer purchase patterns and recommend items that are related to a given product.</span></span> <span data-ttu-id="e0313-154">See loend võib kuvada sisselogitud kasutajale isikupärastatud tulemusi, kui saidi autor valib selle suvandi.</span><span class="sxs-lookup"><span data-stu-id="e0313-154">This list can show personalized results for a signed-in user if the site author chooses that option.</span></span> |
| <span data-ttu-id="e0313-155">Valib teile</span><span class="sxs-lookup"><span data-stu-id="e0313-155">Picks for you</span></span>              | <span data-ttu-id="e0313-156">Tehisintellekt/masina õppimine</span><span class="sxs-lookup"><span data-stu-id="e0313-156">Artificial intelligence/Machine learning</span></span> | <span data-ttu-id="e0313-157">See moodul kasutab masinõpet, et analüüsida sisselogitud kasutaja ostumustreid ja pakkuda isikupärastatud soovitusi, mis põhinevad nendel ostumustritel.</span><span class="sxs-lookup"><span data-stu-id="e0313-157">This module uses machine learning to analyze the purchase patterns of the signed-in user and provide personalized recommendations that are based on those purchase patterns.</span></span> <span data-ttu-id="e0313-158">Külalisekasutaja jaoks on see loend ahendatud.</span><span class="sxs-lookup"><span data-stu-id="e0313-158">For a guest user, this list will be collapsed.</span></span> |

## <a name="add-a-product-collection-module-to-a-category-page"></a><span data-ttu-id="e0313-159">Tootekogumi mooduli lisamine kategooria lehele</span><span class="sxs-lookup"><span data-stu-id="e0313-159">Add a product collection module to a category page</span></span>

<span data-ttu-id="e0313-160">Tootekogumi mooduli lisamiseks kategooria lehele järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="e0313-160">To add a product collection module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="e0313-161">Rakenduses Dynamics 365 Commerce, minge saidile ja looge leht, mis kasutab sama malli nagu teie vaikimisi kategooria lehekülg.</span><span class="sxs-lookup"><span data-stu-id="e0313-161">In Dynamics 365 Commerce, go to your site, and create a page that uses the same template as your default category page.</span></span>
1. <span data-ttu-id="e0313-162">Lehe liigenduses valige pesa **Alamjalus**, valige kolmikpunkt nupp (**...**) ja seejärel valige suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="e0313-162">In the page outline, select the **Sub footer** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e0313-163">Dialoogiaknas **Lisa moodul** valige suvand **Konteiner** ja seejärel valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0313-163">In the **Add Module** dialog box, select **Container**, and then select **OK**.</span></span>
1. <span data-ttu-id="e0313-164">Valige konteineri moodulis kolmikpunkt nupp ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="e0313-164">In the container module, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="e0313-165">Dialoogiaknas **Lisa moodul** valige suvand **Tootekogum** ja seejärel valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0313-165">In the **Add Module** dialog box, select **Product collection**, and then select **OK**.</span></span>  
<span data-ttu-id="e0313-166">![Näidistoote kogumi mooduli viisardi voog](./media/productCollectionModule.png)</span><span class="sxs-lookup"><span data-stu-id="e0313-166">![Example product collection module Wizard flow](./media/productCollectionModule.png)</span></span>
1. <span data-ttu-id="e0313-167">Konfigureerige sätted, valides tootekogumi jaoks sobiv andmeallikas ja sisend.</span><span class="sxs-lookup"><span data-stu-id="e0313-167">Configure settings by selecting an appropriate data source and inputs for the product collection.</span></span>
1. <span data-ttu-id="e0313-168">Tootekogumi mooduli atribuutide paanil valige käsk **Lisa tooteloend**.</span><span class="sxs-lookup"><span data-stu-id="e0313-168">In the properties pane for the product collection module, select **Add a product list**.</span></span>
1. <span data-ttu-id="e0313-169">Dialoogiaknas **Vali tooteloendi konfigureerimine** valige loendi tüüp, sisestage kaupade arv ja valige muud loendi tüübi jaoks saadaolevad suvandid.</span><span class="sxs-lookup"><span data-stu-id="e0313-169">In the **Select product list configuration** dialog box, select the type of list, enter the number of items, and select any other options that are available for the list type.</span></span> <span data-ttu-id="e0313-170">Lisateavet loendi tüüpide kohta leiate järgnevast tabelist.</span><span class="sxs-lookup"><span data-stu-id="e0313-170">For more information about list types, see the table that follows.</span></span> 
1. <span data-ttu-id="e0313-171">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0313-171">Select **OK**.</span></span>
1. <span data-ttu-id="e0313-172">Salvestage leht ja registreerige see.</span><span class="sxs-lookup"><span data-stu-id="e0313-172">Save the page, and check it in.</span></span>

<span data-ttu-id="e0313-173">Järgmine tabel näitab loendi tüüpe, mis on saadaval dialoogiaknas **Vali toote loendi konfigureerimine**.</span><span class="sxs-lookup"><span data-stu-id="e0313-173">The following table shows the list types that are available for selection in the **Select product list configuration** dialog box.</span></span>

| <span data-ttu-id="e0313-174">Tüüp</span><span class="sxs-lookup"><span data-stu-id="e0313-174">Type</span></span>                       | <span data-ttu-id="e0313-175">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e0313-175">Description</span></span> | <span data-ttu-id="e0313-176">Kasutus</span><span class="sxs-lookup"><span data-stu-id="e0313-176">Usage</span></span> | <span data-ttu-id="e0313-177">Lehe kontekst</span><span class="sxs-lookup"><span data-stu-id="e0313-177">Page context</span></span> | <span data-ttu-id="e0313-178">Spetsiifiline kontekst</span><span class="sxs-lookup"><span data-stu-id="e0313-178">Specific context</span></span> | <span data-ttu-id="e0313-179">Isikupärastamine</span><span class="sxs-lookup"><span data-stu-id="e0313-179">Personalization</span></span> |
|----------------------------|-------------|-------|--------------|------------------|-----------------|
| <span data-ttu-id="e0313-180">Tooted kategooriate alusel</span><span class="sxs-lookup"><span data-stu-id="e0313-180">Products by category</span></span>       | <span data-ttu-id="e0313-181">Kindlasse kategooriasse kuuluvate toodete loend.</span><span class="sxs-lookup"><span data-stu-id="e0313-181">A list of products that belong to a given category.</span></span> <span data-ttu-id="e0313-182">See kategooria määratakse kas lehekülje kontekstist või autori pakutavast kontekstist.</span><span class="sxs-lookup"><span data-stu-id="e0313-182">This category is determined from either the page context or the context that the author provides.</span></span> | <span data-ttu-id="e0313-183">Seda tüüpi loendit saab kasutada mis tahes lehel (nt avaleht, kategooria leht, turunduse leht või toote üksikasjade leht \[PDP\]), et edendada kindlat tootekategooriat.</span><span class="sxs-lookup"><span data-stu-id="e0313-183">This type of list can be used on any page (for example, a home page, category page, marketing page, or product details page \[PDP\]) to promote a specific category of products.</span></span> | <span data-ttu-id="e0313-184">Lehe konteksti kategooria, kui see on saadaval (nt kategooria leht)</span><span class="sxs-lookup"><span data-stu-id="e0313-184">Category from the page context, where available (for example, a category page)</span></span> | <span data-ttu-id="e0313-185">Autor võib anda loendi konteksti jaoks kindla kategooria.</span><span class="sxs-lookup"><span data-stu-id="e0313-185">The author can provide a specific category as context for the list.</span></span> | <span data-ttu-id="e0313-186">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="e0313-186">Not applicable</span></span> |
| <span data-ttu-id="e0313-187">Seotud tooted</span><span class="sxs-lookup"><span data-stu-id="e0313-187">Related products</span></span>           | <span data-ttu-id="e0313-188">Toodete loend, mille kauba haldaja on konfigureerinud seotud toodetena seoses seose tüübiga jaemüügis.</span><span class="sxs-lookup"><span data-stu-id="e0313-188">A list of products that a merchandising manager has configured as related products for the relation type in Retail.</span></span> | <span data-ttu-id="e0313-189">Seda tüüpi loendit kasutatakse peamiselt PDP-del, kuid seda saab kasutada mis tahes lehel, kui on esitatud ülemtoode.</span><span class="sxs-lookup"><span data-stu-id="e0313-189">This type of list is used primarily on PDPs, but it can be used on any page if a parent product is provided.</span></span> | <span data-ttu-id="e0313-190">Toode lehelt, seose tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="e0313-190">Product from the page, relation type (mandatory)</span></span> | <span data-ttu-id="e0313-191">Toote saab valida valijas ja seose tüüp on kasutusel.</span><span class="sxs-lookup"><span data-stu-id="e0313-191">The product can be selected in the picker, and the relation type is used.</span></span> | <span data-ttu-id="e0313-192">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="e0313-192">Not applicable</span></span> |
| <span data-ttu-id="e0313-193">Kureeritud</span><span class="sxs-lookup"><span data-stu-id="e0313-193">Curated</span></span>                    | <span data-ttu-id="e0313-194">Kohandatud loend, mille kaupmehed ja toimetajad on jaemüügis loonud.</span><span class="sxs-lookup"><span data-stu-id="e0313-194">A custom list that merchandisers and editors have created in Retail.</span></span> | <span data-ttu-id="e0313-195">Rikastage kategooria lehte, kodulehte, kassa ja ostukorvi lehte ja tootelehti.</span><span class="sxs-lookup"><span data-stu-id="e0313-195">Enrich category page, home page, checkout and cart pages, and product pages</span></span> | <span data-ttu-id="e0313-196">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="e0313-196">Not applicable</span></span> | <span data-ttu-id="e0313-197">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="e0313-197">Not applicable</span></span> | <span data-ttu-id="e0313-198">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="e0313-198">Not applicable</span></span> |
| <span data-ttu-id="e0313-199">Algoritmiline</span><span class="sxs-lookup"><span data-stu-id="e0313-199">Algorithmic</span></span>                | <ul><li><span data-ttu-id="e0313-200">**Uus** – uusimate toodete loend, mis on valitud kanalitele ja kataloogidele.</span><span class="sxs-lookup"><span data-stu-id="e0313-200">**New** – A list of the newest products that have been assorted to channels and catalogs.</span></span></li><li><span data-ttu-id="e0313-201">**Enim müüdud** – toodete loend, mis on järjestatud kõige suurema müügi arvu alusel.</span><span class="sxs-lookup"><span data-stu-id="e0313-201">**Best-selling** – A list of products that are ranked by the highest number of sales.</span></span></li><li><span data-ttu-id="e0313-202">**Populaarsed** – antud perioodi kõrgeima jõudlusega toodete loend.</span><span class="sxs-lookup"><span data-stu-id="e0313-202">**Trending** – A list of the highest-performing products for a given period.</span></span></li></ul> | <span data-ttu-id="e0313-203">Koduleht, rikastage kategooria lehte, kassa ja ostukorvi lehti</span><span class="sxs-lookup"><span data-stu-id="e0313-203">Home page, enrich category page, and checkout and cart pages</span></span> | <span data-ttu-id="e0313-204">Lehe konteksti kategooria (nt kategooria leht)</span><span class="sxs-lookup"><span data-stu-id="e0313-204">Category from the page context (for example, a category page)</span></span> | <span data-ttu-id="e0313-205">Saidi autori määratud kategooria</span><span class="sxs-lookup"><span data-stu-id="e0313-205">The category that is determined by the site author</span></span> | <span data-ttu-id="e0313-206">Toetatud</span><span class="sxs-lookup"><span data-stu-id="e0313-206">Supported</span></span> |
| <span data-ttu-id="e0313-207">Kliendid ostavad sageli koos</span><span class="sxs-lookup"><span data-stu-id="e0313-207">Frequently bought together</span></span> | <span data-ttu-id="e0313-208">Loend, mis kasutab masinõpet, et analüüsida tarbija ostumustreid ja soovitada seotud kaupu, mida sageli ostetakse koos valitud tootega.</span><span class="sxs-lookup"><span data-stu-id="e0313-208">A list that uses machine learning to analyze consumer purchase patterns and recommend related items that are frequently bought together with a given product.</span></span> | <span data-ttu-id="e0313-209">See loendi tüüp on kohaldatav ainult ostukorvi lehele.</span><span class="sxs-lookup"><span data-stu-id="e0313-209">This type of list is applicable only to the cart page.</span></span> | <span data-ttu-id="e0313-210">Ostukorv</span><span class="sxs-lookup"><span data-stu-id="e0313-210">Cart</span></span> | <span data-ttu-id="e0313-211">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="e0313-211">Not applicable</span></span> | <span data-ttu-id="e0313-212">Toetatud</span><span class="sxs-lookup"><span data-stu-id="e0313-212">Supported</span></span> |
| <span data-ttu-id="e0313-213">Inimestele meeldib ka</span><span class="sxs-lookup"><span data-stu-id="e0313-213">People also like</span></span>           | <span data-ttu-id="e0313-214">Loend, mis kasutab masina õppimist, et analüüsida tarbija ostumustreid ja soovitada seotud kaupu, mis on seotud valitud tootega.</span><span class="sxs-lookup"><span data-stu-id="e0313-214">A list that uses machine learning to analyze consumer purchase patterns and recommend items that are related to a given product.</span></span> | <span data-ttu-id="e0313-215">Seda loendi tüüpi kasutatakse PDP-del, et kuvada tooted, mida teised kliendid on ostnud.</span><span class="sxs-lookup"><span data-stu-id="e0313-215">This type of list is used on PDPs to show products that other customers have bought.</span></span> | <span data-ttu-id="e0313-216">Toote kontekst lehelt</span><span class="sxs-lookup"><span data-stu-id="e0313-216">Product context from the page</span></span> | <span data-ttu-id="e0313-217">Saidi autori sisestatud toode</span><span class="sxs-lookup"><span data-stu-id="e0313-217">The product that is provided by the site author</span></span> | <span data-ttu-id="e0313-218">Toetatud</span><span class="sxs-lookup"><span data-stu-id="e0313-218">Supported</span></span> |
| <span data-ttu-id="e0313-219">Valib teile</span><span class="sxs-lookup"><span data-stu-id="e0313-219">Picks for you</span></span>              | <span data-ttu-id="e0313-220">Loend, mis kasutab kliendi eelistuste määramiseks masinõpet.</span><span class="sxs-lookup"><span data-stu-id="e0313-220">A list that uses machine learning to determine customer preferences.</span></span> | <span data-ttu-id="e0313-221">Seda tüüpi loendit saab kasutada mis tahes lehel.</span><span class="sxs-lookup"><span data-stu-id="e0313-221">This type of list can be used on any page.</span></span> | <span data-ttu-id="e0313-222">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="e0313-222">Not applicable</span></span>| <span data-ttu-id="e0313-223">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="e0313-223">Not applicable</span></span> | <span data-ttu-id="e0313-224">Toetatud</span><span class="sxs-lookup"><span data-stu-id="e0313-224">Supported</span></span> | 

## <a name="additional-resources"></a><span data-ttu-id="e0313-225">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e0313-225">Additional resources</span></span>

[<span data-ttu-id="e0313-226">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="e0313-226">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e0313-227">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="e0313-227">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="e0313-228">Sisu rikasplokimoodul</span><span class="sxs-lookup"><span data-stu-id="e0313-228">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="e0313-229">Sisupaigutusmoodul</span><span class="sxs-lookup"><span data-stu-id="e0313-229">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="e0313-230">Konteineri moodul</span><span class="sxs-lookup"><span data-stu-id="e0313-230">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="e0313-231">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="e0313-231">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e0313-232">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="e0313-232">Product recommendations overview</span></span>](product-recommendations.md)