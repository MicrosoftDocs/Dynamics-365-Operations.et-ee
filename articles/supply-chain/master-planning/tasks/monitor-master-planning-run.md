---
title: Koondplaneerimise käitamise jälgimine
description: Selles teemas selgitatakse, kuidas tootmise plaanija saab näha, kas koondplaneerimise käitamine on pooleli.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 045b82af6f65b22e1c683f8de47a6df282711e6a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978124"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="e444e-103">Koondplaneerimise käitamise jälgimine</span><span class="sxs-lookup"><span data-stu-id="e444e-103">Monitor a master planning run</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a><span data-ttu-id="e444e-104">Gantti diagrammi kasutamine koondplaneerimise edenemise visualiseerimiseks</span><span class="sxs-lookup"><span data-stu-id="e444e-104">Use a Gantt chart to visualize master planning progress</span></span>

<span data-ttu-id="e444e-105">Lehel **Koondplaneerimise edenemise kuva** saate vaadata ajalooliste koondplaneerimiste käitamiste üksikasju Gantti diagrammina.</span><span class="sxs-lookup"><span data-stu-id="e444e-105">From the **View master planning progress** page, you can view details of historical master planning runs as a Gantt chart.</span></span> <span data-ttu-id="e444e-106">See funktsioon aitab teil mõista koondplaneerimise erinevatele etappidele kulutatavat aega.</span><span class="sxs-lookup"><span data-stu-id="e444e-106">This functionality can help you understand the time that is spent on the various phases of master planning.</span></span> <span data-ttu-id="e444e-107">Praeguse aktiivse planeerimistöö jaoks saab lehte **Koondplaneerimise edenemise kuva** kasutada edenemise jälgimiseks ja hinnangulise allesjäänud aja vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="e444e-107">For a current active planning job, the **View master planning progress** page can be used to track progress and view the estimated remaining time.</span></span>

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a><span data-ttu-id="e444e-108">Koondplaneerimise edenemise visualiseerimise funktsiooni sisselülitamine ja kasutamine</span><span class="sxs-lookup"><span data-stu-id="e444e-108">Turn on and use the Master plan progress visualization feature</span></span>

<span data-ttu-id="e444e-109">Sulle funktsiooni kasutamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e444e-109">To use this functionality, follow these steps.</span></span>

1. <span data-ttu-id="e444e-110">Valige tööruumis **Funktsiooni haldus** vahekaardil**Uus** loendist suvand **Koondplaneerimise edenemise visualiseerimine**.</span><span class="sxs-lookup"><span data-stu-id="e444e-110">In the **Feature management** workspace, on the **New** tab, select **Master planning progress visualization** in the list.</span></span> <span data-ttu-id="e444e-111">Kui funktsioon vahekaardile **Uus** ei ilmu, vaadake vahekaartidelt **Pole lubatud** ja **Kõik**.</span><span class="sxs-lookup"><span data-stu-id="e444e-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="e444e-112">Valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="e444e-112">Select **Enable now**.</span></span> <span data-ttu-id="e444e-113">Teise võimalusena valige **Graafik**ja seejärel valige kellaaeg, millal soovite funktsiooni sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="e444e-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

<span data-ttu-id="e444e-114">Leht **Koondplaneerimise edenemise kuva** võib kuvada nii ajaloolised planeerimistööd kui ka aktiivsed planeerimistööd.</span><span class="sxs-lookup"><span data-stu-id="e444e-114">The **View master planning progress** page can display both historical planning jobs and active planning jobs.</span></span> 

<span data-ttu-id="e444e-115">Ajalooliste planeerimistööde vaatamiseks on kaks valikut.</span><span class="sxs-lookup"><span data-stu-id="e444e-115">To view historical planning jobs, there are two options.</span></span> 

