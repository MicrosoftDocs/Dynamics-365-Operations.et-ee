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
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 61b988cf2501812e940f726e02d8fc1bcee2c035
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233051"
---
# <a name="change-work-pool-on-work"></a><span data-ttu-id="1a624-103">Muuda töö töökausta</span><span class="sxs-lookup"><span data-stu-id="1a624-103">Change work pool on work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a624-104">Töö korraldamiseks gruppidesse saate kasutada töökaustu.</span><span class="sxs-lookup"><span data-stu-id="1a624-104">You can use work pools to organize work into groups.</span></span> <span data-ttu-id="1a624-105">Näiteks saate luua töökausta kindlas laoasukohas toimuva töö klassifitseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="1a624-105">For example, you can create a work pool to classify work that occurs in a specific warehouse location.</span></span>

<span data-ttu-id="1a624-106">Funktsioon *Töö töökausta muutmine* lisab nupu **Muuda töökausta** tööüksuste toimingupaanile.</span><span class="sxs-lookup"><span data-stu-id="1a624-106">The *Change work pool on work* feature adds a **Change work pool** button to the Action Pane for work items.</span></span> <span data-ttu-id="1a624-107">Tänu sellele saavad laohaldurid hõlpsalt muuta olemasoleva töö töökausta.</span><span class="sxs-lookup"><span data-stu-id="1a624-107">Therefore, warehouse managers can easily change the work pool of existing work.</span></span> <span data-ttu-id="1a624-108">See funktsioon võimaldab halduritel kiiresti reageerida lao kaupluse korruse muudatustele ja see aitab parandada nende võimet kohaneda muutuvate olukordadega ja vajadusega viia töö üle teise töökausta.</span><span class="sxs-lookup"><span data-stu-id="1a624-108">This feature lets managers react quickly to changes on the warehouse shop floor, and it helps improve their ability to adapt to changing situations and the need to transfer work to another work pool.</span></span>

## <a name="turn-on-the-change-work-pool-on-work-feature"></a><span data-ttu-id="1a624-109">Funktsiooni Töö töökausta muutmine sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="1a624-109">Turn on the Change work pool on work feature</span></span>

<span data-ttu-id="1a624-110">Enne, kui alustate selle funktsiooni seadistamist või kasutamist, peate veenduma, et see oleks teie süsteemis saadaval.</span><span class="sxs-lookup"><span data-stu-id="1a624-110">Before you begin to set up or use this feature, you must make sure that it's available in your system.</span></span> <span data-ttu-id="1a624-111">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="1a624-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="1a624-112">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="1a624-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="1a624-113">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="1a624-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1a624-114">**Funktsiooni nimi:** *Töö töökausta muutmine*</span><span class="sxs-lookup"><span data-stu-id="1a624-114">**Feature name:** *Change work pool on work*</span></span>

## <a name="set-up-the-change-work-pool-on-work-feature"></a><span data-ttu-id="1a624-115">Funktsiooni Töö töökausta muutmine seadistamine</span><span class="sxs-lookup"><span data-stu-id="1a624-115">Set up the Change work pool on work feature</span></span>

<span data-ttu-id="1a624-116">Selle funktsiooni kasutamiseks peavad teil olema seadistatud mõned töökaustad.</span><span class="sxs-lookup"><span data-stu-id="1a624-116">To use this feature, you must have some work pools set up.</span></span> <span data-ttu-id="1a624-117">Samuti võite seadistada töömallid, et need määraksid automaatselt kausta.</span><span class="sxs-lookup"><span data-stu-id="1a624-117">You might also set up your work templates so that they automatically assign a pool.</span></span> <span data-ttu-id="1a624-118">Kui soovite töötada läbi hiljem selles teemas käsitletava näidisstsenaariumi, seadistage oma süsteem selles jaotises kirjeldatud viisil.</span><span class="sxs-lookup"><span data-stu-id="1a624-118">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span>

