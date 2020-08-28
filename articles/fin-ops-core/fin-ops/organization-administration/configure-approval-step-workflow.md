---
title: Töövoo kinnitusetappide konfigureerimine
description: See teema selgitab, kuidas konfigureerida kinnitusetapi atribuute.
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69035be84d489d6ea2342c6974cfa9a31531f1c7
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698067"
---
# <a name="configure-approval-steps-in-a-workflow"></a><span data-ttu-id="5307e-103">Töövoo kinnitusetappide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="5307e-103">Configure approval steps in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5307e-104">See teema selgitab, kuidas konfigureerida kinnitusetapi atribuute.</span><span class="sxs-lookup"><span data-stu-id="5307e-104">This topic explains how to configure the properties of an approval step.</span></span>

<span data-ttu-id="5307e-105">Töövoo redaktoris kinnitamisetapi konfigureerimiseks paremklõpsake kinnitamisetappi ja klõpsake seejärel nuppu **Atribuudid**, et avada lehekülg **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="5307e-105">To configure an approval step in the workflow editor, right-click the approval step, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="5307e-106">Seejärel kasutage järgmisi protseduure, et konfigureerida kinnitamisetapi atribuudid.</span><span class="sxs-lookup"><span data-stu-id="5307e-106">Then use the following procedures to configure the properties of the approval step.</span></span>

## <a name="name-the-step"></a><span data-ttu-id="5307e-107">Sammule nime andmine</span><span class="sxs-lookup"><span data-stu-id="5307e-107">Name the step</span></span>
<span data-ttu-id="5307e-108">Sisestage kinnitusetapile nimi järgmisi juhiseid järgides.</span><span class="sxs-lookup"><span data-stu-id="5307e-108">Follow these steps to enter a name for the approval step.</span></span>

1. <span data-ttu-id="5307e-109">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="5307e-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="5307e-110">Väljal **Nimi** sisestage kinnitusetapile kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="5307e-110">In the **Name** field, enter a unique name for the approval step.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="5307e-111">Sisestage teemarida ja juhendid</span><span class="sxs-lookup"><span data-stu-id="5307e-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="5307e-112">Sisestage teemarida ja juhendid kasutajatele, kes on määratud kinnitusetapile.</span><span class="sxs-lookup"><span data-stu-id="5307e-112">You must provide a subject line and instructions to users who are assigned to the approval step.</span></span> <span data-ttu-id="5307e-113">Näiteks kui konfigureerite kinnitusetappi ostutaotlustele, siis näeb kasutaja, kes on etapile määratud, teemarida ja juhiseid leheküljel **Ostutaotlused**.</span><span class="sxs-lookup"><span data-stu-id="5307e-113">For example, if you're configuring an approval step for purchase requisitions, the user who is assigned to the step sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="5307e-114">Teemarida kuvatakse lehe teateribal.</span><span class="sxs-lookup"><span data-stu-id="5307e-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="5307e-115">Kasutaja saab seejärel juhiste nägemiseks klõpsata teateribal.</span><span class="sxs-lookup"><span data-stu-id="5307e-115">The user can then click the icon in the message bar to see the instructions.</span></span> <span data-ttu-id="5307e-116">Teemarea ja juhiste sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="5307e-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="5307e-117">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="5307e-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="5307e-118">Väljale **Tööüksuse teema** sisestage teemarida.</span><span class="sxs-lookup"><span data-stu-id="5307e-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="5307e-119">Teemarea isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="5307e-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="5307e-120">Kohatäitjad asendatakse teemarea kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="5307e-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="5307e-121">Kohatäitja sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="5307e-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="5307e-122">Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.</span><span class="sxs-lookup"><span data-stu-id="5307e-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="5307e-123">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="5307e-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="5307e-124">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="5307e-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="5307e-125">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="5307e-125">Click **Insert**.</span></span>

4. <span data-ttu-id="5307e-126">Teemarea tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="5307e-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="5307e-127">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="5307e-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="5307e-128">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="5307e-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="5307e-129">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="5307e-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="5307e-130">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="5307e-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="5307e-131">Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 3.</span><span class="sxs-lookup"><span data-stu-id="5307e-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="5307e-132">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="5307e-132">Click **Close**.</span></span>

