---
title: Kauba konsolideerimine – asukoha kasutamine
description: Selles teemas antakse teavet funktsiooni kohta, mis hõlbustab laohalduritel kuvada ja filtreerida asukohtade mahulist kasutust terves laos. Haldurid saavad valida asukohti ja luua varude liikumise tööd otse kauba konsolideerimise lehelt, et konsolideerida kaupu ja seeläbi kasutada laos olevat ruumi tõhusamalt.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6edabc51981d8935672b44e53b453cfbaca9031b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004648"
---
# <a name="item-consolidation---location-utilization"></a><span data-ttu-id="3fe3a-104">Kauba konsolideerimine – asukoha kasutamine</span><span class="sxs-lookup"><span data-stu-id="3fe3a-104">Item consolidation - location utilization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fe3a-105">Selles teemas antakse teavet funktsiooni kohta, mis hõlbustab laohalduritel kuvada ja filtreerida asukohtade mahulist kasutust terves laos.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-105">This topic provides information about functionality that makes it easy for warehouse managers to view and filter the volumetric utilization of locations across the warehouse.</span></span> <span data-ttu-id="3fe3a-106">Haldurid saavad valida asukohti ja luua varude liikumise tööd otse lehelt **Kauba konsolideerimine**, et konsolideerida kaupu ja seeläbi kasutada laos olevat ruumi tõhusamalt.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-106">Managers can select locations and create inventory movement work directly from the **Item Consolidation** page to consolidate items and therefore make better use of warehouse space.</span></span>

## <a name="turn-on-the-features"></a><span data-ttu-id="3fe3a-107">Funktsioonide sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="3fe3a-107">Turn on the features</span></span>

<span data-ttu-id="3fe3a-108">Enne, kui saate kasutada selles teemas kirjeldatud funktsioone, peate need oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-108">Before you can use the features that are described in this topic, you must turn them on in your system.</span></span> <span data-ttu-id="3fe3a-109">Administraatorid saavad kasutada tööruumi [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), et kontrollida funktsioonide olekut ja need vajadusel sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="3fe3a-110">Lülitage sisse mõlemad järgmised funktsioonid loendis olevas järjekorras.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-110">Turn on both the following features, in the order that they are listed in.</span></span> <span data-ttu-id="3fe3a-111">(Mõlemad funktsioonid on mooduli **Laohaldus** jaoks.)</span><span class="sxs-lookup"><span data-stu-id="3fe3a-111">(Both features are for the **Warehouse management** module.)</span></span>

1. <span data-ttu-id="3fe3a-112">Laoasukoha olek</span><span class="sxs-lookup"><span data-stu-id="3fe3a-112">Warehouse location status</span></span>
2. <span data-ttu-id="3fe3a-113">Kauba konsolideerimise asukoha kasutamine</span><span class="sxs-lookup"><span data-stu-id="3fe3a-113">Item consolidation location utilization</span></span>

## <a name="warehouse-location-status"></a><span data-ttu-id="3fe3a-114">Laoasukoha olek</span><span class="sxs-lookup"><span data-stu-id="3fe3a-114">Warehouse location status</span></span>

<span data-ttu-id="3fe3a-115">Funktsioon *Lao asukoha olek* lisab lehele **Asukohad** neli uut välja, et jälgida lisateavet asukoha praeguse oleku kohta.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-115">The *Warehouse location status* feature adds four new fields to the **Locations** page to track additional information about the current state of the location:</span></span>

