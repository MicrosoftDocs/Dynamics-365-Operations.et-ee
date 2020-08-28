---
title: Muuda töö töökausta
description: Selles teemas selgitatakse, kuidas saate kasutada tööüksuste nuppu Muuda töökausta olemasoleva töö töökausta muutmiseks.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 344918b77334f9aca11f799f8c031047ad229ee0
ms.sourcegitcommit: d25d0feb3f8a5a760eba50ba5f46e1db02737d25
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677358"
---
# <a name="change-work-pool-on-work"></a><span data-ttu-id="f5526-103">Muuda töö töökausta</span><span class="sxs-lookup"><span data-stu-id="f5526-103">Change work pool on work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5526-104">Töö korraldamiseks gruppidesse saate kasutada töökaustu.</span><span class="sxs-lookup"><span data-stu-id="f5526-104">You can use work pools to organize work into groups.</span></span> <span data-ttu-id="f5526-105">Näiteks saate luua töökausta kindlas laoasukohas toimuva töö klassifitseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="f5526-105">For example, you can create a work pool to classify work that occurs in a specific warehouse location.</span></span>

<span data-ttu-id="f5526-106">Funktsioon *Töö töökausta muutmine* lisab nupu **Muuda töökausta** tööüksuste toimingupaanile.</span><span class="sxs-lookup"><span data-stu-id="f5526-106">The *Change work pool on work* feature adds a **Change work pool** button to the Action Pane for work items.</span></span> <span data-ttu-id="f5526-107">Tänu sellele saavad laohaldurid hõlpsalt muuta olemasoleva töö töökausta.</span><span class="sxs-lookup"><span data-stu-id="f5526-107">Therefore, warehouse managers can easily change the work pool of existing work.</span></span> <span data-ttu-id="f5526-108">See funktsioon võimaldab halduritel kiiresti reageerida lao kaupluse korruse muudatustele ja see aitab parandada nende võimet kohaneda muutuvate olukordadega ja vajadusega viia töö üle teise töökausta.</span><span class="sxs-lookup"><span data-stu-id="f5526-108">This feature lets managers react quickly to changes on the warehouse shop floor, and it helps improve their ability to adapt to changing situations and the need to transfer work to another work pool.</span></span>

## <a name="turn-on-the-change-work-pool-on-work-feature"></a><span data-ttu-id="f5526-109">Funktsiooni Töö töökausta muutmine sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="f5526-109">Turn on the Change work pool on work feature</span></span>

<span data-ttu-id="f5526-110">Enne, kui alustate selle funktsiooni seadistamist või kasutamist, peate veenduma, et see oleks teie süsteemis saadaval.</span><span class="sxs-lookup"><span data-stu-id="f5526-110">Before you begin to set up or use this feature, you must make sure that it's available in your system.</span></span> <span data-ttu-id="f5526-111">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="f5526-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="f5526-112">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="f5526-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f5526-113">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="f5526-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="f5526-114">**Funktsiooni nimi:** *Töö töökausta muutmine*</span><span class="sxs-lookup"><span data-stu-id="f5526-114">**Feature name:** *Change work pool on work*</span></span>

## <a name="set-up-the-change-work-pool-on-work-feature"></a><span data-ttu-id="f5526-115">Funktsiooni Töö töökausta muutmine seadistamine</span><span class="sxs-lookup"><span data-stu-id="f5526-115">Set up the Change work pool on work feature</span></span>

<span data-ttu-id="f5526-116">Selle funktsiooni kasutamiseks peavad teil olema seadistatud mõned töökaustad.</span><span class="sxs-lookup"><span data-stu-id="f5526-116">To use this feature, you must have some work pools set up.</span></span> <span data-ttu-id="f5526-117">Samuti võite seadistada töömallid, et need määraksid automaatselt kausta.</span><span class="sxs-lookup"><span data-stu-id="f5526-117">You might also set up your work templates so that they automatically assign a pool.</span></span> <span data-ttu-id="f5526-118">Kui soovite töötada läbi hiljem selles teemas käsitletava näidisstsenaariumi, seadistage oma süsteem selles jaotises kirjeldatud viisil.</span><span class="sxs-lookup"><span data-stu-id="f5526-118">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span>

