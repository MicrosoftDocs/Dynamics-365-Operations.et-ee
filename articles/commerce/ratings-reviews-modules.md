---
title: Hinnangute ja arvustuste moodulid
description: See teema käsitleb hinnangute ja arvustuste mooduleid, mida Microsoft Dynamics 365 Commerce’i toote üksikasjade lehtedel kasutatakse.
author: gvrmohanreddy
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: a243399536fec3f5361104289c38e550bf8b1144
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193278"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="d6ea4-103">Hinnangute ja arvustuste moodulid</span><span class="sxs-lookup"><span data-stu-id="d6ea4-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d6ea4-104">See teema käsitleb hinnangute ja arvustuste mooduleid, mida Microsoft Dynamics 365 Commerce’i toote üksikasjade lehtedel kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d6ea4-105">Hinnangud ja arvustused e-Commerce’i veebisaitidel aitavad klientidel saada toote kohta teavet enne ostuotsuse tegemist ja on lisaks mehhanism toodete kohta kliendi tagasiside kogumiseks.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-105">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="d6ea4-106">Hinnangud kuvatakse tooteloendi lehtedel, kategoorialoendi lehtedel, otsingutulemuste lehtedel ja teistel saidi lehtedel.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-106">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="d6ea4-107">Hinnangute histogrammid ja toodete ülevaated kuvatakse PDP-del.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-107">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="d6ea4-108">Nupu **Kirjuta arvustus** võimaldab klientidel edastada toote kohta hinnanguid ja arvustusi.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-108">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="d6ea4-109">Neid PDP-funktsioone kontrollivad hinnangute ja ülevaadete moodulid.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-109">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="d6ea4-110">Hinnangute ja arvustuste moodulid PDP-des</span><span class="sxs-lookup"><span data-stu-id="d6ea4-110">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="d6ea4-111">PDP-des näitavad hinnangute ja arvustuste kokkuvõtteid kolm moodulit.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-111">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="d6ea4-112">Arvustuse kirjutamise moodul</span><span class="sxs-lookup"><span data-stu-id="d6ea4-112">Write review module</span></span>
- <span data-ttu-id="d6ea4-113">Toote arvustuste loendi moodul</span><span class="sxs-lookup"><span data-stu-id="d6ea4-113">Product reviews list module</span></span>
- <span data-ttu-id="d6ea4-114">Hinnangute histogrammi moodul</span><span class="sxs-lookup"><span data-stu-id="d6ea4-114">Ratings histogram module</span></span>
 
<span data-ttu-id="d6ea4-115">Järgmisel joonisel on näha, kuidas hinnangute ja arvustuste moodulid PDP-s välja näevad.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-115">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Hinnangute ja arvustuste moodulid PDP-s](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="d6ea4-117">Teavet PDP-de mallide ja paigutuste optimeerimise kohta, et saaksite hinnangute ja arvustute moodulite konfiguratsioone jagada e-kaubanduse saidi mitme PDP vahel, vaadake teemat [Mallide ja paigutuste ülevaade](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d6ea4-117">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="d6ea4-118">Järgmisel joonisel on näha, kuidas dialoogiaken **Lisa moodul** esitab rakenduses Dynamics 365 Commerce hinnangute ja arvustuste mooduleid.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-118">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="d6ea4-119">![Mooduli dialoogiakna lisamine](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="d6ea4-119">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="d6ea4-120">Arvustuse kirjutamise moodul</span><span class="sxs-lookup"><span data-stu-id="d6ea4-120">Write review module</span></span>

<span data-ttu-id="d6ea4-121">Arvustuse kirjutamise moodul hõlmab nuppu **Kirjuta arvustus**, mis võimaldab kasutajatel sisse logida, määrata hinnang ja kirjutada toote kohta arvustus.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-121">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="d6ea4-122">See moodul võimaldab lisaks kasutajatel eelnevalt edastatud hinnangut või arvustust redigeerida.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-122">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="d6ea4-123">See moodul kuvatakse tavaliselt PDP-s hinnangute histogrammi ja toote arvustuste loendi moodulite kohal.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-123">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="d6ea4-124">Järgmisel joonisel on kujutatud dialoogiaken **Kirjuta arvustus**, mis kuvatakse siis, kui klient valib suvandi **Kirjuta arvustus**.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-124">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="d6ea4-125">Klient saab seda dialoogiakent kasutada hinnangu ja arvustuse edastamiseks.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-125">The customer can use this dialog box to submit a rating and a review.</span></span>

