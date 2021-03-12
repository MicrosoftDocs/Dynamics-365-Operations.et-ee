---
title: Pane seinale – pane kauplusesse
description: Selles teemas antakse teavet funktsiooni Pane seinale – pane kauplusesse kohta. See funktsioon võimaldab teil käsitseda stsenaariume, kus peate konsolideerima toote eelpakkimise vaheasukohta konfigureeritavate kriteeriumide põhjal. See aitab vähendada komplekteerimise aega, sest see võimaldab komplekteerimist ühele sihtidentifitseerimisnumbrile ja panna rohkematesse asukohtadesse kui kogumi komplekteerimise puhul.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3f2ae63758fcb6247c5e56433645d9252576c755
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996271"
---
# <a name="put-to-wall---put-to-store"></a><span data-ttu-id="d6e64-105">Pane seinale – pane kauplusesse</span><span class="sxs-lookup"><span data-stu-id="d6e64-105">Put to wall - put to store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6e64-106">Funktsioon *Pane seinale – pane kauplusesse* võimaldab teil käsitseda stsenaariume, kus peate konsolideerima toote eelpakkimise vaheasukohta konfigureeritavate kriteeriumide põhjal.</span><span class="sxs-lookup"><span data-stu-id="d6e64-106">The *Put to wall - put to store* functionality lets you handle scenarios where you must consolidate a product to a prepack staging area, based on configurable criteria.</span></span> <span data-ttu-id="d6e64-107">Kuna see funktsioon võimaldab komplekteerimist ühele sihtidentifitseerimisnumbrile ja panna rohkematesse asukohtadesse kui kogumi komplekteerimise puhul, saavad lühenenud komplekteerimisajast kasu ettevõtted, mis lähetavad kauplustesse või tegelevad väikeste kaupadega.</span><span class="sxs-lookup"><span data-stu-id="d6e64-107">Because this functionality allows for picking to a single target license plate and can use more put positions than cluster picking, companies that ship to stores or handle small items will benefit from decreased picking time.</span></span>

<span data-ttu-id="d6e64-108">Selle funktsiooni töövoog suunab komplekteeritud toote sortimise asukohta eri tüüpi konteineritesse jaotamiseks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-108">The workflow for this functionality directs picked product to a sorting location for distribution into various types of containers.</span></span> <span data-ttu-id="d6e64-109">Üldiselt sisaldab iga sortimise asukoht mitut sortimise paigutust.</span><span class="sxs-lookup"><span data-stu-id="d6e64-109">Generally, each sorting location includes multiple sort positions.</span></span> <span data-ttu-id="d6e64-110">Iga sortimise asukoht määratakse vastavalt äriprotsessi seadistatud kriteeriumidele.</span><span class="sxs-lookup"><span data-stu-id="d6e64-110">Each sort position is assigned according to the criteria that are set by the business process.</span></span> <span data-ttu-id="d6e64-111">Tavalised kriteeriumid on lõppsihtkoht, saadetis või koormus.</span><span class="sxs-lookup"><span data-stu-id="d6e64-111">Typical criteria are the final destination, shipment, or load.</span></span> <span data-ttu-id="d6e64-112">Pärast toote saabumist jaotatakse see kõigi sortimise asukohtade vahel tellimuse, sihtkoha, saadetise või koormusega seostatud koguse põhjal.</span><span class="sxs-lookup"><span data-stu-id="d6e64-112">After a product arrives, it's distributed to each sort position, based on the quantity that is associated with the order, destination, shipment, or load.</span></span> <span data-ttu-id="d6e64-113">Kui konteiner on täis või lõpule viidud, teisaldatakse see sõltuvalt äriprotsessist vahekasukohta või saadetise asukohta edasiseks töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-113">When a container is full or complete, it's moved to a staging location or a shipping location for further handling, depending on the business process.</span></span>

<span data-ttu-id="d6e64-114">Seda ladustamise funktsiooni nimetatakse ka näiteks kiireks panemiseks ja piirjoonte avamisteks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-114">This warehousing functionality is also referred to by other names, such as put-to-light and break opens.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="d6e64-115">Väljamineku sortimise funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="d6e64-115">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="d6e64-116">Enne funktsiooni *Pane seinale – pane kauplusesse* kasutamist peab funktsioon *Väljamineku sortimine* olema teie süsteemis sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="d6e64-116">Before you can use the *Put to wall - put to store* functionality, the *Outbound sorting* feature must be turned on in your system.</span></span> <span data-ttu-id="d6e64-117">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="d6e64-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d6e64-118">Seega on funktsioon loetletud järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="d6e64-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d6e64-119">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="d6e64-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d6e64-120">**Funktsiooni nimi:** *Väljamineku sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-120">**Feature name:** *Outbound sorting*</span></span>

<span data-ttu-id="d6e64-121">Funktsiooni *Väljamineku sortimine* saab kasutada koos funktsiooniga *Organisatsiooniülene vooetapi kood*, kui see on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="d6e64-121">The *Outbound sorting* feature can be used in conjunction with the *Organization wide wave step code* feature if it's turned on.</span></span> <span data-ttu-id="d6e64-122">Samuti peate selle funktsiooni sisse lülitama, kui kasutate eelmääratletud koode, mis seadistatakse vooetapi koodides.</span><span class="sxs-lookup"><span data-stu-id="d6e64-122">You must also turn on this feature if you will use predefined codes that are set up in wave step codes.</span></span> <span data-ttu-id="d6e64-123">Tööruumis **Funktsioonihaldus** loetletakse seda funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="d6e64-123">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="d6e64-124">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="d6e64-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d6e64-125">**Funktsiooni nimi:** *Organisatsiooniülene vooetapi kood*</span><span class="sxs-lookup"><span data-stu-id="d6e64-125">**Feature name:** *Organization wide wave step code*</span></span>

## <a name="setup"></a><span data-ttu-id="d6e64-126">Häälestus</span><span class="sxs-lookup"><span data-stu-id="d6e64-126">Setup</span></span>

<span data-ttu-id="d6e64-127">Selle demo puhul kasutatakse standardseid Contoso andmeid ja ladu *62*.</span><span class="sxs-lookup"><span data-stu-id="d6e64-127">For this demo, standard Contoso data and warehouse *62* are used.</span></span> <span data-ttu-id="d6e64-128">Samuti kasutatakse mõndasid hiljem esitatud täiendusi.</span><span class="sxs-lookup"><span data-stu-id="d6e64-128">Some additions that are noted later are also used.</span></span>

### <a name="location-type"></a><span data-ttu-id="d6e64-129">Asukoha tüüp</span><span class="sxs-lookup"><span data-stu-id="d6e64-129">Location type</span></span>

1. <span data-ttu-id="d6e64-130">Avage jaotis **Laohaldus \> Seadistus \> Ladu \> Asukoha tüübid**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-130">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="d6e64-131">Valige toimingupaanil **Uus**, et luua asukoha tüüp sortimiseks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-131">On the Action Pane, select **New** to create a location type for sorting.</span></span>
1. <span data-ttu-id="d6e64-132">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-132">Set the following values:</span></span>

    - <span data-ttu-id="d6e64-133">**Asukoha tüüp:** *SORTIMINE*</span><span class="sxs-lookup"><span data-stu-id="d6e64-133">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="d6e64-134">**Kirjeldus:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-134">**Description:** *Sort*</span></span>

1. <span data-ttu-id="d6e64-135">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-135">Select **Save**.</span></span>

### <a name="warehouse-management-parameters"></a><span data-ttu-id="d6e64-136">Laohalduse parameetrid</span><span class="sxs-lookup"><span data-stu-id="d6e64-136">Warehouse management parameters</span></span>

1. <span data-ttu-id="d6e64-137">Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-137">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="d6e64-138">Sisestage vahekaardi **Üldine** kiirkaardi **Asukoha tüübid** väljale **Sortimise asukoha tüüp** väärtus *SORTIMINE*.</span><span class="sxs-lookup"><span data-stu-id="d6e64-138">On the **General** tab, on the **Location types** FastTab, in the **Sorting location type** field, enter *SORT*.</span></span>
1. <span data-ttu-id="d6e64-139">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-139">Select **Save**.</span></span>

### <a name="location-profile"></a><span data-ttu-id="d6e64-140">Asukohaprofiil</span><span class="sxs-lookup"><span data-stu-id="d6e64-140">Location profile</span></span>

1. <span data-ttu-id="d6e64-141">Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukohaprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-141">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="d6e64-142">Valige toimingupaanil **Uus**, et luua asukohaprofiil sortimise asukoha jaoks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-142">On the Action Pane, select **New** to create a location profile for the sorting location.</span></span>
1. <span data-ttu-id="d6e64-143">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-143">In the header, set the following values:</span></span>

    - <span data-ttu-id="d6e64-144">**Asukohaprofiili ID:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-144">**Location profile ID:** *Sort*</span></span>
    - <span data-ttu-id="d6e64-145">**Nimi:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-145">**Name:** *Sort*</span></span>

1. <span data-ttu-id="d6e64-146">Määrake kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-146">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d6e64-147">**Asukoha vorming:** *PAKKIMINE*</span><span class="sxs-lookup"><span data-stu-id="d6e64-147">**Location format:** *PACK*</span></span>
    - <span data-ttu-id="d6e64-148">**Asukoha tüüp:** *SORTIMINE*</span><span class="sxs-lookup"><span data-stu-id="d6e64-148">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="d6e64-149">**Kasuta identifitseerimisnumbri jälgimist:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="d6e64-149">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="d6e64-150">**Luba segakaubad:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="d6e64-150">**Allow mixed items:** *Yes*</span></span>
    - <span data-ttu-id="d6e64-151">**Luba varude segaolekud:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="d6e64-151">**Allow mixed inventory statuses:** *Yes*</span></span>