1. <span data-ttu-id="e444e-116">Avage **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid** ja seejärel valige tegumiribal suvand **Ajalugu**.</span><span class="sxs-lookup"><span data-stu-id="e444e-116">Go to **Master planning \> Setup \> Plans \> Master plans**, and then, on the Action Pane, select **History**.</span></span> <span data-ttu-id="e444e-117">Kui soovitud töö on valitud, valige **Päringud** ja valige seejärel **Kuva edenemine**</span><span class="sxs-lookup"><span data-stu-id="e444e-117">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>
1. <span data-ttu-id="e444e-118">Avage **Koondplaneerimine \> Tööruumid \> Koondplaneerimine** ja paanil Koondplaneerimine klõpsake suvandit **Ajalugu**.</span><span class="sxs-lookup"><span data-stu-id="e444e-118">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **History**.</span></span> <span data-ttu-id="e444e-119">Kui soovitud töö on valitud, valige **Päringud** ja valige seejärel **Kuva edenemine**</span><span class="sxs-lookup"><span data-stu-id="e444e-119">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="e444e-120">Aktiivsete planeerimistööde vaatamiseks on kaks valikut.</span><span class="sxs-lookup"><span data-stu-id="e444e-120">To view active planning jobs, there are two options.</span></span> 
1. <span data-ttu-id="e444e-121">Avage **Koondplaneerimine \> Tööruumid \> Koondplaneerimine** ja paanil Tegevus valige suvand **Lõpetamata planeerimisprotsess**.</span><span class="sxs-lookup"><span data-stu-id="e444e-121">Go to **Master planning \> Workspaces \> Master planning**, on the Action Pane, select **Unfinished planning process**.</span></span> <span data-ttu-id="e444e-122">Kui soovitud töö on valitud, valige **Päringud** ja valige seejärel **Kuva edenemine**.</span><span class="sxs-lookup"><span data-stu-id="e444e-122">With the desired job selected, select **Inquiries**,  and then select **View progress**.</span></span>
1. <span data-ttu-id="e444e-123">Avage **Koondplaneerimine \> Tööruumid \> Koondplaneerimine** ja paanil Koondplaneerimine klõpsake suvandit **Kuva edenemine**.</span><span class="sxs-lookup"><span data-stu-id="e444e-123">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **View progress**.</span></span> <span data-ttu-id="e444e-124">Kui soovitud töö on valitud, valige **Päringud** ja valige seejärel **Kuva edenemine**</span><span class="sxs-lookup"><span data-stu-id="e444e-124">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="e444e-125">Pange tähele, et saate aktiivseid töösid vaadata ainult siis kui planeerimistöö on töötlemisel.</span><span class="sxs-lookup"><span data-stu-id="e444e-125">Note you can view active jobs only when a planning job is processing.</span></span>

### <a name="analyze-a-master-planning-job"></a><span data-ttu-id="e444e-126">Koondplaneerimise töö analüüsimine</span><span class="sxs-lookup"><span data-stu-id="e444e-126">Analyze a master planning job</span></span>

<span data-ttu-id="e444e-127">Gantti diagrammis saate iga järgmist planeerimisprotsessi laiendada, et vaadata kulutatud aja kohta lisateavet.</span><span class="sxs-lookup"><span data-stu-id="e444e-127">In the Gantt chart, you can expand each of the following planning processes to view additional details about the time that is spent:</span></span>

- <span data-ttu-id="e444e-128">Käivitamine</span><span class="sxs-lookup"><span data-stu-id="e444e-128">Initializing</span></span>
- <span data-ttu-id="e444e-129">Andmete kustutamine ja lisamine</span><span class="sxs-lookup"><span data-stu-id="e444e-129">Deleting and inserting data</span></span>
- <span data-ttu-id="e444e-130">Laovarude plaanimine</span><span class="sxs-lookup"><span data-stu-id="e444e-130">Coverage planning</span></span>
- <span data-ttu-id="e444e-131">Hilinemised</span><span class="sxs-lookup"><span data-stu-id="e444e-131">Delays</span></span>
- <span data-ttu-id="e444e-132">Tegevusteated</span><span class="sxs-lookup"><span data-stu-id="e444e-132">Action messages</span></span>
- <span data-ttu-id="e444e-133">Lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="e444e-133">Finalization</span></span>
- <span data-ttu-id="e444e-134">Automaatkinnitamine</span><span class="sxs-lookup"><span data-stu-id="e444e-134">Auto-firming</span></span>

<span data-ttu-id="e444e-135">Gantti diagramm on kasulik tööriist, kui soovite vaadata tegevuseteadete kasutamise mõju.</span><span class="sxs-lookup"><span data-stu-id="e444e-135">The Gantt chart is a useful tool if you want to view the impact of using action messages.</span></span>

#### <a name="navigation-in-the-gantt-chart"></a><span data-ttu-id="e444e-136">Gantti diagrammis navigeerimine</span><span class="sxs-lookup"><span data-stu-id="e444e-136">Navigation in the Gantt chart</span></span>

