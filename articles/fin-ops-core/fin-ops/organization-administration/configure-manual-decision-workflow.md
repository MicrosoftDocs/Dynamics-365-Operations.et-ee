---
title: Töövoos käsitsi otsuste konfigureerimine
description: See teema selgitab, kuidas konfigureerida käsitsi otsuse atribuute.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
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
ms.openlocfilehash: f46b875f52d3d3e7c755ee92dcd5faddf0d94356
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177441"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="7447c-103">Töövoos käsitsi otsuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="7447c-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7447c-104">See teema selgitab, kuidas konfigureerida käsitsi otsuse atribuute.</span><span class="sxs-lookup"><span data-stu-id="7447c-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="7447c-105">Töövoo redaktoris käsitsi otsuse loomiseks paremklõpsake käsitsi otsust ja seejärel klõpsake suvandit **Atribuudid**, et avada lehekülg **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="7447c-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="7447c-106">Seejärel kasutage järgmisi protseduure, et konfigureerida käsitsi otsuse atribuudid.</span><span class="sxs-lookup"><span data-stu-id="7447c-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="7447c-107">Andke otsusele nimi</span><span class="sxs-lookup"><span data-stu-id="7447c-107">Name the decision</span></span>

<span data-ttu-id="7447c-108">Käsitsi otsusele nime sisestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="7447c-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="7447c-109">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="7447c-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="7447c-110">Väljal **Nimi** sisestage käsitsi üksuse jaoks kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="7447c-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="7447c-111">Sisestage teemarida ja juhendid</span><span class="sxs-lookup"><span data-stu-id="7447c-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="7447c-112">Sisestage teemarida ja juhendid kasutajatele, kes on määratud käsitsi otsusele.</span><span class="sxs-lookup"><span data-stu-id="7447c-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="7447c-113">Näiteks kui konfigureerite ostutaotluste otsust, näeb kasutaja, kes on otsust määratud, teemarida ja juhiseid lehel **Ostutaotlused**.</span><span class="sxs-lookup"><span data-stu-id="7447c-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="7447c-114">Teemarida kuvatakse lehe teateribal.</span><span class="sxs-lookup"><span data-stu-id="7447c-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="7447c-115">Kasutaja saab seejärel juhiste vaatamiseks klõpsata teateriba.</span><span class="sxs-lookup"><span data-stu-id="7447c-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="7447c-116">Teemarea ja juhiste sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="7447c-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="7447c-117">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="7447c-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="7447c-118">Sisestage teemarida vahekaardi **Juhised** väljale **Tööüksuse teema**.</span><span class="sxs-lookup"><span data-stu-id="7447c-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="7447c-119">Teemarea isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="7447c-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="7447c-120">Kohatäitjad asendatakse teemarea kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="7447c-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="7447c-121">Kohatäitja sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="7447c-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="7447c-122">Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.</span><span class="sxs-lookup"><span data-stu-id="7447c-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="7447c-123">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="7447c-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="7447c-124">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="7447c-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="7447c-125">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="7447c-125">Click **Insert**.</span></span>

4. <span data-ttu-id="7447c-126">Teemarea tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="7447c-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="7447c-127">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="7447c-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="7447c-128">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="7447c-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="7447c-129">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="7447c-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="7447c-130">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="7447c-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="7447c-131">Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 3.</span><span class="sxs-lookup"><span data-stu-id="7447c-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="7447c-132">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="7447c-132">Click **Close**.</span></span>

5. <span data-ttu-id="7447c-133">Väljale **Tööüksuse juhised** sisestage juhised.</span><span class="sxs-lookup"><span data-stu-id="7447c-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="7447c-134">Juhiste isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="7447c-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="7447c-135">Kohatäitjad asendatakse juhiste kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="7447c-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="7447c-136">Kohatäitja sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="7447c-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="7447c-137">Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.</span><span class="sxs-lookup"><span data-stu-id="7447c-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="7447c-138">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="7447c-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="7447c-139">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="7447c-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="7447c-140">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="7447c-140">Click **Insert**.</span></span>

