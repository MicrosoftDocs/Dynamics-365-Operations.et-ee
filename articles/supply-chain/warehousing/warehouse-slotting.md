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
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f6764f8bc082962af37d4775b6fe53d8704658eb
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597454"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="dd5d9-105">Lao ruumi leidmine</span><span class="sxs-lookup"><span data-stu-id="dd5d9-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd5d9-106">Lao ruumi leidmise abil saate konsolideerida nõudlust kauba ja mõõtühiku järgi tellimustest, mille olek on *Tellitud*, *Reserveeritud* või *Väljastatud*.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="dd5d9-107">Loodud nõudlust saab seejärel rakendada asukohtadele, mida kasutatakse koguse, ühiku, füüsiliste dimensioonide, fikseeritud asukohtade ja muu alusel komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="dd5d9-108">Pärast seda, kui ruumi leidmise plaan on loodud, saab luua täiendamise töö, et tuua igasse asukohta sobiv kogus varusid.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="dd5d9-109">See funktsioon aitab laohalduritel nutikalt planeerida komplekteerimise asukohti enne tellimuse lattu väljatamist ja komplekteerimistöö loomist.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="dd5d9-110">Lao ruumi leidmise funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="dd5d9-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="dd5d9-111">Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="dd5d9-112">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="dd5d9-113">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="dd5d9-114">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="dd5d9-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="dd5d9-115">**Funktsiooni nimi** *Lao ruumi leidmise funktsioon*</span><span class="sxs-lookup"><span data-stu-id="dd5d9-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="dd5d9-116">Lao ruumi leidmise seadistamine</span><span class="sxs-lookup"><span data-stu-id="dd5d9-116">Set up warehouse slotting</span></span>

<span data-ttu-id="dd5d9-117">Lao ruumi leidmise kasutamiseks peate seadistama järgmised elemendid oma süsteemis.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="dd5d9-118">Mõõtühikute järkude loomine ruumi leidmise jaoks</span><span class="sxs-lookup"><span data-stu-id="dd5d9-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="dd5d9-119">Mõõtühikute järgud võimaldavad mitme mõõtühiku grupeerimist ruumi leidmise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="dd5d9-120">Näiteks kui erineva suurusega kaste komplekteeritakse samalt kastide komplekteerimise alalt, saab iga suuruse jaoks luua ühe järgu.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="dd5d9-121">**Iga mõõtühiku jaoksa tuleb luua rida, mis on selle järgu osa.**</span><span class="sxs-lookup"><span data-stu-id="dd5d9-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="dd5d9-122">Avage jaotis **Laohaldus \> Häälestus \> Täiendamine \> Ruumi leidmise mõõtühikute järgud**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="dd5d9-123">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-123">Select **New**.</span></span>
1. <span data-ttu-id="dd5d9-124">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="dd5d9-125">**Mõõtühiku järk:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="dd5d9-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="dd5d9-126">**Kirjeldus:** *Iga kasti kaubaalus*</span><span class="sxs-lookup"><span data-stu-id="dd5d9-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="dd5d9-127">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-127">Select **Save**.</span></span>
1. <span data-ttu-id="dd5d9-128">Valige kiirkaardil **Mõõtühikud** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="dd5d9-129">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dd5d9-130">**Ühik:** *Kast*</span><span class="sxs-lookup"><span data-stu-id="dd5d9-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="dd5d9-131">**Kirjeldus:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="dd5d9-132">See täidetakse muudatuste salvestamisel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="dd5d9-133">**Ühiku klass:** *Kogus*</span><span class="sxs-lookup"><span data-stu-id="dd5d9-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="dd5d9-134">Klõpsake valikut **Uus**, et lisada ruudustikku teine rida.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="dd5d9-135">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dd5d9-136">**Ühik:** *ea*</span><span class="sxs-lookup"><span data-stu-id="dd5d9-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="dd5d9-137">**Kirjeldus:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="dd5d9-138">See täidetakse muudatuste salvestamisel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="dd5d9-139">**Ühiku klass:** *Kogus*</span><span class="sxs-lookup"><span data-stu-id="dd5d9-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="dd5d9-140">Klõpsake valikut **Uus**, et lisada ruudustikku kolmas rida.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="dd5d9-141">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dd5d9-142">**Ühik:** *PL*</span><span class="sxs-lookup"><span data-stu-id="dd5d9-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="dd5d9-143">**Kirjeldus:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="dd5d9-144">See täidetakse muudatuste salvestamisel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="dd5d9-145">**Ühiku klass:** *Kogus*</span><span class="sxs-lookup"><span data-stu-id="dd5d9-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="dd5d9-146">Järgu salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="dd5d9-147">Korralduskoodi loomine ruumi leidmiseks</span><span class="sxs-lookup"><span data-stu-id="dd5d9-147">Create a directive code for slotting</span></span>

