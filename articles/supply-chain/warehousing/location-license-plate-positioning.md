---
title: Asukoha litsentsiplaadi paigutus
description: Identifitseerimisnumbri asukoha positsioneerimine võimaldab teil näha, kus identifitseerimisnumber asub mitme kaubaalusega asukohas, nt asukoht, mis kasutab kahekordsete kaubaalustega riiuleid.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6810753c10d03999c38a6163687effd771076c15
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530048"
---
# <a name="location-license-plate-positioning"></a><span data-ttu-id="4c564-103">Asukoha litsentsiplaadi paigutus</span><span class="sxs-lookup"><span data-stu-id="4c564-103">Location license plate positioning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c564-104">Identifitseerimisnumbri asukoha positsioneerimine võimaldab teil näha, kus identifitseerimisnumber asub mitme kaubaalusega asukohas, nt asukoht, mis kasutab kahekordsete kaubaalustega riiuleid.</span><span class="sxs-lookup"><span data-stu-id="4c564-104">License plate location positioning lets you see where a license plate is located in a multi-pallet location, such as a location that uses double-deep pallet racking.</span></span>

<span data-ttu-id="4c564-105">Funktsioon lisab igale lattu paigutatavale identifitseerimisnumbrile järjekorranumbri.</span><span class="sxs-lookup"><span data-stu-id="4c564-105">The feature adds a sequence number to each license plate that is put into a storage location.</span></span> <span data-ttu-id="4c564-106">Seda järjekorranumbrit kasutatakse identifitseerimisnumbrite järjestamiseks laos.</span><span class="sxs-lookup"><span data-stu-id="4c564-106">This sequence number is used to order the license plates in the storage location.</span></span> <span data-ttu-id="4c564-107">Seetõttu toetab funktsioon nutikalt selliseid stsenaariume, kus kliendid kasutavad gravitatsioonipõhist ladustamissüsteemi ja peavad komplekteerimise eesmärgil teadma, milline on identifitseerimisnumbri esikülg.</span><span class="sxs-lookup"><span data-stu-id="4c564-107">Therefore, the feature intelligently supports scenarios where customers are using a gravity racking system and must know, for picking purposes, which license plate is front-facing.</span></span>

<span data-ttu-id="4c564-108">Selles teemas esitletakse stsenaariumi, mis näitab, kuidas funktsiooni häälestada ja kasutada.</span><span class="sxs-lookup"><span data-stu-id="4c564-108">This topic presents a scenario that shows how to set up and use the feature.</span></span>

## <a name="turn-on-the-location-license-plate-positioning-feature"></a><span data-ttu-id="4c564-109">Asukoha identifitseerimisnumbri positsioneerimise funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="4c564-109">Turn on the Location license plate positioning feature</span></span>

<span data-ttu-id="4c564-110">Enne identifitseerimisnumbri asukoha positsioneerimise funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="4c564-110">Before you can use license plate location positioning, the feature must be turned on in your system.</span></span> <span data-ttu-id="4c564-111">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="4c564-111">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="4c564-112">Seega on funktsioon loetletud järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="4c564-112">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="4c564-113">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="4c564-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="4c564-114">**Funktsiooni nimi:** *Asukoha identifitseerimisnumbri positsioneerimine*</span><span class="sxs-lookup"><span data-stu-id="4c564-114">**Feature name:** *Location license plate positioning*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="4c564-115">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="4c564-115">Example scenario</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="4c564-116">Näidisandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="4c564-116">Make sample data available</span></span>

<span data-ttu-id="4c564-117">Selle stsenaariumi kasutamiseks siin soovitatud väärtuste abil, peate kasutama süsteemi, kuhu on installitud näidisandmed.</span><span class="sxs-lookup"><span data-stu-id="4c564-117">To work through this scenario by using the values that are suggested here, you must work on a system where sample data is installed.</span></span> <span data-ttu-id="4c564-118">Enne alustamist peate valima ka juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="4c564-118">Additionally, you must select the **USMF** legal entity before you start.</span></span>

### <a name="set-up-the-feature-for-this-scenario"></a><span data-ttu-id="4c564-119">Funktsiooni seadistamine selle stsenaariumi jaoks</span><span class="sxs-lookup"><span data-stu-id="4c564-119">Set up the feature for this scenario</span></span>

<span data-ttu-id="4c564-120">Viige lõpule järgmised protseduurid funktsiooni *Asukoha identifitseerimisnumbri positsioneerimine* seadistamine siin teemas esitatud stsenaariumi jaoks.</span><span class="sxs-lookup"><span data-stu-id="4c564-120">Complete the following procedures to set up the *Location license plate positioning* feature for the scenario that is presented in this topic.</span></span>

#### <a name="location-profiles"></a><span data-ttu-id="4c564-121">Asukoha profiilid</span><span class="sxs-lookup"><span data-stu-id="4c564-121">Location profiles</span></span>

<span data-ttu-id="4c564-122">Funktsioon peab olema asukohaprofiilis sisse lülitatud iga asukoha jaoks, kus seda kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="4c564-122">The feature must be turned on in the location profile for every location where it will be used.</span></span>

