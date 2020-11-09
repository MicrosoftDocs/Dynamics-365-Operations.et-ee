---
title: Asukoha tootedimensioonide segamine
description: Selles teemas antakse teavet asukohatoote dimensiooni segamise kohta. See asukohaprofiili funktsioon aitab parandada asukohahaldust, kui kasutatakse tootevariante või tooteid, millel on dimensioonid, näiteks moetööstuses. See võimaldab teil otsustada, kas kindlas asukohaprofiilis saab kombineerida konfiguratsioone, värve, laade ja suurusi või kas ühte asukohta saab lisada vaid ühe neist dimensioonidest või nende kombinatsiooni.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 73519f3fe79d3d7d917d3044255f735640b8ccfd
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017157"
---
# <a name="location-product-dimension-mixing"></a><span data-ttu-id="3fff1-105">Asukoha tootedimensioonide segamine</span><span class="sxs-lookup"><span data-stu-id="3fff1-105">Location product dimension mixing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fff1-106">Asukohatoote dimensioonide segamine on asukohaprofiili funktsioon, mis aitab parandada asukohahaldust, kui kasutatakse tootevariante või tooteid, millel on dimensioonid, näiteks moetööstuses.</span><span class="sxs-lookup"><span data-stu-id="3fff1-106">Location product dimension mixing is location profile functionality that helps improve location management when product variants or products that have dimensions are used, such as in the fashion industry.</span></span> <span data-ttu-id="3fff1-107">See võimaldab teil otsustada, kas kindlas asukohaprofiilis saab kombineerida konfiguratsioone, värve, laade ja suurusi või kas ühte asukohta saab lisada vaid ühe neist dimensioonidest või nende kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="3fff1-107">It lets you decide whether configurations, colors, styles, and sizes can be mixed for a specific location profile, or whether just one of these dimensions or a combination of them can be put to the same location.</span></span>

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a><span data-ttu-id="3fff1-108">Asukohatoote dimensiooni segamise funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="3fff1-108">Turn on the Location product dimension mixing feature</span></span>

<span data-ttu-id="3fff1-109">Enne asukohatoote dimensiooni segamise funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="3fff1-109">Before you can use location product dimension mixing, the feature must be turned on in your system.</span></span> <span data-ttu-id="3fff1-110">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="3fff1-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="3fff1-111">Seega on funktsioon loetletud järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="3fff1-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="3fff1-112">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="3fff1-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="3fff1-113">**Funktsiooni nimi:** *Asukohatoote dimensiooni segamine*</span><span class="sxs-lookup"><span data-stu-id="3fff1-113">**Feature name:** *Location product dimension mixing*</span></span>

## <a name="setup"></a><span data-ttu-id="3fff1-114">Häälestus</span><span class="sxs-lookup"><span data-stu-id="3fff1-114">Setup</span></span>

<span data-ttu-id="3fff1-115">Igal asukohal laos on vaja sellega seotud asukohaprofiili, mis kirjeldab asukoha atribuute.</span><span class="sxs-lookup"><span data-stu-id="3fff1-115">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location.</span></span> <span data-ttu-id="3fff1-116">Seega kõik sama asukohaprofiili kasutavad asukohad saavad lubada tootedimensiooni segamist pärast selle seadistamist.</span><span class="sxs-lookup"><span data-stu-id="3fff1-116">Therefore, all locations that use the same location profile will be able to allow product dimension mixing after it has been set up.</span></span>

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a><span data-ttu-id="3fff1-117">Asukohaprofiilide konfigureerimine tootedimensiooni segamise lubamiseks</span><span class="sxs-lookup"><span data-stu-id="3fff1-117">Configure location profiles to allow product dimension mixing</span></span>

1. <span data-ttu-id="3fff1-118">Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukohaprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-118">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="3fff1-119">Valige asukohaprofiilide loendist suvand **HULGI**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-119">In the list of location profiles, select **BULK**.</span></span>
1. <span data-ttu-id="3fff1-120">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-120">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="3fff1-121">Määrake kiirkaardi **Üldine** suvandi **Luba asukohatoote dimensioonipõhine segamine** väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="3fff1-121">On the **General** FastTab, set the **Enable location product dimension specific mixing** option to *Yes*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3fff1-122">Saate määrata selle suvandi väärtuseks *Jah* ainult juhul, kui suvandi **Luba segakaubad** väärtuseks on seatud *Ei*.</span><span class="sxs-lookup"><span data-stu-id="3fff1-122">You can set this option to *Yes* only if the **Allow mixed items** option is set to *No*.</span></span>

