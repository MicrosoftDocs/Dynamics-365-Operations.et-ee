---
title: Töövoos käsitsi otsuste konfigureerimine
description: See teema selgitab, kuidas konfigureerida käsitsi otsuse atribuute.
author: ChrisGarty
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e16ed97351423a50aff433d535ea4c575d97e7fd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747875"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="1870f-103">Töövoos käsitsi otsuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="1870f-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1870f-104">See teema selgitab, kuidas konfigureerida käsitsi otsuse atribuute.</span><span class="sxs-lookup"><span data-stu-id="1870f-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="1870f-105">Töövoo redaktoris käsitsi otsuse loomiseks paremklõpsake käsitsi otsust ja seejärel klõpsake suvandit **Atribuudid**, et avada lehekülg **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="1870f-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="1870f-106">Seejärel kasutage järgmisi protseduure, et konfigureerida käsitsi otsuse atribuudid.</span><span class="sxs-lookup"><span data-stu-id="1870f-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="1870f-107">Andke otsusele nimi</span><span class="sxs-lookup"><span data-stu-id="1870f-107">Name the decision</span></span>

<span data-ttu-id="1870f-108">Käsitsi otsusele nime sisestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="1870f-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="1870f-109">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="1870f-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="1870f-110">Väljal **Nimi** sisestage käsitsi üksuse jaoks kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="1870f-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="1870f-111">Sisestage teemarida ja juhendid</span><span class="sxs-lookup"><span data-stu-id="1870f-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="1870f-112">Sisestage teemarida ja juhendid kasutajatele, kes on määratud käsitsi otsusele.</span><span class="sxs-lookup"><span data-stu-id="1870f-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="1870f-113">Näiteks kui konfigureerite ostutaotluste otsust, näeb kasutaja, kes on otsust määratud, teemarida ja juhiseid lehel **Ostutaotlused**.</span><span class="sxs-lookup"><span data-stu-id="1870f-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="1870f-114">Teemarida kuvatakse lehe teateribal.</span><span class="sxs-lookup"><span data-stu-id="1870f-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="1870f-115">Kasutaja saab seejärel juhiste vaatamiseks klõpsata teateriba.</span><span class="sxs-lookup"><span data-stu-id="1870f-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="1870f-116">Teemarea ja juhiste sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="1870f-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="1870f-117">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="1870f-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="1870f-118">Sisestage teemarida vahekaardi **Juhised** väljale **Tööüksuse teema**.</span><span class="sxs-lookup"><span data-stu-id="1870f-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="1870f-119">Teemarea isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="1870f-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="1870f-120">Kohatäitjad asendatakse teemarea kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="1870f-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="1870f-121">Kohatäitja sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="1870f-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="1870f-122">Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.</span><span class="sxs-lookup"><span data-stu-id="1870f-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="1870f-123">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="1870f-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="1870f-124">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="1870f-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="1870f-125">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="1870f-125">Click **Insert**.</span></span>

4. <span data-ttu-id="1870f-126">Teemarea tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="1870f-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="1870f-127">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="1870f-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="1870f-128">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="1870f-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="1870f-129">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="1870f-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="1870f-130">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="1870f-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="1870f-131">Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 3.</span><span class="sxs-lookup"><span data-stu-id="1870f-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="1870f-132">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="1870f-132">Click **Close**.</span></span>

5. <span data-ttu-id="1870f-133">Väljale **Tööüksuse juhised** sisestage juhised.</span><span class="sxs-lookup"><span data-stu-id="1870f-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="1870f-134">Juhiste isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="1870f-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="1870f-135">Kohatäitjad asendatakse juhiste kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="1870f-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="1870f-136">Kohatäitja sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="1870f-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="1870f-137">Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.</span><span class="sxs-lookup"><span data-stu-id="1870f-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="1870f-138">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="1870f-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="1870f-139">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="1870f-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="1870f-140">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="1870f-140">Click **Insert**.</span></span>