5. <span data-ttu-id="5307e-133">Väljale **Tööüksuse juhised** sisestage juhised.</span><span class="sxs-lookup"><span data-stu-id="5307e-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="5307e-134">Juhiste isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="5307e-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="5307e-135">Kohatäitjad asendatakse juhiste kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="5307e-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="5307e-136">Kohatäitja sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="5307e-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="5307e-137">Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.</span><span class="sxs-lookup"><span data-stu-id="5307e-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="5307e-138">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="5307e-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="5307e-139">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="5307e-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="5307e-140">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="5307e-140">Click **Insert**.</span></span>

7. <span data-ttu-id="5307e-141">Juhiste tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="5307e-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="5307e-142">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="5307e-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="5307e-143">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="5307e-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="5307e-144">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="5307e-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="5307e-145">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="5307e-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="5307e-146">Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 6.</span><span class="sxs-lookup"><span data-stu-id="5307e-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="5307e-147">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="5307e-147">Click **Close**.</span></span>

## <a name="assign-the-approval-step"></a><span data-ttu-id="5307e-148">Määrake kinnitussamm</span><span class="sxs-lookup"><span data-stu-id="5307e-148">Assign the approval step</span></span>

<span data-ttu-id="5307e-149">Järgige neid etappe, et määrata, kellele kinnitusetapp tuleb määrata.</span><span class="sxs-lookup"><span data-stu-id="5307e-149">Follow these steps to specify who the approval step should be assigned to.</span></span>

