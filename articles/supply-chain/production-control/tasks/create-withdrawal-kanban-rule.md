--- 
title: "Väljastamise kanban-reegli loomine"
description: "See protseduur näitab seadistust, mida on vaja, et luua tühistamise kanban-reegel materjali ülekandmiseks säästlikus keskkonnas."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 02c7133d2e02b27fb428874deeda21e2bab28fb6
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="68b08-103">Väljastamise kanban-reegli loomine</span><span class="sxs-lookup"><span data-stu-id="68b08-103">Create a withdrawal kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="68b08-104">See protseduur näitab seadistust, mida on vaja, et luua tühistamise kanban-reegel materjali ülekandmiseks säästlikus keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="68b08-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="68b08-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="68b08-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="68b08-106">Protseduur on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud materjali täiendamist.</span><span class="sxs-lookup"><span data-stu-id="68b08-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="68b08-107">Uue kanban-reegli loomine</span><span class="sxs-lookup"><span data-stu-id="68b08-107">Create new kanban rule</span></span>
1. <span data-ttu-id="68b08-108">Minge jaotisse Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="68b08-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="68b08-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="68b08-109">Click New.</span></span>
3. <span data-ttu-id="68b08-110">Tehke väljal Tüüp vali Tühistamine.</span><span class="sxs-lookup"><span data-stu-id="68b08-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="68b08-111">Kanban-reeglite puhul kasutatakse materjalide või kaupade edastamiseks tüüpi Tühistamine.</span><span class="sxs-lookup"><span data-stu-id="68b08-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="68b08-112">Sisestage või valige väärtus väljal Esimene plaanitegevus.</span><span class="sxs-lookup"><span data-stu-id="68b08-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="68b08-113">Tehke valik ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="68b08-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="68b08-114">See tegevus on seadistatud teisaldama komponente laost 11, asukohast 11 lattu 12 ja asukohta 12.</span><span class="sxs-lookup"><span data-stu-id="68b08-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="68b08-115">Sisestage või valige väärtus väljal Toode.</span><span class="sxs-lookup"><span data-stu-id="68b08-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="68b08-116">Valige suvand M0007.</span><span class="sxs-lookup"><span data-stu-id="68b08-116">Select M0007.</span></span>  
6. <span data-ttu-id="68b08-117">Sisestage number väljale Täitmisaeg.</span><span class="sxs-lookup"><span data-stu-id="68b08-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="68b08-118">Näiteks 60.</span><span class="sxs-lookup"><span data-stu-id="68b08-118">For example, 60.</span></span>  
7. <span data-ttu-id="68b08-119">Sisestage või valige väärtus väljal Mõõtühik.</span><span class="sxs-lookup"><span data-stu-id="68b08-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="68b08-120">Näiteks minutid.</span><span class="sxs-lookup"><span data-stu-id="68b08-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="68b08-121">Kanbanile koguste määramine</span><span class="sxs-lookup"><span data-stu-id="68b08-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="68b08-122">Valige välja Vaikekogus väärtuseks 5.</span><span class="sxs-lookup"><span data-stu-id="68b08-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="68b08-123">See on iga kanbani kohta üle kantav kogus.</span><span class="sxs-lookup"><span data-stu-id="68b08-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="68b08-124">Siseatage väljale Fikseeritud kanban-kogus väärtus 2.</span><span class="sxs-lookup"><span data-stu-id="68b08-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="68b08-125">See on kanbanide, mis peaksid olema aktiivsed, arv.</span><span class="sxs-lookup"><span data-stu-id="68b08-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="68b08-126">Sellisel juhul edastavad iga 2 kanbani 5.</span><span class="sxs-lookup"><span data-stu-id="68b08-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="68b08-127">Sisestage väljale Teatise miinimumpiir väärtus 1.</span><span class="sxs-lookup"><span data-stu-id="68b08-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="68b08-128">Kasutatakse täielike kanbanide, mis peaks olema sihtkohas, minimaalse summa jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="68b08-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="68b08-129">Näiteks kasutatakse seda kanban-koguse ülevaates.</span><span class="sxs-lookup"><span data-stu-id="68b08-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="68b08-130">Sisestage väljale Teatise maksimumpiir väärtus 2.</span><span class="sxs-lookup"><span data-stu-id="68b08-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="68b08-131">Kasutatakse täielike kanbanide, mis peaks olema sihtkohas, maksimaalse summa jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="68b08-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="68b08-132">Näiteks kasutatakse seda kanban-koguse ülevaates.</span><span class="sxs-lookup"><span data-stu-id="68b08-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="68b08-133">Loo kanbane</span><span class="sxs-lookup"><span data-stu-id="68b08-133">Create kanbans</span></span>
1. <span data-ttu-id="68b08-134">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="68b08-134">Click Save.</span></span>
    * <span data-ttu-id="68b08-135">Enne, kui kanbane saab luua, tuleb kanban-reegel salvestada.</span><span class="sxs-lookup"><span data-stu-id="68b08-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="68b08-136">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="68b08-136">Click Add.</span></span>
    * <span data-ttu-id="68b08-137">Pange tähele, et aktiivseid kanbane pole, kuna soovituslik uute kanbanide arv on 2, mis võrdub fikseeritud kanban-kogusega.</span><span class="sxs-lookup"><span data-stu-id="68b08-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="68b08-138">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="68b08-138">Click Create.</span></span>
    * <span data-ttu-id="68b08-139">See loob kaks kanbani.</span><span class="sxs-lookup"><span data-stu-id="68b08-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="68b08-140">Pange tähele, et selle tühistamise kanban-reegli puhul loodi 2 kanbani, igaühe kohta 5.</span><span class="sxs-lookup"><span data-stu-id="68b08-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="68b08-141">See on selle protseduuri viimane etapp.</span><span class="sxs-lookup"><span data-stu-id="68b08-141">This is the last step in this procedure.</span></span>  


