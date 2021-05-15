---
title: Kaastoodete jaoks materjaliplaani loomine
description: Tootmise planeerija plaanib materjalinõudeid valemi kaastoodete kaupade puhul.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920725"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="7cade-103">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="7cade-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7cade-104">Tootmise planeerija plaanib materjalinõudeid valemi kaastoodete kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="7cade-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="7cade-105">Selle protseduuri loomiseks kasutati demoettevõtte USP2 andmeid.</span><span class="sxs-lookup"><span data-stu-id="7cade-105">The demo data company used to create this procedure is USP2.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="7cade-106">Kaastoote nõude loomine</span><span class="sxs-lookup"><span data-stu-id="7cade-106">Create requirement for a co-product</span></span>

1. <span data-ttu-id="7cade-107">Minge **müügi ja turunduse \> tööruumides \> müügitellimuse töötlemisele ja päringule**.</span><span class="sxs-lookup"><span data-stu-id="7cade-107">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="7cade-108">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7cade-108">Select **New**.</span></span>
1. <span data-ttu-id="7cade-109">Valige **Müügitellimus**.</span><span class="sxs-lookup"><span data-stu-id="7cade-109">Select **Sales order**.</span></span>
1. <span data-ttu-id="7cade-110">Sisestage väärtus väljale **Kliendi konto**.</span><span class="sxs-lookup"><span data-stu-id="7cade-110">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="7cade-111">Näide: US-001.</span><span class="sxs-lookup"><span data-stu-id="7cade-111">Example: US-001</span></span>  
1. <span data-ttu-id="7cade-112">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cade-112">Select **OK**.</span></span>
1. <span data-ttu-id="7cade-113">Sisestage väärtus väljale **Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="7cade-113">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="7cade-114">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="7cade-114">Example: P6003</span></span>  
1. <span data-ttu-id="7cade-115">Sisestage arv väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="7cade-115">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="7cade-116">Näide: 50000</span><span class="sxs-lookup"><span data-stu-id="7cade-116">Example: 50000</span></span>  
1. <span data-ttu-id="7cade-117">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7cade-117">Select **Save**.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="7cade-118">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="7cade-118">Create a material plan for co-products</span></span>

