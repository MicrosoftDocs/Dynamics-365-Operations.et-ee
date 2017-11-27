---
title: "Hangete töövood"
description: "Mõned organisatsioonid nõuavad, et ostutaotlused ja ostutellimused kinnitaks muu kasutaja kui see, kes kande sisestas. Kinnitamisprotsessi seadistamiseks saate luua töövoo."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3bf244786e308ebcaee27a16fae378f41086f963
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="0d777-104">Hangete töövood</span><span class="sxs-lookup"><span data-stu-id="0d777-104">Procurement and sourcing workflows</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0d777-105">Mõned organisatsioonid nõuavad, et ostutaotlused ja ostutellimused kinnitaks muu kasutaja kui see, kes kande sisestas.</span><span class="sxs-lookup"><span data-stu-id="0d777-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="0d777-106">Kinnitamisprotsessi seadistamiseks saate luua töövoo.</span><span class="sxs-lookup"><span data-stu-id="0d777-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="0d777-107">Töövoog esindab äriprotsessi.</span><span class="sxs-lookup"><span data-stu-id="0d777-107">A workflow represents a business process.</span></span> <span data-ttu-id="0d777-108">Töövoog määrab, kuidas dokument voogab läbi süsteemi, näidates, kes peab seda töötlema ja kinnitama.</span><span class="sxs-lookup"><span data-stu-id="0d777-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="0d777-109">Töövoo süsteemi kasutamine teie organisatsioonis on mitmeti kasulik.</span><span class="sxs-lookup"><span data-stu-id="0d777-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="0d777-110">**Järjepidevad protsessid** — töövoo süsteem lubab teil määratleda kinnitusprotsessi kindlatele dokumentidele nagu näiteks ostutaotlused ja kuluaruanded.</span><span class="sxs-lookup"><span data-stu-id="0d777-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="0d777-111">Töövoo süsteemi abil tagate, et dokumente töödeldakse ja kinnitatakse järjekindlal ja tõhusal viisil.</span><span class="sxs-lookup"><span data-stu-id="0d777-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="0d777-112">**Protsessi nähtavus** — töövoo süsteem lubab teil jälgida kindla töövoo eksemplari olekut ja ajalugu.</span><span class="sxs-lookup"><span data-stu-id="0d777-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="0d777-113">See aitab teil määratleda, kas töövoos tuleks muudatusi tõhususe parandamiseks.</span><span class="sxs-lookup"><span data-stu-id="0d777-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="0d777-114">**Tööde koondloend** – kasutajad saavad vaadata tööde koondloendit, et näha neile määratud töövoo ülesandeid ja kinnitusi kõigis töövoogudes, milles nad osalevad.</span><span class="sxs-lookup"><span data-stu-id="0d777-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="0d777-115">See on saadaval lehel Tööüksused.</span><span class="sxs-lookup"><span data-stu-id="0d777-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="0d777-116"> Loodavate töövoogude tüübid</span><span class="sxs-lookup"><span data-stu-id="0d777-116">The types of workflows that you can create</span></span>
<span data-ttu-id="0d777-117">Jaotises Hanked on saadaval järgmised töövootüübid.</span><span class="sxs-lookup"><span data-stu-id="0d777-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="0d777-118">**Tüüp**</span><span class="sxs-lookup"><span data-stu-id="0d777-118">**Type**</span></span>                         | <span data-ttu-id="0d777-119">**Kasutage seda tüüpi järgmiseks**</span><span class="sxs-lookup"><span data-stu-id="0d777-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="0d777-120">Ostutaotluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="0d777-120">Purchase requisition review</span></span>      | <span data-ttu-id="0d777-121">Saate luua ülevaatuse töövoogusid ostutaotluste jaoks.</span><span class="sxs-lookup"><span data-stu-id="0d777-121">Create review workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="0d777-122">Ostutaotluse rea eelvaade</span><span class="sxs-lookup"><span data-stu-id="0d777-122">Purchase requisition line review</span></span> | <span data-ttu-id="0d777-123">Saate luua ülevaatuse töövoogusid ostutaotluse ridade jaoks.</span><span class="sxs-lookup"><span data-stu-id="0d777-123">Create review workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="0d777-124">Ostutellimuse töövoog</span><span class="sxs-lookup"><span data-stu-id="0d777-124">Purchase order workflow</span></span>          | <span data-ttu-id="0d777-125">Saate luua ülevaatuse ja kinnitamise töövoogusid ostutellimuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="0d777-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="0d777-126">Ostutellimuse rea töövoog</span><span class="sxs-lookup"><span data-stu-id="0d777-126">Purchase order line workflow</span></span>     | <span data-ttu-id="0d777-127">Saate luua ülevaatuse ja kinnitamise töövoogusid ostutellimuse ridade jaoks.</span><span class="sxs-lookup"><span data-stu-id="0d777-127">Create review and approve workflows for purchase order lines.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="0d777-128">Töövoo loomine</span><span class="sxs-lookup"><span data-stu-id="0d777-128">Creating a workflow</span></span>
<span data-ttu-id="0d777-129">Töövoo loomiseks minge jaotisse Hanked &gt; Seadistus &gt; Hangete töövood ja looge uus töövoog, valides loodava töövoo tüübi.</span><span class="sxs-lookup"><span data-stu-id="0d777-129">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="0d777-130">Töövoo lõuendil saate lohistada töövoo elemendid kujundajasse ja linkida need voogu.</span><span class="sxs-lookup"><span data-stu-id="0d777-130">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="0d777-131">Töövoo elemendid peavad olema konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="0d777-131">The workflow elements should be configured.</span></span> <span data-ttu-id="0d777-132">Kinnitus- ja ülesandetöövoo elementide puhul saate konfigureerida, milline osaleja peaks tegutsema.</span><span class="sxs-lookup"><span data-stu-id="0d777-132">For approval and task workflow elements you can configure which participant should take action.</span></span>
<span data-ttu-id="0d777-133">Osalejate tüübid</span><span class="sxs-lookup"><span data-stu-id="0d777-133">Types of participants</span></span>
----------------------

