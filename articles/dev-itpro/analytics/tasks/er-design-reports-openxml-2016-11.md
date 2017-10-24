--- 
title: Elektroonilise aruandluse (ER) jaoks OpenXML-i vormingus aruannete genereerimiseks konfiguratsiooni koostamine
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab malli elektrooniliste dokumentide loomiseks vormingus OPENXML."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 04def14ddf9b079005bf11acbcaf64b21aa80fdb
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="da8ea-103">Elektroonilise aruandluse (ER) jaoks OpenXML-i vormingus aruannete genereerimiseks konfiguratsiooni koostamine</span><span class="sxs-lookup"><span data-stu-id="da8ea-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da8ea-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab malli elektrooniliste dokumentide loomiseks vormingus OPENXML.</span><span class="sxs-lookup"><span data-stu-id="da8ea-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="da8ea-105">Seda konfiguratsiooni kasutatakse hankija maksete töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="da8ea-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="da8ea-106">Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. Neid etappe saab teha ka GBSI ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="da8ea-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="da8ea-107">Etappide lõpuleviimiseks, peate esmalt läbima protseduuri Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine etapid.</span><span class="sxs-lookup"><span data-stu-id="da8ea-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="da8ea-108">Samuti peab teil olema Exceli fail, mis imporditakse malli loomisel.</span><span class="sxs-lookup"><span data-stu-id="da8ea-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="da8ea-109">Selle faili saab avada siin: https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span><span class="sxs-lookup"><span data-stu-id="da8ea-109">This file can be accessed from:  https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="da8ea-110">Makse andmemudeli konfiguratsiooni üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="da8ea-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="da8ea-111">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="da8ea-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="da8ea-112">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="da8ea-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="da8ea-113">Valige konfiguratsiooni pakkuja näidisettevõtte Litware, Inc. jaoks. Kui seda konfiguratsiooni pakkujat ei kuvata, peate esmalt läbima etapid protseduuris Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="da8ea-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="da8ea-114">Klõpsake valikut Määra aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="da8ea-114">Click Set active.</span></span>
4. <span data-ttu-id="da8ea-115">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="da8ea-115">Click Repositories.</span></span>
    * <span data-ttu-id="da8ea-116">Valige võimaluse korral tüübi Operationsi ressursid jaoks hoidla.</span><span class="sxs-lookup"><span data-stu-id="da8ea-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="da8ea-117">Kui see on saadaval, jätke uue hoidla loomise järgmised etapid vahele.</span><span class="sxs-lookup"><span data-stu-id="da8ea-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="da8ea-118">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="da8ea-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="da8ea-119">Sisestage väljale Konfiguratsiooni hoidla tüüp tekst Operatsiooniressursid.</span><span class="sxs-lookup"><span data-stu-id="da8ea-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="da8ea-120">Klõpsake käsku Loo hoidla.</span><span class="sxs-lookup"><span data-stu-id="da8ea-120">Click Create repository.</span></span>
8. <span data-ttu-id="da8ea-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="da8ea-121">Click OK.</span></span>
9. <span data-ttu-id="da8ea-122">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="da8ea-122">Click Open.</span></span>
10. <span data-ttu-id="da8ea-123">Valige puul väärtus Maksemudel.</span><span class="sxs-lookup"><span data-stu-id="da8ea-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="da8ea-124">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="da8ea-124">Click Import.</span></span>
    * <span data-ttu-id="da8ea-125">Importige see andmemudel.</span><span class="sxs-lookup"><span data-stu-id="da8ea-125">Import this data model.</span></span> <span data-ttu-id="da8ea-126">Seda kasutatakse andmeallikana uues vormingu konfiguratsioonis.</span><span class="sxs-lookup"><span data-stu-id="da8ea-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="da8ea-127">Jätke see etapp vahele, kui see konfiguratsioon on juba imporditud.</span><span class="sxs-lookup"><span data-stu-id="da8ea-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="da8ea-128">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="da8ea-128">Click Yes.</span></span>