### <a name="set-up-work-pools"></a><span data-ttu-id="1a624-119">Töökaustade seadistamine</span><span class="sxs-lookup"><span data-stu-id="1a624-119">Set up work pools</span></span>

<span data-ttu-id="1a624-120">Töökaustad võimaldavad teil korraldada tööüksusi tüübi järgi.</span><span class="sxs-lookup"><span data-stu-id="1a624-120">Work pools let you organize work items by type.</span></span> <span data-ttu-id="1a624-121">Funktsiooniga *Töö töökausta muutmine* töötamiseks peab teil olema saadaval vähemalt kaks töökausta.</span><span class="sxs-lookup"><span data-stu-id="1a624-121">To work with the *Change work pool on work* feature, you must have at least two work pools available.</span></span> <span data-ttu-id="1a624-122">Töökaustade kuvamiseks ja lisamiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="1a624-122">To view and add work pools, follow these steps.</span></span>

1. <span data-ttu-id="1a624-123">Minge jaotisse **Laohaldus \> Seadistus \> Töö \> Töökaustad**.</span><span class="sxs-lookup"><span data-stu-id="1a624-123">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="1a624-124">Kui töötate ettevõtte **USMF** demoandmetega ja töötate läbi selles teemas hiljem esitatud näidisstsenaariumi, lisage kaks töökausta, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="1a624-124">If you're working with demo data from the **USMF** company and will work through the example scenario later in this topic, add two work pools that have the following settings:</span></span>

    - <span data-ttu-id="1a624-125">Töökaust 1:</span><span class="sxs-lookup"><span data-stu-id="1a624-125">Work pool 1:</span></span>

        - <span data-ttu-id="1a624-126">**Töökausta ID:** *E-pood*</span><span class="sxs-lookup"><span data-stu-id="1a624-126">**Work pool ID:** *Webshop*</span></span>
        - <span data-ttu-id="1a624-127">**Kirjeldus:** *E-pood*</span><span class="sxs-lookup"><span data-stu-id="1a624-127">**Description:** *Web Shop*</span></span>

    - <span data-ttu-id="1a624-128">Töökaust 2:</span><span class="sxs-lookup"><span data-stu-id="1a624-128">Work pool 2:</span></span>

        - <span data-ttu-id="1a624-129">**Töökausta ID:** *CallCenter*</span><span class="sxs-lookup"><span data-stu-id="1a624-129">**Work pool ID:** *CallCenter*</span></span>
        - <span data-ttu-id="1a624-130">**Kirjeldus:** *Kõnekeskus*</span><span class="sxs-lookup"><span data-stu-id="1a624-130">**Description:** *Call Center*</span></span>

1. <span data-ttu-id="1a624-131">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1a624-131">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="1a624-132">Töömallide häälestamine</span><span class="sxs-lookup"><span data-stu-id="1a624-132">Set up work templates</span></span>

<span data-ttu-id="1a624-133">Igale oma töömallile saate määrata vaikimisi töökausta vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="1a624-133">For each of your work templates, you can set a default work pool, as you require.</span></span> <span data-ttu-id="1a624-134">Iga asjakohase malli jaoks saate määrata töökausta veerus **Töökausta ID**.</span><span class="sxs-lookup"><span data-stu-id="1a624-134">For each relevant template, you assign a work pool in the **Work pool ID** column.</span></span> <span data-ttu-id="1a624-135">Sellisel juhul pärivad kõik antud malli abil loodud tööüksused automaatselt määratud töökausta.</span><span class="sxs-lookup"><span data-stu-id="1a624-135">In this case, all work items that are generated by using a given template automatically inherit the assigned work pool.</span></span> <span data-ttu-id="1a624-136">Kui töötate ettevõtte **USMF** demoandmetega ja töötate läbi selles teemas hiljem esitatud näidisstsenaariumi, järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="1a624-136">If you're working with the demo data from the **USMF** company and will work through the example scenario later in this topic, follow these steps.</span></span>

