---
title: Voosildi printimine
description: Selles teemas kirjeldatakse voo sildi printimist ja selgitatakse, kuidas seda seadistada.
author: GarmMSFT
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: fe04b841dbb3bb237de53f74d73f2b3f9162ae6b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840433"
---
# <a name="wave-label-printing"></a><span data-ttu-id="9bab4-103">Voosildi printimine</span><span class="sxs-lookup"><span data-stu-id="9bab4-103">Wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bab4-104">Voo siltide printimine pakub alternatiivset lähenemist siltide printimisele, lisatud on uus vooetapi meetod, mis võimaldab teil luua ja printida silte otse voomallist voo käivitamise ajal.</span><span class="sxs-lookup"><span data-stu-id="9bab4-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="9bab4-105">Seetõttu on sildid saadaval juba enne, kui töötajad käitavad töökäsu mobiilses seadmes.</span><span class="sxs-lookup"><span data-stu-id="9bab4-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="9bab4-106">Töötajad saavad manustada nõutavad sildid komplekteerimise ajal, mitte pärast seda.</span><span class="sxs-lookup"><span data-stu-id="9bab4-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="9bab4-107">Voo siltide printimine kasutab sildipaigutuste loomiseks Zebra programmeerimiskeelt (ZPL).</span><span class="sxs-lookup"><span data-stu-id="9bab4-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="9bab4-108">Sildipaigutus jagatakse kolme ossa (päis, keha ja jalus), et lubada korduva ülesehitusega silte.</span><span class="sxs-lookup"><span data-stu-id="9bab4-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="9bab4-109">Voo siltide mallid ütlevad süsteemile, millist sildipaigutust kasutada.</span><span class="sxs-lookup"><span data-stu-id="9bab4-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="9bab4-110">Kasutajad saavad määrata, millist printerit kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="9bab4-110">Users can specify which printer is used.</span></span> <span data-ttu-id="9bab4-111">Nad võivad printida silte vastavalt vajadusele ka üheaegselt mitmelt printerilt.</span><span class="sxs-lookup"><span data-stu-id="9bab4-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="9bab4-112">Lehel **Voo sildi ajalugu** kuvatakse kirjet kõigist selle seadistuse abil loodud siltidest.</span><span class="sxs-lookup"><span data-stu-id="9bab4-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="9bab4-113">Saate printida ja silte tööpäiste alusel eksemplarhaaval rühmitada, saate printida piirjoonesilte tööpäise kohta, samuti saate printida konteineri sisu silte, juhtumi silte ja muid sarnaseid silte.</span><span class="sxs-lookup"><span data-stu-id="9bab4-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="9bab4-114">See funktsioon ei asenda olemasolevat sildi printimise funktsiooni, mis põhineb dokumendi marsruudi valikul.</span><span class="sxs-lookup"><span data-stu-id="9bab4-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="9bab4-115">Voo sildi printimine pakub järgmisi täiustusi.</span><span class="sxs-lookup"><span data-stu-id="9bab4-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="9bab4-116">Saate printida silte vastavalt ühel tööreal olevale pakkide arvule, kasutamata konteinerisse määramist.</span><span class="sxs-lookup"><span data-stu-id="9bab4-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="9bab4-117">(„Pakk” on ühik, mis on määratud ühiku seeriagrupi ridadele.)</span><span class="sxs-lookup"><span data-stu-id="9bab4-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="9bab4-118">Saate printida mitu erinevat siltide järjestust (nt pakkide, kastide ja kaubaaluste sildid).</span><span class="sxs-lookup"><span data-stu-id="9bab4-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="9bab4-119">Saate kaasata siltide loetelu (nt 1/124, 2/124... 124/124) ja määratleda loetelu vahemiku (nt töörida, koormuse rida või saadetis).</span><span class="sxs-lookup"><span data-stu-id="9bab4-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="9bab4-120">Saate luua ja printida veokirja ID siltidele enne veokirja loomist.</span><span class="sxs-lookup"><span data-stu-id="9bab4-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="9bab4-121">Saate luua iga paki jaoks kordumatu konteineri seeriaviisilise lähetamise koodi (SSCC) ja lisada selle igale sildile.</span><span class="sxs-lookup"><span data-stu-id="9bab4-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="9bab4-122">Saate luua GS1-ga ühilduva numbriseeriad veokirja ID ja SSCC jaoks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="9bab4-123">Saate printida silte uuesti nii mobiilsest seadmest kui ka rikkast kliendist.</span><span class="sxs-lookup"><span data-stu-id="9bab4-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="9bab4-124">Saate tühistada silte (nt kiire komplekteerimise stsenaariumides) ja printida need uuesti.</span><span class="sxs-lookup"><span data-stu-id="9bab4-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="9bab4-125">Voo siltide ajaloo puhastamine.</span><span class="sxs-lookup"><span data-stu-id="9bab4-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="9bab4-126">Dokumendi marsruudi valiku paigutuste täiustuste hulka kuuluvad dokumendi marsruudi valiku paigutused ja voo sildi paigutused.</span><span class="sxs-lookup"><span data-stu-id="9bab4-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="9bab4-127">(Lisateavet vt [Identifitseerimisnumbrite dokumendi marsruudi valiku paigutus](../warehousing/document-routing-layout-for-license-plates.md).)</span><span class="sxs-lookup"><span data-stu-id="9bab4-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="9bab4-128">Need täiustused lihtsustavad pakkide sildistamist enne kaubaalusele paigutamist.</span><span class="sxs-lookup"><span data-stu-id="9bab4-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="9bab4-129">Need on eriti kasulikud ettevõtetele, kes saadavad suurtele jaemüüjatele, mis kinnitavad tellimuse sissetulekuid automaatselt, skannides igat pakki eraldi.</span><span class="sxs-lookup"><span data-stu-id="9bab4-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="9bab4-130">Saate rakendada selles teemas kirjeldatud konfiguratsiooni stsenaariume eraldi või koos, sõltuvalt teie ärivajadustest.</span><span class="sxs-lookup"><span data-stu-id="9bab4-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="9bab4-131">Saate kujundada mitu voo sildi malli, mis töötavad järjekorras (kujutatud stsenaariumis 3).</span><span class="sxs-lookup"><span data-stu-id="9bab4-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="9bab4-132">Saate näiteks kasutada stsenaariumi 1 pakkide siltide printimiseks ja stsenaarium 2 kaubaaluste siltide printimiseks (kui kaubaalused on laos erineva suuruse ja kooslusega).</span><span class="sxs-lookup"><span data-stu-id="9bab4-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="9bab4-133">Voo sildi printimise funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="9bab4-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="9bab4-134">Enne funktsiooni *Voo sildi printimine* kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="9bab4-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="9bab4-135">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="9bab4-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="9bab4-136">Seega on funktsioon loetletud järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="9bab4-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="9bab4-137">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="9bab4-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="9bab4-138">**Funktsiooni nimi:** *Voo sildi printimine*</span><span class="sxs-lookup"><span data-stu-id="9bab4-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="9bab4-139">1. stsenaarium: voo sildi printimine, kus luuakse üks voo silt</span><span class="sxs-lookup"><span data-stu-id="9bab4-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="9bab4-140">Selles stsenaariumis näidatakse, kuidas ettevõte saab printida saadetiste silte suurte jaemüüjate jaoks, mis kinnitavad automaatselt tellimuse sissetulekuid, skannides iga pakki eraldi.</span><span class="sxs-lookup"><span data-stu-id="9bab4-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="9bab4-141">Selles stsenaariumis näidatakse täielikku voogu.</span><span class="sxs-lookup"><span data-stu-id="9bab4-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="9bab4-142">Demoandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="9bab4-142">Make demo data available</span></span>

<span data-ttu-id="9bab4-143">Selle stsenaariumiga töötamiseks peavad teil olema installitud demoandmed ja peate valima juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="9bab4-144">Veenduge, et voo sildi meetod oleks saadaval</span><span class="sxs-lookup"><span data-stu-id="9bab4-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="9bab4-145">Peate tõenäoliselt voo protsessi meetodid uuesti looma, et muuta voo siltide printimise meetod kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="9bab4-146">Avage jaotis **Laohaldus \> Seadistus \> Vood \> Voo protsessi meetodid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="9bab4-147">Kinnitage, et loendis oleks **waveLabelPrinting**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="9bab4-148">Kui seda pole, valige selle lisamiseks toimingupaanil **Meetodite uuesti loomine**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="9bab4-149">Voomalli konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="9bab4-149">Configure a wave template</span></span>

