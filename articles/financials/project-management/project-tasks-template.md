---
title: "Projektiülesannete sünkroonimine Project Service Automationist"
description: "See teema kirjeldab malli ja aluseks olevat ülesannet, mida kasutatakse projektiülesannete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Project Service Automation otse rakendusse Dynamics 365 for Finance and Operations."
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
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: et-ee
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a><span data-ttu-id="61041-103">Projektiülesannete sünkroonimine Project Service Automationist otse Finance and Operationsi projektitegevustesse</span><span class="sxs-lookup"><span data-stu-id="61041-103">Synchronize project tasks from Project Service Automation directly to project activities in Finance and Operations</span></span>

<span data-ttu-id="61041-104">See teema kirjeldab malli ja aluseks olevat ülesannet, mida kasutatakse projektiülesannete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Project Service Automation otse rakendusse Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61041-104">This topic describes the template and underlying task that is used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="61041-105">Projektiülesannete integreerimine, kulukannete kategooriad, tunnihinnangud, kuluhinnangud ja funktsioonide lukustamine on saadaval rakenduse Dynamics 365 for Finance and Operations versioonis 8.0.</span><span class="sxs-lookup"><span data-stu-id="61041-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="61041-106">Andmevoog Project Service Automationist Finance and Operationsisse</span><span class="sxs-lookup"><span data-stu-id="61041-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="61041-107">Project Service Automationist Finance and Operationsisse integreerimise lahendus kasutab andmete sünkroonimiseks Project Service Automationi ja Finance and Operationsi eksemplaride vahel andmeintegratsiooni funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="61041-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="61041-108">Andmeintegratsiooni funktsioonis saadaolev integratsioonimall võimaldab andmevoogu projektiülesannete kohta Project Service Automationist Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="61041-108">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="61041-109">Järgmine joonis näitab, kuidas sünkroonitakse andmeid Project Service Automationi ja Finance and Operationsi vahel.</span><span class="sxs-lookup"><span data-stu-id="61041-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="61041-110">[![Andmevoog Project Service Automationi integreerimiseks Finance and Operationsiga](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="61041-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="61041-111">Mall ja ülesanne</span><span class="sxs-lookup"><span data-stu-id="61041-111">Template and task</span></span>

<span data-ttu-id="61041-112">Mallile juurdepääsuks valige Microsoft PowerAppsi halduskeskuses suvand **Projektid** ja seejärel valige paremast ülanurgast suvand **Uus projekt**, et valida avalikud mallid.</span><span class="sxs-lookup"><span data-stu-id="61041-112">To access the template, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="61041-113">Projektiülesannete sünkroonimiseks Project Service Automationist Finance and Operationsisse kasutatakse järgmist malli ja aluseks olevat ülesannet.</span><span class="sxs-lookup"><span data-stu-id="61041-113">The following template and underlying task is used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="61041-114">-**Andmeintegratsiooni malli nimi:** projektiülesanded (Project Service Automationist Finance and Operationsisse) -**Ülesande nimi projektis:** projektiülesanded</span><span class="sxs-lookup"><span data-stu-id="61041-114">-**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops) -**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="61041-115">Enne projektiülesannete sünkroonimist peate sünkroonima projektilepingud ja projektid.</span><span class="sxs-lookup"><span data-stu-id="61041-115">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="61041-116">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="61041-116">Entity set</span></span>

|<span data-ttu-id="61041-117">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="61041-117">Project Service Automation</span></span>               | <span data-ttu-id="61041-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="61041-118">Finance and Operations</span></span>                |
|-----------------------------------------|---------------------------------------|
| <span data-ttu-id="61041-119">Projektiülesanded</span><span class="sxs-lookup"><span data-stu-id="61041-119">Project Tasks</span></span>                           | <span data-ttu-id="61041-120">Projektiülesande integratsiooniüksus.</span><span class="sxs-lookup"><span data-stu-id="61041-120">Integration entity for project task.</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="61041-121">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="61041-121">Entity flow</span></span>

<span data-ttu-id="61041-122">Projektiülesandeid hallatakse Project Service Automationis ja need sünkroonitakse Finance and Operationsiga projektitegevustena.</span><span class="sxs-lookup"><span data-stu-id="61041-122">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="61041-123">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="61041-123">Prerequisites and mapping setup</span></span>

<span data-ttu-id="61041-124">Enne projektiülesannete sünkroonimist peate sünkroonima projektilepingud ja projektid.</span><span class="sxs-lookup"><span data-stu-id="61041-124">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="61041-125">Power Query</span><span class="sxs-lookup"><span data-stu-id="61041-125">Power Query</span></span>

<span data-ttu-id="61041-126">Peate kasutama andmete filtreerimiseks Microsoft Power Queryt, kui täidetud on järgmised tingimused.</span><span class="sxs-lookup"><span data-stu-id="61041-126">You must use Microsoft Power Query to filter data if these conditions are met:</span></span>

- <span data-ttu-id="61041-127">Teil on projektiülesandes ressursikohaseid kirjeid.</span><span class="sxs-lookup"><span data-stu-id="61041-127">You have resource specific records within a project task.</span></span>

<span data-ttu-id="61041-128">Kui peate kasutama Power Queryt, järgige järgmisi juhtnööre.</span><span class="sxs-lookup"><span data-stu-id="61041-128">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="61041-129">Projektiülesannete (Project Service Automationist Finance and Operationsisse) mallil on vaikefilter ressursikohaste kirjete välistamiseks projektiülesandes, seades filtri veerus **IsLineTask** väärtusele **Väär**.</span><span class="sxs-lookup"><span data-stu-id="61041-129">The Project tasks (PSA to Fin and Ops) template has a default filter to exclude resource specific records from within a project task by setting the filter on the **IsLineTask** to **False**.</span></span> <span data-ttu-id="61041-130">Kui loote oma malli, peate selle filtri lisama.</span><span class="sxs-lookup"><span data-stu-id="61041-130">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="61041-131">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="61041-131">Template mapping in Data integration</span></span>

<span data-ttu-id="61041-132">Järgmisel joonisel on toodud näide malliülesande vastendustest andmeintegratsioonis.</span><span class="sxs-lookup"><span data-stu-id="61041-132">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="61041-133">Vastendamine näitab välja teavet. mis sünkroonitakse Project Service Automationist Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="61041-133">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="61041-134">[![Malli vastendamine](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="61041-134">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