- <span data-ttu-id="e444e-137">Valitud grupi laiendamiseks ja üksikasjade kuvamiseks valige puuvaates plussmärk (**+**).</span><span class="sxs-lookup"><span data-stu-id="e444e-137">To expand the selected group and show the details, select the plus sign (**+**) in the tree view.</span></span>
- <span data-ttu-id="e444e-138">Valitud grupi ahendamiseks valige puuvaates miinusmärk (**–**).</span><span class="sxs-lookup"><span data-stu-id="e444e-138">To collapse the selected group, select the minus sign (**–**) in the tree view.</span></span>
- <span data-ttu-id="e444e-139">Saate kasutada navigeerimiseks oma klaviatuuri.</span><span class="sxs-lookup"><span data-stu-id="e444e-139">You can use your keyboard for navigation.</span></span> <span data-ttu-id="e444e-140">Kasutage ridade vahel liikumiseks klahve **Ülesnool** ja **Allanool**.</span><span class="sxs-lookup"><span data-stu-id="e444e-140">Use the **Up arrow** and **Down arrow** keys to move between rows.</span></span> <span data-ttu-id="e444e-141">Gruppide laiendamiseks ja ahendamiseks kasutage klahve **Paremnool** ja **Vasaknool**.</span><span class="sxs-lookup"><span data-stu-id="e444e-141">Use the **Right arrow** and **Left arrow** keys to expand and collapse groups.</span></span>
- <span data-ttu-id="e444e-142">Gantti diagrammis kõikide tasemete avamiseks või sulgemiseks valige suvand **Laienda kõik** või **Ahenda kõik**.</span><span class="sxs-lookup"><span data-stu-id="e444e-142">To open or close all levels in the Gantt chart, select **Expand all** or **Collapse all**.</span></span>
- <span data-ttu-id="e444e-143">Seotud töötlemisaja vaatamiseks liikuge kursoriga üle ülesande.</span><span class="sxs-lookup"><span data-stu-id="e444e-143">To view the related processing time, hover over a task.</span></span> <span data-ttu-id="e444e-144">(Ülesanded on Gantti diagrammi madalaim tase.)</span><span class="sxs-lookup"><span data-stu-id="e444e-144">(Tasks are the lowest level in the Gantt chart.)</span></span>

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a><span data-ttu-id="e444e-145">Tööde võrdlemiseks täiendava koondplaneerimise käivitamise kuvamine</span><span class="sxs-lookup"><span data-stu-id="e444e-145">View an additional master planning run to compare jobs</span></span>

<span data-ttu-id="e444e-146">Kui valite väljal **Täiendava koondplaneerimise käivitamise kuvamine** koondplaneerimise töö, saate vaadata Gantti diagrammis täiendavat koondplaneerimise käitamist ja võrrelda kahte tööd.</span><span class="sxs-lookup"><span data-stu-id="e444e-146">By selecting a master planning job on field **Show additional master planning run**, you can view an additional master planning run in the Gantt chart and compare the two jobs.</span></span>

#### <a name="bom-level-display"></a><span data-ttu-id="e444e-147">Koosluse taseme kuva</span><span class="sxs-lookup"><span data-stu-id="e444e-147">BOM-level display</span></span>

<span data-ttu-id="e444e-148">Koosluse tasemed kuvatakse laovarude planeerimise, viivituste, tegevuste ja kinnitamiste jaoks erinevalt.</span><span class="sxs-lookup"><span data-stu-id="e444e-148">Bill of materials (BOM) levels are shown differently for coverage planning, delays, actions, and firming.</span></span>

- <span data-ttu-id="e444e-149">**Laovarude planeerimine** – koosluse tasemed on näidatud nagu oodatud.</span><span class="sxs-lookup"><span data-stu-id="e444e-149">**Coverage planning** – BOM levels are shown as expected.</span></span> <span data-ttu-id="e444e-150">Need arvutatakse ülevalt alla.</span><span class="sxs-lookup"><span data-stu-id="e444e-150">They are calculated from the top down.</span></span>

    <span data-ttu-id="e444e-151">**Näide:** koosluse tase 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="e444e-151">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="e444e-152">**Viivitused** – koosluse tasemed kuvatakse laovarude planeerimise koosluse tasemetena korrutatud –1-ga.</span><span class="sxs-lookup"><span data-stu-id="e444e-152">**Delays** – BOM levels are shown as the coverage planning BOM levels multiplied by –1.</span></span> <span data-ttu-id="e444e-153">(Teisisõnu on neil negatiivne märk.)</span><span class="sxs-lookup"><span data-stu-id="e444e-153">(In other words, they have a negative sign.)</span></span>

    <span data-ttu-id="e444e-154">**Näide:** koosluse tase –2, –1, 0</span><span class="sxs-lookup"><span data-stu-id="e444e-154">**Example:** BOM level –2, –1, 0</span></span>

