---
title: Tsooniläve täiendamine
description: Tsoonipõhine täiendamine kasutab minimaalse/maksimaakse (min/max) täiendamise strateegiat, kuid see hindab üksikute asukohtade asemel ainult terveid laotsoone. Tänu sellele saavad laohaldurid kiiremini teada, kui komplekteerimistsoonis on vaja täiendavat varu.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d0a97ed7b01a32e9276433713448a672f83f7d02
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814364"
---
# <a name="zone-threshold-replenishment"></a><span data-ttu-id="b7c98-104">Tsooniläve täiendamine</span><span class="sxs-lookup"><span data-stu-id="b7c98-104">Zone threshold replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7c98-105">Tsoonipõhine täiendamine kasutab minimaalse/maksimaakse (min/max) [täiendamise](replenishment.md) strateegiat, kuid see hindab üksikute asukohtade asemel ainult terveid laotsoone.</span><span class="sxs-lookup"><span data-stu-id="b7c98-105">Zone-based replenishment uses a minimum/maximum (min/max) [replenishment](replenishment.md) strategy, but it evaluates whole warehouse zones instead of just individual locations.</span></span> <span data-ttu-id="b7c98-106">Tänu sellele saavad laohaldurid kiiremini teada, kui komplekteerimistsoonis on vaja täiendavat varu.</span><span class="sxs-lookup"><span data-stu-id="b7c98-106">Therefore, warehouse managers can more quickly learn when additional inventory is required in a picking zone.</span></span>

<span data-ttu-id="b7c98-107">Selle funktsiooni seadistus sarnaneb asukohapõhise täiendamise seadistusele.</span><span class="sxs-lookup"><span data-stu-id="b7c98-107">The setup for this feature resembles the setup for location-based replenishment.</span></span> <span data-ttu-id="b7c98-108">Kuid min/max täiendamise malli seadistamise ajal saate ka määrata, kas läve tuleks hinnata asukoha või tsooni põhjal.</span><span class="sxs-lookup"><span data-stu-id="b7c98-108">However, when you set up a template for min/max replenishment, you can also specify whether the threshold should be evaluated per location or per zone.</span></span> <span data-ttu-id="b7c98-109">Kui seadistate tsoonidel põhineva hindamise, peate tsooni valiku päringule lisama kindlad tsoonid.</span><span class="sxs-lookup"><span data-stu-id="b7c98-109">If you set up evaluation that is based on zones, you must add specific zones to the zone selection query.</span></span>

<span data-ttu-id="b7c98-110">Sarnaselt asukohapõhisele min/max täiendamisele, põhineb tsoonipõhine min/max täiendamine minimaalse varu läve häälestusel, mis käivitab valitud kaupade täiendamise töö loomise.</span><span class="sxs-lookup"><span data-stu-id="b7c98-110">Like location-based min/max replenishment, zone-based min/max replenishment is based the setup of a minimum inventory threshold that triggers the creation of replenishment work for selected items.</span></span> <span data-ttu-id="b7c98-111">See täiendamise töö suurendab varusid selle tsooni jaoks määratud maksimaalse läveni.</span><span class="sxs-lookup"><span data-stu-id="b7c98-111">This replenishment work will increase inventory up to the specified maximum threshold for the zone.</span></span>

> [!NOTE]
> <span data-ttu-id="b7c98-112">Praeguses väljalaskes ei toetata tootevariantide tsooni täiendamise protsesse.</span><span class="sxs-lookup"><span data-stu-id="b7c98-112">Zone replenishment processes for product variants aren't supported in the current release.</span></span>


<span data-ttu-id="b7c98-113">Erinevalt asukohapõhisest min/max täiendamisest, ei nõua tsoonipõhine min/max täiendamine fikseeritud asukohti selle hindamiseks, kas asukohad peaksid ladustama kindlat kaupa.</span><span class="sxs-lookup"><span data-stu-id="b7c98-113">Unlike location-based min/max replenishment, zone-based min/max replenishment doesn't require fixed locations to evaluate whether locations should store a specific item.</span></span> <span data-ttu-id="b7c98-114">Tänu sellele võimaldab tsoonipõhine täiendamine kasutada min/max täiendamist ka siis, kui teil pole laos iga kauba või kaubavariandi jaoks fikseeritud asukohti.</span><span class="sxs-lookup"><span data-stu-id="b7c98-114">Therefore, zone-based replenishment lets you use min/max replenishment even if you don't have fixed locations for each item or item variant in the warehouse.</span></span> <span data-ttu-id="b7c98-115">Kui tsoonis langeb kogus määratud lävest allapoole, luuakse täiendamise töö.</span><span class="sxs-lookup"><span data-stu-id="b7c98-115">When a quantity in the zone falls below the specified minimum threshold, replenishment work is created.</span></span> <span data-ttu-id="b7c98-116">Asukohakorraldused määravad, millisesse kindlasse asukohta varud tuleks panna.</span><span class="sxs-lookup"><span data-stu-id="b7c98-116">Location directives will determine which specific location the inventory should be put into.</span></span>

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a><span data-ttu-id="b7c98-117">Funktsiooni Tsooniläve täiendamine sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="b7c98-117">Turn on the Zone threshold replenishment feature</span></span>

<span data-ttu-id="b7c98-118">Enne funktsiooni *Tsooniläve täiendamine* kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="b7c98-118">Before you can use the *Zone threshold replenishment* feature, it must be turned on in your system.</span></span> <span data-ttu-id="b7c98-119">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="b7c98-119">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b7c98-120">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="b7c98-120">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b7c98-121">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="b7c98-121">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b7c98-122">**Funktsiooni nimi:** *Tsooniläve täiendamine*</span><span class="sxs-lookup"><span data-stu-id="b7c98-122">**Feature name:** *Zone threshold replenishment*</span></span>

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a><span data-ttu-id="b7c98-123">Tsoonipõhise täiendamise häälestus</span><span class="sxs-lookup"><span data-stu-id="b7c98-123">Set up zone-based replenishment</span></span>