7. <span data-ttu-id="7447c-141">Juhiste tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="7447c-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="7447c-142">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="7447c-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="7447c-143">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="7447c-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="7447c-144">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="7447c-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="7447c-145">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="7447c-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="7447c-146">Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 6.</span><span class="sxs-lookup"><span data-stu-id="7447c-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="7447c-147">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="7447c-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="7447c-148">Määrake otsuse võimalikud tulemused</span><span class="sxs-lookup"><span data-stu-id="7447c-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="7447c-149">Tavaliselt määratakse dokument otsustajale juhul, kui otsustajale esitatakse küsimus.</span><span class="sxs-lookup"><span data-stu-id="7447c-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="7447c-150">Küsimuse vastus on tavaliselt **Jah** või **Ei** või **Tõene** või **Väär**.</span><span class="sxs-lookup"><span data-stu-id="7447c-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="7447c-151">Käsitsi otsuse võimalike tulemuste määramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="7447c-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="7447c-152">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="7447c-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="7447c-153">Sisestage vahekaardi **Tulemused** väljale **Tulemus 1** tulemuse nimi või suvand.</span><span class="sxs-lookup"><span data-stu-id="7447c-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="7447c-154">Tulemuse tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="7447c-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="7447c-155">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="7447c-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="7447c-156">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="7447c-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="7447c-157">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="7447c-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="7447c-158">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="7447c-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="7447c-159">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="7447c-159">Click **Close**.</span></span>

4. <span data-ttu-id="7447c-160">Sisestage väljale väljale **Tulemus 2** tulemuse nimi või suvand.</span><span class="sxs-lookup"><span data-stu-id="7447c-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="7447c-161">Tulemuse tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="7447c-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="7447c-162">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="7447c-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="7447c-163">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="7447c-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="7447c-164">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="7447c-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="7447c-165">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="7447c-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="7447c-166">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="7447c-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="7447c-167">Määrake, millal teatisi saadetakse</span><span class="sxs-lookup"><span data-stu-id="7447c-167">Specify when notifications are sent</span></span>

<span data-ttu-id="7447c-168">Saate saata inimestele teatisi, kui otsus langetatakse, delegeeritakse või eskaleeritakse.</span><span class="sxs-lookup"><span data-stu-id="7447c-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="7447c-169">Tehke järgmist, et määrata, millal ja kellele teatisi saadetakse.</span><span class="sxs-lookup"><span data-stu-id="7447c-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="7447c-170">Vasakul paanil klõpsake suvandit **Teatised**.</span><span class="sxs-lookup"><span data-stu-id="7447c-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="7447c-171">Märkige ruut sündmuste kõrval, mille puhul saadetakse teatis.</span><span class="sxs-lookup"><span data-stu-id="7447c-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="7447c-172">**\[1. valik\]** – määratud kasutaja on valinud suvandi **\[1. valik\]**.</span><span class="sxs-lookup"><span data-stu-id="7447c-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="7447c-173">**\[2. valik\]** – määratud kasutaja on valinud suvandi **\[2. valik\]**.</span><span class="sxs-lookup"><span data-stu-id="7447c-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="7447c-174">**Delegeerimine** – määratud kasutaja määras otsuse muule kasutajale.</span><span class="sxs-lookup"><span data-stu-id="7447c-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="7447c-175">**Eskaleerimine** – määratud kasutaja ei teinud otsust määratud aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="7447c-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="7447c-176">Valige 2. etapis valitud sündmuse rida.</span><span class="sxs-lookup"><span data-stu-id="7447c-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="7447c-177">Sisestage teatise tekst vahekaardil **Teatise tekst** olevale tekstiväljale.</span><span class="sxs-lookup"><span data-stu-id="7447c-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="7447c-178">Teatise isikupärastamiseks võite sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="7447c-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="7447c-179">Kohatäitjad asendatakse teatise kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="7447c-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="7447c-180">Kohatäitja sisestamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="7447c-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="7447c-181">Tekstiboksis klõpsake seal, kuhu kohatäitja peaks ilmuma.</span><span class="sxs-lookup"><span data-stu-id="7447c-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="7447c-182">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="7447c-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="7447c-183">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="7447c-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="7447c-184">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="7447c-184">Click **Insert**.</span></span>