1. <span data-ttu-id="4c564-123">Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukohaprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="4c564-123">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="4c564-124">Valige vasakpoolsel paanil asukohaprofiilide loendist **BULK-06**.</span><span class="sxs-lookup"><span data-stu-id="4c564-124">In the list of location profiles in the left pane, select **BULK-06**.</span></span>
1. <span data-ttu-id="4c564-125">Funktsioon on lisanud kaks uut suvandit kiirkaardile **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="4c564-125">On the **General** FastTab, two new options have been added by the feature.</span></span> <span data-ttu-id="4c564-126">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="4c564-126">Set the following values:</span></span>

    - <span data-ttu-id="4c564-127">**Luba identifitseerimisnumbri positsioon:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="4c564-127">**Enable license plate position:** *Yes*</span></span>

        <span data-ttu-id="4c564-128">Kui selle suvandi väärtuseks on seatud *Jah*, säilitatakse identifitseerimisnumbri positsioon selle asukoha identifitseerimisnubrite puhul.</span><span class="sxs-lookup"><span data-stu-id="4c564-128">When this option is set to *Yes*, the license plate position will be maintained for license plates in the location.</span></span>

    - <span data-ttu-id="4c564-129">**Kuva mobiilse seadme LP-positsioon:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="4c564-129">**Display mobile device LP position:** *Yes*</span></span>

        <span data-ttu-id="4c564-130">Kui selle suvandi väärtuseks on seatud *Jah*, kuvatakse identifitseerimisnumbri positsioon mobiilse seadme kasutajatele korrigeerimise ja inventuuri ajal.</span><span class="sxs-lookup"><span data-stu-id="4c564-130">When this option is set to *Yes*, the license plate position will be shown to mobile device users during adjustment and counting.</span></span> <span data-ttu-id="4c564-131">Selle suvandi sätet saate muuta ainult juhul, kui funktsioon on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="4c564-131">You can change the setting of this option only when the feature is turned on.</span></span>

1. <span data-ttu-id="4c564-132">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="4c564-132">Select **Save**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="4c564-133">Asukohakorraldus</span><span class="sxs-lookup"><span data-stu-id="4c564-133">Location directives</span></span>

1. <span data-ttu-id="4c564-134">Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.</span><span class="sxs-lookup"><span data-stu-id="4c564-134">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="4c564-135">Veenduge, et vasakpoolsel paanil on välja **Töötellimuse tüüp** väärtuseks seatud *Müügitellimused*.</span><span class="sxs-lookup"><span data-stu-id="4c564-135">In the left pane, make sure that the **Work order type** field is set to *Sales orders*.</span></span>
1. <span data-ttu-id="4c564-136">Valige asukohakorralduste loendis **61 SO tellimuse komplekteerimine**.</span><span class="sxs-lookup"><span data-stu-id="4c564-136">In the list of location directives, select **61 SO Pick order**.</span></span>
1. <span data-ttu-id="4c564-137">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="4c564-137">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4c564-138">Valige kiirkaardil **Read** rida, mille suvandi **Järjekorranumber** väärtus on *2*.</span><span class="sxs-lookup"><span data-stu-id="4c564-138">On the **Lines** FastTab, select the line that has a **Sequence number** value of *2*.</span></span>
1. <span data-ttu-id="4c564-139">Valige kiirkaardil **Asukohakorralduse tegevused** rida, mille suvandi **Nimi** väärtus on *Komplekteeri kaubaalusest väiksem kogus* (see peaks olema ainus rida) ja muutke selle suvandi **Järjekorranumber** väärtuseks *2*.</span><span class="sxs-lookup"><span data-stu-id="4c564-139">On the **Location Directive Actions** FastTab, select the line that has a **Name** value of *Pick for less than pallet* (it should be the only line), and change its **Sequence number** value to *2*.</span></span>
1. <span data-ttu-id="4c564-140">Valige ruudustiku kohal suvand **Uus**, et lisada rida uue asukohakorralduse tegevuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="4c564-140">Select **New** above the grid to add a line for a new location directive action.</span></span>
1. <span data-ttu-id="4c564-141">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="4c564-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="4c564-142">**Järjekorranumber:** *1*</span><span class="sxs-lookup"><span data-stu-id="4c564-142">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="4c564-143">**Nimi:** *Komplekteerimise positsioon 1*</span><span class="sxs-lookup"><span data-stu-id="4c564-143">**Name:** *Pick position 1*</span></span>