- <span data-ttu-id="3fe3a-116">**Kaubakood** – kaup, mis on hetkel asukohas.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-116">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="3fe3a-117">Kui asukoht sisaldab mitut kaupa, jäetakse see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-117">If the location contains multiple items, this field will be blank.</span></span>
- <span data-ttu-id="3fe3a-118">**Viimase tegevuse kuupäev ja kellaaeg** – selle asukohaga tehtud viimase laokande ajatempel.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-118">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="3fe3a-119">**Ajalise jaotuse kuupäev** – kuupäev, mil selle asukoha varud toodi lattu.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-119">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="3fe3a-120">See kuupäev arvutatakse identifitseerimisnumbri aegumiskuupäeva alusel.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-120">This date is calculated based on the license plate aging date.</span></span> <span data-ttu-id="3fe3a-121">Kuigi see kuupäev on täpne identifitseerimisnumbri järgi jälgitavate asukohtade puhul, ei pruugi see olla täpne asukohtade puhul, mida ei jälgita identifitseerimisnumbri järgi.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-121">Although this date is accurate for license plate–tracked locations, it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="3fe3a-122">**Asukoha olek** – selle asukoha olek.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-122">**Location status** – The status of the location.</span></span> <span data-ttu-id="3fe3a-123">Saadaval on neli väärtust.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-123">Four values are available:</span></span>

    - <span data-ttu-id="3fe3a-124">**Määratlemata** – asukohaprofiil ei jälgi olekut.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-124">**Undetermined** – The location profile doesn't track status.</span></span> <span data-ttu-id="3fe3a-125">Seetõttu ei ole praegune olek teada.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-125">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="3fe3a-126">**Tühi** – asukohas pole praegu varusid.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-126">**Empty** – No inventory is currently in the location.</span></span>
    - <span data-ttu-id="3fe3a-127">**Komplekteerimine** – väljaminevad kanded on tehtud asukoha suhtes pärast seda, kui see oli viimati tühi.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-127">**Picking** – Outbound transactions have been performed against the location after it was last empty.</span></span>
    - <span data-ttu-id="3fe3a-128">**Ladustamine** – ainult sissetulevad kanded on tehtud sellest ajast, kui see oli viimati tühi.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-128">**Storage** – Only inbound transactions have been performed since the location was last empty.</span></span>

<span data-ttu-id="3fe3a-129">Need väljad võimaldavad laohalduritel saada täpsemat ülevaadet lao asukohtade oleku kohta.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-129">These fields let warehouse managers get a better overview of the status of the locations in the warehouse.</span></span> <span data-ttu-id="3fe3a-130">Need võimaldavad ka palju täpsemat aruandlust ja filtreerimist.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-130">They also allow for more advanced reporting and filtering.</span></span>

## <a name="set-up-item-consolidation-and-location-utilization"></a><span data-ttu-id="3fe3a-131">Kauba konsolideerimise ja asukoha kasutamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="3fe3a-131">Set up item consolidation and location utilization</span></span>

<span data-ttu-id="3fe3a-132">Selles jaotises kirjeldatakse, kuidas valmistada süsteemi ette kauba konsolideerimise ja asukoha kasutamise kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-132">This section describes how to prepare your system to use item consolidation and location utilization.</span></span> <span data-ttu-id="3fe3a-133">Need protseduurid kasutavad standardsete demoandmete näidisväärtusi.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-133">The procedures use sample values from the standard demo data.</span></span> <span data-ttu-id="3fe3a-134">Kui plaanite töötada näidisstsenaariumiga, mida selles teemas hiljem käsitletakse, valige juriidiline isik **USMF** (mis sisaldab standardseid demoandmeid) ja looge kõik selles jaotises kirjeldatavad kirjed.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-134">If you plan to work through the example scenario that is provided later in this topic, select the **USMF** legal entity (which contains the standard demo data), and create each record that is described in this section.</span></span> <span data-ttu-id="3fe3a-135">Kui te ei plaani töötada näidisstsenaariumiga, saate siin esitatud väärtusi käsitleda sellist tüüpi seadistuste näidetena, mille peate funktsioonide kasutamiseks lõpule viima.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-135">If you don't plan to work through the example scenario, the values that are provided here can be considered examples of the types of setup that you must complete to use the features.</span></span>

### <a name="released-product"></a><span data-ttu-id="3fe3a-136">Väljastatud toode</span><span class="sxs-lookup"><span data-stu-id="3fe3a-136">Released product</span></span>

