---
title: "Töövoos käsitsi ülesande konfigureerimine"
description: "See teema selgitab, kuidas konfigureerida käsitsi ülesande atribuute."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: e2aa02ff489f105e85c0dc6801f398f79126a4dd
ms.openlocfilehash: 98e25e1a132f0767b9c58334f177845c222c3863
ms.contentlocale: et-ee
ms.lasthandoff: 08/23/2017

---

# <a name="configure-a-manual-task-in-a-workflow"></a><span data-ttu-id="c9c8e-103">Töövoos käsitsi ülesande konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="c9c8e-103">Configure a manual task in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c9c8e-104">See teema selgitab, kuidas konfigureerida käsitsi ülesande atribuute.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="c9c8e-105">Töövoo redaktoris käsitsi ülesande loomiseks paremklõpsake ülesannet ja seejärel klõpsake suvandit **Atribuudid**, et avada lehekülg **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="c9c8e-106">Seejärel kasutage järgmisi protseduure, et konfigureerida käsitsi ülesande atribuudid.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="c9c8e-107">Ülesandele nime andmine</span><span class="sxs-lookup"><span data-stu-id="c9c8e-107">Name the task</span></span>
<span data-ttu-id="c9c8e-108">Sisestage käsitsi ülesandele nimi järgmisi juhiseid järgides.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-108">Follow these steps to enter a name for the manual task.</span></span>

1.  <span data-ttu-id="c9c8e-109">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="c9c8e-110">Sisestage ülesande kordumatu nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="c9c8e-111">Sisestage teemarida ja juhendid</span><span class="sxs-lookup"><span data-stu-id="c9c8e-111">Enter a subject line and instructions</span></span>
<span data-ttu-id="c9c8e-112">Sisestage teemarida ja juhendid sellele ülesandele määratud kasutajate jaoks.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="c9c8e-113">Näiteks kui konfigureerite ostutaotluste ülesannet, näeb kasutaja, kes on ülesandele määratud, teemarida ja juhiseid leheküljel **Ostutaotlused**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="c9c8e-114">Teemarida kuvatakse lehe teateribal.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="c9c8e-115">Kasutaja saab seejärel juhiste vaatamiseks klõpsata teateriba.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="c9c8e-116">Teemarea ja juhiste sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-116">Follow these steps to enter a subject line and instructions.</span></span>

1.  <span data-ttu-id="c9c8e-117">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-117">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="c9c8e-118">Väljale **Tööüksuse teema** sisestage teemarida.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-118">In the **Work item subject** field, enter the subject line.</span></span>
3.  <span data-ttu-id="c9c8e-119">Teemarea isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="c9c8e-120">Kohatäitjad asendatakse teemarea kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="c9c8e-121">Kohatäitja sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-121">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="c9c8e-122">Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-122">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="c9c8e-123">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-123">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="c9c8e-124">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-124">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="c9c8e-125">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-125">Click **Insert**.</span></span>

4.  <span data-ttu-id="c9c8e-126">Teemarea tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-126">To add translations of the subject line, follow these steps:</span></span>
    1.  <span data-ttu-id="c9c8e-127">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-127">Click **Translations**.</span></span>
    2.  <span data-ttu-id="c9c8e-128">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-128">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="c9c8e-129">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="c9c8e-130">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-130">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="c9c8e-131">Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 3.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6.  <span data-ttu-id="c9c8e-132">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-132">Click **Close**.</span></span>

5.  <span data-ttu-id="c9c8e-133">Väljale **Tööüksuse juhised** sisestage juhised.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-133">In the **Work item instructions** field, enter the instructions.</span></span>
6.  <span data-ttu-id="c9c8e-134">Juhiste isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="c9c8e-135">Kohatäitjad asendatakse juhiste kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="c9c8e-136">Kohatäitja sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-136">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="c9c8e-137">Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-137">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="c9c8e-138">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-138">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="c9c8e-139">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-139">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="c9c8e-140">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-140">Click **Insert**.</span></span>

