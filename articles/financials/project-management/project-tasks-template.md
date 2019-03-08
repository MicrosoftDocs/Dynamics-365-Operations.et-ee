---
title: Projektiülesannete sünkroonimine otse Project Service Automationist rakendusse Finance and Operations
description: Selles teemas kirjeldatakse malli ja aluseks olevat ülesannet, mida kasutatakse projekti ülesannete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Project Service Automation rakendusse Microsoft Dynamics 365 for Finance and Operations.
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
ms.openlocfilehash: 53e4eab0d455af4ac1e17754f31d46458db742c3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "355169"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="d80a5-103">Projektiülesannete sünkroonimine otse Project Service Automationist rakendusse Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d80a5-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d80a5-104">Selles teemas kirjeldatakse malli ja aluseks olevat ülesannet, mida kasutatakse projekti ülesannete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Project Service Automation rakendusse Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d80a5-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="d80a5-105">Projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine on saadaval rakenduse Microsoft Dynamics 365 for Finance and Operations versioonis 8.0.</span><span class="sxs-lookup"><span data-stu-id="d80a5-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="d80a5-106">Kui kasutate rakendust Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, saate pärast KB 4132657 ja KB 4132660 installimist kasutada projektiülesannete, kulukannete kategooriate, tunnihinnangute, kuluhinnangute ja tegelike näitajate integreerimiseks ning funktsionaalsuse lukustamise konfigureerimiseks malle.</span><span class="sxs-lookup"><span data-stu-id="d80a5-106">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="d80a5-107">Kui peate lähtestama arvestuse jaotusi, soovitame installida KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="d80a5-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="d80a5-108">Tegelike näitajate integratsioon on saadaval rakenduse Microsoft Dynamics 365 for Finance and Operations versioonis 8.0.1 või uuemas.</span><span class="sxs-lookup"><span data-stu-id="d80a5-108">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="d80a5-109">Andmevoog Project Service Automationist Finance and Operationsisse</span><span class="sxs-lookup"><span data-stu-id="d80a5-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="d80a5-110">Project Service Automationist Finance and Operationsisse integreerimise lahendus kasutab andmete sünkroonimiseks Project Service Automationi ja Finance and Operationsi eksemplaride vahel andmeintegratsiooni funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="d80a5-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="d80a5-111">Andmeintegratsiooni funktsioonis saadaolev integratsioonimall võimaldab andmevoogu projektiülesannete kohta Project Service Automationist Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="d80a5-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="d80a5-112">Järgmine joonis näitab, kuidas sünkroonitakse andmeid Project Service Automationi ja Finance and Operationsi vahel.</span><span class="sxs-lookup"><span data-stu-id="d80a5-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="d80a5-113">[![Andmevoog Project Service Automationi integreerimiseks Finance and Operationsiga](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="d80a5-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="d80a5-114">Mall ja ülesanne</span><span class="sxs-lookup"><span data-stu-id="d80a5-114">Template and task</span></span>

<span data-ttu-id="d80a5-115">Mallile juurdepääsuks valige Microsoft PowerAppsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="d80a5-115">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="d80a5-116">Projektiülesannete sünkroonimiseks Project Service Automationist Finance and Operationsisse kasutatakse järgmist malli ja aluseks olevat ülesannet.</span><span class="sxs-lookup"><span data-stu-id="d80a5-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="d80a5-117">**Andmeintegratsioon malli nimi:** projektiülesanded (Project Service Automationist Finance and Operationsisse)</span><span class="sxs-lookup"><span data-stu-id="d80a5-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="d80a5-118">**Ülesande nimi projektis:** projektiülesanded</span><span class="sxs-lookup"><span data-stu-id="d80a5-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="d80a5-119">Enne projektiülesannete sünkroonimist peate sünkroonima projektilepingud ja projektid.</span><span class="sxs-lookup"><span data-stu-id="d80a5-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="d80a5-120">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="d80a5-120">Entity set</span></span>

| <span data-ttu-id="d80a5-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="d80a5-121">Project Service Automation</span></span> | <span data-ttu-id="d80a5-122">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d80a5-122">Finance and Operations</span></span>              |
|----------------------------|-------------------------------------|
| <span data-ttu-id="d80a5-123">Projektiülesanded</span><span class="sxs-lookup"><span data-stu-id="d80a5-123">Project Tasks</span></span>              | <span data-ttu-id="d80a5-124">Projekti ülesande integratsiooniüksus</span><span class="sxs-lookup"><span data-stu-id="d80a5-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="d80a5-125">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="d80a5-125">Entity flow</span></span>

<span data-ttu-id="d80a5-126">Projektiülesandeid hallatakse Project Service Automationis ja need sünkroonitakse Finance and Operationsiga projektitegevustena.</span><span class="sxs-lookup"><span data-stu-id="d80a5-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="d80a5-127">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="d80a5-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="d80a5-128">Enne projektiülesannete sünkroonimist peate sünkroonima projektilepingud ja projektid.</span><span class="sxs-lookup"><span data-stu-id="d80a5-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="d80a5-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="d80a5-129">Power Query</span></span>

<span data-ttu-id="d80a5-130">Peate kasutama andmete filtreerimiseks Microsoft Power Queryt Exceli jaoks, kui täidetud on järgmine tingimus.</span><span class="sxs-lookup"><span data-stu-id="d80a5-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="d80a5-131">Teil on projektiülesandes ressursikohaseid kirjeid.</span><span class="sxs-lookup"><span data-stu-id="d80a5-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="d80a5-132">Kui peate kasutama Power Queryt, järgige järgmist juhtnööri.</span><span class="sxs-lookup"><span data-stu-id="d80a5-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="d80a5-133">Projektiülesannete (Project Service Automationist Finance and Operationsisse) mallil on vaikefilter, mis välistab ressursikohased kirjed projektiülesandest, seades filtri veerus **IsLineTask** väärtusele **Väär**.</span><span class="sxs-lookup"><span data-stu-id="d80a5-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="d80a5-134">Kui loote oma malli, peate selle filtri lisama.</span><span class="sxs-lookup"><span data-stu-id="d80a5-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d80a5-135">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="d80a5-135">Template mapping in Data integration</span></span>

<span data-ttu-id="d80a5-136">Järgmisel joonisel on toodud näide malliülesande vastendustest andmeintegratsioonis.</span><span class="sxs-lookup"><span data-stu-id="d80a5-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="d80a5-137">Vastendamine näitab välja teavet. mis sünkroonitakse Project Service Automationist Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="d80a5-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="d80a5-138">[![Malli vastendamine](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="d80a5-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
