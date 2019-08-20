---
title: Projekti kulukategooriate sünkroonimine Finance and Operationsi ja Project Service Automationi vahel
description: Selles teemas kirjeldatakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti kulukategooriate sünkroonimiseks rakenduste Microsoft Dynamics 365 for Finance and Operations ja Microsoft Dynamics 365 for Project Service Automation vahel.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 90d640bb3eea909238b4ff032fcdb3854014e65e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838363"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="a30c2-103">Projekti kulukategooriate sünkroonimine Finance and Operationsi ja Project Service Automationi vahel</span><span class="sxs-lookup"><span data-stu-id="a30c2-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a30c2-104">Selles teemas kirjeldatakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti kulukategooriate sünkroonimiseks rakenduste Microsoft Dynamics 365 for Finance and Operations ja Microsoft Dynamics 365 for Project Service Automation vahel.</span><span class="sxs-lookup"><span data-stu-id="a30c2-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="a30c2-105">Projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine on saadaval rakenduse Microsoft Dynamics 365 for Finance and Operations versioonis 8.0.</span><span class="sxs-lookup"><span data-stu-id="a30c2-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="a30c2-106">Tegelike näitajate integratsioon on saadaval rakenduse Microsoft Dynamics 365 for Finance and Operations versioonis 8.0.1 või uuemas.</span><span class="sxs-lookup"><span data-stu-id="a30c2-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="a30c2-107">Kui kasutate rakendust Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, saate pärast KB 4132657 ja KB 4132660 installimist kasutada projektiülesannete, kulukannete kategooriate, tunnihinnangute, kuluhinnangute ja tegelike näitajate integreerimiseks ning funktsionaalsuse lukustamise konfigureerimiseks malle.</span><span class="sxs-lookup"><span data-stu-id="a30c2-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="a30c2-108">Kui peate lähtestama arvestuse jaotusi, soovitame installida KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="a30c2-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="a30c2-109">Andmevoog Project Service Automationi ja Finance and Operationsi puhul</span><span class="sxs-lookup"><span data-stu-id="a30c2-109">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="a30c2-110">Project Service Automationi ja Finance and Operationsi integreerimise lahendus kasutab andmete sünkroonimiseks Project Service Automationi ning Finance and Operationsi eksemplaride vahel andmeintegratsiooni funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="a30c2-110">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="a30c2-111">Andmeintegratsiooni funktsioonis saadaolevad integratsioonimallid võimaldavad andmevoogu projekti kulukannete kategooriate kohta Finance and Operationsi ja Project Service Automationi vahel.</span><span class="sxs-lookup"><span data-stu-id="a30c2-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="a30c2-112">Kui projekti kulukategooriad on loodud Finance and Operationsis, on integratsioonivoog esmalt Finance and Operationsist Project Service Automationisse.</span><span class="sxs-lookup"><span data-stu-id="a30c2-112">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation.</span></span> <span data-ttu-id="a30c2-113">Projekti kulukategooriate integratsiooni ID-d värskendatakse seejärel sünkroonimise kaudu Project Service Automationist Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="a30c2-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="a30c2-114">Kui projekti kulukategooriad on loodud Project Service Automationis, on integratsioonivoog esmalt Project Service Automationist Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="a30c2-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="a30c2-115">Enne Project Service Automationist sünkroonimist peavad projekti kategooriad olema juba Finance and Operationsis konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="a30c2-115">The project categories must already be configured in Finance and Operations before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="a30c2-116">Seejärel sünkroonige Finance and Operationsist tagasi Project Service Automationisse ja siis uuesti Project Service Automationist Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="a30c2-116">Then synchronize from Finance and Operations back to Project Service Automation, and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="a30c2-117">Sel viisil saate tagada, et kategooriad on seotud ja duplikaate ei looda.</span><span class="sxs-lookup"><span data-stu-id="a30c2-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="a30c2-118">Tavaliselt luuakse projekti kulukategooriad Finance and Operationsis.</span><span class="sxs-lookup"><span data-stu-id="a30c2-118">Typically, the project expense categories are mastered in Finance and Operations.</span></span> <span data-ttu-id="a30c2-119">Kui need aga ei ole loodud Finance and Operationsis või kui kulukategooriad on juba loodud Project Service Automationis, peate kõigepealt sünkroonima, kasutades projekti kulukannete kategooriate (Project Service Automationist Finance and Operationsisse) malli.</span><span class="sxs-lookup"><span data-stu-id="a30c2-119">However, if they aren't mastered in Finance and Operations, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="a30c2-120">Seejärel sünkroonige, kasutades projekti kulukannete kategooriate (Finance and Operationsist Project Service Automationisse) malli.</span><span class="sxs-lookup"><span data-stu-id="a30c2-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="a30c2-121">Pärast seda peaksite veel üks kord sünkroonima Project Service Automationist Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="a30c2-121">You should then run the synchronization from Project Service Automation to Finance and Operations one more time.</span></span>
>
> <span data-ttu-id="a30c2-122">Kui sünkroonite esmalt Project Service Automationist, peavad enne sünkroonimist olema Finance and Operationsis täidetud järgmised tingimused.</span><span class="sxs-lookup"><span data-stu-id="a30c2-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance and Operations before the synchronization is run:</span></span>
>
> - <span data-ttu-id="a30c2-123">Olemas peab olema ühiskasutuses kategooria, mis vastab Project Service Automationis üles seatud projekti kategooriale, ja see peab olem lubatud nii suvandi **Projekt** kui ka **Kulu** jaoks.</span><span class="sxs-lookup"><span data-stu-id="a30c2-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="a30c2-124">Iga integreeritava Finance and Operationsi juriidilise isiku puhul peavad olemas olema järgmised projekti kategooriad.</span><span class="sxs-lookup"><span data-stu-id="a30c2-124">For each Finance and Operations legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="a30c2-125">**Projekti kategooria** on olemas.</span><span class="sxs-lookup"><span data-stu-id="a30c2-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="a30c2-126">**Kasuta kuludes** on lubatud.</span><span class="sxs-lookup"><span data-stu-id="a30c2-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="a30c2-127">**Aktiivne töölehel** on lubatud.</span><span class="sxs-lookup"><span data-stu-id="a30c2-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="a30c2-128">**Kande tüüp** on määratud olekule **Kulu**.</span><span class="sxs-lookup"><span data-stu-id="a30c2-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="a30c2-129">Järgmine joonis näitab, kuidas sünkroonitakse andmeid Project Service Automationi ja Finance and Operationsi vahel.</span><span class="sxs-lookup"><span data-stu-id="a30c2-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="a30c2-130">[![Andmevoog Project Service Automationi integreerimiseks Finance and Operationsiga](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="a30c2-130">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a><span data-ttu-id="a30c2-131">Projekti kulukategooriate sünkroonimine Finance and Operationsist Project Service Automationisse</span><span class="sxs-lookup"><span data-stu-id="a30c2-131">Project expense category synchronization from Finance and Operations to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="a30c2-132">Mall ja ülesanne</span><span class="sxs-lookup"><span data-stu-id="a30c2-132">Template and task</span></span>

<span data-ttu-id="a30c2-133">Mallile juurdepääsuks valige Microsoft PowerAppsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="a30c2-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a30c2-134">Projekti kulukategooriate sünkroonimiseks Finance and Operationsist Project Service Automationisse kasutatakse järgmist malli ja aluseks olevat ülesannet.</span><span class="sxs-lookup"><span data-stu-id="a30c2-134">The following template and underlying task are used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

- <span data-ttu-id="a30c2-135">**Andmeintegratsioon malli nimi:** projekti kulukannete kategooriad (Finance and Operationsist Project Service Automationisse)</span><span class="sxs-lookup"><span data-stu-id="a30c2-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="a30c2-136">**Ülesande nimi projektis:** kategooriate sünkroonimine Project Service Automationisse</span><span class="sxs-lookup"><span data-stu-id="a30c2-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="a30c2-137">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="a30c2-137">Entity set</span></span>

| <span data-ttu-id="a30c2-138">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a30c2-138">Finance and Operations</span></span>            | <span data-ttu-id="a30c2-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a30c2-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="a30c2-140">Kategooriate integratsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="a30c2-140">Integration entity for categories</span></span> | <span data-ttu-id="a30c2-141">Kandekategooriad</span><span class="sxs-lookup"><span data-stu-id="a30c2-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="a30c2-142">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="a30c2-142">Entity flow</span></span>

<span data-ttu-id="a30c2-143">Projekti kulukategooriaid hallatakse Finance and Operationsis ja need sünkroonitakse Project Service Automationiga kandekategooriatena.</span><span class="sxs-lookup"><span data-stu-id="a30c2-143">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="a30c2-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="a30c2-144">Power Query</span></span>

<span data-ttu-id="a30c2-145">Project Service Automationisse sünkroonimisel peate kasutama Microsoft Power Queryt Exceli jaoks, et määrata kandekategooriale arveldustüüp.</span><span class="sxs-lookup"><span data-stu-id="a30c2-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="a30c2-146">Projekti kulukannete kategooriate (Finance and Operationsist Project Service Automationisse) mallil on olemas vaikeveerg ja vastendus.</span><span class="sxs-lookup"><span data-stu-id="a30c2-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="a30c2-147">Kui loote oma malli, peate lisama selle tingimusveeru Power Querys.</span><span class="sxs-lookup"><span data-stu-id="a30c2-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="a30c2-148">Tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a30c2-148">Follow these steps.</span></span>

1. <span data-ttu-id="a30c2-149">Klõpsake noolt, et avada projekti kulukannete kategooriate (Finance and Operationsist Project Service Automationisse)mallis projekti kulukannete kategooriate vastendamise ülesanne.</span><span class="sxs-lookup"><span data-stu-id="a30c2-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="a30c2-150">Klõpsake linki **Täpsem päring ja filtreerimine**, et avada Power Query.</span><span class="sxs-lookup"><span data-stu-id="a30c2-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="a30c2-151">Valige suvand **Lisa tingimusveerg**.</span><span class="sxs-lookup"><span data-stu-id="a30c2-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="a30c2-152">Andke uuele veerule nimi, nt **ArvelduseTüüp**.</span><span class="sxs-lookup"><span data-stu-id="a30c2-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="a30c2-153">Sisestage järgmine tingimus: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="a30c2-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="a30c2-154">Klõpsake veerus **OK**.</span><span class="sxs-lookup"><span data-stu-id="a30c2-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="a30c2-155">Vastendage see uus veerg kindlasti vastenduslehel.</span><span class="sxs-lookup"><span data-stu-id="a30c2-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="a30c2-156">Järgmisel joonisel on toodud näide malliülesande vastendusest andmeintegratsioonis.</span><span class="sxs-lookup"><span data-stu-id="a30c2-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="a30c2-157">Vastendamine näitab välja teavet. mis sünkroonitakse Finance and Operationsist Project Service Automationisse.</span><span class="sxs-lookup"><span data-stu-id="a30c2-157">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="a30c2-158">[![Malli vastendamine](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a30c2-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="a30c2-159">Projekti kulukategooriate sünkroonimine Project Service Automationist Finance and Operationsisse</span><span class="sxs-lookup"><span data-stu-id="a30c2-159">Project expense category synchronization from Project Service Automation to Finance and Operations</span></span>

### <a name="template-and-task"></a><span data-ttu-id="a30c2-160">Mall ja ülesanne</span><span class="sxs-lookup"><span data-stu-id="a30c2-160">Template and task</span></span>

<span data-ttu-id="a30c2-161">Projekti kulukategooriate sünkroonimiseks Project Service Automationist Finance and Operationsisse kasutatakse järgmist malli ja aluseks olevat ülesannet.</span><span class="sxs-lookup"><span data-stu-id="a30c2-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="a30c2-162">**Malli nimi andmete integratsioonis:** projekti kulukannete kategooriad (Project Service Automationist Finance and Operationsisse)</span><span class="sxs-lookup"><span data-stu-id="a30c2-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="a30c2-163">**Ülesande nimi projektis:** kategooriate sünkroonimine Finance and Operationsisse</span><span class="sxs-lookup"><span data-stu-id="a30c2-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="a30c2-164">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="a30c2-164">Entity set</span></span>

| <span data-ttu-id="a30c2-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a30c2-165">Project Service Automation</span></span> | <span data-ttu-id="a30c2-166">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a30c2-166">Finance and Operations</span></span>            |
|----------------------------|-----------------------------------|
| <span data-ttu-id="a30c2-167">Kandekategooriad</span><span class="sxs-lookup"><span data-stu-id="a30c2-167">Transaction categories</span></span>     | <span data-ttu-id="a30c2-168">Kategooriate integratsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="a30c2-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="a30c2-169">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="a30c2-169">Entity flow</span></span>

<span data-ttu-id="a30c2-170">Projekti kulukategooriaid hallatakse Finance and Operationsis ja need sünkroonitakse Project Service Automationiga kandekategooriatena.</span><span class="sxs-lookup"><span data-stu-id="a30c2-170">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="a30c2-171">Finance and Operationsisse tagasi sünkroonimine värskendab projektikategooriat Finance and Operationsis integratsiooni ID-ga Project Service Automationist.</span><span class="sxs-lookup"><span data-stu-id="a30c2-171">The synchronization back to Finance and Operations updates the project category in Finance and Operations with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a30c2-172">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="a30c2-172">Template mapping in Data integration</span></span>

<span data-ttu-id="a30c2-173">Järgmisel joonisel on toodud näide malliülesande vastendusest andmeintegratsioonis.</span><span class="sxs-lookup"><span data-stu-id="a30c2-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="a30c2-174">Vastendamine näitab välja teavet. mis sünkroonitakse Project Service Automationist Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="a30c2-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="a30c2-175">[![Malli vastendamine](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a30c2-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
