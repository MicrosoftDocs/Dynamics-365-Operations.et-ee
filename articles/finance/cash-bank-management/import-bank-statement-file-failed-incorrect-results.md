---
title: Pangaväljavõtte faili importimise tõrkeotsing
description: On oluline, et pangaväljavõtte fail pangast vastaks paigutusele, mida Microsoft Dynamics 365 Finance toetab. Pangaväljavõtete rangete standardite tõttu töötavad enamik integratsioone õigesti. Mõnikord ei saa väljavõttefaili importida või on sel valed tulemused. Tüüpiliselt põhjustavad neid probleeme väikesed erinevused pangaväljavõtte failis. See artikkel selgitab, kuidas neid erinevusi parandada ja probleeme lahendada.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0e01881a6b68526479d27014d49a718069cffc9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815880"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="23988-107">Pangaväljavõtte faili importimise tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="23988-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23988-108">On oluline, et pangaväljavõtte fail pangast vastaks paigutusele, mida Microsoft Dynamics 365 Finance toetab.</span><span class="sxs-lookup"><span data-stu-id="23988-108">It's important that the bank statement file from the bank matches the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="23988-109">Pangaväljavõtete rangete standardite tõttu töötavad enamik integratsioone õigesti.</span><span class="sxs-lookup"><span data-stu-id="23988-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="23988-110">Mõnikord ei saa väljavõttefaili importida või on sel valed tulemused.</span><span class="sxs-lookup"><span data-stu-id="23988-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="23988-111">Tüüpiliselt põhjustavad neid probleeme väikesed erinevused pangaväljavõtte failis.</span><span class="sxs-lookup"><span data-stu-id="23988-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="23988-112">See artikkel selgitab, kuidas neid erinevusi parandada ja probleeme lahendada.</span><span class="sxs-lookup"><span data-stu-id="23988-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="23988-113">Mis on tõrge?</span><span class="sxs-lookup"><span data-stu-id="23988-113">What is the error?</span></span>
------------------

<span data-ttu-id="23988-114">Kui olete proovinud importida pangaväljavõtte faili, minge tõrke leidmiseks andmehalduse töö ajalukku ja selle käivitamise üksikasjadesse.</span><span class="sxs-lookup"><span data-stu-id="23988-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="23988-115">Tõrge võib aidata, osutades väljavõttele, saldole või väljavõtte reale.</span><span class="sxs-lookup"><span data-stu-id="23988-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="23988-116">Siiski on ebatõenäoline, et see annab piisavalt teavet aitamaks teil tuvastada probleemi põhjustavat välja või elementi.</span><span class="sxs-lookup"><span data-stu-id="23988-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

