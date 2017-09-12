--- 
title: Asenduskanban-reegli loomine
description: "See protseduur keskendub olemasoleva kanban-reegli kindlal kuupäeval uue kanban-reegliga asendamisele."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e5b27200a8d56192d473887f01076eced0f92e4c
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="71770-103">Asenduskanban-reegli loomine</span><span class="sxs-lookup"><span data-stu-id="71770-103">Create a replacement kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71770-104">See protseduur keskendub olemasoleva kanban-reegli kindlal kuupäeval uue kanban-reegliga asendamisele.</span><span class="sxs-lookup"><span data-stu-id="71770-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="71770-105">See on kasulik juhul, kui muudatused tootmisvoos või täiendamise reeglites peavad olema koordineeritud ja ajastatud.</span><span class="sxs-lookup"><span data-stu-id="71770-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="71770-106">Protseduuri loomiseks kasutati demoettevõtte USMF andmeid</span><span class="sxs-lookup"><span data-stu-id="71770-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="71770-107">Protseduur on mõeldud protsessiinsenerile või väärtuse voo haldurile, kui ta valmistab ette tootmist muudetud tootmisvoo või uue täiendusreegli puhul.</span><span class="sxs-lookup"><span data-stu-id="71770-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="71770-108">See toiming asendab kanban-reegli 000022 uue reegliga ja suurendab uue reegli puhul maksimaalset kogust 48-t 100-le.</span><span class="sxs-lookup"><span data-stu-id="71770-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="71770-109">Asendatava kanban-reegli valimine</span><span class="sxs-lookup"><span data-stu-id="71770-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="71770-110">Minge jaotisse Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="71770-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="71770-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="71770-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="71770-112">Valige kanban-reegel 000022.</span><span class="sxs-lookup"><span data-stu-id="71770-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="71770-113">Asenduskanban-reegli loomine</span><span class="sxs-lookup"><span data-stu-id="71770-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="71770-114">Klõpsake suvandit Kanban-reegli asendamine.</span><span class="sxs-lookup"><span data-stu-id="71770-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="71770-115">Sisestage kuupäev ja kellaaeg väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="71770-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="71770-116">Valige kuupäev tulevikus, näiteks üks nädal alates tänasest.</span><span class="sxs-lookup"><span data-stu-id="71770-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="71770-117">See on kuupäev ja kellaaeg, millal uus kanban-reegel muutub aktiivseks ja asendab vana kanban-reegli.</span><span class="sxs-lookup"><span data-stu-id="71770-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="71770-118">Kui kanban-reegel muudab tootmisvoo teed, saab valida muu tegevuse.</span><span class="sxs-lookup"><span data-stu-id="71770-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="71770-119">Selles protseduuris jätame tegevuse samaks.</span><span class="sxs-lookup"><span data-stu-id="71770-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="71770-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="71770-120">Click OK.</span></span>
    * <span data-ttu-id="71770-121">Pange tähele, et luuakse uus kanban-reegel, mis asendab kanban-reeglit 000022.</span><span class="sxs-lookup"><span data-stu-id="71770-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="71770-122">Jõustumise kuupäev määratakse vastavalt kuupäevale, mille valisite kanban-reegli asendamisel.</span><span class="sxs-lookup"><span data-stu-id="71770-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="71770-123">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="71770-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="71770-124">Valige asendatud kanban-reegel 000022.</span><span class="sxs-lookup"><span data-stu-id="71770-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="71770-125">Pange tähele, et asendatud kanban-reeglil on sama kuupäev mis aegumiskuupäev, sest see on kuupäev, millal see aegub.</span><span class="sxs-lookup"><span data-stu-id="71770-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="71770-126">Valige loendist rida 1.</span><span class="sxs-lookup"><span data-stu-id="71770-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="71770-127">Valige loendi ülaosas uus kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="71770-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="71770-128">See on suurima kanban-reegli numbriga kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="71770-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="71770-129">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="71770-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="71770-130">Klõpsake kanban-reegli numbrit, et avada kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="71770-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="71770-131">Asendus-kanban-reegli maksimaalse koguse muutmine</span><span class="sxs-lookup"><span data-stu-id="71770-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="71770-132">Määrake maksimaalse koguse väärtuseks 100.</span><span class="sxs-lookup"><span data-stu-id="71770-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="71770-133">Laiendage kiirkaarti Kogused, et näha välja Maksimaalne kogus.</span><span class="sxs-lookup"><span data-stu-id="71770-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="71770-134">Maksimaalse koguse muutmine väärtusele 100 võimaldab töödelda kuni 100 kanbani.</span><span class="sxs-lookup"><span data-stu-id="71770-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="71770-135">See on selle ülesande viimane etapp.</span><span class="sxs-lookup"><span data-stu-id="71770-135">This is the last step in this task.</span></span>  


