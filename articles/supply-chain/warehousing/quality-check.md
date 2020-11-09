---
title: Kvaliteedikontroll
description: Sellest teemast leiate teavet kvaliteedikontrolli funktsiooni kohta. See funktsioon võimaldab laotöötajatel teha kiireid, pistelisi kontrolle kaupade vastuvõtmisel saabumisalale.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: dfb71f74732d65409003c4f6f74145442a1efa3f
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016627"
---
# <a name="quality-check"></a><span data-ttu-id="36a21-104">Kvaliteedikontroll</span><span class="sxs-lookup"><span data-stu-id="36a21-104">Quality check</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36a21-105">Funktsioon *Kvaliteedikontroll* võimaldab laotöötajatel teha kiireid, pistelisi kontrolle kaupade vastuvõtmisel saabumisalale.</span><span class="sxs-lookup"><span data-stu-id="36a21-105">The *Quality check* feature lets warehouse workers do quick spot checks for quality while they receive items to the inbound dock area.</span></span> <span data-ttu-id="36a21-106">Need pistelised kontrollid on kasulikud, kui töötajad kontrollivad kauba pakendit või muid kergesti äratuntavaid kaupade osi.</span><span class="sxs-lookup"><span data-stu-id="36a21-106">These spot checks are beneficial when workers inspect packaging or other easily recognizable parts of an item.</span></span> <span data-ttu-id="36a21-107">Funktsioon juhendab töötajaid kiirelt vaatama, kas midagi on ilmselgelt vigane või kahjustatud, enne kui nad ladustavad laokaubad ladustamise asukohta.</span><span class="sxs-lookup"><span data-stu-id="36a21-107">The feature guides workers to take a quick look to see whether anything is obviously faulty or damaged before they stock the inventory in its putaway location.</span></span>

<span data-ttu-id="36a21-108">See funktsioon on standardse kvaliteedikontrolli alternatiiv.</span><span class="sxs-lookup"><span data-stu-id="36a21-108">This feature is an alternative to the standard quality check process.</span></span> <span data-ttu-id="36a21-109">See pakub rohkem paindlikkust ja kiiremat töötlemist.</span><span class="sxs-lookup"><span data-stu-id="36a21-109">It offers more flexibility and faster processing.</span></span>

<span data-ttu-id="36a21-110">Selle funktsiooni kasutamisel toimub saabumis- ja kvaliteedikontroll järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="36a21-110">When you use this feature, the arrival and quality check occur in the following way:</span></span>

1. <span data-ttu-id="36a21-111">Kui saadetis saabub, registreerib laotöötaja saabumise.</span><span class="sxs-lookup"><span data-stu-id="36a21-111">When a shipment arrives, a warehouse worker registers the arrival.</span></span> <span data-ttu-id="36a21-112">Asukoha registreerimiseks skannib töötaja ka litsentsiplaadi.</span><span class="sxs-lookup"><span data-stu-id="36a21-112">The worker also scans a license plate to register the location.</span></span>
1. <span data-ttu-id="36a21-113">Töötaja teeb kiire kvaliteedikontrolli ja salvestab selle litsentsiplaadi tulemuse (läbitud või nurjus).</span><span class="sxs-lookup"><span data-stu-id="36a21-113">The worker does a quick quality check and records the result (pass or fail) for that license plate.</span></span>
1. <span data-ttu-id="36a21-114">Aset leiab üks järgmistest toimingutest.</span><span class="sxs-lookup"><span data-stu-id="36a21-114">One of the following actions occurs:</span></span>

    - <span data-ttu-id="36a21-115">Kui kvaliteedikontroll on läbitud, võetakse litsentsiplaat vastu ja suunatakse vastuvõtvasse asukohta, nagu tavaliselt.</span><span class="sxs-lookup"><span data-stu-id="36a21-115">If the quality check is passed, the license plate is accepted and guided to a receiving location, as usual.</span></span>
    - <span data-ttu-id="36a21-116">Kui kvaliteedikontroll ebaõnnestus, lükatakse litsentsiplaat tagasi ja selle olemasolev ladustamistöö suunatakse ümber edasiseks kontrollimiseks alternatiivsesse asukohta.</span><span class="sxs-lookup"><span data-stu-id="36a21-116">If the quality check is failed, the license plate is rejected, and existing putaway work for it is redirected to an alternate location for further inspection.</span></span> <span data-ttu-id="36a21-117">Luuakse uus kvaliteettellimus.</span><span class="sxs-lookup"><span data-stu-id="36a21-117">A new quality order is created.</span></span> <span data-ttu-id="36a21-118">Nurjunud kvaliteedikontrolli põhjal loodud kvaliteettellimuse vaatamiseks avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Kvaliteettellimused**.</span><span class="sxs-lookup"><span data-stu-id="36a21-118">To view the quality order that is created from the failed quality check, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="36a21-119">Seda protsessi saab häälestada ka nii, et kõik skannitud litsentsiplaadid suunatakse kohe kvaliteedikontrolli asukohta.</span><span class="sxs-lookup"><span data-stu-id="36a21-119">This process can also be set up so that all scanned license plates are immediately diverted to the quality check location.</span></span>

## <a name="turn-on-the-quality-check-feature"></a><span data-ttu-id="36a21-120">Kvaliteedikontrolli funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="36a21-120">Turn on the Quality check feature</span></span>

<span data-ttu-id="36a21-121">Enne funktsiooni *Kvaliteedikontroll* kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="36a21-121">Before you can use the *Quality check* feature, it must be turned on in your system.</span></span> <span data-ttu-id="36a21-122">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="36a21-122">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="36a21-123">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="36a21-123">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="36a21-124">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="36a21-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="36a21-125">**Funktsiooni nimi:** *Kvaliteedikontroll*</span><span class="sxs-lookup"><span data-stu-id="36a21-125">**Feature name:** *Quality check*</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="36a21-126">Funktsiooni häälestamine näidisstsenaariumi jaoks</span><span class="sxs-lookup"><span data-stu-id="36a21-126">Set up the feature for the example scenario</span></span>

<span data-ttu-id="36a21-127">Sellest jaotisest leiate juhised ja näite funktsiooni *Kvaliteedikontroll* häälestamise ning näidisandmete ettevalmistamise kohta teemas hiljem esitatud näidisstsenaariumi jaoks.</span><span class="sxs-lookup"><span data-stu-id="36a21-127">This section provides guidelines and an example that shows how to set up the *Quality check* feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="36a21-128">Näidisandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="36a21-128">Make sample data available</span></span>