1. <span data-ttu-id="4c564-144">Kui uus rida on valitud, valige ruudustiku kohal **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="4c564-144">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="4c564-145">Valige päringuredaktoris vahekaart **Liitmised**.</span><span class="sxs-lookup"><span data-stu-id="4c564-145">In the query editor, select the **Joins** tab.</span></span>
1. <span data-ttu-id="4c564-146">Laiendage tabeli liitmist **Asukohad**, et kuvada liitmist tabelis **Varude dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="4c564-146">Expand the **Locations** table join to show the join to the **Inventory dimensions** table.</span></span>
1. <span data-ttu-id="4c564-147">Laiendage tabeli liitmist **Varude dimensioonid**, et kuvada liitmist tabelis **Vaba kaubavaru**.</span><span class="sxs-lookup"><span data-stu-id="4c564-147">Expand the **Inventory dimensions** table join to show the join to the **On-hand inventory** table.</span></span>
1. <span data-ttu-id="4c564-148">Valige **Varude dimensioonid** ja seejärel valige **Lisa tabeli liitmine**.</span><span class="sxs-lookup"><span data-stu-id="4c564-148">Select **Inventory dimensions**, and then select **Add table join**.</span></span>
1. <span data-ttu-id="4c564-149">Valige kuvatava tabelite loendi veerust **Seos** suvand **Identifitseerimisnumber (Identifitseerimisnumber)**.</span><span class="sxs-lookup"><span data-stu-id="4c564-149">In the list of tables that appears, in the **Relation** column, select **License plate (License plate)**.</span></span> <span data-ttu-id="4c564-150">Seejärel valige **Vali**, et lisada **Identifitseerimisnumber** tabeli liitmisse **Varude dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="4c564-150">Then select **Select** to add **License plate** to the **Inventory dimensions** table join.</span></span>
1. <span data-ttu-id="4c564-151">Kui **Identifitseerimisnumber** on valitud, valige **Lisa tabeli liitmine**.</span><span class="sxs-lookup"><span data-stu-id="4c564-151">While **License plate** is still selected, select **Add table join**.</span></span>
1. <span data-ttu-id="4c564-152">Valige kuvatava tabelite loendi veerust **Seos** suvand **Asukoha identifitseerimisnumbri positsioneerimine (Identifitseerimisnumber)**.</span><span class="sxs-lookup"><span data-stu-id="4c564-152">In the list of tables that appears, in the **Relation** column, select **Location license plate positioning (License plate)**.</span></span> <span data-ttu-id="4c564-153">Seejärel valige **Vali**, et lisada **Asukoha identifitseerimisnumbri positsioneerimine** tabeli liitmisse **Varude dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="4c564-153">Then select **Select** to add **Location license plate positioning** to the **Inventory dimensions** table join.</span></span>

    <span data-ttu-id="4c564-154">![Tabeli liitmised](media/LpTableJoin.png "Tabeli liitmised")</span><span class="sxs-lookup"><span data-stu-id="4c564-154">![Table joins](media/LpTableJoin.png "Table joins")</span></span>

1. <span data-ttu-id="4c564-155">Värskendatud liidetud tabelite kinnitamiseks ja päringuredaktori sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c564-155">Select **OK** to confirm the updated joined tables and close the query editor.</span></span>
1. <span data-ttu-id="4c564-156">Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Redigeeri päringut** uuesti, et avada päringuredaktor uuesti.</span><span class="sxs-lookup"><span data-stu-id="4c564-156">On the **Location Directive Actions** FastTab, select **Edit query** again to reopen to the query editor.</span></span>
1. <span data-ttu-id="4c564-157">Vahekaardil **Vahemik** valige käsk **Lisa**, et lisada uus rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="4c564-157">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="4c564-158">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="4c564-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="4c564-159">**Tabel:** *Asukoha identifitseerimisnumbri positsioneerimine*</span><span class="sxs-lookup"><span data-stu-id="4c564-159">**Table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="4c564-160">**Tuletatud tabel:** *Asukoha identifitseerimisnumbri positsioneerimine*</span><span class="sxs-lookup"><span data-stu-id="4c564-160">**Derived table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="4c564-161">**Väli:** *LP positsioon*</span><span class="sxs-lookup"><span data-stu-id="4c564-161">**Field:** *LP Position*</span></span>
    - <span data-ttu-id="4c564-162">**Kriteeriumid:** *1*</span><span class="sxs-lookup"><span data-stu-id="4c564-162">**Criteria:** *1*</span></span>

    <span data-ttu-id="4c564-163">![Uus vahemik](media/LpPositionCriteria.png "Uus vahemik")</span><span class="sxs-lookup"><span data-stu-id="4c564-163">![New range](media/LpPositionCriteria.png "New range")</span></span>

1. <span data-ttu-id="4c564-164">Oma muudatuste kinnitamiseks ja päringu redaktori sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c564-164">Select **OK** to confirm your changes and close the query editor.</span></span>

### <a name="set-up-sample-data-for-this-scenario"></a><span data-ttu-id="4c564-165">Näidisandmete seadistamine selle stsenaariumi jaoks</span><span class="sxs-lookup"><span data-stu-id="4c564-165">Set up sample data for this scenario</span></span>

