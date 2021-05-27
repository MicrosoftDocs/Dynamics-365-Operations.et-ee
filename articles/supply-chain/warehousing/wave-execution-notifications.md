---
title: Voo täitmise teatised
description: Selles teemas kirjeldatakse voo käitamise teatisi ja selgitatakse, kuidas neid seadistada.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2022-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: fee112d3211f619b2146dd21c4f8a52ad33667d6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019150"
---
# <a name="wave-execution-notifications"></a><span data-ttu-id="41039-103">Voo täitmise teatised</span><span class="sxs-lookup"><span data-stu-id="41039-103">Wave execution notifications</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="41039-104">*Voo käivitamisteatised* funktsioon kasutab ärisündmusi ja tegevuskeskust voo käivitamisega seotud teatiste esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="41039-104">The *Wave execution notifications* feature uses business events and the Action center to deliver notifications that are related to wave execution.</span></span> <span data-ttu-id="41039-105">See võimaldab teil määratleda teatisi loovad sündmuste tüübid, neid loovad laod ja neid saavad kasutajad.</span><span class="sxs-lookup"><span data-stu-id="41039-105">It lets you specify the types of events that generate notifications, the warehouses that generate them, and the users who receive them.</span></span>

<span data-ttu-id="41039-106">**Teadete näitamise** nupp (kellukesümbol) navigeerimisriba paremal pool näitab, millal tegevuskeskuse sõnum on praegusele kasutajale saadaval.</span><span class="sxs-lookup"><span data-stu-id="41039-106">The **Show messages** button (bell symbol) on the right side of the navigation bar indicates when an Action center message is available for the current user.</span></span> <span data-ttu-id="41039-107">Kasutaja saab tegevuskeskuse avamiseks ja sõnumite ülevaatamiseks valida nupu **Näita teateid**.</span><span class="sxs-lookup"><span data-stu-id="41039-107">The user can select the **Show messages** button to open the Action center and review the messages.</span></span>

