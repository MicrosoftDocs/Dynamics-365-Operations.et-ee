---
title: Voomalli rühmitamine
description: Voomalli rühmitamine võimaldab süsteemil kasutada voomalli seadistusi, et määrata teie määratletud kriteeriumide põhjal, kuidas see peaks tükeldama väljastatud ridu ja määrama neid uutele või olemasolevatele voogudele. Sellest funktsioonist võib olla kasu ladudes, kus voogusid luuakse kindlate kriteeriumide põhjal, kuid kus juhid eelistavad käsitsi loomise asemel luua voogusid automaatselt.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4dd188cbd17cfed372283ecb3389633b0c0021eb
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530462"
---
# <a name="wave-template-grouping"></a><span data-ttu-id="872af-104">Voomalli rühmitamine</span><span class="sxs-lookup"><span data-stu-id="872af-104">Wave template grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="872af-105">Voomalli rühmitamine võimaldab süsteemil kasutada [voomalli seadistusi](tasks/configure-wave-processing.md), et määrata teie määratletud kriteeriumide põhjal, kuidas see peaks tükeldama väljastatud ridu ja määrama neid uutele või olemasolevatele voogudele.</span><span class="sxs-lookup"><span data-stu-id="872af-105">Wave template grouping enables the system to use [wave template](tasks/configure-wave-processing.md) setups to determine, based on criteria that you define, how it should split released lines and assign them to new or existing waves.</span></span> <span data-ttu-id="872af-106">Sellest funktsioonist võib olla kasu ladudes, kus voogusid luuakse kindlate kriteeriumide põhjal, kuid kus juhid eelistavad käsitsi loomise asemel luua voogusid automaatselt.</span><span class="sxs-lookup"><span data-stu-id="872af-106">This feature can be useful in warehouses where waves are created based on specific criteria, but where managers prefer to create waves automatically instead of manually.</span></span> <span data-ttu-id="872af-107">See võimaldab süsteemil lisada iga äsja väljastatud saadetise esimesele leitavale voole, millel on samad rühmitamise välja väärtused.</span><span class="sxs-lookup"><span data-stu-id="872af-107">It enables the system to add each newly released shipment to the first wave that it finds that has matching grouping field values.</span></span> <span data-ttu-id="872af-108">Kui vastet ei leita, loob süsteem uue saadetise jaoks uue voo.</span><span class="sxs-lookup"><span data-stu-id="872af-108">If no match is found, the system creates a new wave for the new shipment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="872af-109">Voomalli rühmitamine pole toetatud töötüüpide *töömaterjalide komplekteerimine* või *kanbani komplekteerimine* jaoks.</span><span class="sxs-lookup"><span data-stu-id="872af-109">Wave template grouping isn't supported for the work types *production raw material picking* or *Kanban picking*.</span></span> <span data-ttu-id="872af-110">See on seetõttu, et voo rühmitamine põhineb saadetistel ja need töötüübid ei kasuta saadetisi.</span><span class="sxs-lookup"><span data-stu-id="872af-110">This is because wave grouping is based on shipments and these work types don't use shipments.</span></span>

## <a name="turn-on-the-wave-template-grouping-feature"></a><span data-ttu-id="872af-111">Voomalli rühmitamise funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="872af-111">Turn on the Wave template grouping feature</span></span>

<span data-ttu-id="872af-112">Enne funktsiooni *Voomalli rühmitamine* kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="872af-112">Before you can use the *Wave template grouping* feature, it must be turned on in your system.</span></span> <span data-ttu-id="872af-113">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="872af-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="872af-114">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="872af-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="872af-115">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="872af-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="872af-116">**Funktsiooni nimi:** *Voomalli rühmitamine*</span><span class="sxs-lookup"><span data-stu-id="872af-116">**Feature name:** *Wave template grouping*</span></span>

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a><span data-ttu-id="872af-117">Voomalli määramine voomalli rühmitamise kasutamiseks</span><span class="sxs-lookup"><span data-stu-id="872af-117">Set a wave template to use wave template grouping</span></span>

<span data-ttu-id="872af-118">Voomalli rühmitamise kättesaadavaks tegemiseks järgige neid etappe oma [voomalli](tasks/configure-wave-processing.md) seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="872af-118">To make wave template grouping available, follow these steps to set up your [wave template](tasks/configure-wave-processing.md).</span></span>

