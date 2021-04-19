---
title: Plaanitud ristlaadimine
description: Selles teemas kirjeldatakse täiustatud plaanitud ristlaadimist, kus tellimuse jaoks nõutav varude kogus suunatakse sissetulekust või loomisest otse õigesse väljaminevasse väljastus- või koondusalasse. Kõik järelejäänud sissetulevast allikast pärinevad varud suunatakse õigesse ladustamiskohta, kasutades tavalist ladustamise protsessi.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 49807c90c145eee55fae2d515fd19925eb2d944c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810410"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="f67d3-104">Plaanitud ristlaadimine</span><span class="sxs-lookup"><span data-stu-id="f67d3-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f67d3-105">Selles teemas kirjeldatakse täiustatud plaanitud ristlaadimist.</span><span class="sxs-lookup"><span data-stu-id="f67d3-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="f67d3-106">Ristlaadimine on laoprotsess, kus tellimuse jaoks nõutav varude kogus suunatakse sissetulekust või loomisest otse õigesse väljaminevasse väljastus- või koondusalasse.</span><span class="sxs-lookup"><span data-stu-id="f67d3-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="f67d3-107">Kõik järelejäänud sissetulevast allikast pärinevad varud suunatakse õigesse ladustamiskohta, kasutades tavalist ladustamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="f67d3-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="f67d3-108">Ristlaadimine võimaldab töötajatel jätta vahele juba väljaminevasse tellimusse märgitud varude sissetulevat ladustamist ja väljaminevat komplekteerimist.</span><span class="sxs-lookup"><span data-stu-id="f67d3-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="f67d3-109">Selle abil vähendatakse varude liigutamise kordade arvu, kus see on võimalik.</span><span class="sxs-lookup"><span data-stu-id="f67d3-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="f67d3-110">Lisaks, kuna süsteemiga suheldakse vähem, säästetakse rohkem lao kaupluse korrusel olevat aega ja ruumi.</span><span class="sxs-lookup"><span data-stu-id="f67d3-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="f67d3-111">Enne ristlaadimise käivitamist peab kasutaja konfigureerima uue ristlaadimise malli, kus on määratud ristlaadimise tarneallikas ja muud nõuete kogumid.</span><span class="sxs-lookup"><span data-stu-id="f67d3-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="f67d3-112">Kui väljaminev tellimus on loodud, tuleb rida tähistada sissetuleva tellimusega, mis sisaldab sama kaupa.</span><span class="sxs-lookup"><span data-stu-id="f67d3-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="f67d3-113">Sissetuleva tellimuse vastuvõtmise ajal tuvastab ristlaadimise seadistus automaatselt ristlaadimise vajaduse ning loob vajaliku koguse jaoks liikumise töö, mis põhineb asukohakorralduse seadistusel.</span><span class="sxs-lookup"><span data-stu-id="f67d3-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="f67d3-114">Lao kandeid **ei** jäeta registreerimata ristlaadimise tühistamisel, isegi kui selle võimaluse säte on laohalduse parameetrites sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="f67d3-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="f67d3-115">Plaanitud ristilaadimise funktsioonide sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="f67d3-115">Turn on the planned cross docking features</span></span>

