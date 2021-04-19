---
title: Komplekteerimisridade grupeerimine
description: See teema annab ülevaate komplekteerimisridade grupeerimisest.
author: Mirzaab
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: fe0e63ef742b7bfd09684a94d273a1841d24599c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828269"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="6d894-103">Komplekteerimisridade grupeerimine</span><span class="sxs-lookup"><span data-stu-id="6d894-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d894-104">Komplekteerimisridade grupeerimine võimaldab mitu töörida, millel on sama üksus ja asukoht, kombineerida üheks komplekteerimiseks, mis edastatakse mobiilse seadme kasutajale.</span><span class="sxs-lookup"><span data-stu-id="6d894-104">Pick line grouping enables multiple work lines that have the same item and location to be combined into a single pick that is presented to the user on the mobile device.</span></span> <span data-ttu-id="6d894-105">Seega saavad laotöötajad võtta vastu kõige tõhusamad võimalikud juhiseid, kuid nõutav nõutav süsteemi tööridade eraldamine (nt erinevate konteinerite ja tellimuste jaoks) on võimalik säilitada.</span><span class="sxs-lookup"><span data-stu-id="6d894-105">Therefore, warehouse workers can receive the most efficient instructions, but required work line separation (for different containers, orders, and so on) can still be maintained in the system.</span></span>

## <a name="turn-on-the-pick-line-grouping-feature"></a><span data-ttu-id="6d894-106">Komplekteerimisrea grupeerimise funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="6d894-106">Turn on the pick line grouping feature</span></span>

