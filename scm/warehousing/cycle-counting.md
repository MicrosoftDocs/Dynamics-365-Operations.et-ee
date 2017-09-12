---
title: "Tsükliline inventuur"
description: "See artikkel kirjeldab, kuidas kasutada tsüklilist inventuuri laohalduse moodulis oleva ladustamislahendusega. See artikkel ei kehti moodulis Varude haldus oleva ladustamislahenduse puhul."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 90c3859f947ed7710ec16a583a6debcd07ceae67
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="cycle-counting"></a><span data-ttu-id="bd578-104">Tsükliline inventuur</span><span class="sxs-lookup"><span data-stu-id="bd578-104">Cycle counting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bd578-105">See artikkel kirjeldab, kuidas kasutada tsüklilist inventuuri laohalduse moodulis oleva ladustamislahendusega.</span><span class="sxs-lookup"><span data-stu-id="bd578-105">This article describes how you can use cycle counting with the warehousing solution that is available in Warehouse management.</span></span> <span data-ttu-id="bd578-106">See artikkel ei kehti moodulis Varude haldus oleva ladustamislahenduse puhul.</span><span class="sxs-lookup"><span data-stu-id="bd578-106">This article doesn't apply to the warehousing solution that's available in Inventory management.</span></span>

<span data-ttu-id="bd578-107">Tsükliline inventuur on laoprotsess, mida saate kaupade laovaru kontrollimiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="bd578-107">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="bd578-108">Tsüklilise inventuuri protsessi saab kirjeldada kolme etapina.</span><span class="sxs-lookup"><span data-stu-id="bd578-108">The cycle counting process can be described in three steps:</span></span>

1.  <span data-ttu-id="bd578-109">**Tsüklilise inventuuri töö loomine** – tsüklilise inventuuri töö saab luua automaatselt, tuginedes kaupade läveparameetritele või kasutades tsüklilise inventuuri plaani.</span><span class="sxs-lookup"><span data-stu-id="bd578-109">**Create cycle counting work** – Cycle counting work can be created automatically, based on threshold parameters for items or by using a cycle counting plan.</span></span> <span data-ttu-id="bd578-110">Teine võimalus on luua tsüklilise inventuuri töö käsitsi, kasutades lehel **Tsüklilise inventuuri töö kauba alusel** või lehel **Tsüklilise inventuuri töö asukoha alusel** olevaid kauba või lao parameetrid.</span><span class="sxs-lookup"><span data-stu-id="bd578-110">Alternatively, you can manually create cycle counting work by using the item or warehouse parameters on the **Cycle count work by item** page or the **Cycle count work by location** page.</span></span>
2.  <span data-ttu-id="bd578-111">**Tsüklilise inventuuri töötlemine** – pärast tsüklilise inventuuri töö loomist saab teha tsüklilise inventuuri töö, loendades lao asukohas olevad kaubad ja sisestades tulemuse mobiilse seadme abil Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="bd578-111">**Process the cycle count** – After cycle counting work is created, you do the cycle counting work by counting items in a warehouse location and then using a mobile device to enter the result in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="bd578-112">Teise võimalusena saate lugeda kaupu lao asukohas, tsüklilise inventuuri tööd loomata.</span><span class="sxs-lookup"><span data-stu-id="bd578-112">Alternatively, you can count items in a warehouse location without creating cycle counting work.</span></span> <span data-ttu-id="bd578-113">Seda protsessi nimetatakse *punkttsükliliseks inventuuriks*.</span><span class="sxs-lookup"><span data-stu-id="bd578-113">This process is referred to as *spot cycle counting*.</span></span>
3.  <span data-ttu-id="bd578-114">**Tsüklilise inventuuri väärtuse erinevuse lahendamine** – pärast tsüklilist inventuuri on vormil **Kogu töö** kaupadel, mille inventuuri käigus saadud väärtuses on erinevusi, tööolek **Ülevaatuse ootel**.</span><span class="sxs-lookup"><span data-stu-id="bd578-114">**Resolve differences in the counted value** – After a cycle count, any items that have differences in the counted value will have a work status of **Pending review** on the **All work** page.</span></span> <span data-ttu-id="bd578-115">Need erinevused saab lahendada lehel **Ülevaatuse ootel tsüklilise inventuuri töö**.</span><span class="sxs-lookup"><span data-stu-id="bd578-115">You can resolve these differences on the **Cycle count work pending review** page.</span></span>