<span data-ttu-id="dd5d9-148">Peate valima korralduskoodi, mis tuleks malliga seostada.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="dd5d9-149">Avage jaotis **Laohaldus \> Seadistus \> Korralduskoodid**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="dd5d9-150">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dd5d9-151">Sisestage väljale **Korralduskood** väärtus *Ruumi leidmine*.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="dd5d9-152">Sisestage väljale **Korralduse kirjeldus** väärtus *Ruumi leidmine*.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="dd5d9-153">Ruumi leidmise mallide seadistamine</span><span class="sxs-lookup"><span data-stu-id="dd5d9-153">Set up slotting templates</span></span>

<span data-ttu-id="dd5d9-154">Iga ruumi leidmise mall juhib seda, kuidas kindla lao asukohtade jaoks määratakse varusid.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="dd5d9-155">Iga mall peab sisaldama rida iga ruumi leidmise täpsustuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="dd5d9-156">Kasutage selle jaotise protseduure, et häälestada ruumi leidmise malle.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="dd5d9-157">Avage jaotis **Laohaldus \> Seadistus \> Täiendamine \> Ruumi leidmise mallid**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="dd5d9-158">Valige malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-158">Select **New** to create a template.</span></span>

<span data-ttu-id="dd5d9-159">Järgmisena peate seadistama malli päise, ruumi leidmise kirjelduse ja asukohakorraldused järgmistes alamjaotistes kirjeldatud juhiste järgi.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="dd5d9-160">Ruumi leidmise malli päise seadistamine</span><span class="sxs-lookup"><span data-stu-id="dd5d9-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="dd5d9-161">Määrake malli päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="dd5d9-162">**Ruumi leidmise mall:** _61_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="dd5d9-163">**Kirjeldus:** _61_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-163">**Description:** _61_</span></span>
    - <span data-ttu-id="dd5d9-164">**Nõudluse tüüp:** *Müügitellimus*</span><span class="sxs-lookup"><span data-stu-id="dd5d9-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="dd5d9-165">Praegu on *Müügitellimus* ainus toetatud nõudluse tüüp.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="dd5d9-166">**Nõudluse strateegia:** _Tellitud_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="dd5d9-167">Sellel väljal on saadaval järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="dd5d9-168">**Tellitud** – müügitellimuse täielikku tellitud kogust tuleks arvestada nõudlusena.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="dd5d9-169">**Reserveeritud** – ainult reserveeritud müügitellimuse rea (füüsilised ja tellitud) koguseid tuleks arvestada nõudlusena.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="dd5d9-170">**Ladu:** _61_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="dd5d9-171">**Luba voo nõudmisel kasutada reserveerimata koguseid:** _Jah_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="dd5d9-172">Samuti saate määrata päringu hinnatava nõudluse ulatuse kitsendamiseks.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="dd5d9-173">Ruumi leidmise täpsustuste seadistamine iga malli jaoks</span><span class="sxs-lookup"><span data-stu-id="dd5d9-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="dd5d9-174">Iga loodava malli jaoks järgige neid etappe, et lisada rida iga ruumi leidmise täpsustuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="dd5d9-175">Valige kiirkaardil **Ruumi leidmise malli üksikasjad** suvand **Uus**, et luua malli rida.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="dd5d9-176">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dd5d9-177">**Järjestus:** _1_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="dd5d9-178">**Kirjeldus:** _Fikseeritud asukoht_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="dd5d9-179">**Minimaalne kogus:** _1_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="dd5d9-180">See väli määratleb rea jaoks nõutava minimaalse koguse.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="dd5d9-181">**Maksimaalne kogus:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="dd5d9-182">See väli määratleb rea jaoks kehtiva maksimaalse koguse.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="dd5d9-183">**Ühik:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="dd5d9-184">See väli määratleb mõõtühiku, millele minimaalne ja maksimaalne kogus viitab.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="dd5d9-185">**Mõõtühiku järk:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="dd5d9-186">See väli määratleb rea jaoks kehtiva mõõtühiku.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="dd5d9-187">(Lisateavet leiate selle teema varasemast jaotisest [Ruumi leidmise mõõtühikute järkude seadistamine](#unit-tiers).)</span><span class="sxs-lookup"><span data-stu-id="dd5d9-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="dd5d9-188">**Määra ruumi kriteeriumid:** _Koguse kaalumine_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="dd5d9-189">Sellel väljal on saadaval järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="dd5d9-190">**Tühja eeldamine** – see süsteem peaks eeldama, et kõik komplekteerimisala asukohad on tühjad ja neid ei tohiks kontrollida varudes.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="dd5d9-191">**Koguse kaalumine** – see süsteem peaks kontrollima varusid komplekteerimisala asukohtades ja ei tohiks jätta vahele asukohti, mis pole tühjad.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="dd5d9-192">**Korralduskood:** _Ruumi leidmine_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="dd5d9-193">See väli määratleb asukohakorralduse, mida kasutatakse täiendamistöö komplekteerimise asukoha leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="dd5d9-194">**Ületäitumise asukoht:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="dd5d9-195">See väli määratleb asukoha, kuhu varud ladustatakse juhul, kui rea töötlemisel koguse asukohta ei leita.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="dd5d9-196">**Luba loobumine:** _Jah_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="dd5d9-197">Kui selle suvandi väärtuseks on seatud *Jah*, luuakse liikumise töö juhul, kui nõudlusele ei leita ruumi, et võtta varud välja asukohtadest, kus on varusid, kuid leitud ruumi ei kasutatud.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-197">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="dd5d9-198">Seejärel käivitatakse mall uuesti.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-198">The template is then run again.</span></span> <span data-ttu-id="dd5d9-199">Seekord eirab see varusid asukohtades.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="dd5d9-200">See funktsioon töötab kõige paremini siis, kui välja **Ruumi kriteeriumide määramine** on seatud _Koguse kaalumine_.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="dd5d9-201">**Fikseeritud asukoha kasutus:** _Ainult selle toote fikseeritud asukohad_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="dd5d9-202">Sellel väljal on saadaval järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="dd5d9-203">**Fikseeritud ja mittefikseeritud asukohad** – süsteem ei tohiks piirduda ainult fikseeritud asukohtade kasutamisega.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="dd5d9-204">**Ainult selle toote fikseeritud asukohad** – süsteem peaks kasutama ainult nende asukohtade ruumi, mis on selle toote jaoks fikseeritud asukohad.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="dd5d9-205">**Ainult selle tootevariandi fikseeritud asukohad** – süsteem peaks kasutama ainult nende asukohtade ruumi, mis on selle tootevariandi jaoks fikseeritud asukohad.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="dd5d9-206">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-206">Select **Save**.</span></span>
