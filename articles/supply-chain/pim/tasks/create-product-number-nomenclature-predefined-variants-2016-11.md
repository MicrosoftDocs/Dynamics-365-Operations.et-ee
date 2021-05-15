---
title: Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantide jaoks
description: Selles teemas selgitatakse, kuidas seadistada tootenumbri nomenklatuuri eelmääratletud tootevariantide jaoks ja kuidas määrata see sobivale tootedimensiooni grupile.
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920653"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="ef71e-103">Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantide jaoks</span><span class="sxs-lookup"><span data-stu-id="ef71e-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ef71e-104">Selles teemas selgitatakse, kuidas seadistada tootenumbri nomenklatuuri eelmääratletud tootevariantide jaoks ja kuidas määrata see sobivale tootedimensiooni grupile.</span><span class="sxs-lookup"><span data-stu-id="ef71e-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="ef71e-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="ef71e-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ef71e-106">Uus tootenumbri nomenklatuur on määratud tootedimensioonigrupile Värv ja Suurus.</span><span class="sxs-lookup"><span data-stu-id="ef71e-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="ef71e-107">Enamasti teeb selle toimingu toote koostaja.</span><span class="sxs-lookup"><span data-stu-id="ef71e-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="ef71e-108">Tootenumbri nomenklatuuri loomine</span><span class="sxs-lookup"><span data-stu-id="ef71e-108">Create a product number nomenclature</span></span>

1. <span data-ttu-id="ef71e-109">Avage **Tooteteabe haldus \> Seadistamine \> Tootenomenklatuurid**.</span><span class="sxs-lookup"><span data-stu-id="ef71e-109">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="ef71e-110">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ef71e-110">Select **New**.</span></span>
1. <span data-ttu-id="ef71e-111">Väljale **Nimi** sisestage nomenklatuuri nimi, mis aitab tuvastada sihttoote dimensiooni grupi, näiteks `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="ef71e-111">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
1. <span data-ttu-id="ef71e-112">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="ef71e-112">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="ef71e-113">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ef71e-113">Select **Add**.</span></span>
1. <span data-ttu-id="ef71e-114">Valige **Tooteetaloni** number.</span><span class="sxs-lookup"><span data-stu-id="ef71e-114">Select **Product master** number.</span></span>
1. <span data-ttu-id="ef71e-115">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ef71e-115">Select **Add**.</span></span>
1. <span data-ttu-id="ef71e-116">Valige **Tekstikonstant**.</span><span class="sxs-lookup"><span data-stu-id="ef71e-116">Select **Text constant**.</span></span>
1. <span data-ttu-id="ef71e-117">**Sisestage väärtus väljale Tekst.**</span><span class="sxs-lookup"><span data-stu-id="ef71e-117">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="ef71e-118">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ef71e-118">Select **Add**.</span></span>
1. <span data-ttu-id="ef71e-119">Valige **Värv**.</span><span class="sxs-lookup"><span data-stu-id="ef71e-119">Select **Color**.</span></span>
1. <span data-ttu-id="ef71e-120">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ef71e-120">Select **Add**.</span></span>
1. <span data-ttu-id="ef71e-121">Valige **Tekstikonstant**.</span><span class="sxs-lookup"><span data-stu-id="ef71e-121">Select **Text constant**.</span></span>
1. <span data-ttu-id="ef71e-122">**Sisestage väärtus väljale Tekst.**</span><span class="sxs-lookup"><span data-stu-id="ef71e-122">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="ef71e-123">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ef71e-123">Select **Add**.</span></span>
1. <span data-ttu-id="ef71e-124">Valige **Suurus**.</span><span class="sxs-lookup"><span data-stu-id="ef71e-124">Select **Size**.</span></span>
1. <span data-ttu-id="ef71e-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ef71e-125">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="ef71e-126">Nomenklatuuri määramine tooteetalonile</span><span class="sxs-lookup"><span data-stu-id="ef71e-126">Assign the nomenclature to a product master</span></span>

1. <span data-ttu-id="ef71e-127">Valige **Toote dimensiooni grupid**.</span><span class="sxs-lookup"><span data-stu-id="ef71e-127">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="ef71e-128">Valige rühm **SizeCol dimensioon**.</span><span class="sxs-lookup"><span data-stu-id="ef71e-128">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="ef71e-129">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ef71e-129">Select **Edit**.</span></span>
4. <span data-ttu-id="ef71e-130">Valige väärtus **Jah** väljal **Kasuta nomenklatuuri**.</span><span class="sxs-lookup"><span data-stu-id="ef71e-130">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="ef71e-131">Väljale **Tootevariandi numbri nomenklatuur** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="ef71e-131">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="ef71e-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ef71e-132">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]