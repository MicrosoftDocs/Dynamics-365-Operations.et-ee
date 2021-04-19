---
title: Ladustatavad kogumid
description: Kogumite ladustamine pakub võimalust komplekteerida mitu identifitseerimisnumbrit samal ajal ja seejärel neid erinevates asukohtades ladustada. Need võivad olla väga kasulikud jaemüügi ettevõtetele, kus identifitseerimisnumbrid ei ole tavaliselt täis kaubaalused.
author: Mirzaab
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: b3a7d1b7109b83b26c8187a7f0d271f1c82f6d63
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840361"
---
# <a name="putaway-clusters"></a><span data-ttu-id="2652a-104">Ladustatavad kogumid</span><span class="sxs-lookup"><span data-stu-id="2652a-104">Putaway clusters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2652a-105">Kogumite ladustamine pakub võimalust komplekteerida mitu identifitseerimisnumbrit samal ajal ja seejärel neid erinevates asukohtades ladustada.</span><span class="sxs-lookup"><span data-stu-id="2652a-105">Putaway clusters offer a way to pick multiple license plates at the same time and then take them for putaway in different locations.</span></span> <span data-ttu-id="2652a-106">Seda protsessi nimetatakse sageli *veoringiks*.</span><span class="sxs-lookup"><span data-stu-id="2652a-106">This process is often referred to as a *milk run*.</span></span> <span data-ttu-id="2652a-107">Ladustatavad kogumid võivad olla väga kasulikud jaemüügi ettevõtetele, kus identifitseerimisnumbrid ei ole tavaliselt täielikult täis kaubaalused.</span><span class="sxs-lookup"><span data-stu-id="2652a-107">Putaway clusters can be very useful for retail businesses, where license plates typically aren't full pallets of inventory.</span></span> 

## <a name="turn-on-the-cluster-putaway-feature"></a><span data-ttu-id="2652a-108">Kogumite ladustamise funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="2652a-108">Turn on the cluster putaway feature</span></span>

<span data-ttu-id="2652a-109">Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="2652a-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="2652a-110">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="2652a-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="2652a-111">Seega on funktsioon loetletud järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="2652a-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="2652a-112">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="2652a-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="2652a-113">**Funktsiooni nimi:** *Kogumi ladustamise funktsioon*</span><span class="sxs-lookup"><span data-stu-id="2652a-113">**Feature name:** *Cluster putaway feature*</span></span>

## <a name="setup-for-the-example-scenario"></a><span data-ttu-id="2652a-114">Näite seadistamine</span><span class="sxs-lookup"><span data-stu-id="2652a-114">Setup for the example scenario</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="2652a-115">Kogumiprofiilid</span><span class="sxs-lookup"><span data-stu-id="2652a-115">Cluster profiles</span></span>

<span data-ttu-id="2652a-116">Ladustatava kogumi profiil määrab, kuhu kaup läheb, võttes aluseks asukoha, mis on kaubale sissetuleku ajal määratud.</span><span class="sxs-lookup"><span data-stu-id="2652a-116">The putaway cluster profile determines where an item will go, based on the location that is assigned to the item at the time of receipt.</span></span> <span data-ttu-id="2652a-117">Kui nõutavad on erinevad kogumid, tuleb iga mobiilse seadme menüü-üksuse jaoks luua erineva ladustatava kogumi profiil.</span><span class="sxs-lookup"><span data-stu-id="2652a-117">If different clusters are required, different putaway clusters should be created, one for each mobile device menu item.</span></span>

1. <span data-ttu-id="2652a-118">Avage **Laohaldus \> Seadistamine \> Mobiilne seade \> Kogumiprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="2652a-118">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="2652a-119">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2652a-119">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2652a-120">Määrake **Päise** vaates järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="2652a-120">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="2652a-121">**Ladustatava kogumi profiili ID:** *Kogumi ladustamine*</span><span class="sxs-lookup"><span data-stu-id="2652a-121">**Putaway cluster profile ID:** *Cluster putaway*</span></span>
    - <span data-ttu-id="2652a-122">**Ladustatava kogumi profiili ID-nimi:** *Kogumi ladustamine*</span><span class="sxs-lookup"><span data-stu-id="2652a-122">**Putaway cluster profile ID Name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="2652a-123">**Kogumi tüüp:** *Ladustatav*</span><span class="sxs-lookup"><span data-stu-id="2652a-123">**Cluster type:** *Putaway*</span></span>
    - <span data-ttu-id="2652a-124">**Järjekorranumber:** nõustuge vaikeväärtusega.</span><span class="sxs-lookup"><span data-stu-id="2652a-124">**Sequence number:** Accept the default value.</span></span>