1. <span data-ttu-id="5307e-150">Vasakul paanil klõpsake nuppu **Määramine**.</span><span class="sxs-lookup"><span data-stu-id="5307e-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="5307e-151">Vahekaardil **Määramise tüüp** valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe enne, kui lähete 3 etappi.</span><span class="sxs-lookup"><span data-stu-id="5307e-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="5307e-152">Suvand</span><span class="sxs-lookup"><span data-stu-id="5307e-152">Option</span></span></th>
    <th><span data-ttu-id="5307e-153">Kasutajad, kellele kinnitamisetapp on määratud</span><span class="sxs-lookup"><span data-stu-id="5307e-153">Users that the approval step is assigned to</span></span></th>
    <th><span data-ttu-id="5307e-154">Täiendavad etapid</span><span class="sxs-lookup"><span data-stu-id="5307e-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="5307e-155">Osaleja</span><span class="sxs-lookup"><span data-stu-id="5307e-155">Participant</span></span></td>
    <td><span data-ttu-id="5307e-156">Kasutajad, kes on määratud teatud grupile või rollile</span><span class="sxs-lookup"><span data-stu-id="5307e-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5307e-157">Kui olete valinud suvandi <strong>Osaleja</strong> vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong>, valige grupi või rolli tüüp, millele etapp määrata.</span><span class="sxs-lookup"><span data-stu-id="5307e-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the step to.</span></span></li>
    <li><span data-ttu-id="5307e-158">Loendis <strong>Osaleja</strong> valige grupp või roll, millele etapp määrata.</span><span class="sxs-lookup"><span data-stu-id="5307e-158">In the <strong>Participant</strong> list, select the group or role to assign the step to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5307e-159">Hierarhia</span><span class="sxs-lookup"><span data-stu-id="5307e-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="5307e-160">Kasutaja spetsiifilises organisatsioonilises hierarhias</span><span class="sxs-lookup"><span data-stu-id="5307e-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5307e-161">Kui olete valinud suvandi <strong>Hierarhia</strong> vahekaardil <strong>Hierarhia valik</strong> loendis <strong>Hierarhia tüüp</strong>, valige hierarhia tüüp, millele etapp määrata.</span><span class="sxs-lookup"><span data-stu-id="5307e-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the step to.</span></span></li>
    <li><span data-ttu-id="5307e-162">Süsteem peab hierarhiast tooma kasutajanimede vahemiku.</span><span class="sxs-lookup"><span data-stu-id="5307e-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="5307e-163">Need nimed tähistavad kasutajaid, kellele etappi saab määrata.</span><span class="sxs-lookup"><span data-stu-id="5307e-163">These names represent users that the step can be assigned to.</span></span> <span data-ttu-id="5307e-164">Järgige neid etappe, et määrata nende kasutajanimede vahemiku algus- ja lõpp-punkt, mida kasutaja toob.</span><span class="sxs-lookup"><span data-stu-id="5307e-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="5307e-165">Alguspunkti määramiseks valige isik loendist <strong>Alguspunkt</strong>.</span><span class="sxs-lookup"><span data-stu-id="5307e-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="5307e-166">Lõpp-punkti määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="5307e-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="5307e-167">Seejärel sisestage tingimus, mis määrab, kus hierarhias lõpetab süsteem nimede toomise.</span><span class="sxs-lookup"><span data-stu-id="5307e-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="5307e-168">Vahekaardil <strong>Hierarhiasuvandid</strong> määrake, millistele kasutajatele vahemikus tuleb etapp määrata.</span><span class="sxs-lookup"><span data-stu-id="5307e-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the step should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="5307e-169"><strong>Määra kõikidele toodud kasutajatele</strong> – etapp määratakse kõikidele kasutajatele vahemikus.</span><span class="sxs-lookup"><span data-stu-id="5307e-169"><strong>Assign to all users retrieved</strong> – The step is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="5307e-170"><strong>Määra ainult viimati toodud kasutajale</strong> – etapp määratakse ainult viimasele kasutajale vahemikus.</span><span class="sxs-lookup"><span data-stu-id="5307e-170"><strong>Assign only to last user retrieved</strong> – The step is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="5307e-171"><strong>Välista kasutajatelt järgmise tingimusega</strong> – etappi ei määrata vahemiku ühelegi kasutajale , kes vastavad teatud tingimusele.</span><span class="sxs-lookup"><span data-stu-id="5307e-171"><strong>Exclude users with the following condition</strong> – The step isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="5307e-172">Tingimuse määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="5307e-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5307e-173">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="5307e-173">Workflow user</span></span></td>
    <td><span data-ttu-id="5307e-174">Kasutajad praeguses töövoos</span><span class="sxs-lookup"><span data-stu-id="5307e-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="5307e-175">Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</span><span class="sxs-lookup"><span data-stu-id="5307e-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5307e-176">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="5307e-176">User</span></span></td>
    <td><span data-ttu-id="5307e-177">Kindlad kasutajad</span><span class="sxs-lookup"><span data-stu-id="5307e-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5307e-178">Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="5307e-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="5307e-179">Loend <strong>Saadaolevad kasutajad</strong> hõlmab süsteemi kõiki kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="5307e-179">The <strong>Available users</strong> list includes all system users.</span></span> <span data-ttu-id="5307e-180">Valige kasutajad, kellele etapp määrata, ja liigutage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="5307e-180">Select the users to assign the step to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="5307e-181">Vahekaardi **Ajalimiit** väljal **Kestus** määrake, kui palju aega on kasutajal reageerida või vastata dokumentidele, mis jõuavad kinnitusetappi.</span><span class="sxs-lookup"><span data-stu-id="5307e-181">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents that reach the approval step.</span></span> <span data-ttu-id="5307e-182">Tehke üks järgmistest valikutest:</span><span class="sxs-lookup"><span data-stu-id="5307e-182">Select one of the following options:</span></span>

    - <span data-ttu-id="5307e-183">**Tunnid** – sisestage tundide arv, kui kaua on kasutajal aega vastata.</span><span class="sxs-lookup"><span data-stu-id="5307e-183">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="5307e-184">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="5307e-184">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5307e-185">**Päevad** – sisestage päevade arv, kui kaua on kasutajal aega vastata.</span><span class="sxs-lookup"><span data-stu-id="5307e-185">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="5307e-186">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="5307e-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5307e-187">**Nädalad** – sisestage nädalate arv, kui kaua on kasutajal aega vastata.</span><span class="sxs-lookup"><span data-stu-id="5307e-187">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="5307e-188">**Kuud** – valige päev ja nädal, mis ajaks kasutaja peab vastama</span><span class="sxs-lookup"><span data-stu-id="5307e-188">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="5307e-189">Näiteks võite soovida kasutajalt vastust saada kuu kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="5307e-189">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="5307e-190">**Aastad** – valige päev, nädal ja kuu, mis ajaks kasutaja peab vastama</span><span class="sxs-lookup"><span data-stu-id="5307e-190">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="5307e-191">Näiteks võite soovida kasutajalt vastust detsembri kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="5307e-191">For example, you might want the user to respond by Friday of the third week of December.</span></span>

    <span data-ttu-id="5307e-192">Kui kasutaja ei reageeri dokumendile määratud aja jooksul, siis on dokument hilinenud..</span><span class="sxs-lookup"><span data-stu-id="5307e-192">If the user doesn't take action on the document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="5307e-193">Hilinenud dokumenti laiendatakse nende valikute põhjal, mille valite lehe alal **Laiendus**.</span><span class="sxs-lookup"><span data-stu-id="5307e-193">A document that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

