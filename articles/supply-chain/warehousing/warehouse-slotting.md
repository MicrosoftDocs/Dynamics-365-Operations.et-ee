---
title: Lao ruumi leidmine
description: Selles teemas antakse teavet lao ruumi leidmise kohta. Lao ruumi leidmise abil saate konsolideerida nõudlust kauba ja mõõtühiku järgi tellimustest, mille olek on tellitud, reserveeritud või väljastatud. See aitab laohalduritel nutikalt planeerida komplekteerimise asukohti enne tellimuse lattu väljatamist ja komplekteerimistöö loomist.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ed9e6eae2ecc8de8d5eeef4699678e93dd74f193
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017410"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="d948d-105">Lao ruumi leidmine</span><span class="sxs-lookup"><span data-stu-id="d948d-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d948d-106">Lao ruumi leidmise abil saate konsolideerida nõudlust kauba ja mõõtühiku järgi tellimustest, mille olek on *Tellitud* , *Reserveeritud* või *Väljastatud*.</span><span class="sxs-lookup"><span data-stu-id="d948d-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered* , *Reserved* , or *Released*.</span></span> <span data-ttu-id="d948d-107">Loodud nõudlust saab seejärel rakendada asukohtadele, mida kasutatakse koguse, ühiku, füüsiliste dimensioonide, fikseeritud asukohtade ja muu alusel komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="d948d-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="d948d-108">Pärast seda, kui ruumi leidmise plaan on loodud, saab luua täiendamise töö, et tuua igasse asukohta sobiv kogus varusid.</span><span class="sxs-lookup"><span data-stu-id="d948d-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="d948d-109">See funktsioon aitab laohalduritel nutikalt planeerida komplekteerimise asukohti enne tellimuse lattu väljatamist ja komplekteerimistöö loomist.</span><span class="sxs-lookup"><span data-stu-id="d948d-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="d948d-110">Lao ruumi leidmise funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="d948d-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="d948d-111">Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="d948d-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="d948d-112">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="d948d-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d948d-113">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="d948d-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d948d-114">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="d948d-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d948d-115">**Funktsiooni nimi** *Lao ruumi leidmise funktsioon*</span><span class="sxs-lookup"><span data-stu-id="d948d-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="d948d-116">Lao ruumi leidmise seadistamine</span><span class="sxs-lookup"><span data-stu-id="d948d-116">Set up warehouse slotting</span></span>

<span data-ttu-id="d948d-117">Lao ruumi leidmise kasutamiseks peate seadistama järgmised elemendid oma süsteemis.</span><span class="sxs-lookup"><span data-stu-id="d948d-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="d948d-118">Mõõtühikute järkude loomine ruumi leidmise jaoks</span><span class="sxs-lookup"><span data-stu-id="d948d-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="d948d-119">Mõõtühikute järgud võimaldavad mitme mõõtühiku grupeerimist ruumi leidmise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="d948d-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="d948d-120">Näiteks kui erineva suurusega kaste komplekteeritakse samalt kastide komplekteerimise alalt, saab iga suuruse jaoks luua ühe järgu.</span><span class="sxs-lookup"><span data-stu-id="d948d-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="d948d-121">**Iga mõõtühiku jaoksa tuleb luua rida, mis on selle järgu osa.**</span><span class="sxs-lookup"><span data-stu-id="d948d-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="d948d-122">Avage jaotis **Laohaldus \> Häälestus \> Täiendamine \> Ruumi leidmise mõõtühikute järgud**.</span><span class="sxs-lookup"><span data-stu-id="d948d-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="d948d-123">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d948d-123">Select **New**.</span></span>
1. <span data-ttu-id="d948d-124">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="d948d-125">**Mõõtühiku järk:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="d948d-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="d948d-126">**Kirjeldus:** *Iga kasti kaubaalus*</span><span class="sxs-lookup"><span data-stu-id="d948d-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="d948d-127">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d948d-127">Select **Save**.</span></span>
1. <span data-ttu-id="d948d-128">Valige kiirkaardil **Mõõtühikud** suvand **Uus** , et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="d948d-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d948d-129">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d948d-130">**Ühik:** *Kast*</span><span class="sxs-lookup"><span data-stu-id="d948d-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="d948d-131">**Kirjeldus:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="d948d-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="d948d-132">See täidetakse muudatuste salvestamisel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="d948d-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="d948d-133">**Ühiku klass:** *Kogus*</span><span class="sxs-lookup"><span data-stu-id="d948d-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="d948d-134">Klõpsake valikut **Uus** , et lisada ruudustikku teine rida.</span><span class="sxs-lookup"><span data-stu-id="d948d-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="d948d-135">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d948d-136">**Ühik:** *ea*</span><span class="sxs-lookup"><span data-stu-id="d948d-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="d948d-137">**Kirjeldus:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="d948d-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="d948d-138">See täidetakse muudatuste salvestamisel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="d948d-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="d948d-139">**Ühiku klass:** *Kogus*</span><span class="sxs-lookup"><span data-stu-id="d948d-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="d948d-140">Klõpsake valikut **Uus** , et lisada ruudustikku kolmas rida.</span><span class="sxs-lookup"><span data-stu-id="d948d-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="d948d-141">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d948d-142">**Ühik:** *PL*</span><span class="sxs-lookup"><span data-stu-id="d948d-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="d948d-143">**Kirjeldus:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="d948d-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="d948d-144">See täidetakse muudatuste salvestamisel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="d948d-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="d948d-145">**Ühiku klass:** *Kogus*</span><span class="sxs-lookup"><span data-stu-id="d948d-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="d948d-146">Järgu salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d948d-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="d948d-147">Korralduskoodi loomine ruumi leidmiseks</span><span class="sxs-lookup"><span data-stu-id="d948d-147">Create a directive code for slotting</span></span>