7. <span data-ttu-id="1870f-141">Juhiste tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="1870f-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="1870f-142">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="1870f-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="1870f-143">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="1870f-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="1870f-144">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="1870f-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="1870f-145">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="1870f-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="1870f-146">Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 6.</span><span class="sxs-lookup"><span data-stu-id="1870f-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="1870f-147">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="1870f-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="1870f-148">Määrake otsuse võimalikud tulemused</span><span class="sxs-lookup"><span data-stu-id="1870f-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="1870f-149">Tavaliselt määratakse dokument otsustajale juhul, kui otsustajale esitatakse küsimus.</span><span class="sxs-lookup"><span data-stu-id="1870f-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="1870f-150">Küsimuse vastus on tavaliselt **Jah** või **Ei** või **Tõene** või **Väär**.</span><span class="sxs-lookup"><span data-stu-id="1870f-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="1870f-151">Käsitsi otsuse võimalike tulemuste määramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="1870f-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="1870f-152">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="1870f-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="1870f-153">Sisestage vahekaardi **Tulemused** väljale **Tulemus 1** tulemuse nimi või suvand.</span><span class="sxs-lookup"><span data-stu-id="1870f-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="1870f-154">Tulemuse tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="1870f-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="1870f-155">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="1870f-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="1870f-156">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="1870f-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="1870f-157">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="1870f-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="1870f-158">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="1870f-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="1870f-159">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="1870f-159">Click **Close**.</span></span>

4. <span data-ttu-id="1870f-160">Sisestage väljale väljale **Tulemus 2** tulemuse nimi või suvand.</span><span class="sxs-lookup"><span data-stu-id="1870f-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="1870f-161">Tulemuse tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="1870f-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="1870f-162">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="1870f-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="1870f-163">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="1870f-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="1870f-164">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="1870f-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="1870f-165">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="1870f-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="1870f-166">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="1870f-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="1870f-167">Määrake, millal teatisi saadetakse</span><span class="sxs-lookup"><span data-stu-id="1870f-167">Specify when notifications are sent</span></span>

<span data-ttu-id="1870f-168">Saate saata inimestele teatisi, kui otsus langetatakse, delegeeritakse või eskaleeritakse.</span><span class="sxs-lookup"><span data-stu-id="1870f-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="1870f-169">Tehke järgmist, et määrata, millal ja kellele teatisi saadetakse.</span><span class="sxs-lookup"><span data-stu-id="1870f-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="1870f-170">Vasakul paanil klõpsake suvandit **Teatised**.</span><span class="sxs-lookup"><span data-stu-id="1870f-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="1870f-171">Märkige ruut sündmuste kõrval, mille puhul saadetakse teatis.</span><span class="sxs-lookup"><span data-stu-id="1870f-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="1870f-172">**\[1. valik\]** – määratud kasutaja on valinud suvandi **\[1. valik\]**.</span><span class="sxs-lookup"><span data-stu-id="1870f-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="1870f-173">**\[2. valik\]** – määratud kasutaja on valinud suvandi **\[2. valik\]**.</span><span class="sxs-lookup"><span data-stu-id="1870f-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="1870f-174">**Delegeerimine** – määratud kasutaja määras otsuse muule kasutajale.</span><span class="sxs-lookup"><span data-stu-id="1870f-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="1870f-175">**Eskaleerimine** – määratud kasutaja ei teinud otsust määratud aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="1870f-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="1870f-176">Valige 2. etapis valitud sündmuse rida.</span><span class="sxs-lookup"><span data-stu-id="1870f-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="1870f-177">Sisestage teatise tekst vahekaardil **Teatise tekst** olevale tekstiväljale.</span><span class="sxs-lookup"><span data-stu-id="1870f-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="1870f-178">Teatise isikupärastamiseks võite sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="1870f-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="1870f-179">Kohatäitjad asendatakse teatise kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="1870f-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="1870f-180">Kohatäitja sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="1870f-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="1870f-181">Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.</span><span class="sxs-lookup"><span data-stu-id="1870f-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="1870f-182">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="1870f-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="1870f-183">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="1870f-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="1870f-184">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="1870f-184">Click **Insert**.</span></span>

6. <span data-ttu-id="1870f-185">Teatise tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="1870f-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="1870f-186">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="1870f-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="1870f-187">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="1870f-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="1870f-188">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="1870f-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="1870f-189">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="1870f-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="1870f-190">Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 5.</span><span class="sxs-lookup"><span data-stu-id="1870f-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="1870f-191">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="1870f-191">Click **Close**.</span></span>

