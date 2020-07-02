---
title: Töövoos käsitsi otsuste konfigureerimine
description: See teema selgitab, kuidas konfigureerida käsitsi otsuse atribuute.
author: sericks007
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 130cb50369c13bc3478340023c94f169ee5250cf
ms.sourcegitcommit: a5009c8958037afbaa1dd4f1469255b187ced93a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2020
ms.locfileid: "3455029"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="2b9ba-103">Töövoos käsitsi otsuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2b9ba-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b9ba-104">See teema selgitab, kuidas konfigureerida käsitsi otsuse atribuute.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="2b9ba-105">Töövoo redaktoris käsitsi otsuse loomiseks paremklõpsake käsitsi otsust ja seejärel klõpsake suvandit **Atribuudid**, et avada lehekülg **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="2b9ba-106">Seejärel kasutage järgmisi protseduure, et konfigureerida käsitsi otsuse atribuudid.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="2b9ba-107">Andke otsusele nimi</span><span class="sxs-lookup"><span data-stu-id="2b9ba-107">Name the decision</span></span>

<span data-ttu-id="2b9ba-108">Käsitsi otsusele nime sisestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="2b9ba-109">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2b9ba-110">Väljal **Nimi** sisestage käsitsi üksuse jaoks kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="2b9ba-111">Sisestage teemarida ja juhendid</span><span class="sxs-lookup"><span data-stu-id="2b9ba-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="2b9ba-112">Sisestage teemarida ja juhendid kasutajatele, kes on määratud käsitsi otsusele.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="2b9ba-113">Näiteks kui konfigureerite ostutaotluste otsust, näeb kasutaja, kes on otsust määratud, teemarida ja juhiseid lehel **Ostutaotlused**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="2b9ba-114">Teemarida kuvatakse lehe teateribal.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="2b9ba-115">Kasutaja saab seejärel juhiste vaatamiseks klõpsata teateriba.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="2b9ba-116">Teemarea ja juhiste sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="2b9ba-117">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2b9ba-118">Sisestage teemarida vahekaardi **Juhised** väljale **Tööüksuse teema**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="2b9ba-119">Teemarea isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="2b9ba-120">Kohatäitjad asendatakse teemarea kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="2b9ba-121">Kohatäitja sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="2b9ba-122">Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2b9ba-123">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2b9ba-124">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2b9ba-125">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-125">Click **Insert**.</span></span>

4. <span data-ttu-id="2b9ba-126">Teemarea tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="2b9ba-127">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="2b9ba-128">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2b9ba-129">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2b9ba-130">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2b9ba-131">Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 3.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="2b9ba-132">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-132">Click **Close**.</span></span>

5. <span data-ttu-id="2b9ba-133">Väljale **Tööüksuse juhised** sisestage juhised.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="2b9ba-134">Juhiste isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="2b9ba-135">Kohatäitjad asendatakse juhiste kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="2b9ba-136">Kohatäitja sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="2b9ba-137">Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2b9ba-138">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2b9ba-139">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2b9ba-140">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-140">Click **Insert**.</span></span>

7. <span data-ttu-id="2b9ba-141">Juhiste tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="2b9ba-142">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="2b9ba-143">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2b9ba-144">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2b9ba-145">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2b9ba-146">Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 6.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="2b9ba-147">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="2b9ba-148">Määrake otsuse võimalikud tulemused</span><span class="sxs-lookup"><span data-stu-id="2b9ba-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="2b9ba-149">Tavaliselt määratakse dokument otsustajale juhul, kui otsustajale esitatakse küsimus.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="2b9ba-150">Küsimuse vastus on tavaliselt **Jah** või **Ei** või **Tõene** või **Väär**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="2b9ba-151">Käsitsi otsuse võimalike tulemuste määramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="2b9ba-152">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="2b9ba-153">Sisestage vahekaardi **Tulemused** väljale **Tulemus 1** tulemuse nimi või suvand.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="2b9ba-154">Tulemuse tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="2b9ba-155">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="2b9ba-156">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2b9ba-157">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2b9ba-158">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2b9ba-159">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-159">Click **Close**.</span></span>