4. <span data-ttu-id="5307e-194">Kui määrate kinnitusetapi mitmele kasutajale või kasutajate grupile, valige vahekaardil **Lõpetamispoliitika** üks järgmistest suvanditest.</span><span class="sxs-lookup"><span data-stu-id="5307e-194">If you assigned the approval step to multiple users or a group of users, on the **Completion policy** tab, select one of the following options:</span></span>

    - <span data-ttu-id="5307e-195">**Üksikkinnitaja** – dokumendile rakenduva toimingu määrab esimene isik, kes vastab.</span><span class="sxs-lookup"><span data-stu-id="5307e-195">**Single approver** – The action that is applied to the document is determined by the first person who responds.</span></span> <span data-ttu-id="5307e-196">Näiteks Sam on edastanud kuluaruande summale 15 000 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="5307e-196">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="5307e-197">Kuluaruanne on praegu määratud Suele, Jole ja Billile.</span><span class="sxs-lookup"><span data-stu-id="5307e-197">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="5307e-198">Kui Sue reageerib dokumendile esimesena, rakendatakse tema võetud meetmeid dokumendil.</span><span class="sxs-lookup"><span data-stu-id="5307e-198">If Sue is the first person who responds to the document, the action that she takes is applied to the document.</span></span> <span data-ttu-id="5307e-199">Kui Sue lükkab dokumendi tagasi, lükatakse dokument tagasi ja saadetakse uuesti Samile.</span><span class="sxs-lookup"><span data-stu-id="5307e-199">If Sue rejects the document, it's rejected and sent back to Sam.</span></span> <span data-ttu-id="5307e-200">Kui Sue kinnitab dokumendi, saadetakse see Annile kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="5307e-200">If Sue approves the document, it's sent to Ann for approval.</span></span>

        ![Töövoog, millel on kinnitamisprotsess](./media/workflow_multipleusersinstep.gif)

    - <span data-ttu-id="5307e-202">**Enamik kinnitajaid** – tegevus, mis rakendatakse dokumendile, määratakse siis, kui enamik kinnitajaid vastab.</span><span class="sxs-lookup"><span data-stu-id="5307e-202">**Majority of approvers** – The action that is applied to the document is determined when most of the approvers respond.</span></span> <span data-ttu-id="5307e-203">Näiteks Sam on edastanud kuluaruande summale 15 000 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="5307e-203">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="5307e-204">Kuluaruanne on praegu määratud Suele, Jole ja Billile.</span><span class="sxs-lookup"><span data-stu-id="5307e-204">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="5307e-205">Kui Sue ja Jo kinnitavad dokumendi esimesena, siis rakendatakse nende võetud meetmeid dokumendil.</span><span class="sxs-lookup"><span data-stu-id="5307e-205">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document.</span></span>

        - <span data-ttu-id="5307e-206">Kui Sue kinnitab dokumendi, kuid Jo lükkab selle tagasi, lükatakse dokument tagasi ja saadetakse tagasi Samile.</span><span class="sxs-lookup"><span data-stu-id="5307e-206">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="5307e-207">Kui Sue ja Jo mõlemad kinnitavad dokumendi, saadetakse see Annile kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="5307e-207">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="5307e-208">**Kinnitajate protsent** – tegevus, mis rakendatakse dokumendile, määratakse siis, kui teatud protsent kinnitajaid vastavad.</span><span class="sxs-lookup"><span data-stu-id="5307e-208">**Percentage of approvers** – The action that is applied to the document is determined when a specific percentage of the approvers respond.</span></span> <span data-ttu-id="5307e-209">Näiteks Sam on edastanud kuluaruande summale 15 000 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="5307e-209">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="5307e-210">Kuluaruanne on praegu määratud Suele, Jole ja Billile ja te sisestasite protsendiks **50**.</span><span class="sxs-lookup"><span data-stu-id="5307e-210">The expense report is currently assigned to Sue, Jo, and Bill, and you entered **50** as the percentage.</span></span> <span data-ttu-id="5307e-211">Kui Sue ja Jo kinnitavad dokumendi esimesena, siis rakendatakse nende tehtud toiming dokumendile, kuna nad täidavad kinnitajate 50-protsendilist nõuet.</span><span class="sxs-lookup"><span data-stu-id="5307e-211">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document, because they meet the requirement for 50 percent of approvers.</span></span>

        - <span data-ttu-id="5307e-212">Kui Sue kinnitab dokumendi, kuid Jo lükkab selle tagasi, lükatakse dokument tagasi ja saadetakse tagasi Samile.</span><span class="sxs-lookup"><span data-stu-id="5307e-212">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="5307e-213">Kui Sue ja Jo mõlemad kinnitavad dokumendi, saadetakse see Annile kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="5307e-213">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="5307e-214">**Kõik kinnitajad** – kõik kinnitajad peavad dokumendi kinnitama.</span><span class="sxs-lookup"><span data-stu-id="5307e-214">**All approvers** – All the approvers must approve the document.</span></span> <span data-ttu-id="5307e-215">Vastasel juhul ei saa töövoog jätkuda.</span><span class="sxs-lookup"><span data-stu-id="5307e-215">Otherwise, the workflow can't continue.</span></span> <span data-ttu-id="5307e-216">Näiteks Sam on edastanud kuluaruande summale 15 000 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="5307e-216">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="5307e-217">Kuluaruanne on praegu määratud Suele, Jole ja Billile.</span><span class="sxs-lookup"><span data-stu-id="5307e-217">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="5307e-218">Kui Sue ja Jo kinnitavad dokumendi, kuid Bill lükkab selle tagasi, lükatakse dokument tagasi ja saadetakse tagasi Samile.</span><span class="sxs-lookup"><span data-stu-id="5307e-218">If Sue and Joe approve the document, but Bill rejects it, the document is rejected and sent back to Sam.</span></span> <span data-ttu-id="5307e-219">Kui Sue, Jo ja Bill kõik kinnitavad dokumendi, saadetakse see Annile kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="5307e-219">If Sue, Jo, and Bill all approve the document, it's sent to Ann for approval.</span></span>

