---
title: "Kanbani ülekandmise tahvli tugi vöötkoodilugejatele"
description: "Kanbani ülekandmise tahvel toetab vöötkoodiskanneri vidina sisendit toiminguteks Vali, Käivita, Lõpeta ja Tühjenda kanban-töö."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 29ad077cd10b0fa5967d145740f63051b05ad009
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="5a42b-103">Kanbani ülekandmise tahvli tugi vöötkoodilugejatele</span><span class="sxs-lookup"><span data-stu-id="5a42b-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a42b-104">Kanbani ülekandmise tahvel toetab vöötkoodiskanneri vidina sisendit toiminguteks Vali, Käivita, Lõpeta ja Tühjenda kanban-töö.</span><span class="sxs-lookup"><span data-stu-id="5a42b-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="5a42b-105">Registreerimisrežiimid</span><span class="sxs-lookup"><span data-stu-id="5a42b-105">Registration modes</span></span>
------------------

<span data-ttu-id="5a42b-106">Kiirkaardil **Skanneri registreerimine** saate valida registreerimisrežiimi, millega juhitakse tegevust, kui skannite kanban-kaardi numbri või sisestate numbri käsitsi väljale Kanban-kaardi number.</span><span class="sxs-lookup"><span data-stu-id="5a42b-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="5a42b-107">Registreerimisrežiimi määramine</span><span class="sxs-lookup"><span data-stu-id="5a42b-107">Set registration mode</span></span> | <span data-ttu-id="5a42b-108">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="5a42b-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a42b-109">Algus</span><span class="sxs-lookup"><span data-stu-id="5a42b-109">Start</span></span>                 | <span data-ttu-id="5a42b-110">Registreerib kanbani ülekandetöö pooleliolevana.</span><span class="sxs-lookup"><span data-stu-id="5a42b-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="5a42b-111">Lõpule viidud</span><span class="sxs-lookup"><span data-stu-id="5a42b-111">Complete</span></span>              | <span data-ttu-id="5a42b-112">Registreerib kanbani ülekandetöö lõpetatuna.</span><span class="sxs-lookup"><span data-stu-id="5a42b-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="5a42b-113">Tühi</span><span class="sxs-lookup"><span data-stu-id="5a42b-113">Empty</span></span>                 | <span data-ttu-id="5a42b-114">Registreerib kanban-kaardi viidatud materjali käsitlemisühiku tühjana.</span><span class="sxs-lookup"><span data-stu-id="5a42b-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="5a42b-115">Vali</span><span class="sxs-lookup"><span data-stu-id="5a42b-115">Select</span></span>                | <span data-ttu-id="5a42b-116">Registreerib kanban-kaardi numbri ja valib kanban-tööde loendist viidatud töö automaatselt.</span><span class="sxs-lookup"><span data-stu-id="5a42b-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="5a42b-117">Registreerimisrežiimi valimine</span><span class="sxs-lookup"><span data-stu-id="5a42b-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="5a42b-118">Kui kasutate töö valimiseks vöötkoodilugejat, muutub kanban-tahvli kuvarežiim.</span><span class="sxs-lookup"><span data-stu-id="5a42b-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="5a42b-119">Selles režiimis kehtivad järgmised tingimused.</span><span class="sxs-lookup"><span data-stu-id="5a42b-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="5a42b-120">Kuvatakse ainult skannitud kanban-töö.</span><span class="sxs-lookup"><span data-stu-id="5a42b-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="5a42b-121">Valitud töö üksikasjad kuvatakse kiirkaardil **Üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="5a42b-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="5a42b-122">Kiirkaardil **Teated** kuvatakse ainult teated valitud töö kohta.</span><span class="sxs-lookup"><span data-stu-id="5a42b-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="5a42b-123">Töö olekut saate muuta, kasutades funktsioone, mis on saadaval toimingupaanil.</span><span class="sxs-lookup"><span data-stu-id="5a42b-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="5a42b-124">Kanbani ülekandmise tahvlil kuvatakse sel ajal ainult üht tööd.</span><span class="sxs-lookup"><span data-stu-id="5a42b-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="5a42b-125">Saate värskendada tööde loendis olevat teavet käsitsi, klõpsates toimingupaanil käsku **Värskenda** (Shift + F5).</span><span class="sxs-lookup"><span data-stu-id="5a42b-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="5a42b-126">Pärast teabe värskendamist kuvatakse uuesti töö filtri täielikud tulemused.</span><span class="sxs-lookup"><span data-stu-id="5a42b-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="5a42b-127">Töö olek ja võimalikud tegevused</span><span class="sxs-lookup"><span data-stu-id="5a42b-127">Job status and possible actions</span></span>
<span data-ttu-id="5a42b-128">Valitud töö olek ja sündmuse kanbanide mis tahes kinnistatud tööde olek määravad, kas saate tööd edasi töödelda.</span><span class="sxs-lookup"><span data-stu-id="5a42b-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="5a42b-129">Järgmises tabelis kuvatakse teave nende olekute ja ülesannete kohta.</span><span class="sxs-lookup"><span data-stu-id="5a42b-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="5a42b-130">Tööde jaoks või tööde viidatud materjali käsitlemisühikute jaoks saadaolevad olekud.</span><span class="sxs-lookup"><span data-stu-id="5a42b-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="5a42b-131">Iga ülesanne, mida saate töö puhul täita.</span><span class="sxs-lookup"><span data-stu-id="5a42b-131">Each task that you can perform for the job.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5a42b-132">Töö tüüp</span><span class="sxs-lookup"><span data-stu-id="5a42b-132">Job type</span></span></th>
<th><span data-ttu-id="5a42b-133">Töö olek või materjali käsitlemisühiku olek</span><span class="sxs-lookup"><span data-stu-id="5a42b-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="5a42b-134">Komplekteerimislehe värskendamine</span><span class="sxs-lookup"><span data-stu-id="5a42b-134">Update picking list</span></span></th>
<th><span data-ttu-id="5a42b-135">Algus</span><span class="sxs-lookup"><span data-stu-id="5a42b-135">Start</span></span></th>
<th><span data-ttu-id="5a42b-136">Värskenda reserveeringut</span><span class="sxs-lookup"><span data-stu-id="5a42b-136">Update registration</span></span></th>
<th><span data-ttu-id="5a42b-137">Lõpule viidud</span><span class="sxs-lookup"><span data-stu-id="5a42b-137">Complete</span></span></th>
<th><span data-ttu-id="5a42b-138">Tühi</span><span class="sxs-lookup"><span data-stu-id="5a42b-138">Empty</span></span></th>
<th><span data-ttu-id="5a42b-139">Loo sündmuse kanbanid</span><span class="sxs-lookup"><span data-stu-id="5a42b-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5a42b-140">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="5a42b-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="5a42b-141">Pole plaanitud</span><span class="sxs-lookup"><span data-stu-id="5a42b-141">Not planned</span></span></li>
<li><span data-ttu-id="5a42b-142">Kinnistatud töid pole või on kinnistatud tööd lõpule viidud</span><span class="sxs-lookup"><span data-stu-id="5a42b-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="5a42b-143">Jah</span><span class="sxs-lookup"><span data-stu-id="5a42b-143">Yes</span></span></td>
<td><span data-ttu-id="5a42b-144">Jah</span><span class="sxs-lookup"><span data-stu-id="5a42b-144">Yes</span></span></td>
<td><span data-ttu-id="5a42b-145">Jah</span><span class="sxs-lookup"><span data-stu-id="5a42b-145">Yes</span></span></td>
<td><span data-ttu-id="5a42b-146">Jah</span><span class="sxs-lookup"><span data-stu-id="5a42b-146">Yes</span></span></td>
<td><span data-ttu-id="5a42b-147">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-147">No</span></span></td>
<td><span data-ttu-id="5a42b-148">Jah</span><span class="sxs-lookup"><span data-stu-id="5a42b-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a42b-149">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="5a42b-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="5a42b-150">Pole plaanitud</span><span class="sxs-lookup"><span data-stu-id="5a42b-150">Not planned</span></span></li>
<li><span data-ttu-id="5a42b-151">Kinnistatud töö ei ole lõpule viidud</span><span class="sxs-lookup"><span data-stu-id="5a42b-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="5a42b-152">Jah</span><span class="sxs-lookup"><span data-stu-id="5a42b-152">Yes</span></span></td>
<td><span data-ttu-id="5a42b-153">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-153">No</span></span></td>
<td><span data-ttu-id="5a42b-154">Jah</span><span class="sxs-lookup"><span data-stu-id="5a42b-154">Yes</span></span></td>
<td><span data-ttu-id="5a42b-155">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-155">No</span></span></td>
<td><span data-ttu-id="5a42b-156">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-156">No</span></span></td>
<td><span data-ttu-id="5a42b-157">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a42b-158">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="5a42b-158">Transfer</span></span></td>
<td><span data-ttu-id="5a42b-159">Käimas</span><span class="sxs-lookup"><span data-stu-id="5a42b-159">In progress</span></span></td>
<td><span data-ttu-id="5a42b-160">Jah</span><span class="sxs-lookup"><span data-stu-id="5a42b-160">Yes</span></span></td>
<td><span data-ttu-id="5a42b-161">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-161">No</span></span></td>
<td><span data-ttu-id="5a42b-162">Jah</span><span class="sxs-lookup"><span data-stu-id="5a42b-162">Yes</span></span></td>
<td><span data-ttu-id="5a42b-163">Jah</span><span class="sxs-lookup"><span data-stu-id="5a42b-163">Yes</span></span></td>
<td><span data-ttu-id="5a42b-164">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-164">No</span></span></td>
<td><span data-ttu-id="5a42b-165">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a42b-166">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="5a42b-166">Transfer</span></span></td>
<td><span data-ttu-id="5a42b-167">Valmis</span><span class="sxs-lookup"><span data-stu-id="5a42b-167">Completed</span></span></td>
<td><span data-ttu-id="5a42b-168">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-168">No</span></span></td>
<td><span data-ttu-id="5a42b-169">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-169">No</span></span></td>
<td><span data-ttu-id="5a42b-170">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-170">No</span></span></td>
<td><span data-ttu-id="5a42b-171">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-171">No</span></span></td>
<td><span data-ttu-id="5a42b-172">Jah</span><span class="sxs-lookup"><span data-stu-id="5a42b-172">Yes</span></span></td>
<td><span data-ttu-id="5a42b-173">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a42b-174">Ülekanne või protsess</span><span class="sxs-lookup"><span data-stu-id="5a42b-174">Transfer or process</span></span></td>
<td><span data-ttu-id="5a42b-175">Tühi</span><span class="sxs-lookup"><span data-stu-id="5a42b-175">Empty</span></span></td>
<td><span data-ttu-id="5a42b-176">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-176">No</span></span></td>
<td><span data-ttu-id="5a42b-177">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-177">No</span></span></td>
<td><span data-ttu-id="5a42b-178">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-178">No</span></span></td>
<td><span data-ttu-id="5a42b-179">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-179">No</span></span></td>
<td><span data-ttu-id="5a42b-180">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-180">No</span></span></td>
<td><span data-ttu-id="5a42b-181">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a42b-182">Ülekanne või protsess</span><span class="sxs-lookup"><span data-stu-id="5a42b-182">Transfer or process</span></span></td>
<td><span data-ttu-id="5a42b-183">Kanban-kaarti ei leitud</span><span class="sxs-lookup"><span data-stu-id="5a42b-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="5a42b-184">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-184">No</span></span></td>
<td><span data-ttu-id="5a42b-185">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-185">No</span></span></td>
<td><span data-ttu-id="5a42b-186">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-186">No</span></span></td>
<td><span data-ttu-id="5a42b-187">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-187">No</span></span></td>
<td><span data-ttu-id="5a42b-188">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-188">No</span></span></td>
<td><span data-ttu-id="5a42b-189">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a42b-190">Ülekanne või protsess</span><span class="sxs-lookup"><span data-stu-id="5a42b-190">Transfer or process</span></span></td>
<td><span data-ttu-id="5a42b-191">Kanban-kaart leiti, kuid see pole kanbanile määratud</span><span class="sxs-lookup"><span data-stu-id="5a42b-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="5a42b-192">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-192">No</span></span></td>
<td><span data-ttu-id="5a42b-193">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-193">No</span></span></td>
<td><span data-ttu-id="5a42b-194">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-194">No</span></span></td>
<td><span data-ttu-id="5a42b-195">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-195">No</span></span></td>
<td><span data-ttu-id="5a42b-196">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-196">No</span></span></td>
<td><span data-ttu-id="5a42b-197">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a42b-198">Protsess</span><span class="sxs-lookup"><span data-stu-id="5a42b-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="5a42b-199">Pole plaanitud</span><span class="sxs-lookup"><span data-stu-id="5a42b-199">Not planned</span></span></li>
<li><span data-ttu-id="5a42b-200">Ettevalmistatud</span><span class="sxs-lookup"><span data-stu-id="5a42b-200">Prepared</span></span></li>
<li><span data-ttu-id="5a42b-201">Käimas</span><span class="sxs-lookup"><span data-stu-id="5a42b-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="5a42b-202">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-202">No</span></span></td>
<td><span data-ttu-id="5a42b-203">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-203">No</span></span></td>
<td><span data-ttu-id="5a42b-204">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-204">No</span></span></td>
<td><span data-ttu-id="5a42b-205">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-205">No</span></span></td>
<td><span data-ttu-id="5a42b-206">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-206">No</span></span></td>
<td><span data-ttu-id="5a42b-207">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a42b-208">Protsess</span><span class="sxs-lookup"><span data-stu-id="5a42b-208">Process</span></span></td>
<td><span data-ttu-id="5a42b-209">Valmis</span><span class="sxs-lookup"><span data-stu-id="5a42b-209">Completed</span></span></td>
<td><span data-ttu-id="5a42b-210">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-210">No</span></span></td>
<td><span data-ttu-id="5a42b-211">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-211">No</span></span></td>
<td><span data-ttu-id="5a42b-212">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-212">No</span></span></td>
<td><span data-ttu-id="5a42b-213">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-213">No</span></span></td>
<td><span data-ttu-id="5a42b-214">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-214">No</span></span></td>
<td><span data-ttu-id="5a42b-215">Ei</span><span class="sxs-lookup"><span data-stu-id="5a42b-215">No</span></span></td>
</tr>
</tbody>
</table>






