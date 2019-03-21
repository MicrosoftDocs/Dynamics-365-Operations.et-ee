---
title: Töövoo süsteem
description: Teema kirjeldab töövoosüsteemi rakenduses Microsoft Dynamics 365 for Finance and Operationsi.
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a35184a48eff9e320087cb9390a0f1eed1e7ba19
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/01/2019
ms.locfileid: "773084"
---
# <a name="workflow-system"></a><span data-ttu-id="d01b3-103">Töövoo süsteem</span><span class="sxs-lookup"><span data-stu-id="d01b3-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d01b3-104">Teema kirjeldab töövoosüsteemi rakenduses Microsoft Dynamics 365 for Finance and Operationsi.</span><span class="sxs-lookup"><span data-stu-id="d01b3-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="d01b3-105">Mis on töövoog?</span><span class="sxs-lookup"><span data-stu-id="d01b3-105">What is workflow?</span></span>

<span data-ttu-id="d01b3-106">Mõiste *töövoo* saab määratleda kahel viisil: süsteemi ja äriprotsessi.</span><span class="sxs-lookup"><span data-stu-id="d01b3-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="d01b3-107">Töövoog on süsteem</span><span class="sxs-lookup"><span data-stu-id="d01b3-107">Workflow is a system</span></span>

<span data-ttu-id="d01b3-108">Töövoog on koos Dynamics 365 for Finance and Operationsiga installitud süsteem, mis töötab rakendusobjekti serveril (AOS-il).</span><span class="sxs-lookup"><span data-stu-id="d01b3-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="d01b3-109">Töövoo süsteemil on funktsioone, millega saate luua eraldi töövooge või äriprotsesse.</span><span class="sxs-lookup"><span data-stu-id="d01b3-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="d01b3-110">Töövoog on äriprotsess</span><span class="sxs-lookup"><span data-stu-id="d01b3-110">Workflow is a business process</span></span>

<span data-ttu-id="d01b3-111">Töövoog esindab äriprotsessi.</span><span class="sxs-lookup"><span data-stu-id="d01b3-111">A workflow represents a business process.</span></span> <span data-ttu-id="d01b3-112">See määratleb, kuidas dokument voogab või liigub läbi süsteemi, näidates, kes peab täitma ülesannet, otsuse või dokumendi kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="d01b3-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="d01b3-113">Alltoodud joonisel kujutatakse kuluaruannete töövoogu.</span><span class="sxs-lookup"><span data-stu-id="d01b3-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Kasutajatele määratud elementidega töövoog](./media/workflow_user.gif)

<span data-ttu-id="d01b3-115">Selle töövoo paremaks mõistmiseks oletame, et Sam esitab kuluaruande summale 7000 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="d01b3-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="d01b3-116">Selle stsenaariumi kohaselt on Ivani ülesanne Sami lähetatud sissetulekud üle vaadata.</span><span class="sxs-lookup"><span data-stu-id="d01b3-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="d01b3-117">Seejärel peavad Frank ja Sue kuluaruande kinnitama.</span><span class="sxs-lookup"><span data-stu-id="d01b3-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="d01b3-118">Oletame nüüd, et Sam esitab kuluaruande summas 11 000 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="d01b3-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="d01b3-119">Selles stsenaariumis peab Ivan tšekid üle vaatama ning Frank, Sue ja Ann peavad kuluaruande kinnitama.</span><span class="sxs-lookup"><span data-stu-id="d01b3-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="d01b3-120"> Töövoo süsteemi kasutamise eelised</span><span class="sxs-lookup"><span data-stu-id="d01b3-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="d01b3-121">Töövoo süsteemi kasutamine teie organisatsioonis on mitmeti kasulik.</span><span class="sxs-lookup"><span data-stu-id="d01b3-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="d01b3-122">**Järjepidevad protsessid** – töövoo süsteem lubab teil määratleda, kuidas kindlaid dokumente, näiteks ostutaotlused ja kuluaruanded, töödeldakse.</span><span class="sxs-lookup"><span data-stu-id="d01b3-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="d01b3-123">Töövoo süsteemi abil tagate, et dokumente töödeldakse ja kinnitatakse ühtemoodi ja efektiivselt.</span><span class="sxs-lookup"><span data-stu-id="d01b3-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="d01b3-124">**Protsessi nähtavus** – töövoo süsteem lubab teil jälgida kindlate töövoo eksemplaride olekut ja ajalugu.</span><span class="sxs-lookup"><span data-stu-id="d01b3-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="d01b3-125">See aitab teil määratleda, kas töövoos tuleks muudatusi tõhususe parandamiseks.</span><span class="sxs-lookup"><span data-stu-id="d01b3-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="d01b3-126">**Koondatud tööde loend** – kasutajad saavad vaadata koondatud tööde loendit, et näha neile määratud töövoo ülesandeid ja kinnitusi.</span><span class="sxs-lookup"><span data-stu-id="d01b3-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="d01b3-127">Töövoo sisu</span><span class="sxs-lookup"><span data-stu-id="d01b3-127">Workflow content</span></span>

+ [<span data-ttu-id="d01b3-128">Töövoo arhitektuur</span><span class="sxs-lookup"><span data-stu-id="d01b3-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="d01b3-129">Töövoo elemendid</span><span class="sxs-lookup"><span data-stu-id="d01b3-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="d01b3-130">Töövoo tegevused</span><span class="sxs-lookup"><span data-stu-id="d01b3-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="d01b3-131">Töövoo loomine</span><span class="sxs-lookup"><span data-stu-id="d01b3-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="d01b3-132">Töövoo atribuutide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d01b3-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="d01b3-133">Töövoos käsitsi ülesande konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d01b3-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="d01b3-134">Töövoos automaatse ülesande konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d01b3-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="d01b3-135">Töövoo kinnitusprotsessi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d01b3-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="d01b3-136">Töövoo kinnitusetapi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d01b3-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="d01b3-137">Töövoos käsitsi otsuse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d01b3-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="d01b3-138">Töövoos tingimusliku otsuse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d01b3-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="d01b3-139">Töövoos paralleeltegevuse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d01b3-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="d01b3-140">Töövoos paralleelharu konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d01b3-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="d01b3-141">Rea kauba töövoo konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d01b3-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="d01b3-142">Töövoo KKK</span><span class="sxs-lookup"><span data-stu-id="d01b3-142">Workflow FAQ</span></span>](workflow-FAQ.md)
