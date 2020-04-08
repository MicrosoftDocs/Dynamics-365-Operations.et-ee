---
title: Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantide jaoks
description: Selles teemas selgitatakse, kuidas seadistada tootenumbri nomenklatuuri eelmääratletud tootevariantide jaoks ja kuidas määrata see sobivale tootedimensiooni grupile.
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 073b680c48855b2a8902c19cedfbf98cdbfdf17d
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150043"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="2abd6-103">Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantide jaoks</span><span class="sxs-lookup"><span data-stu-id="2abd6-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2abd6-104">Selles teemas selgitatakse, kuidas seadistada tootenumbri nomenklatuuri eelmääratletud tootevariantide jaoks ja kuidas määrata see sobivale tootedimensiooni grupile.</span><span class="sxs-lookup"><span data-stu-id="2abd6-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="2abd6-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="2abd6-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="2abd6-106">Uus tootenumbri nomenklatuur on määratud tootedimensioonigrupile Värv ja Suurus.</span><span class="sxs-lookup"><span data-stu-id="2abd6-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="2abd6-107">Enamasti teeb selle toimingu toote koostaja.</span><span class="sxs-lookup"><span data-stu-id="2abd6-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="2abd6-108">Tootenumbri nomenklatuuri loomine</span><span class="sxs-lookup"><span data-stu-id="2abd6-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="2abd6-109">Valige **Tootevariandi mudeli määratlus**.</span><span class="sxs-lookup"><span data-stu-id="2abd6-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="2abd6-110">Valige **Toote nomenklatuur**.</span><span class="sxs-lookup"><span data-stu-id="2abd6-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="2abd6-111">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2abd6-111">Select **New**.</span></span>
4. <span data-ttu-id="2abd6-112">Väljale **Nimi** sisestage nomenklatuuri nimi, mis aitab tuvastada sihttoote dimensiooni grupi, näiteks `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="2abd6-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="2abd6-113">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="2abd6-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="2abd6-114">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2abd6-114">Select **Add**.</span></span>
7. <span data-ttu-id="2abd6-115">Valige **Tooteetaloni** number.</span><span class="sxs-lookup"><span data-stu-id="2abd6-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="2abd6-116">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2abd6-116">Select **Add**.</span></span>
9. <span data-ttu-id="2abd6-117">Valige **Tekstikonstant**.</span><span class="sxs-lookup"><span data-stu-id="2abd6-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="2abd6-118">**Sisestage väärtus väljale Tekst.**</span><span class="sxs-lookup"><span data-stu-id="2abd6-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="2abd6-119">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2abd6-119">Select **Add**.</span></span>
12. <span data-ttu-id="2abd6-120">Valige **Värv**.</span><span class="sxs-lookup"><span data-stu-id="2abd6-120">Select **Color**.</span></span>
13. <span data-ttu-id="2abd6-121">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2abd6-121">Select **Add**.</span></span>
14. <span data-ttu-id="2abd6-122">Valige **Tekstikonstant**.</span><span class="sxs-lookup"><span data-stu-id="2abd6-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="2abd6-123">**Sisestage väärtus väljale Tekst.**</span><span class="sxs-lookup"><span data-stu-id="2abd6-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="2abd6-124">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2abd6-124">Select **Add**.</span></span>
17. <span data-ttu-id="2abd6-125">Valige **Suurus**.</span><span class="sxs-lookup"><span data-stu-id="2abd6-125">Select **Size**.</span></span>
18. <span data-ttu-id="2abd6-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2abd6-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="2abd6-127">Nomenklatuuri määramine tooteetalonile</span><span class="sxs-lookup"><span data-stu-id="2abd6-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="2abd6-128">Valige **Toote dimensiooni grupid**.</span><span class="sxs-lookup"><span data-stu-id="2abd6-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="2abd6-129">Valige rühm **SizeCol dimensioon**.</span><span class="sxs-lookup"><span data-stu-id="2abd6-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="2abd6-130">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="2abd6-130">Select **Edit**.</span></span>
4. <span data-ttu-id="2abd6-131">Valige väärtus **Jah** väljal **Kasuta nomenklatuuri**.</span><span class="sxs-lookup"><span data-stu-id="2abd6-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="2abd6-132">Väljale **Tootevariandi numbri nomenklatuur** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="2abd6-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="2abd6-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2abd6-133">Close the page.</span></span>

