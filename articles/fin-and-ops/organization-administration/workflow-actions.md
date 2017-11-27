---
title: "Töövoo tegevused"
description: "Selles artiklis selgitatakse toiminguid, mida iga osaleja saab töövoo kinnitusprotsessis teha."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2a4717accfa7e5879ee757820c39f000fa7d3e95
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="workflow-actions"></a><span data-ttu-id="f3afb-103">Töövoo tegevused</span><span class="sxs-lookup"><span data-stu-id="f3afb-103">Workflow actions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f3afb-104">Selles artiklis selgitatakse toiminguid, mida iga osaleja saab töövoo kinnitusprotsessis teha.</span><span class="sxs-lookup"><span data-stu-id="f3afb-104">This article explains the actions that each participant in a workflow approval process can take.</span></span>

<span data-ttu-id="f3afb-105">Töövoog võib hõlmata mitut inimeste gruppi: algataja, ülesandes osalejad, otsustajad ja kinnitajad.</span><span class="sxs-lookup"><span data-stu-id="f3afb-105">A workflow can involve several groups of people: the originator, task assignees, decision makers, and approvers.</span></span> <span data-ttu-id="f3afb-106">Näiteks järgmises kuluaruande töövoos on Sam algataja, järjekorra liikmed on ülesandes osalejad, John on otsustaja ning Frank, Sue ja Ann on kinnitajad.</span><span class="sxs-lookup"><span data-stu-id="f3afb-106">For example, in the following expense report workflow, Sam is the originator, the members of the queue are task assignees, John is a decision maker, and Frank, Sue, and Ann are approvers.</span></span>   

