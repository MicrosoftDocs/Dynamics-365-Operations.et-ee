---
title: "Projekti kulukategooriate sünkroonimine Project Service Automationist"
description: "See teema kirjeldab malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti kulukategooriate sünkroonimiseks rakenduste Microsoft Dynamics 365 for Finance and Operations ning Dynamics 365 for Project Service Automation vahel."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: et-ee
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="fe7e0-103">Projekti kulukategooriate sünkroonimine Finance and Operationsi ja Project Service Automationi vahel</span><span class="sxs-lookup"><span data-stu-id="fe7e0-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

<span data-ttu-id="fe7e0-104">See teema kirjeldab malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti kulukategooriate sünkroonimiseks rakenduste Microsoft Dynamics 365 for Finance and Operations ning Dynamics 365 for Project Service Automation vahel.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> <span data-ttu-id="fe7e0-105">Projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine on saadaval rakenduse Dynamics 365 for Finance and Operations versioonis 8.0.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="fe7e0-106">Andmevoog Project Service Automationi ja Finance and Operationsi puhul</span><span class="sxs-lookup"><span data-stu-id="fe7e0-106">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="fe7e0-107">Project Service Automationi ja Finance and Operationsi integreerimise lahendus kasutab andmete sünkroonimiseks Project Service Automationi ning Finance and Operationsi eksemplaride vahel andmeintegratsiooni funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-107">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="fe7e0-108">Andmeintegratsiooni funktsioonis saadaolevad integratsioonimallid võimaldavad andmevoogu projekti kulukannete kategooriate kohta Finance and Operationsi ja Project Service Automationi vahel.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-108">The integration templates that are available with the Data integration feature enables the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="fe7e0-109">Kui projekti kulukategooriad on loodud Finance and Operationsis, on integratsioonivoog esmalt Finance and Operationsist Project Service Automationisse ja seejärel värskendatakse projekti kulukategooriate integratsiooni ID-sid, sünkroonides need Project Service Automationist Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-109">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation, and then updating the project expense categories integration IDs by synchronizing from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="fe7e0-110">Kui projekti kulukategooriad on loodud Project Service Automationis, on integratsioonivoog esmalt Project Service Automationist Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-110">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="fe7e0-111">Enne Project Service Automationist sünkroonimist peavad projekti kategooriad olema juba Finance and Operationsis konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-111">The project categories must already be configured in Finance and Operations prior to the synchronization from Project Service Automation.</span></span> <span data-ttu-id="fe7e0-112">Seejärel sünkroonige Finance and Operationsist tagasi Project Service Automationisse ja siis uuesti Project Service Automationist Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-112">Then synchronize from Finance and Operations back to Project Service Automation and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="fe7e0-113">See tagab, et kategooriad on seotud ja duplikaate ei looda.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-113">This ensures the categories are linked and duplicates are not created.</span></span>

> [!NOTE]
> <span data-ttu-id="fe7e0-114">Tavaliselt luuakse projekti kulukategooriad Finance and Operationsis.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-114">Typically, the project expense categories will be mastered in Finance and Operations.</span></span> <span data-ttu-id="fe7e0-115">Muul juhul või kui teil on Project Service Automationis kulukategooriad juba loodud, peate esmalt sünkroonima, kasutades projekti kulukannete kategooriaid (Project Service Automationist Finance and Operationsisse), ja seejärel sünkroonima, kasutades projekti kulukannete kategooriaid (Project Service Automationist Finance and Operationsisse).</span><span class="sxs-lookup"><span data-stu-id="fe7e0-115">If that is not your situation, or you already have expense categories created in Project Service Automation, you must first sync using the Project expense transaction categories (PSA to Fin and Ops) and then sync using Project expense transaction categories (Fin and Ops to PSA).</span></span> <span data-ttu-id="fe7e0-116">Seejärel peate sünkroonimise Project Service Automationist Finance and Operationsisse veel üks kord käivitama.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-116">You should then run the sync from PSA to Fin and Ops one more time.</span></span>

