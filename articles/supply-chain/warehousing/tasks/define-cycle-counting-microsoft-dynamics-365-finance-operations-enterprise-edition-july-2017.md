--- 
title: "Tsüklilise inventuuri määratlemine "
description: "Tsükliline inventuur on laoprotsess, mida saate kaupade laovaru kontrollimiseks kasutada."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5a95f63efe3d78dc371cacdc09734490a601b1b8
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="define-cycle-counting"></a><span data-ttu-id="88ead-103">Tsüklilise inventuuri määratlemine </span><span class="sxs-lookup"><span data-stu-id="88ead-103">Define cycle counting</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="88ead-104">Tsükliline inventuur on laoprotsess, mida saate kaupade laovaru kontrollimiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="88ead-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="88ead-105">See tegevuse salvestis näitab, kuidas seadistada inventuuritöö vaikeprioriteeti, lubada mobiilse seadme menüü-üksusel töödelda nii komplekteerimis- kui ka inventuuritoiminguid, lubada inventuuri läve käivitumist, kui asukoht saab tühjaks ja lubada tsüklilise inventuuri plaani teatud kauba kohta kindlas laos.</span><span class="sxs-lookup"><span data-stu-id="88ead-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="88ead-106">Tavaliselt teeb need toimingud laojuht.</span><span class="sxs-lookup"><span data-stu-id="88ead-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="88ead-107">Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="88ead-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="88ead-108">Inventuuritöö prioriteedi määramine</span><span class="sxs-lookup"><span data-stu-id="88ead-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="88ead-109">Avage Laohaldus > Seadistus > Laohalduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="88ead-109">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="88ead-110">Klõpsake vahekaarti Tsükliline inventuur.</span><span class="sxs-lookup"><span data-stu-id="88ead-110">Click the Cycle counting tab.</span></span>
3. <span data-ttu-id="88ead-111">Sisestage number väljale Tsüklilise inventuuri töö vaikeprioriteet.</span><span class="sxs-lookup"><span data-stu-id="88ead-111">In the Default cycle count work priority field, enter a number.</span></span>
    * <span data-ttu-id="88ead-112">See toiming muudab tsüklilise inventuuri töö prioriteeti võrreldes muud tüüpi töödega laos.</span><span class="sxs-lookup"><span data-stu-id="88ead-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="88ead-113">Kui sisestate väiksema numbri kui muud tüüpi töödele, tõstate tsüklilise inventuuri töö prioriteeti.</span><span class="sxs-lookup"><span data-stu-id="88ead-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="88ead-114">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="88ead-114">Click Save.</span></span>
5. <span data-ttu-id="88ead-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="88ead-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="88ead-116">Lubage mobiilne seade</span><span class="sxs-lookup"><span data-stu-id="88ead-116">Enable the mobile device</span></span>
1. <span data-ttu-id="88ead-117">Avage Laohaldus > Seadistus > Mobiilne seade > Mobiilse seadme menüü-üksused.</span><span class="sxs-lookup"><span data-stu-id="88ead-117">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="88ead-118">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="88ead-118">Click New.</span></span>
3. <span data-ttu-id="88ead-119">Sisestage väärtus väljale Menüü-üksuse nimi.</span><span class="sxs-lookup"><span data-stu-id="88ead-119">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="88ead-120">Sisestage väärtus väljale Pealkiri.</span><span class="sxs-lookup"><span data-stu-id="88ead-120">In the Title field, type a value.</span></span>
5. <span data-ttu-id="88ead-121">Valige väljal Režiim suvand Töö.</span><span class="sxs-lookup"><span data-stu-id="88ead-121">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="88ead-122">Valige suvandi Kasuta olemasolevat tööd sätteks Jah.</span><span class="sxs-lookup"><span data-stu-id="88ead-122">Set the Use existing work option to Yes.</span></span>
    * <span data-ttu-id="88ead-123">Kui määrate selle suvandi väärtuseks Jah, otsib süsteem olemasolevat tööd, kui kasutatakse mobiilse seadme menüü-üksust.</span><span class="sxs-lookup"><span data-stu-id="88ead-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="88ead-124">Valige väljal Suunaja suvand Süsteemi suunatud.</span><span class="sxs-lookup"><span data-stu-id="88ead-124">In the Directed by field, select 'System directed'.</span></span>
    * <span data-ttu-id="88ead-125">"Süsteemi suunatud" valimisel suunatakse laotöötaja tööklassides määratud avatud tööle.</span><span class="sxs-lookup"><span data-stu-id="88ead-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="88ead-126">(Loome järgmisena need tööklassid.)</span><span class="sxs-lookup"><span data-stu-id="88ead-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="88ead-127">Laiendage või ahendage jaotist Töö klassid.</span><span class="sxs-lookup"><span data-stu-id="88ead-127">Expand or collapse the Work classes section.</span></span>
    * <span data-ttu-id="88ead-128">Järgmisena loome kaks tööklassi, mida kasutatakse selle mobiilse seadme menüü-üksusega.</span><span class="sxs-lookup"><span data-stu-id="88ead-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="88ead-129">Menüü-üksuse kasutamisel esitatakse päring nende tööklasside kohta ja kasutajale kuvatakse kõrgeima prioriteediga töö.</span><span class="sxs-lookup"><span data-stu-id="88ead-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="88ead-130">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="88ead-130">Click New.</span></span>
