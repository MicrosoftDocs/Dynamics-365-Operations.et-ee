---
title: Kaubakatte reeglite määratlemine
description: Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd44c458da03807ddc1dc9d652da29c1404dbe64
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209601"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="a8e9a-103">Kaubakatte reeglite määratlemine</span><span class="sxs-lookup"><span data-stu-id="a8e9a-103">Define coverage rules for items</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8e9a-104">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a8e9a-105">See protseduur näitab, kuidas luua laovarude reegleid ja tühistada kindla kaupa laovarude sätteid.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="a8e9a-106">Samuti näitab see, kuidas määrata varude vaikesätteid.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="a8e9a-107">Laovarude grupi loomine</span><span class="sxs-lookup"><span data-stu-id="a8e9a-107">Create a coverage group</span></span>
1. <span data-ttu-id="a8e9a-108">Avage **Navigeerimispaan > Moodulid > Koondplaneerimine > Häälestus > Laovarude grupid**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-108">Go to **Navigation pane > Modules > Master planning > Setup > Coverage groups**.</span></span>
2. <span data-ttu-id="a8e9a-109">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-109">Click **New**.</span></span>
3. <span data-ttu-id="a8e9a-110">Sisestage väärtus väljale **Laovarude grupp**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-110">In the **Coverage group** field, type a value.</span></span>
4. <span data-ttu-id="a8e9a-111">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="a8e9a-112">Sisestage väärtus väljale **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-112">In the **Calendar** field, type a value.</span></span> <span data-ttu-id="a8e9a-113">Valige kalender, mida kasutatakse koondplaneerimises gruppi kuuluvate kaupade täiendamissoovituste loomisel.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="a8e9a-114">Valige suvand väljal **Laovarude kood**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-114">In the **Coverage code** field, select an option.</span></span> <span data-ttu-id="a8e9a-115">Valige nõue selle protseduuri jaoks.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-115">Select 'Requirement' for this procedure.</span></span>  
7. <span data-ttu-id="a8e9a-116">Sisestage väärtus „90” **väljale Laovarude ajapiir (päevades)**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-116">In the **Coverage time fence (days) field**, enter '90'.</span></span> <span data-ttu-id="a8e9a-117">Sellesse gruppi kuuluvate kaupade jaoks loob koondplaneerimine täiendamise soovitused kuni 90 päeva ette.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="a8e9a-118">Sisestage väärtus „1” väljale **Negatiivsed päevad**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-118">In the **Negative days** field, enter '1'.</span></span>
9. <span data-ttu-id="a8e9a-119">Sisestage väärtus „1” väljale **Positiivsed päevad**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-119">In the **Positive days** field, enter '1'.</span></span>
10. <span data-ttu-id="a8e9a-120">Laiendage või ahendage jaotist **Muu**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-120">Expand or collapse the **Other** section.</span></span>
11. <span data-ttu-id="a8e9a-121">Sisestage jaotises **Ohutuspiirid päevades** väljale **Vajaduse kuupäeva sissetuleku ohutusvaru** sisestage 1.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-121">Under the **Safety margins in days** section, in the **Receipt margin added to requirement date** field, enter '1'.</span></span> <span data-ttu-id="a8e9a-122">Näiteks kui sissetuleku ohutusvaru on seatud 1 päevale ja ostutellimuse rida on planeeritud sissetulekuks 15. mail, siis arvutatakse planeerimisel korrigeeritud sissetulekukuupäevaks 16. mai.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="a8e9a-123">Sisestage väärtus „1” väljale **Vajaduse kuupäevast maha arvatud väljamineku ohutusvaru**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-123">In the **Issue margin deducted from requirement date** field, enter '1'.</span></span> <span data-ttu-id="a8e9a-124">Näiteks kui ohutusvaru on seatud 1 päevale ja müügitellimuse rida on planeeritud tarnimiseks 15. mail, siis arvutatakse koondplaneerimisel korrigeeritud tarnekuupäevaks 14. mai.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="a8e9a-125">Sisestage väärtus „1” väljale **Kauba täitmisajale lisatud lisatellimuse ohutusvaru**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-125">In the **Reorder margin added to item lead time** field, enter '1'.</span></span>
14. <span data-ttu-id="a8e9a-126">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-126">Click **Save**.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="a8e9a-127">Uue toote loomine</span><span class="sxs-lookup"><span data-stu-id="a8e9a-127">Create a new product</span></span>
1. <span data-ttu-id="a8e9a-128">Avage **Navigeerimispaan > Moodulid > Tooteteabe haldus > Tooted > Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-128">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="a8e9a-129">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-129">Click **New**.</span></span>
3. <span data-ttu-id="a8e9a-130">Sisestage väärtus väljale **Toote number**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-130">In the **Product number** field, type a value.</span></span>
4. <span data-ttu-id="a8e9a-131">Sisestage väärtus väljale **Toote nimi**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-131">In the **Product name** field, type a value.</span></span>
5. <span data-ttu-id="a8e9a-132">Klõpsake väljal **Kauba mudeligrupp** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-132">In the **Item model group** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a8e9a-133">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="a8e9a-134">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="a8e9a-135">Klõpsake väljal **Kaubagrupp** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-135">In the **Item group** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a8e9a-136">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="a8e9a-137">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="a8e9a-138">Klõpsake väljal **Laoala dimensiooni grupp** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-138">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="a8e9a-139">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="a8e9a-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="a8e9a-141">Klõpsake väljal **Jälgimisdimensiooni grupp** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-141">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="a8e9a-142">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="a8e9a-143">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="a8e9a-144">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-144">Click **OK**.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="a8e9a-145">Vaike-tellimissätete seadistamine</span><span class="sxs-lookup"><span data-stu-id="a8e9a-145">Setup default order settings</span></span>
1. <span data-ttu-id="a8e9a-146">Klõpsake **Toimingupaanil** valikut **Plaan**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-146">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="a8e9a-147">Suvandil **Tellimuse sätted** klõpsake **Tellimuse vaikesätted**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-147">Under **Order settings**, click **Default order settings**.</span></span>
3. <span data-ttu-id="a8e9a-148">Sisestage **Ostutellimuste** loomisel vaikekohana kasutatav koht väljal **Ostukoht**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-148">Under **Purchase order**, in the **Default site** field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="a8e9a-149">Sisestage väljale **Varude tegevuskoht** kaupa hoidmise asukoht.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-149">In the **Default warehouse** field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="a8e9a-150">Laiendage või ahendage jaotist **Laoseis**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-150">Expand or collapse the **Inventory** section.</span></span>
6. <span data-ttu-id="a8e9a-151">Sisestage väljale **Mitu** väärtus „10“.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-151">In the **Multiple** field, type '10'.</span></span>
7. <span data-ttu-id="a8e9a-152">Tippige väljale **min. tellimuse kogus** väärtus 10.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-152">In the **Min. order quantity** field, type '10'.</span></span>
8. <span data-ttu-id="a8e9a-153">Tippige väljale **maks. tellimuse kogus** väärtus 100.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-153">In the **Max. order quantity** field, type '100'.</span></span>
9. <span data-ttu-id="a8e9a-154">Tippige väljale **standard tellimuse kogus** väärtus 10.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-154">In the **Standard order quantity**, type '10'.</span></span>
10. <span data-ttu-id="a8e9a-155">Sisestage number väljale **Ostu täitmisaeg**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-155">In the **Purchase lead time** field, enter a number.</span></span>
11. <span data-ttu-id="a8e9a-156">Valige või puhastage märkeruut **Tööpäevad**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-156">Select or clear the **Working days** check box.</span></span>
12. <span data-ttu-id="a8e9a-157">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-157">Click **Save**.</span></span>
13. <span data-ttu-id="a8e9a-158">Väljal **Vaiketellimuse tüüp** valige „Ostutellimus“.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-158">In the **Default order type** field select 'Purchase order'.</span></span>
14. <span data-ttu-id="a8e9a-159">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-159">Click **Save**.</span></span>
15. <span data-ttu-id="a8e9a-160">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-160">Close the page.</span></span> <span data-ttu-id="a8e9a-161">Sulgege leht Tellimuse vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-161">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="a8e9a-162">Kauba lisamine laovarude gruppi</span><span class="sxs-lookup"><span data-stu-id="a8e9a-162">Add an item to a coverage group</span></span>
1. <span data-ttu-id="a8e9a-163">Laiendage või ahendage jaotist **Plaan**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-163">Expand or collapse the **Plan** section.</span></span>
2. <span data-ttu-id="a8e9a-164">Klõpsake väljal **Laovarude grupp** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-164">In the **Coverage group** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a8e9a-165">Leidke loendist loodud **laovarude grupp**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-165">In the list, find the **Coverage group** you have created.</span></span>
4. <span data-ttu-id="a8e9a-166">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-166">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="a8e9a-167">Kauba laovarude reeglite loomine</span><span class="sxs-lookup"><span data-stu-id="a8e9a-167">Create item coverage rules</span></span>
1. <span data-ttu-id="a8e9a-168">Klõpsake **Toimingupaanil** valikut **Plaan**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-168">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="a8e9a-169">Jaotises **Laovarud** klõpsake valikut **Kauba laovaru**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-169">Under **Coverage**, click **Item coverage**.</span></span>
3. <span data-ttu-id="a8e9a-170">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-170">Click **New**.</span></span>
4. <span data-ttu-id="a8e9a-171">Klõpsake vahekaarti **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-171">Click the **General** tab.</span></span>
5. <span data-ttu-id="a8e9a-172">Märkige ruut suvandi **Tühista laovarude rühma** sätted päises.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-172">Check the box on the header of **Override coverage group** settings.</span></span>
6. <span data-ttu-id="a8e9a-173">Sisestage väärtus „60” väljale **Laovarude ajapiir (päevades)**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-173">In the **Coverage time fence (days)** field, enter '60'.</span></span> <span data-ttu-id="a8e9a-174">Kuigi kaubad laovarude grupis Vajadus on plaanitud 90 päeva ette, plaanitakse see kaup 60 päeva ette.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-174">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="a8e9a-175">Sisestage väärtus „2” väljale **Negatiivsed päevad**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-175">In the **Negative days** field, enter '2'.</span></span>
8. <span data-ttu-id="a8e9a-176">Sisestage väärtus „2” väljale **Positiivsed päevad**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-176">In the **Positive days** field, enter '2'.</span></span>
9. <span data-ttu-id="a8e9a-177">Klõpsake vahekaarti **Täitmisaeg**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-177">Click the **Lead time** tab.</span></span>
10. <span data-ttu-id="a8e9a-178">Märkige ruut suvandi **Ost** päises.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-178">Check the box on the header of **Purchase**.</span></span>
11. <span data-ttu-id="a8e9a-179">Sisestage väljale **Ostu aeg** väärtus „5“.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-179">In the **Purchase time** field, enter '5'.</span></span>
12. <span data-ttu-id="a8e9a-180">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a8e9a-180">Click **Save**.</span></span>