## <a name="specify-when-the-approval-step-is-required"></a><span data-ttu-id="5307e-220">Määrake, millal on kinnitamisetapp vajalik</span><span class="sxs-lookup"><span data-stu-id="5307e-220">Specify when the approval step is required</span></span>

<span data-ttu-id="5307e-221">Saate määrata, millal kinnitamisetapp on vajalik.</span><span class="sxs-lookup"><span data-stu-id="5307e-221">You can specify when the approval step is required.</span></span> <span data-ttu-id="5307e-222">Kinnitamisetapp võib alati olla vajalik või see võib olla vajalik ainult juhul, kui teatud tingimused on täidetud.</span><span class="sxs-lookup"><span data-stu-id="5307e-222">The approval step can always be required, or it can be required only if specific conditions are met.</span></span>

### <a name="the-approval-step-is-always-required"></a><span data-ttu-id="5307e-223">Kinnitamisetapp on alati vajalik</span><span class="sxs-lookup"><span data-stu-id="5307e-223">The approval step is always required</span></span>

<span data-ttu-id="5307e-224">Järgige neid etappe, kui kinnitusetapp on alati vajalik.</span><span class="sxs-lookup"><span data-stu-id="5307e-224">Follow these steps if the approval step is always required.</span></span>

1. <span data-ttu-id="5307e-225">Vasakul paanil klõpsake nuppu **Tingimus**.</span><span class="sxs-lookup"><span data-stu-id="5307e-225">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="5307e-226">Valige suvand **Käivita see samm alati**.</span><span class="sxs-lookup"><span data-stu-id="5307e-226">Select the **Always run this step** option.</span></span>

### <a name="the-approval-step-is-required-in-specific-conditions"></a><span data-ttu-id="5307e-227">Kinnitussamm on vajalik teatud tingimustes</span><span class="sxs-lookup"><span data-stu-id="5307e-227">The approval step is required in specific conditions</span></span>

<span data-ttu-id="5307e-228">Teie konfigureeritav kinnitusetapp on vajalik ainult teatud tingimustel.</span><span class="sxs-lookup"><span data-stu-id="5307e-228">The approval step that you're configuring might be required only if specific conditions are met.</span></span> <span data-ttu-id="5307e-229">Näiteks kui konfigureerite kinnitusetappi ostutaotluse töövoole, võite soovida, et kinnitusetapp esineb ainult siis, kui ostutaotluse summa on rohkem kui 10 000 USA dollarit.</span><span class="sxs-lookup"><span data-stu-id="5307e-229">For example, if you're configuring an approval step for a purchase requisition workflow, you might want the approval step to occur only if the amount of the purchase requisition is more than USD 10,000.</span></span> <span data-ttu-id="5307e-230">Järgige neid etappe, et määrata, millal kinnitamisetapp on vajalik.</span><span class="sxs-lookup"><span data-stu-id="5307e-230">Follow these steps to specify when the approval step is required.</span></span>