<span data-ttu-id="b7c98-124">Tsoonipõhise täiendamise seadistamiseks peate konfigureerima süsteemi mitu osa.</span><span class="sxs-lookup"><span data-stu-id="b7c98-124">To set up zone-based replenishment, you must configure several parts of the system.</span></span> <span data-ttu-id="b7c98-125">Selles jaotises tutvustatakse erinevaid sätteid ja esitatakse demoandmete väärtuseid, mida saate sisestada, kui soovite kasutada selle teema lõpus olevat stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="b7c98-125">This section introduces the various settings and provides demo data values that you can enter if you want to work through the scenario at the end of this topic.</span></span>

### <a name="set-up-directive-codes"></a><span data-ttu-id="b7c98-126">Korralduskoodide häälestus</span><span class="sxs-lookup"><span data-stu-id="b7c98-126">Set up directive codes</span></span>

<span data-ttu-id="b7c98-127">[Korralduskoodid](control-warehouse-location-directives.md) võimaldavad teil täpsemalt määratleda asukohamalli, mida kasutatakse töömallis.</span><span class="sxs-lookup"><span data-stu-id="b7c98-127">[Directive codes](control-warehouse-location-directives.md) let you be more specific when you define the location template that is used in a work template.</span></span> <span data-ttu-id="b7c98-128">Iga koodiga luuakse ühine väärtus, millele saate viidata iga mallitüübi konfigureerimisel.</span><span class="sxs-lookup"><span data-stu-id="b7c98-128">Each code establishes a common value that you can refer to when you configure each type of template.</span></span>

#### <a name="view-and-edit-directive-codes"></a><span data-ttu-id="b7c98-129">Korralduskoodide kuvamine ja redigeerimine</span><span class="sxs-lookup"><span data-stu-id="b7c98-129">View and edit directive codes</span></span>

<span data-ttu-id="b7c98-130">Oma korralduskoodide kuvamiseks või redigeerimiseks avage jaotis **Laohaldus \> Häälestus \> Korralduskoodid**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-130">To view or edit your directive codes, go to **Warehouse management \> Setup \> Directive codes**.</span></span>

#### <a name="prepare-demo-data-directive-codes"></a><span data-ttu-id="b7c98-131">Demoandmete korralduskoodide ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="b7c98-131">Prepare demo data directive codes</span></span>

<span data-ttu-id="b7c98-132">Selles näites kirjeldatakse, kuidas valmistada ette korralduskoodi.</span><span class="sxs-lookup"><span data-stu-id="b7c98-132">This example shows how to prepare a directive code.</span></span> <span data-ttu-id="b7c98-133">Kui kavatsete kasutada selle teema lõpus olevat stsenaariumi, kasutage siin esitatud demoandmete väärtusi.</span><span class="sxs-lookup"><span data-stu-id="b7c98-133">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="b7c98-134">Muul juhul saate kasutada oma väärtusi.</span><span class="sxs-lookup"><span data-stu-id="b7c98-134">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="b7c98-135">Valige juriidiline isik **USMF** demoandmetega töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="b7c98-135">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="b7c98-136">Avage jaotis **Laohaldus \> Seadistus \> Korralduskoodid**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-136">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="b7c98-137">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="b7c98-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="b7c98-138">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b7c98-138">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b7c98-139">**Korralduskood:** _Tsooni täiend_</span><span class="sxs-lookup"><span data-stu-id="b7c98-139">**Directive code:** _Zone replen_</span></span>
    - <span data-ttu-id="b7c98-140">**Korralduse kirjeldus:** _Tsooni täiendamine_</span><span class="sxs-lookup"><span data-stu-id="b7c98-140">**Directive description:** _Zone replenishment_</span></span>

1. <span data-ttu-id="b7c98-141">Uue koodi salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-141">Select **Save** to save the new code.</span></span>

### <a name="set-up-replenishment-templates"></a><span data-ttu-id="b7c98-142">Täiendamismallide häälestamine</span><span class="sxs-lookup"><span data-stu-id="b7c98-142">Set up replenishment templates</span></span>

<span data-ttu-id="b7c98-143">[Min/max täiendamismallid](tasks/set-up-min-max-replenishment-process.md) on põhimehhanism komplekteerimiskohtades optimaalsete tasemete säilitamiseks.</span><span class="sxs-lookup"><span data-stu-id="b7c98-143">[Min/max replenishment templates](tasks/set-up-min-max-replenishment-process.md) are the primary mechanism for maintaining optimal levels in picking locations.</span></span> <span data-ttu-id="b7c98-144">Nendes mallides peate seadistama reeglid, mida kasutatakse laovarude täiendamiseks.</span><span class="sxs-lookup"><span data-stu-id="b7c98-144">In these templates, you must set up the rules that will be used to replenish inventory in the warehouse.</span></span> <span data-ttu-id="b7c98-145">Täiendamise hulka, mille jaoks saab malle kasutada, kuulub ka tsoonipõhine täiendamine.</span><span class="sxs-lookup"><span data-stu-id="b7c98-145">The replenishment that the templates can be used for includes zone-based replenishment.</span></span>

#### <a name="view-and-edit-replenishment-templates"></a><span data-ttu-id="b7c98-146">Täiendamismallide kuvamine ja redigeerimine</span><span class="sxs-lookup"><span data-stu-id="b7c98-146">View and edit replenishment templates</span></span>

<span data-ttu-id="b7c98-147">Täiendamismall on reeglistik, mis määrab asikoha täiendamise aja ja viisi.</span><span class="sxs-lookup"><span data-stu-id="b7c98-147">A replenishment template is a set of rules that control when and how a location is replenished.</span></span> <span data-ttu-id="b7c98-148">Saate valida malli täiendamise tegemise aja ja viisi juhtimiseks.</span><span class="sxs-lookup"><span data-stu-id="b7c98-148">You select a template to control when and how replenishment is done.</span></span> <span data-ttu-id="b7c98-149">Täiendamismallide kuvamiseks ja redigeerimiseks avage jaotis **Laohaldus \> Seadistus \> Täiendamine \> Täiendamismallid**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-149">To view or edit your replenishment templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>

#### <a name="prepare-a-demo-data-replenishment-template"></a><span data-ttu-id="b7c98-150">Demoandmete täiendamismalli ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="b7c98-150">Prepare a demo data replenishment template</span></span>