1. <span data-ttu-id="3fff1-123">Määrake kiirkaardi **Lubatud tootedimensioonide segamine** suvandi **Suurus** väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="3fff1-123">On the **Allowed product dimension mixing** FastTab, set the **Size** option to *Yes*.</span></span> <span data-ttu-id="3fff1-124">Selles teemas kirjeldatud stsenaariumis on segamine võimalik ainult nende toodete puhul, millel dimensioon **Suurus** on erinev.</span><span class="sxs-lookup"><span data-stu-id="3fff1-124">In the scenario that is described in this topic, mixing can be done only for products that have different **Size** dimensions.</span></span> <span data-ttu-id="3fff1-125">Kuid muud suvandid on samuti saadaval.</span><span class="sxs-lookup"><span data-stu-id="3fff1-125">However, other options are also available.</span></span>
1. <span data-ttu-id="3fff1-126">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-126">Select **Save**.</span></span>

### <a name="create-a-new-product-master-and-product-variants"></a><span data-ttu-id="3fff1-127">Uue tooteetaloni ja tootevariandi loomine</span><span class="sxs-lookup"><span data-stu-id="3fff1-127">Create a new product master and product variants</span></span>

1. <span data-ttu-id="3fff1-128">Avage **Tooteteabe haldus \> Tooted \> Tooteetalonid**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-128">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="3fff1-129">Tooteetaloni loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-129">On the Action Pane, select **New** to create a product master.</span></span>
1. <span data-ttu-id="3fff1-130">Dialoogiboksis **Uus toode** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3fff1-130">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3fff1-131">**Toote tüüp:** *Kaup*</span><span class="sxs-lookup"><span data-stu-id="3fff1-131">**Product type:** *Item*</span></span>
    - <span data-ttu-id="3fff1-132">**Toote alamtüüp:** *Tooteetalon*</span><span class="sxs-lookup"><span data-stu-id="3fff1-132">**Product subtype:** *Product master*</span></span>
    - <span data-ttu-id="3fff1-133">**Toote number:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="3fff1-133">**Product number:** *B0001*</span></span>
    - <span data-ttu-id="3fff1-134">**Product nimi:** *B0001 Suurus*</span><span class="sxs-lookup"><span data-stu-id="3fff1-134">**Product name:** *B0001 Size*</span></span>
    - <span data-ttu-id="3fff1-135">**Tootedimensioonigrupp:** *Suurus*</span><span class="sxs-lookup"><span data-stu-id="3fff1-135">**Product dimension group:** *Size*</span></span>
    - <span data-ttu-id="3fff1-136">**Konfiguratsiooni tehnoloogia:** *Eelmääratletud variant*</span><span class="sxs-lookup"><span data-stu-id="3fff1-136">**Configuration technology:** *Predefined variant*</span></span>

1. <span data-ttu-id="3fff1-137">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-137">Select **OK**.</span></span>
1. <span data-ttu-id="3fff1-138">Määrake lehe **Toote üksikasjad** kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3fff1-138">On the **Product details** page, on the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3fff1-139">**Loo variandid automaatselt:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="3fff1-139">**Generate variants automatically:** *Yes*</span></span>
    - <span data-ttu-id="3fff1-140">**Suuruse grupp:** *CASUALDHIR*</span><span class="sxs-lookup"><span data-stu-id="3fff1-140">**Size group:** *CASUALDHIR*</span></span>

1. <span data-ttu-id="3fff1-141">Eelmääratletud variantide vaatamiseks valige toimingupaanil **Tootevariandid**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-141">To view the predefined variants, on the Action Pane, select **Product variants**.</span></span>

    <span data-ttu-id="3fff1-142">Kuvatakse leht **Tootevariandid** , mis sisaldab suuruse grupi konfiguratsiooni variantide loendit.</span><span class="sxs-lookup"><span data-stu-id="3fff1-142">The **Product variants** page appears and shows a list of variants from the configuration of the size group.</span></span>

### <a name="release-products-to-the-usmf-company"></a><span data-ttu-id="3fff1-143">Toodete väljastamine ettevõtetele USMF</span><span class="sxs-lookup"><span data-stu-id="3fff1-143">Release products to the USMF company</span></span>

