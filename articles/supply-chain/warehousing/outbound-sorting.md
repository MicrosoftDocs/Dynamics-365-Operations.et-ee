---
title: Väljastuste sortimine
description: Selles teemas antakse teavet väljamineku sortimise kohta. See funktsioon hõlbustab väikeste konteinerite käsitsemist ja aitab lao töötajatel veokis kaubaaluste mahutavust tõhusamalt planeerida ja korraldada.
author: Mirzaab
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3c576209a86f776ac424f7fb9f2b606bea774a67
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828390"
---
# <a name="outbound-sorting"></a><span data-ttu-id="c2ffd-104">Väljastuste sortimine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2ffd-105">See funktsioon hõlbustab väikeste konteinerite käsitsemist ja aitab lao töötajatel veokis kaubaaluste mahutavust tõhusamalt planeerida ja korraldada.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="c2ffd-106">Kui kasutate väljamineku sortimist, saate sortida pakitud konteinereid õigele kaubaalusele, kui need tulevad pakkimisjaamast.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="c2ffd-107">Saate luua ka pakkimise hierarhia.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="c2ffd-108">See funktsioon võimaldab teil luua kaubaaluseid konteineritest, mis on pakitud pakkimise funktsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="c2ffd-109">Konteinerit ei saadeta lõplikku saadetise asukohta, kuna see on algses pakkimisvoos.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="c2ffd-110">Selle asemel saavad töötajad konteineri sulgeda ja teisaldada selle sortimise tüübi asukohta.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="c2ffd-111">Seejärel saavad nad sortida konteinereid asukohtadele, millel on oma identifitseerimisnumber (LP).</span><span class="sxs-lookup"><span data-stu-id="c2ffd-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="c2ffd-112">Kui konteinerid on sorditud, saab luua töö, et saata kogu identifitseerimisnumber lõplikku saadetise laadimise või vaheasukohta, mis põhineb asukohakorraldustel või teie enda nõudmistel.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="c2ffd-113">Lisaks saab sortimise asukoha sulgemise tegevus teisaldada varud kohe lõplikku saadetise asukohta ja komplekteerida tellimusele.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="c2ffd-114">Väljamineku sortimise funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="c2ffd-115">Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="c2ffd-116">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="c2ffd-117">Seega on funktsioon loetletud järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c2ffd-118">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c2ffd-119">**Funktsiooni nimi:** *Väljamineku sortimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="c2ffd-120">Häälestus</span><span class="sxs-lookup"><span data-stu-id="c2ffd-120">Setup</span></span>

<span data-ttu-id="c2ffd-121">Selle stsenaariumi puhul peate kasutama standardseid demoandmeid **USMF** ja ladu *62*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="c2ffd-122">Samuti peate lõpule viima järgmistes alamjaotistes kirjeldatud seadistuse.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="c2ffd-123">Voomalli seadistamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-123">Set up a wave template</span></span>

<span data-ttu-id="c2ffd-124">See seadistus töötleb automaatselt seda voogu ja loob töö, kui rida väljastatakse lattu.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="c2ffd-125">Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="c2ffd-126">Valige mallide loendist **Ladu 62**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="c2ffd-127">Veenduge, et kiirkaardil **Üldine** oleks suvandi **Töötle voogu lattu vabastamisel** väärtuseks seatud *Jah*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="c2ffd-128">Töötaja seadistamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-128">Set up a worker</span></span>

<span data-ttu-id="c2ffd-129">Pakkimisjaama loetakse asukohaks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-129">The packing station is considered a location.</span></span> <span data-ttu-id="c2ffd-130">Lao töötajad, kes logivad pakkimisjaamas sisse, näevad ja töötavad ainult selles konkreetses pakkimise asukohas plaanitud saadetiste ja konteineritega.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="c2ffd-131">Kasutaja, kes logib sisse rakendusse Microsoft Dynamics 365, tuleb seadistada töötajaks Laohalduses.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="c2ffd-132">Kui kasutaja nime ei kuvata töökasutajate loendis, kasutage selle lisamiseks järgmist protseduuri.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="c2ffd-133">Need etapid eeldavad, et kasutaja on süsteemis juba olemas ja on seostatud töövõtja või töötajaga moodulis **Inimressurssid**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="c2ffd-134">Avage jaotis **Laohaldus \> Seadistus \> Töötaja**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="c2ffd-135">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-135">Select **New**.</span></span>
1. <span data-ttu-id="c2ffd-136">Valige väljal **Töötaja** töötajate loendist sihtkasutaja.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="c2ffd-137">Valige käsk **Vali**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-137">Select **Select**.</span></span>
1. <span data-ttu-id="c2ffd-138">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c2ffd-139">Valige kiirkaardil **Kasutajad** suvand **Uus**, et luua mobiilse seadme konto ja seadke sellele järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="c2ffd-140">**Kasutaja ID:** sisestage kordumatu ID.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="c2ffd-141">**Kasutajanimi:** sisestage nimi ID jaoks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="c2ffd-142">**Vaikeladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="c2ffd-143">**Menüü nimi:** *Peamine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="c2ffd-144">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c2ffd-145">Kuvatakse dialoogiboks **Parooli määramine**, kus saate luua lihtsa parooli, mida kasutaja saab mobiilirakendusse sisselogimiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="c2ffd-146">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-146">Set the following values:</span></span>

    - <span data-ttu-id="c2ffd-147">**Parool:** sisestage lihtne parool.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="c2ffd-148">**Kinnita parool:** sisestage uuesti sama parool.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="c2ffd-149">Valige suvand **Sea parool**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-149">Select **Set password**.</span></span>

    <span data-ttu-id="c2ffd-150">Tegevuskeskuse teatis ütleb, et teie loodud kasutaja jaoks on parool määratud.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="c2ffd-151">Asukoha tüübi loomine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-151">Create a location type</span></span>

1. <span data-ttu-id="c2ffd-152">Avage jaotis **Laohaldus \> Seadistus \> Ladu \> Asukoha tüübid**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="c2ffd-153">Valige toimingupaanil **Uus**, et luua asukoha tüüp ja määrake sellele järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="c2ffd-154">**Asukoha tüüp:** *SORTIMINE*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="c2ffd-155">**Kirjeldus:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="c2ffd-156">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="c2ffd-157">Laohalduse parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="c2ffd-158">Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="c2ffd-159">Määrake vahekaardi **Üldine** kiirkaardi **Asukoha tüübid** välja **Sortimise asukoha tüüp** väärtuseks *SORTIMINE*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="c2ffd-160">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="c2ffd-161">Asukohaprofiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-161">Set up a location profile</span></span>

