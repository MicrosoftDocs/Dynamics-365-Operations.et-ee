--- 
title: Kaastoodete jaoks materjaliplaani loomine
description: "Tootmise planeerija plaanib materjalinõudeid valemi kaastoodete kaupade puhul."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 2958f1e5c2e8a0cfa9cc6312f688d3b11b8e013c
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="f5fed-103">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="f5fed-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5fed-104">Tootmise planeerija plaanib materjalinõudeid valemi kaastoodete kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="f5fed-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="f5fed-105">Selle protseduuri loomiseks kasutati demoettevõtte USP2 andmeid.</span><span class="sxs-lookup"><span data-stu-id="f5fed-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="f5fed-106">Kaastoote nõude loomine</span><span class="sxs-lookup"><span data-stu-id="f5fed-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="f5fed-107">Avage Vaikearmatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="f5fed-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="f5fed-108">Klõpsake valikut Müügitellimuse töötlemine ja päring.</span><span class="sxs-lookup"><span data-stu-id="f5fed-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="f5fed-109">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="f5fed-109">Click New.</span></span>
4. <span data-ttu-id="f5fed-110">Klõpsake valikut Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="f5fed-110">Click Sales order.</span></span>
5. <span data-ttu-id="f5fed-111">Sisestage väärtus väljale Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="f5fed-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="f5fed-112">Näide: US-001.</span><span class="sxs-lookup"><span data-stu-id="f5fed-112">Example: US-001</span></span>  
6. <span data-ttu-id="f5fed-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f5fed-113">Click OK.</span></span>
7. <span data-ttu-id="f5fed-114">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="f5fed-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f5fed-115">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="f5fed-115">Example: P6003</span></span>  
8. <span data-ttu-id="f5fed-116">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="f5fed-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="f5fed-117">Näide: 50000</span><span class="sxs-lookup"><span data-stu-id="f5fed-117">Example: 50000</span></span>  
9. <span data-ttu-id="f5fed-118">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f5fed-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="f5fed-119">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="f5fed-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="f5fed-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f5fed-120">Close the page.</span></span>
2. <span data-ttu-id="f5fed-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f5fed-121">Close the page.</span></span>
3. <span data-ttu-id="f5fed-122">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="f5fed-122">Click Master planning.</span></span>
4. <span data-ttu-id="f5fed-123">Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f5fed-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f5fed-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f5fed-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f5fed-125">Näide: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="f5fed-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="f5fed-126">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="f5fed-126">Click Run.</span></span>
7. <span data-ttu-id="f5fed-127">Laiendage või ahendage jaotist Kaasatavad kirjed.</span><span class="sxs-lookup"><span data-stu-id="f5fed-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="f5fed-128">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="f5fed-128">Click Filter.</span></span>
9. <span data-ttu-id="f5fed-129">Valige loendist rida, mille väli = kaubakood.</span><span class="sxs-lookup"><span data-stu-id="f5fed-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="f5fed-130">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="f5fed-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="f5fed-131">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="f5fed-131">Example: P6003</span></span>  
11. <span data-ttu-id="f5fed-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f5fed-132">Click OK.</span></span>
12. <span data-ttu-id="f5fed-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f5fed-133">Click OK.</span></span>
13. <span data-ttu-id="f5fed-134">Klõpsake valikut Planeeritud tellimused.</span><span class="sxs-lookup"><span data-stu-id="f5fed-134">Click Planned orders.</span></span>
14. <span data-ttu-id="f5fed-135">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="f5fed-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f5fed-136">Näiteks saate filtrida välja Kaubakood väärtuse P6000 järgi.</span><span class="sxs-lookup"><span data-stu-id="f5fed-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="f5fed-137">Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="f5fed-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="f5fed-138">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="f5fed-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f5fed-139">Valige mis tahes filtri tagastatud read.</span><span class="sxs-lookup"><span data-stu-id="f5fed-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="f5fed-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f5fed-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="f5fed-141">Laiendage või ahendage jaotist Sidumine.</span><span class="sxs-lookup"><span data-stu-id="f5fed-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="f5fed-142">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f5fed-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f5fed-143">Plaanitud tellimus on seotud kaastoote müügitellimusega.</span><span class="sxs-lookup"><span data-stu-id="f5fed-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="f5fed-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f5fed-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="f5fed-145">Kaastoote nõude loomine</span><span class="sxs-lookup"><span data-stu-id="f5fed-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="f5fed-146">Avage Vaikearmatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="f5fed-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="f5fed-147">Klõpsake valikut Müügitellimuse töötlemine ja päring.</span><span class="sxs-lookup"><span data-stu-id="f5fed-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="f5fed-148">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="f5fed-148">Click New.</span></span>
4. <span data-ttu-id="f5fed-149">Klõpsake valikut Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="f5fed-149">Click Sales order.</span></span>
5. <span data-ttu-id="f5fed-150">Sisestage väärtus väljale Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="f5fed-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="f5fed-151">Näide: US-001.</span><span class="sxs-lookup"><span data-stu-id="f5fed-151">Example: US-001</span></span>  
6. <span data-ttu-id="f5fed-152">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f5fed-152">Click OK.</span></span>
7. <span data-ttu-id="f5fed-153">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="f5fed-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f5fed-154">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="f5fed-154">Example: P6003</span></span>  
8. <span data-ttu-id="f5fed-155">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="f5fed-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="f5fed-156">Näide: 50000</span><span class="sxs-lookup"><span data-stu-id="f5fed-156">Example: 50000</span></span>  
9. <span data-ttu-id="f5fed-157">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f5fed-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="f5fed-158">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="f5fed-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="f5fed-159">Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f5fed-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="f5fed-160">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f5fed-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f5fed-161">Näide: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="f5fed-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="f5fed-162">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="f5fed-162">Click Run.</span></span>
4. <span data-ttu-id="f5fed-163">Laiendage või ahendage jaotist Kaasatavad kirjed.</span><span class="sxs-lookup"><span data-stu-id="f5fed-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="f5fed-164">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="f5fed-164">Click Filter.</span></span>
6. <span data-ttu-id="f5fed-165">Valige loendist rida, mille väli = kaubakood.</span><span class="sxs-lookup"><span data-stu-id="f5fed-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="f5fed-166">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="f5fed-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="f5fed-167">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="f5fed-167">Example: P6003</span></span>  
8. <span data-ttu-id="f5fed-168">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f5fed-168">Click OK.</span></span>
9. <span data-ttu-id="f5fed-169">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f5fed-169">Click OK.</span></span>
10. <span data-ttu-id="f5fed-170">Klõpsake valikut Planeeritud tellimused.</span><span class="sxs-lookup"><span data-stu-id="f5fed-170">Click Planned orders.</span></span>
11. <span data-ttu-id="f5fed-171">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="f5fed-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f5fed-172">Näiteks saate filtrida välja Kaubakood väärtuse P6000 järgi.</span><span class="sxs-lookup"><span data-stu-id="f5fed-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="f5fed-173">Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="f5fed-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="f5fed-174">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="f5fed-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f5fed-175">Valige mis tahes filtri tagastatud read.</span><span class="sxs-lookup"><span data-stu-id="f5fed-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="f5fed-176">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f5fed-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="f5fed-177">Laiendage või ahendage jaotist Sidumine.</span><span class="sxs-lookup"><span data-stu-id="f5fed-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="f5fed-178">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f5fed-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f5fed-179">Plaanitud tellimus on seotud kaastoote müügitellimusega.</span><span class="sxs-lookup"><span data-stu-id="f5fed-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="f5fed-180">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f5fed-180">Close the page.</span></span>
17. <span data-ttu-id="f5fed-181">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="f5fed-181">Click Master planning.</span></span>
18. <span data-ttu-id="f5fed-182">Avage Koondplaneerimine > Seadistus > Koondplaneerimise parameetrid.</span><span class="sxs-lookup"><span data-stu-id="f5fed-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="f5fed-183">Valige väljal Keela kõik planeerimisprotsessid suvand Ei.</span><span class="sxs-lookup"><span data-stu-id="f5fed-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="f5fed-184">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f5fed-184">Close the page.</span></span>


