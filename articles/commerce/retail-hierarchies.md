---
title: Commerce’i hierarhiad
description: Selles artiklis kirjeldatakse rakenduse Dynamics 365 Commerce hierarhiaid.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8f7e4d01970f459f66934fe434ec7307104b39b2
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895277"
---
# <a name="commerce-hierarchies"></a><span data-ttu-id="bcff2-103">Commerce’i hierarhiad</span><span class="sxs-lookup"><span data-stu-id="bcff2-103">Commerce hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bcff2-104">Selles artiklis kirjeldatakse rakenduse Dynamics 365 Commerce hierarhiaid.</span><span class="sxs-lookup"><span data-stu-id="bcff2-104">This article describes hierarchies in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="bcff2-105">Saate luua kategooriahierarhia, et korraldada kanalite kaudu müüdavaid tooteid.</span><span class="sxs-lookup"><span data-stu-id="bcff2-105">You can create a category hierarchy to organize the products that you sell through your channels.</span></span> <span data-ttu-id="bcff2-106">Tootehierarhiate abil saate tooteid kategoriseerida või grupeerida.</span><span class="sxs-lookup"><span data-stu-id="bcff2-106">You can use product hierarchies to categorize or group products.</span></span> <span data-ttu-id="bcff2-107">Seejärel saate neid tooteid kasutada tootesortimentide ja püsikliendiprogrammide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="bcff2-107">You can then use these products to create product assortments and customer loyalty programs.</span></span> <span data-ttu-id="bcff2-108">Saate ka määrata toote atribuute ja omadusi, määrata hinnakujunduse struktuuri, kaasata tooteid tootekampaaniatesse ja kasutada tooteid aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="bcff2-108">You can also assign product attributes and properties, assign a pricing structure, include the products in product promotions, and use the products for reporting.</span></span> <span data-ttu-id="bcff2-109">Saate luua ühe kategooriahierarhia esindama kõiki organisatsiooni tooteid ja kategooriaid ning kasutada seda kategooriahierarhiat mitmel eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="bcff2-109">You can create one category hierarchy to represent all the products and categories in your organization, and then use that category hierarchy for multiple purposes.</span></span> <span data-ttu-id="bcff2-110">Teise võimalusena saate luua mitme kategooria hierarhiad eriotstarbeks, näiteks tootekampaaniate jaoks.</span><span class="sxs-lookup"><span data-stu-id="bcff2-110">Alternatively, you can create multiple category hierarchies for special purposes, such as product promotions.</span></span> <span data-ttu-id="bcff2-111">Tootehierarhia loomisel tuleb määrata kategooria hierarhia tüüp, et tuvastada kategooriahierarhia eesmärk.</span><span class="sxs-lookup"><span data-stu-id="bcff2-111">When you create a product hierarchy, you must assign a category hierarchy type to identify the purpose of the category hierarchy.</span></span> <span data-ttu-id="bcff2-112">Näiteks viidatakse toote sirvimisel võrgus või kassas ainult tootehierarhiaid, millele on määratud tüüp **Kaubanduse navigeerimishierarhia**.</span><span class="sxs-lookup"><span data-stu-id="bcff2-112">For example, only product hierarchies that are assigned the **Commerce navigation hierarchy** type are referenced when you browse products by category online or in point of sale (POS).</span></span>

## <a name="hierarchy-types"></a><span data-ttu-id="bcff2-113">Hierarhia tüübid</span><span class="sxs-lookup"><span data-stu-id="bcff2-113">Hierarchy types</span></span>

<span data-ttu-id="bcff2-114">Järgmises tabelis on loetletud saadaolevad kategooriahierarhia tüübid ja iga tüübi üldeesmärk.</span><span class="sxs-lookup"><span data-stu-id="bcff2-114">The following table lists the types of category hierarchies that are available and the general purpose of each type.</span></span>