<span data-ttu-id="d948d-148">Peate valima korralduskoodi, mis tuleks malliga seostada.</span><span class="sxs-lookup"><span data-stu-id="d948d-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="d948d-149">Avage jaotis **Laohaldus \> Seadistus \> Korralduskoodid**.</span><span class="sxs-lookup"><span data-stu-id="d948d-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="d948d-150">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d948d-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d948d-151">Sisestage väljale **Korralduskood** väärtus *Ruumi leidmine*.</span><span class="sxs-lookup"><span data-stu-id="d948d-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="d948d-152">Sisestage väljale **Korralduse kirjeldus** väärtus *Ruumi leidmine*.</span><span class="sxs-lookup"><span data-stu-id="d948d-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="d948d-153">Ruumi leidmise mallide seadistamine</span><span class="sxs-lookup"><span data-stu-id="d948d-153">Set up slotting templates</span></span>

<span data-ttu-id="d948d-154">Iga ruumi leidmise mall juhib seda, kuidas kindla lao asukohtade jaoks määratakse varusid.</span><span class="sxs-lookup"><span data-stu-id="d948d-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="d948d-155">Iga mall peab sisaldama rida iga ruumi leidmise täpsustuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="d948d-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="d948d-156">Kasutage selle jaotise protseduure, et häälestada ruumi leidmise malle.</span><span class="sxs-lookup"><span data-stu-id="d948d-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="d948d-157">Avage jaotis **Laohaldus \> Seadistus \> Täiendamine \> Ruumi leidmise mallid**.</span><span class="sxs-lookup"><span data-stu-id="d948d-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="d948d-158">Valige malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d948d-158">Select **New** to create a template.</span></span>