1. <span data-ttu-id="d6e64-152">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-152">Select **Save**.</span></span>

### <a name="locations"></a><span data-ttu-id="d6e64-153">Asukohad</span><span class="sxs-lookup"><span data-stu-id="d6e64-153">Locations</span></span>

1. <span data-ttu-id="d6e64-154">Avage **Laohaldus \> Seadistus \> Ladu \> Asukohad**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-154">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="d6e64-155">Tühjendage märkeruut **Loo kontrollnumbrid asukoha jaoks**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-155">Clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="d6e64-156">Valige toimingupaanil **Uus** ja seejärel seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-156">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="d6e64-157">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="d6e64-157">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="d6e64-158">**Asukoht:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-158">**Location:** *Sort*</span></span>
    - <span data-ttu-id="d6e64-159">**Asukohaprofiili ID:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-159">**Location profile ID:** *Sort*</span></span>

1. <span data-ttu-id="d6e64-160">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-160">Select **Save**.</span></span>

### <a name="packing-profiles"></a><span data-ttu-id="d6e64-161">Pakkimisprofiilid</span><span class="sxs-lookup"><span data-stu-id="d6e64-161">Packing profiles</span></span>

1. <span data-ttu-id="d6e64-162">Avage jaotis **Laohaldus \> Seadistus \> Pakkimine \> Pakkimisprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-162">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="d6e64-163">Valige toimingupaanil **Uus** ja seejärel seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-163">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="d6e64-164">**Pakkimisprofiili ID:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-164">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="d6e64-165">**Kirjeldus:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-165">**Description:** *Sort*</span></span>
    - <span data-ttu-id="d6e64-166">**Konteineri pakkimise poliitika:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-166">**Container packing policy:** Leave this field blank.</span></span>
    - <span data-ttu-id="d6e64-167">**Konteineri ID-režiim:** *Automaatne*</span><span class="sxs-lookup"><span data-stu-id="d6e64-167">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="d6e64-168">**Konteineri tüüp:** *KAUBAALUS 48X48*</span><span class="sxs-lookup"><span data-stu-id="d6e64-168">**Container type:** *PALLET 48X48*</span></span>
    - <span data-ttu-id="d6e64-169">**Konteineri automaatne loomine konteineri sulgemisel:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-169">**Autocreate container at container close:** Leave this field blank.</span></span>

1. <span data-ttu-id="d6e64-170">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-170">Select **Save**.</span></span>

### <a name="wave-step-codes"></a><span data-ttu-id="d6e64-171">Vooetapi koodid</span><span class="sxs-lookup"><span data-stu-id="d6e64-171">Wave step codes</span></span>

<span data-ttu-id="d6e64-172">Kui lülitasite sisse funktsiooni *Organisatsiooniülene vooetapi kood*, seadistage järgmine kood.</span><span class="sxs-lookup"><span data-stu-id="d6e64-172">If you turned on the *Organization wide wave step code* feature, set up the following code.</span></span>

1. <span data-ttu-id="d6e64-173">Avage jaotis **Laohaldus \> Seadistus \> Vood \> Vooetapi koodid**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-173">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="d6e64-174">Valige toimingupaanil **Uus** ja seejärel seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-174">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="d6e64-175">**Vooetapi kood:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-175">**Wave step code:** *Sort*</span></span>
    - <span data-ttu-id="d6e64-176">**Vooetapi kirjeldus:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-176">**Wave step description:** *Sort*</span></span>
    - <span data-ttu-id="d6e64-177">**Vooetapi tüüp:** *Sortimismall*</span><span class="sxs-lookup"><span data-stu-id="d6e64-177">**Wave step type:** *Sort template*</span></span>

1. <span data-ttu-id="d6e64-178">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-178">Select **Save**.</span></span>

### <a name="outbound-sorting-template"></a><span data-ttu-id="d6e64-179">Väljastuste sortimise mall</span><span class="sxs-lookup"><span data-stu-id="d6e64-179">Outbound sorting template</span></span>

<span data-ttu-id="d6e64-180">Sortimismall juhib seda, kas sortimise asukohad luuakse, milliseid kriteeriume kasutatakse ja muid sortimisprotsessi atribuute.</span><span class="sxs-lookup"><span data-stu-id="d6e64-180">The sorting template controls whether sort positions are created, what criteria are used, and other attributes of the sorting process.</span></span>

1. <span data-ttu-id="d6e64-181">Avage jaotis **Laohaldus \> Seadistus \> Pakkimine \> Väljamineku sortimismallid**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-181">Go to **Warehouse management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="d6e64-182">Sortimismalli loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-182">On the Action Pane, select **New** to create a sorting template.</span></span>
1. <span data-ttu-id="d6e64-183">Määrake uue malli päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-183">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="d6e64-184">**Väljamineku sortimismalli ID:** *Voo sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-184">**Outbound sorting template ID:** *Wave Sort*</span></span>
    - <span data-ttu-id="d6e64-185">**Kirjeldus:** *Voo sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-185">**Description:** *Wave sort*</span></span>
    - <span data-ttu-id="d6e64-186">**Sortimismalli tüüp:** *Voo nõudlus*</span><span class="sxs-lookup"><span data-stu-id="d6e64-186">**Sort template type:** *Wave demand*</span></span>

        <span data-ttu-id="d6e64-187">See väli määratleb protsessi, milleks sortimismalli kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="d6e64-187">This field defines the process that the sorting template is used for.</span></span> <span data-ttu-id="d6e64-188">Saadaval on järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="d6e64-188">The following values are available:</span></span>

        - <span data-ttu-id="d6e64-189">**Voo nõudlus** – sortimismalli kasutatakse protsessi *Pane seinale* puhul.</span><span class="sxs-lookup"><span data-stu-id="d6e64-189">**Wave demand** – The sorting template is used for the *Put to wall* process.</span></span> <span data-ttu-id="d6e64-190">Seda malli tüüpi kasutatakse pakkimisjaama vahelejätmiseks ja varude töötlemiseks otse lainest.</span><span class="sxs-lookup"><span data-stu-id="d6e64-190">This template type is used to bypass the pack station and process inventory directly out of the wave.</span></span> <span data-ttu-id="d6e64-191">Seda tüüpi saate kasutada ainult juhul, kui **sortimise** voo töötlemise meetod on lisatud voo malli.</span><span class="sxs-lookup"><span data-stu-id="d6e64-191">You can use this type only if the **sorting** wave process method is included in the wave template.</span></span>
        - <span data-ttu-id="d6e64-192">**Konteiner** – sortimismalli kasutatakse protsessi *Kaubaaluse loomine pärast pakkimist* jaoks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-192">**Container** – The sorting template is used for the *Pallet building after packing* process.</span></span> <span data-ttu-id="d6e64-193">Seda malli tüüpi kasutatakse nende konteinerite töötlemiseks, mis on selles pakkimisjaamas suletud ja mis tuleb kaubaalustele sortida.</span><span class="sxs-lookup"><span data-stu-id="d6e64-193">This template type is used to process containers that are closed at the pack station and must be sorted onto pallets.</span></span>

    - <span data-ttu-id="d6e64-194">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="d6e64-194">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="d6e64-195">**Asukoht:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-195">**Location:** *Sort*</span></span>