1. <span data-ttu-id="dd5d9-207">Teise malli rea loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="dd5d9-208">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dd5d9-209">**Järjestus:** _2_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="dd5d9-210">**Kirjeldus:** _Muu_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="dd5d9-211">**Minimaalne kogus:** _1_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="dd5d9-212">**Maksimaalne kogus:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="dd5d9-213">**Ühik:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="dd5d9-214">**Mõõtühiku järk:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="dd5d9-215">**Määra ruumi kriteeriumid:** _Koguse kaalumine_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="dd5d9-216">**Korralduskood:** _Ruumi leidmine_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="dd5d9-217">**Ületäitumise asukoht:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="dd5d9-218">**Luba loobumine:** _Jah_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="dd5d9-219">**Fikseeritud asukohtade kasutamine:** _Fikseeritud ja mittefikseeritud asukohad_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="dd5d9-220">Teise rea päringus saate nüüd määrata kriteeriumid, mille alusel määratletakse, millistest asukohtadest selle rea nõudlusele saab ruumi leida.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="dd5d9-221">Otsige üles rida, kus välja **Järjestus** väärtuseks on seatud *2*.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="dd5d9-222">Valige **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="dd5d9-223">Vahekaardil **Vahemik** valige käsk **Lisa**, et lisada uus rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="dd5d9-224">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dd5d9-225">**Tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="dd5d9-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="dd5d9-226">**Tuletatud tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="dd5d9-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="dd5d9-227">**Väli:** *Asukohaprofiili ID*</span><span class="sxs-lookup"><span data-stu-id="dd5d9-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="dd5d9-228">**Kriteeriumid:** *Pick-06* (valige väljal kahekordne plussmärk \[**++**\] loendi laiendamiseks ja seejärel valige *Pick-06* - *Komplekteerimissait 6*.)</span><span class="sxs-lookup"><span data-stu-id="dd5d9-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="dd5d9-229">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="dd5d9-230">Asukohakorralduste häälestamine</span><span class="sxs-lookup"><span data-stu-id="dd5d9-230">Set up location directives</span></span>