4. <span data-ttu-id="2b9ba-160">Sisestage väljale väljale **Tulemus 2** tulemuse nimi või suvand.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="2b9ba-161">Tulemuse tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="2b9ba-162">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="2b9ba-163">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2b9ba-164">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2b9ba-165">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2b9ba-166">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="2b9ba-167">Määrake, millal teatisi saadetakse</span><span class="sxs-lookup"><span data-stu-id="2b9ba-167">Specify when notifications are sent</span></span>

<span data-ttu-id="2b9ba-168">Saate saata inimestele teatisi, kui otsus langetatakse, delegeeritakse või eskaleeritakse.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="2b9ba-169">Tehke järgmist, et määrata, millal ja kellele teatisi saadetakse.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="2b9ba-170">Vasakul paanil klõpsake suvandit **Teatised**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="2b9ba-171">Märkige ruut sündmuste kõrval, mille puhul saadetakse teatis.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="2b9ba-172">**\[1. valik\]** – määratud kasutaja on valinud suvandi **\[1. valik\]**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="2b9ba-173">**\[2. valik\]** – määratud kasutaja on valinud suvandi **\[2. valik\]**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="2b9ba-174">**Delegeerimine** – määratud kasutaja määras otsuse muule kasutajale.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="2b9ba-175">**Eskaleerimine** – määratud kasutaja ei teinud otsust määratud aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="2b9ba-176">Valige 2. etapis valitud sündmuse rida.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="2b9ba-177">Sisestage teatise tekst vahekaardil **Teatise tekst** olevale tekstiväljale.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="2b9ba-178">Teatise isikupärastamiseks võite sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="2b9ba-179">Kohatäitjad asendatakse teatise kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="2b9ba-180">Kohatäitja sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="2b9ba-181">Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="2b9ba-182">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="2b9ba-183">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="2b9ba-184">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-184">Click **Insert**.</span></span>

6. <span data-ttu-id="2b9ba-185">Teatise tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="2b9ba-186">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="2b9ba-187">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="2b9ba-188">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="2b9ba-189">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="2b9ba-190">Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 5.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="2b9ba-191">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-191">Click **Close**.</span></span>

7. <span data-ttu-id="2b9ba-192">Määrake vahekaardil **Adressaat**, kellele teatised saadetakse.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="2b9ba-193">Valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe, enne kui jätkate 8. etapiga.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2b9ba-194">Suvand</span><span class="sxs-lookup"><span data-stu-id="2b9ba-194">Option</span></span></th>
    <th><span data-ttu-id="2b9ba-195">Teatise adressaadid</span><span class="sxs-lookup"><span data-stu-id="2b9ba-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="2b9ba-196">Täiendavad etapid</span><span class="sxs-lookup"><span data-stu-id="2b9ba-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2b9ba-197">Osaleja</span><span class="sxs-lookup"><span data-stu-id="2b9ba-197">Participant</span></span></td>
    <td><span data-ttu-id="2b9ba-198">Kasutajad, kes on määratud teatud grupile või rollile</span><span class="sxs-lookup"><span data-stu-id="2b9ba-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2b9ba-199">Kui olete valinud suvandi <strong>Osaleja</strong> vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong>, valige grupi või rolli tüüp, millele teatisi saata.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="2b9ba-200">Loendis <strong>Osaleja</strong> valige grupp, millele teatisi saata.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2b9ba-201">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="2b9ba-201">Workflow user</span></span></td>
    <td><span data-ttu-id="2b9ba-202">Kasutajad praeguses töövoos</span><span class="sxs-lookup"><span data-stu-id="2b9ba-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="2b9ba-203">Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2b9ba-204">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="2b9ba-204">User</span></span></td>
    <td><span data-ttu-id="2b9ba-205">Kindlad kasutajad</span><span class="sxs-lookup"><span data-stu-id="2b9ba-205">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2b9ba-206">Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2b9ba-207">Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-207">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="2b9ba-208">Valige kasutajad, kellele teatisi saata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="2b9ba-209">Korrake 3.–7. toimingut iga sündmuse puhul, mille 2. etapis valisite.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="2b9ba-210">Otsuse määramine</span><span class="sxs-lookup"><span data-stu-id="2b9ba-210">Assign a decision</span></span>