1. <span data-ttu-id="872af-119">Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.</span><span class="sxs-lookup"><span data-stu-id="872af-119">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="872af-120">Valige vasakus paanis seadistatav voomall.</span><span class="sxs-lookup"><span data-stu-id="872af-120">In the left pane, select the wave template to set up.</span></span> <span data-ttu-id="872af-121">Kui valmistute seda stsenaariumit demoandmete abil läbi töötama selles teemas hiljem, valige mall **62 saadetise vaikemall**.</span><span class="sxs-lookup"><span data-stu-id="872af-121">If you're preparing to work through the scenario later in this topic by using demo data, select the **62 Shipping default** template.</span></span>
1. <span data-ttu-id="872af-122">Lehe redigeerimisrežiimi panemiseks valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="872af-122">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="872af-123">Määrake kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="872af-123">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="872af-124">**Automatiseeri voo loomine:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="872af-124">**Automate wave creation:** *Yes*</span></span>
    - <span data-ttu-id="872af-125">**Määra avatud voogudele:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="872af-125">**Assign to open waves:** *Yes*</span></span>
    - <span data-ttu-id="872af-126">**Töötle voogu lattu vabastamisel:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="872af-126">**Process wave at release to warehouse:** *No*</span></span>

1. <span data-ttu-id="872af-127">Valige toimingupaanil suvand **Redigeeri päringut**, et avada dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="872af-127">On the Action Pane, select **Edit query** to open the query dialog box.</span></span>
1. <span data-ttu-id="872af-128">Vaadake üle päringu dialoogiboksi vahekaardil **Sortimine** sortimise kriteeriumid ja veenduge, et oleks olemas reegel, mis sisaldab välja, mida soovite kasutada oma voogude rühmitamiseks.</span><span class="sxs-lookup"><span data-stu-id="872af-128">In the query dialog box, on the **Sorting** tab, review the sorting criteria, and make sure that there is a rule that includes the field that you want to use to group your waves.</span></span>

    <span data-ttu-id="872af-129">Kui valmistute seda stsenaariumit demoandmete abil läbi töötama, lisage rida, millel on järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="872af-129">If you're preparing to work through the scenario by using demo data, add a row that has the following values:</span></span>

    - <span data-ttu-id="872af-130">**Tabel:** *Saadetised*</span><span class="sxs-lookup"><span data-stu-id="872af-130">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="872af-131">**Tuletatud tabel:** *Saadetised*</span><span class="sxs-lookup"><span data-stu-id="872af-131">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="872af-132">**Väli:** *Vedaja teenus*</span><span class="sxs-lookup"><span data-stu-id="872af-132">**Field:** *Carrier service*</span></span>

        > [!NOTE]
        > <span data-ttu-id="872af-133">Kui valite selle väärtuse, võidakse kuvada järgmine teade: „Väli Vedaja teenus pole indeksi väli.</span><span class="sxs-lookup"><span data-stu-id="872af-133">After you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="872af-134">Kas soovite lisada sellele sortimise?”</span><span class="sxs-lookup"><span data-stu-id="872af-134">Do you want to add sorting on this?"</span></span> <span data-ttu-id="872af-135">Sortimise lisamiseks valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="872af-135">Select **Yes** to add sorting.</span></span>

    - <span data-ttu-id="872af-136">**Otsingusuund:** *Kasvav*</span><span class="sxs-lookup"><span data-stu-id="872af-136">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="872af-137">Oma muudatuste salvestamiseks ja päringu dialoogiboksi sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="872af-137">Select **OK** to save your changes and close the query dialog box.</span></span>
