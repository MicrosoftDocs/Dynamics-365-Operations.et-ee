---
title: Eelarve plaanimise andmete eraldamine
description: Selles artiklis kirjeldatakse erinevaid Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis saadaolevaid eraldamismeetodeid ja kuidas neid kasutada.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: fd7ec30c8253f343b3d41d54c78696cd512b2ef7
ms.contentlocale: et-ee
ms.lasthandoff: 06/29/2017


---

# <a name="budget-planning-data-allocation"></a><span data-ttu-id="81163-103">Eelarve plaanimise andmete eraldamine</span><span class="sxs-lookup"><span data-stu-id="81163-103">Budget planning data allocation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="81163-104">Selles artiklis kirjeldatakse erinevaid Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis saadaolevaid eraldamismeetodeid ja kuidas neid kasutada.</span><span class="sxs-lookup"><span data-stu-id="81163-104">This article describes the various allocation methods that are available in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and how they can be used.</span></span>  

<span data-ttu-id="81163-105">Saate prognoositud summade täpseks kujutamiseks eelarveplaani andmeid jaotada mitmel viisil.</span><span class="sxs-lookup"><span data-stu-id="81163-105">You can distribute the data in a budget plan in a number of ways to accurately portray the projected amounts.</span></span>

## <a name="allocation-methods"></a><span data-ttu-id="81163-106">Eraldamismeetodid</span><span class="sxs-lookup"><span data-stu-id="81163-106">Allocation methods</span></span>
<span data-ttu-id="81163-107">Kolm eraldamismeetodit (Eralda perioodide lõikes, Eralda dimensioonidele ja Kasuta pearaamatu eraldamisreegleid) saavad luua eelarveplaani read, mis põhinevad sama eelarveplaani ridadel.</span><span class="sxs-lookup"><span data-stu-id="81163-107">Three allocation methods (Allocate across periods, Allocate to dimensions, and Use ledger allocation rules) can create budget plan lines that are based on lines in the same budget plan.</span></span> <span data-ttu-id="81163-108">Kolm teist meetodit (Koonda, Jaota ja Kopeeri eelarveplaanist) saavad luua eelarveplaani read muudest eelarveplaanidest.</span><span class="sxs-lookup"><span data-stu-id="81163-108">Three other methods (Aggregate, Distribute, and Copy from budget plan) can create budget plan lines in other budget plans.</span></span> <span data-ttu-id="81163-109">Kõigi kuue eraldamismeetodi puhul määrate teie sihtstsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="81163-109">For all six allocation methods, you specify the destination scenario.</span></span> <span data-ttu-id="81163-110">Sihtstsenaarium võib olla lähtestsenaariumiga sama või sellest erineda.</span><span class="sxs-lookup"><span data-stu-id="81163-110">The destination scenario can be either the same as the source scenario or different from the source scenario.</span></span> <span data-ttu-id="81163-111">Lisaks saate määrata, kas uued read lisatakse eelarveplaani või asendavad eelarveplaani praegused read.</span><span class="sxs-lookup"><span data-stu-id="81163-111">Additionally, you can specify whether new lines are appended to the budget plan or replace the current lines in the budget plan.</span></span>

<span data-ttu-id="81163-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Eralda perioodide lõikes** – perioodi eraldamiskategooriat kasutatakse eelarveplaani ridade eraldamiseks algsest eelarveplaani stsenaariumist sihtstsenaariumi perioodide lõikes.</span><span class="sxs-lookup"><span data-stu-id="81163-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Allocate across periods** – A period allocation category is used to allocate the budget plan lines from the source budget plan scenario across periods in the destination scenario.</span></span> <span data-ttu-id="81163-113">Algsumma määratakse sihtstsenaariumis mitmele reale perioodi eraldamiskategoorias määratletud protsendi ja kuupäeva põhjal.</span><span class="sxs-lookup"><span data-stu-id="81163-113">The source amount is assigned to multiple lines in the destination scenario, based on the percentage and date that are defined in the period allocation category.</span></span>         

<span data-ttu-id="81163-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Eralda dimensioonidele** – eelarveplaani read eraldatakse algsest eelarve plaanimise stsenaariumist sihtstsenaariumi ühele või enamale reale valitud eelarve eraldustingimuses määratletud protsentide ja finantsdimensioonide põhjal.</span><span class="sxs-lookup"><span data-stu-id="81163-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Allocate to dimensions** – The budget plan lines are allocated from the source budget planning scenario to one or more lines in the destination scenario, based on the percentages and financial dimensions that are defined in a selected budget allocation term.</span></span>           

