---
title: Töörea üksikasjad
description: Selles teemas antakse teavet lehe Töörea üksikasjade lehe kohta, mis näitab teie süsteemi üksikute tööridade põhjalikku, sorditavat ja filtreeritavat loendit.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4f0952cc8778ffc509bed80b3a5038dbf4fb76c2
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597188"
---
# <a name="work-line-details"></a><span data-ttu-id="ed9a9-103">Töörea üksikasjad</span><span class="sxs-lookup"><span data-stu-id="ed9a9-103">Work line details</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed9a9-104">Leht **Töörea üksikasjad** näitab teie süsteemi üksikute tööridade põhjalikku, sorditavat ja filtreeritavat loendit.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-104">The **Work line details** page shows a comprehensive, sortable, and filterable list of the individual work lines in your system.</span></span> <span data-ttu-id="ed9a9-105">See annab täieliku ülevaate laos plaanitavast ja teostatud tööst.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-105">It provides a complete overview of work that is being planned and executed in the warehouse.</span></span> <span data-ttu-id="ed9a9-106">Saate hõlpsalt vahetada kõigi tööridade ja ainult avatud tööridade vaatamise vahel.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-106">You can easily switch between viewing all work lines and viewing only open work lines.</span></span> <span data-ttu-id="ed9a9-107">Iga rea kohta esitatud üksikasjad sisaldavad töö olekut, kaubakoodi, asukohta, töö kogust, koorma ID-d ja saadetise ID-d.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-107">Details that are provided for each line include the work status, item number, location, work quantity, load ID, and shipment ID.</span></span>

## <a name="turn-on-the-work-line-details-feature"></a><span data-ttu-id="ed9a9-108">Töörea üksikasjade funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="ed9a9-108">Turn on the work line details feature</span></span>

<span data-ttu-id="ed9a9-109">Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="ed9a9-110">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-110">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="ed9a9-111">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-111">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ed9a9-112">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="ed9a9-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ed9a9-113">**Funktsiooni nimi:** *Töörea üksikasjad*</span><span class="sxs-lookup"><span data-stu-id="ed9a9-113">**Feature name:** *Work line details*</span></span>

## <a name="open-and-use-the-work-line-details-page"></a><span data-ttu-id="ed9a9-114">Töörea üksikasjade lehe avamine ja kasutamine</span><span class="sxs-lookup"><span data-stu-id="ed9a9-114">Open and use the Work line details page</span></span>

<span data-ttu-id="ed9a9-115">Töörea üksikasjade loendi kuvamiseks avage jaotis **Laohaldus \> Töö \> Töörea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-115">To view the list of work line details, go to **Warehouse management \> Work \> Work line details**.</span></span> <span data-ttu-id="ed9a9-116">Siit saate teha järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-116">From here, you can perform the following actions:</span></span>

- <span data-ttu-id="ed9a9-117">Saate kasutada välja **Filter**, et otsida ridu, mille mis tahes saadaoleval parameetril on kindel väärtus.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-117">Use the **Filter** field to search for lines that have a specific value for any available parameter.</span></span> <span data-ttu-id="ed9a9-118">(Saadaolevate parameetrite hulka kuuluvad paljud parameetrid, mida ei kuvata ruudustiku veergudena.)</span><span class="sxs-lookup"><span data-stu-id="ed9a9-118">(Available parameters include many parameters that aren't shown as columns in the grid.)</span></span>
- <span data-ttu-id="ed9a9-119">Suletud ridade kuvamiseks või peitmiseks kasutake märkeruutu **Kuva suletud**.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-119">Use the **Show closed** check box to show or hide closed lines.</span></span>
- <span data-ttu-id="ed9a9-120">Valige **Kuva dimensioonid**, et avada dialoogiboks **Dimensioonide kuvamine**, kus saate valida, kas kuvada või peita ruudustiku erinevaid dimensiooni veergusid.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-120">Select **Display dimensions** to open the **Dimensions display** dialog box, where you can choose to show or hide various dimension columns in the grid.</span></span>
- <span data-ttu-id="ed9a9-121">Valige mis tahes veeru päis menüü avamiseks, kus saate valida, kas sortida või filtreerida loendit selle veeru väärtuste alusel.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-121">Select any column heading to open a menu where you can choose to sort or filter the list by values in that column.</span></span>
- <span data-ttu-id="ed9a9-122">Valige töörida ja seejärel valige **Asukoha muutmine**, et avada dialoogiboks, kus saate muuta selle töörea asukohta.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-122">Select a work line, and then select **Change location** to open a dialog box where you can change the location for that work line.</span></span> <span data-ttu-id="ed9a9-123">Teie määratud asukoht alistab selle asukohakorralduse häälestuse.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-123">The location that you specify will override the setup of the location directive.</span></span>
- <span data-ttu-id="ed9a9-124">Valige töörida ja seejärel valige **Töörea tühistamine**, et avada dialoogiaken, kus saate vähendada selle töörea kogust osaliselt või täielikult.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-124">Select a work line, and then select **Cancel work line** to open a dialog box where you can partially or fully reduce the quantity of that work line.</span></span>
- <span data-ttu-id="ed9a9-125">Korrigeerige koguseid.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-125">Adjust quantities.</span></span>
- <span data-ttu-id="ed9a9-126">Vaadake mis tahes töörea taga olevaid kandeid.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-126">View the transactions behind any work line.</span></span>

