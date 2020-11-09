---
title: Plaanitud ristlaadimine
description: Selles teemas kirjeldatakse täiustatud plaanitud ristlaadimist, kus tellimuse jaoks nõutav varude kogus suunatakse sissetulekust või loomisest otse õigesse väljaminevasse väljastus- või koondusalasse. Kõik järelejäänud sissetulevast allikast pärinevad varud suunatakse õigesse ladustamiskohta, kasutades tavalist ladustamise protsessi.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cc217f21a5fa70feb9ef9161f3ef2e2b6a333f35
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017755"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="04fc5-104">Plaanitud ristlaadimine</span><span class="sxs-lookup"><span data-stu-id="04fc5-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04fc5-105">Selles teemas kirjeldatakse täiustatud plaanitud ristlaadimist.</span><span class="sxs-lookup"><span data-stu-id="04fc5-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="04fc5-106">Ristlaadimine on laoprotsess, kus tellimuse jaoks nõutav varude kogus suunatakse sissetulekust või loomisest otse õigesse väljaminevasse väljastus- või koondusalasse.</span><span class="sxs-lookup"><span data-stu-id="04fc5-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="04fc5-107">Kõik järelejäänud sissetulevast allikast pärinevad varud suunatakse õigesse ladustamiskohta, kasutades tavalist ladustamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="04fc5-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="04fc5-108">Ristlaadimine võimaldab töötajatel jätta vahele juba väljaminevasse tellimusse märgitud varude sissetulevat ladustamist ja väljaminevat komplekteerimist.</span><span class="sxs-lookup"><span data-stu-id="04fc5-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="04fc5-109">Selle abil vähendatakse varude liigutamise kordade arvu, kus see on võimalik.</span><span class="sxs-lookup"><span data-stu-id="04fc5-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="04fc5-110">Lisaks, kuna süsteemiga suheldakse vähem, säästetakse rohkem lao kaupluse korrusel olevat aega ja ruumi.</span><span class="sxs-lookup"><span data-stu-id="04fc5-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="04fc5-111">Enne ristlaadimise käivitamist peab kasutaja konfigureerima uue ristlaadimise malli, kus on määratud ristlaadimise tarneallikas ja muud nõuete kogumid.</span><span class="sxs-lookup"><span data-stu-id="04fc5-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="04fc5-112">Kui väljaminev tellimus on loodud, tuleb rida tähistada sissetuleva tellimusega, mis sisaldab sama kaupa.</span><span class="sxs-lookup"><span data-stu-id="04fc5-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="04fc5-113">Sissetuleva tellimuse vastuvõtmise ajal tuvastab ristlaadimise seadistus automaatselt ristlaadimise vajaduse ning loob vajaliku koguse jaoks liikumise töö, mis põhineb asukohakorralduse seadistusel.</span><span class="sxs-lookup"><span data-stu-id="04fc5-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="04fc5-114">Lao kandeid **ei** jäeta registreerimata ristlaadimise tühistamisel, isegi kui selle võimaluse säte on laohalduse parameetrites sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="04fc5-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-feature"></a><span data-ttu-id="04fc5-115">Funktsiooni Plaanitud ristilaadimine sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="04fc5-115">Turn on the Planned cross docking feature</span></span>

<span data-ttu-id="04fc5-116">Enne täiustatud plaanitud ristlaadimise kasutamist, peate funktsiooni oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="04fc5-116">Before you can use advanced planned cross-docking, the feature must be turned on in your system.</span></span> <span data-ttu-id="04fc5-117">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="04fc5-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="04fc5-118">Seega on funktsioon loetletud järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="04fc5-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="04fc5-119">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="04fc5-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="04fc5-120">**Funktsiooni nimi** *Plaanitud ristilaadimine*</span><span class="sxs-lookup"><span data-stu-id="04fc5-120">**Feature name:** *Planned cross docking*</span></span>