<span data-ttu-id="4c564-166">Selle stsenaariumi puhul peab kasutaja logima sisse ladustamise mobiilirakendusse, kasutades töötajat, kes on seadistatud laos *61* töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="4c564-166">For this scenario, the user must sign in to the warehousing mobile app by using a worker who is set up for warehouse *61* to perform work.</span></span> <span data-ttu-id="4c564-167">Kasutaja peab ka kanded lõpule viima.</span><span class="sxs-lookup"><span data-stu-id="4c564-167">The user must also complete transactions.</span></span>

<span data-ttu-id="4c564-168">Kuna funktsioon *Asukoha identifitseerimisnumbri positsioneerimine* lisab asukohas identifitseerimisnumbri positsioonidele uue identifikaatori, peate stsenaariumi toetamiseks looma esmalt mõned andmed.</span><span class="sxs-lookup"><span data-stu-id="4c564-168">Because the *Location license plate positioning* feature adds a new identifier for license plate positions in a location, you must first create some data to support the scenario.</span></span>

#### <a name="spot-count-the-first-location"></a><span data-ttu-id="4c564-169">Esimese asukoha punktinventuur</span><span class="sxs-lookup"><span data-stu-id="4c564-169">Spot-count the first location</span></span>

1. <span data-ttu-id="4c564-170">Avage ladustamise mobiilirakendus ja logige sisse lattu *61*.</span><span class="sxs-lookup"><span data-stu-id="4c564-170">Open the warehousing mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="4c564-171">Avage jaotis **Varud \> Punktinventuur**.</span><span class="sxs-lookup"><span data-stu-id="4c564-171">Go to **Inventory \> Spot Counting**.</span></span>
1. <span data-ttu-id="4c564-172">Määrake lehel **Punktinventuur** välja **Asukoht** väärtuseks *01A01R1S1B*.</span><span class="sxs-lookup"><span data-stu-id="4c564-172">On the **Spot Counting** page, set the **Location** field to *01A01R1S1B*.</span></span>
1. <span data-ttu-id="4c564-173">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c564-173">Select **OK**.</span></span>

    <span data-ttu-id="4c564-174">Sellel lehel kuvatakse teie sisestatud asukoht.</span><span class="sxs-lookup"><span data-stu-id="4c564-174">The page shows the location that you entered.</span></span> <span data-ttu-id="4c564-175">Samuti kuvatakse järgmine teade: „Asukoht lõpule viidud, kas soovite lisada uue LP või kauba?”</span><span class="sxs-lookup"><span data-stu-id="4c564-175">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="4c564-176">Asukohas inventuuri lisamiseks valige **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="4c564-176">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="4c564-177">Valige leht **Tsükliline inventuur: lisage uus LP või kaup**, väli **Kaup** ja sisestage seejärel väärtus *A0001*.</span><span class="sxs-lookup"><span data-stu-id="4c564-177">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0001*.</span></span>
1. <span data-ttu-id="4c564-178">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c564-178">Select **OK**.</span></span>
1. <span data-ttu-id="4c564-179">Valige leht **Tsükliline inventuur: lisage uus LP või kaup**, väli **LP** ja sisestage seejärel väärtus *LP1001* (või mis tahes muu teie valitud identifitseerimisnumbri number).</span><span class="sxs-lookup"><span data-stu-id="4c564-179">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1001* (or any other license plate number of your choice).</span></span>

    <span data-ttu-id="4c564-180">Lehel **Tsükliline inventuur: lisage uus LP või kaup** kuvatakse **Identifitseerimisnumbri positsioon 1**.</span><span class="sxs-lookup"><span data-stu-id="4c564-180">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="4c564-181">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c564-181">Select **OK**.</span></span>

    <span data-ttu-id="4c564-182">Nüüd peate määrama kauba koguse, mida identifitseerimisnumbris loendatakse.</span><span class="sxs-lookup"><span data-stu-id="4c564-182">You must now specify the quantity of the item that is counted on the license plate.</span></span>

1. <span data-ttu-id="4c564-183">Määrake välja **Kogus** väärtuseks *10*.</span><span class="sxs-lookup"><span data-stu-id="4c564-183">Set the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="4c564-184">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c564-184">Select **OK**.</span></span>

    <span data-ttu-id="4c564-185">Sellel lehel kuvatakse teie sisestatud asukoht.</span><span class="sxs-lookup"><span data-stu-id="4c564-185">The page shows the location that you entered.</span></span> <span data-ttu-id="4c564-186">Samuti kuvatakse järgmine teade: „Asukoht lõpule viidud, kas soovite lisada uue LP või kauba?”</span><span class="sxs-lookup"><span data-stu-id="4c564-186">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="4c564-187">Asukohas teise inventuuri lisamiseks valige **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="4c564-187">Select **Refresh** to add another count in the location.</span></span>