1. <span data-ttu-id="5307e-231">Vasakul paanil klõpsake nuppu **Tingimus**.</span><span class="sxs-lookup"><span data-stu-id="5307e-231">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="5307e-232">Valige suvand **Käivita see samm üksnes siis, kui järgmine tingimus on täidetud**.</span><span class="sxs-lookup"><span data-stu-id="5307e-232">Select the **Run this step only when the following condition is met** option.</span></span>
3. <span data-ttu-id="5307e-233">Sisestage tingimus.</span><span class="sxs-lookup"><span data-stu-id="5307e-233">Enter a condition.</span></span>
4. <span data-ttu-id="5307e-234">Sisestage täiendavad vajalikud tingimused.</span><span class="sxs-lookup"><span data-stu-id="5307e-234">Enter any additional conditions that are required.</span></span>
5. <span data-ttu-id="5307e-235">Kinnitamaks, et teie sisestatud tingimused on õigesti konfigureeritud, järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="5307e-235">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="5307e-236">Klõpsake nuppu **Test**.</span><span class="sxs-lookup"><span data-stu-id="5307e-236">Click **Test**.</span></span>
    2. <span data-ttu-id="5307e-237">Lehel **Testi töövoo tingimus** alas **Kontrolli tingimust** valige kirje.</span><span class="sxs-lookup"><span data-stu-id="5307e-237">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="5307e-238">Klõpsake nuppu **Test**.</span><span class="sxs-lookup"><span data-stu-id="5307e-238">Click **Test**.</span></span> <span data-ttu-id="5307e-239">Süsteem hindab kirjet otsustamaks, kas see vastab teie määratud tingimustele.</span><span class="sxs-lookup"><span data-stu-id="5307e-239">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="5307e-240">Klõpsake **OK** või valikut **Tühista**, et naasta lehele **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="5307e-240">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-what-happens-when-the-document-is-overdue"></a><span data-ttu-id="5307e-241">Määrake, mis juhtub, kui dokument on hilinenud</span><span class="sxs-lookup"><span data-stu-id="5307e-241">Specify what happens when the document is overdue</span></span>

<span data-ttu-id="5307e-242">Kui kasutaja ei reageeri dokumendile määratud aja jooksul, siis on dokument hilinenud.</span><span class="sxs-lookup"><span data-stu-id="5307e-242">If a user doesn't take action on a document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="5307e-243">Hilinenud dokumenti saab laiendada või automaatselt kinnitamiseks teisele kasutajale määrata.</span><span class="sxs-lookup"><span data-stu-id="5307e-243">A document that is overdue can be escalated, or automatically assigned to another user for approval.</span></span> <span data-ttu-id="5307e-244">Järgige neid etappe dokumendi laiendamiseks, kui see on hilinenud.</span><span class="sxs-lookup"><span data-stu-id="5307e-244">Follow these steps to escalate the document if it's overdue.</span></span>

