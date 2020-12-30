---
title: Töövoo atribuutide konfigureerimine
description: See teema selgitab, kuidas konfigureerida töövoo mitmesuguseid atribuute.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bd3c9bea010099f83d16dad70261bc2d46a1dac
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693278"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="a4d0b-103">Töövoo atribuutide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="a4d0b-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4d0b-104">See teema selgitab, kuidas konfigureerida töövoo mitmesuguseid atribuute.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="a4d0b-105">Avage töövoo töövoo atribuutide töövoo konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="a4d0b-106">Klõpsake töövoo redaktori lõuendit ja seejärel suvandit **Atribuudid**, et avada leht **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="a4d0b-107">Seejärel saate järgmiste protseduuride abil konfigureerida töövoo mitmesuguseid atribuute.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="a4d0b-108">Töövoole nime andmine</span><span class="sxs-lookup"><span data-stu-id="a4d0b-108">Name the workflow</span></span>

<span data-ttu-id="a4d0b-109">Tehke töövoole nime sisestamiseks järgmist.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="a4d0b-110">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="a4d0b-111">Väljal **Nimi** sisestage töövoole kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="a4d0b-112">Näiteks kui loote ostutaotluse töövoo iga riigi/regiooni jaoks, kus tegutsete, võite määrata ostutaotluse töövoo nimeks **Hispaania ostutaotlused** või **Hispaania ostutaotlused**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="a4d0b-113">Töövoo omaniku määramine</span><span class="sxs-lookup"><span data-stu-id="a4d0b-113">Specify the workflow owner</span></span>

<span data-ttu-id="a4d0b-114">Töövoo omanik on isik, kes haldab töövoogu.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="a4d0b-115">Töövoo omaniku määramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="a4d0b-116">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="a4d0b-117">Loendist **Omanik** valige isik, kes töövoogu haldab.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="a4d0b-118">Valige meilimall</span><span class="sxs-lookup"><span data-stu-id="a4d0b-118">Select an email template</span></span>

<span data-ttu-id="a4d0b-119">Tehke järgmist, et valida meilimall, mida kasutatakse töövoo kohta teatiste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="a4d0b-120">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="a4d0b-121">Valige mall loendist **Töövoo teatiste meilimallid**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="a4d0b-122">Kasutajale juhiste sisestamine</span><span class="sxs-lookup"><span data-stu-id="a4d0b-122">Enter instructions for users</span></span>

<span data-ttu-id="a4d0b-123">Võite sisestada juhised kasutajatele, kes saadavad dokumendid töötlemiseks ja kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="a4d0b-124">Kasutajaid nimetatakse ka *algatajateks*.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="a4d0b-125">Näiteks loote ostutaotluse töövoo ja sisestate juhised.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="a4d0b-126">Juhiseid saavad vaadata kasutajad, kes sisestavad ostutaotlusi lehele **Ostutaotlused**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="a4d0b-127">Juhiste vaatamiseks klõpsab algataja töövoo teateribal ikooni.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="a4d0b-128">Kasutajatele juhiste sisestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="a4d0b-129">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="a4d0b-130">Sisestage juhised väljale **Saatmisjuhised**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="a4d0b-131">Juhiste isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="a4d0b-132">Kohatäitjad asendatakse juhiste kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="a4d0b-133">Kohatäitja sisestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="a4d0b-134">Kohatäitja asukoha määramiseks klõpsake välja **Saatmisjuhised**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="a4d0b-135">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="a4d0b-136">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="a4d0b-137">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-137">Click **Insert**.</span></span>

4. <span data-ttu-id="a4d0b-138">Juhiste tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="a4d0b-139">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="a4d0b-140">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="a4d0b-141">Ilmuvas loendis valige keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="a4d0b-142">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="a4d0b-143">Teksti isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="a4d0b-144">Vaadake kohatäitjate sisestamise juhiseid 3. toimingust.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="a4d0b-145">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used-through-activation-conditions"></a><span data-ttu-id="a4d0b-146">Määrake, millal seda töövoogu kasutatakse aktiveerimistingimuste kaudu</span><span class="sxs-lookup"><span data-stu-id="a4d0b-146">Specify when this workflow is used through activation conditions</span></span>

