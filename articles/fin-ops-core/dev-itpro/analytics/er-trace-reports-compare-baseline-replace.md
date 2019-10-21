---
title: Täiustused loodud elektroonilise aruandluse aruannete tulemuste jälgimises ja nende võrdlemises alusväärtustega
description: Selles teemas kirjeldatakse, kuidas elektroonilise aruandluse alusfunktsiooni on täiustatud rakenduse Microsoft Dynamics 365 for Finance and Operations versioonis 10.0.3 (juuni 2019).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: a260be0f8659106907b26bf69bee3b33b09d0c24
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181331"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="1a6f6-103">Täiustused loodud elektroonilise aruandluse aruannete tulemuste jälgimises ja nende võrdlemises alusväärtustega</span><span class="sxs-lookup"><span data-stu-id="1a6f6-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1a6f6-104">Selles teemas kirjeldatakse esimest täiustuste kogumit, mis on tehtud elektroonilise aruandluse raamistiku alusfunktsioonis.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="1a6f6-105">Need täiustused on saadaval rakenduse Microsoft Dynamics 365 for Finance and Operations versioonis 10.0.3 (juuni 2019) ja uuemates versioonides.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="1a6f6-106">Alusreeglite seadistamise automatiseerimine</span><span class="sxs-lookup"><span data-stu-id="1a6f6-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="1a6f6-107">Teemas [Loodud aruandetulemite jälgimine ja nende võrdlemine alusväärtustega](er-trace-reports-compare-baseline.md) kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse raamistikku nii, et see koguks teavet elektroonilise aruandluse vormingu käivitamiste kohta ja hindaks nende käivitamiste tulemusi.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="1a6f6-108">Selle teema näites on toodud etapid, mis tuleb läbida.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="1a6f6-109">Siin on mõned neist etappidest.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-109">Here are some of the steps:</span></span>

- <span data-ttu-id="1a6f6-110">Käivitage elektroonilise aruandluse vorming väljamineva faili loomiseks ja salvestage fail lokaalselt.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="1a6f6-111">Lisage lokaalselt salvestatud fail manusena alusele, mis lisati elektroonilise aruandluse vormingu jaoks.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="1a6f6-112">Konfigureerige alusreeglit lisatud aluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="1a6f6-113">See konfiguratsioon sisaldab järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="1a6f6-114">Määrake elektroonilise aruandluse vormingu element, mida kasutatakse väljamineva faili loomiseks.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="1a6f6-115">Valige manus, mis viitab loodud väljaminevale failile.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="1a6f6-116">Need sammud tuleb läbida käsitsi, kuigi elektroonilise aruandluse uute võimalustega on neid võimalik automatiseerida.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="1a6f6-117">Lisateabe saamiseks selle funktsiooni kohta läbige järgmine näide.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="1a6f6-118">Näide. Alusreeglite seadistamise automatiseerimine</span><span class="sxs-lookup"><span data-stu-id="1a6f6-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="1a6f6-119">Selle näite etappide läbimiseks peate kõigepealt läbima etapid näites teemas [Loodud aruandetulemite jälgimine ja nende võrdlemine alusväärtustega](er-trace-reports-compare-baseline.md) kuni jaotiseni „Uue aluse lisamine kujundatud elektroonilise aruande vormingu jaoks”.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="1a6f6-120">Lisatud aluse ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="1a6f6-120">Review added baseline</span></span>

