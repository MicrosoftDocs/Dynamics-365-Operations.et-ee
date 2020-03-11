---
title: Hinnangute ja arvustuste konfigureerimine
description: Selles teemas kirjeldatakse, kuidas konfigureerida oma e-kaubanduse saiti, et kuvada rakenduses Microsoft Dynamics 365 Commerce klientide antud hinnanguid ja arvustusi.
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
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
ms.openlocfilehash: edd2082b5d2cafcb955f8e3c7762bcba523ac479
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071562"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="b08f6-103">Hinnangute ja arvustuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b08f6-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b08f6-104">Selles teemas kirjeldatakse, kuidas konfigureerida oma e-kaubanduse saiti, et kuvada rakenduses Microsoft Dynamics 365 Commerce klientide antud hinnanguid ja arvustusi.</span><span class="sxs-lookup"><span data-stu-id="b08f6-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b08f6-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="b08f6-105">Overview</span></span>

<span data-ttu-id="b08f6-106">Hinnangud ja arvustused e-Commerce’i veebisaitidel aitavad klientidel saada toote kohta teavet enne ostuotsuse tegemist, näidates neile, mida teised kliendid nendest toodetest arvavad.</span><span class="sxs-lookup"><span data-stu-id="b08f6-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="b08f6-107">E-kaubanduse veebisaitide jaoks on hinnangud ja arvustused lisaks viis klientidelt toodete kohta tagasiside kogumiseks.</span><span class="sxs-lookup"><span data-stu-id="b08f6-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="b08f6-108">Saidi konfigureerimine hinnangute ja arvustuste kuvamiseks</span><span class="sxs-lookup"><span data-stu-id="b08f6-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="b08f6-109">Hinnangute ja arvustuste konfiguratsiooni väärtused (nt rentniku ID, arvustuse teksti pikkus ja arvustuse pealkirja pikkus) konfigureeritakse saidi tasemel.</span><span class="sxs-lookup"><span data-stu-id="b08f6-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="b08f6-110">Saidi konfigureerimiseks hinnangute ja arvustuste kuvamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b08f6-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="b08f6-111">Avage suvand **Koduleht \> Saidid**.</span><span class="sxs-lookup"><span data-stu-id="b08f6-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="b08f6-112">Valige oma saidi nimi.</span><span class="sxs-lookup"><span data-stu-id="b08f6-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="b08f6-113">Avage **Saidi sätted \> Laiendused**.</span><span class="sxs-lookup"><span data-stu-id="b08f6-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="b08f6-114">Sisestage väljale **Arvustuse teksti max pikkus** arvustuse tekstis sisalduvate tärkide maksimaalne arv (nt **1000**).</span><span class="sxs-lookup"><span data-stu-id="b08f6-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="b08f6-115">Sisestage väljale **Arvustuse pealkirja max pikkus** arvustuse pealkirjas sisalduvate tärkide maksimaalne arv (nt **55**).</span><span class="sxs-lookup"><span data-stu-id="b08f6-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="b08f6-116">Valige suvand **Salvesta ja avalda**.</span><span class="sxs-lookup"><span data-stu-id="b08f6-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="b08f6-117">Järgmisel joonisel on näidatud, kuidas see konfiguratsioon rakenduses Dynamics 365 Commerce välja näeb.</span><span class="sxs-lookup"><span data-stu-id="b08f6-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Saidi konfigureerimine hinnangute ja arvustuste kuvamiseks](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="b08f6-119">Toote hinnangu linkimine PDP arvustuste jaotisega</span><span class="sxs-lookup"><span data-stu-id="b08f6-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="b08f6-120">Toote hinnang kuvatakse PDP ülaosas toote pealkirja all.</span><span class="sxs-lookup"><span data-stu-id="b08f6-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="b08f6-121">Toote hinnangut saab konfigureerida nii, et see on lingitud sama PDP jaotisega **Arvustused**.</span><span class="sxs-lookup"><span data-stu-id="b08f6-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="b08f6-122">Toote hinnangu linkimiseks PDP jaotisega **Arvustused** tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b08f6-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="b08f6-123">Avage PDP mall.</span><span class="sxs-lookup"><span data-stu-id="b08f6-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="b08f6-124">Avage suvand **Ostukasti konteinermooduli sätted**.</span><span class="sxs-lookup"><span data-stu-id="b08f6-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="b08f6-125">Suvandis **Ostukast** valige **Toote hinnangud** ja seejärel valige märkeruut **Link täisarvustuste mooduli klõpsamisele**.</span><span class="sxs-lookup"><span data-stu-id="b08f6-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="b08f6-126">Järgmisel joonisel on näidatud, kuidas see konfiguratsioon rakenduses Dynamics 365 Commerce välja näeb.</span><span class="sxs-lookup"><span data-stu-id="b08f6-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Toote hinnangu linkimine PDP arvustuste jaotisega](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="b08f6-128">Privaatsuse ja poliitika lehe lingi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b08f6-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="b08f6-129">Privaatsuse ja poliitika lehe lingi kommenteerimiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="b08f6-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="b08f6-130">Avage suvand **Koduleht \> Saidid**.</span><span class="sxs-lookup"><span data-stu-id="b08f6-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="b08f6-131">Valige oma saidi nimi.</span><span class="sxs-lookup"><span data-stu-id="b08f6-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="b08f6-132">Avage **Saidi sätted \> Laiendused**.</span><span class="sxs-lookup"><span data-stu-id="b08f6-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="b08f6-133">Vahekaardil **Marsruudid** suvandis **RNR-i privaatsus ja poliitika** valige suvand **Lisa link**</span><span class="sxs-lookup"><span data-stu-id="b08f6-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="b08f6-134">Kui link on juba sisestatud ja soovite selle asendada, valige link.</span><span class="sxs-lookup"><span data-stu-id="b08f6-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="b08f6-135">Dialoogiaknas **Lisa link** valige privaatsuse ja poliitika lehe link ning valige seejärel **OK.**</span><span class="sxs-lookup"><span data-stu-id="b08f6-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="b08f6-136">Valige suvand **Salvesta ja avalda**.</span><span class="sxs-lookup"><span data-stu-id="b08f6-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="b08f6-137">Järgmisel joonisel on näidatud, kuidas see konfiguratsioon rakenduses Dynamics 365 Commerce välja näeb.</span><span class="sxs-lookup"><span data-stu-id="b08f6-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Privaatsuse ja poliitika lehe lingi konfigureerimine](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="b08f6-139">Hinnangute ja arvustuste moodulite konfigureerimine toote üksikasjade lehtedel</span><span class="sxs-lookup"><span data-stu-id="b08f6-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="b08f6-140">Lisateavet toote üksikasjade lehtedel hinnangute ja arvustuste moodulite konfigureerimise kohta vt [Hinnangute ja arvustuste moodulid](ratings-reviews-modules.md).</span><span class="sxs-lookup"><span data-stu-id="b08f6-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b08f6-141">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b08f6-141">Additional resources</span></span>

[<span data-ttu-id="b08f6-142">Hinnangute ja arvustuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="b08f6-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="b08f6-143">Hinnangute ja arvustuste kasutamise valimine</span><span class="sxs-lookup"><span data-stu-id="b08f6-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="b08f6-144">Hinnangute ja arvustuste haldus</span><span class="sxs-lookup"><span data-stu-id="b08f6-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="b08f6-145">Hinnangute ja arvustuste moodulite konfigureerimine toote üksikasjade lehtedel</span><span class="sxs-lookup"><span data-stu-id="b08f6-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="b08f6-146">Toote hinnangute sünkroonimine rakenduses Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="b08f6-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