## <a name="setup"></a><span data-ttu-id="04fc5-121">Häälestus</span><span class="sxs-lookup"><span data-stu-id="04fc5-121">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="04fc5-122">Koorma sisestamise meetodite uuesti loomine</span><span class="sxs-lookup"><span data-stu-id="04fc5-122">Regenerate load posting methods</span></span>

<span data-ttu-id="04fc5-123">Plaanitud ristlaadimine rakendatakse koormuse sisestamise meetodina.</span><span class="sxs-lookup"><span data-stu-id="04fc5-123">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="04fc5-124">Pärast funktsiooni sisselülitamist tuleb meetodid uuesti luua.</span><span class="sxs-lookup"><span data-stu-id="04fc5-124">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="04fc5-125">Avage jaotis **Laohaldus \> Seadistus \> Koormuse sisestamise meetodid**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-125">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="04fc5-126">Valige toimingupaanil suvand **Meetodite uuesti loomine**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-126">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="04fc5-127">Kui uuesti loomine on lõpule viidud, peaksite nägema meetodit, mille suvandi **Meetodi nimi** väärtus on *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="04fc5-127">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="04fc5-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="04fc5-128">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="04fc5-129">Ristlaadimise malli loomine</span><span class="sxs-lookup"><span data-stu-id="04fc5-129">Create a cross-docking template</span></span>