13. <span data-ttu-id="da8ea-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da8ea-129">Close the page.</span></span>
14. <span data-ttu-id="da8ea-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da8ea-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="da8ea-131">Uue vormingu konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="da8ea-131">Create a new format configuration</span></span>
1. <span data-ttu-id="da8ea-132">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="da8ea-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="da8ea-133">Valige puul väärtus Maksemudel.</span><span class="sxs-lookup"><span data-stu-id="da8ea-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="da8ea-134">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="da8ea-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="da8ea-135">Sisestage väljale Uus suvand Andmemudelil PaymentModel põhinev vorming.</span><span class="sxs-lookup"><span data-stu-id="da8ea-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="da8ea-136">Looge vorming, mis põhineb andmemudelil PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="da8ea-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="da8ea-137">Tippige väljale Nimi tekst Töölehe aruande näide.</span><span class="sxs-lookup"><span data-stu-id="da8ea-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="da8ea-138">Töölehe aruande näide</span><span class="sxs-lookup"><span data-stu-id="da8ea-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="da8ea-139">Tippige väljale Kirjeldus tekst Töölehe aruande näide hankijate maksete jaoks.</span><span class="sxs-lookup"><span data-stu-id="da8ea-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="da8ea-140">Töölehe aruande näide hankijate maksete jaoks.</span><span class="sxs-lookup"><span data-stu-id="da8ea-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="da8ea-141">Sisestage või valige väärtus väljal Andmemudeli definitsioon.</span><span class="sxs-lookup"><span data-stu-id="da8ea-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="da8ea-142">Valige määratlus CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="da8ea-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="da8ea-143">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="da8ea-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="da8ea-144">Uue dokumendi koostamine töölehe vormingus OPENXML</span><span class="sxs-lookup"><span data-stu-id="da8ea-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="da8ea-145">Tehke puul valik Maksemudel \ töölehe aruande näide.</span><span class="sxs-lookup"><span data-stu-id="da8ea-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="da8ea-146">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="da8ea-146">Click Designer.</span></span>
3. <span data-ttu-id="da8ea-147">Klõpsake toimingupaanil nuppu Impordi.</span><span class="sxs-lookup"><span data-stu-id="da8ea-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="da8ea-148">Klõpsake käsku Impordi Excelist.</span><span class="sxs-lookup"><span data-stu-id="da8ea-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="da8ea-149">Klõpsake suvandit Manused.</span><span class="sxs-lookup"><span data-stu-id="da8ea-149">Click Attachments.</span></span>
    * <span data-ttu-id="da8ea-150">Manustage olemasolev Exceli dokument mallina.</span><span class="sxs-lookup"><span data-stu-id="da8ea-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="da8ea-151">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="da8ea-151">Click New.</span></span>
7. <span data-ttu-id="da8ea-152">Klõpsake suvandit Fail.</span><span class="sxs-lookup"><span data-stu-id="da8ea-152">Click File.</span></span>
    * <span data-ttu-id="da8ea-153">Osutage olemasolevale Exceli failile.</span><span class="sxs-lookup"><span data-stu-id="da8ea-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="da8ea-154">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da8ea-154">Close the page.</span></span>