### <a name="set-up-work-pools"></a><span data-ttu-id="f5526-119">Töökaustade seadistamine</span><span class="sxs-lookup"><span data-stu-id="f5526-119">Set up work pools</span></span>

<span data-ttu-id="f5526-120">Töökaustad võimaldavad teil korraldada tööüksusi tüübi järgi.</span><span class="sxs-lookup"><span data-stu-id="f5526-120">Work pools let you organize work items by type.</span></span> <span data-ttu-id="f5526-121">Funktsiooniga *Töö töökausta muutmine* töötamiseks peab teil olema saadaval vähemalt kaks töökausta.</span><span class="sxs-lookup"><span data-stu-id="f5526-121">To work with the *Change work pool on work* feature, you must have at least two work pools available.</span></span> <span data-ttu-id="f5526-122">Töökaustade kuvamiseks ja lisamiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="f5526-122">To view and add work pools, follow these steps.</span></span>

1. <span data-ttu-id="f5526-123">Minge jaotisse **Laohaldus \> Seadistus \> Töö \> Töökaustad**.</span><span class="sxs-lookup"><span data-stu-id="f5526-123">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="f5526-124">Kui töötate ettevõtte **USMF** demoandmetega ja töötate läbi selles teemas hiljem esitatud näidisstsenaariumi, lisage kaks töökausta, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="f5526-124">If you're working with demo data from the **USMF** company and will work through the example scenario later in this topic, add two work pools that have the following settings:</span></span>

    - <span data-ttu-id="f5526-125">Töökaust 1:</span><span class="sxs-lookup"><span data-stu-id="f5526-125">Work pool 1:</span></span>

        - <span data-ttu-id="f5526-126">**Töökausta ID:** *E-pood*</span><span class="sxs-lookup"><span data-stu-id="f5526-126">**Work pool ID:** *Webshop*</span></span>
        - <span data-ttu-id="f5526-127">**Kirjeldus:** *E-pood*</span><span class="sxs-lookup"><span data-stu-id="f5526-127">**Description:** *Web Shop*</span></span>

    - <span data-ttu-id="f5526-128">Töökaust 2:</span><span class="sxs-lookup"><span data-stu-id="f5526-128">Work pool 2:</span></span>

        - <span data-ttu-id="f5526-129">**Töökausta ID:** *CallCenter*</span><span class="sxs-lookup"><span data-stu-id="f5526-129">**Work pool ID:** *CallCenter*</span></span>
        - <span data-ttu-id="f5526-130">**Kirjeldus:** *Kõnekeskus*</span><span class="sxs-lookup"><span data-stu-id="f5526-130">**Description:** *Call Center*</span></span>

1. <span data-ttu-id="f5526-131">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f5526-131">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="f5526-132">Töömallide häälestamine</span><span class="sxs-lookup"><span data-stu-id="f5526-132">Set up work templates</span></span>

<span data-ttu-id="f5526-133">Igale oma töömallile saate määrata vaikimisi töökausta vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="f5526-133">For each of your work templates, you can set a default work pool, as you require.</span></span> <span data-ttu-id="f5526-134">Iga asjakohase malli jaoks saate määrata töökausta veerus **Töökausta ID**.</span><span class="sxs-lookup"><span data-stu-id="f5526-134">For each relevant template, you assign a work pool in the **Work pool ID** column.</span></span> <span data-ttu-id="f5526-135">Sellisel juhul pärivad kõik antud malli abil loodud tööüksused automaatselt määratud töökausta.</span><span class="sxs-lookup"><span data-stu-id="f5526-135">In this case, all work items that are generated by using a given template automatically inherit the assigned work pool.</span></span> <span data-ttu-id="f5526-136">Kui töötate ettevõtte **USMF** demoandmetega ja töötate läbi selles teemas hiljem esitatud näidisstsenaariumi, järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="f5526-136">If you're working with the demo data from the **USMF** company and will work through the example scenario later in this topic, follow these steps.</span></span>