1. <span data-ttu-id="04fc5-130">Avage **Laohaldus \> Seadistus \> Töö \> Ristlaadimismallid**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-130">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="04fc5-131">Malli loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-131">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="04fc5-132">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="04fc5-132">In the header, set the following values:</span></span>

    - <span data-ttu-id="04fc5-133">**Järjestus:** *1*</span><span class="sxs-lookup"><span data-stu-id="04fc5-133">**Sequence:** *1*</span></span>

        <span data-ttu-id="04fc5-134">See väli määratleb mallide hindamise järjekorra.</span><span class="sxs-lookup"><span data-stu-id="04fc5-134">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="04fc5-135">**Ristlaadimismalli ID:** *51*</span><span class="sxs-lookup"><span data-stu-id="04fc5-135">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="04fc5-136">**Kirjeldus:** *Ladu 51*</span><span class="sxs-lookup"><span data-stu-id="04fc5-136">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="04fc5-137">**Nõudluse vabastamise poliitika:** *Enne tarne vastuvõtmist*</span><span class="sxs-lookup"><span data-stu-id="04fc5-137">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="04fc5-138">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="04fc5-138">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="04fc5-139">Kiirkaardi **Planeerimine** seadistus juhib kuidas mall töötab.</span><span class="sxs-lookup"><span data-stu-id="04fc5-139">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="04fc5-140">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="04fc5-140">Set the following values:</span></span>

    - <span data-ttu-id="04fc5-141">**Nõudluse nõuded:** *Puudub*</span><span class="sxs-lookup"><span data-stu-id="04fc5-141">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="04fc5-142">See väli määratleb nõudluse varude nõuded.</span><span class="sxs-lookup"><span data-stu-id="04fc5-142">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="04fc5-143">Kui nõudlus peab olema seotud tarnega enne vabastamist, valige *Märkimine*.</span><span class="sxs-lookup"><span data-stu-id="04fc5-143">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="04fc5-144">Kui nõudmine tuleb enne vabastamist reserveerida vastavalt tellimusele, valige *Tellimuse reserveerimine*.</span><span class="sxs-lookup"><span data-stu-id="04fc5-144">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="04fc5-145">**Tüübi leidmine:** *Saadetise asukohad*</span><span class="sxs-lookup"><span data-stu-id="04fc5-145">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="04fc5-146">See väli määratleb, kas ristlaadimise töö peaks kasutama saadetise ajastamise/koormuse asukohti või kas see peaks kasutama asukohakorraldusi oma ajastamise/koormuse asukohtade leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="04fc5-146">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="04fc5-147">**Töömall:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="04fc5-147">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="04fc5-148">See väli määratleb töömalli, mida tuleks kasutada ristlaadimise töö loomisel.</span><span class="sxs-lookup"><span data-stu-id="04fc5-148">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="04fc5-149">**Uuesti kinnitamine tarne vastuvõtmisel:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="04fc5-149">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="04fc5-150">See suvand määratleb, kas tarnet tuleb vastuvõtmise ajal uuesti kinnitada.</span><span class="sxs-lookup"><span data-stu-id="04fc5-150">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="04fc5-151">Kui selle suvandi väärtuseks on seatud *Jah* , kontrollitakse nii maksimaalset ajavahemikku kui ka aegumiskuupäevade vahemikku.</span><span class="sxs-lookup"><span data-stu-id="04fc5-151">If this option is set to *Yes* , both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="04fc5-152">**Kinnita maksimaalne ajavahemik:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="04fc5-152">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="04fc5-153">See suvand määratleb, kas maksimaalset ajavahemikku tuleb hinnata tarneallika valimisel.</span><span class="sxs-lookup"><span data-stu-id="04fc5-153">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="04fc5-154">Kui selle suvandi väärtuseks on seatud *Jah* , siis muutuvad maksimaalse ja minimaalse ajavahemiku väljad kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="04fc5-154">If this option is set to *Yes* , the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="04fc5-155">**Maksimaalne ajavahemik** *5*</span><span class="sxs-lookup"><span data-stu-id="04fc5-155">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="04fc5-156">See väli määratleb maksimaalse lubatud ajavahemiku, mis on lubatud tarne saabumise ja nõudluse väljamineku vahel.</span><span class="sxs-lookup"><span data-stu-id="04fc5-156">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="04fc5-157">**Maksimaalse ajavahemiku ühik:** *Päevad*</span><span class="sxs-lookup"><span data-stu-id="04fc5-157">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="04fc5-158">**Minimaalne ajavahemik:** *0*</span><span class="sxs-lookup"><span data-stu-id="04fc5-158">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="04fc5-159">See väli määratleb minimaalse lubatud ajavahemiku, mis on lubatud tarne saabumise ja nõudluse väljamineku vahel.</span><span class="sxs-lookup"><span data-stu-id="04fc5-159">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="04fc5-160">**Minimaalse ajavahemiku ühik:** *Päevad*</span><span class="sxs-lookup"><span data-stu-id="04fc5-160">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="04fc5-161">**Aegumiskuupäevade vahemik** *0*</span><span class="sxs-lookup"><span data-stu-id="04fc5-161">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="04fc5-162">*Esimesena aegunud esimesena välja (FEFO) kriteerium:* see väli määratleb maksimaalse päevade arvu, mis jääb praegu laos oleva partii esimesena aeguva aegumiskuupäeva ja vastuvõetava partii vahele.</span><span class="sxs-lookup"><span data-stu-id="04fc5-162">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="04fc5-163">Kiirkaardil **Tarneallikad** saate määrata selle malli jaoks kehtivad tarnetüübid.</span><span class="sxs-lookup"><span data-stu-id="04fc5-163">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="04fc5-164">Valige **Uus** ja seejärel seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="04fc5-164">Select **New** , and then set the following values:</span></span>

    - <span data-ttu-id="04fc5-165">**Järjekorranumber:** *1*</span><span class="sxs-lookup"><span data-stu-id="04fc5-165">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="04fc5-166">**Tarneallikas:** *Ostutellimus*</span><span class="sxs-lookup"><span data-stu-id="04fc5-166">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="04fc5-167">Tööklassi loomine</span><span class="sxs-lookup"><span data-stu-id="04fc5-167">Create a work class</span></span>

