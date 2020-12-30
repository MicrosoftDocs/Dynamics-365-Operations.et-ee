---
title: „Sarnaste toodete vaatamise” soovituste lubamine
description: Selles teemas kirjeldatakse, kuidas lubada „sarnaste toodete vaatamise” tootesoovitused rakenduses Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: da957850072e233a41a042d5857f81ddbf178f7a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411747"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="a430e-103">„Sarnaste toodete vaatamise” soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="a430e-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a430e-104">Selles teemas kirjeldatakse, kuidas lubada „sarnaste toodete vaatamise” tootesoovitused rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a430e-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a430e-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="a430e-105">Overview</span></span>

<span data-ttu-id="a430e-106">Rakenduse Dynamics 365 Commerce soovituste funktsioon „sarnaste toodete vaatamine” kasutab tehisintellekti ja masinõpet (AI-ML), et pakkuda klientidele visuaalselt sarnaste toodete soovitusi.</span><span class="sxs-lookup"><span data-stu-id="a430e-106">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="a430e-107">Tehes „sarnaste toodete vaatamise” soovitused kõigis Commerce'i jaemüügikanalites kättesaadavaks, saavad jaemüüjad klientide rahulolu suurendada, aidates klientidel leida lihtsamini, mida nad tahavad.</span><span class="sxs-lookup"><span data-stu-id="a430e-107">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="a430e-108">„Sarnaste toodete vaatamise” soovituste funktsioon kasutab alustootevariante, et leida ja soovitada jaemüüja tootekataloogis visuaalselt sarnaseid tooteid.</span><span class="sxs-lookup"><span data-stu-id="a430e-108">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="a430e-109">„Sarnaste toodete vaatamise” soovitused on saadaval nii kassas (POS) kui ka e-kaubanduses.</span><span class="sxs-lookup"><span data-stu-id="a430e-109">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="a430e-110">Näidisstsenaariumid</span><span class="sxs-lookup"><span data-stu-id="a430e-110">Example scenarios</span></span>

- <span data-ttu-id="a430e-111">Klient vaatab musta triibulist kampsunit ja talle soovitatakse sarnast punast kampsunit.</span><span class="sxs-lookup"><span data-stu-id="a430e-111">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="a430e-112">Klient valib algselt vaadatud toote asemel soovitatud toote ja seejärel soovitatakse talle sarnaseid punast värvi tooteid.</span><span class="sxs-lookup"><span data-stu-id="a430e-112">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="a430e-113">Klient kasutab „sarnaste toodete vaatamise” soovitusi, et avastada kõrvarõngad, mis sobivad sõrmusega, mille ostmisest on klient huvitatud.</span><span class="sxs-lookup"><span data-stu-id="a430e-113">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="a430e-114">„Sarnaste toodete vaatamise” soovituste lubamine Commerce'i peakontoris</span><span class="sxs-lookup"><span data-stu-id="a430e-114">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="a430e-115">Tootesoovitusi toetatakse ainult Commerce'i klientide puhul, kes on hakanud kasutama Azure Data Lake Gen2 salvestusruumi.</span><span class="sxs-lookup"><span data-stu-id="a430e-115">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="a430e-116">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="a430e-116">Prerequisites</span></span>

<span data-ttu-id="a430e-117">Enne kui jaemüüjad saavad hakata näitama klientidele „sarnaste toodete vaatamise” soovitusi, tuleb täita kaks eeltingimust.</span><span class="sxs-lookup"><span data-stu-id="a430e-117">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="a430e-118">[Tootesoovituste lubamine](enable-product-recommendations.md) Commerce'i peakontoris.</span><span class="sxs-lookup"><span data-stu-id="a430e-118">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="a430e-119">Veenduge, et meediaserver toetaks HTTPS-i kutseid.</span><span class="sxs-lookup"><span data-stu-id="a430e-119">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="a430e-120">Et soovitusmootor pääseks juurde tootepiltidele, peavad jaemüüjad looma toote URL-id.</span><span class="sxs-lookup"><span data-stu-id="a430e-120">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="a430e-121">Commerce'i peakontoris toote URL-ide loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a430e-121">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a430e-122">Avage **Tootepildid**.</span><span class="sxs-lookup"><span data-stu-id="a430e-122">Go to **Product images**.</span></span>
1. <span data-ttu-id="a430e-123">Valige toimingupaanil **Meediumimalli määratlemine**.</span><span class="sxs-lookup"><span data-stu-id="a430e-123">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="a430e-124">Valige atribuutide paanil **Meediumimalli määratlemine** jaotisest **Meediumide URL-id** suvand **Loo URL-id**.</span><span class="sxs-lookup"><span data-stu-id="a430e-124">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="a430e-125">Kui lubate „sarnaste toodete vaatamise” soovituste funktsiooni, algab tootesoovituste loendite loomise protsess.</span><span class="sxs-lookup"><span data-stu-id="a430e-125">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="a430e-126">Kuluda võib kuni üks päev enne, kui need loendid on saadaval ja nähtavad veebis ning kassaterminalides.</span><span class="sxs-lookup"><span data-stu-id="a430e-126">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="a430e-127">„Sarnaste toodete vaatamise” soovituste funktsiooni lubamiseks Commerce'i peakontoris toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a430e-127">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a430e-128">Avage **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="a430e-128">Go to **Feature management**.</span></span>
1. <span data-ttu-id="a430e-129">Leidke üles ja valige saadaolevate funktsioonide loendist suvand **Sarnaste toodete vaatamine**.</span><span class="sxs-lookup"><span data-stu-id="a430e-129">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="a430e-130">Valige parempoolsel paanil **Luba**, et teenus sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="a430e-130">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="a430e-131">Järgmisel illustratsioonil on näha funktsioon **Sarnaste toodete vaatamine** Commerce'i peakontori lehel **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="a430e-131">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![Sarnaste toodete vaatamise funktsioon Commerce'i peakontori funktsioonihalduse lehel](./media/enableshopsimilarlooks.png)

