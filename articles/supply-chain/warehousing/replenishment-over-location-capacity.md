---
title: Täiendamine üle asukoha võimsuse
description: Selles teemas antakse teavet funktsiooni Täiendamine üle asukoha võimsuse kohta. See funktsioon võimaldab kogu päevast loodavat täiendamistööd ja selle abil saab hallata selle täiendustöö kättesaadavust, tagamaks, et komplekteerimise asukoht jääks varudeta ega ületaks võimsust.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 309df56671bf258e1669ae6d5393de01e2b500f0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823235"
---
# <a name="replenishment-over-location-capacity"></a><span data-ttu-id="36f3f-104">Täiendamine üle asukoha võimsuse</span><span class="sxs-lookup"><span data-stu-id="36f3f-104">Replenishment over location capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36f3f-105">Mõned suurte mahtudega piiratud ruumiga laod peavad lähetama suuremaid kaubakoguseid, kui need mahuvad nende komplekteerimisasukohta.</span><span class="sxs-lookup"><span data-stu-id="36f3f-105">Some high-volume or space-constrained warehouses must ship more quantity of an item in a day than will fit in the picking location.</span></span> <span data-ttu-id="36f3f-106">Funktsioon *Täiendamine üle asukoha võimsuse* võimaldab kogu päevast loodavat täiendamistööd ja selle abil saab hallata selle täiendustöö kättesaadavust, tagamaks, et komplekteerimise asukoht jääks varudeta ega ületaks võimsust.</span><span class="sxs-lookup"><span data-stu-id="36f3f-106">The *Replenishment over location capacity* feature enables all replenishment work that will be required for the day to be created and manages availability of that replenishment work to ensure that the picking location neither runs out of inventory nor goes above capacity.</span></span>

<span data-ttu-id="36f3f-107">Funktsioon võimaldab luua rohkem täiendustöid, kui mahub asukohta ja see blokeerib täiendustööde lõpuleviimise, kui asukoht on täis.</span><span class="sxs-lookup"><span data-stu-id="36f3f-107">The feature enables more replenishment work to be created than will fit in a location, and it blocks replenishment work from being completed when the location is full.</span></span> <span data-ttu-id="36f3f-108">Kuna komplekteerimisasukoha varud langevad alla konfigureeritava läve, muutub rohkem täiendustööd kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="36f3f-108">As inventory in the picking location drops below a configurable threshold, more replenishment work is made available.</span></span>

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a><span data-ttu-id="36f3f-109">Funktsiooni Täiendamine üle asukoha võimsuse sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="36f3f-109">Turn on the Replenishment over location capacity feature</span></span>