1. <span data-ttu-id="04fc5-168">Minge jaotisse **Laohaldus \> Seadistus \> Töö \> Töö klassid**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-168">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="04fc5-169">Tööklassi loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-169">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="04fc5-170">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="04fc5-170">Set the following values:</span></span>

    - <span data-ttu-id="04fc5-171">**Töö klassi ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="04fc5-171">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="04fc5-172">**Kirjeldus:** *Ristlaadima*</span><span class="sxs-lookup"><span data-stu-id="04fc5-172">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="04fc5-173">**Töökäsu tüüp:** *Ristlaadimine*</span><span class="sxs-lookup"><span data-stu-id="04fc5-173">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="04fc5-174">Töömalli loomine</span><span class="sxs-lookup"><span data-stu-id="04fc5-174">Create a work template</span></span>

1. <span data-ttu-id="04fc5-175">Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-175">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="04fc5-176">Määrake välja **Töökäsu tüüp** väärtuseks *Ristlaadimine*.</span><span class="sxs-lookup"><span data-stu-id="04fc5-176">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="04fc5-177">Valige toimingupaanil suvand **Uus** , et lisada vahekaardile rida **Ülevaade**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-177">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="04fc5-178">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="04fc5-178">On the new line, set the following values:</span></span>

    - <span data-ttu-id="04fc5-179">**Järjekorranumber:** *1*</span><span class="sxs-lookup"><span data-stu-id="04fc5-179">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="04fc5-180">**Töömall:** *51 ristlaadimine*</span><span class="sxs-lookup"><span data-stu-id="04fc5-180">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="04fc5-181">**Töömalli kirjeldus:** *51 ristlaadimine*</span><span class="sxs-lookup"><span data-stu-id="04fc5-181">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="04fc5-182">Valige **Salvesta** , et muuta kiirkaart **Töömalli üksikasjad** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="04fc5-182">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="04fc5-183">Valige kiirkaardil **Töömalli üksikasjad** suvand **Uus** , et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="04fc5-183">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="04fc5-184">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="04fc5-184">On the new line, set the following values:</span></span>

    - <span data-ttu-id="04fc5-185">**Töö tüüp:** *Komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="04fc5-185">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="04fc5-186">**Töö klassi ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="04fc5-186">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="04fc5-187">Valige **Uus** , et lisada uus rida ja määrake sellele järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="04fc5-187">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="04fc5-188">**Töö tüüp:** *Ladustamine*</span><span class="sxs-lookup"><span data-stu-id="04fc5-188">**Work type:** *Put*</span></span>
    - <span data-ttu-id="04fc5-189">**Töö klassi ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="04fc5-189">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="04fc5-190">Valige **Salvesta** ja kinnitage, et malli *51 ristlaadimine* on valitud märkeruut **Kehtiv**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-190">Select **Save** , and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="04fc5-191">Töötüübid *Komplekteerimine* ja *Ladustamine* peavad olema samad.</span><span class="sxs-lookup"><span data-stu-id="04fc5-191">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="04fc5-192">Asukohakorralduste loomine</span><span class="sxs-lookup"><span data-stu-id="04fc5-192">Create location directives</span></span>