<span data-ttu-id="2b9ba-211">Järgige neid etappe, et valida, kellele käsitsi otsus määratakse.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="2b9ba-212">Vasakul paanil klõpsake nuppu **Määramine**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="2b9ba-213">Vahekaardil **Määramise tüüp** valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe enne, kui lähete 3 etappi.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2b9ba-214">Suvand</span><span class="sxs-lookup"><span data-stu-id="2b9ba-214">Option</span></span></th>
    <th><span data-ttu-id="2b9ba-215">Kasutajad, kellele otsus on määratud</span><span class="sxs-lookup"><span data-stu-id="2b9ba-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="2b9ba-216">Täiendavad etapid</span><span class="sxs-lookup"><span data-stu-id="2b9ba-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2b9ba-217">Osaleja</span><span class="sxs-lookup"><span data-stu-id="2b9ba-217">Participant</span></span></td>
    <td><span data-ttu-id="2b9ba-218">Kasutajad, kes on määratud teatud grupile või rollile</span><span class="sxs-lookup"><span data-stu-id="2b9ba-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2b9ba-219">Kui olete valinud suvandi <strong>Osaleja</strong> vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong>, valige grupi või rolli tüüp, millele otsus määrata.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="2b9ba-220">Loendis <strong>Osaleja</strong> valige grupp või roll, millele otsus määrata.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2b9ba-221">Hierarhia</span><span class="sxs-lookup"><span data-stu-id="2b9ba-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="2b9ba-222">Kasutaja spetsiifilises organisatsioonilises hierarhias</span><span class="sxs-lookup"><span data-stu-id="2b9ba-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2b9ba-223">Kui olete valinud suvandi <strong>Hierarhia</strong> vahekaardil <strong>Hierarhia valik</strong> loendis <strong>Hierarhia tüüp</strong>, valige hierarhia tüüp, millele otsus määrata.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="2b9ba-224">Süsteem peab hierarhiast tooma kasutajanimede vahemiku.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="2b9ba-225">Need nimed tähistavad kasutajaid, kellele saab otsuse määrata.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="2b9ba-226">Järgige neid etappe, et määrata nende kasutajanimede vahemiku algus- ja lõpp-punkt, mida kasutaja toob.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="2b9ba-227">Alguspunkti määramiseks valige isik loendist <strong>Alguspunkt</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="2b9ba-228">Lõpp-punkti määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="2b9ba-229">Seejärel sisestage tingimus, mis määrab, kus hierarhias lõpetab süsteem nimede toomise.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="2b9ba-230">Vahekaardil <strong>Hierarhiasuvandid</strong> määrake, millistele kasutajatele vahemikus tuleb otsus määrata.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="2b9ba-231"><strong>Määra kõikidele toodud kasutajatele</strong> – otsus määratakse kõikidele kasutajatele vahemikus.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="2b9ba-232"><strong>Määra ainult viimati toodud kasutajale</strong> – otsus määratakse ainult viimasele kasutajale vahemikus.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="2b9ba-233"><strong>Välista kasutajatelt järgmise tingimusega</strong> – otsust ei määrata vahemiku ühelegi kasutajale , kes vastavad teatud tingimusele.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="2b9ba-234">Tingimuse määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2b9ba-235">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="2b9ba-235">Workflow user</span></span></td>
    <td><span data-ttu-id="2b9ba-236">Kasutajad praeguses töövoos</span><span class="sxs-lookup"><span data-stu-id="2b9ba-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="2b9ba-237">Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2b9ba-238">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="2b9ba-238">User</span></span></td>
    <td><span data-ttu-id="2b9ba-239">Kindlad kasutajad</span><span class="sxs-lookup"><span data-stu-id="2b9ba-239">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2b9ba-240">Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2b9ba-241">Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-241">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="2b9ba-242">Valige kasutajad, kellele otsus määrata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="2b9ba-243">Vahekaardi **Ajalimiit** väljal **Kestus** määrake, kui palju aega on kasutajal otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-243">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="2b9ba-244">Tehke üks järgmistest valikutest:</span><span class="sxs-lookup"><span data-stu-id="2b9ba-244">Select one of the following options:</span></span>

    - <span data-ttu-id="2b9ba-245">**Tunnid** – sisestage tundide arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-245">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="2b9ba-246">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-246">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2b9ba-247">**Päevad** – sisestage päevade arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-247">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="2b9ba-248">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-248">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2b9ba-249">**Nädalad** – sisestage nädalate arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-249">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="2b9ba-250">**Kuud** – valige päev ja nädal, mil kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-250">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="2b9ba-251">Näiteks soovite võib-olla, et kasutaja teeks otsuse kuu kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-251">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="2b9ba-252">**Aastad** – valige päev, nädal ja kuu, mil kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-252">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="2b9ba-253">Näiteks soovite võib-olla, et kasutaja teeks otsuse detsembri kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-253">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="2b9ba-254">Kui kasutaja ei tee otsust määratud aja jooksul, on otsuse tähtaeg ületatud.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-254">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="2b9ba-255">Hilinenud otsust eskaleeritakse nende valikute põhjal, mille valite lehe alal **Laiendus**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-255">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="2b9ba-256">Määrake, mis juhtub tähtaja ületanud otsusega</span><span class="sxs-lookup"><span data-stu-id="2b9ba-256">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="2b9ba-257">Kui kasutaja ei tee otsust määratud aja jooksul, on otsuse tähtaeg ületatud.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-257">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="2b9ba-258">Hilinenud otsuse saab eskaleerida või automaatselt muule kasutajale määrata.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-258">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="2b9ba-259">Järgige neid etappe otsuse eskaleerimiseks, kui see on hilinenud.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-259">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="2b9ba-260">Vasakul paanil klõpsake valikut **Laiendus**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-260">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="2b9ba-261">Laiendustee loomiseks märkige ruut **Laiendustee kasutamine**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-261">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="2b9ba-262">Süsteem määrab otsuse automaatselt laiendamistee nimekirjas olevatele kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-262">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="2b9ba-263">Näiteks tähistab järgmine tabel laiendusteed.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-263">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="2b9ba-264">Seeria</span><span class="sxs-lookup"><span data-stu-id="2b9ba-264">Sequence</span></span> | <span data-ttu-id="2b9ba-265">Laiendustee</span><span class="sxs-lookup"><span data-stu-id="2b9ba-265">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="2b9ba-266">1</span><span class="sxs-lookup"><span data-stu-id="2b9ba-266">1</span></span>        | <span data-ttu-id="2b9ba-267">Määra isikule: Donna</span><span class="sxs-lookup"><span data-stu-id="2b9ba-267">Assign to: Donna</span></span>           |
    | <span data-ttu-id="2b9ba-268">2</span><span class="sxs-lookup"><span data-stu-id="2b9ba-268">2</span></span>        | <span data-ttu-id="2b9ba-269">Määra isikule: Erin</span><span class="sxs-lookup"><span data-stu-id="2b9ba-269">Assign to: Erin</span></span>            |
    | <span data-ttu-id="2b9ba-270">3</span><span class="sxs-lookup"><span data-stu-id="2b9ba-270">3</span></span>        | <span data-ttu-id="2b9ba-271">Lõplik tegevus: \[1. valik\]</span><span class="sxs-lookup"><span data-stu-id="2b9ba-271">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="2b9ba-272">Sellise näite korral määrab süsteem hilinenud otsuse Donnale.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-272">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="2b9ba-273">Kui Donna ei tee otsust selleks ettenähtud aja jooksul, määrab süsteem otsuse Erinile.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-273">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="2b9ba-274">Kui Erin ei tee otsust selleks ettenähtud aja jooksul, valib süsteem otsuseks suvandi **\[1. valik\]**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-274">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="2b9ba-275">Laiendustee kasutajale lisamiseks klõpsake valikut **Laienduse lisamine**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-275">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="2b9ba-276">Valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe, enne kui jätkate 4. etapiga.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-276">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="2b9ba-277">Suvand</span><span class="sxs-lookup"><span data-stu-id="2b9ba-277">Option</span></span></th>
    <th><span data-ttu-id="2b9ba-278">Kasutajad, kellele otsus eskaleeritakse</span><span class="sxs-lookup"><span data-stu-id="2b9ba-278">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="2b9ba-279">Täiendavad etapid</span><span class="sxs-lookup"><span data-stu-id="2b9ba-279">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="2b9ba-280">Hierarhia</span><span class="sxs-lookup"><span data-stu-id="2b9ba-280">Hierarchy</span></span></td>
    <td><span data-ttu-id="2b9ba-281">Kasutaja spetsiifilises organisatsioonilises hierarhias</span><span class="sxs-lookup"><span data-stu-id="2b9ba-281">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2b9ba-282">Kui olete valinud suvandi <strong>Hierarhia</strong> vahekaardil <strong>Hierarhia valik</strong> loendis <strong>Hierarhia tüüp</strong>, valige hierarhia tüüp, millele otsus eskaleerida.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-282">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="2b9ba-283">Süsteem peab hierarhiast tooma kasutajanimede vahemiku.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-283">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="2b9ba-284">Need nimed tähistavad kasutajaid, kellele saab otsust eskaleerida.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-284">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="2b9ba-285">Järgige neid etappe, et määrata nende kasutajanimede vahemiku algus- ja lõpp-punkt, mida kasutaja toob.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-285">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="2b9ba-286">Alguspunkti määramiseks valige isik loendist <strong>Alguspunkt</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-286">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="2b9ba-287">Lõpp-punkti määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-287">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="2b9ba-288">Seejärel sisestage tingimus, mis määrab, kus hierarhias lõpetab süsteem nimede toomise.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-288">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="2b9ba-289">Vahekaardil <strong>Hierarhiasuvandid</strong> määrake, millistele kasutajatele vahemikus tuleb otsus eskaleerida.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-289">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="2b9ba-290"><strong>Määra kõikidele toodud kasutajatele</strong> – otsus eskaleeritakse kõikidele kasutajatele vahemikus.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-290"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="2b9ba-291"><strong>Määra ainult viimati toodud kasutajale</strong> – otsus eskaleeritakse ainult viimasele kasutajale vahemikus.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-291"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="2b9ba-292"><strong>Välista kasutajatelt järgmise tingimusega</strong> – otsust ei eskaleerita vahemiku ühelegi kasutajale , kes vastavad teatud tingimusele.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-292"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="2b9ba-293">Tingimuse määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-293">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2b9ba-294">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="2b9ba-294">Workflow user</span></span></td>
    <td><span data-ttu-id="2b9ba-295">Kasutajad praeguses töövoos</span><span class="sxs-lookup"><span data-stu-id="2b9ba-295">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="2b9ba-296">Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-296">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="2b9ba-297">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="2b9ba-297">User</span></span></td>
    <td><span data-ttu-id="2b9ba-298">Kindlad kasutajad</span><span class="sxs-lookup"><span data-stu-id="2b9ba-298">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="2b9ba-299">Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-299">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="2b9ba-300">Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-300">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="2b9ba-301">Valige kasutajad, kellele otsust eskaleerida, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-301">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="2b9ba-302">Vahekaardi **Ajalimiit** väljal **Kestus** määrake, kui palju aega on kasutajal otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-302">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="2b9ba-303">Tehke üks järgmistest valikutest:</span><span class="sxs-lookup"><span data-stu-id="2b9ba-303">Select one of the following options:</span></span>

    - <span data-ttu-id="2b9ba-304">**Tunnid** – sisestage tundide arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-304">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="2b9ba-305">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-305">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2b9ba-306">**Päevad** – sisestage päevade arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-306">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="2b9ba-307">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-307">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2b9ba-308">**Nädalad** – sisestage nädalate arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-308">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="2b9ba-309">**Kuud** – valige päev ja nädal, mil kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-309">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="2b9ba-310">Näiteks soovite võib-olla, et kasutaja teeks otsuse kuu kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-310">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="2b9ba-311">**Aastad** – valige päev, nädal ja kuu, mil kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-311">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="2b9ba-312">Näiteks soovite võib-olla, et kasutaja teeks otsuse detsembri kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-312">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="2b9ba-313">Korrake etappe 3 kuni 4 iga kasutaja puhul, kes tuleb laiendusteele lisada.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-313">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="2b9ba-314">Saate muuta kasutajate järjekorda.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-314">You can change the order of the users.</span></span>
