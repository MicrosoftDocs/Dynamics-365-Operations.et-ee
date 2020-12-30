---
title: Tsooniläve täiendamine
description: Tsoonipõhine täiendamine kasutab minimaalse/maksimaakse (min/max) täiendamise strateegiat, kuid see hindab üksikute asukohtade asemel ainult terveid laotsoone. Tänu sellele saavad laohaldurid kiiremini teada, kui komplekteerimistsoonis on vaja täiendavat varu.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6f4ddd03ec16ac43b007b904eb688563735e0941
ms.sourcegitcommit: d9bffbeae2ba14f06294dd275383077d4d65c4fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/01/2020
ms.locfileid: "4654168"
---
# <a name="zone-threshold-replenishment"></a><span data-ttu-id="ee6f5-104">Tsooniläve täiendamine</span><span class="sxs-lookup"><span data-stu-id="ee6f5-104">Zone threshold replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee6f5-105">Tsoonipõhine täiendamine kasutab minimaalse/maksimaakse (min/max) [täiendamise](replenishment.md) strateegiat, kuid see hindab üksikute asukohtade asemel ainult terveid laotsoone.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-105">Zone-based replenishment uses a minimum/maximum (min/max) [replenishment](replenishment.md) strategy, but it evaluates whole warehouse zones instead of just individual locations.</span></span> <span data-ttu-id="ee6f5-106">Tänu sellele saavad laohaldurid kiiremini teada, kui komplekteerimistsoonis on vaja täiendavat varu.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-106">Therefore, warehouse managers can more quickly learn when additional inventory is required in a picking zone.</span></span>

<span data-ttu-id="ee6f5-107">Selle funktsiooni seadistus sarnaneb asukohapõhise täiendamise seadistusele.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-107">The setup for this feature resembles the setup for location-based replenishment.</span></span> <span data-ttu-id="ee6f5-108">Kuid min/max täiendamise malli seadistamise ajal saate ka määrata, kas läve tuleks hinnata asukoha või tsooni põhjal.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-108">However, when you set up a template for min/max replenishment, you can also specify whether the threshold should be evaluated per location or per zone.</span></span> <span data-ttu-id="ee6f5-109">Kui seadistate tsoonidel põhineva hindamise, peate tsooni valiku päringule lisama kindlad tsoonid.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-109">If you set up evaluation that is based on zones, you must add specific zones to the zone selection query.</span></span>

<span data-ttu-id="ee6f5-110">Sarnaselt asukohapõhisele min/max täiendamisele, põhineb tsoonipõhine min/max täiendamine minimaalse varu läve häälestusel, mis käivitab valitud kaupade täiendamise töö loomise.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-110">Like location-based min/max replenishment, zone-based min/max replenishment is based the setup of a minimum inventory threshold that triggers the creation of replenishment work for selected items.</span></span> <span data-ttu-id="ee6f5-111">See täiendamise töö suurendab varusid selle tsooni jaoks määratud maksimaalse läveni.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-111">This replenishment work will increase inventory up to the specified maximum threshold for the zone.</span></span>

> [!NOTE]
> <span data-ttu-id="ee6f5-112">Praeguses väljalaskes ei toetata tootevariantide tsooni täiendamise protsesse.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-112">Zone replenishment processes for product variants aren't supported in the current release.</span></span>


<span data-ttu-id="ee6f5-113">Erinevalt asukohapõhisest min/max täiendamisest, ei nõua tsoonipõhine min/max täiendamine fikseeritud asukohti selle hindamiseks, kas asukohad peaksid ladustama kindlat kaupa.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-113">Unlike location-based min/max replenishment, zone-based min/max replenishment doesn't require fixed locations to evaluate whether locations should store a specific item.</span></span> <span data-ttu-id="ee6f5-114">Tänu sellele võimaldab tsoonipõhine täiendamine kasutada min/max täiendamist ka siis, kui teil pole laos iga kauba või kaubavariandi jaoks fikseeritud asukohti.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-114">Therefore, zone-based replenishment lets you use min/max replenishment even if you don't have fixed locations for each item or item variant in the warehouse.</span></span> <span data-ttu-id="ee6f5-115">Kui tsoonis langeb kogus määratud lävest allapoole, luuakse täiendamise töö.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-115">When a quantity in the zone falls below the specified minimum threshold, replenishment work is created.</span></span> <span data-ttu-id="ee6f5-116">Asukohakorraldused määravad, millisesse kindlasse asukohta varud tuleks panna.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-116">Location directives will determine which specific location the inventory should be put into.</span></span>

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a><span data-ttu-id="ee6f5-117">Funktsiooni Tsooniläve täiendamine sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="ee6f5-117">Turn on the Zone threshold replenishment feature</span></span>

<span data-ttu-id="ee6f5-118">Enne funktsiooni *Tsooniläve täiendamine* kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-118">Before you can use the *Zone threshold replenishment* feature, it must be turned on in your system.</span></span> <span data-ttu-id="ee6f5-119">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-119">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="ee6f5-120">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-120">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ee6f5-121">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="ee6f5-121">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ee6f5-122">**Funktsiooni nimi:** *Tsooniläve täiendamine*</span><span class="sxs-lookup"><span data-stu-id="ee6f5-122">**Feature name:** *Zone threshold replenishment*</span></span>

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a><span data-ttu-id="ee6f5-123">Tsoonipõhise täiendamise häälestus</span><span class="sxs-lookup"><span data-stu-id="ee6f5-123">Set up zone-based replenishment</span></span>

