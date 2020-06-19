---
title: Töökaardi seadmes lõpetamisest teatamine
description: Selles teemas kirjeldatakse, kuidas konfigureerida süsteemi nii, et töökaardi seadme kasutajad saavad kanda lõpetatud tooted tootmistellimusest üle varudesse.
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403258"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="b212c-103">Töökaardi seadmes lõpetamisest teatamine</span><span class="sxs-lookup"><span data-stu-id="b212c-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b212c-104">Töötajad kasutavad tootmistöö lõpetatud kogustest teatamiseks töökaardi seadme lehte **Edenemisest teatamine**.</span><span class="sxs-lookup"><span data-stu-id="b212c-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="b212c-105">Lõpetatuna teatatud tooted varudesse lisamise kontroll</span><span class="sxs-lookup"><span data-stu-id="b212c-105">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="b212c-106">Selleks, et kontrollida, kas ja kuidas viimase toimingu puhul lõpetatuna teatatud kogused tuleks lisada varudesse, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b212c-106">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="b212c-107">Avage **Toote juhtimine \> Seadistamine \> Tootmise käivitamine \> Tootmistellimuse vaikesätted**.</span><span class="sxs-lookup"><span data-stu-id="b212c-107">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="b212c-108">Määrake vahekaardil **Teata lõpetamisest** välja **Uuenda lõpetatud aruannet võrgus** väärtuseks üks järgmistest väärtustest.</span><span class="sxs-lookup"><span data-stu-id="b212c-108">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="b212c-109">**Ei** – ühtki kogust ei lisata varudesse, kui kogused viimases toimingus esitatakse.</span><span class="sxs-lookup"><span data-stu-id="b212c-109">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="b212c-110">Tootmistellimuse olek ei muutu kunagi.</span><span class="sxs-lookup"><span data-stu-id="b212c-110">The status of the production order will never change.</span></span>
    - <span data-ttu-id="b212c-111">**Olek + Kogus** – tootmistellimuse oleku väärtuseks muutub *Lõpetamine kinnitatud* ja kogus kinnitatakse lõpetatuna varudesse.</span><span class="sxs-lookup"><span data-stu-id="b212c-111">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="b212c-112">**Kogus** – tootmistellimuse oleku väärtus muutub lõpetatuks, kuid tootmistellimuse olek ei muutu kunagi.</span><span class="sxs-lookup"><span data-stu-id="b212c-112">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="b212c-113">**Olek** – muutub üksnes tootmistellimuse olek.</span><span class="sxs-lookup"><span data-stu-id="b212c-113">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="b212c-114">Koguste viimases toimingus kinnitamise järel ei lisata koguseid varudesse.</span><span class="sxs-lookup"><span data-stu-id="b212c-114">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="b212c-115">Koguseid ei jälgita laos, kui toimingud, milles need on lõpetatuna kinnitatud, ei ole määratletud viimase toiminguna.</span><span class="sxs-lookup"><span data-stu-id="b212c-115">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="b212c-116">Samas saab neid koguseid kasutada edenemise kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="b212c-116">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="b212c-117">Samuti saab need kaasata reeglitesse, mis kontrollivad, kas töötajad saavad enne eelmise toimingu kinnitatud koguste kohta määratletud künnise ületamist alustada järgmist toimingut.</span><span class="sxs-lookup"><span data-stu-id="b212c-117">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="b212c-118">Need reeglid saate määratleda lehe **Tootmistellimuse vaikesätted** vahekaardil **Koguste kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="b212c-118">You can define these rules on the **Quantity validation** tab of the **Production order defaults** page.</span></span>

<span data-ttu-id="b212c-119">Lehega **Tootmistellimuse vaikesätted** töötamise kohta vaadake lisateavet teemast [Juhtimise parameetrid tootmise käivitamises](production-parameters-manufacturing-execution.md).</span><span class="sxs-lookup"><span data-stu-id="b212c-119">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="b212c-120">Partii kaudu juhitud kaupade lõpetatuna teatamine</span><span class="sxs-lookup"><span data-stu-id="b212c-120">Report batch-controlled items as finished</span></span>