7.  <span data-ttu-id="c9c8e-141">Juhiste tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-141">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="c9c8e-142">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-142">Click **Translations**.</span></span>
    2.  <span data-ttu-id="c9c8e-143">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-143">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="c9c8e-144">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="c9c8e-145">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-145">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="c9c8e-146">Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 6.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6.  <span data-ttu-id="c9c8e-147">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="c9c8e-148">Ülesande määramine</span><span class="sxs-lookup"><span data-stu-id="c9c8e-148">Assign the task</span></span>
<span data-ttu-id="c9c8e-149">Järgige neid etappe, et valida, kellele käsitsi ülesanne määratakse.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1.  <span data-ttu-id="c9c8e-150">Vasakul paanil klõpsake nuppu **Määramine**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-150">In the left pane, click **Assignment**.</span></span>
2.  <span data-ttu-id="c9c8e-151">Vahekaardil **Määramise tüüp** valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe enne, kui lähete 3 etappi.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c9c8e-152">Suvand</span><span class="sxs-lookup"><span data-stu-id="c9c8e-152">Option</span></span></th>
    <th><span data-ttu-id="c9c8e-153">Kasutajad, kellele ülesanne on määratud</span><span class="sxs-lookup"><span data-stu-id="c9c8e-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="c9c8e-154">Täiendavad etapid</span><span class="sxs-lookup"><span data-stu-id="c9c8e-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="c9c8e-155">Osaleja</span><span class="sxs-lookup"><span data-stu-id="c9c8e-155">Participant</span></span></td>
    <td><span data-ttu-id="c9c8e-156">Kasutajad, kes on määratud teatud grupile või rollile</span><span class="sxs-lookup"><span data-stu-id="c9c8e-156">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="c9c8e-157">Kui olete valinud suvandi <strong>Osaleja</strong> vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong>, valige grupi või rolli tüüp, millele ülesanne määrata.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="c9c8e-158">Loendis <strong>Osaleja</strong> valige grupp või roll, millele ülesanne määrata.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="c9c8e-159">Hierarhia</span><span class="sxs-lookup"><span data-stu-id="c9c8e-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="c9c8e-160">Kasutaja spetsiifilises organisatsioonilises hierarhias</span><span class="sxs-lookup"><span data-stu-id="c9c8e-160">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="c9c8e-161">Kui olete valinud suvandi <strong>Hierarhia</strong> vahekaardil <strong>Hierarhia valik</strong> loendis <strong>Hierarhia tüüp</strong>, valige hierarhia tüüp, millele ülesanne määrata.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="c9c8e-162">Süsteem peab hierarhiast tooma kasutajanimede vahemiku.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="c9c8e-163">Need nimed tähistavad kasutajaid, kellele saab ülesande määrata.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="c9c8e-164">Järgige neid etappe, et määrata nende kasutajanimede vahemiku algus- ja lõpp-punkt, mida kasutaja toob.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="c9c8e-165">Alguspunkti määramiseks valige isik loendist <strong>Alguspunkt</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="c9c8e-166">Lõpp-punkti määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="c9c8e-167">Seejärel sisestage tingimus, mis määrab, kus hierarhias lõpetab süsteem nimede toomise.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="c9c8e-168">Vahekaardil <strong>Hierarhiasuvandid</strong> määrake, millistele kasutajatele vahemikus tuleb ülesanne määrata.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="c9c8e-169"><strong>Määra kõikidele toodud kasutajatele</strong> – ülesanne määratakse kõikidele kasutajatele vahemikus.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="c9c8e-170"><strong>Määra ainult viimati toodud kasutajale</strong> – ülesanne määratakse ainult viimasele kasutajale vahemikus.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="c9c8e-171"><strong>Välista kasutajatelt järgmise tingimusega</strong> – ülesannet ei määrata vahemiku ühelegi kasutajale , kes vastavad teatud tingimusele.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="c9c8e-172">Tingimuse määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="c9c8e-173">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="c9c8e-173">Workflow user</span></span></td>
    <td><span data-ttu-id="c9c8e-174">Kasutajad praeguses töövoos</span><span class="sxs-lookup"><span data-stu-id="c9c8e-174">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="c9c8e-175">Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="c9c8e-176">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="c9c8e-176">User</span></span></td>
    <td><span data-ttu-id="c9c8e-177">Kindlad Microsoft Dynamics 365 for Finance and Operationsi kasutajad</span><span class="sxs-lookup"><span data-stu-id="c9c8e-177">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="c9c8e-178">Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="c9c8e-179">Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki Finance and Operationsi kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-179">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="c9c8e-180">Valige kasutajad, kellele ülesanne määrata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="c9c8e-181">Järjekord</span><span class="sxs-lookup"><span data-stu-id="c9c8e-181">Queue</span></span></td>
    <td><span data-ttu-id="c9c8e-182">Tööüksuste järjekord</span><span class="sxs-lookup"><span data-stu-id="c9c8e-182">A work item queue</span></span></td>
    <td><ol>
    <li><span data-ttu-id="c9c8e-183">Pärast suvandi <strong>Järjekord</strong> valimist klõpsake vahekaarti <strong>Järjekorral põhinev</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="c9c8e-184">Ülesande konkreetsesse järjekorda määramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="c9c8e-185">Valige loendis <strong>Järjekorra tüüp</strong> suvand <strong>Tööüksuste järjekord</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="c9c8e-186">Loendis <strong>Järjekorra nimi</strong> valige järjekord.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="c9c8e-187">Kui konkreetne tingimus peab määrama, millisesse järjekorda ülesanne määratakse, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="c9c8e-188">Valige loendis <strong>Järjekorra tüüp</strong> suvand <strong>Tinglike tööüksuste järjekord</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="c9c8e-189">Loendis <strong>Järjekorra nimi</strong> valige suvand <strong>Tinglik järjekord</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol></li>
    </ol><span data-ttu-id="c9c8e-190">
    <strong>Märkus.</strong> Suvandit kasutatakse ainult mõningate töövoogude puhul, nagu juhtumihaldus.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-190">
    <strong>Note:</strong> This option is used for only a few workflows, such as Case management.</span></span></td>
    </tr>
    </tbody>
    </table>