| <span data-ttu-id="bcff2-115">Kategooriahierarhia tüüp</span><span class="sxs-lookup"><span data-stu-id="bcff2-115">Category hierarchy type</span></span>       | <span data-ttu-id="bcff2-116">Eesmärk</span><span class="sxs-lookup"><span data-stu-id="bcff2-116">Purpose</span></span> |
|-------------------------------|---------|
| <span data-ttu-id="bcff2-117">Tootehierarhia</span><span class="sxs-lookup"><span data-stu-id="bcff2-117">Product hierarchy</span></span>      | <span data-ttu-id="bcff2-118">Kasutage seda hierarhiatüüpi, et määratleda organisatsiooni üldine tootehierarhia.</span><span class="sxs-lookup"><span data-stu-id="bcff2-118">Use this hierarchy type to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="bcff2-119">Saate seda hierarhiatüüpi kasutada tootesündmuste, hinnakujunduse ja kampaaniate, aruandluse ning sortimendi planeerimise jaoks.</span><span class="sxs-lookup"><span data-stu-id="bcff2-119">You can use this hierarchy type for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="bcff2-120">Selle hierarhia tüübi saab määrata ainult ühele tootehierarhiale.</span><span class="sxs-lookup"><span data-stu-id="bcff2-120">Only one product hierarchy can be assigned this hierarchy type.</span></span> |
| <span data-ttu-id="bcff2-121">Täiendav hierarhia</span><span class="sxs-lookup"><span data-stu-id="bcff2-121">Supplemental hierarchy</span></span> | <span data-ttu-id="bcff2-122">Kasutage seda hierarhia tüüpi mis tahes täiendavate kategooriahierarhiate puhul, mille soovite luua.</span><span class="sxs-lookup"><span data-stu-id="bcff2-122">Use this hierarchy type for any additional category hierarchies that you want to create.</span></span> <span data-ttu-id="bcff2-123">Näiteks korraldate kevadel kampaania ujumisriiete müügiks.</span><span class="sxs-lookup"><span data-stu-id="bcff2-123">For example, in the spring, you have a promotion for swimwear.</span></span> <span data-ttu-id="bcff2-124">Seega kaasate ujumisriietest tooted eraldi kategooriahierarhiasse ja rakendate erinevatele tootekategooriatele kampaaniahinnad.</span><span class="sxs-lookup"><span data-stu-id="bcff2-124">Therefore, you include your swimwear products in a separate category hierarchy and apply the promotional pricing to the various product categories.</span></span> |
| <span data-ttu-id="bcff2-125">Navigeerimishierarhia</span><span class="sxs-lookup"><span data-stu-id="bcff2-125">Navigation hierarchy</span></span>   | <span data-ttu-id="bcff2-126">Kasutage seda hierarhiatüüpi toodete grupeerimiseks ja korraldamiseks kategooriatesse, nii et tooteid saab sirvida võrgus või kassas.</span><span class="sxs-lookup"><span data-stu-id="bcff2-126">Use this hierarchy type to group and organize products into categories so that the products can be browsed online or in POS.</span></span> |

<span data-ttu-id="bcff2-127">Kategooriahierarhia abil tooteid struktureerides saate seadistada ja hallata toote atribuute ning omadusi kategooria tasemel.</span><span class="sxs-lookup"><span data-stu-id="bcff2-127">By using a category hierarchy to structure your products, you can set up and maintain product attributes and properties at the category level.</span></span> <span data-ttu-id="bcff2-128">Need atribuudid ja omadused hõlmavad tootedimensioonide ja kassasätteid.</span><span class="sxs-lookup"><span data-stu-id="bcff2-128">These attributes and properties include settings for product dimensions and POS settings.</span></span> <span data-ttu-id="bcff2-129">Kategooriatesse määratud tooted pärivad automaatselt teie määratud atribuudid ja omadused.</span><span class="sxs-lookup"><span data-stu-id="bcff2-129">Any products that you assign to the categories automatically inherit the attributes and properties that you define.</span></span> <span data-ttu-id="bcff2-130">Samal ajal saate kopeerida ka mis tahes toote atribuudisätted valitud kategoorias mitmele tootele.</span><span class="sxs-lookup"><span data-stu-id="bcff2-130">You can also copy the property settings for any product to multiple products in a selected category at the same time.</span></span>