<span data-ttu-id="b7c98-151">Selles näites kirjeldatakse, kuidas valmistada ette täiendamismalli.</span><span class="sxs-lookup"><span data-stu-id="b7c98-151">This example shows how to prepare a replenishment template.</span></span> <span data-ttu-id="b7c98-152">Kui kavatsete kasutada selle teema lõpus olevat stsenaariumi, kasutage siin esitatud demoandmete väärtusi.</span><span class="sxs-lookup"><span data-stu-id="b7c98-152">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="b7c98-153">Muul juhul saate kasutada oma väärtusi.</span><span class="sxs-lookup"><span data-stu-id="b7c98-153">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="b7c98-154">Valige juriidiline isik **USMF** demoandmetega töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="b7c98-154">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="b7c98-155">Avage jaotis **Laohaldus \> Seadistus \> Täiendamine \> Täiendamismallid**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-155">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="b7c98-156">Lehe redigeerimisrežiimi panemiseks valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-156">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="b7c98-157">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida **Ülevaade**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-157">On the Action Pane, select **New** to add a row to the **Overview** grid.</span></span>
1. <span data-ttu-id="b7c98-158">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b7c98-158">In the new row, set the following values.</span></span> <span data-ttu-id="b7c98-159">Võtke vastu vaikeväärtused kõigil teistel väljadel.</span><span class="sxs-lookup"><span data-stu-id="b7c98-159">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="b7c98-160">**Täiendamismall:** _Tsooni min/max täiend_</span><span class="sxs-lookup"><span data-stu-id="b7c98-160">**Replenish template:** _Zone min/max replen_</span></span>
    - <span data-ttu-id="b7c98-161">**Kirjeldus:** _Tsooni min/max täiendamine_</span><span class="sxs-lookup"><span data-stu-id="b7c98-161">**Description:** _Zone min/max replenishment_</span></span>
    - <span data-ttu-id="b7c98-162">**Täiendamise tüüp:** _Minimaalne või maksimaalne_</span><span class="sxs-lookup"><span data-stu-id="b7c98-162">**Replenishment type:** _Minimum or maximum_</span></span>

1. <span data-ttu-id="b7c98-163">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-163">Select **Save**.</span></span>
1. <span data-ttu-id="b7c98-164">Kui uus rida on valitud ruudustikus **Ülevaade**, valige ruudustiku **Täiendamismalli üksikasjad** kohalt suvand **Uus**, et lisada rida, mis on seostatud teie äsja loodud täiendamismalliga *Tsooni min/max. täiend*.</span><span class="sxs-lookup"><span data-stu-id="b7c98-164">While the new row is still selected in the **Overview** grid, select **New** above the **Replenishment Template Details** grid to add a row that is associated with the *Zone Min/Max replen* replenishment template that you just created.</span></span>
1. <span data-ttu-id="b7c98-165">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b7c98-165">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b7c98-166">**Järjekorranumber:** sisestage _1_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-166">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b7c98-167">**Kirjeldus:** Sisestage _Komplekteerimistsooni täiendamine_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-167">**Description:** Enter _Pick zone replenishment_.</span></span>
    - <span data-ttu-id="b7c98-168">**Täiendamise ühik:** valige _ea_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-168">**Replenishment unit:** Select _ea_.</span></span>
    - <span data-ttu-id="b7c98-169">**Taotluse tüüp:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="b7c98-169">**Request type:** Leave this field blank.</span></span>
    - <span data-ttu-id="b7c98-170">**Korralduse kood:** see väli seob täiendamismalli asukohakorraldusega.</span><span class="sxs-lookup"><span data-stu-id="b7c98-170">**Directive code:** This field links the replenishment template with a location directive.</span></span> <span data-ttu-id="b7c98-171">Valige eelnevalt loodud demoandmete korralduskood (_Tsooni täiend_).</span><span class="sxs-lookup"><span data-stu-id="b7c98-171">Select the demo data directive code that you created earlier (_Zone replen_).</span></span>
    - <span data-ttu-id="b7c98-172">**Töömall:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="b7c98-172">**Work template:** Leave this field blank.</span></span>
    - <span data-ttu-id="b7c98-173">**Minimaalne kogus:** see väli määrab koguse, mille puhul täiendamine käivitatakse.</span><span class="sxs-lookup"><span data-stu-id="b7c98-173">**Minimum quantity:** This field sets the quantity that replenishment will be triggered at.</span></span> <span data-ttu-id="b7c98-174">Sisestage _50_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-174">Enter _50_.</span></span>
    - <span data-ttu-id="b7c98-175">**Maksimaalne kogus:** see väli määrab kauba maksimaalse koguse, mis võib tsoonis olla.</span><span class="sxs-lookup"><span data-stu-id="b7c98-175">**Maximum quantity:** This field sets the maximum quantity of an item that can be present in a zone.</span></span> <span data-ttu-id="b7c98-176">Loodud varude täiendamistöö suurendab varud sellele kogusele.</span><span class="sxs-lookup"><span data-stu-id="b7c98-176">Generated replenishment work will increase inventory to this quantity.</span></span> <span data-ttu-id="b7c98-177">Sisestage _150_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-177">Enter _150_.</span></span>
    - <span data-ttu-id="b7c98-178">**Ühik:** see väli määrab minimaalse ja maksimaalse väärtuse ühiku.</span><span class="sxs-lookup"><span data-stu-id="b7c98-178">**Unit:** This field sets the unit for the minimum and maximum values.</span></span> <span data-ttu-id="b7c98-179">Valige _ea_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-179">Select _ea_.</span></span>
    - <span data-ttu-id="b7c98-180">**Nõudluse juurdekasv:** valige _Ümardamine üles_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-180">**Demand increment:** Select _Round up_.</span></span>
    - <span data-ttu-id="b7c98-181">**Tühjade fikseeritud asukohtade täiendamine:** valige see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="b7c98-181">**Replenish empty fixed locations:** Select this check box.</span></span>
    - <span data-ttu-id="b7c98-182">**Ainult fikseeritud asukohtade täiendamine:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="b7c98-182">**Replenish only fixed locations:** Clear this check box.</span></span>
    - <span data-ttu-id="b7c98-183">**Toote päringu režiim:** valige _Toote päring_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-183">**Product query mode:** Select _Product query_.</span></span>
    - <span data-ttu-id="b7c98-184">**Täiendamise läve ulatus:** see väli määratleb, kas mall peaks hindama tsooni või kindla asukoha alusel.</span><span class="sxs-lookup"><span data-stu-id="b7c98-184">**Replenishment threshold scope:** This field defines whether the template should evaluate by zone or by specific location.</span></span> <span data-ttu-id="b7c98-185">Valige _Tsoon_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-185">Select _Zone_.</span></span>
    - <span data-ttu-id="b7c98-186">**Ladu:** valige _61_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-186">**Warehouse:** Select _61_.</span></span>