## <a name="try-out-the-feature"></a><span data-ttu-id="ed9a9-127">Funktsiooni katsetamine</span><span class="sxs-lookup"><span data-stu-id="ed9a9-127">Try out the feature</span></span>

<span data-ttu-id="ed9a9-128">Sellest jaotisest leiate kolmeosalise demo, mis näitab, kuidas töötada töörea üksikasjadega.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-128">This section provides a three-part demo that shows how to work with work line details.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="ed9a9-129">Näidisandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="ed9a9-129">Make sample data available</span></span>

<span data-ttu-id="ed9a9-130">Selle demo kasutamiseks siin määratud näidiskirjete ja -väärtuste abil peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ed9a9-130">To work through this demo by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="ed9a9-131">Enne alustamist peate valima ka juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-131">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="ed9a9-132">Seda demo saate kasutada ka juhistena, kui töötate tootmissüsteemis.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-132">You can also use this demo as guidance when you work on a production system.</span></span> <span data-ttu-id="ed9a9-133">Kuid peate asendama oma väärtused ja teil ei pruugi olla teatud tüüpi nõutavaid kirjeid, mida pakuvad standardsed demoandmed.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-133">However, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a><span data-ttu-id="ed9a9-134">Veendumine, et stsenaariumi häälestus sisaldaks piisavalt vabu varusid</span><span class="sxs-lookup"><span data-stu-id="ed9a9-134">Verify that the scenario setup includes enough available inventory</span></span>

<span data-ttu-id="ed9a9-135">Kui töötate demoandmetega **USMF**, peaksite esmalt veenduma, et teie süsteem oleks seadistatud nii, et igas vastavas komplekteerimise asukohas oleks saadaval piisavalt varusid.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-135">If you're working with the **USMF** demo data, you should first make sure that your system is set up so that enough inventory is available at each relevant pick location.</span></span> <span data-ttu-id="ed9a9-136">Selle demo puhul on eelduseks, et saadaval oleks järgmised varud.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-136">For this demo, the expectation is that you have the following inventory available:</span></span>

- <span data-ttu-id="ed9a9-137">**Kaup M9200:** 45 ea.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-137">**Item M9200:** 45 ea.</span></span> <span data-ttu-id="ed9a9-138">(või rohkem)</span><span class="sxs-lookup"><span data-stu-id="ed9a9-138">(or more)</span></span>
- <span data-ttu-id="ed9a9-139">**Kaup M9202:** 10 ea.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-139">**Item M9202:** 10 ea.</span></span> <span data-ttu-id="ed9a9-140">(või rohkem)</span><span class="sxs-lookup"><span data-stu-id="ed9a9-140">(or more)</span></span>

<span data-ttu-id="ed9a9-141">Järgige neid etappe, et kontrollida, kas piisavalt varusid on saadaval ja teha vajalikke korrigeerimisi.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-141">Follow these steps to verify that enough inventory is available and to make any adjustments that are required.</span></span>

1. <span data-ttu-id="ed9a9-142">Avage jaotis **Laohaldus \> Häälestus \> Asukohakorraldus** ja määratlege, milliseid komplekteerimise asukohti kasutatakse müügitellimuste komplekteerimiseks laos 51.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-142">Go to **Warehouse management \> Setup \> Location directives**, and determine which picking locations are used for sales order picking at warehouse 51.</span></span> <span data-ttu-id="ed9a9-143">(Lisateavet vaadake teemast [Laotöö juhtimine, kasutades töömalle ja asukohakorraldusi](control-warehouse-location-directives.md).)</span><span class="sxs-lookup"><span data-stu-id="ed9a9-143">(For more information, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md).)</span></span>
1. <span data-ttu-id="ed9a9-144">Kontrollige varude tasemeid vastavates asukohtades.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-144">Check the inventory levels at the relevant locations.</span></span>
1. <span data-ttu-id="ed9a9-145">Korrigeerige varu vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-145">Adjust inventory as required.</span></span> <span data-ttu-id="ed9a9-146">Varude korrigeerimiseks saate luua käsitsi liikumisi, kasutada täiendamist või rakendada mis tahes muud voogu.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-146">You can create manual movements, use replenishment, or apply any other flow to adjust the inventory.</span></span>