<span data-ttu-id="d948d-159">Järgmisena peate seadistama malli päise, ruumi leidmise kirjelduse ja asukohakorraldused järgmistes alamjaotistes kirjeldatud juhiste järgi.</span><span class="sxs-lookup"><span data-stu-id="d948d-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="d948d-160">Ruumi leidmise malli päise seadistamine</span><span class="sxs-lookup"><span data-stu-id="d948d-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="d948d-161">Määrake malli päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="d948d-162">**Ruumi leidmise mall:** _61_</span><span class="sxs-lookup"><span data-stu-id="d948d-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="d948d-163">**Kirjeldus:** _61_</span><span class="sxs-lookup"><span data-stu-id="d948d-163">**Description:** _61_</span></span>
    - <span data-ttu-id="d948d-164">**Nõudluse tüüp:** *Müügitellimus*</span><span class="sxs-lookup"><span data-stu-id="d948d-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="d948d-165">Praegu on *Müügitellimus* ainus toetatud nõudluse tüüp.</span><span class="sxs-lookup"><span data-stu-id="d948d-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="d948d-166">**Nõudluse strateegia:** _Tellitud_</span><span class="sxs-lookup"><span data-stu-id="d948d-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="d948d-167">Sellel väljal on saadaval järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="d948d-168">**Tellitud** – müügitellimuse täielikku tellitud kogust tuleks arvestada nõudlusena.</span><span class="sxs-lookup"><span data-stu-id="d948d-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="d948d-169">**Reserveeritud** – ainult reserveeritud müügitellimuse rea (füüsilised ja tellitud) koguseid tuleks arvestada nõudlusena.</span><span class="sxs-lookup"><span data-stu-id="d948d-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="d948d-170">**Ladu:** _61_</span><span class="sxs-lookup"><span data-stu-id="d948d-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="d948d-171">**Luba voo nõudmisel kasutada reserveerimata koguseid:** _Jah_</span><span class="sxs-lookup"><span data-stu-id="d948d-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="d948d-172">Samuti saate määrata päringu hinnatava nõudluse ulatuse kitsendamiseks.</span><span class="sxs-lookup"><span data-stu-id="d948d-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="d948d-173">Ruumi leidmise täpsustuste seadistamine iga malli jaoks</span><span class="sxs-lookup"><span data-stu-id="d948d-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="d948d-174">Iga loodava malli jaoks järgige neid etappe, et lisada rida iga ruumi leidmise täpsustuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="d948d-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="d948d-175">Valige kiirkaardil **Ruumi leidmise malli üksikasjad** suvand **Uus** , et luua malli rida.</span><span class="sxs-lookup"><span data-stu-id="d948d-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="d948d-176">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d948d-177">**Järjestus:** _1_</span><span class="sxs-lookup"><span data-stu-id="d948d-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="d948d-178">**Kirjeldus:** _Fikseeritud asukoht_</span><span class="sxs-lookup"><span data-stu-id="d948d-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="d948d-179">**Minimaalne kogus:** _1_</span><span class="sxs-lookup"><span data-stu-id="d948d-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="d948d-180">See väli määratleb rea jaoks nõutava minimaalse koguse.</span><span class="sxs-lookup"><span data-stu-id="d948d-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="d948d-181">**Maksimaalne kogus:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="d948d-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="d948d-182">See väli määratleb rea jaoks kehtiva maksimaalse koguse.</span><span class="sxs-lookup"><span data-stu-id="d948d-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="d948d-183">**Ühik:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="d948d-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="d948d-184">See väli määratleb mõõtühiku, millele minimaalne ja maksimaalne kogus viitab.</span><span class="sxs-lookup"><span data-stu-id="d948d-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="d948d-185">**Mõõtühiku järk:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="d948d-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="d948d-186">See väli määratleb rea jaoks kehtiva mõõtühiku.</span><span class="sxs-lookup"><span data-stu-id="d948d-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="d948d-187">(Lisateavet leiate selle teema varasemast jaotisest [Ruumi leidmise mõõtühikute järkude seadistamine](#unit-tiers).)</span><span class="sxs-lookup"><span data-stu-id="d948d-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="d948d-188">**Määra ruumi kriteeriumid:** _Koguse kaalumine_</span><span class="sxs-lookup"><span data-stu-id="d948d-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="d948d-189">Sellel väljal on saadaval järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="d948d-190">**Tühja eeldamine** – see süsteem peaks eeldama, et kõik komplekteerimisala asukohad on tühjad ja neid ei tohiks kontrollida varudes.</span><span class="sxs-lookup"><span data-stu-id="d948d-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="d948d-191">**Koguse kaalumine** – see süsteem peaks kontrollima varusid komplekteerimisala asukohtades ja ei tohiks jätta vahele asukohti, mis pole tühjad.</span><span class="sxs-lookup"><span data-stu-id="d948d-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="d948d-192">**Korralduskood:** _Ruumi leidmine_</span><span class="sxs-lookup"><span data-stu-id="d948d-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="d948d-193">See väli määratleb asukohakorralduse, mida kasutatakse täiendamistöö komplekteerimise asukoha leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="d948d-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="d948d-194">**Ületäitumise asukoht:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="d948d-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="d948d-195">See väli määratleb asukoha, kuhu varud ladustatakse juhul, kui rea töötlemisel koguse asukohta ei leita.</span><span class="sxs-lookup"><span data-stu-id="d948d-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="d948d-196">**Luba loobumine:** _Jah_</span><span class="sxs-lookup"><span data-stu-id="d948d-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="d948d-197">Kui selle suvandi väärtuseks on seatud *Jah* , luuakse liikumise töö juhul, kui nõudlusele ei leita ruumi, et võtta varud välja asukohtadest, kus on varusid, kuid leitud ruumi ei kasutatud.</span><span class="sxs-lookup"><span data-stu-id="d948d-197">When this option is set to *Yes* , if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="d948d-198">Seejärel käivitatakse mall uuesti.</span><span class="sxs-lookup"><span data-stu-id="d948d-198">The template is then run again.</span></span> <span data-ttu-id="d948d-199">Seekord eirab see varusid asukohtades.</span><span class="sxs-lookup"><span data-stu-id="d948d-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="d948d-200">See funktsioon töötab kõige paremini siis, kui välja **Ruumi kriteeriumide määramine** on seatud _Koguse kaalumine_.</span><span class="sxs-lookup"><span data-stu-id="d948d-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="d948d-201">**Fikseeritud asukoha kasutus:** _Ainult selle toote fikseeritud asukohad_</span><span class="sxs-lookup"><span data-stu-id="d948d-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="d948d-202">Sellel väljal on saadaval järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="d948d-203">**Fikseeritud ja mittefikseeritud asukohad** – süsteem ei tohiks piirduda ainult fikseeritud asukohtade kasutamisega.</span><span class="sxs-lookup"><span data-stu-id="d948d-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="d948d-204">**Ainult selle toote fikseeritud asukohad** – süsteem peaks kasutama ainult nende asukohtade ruumi, mis on selle toote jaoks fikseeritud asukohad.</span><span class="sxs-lookup"><span data-stu-id="d948d-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="d948d-205">**Ainult selle tootevariandi fikseeritud asukohad** – süsteem peaks kasutama ainult nende asukohtade ruumi, mis on selle tootevariandi jaoks fikseeritud asukohad.</span><span class="sxs-lookup"><span data-stu-id="d948d-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="d948d-206">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d948d-206">Select **Save**.</span></span>
1. <span data-ttu-id="d948d-207">Teise malli rea loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d948d-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="d948d-208">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d948d-209">**Järjestus:** _2_</span><span class="sxs-lookup"><span data-stu-id="d948d-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="d948d-210">**Kirjeldus:** _Muu_</span><span class="sxs-lookup"><span data-stu-id="d948d-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="d948d-211">**Minimaalne kogus:** _1_</span><span class="sxs-lookup"><span data-stu-id="d948d-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="d948d-212">**Maksimaalne kogus:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="d948d-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="d948d-213">**Ühik:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="d948d-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="d948d-214">**Mõõtühiku järk:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="d948d-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="d948d-215">**Määra ruumi kriteeriumid:** _Koguse kaalumine_</span><span class="sxs-lookup"><span data-stu-id="d948d-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="d948d-216">**Korralduskood:** _Ruumi leidmine_</span><span class="sxs-lookup"><span data-stu-id="d948d-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="d948d-217">**Ületäitumise asukoht:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="d948d-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="d948d-218">**Luba loobumine:** _Jah_</span><span class="sxs-lookup"><span data-stu-id="d948d-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="d948d-219">**Fikseeritud asukohtade kasutamine:** _Fikseeritud ja mittefikseeritud asukohad_</span><span class="sxs-lookup"><span data-stu-id="d948d-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="d948d-220">Teise rea päringus saate nüüd määrata kriteeriumid, mille alusel määratletakse, millistest asukohtadest selle rea nõudlusele saab ruumi leida.</span><span class="sxs-lookup"><span data-stu-id="d948d-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="d948d-221">Otsige üles rida, kus välja **Järjestus** väärtuseks on seatud *2*.</span><span class="sxs-lookup"><span data-stu-id="d948d-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="d948d-222">Valige **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="d948d-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="d948d-223">Vahekaardil **Vahemik** valige käsk **Lisa** , et lisada uus rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="d948d-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="d948d-224">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d948d-225">**Tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="d948d-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="d948d-226">**Tuletatud tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="d948d-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="d948d-227">**Väli:** *Asukohaprofiili ID*</span><span class="sxs-lookup"><span data-stu-id="d948d-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="d948d-228">**Kriteeriumid:** *Pick-06* (valige väljal kahekordne plussmärk \[**++**\] loendi laiendamiseks ja seejärel valige *Pick-06* - *Komplekteerimissait 6*.)</span><span class="sxs-lookup"><span data-stu-id="d948d-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="d948d-229">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d948d-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="d948d-230">Asukohakorralduste häälestamine</span><span class="sxs-lookup"><span data-stu-id="d948d-230">Set up location directives</span></span>

<span data-ttu-id="d948d-231">Vähemalt üks asukohakorraldus peab olema seadistatud, et toetada ruumi leidmise valikuid.</span><span class="sxs-lookup"><span data-stu-id="d948d-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="d948d-232">Kasutage selles jaotises olevaid protseduure uue *täiendamise asukohakorralduse* seadistamiseks ruumi leidmise valikute tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="d948d-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="d948d-233">Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.</span><span class="sxs-lookup"><span data-stu-id="d948d-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d948d-234">Valige vasakpoolse paani väljal **Töökäsu tüüp** suvand *Täiendamine*.</span><span class="sxs-lookup"><span data-stu-id="d948d-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="d948d-235">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d948d-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d948d-236">Sisestage uue asukohakorralduse päise väljale **Nimi** väärtus *61 ruumi leidmise komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="d948d-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="d948d-237">Asukohakorralduste kiirkaardi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d948d-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="d948d-238">Määrake kiirkaardil **Asukohakorraldused** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="d948d-239">Võtke vastu vaikeväärtused kõigil teistel väljadel.</span><span class="sxs-lookup"><span data-stu-id="d948d-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="d948d-240">**Töö tüüp:** _Komplekteerimine_</span><span class="sxs-lookup"><span data-stu-id="d948d-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="d948d-241">**Tegevuskoht:** _6_</span><span class="sxs-lookup"><span data-stu-id="d948d-241">**Site:** _6_</span></span>
    - <span data-ttu-id="d948d-242">**Ladu:** _61_</span><span class="sxs-lookup"><span data-stu-id="d948d-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="d948d-243">**Korralduskood:** _Ruumi leidmine_</span><span class="sxs-lookup"><span data-stu-id="d948d-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="d948d-244">Valige **Salvesta** , et muuta kiirkaart **Read** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="d948d-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="d948d-245">Ridade kiirkaardi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d948d-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="d948d-246">Rea loomiseks valige kiirkaardil **Read** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d948d-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="d948d-247">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-247">On the new line, set the following values.</span></span> <span data-ttu-id="d948d-248">Võtke vastu vaikeväärtused kõigil teistel väljadel.</span><span class="sxs-lookup"><span data-stu-id="d948d-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="d948d-249">**Alates kogusest:** _0_</span><span class="sxs-lookup"><span data-stu-id="d948d-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="d948d-250">**Koguseni:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="d948d-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="d948d-251">Valige **Salvesta** , et muuta kiirkaart **Asukohakorralduse toimingud** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="d948d-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="d948d-252">Asukohakorralduste tegevuste kiirkaardi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d948d-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="d948d-253">Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus** , et luua rida.</span><span class="sxs-lookup"><span data-stu-id="d948d-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="d948d-254">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-254">On the new line, set the following values.</span></span> <span data-ttu-id="d948d-255">Võtke vastu vaikeväärtused kõigil teistel väljadel.</span><span class="sxs-lookup"><span data-stu-id="d948d-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="d948d-256">**Nimi:** _Hulgi_</span><span class="sxs-lookup"><span data-stu-id="d948d-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="d948d-257">**Strateegia:** _Puudub_</span><span class="sxs-lookup"><span data-stu-id="d948d-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="d948d-258">Valige **Salvesta** , et muuta nupp **Päringu redigeerimine** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="d948d-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="d948d-259">Redigeeri päringut</span><span class="sxs-lookup"><span data-stu-id="d948d-259">Edit the query</span></span>

1. <span data-ttu-id="d948d-260">Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="d948d-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="d948d-261">Vahekaardil **Vahemik** valige käsk **Lisa** , et lisada uus rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="d948d-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="d948d-262">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d948d-263">**Tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="d948d-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="d948d-264">**Tuletatud tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="d948d-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="d948d-265">**Väli:** *Tsooni ID*</span><span class="sxs-lookup"><span data-stu-id="d948d-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="d948d-266">**Kriteeriumid:** *Hulgi* (valige väljal kahekordne plussmärk \[**++**\] loendi laiendamiseks ja seejärel valige *Hulgi*.)</span><span class="sxs-lookup"><span data-stu-id="d948d-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="d948d-267">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d948d-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="d948d-268">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="d948d-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="d948d-269">Stsenaariumi seadistamine</span><span class="sxs-lookup"><span data-stu-id="d948d-269">Set up the scenario</span></span>

<span data-ttu-id="d948d-270">Selle stsenaariumi puhul saate kasutada sisseehitatud näidisandmeid ja luua selles jaotises kirjeldatud kirjeid.</span><span class="sxs-lookup"><span data-stu-id="d948d-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="d948d-271">USMF-näidisandmete kasutamine</span><span class="sxs-lookup"><span data-stu-id="d948d-271">Use the USMF sample data</span></span>

<span data-ttu-id="d948d-272">Selle stsenaariumi kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="d948d-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="d948d-273">Enne alustamist peate valima ka juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="d948d-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="d948d-274">Nõudluse loomine</span><span class="sxs-lookup"><span data-stu-id="d948d-274">Create demand</span></span>

<span data-ttu-id="d948d-275">Järgige neid etappe nõudluse loomiseks, millele soovite ruumi leidmist rakendada.</span><span class="sxs-lookup"><span data-stu-id="d948d-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="d948d-276">Avage jaotis **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="d948d-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="d948d-277">Müügitellimuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d948d-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="d948d-278">Valige dialoogiboksi **Müügitellimuse loomine** väljal **Kliendi konto** suvand _US-007_.</span><span class="sxs-lookup"><span data-stu-id="d948d-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="d948d-279">Valige väljal **Ladu** väärtus _61_.</span><span class="sxs-lookup"><span data-stu-id="d948d-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="d948d-280">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d948d-280">Select **OK**.</span></span>
1. <span data-ttu-id="d948d-281">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="d948d-281">The new sales order is opened.</span></span> <span data-ttu-id="d948d-282">See lisab uue tühja rea kiirkaardil **Müügitellimuse read**.</span><span class="sxs-lookup"><span data-stu-id="d948d-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d948d-283">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="d948d-284">**Kaup:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="d948d-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="d948d-285">**Kogus:** _20_</span><span class="sxs-lookup"><span data-stu-id="d948d-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="d948d-286">Valige **Lisa rida** , et lisada uus rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="d948d-287">**Kaup:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="d948d-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="d948d-288">**Kogus:** _8_</span><span class="sxs-lookup"><span data-stu-id="d948d-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="d948d-289">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d948d-289">Select **Save**.</span></span>
1. <span data-ttu-id="d948d-290">Teise müügitellimuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d948d-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="d948d-291">Valige dialoogiboksi **Müügitellimuse loomine** väljal **Kliendi konto** suvand _US-008_.</span><span class="sxs-lookup"><span data-stu-id="d948d-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="d948d-292">Valige väljal **Ladu** väärtus _61_.</span><span class="sxs-lookup"><span data-stu-id="d948d-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="d948d-293">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="d948d-293">The new sales order is opened.</span></span> <span data-ttu-id="d948d-294">See lisab uue tühja rea kiirkaardil **Müügitellimuse read**.</span><span class="sxs-lookup"><span data-stu-id="d948d-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d948d-295">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d948d-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="d948d-296">**Kaup:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="d948d-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="d948d-297">**Kogus:** _1_</span><span class="sxs-lookup"><span data-stu-id="d948d-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="d948d-298">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d948d-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="d948d-299">Tavalise ruumi leidmise stsenaariumi ülevaade</span><span class="sxs-lookup"><span data-stu-id="d948d-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="d948d-300">Kui kõik eeltingimuseks olevad elemendid on eelmise jaotise kirjelduste järgi paigas, olete valmis funktsiooni proovima, tehes läbi kõik selles jaotises olevad harjutused.</span><span class="sxs-lookup"><span data-stu-id="d948d-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="d948d-301">Loo nõudlus</span><span class="sxs-lookup"><span data-stu-id="d948d-301">Generate demand</span></span>

1. <span data-ttu-id="d948d-302">Avage jaotis **Laohaldus \> Seadistus \> Täiendamine \> Ruumi leidmise mallid** ja valige eelnevalt loodud ruumi leidmise mall.</span><span class="sxs-lookup"><span data-stu-id="d948d-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates** , and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="d948d-303">Valige toimingupaanil **Loo nõudlus**.</span><span class="sxs-lookup"><span data-stu-id="d948d-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="d948d-304">See käsk hindab kõiki süsteemis olevaid nõudlusi, mis ühtivad ruumi leidmise malli päringuga.</span><span class="sxs-lookup"><span data-stu-id="d948d-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="d948d-305">Kõigi tellimuste kõik nõudlused konsolideeritakse seejärel ühele reale koguse/mõõtühiku kohta.</span><span class="sxs-lookup"><span data-stu-id="d948d-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="d948d-306">Kui protsess on lõpule viidud, kuvatakse teade.</span><span class="sxs-lookup"><span data-stu-id="d948d-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="d948d-307">Ruumi leidmise nõudlus</span><span class="sxs-lookup"><span data-stu-id="d948d-307">Slotting demand</span></span>

<span data-ttu-id="d948d-308">*Ruumi leidmise nõudlus* kuvab nõudluse loomise tulemused ruumi leidmise malli seadistuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="d948d-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="d948d-309">Valige toimingupaanil **Ruumi leidmise nõudlus** , et kuvada käsu **Loo nõudlus** tulemusi.</span><span class="sxs-lookup"><span data-stu-id="d948d-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="d948d-310">Ruumi leidmise nõudluse ridu saab redigeerida.</span><span class="sxs-lookup"><span data-stu-id="d948d-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="d948d-311">Saate kustutada rea, lisada uue rea või redigeerida rea üksikasju.</span><span class="sxs-lookup"><span data-stu-id="d948d-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="d948d-312">Saate redigeerida nõudlust käsitsi või importida selle andmehalduse abil välisest süsteemist.</span><span class="sxs-lookup"><span data-stu-id="d948d-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="d948d-313">Ruumi leidmise nõudluses olevat kasutatakse järgmises etapis, olenemata selle päritolust.</span><span class="sxs-lookup"><span data-stu-id="d948d-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="d948d-314">Nõudluse leidmine</span><span class="sxs-lookup"><span data-stu-id="d948d-314">Locate demand</span></span>

<span data-ttu-id="d948d-315">Kui nõudlus on loodud, peate käsu **Otsi nõudlust** abil looma *ruumi leidmise plaani*.</span><span class="sxs-lookup"><span data-stu-id="d948d-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="d948d-316">Valige toimingupaanil **Otsi nõudlust**.</span><span class="sxs-lookup"><span data-stu-id="d948d-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="d948d-317">Ruumi leidmise protsess töötab.</span><span class="sxs-lookup"><span data-stu-id="d948d-317">The slotting process runs.</span></span> <span data-ttu-id="d948d-318">Kui protsess on lõpule viidud, kuvatakse teade.</span><span class="sxs-lookup"><span data-stu-id="d948d-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="d948d-319">Ruumi leidmise plaan</span><span class="sxs-lookup"><span data-stu-id="d948d-319">Slotting plan</span></span>

<span data-ttu-id="d948d-320">Ruumi leidmise plaan kuvab asukohta, kuhu iga kaup/kogus määrati, kas kasutati ületäitumist, kas loodi loobumistöö ja kasutatud malli rida.</span><span class="sxs-lookup"><span data-stu-id="d948d-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="d948d-321">**Kõik nõudlused, millele ruumi ei leitud, on punasega esile tõstetud.**</span><span class="sxs-lookup"><span data-stu-id="d948d-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="d948d-322">Valige toimingupaanil **Ruumi leidmise plaan** tulemuste kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="d948d-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="d948d-323">Täiendamise loomine</span><span class="sxs-lookup"><span data-stu-id="d948d-323">Create replenishment</span></span>

<span data-ttu-id="d948d-324">Kui ruumi leidmise plaan on loodud, peate selle plaani põhjal looma *täiendamise töö*.</span><span class="sxs-lookup"><span data-stu-id="d948d-324">After the slotting plan has been created, you must create *replenishment work* , based on the plan.</span></span>

- <span data-ttu-id="d948d-325">Valige tegevuste paanil käsk **Käivita täiendamine**.</span><span class="sxs-lookup"><span data-stu-id="d948d-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="d948d-326">Kui protsess on lõpule viidud, kuvatakse teade.</span><span class="sxs-lookup"><span data-stu-id="d948d-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="d948d-327">See teade näitab tööjärgu ID jaoks loodud päiste arvu.</span><span class="sxs-lookup"><span data-stu-id="d948d-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="d948d-328">Kasutatavad asukohakorraldused tuvastatakse igale malli reale määratud korralduskoodi alusel.</span><span class="sxs-lookup"><span data-stu-id="d948d-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="d948d-329">Näpunäited</span><span class="sxs-lookup"><span data-stu-id="d948d-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="d948d-330">Automaatse ruumi leidmise seadistamine</span><span class="sxs-lookup"><span data-stu-id="d948d-330">Set up automatic slotting</span></span>

<span data-ttu-id="d948d-331">Kui kõik vajalikud elemendid on paigas, saate häälestada ruumi leidmise automaatse käivitamise nende etappide abil.</span><span class="sxs-lookup"><span data-stu-id="d948d-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="d948d-332">Avage jaotis **Laohaldus \> Täiendamine \> Käivita ruumi leidmine**.</span><span class="sxs-lookup"><span data-stu-id="d948d-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="d948d-333">Määrake käivitatavad ruumi leidmise etapid.</span><span class="sxs-lookup"><span data-stu-id="d948d-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="d948d-334">Valige vähemalt üks järgmistest ruumi leidmise etappidest.</span><span class="sxs-lookup"><span data-stu-id="d948d-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="d948d-335">Loo nõudlus</span><span class="sxs-lookup"><span data-stu-id="d948d-335">Generate demand</span></span>
    - <span data-ttu-id="d948d-336">Nõudluse leidmine</span><span class="sxs-lookup"><span data-stu-id="d948d-336">Locate demand</span></span>
    - <span data-ttu-id="d948d-337">Täiendustöö loomine</span><span class="sxs-lookup"><span data-stu-id="d948d-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="d948d-338">Ruumi leidmise etapid on progresseeruvad.</span><span class="sxs-lookup"><span data-stu-id="d948d-338">The slotting steps are progressive.</span></span> <span data-ttu-id="d948d-339">Kui soovite valida suvandit *Otsi nõudlust* , peate esmalt valima *Loo nõudlus*.</span><span class="sxs-lookup"><span data-stu-id="d948d-339">If you want to select *Locate demand* , you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="d948d-340">Määrake kasutatav ruumi leidmise mall.</span><span class="sxs-lookup"><span data-stu-id="d948d-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="d948d-341">Soovi korral saate määrata kordumise automaatselt käivituma.</span><span class="sxs-lookup"><span data-stu-id="d948d-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="d948d-342">Selle stsenaariumi harjutuste jaoks **ärge** seadistage automaatset ruumi leidmist.</span><span class="sxs-lookup"><span data-stu-id="d948d-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
