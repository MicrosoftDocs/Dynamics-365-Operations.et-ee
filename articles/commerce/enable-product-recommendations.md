---
title: Tootesoovituste lubamine
description: Selles teemas selgitatakse, kuidas teha tehisintellekti masinõppel (AI-ML) põhinevad tootesoovitused rakenduses Microsoft Dynamics 365 Commerce klientidele kättesaadavaks.
author: bebeale
manager: AnnBe
ms.date: 03/19/2020
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
ms.openlocfilehash: d8a579be5df3c5e7718a6fb4720341f3bd01a64c
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154409"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="abebb-103">Tootesoovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="abebb-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="abebb-104">Selles teemas selgitatakse, kuidas teha tehisintellekti masinõppel (AI-ML) põhinevad tootesoovitused rakenduses Microsoft Dynamics 365 Commerce klientidele kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="abebb-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="abebb-105">Lisateavet tootesoovituste funktsioonide kohta leiate jaotisest [Ülevaade tootesoovitustest](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="abebb-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="abebb-106">Tootesoovituste eelkontroll</span><span class="sxs-lookup"><span data-stu-id="abebb-106">Recommendations pre-check</span></span>

<span data-ttu-id="abebb-107">Enne lubamist võtke arvesse, et tootesoovitusi toetatakse ainult kaubanduse klientide jaoks, kes on migreerinud salvestusruumi kasutama rakendust Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="abebb-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="abebb-108">ADLS lubamise juhiste saamiseks vaadake teemat [Kuidas lubada ADLS Dynamics 365 keskkonnas](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="abebb-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="abebb-109">Lisaks veenduge, et RetailSale’i mõõtmised oleksid lubatud.</span><span class="sxs-lookup"><span data-stu-id="abebb-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="abebb-110">Selle seadistusprotsessi kohta lisateabe saamiseks minge [siia.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="abebb-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="abebb-111">Soovituste sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="abebb-111">Turn on recommendations</span></span>

<span data-ttu-id="abebb-112">Tootesoovituste sisselülitamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="abebb-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="abebb-113">Avage **Jaemüük ja kaubandus &gt; Tootesoovitused &gt; Soovituste parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="abebb-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="abebb-114">Jagatud parameetrite loendis valige suvand **Soovituste loendid**.</span><span class="sxs-lookup"><span data-stu-id="abebb-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="abebb-115">Määrake suvand **Luba soovitused** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="abebb-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![tootesoovituste lubamine](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="abebb-117">See protseduur käivitab tootesoovituste loendite loomise protsessi.</span><span class="sxs-lookup"><span data-stu-id="abebb-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="abebb-118">Enne loenditele juurdepääsu ja nende nägemist kassas või rakenduses Dynamics 365 Commerce, võib kuluda mitu tundi.</span><span class="sxs-lookup"><span data-stu-id="abebb-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="abebb-119">Soovituste loendi parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="abebb-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="abebb-120">Vaikimisi pakub AI-ML-i põhine tootesoovituste loend soovitatavaid väärtusi.</span><span class="sxs-lookup"><span data-stu-id="abebb-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="abebb-121">Saate vaikimisi soovitatud väärtusi muuta, et need vastaksid teie ettevõtte vooga.</span><span class="sxs-lookup"><span data-stu-id="abebb-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="abebb-122">Lisateavet vaikimisi parameetrite muutmise kohta leiate teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="abebb-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="abebb-123">Kassaseadmetes soovituste kuvamine</span><span class="sxs-lookup"><span data-stu-id="abebb-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="abebb-124">Pärast soovituste lubamist kaubanduse kontoris, tuleb soovituste paneel lisada paigutuse tööriista kaudu juhtelemendi kassaekraanile.</span><span class="sxs-lookup"><span data-stu-id="abebb-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="abebb-125">Selle protsessi kohta lisateabe saamiseks vt taamat [Soovituste juhtelemendi lisamine kassaseadmete kandeekraanile](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="abebb-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="abebb-126">Luba isikupärastatud soovitused</span><span class="sxs-lookup"><span data-stu-id="abebb-126">Enable personalized recommendations</span></span>

<span data-ttu-id="abebb-127">Lisateavet isikupärastatud soovituste saamise kohta vaadake jaotisest [Isikupärastatud soovituste lubamine](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="abebb-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="abebb-128">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="abebb-128">Additional resources</span></span>

[<span data-ttu-id="abebb-129">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="abebb-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="abebb-130">ADLS-i lubamine Dynamics 365 Commerce keskkonnas</span><span class="sxs-lookup"><span data-stu-id="abebb-130">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="abebb-131">Isikupärastatud soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="abebb-131">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="abebb-132">Isikupärastatud tootesoovitustest loobumine</span><span class="sxs-lookup"><span data-stu-id="abebb-132">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="abebb-133">Tootesoovituste lisamine kassas</span><span class="sxs-lookup"><span data-stu-id="abebb-133">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="abebb-134">Soovituste lisamine kandeekraanile</span><span class="sxs-lookup"><span data-stu-id="abebb-134">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="abebb-135">AI-ML-i soovituste tulemuste kohandamine</span><span class="sxs-lookup"><span data-stu-id="abebb-135">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="abebb-136">Loo kuraatorite soovitused käsitsi</span><span class="sxs-lookup"><span data-stu-id="abebb-136">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="abebb-137">Soovituste loomine demoandmetega</span><span class="sxs-lookup"><span data-stu-id="abebb-137">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="abebb-138">Tootesoovituste KKK</span><span class="sxs-lookup"><span data-stu-id="abebb-138">Product recommendations FAQ</span></span>](faq-recommendations.md)

