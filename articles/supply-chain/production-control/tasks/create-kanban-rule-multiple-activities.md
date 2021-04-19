---
title: Mitme tegevuse kanban-reegli loomine
description: See protseduur näitab, kuidas luua kanban-reeglit, mis sisaldab tootmisvoost mitut tegevust.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 828b01fbb3b94b1fcb9fe8a565b1191a4f4bf630
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829110"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="4d5a2-103">Mitme tegevuse kanban-reegli loomine</span><span class="sxs-lookup"><span data-stu-id="4d5a2-103">Create a kanban rule for multiple activities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4d5a2-104">See protseduur näitab, kuidas luua kanban-reeglit, mis sisaldab tootmisvoost mitut tegevust.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="4d5a2-105">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="4d5a2-106">See toiming on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud toote tootmist säästlikus keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="4d5a2-107">Looge uus kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="4d5a2-108">Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="4d5a2-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-109">Click New.</span></span>
3. <span data-ttu-id="4d5a2-110">Valige väljalt Täiendusstrateegia väärtus Plaanitud.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="4d5a2-111">Sisestage või valige väärtus väljal Esimene plaanitegevus.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="4d5a2-112">Valige SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="4d5a2-113">Märkige ruut Mitu tegevust.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="4d5a2-114">Eesmärk on kaasata kanban-reeglisse mitu tegevust.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="4d5a2-115">Tootmisvoos valitakse tee viimase plaani tegevuse valimisel.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="4d5a2-116">Sisestage või valige väärtus väljal Viimane plaanitegevus.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="4d5a2-117">Valige SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="4d5a2-118">Pärast selle väärtuse valimist avaneb leht automaatselt.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="4d5a2-119">Valige kanban-voog SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="4d5a2-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-120">Click OK.</span></span>  
7. <span data-ttu-id="4d5a2-121">Laiendage jaotist Üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-121">Expand the Details section.</span></span>
8. <span data-ttu-id="4d5a2-122">Sisestage või valige väärtus väljal Toode.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="4d5a2-123">Valige kaup L0006.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="4d5a2-124">Kanbani loomine ja tööde vaatamine</span><span class="sxs-lookup"><span data-stu-id="4d5a2-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="4d5a2-125">Laiendage jaotist Kanbanid.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="4d5a2-126">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-126">Click Add.</span></span>
3. <span data-ttu-id="4d5a2-127">Sisestage väljale Uute kanbanide arv väärtus 1.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="4d5a2-128">See loob ühe kanbani.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="4d5a2-129">Määrake toote koguseks 3.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="4d5a2-130">Kanban töötleb 3 toodet.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="4d5a2-131">Sisestage kuupäev ja kellaaeg väljale Tähtaja kuupäev/kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="4d5a2-132">Võite sisestada väärtuse Täna.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-132">You can enter Today.</span></span>  
6. <span data-ttu-id="4d5a2-133">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-133">Click Create.</span></span>
7. <span data-ttu-id="4d5a2-134">Klõpsake käsku Details (Üksikasjad).</span><span class="sxs-lookup"><span data-stu-id="4d5a2-134">Click Details.</span></span>
    * <span data-ttu-id="4d5a2-135">Pange tähele, et kanbanil on tootmisvoost kaks protsessitööd.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="4d5a2-136">Esimene on SpeakerAssemblyAndPolish ja teine on SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="4d5a2-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="4d5a2-137">See on viimane etapp!</span><span class="sxs-lookup"><span data-stu-id="4d5a2-137">This is the last step!</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]