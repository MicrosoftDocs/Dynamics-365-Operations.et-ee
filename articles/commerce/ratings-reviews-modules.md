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
ms.openlocfilehash: dee9a6a7e2a5278f069958ce00689b1beb9b1bd7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792143"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="b8a55-103">Hinnangute ja arvustuste moodulid</span><span class="sxs-lookup"><span data-stu-id="b8a55-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b8a55-104">See teema käsitleb hinnangute ja arvustuste mooduleid, mida Microsoft Dynamics 365 Commerce’i toote üksikasjade lehtedel kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="b8a55-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b8a55-105">Hinnangud ja arvustused e-Commerce’i veebisaitidel aitavad klientidel saada toote kohta teavet enne ostuotsuse tegemist ja on lisaks mehhanism toodete kohta kliendi tagasiside kogumiseks.</span><span class="sxs-lookup"><span data-stu-id="b8a55-105">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="b8a55-106">Hinnangud kuvatakse tooteloendi lehtedel, kategoorialoendi lehtedel, otsingutulemuste lehtedel ja teistel saidi lehtedel.</span><span class="sxs-lookup"><span data-stu-id="b8a55-106">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="b8a55-107">Hinnangute histogrammid ja toodete ülevaated kuvatakse PDP-del.</span><span class="sxs-lookup"><span data-stu-id="b8a55-107">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="b8a55-108">Nupu **Kirjuta arvustus** võimaldab klientidel edastada toote kohta hinnanguid ja arvustusi.</span><span class="sxs-lookup"><span data-stu-id="b8a55-108">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="b8a55-109">Neid PDP-funktsioone kontrollivad hinnangute ja ülevaadete moodulid.</span><span class="sxs-lookup"><span data-stu-id="b8a55-109">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="b8a55-110">Hinnangute ja arvustuste moodulid PDP-des</span><span class="sxs-lookup"><span data-stu-id="b8a55-110">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="b8a55-111">PDP-des näitavad hinnangute ja arvustuste kokkuvõtteid kolm moodulit.</span><span class="sxs-lookup"><span data-stu-id="b8a55-111">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="b8a55-112">Arvustuse kirjutamise moodul</span><span class="sxs-lookup"><span data-stu-id="b8a55-112">Write review module</span></span>
- <span data-ttu-id="b8a55-113">Toote arvustuste loendi moodul</span><span class="sxs-lookup"><span data-stu-id="b8a55-113">Product reviews list module</span></span>
- <span data-ttu-id="b8a55-114">Hinnangute histogrammi moodul</span><span class="sxs-lookup"><span data-stu-id="b8a55-114">Ratings histogram module</span></span>
 