1. <span data-ttu-id="c2ffd-162">Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukohaprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="c2ffd-163">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c2ffd-164">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-165">**Asukohaprofiili ID:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="c2ffd-166">**Nimi:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="c2ffd-167">Määrake kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-168">**Asukoha vorming:** *ASRB* (riiulirida-sektsioon-riiul-asukoht)</span><span class="sxs-lookup"><span data-stu-id="c2ffd-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="c2ffd-169">**Asukoha tüüp:** *SORTIMINE*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="c2ffd-170">**Kasuta identifitseerimisnumbri jälgimist:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="c2ffd-171">**Luba segakaubad:** *Jah* (kui määrate selle suvandi väärtuseks *Jah*, määratakse suvandi **Luba segatud varude partiid** väärtuseks *Jah* ja seda ei saa eraldi muuta.)</span><span class="sxs-lookup"><span data-stu-id="c2ffd-171">**Allow mixed items:** *Yes* (When you set this option to *Yes*, the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="c2ffd-172">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="c2ffd-173">Asukoha seadistamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-173">Set up a location</span></span>

1. <span data-ttu-id="c2ffd-174">Avage **Laohaldus \> Seadistus \> Ladu \> Asukohad**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="c2ffd-175">Tühjendage päises märkeruut **Loo kontrollnumbrid asukoha jaoks**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="c2ffd-176">Valige toimingupaanil **Uus**, et luua asukoht ja määrake sellele järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="c2ffd-177">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="c2ffd-178">**Asukoht:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="c2ffd-179">**Asukohaprofiili ID:** *SORTIMINE*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="c2ffd-180">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="c2ffd-181">Väljamineku sortimismalli seadistamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="c2ffd-182">Väljamineku sortimismall määratleb, kas töö luuakse sortimise asukohast ja kas sortimine toimub käsitsi või automaatselt.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="c2ffd-183">Selle stsenaariumi korral loote väljamineku sortimismalli, et koostada kaubaaluseid pärast pakkimisjaama.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="c2ffd-184">Avage jaotis **Laohaldus \> Seadistus \> Pakkimine \> Väljamineku sortimismallid**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="c2ffd-185">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c2ffd-186">Määrake uue malli päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-187">**Väljamineku sortimismalli ID:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="c2ffd-188">**Kirjeldus:** *Automaatne töö loomine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="c2ffd-189">**Väljamineku sortimismalli tüüp:** *Konteiner*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="c2ffd-190">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="c2ffd-191">**Asukoht:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="c2ffd-192">Määrake kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-193">**Sortimise kontrollimine:** *Asukoha skannimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="c2ffd-194">**Loo töö asukoha sulgemisel:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="c2ffd-195">Kui selle suvandi väärtuseks on seatud *Jah*, kui asukoht on suletud, luuakse töö varude lõppsihtkohta teisaldamiseks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-195">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="c2ffd-196">Kui väärtuseks on seatud *Ei*, komplekteeritakse varud asukoha sulgemisel kohe tellimusele.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-196">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="c2ffd-197">**Asukoha määramine:** *Automaatne*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="c2ffd-198">Kui välja väärtuseks on seatud *Käsitsi*, peab kasutaja alati näitama, millisesse asukohta varud sortida tuleb.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-198">If this field is set to *Manual*, the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="c2ffd-199">Kui selleks on seatud *Automaatne*, juhib süsteem varud võimaluse korral automaatselt asukohta, võttes aluseks sortimismalli jaotamised.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-199">If it's set to *Automatic*, the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="c2ffd-200">Valige **Salvesta**, et muuta nupp **Redigeeri päringut** toimingupaanil kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="c2ffd-201">Valige toimingupaanil **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="c2ffd-202">Lisage päringuredaktoris vahekaardile **Sortimine** rida, millel on järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="c2ffd-203">**Tabel:** *Saadetised*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="c2ffd-204">**Tuletatud tabel:** *Saadetised*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="c2ffd-205">**Väli:** *Vedaja teenus*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="c2ffd-206">Kui valite selle väärtuse, võidakse kuvada järgmine teade: „Väli Vedaja teenus pole indeksi väli.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="c2ffd-207">Kas soovite lisada sellele sortimise?”</span><span class="sxs-lookup"><span data-stu-id="c2ffd-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="c2ffd-208">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-208">Select **Yes**.</span></span>

    - <span data-ttu-id="c2ffd-209">**Otsingusuund:** *Kasvav*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="c2ffd-210">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-210">Select **OK**.</span></span>
1. <span data-ttu-id="c2ffd-211">Teile võidakse kuvada järgmine teade: „Grupeerimine lähtestatakse, kas soovite jätkata?”</span><span class="sxs-lookup"><span data-stu-id="c2ffd-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="c2ffd-212">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-212">Select **Yes**.</span></span>

    <span data-ttu-id="c2ffd-213">Toimingupaani nupp **Väljamineku sortimismalli piirid** muutub kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="c2ffd-214">Valige toimingupaanil **Väljamineku sortimismalli piirid**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="c2ffd-215">Määrake dialoogiboksis **Väljamineku sortimise kriteeriumid** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-216">**Viitetabeli nimi:** *Saadetised*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="c2ffd-217">**Viitevälja nimi:** *Vedaja teenus*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="c2ffd-218">**Grupeeri välja alusel:** märkige see ruut, et grupeerida saadetised vedaja teenuse alusel.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="c2ffd-219">Valige **OK**, et salvestada oma sätted ja sulgeda dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="c2ffd-220">Konteineri pakkimise poliitikate seadistamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-220">Set up container packing policies</span></span>

1. <span data-ttu-id="c2ffd-221">Avage jaotis **Laohaldus \> Seadistus \> Konteinerid \> Konteineri pakkimise poliitikad**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="c2ffd-222">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c2ffd-223">Määrake uue poliitika päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-224">**Konteineri pakkimise poliitika:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="c2ffd-225">**Kirjeldus:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="c2ffd-226">Määrake kiirkaardil **Ülevaade** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-227">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="c2ffd-228">**Sortimise vaikeasukoht:** *SORTIMINE*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="c2ffd-229">**Massiühik:** *kg*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="c2ffd-230">**Konteineri sulgemise poliitika:** *Automaatne väljastamine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="c2ffd-231">**Konteineri väljastamise poliitika:** *Konteineri määramine väljamineku sortimise asukohale*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="c2ffd-232">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="c2ffd-233">Pakkimisprofiilide seadistamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-233">Set up packing profiles</span></span>

<span data-ttu-id="c2ffd-234">Looge uus pakkimisprofiil, mida kasutatakse koos sortimise funktsiooniga.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="c2ffd-235">Avage jaotis **Laohaldus \> Seadistus \> Pakkimine \> Pakkimisprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="c2ffd-236">Valige toimingupaanil **Uus**, et luua rida ja määrake sellele järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="c2ffd-237">**Pakkimisprofiili ID:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="c2ffd-238">**Kirjeldus:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="c2ffd-239">**Konteineri pakkimise poliitika:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="c2ffd-240">**Konteineri ID-režiim:** *Automaatne*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="c2ffd-241">**Konteineri tüüp:** *Box-Large*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="c2ffd-242">**Konteineri automaatne loomine konteineri sulgemisel:** tühjendatud (= *Ei*)</span><span class="sxs-lookup"><span data-stu-id="c2ffd-242">**Auto create container at container close:** Cleared (= *No*)</span></span>

1. <span data-ttu-id="c2ffd-243">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="c2ffd-244">Töö klasside seadistamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-244">Set up work classes</span></span>

<span data-ttu-id="c2ffd-245">Seadistage töö klass, mida kasutatakse koos sortimisega.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="c2ffd-246">Minge jaotisse **Laohaldus \> Seadistus \> Töö \> Töö klassid**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="c2ffd-247">Valige toimingupaanil **Uus**, et luua sortimiseks töö klass ja määrake sellele järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="c2ffd-248">**Töö klassi ID:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="c2ffd-249">**Kirjeldus:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="c2ffd-250">**Töötellimuse tüüp:** *Sorditud varude komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="c2ffd-251">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="c2ffd-252">Mobiilse seadme menüü-üksuste seadistamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="c2ffd-253">Uue kaubaaluse menüü-üksuse seadistamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="c2ffd-254">Looge mobiilse seadme menüü-üksus kaubaaluste loomiseks sortimise ajal.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="c2ffd-255">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="c2ffd-256">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c2ffd-257">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-258">**Menüü-üksuse nimi:** *Kaubaaluse loomine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="c2ffd-259">**Pealkiri:** *Kaubaaluse loomine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="c2ffd-260">**Režiim:** *Kaudne*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="c2ffd-261">**Kasuta olemasolevat tööd:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="c2ffd-262">Määrake kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-263">**Tegevuse kood:** *Väljamineku sortimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="c2ffd-264">Kui selle välja väärtuseks on seatud *Väljamineku sortimine*, kuvatakse väli **Väljamineku sortimismalli ID**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-264">When this field is set to *Outbound sorting*, the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="c2ffd-265">**Protsessijuhendi kasutamine:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="c2ffd-266">Kui välja **Tegevuse kood** on seatud *Väljamineku sortimine*, seatakse selle suvandi väärtuseks automaatselt *Jah*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-266">When the **Activity code** field is set to *Outbound sorting*, this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="c2ffd-267">**Väljamineku sortimismalli ID:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="c2ffd-268">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="c2ffd-269">Uue laadimise menüü-üksuse seadistamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-269">Set up a new loading menu item</span></span>

<span data-ttu-id="c2ffd-270">Järgmisena looge menüü-üksus, mis võimaldab kasutajatel teisaldada sorditud laokaupu saadetise asukohta.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="c2ffd-271">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="c2ffd-272">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c2ffd-273">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-274">**Menüü-üksuse nimi:** *Laadimine sortimisest*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="c2ffd-275">**Pealkiri:** *Laadimine sortimisest*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="c2ffd-276">**Režiim:** *töö*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="c2ffd-277">**Kasuta olemasolevat tööd:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="c2ffd-278">Määrake kiirkaardi **Üldine** väljal **Suunaja** väärtuseks *Kasutaja suunatud*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="c2ffd-279">Valige kiirkaardil **Tööklassid** suvand **Uus** ja seejärel seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-279">On the **Work classes** FastTab, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="c2ffd-280">**Töö klassi ID:** *SORTIMINE*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="c2ffd-281">**Töötellimuse tüüp:** *Sorditud varude komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="c2ffd-282">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="c2ffd-283">Mobiilse seadme menüü seadistamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-283">Set up the mobile device menu</span></span>

<span data-ttu-id="c2ffd-284">Nüüd peate lisama uued menüü-üksused mobiilse seadme menüüsse.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="c2ffd-285">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="c2ffd-286">Valige menüü **Väljaminev**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="c2ffd-287">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="c2ffd-288">Otsige üles ja valige veerus **Saadaolevad menüüd ja menüü-üksused** suvand **Kaubaaluse loomine**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="c2ffd-289">Valige paremnoole nupp, et teisaldada **Kaubaaluse loomine** veergu **Menüü struktuur**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="c2ffd-290">Kasutage üles- ja allanoole nuppe, et lisada menüü-üksus **Kaubaaluse loomine** mobiilse seadme menüüs soovitud asukohta.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="c2ffd-291">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-291">Select **Save**.</span></span>
1. <span data-ttu-id="c2ffd-292">Korrake seda protseduuri, et lisada menüü-üksus **Laadimine sortimisest** menüüsse **Väljaminev**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="c2ffd-293">Asukohakorralduste häälestamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-293">Set up location directives</span></span>

<span data-ttu-id="c2ffd-294">*Asukohakorraldused* on reeglid, mis aitavad tuvastada komplekteerimise ja ladustamise asukohti varude liigutamisel.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="c2ffd-295">Nüüd tuleb luua reegel sortimise töö haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="c2ffd-296">Üksiku SKU-korralduse seadistamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="c2ffd-297">Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="c2ffd-298">Muutke vasakpoolsel paanil välja **Töökäsu tüüp** väärtuseks *Sorditud varude komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="c2ffd-299">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c2ffd-300">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-301">**Järjestus:** *1*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="c2ffd-302">**Nimi:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="c2ffd-303">Määrake kiirkaardil **Asukohakorraldused** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-304">**Töö tüüp:** *Ladustamine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="c2ffd-305">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-305">**Site:** *6*</span></span>
    - <span data-ttu-id="c2ffd-306">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="c2ffd-307">**Mitu SKU-d:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="c2ffd-308">Valige **Salvesta**, et muuta tööriistariba kiirkaardil **Read** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="c2ffd-309">Valige kiirkaardil **Read** suvand **Uus** ja seejärel seadke uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-309">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="c2ffd-310">Võtke vastu kõigi teiste väljade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="c2ffd-311">**Järjestus:** *1*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="c2ffd-312">**Alates:** *0*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-312">**From:** *0*</span></span>
    - <span data-ttu-id="c2ffd-313">**Kuni:** *1 000 000*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="c2ffd-314">Valige **Salvesta**, et muuta tööriistariba kiirkaardil **Asukohakorralduse toimingud** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="c2ffd-315">Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus** ja seejärel seadke uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-315">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="c2ffd-316">Võtke vastu kõigi teiste väljade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="c2ffd-317">**Järjestus:** *1*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="c2ffd-318">**Nimi:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="c2ffd-319">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-319">Select **Save**.</span></span>
1. <span data-ttu-id="c2ffd-320">Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="c2ffd-321">Otsige päringuredaktori vahekaardil **Vahemik** üles rida, kus välja **Väli** väärtuseks on seatud *Asukoht*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="c2ffd-322">Määrake selle rea välja **Kriteeriumid** väärtuseks *Baydoor*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="c2ffd-323">Oma sätete salvestamiseks ja päringuredaktori sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="c2ffd-324">Mitme SKU-korralduse seadistamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="c2ffd-325">Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="c2ffd-326">Muutke vasakpoolsel paanil välja **Töökäsu tüüp** väärtuseks *Sorditud varude komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="c2ffd-327">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c2ffd-328">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-329">**Järjestus:** *2*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="c2ffd-330">**Nimi:** *Mitmik-Baydoor*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="c2ffd-331">Määrake kiirkaardil **Asukohakorraldused** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-332">**Töö tüüp:** *Ladustamine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="c2ffd-333">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-333">**Site:** *6*</span></span>
    - <span data-ttu-id="c2ffd-334">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="c2ffd-335">**Mitu SKU-d:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="c2ffd-336">Valige **Salvesta**, et muuta tööriistariba kiirkaardil **Read** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="c2ffd-337">Valige kiirkaardil **Read** suvand **Uus** ja seejärel seadke uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-337">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="c2ffd-338">Võtke vastu kõigi teiste väljade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="c2ffd-339">**Järjestus:** *1*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="c2ffd-340">**Alates:** *0*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-340">**From:** *0*</span></span>
    - <span data-ttu-id="c2ffd-341">**Kuni:** *1 000 000*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="c2ffd-342">Valige **Salvesta**, et muuta tööriistariba kiirkaardil **Asukohakorralduse toimingud** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="c2ffd-343">Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus** ja seejärel seadke uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-343">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="c2ffd-344">Võtke vastu kõigi teiste väljade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="c2ffd-345">**Järjestus:** *1*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="c2ffd-346">**Nimi:** *Mitmik-Baydoor*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="c2ffd-347">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-347">Select **Save**.</span></span>
1. <span data-ttu-id="c2ffd-348">Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="c2ffd-349">Otsige päringuredaktori vahekaardil **Vahemik** üles rida, kus välja **Väli** väärtuseks on seatud *Asukoht*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="c2ffd-350">Määrake selle rea välja **Kriteeriumid** väärtuseks *Baydoor*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="c2ffd-351">Oma sätete salvestamiseks ja päringuredaktori sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="c2ffd-352">Töömallide häälestamine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-352">Set up work templates</span></span>

1. <span data-ttu-id="c2ffd-353">Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="c2ffd-354">Muutke välja **Töökäsu tüüp** väärtuseks *Sorditud varude komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="c2ffd-355">Töömalli loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="c2ffd-356">Vahekaardil **Ülevaade** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-357">**Järjestus:** *1*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="c2ffd-358">**Töömall:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="c2ffd-359">**Töömalli kirjeldus:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="c2ffd-360">Valige **Salvesta**, et muuta kiirkaart **Töömalli üksikasjad** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="c2ffd-361">Valige kiirkaardil **Töömalli üksikasjad** suvand **Jah**, et lisada rida ja seejärel seadke sellele järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="c2ffd-362">**Töö tüüp:** *Komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="c2ffd-363">**Töö klassi ID:** *SORTIMINE*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="c2ffd-364">Valige uuesti **Uus**, et lisada teine rida ja seejärel seadke sellele järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="c2ffd-365">**Töö tüüp:** *Ladustamine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="c2ffd-366">**Töö klassi ID:** *SORTIMINE*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="c2ffd-367">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="c2ffd-368">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="c2ffd-368">Scenario</span></span>

<span data-ttu-id="c2ffd-369">See stsenaarium simuleerib olukorda, kus pakitud konteinerid tuleks pärast pakkimisjaama sorteerida automaatselt erinevatesse asukohtadesse (kaubaalustele), sõltuvalt saadetise vedaja teenusest.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="c2ffd-370">Kui kõik koormuse kõik kaubad on pakitud ja sorditud aadressi järgi, teisaldatakse kaubaalused laadimisukse juurde.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="c2ffd-371">Müügitellimuste ja komplekteerimistöö loomine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="c2ffd-372">Müügitellimuse 1 loomine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-372">Create sales order 1</span></span>

1. <span data-ttu-id="c2ffd-373">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="c2ffd-374">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c2ffd-375">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-376">**Kliendi konto:** *US-005*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="c2ffd-377">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="c2ffd-378">Valige dialoogiboksi sulgemiseks suvand **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="c2ffd-379">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="c2ffd-380">Lülituge vaatele **Päis**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="c2ffd-381">Määrake kiirkaardi **Tarne** jaotises **Transport** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-382">**Vedaja:** *Kaubalennuk*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="c2ffd-383">**Vedaja teenus:** *Õhk*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="c2ffd-384">Minge vaatesse **Read**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="c2ffd-385">Kui uut rida ei lisata ruudustikku automaatselt, siis valige kiirkaardil **Müügitellimuse read** suvand **Lisa rida** selle lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="c2ffd-386">Määrake uuel tellimuse real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-387">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="c2ffd-388">**Kogus:** *2*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="c2ffd-389">Kui uus tellimuse rida on veel valitud, valige kiirkaardi **Müügitellimuse read** ruudustiku kohal olevas menüüs **Varud** suvand **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="c2ffd-390">Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="c2ffd-391">Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="c2ffd-392">Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="c2ffd-393">Saate teate, mis näitab saadetist ja voogu selle tellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="c2ffd-394">Märkige üles voo ID-kood ja saadetise ID-kood.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="c2ffd-395">Müügitellimus 2</span><span class="sxs-lookup"><span data-stu-id="c2ffd-395">Sales order 2</span></span>

1. <span data-ttu-id="c2ffd-396">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="c2ffd-397">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c2ffd-398">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-399">**Kliendi konto:** *US-006*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="c2ffd-400">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="c2ffd-401">Valige dialoogiboksi sulgemiseks suvand **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="c2ffd-402">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-402">The new sales order is opened.</span></span> <span data-ttu-id="c2ffd-403">See peaks sisaldama uut tühja rida kiirkaardi **Müügitellimuse read** ruudustikus.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="c2ffd-404">Määrake sellel tellimuse real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="c2ffd-405">**Kaup:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="c2ffd-406">**Kogus:** *1*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="c2ffd-407">Määrake kiirkaardi **Rea üksikasjad** vahekaardil **Tarne** välja **Tarneviis** väärtuseks *Flowe-STD*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="c2ffd-408">Valige kiirkaardil **Müügitellimuse read** suvand **Lisa rida** ja seejärel seadke teisel tellimuse real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-408">On the **Sales order lines** FastTab, select **Add line**, and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="c2ffd-409">**Kaup:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="c2ffd-410">**Kogus:** *1*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="c2ffd-411">Muutke kiirkaardi **Rea üksikasjad** vahekaardil **Tarne** välja **Tarneviis** väärtuseks *Air C-Air*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="c2ffd-412">Valige kiirkaardil **Müügitellimuse read** esimene tellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="c2ffd-413">Seejärel valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="c2ffd-414">Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="c2ffd-415">Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="c2ffd-416">Valige kiirkaardil **Müügitellimuse read** teine tellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="c2ffd-417">Seejärel valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="c2ffd-418">Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="c2ffd-419">Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="c2ffd-420">Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="c2ffd-421">Saate teate, mis näitab saadetist ja voogu selle tellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="c2ffd-422">Pange tähele, et loodi kaks voo ID-numbrit ja kaks saadetise ID-numbrit, üks iga tarneviisi tarneviisi jaoks müügitellimuse ridadel.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="c2ffd-423">Töö ID-de hankimine töö üksikasjadest</span><span class="sxs-lookup"><span data-stu-id="c2ffd-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="c2ffd-424">Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="c2ffd-425">Lehel kuvatakse müügitellimustest loodud töö ID-d.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="c2ffd-426">Kasutage enda loodud müügitellimuste voo ID-sid ja saadetise ID-sid, et leida iga voo ja saadetise töö ID.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="c2ffd-427">Märkige need töö ID-d üles, sest vajate neid järgmistes etappides.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="c2ffd-428">Pange tähele, et teise müügitellimuse jaoks loodi kaks töö ID-d.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="c2ffd-429">Kui erinevatest asukohtadest komplekteeritakse erinevaid kaupasid, luuakse eraldi töö ID-d.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="c2ffd-430">Kaupade komplekteerimine müügitellimustesse</span><span class="sxs-lookup"><span data-stu-id="c2ffd-430">Pick items for the sales orders</span></span>

<span data-ttu-id="c2ffd-431">Viige loodud töö lõpule, kasutades mobiilset seadet kaupade teisaldamiseks pakkimisjaama.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="c2ffd-432">Logige mobiilses seadmes sisse lattu *62*, kasutades selleks stsenaariumi jaoks loodud kasutaja ID-d (või olemasoleva demoandmete kasutaja ID-d).</span><span class="sxs-lookup"><span data-stu-id="c2ffd-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="c2ffd-433">Valige peamenüüs suvand **Väljaminev**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="c2ffd-434">Valige menüüs **Väljaminev** suvand **Müügi komplekteerimine**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="c2ffd-435">Sisestage väljale **ID** müügitellimuse 1 jaoks loodud töö ID.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="c2ffd-436">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-436">Select **OK**.</span></span>
1. <span data-ttu-id="c2ffd-437">Sisestage lehel **Müügitellimused – komplekteerimine** siht-LP, mis loodi müügitellimuse 1 jaoks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="c2ffd-438">Pange tähele, et kuvatakse komplekteerimise asukoht (*hulgi-001*), kaup (*A0001*) ja kogus (*2 tk*).</span><span class="sxs-lookup"><span data-stu-id="c2ffd-438">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*2 pcs*) are shown.</span></span>
1. <span data-ttu-id="c2ffd-439">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-439">Select **OK**.</span></span>
1. <span data-ttu-id="c2ffd-440">Vaadake üle teave lehel **Ostutellimused – sisestatud**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="c2ffd-441">Väli **Loc** peaks näitama, et komplekteeritud kaubad lähevad asukohta *Pakkimine*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="c2ffd-442">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-442">Select **OK**.</span></span>

    <span data-ttu-id="c2ffd-443">Lehel **Skanni töö ID / identifitseerimisnumbri ID** teade „Töö lõpule viidud”, mis näitab, et töö ID müügitellimusest 1 on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="c2ffd-444">Nüüd saate komplekteerida müügitellimuse 2.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="c2ffd-445">Sisestage väljale **ID** töö ID, mis loodi müügitellimuse 2 jaoks, kus real 1 on kaup *A0001*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="c2ffd-446">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-446">Select **OK**.</span></span>
