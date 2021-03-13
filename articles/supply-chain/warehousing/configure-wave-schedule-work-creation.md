---
title: Voo ajal töö loomise plaanimine
description: Selles teemas kirjeldatakse, kuidas häälestada ja kasutada töö loomise plaanimise voo töötlemismeetodit.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ed8f43c7db139b7b16ac6901d5db56ba2f021690
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078252"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="39fa3-103">Voo ajal töö loomise plaanimine</span><span class="sxs-lookup"><span data-stu-id="39fa3-103">Schedule work creation during wave</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39fa3-104">Kasutage funktsiooni *Töö loomise plaanimine* osana oma voo loomisprotsessist, et aidata suurendada voo töötlemise läbilasku, võimaldades süsteemil luua tööd paralleeltöötlust kasutades.</span><span class="sxs-lookup"><span data-stu-id="39fa3-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="39fa3-105">Kui see funktsioon on lubatud, luuakse plaanitud töö automaatselt, mida süsteem lõpuks töötleb, et luua tegelik töö.</span><span class="sxs-lookup"><span data-stu-id="39fa3-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="39fa3-106">Kui voo laadimise ridade arv saavutab ettemääratud läviväärtuse, loob süsteem tegeliku töö palju kiiremini, rakendades paralleelset asünkroonset töötlemist.</span><span class="sxs-lookup"><span data-stu-id="39fa3-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="enable-the-schedule-work-creation-feature"></a><span data-ttu-id="39fa3-107">Töö loomise plaanimise funktsiooni lubamine</span><span class="sxs-lookup"><span data-stu-id="39fa3-107">Enable the Schedule work creation feature</span></span>

### <a name="enable-the-feature-in-feature-management"></a><span data-ttu-id="39fa3-108">Funktsiooni lubamine funktsioonihalduses</span><span class="sxs-lookup"><span data-stu-id="39fa3-108">Enable the feature in feature management</span></span>

<span data-ttu-id="39fa3-109">Enne funktsiooni *Töö loomise plaanimine* kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="39fa3-109">Before you can use the *Schedule work creation* feature, it must be turned on in your system.</span></span> <span data-ttu-id="39fa3-110">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="39fa3-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="39fa3-111">Seega on funktsioon loetletud järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="39fa3-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="39fa3-112">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="39fa3-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="39fa3-113">**Funktsiooni nimi:** *Töö loomise plaanimine*</span><span class="sxs-lookup"><span data-stu-id="39fa3-113">**Feature name:** *Schedule work creation*</span></span>

> [!NOTE]
> <span data-ttu-id="39fa3-114">Enne *töö loomise plaanimise* lubamist peab funktsioon *Organisatsiooniülene töö blokeerimine* olema sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="39fa3-114">The *Organization-wide work blocking* feature must be enabled before you can enable *Schedule work creation*.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="39fa3-115">Voogude pakett-töötluse käsitsi lubamine</span><span class="sxs-lookup"><span data-stu-id="39fa3-115">Manually enable batch processing of waves</span></span>

<span data-ttu-id="39fa3-116">Laotöö loomiseks paralleelse asünkroonse meetodi kasutamiseks peab teie voo protsess olema käivitatud partiina.</span><span class="sxs-lookup"><span data-stu-id="39fa3-116">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="39fa3-117">Selle häälestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="39fa3-117">To set this up:</span></span>

1. <span data-ttu-id="39fa3-118">Avage  **Laohaldus\>Seadistus \> Laohalduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="39fa3-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>

1. <span data-ttu-id="39fa3-119">Vahekaardil **Üldine** määrake suvand **Töötle vooge pakett-töötlusega** valikule *Jah*.</span><span class="sxs-lookup"><span data-stu-id="39fa3-119">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="39fa3-120">Soovi korral saate valida ka sihtotstarbelise **voo töötlemise pakett-tööde grupi**, et vältida pakett-töötluse järjekorra käitamist teiste protsessidega samal ajal.</span><span class="sxs-lookup"><span data-stu-id="39fa3-120">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>

1. <span data-ttu-id="39fa3-121">Määrake syvandi **Oota lukustust (ms)** aeg, mis kohaldub, kui süsteem töötleb mitut voogu samal ajal.</span><span class="sxs-lookup"><span data-stu-id="39fa3-121">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="39fa3-122">Enamike suuremate laine loomisprotsesside puhul soovitame väärtus *60 000*.</span><span class="sxs-lookup"><span data-stu-id="39fa3-122">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="39fa3-123">Olemasolevate voomallide uue voo etapi meetodi käsitsi lubamine</span><span class="sxs-lookup"><span data-stu-id="39fa3-123">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="39fa3-124">Alustage uue voo etapi meetodi loomisega ja selle lubamisega paralleelse asünkroonse ülesande töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="39fa3-124">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="39fa3-125">Avage jaotis  **Laohaldus \>Seadistus \> Vood \> Voo töötlemise meetodid**.</span><span class="sxs-lookup"><span data-stu-id="39fa3-125">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>