1. <span data-ttu-id="04fc5-193">Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-193">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="04fc5-194">Määrake vasakpoolse paani välja **Töökäsu tüüp** suvandiks *Ristlaadimine*.</span><span class="sxs-lookup"><span data-stu-id="04fc5-194">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="04fc5-195">Valige toimingupaanil **Uus** ja seejärel seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="04fc5-195">On the Action Pane, select **New** , and set the following values:</span></span>

    - <span data-ttu-id="04fc5-196">**Järjekorranumber:** *1*</span><span class="sxs-lookup"><span data-stu-id="04fc5-196">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="04fc5-197">**Nimi:** *51 ladustamine ristlaadimisel*</span><span class="sxs-lookup"><span data-stu-id="04fc5-197">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="04fc5-198">**Töö tüüp:** *Ladustamine*</span><span class="sxs-lookup"><span data-stu-id="04fc5-198">**Work type:** *Put*</span></span>
    - <span data-ttu-id="04fc5-199">**Tegevuskoht:** *5*</span><span class="sxs-lookup"><span data-stu-id="04fc5-199">**Site:** *5*</span></span>
    - <span data-ttu-id="04fc5-200">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="04fc5-200">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="04fc5-201">Valige **Salvesta** , et muuta kiirkaart **Read** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="04fc5-201">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="04fc5-202">Valige kiirkaardil **Read** suvand **Uus** , et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="04fc5-202">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="04fc5-203">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="04fc5-203">On the new line, set the following values:</span></span>

    - <span data-ttu-id="04fc5-204">**Alates kogusest:** *1*</span><span class="sxs-lookup"><span data-stu-id="04fc5-204">**From quantity:** *1*</span></span>
    - <span data-ttu-id="04fc5-205">**Koguseni:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="04fc5-205">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="04fc5-206">Valige **Salvesta** , et muuta kiirkaart **Asukohakorralduse toimingud** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="04fc5-206">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="04fc5-207">Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus** , et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="04fc5-207">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="04fc5-208">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="04fc5-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="04fc5-209">**Nimi:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="04fc5-209">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="04fc5-210">**Fikseeritud asukoha kasutus:** *Fikseeritud ja mittefikseeritud asukohad*</span><span class="sxs-lookup"><span data-stu-id="04fc5-210">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="04fc5-211">Valige **Salvesta** , et muuta tööriistariba **Asukohakorralduse toimingud** nupp **Päringu redigeerimine** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="04fc5-211">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="04fc5-212">Valige päringuredaktori avamiseks **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-212">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="04fc5-213">Veenduge vahekaardil **Vahemik** , et järgmised kaks rida oleksid konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="04fc5-213">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="04fc5-214">Rida 1:</span><span class="sxs-lookup"><span data-stu-id="04fc5-214">Line 1:</span></span>

        - <span data-ttu-id="04fc5-215">**Tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="04fc5-215">**Table:** *Locations*</span></span>
        - <span data-ttu-id="04fc5-216">**Tuletatud tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="04fc5-216">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="04fc5-217">**Väli:** *Ladu*</span><span class="sxs-lookup"><span data-stu-id="04fc5-217">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="04fc5-218">**Kriteeriumid:** *51*</span><span class="sxs-lookup"><span data-stu-id="04fc5-218">**Criteria:** *51*</span></span>

    - <span data-ttu-id="04fc5-219">Rida 2:</span><span class="sxs-lookup"><span data-stu-id="04fc5-219">Line 2:</span></span>

        - <span data-ttu-id="04fc5-220">**Tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="04fc5-220">**Table:** *Locations*</span></span>
        - <span data-ttu-id="04fc5-221">**Tuletatud tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="04fc5-221">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="04fc5-222">**Väli:** *Asukoht*</span><span class="sxs-lookup"><span data-stu-id="04fc5-222">**Field:** *Location*</span></span>
        - <span data-ttu-id="04fc5-223">**Kriteeriumid:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="04fc5-223">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="04fc5-224">Päringuredaktori sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-224">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="04fc5-225">Mobiilse seadme menüü-üksuse loomine</span><span class="sxs-lookup"><span data-stu-id="04fc5-225">Create a mobile device menu item</span></span>

1. <span data-ttu-id="04fc5-226">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-226">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="04fc5-227">Valige vasakpoolse paani menüü-üksuste loendist **Ostu ladustamine**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-227">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="04fc5-228">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-228">Select **Edit**.</span></span>
1. <span data-ttu-id="04fc5-229">Valige kiirkaardil **Tööklassid** suvand **Uus** , et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="04fc5-229">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="04fc5-230">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="04fc5-230">On the new line, set the following values:</span></span>

    - <span data-ttu-id="04fc5-231">**Töö klassi ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="04fc5-231">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="04fc5-232">**Töökäsu tüüp:** *Ristlaadimine*</span><span class="sxs-lookup"><span data-stu-id="04fc5-232">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="04fc5-233">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-233">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="04fc5-234">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="04fc5-234">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="04fc5-235">Ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="04fc5-235">Create a purchase order</span></span>