1. <span data-ttu-id="d6e64-196">Määrake kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-196">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d6e64-197">**Sortimise kontrollimine:** *Asukoha skannimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-197">**Sort verification:** *Position scan*</span></span>

        <span data-ttu-id="d6e64-198">See väli määratleb sortimise käigus nõutava kinnitamise.</span><span class="sxs-lookup"><span data-stu-id="d6e64-198">This field defines the verification that is required during sorting.</span></span> <span data-ttu-id="d6e64-199">Saadaval on järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="d6e64-199">The following values are available:</span></span>

        - <span data-ttu-id="d6e64-200">None</span><span class="sxs-lookup"><span data-stu-id="d6e64-200">None</span></span>
        - <span data-ttu-id="d6e64-201">Litsentsiplaadi skannimine</span><span class="sxs-lookup"><span data-stu-id="d6e64-201">License plate scan</span></span>
        - <span data-ttu-id="d6e64-202">Asukoha skannimine</span><span class="sxs-lookup"><span data-stu-id="d6e64-202">Position scan</span></span>

    - <span data-ttu-id="d6e64-203">**Loo töö asukoha sulgemisel:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="d6e64-203">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="d6e64-204">Kui selle suvandi väärtuseks on seatud *Jah*, kui asukoht on suletud, luuakse töö varude lõppsihtkohta teisaldamiseks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-204">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="d6e64-205">Kui väärtuseks on seatud *Ei*, komplekteeritakse varud asukoha sulgemisel kohe tellimusele.</span><span class="sxs-lookup"><span data-stu-id="d6e64-205">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="d6e64-206">**Asukoha määramine:** *Käsitsi*</span><span class="sxs-lookup"><span data-stu-id="d6e64-206">**Position assignment:** *Manual*</span></span>

        <span data-ttu-id="d6e64-207">See väli määratleb asukoha määramise tüübi.</span><span class="sxs-lookup"><span data-stu-id="d6e64-207">This field defines the type of position assignment.</span></span> <span data-ttu-id="d6e64-208">Saadaval on järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="d6e64-208">The following values are available:</span></span>

        - <span data-ttu-id="d6e64-209">**Käsitsi** – kasutaja peab alati näitama, millisesse asukohta varud sortida tuleb.</span><span class="sxs-lookup"><span data-stu-id="d6e64-209">**Manual** – The user must always indicate which position the inventory should be sorted to.</span></span>
        - <span data-ttu-id="d6e64-210">**Automaatne** – süsteem juhib varud võimaluse korral automaatselt asukohta, võttes aluseks sortimismalli jaotamised.</span><span class="sxs-lookup"><span data-stu-id="d6e64-210">**Automatic** – The system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

    - <span data-ttu-id="d6e64-211">**Määra sortimise asukoha kriteeriumid:** *Kasuta ainult tühja asukohta*</span><span class="sxs-lookup"><span data-stu-id="d6e64-211">**Assign sort position criteria:** *Only use empty position*</span></span>

        <span data-ttu-id="d6e64-212">See väli juhib, kas nõudluse jaoks asukoha määramisel võetakse sortimise asukohtades juba olemasolevaid varusid arvesse.</span><span class="sxs-lookup"><span data-stu-id="d6e64-212">This field controls whether inventory that is already present on sort positions is taken into account when a position is assigned for the demand.</span></span> <span data-ttu-id="d6e64-213">Saadaval on järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="d6e64-213">The following values are available:</span></span>

        - <span data-ttu-id="d6e64-214">**Kasuta ainult tühja asukohta** – arvesse võetakse asukohti, millel on juba nendega seostatud varusid</span><span class="sxs-lookup"><span data-stu-id="d6e64-214">**Only use empty position** – Positions that already have inventory associated with them will be taken into account</span></span>
        - <span data-ttu-id="d6e64-215">**Eelda tühja asukohta** – mis tahes varusid, mis on juba asukohas, eiratakse määramise käigus.</span><span class="sxs-lookup"><span data-stu-id="d6e64-215">**Assume position empty** – Any inventory that is already on the position will be disregarded during assignment.</span></span> <span data-ttu-id="d6e64-216">Kasutatakse kõiki saadaolevaid asukohti.</span><span class="sxs-lookup"><span data-stu-id="d6e64-216">All available positions will be used.</span></span>

    - <span data-ttu-id="d6e64-217">**Vooetapi kood:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-217">**Wave step code:** *Sort*</span></span>

        <span data-ttu-id="d6e64-218">Kui funktsioon *Organisatsiooniülene vooetapi kood* on sisse lülitatud, peab vooetapi kood *Sortimine* olema samuti seadistatud vooetapi koodides.</span><span class="sxs-lookup"><span data-stu-id="d6e64-218">If the *Organization wide wave step code* feature is turned on, the *Sort* wave step code must also be set up in wave step codes.</span></span>

    - <span data-ttu-id="d6e64-219">**Sortimise asukoha automaatne sulgemine:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="d6e64-219">**Auto close sort position:** *Yes*</span></span>

        <span data-ttu-id="d6e64-220">Selle suvandi väärtuseks on seatud *Jah*, suletakse sortimise asukoht automaatselt, kui kõik asukohta tulevad tööd on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="d6e64-220">If this option is set to *Yes*, the sort position will automatically be closed when all work that comes to the position has been completed.</span></span>

    - <span data-ttu-id="d6e64-221">**Sortimise asukohtade arv:** *3*</span><span class="sxs-lookup"><span data-stu-id="d6e64-221">**Number of sort positions:** *3*</span></span>

        <span data-ttu-id="d6e64-222">See väli määratleb süsteemi loodavate sortimise asukohtade maksimaalse arvu.</span><span class="sxs-lookup"><span data-stu-id="d6e64-222">This field defines the maximum number of sort positions that the system will create.</span></span>

    - <span data-ttu-id="d6e64-223">**Sortimise asukoha eesliide:** *SP-*</span><span class="sxs-lookup"><span data-stu-id="d6e64-223">**Sort position prefix:** *SP-*</span></span>

        <span data-ttu-id="d6e64-224">See väli määratleb eesliite, mille süsteem määrab enne asukoha numbrit.</span><span class="sxs-lookup"><span data-stu-id="d6e64-224">This field defines the prefix that the system assigns before the position number.</span></span>

    - <span data-ttu-id="d6e64-225">**Sortimise asukoha automaatne pakkimine:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="d6e64-225">**Auto pack sort position:** *Yes*</span></span>

        <span data-ttu-id="d6e64-226">Kui selle suvandi väärtuseks on määratud *Jah*, pakitakse sortimise asukoha varud konteinerisse, kui asukoht on suletud.</span><span class="sxs-lookup"><span data-stu-id="d6e64-226">If this option is set to *Yes*, the inventory on the sort position will be packed into a container when the position is closed.</span></span>

    - <span data-ttu-id="d6e64-227">**Pakkimisprofiili ID:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-227">**Packing profile ID:** *Sort*</span></span>

        <span data-ttu-id="d6e64-228">See väli määratsel pakkimisprofiili, mida kasutatakse, kui sortimise asukoht pakitakse konteinerisse.</span><span class="sxs-lookup"><span data-stu-id="d6e64-228">This field defines the packing profile that will be used when the sort position is packed into a container.</span></span>

1. <span data-ttu-id="d6e64-229">Valige toimingupaanil **Redigeeri päringut** selle sortimismalli puhul kasutatavate kriteeriumide määramiseks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-229">On the Action Pane, select **Edit query** to specify the criteria that are used for this sorting template.</span></span>
1. <span data-ttu-id="d6e64-230">Valige päringu dialoogiboksis vahekaardil **Sortimine** suvand **Uus**, et lisada rida ja määrake siis järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-230">In the query dialog box, on the **Sorting** tab, select **New** to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="d6e64-231">**Tabel:** *Koormuse üksikasjad*</span><span class="sxs-lookup"><span data-stu-id="d6e64-231">**Table:** *Load details*</span></span>
    - <span data-ttu-id="d6e64-232">**Tuletatud tabel:** *Koormuse üksikasjad*</span><span class="sxs-lookup"><span data-stu-id="d6e64-232">**Derived table:** *Load details*</span></span>
    - <span data-ttu-id="d6e64-233">**Väli:** *Saadetise ID*</span><span class="sxs-lookup"><span data-stu-id="d6e64-233">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="d6e64-234">**Otsingusuund:** *Kasvav*</span><span class="sxs-lookup"><span data-stu-id="d6e64-234">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="d6e64-235">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-235">Select **OK**.</span></span>
1. <span data-ttu-id="d6e64-236">Teile võidakse kuvada järgmine teade: „Grupeerimine lähtestatakse, kas soovite jätkata?”</span><span class="sxs-lookup"><span data-stu-id="d6e64-236">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="d6e64-237">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-237">Select **Yes**.</span></span>

    <span data-ttu-id="d6e64-238">Toimingupaani nupp **Väljamineku sortimismalli piirid** muutub kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-238">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="d6e64-239">Valige toimingupaanil **Väljamineku sortimismalli piirid**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-239">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="d6e64-240">Märkige ruut **Grupeeri välja alusel**, et grupeerida saadetise ID alusel.</span><span class="sxs-lookup"><span data-stu-id="d6e64-240">Select the **Group by field** check box to group by shipment ID.</span></span>

    <span data-ttu-id="d6e64-241">Selle sättega luuakse üks sortimise asukoht saadetise kohta, milleks on voos olev konteiner.</span><span class="sxs-lookup"><span data-stu-id="d6e64-241">This setting will create one sort position per shipment that is a container in the wave.</span></span>

1. <span data-ttu-id="d6e64-242">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-242">Select **OK**.</span></span>

### <a name="wave-process-methods"></a><span data-ttu-id="d6e64-243">Voo töötlemise meetodid</span><span class="sxs-lookup"><span data-stu-id="d6e64-243">Wave process methods</span></span>

1. <span data-ttu-id="d6e64-244">Avage jaotis **Laohaldus \> Seadistus \> Vood \> Voo protsessi meetodid**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-244">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="d6e64-245">Valige toimingupaanil suvand **Meetodite uuesti loomine**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-245">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="d6e64-246">**Sortimise** meetod lisatakse saadaolevate meetodite loendisse ja sellele valitakse voo malli tüüp *Lähetamine*.</span><span class="sxs-lookup"><span data-stu-id="d6e64-246">The **sorting** method is added to the list of available methods, and the *Shipping* wave template type is selected for it.</span></span>

### <a name="wave-templates"></a><span data-ttu-id="d6e64-247">Voomallid</span><span class="sxs-lookup"><span data-stu-id="d6e64-247">Wave templates</span></span>

<span data-ttu-id="d6e64-248">Redigeerige voo nõudluse sortimiseks kasutatavat voo malli.</span><span class="sxs-lookup"><span data-stu-id="d6e64-248">Edit the wave template that is used for wave demand sorting.</span></span>

1. <span data-ttu-id="d6e64-249">Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-249">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="d6e64-250">Valige väljal **Voo malli tüüp** suvand *Lähetamine*.</span><span class="sxs-lookup"><span data-stu-id="d6e64-250">In the **Wave template type** field, select *Shipping*.</span></span>
1. <span data-ttu-id="d6e64-251">Valige olemasolev mall **62 saadetise vaikemall**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-251">Select the existing **62 Shipping default** template.</span></span>
1. <span data-ttu-id="d6e64-252">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-252">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="d6e64-253">Tehke kiirkaardil **Üldine** järgmised muudatused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-253">On the **General** FastTab, make the following changes:</span></span>

    - <span data-ttu-id="d6e64-254">Määrake suvandi **Töötle voogu lattu vabastamisel** väärtuseks *Ei*.</span><span class="sxs-lookup"><span data-stu-id="d6e64-254">Set the **Process wave at release to warehouse** option to *No*.</span></span>
    - <span data-ttu-id="d6e64-255">Määrake suvandi **Määra avatud voogudele** väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="d6e64-255">Set the **Assign to open waves** option to *Yes*.</span></span>