7. <span data-ttu-id="1870f-192">Määrake vahekaardil **Adressaat**, kellele teatised saadetakse.</span><span class="sxs-lookup"><span data-stu-id="1870f-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="1870f-193">Valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe, enne kui jätkate 8. etapiga.</span><span class="sxs-lookup"><span data-stu-id="1870f-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="1870f-194">Suvand</span><span class="sxs-lookup"><span data-stu-id="1870f-194">Option</span></span></th>
    <th><span data-ttu-id="1870f-195">Teatise adressaadid</span><span class="sxs-lookup"><span data-stu-id="1870f-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="1870f-196">Täiendavad etapid</span><span class="sxs-lookup"><span data-stu-id="1870f-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="1870f-197">Osaleja</span><span class="sxs-lookup"><span data-stu-id="1870f-197">Participant</span></span></td>
    <td><span data-ttu-id="1870f-198">Kasutajad, kes on määratud teatud grupile või rollile</span><span class="sxs-lookup"><span data-stu-id="1870f-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="1870f-199">Kui olete valinud suvandi <strong>Osaleja</strong> vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong>, valige grupi või rolli tüüp, millele teatisi saata.</span><span class="sxs-lookup"><span data-stu-id="1870f-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="1870f-200">Loendis <strong>Osaleja</strong> valige grupp, millele teatisi saata.</span><span class="sxs-lookup"><span data-stu-id="1870f-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="1870f-201">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="1870f-201">Workflow user</span></span></td>
    <td><span data-ttu-id="1870f-202">Kasutajad praeguses töövoos</span><span class="sxs-lookup"><span data-stu-id="1870f-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="1870f-203">Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</span><span class="sxs-lookup"><span data-stu-id="1870f-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="1870f-204">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="1870f-204">User</span></span></td>
    <td><span data-ttu-id="1870f-205">Kindlad kasutajad</span><span class="sxs-lookup"><span data-stu-id="1870f-205">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="1870f-206">Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="1870f-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="1870f-207">Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="1870f-207">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="1870f-208">Valige kasutajad, kellele teatisi saata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="1870f-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="1870f-209">Korrake 3.–7. toimingut iga sündmuse puhul, mille 2. etapis valisite.</span><span class="sxs-lookup"><span data-stu-id="1870f-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="1870f-210">Otsuse määramine</span><span class="sxs-lookup"><span data-stu-id="1870f-210">Assign a decision</span></span>

