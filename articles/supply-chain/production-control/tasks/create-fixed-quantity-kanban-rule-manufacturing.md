--- 
title: Fikseeritud kogusega kanban-reegli loomine tootmise jaoks
description: "See protseduur keskendub teisendustegevuste käivitamise eesmärgil fikseeritud tootmise kanban-reegli loomiseks vajalikele etappidele kulusäästliku keskkonna töörakus."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 555d79e8bacbae0287472e68701a04a3c1d635aa
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a><span data-ttu-id="f2110-103">Fikseeritud kogusega kanban-reegli loomine tootmise jaoks</span><span class="sxs-lookup"><span data-stu-id="f2110-103">Create a fixed quantity kanban rule for manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2110-104">See protseduur keskendub teisendustegevuste käivitamise eesmärgil fikseeritud tootmise kanban-reegli loomiseks vajalikele etappidele kulusäästliku keskkonna töörakus.</span><span class="sxs-lookup"><span data-stu-id="f2110-104">This procedure focuses on the setup needed to create a fixed manufacturing kanban rule for triggering transforming activities, at a work cell, in a lean environment.</span></span> <span data-ttu-id="f2110-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="f2110-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f2110-106">Protseduur on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud toote tootmist.</span><span class="sxs-lookup"><span data-stu-id="f2110-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="f2110-107">Uue kanban-reegli loomine</span><span class="sxs-lookup"><span data-stu-id="f2110-107">Create new kanban rule</span></span>
1. <span data-ttu-id="f2110-108">Minge jaotisse Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="f2110-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="f2110-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f2110-109">Click New.</span></span>
    * <span data-ttu-id="f2110-110">Pange tähele, et suvandi Tüüp vaikesäte on Tootmine ja suvandi Täiendusstrateegia vaikesäte on Fikseeritud.</span><span class="sxs-lookup"><span data-stu-id="f2110-110">Notice that the default Type is Manufacturing and Replenishment strategy is Fixed.</span></span> <span data-ttu-id="f2110-111">Te ei pea neid parameetreid muutma.</span><span class="sxs-lookup"><span data-stu-id="f2110-111">You do not have to change these parameters.</span></span>  
3. <span data-ttu-id="f2110-112">Sisestage või valige väärtus väljal Esimene plaanitegevus.</span><span class="sxs-lookup"><span data-stu-id="f2110-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="f2110-113">See on tegevus, mis teostatakse selle kanban-reegli põhjal loodud kanbanide puhul.</span><span class="sxs-lookup"><span data-stu-id="f2110-113">This is the activity that will be performed for kanbans created based on this kanban rule.</span></span>  <span data-ttu-id="f2110-114">Valige suvand SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="f2110-114">Select 'SpeakerTestAndPackaging'.</span></span>  
4. <span data-ttu-id="f2110-115">Laiendage jaotist Üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="f2110-115">Expand the Details section.</span></span>
5. <span data-ttu-id="f2110-116">Sisestage või valige väärtus väljal Toode.</span><span class="sxs-lookup"><span data-stu-id="f2110-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="f2110-117">Valige suvand L0050.</span><span class="sxs-lookup"><span data-stu-id="f2110-117">Select L0050.</span></span>  
6. <span data-ttu-id="f2110-118">Sisestage või valige väärtus väljal Mõõtühik.</span><span class="sxs-lookup"><span data-stu-id="f2110-118">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="f2110-119">Valige minutid.</span><span class="sxs-lookup"><span data-stu-id="f2110-119">Select minutes.</span></span>  
7. <span data-ttu-id="f2110-120">Sisestage number väljale Täitmisaeg.</span><span class="sxs-lookup"><span data-stu-id="f2110-120">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="f2110-121">Sisestage väärtus 5.</span><span class="sxs-lookup"><span data-stu-id="f2110-121">Enter 5.</span></span>  

## <a name="set-quantities"></a><span data-ttu-id="f2110-122">Koguste määramine</span><span class="sxs-lookup"><span data-stu-id="f2110-122">Set quantities</span></span>
1. <span data-ttu-id="f2110-123">Laiendage jaotist Kogused.</span><span class="sxs-lookup"><span data-stu-id="f2110-123">Expand the Quantities section.</span></span>
2. <span data-ttu-id="f2110-124">Valige välja Vaikekogus väärtuseks 10.</span><span class="sxs-lookup"><span data-stu-id="f2110-124">Set Default quantity to '10'.</span></span>
    * <span data-ttu-id="f2110-125">See on iga kanbani kohta üle kantav kogus.</span><span class="sxs-lookup"><span data-stu-id="f2110-125">This is the quantity that will be transferred for each kanban.</span></span>  
3. <span data-ttu-id="f2110-126">Märkige ruut Toote koguse hälve.</span><span class="sxs-lookup"><span data-stu-id="f2110-126">Select the Product quantity variance check box.</span></span>
    * <span data-ttu-id="f2110-127">Sellega saab valitud kanbanid lõpule viia hälbega vaikekogusest.</span><span class="sxs-lookup"><span data-stu-id="f2110-127">With this, selected kanbans can be completed with a variance from the default quantity.</span></span>  <span data-ttu-id="f2110-128">Selleks ei võimaldada kanbanid lõpule viia kogusega 8 kuni 12, määrake mõlema hälbe väärtuseks 2.</span><span class="sxs-lookup"><span data-stu-id="f2110-128">To allow kanbans to be completed with a quantity from 8 to 12, set both variances to 2.</span></span>  
4. <span data-ttu-id="f2110-129">Valige välja Hälve alla väärtuseks 2.</span><span class="sxs-lookup"><span data-stu-id="f2110-129">Set Variance below to '2'.</span></span>
    * <span data-ttu-id="f2110-130">See võimaldab allapoole lõpuleviimist 10 – 2 = 8</span><span class="sxs-lookup"><span data-stu-id="f2110-130">This will allow completing down to 10 - 2 = 8</span></span>  