1. <span data-ttu-id="3fff1-144">Valige toimingupaanil suvand **Toodete väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-144">On the Action Pane, select **Release products**.</span></span>
1. <span data-ttu-id="3fff1-145">Kinnitage lehel **Toodete valimine väljastamiseks** , et tootenumber *B0001* oleks loendis ja seejärel valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-145">On the **Select products to release** page, confirm that product number *B0001* is in the list, and then select **Next**.</span></span>
1. <span data-ttu-id="3fff1-146">Valige **Edasi** , et kinnitada väljastatavad tootevariandid.</span><span class="sxs-lookup"><span data-stu-id="3fff1-146">Select **Next** to confirm the product variants to release.</span></span>
1. <span data-ttu-id="3fff1-147">Valige lehel **Ettevõttete valimine, kuhu väljastada** suvand *USMF* ja klõpsake valiku kinnitamiseks **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-147">On the **Select companies to release to** page, select *USMF* , and then select **Next** to confirm the selection.</span></span>
1. <span data-ttu-id="3fff1-148">Valige lehel **Valiku kinnitamine** väljastamise lõpule viimiseks **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-148">On the **Confirm selection** page, select **Finish** to complete the release.</span></span>

    <span data-ttu-id="3fff1-149">Kuvatakse teade „Toiming lõpule viidud”.</span><span class="sxs-lookup"><span data-stu-id="3fff1-149">You receive an "Operation completed" message.</span></span>

### <a name="update-a-released-product-in-the-usmf-company"></a><span data-ttu-id="3fff1-150">Väljastatud toote värskendamine ettevõttes USMF</span><span class="sxs-lookup"><span data-stu-id="3fff1-150">Update a released product in the USMF company</span></span>

1. <span data-ttu-id="3fff1-151">Veenduge, et olete sisse logitud ettevõttesse **USMF**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-151">Make sure that you're signed in to the **USMF** company.</span></span>
1. <span data-ttu-id="3fff1-152">Väljastatud toote loomise lõpetamiseks minge jaotisse **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-152">Go to **Product information management \> Products \> Released products** to finish creating the released product.</span></span>
1. <span data-ttu-id="3fff1-153">Otsige ja valige kaubakood *B0001* , et avada leht **Väljastatud toote üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-153">Find and select item number *B0001* to open the **Released product details** page.</span></span>
1. <span data-ttu-id="3fff1-154">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-154">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="3fff1-155">Veenduge, et kiirkaardi **Üldine** välja **Kauba mudeligrupp** väärtuseks on seatud *FIFO*.</span><span class="sxs-lookup"><span data-stu-id="3fff1-155">On the **General** FastTab, make sure that the **Item model group** field is set to *FIFO*.</span></span>
1. <span data-ttu-id="3fff1-156">Tehke toimingupaani vahekaardil **Toode** grupis **Häälesta** valik **Dimensioonigrupid**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-156">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Dimension groups**.</span></span>
1. <span data-ttu-id="3fff1-157">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3fff1-157">Set the following values:</span></span>

    - <span data-ttu-id="3fff1-158">**Laoala dimensiooni grupp:** *Ladu*</span><span class="sxs-lookup"><span data-stu-id="3fff1-158">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="3fff1-159">**Jälgimisdimensioonigrupp:** *Puudub*</span><span class="sxs-lookup"><span data-stu-id="3fff1-159">**Tracking dimension group:** *None*</span></span>

1. <span data-ttu-id="3fff1-160">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-160">Select **OK**.</span></span>
1. <span data-ttu-id="3fff1-161">Tehke toimingupaani vahekaardil **Toode** grupis **Häälesta** valik **Reserveerimishierarhia**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-161">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Reservation hierarchy**.</span></span>
1. <span data-ttu-id="3fff1-162">Määrake välja **Reserveerimishierarhia** väärtuseks *Vaikimisi* ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-162">Set the **Reservation hierarchy** field to *Default* , and then select **OK**.</span></span>
1. <span data-ttu-id="3fff1-163">Kiirkaardi **Üldine** jaotises **Haldus** näete, et teie valikud on värskendatud.</span><span class="sxs-lookup"><span data-stu-id="3fff1-163">On the **General** FastTab, in the **Administration** section, notice that your selections have been updated.</span></span>
1. <span data-ttu-id="3fff1-164">Sisestage kiirkaardi **Ost** väljale **Hind** väärtus *10*.</span><span class="sxs-lookup"><span data-stu-id="3fff1-164">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="3fff1-165">Sisestage kiirkaardi **Kulude haldamine** väljale **Kaubagrupp** väärtus *Heli*.</span><span class="sxs-lookup"><span data-stu-id="3fff1-165">On the **Manage costs** FastTab, in the **Item group** field, enter *Audio*.</span></span>
1. <span data-ttu-id="3fff1-166">Sisestage kiirkaardi **Ost** väljale **Hind** väärtus *10*.</span><span class="sxs-lookup"><span data-stu-id="3fff1-166">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="3fff1-167">Sisestage kiirkaardi **Ladu** väljale **Ühiku seeriagrupi ID** väärtus *ea*.</span><span class="sxs-lookup"><span data-stu-id="3fff1-167">On the **Warehouse** FastTab, in the **Unit sequence group ID** field, enter *ea*.</span></span>
1. <span data-ttu-id="3fff1-168">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-168">Select **Save**.</span></span>

