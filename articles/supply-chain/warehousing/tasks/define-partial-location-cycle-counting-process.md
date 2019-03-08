---
title: 'Osalise asukoha tsüklilise inventuuriprotsessi määratlemine '
description: Kui kasutate inventuuri jaoks tsüklilise inventuuri plaane, saate juhtida tegelikke inventuuritöid, kui taotlete, et asukohas loendataks kogu vaba kaubavaru asemel ainult konkreetseid tooteid ja tootevariante.
author: ShylaThompson
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3aafb42cea1664b0629f57fe4492736601902cc1
ms.sourcegitcommit: bacad87e2b9146e08e6fe16af01356954eb90574
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2019
ms.locfileid: "373394"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="36f75-103">Osalise asukoha tsüklilise inventuuriprotsessi määratlemine </span><span class="sxs-lookup"><span data-stu-id="36f75-103">Define partial location cycle counting process</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="36f75-104">Kui kasutate inventuuri jaoks tsüklilise inventuuri plaane, saate juhtida tegelikke inventuuritöid, kui taotlete, et asukohas loendataks kogu vaba kaubavaru asemel ainult konkreetseid tooteid ja tootevariante.</span><span class="sxs-lookup"><span data-stu-id="36f75-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="36f75-105">Konkreetseid tooteid filtreerides saab laojuht vähendada ülevaatamise üldkulusid, vältida konsolideerimisvigu ja säästa aega.</span><span class="sxs-lookup"><span data-stu-id="36f75-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="36f75-106">Tavaliselt teostab seadistusülesanded laojuhataja.</span><span class="sxs-lookup"><span data-stu-id="36f75-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="36f75-107">Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="36f75-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="36f75-108">Tsüklilise inventuuri malli loomine</span><span class="sxs-lookup"><span data-stu-id="36f75-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="36f75-109">Avage Laohaldus > Seadistus > Töö > Töömallid.</span><span class="sxs-lookup"><span data-stu-id="36f75-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="36f75-110">Tehke väljal Töötellimuse tüüp valik „Tsükliline inventuur”.</span><span class="sxs-lookup"><span data-stu-id="36f75-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="36f75-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="36f75-111">Click New.</span></span>
4. <span data-ttu-id="36f75-112">Sisestage number väljale Seerianumber.</span><span class="sxs-lookup"><span data-stu-id="36f75-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="36f75-113">Sortimisjärjestus on kõige väiksemast numbrist suurima numbrini.</span><span class="sxs-lookup"><span data-stu-id="36f75-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="36f75-114">Väärtus peab olema suurem kui 0 (null).</span><span class="sxs-lookup"><span data-stu-id="36f75-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="36f75-115">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="36f75-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="36f75-116">Sisestage väärtus väljale Töömall.</span><span class="sxs-lookup"><span data-stu-id="36f75-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="36f75-117">Tippige väärtus väljale Töömalli kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="36f75-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="36f75-118">Sisestage või valige väärtus väljal Töökausta ID.</span><span class="sxs-lookup"><span data-stu-id="36f75-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="36f75-119">Sisestage arv väljale Töö prioriteet.</span><span class="sxs-lookup"><span data-stu-id="36f75-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="36f75-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="36f75-120">Click Save.</span></span>
11. <span data-ttu-id="36f75-121">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="36f75-121">Click New.</span></span>
12. <span data-ttu-id="36f75-122">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="36f75-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="36f75-123">Valige Töö tüübi väljal „Inventuur”.</span><span class="sxs-lookup"><span data-stu-id="36f75-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="36f75-124">Sisestage või valige väärtus väljal Tööklassi ID.</span><span class="sxs-lookup"><span data-stu-id="36f75-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="36f75-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="36f75-125">Click Save.</span></span>
16. <span data-ttu-id="36f75-126">Klõpsake valikut Töörea jaotused.</span><span class="sxs-lookup"><span data-stu-id="36f75-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="36f75-127">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="36f75-127">Click New.</span></span>
18. <span data-ttu-id="36f75-128">Sisestage number väljale Seerianumber.</span><span class="sxs-lookup"><span data-stu-id="36f75-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="36f75-129">Sortimisjärjestus on kõige väiksemast numbrist suurima numbrini.</span><span class="sxs-lookup"><span data-stu-id="36f75-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="36f75-130">Väärtus peab olema suurem kui 0 (null).</span><span class="sxs-lookup"><span data-stu-id="36f75-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="36f75-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="36f75-131">Click Save.</span></span>
20. <span data-ttu-id="36f75-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="36f75-132">Close the page.</span></span>
21. <span data-ttu-id="36f75-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="36f75-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="36f75-134">Tsükliline inventuuri plaani loomine</span><span class="sxs-lookup"><span data-stu-id="36f75-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="36f75-135">Avage Laohaldus > Seadistus > Tsükliline inventuur > Tsüklilise inventuuri plaanid.</span><span class="sxs-lookup"><span data-stu-id="36f75-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="36f75-136">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="36f75-136">Click New.</span></span>
3. <span data-ttu-id="36f75-137">Sisestage väärtus väljale Tsüklilise inventuuri plaani ID.</span><span class="sxs-lookup"><span data-stu-id="36f75-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="36f75-138">Sisestage väärtus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="36f75-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="36f75-139">Sisestage number väljale Tsükliliste inventuuride maksimumarv.</span><span class="sxs-lookup"><span data-stu-id="36f75-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="36f75-140">Sisestage või valige väärtus väljal Töömall.</span><span class="sxs-lookup"><span data-stu-id="36f75-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="36f75-141">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="36f75-141">Click New.</span></span>
8. <span data-ttu-id="36f75-142">Sisestage number väljale Seerianumber.</span><span class="sxs-lookup"><span data-stu-id="36f75-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="36f75-143">Sortimisjärjestus on kõige väiksemast numbrist suurima numbrini.</span><span class="sxs-lookup"><span data-stu-id="36f75-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="36f75-144">Väärtus peab olema suurem kui 0 (null).</span><span class="sxs-lookup"><span data-stu-id="36f75-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="36f75-145">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="36f75-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="36f75-146">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="36f75-146">Click Save.</span></span>
11. <span data-ttu-id="36f75-147">Klõpsake valikut Määratle tootepäring.</span><span class="sxs-lookup"><span data-stu-id="36f75-147">Click Define product query.</span></span>
12. <span data-ttu-id="36f75-148">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="36f75-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="36f75-149">Sisestage või valige väärtus väljal Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="36f75-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="36f75-150">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="36f75-150">Click OK.</span></span>
15. <span data-ttu-id="36f75-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="36f75-151">Close the page.</span></span>

