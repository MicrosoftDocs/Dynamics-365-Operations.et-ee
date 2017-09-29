---
title: "Jaemüügihierarhiad"
description: "Selles artiklis kirjeldatakse Microsoft Dynamics 365 for Retaili jaemüügihierarhiaid."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 817696566473bc5f31a7ff11c04291351dfd4764
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="retail-hierarchies"></a><span data-ttu-id="313e7-103">Jaemüügihierarhiad</span><span class="sxs-lookup"><span data-stu-id="313e7-103">Retail hierarchies</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="313e7-104">Selles artiklis kirjeldatakse Microsoft Dynamics 365 for Retaili jaemüügihierarhiaid.</span><span class="sxs-lookup"><span data-stu-id="313e7-104">This article describes retail hierarchies in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="313e7-105">Saate luua jaemüügi kategooriahierarhia, et korraldada jaemüügikanalite kaudu müüdavaid tooteid.</span><span class="sxs-lookup"><span data-stu-id="313e7-105">You can create a retail category hierarchy to organize the products that you sell through your retail channels.</span></span> <span data-ttu-id="313e7-106">Jaemüügi tootehierarhiate abil saate tooteid kategoriseerida või grupeerida.</span><span class="sxs-lookup"><span data-stu-id="313e7-106">You can use retail product hierarchies to categorize or group products.</span></span> <span data-ttu-id="313e7-107">Seejärel saate neid tooteid kasutada tootesortimentide ja püsikliendiprogrammide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="313e7-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="313e7-108">Saate ka määrata toote atribuute ja omadusi, määrata hinnakujunduse struktuuri, kaasata tooteid tootekampaaniatesse ja kasutada tooteid aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="313e7-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="313e7-109">Saate luua ühe jaemüügi kategooriahierarhia esindama kõiki organisatsiooni tooteid ja kategooriaid ning seejärel kasutada seda kategooriahierarhiat mitmel eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="313e7-109">You can create one retail category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="313e7-110">Samuti on teil võimalik luua mitu jaemüügi kategooriahierarhiat eriotstarbeks, näiteks tootekampaaniate jaoks.</span><span class="sxs-lookup"><span data-stu-id="313e7-110">Alternatively, you can create multiple retail category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="313e7-111">Jaemüügi tootehierarhia loomisel tuleb määrata kategooria hierarhia tüüp, et tuvastada kategooriahierarhia eesmärk.</span><span class="sxs-lookup"><span data-stu-id="313e7-111">When you create a retail product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="313e7-112">Näiteks viidatakse toote sirvimisel võrgus või kassas ainult tootehierarhiaid, millele on määratud tüüp **Jaemüügi navigeerimishierarhia**.</span><span class="sxs-lookup"><span data-stu-id="313e7-112">For example, only product hierarchies that are assigned the **Retail navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="retail-hierarchy-types"></a><span data-ttu-id="313e7-113">Jaemüügihierarhia tüübid</span><span class="sxs-lookup"><span data-stu-id="313e7-113">Retail hierarchy types</span></span>
<span data-ttu-id="313e7-114">Järgmises tabelis on loetletud saadaolevad jaemüügi kategooriahierarhia tüübid ja iga tüübi üldeesmärk.</span><span class="sxs-lookup"><span data-stu-id="313e7-114">The following table lists the types of retail category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="313e7-115">Kategooriahierarhia tüüp</span><span class="sxs-lookup"><span data-stu-id="313e7-115">Category hierarchy type</span></span>       | <span data-ttu-id="313e7-116">Eesmärk</span><span class="sxs-lookup"><span data-stu-id="313e7-116">Purpose</span></span>                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="313e7-117">Jaemüügi tootehierarhia</span><span class="sxs-lookup"><span data-stu-id="313e7-117">Retail product hierarchy</span></span>      | <span data-ttu-id="313e7-118">Kasutage seda hierarhiatüüpi, et määratleda organisatsiooni üldine tootehierarhia.</span><span class="sxs-lookup"><span data-stu-id="313e7-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="313e7-119">Saate seda hierarhiatüüpi kasutada tootesündmuste, hinnakujunduse ja kampaaniate, aruandluse ning sortimendi planeerimise jaoks.</span><span class="sxs-lookup"><span data-stu-id="313e7-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="313e7-120">Selle hierarhiatüübe saab määrata ainult ühele jaemüügi tootehierarhiale.</span><span class="sxs-lookup"><span data-stu-id="313e7-120">Only one retail product hierarchy can be assigned this hierarchy type.</span></span>                                       |
| <span data-ttu-id="313e7-121">Täiendav jaemüügi hierarhia</span><span class="sxs-lookup"><span data-stu-id="313e7-121">Supplemental retail hierarchy</span></span> | <span data-ttu-id="313e7-122">Kasutage seda hierarhiatüüpi mis tahes täiendavate jaemüügi kategooriahierarhiate puhul, mille soovite luua.</span><span class="sxs-lookup"><span data-stu-id="313e7-122">Use this hierarchy type for any additional retail category hierarchies that you want to create.</span></span> <span data-ttu-id="313e7-123">Näiteks korraldate kevadel kampaania ujumisriiete müügiks.</span><span class="sxs-lookup"><span data-stu-id="313e7-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="313e7-124">Seega kaasate ujumisriietest tooted eraldi kategooriahierarhiasse ja rakendate erinevatele tootekategooriatele kampaaniahinnad.</span><span class="sxs-lookup"><span data-stu-id="313e7-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="313e7-125">Jaemüügi navigeerimishierarhia</span><span class="sxs-lookup"><span data-stu-id="313e7-125">Retail navigation hierarchy</span></span>   | <span data-ttu-id="313e7-126">Kasutage seda hierarhiatüüpi toodete grupeerimiseks ja korraldamiseks kategooriatesse, nii et tooteid saab sirvida võrgus või kassas.</span><span class="sxs-lookup"><span data-stu-id="313e7-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span>                                                                                                                                                                                       |

<span data-ttu-id="313e7-127">Jaemüügi kategooriahierarhia abil tooteid struktureerides saate seadistada ja hallata tooteatribuute ning omadusi kategooria tasemel.</span><span class="sxs-lookup"><span data-stu-id="313e7-127">By using a retail category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="313e7-128">Need atribuudid ja omadused hõlmavad tootedimensioonide ja kassasätteid.</span><span class="sxs-lookup"><span data-stu-id="313e7-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="313e7-129">Kategooriatesse määratud tooted pärivad automaatselt teie määratud atribuudid ja omadused.</span><span class="sxs-lookup"><span data-stu-id="313e7-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="313e7-130">Samal ajal saate kopeerida ka mis tahes toote atribuudisätted valitud kategoorias mitmele tootele.</span><span class="sxs-lookup"><span data-stu-id="313e7-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>