1. <span data-ttu-id="4c564-188">Valige leht **Tsükliline inventuur: lisage uus LP või kaup**, väli **Kaup** ja sisestage seejärel väärtus *A0002*.</span><span class="sxs-lookup"><span data-stu-id="4c564-188">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="4c564-189">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c564-189">Select **OK**.</span></span>
1. <span data-ttu-id="4c564-190">Valige leht **Tsükliline inventuur: lisage uus LP või kaup**, väli **LP** ja sisestage seejärel väärtus *LP1002* (või mis tahes muu teie valitud identifitseerimisnumbri number, eeldusel, et see erineb teie eelnevalt määratud identifitseerimisnumbri numbrist).</span><span class="sxs-lookup"><span data-stu-id="4c564-190">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1002* (or any other license plate number of your choice, provided that it differs from the license plate number that you specified earlier).</span></span>
1. <span data-ttu-id="4c564-191">Muutke identifitseerimisnumbri positsiooni, määrates välja **LP-positsioon** väärtuseks *2*.</span><span class="sxs-lookup"><span data-stu-id="4c564-191">Change the license plate position by setting the **LP Position** field to *2*.</span></span>
1. <span data-ttu-id="4c564-192">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c564-192">Select **OK**.</span></span>
1. <span data-ttu-id="4c564-193">Määrake kauba kogus, mida loendatakse identifitseerimisnumbris, seadistades välja **Kogus** väärtuseks *10*.</span><span class="sxs-lookup"><span data-stu-id="4c564-193">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="4c564-194">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c564-194">Select **OK**.</span></span>

    <span data-ttu-id="4c564-195">Sellel lehel kuvatakse teie sisestatud asukoht.</span><span class="sxs-lookup"><span data-stu-id="4c564-195">The page shows the location that you entered.</span></span> <span data-ttu-id="4c564-196">Samuti kuvatakse järgmine teade: „Asukoht lõpule viidud, kas soovite lisada uue LP või kauba?”</span><span class="sxs-lookup"><span data-stu-id="4c564-196">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="4c564-197">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c564-197">Select **OK**.</span></span>

<span data-ttu-id="4c564-198">Töö on nüüd lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="4c564-198">Work is now completed.</span></span>

#### <a name="spot-count-the-second-location"></a><span data-ttu-id="4c564-199">Teise asukoha punktinventuur</span><span class="sxs-lookup"><span data-stu-id="4c564-199">Spot-count the second location</span></span>

1. <span data-ttu-id="4c564-200">Määrake lehel **Punktinventuur** välja **Asukoht** väärtuseks *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="4c564-200">On the **Spot Counting** page, set the **Location** field to *01A01R1S2B*.</span></span>
1. <span data-ttu-id="4c564-201">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c564-201">Select **OK**.</span></span>

    <span data-ttu-id="4c564-202">Sellel lehel kuvatakse teie sisestatud asukoht.</span><span class="sxs-lookup"><span data-stu-id="4c564-202">The page shows the location that you entered.</span></span> <span data-ttu-id="4c564-203">Samuti kuvatakse järgmine teade: „Asukoht lõpule viidud, kas soovite lisada uue LP või kauba?”</span><span class="sxs-lookup"><span data-stu-id="4c564-203">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="4c564-204">Asukohas inventuuri lisamiseks valige **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="4c564-204">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="4c564-205">Valige leht **Tsükliline inventuur: lisage uus LP või kaup**, väli **Kaup** ja sisestage seejärel väärtus *A0002*.</span><span class="sxs-lookup"><span data-stu-id="4c564-205">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="4c564-206">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c564-206">Select **OK**.</span></span>
1. <span data-ttu-id="4c564-207">Valige leht **Tsükliline inventuur: lisage uus LP või kaup**, väli **LP** ja sisestage seejärel väärtus *LP1003* (või mis tahes muu teie valitud identifitseerimisnumbri number, eeldusel, et see erineb mõlemast teie eelnevalt määratud identifitseerimisnumbri numbrist).</span><span class="sxs-lookup"><span data-stu-id="4c564-207">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1003* (or any other license plate number of your choice, provided that it differs from the both the license plate numbers that you specified in the previous procedure).</span></span>

    <span data-ttu-id="4c564-208">Lehel **Tsükliline inventuur: lisage uus LP või kaup** kuvatakse **Identifitseerimisnumbri positsioon 1**.</span><span class="sxs-lookup"><span data-stu-id="4c564-208">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="4c564-209">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c564-209">Select **OK**.</span></span>
1. <span data-ttu-id="4c564-210">Määrake kauba kogus, mida loendatakse identifitseerimisnumbris, seadistades välja **Kogus** väärtuseks *10*.</span><span class="sxs-lookup"><span data-stu-id="4c564-210">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="4c564-211">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c564-211">Select **OK**.</span></span>

    <span data-ttu-id="4c564-212">Sellel lehel kuvatakse teie sisestatud asukoht.</span><span class="sxs-lookup"><span data-stu-id="4c564-212">The page shows the location that you entered.</span></span> <span data-ttu-id="4c564-213">Samuti kuvatakse järgmine teade: „Asukoht lõpule viidud, kas soovite lisada uue LP või kauba?”</span><span class="sxs-lookup"><span data-stu-id="4c564-213">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="4c564-214">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c564-214">Select **OK**.</span></span>

<span data-ttu-id="4c564-215">Töö on nüüd lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="4c564-215">Work is now completed.</span></span>