<span data-ttu-id="dd5d9-231">Vähemalt üks asukohakorraldus peab olema seadistatud, et toetada ruumi leidmise valikuid.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="dd5d9-232">Kasutage selles jaotises olevaid protseduure uue *täiendamise asukohakorralduse* seadistamiseks ruumi leidmise valikute tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="dd5d9-233">Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="dd5d9-234">Valige vasakpoolse paani väljal **Töökäsu tüüp** suvand *Täiendamine*.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="dd5d9-235">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dd5d9-236">Sisestage uue asukohakorralduse päise väljale **Nimi** väärtus *61 ruumi leidmise komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="dd5d9-237">Asukohakorralduste kiirkaardi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="dd5d9-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="dd5d9-238">Määrake kiirkaardil **Asukohakorraldused** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="dd5d9-239">Võtke vastu vaikeväärtused kõigil teistel väljadel.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="dd5d9-240">**Töö tüüp:** _Komplekteerimine_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="dd5d9-241">**Tegevuskoht:** _6_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-241">**Site:** _6_</span></span>
    - <span data-ttu-id="dd5d9-242">**Ladu:** _61_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="dd5d9-243">**Korralduskood:** _Ruumi leidmine_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="dd5d9-244">Valige **Salvesta**, et muuta kiirkaart **Read** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="dd5d9-245">Ridade kiirkaardi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="dd5d9-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="dd5d9-246">Rea loomiseks valige kiirkaardil **Read** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="dd5d9-247">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-247">On the new line, set the following values.</span></span> <span data-ttu-id="dd5d9-248">Võtke vastu vaikeväärtused kõigil teistel väljadel.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="dd5d9-249">**Alates kogusest:** _0_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="dd5d9-250">**Koguseni:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="dd5d9-251">Valige **Salvesta**, et muuta kiirkaart **Asukohakorralduse toimingud** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="dd5d9-252">Asukohakorralduste tegevuste kiirkaardi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="dd5d9-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="dd5d9-253">Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus**, et luua rida.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="dd5d9-254">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-254">On the new line, set the following values.</span></span> <span data-ttu-id="dd5d9-255">Võtke vastu vaikeväärtused kõigil teistel väljadel.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="dd5d9-256">**Nimi:** _Hulgi_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="dd5d9-257">**Strateegia:** _Puudub_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="dd5d9-258">Valige **Salvesta**, et muuta nupp **Päringu redigeerimine** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="dd5d9-259">Redigeeri päringut</span><span class="sxs-lookup"><span data-stu-id="dd5d9-259">Edit the query</span></span>

1. <span data-ttu-id="dd5d9-260">Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="dd5d9-261">Vahekaardil **Vahemik** valige käsk **Lisa**, et lisada uus rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="dd5d9-262">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="dd5d9-263">**Tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="dd5d9-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="dd5d9-264">**Tuletatud tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="dd5d9-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="dd5d9-265">**Väli:** *Tsooni ID*</span><span class="sxs-lookup"><span data-stu-id="dd5d9-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="dd5d9-266">**Kriteeriumid:** *Hulgi* (valige väljal kahekordne plussmärk \[**++**\] loendi laiendamiseks ja seejärel valige *Hulgi*.)</span><span class="sxs-lookup"><span data-stu-id="dd5d9-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="dd5d9-267">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="dd5d9-268">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="dd5d9-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="dd5d9-269">Stsenaariumi seadistamine</span><span class="sxs-lookup"><span data-stu-id="dd5d9-269">Set up the scenario</span></span>