9. <span data-ttu-id="da8ea-155">Sisestage või valige väärtus väljal Mall.</span><span class="sxs-lookup"><span data-stu-id="da8ea-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="da8ea-156">Valige manustatud Exceli fail, mida kasutada mallina.</span><span class="sxs-lookup"><span data-stu-id="da8ea-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="da8ea-157">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="da8ea-157">Click OK.</span></span>
    * <span data-ttu-id="da8ea-158">Pange tähele, et ER-i vormingu komponendid on loodud kujundamisvormingus viitava MS Exceli dokumendi struktuuri alusel (nimega vahemikud).</span><span class="sxs-lookup"><span data-stu-id="da8ea-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="da8ea-159">Uue andmeallika loomine kogusummade arvutamises valuutakoodide järgi</span><span class="sxs-lookup"><span data-stu-id="da8ea-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="da8ea-160">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="da8ea-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="da8ea-161">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="da8ea-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="da8ea-162">Valige puul väärtus Funktsioonid\grupeerimisalus.</span><span class="sxs-lookup"><span data-stu-id="da8ea-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="da8ea-163">Tippige väljale Nimi tekst PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="da8ea-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="da8ea-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="da8ea-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="da8ea-165">Klõpsake suvandit Grupi redigeerimise alus.</span><span class="sxs-lookup"><span data-stu-id="da8ea-165">Click Edit group by.</span></span>