1. <span data-ttu-id="872af-138">Valige toimingupaanil **Voomalli rühmitamine**.</span><span class="sxs-lookup"><span data-stu-id="872af-138">On the Action Pane, select **Wave template grouping**.</span></span>
1. <span data-ttu-id="872af-139">Vastavalt vajadusele, valige lehel **Voomalli rühmitamine** märkeruut **Grupeerimisalus** iga rea puhul, mida soovite kasutada tellimuseridade voogudeks rühmitamiseks.</span><span class="sxs-lookup"><span data-stu-id="872af-139">On the **Wave template grouping** page, select the **Group by** check box for each row that you want to use to group your order lines into waves, as required.</span></span> <span data-ttu-id="872af-140">Kui valmistute seda stsenaariumit demoandmete abil läbi töötama, märkige ruut **Grupeerimisalus** rea *Vedaja teenus* jaoks.</span><span class="sxs-lookup"><span data-stu-id="872af-140">If you're preparing to work through the scenario by using demo data, select the **Group by** check box for the *Carrier service* row.</span></span>
1. <span data-ttu-id="872af-141">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="872af-141">Select **Save**.</span></span>
1. <span data-ttu-id="872af-142">Sulgege leht **Voomalli rühmitamine**.</span><span class="sxs-lookup"><span data-stu-id="872af-142">Close the **Wave template grouping** page.</span></span>
1. <span data-ttu-id="872af-143">Oma malli salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="872af-143">Select **Save** to save your template.</span></span>

## <a name="scenario"></a><span data-ttu-id="872af-144">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="872af-144">Scenario</span></span>

<span data-ttu-id="872af-145">Selles jaotises antakse skript, mille läbi töötamisel saate teada, mida see funktsioon teeb ja kuidas sellega töötada.</span><span class="sxs-lookup"><span data-stu-id="872af-145">This section provides a script that you can work through to learn what this feature does and how to work with it.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="872af-146">Näidisandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="872af-146">Make sample data available</span></span>

<span data-ttu-id="872af-147">Selle stsenaariumi kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="872af-147">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="872af-148">Enne alustamist peate valima ka juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="872af-148">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="872af-149">Seda stsenaariumi saate kasutada ka juhistena funktsiooni kasutamiseks, kui töötate tootmissüsteemis.</span><span class="sxs-lookup"><span data-stu-id="872af-149">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="872af-150">Kuid sellisel juhul peate asendama oma väärtused ja teil ei pruugi olla teatud tüüpi nõutavaid kirjeid, mida pakuvad standardsed demoandmed.</span><span class="sxs-lookup"><span data-stu-id="872af-150">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="scenario-wave-template-grouping"></a><span data-ttu-id="872af-151">Stsenaarium: Voomalli rühmitamine</span><span class="sxs-lookup"><span data-stu-id="872af-151">Scenario: Wave template grouping</span></span>

<span data-ttu-id="872af-152">Selles stsenaariumis kirjeldatakse, kuidas kasutada voomalli rühmitamist mitme voo automaatseks loomiseks voomallis määratletud rühmitamiskriteeriumi põhjal.</span><span class="sxs-lookup"><span data-stu-id="872af-152">This scenario shows how to use wave template grouping to automatically create multiple waves, based on grouping criteria that are defined in a wave template.</span></span> <span data-ttu-id="872af-153">Selles stsenaariumis seadistatakse voomall süsteemis, et luua üks voog vedaja teenuse kohta.</span><span class="sxs-lookup"><span data-stu-id="872af-153">In this scenario, the wave template is set up in the system to create one wave per carrier service.</span></span>

