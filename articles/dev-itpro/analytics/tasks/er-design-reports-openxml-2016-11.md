--- 
title: Elektroonilise aruandluse konfiguratsioonide kujundamine OpenXML-vormingus aruannete loomiseks
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b42cfe36c57a9526e585bbad0fcd31ff60b90397
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---
# <a name="design-er-configurations-to-generate-reports-in-openxml-format"></a><span data-ttu-id="41e07-103">Elektroonilise aruandluse konfiguratsioonide kujundamine OpenXML-vormingus aruannete loomiseks</span><span class="sxs-lookup"><span data-stu-id="41e07-103">Design ER configurations to generate reports in OpenXML format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41e07-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab malli elektrooniliste dokumentide loomiseks vormingus OPENXML.</span><span class="sxs-lookup"><span data-stu-id="41e07-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="41e07-105">Seda konfiguratsiooni kasutatakse hankija maksete töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="41e07-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="41e07-106">Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. Neid etappe saab teha ka GBSI ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="41e07-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="41e07-107">Etappide lõpuleviimiseks, peate esmalt läbima protseduuri Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine etapid.</span><span class="sxs-lookup"><span data-stu-id="41e07-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="41e07-108">Peate alla laadima ja salvestama Microsoft Exceli faili [Maksearuande mall](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="41e07-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="41e07-109">Makse andmemudeli konfiguratsiooni üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="41e07-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="41e07-110">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="41e07-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="41e07-111">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="41e07-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="41e07-112">Valige konfiguratsiooni pakkuja näidisettevõtte Litware, Inc. jaoks. Kui seda konfiguratsiooni pakkujat ei kuvata, peate esmalt läbima etapid protseduuris Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="41e07-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="41e07-113">Klõpsake valikut Määra aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="41e07-113">Click Set active.</span></span>
4. <span data-ttu-id="41e07-114">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="41e07-114">Click Repositories.</span></span>
    * <span data-ttu-id="41e07-115">Valige võimaluse korral tüübi Operationsi ressursid jaoks hoidla.</span><span class="sxs-lookup"><span data-stu-id="41e07-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="41e07-116">Kui see on saadaval, jätke uue hoidla loomise järgmised etapid vahele.</span><span class="sxs-lookup"><span data-stu-id="41e07-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="41e07-117">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="41e07-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="41e07-118">Sisestage väljale Konfiguratsiooni hoidla tüüp tekst Operatsiooniressursid.</span><span class="sxs-lookup"><span data-stu-id="41e07-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="41e07-119">Klõpsake käsku Loo hoidla.</span><span class="sxs-lookup"><span data-stu-id="41e07-119">Click Create repository.</span></span>
8. <span data-ttu-id="41e07-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="41e07-120">Click OK.</span></span>
9. <span data-ttu-id="41e07-121">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="41e07-121">Click Open.</span></span>
10. <span data-ttu-id="41e07-122">Valige puul väärtus Maksemudel.</span><span class="sxs-lookup"><span data-stu-id="41e07-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="41e07-123">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="41e07-123">Click Import.</span></span>
    * <span data-ttu-id="41e07-124">Importige see andmemudel.</span><span class="sxs-lookup"><span data-stu-id="41e07-124">Import this data model.</span></span> <span data-ttu-id="41e07-125">Seda kasutatakse andmeallikana uues vormingu konfiguratsioonis.</span><span class="sxs-lookup"><span data-stu-id="41e07-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="41e07-126">Jätke see etapp vahele, kui see konfiguratsioon on juba imporditud.</span><span class="sxs-lookup"><span data-stu-id="41e07-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="41e07-127">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="41e07-127">Click Yes.</span></span>