1. <span data-ttu-id="f5526-137">Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.</span><span class="sxs-lookup"><span data-stu-id="f5526-137">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="f5526-138">Lehe redigeerimisrežiimi panemiseks valige toimingupaanil **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="f5526-138">On the Action Pane, select **Edit** to put the page into editing mode.</span></span>
1. <span data-ttu-id="f5526-139">Redigeerige malli, seadistades järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f5526-139">Edit the template by setting the following values:</span></span>

    - <span data-ttu-id="f5526-140">**Töömall:** *62 pakendamiseks komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="f5526-140">**Work template:** *62 Pick to pack*</span></span>
    - <span data-ttu-id="f5526-141">**Töökausta ID:** *E-pood*</span><span class="sxs-lookup"><span data-stu-id="f5526-141">**Work pool ID:** *Webshop*</span></span>

1. <span data-ttu-id="f5526-142">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f5526-142">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="f5526-143">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="f5526-143">Example scenario</span></span>

<span data-ttu-id="f5526-144">Selles stsenaariumis näidatakse, kuidas muuta olemasoleva tööüksuse töötlemisvoogu, muutes selle töökausta.</span><span class="sxs-lookup"><span data-stu-id="f5526-144">This scenario shows how to change the stream of processing for an existing work item by changing its work pool.</span></span> <span data-ttu-id="f5526-145">See kasutab ettevõtte **USMF** demoandmeid ja selles teemas eelnevalt soovitatud sätteid.</span><span class="sxs-lookup"><span data-stu-id="f5526-145">It uses demo data from the **USMF** company and the settings that were suggested earlier in this topic.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="f5526-146">Müügitellimuse loomine ja selle väljastamine lattu</span><span class="sxs-lookup"><span data-stu-id="f5526-146">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="f5526-147">Kinnitage, et kaupadel *A0001* ja *A0002* oleks piisavalt vaba kaubavaru laos *62*.</span><span class="sxs-lookup"><span data-stu-id="f5526-147">Confirm that there is enough on-hand inventory for items *A0001* and *A0002* in warehouse *62*.</span></span> <span data-ttu-id="f5526-148">Avage jaotis **Varude haldus \> Päringud ja aruanded \> Vaba kaubavaru loend** ja redigeerige filtreid järgmiste juhiste järgi.</span><span class="sxs-lookup"><span data-stu-id="f5526-148">Go to **Inventory management \> Inquiries and reports \> On-hand list**, and edit the filters as shown here:</span></span>

    - <span data-ttu-id="f5526-149">Väärtuse **Ladu** alguses on *62*.</span><span class="sxs-lookup"><span data-stu-id="f5526-149">The **Warehouse** value begins with *62*.</span></span>
    - <span data-ttu-id="f5526-150">Väärtus **Kaubakood** on kas *A001* või *A002*.</span><span class="sxs-lookup"><span data-stu-id="f5526-150">The **Item number** value is either *A001* or *A002*.</span></span>

    <span data-ttu-id="f5526-151">Kõigi demoandmete kogus peaks olema 10.</span><span class="sxs-lookup"><span data-stu-id="f5526-151">Demo data should have a quantity of 10 each.</span></span>

    <span data-ttu-id="f5526-152">Järgmisena peate looma müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="f5526-152">Next, you must create a sales order.</span></span>

1. <span data-ttu-id="f5526-153">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="f5526-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="f5526-154">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f5526-154">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f5526-155">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f5526-155">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="f5526-156">**Kliendi konto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="f5526-156">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="f5526-157">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="f5526-157">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="f5526-158">Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5526-158">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="f5526-159">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="f5526-159">The new sales order is opened.</span></span> <span data-ttu-id="f5526-160">See peaks sisaldama uut tühja rida kiirkaardi **Müügitellimuse read** ruudustikus.</span><span class="sxs-lookup"><span data-stu-id="f5526-160">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="f5526-161">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f5526-161">On this line, set the following values:</span></span>

    - <span data-ttu-id="f5526-162">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="f5526-162">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="f5526-163">**Kogus:** *2*</span><span class="sxs-lookup"><span data-stu-id="f5526-163">**Quantity:** *2*</span></span>