#### <a name="work-details"></a><span data-ttu-id="4c564-216">Töö üksikasjad</span><span class="sxs-lookup"><span data-stu-id="4c564-216">Work details</span></span>

> [!NOTE]
> <span data-ttu-id="4c564-217">Mobiilirakenduse punktinventuurid loovad tsüklilise inventuuri töö Microsoft Dynamics 365-s.</span><span class="sxs-lookup"><span data-stu-id="4c564-217">Spot counts from the mobile app create cycle counting work in Microsoft Dynamics 365.</span></span> <span data-ttu-id="4c564-218">See töö eeldab, et loendused aktsepteeritakse enne nende sisestamist varudesse.</span><span class="sxs-lookup"><span data-stu-id="4c564-218">The work requires that the counts be accepted before they are posted to inventory.</span></span>

1. <span data-ttu-id="4c564-219">Logige sisse rakendusse Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4c564-219">Sign in to Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="4c564-220">Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="4c564-220">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="4c564-221">Otsige vahekaardilt **Ülevaade** üles järgmiste väärtustega read.</span><span class="sxs-lookup"><span data-stu-id="4c564-221">On the **Overview** tab, look for the lines that have the following values:</span></span>

    - <span data-ttu-id="4c564-222">**Töötellimuse tüüp:** *Tsükliline inventuur*</span><span class="sxs-lookup"><span data-stu-id="4c564-222">**Work order type:** *Cycle counting*</span></span>
    - <span data-ttu-id="4c564-223">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="4c564-223">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="4c564-224">**Töö olek:** *Läbivaatuse ootel*</span><span class="sxs-lookup"><span data-stu-id="4c564-224">**Work status:** *Pending review*</span></span>

    <span data-ttu-id="4c564-225">Nende ridade jaoks peaks olema loodud kaks töö ID-d.</span><span class="sxs-lookup"><span data-stu-id="4c564-225">Two work IDs should have been created for these lines.</span></span> <span data-ttu-id="4c564-226">Mõlema töö ID loendused tuleb vastu võtta.</span><span class="sxs-lookup"><span data-stu-id="4c564-226">The counts for both these work IDs must be accepted.</span></span>

1. <span data-ttu-id="4c564-227">Valige ruudustikus esimese töö ID töökäsu tüübi *Tsükliline inventuur* jaoks.</span><span class="sxs-lookup"><span data-stu-id="4c564-227">In the grid, select the first work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="4c564-228">Valige toimingupaani vahekaardil **Töö** grupis **Töö** üksus **Tsükliline inventuur**.</span><span class="sxs-lookup"><span data-stu-id="4c564-228">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="4c564-229">Kuvatakse kaks rida, kummagi identifitseerimisnumbri kohta üks.</span><span class="sxs-lookup"><span data-stu-id="4c564-229">Two lines are shown, one for each item and license plate.</span></span> <span data-ttu-id="4c564-230">Väljade **Loendatud kogus**, **Asukoht**, **Identifitseerimisnumber** ja **Kaup** väärtused peaksid vastama mobiilses seadmes loodud inventuuri kirjetele.</span><span class="sxs-lookup"><span data-stu-id="4c564-230">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span> <span data-ttu-id="4c564-231">Kui mõni nendest väljadest pole nähtav, valige toimingupaanil **Kuva dimensioonid** nende ruudustikku lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="4c564-231">If any of these fields aren't visible, select **Display dimensions** on the Action Pane to add them to the grid.</span></span>

1. <span data-ttu-id="4c564-232">Valige mõlemad read.</span><span class="sxs-lookup"><span data-stu-id="4c564-232">Select both lines.</span></span>
1. <span data-ttu-id="4c564-233">Valige toimingupaanil **Kinnita inventuur**.</span><span class="sxs-lookup"><span data-stu-id="4c564-233">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="4c564-234">Kuvatakse teade „Sisestamine – tööleht”.</span><span class="sxs-lookup"><span data-stu-id="4c564-234">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="4c564-235">Valige **Teate üksikasjad** sisestatud töölehe numbri vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="4c564-235">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="4c564-236">Sulgege teate üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="4c564-236">Close the message details.</span></span>
1. <span data-ttu-id="4c564-237">Värskendage lehte **Töö**.</span><span class="sxs-lookup"><span data-stu-id="4c564-237">Refresh the **Work** page.</span></span>

    <span data-ttu-id="4c564-238">Esimese töö ID on suletud ja seda enam ei kuvata.</span><span class="sxs-lookup"><span data-stu-id="4c564-238">The first work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="4c564-239">Suletud töö kuvamiseks märkige ruudustiku kohal märkeruut **Kuva suletud**.</span><span class="sxs-lookup"><span data-stu-id="4c564-239">To view closed work, select the **Show closed** check box above the grid.</span></span>

    <span data-ttu-id="4c564-240">Nüüd saate kinnitada asukohas *01A01R1S2B* oleva identifitseerimisnumbri töö.</span><span class="sxs-lookup"><span data-stu-id="4c564-240">You will now accept the work for the license plate in the *01A01R1S2B* location.</span></span>