1. <span data-ttu-id="1a624-137">Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.</span><span class="sxs-lookup"><span data-stu-id="1a624-137">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="1a624-138">Lehe redigeerimisrežiimi panemiseks valige toimingupaanil **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="1a624-138">On the Action Pane, select **Edit** to put the page into editing mode.</span></span>
1. <span data-ttu-id="1a624-139">Redigeerige malli, seadistades järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="1a624-139">Edit the template by setting the following values:</span></span>

    - <span data-ttu-id="1a624-140">**Töömall:** *62 pakendamiseks komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="1a624-140">**Work template:** *62 Pick to pack*</span></span>
    - <span data-ttu-id="1a624-141">**Töökausta ID:** *E-pood*</span><span class="sxs-lookup"><span data-stu-id="1a624-141">**Work pool ID:** *Webshop*</span></span>

1. <span data-ttu-id="1a624-142">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1a624-142">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="1a624-143">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="1a624-143">Example scenario</span></span>

<span data-ttu-id="1a624-144">Selles stsenaariumis näidatakse, kuidas muuta olemasoleva tööüksuse töötlemisvoogu, muutes selle töökausta.</span><span class="sxs-lookup"><span data-stu-id="1a624-144">This scenario shows how to change the stream of processing for an existing work item by changing its work pool.</span></span> <span data-ttu-id="1a624-145">See kasutab ettevõtte **USMF** demoandmeid ja selles teemas eelnevalt soovitatud sätteid.</span><span class="sxs-lookup"><span data-stu-id="1a624-145">It uses demo data from the **USMF** company and the settings that were suggested earlier in this topic.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="1a624-146">Müügitellimuse loomine ja selle väljastamine lattu</span><span class="sxs-lookup"><span data-stu-id="1a624-146">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="1a624-147">Kinnitage, et kaupadel *A0001* ja *A0002* oleks piisavalt vaba kaubavaru laos *62*.</span><span class="sxs-lookup"><span data-stu-id="1a624-147">Confirm that there is enough on-hand inventory for items *A0001* and *A0002* in warehouse *62*.</span></span> <span data-ttu-id="1a624-148">Avage jaotis **Varude haldus \> Päringud ja aruanded \> Vaba kaubavaru loend** ja redigeerige filtreid järgmiste juhiste järgi.</span><span class="sxs-lookup"><span data-stu-id="1a624-148">Go to **Inventory management \> Inquiries and reports \> On-hand list**, and edit the filters as shown here:</span></span>

    - <span data-ttu-id="1a624-149">Väärtuse **Ladu** alguses on *62*.</span><span class="sxs-lookup"><span data-stu-id="1a624-149">The **Warehouse** value begins with *62*.</span></span>
    - <span data-ttu-id="1a624-150">Väärtus **Kaubakood** on kas *A001* või *A002*.</span><span class="sxs-lookup"><span data-stu-id="1a624-150">The **Item number** value is either *A001* or *A002*.</span></span>

    <span data-ttu-id="1a624-151">Kõigi demoandmete kogus peaks olema 10.</span><span class="sxs-lookup"><span data-stu-id="1a624-151">Demo data should have a quantity of 10 each.</span></span>

    <span data-ttu-id="1a624-152">Järgmisena peate looma müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="1a624-152">Next, you must create a sales order.</span></span>

1. <span data-ttu-id="1a624-153">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="1a624-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="1a624-154">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1a624-154">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1a624-155">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="1a624-155">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="1a624-156">**Kliendi konto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="1a624-156">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="1a624-157">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="1a624-157">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="1a624-158">Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a624-158">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="1a624-159">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="1a624-159">The new sales order is opened.</span></span> <span data-ttu-id="1a624-160">See peaks sisaldama uut tühja rida kiirkaardi **Müügitellimuse read** ruudustikus.</span><span class="sxs-lookup"><span data-stu-id="1a624-160">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="1a624-161">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="1a624-161">On this line, set the following values:</span></span>

    - <span data-ttu-id="1a624-162">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="1a624-162">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="1a624-163">**Kogus:** *2*</span><span class="sxs-lookup"><span data-stu-id="1a624-163">**Quantity:** *2*</span></span>