1. <span data-ttu-id="d6e64-256">Seadistage kiirkaardil **Meetodid** meetod **Sortimine**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-256">On the **Methods** FastTab, set up the **sorting** method:</span></span>

    1. <span data-ttu-id="d6e64-257">Valige ruudustikus **Ülejäänud meetodid** suvand **sortimine**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-257">In the **Remaining Methods** grid, select **sorting**.</span></span>
    2. <span data-ttu-id="d6e64-258">Valige meetodi **sortimine** ruudustikku **Valitud meetodid** teisaldamiseks paremnoole nupp.</span><span class="sxs-lookup"><span data-stu-id="d6e64-258">Select the right arrow button to move **sorting** to the **Selected Methods** grid.</span></span>
    3. <span data-ttu-id="d6e64-259">Valige ruudustikus **Valitud meetodid** suvand **sortimine**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-259">In the **Selected Methods** grid, select **sorting**.</span></span>
    4. <span data-ttu-id="d6e64-260">Seadke välja **Vooetapi kood** väärtuseks *sortimine*.</span><span class="sxs-lookup"><span data-stu-id="d6e64-260">Set the **Wave step code** field to *Sort*.</span></span>

1. <span data-ttu-id="d6e64-261">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-261">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="d6e64-262">Mobiilse seadme menüü-üksused</span><span class="sxs-lookup"><span data-stu-id="d6e64-262">Mobile device menu items</span></span>

1. <span data-ttu-id="d6e64-263">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-263">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="d6e64-264">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-264">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d6e64-265">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-265">In the header, set the following values:</span></span>

    - <span data-ttu-id="d6e64-266">**Menüü-üksuse nimi:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-266">**Menu item name:** *Sort*</span></span>
    - <span data-ttu-id="d6e64-267">**Pealkiri:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-267">**Title:** *Sort*</span></span>
    - <span data-ttu-id="d6e64-268">**Režiim:** *Kaudne*</span><span class="sxs-lookup"><span data-stu-id="d6e64-268">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="d6e64-269">**Kasuta olemasolevat tööd:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="d6e64-269">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="d6e64-270">Määrake kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-270">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d6e64-271">**Tegevuse kood:** *Väljamineku sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-271">**Activity code:** *Outbound sorting*</span></span>
    - <span data-ttu-id="d6e64-272">**Protsessijuhendi kasutamine:** *Jah* (vaikeväärtus)</span><span class="sxs-lookup"><span data-stu-id="d6e64-272">**Use process guide:** *Yes* (default value)</span></span>
    - <span data-ttu-id="d6e64-273">**Väljamineku sortimismalli ID:** *Voo sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-273">**Outbound sorting template ID:** *Wave Sort*</span></span>

1. <span data-ttu-id="d6e64-274">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-274">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="d6e64-275">Mobiilse seadme menüü</span><span class="sxs-lookup"><span data-stu-id="d6e64-275">Mobile device menu</span></span>

1. <span data-ttu-id="d6e64-276">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-276">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="d6e64-277">Valige menüüde loendist suvand **Väljaminev**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-277">In the list of menus, select **Outbound**.</span></span>
1. <span data-ttu-id="d6e64-278">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-278">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="d6e64-279">Otsige üles ja valige ruudustikust **Saadaolevad menüüd ja menüü-üksused** äsja loodud menüü-üksus **Sortimine**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-279">In the **Available Menus And Menu Items** grid, find and select the **Sort** menu item that you just created.</span></span>
1. <span data-ttu-id="d6e64-280">Valige paremnoole nupp, et teisaldada **Sortimine** ruudustikku **Menüü struktuur**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-280">Select the right arrow button to move **Sort** to the **Menu Structure** grid.</span></span> <span data-ttu-id="d6e64-281">Sedasi saate lisada menüü-üksuse menüüsse **Väljaminev**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-281">In this way, you add the menu item to the **Outbound** menu.</span></span>
1. <span data-ttu-id="d6e64-282">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-282">Select **Save**.</span></span>

### <a name="location-directives"></a><span data-ttu-id="d6e64-283">Asukohakorraldus</span><span class="sxs-lookup"><span data-stu-id="d6e64-283">Location directives</span></span>

<span data-ttu-id="d6e64-284">Pärast sortimise lõpule viimist loodud töö suunamiseks peate looma asukohakorraldused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-284">You must create location directives to guide the work that is created after the sorting is completed.</span></span>

1. <span data-ttu-id="d6e64-285">Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-285">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d6e64-286">Valige väljal **Töökäsu tüüp** suvand *Sorditud varude komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="d6e64-286">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="d6e64-287">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-287">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d6e64-288">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-288">In the header, set the following values:</span></span>

    - <span data-ttu-id="d6e64-289">**Järjestus:** *1*</span><span class="sxs-lookup"><span data-stu-id="d6e64-289">**Sequence:** *1*</span></span>
    - <span data-ttu-id="d6e64-290">**Nimi:** *Pane laadimisukse juurde*</span><span class="sxs-lookup"><span data-stu-id="d6e64-290">**Name:** *Put to Baydoor*</span></span>

1. <span data-ttu-id="d6e64-291">Määrake kiirkaardil **Asukohakorraldused** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-291">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="d6e64-292">**Töö tüüp:** *Ladustamine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-292">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d6e64-293">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="d6e64-293">**Site:** *6*</span></span>
    - <span data-ttu-id="d6e64-294">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="d6e64-294">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="d6e64-295">**Korralduse kood:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-295">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="d6e64-296">**Mitu SKU-d:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="d6e64-296">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="d6e64-297">Valige **Salvesta**, et muuta kiirkaart **Read** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-297">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="d6e64-298">Valige kiirkaardil **Read** suvand **Uus** ja seejärel seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-298">On the **Lines** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="d6e64-299">Võtke vastu kõigi teiste väljade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-299">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="d6e64-300">**Järjekorranumber:** *1*</span><span class="sxs-lookup"><span data-stu-id="d6e64-300">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d6e64-301">**Alates kogusest:** *0*</span><span class="sxs-lookup"><span data-stu-id="d6e64-301">**From quantity:** *0*</span></span>
    - <span data-ttu-id="d6e64-302">**Koguseni:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="d6e64-302">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="d6e64-303">Valige **Salvesta**, et muuta kiirkaart **Asukohakorralduse toimingud** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-303">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="d6e64-304">Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus** ja seejärel seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-304">On the **Location Directive Actions** FastTab, select **New**, and then set the following values.</span></span> <span data-ttu-id="d6e64-305">Võtke vastu kõigi teiste väljade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-305">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="d6e64-306">**Järjekorranumber:** *1*</span><span class="sxs-lookup"><span data-stu-id="d6e64-306">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="d6e64-307">**Nimi:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="d6e64-307">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="d6e64-308">Valige **Salvesta**, et muuta kiirkaardi **Asukohakorralduse toimingud** nupp **Päringu redigeerimine** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-308">Select **Save** to make the **Edit query** button on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="d6e64-309">Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-309">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="d6e64-310">Otsige päringu dialoogiboksi vahekaardil **Vahemik** üles rida, kus välja **Väli** väärtuseks on seatud *Asukoht*.</span><span class="sxs-lookup"><span data-stu-id="d6e64-310">In the query dialog box, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="d6e64-311">Määrake selle rea välja **Kriteeriumid** väärtuseks *Baydoor*.</span><span class="sxs-lookup"><span data-stu-id="d6e64-311">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="d6e64-312">Valige redigeerimise kinnitamiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-312">Select **OK** to confirm the edit.</span></span>

### <a name="work-classes"></a><span data-ttu-id="d6e64-313">Töö klassid</span><span class="sxs-lookup"><span data-stu-id="d6e64-313">Work classes</span></span>

1. <span data-ttu-id="d6e64-314">Minge jaotisse **Laohaldus \> Seadistus \> Töö \> Töö klassid**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-314">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="d6e64-315">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-315">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d6e64-316">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-316">In the header, set the following values:</span></span>

    - <span data-ttu-id="d6e64-317">**Töö klassi ID:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-317">**Work class ID:** *Sorting*</span></span>
    - <span data-ttu-id="d6e64-318">**Kirjeldus:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-318">**Description:** *Sorting*</span></span>
    - <span data-ttu-id="d6e64-319">**Töötellimuse tüüp:** *Sorditud varude komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-319">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="d6e64-320">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-320">Select **Save**.</span></span>

### <a name="work-templates"></a><span data-ttu-id="d6e64-321">Töömallid</span><span class="sxs-lookup"><span data-stu-id="d6e64-321">Work templates</span></span>