<span data-ttu-id="1870f-211">Järgige neid etappe, et valida, kellele käsitsi otsus määratakse.</span><span class="sxs-lookup"><span data-stu-id="1870f-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="1870f-212">Vasakul paanil klõpsake nuppu **Määramine**.</span><span class="sxs-lookup"><span data-stu-id="1870f-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="1870f-213">Vahekaardil **Määramise tüüp** valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe enne, kui lähete 3 etappi.</span><span class="sxs-lookup"><span data-stu-id="1870f-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="1870f-214">Suvand</span><span class="sxs-lookup"><span data-stu-id="1870f-214">Option</span></span></th>
    <th><span data-ttu-id="1870f-215">Kasutajad, kellele otsus on määratud</span><span class="sxs-lookup"><span data-stu-id="1870f-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="1870f-216">Täiendavad etapid</span><span class="sxs-lookup"><span data-stu-id="1870f-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="1870f-217">Osaleja</span><span class="sxs-lookup"><span data-stu-id="1870f-217">Participant</span></span></td>
    <td><span data-ttu-id="1870f-218">Kasutajad, kes on määratud teatud grupile või rollile</span><span class="sxs-lookup"><span data-stu-id="1870f-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="1870f-219">Kui olete valinud suvandi <strong>Osaleja</strong> vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong>, valige grupi või rolli tüüp, millele otsus määrata.</span><span class="sxs-lookup"><span data-stu-id="1870f-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="1870f-220">Loendis <strong>Osaleja</strong> valige grupp või roll, millele otsus määrata.</span><span class="sxs-lookup"><span data-stu-id="1870f-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="1870f-221">Hierarhia</span><span class="sxs-lookup"><span data-stu-id="1870f-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="1870f-222">Kasutaja spetsiifilises organisatsioonilises hierarhias</span><span class="sxs-lookup"><span data-stu-id="1870f-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="1870f-223">Kui olete valinud suvandi <strong>Hierarhia</strong> vahekaardil <strong>Hierarhia valik</strong> loendis <strong>Hierarhia tüüp</strong>, valige hierarhia tüüp, millele otsus määrata.</span><span class="sxs-lookup"><span data-stu-id="1870f-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="1870f-224">Süsteem peab hierarhiast tooma kasutajanimede vahemiku.</span><span class="sxs-lookup"><span data-stu-id="1870f-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="1870f-225">Need nimed tähistavad kasutajaid, kellele saab otsuse määrata.</span><span class="sxs-lookup"><span data-stu-id="1870f-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="1870f-226">Järgige neid etappe, et määrata nende kasutajanimede vahemiku algus- ja lõpp-punkt, mida kasutaja toob.</span><span class="sxs-lookup"><span data-stu-id="1870f-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="1870f-227">Alguspunkti määramiseks valige isik loendist <strong>Alguspunkt</strong>.</span><span class="sxs-lookup"><span data-stu-id="1870f-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="1870f-228">Lõpp-punkti määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="1870f-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="1870f-229">Seejärel sisestage tingimus, mis määrab, kus hierarhias lõpetab süsteem nimede toomise.</span><span class="sxs-lookup"><span data-stu-id="1870f-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="1870f-230">Vahekaardil <strong>Hierarhiasuvandid</strong> määrake, millistele kasutajatele vahemikus tuleb otsus määrata.</span><span class="sxs-lookup"><span data-stu-id="1870f-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="1870f-231"><strong>Määra kõikidele toodud kasutajatele</strong> – otsus määratakse kõikidele kasutajatele vahemikus.</span><span class="sxs-lookup"><span data-stu-id="1870f-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="1870f-232"><strong>Määra ainult viimati toodud kasutajale</strong> – otsus määratakse ainult viimasele kasutajale vahemikus.</span><span class="sxs-lookup"><span data-stu-id="1870f-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="1870f-233"><strong>Välista kasutajatelt järgmise tingimusega</strong> – otsust ei määrata vahemiku ühelegi kasutajale , kes vastavad teatud tingimusele.</span><span class="sxs-lookup"><span data-stu-id="1870f-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="1870f-234">Tingimuse määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="1870f-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="1870f-235">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="1870f-235">Workflow user</span></span></td>
    <td><span data-ttu-id="1870f-236">Kasutajad praeguses töövoos</span><span class="sxs-lookup"><span data-stu-id="1870f-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="1870f-237">Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</span><span class="sxs-lookup"><span data-stu-id="1870f-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="1870f-238">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="1870f-238">User</span></span></td>
    <td><span data-ttu-id="1870f-239">Kindlad kasutajad</span><span class="sxs-lookup"><span data-stu-id="1870f-239">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="1870f-240">Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="1870f-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="1870f-241">Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="1870f-241">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="1870f-242">Valige kasutajad, kellele otsus määrata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="1870f-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="1870f-243">Vahekaardi **Ajalimiit** väljal **Kestus** määrake, kui palju aega on kasutajal otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="1870f-243">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="1870f-244">Tehke üks järgmistest valikutest:</span><span class="sxs-lookup"><span data-stu-id="1870f-244">Select one of the following options:</span></span>

    - <span data-ttu-id="1870f-245">**Tunnid** – sisestage tundide arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="1870f-245">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="1870f-246">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="1870f-246">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="1870f-247">**Päevad** – sisestage päevade arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="1870f-247">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="1870f-248">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="1870f-248">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="1870f-249">**Nädalad** – sisestage nädalate arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="1870f-249">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="1870f-250">**Kuud** – valige päev ja nädal, mil kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="1870f-250">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="1870f-251">Näiteks soovite võib-olla, et kasutaja teeks otsuse kuu kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="1870f-251">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="1870f-252">**Aastad** – valige päev, nädal ja kuu, mil kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="1870f-252">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="1870f-253">Näiteks soovite võib-olla, et kasutaja teeks otsuse detsembri kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="1870f-253">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="1870f-254">Kui kasutaja ei tee otsust määratud aja jooksul, on otsuse tähtaeg ületatud.</span><span class="sxs-lookup"><span data-stu-id="1870f-254">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="1870f-255">Hilinenud otsust eskaleeritakse nende valikute põhjal, mille valite lehe alal **Laiendus**.</span><span class="sxs-lookup"><span data-stu-id="1870f-255">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="1870f-256">Määrake, mis juhtub tähtaja ületanud otsusega</span><span class="sxs-lookup"><span data-stu-id="1870f-256">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="1870f-257">Kui kasutaja ei tee otsust määratud aja jooksul, on otsuse tähtaeg ületatud.</span><span class="sxs-lookup"><span data-stu-id="1870f-257">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="1870f-258">Hilinenud otsuse saab eskaleerida või automaatselt muule kasutajale määrata.</span><span class="sxs-lookup"><span data-stu-id="1870f-258">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="1870f-259">Järgige neid etappe otsuse eskaleerimiseks, kui see on hilinenud.</span><span class="sxs-lookup"><span data-stu-id="1870f-259">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="1870f-260">Vasakul paanil klõpsake valikut **Laiendus**.</span><span class="sxs-lookup"><span data-stu-id="1870f-260">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="1870f-261">Laiendustee loomiseks märkige ruut **Laiendustee kasutamine**.</span><span class="sxs-lookup"><span data-stu-id="1870f-261">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="1870f-262">Süsteem määrab otsuse automaatselt laiendamistee nimekirjas olevatele kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="1870f-262">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="1870f-263">Näiteks tähistab järgmine tabel laiendusteed.</span><span class="sxs-lookup"><span data-stu-id="1870f-263">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="1870f-264">Seeria</span><span class="sxs-lookup"><span data-stu-id="1870f-264">Sequence</span></span> | <span data-ttu-id="1870f-265">Laiendustee</span><span class="sxs-lookup"><span data-stu-id="1870f-265">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="1870f-266">1</span><span class="sxs-lookup"><span data-stu-id="1870f-266">1</span></span>        | <span data-ttu-id="1870f-267">Määra isikule: Donna</span><span class="sxs-lookup"><span data-stu-id="1870f-267">Assign to: Donna</span></span>           |
    | <span data-ttu-id="1870f-268">2</span><span class="sxs-lookup"><span data-stu-id="1870f-268">2</span></span>        | <span data-ttu-id="1870f-269">Määra isikule: Erin</span><span class="sxs-lookup"><span data-stu-id="1870f-269">Assign to: Erin</span></span>            |
    | <span data-ttu-id="1870f-270">3</span><span class="sxs-lookup"><span data-stu-id="1870f-270">3</span></span>        | <span data-ttu-id="1870f-271">Lõplik tegevus: \[1. valik\]</span><span class="sxs-lookup"><span data-stu-id="1870f-271">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="1870f-272">Sellise näite korral määrab süsteem hilinenud otsuse Donnale.</span><span class="sxs-lookup"><span data-stu-id="1870f-272">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="1870f-273">Kui Donna ei tee otsust selleks ettenähtud aja jooksul, määrab süsteem otsuse Erinile.</span><span class="sxs-lookup"><span data-stu-id="1870f-273">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="1870f-274">Kui Erin ei tee otsust selleks ettenähtud aja jooksul, valib süsteem otsuseks suvandi **\[1. valik\]**.</span><span class="sxs-lookup"><span data-stu-id="1870f-274">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="1870f-275">Laiendustee kasutajale lisamiseks klõpsake valikut **Laienduse lisamine**.</span><span class="sxs-lookup"><span data-stu-id="1870f-275">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="1870f-276">Valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe, enne kui jätkate 4. etapiga.</span><span class="sxs-lookup"><span data-stu-id="1870f-276">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="1870f-277">Suvand</span><span class="sxs-lookup"><span data-stu-id="1870f-277">Option</span></span></th>
    <th><span data-ttu-id="1870f-278">Kasutajad, kellele otsus eskaleeritakse</span><span class="sxs-lookup"><span data-stu-id="1870f-278">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="1870f-279">Täiendavad etapid</span><span class="sxs-lookup"><span data-stu-id="1870f-279">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="1870f-280">Hierarhia</span><span class="sxs-lookup"><span data-stu-id="1870f-280">Hierarchy</span></span></td>
    <td><span data-ttu-id="1870f-281">Kasutaja spetsiifilises organisatsioonilises hierarhias</span><span class="sxs-lookup"><span data-stu-id="1870f-281">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="1870f-282">Kui olete valinud suvandi <strong>Hierarhia</strong> vahekaardil <strong>Hierarhia valik</strong> loendis <strong>Hierarhia tüüp</strong>, valige hierarhia tüüp, millele otsus eskaleerida.</span><span class="sxs-lookup"><span data-stu-id="1870f-282">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="1870f-283">Süsteem peab hierarhiast tooma kasutajanimede vahemiku.</span><span class="sxs-lookup"><span data-stu-id="1870f-283">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="1870f-284">Need nimed tähistavad kasutajaid, kellele saab otsust eskaleerida.</span><span class="sxs-lookup"><span data-stu-id="1870f-284">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="1870f-285">Järgige neid etappe, et määrata nende kasutajanimede vahemiku algus- ja lõpp-punkt, mida kasutaja toob.</span><span class="sxs-lookup"><span data-stu-id="1870f-285">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="1870f-286">Alguspunkti määramiseks valige isik loendist <strong>Alguspunkt</strong>.</span><span class="sxs-lookup"><span data-stu-id="1870f-286">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="1870f-287">Lõpp-punkti määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="1870f-287">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="1870f-288">Seejärel sisestage tingimus, mis määrab, kus hierarhias lõpetab süsteem nimede toomise.</span><span class="sxs-lookup"><span data-stu-id="1870f-288">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="1870f-289">Vahekaardil <strong>Hierarhiasuvandid</strong> määrake, millistele kasutajatele vahemikus tuleb otsus eskaleerida.</span><span class="sxs-lookup"><span data-stu-id="1870f-289">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="1870f-290"><strong>Määra kõikidele toodud kasutajatele</strong> – otsus eskaleeritakse kõikidele kasutajatele vahemikus.</span><span class="sxs-lookup"><span data-stu-id="1870f-290"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="1870f-291"><strong>Määra ainult viimati toodud kasutajale</strong> – otsus eskaleeritakse ainult viimasele kasutajale vahemikus.</span><span class="sxs-lookup"><span data-stu-id="1870f-291"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="1870f-292"><strong>Välista kasutajatelt järgmise tingimusega</strong> – otsust ei eskaleerita vahemiku ühelegi kasutajale , kes vastavad teatud tingimusele.</span><span class="sxs-lookup"><span data-stu-id="1870f-292"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="1870f-293">Tingimuse määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="1870f-293">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="1870f-294">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="1870f-294">Workflow user</span></span></td>
    <td><span data-ttu-id="1870f-295">Kasutajad praeguses töövoos</span><span class="sxs-lookup"><span data-stu-id="1870f-295">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="1870f-296">Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</span><span class="sxs-lookup"><span data-stu-id="1870f-296">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="1870f-297">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="1870f-297">User</span></span></td>
    <td><span data-ttu-id="1870f-298">Kindlad kasutajad</span><span class="sxs-lookup"><span data-stu-id="1870f-298">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="1870f-299">Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="1870f-299">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="1870f-300">Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="1870f-300">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="1870f-301">Valige kasutajad, kellele otsust eskaleerida, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="1870f-301">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="1870f-302">Vahekaardi **Ajalimiit** väljal **Kestus** määrake, kui palju aega on kasutajal otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="1870f-302">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="1870f-303">Tehke üks järgmistest valikutest:</span><span class="sxs-lookup"><span data-stu-id="1870f-303">Select one of the following options:</span></span>

    - <span data-ttu-id="1870f-304">**Tunnid** – sisestage tundide arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="1870f-304">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="1870f-305">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="1870f-305">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="1870f-306">**Päevad** – sisestage päevade arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="1870f-306">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="1870f-307">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="1870f-307">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="1870f-308">**Nädalad** – sisestage nädalate arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="1870f-308">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="1870f-309">**Kuud** – valige päev ja nädal, mil kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="1870f-309">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="1870f-310">Näiteks soovite võib-olla, et kasutaja teeks otsuse kuu kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="1870f-310">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="1870f-311">**Aastad** – valige päev, nädal ja kuu, mil kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="1870f-311">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="1870f-312">Näiteks soovite võib-olla, et kasutaja teeks otsuse detsembri kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="1870f-312">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="1870f-313">Korrake etappe 3 kuni 4 iga kasutaja puhul, kes tuleb laiendusteele lisada.</span><span class="sxs-lookup"><span data-stu-id="1870f-313">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="1870f-314">Saate muuta kasutajate järjekorda.</span><span class="sxs-lookup"><span data-stu-id="1870f-314">You can change the order of the users.</span></span>
