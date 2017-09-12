--- 
title: Tooteklassifikatsiooni hierarhia loomine
description: "See protseduur selgitab, kuidas luua uut kategooriahierarhiat ja määrata kaubaartikli koodi hierarhiatüüpi."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 46a5d21550cfe1728ee6ca468c4ad523beb719da
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="9df1d-103">Tooteklassifikatsiooni hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="9df1d-103">Create a hierarchy of product classification</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9df1d-104">See protseduur selgitab, kuidas luua uut kategooriahierarhiat ja määrata kaubaartikli koodi hierarhiatüüpi.</span><span class="sxs-lookup"><span data-stu-id="9df1d-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="9df1d-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="9df1d-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9df1d-106">See protseduur on mõeldud kategooriajuhile.</span><span class="sxs-lookup"><span data-stu-id="9df1d-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="9df1d-107">Uue kategooriahierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="9df1d-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="9df1d-108">Minge jaotisse Tooteteabe haldus > Seadistus > Kategooriad ja atribuudid > Kategooriahierarhiad.</span><span class="sxs-lookup"><span data-stu-id="9df1d-108">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="9df1d-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9df1d-109">Click New.</span></span>
3. <span data-ttu-id="9df1d-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="9df1d-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9df1d-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="9df1d-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9df1d-112">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="9df1d-112">Click Create.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="9df1d-113">Hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="9df1d-113">Build the hierarchy</span></span>
1. <span data-ttu-id="9df1d-114">Klõpsake suvandit Uus kategooriasõlm.</span><span class="sxs-lookup"><span data-stu-id="9df1d-114">Click New category node.</span></span>
2. <span data-ttu-id="9df1d-115">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="9df1d-115">In the Name field, type a value.</span></span>
3. <span data-ttu-id="9df1d-116">Sisestage väärtus väljale Kood.</span><span class="sxs-lookup"><span data-stu-id="9df1d-116">In the Code field, type a value.</span></span>
4. <span data-ttu-id="9df1d-117">Sisestage väärtus väljale Hüüdnimi.</span><span class="sxs-lookup"><span data-stu-id="9df1d-117">In the Friendly name field, type a value.</span></span>
5. <span data-ttu-id="9df1d-118">Klõpsake suvandit Uus kategooriasõlm.</span><span class="sxs-lookup"><span data-stu-id="9df1d-118">Click New category node.</span></span>
6. <span data-ttu-id="9df1d-119">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="9df1d-119">In the Name field, type a value.</span></span>
7. <span data-ttu-id="9df1d-120">Sisestage väärtus väljale Kood.</span><span class="sxs-lookup"><span data-stu-id="9df1d-120">In the Code field, type a value.</span></span>
8. <span data-ttu-id="9df1d-121">Sisestage väärtus väljale Hüüdnimi.</span><span class="sxs-lookup"><span data-stu-id="9df1d-121">In the Friendly name field, type a value.</span></span>
9. <span data-ttu-id="9df1d-122">Klõpsake suvandit Uus kategooriasõlm.</span><span class="sxs-lookup"><span data-stu-id="9df1d-122">Click New category node.</span></span>
10. <span data-ttu-id="9df1d-123">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="9df1d-123">In the Name field, type a value.</span></span>
11. <span data-ttu-id="9df1d-124">Sisestage väärtus väljale Kood.</span><span class="sxs-lookup"><span data-stu-id="9df1d-124">In the Code field, type a value.</span></span>
12. <span data-ttu-id="9df1d-125">Sisestage väärtus väljale Hüüdnimi.</span><span class="sxs-lookup"><span data-stu-id="9df1d-125">In the Friendly name field, type a value.</span></span>
13. <span data-ttu-id="9df1d-126">Klõpsake suvandit Uus kategooriasõlm.</span><span class="sxs-lookup"><span data-stu-id="9df1d-126">Click New category node.</span></span>
14. <span data-ttu-id="9df1d-127">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="9df1d-127">In the Name field, type a value.</span></span>
15. <span data-ttu-id="9df1d-128">Sisestage väärtus väljale Kood.</span><span class="sxs-lookup"><span data-stu-id="9df1d-128">In the Code field, type a value.</span></span>
16. <span data-ttu-id="9df1d-129">Sisestage väärtus väljale Hüüdnimi.</span><span class="sxs-lookup"><span data-stu-id="9df1d-129">In the Friendly name field, type a value.</span></span>
17. <span data-ttu-id="9df1d-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9df1d-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="9df1d-131">Hierarhia klassifitseerimine</span><span class="sxs-lookup"><span data-stu-id="9df1d-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="9df1d-132">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9df1d-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="9df1d-133">Klõpsake toimingupaanil suvandit Kategooriahierarhia.</span><span class="sxs-lookup"><span data-stu-id="9df1d-133">On the Action Pane, click Category hierarchy.</span></span>
3. <span data-ttu-id="9df1d-134">Klõpsake suvandit Hierarhiatüübi seostamine.</span><span class="sxs-lookup"><span data-stu-id="9df1d-134">Click Associate hierarchy type.</span></span>
4. <span data-ttu-id="9df1d-135">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9df1d-135">Click New.</span></span>
5. <span data-ttu-id="9df1d-136">Valige suvand väljal Kategoooriahierarhia tüüp.</span><span class="sxs-lookup"><span data-stu-id="9df1d-136">In the Category hierarchy type field, select an option.</span></span>
    * <span data-ttu-id="9df1d-137">Valige toote klassifitseerimiseks suvand Kaubaartikli koodi kategooriahierarhia tüüp.</span><span class="sxs-lookup"><span data-stu-id="9df1d-137">Select the Commodity code category hierarchy type for product classification.</span></span>  
6. <span data-ttu-id="9df1d-138">Klõpsake väljal Kategooriahierarhia otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9df1d-138">In the Category hierarchy field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="9df1d-139">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9df1d-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="9df1d-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9df1d-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9df1d-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9df1d-141">Close the page.</span></span>