<span data-ttu-id="ee6f5-124">Tsoonipõhise täiendamise seadistamiseks peate konfigureerima süsteemi mitu osa.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-124">To set up zone-based replenishment, you must configure several parts of the system.</span></span> <span data-ttu-id="ee6f5-125">Selles jaotises tutvustatakse erinevaid sätteid ja esitatakse demoandmete väärtuseid, mida saate sisestada, kui soovite kasutada selle teema lõpus olevat stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-125">This section introduces the various settings and provides demo data values that you can enter if you want to work through the scenario at the end of this topic.</span></span>

### <a name="set-up-directive-codes"></a><span data-ttu-id="ee6f5-126">Korralduskoodide häälestus</span><span class="sxs-lookup"><span data-stu-id="ee6f5-126">Set up directive codes</span></span>

<span data-ttu-id="ee6f5-127">[Korralduskoodid](control-warehouse-location-directives.md) võimaldavad teil täpsemalt määratleda asukohamalli, mida kasutatakse töömallis.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-127">[Directive codes](control-warehouse-location-directives.md) let you be more specific when you define the location template that is used in a work template.</span></span> <span data-ttu-id="ee6f5-128">Iga koodiga luuakse ühine väärtus, millele saate viidata iga mallitüübi konfigureerimisel.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-128">Each code establishes a common value that you can refer to when you configure each type of template.</span></span>

#### <a name="view-and-edit-directive-codes"></a><span data-ttu-id="ee6f5-129">Korralduskoodide kuvamine ja redigeerimine</span><span class="sxs-lookup"><span data-stu-id="ee6f5-129">View and edit directive codes</span></span>

<span data-ttu-id="ee6f5-130">Oma korralduskoodide kuvamiseks või redigeerimiseks avage jaotis **Laohaldus \> Häälestus \> Korralduskoodid**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-130">To view or edit your directive codes, go to **Warehouse management \> Setup \> Directive codes**.</span></span>

#### <a name="prepare-demo-data-directive-codes"></a><span data-ttu-id="ee6f5-131">Demoandmete korralduskoodide ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="ee6f5-131">Prepare demo data directive codes</span></span>

<span data-ttu-id="ee6f5-132">Selles näites kirjeldatakse, kuidas valmistada ette korralduskoodi.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-132">This example shows how to prepare a directive code.</span></span> <span data-ttu-id="ee6f5-133">Kui kavatsete kasutada selle teema lõpus olevat stsenaariumi, kasutage siin esitatud demoandmete väärtusi.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-133">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="ee6f5-134">Muul juhul saate kasutada oma väärtusi.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-134">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="ee6f5-135">Valige juriidiline isik **USMF** demoandmetega töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-135">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="ee6f5-136">Avage jaotis **Laohaldus \> Seadistus \> Korralduskoodid**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-136">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="ee6f5-137">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="ee6f5-138">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-138">In the new row, set the following values:</span></span>

    - <span data-ttu-id="ee6f5-139">**Korralduskood:** _Tsooni täiend_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-139">**Directive code:** _Zone replen_</span></span>
    - <span data-ttu-id="ee6f5-140">**Korralduse kirjeldus:** _Tsooni täiendamine_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-140">**Directive description:** _Zone replenishment_</span></span>

1. <span data-ttu-id="ee6f5-141">Uue koodi salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-141">Select **Save** to save the new code.</span></span>

### <a name="set-up-replenishment-templates"></a><span data-ttu-id="ee6f5-142">Täiendamismallide häälestamine</span><span class="sxs-lookup"><span data-stu-id="ee6f5-142">Set up replenishment templates</span></span>

<span data-ttu-id="ee6f5-143">[Min/max täiendamismallid](tasks/set-up-min-max-replenishment-process.md) on põhimehhanism komplekteerimiskohtades optimaalsete tasemete säilitamiseks.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-143">[Min/max replenishment templates](tasks/set-up-min-max-replenishment-process.md) are the primary mechanism for maintaining optimal levels in picking locations.</span></span> <span data-ttu-id="ee6f5-144">Nendes mallides peate seadistama reeglid, mida kasutatakse laovarude täiendamiseks.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-144">In these templates, you must set up the rules that will be used to replenish inventory in the warehouse.</span></span> <span data-ttu-id="ee6f5-145">Täiendamise hulka, mille jaoks saab malle kasutada, kuulub ka tsoonipõhine täiendamine.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-145">The replenishment that the templates can be used for includes zone-based replenishment.</span></span>

#### <a name="view-and-edit-replenishment-templates"></a><span data-ttu-id="ee6f5-146">Täiendamismallide kuvamine ja redigeerimine</span><span class="sxs-lookup"><span data-stu-id="ee6f5-146">View and edit replenishment templates</span></span>

<span data-ttu-id="ee6f5-147">Täiendamismall on reeglistik, mis määrab asikoha täiendamise aja ja viisi.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-147">A replenishment template is a set of rules that control when and how a location is replenished.</span></span> <span data-ttu-id="ee6f5-148">Saate valida malli täiendamise tegemise aja ja viisi juhtimiseks.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-148">You select a template to control when and how replenishment is done.</span></span> <span data-ttu-id="ee6f5-149">Täiendamismallide kuvamiseks ja redigeerimiseks avage jaotis **Laohaldus \> Seadistus \> Täiendamine \> Täiendamismallid**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-149">To view or edit your replenishment templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>

#### <a name="prepare-a-demo-data-replenishment-template"></a><span data-ttu-id="ee6f5-150">Demoandmete täiendamismalli ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="ee6f5-150">Prepare a demo data replenishment template</span></span>