1. <span data-ttu-id="2652a-125">Valige **Salvesta**, et muuta nõutud väljad kiirkaardil **Üldine** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="2652a-125">Select **Save** to make the required fields on the **General** FastTab available.</span></span>
1. <span data-ttu-id="2652a-126">Määrake kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="2652a-126">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2652a-127">**Kogumi määramise ajastus:** *Vastuvõtul*</span><span class="sxs-lookup"><span data-stu-id="2652a-127">**Cluster assignment timing:** *At receipt*</span></span>

        <span data-ttu-id="2652a-128">See väli määratleb, kas ladustatav kogum tuleb määrata kohe, kui kaup on vastu võetud või kas see tuleks sorteerida hiljem.</span><span class="sxs-lookup"><span data-stu-id="2652a-128">This field defines whether the putaway cluster should be assigned immediately when the inventory is received, or whether it should be sorted later.</span></span>

    - <span data-ttu-id="2652a-129">**Kogumi määramise reegel:** *Käsitsi*</span><span class="sxs-lookup"><span data-stu-id="2652a-129">**Cluster assignment rule:** *Manual*</span></span>

        <span data-ttu-id="2652a-130">Väli määrab, kas kogumi peaks määrama süsteem automaatselt või peaks seda kasutaja tegema käsitsi.</span><span class="sxs-lookup"><span data-stu-id="2652a-130">This field defines whether the cluster assignment should be determined automatically by the system or manually by the user.</span></span>

    - <span data-ttu-id="2652a-131">**Korralduse kood:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="2652a-131">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="2652a-132">**Ladustatava kogumi asukoht:** *Vastuvõtt*</span><span class="sxs-lookup"><span data-stu-id="2652a-132">**Putaway cluster locate:** *Receipt*</span></span>

        <span data-ttu-id="2652a-133">Saadaval on järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="2652a-133">The following values are available:</span></span>

        - <span data-ttu-id="2652a-134">**Vastuvõtt** –Asukoht leitakse koheselt vastuvõtul.</span><span class="sxs-lookup"><span data-stu-id="2652a-134">**Receipt** – A location is found immediately during receipt.</span></span>
        - <span data-ttu-id="2652a-135">**Suletud kogum** – Asukoht leitakse kui kogum on suletud.</span><span class="sxs-lookup"><span data-stu-id="2652a-135">**Cluster close** – A location is found when the cluster is closed.</span></span>
        - <span data-ttu-id="2652a-136">**Kasutaja suunatud** – Asukoht leitakse, kui ladustatavast kogumist valitakse identifitseerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="2652a-136">**User directed** – A location is found when the license plate is picked from the cluster for putaway.</span></span> <span data-ttu-id="2652a-137">Sellisel juhul pole ladustamisülesande loomisel ühtegi asukohta määratud.</span><span class="sxs-lookup"><span data-stu-id="2652a-137">In this case, no location is specified when the putaway work is created.</span></span> <span data-ttu-id="2652a-138">Ladustamise enda ajal peab kasutaja määrama identifitseerimisnumbri või töö ID, et algatada ladustamise etapp.</span><span class="sxs-lookup"><span data-stu-id="2652a-138">During the putaway itself, the user must scan the license plate or work ID to initiate the put step.</span></span> <span data-ttu-id="2652a-139">Süsteem leiab seejärel ladustamise asukoha uuesti ja ütleb kasutajale, kuhu panna komplekteeritud kogus.</span><span class="sxs-lookup"><span data-stu-id="2652a-139">The system then finds the put location again and tells the user where to put the picked quantity.</span></span>

    - <span data-ttu-id="2652a-140">**Kogumi ladustamine kasutaja kohta:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="2652a-140">**Putaway cluster per user:** *No*</span></span>

        <span data-ttu-id="2652a-141">See väli määratleb, kas kogumite automaatsel määramisel peab iga kogum olema iga kasutaja kohta unikaalne.</span><span class="sxs-lookup"><span data-stu-id="2652a-141">This field defines whether each cluster should be unique per user when clusters are automatically assigned.</span></span> <span data-ttu-id="2652a-142">See on saadaval ainult siis, kui **Kogumi määramise reegli** välja väärtuseks on seatud *Automaatne*.</span><span class="sxs-lookup"><span data-stu-id="2652a-142">It's available only when the **Cluster assignment rule** field is set to *Automatic*.</span></span>

    - <span data-ttu-id="2652a-143">**Ühiku piirang:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="2652a-143">**Unit restriction:** Leave this field blank.</span></span>

        <span data-ttu-id="2652a-144">See väli määratleb ühiku, mis tuleb selle profiili kehtivuseks vastu võtta.</span><span class="sxs-lookup"><span data-stu-id="2652a-144">This field defines the unit that must be received for the profile to be valid.</span></span> <span data-ttu-id="2652a-145">Kui väli on jäetud tühjaks, kehtivad kõik ühikud.</span><span class="sxs-lookup"><span data-stu-id="2652a-145">If it's left blank, all units are valid.</span></span>

    - <span data-ttu-id="2652a-146">**Tööüksuse vaheaeg:** *Individuaalne*</span><span class="sxs-lookup"><span data-stu-id="2652a-146">**Work unit break:** *Individual*</span></span>

        <span data-ttu-id="2652a-147">See väli määratleb, kas kõik varud tuleb konsolideerida (kasutades kogumi ID-d ja identifitseerimisnumbrit) ühele identifitseerimisnumbrile, kui kogum on suletud, ja kas see tuleks ladustada ühe identifitseerimisnumbrina või eraldi vastu võetud identifitseerimisnumbritega.</span><span class="sxs-lookup"><span data-stu-id="2652a-147">This field defines whether all inventory should be consolidated (by using the cluster ID and the license plate) onto one license plate when a cluster is closed, and whether it should be put away as a single license plate or separately on the license plates that were received.</span></span> <span data-ttu-id="2652a-148">See väli pole saadaval, kui välja **Ladustatava kogumi asukoht** väärtuseks on seatud *Vastuvõtt*.</span><span class="sxs-lookup"><span data-stu-id="2652a-148">This field is unavailable when the **Putaway cluster locate** field is set to *Receipt*.</span></span>

    - <span data-ttu-id="2652a-149">**Kogum püsib peamise identifitseerimisnumbrina:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="2652a-149">**Cluster persists as Parent License Plate:** *No*</span></span>

        <span data-ttu-id="2652a-150">Kui see suvand on seatud väärtusele *Jah*, siis kui ladustamise toiming on lõpule viidud, muutub kogumi ID peamiseks identifitseerimisnumbriks ja kõik kogumi ID all olevad üksused seotakse selle peamise identifitseerimisnumbriga.</span><span class="sxs-lookup"><span data-stu-id="2652a-150">If this option is set to *Yes*, when the put step is completed, the cluster ID will become a parent license plate, and all items on the cluster ID will be linked to that parent license plate.</span></span>

