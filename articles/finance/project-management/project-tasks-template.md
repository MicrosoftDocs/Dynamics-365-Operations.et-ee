---
title: Projektiülesannete sünkroonimine otse Project Service Automationist rakendusse Finance and Operations
description: Selles teemas kirjeldatakse malli ja aluseks olevat ülesannet, mida kasutatakse projekti ülesannete sünkroonimiseks rakendusest Microsoft Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance.
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
ms.openlocfilehash: ba475721b69e7c75dfd2197597b54050a3598d37
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770262"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="dca0c-103">Projektiülesannete sünkroonimine otse Project Service Automationist rakendusse Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dca0c-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dca0c-104">Selles teemas kirjeldatakse malli ja aluseks olevat ülesannet, mida kasutatakse projekti ülesannete sünkroonimiseks rakendusest Dynamics 365 Project Service Automation rakendusse Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="dca0c-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="dca0c-105">Versioonis 8.0 on saadaval projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine.</span><span class="sxs-lookup"><span data-stu-id="dca0c-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="dca0c-106">Kui kasutate rakendust Enterprise Edition 7.3.0, saate pärast KB 4132657 ja KB 4132660 installimist kasutada projektiülesannete, kulukannete kategooriate, tunnihinnangute, kuluhinnangute ja tegelike näitajate integreerimiseks ning funktsionaalsuse lukustamise konfigureerimiseks malle.</span><span class="sxs-lookup"><span data-stu-id="dca0c-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="dca0c-107">Kui peate lähtestama arvestuse jaotusi, soovitame installida KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="dca0c-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="dca0c-108">Tegelike näitajate integratsioon on saadaval versioonis 8.0.1 või uuemas.</span><span class="sxs-lookup"><span data-stu-id="dca0c-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="dca0c-109">Project Service Automationi andmevoog rakendusse Finance</span><span class="sxs-lookup"><span data-stu-id="dca0c-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="dca0c-110">Rakendusest Project Service Automation rakendusse Finance integratsiooni lahendus kasutab andmeintegratsiooni funktsiooni, et sünkroonida andmeid Project Service Automationi ja Finance’i eksemplaride vahel.</span><span class="sxs-lookup"><span data-stu-id="dca0c-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="dca0c-111">Andmeintegratsiooni funktsioonis saadaolev integratsioonimall võimaldab andmevoogu projektiülesannete kohta Project Service Automationist Finance’i.</span><span class="sxs-lookup"><span data-stu-id="dca0c-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="dca0c-112">Järgmine illustratsioon näitab, kuidas andmeid Project Service Automationi ja Finance’i vahel sünkroonitakse.</span><span class="sxs-lookup"><span data-stu-id="dca0c-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="dca0c-113">[![Andmevoog Project Service Automationi integreerimiseks Finance’iga](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="dca0c-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="dca0c-114">Mall ja ülesanne</span><span class="sxs-lookup"><span data-stu-id="dca0c-114">Template and task</span></span>

<span data-ttu-id="dca0c-115">Mallile juurdepääsuks valige Microsoft Power Appsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="dca0c-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="dca0c-116">Projekti tegelike näitajate sünkroonimiseks Project Service Automationist Finance’i kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="dca0c-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="dca0c-117">**Andmeintegratsioon malli nimi:** projektiülesanded (Project Service Automationist Finance and Operationsisse)</span><span class="sxs-lookup"><span data-stu-id="dca0c-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="dca0c-118">**Ülesande nimi projektis:** projektiülesanded</span><span class="sxs-lookup"><span data-stu-id="dca0c-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="dca0c-119">Enne projektiülesannete sünkroonimist peate sünkroonima projektilepingud ja projektid.</span><span class="sxs-lookup"><span data-stu-id="dca0c-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="dca0c-120">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="dca0c-120">Entity set</span></span>

| <span data-ttu-id="dca0c-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="dca0c-121">Project Service Automation</span></span> | <span data-ttu-id="dca0c-122">Finantsid</span><span class="sxs-lookup"><span data-stu-id="dca0c-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="dca0c-123">Projektiülesanded</span><span class="sxs-lookup"><span data-stu-id="dca0c-123">Project Tasks</span></span>              | <span data-ttu-id="dca0c-124">Projekti ülesande integratsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="dca0c-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="dca0c-125">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="dca0c-125">Entity flow</span></span>

<span data-ttu-id="dca0c-126">Projektiülesandeid hallatakse Project Service Automationis ja need sünkroonitakse Finance’iga projektitegevustena.</span><span class="sxs-lookup"><span data-stu-id="dca0c-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="dca0c-127">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="dca0c-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="dca0c-128">Enne projektiülesannete sünkroonimist peate sünkroonima projektilepingud ja projektid.</span><span class="sxs-lookup"><span data-stu-id="dca0c-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="dca0c-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="dca0c-129">Power Query</span></span>

<span data-ttu-id="dca0c-130">Peate kasutama andmete filtreerimiseks Microsoft Power Queryt Exceli jaoks, kui täidetud on järgmine tingimus.</span><span class="sxs-lookup"><span data-stu-id="dca0c-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="dca0c-131">Teil on projektiülesandes ressursikohaseid kirjeid.</span><span class="sxs-lookup"><span data-stu-id="dca0c-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="dca0c-132">Kui peate kasutama Power Queryt, järgige järgmist juhtnööri.</span><span class="sxs-lookup"><span data-stu-id="dca0c-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="dca0c-133">Projektiülesannete (Project Service Automationist Finance and Operationsisse) mallil on vaikefilter, mis välistab ressursikohased kirjed projektiülesandest, seades filtri veerus **IsLineTask** väärtusele **Väär**.</span><span class="sxs-lookup"><span data-stu-id="dca0c-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="dca0c-134">Kui loote oma malli, peate selle filtri lisama.</span><span class="sxs-lookup"><span data-stu-id="dca0c-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="dca0c-135">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="dca0c-135">Template mapping in Data integration</span></span>

<span data-ttu-id="dca0c-136">Järgmisel joonisel on toodud näide malliülesande vastendustest andmeintegratsioonis.</span><span class="sxs-lookup"><span data-stu-id="dca0c-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="dca0c-137">Vastendamine näitab välja teavet, mis sünkroonitakse Project Service Automationist rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="dca0c-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="dca0c-138">[![Malli vastendamine](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="dca0c-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
