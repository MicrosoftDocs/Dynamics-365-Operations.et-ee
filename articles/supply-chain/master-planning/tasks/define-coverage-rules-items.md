--- 
title: "Kaubakatte reeglite määratlemine"
description: "Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 14f56c30753da9458d66a46da8935305619fd0b8
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="a501f-103">Kaubakatte reeglite määratlemine</span><span class="sxs-lookup"><span data-stu-id="a501f-103">Define coverage rules for items</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a501f-104">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="a501f-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a501f-105">See protseduur näitab, kuidas luua laovarude reegleid ja tühistada kindla kaupa laovarude sätteid.</span><span class="sxs-lookup"><span data-stu-id="a501f-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="a501f-106">Samuti näitab see, kuidas määrata varude vaikesätteid.</span><span class="sxs-lookup"><span data-stu-id="a501f-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="a501f-107">Laovarude grupi loomine</span><span class="sxs-lookup"><span data-stu-id="a501f-107">Create a coverage group</span></span>
1. <span data-ttu-id="a501f-108">Avage Laovarude grupid.</span><span class="sxs-lookup"><span data-stu-id="a501f-108">Go to Coverage groups.</span></span>
2. <span data-ttu-id="a501f-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a501f-109">Click New.</span></span>
3. <span data-ttu-id="a501f-110">Sisestage väärtus väljale Laovarude grupp.</span><span class="sxs-lookup"><span data-stu-id="a501f-110">In the Coverage group field, type a value.</span></span>
4. <span data-ttu-id="a501f-111">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="a501f-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a501f-112">Sisestage väärtus väljale Kalender.</span><span class="sxs-lookup"><span data-stu-id="a501f-112">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="a501f-113">Valige kalender, mida kasutatakse koondplaneerimises gruppi kuuluvate kaupade täiendamissoovituste loomisel.</span><span class="sxs-lookup"><span data-stu-id="a501f-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="a501f-114">Valige suvand väljal Laovarude kood.</span><span class="sxs-lookup"><span data-stu-id="a501f-114">In the Coverage code field, select an option.</span></span>
    * <span data-ttu-id="a501f-115">Valige nõue selle protseduuri jaoks.</span><span class="sxs-lookup"><span data-stu-id="a501f-115">Select Requirement for this procedure.</span></span>  
7. <span data-ttu-id="a501f-116">Sisestage väärtus „90” väljale Laovarude ajapiir (päevades).</span><span class="sxs-lookup"><span data-stu-id="a501f-116">In the Coverage time fence (days) field, enter '90'.</span></span>
    * <span data-ttu-id="a501f-117">Sellesse gruppi kuuluvate kaupade jaoks loob koondplaneerimine täiendamise soovitused kuni 90 päeva ette.</span><span class="sxs-lookup"><span data-stu-id="a501f-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="a501f-118">Sisestage väärtus „1” väljale Negatiivsed päevad.</span><span class="sxs-lookup"><span data-stu-id="a501f-118">In the Negative days field, enter '1'.</span></span>
