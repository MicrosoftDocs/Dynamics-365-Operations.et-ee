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
ms.openlocfilehash: 11e044e04e05c68af676bf97e6085e9975da5c1d
ms.sourcegitcommit: bef7bd2aac00d7eb837fd275d383b7a5c3f1c1ee
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/19/2021
ms.locfileid: "5911244"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="a7467-104">Plaanitud ristlaadimine</span><span class="sxs-lookup"><span data-stu-id="a7467-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7467-105">Selles teemas kirjeldatakse täiustatud plaanitud ristlaadimist.</span><span class="sxs-lookup"><span data-stu-id="a7467-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="a7467-106">Ristlaadimine on laoprotsess, kus tellimuse jaoks nõutav varude kogus suunatakse sissetulekust või loomisest otse õigesse väljaminevasse väljastus- või koondusalasse.</span><span class="sxs-lookup"><span data-stu-id="a7467-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="a7467-107">Kõik järelejäänud sissetulevast allikast pärinevad varud suunatakse õigesse ladustamiskohta, kasutades tavalist ladustamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="a7467-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="a7467-108">Ristlaadimine võimaldab töötajatel jätta vahele juba väljaminevasse tellimusse märgitud varude sissetulevat ladustamist ja väljaminevat komplekteerimist.</span><span class="sxs-lookup"><span data-stu-id="a7467-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="a7467-109">Selle abil vähendatakse varude liigutamise kordade arvu, kus see on võimalik.</span><span class="sxs-lookup"><span data-stu-id="a7467-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="a7467-110">Lisaks, kuna süsteemiga suheldakse vähem, säästetakse rohkem lao kaupluse korrusel olevat aega ja ruumi.</span><span class="sxs-lookup"><span data-stu-id="a7467-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="a7467-111">Enne ristlaadimise käivitamist peate konfigureerima uue ristlaadimise malli, kus on määratud ristlaadimise tarneallikas ja muud nõuete kogumid.</span><span class="sxs-lookup"><span data-stu-id="a7467-111">Before you can run cross-docking, you must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="a7467-112">Kui väljaminev tellimus on loodud, tuleb rida tähistada sissetuleva tellimusega, mis sisaldab sama kaupa.</span><span class="sxs-lookup"><span data-stu-id="a7467-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span> <span data-ttu-id="a7467-113">Ristlaadimise mallil saate valida direktiivi koodi välja sarnaselt täiendamise ja ostutellimuste seadistamise viisile.</span><span class="sxs-lookup"><span data-stu-id="a7467-113">You can select the directive code field on the cross-docking template, similar to the way you set up replenishment and purchase orders.</span></span>

<span data-ttu-id="a7467-114">Sissetuleva tellimuse vastuvõtmise ajal tuvastab ristlaadimise seadistus automaatselt ristlaadimise vajaduse ning loob vajaliku koguse jaoks liikumise töö, mis põhineb asukohakorralduse seadistusel.</span><span class="sxs-lookup"><span data-stu-id="a7467-114">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="a7467-115">Lao kandeid *ei* jäeta registreerimata ristlaadimise tühistamisel, isegi kui selle võimaluse säte on laohalduse parameetrites sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="a7467-115">Inventory transactions are *not* unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="a7467-116">Plaanitud ristilaadimise funktsioonide sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="a7467-116">Turn on the planned cross docking features</span></span>