13. <span data-ttu-id="41e07-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="41e07-128">Close the page.</span></span>
14. <span data-ttu-id="41e07-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="41e07-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="41e07-130">Uue vormingu konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="41e07-130">Create a new format configuration</span></span>
1. <span data-ttu-id="41e07-131">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="41e07-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="41e07-132">Valige puul väärtus Maksemudel.</span><span class="sxs-lookup"><span data-stu-id="41e07-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="41e07-133">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="41e07-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="41e07-134">Sisestage väljale Uus suvand Andmemudelil PaymentModel põhinev vorming.</span><span class="sxs-lookup"><span data-stu-id="41e07-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="41e07-135">Looge vorming, mis põhineb andmemudelil PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="41e07-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="41e07-136">Tippige väljale Nimi tekst Töölehe aruande näide.</span><span class="sxs-lookup"><span data-stu-id="41e07-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="41e07-137">Töölehe aruande näide</span><span class="sxs-lookup"><span data-stu-id="41e07-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="41e07-138">Tippige väljale Kirjeldus tekst Töölehe aruande näide hankijate maksete jaoks.</span><span class="sxs-lookup"><span data-stu-id="41e07-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="41e07-139">Töölehe aruande näide hankijate maksete jaoks.</span><span class="sxs-lookup"><span data-stu-id="41e07-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="41e07-140">Sisestage või valige väärtus väljal Andmemudeli definitsioon.</span><span class="sxs-lookup"><span data-stu-id="41e07-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="41e07-141">Valige määratlus CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="41e07-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="41e07-142">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="41e07-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="41e07-143">Uue dokumendi koostamine töölehe vormingus OPENXML</span><span class="sxs-lookup"><span data-stu-id="41e07-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="41e07-144">Tehke puul valik Maksemudel \ töölehe aruande näide.</span><span class="sxs-lookup"><span data-stu-id="41e07-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="41e07-145">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="41e07-145">Click Designer.</span></span>
3. <span data-ttu-id="41e07-146">Klõpsake toimingupaanil nuppu Impordi.</span><span class="sxs-lookup"><span data-stu-id="41e07-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="41e07-147">Klõpsake käsku Impordi Excelist.</span><span class="sxs-lookup"><span data-stu-id="41e07-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="41e07-148">Klõpsake suvandit Manused.</span><span class="sxs-lookup"><span data-stu-id="41e07-148">Click Attachments.</span></span>
    * <span data-ttu-id="41e07-149">Manustage olemasolev Exceli dokument mallina.</span><span class="sxs-lookup"><span data-stu-id="41e07-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="41e07-150">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="41e07-150">Click New.</span></span>
7. <span data-ttu-id="41e07-151">Klõpsake suvandit Fail.</span><span class="sxs-lookup"><span data-stu-id="41e07-151">Click File.</span></span>
    * <span data-ttu-id="41e07-152">Osutage olemasolevale Exceli failile.</span><span class="sxs-lookup"><span data-stu-id="41e07-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="41e07-153">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="41e07-153">Close the page.</span></span>
9. <span data-ttu-id="41e07-154">Sisestage või valige väärtus väljal Mall.</span><span class="sxs-lookup"><span data-stu-id="41e07-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="41e07-155">Valige manustatud Exceli fail, mida kasutada mallina.</span><span class="sxs-lookup"><span data-stu-id="41e07-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="41e07-156">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="41e07-156">Click OK.</span></span>
    * <span data-ttu-id="41e07-157">Pange tähele, et ER-i vormingu komponendid on loodud kujundamisvormingus viitava MS Exceli dokumendi struktuuri alusel (nimega vahemikud).</span><span class="sxs-lookup"><span data-stu-id="41e07-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="41e07-158">Uue andmeallika loomine kogusummade arvutamises valuutakoodide järgi</span><span class="sxs-lookup"><span data-stu-id="41e07-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="41e07-159">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="41e07-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="41e07-160">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="41e07-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="41e07-161">Valige puul väärtus Funktsioonid\grupeerimisalus.</span><span class="sxs-lookup"><span data-stu-id="41e07-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="41e07-162">Tippige väljale Nimi tekst PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="41e07-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="41e07-163">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="41e07-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="41e07-164">Klõpsake suvandit Grupi redigeerimise alus.</span><span class="sxs-lookup"><span data-stu-id="41e07-164">Click Edit group by.</span></span>