1. <span data-ttu-id="f5526-164">Valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="f5526-164">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="f5526-165">Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida varud.</span><span class="sxs-lookup"><span data-stu-id="f5526-165">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="f5526-166">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f5526-166">Close the page.</span></span>
1. <span data-ttu-id="f5526-167">Valige kiirkaardil **Müügitellimuse read** suvand **Lisa rida**, et lisada teine rida müügitellimusse.</span><span class="sxs-lookup"><span data-stu-id="f5526-167">On the **Sales order lines** FastTab, select **Add line** to add another line to your sales order.</span></span> <span data-ttu-id="f5526-168">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f5526-168">On this line, set the following values:</span></span>

    - <span data-ttu-id="f5526-169">**Kauba kood:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="f5526-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="f5526-170">**Kogus:** *2*</span><span class="sxs-lookup"><span data-stu-id="f5526-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="f5526-171">Valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="f5526-171">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="f5526-172">Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida varud.</span><span class="sxs-lookup"><span data-stu-id="f5526-172">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="f5526-173">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f5526-173">Close the page.</span></span>
1. <span data-ttu-id="f5526-174">Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="f5526-174">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="f5526-175">Saate teabesõnumid, mis näitavad sellest väljastamisest loodud voo ID-d ja saadetise ID-d.</span><span class="sxs-lookup"><span data-stu-id="f5526-175">You receive informational messages that show the wave ID and shipment ID that were created from the release.</span></span> <span data-ttu-id="f5526-176">Märkige üles voo ID.</span><span class="sxs-lookup"><span data-stu-id="f5526-176">Make a note of the wave ID.</span></span>

### <a name="review-the-outbound-wave"></a><span data-ttu-id="f5526-177">Väljamineva voo ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="f5526-177">Review the outbound wave</span></span>

1. <span data-ttu-id="f5526-178">Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.</span><span class="sxs-lookup"><span data-stu-id="f5526-178">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="f5526-179">Otsige ruudustikust voo ID, mis loodi müügitellimuse väljastamisel.</span><span class="sxs-lookup"><span data-stu-id="f5526-179">In the grid, search for the wave ID that was created from the release of the sales order.</span></span>
1. <span data-ttu-id="f5526-180">Valige voo ID üksikasjade kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="f5526-180">Select the wave ID to view the details.</span></span>
1. <span data-ttu-id="f5526-181">Veenduge, et kiirkaardil **Voo read** oleks kuvatud müügitellimuse saadetise ID.</span><span class="sxs-lookup"><span data-stu-id="f5526-181">On the **Wave lines** FastTab, make sure that a shipment ID is shown for the sales order.</span></span>

    > [!TIP]
    > <span data-ttu-id="f5526-182">Kui suvandi **Töötle voogu lattu vabastamisel** väärtuseks on seatud *Ei* tarnevoo malli häälestuses, peate voogu käsitsi töötlema, valides toimingupaani vahekaardil **Voog** suvandi **Töötlemine**, et luua töö.</span><span class="sxs-lookup"><span data-stu-id="f5526-182">If the **Process wave at release to warehouse** option is set to *No* in the setup for the shipping wave template, you must manually process the wave by selecting **Process** from the **Wave** tab on the Action Pane to create work.</span></span>

1. <span data-ttu-id="f5526-183">Veenduge, et voog oleks töödeldud.</span><span class="sxs-lookup"><span data-stu-id="f5526-183">Make sure that the wave has been processed.</span></span> <span data-ttu-id="f5526-184">Töötlemine loob vajaliku töö.</span><span class="sxs-lookup"><span data-stu-id="f5526-184">This processing creates the required work.</span></span>

