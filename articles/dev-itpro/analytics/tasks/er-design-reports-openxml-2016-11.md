---
title: Elektrooniline aruandlus. OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine (november 2016)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab malli elektrooniliste dokumentide loomiseks vormingus OPENXML.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e6b6b16f202af051ccff02051eb438ea49ff6da
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "326649"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="1ec03-103">Elektrooniline aruandlus. OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine (november 2016)</span><span class="sxs-lookup"><span data-stu-id="1ec03-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1ec03-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab malli elektrooniliste dokumentide loomiseks vormingus OPENXML.</span><span class="sxs-lookup"><span data-stu-id="1ec03-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="1ec03-105">Seda konfiguratsiooni kasutatakse hankija maksete töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="1ec03-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="1ec03-106">Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. Neid etappe saab teha ka GBSI ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="1ec03-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="1ec03-107">Etappide lõpuleviimiseks, peate esmalt läbima protseduuri Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine etapid.</span><span class="sxs-lookup"><span data-stu-id="1ec03-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="1ec03-108">Samuti peab teil olema Exceli fail, mis imporditakse malli loomisel.</span><span class="sxs-lookup"><span data-stu-id="1ec03-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="1ec03-109">Sellele failile pääseb juurde [Maksearuande mallist](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="1ec03-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="1ec03-110">Makse andmemudeli konfiguratsiooni üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="1ec03-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="1ec03-111">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="1ec03-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="1ec03-112">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="1ec03-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1ec03-113">Valige konfiguratsiooni pakkuja näidisettevõtte Litware, Inc. jaoks. Kui seda konfiguratsiooni pakkujat ei kuvata, peate esmalt läbima etapid protseduuris Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="1ec03-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="1ec03-114">Klõpsake valikut Määra aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="1ec03-114">Click Set active.</span></span>
4. <span data-ttu-id="1ec03-115">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="1ec03-115">Click Repositories.</span></span>
    * <span data-ttu-id="1ec03-116">Valige võimaluse korral tüübi Operationsi ressursid jaoks hoidla.</span><span class="sxs-lookup"><span data-stu-id="1ec03-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="1ec03-117">Kui see on saadaval, jätke uue hoidla loomise järgmised etapid vahele.</span><span class="sxs-lookup"><span data-stu-id="1ec03-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="1ec03-118">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="1ec03-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="1ec03-119">Sisestage väljale Konfiguratsiooni hoidla tüüp tekst Operatsiooniressursid.</span><span class="sxs-lookup"><span data-stu-id="1ec03-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="1ec03-120">Klõpsake käsku Loo hoidla.</span><span class="sxs-lookup"><span data-stu-id="1ec03-120">Click Create repository.</span></span>
8. <span data-ttu-id="1ec03-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1ec03-121">Click OK.</span></span>
9. <span data-ttu-id="1ec03-122">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="1ec03-122">Click Open.</span></span>
10. <span data-ttu-id="1ec03-123">Valige puul väärtus Maksemudel.</span><span class="sxs-lookup"><span data-stu-id="1ec03-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="1ec03-124">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="1ec03-124">Click Import.</span></span>
    * <span data-ttu-id="1ec03-125">Importige see andmemudel.</span><span class="sxs-lookup"><span data-stu-id="1ec03-125">Import this data model.</span></span> <span data-ttu-id="1ec03-126">Seda kasutatakse andmeallikana uues vormingu konfiguratsioonis.</span><span class="sxs-lookup"><span data-stu-id="1ec03-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="1ec03-127">Jätke see etapp vahele, kui see konfiguratsioon on juba imporditud.</span><span class="sxs-lookup"><span data-stu-id="1ec03-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="1ec03-128">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="1ec03-128">Click Yes.</span></span>
13. <span data-ttu-id="1ec03-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1ec03-129">Close the page.</span></span>
14. <span data-ttu-id="1ec03-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1ec03-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="1ec03-131">Uue vormingu konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="1ec03-131">Create a new format configuration</span></span>
1. <span data-ttu-id="1ec03-132">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="1ec03-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="1ec03-133">Valige puul väärtus Maksemudel.</span><span class="sxs-lookup"><span data-stu-id="1ec03-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="1ec03-134">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="1ec03-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="1ec03-135">Sisestage väljale Uus suvand Andmemudelil PaymentModel põhinev vorming.</span><span class="sxs-lookup"><span data-stu-id="1ec03-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="1ec03-136">Looge vorming, mis põhineb andmemudelil PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="1ec03-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="1ec03-137">Tippige väljale Nimi tekst Töölehe aruande näide.</span><span class="sxs-lookup"><span data-stu-id="1ec03-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="1ec03-138">Töölehe aruande näide</span><span class="sxs-lookup"><span data-stu-id="1ec03-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="1ec03-139">Tippige väljale Kirjeldus tekst Töölehe aruande näide hankijate maksete jaoks.</span><span class="sxs-lookup"><span data-stu-id="1ec03-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="1ec03-140">Töölehe aruande näide hankijate maksete jaoks.</span><span class="sxs-lookup"><span data-stu-id="1ec03-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="1ec03-141">Sisestage või valige väärtus väljal Andmemudeli definitsioon.</span><span class="sxs-lookup"><span data-stu-id="1ec03-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="1ec03-142">Valige määratlus CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="1ec03-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="1ec03-143">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="1ec03-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="1ec03-144">Uue dokumendi koostamine töölehe vormingus OPENXML</span><span class="sxs-lookup"><span data-stu-id="1ec03-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="1ec03-145">Tehke puul valik Maksemudel \ töölehe aruande näide.</span><span class="sxs-lookup"><span data-stu-id="1ec03-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="1ec03-146">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="1ec03-146">Click Designer.</span></span>
3. <span data-ttu-id="1ec03-147">Klõpsake toimingupaanil nuppu Impordi.</span><span class="sxs-lookup"><span data-stu-id="1ec03-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="1ec03-148">Klõpsake käsku Impordi Excelist.</span><span class="sxs-lookup"><span data-stu-id="1ec03-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="1ec03-149">Klõpsake suvandit Manused.</span><span class="sxs-lookup"><span data-stu-id="1ec03-149">Click Attachments.</span></span>
    * <span data-ttu-id="1ec03-150">Manustage olemasolev Exceli dokument mallina.</span><span class="sxs-lookup"><span data-stu-id="1ec03-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="1ec03-151">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="1ec03-151">Click New.</span></span>
7. <span data-ttu-id="1ec03-152">Klõpsake suvandit Fail.</span><span class="sxs-lookup"><span data-stu-id="1ec03-152">Click File.</span></span>
    * <span data-ttu-id="1ec03-153">Osutage olemasolevale Exceli failile.</span><span class="sxs-lookup"><span data-stu-id="1ec03-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="1ec03-154">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1ec03-154">Close the page.</span></span>
9. <span data-ttu-id="1ec03-155">Sisestage või valige väärtus väljal Mall.</span><span class="sxs-lookup"><span data-stu-id="1ec03-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="1ec03-156">Valige manustatud Exceli fail, mida kasutada mallina.</span><span class="sxs-lookup"><span data-stu-id="1ec03-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="1ec03-157">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1ec03-157">Click OK.</span></span>
    * <span data-ttu-id="1ec03-158">Pange tähele, et ER-i vormingu komponendid on loodud kujundamisvormingus viitava MS Exceli dokumendi struktuuri alusel (nimega vahemikud).</span><span class="sxs-lookup"><span data-stu-id="1ec03-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="1ec03-159">Uue andmeallika loomine kogusummade arvutamises valuutakoodide järgi</span><span class="sxs-lookup"><span data-stu-id="1ec03-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="1ec03-160">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="1ec03-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="1ec03-161">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="1ec03-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="1ec03-162">Valige puul väärtus Funktsioonid\grupeerimisalus.</span><span class="sxs-lookup"><span data-stu-id="1ec03-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="1ec03-163">Tippige väljale Nimi tekst PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="1ec03-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="1ec03-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="1ec03-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="1ec03-165">Klõpsake suvandit Grupi redigeerimise alus.</span><span class="sxs-lookup"><span data-stu-id="1ec03-165">Click Edit group by.</span></span>
6. <span data-ttu-id="1ec03-166">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="1ec03-167">Valige puul suvand model\Payments.</span><span class="sxs-lookup"><span data-stu-id="1ec03-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="1ec03-168">Klõpsake suvandit Lisa väli üksusele.</span><span class="sxs-lookup"><span data-stu-id="1ec03-168">Click Add field to.</span></span>
9. <span data-ttu-id="1ec03-169">Klõpsake suvandit Mida grupeerida.</span><span class="sxs-lookup"><span data-stu-id="1ec03-169">Click What to group.</span></span>
10. <span data-ttu-id="1ec03-170">Laiendage puus sõlme model\Payments.</span><span class="sxs-lookup"><span data-stu-id="1ec03-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="1ec03-171">Valige puul väärtus model\Payments\Currency.</span><span class="sxs-lookup"><span data-stu-id="1ec03-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="1ec03-172">Klõpsake suvandit Lisa väli üksusele.</span><span class="sxs-lookup"><span data-stu-id="1ec03-172">Click Add field to.</span></span>
13. <span data-ttu-id="1ec03-173">Klõpsake suvandit Grupeeritud väljad.</span><span class="sxs-lookup"><span data-stu-id="1ec03-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="1ec03-174">Valige puul väärtus model\Payments\Instructed Amount(InstructedAmount).</span><span class="sxs-lookup"><span data-stu-id="1ec03-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="1ec03-175">Klõpsake suvandit Lisa väli üksusele.</span><span class="sxs-lookup"><span data-stu-id="1ec03-175">Click Add field to.</span></span>
16. <span data-ttu-id="1ec03-176">Klõpsake suvandit Kogumi väljad.</span><span class="sxs-lookup"><span data-stu-id="1ec03-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="1ec03-177">Valige suvand väljalt Meetod.</span><span class="sxs-lookup"><span data-stu-id="1ec03-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="1ec03-178">Valige summa liitmisfunktsioon.</span><span class="sxs-lookup"><span data-stu-id="1ec03-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="1ec03-179">Tippige väljale Nimi tekst TotalInstructuredAmount.</span><span class="sxs-lookup"><span data-stu-id="1ec03-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="1ec03-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="1ec03-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="1ec03-181">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="1ec03-181">Click Save.</span></span>
20. <span data-ttu-id="1ec03-182">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1ec03-182">Close the page.</span></span>
21. <span data-ttu-id="1ec03-183">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1ec03-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="1ec03-184">Vormingu komponentide vastendamine andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="1ec03-184">Map format components to data sources</span></span>
1. <span data-ttu-id="1ec03-185">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="1ec03-186">Laiendage puus sõlme model\Payments.</span><span class="sxs-lookup"><span data-stu-id="1ec03-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="1ec03-187">Laiendage puul suvandit model\Payments\Initiating Party(InitiatingParty).</span><span class="sxs-lookup"><span data-stu-id="1ec03-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="1ec03-188">Valige puul väärtus model\Payments\Initiating Party(InitiatingParty)\Name.</span><span class="sxs-lookup"><span data-stu-id="1ec03-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="1ec03-189">Puuvaates laiendage valikut „Excel\ReportHeader”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="1ec03-190">Puuvaates valige „Excel\ReportHeader\CompanyName”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="1ec03-191">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1ec03-191">Click Bind.</span></span>
8. <span data-ttu-id="1ec03-192">Laiendage puus sõlme model\Payments\Creditor.</span><span class="sxs-lookup"><span data-stu-id="1ec03-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="1ec03-193">Laiendage puul suvandit model\Payments\Creditor\Identification.</span><span class="sxs-lookup"><span data-stu-id="1ec03-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="1ec03-194">Tehke puul valik model\Payments\Creditor\Identification\Source ID(SourceID).</span><span class="sxs-lookup"><span data-stu-id="1ec03-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="1ec03-195">Puuvaates laiendage „Excel\PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="1ec03-196">Puuvaates valige „Excel\PaymLines\VendAccountName”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="1ec03-197">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1ec03-197">Click Bind.</span></span>
14. <span data-ttu-id="1ec03-198">Valige puul suvand model\Payments\Creditor\Name.</span><span class="sxs-lookup"><span data-stu-id="1ec03-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="1ec03-199">Puuvaates valige „Excel\PaymLines\VendName”</span><span class="sxs-lookup"><span data-stu-id="1ec03-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="1ec03-200">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1ec03-200">Click Bind.</span></span>
17. <span data-ttu-id="1ec03-201">Laiendage puul valikut model\Payments\Creditor Agent(CreditorAgent).</span><span class="sxs-lookup"><span data-stu-id="1ec03-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="1ec03-202">Tehke puul valik model\Payments\Creditor Agent(CreditorAgent)\Name.</span><span class="sxs-lookup"><span data-stu-id="1ec03-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="1ec03-203">Puuvaates valige „Excel\PaymLines\Pank”</span><span class="sxs-lookup"><span data-stu-id="1ec03-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="1ec03-204">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1ec03-204">Click Bind.</span></span>
21. <span data-ttu-id="1ec03-205">Tehke puul valik model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber).</span><span class="sxs-lookup"><span data-stu-id="1ec03-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="1ec03-206">Puuvaates valige „Excel\PaymLines\RoutingNumber”</span><span class="sxs-lookup"><span data-stu-id="1ec03-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="1ec03-207">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1ec03-207">Click Bind.</span></span>
24. <span data-ttu-id="1ec03-208">Laiendage puus sõlme „model\Payments\Creditor Account(CreditorAccount)”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="1ec03-209">Laiendage puus sõlme „model\Payments\Creditor Account(CreditorAccount)\Identification”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="1ec03-210">Tehke puus valik model\Payments\Creditor Account(CreditorAccount)\Identification\Number.</span><span class="sxs-lookup"><span data-stu-id="1ec03-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="1ec03-211">Puuvaates valige „Excel\PaymLines\AccountNumber”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="1ec03-212">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1ec03-212">Click Bind.</span></span>
29. <span data-ttu-id="1ec03-213">Valige puul väärtus model\Payments\Instructed Amount(InstructedAmount).</span><span class="sxs-lookup"><span data-stu-id="1ec03-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="1ec03-214">Puuvaates valige „Excel\PaymLines\Deebet”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="1ec03-215">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1ec03-215">Click Bind.</span></span>
32. <span data-ttu-id="1ec03-216">Laiendage puus sõlme model\Payments\Creditor.</span><span class="sxs-lookup"><span data-stu-id="1ec03-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="1ec03-217">Laiendage puus sõlme „model\Payments\Creditor Account(CreditorAccount)”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="1ec03-218">Laiendage puul valikut model\Payments\Creditor Agent(CreditorAgent).</span><span class="sxs-lookup"><span data-stu-id="1ec03-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="1ec03-219">Valige puul väärtus model\Payments\Currency.</span><span class="sxs-lookup"><span data-stu-id="1ec03-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="1ec03-220">Puuvaates valige „Excel\PaymLines\Valuuta”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="1ec03-221">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1ec03-221">Click Bind.</span></span>
38. <span data-ttu-id="1ec03-222">Laiendage puul valikut PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="1ec03-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="1ec03-223">Laiendage puul valikut PaymentByCurrency\grouped.</span><span class="sxs-lookup"><span data-stu-id="1ec03-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="1ec03-224">Tehke puul valik PaymentByCurrency\grouped\Currency.</span><span class="sxs-lookup"><span data-stu-id="1ec03-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="1ec03-225">Puuvaates laiendage valikut „Excel\SummaryLines”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="1ec03-226">Puuvaates valige „Excel\SummaryLines\SummaryCurrency”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="1ec03-227">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1ec03-227">Click Bind.</span></span>
44. <span data-ttu-id="1ec03-228">Laiendage puul valikut PaymentByCurrency\aggregated.</span><span class="sxs-lookup"><span data-stu-id="1ec03-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="1ec03-229">Tehke puul valik PaymentByCurrency\aggregated\TotalInstructuredAmount.</span><span class="sxs-lookup"><span data-stu-id="1ec03-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="1ec03-230">Puuvaates valige „Excel\SummaryLines\SummaryAmount”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="1ec03-231">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1ec03-231">Click Bind.</span></span>
48. <span data-ttu-id="1ec03-232">Tehke puul valik PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="1ec03-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="1ec03-233">Puuvaates valige „Excel\SummaryLines”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="1ec03-234">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1ec03-234">Click Bind.</span></span>
51. <span data-ttu-id="1ec03-235">Valige puul suvand model\Payments.</span><span class="sxs-lookup"><span data-stu-id="1ec03-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="1ec03-236">Puuvaates valige „Excel\PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="1ec03-237">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="1ec03-237">Click Bind.</span></span>
54. <span data-ttu-id="1ec03-238">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="1ec03-238">Click Save.</span></span>
55. <span data-ttu-id="1ec03-239">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1ec03-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="1ec03-240">Loodud konfiguratsiooni kasutamine maksete töötlemiseks</span><span class="sxs-lookup"><span data-stu-id="1ec03-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="1ec03-241">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="1ec03-241">Click Change status.</span></span>
2. <span data-ttu-id="1ec03-242">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="1ec03-242">Click Complete.</span></span>
3. <span data-ttu-id="1ec03-243">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1ec03-243">Click OK.</span></span>
4. <span data-ttu-id="1ec03-244">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1ec03-244">Close the page.</span></span>
5. <span data-ttu-id="1ec03-245">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1ec03-245">Close the page.</span></span>
6. <span data-ttu-id="1ec03-246">Avage Ostureskontro > Makse seadistus > Makseviisid.</span><span class="sxs-lookup"><span data-stu-id="1ec03-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="1ec03-247">Kasutage kiirfiltrit, et filtreerida välja Makseviis väärtusega „Elektrooniline”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="1ec03-248">Elektrooniline</span><span class="sxs-lookup"><span data-stu-id="1ec03-248">Electronic</span></span>  
8. <span data-ttu-id="1ec03-249">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="1ec03-249">Click Edit.</span></span>
9. <span data-ttu-id="1ec03-250">Laiendage jaotist Failivormingud.</span><span class="sxs-lookup"><span data-stu-id="1ec03-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="1ec03-251">Valige väljal Üldine elektrooniline aruandlus suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="1ec03-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="1ec03-252">Sisestage väärtus väljale Ekspordivormingu konfiguratsioon või valige see.</span><span class="sxs-lookup"><span data-stu-id="1ec03-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="1ec03-253">Valige konfiguratsioon Töölehe aruande näide.</span><span class="sxs-lookup"><span data-stu-id="1ec03-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="1ec03-254">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="1ec03-254">Click Save.</span></span>
13. <span data-ttu-id="1ec03-255">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1ec03-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="1ec03-256">Loodud konfiguratsiooni kasutamine makse töölehtede töötlemise testimiseks</span><span class="sxs-lookup"><span data-stu-id="1ec03-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="1ec03-257">Avage Ostureskontro > Maksed > Makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="1ec03-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="1ec03-258">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="1ec03-258">Click New.</span></span>
    * <span data-ttu-id="1ec03-259">Looge uus maksetööleht.</span><span class="sxs-lookup"><span data-stu-id="1ec03-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="1ec03-260">Sisestage väljale Nimi tekst „VendPay”.</span><span class="sxs-lookup"><span data-stu-id="1ec03-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="1ec03-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="1ec03-261">VendPay</span></span>  
