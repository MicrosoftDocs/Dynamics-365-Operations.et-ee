---
title: Projekti kulukategooriate sünkroonimine Finance and Operationsi ja Project Service Automationi vahel
description: Selles teemas kirjeldatakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti kulukategooriate sünkroonimiseks rakenduste Dynamics 365 Finance ja Dynamics 365 Project Service Automation vahel.
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
ms.openlocfilehash: 482febc91a04766216f9887ab59d30cc9aed5096
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250503"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="056c3-103">Projekti kulukategooriate sünkroonimine Finance and Operationsi ja Project Service Automationi vahel</span><span class="sxs-lookup"><span data-stu-id="056c3-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="056c3-104">Selles teemas kirjeldatakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti kulukategooriate sünkroonimiseks rakenduste Dynamics 365 Finance ja Dynamics 365 Project Service Automation vahel.</span><span class="sxs-lookup"><span data-stu-id="056c3-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="056c3-105">Versioonis 8.0 on saadaval projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine.</span><span class="sxs-lookup"><span data-stu-id="056c3-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="056c3-106">Tegelike näitajate integratsioon on saadaval versioonis 8.0.1 või uuemas.</span><span class="sxs-lookup"><span data-stu-id="056c3-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="056c3-107">Kui kasutate rakendust Enterprise Edition 7.3.0, saate pärast KB 4132657 ja KB 4132660 installimist kasutada projektiülesannete, kulukannete kategooriate, tunnihinnangute, kuluhinnangute ja tegelike näitajate integreerimiseks ning funktsionaalsuse lukustamise konfigureerimiseks malle.</span><span class="sxs-lookup"><span data-stu-id="056c3-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="056c3-108">Kui peate lähtestama arvestuse jaotusi, soovitame installida KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="056c3-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="056c3-109">Andmevoog Project Service Automationis Finance’is</span><span class="sxs-lookup"><span data-stu-id="056c3-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="056c3-110">Project Service Automationist Finance’i integreerimise lahendus kasutab andmete sünkroonimiseks Project Service Automationi ja Finance’i eksemplaride vahel andmeintegratsiooni funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="056c3-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="056c3-111">Andmeintegratsiooni funktsioonis saadaolevad integratsioonimallid võimaldavad andmevoogu projekti kulukannete kategooriate kohta Finance’i ja Project Service Automationi vahel.</span><span class="sxs-lookup"><span data-stu-id="056c3-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="056c3-112">Kui projekti kulukategooriad on loodud Finance’is, on integratsioonivoog esmalt Finance’ist Project Service Automationisse.</span><span class="sxs-lookup"><span data-stu-id="056c3-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="056c3-113">Projekti kulukategooriate integratsiooni ID-d värskendatakse seejärel sünkroonimise kaudu Project Service Automationist Finance’i.</span><span class="sxs-lookup"><span data-stu-id="056c3-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="056c3-114">Kui projekti kulukategooriad on loodud Project Service Automationis, on integratsioonivoog esmalt Project Service Automationist Finance’i.</span><span class="sxs-lookup"><span data-stu-id="056c3-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="056c3-115">Enne Project Service Automationist sünkroonimist peavad projekti kategooriad olema juba Finance’is konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="056c3-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="056c3-116">Seejärel sünkroonige Finance’ist tagasi Project Service Automationisse ja siis uuesti Project Service Automationist Finance’i.</span><span class="sxs-lookup"><span data-stu-id="056c3-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="056c3-117">Sel viisil saate tagada, et kategooriad on seotud ja duplikaate ei looda.</span><span class="sxs-lookup"><span data-stu-id="056c3-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="056c3-118">Tavaliselt luuakse projekti kulukategooriad Finance’is.</span><span class="sxs-lookup"><span data-stu-id="056c3-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="056c3-119">Kui need aga ei ole loodud või kui kulukategooriad on juba loodud Project Service Automationis, peate kõigepealt sünkroonima, kasutades projekti kulukannete kategooriate (Project Service Automationist Finance and Operationsisse) malli.</span><span class="sxs-lookup"><span data-stu-id="056c3-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="056c3-120">Seejärel sünkroonige, kasutades projekti kulukannete kategooriate (Finance and Operationsist Project Service Automationisse) malli.</span><span class="sxs-lookup"><span data-stu-id="056c3-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="056c3-121">Pärast seda peaksite veel üks kord sünkroonima Project Service Automationist Finance’i.</span><span class="sxs-lookup"><span data-stu-id="056c3-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="056c3-122">Kui sünkroonite esmalt Project Service Automationist, peavad enne sünkroonimist olema Finance’is täidetud järgmised tingimused.</span><span class="sxs-lookup"><span data-stu-id="056c3-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="056c3-123">Olemas peab olema ühiskasutuses kategooria, mis vastab Project Service Automationis üles seatud projekti kategooriale, ja see peab olem lubatud nii suvandi **Projekt** kui ka **Kulu** jaoks.</span><span class="sxs-lookup"><span data-stu-id="056c3-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="056c3-124">Iga integreeritava Finance’i juriidilise isiku puhul peavad olemas olema järgmised projekti kategooriad.</span><span class="sxs-lookup"><span data-stu-id="056c3-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="056c3-125">**Projekti kategooria** on olemas.</span><span class="sxs-lookup"><span data-stu-id="056c3-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="056c3-126">**Kasuta kuludes** on lubatud.</span><span class="sxs-lookup"><span data-stu-id="056c3-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="056c3-127">**Aktiivne töölehel** on lubatud.</span><span class="sxs-lookup"><span data-stu-id="056c3-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="056c3-128">**Kande tüüp** on määratud olekule **Kulu**.</span><span class="sxs-lookup"><span data-stu-id="056c3-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="056c3-129">Järgmine illustratsioon näitab, kuidas andmeid Project Service Automationi ja Finance’i vahel sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="056c3-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="056c3-130">[![Andmevoog Project Service Automationi integreerimiseks Finance’iga](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="056c3-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="056c3-131">Projekti kulukategooriate sünkroonimine Finance’ist Project Service Automationisse</span><span class="sxs-lookup"><span data-stu-id="056c3-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="056c3-132">Mall ja ülesanne</span><span class="sxs-lookup"><span data-stu-id="056c3-132">Template and task</span></span>

<span data-ttu-id="056c3-133">Mallile juurdepääsuks valige Microsoft PowerAppsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="056c3-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="056c3-134">Projekti kulukategooriate sünkroonimiseks Finance’ist Project Service Automationisse kasutatakse järgmist malli ja aluseks olevat ülesannet.</span><span class="sxs-lookup"><span data-stu-id="056c3-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="056c3-135">**Andmeintegratsioon malli nimi:** projekti kulukannete kategooriad (Finance and Operationsist Project Service Automationisse)</span><span class="sxs-lookup"><span data-stu-id="056c3-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="056c3-136">**Ülesande nimi projektis:** kategooriate sünkroonimine Project Service Automationisse</span><span class="sxs-lookup"><span data-stu-id="056c3-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="056c3-137">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="056c3-137">Entity set</span></span>

| <span data-ttu-id="056c3-138">Finantsid</span><span class="sxs-lookup"><span data-stu-id="056c3-138">Finance</span></span>                           | <span data-ttu-id="056c3-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="056c3-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="056c3-140">Kategooriate integratsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="056c3-140">Integration entity for categories</span></span> | <span data-ttu-id="056c3-141">Kandekategooriad</span><span class="sxs-lookup"><span data-stu-id="056c3-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="056c3-142">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="056c3-142">Entity flow</span></span>

<span data-ttu-id="056c3-143">Projekti kulukategooriaid hallatakse Finance’is ja need sünkroonitakse Project Service Automationiga kandekategooriatena.</span><span class="sxs-lookup"><span data-stu-id="056c3-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="056c3-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="056c3-144">Power Query</span></span>

<span data-ttu-id="056c3-145">Project Service Automationisse sünkroonimisel peate kasutama Microsoft Power Queryt Exceli jaoks, et määrata kandekategooriale arveldustüüp.</span><span class="sxs-lookup"><span data-stu-id="056c3-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="056c3-146">Projekti kulukannete kategooriate (Finance and Operationsist Project Service Automationisse) mallil on olemas vaikeveerg ja vastendus.</span><span class="sxs-lookup"><span data-stu-id="056c3-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="056c3-147">Kui loote oma malli, peate lisama selle tingimusveeru Power Querys.</span><span class="sxs-lookup"><span data-stu-id="056c3-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="056c3-148">Tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="056c3-148">Follow these steps.</span></span>

1. <span data-ttu-id="056c3-149">Klõpsake noolt, et avada projekti kulukannete kategooriate (Finance and Operationsist Project Service Automationisse)mallis projekti kulukannete kategooriate vastendamise ülesanne.</span><span class="sxs-lookup"><span data-stu-id="056c3-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="056c3-150">Klõpsake linki **Täpsem päring ja filtreerimine**, et avada Power Query.</span><span class="sxs-lookup"><span data-stu-id="056c3-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="056c3-151">Valige suvand **Lisa tingimusveerg**.</span><span class="sxs-lookup"><span data-stu-id="056c3-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="056c3-152">Andke uuele veerule nimi, nt **ArvelduseTüüp**.</span><span class="sxs-lookup"><span data-stu-id="056c3-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="056c3-153">Sisestage järgmine tingimus: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="056c3-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="056c3-154">Klõpsake veerus **OK**.</span><span class="sxs-lookup"><span data-stu-id="056c3-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="056c3-155">Vastendage see uus veerg kindlasti vastenduslehel.</span><span class="sxs-lookup"><span data-stu-id="056c3-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="056c3-156">Järgmisel joonisel on toodud näide malliülesande vastendusest andmeintegratsioonis.</span><span class="sxs-lookup"><span data-stu-id="056c3-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="056c3-157">Vastendamine näitab välja teavet, mis sünkroonitakse Finance’ist rakendusse Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="056c3-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="056c3-158">[![Malli vastendamine](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="056c3-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="056c3-159">Projekti kulukategooriate sünkroonimine Finance’ist Project Service Automationisse</span><span class="sxs-lookup"><span data-stu-id="056c3-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="056c3-160">Mall ja ülesanne</span><span class="sxs-lookup"><span data-stu-id="056c3-160">Template and task</span></span>

<span data-ttu-id="056c3-161">Projekti kulukategooriate sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmist malli ja aluseks olevat ülesannet.</span><span class="sxs-lookup"><span data-stu-id="056c3-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="056c3-162">**Malli nimi andmete integratsioonis:** projekti kulukannete kategooriad (Project Service Automationist Finance and Operationsisse)</span><span class="sxs-lookup"><span data-stu-id="056c3-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="056c3-163">**Ülesande nimi projektis:** kategooriate sünkroonimine Finance and Operationsisse</span><span class="sxs-lookup"><span data-stu-id="056c3-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="056c3-164">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="056c3-164">Entity set</span></span>

| <span data-ttu-id="056c3-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="056c3-165">Project Service Automation</span></span> | <span data-ttu-id="056c3-166">Finantsid</span><span class="sxs-lookup"><span data-stu-id="056c3-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="056c3-167">Kandekategooriad</span><span class="sxs-lookup"><span data-stu-id="056c3-167">Transaction categories</span></span>     | <span data-ttu-id="056c3-168">Kategooriate integratsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="056c3-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="056c3-169">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="056c3-169">Entity flow</span></span>

<span data-ttu-id="056c3-170">Projekti kulukategooriaid hallatakse Finance’is ja need sünkroonitakse Project Service Automationiga kandekategooriatena.</span><span class="sxs-lookup"><span data-stu-id="056c3-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="056c3-171">Finance’i tagasi sünkroonimine värskendab projektikategooriat Finance’is integratsiooni ID-ga Project Service Automationist.</span><span class="sxs-lookup"><span data-stu-id="056c3-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="056c3-172">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="056c3-172">Template mapping in Data integration</span></span>

<span data-ttu-id="056c3-173">Järgmisel joonisel on toodud näide malliülesande vastendusest andmeintegratsioonis.</span><span class="sxs-lookup"><span data-stu-id="056c3-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="056c3-174">Vastendamine näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="056c3-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="056c3-175">[![Malli vastendamine](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="056c3-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
