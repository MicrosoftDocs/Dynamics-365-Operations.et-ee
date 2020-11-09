---
title: Süsteemi suunatud tööde järjestus
description: Selles teemas antakse teavet süsteemi suunatud tööde järjestuse kohta. Selle funktsiooni abil saate sortida ja filtreerida töötellimusi, mida süsteem kasutajatele käivitamiseks esitab. See on kasulik olukordades, kus lao komplekteerimise protsessi juhtimiseks on lisakriteeriumid nõutavad.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 86d396b069a354b8fa7e15793372a8293273d238
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017020"
---
# <a name="system-directed-work-sequencing"></a><span data-ttu-id="dfc41-105">Süsteemi suunatud tööde järjestus</span><span class="sxs-lookup"><span data-stu-id="dfc41-105">System-directed work sequencing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dfc41-106">Süsteemi suunatud tööde järjestuse abil saate sortida ja filtreerida töötellimusi, mida süsteem kasutajatele käivitamiseks esitab.</span><span class="sxs-lookup"><span data-stu-id="dfc41-106">System-directed work sequencing lets you sort and filter the work orders that the system presents to users for execution.</span></span> <span data-ttu-id="dfc41-107">See on kasulik olukordades, kus lao komplekteerimisprotsessi juhtimiseks on lisakriteeriumid nõutavad (nt saatmise aeg, komplekteerimistsoon, asukohaprofiil või erinevate kriteeriumide kombinatsioon).</span><span class="sxs-lookup"><span data-stu-id="dfc41-107">It's helpful in scenarios where additional criteria (such as the time of shipping, the picking zone, the location profile, or a combination of various criteria) are required to drive the warehouse picking process.</span></span>

<span data-ttu-id="dfc41-108">See funktsioon laiendab praegust süsteemi suunatud komplekteerimise funktsiooni, lisades süsteemi suunatud päringu järjekorra, kus kasutajad saavad seadistada järjestust ja vähemalt ühe päringu, mis hindab kõiki loodud töökäske.</span><span class="sxs-lookup"><span data-stu-id="dfc41-108">This functionality extends the current system-directed picking functionality by adding a system-directed query order, where users can set up a sequence and one or more queries that will evaluate all work orders that are created.</span></span> <span data-ttu-id="dfc41-109">Hõivatakse ja esitatakse ainult need töökäsud, mis vastavad mobiilse seadme menüü-üksuse häälestuses määratud.</span><span class="sxs-lookup"><span data-stu-id="dfc41-109">Only work orders that meet the criteria that are specified in the setup of the mobile device menu item will be captured and presented.</span></span>

<span data-ttu-id="dfc41-110">Seetõttu võimaldab see funktsioon lao komplekteerimise protsesse täiendavalt optimeerida, kuna see tuvastab määratud kriteeriumidele vastavaid töökäskusid, määrab need õigele mobiilse seadme menüü-üksusele ja esitab need seejärel töötajale kindlate oskuste, komplekteerimisseadmete või muude nõuete põhjal.</span><span class="sxs-lookup"><span data-stu-id="dfc41-110">Therefore, this functionality allows for further optimization of warehouse picking processes as it identifies work orders that match the specified criteria, assigns them to the correct mobile device menu item, and then presents them to a worker, based on a specific skill set, picking equipment, or other requirement.</span></span>

> [!NOTE]
> <span data-ttu-id="dfc41-111">Kui on vaja muid kriteeriume, tuleb kasutada mitut mobiilse seadme menüü-üksust.</span><span class="sxs-lookup"><span data-stu-id="dfc41-111">If different criteria are needed, multiple mobile device menu items must be used.</span></span>

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a><span data-ttu-id="dfc41-112">Lülitage sisse organisatsiooniülene süsteemi suunatud töö järjestamise funktsioon</span><span class="sxs-lookup"><span data-stu-id="dfc41-112">Turn on the Organization-wide system directed work sequencing feature</span></span>

<span data-ttu-id="dfc41-113">Enne süsteemi suunatud tööde järjestamise kasutamist peate selle funktsiooni oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="dfc41-113">Before you can use system-directed work sequencing, the feature must be turned on in your system.</span></span> <span data-ttu-id="dfc41-114">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="dfc41-114">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="dfc41-115">Seega on funktsioon loetletud järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="dfc41-115">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="dfc41-116">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="dfc41-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="dfc41-117">**Funktsiooni nimi:** *Organisatsiooniülene süsteemi suunatud töö järjestamine*</span><span class="sxs-lookup"><span data-stu-id="dfc41-117">**Feature name:** *Organization-wide system directed work sequencing*</span></span>

## <a name="setup"></a><span data-ttu-id="dfc41-118">Häälestus</span><span class="sxs-lookup"><span data-stu-id="dfc41-118">Setup</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="dfc41-119">Demoandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="dfc41-119">Make demo data available</span></span>

