---
title: 'Tsüklilise inventuuri määratlemine '
description: Tsükliline inventuur on laoprotsess, mida saate kaupade laovaru kontrollimiseks kasutada.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountThreshold, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSParameters, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8b7f39fc9a91d9fe219445e409d000266e24775
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016144"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="e2be5-103">Tsüklilise inventuuri määratlemine </span><span class="sxs-lookup"><span data-stu-id="e2be5-103">Define cycle counting</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2be5-104">Tsükliline inventuur on laoprotsess, mida saate kaupade laovaru kontrollimiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="e2be5-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="e2be5-105">See tegevuse salvestis näitab, kuidas seadistada inventuuritöö vaikeprioriteeti, lubada mobiilse seadme menüü-üksusel töödelda nii komplekteerimis- kui ka inventuuritoiminguid, lubada inventuuri läve käivitumist, kui asukoht saab tühjaks ja lubada tsüklilise inventuuri plaani teatud kauba kohta kindlas laos.</span><span class="sxs-lookup"><span data-stu-id="e2be5-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="e2be5-106">Tavaliselt teeb need toimingud laojuht.</span><span class="sxs-lookup"><span data-stu-id="e2be5-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="e2be5-107">Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="e2be5-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="e2be5-108">Inventuuritöö prioriteedi määramine</span><span class="sxs-lookup"><span data-stu-id="e2be5-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="e2be5-109">Paanil **Navigeerimispaan** avage **Moodulid > Laohaldus > Seadistus > Ladu > Laohalduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-109">In the **Navigation pane** , go to **Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="e2be5-110">Klõpsake vahekaarti **Tsükliline inventuur**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-110">Click the **Cycle counting** tab.</span></span>
3. <span data-ttu-id="e2be5-111">Väljale **Vaikimisi tsüklilise inventuuri töö prioriteet** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="e2be5-111">In the **Default cycle count work priority** field, enter a number.</span></span> <span data-ttu-id="e2be5-112">See toiming muudab tsüklilise inventuuri töö prioriteeti võrreldes muud tüüpi töödega laos.</span><span class="sxs-lookup"><span data-stu-id="e2be5-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="e2be5-113">Kui sisestate väiksema numbri kui muud tüüpi töödele, tõstate tsüklilise inventuuri töö prioriteeti.</span><span class="sxs-lookup"><span data-stu-id="e2be5-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="e2be5-114">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-114">Click **Save**.</span></span>
5. <span data-ttu-id="e2be5-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e2be5-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="e2be5-116">Lubage mobiilne seade</span><span class="sxs-lookup"><span data-stu-id="e2be5-116">Enable the mobile device</span></span>
1. <span data-ttu-id="e2be5-117">Paanil **Navigeerimispaan** avage **Moodulid > Laohaldus > Seadistus > Mobiiliseade > Mobiiliseadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-117">In the **Navigation pane** , go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="e2be5-118">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-118">Click **New**.</span></span>
3. <span data-ttu-id="e2be5-119">Sisestage väärtus väljale **Menüü-üksuse nimi**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-119">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="e2be5-120">Sisestage väärtus väljale **Pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-120">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="e2be5-121">Väljal **Režiim** valige "Töö".</span><span class="sxs-lookup"><span data-stu-id="e2be5-121">In the **Mode** field, select 'Work'.</span></span>
6. <span data-ttu-id="e2be5-122">Seadke suvandi **Kasuta olemasolevat tööd** väärtuseks Jah.</span><span class="sxs-lookup"><span data-stu-id="e2be5-122">Set the **Use existing work** option to Yes.</span></span> <span data-ttu-id="e2be5-123">Kui määrate selle suvandi väärtuseks Jah, otsib süsteem olemasolevat tööd, kui kasutatakse mobiilse seadme menüü-üksust.</span><span class="sxs-lookup"><span data-stu-id="e2be5-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="e2be5-124">Väljale **Juhtija** valige "Süsteemi suunatud".</span><span class="sxs-lookup"><span data-stu-id="e2be5-124">In the **Directed by** field, select 'System directed'.</span></span> <span data-ttu-id="e2be5-125">"Süsteemi suunatud" valimisel suunatakse laotöötaja tööklassides määratud avatud tööle.</span><span class="sxs-lookup"><span data-stu-id="e2be5-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="e2be5-126">(Loome järgmisena need tööklassid.)</span><span class="sxs-lookup"><span data-stu-id="e2be5-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="e2be5-127">Laiendage kiirkaarti **Tööklassid**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-127">Expand the **Work classes** fastTab.</span></span> <span data-ttu-id="e2be5-128">Järgmisena loome kaks tööklassi, mida kasutatakse selle mobiilse seadme menüü-üksusega.</span><span class="sxs-lookup"><span data-stu-id="e2be5-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="e2be5-129">Menüü-üksuse kasutamisel esitatakse päring nende tööklasside kohta ja kasutajale kuvatakse kõrgeima prioriteediga töö.</span><span class="sxs-lookup"><span data-stu-id="e2be5-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="e2be5-130">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-130">Click **New**.</span></span>
10. <span data-ttu-id="e2be5-131">Väljale **Tööklassi ID** valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="e2be5-131">In the **Work class ID** field, select a value.</span></span>
11. <span data-ttu-id="e2be5-132">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-132">Click **New**.</span></span>
12. <span data-ttu-id="e2be5-133">Väljale **Tööklassi ID** valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="e2be5-133">In the **Work class ID** field, select a value.</span></span>
13. <span data-ttu-id="e2be5-134">Klõpsake paanil **Toimingupaan** suvandit **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-134">In the **Action Pane** , click **Save**.</span></span>
14. <span data-ttu-id="e2be5-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e2be5-135">Close the page.</span></span>
15. <span data-ttu-id="e2be5-136">Paanil **Navigeerimispaan** avage **Moodulid > Laohaldus > Seadistus > Mobiiliseade > Mobiiliseadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-136">In the **Navigation pane** , go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
16. <span data-ttu-id="e2be5-137">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e2be5-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="e2be5-138">Valige puul äsjaloodud menüü-üksus.</span><span class="sxs-lookup"><span data-stu-id="e2be5-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="e2be5-139">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-139">Click **Edit**.</span></span>
19. <span data-ttu-id="e2be5-140">Klõpsake menüü-üksuse menüüsse lisamiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="e2be5-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="e2be5-141">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-141">Click **Save**.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="e2be5-142">Looge inventuurilävi</span><span class="sxs-lookup"><span data-stu-id="e2be5-142">Create a counting threshold</span></span>
1. <span data-ttu-id="e2be5-143">Paanil **Navigeerimispaan** avage **Moodulid > Laohaldus > Seadistus > Tsükliline inventuur > Tsüklilise inventuuri läved**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-143">In the **Navigation pane** , go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count thresholds**.</span></span>
2. <span data-ttu-id="e2be5-144">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-144">Click **New**.</span></span>
3. <span data-ttu-id="e2be5-145">Väljale **Tsüklilise inventuuri läve ID** sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="e2be5-145">In the **Cycle counting threshold ID** field, type a value.</span></span>
4. <span data-ttu-id="e2be5-146">Seadke suvandi **Töötle tsüklilist inventuuri kohe** väärtuseks Jah.</span><span class="sxs-lookup"><span data-stu-id="e2be5-146">Set the **Process cycle counting immediately** option to Yes.</span></span>
5. <span data-ttu-id="e2be5-147">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-147">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="e2be5-148">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-148">Click **Save**.</span></span>
7. <span data-ttu-id="e2be5-149">Klõpsake **Vali asukohad**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-149">Click **Select locations**.</span></span>
8. <span data-ttu-id="e2be5-150">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e2be5-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="e2be5-151">Väljal **Kriteerium** valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="e2be5-151">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="e2be5-152">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-152">Click **OK**.</span></span>
11. <span data-ttu-id="e2be5-153">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e2be5-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="e2be5-154">Looge tsüklilise inventuuri plaan</span><span class="sxs-lookup"><span data-stu-id="e2be5-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="e2be5-155">Paanil **Navigeerimispaan** avage **Moodulid > Laohaldus > Seadistus > Tsükliline inventuur > Tsüklilise inventuuri plaanid**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-155">In the **Navigation pane** , go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count plans**.</span></span>
2. <span data-ttu-id="e2be5-156">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-156">Click **New**.</span></span>
3. <span data-ttu-id="e2be5-157">Väljale **Tsüklilise inventuuri plaani ID** sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="e2be5-157">In the **Cycle counting plan ID** field, type a value.</span></span>
4. <span data-ttu-id="e2be5-158">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-158">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="e2be5-159">Väljale **Maksimaalne tsükliliste inventuuride arv** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="e2be5-159">In the **Maximum number of cycle counts** field, enter a number.</span></span>
6. <span data-ttu-id="e2be5-160">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-160">Click **Save**.</span></span>
7. <span data-ttu-id="e2be5-161">Klõpsake **Vali asukohad**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-161">Click **Select locations**.</span></span>
8. <span data-ttu-id="e2be5-162">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e2be5-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="e2be5-163">Väljal **Kriteerium** valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="e2be5-163">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="e2be5-164">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-164">Click **OK**.</span></span>
11. <span data-ttu-id="e2be5-165">Väljale **Päevi tsükliliste inventuuride vahel** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="e2be5-165">In the **Days between cycle counting** field, enter a number.</span></span> <span data-ttu-id="e2be5-166">Näiteks kui väljale **Päevi tsükliliste inventuuride vahel** sisestatud 5, luuakse tsüklilisi inventuure iga viie päeva järel.</span><span class="sxs-lookup"><span data-stu-id="e2be5-166">For example, if the **Days between cycle counting** field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="e2be5-167">Kuid kui tsüklilise inventuuri töö töödeldakse kolmandal päeval, luuakse järgmine tsüklilise inventuuri töö viis päeva pärast viimase tsüklilise inventuuri töö töötlemist, kaheksandal päeval.</span><span class="sxs-lookup"><span data-stu-id="e2be5-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="e2be5-168">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-168">Click **Save**.</span></span>
13. <span data-ttu-id="e2be5-169">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-169">Click **New**.</span></span>
14. <span data-ttu-id="e2be5-170">Sisestage arv väljale **Järjekorranumber**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-170">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="e2be5-171">Sortimisjärjestus on kõige väiksemast numbrist suurima numbrini.</span><span class="sxs-lookup"><span data-stu-id="e2be5-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="e2be5-172">Väärtus peab olema suurem kui 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e2be5-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="e2be5-173">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e2be5-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="e2be5-174">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-174">In the **Description** field, type a value.</span></span>
17. <span data-ttu-id="e2be5-175">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-175">Click **Save**.</span></span>
18. <span data-ttu-id="e2be5-176">Klõpsake päringut **Määratle toode**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-176">Click **Define product** query.</span></span>
19. <span data-ttu-id="e2be5-177">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e2be5-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="e2be5-178">Sisestage või valige väärtus väljal **Kriteeriumid**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-178">In the **Criteria** field, enter or select a value.</span></span>
21. <span data-ttu-id="e2be5-179">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2be5-179">Click **OK**.</span></span>
22. <span data-ttu-id="e2be5-180">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e2be5-180">Close the page.</span></span>

