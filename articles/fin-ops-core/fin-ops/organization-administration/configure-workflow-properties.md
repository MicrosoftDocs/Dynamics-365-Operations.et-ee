---
title: Töövoo atribuutide konfigureerimine
description: See teema selgitab, kuidas konfigureerida töövoo mitmesuguseid atribuute.
author: sericks007
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76d44c472989a73d71c2edd19f1187ecd09827ae
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190116"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="e718a-103">Töövoo atribuutide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e718a-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e718a-104">See teema selgitab, kuidas konfigureerida töövoo mitmesuguseid atribuute.</span><span class="sxs-lookup"><span data-stu-id="e718a-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="e718a-105">Avage töövoo töövoo atribuutide töövoo konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="e718a-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="e718a-106">Klõpsake töövoo redaktori lõuendit ja seejärel suvandit **Atribuudid**, et avada leht **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="e718a-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="e718a-107">Seejärel saate järgmiste protseduuride abil konfigureerida töövoo mitmesuguseid atribuute.</span><span class="sxs-lookup"><span data-stu-id="e718a-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="e718a-108">Töövoole nime andmine</span><span class="sxs-lookup"><span data-stu-id="e718a-108">Name the workflow</span></span>

<span data-ttu-id="e718a-109">Tehke töövoole nime sisestamiseks järgmist.</span><span class="sxs-lookup"><span data-stu-id="e718a-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="e718a-110">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="e718a-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="e718a-111">Väljal **Nimi** sisestage töövoole kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="e718a-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="e718a-112">Näiteks kui loote ostutaotluse töövoo iga riigi/regiooni jaoks, kus tegutsete, võite määrata ostutaotluse töövoo nimeks **Hispaania ostutaotlused** või **Hispaania ostutaotlused**.</span><span class="sxs-lookup"><span data-stu-id="e718a-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="e718a-113">Töövoo omaniku määramine</span><span class="sxs-lookup"><span data-stu-id="e718a-113">Specify the workflow owner</span></span>

<span data-ttu-id="e718a-114">Töövoo omanik on isik, kes haldab töövoogu.</span><span class="sxs-lookup"><span data-stu-id="e718a-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="e718a-115">Töövoo omaniku määramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e718a-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="e718a-116">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="e718a-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="e718a-117">Loendist **Omanik** valige isik, kes töövoogu haldab.</span><span class="sxs-lookup"><span data-stu-id="e718a-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="e718a-118">Valige meilimall</span><span class="sxs-lookup"><span data-stu-id="e718a-118">Select an email template</span></span>

<span data-ttu-id="e718a-119">Tehke järgmist, et valida meilimall, mida kasutatakse töövoo kohta teatiste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e718a-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="e718a-120">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="e718a-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="e718a-121">Valige mall loendist **Töövoo teatiste meilimallid**.</span><span class="sxs-lookup"><span data-stu-id="e718a-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="e718a-122">Kasutajale juhiste sisestamine</span><span class="sxs-lookup"><span data-stu-id="e718a-122">Enter instructions for users</span></span>

<span data-ttu-id="e718a-123">Võite sisestada juhised kasutajatele, kes saadavad dokumendid töötlemiseks ja kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="e718a-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="e718a-124">Kasutajaid nimetatakse ka *algatajateks*.</span><span class="sxs-lookup"><span data-stu-id="e718a-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="e718a-125">Näiteks loote ostutaotluse töövoo ja sisestate juhised.</span><span class="sxs-lookup"><span data-stu-id="e718a-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="e718a-126">Juhiseid saavad vaadata kasutajad, kes sisestavad ostutaotlusi lehele **Ostutaotlused**.</span><span class="sxs-lookup"><span data-stu-id="e718a-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="e718a-127">Juhiste vaatamiseks klõpsab algataja töövoo teateribal ikooni.</span><span class="sxs-lookup"><span data-stu-id="e718a-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="e718a-128">Kasutajatele juhiste sisestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e718a-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="e718a-129">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="e718a-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="e718a-130">Sisestage juhised väljale **Saatmisjuhised**.</span><span class="sxs-lookup"><span data-stu-id="e718a-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="e718a-131">Juhiste isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="e718a-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="e718a-132">Kohatäitjad asendatakse juhiste kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="e718a-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="e718a-133">Kohatäitja sisestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e718a-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="e718a-134">Kohatäitja asukoha määramiseks klõpsake välja **Saatmisjuhised**.</span><span class="sxs-lookup"><span data-stu-id="e718a-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="e718a-135">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="e718a-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="e718a-136">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="e718a-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="e718a-137">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="e718a-137">Click **Insert**.</span></span>

