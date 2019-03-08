---
title: Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantide jaoks
description: See juhend näitab, kuidas seadistada eelmääratletud tootevariantidele tootenumbri nomenklatuuri ja kuidas määrata seda sobivale tootedimensioonigrupile.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b49e96677b94d5f669ea41861f64e62e118938c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "364875"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="21de7-103">Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantide jaoks</span><span class="sxs-lookup"><span data-stu-id="21de7-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="21de7-104">See juhend näitab, kuidas seadistada eelmääratletud tootevariantidele tootenumbri nomenklatuuri ja kuidas määrata seda sobivale tootedimensioonigrupile.</span><span class="sxs-lookup"><span data-stu-id="21de7-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="21de7-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="21de7-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="21de7-106">Uus tootenumbri nomenklatuur on määratud tootedimensioonigrupile Värv ja Suurus.</span><span class="sxs-lookup"><span data-stu-id="21de7-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="21de7-107">Enamasti teeb selle toimingu toote koostaja.</span><span class="sxs-lookup"><span data-stu-id="21de7-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="21de7-108">Tootenumbri nomenklatuuri loomine</span><span class="sxs-lookup"><span data-stu-id="21de7-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="21de7-109">Klõpsake valikut Tootevariandi mudeli määratlus.</span><span class="sxs-lookup"><span data-stu-id="21de7-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="21de7-110">Klõpsake valikut Tootenomenklatuur.</span><span class="sxs-lookup"><span data-stu-id="21de7-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="21de7-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="21de7-111">Click New.</span></span>
4. <span data-ttu-id="21de7-112">Sisestage väljale Nimi nomenklatuuri nimi, mis aitab tuvastada siht-tootedimensioonigruppi, nt ColorSize.</span><span class="sxs-lookup"><span data-stu-id="21de7-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="21de7-113">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="21de7-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="21de7-114">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="21de7-114">Click Add.</span></span>
7. <span data-ttu-id="21de7-115">Klõpsake valikut Tooteetaloni number.</span><span class="sxs-lookup"><span data-stu-id="21de7-115">Click Product master number.</span></span>
8. <span data-ttu-id="21de7-116">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="21de7-116">Click Add.</span></span>
9. <span data-ttu-id="21de7-117">Klõpsake valikut Tekstikonstant.</span><span class="sxs-lookup"><span data-stu-id="21de7-117">Click Text constant.</span></span>
10. <span data-ttu-id="21de7-118">Sisestage väärtus väljale Tekst.</span><span class="sxs-lookup"><span data-stu-id="21de7-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="21de7-119">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="21de7-119">Click Add.</span></span>
12. <span data-ttu-id="21de7-120">Klõpsake valikut Värv.</span><span class="sxs-lookup"><span data-stu-id="21de7-120">Click Color.</span></span>
13. <span data-ttu-id="21de7-121">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="21de7-121">Click Add.</span></span>
14. <span data-ttu-id="21de7-122">Klõpsake valikut Tekstikonstant.</span><span class="sxs-lookup"><span data-stu-id="21de7-122">Click Text constant.</span></span>
15. <span data-ttu-id="21de7-123">Sisestage väärtus väljale Tekst.</span><span class="sxs-lookup"><span data-stu-id="21de7-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="21de7-124">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="21de7-124">Click Add.</span></span>
17. <span data-ttu-id="21de7-125">Klõpsake valikut Suurus.</span><span class="sxs-lookup"><span data-stu-id="21de7-125">Click Size.</span></span>
18. <span data-ttu-id="21de7-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="21de7-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="21de7-127">Nomenklatuuri määramine tooteetalonile</span><span class="sxs-lookup"><span data-stu-id="21de7-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="21de7-128">Klõpsake valikut Tootedimensioonigrupid.</span><span class="sxs-lookup"><span data-stu-id="21de7-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="21de7-129">Valige tootedimensioonigrupp SizeCol.</span><span class="sxs-lookup"><span data-stu-id="21de7-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="21de7-130">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="21de7-130">Click Edit.</span></span>
4. <span data-ttu-id="21de7-131">Tehke väljal Kasuta nomenklatuuri valik Jah.</span><span class="sxs-lookup"><span data-stu-id="21de7-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="21de7-132">Sisestage või valige väärtus väljal Tootevariandi numbri nomenklatuur.</span><span class="sxs-lookup"><span data-stu-id="21de7-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="21de7-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="21de7-133">Close the page.</span></span>

