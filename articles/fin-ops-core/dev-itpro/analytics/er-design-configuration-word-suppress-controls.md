---
title: Wordi sisu juhtelementide tühistamine loodud aruannetes
description: See teema kirjeldab, kuidas konfigureerida elektroonilise aruandluse (ER) vormingut, et luua aruandeid Microsoft Word failidena, kus sisu juhtelemendid on tõkestatud.
author: NickSelin
manager: AnnBe
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 81ad25514154dd8982aa4f849f0b2bfeb85270f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562114"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a><span data-ttu-id="8e613-103">Wordi sisu juhtelementide tühistamine loodud aruannetes</span><span class="sxs-lookup"><span data-stu-id="8e613-103">Suppress Word content controls in generated reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e613-104">Aruannete loomiseks Microsoft Word dokumentidena peate kujundama aruannete malli Wordi dokumendina.</span><span class="sxs-lookup"><span data-stu-id="8e613-104">To generate reports as Microsoft Word documents, you must design a template for the reports as a Word document.</span></span> <span data-ttu-id="8e613-105">See mall peab sisaldama Wordi sisu juhtelemente käitusajal sisestatava teabe kohatäitjatena.</span><span class="sxs-lookup"><span data-stu-id="8e613-105">This template must contain Word content controls as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="8e613-106">Wordi vormingus aruannete Wordi dokumendi mallina kasutamiseks saate [konfigureerida](er-design-configuration-word.md) uue [elektroonilise aruandluse (ER)](general-electronic-reporting.md) [lahenduse](er-quick-start1-new-solution.md).</span><span class="sxs-lookup"><span data-stu-id="8e613-106">To use the Word document that is created as a template for your reports, you can [configure](er-design-configuration-word.md) a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="8e613-107">See lahendus peab sisaldama ER-i [konfiguratsiooni](general-electronic-reporting.md#Configuration), mis sisaldab ER-i [vormingu](general-electronic-reporting.md#FormatComponentOutbound) komponenti.</span><span class="sxs-lookup"><span data-stu-id="8e613-107">The solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="8e613-108">See ER-vorming peab olema konfigureeritud kasutama aruande loomiseks loodud malli.</span><span class="sxs-lookup"><span data-stu-id="8e613-108">This ER format must be configured to use the designed template for report generation.</span></span>

<span data-ttu-id="8e613-109">Versioonis 10.0.6 ja Dynamics 365 Finance uuemates versioonides saate konfigureerida ER-vormingus valemeid, et saaks loodud dokumentides ära tõkestada Wordi sisu juhtelemente.</span><span class="sxs-lookup"><span data-stu-id="8e613-109">In version 10.0.6 and later of Dynamics 365 Finance, you can configure formulas in your ER format to suppress some Word content controls in generated documents.</span></span>

<span data-ttu-id="8e613-110">Järgmistes sammudes seletatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse funktsiooninõustaja rolliga kasutaja saab konfigureerida ER-vormingut, mis loob aruandeid Wordi failidena, ja summutavad mõned sisu juhtelemendid loodud aruannetes, mis on konfigureeritud Wordi malli abil.</span><span class="sxs-lookup"><span data-stu-id="8e613-110">The following steps explain how a user who is assigned to the System administrator or Electronic reporting functional consultant role can configure an ER format that generates reports as Word files and suppresses some of the content controls in the generated reports that have been configured by using a Word template.</span></span>

<span data-ttu-id="8e613-111">Neid samme saab teha ettevõtte GBSI.</span><span class="sxs-lookup"><span data-stu-id="8e613-111">These steps can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8e613-112">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="8e613-112">Prerequisites</span></span>

<span data-ttu-id="8e613-113">Toimingute teostamiseks tuleb esmalt läbida järgmised kolm tööjuhist:</span><span class="sxs-lookup"><span data-stu-id="8e613-113">To complete these steps, you must first complete the steps in the following task guides:</span></span>

- [<span data-ttu-id="8e613-114">OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine</span><span class="sxs-lookup"><span data-stu-id="8e613-114">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="8e613-115">ER-i konfiguratsioonide korduvkasutamine Exceli mallidega Wordi vormingus aruannete loomiseks</span><span class="sxs-lookup"><span data-stu-id="8e613-115">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)

<span data-ttu-id="8e613-116">Kui sooritate need ülesandejuhendite sammud, et ette valmistatakse järgmised kaubad:</span><span class="sxs-lookup"><span data-stu-id="8e613-116">When you complete the steps of these task guides, the following items are prepared:</span></span>

- <span data-ttu-id="8e613-117">**Töölehe näidisaruande** ER-vorming, mis on konfigureeritud dokumendi loomiseks Wordi vormingus</span><span class="sxs-lookup"><span data-stu-id="8e613-117">A **Sample worksheet report** ER format that is configured to generate a document in Word format</span></span>
- <span data-ttu-id="8e613-118">[Mustand](general-electronic-reporting.md#component-versioning) versioonist **näidisaruanne** ER-vormingus, mis on märgitud **käivitatavaks**</span><span class="sxs-lookup"><span data-stu-id="8e613-118">A [draft](general-electronic-reporting.md#component-versioning) version of the **Sample worksheet report** ER format that is marked as **Runnable**</span></span>
- <span data-ttu-id="8e613-119">Maksete **elektrooniline** meetod, mis on konfigureeritud kasutama hankija makse töötlemiseks **töölehe näidisaruande** ER-vormingut</span><span class="sxs-lookup"><span data-stu-id="8e613-119">An **Electronic** method of payments that is configured to use the **Sample worksheet report** ER format for vendor payment processing</span></span>

<span data-ttu-id="8e613-120">Peate näidisaruande jaoks alla laadima ja kohalikult salvestama ka järgmised mallid:</span><span class="sxs-lookup"><span data-stu-id="8e613-120">You must also download and save the following template for the sample report:</span></span>

- [<span data-ttu-id="8e613-121">Maksearuande 2 piiratud mall (SampleVendPaymDocReportBounded2.docx)</span><span class="sxs-lookup"><span data-stu-id="8e613-121">Bounded Template 2 of Payment Report (SampleVendPaymDocReportBounded2.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a><span data-ttu-id="8e613-122">Allalaaditud Wordi malli läbivaatamine</span><span class="sxs-lookup"><span data-stu-id="8e613-122">Review the downloaded Word template</span></span>

1. <span data-ttu-id="8e613-123">Avage Wordi desktop rakenduses **SampleVendPaymDocReportBounded2.docx** mallifail, mille varem alla laadisite.</span><span class="sxs-lookup"><span data-stu-id="8e613-123">In the Word desktop application, open the **SampleVendPaymDocReportBounded2.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="8e613-124">Kontrollige, et mallifail sisaldab kokkuvõtte jaotist, mis näitab maksete kogusummasid iga valuutakoodi kohta, mis on töödeldud maksetega täidetud.</span><span class="sxs-lookup"><span data-stu-id="8e613-124">Verify that the template file contains a summary section that shows the total payment amounts for every currency code that has been met in the processed payments.</span></span>

    - <span data-ttu-id="8e613-125">Kokkuvõtte jaotis asub Wordi dokumendi eraldi tabelis.</span><span class="sxs-lookup"><span data-stu-id="8e613-125">The summary section resides in a separate table of the Word document.</span></span>
    - <span data-ttu-id="8e613-126">Selle tabeli esimene rida sisaldab tabeliveergude päiseid.</span><span class="sxs-lookup"><span data-stu-id="8e613-126">The first row of this table holds the table columns headings as the section header.</span></span>
    - <span data-ttu-id="8e613-127">Selle tabeli teises reas on sektsiooni üksikasjadena korduv sisu juhtelement.</span><span class="sxs-lookup"><span data-stu-id="8e613-127">The second row of this table holds the repeating content control as the section details.</span></span>
    - <span data-ttu-id="8e613-128">See sisu juhtelement on vastendatud aruande **SummaryLines** välja **Aruanded** kohandatud XML-i osaga.</span><span class="sxs-lookup"><span data-stu-id="8e613-128">This content control is mapped to the **SummaryLines** field of the **Report** custom XML part.</span></span>
    - <span data-ttu-id="8e613-129">Selle vastendamise põhjal on sisu juhtelement seostatud redigeeritava **SummaryLines** ER-vormingu elemendiga.</span><span class="sxs-lookup"><span data-stu-id="8e613-129">Based on this mapping, the content control is associated with the **SummaryLines** element of the editable ER format.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e613-130">Korduv sisu kontroll on märgistatud **SummaryLines** võtmega, mis vastab kohandatud XML-i osaväljale, millele see on vastendatud.</span><span class="sxs-lookup"><span data-stu-id="8e613-130">The repeating content control is tagged by the **SummaryLines** key that matches the field of the custom XML part that it has been mapped to.</span></span>

    ![Word malli paigutus](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="8e613-132">Olemasoleva elektroonilise aruandluse aruande konfiguratsiooni valimine</span><span class="sxs-lookup"><span data-stu-id="8e613-132">Select the existing ER report configuration</span></span>

<span data-ttu-id="8e613-133">Järgmiste sammude puhul kasutate olemasolevat ER-i konfiguratsiooni, mille konfigureerisite pärast eelnevalt mainitud ülesandejuhendite sammude lõpuleviimist.</span><span class="sxs-lookup"><span data-stu-id="8e613-133">For the following steps, you will reuse the existing ER configuration that you configured when you completed the steps in the previously mentioned task guides.</span></span>

1. <span data-ttu-id="8e613-134">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="8e613-134">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="8e613-135">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="8e613-135">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="8e613-136">Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel** ja valige **Töölehe aruande näide**.</span><span class="sxs-lookup"><span data-stu-id="8e613-136">On the **Configurations** page, in the configuration tree, expand **Payment model**, and select **Sample worksheet report**.</span></span>
4. <span data-ttu-id="8e613-137">Valige **kujundaja** valitud ER-vormingu mustandversiooni redigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="8e613-137">Select **Designer** to edit the draft version of the selected ER format.</span></span>

## <a name="replace-the-current-template-with-the-new-template"></a><span data-ttu-id="8e613-138">Asendage olemasolev mall uue malliga</span><span class="sxs-lookup"><span data-stu-id="8e613-138">Replace the current template with the new template</span></span>

<span data-ttu-id="8e613-139">Praegu kasutatakse SampleVendPaymDocReportBounded.docx dokumenti mallina väljundi loomiseks Wordi vormingus.</span><span class="sxs-lookup"><span data-stu-id="8e613-139">Currently, the SampleVendPaymDocReportBounded.docx file is used as a template to generate the output in Word format.</span></span> <span data-ttu-id="8e613-140">Järgmiste sammudena asendate selle Word malli uue Word malliga SampleVendPaymDocReportBounded2.docx, mille varem alla laadisite.</span><span class="sxs-lookup"><span data-stu-id="8e613-140">In the following steps, you will replace this Word template with the new Word template, SampleVendPaymDocReportBounded2.docx, that you downloaded earlier.</span></span>

1. <span data-ttu-id="8e613-141">Lehel **Vormingu kujundaja** valige suvand **Käivitamine**.</span><span class="sxs-lookup"><span data-stu-id="8e613-141">On the **Format designer** page, select **Attachments**.</span></span>
2. <span data-ttu-id="8e613-142">Olemasoleva Exceli malli eemaldamiseks valige lehel **Manused** suvand **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="8e613-142">On the **Attachments** page, select **Delete** to remove the existing template.</span></span>
3. <span data-ttu-id="8e613-143">Toimingu kinnitamiseks valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="8e613-143">Select **Yes** to confirm the deletion.</span></span>
4. <span data-ttu-id="8e613-144">Valige **Uus** \> **Fail**.</span><span class="sxs-lookup"><span data-stu-id="8e613-144">Select **New** \> **File**.</span></span>
5. <span data-ttu-id="8e613-145">Valige **Sirvi**, ja seejärel sirvige ja valige fail **SampleVendPaymDocReportBounded2.docx** mille varem alla laadisite.</span><span class="sxs-lookup"><span data-stu-id="8e613-145">Select **Browse**, and browse to and select the **SampleVendPaymDocReportBounded2.docx** file that you downloaded earlier.</span></span>
6. <span data-ttu-id="8e613-146">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e613-146">Select **OK**.</span></span>
7. <span data-ttu-id="8e613-147">Sulgege leht **Manused**.</span><span class="sxs-lookup"><span data-stu-id="8e613-147">Close the **Attachments** page.</span></span>
8. <span data-ttu-id="8e613-148">Lehel **vormingu kujundaja** väljal **mall** sisestage või valige **SampleVendPaymDocReportBounded2.docx** fail.</span><span class="sxs-lookup"><span data-stu-id="8e613-148">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReportBounded2.docx** file.</span></span>

## <a name="run-the-format-to-create-word-output"></a><span data-ttu-id="8e613-149">Wordi väljundi loomiseks vormingu käivitamine</span><span class="sxs-lookup"><span data-stu-id="8e613-149">Run the format to create Word output</span></span>

1. <span data-ttu-id="8e613-150">Minge jaotisse **Ostureskontro** \> **Maksed** \> **Makse tööleht**.</span><span class="sxs-lookup"><span data-stu-id="8e613-150">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="8e613-151">Lehel **hankija maksed** vahekaardil **Loend**, valige kõik maksed.</span><span class="sxs-lookup"><span data-stu-id="8e613-151">On the **Vendor payments** page, on the **List** tab, select all the payments.</span></span>
3. <span data-ttu-id="8e613-152">Valige **Makse olek** \> **Puudub**.</span><span class="sxs-lookup"><span data-stu-id="8e613-152">Select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="8e613-153">Valige **Loo maksed**.</span><span class="sxs-lookup"><span data-stu-id="8e613-153">Select **Generate payments**.</span></span>
5. <span data-ttu-id="8e613-154">Valige väljal **Makseviis** **Elektrooniline**.</span><span class="sxs-lookup"><span data-stu-id="8e613-154">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="8e613-155">Valige väljal **Pangakonto** suvand **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="8e613-155">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="8e613-156">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e613-156">Select **OK**.</span></span>
8. <span data-ttu-id="8e613-157">**Elektroonilise aruande** dialoogiaknas valige **Ok** ja analüüsige loodud väljundit.</span><span class="sxs-lookup"><span data-stu-id="8e613-157">In the **Electronic report parameters** dialog box, select **OK**, and analyze the generated output.</span></span>

    ![Hankija maksete lehel töödeldavad maksed](./media/er-design-configuration-word-suppress-controls-image2.gif)

    <span data-ttu-id="8e613-159">Väljund esitatakse Wordi vormingus ja see sisaldab kokkuvõtte jaotist.</span><span class="sxs-lookup"><span data-stu-id="8e613-159">The output is presented in Word format and contains the summary section.</span></span>

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a><span data-ttu-id="8e613-160">Redigeeritava vormingu konfigureerimine kokkuvõttejao vastu kindlustamiseks</span><span class="sxs-lookup"><span data-stu-id="8e613-160">Configure the editable format to suppress the summary section</span></span>

<span data-ttu-id="8e613-161">Kui soovite loodud dokumendis oleva kokkuvõttejao eest vastu võtta, peate seda ER-vormingut käitava kasutaja taotluse alusel muutma redigeeritavat ER-vormingut.</span><span class="sxs-lookup"><span data-stu-id="8e613-161">If you want to suppress the summary section in a generated document, based on the request of a user who runs this ER format, you must modify the editable ER format.</span></span>

1. <span data-ttu-id="8e613-162">Minge **Organisatsiooni haldus** \> **Tööruumid** \> **Elektrooniline aruandlus** juurde ja avage ER-vormingu mustandversioon redigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="8e613-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**, and open the draft version of the ER format for editing.</span></span>
2. <span data-ttu-id="8e613-163">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="8e613-163">Select **Reporting configurations**.</span></span> 
3. <span data-ttu-id="8e613-164">Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel** \> **Töölehe aruande näide**.</span><span class="sxs-lookup"><span data-stu-id="8e613-164">On the **Configurations** page, in the configuration tree, expand **Payment model** \> **Sample worksheet report**.</span></span>
4. <span data-ttu-id="8e613-165">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="8e613-165">Select **Designer**.</span></span>
5. <span data-ttu-id="8e613-166">Laiendage **Vormingukujundaja** lehel **Word** ja valige suvand **SummaryLines**.</span><span class="sxs-lookup"><span data-stu-id="8e613-166">On the **Format designer** page, expand **Word**, and select **SummaryLines**.</span></span>
6. <span data-ttu-id="8e613-167">Lisage vahekaardil **Vastendamine** uus andmeallikas, et küsida kasutajalt käitusajal, kaskokkuvõtte jaotis tuleks tõkestada:</span><span class="sxs-lookup"><span data-stu-id="8e613-167">On the **Mapping** tab, add a new data source to ask the user, at runtime, whether the summary section should be suppressed:</span></span>

    1. <span data-ttu-id="8e613-168">Valige **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="8e613-168">Select **Add root**.</span></span>
    2. <span data-ttu-id="8e613-169">Dialoogiboksis **Andmeallika lisamine** valige **Üldine\kasutaja sisendparameeter** et avada **Kasutaja sisendparameeter andmeallika parameeter** dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="8e613-169">In the **Add data source** dialog box, select **General\User input parameter** to open the **'User input parameter' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="8e613-170">Väljale **Nimi** sisestage suvand **uiptõkesta**.</span><span class="sxs-lookup"><span data-stu-id="8e613-170">In the **Name** field, enter **uipSuppress**.</span></span>
    4. <span data-ttu-id="8e613-171">Väljale **Silt** sisestage **Tõkesta kokkuvõte**.</span><span class="sxs-lookup"><span data-stu-id="8e613-171">In the **Label** field, enter **Suppress summary section**.</span></span>
    5. <span data-ttu-id="8e613-172">Väljal **Toimingute andmetüübi** valige või sisestage **EiJah**.</span><span class="sxs-lookup"><span data-stu-id="8e613-172">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="8e613-173">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e613-173">Select **OK**.</span></span>

7. <span data-ttu-id="8e613-174">Järgmisena tuleb rakenduse loenduse tüübile **EiJah** lisada andmeallikas, mille tüüp:</span><span class="sxs-lookup"><span data-stu-id="8e613-174">Add a new data source of the **NoYes** application enumeration type:</span></span>

    1. <span data-ttu-id="8e613-175">Valige **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="8e613-175">Select **Add root**.</span></span>
    2. <span data-ttu-id="8e613-176">Dialoogiboksis **Andmeallika lisamine** valige **Dynamics 365 for Operations\Andmeallikas** et avada **andmeallika atribuudid** dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="8e613-176">In the **Add data source** dialog box, select **Dynamics 365 for Operations\Enumeration** to open the **'Enumeration' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="8e613-177">Väljale **Nimi** sisestage **enumEiJah**.</span><span class="sxs-lookup"><span data-stu-id="8e613-177">In the **Name** field, enter **enumNoYes**.</span></span>
    4. <span data-ttu-id="8e613-178">Väljale **Silt** sisestage **Tõkesta tingimused**.</span><span class="sxs-lookup"><span data-stu-id="8e613-178">In the **Label** field, enter **Suppress options**.</span></span>
    5. <span data-ttu-id="8e613-179">Väljal **Toimingute andmetüübi** valige või sisestage **EiJah**.</span><span class="sxs-lookup"><span data-stu-id="8e613-179">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="8e613-180">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e613-180">Select **OK**.</span></span>

8. <span data-ttu-id="8e613-181">Valitud **SummaryLinesi** vorminguelemendi puhul konfigureerige valem määramaks, millal valitud vorminguelemendiga seotud Wordi sisu juhtelement tuleb tõkestada:</span><span class="sxs-lookup"><span data-stu-id="8e613-181">For the selected **SummaryLines** format element, configure the formula to specify when the Word content control that is associated with the selected format element should be suppressed:</span></span>

    1. <span data-ttu-id="8e613-182">**Vastendamise** vahekaardil **Eemaldatud** jaotises valige **Redigeeri** et avada **[Valemikoostur](general-electronic-reporting-formula-designer.md)** lehel.</span><span class="sxs-lookup"><span data-stu-id="8e613-182">On the **Mapping** tab, in the **Removed** section, select **Edit** to open the **[Formula designer](general-electronic-reporting-formula-designer.md)** page.</span></span>
    2. <span data-ttu-id="8e613-183">**Valem** väljal, valige valem `uipSuppress = enumNoYes.Yes`.</span><span class="sxs-lookup"><span data-stu-id="8e613-183">In the **Formula** field, enter the formula `uipSuppress = enumNoYes.Yes`.</span></span>
    3. <span data-ttu-id="8e613-184">Valige **Salvesta** ja sulgege leht **Valemikoostaja**.</span><span class="sxs-lookup"><span data-stu-id="8e613-184">Select **Save**, and close the **Formula designer** page.</span></span>

        > [!NOTE]
        > <span data-ttu-id="8e613-185">See valem rakendatakse loodud dokumendile pärast **kõigi teiste vorminguelementide käivitamist**.</span><span class="sxs-lookup"><span data-stu-id="8e613-185">This formula will be applied to a generated document **after all other format elements are run**.</span></span> <span data-ttu-id="8e613-186">Selle valemi rakendamiseks leitakse loodud dokumendist Wordi sisu juhtelement, milleks valem on konfigureeritud (**SummaryLines** antud juhul) mis on märgistatud vorminguelemendina.</span><span class="sxs-lookup"><span data-stu-id="8e613-186">To apply this formula, a Word content control that is tagged as a format element that the formula is configured for (**SummaryLines** in this case) is found in a generated document.</span></span> <span data-ttu-id="8e613-187">Seejärel eemaldatakse see sisu juhtelement täielikult koos wordi tabeli reaga, mis seda hoiab.</span><span class="sxs-lookup"><span data-stu-id="8e613-187">That content control is then completely removed, together with the row in the Word table that holds it.</span></span> <span data-ttu-id="8e613-188">Kokkuvõtte jaotise üksikasjade rida eemaldatakse loodud dokumendist.</span><span class="sxs-lookup"><span data-stu-id="8e613-188">The details row of the summary section is removed from the generated document.</span></span>
        >
        > <span data-ttu-id="8e613-189">Kujundusaja ajal võite konfigureerida vorminguelemendi jaoks valemi **Eemaldatud** kuigi teil pole wordi mallis sisu juhtelementi, mille jaoks te kasutate, silt, mis vastab vorminguelemendi nimele, mille jaoks on konfigureeritud atribuut **Eemaldatud**.</span><span class="sxs-lookup"><span data-stu-id="8e613-189">At design time, you might configure the **Removed** formula for a format element, even though no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span> <span data-ttu-id="8e613-190">Kui valideerite vormingu konstruktsiooni ajal, kuvatakse [selle vastuolu](er-components-inspections.md#i14) kohta hoiatus.</span><span class="sxs-lookup"><span data-stu-id="8e613-190">When you validate the format at design time, you receive a [warning](er-components-inspections.md#i14) about this inconsistency.</span></span>
        >
        > <span data-ttu-id="8e613-191">Käitusajal ilmneb erand, kui wordi mallis, mida kasutate, puudub sisu juhtelement, mille silt vastab vorminguelemendi nimele, mille jaoks on **Eemaldatud** konfigureeritud atribuut.</span><span class="sxs-lookup"><span data-stu-id="8e613-191">At runtime, an exception is thrown if no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span>

    4. <span data-ttu-id="8e613-192">Vahekaardil **Vastendamine** jaotises **Eemaldatud** seadke **Emasüksusega** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="8e613-192">On the **Mapping** tab, in the **Removed** section, set the **With parent** option to **Yes**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="8e613-193">Selle valiku väärtuseks tuleb määrata **jah** et eemaldada kogu Wordi tabel kokkuvõtte sektsiooni üksikasju omav rea emaobjektiks.</span><span class="sxs-lookup"><span data-stu-id="8e613-193">You must set this option to **Yes** to remove the whole Word table as the parent object of the row that holds the summary section details.</span></span> <span data-ttu-id="8e613-194">Kui seadistate valiku väärtuseks **Ei** jääb jaotise päiserida loodud dokumenti.</span><span class="sxs-lookup"><span data-stu-id="8e613-194">If you set this option to **No**, the section header row remains in the generated document.</span></span>

9. <span data-ttu-id="8e613-195">Oma asukohakorralduse muudatuste salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="8e613-195">Select **Save** to save your changes to the editable format.</span></span>

    ![Loodud väljund Wordi vormingus](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a><span data-ttu-id="8e613-197">Wordi väljundi loomiseks vormingu käivitamine</span><span class="sxs-lookup"><span data-stu-id="8e613-197">Run the modified format to create Word output</span></span>

1. <span data-ttu-id="8e613-198">Minge jaotisse **Ostureskontro** \> **Maksed** \> **Makse tööleht**.</span><span class="sxs-lookup"><span data-stu-id="8e613-198">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="8e613-199">Valige loodud maksete aruanne ja valige seejärel käsk **Jooned**.</span><span class="sxs-lookup"><span data-stu-id="8e613-199">Select the payment journal that you created, and then select **Lines**.</span></span>
3. <span data-ttu-id="8e613-200">Valige **hankija maksete** lehel kõik read ja seejärel **makse olek** \> **Pole**.</span><span class="sxs-lookup"><span data-stu-id="8e613-200">On the **Vendor payments** page, select all the rows, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="8e613-201">Valige **Loo maksed**.</span><span class="sxs-lookup"><span data-stu-id="8e613-201">Select **Generate payments**.</span></span>
5. <span data-ttu-id="8e613-202">Valige väljal **Makseviis** **Elektrooniline**.</span><span class="sxs-lookup"><span data-stu-id="8e613-202">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="8e613-203">Valige väljal **Pangakonto** suvand **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="8e613-203">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="8e613-204">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e613-204">Select **OK**.</span></span>
8. <span data-ttu-id="8e613-205">Dialoogiaknas **Elektroonilise aruande parameetrid** väljal **Kuva kokkuvõte** valige suvand **Jah**.</span><span class="sxs-lookup"><span data-stu-id="8e613-205">In the **Electronic report parameters** dialog box, in the **Suppress summary section** field, select **Yes**.</span></span>
9. <span data-ttu-id="8e613-206">Valige **OK** ja analüüsige loodud väljundit.</span><span class="sxs-lookup"><span data-stu-id="8e613-206">Select **OK**, and analyze the generated output.</span></span>

    ![Loodud väljund Wordi vormingus](./media/er-design-configuration-word-suppress-controls-image4.gif)

    <span data-ttu-id="8e613-208">Pange tähele, et väljund ei sisalda kokkuvõtte jaotist, kuna see on tõkestatud.</span><span class="sxs-lookup"><span data-stu-id="8e613-208">Notice that the output doesn't contain the summary section, because it has been suppressed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e613-209">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="8e613-209">Additional resources</span></span>

- [<span data-ttu-id="8e613-210">OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine</span><span class="sxs-lookup"><span data-stu-id="8e613-210">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="8e613-211">Uue ER-i konfiguratsiooni koostamine Wordi vormingus aruannete loomiseks</span><span class="sxs-lookup"><span data-stu-id="8e613-211">Design a new ER configuration to generate reports in Word format</span></span>](er-design-configuration-word.md)
- [<span data-ttu-id="8e613-212">ER-i konfiguratsioonide korduvkasutamine Exceli mallidega Wordi vormingus aruannete loomiseks</span><span class="sxs-lookup"><span data-stu-id="8e613-212">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="8e613-213">Käitusaja probleemide ennetamiseks konfigureeritud ER-i komponendi kontrollimine</span><span class="sxs-lookup"><span data-stu-id="8e613-213">Inspect the configured ER component to prevent runtime issues</span></span>](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]