4. <span data-ttu-id="e718a-138">Juhiste tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="e718a-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="e718a-139">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="e718a-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="e718a-140">Ilmuval lehel klõpsake valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e718a-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="e718a-141">Ilmuvas loendis valige keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="e718a-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="e718a-142">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="e718a-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="e718a-143">Teksti isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="e718a-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="e718a-144">Vaadake kohatäitjate sisestamise juhiseid 3. toimingust.</span><span class="sxs-lookup"><span data-stu-id="e718a-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="e718a-145">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="e718a-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="e718a-146">Määrake töövoo kasutamise aeg.</span><span class="sxs-lookup"><span data-stu-id="e718a-146">Specify when this workflow is used</span></span>

<span data-ttu-id="e718a-147">Sama tüübi järgi saate luua mitmeid töövooge.</span><span class="sxs-lookup"><span data-stu-id="e718a-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="e718a-148">Näiteks võite luua ostutellimuse töövoo iga riigi või regiooni jaoks, kus tegutsete, nagu Taani ostutellimused või Hispaania ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="e718a-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="e718a-149">Kui teil on mitu samal tüübil põhinevat töövoogu, peate määrama, millal iga töövoogu kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="e718a-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="e718a-150">Eelmise näite puhul määrate järgmised tingimused.</span><span class="sxs-lookup"><span data-stu-id="e718a-150">For the preceding example, you specify the following conditions:</span></span>

- <span data-ttu-id="e718a-151">Taani ostutaotlusi kasutatakse siis, kui riik/regioon on DK</span><span class="sxs-lookup"><span data-stu-id="e718a-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="e718a-152">Hispaania ostutaotlusi peab kasutama siis, kui riik/regioon on ES</span><span class="sxs-lookup"><span data-stu-id="e718a-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="e718a-153">Määrake nende toimingute abil, millal konfigureeritavat töövoogu kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="e718a-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="e718a-154">Vasakul paanil klõpsake suvandit **Aktiveerimine**.</span><span class="sxs-lookup"><span data-stu-id="e718a-154">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="e718a-155">Märkige ruut **Määra töövoo käitamise tingimused**.</span><span class="sxs-lookup"><span data-stu-id="e718a-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="e718a-156">Klõpsake **Lisa tingimus**.</span><span class="sxs-lookup"><span data-stu-id="e718a-156">Click **Add condition**.</span></span>
4. <span data-ttu-id="e718a-157">Sisestage tingimus.</span><span class="sxs-lookup"><span data-stu-id="e718a-157">Enter a condition.</span></span>
5. <span data-ttu-id="e718a-158">Sisestage täiendavad vajalikud tingimused.</span><span class="sxs-lookup"><span data-stu-id="e718a-158">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="e718a-159">Tehke järgmist kontrollimaks, kas teie sisestatud tingimused on õigesti määratud.</span><span class="sxs-lookup"><span data-stu-id="e718a-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>

    1. <span data-ttu-id="e718a-160">Klõpsake nuppu **Test**.</span><span class="sxs-lookup"><span data-stu-id="e718a-160">Click **Test**.</span></span>
    2. <span data-ttu-id="e718a-161">Lehel **Testi töövoo tingimus** alas **Kontrolli tingimust** valige kirje.</span><span class="sxs-lookup"><span data-stu-id="e718a-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="e718a-162">Klõpsake nuppu **Test**.</span><span class="sxs-lookup"><span data-stu-id="e718a-162">Click **Test**.</span></span> <span data-ttu-id="e718a-163">Süsteem hindab kirjet otsustamaks, kas see vastab teie määratud tingimustele.</span><span class="sxs-lookup"><span data-stu-id="e718a-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="e718a-164">Näiteks kui loote Hispaania jaoks ostutaotluse töövoogu, näete lehe jaotises **Kontrolli tingimust** ostutaotluste loendit.</span><span class="sxs-lookup"><span data-stu-id="e718a-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="e718a-165">Kui klõpsate käsul **Katseta**, kontrollib süsteem valitud ostutaotlust, et määrata, kas riik/regioon on ES.</span><span class="sxs-lookup"><span data-stu-id="e718a-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4. <span data-ttu-id="e718a-166">Klõpsake **OK** või valikut **Tühista**, et naasta lehele **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="e718a-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="e718a-167">Määrake, millal teatisi saadetakse</span><span class="sxs-lookup"><span data-stu-id="e718a-167">Specify when notifications are sent</span></span>