> <span data-ttu-id="fe7e0-117">Kui sünkroonite esmalt Project Service Automationist, peavad projekti kulukategooriad olema Finance and Operationsis juba seadistatud ja kõik kulukategooriad, mis tuleb Project Service Automationi kandekategooriatega sünkroonida, peavad olema seadistatud olekusse **Aktiivne töölehtedel**.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-117">If synchronizing first from Project Service Automation, the project categories must already be set up in Finance and Operations and any project categories that need to be synched with the Project Service Automation transaction categories must be set up to be **Active in journals**.</span></span>

<span data-ttu-id="fe7e0-118">Järgmine joonis näitab, kuidas sünkroonitakse andmeid Project Service Automationi ja Finance and Operationsi vahel.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-118">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="fe7e0-119">[![Andmevoog Project Service Automationi integreerimiseks Finance and Operationsiga](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="fe7e0-119">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="fe7e0-120">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="fe7e0-120">Templates and tasks</span></span>

<span data-ttu-id="fe7e0-121">Saadaolevatele mallidele juurdepääsuks valige Microsoft PowerAppsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-121">To access available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="fe7e0-122">Projekti kulukategooriate sünkroonimiseks Finance and Operationsist Project Service Automationisse kasutatakse järgmist malli ja aluseks olevat ülesannet.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-122">The following template and underlying task is used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="fe7e0-123">**Andmeintegratsioon malli nimi:** projekti kulukannete kategooriad (Finance and Operationsist Project Service Automationisse)</span><span class="sxs-lookup"><span data-stu-id="fe7e0-123">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
-  <span data-ttu-id="fe7e0-124">**Ülesande nimi projektis:** kategooriate sünkroonimine Project Service Automationisse</span><span class="sxs-lookup"><span data-stu-id="fe7e0-124">**Name of the task in the project:** Sync categories to PSA</span></span>

## <a name="entity-set"></a><span data-ttu-id="fe7e0-125">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="fe7e0-125">Entity set</span></span>

| <span data-ttu-id="fe7e0-126">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fe7e0-126">Finance and Operations</span></span>               | <span data-ttu-id="fe7e0-127">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="fe7e0-127">Project Service Automation</span></span>    |
|--------------------------------------|-------------------------------|
| <span data-ttu-id="fe7e0-128">Kategooriate integratsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="fe7e0-128">Integration entity for categories</span></span>    | <span data-ttu-id="fe7e0-129">Kandekategooriad</span><span class="sxs-lookup"><span data-stu-id="fe7e0-129">Transaction categories</span></span>        |

## <a name="entity-flow"></a><span data-ttu-id="fe7e0-130">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="fe7e0-130">Entity flow</span></span>

<span data-ttu-id="fe7e0-131">Projekti kulukategooriaid hallatakse Finance and Operationsis ja need sünkroonitakse Project Service Automationiga kandekategooriatena.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-131">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="fe7e0-132">Power Query</span><span class="sxs-lookup"><span data-stu-id="fe7e0-132">Power Query</span></span>