5. <span data-ttu-id="f2110-131">Valige välja Hälve üle väärtuseks 2.</span><span class="sxs-lookup"><span data-stu-id="f2110-131">Set Variance above to '2'.</span></span>
    * <span data-ttu-id="f2110-132">See võimaldab ülespoole lõpule viimist 10 + 2 = 12</span><span class="sxs-lookup"><span data-stu-id="f2110-132">This will allow completing up to 10 + 2 = 12</span></span>  
6. <span data-ttu-id="f2110-133">Sisestage number väljale Fikseeritud kanban-kogus.</span><span class="sxs-lookup"><span data-stu-id="f2110-133">In the Fixed kanban quantity field, enter a number.</span></span>
    * <span data-ttu-id="f2110-134">See on kanbanide, mis peaksid olema aktiivsed, arv.</span><span class="sxs-lookup"><span data-stu-id="f2110-134">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="f2110-135">Sel juhul töötlevad viiest kanbanist igaüks kümmet.</span><span class="sxs-lookup"><span data-stu-id="f2110-135">In this case, 5 kanbans processing 10 each.</span></span>  
7. <span data-ttu-id="f2110-136">Sisestage väljale Teatise miinimumpiir väärtus 2.</span><span class="sxs-lookup"><span data-stu-id="f2110-136">In the Alert boundary minimum field, enter '2'.</span></span>
    * <span data-ttu-id="f2110-137">Kasutatakse täielike kanbanide, mis peaks olema sihtkohas, minimaalse summa jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="f2110-137">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="f2110-138">Näiteks kasutatakse seda kanban-koguse ülevaates.</span><span class="sxs-lookup"><span data-stu-id="f2110-138">For example, this is used on the kanban quantity overview.</span></span>  
8. <span data-ttu-id="f2110-139">Sisestage väljale Teatise maksimumpiir väärtus 4.</span><span class="sxs-lookup"><span data-stu-id="f2110-139">In the Alert boundary maximum field, enter '4'.</span></span>
    * <span data-ttu-id="f2110-140">Kasutatakse täielike kanbanide, mis peaks olema sihtkohas, maksimaalse summa jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="f2110-140">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="f2110-141">Näiteks kasutatakse seda kanban-koguse ülevaates.</span><span class="sxs-lookup"><span data-stu-id="f2110-141">For example, this is used on the kanban quantity overview.</span></span>  
9. <span data-ttu-id="f2110-142">Sisestage väljale Automaatse plaanimise kogus väärtus 1.</span><span class="sxs-lookup"><span data-stu-id="f2110-142">In the Automatic planning quantity field, enter '1'.</span></span>
    * <span data-ttu-id="f2110-143">Kui valite selle väärtuseks 1, plaanitakse iga kanban automaatselt.</span><span class="sxs-lookup"><span data-stu-id="f2110-143">Setting this to 1 means that every kanban will be automatically planned.</span></span>   <span data-ttu-id="f2110-144">Kui valite väärtuseks 3, ei plaanita kanbane enne, kui 3 tühja kanbani on plaanimiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="f2110-144">If we entered 3, the kanbans would not be planned until 3 empty kanbans are ready for planning.</span></span> <span data-ttu-id="f2110-145">See on kasulik töö grupeerimiseks ja liiga paljude etappide vältimiseks.</span><span class="sxs-lookup"><span data-stu-id="f2110-145">This is useful for grouping work and avoiding too much setup.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="f2110-146">Kanbanide loomine</span><span class="sxs-lookup"><span data-stu-id="f2110-146">Create Kanbans</span></span>
1. <span data-ttu-id="f2110-147">Laiendage jaotist Kanbanid.</span><span class="sxs-lookup"><span data-stu-id="f2110-147">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="f2110-148">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f2110-148">Click Save.</span></span>
    * <span data-ttu-id="f2110-149">Enne, kui kanbane saab luua, tuleb kanban-reegel salvestada.</span><span class="sxs-lookup"><span data-stu-id="f2110-149">The kanban rule needs to be saved before kanbans can be created.</span></span>  
3. <span data-ttu-id="f2110-150">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f2110-150">Click Add.</span></span>
    * <span data-ttu-id="f2110-151">Pange tähele, et aktiivseid kanbane ei ole, seetõttu on välja "Uute kanbanide arv" soovitatav väärtus 5.</span><span class="sxs-lookup"><span data-stu-id="f2110-151">Note that there are no active kanbans, due to this the suggested 'Number of new kanbans' are 5.</span></span> <span data-ttu-id="f2110-152">See on võrdne väärtusega "Fikseeritud kanban-kogus".</span><span class="sxs-lookup"><span data-stu-id="f2110-152">This is equal to the 'Fixed kanban quantity'.</span></span>  
4. <span data-ttu-id="f2110-153">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="f2110-153">Click Create.</span></span>
    * <span data-ttu-id="f2110-154">See loob 5 kanbani.</span><span class="sxs-lookup"><span data-stu-id="f2110-154">This will create 5 kanbans.</span></span>  
    * <span data-ttu-id="f2110-155">Pange tähele, et selle tootmise kanban-reegli puhul loodi 5 kanbani, igaühe kohta 10.</span><span class="sxs-lookup"><span data-stu-id="f2110-155">Note that 5 kanbans, for 10 each, was created for this manufacturing kanban rule.</span></span> <span data-ttu-id="f2110-156">See on selle protseduuri viimane etapp.</span><span class="sxs-lookup"><span data-stu-id="f2110-156">This is the last step in this procedure.</span></span>  


