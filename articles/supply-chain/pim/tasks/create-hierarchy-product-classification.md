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
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 439df63a4f8f0cc1c030554d18f80e9934c88b00
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426260"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="bdf82-103">Tooteklassifikatsiooni hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="bdf82-103">Create a hierarchy of product classification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bdf82-104">See protseduur selgitab, kuidas luua uut kategooriahierarhiat ja määrata kaubaartikli koodi hierarhiatüüpi.</span><span class="sxs-lookup"><span data-stu-id="bdf82-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="bdf82-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="bdf82-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="bdf82-106">See protseduur on mõeldud kategooriajuhile.</span><span class="sxs-lookup"><span data-stu-id="bdf82-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="bdf82-107">Uue kategooriahierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="bdf82-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="bdf82-108">Avage **Navigeerimispaan > Moodulid > Toote teabe haldus > Häälestus > Kategooriad ja atribuudid > Kategooriahierarhia**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="bdf82-109">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-109">Click **New**.</span></span>
3. <span data-ttu-id="bdf82-110">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="bdf82-111">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="bdf82-112">Klõpsake käsku **Loo**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="bdf82-113">Hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="bdf82-113">Build the hierarchy</span></span>
1. <span data-ttu-id="bdf82-114">Klõpsake **Uus** kategooria sõlm.</span><span class="sxs-lookup"><span data-stu-id="bdf82-114">Click **New** category node.</span></span>
2. <span data-ttu-id="bdf82-115">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="bdf82-116">Sisestage väärtus väljale **Kood**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="bdf82-117">Sisestage väärtus väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="bdf82-118">Klõpsake **Uus** kategooria sõlm.</span><span class="sxs-lookup"><span data-stu-id="bdf82-118">Click **New** category node.</span></span>
6. <span data-ttu-id="bdf82-119">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="bdf82-120">Sisestage väärtus väljale **Kood**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="bdf82-121">Sisestage väärtus väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="bdf82-122">Klõpsake **Uus** kategooria sõlm.</span><span class="sxs-lookup"><span data-stu-id="bdf82-122">Click **New** category node.</span></span>
10. <span data-ttu-id="bdf82-123">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="bdf82-124">Sisestage väärtus väljale **Kood**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="bdf82-125">Sisestage väärtus väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="bdf82-126">Klõpsake **Uus** kategooria sõlm.</span><span class="sxs-lookup"><span data-stu-id="bdf82-126">Click **New** category node.</span></span>
14. <span data-ttu-id="bdf82-127">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="bdf82-128">Sisestage väärtus väljale **Kood**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="bdf82-129">Sisestage väärtus väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="bdf82-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bdf82-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="bdf82-131">Hierarhia klassifitseerimine</span><span class="sxs-lookup"><span data-stu-id="bdf82-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="bdf82-132">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bdf82-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="bdf82-133">**Toimingupaanil** klõpsake **Kategooriahierarhia**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="bdf82-134">Klõpsake suvandit **Hierarhiatüübi seostamine**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="bdf82-135">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-135">Click **New**.</span></span>
5. <span data-ttu-id="bdf82-136">Valige suvand väljal **Kategooriahierarhia tüüp**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="bdf82-137">Valige **Kaubakoodide kategooria hierarhiatüüp toote klassifikatsiooniks**.</span><span class="sxs-lookup"><span data-stu-id="bdf82-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="bdf82-138">Klõpsake väljal **Kategooriahierarhia** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="bdf82-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="bdf82-139">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bdf82-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="bdf82-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="bdf82-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="bdf82-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bdf82-141">Close the page.</span></span>

