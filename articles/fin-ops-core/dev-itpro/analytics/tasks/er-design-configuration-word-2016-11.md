---
title: Exceli mallidega ER-i konfiguratsioonide taaskasutamine Wordi vormingus aruannete loomiseks
description: See teema kirjeldab, kuidas konfigureerida aruande vorminguid, mis loodi aruannete loomiseks Exceli töövihikuna, looma aruandeid Wordi dokumendina.
author: NickSelin
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 728984678d78cf626e2b30222f1d1e603e05d117
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755054"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a><span data-ttu-id="1aa4b-103">Exceli mallidega ER-i konfiguratsioonide taaskasutamine Wordi vormingus aruannete loomiseks</span><span class="sxs-lookup"><span data-stu-id="1aa4b-103">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1aa4b-104">Aruannete loomiseks Microsoft Wordi dokumentidena saate [konfigureerida](../er-design-configuration-word.md) uue [elektroonilise aruandluse (ER)](../general-electronic-reporting.md) [vormingu](../general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="1aa4b-104">To generate reports as Microsoft Word documents, you can [configure](../er-design-configuration-word.md) a new [Electronic reporting (ER)](../general-electronic-reporting.md) [format](../general-electronic-reporting.md#FormatComponentOutbound).</span></span> <span data-ttu-id="1aa4b-105">Teise võimalusena saate taaskasutada ER-vormingut, mis oli algselt mõeldud aruannete loomiseks Exceli töövihikutena.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-105">Alternatively, you can reuse an ER format that was originally designed to generate reports as Excel workbooks.</span></span> <span data-ttu-id="1aa4b-106">Sellisel juhul peate asendama Exceli malli Wordi malliga.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-106">In this case, you must replace the Excel template with a Word template.</span></span>

<span data-ttu-id="1aa4b-107">Järgmised protseduurid näitavad, kuidas kasutaja kas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis saab konfigureerida ER-vormingut, et luua aruandeid Wordi failidena, kasutades uuesti ER-vormingut, mis loodi aruannete loomiseks Exceli failidena.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-107">The following procedures show how a user in either the System administrator role or the Electronic reporting developer role can configure an ER format to generate reports as Word files by reusing an ER format that was designed to generate reports as Excel files.</span></span>

<span data-ttu-id="1aa4b-108">Neid toiminguid saab lõpule viia ettevõttes GBSI.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-108">These procedures can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1aa4b-109">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="1aa4b-109">Prerequisites</span></span>

<span data-ttu-id="1aa4b-110">Nende protsesside lõpuleviimiseks peate esmalt järgima samme tegevuse juhises [Konfiguratsiooni loomine aruannete loomiseks vormingus OPENXML](er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="1aa4b-110">To complete these procedures, you must first follow the steps in the [Design a configuration for generating reports in OPENXML format](er-design-reports-openxml-2016-11.md) task guide.</span></span>

<span data-ttu-id="1aa4b-111">Peate näidisaruande jaoks alla laadima ja kohalikult salvestama ka järgmised mallid:</span><span class="sxs-lookup"><span data-stu-id="1aa4b-111">You must also download and locally save the following templates for the sample report:</span></span>

- [<span data-ttu-id="1aa4b-112">Maksearuande mall (SampleVendPaymDocReport.docx)</span><span class="sxs-lookup"><span data-stu-id="1aa4b-112">Template of Payment Report (SampleVendPaymDocReport.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="1aa4b-113">Maksearuande piiratud mall (SampleVendPaymDocReportBounded.docx)</span><span class="sxs-lookup"><span data-stu-id="1aa4b-113">Bounded Template of Payment Report (SampleVendPaymDocReportBounded.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="1aa4b-114">Need protseduurid n funktsiooni jaoks, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611 (november 2016).</span><span class="sxs-lookup"><span data-stu-id="1aa4b-114">These procedures are for a feature that was added in Dynamics 365 for Operations version 1611 (November 2016).</span></span>

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="1aa4b-115">Olemasoleva elektroonilise aruandluse aruande konfiguratsiooni valimine</span><span class="sxs-lookup"><span data-stu-id="1aa4b-115">Select the existing ER report configuration</span></span>

1. <span data-ttu-id="1aa4b-116">Avage rakenduses Dynamics 365 Finance suvand **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-116">In Dynamics 365 Finance, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="1aa4b-117">Veenduge, et konfiguratsiooni pakkuja **Litware, Inc.** on valitud **aktiivsena**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-117">Make sure that the **Litware, Inc.** configuration provider is selected as **Active**.</span></span> <span data-ttu-id="1aa4b-118">Kui ei, järgige samme tegevuse juhises [Konfiguratsiooni pakkujate loomine ja nende märkimine aktiivseks](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="1aa4b-118">If it isn't, follow the steps in the [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) task guide.</span></span>
3. <span data-ttu-id="1aa4b-119">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-119">Select **Reporting configurations**.</span></span> <span data-ttu-id="1aa4b-120">Taaskasutate olemasolevat elektroonilise aruandluse konfiguratsiooni, mis oli mõeldud aruande väljundi loomiseks OPENXML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-120">You will reuse the existing ER configuration that was designed to generate the report output in OPENXML format.</span></span>
4. <span data-ttu-id="1aa4b-121">Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel** ja valige **Töölehe aruande näide**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-121">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and select **Sample worksheet report**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1aa4b-122">Valitud ER-i vormingu mustandi versiooni saab muuta kiirkaardil **Versioonid**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-122">The draft version of the selected ER format can be edited on the **Versions** FastTab.</span></span>

5. <span data-ttu-id="1aa4b-123">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-123">Select **Designer**.</span></span>
6. <span data-ttu-id="1aa4b-124">Lehel **Vormingukujundaja** pange tähele, et juurvormingu elemendi pealkiri näitab, et praegu kasutatakse Exceli vormingut.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-124">On the **Format designer** page, notice that the title of the root format element indicates that an Excel template is currently used.</span></span>

![Olemasoleva konfiguratsiooni valimine](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a><span data-ttu-id="1aa4b-126">Allalaaditud Wordi malli läbivaatamine</span><span class="sxs-lookup"><span data-stu-id="1aa4b-126">Review the downloaded Word template</span></span>

1. <span data-ttu-id="1aa4b-127">Avage Wordi töölauarakenduses mailifail **SampleVendPaymDocReport.docx**, mille varem alla laadisite.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-127">In the Word desktop application, open the **SampleVendPaymDocReport.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="1aa4b-128">Kinnitage, et mall sisaldab ainult sellise dokumendi paigutust, mille soovite luua elektroonilise aruandluse väljundina.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-128">Verify that the template contains only the layout of the document that you want to generate as ER output.</span></span>

![Wordi malli paigutus töölauarakenduses](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a><span data-ttu-id="1aa4b-130">Exceli malli Wordi malliga asendamine ja kohandatud XML-i osa lisamine</span><span class="sxs-lookup"><span data-stu-id="1aa4b-130">Replace the Excel template with the Word template and add a custom XML part</span></span>

<span data-ttu-id="1aa4b-131">Praegu kasutatakse Exceli dokumenti mallina väljundi loomiseks OPENXML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-131">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="1aa4b-132">Asendate selle malliWordi malli failiga SampleVendPaymDocReport.docx, mille varem alla laadisite.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-132">You will replace this template with the SampleVendPaymDocReport.docx Word template file that you downloaded earlier.</span></span> <span data-ttu-id="1aa4b-133">Lisaks laiendate Wordi malli, lisades kohandatud XML-i osa.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-133">You will also extend the Word template by adding a custom XML part.</span></span>

1. <span data-ttu-id="1aa4b-134">Valige rakenduses Finance lehel **Vormingukujundaja** vahekaardil **Vorming** suvand **Manused**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-134">In Finance, on the **Format designer** page, on the **Format** tab, select **Attachments**.</span></span>
2. <span data-ttu-id="1aa4b-135">Olemasoleva Exceli malli eemaldamiseks valige lehel **Manused** suvand **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-135">On the **Attachments** page, select **Delete** to remove the existing Excel template.</span></span> <span data-ttu-id="1aa4b-136">Muudatuse kinnitamiseks valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-136">Select **Yes** to confirm the change.</span></span>
3. <span data-ttu-id="1aa4b-137">Valige **Uus** \> **Fail**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-137">Select **New** \> **File**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1aa4b-138">Peate valima dokumendi tüübi, mis on ER-i parameetrites [konfigureeritud](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) talletama ER-vormingute malle.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-138">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

4. <span data-ttu-id="1aa4b-139">Valige **Sirvi** ja seejärel sirvige ja valige fail **SampleVendPaymDocReport.docx**, mille varem alla laadisite.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-139">Select **Browse**, and then browse to and select the **SampleVendPaymDocReport.docx** file that you downloaded earlier.</span></span>
5. <span data-ttu-id="1aa4b-140">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-140">Select **OK**.</span></span>
6. <span data-ttu-id="1aa4b-141">Sulgege leht **Manused**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-141">Close the **Attachments** page.</span></span>
7. <span data-ttu-id="1aa4b-142">Lehel **Vormingu kujundaja** väljal **Mall** sisestage või valige fail **SampleVendPaymDocReport.docx**, et kasutada seda Wordi faili Exceli malli asemel, mida kasutati varem.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-142">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReport.docx** file to use that Word template instead of the Excel template that was previously used.</span></span>
8. <span data-ttu-id="1aa4b-143">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-143">Select **Save**.</span></span>

    <span data-ttu-id="1aa4b-144">Lisaks konfiguratsiooni muudatuste salvestamisele värskendab toiming **Salvesta** manustatud Wordi malli.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-144">In addition to storing configuration changes, the **Save** action updates the attached Word template.</span></span> <span data-ttu-id="1aa4b-145">Kujundatud vormingu hierarhiline struktuur lisatakse manustatud Wordi dokumenti uue kohandatud XML-i osana, mille nimeks pannakse **Aruanne**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-145">The hierarchical structure of the designed format is added to the attached Word document as a new custom XML part that is named **Report**.</span></span> <span data-ttu-id="1aa4b-146">Manustatud Wordi mall sisaldab dokumendi paigutust, mis luuakse ER-i väljundina, ja andmete struktuuri, mille ER sellesse malli käitusajal sisestab.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-146">The attached Word template contains the layout of the document that will be generated as ER output and the structure of data that ER will enter in that template at runtime.</span></span>

9. <span data-ttu-id="1aa4b-147">Pange tähele, et juurvormingu elemendi pealkiri näitab, et praegu kasutatakse Wordi vormingut.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-147">Notice that the title of the root format element indicates that a Word template is currently used.</span></span>

    ![Exceli malli Wordi malliga asendamine ja kohandatud XML-i osa lisamine](../media/er-design-configuration-word-2016-11-image03.gif)

10. <span data-ttu-id="1aa4b-149">Vahekaardil **Vorming** valige **Manused**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-149">On the **Format** tab, select **Attachments**.</span></span>

<span data-ttu-id="1aa4b-150">Saate nüüd vastendada kohandatud XML-i osa **Aruanne** elemendid Word dokumendi sisu juhtelementidega.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-150">You can now map the elements of the **Report** custom XML part to the content controls of the Word document.</span></span>

<span data-ttu-id="1aa4b-151">Kui olete tuttav protsessiga kujundada Wordi dokumendid vormidena, mis sisaldavad [sisu juhtelemente](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word), mis on vastendatud [kohandatud XML-i osade](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) elementidega, täitke dokumendi loomiseks kõik järgmise protseduuri sammud.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-151">If you're familiar with the process of designing Word documents as forms that contain [content controls](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) that are mapped to elements of [custom XML parts](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), complete all steps in the next procedure to create the document.</span></span> <span data-ttu-id="1aa4b-152">Lisateabe saamiseks vt [Ankeetide loomine, mida kasutajad täidavad või prindivad Wordis](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span><span class="sxs-lookup"><span data-stu-id="1aa4b-152">For more information, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span></span> <span data-ttu-id="1aa4b-153">Vastasel juhul jätke järgmine protseduur vahele.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-153">Otherwise, skip the next procedure.</span></span>

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a><span data-ttu-id="1aa4b-154">Wordi dokumendi hankimine, mis sisaldab kohandatud XML-i osa ja teeb andmevastendust</span><span class="sxs-lookup"><span data-stu-id="1aa4b-154">Get a Word document that has a custom XML part and do data mapping</span></span>

1. <span data-ttu-id="1aa4b-155">Valige rakenduses Finance lehel **Manused** suvand **Ava**, et laadida valitud mall rakendusest Finance alla ja talletada see kohalikult Wordi dokumendina.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-155">In Finance, on the **Attachments** page, select **Open** to download the selected template from Finance and store it locally as a Word document.</span></span>
3. <span data-ttu-id="1aa4b-156">Avage Wordi töölauarakenduses äsja alla laaditud dokument.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-156">In the Word desktop application, open the document that you just downloaded.</span></span>
4. <span data-ttu-id="1aa4b-157">Valige vahekaardil **Arendaja** suvand **XML-i vastendamise paan**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-157">On the **Developer** tab, select **XML Mapping Pane**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1aa4b-158">Kui vahekaarti **Arendaja** lindil ei kuvata, kohandage linti selle lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-158">If the **Developer** tab doesn't appear on the ribbon, customize the ribbon to add it.</span></span>

5. <span data-ttu-id="1aa4b-159">Valige paanil **XML-i vastendamine** lehel **Kohandatud XML-i osa** kohandatud XML-i osa **Aruanne**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-159">In the **XML Mapping** pane, in the **Custom XML Part** field, select the **Report** custom XML part.</span></span>
6. <span data-ttu-id="1aa4b-160">Vastendage valitud kohandatud XML-i osa **Aruanne** elemendid ja Wordi dokumendi sisu juhtelemendid.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-160">Map the elements of the selected **Report** custom XML part and the content controls of the Word document.</span></span>
7. <span data-ttu-id="1aa4b-161">Salvestage värskendatud Wordi dokument kohalikult nimega **SampleVendPaymDocReportBounded.docx**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-161">Save the updated Word document locally as **SampleVendPaymDocReportBounded.docx**.</span></span>

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="1aa4b-162">Wordi malli läbivaatamine, kus kohandatud XML-i osa on vastendatud sisu juhtelementidega</span><span class="sxs-lookup"><span data-stu-id="1aa4b-162">Review the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="1aa4b-163">Avage Wordi töölauarakenduses mailifail **SampleVendPaymDocReportBounded.docx**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-163">In the Word desktop application, open the **SampleVendPaymDocReportBounded.docx** template file.</span></span>
2. <span data-ttu-id="1aa4b-164">Kinnitage, et mall sisaldab sellise dokumendi paigutust, mille soovite luua elektroonilise aruandluse väljundina.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-164">Verify that the template contains the layout of the document that you want to generate as ER output.</span></span> <span data-ttu-id="1aa4b-165">Andmete kohatäidetena kasutatavad sisu juhtelemendid, mille ER sisestab selles mallis käitusajal, põhinevad vastendustel, mis on konfigureeritud kohandatud XML-i osa **Aruanne** elementide ja Wordi dokumendi sisu juhtelementide vahel.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-165">The content controls that are used as placeholders for data that ER will enter in this template at runtime are based on the mappings that are configured between elements of the **Report** custom XML part and the content controls of the Word document.</span></span>

![Wordi malli eelvaade töölauarakenduses](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="1aa4b-167">Wordi malli üleslaadimine, kus kohandatud XML-i osa on vastendatud sisu juhtelementidega</span><span class="sxs-lookup"><span data-stu-id="1aa4b-167">Upload the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="1aa4b-168">Valige rakenduses Finance lehel **Manused** suvand **Kustuta**, et eemaldada Wordi mall, millel puuduvad vastendused kohandatud XML-i osa **Aruanne** elementide ja sisu juhtelementide vahel.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-168">In Finance, on the **Attachments** page, select **Delete** to remove the Word template that has no mappings between elements of the **Report** custom XML part and content controls.</span></span> <span data-ttu-id="1aa4b-169">Muudatuse kinnitamiseks valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-169">Select **Yes** to confirm the change.</span></span>
2. <span data-ttu-id="1aa4b-170">Valige **Uus** \> **Fail**, et lisada uus mallifail, mis sisaldab vastendusi kohandatud XML-i osa **Aruanne** elementide ja sisu juhtelementide vahel.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-170">Select **New** \> **File** to add a new template file that contains mappings between elements of the **Report** custom XML part and content controls.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1aa4b-171">Peate valima dokumendi tüübi, mis on ER-i parameetrites [konfigureeritud](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) talletama ER-vormingute malle.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-171">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

3. <span data-ttu-id="1aa4b-172">Valige suvand **Sirvi** ning seejärel sirvige ja valige fail **SampleVendPaymDocReportBounded.docx**, mille laadisite alla või valmistasite ette, täites protseduuri jaotises [Wordi dokumendi hankimine, mis sisaldab kohandatud XML-i osa ja teeb andmevastendust](#get-word-doc).</span><span class="sxs-lookup"><span data-stu-id="1aa4b-172">Select **Browse**, and then browse to and select the **SampleVendPaymDocReportBounded.docx** file that you downloaded or prepared by completing the procedure in the [Get a Word that has a custom XML part to do data mapping](#get-word-doc) section.</span></span>
4. <span data-ttu-id="1aa4b-173">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-173">Select **OK**.</span></span>
5. <span data-ttu-id="1aa4b-174">Sulgege leht **Manused**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-174">Close the **Attachments** page.</span></span>
6. <span data-ttu-id="1aa4b-175">Valige lehel **Vormingu koostaja** väljal **Mall** dokument, mille just laadisite alla.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-175">On the **Format designer** page, in the **Template** field, select the document that you just downloaded.</span></span>
7. <span data-ttu-id="1aa4b-176">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-176">Select **Save**.</span></span>
8. <span data-ttu-id="1aa4b-177">Sulgege **Vormingu kujundaja** leht.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-177">Close the **Format designer** page.</span></span>

## <a name="mark-the-configured-format-as-runnable"></a><span data-ttu-id="1aa4b-178">Konfigureeritud vormingu käivitatavaks märkimine</span><span class="sxs-lookup"><span data-stu-id="1aa4b-178">Mark the configured format as runnable</span></span>

<span data-ttu-id="1aa4b-179">Redigeeritava vormingu mustandi versiooni käivitamiseks peate muutma selle [käivitatavaks](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span><span class="sxs-lookup"><span data-stu-id="1aa4b-179">To run the draft version of the editable format, you must make it [runnable](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span></span>

1. <span data-ttu-id="1aa4b-180">Valige rakenduses Finance lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** suvand **Kasutaja parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-180">In Finance, on the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
2. <span data-ttu-id="1aa4b-181">Seadke dialoogiboksis **Kasutaja parameetrid** suvandi **Käivitamissätted** väärtuseks **Jah** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-181">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
3. <span data-ttu-id="1aa4b-182">Vastavalt vajadusele valige **Redigeeri**, et muuta praegune leht redigeeritavaks.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-182">Select **Edit** to make the current page editable, as required.</span></span>
4. <span data-ttu-id="1aa4b-183">Praegu valitud konfiguratsiooni **Töölehe aruande näide** puhul määrake suvand **Käivita mustand** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-183">For the currently selected **Sample worksheet report** configuration, set the **Run Draft** option to **Yes**.</span></span>
5. <span data-ttu-id="1aa4b-184">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-184">Select **Save**.</span></span>

## <a name="run-the-format-to-create-output-in-word-format"></a><span data-ttu-id="1aa4b-185">Vormingu käitamine Wordi vormingus väljundi loomiseks</span><span class="sxs-lookup"><span data-stu-id="1aa4b-185">Run the format to create output in Word format</span></span>

1. <span data-ttu-id="1aa4b-186">Avage rakenduses Finance suvand **Ostureskontro** \> **Maksed** \> **Makse tööleht**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-186">In Finance, go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="1aa4b-187">Varem sisestatud makse töölehel valige suvand **Read**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-187">In a payment journal that you entered earlier, select **Lines**.</span></span>
3. <span data-ttu-id="1aa4b-188">Valige lehel **Hankija maksed** kõik ruudustiku read.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-188">On the **Vendor payments** page, select all rows in the grid.</span></span>
4. <span data-ttu-id="1aa4b-189">Valige **Makse olek** \> **Puudub**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-189">Select **Payment status** \> **None**.</span></span>

    ![Hankija maksete lehel töödeldavad maksed](../media/er-design-configuration-word-2016-11-image05.png)

5. <span data-ttu-id="1aa4b-191">Valige toimingupaanil **Loo maksed**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-191">On the Action Pane, select **Generate payments**.</span></span>
6. <span data-ttu-id="1aa4b-192">Ilmuvad dialoogiaknas tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-192">In the dialog box that appears, follow these steps:</span></span>

    1. <span data-ttu-id="1aa4b-193">Valige väljal **Makseviis** **Elektrooniline**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-193">In the **Method of payment** field, select **Electronic**.</span></span>
    2. <span data-ttu-id="1aa4b-194">Valige väljal **Pangakonto** suvand **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-194">In the **Bank account** field, select **GBSI OPER**.</span></span>
    3. <span data-ttu-id="1aa4b-195">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-195">Select **OK**.</span></span>

7. <span data-ttu-id="1aa4b-196">Valige dialoogiaknas **Elektroonilise aruandluse parameetrid** suvand **OK**.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-196">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="1aa4b-197">Loodud väljund esitatakse Wordi vormingus ja sisaldab töödeldud maksete üksikasju.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-197">The generated output is presented in Word format and contains the details of the processed payments.</span></span> <span data-ttu-id="1aa4b-198">Analüüsige loodud väljundit.</span><span class="sxs-lookup"><span data-stu-id="1aa4b-198">Analyze the generated output.</span></span>

    ![Loodud väljund Wordi vormingus](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a><span data-ttu-id="1aa4b-200">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1aa4b-200">Additional resources</span></span>

- [<span data-ttu-id="1aa4b-201">Uue ER-i konfiguratsiooni loomine Wordi vormingus aruannete loomiseks</span><span class="sxs-lookup"><span data-stu-id="1aa4b-201">Design a new ER configuration to generate reports in Word format</span></span>](../er-design-configuration-word.md)
- [<span data-ttu-id="1aa4b-202">Manustatud pildid ja kujutised ER-iga loodud dokumentides</span><span class="sxs-lookup"><span data-stu-id="1aa4b-202">Embed images and shapes in documents that you generate by using ER</span></span>](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]