6. <span data-ttu-id="7447c-185">Teatise tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="7447c-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="7447c-186">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="7447c-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="7447c-187">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="7447c-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="7447c-188">Ilmuvas loendis valige see keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="7447c-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="7447c-189">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="7447c-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="7447c-190">Teksti isikupärastamiseks saate sisestada kohatäitjad, nagu on kirjeldatud etapis 5.</span><span class="sxs-lookup"><span data-stu-id="7447c-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="7447c-191">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="7447c-191">Click **Close**.</span></span>

7. <span data-ttu-id="7447c-192">Määrake vahekaardil **Adressaat**, kellele teatised saadetakse.</span><span class="sxs-lookup"><span data-stu-id="7447c-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="7447c-193">Valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe, enne kui jätkate 8. etapiga.</span><span class="sxs-lookup"><span data-stu-id="7447c-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="7447c-194">Suvand</span><span class="sxs-lookup"><span data-stu-id="7447c-194">Option</span></span></th>
    <th><span data-ttu-id="7447c-195">Teatise adressaadid</span><span class="sxs-lookup"><span data-stu-id="7447c-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="7447c-196">Täiendavad etapid</span><span class="sxs-lookup"><span data-stu-id="7447c-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="7447c-197">Osaleja</span><span class="sxs-lookup"><span data-stu-id="7447c-197">Participant</span></span></td>
    <td><span data-ttu-id="7447c-198">Kasutajad, kes on määratud teatud grupile või rollile</span><span class="sxs-lookup"><span data-stu-id="7447c-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="7447c-199">Kui olete valinud suvandi <strong>Osaleja</strong> vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong>, valige grupi või rolli tüüp, millele teatisi saata.</span><span class="sxs-lookup"><span data-stu-id="7447c-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="7447c-200">Loendis <strong>Osaleja</strong> valige grupp, millele teatisi saata.</span><span class="sxs-lookup"><span data-stu-id="7447c-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="7447c-201">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="7447c-201">Workflow user</span></span></td>
    <td><span data-ttu-id="7447c-202">Kasutajad praeguses töövoos</span><span class="sxs-lookup"><span data-stu-id="7447c-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="7447c-203">Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</span><span class="sxs-lookup"><span data-stu-id="7447c-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="7447c-204">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="7447c-204">User</span></span></td>
    <td><span data-ttu-id="7447c-205">Kindlad kasutajad</span><span class="sxs-lookup"><span data-stu-id="7447c-205">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="7447c-206">Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="7447c-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="7447c-207">Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="7447c-207">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="7447c-208">Valige kasutajad, kellele teatisi saata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="7447c-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="7447c-209">Korrake 3.–7. toimingut iga sündmuse puhul, mille 2. etapis valisite.</span><span class="sxs-lookup"><span data-stu-id="7447c-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="7447c-210">Otsuse määramine</span><span class="sxs-lookup"><span data-stu-id="7447c-210">Assign a decision</span></span>