<span data-ttu-id="ee6f5-151">Selles näites kirjeldatakse, kuidas valmistada ette täiendamismalli.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-151">This example shows how to prepare a replenishment template.</span></span> <span data-ttu-id="ee6f5-152">Kui kavatsete kasutada selle teema lõpus olevat stsenaariumi, kasutage siin esitatud demoandmete väärtusi.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-152">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="ee6f5-153">Muul juhul saate kasutada oma väärtusi.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-153">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="ee6f5-154">Valige juriidiline isik **USMF** demoandmetega töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-154">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="ee6f5-155">Avage jaotis **Laohaldus \> Seadistus \> Täiendamine \> Täiendamismallid**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-155">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="ee6f5-156">Lehe redigeerimisrežiimi panemiseks valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-156">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="ee6f5-157">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida **Ülevaade**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-157">On the Action Pane, select **New** to add a row to the **Overview** grid.</span></span>
1. <span data-ttu-id="ee6f5-158">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-158">In the new row, set the following values.</span></span> <span data-ttu-id="ee6f5-159">Võtke vastu vaikeväärtused kõigil teistel väljadel.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-159">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="ee6f5-160">**Täiendamismall:** _Tsooni min/max täiend_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-160">**Replenish template:** _Zone min/max replen_</span></span>
    - <span data-ttu-id="ee6f5-161">**Kirjeldus:** _Tsooni min/max täiendamine_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-161">**Description:** _Zone min/max replenishment_</span></span>
    - <span data-ttu-id="ee6f5-162">**Täiendamise tüüp:** _Minimaalne või maksimaalne_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-162">**Replenishment type:** _Minimum or maximum_</span></span>

1. <span data-ttu-id="ee6f5-163">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-163">Select **Save**.</span></span>
1. <span data-ttu-id="ee6f5-164">Kui uus rida on valitud ruudustikus **Ülevaade**, valige ruudustiku **Täiendamismalli üksikasjad** kohalt suvand **Uus**, et lisada rida, mis on seostatud teie äsja loodud täiendamismalliga *Tsooni min/max. täiend*.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-164">While the new row is still selected in the **Overview** grid, select **New** above the **Replenishment Template Details** grid to add a row that is associated with the *Zone Min/Max replen* replenishment template that you just created.</span></span>
1. <span data-ttu-id="ee6f5-165">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-165">In the new row, set the following values:</span></span>

    - <span data-ttu-id="ee6f5-166">**Järjekorranumber:** sisestage _1_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-166">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="ee6f5-167">**Kirjeldus:** Sisestage _Komplekteerimistsooni täiendamine_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-167">**Description:** Enter _Pick zone replenishment_.</span></span>
    - <span data-ttu-id="ee6f5-168">**Täiendamise ühik:** valige _ea_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-168">**Replenishment unit:** Select _ea_.</span></span>
    - <span data-ttu-id="ee6f5-169">**Taotluse tüüp:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-169">**Request type:** Leave this field blank.</span></span>
    - <span data-ttu-id="ee6f5-170">**Korralduse kood:** see väli seob täiendamismalli asukohakorraldusega.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-170">**Directive code:** This field links the replenishment template with a location directive.</span></span> <span data-ttu-id="ee6f5-171">Valige eelnevalt loodud demoandmete korralduskood (_Tsooni täiend_).</span><span class="sxs-lookup"><span data-stu-id="ee6f5-171">Select the demo data directive code that you created earlier (_Zone replen_).</span></span>
    - <span data-ttu-id="ee6f5-172">**Töömall:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-172">**Work template:** Leave this field blank.</span></span>
    - <span data-ttu-id="ee6f5-173">**Minimaalne kogus:** see väli määrab koguse, mille puhul täiendamine käivitatakse.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-173">**Minimum quantity:** This field sets the quantity that replenishment will be triggered at.</span></span> <span data-ttu-id="ee6f5-174">Sisestage _50_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-174">Enter _50_.</span></span>
    - <span data-ttu-id="ee6f5-175">**Maksimaalne kogus:** see väli määrab kauba maksimaalse koguse, mis võib tsoonis olla.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-175">**Maximum quantity:** This field sets the maximum quantity of an item that can be present in a zone.</span></span> <span data-ttu-id="ee6f5-176">Loodud varude täiendamistöö suurendab varud sellele kogusele.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-176">Generated replenishment work will increase inventory to this quantity.</span></span> <span data-ttu-id="ee6f5-177">Sisestage _150_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-177">Enter _150_.</span></span>
    - <span data-ttu-id="ee6f5-178">**Ühik:** see väli määrab minimaalse ja maksimaalse väärtuse ühiku.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-178">**Unit:** This field sets the unit for the minimum and maximum values.</span></span> <span data-ttu-id="ee6f5-179">Valige _ea_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-179">Select _ea_.</span></span>
    - <span data-ttu-id="ee6f5-180">**Nõudluse juurdekasv:** valige _Ümardamine üles_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-180">**Demand increment:** Select _Round up_.</span></span>
    - <span data-ttu-id="ee6f5-181">**Tühjade fikseeritud asukohtade täiendamine:** valige see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-181">**Replenish empty fixed locations:** Select this check box.</span></span>
    - <span data-ttu-id="ee6f5-182">**Ainult fikseeritud asukohtade täiendamine:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-182">**Replenish only fixed locations:** Clear this check box.</span></span>
    - <span data-ttu-id="ee6f5-183">**Toote päringu režiim:** valige _Toote päring_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-183">**Product query mode:** Select _Product query_.</span></span>
    - <span data-ttu-id="ee6f5-184">**Täiendamise läve ulatus:** see väli määratleb, kas mall peaks hindama tsooni või kindla asukoha alusel.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-184">**Replenishment threshold scope:** This field defines whether the template should evaluate by zone or by specific location.</span></span> <span data-ttu-id="ee6f5-185">Valige _Tsoon_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-185">Select _Zone_.</span></span>
    - <span data-ttu-id="ee6f5-186">**Ladu:** valige _61_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-186">**Warehouse:** Select _61_.</span></span>