![Arvustuse kirjutamise dialoogiaken](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="d6ea4-127">Järgmises tabelis on näidatud arvustuse kirjutamise mooduli atribuut, mis tuleb autorluse tööriistas konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-127">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="d6ea4-128">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="d6ea4-128">Property name</span></span> | <span data-ttu-id="d6ea4-129">Väärtus</span><span class="sxs-lookup"><span data-stu-id="d6ea4-129">Value</span></span>        | <span data-ttu-id="d6ea4-130">Atribuudi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d6ea4-130">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="d6ea4-131">Nimi</span><span class="sxs-lookup"><span data-stu-id="d6ea4-131">Name</span></span>          | <span data-ttu-id="d6ea4-132">Arvustuse kirjutamine</span><span class="sxs-lookup"><span data-stu-id="d6ea4-132">Write review</span></span> | <span data-ttu-id="d6ea4-133">Arvustuse kirjutamise mooduli nimi.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-133">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="d6ea4-134">Hinnangute histogrammi moodul</span><span class="sxs-lookup"><span data-stu-id="d6ea4-134">Ratings histogram module</span></span>

<span data-ttu-id="d6ea4-135">Hinnangute histogrammi moodul näitab hinnangute histogrammi.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-135">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="d6ea4-136">See moodul kuvatakse tavaliselt PDP-s arvustuse kirjutamise mooduli ja toote arvustuste loendi mooduli vahel.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-136">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="d6ea4-137">Hinnangute histogrammi moodul ei nõua konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-137">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="d6ea4-138">Peate lihtsalt lisama mooduli PDP mallis.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-138">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="d6ea4-139">Järgmised joonised näitavad, kuidas PDP mall rakenduses Dynamics 365 Commerce välja näeb, kui hinnangute ja arvustuse moodulid on PDP-des kuvamiseks konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-139">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="d6ea4-140">![PDP mall, kui hinnangud ja arvustused on PDP-des kuvamiseks konfigureeritud](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="d6ea4-140">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="d6ea4-141">Toote arvustuste loendi moodul</span><span class="sxs-lookup"><span data-stu-id="d6ea4-141">Product reviews list module</span></span>

<span data-ttu-id="d6ea4-142">Toote arvustuste loendi moodul kuvab toodete arvustuste loendi koos sortimise, filtreerimise ja lehejaotuse valikutega.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-142">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="d6ea4-143">See moodul kuvatakse PDP-s tavaliselt pärast hinnangute histogrammi moodulit</span><span class="sxs-lookup"><span data-stu-id="d6ea4-143">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="d6ea4-144">Järgmises tabelis on näidatud toote arvustuste loendi mooduli atribuudid, mis tuleb autorluse tööriistas konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-144">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="d6ea4-145">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="d6ea4-145">Property name</span></span>              | <span data-ttu-id="d6ea4-146">Väärtus</span><span class="sxs-lookup"><span data-stu-id="d6ea4-146">Value</span></span> | <span data-ttu-id="d6ea4-147">Atribuudi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d6ea4-147">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="d6ea4-148">Igal lehel kuvatavad arvustused</span><span class="sxs-lookup"><span data-stu-id="d6ea4-148">Reviews shown on each page</span></span> | <span data-ttu-id="d6ea4-149">10</span><span class="sxs-lookup"><span data-stu-id="d6ea4-149">10</span></span>    | <span data-ttu-id="d6ea4-150">Arvustuste arv, mida tuleks korraga PDP-s kuvada.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-150">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="d6ea4-151">Nupud **Järgmine** ja **Eelmine** on kaasatud, nii et kasutajad saavad läbi arvustuste lehtede liikuda.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-151">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="d6ea4-152">Hinnangute histogramm – kokkuvõtte vaade</span><span class="sxs-lookup"><span data-stu-id="d6ea4-152">Ratings histogram – Summary view</span></span>

<span data-ttu-id="d6ea4-153">Toote arvustuste loendi moodul sisaldab pesa, kus saate lisada hinnangute histogrammi mooduli.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-153">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="d6ea4-154">Järgmisel joonisel on näidatud, kuidas saate lisada rakenduses Dynamics 365 Commerce hinnangute histogrammi mooduli toote arvustuste loendi moodulile.</span><span class="sxs-lookup"><span data-stu-id="d6ea4-154">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Hinnangute histogrammi mooduli lisamine toote arvustuste loendi moodulis](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="d6ea4-156">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d6ea4-156">Additional resources</span></span>

[<span data-ttu-id="d6ea4-157">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="d6ea4-157">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d6ea4-158">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="d6ea4-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="d6ea4-159">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="d6ea4-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d6ea4-160">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="d6ea4-160">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d6ea4-161">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="d6ea4-161">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d6ea4-162">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="d6ea4-162">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="d6ea4-163">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="d6ea4-163">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]