<span data-ttu-id="dd5d9-270">Selle stsenaariumi puhul saate kasutada sisseehitatud näidisandmeid ja luua selles jaotises kirjeldatud kirjeid.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="dd5d9-271">USMF-näidisandmete kasutamine</span><span class="sxs-lookup"><span data-stu-id="dd5d9-271">Use the USMF sample data</span></span>

<span data-ttu-id="dd5d9-272">Selle stsenaariumi kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="dd5d9-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="dd5d9-273">Enne alustamist peate valima ka juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="dd5d9-274">Nõudluse loomine</span><span class="sxs-lookup"><span data-stu-id="dd5d9-274">Create demand</span></span>

<span data-ttu-id="dd5d9-275">Järgige neid etappe nõudluse loomiseks, millele soovite ruumi leidmist rakendada.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="dd5d9-276">Avage jaotis **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="dd5d9-277">Müügitellimuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="dd5d9-278">Valige dialoogiboksi **Müügitellimuse loomine** väljal **Kliendi konto** suvand _US-007_.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="dd5d9-279">Valige väljal **Ladu** väärtus _61_.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="dd5d9-280">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-280">Select **OK**.</span></span>
1. <span data-ttu-id="dd5d9-281">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-281">The new sales order is opened.</span></span> <span data-ttu-id="dd5d9-282">See lisab uue tühja rea kiirkaardil **Müügitellimuse read**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="dd5d9-283">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="dd5d9-284">**Kaup:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="dd5d9-285">**Kogus:** _20_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="dd5d9-286">Valige **Lisa rida**, et lisada uus rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="dd5d9-287">**Kaup:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="dd5d9-288">**Kogus:** _8_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="dd5d9-289">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-289">Select **Save**.</span></span>
1. <span data-ttu-id="dd5d9-290">Teise müügitellimuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="dd5d9-291">Valige dialoogiboksi **Müügitellimuse loomine** väljal **Kliendi konto** suvand _US-008_.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="dd5d9-292">Valige väljal **Ladu** väärtus _61_.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="dd5d9-293">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-293">The new sales order is opened.</span></span> <span data-ttu-id="dd5d9-294">See lisab uue tühja rea kiirkaardil **Müügitellimuse read**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="dd5d9-295">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="dd5d9-296">**Kaup:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="dd5d9-297">**Kogus:** _1_</span><span class="sxs-lookup"><span data-stu-id="dd5d9-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="dd5d9-298">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="dd5d9-299">Tavalise ruumi leidmise stsenaariumi ülevaade</span><span class="sxs-lookup"><span data-stu-id="dd5d9-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="dd5d9-300">Kui kõik eeltingimuseks olevad elemendid on eelmise jaotise kirjelduste järgi paigas, olete valmis funktsiooni proovima, tehes läbi kõik selles jaotises olevad harjutused.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="dd5d9-301">Loo nõudlus</span><span class="sxs-lookup"><span data-stu-id="dd5d9-301">Generate demand</span></span>

1. <span data-ttu-id="dd5d9-302">Avage jaotis **Laohaldus \> Seadistus \> Täiendamine \> Ruumi leidmise mallid** ja valige eelnevalt loodud ruumi leidmise mall.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="dd5d9-303">Valige toimingupaanil **Loo nõudlus**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="dd5d9-304">See käsk hindab kõiki süsteemis olevaid nõudlusi, mis ühtivad ruumi leidmise malli päringuga.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="dd5d9-305">Kõigi tellimuste kõik nõudlused konsolideeritakse seejärel ühele reale koguse/mõõtühiku kohta.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="dd5d9-306">Kui protsess on lõpule viidud, kuvatakse teade.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="dd5d9-307">Ruumi leidmise nõudlus</span><span class="sxs-lookup"><span data-stu-id="dd5d9-307">Slotting demand</span></span>

