---
title: Hinnangute ja arvustuste konfigureerimine
description: Selles teemas kirjeldatakse, kuidas konfigureerida oma e-kaubanduse saiti, et kuvada rakenduses Microsoft Dynamics 365 Commerce klientide antud hinnanguid ja arvustusi.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0612b32e7751b32ad851f627a53bce2ac491870f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770477"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="4836a-103">Hinnangute ja arvustuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="4836a-103">Configure ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="4836a-104">Selles teemas kirjeldatakse, kuidas konfigureerida oma e-kaubanduse saiti, et kuvada rakenduses Microsoft Dynamics 365 Commerce klientide antud hinnanguid ja arvustusi.</span><span class="sxs-lookup"><span data-stu-id="4836a-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4836a-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="4836a-105">Overview</span></span>

<span data-ttu-id="4836a-106">Hinnangud ja ülevaated e-kaubanduse veebisaidil aitavad klientidel saada toote kohta teavet enne ostuotsuse tegemist, näidates neile, mida teised kliendid nendest toodetest arvavad.</span><span class="sxs-lookup"><span data-stu-id="4836a-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, by showing them what other customers think about those products.</span></span> <span data-ttu-id="4836a-107">E-kaubanduse veebisaitide jaoks on hinnangud ja arvustused lisaks viis klientidelt toodete kohta tagasiside kogumiseks.</span><span class="sxs-lookup"><span data-stu-id="4836a-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="4836a-108">Hinnangud kuvatakse tooteloendi lehtedel, kategoorialoendi lehtedel, otsingutulemuste lehtedel ja teistel saidi lehtedel.</span><span class="sxs-lookup"><span data-stu-id="4836a-108">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> <span data-ttu-id="4836a-109">Hinnangute histogrammid ja toodete ülevaated kuvatakse toote üksikasjade lehtedel (PDP-d).</span><span class="sxs-lookup"><span data-stu-id="4836a-109">Ratings histograms and product reviews are shown on product details pages (PDPs).</span></span> <span data-ttu-id="4836a-110">Nupu **Kirjuta arvustus** võimaldab klientidel edastada toote kohta hinnanguid ja arvustusi.</span><span class="sxs-lookup"><span data-stu-id="4836a-110">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="4836a-111">Hinnangute ja arvustuste moodulid PDP-des</span><span class="sxs-lookup"><span data-stu-id="4836a-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="4836a-112">PDP-des näitavad hinnangute ja arvustuste kokkuvõtteid kolm moodulit.</span><span class="sxs-lookup"><span data-stu-id="4836a-112">Three modules show the ratings and reviews summary on PDPs:</span></span>

- <span data-ttu-id="4836a-113">Arvustuse kirjutamise moodul</span><span class="sxs-lookup"><span data-stu-id="4836a-113">Write review module</span></span>
- <span data-ttu-id="4836a-114">Toote arvustuste loendi moodul</span><span class="sxs-lookup"><span data-stu-id="4836a-114">Product reviews list module</span></span>
- <span data-ttu-id="4836a-115">Hinnangute histogrammi moodul</span><span class="sxs-lookup"><span data-stu-id="4836a-115">Ratings histogram module</span></span>
 
<span data-ttu-id="4836a-116">Järgmisel joonisel on näha, kuidas hinnangute ja arvustuste moodulid PDP-s välja näevad.</span><span class="sxs-lookup"><span data-stu-id="4836a-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Hinnangute ja arvustuste moodulid PDP-s](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="4836a-118">Teavet PDP-de mallide ja paigutuste optimeerimise kohta, et saaksite hinnangute ja arvustute moodulite konfiguratsioone jagada e-kaubanduse saidi mitme PDP vahel, vaadake teemat [Mallide ja paigutuste ülevaade](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4836a-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="4836a-119">Järgmisel joonisel on näha, kuidas dialoogiaken **Lisa moodul** esitab rakenduses Dynamics 365 Commerce hinnangute ja arvustuste mooduleid.</span><span class="sxs-lookup"><span data-stu-id="4836a-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>