<span data-ttu-id="a7467-117">Kui teie süsteemis ei ole veel selles teemas kirjeldatud funktsioone, avage [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja lülitage järgmised funktsioonid järgmises järjekorras sisse.</span><span class="sxs-lookup"><span data-stu-id="a7467-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="a7467-118">*Plaanitud ristlaadimine*</span><span class="sxs-lookup"><span data-stu-id="a7467-118">*Planned cross docking*</span></span>
1. <span data-ttu-id="a7467-119">*Asukohadirektiividega ristiliaadimismallid*</span><span class="sxs-lookup"><span data-stu-id="a7467-119">*Cross docking templates with location directives*</span></span>
    > [!NOTE]
    > <span data-ttu-id="a7467-120">See funktsioon võimaldab määrata ristlaadimise mallil **direktiivi tähise** välja sarnaselt täiendusmallide seadistamise viisiga.</span><span class="sxs-lookup"><span data-stu-id="a7467-120">This feature enables the **Directive code** field to be specified on the cross-docking template, similar to the way you set up replenishment templates.</span></span> <span data-ttu-id="a7467-121">Selle funktsiooni lubamine takistab teil lõpliku *put*-rea ristlaadimise töömalli ridadele direktiivi koodi lisamist.</span><span class="sxs-lookup"><span data-stu-id="a7467-121">Enabling this feature prevents you from adding a directive code on the cross-docking work template lines for the final *Put* line.</span></span> <span data-ttu-id="a7467-122">See tagab, et lõpliku asukoha saab määrata töö loomise ajal enne töömallide kaalumist.</span><span class="sxs-lookup"><span data-stu-id="a7467-122">This ensures that the final put location can be determined during work creation before considering work templates.</span></span>

## <a name="setup"></a><span data-ttu-id="a7467-123">Seadistus</span><span class="sxs-lookup"><span data-stu-id="a7467-123">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="a7467-124">Koorma sisestamise meetodite uuesti loomine</span><span class="sxs-lookup"><span data-stu-id="a7467-124">Regenerate load posting methods</span></span>

<span data-ttu-id="a7467-125">Plaanitud ristlaadimine rakendatakse koormuse sisestamise meetodina.</span><span class="sxs-lookup"><span data-stu-id="a7467-125">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="a7467-126">Pärast funktsiooni sisselülitamist tuleb meetodid uuesti luua.</span><span class="sxs-lookup"><span data-stu-id="a7467-126">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="a7467-127">Avage jaotis **Laohaldus \> Seadistus \> Koormuse sisestamise meetodid**.</span><span class="sxs-lookup"><span data-stu-id="a7467-127">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="a7467-128">Valige toimingupaanil suvand **Meetodite uuesti loomine**.</span><span class="sxs-lookup"><span data-stu-id="a7467-128">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="a7467-129">Kui uuesti loomine on lõpule viidud, peaksite nägema meetodit, mille suvandi **Meetodi nimi** väärtus on *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="a7467-129">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="a7467-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a7467-130">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="a7467-131">Ristlaadimise malli loomine</span><span class="sxs-lookup"><span data-stu-id="a7467-131">Create a cross-docking template</span></span>

1. <span data-ttu-id="a7467-132">Avage **Laohaldus \> Seadistus \> Töö \> Ristlaadimismallid**.</span><span class="sxs-lookup"><span data-stu-id="a7467-132">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="a7467-133">Malli loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a7467-133">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="a7467-134">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a7467-134">In the header, set the following values:</span></span>

    - <span data-ttu-id="a7467-135">**Järjestus:** *1*</span><span class="sxs-lookup"><span data-stu-id="a7467-135">**Sequence:** *1*</span></span>

        <span data-ttu-id="a7467-136">See väli määratleb mallide hindamise järjekorra.</span><span class="sxs-lookup"><span data-stu-id="a7467-136">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="a7467-137">**Ristlaadimismalli ID:** *51*</span><span class="sxs-lookup"><span data-stu-id="a7467-137">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="a7467-138">**Kirjeldus:** *Ladu 51*</span><span class="sxs-lookup"><span data-stu-id="a7467-138">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="a7467-139">**Nõudluse vabastamise poliitika:** *Enne tarne vastuvõtmist*</span><span class="sxs-lookup"><span data-stu-id="a7467-139">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="a7467-140">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="a7467-140">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="a7467-141">Kiirkaardi **Planeerimine** seadistus juhib kuidas mall töötab.</span><span class="sxs-lookup"><span data-stu-id="a7467-141">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="a7467-142">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a7467-142">Set the following values:</span></span>

    - <span data-ttu-id="a7467-143">**Nõudluse nõuded:** *Puudub*</span><span class="sxs-lookup"><span data-stu-id="a7467-143">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="a7467-144">See väli määratleb nõudluse varude nõuded.</span><span class="sxs-lookup"><span data-stu-id="a7467-144">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="a7467-145">Kui nõudlus peab olema seotud tarnega enne vabastamist, valige *Märkimine*.</span><span class="sxs-lookup"><span data-stu-id="a7467-145">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="a7467-146">Kui nõudmine tuleb enne vabastamist reserveerida vastavalt tellimusele, valige *Tellimuse reserveerimine*.</span><span class="sxs-lookup"><span data-stu-id="a7467-146">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="a7467-147">**Tüübi leidmine:** *Saadetise asukohad*</span><span class="sxs-lookup"><span data-stu-id="a7467-147">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="a7467-148">See väli määratleb, kas ristlaadimise töö peaks kasutama saadetise ajastamise/koormuse asukohti või kas see peaks kasutama asukohakorraldusi oma ajastamise/koormuse asukohtade leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="a7467-148">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="a7467-149">**Töömall:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="a7467-149">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="a7467-150">See väli määratleb töömalli, mida tuleks kasutada ristlaadimise töö loomisel.</span><span class="sxs-lookup"><span data-stu-id="a7467-150">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="a7467-151">**Uuesti kinnitamine tarne vastuvõtmisel:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="a7467-151">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="a7467-152">See suvand määratleb, kas tarnet tuleb vastuvõtmise ajal uuesti kinnitada.</span><span class="sxs-lookup"><span data-stu-id="a7467-152">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="a7467-153">Kui selle suvandi väärtuseks on seatud *Jah*, kontrollitakse nii maksimaalset ajavahemikku kui ka aegumiskuupäevade vahemikku.</span><span class="sxs-lookup"><span data-stu-id="a7467-153">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="a7467-154">**Korralduse kood:** jätke see väli tühjaks</span><span class="sxs-lookup"><span data-stu-id="a7467-154">**Directive code:** Leave this field blank</span></span>

        <span data-ttu-id="a7467-155">Selle suvandi lubavad *asukohadirektiivide funktsiooniga ristlaadimismallid*.</span><span class="sxs-lookup"><span data-stu-id="a7467-155">This option is enabled by the *Cross docking templates with location directives* feature.</span></span> <span data-ttu-id="a7467-156">Süsteem kasutab asukohakorraldusi, et aidata määrata parim asukoht ristlaadimise varude teisaldamiseks.</span><span class="sxs-lookup"><span data-stu-id="a7467-156">The system uses location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="a7467-157">Selle seadistamiseks määrake igale asjakohasele ristlaadimise mallile korralduse kood.</span><span class="sxs-lookup"><span data-stu-id="a7467-157">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="a7467-158">Kui määratakse direktiivikood, otsib süsteem töö loomisel asukohadirektiive direktiivikoodi järgi.</span><span class="sxs-lookup"><span data-stu-id="a7467-158">If a directive code is set, the system will search location directives by directive code when work is generated.</span></span> <span data-ttu-id="a7467-159">Sel viisil saate piirata asukohajuhiseid, mida kasutatakse konkreetse ristlaadimise malli puhul.</span><span class="sxs-lookup"><span data-stu-id="a7467-159">In this way, you can limit location directives that are used for a particular cross-docking template.</span></span>

    - <span data-ttu-id="a7467-160">**Kinnita maksimaalne ajavahemik:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="a7467-160">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="a7467-161">See suvand määratleb, kas maksimaalset ajavahemikku tuleb hinnata tarneallika valimisel.</span><span class="sxs-lookup"><span data-stu-id="a7467-161">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="a7467-162">Kui selle suvandi väärtuseks on seatud *Jah*, siis muutuvad maksimaalse ja minimaalse ajavahemiku väljad kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="a7467-162">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="a7467-163">**Maksimaalne ajavahemik** *5*</span><span class="sxs-lookup"><span data-stu-id="a7467-163">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="a7467-164">See väli määratleb maksimaalse lubatud ajavahemiku, mis on lubatud tarne saabumise ja nõudluse väljamineku vahel.</span><span class="sxs-lookup"><span data-stu-id="a7467-164">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="a7467-165">**Maksimaalse ajavahemiku ühik:** *Päevad*</span><span class="sxs-lookup"><span data-stu-id="a7467-165">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="a7467-166">**Minimaalne ajavahemik:** *0*</span><span class="sxs-lookup"><span data-stu-id="a7467-166">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="a7467-167">See väli määratleb minimaalse lubatud ajavahemiku, mis on lubatud tarne saabumise ja nõudluse väljamineku vahel.</span><span class="sxs-lookup"><span data-stu-id="a7467-167">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="a7467-168">**Minimaalse ajavahemiku ühik:** *Päevad*</span><span class="sxs-lookup"><span data-stu-id="a7467-168">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="a7467-169">**Aegumiskuupäevade vahemik** *0*</span><span class="sxs-lookup"><span data-stu-id="a7467-169">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="a7467-170">*Esimesena aegunud esimesena välja (FEFO) kriteerium:* see väli määratleb maksimaalse päevade arvu, mis jääb praegu laos oleva partii esimesena aeguva aegumiskuupäeva ja vastuvõetava partii vahele.</span><span class="sxs-lookup"><span data-stu-id="a7467-170">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="a7467-171">Kiirkaardil **Tarneallikad** saate määrata selle malli jaoks kehtivad tarnetüübid.</span><span class="sxs-lookup"><span data-stu-id="a7467-171">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="a7467-172">Valige **Uus** ja seejärel seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a7467-172">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="a7467-173">**Järjekorranumber:** *1*</span><span class="sxs-lookup"><span data-stu-id="a7467-173">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="a7467-174">**Tarneallikas:** *Ostutellimus*</span><span class="sxs-lookup"><span data-stu-id="a7467-174">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="a7467-175">Tööklassi loomine</span><span class="sxs-lookup"><span data-stu-id="a7467-175">Create a work class</span></span>

1. <span data-ttu-id="a7467-176">Minge jaotisse **Laohaldus \> Seadistus \> Töö \> Töö klassid**.</span><span class="sxs-lookup"><span data-stu-id="a7467-176">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="a7467-177">Tööklassi loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a7467-177">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="a7467-178">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a7467-178">Set the following values:</span></span>

    - <span data-ttu-id="a7467-179">**Töö klassi ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="a7467-179">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="a7467-180">**Kirjeldus:** *Ristlaadima*</span><span class="sxs-lookup"><span data-stu-id="a7467-180">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="a7467-181">**Töökäsu tüüp:** *Ristlaadimine*</span><span class="sxs-lookup"><span data-stu-id="a7467-181">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="a7467-182">Töömalli loomine</span><span class="sxs-lookup"><span data-stu-id="a7467-182">Create a work template</span></span>

1. <span data-ttu-id="a7467-183">Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.</span><span class="sxs-lookup"><span data-stu-id="a7467-183">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="a7467-184">Määrake välja **Töökäsu tüüp** väärtuseks *Ristlaadimine*.</span><span class="sxs-lookup"><span data-stu-id="a7467-184">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="a7467-185">Valige toimingupaanil suvand **Uus**, et lisada vahekaardile rida **Ülevaade**.</span><span class="sxs-lookup"><span data-stu-id="a7467-185">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="a7467-186">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a7467-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a7467-187">**Järjekorranumber:** *1*</span><span class="sxs-lookup"><span data-stu-id="a7467-187">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="a7467-188">**Töömall:** *51 ristlaadimine*</span><span class="sxs-lookup"><span data-stu-id="a7467-188">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="a7467-189">**Töömalli kirjeldus:** *51 ristlaadimine*</span><span class="sxs-lookup"><span data-stu-id="a7467-189">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="a7467-190">Valige **Salvesta**, et muuta kiirkaart **Töömalli üksikasjad** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="a7467-190">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="a7467-191">Valige kiirkaardil **Töömalli üksikasjad** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="a7467-191">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="a7467-192">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a7467-192">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a7467-193">**Töö tüüp:** *Komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="a7467-193">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="a7467-194">**Töö klassi ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="a7467-194">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="a7467-195">Valige **Uus**, et lisada uus rida ja määrake sellele järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a7467-195">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="a7467-196">**Töö tüüp:** *Ladustamine*</span><span class="sxs-lookup"><span data-stu-id="a7467-196">**Work type:** *Put*</span></span>
    - <span data-ttu-id="a7467-197">**Töö klassi ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="a7467-197">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="a7467-198">Valige **Salvesta** ja kinnitage, et malli *51 ristlaadimine* on valitud märkeruut **Kehtiv**.</span><span class="sxs-lookup"><span data-stu-id="a7467-198">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="a7467-199">Töötüübid *Komplekteerimine* ja *Ladustamine* peavad olema samad.</span><span class="sxs-lookup"><span data-stu-id="a7467-199">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="a7467-200">Asukohakorralduste loomine</span><span class="sxs-lookup"><span data-stu-id="a7467-200">Create location directives</span></span>

1. <span data-ttu-id="a7467-201">Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.</span><span class="sxs-lookup"><span data-stu-id="a7467-201">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="a7467-202">Määrake vasakpoolse paani välja **Töökäsu tüüp** suvandiks *Ristlaadimine*.</span><span class="sxs-lookup"><span data-stu-id="a7467-202">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="a7467-203">Valige toimingupaanil **Uus** ja seejärel seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a7467-203">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="a7467-204">**Järjekorranumber:** *1*</span><span class="sxs-lookup"><span data-stu-id="a7467-204">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="a7467-205">**Nimi:** *51 ladustamine ristlaadimisel*</span><span class="sxs-lookup"><span data-stu-id="a7467-205">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="a7467-206">**Töö tüüp:** *Ladustamine*</span><span class="sxs-lookup"><span data-stu-id="a7467-206">**Work type:** *Put*</span></span>
    - <span data-ttu-id="a7467-207">**Tegevuskoht:** *5*</span><span class="sxs-lookup"><span data-stu-id="a7467-207">**Site:** *5*</span></span>
    - <span data-ttu-id="a7467-208">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="a7467-208">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="a7467-209">Valige **Salvesta**, et muuta kiirkaart **Read** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="a7467-209">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="a7467-210">Valige kiirkaardil **Read** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="a7467-210">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="a7467-211">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a7467-211">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a7467-212">**Alates kogusest:** *1*</span><span class="sxs-lookup"><span data-stu-id="a7467-212">**From quantity:** *1*</span></span>
    - <span data-ttu-id="a7467-213">**Koguseni:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="a7467-213">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="a7467-214">Valige **Salvesta**, et muuta kiirkaart **Asukohakorralduse toimingud** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="a7467-214">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="a7467-215">Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="a7467-215">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="a7467-216">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a7467-216">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a7467-217">**Nimi:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="a7467-217">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="a7467-218">**Fikseeritud asukoha kasutus:** *Fikseeritud ja mittefikseeritud asukohad*</span><span class="sxs-lookup"><span data-stu-id="a7467-218">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="a7467-219">Valige **Salvesta**, et muuta tööriistariba **Asukohakorralduse toimingud** nupp **Päringu redigeerimine** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="a7467-219">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="a7467-220">Valige päringuredaktori avamiseks **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="a7467-220">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="a7467-221">Veenduge vahekaardil **Vahemik**, et järgmised kaks rida oleksid konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="a7467-221">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="a7467-222">Rida 1:</span><span class="sxs-lookup"><span data-stu-id="a7467-222">Line 1:</span></span>

        - <span data-ttu-id="a7467-223">**Tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="a7467-223">**Table:** *Locations*</span></span>
        - <span data-ttu-id="a7467-224">**Tuletatud tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="a7467-224">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="a7467-225">**Väli:** *Ladu*</span><span class="sxs-lookup"><span data-stu-id="a7467-225">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="a7467-226">**Kriteeriumid:** *51*</span><span class="sxs-lookup"><span data-stu-id="a7467-226">**Criteria:** *51*</span></span>

    - <span data-ttu-id="a7467-227">Rida 2:</span><span class="sxs-lookup"><span data-stu-id="a7467-227">Line 2:</span></span>

        - <span data-ttu-id="a7467-228">**Tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="a7467-228">**Table:** *Locations*</span></span>
        - <span data-ttu-id="a7467-229">**Tuletatud tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="a7467-229">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="a7467-230">**Väli:** *Asukoht*</span><span class="sxs-lookup"><span data-stu-id="a7467-230">**Field:** *Location*</span></span>
        - <span data-ttu-id="a7467-231">**Kriteeriumid:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="a7467-231">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="a7467-232">Päringuredaktori sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7467-232">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="a7467-233">Mobiilse seadme menüü-üksuse loomine</span><span class="sxs-lookup"><span data-stu-id="a7467-233">Create a mobile device menu item</span></span>

1. <span data-ttu-id="a7467-234">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="a7467-234">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="a7467-235">Valige vasakpoolse paani menüü-üksuste loendist **Ostu ladustamine**.</span><span class="sxs-lookup"><span data-stu-id="a7467-235">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="a7467-236">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="a7467-236">Select **Edit**.</span></span>
1. <span data-ttu-id="a7467-237">Valige kiirkaardil **Tööklassid** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="a7467-237">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="a7467-238">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a7467-238">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a7467-239">**Töö klassi ID:** *CrossDock*</span><span class="sxs-lookup"><span data-stu-id="a7467-239">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="a7467-240">**Töökäsu tüüp:** *Ristlaadimine*</span><span class="sxs-lookup"><span data-stu-id="a7467-240">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="a7467-241">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a7467-241">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="a7467-242">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="a7467-242">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="a7467-243">Ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="a7467-243">Create a purchase order</span></span>

<span data-ttu-id="a7467-244">Järgige neid etappe ostutellimuse loomiseks tarneallikana.</span><span class="sxs-lookup"><span data-stu-id="a7467-244">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="a7467-245">Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="a7467-245">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="a7467-246">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a7467-246">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a7467-247">Dialoogiboksis **Ostutellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a7467-247">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a7467-248">**Hankija konto:** *104*</span><span class="sxs-lookup"><span data-stu-id="a7467-248">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="a7467-249">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="a7467-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="a7467-250">Valige **OK** ja märkige tellimuse number üles.</span><span class="sxs-lookup"><span data-stu-id="a7467-250">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="a7467-251">Kiirkaardile **Ostutellimuse read** lisatakse uus rida.</span><span class="sxs-lookup"><span data-stu-id="a7467-251">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="a7467-252">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a7467-252">On this line, set the following values:</span></span>

    - <span data-ttu-id="a7467-253">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a7467-253">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="a7467-254">**Kogus:** *5*</span><span class="sxs-lookup"><span data-stu-id="a7467-254">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="a7467-255">Loo müügitellimus</span><span class="sxs-lookup"><span data-stu-id="a7467-255">Create a sales order</span></span>

<span data-ttu-id="a7467-256">Järgige neid etappe müügitellimuse loomiseks nõudluse allikana.</span><span class="sxs-lookup"><span data-stu-id="a7467-256">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="a7467-257">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="a7467-257">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a7467-258">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a7467-258">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a7467-259">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a7467-259">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a7467-260">**Kliendi konto:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="a7467-260">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="a7467-261">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="a7467-261">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="a7467-262">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7467-262">Select **OK**.</span></span>
1. <span data-ttu-id="a7467-263">Kiirkaardile **Müügitellimuse read** lisatakse uus rida.</span><span class="sxs-lookup"><span data-stu-id="a7467-263">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="a7467-264">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="a7467-264">On this line, set the following values:</span></span>

    - <span data-ttu-id="a7467-265">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a7467-265">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="a7467-266">**Kogus:** *3*</span><span class="sxs-lookup"><span data-stu-id="a7467-266">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="a7467-267">Plaanitud ristlaadimise loomine</span><span class="sxs-lookup"><span data-stu-id="a7467-267">Create planned cross-docking</span></span>

<span data-ttu-id="a7467-268">Järgige neid etappe osturellimusest plaanitud ristlaadimise loomiseks.</span><span class="sxs-lookup"><span data-stu-id="a7467-268">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="a7467-269">Valige äsja loodud müügitellimuse lehe **Müügitellimuse üksikasjad** toimingupaani vahekaardil **Ladu** grupis **Toimingud** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="a7467-269">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="a7467-270">Lattu vabastamine loob saadetise ja koormusrea müügitellimuse rea jaoks ning püüab eraldada varusid.</span><span class="sxs-lookup"><span data-stu-id="a7467-270">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="a7467-271">Teile kuvatakse teade.</span><span class="sxs-lookup"><span data-stu-id="a7467-271">You receive an informational message.</span></span> <span data-ttu-id="a7467-272">Kuvatakse ka järgmine hoiatusteade: „Voo XXXX jaoks ei loodud ühtegi tööd.</span><span class="sxs-lookup"><span data-stu-id="a7467-272">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="a7467-273">Lisateavet leiate töö loomise ajaloo logist.”</span><span class="sxs-lookup"><span data-stu-id="a7467-273">See the work creation history log for details."</span></span> <span data-ttu-id="a7467-274">Seda käitumist eeldatakse, kuna laos pole varusid.</span><span class="sxs-lookup"><span data-stu-id="a7467-274">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="a7467-275">Valige ruudustiku kohal oleva menüü **Ladu** kiirkaardilt **Müügitellimuse read** suvand **Saadetise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="a7467-275">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="a7467-276">Kuvatakse leht **Saadetise üksikasjad**, mis kuvab müügirea jaoks loodud saadetise.</span><span class="sxs-lookup"><span data-stu-id="a7467-276">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="a7467-277">Pange tähele, et kiirkaardil **Koormusread** on välja **Plaanitud ristlaadimise kogus** väärtuseks seatud *3*.</span><span class="sxs-lookup"><span data-stu-id="a7467-277">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="a7467-278">Kuna laos polnud varusid saadaval, kuid kehtiv tarneallikas saabub ristlaadimismallis määratletud ajavahemikus, loodi ristlaadimise kogus.</span><span class="sxs-lookup"><span data-stu-id="a7467-278">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="a7467-279">Valige kiirkaardil **Koormusread** suvand **Plaanitud ristlaadimine**, et vaadata loodud ristlaadimise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="a7467-279">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="a7467-280">Ristlaadimise töötlemine</span><span class="sxs-lookup"><span data-stu-id="a7467-280">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="a7467-281">Ostutellimuse vastuvõtmine ladustamise mobiilirakendusega</span><span class="sxs-lookup"><span data-stu-id="a7467-281">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="a7467-282">Süsteem võtab ostutellimuselt vastu koguse 5 vastuvõtvasse asukohta ja loob kaks tööd.</span><span class="sxs-lookup"><span data-stu-id="a7467-282">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="a7467-283">Esimese loodud töö ID suvandi **Töötellimuse tüüp** väärtus on *Ristlaadimine* ja see on seotud müügitellimusega.</span><span class="sxs-lookup"><span data-stu-id="a7467-283">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="a7467-284">Selle kogus on 3 ja see suunatakse saatmise lõplikku saatmisasukohta, et seda saaks kohe välja saata.</span><span class="sxs-lookup"><span data-stu-id="a7467-284">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="a7467-285">Teine loodud töö ID suvandi **Töötellimuse tüüp** väärtus on *Ostutellimused* ja see on seotud ostutellimusega.</span><span class="sxs-lookup"><span data-stu-id="a7467-285">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="a7467-286">Sellel on järelejäänud kogus 2, mida ei ristlaaditud ja mis on suunatud lattu ladustamiseks.</span><span class="sxs-lookup"><span data-stu-id="a7467-286">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="a7467-287">Logige mobiilsesse seadmesse lao *51* kasutajana sisse.</span><span class="sxs-lookup"><span data-stu-id="a7467-287">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="a7467-288">Avage jaotis **Sissetulev \> Vastuvõetud ost**.</span><span class="sxs-lookup"><span data-stu-id="a7467-288">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="a7467-289">Sisestage väljale **PONum** oma ostutellimuse number.</span><span class="sxs-lookup"><span data-stu-id="a7467-289">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="a7467-290">Sisestage väljale **Kogus** väärtus *5*.</span><span class="sxs-lookup"><span data-stu-id="a7467-290">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="a7467-291">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7467-291">Select **OK**.</span></span>
1. <span data-ttu-id="a7467-292">Järgmisel lehel määrake välja **Kaup** väärtuseks *A0001*.</span><span class="sxs-lookup"><span data-stu-id="a7467-292">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="a7467-293">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7467-293">Select **OK**.</span></span>
1. <span data-ttu-id="a7467-294">Kinnitage järgmisel lehel väärtused **PONum**, **Kaup** ja **Kogus**, valides **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7467-294">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="a7467-295">Teile kuvatakse teade „Töö lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="a7467-295">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="a7467-296">Väljumiseks valige **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="a7467-296">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="a7467-297">Ristlaadimiseks ja hulgi ladustamine</span><span class="sxs-lookup"><span data-stu-id="a7467-297">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="a7467-298">Praegu on mõlemal töö ID-l sama sihtkoha identifitseerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="a7467-298">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="a7467-299">Järgmiste etappide lõpule viimiseks peate hankima töö ID ja sihtkoha identifitseerimisnumbri ID.</span><span class="sxs-lookup"><span data-stu-id="a7467-299">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="a7467-300">Selle teabe saate hankida ostutellimuse rea ja müügitellimuse rea töö üksikasjadest.</span><span class="sxs-lookup"><span data-stu-id="a7467-300">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="a7467-301">Saate minna ka jaotisse **Laohaldus \> Töö \> Töö üksikasjad** ja filtreerida töö jaoks, kus suvandi **Ladu** väärtus on *51*.</span><span class="sxs-lookup"><span data-stu-id="a7467-301">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="a7467-302">Avage mobiilsel seadmel **Sissetulev \> Ostude ladustamine** ja sisestage töö jaoks sihtidentifitseerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="a7467-302">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="a7467-303">Sisestage väljale **ID** töö üksikasjadest saadud sihtidentifitseerimisnumbri ID.</span><span class="sxs-lookup"><span data-stu-id="a7467-303">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="a7467-304">Lehel ristlaadimise komplekteerimine kuvatakse komplekteerimise asukoht (*RECV*), sihtidentifitseerimisnumber (*identifitseerimisnumber*), kaup (*A0001*) ja kogus (*3*).</span><span class="sxs-lookup"><span data-stu-id="a7467-304">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="a7467-305">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7467-305">Select **OK**.</span></span>
1. <span data-ttu-id="a7467-306">Sisestage väljale **Siht-LP** sihtidentifitseerimisnumber selle identifitseerimisnumbri ID jaoks, mis tuleks ladustada (ristlaadida) saatmise asukohta.</span><span class="sxs-lookup"><span data-stu-id="a7467-306">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="a7467-307">Saate valida mis tahes soovitud identifitseerimisnumbri ID.</span><span class="sxs-lookup"><span data-stu-id="a7467-307">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="a7467-308">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7467-308">Select **OK**.</span></span>
1. <span data-ttu-id="a7467-309">Sisestage järgmisel lehel väljale **ID** sihtidentifitseerimisnumbri ID.</span><span class="sxs-lookup"><span data-stu-id="a7467-309">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="a7467-310">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7467-310">Select **OK**.</span></span>
1. <span data-ttu-id="a7467-311">Kinnitage töö järelejäänud koguse 2 komplekteerimiseks ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7467-311">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="a7467-312">Järgmisel lehel valige **Valmis** komplekteerimise toimingu lõpetamiseks ja alustage ladustamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="a7467-312">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="a7467-313">Mobiilirakendus annab teile nende jaoks asukoha ja identifitseerimisnumbri.</span><span class="sxs-lookup"><span data-stu-id="a7467-313">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="a7467-314">Kinnitage hulgiladustamine **Ladustamine**, valides **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7467-314">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="a7467-315">Järgmisel lehel kinnitage ristlaadimine **Ladustamine**, valides **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7467-315">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="a7467-316">Teile kuvatakse teade „Töö lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="a7467-316">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="a7467-317">Väljumiseks valige **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="a7467-317">Select **Cancel** to exit.</span></span>

<span data-ttu-id="a7467-318">Järgmine illustratsioon näitab, kuidas lõpule viidud ristlaadimise tööd kuvatakse Microsoftis Dynamics 365 Supply Chain Managementis.</span><span class="sxs-lookup"><span data-stu-id="a7467-318">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="a7467-319">![Lõpule viidud ristlaadimise töö](media/PlannedCrossDockingWork.png "Lõpule viidud ristlaadimise töö")</span><span class="sxs-lookup"><span data-stu-id="a7467-319">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]