- <span data-ttu-id="e444e-155">**Tegevussoovitus** – koosluse tasemed on näidatud nagu oodatud.</span><span class="sxs-lookup"><span data-stu-id="e444e-155">**Action message** – BOM levels are shown as expected.</span></span> <span data-ttu-id="e444e-156">Need arvutatakse ülevalt alla.</span><span class="sxs-lookup"><span data-stu-id="e444e-156">They are calculated from the top down.</span></span>

    <span data-ttu-id="e444e-157">**Näide:** koosluse tase 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="e444e-157">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="e444e-158">**Automaatkinnitamine** – koosluse tasemed kuvatakse 999 miinus laovarude planeerimise koosluse tase.</span><span class="sxs-lookup"><span data-stu-id="e444e-158">**Auto-firming** – BOM levels are shown as 999 minus the coverage planning BOM level.</span></span>

    <span data-ttu-id="e444e-159">**Näide:** koosluse tase 999, 998, 997</span><span class="sxs-lookup"><span data-stu-id="e444e-159">**Example:** BOM level 999, 998, 997</span></span>

<span data-ttu-id="e444e-160">Järgmine tabel võtab käitumise kokku.</span><span class="sxs-lookup"><span data-stu-id="e444e-160">The following table summarizes the behavior.</span></span>

| <span data-ttu-id="e444e-161">Kuvatav koosluse tase</span><span class="sxs-lookup"><span data-stu-id="e444e-161">BOM level that is shown</span></span> | <span data-ttu-id="e444e-162">Lõppkaup</span><span class="sxs-lookup"><span data-stu-id="e444e-162">End item</span></span> | <span data-ttu-id="e444e-163">Alamkomponent</span><span class="sxs-lookup"><span data-stu-id="e444e-163">Subcomponent</span></span> | <span data-ttu-id="e444e-164">Toormaterjal</span><span class="sxs-lookup"><span data-stu-id="e444e-164">Raw material</span></span> |
|---|---|---|---|
| <span data-ttu-id="e444e-165">Laovarude plaanimine</span><span class="sxs-lookup"><span data-stu-id="e444e-165">Coverage planning</span></span> | <span data-ttu-id="e444e-166">0</span><span class="sxs-lookup"><span data-stu-id="e444e-166">0</span></span> | <span data-ttu-id="e444e-167">1</span><span class="sxs-lookup"><span data-stu-id="e444e-167">1</span></span> | <span data-ttu-id="e444e-168">2</span><span class="sxs-lookup"><span data-stu-id="e444e-168">2</span></span> |
| <span data-ttu-id="e444e-169">Hilinemised</span><span class="sxs-lookup"><span data-stu-id="e444e-169">Delays</span></span> | <span data-ttu-id="e444e-170">0</span><span class="sxs-lookup"><span data-stu-id="e444e-170">0</span></span> | <span data-ttu-id="e444e-171">–1</span><span class="sxs-lookup"><span data-stu-id="e444e-171">–1</span></span> | <span data-ttu-id="e444e-172">–2</span><span class="sxs-lookup"><span data-stu-id="e444e-172">–2</span></span> |
| <span data-ttu-id="e444e-173">Tegevussoovitus</span><span class="sxs-lookup"><span data-stu-id="e444e-173">Action message</span></span> | <span data-ttu-id="e444e-174">0</span><span class="sxs-lookup"><span data-stu-id="e444e-174">0</span></span> | <span data-ttu-id="e444e-175">1</span><span class="sxs-lookup"><span data-stu-id="e444e-175">1</span></span> | <span data-ttu-id="e444e-176">2</span><span class="sxs-lookup"><span data-stu-id="e444e-176">2</span></span> |
| <span data-ttu-id="e444e-177">Automaatkinnitamine</span><span class="sxs-lookup"><span data-stu-id="e444e-177">Auto-firming</span></span> | <span data-ttu-id="e444e-178">999</span><span class="sxs-lookup"><span data-stu-id="e444e-178">999</span></span> | <span data-ttu-id="e444e-179">998</span><span class="sxs-lookup"><span data-stu-id="e444e-179">998</span></span> | <span data-ttu-id="e444e-180">997</span><span class="sxs-lookup"><span data-stu-id="e444e-180">997</span></span> |

