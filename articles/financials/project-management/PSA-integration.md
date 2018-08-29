---
title: Project Service Automation
description: "See teema annab teavet Project Service Automationi Finance and Operationsiga integreerimislahenduse kohta. See integreerimislahendus kasutab andmeintegratsiooni funktsiooni andmete sünkroonimiseks rakenduste Microsoft Dynamics 365 for Finance and Operations ja Microsoft Dynamics 365 for Project Service Automation eksemplaride vahel teenuse Common Data Service kaudu."
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 4b1d2ae69899a2937d47f6547ee4ba72b2d1ece4
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="6b9c9-104">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6b9c9-104">Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6b9c9-105">Project Service Automationist Finance and Operationsisse integreerimislahendus kasutab andmeintegratsiooni funktsiooni andmete sünkroonimiseks rakenduste Microsoft Dynamics 365 for Finance and Operations ja Microsoft Dynamics 365 for Project Service Automation eksemplaride vahel teenuse Common Data Service kaudu.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-105">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="6b9c9-106">Andmeintegratsiooni funktsiooniga saadaolevad integratsioonimallid võimaldavad andmevoogu projektide, projektilepingute, projektide, projektilepingu ridade, projektilepingu rea vahekokkuvõtete, projektiülesannete, kulukannete kategooriate, tunnihinnangute ja kuluhinnangute kohta Project Service Automationist Finance and Operationisse.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-106">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="6b9c9-107">Kui kasutate rakendust Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, saate pärast KB 4132657 ja KB 4132660 installimist kasutada malle projektiülesannete, kulukannete kategooriate, tunnihinnangute, kuluhinnangute ja tegelike näitajate integreerimiseks ning funktsionaalsuse lukustamise konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="6b9c9-108">Kui peate lähtestama arvestuse jaotusi, soovitame installida KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="6b9c9-109">Kui kasutate Finance and Operationsi versiooni 7.3.0, peate installima KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-109">If you're using Finance and Operations 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="6b9c9-110">Seejärel saate integreerida fikseeritud hinnaga projekte.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-110">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="6b9c9-111">Kui kasutate rakendust Finance and Operations 7.3.0 ja toote tasukanded rakendusest Project Service Automation üle, peate installima KB 4345320, et need tasud projekti arvesse kaasata.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-111">If you're using Finance and Operations 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="6b9c9-112">Kui kasutate rakenduse Microsoft Dynamics 365 for Finance and Operations versiooni 8.0, saate kasutada projektiülesande integreerimist, kulukannete kategooriaid, tunnihinnanguid, kuluhinnanguid ja funktsioonide lukustamist.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-112">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="6b9c9-113">Kui kasutate rakenduse Microsoft Dynamics 365 for Finance and Operations versiooni 8.0.1 või uuemat, saate sünkroonida tegelikke näitajaid.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-113">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0.1, or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="6b9c9-114">Enne kui saate Project Service Automationi Finance and Operationsiga integreerida, peate konfigureerima Service Automationi integratsiooniparameetrid.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-114">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="6b9c9-115">Lisateabe saamiseks vt teemat [Project Service Automationi integratsiooniparameetrid](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6b9c9-115">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="6b9c9-116">See integratsioonilahendus võimaldab otsest sünkroonimist järgmistes stsenaariumides.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-116">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="6b9c9-117">Projektilepingute haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-117">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="6b9c9-118">Projektide loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-118">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="6b9c9-119">Projektilepingu ridade haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-119">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="6b9c9-120">Projektilepingu ridade vahekokkuvõtete haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-120">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="6b9c9-121">Projektiülesannete haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-121">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="6b9c9-122">Kulukannete kategooriate haldamine Finance and Operationsis ja nende sünkroonimine Finance and Operationsist otse Project Service Automationisse.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-122">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="6b9c9-123">Projekti tunnihinnangute loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-123">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="6b9c9-124">Projekti kuluhinnangute loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-124">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="6b9c9-125">Projekti aja, kulu ja tasu tegelike näitajate loomine Project Service Automationis ja projektikannete loomine Project Service Automationi integratsiooni töölehel, et neid saaks sisestada Finance and Operationsis.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-125">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="6b9c9-126">Andmete sünkroonimine</span><span class="sxs-lookup"><span data-stu-id="6b9c9-126">Data synchronization</span></span>

<span data-ttu-id="6b9c9-127">Järgmine joonis näitab, kuidas sünkroonitakse andmeid integratsiooni osana Project Service Automationi ja Finance and Operationsi vahel.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-127">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="6b9c9-128">Kõik mallid pole praegu saadaval.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-128">Not all templates are currently available.</span></span> <span data-ttu-id="6b9c9-129">Mallid väljastatakse, kui need on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-129">Templates will be released as they are completed.</span></span>

<span data-ttu-id="6b9c9-130">[![Project Service Automationi integratsioon Finance and Operationsiga](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="6b9c9-130">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="6b9c9-131">Rakenduse Finance and Operations süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="6b9c9-131">System requirements for Finance and Operations</span></span>

<span data-ttu-id="6b9c9-132">Project Service Automationist Finance and Operationsisse integratsiooni lahenduse kasutamiseks peate installima rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 koos platvormivärskendusega 12 või uuemaga.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-132">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="6b9c9-133">Project Service Automationi süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="6b9c9-133">System requirements for Project Service Automation</span></span>

<span data-ttu-id="6b9c9-134">Project Service Automationist Finance and Operationsisse integratsiooni lahenduse kasutamiseks peate installima järgmised komponendid.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-134">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="6b9c9-135">Rakenduse Microsoft Dynamics 365 for Project Service Automation versioon 9.0.0.0 või uuem</span><span class="sxs-lookup"><span data-stu-id="6b9c9-135">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="6b9c9-136">Lahendus Potentsiaalne klient sularahaks rakendusele Microsoft Dynamics 365 for Sales, versioon 1.14.0.0 (v14) või hilisem</span><span class="sxs-lookup"><span data-stu-id="6b9c9-136">Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="6b9c9-137">Project Service Automationist Finance and Operationsisse lahendus rakendusele Microsoft Dynamics 365 for Project Service Automation versioon 1.0.0.0 või uuem</span><span class="sxs-lookup"><span data-stu-id="6b9c9-137">Project Service Automation to Finance and Operations solution for Microsoft Dynamics 365 for Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="6b9c9-138">Project Service Automationist Finance and Operationsisse integratsiooni lahenduse installimine oma Project Service Automationi eksemplari</span><span class="sxs-lookup"><span data-stu-id="6b9c9-138">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="6b9c9-139">Laadige Project Service Automationi Finance and Operationsiga integreerimislahendus alla [Microsofti allalaadimiskeskusest](https://www.microsoft.com/en-us/download/details.aspx?id=57016) ja järgige lahendusega kaasasolevaid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="6b9c9-139">Download the Project Service Automation to Finance and Operations integration solution from [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>