<span data-ttu-id="41039-108">Ärisündmused toimuvad äriprotsesside käivitamisel.</span><span class="sxs-lookup"><span data-stu-id="41039-108">Business events occur when business processes are run.</span></span> <span data-ttu-id="41039-109">Äriprotsessid valmistatud ülesannetest.</span><span class="sxs-lookup"><span data-stu-id="41039-109">Business processes are made up of tasks.</span></span> <span data-ttu-id="41039-110">Äriprotsessi ajal sooritavad seda osalevad kasutajad nende ülesannete täitmiseks äritoiminguid.</span><span class="sxs-lookup"><span data-stu-id="41039-110">During a business process, the users who participate in it perform business actions to complete those tasks.</span></span> <span data-ttu-id="41039-111">Ärisündmused on mehhanism, mis võimaldab välissüsteemidel saada Finance and Operations rakendustelt teatisi.</span><span class="sxs-lookup"><span data-stu-id="41039-111">Business events provide a mechanism that lets external systems receive notifications from Finance and Operations applications.</span></span> <span data-ttu-id="41039-112">Sel viisil saavad süsteemid sooritada äritoiminguid ja reageerida ärisündmustele.</span><span class="sxs-lookup"><span data-stu-id="41039-112">In this way, the systems can perform business actions in response to the business events.</span></span> <span data-ttu-id="41039-113">Lisateavet leiate teemast [Ärisündmuste ülevaade](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span><span class="sxs-lookup"><span data-stu-id="41039-113">For more information, see [Business events overview](../../fin-ops-core/dev-itpro/business-events/home-page.md).</span></span>

## <a name="turn-on-the-wave-execution-notifications-feature"></a><span data-ttu-id="41039-114">Voo käitamise teatiste funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="41039-114">Turn on the Wave execution notifications feature</span></span>

<span data-ttu-id="41039-115">Enne funktsiooni *Voo käitamise teatised* kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="41039-115">Before you can use the *Wave execution notifications* feature, it must be turned on in your system.</span></span> <span data-ttu-id="41039-116">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="41039-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="41039-117">Seega on funktsioon loetletud järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="41039-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="41039-118">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="41039-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="41039-119">**Funktsiooni nimi:** *voo käitamise teatised*</span><span class="sxs-lookup"><span data-stu-id="41039-119">**Feature name:** *Wave execution notifications*</span></span>

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a><span data-ttu-id="41039-120">Stsenaarium: voo partii käivitamise teatiste saatmine tegevuskeskusele</span><span class="sxs-lookup"><span data-stu-id="41039-120">Scenario: Send wave batch execution notifications to the Action center</span></span>

<span data-ttu-id="41039-121">See stsenaarium näitab kogu voogu teatiste saatmiseks voo partii käivitamise tõrgete kohta konkreetsele rollile tegevuskeskuse kaudu.</span><span class="sxs-lookup"><span data-stu-id="41039-121">This scenario shows the end-to-end flow for sending notifications about wave batch execution errors to a specific role via the Action center.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="41039-122">Demoandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="41039-122">Make demo data available</span></span>

<span data-ttu-id="41039-123">Selle stsenaariumiga töötamiseks peavad teil olema installitud demoandmed ja peate valima juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="41039-123">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a><span data-ttu-id="41039-124">Veenduge, et voog oleksid käitatud partiirežiimis</span><span class="sxs-lookup"><span data-stu-id="41039-124">Make sure that waves are run in batch mode</span></span>

1. <span data-ttu-id="41039-125">Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="41039-125">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="41039-126">Seadke kiirkaardil **Voo töötlemine** suvandi **Voogude töötlemine partiina** väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="41039-126">On the **Wave processing** FastTab, set the **Process waves in batch** option to *Yes*.</span></span>

> [!NOTE]
> <span data-ttu-id="41039-127">Kui soovite keelata voo partii käivitamise teatised, määrake suvandi **Keela voo töötlemise partii teatised** väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="41039-127">If you want to disable wave batch execution notifications, set the **Disable wave processing batch notifications** option to *Yes*.</span></span>

### <a name="configure-a-wave-notification-policy"></a><span data-ttu-id="41039-128">Voo teavituspoliitika konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="41039-128">Configure a wave notification policy</span></span>

<span data-ttu-id="41039-129">Voo teavituspoliitikad määratlevad saadetavate teatiste tüübid ja teavitatud kasutajad.</span><span class="sxs-lookup"><span data-stu-id="41039-129">Wave notification policies define the types of notifications that are sent and the users who are notified.</span></span>

1. <span data-ttu-id="41039-130">Avage jaotis **Laohaldus \> Seadistus \> Vood \> Voo teavituse poliitikad**.</span><span class="sxs-lookup"><span data-stu-id="41039-130">Go to **Warehouse management \> Setup \> Waves \> Wave notification policies**.</span></span>
1. <span data-ttu-id="41039-131">Looge järgmiste sätetega kirje.</span><span class="sxs-lookup"><span data-stu-id="41039-131">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="41039-132">**Voo teavituspoliitika:** *24BatchError*</span><span class="sxs-lookup"><span data-stu-id="41039-132">**Wave notification policy:** *24BatchError*</span></span>
    - <span data-ttu-id="41039-133">**Kirjeldus:** *lao 24 voo partii tõrge*</span><span class="sxs-lookup"><span data-stu-id="41039-133">**Description:** *Warehouse 24 wave batch error*</span></span>
    - <span data-ttu-id="41039-134">**Saada teatis:** *ainult tõrge*</span><span class="sxs-lookup"><span data-stu-id="41039-134">**Send notification on:** *Error only*</span></span>
    - <span data-ttu-id="41039-135">**Rollile:** *Süsteemiadministraator*</span><span class="sxs-lookup"><span data-stu-id="41039-135">**To role:** *System administrator*</span></span>

        > [!NOTE]
        > <span data-ttu-id="41039-136">Kuna see stsenaarium kasutab demoandmeid, valitakse lihtsaks kasutamiseks *süsteemiadministraatori* roll.</span><span class="sxs-lookup"><span data-stu-id="41039-136">Because this scenario uses demo data, the *System administrator* role is selected for the sake of simplicity.</span></span> <span data-ttu-id="41039-137">Kuna olete sisse loginud süsteemiadministraatori kasutajana, saate ka teatisi.</span><span class="sxs-lookup"><span data-stu-id="41039-137">Therefore, because you're signed in as a system administrator user, you will receive the notifications.</span></span> <span data-ttu-id="41039-138">Kuid tavaliselt peaksite siiski valima konkreetsema rolli voo partii käivitamise tõrgetest teatamiseks, nt *Laohaldur*.</span><span class="sxs-lookup"><span data-stu-id="41039-138">However, in practice, you should usually select a more specific role to notify about wave batch execution errors, such as *Warehouse manager*.</span></span>

1. <span data-ttu-id="41039-139">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="41039-139">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="41039-140">Voomalli konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="41039-140">Configure a wave template</span></span>

<span data-ttu-id="41039-141">Voomallid võimaldavad teil linkida kindlaid voo meetodite eksemplare vastava voo sildi mallidega.</span><span class="sxs-lookup"><span data-stu-id="41039-141">Wave templates let you link specific instances of wave methods to corresponding wave label templates.</span></span>

1. <span data-ttu-id="41039-142">Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.</span><span class="sxs-lookup"><span data-stu-id="41039-142">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="41039-143">Määrake loendipaanil välja **Voo malli tüüp** väärtuseks *Saatmine* ja seejärel valige laole 24 *24 saadetise vaikimisi* voomall.</span><span class="sxs-lookup"><span data-stu-id="41039-143">In the list pane, set the **Wave template type** field to *Shipping*, and then select the *24 Shipping Default* wave template for warehouse 24.</span></span>
1. <span data-ttu-id="41039-144">Määrake kiirkaardi **Üldine** välja **Voo teatise poliitika** väärtuseks *24BatchError*.</span><span class="sxs-lookup"><span data-stu-id="41039-144">On the **General** FastTab, set the **Wave notification policy** field to *24BatchError*.</span></span>

### <a name="configure-a-work-template"></a><span data-ttu-id="41039-145">Töömalli konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="41039-145">Configure a work template</span></span>

<span data-ttu-id="41039-146">Töömalle kasutatakse voo käivitamise ajal töö loomiseks.</span><span class="sxs-lookup"><span data-stu-id="41039-146">Work templates are used during wave execution to generate work.</span></span> <span data-ttu-id="41039-147">Selle stsenaariumi korral peaks voo käivitamine käivitama tõrke.</span><span class="sxs-lookup"><span data-stu-id="41039-147">For this scenario, wave execution should trigger an error.</span></span> <span data-ttu-id="41039-148">Seadistades töömalli päringu kasutama olematut laohoonet, tagate, et voo käivitamine nurjub ja saadab teatise.</span><span class="sxs-lookup"><span data-stu-id="41039-148">By setting the work template query to use a nonexistent warehouse, you will ensure that wave execution fails and therefore sends a notification.</span></span>

1. <span data-ttu-id="41039-149">Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.</span><span class="sxs-lookup"><span data-stu-id="41039-149">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="41039-150">Määrake loendipaanil välja **Töömalli tüüp** väärtuseks *Müügitellimused* ja seejärel valige laole 24 *24 SO olek* töömall.</span><span class="sxs-lookup"><span data-stu-id="41039-150">In the list pane, set the **Work template type** field to *Sales orders* and then select the *24 SO Stage* work template for warehouse 24.</span></span>
1. <span data-ttu-id="41039-151">Valige Toimingupaanil nupp **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="41039-151">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="41039-152">Redigeerige päringuredaktori dialoogiboksis vahekaardil **Vahemik** järgmist rida (või lisage see, kui seda pole olemas):</span><span class="sxs-lookup"><span data-stu-id="41039-152">In the query editor dialog box, on the **Range** tab, edit the following row (or add it if it doesn't exist):</span></span>

    - <span data-ttu-id="41039-153">**Tabel:** *Ajutised töökanded*</span><span class="sxs-lookup"><span data-stu-id="41039-153">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="41039-154">**Tuletatud tabel:** *Ajutised töökanded*</span><span class="sxs-lookup"><span data-stu-id="41039-154">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="41039-155">**Väli:** *Ladu*</span><span class="sxs-lookup"><span data-stu-id="41039-155">**Field:** *Warehouse*</span></span>
    - <span data-ttu-id="41039-156">**Kriteerium:** muutke väärtus *24* väärtuseks *Tõrge*.</span><span class="sxs-lookup"><span data-stu-id="41039-156">**Criteria:** Change the value from *24* to *Error*.</span></span>

1. <span data-ttu-id="41039-157">Muutuse kinnitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="41039-157">Select **OK**, and confirm the change.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="41039-158">Müügitellimuse loomine ja selle väljastamine lattu</span><span class="sxs-lookup"><span data-stu-id="41039-158">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="41039-159">Avage jaotis **Müük ja turundus \> Müügitellimus \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="41039-159">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="41039-160">Looge järgmiste sätetega müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="41039-160">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="41039-161">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="41039-161">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="41039-162">**Ladu:** *24*</span><span class="sxs-lookup"><span data-stu-id="41039-162">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="41039-163">Lisage kiirkaardil **Müügitellimuse read** järgmiste sätetega müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="41039-163">On the **Sales order lines** FastTab, add a sales order line that has the following settings:</span></span>

    - <span data-ttu-id="41039-164">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="41039-164">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="41039-165">**Kogus:** *10*</span><span class="sxs-lookup"><span data-stu-id="41039-165">**Quantity:** *10*</span></span>

    > [!NOTE]
    > <span data-ttu-id="41039-166">Need kaubad ja kogused on ainult näited.</span><span class="sxs-lookup"><span data-stu-id="41039-166">These items and quantities are only examples.</span></span> <span data-ttu-id="41039-167">Määratud ladu peab sisaldama piisavalt varu.</span><span class="sxs-lookup"><span data-stu-id="41039-167">The specified warehouse must contain enough stock.</span></span>

1. <span data-ttu-id="41039-168">Kui uus rida on veel valitud kiirkaardil **Müügitellimus**, valige tööriistaribal **Varu \> Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="41039-168">While the new line is still selected on the **Sales order lines** FastTab, select **Inventory \> Reservation** on the toolbar.</span></span>
1. <span data-ttu-id="41039-169">Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**.</span><span class="sxs-lookup"><span data-stu-id="41039-169">On the **Reservation** page, on the Action Pane, select **Reserve lot**.</span></span> <span data-ttu-id="41039-170">Seejärel sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="41039-170">Then close the page.</span></span>
1. <span data-ttu-id="41039-171">Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="41039-171">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

### <a name="notifications-from-wave-batch-job-execution"></a><span data-ttu-id="41039-172">Voo partiitöö käivitamise teatised</span><span class="sxs-lookup"><span data-stu-id="41039-172">Notifications from wave batch job execution</span></span>

<span data-ttu-id="41039-173">Olenevalt teie ärisündmuste seadistusest saate te lõpuks teate voo käivitamise tõrke kohta.</span><span class="sxs-lookup"><span data-stu-id="41039-173">Depending on the setup of your business events, you will eventually receive a notification about wave execution failure.</span></span> <span data-ttu-id="41039-174">Tegevuskeskuse teade sarnaneb järgmise näitega ja sisaldab linki nurjunud voole.</span><span class="sxs-lookup"><span data-stu-id="41039-174">The Action center message will resemble the following example and will include a link to the wave that failed.</span></span>

> <span data-ttu-id="41039-175">**Tõrge voo käivitamise ajal**</span><span class="sxs-lookup"><span data-stu-id="41039-175">**Error during wave execution**</span></span>  
> <span data-ttu-id="41039-176">Voo USMF-000000001 käitamisel esines tõrge.</span><span class="sxs-lookup"><span data-stu-id="41039-176">An error occurred while executing wave USMF-000000001.</span></span>  
> <span data-ttu-id="41039-177">Viimased teated: voo USMF-000000001 jaoks tööd ei loodud.</span><span class="sxs-lookup"><span data-stu-id="41039-177">Last messages: No Work was created for Wave USMF-000000001.</span></span>
>
> <span data-ttu-id="41039-178">**OLEK**</span><span class="sxs-lookup"><span data-stu-id="41039-178">**STATUS**</span></span>  
> <span data-ttu-id="41039-179">Aktiivne</span><span class="sxs-lookup"><span data-stu-id="41039-179">Active</span></span>
>
> <span data-ttu-id="41039-180">Ava voo üksikasjad</span><span class="sxs-lookup"><span data-stu-id="41039-180">Open wave details</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