<span data-ttu-id="e718a-168">Kui dokument esitatakse töötlemiseks, luuakse töövooeksemplar.</span><span class="sxs-lookup"><span data-stu-id="e718a-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="e718a-169">Saate saata kasutajatele teatisi, kui töövool põhinevad töövooeksemplarid käivitatakse, viiakse lõpule, katkestatakse või peatatakse tõrke tõttu.</span><span class="sxs-lookup"><span data-stu-id="e718a-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="e718a-170">Tehke järgmist, et määrata, millal teatisi saadetakse.</span><span class="sxs-lookup"><span data-stu-id="e718a-170">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="e718a-171">Vasakul paanil klõpsake suvandit **Teatised**.</span><span class="sxs-lookup"><span data-stu-id="e718a-171">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="e718a-172">Märkige ruut iga sündmuse juures, mille puhul saadetakse teatis.</span><span class="sxs-lookup"><span data-stu-id="e718a-172">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="e718a-173">**Käivitatud** – teatis saadetakse töövooeksemplari käivitamisel.</span><span class="sxs-lookup"><span data-stu-id="e718a-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="e718a-174">**Peatatud** – teatis saadetakse juhul, kui töövooeksemplar on tõrke tõttu peatatud.</span><span class="sxs-lookup"><span data-stu-id="e718a-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="e718a-175">**Lõpule viidud** – teatis saadetakse töövooeksemplari lõpuleviimisel.</span><span class="sxs-lookup"><span data-stu-id="e718a-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="e718a-176">**Taastamatu** – teatis saadetakse juhul, kui töövooeksemplar on taastamatu tõrke tõttu peatatud.</span><span class="sxs-lookup"><span data-stu-id="e718a-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="e718a-177">**Katkestatud** – teatis saadetakse töövooeksemplari katkestamisel.</span><span class="sxs-lookup"><span data-stu-id="e718a-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="e718a-178">Valige 2. etapis valitud sündmuse rida.</span><span class="sxs-lookup"><span data-stu-id="e718a-178">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="e718a-179">Sisestage teatise tekst vahekaardil **Teatise tekst**.</span><span class="sxs-lookup"><span data-stu-id="e718a-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="e718a-180">Teksti isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="e718a-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="e718a-181">Kohatäitjad asendatakse teksti kasutajatele kuvamisel sobivate andmetega.</span><span class="sxs-lookup"><span data-stu-id="e718a-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="e718a-182">Kohatäitja sisestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e718a-182">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="e718a-183">Kohatäitja asukoha määramiseks klõpsake välja.</span><span class="sxs-lookup"><span data-stu-id="e718a-183">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="e718a-184">Klõpsake nuppu **Sisesta kohatäide**.</span><span class="sxs-lookup"><span data-stu-id="e718a-184">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="e718a-185">Ilmuvas loendis valige sisestamiseks kohatäitja.</span><span class="sxs-lookup"><span data-stu-id="e718a-185">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="e718a-186">Klõpsake nuppu **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="e718a-186">Click **Insert**.</span></span>
    5. <span data-ttu-id="e718a-187">Tavapärane **Teatise teksti** kaasatav kohatäide on „Last Notes: %Workflow.Last note%”, mis kuvab kõiki eelmise etapi kommentaare.</span><span class="sxs-lookup"><span data-stu-id="e718a-187">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="e718a-188">Teksti tõlgete lisamiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="e718a-188">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="e718a-189">Klõpsake valikut **Tõlked**.</span><span class="sxs-lookup"><span data-stu-id="e718a-189">Click **Translations**.</span></span>
    2. <span data-ttu-id="e718a-190">Ilmuval lehel klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e718a-190">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="e718a-191">Ilmuvas loendis valige keel, milles teksti sisestate.</span><span class="sxs-lookup"><span data-stu-id="e718a-191">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="e718a-192">Väljale **Tõlgitud tekst** sisestage tekst.</span><span class="sxs-lookup"><span data-stu-id="e718a-192">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="e718a-193">Teksti isikupärastamiseks saate sisestada kohatäitjad.</span><span class="sxs-lookup"><span data-stu-id="e718a-193">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="e718a-194">Vaadake kohatäitjate sisestamise juhiseid 5. toimingust.</span><span class="sxs-lookup"><span data-stu-id="e718a-194">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="e718a-195">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="e718a-195">Click **Close**.</span></span>