3.  <span data-ttu-id="c9c8e-191">Vahekaardi **Ajalimiit** väljal **Kestus** määrake, kui palju aega on kasutajal ülesande lõpuleviimiseks.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="c9c8e-192">Tehke üks järgmistest valikutest:</span><span class="sxs-lookup"><span data-stu-id="c9c8e-192">Select one of the following options:</span></span>
    -   <span data-ttu-id="c9c8e-193">**Tunnid** – sisestage tundide arv, kui kaua on kasutajal aega ülesande lõpuleviimiseks.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="c9c8e-194">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="c9c8e-195">**Päevad** – sisestage päevade arv, kui kaua on kasutajal aega ülesande lõpuleviimiseks.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="c9c8e-196">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="c9c8e-197">**Nädalad** – sisestage nädalate arv, kui kaua on kasutajal aega ülesande lõpuleviimiseks.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    -   <span data-ttu-id="c9c8e-198">**Kuud** – valige päev ja nädal, mil kasutaja peab ülesande lõpule viima.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="c9c8e-199">Näiteks soovite võib-olla, et kasutaja täidaks ülesande kuu kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="c9c8e-200">**Aastad** – valige päev, nädal ja kuu, mil kasutaja peab ülesande lõpule viima.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="c9c8e-201">Näiteks soovite võib-olla, et kasutaja täidaks ülesande detsembri kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="c9c8e-202">Kui kasutaja ei vii ülesannet määratud aja jooksul lõpule, on ülesande tähtaeg ületatud.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="c9c8e-203">Hilinenud ülesannet saab eskaleerida suvandite põhjal, mille valite lehe jaotises **Laiendus**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="c9c8e-204">Määrake, mis juhtub tähtaja ületanud ülesandega</span><span class="sxs-lookup"><span data-stu-id="c9c8e-204">Specify what happens when the task is overdue</span></span>