<span data-ttu-id="fe7e0-133">Peate kasutama Microsoft Power Queryt kandekategooriale arveldustüübi määramiseks Project Service Automationisse sünkroonimisel.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-133">You must use Microsoft Power Query to set the billing type on the transaction category when synchronizing to Project Service Automation.</span></span> <span data-ttu-id="fe7e0-134">Projekti kulukannete kategooriate (Finance and Operationsist Project Service Automationisse) mallile on vaikeveerg ja vastendus juba antud.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-134">The Project expense transaction categories (Fin and Ops to PSA) template has a default column and mapping already provided.</span></span> <span data-ttu-id="fe7e0-135">Kui loote oma malli, peate lisama selle tingimusveeru Power Querys.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-135">If you create your own template, you must add a conditional column in Power Query.</span></span>
- <span data-ttu-id="fe7e0-136">Avage projekti kulukategooriate ülesande vastenduses vorm Täpsem päring ja filtreerimine.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-136">Open the Advance Query and Filtering form from within the mapping of project expense categories task.</span></span>
- <span data-ttu-id="fe7e0-137">Valige suvand **Lisa tingimusveerg**.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-137">Select **Add Conditional Column**.</span></span>
- <span data-ttu-id="fe7e0-138">Andke uuele veerule nimi, nt BillingType.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-138">Give the new column a name, such as BillingType.</span></span>
- <span data-ttu-id="fe7e0-139">Sisestage järgmine tingimus: kui **CATEGORYID ei ole null, siis 19235001, muidu null**.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-139">Enter the following condition: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
- <span data-ttu-id="fe7e0-140">Klõpsake veerus **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-140">Click **OK** on the column.</span></span>
- <span data-ttu-id="fe7e0-141">Vastendage see uus veerg kindlasti vastenduslehel.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-141">Be sure to map this new column in the mapping page.</span></span>

<span data-ttu-id="fe7e0-142">Järgmisel joonisel on toodud näide malliülesande vastendusest andmeintegratsioonis.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-142">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="fe7e0-143">Vastendamine näitab välja teavet. mis sünkroonitakse Finance and Operationsist Project Service Automationisse.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-143">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="fe7e0-144">[![Malli vastendamine](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="fe7e0-144">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

<span data-ttu-id="fe7e0-145">Projekti kulukategooriate sünkroonimiseks Project Service Automationist Finance and Operationsisse kasutatakse järgmist malli ja aluseks olevat ülesannet.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-145">The following template and underlying task is used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="fe7e0-146">-**Andmeintegratsiooni malli nimi:** projekti kulukannete kategooriad (Project Service Automationist Finance and Operationsisse) -**Ülesande nimi projektis:** kategooriate sünkroonimine Finance and Operationsisse</span><span class="sxs-lookup"><span data-stu-id="fe7e0-146">-**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops) -**Name of the task in the project:** Sync categories to Fin Ops</span></span>

## <a name="entity-set"></a><span data-ttu-id="fe7e0-147">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="fe7e0-147">Entity set</span></span>

| <span data-ttu-id="fe7e0-148">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="fe7e0-148">Project Service Automation</span></span>      | <span data-ttu-id="fe7e0-149">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fe7e0-149">Finance and Operations</span></span>             |
|---------------------------------|------------------------------------|
| <span data-ttu-id="fe7e0-150">Kandekategooriad</span><span class="sxs-lookup"><span data-stu-id="fe7e0-150">Transaction categories</span></span>          | <span data-ttu-id="fe7e0-151">Kategooriate integratsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="fe7e0-151">Integration entity for categories</span></span>  | 

## <a name="entity-flow"></a><span data-ttu-id="fe7e0-152">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="fe7e0-152">Entity flow</span></span>

<span data-ttu-id="fe7e0-153">Projekti kulukategooriaid hallatakse Finance and Operationsis ja need sünkroonitakse Project Service Automationiga kandekategooriatena.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-153">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="fe7e0-154">Tagasi Finance and Operationsisse sünkroonimine värskendab integratsiooni ID Project Service Automationist Finance and Operationsi projektikategoorias.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-154">The synchronization back to Finance and Operations updates the integration ID from Project Service Automation on the Finance and Operations project category.</span></span>

<span data-ttu-id="fe7e0-155">Järgmisel joonisel on toodud näide malliülesande vastendusest andmeintegratsioonis.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-155">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="fe7e0-156">Vastendamine näitab välja teavet. mis sünkroonitakse Project Service Automationist Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="fe7e0-156">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="fe7e0-157">[![Malli vastendamine](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="fe7e0-157">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>

