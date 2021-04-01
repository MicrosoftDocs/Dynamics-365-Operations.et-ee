---
title: Luba "osta sarnase kirjeldusega" soovitused
description: Selles teemas kirjeldatakse, kuidas lubada „osta sarnase kirjeldusega” tootesoovitused rakenduses Microsoft Dynamics 365 Commerce.
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b6b397b1f21e3dfcdb4a2b7fe67ddb541d090a97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234385"
---
# <a name="enable-shop-similar-description-recommendations"></a><span data-ttu-id="8e773-103">Luba "osta sarnaseid kirjeldusi" soovitused</span><span class="sxs-lookup"><span data-stu-id="8e773-103">Enable "shop similar description" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8e773-104">Selles teemas kirjeldatakse, kuidas lubada „osta sarnase kirjeldusega” tootesoovitused rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8e773-104">This topic describes how to enable "shop similar description" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8e773-105">Rakenduse Dynamics 365 Commerce soovituste funktsioon „osta sarnase kirjeldusega” kasutab tehisintellekti ja masinõpet (AI-ML), et pakkuda klientidele sarnaste kirjeldustega tooteid, nagu need, mida klient otsib.</span><span class="sxs-lookup"><span data-stu-id="8e773-105">The "shop similar description" recommendations feature in Dynamics 365 Commerce uses artificial intelligence and machine learning (AI-ML) to deliver recommendations for products that have descriptions that are similar to what the customer is looking for.</span></span> <span data-ttu-id="8e773-106">Tehes „osta sarnaste kirjeldustega” soovitused kõigis Commerce'i jaemüügikanalites kättesaadavaks, saavad jaemüüjad aidata klientidel lihtsamini leida seda, mida nad soovivad.</span><span class="sxs-lookup"><span data-stu-id="8e773-106">By making "shop similar description" recommendations available for all retail channels in Commerce, retailers can help customers easily find what they want.</span></span>

<span data-ttu-id="8e773-107">„Osta sarnase kirjeldusega” funktsionaalsuse soovituse kasutavad toote nime ja kirjeldust, et leida ja soovitada sarnaseid tooteid jaemüüja tootekataloogist.</span><span class="sxs-lookup"><span data-stu-id="8e773-107">The functionality for "shop similar description" recommendations uses the product name and description of seed products to find and recommend similar products in a retailer's product catalog.</span></span>

<span data-ttu-id="8e773-108">„Osta sarnase kirjeldusega” soovitused on saadaval nii kassas (POS) kui ka e-kaubanduse kogemustes.</span><span class="sxs-lookup"><span data-stu-id="8e773-108">"Shop similar description" recommendations are available in both the point of sale (POS) and e-commerce experiences.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="8e773-109">Näidisstsenaariumid</span><span class="sxs-lookup"><span data-stu-id="8e773-109">Example scenarios</span></span>

<span data-ttu-id="8e773-110">Järgmine näitestsenaarium näitab soovituste tüüpe, mida funktsiooniga "osta sarnase kirjeldusega" saab pakkuda.</span><span class="sxs-lookup"><span data-stu-id="8e773-110">The following example scenarios show the types of recommendations that the "shop similar description" functionality can provide:</span></span>

- <span data-ttu-id="8e773-111">Klient vaatab retrostiilis sarvraamidega prille ja saab jaemüüja tööstusharude kontekstis teiste prillide soovitusi, millel on sarnane disain.</span><span class="sxs-lookup"><span data-stu-id="8e773-111">A customer views a pair of retro-style horn-rimmed glasses and receives a set of recommendations for other glasses that have a similar design, in the context of the retailer's industry.</span></span>
- <span data-ttu-id="8e773-112">Klient kasutab soovitust "osta sarnase kirjeldusega", et avastada kohvimaitseid, mis on sarnased varem sellelt jaemüüjalt ostetud maitsele.</span><span class="sxs-lookup"><span data-stu-id="8e773-112">A customer uses "shop similar description" recommendations to discover coffee flavors that are similar to a flavor that they previously purchased from the retailer.</span></span>

## <a name="set-up-shop-similar-description-recommendations"></a><span data-ttu-id="8e773-113">Soovituste "osta sarnase kirjeldusega" seadistamine</span><span class="sxs-lookup"><span data-stu-id="8e773-113">Set up "shop similar description" recommendations</span></span>

<span data-ttu-id="8e773-114">Tootesoovitusi toetatakse ainult Commerce'i klientide puhul, kes on hakanud kasutama Azure Data Lake Storage Gen2 salvestusruumi.</span><span class="sxs-lookup"><span data-stu-id="8e773-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Storage Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="8e773-115">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="8e773-115">Prerequisites</span></span>

<span data-ttu-id="8e773-116">Enne soovituste "osta sarnase kirjeldusega" kuvamist klientidele peate täitma järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="8e773-116">Before "shop similar description" recommendations can be shown to customers, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="8e773-117">[Tootesoovituste lubamine](enable-product-recommendations.md) Commerce'i peakontoris.</span><span class="sxs-lookup"><span data-stu-id="8e773-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="8e773-118">Veenduge, et meediaserver toetaks HTTPS-i kutseid.</span><span class="sxs-lookup"><span data-stu-id="8e773-118">Confirm that the media server supports HTTPS calls.</span></span>

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a><span data-ttu-id="8e773-119">Soovituste "osta sarnase kirjeldusega" funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="8e773-119">Turn on the "shop similar description" recommendations feature</span></span>