1. <span data-ttu-id="b7c98-187">Valige ruudustiku **Täiendamismalli üksikasjad** kohalt **Toodete valimine**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-187">Select **Select products** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="b7c98-188">Valige dialoogiboksi **Toote päring** vahekaardil **Vahemik** suvand **Lisa**, et lisada rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="b7c98-188">In the **Product query** dialog box, on the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="b7c98-189">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b7c98-189">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b7c98-190">**Tabel:** _Kaubad_</span><span class="sxs-lookup"><span data-stu-id="b7c98-190">**Table:** _Items_</span></span>
    - <span data-ttu-id="b7c98-191">**Tuletatud tabel:** _Kaubad_</span><span class="sxs-lookup"><span data-stu-id="b7c98-191">**Derived table:** _Items_</span></span>
    - <span data-ttu-id="b7c98-192">**Väli:** _Kaubakood_</span><span class="sxs-lookup"><span data-stu-id="b7c98-192">**Field:** _Item number_</span></span>
    - <span data-ttu-id="b7c98-193">**Kriteeriumid:** _A0001_</span><span class="sxs-lookup"><span data-stu-id="b7c98-193">**Criteria:** _A0001_</span></span>

1. <span data-ttu-id="b7c98-194">Oma päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-194">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="b7c98-195">Valige ruudustiku **Täiendamismalli üksikasjad** kohalt **Täiendatavate tsoonide valimine**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-195">Select **Select zones to replenish** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="b7c98-196">Valige dialoogiboksi **Tsooni päring** vahekaart **Vahemik**, et lisada rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="b7c98-196">In the **Zone query** dialog box, on the **Range** tab, add a row to the grid.</span></span>
1. <span data-ttu-id="b7c98-197">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b7c98-197">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b7c98-198">**Tabel:** _Lao tsoon_</span><span class="sxs-lookup"><span data-stu-id="b7c98-198">**Table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="b7c98-199">**Tuletatud tabel:** _Lao tsoon_</span><span class="sxs-lookup"><span data-stu-id="b7c98-199">**Derived table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="b7c98-200">**Väli:** _Tsooni ID_</span><span class="sxs-lookup"><span data-stu-id="b7c98-200">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="b7c98-201">**Kriteerium:** _FLOOR_</span><span class="sxs-lookup"><span data-stu-id="b7c98-201">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="b7c98-202">Oma päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-202">Select **OK** to save your query and close the dialog box.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="b7c98-203">Asukohakorralduste häälestamine</span><span class="sxs-lookup"><span data-stu-id="b7c98-203">Set up location directives</span></span>

<span data-ttu-id="b7c98-204">Erinevalt asukohapõhisest min/maks. täiendamisest, nõuab tsoonipõhine min/max täiendamine, et seadistaksite nii komplekteerimise asukoha korralduse kui ka ladustamise korralduse, kuna süsteem hindab komplekteerimise asukoha asemel kogu tsooni väljamineva töö jaoks.</span><span class="sxs-lookup"><span data-stu-id="b7c98-204">Unlike location-based min/max replenishment, zone-based min/max replenishment requires that you set up both pick location directives and put location directives, because the system evaluates the whole zone instead of just the pick location for outbound work.</span></span>

#### <a name="view-and-edit-location-directives"></a><span data-ttu-id="b7c98-205">Asukohakorralduste kuvamine ja redigeerimine</span><span class="sxs-lookup"><span data-stu-id="b7c98-205">View and edit location directives</span></span>

<span data-ttu-id="b7c98-206">Oma asukohakorralduste kuvamiseks või redigeerimiseks avage jaotis **Laohaldus \> Häälestus \> Asukohakorraldus**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-206">To view or edit your location directives, go to **Warehouse management \> Setup \> Location directives**.</span></span>

<span data-ttu-id="b7c98-207">Vaadake järgmises jaotises olevaid näiteid, kuidas kasutada sätteid nõutava komplekteerimise asukohadirektiivi ja komplekteerimise asukohadirektiivi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="b7c98-207">For examples that show how to use the settings to create the required pick location directives and put location directives, see the next section.</span></span>

#### <a name="prepare-demo-data-location-directives"></a><span data-ttu-id="b7c98-208">Demoandmete asukohakorralduste ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="b7c98-208">Prepare demo data location directives</span></span>

<span data-ttu-id="b7c98-209">Demoandmete ettevalmistamiseks, et neid saaks kasutada selle teema lõpus kirjeldatud stsenaariumis, peate looma kaks asukohakorraldust: üks komplekteerimiseks ja teine ladustamiseks.</span><span class="sxs-lookup"><span data-stu-id="b7c98-209">To prepare demo data so that it can be used in the scenario at the end of this topic, you must create two location directives: one for pick and one for put.</span></span>

##### <a name="create-a-replenishment-pick-directive"></a><span data-ttu-id="b7c98-210">Täiendamise komplekteerimise korralduse loomine</span><span class="sxs-lookup"><span data-stu-id="b7c98-210">Create a replenishment pick directive</span></span>

