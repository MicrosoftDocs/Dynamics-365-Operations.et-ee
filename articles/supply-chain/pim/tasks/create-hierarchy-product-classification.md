---
title: Tooteklassifikatsiooni hierarhia loomine
description: See protseduur selgitab, kuidas luua uut kategooriahierarhiat ja määrata kaubaartikli koodi hierarhiatüüpi.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb49f5f3f8a5a788cb4c6d1be69534ba808e3675
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "346820"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="81422-103">Tooteklassifikatsiooni hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="81422-103">Create a hierarchy of product classification</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="81422-104">See protseduur selgitab, kuidas luua uut kategooriahierarhiat ja määrata kaubaartikli koodi hierarhiatüüpi.</span><span class="sxs-lookup"><span data-stu-id="81422-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="81422-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="81422-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="81422-106">See protseduur on mõeldud kategooriajuhile.</span><span class="sxs-lookup"><span data-stu-id="81422-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="81422-107">Uue kategooriahierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="81422-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="81422-108">Minge jaotisse Tooteteabe haldus > Seadistus > Kategooriad ja atribuudid > Kategooriahierarhiad.</span><span class="sxs-lookup"><span data-stu-id="81422-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="81422-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="81422-109">Click New.</span></span>
3. <span data-ttu-id="81422-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="81422-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="81422-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="81422-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="81422-112">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="81422-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="81422-113">Hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="81422-113">Build the hierarchy</span></span>
1. <span data-ttu-id="81422-114">Klõpsake suvandit Uus kategooriasõlm.</span><span class="sxs-lookup"><span data-stu-id="81422-114">Click New category node.</span></span>
2. <span data-ttu-id="81422-115">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="81422-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="81422-116">Sisestage väärtus väljale Kood.</span><span class="sxs-lookup"><span data-stu-id="81422-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="81422-117">Sisestage väärtus väljale Hüüdnimi.</span><span class="sxs-lookup"><span data-stu-id="81422-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="81422-118">Klõpsake suvandit Uus kategooriasõlm.</span><span class="sxs-lookup"><span data-stu-id="81422-118">Click New category node.</span></span>
6. <span data-ttu-id="81422-119">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="81422-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="81422-120">Sisestage väärtus väljale Kood.</span><span class="sxs-lookup"><span data-stu-id="81422-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="81422-121">Sisestage väärtus väljale Hüüdnimi.</span><span class="sxs-lookup"><span data-stu-id="81422-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="81422-122">Klõpsake suvandit Uus kategooriasõlm.</span><span class="sxs-lookup"><span data-stu-id="81422-122">Click New category node.</span></span>
10. <span data-ttu-id="81422-123">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="81422-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="81422-124">Sisestage väärtus väljale Kood.</span><span class="sxs-lookup"><span data-stu-id="81422-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="81422-125">Sisestage väärtus väljale Hüüdnimi.</span><span class="sxs-lookup"><span data-stu-id="81422-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="81422-126">Klõpsake suvandit Uus kategooriasõlm.</span><span class="sxs-lookup"><span data-stu-id="81422-126">Click New category node.</span></span>
14. <span data-ttu-id="81422-127">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="81422-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="81422-128">Sisestage väärtus väljale Kood.</span><span class="sxs-lookup"><span data-stu-id="81422-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="81422-129">Sisestage väärtus väljale Hüüdnimi.</span><span class="sxs-lookup"><span data-stu-id="81422-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="81422-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="81422-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="81422-131">Hierarhia klassifitseerimine</span><span class="sxs-lookup"><span data-stu-id="81422-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="81422-132">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="81422-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="81422-133">Klõpsake toimingupaanil suvandit Kategooriahierarhia.</span><span class="sxs-lookup"><span data-stu-id="81422-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="81422-134">Klõpsake suvandit Hierarhiatüübi seostamine.</span><span class="sxs-lookup"><span data-stu-id="81422-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="81422-135">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="81422-135">Click New.</span></span>
5. <span data-ttu-id="81422-136">Valige suvand väljal Kategoooriahierarhia tüüp.</span><span class="sxs-lookup"><span data-stu-id="81422-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="81422-137">Valige toote klassifitseerimiseks suvand Kaubaartikli koodi kategooriahierarhia tüüp.</span><span class="sxs-lookup"><span data-stu-id="81422-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="81422-138">Klõpsake väljal Kategooriahierarhia otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="81422-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="81422-139">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="81422-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="81422-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="81422-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="81422-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="81422-141">Close the page.</span></span>