<span data-ttu-id="b8a55-115">Järgmisel joonisel on näha, kuidas hinnangute ja arvustuste moodulid PDP-s välja näevad.</span><span class="sxs-lookup"><span data-stu-id="b8a55-115">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Hinnangute ja arvustuste moodulid PDP-s](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="b8a55-117">Teavet PDP-de mallide ja paigutuste optimeerimise kohta, et saaksite hinnangute ja arvustute moodulite konfiguratsioone jagada e-kaubanduse saidi mitme PDP vahel, vaadake teemat [Mallide ja paigutuste ülevaade](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b8a55-117">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="b8a55-118">Järgmisel joonisel on näha, kuidas dialoogiaken **Lisa moodul** esitab rakenduses Dynamics 365 Commerce hinnangute ja arvustuste mooduleid.</span><span class="sxs-lookup"><span data-stu-id="b8a55-118">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="b8a55-119">![Mooduli dialoogiakna lisamine](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="b8a55-119">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="b8a55-120">Arvustuse kirjutamise moodul</span><span class="sxs-lookup"><span data-stu-id="b8a55-120">Write review module</span></span>

<span data-ttu-id="b8a55-121">Arvustuse kirjutamise moodul hõlmab nuppu **Kirjuta arvustus**, mis võimaldab kasutajatel sisse logida, määrata hinnang ja kirjutada toote kohta arvustus.</span><span class="sxs-lookup"><span data-stu-id="b8a55-121">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="b8a55-122">See moodul võimaldab lisaks kasutajatel eelnevalt edastatud hinnangut või arvustust redigeerida.</span><span class="sxs-lookup"><span data-stu-id="b8a55-122">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="b8a55-123">See moodul kuvatakse tavaliselt PDP-s hinnangute histogrammi ja toote arvustuste loendi moodulite kohal.</span><span class="sxs-lookup"><span data-stu-id="b8a55-123">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="b8a55-124">Järgmisel joonisel on kujutatud dialoogiaken **Kirjuta arvustus**, mis kuvatakse siis, kui klient valib suvandi **Kirjuta arvustus**.</span><span class="sxs-lookup"><span data-stu-id="b8a55-124">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="b8a55-125">Klient saab seda dialoogiakent kasutada hinnangu ja arvustuse edastamiseks.</span><span class="sxs-lookup"><span data-stu-id="b8a55-125">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="b8a55-126">![Arvustuse kirjutamise dialoogiaken](media/rnr-eCommerce-write-review-module.png) Järgmises tabelis on näidatud arvustuse kirjutamise mooduli atribuut, mis tuleb autorluse tööriistas konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="b8a55-126">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="b8a55-127">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="b8a55-127">Property name</span></span> | <span data-ttu-id="b8a55-128">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b8a55-128">Value</span></span>        | <span data-ttu-id="b8a55-129">Atribuudi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b8a55-129">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="b8a55-130">Nimi</span><span class="sxs-lookup"><span data-stu-id="b8a55-130">Name</span></span>          | <span data-ttu-id="b8a55-131">Arvustuse kirjutamine</span><span class="sxs-lookup"><span data-stu-id="b8a55-131">Write review</span></span> | <span data-ttu-id="b8a55-132">Arvustuse kirjutamise mooduli nimi.</span><span class="sxs-lookup"><span data-stu-id="b8a55-132">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="b8a55-133">Hinnangute histogrammi moodul</span><span class="sxs-lookup"><span data-stu-id="b8a55-133">Ratings histogram module</span></span>

<span data-ttu-id="b8a55-134">Hinnangute histogrammi moodul näitab hinnangute histogrammi.</span><span class="sxs-lookup"><span data-stu-id="b8a55-134">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="b8a55-135">See moodul kuvatakse tavaliselt PDP-s arvustuse kirjutamise mooduli ja toote arvustuste loendi mooduli vahel.</span><span class="sxs-lookup"><span data-stu-id="b8a55-135">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="b8a55-136">Hinnangute histogrammi moodul ei nõua konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="b8a55-136">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="b8a55-137">Peate lihtsalt lisama mooduli PDP mallis.</span><span class="sxs-lookup"><span data-stu-id="b8a55-137">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="b8a55-138">Järgmised joonised näitavad, kuidas PDP mall rakenduses Dynamics 365 Commerce välja näeb, kui hinnangute ja arvustuse moodulid on PDP-des kuvamiseks konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="b8a55-138">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="b8a55-139">![PDP mall, kui hinnangud ja arvustused on PDP-des kuvamiseks konfigureeritud](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="b8a55-139">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="b8a55-140">Toote arvustuste loendi moodul</span><span class="sxs-lookup"><span data-stu-id="b8a55-140">Product reviews list module</span></span>

<span data-ttu-id="b8a55-141">Toote arvustuste loendi moodul kuvab toodete arvustuste loendi koos sortimise, filtreerimise ja lehejaotuse valikutega.</span><span class="sxs-lookup"><span data-stu-id="b8a55-141">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="b8a55-142">See moodul kuvatakse PDP-s tavaliselt pärast hinnangute histogrammi moodulit</span><span class="sxs-lookup"><span data-stu-id="b8a55-142">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="b8a55-143">Järgmises tabelis on näidatud toote arvustuste loendi mooduli atribuudid, mis tuleb autorluse tööriistas konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="b8a55-143">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="b8a55-144">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="b8a55-144">Property name</span></span>              | <span data-ttu-id="b8a55-145">Väärtus</span><span class="sxs-lookup"><span data-stu-id="b8a55-145">Value</span></span> | <span data-ttu-id="b8a55-146">Atribuudi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b8a55-146">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="b8a55-147">Igal lehel kuvatavad arvustused</span><span class="sxs-lookup"><span data-stu-id="b8a55-147">Reviews shown on each page</span></span> | <span data-ttu-id="b8a55-148">10</span><span class="sxs-lookup"><span data-stu-id="b8a55-148">10</span></span>    | <span data-ttu-id="b8a55-149">Arvustuste arv, mida tuleks korraga PDP-s kuvada.</span><span class="sxs-lookup"><span data-stu-id="b8a55-149">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="b8a55-150">Nupud **Järgmine** ja **Eelmine** on kaasatud, nii et kasutajad saavad läbi arvustuste lehtede liikuda.</span><span class="sxs-lookup"><span data-stu-id="b8a55-150">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="b8a55-151">Hinnangute histogramm – kokkuvõtte vaade</span><span class="sxs-lookup"><span data-stu-id="b8a55-151">Ratings histogram – Summary view</span></span>

<span data-ttu-id="b8a55-152">Toote arvustuste loendi moodul sisaldab pesa, kus saate lisada hinnangute histogrammi mooduli.</span><span class="sxs-lookup"><span data-stu-id="b8a55-152">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="b8a55-153">Järgmisel joonisel on näidatud, kuidas saate lisada rakenduses Dynamics 365 Commerce hinnangute histogrammi mooduli toote arvustuste loendi moodulile.</span><span class="sxs-lookup"><span data-stu-id="b8a55-153">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Hinnangute histogrammi mooduli lisamine toote arvustuste loendi moodulis](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="b8a55-155">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b8a55-155">Additional resources</span></span>

[<span data-ttu-id="b8a55-156">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="b8a55-156">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b8a55-157">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="b8a55-157">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b8a55-158">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="b8a55-158">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b8a55-159">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="b8a55-159">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b8a55-160">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="b8a55-160">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b8a55-161">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="b8a55-161">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b8a55-162">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="b8a55-162">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]