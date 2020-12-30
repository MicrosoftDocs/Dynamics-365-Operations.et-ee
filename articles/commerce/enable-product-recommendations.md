---
title: Tootesoovituste lubamine
description: Selles teemas selgitatakse, kuidas teha tehisintellekti masinõppel (AI-ML) põhinevad tootesoovitused rakenduses Microsoft Dynamics 365 Commerce klientidele kättesaadavaks.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b201e5481cfaf5bb6cd64a89cdb6b5a91f31447f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411557"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="1d58f-103">Tootesoovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="1d58f-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1d58f-104">Selles teemas selgitatakse, kuidas teha tehisintellekti masinõppel (AI-ML) põhinevad tootesoovitused rakenduses Microsoft Dynamics 365 Commerce klientidele kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="1d58f-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="1d58f-105">Lisateavet tootesoovituste funktsioonide kohta leiate jaotisest [Ülevaade tootesoovitustest](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="1d58f-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="1d58f-106">Tootesoovituste eelkontroll</span><span class="sxs-lookup"><span data-stu-id="1d58f-106">Recommendations pre-check</span></span>

<span data-ttu-id="1d58f-107">Enne lubamist võtke arvesse, et tootesoovitusi toetatakse ainult Commerce'i klientide jaoks, kes on migreerinud salvestusruumi kasutama rakenduses Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="1d58f-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage.</span></span> 

<span data-ttu-id="1d58f-108">Enne soovituste lubamist tuleb kontoris lubada järgmised konfiguratsioonid:</span><span class="sxs-lookup"><span data-stu-id="1d58f-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="1d58f-109">Veenduge, et Azure Data Lake Storage oleks ostetud ja keskkonnas edukalt kontrollitud.</span><span class="sxs-lookup"><span data-stu-id="1d58f-109">Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="1d58f-110">Lisateabe saamiseks vt [Veenduge, et Azure Data Lake Storage oleks ostetud ja keskkonnas edukalt kontrollitud](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="1d58f-110">For more information, see [Ensure that Azure Data Lake Storage has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="1d58f-111">Veenduge, et üksuse kaupluse värskendamine oleks automatiseeritud.</span><span class="sxs-lookup"><span data-stu-id="1d58f-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="1d58f-112">Lisateabe saamiseks vt [Veenduge, et üksuse kaupluse värskendamine oleks automatiseeritud](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="1d58f-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="1d58f-113">Kinnitage, et Azure AD identiteedi konfiguratsioon sisaldab kirjet üksuse Soovitused jaoks.</span><span class="sxs-lookup"><span data-stu-id="1d58f-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="1d58f-114">Lisateavet selle tegevuse kohta leiate altpoolt.</span><span class="sxs-lookup"><span data-stu-id="1d58f-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="1d58f-115">Lisaks veenduge, et RetailSale’i mõõtmised oleksid lubatud.</span><span class="sxs-lookup"><span data-stu-id="1d58f-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="1d58f-116">Selle seadistamisprotsessi kohta lisateabe saamiseks vt [Mõõtudega töötamine](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="1d58f-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="1d58f-117">Azure AD identiteedi konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="1d58f-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="1d58f-118">See etapp on nõutav kõigil klientidel, kes kasutavad konfiguratsiooni infrastruktuur teenusena (IaaS).</span><span class="sxs-lookup"><span data-stu-id="1d58f-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="1d58f-119">Klientide, kes kasutavad service fabricut (SF), peaks see etapp olema automaatne ja soovitame kinnitada, et see säte konfigureeritakse ootuspäraselt.</span><span class="sxs-lookup"><span data-stu-id="1d58f-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="1d58f-120">Häälestus</span><span class="sxs-lookup"><span data-stu-id="1d58f-120">Setup</span></span>

1. <span data-ttu-id="1d58f-121">Otsige kontorist lehte **Azure Active Directory rakendused**.</span><span class="sxs-lookup"><span data-stu-id="1d58f-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="1d58f-122">Kontrollige, kas üksusel „RecommendationSystemApplication-1” on olemas kanne.</span><span class="sxs-lookup"><span data-stu-id="1d58f-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="1d58f-123">Kui kannet pole olemas, lisage uus kanne järgmise teabega.</span><span class="sxs-lookup"><span data-stu-id="1d58f-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="1d58f-124">**Kliendi ID** – d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="1d58f-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="1d58f-125">**Nimi** – RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="1d58f-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="1d58f-126">**Kasutaja ID** – RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="1d58f-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="1d58f-127">Salvestage ja sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1d58f-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="1d58f-128">Soovituste sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="1d58f-128">Turn on recommendations</span></span>

<span data-ttu-id="1d58f-129">Tootesoovituste sisselülitamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="1d58f-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="1d58f-130">Commerce'i peakontorist otsige valikut **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="1d58f-130">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="1d58f-131">Saadaolevate funktsioonide vaatamiseks valige **Kõik**.</span><span class="sxs-lookup"><span data-stu-id="1d58f-131">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="1d58f-132">Sisestage otsinguväljale **Soovitused**.</span><span class="sxs-lookup"><span data-stu-id="1d58f-132">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="1d58f-133">Valige funktsioon **Tootesoovitused**.</span><span class="sxs-lookup"><span data-stu-id="1d58f-133">Select the **Product recommendations** feature.</span></span>
1. <span data-ttu-id="1d58f-134">Tehke atribuutide paanil **Tootesoovitused** valik **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="1d58f-134">In the **Product recommendations** properties pane, select **Enable now**.</span></span>

![Soovituste sisselülitamine](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> <span data-ttu-id="1d58f-136">See protseduur käivitab tootesoovituste loendite loomise protsessi.</span><span class="sxs-lookup"><span data-stu-id="1d58f-136">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="1d58f-137">Enne loenditele juurdepääsu ja nende kuvamist kassas või rakenduses Dynamics 365 Commerce, võib kuluda mitu tundi.</span><span class="sxs-lookup"><span data-stu-id="1d58f-137">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="1d58f-138">Soovituste loendi parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="1d58f-138">Configure recommendation list parameters</span></span>

<span data-ttu-id="1d58f-139">Vaikimisi pakub AI-ML-i põhine tootesoovituste loend soovitatavaid väärtusi.</span><span class="sxs-lookup"><span data-stu-id="1d58f-139">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="1d58f-140">Saate vaikimisi soovitatud väärtusi muuta, et need vastaksid teie ettevõtte vooga.</span><span class="sxs-lookup"><span data-stu-id="1d58f-140">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="1d58f-141">Lisateavet vaikimisi parameetrite muutmise kohta leiate teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="1d58f-141">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="1d58f-142">Kassaseadmetes soovituste kuvamine</span><span class="sxs-lookup"><span data-stu-id="1d58f-142">Show recommendations on POS devices</span></span>

<span data-ttu-id="1d58f-143">Pärast soovituste lubamist kaubanduse kontoris, tuleb soovituste paneel lisada paigutuse tööriista kaudu juhtelemendi kassaekraanile.</span><span class="sxs-lookup"><span data-stu-id="1d58f-143">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="1d58f-144">Selle protsessi kohta lisateabe saamiseks vt taamat [Soovituste juhtelemendi lisamine kassaseadmete kandeekraanile](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="1d58f-144">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="1d58f-145">Isikupärastatud soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="1d58f-145">Enable personalized recommendations</span></span>

<span data-ttu-id="1d58f-146">Rakenduses Dynamics 365 Commerce saavad jaemüüjad teha kättesaadavaks isikupärastatud tootesoovitused (tuntud ka kui isikupärastamine).</span><span class="sxs-lookup"><span data-stu-id="1d58f-146">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="1d58f-147">Sel viisil saab isikupärastatud soovitusi lisada kliendi kasutuskogemusele veebis ja kassas.</span><span class="sxs-lookup"><span data-stu-id="1d58f-147">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="1d58f-148">Kui isikupärastamise funktsioon on sisse lülitatud, saab süsteem seostada kasutaja ostu- ja tooteteabe individualiseeritud tootesoovituste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="1d58f-148">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="1d58f-149">Lisateavet isikupärastatud soovituste kohta vaadake jaotisest [Isikupärastatud soovituste lubamine](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="1d58f-149">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1d58f-150">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1d58f-150">Additional resources</span></span>

[<span data-ttu-id="1d58f-151">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="1d58f-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="1d58f-152"> Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas</span><span class="sxs-lookup"><span data-stu-id="1d58f-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="1d58f-153">Isikupärastatud soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="1d58f-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="1d58f-154">„Sarnaste toodete vaatamise” soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="1d58f-154">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="1d58f-155">Isikupärastatud tootesoovitustest loobumine</span><span class="sxs-lookup"><span data-stu-id="1d58f-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="1d58f-156">Tootesoovituste lisamine kassas</span><span class="sxs-lookup"><span data-stu-id="1d58f-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="1d58f-157">Soovituste lisamine kandeekraanile</span><span class="sxs-lookup"><span data-stu-id="1d58f-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="1d58f-158">AI-ML-i soovituste tulemuste kohandamine</span><span class="sxs-lookup"><span data-stu-id="1d58f-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="1d58f-159">Loo kuraatorite soovitused käsitsi</span><span class="sxs-lookup"><span data-stu-id="1d58f-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="1d58f-160">Soovituste loomine demoandmetega</span><span class="sxs-lookup"><span data-stu-id="1d58f-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="1d58f-161">Tootesoovituste KKK</span><span class="sxs-lookup"><span data-stu-id="1d58f-161">Product recommendations FAQ</span></span>](faq-recommendations.md)