<span data-ttu-id="7447c-211">Järgige neid etappe, et valida, kellele käsitsi otsus määratakse.</span><span class="sxs-lookup"><span data-stu-id="7447c-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="7447c-212">Vasakul paanil klõpsake nuppu **Määramine**.</span><span class="sxs-lookup"><span data-stu-id="7447c-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="7447c-213">Vahekaardil **Määramise tüüp** valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe enne, kui lähete 3 etappi.</span><span class="sxs-lookup"><span data-stu-id="7447c-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="7447c-214">Suvand</span><span class="sxs-lookup"><span data-stu-id="7447c-214">Option</span></span></th>
    <th><span data-ttu-id="7447c-215">Kasutajad, kellele otsus on määratud</span><span class="sxs-lookup"><span data-stu-id="7447c-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="7447c-216">Täiendavad etapid</span><span class="sxs-lookup"><span data-stu-id="7447c-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="7447c-217">Osaleja</span><span class="sxs-lookup"><span data-stu-id="7447c-217">Participant</span></span></td>
    <td><span data-ttu-id="7447c-218">Kasutajad, kes on määratud teatud grupile või rollile</span><span class="sxs-lookup"><span data-stu-id="7447c-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="7447c-219">Kui olete valinud suvandi <strong>Osaleja</strong> vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong>, valige grupi või rolli tüüp, millele otsus määrata.</span><span class="sxs-lookup"><span data-stu-id="7447c-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="7447c-220">Loendis <strong>Osaleja</strong> valige grupp või roll, millele otsus määrata.</span><span class="sxs-lookup"><span data-stu-id="7447c-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="7447c-221">Hierarhia</span><span class="sxs-lookup"><span data-stu-id="7447c-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="7447c-222">Kasutaja spetsiifilises organisatsioonilises hierarhias</span><span class="sxs-lookup"><span data-stu-id="7447c-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="7447c-223">Kui olete valinud suvandi <strong>Hierarhia</strong> vahekaardil <strong>Hierarhia valik</strong> loendis <strong>Hierarhia tüüp</strong>, valige hierarhia tüüp, millele otsus määrata.</span><span class="sxs-lookup"><span data-stu-id="7447c-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="7447c-224">Süsteem peab hierarhiast tooma kasutajanimede vahemiku.</span><span class="sxs-lookup"><span data-stu-id="7447c-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="7447c-225">Need nimed tähistavad kasutajaid, kellele saab otsuse määrata.</span><span class="sxs-lookup"><span data-stu-id="7447c-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="7447c-226">Järgige neid etappe, et määrata nende kasutajanimede vahemiku algus- ja lõpp-punkt, mida kasutaja toob.</span><span class="sxs-lookup"><span data-stu-id="7447c-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="7447c-227">Alguspunkti määramiseks valige isik loendist <strong>Alguspunkt</strong>.</span><span class="sxs-lookup"><span data-stu-id="7447c-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="7447c-228">Lõpp-punkti määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="7447c-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="7447c-229">Seejärel sisestage tingimus, mis määrab, kus hierarhias lõpetab süsteem nimede toomise.</span><span class="sxs-lookup"><span data-stu-id="7447c-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="7447c-230">Vahekaardil <strong>Hierarhiasuvandid</strong> määrake, millistele kasutajatele vahemikus tuleb otsus määrata.</span><span class="sxs-lookup"><span data-stu-id="7447c-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="7447c-231"><strong>Määra kõikidele toodud kasutajatele</strong> – otsus määratakse kõikidele kasutajatele vahemikus.</span><span class="sxs-lookup"><span data-stu-id="7447c-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="7447c-232"><strong>Määra ainult viimati toodud kasutajale</strong> – otsus määratakse ainult viimasele kasutajale vahemikus.</span><span class="sxs-lookup"><span data-stu-id="7447c-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="7447c-233"><strong>Välista kasutajatelt järgmise tingimusega</strong> – otsust ei määrata vahemiku ühelegi kasutajale , kes vastavad teatud tingimusele.</span><span class="sxs-lookup"><span data-stu-id="7447c-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="7447c-234">Tingimuse määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="7447c-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="7447c-235">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="7447c-235">Workflow user</span></span></td>
    <td><span data-ttu-id="7447c-236">Kasutajad praeguses töövoos</span><span class="sxs-lookup"><span data-stu-id="7447c-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="7447c-237">Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</span><span class="sxs-lookup"><span data-stu-id="7447c-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="7447c-238">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="7447c-238">User</span></span></td>
    <td><span data-ttu-id="7447c-239">Kindlad kasutajad</span><span class="sxs-lookup"><span data-stu-id="7447c-239">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="7447c-240">Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="7447c-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="7447c-241">Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="7447c-241">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="7447c-242">Valige kasutajad, kellele otsus määrata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="7447c-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="7447c-243">Järjekord</span><span class="sxs-lookup"><span data-stu-id="7447c-243">Queue</span></span></td>
    <td><span data-ttu-id="7447c-244">Tööüksuste järjekord</span><span class="sxs-lookup"><span data-stu-id="7447c-244">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="7447c-245">Pärast suvandi <strong>Järjekord</strong> valimist klõpsake vahekaarti <strong>Järjekorral põhinev</strong>.</span><span class="sxs-lookup"><span data-stu-id="7447c-245">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="7447c-246">Otsuse konkreetsesse järjekorda määramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="7447c-246">To assign the decision to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="7447c-247">Valige loendis <strong>Järjekorra tüüp</strong> suvand <strong>Tööüksuste järjekord</strong>.</span><span class="sxs-lookup"><span data-stu-id="7447c-247">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="7447c-248">Loendis <strong>Järjekorra nimi</strong> valige järjekord.</span><span class="sxs-lookup"><span data-stu-id="7447c-248">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="7447c-249">Kui konkreetne tingimus peab määrama, millisesse järjekorda otsus määratakse, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="7447c-249">If a specific condition should determine which queue the decision is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="7447c-250">Valige loendis <strong>Järjekorra tüüp</strong> suvand <strong>Tinglike tööüksuste järjekord</strong>.</span><span class="sxs-lookup"><span data-stu-id="7447c-250">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="7447c-251">Loendis <strong>Järjekorra nimi</strong> valige suvand <strong>Tinglik järjekord</strong>.</span><span class="sxs-lookup"><span data-stu-id="7447c-251">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="7447c-252">Suvandit kasutatakse ainult mõningate töövoogude puhul, nagu juhtumihaldus.</span><span class="sxs-lookup"><span data-stu-id="7447c-252">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="7447c-253">Vahekaardi **Ajalimiit** väljal **Kestus** määrake, kui palju aega on kasutajal otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="7447c-253">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="7447c-254">Tehke üks järgmistest valikutest:</span><span class="sxs-lookup"><span data-stu-id="7447c-254">Select one of the following options:</span></span>

    - <span data-ttu-id="7447c-255">**Tunnid** – sisestage tundide arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="7447c-255">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="7447c-256">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="7447c-256">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="7447c-257">**Päevad** – sisestage päevade arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="7447c-257">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="7447c-258">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="7447c-258">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="7447c-259">**Nädalad** – sisestage nädalate arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="7447c-259">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="7447c-260">**Kuud** – valige päev ja nädal, mil kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="7447c-260">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="7447c-261">Näiteks soovite võib-olla, et kasutaja teeks otsuse kuu kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="7447c-261">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="7447c-262">**Aastad** – valige päev, nädal ja kuu, mil kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="7447c-262">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="7447c-263">Näiteks soovite võib-olla, et kasutaja teeks otsuse detsembri kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="7447c-263">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="7447c-264">Kui kasutaja ei tee otsust määratud aja jooksul, on otsuse tähtaeg ületatud.</span><span class="sxs-lookup"><span data-stu-id="7447c-264">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="7447c-265">Hilinenud otsust eskaleeritakse nende valikute põhjal, mille valite lehe alal **Laiendus**.</span><span class="sxs-lookup"><span data-stu-id="7447c-265">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="7447c-266">Määrake, mis juhtub tähtaja ületanud otsusega</span><span class="sxs-lookup"><span data-stu-id="7447c-266">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="7447c-267">Kui kasutaja ei tee otsust määratud aja jooksul, on otsuse tähtaeg ületatud.</span><span class="sxs-lookup"><span data-stu-id="7447c-267">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="7447c-268">Hilinenud otsuse saab eskaleerida või automaatselt muule kasutajale määrata.</span><span class="sxs-lookup"><span data-stu-id="7447c-268">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="7447c-269">Järgige neid etappe otsuse eskaleerimiseks, kui see on hilinenud.</span><span class="sxs-lookup"><span data-stu-id="7447c-269">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="7447c-270">Vasakul paanil klõpsake valikut **Laiendus**.</span><span class="sxs-lookup"><span data-stu-id="7447c-270">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="7447c-271">Laiendustee loomiseks märkige ruut **Laiendustee kasutamine**.</span><span class="sxs-lookup"><span data-stu-id="7447c-271">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="7447c-272">Süsteem määrab otsuse automaatselt laiendamistee nimekirjas olevatele kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="7447c-272">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="7447c-273">Näiteks tähistab järgmine tabel laiendusteed.</span><span class="sxs-lookup"><span data-stu-id="7447c-273">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="7447c-274">Seeria</span><span class="sxs-lookup"><span data-stu-id="7447c-274">Sequence</span></span> | <span data-ttu-id="7447c-275">Laiendustee</span><span class="sxs-lookup"><span data-stu-id="7447c-275">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="7447c-276">1</span><span class="sxs-lookup"><span data-stu-id="7447c-276">1</span></span>        | <span data-ttu-id="7447c-277">Määra isikule: Donna</span><span class="sxs-lookup"><span data-stu-id="7447c-277">Assign to: Donna</span></span>           |
    | <span data-ttu-id="7447c-278">2</span><span class="sxs-lookup"><span data-stu-id="7447c-278">2</span></span>        | <span data-ttu-id="7447c-279">Määra isikule: Erin</span><span class="sxs-lookup"><span data-stu-id="7447c-279">Assign to: Erin</span></span>            |
    | <span data-ttu-id="7447c-280">3</span><span class="sxs-lookup"><span data-stu-id="7447c-280">3</span></span>        | <span data-ttu-id="7447c-281">Lõplik tegevus: \[1. valik\]</span><span class="sxs-lookup"><span data-stu-id="7447c-281">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="7447c-282">Sellise näite korral määrab süsteem hilinenud otsuse Donnale.</span><span class="sxs-lookup"><span data-stu-id="7447c-282">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="7447c-283">Kui Donna ei tee otsust selleks ettenähtud aja jooksul, määrab süsteem otsuse Erinile.</span><span class="sxs-lookup"><span data-stu-id="7447c-283">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="7447c-284">Kui Erin ei tee otsust selleks ettenähtud aja jooksul, valib süsteem otsuseks suvandi **\[1. valik\]**.</span><span class="sxs-lookup"><span data-stu-id="7447c-284">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="7447c-285">Laiendustee kasutajale lisamiseks klõpsake valikut **Laienduse lisamine**.</span><span class="sxs-lookup"><span data-stu-id="7447c-285">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="7447c-286">Valige järgmises tabelis üks valikutest ja seejärel järgige selle valiku täiendavaid etappe, enne kui jätkate 4. etapiga.</span><span class="sxs-lookup"><span data-stu-id="7447c-286">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="7447c-287">Suvand</span><span class="sxs-lookup"><span data-stu-id="7447c-287">Option</span></span></th>
    <th><span data-ttu-id="7447c-288">Kasutajad, kellele otsus eskaleeritakse</span><span class="sxs-lookup"><span data-stu-id="7447c-288">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="7447c-289">Täiendavad etapid</span><span class="sxs-lookup"><span data-stu-id="7447c-289">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="7447c-290">Hierarhia</span><span class="sxs-lookup"><span data-stu-id="7447c-290">Hierarchy</span></span></td>
    <td><span data-ttu-id="7447c-291">Kasutaja spetsiifilises organisatsioonilises hierarhias</span><span class="sxs-lookup"><span data-stu-id="7447c-291">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="7447c-292">Kui olete valinud suvandi <strong>Hierarhia</strong> vahekaardil <strong>Hierarhia valik</strong> loendis <strong>Hierarhia tüüp</strong>, valige hierarhia tüüp, millele otsus eskaleerida.</span><span class="sxs-lookup"><span data-stu-id="7447c-292">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="7447c-293">Süsteem peab hierarhiast tooma kasutajanimede vahemiku.</span><span class="sxs-lookup"><span data-stu-id="7447c-293">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="7447c-294">Need nimed tähistavad kasutajaid, kellele saab otsust eskaleerida.</span><span class="sxs-lookup"><span data-stu-id="7447c-294">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="7447c-295">Järgige neid etappe, et määrata nende kasutajanimede vahemiku algus- ja lõpp-punkt, mida kasutaja toob.</span><span class="sxs-lookup"><span data-stu-id="7447c-295">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="7447c-296">Alguspunkti määramiseks valige isik loendist <strong>Alguspunkt</strong>.</span><span class="sxs-lookup"><span data-stu-id="7447c-296">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="7447c-297">Lõpp-punkti määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="7447c-297">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="7447c-298">Seejärel sisestage tingimus, mis määrab, kus hierarhias lõpetab süsteem nimede toomise.</span><span class="sxs-lookup"><span data-stu-id="7447c-298">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="7447c-299">Vahekaardil <strong>Hierarhiasuvandid</strong> määrake, millistele kasutajatele vahemikus tuleb otsus eskaleerida.</span><span class="sxs-lookup"><span data-stu-id="7447c-299">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="7447c-300"><strong>Määra kõikidele toodud kasutajatele</strong> – otsus eskaleeritakse kõikidele kasutajatele vahemikus.</span><span class="sxs-lookup"><span data-stu-id="7447c-300"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="7447c-301"><strong>Määra ainult viimati toodud kasutajale</strong> – otsus eskaleeritakse ainult viimasele kasutajale vahemikus.</span><span class="sxs-lookup"><span data-stu-id="7447c-301"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="7447c-302"><strong>Välista kasutajatelt järgmise tingimusega</strong> – otsust ei eskaleerita vahemiku ühelegi kasutajale , kes vastavad teatud tingimusele.</span><span class="sxs-lookup"><span data-stu-id="7447c-302"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="7447c-303">Tingimuse määramiseks klõpsake valikut <strong>Lisa tingimus</strong>.</span><span class="sxs-lookup"><span data-stu-id="7447c-303">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="7447c-304">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="7447c-304">Workflow user</span></span></td>
    <td><span data-ttu-id="7447c-305">Kasutajad praeguses töövoos</span><span class="sxs-lookup"><span data-stu-id="7447c-305">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="7447c-306">Kui olete valinud suvandi <strong>Töövoo kasutaja</strong> vahekaardil <strong>Töövoo kasutaja</strong> loendis <strong>Töövoo kasutaja</strong> valige kasutaja, kes osaleb töövoos.</span><span class="sxs-lookup"><span data-stu-id="7447c-306">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="7447c-307">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="7447c-307">User</span></span></td>
    <td><span data-ttu-id="7447c-308">Kindlad kasutajad</span><span class="sxs-lookup"><span data-stu-id="7447c-308">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="7447c-309">Kui olete valinud suvandi <strong>Kasutaja</strong>, klõpsake vahekaarti <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="7447c-309">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="7447c-310">Loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="7447c-310">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="7447c-311">Valige kasutajad, kellele otsust eskaleerida, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="7447c-311">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="7447c-312">Vahekaardi **Ajalimiit** väljal **Kestus** määrake, kui palju aega on kasutajal otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="7447c-312">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="7447c-313">Tehke üks järgmistest valikutest:</span><span class="sxs-lookup"><span data-stu-id="7447c-313">Select one of the following options:</span></span>

    - <span data-ttu-id="7447c-314">**Tunnid** – sisestage tundide arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="7447c-314">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="7447c-315">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="7447c-315">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="7447c-316">**Päevad** – sisestage päevade arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="7447c-316">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="7447c-317">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="7447c-317">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="7447c-318">**Nädalad** – sisestage nädalate arv, kui kaua on kasutajal aega otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="7447c-318">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="7447c-319">**Kuud** – valige päev ja nädal, mil kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="7447c-319">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="7447c-320">Näiteks soovite võib-olla, et kasutaja teeks otsuse kuu kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="7447c-320">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="7447c-321">**Aastad** – valige päev, nädal ja kuu, mil kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="7447c-321">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="7447c-322">Näiteks soovite võib-olla, et kasutaja teeks otsuse detsembri kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="7447c-322">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="7447c-323">Korrake etappe 3 kuni 4 iga kasutaja puhul, kes tuleb laiendusteele lisada.</span><span class="sxs-lookup"><span data-stu-id="7447c-323">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="7447c-324">Saate muuta kasutajate järjekorda.</span><span class="sxs-lookup"><span data-stu-id="7447c-324">You can change the order of the users.</span></span>