4. <span data-ttu-id="1ec03-262">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="1ec03-262">Click Lines.</span></span>
5. <span data-ttu-id="1ec03-263">Määrake väljal Konto väärtused GB_SI_000001.</span><span class="sxs-lookup"><span data-stu-id="1ec03-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="1ec03-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="1ec03-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="1ec03-265">Määrake suvandi Deebet väärtuseks 1000.</span><span class="sxs-lookup"><span data-stu-id="1ec03-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="1ec03-266">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="1ec03-266">Click New.</span></span>
8. <span data-ttu-id="1ec03-267">Määrake väljal Konto väärtused GB_SI_000005.</span><span class="sxs-lookup"><span data-stu-id="1ec03-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="1ec03-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="1ec03-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="1ec03-269">Määrake suvandi Deebet väärtuseks 2000.</span><span class="sxs-lookup"><span data-stu-id="1ec03-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="1ec03-270">Tippige väljale Valuuta väärtus EUR.</span><span class="sxs-lookup"><span data-stu-id="1ec03-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="1ec03-271"> eurot</span><span class="sxs-lookup"><span data-stu-id="1ec03-271">EUR</span></span>  
11. <span data-ttu-id="1ec03-272">Määrake väljal Vastaskonto väärtused GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="1ec03-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="1ec03-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="1ec03-273">GBSI OPER</span></span>  
12. <span data-ttu-id="1ec03-274">Tippige väljale Makseviis tekst Elektrooniline.</span><span class="sxs-lookup"><span data-stu-id="1ec03-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="1ec03-275">Elektrooniline</span><span class="sxs-lookup"><span data-stu-id="1ec03-275">Electronic</span></span>  
13. <span data-ttu-id="1ec03-276">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="1ec03-276">Click Save.</span></span>
14. <span data-ttu-id="1ec03-277">Klõpsake valikut Loo maksed.</span><span class="sxs-lookup"><span data-stu-id="1ec03-277">Click Generate payments.</span></span>
15. <span data-ttu-id="1ec03-278">Tippige väljale Makseviis tekst Elektrooniline.</span><span class="sxs-lookup"><span data-stu-id="1ec03-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="1ec03-279">Elektrooniline</span><span class="sxs-lookup"><span data-stu-id="1ec03-279">Electronic</span></span>  
16. <span data-ttu-id="1ec03-280">Väljale Failinimi tippige Maksed.</span><span class="sxs-lookup"><span data-stu-id="1ec03-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="1ec03-281">Tippige näiteks tekst Maksed.</span><span class="sxs-lookup"><span data-stu-id="1ec03-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="1ec03-282">Tippige väljale Pangakonto tekst GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="1ec03-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="1ec03-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="1ec03-283">GBSI OPER</span></span>  
18. <span data-ttu-id="1ec03-284">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1ec03-284">Click OK.</span></span>
19. <span data-ttu-id="1ec03-285">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="1ec03-285">Click OK.</span></span>
    * <span data-ttu-id="1ec03-286">Vaadake loodud tööleht üle, sh makseridade üksikasjad kui ka selles makseteates kasutatud iga valuutakoodi summad.</span><span class="sxs-lookup"><span data-stu-id="1ec03-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  