1. <span data-ttu-id="4c564-241">Valige vahekaardil **Ülevaade** teise töö ID töökäsu tüübi *Tsükliline inventuur* jaoks.</span><span class="sxs-lookup"><span data-stu-id="4c564-241">On the **Overview** tab, select the second work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="4c564-242">Valige toimingupaani vahekaardil **Töö** grupis **Töö** üksus **Tsükliline inventuur**.</span><span class="sxs-lookup"><span data-stu-id="4c564-242">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="4c564-243">Kuvatakse üks rida kauba ja identifitseerimisnumbri jaoks.</span><span class="sxs-lookup"><span data-stu-id="4c564-243">One line is shown, for the item and license plate.</span></span> <span data-ttu-id="4c564-244">Väljade **Loendatud kogus**, **Asukoht**, **Identifitseerimisnumber** ja **Kaup** väärtused peaksid vastama mobiilses seadmes loodud inventuuri kirjetele.</span><span class="sxs-lookup"><span data-stu-id="4c564-244">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span>

1. <span data-ttu-id="4c564-245">Valige rida.</span><span class="sxs-lookup"><span data-stu-id="4c564-245">Select the line.</span></span>
1. <span data-ttu-id="4c564-246">Valige toimingupaanil **Kinnita inventuur**.</span><span class="sxs-lookup"><span data-stu-id="4c564-246">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="4c564-247">Kuvatakse teade „Sisestamine – tööleht”.</span><span class="sxs-lookup"><span data-stu-id="4c564-247">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="4c564-248">Valige **Teate üksikasjad** sisestatud töölehe numbri vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="4c564-248">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="4c564-249">Sulgege teate üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="4c564-249">Close the message details.</span></span>
1. <span data-ttu-id="4c564-250">Värskendage lehte **Töö**.</span><span class="sxs-lookup"><span data-stu-id="4c564-250">Refresh the **Work** page.</span></span>

    <span data-ttu-id="4c564-251">Teise töö ID on suletud ja seda enam ei kuvata.</span><span class="sxs-lookup"><span data-stu-id="4c564-251">The second work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="4c564-252">Suletud töö kuvamiseks märkige ruudustiku kohal märkeruut **Kuva suletud**.</span><span class="sxs-lookup"><span data-stu-id="4c564-252">To view closed work, select the **Show closed** check box above the grid.</span></span>

#### <a name="on-hand-by-location"></a><span data-ttu-id="4c564-253">Laoseis asukoha järgi</span><span class="sxs-lookup"><span data-stu-id="4c564-253">On-hand by location</span></span>

1. <span data-ttu-id="4c564-254">Avage jaotis **Laohaldus \> Päringud ja aruanded \> Vaba varu asukoha järgi**.</span><span class="sxs-lookup"><span data-stu-id="4c564-254">Go to **Warehouse management \> Inquiries and reports \> On-hand by location**.</span></span>
1. <span data-ttu-id="4c564-255">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="4c564-255">Set the following values:</span></span>

    - <span data-ttu-id="4c564-256">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="4c564-256">**Site:** *6*</span></span>
    - <span data-ttu-id="4c564-257">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="4c564-257">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="4c564-258">**Värskenda kõigis asukohtades:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="4c564-258">**Refresh across locations:** *Yes*</span></span>

1. <span data-ttu-id="4c564-259">Pange tähele, et asukohas *01A01R1S1B* on kaks identifitseerimisnumbrit.</span><span class="sxs-lookup"><span data-stu-id="4c564-259">Notice that location *01A01R1S1B* has two license plates:</span></span>

    - <span data-ttu-id="4c564-260">**A0001**, kus välja **LP-positsioon** väärtuseks on seatud *1*</span><span class="sxs-lookup"><span data-stu-id="4c564-260">**A0001**, where the **LP Position** field is set to *1*</span></span>
    - <span data-ttu-id="4c564-261">**A0002**, kus välja **LP-positsioon** väärtuseks on seatud *2*</span><span class="sxs-lookup"><span data-stu-id="4c564-261">**A0002**, where the **LP Position** field is set to *2*</span></span>

1. <span data-ttu-id="4c564-262">Pange tähele, et asukohas *01A01R1S2B* on üks identifitseerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="4c564-262">Notice that location *01A01R1S2B* has one license plate:</span></span>

    - <span data-ttu-id="4c564-263">**A0002**, kus välja **LP-positsioon** väärtuseks on seatud *1*</span><span class="sxs-lookup"><span data-stu-id="4c564-263">**A0002**, where the **LP Position** field is set to *1*</span></span>

### <a name="sales-order-scenario"></a><span data-ttu-id="4c564-264">Müügitellimuse stsenaarium</span><span class="sxs-lookup"><span data-stu-id="4c564-264">Sales order scenario</span></span>