<span data-ttu-id="dd5d9-308">*Ruumi leidmise nõudlus* kuvab nõudluse loomise tulemused ruumi leidmise malli seadistuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="dd5d9-309">Valige toimingupaanil **Ruumi leidmise nõudlus**, et kuvada käsu **Loo nõudlus** tulemusi.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="dd5d9-310">Ruumi leidmise nõudluse ridu saab redigeerida.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="dd5d9-311">Saate kustutada rea, lisada uue rea või redigeerida rea üksikasju.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="dd5d9-312">Saate redigeerida nõudlust käsitsi või importida selle andmehalduse abil välisest süsteemist.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="dd5d9-313">Ruumi leidmise nõudluses olevat kasutatakse järgmises etapis, olenemata selle päritolust.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="dd5d9-314">Nõudluse leidmine</span><span class="sxs-lookup"><span data-stu-id="dd5d9-314">Locate demand</span></span>

<span data-ttu-id="dd5d9-315">Kui nõudlus on loodud, peate käsu **Otsi nõudlust** abil looma *ruumi leidmise plaani*.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="dd5d9-316">Valige toimingupaanil **Otsi nõudlust**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="dd5d9-317">Ruumi leidmise protsess töötab.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-317">The slotting process runs.</span></span> <span data-ttu-id="dd5d9-318">Kui protsess on lõpule viidud, kuvatakse teade.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="dd5d9-319">Ruumi leidmise plaan</span><span class="sxs-lookup"><span data-stu-id="dd5d9-319">Slotting plan</span></span>

<span data-ttu-id="dd5d9-320">Ruumi leidmise plaan kuvab asukohta, kuhu iga kaup/kogus määrati, kas kasutati ületäitumist, kas loodi loobumistöö ja kasutatud malli rida.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="dd5d9-321">**Kõik nõudlused, millele ruumi ei leitud, on punasega esile tõstetud.**</span><span class="sxs-lookup"><span data-stu-id="dd5d9-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="dd5d9-322">Valige toimingupaanil **Ruumi leidmise plaan** tulemuste kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="dd5d9-323">Täiendamise loomine</span><span class="sxs-lookup"><span data-stu-id="dd5d9-323">Create replenishment</span></span>

<span data-ttu-id="dd5d9-324">Kui ruumi leidmise plaan on loodud, peate selle plaani põhjal looma *täiendamise töö*.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-324">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="dd5d9-325">Valige tegevuste paanil käsk **Käivita täiendamine**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="dd5d9-326">Kui protsess on lõpule viidud, kuvatakse teade.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="dd5d9-327">See teade näitab tööjärgu ID jaoks loodud päiste arvu.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="dd5d9-328">Kasutatavad asukohakorraldused tuvastatakse igale malli reale määratud korralduskoodi alusel.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="dd5d9-329">Näpunäited</span><span class="sxs-lookup"><span data-stu-id="dd5d9-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="dd5d9-330">Automaatse ruumi leidmise seadistamine</span><span class="sxs-lookup"><span data-stu-id="dd5d9-330">Set up automatic slotting</span></span>

<span data-ttu-id="dd5d9-331">Kui kõik vajalikud elemendid on paigas, saate häälestada ruumi leidmise automaatse käivitamise nende etappide abil.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="dd5d9-332">Avage jaotis **Laohaldus \> Täiendamine \> Käivita ruumi leidmine**.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="dd5d9-333">Määrake käivitatavad ruumi leidmise etapid.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="dd5d9-334">Valige vähemalt üks järgmistest ruumi leidmise etappidest.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="dd5d9-335">Loo nõudlus</span><span class="sxs-lookup"><span data-stu-id="dd5d9-335">Generate demand</span></span>
    - <span data-ttu-id="dd5d9-336">Nõudluse leidmine</span><span class="sxs-lookup"><span data-stu-id="dd5d9-336">Locate demand</span></span>
    - <span data-ttu-id="dd5d9-337">Täiendustöö loomine</span><span class="sxs-lookup"><span data-stu-id="dd5d9-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="dd5d9-338">Ruumi leidmise etapid on progresseeruvad.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-338">The slotting steps are progressive.</span></span> <span data-ttu-id="dd5d9-339">Kui soovite valida suvandit *Otsi nõudlust*, peate esmalt valima *Loo nõudlus*.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-339">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="dd5d9-340">Määrake kasutatav ruumi leidmise mall.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="dd5d9-341">Soovi korral saate määrata kordumise automaatselt käivituma.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="dd5d9-342">Selle stsenaariumi harjutuste jaoks **ärge** seadistage automaatset ruumi leidmist.</span><span class="sxs-lookup"><span data-stu-id="dd5d9-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
