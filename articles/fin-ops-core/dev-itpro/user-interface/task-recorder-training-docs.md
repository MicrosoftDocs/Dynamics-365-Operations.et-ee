---
title: Dokumentide või koolituse loomine tegevuse salvestaja abil
description: See teema selgitab, mis asjad on tegevuse salvestaja ja tegevuse juhised, kuidas luua tegevuse salvestisi ja kuidas kohandada Microsoft tegevuse juhiseid ja kaasata neid oma spikrisse.
author: josaw1
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4bb523c2817a220623d8a1b6cc1ac04d7b96283
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812645"
---
# <a name="create-documentation-or-training-with-task-recorder"></a><span data-ttu-id="25c71-103">Dokumentide või koolituse loomine tegevuse salvestaja abil</span><span class="sxs-lookup"><span data-stu-id="25c71-103">Create documentation or training with Task Recorder</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25c71-104">See teema selgitab, mis asjad on tegevuse salvestaja ja tegevuse juhised, kuidas luua tegevuse salvestisi ja kuidas kohandada Microsoft tegevuse juhiseid ja kaasata neid oma spikrisse.</span><span class="sxs-lookup"><span data-stu-id="25c71-104">This topic explains what Task recorder and task guides are, how to create task recordings, and how to customize Microsoft task guides and include them in your Help.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25c71-105">Saate salvestada oma rakenduse Dynamics 365 Talent tegevusjuhised, kuid ei saa neid praegu äriprotsesside modelleerija (BPM) teeki salvestada ega neid paanilt Spikker avada.</span><span class="sxs-lookup"><span data-stu-id="25c71-105">You can record your own task guides for Dynamics 365 Talent but you won't be able to save them to a Business Process Modeler (BPM) library or open them from the Help pane at this time.</span></span> <span data-ttu-id="25c71-106">Saate need lokaalselt või võrgukohta salvestada ning seejärel neid tegevuse salvestajaga avada ja esitada.</span><span class="sxs-lookup"><span data-stu-id="25c71-106">You can save them locally or to a network location, and then open and replay them using Task recorder.</span></span> 

<a name="learn-about-task-recorder"></a><span data-ttu-id="25c71-107">Teave tegevuse salvestaja kohta</span><span class="sxs-lookup"><span data-stu-id="25c71-107">Learn about Task recorder</span></span>
-------------------------

<span data-ttu-id="25c71-108">Tegevuse salvestaja on tööriist, mille abil saab salvestada toote kasutajaliideses tehtavaid toiminguid.</span><span class="sxs-lookup"><span data-stu-id="25c71-108">Task recorder is a tool that you can use to record actions that you take in the product user interface (UI).</span></span> <span data-ttu-id="25c71-109">Tegevuse salvestaja kasutamisel jäädvustatakse kõik sündmused, mida kasutajaliideses teete ja mis serveri suhtes käivitatakse, sh väärtuste lisamine, sätete muutmine ja andmete eemaldamine.</span><span class="sxs-lookup"><span data-stu-id="25c71-109">When you use Task recorder, all of the events that you perform in the UI that are executed against the server—including adding values, changing settings, removing data—are captured.</span></span> <span data-ttu-id="25c71-110">Salvestatud toiminguid nimetatakse ühiselt *tegevuse salvestiseks*.</span><span class="sxs-lookup"><span data-stu-id="25c71-110">The steps that you record are collectively called a *task recording*.</span></span> <span data-ttu-id="25c71-111">Tegevuse salvestisi saab kasutada mitmesugusel moel.</span><span class="sxs-lookup"><span data-stu-id="25c71-111">Task recordings can be used in many ways:</span></span>