<span data-ttu-id="dfc41-120">Selle stsenaariumi kasutamiseks selles teemas esitletud väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed demoandmed.</span><span class="sxs-lookup"><span data-stu-id="dfc41-120">To work through the scenario by using the values that are presented in this topic, you must work on a system where the standard demo data is installed.</span></span> <span data-ttu-id="dfc41-121">Peate valima ka juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-121">Additionally, you must select the **USMF** legal entity.</span></span> <span data-ttu-id="dfc41-122">Stsenaarium kasutab ladu *51* demoandmetest.</span><span class="sxs-lookup"><span data-stu-id="dfc41-122">The scenario uses warehouse *51* from the demo data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dfc41-123">Enne tellimuste lattu vabastamist veenduge, et komplekteerimise asukohtadel on tellimuste kõigi üksuste jaoks piisavalt varusid.</span><span class="sxs-lookup"><span data-stu-id="dfc41-123">Before you release the orders to the warehouse, make sure that the pick locations have enough inventory for all the items on the orders.</span></span>
>
> <span data-ttu-id="dfc41-124">Vaikimisi USMF-andmed peaksid seda stsenaariumi toetama.</span><span class="sxs-lookup"><span data-stu-id="dfc41-124">Default USMF data should support this scenario.</span></span> <span data-ttu-id="dfc41-125">Kui te ei kasuta demoandmeid, vaadake üle seadistus **Asukohakorraldus** , et teada, milliseid komplekteerimise asukohti müügitellimuse komplekteerimiseks kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="dfc41-125">If you aren't using demo data, review the **Location directive** setting to learn which picking locations are used for sales order picking.</span></span> <span data-ttu-id="dfc41-126">Kui peate korrigeerima varusid, saate luua käsitsi liikumisi, kasutada täiendamist või kasutada mis tahes muud voogu.</span><span class="sxs-lookup"><span data-stu-id="dfc41-126">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span>

### <a name="set-up-a-mobile-device-menu-item"></a><span data-ttu-id="dfc41-127">Mobiilse seadme menüü-üksuse seadistamine</span><span class="sxs-lookup"><span data-stu-id="dfc41-127">Set up a mobile device menu item</span></span>

1. <span data-ttu-id="dfc41-128">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-128">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="dfc41-129">Valige mobiilse seadme menüü-üksuste loendist suvand **Müügi komplekteerimine – süsteem**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-129">In the list of mobile device menu items, select **Sales Picking – System**.</span></span> <span data-ttu-id="dfc41-130">Nõutav menüü-üksus peaks juba olema olemas.</span><span class="sxs-lookup"><span data-stu-id="dfc41-130">The required menu item should already exist.</span></span> 
1. <span data-ttu-id="dfc41-131">Kinnitage järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="dfc41-131">Confirm the following settings:</span></span>

    - <span data-ttu-id="dfc41-132">Määrake kiirkaardi **Üldine** väljal **Suunaja** väärtuseks *Süsteemi suunatud*.</span><span class="sxs-lookup"><span data-stu-id="dfc41-132">On the **General** FastTab, the **Directed by** field should be set to *System directed*.</span></span>
    - <span data-ttu-id="dfc41-133">Kiirkaardil **Tööklassid** peaksid olema järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="dfc41-133">The **Work classes** FastTab should show the following settings.</span></span>

        | <span data-ttu-id="dfc41-134">Töö klassi ID</span><span class="sxs-lookup"><span data-stu-id="dfc41-134">Work class ID</span></span> | <span data-ttu-id="dfc41-135">Töötellimuse tüüp</span><span class="sxs-lookup"><span data-stu-id="dfc41-135">Work order type</span></span> |
        |---|---|
        | <span data-ttu-id="dfc41-136">Sales</span><span class="sxs-lookup"><span data-stu-id="dfc41-136">Sales</span></span> | <span data-ttu-id="dfc41-137">Müügitellimused</span><span class="sxs-lookup"><span data-stu-id="dfc41-137">Sales orders</span></span> |
        | <span data-ttu-id="dfc41-138">SO-komplekteerimine</span><span class="sxs-lookup"><span data-stu-id="dfc41-138">SO Pick</span></span> | <span data-ttu-id="dfc41-139">Müügitellimused</span><span class="sxs-lookup"><span data-stu-id="dfc41-139">Sales orders</span></span> |

1. <span data-ttu-id="dfc41-140">Valige toimingupaanil **Süsteemi suunatud tööde järjestuse päringud**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-140">On the Action Pane, select **System directed work sequence queries**.</span></span>
1. <span data-ttu-id="dfc41-141">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-141">Select **Edit**.</span></span>
1. <span data-ttu-id="dfc41-142">Kustutage olemasolev rida ja seejärel kinnitage tegevus, valides **Jah**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-142">Delete the existing line, and then confirm the action by selecting **Yes**.</span></span>
1. <span data-ttu-id="dfc41-143">Rea loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-143">On the Action Pane, select **New** to create a line.</span></span>
1. <span data-ttu-id="dfc41-144">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dfc41-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dfc41-145">**Järjekorranumber:** *1*</span><span class="sxs-lookup"><span data-stu-id="dfc41-145">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="dfc41-146">**Kirjelduse väli:** *Töö kogus on alla 20 ja kahaneb*</span><span class="sxs-lookup"><span data-stu-id="dfc41-146">**Description field:** *Work quantity less than 20 and Descending*</span></span>

1. <span data-ttu-id="dfc41-147">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-147">Select **Save**.</span></span>
1. <span data-ttu-id="dfc41-148">Valige toimingupaanil **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-148">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="dfc41-149">Laiendage vahekaardil **Liitmised** liitmise hierarhiat, et kuvada tabel **Tööread**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-149">On the **Joins** tab, expand the join hierarchy to show the **Work lines** table.</span></span>
1. <span data-ttu-id="dfc41-150">Valige tabeli liitmine **Tööread**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-150">Select the **Work lines** table join.</span></span>
1. <span data-ttu-id="dfc41-151">Valige **Lisa tabeli liitmine**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-151">Select **Add table join**.</span></span>
1. <span data-ttu-id="dfc41-152">Otsige kuvatavast loendist ja valige järgmiste sätetega rida.</span><span class="sxs-lookup"><span data-stu-id="dfc41-152">In the list that appears, find and select the row that has the following settings:</span></span>

    - <span data-ttu-id="dfc41-153">**Liitmisrežiim:** *n:1*</span><span class="sxs-lookup"><span data-stu-id="dfc41-153">**Join mode:** *n:1*</span></span>
    - <span data-ttu-id="dfc41-154">**Seos:** *Asukohad (asukoht)*</span><span class="sxs-lookup"><span data-stu-id="dfc41-154">**Relation:** *Locations (Location)*</span></span>