10. <span data-ttu-id="88ead-131">Valige väärtus väljal Tööklassi ID.</span><span class="sxs-lookup"><span data-stu-id="88ead-131">In the Work class ID field, select a value.</span></span>
11. <span data-ttu-id="88ead-132">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="88ead-132">Click New.</span></span>
12. <span data-ttu-id="88ead-133">Valige väärtus väljal Tööklassi ID.</span><span class="sxs-lookup"><span data-stu-id="88ead-133">In the Work class ID field, select a value.</span></span>
13. <span data-ttu-id="88ead-134">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="88ead-134">Click Save.</span></span>
14. <span data-ttu-id="88ead-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="88ead-135">Close the page.</span></span>
15. <span data-ttu-id="88ead-136">Avage Laohaldus > Seadistus > Mobiilne seade > Mobiilse seadme menüü.</span><span class="sxs-lookup"><span data-stu-id="88ead-136">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
16. <span data-ttu-id="88ead-137">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="88ead-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="88ead-138">Valige puul äsjaloodud menüü-üksus.</span><span class="sxs-lookup"><span data-stu-id="88ead-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="88ead-139">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="88ead-139">Click Edit.</span></span>
19. <span data-ttu-id="88ead-140">Klõpsake menüü-üksuse menüüsse lisamiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="88ead-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="88ead-141">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="88ead-141">Click Save.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="88ead-142">Looge inventuurilävi</span><span class="sxs-lookup"><span data-stu-id="88ead-142">Create a counting threshold</span></span>
1. <span data-ttu-id="88ead-143">Avage Laohaldus > Seadistus > Tsükliline inventuur > Tsüklilise inventuuri läved.</span><span class="sxs-lookup"><span data-stu-id="88ead-143">Go to Warehouse management > Setup > Cycle counting > Cycle count thresholds.</span></span>
2. <span data-ttu-id="88ead-144">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="88ead-144">Click New.</span></span>
3. <span data-ttu-id="88ead-145">Sisestage väärtus väljale Tsüklilise inventuuri läve ID.</span><span class="sxs-lookup"><span data-stu-id="88ead-145">In the Cycle counting threshold ID field, type a value.</span></span>
4. <span data-ttu-id="88ead-146">Valige suvandi Töötle tsüklilist inventuuri kohe sätteks Jah.</span><span class="sxs-lookup"><span data-stu-id="88ead-146">Set the Process cycle counting immediately option to Yes.</span></span>
5. <span data-ttu-id="88ead-147">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="88ead-147">In the Description field, type a value.</span></span>
6. <span data-ttu-id="88ead-148">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="88ead-148">Click Save.</span></span>
7. <span data-ttu-id="88ead-149">Klõpsake suvandit Valige asukohad.</span><span class="sxs-lookup"><span data-stu-id="88ead-149">Click Select locations.</span></span>
8. <span data-ttu-id="88ead-150">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="88ead-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="88ead-151">Valige väärtus väljal Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="88ead-151">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="88ead-152">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="88ead-152">Click OK.</span></span>
11. <span data-ttu-id="88ead-153">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="88ead-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="88ead-154">Looge tsüklilise inventuuri plaan</span><span class="sxs-lookup"><span data-stu-id="88ead-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="88ead-155">Avage Laohaldus > Seadistus > Tsükliline inventuur > Tsüklilise inventuuri plaanid.</span><span class="sxs-lookup"><span data-stu-id="88ead-155">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="88ead-156">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="88ead-156">Click New.</span></span>
3. <span data-ttu-id="88ead-157">Sisestage väärtus väljale Tsüklilise inventuuri plaani ID.</span><span class="sxs-lookup"><span data-stu-id="88ead-157">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="88ead-158">Sisestage väärtus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="88ead-158">In the Description field, type a value.</span></span>
5. <span data-ttu-id="88ead-159">Sisestage number väljale Tsükliliste inventuuride maksimumarv.</span><span class="sxs-lookup"><span data-stu-id="88ead-159">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="88ead-160">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="88ead-160">Click Save.</span></span>
7. <span data-ttu-id="88ead-161">Klõpsake suvandit Valige asukohad.</span><span class="sxs-lookup"><span data-stu-id="88ead-161">Click Select locations.</span></span>
8. <span data-ttu-id="88ead-162">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="88ead-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="88ead-163">Valige väärtus väljal Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="88ead-163">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="88ead-164">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="88ead-164">Click OK.</span></span>
11. <span data-ttu-id="88ead-165">Sisestage number väljale Päevi tsükliliste inventuuride vahel.</span><span class="sxs-lookup"><span data-stu-id="88ead-165">In the Days between cycle counting field, enter a number.</span></span>
    * <span data-ttu-id="88ead-166">Näiteks kui välja Päevi tsükliliste inventuuride vahel väärtuseks on määratud 5, luuakse tsüklilise inventuuri töö iga viie päeva järel.</span><span class="sxs-lookup"><span data-stu-id="88ead-166">For example, if the Days between cycle counting field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="88ead-167">Kuid kui tsüklilise inventuuri töö töödeldakse kolmandal päeval, luuakse järgmine tsüklilise inventuuri töö viis päeva pärast viimase tsüklilise inventuuri töö töötlemist, kaheksandal päeval.</span><span class="sxs-lookup"><span data-stu-id="88ead-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="88ead-168">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="88ead-168">Click Save.</span></span>
