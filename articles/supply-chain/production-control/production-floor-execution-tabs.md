---
title: Tootmisosakonna käivitusliidese kujundamine
description: See teema kirjeldab, kuidas kujundada kasutajaliidese sisu iga konfiguratsiooni jaoks.
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 81c5c83128bb81523dee6ede549eece7b0d80e30
ms.sourcegitcommit: d9d1ddce6a334ade8b32b5ea3ac4c1e1a8f72715
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664268"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="418af-103">Tootmisosakonna käivitusliidese kujundamine</span><span class="sxs-lookup"><span data-stu-id="418af-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="418af-104">Saate kujundada kasutajaliidese sisu iga konfiguratsiooni jaoks, mida kasutab tootmisosaoknna käivitusliides.</span><span class="sxs-lookup"><span data-stu-id="418af-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="418af-105">Näiteks võib ühe tööraku töötajal olla vaja avada tööjuhiseid mis on vajalikud, samas kui teises töörakus ei ole juhised vajalikud.</span><span class="sxs-lookup"><span data-stu-id="418af-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="418af-106">Sel juhul tuleb luua kaks konfiguratsiooni, üks nupuga, et avada dokumendi manused, ja üks ilma selle nuputa.</span><span class="sxs-lookup"><span data-stu-id="418af-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="418af-107">Vahekaardi kujundamine</span><span class="sxs-lookup"><span data-stu-id="418af-107">Design a tab</span></span>

<span data-ttu-id="418af-108">Lehel **Tootmisosakonna käivituse konfigureerimine** saate luua ja konfigureerida vahekaarte, tehes toimingupaanil valiku **Vahekaartide kujundamine**.</span><span class="sxs-lookup"><span data-stu-id="418af-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="418af-109">Iga vahekaart on jagatud neljaks osaks, nagu on näha järgmisel joonisel.</span><span class="sxs-lookup"><span data-stu-id="418af-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="418af-110">![Vahekaardi paigutus](media/pfe-tab-layout.png "Vahekaardi paigutus")</span><span class="sxs-lookup"><span data-stu-id="418af-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="418af-111">Joonisel kuvatakse järgmised elemendid.</span><span class="sxs-lookup"><span data-stu-id="418af-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="418af-112">Põhitööriistariba</span><span class="sxs-lookup"><span data-stu-id="418af-112">Primary toolbar</span></span>
1. <span data-ttu-id="418af-113">Lisatööriistariba</span><span class="sxs-lookup"><span data-stu-id="418af-113">Secondary toolbar</span></span>
1. <span data-ttu-id="418af-114">Põhivaade</span><span class="sxs-lookup"><span data-stu-id="418af-114">Main view</span></span>
1. <span data-ttu-id="418af-115">Üksikasjalik vaade</span><span class="sxs-lookup"><span data-stu-id="418af-115">Detailed view</span></span>

<span data-ttu-id="418af-116">Uue vahekaardi loomiseks ja konfigureerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="418af-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="418af-117">Avage **Tootmise juhtimine &gt; Häälestus &gt; Tootmise käivitamine**.</span><span class="sxs-lookup"><span data-stu-id="418af-117">Go to **Production control &gt; Setup &gt; Manufacturing execution**.</span></span>