1. <span data-ttu-id="39fa3-126">Valige  **Meetodite uuesti loomine** ja pange tähele, et *WHSScheduleWorkCreationWaveStepMethod* on lisatud voo töötlemise meetodite loendisse, mida saate oma saatmise voomallides kasutada.</span><span class="sxs-lookup"><span data-stu-id="39fa3-126">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>

1. <span data-ttu-id="39fa3-127">Valige kirje **meetodi nimega** *WHSScheduleWorkCreationWaveStepMethod* ja valige suvand **Ülesande konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="39fa3-127">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>

1. <span data-ttu-id="39fa3-128">Ruudustikku uue rea loomiseks valige tegevuspaanil **Uus** ja kasutage järgmisi sätteid.</span><span class="sxs-lookup"><span data-stu-id="39fa3-128">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="39fa3-129">**Ladu** – valige ladu, mida töö loomise töötlemise plaanimiseks kasutate.</span><span class="sxs-lookup"><span data-stu-id="39fa3-129">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>

    - <span data-ttu-id="39fa3-130">**Pakett-tööde maksimaalne arv** – määrake pakett-tööde maksimaalne arv.</span><span class="sxs-lookup"><span data-stu-id="39fa3-130">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="39fa3-131">Enamasti peaks see väärtus olema vahemikus 8–16, kuid soovitame katsetada teie stsenaariumitel põhineva optimaalse seadistusega.</span><span class="sxs-lookup"><span data-stu-id="39fa3-131">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>

    - <span data-ttu-id="39fa3-132">**Voo töötlemise partii rühm** – valige oma partii järjekorra töötlemise optimeerimiseks sihtotstarbeline voo töötlemise partii grupp.</span><span class="sxs-lookup"><span data-stu-id="39fa3-132">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="39fa3-133">Nüüd olete valmis värskendama olemasolevat voomalli (või looma uue), et kasutada voo töötlemismeetodit *Töö loomise plaanimine*.</span><span class="sxs-lookup"><span data-stu-id="39fa3-133">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="39fa3-134">Avage **Laohaldus\>Seadistus \> Vood \> Voomallid**.</span><span class="sxs-lookup"><span data-stu-id="39fa3-134">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>

1. <span data-ttu-id="39fa3-135">Valige toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="39fa3-135">Select **Edit** on the Action Pane.</span></span>

1. <span data-ttu-id="39fa3-136">Valige loendipaanil voomall, mida soovite värskendada (kui testite demoandmeid kasutades, võite kasutada *24 saadetise vaikemalli*).</span><span class="sxs-lookup"><span data-stu-id="39fa3-136">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>

1. <span data-ttu-id="39fa3-137">Laiendage kiirkaarti **Meetodid** ja valige rida **nimega** *Töö loomise plaanimine* ruudustikus **Ülejäänud meetodid**.</span><span class="sxs-lookup"><span data-stu-id="39fa3-137">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>