<span data-ttu-id="9bab4-150">Voomallid võimaldavad teil linkida kindlaid voo meetodite eksemplare vastava voo sildi malliga.</span><span class="sxs-lookup"><span data-stu-id="9bab4-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="9bab4-151">Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="9bab4-152">Valige voomall, nt **62 Saadetise vaikemall**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="9bab4-153">Teisaldage kiirkaardil **Meetodid** meetod **Voo sildi printimine** veergu **Valitud meetodid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="9bab4-154">Valige veerus **Valitud meetodid** meetod **Voo sildi printimine** ja määrake selle välja **Vooetapi kood** väärtuseks *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="9bab4-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="9bab4-155">Lisateavet vooetapi koodide kohta leiate teemast [Vooetapi koodid](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9bab4-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="9bab4-156">Voo sildi paigutuse loomine</span><span class="sxs-lookup"><span data-stu-id="9bab4-156">Create a wave label layout</span></span>

<span data-ttu-id="9bab4-157">Sildi paigutus juhib, milline teave sildil prinditakse ja kuidas see on paigutatakse. Siin saate sisestada ZPL-koodi, mis saadetakse printerisse.</span><span class="sxs-lookup"><span data-stu-id="9bab4-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="9bab4-158">Avage jaotis **Laohaldus \> Seadistus \> Dokumendi marsruudi valik \> Voo sildi paigutused**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="9bab4-159">Looge järgmiste sätetega kirje.</span><span class="sxs-lookup"><span data-stu-id="9bab4-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-160">**Sildi paigutuse ID:** *Pakk*</span><span class="sxs-lookup"><span data-stu-id="9bab4-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="9bab4-161">**Kirjeldus:** *Pakk (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="9bab4-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="9bab4-162">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="9bab4-163">Valige toimingupaanil **Voo sildi rea sätted**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="9bab4-164">Kuvatakse leht **Voo sildi rea sätted**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="9bab4-165">Siin saate konfigureerida sildi dünaamilise osa.</span><span class="sxs-lookup"><span data-stu-id="9bab4-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="9bab4-166">Lisage järgmiste sätetega rida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-167">**Rea ID:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="9bab4-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="9bab4-168">**Rea tabeli nimi:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="9bab4-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="9bab4-169">**Rea algpaigutus:** *0*</span><span class="sxs-lookup"><span data-stu-id="9bab4-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="9bab4-170">See väli määratleb vertikaalse paigutuse, kus sildil algab rida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="9bab4-171">**Rea kõrgus:** *0*</span><span class="sxs-lookup"><span data-stu-id="9bab4-171">**Row height:** *0*</span></span>

        <span data-ttu-id="9bab4-172">See väli määratleb iga rea kõrguse (punktides) vastavalt ZPL-standardile.</span><span class="sxs-lookup"><span data-stu-id="9bab4-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="9bab4-173">Rea kõrgus on horisontaalsete siltide puhul positiivne ja vertikaalsete siltide puhul negatiivne.</span><span class="sxs-lookup"><span data-stu-id="9bab4-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="9bab4-174">Kuna selles näites on ainult üks rida, saate väärtuseks seada *0* (null).</span><span class="sxs-lookup"><span data-stu-id="9bab4-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="9bab4-175">**Ridu lehel:** *1*</span><span class="sxs-lookup"><span data-stu-id="9bab4-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="9bab4-176">See väli määratleb ridade arvu, mida saab igale sildile printida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="9bab4-177">See seadistus prindib eraldi ZPL-sildi igale kirjele voo siltide tabelis.</span><span class="sxs-lookup"><span data-stu-id="9bab4-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="9bab4-178">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9bab4-178">Close the page.</span></span>
1. <span data-ttu-id="9bab4-179">Valige Toimingupaanil nupp **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="9bab4-180">Lisage päringuredaktori dialoogiboksis vahekaardile **Vahemik** rida, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="9bab4-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-181">**Tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-182">**Tuletatud tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-183">**Väli:** *Töö tüüp*</span><span class="sxs-lookup"><span data-stu-id="9bab4-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="9bab4-184">**Kriteeriumid:** *Komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="9bab4-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="9bab4-185">See päring tagab, et sildile prinditakse ainult komplekteerimise tüübiga tööread, mitte sisestamise tüübiga tööread.</span><span class="sxs-lookup"><span data-stu-id="9bab4-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="9bab4-186">Kui soovite printida veokirja ID-d, valige vahekaardil **Liitmised** tabel **Tööread** ja liitke sellega tabel **Saadetised**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="9bab4-187">Sulgege päringuredaktori dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="9bab4-188">Kiirkaardil **Printeri teksti paigutuse** on kolm jaotist, kuhu saate kirjutada printeri koodi: **Päise jaotis**, **Keha jaotis** ja **Jaluse jaotis**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="9bab4-189">Sisestage jaotise **Päise jaotis** väljale **Sildi päis** nõutava päise kood.</span><span class="sxs-lookup"><span data-stu-id="9bab4-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="9bab4-190">Näiteks kui kasutate Zebra printereid, saate kasutada järgmist koodi.</span><span class="sxs-lookup"><span data-stu-id="9bab4-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="9bab4-191">Sisestage jaotise **Keha jaotis** väljale **Sildi keha** nõutava keha ZPL-kood.</span><span class="sxs-lookup"><span data-stu-id="9bab4-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="9bab4-192">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="9bab4-192">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="9bab4-193">Sisestage jaotise **Keha jaotis** väljale **Sildi jalus** nõutava jaluse ZPL-kood.</span><span class="sxs-lookup"><span data-stu-id="9bab4-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="9bab4-194">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="9bab4-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="9bab4-195">See häälestus prindib igast sildist ühe eksemplari.</span><span class="sxs-lookup"><span data-stu-id="9bab4-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="9bab4-196">Kui vajate rohkem eksemplare (nt ühte eksemplari kaubaaluse kummalegi poolele), määrake jaluse jaotise **\^PQn** väärtuseks **n** nõutav eksemplaride arv.</span><span class="sxs-lookup"><span data-stu-id="9bab4-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="9bab4-197">Näiteks igast sildist nelja eksemplari printimiseks määrake **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="9bab4-198">Teie silt on nüüd kasutamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="9bab4-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="9bab4-199">Voo sildi tüübi loomine</span><span class="sxs-lookup"><span data-stu-id="9bab4-199">Create a wave label type</span></span>

<span data-ttu-id="9bab4-200">Voo sildi tüüpe kasutatakse voo sildi mallide linkimiseks ühiku seeriagrupi ridade ühikule.</span><span class="sxs-lookup"><span data-stu-id="9bab4-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="9bab4-201">Avage jaotis **Laohaldus \> Seadistus \> Dokumendi marsruudi valik \> Voo sildi tüübid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="9bab4-202">Lisage järgmiste sätetega voo sildi tüüp.</span><span class="sxs-lookup"><span data-stu-id="9bab4-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-203">**Sildi tüüp:** *Pakk*</span><span class="sxs-lookup"><span data-stu-id="9bab4-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="9bab4-204">**Kirjeldus:** *Pakk*</span><span class="sxs-lookup"><span data-stu-id="9bab4-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="9bab4-205">Üksuse seeriagruppide häälestamine</span><span class="sxs-lookup"><span data-stu-id="9bab4-205">Set up unit sequence groups</span></span>

<span data-ttu-id="9bab4-206">Järgmisena seadistage voo sildi tüübile ühiku seeriagrupp.</span><span class="sxs-lookup"><span data-stu-id="9bab4-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="9bab4-207">Avage jaotis **Laohaldus \> Seadistus \> Ladu \> Ühiku seeriagrupid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="9bab4-208">Valige grupp **Ea Kast PL**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="9bab4-209">Määrake rea **Kast** välja **Voo taseme tüüp** väärtuseks *Pakk*.</span><span class="sxs-lookup"><span data-stu-id="9bab4-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="9bab4-210">Voo sildi malli loomine</span><span class="sxs-lookup"><span data-stu-id="9bab4-210">Create a wave label template</span></span>

<span data-ttu-id="9bab4-211">Järgmisena looge voo sildi tüübile voo sildi mall.</span><span class="sxs-lookup"><span data-stu-id="9bab4-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="9bab4-212">Avage jaotis **Laohaldus \> Seadistus \> Dokumendi marsruudi valik \> Voo sildi mallid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="9bab4-213">Lisage voo taseme mall ja seadke päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="9bab4-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="9bab4-214">**Voo malli nimi:** *Paki sildid*</span><span class="sxs-lookup"><span data-stu-id="9bab4-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="9bab4-215">**Kirjeldus:** *Paki sildid*</span><span class="sxs-lookup"><span data-stu-id="9bab4-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="9bab4-216">**Vooetapi kood:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="9bab4-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="9bab4-217">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="9bab4-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="9bab4-218">Määrake kiirkaardi **Üldine** välja **Voo sildi tüüp** väärtuseks *Pakk*.</span><span class="sxs-lookup"><span data-stu-id="9bab4-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="9bab4-219">Lisage kiirkaardil **Voo sildi malli üksikasjad** uus rida, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="9bab4-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-220">**Sildi paigutuse ID:** *Pakk*</span><span class="sxs-lookup"><span data-stu-id="9bab4-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="9bab4-221">**Printeri nimi:** valige sobiv ZPL-printer.</span><span class="sxs-lookup"><span data-stu-id="9bab4-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="9bab4-222">**Käivita päring:** *Jah* (see säte on valikuline, kuid see on optimaalse jõudluse tagamiseks soovitatav.)</span><span class="sxs-lookup"><span data-stu-id="9bab4-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="9bab4-223">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="9bab4-224">Valikuline: kui seadistate kliendipõhist sildi kujundust, tuleb teil luua päring kliendi konto leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="9bab4-225">Valige kiirkaardil **Voo sildi malli üksikasjad** suvand **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="9bab4-226">Seejärel lisage päringuredaktori dialoogiboksis vahekaardile **Vahemik** rida, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="9bab4-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-227">**Tabel:** *Saadetised*</span><span class="sxs-lookup"><span data-stu-id="9bab4-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="9bab4-228">**Tuletatud tabel:** *Saadetised*</span><span class="sxs-lookup"><span data-stu-id="9bab4-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="9bab4-229">**Väli:** *Kontonumber*</span><span class="sxs-lookup"><span data-stu-id="9bab4-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="9bab4-230">**Kriteeriumid:** sisestage vastava kliendi kontonumber.</span><span class="sxs-lookup"><span data-stu-id="9bab4-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="9bab4-231">Kui olete lõpetanud, valige päringuredaktori dialoogiboksi sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="9bab4-232">Valige toimingupaanil suvand **Päringu redigeerimine**, et avada terve sildi malli päringuredaktori dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="9bab4-233">Lisage päringuredaktori dialoogiboksis vahekaardile **Sortimine** rida, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="9bab4-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-234">**Tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-235">**Tuletatud tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-236">**Väli:** *Koormuse viiterea ID (kirje-ID)*</span><span class="sxs-lookup"><span data-stu-id="9bab4-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="9bab4-237">**Otsingusuund:** *Kasvav*</span><span class="sxs-lookup"><span data-stu-id="9bab4-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="9bab4-238">Päringuredaktori dialoogiboksi sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="9bab4-239">Teateaken palub teil rühmitamise lähtestamise toimingu kinnitada.</span><span class="sxs-lookup"><span data-stu-id="9bab4-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="9bab4-240">Jätkamiseks valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="9bab4-241">Valige toimingupaanil **Voo sildi malligrupp**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="9bab4-242">Valige dialoogiboksis **Voo sildi malligrupp** rida, kus välja **Viitevälja nimi** väärtuseks on seatud *Viite koormuse rea ID* ja seejärel märkige sellel real ruut **Sildi kooste ID**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id*, and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9bab4-243">See häälestus loob ühe sildi järjestuse („Pakk 1/X”) koormuse rea kohta kogu voos, sõltumata töö rühmitamise seadistusest.</span><span class="sxs-lookup"><span data-stu-id="9bab4-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="9bab4-244">Seda sildi järjestust saab printida sildi paigutusele.</span><span class="sxs-lookup"><span data-stu-id="9bab4-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="9bab4-245">Numbriseeria laienduste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="9bab4-245">Configure number sequence extensions</span></span>

<span data-ttu-id="9bab4-246">Numbriseeria laiendused juhivad konkreetsete numbriseeriate GS1 vastavust.</span><span class="sxs-lookup"><span data-stu-id="9bab4-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="9bab4-247">See konfiguratsioon on praeguse stsenaariumi puhul valikuline.</span><span class="sxs-lookup"><span data-stu-id="9bab4-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="9bab4-248">Lisateavet ja konfigureerimise juhiseid leiate teemast [Numbriseeria laienduste konfigureerimine](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="9bab4-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="9bab4-249">Müügitellimuse loomine ja selle väljastamine lattu</span><span class="sxs-lookup"><span data-stu-id="9bab4-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="9bab4-250">Avage jaotis **Müük ja turundus \> Müügitellimus \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="9bab4-251">Looge järgmiste sätetega müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-252">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9bab4-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9bab4-253">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="9bab4-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="9bab4-254">Lisage kaks müügitellimuse rida, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="9bab4-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="9bab4-255">Müügitellimuse rida 1:</span><span class="sxs-lookup"><span data-stu-id="9bab4-255">Sales order line 1:</span></span>

        - <span data-ttu-id="9bab4-256">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="9bab4-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="9bab4-257">**Kogus:** *9024*</span><span class="sxs-lookup"><span data-stu-id="9bab4-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="9bab4-258">**Ühik:** *ea* (9024 ea = 376 kasti = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="9bab4-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="9bab4-259">Müügitellimuse rida 2:</span><span class="sxs-lookup"><span data-stu-id="9bab4-259">Sales order line 2:</span></span>

        - <span data-ttu-id="9bab4-260">**Kauba kood:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="9bab4-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="9bab4-261">**Kogus:** *9016*</span><span class="sxs-lookup"><span data-stu-id="9bab4-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="9bab4-262">**Ühik:** *ea* (9016 ea = 322 kasti = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="9bab4-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="9bab4-263">Siin esitatud kaubad ja kogused on ainult näited.</span><span class="sxs-lookup"><span data-stu-id="9bab4-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="9bab4-264">Need peavad kasutama ühiku seeriagruppi, mille eelnevalt määratlesite, neile tuleb määratleda vastav ühiku teisendamine ühikult *ea* ühikule *Kast* ühikule *PL* ja neil peab olema kaubavarusid laos *62*.</span><span class="sxs-lookup"><span data-stu-id="9bab4-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="9bab4-265">Lisateavet leiate teemast [Mõõtühik ja varude poliitika](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="9bab4-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="9bab4-266">Valige müügitellimuse rida 1.</span><span class="sxs-lookup"><span data-stu-id="9bab4-266">Select sales order line 1.</span></span> <span data-ttu-id="9bab4-267">Seejärel valige menüü **Varud** jaotisest **Müügitellimuse rida** suvand **Reserveerimised**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="9bab4-268">Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii** ja seejärel sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9bab4-268">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="9bab4-269">Korrake etappe 4 ja 5 müügitellimuse rea 2 puhul.</span><span class="sxs-lookup"><span data-stu-id="9bab4-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="9bab4-270">Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="9bab4-271">Toimub järgmine:</span><span class="sxs-lookup"><span data-stu-id="9bab4-271">The following events occur:</span></span>

    - <span data-ttu-id="9bab4-272">Süsteem töötleb loodud saadetist, kasutades malli, mis sisaldab sildi printimise etappi.</span><span class="sxs-lookup"><span data-stu-id="9bab4-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="9bab4-273">Sildi paigutust kasutatakse sildi vormingu määratlemiseks ja tulemuseks on silt, mis prinditakse sildi mallis valitud printeriga.</span><span class="sxs-lookup"><span data-stu-id="9bab4-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="9bab4-274">Voo sildid luuakse ja prinditakse.</span><span class="sxs-lookup"><span data-stu-id="9bab4-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="9bab4-275">Siltide arv on võrdne pakkide arvuga (selles näites on 376 kasti silti rea 1 ja 322 kasti silti rea 2 jaoks).</span><span class="sxs-lookup"><span data-stu-id="9bab4-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="9bab4-276">Saadetistele luuakse uus veokirja ID.</span><span class="sxs-lookup"><span data-stu-id="9bab4-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="9bab4-277">Kui konfigureerisite numbriseeria laiendused, järgib voo sildi ID numbrivormingut **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="9bab4-278">Saate kuvada ja uuesti printida järgmiste lehtede voo silte.</span><span class="sxs-lookup"><span data-stu-id="9bab4-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="9bab4-279">Valige iga lehe toimingupaani vahekaardil **Saadetised** grupis **Seotud teave** suvand **Voo sildid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="9bab4-280">Kõik saadetised \> Saadetise üksikasjad</span><span class="sxs-lookup"><span data-stu-id="9bab4-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="9bab4-281">Kõik koormused \> Koormuse üksikasjad</span><span class="sxs-lookup"><span data-stu-id="9bab4-281">All loads \> Load details</span></span>
- <span data-ttu-id="9bab4-282">Kõik vood</span><span class="sxs-lookup"><span data-stu-id="9bab4-282">All waves</span></span>
- <span data-ttu-id="9bab4-283">Voo sildid</span><span class="sxs-lookup"><span data-stu-id="9bab4-283">Wave labels</span></span>
- <span data-ttu-id="9bab4-284">Voosildi ajalugu</span><span class="sxs-lookup"><span data-stu-id="9bab4-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="9bab4-285">2. stsenaarium: voo siltide printimine konteinerisse määramiseks (voo sildi kirjeteta)</span><span class="sxs-lookup"><span data-stu-id="9bab4-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="9bab4-286">See stsenaarium võimaldab teil printida voo silte, kui kasutate konteineritesse määramist, et jaotada kaubad automaatselt kastidesse ja seetõttu ei vaja voo sildi kirjet.</span><span class="sxs-lookup"><span data-stu-id="9bab4-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="9bab4-287">Sel juhul toimib konteineri ID SSCC-kohatäitena.</span><span class="sxs-lookup"><span data-stu-id="9bab4-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="9bab4-288">Selle ja 1. stsenaariumi peamised erinevused on järgmised.</span><span class="sxs-lookup"><span data-stu-id="9bab4-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="9bab4-289">**Voo sildi mallid:** te ei vali voo sildi tüüpi voo sildi mallis ja te ei vaja sildi kooste rühmitamist.</span><span class="sxs-lookup"><span data-stu-id="9bab4-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="9bab4-290">Vastasel juhul konfigureerite voo sildi malli ja lingite voo malliga samamoodi, nagu on kirjeldatud stsenaariumis 1.</span><span class="sxs-lookup"><span data-stu-id="9bab4-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="9bab4-291">Peate jätma voo sildi tüübi tühjaks, et voo silte ei loodaks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="9bab4-292">**Voo siltide paigutused:** konfigureerite voo sildi paigutuse rea sätted tööridade jaoks, mitte voo sildi kirjed.</span><span class="sxs-lookup"><span data-stu-id="9bab4-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="9bab4-293">Peate konfigureerima rea sätte sildi paigutuse jaoks, kasutades tabelit **WHSWorkLine** tabeli **WHSWaveLabel** asemel.</span><span class="sxs-lookup"><span data-stu-id="9bab4-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="9bab4-294">Säte **Ridade arv lehekülje kohta** reguleerib ridade arvu, mis on keha jaotises.</span><span class="sxs-lookup"><span data-stu-id="9bab4-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="9bab4-295">See konfiguratsioon sobib ka äristsenaariumide jaoks, kus mitu erinevat kaupa pakitakse ühte sildistatud kasti või kaubaalusele ja seda pakkimise protsessi saab määratleda töö loomisel (näiteks töö, mis on grupeeritud saadetisega).</span><span class="sxs-lookup"><span data-stu-id="9bab4-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="9bab4-296">Selles stsenaariumis näidatakse täielikku voogu.</span><span class="sxs-lookup"><span data-stu-id="9bab4-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="9bab4-297">Demoandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="9bab4-297">Make demo data available</span></span>

<span data-ttu-id="9bab4-298">Selle stsenaariumiga töötamiseks peavad teil olema installitud demoandmed ja peate valima juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="9bab4-299">Veenduge, et voo sildi meetod oleks saadaval</span><span class="sxs-lookup"><span data-stu-id="9bab4-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="9bab4-300">Peate tõenäoliselt voo protsessi meetodid uuesti looma, et muuta voo siltide printimise meetod kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="9bab4-301">Avage jaotis **Laohaldus \> Seadistus \> Vood \> Voo protsessi meetodid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="9bab4-302">Kinnitage, et loendis oleks **waveLabelPrinting**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="9bab4-303">Kui seda pole, valige selle lisamiseks toimingupaanil **Meetodite uuesti loomine**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="9bab4-304">Voomalli seadistamine</span><span class="sxs-lookup"><span data-stu-id="9bab4-304">Set up a wave template</span></span>

<span data-ttu-id="9bab4-305">Voomallid võimaldavad teil linkida kindlaid voo meetodite eksemplare vastava voo sildi malliga.</span><span class="sxs-lookup"><span data-stu-id="9bab4-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="9bab4-306">Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="9bab4-307">Valige voomall, nt **63 konteinerisse määramine**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="9bab4-308">Teisaldage kiirkaardil **Meetodid** meetod **Voo sildi printimine** veergu **Valitud meetodid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="9bab4-309">Valige veerus **Valitud meetodid** meetod **Voo sildi printimine** ja määrake selle välja **Vooetapi kood** väärtuseks *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="9bab4-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="9bab4-310">Lisateavet vooetapi koodide kohta leiate teemast [Vooetapi koodid](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9bab4-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="9bab4-311">Voo sildi paigutuse loomine</span><span class="sxs-lookup"><span data-stu-id="9bab4-311">Create a wave label layout</span></span>

1. <span data-ttu-id="9bab4-312">Avage jaotis **Laohaldus \> Seadistus \> Dokumendi marsruudi valik \> Voo sildi paigutused**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="9bab4-313">Looge järgmiste sätetega kirje.</span><span class="sxs-lookup"><span data-stu-id="9bab4-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-314">**Sildi paigutuse ID:** *Pakk*</span><span class="sxs-lookup"><span data-stu-id="9bab4-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="9bab4-315">**Kirjeldus:** *Pakk (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="9bab4-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="9bab4-316">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="9bab4-317">Valige toimingupaanil **Voo sildi rea sätted**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="9bab4-318">Kuvatakse leht **Voo sildi rea sätted**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="9bab4-319">Siin saate konfigureerida sildi dünaamilise osa.</span><span class="sxs-lookup"><span data-stu-id="9bab4-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="9bab4-320">Lisage järgmiste sätetega rida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-321">**Rea ID:** *WorkLine*</span><span class="sxs-lookup"><span data-stu-id="9bab4-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="9bab4-322">**Rea tabeli nimi:** *WHSWorkLine*</span><span class="sxs-lookup"><span data-stu-id="9bab4-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="9bab4-323">**Rea algpaigutus:** *500*</span><span class="sxs-lookup"><span data-stu-id="9bab4-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="9bab4-324">See väli määratleb vertikaalse paigutuse, kus sildil algab rida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="9bab4-325">**Rea kõrgus:** *–50*</span><span class="sxs-lookup"><span data-stu-id="9bab4-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="9bab4-326">See väli määratleb iga rea kõrguse.</span><span class="sxs-lookup"><span data-stu-id="9bab4-326">This field defines the height of each row.</span></span> <span data-ttu-id="9bab4-327">Rea kõrgus on horisontaalsete siltide puhul positiivne ja vertikaalsete siltide puhul negatiivne.</span><span class="sxs-lookup"><span data-stu-id="9bab4-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="9bab4-328">**Ridu lehel:** *5*</span><span class="sxs-lookup"><span data-stu-id="9bab4-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="9bab4-329">See väli määratleb ridade arvu, mida saab igale sildile printida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="9bab4-330">See seadistus prindib mitu ZPL-silti töö kohta, kus igal lehel võib olla kuni viis töörida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="9bab4-331">Näiteks kui silt prinditakse konteinerile, millel on 12 rida, prinditakse kolm silti.</span><span class="sxs-lookup"><span data-stu-id="9bab4-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="9bab4-332">Kui soovite printida iga komplekteerimise rea kohta eraldi sildi, seadke väärtuseks *1*.</span><span class="sxs-lookup"><span data-stu-id="9bab4-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="9bab4-333">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9bab4-333">Close the page.</span></span>
1. <span data-ttu-id="9bab4-334">Valige Toimingupaanil nupp **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="9bab4-335">Lisage päringuredaktori dialoogiboksis vahekaardile **Vahemik** rida, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="9bab4-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-336">**Tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-337">**Tuletatud tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-338">**Väli:** *Töö tüüp*</span><span class="sxs-lookup"><span data-stu-id="9bab4-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="9bab4-339">**Kriteeriumid:** *Komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="9bab4-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="9bab4-340">Kui soovite printida veokirja ID-d, valige vahekaardil **Liitmised** tabel **Tööread** ja liitke sellega tabel **Saadetised**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="9bab4-341">Sulgege päringuredaktori dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="9bab4-342">Kiirkaardil **Printeri teksti paigutuse** on kolm jaotist, kuhu saate kirjutada printeri koodi: **Päise jaotis**, **Keha jaotis** ja **Jaluse jaotis**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="9bab4-343">Sisestage jaotise **Päise jaotis** väljale **Sildi päis** nõutava päise kood.</span><span class="sxs-lookup"><span data-stu-id="9bab4-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="9bab4-344">Näiteks kui kasutate Zebra printereid, saate kasutada järgmist koodi.</span><span class="sxs-lookup"><span data-stu-id="9bab4-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="9bab4-345">Sisestage jaotise **Keha jaotis** väljale **Sildi keha** nõutava keha ZPL-kood.</span><span class="sxs-lookup"><span data-stu-id="9bab4-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="9bab4-346">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="9bab4-346">Here is an example.</span></span>

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="9bab4-347">Sisestage jaotise **Keha jaotis** väljale **Sildi jalus** nõutava jaluse ZPL-kood.</span><span class="sxs-lookup"><span data-stu-id="9bab4-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="9bab4-348">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="9bab4-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="9bab4-349">See häälestus prindib igast sildist ühe eksemplari.</span><span class="sxs-lookup"><span data-stu-id="9bab4-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="9bab4-350">Kui vajate rohkem eksemplare (nt ühte eksemplari kaubaaluse kummalegi poolele), määrake jaluse jaotise **\^PQn** väärtuseks **n** nõutav eksemplaride arv.</span><span class="sxs-lookup"><span data-stu-id="9bab4-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="9bab4-351">Näiteks igast sildist nelja eksemplari printimiseks määrake **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="9bab4-352">Teie silt on nüüd kasutamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="9bab4-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="9bab4-353">Voo sildi malli loomine</span><span class="sxs-lookup"><span data-stu-id="9bab4-353">Create a wave label template</span></span>

1. <span data-ttu-id="9bab4-354">Avage jaotis **Laohaldus \> Seadistus \> Dokumendi marsruudi valik \> Voo sildi mallid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="9bab4-355">Lisage voo taseme mall ja seadke päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="9bab4-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="9bab4-356">**Voo malli nimi:** *Konteineri sildid*</span><span class="sxs-lookup"><span data-stu-id="9bab4-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="9bab4-357">**Kirjeldus:** *Konteineri sildid*</span><span class="sxs-lookup"><span data-stu-id="9bab4-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="9bab4-358">**Vooetapi kood:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="9bab4-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="9bab4-359">**Ladu:** *63*</span><span class="sxs-lookup"><span data-stu-id="9bab4-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="9bab4-360">Lisage kiirkaardil **Voo sildi malli üksikasjad** rida, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="9bab4-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-361">**Sildi paigutuse ID:** *Konteiner*</span><span class="sxs-lookup"><span data-stu-id="9bab4-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="9bab4-362">**Printeri nimi:** valige sobiv ZPL-printer.</span><span class="sxs-lookup"><span data-stu-id="9bab4-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="9bab4-363">**Käivita päring:** *Jah* (see säte on valikuline, kuid see on optimaalse jõudluse tagamiseks soovitatav.)</span><span class="sxs-lookup"><span data-stu-id="9bab4-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="9bab4-364">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="9bab4-365">Valikuline: kui seadistate kliendipõhist sildi kujundust, tuleb teil luua päring kliendi konto leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="9bab4-366">Valige kiirkaardil **Voo sildi malli üksikasjad** suvand **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="9bab4-367">Seejärel lisage päringuredaktori dialoogiboksis vahekaardile **Vahemik** rida, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="9bab4-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-368">**Tabel:** *Saadetised*</span><span class="sxs-lookup"><span data-stu-id="9bab4-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="9bab4-369">**Tuletatud tabel:** *Saadetised*</span><span class="sxs-lookup"><span data-stu-id="9bab4-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="9bab4-370">**Väli:** *Kontonumber*</span><span class="sxs-lookup"><span data-stu-id="9bab4-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="9bab4-371">**Kriteeriumid:** sisestage vastava kliendi kontonumber.</span><span class="sxs-lookup"><span data-stu-id="9bab4-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="9bab4-372">Kui olete lõpetanud, valige päringuredaktori dialoogiboksi sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="9bab4-373">Numbriseeria laienduste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="9bab4-373">Configure number sequence extensions</span></span>

<span data-ttu-id="9bab4-374">Numbriseeria laiendused juhivad konkreetsete numbriseeriate GS1 vastavust.</span><span class="sxs-lookup"><span data-stu-id="9bab4-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="9bab4-375">See konfiguratsioon on praeguse stsenaariumi puhul valikuline.</span><span class="sxs-lookup"><span data-stu-id="9bab4-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="9bab4-376">Lisateavet ja konfigureerimise juhiseid leiate teemast [Numbriseeria laienduste konfigureerimine](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="9bab4-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="9bab4-377">Müügitellimuse loomine ja selle väljastamine lattu</span><span class="sxs-lookup"><span data-stu-id="9bab4-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="9bab4-378">Avage jaotis **Müük ja turundus \> Müügitellimus \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="9bab4-379">Looge järgmiste sätetega müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-380">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9bab4-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9bab4-381">**Ladu:** *63*</span><span class="sxs-lookup"><span data-stu-id="9bab4-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="9bab4-382">Lisage viis müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="9bab4-383">Müügitellimuse rida 1:</span><span class="sxs-lookup"><span data-stu-id="9bab4-383">Sales order line 1:</span></span>

        - <span data-ttu-id="9bab4-384">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="9bab4-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="9bab4-385">**Kogus:** *10*</span><span class="sxs-lookup"><span data-stu-id="9bab4-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="9bab4-386">Müügitellimuse rida 2:</span><span class="sxs-lookup"><span data-stu-id="9bab4-386">Sales order line 2:</span></span>

        - <span data-ttu-id="9bab4-387">**Kauba kood:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="9bab4-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="9bab4-388">**Kogus:** *20*</span><span class="sxs-lookup"><span data-stu-id="9bab4-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="9bab4-389">Müügitellimuse rida 3:</span><span class="sxs-lookup"><span data-stu-id="9bab4-389">Sales order line 3:</span></span>

        - <span data-ttu-id="9bab4-390">**Kauba kood:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="9bab4-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="9bab4-391">**Kogus:** *20*</span><span class="sxs-lookup"><span data-stu-id="9bab4-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="9bab4-392">Müügitellimuse rida 4:</span><span class="sxs-lookup"><span data-stu-id="9bab4-392">Sales order line 4:</span></span>

        - <span data-ttu-id="9bab4-393">**Kauba kood:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="9bab4-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="9bab4-394">**Kogus:** *40*</span><span class="sxs-lookup"><span data-stu-id="9bab4-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="9bab4-395">Müügitellimuse rida 5:</span><span class="sxs-lookup"><span data-stu-id="9bab4-395">Sales order line 5:</span></span>

        - <span data-ttu-id="9bab4-396">**Kauba kood:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="9bab4-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="9bab4-397">**Kogus:** *50*</span><span class="sxs-lookup"><span data-stu-id="9bab4-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="9bab4-398">Siin esitatud kaubad ja kogused on ainult näited.</span><span class="sxs-lookup"><span data-stu-id="9bab4-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="9bab4-399">Neil peab olema laovaru määratud laos.</span><span class="sxs-lookup"><span data-stu-id="9bab4-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="9bab4-400">Valige müügitellimuse rida 1.</span><span class="sxs-lookup"><span data-stu-id="9bab4-400">Select sales order line 1.</span></span> <span data-ttu-id="9bab4-401">Seejärel valige menüü **Varud** jaotisest **Müügitellimuse rida** suvand **Reserveerimised**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="9bab4-402">Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii** ja seejärel sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9bab4-402">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="9bab4-403">Korrake etappe 4 ja 5 iga täiendava müügitellimuse rea.</span><span class="sxs-lookup"><span data-stu-id="9bab4-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="9bab4-404">Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="9bab4-405">Toimub järgmine:</span><span class="sxs-lookup"><span data-stu-id="9bab4-405">The following events occur:</span></span>

    - <span data-ttu-id="9bab4-406">Süsteem töötleb loodud saadetist, kasutades malli, mis sisaldab sildi printimise etappi.</span><span class="sxs-lookup"><span data-stu-id="9bab4-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="9bab4-407">Sildi paigutust kasutatakse sildi vormingu määratlemiseks ja lõpptulemuseks on silt, millel on viis rida ja mis prinditakse sildi mallis valitud printeriga.</span><span class="sxs-lookup"><span data-stu-id="9bab4-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="9bab4-408">Saadetistele luuakse uus veokirja ID.</span><span class="sxs-lookup"><span data-stu-id="9bab4-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="9bab4-409">Kui konfigureerisite numbriseeria laiendused, järgib voo sildi ID numbrivormingut **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="9bab4-410">Saate need voo sildid uuesti printida, avades jaotise **Laohaldus \> Päringud ja aruanded \> Laine sildi ajalugu**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="9bab4-411">3. stsenaarium: voo sildi printimine mitmeastmeliste siltide puhul</span><span class="sxs-lookup"><span data-stu-id="9bab4-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="9bab4-412">Selles stsenaariumis näidatakse, kuidas kasutada voo siltide printimise funktsiooni, kui ladustamisprotsessid nõuavad mitmeastmelisi saadetise silte.</span><span class="sxs-lookup"><span data-stu-id="9bab4-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="9bab4-413">Näiteks võib olla vaja printida eraldi sildid pakkide ja kaubaaluste jaoks ning piirjoonesilt terve saadetise jaoks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="9bab4-414">Piirjoonesildid on siltide eritüüp, mida saab kasutada rullide ja konteinerite eraldajana, nt sildid saadetise ID ja vöötkoodi jaoks, et silte saaks pärast printimist hõlpsasti sortida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="9bab4-415">Peamine erinevus selle stsenaariumi konfiguratsiooni ja 1. stsenaariumi konfiguratsiooni vahel on see, et lisaks piirjoonesiltide lubamisele tuleb mitu voo sildi tüüpi seostada voo sildi mallide ja ühiku seeriagrupi ridadega.</span><span class="sxs-lookup"><span data-stu-id="9bab4-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="9bab4-416">Selle konfiguratsiooni saavutamiseks peate seadistama selle stsenaariumi jaoks järgmised elemendid.</span><span class="sxs-lookup"><span data-stu-id="9bab4-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="9bab4-417">**Voo töötlemise meetodid:** peate märkima voo sildi meetodiks korratav, lisama selle mallile kaks (või enam) korda ja seadma erinevad vooetapi koodid.</span><span class="sxs-lookup"><span data-stu-id="9bab4-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="9bab4-418">**Voo siltide mallid:** peate konfigureerima voo sildi mallid ja linkima need voo malliga.</span><span class="sxs-lookup"><span data-stu-id="9bab4-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="9bab4-419">Igal voo sildi mallil on oma voo sildi tüüp.</span><span class="sxs-lookup"><span data-stu-id="9bab4-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="9bab4-420">**Voo sildi paigutused:** peate looma mitu voo sildi paigutust.</span><span class="sxs-lookup"><span data-stu-id="9bab4-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="9bab4-421">Iga sildi astme kohta tuleb eraldi sildi paigutus ja piirjoonesildile oma paigutus.</span><span class="sxs-lookup"><span data-stu-id="9bab4-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="9bab4-422">Selles stsenaariumis näidatakse täielikku voogu.</span><span class="sxs-lookup"><span data-stu-id="9bab4-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="9bab4-423">Demoandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="9bab4-423">Make demo data available</span></span>

<span data-ttu-id="9bab4-424">Selle stsenaariumiga töötamiseks peavad teil olema installitud demoandmed ja peate valima juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="9bab4-425">Voo protsessi meetodi seadistamine</span><span class="sxs-lookup"><span data-stu-id="9bab4-425">Set up a wave process method</span></span>

1. <span data-ttu-id="9bab4-426">Avage jaotis **Laohaldus \> Seadistus \> Vood \> Voo protsessi meetodid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="9bab4-427">Kinnitage, et loendis oleks **waveLabelPrinting**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="9bab4-428">Kui seda pole, valige selle lisamiseks toimingupaanil **Meetodite uuesti loomine**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="9bab4-429">Märkige meetodi **waveLabelPrinting** puhul ruut **Muuda meetod korduvaks**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="9bab4-430">Voomalli seadistamine</span><span class="sxs-lookup"><span data-stu-id="9bab4-430">Set up a wave template</span></span>

1. <span data-ttu-id="9bab4-431">Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="9bab4-432">Valige voomall, nt **62 Saadetise vaikemall**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="9bab4-433">Teisaldage kiirkaardil **Meetodid** meetod **Voo sildi printimine** veergu **Valitud meetodid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="9bab4-434">Määrake veerus **Valitud meetodid** väärtus **Vooetapi kood**, nt *Pakk* meetodi **Voo sildi printimine** jaoks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton*, to the **Wave label printing** method.</span></span> <span data-ttu-id="9bab4-435">Lisateavet vooetapi koodide kohta leiate teemast [Vooetapi koodid](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9bab4-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="9bab4-436">Teisaldage meetod **Voo sildi printimine** teist korda veergu **Valitud meetodid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="9bab4-437">Määrake veerus **Valitud meetodid** erinev väärtus **Vooetapi kood**, nt *Kaubaalus* teise meetodi **Voo sildi printimine** jaoks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet*, to the second **Wave label printing** method.</span></span> <span data-ttu-id="9bab4-438">Lisateavet vooetapi koodide kohta leiate teemast [Vooetapi koodid](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9bab4-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="9bab4-439">Voo sildi kolme paigutuse loomine</span><span class="sxs-lookup"><span data-stu-id="9bab4-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="9bab4-440">Avage jaotis **Laohaldus \> Seadistus \> Dokumendi marsruudi valik \> Voo sildi paigutused**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="9bab4-441">Looge järgmiste sätetega kirje.</span><span class="sxs-lookup"><span data-stu-id="9bab4-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-442">**Sildi paigutuse ID:** *Pakk*</span><span class="sxs-lookup"><span data-stu-id="9bab4-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="9bab4-443">**Kirjeldus:** *Pakk (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="9bab4-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="9bab4-444">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="9bab4-445">Valige toimingupaanil **Voo sildi rea sätted**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="9bab4-446">Kuvatakse leht **Voo sildi rea sätted**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="9bab4-447">Siin saate konfigureerida sildi dünaamilise osa.</span><span class="sxs-lookup"><span data-stu-id="9bab4-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="9bab4-448">Lisage järgmiste sätetega rida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-449">**Rea ID:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="9bab4-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="9bab4-450">**Rea tabeli nimi:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="9bab4-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="9bab4-451">**Rea algpaigutus:** *0*</span><span class="sxs-lookup"><span data-stu-id="9bab4-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="9bab4-452">See väli määratleb vertikaalse paigutuse, kus sildil algab rida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="9bab4-453">**Rea kõrgus:** *0*</span><span class="sxs-lookup"><span data-stu-id="9bab4-453">**Row height:** *0*</span></span>

        <span data-ttu-id="9bab4-454">See väli määratleb iga rea kõrguse (punktides) vastavalt ZPL-standardile.</span><span class="sxs-lookup"><span data-stu-id="9bab4-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="9bab4-455">Rea kõrgus on horisontaalsete siltide puhul positiivne ja vertikaalsete siltide puhul negatiivne.</span><span class="sxs-lookup"><span data-stu-id="9bab4-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="9bab4-456">Kuna selles näites on ainult üks rida, saate väärtuseks seada *0* (null).</span><span class="sxs-lookup"><span data-stu-id="9bab4-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="9bab4-457">**Ridu lehel:** *1*</span><span class="sxs-lookup"><span data-stu-id="9bab4-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="9bab4-458">See väli määratleb ridade arvu, mida saab igale sildile printida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="9bab4-459">See seadistus prindib eraldi ZPL-sildi igale kirjele voo siltide tabelis.</span><span class="sxs-lookup"><span data-stu-id="9bab4-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="9bab4-460">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9bab4-460">Close the page.</span></span>
1. <span data-ttu-id="9bab4-461">Valige Toimingupaanil nupp **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="9bab4-462">Lisage päringuredaktori dialoogiboksis vahekaardile **Vahemik** rida, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="9bab4-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-463">**Tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-464">**Tuletatud tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-465">**Väli:** *Töö tüüp*</span><span class="sxs-lookup"><span data-stu-id="9bab4-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="9bab4-466">**Kriteeriumid:** *Komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="9bab4-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="9bab4-467">See päring tagab, et sildile prinditakse ainult komplekteerimise tüübiga tööread, mitte sisestamise tüübiga tööread.</span><span class="sxs-lookup"><span data-stu-id="9bab4-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="9bab4-468">Kui soovite printida veokirja ID-d, valige vahekaardil **Liitmised** tabel **Tööread** ja liitke sellega tabel **Saadetised**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="9bab4-469">Sulgege päringuredaktori dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="9bab4-470">Kiirkaardil **Printeri teksti paigutuse** on kolm jaotist, kuhu saate kirjutada printeri koodi: **Päise jaotis**, **Keha jaotis** ja **Jaluse jaotis**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="9bab4-471">Sisestage jaotise **Päise jaotis** väljale **Sildi päis** nõutava päise kood.</span><span class="sxs-lookup"><span data-stu-id="9bab4-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="9bab4-472">Näiteks kui kasutate Zebra printereid, saate kasutada järgmist koodi.</span><span class="sxs-lookup"><span data-stu-id="9bab4-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="9bab4-473">Sisestage jaotise **Keha jaotis** väljale **Sildi keha** nõutava keha ZPL-kood.</span><span class="sxs-lookup"><span data-stu-id="9bab4-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="9bab4-474">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="9bab4-474">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="9bab4-475">Sisestage jaotise **Keha jaotis** väljale **Sildi jalus** nõutava jaluse ZPL-kood.</span><span class="sxs-lookup"><span data-stu-id="9bab4-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="9bab4-476">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="9bab4-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="9bab4-477">See häälestus prindib igast sildist ühe eksemplari.</span><span class="sxs-lookup"><span data-stu-id="9bab4-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="9bab4-478">Kui vajate rohkem eksemplare (nt ühte eksemplari kaubaaluse kummalegi poolele), määrake jaluse jaotise **\^PQn** väärtuseks **n** nõutav eksemplaride arv.</span><span class="sxs-lookup"><span data-stu-id="9bab4-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="9bab4-479">Näiteks igast sildist nelja eksemplari printimiseks määrake **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="9bab4-480">Esimene silt on nüüd kasutamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="9bab4-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="9bab4-481">Looge järgmiste sätetega teine paigutuse kirje.</span><span class="sxs-lookup"><span data-stu-id="9bab4-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-482">**Sildi paigutuse ID:** *Kaubaalus*</span><span class="sxs-lookup"><span data-stu-id="9bab4-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="9bab4-483">**Kirjeldus:** *Kaubaalus*</span><span class="sxs-lookup"><span data-stu-id="9bab4-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="9bab4-484">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="9bab4-485">Valige toimingupaanil **Voo sildi rea sätted**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="9bab4-486">Kuvatakse leht **Voo sildi rea sätted**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="9bab4-487">Siin saate konfigureerida sildi dünaamilise osa.</span><span class="sxs-lookup"><span data-stu-id="9bab4-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="9bab4-488">Lisage järgmiste sätetega rida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-489">**Rea ID:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="9bab4-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="9bab4-490">**Rea tabeli nimi:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="9bab4-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="9bab4-491">**Rea algpaigutus:** *0*</span><span class="sxs-lookup"><span data-stu-id="9bab4-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="9bab4-492">See väli määratleb vertikaalse paigutuse, kus sildil algab rida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="9bab4-493">**Rea kõrgus:** *0*</span><span class="sxs-lookup"><span data-stu-id="9bab4-493">**Row height:** *0*</span></span>

        <span data-ttu-id="9bab4-494">See väli määratleb iga rea kõrguse (punktides) vastavalt ZPL-standardile.</span><span class="sxs-lookup"><span data-stu-id="9bab4-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="9bab4-495">Rea kõrgus on horisontaalsete siltide puhul positiivne ja vertikaalsete siltide puhul negatiivne.</span><span class="sxs-lookup"><span data-stu-id="9bab4-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="9bab4-496">Kuna selles näites on ainult üks rida, saate väärtuseks seada *0* (null).</span><span class="sxs-lookup"><span data-stu-id="9bab4-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="9bab4-497">**Ridu lehel:** *1*</span><span class="sxs-lookup"><span data-stu-id="9bab4-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="9bab4-498">See väli määratleb ridade arvu, mida saab igale sildile printida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="9bab4-499">See seadistus prindib eraldi ZPL-sildi igale kirjele voo siltide tabelis.</span><span class="sxs-lookup"><span data-stu-id="9bab4-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="9bab4-500">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9bab4-500">Close the page.</span></span>
1. <span data-ttu-id="9bab4-501">Valige Toimingupaanil nupp **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="9bab4-502">Lisage päringuredaktori dialoogiboksis vahekaardile **Vahemik** rida, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="9bab4-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-503">**Tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-504">**Tuletatud tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-505">**Väli:** *Töö tüüp*</span><span class="sxs-lookup"><span data-stu-id="9bab4-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="9bab4-506">**Kriteeriumid:** *Komplekteerimine*</span><span class="sxs-lookup"><span data-stu-id="9bab4-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="9bab4-507">See päring tagab, et sildile prinditakse ainult komplekteerimise tüübiga tööread, mitte sisestamise tüübiga tööread.</span><span class="sxs-lookup"><span data-stu-id="9bab4-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="9bab4-508">Kui soovite printida veokirja ID-d, valige vahekaardil **Liitmised** tabel **Tööread** ja liitke sellega tabel **Saadetised**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="9bab4-509">Sulgege päringuredaktori dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="9bab4-510">Kiirkaardil **Printeri teksti paigutuse** on kolm jaotist, kuhu saate kirjutada printeri koodi: **Päise jaotis**, **Keha jaotis** ja **Jaluse jaotis**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="9bab4-511">Sisestage jaotise **Päise jaotis** väljale **Sildi päis** nõutava päise kood.</span><span class="sxs-lookup"><span data-stu-id="9bab4-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="9bab4-512">Näiteks kui kasutate Zebra printereid, saate kasutada järgmist koodi.</span><span class="sxs-lookup"><span data-stu-id="9bab4-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="9bab4-513">Sisestage jaotise **Keha jaotis** väljale **Sildi keha** nõutava keha ZPL-kood.</span><span class="sxs-lookup"><span data-stu-id="9bab4-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="9bab4-514">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="9bab4-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="9bab4-515">Sisestage jaotise **Keha jaotis** väljale **Sildi jalus** nõutava jaluse ZPL-kood.</span><span class="sxs-lookup"><span data-stu-id="9bab4-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="9bab4-516">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="9bab4-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="9bab4-517">See häälestus prindib igast sildist ühe eksemplari.</span><span class="sxs-lookup"><span data-stu-id="9bab4-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="9bab4-518">Kui vajate rohkem eksemplare (nt ühte eksemplari kaubaaluse kummalegi poolele), määrake jaluse jaotise **\^PQn** väärtuseks **n** nõutav eksemplaride arv.</span><span class="sxs-lookup"><span data-stu-id="9bab4-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="9bab4-519">Näiteks igast sildist nelja eksemplari printimiseks määrake **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="9bab4-520">Teine silt on nüüd kasutamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="9bab4-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="9bab4-521">Looge järgmiste sätetega kolmas paigutuse kirje.</span><span class="sxs-lookup"><span data-stu-id="9bab4-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-522">**Sildi paigutuse ID:** *Piirjoon*</span><span class="sxs-lookup"><span data-stu-id="9bab4-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="9bab4-523">**Kirjeldus:** *Piirjoonesilt*</span><span class="sxs-lookup"><span data-stu-id="9bab4-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="9bab4-524">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="9bab4-525">Kiirkaardil **Printeri teksti paigutuse** on kolm jaotist, kuhu saate kirjutada printeri koodi: **Päise jaotis**, **Keha jaotis** ja **Jaluse jaotis**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="9bab4-526">Sisestage jaotise **Päise jaotis** väljale **Sildi päis** nõutava päise ZPL-kood.</span><span class="sxs-lookup"><span data-stu-id="9bab4-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="9bab4-527">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="9bab4-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="9bab4-528">Seekord pole keha nõutav.</span><span class="sxs-lookup"><span data-stu-id="9bab4-528">This time, no body is required.</span></span> <span data-ttu-id="9bab4-529">Seega, sisestage ainult nõutav tekst jaotises **Jaluse jaotis**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="9bab4-530">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="9bab4-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="9bab4-531">Kolmas silt on nüüd kasutamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="9bab4-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9bab4-532">See kolmas silt on piirjoonesilt, mida kasutatakse sildi rullide vahelise eraldajana.</span><span class="sxs-lookup"><span data-stu-id="9bab4-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="9bab4-533">Voo sildi kahe tüübi loomine</span><span class="sxs-lookup"><span data-stu-id="9bab4-533">Create two wave label types</span></span>

1. <span data-ttu-id="9bab4-534">Avage jaotis **Laohaldus \> Seadistus \> Dokumendi marsruudi valik \> Voo sildi tüübid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="9bab4-535">Looge järgmiste sätetega kirje.</span><span class="sxs-lookup"><span data-stu-id="9bab4-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-536">**Sildi tüüp:** *Pakk*</span><span class="sxs-lookup"><span data-stu-id="9bab4-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="9bab4-537">**Kirjeldus:** *Pakk*</span><span class="sxs-lookup"><span data-stu-id="9bab4-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="9bab4-538">Looge järgmiste sätetega teine kirje.</span><span class="sxs-lookup"><span data-stu-id="9bab4-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-539">**Sildi tüüp:** *Kaubaalus*</span><span class="sxs-lookup"><span data-stu-id="9bab4-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="9bab4-540">**Kirjeldus:** *Kaubaalus*</span><span class="sxs-lookup"><span data-stu-id="9bab4-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="9bab4-541">Üksuse seeriagruppide häälestamine</span><span class="sxs-lookup"><span data-stu-id="9bab4-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="9bab4-542">Avage jaotis **Laohaldus \> Seadistus \> Ladu \> Ühiku seeriagrupid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="9bab4-543">Valige või looge grupp **Ea Kast PL**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="9bab4-544">Määrake rea **Kast** välja **Voo taseme tüüp** väärtuseks *Pakk*.</span><span class="sxs-lookup"><span data-stu-id="9bab4-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="9bab4-545">Määrake rea **PL** välja **Voo taseme tüüp** väärtuseks *Kaubaalus*.</span><span class="sxs-lookup"><span data-stu-id="9bab4-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="9bab4-546">Voo sildi mallide loomine</span><span class="sxs-lookup"><span data-stu-id="9bab4-546">Create wave label templates</span></span>

1. <span data-ttu-id="9bab4-547">Avage jaotis **Laohaldus \> Seadistus \> Dokumendi marsruudi valik \> Voo sildi mallid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="9bab4-548">Looge järgmiste sätetega sildi mall.</span><span class="sxs-lookup"><span data-stu-id="9bab4-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-549">**Voo malli nimi:** *Paki sildid*</span><span class="sxs-lookup"><span data-stu-id="9bab4-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="9bab4-550">**Kirjeldus:** *Paki sildid*</span><span class="sxs-lookup"><span data-stu-id="9bab4-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="9bab4-551">**Vooetapi kood:** *Pakk*</span><span class="sxs-lookup"><span data-stu-id="9bab4-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="9bab4-552">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="9bab4-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="9bab4-553">Valige kiirkaardil **Üldine** väljal **Voo sildi tüüp** suvand, nt *Pakk*.</span><span class="sxs-lookup"><span data-stu-id="9bab4-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="9bab4-554">Lisage kiirkaardil **Voo sildi malli üksikasjad** rida, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="9bab4-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-555">**Sildi paigutuse ID:** *Pakk*</span><span class="sxs-lookup"><span data-stu-id="9bab4-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="9bab4-556">**Printeri nimi:** valige sobiv ZPL-printer.</span><span class="sxs-lookup"><span data-stu-id="9bab4-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="9bab4-557">**Käivita päring:** *Jah* (see säte on valikuline, kuid see on optimaalse jõudluse tagamiseks soovitatav.)</span><span class="sxs-lookup"><span data-stu-id="9bab4-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="9bab4-558">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="9bab4-559">Valikuline: kui seadistate kliendipõhist sildi kujundust, tuleb teil luua päring kliendi konto leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="9bab4-560">Valige kiirkaardil **Voo sildi malli üksikasjad** suvand **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="9bab4-561">Seejärel lisage päringuredaktori dialoogiboksis vahekaardile **Vahemik** rida, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="9bab4-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-562">**Tabel:** *Saadetised*</span><span class="sxs-lookup"><span data-stu-id="9bab4-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="9bab4-563">**Tuletatud tabel:** *Saadetised*</span><span class="sxs-lookup"><span data-stu-id="9bab4-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="9bab4-564">**Väli:** *Kontonumber*</span><span class="sxs-lookup"><span data-stu-id="9bab4-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="9bab4-565">**Kriteeriumid:** sisestage vastava kliendi kontonumber.</span><span class="sxs-lookup"><span data-stu-id="9bab4-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="9bab4-566">Kui olete lõpetanud, valige päringuredaktori dialoogiboksi sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="9bab4-567">Valige toimingupaanil suvand **Päringu redigeerimine**, et avada terve sildi malli päringuredaktori dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="9bab4-568">Lisage päringuredaktori dialoogiboksis vahekaardile **Sortimine** rida, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="9bab4-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-569">**Tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-570">**Tuletatud tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-571">**Väli:** *Koormuse viiterea ID (kirje-ID)*</span><span class="sxs-lookup"><span data-stu-id="9bab4-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="9bab4-572">**Otsingusuund:** *Kasvav*</span><span class="sxs-lookup"><span data-stu-id="9bab4-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="9bab4-573">Lisage järgmiste sätetega teine rida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-574">**Tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-575">**Tuletatud tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-576">**Väli:** *Saadetise ID*</span><span class="sxs-lookup"><span data-stu-id="9bab4-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="9bab4-577">**Otsingusuund:** *Kasvav*</span><span class="sxs-lookup"><span data-stu-id="9bab4-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="9bab4-578">Päringuredaktori dialoogiboksi sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="9bab4-579">Teateaken palub teil rühmitamise lähtestamise toimingu kinnitada.</span><span class="sxs-lookup"><span data-stu-id="9bab4-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="9bab4-580">Jätkamiseks valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="9bab4-581">Valige toimingupaanil **Voo sildi malligrupp**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="9bab4-582">Määrake dialoogiboksi **Voo sildi malli grupp** reale, kus välja **Viitevälja nimi** väärtuseks on seatud *Saadetise ID*, järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="9bab4-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="9bab4-583">**Prindi piirjoonesilt:** märkige see ruut.</span><span class="sxs-lookup"><span data-stu-id="9bab4-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="9bab4-584">**Sildi paigutuse ID:** valige piirjoonesilt.</span><span class="sxs-lookup"><span data-stu-id="9bab4-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="9bab4-585">(Valige näiteks sildi paigutus *Piirjoon*, mille eelnevalt selles stsenaariumis lõite.)</span><span class="sxs-lookup"><span data-stu-id="9bab4-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="9bab4-586">**Printeri nimi:** valige piirjoonesildile printer.</span><span class="sxs-lookup"><span data-stu-id="9bab4-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="9bab4-587">(Tavaliselt tuleb sildi rullide tükeldamise eesmärgil valida sama printer, mis on valitud kiirkaardil **Voo sildi malli üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="9bab4-588">Kuid ka muud stsenaariumid on võimalikud.)</span><span class="sxs-lookup"><span data-stu-id="9bab4-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="9bab4-589">Märkige real, kus välja **Viitevälja nimi** väärtuseks on seatud *Koormuse viiterea ID*, ruut **Sildi kooste ID**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-589">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9bab4-590">See häälestus loob ühe sildi järjestuse („Pakk 1/X”) koormuse rea kohta kogu voos, sõltumata töö rühmitamise seadistusest.</span><span class="sxs-lookup"><span data-stu-id="9bab4-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="9bab4-591">Seda sildi järjestust saab printida sildi paigutusele.</span><span class="sxs-lookup"><span data-stu-id="9bab4-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="9bab4-592">Lisaks eraldatakse erinevate saadetiste sildid valitud piirjoonesildiga.</span><span class="sxs-lookup"><span data-stu-id="9bab4-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="9bab4-593">Valige **OK** dialoogiboksi **Voo sildi malli grupp** sulgemiseks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="9bab4-594">Looge järgmiste sätetega teine sildi mall.</span><span class="sxs-lookup"><span data-stu-id="9bab4-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-595">**Voo malli nimi:** *Kaubaaluse sildid*</span><span class="sxs-lookup"><span data-stu-id="9bab4-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="9bab4-596">**Kirjeldus:** *Kaubaaluse sildid*</span><span class="sxs-lookup"><span data-stu-id="9bab4-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="9bab4-597">**Vooetapi kood:** *Kaubaalus*</span><span class="sxs-lookup"><span data-stu-id="9bab4-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="9bab4-598">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="9bab4-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="9bab4-599">Valige kiirkaardil **Üldine** väljal **Voo sildi tüüp** suvand, nt *Kaubaalus*.</span><span class="sxs-lookup"><span data-stu-id="9bab4-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="9bab4-600">Lisage kiirkaardil **Voo sildi malli üksikasjad** rida, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="9bab4-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-601">**Sildi paigutuse ID:** *Kaubaalus*</span><span class="sxs-lookup"><span data-stu-id="9bab4-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="9bab4-602">**Printeri nimi:** valige sobiv ZPL-printer.</span><span class="sxs-lookup"><span data-stu-id="9bab4-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="9bab4-603">**Käivita päring:** *Jah* (see säte on valikuline, kuid see on optimaalse jõudluse tagamiseks soovitatav.)</span><span class="sxs-lookup"><span data-stu-id="9bab4-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="9bab4-604">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="9bab4-605">Valikuline: kui seadistate kliendipõhist sildi kujundust, tuleb teil luua päring kliendi konto leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="9bab4-606">Valige kiirkaardil **Voo sildi malli üksikasjad** suvand **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="9bab4-607">Seejärel lisage päringuredaktori dialoogiboksis vahekaardile **Vahemik** rida, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="9bab4-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-608">**Tabel:** *Saadetised*</span><span class="sxs-lookup"><span data-stu-id="9bab4-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="9bab4-609">**Tuletatud tabel:** *Saadetised*</span><span class="sxs-lookup"><span data-stu-id="9bab4-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="9bab4-610">**Väli:** *Kontonumber*</span><span class="sxs-lookup"><span data-stu-id="9bab4-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="9bab4-611">**Kriteeriumid:** sisestage vastava kliendi kontonumber.</span><span class="sxs-lookup"><span data-stu-id="9bab4-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="9bab4-612">Kui olete lõpetanud, valige päringuredaktori dialoogiboksi sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="9bab4-613">Valige toimingupaanil suvand **Päringu redigeerimine**, et avada terve sildi malli päringuredaktori dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="9bab4-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="9bab4-614">Lisage päringuredaktori dialoogiboksis vahekaardile **Sortimine** rida, millel on järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="9bab4-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-615">**Tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-616">**Tuletatud tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-617">**Väli:** *Koormuse viiterea ID (kirje-ID)*</span><span class="sxs-lookup"><span data-stu-id="9bab4-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="9bab4-618">**Otsingusuund:** *Kasvav*</span><span class="sxs-lookup"><span data-stu-id="9bab4-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="9bab4-619">Lisage järgmiste sätetega teine rida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-620">**Tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-621">**Tuletatud tabel:** *Tööread*</span><span class="sxs-lookup"><span data-stu-id="9bab4-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="9bab4-622">**Väli:** *Saadetise ID*</span><span class="sxs-lookup"><span data-stu-id="9bab4-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="9bab4-623">**Otsingusuund:** *Kasvav*</span><span class="sxs-lookup"><span data-stu-id="9bab4-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="9bab4-624">Päringuredaktori dialoogiboksi sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="9bab4-625">Teateaken palub teil rühmitamise lähtestamise toimingu kinnitada.</span><span class="sxs-lookup"><span data-stu-id="9bab4-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="9bab4-626">Jätkamiseks valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="9bab4-627">Valige toimingupaanil **Voo sildi malligrupp**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="9bab4-628">Määrake dialoogiboksi **Voo sildi malli grupp** reale, kus välja **Viitevälja nimi** väärtuseks on seatud *Saadetise ID*, järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="9bab4-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="9bab4-629">**Prindi piirjoonesilt:** märkige see ruut.</span><span class="sxs-lookup"><span data-stu-id="9bab4-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="9bab4-630">**Sildi paigutuse ID:** valige piirjoonesilt.</span><span class="sxs-lookup"><span data-stu-id="9bab4-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="9bab4-631">(Valige näiteks sildi paigutus *Piirjoon*, mille eelnevalt selles stsenaariumis lõite.)</span><span class="sxs-lookup"><span data-stu-id="9bab4-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="9bab4-632">**Printeri nimi:** valige piirjoonesildile printer.</span><span class="sxs-lookup"><span data-stu-id="9bab4-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="9bab4-633">(Tavaliselt tuleb sildi rullide tükeldamise eesmärgil valida sama printer, mis on valitud kiirkaardil **Voo sildi malli üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="9bab4-634">Kuid ka muud stsenaariumid on võimalikud.)</span><span class="sxs-lookup"><span data-stu-id="9bab4-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="9bab4-635">Märkige real, kus välja **Viitevälja nimi** väärtuseks on seatud *Koormuse viiterea ID*, ruut **Sildi kooste ID**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-635">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9bab4-636">See häälestus loob ühe sildi järjestuse („Pakk 1/X”) koormuse rea kohta kogu voos, sõltumata töö rühmitamise seadistusest.</span><span class="sxs-lookup"><span data-stu-id="9bab4-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="9bab4-637">Seda sildi järjestust saab printida sildi paigutusele.</span><span class="sxs-lookup"><span data-stu-id="9bab4-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="9bab4-638">Lisaks eraldatakse erinevate saadetiste sildid valitud piirjoonesildiga.</span><span class="sxs-lookup"><span data-stu-id="9bab4-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="9bab4-639">Numbriseeria laienduste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="9bab4-639">Configure number sequence extensions</span></span>

<span data-ttu-id="9bab4-640">Numbriseeria laiendused juhivad konkreetsete numbriseeriate GS1 vastavust.</span><span class="sxs-lookup"><span data-stu-id="9bab4-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="9bab4-641">See konfiguratsioon on praeguse stsenaariumi puhul valikuline.</span><span class="sxs-lookup"><span data-stu-id="9bab4-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="9bab4-642">Lisateavet ja konfigureerimise juhiseid leiate teemast [Numbriseeria laienduste konfigureerimine](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="9bab4-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="9bab4-643">Müügitellimuse loomine ja selle väljastamine lattu</span><span class="sxs-lookup"><span data-stu-id="9bab4-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="9bab4-644">Avage jaotis **Müük ja turundus \> Müügitellimus \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="9bab4-645">Looge järgmiste sätetega müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="9bab4-646">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="9bab4-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="9bab4-647">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="9bab4-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="9bab4-648">Lisage kaks müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="9bab4-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="9bab4-649">Müügitellimuse rida 1:</span><span class="sxs-lookup"><span data-stu-id="9bab4-649">Sales order line 1:</span></span>

        - <span data-ttu-id="9bab4-650">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="9bab4-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="9bab4-651">**Kogus:** *9024*</span><span class="sxs-lookup"><span data-stu-id="9bab4-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="9bab4-652">**Ühik:** *ea* (9024 ea = 376 kasti = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="9bab4-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="9bab4-653">Müügitellimuse rida 2:</span><span class="sxs-lookup"><span data-stu-id="9bab4-653">Sales order line 2:</span></span>

        - <span data-ttu-id="9bab4-654">**Kauba kood:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="9bab4-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="9bab4-655">**Kogus:** *9016*</span><span class="sxs-lookup"><span data-stu-id="9bab4-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="9bab4-656">**Ühik:** *ea* (9016 ea = 322 kasti = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="9bab4-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="9bab4-657">Siin esitatud kaubad ja kogused on ainult näited.</span><span class="sxs-lookup"><span data-stu-id="9bab4-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="9bab4-658">Need peavad kasutama ühiku seeriagruppi, mille eelnevalt määratlesite, neile tuleb määratleda vastav ühiku teisendamine ühikult *ea* ühikule *Kast* ühikule *PL* ja neil peab olema kaubavarusid laos *62*.</span><span class="sxs-lookup"><span data-stu-id="9bab4-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="9bab4-659">Lisateavet leiate teemast [Mõõtühik ja varude poliitika](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="9bab4-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="9bab4-660">Valige müügitellimuse rida 1.</span><span class="sxs-lookup"><span data-stu-id="9bab4-660">Select sales order line 1.</span></span> <span data-ttu-id="9bab4-661">Seejärel valige menüü **Varud** jaotisest **Müügitellimuse rida** suvand **Reserveerimised**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="9bab4-662">Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii** ja seejärel sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9bab4-662">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="9bab4-663">Korrake etappe 4 ja 5 müügitellimuse rea 2 puhul.</span><span class="sxs-lookup"><span data-stu-id="9bab4-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="9bab4-664">Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="9bab4-665">Toimub järgmine:</span><span class="sxs-lookup"><span data-stu-id="9bab4-665">The following events occur:</span></span> 

    - <span data-ttu-id="9bab4-666">Süsteem töötleb loodud saadetist, kasutades malli, mis sisaldab sildi printimise etappi.</span><span class="sxs-lookup"><span data-stu-id="9bab4-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="9bab4-667">Sildi paigutust kasutatakse sildi vormingu määratlemiseks ja tulemuseks on silt, mis prinditakse sildi mallis valitud printeriga.</span><span class="sxs-lookup"><span data-stu-id="9bab4-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="9bab4-668">Voo sildid luuakse ja prinditakse.</span><span class="sxs-lookup"><span data-stu-id="9bab4-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="9bab4-669">Siltide arv on võrdne pakkide arvuga (selles näites on 376 kasti silti 1. rea kohta, 322 kasti silti 2. rea kohta, 47 PL silti 1. rea kohta, 47 PL silti 2. rea kohta ja kaks piirjoonesilti, millel on saadetise ID).</span><span class="sxs-lookup"><span data-stu-id="9bab4-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="9bab4-670">Saadetistele luuakse uus veokirja ID.</span><span class="sxs-lookup"><span data-stu-id="9bab4-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="9bab4-671">Kui konfigureerisite numbriseeria laiendused, järgib voo sildi ID numbrivormingut **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="9bab4-672">Saate kuvada ja uuesti printida järgmiste lehtede voo silte.</span><span class="sxs-lookup"><span data-stu-id="9bab4-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="9bab4-673">Kõik saadetised \> Saadetise üksikasjad</span><span class="sxs-lookup"><span data-stu-id="9bab4-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="9bab4-674">Kõik koormused \> Koormuse üksikasjad</span><span class="sxs-lookup"><span data-stu-id="9bab4-674">All loads \> Load details</span></span>
- <span data-ttu-id="9bab4-675">Kõik vood</span><span class="sxs-lookup"><span data-stu-id="9bab4-675">All waves</span></span>
- <span data-ttu-id="9bab4-676">Voo sildid</span><span class="sxs-lookup"><span data-stu-id="9bab4-676">Wave labels</span></span>
- <span data-ttu-id="9bab4-677">Voosildi ajalugu</span><span class="sxs-lookup"><span data-stu-id="9bab4-677">Wave label history</span></span>

<span data-ttu-id="9bab4-678">Enamiku nende lehtede puhul leiate vastava funktsiooni, valides toimingupaani vahekaardi **Saadetised** grupis **Seotud teave** suvandi **Voo sildid**.</span><span class="sxs-lookup"><span data-stu-id="9bab4-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9bab4-679">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="9bab4-679">Additional resources</span></span>

- [<span data-ttu-id="9bab4-680">Voosiltide uuesti printimine ja tühistamine</span><span class="sxs-lookup"><span data-stu-id="9bab4-680">Reprint and void wave labels</span></span>](reprint-and-void-wave-labels.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]