1. <span data-ttu-id="3fe3a-137">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-137">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="3fe3a-138">Valige väljal **Kaubakood** suvand *M9201* ja avage üksikasjade leht.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-138">In the **Item number** field, select *M9201*, and open the details page.</span></span>
1. <span data-ttu-id="3fe3a-139">Valige toimingupaani vahekaardi **Varude haldamine** grupis **Ladu** suvand **Füüsilised dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-139">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="3fe3a-140">Valige toimingupaani lehel **Füüsilised dimensioonid** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-140">On the **Physical dimension** page, on the Action Pane, select **New**.</span></span>

    <span data-ttu-id="3fe3a-141">Ruudustikku lisatakse uus rida.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-141">A new line is added to the grid.</span></span> <span data-ttu-id="3fe3a-142">Väli **Kaubakood** on eelseadistatud.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-142">The **Item number** field is preset.</span></span>

1. <span data-ttu-id="3fe3a-143">Valige *ea* väljal **Ühik**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-143">In the **Unit** field, select *ea*.</span></span> <span data-ttu-id="3fe3a-144">Rea ülejäänud väljad määratakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-144">The remaining fields on the line are automatically set.</span></span>
1. <span data-ttu-id="3fe3a-145">Valige **Salvesta** ja sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-145">Select **Save**, and close the page.</span></span>

### <a name="location-profile"></a><span data-ttu-id="3fe3a-146">Asukohaprofiil</span><span class="sxs-lookup"><span data-stu-id="3fe3a-146">Location profile</span></span>

1. <span data-ttu-id="3fe3a-147">Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukohaprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-147">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="3fe3a-148">Valige asukohaprofiilide loendist suvand **KORRUS-05**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-148">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="3fe3a-149">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-149">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="3fe3a-150">Veenduge, et kiirkaardil **Üldine** oleks mõlema järgmise suvandi väärtuseks seatud *Jah*.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-150">On the **General** FastTab, make sure that both the following options are set to *Yes*:</span></span>

    - <span data-ttu-id="3fe3a-151">Luba kaup asukohas</span><span class="sxs-lookup"><span data-stu-id="3fe3a-151">Enable item in location</span></span>
    - <span data-ttu-id="3fe3a-152">Luba asukoha olek</span><span class="sxs-lookup"><span data-stu-id="3fe3a-152">Enable location status</span></span>

1. <span data-ttu-id="3fe3a-153">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-153">Select **Save**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="3fe3a-154">Kui suvandite **Luba kaup asukohas** ja **Luba asukoha olek** väärtuseks oli juba seatud *Jah*, jätkake etapis 10 toodud juhistega kiirkaardi **Dimensioonid** seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-154">If the **Enable item in location** and **Enable location status** options were already set to *Yes*, skip ahead to the instructions for setting up the **Dimensions** FastTab in step 10.</span></span> <span data-ttu-id="3fe3a-155">Kui suvandite väärtuseks polnud seatud *Jah*, peate käivitama ühtsuskontrolli mooduli **Laohaldus** jaoks pärast nende käsitsi määramist.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-155">If the options weren't already set to *Yes*, you must run a consistency check for the **Warehouse management** module after you manually set them.</span></span> <span data-ttu-id="3fe3a-156">Sellisel juhul jätkake järgmise etapiga.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-156">In this case, continue to the next step.</span></span>

1. <span data-ttu-id="3fe3a-157">Ühtsuskontrolli käivitamiseks avage jaotis **Süsteemi administreerimine \> Perioodilised ülesanded \> Andmebaas \> Ühtsuskontroll**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-157">To run the consistency check, go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="3fe3a-158">Dialoogiboksis **Ühtsuskontroll** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-158">In the **Consistency check** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3fe3a-159">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-159">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="3fe3a-160">**Kontroll/parandus:** *Kontroll*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-160">**Check/Fix:** *Check*</span></span>
    - <span data-ttu-id="3fe3a-161">**Alates kuupäevast:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-161">**From date:** Leave this field blank.</span></span>
    - <span data-ttu-id="3fe3a-162">**Lao asukoha oleku ühtsuskontroll:** märkige see ruut.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-162">**Warehouse location status consistency check:** Select this check box.</span></span>