1. <span data-ttu-id="d6e64-322">Avage jaotis **Laohaldus \> Töö \> Töömallid**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-322">Go to **Warehouse management \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="d6e64-323">Valige väljal **Töökäsu tüüp** suvand *Müügitellimused*.</span><span class="sxs-lookup"><span data-stu-id="d6e64-323">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="d6e64-324">Valige ruudustikus töömall **62 pakkimiseks komplekteerimine**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-324">In the grid, select the **62 Pick to pack** work template.</span></span>
1. <span data-ttu-id="d6e64-325">Valige toimingupaanilt suvand **Tööpäise piirid**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-325">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="d6e64-326">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-326">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="d6e64-327">Tühjendage real, kus välja **Välja nimi** väärtuseks on seatud *Saadetise ID*, märkeruut **Grupeeri selle välja alusel**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-327">On the line where the **Field name** field is set to *Shipment ID*, clear the **Group by this field** check box.</span></span>
1. <span data-ttu-id="d6e64-328">Valige **Salvesta** ja seejärel sulgege dialoogiboks **Tööpäise piirid**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-328">Select **Save**, and then close the **Work header breaks** dialog box.</span></span>
1. <span data-ttu-id="d6e64-329">Valige väljal **Töökäsu tüüp** suvand *Sorditud varude komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="d6e64-329">In the **Work order type** field, select *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="d6e64-330">Valige töömalli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-330">Select **New** to create a work template.</span></span>
1. <span data-ttu-id="d6e64-331">Määrake jaotises **Ülevaade** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-331">In the **Overview** section, set the following values.</span></span> <span data-ttu-id="d6e64-332">Võtke vastu kõigi teiste väljade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-332">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="d6e64-333">**Töömall:** *Sorditud komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-333">**Work template:** *Sorted picking*</span></span>
    - <span data-ttu-id="d6e64-334">**Töömalli kirjeldus:** *Sorditud komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-334">**Work template description:** *Sorted picking*</span></span>

1. <span data-ttu-id="d6e64-335">Valige **Salvesta**, et muuta jaotis **Töömalli üksikasjad** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-335">Select **Save** to make the **Work Template Details** section available.</span></span>
1. <span data-ttu-id="d6e64-336">Loote kaks rida jaotises **Töömalli üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-336">In the **Work Template Details** section, you will create two lines.</span></span> <span data-ttu-id="d6e64-337">Valige **Uus** ja seejärel seadke järgmised väärtused 1. rea jaoks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-337">Select **New**, and then set the following values for line 1:</span></span>

    - <span data-ttu-id="d6e64-338">**Töö tüüp:** *Komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-338">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="d6e64-339">**Kohustuslik:** valitud (= *Jah*)</span><span class="sxs-lookup"><span data-stu-id="d6e64-339">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="d6e64-340">**Töö klassi ID:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-340">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="d6e64-341">Valige **Uus** uuesti ja seejärel seadke järgmised väärtused 2. rea jaoks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-341">Select **New** again, and then set the following values for line 2:</span></span>

    - <span data-ttu-id="d6e64-342">**Töö tüüp:** *Ladustamine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-342">**Work type:** *Put*</span></span>
    - <span data-ttu-id="d6e64-343">**Kohustuslik:** valitud (= *Jah*)</span><span class="sxs-lookup"><span data-stu-id="d6e64-343">**Mandatory:** Selected (= *Yes*)</span></span>
    - <span data-ttu-id="d6e64-344">**Töö klassi ID:** *Sortimine*</span><span class="sxs-lookup"><span data-stu-id="d6e64-344">**Work class ID:** *Sorting*</span></span>

1. <span data-ttu-id="d6e64-345">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-345">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="d6e64-346">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="d6e64-346">Example scenario</span></span>

<span data-ttu-id="d6e64-347">See stsenaarium simuleerib olukorda, kus ladu talletab asukohtades väikeseid kaupasid ja peab need enne lähetamist kastidesse pakkima, kuid pakkimisjaama funktsioon ei ole sobilik.</span><span class="sxs-lookup"><span data-stu-id="d6e64-347">This scenario simulates a situation where the warehouse stores small items in locations and must pack them into boxes before they are shipped, and where packing station functionality isn't really suitable.</span></span> <span data-ttu-id="d6e64-348">Komplekteerimise kiiruse suurendamiseks komplekteerivad töötajad mitme kliendi ja erinevate aadressidega tellimusi üheaegselt.</span><span class="sxs-lookup"><span data-stu-id="d6e64-348">Workers pick orders for multiple customers and different addresses at the same time to increase the picking speed.</span></span> <span data-ttu-id="d6e64-349">Kui komplekteerimine on lõpule viidud, saabuvad töötajad sorteerimise asukohta, kus komplekteeritud kaubad sorditakse nõutavate kriteeriumide alusel õigesse kasti.</span><span class="sxs-lookup"><span data-stu-id="d6e64-349">After picking has been completed, the workers arrive at the sorting location, where the picked items can be sorted to the correct box, based on required criteria.</span></span> <span data-ttu-id="d6e64-350">Selles näites kasutatakse saadetise ID-d õige kasti määratlemiseks, kuna igal saadetisel on erinev aadress.</span><span class="sxs-lookup"><span data-stu-id="d6e64-350">In this example, the shipment ID will be used to determine the correct box, because each shipment has a different address.</span></span> <span data-ttu-id="d6e64-351">Kui koormuse kõik kaubad on pakitud ja sorditud saadetise järgi, teisaldatakse kastid vaheasukohta ja lõpuks laaditakse veokile.</span><span class="sxs-lookup"><span data-stu-id="d6e64-351">After all items from the load are packed and sorted by shipment, the boxes will be moved to the staging area and eventually loaded onto a truck.</span></span>

<span data-ttu-id="d6e64-352">Enne stsenaariumi käivitamist veenduge, et kõik standardsed ladustamise funktsioonid oleksid teie laos õigesti seadistatud.</span><span class="sxs-lookup"><span data-stu-id="d6e64-352">Before you start the scenario, make sure that all standard warehouse functionality is set up correctly for your warehouse.</span></span> <span data-ttu-id="d6e64-353">Sellel otstarbel kasutatakse standardset Contoso ladu *62*.</span><span class="sxs-lookup"><span data-stu-id="d6e64-353">Standard Contoso warehouse *62* is used for this purpose.</span></span> <span data-ttu-id="d6e64-354">Standardseid konfiguratsioone pole muudetud, peale selle, mida kirjeldatakse häälestuses.</span><span class="sxs-lookup"><span data-stu-id="d6e64-354">Standard configurations haven't been changed, besides what is described in the setup.</span></span>

### <a name="create-demand"></a><span data-ttu-id="d6e64-355">Nõudluse loomine</span><span class="sxs-lookup"><span data-stu-id="d6e64-355">Create demand</span></span>

<span data-ttu-id="d6e64-356">Enne selle funktsiooni demonstreerimist peate looma mõne nõudluse.</span><span class="sxs-lookup"><span data-stu-id="d6e64-356">Before the functionality can be demonstrated, you must create some demand.</span></span> <span data-ttu-id="d6e64-357">Selles stsenaariumis loote kolm müügitellimust kolme erineva kliendi jaoks erinevate tarneaadresside simuleerimiseks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-357">For this scenario, you will create three sales orders for three different customers to simulate different delivery addresses.</span></span> <span data-ttu-id="d6e64-358">Sedasi loote kolm eraldi saadetist.</span><span class="sxs-lookup"><span data-stu-id="d6e64-358">In this way, you will create three separate shipments.</span></span>

<span data-ttu-id="d6e64-359">Enne müügitellimuste ja saadetiste loomist veenduge, et komplekteerimise asukohtadel oleks tellimuste kõikide kaupade jaoks piisavalt varusid.</span><span class="sxs-lookup"><span data-stu-id="d6e64-359">Before you create sales orders and shipments, make sure that the pick locations have enough inventory for all the items on the orders.</span></span> <span data-ttu-id="d6e64-360">Vaadake üle asukohakorralduse seadistused, et kinnitada müügitellimuse komplekteerimiseks kasutatavad komplekteerimise asukohad.</span><span class="sxs-lookup"><span data-stu-id="d6e64-360">Review the location directive settings to confirm the picking locations that are used for sales order picking.</span></span> <span data-ttu-id="d6e64-361">Kui peate korrigeerima varusid, saate luua käsitsi liikumisi, kasutada täiendamist või kasutada mis tahes muud voogu.</span><span class="sxs-lookup"><span data-stu-id="d6e64-361">If you must adjust the inventory, you can create manual movements, use replenishment, or use any other flow.</span></span> <span data-ttu-id="d6e64-362">Seejärel reserveerige varud.</span><span class="sxs-lookup"><span data-stu-id="d6e64-362">Then reserve the inventory.</span></span>

1. <span data-ttu-id="d6e64-363">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-363">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d6e64-364">1 tellimuse müügitellimuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-364">Select **New** to create a sales order for order 1.</span></span>
1. <span data-ttu-id="d6e64-365">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-365">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d6e64-366">**Klient:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="d6e64-366">**Customer:** *US-001*</span></span>
    - <span data-ttu-id="d6e64-367">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="d6e64-367">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="d6e64-368">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-368">Select **OK**.</span></span>
1. <span data-ttu-id="d6e64-369">Kiirkaardile **Müügitellimuse read** lisatakse uus rida.</span><span class="sxs-lookup"><span data-stu-id="d6e64-369">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d6e64-370">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-370">Set the following values:</span></span>

    - <span data-ttu-id="d6e64-371">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d6e64-371">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d6e64-372">**Kogus:** *5*</span><span class="sxs-lookup"><span data-stu-id="d6e64-372">**Quantity:** *5*</span></span>

1. <span data-ttu-id="d6e64-373">Valige **Lisa rida**, et lisada teine rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-373">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="d6e64-374">**Kauba kood:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="d6e64-374">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="d6e64-375">**Kogus:** *10*</span><span class="sxs-lookup"><span data-stu-id="d6e64-375">**Quantity:** *10*</span></span>

1. <span data-ttu-id="d6e64-376">Korrake järgmisi etappe iga müügirea puhul, et reserveerida selle jaoks varud.</span><span class="sxs-lookup"><span data-stu-id="d6e64-376">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="d6e64-377">Valige ruudustiku kohal oleva menüü **Varud** kiirkaardilt **Müügitellimuse read** suvand **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-377">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="d6e64-378">Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii** ja seejärel sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d6e64-378">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="d6e64-379">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-379">Select **Save**.</span></span>