### <a name="create-a-location-directive"></a><span data-ttu-id="3fff1-169">Asukohakorralduse loomine</span><span class="sxs-lookup"><span data-stu-id="3fff1-169">Create a location directive</span></span>

1. <span data-ttu-id="3fff1-170">Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-170">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="3fff1-171">Valige vasakpoolse paani väljal **Töökäsu tüüp** suvand *Ostutellimused*.</span><span class="sxs-lookup"><span data-stu-id="3fff1-171">In the left pane, in the **Work order type** field, select *Purchase orders*.</span></span>
1. <span data-ttu-id="3fff1-172">Valige loendis asukohakorraldus, mille nimi on *24 otse-PO*.</span><span class="sxs-lookup"><span data-stu-id="3fff1-172">In the list, select the location directive that is named *24 PO Direct*.</span></span>
1. <span data-ttu-id="3fff1-173">Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus** , et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="3fff1-173">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="3fff1-174">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3fff1-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3fff1-175">**Järjekorranumber:** *1*</span><span class="sxs-lookup"><span data-stu-id="3fff1-175">**Sequence number:** *1*</span></span>

        <span data-ttu-id="3fff1-176">Uus rida peaks olema eelnevalt olemasoleva rea ees.</span><span class="sxs-lookup"><span data-stu-id="3fff1-176">The new line should be in front of the previously existing line.</span></span> <span data-ttu-id="3fff1-177">Muudatuse tegemiseks kasutage tööriistariba nuppe **Nihuta üles** ja **Nihuta alla** või muutke olemasoleva rea suvandi **Järjekorranumber** väärtuseks *2*.</span><span class="sxs-lookup"><span data-stu-id="3fff1-177">To make the change, use the **Move up** and **Move down** buttons on the toolbar, or change the existing line's **Sequence number** value to *2*.</span></span>

    - <span data-ttu-id="3fff1-178">**Nimi:** *Pane asukohaprofiili HULGI*</span><span class="sxs-lookup"><span data-stu-id="3fff1-178">**Name:** *Put to BULK Location profile*</span></span>
    - <span data-ttu-id="3fff1-179">**Fikseeritud asukoha kasutus:** *Fikseeritud ja mittefikseeritud asukohad*</span><span class="sxs-lookup"><span data-stu-id="3fff1-179">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>
    - <span data-ttu-id="3fff1-180">**Luba negatiivne laovaru:** *Tühjenda see märkeruut (=Ei)*</span><span class="sxs-lookup"><span data-stu-id="3fff1-180">**Allow negative inventory:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="3fff1-181">**Partii lubatud:** *Tühjenda see märkeruut (=Ei)*</span><span class="sxs-lookup"><span data-stu-id="3fff1-181">**Batch enabled:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="3fff1-182">**Strateegia:** *Puudub*</span><span class="sxs-lookup"><span data-stu-id="3fff1-182">**Strategy:** *None*</span></span>

1. <span data-ttu-id="3fff1-183">Kui uus rida on valitud, valige ruudustiku kohal **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-183">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="3fff1-184">Valige päringu dialoogiboksis vahekaardil **Vahemik** suvand **Lisa** , et lisada rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="3fff1-184">In the query dialog box, on the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="3fff1-185">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3fff1-185">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3fff1-186">**Tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="3fff1-186">**Table:** *Locations*</span></span>
    - <span data-ttu-id="3fff1-187">**Tuletatud tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="3fff1-187">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="3fff1-188">**Väli:** *Asukohaprofiili ID*</span><span class="sxs-lookup"><span data-stu-id="3fff1-188">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="3fff1-189">**Kriteeriumid:** *BULK*</span><span class="sxs-lookup"><span data-stu-id="3fff1-189">**Criteria:** *BULK*</span></span>

