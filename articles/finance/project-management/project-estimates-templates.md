---
title: Projektihinnangute sünkroonimine otse Project Service Automationist rakendusse Finance and Operations
description: Selles teemas kirjeldatakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti eeldatavate tundide ja projekti eeldatava kulu sünkroonimiseks rakendusest Microsoft Dynamics 365 Project Service Automation otse rakendusse Dynamics 365 Finance.
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ebf0fce60ad006e798aa4f404fbffcf10a0b31f9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770285"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="c8ffd-103">Projektihinnangute sünkroonimine otse Project Service Automationist rakendusse Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c8ffd-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c8ffd-104">Selles teemas kirjeldatakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti eeldatavate tundide ja projekti eeldatava kulu sünkroonimiseks rakendusest Dynamics 365 Project Service Automation otse rakendusse Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="c8ffd-105">Versioonis 8.0 on saadaval projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="c8ffd-106">Tegelike näitajate integratsioon on saadaval versioonis 8.0.1 või uuemas.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="c8ffd-107">Project Service Automationi andmevoog rakendusse Finance</span><span class="sxs-lookup"><span data-stu-id="c8ffd-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="c8ffd-108">Rakendusest Project Service Automation rakendusse Finance integratsiooni lahendus kasutab andmeintegratsiooni funktsiooni, et sünkroonida andmeid Project Service Automationi ja Finance’i eksemplaride vahel.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="c8ffd-109">Andmeintegratsiooni funktsioonis saadaolevad integratsioonimallid võimaldavad andmevoogu projekti tunnihinnangute ja projekti kuluhinnangute kohta Project Service Automationist Finance’i.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c8ffd-110">Järgmine illustratsioon näitab, kuidas andmeid Project Service Automationi ja Finance’i vahel sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="c8ffd-111">[![Andmevoog Project Service Automationi integreerimiseks Finance’iga](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="c8ffd-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="c8ffd-112">Projekti eeldatavad tunnid</span><span class="sxs-lookup"><span data-stu-id="c8ffd-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="c8ffd-113">Mall ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="c8ffd-113">Template and tasks</span></span>

<span data-ttu-id="c8ffd-114">Saadaolevatele mallidele juurdepääsuks valige Microsoft Power Appsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="c8ffd-115">Projekti tunnihinnangute sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="c8ffd-116">**Andmeintegratsioon malli nimi:** projekti tunnihinnangud (Project Service Automationist Finance and Operationsisse)</span><span class="sxs-lookup"><span data-stu-id="c8ffd-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="c8ffd-117">**Ülesannete nimed projektis:**</span><span class="sxs-lookup"><span data-stu-id="c8ffd-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="c8ffd-118">Kandeseosed</span><span class="sxs-lookup"><span data-stu-id="c8ffd-118">Transaction relationships</span></span>
    - <span data-ttu-id="c8ffd-119">Kuluhinnangud</span><span class="sxs-lookup"><span data-stu-id="c8ffd-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="c8ffd-120">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="c8ffd-120">Entity set</span></span>

| <span data-ttu-id="c8ffd-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c8ffd-121">Project Service Automation</span></span> | <span data-ttu-id="c8ffd-122">Finantsid</span><span class="sxs-lookup"><span data-stu-id="c8ffd-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="c8ffd-123">Projektiülesanded</span><span class="sxs-lookup"><span data-stu-id="c8ffd-123">Project tasks</span></span>              | <span data-ttu-id="c8ffd-124">Projekti eeldatavate tundide integratsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="c8ffd-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="c8ffd-125">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="c8ffd-125">Entity flow</span></span>

<span data-ttu-id="c8ffd-126">Projekti tunnihinnanguid hallatakse Project Service Automationis ja need sünkroonitakse Finance’iga projekti tunnieelarvetena.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="c8ffd-127">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="c8ffd-127">Prerequisites</span></span>

<span data-ttu-id="c8ffd-128">Enne projekti tunnihinnangute sünkroonimist peate sünkroonima projektid, projektiülesanded ja projekti kulukannete kategooriad.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="c8ffd-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="c8ffd-129">Power Query</span></span>

<span data-ttu-id="c8ffd-130">Porjekti eeldatavate tundide mallis peate kasutama Microsoft Power Queryt Exceli jaoks, et täita järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="c8ffd-131">Eelarve vaikemudeli ID seadistamine, mida kasutatakse, kui integratsioon loob uued tunnieelarved.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="c8ffd-132">Ülesandest kõigi ressursikohaste kirjete väljafiltreerimine, mille integratsioon tunnieelarveteks nurjub.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="c8ffd-133">Kõigi tühjade kandekategooria ridade väljafiltreerimine.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="c8ffd-134">Selle ülesande täitmatajätmine võib põhjustada valesid tunnieelarved.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="c8ffd-135">Eelarve vaikemudeli ID määramine</span><span class="sxs-lookup"><span data-stu-id="c8ffd-135">Set the default forecast model ID</span></span>

<span data-ttu-id="c8ffd-136">Eelarvemudeli vaike-ID värskendamiseks mallis klõpsake noolt **Vastendus**, et avada vastendus.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="c8ffd-137">Seejärel valige link **Täpsem päring ja filtreerimine**.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="c8ffd-138">Kui kasutate projekti tunnihinnangute (Project Service Automationist Finance and Operationsisse) vaikemalli, valige **Sisestatud tingimus** loendist **Rakendatud etapid**.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="c8ffd-139">Asendage kirjes **Funktsioon** sõne **O\_forecast** selle eelarvemudeli ID nimega, mida tuleb integratsioonis kasutada.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="c8ffd-140">Vaikemall kasutab eelarvemudeli ID-d demoandmetest.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="c8ffd-141">Uue malli loomisel peate lisama selle veeru.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="c8ffd-142">Power Querys valige **Lisa tingimusveerg** ja andke uuele veerule nimi, nt **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="c8ffd-143">Sisestage veerule tingimus, mis kui projektiülesanne ei ole null, siis \<sisestage eelarvemudeli ID\>; muidu null.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="c8ffd-144">Ressursikohaste kirjete väljafiltreerimine</span><span class="sxs-lookup"><span data-stu-id="c8ffd-144">Filter out resource-specific records</span></span>

<span data-ttu-id="c8ffd-145">Projekti tunnihinnangute (Project Service Automationist Finance and Operationsisse) mallil on vaikefilter, mis eemaldab kõik ressursikohased kirjed.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="c8ffd-146">Kui loote oma malli, peate selle filtri lisama.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="c8ffd-147">Valige link **Täpsem päring ja filtreerimine**, et filtreerida veerg **msdyn\_islinetask**, nii et kaasatud oleks ainult kirjed väärtusega **Väär**.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="c8ffd-148">Tühjade kandekategooria ridade väljafiltreerimine</span><span class="sxs-lookup"><span data-stu-id="c8ffd-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="c8ffd-149">Peate lisama filtri, millega eemaldada kõik tühjade kandekategooriatega read.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="c8ffd-150">See ülesanne on nõutav, olenemata sellest, kas kasutate vaikemalli või loote oma malli.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="c8ffd-151">See filter eemaldab kõik Project Service Automationist pärinevad kokkuvõtteread, mille tõttu võivad tunnieelarved Finance’is valed olla.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="c8ffd-152">Valige link **Täpsem päring ja filtreerimine**, et filtreerida välja nullkirjed veerus **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c8ffd-153">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="c8ffd-153">Template mapping in Data integration</span></span>

<span data-ttu-id="c8ffd-154">Järgmisel joonisel on toodud näide malliülesande vastendusest andmeintegratsioonis.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="c8ffd-155">Vastendamine näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c8ffd-156">[![Malli vastendamine](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="c8ffd-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="c8ffd-157">Projekti kuluhinnangud</span><span class="sxs-lookup"><span data-stu-id="c8ffd-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="c8ffd-158">Mall ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="c8ffd-158">Template and tasks</span></span>

<span data-ttu-id="c8ffd-159">Projekti tunnihinnangute sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="c8ffd-160">**Andmeintegratsioon malli nimi:** projekti kuluhinnangud (Project Service Automationist Finance and Operationsisse)</span><span class="sxs-lookup"><span data-stu-id="c8ffd-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="c8ffd-161">**Ülesannete nimed projektis:**</span><span class="sxs-lookup"><span data-stu-id="c8ffd-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="c8ffd-162">Kandeseosed</span><span class="sxs-lookup"><span data-stu-id="c8ffd-162">Transaction relationships</span></span> 
    - <span data-ttu-id="c8ffd-163">Kuluhinnangud</span><span class="sxs-lookup"><span data-stu-id="c8ffd-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="c8ffd-164">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="c8ffd-164">Entity set</span></span>

| <span data-ttu-id="c8ffd-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c8ffd-165">Project Service Automation</span></span> | <span data-ttu-id="c8ffd-166">Finantsid</span><span class="sxs-lookup"><span data-stu-id="c8ffd-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="c8ffd-167">Kandeühendused</span><span class="sxs-lookup"><span data-stu-id="c8ffd-167">Transaction Connections</span></span>    | <span data-ttu-id="c8ffd-168">Projekti kande seoste integratsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="c8ffd-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="c8ffd-169">Hinnanguread</span><span class="sxs-lookup"><span data-stu-id="c8ffd-169">Estimate Lines</span></span>             | <span data-ttu-id="c8ffd-170">Projekti eeldatava kulu integratsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="c8ffd-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="c8ffd-171">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="c8ffd-171">Entity flow</span></span>

<span data-ttu-id="c8ffd-172">Projekti kuluhinnanguid hallatakse Project Service Automationis ja need sünkroonitakse Finance’iga projekti kulueelarvetena.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="c8ffd-173">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="c8ffd-173">Prerequisites</span></span>

<span data-ttu-id="c8ffd-174">Enne projekti kuluhinnangute sünkroonimist peate sünkroonima projektid, projektiülesanded ja projekti kulukannete kategooriad.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="c8ffd-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="c8ffd-175">Power Query</span></span>

<span data-ttu-id="c8ffd-176">Projekti kuluhinnangute mallis peate kasutama Power Queryt järgmiste ülesannete täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="c8ffd-177">Filtreerimine kaasamaks ainult kuluhinnangu rea kirjed.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="c8ffd-178">Eelarve vaikemudeli ID seadistamine, mida kasutatakse, kui integratsioon loob uued tunnieelarved.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="c8ffd-179">Arveldustüüpide teisendamine</span><span class="sxs-lookup"><span data-stu-id="c8ffd-179">Transform the billing types.</span></span>
- <span data-ttu-id="c8ffd-180">Kandetüüpide teisendamine.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="c8ffd-181">Filtreerimine kaasamaks ainult kuluhinnangu read</span><span class="sxs-lookup"><span data-stu-id="c8ffd-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="c8ffd-182">Projekti kuluhinnangute (Project Service Automationist Finance and Operationsisse) mallil on vaikefilter, mis kaasab integratsiooni ainult kuluread.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="c8ffd-183">Kui loote oma malli, peate selle filtri lisama.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="c8ffd-184">Valige ülesanne **Kandeseosed** ja seejärel klõpsake noolt **Vastendus**, et avada vastendus.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="c8ffd-185">Valige link **Täpsem päring ja filtreerimine**.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="c8ffd-186">Filtreerige veergu **msdyn\_transactiontype1**, nii et kuvataks ainult **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="c8ffd-187">Eelarve vaikemudeli ID määramine</span><span class="sxs-lookup"><span data-stu-id="c8ffd-187">Set the default forecast model ID</span></span>

<span data-ttu-id="c8ffd-188">Eelarvemudeli vaike-ID värskendamiseks mallis klõpsake valige ülesanne **Kuluhinnangud** ja seejärel klõpsake noolt **Vastendus**, et avada vastendus.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="c8ffd-189">Valige link **Täpsem päring ja filtreerimine**.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="c8ffd-190">Kui kasutate projekti kuluhinnangute (Project Service Automationist Finance and Operationsisse) vaikemalli, valige Power Querys esimene **Sisestatud tingimus** jaotises **Rakendatud etapid**.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="c8ffd-191">Asendage kirjes **Funktsioon** sõne **O\_forecast** selle eelarvemudeli ID nimega, mida tuleb integratsioonis kasutada.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="c8ffd-192">Vaikemall kasutab eelarvemudeli ID-d demoandmetest.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="c8ffd-193">Uue malli loomisel peate lisama selle veeru.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="c8ffd-194">Power Querys valige **Lisa tingimusveerg** ja andke uuele veerule nimi, nt **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="c8ffd-195">Sisestage veerule tingimus, mis kui hinnangurea ID ei ole null, siis \<sisestage eelarvemudeli ID\>; muidu null.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="c8ffd-196">Arveldustüüpide teisendamine</span><span class="sxs-lookup"><span data-stu-id="c8ffd-196">Transform the billing types</span></span>

<span data-ttu-id="c8ffd-197">Projekti kuluhinnangute (Project Service Automationist Finance and Operationsisse) malli on lisatud tingimusveerg, mida kasutatakse Project Service Automationist integratsiooni käigus saadud arveldustüüpide teisendamiseks.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="c8ffd-198">Kui loote oma malli, peate selle tingimusveeru lisama.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="c8ffd-199">Valige link **Täpsem päring ja filtreerimine** ja seejärel valige **Lisa tingimusveerg**.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="c8ffd-200">Andke uuele veerule nimi, nt **ArvelduseTüüp**.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="c8ffd-201">Sisestage järgmine tingimus:</span><span class="sxs-lookup"><span data-stu-id="c8ffd-201">Then enter the following condition:</span></span>

<span data-ttu-id="c8ffd-202">Kui **msdyn\_billingtype** = 192350000 , siis **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="c8ffd-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="c8ffd-203">muidu kui **msdyn\_billingtype** = 192350001, siis **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="c8ffd-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="c8ffd-204">muidu kui **msdyn\_billingtype** = 192350002, siis **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="c8ffd-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="c8ffd-205">muidu **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="c8ffd-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="c8ffd-206">Kandetüüpide teisendamine</span><span class="sxs-lookup"><span data-stu-id="c8ffd-206">Transform the transaction types</span></span>

<span data-ttu-id="c8ffd-207">Projekti kuluhinnangute (Project Service Automationist Finance and Operationsisse) malli on lisatud tingimusveerg, mida kasutatakse Project Service Automationist integratsiooni käigus saadud kandetüüpide teisendamiseks.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="c8ffd-208">Kui loote oma malli, peate selle tingimusveeru lisama.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="c8ffd-209">Valige link **Täpsem päring ja filtreerimine** ja seejärel valige **Lisa tingimusveerg**.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="c8ffd-210">Andke uuele veerule nimi, nt **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="c8ffd-211">Sisestage järgmine tingimus:</span><span class="sxs-lookup"><span data-stu-id="c8ffd-211">Then enter the following condition:</span></span>

<span data-ttu-id="c8ffd-212">Kui **msdyn\_transactiontypecode** = 192350000, siis **Cost**</span><span class="sxs-lookup"><span data-stu-id="c8ffd-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="c8ffd-213">muidu kui **msdyn\_transactiontypecode** = 192350005, siis **Sales**</span><span class="sxs-lookup"><span data-stu-id="c8ffd-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="c8ffd-214">muidu **null**</span><span class="sxs-lookup"><span data-stu-id="c8ffd-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c8ffd-215">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="c8ffd-215">Template mapping in Data integration</span></span>

<span data-ttu-id="c8ffd-216">Järgmisel joonisel on toodud näited malliülesande vastendustest andmeintegratsioonis.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="c8ffd-217">Vastendamine näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="c8ffd-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c8ffd-218">[![Malli vastendamine](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="c8ffd-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="c8ffd-219">[![Malli vastendamine](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="c8ffd-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