<span data-ttu-id="872af-154">Enne alustamist valmistage voomall ette selles teemas eelnevalt kirjeldatud jaotises [Voomalli määramine voomalli rühmitamise kasutamiseks](#set-up-template) olevate juhiste põhjal.</span><span class="sxs-lookup"><span data-stu-id="872af-154">Before you begin, prepare your wave template as described in the [Set a wave template to use wave template grouping](#set-up-template) section earlier in this topic.</span></span> <span data-ttu-id="872af-155">Kui te töötate demoandmetega selles stsenaariumis, kasutage kindlasti demoandmete väärtusi, mida selles protseduuris soovitatakse.</span><span class="sxs-lookup"><span data-stu-id="872af-155">If you will be working with demo data for this scenario, be sure to use the demo data values that are suggested in that procedure.</span></span> <span data-ttu-id="872af-156">See seadistus rühmitab teie vood vastavalt vedaja teenusele, mis määratakse iga müügitellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="872af-156">This setup will group your waves according to the carrier service that is set for each sales order.</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="872af-157">Müügitellimuse 1 loomine</span><span class="sxs-lookup"><span data-stu-id="872af-157">Create sales order 1</span></span>

1. <span data-ttu-id="872af-158">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="872af-158">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="872af-159">Müügitellimuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="872af-159">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="872af-160">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="872af-160">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="872af-161">Määrake kiirkaardi **Klient** välja **Kliendi konto** väärtuseks *US-004*.</span><span class="sxs-lookup"><span data-stu-id="872af-161">On the **Customer** FastTab, set the **Customer account** field to *US-004*.</span></span>
    - <span data-ttu-id="872af-162">Määrake kiirkaardi **Üldine** välja **Ladu** väärtuseks *62*.</span><span class="sxs-lookup"><span data-stu-id="872af-162">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="872af-163">Valige müügitellimuse loomiseks **OK** ja sulgege dialoogiboks **Müügitellimuse loomine**.</span><span class="sxs-lookup"><span data-stu-id="872af-163">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="872af-164">Uus müügitellimus avatakse vaates **Read**.</span><span class="sxs-lookup"><span data-stu-id="872af-164">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="872af-165">Märkige üles müügitellimuse number.</span><span class="sxs-lookup"><span data-stu-id="872af-165">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="872af-166">Lülituge vaatele **Päis**.</span><span class="sxs-lookup"><span data-stu-id="872af-166">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="872af-167">Määrake kiirkaardi **Tarne** jaotises **Transport** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="872af-167">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="872af-168">**Vedaja:** *Kaubalennuk*</span><span class="sxs-lookup"><span data-stu-id="872af-168">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="872af-169">**Vedaja teenus:** *Õhk*</span><span class="sxs-lookup"><span data-stu-id="872af-169">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="872af-170">Minge tagasi vaatesse **Read**.</span><span class="sxs-lookup"><span data-stu-id="872af-170">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="872af-171">Valige jaotises **Müügitellimuse read** suvand **Lisa rida**, et lisada rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="872af-171">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="872af-172">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="872af-172">On the new line, set the following values:</span></span>

    - <span data-ttu-id="872af-173">**Kauba kood:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="872af-173">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="872af-174">**Kogus:** *2*</span><span class="sxs-lookup"><span data-stu-id="872af-174">**Quantity:** *2*</span></span>

1. <span data-ttu-id="872af-175">Valige uus tellimuserida ja seejärel valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="872af-175">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="872af-176">Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.</span><span class="sxs-lookup"><span data-stu-id="872af-176">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="872af-177">Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="872af-177">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="872af-178">Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="872af-178">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="872af-179">Saate teate, mis näitab saadetist ja voogu selle tellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="872af-179">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="872af-180">Märkige üles voo ID-kood ja saadetise ID-koodid.</span><span class="sxs-lookup"><span data-stu-id="872af-180">Make a note of the wave ID number and the shipment ID numbers.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a><span data-ttu-id="872af-181">Müügitellimuse 1 jaoks loodud voo kuvamine</span><span class="sxs-lookup"><span data-stu-id="872af-181">View the wave that was created from sales order 1</span></span>

1. <span data-ttu-id="872af-182">Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.</span><span class="sxs-lookup"><span data-stu-id="872af-182">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="872af-183">Valige voo ID, mis loodi müügitellimusest.</span><span class="sxs-lookup"><span data-stu-id="872af-183">Select the wave ID that was created from the sales order.</span></span>
1. <span data-ttu-id="872af-184">Valige voo ID link, et avada voo üksikasjade leht.</span><span class="sxs-lookup"><span data-stu-id="872af-184">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="872af-185">Pange tähele, et saadetis on lisatud kiirkaardile **Voo read**.</span><span class="sxs-lookup"><span data-stu-id="872af-185">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="872af-186">Müügitellimuse 2 loomine</span><span class="sxs-lookup"><span data-stu-id="872af-186">Create sales order 2</span></span>

1. <span data-ttu-id="872af-187">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="872af-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="872af-188">Müügitellimuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="872af-188">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="872af-189">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="872af-189">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="872af-190">Määrake kiirkaardi **Klient** välja **Kliendi konto** väärtuseks *US-005*.</span><span class="sxs-lookup"><span data-stu-id="872af-190">On the **Customer** FastTab, set the **Customer account** field to *US-005*.</span></span>
    - <span data-ttu-id="872af-191">Määrake kiirkaardi **Üldine** välja **Ladu** väärtuseks *62*.</span><span class="sxs-lookup"><span data-stu-id="872af-191">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="872af-192">Valige müügitellimuse loomiseks **OK** ja sulgege dialoogiboks **Müügitellimuse loomine**.</span><span class="sxs-lookup"><span data-stu-id="872af-192">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="872af-193">Uus müügitellimus avatakse vaates **Read**.</span><span class="sxs-lookup"><span data-stu-id="872af-193">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="872af-194">Märkige üles müügitellimuse number.</span><span class="sxs-lookup"><span data-stu-id="872af-194">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="872af-195">Lülituge vaatele **Päis**.</span><span class="sxs-lookup"><span data-stu-id="872af-195">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="872af-196">Määrake kiirkaardi **Tarne** jaotises **Transport** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="872af-196">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="872af-197">**Vedaja:** *Voogude liigutamine*</span><span class="sxs-lookup"><span data-stu-id="872af-197">**Shipping carrier:** *Flower moving*</span></span>
    - <span data-ttu-id="872af-198">**Vedaja teenus:** *Std*</span><span class="sxs-lookup"><span data-stu-id="872af-198">**Carrier service:** *Std*</span></span>

1. <span data-ttu-id="872af-199">Minge tagasi vaatesse **Read**.</span><span class="sxs-lookup"><span data-stu-id="872af-199">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="872af-200">Valige jaotises **Müügitellimuse read** suvand **Lisa rida**, et lisada rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="872af-200">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="872af-201">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="872af-201">On the new line, set the following values:</span></span>

    - <span data-ttu-id="872af-202">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="872af-202">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="872af-203">**Kogus:** *1*</span><span class="sxs-lookup"><span data-stu-id="872af-203">**Quantity:** *1*</span></span>

1. <span data-ttu-id="872af-204">Valige uus tellimuserida ja seejärel valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="872af-204">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="872af-205">Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.</span><span class="sxs-lookup"><span data-stu-id="872af-205">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="872af-206">Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="872af-206">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="872af-207">Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="872af-207">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="872af-208">Saate teate, mis näitab saadetist ja voogu selle tellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="872af-208">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="872af-209">Märkige üles voo ID-kood ja saadetise ID-koodid.</span><span class="sxs-lookup"><span data-stu-id="872af-209">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="872af-210">Pange tähele, et voo ID erineb esimese müügitellimuse voo ID-st.</span><span class="sxs-lookup"><span data-stu-id="872af-210">Notice that the wave ID differs from the wave ID of the first sales order.</span></span>

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a><span data-ttu-id="872af-211">Müügitellimuse 2 jaoks loodud voo kuvamine</span><span class="sxs-lookup"><span data-stu-id="872af-211">View the wave that was created from sales order 2</span></span>

1. <span data-ttu-id="872af-212">Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.</span><span class="sxs-lookup"><span data-stu-id="872af-212">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="872af-213">Valige voo ID, mis loodi teisest müügitellimusest.</span><span class="sxs-lookup"><span data-stu-id="872af-213">Select the wave ID that was created from the second sales order.</span></span>
1. <span data-ttu-id="872af-214">Valige voo ID link, et avada voo üksikasjade leht.</span><span class="sxs-lookup"><span data-stu-id="872af-214">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="872af-215">Pange tähele, et saadetis on lisatud kiirkaardile **Voo read**.</span><span class="sxs-lookup"><span data-stu-id="872af-215">Notice that the shipment has been added to the **Wave lines** FastTab.</span></span>

<span data-ttu-id="872af-216">Selle saadetise jaoks loodi uus voog, kuna see kasutab esimesest müügitellimusest erinevat vedaja teenust.</span><span class="sxs-lookup"><span data-stu-id="872af-216">A new wave was created for this shipment, because it uses a different carrier service than the first sales order.</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="872af-217">Müügitellimuse 3 loomine</span><span class="sxs-lookup"><span data-stu-id="872af-217">Create sales order 3</span></span>

1. <span data-ttu-id="872af-218">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="872af-218">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="872af-219">Müügitellimuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="872af-219">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="872af-220">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="872af-220">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="872af-221">Määrake kiirkaardi **Klient** välja **Kliendi konto** väärtuseks *US-006*.</span><span class="sxs-lookup"><span data-stu-id="872af-221">On the **Customer** FastTab, set the **Customer account** field to *US-006*.</span></span>
    - <span data-ttu-id="872af-222">Määrake kiirkaardi **Üldine** välja **Ladu** väärtuseks *62*.</span><span class="sxs-lookup"><span data-stu-id="872af-222">On the **General** FastTab, set the **Warehouse** field to *62*.</span></span>

1. <span data-ttu-id="872af-223">Valige müügitellimuse loomiseks **OK** ja sulgege dialoogiboks **Müügitellimuse loomine**.</span><span class="sxs-lookup"><span data-stu-id="872af-223">Select **OK** to create the sales order and close the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="872af-224">Uus müügitellimus avatakse vaates **Read**.</span><span class="sxs-lookup"><span data-stu-id="872af-224">The new sales order is opened in the **Lines** view.</span></span> <span data-ttu-id="872af-225">Märkige üles müügitellimuse number.</span><span class="sxs-lookup"><span data-stu-id="872af-225">Make a note of the sales order number.</span></span>
1. <span data-ttu-id="872af-226">Lülituge vaatele **Päis**.</span><span class="sxs-lookup"><span data-stu-id="872af-226">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="872af-227">Määrake kiirkaardi **Tarne** jaotises **Transport** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="872af-227">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="872af-228">**Vedaja:** *Kaubalennuk*</span><span class="sxs-lookup"><span data-stu-id="872af-228">**Shipping carrier:** *Air Cargo*</span></span>
    - <span data-ttu-id="872af-229">**Vedaja teenus:** *Õhk*</span><span class="sxs-lookup"><span data-stu-id="872af-229">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="872af-230">Minge tagasi vaatesse **Read**.</span><span class="sxs-lookup"><span data-stu-id="872af-230">Switch back to the **Lines** view.</span></span>
1. <span data-ttu-id="872af-231">Valige jaotises **Müügitellimuse read** suvand **Lisa rida**, et lisada rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="872af-231">In the **Sales order lines** section, select **Add line** to add a line to the grid.</span></span>
1. <span data-ttu-id="872af-232">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="872af-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="872af-233">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="872af-233">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="872af-234">**Kogus:** *1*</span><span class="sxs-lookup"><span data-stu-id="872af-234">**Quantity:** *1*</span></span>

1. <span data-ttu-id="872af-235">Valige uus tellimuserida ja seejärel valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="872af-235">Select the new order line, and then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="872af-236">Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.</span><span class="sxs-lookup"><span data-stu-id="872af-236">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="872af-237">Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="872af-237">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="872af-238">Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="872af-238">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="872af-239">Saate teate, mis näitab saadetist ja voogu selle tellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="872af-239">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="872af-240">Märkige üles voo ID-kood ja saadetise ID-koodid.</span><span class="sxs-lookup"><span data-stu-id="872af-240">Make a note of the wave ID number and the shipment ID numbers.</span></span> <span data-ttu-id="872af-241">Saadetis määrati olemasolevale voole esimesest müügitellimusest.</span><span class="sxs-lookup"><span data-stu-id="872af-241">The shipment has been assigned to the existing wave from the first sales order.</span></span>

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a><span data-ttu-id="872af-242">Müügitellimuste 1 ja 3 voo kuvamine</span><span class="sxs-lookup"><span data-stu-id="872af-242">View the wave for sales orders 1 and 3</span></span>

1. <span data-ttu-id="872af-243">Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.</span><span class="sxs-lookup"><span data-stu-id="872af-243">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="872af-244">Valige voo ID, mis loodi kolmandast müügitellimusest.</span><span class="sxs-lookup"><span data-stu-id="872af-244">Select the wave ID that was created from the third sales order.</span></span>
1. <span data-ttu-id="872af-245">Valige voo ID link, et avada voo üksikasjade leht.</span><span class="sxs-lookup"><span data-stu-id="872af-245">Select the wave ID link to open the wave details page.</span></span>
1. <span data-ttu-id="872af-246">Pange tähele, et saadetis lisati kiirkaardile **Voo read** koos esimese müügitellimuse saadetisega.</span><span class="sxs-lookup"><span data-stu-id="872af-246">Notice that the shipment has been added to the **Wave lines** FastTab, together with the shipment for the first sales order.</span></span>