1. <span data-ttu-id="2652a-151">**Kogumi sortimise** kiirkaardil saate määratleda ladustamise sortimise kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="2652a-151">On the **Cluster sorting** FastTab, you can define putaway sorting criteria.</span></span> <span data-ttu-id="2652a-152">Valige tööriistaribal **Uus**, et lisada rida ja seejärel seadke sellele järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="2652a-152">Select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="2652a-153">**Järjekorranumber:** nõustuge vaikeväärtusega.</span><span class="sxs-lookup"><span data-stu-id="2652a-153">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="2652a-154">**Välja nimi:** *WMSLocationId*</span><span class="sxs-lookup"><span data-stu-id="2652a-154">**Field name:** *WMSLocationId*</span></span>

        <span data-ttu-id="2652a-155">See väli määratleb välja, mida see rida peaks sortimise kriteeriumina kasutama.</span><span class="sxs-lookup"><span data-stu-id="2652a-155">This field defines the field that this line should use as a sorting criterion.</span></span>

    - <span data-ttu-id="2652a-156">**Sortimine:** *Tõusev järjestus*</span><span class="sxs-lookup"><span data-stu-id="2652a-156">**Sorting:** *Ascending*</span></span>

        <span data-ttu-id="2652a-157">See väli määrab, kas sortimine peaks toimuma kasvavas või kahanevas järjestuses.</span><span class="sxs-lookup"><span data-stu-id="2652a-157">This field defines whether sorting should be done in ascending or descending order.</span></span>

1. <span data-ttu-id="2652a-158">Valige **Kogumi töömall** kiirkaardi tööriistaribal **Uus**, et lisada rida ja seejärel seadke sellele järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="2652a-158">On the **Cluster work template** FastTab, select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="2652a-159">**Töötellimuse tüüp:** *ostutellimused*</span><span class="sxs-lookup"><span data-stu-id="2652a-159">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="2652a-160">**Töömall:** *61 Ostutellimuse suunamine*</span><span class="sxs-lookup"><span data-stu-id="2652a-160">**Work template:** *61 PO Direct*</span></span>

1. <span data-ttu-id="2652a-161">Tegevuspaanil valige **Salvesta** ja seejärel valige **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="2652a-161">On the Action Pane, select **Save**, and then select **Edit query**.</span></span>
1. <span data-ttu-id="2652a-162">Valige **Kogumi ladustamise** dialoogiboksis **Vahemik** vahekaardil suvand **Add**, et lisada päringule teine rida.</span><span class="sxs-lookup"><span data-stu-id="2652a-162">In the **Cluster putaway** dialog box, on the **Range** tab, select **Add** to add a second line to the query.</span></span> <span data-ttu-id="2652a-163">Seejärel värskendage päringu ridu, nagu näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="2652a-163">Then update the query lines as shown in the following table.</span></span>

    | <span data-ttu-id="2652a-164">Tabel</span><span class="sxs-lookup"><span data-stu-id="2652a-164">Table</span></span> | <span data-ttu-id="2652a-165">Tuletatud tabel</span><span class="sxs-lookup"><span data-stu-id="2652a-165">Derived table</span></span> | <span data-ttu-id="2652a-166">Field</span><span class="sxs-lookup"><span data-stu-id="2652a-166">Field</span></span> | <span data-ttu-id="2652a-167">Kriteerium</span><span class="sxs-lookup"><span data-stu-id="2652a-167">Criteria</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="2652a-168">Töö</span><span class="sxs-lookup"><span data-stu-id="2652a-168">Work</span></span> | <span data-ttu-id="2652a-169">Töö</span><span class="sxs-lookup"><span data-stu-id="2652a-169">Work</span></span> | <span data-ttu-id="2652a-170">Ladu</span><span class="sxs-lookup"><span data-stu-id="2652a-170">Warehouse</span></span> | <span data-ttu-id="2652a-171">*61*</span><span class="sxs-lookup"><span data-stu-id="2652a-171">*61*</span></span> |
    | <span data-ttu-id="2652a-172">Töö</span><span class="sxs-lookup"><span data-stu-id="2652a-172">Work</span></span> | <span data-ttu-id="2652a-173">Töö</span><span class="sxs-lookup"><span data-stu-id="2652a-173">Work</span></span> | <span data-ttu-id="2652a-174">Töö ID</span><span class="sxs-lookup"><span data-stu-id="2652a-174">Work ID</span></span> | <span data-ttu-id="2652a-175">Jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="2652a-175">Leave this field blank.</span></span> |