1. <span data-ttu-id="1a624-164">Valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="1a624-164">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="1a624-165">Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida varud.</span><span class="sxs-lookup"><span data-stu-id="1a624-165">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="1a624-166">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1a624-166">Close the page.</span></span>
1. <span data-ttu-id="1a624-167">Valige kiirkaardil **Müügitellimuse read** suvand **Lisa rida**, et lisada teine rida müügitellimusse.</span><span class="sxs-lookup"><span data-stu-id="1a624-167">On the **Sales order lines** FastTab, select **Add line** to add another line to your sales order.</span></span> <span data-ttu-id="1a624-168">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="1a624-168">On this line, set the following values:</span></span>

    - <span data-ttu-id="1a624-169">**Kauba kood:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="1a624-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="1a624-170">**Kogus:** *2*</span><span class="sxs-lookup"><span data-stu-id="1a624-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="1a624-171">Valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="1a624-171">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="1a624-172">Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida varud.</span><span class="sxs-lookup"><span data-stu-id="1a624-172">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="1a624-173">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1a624-173">Close the page.</span></span>
1. <span data-ttu-id="1a624-174">Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="1a624-174">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="1a624-175">Saate teabesõnumid, mis näitavad sellest väljastamisest loodud voo ID-d ja saadetise ID-d.</span><span class="sxs-lookup"><span data-stu-id="1a624-175">You receive informational messages that show the wave ID and shipment ID that were created from the release.</span></span> <span data-ttu-id="1a624-176">Märkige üles voo ID.</span><span class="sxs-lookup"><span data-stu-id="1a624-176">Make a note of the wave ID.</span></span>

### <a name="review-the-outbound-wave"></a><span data-ttu-id="1a624-177">Väljamineva voo ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="1a624-177">Review the outbound wave</span></span>

1. <span data-ttu-id="1a624-178">Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.</span><span class="sxs-lookup"><span data-stu-id="1a624-178">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="1a624-179">Otsige ruudustikust voo ID, mis loodi müügitellimuse väljastamisel.</span><span class="sxs-lookup"><span data-stu-id="1a624-179">In the grid, search for the wave ID that was created from the release of the sales order.</span></span>
1. <span data-ttu-id="1a624-180">Valige voo ID üksikasjade kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="1a624-180">Select the wave ID to view the details.</span></span>
1. <span data-ttu-id="1a624-181">Veenduge, et kiirkaardil **Voo read** oleks kuvatud müügitellimuse saadetise ID.</span><span class="sxs-lookup"><span data-stu-id="1a624-181">On the **Wave lines** FastTab, make sure that a shipment ID is shown for the sales order.</span></span>

    > [!TIP]
    > <span data-ttu-id="1a624-182">Kui suvandi **Töötle voogu lattu vabastamisel** väärtuseks on seatud *Ei* tarnevoo malli häälestuses, peate voogu käsitsi töötlema, valides toimingupaani vahekaardil **Voog** suvandi **Töötlemine**, et luua töö.</span><span class="sxs-lookup"><span data-stu-id="1a624-182">If the **Process wave at release to warehouse** option is set to *No* in the setup for the shipping wave template, you must manually process the wave by selecting **Process** from the **Wave** tab on the Action Pane to create work.</span></span>

1. <span data-ttu-id="1a624-183">Veenduge, et voog oleks töödeldud.</span><span class="sxs-lookup"><span data-stu-id="1a624-183">Make sure that the wave has been processed.</span></span> <span data-ttu-id="1a624-184">Töötlemine loob vajaliku töö.</span><span class="sxs-lookup"><span data-stu-id="1a624-184">This processing creates the required work.</span></span>