<span data-ttu-id="c9c8e-205">Kui kasutaja ei vii käsitsi ülesannet määratud aja jooksul lõpule, on ülesande tähtaeg ületatud.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="c9c8e-206">Hilinenud ülesannet saab eskaleerida või automaatselt muule kasutajale määrata.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="c9c8e-207">Järgige neid toiminguid hilinenud ülesande eskaleerimiseks.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-207">Follow these steps to escalate the task if it's overdue.</span></span>

1.  <span data-ttu-id="c9c8e-208">Vasakul paanil klõpsake valikut **Laiendus**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-208">In the left pane, click **Escalation**.</span></span>
2.  <span data-ttu-id="c9c8e-209">Laiendustee loomiseks märkige ruut **Laiendustee kasutamine**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="c9c8e-210">Süsteem määrab ülesande automaatselt laiendamistee nimekirjas olevatele kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="c9c8e-211">Näiteks tähistab järgmine tabel laiendusteed.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="c9c8e-212">Seeria</span><span class="sxs-lookup"><span data-stu-id="c9c8e-212">Sequence</span></span> | <span data-ttu-id="c9c8e-213">Laiendustee</span><span class="sxs-lookup"><span data-stu-id="c9c8e-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="c9c8e-214">1</span><span class="sxs-lookup"><span data-stu-id="c9c8e-214">1</span></span>        | <span data-ttu-id="c9c8e-215">Määra isikule: Donna</span><span class="sxs-lookup"><span data-stu-id="c9c8e-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="c9c8e-216">2</span><span class="sxs-lookup"><span data-stu-id="c9c8e-216">2</span></span>        | <span data-ttu-id="c9c8e-217">Määra isikule: Erin</span><span class="sxs-lookup"><span data-stu-id="c9c8e-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="c9c8e-218">3</span><span class="sxs-lookup"><span data-stu-id="c9c8e-218">3</span></span>        | <span data-ttu-id="c9c8e-219">Lõpptegevus: lükka tagasi</span><span class="sxs-lookup"><span data-stu-id="c9c8e-219">Final action: Reject</span></span> |

    <span data-ttu-id="c9c8e-220">Sellise näite korral määrab süsteem hilinenud ülesande Donnale.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="c9c8e-221">Kui Donna ei täida ülesannet selleks ettenähtud aja jooksul, määrab süsteem ülesande Erinile.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="c9c8e-222">Kui Erin ei täida ülesannet määratud aja jooksul, lükkab süsteem töötlemiseks edastatud dokumendi tagasi.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>
