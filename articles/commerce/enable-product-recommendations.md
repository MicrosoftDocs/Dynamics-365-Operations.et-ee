---
title: Tootesoovituste lubamine
description: Selles teemas selgitatakse, kuidas teha tehisintellekti masinõppel (AI-ML) põhinevad tootesoovitused rakenduses Microsoft Dynamics 365 Commerce klientidele kättesaadavaks.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024952"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="3d314-103">Tootesoovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="3d314-103">Enable product recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3d314-104">Selles teemas selgitatakse, kuidas teha tehisintellekti masinõppel (AI-ML) põhinevad tootesoovitused rakenduses Microsoft Dynamics 365 Commerce klientidele kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="3d314-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="3d314-105">Lisateavet tootesoovituste funktsioonide kohta leiate jaotisest [Ülevaade tootesoovitustest](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="3d314-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="3d314-106">Tootesoovituste eelkontroll</span><span class="sxs-lookup"><span data-stu-id="3d314-106">Recommendations pre-check</span></span>

<span data-ttu-id="3d314-107">Enne lubamist võtke arvesse, et tootesoovitusi toetatakse ainult kaubanduse klientide jaoks, kes on migreerinud salvestusruumi kasutama rakendust Azure Data Lake Storage (ADLS).</span><span class="sxs-lookup"><span data-stu-id="3d314-107">Before enabling, please note that product recommendations are only supported for Commerce customers who have migrated their storage to using Azure Data Lake Storage (ADLS).</span></span> 

<span data-ttu-id="3d314-108">ADLS lubamise juhiste saamiseks vaadake teemat [Kuidas lubada ADLS Dynamics 365 keskkonnas](enable-ADLS-environment.md).</span><span class="sxs-lookup"><span data-stu-id="3d314-108">For steps on enabling ADLS, see [How to enable ADLS in a Dynamics 365 environment](enable-ADLS-environment.md).</span></span>

<span data-ttu-id="3d314-109">Lisaks veenduge, et RetailSale’i mõõtmised oleksid lubatud.</span><span class="sxs-lookup"><span data-stu-id="3d314-109">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="3d314-110">Selle seadistusprotsessi kohta lisateabe saamiseks minge [siia.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="3d314-110">To learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="3d314-111">Soovituste sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="3d314-111">Turn on recommendations</span></span>

<span data-ttu-id="3d314-112">Tootesoovituste sisselülitamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3d314-112">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="3d314-113">Avage **Jaemüük ja kaubandus &gt; Tootesoovitused &gt; Soovituste parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="3d314-113">Go to **Retail and Commerce &gt; Product recommendations &gt; Recommendation parameters**.</span></span>
1. <span data-ttu-id="3d314-114">Jagatud parameetrite loendis valige suvand **Soovituste loendid**.</span><span class="sxs-lookup"><span data-stu-id="3d314-114">In the list of shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="3d314-115">Määrake suvand **Luba soovitused** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="3d314-115">Set the **Enable recommendations** option to **Yes**.</span></span>

![tootesoovituste lubamine](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="3d314-117">See protseduur käivitab tootesoovituste loendite loomise protsessi.</span><span class="sxs-lookup"><span data-stu-id="3d314-117">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="3d314-118">Enne loenditele juurdepääsu ja nende nägemist kassas või rakenduses Dynamics 365 Commerce, võib kuluda mitu tundi.</span><span class="sxs-lookup"><span data-stu-id="3d314-118">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="3d314-119">Soovituste loendi parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="3d314-119">Configure recommendation list parameters</span></span>

<span data-ttu-id="3d314-120">Vaikimisi pakub AI-ML-i põhine tootesoovituste loend soovitatavaid väärtusi.</span><span class="sxs-lookup"><span data-stu-id="3d314-120">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="3d314-121">Saate vaikimisi soovitatud väärtusi muuta, et need vastaksid teie ettevõtte vooga.</span><span class="sxs-lookup"><span data-stu-id="3d314-121">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="3d314-122">Lisateavet vaikimisi parameetrite muutmise kohta leiate teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="3d314-122">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="3d314-123">Kassaseadmetes soovituste kuvamine</span><span class="sxs-lookup"><span data-stu-id="3d314-123">Show recommendations on POS devices</span></span>

<span data-ttu-id="3d314-124">Pärast soovituste lubamist kaubanduse kontoris, tuleb soovituste paneel lisada paigutuse tööriista kaudu juhtelemendi kassaekraanile.</span><span class="sxs-lookup"><span data-stu-id="3d314-124">After enabling recommendations in Commerce back office, the recommendations panel must be added to the control POS screen using the layout tool.</span></span> <span data-ttu-id="3d314-125">Selle protsessi kohta lisateabe saamiseks vt taamat [Soovituste juhtelemendi lisamine kassaseadmete kandeekraanile](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="3d314-125">To learn about this process, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span> 

## <a name="enable-personalized-recommendations"></a><span data-ttu-id="3d314-126">Luba isikupärastatud soovitused</span><span class="sxs-lookup"><span data-stu-id="3d314-126">Enable personalized recommendations</span></span>

<span data-ttu-id="3d314-127">Lisateavet isikupärastatud soovituste saamise kohta vaadake jaotisest [Isikupärastatud soovituste lubamine](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="3d314-127">To learn more about how to receive personalized recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3d314-128">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3d314-128">Additional resources</span></span>

[<span data-ttu-id="3d314-129">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="3d314-129">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="3d314-130">Luba isikupärastatud soovitused</span><span class="sxs-lookup"><span data-stu-id="3d314-130">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="3d314-131">Tootesoovituste loendite lisamine lehtedele</span><span class="sxs-lookup"><span data-stu-id="3d314-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="3d314-132">Kassaseadmetele soovituste paneeli lisamine</span><span class="sxs-lookup"><span data-stu-id="3d314-132">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="3d314-133">Tootekogumi mooduli ülevaade</span><span class="sxs-lookup"><span data-stu-id="3d314-133">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="3d314-134">ADLS lubamine Dynamics 365 keskkonnas</span><span class="sxs-lookup"><span data-stu-id="3d314-134">Enable ADLS in Dynamics 365 environment</span></span>](enable-ADLS-environment.md)

