---
title: Müügisündmuse kanban-reegli loomine
description: See protseduur keskendub müügitellimuse loomise ajal käivitatava kanban-reegli loomiseks vajalikule seadistusele.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e33be986886d31c5275df3e36e2ce632f32c6f0d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228559"
---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="abf0c-103">Müügisündmuse kanban-reegli loomine</span><span class="sxs-lookup"><span data-stu-id="abf0c-103">Create a sales event kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="abf0c-104">See protseduur keskendub müügitellimuse loomise ajal käivitatava kanban-reegli loomiseks vajalikule seadistusele.</span><span class="sxs-lookup"><span data-stu-id="abf0c-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="abf0c-105">Sündmuse kanban-reegel täiendab müügitellimuse ridadelt pärinevaid nõudeid.</span><span class="sxs-lookup"><span data-stu-id="abf0c-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="abf0c-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="abf0c-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="abf0c-107">See on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud toote tootmist.</span><span class="sxs-lookup"><span data-stu-id="abf0c-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="abf0c-108">Looge uus kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="abf0c-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="abf0c-109">Minge jaotisse Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="abf0c-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="abf0c-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="abf0c-110">Click New.</span></span>
3. <span data-ttu-id="abf0c-111">Valige väljal Täiendusstrateegia suvand Sündmus.</span><span class="sxs-lookup"><span data-stu-id="abf0c-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="abf0c-112">Suvandi Sündmus valimine tähendab, et kanban-reegli käivitab sündmus, näiteks müügitellimuse rea loomine.</span><span class="sxs-lookup"><span data-stu-id="abf0c-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="abf0c-113">Seda rakendatakse aladele, kus iga kanban peaks hõlmama kindlat nõudlust.</span><span class="sxs-lookup"><span data-stu-id="abf0c-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="abf0c-114">Sisestage või valige väärtus väljal Esimene plaanitegevus.</span><span class="sxs-lookup"><span data-stu-id="abf0c-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="abf0c-115">Valige suvand Lõplik assembler.</span><span class="sxs-lookup"><span data-stu-id="abf0c-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="abf0c-116">Laiendage jaotist Üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="abf0c-116">Expand the Details section.</span></span>
6. <span data-ttu-id="abf0c-117">Sisestage või valige väärtus väljal Toode.</span><span class="sxs-lookup"><span data-stu-id="abf0c-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="abf0c-118">Valige suvand L0050.</span><span class="sxs-lookup"><span data-stu-id="abf0c-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="abf0c-119">Sündmuse määratlemine</span><span class="sxs-lookup"><span data-stu-id="abf0c-119">Define an event</span></span>
1. <span data-ttu-id="abf0c-120">Laiendage jaotist Sündmused.</span><span class="sxs-lookup"><span data-stu-id="abf0c-120">Expand the Events section.</span></span>
2. <span data-ttu-id="abf0c-121">Valige väljal Müügisündmus suvand Automaatne.</span><span class="sxs-lookup"><span data-stu-id="abf0c-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="abf0c-122">Kui valite müügisündmuse sätteks Automaatne, käivitatakse see kanban-reegel automaatselt, kui müügirida ühtib toote ja vastuvõtukohaga.</span><span class="sxs-lookup"><span data-stu-id="abf0c-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="abf0c-123">Selle protseduuris on see toode L0050 laos 13.</span><span class="sxs-lookup"><span data-stu-id="abf0c-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="abf0c-124">Valige välja Sündmuste miinimumkogus väärtuseks 50.</span><span class="sxs-lookup"><span data-stu-id="abf0c-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="abf0c-125">Kui sündmuse miinimumkogus on 50, käivitatakse kanban-reegel ainult sündmustega, mille kogus on vähemalt 50.</span><span class="sxs-lookup"><span data-stu-id="abf0c-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="abf0c-126">Laiendage jaotist Tootmisvoog.</span><span class="sxs-lookup"><span data-stu-id="abf0c-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="abf0c-127">Pange tähele, et vastuvõtukoht on ladu 13.</span><span class="sxs-lookup"><span data-stu-id="abf0c-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="abf0c-128">See tähendab, et see kanban-reegel käivitatakse selle asukoha puhul.</span><span class="sxs-lookup"><span data-stu-id="abf0c-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="abf0c-129">Selles näites käivitab selle kanban-reegli müügirida tootele L0050, mille kogus on vähemalt 50, laos 13.</span><span class="sxs-lookup"><span data-stu-id="abf0c-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="abf0c-130">Müügirea loomine sündmuse kanban-reegli loomiseks</span><span class="sxs-lookup"><span data-stu-id="abf0c-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="abf0c-131">Avage Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="abf0c-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="abf0c-132">Kanban-reegli salvestamisel kuvatakse hoiatus, mis tähendab, et kanbanid luuakse müügitellimuse loomisel reaalajas.</span><span class="sxs-lookup"><span data-stu-id="abf0c-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="abf0c-133">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="abf0c-133">Click New.</span></span>
3. <span data-ttu-id="abf0c-134">Valige või sisestage väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="abf0c-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="abf0c-135">Valige näiteks US-003.</span><span class="sxs-lookup"><span data-stu-id="abf0c-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="abf0c-136">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="abf0c-136">Click OK.</span></span>
5. <span data-ttu-id="abf0c-137">Sisestage väljale Kaubakood tüüp L0050.</span><span class="sxs-lookup"><span data-stu-id="abf0c-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="abf0c-138">Sisestage väljale Tegevuskoht väärtus 1.</span><span class="sxs-lookup"><span data-stu-id="abf0c-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="abf0c-139">Valige tegevuskoht 1, kuna ladu 13 asub tegevuskohas 1.</span><span class="sxs-lookup"><span data-stu-id="abf0c-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="abf0c-140">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="abf0c-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="abf0c-141">Valige välja Ladu väärtuseks 13.</span><span class="sxs-lookup"><span data-stu-id="abf0c-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="abf0c-142">Määrake koguse väärtuseks 75.</span><span class="sxs-lookup"><span data-stu-id="abf0c-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="abf0c-143">Loodud kanban-reegli käivitamiseks sisestage koguseks vähemalt 50.</span><span class="sxs-lookup"><span data-stu-id="abf0c-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="abf0c-144">Kontrollimine, kas kanban on loodud</span><span class="sxs-lookup"><span data-stu-id="abf0c-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="abf0c-145">Klõpsake valikut Toode ja tarnimine.</span><span class="sxs-lookup"><span data-stu-id="abf0c-145">Click Product and supply.</span></span>
2. <span data-ttu-id="abf0c-146">Klõpsake suvandit Kuva sidumispuu.</span><span class="sxs-lookup"><span data-stu-id="abf0c-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="abf0c-147">Pange tähele, et luuakse kanban, mille kogus on sama mis müügireal.</span><span class="sxs-lookup"><span data-stu-id="abf0c-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="abf0c-148">Samuti näete toote L0050 tootmiseks vajalikke materjaliväljastusi.</span><span class="sxs-lookup"><span data-stu-id="abf0c-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="abf0c-149">See on selle protseduuri viimane etapp.</span><span class="sxs-lookup"><span data-stu-id="abf0c-149">This is the last step in this procedure.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]