3.  <span data-ttu-id="c9c8e-223">Laiendustee kasutajale lisamiseks klõpsake valikut **Laienduse lisamine**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="c9c8e-224">Vahekaardil **Määramise tüüp** valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe, enne kui jätkate 4. etapiga.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c9c8e-225">Suvand</span><span class="sxs-lookup"><span data-stu-id="c9c8e-225">Option</span></span></th>
    <th><span data-ttu-id="c9c8e-226">Kasutajad, kellele ülesanne eskaleeritakse</span><span class="sxs-lookup"><span data-stu-id="c9c8e-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="c9c8e-227">Täiendavad etapid</span><span class="sxs-lookup"><span data-stu-id="c9c8e-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="c9c8e-228">Hierarhia</span><span class="sxs-lookup"><span data-stu-id="c9c8e-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="c9c8e-229">Kasutaja spetsiifilises organisatsioonilises hierarhias</span><span class="sxs-lookup"><span data-stu-id="c9c8e-229">Users in a specific organizational hierarchy</span></span></td>
    <td><ol>
    <li><span data-ttu-id="c9c8e-230">Kui olete valinud vahekaardil <strong>Hierarhia valik</strong> loendis <strong>Hierarhia tüüp</strong> suvandi <strong>Hierarhia</strong>, valige hierarhia tüüp, millele ülesanne eskaleerida.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="c9c8e-231">Süsteem peab hierarhiast tooma kasutajanimede vahemiku.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="c9c8e-232">Need nimed tähistavad kasutajaid, kellele saab ülesannet eskaleerida.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="c9c8e-233">Järgige neid etappe, et määrata nende kasutajanimede vahemiku algus- ja lõpp-punkt, mida kasutaja toob.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="c9c8e-234">Alguspunkti määramiseks valige isik loendist <strong>Alguspunkt</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="c9c8e-235">Lõpp-punkti määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="c9c8e-236">Seejärel sisestage tingimus, mis määrab, kus hierarhias lõpetab süsteem nimede toomise.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol></li>
    <li><span data-ttu-id="c9c8e-237">Vahekaardil <strong>Hierarhiasuvandid</strong> määrake, millistele kasutajatele vahemikus tuleb ülesanne eskaleerida.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="c9c8e-238"><strong>Määra kõikidele toodud kasutajatele</strong> – ülesanne eskaleeritakse kõikidele kasutajatele vahemikus.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="c9c8e-239"><strong>Määra ainult viimati toodud kasutajale</strong> – ülesanne eskaleeritakse ainult viimasele kasutajale vahemikus.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="c9c8e-240"><strong>Välista kasutajatelt järgmise tingimusega</strong> – ülesannet ei eskaleerita vahemiku ühelegi kasutajale, kes vastavad teatud tingimusele.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="c9c8e-241">Tingimuse määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="c9c8e-242">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="c9c8e-242">Workflow user</span></span></td>
    <td><span data-ttu-id="c9c8e-243">Kasutajad praeguses töövoos</span><span class="sxs-lookup"><span data-stu-id="c9c8e-243">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="c9c8e-244">Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="c9c8e-245">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="c9c8e-245">User</span></span></td>
    <td><span data-ttu-id="c9c8e-246">Konkreetsed Finance and Operationsi kasutajad</span><span class="sxs-lookup"><span data-stu-id="c9c8e-246">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="c9c8e-247">Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="c9c8e-248">Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki Finance and Operationsi kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-248">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="c9c8e-249">Valige kasutajad, kellele ülesanne eskaleerida, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

4.  <span data-ttu-id="c9c8e-250">Vahekaardi **Ajalimiit** väljal **Kestus** määrake, kui palju aega on kasutajal ülesande lõpuleviimiseks.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="c9c8e-251">Tehke üks järgmistest valikutest:</span><span class="sxs-lookup"><span data-stu-id="c9c8e-251">Select one of the following options:</span></span>
    -   <span data-ttu-id="c9c8e-252">**Tunnid** – sisestage tundide arv, kui kaua on kasutajal aega ülesande lõpuleviimiseks.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="c9c8e-253">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="c9c8e-254">**Päevad** – sisestage päevade arv, kui kaua on kasutajal aega ülesande lõpuleviimiseks.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="c9c8e-255">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="c9c8e-256">**Nädalad** – sisestage nädalate arv, kui kaua on kasutajal aega ülesande lõpuleviimiseks.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    -   <span data-ttu-id="c9c8e-257">**Kuud** – valige päev ja nädal, mil kasutaja peab ülesande lõpule viima.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="c9c8e-258">Näiteks soovite võib-olla, et kasutaja täidaks ülesande kuu kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="c9c8e-259">**Aastad** – valige päev, nädal ja kuu, mil kasutaja peab ülesande lõpule viima.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="c9c8e-260">Näiteks soovite võib-olla, et kasutaja täidaks ülesande detsembri kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5.  <span data-ttu-id="c9c8e-261">Korrake etappe 3 kuni 4 iga kasutaja puhul, kes tuleb laiendusteele lisada.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="c9c8e-262">Saate muuta kasutajate järjekorda.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-262">You can change the order of the users.</span></span>
