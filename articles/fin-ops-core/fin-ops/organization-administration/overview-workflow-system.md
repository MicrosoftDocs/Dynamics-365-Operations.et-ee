---
title: Töövoosüsteemi ülevaade
description: Teema kirjeldab töövoosüsteemi.
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: feb4ef0233b99420ebdd8781aae0191c9fa379f8
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692838"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="2be6e-103">Töövoosüsteemi ülevaade</span><span class="sxs-lookup"><span data-stu-id="2be6e-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2be6e-104">Teema kirjeldab töövoosüsteemi.</span><span class="sxs-lookup"><span data-stu-id="2be6e-104">This topic describes the workflow system.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="2be6e-105">Mis on töövoog?</span><span class="sxs-lookup"><span data-stu-id="2be6e-105">What is workflow?</span></span>

<span data-ttu-id="2be6e-106">Mõiste *töövoo* saab määratleda kahel viisil: süsteemi ja äriprotsessi.</span><span class="sxs-lookup"><span data-stu-id="2be6e-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="2be6e-107">Töövoog on süsteem</span><span class="sxs-lookup"><span data-stu-id="2be6e-107">Workflow is a system</span></span>

<span data-ttu-id="2be6e-108">Töövoog on süsteem, mis töötab rakendusobjekti serveris (AOS).</span><span class="sxs-lookup"><span data-stu-id="2be6e-108">Workflow is a system that runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="2be6e-109">Töövoo süsteemil on funktsioone, millega saate luua eraldi töövooge või äriprotsesse.</span><span class="sxs-lookup"><span data-stu-id="2be6e-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="2be6e-110">Töövoog on äriprotsess</span><span class="sxs-lookup"><span data-stu-id="2be6e-110">Workflow is a business process</span></span>

<span data-ttu-id="2be6e-111">Töövoog esindab äriprotsessi.</span><span class="sxs-lookup"><span data-stu-id="2be6e-111">A workflow represents a business process.</span></span> <span data-ttu-id="2be6e-112">See määratleb, kuidas dokument voogab või liigub läbi süsteemi, näidates, kes peab täitma ülesannet, otsuse või dokumendi kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="2be6e-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="2be6e-113">Alltoodud joonisel kujutatakse kuluaruannete töövoogu.</span><span class="sxs-lookup"><span data-stu-id="2be6e-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Kasutajatele määratud elementidega töövoog](./media/workflow_user.gif)

<span data-ttu-id="2be6e-115">Selle töövoo paremaks mõistmiseks oletame, et Sam esitab kuluaruande summale 7000 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="2be6e-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="2be6e-116">Selle stsenaariumi kohaselt on Ivani ülesanne Sami lähetatud sissetulekud üle vaadata.</span><span class="sxs-lookup"><span data-stu-id="2be6e-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="2be6e-117">Seejärel peavad Frank ja Sue kuluaruande kinnitama.</span><span class="sxs-lookup"><span data-stu-id="2be6e-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="2be6e-118">Oletame nüüd, et Sam esitab kuluaruande summas 11 000 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="2be6e-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="2be6e-119">Selles stsenaariumis peab Ivan tšekid üle vaatama ning Frank, Sue ja Ann peavad kuluaruande kinnitama.</span><span class="sxs-lookup"><span data-stu-id="2be6e-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="2be6e-120"> Töövoo süsteemi kasutamise eelised</span><span class="sxs-lookup"><span data-stu-id="2be6e-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="2be6e-121">Töövoo süsteemi kasutamine teie organisatsioonis on mitmeti kasulik.</span><span class="sxs-lookup"><span data-stu-id="2be6e-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="2be6e-122">**Järjepidevad protsessid** – töövoo süsteem lubab teil määratleda, kuidas kindlaid dokumente, näiteks ostutaotlused ja kuluaruanded, töödeldakse.</span><span class="sxs-lookup"><span data-stu-id="2be6e-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="2be6e-123">Töövoo süsteemi abil tagate, et dokumente töödeldakse ja kinnitatakse ühtemoodi ja efektiivselt.</span><span class="sxs-lookup"><span data-stu-id="2be6e-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="2be6e-124">**Protsessi nähtavus** – töövoo süsteem lubab teil jälgida kindlate töövoo eksemplaride olekut ja ajalugu.</span><span class="sxs-lookup"><span data-stu-id="2be6e-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="2be6e-125">See aitab teil määratleda, kas töövoos tuleks muudatusi tõhususe parandamiseks.</span><span class="sxs-lookup"><span data-stu-id="2be6e-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="2be6e-126">**Koondatud tööde loend** – kasutajad saavad vaadata koondatud tööde loendit, et näha neile määratud töövoo ülesandeid ja kinnitusi.</span><span class="sxs-lookup"><span data-stu-id="2be6e-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="2be6e-127">Töövoo sisu</span><span class="sxs-lookup"><span data-stu-id="2be6e-127">Workflow content</span></span>

+ [<span data-ttu-id="2be6e-128">Töövoo süsteemi arhitektuur</span><span class="sxs-lookup"><span data-stu-id="2be6e-128">Workflow system architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="2be6e-129">Töövooelemendid</span><span class="sxs-lookup"><span data-stu-id="2be6e-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="2be6e-130">Tegevused töövoo kinnitusprotsessis</span><span class="sxs-lookup"><span data-stu-id="2be6e-130">Actions in workflow approval processes</span></span>](workflow-actions.md)
+ [<span data-ttu-id="2be6e-131">Töövoogude loomise ülevaade</span><span class="sxs-lookup"><span data-stu-id="2be6e-131">Create workflows overview</span></span>](create-workflow.md)
+ [<span data-ttu-id="2be6e-132">Töövooatribuutide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2be6e-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="2be6e-133">Töövoos käsitsi ülesannete konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2be6e-133">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="2be6e-134">Töövoos automaatsete ülesannete konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2be6e-134">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="2be6e-135">Töövoo kinnitusprotsesside konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2be6e-135">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="2be6e-136">Töövoo kinnitusetappide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2be6e-136">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="2be6e-137">Töövoos käsitsi otsuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2be6e-137">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="2be6e-138">Töövoos tingimuslike otsuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2be6e-138">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="2be6e-139">Paralleeltegevuste konfigureerimine töövoos</span><span class="sxs-lookup"><span data-stu-id="2be6e-139">Configure parallel activities in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="2be6e-140">Paralleelharude konfigureerimine töövoos</span><span class="sxs-lookup"><span data-stu-id="2be6e-140">Configure parallel branches in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="2be6e-141">Reakauba töövoogude konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2be6e-141">Configure line-item workflows</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="2be6e-142">Töövoo KKK</span><span class="sxs-lookup"><span data-stu-id="2be6e-142">Workflow FAQ</span></span>](workflow-FAQ.md)