<span data-ttu-id="81163-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Koonda** – eelarveplaani read koondatakse seostatud (tütar-) eelarveplaanide algsest eelarveplaani stsenaariumist eelarve emaplaani sihtstsenaariumisse.</span><span class="sxs-lookup"><span data-stu-id="81163-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Aggregate** – The budget plan lines are aggregated from the source budget plan scenario in the associated (child) budget plans to the destination scenario in the parent budget plan.</span></span> <span data-ttu-id="81163-116">See meetod võimaldab eelarvesummad, mis valmistatakse ette organisatsiooni madalamal tasemel kõrgemal tasemel konsolideerimiseks.</span><span class="sxs-lookup"><span data-stu-id="81163-116">This method enables budget amounts that are prepared at a lower level in the organization to be consolidated at a higher level.</span></span>          

<span data-ttu-id="81163-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Jaota** – eelarveplaani read jaotatakse eelarve emaplaani algsest eelarve plaanimise stsenaariumist seostatud (tütar-) eelarveplaanide sihtstsenaariumisse seotud plaanide organisatsiooniüksuste finantsdimensioonide põhjal.</span><span class="sxs-lookup"><span data-stu-id="81163-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Distribute** – The budget plan lines are distributed from the source budget planning scenario in the parent budget plan to the destination scenario in the associated (child) budget plans, based on the financial dimensions of the organization units of the associated plans.</span></span> <span data-ttu-id="81163-118">See meetod võimaldab eelarvesummad, mis valmistatakse ette organisatsiooni kõrgemal tasemel veelgi lokaliseeritumaks ülevaatamiseks levitamiseks.</span><span class="sxs-lookup"><span data-stu-id="81163-118">This method enables budget amounts that are prepared at a higher level in the organization to be spread out for more localized review.</span></span>           

<span data-ttu-id="81163-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Kasuta pearaamatu eraldamisreegleid** – eelarveplaani read jaotatakse algse eelarve plaanimise stsenaariumist sihtstsenaariumisse valitud pearaamatu eraldamisreegli põhjal.</span><span class="sxs-lookup"><span data-stu-id="81163-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Use ledger allocation rules** – The budget plan lines are distributed from the source budget planning scenario to the destination scenario, based on the ledger allocation rule that is selected.</span></span> 

<span data-ttu-id="81163-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopeeri eelarveplaanist** – nagu eraldamismeetodi jaotamise puhul, luuakse eelarveplaani read sihtkohas seotud eelarveplaani ridade põhjal.</span><span class="sxs-lookup"><span data-stu-id="81163-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Copy from budget plan** – As in the Distribute allocation method, budget plan lines are created in the destination, based on lines in a related budget plan.</span></span> <span data-ttu-id="81163-121">Selle meetodi puhul ei pea algne eelarveplaan olema emaplaan, vaid võib olla eelarveplaani hierarhias mis tahes kõrgemal tasemel.</span><span class="sxs-lookup"><span data-stu-id="81163-121">However, for this method, the source budget plan doesn't have to be the parent but can be at any higher level in the budget plan hierarchy.</span></span> <span data-ttu-id="81163-122">See eraldamismeetod on kasulik, kui konsolideeritud summasid eelarvestatakse algselt palju kõrgemal tasemel ning tuleb enne kõrgema taseme kinnituse saamist viia üksikasjalikuks läbivaatamiseks ja korrigeerimiseks organisatsiooni madalamale tasemele.</span><span class="sxs-lookup"><span data-stu-id="81163-122">This allocation method is useful if consolidated amounts are originally budgeted at a much higher level, and must be transferred to a lower level of the organization for detailed review and adjustment before they can receive upper-level approval.</span></span>          

## <a name="using-allocation-methods-in-a-budget-plan"></a><span data-ttu-id="81163-123">Eraldamismeetodite kasutamine eelarveplaanis</span><span class="sxs-lookup"><span data-stu-id="81163-123">Using allocation methods in a budget plan</span></span>
<span data-ttu-id="81163-124">Eelarveplaani lehel eraldamiseks valige eraldatavad read ja seejärel klõpsake suvandit **Eralda eelarve**.</span><span class="sxs-lookup"><span data-stu-id="81163-124">To perform allocations on the budget plan page, select the lines to allocate, and then click **Allocate budget**.</span></span>

<span data-ttu-id="81163-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span><span class="sxs-lookup"><span data-stu-id="81163-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span></span> 

