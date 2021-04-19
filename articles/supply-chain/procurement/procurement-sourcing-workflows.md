---
title: Hangete töövood
description: Mõned organisatsioonid nõuavad, et ostutaotlused ja ostutellimused kinnitaks muu kasutaja kui see, kes kande sisestas. Kinnitamisprotsessi seadistamiseks saate luua töövoo.
author: kamaybac
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd9ee69e180f2ff605c4f373a95d2346ccc73c0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807940"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="2de32-104">Hangete töövood</span><span class="sxs-lookup"><span data-stu-id="2de32-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2de32-105">Mõned organisatsioonid nõuavad, et ostutaotlused ja ostutellimused kinnitaks muu kasutaja kui see, kes kande sisestas.</span><span class="sxs-lookup"><span data-stu-id="2de32-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="2de32-106">Kinnitamisprotsessi seadistamiseks saate luua töövoo.</span><span class="sxs-lookup"><span data-stu-id="2de32-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="2de32-107">Töövoog esindab äriprotsessi.</span><span class="sxs-lookup"><span data-stu-id="2de32-107">A workflow represents a business process.</span></span> <span data-ttu-id="2de32-108">Töövoog määrab, kuidas dokument voogab läbi süsteemi, näidates, kes peab seda töötlema ja kinnitama.</span><span class="sxs-lookup"><span data-stu-id="2de32-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="2de32-109">Töövoo süsteemi kasutamine teie organisatsioonis on mitmeti kasulik.</span><span class="sxs-lookup"><span data-stu-id="2de32-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="2de32-110">**Järjepidevad protsessid** — töövoo süsteem lubab teil määratleda kinnitusprotsessi kindlatele dokumentidele nagu näiteks ostutaotlused ja kuluaruanded.</span><span class="sxs-lookup"><span data-stu-id="2de32-110">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="2de32-111">Töövoo süsteemi abil tagate, et dokumente töödeldakse ja kinnitatakse järjekindlal ja tõhusal viisil.</span><span class="sxs-lookup"><span data-stu-id="2de32-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="2de32-112">**Protsessi nähtavus** — töövoo süsteem lubab teil jälgida kindla töövoo eksemplari olekut ja ajalugu.</span><span class="sxs-lookup"><span data-stu-id="2de32-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="2de32-113">See aitab teil määratleda, kas töövoos tuleks muudatusi tõhususe parandamiseks.</span><span class="sxs-lookup"><span data-stu-id="2de32-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="2de32-114">**Tööde koondloend** – kasutajad saavad vaadata tööde koondloendit, et näha neile määratud töövoo ülesandeid ja kinnitusi kõigis töövoogudes, milles nad osalevad.</span><span class="sxs-lookup"><span data-stu-id="2de32-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="2de32-115">See on saadaval lehel Tööüksused.</span><span class="sxs-lookup"><span data-stu-id="2de32-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="2de32-116"> Loodavate töövoogude tüübid</span><span class="sxs-lookup"><span data-stu-id="2de32-116">The types of workflows that you can create</span></span>

<span data-ttu-id="2de32-117">Jaotises Hanked on saadaval järgmised töövootüübid.</span><span class="sxs-lookup"><span data-stu-id="2de32-117">The following workflow types are available for Procurement and sourcing.</span></span>

| <span data-ttu-id="2de32-118">Tüüp</span><span class="sxs-lookup"><span data-stu-id="2de32-118">Type</span></span> | <span data-ttu-id="2de32-119">Kasutage seda tüüpi järgmiseks</span><span class="sxs-lookup"><span data-stu-id="2de32-119">Use this type to</span></span> |
|---|---|
| <span data-ttu-id="2de32-120">Ostutaotluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="2de32-120">Purchase requisition review</span></span> | <span data-ttu-id="2de32-121">Saate luua ostutaotluste jaoks ülevaatuse ja kinnitamise töövood.</span><span class="sxs-lookup"><span data-stu-id="2de32-121">Create review and approval workflows for purchase requisitions.</span></span> |
| <span data-ttu-id="2de32-122">Ostutaotluse rea eelvaade</span><span class="sxs-lookup"><span data-stu-id="2de32-122">Purchase requisition line review</span></span> | <span data-ttu-id="2de32-123">Saate luua ostutaotluse ridade jaoks ülevaatuse ja kinnitamise töövood.</span><span class="sxs-lookup"><span data-stu-id="2de32-123">Create review and approval workflows for purchase requisition lines.</span></span> |
| <span data-ttu-id="2de32-124">Ostutellimuse töövoog</span><span class="sxs-lookup"><span data-stu-id="2de32-124">Purchase order workflow</span></span> | <span data-ttu-id="2de32-125">Saate luua ülevaatuse ja kinnitamise töövoogusid ostutellimuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="2de32-125">Create review and approval workflows for purchase orders.</span></span> |
| <span data-ttu-id="2de32-126">Ostutellimuse rea töövoog</span><span class="sxs-lookup"><span data-stu-id="2de32-126">Purchase order line workflow</span></span> | <span data-ttu-id="2de32-127">Saate luua ülevaatuse ja kinnitamise töövoogusid ostutellimuse ridade jaoks.</span><span class="sxs-lookup"><span data-stu-id="2de32-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="2de32-128">Hankija lisamise rakenduse töövoog</span><span class="sxs-lookup"><span data-stu-id="2de32-128">Vendor add application workflow</span></span> | <span data-ttu-id="2de32-129">Saate luua ülevaatuse ja kinnitamise töövood uute hankijate lisamiseks hankija nõuete kaudu.</span><span class="sxs-lookup"><span data-stu-id="2de32-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="2de32-130">Uue töövoo lisamisel võidakse kuvada ka järgmised iganenud töövood, mis on loetletud dialoogiboksis **Töövoo loomine**.</span><span class="sxs-lookup"><span data-stu-id="2de32-130">When you are adding a new workflow, you might also see the following obsolete workflows listed in the **Create workflow** dialog box.</span></span> <span data-ttu-id="2de32-131">Need on seotud *vastuvõtukinnituse* funktsiooniga, mis oli saadaval teenuses [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), aga mis on nüüd iganenud.</span><span class="sxs-lookup"><span data-stu-id="2de32-131">These are related to the *confirmation of receipt* functionality that was available in [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), but which has now been deprecated.</span></span> <span data-ttu-id="2de32-132">Neid töövooge praegu ei toetata.</span><span class="sxs-lookup"><span data-stu-id="2de32-132">These workflows are currently unsupported.</span></span>
> 
> - <span data-ttu-id="2de32-133">Tarnetähtaja teate töövoog</span><span class="sxs-lookup"><span data-stu-id="2de32-133">Delivery due date notification workflow</span></span>
> - <span data-ttu-id="2de32-134">Arve saamise teatise töövoog</span><span class="sxs-lookup"><span data-stu-id="2de32-134">Invoice received notification workflow</span></span>
> - <span data-ttu-id="2de32-135">Toote sissetuleku nurjunud teatise töövoog</span><span class="sxs-lookup"><span data-stu-id="2de32-135">Product receipt failed notification workflow</span></span>
> - <span data-ttu-id="2de32-136">Kinnitamata toote sissetuleku tagasilükkamise teatise töövoog</span><span class="sxs-lookup"><span data-stu-id="2de32-136">Unconfirmed product receipt rejection notification workflow</span></span>