1. <span data-ttu-id="2652a-176">Päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="2652a-176">Select **OK** to save the query and close the dialog box.</span></span>
1. <span data-ttu-id="2652a-177">Valige tegevuspaanil **Salvesta** ja sulgege lehekülg.</span><span class="sxs-lookup"><span data-stu-id="2652a-177">On the Action Pane, select **Save**, and close the page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2652a-178">Kogumi profiilil olevad väljad, mis kuvatakse tuhmina, kui **Kogumi ID loomine** on seatud valikule *Jah*, ei ole saadaval ja ei arvestata funktsiooni kasutamisel.</span><span class="sxs-lookup"><span data-stu-id="2652a-178">Fields in the cluster profile that appear dimmed when **Generate cluster ID** is set to *Yes* are unavailable and won't be considered when this feature is used.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="2652a-179">Mobiilse seadme menüü-üksused</span><span class="sxs-lookup"><span data-stu-id="2652a-179">Mobile device menu items</span></span>

<span data-ttu-id="2652a-180">Selle funktsiooni jaoks on saadaval kaks uut mobiilse seadme menüükäsku.</span><span class="sxs-lookup"><span data-stu-id="2652a-180">Two new mobile device menu items are available for this feature.</span></span> <span data-ttu-id="2652a-181">**Võta vastu ja sordi kogum** menüükäsku kasutatakse saadud kauba sortimiseks ladustatavatesse kogumitesse vastuvõtul.</span><span class="sxs-lookup"><span data-stu-id="2652a-181">The **Receive and sort cluster** menu item is used to sort the received inventory into a putaway cluster upon receipt.</span></span> <span data-ttu-id="2652a-182">**Ladustatav kogum** menüükäsku kasutatakse, et ladustada kogum pärast selle määramist.</span><span class="sxs-lookup"><span data-stu-id="2652a-182">The **Cluster putaway** menu item is used to put the cluster away after it has been assigned.</span></span>

#### <a name="receive-and-sort-cluster"></a><span data-ttu-id="2652a-183">Võta vastu ja sordi kogum</span><span class="sxs-lookup"><span data-stu-id="2652a-183">Receive and sort cluster</span></span>

<span data-ttu-id="2652a-184">Looge uus mobiilse seadme menüükäsk kauba vastuvõtmiseks ja kogumisse sortimiseks.</span><span class="sxs-lookup"><span data-stu-id="2652a-184">Create a new mobile device menu item for receiving inventory and sorting into a cluster.</span></span> <span data-ttu-id="2652a-185">See menüükäsk loob sissetuleva töö pärast kauba vastuvõtmist, mis näitab, et ladustatavate kogumite puhul kasutatakse vastuvõtvat menüükäsku.</span><span class="sxs-lookup"><span data-stu-id="2652a-185">This menu item will create inbound work after inventory is received, which indicates that the receiving menu item will be used for putaway clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="2652a-186">**Võta vastu ja sordi kogum** menüükäsku saab kasutada järgmiste vastuvõtvate menüükäskudega:</span><span class="sxs-lookup"><span data-stu-id="2652a-186">The **Receive and sort cluster** menu item can be used with the following receiving menu items:</span></span>
>
> - <span data-ttu-id="2652a-187">Vastuvõttev ostutellimuse rida</span><span class="sxs-lookup"><span data-stu-id="2652a-187">Purchase order line receiving</span></span>
> - <span data-ttu-id="2652a-188">Vastuvõttev ostutellimuse üksus</span><span class="sxs-lookup"><span data-stu-id="2652a-188">Purchase order item receiving</span></span>
> - <span data-ttu-id="2652a-189">Vastuvõetav koormas olev kaup</span><span class="sxs-lookup"><span data-stu-id="2652a-189">Load item receiving</span></span>

1. <span data-ttu-id="2652a-190">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüükäsud**.</span><span class="sxs-lookup"><span data-stu-id="2652a-190">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="2652a-191">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2652a-191">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2652a-192">Määrake **Päise** vaates järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="2652a-192">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="2652a-193">**Menüükäsu nimi:** *Võta vastu ja sordi kogum*</span><span class="sxs-lookup"><span data-stu-id="2652a-193">**Menu item name:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="2652a-194">**Nimi:** *Võta vastu ja sordi kogum*</span><span class="sxs-lookup"><span data-stu-id="2652a-194">**Title:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="2652a-195">**Režiim:** *töö*</span><span class="sxs-lookup"><span data-stu-id="2652a-195">**Mode:** *Work*</span></span>
    - <span data-ttu-id="2652a-196">**Kasuta olemasolevat tööd:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="2652a-196">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="2652a-197">Määrake kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="2652a-197">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="2652a-198">**Töö loomise protsess:** *vastuvõttev ostutellimuse kaup*</span><span class="sxs-lookup"><span data-stu-id="2652a-198">**Work creation process:** *Purchase order item receiving*</span></span>
    - <span data-ttu-id="2652a-199">**Loo litsentsiplaat:** *jah*</span><span class="sxs-lookup"><span data-stu-id="2652a-199">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="2652a-200">**Määra ladustatav kogum:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="2652a-200">**Assign putaway cluster:** *Yes*</span></span>

        > [!NOTE]
        > <span data-ttu-id="2652a-201">**Kogumi ladustamise määramise** valik on saadaval ainult ühe-etapilise *Töö loomise protsessi* tegevuse vastuvõtmiseks.</span><span class="sxs-lookup"><span data-stu-id="2652a-201">The **Assign putaway cluster** option is available only for the one-step *Work creation process* activity for receiving.</span></span>

    <span data-ttu-id="2652a-202">Võtke vastu ülejäänud väljade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="2652a-202">Accept the default values for the remaining fields.</span></span>