<span data-ttu-id="04fc5-236">Järgige neid etappe ostutellimuse loomiseks tarneallikana.</span><span class="sxs-lookup"><span data-stu-id="04fc5-236">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="04fc5-237">Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-237">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="04fc5-238">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-238">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="04fc5-239">Dialoogiboksis **Ostutellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="04fc5-239">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="04fc5-240">**Hankija konto:** *104*</span><span class="sxs-lookup"><span data-stu-id="04fc5-240">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="04fc5-241">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="04fc5-241">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="04fc5-242">Valige **OK** ja märkige tellimuse number üles.</span><span class="sxs-lookup"><span data-stu-id="04fc5-242">Select **OK** , and make a note of the order number.</span></span>
1. <span data-ttu-id="04fc5-243">Kiirkaardile **Ostutellimuse read** lisatakse uus rida.</span><span class="sxs-lookup"><span data-stu-id="04fc5-243">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="04fc5-244">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="04fc5-244">On this line, set the following values:</span></span>

    - <span data-ttu-id="04fc5-245">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="04fc5-245">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="04fc5-246">**Kogus:** *5*</span><span class="sxs-lookup"><span data-stu-id="04fc5-246">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="04fc5-247">Loo müügitellimus</span><span class="sxs-lookup"><span data-stu-id="04fc5-247">Create a sales order</span></span>

<span data-ttu-id="04fc5-248">Järgige neid etappe müügitellimuse loomiseks nõudluse allikana.</span><span class="sxs-lookup"><span data-stu-id="04fc5-248">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="04fc5-249">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-249">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="04fc5-250">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-250">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="04fc5-251">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="04fc5-251">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="04fc5-252">**Kliendi konto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="04fc5-252">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="04fc5-253">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="04fc5-253">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="04fc5-254">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-254">Select **OK**.</span></span>
1. <span data-ttu-id="04fc5-255">Kiirkaardile **Müügitellimuse read** lisatakse uus rida.</span><span class="sxs-lookup"><span data-stu-id="04fc5-255">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="04fc5-256">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="04fc5-256">On this line, set the following values:</span></span>

    - <span data-ttu-id="04fc5-257">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="04fc5-257">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="04fc5-258">**Kogus:** *3*</span><span class="sxs-lookup"><span data-stu-id="04fc5-258">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="04fc5-259">Plaanitud ristlaadimise loomine</span><span class="sxs-lookup"><span data-stu-id="04fc5-259">Create planned cross-docking</span></span>

