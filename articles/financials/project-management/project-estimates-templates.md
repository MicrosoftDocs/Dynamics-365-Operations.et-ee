---
title: Projektihinnangute sünkroonimine otse Project Service Automationist rakendusse Finance and Operations
description: Selles teemas kirjeldatakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti eeldatavate tundide ja projekti eeldatava kulu sünkroonimiseks rakendusest Microsoft Dynamics 365 for Project Service Automation otse rakendusse Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556548"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="83ddc-103">Projektihinnangute sünkroonimine otse Project Service Automationist rakendusse Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="83ddc-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="83ddc-104">Selles teemas kirjeldatakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projekti eeldatavate tundide ja projekti eeldatava kulu sünkroonimiseks rakendusest Microsoft Dynamics 365 for Project Service Automation otse rakendusse Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="83ddc-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="83ddc-105">Rakenduse Microsoft Dynamics 365 for Finance and Operations versioonis 8.0 on saadaval projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine.</span><span class="sxs-lookup"><span data-stu-id="83ddc-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="83ddc-106">Tegelike näitajate integratsioon on saadaval rakenduse Microsoft Dynamics 365 for Finance and Operations versioonis 8.0.1 või uuemas.</span><span class="sxs-lookup"><span data-stu-id="83ddc-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="83ddc-107">Kui kasutate rakendust Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, saate pärast KB 4132657 ja KB 4132660 installimist kasutada projektiülesannete, kulukannete kategooriate, tunnihinnangute, kuluhinnangute ja tegelike näitajate integreerimiseks ning funktsionaalsuse lukustamise konfigureerimiseks malle.</span><span class="sxs-lookup"><span data-stu-id="83ddc-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="83ddc-108">Kui peate lähtestama arvestuse jaotusi, soovitame installida KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="83ddc-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="83ddc-109">Andmevoog Project Service Automationist Finance and Operationsisse</span><span class="sxs-lookup"><span data-stu-id="83ddc-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="83ddc-110">Project Service Automationist Finance and Operationsisse integreerimise lahendus kasutab andmete sünkroonimiseks Project Service Automationi ja Finance and Operationsi eksemplaride vahel andmeintegratsiooni funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="83ddc-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="83ddc-111">Andmeintegratsiooni funktsioonis saadaolevad integratsioonimallid võimaldavad andmevoogu projekti tunnihinnangute ja projekti kuluhinnangute kohta Project Service Automationist Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="83ddc-111">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="83ddc-112">Järgmine joonis näitab, kuidas sünkroonitakse andmeid Project Service Automationi ja Finance and Operationsi vahel.</span><span class="sxs-lookup"><span data-stu-id="83ddc-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="83ddc-113">[![Andmevoog Project Service Automationi integreerimiseks Finance and Operationsiga](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="83ddc-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="83ddc-114">Projekti eeldatavad tunnid</span><span class="sxs-lookup"><span data-stu-id="83ddc-114">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="83ddc-115">Mall ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="83ddc-115">Template and tasks</span></span>

<span data-ttu-id="83ddc-116">Saadaolevatele mallidele juurdepääsuks valige Microsoft PowerAppsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="83ddc-116">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="83ddc-117">Projekti tunnihinnangute sünkroonimiseks Project Service Automationist Finance and Operationsisse kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="83ddc-117">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="83ddc-118">**Andmeintegratsioon malli nimi:** projekti tunnihinnangud (Project Service Automationist Finance and Operationsisse)</span><span class="sxs-lookup"><span data-stu-id="83ddc-118">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="83ddc-119">**Ülesannete nimed projektis:**</span><span class="sxs-lookup"><span data-stu-id="83ddc-119">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="83ddc-120">Kandeseosed</span><span class="sxs-lookup"><span data-stu-id="83ddc-120">Transaction relationships</span></span>
    - <span data-ttu-id="83ddc-121">Kuluhinnangud</span><span class="sxs-lookup"><span data-stu-id="83ddc-121">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="83ddc-122">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="83ddc-122">Entity set</span></span>

| <span data-ttu-id="83ddc-123">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="83ddc-123">Project Service Automation</span></span> | <span data-ttu-id="83ddc-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="83ddc-124">Finance and Operations</span></span>                        |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="83ddc-125">Projektiülesanded</span><span class="sxs-lookup"><span data-stu-id="83ddc-125">Project tasks</span></span>              | <span data-ttu-id="83ddc-126">Projekti eeldatavate tundide integratsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="83ddc-126">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="83ddc-127">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="83ddc-127">Entity flow</span></span>

<span data-ttu-id="83ddc-128">Projekti tunnihinnanguid hallatakse Project Service Automationis ja need sünkroonitakse Finance and Operationsiga projekti tunnieelarvetena.</span><span class="sxs-lookup"><span data-stu-id="83ddc-128">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="83ddc-129">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="83ddc-129">Prerequisites</span></span>

<span data-ttu-id="83ddc-130">Enne projekti tunnihinnangute sünkroonimist peate sünkroonima projektid, projektiülesanded ja projekti kulukannete kategooriad.</span><span class="sxs-lookup"><span data-stu-id="83ddc-130">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="83ddc-131">Power Query</span><span class="sxs-lookup"><span data-stu-id="83ddc-131">Power Query</span></span>

<span data-ttu-id="83ddc-132">Porjekti eeldatavate tundide mallis peate kasutama Microsoft Power Queryt Exceli jaoks, et täita järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="83ddc-132">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="83ddc-133">Eelarve vaikemudeli ID seadistamine, mida kasutatakse, kui integratsioon loob uued tunnieelarved.</span><span class="sxs-lookup"><span data-stu-id="83ddc-133">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="83ddc-134">Ülesandest kõigi ressursikohaste kirjete väljafiltreerimine, mille integratsioon tunnieelarveteks nurjub.</span><span class="sxs-lookup"><span data-stu-id="83ddc-134">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="83ddc-135">Kõigi tühjade kandekategooria ridade väljafiltreerimine.</span><span class="sxs-lookup"><span data-stu-id="83ddc-135">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="83ddc-136">Selle ülesande täitmatajätmine võib põhjustada valesid tunnieelarved.</span><span class="sxs-lookup"><span data-stu-id="83ddc-136">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="83ddc-137">Eelarve vaikemudeli ID määramine</span><span class="sxs-lookup"><span data-stu-id="83ddc-137">Set the default forecast model ID</span></span>

<span data-ttu-id="83ddc-138">Eelarvemudeli vaike-ID värskendamiseks mallis klõpsake noolt **Vastendus**, et avada vastendus.</span><span class="sxs-lookup"><span data-stu-id="83ddc-138">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="83ddc-139">Seejärel valige link **Täpsem päring ja filtreerimine**.</span><span class="sxs-lookup"><span data-stu-id="83ddc-139">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="83ddc-140">Kui kasutate projekti tunnihinnangute (Project Service Automationist Finance and Operationsisse) vaikemalli, valige **Sisestatud tingimus** loendist **Rakendatud etapid**.</span><span class="sxs-lookup"><span data-stu-id="83ddc-140">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="83ddc-141">Asendage kirjes **Funktsioon** sõne **O\_forecast** selle eelarvemudeli ID nimega, mida tuleb integratsioonis kasutada.</span><span class="sxs-lookup"><span data-stu-id="83ddc-141">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="83ddc-142">Vaikemall kasutab eelarvemudeli ID-d demoandmetest.</span><span class="sxs-lookup"><span data-stu-id="83ddc-142">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="83ddc-143">Uue malli loomisel peate lisama selle veeru.</span><span class="sxs-lookup"><span data-stu-id="83ddc-143">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="83ddc-144">Power Querys valige **Lisa tingimusveerg** ja andke uuele veerule nimi, nt **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="83ddc-144">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="83ddc-145">Sisestage veerule tingimus, mis kui projektiülesanne ei ole null, siis \<sisestage eelarvemudeli ID\>; muidu null.</span><span class="sxs-lookup"><span data-stu-id="83ddc-145">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="83ddc-146">Ressursikohaste kirjete väljafiltreerimine</span><span class="sxs-lookup"><span data-stu-id="83ddc-146">Filter out resource-specific records</span></span>

<span data-ttu-id="83ddc-147">Projekti tunnihinnangute (Project Service Automationist Finance and Operationsisse) mallil on vaikefilter, mis eemaldab kõik ressursikohased kirjed.</span><span class="sxs-lookup"><span data-stu-id="83ddc-147">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="83ddc-148">Kui loote oma malli, peate selle filtri lisama.</span><span class="sxs-lookup"><span data-stu-id="83ddc-148">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="83ddc-149">Valige link **Täpsem päring ja filtreerimine**, et filtreerida veerg **msdyn\_islinetask**, nii et kaasatud oleks ainult kirjed väärtusega **Väär**.</span><span class="sxs-lookup"><span data-stu-id="83ddc-149">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="83ddc-150">Tühjade kandekategooria ridade väljafiltreerimine</span><span class="sxs-lookup"><span data-stu-id="83ddc-150">Filter out empty transaction category rows</span></span>

<span data-ttu-id="83ddc-151">Peate lisama filtri, millega eemaldada kõik tühjade kandekategooriatega read.</span><span class="sxs-lookup"><span data-stu-id="83ddc-151">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="83ddc-152">See ülesanne on nõutav, olenemata sellest, kas kasutate vaikemalli või loote oma malli.</span><span class="sxs-lookup"><span data-stu-id="83ddc-152">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="83ddc-153">See filter eemaldab kõik Project Service Automationist pärinevad kokkuvõtteread, mille tõttu võivad tunnieelarved Finance and Operationsis valed olla.</span><span class="sxs-lookup"><span data-stu-id="83ddc-153">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance and Operations to be incorrect.</span></span> <span data-ttu-id="83ddc-154">Valige link **Täpsem päring ja filtreerimine**, et filtreerida välja nullkirjed veerus **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="83ddc-154">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="83ddc-155">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="83ddc-155">Template mapping in Data integration</span></span>

<span data-ttu-id="83ddc-156">Järgmisel joonisel on toodud näide malliülesande vastendusest andmeintegratsioonis.</span><span class="sxs-lookup"><span data-stu-id="83ddc-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="83ddc-157">Vastendamine näitab välja teavet. mis sünkroonitakse Project Service Automationist Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="83ddc-157">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="83ddc-158">[![Malli vastendamine](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="83ddc-158">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="83ddc-159">Projekti kuluhinnangud</span><span class="sxs-lookup"><span data-stu-id="83ddc-159">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="83ddc-160">Mall ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="83ddc-160">Template and tasks</span></span>

<span data-ttu-id="83ddc-161">Projekti kuluhinnangute sünkroonimiseks Project Service Automationist Finance and Operationsisse kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="83ddc-161">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="83ddc-162">**Andmeintegratsioon malli nimi:** projekti kuluhinnangud (Project Service Automationist Finance and Operationsisse)</span><span class="sxs-lookup"><span data-stu-id="83ddc-162">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="83ddc-163">**Ülesannete nimed projektis:**</span><span class="sxs-lookup"><span data-stu-id="83ddc-163">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="83ddc-164">Kandeseosed</span><span class="sxs-lookup"><span data-stu-id="83ddc-164">Transaction relationships</span></span> 
    - <span data-ttu-id="83ddc-165">Kuluhinnangud</span><span class="sxs-lookup"><span data-stu-id="83ddc-165">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="83ddc-166">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="83ddc-166">Entity set</span></span>

| <span data-ttu-id="83ddc-167">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="83ddc-167">Project Service Automation</span></span> | <span data-ttu-id="83ddc-168">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="83ddc-168">Finance and Operations</span></span>                                   |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="83ddc-169">Kandeühendused</span><span class="sxs-lookup"><span data-stu-id="83ddc-169">Transaction Connections</span></span>    | <span data-ttu-id="83ddc-170">Projekti kande seoste integratsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="83ddc-170">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="83ddc-171">Hinnanguread</span><span class="sxs-lookup"><span data-stu-id="83ddc-171">Estimate Lines</span></span>             | <span data-ttu-id="83ddc-172">Projekti eeldatava kulu integratsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="83ddc-172">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="83ddc-173">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="83ddc-173">Entity flow</span></span>

<span data-ttu-id="83ddc-174">Projekti kuluhinnanguid hallatakse Project Service Automationis ja need sünkroonitakse Finance and Operationsiga projekti kulueelarvetena.</span><span class="sxs-lookup"><span data-stu-id="83ddc-174">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="83ddc-175">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="83ddc-175">Prerequisites</span></span>

<span data-ttu-id="83ddc-176">Enne projekti kuluhinnangute sünkroonimist peate sünkroonima projektid, projektiülesanded ja projekti kulukannete kategooriad.</span><span class="sxs-lookup"><span data-stu-id="83ddc-176">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="83ddc-177">Power Query</span><span class="sxs-lookup"><span data-stu-id="83ddc-177">Power Query</span></span>

<span data-ttu-id="83ddc-178">Projekti kuluhinnangute mallis peate kasutama Power Queryt järgmiste ülesannete täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="83ddc-178">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="83ddc-179">Filtreerimine kaasamaks ainult kuluhinnangu rea kirjed.</span><span class="sxs-lookup"><span data-stu-id="83ddc-179">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="83ddc-180">Eelarve vaikemudeli ID seadistamine, mida kasutatakse, kui integratsioon loob uued tunnieelarved.</span><span class="sxs-lookup"><span data-stu-id="83ddc-180">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="83ddc-181">Arveldustüüpide teisendamine</span><span class="sxs-lookup"><span data-stu-id="83ddc-181">Transform the billing types.</span></span>
- <span data-ttu-id="83ddc-182">Kandetüüpide teisendamine.</span><span class="sxs-lookup"><span data-stu-id="83ddc-182">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="83ddc-183">Filtreerimine kaasamaks ainult kuluhinnangu read</span><span class="sxs-lookup"><span data-stu-id="83ddc-183">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="83ddc-184">Projekti kuluhinnangute (Project Service Automationist Finance and Operationsisse) mallil on vaikefilter, mis kaasab integratsiooni ainult kuluread.</span><span class="sxs-lookup"><span data-stu-id="83ddc-184">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="83ddc-185">Kui loote oma malli, peate selle filtri lisama.</span><span class="sxs-lookup"><span data-stu-id="83ddc-185">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="83ddc-186">Valige ülesanne **Kandeseosed** ja seejärel klõpsake noolt **Vastendus**, et avada vastendus.</span><span class="sxs-lookup"><span data-stu-id="83ddc-186">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="83ddc-187">Valige link **Täpsem päring ja filtreerimine**.</span><span class="sxs-lookup"><span data-stu-id="83ddc-187">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="83ddc-188">Filtreerige veergu **msdyn\_transactiontype1**, nii et kuvataks ainult **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="83ddc-188">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="83ddc-189">Eelarve vaikemudeli ID määramine</span><span class="sxs-lookup"><span data-stu-id="83ddc-189">Set the default forecast model ID</span></span>

<span data-ttu-id="83ddc-190">Eelarvemudeli vaike-ID värskendamiseks mallis klõpsake valige ülesanne **Kuluhinnangud** ja seejärel klõpsake noolt **Vastendus**, et avada vastendus.</span><span class="sxs-lookup"><span data-stu-id="83ddc-190">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="83ddc-191">Valige link **Täpsem päring ja filtreerimine**.</span><span class="sxs-lookup"><span data-stu-id="83ddc-191">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="83ddc-192">Kui kasutate projekti kuluhinnangute (Project Service Automationist Finance and Operationsisse) vaikemalli, valige Power Querys esimene **Sisestatud tingimus** jaotises **Rakendatud etapid**.</span><span class="sxs-lookup"><span data-stu-id="83ddc-192">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="83ddc-193">Asendage kirjes **Funktsioon** sõne **O\_forecast** selle eelarvemudeli ID nimega, mida tuleb integratsioonis kasutada.</span><span class="sxs-lookup"><span data-stu-id="83ddc-193">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="83ddc-194">Vaikemall kasutab eelarvemudeli ID-d demoandmetest.</span><span class="sxs-lookup"><span data-stu-id="83ddc-194">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="83ddc-195">Uue malli loomisel peate lisama selle veeru.</span><span class="sxs-lookup"><span data-stu-id="83ddc-195">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="83ddc-196">Power Querys valige **Lisa tingimusveerg** ja andke uuele veerule nimi, nt **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="83ddc-196">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="83ddc-197">Sisestage veerule tingimus, mis kui hinnangurea ID ei ole null, siis \<sisestage eelarvemudeli ID\>; muidu null.</span><span class="sxs-lookup"><span data-stu-id="83ddc-197">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="83ddc-198">Arveldustüüpide teisendamine</span><span class="sxs-lookup"><span data-stu-id="83ddc-198">Transform the billing types</span></span>

<span data-ttu-id="83ddc-199">Projekti kuluhinnangute (Project Service Automationist Finance and Operationsisse) malli on lisatud tingimusveerg, mida kasutatakse Project Service Automationist integratsiooni käigus saadud arveldustüüpide teisendamiseks.</span><span class="sxs-lookup"><span data-stu-id="83ddc-199">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="83ddc-200">Kui loote oma malli, peate selle tingimusveeru lisama.</span><span class="sxs-lookup"><span data-stu-id="83ddc-200">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="83ddc-201">Valige link **Täpsem päring ja filtreerimine** ja seejärel valige **Lisa tingimusveerg**.</span><span class="sxs-lookup"><span data-stu-id="83ddc-201">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="83ddc-202">Andke uuele veerule nimi, nt **ArvelduseTüüp**.</span><span class="sxs-lookup"><span data-stu-id="83ddc-202">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="83ddc-203">Sisestage järgmine tingimus:</span><span class="sxs-lookup"><span data-stu-id="83ddc-203">Then enter the following condition:</span></span>

<span data-ttu-id="83ddc-204">Kui **msdyn\_billingtype** = 192350000 , siis **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="83ddc-204">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="83ddc-205">muidu kui **msdyn\_billingtype** = 192350001, siis **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="83ddc-205">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="83ddc-206">muidu kui **msdyn\_billingtype** = 192350002, siis **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="83ddc-206">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="83ddc-207">muidu **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="83ddc-207">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="83ddc-208">Kandetüüpide teisendamine</span><span class="sxs-lookup"><span data-stu-id="83ddc-208">Transform the transaction types</span></span>

<span data-ttu-id="83ddc-209">Projekti kuluhinnangute (Project Service Automationist Finance and Operationsisse) malli on lisatud tingimusveerg, mida kasutatakse Project Service Automationist integratsiooni käigus saadud kandetüüpide teisendamiseks.</span><span class="sxs-lookup"><span data-stu-id="83ddc-209">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="83ddc-210">Kui loote oma malli, peate selle tingimusveeru lisama.</span><span class="sxs-lookup"><span data-stu-id="83ddc-210">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="83ddc-211">Valige link **Täpsem päring ja filtreerimine** ja seejärel valige **Lisa tingimusveerg**.</span><span class="sxs-lookup"><span data-stu-id="83ddc-211">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="83ddc-212">Andke uuele veerule nimi, nt **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="83ddc-212">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="83ddc-213">Sisestage järgmine tingimus:</span><span class="sxs-lookup"><span data-stu-id="83ddc-213">Then enter the following condition:</span></span>

<span data-ttu-id="83ddc-214">Kui **msdyn\_transactiontypecode** = 192350000, siis **Cost**</span><span class="sxs-lookup"><span data-stu-id="83ddc-214">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="83ddc-215">muidu kui **msdyn\_transactiontypecode** = 192350005, siis **Sales**</span><span class="sxs-lookup"><span data-stu-id="83ddc-215">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="83ddc-216">muidu **null**</span><span class="sxs-lookup"><span data-stu-id="83ddc-216">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="83ddc-217">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="83ddc-217">Template mapping in Data integration</span></span>

<span data-ttu-id="83ddc-218">Järgmisel joonisel on toodud näited malliülesande vastendustest andmeintegratsioonis.</span><span class="sxs-lookup"><span data-stu-id="83ddc-218">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="83ddc-219">Vastendamine näitab välja teavet. mis sünkroonitakse Project Service Automationist Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="83ddc-219">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="83ddc-220">[![Malli vastendamine](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="83ddc-220">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="83ddc-221">[![Malli vastendamine](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="83ddc-221">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
