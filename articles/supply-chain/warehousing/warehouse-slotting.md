---
title: Lao ruumi leidmine
description: Selles teemas antakse teavet lao ruumi leidmise kohta. Lao ruumi leidmise abil saate konsolideerida nõudlust kauba ja mõõtühiku järgi tellimustest, mille olek on tellitud, reserveeritud või väljastatud. See aitab laohalduritel nutikalt planeerida komplekteerimise asukohti enne tellimuse lattu väljatamist ja komplekteerimistöö loomist.
author: mirzaab
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0dd1f42b7bb337ccb65b7e4bdd9d307d074ae0d0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838150"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="93f22-105">Lao ruumi leidmine</span><span class="sxs-lookup"><span data-stu-id="93f22-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93f22-106">Mitmed saadavalolevad laoruumi paigutamise funktsioonid aitavad laohalduritel nutikalt planeerida komplekteerimise asukohti enne tellimuse lattu väljastamist ja komplekteerimistöö loomist.</span><span class="sxs-lookup"><span data-stu-id="93f22-106">Several warehouse slotting features are available to help warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

<span data-ttu-id="93f22-107">*Lao paigutamise funktsiooni* abil saate konsolideerida nõudlust kauba ja mõõtühiku järgi tellimustest, mille olek on *Tellitud*, *Reserveeritud* või *Väljastatud*.</span><span class="sxs-lookup"><span data-stu-id="93f22-107">The *Warehouse slotting feature* lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="93f22-108">Loodud nõudlust saab seejärel rakendada asukohtadele, mida kasutatakse koguse, ühiku, füüsiliste dimensioonide, fikseeritud asukohtade ja muu alusel komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="93f22-108">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="93f22-109">Pärast seda, kui ruumi leidmise plaan on loodud, saab luua täiendamise töö, et tuua igasse asukohta sobiv kogus varusid.</span><span class="sxs-lookup"><span data-stu-id="93f22-109">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="93f22-110">*Üleviimistellimustele laoruumi leidmise* funktsioon võimaldab laohaldajatel täiendada komplekteerimise asukohti, mis põhinevad nõudel, mis ei ole veel lattu väljastatud.</span><span class="sxs-lookup"><span data-stu-id="93f22-110">The *Warehouse slotting for transfer orders* feature lets warehouse managers replenish picking locations, based on demand from transfer orders that aren't yet released to the warehouse.</span></span> <span data-ttu-id="93f22-111">See tagab, et kõik komplekteerimise asukohad kaasavad kõik kaubad, mis on vajalikud üleviimistellimuste jaoks pärast nende lattu väljastamist.</span><span class="sxs-lookup"><span data-stu-id="93f22-111">It ensures that picking locations will include all the items that are required for the transfer orders after they are released to warehouse.</span></span> <span data-ttu-id="93f22-112">Selle funktsiooni kasutamiseks tuleb teil sisse lülitada ka *Laoruumi leidmise funktsioon*.</span><span class="sxs-lookup"><span data-stu-id="93f22-112">This feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span>

<span data-ttu-id="93f22-113">*Laoruumi eraldamise täiustuste* funktsioon lisab valiku malli ridadele, mida kasutatakse *Laoruumi eraldamise funktsioonis*.</span><span class="sxs-lookup"><span data-stu-id="93f22-113">The *Warehouse slotting allocation enhancements* feature adds an option for the template lines that are used by the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="93f22-114">Suvand võimaldab süsteemil kaaluda olemasolevat vaba kaubavaru sihtkoha asukohas.</span><span class="sxs-lookup"><span data-stu-id="93f22-114">The option enables the system to consider existing on-hand inventory at a target location.</span></span> <span data-ttu-id="93f22-115">Seetõttu võidakse ruumi loomiseks luua vähem täiendusi.</span><span class="sxs-lookup"><span data-stu-id="93f22-115">Therefore, fewer replenishments might be generated for slotting.</span></span> <span data-ttu-id="93f22-116">*Laoruumi paigutamise täiustamise* funktsioon nõuab, et kasutataks ka *Laoruumi eraldamise funktsiooni*.</span><span class="sxs-lookup"><span data-stu-id="93f22-116">The *Warehouse slotting allocation enhancements* feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="93f22-117">Seda saab soovi korral kasutada koos *Lao ümberpaigutamisega üleviimistellimuste* funktsiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="93f22-117">It can optionally be used together with the *Warehouse slotting for transfer orders* feature.</span></span>

## <a name="turn-on-the-warehouse-slotting-features"></a><span data-ttu-id="93f22-118">Laoruumi leidmise funktsioonide sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="93f22-118">Turn on the warehouse slotting features</span></span>

<span data-ttu-id="93f22-119">Enne nende funktsioonide kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="93f22-119">Before you can use these features, they must be turned on in your system.</span></span> <span data-ttu-id="93f22-120">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsioonide olekut ja need vajadusel sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="93f22-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="93f22-121">Järgmiste funktsioonide sisselülitamine vastavalt vajadusele:</span><span class="sxs-lookup"><span data-stu-id="93f22-121">Turn on the following features as required:</span></span>

- <span data-ttu-id="93f22-122">Laopesade planeerimise funktsioon</span><span class="sxs-lookup"><span data-stu-id="93f22-122">Warehouse slotting feature</span></span>
- <span data-ttu-id="93f22-123">Laoruumi leidmine üleviimistellimuste jaoks</span><span class="sxs-lookup"><span data-stu-id="93f22-123">Warehouse slotting for transfer orders</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="93f22-124">*Laoruumi leidmise funktsioon* peab enne seda funktsiooni olema sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="93f22-124">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

- <span data-ttu-id="93f22-125">Laoruumi leidmise eraldamise täiustused</span><span class="sxs-lookup"><span data-stu-id="93f22-125">Warehouse slotting allocation enhancements</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="93f22-126">*Laoruumi leidmise funktsioon* peab enne seda funktsiooni olema sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="93f22-126">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="93f22-127">Lao ruumi leidmise seadistamine</span><span class="sxs-lookup"><span data-stu-id="93f22-127">Set up warehouse slotting</span></span>