6. <span data-ttu-id="41e07-165">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="41e07-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="41e07-166">Valige puul suvand model\Payments.</span><span class="sxs-lookup"><span data-stu-id="41e07-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="41e07-167">Klõpsake suvandit Lisa väli üksusele.</span><span class="sxs-lookup"><span data-stu-id="41e07-167">Click Add field to.</span></span>
9. <span data-ttu-id="41e07-168">Klõpsake suvandit Mida grupeerida.</span><span class="sxs-lookup"><span data-stu-id="41e07-168">Click What to group.</span></span>
10. <span data-ttu-id="41e07-169">Laiendage puus sõlme model\Payments.</span><span class="sxs-lookup"><span data-stu-id="41e07-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="41e07-170">Valige puul väärtus model\Payments\Currency.</span><span class="sxs-lookup"><span data-stu-id="41e07-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="41e07-171">Klõpsake suvandit Lisa väli üksusele.</span><span class="sxs-lookup"><span data-stu-id="41e07-171">Click Add field to.</span></span>
13. <span data-ttu-id="41e07-172">Klõpsake suvandit Grupeeritud väljad.</span><span class="sxs-lookup"><span data-stu-id="41e07-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="41e07-173">Valige puul väärtus model\Payments\Instructed Amount(InstructedAmount).</span><span class="sxs-lookup"><span data-stu-id="41e07-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="41e07-174">Klõpsake suvandit Lisa väli üksusele.</span><span class="sxs-lookup"><span data-stu-id="41e07-174">Click Add field to.</span></span>
16. <span data-ttu-id="41e07-175">Klõpsake suvandit Kogumi väljad.</span><span class="sxs-lookup"><span data-stu-id="41e07-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="41e07-176">Valige suvand väljalt Meetod.</span><span class="sxs-lookup"><span data-stu-id="41e07-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="41e07-177">Valige summa liitmisfunktsioon.</span><span class="sxs-lookup"><span data-stu-id="41e07-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="41e07-178">Tippige väljale Nimi tekst TotalInstructuredAmount.</span><span class="sxs-lookup"><span data-stu-id="41e07-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="41e07-179">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="41e07-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="41e07-180">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="41e07-180">Click Save.</span></span>
20. <span data-ttu-id="41e07-181">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="41e07-181">Close the page.</span></span>
21. <span data-ttu-id="41e07-182">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="41e07-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="41e07-183">Vormingu komponentide vastendamine andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="41e07-183">Map format components to data sources</span></span>
1. <span data-ttu-id="41e07-184">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="41e07-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="41e07-185">Laiendage puus sõlme model\Payments.</span><span class="sxs-lookup"><span data-stu-id="41e07-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="41e07-186">Laiendage puul suvandit model\Payments\Initiating Party(InitiatingParty).</span><span class="sxs-lookup"><span data-stu-id="41e07-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="41e07-187">Valige puul väärtus model\Payments\Initiating Party(InitiatingParty)\Name.</span><span class="sxs-lookup"><span data-stu-id="41e07-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="41e07-188">Puuvaates laiendage valikut „Excel\ReportHeader”.</span><span class="sxs-lookup"><span data-stu-id="41e07-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="41e07-189">Puuvaates valige „Excel\ReportHeader\CompanyName”.</span><span class="sxs-lookup"><span data-stu-id="41e07-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="41e07-190">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="41e07-190">Click Bind.</span></span>
8. <span data-ttu-id="41e07-191">Laiendage puus sõlme model\Payments\Creditor.</span><span class="sxs-lookup"><span data-stu-id="41e07-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="41e07-192">Laiendage puul suvandit model\Payments\Creditor\Identification.</span><span class="sxs-lookup"><span data-stu-id="41e07-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="41e07-193">Tehke puul valik model\Payments\Creditor\Identification\Source ID(SourceID).</span><span class="sxs-lookup"><span data-stu-id="41e07-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="41e07-194">Puuvaates laiendage „Excel\PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="41e07-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="41e07-195">Puuvaates valige „Excel\PaymLines\VendAccountName”.</span><span class="sxs-lookup"><span data-stu-id="41e07-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="41e07-196">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="41e07-196">Click Bind.</span></span>
14. <span data-ttu-id="41e07-197">Valige puul suvand model\Payments\Creditor\Name.</span><span class="sxs-lookup"><span data-stu-id="41e07-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="41e07-198">Puuvaates valige „Excel\PaymLines\VendName”</span><span class="sxs-lookup"><span data-stu-id="41e07-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="41e07-199">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="41e07-199">Click Bind.</span></span>
17. <span data-ttu-id="41e07-200">Laiendage puul valikut model\Payments\Creditor Agent(CreditorAgent).</span><span class="sxs-lookup"><span data-stu-id="41e07-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="41e07-201">Tehke puul valik model\Payments\Creditor Agent(CreditorAgent)\Name.</span><span class="sxs-lookup"><span data-stu-id="41e07-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="41e07-202">Puuvaates valige „Excel\PaymLines\Pank”</span><span class="sxs-lookup"><span data-stu-id="41e07-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="41e07-203">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="41e07-203">Click Bind.</span></span>
21. <span data-ttu-id="41e07-204">Tehke puul valik model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber).</span><span class="sxs-lookup"><span data-stu-id="41e07-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="41e07-205">Puuvaates valige „Excel\PaymLines\RoutingNumber”</span><span class="sxs-lookup"><span data-stu-id="41e07-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="41e07-206">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="41e07-206">Click Bind.</span></span>
24. <span data-ttu-id="41e07-207">Laiendage puus sõlme „model\Payments\Creditor Account(CreditorAccount)”.</span><span class="sxs-lookup"><span data-stu-id="41e07-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="41e07-208">Laiendage puus sõlme „model\Payments\Creditor Account(CreditorAccount)\Identification”.</span><span class="sxs-lookup"><span data-stu-id="41e07-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="41e07-209">Tehke puus valik model\Payments\Creditor Account(CreditorAccount)\Identification\Number.</span><span class="sxs-lookup"><span data-stu-id="41e07-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="41e07-210">Puuvaates valige „Excel\PaymLines\AccountNumber”.</span><span class="sxs-lookup"><span data-stu-id="41e07-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="41e07-211">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="41e07-211">Click Bind.</span></span>
29. <span data-ttu-id="41e07-212">Valige puul väärtus model\Payments\Instructed Amount(InstructedAmount).</span><span class="sxs-lookup"><span data-stu-id="41e07-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="41e07-213">Puuvaates valige „Excel\PaymLines\Deebet”.</span><span class="sxs-lookup"><span data-stu-id="41e07-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="41e07-214">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="41e07-214">Click Bind.</span></span>
32. <span data-ttu-id="41e07-215">Laiendage puus sõlme model\Payments\Creditor.</span><span class="sxs-lookup"><span data-stu-id="41e07-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="41e07-216">Laiendage puus sõlme „model\Payments\Creditor Account(CreditorAccount)”.</span><span class="sxs-lookup"><span data-stu-id="41e07-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="41e07-217">Laiendage puul valikut model\Payments\Creditor Agent(CreditorAgent).</span><span class="sxs-lookup"><span data-stu-id="41e07-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="41e07-218">Valige puul väärtus model\Payments\Currency.</span><span class="sxs-lookup"><span data-stu-id="41e07-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="41e07-219">Puuvaates valige „Excel\PaymLines\Valuuta”.</span><span class="sxs-lookup"><span data-stu-id="41e07-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="41e07-220">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="41e07-220">Click Bind.</span></span>
38. <span data-ttu-id="41e07-221">Laiendage puul valikut PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="41e07-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="41e07-222">Laiendage puul valikut PaymentByCurrency\grouped.</span><span class="sxs-lookup"><span data-stu-id="41e07-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="41e07-223">Tehke puul valik PaymentByCurrency\grouped\Currency.</span><span class="sxs-lookup"><span data-stu-id="41e07-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="41e07-224">Puuvaates laiendage valikut „Excel\SummaryLines”.</span><span class="sxs-lookup"><span data-stu-id="41e07-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="41e07-225">Puuvaates valige „Excel\SummaryLines\SummaryCurrency”.</span><span class="sxs-lookup"><span data-stu-id="41e07-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="41e07-226">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="41e07-226">Click Bind.</span></span>
44. <span data-ttu-id="41e07-227">Laiendage puul valikut PaymentByCurrency\aggregated.</span><span class="sxs-lookup"><span data-stu-id="41e07-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="41e07-228">Tehke puul valik PaymentByCurrency\aggregated\TotalInstructuredAmount.</span><span class="sxs-lookup"><span data-stu-id="41e07-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="41e07-229">Puuvaates valige „Excel\SummaryLines\SummaryAmount”.</span><span class="sxs-lookup"><span data-stu-id="41e07-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="41e07-230">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="41e07-230">Click Bind.</span></span>
48. <span data-ttu-id="41e07-231">Tehke puul valik PaymentByCurrency.</span><span class="sxs-lookup"><span data-stu-id="41e07-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="41e07-232">Puuvaates valige „Excel\SummaryLines”.</span><span class="sxs-lookup"><span data-stu-id="41e07-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="41e07-233">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="41e07-233">Click Bind.</span></span>
51. <span data-ttu-id="41e07-234">Valige puul suvand model\Payments.</span><span class="sxs-lookup"><span data-stu-id="41e07-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="41e07-235">Puuvaates valige „Excel\PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="41e07-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="41e07-236">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="41e07-236">Click Bind.</span></span>
54. <span data-ttu-id="41e07-237">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="41e07-237">Click Save.</span></span>
55. <span data-ttu-id="41e07-238">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="41e07-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="41e07-239">Loodud konfiguratsiooni kasutamine maksete töötlemiseks</span><span class="sxs-lookup"><span data-stu-id="41e07-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="41e07-240">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="41e07-240">Click Change status.</span></span>
2. <span data-ttu-id="41e07-241">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="41e07-241">Click Complete.</span></span>
3. <span data-ttu-id="41e07-242">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="41e07-242">Click OK.</span></span>
4. <span data-ttu-id="41e07-243">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="41e07-243">Close the page.</span></span>
5. <span data-ttu-id="41e07-244">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="41e07-244">Close the page.</span></span>
6. <span data-ttu-id="41e07-245">Avage Ostureskontro > Makse seadistus > Makseviisid.</span><span class="sxs-lookup"><span data-stu-id="41e07-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="41e07-246">Kasutage kiirfiltrit, et filtreerida välja Makseviis väärtusega „Elektrooniline”.</span><span class="sxs-lookup"><span data-stu-id="41e07-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="41e07-247">Elektrooniline</span><span class="sxs-lookup"><span data-stu-id="41e07-247">Electronic</span></span>  
8. <span data-ttu-id="41e07-248">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="41e07-248">Click Edit.</span></span>
9. <span data-ttu-id="41e07-249">Laiendage jaotist Failivormingud.</span><span class="sxs-lookup"><span data-stu-id="41e07-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="41e07-250">Valige väljal Üldine elektrooniline aruandlus suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="41e07-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="41e07-251">Sisestage väärtus väljale Ekspordivormingu konfiguratsioon või valige see.</span><span class="sxs-lookup"><span data-stu-id="41e07-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="41e07-252">Valige konfiguratsioon Töölehe aruande näide.</span><span class="sxs-lookup"><span data-stu-id="41e07-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="41e07-253">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="41e07-253">Click Save.</span></span>
13. <span data-ttu-id="41e07-254">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="41e07-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="41e07-255">Loodud konfiguratsiooni kasutamine makse töölehtede töötlemise testimiseks</span><span class="sxs-lookup"><span data-stu-id="41e07-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="41e07-256">Avage Ostureskontro > Maksed > Makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="41e07-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="41e07-257">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="41e07-257">Click New.</span></span>
    * <span data-ttu-id="41e07-258">Looge uus maksetööleht.</span><span class="sxs-lookup"><span data-stu-id="41e07-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="41e07-259">Sisestage väljale Nimi tekst „VendPay”.</span><span class="sxs-lookup"><span data-stu-id="41e07-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="41e07-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="41e07-260">VendPay</span></span>  