<span data-ttu-id="bd578-116">Järgmine illustratsioon näitab tsüklilise inventuuri protsessi.</span><span class="sxs-lookup"><span data-stu-id="bd578-116">The following illustration shows the cycle counting process.</span></span> ![Tsüklilise inventuuri protsessivoog](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a><span data-ttu-id="bd578-118">Tsüklilise inventuuri eeltingimused</span><span class="sxs-lookup"><span data-stu-id="bd578-118">Cycle counting prerequisites</span></span>
<span data-ttu-id="bd578-119">Järgmises tabelis kuvatakse eeltingimused, mis peavad olema olemas, enne kui saate tsüklilist inventuuri kasutada.</span><span class="sxs-lookup"><span data-stu-id="bd578-119">The following table shows the prerequisites that must be in place before you can use cycle counting.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd578-120">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="bd578-120">Prerequisite</span></span></th>
<th><span data-ttu-id="bd578-121">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="bd578-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bd578-122">Kaup</span><span class="sxs-lookup"><span data-stu-id="bd578-122">Item</span></span></td>
<td><span data-ttu-id="bd578-123">Kauba puhul peavad olema lubatud laohaldusprotsessid.</span><span class="sxs-lookup"><span data-stu-id="bd578-123">The item must be enabled for warehouse management processes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd578-124">Ladu</span><span class="sxs-lookup"><span data-stu-id="bd578-124">Warehouse</span></span></td>
<td><span data-ttu-id="bd578-125">Laos peavad olema lubatud laohaldusprotsessid.</span><span class="sxs-lookup"><span data-stu-id="bd578-125">The warehouse must be enabled for warehouse management processes.</span></span> <span data-ttu-id="bd578-126">Laohaldusprotsesside lubamiseks laos valige ladu lehelt <strong>Laod</strong> ja märkige seejärel valik <strong>Kasuta laohaldusprotsesse</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd578-126">To enable the warehouse for warehouse management processes, on the <strong>Warehouses</strong> page, select the warehouse, and then select the <strong>Use warehouse management processes</strong> option.</span></span> <span data-ttu-id="bd578-127">Kui soovite, et töötajad saaksid tsüklilise inventuuri käigus aluseid teisaldada, märkige kiirkaardil <strong>Laohaldus</strong> ruut <strong>Luba kaubaaluse teisaldamine tsüklilises inventuuris</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd578-127">To enable workers to move pallets during a cycle count, on the <strong>Warehouse management</strong> FastTab, select the <strong>Allow pallet moves during cycle counting</strong> option.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd578-128">Töökaustad</span><span class="sxs-lookup"><span data-stu-id="bd578-128">Work pools</span></span></td>
<td><span data-ttu-id="bd578-129">Valikuline: saate luua töökausta laotöö eraldamiseks töö (praegusel juhul tsüklilise inventuuri töö) tüübi alusel.</span><span class="sxs-lookup"><span data-stu-id="bd578-129">Optional: Create a work pool to segregate the warehouse work, based on the type of work (in this case, cycle counting work).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd578-130">Asukohad</span><span class="sxs-lookup"><span data-stu-id="bd578-130">Locations</span></span></td>
<td><span data-ttu-id="bd578-131">Tsüklilise inventuuri lubamine asukohtades.</span><span class="sxs-lookup"><span data-stu-id="bd578-131">Enable cycle counting for locations.</span></span> <span data-ttu-id="bd578-132">Tsüklilise inventuuri lubamiseks lao asukoha puhul tehke lehel <strong>Asukohaprofiilid</strong> valik <strong>Luba tsükliline inventuur</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd578-132">To enable cycle counting for a warehouse location, on the <strong>Location profiles</strong> page, select the <strong>Allow cycle counting</strong> option.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd578-133">Laohalduse parameetrid</span><span class="sxs-lookup"><span data-stu-id="bd578-133">Warehouse management parameters</span></span></td>
<td><span data-ttu-id="bd578-134">Tsüklilise inventuuri parameetrite häälestamine.</span><span class="sxs-lookup"><span data-stu-id="bd578-134">Set up parameters for cycle counting.</span></span> <span data-ttu-id="bd578-135">Määrake tsüklilisele inventuurile lehel <strong>Laohalduse parameetrid</strong> vaikimisi korrigeerimistüübi kood, tööklassi ID ja töö prioriteet.</span><span class="sxs-lookup"><span data-stu-id="bd578-135">On the <strong>Warehouse management parameters</strong> page, specify the default adjustment type code, work class ID, and work priority for cycle counting.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd578-136">Mobiilne seade</span><span class="sxs-lookup"><span data-stu-id="bd578-136">Mobile device</span></span></td>
<td><ul>
<li><span data-ttu-id="bd578-137">Looge ühele järgmistest meetoditest menüü-üksus lehel <strong>Mobiilse seadme menüü-üksused</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd578-137">Create a menu item for one of the following methods on the <strong>Mobile device menu items</strong> page:</span></span>
<ul>
<li><span data-ttu-id="bd578-138">Kasutaja juhitud tsükliline inventuur</span><span class="sxs-lookup"><span data-stu-id="bd578-138">User directed cycle counting</span></span></li>
<li><span data-ttu-id="bd578-139">Süsteemi juhitud tsükliline inventuur</span><span class="sxs-lookup"><span data-stu-id="bd578-139">System directed cycle counting</span></span></li>
<li><span data-ttu-id="bd578-140">Tsüklilise inventuuri rühmitamine</span><span class="sxs-lookup"><span data-stu-id="bd578-140">Cycle count grouping</span></span></li>
<li><span data-ttu-id="bd578-141">Punkttsükliline inventuur</span><span class="sxs-lookup"><span data-stu-id="bd578-141">Spot cycle counting</span></span></li>
</ul>
</li>
<li><span data-ttu-id="bd578-142">Menüü seadistamine mobiilsele seadmele.</span><span class="sxs-lookup"><span data-stu-id="bd578-142">Set up a menu for the mobile device.</span></span></li>
<li><span data-ttu-id="bd578-143">Töö kasutajakonto loomine ja mobiilse seadme menüü määramine töö kasutaja ID-le.</span><span class="sxs-lookup"><span data-stu-id="bd578-143">Create a work user account, and assign a mobile device menu to the work user ID.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd578-144">Seostuv seadistustoiming</span><span class="sxs-lookup"><span data-stu-id="bd578-144">Related setup task</span></span></td>
<td><span data-ttu-id="bd578-145">Tsüklilise inventuuri plaani seadistamine lao asukohale.</span><span class="sxs-lookup"><span data-stu-id="bd578-145">Set up a cycle counting plan for a warehouse location.</span></span></td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a><span data-ttu-id="bd578-146">Automaatne tsüklilise inventuuri loomine</span><span class="sxs-lookup"><span data-stu-id="bd578-146">Automatically create cycle counting work</span></span>
<span data-ttu-id="bd578-147">Korduvaks tsüklilise inventuuri töö loomiseks on kaks võimalust: seadistada tsüklilise inventuuri läved või seadistada tsüklilise inventuuri plaanid.</span><span class="sxs-lookup"><span data-stu-id="bd578-147">There are two ways to schedule recurring creation of cycle counting work: set up cycle counting thresholds or set up cycle counting plans.</span></span>

-   <span data-ttu-id="bd578-148">Tsüklilise inventuuri lävi näitab laokaupade koguse või protsendi piirangut.</span><span class="sxs-lookup"><span data-stu-id="bd578-148">A cycle counting threshold indicates the quantity or percentage limit of inventory items.</span></span> <span data-ttu-id="bd578-149">Tsüklilise inventuuri töö luuakse lävepiirini jõudmisel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="bd578-149">Cycle counting work is automatically created when the threshold limit is reached.</span></span>
-   <span data-ttu-id="bd578-150">Tsüklilise inventuuri plaan loob tsüklilise inventuuri töö kohe või perioodiliselt pakett-töö kaudu.</span><span class="sxs-lookup"><span data-stu-id="bd578-150">A cycle counting plan creates cycle counting work either immediately or periodically through a batch job.</span></span> <span data-ttu-id="bd578-151">Kui tsüklilise inventuuri töö on loodud, sisaldab inventuuri töö rida teavet inventuuri asukoha kohta.</span><span class="sxs-lookup"><span data-stu-id="bd578-151">When cycle counting work is created, the counting work line includes information about the location to count.</span></span> <span data-ttu-id="bd578-152">Selle asukohaga seostatud vaba kaubavaru on blokeeritud ja on seetõttu reserveerimise ning väljamineva töötluse isegi siis, kui on olemas avatud inventuuri töö.</span><span class="sxs-lookup"><span data-stu-id="bd578-152">The on-hand inventory that is associated with this location isn't blocked, and is therefore available for reservation and outbound processing, even though open counting work exists.</span></span>

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a><span data-ttu-id="bd578-153">Tsüklilise inventuuri töö loomine kaupade läveparameetrite põhjal</span><span class="sxs-lookup"><span data-stu-id="bd578-153">Create cycle counting work, based on threshold parameters for items</span></span>

<span data-ttu-id="bd578-154">Tsüklilise inventuuri töö saab luua, kui kaupade arv langeb asukohas alla konkreetse läveväärtuse.</span><span class="sxs-lookup"><span data-stu-id="bd578-154">Cycle counting work can be created when the number of items falls below a specific threshold value in a location.</span></span> <span data-ttu-id="bd578-155">Näiteks on 60 kaupa asukohas, mille tsüklilise inventuuri läve kogus on 40.</span><span class="sxs-lookup"><span data-stu-id="bd578-155">For example, there are 60 items in a location that has a cycle counting threshold of 40.</span></span> <span data-ttu-id="bd578-156">Müügitellimuse kande käigus komplekteeritakse asukohast 25 kaupa ja need paigutatakse vaheasukohta.</span><span class="sxs-lookup"><span data-stu-id="bd578-156">During a sales order transaction, 25 items are picked from the location and put in a staging location.</span></span> <span data-ttu-id="bd578-157">Kuna uus kaupade arv 35 on lävekogusest väiksem, luuakse asukohas automaatselt tsüklilise inventuuri töö.</span><span class="sxs-lookup"><span data-stu-id="bd578-157">Because the new item count, 35, is less than the threshold quantity, cycle counting work is automatically created for the location.</span></span>

### <a name="schedule-cycle-counting-work"></a><span data-ttu-id="bd578-158">Tsüklilise inventuuri töö plaanimine</span><span class="sxs-lookup"><span data-stu-id="bd578-158">Schedule cycle counting work</span></span>

<span data-ttu-id="bd578-159">Saate ajastada tsüklilise inventuuri plaane tsüklilise inventuuri töö loomiseks kohe või perioodiliselt.</span><span class="sxs-lookup"><span data-stu-id="bd578-159">You can schedule cycle counting plans to create cycle counting work immediately or periodically.</span></span> <span data-ttu-id="bd578-160">Tsüklilise inventuuri plaanide seadistamisega saate kontrollida töökausta, mille jaoks tsüklilise inventuuri töö luuakse, maksimaalset tsükliliste inventuuride arvu, mis kaupadele erinevates asukohtades luuakse, ja päevade arvu enne lao asukohas uue inventuuri läbiviimist.</span><span class="sxs-lookup"><span data-stu-id="bd578-160">By setting up cycle counting plans, you can control the work pool that cycle counting work is created for, the maximum number of cycle counts that are created for items in different locations, and the number of days before a warehouse location is counted again.</span></span> <span data-ttu-id="bd578-161">Näiteks on kaup laos saadaval kolmes asukohas ja maksimaalseks tsükliliste inventuuride arvuks on määratud **2**.</span><span class="sxs-lookup"><span data-stu-id="bd578-161">For example, an item is available in three locations in the warehouse, and the maximum number of cycle counts is set to **2**.</span></span> <span data-ttu-id="bd578-162">Sellisel juhul luuakse tsüklilise inventuuri plaani käivitamisel kaks tsüklilist inventuuri kahes asukohas, kus kaup olemas on.</span><span class="sxs-lookup"><span data-stu-id="bd578-162">In this case, when you run the cycle counting plan, two cycle counts are created for the two locations where the item is present.</span></span> <span data-ttu-id="bd578-163">Teine näide: määrate tsükliliste inventuuride vaheliseks päevade arvuks **5**.</span><span class="sxs-lookup"><span data-stu-id="bd578-163">As another example, you set the number of days between cycle counts to **5**.</span></span> <span data-ttu-id="bd578-164">Sel juhul luuakse tsüklilise inventuuri töö iga viie päeva järel.</span><span class="sxs-lookup"><span data-stu-id="bd578-164">In this case, cycle counting work is created every five days.</span></span> <span data-ttu-id="bd578-165">Kuid kui tsüklilise inventuuri töö töödeldakse 3. päeval, luuakse järgmine tsüklilise inventuuri töö viis päeva pärast viimase tsüklilise inventuuri töö töötlemist, 8. päeval.</span><span class="sxs-lookup"><span data-stu-id="bd578-165">However, if cycle counting work is processed on day 3, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>

## <a name="create-cycle-counting-work-manually"></a><span data-ttu-id="bd578-166">Tsüklilise inventuuri loomine käsitsi</span><span class="sxs-lookup"><span data-stu-id="bd578-166">Create cycle counting work manually</span></span>
<span data-ttu-id="bd578-167">Tsüklilise inventuuri töö loomiseks käsitsi võite kasutada lehte **Tsükliline inventuur kauba alusel** või **Tsükliline inventuur asukoha alusel**.</span><span class="sxs-lookup"><span data-stu-id="bd578-167">To create cycle counting work manually, you can use the **Cycle count work by item** or **Cycle count work by location** page.</span></span> <span data-ttu-id="bd578-168">Saate määrata loodavate tsükliliste inventuuride maksimumarvu.</span><span class="sxs-lookup"><span data-stu-id="bd578-168">You can specify the maximum number of cycle counts to create.</span></span> <span data-ttu-id="bd578-169">Näiteks kui laojuhataja määrab väärtuse **5**, luuakse tsüklilise inventuuri töö viiele asukohale, isegi kui kaup on 10-s asukohas olemas.</span><span class="sxs-lookup"><span data-stu-id="bd578-169">For example, if the warehouse manager specifies a value of **5**, cycle counting work is created for five locations, even if the item is present in 10 locations.</span></span> <span data-ttu-id="bd578-170">Saate valida ka töökausta ID, kuhu loodavate tsüklilise inventuuri tööde ID-d määratakse.</span><span class="sxs-lookup"><span data-stu-id="bd578-170">You can also select a work pool ID to assign the cycle counting work IDs that are created to.</span></span> <span data-ttu-id="bd578-171">Töökausta ID töötlemisel tsüklilise inventuuri jaoks töödeldakse sellesse töökausta määratud tsüklilise inventuuri tööde ID-d grupina.</span><span class="sxs-lookup"><span data-stu-id="bd578-171">When a work pool ID is processed for cycle counting, the cycle counting work IDs that are assigned to the work pool are processed as a group.</span></span>

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a><span data-ttu-id="bd578-172">Tsüklilise inventuuri läbiviimine mobiilse seadmega</span><span class="sxs-lookup"><span data-stu-id="bd578-172">Perform a cycle count by using a mobile device</span></span>
<span data-ttu-id="bd578-173">Tsüklilise inventuuri töö tegemiseks mobiilses seadmes on Finance and Operationsis mitu võimalust.</span><span class="sxs-lookup"><span data-stu-id="bd578-173">There are several methods for processing cycle counting work by using Finance and Operations on a mobile device:</span></span>

-   <span data-ttu-id="bd578-174">**Kasutaja juhitud** – töötaja saab määrata tsüklilise inventuuri töö ID, mille olek on **Avatud**.</span><span class="sxs-lookup"><span data-stu-id="bd578-174">**User directed** – The worker can specify a cycle counting work ID that has a status of **Open**.</span></span>
-   <span data-ttu-id="bd578-175">**Süsteemi juhitud** – Finance and Operations määrab töötajale tsüklilise inventuuri töö ID.</span><span class="sxs-lookup"><span data-stu-id="bd578-175">**System directed** – Finance and Operations assigns a cycle counting work ID to the worker.</span></span>
-   <span data-ttu-id="bd578-176">**Tsüklilise inventuuri rühmitamine** – töötaja saab rühmitada teatud asukoha, tsooni või töökausta tsüklilise inventuuri töö ID-d.</span><span class="sxs-lookup"><span data-stu-id="bd578-176">**Cycle count grouping** – The worker can group cycle counting work IDs that are specific to a particular location, zone, or work pool.</span></span>
-   <span data-ttu-id="bd578-177">**Punkttsükliline inventuur** – valikuline: töötaja saab loendada kaupu lao asukohas igal ajal, tsüklilise inventuuri tööd loomata, sisestades asukoha ID.</span><span class="sxs-lookup"><span data-stu-id="bd578-177">**Spot cycle counting** – The worker can count items in a warehouse location at any time, without creating cycle counting work.</span></span> <span data-ttu-id="bd578-178">Punkttsüklilise inventuuri läbiviimiseks asukohas sisestab töötaja asukoha ID.</span><span class="sxs-lookup"><span data-stu-id="bd578-178">To perform spot cycle counting in a location, the worker enters the location ID.</span></span>

<span data-ttu-id="bd578-179">Järgmine näide illustreerib, kuidas saate mobiilse seadme abil punkttsüklilist inventuuri teha.</span><span class="sxs-lookup"><span data-stu-id="bd578-179">The following example shows how you can perform spot cycle counting by using a mobile device.</span></span> <span data-ttu-id="bd578-180">Juhised, mida töötaja seadmel näeb, erinevad, olenevalt punkttsüklilise inventuuri menüü-üksuse seadistusest.</span><span class="sxs-lookup"><span data-stu-id="bd578-180">The instructions that the worker sees on the device vary, depending on the setup of the menu item for spot cycle counting.</span></span>

1.  <span data-ttu-id="bd578-181">Valige mobiilsel seadmel menüüelement punkttsüklilise inventuuri töö töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="bd578-181">On the mobile device, select the menu item to process spot cycle counting work.</span></span>
2.  <span data-ttu-id="bd578-182">Registreerige asukoht, millele punkttsüklilist inventuuri teha.</span><span class="sxs-lookup"><span data-stu-id="bd578-182">Register the location to perform spot cycle counting for.</span></span>
3.  <span data-ttu-id="bd578-183">Registreerige ja kinnitage kaubakood ja loendatud kaupade kogus.</span><span class="sxs-lookup"><span data-stu-id="bd578-183">Register and confirm the item number and the counted item quantity.</span></span> <span data-ttu-id="bd578-184">**Märkus:** tsüklilise inventuuri olekuks määratakse **Ülevaatuse ootel** või **Suletud** lehel **Kogu töö**,olenevalt lehel **Töötaja** määratud parameetritest.</span><span class="sxs-lookup"><span data-stu-id="bd578-184">**Note:** The status of the cycle counting work is updated to either **Pending review** or **Closed** on the **All work** page, depending on the parameters that are set on the **Worker** page.</span></span>
4.  <span data-ttu-id="bd578-185">Valikuline: korrake 3. sammu asukoha ülejäänud kaupade puhul ja kinnitage, et pole rohkem loendatavaid kaupu.</span><span class="sxs-lookup"><span data-stu-id="bd578-185">Optional: Repeat step 3 for the remaining items in the location, and confirm that no additional items are available for counting.</span></span>

## <a name="resolve-cycle-counting-differences"></a><span data-ttu-id="bd578-186">Tsüklilise inventuuri erinevuste lahendamine</span><span class="sxs-lookup"><span data-stu-id="bd578-186">Resolve cycle counting differences</span></span>
<span data-ttu-id="bd578-187">Tsüklilise inventuuri erinevus ilmneb järgmistes stsenaariumides, kui valiku **On tsüklilise inventuuri ülevaataja** väärtuseks on töö kasutaja ID puhul määratud **Ei**.</span><span class="sxs-lookup"><span data-stu-id="bd578-187">A cycle counting difference occurs in the following scenarios if the **Is a cycle count supervisor** option is set to **No** for a work user ID:</span></span>

-   <span data-ttu-id="bd578-188">Loendatud väärtus jääb lehe **Töö kasutajad** väljadel **Maksimaalne protsendi piirang** või **Maksimaalse koguse piirang** määratletud hälbepiiridest välja.</span><span class="sxs-lookup"><span data-stu-id="bd578-188">The counted value isn't within the deviation limits that are specified in the **Maximum percentage limit** or **Maximum quantity limit** fields on the **Work users** page.</span></span> <span data-ttu-id="bd578-189">Näiteks on asukohas vaba kaubavaru kogus 50 ja töö kasutaja hälbepiir on 10.</span><span class="sxs-lookup"><span data-stu-id="bd578-189">For example, the on-hand inventory quantity in a location is 50, and the deviation limit for the work user is 10.</span></span> <span data-ttu-id="bd578-190">Kui töö kasutaja sisestab väärtuse, mis ei ole vahemikus 40–60, tekib erinevus.</span><span class="sxs-lookup"><span data-stu-id="bd578-190">If the work user enters a value that isn't between 40 and 60, a difference occurs.</span></span>
-   <span data-ttu-id="bd578-191">Tsüklilise inventuuri väärtus erineb vaba kaubavaru kogusest ja kindlaid hälbepiire pole määratud.</span><span class="sxs-lookup"><span data-stu-id="bd578-191">The counted value differs from the on-hand inventory quantity, and no deviation limits are set.</span></span>

<span data-ttu-id="bd578-192">Saate korrigeerida loendatud väärtuse erinevusi ja kinnitada siis loendatud väärtuse lehel **Ülevaatuse ootel tsükliline inventuur**.</span><span class="sxs-lookup"><span data-stu-id="bd578-192">You can adjust differences in the counted value and then accept the counted value on the **Cycle count pending review** page.</span></span> <span data-ttu-id="bd578-193">Kauba muudetud kogust saab kontrollida lehel **Vaba varu asukoha järgi**.</span><span class="sxs-lookup"><span data-stu-id="bd578-193">You can verify the modified count of the item quantity on the **On hand by location** page.</span></span> <span data-ttu-id="bd578-194">Loendatud väärtus lükatakse tagasi, kui erinevust ei saa kinnitada.</span><span class="sxs-lookup"><span data-stu-id="bd578-194">The counted value is rejected if the difference can't be approved.</span></span>

# <a name="see-also"></a><span data-ttu-id="bd578-195">Vt ka</span><span class="sxs-lookup"><span data-stu-id="bd578-195">See also</span></span>
[<span data-ttu-id="bd578-196">Mobiilsete seadmete konfigureerimine lao töö jaoks</span><span class="sxs-lookup"><span data-stu-id="bd578-196">Configure mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)