<span data-ttu-id="36a21-129">Selle [näidisstsenaariumi](#example-scenario) kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="36a21-129">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="36a21-130">Enne alustamist peate valima ka juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="36a21-130">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="quality-check-template"></a><a name="quality-template"></a><span data-ttu-id="36a21-131">Kvaliteedikontrolli mall</span><span class="sxs-lookup"><span data-stu-id="36a21-131">Quality check template</span></span>

<span data-ttu-id="36a21-132">Kvaliteedikontrolli mall määratleb reeglid, mille alusel saab vastuvõtmise ajal teha kiireid, pistelisi kontrolle.</span><span class="sxs-lookup"><span data-stu-id="36a21-132">The quality check template defines the rules for doing quick spot checks for quality at the time of receiving.</span></span>

1. <span data-ttu-id="36a21-133">Avage **Laohaldus \> Häälestamine \> Töö \> Kvaliteedikontrolli mall**.</span><span class="sxs-lookup"><span data-stu-id="36a21-133">Go to **Warehouse management \> Setup \> Work \> Quality check template**.</span></span>
1. <span data-ttu-id="36a21-134">Malli lisamiseks tabelisse klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="36a21-134">Select **New** to add a template to the grid.</span></span>
1. <span data-ttu-id="36a21-135">Uue malli määratlemiseks määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-135">Set the following values to define the new template:</span></span>

    - <span data-ttu-id="36a21-136">**Kvaliteedikontrolli malli nimi:** *Laadimissilla kontroll*</span><span class="sxs-lookup"><span data-stu-id="36a21-136">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="36a21-137">Sisestage nimi, mis tuvastab sellele mallile rakendatud poliitikad.</span><span class="sxs-lookup"><span data-stu-id="36a21-137">Enter a name that identifies the policies applied for this template.</span></span>

    - <span data-ttu-id="36a21-138">**Vastuvõtupoliitika:** *Küsi kasutajalt*</span><span class="sxs-lookup"><span data-stu-id="36a21-138">**Acceptance policy:** *Prompt user*</span></span>

        <span data-ttu-id="36a21-139">Määrake, kas kasutajatelt peaks töö töötlemise ajal küsima varude vastuvõtmist või tagasilükkamist või kas kvaliteet tuleks automaatselt tagasi lükata.</span><span class="sxs-lookup"><span data-stu-id="36a21-139">Specify whether users should be prompted to accept or reject the quality of the inventory while they process the work, or whether the quality should automatically be rejected.</span></span> <span data-ttu-id="36a21-140">Saadaolevad valikud on *Lükka automaatselt tagasi* ja *Küsi kasutajalt*.</span><span class="sxs-lookup"><span data-stu-id="36a21-140">The available options are *Auto reject* and *Prompt user*.</span></span>

    - <span data-ttu-id="36a21-141">**Kvaliteeditöötluse poliitika:** *Loo kvaliteettellimus*</span><span class="sxs-lookup"><span data-stu-id="36a21-141">**Quality processing policy:** *Create quality order*</span></span>

        <span data-ttu-id="36a21-142">Valige poliitika, mida tuleks kasutada varude kvaliteedi tagasilükkamise korral.</span><span class="sxs-lookup"><span data-stu-id="36a21-142">Select the policy that should be used when the quality of the inventory is rejected.</span></span> <span data-ttu-id="36a21-143">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="36a21-143">The following options are available:</span></span>

        - <span data-ttu-id="36a21-144">*Loo ainult töö* – varude liikumise lihtsustamiseks looge vaid töö.</span><span class="sxs-lookup"><span data-stu-id="36a21-144">*Create work only* – Just create work to facilitate inventory movement.</span></span>
        - <span data-ttu-id="36a21-145">*Loo kvaliteettellimus* – kvaliteedikatsete lihtsustamiseks saate luua kvaliteettellimuse.</span><span class="sxs-lookup"><span data-stu-id="36a21-145">*Create quality order* – Create a quality order to facilitate quality tests.</span></span>

    - <span data-ttu-id="36a21-146">**Katsegrupp:** *Raamistus*</span><span class="sxs-lookup"><span data-stu-id="36a21-146">**Test group:** *Enclosure*</span></span>

        <span data-ttu-id="36a21-147">Määrake katsegrupp, mida tuleks loodud kvaliteettellimuses kasutada.</span><span class="sxs-lookup"><span data-stu-id="36a21-147">Specify the test group that should be used in the quality order that is created.</span></span> <span data-ttu-id="36a21-148">Katsegrupid häälestatakse mooduli **Laohaldus**.</span><span class="sxs-lookup"><span data-stu-id="36a21-148">Test groups are set up in the **Inventory management** module.</span></span>

        <span data-ttu-id="36a21-149">Jätke katsegrupi jaoks suvand **Purustav katse** väljalülitatuks.</span><span class="sxs-lookup"><span data-stu-id="36a21-149">Leave the **Destructive text** option turned off for the test group.</span></span> <span data-ttu-id="36a21-150">See suvand määratleb, kas näidis tuleks katsegrupi katse osana hävitada.</span><span class="sxs-lookup"><span data-stu-id="36a21-150">This option defines whether the sample will be destroyed as part of the tests in the test group.</span></span> <span data-ttu-id="36a21-151">Purustava katse kasutamisel genereerib süsteem varude kande, kui kauba jaoks luuakse kvaliteettellimus.</span><span class="sxs-lookup"><span data-stu-id="36a21-151">If a destructive test is used, the system generates an inventory transaction when a quality order is created for an item.</span></span> <span data-ttu-id="36a21-152">Uus laokanne prognoosib varude vähendamist testikoguse puhul.</span><span class="sxs-lookup"><span data-stu-id="36a21-152">The new inventory transaction predicts the inventory reduction for the test quantity.</span></span> <span data-ttu-id="36a21-153">Varude vähendamine toimub, kui kvaliteettellimus viiakse lõpule kinnitamisetapi kaudu.</span><span class="sxs-lookup"><span data-stu-id="36a21-153">The inventory reduction occurs when the quality order is completed through the validation step.</span></span> <span data-ttu-id="36a21-154">Varude ülekanne tuvastatakse kvaliteettellimusena.</span><span class="sxs-lookup"><span data-stu-id="36a21-154">The inventory transaction is identified as a quality order.</span></span>

### <a name="work-class--quality-check"></a><a name="work-class"></a><span data-ttu-id="36a21-155">Tööklass – kvaliteedikontroll</span><span class="sxs-lookup"><span data-stu-id="36a21-155">Work class – Quality check</span></span>

<span data-ttu-id="36a21-156">Tööklassidega suunatakse ja/või piiratakse töötellimuse ridade tüüpi, mida laotöötajad saavad mobiilses seadmes töödelda.</span><span class="sxs-lookup"><span data-stu-id="36a21-156">Work classes are used to direct and/or limit the type of work order lines that warehouse workers can process on a mobile device.</span></span>

1. <span data-ttu-id="36a21-157">Minge jaotisse **Laohaldus \> Seadistus \> Töö \> Töö klassid**.</span><span class="sxs-lookup"><span data-stu-id="36a21-157">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="36a21-158">Valige tööklassi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="36a21-158">Select **New** to create a work class.</span></span>
1. <span data-ttu-id="36a21-159">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-159">In the header, set the following values:</span></span>

    - <span data-ttu-id="36a21-160">**Tööklassi ID:** *QC-kontroll*</span><span class="sxs-lookup"><span data-stu-id="36a21-160">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="36a21-161">Sisestage tööklassi tuvastav nimi.</span><span class="sxs-lookup"><span data-stu-id="36a21-161">Enter a name that identifies the work class.</span></span>

    - <span data-ttu-id="36a21-162">**Kirjeldus:** *QC-kontroll*</span><span class="sxs-lookup"><span data-stu-id="36a21-162">**Description:** *QC Check*</span></span>

        <span data-ttu-id="36a21-163">Sisestage lühikirjeldus, mis näitab, milleks tööklassi kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="36a21-163">Enter a short description that indicates what the work class is used for.</span></span>

    - <span data-ttu-id="36a21-164">**Töökäsu tüüp:** *Kvaliteet kvaliteedikontrollis*</span><span class="sxs-lookup"><span data-stu-id="36a21-164">**Work order type:** *Quality in quality check*</span></span>

        <span data-ttu-id="36a21-165">Valige tööklassi loodud töökäsu tüüp.</span><span class="sxs-lookup"><span data-stu-id="36a21-165">Select the type of work order that is created by the work class.</span></span> <span data-ttu-id="36a21-166">Kui häälestate kvaliteedikontrolli töö, valige alati *Kvaliteet kvaliteedikontrollis*.</span><span class="sxs-lookup"><span data-stu-id="36a21-166">When you set up quality control work, always select *Quality in quality check*.</span></span>

1. <span data-ttu-id="36a21-167">Jätke kiirkaardil **Ladustamise sobivad asukohatüübid** väli **Asukohatüüp** tühjaks.</span><span class="sxs-lookup"><span data-stu-id="36a21-167">On the **Valid put location types** FastTab, leave the **Location type** field blank.</span></span>

    <span data-ttu-id="36a21-168">Kui valite asukohatüübi, piiritlete asukohad, kuhu kaupu saab ladustada pärast komplekteerimist.</span><span class="sxs-lookup"><span data-stu-id="36a21-168">If you select a location type, you limit the locations where items can be put after they are picked.</span></span> <span data-ttu-id="36a21-169">Seda välja kasutatakse, kui asukohakorraldus püüab asukohta lahendada või kui laotöötaja määrab mobiilse seadme menüü-üksuse jaoks asukoha käsitsi.</span><span class="sxs-lookup"><span data-stu-id="36a21-169">This field is used when a location directive tries to resolve the location, or when a warehouse worker manually specifies the location for the mobile device menu item.</span></span>

<span data-ttu-id="36a21-170">Lisateabe saamiseks tööklasside ja nende loomise kohta vt [Tööklassi loomine](tasks/create-work-class.md).</span><span class="sxs-lookup"><span data-stu-id="36a21-170">For more information about work classes and how to create them, see [Create a work class](tasks/create-work-class.md).</span></span>

### <a name="work-template"></a><span data-ttu-id="36a21-171">Töömall</span><span class="sxs-lookup"><span data-stu-id="36a21-171">Work template</span></span>

<span data-ttu-id="36a21-172">Töömallid võimaldavad teil määratleda tööüksuse toimingud, mida tuleb laos teha.</span><span class="sxs-lookup"><span data-stu-id="36a21-172">Work templates let you define the work operations that must be performed in the warehouse.</span></span> <span data-ttu-id="36a21-173">Tavaliselt koosnevad lao tööüksuse toimingud paarist tegevusest: laotöötaja komplekteerib ühes kohas vaba kaubavaru ja viib komplekteeritud kaubavarud teise kohta.</span><span class="sxs-lookup"><span data-stu-id="36a21-173">Typically, warehouse work operations consist of a pair of actions: a warehouse worker picks on-hand inventory up in one location and then puts the picked inventory down in another location.</span></span> <span data-ttu-id="36a21-174">Kvaliteedikontrolli töömall määratleb tööüksuse toimingud kvaliteedikontrolliks.</span><span class="sxs-lookup"><span data-stu-id="36a21-174">A work template for quality control defines the work operations for doing quality checks.</span></span>

#### <a name="purchase-orders"></a><span data-ttu-id="36a21-175">Ostutellimused</span><span class="sxs-lookup"><span data-stu-id="36a21-175">Purchase orders</span></span>

1. <span data-ttu-id="36a21-176">Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.</span><span class="sxs-lookup"><span data-stu-id="36a21-176">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="36a21-177">Seadke päises väli **Töökäsu tüüp** väärtusele *Ostutellimus*.</span><span class="sxs-lookup"><span data-stu-id="36a21-177">In the header, set the **Work order type** field to *Purchase orders*.</span></span>
1. <span data-ttu-id="36a21-178">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="36a21-178">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="36a21-179">Valige töömall, mis peaks sisaldama kvaliteedikontrolli etappi.</span><span class="sxs-lookup"><span data-stu-id="36a21-179">Select a work template that should include a quality check step.</span></span> <span data-ttu-id="36a21-180">Valige jaotise **Ülevaade** väljal **Töömall** suvand *51 Ostutellimuse vastuvõtmine*.</span><span class="sxs-lookup"><span data-stu-id="36a21-180">In the **Overview** section, in the **Work template** field, select *51 PO Receipt*.</span></span>
1. <span data-ttu-id="36a21-181">Märkate, et jaotise **Töömalli üksikasjad** tabelis on kaks olemasolevat rida: üks tegevusele *Komplekteerimine* ja teine tegevusele *Ladustamine*.</span><span class="sxs-lookup"><span data-stu-id="36a21-181">In the **Work template details** section, notice that the grid has two existing lines: one for *Pick* and one for *Put*.</span></span>
1. <span data-ttu-id="36a21-182">Tehke jaotises **Töömalli üksikasjad** valik **Uus** , et lisada tabelisse kvaliteedikontrolli rida.</span><span class="sxs-lookup"><span data-stu-id="36a21-182">In the **Work template details** section, select **New** to add a row for quality control to the grid.</span></span> <span data-ttu-id="36a21-183">Pange tähele, et uue rea välja **Reanumber** väärtuseks on määratud *3*.</span><span class="sxs-lookup"><span data-stu-id="36a21-183">Notice that the **Line number** field for the new line is set to *3*.</span></span>
1. <span data-ttu-id="36a21-184">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-184">On the new line, set the following values.</span></span> <span data-ttu-id="36a21-185">Võtke vastu ülejäänud väljade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-185">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="36a21-186">**Töö tüüp:** *Kvaliteedikontroll*</span><span class="sxs-lookup"><span data-stu-id="36a21-186">**Work type:** *Quality check*</span></span>
    - <span data-ttu-id="36a21-187">**Tööklassi ID:** *Ost*</span><span class="sxs-lookup"><span data-stu-id="36a21-187">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="36a21-188">**Kvaliteedikontrolli malli nimi:** *Laadimissilla kontroll*</span><span class="sxs-lookup"><span data-stu-id="36a21-188">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="36a21-189">Valige tööklassi kordumatu kood.</span><span class="sxs-lookup"><span data-stu-id="36a21-189">Select the unique ID for the work class.</span></span> <span data-ttu-id="36a21-190">Selle väärtuse abil saate konfigureerida mobiilse seadme menüüelemente ja töö tüüpe, mida need menüüelemendid saavad töödelda.</span><span class="sxs-lookup"><span data-stu-id="36a21-190">You use this value to configure the menu items on the mobile device and the types of work that those menu items can process.</span></span>

1. <span data-ttu-id="36a21-191">Oma senise töö salvestamiseks valige tegevuspaanil **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="36a21-191">On the Action Pane, select **Save** to save your work so far.</span></span>

    <span data-ttu-id="36a21-192">Kuvatakse teade, mis ütleb: "Ei sobi – kvaliteedi kontroll peab toimuma kohe pärast komplekteerimist."</span><span class="sxs-lookup"><span data-stu-id="36a21-192">You receive an informational message that states, "Invalid - Quality check must come directly after a pick."</span></span> <span data-ttu-id="36a21-193">Seetõttu peate muutma just lisatud rea **Reanumber** väärtust.</span><span class="sxs-lookup"><span data-stu-id="36a21-193">Therefore, you must change the **Line number** value for the line that you just added.</span></span>

1. <span data-ttu-id="36a21-194">Uue rea **Reanumbri** väärtuse muutmiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="36a21-194">Follow these steps to change the **Line number** value for the new line:</span></span>

    1. <span data-ttu-id="36a21-195">Valige jaotises **Töömalli üksikasjad** rida, milles välja **Töö tüüp** väärtuseks on määratud *Kvaliteedikontroll*.</span><span class="sxs-lookup"><span data-stu-id="36a21-195">In the **Work template details** section, select the line where the **Work type** field is set to *Quality check*.</span></span>
    2. <span data-ttu-id="36a21-196">Valige nupud **Teisalda üles** või **Teisalda alla** , et viia rida *Kvaliteedikontroll* kohta, kus see asub pärast rida *Komplekteerimine*.</span><span class="sxs-lookup"><span data-stu-id="36a21-196">Select the **Move up** or **Move down** button to move the *Quality check* line so that it's after the *Pick* line.</span></span>

1. <span data-ttu-id="36a21-197">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="36a21-197">On the Action Pane, select **Save**.</span></span>

#### <a name="quality-in-quality-check"></a><span data-ttu-id="36a21-198">Kvaliteet kvaliteedikontrollis</span><span class="sxs-lookup"><span data-stu-id="36a21-198">Quality in quality check</span></span>

<span data-ttu-id="36a21-199">Järgmisena looge kvaliteedikontrolli jaoks töömall.</span><span class="sxs-lookup"><span data-stu-id="36a21-199">Next, create a work template for the quality check.</span></span>

1. <span data-ttu-id="36a21-200">Muutke lehe **Töömallid** päises välja **Töökäsu tüüp** väärtuseks *Kvaliteet kvaliteedikontrollis*.</span><span class="sxs-lookup"><span data-stu-id="36a21-200">In the header of the **Work templates** page, change the value of the **Work order type** field to *Quality in quality check*.</span></span>
1. <span data-ttu-id="36a21-201">Valige tegevuspaanil suvand **Uus** , et lisada rida jaotise **Ülevaade** tabelisse.</span><span class="sxs-lookup"><span data-stu-id="36a21-201">On the Action Pane, select **New** to add a row to the grid in the **Overview** section.</span></span>
1. <span data-ttu-id="36a21-202">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-202">In the new row, set the following values:</span></span>

    - <span data-ttu-id="36a21-203">**Töömall:** *51 Kvaliteedikontroll*</span><span class="sxs-lookup"><span data-stu-id="36a21-203">**Work template:** *51 Quality Check*</span></span>

        <span data-ttu-id="36a21-204">Sisestage mallile nimi.</span><span class="sxs-lookup"><span data-stu-id="36a21-204">Enter a name for the template.</span></span>

    - <span data-ttu-id="36a21-205">**Töömalli kirjeldus:** *51 Kvaliteedikontroll*</span><span class="sxs-lookup"><span data-stu-id="36a21-205">**Work template description:** *51 Quality Check*</span></span>

1. <span data-ttu-id="36a21-206">Valige tegevuspaanil **Salvesta** , et muuta jaotis **Töömalli üksikasjad** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="36a21-206">On the Action Pane, select **Save** to make the **Work template details** section available.</span></span>
1. <span data-ttu-id="36a21-207">Kui jaotises **Ülevaade** on uus mall endiselt valitud, tehke jaotises **Töömalli üksikasjad** valik **Uus** ja lisage rida seal olevasse tabelisse.</span><span class="sxs-lookup"><span data-stu-id="36a21-207">While the new template is still selected in the **Overview** section, select **New** in the **Work template details** section to add a row to the grid there.</span></span>
1. <span data-ttu-id="36a21-208">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-208">In the new row, set the following values:</span></span>

    - <span data-ttu-id="36a21-209">**Töö tüüp:** *Komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="36a21-209">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="36a21-210">**Tööklassi ID:** *QC-kontroll*</span><span class="sxs-lookup"><span data-stu-id="36a21-210">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="36a21-211">Valige varem kvaliteedikontrolli jaoks loodud [tööklassi](#work-class) nimi.</span><span class="sxs-lookup"><span data-stu-id="36a21-211">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="36a21-212">Muu rea tabelisse lisamiseks tehke jaotises **Töömalli üksikasjad** uuesti valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="36a21-212">In the **Work template details** section, select **New** again to add another row.</span></span>
1. <span data-ttu-id="36a21-213">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-213">In the new row, set the following values:</span></span>

    - <span data-ttu-id="36a21-214">**Töö tüüp:** *Ladustamine*</span><span class="sxs-lookup"><span data-stu-id="36a21-214">**Work type:** *Put*</span></span>
    - <span data-ttu-id="36a21-215">**Tööklassi ID:** *QC-kontroll*</span><span class="sxs-lookup"><span data-stu-id="36a21-215">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="36a21-216">Valige varem kvaliteedikontrolli jaoks loodud [tööklassi](#work-class) nimi.</span><span class="sxs-lookup"><span data-stu-id="36a21-216">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="36a21-217">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="36a21-217">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="36a21-218">Töömallide kohta lisateabe saamiseks vt [Laotöö juhtimine töömallide ja asukohakorraldustega](control-warehouse-location-directives.md)</span><span class="sxs-lookup"><span data-stu-id="36a21-218">For more information about work templates, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md)</span></span>

### <a name="location-directive--quality-failures"></a><span data-ttu-id="36a21-219">Asukohakorraldus – kvaliteedivead</span><span class="sxs-lookup"><span data-stu-id="36a21-219">Location directive – Quality failures</span></span>

<span data-ttu-id="36a21-220">Asukoha korraldused on reeglid, mis aitavad tuvastada komplekteerimise ja mahapanemise asukohti varude liigutamisel.</span><span class="sxs-lookup"><span data-stu-id="36a21-220">Location directives are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="36a21-221">Näiteks määratleb asukohakorraldus müügitellimuse kandes koha, kus kaubad komplekteeritakse ja kuhu komplekteeritud kaubad maha pannakse.</span><span class="sxs-lookup"><span data-stu-id="36a21-221">For example, in a sales order transaction, a location directive determines where the items will be picked and where the picked items will be put.</span></span> <span data-ttu-id="36a21-222">Peate konfigureerima asukohakorralduse reegli, et määratleda, kuidas nurjunud kvaliteedikontrolli käsitletakse.</span><span class="sxs-lookup"><span data-stu-id="36a21-222">You must configure a location directive rule to define how failed quality checks will be handled.</span></span>

1. <span data-ttu-id="36a21-223">Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.</span><span class="sxs-lookup"><span data-stu-id="36a21-223">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="36a21-224">Seda tüüpi asukohakorraldustega töötamiseks määrake vasakpoolsel paanil välja **Töökäsu tüüp** väärtuseks *Ostutellimused*.</span><span class="sxs-lookup"><span data-stu-id="36a21-224">In the left pane, set the **Work order type** field to *Purchase orders* to work with location directives of that type.</span></span>
1. <span data-ttu-id="36a21-225">Kvaliteedikontrollide asukohakorralduse loomiseks valige tegevuspaanil **Uus**.</span><span class="sxs-lookup"><span data-stu-id="36a21-225">On the Action Pane, select **New** to create a location directive for quality checks.</span></span>
1. <span data-ttu-id="36a21-226">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-226">In the header, set the following values:</span></span>

    - <span data-ttu-id="36a21-227">**Järjekorranumber:** nõustuge vaikeväärtusega.</span><span class="sxs-lookup"><span data-stu-id="36a21-227">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="36a21-228">**Nimi:** *51 Kvaliteedikontrolli*</span><span class="sxs-lookup"><span data-stu-id="36a21-228">**Name:** *51 To Quality*</span></span>

1. <span data-ttu-id="36a21-229">Määrake kiirkaardil **Asukohakorraldused** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-229">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="36a21-230">Võtke vastu ülejäänud väljade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-230">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="36a21-231">**Töö tüüp:** *Ladustamine*</span><span class="sxs-lookup"><span data-stu-id="36a21-231">**Work type:** *Put*</span></span>
    - <span data-ttu-id="36a21-232">**Tegevuskoht:** *5*</span><span class="sxs-lookup"><span data-stu-id="36a21-232">**Site:** *5*</span></span>
    - <span data-ttu-id="36a21-233">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="36a21-233">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="36a21-234">Korralduse salvestamiseks tegevuspaanil valige **Salvesta** ja muutke kiirkaart **Read** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="36a21-234">On the Action Pane select **Save** to save your directive and make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="36a21-235">Valige kiirkaardil **Read** suvand **Uus** , et lisada rida ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="36a21-235">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="36a21-236">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-236">On the new line, set the following values.</span></span> <span data-ttu-id="36a21-237">Võtke vastu ülejäänud väljade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-237">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="36a21-238">**Alates kogusest:** *1*</span><span class="sxs-lookup"><span data-stu-id="36a21-238">**From quantity:** *1*</span></span>
    - <span data-ttu-id="36a21-239">**Koguseni:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="36a21-239">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="36a21-240">Uue rea salvestamiseks ja kiirkaardi **Asukohakorralduse tegevused** kättesaadavaks muutmiseks valige tegevuspaanil **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="36a21-240">On the Action Pane, select **Save** to save the new line and make the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="36a21-241">Kui kiirkaardil **Read** on uus rida endiselt valitud, tehke kiirkaardil **Asukohakorralduse toimingud** valik **Uus** rea sinna lisamiseks tabelis, et saaksite rea jaoks tegevuse häälestada.</span><span class="sxs-lookup"><span data-stu-id="36a21-241">While the new line is still selected on the **Lines** FastTab, select **New** on the **Location directive actions** FastTab to add a row to the grid there, so that you can set up an action for the line.</span></span>
1. <span data-ttu-id="36a21-242">Uues reas määrake välja **Nimi** väärtuseks *Kvaliteet*.</span><span class="sxs-lookup"><span data-stu-id="36a21-242">In the new row, set the **Name** field to *Quality*.</span></span> <span data-ttu-id="36a21-243">Võtke vastu ülejäänud väljade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-243">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="36a21-244">Valige tegevuspaanil **Salvesta** , et muuta kiirkaardi **Asukohakorralduse tegevused** nupp **Redigeeri päringut** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="36a21-244">On the Action Pane, select **Save** to make the **Edit query** button on the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="36a21-245">Kui teie lisatud rida on kiirkaardil **Asukohakorralduse tegevused** endiselt valitud, valige käsk **Redigeeri päringut** , et avada dialoogiboks, kus saate redigeerida tegevuse päringut.</span><span class="sxs-lookup"><span data-stu-id="36a21-245">While the line that you just added is still selected on the **Location directive actions** FastTab, select **Edit query** to open a dialog box where you can edit the query for the action.</span></span>
1. <span data-ttu-id="36a21-246">Vahekaardil **Vahemik** valige käsk **Lisa** , et lisada uus rida päringusse.</span><span class="sxs-lookup"><span data-stu-id="36a21-246">On the **Range** tab, select **Add** to add a row to the query.</span></span>
1. <span data-ttu-id="36a21-247">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-247">In the new row, set the following values:</span></span>

    - <span data-ttu-id="36a21-248">**Tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="36a21-248">**Table:** *Locations*</span></span>
    - <span data-ttu-id="36a21-249">**Tuletatud tabel:** *Asukohad*</span><span class="sxs-lookup"><span data-stu-id="36a21-249">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="36a21-250">**Väli:** *Asukoht*</span><span class="sxs-lookup"><span data-stu-id="36a21-250">**Field:** *Location*</span></span>
    - <span data-ttu-id="36a21-251">**Kriteeriumid:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="36a21-251">**Criteria:** *QMS*</span></span>

    <span data-ttu-id="36a21-252">*QMS* -i asukoht on kvaliteedi laoasukoht.</span><span class="sxs-lookup"><span data-stu-id="36a21-252">The *QMS* location is a warehouse location for quality.</span></span>

1. <span data-ttu-id="36a21-253">Valige dialoogiboksi sulgemiseks suvand **OK**.</span><span class="sxs-lookup"><span data-stu-id="36a21-253">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="36a21-254">Nüüd peate lao *51* jaoks muutma ostutellimuse asukohakorralduste järjestust.</span><span class="sxs-lookup"><span data-stu-id="36a21-254">You must now change the sequence of purchase order location directives for warehouse *51*.</span></span> <span data-ttu-id="36a21-255">Salvestage uus asukohakorraldus *51 kvaliteedikontrolli* , värskendage lehte ja valige loendist asukohakorraldus.</span><span class="sxs-lookup"><span data-stu-id="36a21-255">Save the new *51 To Quality* location directive, refresh the page, and select the location directive in the list.</span></span> <span data-ttu-id="36a21-256">Seejärel kasutage lao *51* asukohakorralduse järgmisesse järjestusse panemiseks tegevuspaanil nuppe **Nihuta üles** ja **Nihuta alla**.</span><span class="sxs-lookup"><span data-stu-id="36a21-256">Then use the **Move up** and **Move down** buttons on the Action Pane to put the location directive for warehouse *51* in the following order.</span></span> <span data-ttu-id="36a21-257">(Enne kui valite **Nihuta üles** või **Nihuta alla** , peate loendis valima asukohakorralduse.)</span><span class="sxs-lookup"><span data-stu-id="36a21-257">(Before you select **Move up** or **Move down** , you must select a location directive in the list.)</span></span>

    1. <span data-ttu-id="36a21-258">51 Kvaliteedikontrolli</span><span class="sxs-lookup"><span data-stu-id="36a21-258">51 To Quality</span></span>
    2. <span data-ttu-id="36a21-259">51 otse-PO</span><span class="sxs-lookup"><span data-stu-id="36a21-259">51 PO Direct</span></span>
    3. <span data-ttu-id="36a21-260">51 QMS</span><span class="sxs-lookup"><span data-stu-id="36a21-260">51 QMS</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="36a21-261">Mobiilse seadme menüü-üksused</span><span class="sxs-lookup"><span data-stu-id="36a21-261">Mobile device menu items</span></span>

<span data-ttu-id="36a21-262">Konfigureerige menüü-üksus, et mobiilsetes seadmetes olek võimalik kasutada funktsiooni **Kvaliteedikontroll**.</span><span class="sxs-lookup"><span data-stu-id="36a21-262">Configure a menu item so that mobile devices can perform the **Quality Check** function.</span></span>

#### <a name="purchase-putaway"></a><span data-ttu-id="36a21-263">Ostu ladustamine</span><span class="sxs-lookup"><span data-stu-id="36a21-263">Purchase putaway</span></span>

1. <span data-ttu-id="36a21-264">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="36a21-264">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="36a21-265">Valige loendist menüü-üksus **Ostu ladustamine**.</span><span class="sxs-lookup"><span data-stu-id="36a21-265">In the list, select the **Purchase put-away** menu item.</span></span>
1. <span data-ttu-id="36a21-266">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="36a21-266">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="36a21-267">Rea tabelisse lisamiseks valige jaotisest **Tööklassid** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="36a21-267">In the **Work classes** section, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="36a21-268">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-268">In the new row, set the following values:</span></span>

    - <span data-ttu-id="36a21-269">**Tööklassi ID:** *QC-kontroll*</span><span class="sxs-lookup"><span data-stu-id="36a21-269">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="36a21-270">Sisestage varem kvaliteedikontrolli jaoks loodud [tööklassi](#work-class) nimi.</span><span class="sxs-lookup"><span data-stu-id="36a21-270">Enter the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

    - <span data-ttu-id="36a21-271">**Töökäsu tüüp:** *Kvaliteet kvaliteedikontrollis*</span><span class="sxs-lookup"><span data-stu-id="36a21-271">**Work order type:** *Quality in quality check*</span></span>

1. <span data-ttu-id="36a21-272">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="36a21-272">On the Action Pane, select **Save**.</span></span>

#### <a name="purchase-order-line-receiving"></a><span data-ttu-id="36a21-273">Vastuvõttev ostutellimuse rida</span><span class="sxs-lookup"><span data-stu-id="36a21-273">Purchase order line receiving</span></span>

1. <span data-ttu-id="36a21-274">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="36a21-274">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="36a21-275">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="36a21-275">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="36a21-276">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-276">In the header, set the following values:</span></span>

    - <span data-ttu-id="36a21-277">**Menüü-üksuse nimi:** *Vastuvõttev ostutellimuse rida*</span><span class="sxs-lookup"><span data-stu-id="36a21-277">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="36a21-278">**Pealkiri:** *Vastuvõttev ostutellimuse rida*</span><span class="sxs-lookup"><span data-stu-id="36a21-278">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="36a21-279">**Režiim:** *töö*</span><span class="sxs-lookup"><span data-stu-id="36a21-279">**Mode:** *Work*</span></span>
    - <span data-ttu-id="36a21-280">**Kasuta olemasolevat tööd:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="36a21-280">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="36a21-281">Määrake kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-281">On the **General** FastTab, set the following values.</span></span> <span data-ttu-id="36a21-282">Võtke vastu ülejäänud väljade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-282">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="36a21-283">**Töö loomise protsess:** *Vastuvõttev ostutellimuse rida ja ladustamine*</span><span class="sxs-lookup"><span data-stu-id="36a21-283">**Work creation process:** *Purchase order line receiving and put away*</span></span>
    - <span data-ttu-id="36a21-284">**Loo litsentsiplaat:** *jah*</span><span class="sxs-lookup"><span data-stu-id="36a21-284">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="36a21-285">**Töömall:** *51 Ostutellimuse vastuvõtmine*</span><span class="sxs-lookup"><span data-stu-id="36a21-285">**Work template:** *51 PO Receipt*</span></span>

1. <span data-ttu-id="36a21-286">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="36a21-286">On the Action Pane, select **Save**.</span></span>

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="36a21-287">Menüü-üksuse lisamine mobiilse seadme menüüsse</span><span class="sxs-lookup"><span data-stu-id="36a21-287">Add the menu item to a mobile device menu</span></span>

1. <span data-ttu-id="36a21-288">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.</span><span class="sxs-lookup"><span data-stu-id="36a21-288">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="36a21-289">Valige vasakul paanil menüü **Sissetulev**.</span><span class="sxs-lookup"><span data-stu-id="36a21-289">In the left pane, select the **Inbound** menu.</span></span>
1. <span data-ttu-id="36a21-290">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="36a21-290">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="36a21-291">Valige veerus **Saadaolevad menüüd ja menüü-üksused** uus menüü-üksus **Vastuvõttev ostutellimuse rida**.</span><span class="sxs-lookup"><span data-stu-id="36a21-291">In the **Available menus and menu items** column, select the new **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="36a21-292">Valige paremnoole nupp, et teisaldada **Vastuvõttev ostutellimuse rida** veergu **Menüü struktuur**.</span><span class="sxs-lookup"><span data-stu-id="36a21-292">Select the right arrow button to move **PO line receiving** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="36a21-293">Tehke veerus **Menüü struktuur** valik **Vastuvõttev ostutellimuse rida** ja seejärel valige menüü-üksuse soovitud kohta viimiseks mobiilse seadme menüüs üles- või allanoolenupp.</span><span class="sxs-lookup"><span data-stu-id="36a21-293">In the **Menu structure** column, select **PO line receiving** , and then select the up arrow or down arrow button to move the menu item to the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="36a21-294">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="36a21-294">On the Action Pane, select **Save**.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="36a21-295">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="36a21-295">Example scenario</span></span>

<span data-ttu-id="36a21-296">Pärast seda, kui olete teinud kõik eelnevalt kirjeldatud näidisandmed kättesaadavaks ja need häälestanud, saate töötada selle stsenaariumi abil, et proovida funktsiooni *Kvaliteedikontroll*.</span><span class="sxs-lookup"><span data-stu-id="36a21-296">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Quality check* feature.</span></span> <span data-ttu-id="36a21-297">Selles stsenaariumis kuvatavad väärtused eeldavad, et töötate standardsete demo andmetega, et valisite juriidilise isiku **USMF** ja olete ette valmistanud näidiskirjed, mida on selles teemas varem kirjeldatud.</span><span class="sxs-lookup"><span data-stu-id="36a21-297">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="36a21-298">See stsenaarium toimib ka näitena selle kohta, kuidas seda funktsiooni saab tootmises kasutada.</span><span class="sxs-lookup"><span data-stu-id="36a21-298">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="36a21-299">Ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="36a21-299">Create a purchase order</span></span>

1. <span data-ttu-id="36a21-300">Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="36a21-300">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="36a21-301">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="36a21-301">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="36a21-302">Dialoogiboksis **Ostutellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-302">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="36a21-303">**Hankija konto:** *104*</span><span class="sxs-lookup"><span data-stu-id="36a21-303">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="36a21-304">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="36a21-304">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="36a21-305">Dialoogiboksi sulgemiseks ja uue müügitellimuse loomiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="36a21-305">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="36a21-306">Kiirkaardil **Müügitellimuse read** sisaldab tabel uut, tühja rida.</span><span class="sxs-lookup"><span data-stu-id="36a21-306">On the **Purchase order lines** FastTab, the grid contains a new, blank line.</span></span> <span data-ttu-id="36a21-307">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="36a21-307">On this line, set the following values:</span></span>

    - <span data-ttu-id="36a21-308">**Kauba kood:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="36a21-308">**Item number:** *M9203*</span></span>
    - <span data-ttu-id="36a21-309">**Kogus:** *3*</span><span class="sxs-lookup"><span data-stu-id="36a21-309">**Quantity:** *3*</span></span>
    - <span data-ttu-id="36a21-310">**Ühik:** *PL*</span><span class="sxs-lookup"><span data-stu-id="36a21-310">**Unit:** *PL*</span></span>

1. <span data-ttu-id="36a21-311">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="36a21-311">On the Action Pane, select **Save**.</span></span>

### <a name="process-quality-check-receiving"></a><span data-ttu-id="36a21-312">Kvaliteedikontrolli vastuvõtmise töötlemine</span><span class="sxs-lookup"><span data-stu-id="36a21-312">Process quality check receiving</span></span>

<span data-ttu-id="36a21-313">Pärast ostutellimuse loomist saab selle vastu võtta, kasutades menüü-üksust **Vastuvõttev ostutellimuse rida** ja funktsiooni *Kvaliteedikontrolli* funktsionaalsust.</span><span class="sxs-lookup"><span data-stu-id="36a21-313">After the purchase order has been created, it can be received by using the **PO line receiving** menu item and the functionality of the *Quality check* feature.</span></span>

#### <a name="receive-pallet-1"></a><span data-ttu-id="36a21-314">Kaubaaluse 1 vastuvõtmine</span><span class="sxs-lookup"><span data-stu-id="36a21-314">Receive pallet 1</span></span>

1. <span data-ttu-id="36a21-315">Logige laorakendusse sisse lao *51* kasutajana.</span><span class="sxs-lookup"><span data-stu-id="36a21-315">Sign in to the warehouse app as a user for warehouse *51*.</span></span> <span data-ttu-id="36a21-316">(Sisestage *51* kasutaja ID-na ja *1* paroolina.)</span><span class="sxs-lookup"><span data-stu-id="36a21-316">(Enter *51* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="36a21-317">Avage **Sissetulev \> Vastuvõttev ostutellimuse rida**.</span><span class="sxs-lookup"><span data-stu-id="36a21-317">Go to **Inbound \> PO line receiving**.</span></span>
1. <span data-ttu-id="36a21-318">Sisestage väljale **PONUM** ostutellimuse number.</span><span class="sxs-lookup"><span data-stu-id="36a21-318">In the **PONUM** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="36a21-319">Kinnitage ostutellimuse number.</span><span class="sxs-lookup"><span data-stu-id="36a21-319">Confirm the purchase order number.</span></span>
1. <span data-ttu-id="36a21-320">Sisestage sissetuleva ostutellimuse rea number väljale **LINENUM**.</span><span class="sxs-lookup"><span data-stu-id="36a21-320">In the **LINENUM** field, enter the number of the purchase order line that is being received.</span></span> <span data-ttu-id="36a21-321">Kuna tellimusel on selles stsenaariumis ainult üks rida, sisestate väljale **LINENUM** iga vastuvõtmisetapi jaoks *1*.</span><span class="sxs-lookup"><span data-stu-id="36a21-321">Because the order has only one line in this scenario, you will enter *1* in the **LINENUM** field for each receiving step.</span></span>
1. <span data-ttu-id="36a21-322">Kinnitage reanumber.</span><span class="sxs-lookup"><span data-stu-id="36a21-322">Confirm the line number.</span></span>
1. <span data-ttu-id="36a21-323">Sisestage vastuvõetav kogus väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="36a21-323">In the **QTY** field, enter the quantity to receive.</span></span> <span data-ttu-id="36a21-324">Kuna selle stsenaariumi ostutellimuses on kolm kaubaalust ( *PL* ) ja vastuvõtu etappe on kolm, sisestate iga vastuvõtuetapi jaoks väljale **Kogus** numbri *1*.</span><span class="sxs-lookup"><span data-stu-id="36a21-324">Because the purchase order is for three pallets ( *PL* ) in this scenario, and there are three receiving steps, you will enter *1* in the **QTY** field for each receiving step.</span></span>
1. <span data-ttu-id="36a21-325">Kinnitage kogus.</span><span class="sxs-lookup"><span data-stu-id="36a21-325">Confirm the quantity.</span></span>

    <span data-ttu-id="36a21-326">Kuvataval lehel **Kvaliteedikontroll** pole sisestusvälju.</span><span class="sxs-lookup"><span data-stu-id="36a21-326">The **Quality check** page that appears has no entry fields.</span></span> <span data-ttu-id="36a21-327">Sellel on allosas ainult kinnituse (märge) nupp ja ülaosas menüünupp ( **≡** ).</span><span class="sxs-lookup"><span data-stu-id="36a21-327">It has only the confirmation (check mark) button at the bottom and the Menu button ( **≡** ) at the top.</span></span> <span data-ttu-id="36a21-328">(Menüünupule on mõnikord viidatud ka kui hamburgerile või hamburgerinupule). Kvaliteedikontrolli protsessi kiirendamiseks, kui kaubaalus läbib kvaliteedikontrolli, kinnitab kasutaja vaid lehe **Kvaliteedikontroll**.</span><span class="sxs-lookup"><span data-stu-id="36a21-328">(The Menu button is sometimes referred to as the hamburger or the hamburger button.) To expedite the quality check process, when the pallet passes the quality check, the user just confirms the **Quality check** page.</span></span>

    <span data-ttu-id="36a21-329">![Kvaliteedikontrolli leht](media/quality-check.png "Kvaliteedikontrolli leht")</span><span class="sxs-lookup"><span data-stu-id="36a21-329">![Quality check page](media/quality-check.png "Quality check page")</span></span>

1. <span data-ttu-id="36a21-330">Kaubaaluse 1 kvaliteedikontrolli läbimiseks valige kinnitusnupp realt 1.</span><span class="sxs-lookup"><span data-stu-id="36a21-330">Select the confirmation button to pass the quality check for pallet 1 from line 1.</span></span>

    <span data-ttu-id="36a21-331">Kuvataval lehel **Ostutellimused: ladustamine** kuvatakse ladustamistöö üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="36a21-331">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="36a21-332">**LOC:** Süsteemi määratud asukoht</span><span class="sxs-lookup"><span data-stu-id="36a21-332">**LOC:** The system determined location</span></span>

        <span data-ttu-id="36a21-333">See asukoht on ostutellimuse jaoks määratud ladustamise asukoht.</span><span class="sxs-lookup"><span data-stu-id="36a21-333">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="36a21-334">**LP:** Süsteemi genereeritud loodud identifitseerimisnumbri ID</span><span class="sxs-lookup"><span data-stu-id="36a21-334">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="36a21-335">**Kaup:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="36a21-335">**Item:** *M9203*</span></span>
    - <span data-ttu-id="36a21-336">**Kogus:** *1 PL: igat toodet 100*</span><span class="sxs-lookup"><span data-stu-id="36a21-336">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="36a21-337">Kuvatakse ka kauba kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="36a21-337">The item description is also shown.</span></span>

1. <span data-ttu-id="36a21-338">Kinnitage ladustamistöö.</span><span class="sxs-lookup"><span data-stu-id="36a21-338">Confirm the putaway work.</span></span>

    <span data-ttu-id="36a21-339">Vastuvõtva ostutellimuse rea lehele **Ülesanne** saate teate "Töö on lõpule viidud".</span><span class="sxs-lookup"><span data-stu-id="36a21-339">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="36a21-340">Väli **LINENUM** on saadaval, et saaksite hakata vastu võtma järgmist kaubaalust.</span><span class="sxs-lookup"><span data-stu-id="36a21-340">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

#### <a name="receive-pallet-2"></a><span data-ttu-id="36a21-341">Kaubaaluse 2 vastuvõtmine</span><span class="sxs-lookup"><span data-stu-id="36a21-341">Receive pallet 2</span></span>

<span data-ttu-id="36a21-342">Selles stsenaariumis lükatakse kaubaalus 2 tagasi.</span><span class="sxs-lookup"><span data-stu-id="36a21-342">For this scenario, pallet 2 will be rejected.</span></span>

1. <span data-ttu-id="36a21-343">Sisestage väljale **LINENUM** arv *1* ja kinnitage reanumber.</span><span class="sxs-lookup"><span data-stu-id="36a21-343">In the **LINENUM** field, enter *1* , and confirm the line number.</span></span>
1. <span data-ttu-id="36a21-344">Väli **Kogus** on nüüd saadaval.</span><span class="sxs-lookup"><span data-stu-id="36a21-344">The **QTY** field is now available.</span></span> <span data-ttu-id="36a21-345">Sisestage *1* ja kinnitage kogus.</span><span class="sxs-lookup"><span data-stu-id="36a21-345">Enter *1* , and confirm the quantity.</span></span>

    <span data-ttu-id="36a21-346">Kuvatakse leht **Kvaliteedikontroll**.</span><span class="sxs-lookup"><span data-stu-id="36a21-346">The **Quality check** page appears.</span></span> <span data-ttu-id="36a21-347">Selle vastuvõtu puhul on kaubaaluse kvaliteet tagasi lükatud ja pannakse kvaliteediasukohta *QMS*.</span><span class="sxs-lookup"><span data-stu-id="36a21-347">For this receipt, the pallet will be rejected for quality, and it will be put into the *QMS* quality location.</span></span>

1. <span data-ttu-id="36a21-348">Valige lehe ülaosas nupp Menüü ( **≡** ) ja seejärel valige menüüs **Lükka tagasi**.</span><span class="sxs-lookup"><span data-stu-id="36a21-348">Select the Menu button ( **≡** ) at the top of the page, and then, on the menu, select **Reject**.</span></span>
1. <span data-ttu-id="36a21-349">Sisestage kuvatavale lehele **Ülesanne** suvand **QMS** asukohana *Ladusta* , et saate kaubaalus täiendavasse kontrolli.</span><span class="sxs-lookup"><span data-stu-id="36a21-349">On the **Task** page that appears, enter **QMS** as the *Put* location to send the pallet to for further inspection.</span></span>

    <span data-ttu-id="36a21-350">Kuvataval lehel **Kvaliteet kvaliteedikontrollis: ladustamine** kuvatakse ladustamistöö üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="36a21-350">The **Quality in quality check: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="36a21-351">**LOC:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="36a21-351">**LOC:** *QMS*</span></span>

        <span data-ttu-id="36a21-352">See asukoht on tagasilükatud ostutellimuse vastuvõetava kauba kvaliteedi tagasilükkamise jaoks määratud ladustamise asukoht.</span><span class="sxs-lookup"><span data-stu-id="36a21-352">This location is the designated putaway location for rejected quality receiving.</span></span>

    - <span data-ttu-id="36a21-353">**LP:** Süsteemi genereeritud loodud identifitseerimisnumbri ID</span><span class="sxs-lookup"><span data-stu-id="36a21-353">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="36a21-354">**Kaup:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="36a21-354">**Item:** *M9203*</span></span>
    - <span data-ttu-id="36a21-355">**Kogus:** *1 PL: igat toodet 100*</span><span class="sxs-lookup"><span data-stu-id="36a21-355">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="36a21-356">Kuvatakse ka kauba kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="36a21-356">The item description is also shown.</span></span>

1. <span data-ttu-id="36a21-357">Kinnitage ladustamistöö.</span><span class="sxs-lookup"><span data-stu-id="36a21-357">Confirm the putaway work.</span></span>

    <span data-ttu-id="36a21-358">Vastuvõtva ostutellimuse rea lehele **Ülesanne** saate teate "Töö on lõpule viidud".</span><span class="sxs-lookup"><span data-stu-id="36a21-358">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="36a21-359">Väli **LINENUM** on saadaval, et saaksite hakata vastu võtma järgmist kaubaalust.</span><span class="sxs-lookup"><span data-stu-id="36a21-359">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

<span data-ttu-id="36a21-360">Olete nüüd kvaliteedikontrolli lõpule viinud ja loonud tagasilükatud kaubaaluse jaoks kvaliteettellimuse.</span><span class="sxs-lookup"><span data-stu-id="36a21-360">You've now completed the quality check and created a quality order for the rejected pallet.</span></span> <span data-ttu-id="36a21-361">Loodud tellimuse vaatamiseks avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Kvaliteettellimused**.</span><span class="sxs-lookup"><span data-stu-id="36a21-361">To view the order that was created, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="36a21-362">Nüüd saab töödelda kvaliteettellimust.</span><span class="sxs-lookup"><span data-stu-id="36a21-362">Quality order testing can now be processed.</span></span> <span data-ttu-id="36a21-363">See teema ei hõlma kvaliteedi testimist.</span><span class="sxs-lookup"><span data-stu-id="36a21-363">Quality testing isn't covered in this topic.</span></span>

<span data-ttu-id="36a21-364">Lisateavet kvaliteedijuhtimise kohta vt [Kvaliteedijuhtimise ülevaade](../inventory/enable-quality-management.md)</span><span class="sxs-lookup"><span data-stu-id="36a21-364">For more information about quality management, see [Quality management overview](../inventory/enable-quality-management.md)</span></span>

#### <a name="receive-pallet-3"></a><span data-ttu-id="36a21-365">Kaubaaluse 3 vastuvõtmine</span><span class="sxs-lookup"><span data-stu-id="36a21-365">Receive pallet 3</span></span>

<span data-ttu-id="36a21-366">Selle stsenaariumi võetakse kaubaalus 3 vastu.</span><span class="sxs-lookup"><span data-stu-id="36a21-366">For this scenario, pallet 3 will be accepted.</span></span>

1. <span data-ttu-id="36a21-367">Sisestage väljale **LINENUM** arv *1* ja kinnitage reanumber.</span><span class="sxs-lookup"><span data-stu-id="36a21-367">In the **LINENUM** field, enter *1* , and confirm the line number.</span></span>
1. <span data-ttu-id="36a21-368">Väli **Kogus** on nüüd saadaval.</span><span class="sxs-lookup"><span data-stu-id="36a21-368">The **QTY** field is now available.</span></span> <span data-ttu-id="36a21-369">Sisestage *1* ja kinnitage kogus.</span><span class="sxs-lookup"><span data-stu-id="36a21-369">Enter *1* , and confirm the quantity.</span></span>

    <span data-ttu-id="36a21-370">Kuvatakse leht **Kvaliteedikontroll**.</span><span class="sxs-lookup"><span data-stu-id="36a21-370">The **Quality check** page appears.</span></span> <span data-ttu-id="36a21-371">Selle kviitungi puhul on kaubaaluse kvaliteet vastu võetud ja see pannakse ladustamise hulgiasukohta.</span><span class="sxs-lookup"><span data-stu-id="36a21-371">For this receipt, the pallet will be accepted for quality, and it will be put into a bulk putaway location.</span></span>

1. <span data-ttu-id="36a21-372">Kvaliteedikontrolli läbimiseks valige kinnitusnupp.</span><span class="sxs-lookup"><span data-stu-id="36a21-372">Select the confirmation button to pass the quality check.</span></span>

    <span data-ttu-id="36a21-373">Kuvataval lehel **Ostutellimused: ladustamine** kuvatakse ladustamistöö üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="36a21-373">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="36a21-374">**LOC:** Süsteemi määratud asukoht</span><span class="sxs-lookup"><span data-stu-id="36a21-374">**LOC:** The system determined location</span></span>

        <span data-ttu-id="36a21-375">See asukoht on ostutellimuse jaoks määratud ladustamise asukoht.</span><span class="sxs-lookup"><span data-stu-id="36a21-375">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="36a21-376">**LP:** Süsteemi genereeritud loodud identifitseerimisnumbri ID</span><span class="sxs-lookup"><span data-stu-id="36a21-376">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="36a21-377">**Kaup:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="36a21-377">**Item:** *M9203*</span></span>
    - <span data-ttu-id="36a21-378">**Kogus:** *1 PL: igat toodet 100*</span><span class="sxs-lookup"><span data-stu-id="36a21-378">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="36a21-379">Kuvatakse ka kauba kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="36a21-379">The item description is also shown.</span></span>

1. <span data-ttu-id="36a21-380">Kinnitage ladustamistöö.</span><span class="sxs-lookup"><span data-stu-id="36a21-380">Confirm the putaway work.</span></span>

    <span data-ttu-id="36a21-381">Vastuvõtva ostutellimuse rea lehele **Ülesanne** saate teate "Töö on lõpule viidud".</span><span class="sxs-lookup"><span data-stu-id="36a21-381">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="36a21-382">Väli **LINENUM** on saadaval, et saaksite hakata vastu võtma järgmist kaubaalust.</span><span class="sxs-lookup"><span data-stu-id="36a21-382">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

1. <span data-ttu-id="36a21-383">Valige lehe ülaosas nupp Menüü ( **≡** ) ja seejärel tehke menüüsse naasmiseks valik **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="36a21-383">Select the Menu button ( **≡** ) at the top of the page, and then, on the menu, select **Cancel** to return to the menu.</span></span>

<span data-ttu-id="36a21-384">Nüüd saate mobiilirakenduse sulgeda.</span><span class="sxs-lookup"><span data-stu-id="36a21-384">You can now close the mobile app.</span></span>