9. <span data-ttu-id="a501f-119">Sisestage väärtus „1” väljale Positiivsed päevad.</span><span class="sxs-lookup"><span data-stu-id="a501f-119">In the Positive days field, enter '1'.</span></span>
10. <span data-ttu-id="a501f-120">Laiendage või ahendage jaotist Muu.</span><span class="sxs-lookup"><span data-stu-id="a501f-120">Expand or collapse the Other section.</span></span>
11. <span data-ttu-id="a501f-121">Sisestage väärtus „1” väljale Vajaduse kuupäevale lisatud sissetuleku ohutusvaru.</span><span class="sxs-lookup"><span data-stu-id="a501f-121">In the Receipt margin added to requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="a501f-122">Näiteks kui sissetuleku ohutusvaru on seatud 1 päevale ja ostutellimuse rida on planeeritud sissetulekuks 15. mail, siis arvutatakse planeerimisel korrigeeritud sissetulekukuupäevaks 16. mai.</span><span class="sxs-lookup"><span data-stu-id="a501f-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="a501f-123">Sisestage väärtus „1” väljale Vajaduse kuupäevast maha arvatud väljamineku ohutusvaru.</span><span class="sxs-lookup"><span data-stu-id="a501f-123">In the Issue margin deducted from requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="a501f-124">Näiteks kui ohutusvaru on seatud 1 päevale ja müügitellimuse rida on planeeritud tarnimiseks 15. mail, siis arvutatakse koondplaneerimisel korrigeeritud tarnekuupäevaks 14. mai.</span><span class="sxs-lookup"><span data-stu-id="a501f-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="a501f-125">Sisestage väärtus „1” väljale Kauba täitmisajale lisatud lisatellimuse ohutusvaru.</span><span class="sxs-lookup"><span data-stu-id="a501f-125">In the Reorder margin added to item lead time field, enter '1'.</span></span>
14. <span data-ttu-id="a501f-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a501f-126">Click Save.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="a501f-127">Uue toote loomine</span><span class="sxs-lookup"><span data-stu-id="a501f-127">Create a new product</span></span>
1. <span data-ttu-id="a501f-128">Avage Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="a501f-128">Go to Released products.</span></span>
2. <span data-ttu-id="a501f-129">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a501f-129">Click New.</span></span>
3. <span data-ttu-id="a501f-130">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="a501f-130">In the Product number field, type a value.</span></span>
4. <span data-ttu-id="a501f-131">Sisestage väärtus väljale Toote nimi.</span><span class="sxs-lookup"><span data-stu-id="a501f-131">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="a501f-132">Klõpsake väljal Kauba mudeligrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a501f-132">In the Item model group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a501f-133">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a501f-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="a501f-134">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a501f-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="a501f-135">Klõpsake väljal Kaubagrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a501f-135">In the Item group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a501f-136">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a501f-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="a501f-137">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a501f-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="a501f-138">Klõpsake väljal Laoala dimensiooni grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a501f-138">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="a501f-139">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a501f-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="a501f-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a501f-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="a501f-141">Klõpsake väljal Jälgimisdimensiooni grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a501f-141">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="a501f-142">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a501f-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="a501f-143">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a501f-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="a501f-144">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a501f-144">Click OK.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="a501f-145">Vaike-tellimissätete seadistamine</span><span class="sxs-lookup"><span data-stu-id="a501f-145">Setup default order settings</span></span>
1. <span data-ttu-id="a501f-146">Klõpsake toimingupaanil valikut Plaan.</span><span class="sxs-lookup"><span data-stu-id="a501f-146">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="a501f-147">Klõpsake valikut Tellimuse vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="a501f-147">Click Default order settings.</span></span>
3. <span data-ttu-id="a501f-148">Sisestage ostutellimuste loomisel vaikekohana kasutatav koht väljal Ostukoht.</span><span class="sxs-lookup"><span data-stu-id="a501f-148">In the Purchase site field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="a501f-149">Sisestage väljale Varude tegevuskoht kaupa hoidmise asukoht.</span><span class="sxs-lookup"><span data-stu-id="a501f-149">In the Inventory site field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="a501f-150">Laiendage või ahendage jaotist Varud.</span><span class="sxs-lookup"><span data-stu-id="a501f-150">Expand or collapse the Inventory section.</span></span>
6. <span data-ttu-id="a501f-151">Määrake valiku Mitu väärtuseks „10”.</span><span class="sxs-lookup"><span data-stu-id="a501f-151">Set Multiple to '10'.</span></span>
7. <span data-ttu-id="a501f-152">Määrake Min</span><span class="sxs-lookup"><span data-stu-id="a501f-152">Set Min.</span></span> <span data-ttu-id="a501f-153">tellimuse koguseks 10.</span><span class="sxs-lookup"><span data-stu-id="a501f-153">order quantity to '10'.</span></span>
8. <span data-ttu-id="a501f-154">Määra maksimaalseks</span><span class="sxs-lookup"><span data-stu-id="a501f-154">Set Max.</span></span> <span data-ttu-id="a501f-155">tellimuse koguseks 100.</span><span class="sxs-lookup"><span data-stu-id="a501f-155">order quantity to '100'.</span></span>
9. <span data-ttu-id="a501f-156">Määrake välja Vaikekogus väärtuseks „10”.</span><span class="sxs-lookup"><span data-stu-id="a501f-156">Set Standard order quantity to '10'.</span></span>
10. <span data-ttu-id="a501f-157">Sisestage arv väljale Ostu täitmisaeg.</span><span class="sxs-lookup"><span data-stu-id="a501f-157">In the Purchase lead time field, enter a number.</span></span>
11. <span data-ttu-id="a501f-158">Valige või tühjendage märkeruut Tööpäevad.</span><span class="sxs-lookup"><span data-stu-id="a501f-158">Select or clear the Working days check box.</span></span>
12. <span data-ttu-id="a501f-159">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a501f-159">Click Save.</span></span>
13. <span data-ttu-id="a501f-160">Valige Ostutellimus väljal Vaikimisi tellimusetüüp.</span><span class="sxs-lookup"><span data-stu-id="a501f-160">In the Default order type field select 'Purchase order'.</span></span>
14. <span data-ttu-id="a501f-161">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a501f-161">Click Save.</span></span>
15. <span data-ttu-id="a501f-162">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a501f-162">Close the page.</span></span>
    * <span data-ttu-id="a501f-163">Sulgege leht Tellimuse vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="a501f-163">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="a501f-164">Kauba lisamine laovarude gruppi</span><span class="sxs-lookup"><span data-stu-id="a501f-164">Add an item to a coverage group</span></span>