> [!NOTE]
> <span data-ttu-id="23988-117">Imporditud pangaväljavõtted võivad kattuda ainult ühe ajapunkti puhul.</span><span class="sxs-lookup"><span data-stu-id="23988-117">Imported bank statements can overlap only for single a point in time.</span></span>  <span data-ttu-id="23988-118">Näiteks kui väljavõte lõpeb 1. jaanuaril 2021 kell 00.00, võib järgmise väljavõtte alguskuupäev olla 00.00 1. jaanuaril 2021 00:00:00.</span><span class="sxs-lookup"><span data-stu-id="23988-118">For example, if a statement ends at 12:00 AM on January 1, 2021, then beginning date for the next statement can be 12:00 AM on Jarnuary 1, 2021 12:00:00 AM.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="23988-119">Millised on erinevused?</span><span class="sxs-lookup"><span data-stu-id="23988-119">What are the differences?</span></span>
<span data-ttu-id="23988-120">Võrrelge panga faili paigutuse määratlust Finance'i impordi määratlusega ja pange tähele mis tahes võimalikke erinevusi väljades ja elementides.</span><span class="sxs-lookup"><span data-stu-id="23988-120">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="23988-121">Võrrelge pangaväljavõtte faili seotud Finance'i näidisfailiga.</span><span class="sxs-lookup"><span data-stu-id="23988-121">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="23988-122">ISO20022 failides peaks võimalikke erinevusi lihtne märgata olema.</span><span class="sxs-lookup"><span data-stu-id="23988-122">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="23988-123">Ajavöönd on imporditud pangaväljavõtetes erinev</span><span class="sxs-lookup"><span data-stu-id="23988-123">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="23988-124">Impordifaili kuupäeva-kellaaja väärtused võivad erineda Finance and Operationsis kuvatavatest kuupäeva-kellaaja väärtustest.</span><span class="sxs-lookup"><span data-stu-id="23988-124">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="23988-125">Selle lahknevuse vältimiseks sisestage ajavööndi eelistus lehele **Andmeallika konfigureerimine**.</span><span class="sxs-lookup"><span data-stu-id="23988-125">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="23988-126">Lisateavet ajavööndi eelistuste sisestamise kohta leiate teemast [Täpsema panga vastavusseviimise importimisprotsessi seadistamine](set-up-advanced-bank-reconciliation-import-process.md).</span><span class="sxs-lookup"><span data-stu-id="23988-126">For more information about entering a time zone preference, see [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>

## <a name="transformations"></a><span data-ttu-id="23988-127">Teisendused</span><span class="sxs-lookup"><span data-stu-id="23988-127">Transformations</span></span>
<span data-ttu-id="23988-128">Tüüpiliselt tuleb muudatus teha ühes kolmest teisendusest.</span><span class="sxs-lookup"><span data-stu-id="23988-128">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="23988-129">Iga teisendus on kirjutatud spetsiifilise standardi jaoks.</span><span class="sxs-lookup"><span data-stu-id="23988-129">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="23988-130">Ressursi nimi</span><span class="sxs-lookup"><span data-stu-id="23988-130">Resource name</span></span>                                         | <span data-ttu-id="23988-131">Faili nimi</span><span class="sxs-lookup"><span data-stu-id="23988-131">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="23988-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="23988-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="23988-133">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="23988-133">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="23988-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="23988-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="23988-135">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="23988-135">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="23988-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="23988-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="23988-137">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="23988-137">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="23988-138">Silumise teisendused</span><span class="sxs-lookup"><span data-stu-id="23988-138">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="23988-139">BAI2 ja MT940 failide korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="23988-139">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="23988-140">BAI2 ja MT940 failid on tekstipõhised failid ja nõuavad korrigeerimist, et lubada XSLT-dokumendi teisenduste (Extensible Stylesheet Language Transformations) silumist</span><span class="sxs-lookup"><span data-stu-id="23988-140">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="23988-141">Programm teeb selle korrigeerimise faili importimisel.</span><span class="sxs-lookup"><span data-stu-id="23988-141">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="23988-142">Looge XML-fail ja kopeerige järgmine tekst sellesse.</span><span class="sxs-lookup"><span data-stu-id="23988-142">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="23988-143">Kopeerige pangaväljavõtte faili sisu ja kleepige need XML-faili, et need asendaks teksti **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="23988-143">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="23988-144">XSLT silumine</span><span class="sxs-lookup"><span data-stu-id="23988-144">Debug the XSLT</span></span>

<span data-ttu-id="23988-145">Lisateavet vt <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="23988-145">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="23988-146">Käivitage Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="23988-146">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="23988-147">Looge konsooli rakendus.</span><span class="sxs-lookup"><span data-stu-id="23988-147">Create a console application.</span></span>
3.  <span data-ttu-id="23988-148">Avage sobiv XSLT.</span><span class="sxs-lookup"><span data-stu-id="23988-148">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="23988-149">Klõpsake XLST ja selle atribuutide lehekülge.</span><span class="sxs-lookup"><span data-stu-id="23988-149">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="23988-150">Määrake sisend pangaväljavõtte faili asukohale.</span><span class="sxs-lookup"><span data-stu-id="23988-150">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="23988-151">Määratlege väljundi asukoht ja faili nimi.</span><span class="sxs-lookup"><span data-stu-id="23988-151">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="23988-152">Määrake nõutud murdepunktid.</span><span class="sxs-lookup"><span data-stu-id="23988-152">Set the required break points.</span></span>
8.  <span data-ttu-id="23988-153">Menüüs klõpsake valikuid **XML** &gt; **Käivita XSLT silumine**.</span><span class="sxs-lookup"><span data-stu-id="23988-153">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="23988-154">XSLT-väljundi vormindamine</span><span class="sxs-lookup"><span data-stu-id="23988-154">Format the XSLT output</span></span>

<span data-ttu-id="23988-155">Teisenduse käitamisel loob see väljundfaili, mida saate vaadata Visual Studios.</span><span class="sxs-lookup"><span data-stu-id="23988-155">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="23988-156">Kasutage otseteid Ctrl+A, Ctrl+K ja Ctrl+D, et väljundfaili kiiresti vormindada.</span><span class="sxs-lookup"><span data-stu-id="23988-156">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="23988-157">Teisenduse korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="23988-157">Adjust the transformation</span></span>

<span data-ttu-id="23988-158">Korrigeerige teisendust, et saada sobiv väli või element pangaväljavõtte failis.</span><span class="sxs-lookup"><span data-stu-id="23988-158">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="23988-159">Seejärel vastendage see väli või element sobiva Finance'i elemendiga.</span><span class="sxs-lookup"><span data-stu-id="23988-159">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="23988-160">Deebeti/kreediti indikaator</span><span class="sxs-lookup"><span data-stu-id="23988-160">Debit/credit indicator</span></span>

<span data-ttu-id="23988-161">Mõnikord võib deebetid importida kreedititena ja kreediteid võib importida deebetitena.</span><span class="sxs-lookup"><span data-stu-id="23988-161">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="23988-162">Selle probleemi lahendamiseks peate muutma sobivat XSLT-d.</span><span class="sxs-lookup"><span data-stu-id="23988-162">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="23988-163">Kui pangaväljavõtted tulevad mitmest pangast, veenduge, et need kõik kasutavad sama deebeti/kreediti lähenemist, või looge eraldi teisendused.</span><span class="sxs-lookup"><span data-stu-id="23988-163">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="23988-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator mall</span><span class="sxs-lookup"><span data-stu-id="23988-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="23988-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit mall</span><span class="sxs-lookup"><span data-stu-id="23988-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="23988-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator mall</span><span class="sxs-lookup"><span data-stu-id="23988-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="23988-167">Näited pangaväljavõtte vormingutest ja tehnilistest paigutustest</span><span class="sxs-lookup"><span data-stu-id="23988-167">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="23988-168">Järgmises tabelis on esitatud näited tehnilise paigutuse määratlustest täiustatud panga vastavusseviimise impordifailide ja kolme seotud pangaväljavõtte näidisfailide puhul.</span><span class="sxs-lookup"><span data-stu-id="23988-168">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="23988-169">Näidisfailid ja tehnilised paigutused saab laadida alla siit: [Impordifaili näited](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="23988-169">You can download the example files and technical layouts here: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="23988-170">Tehnilise paigutuse määratlus</span><span class="sxs-lookup"><span data-stu-id="23988-170">Technical layout definition</span></span>                             | <span data-ttu-id="23988-171">Pangaväljavõtte näidisfail</span><span class="sxs-lookup"><span data-stu-id="23988-171">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="23988-172">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="23988-172">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="23988-173">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="23988-173">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="23988-174">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="23988-174">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="23988-175">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="23988-175">ISO20022StatementExample</span></span>](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| <span data-ttu-id="23988-176">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="23988-176">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="23988-177">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="23988-177">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