### <a name="view-work-details-and-change-the-work-pool"></a><span data-ttu-id="f5526-185">Töö üksikasjade kuvamine ja töökausta muutmine</span><span class="sxs-lookup"><span data-stu-id="f5526-185">View work details and change the work pool</span></span>

<span data-ttu-id="f5526-186">Saate kasutada lehte **Töö üksikasjad** loodud töö kuvamiseks ja töökausta haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="f5526-186">You can use the **Work details** page to view the work that was created and to manage the work pool.</span></span>

1. <span data-ttu-id="f5526-187">Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="f5526-187">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="f5526-188">Valige äsja loodud töö rida.</span><span class="sxs-lookup"><span data-stu-id="f5526-188">Select the row for the work that was just created.</span></span> <span data-ttu-id="f5526-189">Veerus **Tellimuse number** kuvatakse müügitellimuse number.</span><span class="sxs-lookup"><span data-stu-id="f5526-189">The **Order number** column will show the sales order number.</span></span>

    <span data-ttu-id="f5526-190">Väli **Töökausta ID** määratakse töömallis seadistatud töökausta ID jaoks.</span><span class="sxs-lookup"><span data-stu-id="f5526-190">The **Work pool ID** field will be set to the work pool ID that was set up in the work template.</span></span>

    > [!TIP]
    > <span data-ttu-id="f5526-191">Kui teile ei kuvata välja **Töökausta ID**, lisage veerg ruudustikku ja värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="f5526-191">If you don't see the **Work pool ID** field, add the column to the grid, and then refresh the page.</span></span>

1. <span data-ttu-id="f5526-192">Töö ID-ga seostatud töökausta muutmiseks, valige toimingupaani vahekaardil **Töö** suvand **Töökausta ID muutmine**.</span><span class="sxs-lookup"><span data-stu-id="f5526-192">To change the work pool that is associated with the work ID, on the Action Pane, on the **Work** tab, select **Change Work pool ID**.</span></span>
1. <span data-ttu-id="f5526-193">Valige dialoogiboksi **Muuda töökausta** kiirkaardi **Parameetrid** väljal **Töökausta ID** suvand *CallCenter*.</span><span class="sxs-lookup"><span data-stu-id="f5526-193">In the **Change work pool** dialog box, on the **Parameters** FastTab, in the **Work pool ID** field, select *CallCenter*.</span></span>
1. <span data-ttu-id="f5526-194">Muudatuse rakendamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5526-194">Select **OK** to apply your change.</span></span>
1. <span data-ttu-id="f5526-195">Pange tähele, et välja **Töökausta ID** väärtuseks on nüüd muudetud *CallCenter*.</span><span class="sxs-lookup"><span data-stu-id="f5526-195">Notice that the value of the **Work pool ID** field has now been changed to *CallCenter*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5526-196">Kui kuvatakse dialoogiboks **Muuda töökausta** võib väli **Töökausta ID** olla vaikimisi tühi.</span><span class="sxs-lookup"><span data-stu-id="f5526-196">When the **Change work pool** dialog box appears, the **Work pool ID** field might be blank by default.</span></span> <span data-ttu-id="f5526-197">Kui väli on tühi ja valite siis muudatuste rakendamiseks **OK**, eemaldatakse töökaust tööst täielikult.</span><span class="sxs-lookup"><span data-stu-id="f5526-197">If the field is blank when you select **OK** to apply changes, you will remove the work pool completely from the work.</span></span>
>
> <span data-ttu-id="f5526-198">Lisaks töökaustade vahetamisele, saate kasutada seda protseduuri töökausta lisamiseks mis tahes tööüksusele, millelt see puudub või töökausta eemaldamiseks tööüksusest, millel see on.</span><span class="sxs-lookup"><span data-stu-id="f5526-198">In addition to switching work pools, you can use this procedure to add a work pool to any work item that doesn't have one, or to remove a work pool from any work item that does have one.</span></span>