1. <span data-ttu-id="3fff1-190">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-190">Select **OK**.</span></span>
1. <span data-ttu-id="3fff1-191">Valige toimingupaani lehel **Asukohakorraldused** suvand **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-191">On the **Location directives** page, on the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="3fff1-192">Kui kasutate kiirkaardi **Asukohakorralduse tegevused** väljal **Strateegia** asukohastrateegiat *Konsolideerimine* alistatakse kiirkaardi **Lubatud tootedimensioonide segamine** häälestus **Asukohaprofiilides** ja kaubad pannakse samasse asukohta isegi juhul, kui häälestus ei luba seda käitumist.</span><span class="sxs-lookup"><span data-stu-id="3fff1-192">On the **Location Directive Actions** FastTab **Strategy** field, if you use the *Consolidate* location strategy, the setup of the **Allowed product dimension mixing** FastTab on the **Location profiles** will be overridden, and items will be put to the same location even if this behavior isn't allowed by the setup.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="3fff1-193">Mobiilse seadme menüü-üksuse loomine</span><span class="sxs-lookup"><span data-stu-id="3fff1-193">Create a mobile device menu item</span></span>

1. <span data-ttu-id="3fff1-194">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-194">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="3fff1-195">Valige toimingupaanil **Uus** , et luua menüü-üksus sortimise jaoks.</span><span class="sxs-lookup"><span data-stu-id="3fff1-195">On the Action Pane, select **New** to create a menu item to use for sorting.</span></span>
1. <span data-ttu-id="3fff1-196">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3fff1-196">In the header, set the following values:</span></span>

    - <span data-ttu-id="3fff1-197">**Menüü-üksuse nimi:** *Vastuvõttev ostutellimuse rida*</span><span class="sxs-lookup"><span data-stu-id="3fff1-197">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="3fff1-198">**Pealkiri:** *Vastuvõttev ostutellimuse rida*</span><span class="sxs-lookup"><span data-stu-id="3fff1-198">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="3fff1-199">**Režiim:** *töö*</span><span class="sxs-lookup"><span data-stu-id="3fff1-199">**Mode:** *Work*</span></span>
    - <span data-ttu-id="3fff1-200">**Kasuta olemasolevat tööd:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="3fff1-200">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="3fff1-201">Määrake kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3fff1-201">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="3fff1-202">**Töö loomise protsess:** *Vastuvõttev ostutellimuse rida ja ladustamine*</span><span class="sxs-lookup"><span data-stu-id="3fff1-202">**Work creation process:** *Purchase order line receiving and putaway*</span></span>
    - <span data-ttu-id="3fff1-203">**Loo litsentsiplaat:** *jah*</span><span class="sxs-lookup"><span data-stu-id="3fff1-203">**Generate license plate:** *Yes*</span></span>

1. <span data-ttu-id="3fff1-204">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-204">Select **Save**.</span></span>

### <a name="configure-the-mobile-device-menu"></a><span data-ttu-id="3fff1-205">Mobiilseadme menüü konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="3fff1-205">Configure the mobile device menu</span></span>

1. <span data-ttu-id="3fff1-206">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="3fff1-207">Valige menüüde loendist suvand **Sissetulev**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-207">In the list of menus, select **Inbound**.</span></span>
1. <span data-ttu-id="3fff1-208">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-208">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="3fff1-209">Otsige üles ja valige loendist **Saadaolevad menüüd ja menüü-üksused** suvand **Vastuvõttev ostutellimuse rida**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-209">In the **Available Menus And Menu Items** list, find and select the **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="3fff1-210">Valige parempoolne noolenupp, et nihutada menüü-üksus **Vastuvõttev ostutellimuse rida** loendisse **Menüüstruktuur**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-210">Select the right arrow button to move the **PO line receiving** menu item to the **Menu Structure** list.</span></span> <span data-ttu-id="3fff1-211">Sedasi saate lisada uue menüü-üksuse valitud menüüsse.</span><span class="sxs-lookup"><span data-stu-id="3fff1-211">In this way, you add your new menu item to the selected menu.</span></span>
1. <span data-ttu-id="3fff1-212">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-212">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="3fff1-213">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="3fff1-213">Scenario</span></span>