<span data-ttu-id="6d894-107">Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="6d894-107">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="6d894-108">Administraatorid saavad kasutada [Funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="6d894-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="6d894-109">Seega on funktsioon loetletud järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="6d894-109">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="6d894-110">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="6d894-110">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="6d894-111">**Funktsiooni nimi:** *Komplekteerimisridade grupeerimine*</span><span class="sxs-lookup"><span data-stu-id="6d894-111">**Feature name:** *Pick line grouping*</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="6d894-112">Komplekteerimisridade grupeerimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="6d894-112">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="6d894-113">Mobiilse seadme menüü-üksuse loomine</span><span class="sxs-lookup"><span data-stu-id="6d894-113">Create a mobile device menu item</span></span>

1. <span data-ttu-id="6d894-114">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüükäsud**.</span><span class="sxs-lookup"><span data-stu-id="6d894-114">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="6d894-115">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6d894-115">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6d894-116">Väljale **Menüü-üksuse nimi** sisestage *Müügigrupi rea komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="6d894-116">In the **Menu item name** field, enter *Sales group line picking*.</span></span>
1. <span data-ttu-id="6d894-117">Väljale **Pealkiri** sisestage *Müügigrupi rea komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="6d894-117">In the **Title** field, enter *Sales group line picking*.</span></span> <span data-ttu-id="6d894-118">See pealkiri kuvatakse mobiilse seadme menüüs.</span><span class="sxs-lookup"><span data-stu-id="6d894-118">This title will be shown on the mobile device menu.</span></span>
1. <span data-ttu-id="6d894-119">Valige väljal **Režiim** suvand *Töö*.</span><span class="sxs-lookup"><span data-stu-id="6d894-119">In the **Mode** field, select *Work*.</span></span>
1. <span data-ttu-id="6d894-120">Valige suvandi **Kasuta olemasolevat tööd** sätteks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="6d894-120">Set the **Use existing work** option to *Yes*.</span></span>
1. <span data-ttu-id="6d894-121">Määrake kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="6d894-121">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="6d894-122">Väljale **Juhtija** valige *Kasutaja suunatud*.</span><span class="sxs-lookup"><span data-stu-id="6d894-122">In the **Directed by** field, select *User directed*.</span></span>
    - <span data-ttu-id="6d894-123">Määrake suvand **Loo litsentsiplaat** valikule *Jah*.</span><span class="sxs-lookup"><span data-stu-id="6d894-123">Set the **Generate license plate** option to *Yes*.</span></span>
    - <span data-ttu-id="6d894-124">Määrake suvand **Grupi komplekteerimine** valikule *Jah*.</span><span class="sxs-lookup"><span data-stu-id="6d894-124">Set the **Group pick** option to *Yes*.</span></span>
    - <span data-ttu-id="6d894-125">Võtke vastu ülejäänud väljade vaikesuvandid.</span><span class="sxs-lookup"><span data-stu-id="6d894-125">Accept the default values for the remaining options.</span></span>

1. <span data-ttu-id="6d894-126">Järgige neid etappe, et konfigureerida mobiilse seadme menüü-üksuse kehtivad töö klassid.</span><span class="sxs-lookup"><span data-stu-id="6d894-126">Follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="6d894-127">Valige kiirkaardil **Tööklassid** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6d894-127">On the **Work classes** FastTab, elect **New**.</span></span>
    2. <span data-ttu-id="6d894-128">Väljal **Töö klassi ID** saate valida kas suvandi *Müük* või *SO komplekteerimine*, olenevalt kasutatavast laost.</span><span class="sxs-lookup"><span data-stu-id="6d894-128">In the **Work class ID** field, you can select either *Sales* or *SO Pick*, depending on the warehouse that you will use.</span></span> <span data-ttu-id="6d894-129">Valige selle stsenaariumi jaoks *SO-komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="6d894-129">For this scenario, select *SO Pick*.</span></span>

        <span data-ttu-id="6d894-130">Väli **Töökäsu tüüp** seatakse automaatselt valikule *Müügitellimused*.</span><span class="sxs-lookup"><span data-stu-id="6d894-130">The **Work order type** field is automatically set to *Sales orders*.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="6d894-131">Mobiilse seadme menüü seadistamine</span><span class="sxs-lookup"><span data-stu-id="6d894-131">Set up a mobile device menu</span></span>

<span data-ttu-id="6d894-132">Järgige neid samme äsja loodud menüükäsu lisamiseks menüüsse **Väljastus**.</span><span class="sxs-lookup"><span data-stu-id="6d894-132">Follow these steps to add the menu item that you just created to the **Outbound** menu.</span></span>

1. <span data-ttu-id="6d894-133">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.</span><span class="sxs-lookup"><span data-stu-id="6d894-133">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="6d894-134">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="6d894-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="6d894-135">Loendi paan kuvab kõik olemasolevad mobiilse seadme menüüd.</span><span class="sxs-lookup"><span data-stu-id="6d894-135">The list pane shows all existing mobile device menus.</span></span> <span data-ttu-id="6d894-136">Valige loendist *Väljastus*.</span><span class="sxs-lookup"><span data-stu-id="6d894-136">Select *Outbound* in the list.</span></span>
1. <span data-ttu-id="6d894-137">Otsige üles loendist üles suvand **Saadaolevad menüüd ja menüü-üksused**, leidke ja valige loodud menüü-üksus *Müügigrupi rea komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="6d894-137">In the **Available menus and menu items** list, find and select the *Sales group line picking* menu item that you created.</span></span>
1. <span data-ttu-id="6d894-138">Valige parempoolne noolenupp, et nihutada menüü-üksus *Müügigrupi rea komplekteerimine* loendisse **Menüüstruktuur**.</span><span class="sxs-lookup"><span data-stu-id="6d894-138">Select the right arrow button to move the *Sales group line picking* menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="6d894-139">Kasutage üles ja alla noolenuppe, et teisaldada menüü-üksus soovitud asukohta menüüstruktuuris.</span><span class="sxs-lookup"><span data-stu-id="6d894-139">Use the up arrow and down arrow buttons to move the menu item into the desired position in the menu structure.</span></span>
1. <span data-ttu-id="6d894-140">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="6d894-140">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="6d894-141">Töömalli häälestamine</span><span class="sxs-lookup"><span data-stu-id="6d894-141">Set up a work template</span></span>

1. <span data-ttu-id="6d894-142">Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.</span><span class="sxs-lookup"><span data-stu-id="6d894-142">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="6d894-143">Valige väljal **Töökäsu tüüp** suvand *Müügitellimused*.</span><span class="sxs-lookup"><span data-stu-id="6d894-143">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="6d894-144">Ruudustikus **Ülevaade** leidke ja valige töömall, mida tuleks selle funktsiooniga kasutada.</span><span class="sxs-lookup"><span data-stu-id="6d894-144">In the **Overview** grid, find and select the work template that should be used with this function.</span></span> <span data-ttu-id="6d894-145">Valige selle stsenaariumi jaoks mall *51 Ettevalmistamiseks komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="6d894-145">For this scenario, select the *51 Pick to stage* template.</span></span>
1. <span data-ttu-id="6d894-146">Valige Toimingupaanil nupp **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="6d894-146">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="6d894-147">Valige päringuredaktori dialoogiboksis vahekaardil **Sortimine** suvand **Lisa** ja määrake siis järgmised uue rea väärtused.</span><span class="sxs-lookup"><span data-stu-id="6d894-147">In the query editor dialog box, on the **Sorting** tab, select **Add**, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="6d894-148">Valige veerus **Tabel** suvand *Ajutised töökanded*.</span><span class="sxs-lookup"><span data-stu-id="6d894-148">In the **Table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="6d894-149">Valige veerus **Tuletatud tabel** suvand *Ajutised töökanded*.</span><span class="sxs-lookup"><span data-stu-id="6d894-149">In the **Derived table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="6d894-150">Valige veerus **Väli** suvand *Kaubakood*.</span><span class="sxs-lookup"><span data-stu-id="6d894-150">In the **Field** column, select *Item number*.</span></span>
    - <span data-ttu-id="6d894-151">Valige veerus **Otsingu suund** suvand *Kasvav*.</span><span class="sxs-lookup"><span data-stu-id="6d894-151">In the **Search direction** column, select *Ascending*.</span></span>

1. <span data-ttu-id="6d894-152">Valige **OK**, et sulgeda dialoogiboks ja salvestada oma sätted.</span><span class="sxs-lookup"><span data-stu-id="6d894-152">Select **OK** to close the dialog box and save your selection.</span></span>
1. <span data-ttu-id="6d894-153">Teile kuvatakse järgmine teade: „Grupeerimine lähtestatakse, kas soovite jätkata?”</span><span class="sxs-lookup"><span data-stu-id="6d894-153">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="6d894-154">Jätkamiseks valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="6d894-154">Select **Yes** to continue.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d894-155">Komplekteerimisrea grupeerimise funktsiooni töötamiseks peavad töö read olema sorditud kauba ID järgi.</span><span class="sxs-lookup"><span data-stu-id="6d894-155">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="6d894-156">Kui samu üksuseid sisaldavad read ei ole üksteise järel järjestatud, siis neid ei grupeerita.</span><span class="sxs-lookup"><span data-stu-id="6d894-156">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="6d894-157">Näide</span><span class="sxs-lookup"><span data-stu-id="6d894-157">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="6d894-158">Komplekteerimistöö loomine</span><span class="sxs-lookup"><span data-stu-id="6d894-158">Create picking work</span></span>

<span data-ttu-id="6d894-159">Enne kogumi komplekteerimise seadistamist peate looma mõne sobiliku väljamineva töö.</span><span class="sxs-lookup"><span data-stu-id="6d894-159">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="6d894-160">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="6d894-160">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="6d894-161">Müügitellimuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6d894-161">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="6d894-162">Valige *US-004* väljalt **Kliendi konto**.</span><span class="sxs-lookup"><span data-stu-id="6d894-162">In the **Customer account** field, select *US-004*.</span></span>
1. <span data-ttu-id="6d894-163">Kiirkaardi **Üldine** väljal **Ladu** valige *51*.</span><span class="sxs-lookup"><span data-stu-id="6d894-163">On the **General** FastTab, in the **Warehouse** field, select *51*.</span></span>
1. <span data-ttu-id="6d894-164">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="6d894-164">Select **OK**.</span></span>
1. <span data-ttu-id="6d894-165">Lisage kiirkaardil **Müügitellimuse read** järgmised kuus rida:</span><span class="sxs-lookup"><span data-stu-id="6d894-165">On the **Sales order lines** FastTab, add the following six lines:</span></span>

    - <span data-ttu-id="6d894-166">**1. rida:** valige väljal **Kaubakood** väärtus *M9200*.</span><span class="sxs-lookup"><span data-stu-id="6d894-166">**Line 1:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="6d894-167">Sisestage väljale **Kogus** väärtus *3*.</span><span class="sxs-lookup"><span data-stu-id="6d894-167">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="6d894-168">**2. rida:** valige väljal **Kaubakood** väärtus *M9201*.</span><span class="sxs-lookup"><span data-stu-id="6d894-168">**Line 2:** In the **Item number** field, select *M9201*.</span></span> <span data-ttu-id="6d894-169">Sisestage väljale **Kogus** väärtus *3*.</span><span class="sxs-lookup"><span data-stu-id="6d894-169">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="6d894-170">**3. rida:** valige väljal **Kaubakood** väärtus *M9202*.</span><span class="sxs-lookup"><span data-stu-id="6d894-170">**Line 3:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="6d894-171">Sisestage väljale **Kogus** väärtus *2*.</span><span class="sxs-lookup"><span data-stu-id="6d894-171">In the **Quantity** field, enter *2*.</span></span>
    - <span data-ttu-id="6d894-172">**4. rida:** valige väljal **Kaubakood** väärtus *M9200*.</span><span class="sxs-lookup"><span data-stu-id="6d894-172">**Line 4:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="6d894-173">Sisestage väljale **Kogus** väärtus *1*.</span><span class="sxs-lookup"><span data-stu-id="6d894-173">In the **Quantity** field, enter *1*.</span></span>
    - <span data-ttu-id="6d894-174">**5. rida:** valige väljal **Kaubakood** väärtus *M9200*.</span><span class="sxs-lookup"><span data-stu-id="6d894-174">**Line 5:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="6d894-175">Sisestage väljale **Kogus** väärtus *3*.</span><span class="sxs-lookup"><span data-stu-id="6d894-175">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="6d894-176">**6. rida:** valige väljal **Kaubakood** väärtus *M9202*.</span><span class="sxs-lookup"><span data-stu-id="6d894-176">**Line 6:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="6d894-177">Sisestage väljale **Kogus** väärtus *7*.</span><span class="sxs-lookup"><span data-stu-id="6d894-177">In the **Quantity** field, enter *7*.</span></span>

    <span data-ttu-id="6d894-178">Siin on iga üksuse üldkoguste kokkuvõte.</span><span class="sxs-lookup"><span data-stu-id="6d894-178">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="6d894-179">**Üksus M9200:** igat *7*</span><span class="sxs-lookup"><span data-stu-id="6d894-179">**Item M9200:** *7* each</span></span>
    - <span data-ttu-id="6d894-180">**Üksus M9201:** igat *3*</span><span class="sxs-lookup"><span data-stu-id="6d894-180">**Item M9201:** *3* each</span></span>
    - <span data-ttu-id="6d894-181">**Üksus M9202:** igat *9*</span><span class="sxs-lookup"><span data-stu-id="6d894-181">**Item M9202:** *9* each</span></span>

1. <span data-ttu-id="6d894-182">Enne tellimuste lattu vabastamist peate veenduma, et komplekteerimise asukohtadel on kõikide tellimuste kõigi üksuste jaoks piisavalt varusid.</span><span class="sxs-lookup"><span data-stu-id="6d894-182">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="6d894-183">Vaadake üle seadistus **Asukoha korraldus**, et määratleda, milliseid komplekteerimise asukohti müügitellimuse komplekteerimiseks kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="6d894-183">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span> <span data-ttu-id="6d894-184">Kui kasutate Contoso demo andmekeskkonda laole *51*, veenduge, et varud oleks olemas.</span><span class="sxs-lookup"><span data-stu-id="6d894-184">If you're using the Contoso demo data environment for warehouse *51*, confirm that there is available inventory.</span></span>

    <span data-ttu-id="6d894-185">Peate nüüd reserveerima iga rea laovaru.</span><span class="sxs-lookup"><span data-stu-id="6d894-185">You must now reserve the inventory for each line.</span></span>

1. <span data-ttu-id="6d894-186">Kiirkaardil **Müügitellimuse read** valige üks ridadest, mis tuleb reserveerida.</span><span class="sxs-lookup"><span data-stu-id="6d894-186">On the **Sales order lines** FastTab, select one of the lines that must be reserved.</span></span>
1. <span data-ttu-id="6d894-187">Valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="6d894-187">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="6d894-188">Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et rakendada reserveering.</span><span class="sxs-lookup"><span data-stu-id="6d894-188">On the **Reservation** page, on the Action Pane, select **Reserve lot** to apply the reservation.</span></span> <span data-ttu-id="6d894-189">Seejärel sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6d894-189">Then close the page.</span></span>
1. <span data-ttu-id="6d894-190">Korrake samme 8 kuni 10 ülejäänud ridade puhul, mis tuleb reserveerida.</span><span class="sxs-lookup"><span data-stu-id="6d894-190">Repeat steps 8 through 10 for the remaining lines that must be reserved.</span></span>

    <span data-ttu-id="6d894-191">Peate nüüd vabastama müügitellimuse lattu.</span><span class="sxs-lookup"><span data-stu-id="6d894-191">You must now release the sales order to the warehouse.</span></span>

1. <span data-ttu-id="6d894-192">Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="6d894-192">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="6d894-193">Saate teate, mis ütleb, et saadetis ja voog on loodud ning et voog on esitatud partiina käitamiseks.</span><span class="sxs-lookup"><span data-stu-id="6d894-193">You receive a message that states that a shipment and a wave have been created, and that the wave has been submitted to run in a batch.</span></span>

    <span data-ttu-id="6d894-194">Kui voog ja kõik allavoolu tööd on lõpetatud, luuakse kuue reaga töö jaoks töö ID.</span><span class="sxs-lookup"><span data-stu-id="6d894-194">When the wave and all downstream jobs have been completed, a work ID is created for work that has six lines.</span></span> <span data-ttu-id="6d894-195">Read sorditakse kaubakoodi alusel.</span><span class="sxs-lookup"><span data-stu-id="6d894-195">The lines are sorted by item number.</span></span>

1. <span data-ttu-id="6d894-196">Avage **Laohaldus \> Töö \> Kõik töö**, et vaadata loodud tööd.</span><span class="sxs-lookup"><span data-stu-id="6d894-196">Go to **Warehouse management \> Work \> All work** to view the work that was created.</span></span> <span data-ttu-id="6d894-197">Märkige üles **Töö ID** väärtus, kuna vajate seda järgmises protseduuris.</span><span class="sxs-lookup"><span data-stu-id="6d894-197">Make a note of the **Work ID** value, because you will need it in the next procedure.</span></span>

### <a name="initiate-picking-from-the-mobile-device"></a><span data-ttu-id="6d894-198">Komplekteerimise käivitamine mobiilsest seadmest</span><span class="sxs-lookup"><span data-stu-id="6d894-198">Initiate picking from the mobile device</span></span>

1. <span data-ttu-id="6d894-199">Logige mobiilsesse seadmesse sisse kasutajana, kes on seadistatud lao *51* jaoks.</span><span class="sxs-lookup"><span data-stu-id="6d894-199">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="6d894-200">Valige mobiilses seadmes menüü, mis sisaldab uut mobiilse seadme menüü-üksust.</span><span class="sxs-lookup"><span data-stu-id="6d894-200">On the mobile device, select the menu that includes the new mobile device menu item.</span></span> <span data-ttu-id="6d894-201">Valige selle stsenaariumi jaoks **Väljastav**.</span><span class="sxs-lookup"><span data-stu-id="6d894-201">For this scenario, select **Outbound**.</span></span>
1. <span data-ttu-id="6d894-202">Valige menüü-üksus **Müügigrupi rea komplekteerimine** ja käivitage komplekteerimine.</span><span class="sxs-lookup"><span data-stu-id="6d894-202">Select the **Sales group line picking** menu item to initiate the pick.</span></span>
1. <span data-ttu-id="6d894-203">Sisestage **Töö ID** väärtus, mille eelmises protseduuris kindlaks tegite.</span><span class="sxs-lookup"><span data-stu-id="6d894-203">Enter the **Work ID** value that you made a note of in the previous procedure.</span></span>

    <span data-ttu-id="6d894-204">Peaksite nägema komplekteerimise etappe, kus kauba *M9200* kõik komplekteeritud read on grupeeritud ja teil tuleks saada juhis *7* iga kauba *M9200* komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="6d894-204">You should see a pick step where all pick lines for item *M9200* are grouped, and you should receive an instruction to pick *7* each of item *M9200*.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="6d894-205">Mobiilses seadmes on kolme komplekteerimise töörea komplekteerimistöö koondatud kasutaja üheks komplekteerimissammuks.</span><span class="sxs-lookup"><span data-stu-id="6d894-205">On the mobile device, the pick work for the three pick work lines has been aggregated into one picking step for the user.</span></span>

1. <span data-ttu-id="6d894-206">Kinnitage komplekteerimise etapp.</span><span class="sxs-lookup"><span data-stu-id="6d894-206">Confirm the pick step.</span></span>
1. <span data-ttu-id="6d894-207">Avage töö ID töö leht ja pange tähele, et kõik kolm üksuse *M9200* komplekteerimisrida suleti samaaegselt.</span><span class="sxs-lookup"><span data-stu-id="6d894-207">Go to the work page for the work ID, and notice that all three pick lines for item *M9200* were closed simultaneously.</span></span>
1. <span data-ttu-id="6d894-208">Minge tagasi mobiilsesse seadmesse ja jätkake komplekteerimisega.</span><span class="sxs-lookup"><span data-stu-id="6d894-208">Go back to the mobile device, and continue to pick.</span></span> <span data-ttu-id="6d894-209">Esitada tuleks kauba *M9201* töörida 4.</span><span class="sxs-lookup"><span data-stu-id="6d894-209">Work line 4 for item *M9201* should be presented.</span></span> <span data-ttu-id="6d894-210">Kuna tellimusel oli ainult üks töörida, ei ole midagi liita.</span><span class="sxs-lookup"><span data-stu-id="6d894-210">Because there was only one work line on the order, there is nothing to aggregate.</span></span>
1. <span data-ttu-id="6d894-211">Kinnitage komplekteerimise etapp.</span><span class="sxs-lookup"><span data-stu-id="6d894-211">Confirm the pick step.</span></span>
1. <span data-ttu-id="6d894-212">Viimane komplekteerimise etapp mobiilsel seadmel koondab töökäsu viimased kaks komplekteerimisrida.</span><span class="sxs-lookup"><span data-stu-id="6d894-212">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>
1. <span data-ttu-id="6d894-213">Viige lõpule kõik *üheksa* eseme *M9202* komplekteerimise sammu.</span><span class="sxs-lookup"><span data-stu-id="6d894-213">Complete the pick step for *9* each of item *M9202*.</span></span>
1. <span data-ttu-id="6d894-214">Kinnitage võtmise etapp ja mis tahes täiendavad komplekteerimise/võtmise paarid töö lõpetamiseks.</span><span class="sxs-lookup"><span data-stu-id="6d894-214">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!IMPORTANT]
>
> - <span data-ttu-id="6d894-215">Tööridu saab grupeerida ainult siis, kui need on järjekorras.</span><span class="sxs-lookup"><span data-stu-id="6d894-215">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="6d894-216">Järgmisi funktsioone ei toetata.</span><span class="sxs-lookup"><span data-stu-id="6d894-216">The following functionality isn't supported:</span></span>
>
>   - <span data-ttu-id="6d894-217">Tegeliku kaaluga kaubad</span><span class="sxs-lookup"><span data-stu-id="6d894-217">Catch-weight items</span></span>
>
>    <span data-ttu-id="6d894-218">Kui töös sisalduvad tegeliku kaaluga kaubad, kuvatakse teile enne komplekteerimise alustamist tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="6d894-218">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>
>   - <span data-ttu-id="6d894-219">Osade komplekteerimine</span><span class="sxs-lookup"><span data-stu-id="6d894-219">Piece picking</span></span>
>   - <span data-ttu-id="6d894-220">Töö read, millel on lõpetamata täiendamise töö</span><span class="sxs-lookup"><span data-stu-id="6d894-220">Work lines that have unfinished replenishment work</span></span>
>   - <span data-ttu-id="6d894-221">Ülekomplekteerimine</span><span class="sxs-lookup"><span data-stu-id="6d894-221">Over-picking</span></span>
>   - <span data-ttu-id="6d894-222">Kiirelt komplekteeritava kauba ümberjaotamine</span><span class="sxs-lookup"><span data-stu-id="6d894-222">Short picking with item reallocation</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]