<span data-ttu-id="f67d3-116">Kui teie süsteemis ei ole veel selles teemas kirjeldatud funktsioone, avage [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja lülitage järgmised funktsioonid järgmises järjekorras sisse.</span><span class="sxs-lookup"><span data-stu-id="f67d3-116">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="f67d3-117">*Plaanitud ristlaadimine*</span><span class="sxs-lookup"><span data-stu-id="f67d3-117">*Planned cross docking*</span></span>
2. <span data-ttu-id="f67d3-118">*Asukohadirektiividega ristiliaadimismallid*</span><span class="sxs-lookup"><span data-stu-id="f67d3-118">*Cross docking templates with location directives*</span></span>

## <a name="setup"></a><span data-ttu-id="f67d3-119">Seadistus</span><span class="sxs-lookup"><span data-stu-id="f67d3-119">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="f67d3-120">Koorma sisestamise meetodite uuesti loomine</span><span class="sxs-lookup"><span data-stu-id="f67d3-120">Regenerate load posting methods</span></span>

<span data-ttu-id="f67d3-121">Plaanitud ristlaadimine rakendatakse koormuse sisestamise meetodina.</span><span class="sxs-lookup"><span data-stu-id="f67d3-121">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="f67d3-122">Pärast funktsiooni sisselülitamist tuleb meetodid uuesti luua.</span><span class="sxs-lookup"><span data-stu-id="f67d3-122">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="f67d3-123">Avage jaotis **Laohaldus \> Seadistus \> Koormuse sisestamise meetodid**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-123">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="f67d3-124">Valige toimingupaanil suvand **Meetodite uuesti loomine**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-124">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="f67d3-125">Kui uuesti loomine on lõpule viidud, peaksite nägema meetodit, mille suvandi **Meetodi nimi** väärtus on *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="f67d3-125">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="f67d3-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f67d3-126">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="f67d3-127">Ristlaadimise malli loomine</span><span class="sxs-lookup"><span data-stu-id="f67d3-127">Create a cross-docking template</span></span>

1. <span data-ttu-id="f67d3-128">Avage **Laohaldus \> Seadistus \> Töö \> Ristlaadimismallid**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-128">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="f67d3-129">Malli loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-129">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="f67d3-130">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f67d3-130">In the header, set the following values:</span></span>

    - <span data-ttu-id="f67d3-131">**Järjestus:** *1*</span><span class="sxs-lookup"><span data-stu-id="f67d3-131">**Sequence:** *1*</span></span>

        <span data-ttu-id="f67d3-132">See väli määratleb mallide hindamise järjekorra.</span><span class="sxs-lookup"><span data-stu-id="f67d3-132">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="f67d3-133">**Ristlaadimismalli ID:** *51*</span><span class="sxs-lookup"><span data-stu-id="f67d3-133">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="f67d3-134">**Kirjeldus:** *Ladu 51*</span><span class="sxs-lookup"><span data-stu-id="f67d3-134">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="f67d3-135">**Nõudluse vabastamise poliitika:** *Enne tarne vastuvõtmist*</span><span class="sxs-lookup"><span data-stu-id="f67d3-135">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="f67d3-136">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="f67d3-136">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="f67d3-137">Kiirkaardi **Planeerimine** seadistus juhib kuidas mall töötab.</span><span class="sxs-lookup"><span data-stu-id="f67d3-137">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="f67d3-138">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f67d3-138">Set the following values:</span></span>

    - <span data-ttu-id="f67d3-139">**Nõudluse nõuded:** *Puudub*</span><span class="sxs-lookup"><span data-stu-id="f67d3-139">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="f67d3-140">See väli määratleb nõudluse varude nõuded.</span><span class="sxs-lookup"><span data-stu-id="f67d3-140">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="f67d3-141">Kui nõudlus peab olema seotud tarnega enne vabastamist, valige *Märkimine*.</span><span class="sxs-lookup"><span data-stu-id="f67d3-141">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="f67d3-142">Kui nõudmine tuleb enne vabastamist reserveerida vastavalt tellimusele, valige *Tellimuse reserveerimine*.</span><span class="sxs-lookup"><span data-stu-id="f67d3-142">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="f67d3-143">**Tüübi leidmine:** *Saadetise asukohad*</span><span class="sxs-lookup"><span data-stu-id="f67d3-143">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="f67d3-144">See väli määratleb, kas ristlaadimise töö peaks kasutama saadetise ajastamise/koormuse asukohti või kas see peaks kasutama asukohakorraldusi oma ajastamise/koormuse asukohtade leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="f67d3-144">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="f67d3-145">**Töömall:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="f67d3-145">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="f67d3-146">See väli määratleb töömalli, mida tuleks kasutada ristlaadimise töö loomisel.</span><span class="sxs-lookup"><span data-stu-id="f67d3-146">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="f67d3-147">**Uuesti kinnitamine tarne vastuvõtmisel:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="f67d3-147">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="f67d3-148">See suvand määratleb, kas tarnet tuleb vastuvõtmise ajal uuesti kinnitada.</span><span class="sxs-lookup"><span data-stu-id="f67d3-148">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="f67d3-149">Kui selle suvandi väärtuseks on seatud *Jah*, kontrollitakse nii maksimaalset ajavahemikku kui ka aegumiskuupäevade vahemikku.</span><span class="sxs-lookup"><span data-stu-id="f67d3-149">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="f67d3-150">**Korralduse kood** jätke see väli tühjaks</span><span class="sxs-lookup"><span data-stu-id="f67d3-150">**Directive code** Leave this field blank</span></span>

        <span data-ttu-id="f67d3-151">See valik võimaldab süsteemil kasutada asukohakorraldusi, et aidata määrata parim asukoht ristlaadimise varude teisaldamiseks.</span><span class="sxs-lookup"><span data-stu-id="f67d3-151">This option enables the system to use location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="f67d3-152">Selle seadistamiseks määrake igale asjakohasele ristlaadimise mallile korralduse kood.</span><span class="sxs-lookup"><span data-stu-id="f67d3-152">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="f67d3-153">Iga korralduse kood tähistab kordumatut asukohakorraldust.</span><span class="sxs-lookup"><span data-stu-id="f67d3-153">Each directive code identifies a unique location directive.</span></span>

    - <span data-ttu-id="f67d3-154">**Kinnita maksimaalne ajavahemik:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="f67d3-154">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="f67d3-155">See suvand määratleb, kas maksimaalset ajavahemikku tuleb hinnata tarneallika valimisel.</span><span class="sxs-lookup"><span data-stu-id="f67d3-155">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="f67d3-156">Kui selle suvandi väärtuseks on seatud *Jah*, siis muutuvad maksimaalse ja minimaalse ajavahemiku väljad kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="f67d3-156">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="f67d3-157">**Maksimaalne ajavahemik** *5*</span><span class="sxs-lookup"><span data-stu-id="f67d3-157">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="f67d3-158">See väli määratleb maksimaalse lubatud ajavahemiku, mis on lubatud tarne saabumise ja nõudluse väljamineku vahel.</span><span class="sxs-lookup"><span data-stu-id="f67d3-158">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="f67d3-159">**Maksimaalse ajavahemiku ühik:** *Päevad*</span><span class="sxs-lookup"><span data-stu-id="f67d3-159">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="f67d3-160">**Minimaalne ajavahemik:** *0*</span><span class="sxs-lookup"><span data-stu-id="f67d3-160">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="f67d3-161">See väli määratleb minimaalse lubatud ajavahemiku, mis on lubatud tarne saabumise ja nõudluse väljamineku vahel.</span><span class="sxs-lookup"><span data-stu-id="f67d3-161">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="f67d3-162">**Minimaalse ajavahemiku ühik:** *Päevad*</span><span class="sxs-lookup"><span data-stu-id="f67d3-162">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="f67d3-163">**Aegumiskuupäevade vahemik** *0*</span><span class="sxs-lookup"><span data-stu-id="f67d3-163">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="f67d3-164">*Esimesena aegunud esimesena välja (FEFO) kriteerium:* see väli määratleb maksimaalse päevade arvu, mis jääb praegu laos oleva partii esimesena aeguva aegumiskuupäeva ja vastuvõetava partii vahele.</span><span class="sxs-lookup"><span data-stu-id="f67d3-164">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="f67d3-165">Kiirkaardil **Tarneallikad** saate määrata selle malli jaoks kehtivad tarnetüübid.</span><span class="sxs-lookup"><span data-stu-id="f67d3-165">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="f67d3-166">Valige **Uus** ja seejärel seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f67d3-166">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="f67d3-167">**Järjekorranumber:** *1*</span><span class="sxs-lookup"><span data-stu-id="f67d3-167">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="f67d3-168">**Tarneallikas:** *Ostutellimus*</span><span class="sxs-lookup"><span data-stu-id="f67d3-168">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="f67d3-169">Tööklassi loomine</span><span class="sxs-lookup"><span data-stu-id="f67d3-169">Create a work class</span></span>

1. <span data-ttu-id="f67d3-170">Minge jaotisse **Laohaldus \> Seadistus \> Töö \> Töö klassid**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-170">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="f67d3-171">Tööklassi loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-171">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="f67d3-172">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f67d3-172">Set the following values:</span></span>

    - <span data-ttu-id="f67d3-173">**Töö klassi ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="f67d3-173">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="f67d3-174">**Kirjeldus:** *Ristlaadima*</span><span class="sxs-lookup"><span data-stu-id="f67d3-174">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="f67d3-175">**Töökäsu tüüp:** *Ristlaadimine*</span><span class="sxs-lookup"><span data-stu-id="f67d3-175">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="f67d3-176">Töömalli loomine</span><span class="sxs-lookup"><span data-stu-id="f67d3-176">Create a work template</span></span>

1. <span data-ttu-id="f67d3-177">Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-177">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="f67d3-178">Määrake välja **Töökäsu tüüp** väärtuseks *Ristlaadimine*.</span><span class="sxs-lookup"><span data-stu-id="f67d3-178">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="f67d3-179">Valige toimingupaanil suvand **Uus**, et lisada vahekaardile rida **Ülevaade**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-179">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="f67d3-180">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f67d3-180">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f67d3-181">**Järjekorranumber:** *1*</span><span class="sxs-lookup"><span data-stu-id="f67d3-181">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="f67d3-182">**Töömall:** *51 ristlaadimine*</span><span class="sxs-lookup"><span data-stu-id="f67d3-182">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="f67d3-183">**Töömalli kirjeldus:** *51 ristlaadimine*</span><span class="sxs-lookup"><span data-stu-id="f67d3-183">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="f67d3-184">Valige **Salvesta**, et muuta kiirkaart **Töömalli üksikasjad** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="f67d3-184">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="f67d3-185">Valige kiirkaardil **Töömalli üksikasjad** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="f67d3-185">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="f67d3-186">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f67d3-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f67d3-187">**Töö tüüp:** *Komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="f67d3-187">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="f67d3-188">**Töö klassi ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="f67d3-188">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="f67d3-189">Valige **Uus**, et lisada uus rida ja määrake sellele järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f67d3-189">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="f67d3-190">**Töö tüüp:** *Ladustamine*</span><span class="sxs-lookup"><span data-stu-id="f67d3-190">**Work type:** *Put*</span></span>
    - <span data-ttu-id="f67d3-191">**Töö klassi ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="f67d3-191">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="f67d3-192">Valige **Salvesta** ja kinnitage, et malli *51 ristlaadimine* on valitud märkeruut **Kehtiv**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-192">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="f67d3-193">Töötüübid *Komplekteerimine* ja *Ladustamine* peavad olema samad.</span><span class="sxs-lookup"><span data-stu-id="f67d3-193">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="f67d3-194">Asukohakorralduste loomine</span><span class="sxs-lookup"><span data-stu-id="f67d3-194">Create location directives</span></span>

1. <span data-ttu-id="f67d3-195">Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-195">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="f67d3-196">Määrake vasakpoolse paani välja **Töökäsu tüüp** suvandiks *Ristlaadimine*.</span><span class="sxs-lookup"><span data-stu-id="f67d3-196">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="f67d3-197">Valige toimingupaanil **Uus** ja seejärel seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f67d3-197">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="f67d3-198">**Järjekorranumber:** *1*</span><span class="sxs-lookup"><span data-stu-id="f67d3-198">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="f67d3-199">**Nimi:** *51 ladustamine ristlaadimisel*</span><span class="sxs-lookup"><span data-stu-id="f67d3-199">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="f67d3-200">**Töö tüüp:** *Ladustamine*</span><span class="sxs-lookup"><span data-stu-id="f67d3-200">**Work type:** *Put*</span></span>
    - <span data-ttu-id="f67d3-201">**Tegevuskoht:** *5*</span><span class="sxs-lookup"><span data-stu-id="f67d3-201">**Site:** *5*</span></span>
    - <span data-ttu-id="f67d3-202">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="f67d3-202">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="f67d3-203">Valige **Salvesta**, et muuta kiirkaart **Read** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="f67d3-203">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="f67d3-204">Valige kiirkaardil **Read** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="f67d3-204">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="f67d3-205">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f67d3-205">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f67d3-206">**Alates kogusest:** *1*</span><span class="sxs-lookup"><span data-stu-id="f67d3-206">**From quantity:** *1*</span></span>
    - <span data-ttu-id="f67d3-207">**Koguseni:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="f67d3-207">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="f67d3-208">Valige **Salvesta**, et muuta kiirkaart **Asukohakorralduse toimingud** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="f67d3-208">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="f67d3-209">Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="f67d3-209">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="f67d3-210">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f67d3-210">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f67d3-211">**Nimi:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="f67d3-211">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="f67d3-212">**Fikseeritud asukoha kasutus:** *Fikseeritud ja mittefikseeritud asukohad*</span><span class="sxs-lookup"><span data-stu-id="f67d3-212">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="f67d3-213">Valige **Salvesta**, et muuta tööriistariba **Asukohakorralduse toimingud** nupp **Päringu redigeerimine** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="f67d3-213">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="f67d3-214">Valige päringuredaktori avamiseks **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-214">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="f67d3-215">Veenduge vahekaardil **Vahemik**, et järgmised kaks rida oleksid konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="f67d3-215">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="f67d3-216">Rida 1:</span><span class="sxs-lookup"><span data-stu-id="f67d3-216">Line 1:</span></span>

        - <span data-ttu-id="f67d3-217">**Tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="f67d3-217">**Table:** *Locations*</span></span>
        - <span data-ttu-id="f67d3-218">**Tuletatud tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="f67d3-218">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="f67d3-219">**Väli:** *Ladu*</span><span class="sxs-lookup"><span data-stu-id="f67d3-219">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="f67d3-220">**Kriteeriumid:** *51*</span><span class="sxs-lookup"><span data-stu-id="f67d3-220">**Criteria:** *51*</span></span>

    - <span data-ttu-id="f67d3-221">Rida 2:</span><span class="sxs-lookup"><span data-stu-id="f67d3-221">Line 2:</span></span>

        - <span data-ttu-id="f67d3-222">**Tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="f67d3-222">**Table:** *Locations*</span></span>
        - <span data-ttu-id="f67d3-223">**Tuletatud tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="f67d3-223">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="f67d3-224">**Väli:** *Asukoht*</span><span class="sxs-lookup"><span data-stu-id="f67d3-224">**Field:** *Location*</span></span>
        - <span data-ttu-id="f67d3-225">**Kriteeriumid:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="f67d3-225">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="f67d3-226">Päringuredaktori sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-226">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="f67d3-227">Mobiilse seadme menüü-üksuse loomine</span><span class="sxs-lookup"><span data-stu-id="f67d3-227">Create a mobile device menu item</span></span>

1. <span data-ttu-id="f67d3-228">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-228">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="f67d3-229">Valige vasakpoolse paani menüü-üksuste loendist **Ostu ladustamine**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-229">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="f67d3-230">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-230">Select **Edit**.</span></span>
1. <span data-ttu-id="f67d3-231">Valige kiirkaardil **Tööklassid** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="f67d3-231">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="f67d3-232">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f67d3-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="f67d3-233">**Töö klassi ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="f67d3-233">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="f67d3-234">**Töökäsu tüüp:** *Ristlaadimine*</span><span class="sxs-lookup"><span data-stu-id="f67d3-234">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="f67d3-235">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-235">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="f67d3-236">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="f67d3-236">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="f67d3-237">Ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="f67d3-237">Create a purchase order</span></span>

<span data-ttu-id="f67d3-238">Järgige neid etappe ostutellimuse loomiseks tarneallikana.</span><span class="sxs-lookup"><span data-stu-id="f67d3-238">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="f67d3-239">Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-239">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="f67d3-240">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-240">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f67d3-241">Dialoogiboksis **Ostutellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f67d3-241">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="f67d3-242">**Hankija konto:** *104*</span><span class="sxs-lookup"><span data-stu-id="f67d3-242">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="f67d3-243">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="f67d3-243">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="f67d3-244">Valige **OK** ja märkige tellimuse number üles.</span><span class="sxs-lookup"><span data-stu-id="f67d3-244">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="f67d3-245">Kiirkaardile **Ostutellimuse read** lisatakse uus rida.</span><span class="sxs-lookup"><span data-stu-id="f67d3-245">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="f67d3-246">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f67d3-246">On this line, set the following values:</span></span>

    - <span data-ttu-id="f67d3-247">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="f67d3-247">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="f67d3-248">**Kogus:** *5*</span><span class="sxs-lookup"><span data-stu-id="f67d3-248">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="f67d3-249">Loo müügitellimus</span><span class="sxs-lookup"><span data-stu-id="f67d3-249">Create a sales order</span></span>

<span data-ttu-id="f67d3-250">Järgige neid etappe müügitellimuse loomiseks nõudluse allikana.</span><span class="sxs-lookup"><span data-stu-id="f67d3-250">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="f67d3-251">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-251">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="f67d3-252">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-252">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f67d3-253">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f67d3-253">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="f67d3-254">**Kliendi konto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="f67d3-254">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="f67d3-255">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="f67d3-255">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="f67d3-256">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-256">Select **OK**.</span></span>
1. <span data-ttu-id="f67d3-257">Kiirkaardile **Müügitellimuse read** lisatakse uus rida.</span><span class="sxs-lookup"><span data-stu-id="f67d3-257">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="f67d3-258">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f67d3-258">On this line, set the following values:</span></span>

    - <span data-ttu-id="f67d3-259">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="f67d3-259">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="f67d3-260">**Kogus:** *3*</span><span class="sxs-lookup"><span data-stu-id="f67d3-260">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="f67d3-261">Plaanitud ristlaadimise loomine</span><span class="sxs-lookup"><span data-stu-id="f67d3-261">Create planned cross-docking</span></span>

<span data-ttu-id="f67d3-262">Järgige neid etappe osturellimusest plaanitud ristlaadimise loomiseks.</span><span class="sxs-lookup"><span data-stu-id="f67d3-262">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="f67d3-263">Valige äsja loodud müügitellimuse lehe **Müügitellimuse üksikasjad** toimingupaani vahekaardil **Ladu** grupis **Toimingud** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-263">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="f67d3-264">Lattu vabastamine loob saadetise ja koormusrea müügitellimuse rea jaoks ning püüab eraldada varusid.</span><span class="sxs-lookup"><span data-stu-id="f67d3-264">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="f67d3-265">Teile kuvatakse teade.</span><span class="sxs-lookup"><span data-stu-id="f67d3-265">You receive an informational message.</span></span> <span data-ttu-id="f67d3-266">Kuvatakse ka järgmine hoiatusteade: „Voo XXXX jaoks ei loodud ühtegi tööd.</span><span class="sxs-lookup"><span data-stu-id="f67d3-266">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="f67d3-267">Lisateavet leiate töö loomise ajaloo logist.”</span><span class="sxs-lookup"><span data-stu-id="f67d3-267">See the work creation history log for details."</span></span> <span data-ttu-id="f67d3-268">Seda käitumist eeldatakse, kuna laos pole varusid.</span><span class="sxs-lookup"><span data-stu-id="f67d3-268">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="f67d3-269">Valige ruudustiku kohal oleva menüü **Ladu** kiirkaardilt **Müügitellimuse read** suvand **Saadetise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-269">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="f67d3-270">Kuvatakse leht **Saadetise üksikasjad**, mis kuvab müügirea jaoks loodud saadetise.</span><span class="sxs-lookup"><span data-stu-id="f67d3-270">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="f67d3-271">Pange tähele, et kiirkaardil **Koormusread** on välja **Plaanitud ristlaadimise kogus** väärtuseks seatud *3*.</span><span class="sxs-lookup"><span data-stu-id="f67d3-271">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="f67d3-272">Kuna laos polnud varusid saadaval, kuid kehtiv tarneallikas saabub ristlaadimismallis määratletud ajavahemikus, loodi ristlaadimise kogus.</span><span class="sxs-lookup"><span data-stu-id="f67d3-272">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="f67d3-273">Valige kiirkaardil **Koormusread** suvand **Plaanitud ristlaadimine**, et vaadata loodud ristlaadimise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="f67d3-273">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="f67d3-274">Ristlaadimise töötlemine</span><span class="sxs-lookup"><span data-stu-id="f67d3-274">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="f67d3-275">Ostutellimuse vastuvõtmine ladustamise mobiilirakendusega</span><span class="sxs-lookup"><span data-stu-id="f67d3-275">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="f67d3-276">Süsteem võtab ostutellimuselt vastu koguse 5 vastuvõtvasse asukohta ja loob kaks tööd.</span><span class="sxs-lookup"><span data-stu-id="f67d3-276">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="f67d3-277">Esimese loodud töö ID suvandi **Töötellimuse tüüp** väärtus on *Ristlaadimine* ja see on seotud müügitellimusega.</span><span class="sxs-lookup"><span data-stu-id="f67d3-277">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="f67d3-278">Selle kogus on 3 ja see suunatakse saatmise lõplikku saatmisasukohta, et seda saaks kohe välja saata.</span><span class="sxs-lookup"><span data-stu-id="f67d3-278">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="f67d3-279">Teine loodud töö ID suvandi **Töötellimuse tüüp** väärtus on *Ostutellimused* ja see on seotud ostutellimusega.</span><span class="sxs-lookup"><span data-stu-id="f67d3-279">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="f67d3-280">Sellel on järelejäänud kogus 2, mida ei ristlaaditud ja mis on suunatud lattu ladustamiseks.</span><span class="sxs-lookup"><span data-stu-id="f67d3-280">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="f67d3-281">Logige mobiilsesse seadmesse lao *51* kasutajana sisse.</span><span class="sxs-lookup"><span data-stu-id="f67d3-281">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="f67d3-282">Avage jaotis **Sissetulev \> Vastuvõetud ost**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-282">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="f67d3-283">Sisestage väljale **PONum** oma ostutellimuse number.</span><span class="sxs-lookup"><span data-stu-id="f67d3-283">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="f67d3-284">Sisestage väljale **Kogus** väärtus *5*.</span><span class="sxs-lookup"><span data-stu-id="f67d3-284">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="f67d3-285">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-285">Select **OK**.</span></span>
1. <span data-ttu-id="f67d3-286">Järgmisel lehel määrake välja **Kaup** väärtuseks *A0001*.</span><span class="sxs-lookup"><span data-stu-id="f67d3-286">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="f67d3-287">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-287">Select **OK**.</span></span>
1. <span data-ttu-id="f67d3-288">Kinnitage järgmisel lehel väärtused **PONum**, **Kaup** ja **Kogus**, valides **OK**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-288">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="f67d3-289">Teile kuvatakse teade „Töö lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="f67d3-289">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="f67d3-290">Väljumiseks valige **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-290">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="f67d3-291">Ristlaadimiseks ja hulgi ladustamine</span><span class="sxs-lookup"><span data-stu-id="f67d3-291">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="f67d3-292">Praegu on mõlemal töö ID-l sama sihtkoha identifitseerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="f67d3-292">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="f67d3-293">Järgmiste etappide lõpule viimiseks peate hankima töö ID ja sihtkoha identifitseerimisnumbri ID.</span><span class="sxs-lookup"><span data-stu-id="f67d3-293">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="f67d3-294">Selle teabe saate hankida ostutellimuse rea ja müügitellimuse rea töö üksikasjadest.</span><span class="sxs-lookup"><span data-stu-id="f67d3-294">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="f67d3-295">Saate minna ka jaotisse **Laohaldus \> Töö \> Töö üksikasjad** ja filtreerida töö jaoks, kus suvandi **Ladu** väärtus on *51*.</span><span class="sxs-lookup"><span data-stu-id="f67d3-295">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="f67d3-296">Avage mobiilsel seadmel **Sissetulev \> Ostude ladustamine** ja sisestage töö jaoks sihtidentifitseerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="f67d3-296">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="f67d3-297">Sisestage väljale **ID** töö üksikasjadest saadud sihtidentifitseerimisnumbri ID.</span><span class="sxs-lookup"><span data-stu-id="f67d3-297">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="f67d3-298">Lehel ristlaadimise komplekteerimine kuvatakse komplekteerimise asukoht (*RECV*), sihtidentifitseerimisnumber (*identifitseerimisnumber*), kaup (*A0001*) ja kogus (*3*).</span><span class="sxs-lookup"><span data-stu-id="f67d3-298">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="f67d3-299">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-299">Select **OK**.</span></span>
1. <span data-ttu-id="f67d3-300">Sisestage väljale **Siht-LP** sihtidentifitseerimisnumber selle identifitseerimisnumbri ID jaoks, mis tuleks ladustada (ristlaadida) saatmise asukohta.</span><span class="sxs-lookup"><span data-stu-id="f67d3-300">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="f67d3-301">Saate valida mis tahes soovitud identifitseerimisnumbri ID.</span><span class="sxs-lookup"><span data-stu-id="f67d3-301">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="f67d3-302">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-302">Select **OK**.</span></span>
1. <span data-ttu-id="f67d3-303">Sisestage järgmisel lehel väljale **ID** sihtidentifitseerimisnumbri ID.</span><span class="sxs-lookup"><span data-stu-id="f67d3-303">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="f67d3-304">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-304">Select **OK**.</span></span>
1. <span data-ttu-id="f67d3-305">Kinnitage töö järelejäänud koguse 2 komplekteerimiseks ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-305">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="f67d3-306">Järgmisel lehel valige **Valmis** komplekteerimise toimingu lõpetamiseks ja alustage ladustamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="f67d3-306">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="f67d3-307">Mobiilirakendus annab teile nende jaoks asukoha ja identifitseerimisnumbri.</span><span class="sxs-lookup"><span data-stu-id="f67d3-307">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="f67d3-308">Kinnitage hulgiladustamine **Ladustamine**, valides **OK**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-308">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="f67d3-309">Järgmisel lehel kinnitage ristlaadimine **Ladustamine**, valides **OK**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-309">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="f67d3-310">Teile kuvatakse teade „Töö lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="f67d3-310">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="f67d3-311">Väljumiseks valige **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="f67d3-311">Select **Cancel** to exit.</span></span>

<span data-ttu-id="f67d3-312">Järgmine illustratsioon näitab, kuidas lõpule viidud ristlaadimise tööd kuvatakse Microsoftis Dynamics 365 Supply Chain Managementis.</span><span class="sxs-lookup"><span data-stu-id="f67d3-312">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="f67d3-313">![Lõpule viidud ristlaadimise töö](media/PlannedCrossDockingWork.png "Lõpule viidud ristlaadimise töö")</span><span class="sxs-lookup"><span data-stu-id="f67d3-313">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]