<span data-ttu-id="3fff1-214">See demostsenaarium näitab, kuidas kahte erinevat tootevarianti saab lisada samasse asukohta, kui asukohaprofiil ei luba segakaupu, kuid funktsioon *Asukohatoote dimensiooni segamine* on lubatud.</span><span class="sxs-lookup"><span data-stu-id="3fff1-214">This demo scenario shows how two different product variants can be put to the same location when the location profile doesn't allow for mixed items, but the *Location product dimension mixing* feature is enabled.</span></span> <span data-ttu-id="3fff1-215">Sellisel juhul saate kasutada varianti **Suurus** kriteeriumina.</span><span class="sxs-lookup"><span data-stu-id="3fff1-215">In this case, you will use the **Size** variant as the criterion.</span></span>

<span data-ttu-id="3fff1-216">Enne alustamist veenduge, et laos *24* , mis kasutab asukohaprofiili *HULGI* , poleks tühjasid asukohti.</span><span class="sxs-lookup"><span data-stu-id="3fff1-216">Before you begin, make sure that there are empty locations in warehouse *24* that use the *BULK* location profile.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="3fff1-217">Ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="3fff1-217">Create a purchase order</span></span>

<span data-ttu-id="3fff1-218">Loote ostutellimuse, millel on kolm rida: kaks rida sama tootenumbriga, kuid erineva variandiga **Suurus** ja kolmanda rea erinevale tootele, millel pole variante.</span><span class="sxs-lookup"><span data-stu-id="3fff1-218">You will create a purchase order that has three lines: two lines for the same product number but different **Size** variants, and a third line for a different product that has no variants.</span></span>

1. <span data-ttu-id="3fff1-219">Avage jaotis **Ostureskontro \> Ostutellimused \> Kõik ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-219">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="3fff1-220">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-220">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3fff1-221">Dialoogiboksis **Ostutellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3fff1-221">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="3fff1-222">**Hankija konto:** *1001*</span><span class="sxs-lookup"><span data-stu-id="3fff1-222">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="3fff1-223">**Ladu:** *24*</span><span class="sxs-lookup"><span data-stu-id="3fff1-223">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="3fff1-224">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-224">Select **OK**.</span></span>
1. <span data-ttu-id="3fff1-225">Luuakse ostutellimus ja lisatakse uus rida kiirkaardile **OIstutellimuse read**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-225">The purchase order is created, and a new line is added on the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="3fff1-226">Märkige üles ostutellimuse number.</span><span class="sxs-lookup"><span data-stu-id="3fff1-226">Make a note of the purchase order number.</span></span>
1. <span data-ttu-id="3fff1-227">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3fff1-227">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3fff1-228">**Kauba kood:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="3fff1-228">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="3fff1-229">**Suurus** *L*</span><span class="sxs-lookup"><span data-stu-id="3fff1-229">**Size** *L*</span></span>
    - <span data-ttu-id="3fff1-230">**Kogus:** *2*</span><span class="sxs-lookup"><span data-stu-id="3fff1-230">**Quantity:** *2*</span></span>

1. <span data-ttu-id="3fff1-231">Valige ruudustiku kohal **Lisa rida** , et lisada teine ostutellimuse rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3fff1-231">Select **Add line** above the grid to add a second purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="3fff1-232">**Kauba kood:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="3fff1-232">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="3fff1-233">**Suurus** *XL*</span><span class="sxs-lookup"><span data-stu-id="3fff1-233">**Size** *XL*</span></span>
    - <span data-ttu-id="3fff1-234">**Kogus:** *2*</span><span class="sxs-lookup"><span data-stu-id="3fff1-234">**Quantity:** *2*</span></span>

1. <span data-ttu-id="3fff1-235">Valige **Lisa rida** , et lisada kolmas ostutellimuse rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3fff1-235">Select **Add line** to add a third purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="3fff1-236">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="3fff1-236">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="3fff1-237">**Kogus:** *1*</span><span class="sxs-lookup"><span data-stu-id="3fff1-237">**Quantity:** *1*</span></span>

<span data-ttu-id="3fff1-238">1.Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-238">1.Select **Save**.</span></span>

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a><span data-ttu-id="3fff1-239">Ostutellimuse ridade vastuvõtmine laorakenduses</span><span class="sxs-lookup"><span data-stu-id="3fff1-239">Receive purchase order lines in the warehouse app</span></span>