1. <span data-ttu-id="5307e-245">Vasakul paanil klõpsake valikut **Laiendus**.</span><span class="sxs-lookup"><span data-stu-id="5307e-245">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="5307e-246">Laiendustee loomiseks märkige ruut **Laiendustee kasutamine**.</span><span class="sxs-lookup"><span data-stu-id="5307e-246">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="5307e-247">Süsteem määrab dokumendi automaatselt laiendamistee nimekirjas olevatele kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="5307e-247">The system automatically assigns the document to the users who are listed in the escalation path.</span></span> <span data-ttu-id="5307e-248">Näiteks tähistab järgmine tabel laiendusteed.</span><span class="sxs-lookup"><span data-stu-id="5307e-248">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="5307e-249">Seeria</span><span class="sxs-lookup"><span data-stu-id="5307e-249">Sequence</span></span> | <span data-ttu-id="5307e-250">Laiendustee</span><span class="sxs-lookup"><span data-stu-id="5307e-250">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="5307e-251">1</span><span class="sxs-lookup"><span data-stu-id="5307e-251">1</span></span>        | <span data-ttu-id="5307e-252">Määra isikule: Donna</span><span class="sxs-lookup"><span data-stu-id="5307e-252">Assign to: Donna</span></span>     |
    | <span data-ttu-id="5307e-253">2</span><span class="sxs-lookup"><span data-stu-id="5307e-253">2</span></span>        | <span data-ttu-id="5307e-254">Määra isikule: Erin</span><span class="sxs-lookup"><span data-stu-id="5307e-254">Assign to: Erin</span></span>      |
    | <span data-ttu-id="5307e-255">3</span><span class="sxs-lookup"><span data-stu-id="5307e-255">3</span></span>        | <span data-ttu-id="5307e-256">Lõpptegevus: lükka tagasi</span><span class="sxs-lookup"><span data-stu-id="5307e-256">Final action: Reject</span></span> |

    <span data-ttu-id="5307e-257">Sellise näite korral määrab süsteem hilinenud dokumendi Donnale.</span><span class="sxs-lookup"><span data-stu-id="5307e-257">In this example, the system assigns the overdue document to Donna.</span></span> <span data-ttu-id="5307e-258">Kui Donna ei vasta määratud aja jooksul, siis määrab süsteem dokumendi Erinile.</span><span class="sxs-lookup"><span data-stu-id="5307e-258">If Donna doesn't respond in the allotted time, the system assigns the document to Erin.</span></span> <span data-ttu-id="5307e-259">Kui Erin ei vasta määratud aja jooksul, siis lükkab süsteem dokumendi tagasi.</span><span class="sxs-lookup"><span data-stu-id="5307e-259">If Erin doesn't respond in the allotted time, the system rejects the document.</span></span>

