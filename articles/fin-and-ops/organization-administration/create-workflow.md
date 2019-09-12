---
title: Töövoogude ülevaate loomine
description: See teema selgitab, kuidas töövoogu luua.
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: 1dc2b2cd6b9372fb60d0e112b5dbb0b60898caca
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865036"
---
# <a name="create-workflows-overview"></a><span data-ttu-id="fcd41-103">Töövoogude ülevaate loomine</span><span class="sxs-lookup"><span data-stu-id="fcd41-103">Create workflows overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fcd41-104">See teema selgitab, kuidas töövoogu luua.</span><span class="sxs-lookup"><span data-stu-id="fcd41-104">This topic explains how to create a workflow.</span></span>

## <a name="open-the-workflow-editor"></a><span data-ttu-id="fcd41-105">Avage töövoo redaktor</span><span class="sxs-lookup"><span data-stu-id="fcd41-105">Open the workflow editor</span></span>

<span data-ttu-id="fcd41-106">Microsoft Dynamics 365 for Finance and Operationsi moodul, millega töötate, määrab töövootüübid, mida saate luua.</span><span class="sxs-lookup"><span data-stu-id="fcd41-106">The Microsoft Dynamics 365 for Finance and Operations module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="fcd41-107">Läbige need etapid töövoo tüübi valimiseks, et luua ja avada töövoo redaktor.</span><span class="sxs-lookup"><span data-stu-id="fcd41-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1. <span data-ttu-id="fcd41-108">Avage moodul, mille jaoks soovite luua uue töövoo.</span><span class="sxs-lookup"><span data-stu-id="fcd41-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="fcd41-109">Näiteks ostutaotluste jaoks töövoo loomiseks klõpsake valikut **Hanked**.</span><span class="sxs-lookup"><span data-stu-id="fcd41-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2. <span data-ttu-id="fcd41-110">Klõpsake valikuid **Seadistus** &gt; **Mooduli \[mooduli nimi\] töövood**.</span><span class="sxs-lookup"><span data-stu-id="fcd41-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3. <span data-ttu-id="fcd41-111">Ilmuva loendilehe tegumiribal klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="fcd41-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4. <span data-ttu-id="fcd41-112">Lehel **Töövoo loomine** valige loomiseks töövoo tüüp ja klõpsake seejärel valikut **Töövoo loomine**.</span><span class="sxs-lookup"><span data-stu-id="fcd41-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="fcd41-113">Ilmub töövooredaktor.</span><span class="sxs-lookup"><span data-stu-id="fcd41-113">The workflow editor appears.</span></span> <span data-ttu-id="fcd41-114">Nüüd saate kasutada töövoo kujundamiseks järgmiseid protseduure.</span><span class="sxs-lookup"><span data-stu-id="fcd41-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="fcd41-115">Lohistage töövoo elemendid lõuend</span><span class="sxs-lookup"><span data-stu-id="fcd41-115">Drag workflow elements onto the canvas</span></span>

<span data-ttu-id="fcd41-116">Töövooredaktori ala **Töövoo elemendid** sisaldab elemente, mida saate oma töövoole lisada.</span><span class="sxs-lookup"><span data-stu-id="fcd41-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="fcd41-117">Töövoole elementide lisamiseks lohistage need lõuendile.</span><span class="sxs-lookup"><span data-stu-id="fcd41-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="fcd41-118">Ühendage elemendid</span><span class="sxs-lookup"><span data-stu-id="fcd41-118">Connect the elements</span></span>

<span data-ttu-id="fcd41-119">Ühe töövoo elemendi teisega ühendamiseks hoidke kursorit elemendi kohal, kuni ühenduspunktid kuvatakse.</span><span class="sxs-lookup"><span data-stu-id="fcd41-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="fcd41-120">Klõpsake ühenduspunkti ja lohistage see teisele elemendile.</span><span class="sxs-lookup"><span data-stu-id="fcd41-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="fcd41-121">Ühendage kindlasti kõik elemendid.</span><span class="sxs-lookup"><span data-stu-id="fcd41-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="fcd41-122">Konfigureerige töövoo atribuudid</span><span class="sxs-lookup"><span data-stu-id="fcd41-122">Configure the properties of the workflow</span></span>

<span data-ttu-id="fcd41-123">Järgige neid juhiseid töövoo atribuutide konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="fcd41-123">Follow these steps to configure the properties of the workflow.</span></span>