1. <span data-ttu-id="dfc41-155">Valige käsk **Vali**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-155">Select **Select**.</span></span>

    <span data-ttu-id="dfc41-156">Asukohad lisatakse tabeli liitmisse.</span><span class="sxs-lookup"><span data-stu-id="dfc41-156">Locations are added to the table join.</span></span>

1. <span data-ttu-id="dfc41-157">Valige vahekaardil **Sortimine** suvand **Lisa** , et lisada rida.</span><span class="sxs-lookup"><span data-stu-id="dfc41-157">On the **Sorting** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="dfc41-158">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dfc41-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dfc41-159">**Tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="dfc41-159">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="dfc41-160">**Tuletatud tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="dfc41-160">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="dfc41-161">**Väli:** *Töö kogus* (valige kuvatavas teateaknas **Jah** , et lisada sellele väljale sortimine.)</span><span class="sxs-lookup"><span data-stu-id="dfc41-161">**Field:** *Work quantity* (In the message box that appears, select **Yes** to add sorting to this field.)</span></span>
    - <span data-ttu-id="dfc41-162">**Otsingusuund:** *Kahanev*</span><span class="sxs-lookup"><span data-stu-id="dfc41-162">**Search direction:** *Descending*</span></span>

1. <span data-ttu-id="dfc41-163">Valige vahekaart **Vahemik**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-163">Select the **Range** tab.</span></span>

    <span data-ttu-id="dfc41-164">Kui järjestuses peaksid olema kaasatud ainult kindlad töökriteeriumid, saate need määrata vahekaardil **Vahemik**. Selles näites soovite kaasata ainult töö, kus kogus on väiksem kui 20 ea (madalaim mõõtühik).</span><span class="sxs-lookup"><span data-stu-id="dfc41-164">If only specific work criteria should be included in the sequencing, you can specify them on the **Range** tab. In this example, you want to include only work where the quantity is less than 20 ea (the lowest unit of measure).</span></span>

    <span data-ttu-id="dfc41-165">Pange tähele, et osad read on juba kaasatud.</span><span class="sxs-lookup"><span data-stu-id="dfc41-165">Notice that some lines are already included.</span></span> <span data-ttu-id="dfc41-166">Neid ridu ei tohi eemaldada.</span><span class="sxs-lookup"><span data-stu-id="dfc41-166">Those lines should not be removed.</span></span>

1. <span data-ttu-id="dfc41-167">Rea lisamiseks valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-167">Select **Add** to add a line.</span></span>
1. <span data-ttu-id="dfc41-168">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dfc41-168">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dfc41-169">**Tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="dfc41-169">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="dfc41-170">**Tuletatud tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="dfc41-170">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="dfc41-171">**Väli:** *Varude töö kogus*</span><span class="sxs-lookup"><span data-stu-id="dfc41-171">**Field:** *Inventory work quantity*</span></span>
    - <span data-ttu-id="dfc41-172">**Kriteeriumid:** *\<20* (vähem kui 20)</span><span class="sxs-lookup"><span data-stu-id="dfc41-172">**Criteria:** *\<20* (less than 20)</span></span>

1. <span data-ttu-id="dfc41-173">Teise rea lisamiseks valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-173">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="dfc41-174">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dfc41-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dfc41-175">**Tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="dfc41-175">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="dfc41-176">**Tuletatud tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="dfc41-176">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="dfc41-177">**Väli:** *Töö tüüp*</span><span class="sxs-lookup"><span data-stu-id="dfc41-177">**Field:** *Work type*</span></span>
    - <span data-ttu-id="dfc41-178">**Kriteeriumid:** *Komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="dfc41-178">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="dfc41-179">Teise rea lisamiseks valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-179">Select **Add** to add another line.</span></span>
1. <span data-ttu-id="dfc41-180">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dfc41-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dfc41-181">**Tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="dfc41-181">**Table:** *Locations*</span></span>
    - <span data-ttu-id="dfc41-182">**Tuletatud tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="dfc41-182">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="dfc41-183">**Väli:** *Asukohaprofiili ID*</span><span class="sxs-lookup"><span data-stu-id="dfc41-183">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="dfc41-184">**Kriteeriumid:** *!ETAPP*</span><span class="sxs-lookup"><span data-stu-id="dfc41-184">**Criteria:** *!STAGE*</span></span>

        > [!IMPORTANT]
        > <span data-ttu-id="dfc41-185">Lisage kindlasti ka hüüumärk ( *!* ) suvandi *ETAPP* ette.</span><span class="sxs-lookup"><span data-stu-id="dfc41-185">Be sure to include the exclamation point ( *!* ) in front of *STAGE*.</span></span>

1. <span data-ttu-id="dfc41-186">Päringu salvestamiseks ja sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-186">Select **OK** to save and close the query.</span></span>
1. <span data-ttu-id="dfc41-187">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-187">Select **Save**.</span></span>
1. <span data-ttu-id="dfc41-188">Sulgege leht lehele **Mobiilse seadme menüü-üksused** naasmiseks.</span><span class="sxs-lookup"><span data-stu-id="dfc41-188">Close the page to return to the **Mobile device menu items** page.</span></span>