6. <span data-ttu-id="7447c-325">Kui kasutajad eskaleerimisteel ei tee otsust määratud aja jooksul, langetab otsuse süsteem.</span><span class="sxs-lookup"><span data-stu-id="7447c-325">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="7447c-326">Süsteemi valitava suvandi määramiseks valige rida **Tegevus** ja seejärel valige suvand vahekaardi **Lõpptegevus**.</span><span class="sxs-lookup"><span data-stu-id="7447c-326">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="7447c-327">Ajalimiidi seadmine</span><span class="sxs-lookup"><span data-stu-id="7447c-327">Set a time limit</span></span>

<span data-ttu-id="7447c-328">Kui otsus tuleb teha teatud ajaks, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="7447c-328">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="7447c-329">Selle protseduuri käigus valitud suvandid alistavad lehe jaotistes **Määramine** ja **Eskaleerimine** valitud suvandid.</span><span class="sxs-lookup"><span data-stu-id="7447c-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="7447c-330">Klõpsake vasakpoolsel paanil suvandit **Täpsemad sätted**.</span><span class="sxs-lookup"><span data-stu-id="7447c-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="7447c-331">Märkige ruut **Määra töövoo elemendi jaoks ajalimiit**.</span><span class="sxs-lookup"><span data-stu-id="7447c-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="7447c-332">Määrake väljal **Kestus**, mis ajaks peab otsus olema tehtud.</span><span class="sxs-lookup"><span data-stu-id="7447c-332">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="7447c-333">Tehke üks järgmistest valikutest:</span><span class="sxs-lookup"><span data-stu-id="7447c-333">Select one of the following options:</span></span>

    - <span data-ttu-id="7447c-334">**Tunnid** – sisestage tundide arv.</span><span class="sxs-lookup"><span data-stu-id="7447c-334">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="7447c-335">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="7447c-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="7447c-336">**Päevad** – sisestage päevade arv.</span><span class="sxs-lookup"><span data-stu-id="7447c-336">**Days** – Enter the number of days.</span></span> <span data-ttu-id="7447c-337">Seejärel valige kalender, mida teie organisatsioon kasutab, ja sisestage organisatsiooni töönädala kohta teave.</span><span class="sxs-lookup"><span data-stu-id="7447c-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="7447c-338">**Nädalad** – sisestage nädalate arv.</span><span class="sxs-lookup"><span data-stu-id="7447c-338">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="7447c-339">**Kuud** – valige päev ja nädal, mis ajaks kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="7447c-339">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="7447c-340">Näiteks soovite võib-olla, et otsus oleks tehtud kuu kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="7447c-340">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="7447c-341">**Aastad** – valige päev, nädal ja kuu, mis ajaks kasutaja peab otsuse tegema.</span><span class="sxs-lookup"><span data-stu-id="7447c-341">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="7447c-342">Näiteks soovite võib-olla, et otsus oleks tehtud detsembri kolmanda nädala reedeks.</span><span class="sxs-lookup"><span data-stu-id="7447c-342">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="7447c-343">Ajalimiidi ületamisel langetab otsuse süsteem.</span><span class="sxs-lookup"><span data-stu-id="7447c-343">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="7447c-344">Loendist **Tegevus** valige suvand, mille süsteem peaks valima.</span><span class="sxs-lookup"><span data-stu-id="7447c-344">In the **Action** list, select the option that the system should select.</span></span>
