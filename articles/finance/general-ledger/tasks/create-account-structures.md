---
title: Kontostruktuuride loomine
description: See ülesandejuhend kirjeldab konto struktuuri loomise etappe.
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aece2b79633802d28ba3b4fd8b51788e26c17a67
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815160"
---
# <a name="create-account-structures"></a><span data-ttu-id="16b20-103">Kontostruktuuride loomine</span><span class="sxs-lookup"><span data-stu-id="16b20-103">Create account structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="16b20-104">See ülesandejuhend kirjeldab konto struktuuri loomise etappe.</span><span class="sxs-lookup"><span data-stu-id="16b20-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="16b20-105">Etapid kasutavad demoandmete ettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="16b20-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="16b20-106">Avage **Navigeerimispaan > Moodulid > Pearaamat > Kontoplaan > Struktuurid > Konfigureeri konto struktuure**.</span><span class="sxs-lookup"><span data-stu-id="16b20-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="16b20-107">Rippdialoogi avamiseks klõpsake paanil **Toimingupaan** nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="16b20-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="16b20-108">Väljale **Konto struktuur** sisestage nimi, mis kirjeldab konto struktuuri eesmärki.</span><span class="sxs-lookup"><span data-stu-id="16b20-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="16b20-109">Väljale **Kirjeldus** sisestage kirjeldus, mis täpsustab konto struktuuri eesmärki.</span><span class="sxs-lookup"><span data-stu-id="16b20-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="16b20-110">Klõpsake käsku **Loo**.</span><span class="sxs-lookup"><span data-stu-id="16b20-110">Click **Create**.</span></span>
6. <span data-ttu-id="16b20-111">Suvandis **Segmendid ja lubatud väärtused** klõpsake käsku **Lisa segment**.</span><span class="sxs-lookup"><span data-stu-id="16b20-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="16b20-112">Dimensioonide loendist valige dimensioon, mille soovite lisada konto struktuuri.</span><span class="sxs-lookup"><span data-stu-id="16b20-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="16b20-113">Loendi lõpus klõpsake käsku **Lisa segment**.</span><span class="sxs-lookup"><span data-stu-id="16b20-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="16b20-114">Korrake etappe 6 ja 9 vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="16b20-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="16b20-115">Jaotises **Lubatud väärtuse üksikasjad** valige segment, et redigeerida lubatud väärtusi.</span><span class="sxs-lookup"><span data-stu-id="16b20-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="16b20-116">Näiteks klõpsake välja **Põhikonto**.</span><span class="sxs-lookup"><span data-stu-id="16b20-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="16b20-117">Väljal **Tehtemärk** valige suvand, näiteks "on vahemikus ja hõlmab".</span><span class="sxs-lookup"><span data-stu-id="16b20-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="16b20-118">Sisestage väärtus väljale **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="16b20-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="16b20-119">Näiteks 600 000.</span><span class="sxs-lookup"><span data-stu-id="16b20-119">For example, 600000.</span></span>  
13. <span data-ttu-id="16b20-120">Sisestage väärtus väljale **Kuni**.</span><span class="sxs-lookup"><span data-stu-id="16b20-120">In the **through** field, type a value.</span></span> <span data-ttu-id="16b20-121">Näiteks 699 999.</span><span class="sxs-lookup"><span data-stu-id="16b20-121">For example, 699999.</span></span>  
14. <span data-ttu-id="16b20-122">Jaotises **Lubatud väärtuse üksikasjad** klõpsake käsku **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="16b20-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="16b20-123">Korrake etappe 10 ja 15 vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="16b20-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="16b20-124">Jaotises **Lubatud väärtuse üksikasjad** klõpsake käsku **Lisa uus kriteerium**.</span><span class="sxs-lookup"><span data-stu-id="16b20-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="16b20-125">Väljal Tehtemärk valige suvand, näiteks "on vahemikus ja hõlmab".</span><span class="sxs-lookup"><span data-stu-id="16b20-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="16b20-126">Sisestage väärtus väljale **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="16b20-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="16b20-127">Näiteks 033.</span><span class="sxs-lookup"><span data-stu-id="16b20-127">For example, 033.</span></span>  
19. <span data-ttu-id="16b20-128">Sisestage väärtus väljale **Kuni**.</span><span class="sxs-lookup"><span data-stu-id="16b20-128">In the **through** field, type a value.</span></span> <span data-ttu-id="16b20-129">Näiteks 034.</span><span class="sxs-lookup"><span data-stu-id="16b20-129">For example, 034.</span></span>  
20. <span data-ttu-id="16b20-130">Klõpsake käsku **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="16b20-130">Click **Apply**.</span></span>
21. <span data-ttu-id="16b20-131">Valige ruudustikus segment, mille lubatud väärtusi soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="16b20-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="16b20-132">Näiteks Kulukeskus.</span><span class="sxs-lookup"><span data-stu-id="16b20-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="16b20-133">Sisestage väärtus väljale **Kulukeskus**.</span><span class="sxs-lookup"><span data-stu-id="16b20-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="16b20-134">Näiteks 007 … 021.</span><span class="sxs-lookup"><span data-stu-id="16b20-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="16b20-135">Suvandis **Segmendid ja lubatud väärtused** klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="16b20-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="16b20-136">Sisestage väärtus väljale **Põhikonto**.</span><span class="sxs-lookup"><span data-stu-id="16b20-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="16b20-137">Näiteks 600 000 … 699 999</span><span class="sxs-lookup"><span data-stu-id="16b20-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="16b20-138">Valige ruudustikus segment, mille lubatud väärtusi soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="16b20-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="16b20-139">Näiteks Osakond.</span><span class="sxs-lookup"><span data-stu-id="16b20-139">For example, Department.</span></span>  
26. <span data-ttu-id="16b20-140">Sisestage väärtus väljale Osakond.</span><span class="sxs-lookup"><span data-stu-id="16b20-140">In the Department field, type a value.</span></span> <span data-ttu-id="16b20-141">Näiteks 032.</span><span class="sxs-lookup"><span data-stu-id="16b20-141">For example, 032.</span></span>  
27. <span data-ttu-id="16b20-142">Sisestage väärtus väljale Kulukeskus.</span><span class="sxs-lookup"><span data-stu-id="16b20-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="16b20-143">Näiteks 086.</span><span class="sxs-lookup"><span data-stu-id="16b20-143">For example, 086.</span></span>  
28. <span data-ttu-id="16b20-144">Paanil **Toimingupaan** klõpsake käsku **Kontrolli**.</span><span class="sxs-lookup"><span data-stu-id="16b20-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="16b20-145">Paanil **Toimingupaan** klõpsake käsku **Aktiveeri**.</span><span class="sxs-lookup"><span data-stu-id="16b20-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="16b20-146">Klõpsake käsku **Aktiveeri**.</span><span class="sxs-lookup"><span data-stu-id="16b20-146">Click **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]