---
title: Tooteklassifikatsiooni hierarhia loomine
description: See protseduur selgitab, kuidas luua uut kategooriahierarhiat ja määrata kaubaartikli koodi hierarhiatüüpi.
author: ShylaThompson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategoryHierarchyCreate, EcoResCategory, EcoResCategoryHierarchyRole
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: faf43eb15283ffd7e36ad38728f166884dddcd85
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844821"
---
# <a name="create-a-hierarchy-of-product-classification"></a><span data-ttu-id="b5112-103">Tooteklassifikatsiooni hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="b5112-103">Create a hierarchy of product classification</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b5112-104">See protseduur selgitab, kuidas luua uut kategooriahierarhiat ja määrata kaubaartikli koodi hierarhiatüüpi.</span><span class="sxs-lookup"><span data-stu-id="b5112-104">This procedure shows how to create a new category hierarchy and assign a commodity code hierarchy type.</span></span> <span data-ttu-id="b5112-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="b5112-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b5112-106">See protseduur on mõeldud kategooriajuhile.</span><span class="sxs-lookup"><span data-stu-id="b5112-106">This procedure is intended for the category manager.</span></span>


## <a name="create-the-new-category-hierarchy"></a><span data-ttu-id="b5112-107">Uue kategooriahierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="b5112-107">Create the new category hierarchy</span></span>
1. <span data-ttu-id="b5112-108">Avage **Navigeerimispaan > Moodulid > Toote teabe haldus > Häälestus > Kategooriad ja atribuudid > Kategooriahierarhia**.</span><span class="sxs-lookup"><span data-stu-id="b5112-108">Go to **Navigation pane > Modules > Product information management > Setup > Categories and attributes > Category hierarchies**.</span></span>
2. <span data-ttu-id="b5112-109">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b5112-109">Click **New**.</span></span>
3. <span data-ttu-id="b5112-110">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="b5112-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="b5112-111">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="b5112-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="b5112-112">Klõpsake käsku **Loo**.</span><span class="sxs-lookup"><span data-stu-id="b5112-112">Click **Create**.</span></span>

## <a name="build-the-hierarchy"></a><span data-ttu-id="b5112-113">Hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="b5112-113">Build the hierarchy</span></span>
1. <span data-ttu-id="b5112-114">Klõpsake **Uus** kategooria sõlm.</span><span class="sxs-lookup"><span data-stu-id="b5112-114">Click **New** category node.</span></span>
2. <span data-ttu-id="b5112-115">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="b5112-115">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="b5112-116">Sisestage väärtus väljale **Kood**.</span><span class="sxs-lookup"><span data-stu-id="b5112-116">In the **Code** field, type a value.</span></span>
4. <span data-ttu-id="b5112-117">Sisestage väärtus väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="b5112-117">In the **Friendly name** field, type a value.</span></span>
5. <span data-ttu-id="b5112-118">Klõpsake **Uus** kategooria sõlm.</span><span class="sxs-lookup"><span data-stu-id="b5112-118">Click **New** category node.</span></span>
6. <span data-ttu-id="b5112-119">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="b5112-119">In the **Name** field, type a value.</span></span>
7. <span data-ttu-id="b5112-120">Sisestage väärtus väljale **Kood**.</span><span class="sxs-lookup"><span data-stu-id="b5112-120">In the **Code** field, type a value.</span></span>
8. <span data-ttu-id="b5112-121">Sisestage väärtus väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="b5112-121">In the **Friendly name** field, type a value.</span></span>
9. <span data-ttu-id="b5112-122">Klõpsake **Uus** kategooria sõlm.</span><span class="sxs-lookup"><span data-stu-id="b5112-122">Click **New** category node.</span></span>
10. <span data-ttu-id="b5112-123">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="b5112-123">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="b5112-124">Sisestage väärtus väljale **Kood**.</span><span class="sxs-lookup"><span data-stu-id="b5112-124">In the **Code** field, type a value.</span></span>
12. <span data-ttu-id="b5112-125">Sisestage väärtus väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="b5112-125">In the **Friendly name** field, type a value.</span></span>
13. <span data-ttu-id="b5112-126">Klõpsake **Uus** kategooria sõlm.</span><span class="sxs-lookup"><span data-stu-id="b5112-126">Click **New** category node.</span></span>
14. <span data-ttu-id="b5112-127">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="b5112-127">In the **Name** field, type a value.</span></span>
15. <span data-ttu-id="b5112-128">Sisestage väärtus väljale **Kood**.</span><span class="sxs-lookup"><span data-stu-id="b5112-128">In the **Code** field, type a value.</span></span>
16. <span data-ttu-id="b5112-129">Sisestage väärtus väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="b5112-129">In the **Friendly name** field, type a value.</span></span>
17. <span data-ttu-id="b5112-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b5112-130">Close the page.</span></span>

## <a name="classify-the-hierarchy"></a><span data-ttu-id="b5112-131">Hierarhia klassifitseerimine</span><span class="sxs-lookup"><span data-stu-id="b5112-131">Classify the hierarchy</span></span>
1. <span data-ttu-id="b5112-132">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b5112-132">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="b5112-133">**Toimingupaanil** klõpsake **Kategooriahierarhia**.</span><span class="sxs-lookup"><span data-stu-id="b5112-133">On the **Action Pane**, click **Category hierarchy**.</span></span>
3. <span data-ttu-id="b5112-134">Klõpsake suvandit **Hierarhiatüübi seostamine**.</span><span class="sxs-lookup"><span data-stu-id="b5112-134">Click **Associate hierarchy type**.</span></span>
4. <span data-ttu-id="b5112-135">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b5112-135">Click **New**.</span></span>
5. <span data-ttu-id="b5112-136">Valige suvand väljal **Kategooriahierarhia tüüp**.</span><span class="sxs-lookup"><span data-stu-id="b5112-136">In the **Category hierarchy type** field, select an option.</span></span> <span data-ttu-id="b5112-137">Valige **Kaubakoodide kategooria hierarhiatüüp toote klassifikatsiooniks**.</span><span class="sxs-lookup"><span data-stu-id="b5112-137">Select the **Commodity code category hierarchy type for product classification**.</span></span>  
6. <span data-ttu-id="b5112-138">Klõpsake väljal **Kategooriahierarhia** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b5112-138">In the **Category hierarchy** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="b5112-139">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b5112-139">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="b5112-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b5112-140">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b5112-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b5112-141">Close the page.</span></span>