1. <span data-ttu-id="2652a-203">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2652a-203">On the Action Pane, select **Save**.</span></span>

#### <a name="cluster-putaway"></a><span data-ttu-id="2652a-204">Kogumi kõrvalepanek</span><span class="sxs-lookup"><span data-stu-id="2652a-204">Cluster putaway</span></span>

<span data-ttu-id="2652a-205">Looge uus mobiilse seadme menüükäsk, et panna kogum ära pärast selle määramist.</span><span class="sxs-lookup"><span data-stu-id="2652a-205">Create a new mobile device menu item for putting the cluster away after it has been assigned.</span></span>

1. <span data-ttu-id="2652a-206">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüükäsud**.</span><span class="sxs-lookup"><span data-stu-id="2652a-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="2652a-207">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2652a-207">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2652a-208">Määrake **Päise** vaates järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="2652a-208">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="2652a-209">**Menüükäsu nimi:** *Kogumi ladustamine*</span><span class="sxs-lookup"><span data-stu-id="2652a-209">**Menu item name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="2652a-210">**Pealkiri:** *Kogumi ladustamine*</span><span class="sxs-lookup"><span data-stu-id="2652a-210">**Title:** *Cluster putaway*</span></span>
    - <span data-ttu-id="2652a-211">**Režiim:** *töö*</span><span class="sxs-lookup"><span data-stu-id="2652a-211">**Mode:** *Work*</span></span>
    - <span data-ttu-id="2652a-212">**Kasuta olemasolevat tööd:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="2652a-212">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="2652a-213">Määrake kiirkaardi **Üldine** väljal **Suunaja** väärtuseks *Kogumi ladustamine*.</span><span class="sxs-lookup"><span data-stu-id="2652a-213">On the **General** FastTab, set the **Directed by** field to *Cluster putaway*.</span></span> <span data-ttu-id="2652a-214">Võtke vastu ülejäänud väljade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="2652a-214">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="2652a-215">Kiirkaardil **Tööklassid** seadistage sellele mobiilse seadme menüükäsule kehtiv tööklass:</span><span class="sxs-lookup"><span data-stu-id="2652a-215">On the **Work classes** FastTab, set up the valid work class for this mobile device menu item:</span></span>

    - <span data-ttu-id="2652a-216">**Tööklassi ID:** *Ost*</span><span class="sxs-lookup"><span data-stu-id="2652a-216">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="2652a-217">**Töötellimuse tüüp:** *ostutellimused*</span><span class="sxs-lookup"><span data-stu-id="2652a-217">**Work order type:** *Purchase orders*</span></span>

1. <span data-ttu-id="2652a-218">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2652a-218">On the Action Pane, select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="2652a-219">Mobiilse seadme menüü</span><span class="sxs-lookup"><span data-stu-id="2652a-219">Mobile device menu</span></span>

<span data-ttu-id="2652a-220">Lisage menüü-üksused, mille äsja lõite mobiilse rakenduse sissetulevale menüüle.</span><span class="sxs-lookup"><span data-stu-id="2652a-220">Add the menu items that you just created to the inbound menu of the mobile app.</span></span>

1. <span data-ttu-id="2652a-221">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.</span><span class="sxs-lookup"><span data-stu-id="2652a-221">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="2652a-222">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="2652a-222">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="2652a-223">Valige menüü loendist suvand **Sissetulev**.</span><span class="sxs-lookup"><span data-stu-id="2652a-223">In the menu list, select **Inbound**.</span></span>
1. <span data-ttu-id="2652a-224">Otsige üles ja valige loendist **Saadaolevad menüüd ja menüü-üksused** suvand **Võta vastu ja sordi kogum**.</span><span class="sxs-lookup"><span data-stu-id="2652a-224">In the **Available menus and menu items** list, find and select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="2652a-225">Valige parempoolne noolenupp, et nihutada valitud menüü-üksus **Menüüstruktuuri** loendisse.</span><span class="sxs-lookup"><span data-stu-id="2652a-225">Select the right arrow button to move the selected menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="2652a-226">Kasutage üles ja alla noolenuppe, et teisaldada menüü-üksus soovitud asukohta menüüs.</span><span class="sxs-lookup"><span data-stu-id="2652a-226">Use the up arrow or down arrow button to move the menu item into the desired position in the menu.</span></span>
1. <span data-ttu-id="2652a-227">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2652a-227">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="2652a-228">Korrake samme 4 kuni 7, et lisada ülejäänud menüü-üksused:</span><span class="sxs-lookup"><span data-stu-id="2652a-228">Repeat steps 4 through 7 to add the remaining menu items:</span></span>

    - <span data-ttu-id="2652a-229">Kogumi määramine</span><span class="sxs-lookup"><span data-stu-id="2652a-229">Assign cluster</span></span>
    - <span data-ttu-id="2652a-230">Kogumi kõrvalepanek</span><span class="sxs-lookup"><span data-stu-id="2652a-230">Cluster putaway</span></span>

## <a name="example-scenario"></a><span data-ttu-id="2652a-231">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="2652a-231">Example scenario</span></span>