> [!NOTE]
> <span data-ttu-id="dfc41-189">See häälestus määratleb kriteeriumid, mida kasutatakse sobiva töö sisestamiseks mobiilse seadme menüü-üksusesse.</span><span class="sxs-lookup"><span data-stu-id="dfc41-189">This setup defines the criteria that will be used to feed eligible work to the mobile device menu item.</span></span> <span data-ttu-id="dfc41-190">Kui lisate päringusse veel kriteeriumide ridu, kasutab süsteem kõigepealt päringu rida, millel on väikseim järjekorranumber.</span><span class="sxs-lookup"><span data-stu-id="dfc41-190">If you add more criteria lines to the query, the system will use the query line that has lowest sequence number first.</span></span> <span data-ttu-id="dfc41-191">Teisisõnu, kõigepealt esitatajse kasutajale kõik sobivad tööd järjekorranumbriga 1 ja seejärel kõik tööd järjekorranumbriga 2.</span><span class="sxs-lookup"><span data-stu-id="dfc41-191">In other words, all eligible work for sequence number 1 will be presented to the user first, and then all work for sequence number 2.</span></span> <span data-ttu-id="dfc41-192">Seetõttu, kui kindlat vahemikku ja sortimist tuleb kasutada koos, tuleb need määrata samas süsteemi suunatud tööde järjestuse päringus.</span><span class="sxs-lookup"><span data-stu-id="dfc41-192">Therefore, if a specific range and sorting must be used together, they should be specified in the same system-directed work sequence query.</span></span>
>
> <span data-ttu-id="dfc41-193">See seadistus hõivab mis tahes töö, millel on vähemalt üks rida, kus kogus on väiksem kui 20 ea.</span><span class="sxs-lookup"><span data-stu-id="dfc41-193">This setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="dfc41-194">Seega, kui töös on rida, kus kogus on täpselt 20 ea või üle selle, on see kehtiv, tingimusel, et sellel on ka vähemalt üks rida, kus kogus on väiksem kui 20 ea.</span><span class="sxs-lookup"><span data-stu-id="dfc41-194">Therefore, if the work has a line where the quantity is exactly 20 ea or more than 20 ea, it will be valid, provided that it also has at least one line where the quantity is less than 20 ea.</span></span>

### <a name="location-directives"></a><span data-ttu-id="dfc41-195">Asukohakorraldus</span><span class="sxs-lookup"><span data-stu-id="dfc41-195">Location directives</span></span>

<span data-ttu-id="dfc41-196">Kui kasutate Contoso vaikeandmeid, ei nõua asukohakorralduse tegevuse päring muudatusi.</span><span class="sxs-lookup"><span data-stu-id="dfc41-196">If you're using default Contoso data, the query for the location directive action won't require changes.</span></span> <span data-ttu-id="dfc41-197">Kuid veendumaks, et asukohakorraldused hõivaksid müügitellimuste kaubad, kui rakendate funktsiooni mitte-Contoso keskkonnas, looge uus asukohakorraldus.</span><span class="sxs-lookup"><span data-stu-id="dfc41-197">However, to make sure that the location directives will capture the items on the sales orders when you apply the feature in a non-Contoso environment, create a new location directive.</span></span> <span data-ttu-id="dfc41-198">Demokeskkonnas sätete kinnitamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="dfc41-198">To verify the settings in the demo environment, follow these steps.</span></span>

1. <span data-ttu-id="dfc41-199">Avage **Laohaldus** \> **Seadistus** \> **Asukohakorraldused**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-199">Go to **Warehouse management** \> **Setup** \> **Location directives**.</span></span>
1. <span data-ttu-id="dfc41-200">Valige väljal **Töökäsu tüüp** suvand *Müügitellimused*.</span><span class="sxs-lookup"><span data-stu-id="dfc41-200">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="dfc41-201">Valige asukohakorraldus, mille nimi on *51 komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="dfc41-201">Select the location directive that is named *51 Pick*.</span></span>
1. <span data-ttu-id="dfc41-202">Valige kiirkaardil **Asukohakorralduse tegevused** toimingu **Komplekteerimine** kohta käiv rida.</span><span class="sxs-lookup"><span data-stu-id="dfc41-202">On the **Location Directive Actions** FastTab, select the line for the **Pick** action.</span></span>
1. <span data-ttu-id="dfc41-203">Valige ruudustiku kohal **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-203">Select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="dfc41-204">Vaadake üle päring **Vahemik**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-204">Review the **Range** query.</span></span>

    1. <span data-ttu-id="dfc41-205">Otsige üles rida, kus välja **Väli** väärtuseks on seatud *Asukoht*.</span><span class="sxs-lookup"><span data-stu-id="dfc41-205">Find the line where the **Field** field is set to *Location*.</span></span>
    2. <span data-ttu-id="dfc41-206">Veenduge, et väli **Kriteerium** oleks tühi (st piiranguid pole).</span><span class="sxs-lookup"><span data-stu-id="dfc41-206">Make sure that the **Criteria** field is blank (that is, there are no restrictions).</span></span>

## <a name="scenario"></a><span data-ttu-id="dfc41-207">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="dfc41-207">Scenario</span></span>

### <a name="create-sales-order-picking-work"></a><span data-ttu-id="dfc41-208">Müügitellimuse komplekteerimistöö loomine</span><span class="sxs-lookup"><span data-stu-id="dfc41-208">Create sales order picking work</span></span>

<span data-ttu-id="dfc41-209">Enne süsteemi suunatud komplekteerimise käitamist tuleb luua väljaminevaid töid.</span><span class="sxs-lookup"><span data-stu-id="dfc41-209">Before system-directed picking is run, some outbound work should be created.</span></span> <span data-ttu-id="dfc41-210">Selle stsenaariumi puhul loote neli müügitellimust, mis põhinevad määratud süsteemi suunatud tööde järjestuse päringutel.</span><span class="sxs-lookup"><span data-stu-id="dfc41-210">For this scenario, you will create four sales orders that are based on the specified system-directed work sequence queries.</span></span>

