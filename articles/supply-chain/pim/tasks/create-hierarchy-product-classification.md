---
title: Tooteklassifikatsiooni hierarhia loomine
description: See protseduur selgitab, kuidas luua uut kategooriahierarhiat ja määrata kaubaartikli koodi hierarhiatüüpi.
author: ShylaThompson
manager: tfehr
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole, EcoResProductCategory, EcoResCategorySearchList, EcoResCategoryHierarchyFactbox, EcoResCategoryFriendlyName, EcoResCategoryAddProduct
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf414ca0a21ea8816eba9a5ef95c988dd31f0249
ms.sourcegitcommit: 59a9e840989bc9f2c7004efa3499b69c09a91b06
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677852"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="f2f58-103">Tooteklassifikatsiooni hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="f2f58-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2f58-104">See protseduur selgitab, kuidas luua uut kategooriahierarhiat ja määrata kaubaartikli koodi hierarhiatüüpi.</span><span class="sxs-lookup"><span data-stu-id="f2f58-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="f2f58-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="f2f58-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f2f58-106">See protseduur on mõeldud kategooriajuhile.</span><span class="sxs-lookup"><span data-stu-id="f2f58-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="f2f58-107">Uue kategooriahierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="f2f58-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="f2f58-108">Avage **Navigeerimispaan > Moodulid > Toote teabe haldus > Häälestus > Kategooriad ja atribuudid > Kategooriahierarhia**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="f2f58-109">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-109">Click **New**.</span></span>
3. <span data-ttu-id="f2f58-110">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="f2f58-111">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="f2f58-112">Klõpsake käsku **Loo**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="f2f58-113">Hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="f2f58-113">Build the hierarchy</span></span>
1. <span data-ttu-id="f2f58-114">Klõpsake **Uus** kategooria sõlm.</span><span class="sxs-lookup"><span data-stu-id="f2f58-114">Click **New** category node.</span></span>
2. <span data-ttu-id="f2f58-115">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="f2f58-116">Sisestage väärtus väljale **Kood**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="f2f58-117">Sisestage väärtus väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="f2f58-118">Klõpsake **Uus** kategooria sõlm.</span><span class="sxs-lookup"><span data-stu-id="f2f58-118">Click **New** category node.</span></span>
6. <span data-ttu-id="f2f58-119">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="f2f58-120">Sisestage väärtus väljale **Kood**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="f2f58-121">Sisestage väärtus väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="f2f58-122">Klõpsake **Uus** kategooria sõlm.</span><span class="sxs-lookup"><span data-stu-id="f2f58-122">Click **New** category node.</span></span>
10. <span data-ttu-id="f2f58-123">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="f2f58-124">Sisestage väärtus väljale **Kood**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="f2f58-125">Sisestage väärtus väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="f2f58-126">Klõpsake **Uus** kategooria sõlm.</span><span class="sxs-lookup"><span data-stu-id="f2f58-126">Click **New** category node.</span></span>
14. <span data-ttu-id="f2f58-127">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="f2f58-128">Sisestage väärtus väljale **Kood**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="f2f58-129">Sisestage väärtus väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="f2f58-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f2f58-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="f2f58-131">Hierarhia klassifitseerimine</span><span class="sxs-lookup"><span data-stu-id="f2f58-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="f2f58-132">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f2f58-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="f2f58-133">**Toimingupaanil** klõpsake **Kategooriahierarhia**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="f2f58-134">Klõpsake suvandit **Hierarhiatüübi seostamine**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="f2f58-135">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-135">Click **New**.</span></span>
5. <span data-ttu-id="f2f58-136">Valige suvand väljal **Kategooriahierarhia tüüp**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="f2f58-137">Valige **Kaubakoodide kategooria hierarhiatüüp toote klassifikatsiooniks**.</span><span class="sxs-lookup"><span data-stu-id="f2f58-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="f2f58-138">Klõpsake väljal **Kategooriahierarhia** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f2f58-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f2f58-139">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f2f58-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="f2f58-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f2f58-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f2f58-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f2f58-141">Close the page.</span></span>