<span data-ttu-id="b212c-121">Töökaardi seade toetab partiikaupade aruandluse osas kolme stsenaariumit.</span><span class="sxs-lookup"><span data-stu-id="b212c-121">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="b212c-122">Need stsenaariumid kehtivad nii kaupadele, mis on lubatud täpsemate laoprotsesside jaoks, kui ka kaupadele, mis ei ole täpsemate laoprotsesside jaoks lubatud.</span><span class="sxs-lookup"><span data-stu-id="b212c-122">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="b212c-123">**Käsitsi määratud partiinumbrid:** töötajad sisestavad kohandatud partiinumbri.</span><span class="sxs-lookup"><span data-stu-id="b212c-123">**Manually assigned batch numbers:** Workers enter a custom batch number.</span></span> <span data-ttu-id="b212c-124">Partiinumber võib tuleneda välisallikast, mis ei ole süsteemile teada.</span><span class="sxs-lookup"><span data-stu-id="b212c-124">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="b212c-125">**Eelmääratletud partiinumbrid:** töötajad valivad partiinumbri partiinumbrite loetelust, mille süsteem on enne tootmistellimuse töökaardi seadmele väljastamist automaatselt loonud.</span><span class="sxs-lookup"><span data-stu-id="b212c-125">**Predefined batch numbers:** Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="b212c-126">**Kindlaks määratud partiinumbrid:** töötajad ei sisesta ega vali partiinumbrit.</span><span class="sxs-lookup"><span data-stu-id="b212c-126">**Fixed batch numbers:** Workers don't enter or select a batch number.</span></span> <span data-ttu-id="b212c-127">Selle asemel määrab süsteem tootmistellimusele enne väljastamist automaatselt partiinumbri.</span><span class="sxs-lookup"><span data-stu-id="b212c-127">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>

<span data-ttu-id="b212c-128">Iga stsenaariumi lubamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b212c-128">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="b212c-129">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="b212c-129">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="b212c-130">Valige konfigureeritav toode.</span><span class="sxs-lookup"><span data-stu-id="b212c-130">Select the product to configure.</span></span>
1. <span data-ttu-id="b212c-131">Valige kiirkaardil **Varude haldus** väljal **Partiinumbri grupp** jälgimisnumbri grupp, mis on seadistatud teie stsenaariumi toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="b212c-131">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="b212c-132">Kui partii juhitud tootele ei määrata partiinumbri gruppi, siis võimaldab töökaardi seade vaikesättena sisestada partiinumbri lõpetamisest teatamise ajal käsitsi.</span><span class="sxs-lookup"><span data-stu-id="b212c-132">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="b212c-133">Järgnevates alajaotistes kirjeldatakse, kuidas seadistada jälgimisnumbri gruppe, mis toetaks igat partiikaupade aruandlusega seotud stsenaariumit.</span><span class="sxs-lookup"><span data-stu-id="b212c-133">The following subsections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a><span data-ttu-id="b212c-134">Partiinumbri aruandluse lubamine töökaardi seadmes</span><span class="sxs-lookup"><span data-stu-id="b212c-134">Enable batch number reporting on the job card device</span></span>