1. <span data-ttu-id="3fe3a-163">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-163">Select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="3fe3a-164">Teile kuvatakse teade, kui ühtsuskontroll on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-164">When the consistency check is completed, you receive a notification.</span></span> <span data-ttu-id="3fe3a-165">Teate kuvamiseks avage [Tegevuskeskus](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications).</span><span class="sxs-lookup"><span data-stu-id="3fe3a-165">Open the [Action Center](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) to view the message.</span></span> <span data-ttu-id="3fe3a-166">Valige üksikasjade kuvamiseks **Halda üksikasju**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-166">Select **Message details** to view the details.</span></span>
    >
    > <span data-ttu-id="3fe3a-167">Kui ühtsuskontroll kuvab teadet „Leiti vale asukoha oleku teave asukoha XXXX jaoks laos XX”, peate käivitama ühtsuskontrolli uuesti.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-167">If the message for the consistency check states, "Incorrect location status information found for location XXXX in warehouse XX," you must run the consistency check again.</span></span> <span data-ttu-id="3fe3a-168">Seekord seadke välja **Kontroll/parandus** väärtuseks *Paranda tõrge*.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-168">This time, set the **Check/Fix** field to *Fix error*.</span></span> <span data-ttu-id="3fe3a-169">Kontrollige teateid, veendumaks, et tõrkeid ei leitud.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-169">View the messages to make sure that no errors were found.</span></span>

1. <span data-ttu-id="3fe3a-170">Nüüd peate asukohaprofiili seadistamise lõpetama.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-170">You must now finish setting up the location profile.</span></span> <span data-ttu-id="3fe3a-171">Naaske jaotisse **Laohaldus \> Seadistus \> Ladu \> Asukohaprofiilid**, valige asukohaprofiil **KORRUS-05** ja seejärel valige toimingupaanil **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-171">Go back to **Warehouse management \> Setup \> Warehouse \> Location profiles**, select location profile **FLOOR-05**, and then, on the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="3fe3a-172">Määrake kiirkaardil **Dimensioonid** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-172">On the **Dimensions** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3fe3a-173">**Mahu kasutamise protsent:** *100*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-173">**Volume utilization percentage:** *100*</span></span>
    - <span data-ttu-id="3fe3a-174">**Lao asukoha jaoks kasutatav mahuline meetod:** *Kasuta asukoha mahtu*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-174">**Volumetric method used for inventory location:** *Use location volume*</span></span>
    - <span data-ttu-id="3fe3a-175">**Asukoha tegelik kõrgus:** *10*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-175">**Actual location height:** *10*</span></span>
    - <span data-ttu-id="3fe3a-176">**Asukoha tegelik laius:** *10*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-176">**Actual location width:** *10*</span></span>
    - <span data-ttu-id="3fe3a-177">**Asukoha tegelik sügavus:** *10*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-177">**Actual location depth:** *10*</span></span>
    - <span data-ttu-id="3fe3a-178">**Maksimaalne kaal:** *100*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-178">**Maximum weight:** *100*</span></span>

1. <span data-ttu-id="3fe3a-179">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-179">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="3fe3a-180">Mobiilse seadme menüü-üksused</span><span class="sxs-lookup"><span data-stu-id="3fe3a-180">Mobile device menu items</span></span>

1. <span data-ttu-id="3fe3a-181">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-181">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="3fe3a-182">Valige toimingupaanil **Uus**, et luua menüü-üksus sortimiseks.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-182">On the Action Pane, select **New** to create a menu item for sorting.</span></span>
1. <span data-ttu-id="3fe3a-183">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-183">In the header, set the following values:</span></span>

    - <span data-ttu-id="3fe3a-184">**Menüü-üksuse nimi:** *Korrigeeri üksuses*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-184">**Menu item name:** *Adjust In*</span></span>
    - <span data-ttu-id="3fe3a-185">**Pealkiri:** *Korrigeeri üksuses*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-185">**Title:** *Adjust In*</span></span>
    - <span data-ttu-id="3fe3a-186">**Režiim:** *töö*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-186">**Mode:** *Work*</span></span>
    - <span data-ttu-id="3fe3a-187">**Kasuta olemasolevat tööd:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-187">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="3fe3a-188">Määrake kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-188">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3fe3a-189">**Töö loomise protsess:** *Korrigeeri üksuses*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-189">**Work creation process:** *Adjustment in*</span></span>
    - <span data-ttu-id="3fe3a-190">**Varude korrigeerimistüübid:** *Korrigeeri üksuses*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-190">**Inventory adjustment types:** *Adjust in*</span></span>