1. <span data-ttu-id="d6e64-380">2 tellimuse müügitellimuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-380">Select **New** to create a sales order for order 2.</span></span>
1. <span data-ttu-id="d6e64-381">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-381">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d6e64-382">**Klient:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="d6e64-382">**Customer:** *US-004*</span></span>
    - <span data-ttu-id="d6e64-383">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="d6e64-383">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="d6e64-384">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-384">Select **OK**.</span></span>
1. <span data-ttu-id="d6e64-385">Kiirkaardile **Müügitellimuse read** lisatakse uus rida.</span><span class="sxs-lookup"><span data-stu-id="d6e64-385">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d6e64-386">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-386">Set the following values:</span></span>

    - <span data-ttu-id="d6e64-387">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d6e64-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d6e64-388">**Kogus:** *7*</span><span class="sxs-lookup"><span data-stu-id="d6e64-388">**Quantity:** *7*</span></span>

1. <span data-ttu-id="d6e64-389">Valige **Lisa rida**, et lisada teine rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-389">Select **Add line** to add a second line, and set the following values:</span></span>

    - <span data-ttu-id="d6e64-390">**Kauba kood:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="d6e64-390">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="d6e64-391">**Kogus:** *3*</span><span class="sxs-lookup"><span data-stu-id="d6e64-391">**Quantity:** *3*</span></span>

1. <span data-ttu-id="d6e64-392">Korrake järgmisi etappe iga müügirea puhul, et reserveerida selle jaoks varud.</span><span class="sxs-lookup"><span data-stu-id="d6e64-392">Repeat the following steps for each sales line on the order to reserve inventory for it:</span></span>

    1. <span data-ttu-id="d6e64-393">Valige ruudustiku kohal oleva menüü **Varud** kiirkaardilt **Müügitellimuse read** suvand **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-393">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="d6e64-394">Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii** ja seejärel sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d6e64-394">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="d6e64-395">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-395">Select **Save**.</span></span>

1. <span data-ttu-id="d6e64-396">3 tellimuse müügitellimuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-396">Select **New** to create a sales order for order 3.</span></span>
1. <span data-ttu-id="d6e64-397">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-397">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d6e64-398">**Klient:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="d6e64-398">**Customer:** *US-007*</span></span>
    - <span data-ttu-id="d6e64-399">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="d6e64-399">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="d6e64-400">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-400">Select **OK**.</span></span>
1. <span data-ttu-id="d6e64-401">Kiirkaardile **Müügitellimuse read** lisatakse uus rida.</span><span class="sxs-lookup"><span data-stu-id="d6e64-401">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d6e64-402">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d6e64-402">Set the following values:</span></span>

    - <span data-ttu-id="d6e64-403">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d6e64-403">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d6e64-404">**Kogus:** *8*</span><span class="sxs-lookup"><span data-stu-id="d6e64-404">**Quantity:** *8*</span></span>

1. <span data-ttu-id="d6e64-405">Müügirea varude reserveerimiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="d6e64-405">Follow these steps to reserve inventory for the sales line:</span></span>

    1. <span data-ttu-id="d6e64-406">Valige ruudustiku kohal oleva menüü **Varud** kiirkaardilt **Müügitellimuse read** suvand **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-406">On the **Sales order lines** FastTab, on the **Inventory** menu, select **Reservation**.</span></span>
    1. <span data-ttu-id="d6e64-407">Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii** ja seejärel sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d6e64-407">On the **Reservation** page, select **Reserve lot**, and then close the page.</span></span>
    1. <span data-ttu-id="d6e64-408">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-408">Select **Save**.</span></span>

<span data-ttu-id="d6e64-409">Viige lõpule järgmine protseduur, et vabastada kõik müügitellimused lattu.</span><span class="sxs-lookup"><span data-stu-id="d6e64-409">Complete the following procedure to release each sales order to the warehouse.</span></span> <span data-ttu-id="d6e64-410">Luuakse kolm erinevat saadetist.</span><span class="sxs-lookup"><span data-stu-id="d6e64-410">Three different shipments will be created.</span></span> <span data-ttu-id="d6e64-411">Seejärel saate lisada kõik kolm saadetist ühte uude voogu.</span><span class="sxs-lookup"><span data-stu-id="d6e64-411">You will then add all three shipments to one new wave.</span></span>

1. <span data-ttu-id="d6e64-412">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-412">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d6e64-413">Valige ruudustikus esimene enda loodud müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="d6e64-413">In the grid, select the first sales order that you created.</span></span>
1. <span data-ttu-id="d6e64-414">Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-414">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="d6e64-415">Saate teabesõnumi, mis näitab loodud voo ID-d ja saadetise ID-d.</span><span class="sxs-lookup"><span data-stu-id="d6e64-415">You receive an informational message that shows the wave ID and shipment ID that were created.</span></span>

1. <span data-ttu-id="d6e64-416">Korrake eelmisi etappe, et vabastada 2. ja 3. müügitellimus lattu.</span><span class="sxs-lookup"><span data-stu-id="d6e64-416">Repeat the previous steps to release sales orders 2 and 3 to the warehouse.</span></span> <span data-ttu-id="d6e64-417">Pange tähele, et saadud teabesõnum näitab, et saadetis on lisatud voogu, mis loodi 1. müügitellimuse väljastamisel.</span><span class="sxs-lookup"><span data-stu-id="d6e64-417">Notice that the informational message that you receive indicates that a shipment has been added to the wave that was created when you released sales order 1.</span></span>
1. <span data-ttu-id="d6e64-418">Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-418">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="d6e64-419">Valige voo ID, mis loodi müügitellimuse väljastamisel, et avada leht **Vood**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-419">Select the wave ID that was created from the release of the sales orders to open the **Waves** page.</span></span> <span data-ttu-id="d6e64-420">Sellel lehel kuvatakse voo üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="d6e64-420">This page shows the wave details.</span></span> <span data-ttu-id="d6e64-421">Kiirkaardil **Voo read** kuvatakse loodud saadetised.</span><span class="sxs-lookup"><span data-stu-id="d6e64-421">The **Wave lines** FastTab shows the shipments that were created.</span></span>

    <span data-ttu-id="d6e64-422">Nüüd peate looma töö, et teisaldada kaubad komplekteerimise asukohtadest sortimise asukohta.</span><span class="sxs-lookup"><span data-stu-id="d6e64-422">You must now create work to bring items from the picking locations to the sorting location.</span></span>

1. <span data-ttu-id="d6e64-423">Klõpsake toimingupaanil suvandit **Töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-423">On the Action Pane, select **Process**.</span></span>

    <span data-ttu-id="d6e64-424">Voo töötlemisel kasutab sortimise meetod sortimismalli varude määrmiseks sortimise asukohtadesse.</span><span class="sxs-lookup"><span data-stu-id="d6e64-424">During wave processing, the sorting method will use the sorting template to assign the inventory to sort positions.</span></span> <span data-ttu-id="d6e64-425">Kui voo töötlemine on lõpule viidud, kuvatakse teabesõnum, mis teatab, et voog on sisestatud ja töö on loodud.</span><span class="sxs-lookup"><span data-stu-id="d6e64-425">When wave processing is completed, you receive an informational message that states that the wave has been posted and work has been created.</span></span>

1. <span data-ttu-id="d6e64-426">Valige toimingupaani vahekaardi **Voog** grupis **Seotud teave** suvand **Töö**, et kuvada loodud tööd.</span><span class="sxs-lookup"><span data-stu-id="d6e64-426">On the Action Pane, on the **Wave** tab, in the **Related information** group, select **Work** to view the work that was created.</span></span> <span data-ttu-id="d6e64-427">Märkige üles töö ID.</span><span class="sxs-lookup"><span data-stu-id="d6e64-427">Make a note of the work ID.</span></span>
1. <span data-ttu-id="d6e64-428">Avage jaotis **Laohaldus \> Pakkimine ja konteinerisse määramine \> Väljamineku sortimise asukoha määramised**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-428">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="d6e64-429">Vasakpoolses veerus saate kuvada iga saadetise jaoks loodud väljamineku sortimise asukohta.</span><span class="sxs-lookup"><span data-stu-id="d6e64-429">In the left column, you can view the outbound sorting position that was created for each shipment.</span></span>
1. <span data-ttu-id="d6e64-430">Kiirkaardil **Sortimise asukoha kriteeriumid** saate kuvada selle asukoha saadetise ID-d.</span><span class="sxs-lookup"><span data-stu-id="d6e64-430">On the **Sort position criteria** FastTab, you can view the shipment ID for that position.</span></span>

<span data-ttu-id="d6e64-431">Loodi üks töö ID, et teisaldada varud komplekteerimise asukohtadest sortimise asukohta.</span><span class="sxs-lookup"><span data-stu-id="d6e64-431">One work ID has been created to bring inventory from the picking locations to the sorting location.</span></span> <span data-ttu-id="d6e64-432">Töö lõpule viimiseks vajate töö ID-d, mis loodi voo töötlemisel.</span><span class="sxs-lookup"><span data-stu-id="d6e64-432">To complete the work, you will need the work ID that was created during wave processing.</span></span>

### <a name="sales-order-picking-to-the-sorting-location"></a><span data-ttu-id="d6e64-433">Müügitellimuse komplekteerimine sortimise asukohta</span><span class="sxs-lookup"><span data-stu-id="d6e64-433">Sales order picking to the sorting location</span></span>