6.  <span data-ttu-id="c9c8e-263">Kui kasutajad eskaleerimisteel ei täida ülesannet määratud aja jooksul, teeb süsteem ülesandega tegevuse.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="c9c8e-264">Süsteemi tegevuse määramiseks valige rida **Tegevus** ja seejärel valige tegevus vahekaardi **Lõpptegevus**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="c9c8e-265">Määrake, millal süsteem ülesandega automaatselt toimingu teeb</span><span class="sxs-lookup"><span data-stu-id="c9c8e-265">Specify when the system automatically acts on the task</span></span>
<span data-ttu-id="c9c8e-266">Saate konfigureerida süsteemi, nii et see teeks käsitsi ülesandega toimingu, kui teatud tingimused on täidetud.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="c9c8e-267">Näiteks peab ülesande nõuete kohaselt kuluaruannete osakonna liige üle vaatama sissetulekud, mis saadetakse koos kuluaruandega.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="c9c8e-268">Ettevõtte poliitika kohaselt tuleb ülesanne täita juhul, kui kuluaruande kogusumma on suurem kui 100 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="c9c8e-269">Sel juhul saate konfigureerida süsteemi nii, et ülesande olekuks määratakse automaatselt **Lõpule viidud**, kui summa on väiksem kui 100.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="c9c8e-270">Järgige neid toiminguid, et määrata, millal süsteem käsitsi ülesande puhul tegevuse teeb.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1.  <span data-ttu-id="c9c8e-271">Klõpsake vasakpoolsel paanil suvandit **Automaatsed tegevused**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-271">In the left pane, click **Automatic actions**.</span></span>
2.  <span data-ttu-id="c9c8e-272">Märkige ruut **Luba automaatsed tegevused**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-272">Select the **Enable automatic actions** check box.</span></span>
3.  <span data-ttu-id="c9c8e-273">Klõpsake **Lisa tingimus**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-273">Click **Add condition**.</span></span>
4.  <span data-ttu-id="c9c8e-274">Sisestage tingimus.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-274">Enter a condition.</span></span>
5.  <span data-ttu-id="c9c8e-275">Sisestage täiendavad vajalikud tingimused.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-275">Enter any additional conditions that are required.</span></span>
6.  <span data-ttu-id="c9c8e-276">Kinnitamaks, et teie sisestatud tingimused on õigesti konfigureeritud, järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="c9c8e-277">Klõpsake nuppu **Test**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-277">Click **Test**.</span></span>
    2.  <span data-ttu-id="c9c8e-278">Lehel **Testi töövoo tingimus** alas **Kontrolli tingimust** valige kirje.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="c9c8e-279">Klõpsake nuppu **Test**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-279">Click **Test**.</span></span> <span data-ttu-id="c9c8e-280">Süsteem hindab kirjet otsustamaks, kas see vastab teie määratud tingimustele.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="c9c8e-281">Klõpsake **OK** või valikut **Tühista**, et naasta lehele **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7.  <span data-ttu-id="c9c8e-282">Loendist **Automaatse lõpuleviimise tegevus** valige tegevus, mille süsteem peaks ülesande puhul tegema.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="c9c8e-283">Määrake, millal teatisi saadetakse</span><span class="sxs-lookup"><span data-stu-id="c9c8e-283">Specify when notifications are sent</span></span>
<span data-ttu-id="c9c8e-284">Võite saata inimestele teatisi käsitsi ülesande delegeerimisel, eskaleerimisel, lõpuleviimisel või tagasilükkamisel või muudatuse taotlemisel.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="c9c8e-285">Tehke järgmist, et määrata, millal ja kellele teatisi saadetakse.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1.  <span data-ttu-id="c9c8e-286">Vasakul paanil klõpsake suvandit **Teatised**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-286">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="c9c8e-287">Märkige ruut sündmuste kõrval, mille puhul saadetakse teatis.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-287">Select the check box next to the events that notifications should be sent for:</span></span>
    -   <span data-ttu-id="c9c8e-288">**Delegeerimine** – ülesanne määrati muule kasutajale.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-288">**Delegate** – The task has been assigned to another user.</span></span>
    -   <span data-ttu-id="c9c8e-289">**Eskaleerimine** – määratud kasutaja ei viinud toimingut määratud aja jooksul lõpule.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    -   <span data-ttu-id="c9c8e-290">**Lõpule viidud** – määratud kasutaja viis ülesande lõpule.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-290">**Complete** – The assigned user has completed the task.</span></span>
    -   <span data-ttu-id="c9c8e-291">**Tagasi lükatud** – määratud kasutaja lükkas esitatud dokumendi tagasi.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    -   <span data-ttu-id="c9c8e-292">**Muudatuse taotlus** – määratud kasutaja taotles esitatud dokumendi muutmist.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3.  <span data-ttu-id="c9c8e-293">Valige 2. etapis valitud sündmuse rida.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-293">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="c9c8e-294">Sisestage teatise tekst vahekaardil **Teatise tekst** olevale tekstiväljale.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5.  <span data-ttu-id="c9c8e-295">Teatise isikupärastamiseks võite sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="c9c8e-296">Kohatäitjad asendatakse teatise kasutajatele kuvamisel sobiva teabega.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="c9c8e-297">Kohatäitja sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-297">Follow these steps to insert a placeholder:</span></span>
    1.  <span data-ttu-id="c9c8e-298">Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-298">In the text box, click where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="c9c8e-299">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-299">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="c9c8e-300">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-300">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="c9c8e-301">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-301">Click **Insert**.</span></span>