<span data-ttu-id="2652a-232">See stsenaarium simuleerib ladustatava kogumi töötlemist.</span><span class="sxs-lookup"><span data-stu-id="2652a-232">This scenario simulates putaway cluster processing.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="2652a-233">Ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="2652a-233">Create a purchase order</span></span>

1. <span data-ttu-id="2652a-234">Avage jaotis **Ostureskontro \> Ostutellimused \> Kõik ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="2652a-234">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="2652a-235">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2652a-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="2652a-236">Dialoogiboksis **Ostutellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="2652a-236">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="2652a-237">**Hankija konto:** *1001*</span><span class="sxs-lookup"><span data-stu-id="2652a-237">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="2652a-238">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="2652a-238">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="2652a-239">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2652a-239">Select **OK**.</span></span>

    <span data-ttu-id="2652a-240">Ilmub leht **Kõik ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="2652a-240">The **All purchase orders** page appears.</span></span>

1. <span data-ttu-id="2652a-241">Klõpsake **Kõik ostutellimused** lehe kiirkaardil **Ostutellimuse read** nuppu **Lisa rida**, et lisada järgmised read:</span><span class="sxs-lookup"><span data-stu-id="2652a-241">On the **All purchase orders** page, on the **Purchase order lines** FastTab, use the **Add line** button to add the following lines:</span></span>

    - <span data-ttu-id="2652a-242">Ostutellimuse rida 1:</span><span class="sxs-lookup"><span data-stu-id="2652a-242">Purchase order line 1:</span></span>

        - <span data-ttu-id="2652a-243">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="2652a-243">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="2652a-244">**Kogus:** *10*</span><span class="sxs-lookup"><span data-stu-id="2652a-244">**Quantity:** *10*</span></span>

    - <span data-ttu-id="2652a-245">Ostutellimuse rida 2:</span><span class="sxs-lookup"><span data-stu-id="2652a-245">Purchase order line 2:</span></span>

        - <span data-ttu-id="2652a-246">**Kauba kood:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="2652a-246">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="2652a-247">**Kogus:** *20*</span><span class="sxs-lookup"><span data-stu-id="2652a-247">**Quantity:** *20*</span></span>

    - <span data-ttu-id="2652a-248">Ostutellimuse rida 3:</span><span class="sxs-lookup"><span data-stu-id="2652a-248">Purchase order line 3:</span></span>

        - <span data-ttu-id="2652a-249">**Kauba kood:** *M9215*</span><span class="sxs-lookup"><span data-stu-id="2652a-249">**Item number:** *M9215*</span></span>
        - <span data-ttu-id="2652a-250">**Kogus:** *30*</span><span class="sxs-lookup"><span data-stu-id="2652a-250">**Quantity:** *30*</span></span>

1. <span data-ttu-id="2652a-251">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2652a-251">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="2652a-252">Märkige üles ostutellimuse number.</span><span class="sxs-lookup"><span data-stu-id="2652a-252">Make a note of the purchase order number.</span></span>

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a><span data-ttu-id="2652a-253">Võtke varud vastu ja pange mobiilselt seadmelt ära</span><span class="sxs-lookup"><span data-stu-id="2652a-253">Receive inventory and put it away from the mobile device</span></span>

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a><span data-ttu-id="2652a-254">Võtke kaup vastu ja sortige kogumisse</span><span class="sxs-lookup"><span data-stu-id="2652a-254">Receive and sort the inventory into a cluster</span></span>

1. <span data-ttu-id="2652a-255">Logige mobiilirakendusse Warehouse Management sisse kasutajana, kes on seadistatud lao *61* jaoks.</span><span class="sxs-lookup"><span data-stu-id="2652a-255">Sign in to the Warehouse Management mobile app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="2652a-256">Valige peamenüüs suvand **Sissetulev**.</span><span class="sxs-lookup"><span data-stu-id="2652a-256">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="2652a-257">**Sissetulev** menüüs valige **Võta vastu ja sordi kogum**.</span><span class="sxs-lookup"><span data-stu-id="2652a-257">On the **Inbound** menu, select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="2652a-258">Sisestage väljale **Ponum** ostutellimuse number.</span><span class="sxs-lookup"><span data-stu-id="2652a-258">In the **Ponum** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="2652a-259">Valige **OK** (märkenupp).</span><span class="sxs-lookup"><span data-stu-id="2652a-259">Select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="2652a-260">Valige väli **Kaup**, sisestage kauba number *A0001* ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="2652a-260">Select the **Item** field, enter item number *A0001*, and then select **OK**.</span></span>
1. <span data-ttu-id="2652a-261">Valige väli **Kogus**, sisestage *10*, kasutades numbriklahvistikku ja märkige seejärel märkeruut.</span><span class="sxs-lookup"><span data-stu-id="2652a-261">Select the **Qty** field, enter *10* by using the number pad, and then select the check mark button.</span></span>
1. <span data-ttu-id="2652a-262">Valige ülesande lehel **Kogus** sisestatud koguse kinnitamiseks **OK** (märkeruut).</span><span class="sxs-lookup"><span data-stu-id="2652a-262">On the **Qty** task page, select **OK** (the check mark button) to confirm the quantity that you entered.</span></span>
1. <span data-ttu-id="2652a-263">**Üksuse** ülesande lehel valige **OK**, et kinnitada *A0001* üksuse sisestamine.</span><span class="sxs-lookup"><span data-stu-id="2652a-263">On the **Item** task page, select **OK** to confirm that item *A0001* was entered.</span></span>
1. <span data-ttu-id="2652a-264">Valige **Kogumi ID** väli ja sisestage väärtus, et määrata loodavale kogumile ID.</span><span class="sxs-lookup"><span data-stu-id="2652a-264">Select the **Cluster ID** field, and enter a value to assign an ID for the cluster that you're creating.</span></span>

    <span data-ttu-id="2652a-265">Siin sisestatud ID-d kasutatakse siis, kui ostutellimuse kaks järelejäänud kaupa on vastu võetud.</span><span class="sxs-lookup"><span data-stu-id="2652a-265">The ID that you enter here will be used when the two remaining items on the purchase order are received.</span></span>