1. <span data-ttu-id="b7c98-211">Valige juriidiline isik **USMF** demoandmetega töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="b7c98-211">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="b7c98-212">Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-212">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b7c98-213">Määrake vasakpoolse paani välja **Töökäsu tüüp** suvandiks _Täiendamine_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-213">In the left pane, set the **Work order type** field to _Replenishment_.</span></span>
1. <span data-ttu-id="b7c98-214">Uue korralduse loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-214">On the Action Pane, select **New** to create a new directive.</span></span>
1. <span data-ttu-id="b7c98-215">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b7c98-215">Set the following values:</span></span>

    - <span data-ttu-id="b7c98-216">**Järjekorranumber:** nõustuge vaikeväärtusega.</span><span class="sxs-lookup"><span data-stu-id="b7c98-216">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="b7c98-217">**Nimi:** sisestage _Tsooni komplekteerimine_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-217">**Name:** Enter _Zone pick_.</span></span>
    - <span data-ttu-id="b7c98-218">**Töö tüüp:** Valige _Komplekteerimine_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-218">**Work type:** Select _Pick_.</span></span>
    - <span data-ttu-id="b7c98-219">**Tegevuskoht:** valige _6_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-219">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="b7c98-220">**Ladu:** valige _61_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-220">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="b7c98-221">**Korralduse kood:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="b7c98-221">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="b7c98-222">**Mitmik-SKU:** määrake selle suvandi väärtuseks _Ei_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-222">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="b7c98-223">Valige **Salvesta**, et luua korraldus, millel on teie siiani konfigureeritud sätted.</span><span class="sxs-lookup"><span data-stu-id="b7c98-223">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="b7c98-224">Valige kiirkaardil **Read** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="b7c98-224">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b7c98-225">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b7c98-225">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b7c98-226">**Järjekorranumber:** sisestage _1_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-226">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b7c98-227">**Alates kogusest:** sisestage _0_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-227">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="b7c98-228">**Kuni koguseni:** sisestage _10000000_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-228">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="b7c98-229">**Ühik:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="b7c98-229">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="b7c98-230">**Koguse asukoha leidmine:** valige _Puudub_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-230">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="b7c98-231">**Piira ühiku alusel:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="b7c98-231">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="b7c98-232">**Ümardage ühikuni:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="b7c98-232">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="b7c98-233">**Pakendi koguse asukoha leidmine:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="b7c98-233">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="b7c98-234">**Luba tükeldamine:** märkige see ruut.</span><span class="sxs-lookup"><span data-stu-id="b7c98-234">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="b7c98-235">Uue rea salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-235">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="b7c98-236">Kui teie uus rida on valitud ruudustikul **Read**, valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="b7c98-236">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="b7c98-237">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b7c98-237">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b7c98-238">**Järjekorranumber:** sisestage _1_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-238">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b7c98-239">**Nimi:** sisestage _Hulgikomplekteerimine_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-239">**Name:** Enter _Pick from bulk_.</span></span>
    - <span data-ttu-id="b7c98-240">**Fikseeritud asukoha kasutus:** valige _Fikseeritud ja mittefikseeritud asukohad_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-240">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="b7c98-241">**Luba negatiivne laovaru:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="b7c98-241">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="b7c98-242">**Partii lubatud:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="b7c98-242">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="b7c98-243">**Strateegia:** valige _Puudub_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-243">**Strategy:** Select _None_.</span></span>

1. <span data-ttu-id="b7c98-244">Uue tegevuse salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-244">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="b7c98-245">Kui uus tegevus on valitud, valige ruudustiku **Asukohakorralduse tegevused** kohalt suvand **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-245">While your new action still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="b7c98-246">Kuvatakse päringu dialoogiboks, kust saate valida asukohad, millest täiendada.</span><span class="sxs-lookup"><span data-stu-id="b7c98-246">A query dialog box appears, where you can select the locations to replenish from.</span></span> <span data-ttu-id="b7c98-247">Vahekaardil **Vahemik** valige käsk **Lisa**, et lisada uus rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="b7c98-247">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="b7c98-248">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b7c98-248">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b7c98-249">**Tabel:** _Asukohad_</span><span class="sxs-lookup"><span data-stu-id="b7c98-249">**Table:** _Locations_</span></span>
    - <span data-ttu-id="b7c98-250">**Tuletatud tabel:** _Asukohad_</span><span class="sxs-lookup"><span data-stu-id="b7c98-250">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="b7c98-251">**Väli:** _Tsooni ID_</span><span class="sxs-lookup"><span data-stu-id="b7c98-251">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="b7c98-252">**Kriteeriumid:** _BULK_</span><span class="sxs-lookup"><span data-stu-id="b7c98-252">**Criteria:** _BULK_</span></span>

1. <span data-ttu-id="b7c98-253">Oma päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-253">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="b7c98-254">Oma asukohakorralduse salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-254">Select **Save** to save your location directive.</span></span>

##### <a name="create-a-replenishment-put-directive"></a><span data-ttu-id="b7c98-255">Täiendamise ladustamise korralduse loomine</span><span class="sxs-lookup"><span data-stu-id="b7c98-255">Create a replenishment put directive</span></span>