<span data-ttu-id="93f22-128">Lao ruumi leidmise kasutamiseks peate seadistama järgmised elemendid oma süsteemis:</span><span class="sxs-lookup"><span data-stu-id="93f22-128">To use warehouse slotting, you must set up the following elements in your system:</span></span>

- <span data-ttu-id="93f22-129">Ruumi leidmise mõõtühiku järgud</span><span class="sxs-lookup"><span data-stu-id="93f22-129">Slotting unit of measure tiers</span></span>
- <span data-ttu-id="93f22-130">Korralduse koodid</span><span class="sxs-lookup"><span data-stu-id="93f22-130">Directive codes</span></span>
- <span data-ttu-id="93f22-131">Ruumi leidmise mallid</span><span class="sxs-lookup"><span data-stu-id="93f22-131">Slotting templates</span></span>
- <span data-ttu-id="93f22-132">Asukohakorraldus</span><span class="sxs-lookup"><span data-stu-id="93f22-132">Location directives</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="93f22-133">Mõõtühikute järkude loomine ruumi leidmise jaoks</span><span class="sxs-lookup"><span data-stu-id="93f22-133">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="93f22-134">Mõõtühikute järgud võimaldavad mitme mõõtühiku grupeerimist ruumi leidmise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="93f22-134">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="93f22-135">Näiteks kui erineva suurusega kaste komplekteeritakse samalt kastide komplekteerimise alalt, saab iga suuruse jaoks luua ühe järgu.</span><span class="sxs-lookup"><span data-stu-id="93f22-135">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="93f22-136">**Iga mõõtühiku jaoksa tuleb luua rida, mis on selle järgu osa.**</span><span class="sxs-lookup"><span data-stu-id="93f22-136">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="93f22-137">Avage jaotis **Laohaldus \> Häälestus \> Täiendamine \> Ruumi leidmise mõõtühikute järgud**.</span><span class="sxs-lookup"><span data-stu-id="93f22-137">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="93f22-138">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="93f22-138">Select **New**.</span></span>
1. <span data-ttu-id="93f22-139">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-139">In the header, set the following values:</span></span>

    - <span data-ttu-id="93f22-140">**Mõõtühiku järk:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="93f22-140">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="93f22-141">**Kirjeldus:** *Iga kasti kaubaalus*</span><span class="sxs-lookup"><span data-stu-id="93f22-141">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="93f22-142">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="93f22-142">Select **Save**.</span></span>
1. <span data-ttu-id="93f22-143">Valige kiirkaardil **Mõõtühikud** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="93f22-143">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="93f22-144">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="93f22-145">**Ühik:** *Kast*</span><span class="sxs-lookup"><span data-stu-id="93f22-145">**Unit:** *Box*</span></span>
    - <span data-ttu-id="93f22-146">**Kirjeldus:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="93f22-146">**Description:** Leave this field blank.</span></span> <span data-ttu-id="93f22-147">See täidetakse muudatuste salvestamisel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="93f22-147">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="93f22-148">**Ühiku klass:** *Kogus*</span><span class="sxs-lookup"><span data-stu-id="93f22-148">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="93f22-149">Klõpsake valikut **Uus**, et lisada ruudustikku teine rida.</span><span class="sxs-lookup"><span data-stu-id="93f22-149">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="93f22-150">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-150">On the new line, set the following values:</span></span>

    - <span data-ttu-id="93f22-151">**Ühik:** *ea*</span><span class="sxs-lookup"><span data-stu-id="93f22-151">**Unit:** *ea*</span></span>
    - <span data-ttu-id="93f22-152">**Kirjeldus:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="93f22-152">**Description:** Leave this field blank.</span></span> <span data-ttu-id="93f22-153">See täidetakse muudatuste salvestamisel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="93f22-153">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="93f22-154">**Ühiku klass:** *Kogus*</span><span class="sxs-lookup"><span data-stu-id="93f22-154">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="93f22-155">Klõpsake valikut **Uus**, et lisada ruudustikku kolmas rida.</span><span class="sxs-lookup"><span data-stu-id="93f22-155">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="93f22-156">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-156">On the new line, set the following values:</span></span>

    - <span data-ttu-id="93f22-157">**Ühik:** *PL*</span><span class="sxs-lookup"><span data-stu-id="93f22-157">**Unit:** *PL*</span></span>
    - <span data-ttu-id="93f22-158">**Kirjeldus:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="93f22-158">**Description:** Leave this field blank.</span></span> <span data-ttu-id="93f22-159">See täidetakse muudatuste salvestamisel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="93f22-159">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="93f22-160">**Ühiku klass:** *Kogus*</span><span class="sxs-lookup"><span data-stu-id="93f22-160">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="93f22-161">Järgu salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="93f22-161">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="93f22-162">Korralduskoodi loomine ruumi leidmiseks</span><span class="sxs-lookup"><span data-stu-id="93f22-162">Create a directive code for slotting</span></span>

<span data-ttu-id="93f22-163">Peate valima korralduskoodi, mis tuleks malliga seostada.</span><span class="sxs-lookup"><span data-stu-id="93f22-163">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="93f22-164">Avage jaotis **Laohaldus \> Seadistus \> Korralduskoodid**.</span><span class="sxs-lookup"><span data-stu-id="93f22-164">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="93f22-165">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="93f22-165">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="93f22-166">Sisestage väljale **Korralduskood** väärtus *Ruumi leidmine*.</span><span class="sxs-lookup"><span data-stu-id="93f22-166">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="93f22-167">Sisestage väljale **Korralduse kirjeldus** väärtus *Ruumi leidmine*.</span><span class="sxs-lookup"><span data-stu-id="93f22-167">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="93f22-168">Ruumi leidmise mallide seadistamine</span><span class="sxs-lookup"><span data-stu-id="93f22-168">Set up slotting templates</span></span>