<span data-ttu-id="04fc5-260">Järgige neid etappe osturellimusest plaanitud ristlaadimise loomiseks.</span><span class="sxs-lookup"><span data-stu-id="04fc5-260">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="04fc5-261">Valige äsja loodud müügitellimuse lehe **Müügitellimuse üksikasjad** toimingupaani vahekaardil **Ladu** grupis **Toimingud** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-261">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="04fc5-262">Lattu vabastamine loob saadetise ja koormusrea müügitellimuse rea jaoks ning püüab eraldada varusid.</span><span class="sxs-lookup"><span data-stu-id="04fc5-262">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="04fc5-263">Teile kuvatakse teade.</span><span class="sxs-lookup"><span data-stu-id="04fc5-263">You receive an informational message.</span></span> <span data-ttu-id="04fc5-264">Kuvatakse ka järgmine hoiatusteade: „Voo XXXX jaoks ei loodud ühtegi tööd.</span><span class="sxs-lookup"><span data-stu-id="04fc5-264">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="04fc5-265">Lisateavet leiate töö loomise ajaloo logist.”</span><span class="sxs-lookup"><span data-stu-id="04fc5-265">See the work creation history log for details."</span></span> <span data-ttu-id="04fc5-266">Seda käitumist eeldatakse, kuna laos pole varusid.</span><span class="sxs-lookup"><span data-stu-id="04fc5-266">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="04fc5-267">Valige ruudustiku kohal oleva menüü **Ladu** kiirkaardilt **Müügitellimuse read** suvand **Saadetise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-267">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="04fc5-268">Kuvatakse leht **Saadetise üksikasjad** , mis kuvab müügirea jaoks loodud saadetise.</span><span class="sxs-lookup"><span data-stu-id="04fc5-268">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="04fc5-269">Pange tähele, et kiirkaardil **Koormusread** on välja **Plaanitud ristlaadimise kogus** väärtuseks seatud *3*.</span><span class="sxs-lookup"><span data-stu-id="04fc5-269">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="04fc5-270">Kuna laos polnud varusid saadaval, kuid kehtiv tarneallikas saabub ristlaadimismallis määratletud ajavahemikus, loodi ristlaadimise kogus.</span><span class="sxs-lookup"><span data-stu-id="04fc5-270">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="04fc5-271">Valige kiirkaardil **Koormusread** suvand **Plaanitud ristlaadimine** , et vaadata loodud ristlaadimise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="04fc5-271">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="04fc5-272">Ristlaadimise töötlemine</span><span class="sxs-lookup"><span data-stu-id="04fc5-272">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="04fc5-273">Ostutellimuse vastuvõtmine ladustamise mobiilirakendusega</span><span class="sxs-lookup"><span data-stu-id="04fc5-273">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="04fc5-274">Süsteem võtab ostutellimuselt vastu koguse 5 vastuvõtvasse asukohta ja loob kaks tööd.</span><span class="sxs-lookup"><span data-stu-id="04fc5-274">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="04fc5-275">Esimese loodud töö ID suvandi **Töötellimuse tüüp** väärtus on *Ristlaadimine* ja see on seotud müügitellimusega.</span><span class="sxs-lookup"><span data-stu-id="04fc5-275">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="04fc5-276">Selle kogus on 3 ja see suunatakse saatmise lõplikku saatmisasukohta, et seda saaks kohe välja saata.</span><span class="sxs-lookup"><span data-stu-id="04fc5-276">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="04fc5-277">Teine loodud töö ID suvandi **Töötellimuse tüüp** väärtus on *Ostutellimused* ja see on seotud ostutellimusega.</span><span class="sxs-lookup"><span data-stu-id="04fc5-277">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="04fc5-278">Sellel on järelejäänud kogus 2, mida ei ristlaaditud ja mis on suunatud lattu ladustamiseks.</span><span class="sxs-lookup"><span data-stu-id="04fc5-278">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="04fc5-279">Logige mobiilsesse seadmesse lao *51* kasutajana sisse.</span><span class="sxs-lookup"><span data-stu-id="04fc5-279">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="04fc5-280">Avage jaotis **Sissetulev \> Vastuvõetud ost**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-280">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="04fc5-281">Sisestage väljale **PONum** oma ostutellimuse number.</span><span class="sxs-lookup"><span data-stu-id="04fc5-281">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="04fc5-282">Sisestage väljale **Kogus** väärtus *5*.</span><span class="sxs-lookup"><span data-stu-id="04fc5-282">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="04fc5-283">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-283">Select **OK**.</span></span>
1. <span data-ttu-id="04fc5-284">Järgmisel lehel määrake välja **Kaup** väärtuseks *A0001*.</span><span class="sxs-lookup"><span data-stu-id="04fc5-284">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="04fc5-285">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-285">Select **OK**.</span></span>
1. <span data-ttu-id="04fc5-286">Kinnitage järgmisel lehel väärtused **PONum** , **Kaup** ja **Kogus** , valides **OK**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-286">On the next page, confirm the **PONum** , **Item** , and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="04fc5-287">Teile kuvatakse teade „Töö lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="04fc5-287">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="04fc5-288">Väljumiseks valige **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-288">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="04fc5-289">Ristlaadimiseks ja hulgi ladustamine</span><span class="sxs-lookup"><span data-stu-id="04fc5-289">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="04fc5-290">Praegu on mõlemal töö ID-l sama sihtkoha identifitseerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="04fc5-290">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="04fc5-291">Järgmiste etappide lõpule viimiseks peate hankima töö ID ja sihtkoha identifitseerimisnumbri ID.</span><span class="sxs-lookup"><span data-stu-id="04fc5-291">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="04fc5-292">Selle teabe saate hankida ostutellimuse rea ja müügitellimuse rea töö üksikasjadest.</span><span class="sxs-lookup"><span data-stu-id="04fc5-292">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="04fc5-293">Saate minna ka jaotisse **Laohaldus \> Töö \> Töö üksikasjad** ja filtreerida töö jaoks, kus suvandi **Ladu** väärtus on *51*.</span><span class="sxs-lookup"><span data-stu-id="04fc5-293">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="04fc5-294">Avage mobiilsel seadmel **Sissetulev \> Ostude ladustamine** ja sisestage töö jaoks sihtidentifitseerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="04fc5-294">On the mobile device, go to **Inbound \> Purchase put-away** , and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="04fc5-295">Sisestage väljale **ID** töö üksikasjadest saadud sihtidentifitseerimisnumbri ID.</span><span class="sxs-lookup"><span data-stu-id="04fc5-295">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="04fc5-296">Lehel ristlaadimise komplekteerimine kuvatakse komplekteerimise asukoht ( *RECV* ), sihtidentifitseerimisnumber ( *identifitseerimisnumber* ), kaup ( *A0001* ) ja kogus ( *3* ).</span><span class="sxs-lookup"><span data-stu-id="04fc5-296">The cross-docking pick page shows the picking location ( *RECV* ), target license plate ( *license plate* ), item ( *A0001* ), and quantity ( *3* ).</span></span>

