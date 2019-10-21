---
title: Project Service Automationi ülevaade
description: Sellest teemast leiate teavet Dynamics 365 Project Service Automationi Dynamics 365 Financesse integreerimise kohta.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250549"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="c3ba5-103">Project Service Automationi ülevaade</span><span class="sxs-lookup"><span data-stu-id="c3ba5-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c3ba5-104">Project Service Automationist Finance’ga integratsiooni lahendus kasutab andmete sünkroonimiseks rakenduste Dynamics 365 Finance ja Dynamics 365 Project Service Automation eksemplaride vahel teenuse Common Data Service kaudu andmeintegratsiooni funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="c3ba5-105">Andmeintegratsiooni funktsiooniga saadaolevad integratsioonimallid võimaldavad andmevoogu projektide, projektilepingute, projektide, projektilepingu ridade, projektilepingu rea vahekokkuvõtete, projektiülesannete, kulukannete kategooriate, tunnihinnangute ja kuluhinnangute kohta Project Service Automationist Finance’i.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="c3ba5-106">Kui kasutate versiooni 7.3.0, peate installima KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="c3ba5-107">Seejärel saate integreerida fikseeritud hinnaga projekte.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="c3ba5-108">Kui kasutate versiooni 7.3.0 ja toote tasukanded rakendusest Project Service Automation üle, peate installima KB 4345320, et need tasud projekti arvesse kaasata.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="c3ba5-109">Kui kasutate versiooni 8.0, saate kasutada projektiülesannete integreerimist, kulukannete kategooriaid, tunnihinnanguid, kuluhinnanguid ja funktsioonide lukustamist.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="c3ba5-110">Kui kasutate versooni 8.0.1 või uuemat, saate sünkroonida tegelikke näitajaid.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="c3ba5-111">Enne kui saate Project Service Automationi Finance’iga integreerida, peate konfigureerima Project Service Automationi integratsiooniparameetrid.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="c3ba5-112">Lisateabe saamiseks vt teemat [Project Service Automationi integratsiooniparameetrid](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c3ba5-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="c3ba5-113">See integratsioonilahendus võimaldab otsest sünkroonimist järgmistes stsenaariumides.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="c3ba5-114">Projektilepingute haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance’i.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c3ba5-115">Projektide loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance’i.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c3ba5-116">Projektilepingute haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance’i.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c3ba5-117">Projektilepingute vahekokkuvõtete haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance’i.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c3ba5-118">Projektilepingute haldamine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance’i.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c3ba5-119">Kulukannete kategooriate haldamine Finance’is ja nende sünkroonimine Finance’ist otse Project Service Automationisse.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="c3ba5-120">Projekti tunnihinnangute loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance’i.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c3ba5-121">Projekti tunnihinnangute loomine Project Service Automationis ja nende sünkroonimine Project Service Automationist otse Finance’i.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c3ba5-122">Projekti aja, kulu ja tasu tegelike näitajate loomine Project Service Automationis ja projektikannete loomine Project Service Automationi integratsiooni töölehel, et neid saaks sisestada Finance’i.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="c3ba5-123">Andmete sünkroonimine</span><span class="sxs-lookup"><span data-stu-id="c3ba5-123">Data synchronization</span></span>

<span data-ttu-id="c3ba5-124">Järgmine joonis näitab, kuidas sünkroonitakse andmeid integratsiooni osana Project Service Automationi ja Finance’i vahel.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="c3ba5-125">Kõik mallid pole praegu saadaval.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-125">Not all templates are currently available.</span></span> <span data-ttu-id="c3ba5-126">Mallid väljastatakse, kui need on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="c3ba5-127">[![Project Service Automationi integreerimisparameetrid Finance’iga](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="c3ba5-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="c3ba5-128">Rakenduse Finance süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="c3ba5-128">System requirements for Finance</span></span>

<span data-ttu-id="c3ba5-129">Project Service Automationist Finance’iga integratsiooni lahenduse kasutamiseks peate installima rakenduse Enterprise edition 7.3 platvormivärskendusega 12 või uuemaga.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="c3ba5-130">Project Service Automationi süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="c3ba5-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="c3ba5-131">Project Service Automationist Finance’i integratsiooni lahenduse kasutamiseks peate installima järgmised komponendid.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="c3ba5-132">Dynamics 365 Project Service Automationi versioon 9.0.0.0 või uuem</span><span class="sxs-lookup"><span data-stu-id="c3ba5-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="c3ba5-133">Lahendus Prospect to cash rakendusele Dynamics 365 Sales, versioon 1.14.0.0 (v14) või hilisem.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="c3ba5-134">Project Service Automationi Finance’iga integratsiooni lahendus rakenduse Dynamics 365 Project Service Automation versioonile 1.0.0.0 või uuemale</span><span class="sxs-lookup"><span data-stu-id="c3ba5-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="c3ba5-135">Project Service Automationist Finance’i integratsiooni lahenduse installimine oma Project Service Automationi eksemplari</span><span class="sxs-lookup"><span data-stu-id="c3ba5-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="c3ba5-136">Laadige Project Service Automationi Finance’iga integreerimislahendus alla [Microsofti allalaadimiskeskusest](https://www.microsoft.com/download/details.aspx?id=57016) ja järgige lahendusega kaasasolevaid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="c3ba5-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