1. <span data-ttu-id="39fa3-138">Valige nool, mis osutab veerule **Valitud meetodid**, et teisaldada valitud rida sellesse veergu.</span><span class="sxs-lookup"><span data-stu-id="39fa3-138">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="39fa3-139">(Teil saab olla korraga ainult üks valitud meetod, mis kasuab kas suvandit *WHSScheduleWorkCreationWaveStepMethod* või *createWork*, seega olemasolev rida **meetodi nimega** *createWork* teisaldatakse aytomaatselt ruudustikku **Ülejäänud meetodid**.)</span><span class="sxs-lookup"><span data-stu-id="39fa3-139">(You can only have one selected method at a time that uses either *WHSScheduleWorkCreationWaveStepMethod* or *createWork*, so the existing row with **Method name** *createWork* is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="39fa3-140">Voo ülesande töötlemise lävendi andmete määramine</span><span class="sxs-lookup"><span data-stu-id="39fa3-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="39fa3-141">Voo töötlemise esimest korda käitamisel kasutades mis tahes ülesandepõhist töötlemist loob süsteem vaikimisi voo ülesande töötlemise lävendi andmed.</span><span class="sxs-lookup"><span data-stu-id="39fa3-141">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="39fa3-142">Andmeid kasutatakse voo töötluse asünkroonse ja ülesandepõhise töötluse juhtimiseks, mis võimaldab sellel töödelda ja luua tööd paralleelselt.</span><span class="sxs-lookup"><span data-stu-id="39fa3-142">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="39fa3-143">Vaikeandmed kasutavad algselt koormusridade minimaalse arvu läviväärtusena väärtust 15 (MINIMUMWAVELOADLINES).</span><span class="sxs-lookup"><span data-stu-id="39fa3-143">The default data will initially use a threshold value of 15 for the minimum number of load lines (MINIMUMWAVELOADLINES).</span></span> <span data-ttu-id="39fa3-144">See tähendab, et kui süsteem töötleb voogu enam kui 15 koormusreaga, kasutab see asünkroonset ülesande töötlemist.</span><span class="sxs-lookup"><span data-stu-id="39fa3-144">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="39fa3-145">Saate neid andmeid katsekeskkonnas tabelisse **WHSWaveTaskProcessingThresholdParameters** käsitsi sisestada/värskendada, kuid kui peate seda sätet töökeskkonnas muutma, peate värskendamise taotlemiseks võtma ühendust Microsofti toega.</span><span class="sxs-lookup"><span data-stu-id="39fa3-145">You can manually insert/update this data in the **WHSWaveTaskProcessingThresholdParameters** table in your test environments, but if you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-feature"></a><span data-ttu-id="39fa3-146">Funktsiooniga töötamine</span><span class="sxs-lookup"><span data-stu-id="39fa3-146">Work with the feature</span></span>

<span data-ttu-id="39fa3-147">Kui funktsioon *Töö loomise plaanimine* on lubatud, loob voo töötlemine plaanitud töö, mida kasutatakse lõpuks uue töö loomisprotsessi poolt.</span><span class="sxs-lookup"><span data-stu-id="39fa3-147">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="39fa3-148">Töö loomise ajal töö blokeeritakse, kasutades funktsiooni *Organisatsiooniülene töö blokeerimine*.</span><span class="sxs-lookup"><span data-stu-id="39fa3-148">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span>

<span data-ttu-id="39fa3-149">Järgmine vooskeem näitab, kuidas plaanitud tööd laine töötlemise ajal luuakse.</span><span class="sxs-lookup"><span data-stu-id="39fa3-149">The following flowchart shows how planned work is created during wave processing.</span></span>

![Töö loomise graafik](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="39fa3-151">Plaanitud töö</span><span class="sxs-lookup"><span data-stu-id="39fa3-151">Planned work</span></span>

<span data-ttu-id="39fa3-152">Leht **Plaanitud töö üksikasjad** (**Laohaldus \> Töö \> Plaanitud töö üksikasjad**) näitab teavet plaanitud töö kohta, mis voo töötlemise ajal algselt luuakse.</span><span class="sxs-lookup"><span data-stu-id="39fa3-152">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="39fa3-153">Saadaval on järgmised suvandi **Protsessi olek** väärtused.</span><span class="sxs-lookup"><span data-stu-id="39fa3-153">The following **Process status** values are available:</span></span>

- <span data-ttu-id="39fa3-154">**Järjekorras** – plaanitud töö on töö loomiseks kasutamiseks ootel.</span><span class="sxs-lookup"><span data-stu-id="39fa3-154">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="39fa3-155">**Lõpetatud** – plaanitud töä on töö loomiseks kasutatud.</span><span class="sxs-lookup"><span data-stu-id="39fa3-155">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="39fa3-156">**Nurjus** – voo töötlemine nurjus.</span><span class="sxs-lookup"><span data-stu-id="39fa3-156">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="39fa3-157">Pange tähele, et plaanitud töö võib olla olekus **Nurjunud** koos või ilma seotud tegeliku tööta.</span><span class="sxs-lookup"><span data-stu-id="39fa3-157">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="39fa3-158">Kui tegeliku töö loomise protsess nurjub, jääb tegelik töö olekusse *Tühistatud*.</span><span class="sxs-lookup"><span data-stu-id="39fa3-158">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="39fa3-159">Töö loomisprotsessi pakett-töö</span><span class="sxs-lookup"><span data-stu-id="39fa3-159">Batch job for the work creation process</span></span>

<span data-ttu-id="39fa3-160">Töötlemise voogude pakett-tööde vaatamiseks valige tegevuspaanil **Pakett-tööd** lehel **Kõik vood**.</span><span class="sxs-lookup"><span data-stu-id="39fa3-160">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="39fa3-161">Siit saate vaadata iga pakett-töö ID kohta kõiki partii ülesande üksikasju.</span><span class="sxs-lookup"><span data-stu-id="39fa3-161">From here, you can view all the batch task details for each of the batch job IDs.</span></span>
