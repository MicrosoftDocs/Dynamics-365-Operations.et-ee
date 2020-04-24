---
title: Kaastoodete jaoks materjaliplaani loomine
description: Tootmise planeerija plaanib materjalinõudeid valemi kaastoodete kaupade puhul.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5915dca3af0650883ef5c90dbc50332af5be6cbd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209670"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="a61d7-103">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="a61d7-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a61d7-104">Tootmise planeerija plaanib materjalinõudeid valemi kaastoodete kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="a61d7-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="a61d7-105">Selle protseduuri loomiseks kasutati demoettevõtte USP2 andmeid.</span><span class="sxs-lookup"><span data-stu-id="a61d7-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="a61d7-106">Kaastoote nõude loomine</span><span class="sxs-lookup"><span data-stu-id="a61d7-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="a61d7-107">Avage Vaikearmatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="a61d7-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="a61d7-108">Klõpsake valikut Müügitellimuse töötlemine ja päring.</span><span class="sxs-lookup"><span data-stu-id="a61d7-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="a61d7-109">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="a61d7-109">Click New.</span></span>
4. <span data-ttu-id="a61d7-110">Klõpsake valikut Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="a61d7-110">Click Sales order.</span></span>
5. <span data-ttu-id="a61d7-111">Sisestage väärtus väljale Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="a61d7-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="a61d7-112">Näide: US-001.</span><span class="sxs-lookup"><span data-stu-id="a61d7-112">Example: US-001</span></span>  
6. <span data-ttu-id="a61d7-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a61d7-113">Click OK.</span></span>
7. <span data-ttu-id="a61d7-114">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="a61d7-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a61d7-115">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="a61d7-115">Example: P6003</span></span>  
8. <span data-ttu-id="a61d7-116">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="a61d7-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="a61d7-117">Näide: 50000</span><span class="sxs-lookup"><span data-stu-id="a61d7-117">Example: 50000</span></span>  
9. <span data-ttu-id="a61d7-118">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a61d7-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="a61d7-119">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="a61d7-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="a61d7-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a61d7-120">Close the page.</span></span>
2. <span data-ttu-id="a61d7-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a61d7-121">Close the page.</span></span>
3. <span data-ttu-id="a61d7-122">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="a61d7-122">Click Master planning.</span></span>
4. <span data-ttu-id="a61d7-123">Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a61d7-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a61d7-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a61d7-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a61d7-125">Näide: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="a61d7-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="a61d7-126">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="a61d7-126">Click Run.</span></span>
7. <span data-ttu-id="a61d7-127">Laiendage või ahendage jaotist Kaasatavad kirjed.</span><span class="sxs-lookup"><span data-stu-id="a61d7-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="a61d7-128">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="a61d7-128">Click Filter.</span></span>
9. <span data-ttu-id="a61d7-129">Valige loendist rida, mille väli = kaubakood.</span><span class="sxs-lookup"><span data-stu-id="a61d7-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="a61d7-130">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="a61d7-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="a61d7-131">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="a61d7-131">Example: P6003</span></span>  
11. <span data-ttu-id="a61d7-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a61d7-132">Click OK.</span></span>
12. <span data-ttu-id="a61d7-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a61d7-133">Click OK.</span></span>
13. <span data-ttu-id="a61d7-134">Klõpsake valikut Planeeritud tellimused.</span><span class="sxs-lookup"><span data-stu-id="a61d7-134">Click Planned orders.</span></span>
14. <span data-ttu-id="a61d7-135">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="a61d7-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a61d7-136">Näiteks saate filtrida välja Kaubakood väärtuse P6000 järgi.</span><span class="sxs-lookup"><span data-stu-id="a61d7-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="a61d7-137">Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="a61d7-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="a61d7-138">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="a61d7-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a61d7-139">Valige mis tahes filtri tagastatud read.</span><span class="sxs-lookup"><span data-stu-id="a61d7-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="a61d7-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a61d7-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="a61d7-141">Laiendage või ahendage jaotist Sidumine.</span><span class="sxs-lookup"><span data-stu-id="a61d7-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="a61d7-142">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a61d7-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a61d7-143">Plaanitud tellimus on seotud kaastoote müügitellimusega.</span><span class="sxs-lookup"><span data-stu-id="a61d7-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="a61d7-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a61d7-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="a61d7-145">Kaastoote nõude loomine</span><span class="sxs-lookup"><span data-stu-id="a61d7-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="a61d7-146">Avage Vaikearmatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="a61d7-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="a61d7-147">Klõpsake valikut Müügitellimuse töötlemine ja päring.</span><span class="sxs-lookup"><span data-stu-id="a61d7-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="a61d7-148">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="a61d7-148">Click New.</span></span>
4. <span data-ttu-id="a61d7-149">Klõpsake valikut Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="a61d7-149">Click Sales order.</span></span>
5. <span data-ttu-id="a61d7-150">Sisestage väärtus väljale Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="a61d7-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="a61d7-151">Näide: US-001.</span><span class="sxs-lookup"><span data-stu-id="a61d7-151">Example: US-001</span></span>  
6. <span data-ttu-id="a61d7-152">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a61d7-152">Click OK.</span></span>
7. <span data-ttu-id="a61d7-153">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="a61d7-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a61d7-154">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="a61d7-154">Example: P6003</span></span>  
8. <span data-ttu-id="a61d7-155">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="a61d7-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="a61d7-156">Näide: 50000</span><span class="sxs-lookup"><span data-stu-id="a61d7-156">Example: 50000</span></span>  
9. <span data-ttu-id="a61d7-157">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a61d7-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="a61d7-158">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="a61d7-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="a61d7-159">Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a61d7-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="a61d7-160">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a61d7-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a61d7-161">Näide: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="a61d7-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="a61d7-162">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="a61d7-162">Click Run.</span></span>
4. <span data-ttu-id="a61d7-163">Laiendage või ahendage jaotist Kaasatavad kirjed.</span><span class="sxs-lookup"><span data-stu-id="a61d7-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="a61d7-164">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="a61d7-164">Click Filter.</span></span>
6. <span data-ttu-id="a61d7-165">Valige loendist rida, mille väli = kaubakood.</span><span class="sxs-lookup"><span data-stu-id="a61d7-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="a61d7-166">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="a61d7-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="a61d7-167">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="a61d7-167">Example: P6003</span></span>  
8. <span data-ttu-id="a61d7-168">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a61d7-168">Click OK.</span></span>
9. <span data-ttu-id="a61d7-169">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a61d7-169">Click OK.</span></span>
10. <span data-ttu-id="a61d7-170">Klõpsake valikut Planeeritud tellimused.</span><span class="sxs-lookup"><span data-stu-id="a61d7-170">Click Planned orders.</span></span>
11. <span data-ttu-id="a61d7-171">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="a61d7-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a61d7-172">Näiteks saate filtrida välja Kaubakood väärtuse P6000 järgi.</span><span class="sxs-lookup"><span data-stu-id="a61d7-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="a61d7-173">Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="a61d7-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="a61d7-174">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="a61d7-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a61d7-175">Valige mis tahes filtri tagastatud read.</span><span class="sxs-lookup"><span data-stu-id="a61d7-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="a61d7-176">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a61d7-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="a61d7-177">Laiendage või ahendage jaotist Sidumine.</span><span class="sxs-lookup"><span data-stu-id="a61d7-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="a61d7-178">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a61d7-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a61d7-179">Plaanitud tellimus on seotud kaastoote müügitellimusega.</span><span class="sxs-lookup"><span data-stu-id="a61d7-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="a61d7-180">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a61d7-180">Close the page.</span></span>
17. <span data-ttu-id="a61d7-181">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="a61d7-181">Click Master planning.</span></span>
18. <span data-ttu-id="a61d7-182">Avage Koondplaneerimine > Seadistus > Koondplaneerimise parameetrid.</span><span class="sxs-lookup"><span data-stu-id="a61d7-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="a61d7-183">Valige väljal Keela kõik planeerimisprotsessid suvand Ei.</span><span class="sxs-lookup"><span data-stu-id="a61d7-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="a61d7-184">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a61d7-184">Close the page.</span></span>