1. <span data-ttu-id="3fff1-240">Logige laorakendusse sisse kasutajana, kes on lubatud lao *24* jaoks.</span><span class="sxs-lookup"><span data-stu-id="3fff1-240">Sign in to the warehouse app as a user who is enabled for warehouse *24*.</span></span>
1. <span data-ttu-id="3fff1-241">Valige menüü **Sissetulev**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-241">Select the **Inbound** menu.</span></span>
1. <span data-ttu-id="3fff1-242">Valige **Vastuvõttev ostutellimuse rida**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-242">Select **PO Line receiving**.</span></span>
1. <span data-ttu-id="3fff1-243">Valige väli **PONUM** ja sisestage ostutellimuse number.</span><span class="sxs-lookup"><span data-stu-id="3fff1-243">Select the **PONUM** field, and then enter the purchase order number.</span></span>
1. <span data-ttu-id="3fff1-244">Kinnitage kirje, valides lehe allosas kinnitamise nupu (✔).</span><span class="sxs-lookup"><span data-stu-id="3fff1-244">Confirm your entry by selecting the confirm button ( ✔ ) at the bottom of the page.</span></span>
1. <span data-ttu-id="3fff1-245">Sisestage sissetuleva ostutellimuse rea number.</span><span class="sxs-lookup"><span data-stu-id="3fff1-245">Enter the line number from the purchase order that is being received.</span></span> <span data-ttu-id="3fff1-246">Valige väli **LINENUM** ja seejärel kasutage numbriklahvistikku väärtuse *1* sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="3fff1-246">Select the **LINENUM** field, and then use the number pad to enter *1*.</span></span>
1. <span data-ttu-id="3fff1-247">Kinnitage kirje.</span><span class="sxs-lookup"><span data-stu-id="3fff1-247">Confirm your entry.</span></span>
1. <span data-ttu-id="3fff1-248">Sisestage sissetulev kogus.</span><span class="sxs-lookup"><span data-stu-id="3fff1-248">Enter the quantity to receive.</span></span> <span data-ttu-id="3fff1-249">Valige plussmärgi nupp ( **+** ) kaks korda, et suurendada välja **Kogus** väärtuseks *2*.</span><span class="sxs-lookup"><span data-stu-id="3fff1-249">Select the plus sign ( **+** ) button two times to increase the value in the **Qty** field to *2*.</span></span>
1. <span data-ttu-id="3fff1-250">Registreerige oma kirje, valides lehe allosas nupu (✔) ja seejärel kinnitage oma kirje, valides nupu (✔) uuesti.</span><span class="sxs-lookup"><span data-stu-id="3fff1-250">Register your entry by selecting the button ( ✔ ) at the bottom of the page, and then confirm your entry by selecting the button ( ✔ ) again.</span></span>
1. <span data-ttu-id="3fff1-251">Vaadake teavet lehel **Ostutellimused: sisestatud**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-251">View the information on the **Purchase orders: Put** page.</span></span> <span data-ttu-id="3fff1-252">Sellel lehel kuvatakse ladustamiseks loodud töö (Töö 1).</span><span class="sxs-lookup"><span data-stu-id="3fff1-252">This page shows the work that has been created for the put-away (Work 1).</span></span>

    <span data-ttu-id="3fff1-253">Kuvatakse asukoht, kuhu vastuvõetud kaup ladustatakse, identifitseerimisnumber, kaup, suurus ja ülesande **Vastuvõttev ostutellimuse rida** kogus, mille äsja lõpule viisite.</span><span class="sxs-lookup"><span data-stu-id="3fff1-253">The location where the received item will be put away, the license plate, the item, the size, and the quantity of the **PO Line receiving** task that you just completed are shown.</span></span>

1. <span data-ttu-id="3fff1-254">Kinnitage ladustamise töö.</span><span class="sxs-lookup"><span data-stu-id="3fff1-254">Confirm the put-away work.</span></span>
1. <span data-ttu-id="3fff1-255">Korrake etappe 4–11 ostutellimuse rea 2 jaoks.</span><span class="sxs-lookup"><span data-stu-id="3fff1-255">Repeat the steps 4 through 11 for the purchase order line 2.</span></span> <span data-ttu-id="3fff1-256">Kuid etapis 8 määrake koguseks *1*.</span><span class="sxs-lookup"><span data-stu-id="3fff1-256">However, in step 8, specify a quantity of *1*.</span></span>

    <span data-ttu-id="3fff1-257">Luuakse uus ladustamise töö (Töö 2) Tööga 1 samasse asukohta.</span><span class="sxs-lookup"><span data-stu-id="3fff1-257">New put-away work (Work 2) is created for the same location as Work 1.</span></span>

