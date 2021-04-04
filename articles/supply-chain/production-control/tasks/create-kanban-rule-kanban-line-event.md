---
title: Kanban-rea sündmuse abil kanban-reegli loomine
description: See protseduur loob kanban-reegli, kasutades kanban-rea sündmuste seadistust protsessitegevusest tõmbamise käivitamiseks.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc838a64e74b561dd17fd2b568fa8c190a1dfcfe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255201"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a><span data-ttu-id="de17c-103">Kanban-rea sündmuse abil kanban-reegli loomine</span><span class="sxs-lookup"><span data-stu-id="de17c-103">Create a kanban rule using a kanban line event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="de17c-104">See protseduur loob kanban-reegli, kasutades kanban-rea sündmuste seadistust protsessitegevusest tõmbamise käivitamiseks.</span><span class="sxs-lookup"><span data-stu-id="de17c-104">This procedure creates a kanban rule by using the kanban line event setting to trigger pull from a process activity.</span></span> <span data-ttu-id="de17c-105">Kanban-reegli käivitab kanban-protsessi tegevus, mille kogus on kummagi puhul vähemalt 25.</span><span class="sxs-lookup"><span data-stu-id="de17c-105">The kanban rule is triggered by a kanban process activity, with a quantity equal to or greater than 25 each.</span></span> <span data-ttu-id="de17c-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="de17c-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="de17c-107">See toiming on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud toote tootmist säästlikus keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="de17c-107">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-kanban-rule"></a><span data-ttu-id="de17c-108">Kanban-reegli loomine</span><span class="sxs-lookup"><span data-stu-id="de17c-108">Create a kanban rule</span></span>
1. <span data-ttu-id="de17c-109">Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="de17c-109">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="de17c-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="de17c-110">Click New.</span></span>
3. <span data-ttu-id="de17c-111">Valige väljal Täiendusstrateegia suvand Sündmus.</span><span class="sxs-lookup"><span data-stu-id="de17c-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="de17c-112">See loob kanbanid otse nõudlusest.</span><span class="sxs-lookup"><span data-stu-id="de17c-112">This generates kanbans directly from demand.</span></span> <span data-ttu-id="de17c-113">Seda kasutatakse tellimuse järgi tegemise stsenaariumeid määratlevate reeglite seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="de17c-113">It is used to set up rules that define a make-to-order scenario.</span></span>  
4. <span data-ttu-id="de17c-114">Sisestage või valige väärtus väljal Esimene plaanitegevus.</span><span class="sxs-lookup"><span data-stu-id="de17c-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="de17c-115">Sisestage või valige SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="de17c-115">Enter or select SpeakerAssemblyAndPolish.</span></span> <span data-ttu-id="de17c-116">Tootmise kanban-reegli esimene tegevus on protsessitegevus tootmisvoos.</span><span class="sxs-lookup"><span data-stu-id="de17c-116">The first activity of a manufacturing kanban rule is a process activity in the production flow.</span></span> <span data-ttu-id="de17c-117">Tegevuse valimisel kopeeritakse selle kehtivuskuupäevade kanban-reegli kehtivuse kuupäevadele.</span><span class="sxs-lookup"><span data-stu-id="de17c-117">When you select the activity, the validity dates of the activity are copied to the validity dates of the kanban rule.</span></span>  
5. <span data-ttu-id="de17c-118">Laiendage jaotist Üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="de17c-118">Expand the Details section.</span></span>
6. <span data-ttu-id="de17c-119">Sisestage väljale Toode väärtus L0001.</span><span class="sxs-lookup"><span data-stu-id="de17c-119">In the Product field, type 'L0001'.</span></span>
7. <span data-ttu-id="de17c-120">Laiendage jaotist Sündmused.</span><span class="sxs-lookup"><span data-stu-id="de17c-120">Expand the Events section.</span></span>
8. <span data-ttu-id="de17c-121">Valige väljal Kanban-rea sündmus väärtus Automaatne.</span><span class="sxs-lookup"><span data-stu-id="de17c-121">In the Kanban line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="de17c-122">See loob nõudmisel sündmuse kanbanid.</span><span class="sxs-lookup"><span data-stu-id="de17c-122">This generates event kanbans on demand.</span></span>  <span data-ttu-id="de17c-123">Selle välja abil saate konfigureerida kanban-reeglid, mis täiendavad järgmiste protsessitegevuste jaoks vajalikku materjali.</span><span class="sxs-lookup"><span data-stu-id="de17c-123">The field is used to configure kanban rules that replenish material that is required for a downstream process activity.</span></span> <span data-ttu-id="de17c-124">Valiku Automaatne korral luuakse koos nõudlusega sündmuse kanbanid.</span><span class="sxs-lookup"><span data-stu-id="de17c-124">When you select Automatic, the event kanbans are created with the demand.</span></span> <span data-ttu-id="de17c-125">See säte on soovitatav kui plaanite viia tootmise läbi samal päeval.</span><span class="sxs-lookup"><span data-stu-id="de17c-125">This setting is recommended if you expect to execute production on the same day.</span></span>  
9. <span data-ttu-id="de17c-126">Valige välja Sündmuste miinimumkogus väärtuseks 25.</span><span class="sxs-lookup"><span data-stu-id="de17c-126">Set Minimum event quantity to '25'.</span></span>
    * <span data-ttu-id="de17c-127">Sündmuse kanbanid luuakse, kui nõudluse kogus on selle välja väärtusega võrdne või sellest suurem.</span><span class="sxs-lookup"><span data-stu-id="de17c-127">Event kanbans are generated when the demand quantity is equal to or more than this field.</span></span> <span data-ttu-id="de17c-128">Sellest on kasu, kui soovite toota ühel masinal sellest väljast väiksema tellimuse koguse ja teisel masinal sellest väljast suurema koguse.</span><span class="sxs-lookup"><span data-stu-id="de17c-128">This is useful if you want to produce an order quantity less than this field on one machine and more than this field on another machine.</span></span>  