### <a name="part-1-create-picking-work"></a><span data-ttu-id="ed9a9-147">1. osa: komplekteerimistöö loomine</span><span class="sxs-lookup"><span data-stu-id="ed9a9-147">Part 1: Create picking work</span></span>

<span data-ttu-id="ed9a9-148">Enne töö loomise alustamist veenduge, et teie ladu on seadistatud nii, et see vastaks töötaotlustele oodatud viisil.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-148">Before you start to create work, make sure that your warehouse is set up to respond to work requests in the expected manner.</span></span>

<span data-ttu-id="ed9a9-149">Komplekteerimistöö loomiseks järgige neid etappe.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-149">Follow these steps to create some picking work.</span></span>

1. <span data-ttu-id="ed9a9-150">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-150">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="ed9a9-151">Valige **Uus**, et avada dialoogiboks **Müügitellimuse loomine**.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-151">Select **New** to open the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="ed9a9-152">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-152">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ed9a9-153">Määrake kiirkaardi **Klient** välja **Kliendi konto** väärtuseks _US-001_.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-153">On the **Customer** FastTab, set the **Customer account** field to _US-001_.</span></span>
    - <span data-ttu-id="ed9a9-154">Määrake kiirkaardi **Üldine** välja **Ladu** väärtuseks _51_.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-154">On the **General** FastTab, set the **Warehouse** field to _51_.</span></span>

1. <span data-ttu-id="ed9a9-155">Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-155">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="ed9a9-156">Teie uus müügitellimus on avatud.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-156">Your new sales order is opened.</span></span> <span data-ttu-id="ed9a9-157">See lisab uue tühja rea ruudustikku **Müügitellimuse read**.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-157">It includes a new, empty row in the **Sales order lines** grid.</span></span> <span data-ttu-id="ed9a9-158">Määrake sellel tellimuse real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-158">On this order line, set the following values:</span></span>

    - <span data-ttu-id="ed9a9-159">**Kauba kood:** _M9200_</span><span class="sxs-lookup"><span data-stu-id="ed9a9-159">**Item number:** _M9200_</span></span>
    - <span data-ttu-id="ed9a9-160">**Kogus:** _20_</span><span class="sxs-lookup"><span data-stu-id="ed9a9-160">**Quantity:** _20_</span></span>
    - <span data-ttu-id="ed9a9-161">**Ühik:** _ea_</span><span class="sxs-lookup"><span data-stu-id="ed9a9-161">**Unit:** _ea_</span></span>

1. <span data-ttu-id="ed9a9-162">Valige uus tellimuserida ja seejärel valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine** lehe **Reserveerimine** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-162">Select the new order line, and then, on the **Inventory** menu, select **Reservation** to open the **Reservation** page.</span></span>
1. <span data-ttu-id="ed9a9-163">Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-163">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="ed9a9-164">Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-164">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="ed9a9-165">Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-165">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span> <span data-ttu-id="ed9a9-166">Süsteem loob saadetise, lisab selle uuele koormusele ja loob vajaliku töö.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-166">The system creates a shipment, adds it to a new load, and creates the required work.</span></span>
1. <span data-ttu-id="ed9a9-167">Looge teine müügitellimus sama kliendi konto ja lao jaoks, mida kasutasite esimese tellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-167">Create a second sales order for the same customer account and warehouse that you used for the first order.</span></span> <span data-ttu-id="ed9a9-168">Lisage sellele tellimusele kaks järgmist tellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-168">Add the following two order lines to this order:</span></span>

    - <span data-ttu-id="ed9a9-169">**Rida 1:** määrake välja **Kaubakood** väärtuseks _M9200_, välja **Kogus** väärtuseks _25_ ja välja **Ühik** väärtuseks _ea_.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-169">**Line 1:** Set the **Item number** field to _M9200_, the **Quantity** field to _25_, and the **Unit** field to _ea_.</span></span>
    - <span data-ttu-id="ed9a9-170">**Rida 2:** määrake välja **Kaubakood** väärtuseks _M9202_, välja **Kogus** väärtuseks _10_ ja välja **Ühik** väärtuseks _ea_.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-170">**Line 2:** Set the **Item number** field to _M9202_, the **Quantity** field to _10_, and the **Unit** field to _ea_.</span></span>

1. <span data-ttu-id="ed9a9-171">Korrake etappe 6–8, et reserveerida varud iga tellimuserea jaoks (ükshaaval) ja seejärel korrake etappi 9 tellimuse vabastamiseks lattu.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-171">Repeat steps 6 through 8 to reserve the inventory for each order line (one at a time), and then repeat step 9 to release the order to the warehouse.</span></span>