1. <span data-ttu-id="7cade-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="7cade-119">Close the page.</span></span>
1. <span data-ttu-id="7cade-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="7cade-120">Close the page.</span></span>
1. <span data-ttu-id="7cade-121">Valige **Koondplaneerimine**.</span><span class="sxs-lookup"><span data-stu-id="7cade-121">Select **Master planning**.</span></span>
1. <span data-ttu-id="7cade-122">Väljal **Plaan** valige ripploendi nuppu, et avada otsing.</span><span class="sxs-lookup"><span data-stu-id="7cade-122">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
1. <span data-ttu-id="7cade-123">Valige loendis link valitud reas.</span><span class="sxs-lookup"><span data-stu-id="7cade-123">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="7cade-124">Näide: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="7cade-124">Example: MasterPlan</span></span>  
1. <span data-ttu-id="7cade-125">Valige käsk **Käitus**.</span><span class="sxs-lookup"><span data-stu-id="7cade-125">Select **Run**.</span></span>
1. <span data-ttu-id="7cade-126">Laiendage või ahendage jaotist **Kaasatavad kirjed**.</span><span class="sxs-lookup"><span data-stu-id="7cade-126">Expand or collapse the **Records to include** section.</span></span>
1. <span data-ttu-id="7cade-127">Valige **Filter**.</span><span class="sxs-lookup"><span data-stu-id="7cade-127">Select **Filter**.</span></span>
1. <span data-ttu-id="7cade-128">Valige loendist rida **Välja** = *üksuse numbri* kohta.</span><span class="sxs-lookup"><span data-stu-id="7cade-128">In the list, select the row for **Field** = *Item number*.</span></span>
1. <span data-ttu-id="7cade-129">Sisestage väärtus väljale **Kriteerium**.</span><span class="sxs-lookup"><span data-stu-id="7cade-129">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="7cade-130">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="7cade-130">Example: P6003</span></span>  
1. <span data-ttu-id="7cade-131">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cade-131">Select **OK**.</span></span>
1. <span data-ttu-id="7cade-132">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cade-132">Select **OK**.</span></span>
1. <span data-ttu-id="7cade-133">Valige **Plaanitud tellimused**.</span><span class="sxs-lookup"><span data-stu-id="7cade-133">Select **Planned orders**.</span></span>
1. <span data-ttu-id="7cade-134">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="7cade-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="7cade-135">Näiteks saate filtrida välja **Kaubakood** väärtuse P6000 järgi.</span><span class="sxs-lookup"><span data-stu-id="7cade-135">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="7cade-136">Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="7cade-136">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
1. <span data-ttu-id="7cade-137">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="7cade-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7cade-138">Valige mis tahes filtri tagastatud read.</span><span class="sxs-lookup"><span data-stu-id="7cade-138">Select any of the rows returned by the filter.</span></span>  
1. <span data-ttu-id="7cade-139">Valige loendis link valitud reas.</span><span class="sxs-lookup"><span data-stu-id="7cade-139">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="7cade-140">Laiendage jaotist **Sidumine**.</span><span class="sxs-lookup"><span data-stu-id="7cade-140">Expand the **Pegging** section.</span></span>
1. <span data-ttu-id="7cade-141">Valige loendis link valitud reas.</span><span class="sxs-lookup"><span data-stu-id="7cade-141">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="7cade-142">Plaanitud tellimus on seotud kaastoote müügitellimusega.</span><span class="sxs-lookup"><span data-stu-id="7cade-142">The planned order is pegged to the sales order for the co-product.</span></span>  
1. <span data-ttu-id="7cade-143">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="7cade-143">Close the page.</span></span>

## <a name="create-a-second-requirement-for-a-co-product"></a><span data-ttu-id="7cade-144">Teise kaastoote nõude loomine</span><span class="sxs-lookup"><span data-stu-id="7cade-144">Create a second requirement for a co-product</span></span>

1. <span data-ttu-id="7cade-145">Minge **müügi ja turunduse \> tööruumides \> müügitellimuse töötlemisele ja päringule**.</span><span class="sxs-lookup"><span data-stu-id="7cade-145">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="7cade-146">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7cade-146">Select **New**.</span></span>
1. <span data-ttu-id="7cade-147">Valige **Müügitellimus**.</span><span class="sxs-lookup"><span data-stu-id="7cade-147">Select **Sales order**.</span></span>
1. <span data-ttu-id="7cade-148">Sisestage väärtus väljale **Kliendi konto**.</span><span class="sxs-lookup"><span data-stu-id="7cade-148">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="7cade-149">Näide: US-001.</span><span class="sxs-lookup"><span data-stu-id="7cade-149">Example: US-001</span></span>  
1. <span data-ttu-id="7cade-150">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cade-150">Select **OK**.</span></span>
1. <span data-ttu-id="7cade-151">Sisestage väärtus väljale **Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="7cade-151">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="7cade-152">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="7cade-152">Example: P6003</span></span>  
1. <span data-ttu-id="7cade-153">Sisestage arv väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="7cade-153">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="7cade-154">Näide: 50000</span><span class="sxs-lookup"><span data-stu-id="7cade-154">Example: 50000</span></span>  
1. <span data-ttu-id="7cade-155">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7cade-155">Select **Save**.</span></span>

## <a name="create-a-second-material-plan-for-co-products"></a><span data-ttu-id="7cade-156">Kaastoodete jaoks teise materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="7cade-156">Create a second material plan for co-products</span></span>