3. <span data-ttu-id="5307e-260">Laiendustee kasutajale lisamiseks klõpsake valikut **Laienduse lisamine**.</span><span class="sxs-lookup"><span data-stu-id="5307e-260">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="5307e-261">Vahekaardil **Määramise tüüp** valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe enne, kui lähete 4 etappi.</span><span class="sxs-lookup"><span data-stu-id="5307e-261">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="5307e-262">Suvand</span><span class="sxs-lookup"><span data-stu-id="5307e-262">Option</span></span></th>
    <th><span data-ttu-id="5307e-263">Kasutajad, kellele dokument on laiendatud</span><span class="sxs-lookup"><span data-stu-id="5307e-263">Users that the document is escalated to</span></span></th>
    <th><span data-ttu-id="5307e-264">Täiendavad etapid</span><span class="sxs-lookup"><span data-stu-id="5307e-264">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="5307e-265">Hierarhia</span><span class="sxs-lookup"><span data-stu-id="5307e-265">Hierarchy</span></span></td>
    <td><span data-ttu-id="5307e-266">Kasutaja spetsiifilises organisatsioonilises hierarhias</span><span class="sxs-lookup"><span data-stu-id="5307e-266">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5307e-267">Kui olete valinud suvandi <strong>Hierarhia</strong> vahekaardil <strong>Hierarhia valik</strong> loendis <strong>Hierarhia tüüp</strong>, valige hierarhia tüüp, millele dokument laiendada.</span><span class="sxs-lookup"><span data-stu-id="5307e-267">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the document to.</span></span></li>
    <li><span data-ttu-id="5307e-268">Süsteem peab hierarhiast tooma kasutajanimede vahemiku.</span><span class="sxs-lookup"><span data-stu-id="5307e-268">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="5307e-269">Need nimed tähistavad kasutajaid, kellele dokumenti saab laiendada.</span><span class="sxs-lookup"><span data-stu-id="5307e-269">These names represent users that the document can be escalated to.</span></span> <span data-ttu-id="5307e-270">Järgige neid etappe, et määrata nende kasutajanimede vahemiku algus- ja lõpp-punkt, mida kasutaja toob.</span><span class="sxs-lookup"><span data-stu-id="5307e-270">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="5307e-271">Alguspunkti määramiseks valige isik loendist <strong>Alguspunkt</strong>.</span><span class="sxs-lookup"><span data-stu-id="5307e-271">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="5307e-272">Lõpp-punkti määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="5307e-272">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="5307e-273">Seejärel sisestage tingimus, mis määrab, kus hierarhias lõpetab süsteem nimede toomise.</span><span class="sxs-lookup"><span data-stu-id="5307e-273">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="5307e-274">Vahekaardil <strong>Hierarhiasuvandid</strong> määrake, millistele kasutajatele vahemikus tuleb dokument määrata.</span><span class="sxs-lookup"><span data-stu-id="5307e-274">On the <strong>Hierarchy options</strong> tab, specify which users in the range the document should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="5307e-275"><strong>Määra kõikidele toodud kasutajatele</strong> – dokument laiendatakse kõikidele kasutajatele vahemikus.</span><span class="sxs-lookup"><span data-stu-id="5307e-275"><strong>Assign to all users retrieved</strong> – The document is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="5307e-276"><strong>Määra ainult viimati toodud kasutajale</strong> – dokumenti laiendatakse ainult viimasele kasutajale vahemikus.</span><span class="sxs-lookup"><span data-stu-id="5307e-276"><strong>Assign only to last user retrieved</strong> – The document is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="5307e-277"><strong>Välista kasutajatelt järgmise tingimusega</strong> – dokumenti ei laiendata vahemiku ühelegi kasutajale, kes vastavad teatud tingimusele.</span><span class="sxs-lookup"><span data-stu-id="5307e-277"><strong>Exclude users with the following condition</strong> – The document isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="5307e-278">Tingimuse määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="5307e-278">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5307e-279">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="5307e-279">Workflow user</span></span></td>
    <td><span data-ttu-id="5307e-280">Kasutajad praeguses töövoos</span><span class="sxs-lookup"><span data-stu-id="5307e-280">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="5307e-281">Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</span><span class="sxs-lookup"><span data-stu-id="5307e-281">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="5307e-282">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="5307e-282">User</span></span></td>
    <td><span data-ttu-id="5307e-283">Kindlad kasutajad</span><span class="sxs-lookup"><span data-stu-id="5307e-283">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="5307e-284">Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="5307e-284">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="5307e-285">Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="5307e-285">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="5307e-286">Valige kasutajad, kellele dokumenti laiendada ja liigutage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="5307e-286">Select the users to escalate the document to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="5307e-287">Vahekaardi **Ajalimiit** väljal **Kestus** määrake, kui palju aega on kasutajal dokumentidele reageerida või vastata.</span><span class="sxs-lookup"><span data-stu-id="5307e-287">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents.</span></span> <span data-ttu-id="5307e-288">Tehke üks järgmistest valikutest:</span><span class="sxs-lookup"><span data-stu-id="5307e-288">Select one of the following options:</span></span>

    - <span data-ttu-id="5307e-289">**Tunnid** – sisestage tundide arv, kui kaua on kasutajal aega vastata.</span><span class="sxs-lookup"><span data-stu-id="5307e-289">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="5307e-290">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="5307e-290">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5307e-291">**Päevad** – sisestage päevade arv, kui kaua on kasutajal aega vastata.</span><span class="sxs-lookup"><span data-stu-id="5307e-291">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="5307e-292">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="5307e-292">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="5307e-293">**Nädalad** – sisestage nädalate arv, kui kaua on kasutajal aega vastata.</span><span class="sxs-lookup"><span data-stu-id="5307e-293">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="5307e-294">**Kuud** – valige päev ja nädal, mis ajaks kasutaja peab vastama</span><span class="sxs-lookup"><span data-stu-id="5307e-294">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="5307e-295">Näiteks võite soovida kasutajalt vastust saada kuu kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="5307e-295">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="5307e-296">**Aastad** – valige päev, nädal ja kuu, mis ajaks kasutaja peab vastama</span><span class="sxs-lookup"><span data-stu-id="5307e-296">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="5307e-297">Näiteks võite soovida kasutajalt vastust detsembri kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="5307e-297">For example, you might want the user to respond by Friday of the third week of December.</span></span>

5. <span data-ttu-id="5307e-298">Korrake etappe 3 kuni 4 iga kasutaja puhul, kes tuleb laiendusteele lisada.</span><span class="sxs-lookup"><span data-stu-id="5307e-298">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="5307e-299">Saate muuta kasutajate järjekorda.</span><span class="sxs-lookup"><span data-stu-id="5307e-299">You can change the order of the users.</span></span>
6. <span data-ttu-id="5307e-300">Kui kasutajad laiendusteel ei reageeri määratud aja jooksul, siis reageerib süsteem dokumendile automaatselt.</span><span class="sxs-lookup"><span data-stu-id="5307e-300">If the users in the escalation path don't respond in the allotted time, the system automatically take action on the document.</span></span> <span data-ttu-id="5307e-301">Süsteemi tegevuse määramiseks valige rida **Tegevus** ja seejärel valige tegevus vahekaardi **Lõpptegevus**.</span><span class="sxs-lookup"><span data-stu-id="5307e-301">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>