1. <span data-ttu-id="2652a-266">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2652a-266">Select **OK**.</span></span>

    <span data-ttu-id="2652a-267">Ilmub **Ponum** ülesande leht ja kuvatakse teade "Töö lõpetatud".</span><span class="sxs-lookup"><span data-stu-id="2652a-267">The **Ponum** task page appears and shows a "Work completed" message.</span></span>

    <span data-ttu-id="2652a-268">Kaup *A0001* on nüüd *RECV* asukohta vastu võetud ja määratud kogumi ID-le, mille sisestasite sammus 10.</span><span class="sxs-lookup"><span data-stu-id="2652a-268">Item *A0001* has now been received into the *RECV* location and assigned to the cluster ID that you entered in step 10.</span></span>

1. <span data-ttu-id="2652a-269">Korrake samme 4 kuni 11, et saada ostutellimusest ülejäänud kaks kaupa ja määrata need klastri ID-le:</span><span class="sxs-lookup"><span data-stu-id="2652a-269">Repeat steps 4 through 11 to receive the remaining two items from the purchase order and assign them to the cluster ID:</span></span>

    - <span data-ttu-id="2652a-270">Kauba *A0002* kogus *20*</span><span class="sxs-lookup"><span data-stu-id="2652a-270">A quantity of *20* for item *A0002*</span></span>
    - <span data-ttu-id="2652a-271">Kauba *M9215* kogus *30*</span><span class="sxs-lookup"><span data-stu-id="2652a-271">A quantity of *30* for item *M9215*</span></span>

#### <a name="close-the-cluster"></a><span data-ttu-id="2652a-272">Kogumi sulgemine</span><span class="sxs-lookup"><span data-stu-id="2652a-272">Close the cluster</span></span>

<span data-ttu-id="2652a-273">Enne kui kogumis olevad kaubad saab ladustada, peab kogum olema suletud.</span><span class="sxs-lookup"><span data-stu-id="2652a-273">Before the items in the cluster can be put away, the cluster must be closed.</span></span>