1. <span data-ttu-id="a501f-165">Laiendage või ahendage jaotist Plaan.</span><span class="sxs-lookup"><span data-stu-id="a501f-165">Expand or collapse the Plan section.</span></span>
2. <span data-ttu-id="a501f-166">Klõpsake väljal Laovarude grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a501f-166">In the Coverage group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a501f-167">Leidke loendist loodud laovarude grupp.</span><span class="sxs-lookup"><span data-stu-id="a501f-167">In the list, find the Coverage group you have created.</span></span>
4. <span data-ttu-id="a501f-168">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a501f-168">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="a501f-169">Kauba laovarude reeglite loomine</span><span class="sxs-lookup"><span data-stu-id="a501f-169">Create item coverage rules</span></span>
1. <span data-ttu-id="a501f-170">Klõpsake toimingupaanil valikut Plaan.</span><span class="sxs-lookup"><span data-stu-id="a501f-170">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="a501f-171">Klõpsake valikut Kauba laovarud.</span><span class="sxs-lookup"><span data-stu-id="a501f-171">Click Item coverage.</span></span>
3. <span data-ttu-id="a501f-172">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a501f-172">Click New.</span></span>
4. <span data-ttu-id="a501f-173">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="a501f-173">Click the General tab.</span></span>
5. <span data-ttu-id="a501f-174">Märkige ruut suvandi Tühista laovarude grupi sätted päises.</span><span class="sxs-lookup"><span data-stu-id="a501f-174">Check the box on the header of Override coverage group settings.</span></span>
6. <span data-ttu-id="a501f-175">Sisestage väärtus „60” väljale Laovarude ajapiir (päevades).</span><span class="sxs-lookup"><span data-stu-id="a501f-175">In the Coverage time fence (days) field, enter '60'.</span></span>
    * <span data-ttu-id="a501f-176">Kuigi kaubad laovarude grupis Vajadus on plaanitud 90 päeva ette, plaanitakse see kaup 60 päeva ette.</span><span class="sxs-lookup"><span data-stu-id="a501f-176">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="a501f-177">Sisestage väärtus „2” väljale Negatiivsed päevad.</span><span class="sxs-lookup"><span data-stu-id="a501f-177">In the Negative days field, enter '2'.</span></span>
8. <span data-ttu-id="a501f-178">Sisestage väärtus „2” väljale Positiivsed päevad.</span><span class="sxs-lookup"><span data-stu-id="a501f-178">In the Positive days field, enter '2'.</span></span>
9. <span data-ttu-id="a501f-179">Klõpsake vahekaarti Täitmisaeg.</span><span class="sxs-lookup"><span data-stu-id="a501f-179">Click the Lead time tab.</span></span>
10. <span data-ttu-id="a501f-180">Märkige ruut suvandi Ost päises.</span><span class="sxs-lookup"><span data-stu-id="a501f-180">Check the box on the header of Purchase.</span></span>
11. <span data-ttu-id="a501f-181">Sisestage väärtus „5” väljale Ostuaeg.</span><span class="sxs-lookup"><span data-stu-id="a501f-181">In the Purchase time field, enter '5'.</span></span>
12. <span data-ttu-id="a501f-182">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a501f-182">Click Save.</span></span>