<span data-ttu-id="b212c-135">Selleks, et lubada töökaardi seadmel aktsepteerida lõpetatuna kinnitamise ajal partiinumbrit, peate kasutama [funktsioonihaldust](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), et lülitada sisse järgmised funktsioonid (samas järjekorras).</span><span class="sxs-lookup"><span data-stu-id="b212c-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="b212c-136">Töökaardi vahendi aruande edenemise dialoogi täiustatud kasutuskogemus</span><span class="sxs-lookup"><span data-stu-id="b212c-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="b212c-137">Luba sisestada partii- ja seerianumbreid, kui need märgitakse töökaardi vahendil lõpetatuks (eelvaade)</span><span class="sxs-lookup"><span data-stu-id="b212c-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device (Preview)</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="b212c-138">Jälgimisnumbri grupi seadistamine, mis võimaldab töötajatel partiinumbri käsitsi määrata</span><span class="sxs-lookup"><span data-stu-id="b212c-138">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="b212c-139">Käsitsi määratud partiinumbrite lubamiseks seadistage jälgimisgrupi number, toimides järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b212c-139">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="b212c-140">Avage **Varude haldus \> Seadistamine \> Dimensioonid \> Jälgimisnumbri grupid**.</span><span class="sxs-lookup"><span data-stu-id="b212c-140">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="b212c-141">Looge või valige seadistamiseks jälgimisnumbri grupp.</span><span class="sxs-lookup"><span data-stu-id="b212c-141">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="b212c-142">Seadke kiirkaardil **Üldine** suvandi **Käsitsi** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b212c-142">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="b212c-143">![Jälgimisnumbrite gruppide leht](media/tracking-number-group-manual.png "Jälgimisnumbrite gruppide leht")</span><span class="sxs-lookup"><span data-stu-id="b212c-143">![Tracking number groups page](media/tracking-number-group-manual.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="b212c-144">Seadke vastavalt vajadusele muud väärtused ja seejärel valige antud jälgimisnumbri grupp nende väljastatud toodete partiinumbri grupiks, mille jaoks soovite seda stsenaariumit kasutada.</span><span class="sxs-lookup"><span data-stu-id="b212c-144">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="b212c-145">Antud stsenaariumi kasutamisel on töökaardi seadmes toodud lehel **Edenemisest teadaandmine** väljal **Partiinumber** tekstikast, kus töötajad saavad sisestada mis tahes väärtuse.</span><span class="sxs-lookup"><span data-stu-id="b212c-145">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="b212c-146">![Edenemisest teatamise leht koos käsitsi sisestatavate partiinumbrite väljaga](media/job-card-device-batch-manual.png "Edenemisest teatamise leht koos käsitsi sisestatavate partiinumbrite väljaga")</span><span class="sxs-lookup"><span data-stu-id="b212c-146">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="b212c-147">Eelmääratletud partiinumbrite loetelu esitava jälgimisnumbri grupi seadistamine</span><span class="sxs-lookup"><span data-stu-id="b212c-147">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="b212c-148">Eelmääratletud partiinumbrite loetelu esitamiseks seadistage jälgimisgrupi number, toimides järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b212c-148">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="b212c-149">Avage **Varude haldus \> Seadistamine > Dimensioonid \> Jälgimisnumbri grupid**.</span><span class="sxs-lookup"><span data-stu-id="b212c-149">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="b212c-150">Looge või valige seadistamiseks jälgimisnumbri grupp.</span><span class="sxs-lookup"><span data-stu-id="b212c-150">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="b212c-151">Seadke kiirkaardil **Üldine** suvandi **Ainult laokannetele** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b212c-151">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="b212c-152">Partiinumbrite koguse kaupa eraldamiseks sisestatud väärtuse alusel kasutage välja **Koguse kohta**.</span><span class="sxs-lookup"><span data-stu-id="b212c-152">Use the **Per qty.** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="b212c-153">Näiteks on teil kümne tüki tootmistellimus ja välja **Koguse kohta** väärtuseks on seatud *2*.</span><span class="sxs-lookup"><span data-stu-id="b212c-153">For example, you have a production order for ten pieces, and the **Per qty.** field is set to *2*.</span></span> <span data-ttu-id="b212c-154">Sellisel juhul määratakse tootmistellimusele loomisel viis partiinumbrit.</span><span class="sxs-lookup"><span data-stu-id="b212c-154">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="b212c-155">![Jälgimisnumbrite gruppide leht](media/tracking-number-group-predefined.png "Jälgimisnumbrite gruppide leht")</span><span class="sxs-lookup"><span data-stu-id="b212c-155">![Tracking number groups page](media/tracking-number-group-predefined.png "The Tracking number groups page")</span></span>

1. <span data-ttu-id="b212c-156">Seadke vastavalt vajadusele muud väärtused ja seejärel valige antud jälgimisnumbri grupp nende väljastatud toodete partiinumbri grupiks, mille jaoks soovite seda stsenaariumit kasutada.</span><span class="sxs-lookup"><span data-stu-id="b212c-156">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="b212c-157">Antud stsenaariumi kasutamisel on töökaardi seadmes toodud lehel **Edenemisest teadaandmine** väljal **Partiinumber** ripploend, kus töötajad peavad valima eelmääratletud väärtuse.</span><span class="sxs-lookup"><span data-stu-id="b212c-157">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="b212c-158">![Edenemisest teatamise leht koos eelmääratletud partiinumbrite loeteluga](media/job-card-device-batch-predefined.png "Edenemisest teadaandmise leht koos eelmääratletud partiinumbrite loeteluga")</span><span class="sxs-lookup"><span data-stu-id="b212c-158">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="b212c-159">Automaatselt partiinumbreid määrava jälgimisnumbri grupi seadistamine</span><span class="sxs-lookup"><span data-stu-id="b212c-159">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="b212c-160">Kui partiinumbrid tuleks määrata automaatselt ja töötaja sisendita, siis toimige jälgimisnumbri grupi seadistamisel järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b212c-160">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="b212c-161">Avage **Varude haldus \> Seadistamine \> Dimensioonid \> Jälgimisnumbri grupid**.</span><span class="sxs-lookup"><span data-stu-id="b212c-161">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="b212c-162">Looge või valige seadistamiseks jälgimisnumbri grupp.</span><span class="sxs-lookup"><span data-stu-id="b212c-162">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="b212c-163">Seadke kiirkaardil **Üldine** suvandi **Ainult laokannetele** väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="b212c-163">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="b212c-164">Seadistage suvandi **Käsitsi** väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="b212c-164">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="b212c-165">![Jälgimisnumbrite gruppide leht](media/tracking-number-group-fixed.png "Jälgimisnumbrite gruppide leht")</span><span class="sxs-lookup"><span data-stu-id="b212c-165">![Tracking number groups page](media/tracking-number-group-fixed.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="b212c-166">Seadke vastavalt vajadusele muud väärtused ja seejärel valige antud jälgimisnumbri grupp nende väljastatud toodete partiinumbri grupiks, mille jaoks soovite seda stsenaariumit kasutada.</span><span class="sxs-lookup"><span data-stu-id="b212c-166">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="b212c-167">Antud stsenaariumi kasutamisel on töökaardi seadmes toodud lehel **Edenemisest teadaandmine** väljal **Partiinumber** väärtus, kuid töötajad ei saa seda muuta.</span><span class="sxs-lookup"><span data-stu-id="b212c-167">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="b212c-168">![Edenemisest teatamise leht koos kindlaks määratud partiinumbriga](media/job-card-device-batch-fixed.png "Edenemisest teatamise leht koos kindlaks määratud partiinumbriga")</span><span class="sxs-lookup"><span data-stu-id="b212c-168">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="b212c-169">Lõpetatuna kinnitamine litsentsiplaadil</span><span class="sxs-lookup"><span data-stu-id="b212c-169">Report as finished to a license plate</span></span>