7. <span data-ttu-id="e718a-196">Vahekaardil **Adressaat** määrake järgmiste valikute abil, kellele teatisi saadetakse.</span><span class="sxs-lookup"><span data-stu-id="e718a-196">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="e718a-197">Suvand</span><span class="sxs-lookup"><span data-stu-id="e718a-197">Option</span></span></th>
    <th><span data-ttu-id="e718a-198">Teatised saadetakse neile kasutajatele</span><span class="sxs-lookup"><span data-stu-id="e718a-198">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="e718a-199">Teatiste saatmiseks tehke järgmist</span><span class="sxs-lookup"><span data-stu-id="e718a-199">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="e718a-200">Osaleja</span><span class="sxs-lookup"><span data-stu-id="e718a-200">Participant</span></span></td>
    <td><span data-ttu-id="e718a-201">Kasutajad, kes on määratud teatud grupile või rollile</span><span class="sxs-lookup"><span data-stu-id="e718a-201">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="e718a-202">Klõpsake vahekaardil <strong>Adressaat</strong> suvandit <strong>Osaleja</strong>.</span><span class="sxs-lookup"><span data-stu-id="e718a-202">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="e718a-203">Valige vahekaardil <strong>Rollipõhine</strong> loendis <strong>Osaleja tüüp</strong> grupi või rolli tüüp, millele teatisi saata.</span><span class="sxs-lookup"><span data-stu-id="e718a-203">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="e718a-204">Loendis <strong>Osaleja</strong> valige grupp või roll, millele teatisi saata.</span><span class="sxs-lookup"><span data-stu-id="e718a-204">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="e718a-205">Töövoo kasutaja</span><span class="sxs-lookup"><span data-stu-id="e718a-205">Workflow user</span></span></td>
    <td><span data-ttu-id="e718a-206">Töövoos osalevad kasutajad</span><span class="sxs-lookup"><span data-stu-id="e718a-206">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="e718a-207">Klõpsake vahekaardil <strong>Adressaat</strong> suvandit <strong>Töövoo kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="e718a-207">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="e718a-208">Valige töövoos osaleja vahekaardi <strong>Töövoo kasutaja</strong> loendist <strong>Töövoo kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="e718a-208">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="e718a-209">Kasutaja</span><span class="sxs-lookup"><span data-stu-id="e718a-209">User</span></span></td>
    <td><span data-ttu-id="e718a-210">Kindlad kasutajad</span><span class="sxs-lookup"><span data-stu-id="e718a-210">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="e718a-211">Klõpsake vahekaardil <strong>Adressaat</strong> suvandit <strong>Kasutaja</strong>.</span><span class="sxs-lookup"><span data-stu-id="e718a-211">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="e718a-212">Vahekaardi <strong>Kasutaja</strong> loend <strong>Saadaolevad kasutajad</strong> hõlmab kõiki kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="e718a-212">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="e718a-213">Valige kasutajad, kellele teatisi saata, ja teisaldage need kasutajad seejärel loendisse <strong>Valitud kasutajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="e718a-213">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="e718a-214">Korrake 3.–7. toimingut iga sündmuse puhul, mille 2. etapis valisite.</span><span class="sxs-lookup"><span data-stu-id="e718a-214">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="e718a-215">Sisestage märkusi töövoogu tehtud muudatuste kohta.</span><span class="sxs-lookup"><span data-stu-id="e718a-215">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="e718a-216">Töövoos tehtud muudatuste kohta kommentaaride sisestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e718a-216">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="e718a-217">Vasakul paanil klõpsake nuppu **Märkused**.</span><span class="sxs-lookup"><span data-stu-id="e718a-217">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="e718a-218">Sisestage kommentaarid väljale **Sisestage kommentaarid töövoo kohta**.</span><span class="sxs-lookup"><span data-stu-id="e718a-218">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="e718a-219">Vaadake kommentaarid üle.</span><span class="sxs-lookup"><span data-stu-id="e718a-219">Review your comments.</span></span> <span data-ttu-id="e718a-220">Pärast kommentaaride lisamist ei saa neid muuta.</span><span class="sxs-lookup"><span data-stu-id="e718a-220">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="e718a-221">Klõpsake käsku **Lisa**, et lisada kommentaar jaotisesse **Kommentaaride ajalugu**.</span><span class="sxs-lookup"><span data-stu-id="e718a-221">Click **Add** to add your comments to the **Comment history** area.</span></span>