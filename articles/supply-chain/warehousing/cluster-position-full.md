---
title: Kogumi positsioon on täis
description: Sellest teemast leiate teavet funktsiooni „Kogumi positsioon on täis” kohta. See funktsioon pakub alternatiivi tööjaotuse reeglite jäigemale jõustamisele kogumi komplekteerimisel, kuna see võimaldab suuremat veavaru konteinerite või koormate mahupiirangutes.
author: Mirzaab
manager: tfehr
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9c90380cb5d109e331a2552ba779525b66d10fa6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001095"
---
# <a name="cluster-position-full"></a><span data-ttu-id="afe47-104">Kogumi positsioon on täis</span><span class="sxs-lookup"><span data-stu-id="afe47-104">Cluster position full</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afe47-105">Funktsioon *Kogumi positsioon on täis* pakub alternatiivi tööjaotuse reeglite jäigemale jõustamisele kogumi komplekteerimisel, kuna see võimaldab suuremat veavaru konteinerite või koormate mahupiirangutes.</span><span class="sxs-lookup"><span data-stu-id="afe47-105">The *Cluster position full* feature offers an alternative to more rigid enforcement of work break rules when cluster picking is used, because it enables a larger margin of error in the volumetric constraints of containers or totes.</span></span> <span data-ttu-id="afe47-106">Tavaliselt ei mahu kõik töökäsu kaubad valitud konteinerisse.</span><span class="sxs-lookup"><span data-stu-id="afe47-106">In a common scenario, not all items on a work order fit into a selected container.</span></span> <span data-ttu-id="afe47-107">Kogumeid komplekteerivatel laotöötajatel on selle stsenaariumi korral vähe võimalusi: nad peavad muutuma konteinerit suuremaks või pidama nõu juhiga, et leida muu lahendus.</span><span class="sxs-lookup"><span data-stu-id="afe47-107">Warehouse workers who are cluster picking have few options in this scenario: they must either change to a larger container size or work with their supervisor to come up with a different solution.</span></span>

<span data-ttu-id="afe47-108">See funktsioon pakub võimalust kasutada nuppu **Täielik** ühe kogumi tööüksuse korral.</span><span class="sxs-lookup"><span data-stu-id="afe47-108">This feature introduces the ability to run the **Full** button on one of the work units in a cluster.</span></span> <span data-ttu-id="afe47-109">Vanemates versioonides oli see suvand saadaval ainult tavalise tellimuse komplekteerimiseks, mitte kogumi komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="afe47-109">In older versions, this option was available only for regular order picking, not for cluster picking.</span></span> <span data-ttu-id="afe47-110">See funktsioon erineb standardsest nupust **Täielik**, kuna see tühistab ülejäänud töö.</span><span class="sxs-lookup"><span data-stu-id="afe47-110">However, this feature differs from the standard **Full** button in that it cancels the remaining work.</span></span> <span data-ttu-id="afe47-111">See ei viita sellele, et kasutaja lisab samasse kogumisse veel ühe asukoha ning see ei loo automaatselt uut tööd.</span><span class="sxs-lookup"><span data-stu-id="afe47-111">It doesn't suggest that the user add another bin to the same cluster, and it doesn't automatically create new work.</span></span>

## <a name="turn-on-the-cluster-position-full-feature"></a><span data-ttu-id="afe47-112">Funktsiooni „Kogumi positsioon on täis” sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="afe47-112">Turn on the Cluster position full feature</span></span>

<span data-ttu-id="afe47-113">Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="afe47-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="afe47-114">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="afe47-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="afe47-115">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="afe47-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="afe47-116">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="afe47-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="afe47-117">**Funktsiooni nimi:** *Kogumi positsioon on täis*</span><span class="sxs-lookup"><span data-stu-id="afe47-117">**Feature name:** *Cluster position full*</span></span>

## <a name="setup"></a><span data-ttu-id="afe47-118">Seadistus</span><span class="sxs-lookup"><span data-stu-id="afe47-118">Setup</span></span>

<span data-ttu-id="afe47-119">Selles jaotises on toodud juhised ja näide selle kohta, kuidas seadistada ja kasutada funktsiooni *Kogumi positsioon on täis*.</span><span class="sxs-lookup"><span data-stu-id="afe47-119">This section provides guidelines, and an example that shows how to set up and use the *Cluster position full* feature.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="afe47-120">Näidisandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="afe47-120">Make sample data available</span></span>