<span data-ttu-id="f3afb-107">[![Töövoog\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span><span class="sxs-lookup"><span data-stu-id="f3afb-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span></span> 

<span data-ttu-id="f3afb-108">Järgmistes jaotistes selgitatakse töövoo toiminguid, mida iga grupp saab teha.</span><span class="sxs-lookup"><span data-stu-id="f3afb-108">The following sections explain the workflow actions that each group can perform.</span></span>

## <a name="actions-that-an-originator-can-perform"></a><span data-ttu-id="f3afb-109">Toimingud, mida algataja saab teha</span><span class="sxs-lookup"><span data-stu-id="f3afb-109">Actions that an originator can perform</span></span>
<span data-ttu-id="f3afb-110">Algataja alustab töövoo eksemplari, edastades dokumendi töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="f3afb-110">The originator starts a workflow instance by submitting a document for processing.</span></span> <span data-ttu-id="f3afb-111">Näiteks Sam peab oma kuluaruande esitamiseks klõpsama nuppu **Edasta** lehel **Kuluaruanne**.</span><span class="sxs-lookup"><span data-stu-id="f3afb-111">For example, Sam must click the **Submit** button on the **Expense report** page to submit his expense report.</span></span>

## <a name="actions-that-a-task-assignee-can-perform"></a><span data-ttu-id="f3afb-112">Toimingud, mida ülesandes osaleja saab teha</span><span class="sxs-lookup"><span data-stu-id="f3afb-112">Actions that a task assignee can perform</span></span>
<span data-ttu-id="f3afb-113">Ülesande saab määrata mitmele inimesele või tööüksuste järjekorrale, mida jälgib mitu inimest.</span><span class="sxs-lookup"><span data-stu-id="f3afb-113">A task can be assigned to multiple people or to a work item queue that is monitored by several people.</span></span> <span data-ttu-id="f3afb-114">Ülesande täita saab siiski ainult üks inimene.</span><span class="sxs-lookup"><span data-stu-id="f3afb-114">However, only one person can complete a task.</span></span> <span data-ttu-id="f3afb-115">Näiteks Sam on esitanud kuluaruande ja on suunanud oma sissetulekud oma organisatsiooni kuluaruannete osakonnale ülevaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="f3afb-115">For example, Sam has submitted an expense report and has routed his receipts to his organization's Expense Reports department for review.</span></span> 

<span data-ttu-id="f3afb-116">Ettevõtte Adventure Works kuluaruannete osakonna liikmed jälgivad järjekorda.</span><span class="sxs-lookup"><span data-stu-id="f3afb-116">The members of the Adventure Works Expense Reports department monitor the queue.</span></span> <span data-ttu-id="f3afb-117">Julie, selle osakonna liige, on võtnud vastu ülesande vaadata üle Sami kuluaruanne ja kviitungid.</span><span class="sxs-lookup"><span data-stu-id="f3afb-117">Julie, a member of that department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="f3afb-118">Ta võib nüüd teha ühe järgmistest toimingutest: lõpule viia, tagasi lükata, delegeerida, paluda muutmist, ümber määrata või vabastada.</span><span class="sxs-lookup"><span data-stu-id="f3afb-118">She can now perform one of the following actions: complete, reject, delegate, request change, reassign, or release.</span></span> 

<span data-ttu-id="f3afb-119">**Märkus.** Kasutatavad toimingud on erinevad, olenevalt sellest, kuidas tarkvaraarendaja ülesande üles ehitas.</span><span class="sxs-lookup"><span data-stu-id="f3afb-119">**Note:** The actions that are available vary, depending on how the software developer designed the task.</span></span>

### <a name="complete"></a><span data-ttu-id="f3afb-120">Lõpule viimine</span><span class="sxs-lookup"><span data-stu-id="f3afb-120">Complete</span></span>

<span data-ttu-id="f3afb-121">Kui kasutaja viib ülesande lõpule, määratakse töötlemiseks edastatud dokument vajaduse korral järgmisele töövoo kasutajale, kui järgmine kasutaja on olemas.</span><span class="sxs-lookup"><span data-stu-id="f3afb-121">When a user completes a task, the document that was submitted for processing is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="f3afb-122">Kui rohkem töötlemist ei ole vaja, siis töövoo protsess lõpeb.</span><span class="sxs-lookup"><span data-stu-id="f3afb-122">If no additional processing is required, the workflow process ends.</span></span> 

<span data-ttu-id="f3afb-123">Näiteks Julie, ettevõtte Adventure Works kuluaruannete osakonna liige, on võtnud vastu ülesande vaadata üle Sami kuluaruanne ja kviitungid.</span><span class="sxs-lookup"><span data-stu-id="f3afb-123">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam’s expense report and receipts.</span></span> <span data-ttu-id="f3afb-124">Kui Julie on oma ülevaatuse lõpetanud, määratakse dokument Johnile.</span><span class="sxs-lookup"><span data-stu-id="f3afb-124">After Julie completes her review, the document is assigned to John.</span></span>

### <a name="reject"></a><span data-ttu-id="f3afb-125">Lükka tagasi</span><span class="sxs-lookup"><span data-stu-id="f3afb-125">Reject</span></span>

<span data-ttu-id="f3afb-126">Kui kasutaja lükkab dokumendi tagasi, lõpeb töövooprotsess.</span><span class="sxs-lookup"><span data-stu-id="f3afb-126">When a user rejects a document, the workflow process ends.</span></span> 

<span data-ttu-id="f3afb-127">Näiteks Julie, ettevõtte Adventure Works kuluaruannete osakonna liige, on võtnud vastu ülesande vaadata üle Sami kuluaruanne ja kviitungid.</span><span class="sxs-lookup"><span data-stu-id="f3afb-127">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam’s expense report and receipts.</span></span> <span data-ttu-id="f3afb-128">Kui Julie selle kuluaruande tagasi lükkab, lõpeb töövoog.</span><span class="sxs-lookup"><span data-stu-id="f3afb-128">If Julie rejects the expense report, the workflow process ends.</span></span> 

<span data-ttu-id="f3afb-129">Sam saab seejärel kuluaruande uuesti esitada.</span><span class="sxs-lookup"><span data-stu-id="f3afb-129">Sam can then resubmit the expense report.</span></span> <span data-ttu-id="f3afb-130">Ta saab teha esmalt muudatusi või edastada uuesti algse versiooni.</span><span class="sxs-lookup"><span data-stu-id="f3afb-130">He can make changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="f3afb-131">Kui Sam kuluaruande uuesti esitab, käivitatakse töövoo protsess käsitsi ülevaatamise toimingust.</span><span class="sxs-lookup"><span data-stu-id="f3afb-131">If Sam resubmits the expense report, the workflow process starts at the manual review task.</span></span>

### <a name="delegate"></a><span data-ttu-id="f3afb-132">Delegeeri</span><span class="sxs-lookup"><span data-stu-id="f3afb-132">Delegate</span></span>

<span data-ttu-id="f3afb-133">Kui kasutaja delegeerib ülesande, määratakse ülesanne teisele kasutajale.</span><span class="sxs-lookup"><span data-stu-id="f3afb-133">When a user delegates a task, the task is assigned to another user.</span></span> 

<span data-ttu-id="f3afb-134">Näiteks Julie, ettevõtte Adventure Works kuluaruannete osakonna liige, on võtnud vastu ülesande vaadata üle Sami kuluaruanne ja kviitungid.</span><span class="sxs-lookup"><span data-stu-id="f3afb-134">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="f3afb-135">Julie delegeerib ülesande Timile, kes on tema assistent.</span><span class="sxs-lookup"><span data-stu-id="f3afb-135">Julie delegates this task to Tim, who is her assistant.</span></span> 

<span data-ttu-id="f3afb-136">Tim tegutseb seejärel Julie nimel.</span><span class="sxs-lookup"><span data-stu-id="f3afb-136">Tim then acts on behalf of Julie.</span></span> <span data-ttu-id="f3afb-137">Seetõttu, kui Tim ülevaatamise lõpetab, määratakse kuluaruanne Johnile, just nii, nagu Julie oleks selle ülesande täitnud.</span><span class="sxs-lookup"><span data-stu-id="f3afb-137">Therefore, when Tim completes his review, the expense report is assigned to John, just as if Julie had completed the task.</span></span>

### <a name="request-change"></a><span data-ttu-id="f3afb-138">Taotle muudatust</span><span class="sxs-lookup"><span data-stu-id="f3afb-138">Request change</span></span>

<span data-ttu-id="f3afb-139">Kui kasutaja taotleb edastatud dokumendi muutmist, saadetakse dokument tagasi algatajale.</span><span class="sxs-lookup"><span data-stu-id="f3afb-139">When a user requests a change to a document that was submitted, the document is sent back to the originator.</span></span> 

<span data-ttu-id="f3afb-140">Näiteks Julie, ettevõtte Adventure Works kuluaruannete osakonna liige, on võtnud vastu ülesande vaadata üle Sami kuluaruanne ja kviitungid.</span><span class="sxs-lookup"><span data-stu-id="f3afb-140">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="f3afb-141">Julie märkab kuluaruandes mõnda viga ja soovib muudatusi.</span><span class="sxs-lookup"><span data-stu-id="f3afb-141">Julie notices some errors on the expense report and requests changes.</span></span> <span data-ttu-id="f3afb-142">Kuluaruanne saadetakse tagasi Samile.</span><span class="sxs-lookup"><span data-stu-id="f3afb-142">The expense report is sent back to Sam.</span></span> 

<span data-ttu-id="f3afb-143">Sam saab kuluaruande uuesti esitada.</span><span class="sxs-lookup"><span data-stu-id="f3afb-143">Sam can resubmit the expense report.</span></span> <span data-ttu-id="f3afb-144">Ta võib teha esmalt soovitud muudatused või edastada uuesti algse versiooni.</span><span class="sxs-lookup"><span data-stu-id="f3afb-144">He can make the requested changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="f3afb-145">Kui Sam kuluaruande uuesti esitab, peab tööüksuste järjekorra liige kuluaruande ja kviitungid uuesti üle vaatama.</span><span class="sxs-lookup"><span data-stu-id="f3afb-145">If Sam resubmits the expense report, a member of the work item queue must review the expense report and the receipts again.</span></span>

### <a name="reassign"></a><span data-ttu-id="f3afb-146">Määra uuesti</span><span class="sxs-lookup"><span data-stu-id="f3afb-146">Reassign</span></span>

<span data-ttu-id="f3afb-147">Tööüksuste järjekorra liikmed võivad määrata selles järjekorras olevaid dokumente ka teise järjekorda ümber.</span><span class="sxs-lookup"><span data-stu-id="f3afb-147">The members of a work item queue can reassign documents that are in that queue to another queue.</span></span> 

<span data-ttu-id="f3afb-148">Näiteks Julie, ettevõtte Adventure Works kuluaruannete osakonna liige, jälgib järjekorda.</span><span class="sxs-lookup"><span data-stu-id="f3afb-148">For example, Julie, a member of the Adventure Works Expense Reports department, is monitoring the queue.</span></span> <span data-ttu-id="f3afb-149">Et aidata töökoormust tasakaalustada, võib ta kuluaruande ja sellega kaasas olevad kviitungid teise järjekorda ümber määrata.</span><span class="sxs-lookup"><span data-stu-id="f3afb-149">To help balance the workload, she can reassign the expense report, and the receipts that are included with it, to another queue.</span></span>

### <a name="release"></a><span data-ttu-id="f3afb-150">Vabasta</span><span class="sxs-lookup"><span data-stu-id="f3afb-150">Release</span></span>

<span data-ttu-id="f3afb-151">Aeg-ajalt võib tööüksuste järjekorra liige ülesande vastu võtta, kuid seejärel otsustada, et ta ei saa seda lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="f3afb-151">Occasionally, a member of a work item queue might accept a task, but then decide that he or she can't complete the task.</span></span> <span data-ttu-id="f3afb-152">Sel juhul võib ülesande vastuvõtnud inimene vabastada dokumendi tagasi tööüksuste järjekorda.</span><span class="sxs-lookup"><span data-stu-id="f3afb-152">In this case, the person who accepted the task can release the document back to the work item queue.</span></span> 

<span data-ttu-id="f3afb-153">Näiteks Julie, ettevõtte Adventure Works kuluaruannete osakonna liige, on võtnud vastu ülesande vaadata üle Sami kuluaruanne ja kviitungid.</span><span class="sxs-lookup"><span data-stu-id="f3afb-153">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="f3afb-154">Kui Julie otsustab, et ta ei saa ülesannet lõpule viia, võib ta dokumendi vabastada.</span><span class="sxs-lookup"><span data-stu-id="f3afb-154">If Julie decides that she can't complete the task, she can release the document.</span></span> <span data-ttu-id="f3afb-155">Kuluaruanne tagastatakse järjekorda, et ettevõtte Adventure Works kuluaruannete osakonna teised liikmed saaksid ülesande täita.</span><span class="sxs-lookup"><span data-stu-id="f3afb-155">The expense report is returned to the queue, so that other members of the Adventure Works Expense Reports department can complete the task.</span></span>

## <a name="actions-that-a-decision-maker-can-perform"></a><span data-ttu-id="f3afb-156">Toimingud, mida otsustaja saab teha</span><span class="sxs-lookup"><span data-stu-id="f3afb-156">Actions that a decision maker can perform</span></span>
<span data-ttu-id="f3afb-157">Tavaliselt määratakse dokument otsustajale seetõttu, et selles on küsimus, millele otsustaja peab vastama.</span><span class="sxs-lookup"><span data-stu-id="f3afb-157">Typically, a document is assigned to a decision maker, because there is a question that the decision maker must answer.</span></span> <span data-ttu-id="f3afb-158">Küsimuse vastus on tavaliselt **Jah** või **Ei** või **Tõene** või **Väär**.</span><span class="sxs-lookup"><span data-stu-id="f3afb-158">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="f3afb-159">Kui otsustaja valikut ei tee, võib ta otsustamise delegeerida.</span><span class="sxs-lookup"><span data-stu-id="f3afb-159">If the decision maker doesn't select one of those choices, he or she can delegate the decision.</span></span>

### <a name="choice-1-or-choice-2"></a><span data-ttu-id="f3afb-160">\[Valik 1\] või \[Valik 2\]</span><span class="sxs-lookup"><span data-stu-id="f3afb-160">\[Choice 1\] or \[Choice 2\]</span></span>

<span data-ttu-id="f3afb-161">Otsustaja peab dokumendiga seotud küsimusele vastama.</span><span class="sxs-lookup"><span data-stu-id="f3afb-161">A decision maker must answer a question that is related to the document.</span></span> <span data-ttu-id="f3afb-162">Küsimuse vastus on tavaliselt **Jah** või **Ei** või **Tõene** või **Väär**.</span><span class="sxs-lookup"><span data-stu-id="f3afb-162">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="f3afb-163">Otsustaja valitud vastus määrab dokumendi töötlemiseks kasutatava töövooharu.</span><span class="sxs-lookup"><span data-stu-id="f3afb-163">The answer that the decision maker selects determines the workflow branch that is used to process the document.</span></span> 

<span data-ttu-id="f3afb-164">Näiteks Sami kuluaruanne on määratud Johnile.</span><span class="sxs-lookup"><span data-stu-id="f3afb-164">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="f3afb-165">John peab otsustama, kas dokumendi teave nõuab Sami juhile helistamist.</span><span class="sxs-lookup"><span data-stu-id="f3afb-165">John must decide whether the information in the document requires a call to Sam's manager.</span></span> <span data-ttu-id="f3afb-166">Kui John leiab, et kõne on vajalik, määratakse kuluaruanne Arethale, kes peab siis Sami juhile helistama.</span><span class="sxs-lookup"><span data-stu-id="f3afb-166">If John decides that a call is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="f3afb-167">Kui John otsustab, et kõne pole vajalik, määratakse kuluaruanne Frankile kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="f3afb-167">If John decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

### <a name="delegate"></a><span data-ttu-id="f3afb-168">Delegeeri</span><span class="sxs-lookup"><span data-stu-id="f3afb-168">Delegate</span></span>

<span data-ttu-id="f3afb-169">Kui otsustaja otsuse delegeerib, määratakse dokument teisele kasutajale, kes peab otsuse langetama.</span><span class="sxs-lookup"><span data-stu-id="f3afb-169">When a decision maker delegates a decision, the document is assigned to another user who must make the decision.</span></span> 

<span data-ttu-id="f3afb-170">Näiteks Sami kuluaruanne on määratud Johnile.</span><span class="sxs-lookup"><span data-stu-id="f3afb-170">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="f3afb-171">John delegeerib otsustamise Mariale, kes on tema assistent.</span><span class="sxs-lookup"><span data-stu-id="f3afb-171">John delegates the decision to Maria, who is his assistant.</span></span> 

<span data-ttu-id="f3afb-172">Maria tegutseb seejärel Johni nimel.</span><span class="sxs-lookup"><span data-stu-id="f3afb-172">Maria then acts on behalf of John.</span></span> <span data-ttu-id="f3afb-173">Kui Maria leiab, et kõne Sami juhile on vajalik, määratakse kuluaruanne Arethale, kes peab siis Sami juhile helistama.</span><span class="sxs-lookup"><span data-stu-id="f3afb-173">If Maria decides that a call to Sam's manager is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="f3afb-174">Kui Maria otsustab, et kõne pole vajalik, määratakse kuluaruanne Frankile kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="f3afb-174">If Maria decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

## <a name="actions-that-an-approver-can-perform"></a><span data-ttu-id="f3afb-175">Toimingud, mida kinnitaja saab teha</span><span class="sxs-lookup"><span data-stu-id="f3afb-175">Actions that an approver can perform</span></span>
<span data-ttu-id="f3afb-176">Kui dokument määratakse kinnitajale, saab kinnitaja teha ühe järgmistest toimingutest: kinnitada, tagasi lükata, delegeerida või paluda muutmist.</span><span class="sxs-lookup"><span data-stu-id="f3afb-176">When a document is assigned to an approver, the approver can perform one of the following actions: approve, reject, delegate, or request change.</span></span>

### <a name="approve"></a><span data-ttu-id="f3afb-177">Kinnitamine</span><span class="sxs-lookup"><span data-stu-id="f3afb-177">Approve</span></span>

<span data-ttu-id="f3afb-178">Kui kinnitaja kinnitab dokumendi, määratakse see vajadusel järgmisele töövoo kasutajale, kui järgmine kasutaja on olemas.</span><span class="sxs-lookup"><span data-stu-id="f3afb-178">When an approver approves a document, the document is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="f3afb-179">Kui rohkem töötlemist ei ole vaja, siis töövoo protsess lõpeb.</span><span class="sxs-lookup"><span data-stu-id="f3afb-179">If no additional processing is required, the workflow process ends.</span></span> 

<span data-ttu-id="f3afb-180">Näiteks Sam on esitanud kuluaruande väärtuses USD 6000 ja see dokument on määratud Frankile.</span><span class="sxs-lookup"><span data-stu-id="f3afb-180">For example, Sam has submitted an expense report for USD 6,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="f3afb-181">Kui Frank kinnitab dokumendi, määratakse see Suele kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="f3afb-181">When Frank approves the document, it's assigned to Sue for approval.</span></span> <span data-ttu-id="f3afb-182">Kui Sue on kuluaruande kinnitanud, siis töövoo protsess lõpeb.</span><span class="sxs-lookup"><span data-stu-id="f3afb-182">When Sue approves the expense report, the workflow process ends.</span></span>

### <a name="reject"></a><span data-ttu-id="f3afb-183">Lükka tagasi</span><span class="sxs-lookup"><span data-stu-id="f3afb-183">Reject</span></span>

<span data-ttu-id="f3afb-184">Kui kinnitaja lükkab dokumendi tagasi, lõpeb töövoo protsess.</span><span class="sxs-lookup"><span data-stu-id="f3afb-184">When an approver rejects a document, the workflow process ends.</span></span> 

<span data-ttu-id="f3afb-185">Näiteks Sam on esitanud kuluaruande väärtuses USD 12 000 ja see dokument on määratud Suele.</span><span class="sxs-lookup"><span data-stu-id="f3afb-185">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="f3afb-186">Kui Sue selle kuluaruande tagasi lükkab, lõpeb töövoog.</span><span class="sxs-lookup"><span data-stu-id="f3afb-186">If Sue rejects the expense report, the workflow process ends.</span></span> 

<span data-ttu-id="f3afb-187">Sam saab kuluaruande uuesti esitada.</span><span class="sxs-lookup"><span data-stu-id="f3afb-187">Sam can resubmit the expense report.</span></span> <span data-ttu-id="f3afb-188">Ta võib teha esmalt muudatused või edastada uuesti kuluaruande algse versiooni.</span><span class="sxs-lookup"><span data-stu-id="f3afb-188">He can make changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="f3afb-189">Kui Sam taasesitab kuluaruande, käivitatakse kinnitusprotsess uuesti.</span><span class="sxs-lookup"><span data-stu-id="f3afb-189">If Sam resubmits the expense report, the workflow process starts at the approval process.</span></span>

### <a name="delegate"></a><span data-ttu-id="f3afb-190">Delegeeri</span><span class="sxs-lookup"><span data-stu-id="f3afb-190">Delegate</span></span>

<span data-ttu-id="f3afb-191">Kui kinnitaja delegeerib dokumendi, määratakse dokument kinnitamiseks teisele kasutajale.</span><span class="sxs-lookup"><span data-stu-id="f3afb-191">When an approver delegates a document, the document is assigned to another user for approval.</span></span> 

<span data-ttu-id="f3afb-192">Näiteks Sam on esitanud kuluaruande väärtuses USD 12,000 ja see dokument on määratud Frankile.</span><span class="sxs-lookup"><span data-stu-id="f3afb-192">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="f3afb-193">Frank delegeerib kuluaruande Annile.</span><span class="sxs-lookup"><span data-stu-id="f3afb-193">Frank delegates the expense report to Ann.</span></span> 

<span data-ttu-id="f3afb-194">Ann tegutseb seejärel Franki nimel.</span><span class="sxs-lookup"><span data-stu-id="f3afb-194">Ann then acts on behalf of Frank.</span></span> <span data-ttu-id="f3afb-195">Seetõttu, kui Ann kinnitab dokumendi, määratakse see Suele kinnitamiseks, täpselt nagu Frank oleks pidanud seda kinnitama.</span><span class="sxs-lookup"><span data-stu-id="f3afb-195">Therefore, when Ann approves the document, it's assigned to Sue for approval, just as if Frank had approved it.</span></span> <span data-ttu-id="f3afb-196">Kui Sue on dokumendi kinnitanud, saadetakse see Annile kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="f3afb-196">After Sue approves the document, it's sent to Ann for approval.</span></span>

### <a name="request-change"></a><span data-ttu-id="f3afb-197">Taotle muudatust</span><span class="sxs-lookup"><span data-stu-id="f3afb-197">Request change</span></span>

<span data-ttu-id="f3afb-198">Kui kinnitaja taotleb dokumendi muutmist, saadetakse dokument tagasi algatajale.</span><span class="sxs-lookup"><span data-stu-id="f3afb-198">When an approver requests a change to a document, the document is sent back to the originator.</span></span> 

<span data-ttu-id="f3afb-199">Näiteks Sam on esitanud kuluaruande väärtuses USD 12 000 ja see dokument on määratud Suele.</span><span class="sxs-lookup"><span data-stu-id="f3afb-199">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="f3afb-200">Kui Sue soovib muutmist, saadetakse kuluaruanne tagasi Samile.</span><span class="sxs-lookup"><span data-stu-id="f3afb-200">If Sue requests a change, the expense report is sent back to Sam.</span></span> 

<span data-ttu-id="f3afb-201">Sam saab kuluaruande uuesti esitada.</span><span class="sxs-lookup"><span data-stu-id="f3afb-201">Sam can resubmit the expense report.</span></span> <span data-ttu-id="f3afb-202">Ta võib teha esmalt soovitud muudatused või edastada uuesti kuluaruande algse versiooni.</span><span class="sxs-lookup"><span data-stu-id="f3afb-202">He can make the requested changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="f3afb-203">Kui Sam taasesitab kuluaruande, saadetakse see Frankile kinnitamiseks, sest Frank on selle kinnitamisprotsessi esimene kinnitaja.</span><span class="sxs-lookup"><span data-stu-id="f3afb-203">If Sam resubmits the expense report, it's sent to Frank for approval, because Frank is the first approver in the approval process.</span></span>




