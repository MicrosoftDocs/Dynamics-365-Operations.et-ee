---
title: Kaastoodete jaoks materjaliplaani loomine
description: Tootmise planeerija plaanib materjalinõudeid valemi kaastoodete kaupade puhul.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e59ff769685677b0970dbc7d4c9d4d2c1e5b63d1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835954"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="dcf2d-103">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="dcf2d-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dcf2d-104">Tootmise planeerija plaanib materjalinõudeid valemi kaastoodete kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="dcf2d-105">Selle protseduuri loomiseks kasutati demoettevõtte USP2 andmeid.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="dcf2d-106">Kaastoote nõude loomine</span><span class="sxs-lookup"><span data-stu-id="dcf2d-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="dcf2d-107">Avage Vaikearmatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="dcf2d-108">Klõpsake valikut Müügitellimuse töötlemine ja päring.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="dcf2d-109">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-109">Click New.</span></span>
4. <span data-ttu-id="dcf2d-110">Klõpsake valikut Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-110">Click Sales order.</span></span>
5. <span data-ttu-id="dcf2d-111">Sisestage väärtus väljale Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="dcf2d-112">Näide: US-001.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-112">Example: US-001</span></span>  
6. <span data-ttu-id="dcf2d-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-113">Click OK.</span></span>
7. <span data-ttu-id="dcf2d-114">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="dcf2d-115">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-115">Example: P6003</span></span>  
8. <span data-ttu-id="dcf2d-116">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="dcf2d-117">Näide: 50000</span><span class="sxs-lookup"><span data-stu-id="dcf2d-117">Example: 50000</span></span>  
9. <span data-ttu-id="dcf2d-118">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="dcf2d-119">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="dcf2d-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="dcf2d-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-120">Close the page.</span></span>
2. <span data-ttu-id="dcf2d-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-121">Close the page.</span></span>
3. <span data-ttu-id="dcf2d-122">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-122">Click Master planning.</span></span>
4. <span data-ttu-id="dcf2d-123">Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="dcf2d-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dcf2d-125">Näide: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="dcf2d-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="dcf2d-126">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-126">Click Run.</span></span>
7. <span data-ttu-id="dcf2d-127">Laiendage või ahendage jaotist Kaasatavad kirjed.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="dcf2d-128">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-128">Click Filter.</span></span>
9. <span data-ttu-id="dcf2d-129">Valige loendist rida, mille väli = kaubakood.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="dcf2d-130">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="dcf2d-131">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-131">Example: P6003</span></span>  
11. <span data-ttu-id="dcf2d-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-132">Click OK.</span></span>
12. <span data-ttu-id="dcf2d-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-133">Click OK.</span></span>
13. <span data-ttu-id="dcf2d-134">Klõpsake valikut Planeeritud tellimused.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-134">Click Planned orders.</span></span>
14. <span data-ttu-id="dcf2d-135">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="dcf2d-136">Näiteks saate filtrida välja Kaubakood väärtuse P6000 järgi.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="dcf2d-137">Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="dcf2d-138">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="dcf2d-139">Valige mis tahes filtri tagastatud read.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="dcf2d-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="dcf2d-141">Laiendage või ahendage jaotist Sidumine.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="dcf2d-142">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dcf2d-143">Plaanitud tellimus on seotud kaastoote müügitellimusega.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="dcf2d-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="dcf2d-145">Kaastoote nõude loomine</span><span class="sxs-lookup"><span data-stu-id="dcf2d-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="dcf2d-146">Avage Vaikearmatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="dcf2d-147">Klõpsake valikut Müügitellimuse töötlemine ja päring.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="dcf2d-148">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-148">Click New.</span></span>
4. <span data-ttu-id="dcf2d-149">Klõpsake valikut Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-149">Click Sales order.</span></span>
5. <span data-ttu-id="dcf2d-150">Sisestage väärtus väljale Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="dcf2d-151">Näide: US-001.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-151">Example: US-001</span></span>  
6. <span data-ttu-id="dcf2d-152">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-152">Click OK.</span></span>
7. <span data-ttu-id="dcf2d-153">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="dcf2d-154">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-154">Example: P6003</span></span>  
8. <span data-ttu-id="dcf2d-155">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="dcf2d-156">Näide: 50000</span><span class="sxs-lookup"><span data-stu-id="dcf2d-156">Example: 50000</span></span>  
9. <span data-ttu-id="dcf2d-157">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="dcf2d-158">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="dcf2d-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="dcf2d-159">Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="dcf2d-160">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dcf2d-161">Näide: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="dcf2d-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="dcf2d-162">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-162">Click Run.</span></span>
4. <span data-ttu-id="dcf2d-163">Laiendage või ahendage jaotist Kaasatavad kirjed.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="dcf2d-164">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-164">Click Filter.</span></span>
6. <span data-ttu-id="dcf2d-165">Valige loendist rida, mille väli = kaubakood.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="dcf2d-166">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="dcf2d-167">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-167">Example: P6003</span></span>  
8. <span data-ttu-id="dcf2d-168">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-168">Click OK.</span></span>
9. <span data-ttu-id="dcf2d-169">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-169">Click OK.</span></span>
10. <span data-ttu-id="dcf2d-170">Klõpsake valikut Planeeritud tellimused.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-170">Click Planned orders.</span></span>
11. <span data-ttu-id="dcf2d-171">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="dcf2d-172">Näiteks saate filtrida välja Kaubakood väärtuse P6000 järgi.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="dcf2d-173">Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="dcf2d-174">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="dcf2d-175">Valige mis tahes filtri tagastatud read.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="dcf2d-176">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="dcf2d-177">Laiendage või ahendage jaotist Sidumine.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="dcf2d-178">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dcf2d-179">Plaanitud tellimus on seotud kaastoote müügitellimusega.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="dcf2d-180">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-180">Close the page.</span></span>
17. <span data-ttu-id="dcf2d-181">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-181">Click Master planning.</span></span>
18. <span data-ttu-id="dcf2d-182">Avage Koondplaneerimine > Seadistus > Koondplaneerimise parameetrid.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="dcf2d-183">Valige väljal Keela kõik planeerimisprotsessid suvand Ei.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="dcf2d-184">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dcf2d-184">Close the page.</span></span>