1. <span data-ttu-id="04fc5-297">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-297">Select **OK**.</span></span>
1. <span data-ttu-id="04fc5-298">Sisestage väljale **Siht-LP** sihtidentifitseerimisnumber selle identifitseerimisnumbri ID jaoks, mis tuleks ladustada (ristlaadida) saatmise asukohta.</span><span class="sxs-lookup"><span data-stu-id="04fc5-298">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="04fc5-299">Saate valida mis tahes soovitud identifitseerimisnumbri ID.</span><span class="sxs-lookup"><span data-stu-id="04fc5-299">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="04fc5-300">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-300">Select **OK**.</span></span>
1. <span data-ttu-id="04fc5-301">Sisestage järgmisel lehel väljale **ID** sihtidentifitseerimisnumbri ID.</span><span class="sxs-lookup"><span data-stu-id="04fc5-301">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="04fc5-302">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-302">Select **OK**.</span></span>
1. <span data-ttu-id="04fc5-303">Kinnitage töö järelejäänud koguse 2 komplekteerimiseks ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-303">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="04fc5-304">Järgmisel lehel valige **Valmis** komplekteerimise toimingu lõpetamiseks ja alustage ladustamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="04fc5-304">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="04fc5-305">Mobiilirakendus annab teile nende jaoks asukoha ja identifitseerimisnumbri.</span><span class="sxs-lookup"><span data-stu-id="04fc5-305">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="04fc5-306">Kinnitage hulgiladustamine **Ladustamine** , valides **OK**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-306">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="04fc5-307">Järgmisel lehel kinnitage ristlaadimine **Ladustamine** , valides **OK**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-307">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="04fc5-308">Teile kuvatakse teade „Töö lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="04fc5-308">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="04fc5-309">Väljumiseks valige **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="04fc5-309">Select **Cancel** to exit.</span></span>

<span data-ttu-id="04fc5-310">Järgmine illustratsioon näitab, kuidas lõpule viidud ristlaadimise tööd kuvatakse Microsoftis Dynamics 365 Supply Chain Managementis.</span><span class="sxs-lookup"><span data-stu-id="04fc5-310">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="04fc5-311">![Lõpule viidud ristlaadimise töö](media/PlannedCrossDockingWork.png "Lõpule viidud ristlaadimise töö")</span><span class="sxs-lookup"><span data-stu-id="04fc5-311">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>