1. <span data-ttu-id="d6e64-434">Logige mobiilirakendusse lao *62* töötajana sisse.</span><span class="sxs-lookup"><span data-stu-id="d6e64-434">Sign in to the mobile app as a worker in warehouse *62*.</span></span>
1. <span data-ttu-id="d6e64-435">Valige peamenüüs suvand **Väljaminev**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-435">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="d6e64-436">Valige menüüs **Väljaminev** suvand **Müügi komplekteerimine**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-436">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="d6e64-437">Valige väli **ID** ja seejärel sisestage voo töötlemisest pärineva töö ID.</span><span class="sxs-lookup"><span data-stu-id="d6e64-437">Select the **ID** field, and then enter the work ID from the wave processing.</span></span>
1. <span data-ttu-id="d6e64-438">Kinnitage kirje.</span><span class="sxs-lookup"><span data-stu-id="d6e64-438">Confirm your entry.</span></span>

    <span data-ttu-id="d6e64-439">Järgmisena palutakse teil sisestada sihtidentifitseerimisnumber (LP).</span><span class="sxs-lookup"><span data-stu-id="d6e64-439">Next, you're prompted to enter a target license plate (LP).</span></span> <span data-ttu-id="d6e64-440">Pange tähele, et 1. müügitellimuse 1. rida tuleb komplekteerida ja lisada sihtidentifitseerimisnumbrile.</span><span class="sxs-lookup"><span data-stu-id="d6e64-440">Notice that line 1 from sales order 1 is what must be picked and added to the target license plate.</span></span> <span data-ttu-id="d6e64-441">Kuvatakse kaubakood, kogus, kauba kirjeldus ja komplekteerimise asukoht.</span><span class="sxs-lookup"><span data-stu-id="d6e64-441">The item number, quantity, item description, and pick location are shown.</span></span>

1. <span data-ttu-id="d6e64-442">Sisestage väljale **Siht-LP** identifitseerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="d6e64-442">In the **Target LP** field, enter a license plate number.</span></span>

    <span data-ttu-id="d6e64-443">Peate komplekteerima kõik read, mis loodi töödeldud voost samale sihtidentifitseerimisnumbrile.</span><span class="sxs-lookup"><span data-stu-id="d6e64-443">You will pick all lines that were created from the processed wave onto the same target license plate.</span></span>

1. <span data-ttu-id="d6e64-444">Kinnitage kirje.</span><span class="sxs-lookup"><span data-stu-id="d6e64-444">Confirm your entry.</span></span>

    <span data-ttu-id="d6e64-445">Mobiilirakendus esitab nüüd lehtede kogumi **Komplekteerimine**, mis suunavad teid komplekteerimise asukohta ning komplekteerimiseks vajalikule kaubale ja kogusele.</span><span class="sxs-lookup"><span data-stu-id="d6e64-445">The mobile app now presents a series of **Pick** pages that point you to the picking location, and to the item and quantity that must be picked.</span></span> <span data-ttu-id="d6e64-446">Pärast komplekteeritud kauba identifitseerimisnumbrile lisamist peate kinnitama komplekteerimise töö.</span><span class="sxs-lookup"><span data-stu-id="d6e64-446">After the picked item is added to the license plate, you will confirm the pick work.</span></span> <span data-ttu-id="d6e64-447">Viimane leht on töö komplekteeritud kaupade panemiseks sortimise asukohta.</span><span class="sxs-lookup"><span data-stu-id="d6e64-447">The last page will be the work to put the picked items into the sorting location.</span></span>

1. <span data-ttu-id="d6e64-448">Kinnitage esimene komplekteerimise töö.</span><span class="sxs-lookup"><span data-stu-id="d6e64-448">Confirm the first pick work.</span></span>
1. <span data-ttu-id="d6e64-449">Kuvatakse järgmine komplekteerimise töö.</span><span class="sxs-lookup"><span data-stu-id="d6e64-449">The next pick work is shown.</span></span> <span data-ttu-id="d6e64-450">Kinnitage komplekteerimine.</span><span class="sxs-lookup"><span data-stu-id="d6e64-450">Confirm the pick.</span></span>
1. <span data-ttu-id="d6e64-451">Jätkake järelejäänud komplekteerimise tööde kinnitamist.</span><span class="sxs-lookup"><span data-stu-id="d6e64-451">Continue to confirm the remaining pick work.</span></span>
1. <span data-ttu-id="d6e64-452">Viimane etapp on panemise töö lõpule viimine.</span><span class="sxs-lookup"><span data-stu-id="d6e64-452">The last step is to complete the put work.</span></span> <span data-ttu-id="d6e64-453">Kinnitage kõrvalepanek sortimise asukohta.</span><span class="sxs-lookup"><span data-stu-id="d6e64-453">Confirm the put-away to the sorting location.</span></span>

    <span data-ttu-id="d6e64-454">Teile kuvatakse teade „Töö lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="d6e64-454">You receive a "Work completed" message.</span></span>

1. <span data-ttu-id="d6e64-455">Väljuge mobiilirakenduse suvandist **Müügi komplekteerimine**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-455">Exit **Sales Picking** on the mobile app.</span></span>

### <a name="sortingput-to-wall"></a><span data-ttu-id="d6e64-456">Sortimine/pane seinale</span><span class="sxs-lookup"><span data-stu-id="d6e64-456">Sorting/put-to-wall</span></span>

<span data-ttu-id="d6e64-457">Kui kõik varud on pandud sortimise asukohta, tuleb need sortida õigesse sortimise paigutusse.</span><span class="sxs-lookup"><span data-stu-id="d6e64-457">Now that all inventory has been put to the sorting location, it must be sorted to the correct sort position.</span></span>

1. <span data-ttu-id="d6e64-458">Logige mobiilirakendusse sisse.</span><span class="sxs-lookup"><span data-stu-id="d6e64-458">Sign in to the mobile app.</span></span>
1. <span data-ttu-id="d6e64-459">Valige peamenüüs suvand **Väljaminev**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-459">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="d6e64-460">Valige menüüs **Väljaminev** suvand **Sortimine**, et alustada kaupade sortimist.</span><span class="sxs-lookup"><span data-stu-id="d6e64-460">On the **Outbound** menu, select **Sort** to start to sort the items.</span></span>
1. <span data-ttu-id="d6e64-461">Sisestage väljale **LP/CON** komplekteeritud müügitellimuse töö sihtidentifitseerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="d6e64-461">In the **LP/CON** field, enter the target license plate of the picked sales order work.</span></span>
1. <span data-ttu-id="d6e64-462">Kinnitage kirje.</span><span class="sxs-lookup"><span data-stu-id="d6e64-462">Confirm your entry.</span></span>
1. <span data-ttu-id="d6e64-463">Sisestage esimesena sorditava kauba kood.</span><span class="sxs-lookup"><span data-stu-id="d6e64-463">Enter the item number to sort first.</span></span>
1. <span data-ttu-id="d6e64-464">Süsteem määratleb esimese sortimise asukoha, mida tuleks kuvada.</span><span class="sxs-lookup"><span data-stu-id="d6e64-464">The system determines the first sort position that should be shown.</span></span> <span data-ttu-id="d6e64-465">Kinnitage sortimise asukoht.</span><span class="sxs-lookup"><span data-stu-id="d6e64-465">Confirm the sort position.</span></span>
1. <span data-ttu-id="d6e64-466">Teil palutakse määrata identifitseerimisnumber sortimise asukohale.</span><span class="sxs-lookup"><span data-stu-id="d6e64-466">You're prompted to assign a license plate to the sort position.</span></span> <span data-ttu-id="d6e64-467">Valige väli **LP**, sisestage identifitseerimisnumbr ja kinnitage kirje.</span><span class="sxs-lookup"><span data-stu-id="d6e64-467">Select the **LP** field, enter a license plate number, and then confirm your entry.</span></span>

    <span data-ttu-id="d6e64-468">Kuna sortimise asukoht on seostatud saadetise ID-ga, sordite komplekteeritud kaubad väljaminevale saadetisele ja müügitellimusele omasele identifitseerimisnumbrile.</span><span class="sxs-lookup"><span data-stu-id="d6e64-468">Because the sort position is related to the shipment ID, you will sort the picked items into a license plate that is specific to the outbound shipment and sales order.</span></span>

    <span data-ttu-id="d6e64-469">Järgmisel lehel kuvatakse kauba ID, kogus, sortimise asukoha ID ja identifitseerimisnumbri ID-d „alates” (komplekteerimine) ja „kuni” (sortimine).</span><span class="sxs-lookup"><span data-stu-id="d6e64-469">The next page shows the item ID, quantity, sort position ID, and the "from" (picking) and "to" (sorting) license plate IDs.</span></span> <span data-ttu-id="d6e64-470">Sellel lehel olev teave juhendab teid sortima määratud kauba ja kogused komplekteerimise identifitseerimisnumbrilt sortimise identifitseerimisnumbrile.</span><span class="sxs-lookup"><span data-stu-id="d6e64-470">The information on this page instructs you to sort the specified item and quantities from the picking license plate into the sorting license plate.</span></span>

