---
title: Mitme tegevuse kanban-reegli loomine
description: See protseduur näitab, kuidas luua kanban-reeglit, mis sisaldab tootmisvoost mitut tegevust.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68cac0f581e786cdb3801e03fb60db7bc05ffb2f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212211"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="3171a-103">Mitme tegevuse kanban-reegli loomine</span><span class="sxs-lookup"><span data-stu-id="3171a-103">Create a kanban rule for multiple activities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3171a-104">See protseduur näitab, kuidas luua kanban-reeglit, mis sisaldab tootmisvoost mitut tegevust.</span><span class="sxs-lookup"><span data-stu-id="3171a-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="3171a-105">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="3171a-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="3171a-106">See toiming on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud toote tootmist säästlikus keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="3171a-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="3171a-107">Looge uus kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="3171a-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="3171a-108">Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="3171a-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="3171a-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="3171a-109">Click New.</span></span>
3. <span data-ttu-id="3171a-110">Valige väljalt Täiendusstrateegia väärtus Plaanitud.</span><span class="sxs-lookup"><span data-stu-id="3171a-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="3171a-111">Sisestage või valige väärtus väljal Esimene plaanitegevus.</span><span class="sxs-lookup"><span data-stu-id="3171a-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="3171a-112">Valige SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="3171a-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="3171a-113">Märkige ruut Mitu tegevust.</span><span class="sxs-lookup"><span data-stu-id="3171a-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="3171a-114">Eesmärk on kaasata kanban-reeglisse mitu tegevust.</span><span class="sxs-lookup"><span data-stu-id="3171a-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="3171a-115">Tootmisvoos valitakse tee viimase plaani tegevuse valimisel.</span><span class="sxs-lookup"><span data-stu-id="3171a-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="3171a-116">Sisestage või valige väärtus väljal Viimane plaanitegevus.</span><span class="sxs-lookup"><span data-stu-id="3171a-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="3171a-117">Valige SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="3171a-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="3171a-118">Pärast selle väärtuse valimist avaneb leht automaatselt.</span><span class="sxs-lookup"><span data-stu-id="3171a-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="3171a-119">Valige kanban-voog SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="3171a-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="3171a-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3171a-120">Click OK.</span></span>  
7. <span data-ttu-id="3171a-121">Laiendage jaotist Üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="3171a-121">Expand the Details section.</span></span>
8. <span data-ttu-id="3171a-122">Sisestage või valige väärtus väljal Toode.</span><span class="sxs-lookup"><span data-stu-id="3171a-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="3171a-123">Valige kaup L0006.</span><span class="sxs-lookup"><span data-stu-id="3171a-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="3171a-124">Kanbani loomine ja tööde vaatamine</span><span class="sxs-lookup"><span data-stu-id="3171a-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="3171a-125">Laiendage jaotist Kanbanid.</span><span class="sxs-lookup"><span data-stu-id="3171a-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="3171a-126">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="3171a-126">Click Add.</span></span>
3. <span data-ttu-id="3171a-127">Sisestage väljale Uute kanbanide arv väärtus 1.</span><span class="sxs-lookup"><span data-stu-id="3171a-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="3171a-128">See loob ühe kanbani.</span><span class="sxs-lookup"><span data-stu-id="3171a-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="3171a-129">Määrake toote koguseks 3.</span><span class="sxs-lookup"><span data-stu-id="3171a-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="3171a-130">Kanban töötleb 3 toodet.</span><span class="sxs-lookup"><span data-stu-id="3171a-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="3171a-131">Sisestage kuupäev ja kellaaeg väljale Tähtaja kuupäev/kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="3171a-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="3171a-132">Võite sisestada väärtuse Täna.</span><span class="sxs-lookup"><span data-stu-id="3171a-132">You can enter Today.</span></span>  
6. <span data-ttu-id="3171a-133">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="3171a-133">Click Create.</span></span>
7. <span data-ttu-id="3171a-134">Klõpsake käsku Details (Üksikasjad).</span><span class="sxs-lookup"><span data-stu-id="3171a-134">Click Details.</span></span>
    * <span data-ttu-id="3171a-135">Pange tähele, et kanbanil on tootmisvoost kaks protsessitööd.</span><span class="sxs-lookup"><span data-stu-id="3171a-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="3171a-136">Esimene on SpeakerAssemblyAndPolish ja teine on SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="3171a-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="3171a-137">See on viimane etapp!</span><span class="sxs-lookup"><span data-stu-id="3171a-137">This is the last step!</span></span>  