### <a name="view-work-details-and-change-the-work-pool"></a><span data-ttu-id="1a624-185">Töö üksikasjade kuvamine ja töökausta muutmine</span><span class="sxs-lookup"><span data-stu-id="1a624-185">View work details and change the work pool</span></span>

<span data-ttu-id="1a624-186">Saate kasutada lehte **Töö üksikasjad** loodud töö kuvamiseks ja töökausta haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="1a624-186">You can use the **Work details** page to view the work that was created and to manage the work pool.</span></span>

1. <span data-ttu-id="1a624-187">Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="1a624-187">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="1a624-188">Valige äsja loodud töö rida.</span><span class="sxs-lookup"><span data-stu-id="1a624-188">Select the row for the work that was just created.</span></span> <span data-ttu-id="1a624-189">Veerus **Tellimuse number** kuvatakse müügitellimuse number.</span><span class="sxs-lookup"><span data-stu-id="1a624-189">The **Order number** column will show the sales order number.</span></span>

    <span data-ttu-id="1a624-190">Väli **Töökausta ID** määratakse töömallis seadistatud töökausta ID jaoks.</span><span class="sxs-lookup"><span data-stu-id="1a624-190">The **Work pool ID** field will be set to the work pool ID that was set up in the work template.</span></span>

    > [!TIP]
    > <span data-ttu-id="1a624-191">Kui teile ei kuvata välja **Töökausta ID**, lisage veerg ruudustikku ja värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="1a624-191">If you don't see the **Work pool ID** field, add the column to the grid, and then refresh the page.</span></span>

1. <span data-ttu-id="1a624-192">Töö ID-ga seostatud töökausta muutmiseks, valige toimingupaani vahekaardil **Töö** suvand **Töökausta ID muutmine**.</span><span class="sxs-lookup"><span data-stu-id="1a624-192">To change the work pool that is associated with the work ID, on the Action Pane, on the **Work** tab, select **Change Work pool ID**.</span></span>
1. <span data-ttu-id="1a624-193">Valige dialoogiboksi **Muuda töökausta** kiirkaardi **Parameetrid** väljal **Töökausta ID** suvand *CallCenter*.</span><span class="sxs-lookup"><span data-stu-id="1a624-193">In the **Change work pool** dialog box, on the **Parameters** FastTab, in the **Work pool ID** field, select *CallCenter*.</span></span>
1. <span data-ttu-id="1a624-194">Muudatuse rakendamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a624-194">Select **OK** to apply your change.</span></span>
1. <span data-ttu-id="1a624-195">Pange tähele, et välja **Töökausta ID** väärtuseks on nüüd muudetud *CallCenter*.</span><span class="sxs-lookup"><span data-stu-id="1a624-195">Notice that the value of the **Work pool ID** field has now been changed to *CallCenter*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1a624-196">Kui kuvatakse dialoogiboks **Muuda töökausta** võib väli **Töökausta ID** olla vaikimisi tühi.</span><span class="sxs-lookup"><span data-stu-id="1a624-196">When the **Change work pool** dialog box appears, the **Work pool ID** field might be blank by default.</span></span> <span data-ttu-id="1a624-197">Kui väli on tühi ja valite siis muudatuste rakendamiseks **OK**, eemaldatakse töökaust tööst täielikult.</span><span class="sxs-lookup"><span data-stu-id="1a624-197">If the field is blank when you select **OK** to apply changes, you will remove the work pool completely from the work.</span></span>
>
> <span data-ttu-id="1a624-198">Lisaks töökaustade vahetamisele, saate kasutada seda protseduuri töökausta lisamiseks mis tahes tööüksusele, millelt see puudub või töökausta eemaldamiseks tööüksusest, millel see on.</span><span class="sxs-lookup"><span data-stu-id="1a624-198">In addition to switching work pools, you can use this procedure to add a work pool to any work item that doesn't have one, or to remove a work pool from any work item that does have one.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]