---
title: Minimaalsete laovarude sündmuse abil kanban-reegli loomine
description: See protseduur keskendub seadistusele, mis on vajalik kanban-reegli loomiseks, kasutades minimaalset laosündmust tagamiseks, et konkreetne toode oleks alati konkreetses asukohas saadaval.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 297ee73daf10dffd027dadec11725ae6f0408d4c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255153"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="77fa4-103">Minimaalsete laovarude sündmuse abil kanban-reegli loomine</span><span class="sxs-lookup"><span data-stu-id="77fa4-103">Create a kanban rule using a minimum stock event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="77fa4-104">See protseduur keskendub seadistusele, mis on vajalik kanban-reegli loomiseks, kasutades minimaalset laosündmust tagamiseks, et konkreetne toode oleks alati konkreetses asukohas saadaval.</span><span class="sxs-lookup"><span data-stu-id="77fa4-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="77fa4-105">Luuakse kanban-reegel materjali üleviimiseks asukohta, kui varude tase langeb alla 200 ühiku.</span><span class="sxs-lookup"><span data-stu-id="77fa4-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="77fa4-106">Sidumissündmuse töötlemise käivitamisega luuakse vajalikud kanbanid.</span><span class="sxs-lookup"><span data-stu-id="77fa4-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="77fa4-107">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="77fa4-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="77fa4-108">See toiming on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud toote tootmist säästlikus keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="77fa4-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="77fa4-109">Looge uus kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="77fa4-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="77fa4-110">Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="77fa4-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="77fa4-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="77fa4-111">Click New.</span></span>
3. <span data-ttu-id="77fa4-112">Tehke väljal Tüüp vali Tühistamine.</span><span class="sxs-lookup"><span data-stu-id="77fa4-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="77fa4-113">Seda tüüpi kasutatakse ülekande-kanbanide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="77fa4-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="77fa4-114">Valige väljal Täiendusstrateegia suvand Sündmus.</span><span class="sxs-lookup"><span data-stu-id="77fa4-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="77fa4-115">Sündmusel põhinevate kanbanide ülekandmise loomiseks kasutatakse sündmuse strateegiat.</span><span class="sxs-lookup"><span data-stu-id="77fa4-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="77fa4-116">Edaspidi käivitate protseduuris üleviimise kanbanid, kasutades varude täiendamist.</span><span class="sxs-lookup"><span data-stu-id="77fa4-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="77fa4-117">Sisestage või valige väärtus väljal Esimene plaanitegevus.</span><span class="sxs-lookup"><span data-stu-id="77fa4-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="77fa4-118">Sisestage või valige väärtus ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="77fa4-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="77fa4-119">Sellel ülekandmistegevusel on sissetulev (väljund) ladu ja asukoht 12, mis tähendab, et materjalid teisaldatakse asukohta 12 laos 12.</span><span class="sxs-lookup"><span data-stu-id="77fa4-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="77fa4-120">Laiendage jaotist Üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="77fa4-120">Expand the Details section.</span></span>
7. <span data-ttu-id="77fa4-121">Sisestage või valige väärtus väljal Toode.</span><span class="sxs-lookup"><span data-stu-id="77fa4-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="77fa4-122">Valige suvand M0007.</span><span class="sxs-lookup"><span data-stu-id="77fa4-122">Select M0007.</span></span>  
8. <span data-ttu-id="77fa4-123">Laiendage jaotist Sündmused.</span><span class="sxs-lookup"><span data-stu-id="77fa4-123">Expand the Events section.</span></span>
9. <span data-ttu-id="77fa4-124">Valige väljalt Varude täiendamise sündmus väärtus Partii.</span><span class="sxs-lookup"><span data-stu-id="77fa4-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="77fa4-125">See loob kanbanid materjalivajaduste rahuldamiseks seotud asukohas sidumissündmuse töötlemise ajal.</span><span class="sxs-lookup"><span data-stu-id="77fa4-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="77fa4-126">Määrake kauba miinimumkogus</span><span class="sxs-lookup"><span data-stu-id="77fa4-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="77fa4-127">Klõpsake, et järgida linki väljal Toode.</span><span class="sxs-lookup"><span data-stu-id="77fa4-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="77fa4-128">Klõpsake, et järgida linki väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="77fa4-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="77fa4-129">Laiendage toote pildi kiirinfot.</span><span class="sxs-lookup"><span data-stu-id="77fa4-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="77fa4-130">Klõpsake toimingupaanil valikut Plaan.</span><span class="sxs-lookup"><span data-stu-id="77fa4-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="77fa4-131">Klõpsake valikut Kauba laovarud.</span><span class="sxs-lookup"><span data-stu-id="77fa4-131">Click Item coverage.</span></span>
6. <span data-ttu-id="77fa4-132">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="77fa4-132">Click New.</span></span>
7. <span data-ttu-id="77fa4-133">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="77fa4-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="77fa4-134">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="77fa4-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="77fa4-135">Valige välja Ladu väärtuseks 12.</span><span class="sxs-lookup"><span data-stu-id="77fa4-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="77fa4-136">Määra valiku Miinimum väärtuseks 200.</span><span class="sxs-lookup"><span data-stu-id="77fa4-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="77fa4-137">Käivitage pakettsündmuse loomise töö</span><span class="sxs-lookup"><span data-stu-id="77fa4-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="77fa4-138">Avage Tootmise juhtimine > Perioodilised ülesanded > Kanban-töö pakktöötlus > Sidumissündmuse töötlemine.</span><span class="sxs-lookup"><span data-stu-id="77fa4-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="77fa4-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="77fa4-139">Click OK.</span></span>
3. <span data-ttu-id="77fa4-140">Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="77fa4-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="77fa4-141">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="77fa4-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="77fa4-142">Valige varem loodud kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="77fa4-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="77fa4-143">Laiendage jaotist Kanbanid.</span><span class="sxs-lookup"><span data-stu-id="77fa4-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="77fa4-144">Pange tähele, et kanban loodi vajaliku materjali üleviimiseks lattu 12.</span><span class="sxs-lookup"><span data-stu-id="77fa4-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]