10. <span data-ttu-id="de17c-129">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="de17c-129">Click Save.</span></span>

## <a name="create-sales-order-and-trigger-kanban-chain"></a><span data-ttu-id="de17c-130">Müügitellimuse loomine ja kanban-ahela käivitamine</span><span class="sxs-lookup"><span data-stu-id="de17c-130">Create sales order and trigger kanban chain</span></span>
1. <span data-ttu-id="de17c-131">Avage Müük ja turundus > Müügitellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="de17c-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="de17c-132">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="de17c-132">Click New.</span></span>
3. <span data-ttu-id="de17c-133">Valige või sisestage väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="de17c-133">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="de17c-134">Valige kliendikood US-003, metsa hulgimüük.</span><span class="sxs-lookup"><span data-stu-id="de17c-134">Select Customer account US-003, Forest Wholesales.</span></span>  
4. <span data-ttu-id="de17c-135">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="de17c-135">Click OK.</span></span>
5. <span data-ttu-id="de17c-136">Sisestage väljale Kaubakood tüüp L0001.</span><span class="sxs-lookup"><span data-stu-id="de17c-136">In the Item number field, type 'L0001'.</span></span>
    * <span data-ttu-id="de17c-137">L0001 on kaup, millele kanban-reegli lõite.</span><span class="sxs-lookup"><span data-stu-id="de17c-137">L0001 is the item for which you created the kanban rule.</span></span>  
6. <span data-ttu-id="de17c-138">Määrake koguse väärtuseks 27.</span><span class="sxs-lookup"><span data-stu-id="de17c-138">Set Quantity to '27'.</span></span>
    * <span data-ttu-id="de17c-139">Kuna 27 on suurem kui kanban-reegli miinimumkogus 25, käivitab see sündmuse kanbani.</span><span class="sxs-lookup"><span data-stu-id="de17c-139">Because 27 is higher than the minimum quantity of 25 on the kanban rule, this will trigger an event kanban.</span></span>  
7. <span data-ttu-id="de17c-140">Sisestage väljale Tegevuskoht väärtus 1.</span><span class="sxs-lookup"><span data-stu-id="de17c-140">In the Site field, type '1'.</span></span>
8. <span data-ttu-id="de17c-141">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="de17c-141">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="de17c-142">Valige ladu 13.</span><span class="sxs-lookup"><span data-stu-id="de17c-142">Select warehouse 13.</span></span>  
9. <span data-ttu-id="de17c-143">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="de17c-143">Click Save.</span></span>

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a><span data-ttu-id="de17c-144">Kanban-reegliga loodud kanbani kuvamine</span><span class="sxs-lookup"><span data-stu-id="de17c-144">View the kanban generated by the kanban rule</span></span>
1. <span data-ttu-id="de17c-145">Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="de17c-145">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="de17c-146">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="de17c-146">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="de17c-147">Laiendage jaotist Kanbanid.</span><span class="sxs-lookup"><span data-stu-id="de17c-147">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="de17c-148">Pange tähele, et 27 jaoks loodi kanban selleks, et töödelda loodud kanban-reeglil põhinevat tegevust.</span><span class="sxs-lookup"><span data-stu-id="de17c-148">Notice that a kanban for 27 was created to process the  activity based on the created kanban rule.</span></span>  
    * <span data-ttu-id="de17c-149">See on viimane etapp.</span><span class="sxs-lookup"><span data-stu-id="de17c-149">This is the last step.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]