<span data-ttu-id="93f22-169">Iga ruumi leidmise mall juhib seda, kuidas kindla lao asukohtade jaoks määratakse varusid.</span><span class="sxs-lookup"><span data-stu-id="93f22-169">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="93f22-170">Iga mall peab sisaldama rida iga ruumi leidmise täpsustuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="93f22-170">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="93f22-171">Kasutage selle jaotise protseduure, et häälestada ruumi leidmise malle.</span><span class="sxs-lookup"><span data-stu-id="93f22-171">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="93f22-172">Avage jaotis **Laohaldus \> Seadistus \> Täiendamine \> Ruumi leidmise mallid**.</span><span class="sxs-lookup"><span data-stu-id="93f22-172">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="93f22-173">Valige malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="93f22-173">Select **New** to create a template.</span></span>

<span data-ttu-id="93f22-174">Järgmisena peate seadistama malli päise, ruumi leidmise kirjelduse ja asukohakorraldused järgmistes alamjaotistes kirjeldatud juhiste järgi.</span><span class="sxs-lookup"><span data-stu-id="93f22-174">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span> <span data-ttu-id="93f22-175">Üleviimistellimuste paigutamine meenutab müügitellimuste paigutamise seadistust, kuid **Nõudluse tüüp** välja väärtuseks seatakse *Üleviimistellimused*, mitte *Müügitellimused*.</span><span class="sxs-lookup"><span data-stu-id="93f22-175">The setup for slotting for transfer orders resembles the setup for slotting for sales orders, but the **Demand type** field is set *Transfer orders* instead of *Sales order*.</span></span>

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a><span data-ttu-id="93f22-176">Müügitellimuse paigutamiseks kasutatava malli päise seadistamine</span><span class="sxs-lookup"><span data-stu-id="93f22-176">Set up the header for a sales order slotting template</span></span>

1. <span data-ttu-id="93f22-177">Määrake malli päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-177">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="93f22-178">**Ruumi leidmise mall:** _61_</span><span class="sxs-lookup"><span data-stu-id="93f22-178">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="93f22-179">**Kirjeldus:** _61_</span><span class="sxs-lookup"><span data-stu-id="93f22-179">**Description:** _61_</span></span>
    - <span data-ttu-id="93f22-180">**Nõudluse tüüp:** *Müügitellimus*</span><span class="sxs-lookup"><span data-stu-id="93f22-180">**Demand type:** *Sales order*</span></span>

        > [!NOTE]
        > <span data-ttu-id="93f22-181">Praegu *Müügitellimused* ja *Üleviimistellimused* ainukesed toetatavad nõudluse tüübid.</span><span class="sxs-lookup"><span data-stu-id="93f22-181">Currently, *Sales orders* and *Transfer orders* are the only demand types that are supported.</span></span> <span data-ttu-id="93f22-182">*Üleviimistellimusi* saate valida ainult juhul, kui *Laoruumi leidmine üleviimistellimusele* funktsioon on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="93f22-182">You can select *Transfer orders* only if the *Warehouse Slotting for transfer orders* feature is turned on.</span></span>

    - <span data-ttu-id="93f22-183">**Nõudluse strateegia:** _Tellitud_</span><span class="sxs-lookup"><span data-stu-id="93f22-183">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="93f22-184">Sellel väljal on saadaval järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-184">The following values are available in this field:</span></span>

        - <span data-ttu-id="93f22-185">**Tellitud** – müügitellimuse täielikku tellitud kogust tuleks arvestada nõudlusena.</span><span class="sxs-lookup"><span data-stu-id="93f22-185">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="93f22-186">**Reserveeritud** – ainult reserveeritud müügitellimuse rea (füüsilised ja tellitud) koguseid tuleks arvestada nõudlusena.</span><span class="sxs-lookup"><span data-stu-id="93f22-186">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>
        - <span data-ttu-id="93f22-187">**Väljastatud** – Väljastatud kogus tuleks lugeda nõudluseks.</span><span class="sxs-lookup"><span data-stu-id="93f22-187">**Released** – The released quantity should be considered demand.</span></span>

    - <span data-ttu-id="93f22-188">**Ladu:** _61_</span><span class="sxs-lookup"><span data-stu-id="93f22-188">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="93f22-189">**Luba voo nõudmisel kasutada reserveerimata koguseid:** _Jah_</span><span class="sxs-lookup"><span data-stu-id="93f22-189">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="93f22-190">Samuti saate määrata päringu hinnatava nõudluse ulatuse kitsendamiseks.</span><span class="sxs-lookup"><span data-stu-id="93f22-190">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="93f22-191">Ruumi leidmise täpsustuste seadistamine iga malli jaoks</span><span class="sxs-lookup"><span data-stu-id="93f22-191">Set up slotting specifications for each template</span></span>