![Mooduli dialoogiakna lisamine](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a><span data-ttu-id="4836a-121">Arvustuse kirjutamise moodul</span><span class="sxs-lookup"><span data-stu-id="4836a-121">Write review module</span></span>

<span data-ttu-id="4836a-122">Arvustuse kirjutamise moodul hõlmab nuppu **Kirjuta arvustus**, mis võimaldab kasutajatel sisse logida, määrata hinnang ja kirjutada toote kohta arvustus.</span><span class="sxs-lookup"><span data-stu-id="4836a-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="4836a-123">See moodul võimaldab lisaks kasutajatel eelnevalt edastatud hinnangut või arvustust redigeerida.</span><span class="sxs-lookup"><span data-stu-id="4836a-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="4836a-124">See moodul kuvatakse tavaliselt PDP-s hinnangute histogrammi ja toote arvustuste loendi moodulite kohal.</span><span class="sxs-lookup"><span data-stu-id="4836a-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>

<span data-ttu-id="4836a-125">Järgmisel joonisel on kujutatud dialoogiaken **Kirjuta arvustus**, mis kuvatakse siis, kui klient valib suvandi **Kirjuta arvustus**.</span><span class="sxs-lookup"><span data-stu-id="4836a-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="4836a-126">Klient saab seda dialoogiakent kasutada hinnangu ja arvustuse edastamiseks.</span><span class="sxs-lookup"><span data-stu-id="4836a-126">The customer can use this dialog box to submit a rating and a review.</span></span>

![Arvustuse kirjutamise dialoogiaken](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="4836a-128">Järgmises tabelis on näidatud arvustuse kirjutamise mooduli atribuut, mis tuleb autorluse tööriistas konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="4836a-128">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="4836a-129">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="4836a-129">Property name</span></span> | <span data-ttu-id="4836a-130">Väärtus</span><span class="sxs-lookup"><span data-stu-id="4836a-130">Value</span></span>        | <span data-ttu-id="4836a-131">Atribuudi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="4836a-131">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="4836a-132">Nimi</span><span class="sxs-lookup"><span data-stu-id="4836a-132">Name</span></span>          | <span data-ttu-id="4836a-133">Arvustuse kirjutamine</span><span class="sxs-lookup"><span data-stu-id="4836a-133">Write review</span></span> | <span data-ttu-id="4836a-134">Arvustuse kirjutamise mooduli nimi.</span><span class="sxs-lookup"><span data-stu-id="4836a-134">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="4836a-135">Hinnangute histogrammi moodul</span><span class="sxs-lookup"><span data-stu-id="4836a-135">Ratings histogram module</span></span>

<span data-ttu-id="4836a-136">Hinnangute histogrammi moodul näitab hinnangute histogrammi.</span><span class="sxs-lookup"><span data-stu-id="4836a-136">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="4836a-137">See moodul kuvatakse tavaliselt PDP-s arvustuse kirjutamise mooduli ja toote arvustuste loendi mooduli vahel.</span><span class="sxs-lookup"><span data-stu-id="4836a-137">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>

<span data-ttu-id="4836a-138">Hinnangute histogrammi moodul ei nõua konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="4836a-138">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="4836a-139">Peate lihtsalt lisama mooduli PDP mallis.</span><span class="sxs-lookup"><span data-stu-id="4836a-139">You just have to add the module in the PDP template.</span></span> 

<span data-ttu-id="4836a-140">Järgmised joonised näitavad, kuidas PDP mall rakenduses Dynamics 365 Commerce välja näeb, kui hinnangute ja arvustuse moodulid on PDP-des kuvamiseks konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="4836a-140">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>

![PDP mall, kui hinnangud ja arvustused on PDP-des kuvamiseks konfigureeritud](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a><span data-ttu-id="4836a-142">Toote arvustuste loendi moodul</span><span class="sxs-lookup"><span data-stu-id="4836a-142">Product reviews list module</span></span>

<span data-ttu-id="4836a-143">Toote arvustuste loendi moodul kuvab toodete arvustuste loendi koos sortimise, filtreerimise ja lehejaotuse valikutega.</span><span class="sxs-lookup"><span data-stu-id="4836a-143">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="4836a-144">See moodul kuvatakse PDP-s tavaliselt pärast hinnangute histogrammi moodulit</span><span class="sxs-lookup"><span data-stu-id="4836a-144">This module typically appears after the ratings histogram module on a PDP.</span></span>

<span data-ttu-id="4836a-145">Järgmises tabelis on näidatud toote arvustuste loendi mooduli atribuudid, mis tuleb autorluse tööriistas konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="4836a-145">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="4836a-146">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="4836a-146">Property name</span></span>              | <span data-ttu-id="4836a-147">Väärtus</span><span class="sxs-lookup"><span data-stu-id="4836a-147">Value</span></span> | <span data-ttu-id="4836a-148">Atribuudi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="4836a-148">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="4836a-149">Igal lehel kuvatavad arvustused</span><span class="sxs-lookup"><span data-stu-id="4836a-149">Reviews shown on each page</span></span> | <span data-ttu-id="4836a-150">10</span><span class="sxs-lookup"><span data-stu-id="4836a-150">10</span></span>    | <span data-ttu-id="4836a-151">Arvustuste arv, mida tuleks korraga PDP-s kuvada.</span><span class="sxs-lookup"><span data-stu-id="4836a-151">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="4836a-152">Nupud **Järgmine** ja **Eelmine** on kaasatud, nii et kasutajad saavad läbi arvustuste lehtede liikuda.</span><span class="sxs-lookup"><span data-stu-id="4836a-152">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="4836a-153">Hinnangute histogramm – kokkuvõtte vaade</span><span class="sxs-lookup"><span data-stu-id="4836a-153">Ratings histogram – Summary view</span></span>

<span data-ttu-id="4836a-154">Toote arvustuste loendi moodul sisaldab pesa, kus saate lisada hinnangute histogrammi mooduli.</span><span class="sxs-lookup"><span data-stu-id="4836a-154">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="4836a-155">Järgmisel joonisel on näidatud, kuidas saate lisada rakenduses Dynamics 365 Commerce hinnangute histogrammi mooduli toote arvustuste loendi moodulile.</span><span class="sxs-lookup"><span data-stu-id="4836a-155">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Hinnangute histogrammi mooduli lisamine toote arvustuste loendi moodulis](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="4836a-157">Saidi konfigureerimine hinnangute ja arvustuste kuvamiseks</span><span class="sxs-lookup"><span data-stu-id="4836a-157">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="4836a-158">Hinnangute ja arvustuste konfiguratsiooni väärtused (nt rentniku ID, arvustuse teksti pikkus ja arvustuse pealkirja pikkus) konfigureeritakse saidi tasemel.</span><span class="sxs-lookup"><span data-stu-id="4836a-158">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="4836a-159">Saidi konfigureerimiseks hinnangute ja arvustuste kuvamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4836a-159">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="4836a-160">Avage suvand **Koduleht \> Saidid**.</span><span class="sxs-lookup"><span data-stu-id="4836a-160">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="4836a-161">Valige oma saidi nimi.</span><span class="sxs-lookup"><span data-stu-id="4836a-161">Select the name of your site.</span></span> 
1. <span data-ttu-id="4836a-162">Avage suvand **Saidi haldus \> Laiendatavus**.</span><span class="sxs-lookup"><span data-stu-id="4836a-162">Go to **Site management \> Extensibility**.</span></span> 
1. <span data-ttu-id="4836a-163">Sisestage väljale **Arvustuse teksti max pikkus** arvustuse tekstis sisalduvate tärkide maksimaalne arv (nt **1000**).</span><span class="sxs-lookup"><span data-stu-id="4836a-163">In the **Review Text Max Length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="4836a-164">Sisestage väljale **Arvustuse pealkirja max pikkus** arvustuse pealkirjas sisalduvate tärkide maksimaalne arv (nt **55**).</span><span class="sxs-lookup"><span data-stu-id="4836a-164">In the **Review Title Max Length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="4836a-165">Valige suvand **Salvesta ja avalda**.</span><span class="sxs-lookup"><span data-stu-id="4836a-165">Select **Save and Publish**.</span></span> 

<span data-ttu-id="4836a-166">Järgmisel joonisel on näidatud, kuidas see konfiguratsioon rakenduses Dynamics 365 Commerce välja näeb.</span><span class="sxs-lookup"><span data-stu-id="4836a-166">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Saidi konfigureerimine hinnangute ja arvustuste kuvamiseks](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="4836a-168">Toote hinnangu linkimine PDP arvustuste jaotisega</span><span class="sxs-lookup"><span data-stu-id="4836a-168">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="4836a-169">Toote hinnang kuvatakse PDP ülaosas toote pealkirja all.</span><span class="sxs-lookup"><span data-stu-id="4836a-169">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="4836a-170">Toote hinnangut saab konfigureerida nii, et see on lingitud sama PDP jaotisega **Arvustused**.</span><span class="sxs-lookup"><span data-stu-id="4836a-170">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="4836a-171">Toote hinnangu linkimiseks PDP jaotisega **Arvustused** tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="4836a-171">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="4836a-172">Avage PDP mall.</span><span class="sxs-lookup"><span data-stu-id="4836a-172">Open the PDP template.</span></span> 
1. <span data-ttu-id="4836a-173">Avage suvand **Ostukasti konteinermooduli sätted**.</span><span class="sxs-lookup"><span data-stu-id="4836a-173">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="4836a-174">Suvandis **Ostukast** valige **Toote hinnangud** ja seejärel valige märkeruut **Link täisarvustuste mooduli klõpsamisele**.</span><span class="sxs-lookup"><span data-stu-id="4836a-174">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="4836a-175">Järgmisel joonisel on näidatud, kuidas see konfiguratsioon rakenduses Dynamics 365 Commerce välja näeb.</span><span class="sxs-lookup"><span data-stu-id="4836a-175">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Toote hinnangu linkimine PDP arvustuste jaotisega](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="4836a-177">Privaatsuse ja poliitika lehe lingi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="4836a-177">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="4836a-178">Privaatsuse ja poliitika lehe lingi kommenteerimiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="4836a-178">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="4836a-179">Avage suvand **Koduleht \> Saidid**.</span><span class="sxs-lookup"><span data-stu-id="4836a-179">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="4836a-180">Valige oma saidi nimi.</span><span class="sxs-lookup"><span data-stu-id="4836a-180">Select the name of your site.</span></span> 
1. <span data-ttu-id="4836a-181">Avage suvand **Saidi haldus \> Laiendatavus**</span><span class="sxs-lookup"><span data-stu-id="4836a-181">Go to **Site management \> Extensibility**</span></span>
1. <span data-ttu-id="4836a-182">Vahekaardil **Marsruudid** suvandis **RNR-i privaatsus ja poliitika** valige suvand **Lisa link**</span><span class="sxs-lookup"><span data-stu-id="4836a-182">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="4836a-183">Kui link on juba sisestatud ja soovite selle asendada, valige link.</span><span class="sxs-lookup"><span data-stu-id="4836a-183">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="4836a-184">Dialoogiaknas **Lisa link** valige privaatsuse ja poliitika lehe link ning valige seejärel **OK.**</span><span class="sxs-lookup"><span data-stu-id="4836a-184">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="4836a-185">Valige suvand **Salvesta ja avalda**.</span><span class="sxs-lookup"><span data-stu-id="4836a-185">Select **Save and Publish**.</span></span> 

<span data-ttu-id="4836a-186">Järgmisel joonisel on näidatud, kuidas see konfiguratsioon rakenduses Dynamics 365 Commerce välja näeb.</span><span class="sxs-lookup"><span data-stu-id="4836a-186">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Privaatsuse ja poliitika lehe lingi konfigureerimine](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a><span data-ttu-id="4836a-188">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4836a-188">Additional resources</span></span>

[<span data-ttu-id="4836a-189">Hinnangute ja arvustuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="4836a-189">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="4836a-190">Hinnangute ja arvustuste kasutamise valimine</span><span class="sxs-lookup"><span data-stu-id="4836a-190">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="4836a-191">Hinnangute ja arvustuste haldus</span><span class="sxs-lookup"><span data-stu-id="4836a-191">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="4836a-192">Toote hinnangute sünkroonimine rakenduses Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="4836a-192">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