1. <span data-ttu-id="fcd41-124">Klõpsake lõuend veendumaks, et töövoo element pole valitud.</span><span class="sxs-lookup"><span data-stu-id="fcd41-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2. <span data-ttu-id="fcd41-125">Klõpsake valikut **Atribuudid**, et avada töövoo leht **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="fcd41-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3. <span data-ttu-id="fcd41-126">Järgige teemas [Töövoo atribuutide konfigureerimine](configure-workflow-properties.md) kirjeldatud protseduure.</span><span class="sxs-lookup"><span data-stu-id="fcd41-126">Follow the procedures in the [Configure the properties of a workflow](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="fcd41-127">Töövoo elementide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="fcd41-127">Configure the elements of the workflow</span></span>

<span data-ttu-id="fcd41-128">Konfigureerige iga elemendi läbite lõuendile.</span><span class="sxs-lookup"><span data-stu-id="fcd41-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="fcd41-129">Iga töövooelemendi konfigureerimise kohta lisateabe saamiseks vaadake järgmisi teemasid.</span><span class="sxs-lookup"><span data-stu-id="fcd41-129">For information about how to configure each workflow element, see the following topics:</span></span>

- [<span data-ttu-id="fcd41-130">Käsitsi ülesande konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="fcd41-130">Configure a manual task</span></span>](configure-manual-task-workflow.md)
- [<span data-ttu-id="fcd41-131">Automatiseeritud ülesande konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="fcd41-131">Configure an automated task</span></span>](configure-automated-task-workflow.md)
- [<span data-ttu-id="fcd41-132">Kinnitusprotsessi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="fcd41-132">Configure an approval process</span></span>](configure-approval-process-workflow.md)
- [<span data-ttu-id="fcd41-133">Kinnitussammu konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="fcd41-133">Configure an approval step</span></span>](configure-approval-step-workflow.md)
- [<span data-ttu-id="fcd41-134">Käsitsi otsuse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="fcd41-134">Configure a manual decision</span></span>](configure-manual-decision-workflow.md)
- [<span data-ttu-id="fcd41-135">Tingimusliku otsuse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="fcd41-135">Configure a conditional decision</span></span>](configure-conditional-decision-workflow.md)
- [<span data-ttu-id="fcd41-136">Paralleeltegevuse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="fcd41-136">Configure a parallel activity</span></span>](configure-parallel-activity-workflow.md)
- [<span data-ttu-id="fcd41-137">Paralleelharu konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="fcd41-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
- [<span data-ttu-id="fcd41-138">Reakauba töövoo konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="fcd41-138">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="fcd41-139">Lahenda tõrkeid ja hoiatusi</span><span class="sxs-lookup"><span data-stu-id="fcd41-139">Resolve any errors or warnings</span></span>

<span data-ttu-id="fcd41-140">Töövooredaktori allservas olev paan **Tõrked ja hoiatused** näitab töövoo jaoks loodud teateid.</span><span class="sxs-lookup"><span data-stu-id="fcd41-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="fcd41-141">Selle elemendi leidmiseks, kus tõrge või hoiatus ilmnes, topeltklõpsake tõrget või hoiatusteadet.</span><span class="sxs-lookup"><span data-stu-id="fcd41-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="fcd41-142">Enne töövoo aktiivseks tegemist peate lahendama kõik tõrked ja hoiatused.</span><span class="sxs-lookup"><span data-stu-id="fcd41-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="fcd41-143">Salvestage ja aktiveerige töövoog</span><span class="sxs-lookup"><span data-stu-id="fcd41-143">Save and activate the workflow</span></span>

<span data-ttu-id="fcd41-144">Kui olete valmis töövoo salvestama ja aktiveerima, järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="fcd41-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1. <span data-ttu-id="fcd41-145">Klõpsake valikut **Salvesta ja sule**, et sulgeda töövooredaktor ja avada leht **Salvesta töövoog**.</span><span class="sxs-lookup"><span data-stu-id="fcd41-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2. <span data-ttu-id="fcd41-146">Sisestage kommentaarid töövoole tehtud muudatuste kohta ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="fcd41-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3. <span data-ttu-id="fcd41-147">Kui kõik tõrked ja hoiatused on lahendatud, ilmub leht **Aktiveeri töövoog**.</span><span class="sxs-lookup"><span data-stu-id="fcd41-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="fcd41-148">Tehke üks järgmistest valikutest:</span><span class="sxs-lookup"><span data-stu-id="fcd41-148">Select one of the following options:</span></span>

    - <span data-ttu-id="fcd41-149">Töövoo selle versiooni aktiveerimiseks klõpsake valikut **Aktiveeri uus versioon**.</span><span class="sxs-lookup"><span data-stu-id="fcd41-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="fcd41-150">Kui töövoog on aktiivne, saavad kasutajad esitada töötlemiseks dokumente.</span><span class="sxs-lookup"><span data-stu-id="fcd41-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    - <span data-ttu-id="fcd41-151">Kui te ei soovi seda versiooni aktiveerida, klõpsake valikut **Ära aktiveeri uut versiooni**.</span><span class="sxs-lookup"><span data-stu-id="fcd41-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="fcd41-152">Saate töövoo hiljem aktiveerida.</span><span class="sxs-lookup"><span data-stu-id="fcd41-152">You can activate the workflow later.</span></span>