<span data-ttu-id="93f22-192">Iga loodava müügitellimuse malli jaoks järgige neid etappe, et lisada rida iga ruumi leidmise täpsustuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="93f22-192">For each sales order template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="93f22-193">Valige kiirkaardil **Ruumi leidmise malli üksikasjad** suvand **Uus**, et luua malli rida.</span><span class="sxs-lookup"><span data-stu-id="93f22-193">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="93f22-194">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-194">On the new line, set the following values:</span></span>

    - <span data-ttu-id="93f22-195">**Järjestus:** _1_</span><span class="sxs-lookup"><span data-stu-id="93f22-195">**Sequence:** _1_</span></span>
    - <span data-ttu-id="93f22-196">**Kirjeldus:** _Fikseeritud asukoht_</span><span class="sxs-lookup"><span data-stu-id="93f22-196">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="93f22-197">**Minimaalne kogus:** _1_</span><span class="sxs-lookup"><span data-stu-id="93f22-197">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="93f22-198">See väli määratleb rea jaoks nõutava minimaalse koguse.</span><span class="sxs-lookup"><span data-stu-id="93f22-198">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="93f22-199">**Maksimaalne kogus:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="93f22-199">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="93f22-200">See väli määratleb rea jaoks kehtiva maksimaalse koguse.</span><span class="sxs-lookup"><span data-stu-id="93f22-200">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="93f22-201">**Ühik:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="93f22-201">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="93f22-202">See väli määratleb mõõtühiku, millele minimaalne ja maksimaalne kogus viitab.</span><span class="sxs-lookup"><span data-stu-id="93f22-202">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="93f22-203">**Mõõtühiku järk:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="93f22-203">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="93f22-204">See väli määratleb rea jaoks kehtiva mõõtühiku.</span><span class="sxs-lookup"><span data-stu-id="93f22-204">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="93f22-205">(Lisateavet leiate selle teema varasemast jaotisest [Ruumi leidmise mõõtühikute järkude seadistamine](#unit-tiers).)</span><span class="sxs-lookup"><span data-stu-id="93f22-205">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="93f22-206">**Määra ruumi kriteeriumid:** _Koguse kaalumine_</span><span class="sxs-lookup"><span data-stu-id="93f22-206">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="93f22-207">Sellel väljal on saadaval järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-207">The following values are available in this field:</span></span>

        - <span data-ttu-id="93f22-208">**Tühja eeldamine** – see süsteem peaks eeldama, et kõik komplekteerimisala asukohad on tühjad ja neid ei tohiks kontrollida varudes.</span><span class="sxs-lookup"><span data-stu-id="93f22-208">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="93f22-209">**Koguse kaalumine** – see süsteem peaks kontrollima varusid komplekteerimisala asukohtades ja ei tohiks jätta vahele asukohti, mis pole tühjad.</span><span class="sxs-lookup"><span data-stu-id="93f22-209">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>
        - <span data-ttu-id="93f22-210">**Arvestage laoseisu** – Süsteem peaks kontrollima, kas sihtkohas oleva kauba jaoks on reserveeritud kogused.</span><span class="sxs-lookup"><span data-stu-id="93f22-210">**Consider on-hand** – The system should check whether any target location contains unreserved quantities for the item on the demand line.</span></span> <span data-ttu-id="93f22-211">Kui kogus on piisavalt suur, et rahuldada vähemalt üht nõudluse rea ühikut, vähendatakse loodud paigutamise plaani kirjet saadaoleva summa võrra.</span><span class="sxs-lookup"><span data-stu-id="93f22-211">If the quantity is large enough to satisfy at least one unit of the demand line, the generated slotting plan record is reduced by the available amount.</span></span> <span data-ttu-id="93f22-212">Näiteks kui nõudlus on 10 kasti ja üks kast on laos olemas, on leitud nõudlus üheksa kasti.</span><span class="sxs-lookup"><span data-stu-id="93f22-212">For example, if the demand is 10 cases, and one case is on hand, the located demand will be nine cases.</span></span> <span data-ttu-id="93f22-213">Kui nõudlus on 10 kasti ja üks kast on käepärast, on leitud nõudlus 10 kasti.</span><span class="sxs-lookup"><span data-stu-id="93f22-213">If the demand is 10 cases, and one each is on hand, the located demand will be 10 cases.</span></span> <span data-ttu-id="93f22-214">See väärtus on saadaval ainult siis, kui funktsioon *Lao paigutamise täiustamine* on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="93f22-214">This value is available only when the *Warehouse slotting allocation enhancements* feature is turned on.</span></span>

    - <span data-ttu-id="93f22-215">**Korralduskood:** _Ruumi leidmine_</span><span class="sxs-lookup"><span data-stu-id="93f22-215">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="93f22-216">See väli määratleb asukohakorralduse, mida kasutatakse täiendamistöö komplekteerimise asukoha leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="93f22-216">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="93f22-217">**Ületäitumise asukoht:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="93f22-217">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="93f22-218">See väli määratleb asukoha, kuhu varud ladustatakse juhul, kui rea töötlemisel koguse asukohta ei leita.</span><span class="sxs-lookup"><span data-stu-id="93f22-218">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="93f22-219">**Luba loobumine:** _Jah_</span><span class="sxs-lookup"><span data-stu-id="93f22-219">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="93f22-220">Kui selle suvandi väärtuseks on seatud *Jah*, luuakse liikumise töö juhul, kui nõudlusele ei leita ruumi, et võtta varud välja asukohtadest, kus on varusid, kuid leitud ruumi ei kasutatud.</span><span class="sxs-lookup"><span data-stu-id="93f22-220">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="93f22-221">Seejärel käivitatakse mall uuesti.</span><span class="sxs-lookup"><span data-stu-id="93f22-221">The template is then run again.</span></span> <span data-ttu-id="93f22-222">Seekord eirab see varusid asukohtades.</span><span class="sxs-lookup"><span data-stu-id="93f22-222">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="93f22-223">See funktsioon töötab kõige paremini siis, kui välja **Ruumi kriteeriumide määramine** on seatud _Koguse kaalumine_.</span><span class="sxs-lookup"><span data-stu-id="93f22-223">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="93f22-224">**Fikseeritud asukoha kasutus:** _Ainult selle toote fikseeritud asukohad_</span><span class="sxs-lookup"><span data-stu-id="93f22-224">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="93f22-225">Sellel väljal on saadaval järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-225">The following values are available in this field:</span></span>

        - <span data-ttu-id="93f22-226">**Fikseeritud ja mittefikseeritud asukohad** – süsteem ei tohiks piirduda ainult fikseeritud asukohtade kasutamisega.</span><span class="sxs-lookup"><span data-stu-id="93f22-226">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="93f22-227">**Ainult selle toote fikseeritud asukohad** – süsteem peaks kasutama ainult nende asukohtade ruumi, mis on selle toote jaoks fikseeritud asukohad.</span><span class="sxs-lookup"><span data-stu-id="93f22-227">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="93f22-228">**Ainult selle tootevariandi fikseeritud asukohad** – süsteem peaks kasutama ainult nende asukohtade ruumi, mis on selle tootevariandi jaoks fikseeritud asukohad.</span><span class="sxs-lookup"><span data-stu-id="93f22-228">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

> [!NOTE]
> <span data-ttu-id="93f22-229">Kui paigutamise mall sisaldab vähemalt ühte rida, kus välja **Määra ruumi kriteerium** väärtuseks on seatud *Arvestage olemasolevat kaubavaru*, ei lubata mitte ühtegi malli rida soiku jääda.</span><span class="sxs-lookup"><span data-stu-id="93f22-229">If the slotting template contains at least one line where the **Assign slot criteria** field is set to *Consider on-hand*, let-ups are no longer allowed for any line in the template.</span></span>

1. <span data-ttu-id="93f22-230">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="93f22-230">Select **Save**.</span></span>
1. <span data-ttu-id="93f22-231">Teise malli rea loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="93f22-231">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="93f22-232">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="93f22-233">**Järjestus:** _2_</span><span class="sxs-lookup"><span data-stu-id="93f22-233">**Sequence:** _2_</span></span>
    - <span data-ttu-id="93f22-234">**Kirjeldus:** _Muu_</span><span class="sxs-lookup"><span data-stu-id="93f22-234">**Description:** _Other_</span></span>
    - <span data-ttu-id="93f22-235">**Minimaalne kogus:** _1_</span><span class="sxs-lookup"><span data-stu-id="93f22-235">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="93f22-236">**Maksimaalne kogus:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="93f22-236">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="93f22-237">**Ühik:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="93f22-237">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="93f22-238">**Mõõtühiku järk:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="93f22-238">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="93f22-239">**Määra ruumi kriteeriumid:** _Koguse kaalumine_</span><span class="sxs-lookup"><span data-stu-id="93f22-239">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="93f22-240">**Korralduskood:** _Ruumi leidmine_</span><span class="sxs-lookup"><span data-stu-id="93f22-240">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="93f22-241">**Ületäitumise asukoht:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="93f22-241">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="93f22-242">**Luba loobumine:** _Jah_</span><span class="sxs-lookup"><span data-stu-id="93f22-242">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="93f22-243">**Fikseeritud asukohtade kasutamine:** _Fikseeritud ja mittefikseeritud asukohad_</span><span class="sxs-lookup"><span data-stu-id="93f22-243">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="93f22-244">Teise rea päringus saate nüüd määrata kriteeriumid, mille alusel määratletakse, millistest asukohtadest selle rea nõudlusele saab ruumi leida.</span><span class="sxs-lookup"><span data-stu-id="93f22-244">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="93f22-245">Otsige üles rida, kus välja **Järjestus** väärtuseks on seatud *2*.</span><span class="sxs-lookup"><span data-stu-id="93f22-245">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="93f22-246">Valige **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="93f22-246">Select **Edit query**.</span></span>
1. <span data-ttu-id="93f22-247">Vahekaardil **Vahemik** valige käsk **Lisa**, et lisada uus rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="93f22-247">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="93f22-248">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-248">On the new line, set the following values:</span></span>

    - <span data-ttu-id="93f22-249">**Tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="93f22-249">**Table:** *Locations*</span></span>
    - <span data-ttu-id="93f22-250">**Tuletatud tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="93f22-250">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="93f22-251">**Väli:** *Asukohaprofiili ID*</span><span class="sxs-lookup"><span data-stu-id="93f22-251">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="93f22-252">**Kriteeriumid:** *Pick-06* (valige väljal kahekordne plussmärk \[**++**\] loendi laiendamiseks ja seejärel valige *Pick-06* - *Komplekteerimissait 6*.)</span><span class="sxs-lookup"><span data-stu-id="93f22-252">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="93f22-253">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="93f22-253">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="93f22-254">Asukohakorralduste häälestamine</span><span class="sxs-lookup"><span data-stu-id="93f22-254">Set up location directives</span></span>

<span data-ttu-id="93f22-255">Vähemalt üks asukohakorraldus peab olema seadistatud, et toetada ruumi leidmise valikuid.</span><span class="sxs-lookup"><span data-stu-id="93f22-255">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="93f22-256">Kasutage selles jaotises olevaid protseduure uue *täiendamise asukohakorralduse* seadistamiseks ruumi leidmise valikute tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="93f22-256">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="93f22-257">Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.</span><span class="sxs-lookup"><span data-stu-id="93f22-257">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="93f22-258">Valige vasakpoolse paani väljal **Töökäsu tüüp** suvand *Täiendamine*.</span><span class="sxs-lookup"><span data-stu-id="93f22-258">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="93f22-259">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="93f22-259">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="93f22-260">Sisestage uue asukohakorralduse päise väljale **Nimi** väärtus *61 ruumi leidmise komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="93f22-260">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>
1. <span data-ttu-id="93f22-261">**Järjekorranumber** väljal nõustuge vaikeväärtusega.</span><span class="sxs-lookup"><span data-stu-id="93f22-261">In the **Sequence number** field, accept the default value.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="93f22-262">Asukohakorralduste kiirkaardi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="93f22-262">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="93f22-263">Määrake kiirkaardil **Asukohakorraldused** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-263">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="93f22-264">Võtke vastu vaikeväärtused kõigil teistel väljadel.</span><span class="sxs-lookup"><span data-stu-id="93f22-264">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="93f22-265">**Töö tüüp:** _Komplekteerimine_</span><span class="sxs-lookup"><span data-stu-id="93f22-265">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="93f22-266">**Tegevuskoht:** _6_</span><span class="sxs-lookup"><span data-stu-id="93f22-266">**Site:** _6_</span></span>
    - <span data-ttu-id="93f22-267">**Ladu:** _61_</span><span class="sxs-lookup"><span data-stu-id="93f22-267">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="93f22-268">**Korralduskood:** _Ruumi leidmine_</span><span class="sxs-lookup"><span data-stu-id="93f22-268">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="93f22-269">Valige **Salvesta**, et muuta kiirkaart **Read** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="93f22-269">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="93f22-270">Ridade kiirkaardi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="93f22-270">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="93f22-271">Rea loomiseks valige kiirkaardil **Read** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="93f22-271">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="93f22-272">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-272">On the new line, set the following values.</span></span>

    - <span data-ttu-id="93f22-273">**Alates kogusest:** _0_</span><span class="sxs-lookup"><span data-stu-id="93f22-273">**From quantity:** _0_</span></span>
    - <span data-ttu-id="93f22-274">**Koguseni:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="93f22-274">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="93f22-275">Võtke vastu ülejäänud väljade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-275">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="93f22-276">Valige **Salvesta**, et muuta kiirkaart **Asukohakorralduse toimingud** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="93f22-276">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="93f22-277">Asukohakorralduste tegevuste kiirkaardi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="93f22-277">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="93f22-278">Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus**, et luua rida.</span><span class="sxs-lookup"><span data-stu-id="93f22-278">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="93f22-279">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-279">On the new line, set the following values.</span></span> <span data-ttu-id="93f22-280">Võtke vastu vaikeväärtused kõigil teistel väljadel.</span><span class="sxs-lookup"><span data-stu-id="93f22-280">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="93f22-281">**Järjekorranumber:** nõustuge vaikeväärtusega.</span><span class="sxs-lookup"><span data-stu-id="93f22-281">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="93f22-282">**Nimi:** _Hulgi_</span><span class="sxs-lookup"><span data-stu-id="93f22-282">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="93f22-283">**Strateegia:** _Puudub_</span><span class="sxs-lookup"><span data-stu-id="93f22-283">**Strategy:** _None_</span></span>

1. <span data-ttu-id="93f22-284">Võtke vastu ülejäänud väljade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-284">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="93f22-285">Valige **Salvesta**, et muuta nupp **Päringu redigeerimine** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="93f22-285">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="93f22-286">Redigeeri päringut</span><span class="sxs-lookup"><span data-stu-id="93f22-286">Edit the query</span></span>

1. <span data-ttu-id="93f22-287">Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="93f22-287">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="93f22-288">Vahekaardil **Vahemik** valige käsk **Lisa**, et lisada uus rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="93f22-288">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="93f22-289">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-289">On the new line, set the following values:</span></span>

    - <span data-ttu-id="93f22-290">**Tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="93f22-290">**Table:** *Locations*</span></span>
    - <span data-ttu-id="93f22-291">**Tuletatud tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="93f22-291">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="93f22-292">**Väli:** *Tsooni ID*</span><span class="sxs-lookup"><span data-stu-id="93f22-292">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="93f22-293">**Kriteeriumid:** *Hulgi* (valige väljal kahekordne plussmärk \[**++**\] loendi laiendamiseks ja seejärel valige *Hulgi*.)</span><span class="sxs-lookup"><span data-stu-id="93f22-293">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="93f22-294">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="93f22-294">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="93f22-295">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="93f22-295">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="93f22-296">Stsenaariumi seadistamine</span><span class="sxs-lookup"><span data-stu-id="93f22-296">Set up the scenario</span></span>

<span data-ttu-id="93f22-297">Selle stsenaariumi puhul saate kasutada sisseehitatud näidisandmeid ja luua selles jaotises kirjeldatud kirjeid.</span><span class="sxs-lookup"><span data-stu-id="93f22-297">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="93f22-298">USMF-näidisandmete kasutamine</span><span class="sxs-lookup"><span data-stu-id="93f22-298">Use the USMF sample data</span></span>

<span data-ttu-id="93f22-299">Selle stsenaariumi kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="93f22-299">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="93f22-300">Enne alustamist peate valima ka juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="93f22-300">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="93f22-301">Nõudluse loomine</span><span class="sxs-lookup"><span data-stu-id="93f22-301">Create demand</span></span>

<span data-ttu-id="93f22-302">Järgige neid etappe nõudluse loomiseks, millele soovite ruumi leidmist rakendada.</span><span class="sxs-lookup"><span data-stu-id="93f22-302">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="93f22-303">Avage jaotis **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="93f22-303">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="93f22-304">Müügitellimuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="93f22-304">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="93f22-305">Valige dialoogiboksi **Müügitellimuse loomine** väljal **Kliendi konto** suvand _US-007_.</span><span class="sxs-lookup"><span data-stu-id="93f22-305">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="93f22-306">Valige väljal **Ladu** väärtus _61_.</span><span class="sxs-lookup"><span data-stu-id="93f22-306">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="93f22-307">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="93f22-307">Select **OK**.</span></span>
1. <span data-ttu-id="93f22-308">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="93f22-308">The new sales order is opened.</span></span> <span data-ttu-id="93f22-309">See lisab uue tühja rea kiirkaardil **Müügitellimuse read**.</span><span class="sxs-lookup"><span data-stu-id="93f22-309">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="93f22-310">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-310">On this line, set the following values:</span></span>

    - <span data-ttu-id="93f22-311">**Kaup:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="93f22-311">**Item:** _L0101_</span></span>
    - <span data-ttu-id="93f22-312">**Kogus:** _20_</span><span class="sxs-lookup"><span data-stu-id="93f22-312">**Quantity:** _20_</span></span>

1. <span data-ttu-id="93f22-313">Valige **Lisa rida**, et lisada uus rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-313">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="93f22-314">**Kaup:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="93f22-314">**Item:** _T0100_</span></span>
    - <span data-ttu-id="93f22-315">**Kogus:** _8_</span><span class="sxs-lookup"><span data-stu-id="93f22-315">**Quantity:** _8_</span></span>

1. <span data-ttu-id="93f22-316">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="93f22-316">Select **Save**.</span></span>
1. <span data-ttu-id="93f22-317">Teise müügitellimuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="93f22-317">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="93f22-318">Valige dialoogiboksi **Müügitellimuse loomine** väljal **Kliendi konto** suvand _US-008_.</span><span class="sxs-lookup"><span data-stu-id="93f22-318">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="93f22-319">Valige väljal **Ladu** väärtus _61_.</span><span class="sxs-lookup"><span data-stu-id="93f22-319">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="93f22-320">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="93f22-320">The new sales order is opened.</span></span> <span data-ttu-id="93f22-321">See lisab uue tühja rea kiirkaardil **Müügitellimuse read**.</span><span class="sxs-lookup"><span data-stu-id="93f22-321">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="93f22-322">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="93f22-322">On this line, set the following values:</span></span>

    - <span data-ttu-id="93f22-323">**Kaup:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="93f22-323">**Item:** _T0100_</span></span>
    - <span data-ttu-id="93f22-324">**Kogus:** _1_</span><span class="sxs-lookup"><span data-stu-id="93f22-324">**Quantity:** _1_</span></span>

1. <span data-ttu-id="93f22-325">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="93f22-325">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="93f22-326">Tavalise ruumi leidmise stsenaariumi ülevaade</span><span class="sxs-lookup"><span data-stu-id="93f22-326">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="93f22-327">Kui kõik eeltingimuseks olevad elemendid on eelmise jaotise kirjelduste järgi paigas, olete valmis funktsiooni proovima, tehes läbi kõik selles jaotises olevad harjutused.</span><span class="sxs-lookup"><span data-stu-id="93f22-327">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="93f22-328">Loo nõudlus</span><span class="sxs-lookup"><span data-stu-id="93f22-328">Generate demand</span></span>

1. <span data-ttu-id="93f22-329">Avage jaotis **Laohaldus \> Seadistus \> Täiendamine \> Ruumi leidmise mallid** ja valige eelnevalt loodud ruumi leidmise mall.</span><span class="sxs-lookup"><span data-stu-id="93f22-329">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="93f22-330">Valige toimingupaanil **Loo nõudlus**.</span><span class="sxs-lookup"><span data-stu-id="93f22-330">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="93f22-331">See käsk hindab kõiki süsteemis olevaid nõudlusi, mis ühtivad ruumi leidmise malli päringuga.</span><span class="sxs-lookup"><span data-stu-id="93f22-331">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="93f22-332">Kõigi tellimuste kõik nõudlused konsolideeritakse seejärel ühele reale koguse/mõõtühiku kohta.</span><span class="sxs-lookup"><span data-stu-id="93f22-332">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="93f22-333">Kui protsess on lõpule viidud, kuvatakse teade.</span><span class="sxs-lookup"><span data-stu-id="93f22-333">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="93f22-334">Ruumi leidmise nõudlus</span><span class="sxs-lookup"><span data-stu-id="93f22-334">Slotting demand</span></span>

<span data-ttu-id="93f22-335">*Ruumi leidmise nõudlus* kuvab nõudluse loomise tulemused ruumi leidmise malli seadistuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="93f22-335">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="93f22-336">Valige toimingupaanil **Ruumi leidmise nõudlus**, et kuvada käsu **Loo nõudlus** tulemusi.</span><span class="sxs-lookup"><span data-stu-id="93f22-336">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="93f22-337">Ruumi leidmise nõudluse ridu saab redigeerida.</span><span class="sxs-lookup"><span data-stu-id="93f22-337">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="93f22-338">Saate kustutada rea, lisada uue rea või redigeerida rea üksikasju.</span><span class="sxs-lookup"><span data-stu-id="93f22-338">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="93f22-339">Saate redigeerida nõudlust käsitsi või importida selle andmehalduse abil välisest süsteemist.</span><span class="sxs-lookup"><span data-stu-id="93f22-339">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="93f22-340">Ruumi leidmise nõudluses olevat kasutatakse järgmises etapis, olenemata selle päritolust.</span><span class="sxs-lookup"><span data-stu-id="93f22-340">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="93f22-341">Nõudluse leidmine</span><span class="sxs-lookup"><span data-stu-id="93f22-341">Locate demand</span></span>

<span data-ttu-id="93f22-342">Kui nõudlus on loodud, peate käsu **Otsi nõudlust** abil looma *ruumi leidmise plaani*.</span><span class="sxs-lookup"><span data-stu-id="93f22-342">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="93f22-343">Valige toimingupaanil **Otsi nõudlust**.</span><span class="sxs-lookup"><span data-stu-id="93f22-343">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="93f22-344">Ruumi leidmise protsess töötab.</span><span class="sxs-lookup"><span data-stu-id="93f22-344">The slotting process runs.</span></span> <span data-ttu-id="93f22-345">Kui protsess on lõpule viidud, kuvatakse teade.</span><span class="sxs-lookup"><span data-stu-id="93f22-345">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="93f22-346">Ruumi leidmise plaan</span><span class="sxs-lookup"><span data-stu-id="93f22-346">Slotting plan</span></span>

<span data-ttu-id="93f22-347">Ruumi leidmise plaan kuvab asukohta, kuhu iga kaup/kogus määrati, kas kasutati ületäitumist, kas loodi loobumistöö ja kasutatud malli rida.</span><span class="sxs-lookup"><span data-stu-id="93f22-347">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="93f22-348">*Kõik nõudlused, millele ruumi ei leitud, on punasega esile tõstetud.*</span><span class="sxs-lookup"><span data-stu-id="93f22-348">*Any demand that could not be slotted is highlighted in red.*</span></span>

- <span data-ttu-id="93f22-349">Valige toimingupaanil **Ruumi leidmise plaan** tulemuste kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="93f22-349">On the Action Pane, select **Slotting plan** to view the results.</span></span>

> [!NOTE]
> - <span data-ttu-id="93f22-350">**Nõudluse loomise**, **Nõudluse leidmise** ja **Täiendamise** protsesside käivitamine on nüüd käivitatud.</span><span class="sxs-lookup"><span data-stu-id="93f22-350">The **Generate demand**, **Locate demand**, and **Run replenishment** processes are now run in a sandbox.</span></span> <span data-ttu-id="93f22-351">(Need protsessid on saadaval tegumiribal **Paigutuse mallid** lehel.)</span><span class="sxs-lookup"><span data-stu-id="93f22-351">(These processes are available from the Action Pane on the **Slotting templates** page.)</span></span>
> - <span data-ttu-id="93f22-352">**Nõudluse loomise**, **Nõudluse leidmise** ja **Täiendamise käivitamise** protsessid on lukus tagamaks, et neid ei saa samal ajal käivitada.</span><span class="sxs-lookup"><span data-stu-id="93f22-352">The **Generate demand**, **Locate demand**, and **Run replenishment** processes have a lock to ensure that they can't be triggered at the same time.</span></span> <span data-ttu-id="93f22-353">Muul juhul võidakse kasutatavaid andmeid kustutada.</span><span class="sxs-lookup"><span data-stu-id="93f22-353">Otherwise, the data that is used could be deleted.</span></span>
> - <span data-ttu-id="93f22-354">**Nõudluse loomine** ja **Nõudluse leidmise** protsessid näitavad hoiatust, kui käivitamine ei loo kirjeid või kui kirjetel puudub teave.</span><span class="sxs-lookup"><span data-stu-id="93f22-354">The **Generate demand** and **Locate demand** processes show a warning if the run didn't generate records, or if the records are missing information.</span></span>
> - <span data-ttu-id="93f22-355">Kui valite **Paigutusplaani**, ei ole tegumiribal nuppe **Uus**, **Redigeeri** või **Kustuta**, sest andmeallikat ei saa redigeerida.</span><span class="sxs-lookup"><span data-stu-id="93f22-355">When you select **Slotting plan**, the page doesn't have **New**, **Edit**, or **Delete** buttons on the Action Pane, because the data source can't be edited.</span></span>
> - <span data-ttu-id="93f22-356">Kui valite **Täitmise käivitamise**, kinnitab süsteem valitud teenindusaegade malli ja protsessid.</span><span class="sxs-lookup"><span data-stu-id="93f22-356">When you select **Run replenishment**, the system validates the selected slot template and processes.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="93f22-357">Täiendamise loomine</span><span class="sxs-lookup"><span data-stu-id="93f22-357">Create replenishment</span></span>

<span data-ttu-id="93f22-358">Kui ruumi leidmise plaan on loodud, peate selle plaani põhjal looma *täiendamise töö*.</span><span class="sxs-lookup"><span data-stu-id="93f22-358">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="93f22-359">Valige tegevuste paanil käsk **Käivita täiendamine**.</span><span class="sxs-lookup"><span data-stu-id="93f22-359">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="93f22-360">Kui protsess on lõpule viidud, kuvatakse teade.</span><span class="sxs-lookup"><span data-stu-id="93f22-360">An informational message appears when the process is completed.</span></span> <span data-ttu-id="93f22-361">See teade näitab tööjärgu ID jaoks loodud päiste arvu.</span><span class="sxs-lookup"><span data-stu-id="93f22-361">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="93f22-362">Kasutatavad asukohakorraldused tuvastatakse igale malli reale määratud korralduskoodi alusel.</span><span class="sxs-lookup"><span data-stu-id="93f22-362">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="93f22-363">Näpunäited</span><span class="sxs-lookup"><span data-stu-id="93f22-363">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="93f22-364">Automaatse ruumi leidmise seadistamine</span><span class="sxs-lookup"><span data-stu-id="93f22-364">Set up automatic slotting</span></span>

<span data-ttu-id="93f22-365">Kui kõik vajalikud elemendid on paigas, saate häälestada ruumi leidmise automaatse käivitamise nende etappide abil.</span><span class="sxs-lookup"><span data-stu-id="93f22-365">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="93f22-366">Avage jaotis **Laohaldus \> Täiendamine \> Käivita ruumi leidmine**.</span><span class="sxs-lookup"><span data-stu-id="93f22-366">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="93f22-367">Määrake käivitatavad ruumi leidmise etapid.</span><span class="sxs-lookup"><span data-stu-id="93f22-367">Specify the slotting steps to run.</span></span> <span data-ttu-id="93f22-368">Valige vähemalt üks järgmistest ruumi leidmise etappidest.</span><span class="sxs-lookup"><span data-stu-id="93f22-368">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="93f22-369">Loo nõudlus</span><span class="sxs-lookup"><span data-stu-id="93f22-369">Generate demand</span></span>
    - <span data-ttu-id="93f22-370">Nõudluse leidmine</span><span class="sxs-lookup"><span data-stu-id="93f22-370">Locate demand</span></span>
    - <span data-ttu-id="93f22-371">Täiendustöö loomine</span><span class="sxs-lookup"><span data-stu-id="93f22-371">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="93f22-372">Ruumi leidmise etapid on progresseeruvad.</span><span class="sxs-lookup"><span data-stu-id="93f22-372">The slotting steps are progressive.</span></span> <span data-ttu-id="93f22-373">Kui soovite valida suvandit *Otsi nõudlust*, peate esmalt valima *Loo nõudlus*.</span><span class="sxs-lookup"><span data-stu-id="93f22-373">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="93f22-374">Määrake kasutatav ruumi leidmise mall.</span><span class="sxs-lookup"><span data-stu-id="93f22-374">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="93f22-375">Soovi korral saate määrata kordumise automaatselt käivituma.</span><span class="sxs-lookup"><span data-stu-id="93f22-375">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="93f22-376">Selle stsenaariumi harjutuste jaoks **ärge** seadistage automaatset ruumi leidmist.</span><span class="sxs-lookup"><span data-stu-id="93f22-376">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]