<span data-ttu-id="a430e-133">Kui eelmised ülesanded on lõpule viidud, täiendatakse kassaterminale automaatselt kontekstilise paneeliga **Sarnaste toodete ostmine**.</span><span class="sxs-lookup"><span data-stu-id="a430e-133">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="a430e-134">Valides suvandi **Vaata lisa**, saavad kassaterminali kasutajaid avada spetsiaalse „sarnaste toodete vaatamise” lehe, mida saab veelgi filtreerida.</span><span class="sxs-lookup"><span data-stu-id="a430e-134">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="a430e-135">Kui lülitate „sarnaste toodete vaatamise” soovituste funktsiooni välja, ei mõjutata muid tootesoovituste tüüpe.</span><span class="sxs-lookup"><span data-stu-id="a430e-135">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="a430e-136">Lisateavet tootesoovituste kohta leiate teemast [Tootesoovituste ülevaade](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="a430e-136">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="a430e-137">Sarnaste toodete vaatamise nupu lisamine toote üksikasjade lehele Commerce'i saidiehitaja abil</span><span class="sxs-lookup"><span data-stu-id="a430e-137">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="a430e-138">Pärast „sarnaste toodete vaatamise” soovituste funktsiooni lubamist Commerce'i peakontoris saavad jaemüüjad lisada Commerce'i saidiehitaja suvandi abil nupu **Vaata sarnaseid tooteid** mis tahes toote üksikasjade lehel (PDP) olevasse ostkasti.</span><span class="sxs-lookup"><span data-stu-id="a430e-138">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="a430e-139">Klient, kes valib selle nupu, viiakse spetsiaalsele „sarnaste toodete vaatamise” lehele, millel näidatakse visuaalselt sarnaseid tooteid.</span><span class="sxs-lookup"><span data-stu-id="a430e-139">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="a430e-140">Seal saab klient toodete edasiseks filtreerimiseks kasutada suvandeid.</span><span class="sxs-lookup"><span data-stu-id="a430e-140">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="a430e-141">Et lisada nupp **Vaata sarnaseid tooteid** toote üksikasjade lehele Commerce'i saidiehitaja abil toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a430e-141">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="a430e-142">Avage olemasolev saidiehitaja leht, mis sisaldab ostukastimoodulit.</span><span class="sxs-lookup"><span data-stu-id="a430e-142">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="a430e-143">Valige vasakpoolsel navigeerimispaanil ostukastimoodul.</span><span class="sxs-lookup"><span data-stu-id="a430e-143">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="a430e-144">Valige parempoolsel navigeerimispaanil märkeruut **Luba sarnaste toodete vaatamise link**.</span><span class="sxs-lookup"><span data-stu-id="a430e-144">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="a430e-145">Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="a430e-145">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="a430e-146">Pärast lehe avaldamist on PDP-l nupp **Vaata sarnaseid tooteid**.</span><span class="sxs-lookup"><span data-stu-id="a430e-146">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="a430e-147">Järgmisel illustratsioonil on näha saidiehitajas toodete üksikasjade näidislehel märkeruut **Luba sarnaste toodete vaatamise link** ja nupp **Vaata sarnaseid tooteid**.</span><span class="sxs-lookup"><span data-stu-id="a430e-147">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![Saidiehitajas toote üksikasjade lehel olev märkeruut „Luba sarnaste toodete vaatamise link” ja nupp „Vaata sarnaseid tooteid”](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="a430e-149">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a430e-149">Additional resources</span></span>

[<span data-ttu-id="a430e-150">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="a430e-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a430e-151"> Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas</span><span class="sxs-lookup"><span data-stu-id="a430e-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="a430e-152">Luba tootesoovitused</span><span class="sxs-lookup"><span data-stu-id="a430e-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="a430e-153">Isikupärastatud tootesoovitustest loobumine</span><span class="sxs-lookup"><span data-stu-id="a430e-153">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="a430e-154">Tootesoovituste lisamine kassas</span><span class="sxs-lookup"><span data-stu-id="a430e-154">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="a430e-155">Soovituste lisamine kandeekraanile</span><span class="sxs-lookup"><span data-stu-id="a430e-155">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="a430e-156">AI-ML-i soovituste tulemuste kohandamine</span><span class="sxs-lookup"><span data-stu-id="a430e-156">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="a430e-157">Loo kuraatorite soovitused käsitsi</span><span class="sxs-lookup"><span data-stu-id="a430e-157">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="a430e-158">Soovituste loomine demoandmetega</span><span class="sxs-lookup"><span data-stu-id="a430e-158">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="a430e-159">Tootesoovituste KKK</span><span class="sxs-lookup"><span data-stu-id="a430e-159">Product recommendations FAQ</span></span>](faq-recommendations.md)