6. <span data-ttu-id="2b9ba-315">Kui kasutajad eskaleerimisteel ei tee otsust määratud aja jooksul, langetab otsuse süsteem.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-315">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="2b9ba-316">Süsteemi valitava suvandi määramiseks valige rida **Tegevus** ja seejärel valige suvand vahekaardi **Lõpptegevus**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-316">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="2b9ba-317">Ajalimiidi seadmine</span><span class="sxs-lookup"><span data-stu-id="2b9ba-317">Set a time limit</span></span>

<span data-ttu-id="2b9ba-318">Kui otsus tuleb teha teatud ajaks, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-318">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="2b9ba-319">Selle protseduuri käigus valitud suvandid alistavad lehe jaotistes **Määramine** ja **Eskaleerimine** valitud suvandid.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-319">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="2b9ba-320">Klõpsake vasakpoolsel paanil suvandit **Täpsemad sätted**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-320">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="2b9ba-321">Märkige ruut **Määra töövoo elemendi jaoks ajalimiit**.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-321">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="2b9ba-322">Määrake väljal **Kestus**, mis ajaks peab otsus olema tehtud.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-322">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="2b9ba-323">Tehke üks järgmistest valikutest:</span><span class="sxs-lookup"><span data-stu-id="2b9ba-323">Select one of the following options:</span></span>

    - <span data-ttu-id="2b9ba-324">**Tunnid** – sisestage tundide arv.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-324">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="2b9ba-325">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-325">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2b9ba-326">**Päevad** – sisestage päevade arv.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-326">**Days** – Enter the number of days.</span></span> <span data-ttu-id="2b9ba-327">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-327">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="2b9ba-328">**Nädalad** – sisestage nädalate arv.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-328">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="2b9ba-329">**Kuud** – valige päev ja nädal, mis ajaks kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-329">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="2b9ba-330">Näiteks soovite võib-olla, et otsus oleks tehtud kuu kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-330">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="2b9ba-331">**Aastad** – valige päev, nädal ja kuu, mis ajaks kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-331">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="2b9ba-332">Näiteks soovite võib-olla, et otsus oleks tehtud detsembri kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-332">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="2b9ba-333">Ajalimiidi ületamisel langetab otsuse süsteem.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-333">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="2b9ba-334">Loendist **Tegevus** valige suvand, mille süsteem peaks valima.</span><span class="sxs-lookup"><span data-stu-id="2b9ba-334">In the **Action** list, select the option that the system should select.</span></span>