<span data-ttu-id="afe47-121">Selle [näidisstsenaariumi](#example-scenario) kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="afe47-121">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="afe47-122">Enne alustamist peate valima ka juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="afe47-122">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="afe47-123">Seda näidisstsenaariumi saate kasutada ka juhistena funktsiooni kasutamiseks, kui töötate tootmissüsteemis.</span><span class="sxs-lookup"><span data-stu-id="afe47-123">You can also use the example scenario as guidance for working with this feature on a production system.</span></span> <span data-ttu-id="afe47-124">Sel juhul tuleb teil siiski sisestada oma väärtused siin kirjeldatud sätete jaoks.</span><span class="sxs-lookup"><span data-stu-id="afe47-124">However, in that case, you must substitute your own values for the settings that are described here.</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="afe47-125">Kogumiprofiilid</span><span class="sxs-lookup"><span data-stu-id="afe47-125">Cluster profiles</span></span>

<span data-ttu-id="afe47-126">Peate määrama, kas kogumi ID luuakse automaatselt, kui mitut positsioone kasutatakse, kui kogumid on tükeldatud ning kuidas komplekteerimistööd järjestatakse ja kontrollitakse.</span><span class="sxs-lookup"><span data-stu-id="afe47-126">You must specify whether cluster IDs are automatically generated, how many positions are used, when clusters are broken, and how the picking work is sequenced and verified.</span></span>

1. <span data-ttu-id="afe47-127">Avage **Laohaldus \> Seadistamine \> Mobiilne seade \> Kogumiprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="afe47-127">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="afe47-128">Valige loendipaanil kirje **Loo kogum**.</span><span class="sxs-lookup"><span data-stu-id="afe47-128">In the list pane, select the **Create Cluster** record.</span></span>
1. <span data-ttu-id="afe47-129">Määrake kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="afe47-129">On the **General** FastTab, verify the following values:</span></span>

    - <span data-ttu-id="afe47-130">**Loo kogumi ID:** *jah*</span><span class="sxs-lookup"><span data-stu-id="afe47-130">**Generate cluster ID:** *Yes*</span></span>
    - <span data-ttu-id="afe47-131">**Aktiveeri ametikohad:** *jah*</span><span class="sxs-lookup"><span data-stu-id="afe47-131">**Activate positions:** *Yes*</span></span>
    - <span data-ttu-id="afe47-132">**Ametikohtade arv:** *2*</span><span class="sxs-lookup"><span data-stu-id="afe47-132">**Number of positions:** *2*</span></span>
    - <span data-ttu-id="afe47-133">**Ametikoha nimi:** *numbriline*</span><span class="sxs-lookup"><span data-stu-id="afe47-133">**Position name:** *Numeric*</span></span>
    - <span data-ttu-id="afe47-134">**Tükelda kogum asukohas:** *pane*</span><span class="sxs-lookup"><span data-stu-id="afe47-134">**Break cluster at:** *Put*</span></span>
    - <span data-ttu-id="afe47-135">**Sortimise kontrollimistüüp:** *asukoha skannimine*</span><span class="sxs-lookup"><span data-stu-id="afe47-135">**Sort verification type:** *Position scan*</span></span>

1. <span data-ttu-id="afe47-136">Kiirkaardil **Kogumi sortimine**.</span><span class="sxs-lookup"><span data-stu-id="afe47-136">In the **Cluster sorting** FastTab.</span></span> <span data-ttu-id="afe47-137">Ruudustik peaks olema tühi (st see ei tohi sisaldada ridu).</span><span class="sxs-lookup"><span data-stu-id="afe47-137">The grid should be blank (that is, it should contain no lines).</span></span>

### <a name="work-templates"></a><span data-ttu-id="afe47-138">Töömallid</span><span class="sxs-lookup"><span data-stu-id="afe47-138">Work templates</span></span>

<span data-ttu-id="afe47-139">Peate määrama, kuidas luuakse komplekteerimistöö kogumi komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="afe47-139">You must define how the picking work for cluster picking is created.</span></span>

1. <span data-ttu-id="afe47-140">Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.</span><span class="sxs-lookup"><span data-stu-id="afe47-140">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="afe47-141">Seadke lehe ülaosas välja **Töökäsu tüüp** väärtuseks *Müügitellimused*.</span><span class="sxs-lookup"><span data-stu-id="afe47-141">At the top of the page, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="afe47-142">Veenduge, et järgnevad demoandmete töömallid on loetletud.</span><span class="sxs-lookup"><span data-stu-id="afe47-142">Make sure that the following work templates from the demo data are listed.</span></span> <span data-ttu-id="afe47-143">Kui need pole saadaval, ei saa te stsenaariumi lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="afe47-143">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="afe47-144">61 SO etapp</span><span class="sxs-lookup"><span data-stu-id="afe47-144">61 SO Stage</span></span>
    - <span data-ttu-id="afe47-145">61 SO kogumi komplekteerimine</span><span class="sxs-lookup"><span data-stu-id="afe47-145">61 SO Cluster pick</span></span>

### <a name="location-directives"></a><span data-ttu-id="afe47-146">Asukohakorraldus</span><span class="sxs-lookup"><span data-stu-id="afe47-146">Location directives</span></span>

<span data-ttu-id="afe47-147">Peate määrama, millisest asukohast kaubad komplekteeritakse ja kuhu need pannakse.</span><span class="sxs-lookup"><span data-stu-id="afe47-147">You must specify where items are picked from and where they are put.</span></span>

1. <span data-ttu-id="afe47-148">Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.</span><span class="sxs-lookup"><span data-stu-id="afe47-148">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="afe47-149">Seadke loendi päises välja **Töökäsu tüüp** väärtuseks *Müügitellimus*.</span><span class="sxs-lookup"><span data-stu-id="afe47-149">In the list header, set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="afe47-150">Veenduge, et järgnevad demoandmete müügitellimusekorraldused on loetletud.</span><span class="sxs-lookup"><span data-stu-id="afe47-150">Make sure that the following sales order directives from the demo data are listed.</span></span> <span data-ttu-id="afe47-151">Kui need pole saadaval, ei saa te stsenaariumi lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="afe47-151">If they aren't available, you won't be able to complete the scenario.</span></span>

    - <span data-ttu-id="afe47-152">61 kogumi komplekteerimine</span><span class="sxs-lookup"><span data-stu-id="afe47-152">61 Cluster pick</span></span>
    - <span data-ttu-id="afe47-153">61 SO-komplekteerimise tellimus</span><span class="sxs-lookup"><span data-stu-id="afe47-153">61 SO Pick order</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="afe47-154">Mobiilse seadme menüü-üksused</span><span class="sxs-lookup"><span data-stu-id="afe47-154">Mobile device menu items</span></span>

<span data-ttu-id="afe47-155">Peate konfigureerima mobiilse seadme menüü-üksuse kasutama olemasolevat tööd, mida juhitakse kogumi komplekteerimisega.</span><span class="sxs-lookup"><span data-stu-id="afe47-155">You must configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="afe47-156">Kogumi komplekteerimiseks tuleb sisse lülitada mobiilse seadme menüü-üksuses parameeter **Luba töö tükeldamine** ja lisada tööklass *SO-komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="afe47-156">In the mobile device menu item for cluster picking, the **Allow splitting of work** parameter must be turned on, and the *SO Pick* work class must be added.</span></span>

1. <span data-ttu-id="afe47-157">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="afe47-157">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="afe47-158">Valige loendipaanil kirje **Kogumi komplekteerimise loomine**.</span><span class="sxs-lookup"><span data-stu-id="afe47-158">In the list pane, select the **Cluster Pick Create** record.</span></span>
1. <span data-ttu-id="afe47-159">Valige tegevuse paanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="afe47-159">Select **Edit** in the Action pane.</span></span>
1. <span data-ttu-id="afe47-160">Määrake kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="afe47-160">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="afe47-161">**Juhataja:** *Kogumi komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="afe47-161">**Directed by:** *Cluster picking*</span></span>
    - <span data-ttu-id="afe47-162">**Loo litsentsiplaat:** *jah*</span><span class="sxs-lookup"><span data-stu-id="afe47-162">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="afe47-163">**Luba töö tükeldamine:** *jah*</span><span class="sxs-lookup"><span data-stu-id="afe47-163">**Allow splitting of work:** *Yes*</span></span>
    - <span data-ttu-id="afe47-164">**Kogumi profiili ID:** *Loo kogum*</span><span class="sxs-lookup"><span data-stu-id="afe47-164">**Cluster profile ID:** *Create Cluster*</span></span>

    <span data-ttu-id="afe47-165">Võtke vastu vaikeväärtused kõigil teistel väljadel.</span><span class="sxs-lookup"><span data-stu-id="afe47-165">Accept the default values for all other fields.</span></span>

1. <span data-ttu-id="afe47-166">Lisage kiirkaardil **Tööklassid** kaks järgmist rida vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="afe47-166">On the **Work classes** FastTab, add the following two lines, as required:</span></span>

    - <span data-ttu-id="afe47-167">Rida 1 (tavaliselt olemas demoandmetes):</span><span class="sxs-lookup"><span data-stu-id="afe47-167">Line 1 (usually present in demo data):</span></span>

        - <span data-ttu-id="afe47-168">**Tööklassi ID:** *müük*</span><span class="sxs-lookup"><span data-stu-id="afe47-168">**Work class ID:** *Sales*</span></span> 
        - <span data-ttu-id="afe47-169">**Töökäsu tüüp:** *müügitellimused*</span><span class="sxs-lookup"><span data-stu-id="afe47-169">**Work order type:** *Sales orders*</span></span>

    - <span data-ttu-id="afe47-170">Rida 2 (ei pruugi olla demoandmetes olemas):</span><span class="sxs-lookup"><span data-stu-id="afe47-170">Line 2 (probably not present in demo data):</span></span>

        - <span data-ttu-id="afe47-171">**Töö klassi ID:** *SO-komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="afe47-171">**Work class ID:** *SO Pick*</span></span>
        - <span data-ttu-id="afe47-172">**Töökäsu tüüp:** *müügitellimused*</span><span class="sxs-lookup"><span data-stu-id="afe47-172">**Work order type:** *Sales orders*</span></span>

1. <span data-ttu-id="afe47-173">Avage tegevuse paanil **Töö kinnituse häälestus**.</span><span class="sxs-lookup"><span data-stu-id="afe47-173">Go to **Work confirmation setup** in the Action pane.</span></span>
1. <span data-ttu-id="afe47-174">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="afe47-174">Select **Edit**.</span></span>
1. <span data-ttu-id="afe47-175">Sisestage ruudustiku reale järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="afe47-175">Enter the following values on the line in grid.</span></span>
    - <span data-ttu-id="afe47-176">**Töö tüüp** - *Komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="afe47-176">**Work type** - *Pick*</span></span>
    - <span data-ttu-id="afe47-177">**Toote kinnitus** - *Valige märkeruut*</span><span class="sxs-lookup"><span data-stu-id="afe47-177">**Product confirmation** - *Select the check box*</span></span>

1. <span data-ttu-id="afe47-178">Valige tegevuse paanil **Salvesta** ja sulgege lehekülg.</span><span class="sxs-lookup"><span data-stu-id="afe47-178">Select **Save** in the Action pane and close the page.</span></span>

## <a name="create-picking-work"></a><span data-ttu-id="afe47-179">Komplekteerimistöö loomine</span><span class="sxs-lookup"><span data-stu-id="afe47-179">Create picking work</span></span>

<span data-ttu-id="afe47-180">Enne kui saate alustada kogumi komplekteerimist, peate looma mõne väljamineva töö.</span><span class="sxs-lookup"><span data-stu-id="afe47-180">Before you can start cluster picking, you must create some outbound work.</span></span> <span data-ttu-id="afe47-181">Varasemalt loodud kogumiprofiil määrab kaks kogumi positsiooni.</span><span class="sxs-lookup"><span data-stu-id="afe47-181">The cluster profile that you created earlier specifies two cluster positions.</span></span> <span data-ttu-id="afe47-182">Seetõttu tuleb müügitellimuse komplekteerimiseks luua vähemalt kaks töö ID-d.</span><span class="sxs-lookup"><span data-stu-id="afe47-182">Therefore, at least two work IDs must be created for sales order picking.</span></span> <span data-ttu-id="afe47-183">Selle stsenaariumi korral tehakse kandeid laos *61* ning kasutatakse kaupu *L0101* ja *T0100*.</span><span class="sxs-lookup"><span data-stu-id="afe47-183">For this scenario, transactions will occur in warehouse *61*, and they will use items *L0101* and *T0100*.</span></span> <span data-ttu-id="afe47-184">Demoandmetel peaks olema piisavalt nende kaupade vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="afe47-184">The demo data should have enough on-hand inventory of these items.</span></span> <span data-ttu-id="afe47-185">Veenduge, et teil on kannete lõpetamiseks piisavalt varusid.</span><span class="sxs-lookup"><span data-stu-id="afe47-185">Make sure that you have enough inventory to complete the transactions.</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="afe47-186">Müügitellimuse 1 loomine</span><span class="sxs-lookup"><span data-stu-id="afe47-186">Create sales order 1</span></span>

1. <span data-ttu-id="afe47-187">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="afe47-187">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="afe47-188">Müügitellimuse 1 loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="afe47-188">Select **New** to create sales order 1.</span></span>
1. <span data-ttu-id="afe47-189">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="afe47-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="afe47-190">**Kliendi konto:** *US-010*</span><span class="sxs-lookup"><span data-stu-id="afe47-190">**Customer account:** *US-010*</span></span>
    - <span data-ttu-id="afe47-191">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="afe47-191">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="afe47-192">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="afe47-192">Select **OK**.</span></span>
1. <span data-ttu-id="afe47-193">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="afe47-193">The new sales order is opened.</span></span> <span data-ttu-id="afe47-194">Lisage kiirkaardil **Müügitellimuse read** järgmiste sätetega rida.</span><span class="sxs-lookup"><span data-stu-id="afe47-194">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="afe47-195">**Kauba kood:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="afe47-195">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="afe47-196">**Kogus:** *5*</span><span class="sxs-lookup"><span data-stu-id="afe47-196">**Quantity:** *5*</span></span>

1. <span data-ttu-id="afe47-197">Määrake kiirkaardi **Rea üksikasjad** vahekaardi **Tarne** välja **Kinnitatud tarnekuupäev** väärtuseks tänane kuupäev.</span><span class="sxs-lookup"><span data-stu-id="afe47-197">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="afe47-198">Lisage kiirkaardil **Müügitellimuse read** järgmiste sätetega teine rida.</span><span class="sxs-lookup"><span data-stu-id="afe47-198">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="afe47-199">**Kauba kood:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="afe47-199">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="afe47-200">**Kogus:** *20*</span><span class="sxs-lookup"><span data-stu-id="afe47-200">**Quantity:** *20*</span></span>

1. <span data-ttu-id="afe47-201">Määrake kiirkaardi **Rea üksikasjad** vahekaardi **Tarne** välja **Kinnitatud tarnekuupäev** väärtuseks tänane kuupäev.</span><span class="sxs-lookup"><span data-stu-id="afe47-201">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="afe47-202">Iga äsja lisatud rea korral järgige varude reserveerimiseks järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="afe47-202">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="afe47-203">Valige reserveeritav rida.</span><span class="sxs-lookup"><span data-stu-id="afe47-203">Select the line to reserve.</span></span>
    2. <span data-ttu-id="afe47-204">Tehke kiirkaardil **Müügitellimuse read** valik **Varud \> Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="afe47-204">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="afe47-205">Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida varud.</span><span class="sxs-lookup"><span data-stu-id="afe47-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="afe47-206">Sulgege leht **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="afe47-206">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="afe47-207">Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="afe47-207">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="afe47-208">Kui väljalase on lõpule viidud, saate teabesõnumeid, mis näitavad loodud voo ja koormuse ID-sid.</span><span class="sxs-lookup"><span data-stu-id="afe47-208">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="afe47-209">Müügitellimuse 2 loomine</span><span class="sxs-lookup"><span data-stu-id="afe47-209">Create sales order 2</span></span>

1. <span data-ttu-id="afe47-210">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="afe47-210">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="afe47-211">Müügitellimuse 2 loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="afe47-211">Select **New** to create sales order 2.</span></span>
1. <span data-ttu-id="afe47-212">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="afe47-212">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="afe47-213">**Kliendi konto:** *US-011*</span><span class="sxs-lookup"><span data-stu-id="afe47-213">**Customer account:** *US-011*</span></span>
    - <span data-ttu-id="afe47-214">**Ladu:** *61*</span><span class="sxs-lookup"><span data-stu-id="afe47-214">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="afe47-215">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="afe47-215">Select **OK**.</span></span>
1. <span data-ttu-id="afe47-216">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="afe47-216">The new sales order is opened.</span></span> <span data-ttu-id="afe47-217">Lisage kiirkaardil **Müügitellimuse read** järgmiste sätetega rida.</span><span class="sxs-lookup"><span data-stu-id="afe47-217">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="afe47-218">**Kauba kood:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="afe47-218">**Item number:** *L0101*</span></span>
    - <span data-ttu-id="afe47-219">**Kogus:** *20*</span><span class="sxs-lookup"><span data-stu-id="afe47-219">**Quantity:** *20*</span></span>

1. <span data-ttu-id="afe47-220">Määrake kiirkaardi **Rea üksikasjad** vahekaardi **Tarne** välja **Kinnitatud tarnekuupäev** väärtuseks tänane kuupäev.</span><span class="sxs-lookup"><span data-stu-id="afe47-220">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="afe47-221">Lisage kiirkaardil **Müügitellimuse read** järgmiste sätetega teine rida.</span><span class="sxs-lookup"><span data-stu-id="afe47-221">On the **Sales order lines** FastTab, add a second line that has the following settings:</span></span>

    - <span data-ttu-id="afe47-222">**Kauba kood:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="afe47-222">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="afe47-223">**Kogus:** *2*</span><span class="sxs-lookup"><span data-stu-id="afe47-223">**Quantity:** *2*</span></span>

1. <span data-ttu-id="afe47-224">Määrake kiirkaardi **Rea üksikasjad** vahekaardi **Tarne** välja **Kinnitatud tarnekuupäev** väärtuseks tänane kuupäev.</span><span class="sxs-lookup"><span data-stu-id="afe47-224">On the **Line details** FastTab, on the **Delivery** tab, set the **Confirmed ship date** field to today's date.</span></span>
1. <span data-ttu-id="afe47-225">Iga äsja lisatud rea korral järgige varude reserveerimiseks järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="afe47-225">For each line that you just added, follow these steps to reserve inventory:</span></span>

    1. <span data-ttu-id="afe47-226">Valige reserveeritav rida.</span><span class="sxs-lookup"><span data-stu-id="afe47-226">Select the line to reserve.</span></span>
    2. <span data-ttu-id="afe47-227">Tehke kiirkaardil **Müügitellimuse read** valik **Varud \> Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="afe47-227">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
    3. <span data-ttu-id="afe47-228">Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida varud.</span><span class="sxs-lookup"><span data-stu-id="afe47-228">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
    4. <span data-ttu-id="afe47-229">Sulgege leht **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="afe47-229">Close the **Reservation** page.</span></span>

1. <span data-ttu-id="afe47-230">Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="afe47-230">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="afe47-231">Kui väljalase on lõpule viidud, saate teabesõnumeid, mis näitavad loodud voo ja koormuse ID-sid.</span><span class="sxs-lookup"><span data-stu-id="afe47-231">When the release is completed, you receive informational messages that show the wave and load IDs that were created.</span></span>

### <a name="get-work-ids-and-license-plate-numbers"></a><span data-ttu-id="afe47-232">Töö ID-de ja identifitseerimisnumbrite hankimine</span><span class="sxs-lookup"><span data-stu-id="afe47-232">Get work IDs and license plate numbers</span></span>

<span data-ttu-id="afe47-233">Loodud peaks olema kaks töö ID-d, millest igaühel on kaks komplekteerimise rida.</span><span class="sxs-lookup"><span data-stu-id="afe47-233">Two work IDs should have been created, each of which has two pick lines.</span></span> <span data-ttu-id="afe47-234">Järgige neid samme, et leida töö ID-d ja litsentsiplaat määranguid.</span><span class="sxs-lookup"><span data-stu-id="afe47-234">Follow these steps to find the work IDs and license plate assignments.</span></span>

1. <span data-ttu-id="afe47-235">Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="afe47-235">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="afe47-236">Otsige ruudustikust **Ülevaade** veergu **Tellimuse number** kahe äsja loodud müügitellimuse kohta.</span><span class="sxs-lookup"><span data-stu-id="afe47-236">In the **Overview** grid, search the **Order number** column for the two sales orders that you just created.</span></span> <span data-ttu-id="afe47-237">Märkige iga müügitellimuse kohta vastav töö ID.</span><span class="sxs-lookup"><span data-stu-id="afe47-237">For each sales order, make a note of the corresponding work ID.</span></span>
1. <span data-ttu-id="afe47-238">Valige rida iga müügitellimuse jaoks, et kuvada seotud teave ruudustikus **Read**.</span><span class="sxs-lookup"><span data-stu-id="afe47-238">Select the row for each sales order to show related information in the **Lines** grid.</span></span> <span data-ttu-id="afe47-239">Märkige asukoht, kust iga kaup komplekteeritakse.</span><span class="sxs-lookup"><span data-stu-id="afe47-239">Make a note of the location that each item will be picked from.</span></span>
1. <span data-ttu-id="afe47-240">Avage **Laohaldus \> Päringud ja aruanded \> Vabade kaubavarude loend**.</span><span class="sxs-lookup"><span data-stu-id="afe47-240">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="afe47-241">Valige toimingupaanil **Dimensioonid**, et avada dialoogiboks **Dimensiooni kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="afe47-241">On the Action Pane, select **Dimensions** to open the **Dimension display** dialog box.</span></span>
1. <span data-ttu-id="afe47-242">Veenduge, et ruudud **Litsentsiplaat**, **Ladu** ja **Kaubakood** on märgitud ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="afe47-242">Make sure that the **License plate**, **Warehouse**, and **Item number** check boxes are selected, and then select **OK**.</span></span>
1. <span data-ttu-id="afe47-243">Määrake paanil **Filter** järgmised filtrid.</span><span class="sxs-lookup"><span data-stu-id="afe47-243">In the **Filter** pane, set the following filters:</span></span>

    - <span data-ttu-id="afe47-244">**Kaubakood** – **üks (mitmest)** – *L0101* ja *T100*</span><span class="sxs-lookup"><span data-stu-id="afe47-244">**Item number** – **is one of** – *L0101* and *T100*</span></span>
    - <span data-ttu-id="afe47-245">**Ladu** – **algab väärtusega** – *61*</span><span class="sxs-lookup"><span data-stu-id="afe47-245">**Warehouse** – **begins with** – *61*</span></span>

1. <span data-ttu-id="afe47-246">Märkige üles kuvatavad **litsentsiplaadi** väärtused.</span><span class="sxs-lookup"><span data-stu-id="afe47-246">Make a note of the **License plate** values that are shown.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="afe47-247">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="afe47-247">Example scenario</span></span>

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a><span data-ttu-id="afe47-248">Mobiilse seadme voo käivitamine – toote töö kinnituse häälestus</span><span class="sxs-lookup"><span data-stu-id="afe47-248">Mobile device flow execution – Work confirmation setup for the product</span></span>

1. <span data-ttu-id="afe47-249">Logige laorakendusse sisse lao *61* kasutajana.</span><span class="sxs-lookup"><span data-stu-id="afe47-249">Sign in to the warehouse app as a user in warehouse *61*.</span></span>
1. <span data-ttu-id="afe47-250">Valige **Väljaminev \> Kogumi komplekteerimise loomine**.</span><span class="sxs-lookup"><span data-stu-id="afe47-250">Go to **Outbound \> Cluster pick create**.</span></span>

    <span data-ttu-id="afe47-251">Kuvatakse leht **ÜLESANNE: töö määramine kogumile**.</span><span class="sxs-lookup"><span data-stu-id="afe47-251">The **TASK: Assign work to Cluster** page appears.</span></span>

1. <span data-ttu-id="afe47-252">Sisestage müügitellimuse 1 töö ID, et määrata see kogumi positsioonile 1.</span><span class="sxs-lookup"><span data-stu-id="afe47-252">Enter the work ID for sales order 1 to assign it to cluster position 1.</span></span>
1. <span data-ttu-id="afe47-253">Valige **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="afe47-253">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="afe47-254">Sisestage müügitellimuse 2 töö ID, et määrata see kogumi positsioonile 2.</span><span class="sxs-lookup"><span data-stu-id="afe47-254">Enter the work ID for sales order 2 to assign it to cluster position 2.</span></span>
1. <span data-ttu-id="afe47-255">Valige **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="afe47-255">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="afe47-256">Kuvatakse leht **ÜLESANNE: kogumi komplekteerimise loomine: komplekteerimine** ja *Kaup L0101 2 PL*.</span><span class="sxs-lookup"><span data-stu-id="afe47-256">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item L0101 2 PL*.</span></span>

<span data-ttu-id="afe47-257">Kuna kogumi profiil seab positsioonide arvuks 2, suunab süsteem teid automaatselt esimesele konsolideerivale komplekteerimisele: kauba *L0101* kaks kaubaalust (PL).</span><span class="sxs-lookup"><span data-stu-id="afe47-257">Because the cluster profile set the number of positions to 2, the system automatically directs you to the first consolidate pick: two pallets (PL) of item *L0101*.</span></span>

<span data-ttu-id="afe47-258">Järgmistel etappidel saate toimingu kohta lisateabe (nt komplekteerimiskoha) vaatamiseks igal ajal valida vahekaardi **Üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="afe47-258">At any time during the following steps, you can select the **Details** tab to view additional information about the task, such as the picking location.</span></span>

1. <span data-ttu-id="afe47-259">Määrake välja **KAUP** väärtuseks *L0101*.</span><span class="sxs-lookup"><span data-stu-id="afe47-259">Set the **ITEM** field to *L0101*.</span></span> <span data-ttu-id="afe47-260">See kinnitab selle menüü-üksuse jaoks vajaliku kaubakoodi (konfigureerisite selle varem menüü-üksuse loomisel, tehes lehel **Mobiilse seadme menüükäsk** valiku **Töö kinnituse häälestus**).</span><span class="sxs-lookup"><span data-stu-id="afe47-260">This confirms the item number, which is required for this menu item (you configured this earlier by selecting **Work confirmation setup**  from the **Mobile device menu item** page when you created this menu item).</span></span>
1. <span data-ttu-id="afe47-261">Sisestage identifitseerimisnumber, mis on seotud asukohas oleva komplekteeritava kaubaga.</span><span class="sxs-lookup"><span data-stu-id="afe47-261">Enter the license plate number that is associated with the item in the location that is being picked.</span></span> <span data-ttu-id="afe47-262">Peate valima kaks kaubaalust.</span><span class="sxs-lookup"><span data-stu-id="afe47-262">You will pick two pallets.</span></span>
1. <span data-ttu-id="afe47-263">Määrake välja **LP** väärtuseks *LP\_PICK\_01*.</span><span class="sxs-lookup"><span data-stu-id="afe47-263">Set the **LP** field to *LP\_PICK\_01*.</span></span>
1. <span data-ttu-id="afe47-264">Valige **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="afe47-264">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="afe47-265">Kuvatakse leht **ÜLESANNE: sortimine: kogumi komplekteerimise loomine**.</span><span class="sxs-lookup"><span data-stu-id="afe47-265">The **TASK: Sort: Cluster Pick Create** page appears.</span></span> <span data-ttu-id="afe47-266">Siin sordite kaks komplekteeritud kaubaalust komplekteerimise positsioonile.</span><span class="sxs-lookup"><span data-stu-id="afe47-266">Here, you will sort the two picked pallets into a pick position.</span></span> <span data-ttu-id="afe47-267">See positsioon võib olla koorem või konteiner, mida kasutatakse komplekteeritud varude eraldamiseks müügitellimuse järgi.</span><span class="sxs-lookup"><span data-stu-id="afe47-267">This position might be a tote or container that is used to separate the picked inventory by sales order.</span></span>

1. <span data-ttu-id="afe47-268">Vaadake üksikasju, mis kuvatakse kauba (*L0101*) ja koguse (*20* ea) kohta, mis sorditakse positsioonile 1 (müügitellimuse 1 korral).</span><span class="sxs-lookup"><span data-stu-id="afe47-268">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="afe47-269">Seadke välja **POSITSIOONI NIMI** väärtuseks *1*.</span><span class="sxs-lookup"><span data-stu-id="afe47-269">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="afe47-270">Valige **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="afe47-270">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="afe47-271">Vaadake üksikasju, mis kuvatakse kauba (*L0101*) ja koguse (*20* ea) kohta, mis sorditakse positsioonile 2 (müügitellimuse 2 korral).</span><span class="sxs-lookup"><span data-stu-id="afe47-271">View the details that are shown for the item (*L0101*) and quantity (*20* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="afe47-272">Seadke välja **POSITSIOONI NIMI** väärtuseks *2*.</span><span class="sxs-lookup"><span data-stu-id="afe47-272">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="afe47-273">Valige **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="afe47-273">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="afe47-274">Kuvatakse leht **ÜLESANNE: kogumi komplekteerimise loomine: komplekteerimine** ja *Kaup T0100 7 ea*.</span><span class="sxs-lookup"><span data-stu-id="afe47-274">The **TASK: Cluster Pick Create: Pick** page appears and shows *Item T0100 7 ea*.</span></span>

<span data-ttu-id="afe47-275">Selle stsenaariumi korral ei saa positsioon 1 aktsepteerida kaupade täielikku kogust, mis tuleb komplekteerida müügitellimuse 1 täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="afe47-275">In this scenario, position 1 can't accept the full quantity of items that must be picked to fulfill sales order 1.</span></span> <span data-ttu-id="afe47-276">Positsioon peab olema märgitud täielikuna.</span><span class="sxs-lookup"><span data-stu-id="afe47-276">A position must be marked as full.</span></span> <span data-ttu-id="afe47-277">Selle stsenaariumi korral peate viima lõpule teise kauba osalise komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="afe47-277">In this scenario, you will do a partial pick of the second item.</span></span> <span data-ttu-id="afe47-278">Teine kaup komplekteeritakse osaliselt positsiooni 1 jaoks ja luuakse tellimuse täitmiseks uus töö, mille korral komplekteeritakse järelejäänud kogus.</span><span class="sxs-lookup"><span data-stu-id="afe47-278">The second item will be partially picked for position 1, and new work will be created to pick the remaining quantity to fulfill the order.</span></span>

1. <span data-ttu-id="afe47-279">Valige nupp Menüü (nimetatakse mõnikord hamburgeriks või hamburgeri nupuks) ja seejärel valige **Kogumi positsioon on täis**.</span><span class="sxs-lookup"><span data-stu-id="afe47-279">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Position full**.</span></span>
1. <span data-ttu-id="afe47-280">Määrake positsioon, mis on täis, ja valige *1*.</span><span class="sxs-lookup"><span data-stu-id="afe47-280">Identify the position that is full, and select *1*.</span></span>
1. <span data-ttu-id="afe47-281">Valige **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="afe47-281">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="afe47-282">Sisestage komplekteeritav kogus, mida saab endiselt komplekteerida positsioonile 1.</span><span class="sxs-lookup"><span data-stu-id="afe47-282">Enter the pick quantity that can still be picked into position 1.</span></span> <span data-ttu-id="afe47-283">Süsteem saab määrata, millise kaubakoodi järgi komplekteeritakse.</span><span class="sxs-lookup"><span data-stu-id="afe47-283">The system can determine which item number is being picked.</span></span>
1. <span data-ttu-id="afe47-284">Sisestage *2*.</span><span class="sxs-lookup"><span data-stu-id="afe47-284">Enter *2*.</span></span>
1. <span data-ttu-id="afe47-285">Valige **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="afe47-285">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="afe47-286">Ülejäänud kauba positsioonile 2 komplekteerimise lõpuleviimiseks kinnitage kaubakood.</span><span class="sxs-lookup"><span data-stu-id="afe47-286">Confirm the item number to complete the pick of the remaining item into position 2.</span></span>
1. <span data-ttu-id="afe47-287">Määrake välja **KAUP** väärtuseks *T0100*.</span><span class="sxs-lookup"><span data-stu-id="afe47-287">Set the **ITEM** field to *T0100*.</span></span>
1. <span data-ttu-id="afe47-288">Valige **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="afe47-288">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="afe47-289">Sisestage litsentsiplaat, millelt kaup komplekteeritakse, seades välja **LP** väärtuseks *LPREPL04*.</span><span class="sxs-lookup"><span data-stu-id="afe47-289">Enter the license plate that the item is being picked from by setting the **LP** field to *LPREPL04*.</span></span>
1. <span data-ttu-id="afe47-290">Valige **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="afe47-290">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="afe47-291">Vaadake üksikasju, mis kuvatakse kauba (*T0100*) ja koguse (*2* ea) kohta, mis sorditakse positsioonile 2 (müügitellimuse 2 korral).</span><span class="sxs-lookup"><span data-stu-id="afe47-291">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 2 (for sales order 2).</span></span>
1. <span data-ttu-id="afe47-292">Seadke välja **POSITSIOONI NIMI** väärtuseks *2*.</span><span class="sxs-lookup"><span data-stu-id="afe47-292">Set the **POSITION NA** field to *2*.</span></span>
1. <span data-ttu-id="afe47-293">Valige **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="afe47-293">Select **OK** (check mark symbol).</span></span>
1. <span data-ttu-id="afe47-294">Vaadake üksikasju, mis kuvatakse kauba (*T0100*) ja koguse (*2* ea) kohta, mis sorditakse positsioonile 1 (müügitellimuse 1 korral).</span><span class="sxs-lookup"><span data-stu-id="afe47-294">View the details that are shown for the item (*T0100*) and quantity (*2* ea) that will be sorted into position 1 (for sales order 1).</span></span>
1. <span data-ttu-id="afe47-295">Seadke välja **POSITSIOONI NIMI** väärtuseks *1*.</span><span class="sxs-lookup"><span data-stu-id="afe47-295">Set the **POSITION NA** field to *1*.</span></span>
1. <span data-ttu-id="afe47-296">Valige **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="afe47-296">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="afe47-297">Kuvatakse leht **ÜLESANNE: kogumi komplekteerimise loomine: komplekteerimine**.</span><span class="sxs-lookup"><span data-stu-id="afe47-297">The **TASK: Cluster Pick Create: Put** page appears.</span></span>

<span data-ttu-id="afe47-298">Selle stsenaariumi korral on kogumi komplekteerimine lõpule viidud ja kasutaja on suunanud komplekteeritud esemed positsioonist 1 ja 2 vaheasukohta *STAGE01*.</span><span class="sxs-lookup"><span data-stu-id="afe47-298">In this scenario, the cluster pick has been completed, and the user is directed to put away the picked items from position 1 and position 2 into staging location *STAGE01*.</span></span>

1. <span data-ttu-id="afe47-299">Vaadake üle lehel olev teave.</span><span class="sxs-lookup"><span data-stu-id="afe47-299">Review the information on the page.</span></span> <span data-ttu-id="afe47-300">See näitab, et lõplik kogus *44* pannakse vaheasukohta.</span><span class="sxs-lookup"><span data-stu-id="afe47-300">It shows that a total quantity of *44* will be put to the staging location.</span></span>
1. <span data-ttu-id="afe47-301">Valige **OK** (märke sümbol).</span><span class="sxs-lookup"><span data-stu-id="afe47-301">Select **OK** (check mark symbol).</span></span>

    <span data-ttu-id="afe47-302">Teile kuvatakse teade „Kogum on lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="afe47-302">You receive a "Cluster Completed" message.</span></span>

<span data-ttu-id="afe47-303">Ülejäänud koguse komplekteerimiseks saate nüüd kasutada menüükäsku **Müügi komplekteerimine**.</span><span class="sxs-lookup"><span data-stu-id="afe47-303">You can now use the **Sales Picking** menu item to pick the remaining quantity.</span></span> <span data-ttu-id="afe47-304">Seejärel saate kasutada menüükäsku **Müügi laadimine**, et teisaldada kaubad vaheasukohast kuni laadimisdokki.</span><span class="sxs-lookup"><span data-stu-id="afe47-304">You can then use the **Sales loading** menu item to move the items from the staging location to the loading dock.</span></span>