1. <span data-ttu-id="3fe3a-191">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-191">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="3fe3a-192">Mobiilse seadme menüü</span><span class="sxs-lookup"><span data-stu-id="3fe3a-192">Mobile device menu</span></span>

1. <span data-ttu-id="3fe3a-193">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-193">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="3fe3a-194">Valige menüüde loendist suvand **Varud**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-194">In the list of menus, select **Inventory**.</span></span>
1. <span data-ttu-id="3fe3a-195">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-195">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="3fe3a-196">Otsige üles ja valige loendist **Saadaolevad menüüd ja menüü-üksused** suvand **Korrigeeri üksuses**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-196">In the **Available Menus And Menu Items** list, find and select the **Adjust In** menu item.</span></span>
1. <span data-ttu-id="3fe3a-197">Valige paremnoole nupp, et teisaldada **Korrigeeri üksuses** loendisse **Menüü struktuur**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-197">Select the right arrow button to move **Adjust In** to the **Menu Structure** list.</span></span> <span data-ttu-id="3fe3a-198">Sedasi saate lisada uue menüü-üksuse valitud menüüsse.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-198">In this way, you add the new menu item to the selected menu.</span></span>
1. <span data-ttu-id="3fe3a-199">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-199">Select **Save**.</span></span>

### <a name="movement-types"></a><span data-ttu-id="3fe3a-200">Teisaldamise tüübid</span><span class="sxs-lookup"><span data-stu-id="3fe3a-200">Movement types</span></span>

1. <span data-ttu-id="3fe3a-201">Avage jaotis **Laohaldus \> Seadistus \> Varud \> Liikumise tüübid**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-201">Go to **Warehouse management \> Setup \> Inventory \> Movement types**.</span></span>
1. <span data-ttu-id="3fe3a-202">Valige toimingupaanil **Uus** ja seejärel seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-202">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="3fe3a-203">**Liikumise tüübi kood:** *KONSOLIDEERI*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-203">**Movement type code:** *CONSOLIDATE*</span></span>
    - <span data-ttu-id="3fe3a-204">**Kirjeldus:** *Konsolideeri asukohad*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-204">**Description:** *Consolidate locations*</span></span>
    - <span data-ttu-id="3fe3a-205">**Töö klassi ID:** *InvMov*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-205">**Work class ID:** *InvMov*</span></span>

1. <span data-ttu-id="3fe3a-206">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-206">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="3fe3a-207">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="3fe3a-207">Example scenario</span></span>

<span data-ttu-id="3fe3a-208">Järgmine stsenaarium kasutab mobiilse seadme laorakendust, et teha varude *korrigeerimist üksusesse* lao kahes asukohas.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-208">The following scenario uses the warehouse app on a mobile device to make an inventory *adjustment in* to two locations in the warehouse.</span></span>

### <a name="add-inventory-to-locations"></a><span data-ttu-id="3fe3a-209">Varude lisamine asukohtadesse</span><span class="sxs-lookup"><span data-stu-id="3fe3a-209">Add inventory to locations</span></span>

1. <span data-ttu-id="3fe3a-210">Logige mobiilsesse seadmesse sisse kasutajana, kes on seadistatud lao *51* jaoks.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-210">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="3fe3a-211">Avage jaotis **Varud \> Korrigeeri üksuses**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-211">Go to **Inventory \> Adjust In**.</span></span>

    <span data-ttu-id="3fe3a-212">Nüüd saate sisestada esimese asukoha korrigeerimise.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-212">You will now enter the first location adjustment.</span></span>