<span data-ttu-id="36f3f-110">Selle funktsiooni kättesaadavaks muutmiseks lülitage [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse järgmised funktsioonid (vastavas järjekorras).</span><span class="sxs-lookup"><span data-stu-id="36f3f-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in this order):</span></span>

1. <span data-ttu-id="36f3f-111">Organisatsiooniülene töö blokeerimine</span><span class="sxs-lookup"><span data-stu-id="36f3f-111">Organization-wide work blocking</span></span>
1. <span data-ttu-id="36f3f-112">Täiendamine üle asukoha võimsuse</span><span class="sxs-lookup"><span data-stu-id="36f3f-112">Replenishment over location capacity</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="36f3f-113">Funktsiooni häälestamine näidisstsenaariumi jaoks</span><span class="sxs-lookup"><span data-stu-id="36f3f-113">Set up the feature for the example scenario</span></span>

<span data-ttu-id="36f3f-114">Sellest jaotisest leiate juhised ja näite selle funktsiooni häälestamise ning näidisandmete ettevalmistamise kohta teemas hiljem esitatud näidisstsenaariumi jaoks.</span><span class="sxs-lookup"><span data-stu-id="36f3f-114">This section provides guidelines and an example that shows how to set up this feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="enable-sample-data"></a><span data-ttu-id="36f3f-115">Luba näidisandmed</span><span class="sxs-lookup"><span data-stu-id="36f3f-115">Enable sample data</span></span>

<span data-ttu-id="36f3f-116">Selle [näidisstsenaariumi](#example-scenario) kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="36f3f-116">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="36f3f-117">Enne alustamist peate valima ka juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-117">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="location-profile"></a><span data-ttu-id="36f3f-118">Asukohaprofiil</span><span class="sxs-lookup"><span data-stu-id="36f3f-118">Location profile</span></span>

<span data-ttu-id="36f3f-119">Lubage täiendamine üle võimsuse funktsioon asukohaprofiilis.</span><span class="sxs-lookup"><span data-stu-id="36f3f-119">Enable the replenish over capacity functionality on the location profile.</span></span>

1. <span data-ttu-id="36f3f-120">Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukohtade profiilid**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-120">Go to **Warehouse management \> Setup \> Warehouse \> Locations profiles**.</span></span>
1. <span data-ttu-id="36f3f-121">Valige vasakpoolselt paanilt **PICK-06**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-121">In the left pane, select **PICK-06**.</span></span>
1. <span data-ttu-id="36f3f-122">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-122">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="36f3f-123">Määrake kiirkaardil **Täiendamine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36f3f-123">On the **Replenishment** FastTab, set the following values:</span></span>

    - <span data-ttu-id="36f3f-124">**Ületa asukoha võimsus:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="36f3f-124">**Exceed Location Capacity:** *Yes*</span></span>

        <span data-ttu-id="36f3f-125">Kui see on lubatud, lubatakse täiendustööl asukoha maksimaalset võimsust ületada.</span><span class="sxs-lookup"><span data-stu-id="36f3f-125">When enabled, the maximum capacity of the location will be allowed to be exceeded by replenishment work.</span></span> <span data-ttu-id="36f3f-126">See võimaldab ka muud väljad kiirkaardil **Täiendamine**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-126">This also enables other fields on the **Replenishment** FastTab.</span></span>

    - <span data-ttu-id="36f3f-127">**Töö kättesaadavusläve tüüp:** *Kogus*</span><span class="sxs-lookup"><span data-stu-id="36f3f-127">**Work availability threshold type:** *Quantity*</span></span>

        <span data-ttu-id="36f3f-128">See väli määratleb meetodi, mida kasutatakse, kui rohkem tööd tuleb vabastada.</span><span class="sxs-lookup"><span data-stu-id="36f3f-128">This field defines the method that is used to determine when more work should be released.</span></span> <span data-ttu-id="36f3f-129">Saate vabastada kas koguse või protsendi järgi.</span><span class="sxs-lookup"><span data-stu-id="36f3f-129">You can release by either quantity or a percentage:</span></span>

        - <span data-ttu-id="36f3f-130">*Protsent* – Valige see suvand, et kasutada protsentuaalset võimsust, mille aluseks on ladustamispiirangud või mahud.</span><span class="sxs-lookup"><span data-stu-id="36f3f-130">*Percent* – Select this option to use percentage capacity that is based on stocking limits or volumetrics.</span></span> <span data-ttu-id="36f3f-131">Selle suvandi valimine lubab välja **Ületäitumise protsent** ja keelab kaks kogusega seotud välja, **Ületäitumise kogus** ja **Ületäitumise ühik**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-131">Selecting this option enables the **Overflow percentage** field, and disables the two quantity related fields,  **Overflow quantity** and **Overflow unit**.</span></span>

            <span data-ttu-id="36f3f-132">Seda valikut saate kasutada siis, kui komplekteerimisasukohad kasutavad mahtu.</span><span class="sxs-lookup"><span data-stu-id="36f3f-132">You can use this option if the picking locations use volumetrics.</span></span>

            <span data-ttu-id="36f3f-133">Kui see suvand on valitud, määrake väli **Ületäitumise protsent** protsendini, milleni täiendustöö tehakse kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="36f3f-133">If this option is selected, set the **Overflow percentage** field to the percentage at which more replenishment work will be made available.</span></span>

        - <span data-ttu-id="36f3f-134">*Kogus* – Valige see suvand kindla koguse väärtuse kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="36f3f-134">*Quantity* – Select this option to use a specific quantity value.</span></span> <span data-ttu-id="36f3f-135">Selle suvandi valimine keelab välja **Ületäitumise protsent** ja lubab väljad **Ületäitumise kogus** ja **Ületäitumise ühik**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-135">Selecting this option disables the **Overflow percentage** field and enables **Overflow quantity** and **Overflow unit** fields.</span></span>

            <span data-ttu-id="36f3f-136">Kasutage seda suvandit, kui te ei kasuta täiendatavate asukohtade jaoks mahtu või kui teil on püsikogused, millele soovite asukohta rohkem varusid tuua.</span><span class="sxs-lookup"><span data-stu-id="36f3f-136">Use this option when you aren't using volumetrics for the locations that are being replenished, or when you have consistent quantities at which you want more inventory to be brought to the location.</span></span>

           <span data-ttu-id="36f3f-137">Kui see suvand on valitud, määrake väljad **Ületäitumise kogus** ja **Ületäitumise ühik** kogusele ja ühikule, mille juures tehakse rohkem täiendustööd kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="36f3f-137">If this option is selected, set the **Overflow quantity** and **Overflow unit** fields to the quantity and unit at which more replenishment work will be made available.</span></span>

    - <span data-ttu-id="36f3f-138">**Ületäitumise kogus:** *0,65*</span><span class="sxs-lookup"><span data-stu-id="36f3f-138">**Overflow quantity:** *0.65*</span></span>

        <span data-ttu-id="36f3f-139">See väli määratleb koguse, mille juures asukoht täitub üle.</span><span class="sxs-lookup"><span data-stu-id="36f3f-139">This field defines the quantity at which the location overflows.</span></span>

        <span data-ttu-id="36f3f-140">Töö on saadaval alati, kui asukoha laoseisu ja töö kogus jääb sellest väärtusest allapoole.</span><span class="sxs-lookup"><span data-stu-id="36f3f-140">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this value.</span></span> <span data-ttu-id="36f3f-141">Kõik sellest väärtusest suuremad täiendustööd blokeeritakse ja blokeerimine tuleb tühistada käsitsi.</span><span class="sxs-lookup"><span data-stu-id="36f3f-141">Any replenishment work above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="36f3f-142">Asukoha ladustamispiirangud võetakse arvesse töökoguse arvutamisel.</span><span class="sxs-lookup"><span data-stu-id="36f3f-142">Location stocking limits are considered when the work quantity is calculated.</span></span>

    - <span data-ttu-id="36f3f-143">**Ületäitumise ühik:** *PL*</span><span class="sxs-lookup"><span data-stu-id="36f3f-143">**Overflow unit:** *PL*</span></span>

        <span data-ttu-id="36f3f-144">See väli määratleb ületäitumise kogused seostatud ühiku.</span><span class="sxs-lookup"><span data-stu-id="36f3f-144">This field defines the unit that is associated with the overflow quantity.</span></span>

        <span data-ttu-id="36f3f-145">Sel juhul tehakse rohkem täiendustööd kättesaadavaks, kui asukoht jõuab 0,65 kaubaaluseni (PL).</span><span class="sxs-lookup"><span data-stu-id="36f3f-145">In this case, more replenishment work will be made available when the location gets down to 0.65 pallet (PL).</span></span>

    - <span data-ttu-id="36f3f-146">**Ületäitumise protsent**</span><span class="sxs-lookup"><span data-stu-id="36f3f-146">**Overflow percentage**</span></span>

        <span data-ttu-id="36f3f-147">See väli määratleb protsendi, mille juures asukoht täitub üle.</span><span class="sxs-lookup"><span data-stu-id="36f3f-147">This field defines the percentage at which the location overflows.</span></span>

        <span data-ttu-id="36f3f-148">Töö on saadaval alati, kui asukoha laoseisu ja töö kogus jääb sellest protsendist allapoole.</span><span class="sxs-lookup"><span data-stu-id="36f3f-148">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this percentage.</span></span> <span data-ttu-id="36f3f-149">Kõik sellest väärtusest suuremad täiendustöö koguse protsendid blokeeritakse ja blokeerimine tuleb tühistada käsitsi.</span><span class="sxs-lookup"><span data-stu-id="36f3f-149">Any replenishment work quantity percentage above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="36f3f-150">Asukoha ladustamispiirangud võetakse arvesse töökoguse protsendi arvutamisel.</span><span class="sxs-lookup"><span data-stu-id="36f3f-150">Location stocking limits are considered when the work quantity percentage is calculated.</span></span> <span data-ttu-id="36f3f-151">Kui asukoha ladustamispiiranguid pole määratletud, arvutatakse töö koguse protsent mahu järgi, kui asukohaprofiilis on määratletud mahupiirangud.</span><span class="sxs-lookup"><span data-stu-id="36f3f-151">If no location stocking limits are defined, the work quantity percentage is calculated by volume if volume constraints are defined for the location profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36f3f-152">Kui kasutate juriidilise isiku **USMF** demoandmeid ja eelnevalt lülitasite sisse funktsiooni *Asukoha identifitseerimisnumbri paigutus*, peate näidisstsenaariumi mobiilse seade etappides välja lülitama asukohaprofiili **BULK-06** sätte **Luba identifitseerimisnumbri paigutus**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-152">If you're using the demo data for the **USMF** legal entity and previously turned on the *Location license plate positioning* feature, you must turn off the **Enable license plate positioning** setting for the **BULK-06** location profile to complete the mobile steps in the example scenario.</span></span>

### <a name="wave-step-code"></a><span data-ttu-id="36f3f-153">Vooetapi kood</span><span class="sxs-lookup"><span data-stu-id="36f3f-153">Wave step code</span></span>

> [!NOTE]
> <span data-ttu-id="36f3f-154">Siin kirjeldatud vooetapi koodi häälestamiseks on võimalik, et peate funktsiooni nimega *Organisatsiooniülene voo etapi kood* sisselülitamiseks kasutama [funktsioonihaldust](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="36f3f-154">To set up a wave step code as described here, you might first have to use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named *Organization wide wave step code*.</span></span>

1. <span data-ttu-id="36f3f-155">Avage **Laohaldus \> Häälestamine \> Vood \> Vooetapi koodid**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-155">Go to **Warehouse Management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="36f3f-156">Valige **Uus** ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36f3f-156">Select **New**, and set the following values:</span></span>

    - <span data-ttu-id="36f3f-157">**Vooetapi kood:** *Täiend*</span><span class="sxs-lookup"><span data-stu-id="36f3f-157">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="36f3f-158">**Vooetapi kirjeldus:** *Täiendamine*</span><span class="sxs-lookup"><span data-stu-id="36f3f-158">**Wave step description:** *Replenishment*</span></span>
    - <span data-ttu-id="36f3f-159">**Vooetapi tüüp:** *Täiendamine*</span><span class="sxs-lookup"><span data-stu-id="36f3f-159">**Wave step type:** *Replenishment*</span></span>

1. <span data-ttu-id="36f3f-160">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-160">Select **Save**.</span></span>

### <a name="replenishment-template"></a><span data-ttu-id="36f3f-161">Täiendamise mall</span><span class="sxs-lookup"><span data-stu-id="36f3f-161">Replenishment template</span></span>

<span data-ttu-id="36f3f-162">Täiendamise mallid on reeglistik, mis määrab asikoha täiendamise aja ja viisi.</span><span class="sxs-lookup"><span data-stu-id="36f3f-162">Replenishment templates are a set of rules that control when and how a location is replenished.</span></span>

1. <span data-ttu-id="36f3f-163">Avage jaotis **Laohaldus \> Seadistus \> Täiendamine \> Täiendamismallid**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-163">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="36f3f-164">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-164">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="36f3f-165">Valige jaotises **Ülevaade** rida, mille välja **Täiendamismalli** väärtuseks on seatud *Nõudluse tõttu täiendamine*.</span><span class="sxs-lookup"><span data-stu-id="36f3f-165">In the **Overview** section, select the line where the **Replenish template** field is set to *Demand replenish*.</span></span>
1. <span data-ttu-id="36f3f-166">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36f3f-166">Set the following values:</span></span>

    - <span data-ttu-id="36f3f-167">**Vooetapi kood:** *Täiend*</span><span class="sxs-lookup"><span data-stu-id="36f3f-167">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="36f3f-168">**Luba voo nõudmisel kasutada reserveerimata koguseid:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="36f3f-168">**Allow wave demand to use unreserved quantities:** *Yes*</span></span>

1. <span data-ttu-id="36f3f-169">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-169">Select **Save**.</span></span>

### <a name="wave-template"></a><span data-ttu-id="36f3f-170">Voo mall</span><span class="sxs-lookup"><span data-stu-id="36f3f-170">Wave template</span></span>

1. <span data-ttu-id="36f3f-171">Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-171">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="36f3f-172">Määrake vasakpoolse paani välja **Voomalli tüüp** suvandiks *Lähetamine*.</span><span class="sxs-lookup"><span data-stu-id="36f3f-172">In the left pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="36f3f-173">Valige loendist mall **61 Lähetamine**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-173">Select template **61 Shipping** in the list.</span></span>
1. <span data-ttu-id="36f3f-174">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-174">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="36f3f-175">Seadke kiirkaardil **Üldine** suvandi **Automaatse täiendustöö vabastamine** väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="36f3f-175">On the **General** FastTab, set the **Automate replenishment work release** option to *Yes*.</span></span>

    <span data-ttu-id="36f3f-176">Valige selle suvandi väärtuseks *Jah* nõudlusel põhineva täiendustöö loomiseks ja selle automaatseks väljastamiseks.</span><span class="sxs-lookup"><span data-stu-id="36f3f-176">Set this option to *Yes* to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="36f3f-177">Selleks peab voomallile lisama täiendusvoo meetodi ja looma täiendamismalli tüübiga **Voo nõue**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-177">You must add the replenishment wave method to the wave template and create a replenishment template of the **Wave demand** type.</span></span> <span data-ttu-id="36f3f-178">Häälestage lehel **Täiendamise mall** täiendamise mall.</span><span class="sxs-lookup"><span data-stu-id="36f3f-178">Set up a replenishment template on the **Replenishment templates** page.</span></span> <span data-ttu-id="36f3f-179">Täiendamise malli häälestamiseks tuleb lisada voo mallile täiendamise meetod.</span><span class="sxs-lookup"><span data-stu-id="36f3f-179">To set up a replenishment template, you must add the replenish method to the wave template.</span></span>

1. <span data-ttu-id="36f3f-180">Otsige kiirkaardi **Meetodid** veerust **Valitud meetodid**, järgmine rida:</span><span class="sxs-lookup"><span data-stu-id="36f3f-180">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="36f3f-181">**Meetodi nimi:** *täiendamine*</span><span class="sxs-lookup"><span data-stu-id="36f3f-181">**Method name:** *replenish*</span></span>
    - <span data-ttu-id="36f3f-182">**Nimi:** *Täiendamine*</span><span class="sxs-lookup"><span data-stu-id="36f3f-182">**Name:** *Replenishment*</span></span>

1. <span data-ttu-id="36f3f-183">Seadke selle rea välja **Vooetapi kood** väärtuseks *Täiend*.</span><span class="sxs-lookup"><span data-stu-id="36f3f-183">Set the **Wave step code** field for this line to *Replen*.</span></span>
1. <span data-ttu-id="36f3f-184">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-184">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="36f3f-185">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="36f3f-185">Example scenario</span></span>

<span data-ttu-id="36f3f-186">Pärast seda, kui olete teinud kõik eelnevalt kirjeldatud näidisandmed kättesaadavaks ja need häälestanud, saate töötada selle stsenaariumi abil, et proovida funktsiooni *Täiendamine üle asukoha võimsuse*.</span><span class="sxs-lookup"><span data-stu-id="36f3f-186">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Replenishment over location capacity* feature.</span></span> <span data-ttu-id="36f3f-187">Selles stsenaariumis kuvatavad väärtused eeldavad, et töötate standardsete demo andmetega, et valisite juriidilise isiku **USMF** ja olete ette valmistanud näidiskirjed, mida on selles teemas varem kirjeldatud.</span><span class="sxs-lookup"><span data-stu-id="36f3f-187">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="36f3f-188">See stsenaarium toimib ka näitena selle kohta, kuidas seda funktsiooni saab tootmises kasutada.</span><span class="sxs-lookup"><span data-stu-id="36f3f-188">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-replenishment-work"></a><span data-ttu-id="36f3f-189">Täiendustöö loomine</span><span class="sxs-lookup"><span data-stu-id="36f3f-189">Create replenishment work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="36f3f-190">Müügitellimuse 1 loomine</span><span class="sxs-lookup"><span data-stu-id="36f3f-190">Create sales order 1</span></span>

1. <span data-ttu-id="36f3f-191">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-191">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="36f3f-192">Valige tegevuspaanil **Uus**, et avada dialoogiboks uue müügitellimuse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="36f3f-192">On the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="36f3f-193">Määrake dialoogiboksis järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36f3f-193">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="36f3f-194">**Kliendi konto:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="36f3f-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="36f3f-195">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="36f3f-195">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="36f3f-196">Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-196">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="36f3f-197">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="36f3f-197">The new sales order is opened.</span></span> <span data-ttu-id="36f3f-198">See lisab uue, tühja rea kiirkaardil **Müügitellimuse read**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-198">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="36f3f-199">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36f3f-199">On this line, set the following values:</span></span>

    - <span data-ttu-id="36f3f-200">**Kauba kood:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="36f3f-200">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="36f3f-201">**Kogus:** *40*</span><span class="sxs-lookup"><span data-stu-id="36f3f-201">**Quantity:** *40*</span></span>

1. <span data-ttu-id="36f3f-202">Tehke kiirkaardil **Müügitellimuse read** valik **Varud \> Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-202">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="36f3f-203">Valige tegevuspaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-203">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="36f3f-204">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="36f3f-204">Close the page.</span></span>
1. <span data-ttu-id="36f3f-205">Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-205">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="36f3f-206">Saate teabesõnumi, mis näitab loodud voo ja saadetise ID-d.</span><span class="sxs-lookup"><span data-stu-id="36f3f-206">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="36f3f-207">Luuakse ka täiendusvoog.</span><span class="sxs-lookup"><span data-stu-id="36f3f-207">A replenishment wave is also created.</span></span>

    <span data-ttu-id="36f3f-208">Saate ka hoiatusteate, mis ütleb: "Töö ID XXXX blokeeringut ei saa tühistada, kuna see on lõpuleviimata täiendustöö."</span><span class="sxs-lookup"><span data-stu-id="36f3f-208">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="36f3f-209">Müügitellimuse 2 loomine</span><span class="sxs-lookup"><span data-stu-id="36f3f-209">Create sales order 2</span></span>

1. <span data-ttu-id="36f3f-210">Tehke tegevuspaani lehel **Kõik müügitellimused** valik **Uus**, et avada dialoogiboks uue müügitellimuse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="36f3f-210">On the **All sales orders**, page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="36f3f-211">Määrake dialoogiboksis järgmine väärtus.</span><span class="sxs-lookup"><span data-stu-id="36f3f-211">In the dialog box, set the following value:</span></span>

    - <span data-ttu-id="36f3f-212">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="36f3f-212">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="36f3f-213">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="36f3f-213">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="36f3f-214">Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-214">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="36f3f-215">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="36f3f-215">The new sales order is opened.</span></span> <span data-ttu-id="36f3f-216">See lisab uue, tühja rea kiirkaardil **Müügitellimuse read**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-216">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="36f3f-217">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36f3f-217">On this line, set the following values:</span></span>

    - <span data-ttu-id="36f3f-218">**Kauba kood:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="36f3f-218">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="36f3f-219">**Kogus:** *60*</span><span class="sxs-lookup"><span data-stu-id="36f3f-219">**Quantity:** *60*</span></span>

1. <span data-ttu-id="36f3f-220">Tehke kiirkaardil **Müügitellimuse read** valik **Varud \> Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-220">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="36f3f-221">Valige tegevuspaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-221">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="36f3f-222">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="36f3f-222">Close the page.</span></span>
1. <span data-ttu-id="36f3f-223">Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-223">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="36f3f-224">Saate teabesõnumi, mis näitab loodud voo ja saadetise ID-d.</span><span class="sxs-lookup"><span data-stu-id="36f3f-224">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="36f3f-225">Luuakse ka täiendusvoog.</span><span class="sxs-lookup"><span data-stu-id="36f3f-225">A replenishment wave is also created.</span></span>

    <span data-ttu-id="36f3f-226">Saate ka hoiatusteate, mis ütleb: "Töö ID XXXX blokeeringut ei saa tühistada, kuna see on lõpuleviimata täiendustöö."</span><span class="sxs-lookup"><span data-stu-id="36f3f-226">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="36f3f-227">Müügitellimuse 3 loomine</span><span class="sxs-lookup"><span data-stu-id="36f3f-227">Create sales order 3</span></span>

1. <span data-ttu-id="36f3f-228">Tehke tegevuspaani lehel **Kõik müügitellimused** valik **Uus**, et avada dialoogiboks uue müügitellimuse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="36f3f-228">On the **All sales orders** page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="36f3f-229">Määrake dialoogiboksis järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36f3f-229">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="36f3f-230">**Kliendi konto:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="36f3f-230">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="36f3f-231">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="36f3f-231">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="36f3f-232">Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-232">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="36f3f-233">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="36f3f-233">The new sales order is opened.</span></span> <span data-ttu-id="36f3f-234">See lisab uue, tühja rea kiirkaardil **Müügitellimuse read**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-234">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="36f3f-235">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36f3f-235">On this line, set the following values:</span></span>

    - <span data-ttu-id="36f3f-236">**Kauba kood:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="36f3f-236">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="36f3f-237">**Kogus:** *30*</span><span class="sxs-lookup"><span data-stu-id="36f3f-237">**Quantity:** *30*</span></span>

1. <span data-ttu-id="36f3f-238">Tehke kiirkaardil **Müügitellimuse read** valik **Varud \> Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-238">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="36f3f-239">Valige tegevuspaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-239">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="36f3f-240">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="36f3f-240">Close the page.</span></span>
1. <span data-ttu-id="36f3f-241">Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-241">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="36f3f-242">Saate teabesõnumi, mis näitab loodud voo ja saadetise ID-d.</span><span class="sxs-lookup"><span data-stu-id="36f3f-242">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="36f3f-243">Luuakse ka täiendusvoog.</span><span class="sxs-lookup"><span data-stu-id="36f3f-243">A replenishment wave is also created.</span></span>

    <span data-ttu-id="36f3f-244">Saate ka hoiatusteate, mis ütleb: "Töö ID XXXX blokeeringut ei saa tühistada, kuna see on lõpuleviimata täiendustöö."</span><span class="sxs-lookup"><span data-stu-id="36f3f-244">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="view-work-details"></a><span data-ttu-id="36f3f-245">Kuva töö üksikasjad</span><span class="sxs-lookup"><span data-stu-id="36f3f-245">View work details</span></span>

1. <span data-ttu-id="36f3f-246">Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-246">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="36f3f-247">Filtreerige jaotises **Ülevaade** lao *61* veerg **Ladu**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-247">In the **Overview** section, filter the **Warehouse** column for warehouse *61*.</span></span>
1. <span data-ttu-id="36f3f-248">Peaksite nägema, et kolme nõudluse müügitellimuse jaoks loodi seitse töö ID-d.</span><span class="sxs-lookup"><span data-stu-id="36f3f-248">You should see that seven work IDs were created for the three demand sales orders.</span></span>

    - <span data-ttu-id="36f3f-249">Kolmel seitsmest töö ID-st on *Täiendamise* **Töökäsu tüübi** väärtus ja neljal on *Müügitellimuse* **Töökäsu tüübi** väärtus.</span><span class="sxs-lookup"><span data-stu-id="36f3f-249">Three of the seven work IDs have a **Work order type** value of *Replenishment*, and four have a **Work order type** value of *Sales orders*.</span></span>
    - <span data-ttu-id="36f3f-250">Kõik kolm töö ID-d mille *Täiendamise* väärtusel on **Töökäsu tüüp** sama asukohaga *Komplekteerimine* ja *Ladustamine* jaotises **Read**:</span><span class="sxs-lookup"><span data-stu-id="36f3f-250">All three work IDs that have a **Work order type** value of *Replenishment* have the same *Pick* and *Put* locations in the **Lines** section:</span></span>

        - <span data-ttu-id="36f3f-251">**Komplekteerimine:** *02A01R5S1B*</span><span class="sxs-lookup"><span data-stu-id="36f3f-251">**Pick:** *02A01R5S1B*</span></span>
        - <span data-ttu-id="36f3f-252">**Ladustamine:** *06A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="36f3f-252">**Put:** *06A01R2S1B*</span></span>

    - <span data-ttu-id="36f3f-253">Müügitellimuse 1 jaoks loodi kaks töö ID-d.</span><span class="sxs-lookup"><span data-stu-id="36f3f-253">Two work IDs were created for sales order 1.</span></span>

1. <span data-ttu-id="36f3f-254">Märkige üles müügitellimuste töö ID-d.</span><span class="sxs-lookup"><span data-stu-id="36f3f-254">Make a note of the work IDs for the sales orders.</span></span>

<span data-ttu-id="36f3f-255">Vabast kogusest olenevalt võivad loodud töökogused veidi erineda.</span><span class="sxs-lookup"><span data-stu-id="36f3f-255">Depending on your on-hand quantities, the work quantities that are created might vary slightly.</span></span> <span data-ttu-id="36f3f-256">Kuid üldiselt peaksid loodud tööpäised vastama selle stsenaariumi näitele.</span><span class="sxs-lookup"><span data-stu-id="36f3f-256">However, overall, the work headers that are created should match this scenario example.</span></span>

#### <a name="on-hand-inventory-license-plate-id"></a><span data-ttu-id="36f3f-257">Vaba kaubavaru identifitseerimisnumbri ID</span><span class="sxs-lookup"><span data-stu-id="36f3f-257">On-hand inventory license plate ID</span></span>

<span data-ttu-id="36f3f-258">Selle stsenaariumi korral saate hiljem kasutada mobiilirakendust Warehouse Management (või emulaatorit), kus tuleb komplekteerimis- ja täiendusstsenaariumite jaoks tuvastada identifitseerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="36f3f-258">Later in this scenario, you will use the Warehouse Management mobile app (or an emulator), where you must identify the license plate to complete the picking and replenishment scenarios.</span></span>

<span data-ttu-id="36f3f-259">Identifitseerimisnumbri ID-de hilisemaks leidmiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="36f3f-259">To find the license plate IDs that you will need later, follow these steps.</span></span>

1. <span data-ttu-id="36f3f-260">Avage **Laohaldus \> Päringud ja aruanded \> Vabade kaubavarude loend**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-260">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="36f3f-261">Filtripaani avamiseks valige nupp **Kuva filtrid**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-261">Select the **Show filters** button to open the filter pane.</span></span>
1. <span data-ttu-id="36f3f-262">Stsenaariumi jaoks identifitseerimisnumbrite saamiseks sisestage järgmised filtreerimiskriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="36f3f-262">Enter the following filtering criteria to get the license plates for the scenario.</span></span> <span data-ttu-id="36f3f-263">Kasutage filtrit *alguses on*.</span><span class="sxs-lookup"><span data-stu-id="36f3f-263">Use the *begins with* filter.</span></span>

    - <span data-ttu-id="36f3f-264">**Kauba kood:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="36f3f-264">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="36f3f-265">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="36f3f-265">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="36f3f-266">Valige **Rakendamine**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-266">Select **Apply**.</span></span>
1. <span data-ttu-id="36f3f-267">Valige toimingupaanil **Dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-267">On the Action Pane, select **Dimensions**.</span></span>
1. <span data-ttu-id="36f3f-268">Valige kõik väärtused jaotise **Laoala dimensioonid** dialoogiboks **Dimensioonide kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-268">In the **Dimensions display** dialog box, in the **Storage Dimensions** section, select all the values.</span></span>
1. <span data-ttu-id="36f3f-269">Tehke jaotises **Kanded** valik **Kauba kood** ja **Kogus \<\> 0**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-269">In the **Transactions** section, select **Item number** and **Quantity \<\> 0**.</span></span>
1. <span data-ttu-id="36f3f-270">Kui olete lõpetanud, valige dialoogiboksi sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-270">When you've finished, select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="36f3f-271">Tabeli **Vabad varud** kuvatakse identifitseerimisnumbrid kaubale *T0100* igas kohas.</span><span class="sxs-lookup"><span data-stu-id="36f3f-271">The **On-hand** grid shows the license plate numbers for item *T0100* in each location.</span></span> <span data-ttu-id="36f3f-272">Märkige üles igale asukohale vastav identifitseerimisnumber, kuna seda teavet on hiljem vaja.</span><span class="sxs-lookup"><span data-stu-id="36f3f-272">Make a note of the license plate that is in each location, because you will need this information later.</span></span>
1. <span data-ttu-id="36f3f-273">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="36f3f-273">Close the page.</span></span>

### <a name="process-steps"></a><span data-ttu-id="36f3f-274">Protsessi etapid</span><span class="sxs-lookup"><span data-stu-id="36f3f-274">Process steps</span></span>

<span data-ttu-id="36f3f-275">Teete lao asukoha täiendamise esimese kahe töö ID-de jaoks.</span><span class="sxs-lookup"><span data-stu-id="36f3f-275">You will perform the warehouse location replenishment for the first two work IDs.</span></span> <span data-ttu-id="36f3f-276">Töö kolmanda täiendamise töö jaoks blokeeritakse seni, kuni varude tase komplekteerimise asukohas langeb allapoole läve.</span><span class="sxs-lookup"><span data-stu-id="36f3f-276">Work on the third replenishment work will be blocked until the inventory level in the picking location falls below the threshold.</span></span>

#### <a name="replenishment"></a><span data-ttu-id="36f3f-277">Täiendamine</span><span class="sxs-lookup"><span data-stu-id="36f3f-277">Replenishment</span></span>

1. <span data-ttu-id="36f3f-278">Logige mobiilirakendusse Warehouse Management sisse lao *61* kasutajana.</span><span class="sxs-lookup"><span data-stu-id="36f3f-278">Sign in to the Warehouse Management mobile app as a user in warehouse *61*.</span></span> <span data-ttu-id="36f3f-279">(Sisestage *61* kasutaja ID-na ja *1* paroolina.)</span><span class="sxs-lookup"><span data-stu-id="36f3f-279">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="36f3f-280">Avage **Varud \> Täiendamine**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-280">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="36f3f-281">Teil palutakse esimene täiendustöö lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="36f3f-281">You're prompted to complete the first replenishment work.</span></span> <span data-ttu-id="36f3f-282">Kuvatakse kaubakood, kogus, asukoht ja komplekteerimise asukoht.</span><span class="sxs-lookup"><span data-stu-id="36f3f-282">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="36f3f-283">Sisestage väljale **LP** kauba identifitseerimisnumber näidatud asukohas.</span><span class="sxs-lookup"><span data-stu-id="36f3f-283">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="36f3f-284">Valige nupp **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="36f3f-284">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="36f3f-285">Süsteem genereerib sihtkoha identifitseerimisnumbri komplekteeritud kauba uue identifitseerimisnumbri jaoks.</span><span class="sxs-lookup"><span data-stu-id="36f3f-285">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="36f3f-286">Valige väärtuse kinnitamiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-286">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="36f3f-287">Kuvatakse ladustamistöö, mis juhendab kasutajat paigutama sihtkoha identifitseerimisnumbrit täiendamise asukohta.</span><span class="sxs-lookup"><span data-stu-id="36f3f-287">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="36f3f-288">*Ladustamise* asukoht peab olema **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-288">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="36f3f-289">Kinnitage ladustamise üksikasjad ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-289">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="36f3f-290">Kuvatakse teade "Töö on lõpule viidud" ja kuvatakse järgmise täiendamise komplekteerimisülesande üksikasjad: kauba kood, kogus ja asukoht, kust komplekteerida.</span><span class="sxs-lookup"><span data-stu-id="36f3f-290">You receive a "Work Completed" message, and the details of the next replenishment pick task are shown: the item number, quantity, and location to pick from.</span></span> <span data-ttu-id="36f3f-291">Komplekteerimise asukoht on sama, mis esimese täiendamise asukoht.</span><span class="sxs-lookup"><span data-stu-id="36f3f-291">The picking location will be the same as the first replenishment location.</span></span> <span data-ttu-id="36f3f-292">Seetõttu on identifitseerimisnumbril sama identifitseerimisnumbri ID, mida kasutati esimese täiendustöö ülesande jaoks.</span><span class="sxs-lookup"><span data-stu-id="36f3f-292">Therefore, the license plate will have the same license plate ID that was used for the first replenishment work task.</span></span>

1. <span data-ttu-id="36f3f-293">Korrake eelnevaid samme teise tööülesande täiendustöö lõpuleviimiseks.</span><span class="sxs-lookup"><span data-stu-id="36f3f-293">Repeat the preceding steps to complete the replenishment work for the second work task.</span></span> <span data-ttu-id="36f3f-294">Koguse ja sihtkoha identifitseerimisnumber erinevad esimese tööülesande kogusest ja sihtkoha identifitseerimisnumbrist.</span><span class="sxs-lookup"><span data-stu-id="36f3f-294">The quantity and target license plate will differ from the quantity and target license plate for the first work task.</span></span>

<span data-ttu-id="36f3f-295">Pärast teise täiendustöö lõpuleviimist saate teate "Töö on lõpule viidud".</span><span class="sxs-lookup"><span data-stu-id="36f3f-295">After the second replenishment work is completed, you receive a "Work Completed" message.</span></span> <span data-ttu-id="36f3f-296">Mobiilne seade teavitab teile, et tööd pole saadaval ka siis, kui mõni täiendustöö on alles jäänud.</span><span class="sxs-lookup"><span data-stu-id="36f3f-296">The mobile device also informs you that there is no work available, even though some replenishment work remains.</span></span> <span data-ttu-id="36f3f-297">Selline käitumine ilmneb seetõttu, et täiendustöö olekuks on *Hoitakse* ja on seetõttu märgitud väärtuseks **Blokeeritud**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-297">This behavior occurs because the replenishment work has an availability status of *Held* and is therefore marked as **Blocked**.</span></span>

<span data-ttu-id="36f3f-298">Olek *Hoitakse* käivitati, kuna komplekteerimise asukoha asukohaprofiili määratluse **Ületäitumise kogus** väärtuseks on *0,65 PL*.</span><span class="sxs-lookup"><span data-stu-id="36f3f-298">The *Held* status was triggered because the location profile for the picking location that the work is being assigned to has an **Overflow quantity** value of *0.65 PL*.</span></span> <span data-ttu-id="36f3f-299">Kaks eelmist täiendustöö ülesannet täitsid asukoha peaaegu kauba *T0100* ületäitumise piirini.</span><span class="sxs-lookup"><span data-stu-id="36f3f-299">The two previous replenishment work tasks filled the location almost to its overflow limit for item *T0100*.</span></span> <span data-ttu-id="36f3f-300">(Kaubaühiku teisendus kaubale on *1 PL = 100 ühikut* .) Seetõttu põhjustaks järelejäänud täiendustöö asukoha ületäitumispiirangu ületamise.</span><span class="sxs-lookup"><span data-stu-id="36f3f-300">(The unit conversion for the item is *1 PL = 100 ea*.) Therefore, the remaining replenishment work would cause the location to exceed its overflow limit.</span></span>

<span data-ttu-id="36f3f-301">Kuni asukohast komplekteeritakse mobiilse seadme menüü-üksuses piisavalt varusid nende toomiseks allapoole vabastusläve, jääb see täiendustöö blokeerituks.</span><span class="sxs-lookup"><span data-stu-id="36f3f-301">Until enough inventory is picked from the location to bring it below the work release threshold on the mobile device menu item, this replenishment work will remain blocked.</span></span>

#### <a name="sales-order-pick"></a><span data-ttu-id="36f3f-302">Müügitellimuse komplekteerimine</span><span class="sxs-lookup"><span data-stu-id="36f3f-302">Sales order pick</span></span>

<span data-ttu-id="36f3f-303">Enne kui järelejäänud täiendamistöö ülesannet saab lõpule viia, tuleb komplekteerimise asukohast tühjendada varud tasemeni, milles ülejäänud täiendustöö blokeeringu saaks tühistada.</span><span class="sxs-lookup"><span data-stu-id="36f3f-303">Before the remaining replenishment work task can be completed, the picking location must be depleted of inventory to a level where the remaining replenishment work can be unblocked.</span></span> <span data-ttu-id="36f3f-304">Teisisõnu ei saa vaba kaubavaru koguse summa asukohas ja varude täiendamise kogus ületada **Ületäitumise koguse** väärtust.</span><span class="sxs-lookup"><span data-stu-id="36f3f-304">In other words, the sum of the quantity of on-hand inventory in the location and the replenishment quantity can't exceed the **Overflow quantity** value.</span></span> <span data-ttu-id="36f3f-305">Kui see summa on ületäitumise kogusest väiksem, tühistatakse järelejäänud täiendustöö blokeering.</span><span class="sxs-lookup"><span data-stu-id="36f3f-305">When this sum is less than the overflow quantity, the remaining replenishment work will be unblocked.</span></span>

1. <span data-ttu-id="36f3f-306">Logige mobiilirakendusse Warehouse Management sisse lao *61* kasutajana.</span><span class="sxs-lookup"><span data-stu-id="36f3f-306">Sign in to the Warehouse Management mobile app as a user in warehouse *61*.</span></span> <span data-ttu-id="36f3f-307">(Sisestage *61* kasutaja ID-na ja *1* paroolina.)</span><span class="sxs-lookup"><span data-stu-id="36f3f-307">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="36f3f-308">Avage **Väljaminev \> Müügi komplekteerimine**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-308">Go to **Outbound \> Sales Picking**.</span></span>
1. <span data-ttu-id="36f3f-309">Sisestage müügitellimuse 1 esimene töö ID.</span><span class="sxs-lookup"><span data-stu-id="36f3f-309">Enter the first work ID for sales order 1.</span></span>

    <span data-ttu-id="36f3f-310">Vaadake müügitellimuse töö ID-d, mille kohta varem märkme tegite, lehelt **Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-310">Refer to the work IDs for sales orders that you made a note of earlier, on the **Work details** page.</span></span> <span data-ttu-id="36f3f-311">Siia sisestatav töö ID genereerib 10 ea komplekteerimistöö kahest erinvast asukohast.</span><span class="sxs-lookup"><span data-stu-id="36f3f-311">The work ID that you enter here will generate pick work for a quantity of 10 ea from two separate locations.</span></span>

1. <span data-ttu-id="36f3f-312">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-312">Select **OK**.</span></span>

    <span data-ttu-id="36f3f-313">Ülesandelehel **Müügitellimus: komplekteerimine** kuvatakse kauba kood, kogus ja komplekteerimine esimesest asukohast.</span><span class="sxs-lookup"><span data-stu-id="36f3f-313">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the first location.</span></span>

1. <span data-ttu-id="36f3f-314">Sisestage väljale **LP** kauba identifitseerimisnumber näidatud asukohas.</span><span class="sxs-lookup"><span data-stu-id="36f3f-314">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="36f3f-315">Valige nupp **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="36f3f-315">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="36f3f-316">Ülesandelehel **Müügitellimus: komplekteerimine** kuvatakse kauba kood, kogus ja komplekteerimine teisest asukohast.</span><span class="sxs-lookup"><span data-stu-id="36f3f-316">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the next location.</span></span>

1. <span data-ttu-id="36f3f-317">Sisestage väljale **LP** kauba identifitseerimisnumber näidatud asukohas.</span><span class="sxs-lookup"><span data-stu-id="36f3f-317">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="36f3f-318">Valige nupp **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="36f3f-318">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="36f3f-319">Lehel **Müügitellimused: ladustamine** suunab ära panema mõlemad lõpuleviidud komplekteerimistööd väljaminevasse ettevalmistusasukohta.</span><span class="sxs-lookup"><span data-stu-id="36f3f-319">The **Sales orders: Put** page instructs you to put away both the completed picking works to the outbound staging location.</span></span>

1. <span data-ttu-id="36f3f-320">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-320">Select **OK**.</span></span>

    <span data-ttu-id="36f3f-321">Teile kuvatakse teade „Töö lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="36f3f-321">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="36f3f-322">Sisestage müügitellimuse 1 teine töö ID.</span><span class="sxs-lookup"><span data-stu-id="36f3f-322">Enter the second work ID for sales order 1.</span></span>

    <span data-ttu-id="36f3f-323">Selle töö ID jaoks on ainult üks komplekteerimisülesanne.</span><span class="sxs-lookup"><span data-stu-id="36f3f-323">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="36f3f-324">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-324">Select **OK**.</span></span>

    <span data-ttu-id="36f3f-325">Ülesandelehel **Müügitellimus: komplekteerimine** kuvatakse kauba kood, kogus ja komplekteerimiskoht.</span><span class="sxs-lookup"><span data-stu-id="36f3f-325">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="36f3f-326">Sisestage väljale **LP** kauba identifitseerimisnumber näidatud asukohas.</span><span class="sxs-lookup"><span data-stu-id="36f3f-326">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="36f3f-327">Teie määratud identifitseerimisnumber on üks süsteemi genereeritud identifitseerimisnumbritest täiendustöö ülesandest.</span><span class="sxs-lookup"><span data-stu-id="36f3f-327">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="36f3f-328">Veendumaks, et hõivate õige identifitseerimisnumbri ID, kontrollige varude kaupa, asukohta ja kogust lehelt **Vaba kaubavaru loend**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-328">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="36f3f-329">Valige nupp **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="36f3f-329">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="36f3f-330">Kinnitage ladustamisülesande juhised väljaminevasse ettevalmistusasukohta.</span><span class="sxs-lookup"><span data-stu-id="36f3f-330">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="36f3f-331">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-331">Select **OK**.</span></span>

    <span data-ttu-id="36f3f-332">Teile kuvatakse teade „Töö lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="36f3f-332">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="36f3f-333">Müügitellimus 2 on komplekteerimisel blokeeritud, kuna sellega seotud täiendusülesanne pole lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="36f3f-333">Sales order 2 is blocked from picking because the replenishment task that it's linked to isn't completed.</span></span> <span data-ttu-id="36f3f-334">Praegu on komplekteerimise asukohas veel 30 ühikut kogust ja müügitellimuse 2 varude täiendamise kogus on 60 ühikut.</span><span class="sxs-lookup"><span data-stu-id="36f3f-334">Currently, there is still a quantity of 30 ea in the picking location, and the replenishment quantity for sales order 2 is 60 ea.</span></span> <span data-ttu-id="36f3f-335">Vaba kaubavaru ja täiendamise varude summa (90 ühikut) ületab ületäitumise koguse 0,65 PL (või 65 ühikut).</span><span class="sxs-lookup"><span data-stu-id="36f3f-335">The sum of the on-hand inventory and the replenishment inventory (90 ea) exceeds the overflow quantity of 0.65 PL (or 65 ea).</span></span> <span data-ttu-id="36f3f-336">Enne täiendustöö lõpuleviimist tuleb komplekteerida müügitellimus 3.</span><span class="sxs-lookup"><span data-stu-id="36f3f-336">Before the replenishment work can be completed, sales order 3 must be picked.</span></span>

1. <span data-ttu-id="36f3f-337">Sisestage müügitellimuse 3 töö ID.</span><span class="sxs-lookup"><span data-stu-id="36f3f-337">Enter the work ID for sales order 3.</span></span>

    <span data-ttu-id="36f3f-338">Selle töö ID jaoks on ainult üks komplekteerimisülesanne.</span><span class="sxs-lookup"><span data-stu-id="36f3f-338">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="36f3f-339">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-339">Select **OK**.</span></span>

    <span data-ttu-id="36f3f-340">Ülesandelehel **Müügitellimus: komplekteerimine** kuvatakse kauba kood, kogus ja komplekteerimiskoht.</span><span class="sxs-lookup"><span data-stu-id="36f3f-340">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="36f3f-341">Sisestage väljale **LP** kauba identifitseerimisnumber näidatud asukohas.</span><span class="sxs-lookup"><span data-stu-id="36f3f-341">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="36f3f-342">Teie määratud identifitseerimisnumber on üks süsteemi genereeritud identifitseerimisnumbritest täiendustöö ülesandest.</span><span class="sxs-lookup"><span data-stu-id="36f3f-342">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="36f3f-343">Veendumaks, et hõivate õige identifitseerimisnumbri ID, kontrollige varude kaupa, asukohta ja kogust lehelt **Vaba kaubavaru loend**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-343">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="36f3f-344">Valige nupp **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="36f3f-344">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="36f3f-345">Kinnitage ladustamisülesande juhised väljaminevasse ettevalmistusasukohta.</span><span class="sxs-lookup"><span data-stu-id="36f3f-345">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="36f3f-346">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-346">Select **OK**.</span></span>

    <span data-ttu-id="36f3f-347">Teile kuvatakse teade „Töö lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="36f3f-347">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="36f3f-348">Kohe, kui vaba kaubavaru koguse summa komplekteerimise asukohas ja täiendamise kogus on alla piirmäära, saate töödelda järelejäänud täiendustööd.</span><span class="sxs-lookup"><span data-stu-id="36f3f-348">As soon as the sum of the on-hand quantity in the picking location and the replenishment quantity is below the threshold, you will be able to process the remaining replenishment work.</span></span>

<span data-ttu-id="36f3f-349">Minge tagasi lehele **Töö üksikasjad** ja märkate, et täiendustöö kättesaadavus täiendamise (müügitellimus 2) viimaseks osaks on *Avatud*, kuna asukohas on nüüd piisavalt ruumi täiendamisega nõustumiseks.</span><span class="sxs-lookup"><span data-stu-id="36f3f-349">Return to the **Work details** page, and notice that the replenishment work availability for the final piece of replenishment (for sales order 2) is *Open*, because there is now enough space in the location to accept the replenishment.</span></span>

<span data-ttu-id="36f3f-350">Nüüd saate seda täiendustööd mobiilse seadme kaudu töödelda.</span><span class="sxs-lookup"><span data-stu-id="36f3f-350">You can now process this replenishment work via the mobile device.</span></span>

1. <span data-ttu-id="36f3f-351">Avage **Varud \> Täiendamine**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-351">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="36f3f-352">Teil palutakse lõpetada ülejäänud täiendustöö.</span><span class="sxs-lookup"><span data-stu-id="36f3f-352">You're prompted to complete the remaining replenishment work.</span></span> <span data-ttu-id="36f3f-353">Kuvatakse kaubakood, kogus, asukoht ja komplekteerimise asukoht.</span><span class="sxs-lookup"><span data-stu-id="36f3f-353">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="36f3f-354">Sisestage väljale **LP** kauba identifitseerimisnumber näidatud asukohas.</span><span class="sxs-lookup"><span data-stu-id="36f3f-354">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="36f3f-355">Valige nupp **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="36f3f-355">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="36f3f-356">Süsteem genereerib sihtkoha identifitseerimisnumbri komplekteeritud kauba uue identifitseerimisnumbri jaoks.</span><span class="sxs-lookup"><span data-stu-id="36f3f-356">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="36f3f-357">Valige väärtuse kinnitamiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-357">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="36f3f-358">Kuvatakse ladustamistöö, mis juhendab kasutajat paigutama sihtkoha identifitseerimisnumbrit täiendamise asukohta.</span><span class="sxs-lookup"><span data-stu-id="36f3f-358">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="36f3f-359">*Ladustamise* asukoht peab olema **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-359">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="36f3f-360">Kinnitage ladustamise üksikasjad ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-360">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="36f3f-361">Saate sõnumid "Töö on lõpule viidud" ja "Ühtegi tööd pole saadaval".</span><span class="sxs-lookup"><span data-stu-id="36f3f-361">You receive "Work Completed" and "No Work Available" messages.</span></span>

<span data-ttu-id="36f3f-362">Nüüd saate komplekteerida müügitellimuse 2.</span><span class="sxs-lookup"><span data-stu-id="36f3f-362">You can now pick sales order 2.</span></span> <span data-ttu-id="36f3f-363">Selle blokeering tühistati, kui müügitellimusega seotud täiendustöö viidi lõpule.</span><span class="sxs-lookup"><span data-stu-id="36f3f-363">It became unblocked when the replenishment work that is linked to the sales order was completed.</span></span>

1. <span data-ttu-id="36f3f-364">Sisestage müügitellimuse 2 töö ID.</span><span class="sxs-lookup"><span data-stu-id="36f3f-364">Enter the work ID for sales order 2.</span></span>

    <span data-ttu-id="36f3f-365">Selle töö ID jaoks on ainult üks komplekteerimisülesanne.</span><span class="sxs-lookup"><span data-stu-id="36f3f-365">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="36f3f-366">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-366">Select **OK**.</span></span>

    <span data-ttu-id="36f3f-367">Ülesandelehel **Müügitellimus: komplekteerimine** kuvatakse kauba kood, kogus ja komplekteerimiskoht.</span><span class="sxs-lookup"><span data-stu-id="36f3f-367">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="36f3f-368">Sisestage väljale **LP** kauba identifitseerimisnumber näidatud asukohas.</span><span class="sxs-lookup"><span data-stu-id="36f3f-368">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="36f3f-369">Teie määratud identifitseerimisnumber on süsteemi genereeritud identifitseerimisnumber täiendustöö ülesandest.</span><span class="sxs-lookup"><span data-stu-id="36f3f-369">The license plate that you specify will be the system-generated license plate from the replenishment work task.</span></span> <span data-ttu-id="36f3f-370">Veendumaks, et hõivate õige identifitseerimisnumbri ID, kontrollige varude kaupa, asukohta ja kogust lehelt **Vaba kaubavaru loend**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-370">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="36f3f-371">Valige nupp **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="36f3f-371">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="36f3f-372">Kinnitage ladustamisülesande juhised väljaminevasse ettevalmistusasukohta.</span><span class="sxs-lookup"><span data-stu-id="36f3f-372">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="36f3f-373">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-373">Select **OK**.</span></span>

    <span data-ttu-id="36f3f-374">Teile kuvatakse teade „Töö lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="36f3f-374">You receive a "Work Completed" message.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="36f3f-375">Märkmed ja näpunäited</span><span class="sxs-lookup"><span data-stu-id="36f3f-375">Notes and tips</span></span>

- <span data-ttu-id="36f3f-376">See funktsioon töötab kõigi täiendustüüpidega: voo nõudlus, min/max, koormuse nõudlus ja leidmine.</span><span class="sxs-lookup"><span data-stu-id="36f3f-376">This functionality works with all types of replenishment: wave demand, min/max, load demand, and slotting.</span></span>
- <span data-ttu-id="36f3f-377">Soovi korral saate iga tööpäise täiendustöö saadavuse käsitsi alistada lehel **Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="36f3f-377">You can manually override the replenishment work availability for each work header from the **Work details** page if you want.</span></span>
- <span data-ttu-id="36f3f-378">Kui süsteem määrab täiendustöö kättesaadavuse, võtab see arvesse kõik varud, mis on enne töö lõpuleviimist asukohas juba olemas.</span><span class="sxs-lookup"><span data-stu-id="36f3f-378">When the system sets the replenishment work availability, it considers any inventory that is already in the location before any work is completed</span></span>
- <span data-ttu-id="36f3f-379">Müügitellimustöö iga osa on seotud konkreetse täiendustööga.</span><span class="sxs-lookup"><span data-stu-id="36f3f-379">Each piece of sales order work is linked to a specific replenishment work.</span></span> <span data-ttu-id="36f3f-380">Vastavat müügi töö saadavuse funktsiooni pole.</span><span class="sxs-lookup"><span data-stu-id="36f3f-380">There is no corresponding sales work availability functionality.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]