1. <span data-ttu-id="ee6f5-187">Valige ruudustiku **Täiendamismalli üksikasjad** kohalt **Toodete valimine**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-187">Select **Select products** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="ee6f5-188">Valige dialoogiboksi **Toote päring** vahekaardil **Vahemik** suvand **Lisa**, et lisada rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-188">In the **Product query** dialog box, on the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="ee6f5-189">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-189">In the new row, set the following values:</span></span>

    - <span data-ttu-id="ee6f5-190">**Tabel:** _Kaubad_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-190">**Table:** _Items_</span></span>
    - <span data-ttu-id="ee6f5-191">**Tuletatud tabel:** _Kaubad_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-191">**Derived table:** _Items_</span></span>
    - <span data-ttu-id="ee6f5-192">**Väli:** _Kaubakood_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-192">**Field:** _Item number_</span></span>
    - <span data-ttu-id="ee6f5-193">**Kriteeriumid:** _A0001_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-193">**Criteria:** _A0001_</span></span>

1. <span data-ttu-id="ee6f5-194">Oma päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-194">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="ee6f5-195">Valige ruudustiku **Täiendamismalli üksikasjad** kohalt **Täiendatavate tsoonide valimine**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-195">Select **Select zones to replenish** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="ee6f5-196">Valige dialoogiboksi **Tsooni päring** vahekaart **Vahemik**, et lisada rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-196">In the **Zone query** dialog box, on the **Range** tab, add a row to the grid.</span></span>
1. <span data-ttu-id="ee6f5-197">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-197">In the new row, set the following values:</span></span>

    - <span data-ttu-id="ee6f5-198">**Tabel:** _Lao tsoon_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-198">**Table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="ee6f5-199">**Tuletatud tabel:** _Lao tsoon_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-199">**Derived table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="ee6f5-200">**Väli:** _Tsooni ID_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-200">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="ee6f5-201">**Kriteerium:** _FLOOR_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-201">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="ee6f5-202">Oma päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-202">Select **OK** to save your query and close the dialog box.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="ee6f5-203">Asukohakorralduste häälestamine</span><span class="sxs-lookup"><span data-stu-id="ee6f5-203">Set up location directives</span></span>

<span data-ttu-id="ee6f5-204">Erinevalt asukohapõhisest min/maks. täiendamisest, nõuab tsoonipõhine min/max täiendamine, et seadistaksite nii komplekteerimise asukoha korralduse kui ka ladustamise korralduse, kuna süsteem hindab komplekteerimise asukoha asemel kogu tsooni väljamineva töö jaoks.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-204">Unlike location-based min/max replenishment, zone-based min/max replenishment requires that you set up both pick location directives and put location directives, because the system evaluates the whole zone instead of just the pick location for outbound work.</span></span>

#### <a name="view-and-edit-location-directives"></a><span data-ttu-id="ee6f5-205">Asukohakorralduste kuvamine ja redigeerimine</span><span class="sxs-lookup"><span data-stu-id="ee6f5-205">View and edit location directives</span></span>

<span data-ttu-id="ee6f5-206">Oma asukohakorralduste kuvamiseks või redigeerimiseks avage jaotis **Laohaldus \> Häälestus \> Asukohakorraldus**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-206">To view or edit your location directives, go to **Warehouse management \> Setup \> Location directives**.</span></span>

<span data-ttu-id="ee6f5-207">Vaadake järgmises jaotises olevaid näiteid, kuidas kasutada sätteid nõutava komplekteerimise asukohadirektiivi ja komplekteerimise asukohadirektiivi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-207">For examples that show how to use the settings to create the required pick location directives and put location directives, see the next section.</span></span>

#### <a name="prepare-demo-data-location-directives"></a><span data-ttu-id="ee6f5-208">Demoandmete asukohakorralduste ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="ee6f5-208">Prepare demo data location directives</span></span>

<span data-ttu-id="ee6f5-209">Demoandmete ettevalmistamiseks, et neid saaks kasutada selle teema lõpus kirjeldatud stsenaariumis, peate looma kaks asukohakorraldust: üks komplekteerimiseks ja teine ladustamiseks.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-209">To prepare demo data so that it can be used in the scenario at the end of this topic, you must create two location directives: one for pick and one for put.</span></span>

##### <a name="create-a-replenishment-pick-directive"></a><span data-ttu-id="ee6f5-210">Täiendamise komplekteerimise korralduse loomine</span><span class="sxs-lookup"><span data-stu-id="ee6f5-210">Create a replenishment pick directive</span></span>