1. <span data-ttu-id="d6e64-471">Kinnitage sortimise asukoht.</span><span class="sxs-lookup"><span data-stu-id="d6e64-471">Confirm the sort position.</span></span>
1. <span data-ttu-id="d6e64-472">Sortige kaubad esimeses sortimise asukohas.</span><span class="sxs-lookup"><span data-stu-id="d6e64-472">Sort the items in the first sort position.</span></span> <span data-ttu-id="d6e64-473">Kui olete lõpetanud, suunab süsteem teid järgmisse sortimise asukohta.</span><span class="sxs-lookup"><span data-stu-id="d6e64-473">When you've finished, the system directs you to the next sort position.</span></span>
1. <span data-ttu-id="d6e64-474">Korrake seda protsessi töökäsu kõigi komplekteeritud ridade puhul.</span><span class="sxs-lookup"><span data-stu-id="d6e64-474">Repeat this process for all picked lines on the work order.</span></span> <span data-ttu-id="d6e64-475">Seda protsessi tuleks kasutada ka juhul, kui on mitu sama kaubakoodiga komplekteerimise rida.</span><span class="sxs-lookup"><span data-stu-id="d6e64-475">You should also use this process when there are multiple pick lines that have the same item number.</span></span>

    <span data-ttu-id="d6e64-476">Kui kordate seda protsessi kõigi kaupade puhul, hindab süsteem kriteeriume järgmisest skannitud kaubast (töörida) ja määrab, millisesse sortimise asukohta see tuleks panna.</span><span class="sxs-lookup"><span data-stu-id="d6e64-476">As you repeat this process for all items, the system evaluates the criteria from the next scanned item (work line) and determines which sorting position it should be put to.</span></span> <span data-ttu-id="d6e64-477">Teid suunatakse automaatselt kaupa õigesse sortimise asukohta panema.</span><span class="sxs-lookup"><span data-stu-id="d6e64-477">You're automatically directed to put the item to the correct sort position.</span></span> <span data-ttu-id="d6e64-478">Sõltuvalt kinnituse seadistusest, suunatakse teid kinnitama seda tegevust asukoha numbri ja identifitseerimisnumbri ID sisestamisega.</span><span class="sxs-lookup"><span data-stu-id="d6e64-478">Depending on the confirmation setup, you're also directed to confirm this action by entering the position number or license plate ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d6e64-479">Kui automaatne sortimine on sisse lülitatud, ei ole käsitsi alistamine saadaval.</span><span class="sxs-lookup"><span data-stu-id="d6e64-479">If automatic sorting is turned on, manual override isn't available.</span></span>

1. <span data-ttu-id="d6e64-480">Kui olete lõpetanud, avage rakenduses Microsoft Dynamics 365 Supply Chain Management leht **Väljamineku sortimise asukoha määramised**, et vaadata üle asukohtade olek.</span><span class="sxs-lookup"><span data-stu-id="d6e64-480">When you've finished, in Microsoft Dynamics 365 Supply Chain Management, open the **Outbound sorting position assignments** page to review the status of the positions.</span></span>

    - <span data-ttu-id="d6e64-481">Kui asukohad suletakse automaatselt, valige **Kuva suletud** suletud asukohtade kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-481">If positions are closed automatically, select **Show closed** to show the closed positions.</span></span>
    - <span data-ttu-id="d6e64-482">Pange tähele, et kuvataksesortimise asukoha kanded.</span><span class="sxs-lookup"><span data-stu-id="d6e64-482">Notice that sort position transactions are shown.</span></span> <span data-ttu-id="d6e64-483">Kuvatakse asukoha kaudu töödeldud kaup ja kogus.</span><span class="sxs-lookup"><span data-stu-id="d6e64-483">The item and quantity that were processed through the position are shown.</span></span>

    <span data-ttu-id="d6e64-484">Kui seadistate väljamineku sortimismalli, seadke suvandi **Sortimise asukoha automaatne sulgemine** väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="d6e64-484">When you set up the outbound sorting template, you set the **Auto close sort position** option to *Yes*.</span></span> <span data-ttu-id="d6e64-485">Seega, asukoht suletakse automaatselt pärast sellele viimaste eeldatavate varude panemist.</span><span class="sxs-lookup"><span data-stu-id="d6e64-485">Therefore, the position is automatically closed after the last expected inventory is put to it.</span></span> <span data-ttu-id="d6e64-486">Sortimise asukohtade olek on **Suletud** ja töö on loodud, et teisaldada sorditud varud asukohta *Baydoor*.</span><span class="sxs-lookup"><span data-stu-id="d6e64-486">The sort positions are in **Closed** status, and work has been created to move the sorted inventory to *Baydoor* location.</span></span>

1. <span data-ttu-id="d6e64-487">Viige sorditud varude komplekteerimise töö lõpule, et teisaldada varud lähetuse asukohta.</span><span class="sxs-lookup"><span data-stu-id="d6e64-487">Complete the sorted inventory picking work to move the inventory to the shipping location.</span></span> <span data-ttu-id="d6e64-488">Kui varud on valmis, kinnitage need lähetuseks.</span><span class="sxs-lookup"><span data-stu-id="d6e64-488">When the inventory is ready, ship-confirm it.</span></span>

> [!NOTE]
> <span data-ttu-id="d6e64-489">Sorditud varude komplekteerimise töö õigesti töötlemiseks peaks teisaldamise ja laadimise protsessis kasutama mobiilse seadme menüü-üksust, millel on tööklassi ID seal, kus välja **Töökäsu tüüp** väärtuseks on seatud *Sorditud varude komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="d6e64-489">For sorted inventory picking work to be processed correctly, a mobile device menu item that has a work class ID where the **Work order type** field is set to *Sorted inventory picking* should be used for the movement and loading process.</span></span>

### <a name="manually-close-a-position-optional"></a><span data-ttu-id="d6e64-490">Asukoha käsitsi sulgemine (valikuline)</span><span class="sxs-lookup"><span data-stu-id="d6e64-490">Manually close a position (optional)</span></span>

<span data-ttu-id="d6e64-491">Kui sortimise asukohti on vaja käsitsi sulgeda, peab väljamineku sortimismalli suvandi **Sortimise asukoha automaatne sulgemine** väärtuseks olema *Ei* ja sulgemine tuleb teha enne, kui varusid saab teisaldada laadimisukse piirkonda.</span><span class="sxs-lookup"><span data-stu-id="d6e64-491">If sort positions should be closed manually, the **Auto close sort position** option for the outbound sorting template must be set to *No*, and closing must be done before inventory can be moved to the bay door area.</span></span> <span data-ttu-id="d6e64-492">Asukohti saab sulgeda mitmel viisil.</span><span class="sxs-lookup"><span data-stu-id="d6e64-492">Positions can be closed in various ways:</span></span>

- <span data-ttu-id="d6e64-493">Laorakenduse kaudu.</span><span class="sxs-lookup"><span data-stu-id="d6e64-493">Via the warehouse app:</span></span>

    - <span data-ttu-id="d6e64-494">Kasutaja saab skannida ühte kaupa, mis on juba asukohas ja seejärel valida asukoha sulgemiseks **Sule**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-494">The user can scan one of the items that are already on the position and then select **Close** to close the position.</span></span>
    - <span data-ttu-id="d6e64-495">Kui kasutaja skannib konteinerit, mis on juba sorditud konteiner, kuvatakse tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="d6e64-495">If the user scans a container that has already been sorted container, an error message is shown.</span></span> <span data-ttu-id="d6e64-496">Kuid kasutaja saab siiski jätkata asukoha sulgemisega.</span><span class="sxs-lookup"><span data-stu-id="d6e64-496">However, the user can still continue to close the position.</span></span>

- <span data-ttu-id="d6e64-497">Microsoft Dynamics 365 Supply Chain Managementi lehe **Väljamineku sortimise asukoha määramised** kaudu.</span><span class="sxs-lookup"><span data-stu-id="d6e64-497">From the Microsoft Dynamics 365 Supply Chain Management **Outbound sorting position assignments** page:</span></span>

    - <span data-ttu-id="d6e64-498">Kasutaja saab valida väljamineku sortimise asukoha kirje ja seejärel valida toimingupaanil **Sule asukoht**.</span><span class="sxs-lookup"><span data-stu-id="d6e64-498">The user can select the outbound sorting position record and then select **Close position** on the Action Pane.</span></span>

## <a name="tips"></a><span data-ttu-id="d6e64-499">Näpunäited</span><span class="sxs-lookup"><span data-stu-id="d6e64-499">Tips</span></span>

- <span data-ttu-id="d6e64-500">Ku kaup on juba määratud ühte asukohta, ei saa seda mujale teisaldada.</span><span class="sxs-lookup"><span data-stu-id="d6e64-500">Items can't be moved between positions after they have been assigned to one.</span></span> <span data-ttu-id="d6e64-501">Süsteem hindab kogust, kui palju ühest kaubast tuleks kindlasse asukohta panna.</span><span class="sxs-lookup"><span data-stu-id="d6e64-501">The system evaluates how many of each item should go to a specific position.</span></span>
- <span data-ttu-id="d6e64-502">Sortimismalli saab konfigureerida automaatselt konteinereid looma asukohtade sulgemisel.</span><span class="sxs-lookup"><span data-stu-id="d6e64-502">Sorts template can be configured to automatically create containers when positions are closed.</span></span> <span data-ttu-id="d6e64-503">See lähenemine loob standardse konteineri ID struktuuri määratud pakkimise profiili põhjal.</span><span class="sxs-lookup"><span data-stu-id="d6e64-503">This approach will create standard container ID structure that is based on the specified packing profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d6e64-504">Kui liikumise töö on loodud sortimise asukohast, ei tohi tööd tühistada.</span><span class="sxs-lookup"><span data-stu-id="d6e64-504">After movement work has been created from the sorting location, you must not cancel the work.</span></span> <span data-ttu-id="d6e64-505">Vastasel juhul kustutatakse asukoht ja selles olevad konteinerid süsteemist ja need pole edasiseks töötlemiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="d6e64-505">Otherwise, the position and the containers in it will be deleted from the system and unavailable for further processing.</span></span> <span data-ttu-id="d6e64-506">Samuti eemaldatakse varud.</span><span class="sxs-lookup"><span data-stu-id="d6e64-506">The inventory will also be removed.</span></span>