### <a name="part-2-change-the-location-for-a-work-line"></a><span data-ttu-id="ed9a9-172">2. osa: töörea asukoha muutmine</span><span class="sxs-lookup"><span data-stu-id="ed9a9-172">Part 2: Change the location for a work line</span></span>

1. <span data-ttu-id="ed9a9-173">Avage jaotis **Laohaldus \> Töö \> Töörea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-173">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="ed9a9-174">Otsige üles ja valige üks selle demo jaoks loodud tööridadest.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-174">Find and select one of the work lines that you created for this demo.</span></span>
1. <span data-ttu-id="ed9a9-175">Valige **Asukoha muutmine** dialoogiboksi **Vali uus asukoht** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-175">Select **Change location** to open the **Select new location** dialog box.</span></span>
1. <span data-ttu-id="ed9a9-176">Valige dialoogiboksi **Vali uus asukoht** väljal **Asukoht** töörea jaoks uus asukoht.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-176">In the **Select new location** dialog box, in the **Location** field, select a new location for the work line.</span></span>
1. <span data-ttu-id="ed9a9-177">Valige **OK**, et rakendada oma muudatus ja sulgeda dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-177">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed9a9-178">Asukohamuudatusi saate esitada ainult juhul, kui uues asukohas on saadaval piisavalt vaba varu (komplekteerimiseks) või kui see läbib asukoha tüübi kinnitamise (ladustamiseks).</span><span class="sxs-lookup"><span data-stu-id="ed9a9-178">You can submit location changes only if the new location has enough inventory available (for a pick), or if it passes location-type validation (for a put).</span></span>

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a><span data-ttu-id="ed9a9-179">3. osa: töörea koguse muutmine või töörea tühistamine</span><span class="sxs-lookup"><span data-stu-id="ed9a9-179">Part 3: Change the quantity of a work line or cancel a work line</span></span>

1. <span data-ttu-id="ed9a9-180">Avage jaotis **Laohaldus \> Töö \> Töörea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-180">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="ed9a9-181">Otsige üles ja valige üks selle demo jaoks loodud tööridadest.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-181">Find and select one of the work lines that you created for this demo.</span></span> <span data-ttu-id="ed9a9-182">Võtke arvesse, et saate tühistada või muuta koguseid ainult nendel tööridadel, kus töö tüüp on _komplekteerimine_.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-182">Note that you can cancel or change quantities only for work lines where the work type is _pick_.</span></span>
1. <span data-ttu-id="ed9a9-183">Valige **Töörea tühistamine** dialoogiboksi **Tühistatav kogus** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-183">Select **Cancel work line** to open the **Quantity to cancel** dialog box.</span></span>
1. <span data-ttu-id="ed9a9-184">Muutke dialoogiboksis **Tühistatav kogus** välja **Kogus** väärtust, et määrata kogus, mis tuleks *lahutada* kogusest, mis on praegu sellele reale määratud.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-184">In the **Quantity to cancel** dialog box, change the value in the **Quantity** field to specify the quantity that should be *subtracted from* the quantity that is currently specified for the line.</span></span> <span data-ttu-id="ed9a9-185">Vaikimisi kuvatakse väljal **Kogus** täielikku kogust.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-185">By default, the **Quantity** field shows the full quantity.</span></span>

    - <span data-ttu-id="ed9a9-186">Kui tühistate täieliku koguse, muudetakse väärtus **Töö olek** olekusse _Tühistatud_, kuid väljal **Töö kogus** kuvatakse jätkuvalt algset väärtust.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-186">If you cancel the full quantity, the **Work status** value will be changed to _Canceled_, but the **Work quantity** field will still show the original value.</span></span>
    - <span data-ttu-id="ed9a9-187">Kui tühistate ainult osa kogusest, värskendatakse välja **Töö kogus**, et see kuvaks uut väärtust, kuid väärtus **Töö olek** ei muutu.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-187">If you cancel just part of the quantity, the **Work quantity** field will be updated to show the new value, but the **Work status** value won't change.</span></span>

1. <span data-ttu-id="ed9a9-188">Valige **OK**, et rakendada oma muudatus ja sulgeda dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-188">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed9a9-189">Kui tühistate ainult osa töörea kogusest, peate eemaldama aegunud koguse ka koormuse realt.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-189">If you cancel just part of the quantity for a work line, you must also remove the obsolete quantity from the load line.</span></span> <span data-ttu-id="ed9a9-190">Vastasel juhul, kui alatarne on õigesti seadistatud, ei saa koormuse rida kinnitada saatmiseks.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-190">Otherwise, unless under-delivery is set up correctly, the load line can't be ship-confirmed.</span></span>