<span data-ttu-id="0d777-134">Saate määrata kinnitamisetapi järgmistele osalejate gruppidele.</span><span class="sxs-lookup"><span data-stu-id="0d777-134">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="0d777-135">Kasutajagrupp</span><span class="sxs-lookup"><span data-stu-id="0d777-135">User group</span></span>    | <span data-ttu-id="0d777-136">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0d777-136">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="0d777-137">Osaleja</span><span class="sxs-lookup"><span data-stu-id="0d777-137">Participant</span></span>   | <span data-ttu-id="0d777-138">Määrake kinnitamisetapp grupi või rolli liikmetele.</span><span class="sxs-lookup"><span data-stu-id="0d777-138">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="0d777-139">Hierarhia</span><span class="sxs-lookup"><span data-stu-id="0d777-139">Hierarchy</span></span>     | <span data-ttu-id="0d777-140">Määrake kinnitamisetapp teatud organisatsioonihierarhia kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="0d777-140">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="0d777-141">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="0d777-141">Workflow user</span></span> | <span data-ttu-id="0d777-142">Määrake kinnitamisetapp selle töövoo kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="0d777-142">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="0d777-143">Järjekord</span><span class="sxs-lookup"><span data-stu-id="0d777-143">Queue</span></span>         | <span data-ttu-id="0d777-144">Määrake kinnitusetapp tööüksuste järjekorda.</span><span class="sxs-lookup"><span data-stu-id="0d777-144">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="0d777-145">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="0d777-145">User</span></span>          | <span data-ttu-id="0d777-146">Määrake kinnitamisetapp konkreetsetele kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="0d777-146">Assign the approval step to specific users.</span></span>                               |



<a name="see-also"></a><span data-ttu-id="0d777-147">Vt ka</span><span class="sxs-lookup"><span data-stu-id="0d777-147">See also</span></span>
--------

[<span data-ttu-id="0d777-148">Äriprotsessi töövoogude määratlemine ostutaotluste jaoks</span><span class="sxs-lookup"><span data-stu-id="0d777-148">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[<span data-ttu-id="0d777-149">Ostutaotluse töövoog</span><span class="sxs-lookup"><span data-stu-id="0d777-149">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)




