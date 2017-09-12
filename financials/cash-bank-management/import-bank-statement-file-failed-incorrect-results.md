---
title: "Pangaväljavõtte faili importimise tõrkeotsing"
description: "On oluline, et pangaväljavõtte fail pangast vastaks paigutusele, mida Microsoft Dynamics 365 for Finance and Operations, Enterprise edition toetab. Pangaväljavõtete rangete standardite tõttu töötavad enamik integratsioone õigesti. Mõnikord ei saa väljavõttefaili importida või on sel valed tulemused. Tüüpiliselt põhjustavad neid probleeme väikesed erinevused pangaväljavõtte failis. See artikkel selgitab, kuidas neid erinevusi parandada ja probleeme lahendada."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 51cd32217b2f753f606e3060b4872a8274f16549
ms.contentlocale: et-ee
ms.lasthandoff: 07/18/2017

---

# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="7bdb9-107">Pangaväljavõtte faili importimise tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="7bdb9-107">Bank statement file import troubleshooting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7bdb9-108">On oluline, et pangaväljavõtte fail pangast vastaks paigutusele, mida Microsoft Dynamics 365 for Finance and Operations, Enterprise edition toetab.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 for Finance and Operations, Enterprise edition supports.</span></span> <span data-ttu-id="7bdb9-109">Pangaväljavõtete rangete standardite tõttu töötavad enamik integratsioone õigesti.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="7bdb9-110">Mõnikord ei saa väljavõttefaili importida või on sel valed tulemused.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="7bdb9-111">Tüüpiliselt põhjustavad neid probleeme väikesed erinevused pangaväljavõtte failis.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="7bdb9-112">See artikkel selgitab, kuidas neid erinevusi parandada ja probleeme lahendada.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="7bdb9-113">Mis on tõrge?</span><span class="sxs-lookup"><span data-stu-id="7bdb9-113">What is the error?</span></span>
------------------

<span data-ttu-id="7bdb9-114">Kui olete proovinud importida pangaväljavõtte faili, minge tõrke leidmiseks andmehalduse töö ajalukku ja selle käivitamise üksikasjadesse.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="7bdb9-115">Tõrge võib aidata, osutades väljavõttele, saldole või väljavõtte reale.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="7bdb9-116">Siiski on ebatõenäoline, et see annab piisavalt teavet aitamaks teil tuvastada probleemi põhjustavat välja või elementi.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="7bdb9-117">Millised on erinevused?</span><span class="sxs-lookup"><span data-stu-id="7bdb9-117">What are the differences?</span></span>
<span data-ttu-id="7bdb9-118">Võrrelge panga faili paigutuse määratlust Finance and Operationsi impordi määratlusega ja pange tähele mis tahes võimalikke erinevusi väljades ja elementides.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-118">Compare the bank file layout definition to the Finance and Operations import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="7bdb9-119">Võrrelge pangaväljavõtte faili seotud Finance and Operationsi näidisfailiga.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-119">Compare the bank statement file to the related sample Finance and Operations file.</span></span> <span data-ttu-id="7bdb9-120">ISO20022 failides peaks võimalikke erinevusi lihtne märgata olema.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="transformations"></a><span data-ttu-id="7bdb9-121">Teisendused</span><span class="sxs-lookup"><span data-stu-id="7bdb9-121">Transformations</span></span>
<span data-ttu-id="7bdb9-122">Tüüpiliselt tuleb muudatus teha ühes kolmest teisendusest.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-122">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="7bdb9-123">Iga teisendus on kirjutatud spetsiifilise standardi jaoks.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-123">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="7bdb9-124">Ressursi nimi</span><span class="sxs-lookup"><span data-stu-id="7bdb9-124">Resource name</span></span>                                         | <span data-ttu-id="7bdb9-125">Faili nimi</span><span class="sxs-lookup"><span data-stu-id="7bdb9-125">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="7bdb9-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="7bdb9-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="7bdb9-127">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="7bdb9-127">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="7bdb9-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="7bdb9-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="7bdb9-129">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="7bdb9-129">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="7bdb9-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="7bdb9-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="7bdb9-131">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="7bdb9-131">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="7bdb9-132">Silumise teisendused</span><span class="sxs-lookup"><span data-stu-id="7bdb9-132">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="7bdb9-133">BAI2 ja MT940 failide korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="7bdb9-133">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="7bdb9-134">BAI2 ja MT940 failid on tekstipõhised failid ja nõuavad korrigeerimist, et lubada XSLT-dokumendi teisenduste (Extensible Stylesheet Language Transformations) silumist</span><span class="sxs-lookup"><span data-stu-id="7bdb9-134">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="7bdb9-135">Programm teeb selle korrigeerimise faili importimisel.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-135">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="7bdb9-136">Looge XML-fail ja kopeerige järgmine tekst sellesse.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-136">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="7bdb9-137">Kopeerige pangaväljavõtte faili sisu ja kleepige need XML-faili, et need asendaks teksti **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-137">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="7bdb9-138">XSLT silumine</span><span class="sxs-lookup"><span data-stu-id="7bdb9-138">Debug the XSLT</span></span>