4. <span data-ttu-id="41e07-261">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="41e07-261">Click Lines.</span></span>
5. <span data-ttu-id="41e07-262">Määrake väljal Konto väärtused GB_SI_000001.</span><span class="sxs-lookup"><span data-stu-id="41e07-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="41e07-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="41e07-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="41e07-264">Määrake suvandi Deebet väärtuseks 1000.</span><span class="sxs-lookup"><span data-stu-id="41e07-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="41e07-265">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="41e07-265">Click New.</span></span>
8. <span data-ttu-id="41e07-266">Määrake väljal Konto väärtused GB_SI_000005.</span><span class="sxs-lookup"><span data-stu-id="41e07-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="41e07-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="41e07-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="41e07-268">Määrake suvandi Deebet väärtuseks 2000.</span><span class="sxs-lookup"><span data-stu-id="41e07-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="41e07-269">Tippige väljale Valuuta väärtus EUR.</span><span class="sxs-lookup"><span data-stu-id="41e07-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="41e07-270"> eurot</span><span class="sxs-lookup"><span data-stu-id="41e07-270">EUR</span></span>  
11. <span data-ttu-id="41e07-271">Määrake väljal Vastaskonto väärtused GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="41e07-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="41e07-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="41e07-272">GBSI OPER</span></span>  
12. <span data-ttu-id="41e07-273">Tippige väljale Makseviis tekst Elektrooniline.</span><span class="sxs-lookup"><span data-stu-id="41e07-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="41e07-274">Elektrooniline</span><span class="sxs-lookup"><span data-stu-id="41e07-274">Electronic</span></span>  
13. <span data-ttu-id="41e07-275">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="41e07-275">Click Save.</span></span>
14. <span data-ttu-id="41e07-276">Klõpsake valikut Loo maksed.</span><span class="sxs-lookup"><span data-stu-id="41e07-276">Click Generate payments.</span></span>
15. <span data-ttu-id="41e07-277">Tippige väljale Makseviis tekst Elektrooniline.</span><span class="sxs-lookup"><span data-stu-id="41e07-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="41e07-278">Elektrooniline</span><span class="sxs-lookup"><span data-stu-id="41e07-278">Electronic</span></span>  
16. <span data-ttu-id="41e07-279">Väljale Failinimi tippige Maksed.</span><span class="sxs-lookup"><span data-stu-id="41e07-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="41e07-280">Tippige näiteks tekst Maksed.</span><span class="sxs-lookup"><span data-stu-id="41e07-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="41e07-281">Tippige väljale Pangakonto tekst GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="41e07-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="41e07-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="41e07-282">GBSI OPER</span></span>  
18. <span data-ttu-id="41e07-283">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="41e07-283">Click OK.</span></span>
19. <span data-ttu-id="41e07-284">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="41e07-284">Click OK.</span></span>
    * <span data-ttu-id="41e07-285">Vaadake loodud tööleht üle, sh makseridade üksikasjad kui ka selles makseteates kasutatud iga valuutakoodi summad.</span><span class="sxs-lookup"><span data-stu-id="41e07-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


