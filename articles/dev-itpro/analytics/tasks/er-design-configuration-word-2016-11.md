--- 
title: Elektroonilise aruandluse (ER) Microsoft Wordi vormingus aruannete genereerimiseks konfiguratsiooni koostamine
description: "Järgmine etapp selgitab, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis olev kasutaja saab konfigureerida elektroonilise aruandluse (ER) vorminguid, et luua aruandeid Microsoft Word failidena."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e85a4cd660300dc526ad7da3aece41bc95fd9bdc
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="design-a-configuration-for-generating-reports-in-microsoft-word-format-for-electronic-reporting-er"></a><span data-ttu-id="4995e-103">Elektroonilise aruandluse (ER) Microsoft Wordi vormingus aruannete genereerimiseks konfiguratsiooni koostamine</span><span class="sxs-lookup"><span data-stu-id="4995e-103">Design a configuration for generating reports in Microsoft Word format for electronic reporting (ER)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4995e-104">Järgmine etapp selgitab, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis olev kasutaja saab konfigureerida elektroonilise aruandluse (ER) vorminguid, et luua aruandeid Microsoft Word failidena.</span><span class="sxs-lookup"><span data-stu-id="4995e-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="4995e-105">Neid toiminguid saab teha GBSI ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="4995e-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="4995e-106">Nende etappide lõpuleviimiseks peate esmalt läbima tegevusejuhises „ER-i konfiguratsiooni loomine aruannete loomiseks vormingus OPENXML” esitatud etapid.</span><span class="sxs-lookup"><span data-stu-id="4995e-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="4995e-107">Eelnevalt peate näidisaruande jaoks alla laadima ja kohalikult salvestama ka järgmised mallid:</span><span class="sxs-lookup"><span data-stu-id="4995e-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

