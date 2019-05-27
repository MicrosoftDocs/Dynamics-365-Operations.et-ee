---
title: Kontostruktuuride loomine
description: See ülesandejuhend kirjeldab konto struktuuri loomise etappe.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7dd71cc072d49f47b1d77d3a688984cd4aaa624
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571278"
---
# <a name="create-account-structures"></a><span data-ttu-id="f8ad3-103">Kontostruktuuride loomine</span><span class="sxs-lookup"><span data-stu-id="f8ad3-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f8ad3-104">See ülesandejuhend kirjeldab konto struktuuri loomise etappe.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="f8ad3-105">Etapid kasutavad demoandmete ettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="f8ad3-106">Minge jaotisse Pearaamat > Kontoplaan > Struktuurid > Konto struktuuride konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-106">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
2. <span data-ttu-id="f8ad3-107">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-107">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="f8ad3-108">Sisestage väljale Konto struktuur nimi, mis kirjeldab konto struktuuri eesmärki.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-108">In the Account structure field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="f8ad3-109">Sisestage väljale Kirjeldus kirjeldus, mis määrab konto struktuuri eesmärgi.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-109">In the Description field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="f8ad3-110">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-110">Click Create.</span></span>
6. <span data-ttu-id="f8ad3-111">Klõpsake suvandit Segmendi lisamine.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-111">Click Add segment.</span></span>
7. <span data-ttu-id="f8ad3-112">Valige loendist Dimensioon konto struktuurile lisatav dimensioon.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-112">In the Dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="f8ad3-113">Klõpsake suvandit Segmendi lisamine.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-113">Click Add segment.</span></span>
9. <span data-ttu-id="f8ad3-114">Klõpsake suvandit Segmendi lisamine.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-114">Click Add segment.</span></span>
10. <span data-ttu-id="f8ad3-115">Valige loendist Dimensioon konto struktuurile lisatav dimensioon.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-115">In the Dimensions list, select the dimension to add to the account structure.</span></span>
11. <span data-ttu-id="f8ad3-116">Klõpsake suvandit Segmendi lisamine.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-116">Click Add segment.</span></span>
12. <span data-ttu-id="f8ad3-117">Klõpsake suvandit Segmendi lisamine.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-117">Click Add segment.</span></span>
13. <span data-ttu-id="f8ad3-118">Valige loendist Dimensioon konto struktuurile lisatav dimensioon.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-118">In the Dimensions list, select the dimension to add to the account structure.</span></span>
14. <span data-ttu-id="f8ad3-119">Klõpsake suvandit Segmendi lisamine.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-119">Click Add segment.</span></span>
15. <span data-ttu-id="f8ad3-120">Valige ruudustikus segment, mille lubatud väärtusi soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-120">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="f8ad3-121">Klõpsake näiteks suvandit Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-121">For example, click in Main Account.</span></span>  
16. <span data-ttu-id="f8ad3-122">Valige suvand väljal Operaator, näiteks „vahemikus ja hõlmab”.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-122">In the Operator field, select an option, such as is between and includes.</span></span>
17. <span data-ttu-id="f8ad3-123">Sisestage väärtus väljale Väärtus.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-123">In the Value field, type a value.</span></span>
    * <span data-ttu-id="f8ad3-124">Näiteks 600 000.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-124">For example, 600000.</span></span>  
18. <span data-ttu-id="f8ad3-125">Sisestage väärtus väljale Kuni.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-125">In the through field, type a value.</span></span>
    * <span data-ttu-id="f8ad3-126">Näiteks 699 999.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-126">For example, 699999.</span></span>  