6.  <span data-ttu-id="c9c8e-302">Teatise tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-302">To add translations of the notification, follow these steps:</span></span>
    1.  <span data-ttu-id="c9c8e-303">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-303">Click **Translations**.</span></span>
    2.  <span data-ttu-id="c9c8e-304">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-304">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="c9c8e-305">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4.  <span data-ttu-id="c9c8e-306">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-306">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="c9c8e-307">Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 5.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6.  <span data-ttu-id="c9c8e-308">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-308">Click **Close**.</span></span>

7.  <span data-ttu-id="c9c8e-309">Määrake vahekaardil **Adressaat**, kellele teatised saadetakse.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="c9c8e-310">Valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe, enne kui jätkate 8. etapiga.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c9c8e-311">Suvand</span><span class="sxs-lookup"><span data-stu-id="c9c8e-311">Option</span></span></th>
    <th><span data-ttu-id="c9c8e-312">Teatise adressaadid</span><span class="sxs-lookup"><span data-stu-id="c9c8e-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="c9c8e-313">Täiendavad etapid</span><span class="sxs-lookup"><span data-stu-id="c9c8e-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="c9c8e-314">Osaleja</span><span class="sxs-lookup"><span data-stu-id="c9c8e-314">Participant</span></span></td>
    <td><span data-ttu-id="c9c8e-315">Kasutajad, kes on määratud teatud grupile või rollile</span><span class="sxs-lookup"><span data-stu-id="c9c8e-315">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="c9c8e-316">Kui olete valinud suvandi <strong>Osaleja</strong> vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong>, valige grupi või rolli tüüp, millele teatisi saata.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="c9c8e-317">Loendis <strong>Osaleja</strong> valige grupp või roll, millele teatisi saata.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="c9c8e-318">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="c9c8e-318">Workflow user</span></span></td>
    <td><span data-ttu-id="c9c8e-319">Kasutajad praeguses töövoos</span><span class="sxs-lookup"><span data-stu-id="c9c8e-319">Users in the current workflow</span></span></td>
    <td><ul>
    <li><span data-ttu-id="c9c8e-320">Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="c9c8e-321">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="c9c8e-321">User</span></span></td>
    <td><span data-ttu-id="c9c8e-322">Konkreetsed Finance and Operationsi kasutajad</span><span class="sxs-lookup"><span data-stu-id="c9c8e-322">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="c9c8e-323">Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="c9c8e-324">Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki Finance and Operationsi kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-324">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="c9c8e-325">Valige kasutajad, kellele teatisi saata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="c9c8e-326">Korrake 3.–7. toimingut iga sündmuse puhul, mille 2. etapis valisite.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="c9c8e-327">Ajalimiidi seadmine</span><span class="sxs-lookup"><span data-stu-id="c9c8e-327">Set a time limit</span></span>
<span data-ttu-id="c9c8e-328">Kui käsitsi ülesanne tuleb teatud ajaks lõpule viia, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-328">Follow these steps if the manual task must be completed in a specific time.</span></span> 

