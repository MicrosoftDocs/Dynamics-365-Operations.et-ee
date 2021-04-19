---
title: Kanbani ülekandmise tahvli tugi vöötkoodilugejatele
description: Kanbani ülekandmise tahvel toetab vöötkoodiskanneri vidina sisendit toiminguteks Vali, Käivita, Lõpeta ja Tühjenda kanban-töö.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a7073fb5d77e2d11569e86b92433864371f0e1d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825863"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="202c1-103">Kanbani ülekandmise tahvli tugi vöötkoodilugejatele</span><span class="sxs-lookup"><span data-stu-id="202c1-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="202c1-104">Kanbani ülekandmise tahvel toetab vöötkoodiskanneri vidina sisendit toiminguteks Vali, Käivita, Lõpeta ja Tühjenda kanban-töö.</span><span class="sxs-lookup"><span data-stu-id="202c1-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="202c1-105">Registreerimisrežiimid</span><span class="sxs-lookup"><span data-stu-id="202c1-105">Registration modes</span></span>
------------------

<span data-ttu-id="202c1-106">Kiirkaardil **Skanneri registreerimine** saate valida registreerimisrežiimi, millega juhitakse tegevust, kui skannite kanban-kaardi numbri või sisestate numbri käsitsi väljale Kanban-kaardi number.</span><span class="sxs-lookup"><span data-stu-id="202c1-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="202c1-107">Registreerimisrežiimi määramine</span><span class="sxs-lookup"><span data-stu-id="202c1-107">Set registration mode</span></span> | <span data-ttu-id="202c1-108">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="202c1-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="202c1-109">Algus</span><span class="sxs-lookup"><span data-stu-id="202c1-109">Start</span></span>                 | <span data-ttu-id="202c1-110">Registreerib kanbani ülekandetöö pooleliolevana.</span><span class="sxs-lookup"><span data-stu-id="202c1-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="202c1-111">Lõpule viidud</span><span class="sxs-lookup"><span data-stu-id="202c1-111">Complete</span></span>              | <span data-ttu-id="202c1-112">Registreerib kanbani ülekandetöö lõpetatuna.</span><span class="sxs-lookup"><span data-stu-id="202c1-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="202c1-113">Tühi</span><span class="sxs-lookup"><span data-stu-id="202c1-113">Empty</span></span>                 | <span data-ttu-id="202c1-114">Registreerib kanban-kaardi viidatud materjali käsitlemisühiku tühjana.</span><span class="sxs-lookup"><span data-stu-id="202c1-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="202c1-115">Vali</span><span class="sxs-lookup"><span data-stu-id="202c1-115">Select</span></span>                | <span data-ttu-id="202c1-116">Registreerib kanban-kaardi numbri ja valib kanban-tööde loendist viidatud töö automaatselt.</span><span class="sxs-lookup"><span data-stu-id="202c1-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="202c1-117">Registreerimisrežiimi valimine</span><span class="sxs-lookup"><span data-stu-id="202c1-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="202c1-118">Kui kasutate töö valimiseks vöötkoodilugejat, muutub kanban-tahvli kuvarežiim.</span><span class="sxs-lookup"><span data-stu-id="202c1-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="202c1-119">Selles režiimis kehtivad järgmised tingimused.</span><span class="sxs-lookup"><span data-stu-id="202c1-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="202c1-120">Kuvatakse ainult skannitud kanban-töö.</span><span class="sxs-lookup"><span data-stu-id="202c1-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="202c1-121">Valitud töö üksikasjad kuvatakse kiirkaardil **Üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="202c1-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="202c1-122">Kiirkaardil **Teated** kuvatakse ainult teated valitud töö kohta.</span><span class="sxs-lookup"><span data-stu-id="202c1-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="202c1-123">Töö olekut saate muuta, kasutades funktsioone, mis on saadaval toimingupaanil.</span><span class="sxs-lookup"><span data-stu-id="202c1-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="202c1-124">Kanbani ülekandmise tahvlil kuvatakse sel ajal ainult üht tööd.</span><span class="sxs-lookup"><span data-stu-id="202c1-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="202c1-125">Saate värskendada tööde loendis olevat teavet käsitsi, klõpsates toimingupaanil käsku **Värskenda** (Shift + F5).</span><span class="sxs-lookup"><span data-stu-id="202c1-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="202c1-126">Pärast teabe värskendamist kuvatakse uuesti töö filtri täielikud tulemused.</span><span class="sxs-lookup"><span data-stu-id="202c1-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="202c1-127">Töö olek ja võimalikud tegevused</span><span class="sxs-lookup"><span data-stu-id="202c1-127">Job status and possible actions</span></span>
<span data-ttu-id="202c1-128">Valitud töö olek ja sündmuse kanbanide mis tahes kinnistatud tööde olek määravad, kas saate tööd edasi töödelda.</span><span class="sxs-lookup"><span data-stu-id="202c1-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="202c1-129">Järgmises tabelis kuvatakse teave nende olekute ja ülesannete kohta.</span><span class="sxs-lookup"><span data-stu-id="202c1-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="202c1-130">Tööde jaoks või tööde viidatud materjali käsitlemisühikute jaoks saadaolevad olekud.</span><span class="sxs-lookup"><span data-stu-id="202c1-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="202c1-131">Iga ülesanne, mida saate töö puhul täita.</span><span class="sxs-lookup"><span data-stu-id="202c1-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="202c1-132">Töö tüüp</span><span class="sxs-lookup"><span data-stu-id="202c1-132">Job type</span></span></th>
<th><span data-ttu-id="202c1-133">Töö olek või materjali käsitlemisühiku olek</span><span class="sxs-lookup"><span data-stu-id="202c1-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="202c1-134">Komplekteerimislehe värskendamine</span><span class="sxs-lookup"><span data-stu-id="202c1-134">Update picking list</span></span></th>
<th><span data-ttu-id="202c1-135">Algus</span><span class="sxs-lookup"><span data-stu-id="202c1-135">Start</span></span></th>
<th><span data-ttu-id="202c1-136">Värskenda reserveeringut</span><span class="sxs-lookup"><span data-stu-id="202c1-136">Update registration</span></span></th>
<th><span data-ttu-id="202c1-137">Lõpule viidud</span><span class="sxs-lookup"><span data-stu-id="202c1-137">Complete</span></span></th>
<th><span data-ttu-id="202c1-138">Tühi</span><span class="sxs-lookup"><span data-stu-id="202c1-138">Empty</span></span></th>
<th><span data-ttu-id="202c1-139">Loo sündmuse kanbanid</span><span class="sxs-lookup"><span data-stu-id="202c1-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="202c1-140">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="202c1-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="202c1-141">Pole plaanitud</span><span class="sxs-lookup"><span data-stu-id="202c1-141">Not planned</span></span></li>
<li><span data-ttu-id="202c1-142">Kinnistatud töid pole või on kinnistatud tööd lõpule viidud</span><span class="sxs-lookup"><span data-stu-id="202c1-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="202c1-143">Jah</span><span class="sxs-lookup"><span data-stu-id="202c1-143">Yes</span></span></td>
<td><span data-ttu-id="202c1-144">Jah</span><span class="sxs-lookup"><span data-stu-id="202c1-144">Yes</span></span></td>
<td><span data-ttu-id="202c1-145">Jah</span><span class="sxs-lookup"><span data-stu-id="202c1-145">Yes</span></span></td>
<td><span data-ttu-id="202c1-146">Jah</span><span class="sxs-lookup"><span data-stu-id="202c1-146">Yes</span></span></td>
<td><span data-ttu-id="202c1-147">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-147">No</span></span></td>
<td><span data-ttu-id="202c1-148">Jah</span><span class="sxs-lookup"><span data-stu-id="202c1-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="202c1-149">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="202c1-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="202c1-150">Pole plaanitud</span><span class="sxs-lookup"><span data-stu-id="202c1-150">Not planned</span></span></li>
<li><span data-ttu-id="202c1-151">Kinnistatud töö ei ole lõpule viidud</span><span class="sxs-lookup"><span data-stu-id="202c1-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="202c1-152">Jah</span><span class="sxs-lookup"><span data-stu-id="202c1-152">Yes</span></span></td>
<td><span data-ttu-id="202c1-153">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-153">No</span></span></td>
<td><span data-ttu-id="202c1-154">Jah</span><span class="sxs-lookup"><span data-stu-id="202c1-154">Yes</span></span></td>
<td><span data-ttu-id="202c1-155">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-155">No</span></span></td>
<td><span data-ttu-id="202c1-156">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-156">No</span></span></td>
<td><span data-ttu-id="202c1-157">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="202c1-158">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="202c1-158">Transfer</span></span></td>
<td><span data-ttu-id="202c1-159">Käimas</span><span class="sxs-lookup"><span data-stu-id="202c1-159">In progress</span></span></td>
<td><span data-ttu-id="202c1-160">Jah</span><span class="sxs-lookup"><span data-stu-id="202c1-160">Yes</span></span></td>
<td><span data-ttu-id="202c1-161">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-161">No</span></span></td>
<td><span data-ttu-id="202c1-162">Jah</span><span class="sxs-lookup"><span data-stu-id="202c1-162">Yes</span></span></td>
<td><span data-ttu-id="202c1-163">Jah</span><span class="sxs-lookup"><span data-stu-id="202c1-163">Yes</span></span></td>
<td><span data-ttu-id="202c1-164">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-164">No</span></span></td>
<td><span data-ttu-id="202c1-165">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="202c1-166">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="202c1-166">Transfer</span></span></td>
<td><span data-ttu-id="202c1-167">Valmis</span><span class="sxs-lookup"><span data-stu-id="202c1-167">Completed</span></span></td>
<td><span data-ttu-id="202c1-168">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-168">No</span></span></td>
<td><span data-ttu-id="202c1-169">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-169">No</span></span></td>
<td><span data-ttu-id="202c1-170">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-170">No</span></span></td>
<td><span data-ttu-id="202c1-171">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-171">No</span></span></td>
<td><span data-ttu-id="202c1-172">Jah</span><span class="sxs-lookup"><span data-stu-id="202c1-172">Yes</span></span></td>
<td><span data-ttu-id="202c1-173">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="202c1-174">Ülekanne või protsess</span><span class="sxs-lookup"><span data-stu-id="202c1-174">Transfer or process</span></span></td>
<td><span data-ttu-id="202c1-175">Tühi</span><span class="sxs-lookup"><span data-stu-id="202c1-175">Empty</span></span></td>
<td><span data-ttu-id="202c1-176">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-176">No</span></span></td>
<td><span data-ttu-id="202c1-177">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-177">No</span></span></td>
<td><span data-ttu-id="202c1-178">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-178">No</span></span></td>
<td><span data-ttu-id="202c1-179">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-179">No</span></span></td>
<td><span data-ttu-id="202c1-180">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-180">No</span></span></td>
<td><span data-ttu-id="202c1-181">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="202c1-182">Ülekanne või protsess</span><span class="sxs-lookup"><span data-stu-id="202c1-182">Transfer or process</span></span></td>
<td><span data-ttu-id="202c1-183">Kanban-kaarti ei leitud</span><span class="sxs-lookup"><span data-stu-id="202c1-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="202c1-184">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-184">No</span></span></td>
<td><span data-ttu-id="202c1-185">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-185">No</span></span></td>
<td><span data-ttu-id="202c1-186">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-186">No</span></span></td>
<td><span data-ttu-id="202c1-187">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-187">No</span></span></td>
<td><span data-ttu-id="202c1-188">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-188">No</span></span></td>
<td><span data-ttu-id="202c1-189">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="202c1-190">Ülekanne või protsess</span><span class="sxs-lookup"><span data-stu-id="202c1-190">Transfer or process</span></span></td>
<td><span data-ttu-id="202c1-191">Kanban-kaart leiti, kuid see pole kanbanile määratud</span><span class="sxs-lookup"><span data-stu-id="202c1-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="202c1-192">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-192">No</span></span></td>
<td><span data-ttu-id="202c1-193">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-193">No</span></span></td>
<td><span data-ttu-id="202c1-194">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-194">No</span></span></td>
<td><span data-ttu-id="202c1-195">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-195">No</span></span></td>
<td><span data-ttu-id="202c1-196">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-196">No</span></span></td>
<td><span data-ttu-id="202c1-197">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="202c1-198">Protsess</span><span class="sxs-lookup"><span data-stu-id="202c1-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="202c1-199">Pole plaanitud</span><span class="sxs-lookup"><span data-stu-id="202c1-199">Not planned</span></span></li>
<li><span data-ttu-id="202c1-200">Ettevalmistatud</span><span class="sxs-lookup"><span data-stu-id="202c1-200">Prepared</span></span></li>
<li><span data-ttu-id="202c1-201">Käimas</span><span class="sxs-lookup"><span data-stu-id="202c1-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="202c1-202">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-202">No</span></span></td>
<td><span data-ttu-id="202c1-203">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-203">No</span></span></td>
<td><span data-ttu-id="202c1-204">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-204">No</span></span></td>
<td><span data-ttu-id="202c1-205">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-205">No</span></span></td>
<td><span data-ttu-id="202c1-206">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-206">No</span></span></td>
<td><span data-ttu-id="202c1-207">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="202c1-208">Protsess</span><span class="sxs-lookup"><span data-stu-id="202c1-208">Process</span></span></td>
<td><span data-ttu-id="202c1-209">Valmis</span><span class="sxs-lookup"><span data-stu-id="202c1-209">Completed</span></span></td>
<td><span data-ttu-id="202c1-210">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-210">No</span></span></td>
<td><span data-ttu-id="202c1-211">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-211">No</span></span></td>
<td><span data-ttu-id="202c1-212">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-212">No</span></span></td>
<td><span data-ttu-id="202c1-213">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-213">No</span></span></td>
<td><span data-ttu-id="202c1-214">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-214">No</span></span></td>
<td><span data-ttu-id="202c1-215">Ei</span><span class="sxs-lookup"><span data-stu-id="202c1-215">No</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]