1. <span data-ttu-id="ee6f5-211">Valige juriidiline isik **USMF** demoandmetega töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-211">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="ee6f5-212">Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-212">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="ee6f5-213">Määrake vasakpoolse paani välja **Töökäsu tüüp** suvandiks _Täiendamine_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-213">In the left pane, set the **Work order type** field to _Replenishment_.</span></span>
1. <span data-ttu-id="ee6f5-214">Uue korralduse loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-214">On the Action Pane, select **New** to create a new directive.</span></span>
1. <span data-ttu-id="ee6f5-215">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-215">Set the following values:</span></span>

    - <span data-ttu-id="ee6f5-216">**Järjekorranumber:** nõustuge vaikeväärtusega.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-216">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="ee6f5-217">**Nimi:** sisestage _Tsooni komplekteerimine_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-217">**Name:** Enter _Zone pick_.</span></span>
    - <span data-ttu-id="ee6f5-218">**Töö tüüp:** Valige _Komplekteerimine_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-218">**Work type:** Select _Pick_.</span></span>
    - <span data-ttu-id="ee6f5-219">**Tegevuskoht:** valige _6_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-219">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="ee6f5-220">**Ladu:** valige _61_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-220">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="ee6f5-221">**Korralduse kood:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-221">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="ee6f5-222">**Mitmik-SKU:** määrake selle suvandi väärtuseks _Ei_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-222">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="ee6f5-223">Valige **Salvesta**, et luua korraldus, millel on teie siiani konfigureeritud sätted.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-223">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="ee6f5-224">Valige kiirkaardil **Read** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-224">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="ee6f5-225">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-225">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ee6f5-226">**Järjekorranumber:** sisestage _1_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-226">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="ee6f5-227">**Alates kogusest:** sisestage _0_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-227">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="ee6f5-228">**Kuni koguseni:** sisestage _10000000_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-228">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="ee6f5-229">**Ühik:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-229">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="ee6f5-230">**Koguse asukoha leidmine:** valige _Puudub_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-230">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="ee6f5-231">**Piira ühiku alusel:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-231">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="ee6f5-232">**Ümardage ühikuni:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-232">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="ee6f5-233">**Pakendi koguse asukoha leidmine:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-233">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="ee6f5-234">**Luba tükeldamine:** märkige see ruut.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-234">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="ee6f5-235">Uue rea salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-235">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="ee6f5-236">Kui teie uus rida on valitud ruudustikul **Read**, valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-236">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="ee6f5-237">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-237">In the new row, set the following values:</span></span>

    - <span data-ttu-id="ee6f5-238">**Järjekorranumber:** sisestage _1_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-238">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="ee6f5-239">**Nimi:** sisestage _Hulgikomplekteerimine_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-239">**Name:** Enter _Pick from bulk_.</span></span>
    - <span data-ttu-id="ee6f5-240">**Fikseeritud asukoha kasutus:** valige _Fikseeritud ja mittefikseeritud asukohad_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-240">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="ee6f5-241">**Luba negatiivne laovaru:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-241">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="ee6f5-242">**Partii lubatud:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-242">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="ee6f5-243">**Strateegia:** valige _Puudub_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-243">**Strategy:** Select _None_.</span></span>

1. <span data-ttu-id="ee6f5-244">Uue tegevuse salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-244">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="ee6f5-245">Kui uus tegevus on valitud, valige ruudustiku **Asukohakorralduse tegevused** kohalt suvand **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-245">While your new action still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="ee6f5-246">Kuvatakse päringu dialoogiboks, kust saate valida asukohad, millest täiendada.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-246">A query dialog box appears, where you can select the locations to replenish from.</span></span> <span data-ttu-id="ee6f5-247">Vahekaardil **Vahemik** valige käsk **Lisa**, et lisada uus rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-247">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="ee6f5-248">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-248">In the new row, set the following values:</span></span>

    - <span data-ttu-id="ee6f5-249">**Tabel:** _Asukohad_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-249">**Table:** _Locations_</span></span>
    - <span data-ttu-id="ee6f5-250">**Tuletatud tabel:** _Asukohad_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-250">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="ee6f5-251">**Väli:** _Tsooni ID_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-251">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="ee6f5-252">**Kriteeriumid:** _BULK_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-252">**Criteria:** _BULK_</span></span>

1. <span data-ttu-id="ee6f5-253">Oma päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-253">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="ee6f5-254">Oma asukohakorralduse salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-254">Select **Save** to save your location directive.</span></span>

##### <a name="create-a-replenishment-put-directive"></a><span data-ttu-id="ee6f5-255">Täiendamise ladustamise korralduse loomine</span><span class="sxs-lookup"><span data-stu-id="ee6f5-255">Create a replenishment put directive</span></span>

1. <span data-ttu-id="ee6f5-256">Veenduge, et vasakpoolse paani lehel **Asukohakorraldused** oleks välja **Töökäsu tüüp** väärtuseks _Täiendamine_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-256">On the **Location directives** page, in the left pane, make sure that the **Work order type** field is still set to _Replenishment_.</span></span>
1. <span data-ttu-id="ee6f5-257">Muu korralduse loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-257">On the Action Pane, select **New** to create another new directive.</span></span>
1. <span data-ttu-id="ee6f5-258">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-258">Set the following values:</span></span>

    - <span data-ttu-id="ee6f5-259">**Järjekorranumber:** nõustuge vaikeväärtusega.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-259">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="ee6f5-260">**Nimi:** sisestage _Tsooni ladustamine_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-260">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="ee6f5-261">**Töötellimuse tüüp:** valige _Ladustamine_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-261">**Work order type:** Select _Put_.</span></span>
    - <span data-ttu-id="ee6f5-262">**Tegevuskoht:** valige _6_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-262">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="ee6f5-263">**Ladu:** valige _61_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-263">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="ee6f5-264">**Korralduskood:** valige _Tsooni täiend_, et linkida see asukohakorraldus eelnevalt loodud täiendamismalliga, kasutades eelnevalt loodud koodi.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-264">**Directive code:** Select _Zone replen_ to link this location directive with the replenishment template that you created earlier by using the code that you created earlier.</span></span>
    - <span data-ttu-id="ee6f5-265">**Mitmik-SKU:** määrake selle suvandi väärtuseks _Ei_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-265">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="ee6f5-266">Valige **Salvesta**, et luua korraldus, millel on teie siiani konfigureeritud sätted.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-266">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="ee6f5-267">Valige kiirkaardil **Read** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-267">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="ee6f5-268">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-268">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ee6f5-269">**Järjekorranumber:** sisestage _1_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-269">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="ee6f5-270">**Alates kogusest:** sisestage _0_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-270">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="ee6f5-271">**Kuni koguseni:** sisestage _10000000_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-271">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="ee6f5-272">**Ühik:** jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-272">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="ee6f5-273">**Koguse asukoha leidmine:** valige _Puudub_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-273">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="ee6f5-274">**Piira ühiku alusel:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-274">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="ee6f5-275">**Ümardage ühikuni:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-275">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="ee6f5-276">**Pakendi koguse asukoha leidmine:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-276">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="ee6f5-277">**Luba tükeldamine:** märkige see ruut.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-277">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="ee6f5-278">Uue rea salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-278">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="ee6f5-279">Kui teie uus rida on valitud ruudustikul **Read**, valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus**, et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-279">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="ee6f5-280">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-280">In the new row, set the following values:</span></span>

    - <span data-ttu-id="ee6f5-281">**Järjekorranumber:** sisestage _1_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-281">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="ee6f5-282">**Nimi:** sisestage _Tsooni ladustamine_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-282">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="ee6f5-283">**Fikseeritud asukoha kasutus:** valige _Fikseeritud ja mittefikseeritud asukohad_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-283">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="ee6f5-284">**Luba negatiivne laovaru:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-284">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="ee6f5-285">**Partii lubatud:** tühjendage see märkeruut.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-285">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="ee6f5-286">**Strateegia:** valige _Konsolideeri_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-286">**Strategy:** Select _Consolidate_.</span></span>