6. <span data-ttu-id="da8ea-166">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="da8ea-167">Valige puul suvand model\Payments.</span><span class="sxs-lookup"><span data-stu-id="da8ea-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="da8ea-168">Klõpsake suvandit Lisa väli üksusele.</span><span class="sxs-lookup"><span data-stu-id="da8ea-168">Click Add field to.</span></span>
9. <span data-ttu-id="da8ea-169">Klõpsake suvandit Mida grupeerida.</span><span class="sxs-lookup"><span data-stu-id="da8ea-169">Click What to group.</span></span>
10. <span data-ttu-id="da8ea-170">Laiendage puus sõlme model\Payments.</span><span class="sxs-lookup"><span data-stu-id="da8ea-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="da8ea-171">Valige puul väärtus model\Payments\Currency.</span><span class="sxs-lookup"><span data-stu-id="da8ea-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="da8ea-172">Klõpsake suvandit Lisa väli üksusele.</span><span class="sxs-lookup"><span data-stu-id="da8ea-172">Click Add field to.</span></span>
13. <span data-ttu-id="da8ea-173">Klõpsake suvandit Grupeeritud väljad.</span><span class="sxs-lookup"><span data-stu-id="da8ea-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="da8ea-174">Valige puul väärtus model\Payments\Instructed Amount(InstructedAmount).</span><span class="sxs-lookup"><span data-stu-id="da8ea-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="da8ea-175">Klõpsake suvandit Lisa väli üksusele.</span><span class="sxs-lookup"><span data-stu-id="da8ea-175">Click Add field to.</span></span>
16. <span data-ttu-id="da8ea-176">Klõpsake suvandit Kogumi väljad.</span><span class="sxs-lookup"><span data-stu-id="da8ea-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="da8ea-177">Valige suvand väljalt Meetod.</span><span class="sxs-lookup"><span data-stu-id="da8ea-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="da8ea-178">Valige summa liitmisfunktsioon.</span><span class="sxs-lookup"><span data-stu-id="da8ea-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="da8ea-179">Tippige väljale Nimi tekst TotalInstructuredAmount.</span><span class="sxs-lookup"><span data-stu-id="da8ea-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="da8ea-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="da8ea-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="da8ea-181">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="da8ea-181">Click Save.</span></span>
20. <span data-ttu-id="da8ea-182">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da8ea-182">Close the page.</span></span>
21. <span data-ttu-id="da8ea-183">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="da8ea-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="da8ea-184">Vormingu komponentide vastendamine andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="da8ea-184">Map format components to data sources</span></span>
1. <span data-ttu-id="da8ea-185">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="da8ea-186">Laiendage puus sõlme model\Payments.</span><span class="sxs-lookup"><span data-stu-id="da8ea-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="da8ea-187">Laiendage puul suvandit model\Payments\Initiating Party(InitiatingParty).</span><span class="sxs-lookup"><span data-stu-id="da8ea-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="da8ea-188">Valige puul väärtus model\Payments\Initiating Party(InitiatingParty)\Name.</span><span class="sxs-lookup"><span data-stu-id="da8ea-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="da8ea-189">Puuvaates laiendage valikut „Excel\ReportHeader”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="da8ea-190">Puuvaates valige „Excel\ReportHeader\CompanyName”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="da8ea-191">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="da8ea-191">Click Bind.</span></span>
8. <span data-ttu-id="da8ea-192">Laiendage puus sõlme model\Payments\Creditor.</span><span class="sxs-lookup"><span data-stu-id="da8ea-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="da8ea-193">Laiendage puul suvandit model\Payments\Creditor\Identification.</span><span class="sxs-lookup"><span data-stu-id="da8ea-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="da8ea-194">Tehke puul valik model\Payments\Creditor\Identification\Source ID(SourceID).</span><span class="sxs-lookup"><span data-stu-id="da8ea-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="da8ea-195">Puuvaates laiendage „Excel\PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="da8ea-196">Puuvaates valige „Excel\PaymLines\VendAccountName”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="da8ea-197">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="da8ea-197">Click Bind.</span></span>
14. <span data-ttu-id="da8ea-198">Valige puul suvand model\Payments\Creditor\Name.</span><span class="sxs-lookup"><span data-stu-id="da8ea-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="da8ea-199">Puuvaates valige „Excel\PaymLines\VendName”</span><span class="sxs-lookup"><span data-stu-id="da8ea-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="da8ea-200">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="da8ea-200">Click Bind.</span></span>
17. <span data-ttu-id="da8ea-201">Laiendage puul valikut model\Payments\Creditor Agent(CreditorAgent).</span><span class="sxs-lookup"><span data-stu-id="da8ea-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="da8ea-202">Tehke puul valik model\Payments\Creditor Agent(CreditorAgent)\Name.</span><span class="sxs-lookup"><span data-stu-id="da8ea-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="da8ea-203">Puuvaates valige „Excel\PaymLines\Pank”</span><span class="sxs-lookup"><span data-stu-id="da8ea-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="da8ea-204">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="da8ea-204">Click Bind.</span></span>
21. <span data-ttu-id="da8ea-205">Tehke puul valik model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber).</span><span class="sxs-lookup"><span data-stu-id="da8ea-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="da8ea-206">Puuvaates valige „Excel\PaymLines\RoutingNumber”</span><span class="sxs-lookup"><span data-stu-id="da8ea-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="da8ea-207">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="da8ea-207">Click Bind.</span></span>
24. <span data-ttu-id="da8ea-208">Laiendage puus sõlme „model\Payments\Creditor Account(CreditorAccount)”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="da8ea-209">Laiendage puus sõlme „model\Payments\Creditor Account(CreditorAccount)\Identification”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="da8ea-210">Tehke puus valik model\Payments\Creditor Account(CreditorAccount)\Identification\Number.</span><span class="sxs-lookup"><span data-stu-id="da8ea-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="da8ea-211">Puuvaates valige „Excel\PaymLines\AccountNumber”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="da8ea-212">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="da8ea-212">Click Bind.</span></span>
29. <span data-ttu-id="da8ea-213">Valige puul väärtus model\Payments\Instructed Amount(InstructedAmount).</span><span class="sxs-lookup"><span data-stu-id="da8ea-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="da8ea-214">Puuvaates valige „Excel\PaymLines\Deebet”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="da8ea-215">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="da8ea-215">Click Bind.</span></span>
32. <span data-ttu-id="da8ea-216">Laiendage puus sõlme model\Payments\Creditor.</span><span class="sxs-lookup"><span data-stu-id="da8ea-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="da8ea-217">Laiendage puus sõlme „model\Payments\Creditor Account(CreditorAccount)”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="da8ea-218">Laiendage puul valikut model\Payments\Creditor Agent(CreditorAgent).</span><span class="sxs-lookup"><span data-stu-id="da8ea-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="da8ea-219">Valige puul väärtus model\Payments\Currency.</span><span class="sxs-lookup"><span data-stu-id="da8ea-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="da8ea-220">Puuvaates valige „Excel\PaymLines\Valuuta”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="da8ea-221">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="da8ea-221">Click Bind.</span></span>
38. <span data-ttu-id="da8ea-222">Laiendage puul valikut PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="da8ea-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="da8ea-223">Laiendage puul valikut PaymentByCurrency\grouped.</span><span class="sxs-lookup"><span data-stu-id="da8ea-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="da8ea-224">Tehke puul valik PaymentByCurrency\grouped\Currency.</span><span class="sxs-lookup"><span data-stu-id="da8ea-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="da8ea-225">Puuvaates laiendage valikut „Excel\SummaryLines”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="da8ea-226">Puuvaates valige „Excel\SummaryLines\SummaryCurrency”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="da8ea-227">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="da8ea-227">Click Bind.</span></span>
44. <span data-ttu-id="da8ea-228">Laiendage puul valikut PaymentByCurrency\aggregated.</span><span class="sxs-lookup"><span data-stu-id="da8ea-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="da8ea-229">Tehke puul valik PaymentByCurrency\aggregated\TotalInstructuredAmount.</span><span class="sxs-lookup"><span data-stu-id="da8ea-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="da8ea-230">Puuvaates valige „Excel\SummaryLines\SummaryAmount”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="da8ea-231">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="da8ea-231">Click Bind.</span></span>
48. <span data-ttu-id="da8ea-232">Tehke puul valik PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="da8ea-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="da8ea-233">Puuvaates valige „Excel\SummaryLines”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="da8ea-234">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="da8ea-234">Click Bind.</span></span>
51. <span data-ttu-id="da8ea-235">Valige puul suvand model\Payments.</span><span class="sxs-lookup"><span data-stu-id="da8ea-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="da8ea-236">Puuvaates valige „Excel\PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="da8ea-237">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="da8ea-237">Click Bind.</span></span>
54. <span data-ttu-id="da8ea-238">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="da8ea-238">Click Save.</span></span>
55. <span data-ttu-id="da8ea-239">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da8ea-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="da8ea-240">Loodud konfiguratsiooni kasutamine maksete töötlemiseks</span><span class="sxs-lookup"><span data-stu-id="da8ea-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="da8ea-241">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="da8ea-241">Click Change status.</span></span>
2. <span data-ttu-id="da8ea-242">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="da8ea-242">Click Complete.</span></span>
3. <span data-ttu-id="da8ea-243">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="da8ea-243">Click OK.</span></span>
4. <span data-ttu-id="da8ea-244">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da8ea-244">Close the page.</span></span>
5. <span data-ttu-id="da8ea-245">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da8ea-245">Close the page.</span></span>
6. <span data-ttu-id="da8ea-246">Avage Ostureskontro > Makse seadistus > Makseviisid.</span><span class="sxs-lookup"><span data-stu-id="da8ea-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="da8ea-247">Kasutage kiirfiltrit, et filtreerida välja Makseviis väärtusega „Elektrooniline”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="da8ea-248">Elektrooniline</span><span class="sxs-lookup"><span data-stu-id="da8ea-248">Electronic</span></span>  
8. <span data-ttu-id="da8ea-249">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="da8ea-249">Click Edit.</span></span>
9. <span data-ttu-id="da8ea-250">Laiendage jaotist Failivormingud.</span><span class="sxs-lookup"><span data-stu-id="da8ea-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="da8ea-251">Valige väljal Üldine elektrooniline aruandlus suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="da8ea-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="da8ea-252">Sisestage väärtus väljale Ekspordivormingu konfiguratsioon või valige see.</span><span class="sxs-lookup"><span data-stu-id="da8ea-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="da8ea-253">Valige konfiguratsioon Töölehe aruande näide.</span><span class="sxs-lookup"><span data-stu-id="da8ea-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="da8ea-254">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="da8ea-254">Click Save.</span></span>
13. <span data-ttu-id="da8ea-255">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da8ea-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="da8ea-256">Loodud konfiguratsiooni kasutamine makse töölehtede töötlemise testimiseks</span><span class="sxs-lookup"><span data-stu-id="da8ea-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="da8ea-257">Avage Ostureskontro > Maksed > Makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="da8ea-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="da8ea-258">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="da8ea-258">Click New.</span></span>
    * <span data-ttu-id="da8ea-259">Looge uus maksetööleht.</span><span class="sxs-lookup"><span data-stu-id="da8ea-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="da8ea-260">Sisestage väljale Nimi tekst „VendPay”.</span><span class="sxs-lookup"><span data-stu-id="da8ea-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="da8ea-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="da8ea-261">VendPay</span></span>  
