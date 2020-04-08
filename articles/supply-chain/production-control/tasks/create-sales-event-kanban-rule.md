---
title: Müügisündmuse kanban-reegli loomine
description: See protseduur keskendub müügitellimuse loomise ajal käivitatava kanban-reegli loomiseks vajalikule seadistusele.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e17778d0fb05a1a5f7562027dc4e7f037e95e555
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149155"
---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="8163b-103">Müügisündmuse kanban-reegli loomine</span><span class="sxs-lookup"><span data-stu-id="8163b-103">Create a sales event kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8163b-104">See protseduur keskendub müügitellimuse loomise ajal käivitatava kanban-reegli loomiseks vajalikule seadistusele.</span><span class="sxs-lookup"><span data-stu-id="8163b-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="8163b-105">Sündmuse kanban-reegel täiendab müügitellimuse ridadelt pärinevaid nõudeid.</span><span class="sxs-lookup"><span data-stu-id="8163b-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="8163b-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="8163b-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8163b-107">See on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud toote tootmist.</span><span class="sxs-lookup"><span data-stu-id="8163b-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="8163b-108">Looge uus kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="8163b-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="8163b-109">Minge jaotisse Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="8163b-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="8163b-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="8163b-110">Click New.</span></span>
3. <span data-ttu-id="8163b-111">Valige väljal Täiendusstrateegia suvand Sündmus.</span><span class="sxs-lookup"><span data-stu-id="8163b-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="8163b-112">Suvandi Sündmus valimine tähendab, et kanban-reegli käivitab sündmus, näiteks müügitellimuse rea loomine.</span><span class="sxs-lookup"><span data-stu-id="8163b-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="8163b-113">Seda rakendatakse aladele, kus iga kanban peaks hõlmama kindlat nõudlust.</span><span class="sxs-lookup"><span data-stu-id="8163b-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="8163b-114">Sisestage või valige väärtus väljal Esimene plaanitegevus.</span><span class="sxs-lookup"><span data-stu-id="8163b-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="8163b-115">Valige suvand Lõplik assembler.</span><span class="sxs-lookup"><span data-stu-id="8163b-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="8163b-116">Laiendage jaotist Üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="8163b-116">Expand the Details section.</span></span>
6. <span data-ttu-id="8163b-117">Sisestage või valige väärtus väljal Toode.</span><span class="sxs-lookup"><span data-stu-id="8163b-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="8163b-118">Valige suvand L0050.</span><span class="sxs-lookup"><span data-stu-id="8163b-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="8163b-119">Sündmuse määratlemine</span><span class="sxs-lookup"><span data-stu-id="8163b-119">Define an event</span></span>
1. <span data-ttu-id="8163b-120">Laiendage jaotist Sündmused.</span><span class="sxs-lookup"><span data-stu-id="8163b-120">Expand the Events section.</span></span>
2. <span data-ttu-id="8163b-121">Valige väljal Müügisündmus suvand Automaatne.</span><span class="sxs-lookup"><span data-stu-id="8163b-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="8163b-122">Kui valite müügisündmuse sätteks Automaatne, käivitatakse see kanban-reegel automaatselt, kui müügirida ühtib toote ja vastuvõtukohaga.</span><span class="sxs-lookup"><span data-stu-id="8163b-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="8163b-123">Selle protseduuris on see toode L0050 laos 13.</span><span class="sxs-lookup"><span data-stu-id="8163b-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="8163b-124">Valige välja Sündmuste miinimumkogus väärtuseks 50.</span><span class="sxs-lookup"><span data-stu-id="8163b-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="8163b-125">Kui sündmuse miinimumkogus on 50, käivitatakse kanban-reegel ainult sündmustega, mille kogus on vähemalt 50.</span><span class="sxs-lookup"><span data-stu-id="8163b-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="8163b-126">Laiendage jaotist Tootmisvoog.</span><span class="sxs-lookup"><span data-stu-id="8163b-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="8163b-127">Pange tähele, et vastuvõtukoht on ladu 13.</span><span class="sxs-lookup"><span data-stu-id="8163b-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="8163b-128">See tähendab, et see kanban-reegel käivitatakse selle asukoha puhul.</span><span class="sxs-lookup"><span data-stu-id="8163b-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="8163b-129">Selles näites käivitab selle kanban-reegli müügirida tootele L0050, mille kogus on vähemalt 50, laos 13.</span><span class="sxs-lookup"><span data-stu-id="8163b-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="8163b-130">Müügirea loomine sündmuse kanban-reegli loomiseks</span><span class="sxs-lookup"><span data-stu-id="8163b-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="8163b-131">Avage Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="8163b-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="8163b-132">Kanban-reegli salvestamisel kuvatakse hoiatus, mis tähendab, et kanbanid luuakse müügitellimuse loomisel reaalajas.</span><span class="sxs-lookup"><span data-stu-id="8163b-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="8163b-133">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="8163b-133">Click New.</span></span>
3. <span data-ttu-id="8163b-134">Valige või sisestage väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="8163b-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="8163b-135">Valige näiteks US-003.</span><span class="sxs-lookup"><span data-stu-id="8163b-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="8163b-136">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="8163b-136">Click OK.</span></span>
5. <span data-ttu-id="8163b-137">Sisestage väljale Kaubakood tüüp L0050.</span><span class="sxs-lookup"><span data-stu-id="8163b-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="8163b-138">Sisestage väljale Tegevuskoht väärtus 1.</span><span class="sxs-lookup"><span data-stu-id="8163b-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="8163b-139">Valige tegevuskoht 1, kuna ladu 13 asub tegevuskohas 1.</span><span class="sxs-lookup"><span data-stu-id="8163b-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="8163b-140">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="8163b-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="8163b-141">Valige välja Ladu väärtuseks 13.</span><span class="sxs-lookup"><span data-stu-id="8163b-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="8163b-142">Määrake koguse väärtuseks 75.</span><span class="sxs-lookup"><span data-stu-id="8163b-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="8163b-143">Loodud kanban-reegli käivitamiseks sisestage koguseks vähemalt 50.</span><span class="sxs-lookup"><span data-stu-id="8163b-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="8163b-144">Kontrollimine, kas kanban on loodud</span><span class="sxs-lookup"><span data-stu-id="8163b-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="8163b-145">Klõpsake valikut Toode ja tarnimine.</span><span class="sxs-lookup"><span data-stu-id="8163b-145">Click Product and supply.</span></span>
2. <span data-ttu-id="8163b-146">Klõpsake suvandit Kuva sidumispuu.</span><span class="sxs-lookup"><span data-stu-id="8163b-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="8163b-147">Pange tähele, et luuakse kanban, mille kogus on sama mis müügireal.</span><span class="sxs-lookup"><span data-stu-id="8163b-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="8163b-148">Samuti näete toote L0050 tootmiseks vajalikke materjaliväljastusi.</span><span class="sxs-lookup"><span data-stu-id="8163b-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="8163b-149">See on selle protseduuri viimane etapp.</span><span class="sxs-lookup"><span data-stu-id="8163b-149">This is the last step in this procedure.</span></span>  

