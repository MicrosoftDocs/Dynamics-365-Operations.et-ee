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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568416"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="aa8e3-103">Tooteklassifikatsiooni hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="aa8e3-103">Create a hierarchy of product classification</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aa8e3-104">See protseduur selgitab, kuidas luua uut kategooriahierarhiat ja määrata kaubaartikli koodi hierarhiatüüpi.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="aa8e3-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="aa8e3-106">See protseduur on mõeldud kategooriajuhile.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="aa8e3-107">Uue kategooriahierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="aa8e3-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="aa8e3-108">Minge jaotisse Tooteteabe haldus > Seadistus > Kategooriad ja atribuudid > Kategooriahierarhiad.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="aa8e3-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-109">Click New.</span></span>
3. <span data-ttu-id="aa8e3-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="aa8e3-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="aa8e3-112">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="aa8e3-113">Hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="aa8e3-113">Build the hierarchy</span></span>
1. <span data-ttu-id="aa8e3-114">Klõpsake suvandit Uus kategooriasõlm.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-114">Click New category node.</span></span>
2. <span data-ttu-id="aa8e3-115">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="aa8e3-116">Sisestage väärtus väljale Kood.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="aa8e3-117">Sisestage väärtus väljale Hüüdnimi.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="aa8e3-118">Klõpsake suvandit Uus kategooriasõlm.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-118">Click New category node.</span></span>
6. <span data-ttu-id="aa8e3-119">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="aa8e3-120">Sisestage väärtus väljale Kood.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="aa8e3-121">Sisestage väärtus väljale Hüüdnimi.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="aa8e3-122">Klõpsake suvandit Uus kategooriasõlm.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-122">Click New category node.</span></span>
10. <span data-ttu-id="aa8e3-123">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="aa8e3-124">Sisestage väärtus väljale Kood.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="aa8e3-125">Sisestage väärtus väljale Hüüdnimi.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="aa8e3-126">Klõpsake suvandit Uus kategooriasõlm.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-126">Click New category node.</span></span>
14. <span data-ttu-id="aa8e3-127">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="aa8e3-128">Sisestage väärtus väljale Kood.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="aa8e3-129">Sisestage väärtus väljale Hüüdnimi.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="aa8e3-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="aa8e3-131">Hierarhia klassifitseerimine</span><span class="sxs-lookup"><span data-stu-id="aa8e3-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="aa8e3-132">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="aa8e3-133">Klõpsake toimingupaanil suvandit Kategooriahierarhia.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="aa8e3-134">Klõpsake suvandit Hierarhiatüübi seostamine.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="aa8e3-135">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-135">Click New.</span></span>
5. <span data-ttu-id="aa8e3-136">Valige suvand väljal Kategoooriahierarhia tüüp.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="aa8e3-137">Valige toote klassifitseerimiseks suvand Kaubaartikli koodi kategooriahierarhia tüüp.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="aa8e3-138">Klõpsake väljal Kategooriahierarhia otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="aa8e3-139">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="aa8e3-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="aa8e3-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="aa8e3-141">Close the page.</span></span>

