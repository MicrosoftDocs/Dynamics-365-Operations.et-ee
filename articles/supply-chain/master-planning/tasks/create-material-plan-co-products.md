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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2958f1e5c2e8a0cfa9cc6312f688d3b11b8e013c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "337137"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="b83ad-103">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="b83ad-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b83ad-104">Tootmise planeerija plaanib materjalinõudeid valemi kaastoodete kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="b83ad-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="b83ad-105">Selle protseduuri loomiseks kasutati demoettevõtte USP2 andmeid.</span><span class="sxs-lookup"><span data-stu-id="b83ad-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="b83ad-106">Kaastoote nõude loomine</span><span class="sxs-lookup"><span data-stu-id="b83ad-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="b83ad-107">Avage Vaikearmatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="b83ad-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="b83ad-108">Klõpsake valikut Müügitellimuse töötlemine ja päring.</span><span class="sxs-lookup"><span data-stu-id="b83ad-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="b83ad-109">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="b83ad-109">Click New.</span></span>
4. <span data-ttu-id="b83ad-110">Klõpsake valikut Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="b83ad-110">Click Sales order.</span></span>
5. <span data-ttu-id="b83ad-111">Sisestage väärtus väljale Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="b83ad-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="b83ad-112">Näide: US-001.</span><span class="sxs-lookup"><span data-stu-id="b83ad-112">Example: US-001</span></span>  
6. <span data-ttu-id="b83ad-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b83ad-113">Click OK.</span></span>
7. <span data-ttu-id="b83ad-114">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="b83ad-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b83ad-115">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="b83ad-115">Example: P6003</span></span>  
8. <span data-ttu-id="b83ad-116">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="b83ad-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b83ad-117">Näide: 50000</span><span class="sxs-lookup"><span data-stu-id="b83ad-117">Example: 50000</span></span>  
9. <span data-ttu-id="b83ad-118">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b83ad-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="b83ad-119">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="b83ad-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="b83ad-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b83ad-120">Close the page.</span></span>
2. <span data-ttu-id="b83ad-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b83ad-121">Close the page.</span></span>
3. <span data-ttu-id="b83ad-122">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="b83ad-122">Click Master planning.</span></span>
4. <span data-ttu-id="b83ad-123">Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b83ad-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b83ad-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b83ad-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b83ad-125">Näide: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="b83ad-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="b83ad-126">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="b83ad-126">Click Run.</span></span>
7. <span data-ttu-id="b83ad-127">Laiendage või ahendage jaotist Kaasatavad kirjed.</span><span class="sxs-lookup"><span data-stu-id="b83ad-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="b83ad-128">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="b83ad-128">Click Filter.</span></span>
9. <span data-ttu-id="b83ad-129">Valige loendist rida, mille väli = kaubakood.</span><span class="sxs-lookup"><span data-stu-id="b83ad-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="b83ad-130">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="b83ad-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="b83ad-131">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="b83ad-131">Example: P6003</span></span>  
11. <span data-ttu-id="b83ad-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b83ad-132">Click OK.</span></span>
12. <span data-ttu-id="b83ad-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b83ad-133">Click OK.</span></span>
13. <span data-ttu-id="b83ad-134">Klõpsake valikut Planeeritud tellimused.</span><span class="sxs-lookup"><span data-stu-id="b83ad-134">Click Planned orders.</span></span>
14. <span data-ttu-id="b83ad-135">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="b83ad-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b83ad-136">Näiteks saate filtrida välja Kaubakood väärtuse P6000 järgi.</span><span class="sxs-lookup"><span data-stu-id="b83ad-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="b83ad-137">Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="b83ad-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="b83ad-138">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b83ad-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b83ad-139">Valige mis tahes filtri tagastatud read.</span><span class="sxs-lookup"><span data-stu-id="b83ad-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="b83ad-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b83ad-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="b83ad-141">Laiendage või ahendage jaotist Sidumine.</span><span class="sxs-lookup"><span data-stu-id="b83ad-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="b83ad-142">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b83ad-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b83ad-143">Plaanitud tellimus on seotud kaastoote müügitellimusega.</span><span class="sxs-lookup"><span data-stu-id="b83ad-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="b83ad-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b83ad-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="b83ad-145">Kaastoote nõude loomine</span><span class="sxs-lookup"><span data-stu-id="b83ad-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="b83ad-146">Avage Vaikearmatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="b83ad-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="b83ad-147">Klõpsake valikut Müügitellimuse töötlemine ja päring.</span><span class="sxs-lookup"><span data-stu-id="b83ad-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="b83ad-148">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="b83ad-148">Click New.</span></span>
4. <span data-ttu-id="b83ad-149">Klõpsake valikut Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="b83ad-149">Click Sales order.</span></span>
5. <span data-ttu-id="b83ad-150">Sisestage väärtus väljale Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="b83ad-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="b83ad-151">Näide: US-001.</span><span class="sxs-lookup"><span data-stu-id="b83ad-151">Example: US-001</span></span>  
6. <span data-ttu-id="b83ad-152">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b83ad-152">Click OK.</span></span>
7. <span data-ttu-id="b83ad-153">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="b83ad-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b83ad-154">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="b83ad-154">Example: P6003</span></span>  
8. <span data-ttu-id="b83ad-155">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="b83ad-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b83ad-156">Näide: 50000</span><span class="sxs-lookup"><span data-stu-id="b83ad-156">Example: 50000</span></span>  
9. <span data-ttu-id="b83ad-157">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b83ad-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="b83ad-158">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="b83ad-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="b83ad-159">Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b83ad-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="b83ad-160">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b83ad-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b83ad-161">Näide: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="b83ad-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="b83ad-162">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="b83ad-162">Click Run.</span></span>
4. <span data-ttu-id="b83ad-163">Laiendage või ahendage jaotist Kaasatavad kirjed.</span><span class="sxs-lookup"><span data-stu-id="b83ad-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="b83ad-164">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="b83ad-164">Click Filter.</span></span>
6. <span data-ttu-id="b83ad-165">Valige loendist rida, mille väli = kaubakood.</span><span class="sxs-lookup"><span data-stu-id="b83ad-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="b83ad-166">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="b83ad-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="b83ad-167">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="b83ad-167">Example: P6003</span></span>  
8. <span data-ttu-id="b83ad-168">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b83ad-168">Click OK.</span></span>
9. <span data-ttu-id="b83ad-169">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b83ad-169">Click OK.</span></span>
10. <span data-ttu-id="b83ad-170">Klõpsake valikut Planeeritud tellimused.</span><span class="sxs-lookup"><span data-stu-id="b83ad-170">Click Planned orders.</span></span>
11. <span data-ttu-id="b83ad-171">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="b83ad-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b83ad-172">Näiteks saate filtrida välja Kaubakood väärtuse P6000 järgi.</span><span class="sxs-lookup"><span data-stu-id="b83ad-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="b83ad-173">Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="b83ad-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="b83ad-174">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b83ad-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b83ad-175">Valige mis tahes filtri tagastatud read.</span><span class="sxs-lookup"><span data-stu-id="b83ad-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="b83ad-176">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b83ad-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="b83ad-177">Laiendage või ahendage jaotist Sidumine.</span><span class="sxs-lookup"><span data-stu-id="b83ad-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="b83ad-178">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b83ad-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b83ad-179">Plaanitud tellimus on seotud kaastoote müügitellimusega.</span><span class="sxs-lookup"><span data-stu-id="b83ad-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="b83ad-180">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b83ad-180">Close the page.</span></span>
17. <span data-ttu-id="b83ad-181">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="b83ad-181">Click Master planning.</span></span>
18. <span data-ttu-id="b83ad-182">Avage Koondplaneerimine > Seadistus > Koondplaneerimise parameetrid.</span><span class="sxs-lookup"><span data-stu-id="b83ad-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="b83ad-183">Valige väljal Keela kõik planeerimisprotsessid suvand Ei.</span><span class="sxs-lookup"><span data-stu-id="b83ad-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="b83ad-184">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b83ad-184">Close the page.</span></span>