<span data-ttu-id="dfc41-211">Iga müügitellimuse jaoks tuleb reserveerida varude kogused.</span><span class="sxs-lookup"><span data-stu-id="dfc41-211">You will reserve inventory quantities for each sales order.</span></span> <span data-ttu-id="dfc41-212">Seetõttu ei saa reserveeritud varusid laost teiste tellimuste jaoks võtta ilma varude reserveeringu täieliku või osalise tühistamiseta.</span><span class="sxs-lookup"><span data-stu-id="dfc41-212">Therefore, reserved inventory can't be withdrawn from the warehouse for other orders unless the inventory reservation, or part of the inventory reservation, is canceled.</span></span>

<span data-ttu-id="dfc41-213">Seejärel vabastate iga müügitellimuse lattu, et luua väljaminev töö.</span><span class="sxs-lookup"><span data-stu-id="dfc41-213">You will then release each sales order to the warehouse to create the outbound work.</span></span>

#### <a name="sales-order-1"></a><span data-ttu-id="dfc41-214">Müügitellimus 1</span><span class="sxs-lookup"><span data-stu-id="dfc41-214">Sales order 1</span></span>

1. <span data-ttu-id="dfc41-215">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-215">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="dfc41-216">Müügitellimuse 1 loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-216">On the Action Pane, select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="dfc41-217">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dfc41-217">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="dfc41-218">Määrake jaotise **Klient** välja **Kliendi konto** väärtuseks *US-004*.</span><span class="sxs-lookup"><span data-stu-id="dfc41-218">In the **Customer** section, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="dfc41-219">Määrake jaotise **Üldine** välja **Ladu** väärtuseks *51*.</span><span class="sxs-lookup"><span data-stu-id="dfc41-219">In the **General** section, set the **Warehouse** field to *51*.</span></span>

1. <span data-ttu-id="dfc41-220">Valige dialoogiboksi sulgemiseks suvand **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-220">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="dfc41-221">Märkige üles müügitellimuse number.</span><span class="sxs-lookup"><span data-stu-id="dfc41-221">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="dfc41-222">Lisage uuele müügitellimusele rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dfc41-222">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="dfc41-223">**Kauba kood:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="dfc41-223">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="dfc41-224">**Kogus:** *20*</span><span class="sxs-lookup"><span data-stu-id="dfc41-224">**Quantity:** *20*</span></span>

1. <span data-ttu-id="dfc41-225">Valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-225">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="dfc41-226">Valige lehel **Reserveerimine** varude reserveerimiseks suvand **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-226">On the **Reservation** page, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="dfc41-227">Sulgege leht **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-227">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="dfc41-228">Tehke Toimingupaani vahekaardil **Ladu** valik **Lattu väljastamine** , et luua lao jaoks töö.</span><span class="sxs-lookup"><span data-stu-id="dfc41-228">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse** to create work for the warehouse.</span></span>

    <span data-ttu-id="dfc41-229">Saate teabesõnumid, mis näitavad selle müügitellimuse jaoks loodud voo ID ja saadetise ID-d.</span><span class="sxs-lookup"><span data-stu-id="dfc41-229">You receive informational messages that show the wave ID and shipment IDs that were created for the sales order.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="dfc41-230">Müügitellimus 2</span><span class="sxs-lookup"><span data-stu-id="dfc41-230">Sales order 2</span></span>

1. <span data-ttu-id="dfc41-231">Müügitellimuse 2 loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-231">On the Action Pane, select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="dfc41-232">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dfc41-232">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="dfc41-233">**Kliendi konto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="dfc41-233">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="dfc41-234">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="dfc41-234">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="dfc41-235">Valige dialoogiboksi sulgemiseks suvand **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-235">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="dfc41-236">Märkige üles müügitellimuse number.</span><span class="sxs-lookup"><span data-stu-id="dfc41-236">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="dfc41-237">Lisage uuele müügitellimusele rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dfc41-237">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="dfc41-238">**Kauba kood:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="dfc41-238">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="dfc41-239">**Kogus:** *5*</span><span class="sxs-lookup"><span data-stu-id="dfc41-239">**Quantity:** *5*</span></span>

1. <span data-ttu-id="dfc41-240">Valige **Lisa rida** , et lisada teine rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dfc41-240">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="dfc41-241">**Kauba kood:** *M9201*</span><span class="sxs-lookup"><span data-stu-id="dfc41-241">**Item number:** *M9201*</span></span>
    - <span data-ttu-id="dfc41-242">**Kogus:** *1*</span><span class="sxs-lookup"><span data-stu-id="dfc41-242">**Quantity:** *1*</span></span>

1. <span data-ttu-id="dfc41-243">Reserveerige varud mõlemale reale.</span><span class="sxs-lookup"><span data-stu-id="dfc41-243">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="dfc41-244">Väljastage tellimus lattu.</span><span class="sxs-lookup"><span data-stu-id="dfc41-244">Release the order to the warehouse.</span></span>

#### <a name="sales-order-3"></a><span data-ttu-id="dfc41-245">Müügitellimus 3</span><span class="sxs-lookup"><span data-stu-id="dfc41-245">Sales order 3</span></span>

1. <span data-ttu-id="dfc41-246">Müügitellimuse 3 loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-246">On the Action Pane, select **New** to create sales order 3.</span></span>
1. <span data-ttu-id="dfc41-247">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dfc41-247">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="dfc41-248">**Kliendi konto:** *US-009*</span><span class="sxs-lookup"><span data-stu-id="dfc41-248">**Customer account:** *US-009*</span></span>
    - <span data-ttu-id="dfc41-249">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="dfc41-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="dfc41-250">Valige dialoogiboksi sulgemiseks suvand **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-250">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="dfc41-251">Märkige üles müügitellimuse number.</span><span class="sxs-lookup"><span data-stu-id="dfc41-251">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="dfc41-252">Lisage uuele müügitellimusele rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dfc41-252">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="dfc41-253">**Kauba kood:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="dfc41-253">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="dfc41-254">**Kogus:** *7*</span><span class="sxs-lookup"><span data-stu-id="dfc41-254">**Quantity:** *7*</span></span>