## <a name="creating-a-workflow"></a><span data-ttu-id="2de32-137">Töövoo loomine</span><span class="sxs-lookup"><span data-stu-id="2de32-137">Creating a workflow</span></span>

<span data-ttu-id="2de32-138">Töövoo loomiseks minge jaotisse Hanked &gt; Seadistus &gt; Hangete töövood ja looge uus töövoog, valides loodava töövoo tüübi.</span><span class="sxs-lookup"><span data-stu-id="2de32-138">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span> 

<span data-ttu-id="2de32-139">Töövoo lõuendil saate lohistada töövoo elemendid kujundajasse ja linkida need voogu.</span><span class="sxs-lookup"><span data-stu-id="2de32-139">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="2de32-140">Töövoo elemendid peavad olema konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="2de32-140">The workflow elements should be configured.</span></span> <span data-ttu-id="2de32-141">Kinnitus- ja ülesandetöövoo elementide puhul saate konfigureerida, milline osaleja peaks tegutsema.</span><span class="sxs-lookup"><span data-stu-id="2de32-141">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="2de32-142">Osalejate tüübid</span><span class="sxs-lookup"><span data-stu-id="2de32-142">Types of participants</span></span>

<span data-ttu-id="2de32-143">Saate määrata kinnitamisetapi järgmistele osalejate gruppidele.</span><span class="sxs-lookup"><span data-stu-id="2de32-143">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="2de32-144">Kasutajagrupp</span><span class="sxs-lookup"><span data-stu-id="2de32-144">User group</span></span> | <span data-ttu-id="2de32-145">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2de32-145">Description</span></span> |
|---|---|
| <span data-ttu-id="2de32-146">Osaleja</span><span class="sxs-lookup"><span data-stu-id="2de32-146">Participant</span></span> | <span data-ttu-id="2de32-147">Määrake kinnitamisetapp grupi või rolli liikmetele.</span><span class="sxs-lookup"><span data-stu-id="2de32-147">Assign the approval step to members of a group or role.</span></span> |
| <span data-ttu-id="2de32-148">Hierarhia</span><span class="sxs-lookup"><span data-stu-id="2de32-148">Hierarchy</span></span> | <span data-ttu-id="2de32-149">Määrake kinnitamisetapp teatud organisatsioonihierarhia kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="2de32-149">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="2de32-150">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="2de32-150">Workflow user</span></span> | <span data-ttu-id="2de32-151">Määrake kinnitamisetapp selle töövoo kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="2de32-151">Assign the approval step to users of this workflow.</span></span> |
| <span data-ttu-id="2de32-152">Järjekord</span><span class="sxs-lookup"><span data-stu-id="2de32-152">Queue</span></span> | <span data-ttu-id="2de32-153">Määrake kinnitusetapp tööüksuste järjekorda.</span><span class="sxs-lookup"><span data-stu-id="2de32-153">Assign the approval step to a work item queue.</span></span> |
| <span data-ttu-id="2de32-154">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="2de32-154">User</span></span> | <span data-ttu-id="2de32-155">Määrake kinnitamisetapp konkreetsetele kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="2de32-155">Assign the approval step to specific users.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="2de32-156">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2de32-156">Additional resources</span></span>

- [<span data-ttu-id="2de32-157">Äriprotsessi töövoogude määratlemine ostutaotluste jaoks</span><span class="sxs-lookup"><span data-stu-id="2de32-157">Defining business process workflows for purchase requisitions</span></span>](https://www.microsoft.com/download/details.aspx?id=101821)
- [<span data-ttu-id="2de32-158">Ostutaotluse töövoog</span><span class="sxs-lookup"><span data-stu-id="2de32-158">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)
- [<span data-ttu-id="2de32-159">Hankijate vastuvõtmine</span><span class="sxs-lookup"><span data-stu-id="2de32-159">Onboard vendors</span></span>](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]