<span data-ttu-id="4c564-265">Nüüd, kui funktsioon *Asukoha identifitseerimisnumbri positsioneerimine* on seadistatud ja varud on etapiviisilised, peate looma müügitellimuse komplekteerimistöö loomiseks, mis suunab lao töötaja komplekteerima kaupa *A0002* varude asukohast, kus kaubaaluse ID on positsioonil *1*.</span><span class="sxs-lookup"><span data-stu-id="4c564-265">Now that the *Location license plate positioning* feature has been set up, and the inventory has been staged, you must create a sales order to generate picking work that will direct the warehouse worker to pick item *A0002* from the inventory location where the pallet ID is in position *1*.</span></span>

1. <span data-ttu-id="4c564-266">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="4c564-266">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="4c564-267">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="4c564-267">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4c564-268">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="4c564-268">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="4c564-269">**Kliendi konto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="4c564-269">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="4c564-270">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="4c564-270">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="4c564-271">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c564-271">Select **OK**.</span></span>
1. <span data-ttu-id="4c564-272">Kiirkaardi **Müügitellimuse read** ruudustikku on lisatud uus rida.</span><span class="sxs-lookup"><span data-stu-id="4c564-272">A new line is added to the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="4c564-273">Määrake sellel uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="4c564-273">On this new line, set the following values:</span></span>

    - <span data-ttu-id="4c564-274">**Kauba kood:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="4c564-274">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="4c564-275">**Kogus:** *1*</span><span class="sxs-lookup"><span data-stu-id="4c564-275">**Quantity:** *1*</span></span>

1. <span data-ttu-id="4c564-276">Valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="4c564-276">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="4c564-277">Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida varud tellimuserea jaoks.</span><span class="sxs-lookup"><span data-stu-id="4c564-277">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve inventory for the order line.</span></span>
1. <span data-ttu-id="4c564-278">Sulgege leht **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="4c564-278">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="4c564-279">Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="4c564-279">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="4c564-280">Saate teabesõnumi, mis näitab selle tellimuse jaoks loodud voo ID-d ja saadetise ID-d.</span><span class="sxs-lookup"><span data-stu-id="4c564-280">You receive an informational message that indicates the wave ID and shipment ID that were created for the order.</span></span>

1. <span data-ttu-id="4c564-281">Valige ruudustiku kohal oleva menüü **Ladu** kiirkaardilt **Müügitellimuse read** suvand **Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="4c564-281">On the **Sales order lines** FastTab, on the **Warehouse** menu above the grid, select **Work details**.</span></span>
1. <span data-ttu-id="4c564-282">Kuvatakse leht **Töö**, mis kuvab müügirea jaoks loodud töö.</span><span class="sxs-lookup"><span data-stu-id="4c564-282">The **Work** page appears and shows the work that was created for the sales line.</span></span> <span data-ttu-id="4c564-283">Märkige üles kuvatav töö ID.</span><span class="sxs-lookup"><span data-stu-id="4c564-283">Make a note of the work ID that is shown.</span></span>

### <a name="sales-picking-scenario"></a><span data-ttu-id="4c564-284">Müügi komplekteerimise stsenaarium</span><span class="sxs-lookup"><span data-stu-id="4c564-284">Sales picking scenario</span></span>

1. <span data-ttu-id="4c564-285">Avage mobiilirakendus ja logige sisse lattu *61*.</span><span class="sxs-lookup"><span data-stu-id="4c564-285">Open the mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="4c564-286">Avage jaotis **Väljaminev \> Müügi komplekteerimine**.</span><span class="sxs-lookup"><span data-stu-id="4c564-286">Go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="4c564-287">Valige leht **Töö ID / identifitseerimisnumbri ID skannimine**, valige väli **ID** ja sisestage seejärel müügirea välja töö ID.</span><span class="sxs-lookup"><span data-stu-id="4c564-287">On the **Scan a work ID / license plate ID** page, select the **ID** field, and then enter the work ID from the sales line.</span></span>
1. <span data-ttu-id="4c564-288">Pange tähele, et komplekteerimistöö suunab teid komplekteerima kauba *A0002* asukohast *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="4c564-288">Notice that the picking work directs you to pick item *A0002* from location *01A01R1S2B*.</span></span> <span data-ttu-id="4c564-289">Saate selle juhise seetõttu, et kaup *A0002* on identifitseerimisnumbri all, mis on selles asukohas positsioonis *1*.</span><span class="sxs-lookup"><span data-stu-id="4c564-289">You receive this instruction because item *A0002* is on a license plate that is in position *1* in that location.</span></span>

    <span data-ttu-id="4c564-290">![Positsiooni 1 asukoht](media/LocationLicensePlatePositioning.png "Positsiooni 1 asukoht")</span><span class="sxs-lookup"><span data-stu-id="4c564-290">![Position 1 location](media/LocationLicensePlatePositioning.png "Position 1 location")</span></span>

1. <span data-ttu-id="4c564-291">Sisestage selle asukoha jaoks loodud identifitseerimisnumbri ID ja seejärel järgige viipasid müügitellimuse komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="4c564-291">Enter the license plate ID that you created for the location, and then follow the prompts to pick the sales order.</span></span>