<span data-ttu-id="c9c8e-329">**Märkus.** Selle protseduuri käigus valitud suvandid alistavad lehe jaotistes **Määramine** ja **Eskaleerimine** valitud suvandid.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-329">**Note:** The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1.  <span data-ttu-id="c9c8e-330">Klõpsake vasakpoolsel paanil suvandit **Täpsemad sätted**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-330">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="c9c8e-331">Märkige ruut **Määra töövoo elemendi jaoks ajalimiit**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3.  <span data-ttu-id="c9c8e-332">Määrake väljal **Kestus**, mis ajaks peab ülesanne olema lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="c9c8e-333">Tehke üks järgmistest valikutest:</span><span class="sxs-lookup"><span data-stu-id="c9c8e-333">Select one of the following options:</span></span>
    -   <span data-ttu-id="c9c8e-334">**Tunnid** – sisestage tundide arv, mille jooksul tuleb ülesanne lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="c9c8e-335">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="c9c8e-336">**Päevad** – sisestage päevade arv, mille jooksul tuleb ülesanne lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="c9c8e-337">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    -   <span data-ttu-id="c9c8e-338">**Nädalad** – sisestage nädalate arv, mille jooksul tuleb ülesanne lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    -   <span data-ttu-id="c9c8e-339">**Kuud** – valige päev ja nädal, mil kasutaja peab ülesande lõpule viima.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="c9c8e-340">Näiteks soovite võib-olla, et ülesanne oleks täidetud kuu kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    -   <span data-ttu-id="c9c8e-341">**Aastad** – valige päev, nädal ja kuu, mil kasutaja peab ülesande lõpule viima.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="c9c8e-342">Näiteks soovite võib-olla, et ülesanne oleks täidetud detsembri kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4.  <span data-ttu-id="c9c8e-343">Ajalimiidi ületamisel teeb süsteem ülesandega tegevuse.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="c9c8e-344">Loendist **Tegevus** valige tegevus, mida süsteem peaks tegema.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="c9c8e-345">Määrake, millised tegevused on kasutaja jaoks saadaval</span><span class="sxs-lookup"><span data-stu-id="c9c8e-345">Specify which actions are available to the user</span></span>
<span data-ttu-id="c9c8e-346">Kui kasutajale määratakse käsitsi ülesanne, tuleb kasutajal teha sellega tegevus.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="c9c8e-347">Järgige neid toiminguid, et määrata, millised tegevused on kasutaja jaoks ülesande puhul saadaval.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-347">Follow these steps to specify which actions the user can take on the task.</span></span> <span data-ttu-id="c9c8e-348">**Märkus.** Saadaolevad tegevused erinevad olenevalt ülesande kujundusest.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-348">**Note:** The actions that are available vary, depending on the design of the task.</span></span>

1.  <span data-ttu-id="c9c8e-349">Klõpsake vasakpoolsel paanil suvandit **Täpsemad sätted**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-349">In the left pane, click **Advanced settings**.</span></span>
2.  <span data-ttu-id="c9c8e-350">Märkige ruut **Lõpule viidud**, kui soovite anda kasutajale õiguse märkida ülesande olekuks **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3.  <span data-ttu-id="c9c8e-351">Märkige ruut **Lükka tagasi**, kui soovite anda kasutajale õiguse lükata esitatud dokument tagasi.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4.  <span data-ttu-id="c9c8e-352">Märkige ruut **Taotle muudatust**, kui soovite anda kasutajale õiguse taotleda muudatuste tegemist talle edastatud dokumendis.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5.  <span data-ttu-id="c9c8e-353">Märkige ruut **Delegeeri**, kui soovite anda kasutajale õiguse delegeerida ülesanne teisele kasutajale.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6.  <span data-ttu-id="c9c8e-354">Märkige ruut **Määra ümber**, kui soovite anda kasutajale õiguse määrata ülesanne ümber teisele kasutajale tööüksuste järjekorras.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7.  <span data-ttu-id="c9c8e-355">Märkige ruut **Vabasta**, kui soovite anda kasutajale õiguse määrata ülesanne ümber teisele kasutajale tööüksuste järjekorras.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="c9c8e-356">Muu kasutaja saab ülesande täita.</span><span class="sxs-lookup"><span data-stu-id="c9c8e-356">Another user can then complete the task.</span></span>





