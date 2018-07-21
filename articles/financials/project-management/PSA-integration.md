---
title: Project Service Automation
description: "See lahendus kasutab andmeintegratsiooni funktsiooni andmete sünkroonimiseks rakenduste Microsoft Dynamics 365 for Finance and Operations ja Microsoft Dynamics 365 for Project Service Automation eksemplaride vahel teenuse Common Data Service (CDS) kaudu."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: et-ee
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="30c1e-103">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="30c1e-103">Project Service Automation</span></span>

<span data-ttu-id="30c1e-104">Project Service Automationist Finance and Operationsisse integratsiooni lahendus kasutab andmeintegratsiooni funktsiooni andmete sünkroonimiseks rakenduste Microsoft Dynamics 365 for Finance and Operations ja Microsoft Dynamics 365 for Project Service Automation eksemplaride vahel teenuse Common Data Service (CDS) kaudu.</span><span class="sxs-lookup"><span data-stu-id="30c1e-104">The Project Service Automation to Finance and Operations integration solution uses the Data Integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via the Common Data Service (CDS).</span></span> <span data-ttu-id="30c1e-105">Andmeintegratsiooni funktsiooniga saadaolevad integratsioonimallid võimaldavad andmevoogu projektide, projektilepingute, projektide, projektilepingu ridade, projektilepingu rea vahekokkuvõtete, projektiülesannete, kulukannete kategooriate, tunnihinnangute ja kuluhinnangute kohta Project Service Automationist Finance and Operationisse.</span><span class="sxs-lookup"><span data-stu-id="30c1e-105">The integration templates that are available with the Data Integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="30c1e-106">Kui kasutate rakendust Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, peate installima KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="30c1e-106">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="30c1e-107">See võimaldab teil integreerida fikseeritud hinnaga projekte.</span><span class="sxs-lookup"><span data-stu-id="30c1e-107">This will allow you to integrate fixed price projects.</span></span>
>
> <span data-ttu-id="30c1e-108">Kui kasutate rakenduse Dynamics 365 for Finance and Operations versiooni 8.0, saate kasutada projektiülesannete integreerimist, kulukannete kategooriaid, tunnihinnanguid, kuluhinnanguid ja funktsioonide lukustamist.</span><span class="sxs-lookup"><span data-stu-id="30c1e-108">If you are using Dynamics 365 for Finance and Operations version 8.0, you will be able to use project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
>
> <span data-ttu-id="30c1e-109">Kui kasutate rakenduse Dynamics 365 for Finance and Operations versiooni 8.0.1, saate sünkroonida tegelikke näitajaid.</span><span class="sxs-lookup"><span data-stu-id="30c1e-109">If you are using Dynamics 365 for Finance and Operations version 8.0.1, you will be able to synchronize actuals.</span></span>
>
> <span data-ttu-id="30c1e-110">Kui kasutate rakendust Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, saate pärast KB 4132657 ja KB 4132660 installimist kasutada malle projektiülesannete, kulukannete kategooriate, tunnihinnangute, kuluhinnangute ja tegelike näitajate integreerimiseks ning funktsionaalsuse lukustamise konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="30c1e-110">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="30c1e-111">Kui peate lähtestama arvestuse jaotusi, soovitame installida KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="30c1e-111">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

<span data-ttu-id="30c1e-112">Enne kui saate Project Service Automationi Finance and Operationsiga integreerida, peate konfigureerima Service Automationi integratsiooniparameetrid.</span><span class="sxs-lookup"><span data-stu-id="30c1e-112">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="30c1e-113">Lisateabe saamiseks vt teemat Project Service Automationi integratsiooniparameetrid.</span><span class="sxs-lookup"><span data-stu-id="30c1e-113">For more information, see Project Service Automation integration parameters.</span></span>

<span data-ttu-id="30c1e-114">See integratsioonilahendus võimaldab otsest sünkroonimist järgmistes stsenaariumides.</span><span class="sxs-lookup"><span data-stu-id="30c1e-114">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="30c1e-115">Projektilepingute haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="30c1e-115">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="30c1e-116">Projektide loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="30c1e-116">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="30c1e-117">Projektilepingu ridade haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="30c1e-117">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="30c1e-118">Projektilepingu ridade vahekokkuvõtete haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="30c1e-118">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="30c1e-119">Projektiülesannete haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="30c1e-119">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="30c1e-120">Kulukannete kategooriate haldamine Finance and Operationsis ja nende sünkroonimine Finance and Operationsist otse Project Service Automationisse.</span><span class="sxs-lookup"><span data-stu-id="30c1e-120">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="30c1e-121">Projekti tunnihinnangute loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="30c1e-121">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="30c1e-122">Projekti kuluhinnangute loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="30c1e-122">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="30c1e-123">Andmete sünkroonimine</span><span class="sxs-lookup"><span data-stu-id="30c1e-123">Data synchronization</span></span>
<span data-ttu-id="30c1e-124">Järgmine joonis näitab, kuidas sünkroonitakse andmeid integratsiooni osana Project Service Automationi ja Finance and Operationsi vahel.</span><span class="sxs-lookup"><span data-stu-id="30c1e-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="30c1e-125">Kõik mallid pole praegu saadaval.</span><span class="sxs-lookup"><span data-stu-id="30c1e-125">Not all templates are currently available.</span></span> <span data-ttu-id="30c1e-126">Mallid väljastatakse, kui need on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="30c1e-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="30c1e-127">[![Project Service Automationi integratsioon Finance and Operationsiga](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="30c1e-127">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="30c1e-128">Rakenduse Finance and Operations süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="30c1e-128">System requirements for Finance and Operations</span></span>

<span data-ttu-id="30c1e-129">Project Service Automationist Finance and Operationsisse integratsiooni lahenduse kasutamiseks peate installima rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 koos platvormivärskendusega 12 või uuemaga.</span><span class="sxs-lookup"><span data-stu-id="30c1e-129">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="30c1e-130">Project Service Automationi süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="30c1e-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="30c1e-131">Project Service Automationist Finance and Operationsisse integratsiooni lahenduse kasutamiseks peate installima järgmised komponendid.</span><span class="sxs-lookup"><span data-stu-id="30c1e-131">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="30c1e-132">Rakenduse Microsoft Dynamics 365 for Project Service Automation versioon 9.0.0.0 või uuem.</span><span class="sxs-lookup"><span data-stu-id="30c1e-132">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later.</span></span>
- <span data-ttu-id="30c1e-133">Lahendus Potentsiaalne klient sularahaks rakendusele Dynamics 365 for Sales, versioon 1.14.0.0 (v14) või hilisem.</span><span class="sxs-lookup"><span data-stu-id="30c1e-133">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>
- <span data-ttu-id="30c1e-134">Project Service Automationist Operationsisse lahendus rakendusele Dynamics 365 for Project Service Automation versioon 1.0.0.0 või uuem.</span><span class="sxs-lookup"><span data-stu-id="30c1e-134">Project Service Automation to Operations solution for Dynamics 365 for Project Service Automation version 1.0.0.0 or later.</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="30c1e-135">Project Service Automationist Finance and Operationsisse integratsiooni lahenduse installimine oma Project Service Automationi eksemplari</span><span class="sxs-lookup"><span data-stu-id="30c1e-135">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>



