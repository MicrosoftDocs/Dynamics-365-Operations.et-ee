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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a87935f8f30d909f1a6a62ed7be00c83476a36a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214366"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="f8778-103">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="f8778-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f8778-104">Tootmise planeerija plaanib materjalinõudeid valemi kaastoodete kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="f8778-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="f8778-105">Selle protseduuri loomiseks kasutati demoettevõtte USP2 andmeid.</span><span class="sxs-lookup"><span data-stu-id="f8778-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="f8778-106">Kaastoote nõude loomine</span><span class="sxs-lookup"><span data-stu-id="f8778-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="f8778-107">Avage Vaikearmatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="f8778-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="f8778-108">Klõpsake valikut Müügitellimuse töötlemine ja päring.</span><span class="sxs-lookup"><span data-stu-id="f8778-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="f8778-109">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="f8778-109">Click New.</span></span>
4. <span data-ttu-id="f8778-110">Klõpsake valikut Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="f8778-110">Click Sales order.</span></span>
5. <span data-ttu-id="f8778-111">Sisestage väärtus väljale Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="f8778-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="f8778-112">Näide: US-001.</span><span class="sxs-lookup"><span data-stu-id="f8778-112">Example: US-001</span></span>  
6. <span data-ttu-id="f8778-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f8778-113">Click OK.</span></span>
7. <span data-ttu-id="f8778-114">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="f8778-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f8778-115">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="f8778-115">Example: P6003</span></span>  
8. <span data-ttu-id="f8778-116">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="f8778-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="f8778-117">Näide: 50000</span><span class="sxs-lookup"><span data-stu-id="f8778-117">Example: 50000</span></span>  
9. <span data-ttu-id="f8778-118">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f8778-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="f8778-119">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="f8778-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="f8778-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f8778-120">Close the page.</span></span>
2. <span data-ttu-id="f8778-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f8778-121">Close the page.</span></span>
3. <span data-ttu-id="f8778-122">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="f8778-122">Click Master planning.</span></span>
4. <span data-ttu-id="f8778-123">Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f8778-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f8778-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f8778-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f8778-125">Näide: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="f8778-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="f8778-126">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="f8778-126">Click Run.</span></span>
7. <span data-ttu-id="f8778-127">Laiendage või ahendage jaotist Kaasatavad kirjed.</span><span class="sxs-lookup"><span data-stu-id="f8778-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="f8778-128">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="f8778-128">Click Filter.</span></span>
9. <span data-ttu-id="f8778-129">Valige loendist rida, mille väli = kaubakood.</span><span class="sxs-lookup"><span data-stu-id="f8778-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="f8778-130">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="f8778-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="f8778-131">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="f8778-131">Example: P6003</span></span>  
11. <span data-ttu-id="f8778-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f8778-132">Click OK.</span></span>
12. <span data-ttu-id="f8778-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f8778-133">Click OK.</span></span>
13. <span data-ttu-id="f8778-134">Klõpsake valikut Planeeritud tellimused.</span><span class="sxs-lookup"><span data-stu-id="f8778-134">Click Planned orders.</span></span>
14. <span data-ttu-id="f8778-135">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="f8778-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f8778-136">Näiteks saate filtrida välja Kaubakood väärtuse P6000 järgi.</span><span class="sxs-lookup"><span data-stu-id="f8778-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="f8778-137">Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="f8778-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="f8778-138">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="f8778-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f8778-139">Valige mis tahes filtri tagastatud read.</span><span class="sxs-lookup"><span data-stu-id="f8778-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="f8778-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f8778-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="f8778-141">Laiendage või ahendage jaotist Sidumine.</span><span class="sxs-lookup"><span data-stu-id="f8778-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="f8778-142">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f8778-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f8778-143">Plaanitud tellimus on seotud kaastoote müügitellimusega.</span><span class="sxs-lookup"><span data-stu-id="f8778-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="f8778-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f8778-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="f8778-145">Kaastoote nõude loomine</span><span class="sxs-lookup"><span data-stu-id="f8778-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="f8778-146">Avage Vaikearmatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="f8778-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="f8778-147">Klõpsake valikut Müügitellimuse töötlemine ja päring.</span><span class="sxs-lookup"><span data-stu-id="f8778-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="f8778-148">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="f8778-148">Click New.</span></span>
4. <span data-ttu-id="f8778-149">Klõpsake valikut Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="f8778-149">Click Sales order.</span></span>
5. <span data-ttu-id="f8778-150">Sisestage väärtus väljale Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="f8778-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="f8778-151">Näide: US-001.</span><span class="sxs-lookup"><span data-stu-id="f8778-151">Example: US-001</span></span>  
6. <span data-ttu-id="f8778-152">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f8778-152">Click OK.</span></span>
7. <span data-ttu-id="f8778-153">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="f8778-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="f8778-154">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="f8778-154">Example: P6003</span></span>  
8. <span data-ttu-id="f8778-155">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="f8778-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="f8778-156">Näide: 50000</span><span class="sxs-lookup"><span data-stu-id="f8778-156">Example: 50000</span></span>  
9. <span data-ttu-id="f8778-157">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f8778-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="f8778-158">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="f8778-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="f8778-159">Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f8778-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="f8778-160">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f8778-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f8778-161">Näide: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="f8778-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="f8778-162">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="f8778-162">Click Run.</span></span>
4. <span data-ttu-id="f8778-163">Laiendage või ahendage jaotist Kaasatavad kirjed.</span><span class="sxs-lookup"><span data-stu-id="f8778-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="f8778-164">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="f8778-164">Click Filter.</span></span>
6. <span data-ttu-id="f8778-165">Valige loendist rida, mille väli = kaubakood.</span><span class="sxs-lookup"><span data-stu-id="f8778-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="f8778-166">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="f8778-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="f8778-167">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="f8778-167">Example: P6003</span></span>  
8. <span data-ttu-id="f8778-168">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f8778-168">Click OK.</span></span>
9. <span data-ttu-id="f8778-169">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f8778-169">Click OK.</span></span>
10. <span data-ttu-id="f8778-170">Klõpsake valikut Planeeritud tellimused.</span><span class="sxs-lookup"><span data-stu-id="f8778-170">Click Planned orders.</span></span>
11. <span data-ttu-id="f8778-171">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="f8778-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f8778-172">Näiteks saate filtrida välja Kaubakood väärtuse P6000 järgi.</span><span class="sxs-lookup"><span data-stu-id="f8778-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="f8778-173">Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="f8778-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="f8778-174">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="f8778-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f8778-175">Valige mis tahes filtri tagastatud read.</span><span class="sxs-lookup"><span data-stu-id="f8778-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="f8778-176">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f8778-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="f8778-177">Laiendage või ahendage jaotist Sidumine.</span><span class="sxs-lookup"><span data-stu-id="f8778-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="f8778-178">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f8778-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f8778-179">Plaanitud tellimus on seotud kaastoote müügitellimusega.</span><span class="sxs-lookup"><span data-stu-id="f8778-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="f8778-180">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f8778-180">Close the page.</span></span>
17. <span data-ttu-id="f8778-181">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="f8778-181">Click Master planning.</span></span>
18. <span data-ttu-id="f8778-182">Avage Koondplaneerimine > Seadistus > Koondplaneerimise parameetrid.</span><span class="sxs-lookup"><span data-stu-id="f8778-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="f8778-183">Valige väljal Keela kõik planeerimisprotsessid suvand Ei.</span><span class="sxs-lookup"><span data-stu-id="f8778-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="f8778-184">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f8778-184">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]