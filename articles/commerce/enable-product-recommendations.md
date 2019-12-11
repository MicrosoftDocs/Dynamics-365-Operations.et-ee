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
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770135"
---
# <a name="enable-product-recommendations"></a><span data-ttu-id="b58d1-103">Tootesoovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="b58d1-103">Enable product recommendations</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b58d1-104">Selles teemas selgitatakse, kuidas teha tehisintellekti masinõppel (AI-ML) põhinevad tootesoovitused rakenduses Microsoft Dynamics 365 Commerce klientidele kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="b58d1-104">This topic explains how to make product recommendations that are based on artificial intelligence-machine learning (AI-ML) available for Microsoft Dynamics 365 Commerce customers.</span></span> <span data-ttu-id="b58d1-105">Lisateavet tootesoovituste funktsioonide kohta leiate jaotisest [Ülevaade tootesoovitustest](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="b58d1-105">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="recommendations-pre-check"></a><span data-ttu-id="b58d1-106">Tootesoovituste eelkontroll</span><span class="sxs-lookup"><span data-stu-id="b58d1-106">Recommendations pre-check</span></span>
<span data-ttu-id="b58d1-107">Enne lubamist võtke arvesse, et tootesoovitusi toetatakse ainult F&O klientide jaoks, mis toetavad järku 10.0.6 ja on migreerinud salvestusruumi kasutama BDL-i.</span><span class="sxs-lookup"><span data-stu-id="b58d1-107">Before enabling, please note that product recommendations are only supported for F&O customers supporting build 10.0.6 and have migrated their storage to using BDL.</span></span> 

<span data-ttu-id="b58d1-108">Lisaks veenduge, et RetailSale’i mõõtmised oleksid lubatud.</span><span class="sxs-lookup"><span data-stu-id="b58d1-108">Additionally, ensure that RetailSale measurements have been enabled.</span></span> <span data-ttu-id="b58d1-109">Selle seadistusprotsessi kohta lisateabe saamiseks minge [siia.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span><span class="sxs-lookup"><span data-stu-id="b58d1-109">To Learn more about this set up process, go [here.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)</span></span>


## <a name="turn-on-recommendations"></a><span data-ttu-id="b58d1-110">Soovituste sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="b58d1-110">Turn on recommendations</span></span>

<span data-ttu-id="b58d1-111">Tootesoovituste sisselülitamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b58d1-111">To turn on product recommendations, follow these steps.</span></span>

1. <span data-ttu-id="b58d1-112">Avage **Jaemüük** &gt; **Tootesoovitused** &gt; **Soovituste parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="b58d1-112">Go to **Retail** &gt; **Product recommendations** &gt; **Recommendation parameters**.</span></span>
1. <span data-ttu-id="b58d1-113">Jaemüügi jagatud parameetrite loendis valige suvand **Soovituste loendid**.</span><span class="sxs-lookup"><span data-stu-id="b58d1-113">In the list of retail shared parameters, select **Recommendation Lists**.</span></span>
1. <span data-ttu-id="b58d1-114">Määrake suvand **Luba soovitused** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b58d1-114">Set the **Enable recommendations** option to **Yes**.</span></span>

![tootesoovituste lubamine](./media/enableproductrecommendations.png)

> [!NOTE]
> <span data-ttu-id="b58d1-116">See protseduur käivitab tootesoovituste loendite loomise protsessi.</span><span class="sxs-lookup"><span data-stu-id="b58d1-116">This procedure starts the process of generating product recommendation lists.</span></span> <span data-ttu-id="b58d1-117">Enne loenditele juurdepääsu ja nende nägemist kassas või rakenduses Dynamics 365 for Commerce, võib kuluda mitu tundi.</span><span class="sxs-lookup"><span data-stu-id="b58d1-117">Up to several hours might be required before the lists are available and can be seen at the point of sale (POS) or in Dynamics 365 for Commerce.</span></span>

## <a name="configure-recommendation-list-parameters"></a><span data-ttu-id="b58d1-118">Soovituste loendi parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b58d1-118">Configure recommendation list parameters</span></span>
<span data-ttu-id="b58d1-119">Vaikimisi pakub AI-ML-i põhine tootesoovituste loend soovitatavaid väärtusi.</span><span class="sxs-lookup"><span data-stu-id="b58d1-119">By default, the AI-ML-based product recommendation list provides suggested values.</span></span> <span data-ttu-id="b58d1-120">Saate vaikimisi soovitatud väärtusi muuta, et need vastaksid teie ettevõtte vooga.</span><span class="sxs-lookup"><span data-stu-id="b58d1-120">You can change the default suggested values to suit the flow of your business.</span></span> <span data-ttu-id="b58d1-121">Lisateavet vaikimisi parameetrite muutmise kohta leiate teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="b58d1-121">To learn more about how to change the default parameters, go to [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="show-recommendations-on-pos-devices"></a><span data-ttu-id="b58d1-122">Kassaseadmetes soovituste kuvamine</span><span class="sxs-lookup"><span data-stu-id="b58d1-122">Show recommendations on POS devices</span></span>
<span data-ttu-id="b58d1-123">Pärast soovituste lubamist kontoris, tuleb soovituste paneel lisada paigutuse tööriista kaudu juhtelemendi kassaekraanile.</span><span class="sxs-lookup"><span data-stu-id="b58d1-123">After enabling recommendations in the back office, the recommendations pannel must be added to the control POS screen via the layout tool.</span></span> <span data-ttu-id="b58d1-124">Selle protsessi kohta teabe saamiseks minge [siia.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span><span class="sxs-lookup"><span data-stu-id="b58d1-124">To learn about this process, go [here.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)</span></span>


## <a name="additional-resources"></a><span data-ttu-id="b58d1-125">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b58d1-125">Additional resources</span></span>

[<span data-ttu-id="b58d1-126">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="b58d1-126">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="b58d1-127">Tootesoovituste loendite lisamine lehtedele</span><span class="sxs-lookup"><span data-stu-id="b58d1-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="b58d1-128">Kassaseadmetele soovituste paneeli lisamine</span><span class="sxs-lookup"><span data-stu-id="b58d1-128">Add recommendations panel to POS devices</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