<span data-ttu-id="a4d0b-147">Sama töövoo tüübi järgi saate luua mitmeid töövooge.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-147">You can create multiple workflows that are based on the same workflow type.</span></span> <span data-ttu-id="a4d0b-148">Kui teil on mitu samal tüübil põhinevat töövoogu, peate määrama, millal iga töövoogu aktiveerimistingimuste abil kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-148">When you have multiple workflows that are based on the same type, you must specify when each workflow is used using activation conditions.</span></span> <span data-ttu-id="a4d0b-149">Kui aktiveerimistingimused ei ole täidetud, kasutatakse vaikimisi töövoogu.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-149">If activation conditions are not met, then the default workflow is used.</span></span> <span data-ttu-id="a4d0b-150">Kui töövoo tüübi jaoks on määratletud ainult üks töövoo konfiguratsioon, kasutatakse töövoo konfiguratsiooni sõltumata aktiveerimistingimustest.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-150">Similarly, if there is only one workflow configuration defined for a workflow type, then that workflow configuration will be used regardless of the activation conditions.</span></span>

<span data-ttu-id="a4d0b-151">Näiteks võite luua ostutellimuse töövoo iga riigi või regiooni jaoks, kus tegutsete, nagu Taani ostutellimused või Hispaania ostutellimused, järgmistel tingimustel.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-151">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain, with the following conditions:</span></span>

- <span data-ttu-id="a4d0b-152">Taani ostutaotlusi kasutatakse siis, kui riik/regioon on DK</span><span class="sxs-lookup"><span data-stu-id="a4d0b-152">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="a4d0b-153">Hispaania ostutaotlusi peab kasutama siis, kui riik/regioon on ES</span><span class="sxs-lookup"><span data-stu-id="a4d0b-153">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="a4d0b-154">Määrake nende toimingute abil, millal konfigureeritavat töövoogu kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-154">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="a4d0b-155">Vasakul paanil klõpsake suvandit **Aktiveerimine**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-155">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="a4d0b-156">Märkige ruut **Määra töövoo käitamise tingimused**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-156">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="a4d0b-157">Klõpsake **Lisa tingimus**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-157">Click **Add condition**.</span></span>
4. <span data-ttu-id="a4d0b-158">Sisestage tingimus.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-158">Enter a condition.</span></span>
5. <span data-ttu-id="a4d0b-159">Sisestage täiendavad vajalikud tingimused.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-159">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="a4d0b-160">Vaadake läbi mõningate sihtkirjetega töövoog, et kinnitada, kas tingimus kaasab ja välistab kirjeid õigesti.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-160">Run through the workflow with some target records to verify that the condition correctly includes and excludes records.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="a4d0b-161">Määrake, millal teatisi saadetakse</span><span class="sxs-lookup"><span data-stu-id="a4d0b-161">Specify when notifications are sent</span></span>

<span data-ttu-id="a4d0b-162">Kui dokument esitatakse töötlemiseks, luuakse töövooeksemplar.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-162">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="a4d0b-163">Saate saata kasutajatele teatisi, kui töövool põhinevad töövooeksemplarid käivitatakse, viiakse lõpule, katkestatakse või peatatakse tõrke tõttu.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-163">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="a4d0b-164">Tehke järgmist, et määrata, millal teatisi saadetakse.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-164">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="a4d0b-165">Vasakul paanil klõpsake suvandit **Teatised**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-165">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="a4d0b-166">Märkige ruut iga sündmuse juures, mille puhul saadetakse teatis.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-166">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="a4d0b-167">**Käivitatud** – teatis saadetakse töövooeksemplari käivitamisel.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-167">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="a4d0b-168">**Peatatud** – teatis saadetakse juhul, kui töövooeksemplar on tõrke tõttu peatatud.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-168">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="a4d0b-169">**Lõpule viidud** – teatis saadetakse töövooeksemplari lõpuleviimisel.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-169">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="a4d0b-170">**Taastamatu** – teatis saadetakse juhul, kui töövooeksemplar on taastamatu tõrke tõttu peatatud.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-170">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="a4d0b-171">**Katkestatud** – teatis saadetakse töövooeksemplari katkestamisel.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-171">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="a4d0b-172">Valige 2. etapis valitud sündmuse rida.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-172">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="a4d0b-173">Sisestage teatise tekst vahekaardil **Teatise tekst**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-173">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="a4d0b-174">Teksti isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-174">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="a4d0b-175">Kohatäitjad asendatakse teksti kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-175">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="a4d0b-176">Kohatäitja sisestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-176">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="a4d0b-177">Kohatäitja asukoha määramiseks klõpsake välja.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-177">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="a4d0b-178">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-178">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="a4d0b-179">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-179">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="a4d0b-180">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-180">Click **Insert**.</span></span>
    5. <span data-ttu-id="a4d0b-181">Tavapärane **Teatise teksti** kaasatav kohatäide on „Viimased märkmed: %Workflow.Last note%”, mis kuvab kõiki eelmise etapi kommentaare.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-181">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="a4d0b-182">Teksti tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-182">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="a4d0b-183">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-183">Click **Translations**.</span></span>
    2. <span data-ttu-id="a4d0b-184">Ilmuval lehel klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-184">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="a4d0b-185">Ilmuvas loendis valige keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-185">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="a4d0b-186">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-186">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="a4d0b-187">Teksti isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-187">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="a4d0b-188">Vaadake kohatäitjate sisestamise juhiseid 5. toimingust.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-188">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="a4d0b-189">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-189">Click **Close**.</span></span>