13. <span data-ttu-id="88ead-169">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="88ead-169">Click New.</span></span>
14. <span data-ttu-id="88ead-170">Sisestage number väljale Seerianumber.</span><span class="sxs-lookup"><span data-stu-id="88ead-170">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="88ead-171">Sortimisjärjestus on kõige väiksemast numbrist suurima numbrini.</span><span class="sxs-lookup"><span data-stu-id="88ead-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="88ead-172">Väärtus peab olema suurem kui 0 (null).</span><span class="sxs-lookup"><span data-stu-id="88ead-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="88ead-173">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="88ead-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="88ead-174">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="88ead-174">In the Description field, type a value.</span></span>
17. <span data-ttu-id="88ead-175">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="88ead-175">Click Save.</span></span>
18. <span data-ttu-id="88ead-176">Klõpsake valikut Määratle tootepäring.</span><span class="sxs-lookup"><span data-stu-id="88ead-176">Click Define product query.</span></span>
19. <span data-ttu-id="88ead-177">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="88ead-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="88ead-178">Sisestage või valige väärtus väljal Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="88ead-178">In the Criteria field, enter or select a value.</span></span>
21. <span data-ttu-id="88ead-179">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="88ead-179">Click OK.</span></span>
22. <span data-ttu-id="88ead-180">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="88ead-180">Close the page.</span></span>


