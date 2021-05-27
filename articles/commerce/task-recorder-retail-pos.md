---
title: Tegevuse salvestaja ning spikker Retail Modern POS-i (MPOS) ja pilvekassa jaoks
description: Selles teemas kirjeldatakse tegevuse salvestaja kasutamist Retail Modern POS-is (MPOS) ja pilvekassas.
author: mugunthanm
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 02e8bb1bfb088a877ef23b7a81982868700f4ae2
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6028103"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="c0599-103">Tegevuse salvestaja ning spikker Retail Modern POS-i (MPOS) ja pilvekassa jaoks</span><span class="sxs-lookup"><span data-stu-id="c0599-103">Task recorder and Help for Retail Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c0599-104">Selles teemas kirjeldatakse tegevuse salvestaja kasutamist Retail Modern POS-is (MPOS) ja pilvekassas.</span><span class="sxs-lookup"><span data-stu-id="c0599-104">This topic describes how to use Task recorder in Retail Modern POS and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="c0599-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="c0599-105">Overview</span></span>

<span data-ttu-id="c0599-106">Tegevuse salvestaja Retail Modern POSis või pilvekassas on uus lahendus, mille eesmärk on pöörata tähelepanu suurele tundlikkusele.</span><span class="sxs-lookup"><span data-stu-id="c0599-106">Task recorder in Retail Modern POS or Cloud POS is a new solution that was built with a focus on high responsiveness.</span></span> <span data-ttu-id="c0599-107">Sellel on paindlik rakenduse programmeerimisliides (API) laiendatavuse ja sujuva integratsiooni tagamiseks äriprotsessi salvestiste tarbijatega.</span><span class="sxs-lookup"><span data-stu-id="c0599-107">It provides a flexible application programming interface (API) for extensibility and seamless integration with consumers of business process recordings.</span></span> <span data-ttu-id="c0599-108">Peale selle on tõstetud esile tegevuse salvestaja integratsioon äriprotsesside modelleerija (BPM) tööriistaga teenuses Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)).</span><span class="sxs-lookup"><span data-stu-id="c0599-108">Additionally, Task recorder integration with the Business process modeler (BPM) tool on Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) has been brought forward.</span></span> <span data-ttu-id="c0599-109">Seetõttu saavad kasutajad luua oma rakenduste analüüsimiseks ja kujundamiseks salvestistest jätkuvalt rikkalikke äriprotsessi diagramme.</span><span class="sxs-lookup"><span data-stu-id="c0599-109">Therefore, users can continue to produce rich business process diagrams from recordings to analyze and design their applications.</span></span>

## <a name="architecture"></a><span data-ttu-id="c0599-110">Arhitektuur</span><span class="sxs-lookup"><span data-stu-id="c0599-110">Architecture</span></span>