7. <span data-ttu-id="a4d0b-190">Vahekaardil **Adressaat** määrake järgmiste valikute abil, kellele teatisi saadetakse.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-190">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="a4d0b-191">Suvand</span><span class="sxs-lookup"><span data-stu-id="a4d0b-191">Option</span></span></th>
    <th><span data-ttu-id="a4d0b-192">Teatised saadetakse neile kasutajatele</span><span class="sxs-lookup"><span data-stu-id="a4d0b-192">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="a4d0b-193">Teatiste saatmiseks tehke järgmist</span><span class="sxs-lookup"><span data-stu-id="a4d0b-193">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="a4d0b-194">Osaleja</span><span class="sxs-lookup"><span data-stu-id="a4d0b-194">Participant</span></span></td>
    <td><span data-ttu-id="a4d0b-195">Kasutajad, kes on määratud teatud grupile või rollile</span><span class="sxs-lookup"><span data-stu-id="a4d0b-195">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a4d0b-196">Klõpsake vahekaardil <strong>Adressaat</strong> suvandit <strong>Osaleja</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-196">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="a4d0b-197">Valige vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong> grupi või rolli tüüp, millele teatisi saata.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-197">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="a4d0b-198">Loendis <strong>Osaleja</strong> valige grupp või roll, millele teatisi saata.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-198">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a4d0b-199">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="a4d0b-199">Workflow user</span></span></td>
    <td><span data-ttu-id="a4d0b-200">Töövoos osalevad kasutajad</span><span class="sxs-lookup"><span data-stu-id="a4d0b-200">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a4d0b-201">Klõpsake vahekaardil <strong>Adressaat</strong> suvandit <strong>Töövoo kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-201">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="a4d0b-202">Valige töövoos osaleja vahekaardi <strong>Töövoo kasutaja</strong> loendist <strong>Töövoo kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-202">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="a4d0b-203">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="a4d0b-203">User</span></span></td>
    <td><span data-ttu-id="a4d0b-204">Kindlad kasutajad</span><span class="sxs-lookup"><span data-stu-id="a4d0b-204">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="a4d0b-205">Klõpsake vahekaardil <strong>Adressaat</strong> suvandit <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-205">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="a4d0b-206">Vahekaardi <strong>Kasutaja</strong> loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-206">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="a4d0b-207">Valige kasutajad, kellele teatisi saata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-207">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="a4d0b-208">Korrake 3.–7. toimingut iga sündmuse puhul, mille 2. etapis valisite.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-208">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="a4d0b-209">Sisestage märkusi töövoogu tehtud muudatuste kohta.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-209">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="a4d0b-210">Töövoos tehtud muudatuste kohta kommentaaride sisestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-210">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="a4d0b-211">Vasakul paanil klõpsake nuppu **Märkused**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-211">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="a4d0b-212">Sisestage kommentaarid väljale **Sisestage kommentaarid töövoo kohta**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-212">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="a4d0b-213">Vaadake kommentaarid üle.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-213">Review your comments.</span></span> <span data-ttu-id="a4d0b-214">Pärast kommentaaride lisamist ei saa neid muuta.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-214">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="a4d0b-215">Klõpsake käsku **Lisa**, et lisada kommentaar jaotisesse **Kommentaaride ajalugu**.</span><span class="sxs-lookup"><span data-stu-id="a4d0b-215">Click **Add** to add your comments to the **Comment history** area.</span></span>
