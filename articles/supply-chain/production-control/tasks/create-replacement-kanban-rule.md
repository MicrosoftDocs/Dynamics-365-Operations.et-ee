---
title: Asenduskanban-reegli loomine
description: See protseduur keskendub olemasoleva kanban-reegli kindlal kuupäeval uue kanban-reegliga asendamisele.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6d507418965f0ebcd657ef6363ec206eb73a722f
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146947"
---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="2f0a6-103">Asenduskanban-reegli loomine</span><span class="sxs-lookup"><span data-stu-id="2f0a6-103">Create a replacement kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2f0a6-104">See protseduur keskendub olemasoleva kanban-reegli kindlal kuupäeval uue kanban-reegliga asendamisele.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="2f0a6-105">See on kasulik juhul, kui muudatused tootmisvoos või täiendamise reeglites peavad olema koordineeritud ja ajastatud.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="2f0a6-106">Protseduuri loomiseks kasutati demoettevõtte USMF andmeid</span><span class="sxs-lookup"><span data-stu-id="2f0a6-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="2f0a6-107">Protseduur on mõeldud protsessiinsenerile või väärtuse voo haldurile, kui ta valmistab ette tootmist muudetud tootmisvoo või uue täiendusreegli puhul.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="2f0a6-108">See toiming asendab kanban-reegli 000022 uue reegliga ja suurendab uue reegli puhul maksimaalset kogust 48-t 100-le.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="2f0a6-109">Asendatava kanban-reegli valimine</span><span class="sxs-lookup"><span data-stu-id="2f0a6-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="2f0a6-110">Minge jaotisse Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="2f0a6-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2f0a6-112">Valige kanban-reegel 000022.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="2f0a6-113">Asenduskanban-reegli loomine</span><span class="sxs-lookup"><span data-stu-id="2f0a6-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="2f0a6-114">Klõpsake suvandit Kanban-reegli asendamine.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="2f0a6-115">Sisestage kuupäev ja kellaaeg väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="2f0a6-116">Valige kuupäev tulevikus, näiteks üks nädal alates tänasest.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="2f0a6-117">See on kuupäev ja kellaaeg, millal uus kanban-reegel muutub aktiivseks ja asendab vana kanban-reegli.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="2f0a6-118">Kui kanban-reegel muudab tootmisvoo teed, saab valida muu tegevuse.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="2f0a6-119">Selles protseduuris jätame tegevuse samaks.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="2f0a6-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-120">Click OK.</span></span>
    * <span data-ttu-id="2f0a6-121">Pange tähele, et luuakse uus kanban-reegel, mis asendab kanban-reeglit 000022.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="2f0a6-122">Jõustumise kuupäev määratakse vastavalt kuupäevale, mille valisite kanban-reegli asendamisel.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="2f0a6-123">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2f0a6-124">Valige asendatud kanban-reegel 000022.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="2f0a6-125">Pange tähele, et asendatud kanban-reeglil on sama kuupäev mis aegumiskuupäev, sest see on kuupäev, millal see aegub.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="2f0a6-126">Valige loendist rida 1.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="2f0a6-127">Valige loendi ülaosas uus kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="2f0a6-128">See on suurima kanban-reegli numbriga kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="2f0a6-129">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2f0a6-130">Klõpsake kanban-reegli numbrit, et avada kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="2f0a6-131">Asendus-kanban-reegli maksimaalse koguse muutmine</span><span class="sxs-lookup"><span data-stu-id="2f0a6-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="2f0a6-132">Määrake maksimaalse koguse väärtuseks 100.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="2f0a6-133">Laiendage kiirkaarti Kogused, et näha välja Maksimaalne kogus.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="2f0a6-134">Maksimaalse koguse muutmine väärtusele 100 võimaldab töödelda kuni 100 kanbani.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="2f0a6-135">See on selle ülesande viimane etapp.</span><span class="sxs-lookup"><span data-stu-id="2f0a6-135">This is the last step in this task.</span></span>  