19. <span data-ttu-id="f8ad3-127">Klõpsake käsku Apply (Rakenda).</span><span class="sxs-lookup"><span data-stu-id="f8ad3-127">Click Apply.</span></span>
20. <span data-ttu-id="f8ad3-128">Valige ruudustikus segment, mille lubatud väärtusi soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-128">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="f8ad3-129">Näiteks Osakond.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-129">For example, Department.</span></span>  
21. <span data-ttu-id="f8ad3-130">Valige suvand väljal Operaator, näiteks „vahemikus ja hõlmab”.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-130">In the Operator field, select an option, such as is between and includes.</span></span>
22. <span data-ttu-id="f8ad3-131">Sisestage väärtus väljale Väärtus.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-131">In the Value field, type a value.</span></span>
    * <span data-ttu-id="f8ad3-132">Näiteks 022.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-132">For example, 022.</span></span>  
23. <span data-ttu-id="f8ad3-133">Sisestage väärtus väljale Kuni.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-133">In the through field, type a value.</span></span>
    * <span data-ttu-id="f8ad3-134">Näiteks 031.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-134">For example, 031.</span></span>  
24. <span data-ttu-id="f8ad3-135">Klõpsake suvandit Uute kriteeriumide lisamine.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-135">Click Add new criteria.</span></span>
25. <span data-ttu-id="f8ad3-136">Valige suvand väljal Operaator, näiteks „vahemikus ja hõlmab”.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-136">In the Operator field, select an option, such as is between and includes.</span></span>
26. <span data-ttu-id="f8ad3-137">Sisestage väärtus väljale Väärtus.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-137">In the Value field, type a value.</span></span>
    * <span data-ttu-id="f8ad3-138">Näiteks 033.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-138">For example, 033.</span></span>  
27. <span data-ttu-id="f8ad3-139">Sisestage väärtus väljale Kuni.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-139">In the through field, type a value.</span></span>
    * <span data-ttu-id="f8ad3-140">Näiteks 034.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-140">For example, 034.</span></span>  
28. <span data-ttu-id="f8ad3-141">Klõpsake käsku Apply (Rakenda).</span><span class="sxs-lookup"><span data-stu-id="f8ad3-141">Click Apply.</span></span>
29. <span data-ttu-id="f8ad3-142">Valige ruudustikus segment, mille lubatud väärtusi soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-142">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="f8ad3-143">Näiteks Kulukeskus.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-143">For example, Cost Center.</span></span>  
30. <span data-ttu-id="f8ad3-144">Sisestage väärtus väljale CostCenter.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-144">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="f8ad3-145">Näiteks 007 … 021.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-145">For example, 007..021.</span></span>  
31. <span data-ttu-id="f8ad3-146">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-146">Click Add.</span></span>
32. <span data-ttu-id="f8ad3-147">Sisestage väärtus väljale MainAccount.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-147">In the MainAccount field, type a value.</span></span>
    * <span data-ttu-id="f8ad3-148">Näiteks 600 000 … 699 999</span><span class="sxs-lookup"><span data-stu-id="f8ad3-148">For example, 600000..699999</span></span>  
33. <span data-ttu-id="f8ad3-149">Valige ruudustikus segment, mille lubatud väärtusi soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-149">In the grid, select the segment to edit the allowed values.</span></span>
    * <span data-ttu-id="f8ad3-150">Näiteks Osakond.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-150">For example, Department.</span></span>  
34. <span data-ttu-id="f8ad3-151">Sisestage väärtus väljale Department.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-151">In the Department field, type a value.</span></span>
    * <span data-ttu-id="f8ad3-152">Näiteks 032.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-152">For example, 032.</span></span>  
35. <span data-ttu-id="f8ad3-153">Sisestage väärtus väljale CostCenter.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-153">In the CostCenter field, type a value.</span></span>
    * <span data-ttu-id="f8ad3-154">Näiteks 086.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-154">For example, 086.</span></span>  
36. <span data-ttu-id="f8ad3-155">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-155">Click Validate.</span></span>
37. <span data-ttu-id="f8ad3-156">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-156">Click Activate.</span></span>
38. <span data-ttu-id="f8ad3-157">Klõpsake käsku Aktiveeri.</span><span class="sxs-lookup"><span data-stu-id="f8ad3-157">Click Activate.</span></span>

