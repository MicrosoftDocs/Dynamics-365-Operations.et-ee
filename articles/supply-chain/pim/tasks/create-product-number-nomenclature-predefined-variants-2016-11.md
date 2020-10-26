---
title: Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantide jaoks
description: Selles teemas selgitatakse, kuidas seadistada tootenumbri nomenklatuuri eelmääratletud tootevariantide jaoks ja kuidas määrata see sobivale tootedimensiooni grupile.
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6871765a450295a3f308ec7e706f1b126071585f
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986043"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="d6297-103">Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantide jaoks</span><span class="sxs-lookup"><span data-stu-id="d6297-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d6297-104">Selles teemas selgitatakse, kuidas seadistada tootenumbri nomenklatuuri eelmääratletud tootevariantide jaoks ja kuidas määrata see sobivale tootedimensiooni grupile.</span><span class="sxs-lookup"><span data-stu-id="d6297-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="d6297-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="d6297-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d6297-106">Uus tootenumbri nomenklatuur on määratud tootedimensioonigrupile Värv ja Suurus.</span><span class="sxs-lookup"><span data-stu-id="d6297-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="d6297-107">Enamasti teeb selle toimingu toote koostaja.</span><span class="sxs-lookup"><span data-stu-id="d6297-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="d6297-108">Tootenumbri nomenklatuuri loomine</span><span class="sxs-lookup"><span data-stu-id="d6297-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="d6297-109">Valige **Tootevariandi mudeli määratlus**.</span><span class="sxs-lookup"><span data-stu-id="d6297-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="d6297-110">Valige **Toote nomenklatuur**.</span><span class="sxs-lookup"><span data-stu-id="d6297-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="d6297-111">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d6297-111">Select **New**.</span></span>
4. <span data-ttu-id="d6297-112">Väljale **Nimi** sisestage nomenklatuuri nimi, mis aitab tuvastada sihttoote dimensiooni grupi, näiteks `ColorSize`.</span><span class="sxs-lookup"><span data-stu-id="d6297-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="d6297-113">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="d6297-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="d6297-114">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d6297-114">Select **Add**.</span></span>
7. <span data-ttu-id="d6297-115">Valige **Tooteetaloni** number.</span><span class="sxs-lookup"><span data-stu-id="d6297-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="d6297-116">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d6297-116">Select **Add**.</span></span>
9. <span data-ttu-id="d6297-117">Valige **Tekstikonstant**.</span><span class="sxs-lookup"><span data-stu-id="d6297-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="d6297-118">**Sisestage väärtus väljale Tekst.**</span><span class="sxs-lookup"><span data-stu-id="d6297-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="d6297-119">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d6297-119">Select **Add**.</span></span>
12. <span data-ttu-id="d6297-120">Valige **Värv**.</span><span class="sxs-lookup"><span data-stu-id="d6297-120">Select **Color**.</span></span>
13. <span data-ttu-id="d6297-121">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d6297-121">Select **Add**.</span></span>
14. <span data-ttu-id="d6297-122">Valige **Tekstikonstant**.</span><span class="sxs-lookup"><span data-stu-id="d6297-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="d6297-123">**Sisestage väärtus väljale Tekst.**</span><span class="sxs-lookup"><span data-stu-id="d6297-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="d6297-124">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d6297-124">Select **Add**.</span></span>
17. <span data-ttu-id="d6297-125">Valige **Suurus**.</span><span class="sxs-lookup"><span data-stu-id="d6297-125">Select **Size**.</span></span>
18. <span data-ttu-id="d6297-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d6297-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="d6297-127">Nomenklatuuri määramine tooteetalonile</span><span class="sxs-lookup"><span data-stu-id="d6297-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="d6297-128">Valige **Toote dimensiooni grupid**.</span><span class="sxs-lookup"><span data-stu-id="d6297-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="d6297-129">Valige rühm **SizeCol dimensioon**.</span><span class="sxs-lookup"><span data-stu-id="d6297-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="d6297-130">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="d6297-130">Select **Edit**.</span></span>
4. <span data-ttu-id="d6297-131">Valige väärtus **Jah** väljal **Kasuta nomenklatuuri**.</span><span class="sxs-lookup"><span data-stu-id="d6297-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="d6297-132">Väljale **Tootevariandi numbri nomenklatuur** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="d6297-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="d6297-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d6297-133">Close the page.</span></span>