<span data-ttu-id="b212c-170">Täpsemad laoprotsessid rakendavad lao asukohtades varude jälgimiseks vastaval otstarbel seadistatud litsentsiplaadi dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="b212c-170">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="b212c-171">Sellisel juhul nõutakse töötajalt koguste lõpetamisest teatamisel identifitseerimisnumbrit.</span><span class="sxs-lookup"><span data-stu-id="b212c-171">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="b212c-172">Litsentsiplaadi aruandluse ja sildi printimise lubamine</span><span class="sxs-lookup"><span data-stu-id="b212c-172">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="b212c-173">Antud jaotises kirjeldatud funktsioonide kasutamiseks peate kasutama [funktsioonihaldust](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), et lülitada sisse järgmised funktsioonid (samas järjekorras).</span><span class="sxs-lookup"><span data-stu-id="b212c-173">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="b212c-174">Töökaardi vahendile on lisatud lõpetatuks märkimise litsentsiplaat</span><span class="sxs-lookup"><span data-stu-id="b212c-174">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="b212c-175">Identifitseerimisnumbri automaatse genereerimise lubamine lõpetamisest teatamisel töökaardi vahendis</span><span class="sxs-lookup"><span data-stu-id="b212c-175">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="b212c-176">Sildi printimine töökaardi vahendilt</span><span class="sxs-lookup"><span data-stu-id="b212c-176">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="b212c-177">Litsentsiplaadile lõpetamisest teatamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="b212c-177">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="b212c-178">Selleks, et kontrollida, kas töötajad peaksid koguste lõpetamisest teatamisel kasutama olemasolevat litsentsiplaati või looma uue litsentsiplaadi, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b212c-178">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="b212c-179">Avage **Tootmise juhtimine \> Seadistus \> Tootmise käivitamine \> Töökaardi konfigureerimine seadmetele**.</span><span class="sxs-lookup"><span data-stu-id="b212c-179">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="b212c-180">Määrake igale seadmele järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="b212c-180">Set the following options for each device:</span></span>

    - <span data-ttu-id="b212c-181">**Loo litsentsiplaat** – seadke suvandi väärtuseks **Jah**, et luua iga lõpetamisest teatamise korral uus litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="b212c-181">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="b212c-182">Seadke väärtuseks **Ei**, kui iga lõpetamisest kinnitamise korral tuleks kasutada olemasolevat litsentsiplaati.</span><span class="sxs-lookup"><span data-stu-id="b212c-182">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="b212c-183">**Prindi silt** – seadke suvandi väärtuseks **Jah**, kui töötaja peab printima iga lõpetamisest kinnitamise jaoks litsentsiplaadi sildi.</span><span class="sxs-lookup"><span data-stu-id="b212c-183">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="b212c-184">Kui silti pole vaja, siis seadke väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="b212c-184">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="b212c-185">![Töökaardi konfigureerimine seadmete lehe jaoks](media/config-job-card-raf.png "Töökaardi konfigureerimine seadmete lehe jaoks")</span><span class="sxs-lookup"><span data-stu-id="b212c-185">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="b212c-186">Sildi konfigureerimiseks avage **Laohaldus \> Seadistus \> Dokumendi marsruudivalik \> Dokumendi marsruudivalik**.</span><span class="sxs-lookup"><span data-stu-id="b212c-186">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="b212c-187">Lisateavet vt teemast [Litsentsiplaadi printimise lubamine](../warehousing/tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="b212c-187">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>