[<span data-ttu-id="4995e-108">Maksearuande mall</span><span class="sxs-lookup"><span data-stu-id="4995e-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

[<span data-ttu-id="4995e-109">Maksearuande piiratud mall</span><span class="sxs-lookup"><span data-stu-id="4995e-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="4995e-110">See protseduur on funktsiooni jaoks, mis lisati rakenduse Microsoft Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="4995e-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="4995e-111">Olemasoleva elektroonilise aruandluse aruande konfiguratsiooni valimine</span><span class="sxs-lookup"><span data-stu-id="4995e-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="4995e-112">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="4995e-112">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="4995e-113">Veenduge, et konfiguratsiooni pakkuja Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="4995e-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="4995e-114">on valitud aktiivsena.</span><span class="sxs-lookup"><span data-stu-id="4995e-114">is selected as active.</span></span>  
2. <span data-ttu-id="4995e-115">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="4995e-115">Click Reporting configurations.</span></span>
    * <span data-ttu-id="4995e-116">Taaskasutame olemasolevat elektroonilise aruandluse konfiguratsiooni, mis on algselt mõeldud aruande väljundi loomiseks OPENXML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="4995e-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="4995e-117">Laiendage puus sõlme „Payment model”.</span><span class="sxs-lookup"><span data-stu-id="4995e-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="4995e-118">Tehke puul valik Maksemudel \ töölehe aruande näide.</span><span class="sxs-lookup"><span data-stu-id="4995e-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="4995e-119">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="4995e-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="4995e-120">Exceli malli asendamine Wordi malliga</span><span class="sxs-lookup"><span data-stu-id="4995e-120">Replace the Excel template with the Word template</span></span>
    * <span data-ttu-id="4995e-121">Praegu kasutatakse Exceli dokumenti mallina väljundi loomiseks OPENXML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="4995e-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="4995e-122">Impordime aruande malli Wordi vormingus.</span><span class="sxs-lookup"><span data-stu-id="4995e-122">We will import the report’s template in Word format.</span></span>  
1. <span data-ttu-id="4995e-123">Klõpsake suvandit Manused.</span><span class="sxs-lookup"><span data-stu-id="4995e-123">Click Attachments.</span></span>
    * <span data-ttu-id="4995e-124">Asendage olemasolev Exceli mall varem allalaaditud Wordi malliga (Maksearuande mall).</span><span class="sxs-lookup"><span data-stu-id="4995e-124">Replace the existing Excel template with the Word template that you downloaded earlier, Template of Payment Report.</span></span> <span data-ttu-id="4995e-125">Pange tähele, et see mall sisaldab ainult sellise dokumendi paigutust, mida soovime luua elektroonilise aruandluse väljundina.</span><span class="sxs-lookup"><span data-stu-id="4995e-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="4995e-126">Klõpsake  Kustuta.</span><span class="sxs-lookup"><span data-stu-id="4995e-126">Click Delete.</span></span>
3. <span data-ttu-id="4995e-127">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="4995e-127">Click Yes.</span></span>
4. <span data-ttu-id="4995e-128">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="4995e-128">Click New.</span></span>
5. <span data-ttu-id="4995e-129">Klõpsake suvandit Fail.</span><span class="sxs-lookup"><span data-stu-id="4995e-129">Click File.</span></span>
6. <span data-ttu-id="4995e-130">Klõpsake käsku Sirvi.</span><span class="sxs-lookup"><span data-stu-id="4995e-130">Click Browse.</span></span> <span data-ttu-id="4995e-131">Navigeerige asukohta ja valige varasemalt allalaaditud SampleVendPaymDocReport.docx.</span><span class="sxs-lookup"><span data-stu-id="4995e-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="4995e-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="4995e-132">Click OK.</span></span>
    * <span data-ttu-id="4995e-133">Valige eelmises etapis allalaaditud mall.</span><span class="sxs-lookup"><span data-stu-id="4995e-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="4995e-134">Sisestage või valige väärtus väljal Mall.</span><span class="sxs-lookup"><span data-stu-id="4995e-134">In the Template field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="4995e-135">Kohandatud XML-i osa lisamise abil Wordi malli laiendamine</span><span class="sxs-lookup"><span data-stu-id="4995e-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="4995e-136">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="4995e-136">Click Save.</span></span>
    * <span data-ttu-id="4995e-137">Lisaks konfiguratsiooni muudatuste salvestamisele värskendab toiming Salvesta ka manustatud Wordi malli.</span><span class="sxs-lookup"><span data-stu-id="4995e-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="4995e-138">Kujundatud vormingu struktuur porditakse manustatud Wordi dokumenti uue kohandatud XML-i osana, mille nimi on „Aruanne”.</span><span class="sxs-lookup"><span data-stu-id="4995e-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="4995e-139">Pange tähele, et manustatud Wordi mall sisaldab mitte ainult sellise dokumendi paigutust, mida soovime luua elektroonilise aruandluse väljundina, vaid see sisaldab ka andmete struktuuri, mille elektrooniline aruandlus sisestab käitusajal sellesse malli.</span><span class="sxs-lookup"><span data-stu-id="4995e-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="4995e-140">Klõpsake suvandit Manused.</span><span class="sxs-lookup"><span data-stu-id="4995e-140">Click Attachments.</span></span>
    * <span data-ttu-id="4995e-141">Nüüd peate siduma kohandatud XML-i osa „Aruanne” elemendid Wordi dokumendi osadega.</span><span class="sxs-lookup"><span data-stu-id="4995e-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    * <span data-ttu-id="4995e-142">Kui olete tuttav Wordi dokumentidega, mida saab kujundada vormidena, mis sisaldavad kohandatud XML-i osade elementidega seotud sisu juhtelemente – läbige sellise dokumendi loomiseks kõik järgmises alamülesandes olevad etapid.</span><span class="sxs-lookup"><span data-stu-id="4995e-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="4995e-143">Lisateabe saamiseks klõpsake linki https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span><span class="sxs-lookup"><span data-stu-id="4995e-143">For more details, see this link https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span></span> <span data-ttu-id="4995e-144">Vastasel juhul jätke vahele järgmise alamülesande etapid.</span><span class="sxs-lookup"><span data-stu-id="4995e-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="4995e-145">Andmete sidumiste tegemiseks kohandatud XML-i osaga Wordi hankimine</span><span class="sxs-lookup"><span data-stu-id="4995e-145">Get Word with custom XML part to do data bindings</span></span>
    * <span data-ttu-id="4995e-146">Avage see dokument Wordis ja tehke järgmist. Avage Wordi vahekaart Arendaja (kohandage linti, kui see pole veel lubatud).</span><span class="sxs-lookup"><span data-stu-id="4995e-146">Open this document in Word and do the following:  - Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>  <span data-ttu-id="4995e-147">- Valige XML-i vastendamise paan.</span><span class="sxs-lookup"><span data-stu-id="4995e-147">- Select XML mapping pane.</span></span>  <span data-ttu-id="4995e-148">- Valige otsingust kohandatud XML-i osa „Aruanne”.</span><span class="sxs-lookup"><span data-stu-id="4995e-148">- Select the ‘Report’ custom XML part in the lookup.</span></span>  <span data-ttu-id="4995e-149">- Tehke valitud kohandatud XML-i osa elementide ja Wordi dokumendi sisu juhtelementide vastendamine.</span><span class="sxs-lookup"><span data-stu-id="4995e-149">- Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="4995e-150">- Salvestage värskendatud Wordi dokument kohalikule kettale.</span><span class="sxs-lookup"><span data-stu-id="4995e-150">- Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="4995e-151">Wordi malli üleslaadimine sisu juhtelementidega seotud kohandatud XML-i osaga</span><span class="sxs-lookup"><span data-stu-id="4995e-151">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="4995e-152">Klõpsake  Kustuta.</span><span class="sxs-lookup"><span data-stu-id="4995e-152">Click Delete.</span></span>
2. <span data-ttu-id="4995e-153">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="4995e-153">Click Yes.</span></span>
    * <span data-ttu-id="4995e-154">Lisage uus mall.</span><span class="sxs-lookup"><span data-stu-id="4995e-154">Add a new template.</span></span> <span data-ttu-id="4995e-155">Kui viisite lõpule eelmises alamülesandes esitatud etapid, valige ettevalmistatud ja kohalikult salvestatud Wordi dokument.</span><span class="sxs-lookup"><span data-stu-id="4995e-155">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="4995e-156">Vastasel juhul valige varasemalt allalaaditud MS Wordi mall SampleVendPaymDocReportBounded.docx.</span><span class="sxs-lookup"><span data-stu-id="4995e-156">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="4995e-157">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="4995e-157">Click New.</span></span>
4. <span data-ttu-id="4995e-158">Klõpsake suvandit Fail.</span><span class="sxs-lookup"><span data-stu-id="4995e-158">Click File.</span></span>
5. <span data-ttu-id="4995e-159">Klõpsake käsku Sirvi.</span><span class="sxs-lookup"><span data-stu-id="4995e-159">Click Browse.</span></span> <span data-ttu-id="4995e-160">Navigeerige asukohta ja valige varasemalt allalaaditud SampleVendPaymDocReportBounded.docx.</span><span class="sxs-lookup"><span data-stu-id="4995e-160">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="4995e-161">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="4995e-161">Click OK.</span></span>
6. <span data-ttu-id="4995e-162">Väljal Mall valige eelmises etapis allalaaditud dokument.</span><span class="sxs-lookup"><span data-stu-id="4995e-162">In the Template field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="4995e-163">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="4995e-163">Click Save.</span></span>
8. <span data-ttu-id="4995e-164">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4995e-164">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="4995e-165">Wordi väljundi loomiseks vormingu käivitamine</span><span class="sxs-lookup"><span data-stu-id="4995e-165">Execute the format to create Word output</span></span>
1. <span data-ttu-id="4995e-166">Klõpsake tegumiribal valikut Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="4995e-166">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="4995e-167">Klõpsake valikut Kasutaja parameetrid.</span><span class="sxs-lookup"><span data-stu-id="4995e-167">Click User parameters.</span></span>
3. <span data-ttu-id="4995e-168">Tehke väljal Käivita sätted valik Jah.</span><span class="sxs-lookup"><span data-stu-id="4995e-168">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="4995e-169">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="4995e-169">Click OK.</span></span>
5. <span data-ttu-id="4995e-170">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="4995e-170">Click Edit.</span></span>
6. <span data-ttu-id="4995e-171">Tehke väljal Käivita mustand valik Jah.</span><span class="sxs-lookup"><span data-stu-id="4995e-171">Select Yes in the Run Draft field.</span></span>
7. <span data-ttu-id="4995e-172">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="4995e-172">Click Save.</span></span>
8. <span data-ttu-id="4995e-173">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4995e-173">Close the page.</span></span>
9. <span data-ttu-id="4995e-174">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4995e-174">Close the page.</span></span>
10. <span data-ttu-id="4995e-175">Avage Ostureskontro > Maksed > Makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="4995e-175">Go to Accounts payable > Payments > Payment journal.</span></span>
11. <span data-ttu-id="4995e-176">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="4995e-176">Click Lines.</span></span>
12. <span data-ttu-id="4995e-177">Märkige või tühjendage loendis kõik read.</span><span class="sxs-lookup"><span data-stu-id="4995e-177">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="4995e-178">Klõpsake suvandit Makse olek.</span><span class="sxs-lookup"><span data-stu-id="4995e-178">Click Payment status.</span></span>
14. <span data-ttu-id="4995e-179">Klõpsake nuppu Puudub.</span><span class="sxs-lookup"><span data-stu-id="4995e-179">Click None.</span></span>
15. <span data-ttu-id="4995e-180">Klõpsake valikut Loo maksed.</span><span class="sxs-lookup"><span data-stu-id="4995e-180">Click Generate payments.</span></span>
16. <span data-ttu-id="4995e-181">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="4995e-181">Click OK.</span></span>
17. <span data-ttu-id="4995e-182">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="4995e-182">Click OK.</span></span>
    * <span data-ttu-id="4995e-183">Analüüsige loodud väljundit.</span><span class="sxs-lookup"><span data-stu-id="4995e-183">Analyze the generated output.</span></span> <span data-ttu-id="4995e-184">Pange tähele, et loodud väljundit esitatakse Wordi vormingus ja sisaldab töödeldud maksete üksikasju.</span><span class="sxs-lookup"><span data-stu-id="4995e-184">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  


