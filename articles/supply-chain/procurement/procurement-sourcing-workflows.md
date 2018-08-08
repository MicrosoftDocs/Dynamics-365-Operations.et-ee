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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 06ab745d9df9b095b861cf7bc79aba6d1361eeb0
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---

# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="8fdc8-104">Hangete töövood</span><span class="sxs-lookup"><span data-stu-id="8fdc8-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fdc8-105">Mõned organisatsioonid nõuavad, et ostutaotlused ja ostutellimused kinnitaks muu kasutaja kui see, kes kande sisestas.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="8fdc8-106">Kinnitamisprotsessi seadistamiseks saate luua töövoo.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="8fdc8-107">Töövoog esindab äriprotsessi.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-107">A workflow represents a business process.</span></span> <span data-ttu-id="8fdc8-108">Töövoog määrab, kuidas dokument voogab läbi süsteemi, näidates, kes peab seda töötlema ja kinnitama.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="8fdc8-109">Töövoo süsteemi kasutamine teie organisatsioonis on mitmeti kasulik.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="8fdc8-110">**Järjepidevad protsessid** — töövoo süsteem lubab teil määratleda kinnitusprotsessi kindlatele dokumentidele nagu näiteks ostutaotlused ja kuluaruanded.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="8fdc8-111">Töövoo süsteemi abil tagate, et dokumente töödeldakse ja kinnitatakse järjekindlal ja tõhusal viisil.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="8fdc8-112">**Protsessi nähtavus** — töövoo süsteem lubab teil jälgida kindla töövoo eksemplari olekut ja ajalugu.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="8fdc8-113">See aitab teil määratleda, kas töövoos tuleks muudatusi tõhususe parandamiseks.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="8fdc8-114">**Tööde koondloend** – kasutajad saavad vaadata tööde koondloendit, et näha neile määratud töövoo ülesandeid ja kinnitusi kõigis töövoogudes, milles nad osalevad.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="8fdc8-115">See on saadaval lehel Tööüksused.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="8fdc8-116"> Loodavate töövoogude tüübid</span><span class="sxs-lookup"><span data-stu-id="8fdc8-116">The types of workflows that you can create</span></span>
<span data-ttu-id="8fdc8-117">Jaotises Hanked on saadaval järgmised töövootüübid.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8fdc8-118">**Tüüp**</span><span class="sxs-lookup"><span data-stu-id="8fdc8-118">**Type**</span></span>                         | <span data-ttu-id="8fdc8-119">**Kasutage seda tüüpi järgmiseks**</span><span class="sxs-lookup"><span data-stu-id="8fdc8-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="8fdc8-120">Ostutaotluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="8fdc8-120">Purchase requisition review</span></span>      | <span data-ttu-id="8fdc8-121">Saate luua ostutaotluste jaoks ülevaatuse ja kinnitamise töövood.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-121">Create review and approval workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="8fdc8-122">Ostutaotluse rea eelvaade</span><span class="sxs-lookup"><span data-stu-id="8fdc8-122">Purchase requisition line review</span></span> | <span data-ttu-id="8fdc8-123">Saate luua ostutaotluse ridade jaoks ülevaatuse ja kinnitamise töövood.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-123">Create review and approval workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="8fdc8-124">Ostutellimuse töövoog</span><span class="sxs-lookup"><span data-stu-id="8fdc8-124">Purchase order workflow</span></span>          | <span data-ttu-id="8fdc8-125">Saate luua ülevaatuse ja kinnitamise töövoogusid ostutellimuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="8fdc8-126">Ostutellimuse rea töövoog</span><span class="sxs-lookup"><span data-stu-id="8fdc8-126">Purchase order line workflow</span></span>     | <span data-ttu-id="8fdc8-127">Saate luua ülevaatuse ja kinnitamise töövoogusid ostutellimuse ridade jaoks.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="8fdc8-128">Hankija lisamise rakenduse töövoog</span><span class="sxs-lookup"><span data-stu-id="8fdc8-128">Vendor add application workflow</span></span>  | <span data-ttu-id="8fdc8-129">Saate luua ülevaatuse ja kinnitamise töövood uute hankijate lisamiseks hankija nõuete kaudu.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="8fdc8-130">Töövoo loomine</span><span class="sxs-lookup"><span data-stu-id="8fdc8-130">Creating a workflow</span></span>
<span data-ttu-id="8fdc8-131">Töövoo loomiseks minge jaotisse Hanked &gt; Seadistus &gt; Hangete töövood ja looge uus töövoog, valides loodava töövoo tüübi.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-131">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="8fdc8-132">Töövoo lõuendil saate lohistada töövoo elemendid kujundajasse ja linkida need voogu.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-132">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="8fdc8-133">Töövoo elemendid peavad olema konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-133">The workflow elements should be configured.</span></span> <span data-ttu-id="8fdc8-134">Kinnitus- ja ülesandetöövoo elementide puhul saate konfigureerida, milline osaleja peaks tegutsema.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-134">For approval and task workflow elements you can configure which participant should take action.</span></span>
<span data-ttu-id="8fdc8-135">Osalejate tüübid</span><span class="sxs-lookup"><span data-stu-id="8fdc8-135">Types of participants</span></span>
----------------------

<span data-ttu-id="8fdc8-136">Saate määrata kinnitamisetapi järgmistele osalejate gruppidele.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-136">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="8fdc8-137">Kasutajagrupp</span><span class="sxs-lookup"><span data-stu-id="8fdc8-137">User group</span></span>    | <span data-ttu-id="8fdc8-138">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8fdc8-138">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="8fdc8-139">Osaleja</span><span class="sxs-lookup"><span data-stu-id="8fdc8-139">Participant</span></span>   | <span data-ttu-id="8fdc8-140">Määrake kinnitamisetapp grupi või rolli liikmetele.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-140">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="8fdc8-141">Hierarhia</span><span class="sxs-lookup"><span data-stu-id="8fdc8-141">Hierarchy</span></span>     | <span data-ttu-id="8fdc8-142">Määrake kinnitamisetapp teatud organisatsioonihierarhia kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-142">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="8fdc8-143">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="8fdc8-143">Workflow user</span></span> | <span data-ttu-id="8fdc8-144">Määrake kinnitamisetapp selle töövoo kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-144">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="8fdc8-145">Järjekord</span><span class="sxs-lookup"><span data-stu-id="8fdc8-145">Queue</span></span>         | <span data-ttu-id="8fdc8-146">Määrake kinnitusetapp tööüksuste järjekorda.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-146">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="8fdc8-147">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="8fdc8-147">User</span></span>          | <span data-ttu-id="8fdc8-148">Määrake kinnitamisetapp konkreetsetele kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="8fdc8-148">Assign the approval step to specific users.</span></span>                               |



<a name="additional-resources"></a><span data-ttu-id="8fdc8-149">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="8fdc8-149">Additional resources</span></span>
--------

[<span data-ttu-id="8fdc8-150">Äriprotsessi töövoogude määratlemine ostutaotluste jaoks</span><span class="sxs-lookup"><span data-stu-id="8fdc8-150">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[<span data-ttu-id="8fdc8-151">Ostutaotluse töövoog</span><span class="sxs-lookup"><span data-stu-id="8fdc8-151">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)

[<span data-ttu-id="8fdc8-152">Hankijate sotsialiseerimine</span><span class="sxs-lookup"><span data-stu-id="8fdc8-152">Onboarding vendors</span></span>](vendor-onboarding.md)