4. <span data-ttu-id="da8ea-262">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="da8ea-262">Click Lines.</span></span>
5. <span data-ttu-id="da8ea-263">Määrake väljal Konto väärtused GB_SI_000001.</span><span class="sxs-lookup"><span data-stu-id="da8ea-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="da8ea-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="da8ea-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="da8ea-265">Määrake suvandi Deebet väärtuseks 1000.</span><span class="sxs-lookup"><span data-stu-id="da8ea-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="da8ea-266">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="da8ea-266">Click New.</span></span>
8. <span data-ttu-id="da8ea-267">Määrake väljal Konto väärtused GB_SI_000005.</span><span class="sxs-lookup"><span data-stu-id="da8ea-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="da8ea-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="da8ea-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="da8ea-269">Määrake suvandi Deebet väärtuseks 2000.</span><span class="sxs-lookup"><span data-stu-id="da8ea-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="da8ea-270">Tippige väljale Valuuta väärtus EUR.</span><span class="sxs-lookup"><span data-stu-id="da8ea-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="da8ea-271"> eurot</span><span class="sxs-lookup"><span data-stu-id="da8ea-271">EUR</span></span>  
11. <span data-ttu-id="da8ea-272">Määrake väljal Vastaskonto väärtused GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="da8ea-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="da8ea-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="da8ea-273">GBSI OPER</span></span>  
12. <span data-ttu-id="da8ea-274">Tippige väljale Makseviis tekst Elektrooniline.</span><span class="sxs-lookup"><span data-stu-id="da8ea-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="da8ea-275">Elektrooniline</span><span class="sxs-lookup"><span data-stu-id="da8ea-275">Electronic</span></span>  
13. <span data-ttu-id="da8ea-276">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="da8ea-276">Click Save.</span></span>
14. <span data-ttu-id="da8ea-277">Klõpsake valikut Loo maksed.</span><span class="sxs-lookup"><span data-stu-id="da8ea-277">Click Generate payments.</span></span>
15. <span data-ttu-id="da8ea-278">Tippige väljale Makseviis tekst Elektrooniline.</span><span class="sxs-lookup"><span data-stu-id="da8ea-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="da8ea-279">Elektrooniline</span><span class="sxs-lookup"><span data-stu-id="da8ea-279">Electronic</span></span>  
16. <span data-ttu-id="da8ea-280">Väljale Failinimi tippige Maksed.</span><span class="sxs-lookup"><span data-stu-id="da8ea-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="da8ea-281">Tippige näiteks tekst Maksed.</span><span class="sxs-lookup"><span data-stu-id="da8ea-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="da8ea-282">Tippige väljale Pangakonto tekst GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="da8ea-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="da8ea-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="da8ea-283">GBSI OPER</span></span>  
18. <span data-ttu-id="da8ea-284">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="da8ea-284">Click OK.</span></span>
19. <span data-ttu-id="da8ea-285">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="da8ea-285">Click OK.</span></span>
    * <span data-ttu-id="da8ea-286">Vaadake loodud tööleht üle, sh makseridade üksikasjad kui ka selles makseteates kasutatud iga valuutakoodi summad.</span><span class="sxs-lookup"><span data-stu-id="da8ea-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