1. <span data-ttu-id="c2ffd-447">Sisestage lehele **Müügitellimused – komplekteerimine** siht-LP.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="c2ffd-448">Pange tähele, et kuvatakse komplekteerimise asukoht (*hulgi-001*), kaup (*A0001*) ja kogus (*1 tk*).</span><span class="sxs-lookup"><span data-stu-id="c2ffd-448">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="c2ffd-449">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-449">Select **OK**.</span></span>
1. <span data-ttu-id="c2ffd-450">Vaadake üle teave lehel **Ostutellimused – sisestatud**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="c2ffd-451">Väli **Loc** peaks näitama, et komplekteeritud kaubad lähevad asukohta *Pakkimine*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="c2ffd-452">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-452">Select **OK**.</span></span>

    <span data-ttu-id="c2ffd-453">Lehel **Skanni töö ID / identifitseerimisnumbri ID** teade „Töö lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="c2ffd-454">See teade näitab, et müügitellimuse 2 rea 1 töö ID on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="c2ffd-455">Sisestage väljale **ID** töö ID, mis loodi müügitellimuse 2 jaoks, kus real 2 on kaup *A0002*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="c2ffd-456">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-456">Select **OK**.</span></span>
1. <span data-ttu-id="c2ffd-457">Sisestage lehele **Müügitellimused – komplekteerimine** siht-LP.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="c2ffd-458">Pange tähele, et kuvatakse komplekteerimise asukoht (*hulgi-002*), kaup (*A0001*) ja kogus (*1 tk*).</span><span class="sxs-lookup"><span data-stu-id="c2ffd-458">Notice that the picking location (*bulk-002*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="c2ffd-459">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-459">Select **OK**.</span></span>
1. <span data-ttu-id="c2ffd-460">Vaadake üle teave lehel **Ostutellimused – sisestatud**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="c2ffd-461">Väli **Loc** peaks näitama, et komplekteeritud kaubad lähevad asukohta *Pakkimine*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="c2ffd-462">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-462">Select **OK**.</span></span>

    <span data-ttu-id="c2ffd-463">Lehel **Skanni töö ID / identifitseerimisnumbri ID** teade „Töö lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="c2ffd-464">See teade näitab, et müügitellimuse 2 rea 2 töö ID on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="c2ffd-465">Müügitellimuste pakkimine konteineritesse</span><span class="sxs-lookup"><span data-stu-id="c2ffd-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="c2ffd-466">Müügitellimuse 1 pakkimine konteineritesse</span><span class="sxs-lookup"><span data-stu-id="c2ffd-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="c2ffd-467">Avage jaotis **Laohaldus \> Pakkimine ja konteinerisse paigutamine \> Pakkimine**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="c2ffd-468">Kuvatavas dialoogiboks **Pakkimisjaama valimine**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="c2ffd-469">Vaikimisi peaks olema väljal **Töötaja** töötaja nimi, mille seadistasite eelnevalt.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="c2ffd-470">Määrake järgmised väärtused kindlas pakkimisasukohas plaanitud saadetiste ja konteinerite kuvamiseks ja nendega töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="c2ffd-471">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-471">**Site:** *6*</span></span>
    - <span data-ttu-id="c2ffd-472">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="c2ffd-473">**Asukoht:** *Pakkimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="c2ffd-474">**Pakkimisprofiili ID:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="c2ffd-475">Valige dialoogiboksi sulgemiseks suvand **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="c2ffd-476">Sisestage lehe **Pakkimine** väljale **Identifitseerimisnumber** müügitellimuse 1 siht-LP.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="c2ffd-477">Seejärel valige **Vahekaart** või vajutage klaviatuuril **Sisestusklahvi (Enter)** väljalt väljumiseks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="c2ffd-478">Valige toimingupaanil nupp **Uus konteiner**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="c2ffd-479">Nõustuge kõigi vaikesätetega ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="c2ffd-480">Märkige üles konteineri ID.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="c2ffd-481">Määrake kiirkaardil **Kauba pakkimine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-482">**Kogus:** *1*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="c2ffd-483">**Identifikaator:** kaup *A0001*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="c2ffd-484">Valige toimingupaanil nupp **Sule konteiner**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="c2ffd-485">Valige dialoogiboksis **Sule konteiner** suvand **Süsteemi kaalu toomine**, et süsteem värskendaks välja **Brutokaal**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="c2ffd-486">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-486">Select **OK**.</span></span> <span data-ttu-id="c2ffd-487">Konteiner teisaldatakse asukohta *SORTIMINE* ja on sortimiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="c2ffd-488">Looge teine konteiner, et lisada teine kaup müügitellimuse 1 LP-st uude konteinerisse.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="c2ffd-489">Valige toimingupaanil nupp **Uus konteiner**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="c2ffd-490">Nõustuge kõigi vaikesätetega ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="c2ffd-491">Märkige üles konteineri ID.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="c2ffd-492">Määrake kiirkaardil **Kauba pakkimine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-493">**Kogus:** *1*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="c2ffd-494">**Identifikaator:** kaup *A0001*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="c2ffd-495">Valige toimingupaanil nupp **Sule konteiner**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="c2ffd-496">Valige dialoogiboksis **Sule konteiner** suvand **Süsteemi kaalu toomine**, et süsteem värskendaks välja **Brutokaal**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="c2ffd-497">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-497">Select **OK**.</span></span> <span data-ttu-id="c2ffd-498">Konteiner teisaldatakse asukohta *SORTIMINE* ja on sortimiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="c2ffd-499">Müügitellimuse 2 pakkimine konteineritesse</span><span class="sxs-lookup"><span data-stu-id="c2ffd-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="c2ffd-500">Sisestage lehe **Pakkimine** väljale **Identifitseerimisnumber** siht-LP müügitellimuse 2 rea 1 jaoks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="c2ffd-501">Seejärel valige **Vahekaart** või vajutage klaviatuuril **Sisestusklahvi (Enter)** väljalt väljumiseks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="c2ffd-502">Valige toimingupaanil nupp **Uus konteiner**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="c2ffd-503">Nõustuge kõigi vaikesätetega ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="c2ffd-504">Märkige üles konteineri ID.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="c2ffd-505">Määrake kiirkaardil **Kauba pakkimine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-506">**Kogus:** *1*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="c2ffd-507">**Identifikaator:** kaup *A0001*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="c2ffd-508">Valige toimingupaanil nupp **Sule konteiner**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="c2ffd-509">Valige dialoogiboksis **Sule konteiner** suvand **Süsteemi kaalu toomine**, et süsteem värskendaks välja **Brutokaal**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="c2ffd-510">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-510">Select **OK**.</span></span> <span data-ttu-id="c2ffd-511">Konteiner teisaldatakse asukohta *SORTIMINE* ja on sortimiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="c2ffd-512">Sisestage väljale **Identifitseerimisnumber või saadetis** siht-LP müügitellimuse 2 rea 2 jaoks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="c2ffd-513">Seejärel valige **Vahekaart** või vajutage klaviatuuril **Sisestusklahvi (Enter)** väljalt väljumiseks.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="c2ffd-514">Valige toimingupaanil nupp **Uus konteiner**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="c2ffd-515">Nõustuge kõigi vaikesätetega ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="c2ffd-516">Märkige üles konteineri ID.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="c2ffd-517">Määrake kiirkaardil **Kauba pakkimine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c2ffd-518">**Kogus:** *1*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="c2ffd-519">**Identifikaatori väli:** kaup *A0002*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="c2ffd-520">Valige toimingupaanil nupp **Sule konteiner**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="c2ffd-521">Valige dialoogiboksis **Sule konteiner** suvand **Süsteemi kaalu toomine**, et süsteem värskendaks välja **Brutokaal**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="c2ffd-522">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-522">Select **OK**.</span></span> <span data-ttu-id="c2ffd-523">Konteiner teisaldatakse asukohta *SORTIMINE* ja on sortimiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="c2ffd-524">Konteineri üksikasjade kuvamiseks avage jaotis **Laohaldus \> Pakkimine ja konteinerisse määramine \> Konteinerid** ja otsige pakkimise ajal loodud konteineri ID-sid.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers**, and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="c2ffd-525">Konteinerite sortimine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2ffd-526">Kui avate mobiilirakenduses menüü-üksuse **Kaubaaluse loomine**, et teha väljamineku sortimist, kuvatakse nupp, mille märgistus on **Täielik**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="c2ffd-527">*Ärge kasutage nuppu **Täielik** asukoha sortimiseks või sulgemiseks.*</span><span class="sxs-lookup"><span data-stu-id="c2ffd-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="c2ffd-528">Nupp **Täielik** on vaikimisi saadaval ja seda ei saa lehelt keelata ega eemaldada.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="c2ffd-529">Seda ei kasutata funktsiooni *Väljamineku sortimine*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="c2ffd-530">Esimese konteineri sortimine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-530">Sort the first container</span></span>

1. <span data-ttu-id="c2ffd-531">Logige mobiilses seadmes sisse lattu *62*, kasutades selleks stsenaariumi jaoks loodud kasutaja ID-d (või olemasoleva demoandmete kasutaja ID-d).</span><span class="sxs-lookup"><span data-stu-id="c2ffd-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="c2ffd-532">Valige peamenüüs suvand **Väljaminev**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="c2ffd-533">Valige menüüs **Väljaminev** suvand **Kaubaaluse loomine**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="c2ffd-534">Sisestage väljale **LP/Con** esimese konteineri ID, mis on seostatud müügitellimusega 1.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="c2ffd-535">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-535">Select **OK**.</span></span>
1. <span data-ttu-id="c2ffd-536">Kuna ühtegi sortimise asukohta pole praegu olemas, peate selle määrama.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="c2ffd-537">Sisestage väljale **Sortimise asukoha ID** väärtus *SP01*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="c2ffd-538">Kuna ükski LP pole praegu seotud asukohaga *SP01*, peate selle määrama.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-538">Because no LP is currently associated with sort position *SP01*, you must specify one.</span></span> <span data-ttu-id="c2ffd-539">Sisestage väljale **LP** väärtus *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="c2ffd-540">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-540">Select **OK**.</span></span>
1. <span data-ttu-id="c2ffd-541">Kuna sortimise asukoha kinnitamine on sisse lülitatud, peate sisestama sortimise asukoha ID uuesti.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="c2ffd-542">Sisestage väljale **Sortimise asukoha ID** väärtus *SP01*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="c2ffd-543">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-543">Select **OK**.</span></span>

    <span data-ttu-id="c2ffd-544">Teile kuvatakse teade „Töö lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="c2ffd-545">Sortimise asukoha ja selles oleva LP kuvamiseks avage jaotis **Laohaldus \> Pakkimine ja konteinerisse määramine \> Väljamineku sortimise asukoha määramised**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="c2ffd-546">Lehel **Väljamineku sortimise asukoha määramised** kuvatakse kõik praegu aktiivsed sortimise asukohad.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="c2ffd-547">Väljal **Sortimise asukoha kanded** kuvatakse LP, mis on seostatud iga sortimise asukohaga ja selles asukohas olevad konteinerid.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="c2ffd-548">Pange tähele, et üks sortimise asukoht on praegu olemas ja kiirkaardil **Sortimise asukoha kriteeriumid** kuvatakse kriteerium **Saadetis – vedaja teenus – õhk**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="c2ffd-549">Järelejäänud konteinerite sortimine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="c2ffd-550">Logige mobiilses seadmes sisse lattu *62*, kasutades selleks stsenaariumi jaoks loodud kasutaja ID-d (või olemasoleva demoandmete kasutaja ID-d).</span><span class="sxs-lookup"><span data-stu-id="c2ffd-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="c2ffd-551">Valige peamenüüs suvand **Väljaminev**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="c2ffd-552">Valige menüüs **Väljaminev** suvand **Kaubaaluse loomine**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="c2ffd-553">Sisestage väljale **LP/Con** teise konteineri ID, mis on seostatud müügitellimusega 1.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="c2ffd-554">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-554">Select **OK**.</span></span> <span data-ttu-id="c2ffd-555">Kuna sortimismall on seadistatud automaatselt sortima ja vastavate kriteeriumidega sortimise asukoht on juba olemas, suunatakse teid automaatselt õigesse sortimise asukohta.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="c2ffd-556">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-556">Select **OK**.</span></span>
1. <span data-ttu-id="c2ffd-557">Kinnitage sortimise asukoha ID, et näidata, et varud on õiges kohas.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="c2ffd-558">Sisestage väljale **Sortimise asukoha ID** väärtus *SP01*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="c2ffd-559">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-559">Select **OK**.</span></span>

    <span data-ttu-id="c2ffd-560">Töö müügitellimuse 1 teise konteineriga on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="c2ffd-561">Nüüd saate sortida müügitellimuse 2 ülejäänud konteinerid.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="c2ffd-562">Sisestage väljale **LP/Con** müügitellimuse 2 konteineri ID, milles on kaup *A0001*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="c2ffd-563">Kuna vedaja teenus on erinev, palutakse teil sisestada uus sortimise asukoht ja määrata sellele asukohale LP.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="c2ffd-564">Kasutage sortimise asukohta *SP02* ja LP-d *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="c2ffd-565">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-565">Select **OK**.</span></span>
1. <span data-ttu-id="c2ffd-566">Kinnitage sortimise asukoht, sisestades väljale **Sortimise asukoha ID** väärtuse *SP02*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="c2ffd-567">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-567">Select **OK**.</span></span>

    <span data-ttu-id="c2ffd-568">Töö konteineriga on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="c2ffd-569">Sisestage väljale **LP/Con** müügitellimuse 2 järelejäänud konteineri ID, milles on kaup *A0002*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="c2ffd-570">Kuna vedaja teenus ühtib müügitellimuse 1 vedaja teenusega, kuvab süsteem olemasoleva sortimise asukoha, millel on vastavad kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="c2ffd-571">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-571">Select **OK**.</span></span>
1. <span data-ttu-id="c2ffd-572">Kinnitage sortimise asukoht, sisestades väljale **Sortimise asukoha ID** väärtuse *SP01*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="c2ffd-573">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-573">Select **OK**.</span></span>

    <span data-ttu-id="c2ffd-574">Töö konteineriga on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="c2ffd-575">Väljamineku sortimise asukohtade sulgemine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="c2ffd-576">Kui kõik varud on sorditud, tuleb asukoht enne töö loomist sulgeda.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="c2ffd-577">Luuakse sorditud varude komplekteerimistöö, et teisaldada varud laadimisukse juurde.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="c2ffd-578">Asukoha sulgemine mobiilsest seadmest</span><span class="sxs-lookup"><span data-stu-id="c2ffd-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="c2ffd-579">Logige mobiilses seadmes sisse lattu *62*, kasutades selleks stsenaariumi jaoks loodud kasutaja ID-d (või olemasoleva demoandmete kasutaja ID-d).</span><span class="sxs-lookup"><span data-stu-id="c2ffd-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="c2ffd-580">Valige peamenüüs suvand **Väljaminev**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="c2ffd-581">Valige menüüs **Väljaminev** suvand **Kaubaaluse loomine**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="c2ffd-582">Sisestage väljale **LP/Con** konteineri ID, mis sorditi sortimise asukohta *SP01*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="c2ffd-583">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-583">Select **OK**.</span></span>
1. <span data-ttu-id="c2ffd-584">Teile kuvatakse järgmine teade: „Konteiner on juba sorditud asukohta SP01.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="c2ffd-585">Kas soovite selle asukoha sulgeda?”</span><span class="sxs-lookup"><span data-stu-id="c2ffd-585">Close the position?"</span></span> <span data-ttu-id="c2ffd-586">Valige suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-586">Select **Close**.</span></span>

    <span data-ttu-id="c2ffd-587">Töö on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="c2ffd-588">Asukoha sulgemine väljamineku sortimise asukoha määramistest</span><span class="sxs-lookup"><span data-stu-id="c2ffd-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="c2ffd-589">Avage jaotis **Laohaldus \> Pakkimine ja konteinerisse määramine \> Väljamineku sortimise asukoha määramised**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="c2ffd-590">Valige vasakust veerust **SP02**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="c2ffd-591">See väljamineku sortimise asukoha rida on see, mille sulgete.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="c2ffd-592">Valige toimingupaanil nupp **Sule asukoht**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="c2ffd-593">Sortimise asukoha kirje on suletud ja seda enam ei kuvata.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="c2ffd-594">Kõigi suletud asukoha kirjete kuvamiseks märkige ruut **Kuva suletud**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="c2ffd-595">Sorditud varude komplekteerimine</span><span class="sxs-lookup"><span data-stu-id="c2ffd-595">Sorted inventory picking</span></span>

<span data-ttu-id="c2ffd-596">Peate viima lõpule sorditud varude komplekteerimistöö.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="c2ffd-597">Kui see on lõpule viidud, komplekteeritakse varud müügitellimusele.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="c2ffd-598">Seejärel kehtivad kõik muud laoprotsessid.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="c2ffd-599">Logige mobiilses seadmes sisse lattu *62*, kasutades selleks stsenaariumi jaoks loodud kasutaja ID-d (või olemasoleva demoandmete kasutaja ID-d).</span><span class="sxs-lookup"><span data-stu-id="c2ffd-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="c2ffd-600">Valige peamenüüs suvand **Väljaminev**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="c2ffd-601">Valige menüüs **Väljaminek** suvand **Laadi sortimisest**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="c2ffd-602">Sisestage esimese sortimise asukoha siht-LP ID *SP01*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="c2ffd-603">Määrake välja **ID** väärtuseks *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="c2ffd-604">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-604">Select **OK**.</span></span>
1. <span data-ttu-id="c2ffd-605">Lehel **Sorditud varude komplekteerimine: komplekteerimine** kuvatakse komplekteerimistöö, mida tuleb teha.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="c2ffd-606">Komplekteerige askohast *SORTIMINE* ja siht-LP-st *PLP01*, millel on mitu kaupa ja kogus *3*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-606">Pick from the *SORT* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="c2ffd-607">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-607">Select **OK**.</span></span>
1. <span data-ttu-id="c2ffd-608">Lehel **Sorditud varude komplekteerimine: sisestatud** kuvatakse sisestamistöö, mida tuleb teha.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="c2ffd-609">Sisestage askohta *Baydoor* ja siht-LP *PLP01*, millel on mitu kaupa ja kogus *3*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-609">Put to the *Baydoor* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="c2ffd-610">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-610">Select **OK**.</span></span>

    <span data-ttu-id="c2ffd-611">Töö on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-611">Work is completed.</span></span>

1. <span data-ttu-id="c2ffd-612">Sisestage teise sortimise asukoha identifitseerimisnumbri ID *SP02*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="c2ffd-613">Määrake välja **ID** väärtuseks *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="c2ffd-614">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-614">Select **OK**.</span></span>
1. <span data-ttu-id="c2ffd-615">Lehel **Sorditud varude komplekteerimine: komplekteerimine** kuvatakse komplekteerimistöö, mida tuleb teha.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="c2ffd-616">Komplekteerige askohast *SORTIMINE* ja siht-LP-st *PLP02*, millel on mitu kaupa ja kogus *1*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-616">Pick from the *SORT* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="c2ffd-617">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-617">Select **OK**.</span></span>
1. <span data-ttu-id="c2ffd-618">Lehel **Sorditud varude komplekteerimine: sisestatud** kuvatakse sisestamistöö, mida tuleb teha.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="c2ffd-619">Sisestage askohta *Baydoor* ja siht-LP *PLP02*, millel on mitu kaupa ja kogus *1*.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-619">Put to the *Baydoor* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="c2ffd-620">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-620">Select **OK**.</span></span>

    <span data-ttu-id="c2ffd-621">Töö on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-621">Work is completed.</span></span>

<span data-ttu-id="c2ffd-622">Sellest alates kehtivad kõik muud laoprotsessid.</span><span class="sxs-lookup"><span data-stu-id="c2ffd-622">From this point forward, all other warehouse processes apply.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]