<span data-ttu-id="81163-126">Seejärel valige eraldamismeetod.</span><span class="sxs-lookup"><span data-stu-id="81163-126">Next, select an allocation method.</span></span> <span data-ttu-id="81163-127">Seejärel määratakse ülejäänud väljad teie valitud meetodi alusel.</span><span class="sxs-lookup"><span data-stu-id="81163-127">The remaining fields are then set, based on the method that you selected.</span></span> <span data-ttu-id="81163-128">Need väljad hõlmavad eelarveplaani andmete allikat ja sihtkohta ning suvandit, mis võimaldab teil korrutada allika määratud teguriga hulgikorrigeerimise lihtsustamiseks sihtsummade loomisel.</span><span class="sxs-lookup"><span data-stu-id="81163-128">These fields include the source and destination of the budget plan data, and an option that lets you multiply the source by a specified factor when the destination amounts are created, to simplify bulk adjustment.</span></span> <span data-ttu-id="81163-129">Saate määrata ka suvandi **Lisa plaani**.</span><span class="sxs-lookup"><span data-stu-id="81163-129">You can also set the **Append to plan** option.</span></span> <span data-ttu-id="81163-130">Valige olemasoleva eelarveplaani ridade asendamiseks **Ei** või valige **Jah** olemasoleva eelarveplaani ridade säilitamiseks ja uute ridade lisamiseks eraldatud summade puhul.</span><span class="sxs-lookup"><span data-stu-id="81163-130">Select **No** to replace the existing budget plan lines, or select **Yes** to retain the existing budget plan lines and add new lines for the allocated amounts.</span></span>

## <a name="automating-allocations-during-a-workflow"></a><span data-ttu-id="81163-131">Eraldamiste automatiseerimine töövoos</span><span class="sxs-lookup"><span data-stu-id="81163-131">Automating allocations during a workflow</span></span>
<span data-ttu-id="81163-132">Üks võimas funktsioon lubab eelarve plaanimise töövoo osana eraldada automaatselt.</span><span class="sxs-lookup"><span data-stu-id="81163-132">One powerful feature enables allocations to be performed automatically as part of a budget planning workflow.</span></span> <span data-ttu-id="81163-133">Eelarveplaani liikumisel läbi selle töövoo saavad automatiseeritud ülesanded tugineda eraldamisele määratud eelarve plaanimise etapis.</span><span class="sxs-lookup"><span data-stu-id="81163-133">As a budget plan moves through its workflow, automated tasks can invoke an allocation at a specified budget planning stage.</span></span> 

<span data-ttu-id="81163-134">Automaatse eraldamise seadistamiseks peate esmalt looma eraldamisgraafiku lehel **Eelarve plaanimise konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="81163-134">To set up automated allocation, you must first create an allocation schedule on the **Budget planning configuration** page.</span></span> <span data-ttu-id="81163-135">Eraldamisgraafik määratleb automaatse eraldamise käitamisel kasutatava eraldamismeetodi ja eri eraldamissuvandite väärtused (vt kirjeldusi eelmistest jaotistest).</span><span class="sxs-lookup"><span data-stu-id="81163-135">The allocation schedule defines the allocation method that will be used when the automated allocation is run, and the values of the various allocation options (see the previous section for descriptions).</span></span> 

<span data-ttu-id="81163-136">Seejärel loote etapi eraldamise lehel **Eelarve plaanimise konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="81163-136">Next, you create a stage allocation on the **Budget planning configuration** page.</span></span> <span data-ttu-id="81163-137">Etapi eraldamine määrab eraldamisgraafiku eelarve plaanimise töövoogu ja etappi.</span><span class="sxs-lookup"><span data-stu-id="81163-137">The stage allocation assigns an allocation schedule to the budget planning workflow and stage.</span></span> 

<span data-ttu-id="81163-138">Lõpuks lisate eelarve plaanimise etapi eraldamise automatiseeritud ülesande soovitud töövooetapis.</span><span class="sxs-lookup"><span data-stu-id="81163-138">Finally, add an automated task for budget planning stage allocation at the desired workflow stage.</span></span> <span data-ttu-id="81163-139">Järgmises näites on töövoogu lisatud kaks eelarve plaanimise etapi eraldamist (punasega esile tõstetud).</span><span class="sxs-lookup"><span data-stu-id="81163-139">In the following example, two budget planning stage allocations (outlined in red) have been inserted into the workflow.</span></span>

<span data-ttu-id="81163-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span><span class="sxs-lookup"><span data-stu-id="81163-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span></span>