<span data-ttu-id="8e773-120">„Osta sarnase kirjeldusega” soovituste funktsiooni lubamiseks Commerce'i peakontoris toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="8e773-120">To turn on the "shop similar description" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="8e773-121">Otsige ja valige tööruumi **Funktsioonihaldus** saadaolevate funktsioonide loendist **Osta sarnase kirjeldusega**.</span><span class="sxs-lookup"><span data-stu-id="8e773-121">In the **Feature management** workspace, in the list of available features, search for and select **Shop similar description**.</span></span>
1. <span data-ttu-id="8e773-122">Valige parempoolselt paanilt **Luba**.</span><span class="sxs-lookup"><span data-stu-id="8e773-122">In the right pane, select **Enable**.</span></span>

> [!NOTE]
> <span data-ttu-id="8e773-123">Kui lülitate funktsiooni sisse, hakkab süsteem looma tootesoovituste loendeid.</span><span class="sxs-lookup"><span data-stu-id="8e773-123">When you turn on the feature, the system starts to generate product recommendation lists.</span></span> <span data-ttu-id="8e773-124">Kuluda võib kuni üks päev enne, kui need loendid on saadaval ja nähtavad veebis ning kassaterminalides.</span><span class="sxs-lookup"><span data-stu-id="8e773-124">It might take up to a day for those lists to become available and visible online and on POS terminals.</span></span>
>
> <span data-ttu-id="8e773-125">Kui lülitate selle funktsiooni välja, siis teist tüüpi tootesoovitusi see ei mõjutata.</span><span class="sxs-lookup"><span data-stu-id="8e773-125">If you turn off the feature, other types of product recommendations aren't affected.</span></span> <span data-ttu-id="8e773-126">Lisateavet tootesoovituste kohta leiate teemast [Tootesoovituste ülevaade](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="8e773-126">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a><span data-ttu-id="8e773-127">Nupu Osta sarnase kirjeldusega lisamine toote üksikasjade lehtedele</span><span class="sxs-lookup"><span data-stu-id="8e773-127">Add a Shop similar description button to product details pages</span></span>

<span data-ttu-id="8e773-128">Pärast „Osta sarnase kirjeldusega” soovituste funktsiooni lubamist Commerce'i peakontoris saate mistahes toote üksikasjade lehele (DPD) lisada nupu **Osta sarnase kirjeldusega**.</span><span class="sxs-lookup"><span data-stu-id="8e773-128">After you turn on the "shop similar description" recommendations feature in Commerce headquarters, you can add a **Shop similar description** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="8e773-129">Klient, kes valib selle nupu, viiakse spetsiaalsele **Osta sarnase kirjeldusega** lehele, millel näidatakse visuaalselt sarnaseid tooteid.</span><span class="sxs-lookup"><span data-stu-id="8e773-129">A customer who selects this button is taken to a dedicated **Shop similar description** page that shows visually similar products.</span></span> <span data-ttu-id="8e773-130">Seal saab klient toodete edasiseks filtreerimiseks kasutada suvandeid.</span><span class="sxs-lookup"><span data-stu-id="8e773-130">The customer can then use selectors to further filter the products.</span></span>

<span data-ttu-id="8e773-131">Et lisada nupp **Osta sarnase kirjeldusega** toote üksikasjade lehele Commerce'i saidiehitaja abil toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="8e773-131">To add a **Shop similar description** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="8e773-132">Avage olemasolev saidiehitaja leht, mis sisaldab ostukastimoodulit.</span><span class="sxs-lookup"><span data-stu-id="8e773-132">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="8e773-133">Valige vasakpoolsel navigeerimispaanil ostukastimoodul.</span><span class="sxs-lookup"><span data-stu-id="8e773-133">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="8e773-134">Valige parempoolsel navigeerimispaanil märkeruut **Luba link Osta sarnase kirjeldusega**.</span><span class="sxs-lookup"><span data-stu-id="8e773-134">In the right pane, select the **Enable Shop Similar description Link** check box.</span></span>
1. <span data-ttu-id="8e773-135">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="8e773-135">Select **Save**.</span></span>
1. <span data-ttu-id="8e773-136">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="8e773-136">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="8e773-137">Pärast lehe avaldamist on PDP-l nupp **Osta sarnase kirjeldusega**.</span><span class="sxs-lookup"><span data-stu-id="8e773-137">After the page is published, the PDP will include a **Shop similar description** button.</span></span>

<span data-ttu-id="8e773-138">Järgmisel illustratsioonil on näha saidiehitajas toodete üksikasjade näidislehel märkeruut **Luba link Osta sarnase kirjeldusega** ja nupp **Osta sarnase kirjeldusega**.</span><span class="sxs-lookup"><span data-stu-id="8e773-138">The following illustration shows the **Enable shop similar description Link** check box and the **Shop similar description** button on an example PDP in site builder.</span></span>

![Lingi märkeruut Luba link Osta sarnase kirjeldusega ja nupp Osta sarnase kirjeldusega saidiehitaja DPD-s](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a><span data-ttu-id="8e773-140">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="8e773-140">Additional resources</span></span>

[<span data-ttu-id="8e773-141">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="8e773-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="8e773-142">Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas</span><span class="sxs-lookup"><span data-stu-id="8e773-142">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="8e773-143">Luba tootesoovitused</span><span class="sxs-lookup"><span data-stu-id="8e773-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="8e773-144">Luba "osta sarnaseid" soovitused</span><span class="sxs-lookup"><span data-stu-id="8e773-144">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="8e773-145">AI-ML-i soovituste tulemuste kohandamine</span><span class="sxs-lookup"><span data-stu-id="8e773-145">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="8e773-146">Loo kuraatorite soovitused käsitsi</span><span class="sxs-lookup"><span data-stu-id="8e773-146">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="8e773-147">Tootesoovituste KKK</span><span class="sxs-lookup"><span data-stu-id="8e773-147">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]