-   <span data-ttu-id="25c71-112">**Tegevuse salvestisi saab esitada tegevuse juhistena.**</span><span class="sxs-lookup"><span data-stu-id="25c71-112">**Task recordings can be played as task guides.**</span></span> <span data-ttu-id="25c71-113">Tegevusjuhised on spikri kasutuskogemuse lahutamatu osa.</span><span class="sxs-lookup"><span data-stu-id="25c71-113">Task guides are an integral piece of the Help experience.</span></span><span data-ttu-id="25c71-114"> Tegevuse juhis on kontrollitud, juhendatud, interaktiivne kogemus, mis juhib teid äriprotsessi etappides.</span><span class="sxs-lookup"><span data-stu-id="25c71-114"> A task guide is a controlled, guided, interactive experience through the steps of a business process.</span></span> <span data-ttu-id="25c71-115">Kasutajal palutakse läbida iga etapp hüpikviiba (ehk mulli) abil, mis liigub läbi kasutajaliidese ja osutab kasutajaliidese elemendile, millega kasutaja peaks suhtlema.</span><span class="sxs-lookup"><span data-stu-id="25c71-115">The user is instructed to complete each step by way of a pop-up prompt (or "bubble"), which will animate across the UI and point to the UI element that the user should interact with.</span></span> <span data-ttu-id="25c71-116">„Mull” annab ka teavet selle kohta, kuidas suhelda elemendiga, nagu „Klõpsake siin” või „Sisestage sellele väljale väärtus”.</span><span class="sxs-lookup"><span data-stu-id="25c71-116">The "bubble" also provides information about how to interact with the element, such as “Click here” or “In this field, enter a value.”</span></span><span data-ttu-id="25c71-117"> Tegevuse juhis käitatakse kasutaja praeguse andmekogumi suhtes ja sisestatud andmed salvestatakse kasutaja keskkonda.</span><span class="sxs-lookup"><span data-stu-id="25c71-117"> A task guide runs against the user’s current data set and the data that is entered is saved in the user’s environment.</span></span>
-   <span data-ttu-id="25c71-118">**Tegevuse salvestisi saab kuvada spikri paanil protseduuri juhistena.**</span><span class="sxs-lookup"><span data-stu-id="25c71-118">**Task recordings can be displayed as procedural steps in the Help pane.**</span></span> <span data-ttu-id="25c71-119">Saate kasutada spikri paani tegevuse salvestiste otsimiseks ja kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="25c71-119">You can use the Help pane to search for and display task recordings.</span></span> <span data-ttu-id="25c71-120">Saate juurdepääsu spikripaanile, klõpsates ülemisel navigatsiooniribal ikooni **?**</span><span class="sxs-lookup"><span data-stu-id="25c71-120">You can access the Help pane by clicking the **?**</span></span> <span data-ttu-id="25c71-121">või saate kasutada kiirklahvikombinatsiooni  **Ctrl+Shift+?**.</span><span class="sxs-lookup"><span data-stu-id="25c71-121">icon in the top navigation bar or you can use the shortcut key combination, **Ctrl+Shift+?**.</span></span> <span data-ttu-id="25c71-122">Saate lugeda spikripaanilt tegevuse salvestise juhiseid või otsustada esitada salvestise tegevuse juhisena, nii et see juhib teid läbi kasutajaliidese.</span><span class="sxs-lookup"><span data-stu-id="25c71-122">You can read the steps of a task recording in the Help pane, or you can opt to play the recording as a task guide so it guides you through the UI.</span></span>
-   <span data-ttu-id="25c71-123">**Tegevuse salvestised saab BPM-i salvestada.**</span><span class="sxs-lookup"><span data-stu-id="25c71-123">**Task recordings can be saved to BPM.**</span></span> <span data-ttu-id="25c71-124">Saate oma tegevuse salvestise salvestada hierarhia reale BPM-i teegis teenuses Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="25c71-124">You can save your task recording to a line of a hierarchy in a BPM library in Lifecycle Services (LCS).</span></span> <span data-ttu-id="25c71-125">Salvestisest luuakse toimingute loend ja äriprotsessi voodiagramm.</span><span class="sxs-lookup"><span data-stu-id="25c71-125">A list of steps and a business process flow chart will be generated from the recording.</span></span> <span data-ttu-id="25c71-126">BPM-i teeki salvestatud tegevuse salvestised võib kuvada spikrina.</span><span class="sxs-lookup"><span data-stu-id="25c71-126">Task recordings that have been saved to a BPM library can be shown as Help.</span></span>
-   <span data-ttu-id="25c71-127">**Tegevuse salvestised saab salvestada Wordi dokumentidena.**</span><span class="sxs-lookup"><span data-stu-id="25c71-127">**Task recordings can be saved as Word documents.**</span></span> <span data-ttu-id="25c71-128">See võimaldab hõlpsasti prinditavaid koolitusjuhendeid koostada.</span><span class="sxs-lookup"><span data-stu-id="25c71-128">This allows you to easily produce printable training guides.</span></span>