1. <span data-ttu-id="ee6f5-287">Uue tegevuse salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-287">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="ee6f5-288">Kui uus tegevus on endiselt valitud, valige ruudustiku **Asukohakorralduse tegevused** kohalt suvand **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-288">While your new action is still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="ee6f5-289">Kuvatakse päringu dialoogiboks, kust saate valida tsooni, kuhu täiendada.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-289">A query dialog box appears, where you can select the zone to replenish to.</span></span> <span data-ttu-id="ee6f5-290">See tsoon peaks vastama täiendamismallis määratud tsoonile.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-290">This zone should be the same zone that is specified in the replenishment template.</span></span> <span data-ttu-id="ee6f5-291">Vahekaardil **Vahemik** valige käsk **Lisa**, et lisada uus rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-291">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="ee6f5-292">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-292">In the new row, set the following values:</span></span>

    - <span data-ttu-id="ee6f5-293">**Tabel:** _Asukohad_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-293">**Table:** _Locations_</span></span>
    - <span data-ttu-id="ee6f5-294">**Tuletatud tabel:** _Asukohad_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-294">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="ee6f5-295">**Väli:** _Tsooni ID_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-295">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="ee6f5-296">**Kriteerium:** _FLOOR_</span><span class="sxs-lookup"><span data-stu-id="ee6f5-296">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="ee6f5-297">Oma päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-297">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="ee6f5-298">Oma asukohakorralduse salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-298">Select **Save** to save your location directive.</span></span>

## <a name="scenario"></a><span data-ttu-id="ee6f5-299">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="ee6f5-299">Scenario</span></span>

<span data-ttu-id="ee6f5-300">Selles jaotises esitatakse näidisstsenaarium, mis näitab, kuidas selle funktsiooniga töötada.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-300">This section provides a sample scenario that shows how to work with the feature.</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a><span data-ttu-id="ee6f5-301">Valmistage ette näidisstsenaariumi jaoks nõutavad näidisandmed</span><span class="sxs-lookup"><span data-stu-id="ee6f5-301">Prepare the sample data that is required for the sample scenario</span></span>

<span data-ttu-id="ee6f5-302">Enne kui alustate stsenaariumi kasutamist, peate aktiveerima näidisandmed ja seadistama selle funktsiooni selle teema käesolevas ja eelnevates jaotistes kirjeldatu järgi.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-302">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section and in the previous sections of this topic.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="ee6f5-303">Juriidilise isiku USMF kasutamine</span><span class="sxs-lookup"><span data-stu-id="ee6f5-303">Use the USMF legal entity</span></span>

<span data-ttu-id="ee6f5-304">Selle stsenaariumi kasutamiseks siin määratud näidiskirjete ja -väärtuste abil peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ee6f5-304">To work through the scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="ee6f5-305">Enne alustamist peate valima ka juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-305">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="prepare-additional-sample-data"></a><span data-ttu-id="ee6f5-306">Täiendavate näidisandmete ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="ee6f5-306">Prepare additional sample data</span></span>