1. <span data-ttu-id="b7c98-256">Veenduge, et vasakpoolse paani lehel **Asukohakorraldused** oleks välja **Töökäsu tüüp** väärtuseks _Täiendamine_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-256">On the **Location directives** page, in the left pane, make sure that the **Work order type** field is still set to _Replenishment_.</span></span>
1. <span data-ttu-id="b7c98-257">Muu korralduse loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-257">On the Action Pane, select **New** to create another new directive.</span></span>
1. <span data-ttu-id="b7c98-258">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b7c98-258">Set the following values:</span></span>

    - <span data-ttu-id="b7c98-259">**Järjekorranumber:** nõustuge vaikeväärtusega.</span><span class="sxs-lookup"><span data-stu-id="b7c98-259">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="b7c98-260">**Nimi:** sisestage _Tsooni ladustamine_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-260">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="b7c98-261">**Töötellimuse tüüp:** valige _Ladustamine_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-261">**Work order type:** Select _Put_.</span></span>
    - <span data-ttu-id="b7c98-262">**Tegevuskoht:** valige _6_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-262">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="b7c98-263">**Ladu:** valige _61_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-263">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="b7c98-264">**Korralduskood:** valige _Tsooni täiend_, et linkida see asukohakorraldus eelnevalt loodud täiendamismalliga, kasutades eelnevalt loodud koodi.</span><span class="sxs-lookup"><span data-stu-id="b7c98-264">**Directive code:** Select _Zone replen_ to link this location directive with the replenishment template that you created earlier by using the code that you created earlier.</span></span>
    - <span data-ttu-id="b7c98-265">**Mitmik-SKU:** määrake selle suvandi väärtuseks _Ei_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-265">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="b7c98-266">Valige **Salvesta**, et luua korraldus, millel on teie siiani konfigureeritud sätted.</span><span class="sxs-lookup"><span data-stu-id="b7c98-266">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="b7c98-267">Valige kiirkaardil **Read** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="b7c98-267">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b7c98-268">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b7c98-268">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b7c98-269">**Järjekorranumber:** sisestage _1_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-269">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b7c98-270">**Alates kogusest:** sisestage _0_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-270">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="b7c98-271">**Kuni koguseni:** sisestage _10000000_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-271">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="b7c98-272">**Ühik:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="b7c98-272">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="b7c98-273">**Koguse asukoha leidmine:** valige _Puudub_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-273">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="b7c98-274">**Piira ühiku alusel:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="b7c98-274">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="b7c98-275">**Ümardage ühikuni:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="b7c98-275">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="b7c98-276">**Pakendi koguse asukoha leidmine:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="b7c98-276">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="b7c98-277">**Luba tükeldamine:** märkige see ruut.</span><span class="sxs-lookup"><span data-stu-id="b7c98-277">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="b7c98-278">Uue rea salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-278">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="b7c98-279">Kui teie uus rida on valitud ruudustikul **Read**, valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="b7c98-279">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="b7c98-280">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b7c98-280">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b7c98-281">**Järjekorranumber:** sisestage _1_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-281">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="b7c98-282">**Nimi:** sisestage _Tsooni ladustamine_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-282">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="b7c98-283">**Fikseeritud asukoha kasutus:** valige _Fikseeritud ja mittefikseeritud asukohad_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-283">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="b7c98-284">**Luba negatiivne laovaru:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="b7c98-284">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="b7c98-285">**Partii lubatud:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="b7c98-285">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="b7c98-286">**Strateegia:** valige _Konsolideeri_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-286">**Strategy:** Select _Consolidate_.</span></span>

1. <span data-ttu-id="b7c98-287">Uue tegevuse salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-287">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="b7c98-288">Kui uus tegevus on endiselt valitud, valige ruudustiku **Asukohakorralduse tegevused** kohalt suvand **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-288">While your new action is still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="b7c98-289">Kuvatakse päringu dialoogiboks, kust saate valida tsooni, kuhu täiendada.</span><span class="sxs-lookup"><span data-stu-id="b7c98-289">A query dialog box appears, where you can select the zone to replenish to.</span></span> <span data-ttu-id="b7c98-290">See tsoon peaks vastama täiendamismallis määratud tsoonile.</span><span class="sxs-lookup"><span data-stu-id="b7c98-290">This zone should be the same zone that is specified in the replenishment template.</span></span> <span data-ttu-id="b7c98-291">Vahekaardil **Vahemik** valige käsk **Lisa**, et lisada uus rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="b7c98-291">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="b7c98-292">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b7c98-292">In the new row, set the following values:</span></span>

    - <span data-ttu-id="b7c98-293">**Tabel:** _Asukohad_</span><span class="sxs-lookup"><span data-stu-id="b7c98-293">**Table:** _Locations_</span></span>
    - <span data-ttu-id="b7c98-294">**Tuletatud tabel:** _Asukohad_</span><span class="sxs-lookup"><span data-stu-id="b7c98-294">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="b7c98-295">**Väli:** _Tsooni ID_</span><span class="sxs-lookup"><span data-stu-id="b7c98-295">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="b7c98-296">**Kriteerium:** _FLOOR_</span><span class="sxs-lookup"><span data-stu-id="b7c98-296">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="b7c98-297">Oma päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-297">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="b7c98-298">Oma asukohakorralduse salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-298">Select **Save** to save your location directive.</span></span>

## <a name="scenario"></a><span data-ttu-id="b7c98-299">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="b7c98-299">Scenario</span></span>

<span data-ttu-id="b7c98-300">Selles jaotises esitatakse näidisstsenaarium, mis näitab, kuidas selle funktsiooniga töötada.</span><span class="sxs-lookup"><span data-stu-id="b7c98-300">This section provides a sample scenario that shows how to work with the feature.</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a><span data-ttu-id="b7c98-301">Valmistage ette näidisstsenaariumi jaoks nõutavad näidisandmed</span><span class="sxs-lookup"><span data-stu-id="b7c98-301">Prepare the sample data that is required for the sample scenario</span></span>

<span data-ttu-id="b7c98-302">Enne kui alustate stsenaariumi kasutamist, peate aktiveerima näidisandmed ja seadistama selle funktsiooni selle teema käesolevas ja eelnevates jaotistes kirjeldatu järgi.</span><span class="sxs-lookup"><span data-stu-id="b7c98-302">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section and in the previous sections of this topic.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="b7c98-303">Juriidilise isiku USMF kasutamine</span><span class="sxs-lookup"><span data-stu-id="b7c98-303">Use the USMF legal entity</span></span>

<span data-ttu-id="b7c98-304">Selle stsenaariumi kasutamiseks siin määratud näidiskirjete ja -väärtuste abil peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="b7c98-304">To work through the scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="b7c98-305">Enne alustamist peate valima ka juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-305">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="prepare-additional-sample-data"></a><span data-ttu-id="b7c98-306">Täiendavate näidisandmete ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="b7c98-306">Prepare additional sample data</span></span>