<span data-ttu-id="25c71-129">Saate luua oma tegevuse salvestisi, esitada Microsofti pakutavaid tegevuse salvestisi või muuta Microsofti pakutavaid tegevuse salvestisi teie konfiguratsiooni kajastamiseks.</span><span class="sxs-lookup"><span data-stu-id="25c71-129">You can create your own task recordings, play task recordings provided by Microsoft, or modify Microsoft-provided task recordings to reflect your configuration.</span></span><span data-ttu-id="25c71-130"> Lisateavet tegevuse salvestaja kohta vt teemast [Tegevuse salvestaja](task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="25c71-130"> For more information about Task recorder, see [Task recorder](task-recorder.md).</span></span>

## <a name="plan-your-task-recording"></a><span data-ttu-id="25c71-131">Tegevuse salvestaja plaanimine</span><span class="sxs-lookup"><span data-stu-id="25c71-131">Plan your task recording</span></span>
<span data-ttu-id="25c71-132">Kui loote uut tegevuse salvestust või tuginete oma salvestise puhul Microsofti tegevuse salvestisele, pidage meeles järgmist.</span><span class="sxs-lookup"><span data-stu-id="25c71-132">Whether you’re creating a new task recording or basing your recording on a Microsoft task recording, keep the following information in mind.</span></span>

-   <span data-ttu-id="25c71-133">Plaanige oma salvestist sarnaselt videole.</span><span class="sxs-lookup"><span data-stu-id="25c71-133">Plan your recording like you would a video.</span></span> <span data-ttu-id="25c71-134">Tehke kõik otsused aegsasti.</span><span class="sxs-lookup"><span data-stu-id="25c71-134">Make all your decisions ahead of time.</span></span>
-   <span data-ttu-id="25c71-135">Läbige äriprotsess vähemalt üks kord ilma seda salvestamata, et toimingutest aru saada.</span><span class="sxs-lookup"><span data-stu-id="25c71-135">Walk through the business process once or twice without recording it to understand the steps.</span></span>
-   <span data-ttu-id="25c71-136">Kui protsessis liigute, siis pange enne salvestamist tähele, kus kasutate kiirklahve või klahvi **Enter**, et saaksite nende kasutamist tegeliku salvestamise ajal vältida.</span><span class="sxs-lookup"><span data-stu-id="25c71-136">When you walk through the process before you record, notice where you use shortcut keys or the **Enter** key, so that you can avoid using them during the actual recording.</span></span>
-   <span data-ttu-id="25c71-137">Tuvastage järgmine.</span><span class="sxs-lookup"><span data-stu-id="25c71-137">Identify the following:</span></span>
    -   <span data-ttu-id="25c71-138">Kas soovite grupeerida toimingud alamtegevusteks?</span><span class="sxs-lookup"><span data-stu-id="25c71-138">Do you want to group steps together into sub-tasks?</span></span> <span data-ttu-id="25c71-139">Alamtegevused eraldavad visuaalselt protsessi osi.</span><span class="sxs-lookup"><span data-stu-id="25c71-139">Sub-tasks visually set apart sections of a process.</span></span> <span data-ttu-id="25c71-140">Näiteks kui loote salvestist toimingust Toote loomine ja väljastamine, võib olla vaja grupeerida toimingud, mida on vaja toote loomiseks, ja seejärel grupeerida toimingud, mida on vaja toote väljastamiseks.</span><span class="sxs-lookup"><span data-stu-id="25c71-140">For example, if you are creating a recording for "Creating and releasing a product," you may want to group together the steps that are required to create a product, and then group together the steps that are required to release the product.</span></span> <span data-ttu-id="25c71-141">Alamtoimingud muudavad ka pikkade protsesside lugemise hõlpsamaks.</span><span class="sxs-lookup"><span data-stu-id="25c71-141">Sub-tasks also make longer processes easier to read.</span></span>
    -   <span data-ttu-id="25c71-142">Kas soovite lisada marginaale ja kui soovite, siis kuhu?</span><span class="sxs-lookup"><span data-stu-id="25c71-142">Do you want to add annotations, and if so, where?</span></span> <span data-ttu-id="25c71-143">Vt lisateavet allolevast jaotisest Erinevad marginaalide tüübid.</span><span class="sxs-lookup"><span data-stu-id="25c71-143">See "Understand the different types of annotations" below for more information.</span></span>
    -   <span data-ttu-id="25c71-144">Millised väärtused lisate erinevatele väljadele, kui äriprotsessi toiminguid teete?</span><span class="sxs-lookup"><span data-stu-id="25c71-144">What values will you add in the various fields as you complete the steps of the business process?</span></span> <span data-ttu-id="25c71-145">On hea teada, mida jätkates valida või sisestada, et salvestamise ajal ei peaks tagasi minema ega vigu parandama.</span><span class="sxs-lookup"><span data-stu-id="25c71-145">It is a good idea to know what you'll select or enter as you proceed so that you don't backtrack or fix mistakes as you're recording.</span></span>

<span data-ttu-id="25c71-146">**Kirjutage oma kirjeldus ja marginaalid aegsasti valmis**</span><span class="sxs-lookup"><span data-stu-id="25c71-146">**Write your description and annotations ahead of time**</span></span>

-   <span data-ttu-id="25c71-147">Iga tegevuse salvestise alguses on kirjelduse väli, kuhu saab sisestada salvestise tutvustuse.</span><span class="sxs-lookup"><span data-stu-id="25c71-147">At the beginning of each task recording, there’s a description field that allows you to enter an introduction to the recording.</span></span> <span data-ttu-id="25c71-148">Kirjeldus tasub kirjutada ja salvestada aegsasti eraldi dokumenti, et saaksite selle salvestamise ajal kopeerida ja tegevuse salvestisse kleepida.</span><span class="sxs-lookup"><span data-stu-id="25c71-148">It is a good idea to write and save the description ahead of time in a separate document so you can copy and paste it into the task recording when you are recording.</span></span> <span data-ttu-id="25c71-149">Sel viisil saate teksti viimistlemiseks aega võtta, kui te parajasti salvestamisega ei tegele.</span><span class="sxs-lookup"><span data-stu-id="25c71-149">That way, you can spend time refining the text when you aren't in the process of recording.</span></span> <span data-ttu-id="25c71-150">Teksti lõikamine ja kleepimine muudab salvestusprotsessi kiiremaks ja sujuvamaks.</span><span class="sxs-lookup"><span data-stu-id="25c71-150">Cutting and pasting the text makes the recording process go more quickly and smoothly.</span></span>
-   <span data-ttu-id="25c71-151">Iga tegevuse salvestamise toimingu ajal saate marginaale koostada.</span><span class="sxs-lookup"><span data-stu-id="25c71-151">For each step in a task recording, you can create annotations.</span></span> <span data-ttu-id="25c71-152">Tegevuse juhise taasesitamise ajal kuvatakse marginaalid „mullis” toimingu teksti kohal või all.</span><span class="sxs-lookup"><span data-stu-id="25c71-152">During playback of a task guide, annotations appear in the "bubble" as notes above or below the text for the step.</span></span> <span data-ttu-id="25c71-153">Kui vaadata marginaale spikripaanil tekstina, kuvatakse need toimingu sees tekstina.</span><span class="sxs-lookup"><span data-stu-id="25c71-153">When viewed as text in the Help pane, annotations appear as text inline in the step.</span></span> <span data-ttu-id="25c71-154">Nagu kirjelduste puhul, tasub marginaalid eraldi dokumenti kirjutada ja salvestada.</span><span class="sxs-lookup"><span data-stu-id="25c71-154">As with the description, it is a good idea to write and save your annotations in a separate document.</span></span> <span data-ttu-id="25c71-155">Tegevuse salvestise salvestamise ajal saate marginaale sellest dokumendist lõigata ja kleepida.</span><span class="sxs-lookup"><span data-stu-id="25c71-155">When you’re recording the task recording, cut and paste the annotations in from that document.</span></span>

<span data-ttu-id="25c71-156">**Erinevad marginaalide tüübid** Kõik marginaalid on valikulised.</span><span class="sxs-lookup"><span data-stu-id="25c71-156">**Understand the different types of annotations** All annotations are optional.</span></span> <span data-ttu-id="25c71-157">Lisage need ainult siis, kui nad annavad kasutajale kasulikku teavet.</span><span class="sxs-lookup"><span data-stu-id="25c71-157">Only add them when they’ll provide helpful information to the user.</span></span>

-   <span data-ttu-id="25c71-158">**Pealkiri**: pealkirja marginaal kuvatakse enne toimingu teksti, mille tegevuse salvestaja automaatselt loob.</span><span class="sxs-lookup"><span data-stu-id="25c71-158">**Title**: A title annotation will appear before the step text that task recorder automatically generates.</span></span><span data-ttu-id="25c71-159"> Tegevuse juhises ilmub automaatselt loodud teksti kohal pealkirja marginaal.</span><span class="sxs-lookup"><span data-stu-id="25c71-159"> In the task guide, the title annotation appears above the automatically generated text.</span></span> <span data-ttu-id="25c71-160">Kasutage seda tüüpi marginaali selgitamiseks, miks kasutaja seda toimingut teeb, või täiendava konteksti pakkumiseks.</span><span class="sxs-lookup"><span data-stu-id="25c71-160">Use this type of annotation to explain why the user is doing the step or to give additional context.</span></span>

<span data-ttu-id="25c71-161">See on redigeerimispaan, mida marginaali lisamisel näete, kui oma salvestist teete.</span><span class="sxs-lookup"><span data-stu-id="25c71-161">This is the editing pane that you see when you add an annotation as you create your recording.</span></span> <span data-ttu-id="25c71-162">Sisestage marginaali pealkiri väljale **Pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="25c71-162">Enter a title annotation in the **Title** box.</span></span> 

<span data-ttu-id="25c71-163">[![Pealkirja marginaaliga redigeerimispaan](./media/screen1.png)](./media/screen1.png)</span><span class="sxs-lookup"><span data-stu-id="25c71-163">[![Editing pane with title annotation](./media/screen1.png)](./media/screen1.png)</span></span> 

<span data-ttu-id="25c71-164">Selline näeb välja marginaali pealkiri tegevusjuhises mullina.</span><span class="sxs-lookup"><span data-stu-id="25c71-164">This is what the title annotation looks like in the "bubble" in the task guide.</span></span> 

<span data-ttu-id="25c71-165">[![Pealkirja marginaali ilme tegevuse juhises](./media/screen2.png)](./media/screen2.png)</span><span class="sxs-lookup"><span data-stu-id="25c71-165">[![Title annotation appearance in task guide](./media/screen2.png)](./media/screen2.png)</span></span>

-   <span data-ttu-id="25c71-166">**Märkmed.** Märkmete marginaal kuvatakse pärast toimingu teksti, mille tegevuse salvestaja automaatselt loob.</span><span class="sxs-lookup"><span data-stu-id="25c71-166">**Notes:** A notes annotation will appear after the step text that task recorder automatically generates.</span></span> <span data-ttu-id="25c71-167">Tegevuse juhises on see nähtav ainult juhul, kui kasutaja klõpsab linki **Kuva rohkem** ülesande juhise mullis.</span><span class="sxs-lookup"><span data-stu-id="25c71-167">In the task guide it will only be visible if the user clicks the **Show more** link in the task guide bubble.</span></span> <span data-ttu-id="25c71-168">Kasutage seda tüüpi marginaali millegi kirjeldamiseks, mida kasutajal on toimingu tegemiseks vaja teada.</span><span class="sxs-lookup"><span data-stu-id="25c71-168">Use this type of annotation to describe anything that a user needs to know to complete the step.</span></span>

<span data-ttu-id="25c71-169">See on redigeerimispaan, mida marginaali lisamisel näete, kui oma salvestist teete.</span><span class="sxs-lookup"><span data-stu-id="25c71-169">This is the editing pane that you see when you add an annotation as you create your recording.</span></span> <span data-ttu-id="25c71-170">Sisestage marginaali märkused väljale **Märkused**.</span><span class="sxs-lookup"><span data-stu-id="25c71-170">Enter a notes annotation in the **Notes** box.</span></span> 

<span data-ttu-id="25c71-171">[![Redigeerimispaan marginaaliga väljal Märkused](./media/screen3.png)](./media/screen3.png)</span><span class="sxs-lookup"><span data-stu-id="25c71-171">[![Editing pane with annotation in Notes box](./media/screen3.png)](./media/screen3.png)</span></span> 

<span data-ttu-id="25c71-172">Selline näeb välja märkuste marginaal tegevusjuhises mullina.</span><span class="sxs-lookup"><span data-stu-id="25c71-172">This is what the notes annotation looks like in the "bubble" in the task guide.</span></span>

<span data-ttu-id="25c71-173">[![Märkuste marginaali ilme tegevuse juhises](./media/screen4.png)](./media/screen4.png)</span><span class="sxs-lookup"><span data-stu-id="25c71-173">[![Notes annotation appearance in task guide](./media/screen4.png)](./media/screen4.png)</span></span>

-   <span data-ttu-id="25c71-174">**Teabeetapp**: nende marginaalide loomiseks paremklõpsake juhtelemendil või kõikjal vormis &lt; **Tegevuse salvestaja** &lt; **Lisa teabeetapp**.</span><span class="sxs-lookup"><span data-stu-id="25c71-174">**Info step**: These annotations are created by right clicking on a control or anywhere on a form &lt; **Task recorder** &lt; **Add info step.**</span></span> <span data-ttu-id="25c71-175">Teabeetapid kuvatakse nummerdatud etapina igas punktis, kuhu selle sisestate, isegi kui kasutajaliideses ei salvestatud ühtki tegevust.</span><span class="sxs-lookup"><span data-stu-id="25c71-175">Info steps appear as a numbered step at whatever point you insert it, even though no action was recorded in the UI.</span></span> <span data-ttu-id="25c71-176">Saate lisada vormi-taseme teabeetapi või juhtelemendiga seotud teabeetapi.</span><span class="sxs-lookup"><span data-stu-id="25c71-176">You can add a form-level info step or an info step associated with a control.</span></span> <span data-ttu-id="25c71-177">Kui teabeetapp on vormiga seotud, ilmub vormile tegevuse juhise esitamisel tegevuse juhise „mull” ilma kursorita.</span><span class="sxs-lookup"><span data-stu-id="25c71-177">When an info step is associated with a form, the task guide “bubble” will appear someplace on the form, with no pointer, when the task guide is played.</span></span> <span data-ttu-id="25c71-178">Kui teabeetapp on seotud juhtelemendiga, osutab tegevuse juhise „mull” tegevuse juhise esitamisel juhtelemendina.</span><span class="sxs-lookup"><span data-stu-id="25c71-178">When an info step is associated with a control, the task guide “bubble” will point to the control when the task guide is played.</span></span><span data-ttu-id="25c71-179"> Spikripaanil kuvatakse teabeetapi mis tahes sisestatud tekstiga marginaal nummerdatud etapina.</span><span class="sxs-lookup"><span data-stu-id="25c71-179"> In the Help pane, an info step annotation will appear as a numbered step with whatever text you entered.</span></span> <span data-ttu-id="25c71-180">Kasutage teabeetappe kasutaja ettevalmistamiseks järgmisteks toiminguteks, väljaspool rakendust tehtavate toimingute kirjeldamiseks või teistele salvestistele viitamiseks (kuigi marginaalides ei saa hüperlinke luua).</span><span class="sxs-lookup"><span data-stu-id="25c71-180">Use info steps to prepare the user for the next steps, to describe steps that need to be done outside of the application, or to refer to other recordings (although you cannot create hyperlinks in annotations).</span></span>

<span data-ttu-id="25c71-181">**Määrake, kui pika salvestise teete**</span><span class="sxs-lookup"><span data-stu-id="25c71-181">**Determine how long to make your recording**</span></span>

-   <span data-ttu-id="25c71-182">Kasutaja tavaliselt loeb salvestist või esitab selle algusest lõpuni, seega ärge kombineerige etappe või toiminguid, mida on parem teha eraldi.</span><span class="sxs-lookup"><span data-stu-id="25c71-182">The user will generally either read or play the recording from start to finish, so don’t combine steps or tasks that are better done separately.</span></span>
-   <span data-ttu-id="25c71-183">Püüdke mitte salvestada pikka stsenaariumi, mis hõlmab mitut alamprotsessi.</span><span class="sxs-lookup"><span data-stu-id="25c71-183">Try not to record a long scenario that spans multiple sub-processes.</span></span> <span data-ttu-id="25c71-184">Näiteks toiming Poe klienditeenuse laua kasutamine on liiga lai; jagage see lühemateks toiminguteks nagu Tagastuste aktsepteerimine ja Kinkekaardile lisamine.</span><span class="sxs-lookup"><span data-stu-id="25c71-184">For example, “Operate in-store customer service desk” is too broad; break it up into shorter tasks such as “Accept returns” and “Add to gift card.”</span></span>
-   <span data-ttu-id="25c71-185">Kui tegevust saab teha mitme äriprotsessi raames, looge sellele eraldi salvestis ja saate sellele teistes salvestistes viidata.</span><span class="sxs-lookup"><span data-stu-id="25c71-185">If a task can be carried out as part of several different business processes, create a separate recording for it, and you can refer to it in the other recordings.</span></span>
-   <span data-ttu-id="25c71-186">Kui protsess hõlmab mitut tegevust, mida inimene tõenäoliselt korraga teeb, võite hoida tegevusi ühes salvestises, nt Funktsiooniprofiilide seadistamine ja määramine.</span><span class="sxs-lookup"><span data-stu-id="25c71-186">If the process involves multiple tasks that the person likely does all at once, you can keep the tasks in one recording, for example, “Set up and assign functionality profiles.”</span></span>
-   <span data-ttu-id="25c71-187">Kui see on midagi sellist, mida tehakse üks kord (nt konfigureerimine) ja siis tehakse kohe teine tegevus, mida võidakse teha korduvalt ja eraldi, eraldage need kaheks tegevuse salvestiseks.</span><span class="sxs-lookup"><span data-stu-id="25c71-187">If it is something someone does once (such as configuration) and then another task that they can do immediately afterward but may do repeatedly, and on its own, break them up into two task recordings.</span></span>

<span data-ttu-id="25c71-188">**Otsustage, kust kasutajaliideses salvestamist alustada** Lehekülg, millel tegevuse salvestise salvestamise käivitamisel asute, mõjutab seda, millisel lehekülje jaoks tegevuse juhis kuvatakse.</span><span class="sxs-lookup"><span data-stu-id="25c71-188">**Decide where, in the UI, to start a recording** The page that you are on when you start recording a task recording affects which page the task guide is displayed for.</span></span><span data-ttu-id="25c71-189"> Näiteks kui soovite, et teie tegevuse salvestis oleks loetletud spikripaanil, kui kasutaja klõpsab lehel Pearaamatu parameetrid spikrit, tuleb alustada salvestamist lehelt Pearaamatu parameetrid.</span><span class="sxs-lookup"><span data-stu-id="25c71-189"> For example, if you want your task recording to be listed in the Help pane when a user clicks Help on the General ledger parameters page, you must start your recording on the General ledger parameters page.</span></span> <span data-ttu-id="25c71-190">**Salvestiste salvestamine axtr-failidena** Kui olete tegevuse salvestise loomise või redigeerimise lõpetanud, kuvatakse teile mitu valikut salvestise allalaadimiseks või salvestamiseks.</span><span class="sxs-lookup"><span data-stu-id="25c71-190">**Save recordings as .axtr files** When you are done creating or editing a task recording, you are presented with several options for how you want to download, or save the recording.</span></span> <span data-ttu-id="25c71-191">Saate laadida failid alla tegevuse salvestise paketina (.axtr), laadida need alla töötlemata salvestise failina (.xml), Wordi dokumendina või salvestada faili LCS-i teeki.</span><span class="sxs-lookup"><span data-stu-id="25c71-191">You can download the file as a task recording package (.axtr), download it as a raw recording file (.xml), download it as a Word document, or save the file to an LCS library.</span></span> <span data-ttu-id="25c71-192">On soovitatav salvestada tegevuse salvestis alati tegevuse salvestise paketifailina (.axtr).</span><span class="sxs-lookup"><span data-stu-id="25c71-192">It is a good idea to always save your task recording as a task recording package file (.axtr).</span></span> <span data-ttu-id="25c71-193">See aitab faili hõlpsamini hallata, kui hiljem peaks olema vaja protseduure või marginaale muuta.</span><span class="sxs-lookup"><span data-stu-id="25c71-193">This will help make maintenance of the file easier if procedures or annotations need to change later.</span></span> <span data-ttu-id="25c71-194">Kui soovite laadida faili alla Wordi dokumendina, salvestage see samuti tegevuse salvestise paketifailina.</span><span class="sxs-lookup"><span data-stu-id="25c71-194">If you want to download the file as a Word document, also save it as a task recording package file.</span></span>

## <a name="create-your-task-recording"></a><span data-ttu-id="25c71-195">Tegevuse salvestise loomine</span><span class="sxs-lookup"><span data-stu-id="25c71-195">Create your task recording</span></span>
<span data-ttu-id="25c71-196">Üksikasjalikud protsessijuhised leiate jaotisest [Tegevuse salvestaja ressursid](task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="25c71-196">For detailed walk-through steps, see [Task recorder resources](task-recorder.md).</span></span>

## <a name="copy-and-customize-microsofts-task-recordings"></a><span data-ttu-id="25c71-197">Microsofti tegevuse salvestiste kopeerimine ja kohandamine</span><span class="sxs-lookup"><span data-stu-id="25c71-197">Copy and customize Microsoft's task recordings</span></span>
<span data-ttu-id="25c71-198">Saate Microsofti tegevuse salvestised alla laadida ja neid redigeerida, et kasutada neid oma spikridokumentides või koolitusmaterjalides.</span><span class="sxs-lookup"><span data-stu-id="25c71-198">You can download and edit Microsoft's task recordings to use them for your own Help documentation or training materials.</span></span> <span data-ttu-id="25c71-199">Microsofti tegevuse salvestise allalaadimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="25c71-199">To download a Microsoft task recording, follow these steps:</span></span>

1.  <span data-ttu-id="25c71-200">Avage tegevuse salvestaja.</span><span class="sxs-lookup"><span data-stu-id="25c71-200">Open Task recorder.</span></span> <span data-ttu-id="25c71-201">Tegevuse salvestaja asub menüüs **Sätted**.</span><span class="sxs-lookup"><span data-stu-id="25c71-201">Task recorder is located in the **Settings** menu.</span></span>
2.  <span data-ttu-id="25c71-202">Klõpsake tegevuse salvestaja paanil valikut **Salvestise haldamine.**</span><span class="sxs-lookup"><span data-stu-id="25c71-202">In the Task recorder pane, click **Maintain a recording.**</span></span>
3.  <span data-ttu-id="25c71-203">Jaotises **Kus salvestis asub** klõpsake valikut **See on LCS-i teegis**.</span><span class="sxs-lookup"><span data-stu-id="25c71-203">Under **Where is the recording**, click **It is in an LCS library**.</span></span>
4.  <span data-ttu-id="25c71-204">Klõpsake valikut **LCS-i teegi valimine**.</span><span class="sxs-lookup"><span data-stu-id="25c71-204">Click **Select the LCS library**.</span></span>
5.  <span data-ttu-id="25c71-205">Valige Microsofti globaalne teek.</span><span class="sxs-lookup"><span data-stu-id="25c71-205">Select the Microsoft global library.</span></span>
6.  <span data-ttu-id="25c71-206">Valige puult äriprotsessi teegi sõlm, millega tegevuse salvestis on seotud.</span><span class="sxs-lookup"><span data-stu-id="25c71-206">In the tree, select the business process library node that the task recording is associated with.</span></span>
7.  <span data-ttu-id="25c71-207">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="25c71-207">Click **OK**.</span></span>
8.  <span data-ttu-id="25c71-208">Klõpsake käsku **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="25c71-208">Click **Start**.</span></span>
9.  <span data-ttu-id="25c71-209">Selles punktis liikuge läbi salvestise, muutes jooksvalt toiminguid ja salvestades need uuesti. **Märkus**. Kui teil on vaja ainult salvestise teksti muuta, võite avada salvestise režiimis **Salvestise marginaalide redigeerimine** ja seejärel selle salvestada.</span><span class="sxs-lookup"><span data-stu-id="25c71-209">At this point, step through the recording, changing any steps as you go to re-record it. **Note**: If you only need to change the text of a recording, you can open the recording in **Edit a recording's annotations** mode, and then save it.</span></span>
10. <span data-ttu-id="25c71-210">Kui salvestis on lõpuni mänginud, klõpsake ekraani ülaosas tegevuse salvestaja ribal nuppu **Peata**.</span><span class="sxs-lookup"><span data-stu-id="25c71-210">After the recording has played to the end, click **Stop** in the task recorder bar at the top of the screen.</span></span>
11. <span data-ttu-id="25c71-211">Valige, kuidas tegevuse salvestist salvestada soovite.</span><span class="sxs-lookup"><span data-stu-id="25c71-211">Choose how you want to save the task recording.</span></span>

## <a name="include-your-task-recordings-in-the-help-pane"></a><span data-ttu-id="25c71-212">Tegevuse salvestiste lisamine spikripaanis</span><span class="sxs-lookup"><span data-stu-id="25c71-212">Include your task recordings in the Help pane</span></span>
<span data-ttu-id="25c71-213">Oma kohandatud tegevuse salvestiste kuvamiseks spikripaanil, et neid saaks tegevuse juhistena taasesitada või tekstina kuvada, tuleb salvestada tegevuse salvestised oma BPM-i teeki ja seejärel uuendada oma spikrisüsteemi parameetreid nii, et need osutaksid teie BPM-i teegile.</span><span class="sxs-lookup"><span data-stu-id="25c71-213">To show your own custom task recordings in the Help pane so that they can be played back as task guides or viewed as text, you must save your task recordings to your own BPM library, and then update your Help system parameters to point to your BPM library.</span></span> <span data-ttu-id="25c71-214">Lisateabe saamiseks vaadake teemat [Spikrisüsteemi ühendamine](../../fin-ops/get-started/help-connect.md).</span><span class="sxs-lookup"><span data-stu-id="25c71-214">For more information, see [Connect the Help system](../../fin-ops/get-started/help-connect.md).</span></span>

<a name="additional-resources"></a><span data-ttu-id="25c71-215">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="25c71-215">Additional resources</span></span>
--------

[<span data-ttu-id="25c71-216">Spikrisüsteem</span><span class="sxs-lookup"><span data-stu-id="25c71-216">Help system</span></span>](../../fin-ops/get-started/help-overview.md)

[<span data-ttu-id="25c71-217">Spikrisüsteemi ühendamine</span><span class="sxs-lookup"><span data-stu-id="25c71-217">Connect the Help system</span></span>](../../fin-ops/get-started/help-connect.md)

[<span data-ttu-id="25c71-218">Tegevuse salvestaja</span><span class="sxs-lookup"><span data-stu-id="25c71-218">Task Recorder</span></span>](task-recorder.md)

[<span data-ttu-id="25c71-219">Tegevuse salvestajaga Richi spikriteemade loomine (väline link)</span><span class="sxs-lookup"><span data-stu-id="25c71-219">Create Rich Help Topics with Task Recorder (external link)</span></span>](https://mbspartner.microsoft.com/AX/Videos/970)