6. <span data-ttu-id="1870f-315">Kui kasutajad eskaleerimisteel ei tee otsust määratud aja jooksul, langetab otsuse süsteem.</span><span class="sxs-lookup"><span data-stu-id="1870f-315">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="1870f-316">Süsteemi valitava suvandi määramiseks valige rida **Tegevus** ja seejärel valige suvand vahekaardi **Lõpptegevus**.</span><span class="sxs-lookup"><span data-stu-id="1870f-316">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="1870f-317">Ajalimiidi seadmine</span><span class="sxs-lookup"><span data-stu-id="1870f-317">Set a time limit</span></span>

<span data-ttu-id="1870f-318">Kui otsus tuleb teha teatud ajaks, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="1870f-318">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="1870f-319">Selle protseduuri käigus valitud suvandid alistavad lehe jaotistes **Määramine** ja **Eskaleerimine** valitud suvandid.</span><span class="sxs-lookup"><span data-stu-id="1870f-319">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="1870f-320">Klõpsake vasakpoolsel paanil suvandit **Täpsemad sätted**.</span><span class="sxs-lookup"><span data-stu-id="1870f-320">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="1870f-321">Märkige ruut **Määra töövoo elemendi jaoks ajalimiit**.</span><span class="sxs-lookup"><span data-stu-id="1870f-321">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="1870f-322">Määrake väljal **Kestus**, mis ajaks peab otsus olema tehtud.</span><span class="sxs-lookup"><span data-stu-id="1870f-322">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="1870f-323">Tehke üks järgmistest valikutest:</span><span class="sxs-lookup"><span data-stu-id="1870f-323">Select one of the following options:</span></span>

    - <span data-ttu-id="1870f-324">**Tunnid** – sisestage tundide arv.</span><span class="sxs-lookup"><span data-stu-id="1870f-324">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="1870f-325">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="1870f-325">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="1870f-326">**Päevad** – sisestage päevade arv.</span><span class="sxs-lookup"><span data-stu-id="1870f-326">**Days** – Enter the number of days.</span></span> <span data-ttu-id="1870f-327">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="1870f-327">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="1870f-328">**Nädalad** – sisestage nädalate arv.</span><span class="sxs-lookup"><span data-stu-id="1870f-328">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="1870f-329">**Kuud** – valige päev ja nädal, mis ajaks kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="1870f-329">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="1870f-330">Näiteks soovite võib-olla, et otsus oleks tehtud kuu kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="1870f-330">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="1870f-331">**Aastad** – valige päev, nädal ja kuu, mis ajaks kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="1870f-331">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="1870f-332">Näiteks soovite võib-olla, et otsus oleks tehtud detsembri kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="1870f-332">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="1870f-333">Ajalimiidi ületamisel langetab otsuse süsteem.</span><span class="sxs-lookup"><span data-stu-id="1870f-333">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="1870f-334">Loendist **Tegevus** valige suvand, mille süsteem peaks valima.</span><span class="sxs-lookup"><span data-stu-id="1870f-334">In the **Action** list, select the option that the system should select.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]