1. <span data-ttu-id="3fe3a-213">Valige ülesandes **Korrigeeri üksuses** asukoht, mille jaoks varude korrigeerimist teha.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-213">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="3fe3a-214">Valige väljal **LOC** suvand *LP-001*.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-214">In the **LOC** field, select *LP-001*.</span></span>
1. <span data-ttu-id="3fe3a-215">Kinnitage asukoht.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-215">Confirm the location.</span></span>
1. <span data-ttu-id="3fe3a-216">Looge asukohta lisatava kauba jaoks identifitseerimisnumbri ID.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-216">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="3fe3a-217">Sisestage väljale **LP** väärtus *LP00101*.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-217">In the **LP** field, enter *LP00101*.</span></span>
1. <span data-ttu-id="3fe3a-218">Kinnitage identifitseerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-218">Confirm the license plate.</span></span>
1. <span data-ttu-id="3fe3a-219">Sisestage kaup, mis lisatakse identifitseerimisnumbrile.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-219">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="3fe3a-220">Sisestage väljale **ITEM** väärtus *M9201*.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-220">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="3fe3a-221">Kinnitage kaup.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-221">Confirm the item.</span></span>
1. <span data-ttu-id="3fe3a-222">Sisestage lisatava kauba kogus.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-222">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="3fe3a-223">Sisestage väljale **KOGUS** väärtus *10*.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-223">In the **QTY** field, enter *10*.</span></span>
1. <span data-ttu-id="3fe3a-224">Kinnitage kogus.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-224">Confirm the quantity.</span></span>

    <span data-ttu-id="3fe3a-225">Teile kuvatakse teade „Töö lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-225">You receive a "Work Completed" message.</span></span> <span data-ttu-id="3fe3a-226">Nüüd saate sisestada teise asukoha korrigeerimise.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-226">You will now enter the second location adjustment.</span></span>

1. <span data-ttu-id="3fe3a-227">Valige ülesandes **Korrigeeri üksuses** asukoht, mille jaoks varude korrigeerimist teha.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-227">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="3fe3a-228">Valige väljal **LOC** suvand *LP-002*.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-228">In the **LOC** field, select *LP-002*.</span></span>
1. <span data-ttu-id="3fe3a-229">Kinnitage asukoht.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-229">Confirm the location.</span></span>
1. <span data-ttu-id="3fe3a-230">Looge asukohta lisatava kauba jaoks identifitseerimisnumbri ID.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-230">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="3fe3a-231">Sisestage väljale **LP** väärtus *LP00201*.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-231">In the **LP** field, enter *LP00201*.</span></span>
1. <span data-ttu-id="3fe3a-232">Kinnitage identifitseerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-232">Confirm the license plate.</span></span>
1. <span data-ttu-id="3fe3a-233">Sisestage kaup, mis lisatakse identifitseerimisnumbrile.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-233">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="3fe3a-234">Sisestage väljale **ITEM** väärtus *M9201*.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-234">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="3fe3a-235">Kinnitage kaup.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-235">Confirm the item.</span></span>
1. <span data-ttu-id="3fe3a-236">Sisestage lisatava kauba kogus.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-236">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="3fe3a-237">Sisestage väljale **KOGUS** väärtus *15*.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-237">In the **QTY** field, enter *15*.</span></span>
1. <span data-ttu-id="3fe3a-238">Kinnitage kogus.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-238">Confirm the quantity.</span></span>

    <span data-ttu-id="3fe3a-239">Teile kuvatakse teade „Töö lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-239">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="3fe3a-240">Valige nupp Menüü (nimetatakse mõnikord hamburgeriks või hamburgeri nupuks) ja seejärel valige **Tühista**, et väljuda ülesandest **Korrigeeri üksuses**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-240">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit the **Adjustment in** task.</span></span>

### <a name="consolidate-locations"></a><span data-ttu-id="3fe3a-241">Asukohtade konsolideerimine</span><span class="sxs-lookup"><span data-stu-id="3fe3a-241">Consolidate locations</span></span>