#### <a name="visualize-progress"></a><span data-ttu-id="e444e-181">Edenemise visualiseerimine</span><span class="sxs-lookup"><span data-stu-id="e444e-181">Visualize progress</span></span>

<span data-ttu-id="e444e-182">Kui vaatate praegu käitatavat koondplaneerimise tööd, kuvatakse edenemine Gantti diagrammi värvide kaudu.</span><span class="sxs-lookup"><span data-stu-id="e444e-182">If you view a master planning job that is currently running, progress is shown through colors in the Gantt chart.</span></span> <span data-ttu-id="e444e-183">Järgmised värvid kehtivad sinisele teemale.</span><span class="sxs-lookup"><span data-stu-id="e444e-183">The following colors apply to the blue theme.</span></span> <span data-ttu-id="e444e-184">Teistes värvikujundustes on värvid erinevad.</span><span class="sxs-lookup"><span data-stu-id="e444e-184">For other color themes, the colors will differ.</span></span>

- <span data-ttu-id="e444e-185">**Tumesinine** – lõpuleviidud planeerimisülesanded.</span><span class="sxs-lookup"><span data-stu-id="e444e-185">**Dark blue** – Completed planning tasks.</span></span>
- <span data-ttu-id="e444e-186">**Oranž** – hetkel pooleli olev ülesanne.</span><span class="sxs-lookup"><span data-stu-id="e444e-186">**Orange** – The task that is currently in progress.</span></span>
- <span data-ttu-id="e444e-187">**Helesinine** – järelejäänud ülesannete hinnang.</span><span class="sxs-lookup"><span data-stu-id="e444e-187">**Light blue** – The estimate for remaining tasks.</span></span>

<span data-ttu-id="e444e-188">Värv kuvatakse ainult Gantti diagrammi madalaimal tasemel.</span><span class="sxs-lookup"><span data-stu-id="e444e-188">The color is shown only on the lowest level in the Gantt chart.</span></span> <span data-ttu-id="e444e-189">Koondplaneerimise tööd kõikide ülesannete vaatamiseks valige **Laienda kõik**.</span><span class="sxs-lookup"><span data-stu-id="e444e-189">Select **Expand all** to view all tasks in the master planning job.</span></span> <span data-ttu-id="e444e-190">Järelejäänud ülesannete hinnang põhineb ajaloolistel koondplaneerimise töödel.</span><span class="sxs-lookup"><span data-stu-id="e444e-190">The estimate of remaining tasks is based on historical master planning jobs.</span></span>

## <a name="run-master-planning-and-track-processing-time"></a><span data-ttu-id="e444e-191">Koondplaneerimise käitamine ja töötlemisaja jälgimine</span><span class="sxs-lookup"><span data-stu-id="e444e-191">Run master planning and track processing time</span></span>

1. <span data-ttu-id="e444e-192">Valige vaikimisi armatuurlaual **Koondplaneerimine**.</span><span class="sxs-lookup"><span data-stu-id="e444e-192">On the default dashboard, select **Master planning**.</span></span>
1. <span data-ttu-id="e444e-193">Sisestage või valige väärtus väljal **Plaan**.</span><span class="sxs-lookup"><span data-stu-id="e444e-193">In the **Plan** field, enter or select a value.</span></span>
1. <span data-ttu-id="e444e-194">Valige käsk **Käitus**.</span><span class="sxs-lookup"><span data-stu-id="e444e-194">Select **Run**.</span></span>
1. <span data-ttu-id="e444e-195">Määrake suvandi **Töötlemisaja jälgimine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e444e-195">Set the **Track processing time** option to **Yes**.</span></span>
1. <span data-ttu-id="e444e-196">Väljale **Lõimede arv** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="e444e-196">In the **Number of threads** field, enter a number.</span></span>
1. <span data-ttu-id="e444e-197">Valige kiirkaardil **Kaasatavad kirjed** suvand **Filter**.</span><span class="sxs-lookup"><span data-stu-id="e444e-197">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="e444e-198">Valige ruudustikus rida, kus väli **Väli** on määratud üksusele **Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="e444e-198">In the grid, select the row where the **Field** field is set to **Item number**.</span></span>
1. <span data-ttu-id="e444e-199">Sisestage väljal **Kriteeriumid** väärtus.</span><span class="sxs-lookup"><span data-stu-id="e444e-199">In the **Criteria** field, enter a value.</span></span>
1. <span data-ttu-id="e444e-200">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e444e-200">Select **OK**.</span></span>