1. <span data-ttu-id="3fff1-258">Korrake etappe 4–11 uuesti ostutellimuse rea 2 jaoks.</span><span class="sxs-lookup"><span data-stu-id="3fff1-258">Repeat the steps 4 through 11 again for purchase order line 2.</span></span> <span data-ttu-id="3fff1-259">Etapis 8 määrake järelejäänud koguseks *1*.</span><span class="sxs-lookup"><span data-stu-id="3fff1-259">In step 8, specify the remaining quantity of *1*.</span></span>

    <span data-ttu-id="3fff1-260">Luuakse uus ladustamise töö (Töö 3) Tööga 1 ja 2 samasse asukohta.</span><span class="sxs-lookup"><span data-stu-id="3fff1-260">New put-away work (Work 3) is created for the same location as Work 1 and Work 2.</span></span> <span data-ttu-id="3fff1-261">Selline käitumine ilmneb juhul, kui kasutatakse asukohakorraldust *Konsolideerimine* ja kiirkaart **Lubatud tootedimensiooni segamine** seadistuses *Hulgi* **Asukohaprofiilid** lubab variandi **Suurus** segamist asukohas.</span><span class="sxs-lookup"><span data-stu-id="3fff1-261">This behavior occurs because the *Consolidate* location directive strategy is used, and the **Allowed product dimension mixing** FastTab on the *Bulk* **Location profiles** setup allows the **Size** variant to be mixed on a location.</span></span>

1. <span data-ttu-id="3fff1-262">Korrake etappe 4–11 ostutellimuse rea 3 jaoks.</span><span class="sxs-lookup"><span data-stu-id="3fff1-262">Repeat the steps 4 through 11 for purchase order line 3.</span></span> <span data-ttu-id="3fff1-263">Määrake etapis 8 kogus *1* kaubakoodi *A0001* jaoks.</span><span class="sxs-lookup"><span data-stu-id="3fff1-263">In step 8, specify a quantity of *1* for item number *A0001*.</span></span>

    <span data-ttu-id="3fff1-264">Luuakse uus ladustamise töö (Töö 4) ostutellimuse ridadel 1 ja 2 kasutatud asukohast erinevas asukohas.</span><span class="sxs-lookup"><span data-stu-id="3fff1-264">New put-away work (Work 4) is created for a different location than the location that is used for purchase order lines 1 and 2.</span></span> <span data-ttu-id="3fff1-265">Selline käitumine ilmneb seetõttu, et asukohaprofiil ei luba segatooteid, kuid see lubab segadimensioone samal tooteetalonil.</span><span class="sxs-lookup"><span data-stu-id="3fff1-265">This behavior occurs because the location profile doesn't allow for mixed products, but it does allow for mixed dimensions of the same product master.</span></span>

1. <span data-ttu-id="3fff1-266">Valige lehe ülaosas nupp Menüü (nimetatakse mõnikord hamburgeriks või hamburgeri nupuks) ja seejärel valige **Tühista** , et väljuda suvandist **Vastuvõttev ostutellimuse rida**.</span><span class="sxs-lookup"><span data-stu-id="3fff1-266">Select the Menu button at the top of the page (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit **PO Line receiving**.</span></span>

> [!TIP]
> <span data-ttu-id="3fff1-267">Võite seda stsenaariumi korrata, kuid määrake seekord jaotise *HULGI* **Asukohaprofiilid** kiirkaardil **Luba tootedimensioonide segamine** suvandi väärtuseks **Suurus** - *Ei* , et ühtegi tootedimensiooni ei saaks segada.</span><span class="sxs-lookup"><span data-stu-id="3fff1-267">You can repeat this scenario, but this time, set **Size** - *No* under the **Allow product dimension mixing** FastTab on the *BULK* **Location profiles** , so that none of the product dimensions can be mixed.</span></span> <span data-ttu-id="3fff1-268">Sellisel juhul pannakse ostutellimuse vastuvõtmisel iga tootevariant uude asukohta.</span><span class="sxs-lookup"><span data-stu-id="3fff1-268">In this case, when you receive the purchase order, each product variant will be put to a new location.</span></span>