1. <span data-ttu-id="3fe3a-242">Avage jaotis **Laohaldus \> Perioodilised ülesanded \> Kauba konsolideerimine**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-242">Go to **Warehouse management \> Periodic tasks \> Item consolidation**.</span></span>
1. <span data-ttu-id="3fe3a-243">Valige päises ladu, mille jaoks soovite konsolideerimist teha.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-243">In the header, select a warehouse to do the consolidation for.</span></span> <span data-ttu-id="3fe3a-244">Sisestage väljal **Ladu** väärtus *51*.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-244">In the **Warehouse** field, enter *51*.</span></span>

    <span data-ttu-id="3fe3a-245">Kuvatakse kirje iga asukoha kohta, kus kaup *M9201* korrigeeriti.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-245">A record is shown for each location where item *M9201* was adjusted.</span></span> <span data-ttu-id="3fe3a-246">Veerus **Kasutuse protsent** kuvatakse iga asukoha mahuline kasutamine.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-246">The **Utilization percentage** column shows the volumetric utilization of each location.</span></span>

1. <span data-ttu-id="3fe3a-247">Varude konsolideerimiseks valige kõik konsolideeritavad asukohad ja seejärel valige toimingupaanil **Konsolideeri varud**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-247">To consolidate inventory, select all the locations that must be consolidated, and then, on the Action Pane, select **Consolidate Inventory**.</span></span>
1. <span data-ttu-id="3fe3a-248">Määrake dialoogiboksis **Konsolideeri varud** asukoht ja liikumise tüüp, mida tuleks kasutada varude liikumise töö loomiseks.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-248">In the **Consolidate inventory** dialog box, specify the location and movement type that should be used to create the work for inventory movement.</span></span> <span data-ttu-id="3fe3a-249">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-249">Set the following values:</span></span>

    - <span data-ttu-id="3fe3a-250">**Asukoht:** *LP-001*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-250">**Location:** *LP-001*</span></span>
    - <span data-ttu-id="3fe3a-251">**Liikumise tüübi kood:** *KONSOLIDEERI*</span><span class="sxs-lookup"><span data-stu-id="3fe3a-251">**Movement type code:** *CONSOLIDATE*</span></span>

1. <span data-ttu-id="3fe3a-252">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-252">Select **OK**.</span></span>
1. <span data-ttu-id="3fe3a-253">Saate teate, mis kuvab loodud liikumise töö.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-253">You receive an informational message that shows the movement work that was created.</span></span> <span data-ttu-id="3fe3a-254">Märkige üles liikumise ID.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-254">Make a note of the movement work ID.</span></span>

### <a name="view-movement-work"></a><span data-ttu-id="3fe3a-255">Liikumise töö kuvamine</span><span class="sxs-lookup"><span data-stu-id="3fe3a-255">View movement work</span></span>

1. <span data-ttu-id="3fe3a-256">Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-256">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="3fe3a-257">Vaadake loodud tööd.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-257">View the work that was created.</span></span> <span data-ttu-id="3fe3a-258">Kasutage liikumise töö ID-d varude konsolideerimisest, et filtreerida või otsida tööruudustikku.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-258">Use the movement work ID from the inventory consolidation to filter or search the work grid.</span></span>

    <span data-ttu-id="3fe3a-259">Selle stsenaariumi puhul kasutati varude konsolideerimise asukohana olemasolevat asukohta, millel oli varusid.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-259">In this scenario, an existing location that had inventory was used as the inventory consolidation location.</span></span> <span data-ttu-id="3fe3a-260">Seetõttu loodi ainult üks töö ID.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-260">Therefore, only one work ID was created.</span></span>

    > [!NOTE]
   > <span data-ttu-id="3fe3a-261">Süsteem loob ühe töö ID iga liikumise kohta, mis tuleb lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-261">The system creates one work ID for each move that must be completed.</span></span> <span data-ttu-id="3fe3a-262">Kui määrate juba varusid sisaldava asukoha, luuakse ainult üks töö ID.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-262">If you specify a location that already contains inventory, only one work ID is created.</span></span> <span data-ttu-id="3fe3a-263">Kui määrate uue asukoha, luuakse kaks töö ID-d.</span><span class="sxs-lookup"><span data-stu-id="3fe3a-263">If you specify a new location, two work IDs are created.</span></span>