<span data-ttu-id="7bdb9-139">Lisateabe saamiseks vaadake <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-139">For more information, see <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="7bdb9-140">Käivitage Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-140">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="7bdb9-141">Looge konsooli rakendus.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-141">Create a console application.</span></span>
3.  <span data-ttu-id="7bdb9-142">Avage sobiv XSLT.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-142">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="7bdb9-143">Klõpsake XLST ja selle atribuutide lehekülge.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-143">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="7bdb9-144">Määrake sisend pangaväljavõtte faili asukohale.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-144">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="7bdb9-145">Määratlege väljundi asukoht ja faili nimi.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-145">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="7bdb9-146">Määrake nõutud murdepunktid.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-146">Set the required break points.</span></span>
8.  <span data-ttu-id="7bdb9-147">Menüüs klõpsake valikuid **XML** &gt; **Käivita XSLT silumine**.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-147">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="7bdb9-148">XSLT-väljundi vormindamine</span><span class="sxs-lookup"><span data-stu-id="7bdb9-148">Format the XSLT output</span></span>

<span data-ttu-id="7bdb9-149">Teisenduse käitamisel loob see väljundfaili, mida saate vaadata Visual Studios.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-149">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="7bdb9-150">Kasutage otseteid Ctrl+A, Ctrl+K ja Ctrl+D, et väljundfaili kiiresti vormindada.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-150">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="7bdb9-151">Teisenduse korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="7bdb9-151">Adjust the transformation</span></span>

<span data-ttu-id="7bdb9-152">Korrigeerige teisendust, et saada sobiv väli või element pangaväljavõtte failis.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-152">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="7bdb9-153">Seejärel vastendage see väli või element sobiva Finance and Operationsi elemendiga.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-153">Then map that field or element to the appropriate Finance and Operations element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="7bdb9-154">Deebeti/kreediti indikaator</span><span class="sxs-lookup"><span data-stu-id="7bdb9-154">Debit/credit indicator</span></span>

<span data-ttu-id="7bdb9-155">Mõnikord võib deebetid importida kreedititena ja kreediteid võib importida deebetitena.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-155">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="7bdb9-156">Selle probleemi lahendamiseks peate muutma sobivat XSLT-d.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-156">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="7bdb9-157">Kui pangaväljavõtted tulevad mitmest pangast, veenduge, et need kõik kasutavad sama deebeti/kreediti lähenemist, või looge eraldi teisendused.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-157">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="7bdb9-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator mall</span><span class="sxs-lookup"><span data-stu-id="7bdb9-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="7bdb9-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit mall</span><span class="sxs-lookup"><span data-stu-id="7bdb9-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="7bdb9-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator mall</span><span class="sxs-lookup"><span data-stu-id="7bdb9-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="7bdb9-161">Näited pangaväljavõtte vormingutest ja tehnilistest paigutustest</span><span class="sxs-lookup"><span data-stu-id="7bdb9-161">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="7bdb9-162">Järgmises tabelis on esitatud näited tehnilise paigutuse määratlustest täiustatud panga vastavusseviimise impordifailide ja kolme seotud pangaväljavõtte näidisfailide puhul.</span><span class="sxs-lookup"><span data-stu-id="7bdb9-162">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="7bdb9-163">Näidisfailid ja tehnilised paigutused saab laadida alla siit: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="7bdb9-163">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="7bdb9-164">Tehnilise paigutuse määratlus</span><span class="sxs-lookup"><span data-stu-id="7bdb9-164">Technical layout definition</span></span>                             | <span data-ttu-id="7bdb9-165">Pangaväljavõtte näidisfail</span><span class="sxs-lookup"><span data-stu-id="7bdb9-165">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="7bdb9-166">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="7bdb9-166">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="7bdb9-167">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="7bdb9-167">MT940StatementExample</span></span>                |
| <span data-ttu-id="7bdb9-168">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="7bdb9-168">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="7bdb9-169">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="7bdb9-169">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="7bdb9-170">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="7bdb9-170">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="7bdb9-171">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="7bdb9-171">BAI2StatementExample</span></span>                 |