1. <span data-ttu-id="dfc41-255">Valige **Lisa rida** , et lisada teine rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dfc41-255">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="dfc41-256">**Kauba kood:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="dfc41-256">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="dfc41-257">**Kogus:** *8*</span><span class="sxs-lookup"><span data-stu-id="dfc41-257">**Quantity:** *8*</span></span>

1. <span data-ttu-id="dfc41-258">Reserveerige varud mõlemale reale.</span><span class="sxs-lookup"><span data-stu-id="dfc41-258">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="dfc41-259">Väljastage tellimus lattu.</span><span class="sxs-lookup"><span data-stu-id="dfc41-259">Release the order to the warehouse.</span></span>

#### <a name="sales-order-4"></a><span data-ttu-id="dfc41-260">Müügitellimus 4</span><span class="sxs-lookup"><span data-stu-id="dfc41-260">Sales order 4</span></span>

1. <span data-ttu-id="dfc41-261">Müügitellimuse 4 loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-261">On the Action Pane, select **New** to create sales order 4.</span></span>
1. <span data-ttu-id="dfc41-262">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dfc41-262">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="dfc41-263">**Kliendi konto:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="dfc41-263">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="dfc41-264">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="dfc41-264">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="dfc41-265">Valige dialoogiboksi sulgemiseks suvand **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-265">Select **OK** to close the dialog box.</span></span> <span data-ttu-id="dfc41-266">Märkige üles müügitellimuse number.</span><span class="sxs-lookup"><span data-stu-id="dfc41-266">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="dfc41-267">Lisage uuele müügitellimusele rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dfc41-267">Add a line to the new sales order, and set the following values:</span></span>

    - <span data-ttu-id="dfc41-268">**Kauba kood:** *M9200*</span><span class="sxs-lookup"><span data-stu-id="dfc41-268">**Item number:** *M9200*</span></span>
    - <span data-ttu-id="dfc41-269">**Kogus:** *25*</span><span class="sxs-lookup"><span data-stu-id="dfc41-269">**Quantity:** *25*</span></span>

1. <span data-ttu-id="dfc41-270">Valige **Lisa rida** , et lisada teine rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dfc41-270">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="dfc41-271">**Kauba kood:** *M9202*</span><span class="sxs-lookup"><span data-stu-id="dfc41-271">**Item number:** *M9202*</span></span>
    - <span data-ttu-id="dfc41-272">**Kogus:** *10*</span><span class="sxs-lookup"><span data-stu-id="dfc41-272">**Quantity:** *10*</span></span>

1. <span data-ttu-id="dfc41-273">Reserveerige varud mõlemale reale.</span><span class="sxs-lookup"><span data-stu-id="dfc41-273">Reserve inventory for both lines.</span></span>
1. <span data-ttu-id="dfc41-274">Väljastage tellimus lattu.</span><span class="sxs-lookup"><span data-stu-id="dfc41-274">Release the order to the warehouse.</span></span>

### <a name="get-work-ids-for-the-work-that-was-created"></a><span data-ttu-id="dfc41-275">Loodud töö jaoks töö ID-de hankimine</span><span class="sxs-lookup"><span data-stu-id="dfc41-275">Get work IDs for the work that was created</span></span>

1. <span data-ttu-id="dfc41-276">Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-276">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="dfc41-277">Filtreerige välja **Ladu** , et kuvatakse ainult lao *51* töö.</span><span class="sxs-lookup"><span data-stu-id="dfc41-277">Filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="dfc41-278">Neli töö ID-d peaks olema loodud.</span><span class="sxs-lookup"><span data-stu-id="dfc41-278">Four work IDs should have been created.</span></span> <span data-ttu-id="dfc41-279">Märkige üles kõigi müügitellimuste töö ID-d.</span><span class="sxs-lookup"><span data-stu-id="dfc41-279">Make a note of the work ID for each sales order.</span></span>

    | <span data-ttu-id="dfc41-280">Müügitellimuse ID</span><span class="sxs-lookup"><span data-stu-id="dfc41-280">Sales order ID</span></span> | <span data-ttu-id="dfc41-281">Töö ID</span><span class="sxs-lookup"><span data-stu-id="dfc41-281">Work ID</span></span> | <span data-ttu-id="dfc41-282">Töö kogus</span><span class="sxs-lookup"><span data-stu-id="dfc41-282">Work quantity</span></span> |
    |---|---|---|
    | <span data-ttu-id="dfc41-283">Müügitellimus 1</span><span class="sxs-lookup"><span data-stu-id="dfc41-283">Sales Order 1</span></span> | <span data-ttu-id="dfc41-284">Töö ID 1</span><span class="sxs-lookup"><span data-stu-id="dfc41-284">Work ID 1</span></span> | <span data-ttu-id="dfc41-285">20 ea</span><span class="sxs-lookup"><span data-stu-id="dfc41-285">20 ea</span></span> |
    | <span data-ttu-id="dfc41-286">Müügitellimus 2</span><span class="sxs-lookup"><span data-stu-id="dfc41-286">Sales Order 2</span></span> | <span data-ttu-id="dfc41-287">Töö ID 2</span><span class="sxs-lookup"><span data-stu-id="dfc41-287">Work ID 2</span></span> | <span data-ttu-id="dfc41-288">6 ea (mõlema rea summa)</span><span class="sxs-lookup"><span data-stu-id="dfc41-288">6 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="dfc41-289">Müügitellimus 3</span><span class="sxs-lookup"><span data-stu-id="dfc41-289">Sales Order 3</span></span> | <span data-ttu-id="dfc41-290">Töö ID 3</span><span class="sxs-lookup"><span data-stu-id="dfc41-290">Work ID 3</span></span> | <span data-ttu-id="dfc41-291">15 ea (mõlema rea summa)</span><span class="sxs-lookup"><span data-stu-id="dfc41-291">15 ea (sum of both lines)</span></span> |
    | <span data-ttu-id="dfc41-292">Müügitellimus 4</span><span class="sxs-lookup"><span data-stu-id="dfc41-292">Sales Order 4</span></span> | <span data-ttu-id="dfc41-293">Töö ID 4</span><span class="sxs-lookup"><span data-stu-id="dfc41-293">Work ID 4</span></span> | <span data-ttu-id="dfc41-294">35 ea (mõlema rea summa)</span><span class="sxs-lookup"><span data-stu-id="dfc41-294">35 ea (sum of both lines)</span></span> |