<span data-ttu-id="c0599-111">Tegevuse salvestaja suudab salvestada täpselt ja tõetruult kasutaja toiminguid kliendis.</span><span class="sxs-lookup"><span data-stu-id="c0599-111">Task recorder can record user actions in the client with exact fidelity.</span></span> <span data-ttu-id="c0599-112">Iga juhtelement on seadistatud teavitama tegevuse salvestajat kasutaja toimingu täitmisest.</span><span class="sxs-lookup"><span data-stu-id="c0599-112">Each control is instrumented to notify Task recorder about the execution of a user action.</span></span> <span data-ttu-id="c0599-113">Juhtelement teavitab tegevuse salvestajat, et toimus sündmus, ja edastab kogu asjassepuutuva teabe vastava kasutaja toimingu kohta reaalajas.</span><span class="sxs-lookup"><span data-stu-id="c0599-113">The control notifies Task recorder that an event occurred and passes along all pertinent information about the corresponding user action in real time.</span></span> <span data-ttu-id="c0599-114">Selle teabe põhjal suudab tegevuse salvestaja jäädvustada kasutaja toimingu tüübi (nt nupuvajutus, väärtuse sisestus või navigeerimine) ja mis tahes andmed, mis on kasutaja toiminguga seotud (nt sisestatud andmete väärtus ja tüüp, vormi kontekst või kirje kontekst).</span><span class="sxs-lookup"><span data-stu-id="c0599-114">From this information, Task recorder can capture the type of user action (such as a button click, value entry, or navigation) and any data that is related to the user action (such as the input data value and type, form context, or record context).</span></span> <span data-ttu-id="c0599-115">Tegevuse salvestaja lisab teabele piisavalt üksikasju, garanteerimaks, et salvestise taasesitamisel suudetakse teha salvestatud toiminguid täpselt samamoodi, nagu kasutaja neid tegi.</span><span class="sxs-lookup"><span data-stu-id="c0599-115">Task recorder persists the information with enough detail to help guarantee that a playback of the recording can perform the recorded actions exactly as the user performed them.</span></span> <span data-ttu-id="c0599-116">(Taasesituse funktsioon ei ole veel Retail modern POS-is ega pilvekassas juurutatud.)</span><span class="sxs-lookup"><span data-stu-id="c0599-116">(The playback feature isn't yet implemented at Retail modern POS or Cloud POS.)</span></span>

## <a name="basic-configuration"></a><span data-ttu-id="c0599-117">Põhikonfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="c0599-117">Basic configuration</span></span>

<span data-ttu-id="c0599-118">Tegevuse salvestamise lubamiseks kassas tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c0599-118">To enable task recording in POS, follow these steps.</span></span>

1. <span data-ttu-id="c0599-119">Klõpsake valikuid **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Registrid**.</span><span class="sxs-lookup"><span data-stu-id="c0599-119">Click **Retail and Commerce** &gt; **Channel Setup** &gt; **POS Setup** &gt; **Registers**.</span></span>
2. <span data-ttu-id="c0599-120">Klõpsake registrit, millel tegevuse salvestis aktiveerida.</span><span class="sxs-lookup"><span data-stu-id="c0599-120">Click the register to enable task recording on.</span></span>
3. <span data-ttu-id="c0599-121">Määrake vahekaardil **Registreeri** kiirkaardil **Üldine** valiku **Tegevuse salvestamise lubamine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="c0599-121">On the **Register** tab, on the **General** FastTab, set the **Enable task recording** option to **Yes**.</span></span>
4. <span data-ttu-id="c0599-122">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c0599-122">Click **Save**.</span></span>
5. <span data-ttu-id="c0599-123">Avage **Jaemüük ja kaubandus** &gt; **Jaemüügi ja kaubanduse IT** &gt; **Jaotusgraafik**.</span><span class="sxs-lookup"><span data-stu-id="c0599-123">Go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedule**.</span></span>
6. <span data-ttu-id="c0599-124">Valige töö **Registrid (1090)** ja klõpsake siis käsku **Käivita kohe**.</span><span class="sxs-lookup"><span data-stu-id="c0599-124">Select the **Registers (1090)** job, and then click **Run now**.</span></span>

## <a name="create-a-recording"></a><span data-ttu-id="c0599-125">Salvestise loomine</span><span class="sxs-lookup"><span data-stu-id="c0599-125">Create a recording</span></span>

<span data-ttu-id="c0599-126">Tehke järgmist uue salvestise loomiseks tegevuse salvestaja abil.</span><span class="sxs-lookup"><span data-stu-id="c0599-126">Follow these steps to create a new recording using Task recorder.</span></span>

1. <span data-ttu-id="c0599-127">Käivitage Retail Modern POS või pilvekassa ja logige sisse.</span><span class="sxs-lookup"><span data-stu-id="c0599-127">Start Retail Modern POS or Cloud POS, and sign in.</span></span>
2. <span data-ttu-id="c0599-128">Klõpsake lehel **Sätted** jaotises **Tegevuse salvestaja** valikut **Ava tegevuse salvestaja**.</span><span class="sxs-lookup"><span data-stu-id="c0599-128">On the **Settings** page, in the **Task Recorder** section, click **Open task recorder**.</span></span> <span data-ttu-id="c0599-129">Kuvatakse paan **Tegevuse salvestaja**.</span><span class="sxs-lookup"><span data-stu-id="c0599-129">The **Task recorder** pane appears.</span></span> <span data-ttu-id="c0599-130">Võite klõpsata nuppu **Sule** (**X**) ülemises paremas nurgas paani **Tegevuse salvestaja** sulgemiseks enne uue salvestuse alustamist.</span><span class="sxs-lookup"><span data-stu-id="c0599-130">You can click the **Close** button (**X**) in the upper-right corner to close the **Task recorder** pane before you begin a new recording.</span></span> <span data-ttu-id="c0599-131">Paani taasavamiseks korrake toimingut 2.</span><span class="sxs-lookup"><span data-stu-id="c0599-131">To reopen the pane, repeat step 2.</span></span>

    <span data-ttu-id="c0599-132">[![Tegevuse salvestaja paan](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span><span class="sxs-lookup"><span data-stu-id="c0599-132">[![Task recorder pane](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span></span>

3. <span data-ttu-id="c0599-133">Sisestage salvestise nimi ja kirjeldus, ning seejärel klõpsake nuppu **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="c0599-133">Enter a name and description for the recording, and then click **Start**.</span></span> <span data-ttu-id="c0599-134">Salvestusseanss algab kohe, kui klõpsate nuppu **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="c0599-134">The recording session begins as soon as you click **Start**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c0599-135">Kui klõpsate nuppu **Sule** (**X**) ülemises paremas nurgas sel ajal, kui salvestamine käib, siis paan **Tegevuse salvestaja** suletakse, kuid salvestusseanssi ei lõpetata.</span><span class="sxs-lookup"><span data-stu-id="c0599-135">If you click the **Close** button (**X**) in the upper-right corner while recording is in progress, the **Task recorder** pane is closed, but the recording session isn't ended.</span></span> <span data-ttu-id="c0599-136">Tegevuse salvestaja paani taasavamiseks klõpsake nuppu **Spikker** (küsimärk) ekraani ülaosas.</span><span class="sxs-lookup"><span data-stu-id="c0599-136">To reopen the Task recorder pane, click the **Help** button (question mark) at the top of the screen.</span></span>
    >
    > <span data-ttu-id="c0599-137">[![Küsimärk](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="c0599-137">[![Question mark](./media/help.jpg)](./media/help.jpg)</span></span>

4. <span data-ttu-id="c0599-138">Pärast nupu **Käivita** klõpsamist läheb tegevuse salvestaja salvestusrežiimi.</span><span class="sxs-lookup"><span data-stu-id="c0599-138">After you click **Start**, Task recorder enters recording mode.</span></span> <span data-ttu-id="c0599-139">Paanil **Tegevuse salvestaja** on näha salvestusprotsessiga seotud andmed ja nupud.</span><span class="sxs-lookup"><span data-stu-id="c0599-139">The **Task recorder** pane shows information and controls that are related to the recording process.</span></span>
5. <span data-ttu-id="c0599-140">Tehke uuesti toimingud, mida soovite Retail Modern POS-i või pilvekassa kasutajaliideses teha.</span><span class="sxs-lookup"><span data-stu-id="c0599-140">Perform the actions that you want to perform in the Retail Modern POS or Cloud POS user interface (UI).</span></span>
6. <span data-ttu-id="c0599-141">Salvestusseansi lõpetamiseks klõpsake nuppu **Peata**.</span><span class="sxs-lookup"><span data-stu-id="c0599-141">To end the recording session, click **Stop**.</span></span>

## <a name="download-options"></a><span data-ttu-id="c0599-142">Allalaadimisvalikud</span><span class="sxs-lookup"><span data-stu-id="c0599-142">Download options</span></span>

<span data-ttu-id="c0599-143">Pärast salvestusseansi lõpetamist kuvatakse mitu valikut, et saaksite oma salvestise alla laadida.</span><span class="sxs-lookup"><span data-stu-id="c0599-143">After you end the recording session, several options are shown, so that you can download your recording.</span></span>

<span data-ttu-id="c0599-144">[![Allalaadimisvalikud](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span><span class="sxs-lookup"><span data-stu-id="c0599-144">[![Download options](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span></span>

### <a name="save-to-this-pc"></a><span data-ttu-id="c0599-145">Salvesta sellesse arvutisse</span><span class="sxs-lookup"><span data-stu-id="c0599-145">Save to this PC</span></span>

<span data-ttu-id="c0599-146">Salvestuspaketti saab kasutada tegevuse juhise esitamiseks, salvestise säilitamiseks või salvestise märkuste redigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="c0599-146">You can use the recording package to play a Task guide, maintain the recording, or edit the annotations in the recording.</span></span> <span data-ttu-id="c0599-147">(See funktsioon ei ole veel Retail Modern POS-is ega pilvekassas juurutatud.)</span><span class="sxs-lookup"><span data-stu-id="c0599-147">(This feature isn't yet implemented in Retail Modern POS and Cloud POS.)</span></span>

### <a name="export-as-word-document"></a><span data-ttu-id="c0599-148">Ekspordi Wordi dokumendina</span><span class="sxs-lookup"><span data-stu-id="c0599-148">Export as Word document</span></span>

<span data-ttu-id="c0599-149">Saate salvestada salvestise Microsoft Wordi dokumendina.</span><span class="sxs-lookup"><span data-stu-id="c0599-149">You can save the recording as a Microsoft Word document.</span></span> <span data-ttu-id="c0599-150">Dokument sisaldab salvestatud toiminguid ja hõivatud kuvatõmmiseid.</span><span class="sxs-lookup"><span data-stu-id="c0599-150">The document will contain the recorded steps and the screenshots that were captured.</span></span>

### <a name="save-as-developer-recording"></a><span data-ttu-id="c0599-151">Salvesta arendaja salvestisena</span><span class="sxs-lookup"><span data-stu-id="c0599-151">Save as developer recording</span></span>

<span data-ttu-id="c0599-152">Töötlemata salvestusfail on kasulik arendaja stsenaariumide, nt testkoodi loomise jaoks.</span><span class="sxs-lookup"><span data-stu-id="c0599-152">The raw recording file will be useful for developer scenarios such as test code generation.</span></span> <span data-ttu-id="c0599-153">(See funktsioon ei ole veel juurutatud)</span><span class="sxs-lookup"><span data-stu-id="c0599-153">(This feature isn't yet implemented.)</span></span>

## <a name="recording-controls"></a><span data-ttu-id="c0599-154">Salvestamise juhtelemendid</span><span class="sxs-lookup"><span data-stu-id="c0599-154">Recording controls</span></span>

<span data-ttu-id="c0599-155">[![Salvestamise juhtelemendid](./media/controls.jpg)](./media/controls.jpg)</span><span class="sxs-lookup"><span data-stu-id="c0599-155">[![Recording controls](./media/controls.jpg)](./media/controls.jpg)</span></span>

### <a name="stop"></a><span data-ttu-id="c0599-156">Peata</span><span class="sxs-lookup"><span data-stu-id="c0599-156">Stop</span></span>

<span data-ttu-id="c0599-157">Salvestusseansi lõpetamiseks klõpsake nuppu **Peata**.</span><span class="sxs-lookup"><span data-stu-id="c0599-157">Click **Stop** to end the recording session.</span></span> <span data-ttu-id="c0599-158">Arvestage, et pärast seansi lõpetamist ei saa seda uuesti käivitada.</span><span class="sxs-lookup"><span data-stu-id="c0599-158">Note that you can't restart a session after you end it.</span></span> <span data-ttu-id="c0599-159">Seega veenduge enne lõpetamist, et salvestamine oleks lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="c0599-159">Therefore, make sure that the recording is completed before you end it.</span></span>

### <a name="pause"></a><span data-ttu-id="c0599-160">Paus</span><span class="sxs-lookup"><span data-stu-id="c0599-160">Pause</span></span>

<span data-ttu-id="c0599-161">Salvestusseansi ajutiseks peatamiseks (pausi tegemiseks) ja toiminguga jätkamiseks klõpsake nuppu **Paus**.</span><span class="sxs-lookup"><span data-stu-id="c0599-161">Click **Pause** to temporarily stop (pause) the recording session and continue with the operation.</span></span> <span data-ttu-id="c0599-162">Toiminguid, mida teete pärast nupu **Paus** klõpsamist, ei salvestata.</span><span class="sxs-lookup"><span data-stu-id="c0599-162">Steps that you perform after you click **Pause** aren't recorded.</span></span>

### <a name="continue"></a><span data-ttu-id="c0599-163">Jätka</span><span class="sxs-lookup"><span data-stu-id="c0599-163">Continue</span></span>

<span data-ttu-id="c0599-164">Salvestamisseansi jätkamiseks pärast pausi klõpsake **Jätka**.</span><span class="sxs-lookup"><span data-stu-id="c0599-164">To resume the recording session after you've paused it, click **Continue**.</span></span>

### <a name="capture-screenshots"></a><span data-ttu-id="c0599-165">Tee kuvatõmmised</span><span class="sxs-lookup"><span data-stu-id="c0599-165">Capture screenshots</span></span>

<span data-ttu-id="c0599-166">Tegevuse salvestaja suudab jäädvustada Retail Modern POS-i kasutajaliidese kuvatõmmiseid äriprotsessi salvestamise ajal.</span><span class="sxs-lookup"><span data-stu-id="c0599-166">Task recorder can capture screenshots of the Retail Modern POS UI as you record a business process.</span></span> <span data-ttu-id="c0599-167">Kuvatõmmise jäädvustamise funktsiooni sisselülitamiseks määrake suvandi **Jäädvusta kuvatõmmis** väärtuseks **Jah** ja seejärel alustage jäädvustamist.</span><span class="sxs-lookup"><span data-stu-id="c0599-167">To turn on the screenshot capture feature, set the **Capture screenshot** option to **Yes** and then make the recording.</span></span> <span data-ttu-id="c0599-168">Kui lõpetate salvestamise, klõpsake **Peata** ja laadige alla Wordi dokument.</span><span class="sxs-lookup"><span data-stu-id="c0599-168">Once the recording is completed, click **Stop** and download the Word document.</span></span> <span data-ttu-id="c0599-169">Dokumendis on sammud asjakohaste kuvatõmmistega.</span><span class="sxs-lookup"><span data-stu-id="c0599-169">The document will contain the steps with relevant screenshots.</span></span>

> [!NOTE]
> <span data-ttu-id="c0599-170">Pilvekassas ei toetata kuvatõmmise jäädvustamise funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="c0599-170">Capture screenshot functionality is not supported in Cloud POS.</span></span>

### <a name="start-task-and-end-task"></a><span data-ttu-id="c0599-171">Tegevuse alustamine ja lõpetamine</span><span class="sxs-lookup"><span data-stu-id="c0599-171">Start task and End task</span></span>

<span data-ttu-id="c0599-172">Saate määrata rühmitatud toimingute kogumi alguse ja lõpu nuppudega **Alusta tegevust** ja **Lõpeta** **tegevus**.</span><span class="sxs-lookup"><span data-stu-id="c0599-172">You can specify the beginning and end of a set of grouped steps by using the **Start task** and **End** **task** buttons.</span></span> <span data-ttu-id="c0599-173">Klõpsake nuppu **Alusta tegevust** toimingu „Alusta tegevust” lisamiseks ja tehke siis toimingud, mis tuleks rühma lisada.</span><span class="sxs-lookup"><span data-stu-id="c0599-173">Click **Start task** to add a "Start Task" step, and then perform the steps that should be included in the group.</span></span> <span data-ttu-id="c0599-174">Kui olete rühma toimingute tegemise lõpetanud, klõpsake valikut **Lõpeta toiming**.</span><span class="sxs-lookup"><span data-stu-id="c0599-174">After you've finished performing the steps for the group, click **End task**.</span></span> <span data-ttu-id="c0599-175">Toimingute abil saate oma protseduure korraldada.</span><span class="sxs-lookup"><span data-stu-id="c0599-175">Tasks help you organize your procedures.</span></span> <span data-ttu-id="c0599-176">Toiminguid saab pesastada teistesse toimingutesse.</span><span class="sxs-lookup"><span data-stu-id="c0599-176">Tasks can be nested within other tasks.</span></span> <span data-ttu-id="c0599-177">Sel viisil saate korraldada paremini väga pikki ja keerukaid äriprotsesse.</span><span class="sxs-lookup"><span data-stu-id="c0599-177">In this way, you can better organize very long and complex business processes.</span></span>

## <a name="adding-annotations"></a><span data-ttu-id="c0599-178">Märkuste lisamine</span><span class="sxs-lookup"><span data-stu-id="c0599-178">Adding annotations</span></span>

<span data-ttu-id="c0599-179">Märkus on lisatekst, mille saab toimingule salvestises lisada.</span><span class="sxs-lookup"><span data-stu-id="c0599-179">An annotation is additional text that you add to a step in a recording.</span></span> <span data-ttu-id="c0599-180">Näiteks saab märkusi kasutada kasutajale täiendava konteksti või juhiste andmiseks.</span><span class="sxs-lookup"><span data-stu-id="c0599-180">For example, you can use annotations to give the user more context or instructions.</span></span> <span data-ttu-id="c0599-181">Märkusi saab lisada enne või pärast toimingut.</span><span class="sxs-lookup"><span data-stu-id="c0599-181">You can add annotations before or after a step.</span></span> <span data-ttu-id="c0599-182">Märkuse saab lisada mis tahes toimingule, klõpsates toimingust paremal asuvat nuppu **Redigeeri** (pliiatsi sümbol).</span><span class="sxs-lookup"><span data-stu-id="c0599-182">You can add an annotation to any step by clicking the **Edit** button (pencil symbol) to the right of the step.</span></span>

<span data-ttu-id="c0599-183">[![Toimingu redigeerimise nupp](./media/annotate.jpg)](./media/annotate.jpg)</span><span class="sxs-lookup"><span data-stu-id="c0599-183">[![Edit button for a step](./media/annotate.jpg)](./media/annotate.jpg)</span></span>

### <a name="texts-and-notes"></a><span data-ttu-id="c0599-184">Tekstid ja märkused</span><span class="sxs-lookup"><span data-stu-id="c0599-184">Texts and notes</span></span>

<span data-ttu-id="c0599-185">Väljade **Tekstid** ja **Märkused** abil saab lisada teksti, mis peaks olema tegevuse juhises toiminguga seotud.</span><span class="sxs-lookup"><span data-stu-id="c0599-185">You can use the **Texts** and **Notes** fields to add text that should be associated with a step in a Task guide.</span></span>

<span data-ttu-id="c0599-186">[![Teksti ja märkuste väljad](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span><span class="sxs-lookup"><span data-stu-id="c0599-186">[![Text and Notes fields](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span></span>

#### <a name="text"></a><span data-ttu-id="c0599-187">Tekst</span><span class="sxs-lookup"><span data-stu-id="c0599-187">Text</span></span>

<span data-ttu-id="c0599-188">Väljale **Tekst** sisestatav tekst kuvatakse tegevuse juhises toimingu teksti *kohal*.</span><span class="sxs-lookup"><span data-stu-id="c0599-188">Text that you enter in the **Text** field appears *above* the step text in the Task guide.</span></span> <span data-ttu-id="c0599-189">See asukoht sobib teksti jaoks, mida kasutaja peaks enne toimingu tegemist lugema.</span><span class="sxs-lookup"><span data-stu-id="c0599-189">This location is appropriate for text that you want the user to read before the user completes the step.</span></span>

#### <a name="notes"></a><span data-ttu-id="c0599-190">Märkmed</span><span class="sxs-lookup"><span data-stu-id="c0599-190">Notes</span></span>

<span data-ttu-id="c0599-191">Väljale **Märkused** sisestatav tekst kuvatakse tegevuse juhises toimingu teksti *all*.</span><span class="sxs-lookup"><span data-stu-id="c0599-191">Text that you enter in the **Notes** field appears *below* the step text in the Task guide.</span></span> <span data-ttu-id="c0599-192">Märkuse teksti lugemiseks peab kasutaja toimingu teksti hüpikaknas laiendama.</span><span class="sxs-lookup"><span data-stu-id="c0599-192">To read the note text, the user must expand the step text in the pop-up window.</span></span> <span data-ttu-id="c0599-193">See asukoht sobib soovi korral loetava materjali jaoks või muu teabe jaoks, millest kasutajale võib abi olla, kuid mis pole toimingu tegemise jaoks kasutajale tingimata vajalik.</span><span class="sxs-lookup"><span data-stu-id="c0599-193">This location is appropriate for optional reading material or other information that might be useful to the user, but that the user doesn't require in order to complete the action.</span></span>

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a><span data-ttu-id="c0599-194">Spikker Retail Modern POS-is ja pilvekassas</span><span class="sxs-lookup"><span data-stu-id="c0599-194">Help in Retail Modern POS and Cloud POS</span></span>

<span data-ttu-id="c0599-195">Oma kohandatud tegevuse salvestiste kuvamiseks Retail Modern POS-i ja pilvekassa spikripaanil, et neid saaks tekstina kuvada, peate salvestama tegevuse salvestised oma BPM-i teeki ja seejärel värskendama oma spikrisüsteemi parameetreid nii, et need osutaksid teie BPM-i teegile.</span><span class="sxs-lookup"><span data-stu-id="c0599-195">To show your own custom task recordings in the Help pane of Retail Modern POS and Cloud POS so that they can be viewed as text, you must save your task recordings to your own BPM library, and then update your Help system parameters to point to your BPM library.</span></span> <span data-ttu-id="c0599-196">Lisateavet leiate jaotisest [Spikrisüsteemi ühendamine](../fin-ops-core/fin-ops/get-started/help-connect.md).</span><span class="sxs-lookup"><span data-stu-id="c0599-196">For more information, see [Connecting the Help system](../fin-ops-core/fin-ops/get-started/help-connect.md).</span></span> <span data-ttu-id="c0599-197">Retail Modern POS-i ja pilvekassa spikker otsib LCS-ist reaalajas.</span><span class="sxs-lookup"><span data-stu-id="c0599-197">Retail Modern POS and Cloud POS Help searches LCS in real time.</span></span> <span data-ttu-id="c0599-198">See otsib kõigist BPM-i teekidest, mis on Commerce’i spikrisüsteemi parameetrites valitud, ja kuvab asjakohased tulemused.</span><span class="sxs-lookup"><span data-stu-id="c0599-198">It searches across all the BPM libraries that are selected in the Commerce Help system parameters and shows the relevant results.</span></span> <span data-ttu-id="c0599-199">**Spikri** menüü avamiseks klõpsake ekraani ülaosas **spikri** nuppu (küsimärk) ning sisestage siis otsinguväljale oma protsess nimi ja vajutage otsingunuppu.</span><span class="sxs-lookup"><span data-stu-id="c0599-199">To access the **Help** menu, click the **Help** button (question mark) at the top of the screen and then in the search box type your process name and hit the search button.</span></span>

<span data-ttu-id="c0599-200">[![Nupp Spikker](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="c0599-200">[![Help button](./media/help.jpg)](./media/help.jpg)</span></span>

<span data-ttu-id="c0599-201">Kui klõpsate otsingutulemustes valikut Tegevuse juhis, saate vaadata toiminguid spikriteemana või eksportida toimingud Wordi dokumenti.</span><span class="sxs-lookup"><span data-stu-id="c0599-201">When you click a Task guide in the search results, you can either view the steps as a Help topic or export the steps to a Word document.</span></span>

> [!NOTE]
> <span data-ttu-id="c0599-202">Retail Modern POS-i ja pilvekassa spikker ei kuva tegevusjuhiseid selle põhjal, millisel vormil olete või millist toimingut teete.</span><span class="sxs-lookup"><span data-stu-id="c0599-202">Help in Retail Modern POS and Cloud POS will not bring up task guides according to what form you're on or operation you're doing.</span></span> <span data-ttu-id="c0599-203">Protsessi nimi tuleb sisestada otsinguväljale ja klõpsata siis nuppu **Otsing**.</span><span class="sxs-lookup"><span data-stu-id="c0599-203">You have to type the process name in the search box and then click **Search**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]