1. <span data-ttu-id="7cade-157">Väljal **Plaan** valige ripploendi nuppu, et avada otsing.</span><span class="sxs-lookup"><span data-stu-id="7cade-157">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="7cade-158">Valige loendis link valitud reas.</span><span class="sxs-lookup"><span data-stu-id="7cade-158">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="7cade-159">Näide: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="7cade-159">Example: MasterPlan</span></span>  
3. <span data-ttu-id="7cade-160">Valige käsk **Käitus**.</span><span class="sxs-lookup"><span data-stu-id="7cade-160">Select **Run**.</span></span>
4. <span data-ttu-id="7cade-161">Laiendage või ahendage jaotist **Kaasatavad kirjed**.</span><span class="sxs-lookup"><span data-stu-id="7cade-161">Expand or collapse the **Records to include** section.</span></span>
5. <span data-ttu-id="7cade-162">Valige **Filter**.</span><span class="sxs-lookup"><span data-stu-id="7cade-162">Select **Filter**.</span></span>
6. <span data-ttu-id="7cade-163">Valige loendist rida **Välja** = *üksuse numbri* kohta.</span><span class="sxs-lookup"><span data-stu-id="7cade-163">In the list, select the row for **Field** = *Item number*.</span></span>
7. <span data-ttu-id="7cade-164">Sisestage väärtus väljale *Kriteerium*.</span><span class="sxs-lookup"><span data-stu-id="7cade-164">In the *Criteria* field, type a value.</span></span>
    * <span data-ttu-id="7cade-165">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="7cade-165">Example: P6003</span></span>  
8. <span data-ttu-id="7cade-166">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cade-166">Select **OK**.</span></span>
9. <span data-ttu-id="7cade-167">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="7cade-167">Select **OK**.</span></span>
10. <span data-ttu-id="7cade-168">Valige **Plaanitud tellimused**.</span><span class="sxs-lookup"><span data-stu-id="7cade-168">Select **Planned orders**.</span></span>
11. <span data-ttu-id="7cade-169">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="7cade-169">Use the Quick Filter to find records.</span></span> <span data-ttu-id="7cade-170">Näiteks saate filtrida välja **Kaubakood** väärtuse P6000 järgi.</span><span class="sxs-lookup"><span data-stu-id="7cade-170">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="7cade-171">Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="7cade-171">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="7cade-172">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="7cade-172">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7cade-173">Valige mis tahes filtri tagastatud read.</span><span class="sxs-lookup"><span data-stu-id="7cade-173">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="7cade-174">Valige loendis link valitud reas.</span><span class="sxs-lookup"><span data-stu-id="7cade-174">In the list, select the link in the selected row.</span></span>
14. <span data-ttu-id="7cade-175">Laiendage või ahendage jaotist **Sidumine**.</span><span class="sxs-lookup"><span data-stu-id="7cade-175">Expand or collapse the **Pegging** section.</span></span>
15. <span data-ttu-id="7cade-176">Valige loendis link valitud reas.</span><span class="sxs-lookup"><span data-stu-id="7cade-176">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="7cade-177">Plaanitud tellimus on seotud kaastoote müügitellimusega.</span><span class="sxs-lookup"><span data-stu-id="7cade-177">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="7cade-178">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="7cade-178">Close the page.</span></span>
17. <span data-ttu-id="7cade-179">Valige **Koondplaneerimine**.</span><span class="sxs-lookup"><span data-stu-id="7cade-179">Select **Master planning**.</span></span>
18. <span data-ttu-id="7cade-180">Avage **Koondplaneerimine \> Seadistus \> Koondplaneerimise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="7cade-180">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
19. <span data-ttu-id="7cade-181">Valige väljal *Keela kõik planeerimisprotsessid* suvand **Ei**.</span><span class="sxs-lookup"><span data-stu-id="7cade-181">Select *No* in the **Disable all planning processes** field.</span></span>
20. <span data-ttu-id="7cade-182">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="7cade-182">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]