<span data-ttu-id="b7c98-307">Pärast juriidilise isiku **USMF** valimist, lisage nõutavad täiendavad näidisandmed, nagu on kirjeldatud selle teema varasemas jaotises [Tsoonipõhise täiendamise häälestus](#setup).</span><span class="sxs-lookup"><span data-stu-id="b7c98-307">After you've selected the **USMF** legal entity, add the additional sample data that is required, as described in the [Set up zone-based replenishment](#setup) section earlier in this topic.</span></span>

#### <a name="check-your-on-hand-inventory"></a><span data-ttu-id="b7c98-308">Vaba kaubavaru kontrollimine</span><span class="sxs-lookup"><span data-stu-id="b7c98-308">Check your on-hand inventory</span></span>

<span data-ttu-id="b7c98-309">Järgige neid etappe, et veenduda, kas teie süsteem sisaldab näidisstsenaariumi toetamiseks piisavalt varusid.</span><span class="sxs-lookup"><span data-stu-id="b7c98-309">Follow these steps to make sure that your system includes enough inventory to support the sample scenario.</span></span>

1. <span data-ttu-id="b7c98-310">Veenduge, et kauba *A0001* jaoks oleks vaba kaubavaru komplekteerimistsooni kahes eri asukohas (*FLOOR*), mis on määratud täiendamismallis.</span><span class="sxs-lookup"><span data-stu-id="b7c98-310">Make sure that there is on-hand inventory for item *A0001* at two different locations in the pick zone (*FLOOR*) that is specified in the replenishment template.</span></span> <span data-ttu-id="b7c98-311">Kuid kogu varu peaks olema väiksem kui nõutav minimaalne kogus (*50*), mis on määratletud täiendamismallis.</span><span class="sxs-lookup"><span data-stu-id="b7c98-311">However, the total inventory should be less than the required minimum quantity (*50*) that is specified on the replenishment template.</span></span> <span data-ttu-id="b7c98-312">Sel viisil saate simuleerida, kuidas toimub arvutamine üksiku asukoha asemel terve tsooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="b7c98-312">In this way, you can simulate how the calculation occurs for the whole zone instead of just for a single location.</span></span> <span data-ttu-id="b7c98-313">**Kasutage varude korrigeerimiseks mis tahes laoprotsessi.**</span><span class="sxs-lookup"><span data-stu-id="b7c98-313">**Use any of the warehouse processes to adjust inventory as required.**</span></span>
1. <span data-ttu-id="b7c98-314">Veenduge, et kauba *A0001* jaoks oleks piisavalt varusid hulgiasukohas, mis on määratud tsooni komplekteerimise asukohakorralduses, kus täiendamistöö peaks komplekteerima kaubad tsooni ID-st *BULK*.</span><span class="sxs-lookup"><span data-stu-id="b7c98-314">Make sure that there is enough inventory for item *A0001* at a bulk location that is specified in the zone pick location directive where the replenishment work should pick the items from zone ID *BULK*.</span></span> <span data-ttu-id="b7c98-315">Kogu varu peaks olema rohkem kui nõutav maksimaalne kogus (*150*), mis on määratletud täiendamismallis.</span><span class="sxs-lookup"><span data-stu-id="b7c98-315">The total inventory must be more than the required maximum quantity (*150*) that is specified in the replenishment template.</span></span>
1. <span data-ttu-id="b7c98-316">Valikuline, kuid soovitatav: tehke lao korrigeerimise töölehe loomiseks järgmist.</span><span class="sxs-lookup"><span data-stu-id="b7c98-316">Optional but recommended: Follow these steps to create an inventory adjustment journal:</span></span>

    1. <span data-ttu-id="b7c98-317">Avage jaotis **Varude haldus \> Töölehe sisestused \> Kaubad \> Varude korrigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-317">Go to **Inventory management \> Journal entries \> Items \> Inventory adjustment**.</span></span>
    1. <span data-ttu-id="b7c98-318">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-318">Select **New**.</span></span>
    1. <span data-ttu-id="b7c98-319">Valige dialoogiboksi **Varude töölehe loomine** väljal **Ladu** väärtus *61*.</span><span class="sxs-lookup"><span data-stu-id="b7c98-319">In the **Create inventory journal** dialog box, in the **Warehouse** field, select *61*.</span></span>
    1. <span data-ttu-id="b7c98-320">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-320">Select **OK**.</span></span>
    1. <span data-ttu-id="b7c98-321">Kasutage kiirkaardil **Töölehe read** nuppu **Uus**, et lisada ruudustikku kolm rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b7c98-321">On the **Journal lines** FastTab, use the **New** button to add three lines to the grid, and set the following values.</span></span> <span data-ttu-id="b7c98-322">Pärast kõigi ridade seadistamise lõpule viimist valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-322">After you've finished setting up each line, select **Save**.</span></span>

        - <span data-ttu-id="b7c98-323">**Rida 1:**</span><span class="sxs-lookup"><span data-stu-id="b7c98-323">**Line 1:**</span></span>

            - <span data-ttu-id="b7c98-324">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b7c98-324">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="b7c98-325">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="b7c98-325">**Site:** *6*</span></span>
            - <span data-ttu-id="b7c98-326">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="b7c98-326">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="b7c98-327">**Asukoht:** *02A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="b7c98-327">**Location:** *02A01R1S1B*</span></span>
            - <span data-ttu-id="b7c98-328">**Identifitseerimisnumber:** valige loendist olemasolev identifitseerimisnumber või looge uus.</span><span class="sxs-lookup"><span data-stu-id="b7c98-328">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="b7c98-329">**Kogus:** *1000*</span><span class="sxs-lookup"><span data-stu-id="b7c98-329">**Quantity:** *1000*</span></span>

        - <span data-ttu-id="b7c98-330">**Rida 2:**</span><span class="sxs-lookup"><span data-stu-id="b7c98-330">**Line 2:**</span></span>

            - <span data-ttu-id="b7c98-331">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b7c98-331">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="b7c98-332">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="b7c98-332">**Site:** *6*</span></span>
            - <span data-ttu-id="b7c98-333">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="b7c98-333">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="b7c98-334">**Asukoht:** *07A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="b7c98-334">**Location:** *07A01R2S1B*</span></span>
            - <span data-ttu-id="b7c98-335">**Identifitseerimisnumber:** valige loendist olemasolev identifitseerimisnumber või looge uus.</span><span class="sxs-lookup"><span data-stu-id="b7c98-335">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="b7c98-336">**Kogus:** *15*</span><span class="sxs-lookup"><span data-stu-id="b7c98-336">**Quantity:** *15*</span></span>

        - <span data-ttu-id="b7c98-337">**Rida 3:**</span><span class="sxs-lookup"><span data-stu-id="b7c98-337">**Line 3:**</span></span>

            - <span data-ttu-id="b7c98-338">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="b7c98-338">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="b7c98-339">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="b7c98-339">**Site:** *6*</span></span>
            - <span data-ttu-id="b7c98-340">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="b7c98-340">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="b7c98-341">**Asukoht:** *07A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="b7c98-341">**Location:** *07A01R1S1B*</span></span>
            - <span data-ttu-id="b7c98-342">**Identifitseerimisnumber:** valige loendist olemasolev identifitseerimisnumber või looge uus.</span><span class="sxs-lookup"><span data-stu-id="b7c98-342">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="b7c98-343">**Kogus:** *10*</span><span class="sxs-lookup"><span data-stu-id="b7c98-343">**Quantity:** *10*</span></span>

    1. <span data-ttu-id="b7c98-344">Valige toimingupaanil **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-344">On the Action Pane, select **Validate**.</span></span> <span data-ttu-id="b7c98-345">Lahendage kõik leitud tõrked enne järgmisse etappi liikumist.</span><span class="sxs-lookup"><span data-stu-id="b7c98-345">Address any errors that are found before you move on to the next step.</span></span>
    1. <span data-ttu-id="b7c98-346">Varude lattu sisestamiseks valige toimingupaanil **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-346">On the Action Pane, select **Post** to post the inventory to the warehouse.</span></span>

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a><span data-ttu-id="b7c98-347">Näidisstsenaarium: käivitage tsoonipõhine min/max täiendamine</span><span class="sxs-lookup"><span data-stu-id="b7c98-347">Sample scenario: Run zone-based min/max replenishment</span></span>

<span data-ttu-id="b7c98-348">Kui kõik eeltingimuseks olevad näidisandmed on olemas, saate käivitada täiendamise, järgides neid etappe.</span><span class="sxs-lookup"><span data-stu-id="b7c98-348">After all the prerequisite sample data is in place, you can trigger replenishment by following these steps.</span></span>

1. <span data-ttu-id="b7c98-349">Avage jaotis **Laohaldus \> Täiendamine \> Täiendamine**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-349">Go to **Warehouse management \> Replenishment \> Replenishments**.</span></span>
1. <span data-ttu-id="b7c98-350">Valige dialoogiboksi **Täiendamine** kiirkaardil **Kaasatavad kirjed** suvand **Filter**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-350">In the **Replenishment** dialog box, on the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="b7c98-351">Redigeerige dialoogiboksi **Päring** vahekaardil **Vahemik** tabeli vaikerida järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="b7c98-351">In the **Inquiry** dialog box, on the **Range** tab, edit the default table row in the following way:</span></span>

    - <span data-ttu-id="b7c98-352">**Tabel:** valige _Täiendamismallid_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-352">**Table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="b7c98-353">**Tuletatud tabel:** valige _Täiendamismallid_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-353">**Derived table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="b7c98-354">**Väli:** valige _Täiendamismall_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-354">**Field:** Select _Replenishment template_.</span></span>
    - <span data-ttu-id="b7c98-355">**Kriteeriumid:** valige _Tsoon min/max täiend_.</span><span class="sxs-lookup"><span data-stu-id="b7c98-355">**Criteria:** Select _Zone min/max replen_.</span></span> <span data-ttu-id="b7c98-356">Selle sama täiendamismalli lõite selle stsenaariumi jaoks demoandmete ettevalmistamise ajal.</span><span class="sxs-lookup"><span data-stu-id="b7c98-356">This replenishment template is the replenishment template that you created while you were preparing the demo data for this scenario.</span></span>

1. <span data-ttu-id="b7c98-357">Päringu salvestamiseks sulgemiseks valige **OK** ja minge tagasi dialoogiboksi **Täiendamine**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-357">Select **OK** to save the query and go back to the **Replenishment** dialog box.</span></span>
1. <span data-ttu-id="b7c98-358">Täiendamismalli käitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-358">Select **OK** to run the replenishment template.</span></span>

<span data-ttu-id="b7c98-359">Täiendamistöö on nüüd loodud, et komplekteerida varusid tsoonist *BULK* ja täiendada tsooni *FLOOR*.</span><span class="sxs-lookup"><span data-stu-id="b7c98-359">Replenishment work is now created to pick inventory from the *BULK* zone and replenish it to the *FLOOR* zone.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="b7c98-360">Märkmed ja näpunäited</span><span class="sxs-lookup"><span data-stu-id="b7c98-360">Notes and tips</span></span>

<span data-ttu-id="b7c98-361">Siin on mõningaid märkuseid ja näpunäited funktsiooniga töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="b7c98-361">Here are a few notes and tips for working with the feature:</span></span>

- <span data-ttu-id="b7c98-362">Täiendamistöö seadistamiseks, mis läheks soovitud tsooni, saate linkida täiendamismalli read ja asukohkorraldused ühel järgmistest viisidest.</span><span class="sxs-lookup"><span data-stu-id="b7c98-362">To set up replenishment work that goes to the desired zone, you can link the replenishment template lines and location directives in either of the following ways:</span></span>

    - <span data-ttu-id="b7c98-363">Redigeerige asukohakorralduse päise päringut ja filtreerige valitud täiendamismalli read.</span><span class="sxs-lookup"><span data-stu-id="b7c98-363">Edit the location directive header query, and filter the selected replenishment template lines.</span></span>
    - <span data-ttu-id="b7c98-364">Kasutage korralduskoodi täiendamismalli real ja muutke see ladustamise asukohakorraldusele vastavaks.</span><span class="sxs-lookup"><span data-stu-id="b7c98-364">Use a directive code on the replenishment template line, and match it to the put location directive.</span></span>

- <span data-ttu-id="b7c98-365">Kui kasutate dünaamilisi asukohti, luuakse täiendamistöö kas esimese saadaoleva asukoha või juba varusid sisaldava asukoha jaoks, kui asukohakorralduse tegevus on seadistatud kasutama strateegiat **Konsolideerimine**.</span><span class="sxs-lookup"><span data-stu-id="b7c98-365">If you're using dynamic locations, replenishment work will be created either for the first available location or for a location that already contains inventory, if the location directive action is set up to use the **Consolidate** strategy.</span></span>
- <span data-ttu-id="b7c98-366">Kui kasutate tsoonide asemel fikseeritud asukohti, peaksite kasutama [standardset min/max täiendamist](tasks/set-up-min-max-replenishment-process.md).</span><span class="sxs-lookup"><span data-stu-id="b7c98-366">If you're using fixed locations instead of zones, you should use [standard min/max replenishment](tasks/set-up-min-max-replenishment-process.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]