1. <span data-ttu-id="1a6f6-121">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="1a6f6-122">Valige suvand **Alused**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1a6f6-123">Nupp **Alused** toimingupaanil on saadaval vaid siis, kui elektroonilise aruandluse kasutaja parameeter **Käivita silumisrežiimis** on praeguse ettevõtte jaoks sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="1a6f6-124">Alus on lisatud valitud vormingu **Vorming elektroonilise aruandluse aluste õppimiseks** jaoks, aga alusreegleid pole veel selle aluse jaoks lisatud.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="1a6f6-125">![Elektroonilise aruandluse vormingu aluste leht](media/GER-BaselineSample-AddBaseline2.PNG "Elektroonilise aruandluse vormingu aluste lehe kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="1a6f6-125">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="1a6f6-126">Uue alusreegli tegemine</span><span class="sxs-lookup"><span data-stu-id="1a6f6-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="1a6f6-127">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="1a6f6-128">Laiendage puul suvandit **Elektroonilise aruandluse aluste õppimise mudel**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="1a6f6-129">Valige puus suvandid **Elektroonilise aruandluse aluste õppimise mudel\\Vorming elektroonilise aruandluse aluste õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="1a6f6-130">Kiirkaardil **Versioonid** valige käsk **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="1a6f6-131">Sisestage väljale **Sisestage ID** väärtus **1**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="1a6f6-132">Määrake suvand **Alusfailide tegemine** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="1a6f6-133">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-133">Select **OK**.</span></span>

    <span data-ttu-id="1a6f6-134">![Elektroonilise aruande parameetrite dialoogiaken](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Elektroonilise aruande parameetrite dialoogiakna kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="1a6f6-134">![Electronic report parameters dialog box](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Screenshot of the Electronic report parameters dialog box")</span></span>

8. <span data-ttu-id="1a6f6-135">Valige suvand **Alused**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-135">Select **Baselines**.</span></span>

    <span data-ttu-id="1a6f6-136">![Elektroonilise aruandluse vormingu aluste leht](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Elektroonilise aruandluse vormingu aluste lehe kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="1a6f6-136">![Electronic reporting format baselines page](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="1a6f6-137">Loodud väljaminev fail manustatakse automaatselt käivitatud elektroonilise aruandluse vormingu alusele.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-137">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="1a6f6-138">Alusreegel on sellele alusele automaatselt lisatud ja sisaldab ka viidet manustatud failile.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-138">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="1a6f6-139">Väljale **Nimi** sisestage **Alus 1**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-139">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="1a6f6-140">Sisestage väljale **Failinime mask** väärtus **.xml**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-140">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="1a6f6-141">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-141">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="1a6f6-142">Vormingu käivitamine</span><span class="sxs-lookup"><span data-stu-id="1a6f6-142">Run the format</span></span>

<span data-ttu-id="1a6f6-143">Nüüd olete valmis läbima ülejäänud sammud näites teemas [Loodud aruandetulemite jälgimine ja nende võrdlemine alusväärtustega](er-trace-reports-compare-baseline.md), alustades jaotisest „Kujundatud elektroonilise aruandluse vormingu käitamine ja logi ülevaatamine tulemuste analüüsimiseks”.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-143">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="1a6f6-144">Kui kustutate automaatselt lisatud alusreegli kiirkaardilt **Alused**, ei kustutata viidatud manust automaatselt.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-144">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="1a6f6-145">Aluse konfigureerimine nii, et see eiraks elektroonilise aruandluse väljundi pidevalt muutuvaid osasid</span><span class="sxs-lookup"><span data-stu-id="1a6f6-145">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="1a6f6-146">Kui elektroonilise aruandluse vorming on kujundatud sisaldama teavet, mis muutub vormingu käivitamisel, peab vormingul olema kohustus kasutada elektroonilise aruandluse alusfunktsiooni loodud tulemuste võrdlemiseks alusväärtustega.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-146">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="1a6f6-147">Näiteks võib teave olla töötlemiskuupäev ja -kellaaeg või eri vormingutes loodud dokumendi kordumatu ID (globaalne ainuidentifikaator \[GUID\] jne).</span><span class="sxs-lookup"><span data-stu-id="1a6f6-147">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="1a6f6-148">Elektroonilise aruandluse uue võimalusega saate konfigureerida alusreeglit nii, et see eirab elektroonilise aruandluse vormingu muudetavaid elemente, kui vormingut käivitatakse eesmärgiga võrrelda alusväärtusi vormingu käivitamise tulemustega.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-148">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="1a6f6-149">Lisateabe saamiseks selle funktsiooni kohta läbige järgmine näide.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-149">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="1a6f6-150">Näide. Aluse konfigureerimine nii, et see eiraks elektroonilise aruandluse väljundi pidevalt muutuvaid osasid</span><span class="sxs-lookup"><span data-stu-id="1a6f6-150">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="1a6f6-151">Selle näite etappide läbimiseks peate kõigepealt läbima etapid näites teemas [Loodud aruandetulemite jälgimine ja nende võrdlemine alusväärtustega](er-trace-reports-compare-baseline.md).</span><span class="sxs-lookup"><span data-stu-id="1a6f6-151">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="1a6f6-152">Konfigureeritud elektroonilise aruandluse vormingu muutmine</span><span class="sxs-lookup"><span data-stu-id="1a6f6-152">Modify a configured ER format</span></span>

1. <span data-ttu-id="1a6f6-153">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-153">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="1a6f6-154">Laiendage puul suvandit **Elektroonilise aruandluse aluste õppimise mudel**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-154">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="1a6f6-155">Valige puus suvandid **Elektroonilise aruandluse aluste õppimise mudel\\Vorming elektroonilise aruandluse aluste õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-155">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="1a6f6-156">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-156">Select **Designer**.</span></span>
5. <span data-ttu-id="1a6f6-157">Valige puul suvand **Väljund\\Dokument**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-157">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="1a6f6-158">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-158">Select **Add**.</span></span>
7. <span data-ttu-id="1a6f6-159">Dialoogiakna ripploendist puul valige suvandid **XML\\Atribuut**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-159">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="1a6f6-160">Välja **Nimi** sisestage väärtus **ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-160">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="1a6f6-161">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-161">Select **OK**.</span></span>
10. <span data-ttu-id="1a6f6-162">Vahekaardilt **Vastendamine** puul valige suvandid **Väljund\\Dokument\\ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-162">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="1a6f6-163">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-163">Select **Edit formula**.</span></span>
12. <span data-ttu-id="1a6f6-164">Sisestage väljale **Valem** järgmine avaldis: **DATETIMEFORMAT(NOW(), "O")**</span><span class="sxs-lookup"><span data-stu-id="1a6f6-164">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="1a6f6-165">Valige nupp **Salvesta** ja seejärel suvand **Katse**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-165">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="1a6f6-166">Valige uuesti suvand **Katse**, et konfigureeritud avaldist uuesti kontrollida.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-166">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="1a6f6-167">![Valemikoostaja leht](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Valemikoostaja lehe kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="1a6f6-167">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="1a6f6-168">Vahekaardil **Katsetulemus** näidatakse, et konfigureeritud avaldis annab käivitamisel alati tulemuseks erineva kuupäeva ja kellaaja väärtuse.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-168">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="1a6f6-169">Sulgege leht **Valemikoostaja** ja valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-169">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="1a6f6-170">![Vormingu koostaja leht](media/GER-BaselineSample-FormatMappingDesign2.PNG "Vormingu koostaja lehe kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="1a6f6-170">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="1a6f6-171">Sulgege **Vormingu koostaja** leht.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-171">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="1a6f6-172">Olemasoleva alusreegli eemaldamine</span><span class="sxs-lookup"><span data-stu-id="1a6f6-172">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="1a6f6-173">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-173">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="1a6f6-174">Valige suvand **Alused**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-174">Select **Baselines**.</span></span>
3. <span data-ttu-id="1a6f6-175">Aluste loendist valige alus, mis on konfigureeritud vormingu **Vorming elektroonilise aruandluse aluste õppimiseks** jaoks.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-175">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="1a6f6-176">Kiirkaardilt **Alused** valige käsk **Kustuta**, et eemaldada varem konfigureeritud alusreegel.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-176">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="1a6f6-177">![Elektroonilise aruandluse vormingu aluste leht](media/GER-BaselineSample-AddBaseline3.PNG "Elektroonilise aruandluse vormingu aluste lehe kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="1a6f6-177">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="1a6f6-178">Kujundatud elektroonilise aruandluse vormingu sidumiste asenduste määratlemine</span><span class="sxs-lookup"><span data-stu-id="1a6f6-178">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="1a6f6-179">Valige lehel **Konfiguratsioonid** kiirkaardil **Asendused** suvand **Komponentide valimine**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-179">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="1a6f6-180">Laiendage Vormingu komponentide puul suvandit **Väljund**, laiendage suvandeid **Väljund\\Dokument** ja seejärel valige suvandi **Väljund\\Dokument\\ProcessingDateTime** märkeruut.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-180">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>

    <span data-ttu-id="1a6f6-181">![Komponentide dialoogiakna valimine](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Komponentide dialoogiakna valimise kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="1a6f6-181">![Select Components dialog box](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Screenshot of the Select Components dialog box")</span></span>

3. <span data-ttu-id="1a6f6-182">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-182">Select **OK**.</span></span>

<span data-ttu-id="1a6f6-183">![Elektroonilise aruandluse vormingu aluste leht](media/GER-BaselineSample-AddBaseline4.PNG "Elektroonilise aruandluse vormingu aluste lehe kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="1a6f6-183">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="1a6f6-184">Valitud elektroonilise aruandluse vormingu komponent on lisatud komponentide loendisse kiirkaardil **Asendused**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-184">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="1a6f6-185">Kui aluse elektroonilise aruandluse vorming käivitatakse silumisrežiimis, asendatakse vormingu sidumine iga komponendi jaoks veerus **Sidumine** kuvatud sidumisega.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-185">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="1a6f6-186">Kiirkaardil **Asendused** loendatud komponendi vaikesidumise muutmiseks valige nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-186">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="1a6f6-187">Uue alusreegli tegemine</span><span class="sxs-lookup"><span data-stu-id="1a6f6-187">Make a new baseline rule</span></span>

<span data-ttu-id="1a6f6-188">Järgige etappe selle teema jaotises „Näide. Alusreeglite seadistamise automatiseerimine”.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-188">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="1a6f6-189">Teatis hoiatab teid, et väljaminev fail on loodud, kasutades alussätteid, ja et tekkinud on vormingu sidumiste sundasendamine.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-189">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="1a6f6-190">![Teatis konfiguratsioonide lehel](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Kuvatõmmis teatisest konfiguratsioonide lehel")</span><span class="sxs-lookup"><span data-stu-id="1a6f6-190">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="1a6f6-191">Vormingu sidumiste asendamise hoiatuste peitmine</span><span class="sxs-lookup"><span data-stu-id="1a6f6-191">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="1a6f6-192">Konkreetsete elektroonilise aruandluse parameetrite seadistamisega saate peita teatiseid, mis annavad hoiatusi vormingu sidumiste asendamise kohta.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-192">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="1a6f6-193">See võib olla kasulik, kui vormingu sidumised asendatakse järelevalveta režiimis, kasutades tööriista Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-193">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="1a6f6-194">Sellisel juhul võib hoiatust pidada käimasoleva testjuhtumi tõrkeks.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-194">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="1a6f6-195">Valige lehe **Konfiguratsioonid** toimingupaani vahekaardilt **Konfiguratsioonid** suvand **Kasutaja parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="1a6f6-196">Seadistage suvand **Aluse hoiatuste peitmine** valikule **Jah** ja klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-196">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

<span data-ttu-id="1a6f6-197">![Kasutaja parameetrite dialoogiaken](media/GER-BaselineSample-ERUserParameters1.png "Kasutaja parameetrite dialoogiakna kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="1a6f6-197">![User parameters dialog box](media/GER-BaselineSample-ERUserParameters1.png "Screenshot of the User parameters dialog box")</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="1a6f6-198">Vaadake genereeritud alusfail üle.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-198">Review the generated baseline file</span></span>

1. <span data-ttu-id="1a6f6-199">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-199">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="1a6f6-200">Valige suvand **Alused**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-200">Select **Baselines**.</span></span>
3. <span data-ttu-id="1a6f6-201">Valige suvand **Manused**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-201">Select **Attachments**.</span></span>

    <span data-ttu-id="1a6f6-202">![Manuste leht](media/GER-BaselineSample-AttachedBaselineFile.PNG "Manuste lehe kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="1a6f6-202">![Attachments page](media/GER-BaselineSample-AttachedBaselineFile.PNG "Screenshot of the Attachments page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="1a6f6-203">Loodud fail sisaldab töötlemise kuupäeva ja kellaaja teksti (**"#"**) sidumisest, mis konfigureeriti lisatud alusreeglis, mitte vormingu sidumisest.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-203">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>

4. <span data-ttu-id="1a6f6-204">Sulgege leht **Manused**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-204">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="1a6f6-205">Kujundatud elektroonilise aruandluse vormingu käitamine ja logi ülevaatamine tulemuste analüüsimiseks</span><span class="sxs-lookup"><span data-stu-id="1a6f6-205">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="1a6f6-206">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-206">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="1a6f6-207">Laiendage puul suvandit **Elektroonilise aruandluse aluste õppimise mudel**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-207">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="1a6f6-208">Valige puus suvandid **Elektroonilise aruandluse aluste õppimise mudel\\Vorming elektroonilise aruandluse aluste õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-208">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="1a6f6-209">Kiirkaardil **Versioonid** valige käsk **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-209">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="1a6f6-210">Sisestage väljale **Sisestage ID** väärtus **1**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-210">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="1a6f6-211">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-211">Select **OK**.</span></span>
7. <span data-ttu-id="1a6f6-212">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsiooni silumislogid**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-212">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="1a6f6-213">Käivituslogi sisaldab teavet loodud faili ja konfigureeritud aluse võrdluse tulemusi.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-213">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="1a6f6-214">Logi näitab, et loodud fail ja alus on võrdsed, kuigi käivitatud vorming sisaldab sidumist pidevalt muutuva kuupäeva ja kellaaja väärtuse sisestamiseks väljaminevasse faili.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-214">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="1a6f6-215">Kuigi väljaminev fail on loodud, kasutades alussätteid, mis käivitavad vormingu sidumiste sundasenduse, ei saa te asendamise kohta hoiatusi.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-215">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="1a6f6-216">Alussätete vahetamine keskkondade vahel</span><span class="sxs-lookup"><span data-stu-id="1a6f6-216">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="1a6f6-217">Alussätete eksportimine</span><span class="sxs-lookup"><span data-stu-id="1a6f6-217">Export baseline settings</span></span>

<span data-ttu-id="1a6f6-218">Elektroonilise aruandluse uute võimalustega saate eksportida alussätteid valitud elektroonilise aruandluse vormingu jaoks praegusest keskkonnast ja salvestada need XML-failidena.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-218">The new ER capabilities let you export baseline settings for the selected ER format from the current environment and store them as XML files.</span></span> 

<span data-ttu-id="1a6f6-219">Alussätete eksportimiseks valige lehel **Elektroonilise aruandluse vormingu alused** käsk **Ekspordi**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-219">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="1a6f6-220">Impordi alussätted</span><span class="sxs-lookup"><span data-stu-id="1a6f6-220">Import baseline settings</span></span>

<span data-ttu-id="1a6f6-221">Eksporditud alussätteid saab importida teise keskkonda.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-221">Exported baseline settings can be imported into a different environment.</span></span> <span data-ttu-id="1a6f6-222">Keskkond tuleb kõigepealt importida elektroonilise aruandluse vorminguna.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-222">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="1a6f6-223">Seejärel saate importida alussätteid.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-223">You can then import the baseline settings.</span></span>

<span data-ttu-id="1a6f6-224">Alussätete importimiseks lokaalselt salvestatud XML-failist valige lehel **Elektroonilise aruandluse vormingu alused** käsk **Impordi** ja seejärel käsk **Sirvi**, et valida XML-fail.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-224">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="1a6f6-225">![Alussätete importimise dialoogiaken](media/GER-BaselineSample-ImportBaseline1.PNG "Alussätete importimise dialoogiakna kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="1a6f6-225">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="1a6f6-226">Alussätete importimiseks Microsoft SharePoint Serverisse salvestatud XML-failist praeguste dokumendihalduse sätete ja valitud dokumendi tüübi põhjal valige lehel **Elektroonilise aruandluse vormingu alused** käsk **Impordi allikast**.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-226">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="1a6f6-227">Seejärel valige dokumendi tüüp ja XML-fail.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-227">Then select the document type and the XML file.</span></span> <span data-ttu-id="1a6f6-228">SharePointi kaustale ligipääsemiseks vajalik dokumendi tüüp peab olema varem konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-228">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="1a6f6-229">![Allikast importimise dialoogiaken](media/GER-BaselineSample-ImportBaseline2.PNG "Allikast importimise dialoogiakna kuvatõmmis")</span><span class="sxs-lookup"><span data-stu-id="1a6f6-229">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="1a6f6-230">Dialoogiaknast **Allikast importimine** vajaliku dokumendi tüübi ja faili nime valimise etappide salvestamiseks saate kasutada tegevuse salvestajat.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-230">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="1a6f6-231">Nii saate säilitada vajalikke alussätteid SharePointi serveris ja seejärel need automaatselt importida, esitades tegevuse salvestist automaatsete katsete käivitamisel tööriistaga Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="1a6f6-231">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1a6f6-232">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1a6f6-232">Additional resources</span></span>

- [<span data-ttu-id="1a6f6-233">Loodud aruandetulemite jälgimine ja nende võrdlemine alusväärtustega</span><span class="sxs-lookup"><span data-stu-id="1a6f6-233">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="1a6f6-234">Ülesande salvestaja</span><span class="sxs-lookup"><span data-stu-id="1a6f6-234">Task recorder</span></span>](../user-interface/task-recorder.md)