<span data-ttu-id="dfc41-295">Enne voo käitamist mobiilses seadmes veenduge, et ainult teie äsja loodud töö olek oleks *Avatud* lao *51* ja töökäsu tüübi *Müügitellimus* jaoks.</span><span class="sxs-lookup"><span data-stu-id="dfc41-295">Before you run the flow on the mobile device, make sure that only the work that you just created is in *Open* status for warehouse *51* and the *Sales order* work order type.</span></span> <span data-ttu-id="dfc41-296">Vastasel juhul võivad testi tulemused erineda, kuna süsteemi suunatud komplekteerimine sisaldab kõiki sobivaid töid.</span><span class="sxs-lookup"><span data-stu-id="dfc41-296">Otherwise, the results of the test might vary, because the system-direct picking will include all eligible work.</span></span>

1. <span data-ttu-id="dfc41-297">Avage jaotis **Laohaldus \> Töö \> Väljaminev \> Avatud müügitöö**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-297">Go to **Warehouse management \> Work \> Outbound \> Open sales work**.</span></span>
1. <span data-ttu-id="dfc41-298">Filtreerige ruudustiku **Avatud müügitöö** välja **Ladu** , et kuvatakse ainult lao *51* töö.</span><span class="sxs-lookup"><span data-stu-id="dfc41-298">In the **Open sales work** grid, filter on the **Warehouse** field so that only work for warehouse *51* is shown.</span></span>
1. <span data-ttu-id="dfc41-299">Kinnitage, et kuvatakse teie varasemalt loodud nelja töö ID-d.</span><span class="sxs-lookup"><span data-stu-id="dfc41-299">Confirm that only the four work IDs that you created earlier are shown.</span></span>
1. <span data-ttu-id="dfc41-300">Sulgege leht **Töö**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-300">Close the **Work** page.</span></span>

### <a name="mobile-device-flow-execution"></a><span data-ttu-id="dfc41-301">Mobiilse seadme voo käivitamine</span><span class="sxs-lookup"><span data-stu-id="dfc41-301">Mobile device flow execution</span></span>

<span data-ttu-id="dfc41-302">Vastavalt seadistusele esitab süsteem kasutajale tööd, mis on sorditud kõrgeimast töörea kogusest madalaimale.</span><span class="sxs-lookup"><span data-stu-id="dfc41-302">Based on the setup, the system will feed the user work that is sorted from the highest work line quantity to the lowest.</span></span> <span data-ttu-id="dfc41-303">Iga rea kogus on väiksem kui 20 ea.</span><span class="sxs-lookup"><span data-stu-id="dfc41-303">The quantity on every line will be less than 20 ea.</span></span>

<span data-ttu-id="dfc41-304">Pidage meeles, et see seadistus hõivab mis tahes töö, millel on vähemalt üks rida, kus kogus on väiksem kui 20 ea.</span><span class="sxs-lookup"><span data-stu-id="dfc41-304">Remember that this setup will capture any work that has at least one line where the quantity is less than 20 ea.</span></span> <span data-ttu-id="dfc41-305">Seega, kui töös on teine rida, kus kogus on täpselt 20 ea või enam, on see samuti kehtiv.</span><span class="sxs-lookup"><span data-stu-id="dfc41-305">Therefore, if the work has another line where the quantity is exactly 20 ea or more than 20 ea, it will also be valid.</span></span>

#### <a name="mobile-app"></a><span data-ttu-id="dfc41-306">Mobiilirakendus</span><span class="sxs-lookup"><span data-stu-id="dfc41-306">Mobile app</span></span>

1. <span data-ttu-id="dfc41-307">Logige ladustamise rakendusse lao *51* kasutajana sisse.</span><span class="sxs-lookup"><span data-stu-id="dfc41-307">Sign in to the warehousing app as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="dfc41-308">Avage jaotis **Väljaminev \> Müügi komplekteerimine – süsteem**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-308">Go to **Outbound \> Sales Picking - System**.</span></span>

    <span data-ttu-id="dfc41-309">Esitatakse töö ID *4* komplekteerimise etapp.</span><span class="sxs-lookup"><span data-stu-id="dfc41-309">The pick step for work ID *4* is presented.</span></span> <span data-ttu-id="dfc41-310">Kõigepealt esitatakse see töö ID selle süsteemi suunatud päringu seadistuse tõttu, kus te määrasite, et töö tuleks järjestada töörea kahaneva koguse põhjal.</span><span class="sxs-lookup"><span data-stu-id="dfc41-310">This work ID is presented first because of the setup of the system-directed query order, where you specified that work should be sequenced based on descending work line quantity.</span></span>