1. <span data-ttu-id="2652a-274">Minge Supply Chain Managementis **Laohaldus \> Töö \> Väljaminev \> Töökogumid**.</span><span class="sxs-lookup"><span data-stu-id="2652a-274">In Supply Chain Management, go to **Warehouse management \> Work \> Outbound \> Work clusters**.</span></span>
1. <span data-ttu-id="2652a-275">Otsige **Töökogumid** lehe **Töökogumid** jaotisest **Kogumi ID** väljalt eelnevalt sisestatud kogumi ID-d.</span><span class="sxs-lookup"><span data-stu-id="2652a-275">On the **Work clusters** page, in the **Work cluster** section, search the **Cluster ID** field for the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="2652a-276">Kui kogumit ei ole kuvatud, võib see olla juba suletud.</span><span class="sxs-lookup"><span data-stu-id="2652a-276">If the cluster isn't shown, it might already have been closed.</span></span> <span data-ttu-id="2652a-277">Määramaks, kas kogum suleti, märkige **Kuva suletud töö** valikruut ja otsige eelnevalt sisestatud kogumi ID-d.</span><span class="sxs-lookup"><span data-stu-id="2652a-277">To determine whether the cluster was closed, select the **Show closed work** check box, and search for the cluster ID that you entered earlier.</span></span> <span data-ttu-id="2652a-278">Seejärel järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="2652a-278">Then follow one of these steps:</span></span>

    - <span data-ttu-id="2652a-279">Kui kogum on suletud, jätke selle protseduuri ülejäänud sammud vahele ja liikuge edasi järgmisele protseduurile, [Kogumi ladustamine](#put-the-cluster-away).</span><span class="sxs-lookup"><span data-stu-id="2652a-279">If the cluster has been closed, skip the remaining steps of this procedure, and move on to the next procedure, [Put the cluster away](#put-the-cluster-away).</span></span>
    - <span data-ttu-id="2652a-280">Kui kogum ei ole suletud, järgige selle protseduuri järelejäänud etappe, et kogum käsitsi sulgeda.</span><span class="sxs-lookup"><span data-stu-id="2652a-280">If the cluster hasn't been closed, follow the remaining steps of this procedure to manually close the cluster.</span></span> <span data-ttu-id="2652a-281">Seejärel minge edasi järgmise protseduuri juurde.</span><span class="sxs-lookup"><span data-stu-id="2652a-281">Then move on to the next procedure.</span></span>

1. <span data-ttu-id="2652a-282">Valige **Töökogumi** jaotises eelnevalt sisestatud kogumi ID.</span><span class="sxs-lookup"><span data-stu-id="2652a-282">In the **Work cluster** section, select the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="2652a-283">Valige toimingupaanil nupp **Sule kogum**.</span><span class="sxs-lookup"><span data-stu-id="2652a-283">On the Action Pane, select **Close cluster**.</span></span>

    <span data-ttu-id="2652a-284">Pärast seda, kui kogum on suletud, ei kuvata seda enam **Töökogumi** jaotises (välja arvatud juhul, kui **Kuva suletud töö** märkeruut on märgitud).</span><span class="sxs-lookup"><span data-stu-id="2652a-284">After the cluster has been closed, it's no longer shown in the **Work cluster** section (unless the **Show closed work** check box is selected).</span></span>

#### <a name="put-the-cluster-away"></a><span data-ttu-id="2652a-285">Ladusta kogum</span><span class="sxs-lookup"><span data-stu-id="2652a-285">Put the cluster away</span></span>

1. <span data-ttu-id="2652a-286">Logige mobiilirakendusse Warehouse Management sisse kasutajana, kes on seadistatud lao *61* jaoks.</span><span class="sxs-lookup"><span data-stu-id="2652a-286">Sign in to the Warehouse Management mobile app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="2652a-287">Valige peamenüüs suvand **Sissetulev**.</span><span class="sxs-lookup"><span data-stu-id="2652a-287">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="2652a-288">Valige **Sissetulev** menüüs **Kogumi ladustamine**.</span><span class="sxs-lookup"><span data-stu-id="2652a-288">On the **Inbound** menu, select **Cluster putaway**.</span></span>
1. <span data-ttu-id="2652a-289">Valige **Kogumi ID** ja sisestage kogumi ID, mille sisestasite varasemalt suletud kogumi jaoks.</span><span class="sxs-lookup"><span data-stu-id="2652a-289">Select **Cluster ID**, and enter the cluster ID that you entered earlier for the closed cluster.</span></span>
1. <span data-ttu-id="2652a-290">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2652a-290">Select **OK**.</span></span>

    <span data-ttu-id="2652a-291">Kuvatakse leht **Kogumi ladustamine: Komplekteeri**.</span><span class="sxs-lookup"><span data-stu-id="2652a-291">The **Cluster putaway: Pick** page appears.</span></span> <span data-ttu-id="2652a-292">See näitab kogumi ID-d, komplekteerimise asukohta, kaupu (kuvatakse väärtus *Mitu*) ja kogumi lõppkogus, mis tuleb komplekteerida.</span><span class="sxs-lookup"><span data-stu-id="2652a-292">It shows the cluster ID, the picking location, the items (the value *Multiple* will be shown), and the total quantity in the cluster that must be picked.</span></span>

1. <span data-ttu-id="2652a-293">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2652a-293">Select **OK**.</span></span>

    <span data-ttu-id="2652a-294">Kuvatakse leht **Kogumi ladustamine: Ladusta**.</span><span class="sxs-lookup"><span data-stu-id="2652a-294">The **Cluster putaway: Put** page appears.</span></span> <span data-ttu-id="2652a-295">**Ladusta** juhistes määratletakse kogumi ID, ladustamise asukoht, kaubad, kogus kokku ja identifitseerimisnumbrid kogumis olevate kaupade jaoks.</span><span class="sxs-lookup"><span data-stu-id="2652a-295">The **Put** instructions identify the cluster ID, the put location, the items, the total quantity, and the license plate IDs for the items that have been received on the cluster.</span></span>

    <span data-ttu-id="2652a-296">Teil on kindlad valikud selle etapi alistamiseks või vahele jätmiseks.</span><span class="sxs-lookup"><span data-stu-id="2652a-296">You have the standard options to override or pass this step.</span></span>

    <span data-ttu-id="2652a-297">![Kogumi ladustamine: Komplekteerimise leht](media/Cluster_putaway-Put.png "Kogumi ladustamine: Komplekteerimise leht")</span><span class="sxs-lookup"><span data-stu-id="2652a-297">![Cluster putaway: Put page](media/Cluster_putaway-Put.png "Cluster putaway: Put page")</span></span>

1. <span data-ttu-id="2652a-298">Kogumi ladustamise kinnitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="2652a-298">Select **OK** to confirm the putaway of the cluster.</span></span>

    <span data-ttu-id="2652a-299">Kuvatakse teade „Kogum on lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="2652a-299">A "Cluster completed" message is shown.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="2652a-300">Märkmed ja näpunäited</span><span class="sxs-lookup"><span data-stu-id="2652a-300">Notes and tips</span></span>

<span data-ttu-id="2652a-301">Juhtudel, kus kogumi ID muutub pesastatud kaubaaluse peamiseks identifitseerimisnumbriks, antakse ladustamisasukoht automaatselt, kui kogumi ID on skaneeritud.</span><span class="sxs-lookup"><span data-stu-id="2652a-301">For cases where the cluster ID becomes the parent license plate for a nested pallet, the put position is automatically given when the cluster ID is scanned.</span></span> <span data-ttu-id="2652a-302">Täiendavat identifitseerimisnumbrit ei tohi skaneerida, isegi kui identifitseerimisnumbri loomine on seatud käsitsi.</span><span class="sxs-lookup"><span data-stu-id="2652a-302">No further license plate must be scanned, even if license plate generation is set to manual.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]