1. <span data-ttu-id="418af-118">Lehe **Vahekaartide kujundamine** avamiseks valige toimingupaanil **Vahekaartide kujundamine**.</span><span class="sxs-lookup"><span data-stu-id="418af-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="418af-119">![Vahekaartide kujundamise leht](media/pfe-design-tabs.png "Vahekaartide kujundamise leht")</span><span class="sxs-lookup"><span data-stu-id="418af-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="418af-120">Valige Toimingupaanil suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="418af-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="418af-121">Määrake lehe päises järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="418af-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="418af-122">**Vahekaardi nimi** – määrake vahekaardi nimi.</span><span class="sxs-lookup"><span data-stu-id="418af-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="418af-123">**Põhivaade** – valige üks kahest eelnevalt määratletud tööloendist (*Aktiivsed tööd* või *Kõik tööd*).</span><span class="sxs-lookup"><span data-stu-id="418af-123">**Main view** - Select between the two pre-defined job lists (*Active jobs* or *All jobs*).</span></span>
    - <span data-ttu-id="418af-124">**Üksikasjalik vaade** – valige tühi väärtus või **töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="418af-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="418af-125">Kui valite tühja väärtuse, ei ole vahekaardil ühtegi üksikasjalikku vaadet. Kui valite **töö üksikasjad**, sisaldab üksikasjalik vaade põhivaates tööde loendis valitud töö üksikasjalikku kirjeldust.</span><span class="sxs-lookup"><span data-stu-id="418af-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="418af-126">Valige jaotises **Põhitööriistariba** nupud, mis peaksid põhitööriistaribal olema.</span><span class="sxs-lookup"><span data-stu-id="418af-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="418af-127">Veerus **Saadaolevad toimingud** kuvatakse loend kõigist nuppudest, mida saab lisada.</span><span class="sxs-lookup"><span data-stu-id="418af-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="418af-128">Veerg **Valitud tegevused** näitab kõigi praegusse konfiguratsiooni kaasatud nuppude loendit.</span><span class="sxs-lookup"><span data-stu-id="418af-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="418af-129">Kasutage nuppe veergude vahel, et teisaldada valitud üksused veergude vahel vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="418af-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="418af-130">Kasutage veeru **Valitud toimingud** kõrval üles- ja allanuppe, et kontrollida, millises järjekorras on nupud kasutajaliideses esitatud.</span><span class="sxs-lookup"><span data-stu-id="418af-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="418af-131">Valige jaotises **Lisa** **tööriistariba** nupud, mis peaksid lisatööriistaribal olema.</span><span class="sxs-lookup"><span data-stu-id="418af-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="418af-132">Veerus **Saadaolevad toimingud** kuvatakse loend kõigist nuppudest, mida saab lisada.</span><span class="sxs-lookup"><span data-stu-id="418af-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="418af-133">Veerg **Valitud tegevused** näitab kõigi praegusse konfiguratsiooni kaasatud nuppude loendit.</span><span class="sxs-lookup"><span data-stu-id="418af-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="418af-134">Kasutage nuppe veergude vahel, et teisaldada valitud üksused veergude vahel vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="418af-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="418af-135">Kasutage veeru **Valitud toimingud** kõrval üles- ja allanuppe, et kontrollida, millises järjekorras on nupud kasutajaliideses esitatud.</span><span class="sxs-lookup"><span data-stu-id="418af-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="418af-136">Vahekaardi seostamine konfiguratsiooniga</span><span class="sxs-lookup"><span data-stu-id="418af-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="418af-137">Kui olete kõik vajalikud vahekaardid loonud, saate need konfiguratsiooniga seostada.</span><span class="sxs-lookup"><span data-stu-id="418af-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="418af-138">Avage **Tootmise juhtimine &gt; Häälestus &gt; Tootmisosakonna käivituse konfigureerimine**.</span><span class="sxs-lookup"><span data-stu-id="418af-138">Go to **Production control &gt; Setup &gt; Configure production floor execution**.</span></span>

    <span data-ttu-id="418af-139">![Tootmisosakonna käitus](media/pfe-config-prod-floor-execution.png "Tootmisosakonna käitus")</span><span class="sxs-lookup"><span data-stu-id="418af-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="418af-140">Valige kiirkaardil **Vahekaartide valimine** käsk **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="418af-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="418af-141">Ruudustikku lisatakse uus rida.</span><span class="sxs-lookup"><span data-stu-id="418af-141">A new row is added to the grid.</span></span> <span data-ttu-id="418af-142">Selle uue rea jaoks valige vahekaardi nimi, mida soovite konfiguratsiooni lisada.</span><span class="sxs-lookup"><span data-stu-id="418af-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="418af-143">Jätkake täiendavate vahekaartide lisamist vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="418af-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="418af-144">Vahekaartide korraldamiseks vastavalt vajadusele kasutage nuppe **Nihuta üles** ja **Nihuta alla**.</span><span class="sxs-lookup"><span data-stu-id="418af-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="418af-145">Vahekaardid kuvatakse ülaltoodud kuvatõmmisel kuvatud järjekorras vasakult paremale (ülemine vahekaart kuvatakse vasakul).</span><span class="sxs-lookup"><span data-stu-id="418af-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>
