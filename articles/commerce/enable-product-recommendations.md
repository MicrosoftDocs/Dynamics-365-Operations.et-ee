---
title: Tootesoovituste lubamine
description: Selles teemas selgitatakse, kuidas teha tehisintellekti masinõppel (AI-ML) põhinevad tootesoovitused rakenduses Microsoft Dynamics 365 Commerce klientidele kättesaadavaks.
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
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
ms.openlocfilehash: d38d7b0e98d84e23d7a51c5d8ee65df4a3b9e4a7
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259790"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="a9d63-103">Tootesoovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="a9d63-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a9d63-104">Selles teemas selgitatakse, kuidas teha tehisintellekti masinõppel (AI-ML) põhinevad tootesoovitused rakenduses Microsoft Dynamics 365 Commerce klientidele kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="a9d63-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="a9d63-105">Lisateavet tootesoovituste funktsioonide kohta leiate jaotisest [Ülevaade tootesoovitustest](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="a9d63-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="a9d63-106">Tootesoovituste eelkontroll</span><span class="sxs-lookup"><span data-stu-id="a9d63-106">Recommendations pre-check</span></span>

<span data-ttu-id="a9d63-107">Enne lubamist võtke arvesse, et tootesoovitusi toetatakse ainult Commerce'i klientide jaoks, kes on migreerinud salvestusruumi kasutama rakendust Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="a9d63-107">Before enabling, note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="a9d63-108">Enne soovituste lubamist tuleb kontoris lubada järgmised konfiguratsioonid:</span><span class="sxs-lookup"><span data-stu-id="a9d63-108">The following configurations must be enabled in the back office before enabling recommendations:</span></span>

1. <span data-ttu-id="a9d63-109">Veenduge, et ADLS oleks ostetud ja keskkonnas edukalt kontrollitud.</span><span class="sxs-lookup"><span data-stu-id="a9d63-109">Ensure that ADLS has been purchased and successfully verified in the environment.</span></span> <span data-ttu-id="a9d63-110">Lisateabe saamisesk vt [Veenduge, et ADLS oleks ostetud ja keskkonnas edukalt kontrollitud](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a9d63-110">For more information, see [Ensure that ADLS has been purchased and successfully verified in the environment](enable-ADLS-environment.md).</span></span>
2. <span data-ttu-id="a9d63-111">Veenduge, et üksuse kaupluse värskendamine oleks automatiseeritud.</span><span class="sxs-lookup"><span data-stu-id="a9d63-111">Ensure that the entity store refresh has been automated.</span></span> <span data-ttu-id="a9d63-112">Lisateabe saamiseks vt [Veenduge, et üksuse kaupluse värskendamine oleks automatiseeritud](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="a9d63-112">For more information, see [Ensure that the Entity store refresh has been automated](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md).</span></span>
3. <span data-ttu-id="a9d63-113">Kinnitage, et Azure AD identiteedi konfiguratsioon sisaldab kirjet üksuse Soovitused jaoks.</span><span class="sxs-lookup"><span data-stu-id="a9d63-113">Confirm that Azure AD Identity configuration contains an entry for Recommendations.</span></span> <span data-ttu-id="a9d63-114">Lisateavet selle tegevuse kohta leiate altpoolt.</span><span class="sxs-lookup"><span data-stu-id="a9d63-114">More information on how to do this action is below.</span></span>

<span data-ttu-id="a9d63-115">Lisaks veenduge, et RetailSale’i mõõtmised oleksid lubatud.</span><span class="sxs-lookup"><span data-stu-id="a9d63-115">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="a9d63-116">Selle seadistamisprotsessi kohta lisateabe saamiseks vt [Mõõtudega töötamine](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span><span class="sxs-lookup"><span data-stu-id="a9d63-116">To learn more about this set up process, see [Work with measures](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures).</span></span>

## <a name="azure-ad-identity-configuration"></a><span data-ttu-id="a9d63-117">Azure AD identiteedi konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="a9d63-117">Azure AD Identity configuration</span></span>

<span data-ttu-id="a9d63-118">See etapp on nõutav kõigil klientidel, kes kasutavad konfiguratsiooni infrastruktuur teenusena (IaaS).</span><span class="sxs-lookup"><span data-stu-id="a9d63-118">This step is required for all customers running an infra-structure as a service (IaaS) configuration.</span></span> <span data-ttu-id="a9d63-119">Klientide, kes kasutavad service fabricut (SF), peaks see etapp olema automaatne ja soovitame kinnitada, et see säte konfigureeritakse ootuspäraselt.</span><span class="sxs-lookup"><span data-stu-id="a9d63-119">For customers running on service fabric (SF), this step should be automatic and we recommend verifying the setting is configured as expected.</span></span>

### <a name="setup"></a><span data-ttu-id="a9d63-120">Häälestus</span><span class="sxs-lookup"><span data-stu-id="a9d63-120">Setup</span></span>

1. <span data-ttu-id="a9d63-121">Otsige kontorist lehte **Azure Active Directory rakendused**.</span><span class="sxs-lookup"><span data-stu-id="a9d63-121">From the back office, search for the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="a9d63-122">Kontrollige, kas üksusel „RecommendationSystemApplication-1” on olemas kanne.</span><span class="sxs-lookup"><span data-stu-id="a9d63-122">Verify if an entry exists for "RecommendationSystemApplication-1".</span></span>

<span data-ttu-id="a9d63-123">Kui kannet pole olemas, lisage uus kanne järgmise teabega.</span><span class="sxs-lookup"><span data-stu-id="a9d63-123">If the entry does not exist, add a new entry with the following information:</span></span>

- <span data-ttu-id="a9d63-124">**Kliendi ID** – d37b07e8-dd1c-4514-835d-8b918e6f9727</span><span class="sxs-lookup"><span data-stu-id="a9d63-124">**Client Id** - d37b07e8-dd1c-4514-835d-8b918e6f9727</span></span>
- <span data-ttu-id="a9d63-125">**Nimi** – RecommendationSystemApplication-1</span><span class="sxs-lookup"><span data-stu-id="a9d63-125">**Name** - RecommendationSystemApplication-1</span></span>
- <span data-ttu-id="a9d63-126">**Kasutaja ID** – RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="a9d63-126">**User Id** - RetailServiceAccount</span></span>

<span data-ttu-id="a9d63-127">Salvestage ja sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a9d63-127">Save and close the page.</span></span> 

## <a name="turn-on-recommendations"></a><span data-ttu-id="a9d63-128">Soovituste sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="a9d63-128">Turn on recommendations</span></span>

<span data-ttu-id="a9d63-129">Tootesoovituste sisselülitamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a9d63-129">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="a9d63-130">Avage **Jaemüük ja kaubandus &gt; Tootesoovitused &gt; Soovituste parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="a9d63-130">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="a9d63-131">Jagatud parameetrite loendis valige suvand **Soovituste loendid**.</span><span class="sxs-lookup"><span data-stu-id="a9d63-131">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="a9d63-132">Määrake suvand **Luba soovitused** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="a9d63-132">Set the **Enable recommendations** option to **Yes**.</span></span>

![Soovituste sisselülitamine](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="a9d63-134">See protseduur käivitab tootesoovituste loendite loomise protsessi.</span><span class="sxs-lookup"><span data-stu-id="a9d63-134">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="a9d63-135">Enne loenditele juurdepääsu ja nende kuvamist kassas või rakenduses Dynamics 365 Commerce, võib kuluda mitu tundi.</span><span class="sxs-lookup"><span data-stu-id="a9d63-135">It may take several hours before the lists are available and can be viewed at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="a9d63-136">Soovituste loendi parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="a9d63-136">Configure recommendation list parameters</span></span>

<span data-ttu-id="a9d63-137">Vaikimisi pakub AI-ML-i põhine tootesoovituste loend soovitatavaid väärtusi.</span><span class="sxs-lookup"><span data-stu-id="a9d63-137">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="a9d63-138">Saate vaikimisi soovitatud väärtusi muuta, et need vastaksid teie ettevõtte vooga.</span><span class="sxs-lookup"><span data-stu-id="a9d63-138">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="a9d63-139">Lisateavet vaikimisi parameetrite muutmise kohta leiate teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="a9d63-139">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="a9d63-140">Kassaseadmetes soovituste kuvamine</span><span class="sxs-lookup"><span data-stu-id="a9d63-140">Show recommendations on POS devices</span></span>

<span data-ttu-id="a9d63-141">Pärast soovituste lubamist kaubanduse kontoris, tuleb soovituste paneel lisada paigutuse tööriista kaudu juhtelemendi kassaekraanile.</span><span class="sxs-lookup"><span data-stu-id="a9d63-141">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="a9d63-142">Selle protsessi kohta lisateabe saamiseks vt taamat [Soovituste juhtelemendi lisamine kassaseadmete kandeekraanile](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="a9d63-142">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="a9d63-143">Isikupärastatud soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="a9d63-143">Enable personalized recommendations</span></span>

<span data-ttu-id="a9d63-144">Rakenduses Dynamics 365 Commerce saavad jaemüüjad teha kättesaadavaks isikupärastatud tootesoovitused (tuntud ka kui isikupärastamine).</span><span class="sxs-lookup"><span data-stu-id="a9d63-144">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="a9d63-145">Sel viisil saab isikupärastatud soovitusi lisada kliendi kasutuskogemusele veebis ja kassas.</span><span class="sxs-lookup"><span data-stu-id="a9d63-145">In this way, personalized recommendations can be incorporated into the online customer experience and at the point of sale.</span></span> <span data-ttu-id="a9d63-146">Kui isikupärastamise funktsioon on sisse lülitatud, saab süsteem seostada kasutaja ostu- ja tooteteabe individualiseeritud tootesoovituste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="a9d63-146">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

<span data-ttu-id="a9d63-147">Lisateavet isikupärastatud soovituste kohta vaadake jaotisest [Isikupärastatud soovituste lubamine](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="a9d63-147">To learn more about personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a9d63-148">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a9d63-148">Additional resources</span></span>

[<span data-ttu-id="a9d63-149">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="a9d63-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a9d63-150">ADLS-i lubamine Dynamics 365 Commerce keskkonnas</span><span class="sxs-lookup"><span data-stu-id="a9d63-150">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="a9d63-151">Isikupärastatud soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="a9d63-151">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="a9d63-152">Isikupärastatud tootesoovitustest loobumine</span><span class="sxs-lookup"><span data-stu-id="a9d63-152">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="a9d63-153">Tootesoovituste lisamine kassas</span><span class="sxs-lookup"><span data-stu-id="a9d63-153">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="a9d63-154">Soovituste lisamine kandeekraanile</span><span class="sxs-lookup"><span data-stu-id="a9d63-154">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="a9d63-155">AI-ML-i soovituste tulemuste kohandamine</span><span class="sxs-lookup"><span data-stu-id="a9d63-155">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="a9d63-156">Loo kuraatorite soovitused käsitsi</span><span class="sxs-lookup"><span data-stu-id="a9d63-156">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="a9d63-157">Soovituste loomine demoandmetega</span><span class="sxs-lookup"><span data-stu-id="a9d63-157">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="a9d63-158">Tootesoovituste KKK</span><span class="sxs-lookup"><span data-stu-id="a9d63-158">Product recommendations FAQ</span></span>](faq-recommendations.md)