<span data-ttu-id="ee6f5-307">Pärast juriidilise isiku **USMF** valimist, lisage nõutavad täiendavad näidisandmed, nagu on kirjeldatud selle teema varasemas jaotises [Tsoonipõhise täiendamise häälestus](#setup).</span><span class="sxs-lookup"><span data-stu-id="ee6f5-307">After you've selected the **USMF** legal entity, add the additional sample data that is required, as described in the [Set up zone-based replenishment](#setup) section earlier in this topic.</span></span>

#### <a name="check-your-on-hand-inventory"></a><span data-ttu-id="ee6f5-308">Vaba kaubavaru kontrollimine</span><span class="sxs-lookup"><span data-stu-id="ee6f5-308">Check your on-hand inventory</span></span>

<span data-ttu-id="ee6f5-309">Järgige neid etappe, et veenduda, kas teie süsteem sisaldab näidisstsenaariumi toetamiseks piisavalt varusid.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-309">Follow these steps to make sure that your system includes enough inventory to support the sample scenario.</span></span>

1. <span data-ttu-id="ee6f5-310">Veenduge, et kauba *A0001* jaoks oleks vaba kaubavaru komplekteerimistsooni kahes eri asukohas (*FLOOR*), mis on määratud täiendamismallis.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-310">Make sure that there is on-hand inventory for item *A0001* at two different locations in the pick zone (*FLOOR*) that is specified in the replenishment template.</span></span> <span data-ttu-id="ee6f5-311">Kuid kogu varu peaks olema väiksem kui nõutav minimaalne kogus (*50*), mis on määratletud täiendamismallis.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-311">However, the total inventory should be less than the required minimum quantity (*50*) that is specified on the replenishment template.</span></span> <span data-ttu-id="ee6f5-312">Sel viisil saate simuleerida, kuidas toimub arvutamine üksiku asukoha asemel terve tsooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-312">In this way, you can simulate how the calculation occurs for the whole zone instead of just for a single location.</span></span> <span data-ttu-id="ee6f5-313">**Kasutage varude korrigeerimiseks mis tahes laoprotsessi.**</span><span class="sxs-lookup"><span data-stu-id="ee6f5-313">**Use any of the warehouse processes to adjust inventory as required.**</span></span>
1. <span data-ttu-id="ee6f5-314">Veenduge, et kauba *A0001* jaoks oleks piisavalt varusid hulgiasukohas, mis on määratud tsooni komplekteerimise asukohakorralduses, kus täiendamistöö peaks komplekteerima kaubad tsooni ID-st *BULK*.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-314">Make sure that there is enough inventory for item *A0001* at a bulk location that is specified in the zone pick location directive where the replenishment work should pick the items from zone ID *BULK*.</span></span> <span data-ttu-id="ee6f5-315">Kogu varu peaks olema rohkem kui nõutav maksimaalne kogus (*150*), mis on määratletud täiendamismallis.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-315">The total inventory must be more than the required maximum quantity (*150*) that is specified in the replenishment template.</span></span>
1. <span data-ttu-id="ee6f5-316">Valikuline, kuid soovitatav: tehke lao korrigeerimise töölehe loomiseks järgmist.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-316">Optional but recommended: Follow these steps to create an inventory adjustment journal:</span></span>

    1. <span data-ttu-id="ee6f5-317">Avage jaotis **Varude haldus \> Töölehe sisestused \> Kaubad \> Varude korrigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-317">Go to **Inventory management \> Journal entries \> Items \> Inventory adjustment**.</span></span>
    1. <span data-ttu-id="ee6f5-318">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-318">Select **New**.</span></span>
    1. <span data-ttu-id="ee6f5-319">Valige dialoogiboksi **Varude töölehe loomine** väljal **Ladu** väärtus *61*.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-319">In the **Create inventory journal** dialog box, in the **Warehouse** field, select *61*.</span></span>
    1. <span data-ttu-id="ee6f5-320">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-320">Select **OK**.</span></span>
    1. <span data-ttu-id="ee6f5-321">Kasutage kiirkaardil **Töölehe read** nuppu **Uus**, et lisada ruudustikku kolm rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-321">On the **Journal lines** FastTab, use the **New** button to add three lines to the grid, and set the following values.</span></span> <span data-ttu-id="ee6f5-322">Pärast kõigi ridade seadistamise lõpule viimist valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-322">After you've finished setting up each line, select **Save**.</span></span>

        - <span data-ttu-id="ee6f5-323">**Rida 1:**</span><span class="sxs-lookup"><span data-stu-id="ee6f5-323">**Line 1:**</span></span>

            - <span data-ttu-id="ee6f5-324">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ee6f5-324">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="ee6f5-325">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="ee6f5-325">**Site:** *6*</span></span>
            - <span data-ttu-id="ee6f5-326">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="ee6f5-326">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="ee6f5-327">**Asukoht:** *02A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="ee6f5-327">**Location:** *02A01R1S1B*</span></span>
            - <span data-ttu-id="ee6f5-328">**Identifitseerimisnumber:** valige loendist olemasolev identifitseerimisnumber või looge uus.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-328">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="ee6f5-329">**Kogus:** *1000*</span><span class="sxs-lookup"><span data-stu-id="ee6f5-329">**Quantity:** *1000*</span></span>

        - <span data-ttu-id="ee6f5-330">**Rida 2:**</span><span class="sxs-lookup"><span data-stu-id="ee6f5-330">**Line 2:**</span></span>

            - <span data-ttu-id="ee6f5-331">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ee6f5-331">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="ee6f5-332">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="ee6f5-332">**Site:** *6*</span></span>
            - <span data-ttu-id="ee6f5-333">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="ee6f5-333">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="ee6f5-334">**Asukoht:** *07A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="ee6f5-334">**Location:** *07A01R2S1B*</span></span>
            - <span data-ttu-id="ee6f5-335">**Identifitseerimisnumber:** valige loendist olemasolev identifitseerimisnumber või looge uus.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-335">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="ee6f5-336">**Kogus:** *15*</span><span class="sxs-lookup"><span data-stu-id="ee6f5-336">**Quantity:** *15*</span></span>

        - <span data-ttu-id="ee6f5-337">**Rida 3:**</span><span class="sxs-lookup"><span data-stu-id="ee6f5-337">**Line 3:**</span></span>

            - <span data-ttu-id="ee6f5-338">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ee6f5-338">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="ee6f5-339">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="ee6f5-339">**Site:** *6*</span></span>
            - <span data-ttu-id="ee6f5-340">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="ee6f5-340">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="ee6f5-341">**Asukoht:** *07A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="ee6f5-341">**Location:** *07A01R1S1B*</span></span>
            - <span data-ttu-id="ee6f5-342">**Identifitseerimisnumber:** valige loendist olemasolev identifitseerimisnumber või looge uus.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-342">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="ee6f5-343">**Kogus:** *10*</span><span class="sxs-lookup"><span data-stu-id="ee6f5-343">**Quantity:** *10*</span></span>

    1. <span data-ttu-id="ee6f5-344">Valige toimingupaanil **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-344">On the Action Pane, select **Validate**.</span></span> <span data-ttu-id="ee6f5-345">Lahendage kõik leitud tõrked enne järgmisse etappi liikumist.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-345">Address any errors that are found before you move on to the next step.</span></span>
    1. <span data-ttu-id="ee6f5-346">Varude lattu sisestamiseks valige toimingupaanil **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-346">On the Action Pane, select **Post** to post the inventory to the warehouse.</span></span>

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a><span data-ttu-id="ee6f5-347">Näidisstsenaarium: käivitage tsoonipõhine min/max täiendamine</span><span class="sxs-lookup"><span data-stu-id="ee6f5-347">Sample scenario: Run zone-based min/max replenishment</span></span>

<span data-ttu-id="ee6f5-348">Kui kõik eeltingimuseks olevad näidisandmed on olemas, saate käivitada täiendamise, järgides neid etappe.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-348">After all the prerequisite sample data is in place, you can trigger replenishment by following these steps.</span></span>

1. <span data-ttu-id="ee6f5-349">Avage jaotis **Laohaldus \> Täiendamine \> Täiendamine**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-349">Go to **Warehouse management \> Replenishment \> Replenishments**.</span></span>
1. <span data-ttu-id="ee6f5-350">Valige dialoogiboksi **Täiendamine** kiirkaardil **Kaasatavad kirjed** suvand **Filter**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-350">In the **Replenishment** dialog box, on the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="ee6f5-351">Redigeerige dialoogiboksi **Päring** vahekaardil **Vahemik** tabeli vaikerida järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-351">In the **Inquiry** dialog box, on the **Range** tab, edit the default table row in the following way:</span></span>

    - <span data-ttu-id="ee6f5-352">**Tabel:** valige _Täiendamismallid_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-352">**Table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="ee6f5-353">**Tuletatud tabel:** valige _Täiendamismallid_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-353">**Derived table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="ee6f5-354">**Väli:** valige _Täiendamismall_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-354">**Field:** Select _Replenishment template_.</span></span>
    - <span data-ttu-id="ee6f5-355">**Kriteeriumid:** valige _Tsoon min/max täiend_.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-355">**Criteria:** Select _Zone min/max replen_.</span></span> <span data-ttu-id="ee6f5-356">Selle sama täiendamismalli lõite selle stsenaariumi jaoks demoandmete ettevalmistamise ajal.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-356">This replenishment template is the replenishment template that you created while you were preparing the demo data for this scenario.</span></span>

1. <span data-ttu-id="ee6f5-357">Päringu salvestamiseks sulgemiseks valige **OK** ja minge tagasi dialoogiboksi **Täiendamine**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-357">Select **OK** to save the query and go back to the **Replenishment** dialog box.</span></span>
1. <span data-ttu-id="ee6f5-358">Täiendamismalli käitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-358">Select **OK** to run the replenishment template.</span></span>

<span data-ttu-id="ee6f5-359">Täiendamistöö on nüüd loodud, et komplekteerida varusid tsoonist *BULK* ja täiendada tsooni *FLOOR*.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-359">Replenishment work is now created to pick inventory from the *BULK* zone and replenish it to the *FLOOR* zone.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="ee6f5-360">Märkmed ja näpunäited</span><span class="sxs-lookup"><span data-stu-id="ee6f5-360">Notes and tips</span></span>

<span data-ttu-id="ee6f5-361">Siin on mõningaid märkuseid ja näpunäited funktsiooniga töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-361">Here are a few notes and tips for working with the feature:</span></span>

- <span data-ttu-id="ee6f5-362">Täiendamistöö seadistamiseks, mis läheks soovitud tsooni, saate linkida täiendamismalli read ja asukohkorraldused ühel järgmistest viisidest.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-362">To set up replenishment work that goes to the desired zone, you can link the replenishment template lines and location directives in either of the following ways:</span></span>

    - <span data-ttu-id="ee6f5-363">Redigeerige asukohakorralduse päise päringut ja filtreerige valitud täiendamismalli read.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-363">Edit the location directive header query, and filter the selected replenishment template lines.</span></span>
    - <span data-ttu-id="ee6f5-364">Kasutage korralduskoodi täiendamismalli real ja muutke see ladustamise asukohakorraldusele vastavaks.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-364">Use a directive code on the replenishment template line, and match it to the put location directive.</span></span>

- <span data-ttu-id="ee6f5-365">Kui kasutate dünaamilisi asukohti, luuakse täiendamistöö kas esimese saadaoleva asukoha või juba varusid sisaldava asukoha jaoks, kui asukohakorralduse tegevus on seadistatud kasutama strateegiat **Konsolideerimine**.</span><span class="sxs-lookup"><span data-stu-id="ee6f5-365">If you're using dynamic locations, replenishment work will be created either for the first available location or for a location that already contains inventory, if the location directive action is set up to use the **Consolidate** strategy.</span></span>
- <span data-ttu-id="ee6f5-366">Kui kasutate tsoonide asemel fikseeritud asukohti, peaksite kasutama [standardset min/max täiendamist](tasks/set-up-min-max-replenishment-process.md).</span><span class="sxs-lookup"><span data-stu-id="ee6f5-366">If you're using fixed locations instead of zones, you should use [standard min/max replenishment](tasks/set-up-min-max-replenishment-process.md).</span></span>