1. <span data-ttu-id="dfc41-311">Viige lõpule nõutav komplekteerimine ja ladustamine töö ID sulgemiseks.</span><span class="sxs-lookup"><span data-stu-id="dfc41-311">Complete the required pick and put to close the work ID.</span></span>

    <span data-ttu-id="dfc41-312">Järgmisena esitatakse töö ID *3*.</span><span class="sxs-lookup"><span data-stu-id="dfc41-312">Next, work ID *3* is presented.</span></span> <span data-ttu-id="dfc41-313">Üks selle töörida on järjekorras järgmine selle töörea koguse põhjal.</span><span class="sxs-lookup"><span data-stu-id="dfc41-313">One of its work lines is next in the sequence, based on the work line quantity.</span></span>

1. <span data-ttu-id="dfc41-314">Viige lõpule komplekteerimine ja ladustamine töö ID sulgemiseks.</span><span class="sxs-lookup"><span data-stu-id="dfc41-314">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="dfc41-315">Järgmisena esitatakse töö ID *2*.</span><span class="sxs-lookup"><span data-stu-id="dfc41-315">Next, work ID *2* is presented.</span></span> <span data-ttu-id="dfc41-316">Selle töö komplekteerimise rida on järjekorras järgmine.</span><span class="sxs-lookup"><span data-stu-id="dfc41-316">This work's pick line is next in the sequence.</span></span>

1. <span data-ttu-id="dfc41-317">Viige lõpule komplekteerimine ja ladustamine töö ID sulgemiseks.</span><span class="sxs-lookup"><span data-stu-id="dfc41-317">Complete the pick and put to close the work ID.</span></span>

    <span data-ttu-id="dfc41-318">Rohkem töid ei tohiks olla teile esitatud.</span><span class="sxs-lookup"><span data-stu-id="dfc41-318">No further work should be presented to you.</span></span> <span data-ttu-id="dfc41-319">Töö ID *1* pole selle mobiilse seadme menüü-üksuse jaoks sobilik, kuna päring määrab, et tööpäiseid käsitletakse ainult juhul, kui tööridade kogus on väiksem kui 20 ea.</span><span class="sxs-lookup"><span data-stu-id="dfc41-319">Work ID *1* isn't eligible for this mobile device menu item, because the query specifies that work headers are considered only if the quantity on the work lines is less than 20 ea.</span></span>

## <a name="tips"></a><span data-ttu-id="dfc41-320">Näpunäited</span><span class="sxs-lookup"><span data-stu-id="dfc41-320">Tips</span></span>

<span data-ttu-id="dfc41-321">Süsteemi suunatud tööde järjestuse päringud on *kaasa arvatud*.</span><span class="sxs-lookup"><span data-stu-id="dfc41-321">The system-directed work sequence queries are *inclusive*.</span></span> <span data-ttu-id="dfc41-322">Seda on oluline meeles pidada osade seadistuste puhul.</span><span class="sxs-lookup"><span data-stu-id="dfc41-322">It's important that you remember this fact for some setups.</span></span> <span data-ttu-id="dfc41-323">Kui soovite näiteks, et konkreetne menüü-üksus töötleks ainult tööd, kus tööüksus on *ea* ja määrate selle piirangu päringu vahekaardil **Vahemik**.</span><span class="sxs-lookup"><span data-stu-id="dfc41-323">For example, you want a specific menu item to process only work where the work unit is *ea* , and you specify that restriction on the **Range** tab of the query.</span></span> <span data-ttu-id="dfc41-324">Sellisel juhul esitatakse töötajale kõik tööd, kus vähemalt ühe töörea üksuseks on seatud *ea*.</span><span class="sxs-lookup"><span data-stu-id="dfc41-324">In this case, all work where at least one work line has the work unit set to *ea* will be fed to the worker.</span></span> <span data-ttu-id="dfc41-325">Seetõttu võib see töö sisaldada ka tööd, kus tööridadel on muu tööüksus kui *ea* (nt *kast* või *kaubaalus* ).</span><span class="sxs-lookup"><span data-stu-id="dfc41-325">Therefore, this work might also include work where work lines have a work unit other than *ea* (such as *box* or *pallet* ).</span></span> <span data-ttu-id="dfc41-326">Päring välistab ainult töö, kus ühelegi tööreale pole määratud tööühikuks *ea*.</span><span class="sxs-lookup"><span data-stu-id="dfc41-326">The query will exclude only work where no work line has the work unit set to *ea*.</span></span>

<span data-ttu-id="dfc41-327">Seetõttu hõivas päring selle stsenaariumi näites ka töö ID *4*.</span><span class="sxs-lookup"><span data-stu-id="dfc41-327">Therefore, in the example from this scenario, work ID *4* was also captured by the query.</span></span> <span data-ttu-id="dfc41-328">Selle loomise ajal lisati kaks rida: üks 25 ea kohta ja teine 10 ea kohta.</span><span class="sxs-lookup"><span data-stu-id="dfc41-328">When it was created, two lines were added: one for 25 ea and another for 10 ea.</span></span> <span data-ttu-id="dfc41-329">Töö esitati ikkagi kasutajale, sest vähemalt ühe töörea kogus on väiksem kui 20 ea.</span><span class="sxs-lookup"><span data-stu-id="dfc41-329">The work was still presented to the user, because at least one work line has a quantity of less than 20 ea.</span></span>

<span data-ttu-id="dfc41-330">Sõltuvalt stsenaariumist saate seda käitumist vältida tööpauside abil.</span><span class="sxs-lookup"><span data-stu-id="dfc41-330">Depending on the scenario, you can prevent this behavior by using work breaks.</span></span>
