--- 
title: Avaldiste kujundamine, millega kutsuda rakendusklasside meetodeid (elektrooniline aruandlus)
description: Juhendis kirjeldatakse, kuidas taaskasutada olemasolevat rakendusloogikat elektroonilise aruandluse (ER) konfiguratsioonides, kutsudes ER-i rakendusklasside vajalikke meetodeid.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: b0a1dba5afbd7beba45149340f637223f6ecedcf
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---
# <a name="design-expressions-to-call-application-class-methods-er"></a><span data-ttu-id="66e9d-103">Avaldiste kujundamine, millega kutsuda rakendusklasside meetodeid (elektrooniline aruandlus)</span><span class="sxs-lookup"><span data-stu-id="66e9d-103">Design expressions to call application class methods (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="66e9d-104">Juhendis kirjeldatakse, kuidas taaskasutada olemasolevat rakendusloogikat elektroonilise aruandluse (ER) konfiguratsioonides, kutsudes ER-i rakendusklasside vajalikke meetodeid.</span><span class="sxs-lookup"><span data-stu-id="66e9d-104">This guide provides information about how to reuse the existing application logic in Electronic reporting (ER) configurations by calling required methods of application classes in ER expressions.</span></span> <span data-ttu-id="66e9d-105">Kutsumisklasside argumentide väärtusi saab käitusajal dünaamiliselt määratleda: näiteks sõelumisdokumendis oleva teabe alusel, et tagada selle õigsus.</span><span class="sxs-lookup"><span data-stu-id="66e9d-105">Values of arguments for calling classes can be defined dynamically at run-time: for example, based on information in the parsing document to ensure its correctness.</span></span> <span data-ttu-id="66e9d-106">Selle juhise järgi koostate näidisettevõtte Litware, Inc jaoks vajalikud elektroonilise aruandluse konfiguratsioonid. Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll.</span><span class="sxs-lookup"><span data-stu-id="66e9d-106">In this guide, you will create the required ER configurations for the sample company, Litware, Inc. This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> 

<span data-ttu-id="66e9d-107">Need etapid saab lõpule viia ükskõik millise andmekomplekti abil.</span><span class="sxs-lookup"><span data-stu-id="66e9d-107">These steps can be completed using any data set.</span></span> <span data-ttu-id="66e9d-108">Peate ka järgmise faili alla laadima ja kohalikult salvestama: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span><span class="sxs-lookup"><span data-stu-id="66e9d-108">You must also download and save the following file locally: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span></span>

<span data-ttu-id="66e9d-109">Etappide lõpuleviimiseks peate esmalt läbima protseduuri „Pakkuja elektroonilise aruandluse konfiguratsiooni loomine ning aktiivseks märkimine” etapid.</span><span class="sxs-lookup"><span data-stu-id="66e9d-109">To complete these steps, you must first complete the steps in the procedure, “ER Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="66e9d-110">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="66e9d-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="66e9d-111">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena.</span><span class="sxs-lookup"><span data-stu-id="66e9d-111">Verify that the configuration provider for sample company, Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="66e9d-112">Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” esitatud juhised.</span><span class="sxs-lookup"><span data-stu-id="66e9d-112">If you don’t see this configuration provider, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>   
    * <span data-ttu-id="66e9d-113">Oletame, et koostate sissetulevate pangaväljavõtete sõelumise protsessi avalduse andmete värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="66e9d-113">Let’s assume that you are designing a process for parsing incoming bank statements for an application data update.</span></span> <span data-ttu-id="66e9d-114">Sissetulevad pangaväljavõtted saadetakse teile TXT-failidena, mis sisaldavad IBAN-koode.</span><span class="sxs-lookup"><span data-stu-id="66e9d-114">You will receive the incoming bank statements as TXT files that contain IBAN codes.</span></span> <span data-ttu-id="66e9d-115">Pangaväljavõtte importimise osana peate selle IBAN-koodide õigsust kontrollima loogikaga, mis on juba saadaval rakenduses Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="66e9d-115">As part of the bank statement import process, you need to validate the correctness of this IBAN codes using the logic that is already available in Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>   

## <a name="import-a-new-er-model-configuration"></a><span data-ttu-id="66e9d-116">Uue elektroonilise aruandluse mudeli konfiguratsiooni importimine</span><span class="sxs-lookup"><span data-stu-id="66e9d-116">Import a new ER model configuration</span></span>
1. <span data-ttu-id="66e9d-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="66e9d-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="66e9d-118">Valige Microsofti pakkuja paan.</span><span class="sxs-lookup"><span data-stu-id="66e9d-118">Select the Microsoft provider tile.</span></span>  
2. <span data-ttu-id="66e9d-119">Klõpsake valikut Hoidlad.</span><span class="sxs-lookup"><span data-stu-id="66e9d-119">Click Repositories.</span></span>
3. <span data-ttu-id="66e9d-120">Klõpsake suvandit Näita filtreid.</span><span class="sxs-lookup"><span data-stu-id="66e9d-120">Click Show filters.</span></span>
4. <span data-ttu-id="66e9d-121">Lisage filtriväli „Tüübi nimi”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-121">Add a filter field ‘Type name’.</span></span> <span data-ttu-id="66e9d-122">Väljale Nimi sisestage väärtus „ressursid”, valige filtri tehtemärk „sisaldab” ja klõpsake käsku Rakenda.</span><span class="sxs-lookup"><span data-stu-id="66e9d-122">In the Name field, enter the value “resources”, select the “contains” filter operator, and then click Apply.</span></span>
5. <span data-ttu-id="66e9d-123">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="66e9d-123">Click Open.</span></span>
6. <span data-ttu-id="66e9d-124">Valige puul väärtus Maksemudel.</span><span class="sxs-lookup"><span data-stu-id="66e9d-124">In the tree, select 'Payment model'.</span></span>
    * <span data-ttu-id="66e9d-125">Kui nupp Impordi kiirkaardil Versioonid ei ole lubatud, olete ER-i konfiguratsiooni „Maksemudel” 1. versiooni juba importinud.</span><span class="sxs-lookup"><span data-stu-id="66e9d-125">If the Import button on the Versions FastTab is not enabled, you have already imported the version 1 one of the ER configuration ‘Payment model’.</span></span> <span data-ttu-id="66e9d-126">Võite alamülesande ülejäänud etapid vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="66e9d-126">You can skip the rest steps in this sub-task.</span></span>   
7. <span data-ttu-id="66e9d-127">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="66e9d-127">Click Import.</span></span>
8. <span data-ttu-id="66e9d-128">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="66e9d-128">Click Yes.</span></span>
9. <span data-ttu-id="66e9d-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="66e9d-129">Close the page.</span></span>
10. <span data-ttu-id="66e9d-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="66e9d-130">Close the page.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="66e9d-131">Uue elektroonilise aruandluse vormingu konfiguratsiooni lisamine</span><span class="sxs-lookup"><span data-stu-id="66e9d-131">Add a new ER format configuration</span></span>
1. <span data-ttu-id="66e9d-132">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="66e9d-132">Click Reporting configurations.</span></span>
    * <span data-ttu-id="66e9d-133">Lisage uus ER-i vorming, et sõeluda TXT-vormingus sissetulevaid pangaväljavõtteid.</span><span class="sxs-lookup"><span data-stu-id="66e9d-133">Add a new ER format to parse incoming bank statements in TXT format.</span></span>  
2. <span data-ttu-id="66e9d-134">Valige puul väärtus Maksemudel.</span><span class="sxs-lookup"><span data-stu-id="66e9d-134">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="66e9d-135">Klõpsake valikut Loo konfiguratsioon, et avada dialoogimenüü.</span><span class="sxs-lookup"><span data-stu-id="66e9d-135">Click Create configuration to open the dialog menu.</span></span>
4. <span data-ttu-id="66e9d-136">Sisestage väljale Uus suvand Andmemudelil PaymentModel põhinev vorming.</span><span class="sxs-lookup"><span data-stu-id="66e9d-136">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
5. <span data-ttu-id="66e9d-137">Väljale Nimi tippige „Panga väljavõtte impordivorming (näidis)”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-137">In the Name field, type 'Bank statement import format (sample)'.</span></span>
    * <span data-ttu-id="66e9d-138">Pangaväljavõtte impordivorming (näide)</span><span class="sxs-lookup"><span data-stu-id="66e9d-138">Bank statement import format (sample)</span></span>  
6. <span data-ttu-id="66e9d-139">Väljal Toetab andmeimporti valige Jah.</span><span class="sxs-lookup"><span data-stu-id="66e9d-139">Select Yes in the Supports data import field.</span></span>
7. <span data-ttu-id="66e9d-140">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="66e9d-140">Click Create configuration.</span></span>

## <a name="design-the-er-format-configuration---format"></a><span data-ttu-id="66e9d-141">Elektroonilise aruandluse vormingu konfiguratsiooni kujundamine – vorming</span><span class="sxs-lookup"><span data-stu-id="66e9d-141">Design the ER format configuration - format</span></span>
1. <span data-ttu-id="66e9d-142">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="66e9d-142">Click Designer.</span></span>
    * <span data-ttu-id="66e9d-143">Kujundatud vorming tähistab TXT-vormingus välise faili eeldatavat struktuuri.</span><span class="sxs-lookup"><span data-stu-id="66e9d-143">The designed format represents the expected structure of the external file in TXT format.</span></span>  
2. <span data-ttu-id="66e9d-144">Klõpsake dialoogimenüü avamiseks suvandit Lisa juur.</span><span class="sxs-lookup"><span data-stu-id="66e9d-144">Click Add root to open the dialog menu.</span></span>
3. <span data-ttu-id="66e9d-145">Valige puult Tekst \ Seeria.</span><span class="sxs-lookup"><span data-stu-id="66e9d-145">In the tree, select 'Text\Sequence'.</span></span>
4. <span data-ttu-id="66e9d-146">Tippige Juur väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="66e9d-146">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="66e9d-147">Juur</span><span class="sxs-lookup"><span data-stu-id="66e9d-147">Root</span></span>  
5. <span data-ttu-id="66e9d-148">Valige väljal Erimärgid Uus rida – Windows (CR LF).</span><span class="sxs-lookup"><span data-stu-id="66e9d-148">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
    * <span data-ttu-id="66e9d-149">Suvand „Uus rida – Windows (CR LF)” on väljal „Erimärgid” valitud.</span><span class="sxs-lookup"><span data-stu-id="66e9d-149">The option ‘New line - Windows (CR LF)’ has been selected in the ‘Special characters’ field.</span></span> <span data-ttu-id="66e9d-150">Selle sätte alusel arvestatakse sõelumisfaili iga rida eraldi kirjena.</span><span class="sxs-lookup"><span data-stu-id="66e9d-150">Based on this setting, each line in the parsing file is considered a separate record.</span></span>  
6. <span data-ttu-id="66e9d-151">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="66e9d-151">Click OK.</span></span>
7. <span data-ttu-id="66e9d-152">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="66e9d-152">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="66e9d-153">Valige puult Tekst \ Seeria.</span><span class="sxs-lookup"><span data-stu-id="66e9d-153">In the tree, select 'Text\Sequence'.</span></span>
9. <span data-ttu-id="66e9d-154">Väljale Nimi tippige „Read”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-154">In the Name field, type 'Rows'.</span></span>
    * <span data-ttu-id="66e9d-155">Read</span><span class="sxs-lookup"><span data-stu-id="66e9d-155">Rows</span></span>  
10. <span data-ttu-id="66e9d-156">Valige kordsuse väljal „One many”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-156">In the Multiplicity field, select 'One many'.</span></span>
    * <span data-ttu-id="66e9d-157">Väljal „Mitmekordsus” on valitud suvand „Üks, mitu”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-157">The option ‘One many’ has been selected in the ‘Multiplicity’ field.</span></span> <span data-ttu-id="66e9d-158">Selle sätte alusel eeldatakse, et sõelumisfailis esitatakse vähemalt üks rida.</span><span class="sxs-lookup"><span data-stu-id="66e9d-158">Based on this setting, it is expected that at least one line will be presented in the parsing file.</span></span>  
11. <span data-ttu-id="66e9d-159">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="66e9d-159">Click OK.</span></span>
12. <span data-ttu-id="66e9d-160">Valige puul väärtus „Juur\Read”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-160">In the tree, select 'Root\Rows'.</span></span>
13. <span data-ttu-id="66e9d-161">Klõpsake käsku Lisa seeria.</span><span class="sxs-lookup"><span data-stu-id="66e9d-161">Click Add Sequence.</span></span>
14. <span data-ttu-id="66e9d-162">Väljale Nimi tippige „Väljad”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-162">In the Name field, type 'Fields'.</span></span>
    * <span data-ttu-id="66e9d-163">Väljad</span><span class="sxs-lookup"><span data-stu-id="66e9d-163">Fields</span></span>  
15. <span data-ttu-id="66e9d-164">Valige kordsuse väljal „Exactly one”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-164">In the Multiplicity field, select 'Exactly one'.</span></span>
16. <span data-ttu-id="66e9d-165">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="66e9d-165">Click OK.</span></span>
17. <span data-ttu-id="66e9d-166">Puul valige „Juur\Read\Väljad”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-166">In the tree, select 'Root\Rows\Fields'.</span></span>
18. <span data-ttu-id="66e9d-167">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="66e9d-167">Click Add to open the drop dialog.</span></span>
19. <span data-ttu-id="66e9d-168">Valige puul suvand Tekst\String.</span><span class="sxs-lookup"><span data-stu-id="66e9d-168">In the tree, select 'Text\String'.</span></span>
20. <span data-ttu-id="66e9d-169">Sisestage väljale Nimi suvand IBAN.</span><span class="sxs-lookup"><span data-stu-id="66e9d-169">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="66e9d-170">IBAN</span><span class="sxs-lookup"><span data-stu-id="66e9d-170">IBAN</span></span>  
21. <span data-ttu-id="66e9d-171">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="66e9d-171">Click OK.</span></span>
    * <span data-ttu-id="66e9d-172">See on konfigureeritud nii, et sõelumisfaili iga rida sisaldab ainult IBAN-koodi.</span><span class="sxs-lookup"><span data-stu-id="66e9d-172">It has been configured that each line in the parsing file contains the only IBAN code.</span></span>  
22. <span data-ttu-id="66e9d-173">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="66e9d-173">Click Save.</span></span>

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a><span data-ttu-id="66e9d-174">ER-i vormingu konfiguratsiooni loomine – andmemudeliga vastendamine</span><span class="sxs-lookup"><span data-stu-id="66e9d-174">Design the ER format configuration – mapping to data model</span></span>
1. <span data-ttu-id="66e9d-175">Klõpsake nuppu Vormingu vastendamine mudeliga.</span><span class="sxs-lookup"><span data-stu-id="66e9d-175">Click Map format to model.</span></span>
2. <span data-ttu-id="66e9d-176">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="66e9d-176">Click New.</span></span>
3. <span data-ttu-id="66e9d-177">Väljale Definitsioon tippige „BankToCustomerDebitCreditNotificationInitiation”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-177">In the Definition field, type 'BankToCustomerDebitCreditNotificationInitiation'.</span></span>
    * <span data-ttu-id="66e9d-178">BankToCustomerDebitCreditNotificationInitiation</span><span class="sxs-lookup"><span data-stu-id="66e9d-178">BankToCustomerDebitCreditNotificationInitiation</span></span>  
4. <span data-ttu-id="66e9d-179">ResolveChanges definitsiooni.</span><span class="sxs-lookup"><span data-stu-id="66e9d-179">ResolveChanges the Definition.</span></span>
5. <span data-ttu-id="66e9d-180">Sisestage nimeväljale valik „Vastendamine andmemudeliga”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-180">In the Name field, type 'Mapping to data model'.</span></span>
    * <span data-ttu-id="66e9d-181">Andmemudeliga vastendamine</span><span class="sxs-lookup"><span data-stu-id="66e9d-181">Mapping to data model</span></span>  
6. <span data-ttu-id="66e9d-182">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="66e9d-182">Click Save.</span></span>
7. <span data-ttu-id="66e9d-183">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="66e9d-183">Click Designer.</span></span>
8. <span data-ttu-id="66e9d-184">Valige puul suvand „Dynamics 365 for Operations\Klass“.</span><span class="sxs-lookup"><span data-stu-id="66e9d-184">In the tree, select 'Dynamics 365 for Operations\Class'.</span></span>
9. <span data-ttu-id="66e9d-185">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="66e9d-185">Click Add root.</span></span>
    * <span data-ttu-id="66e9d-186">Lisage uus andmeallikas, et kutsuda olemasolev rakendusloogika IBAN-koodide kontrollimiseks.</span><span class="sxs-lookup"><span data-stu-id="66e9d-186">Add a new data source to call the existing application logic for IBAN codes validation.</span></span>  
10. <span data-ttu-id="66e9d-187">Väljale Nimi tippige „check_codes”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-187">In the Name field, type 'check_codes'.</span></span>
    * <span data-ttu-id="66e9d-188">check_codes</span><span class="sxs-lookup"><span data-stu-id="66e9d-188">check_codes</span></span>  
11. <span data-ttu-id="66e9d-189">Väljale Klass tippige „ISO7064”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-189">In the Class field, type 'ISO7064'.</span></span>
    * <span data-ttu-id="66e9d-190">ISO7064</span><span class="sxs-lookup"><span data-stu-id="66e9d-190">ISO7064</span></span>  
12. <span data-ttu-id="66e9d-191">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="66e9d-191">Click OK.</span></span>
13. <span data-ttu-id="66e9d-192">Laiendage puul valikut „format”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-192">In the tree, expand 'format'.</span></span>
14. <span data-ttu-id="66e9d-193">Laiendage puul valikut „format\Root: Sequence(Root)”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-193">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
15. <span data-ttu-id="66e9d-194">Valige puul „format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-194">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
16. <span data-ttu-id="66e9d-195">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="66e9d-195">Click Bind.</span></span>
17. <span data-ttu-id="66e9d-196">Laiendage puul jaotist „format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-196">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
18. <span data-ttu-id="66e9d-197">Laiendage puu jaotist „format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-197">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
19. <span data-ttu-id="66e9d-198">Valige puul „format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-198">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
20. <span data-ttu-id="66e9d-199">Laiendage puul valikut „Payments = format.Root.Rows”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-199">In the tree, expand 'Payments = format.Root.Rows'.</span></span>
21. <span data-ttu-id="66e9d-200">Laiendage puus sõlme „Payments = format.Root.Rows\Creditor Account(CreditorAccount)”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-200">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)'.</span></span>
22. <span data-ttu-id="66e9d-201">Laiendage puus sõlme „Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-201">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification'.</span></span>
23. <span data-ttu-id="66e9d-202">Valige puus „Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-202">In the tree, select 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN'.</span></span>
24. <span data-ttu-id="66e9d-203">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="66e9d-203">Click Bind.</span></span>
25. <span data-ttu-id="66e9d-204">Klõpsake vahekaarti Kinnitused.</span><span class="sxs-lookup"><span data-stu-id="66e9d-204">Click the Validations tab.</span></span>
26. <span data-ttu-id="66e9d-205">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="66e9d-205">Click New.</span></span>
    * <span data-ttu-id="66e9d-206">Lisage uus kinnitamisreegel, mis kuvab sõelumisfailis kehtetut IBAN-koodi sisaldava rea puhul tõrke.</span><span class="sxs-lookup"><span data-stu-id="66e9d-206">Add a new validation rule that displays an error for any line in the parsing file that contains invalid IBAN code.</span></span>  
27. <span data-ttu-id="66e9d-207">Klõpsake nuppu Muuda tingimust.</span><span class="sxs-lookup"><span data-stu-id="66e9d-207">Click Edit condition.</span></span>
28. <span data-ttu-id="66e9d-208">Laiendage puul suvandit „check_codes”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-208">In the tree, expand 'check_codes'.</span></span>
29. <span data-ttu-id="66e9d-209">Valige puul „check_codes\verifyMOD1271_36”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-209">In the tree, select 'check_codes\verifyMOD1271_36'.</span></span>
30. <span data-ttu-id="66e9d-210">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="66e9d-210">Click Add data source.</span></span>
31. <span data-ttu-id="66e9d-211">Väljale Valem sisestage „check_codes.verifyMOD1271_36(”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-211">In the Formula field, enter 'check_codes.verifyMOD1271_36('.</span></span>
    * <span data-ttu-id="66e9d-212">check_codes.verifyMOD1271_36(</span><span class="sxs-lookup"><span data-stu-id="66e9d-212">check_codes.verifyMOD1271_36(</span></span>  
32. <span data-ttu-id="66e9d-213">Laiendage puul valikut „format”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-213">In the tree, expand 'format'.</span></span>
33. <span data-ttu-id="66e9d-214">Laiendage puul valikut „format\Root: Sequence(Root)”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-214">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
34. <span data-ttu-id="66e9d-215">Laiendage puul jaotist „format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-215">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
35. <span data-ttu-id="66e9d-216">Laiendage puu jaotist „format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-216">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
36. <span data-ttu-id="66e9d-217">Valige puul „format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-217">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
37. <span data-ttu-id="66e9d-218">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="66e9d-218">Click Add data source.</span></span>
38. <span data-ttu-id="66e9d-219">Väljale Valem sisestage „check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-219">In the Formula field, enter 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="66e9d-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="66e9d-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span></span>  
39. <span data-ttu-id="66e9d-221">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="66e9d-221">Click Save.</span></span>
40. <span data-ttu-id="66e9d-222">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="66e9d-222">Close the page.</span></span>
    * <span data-ttu-id="66e9d-223">Kontrollimise tingimus on konfigureeritud nii, et kehtetu IBAN-koodi puhul tagastatakse väärtus VÄÄR, kutsudes rakendusklassi „ISO7064” olemasoleva meetodi „verifyMOD1271_36”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-223">The validation condition has been configured to return FALSE for any invalid IBAN code by calling the existing method ‘verifyMOD1271_36’ of the application class ‘ISO7064’.</span></span> <span data-ttu-id="66e9d-224">Pange tähele, et IBAN-koodi väärtus määratletakse käitusajal dünaamiliselt kutsumismeetodi argumendina sõelutava TXT-faili sisu alusel.</span><span class="sxs-lookup"><span data-stu-id="66e9d-224">Note that the value of the IBAN code is defined dynamically at run-time as the argument of the calling method based on the content of the parsing TXT file.</span></span>   
41. <span data-ttu-id="66e9d-225">Klõpsake käsku Redigeeri teadet.</span><span class="sxs-lookup"><span data-stu-id="66e9d-225">Click Edit message.</span></span>
42. <span data-ttu-id="66e9d-226">Väljale Valem sisestage „CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)”.</span><span class="sxs-lookup"><span data-stu-id="66e9d-226">In the Formula field, enter 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="66e9d-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="66e9d-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span></span>  
43. <span data-ttu-id="66e9d-228">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="66e9d-228">Click Save.</span></span>
44. <span data-ttu-id="66e9d-229">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="66e9d-229">Close the page.</span></span>
45. <span data-ttu-id="66e9d-230">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="66e9d-230">Click Save.</span></span>
46. <span data-ttu-id="66e9d-231">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="66e9d-231">Close the page.</span></span>

## <a name="run-the-format-mapping"></a><span data-ttu-id="66e9d-232">Vormingu vastendamise käitamine</span><span class="sxs-lookup"><span data-stu-id="66e9d-232">Run the format mapping</span></span>
<span data-ttu-id="66e9d-233">Testimiseks käivitage vorminduse vastendamine allalaaditud failiga SampleIncomingMessage.txt.</span><span class="sxs-lookup"><span data-stu-id="66e9d-233">For testing purposes, execute the format mapping using the SampleIncomingMessage.txt file that you downloaded.</span></span> <span data-ttu-id="66e9d-234">Loodud väljund hõlmab andmeid, mis imporditakse valitud TXT-failist ja täidetakse reaalsel importimisel kohandatud andmemudeliga.</span><span class="sxs-lookup"><span data-stu-id="66e9d-234">The generated output includes data that will be imported from the selected TXT file and populated to the custom data model during the real import.</span></span>   
1. <span data-ttu-id="66e9d-235">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="66e9d-235">Click Run.</span></span>
    * <span data-ttu-id="66e9d-236">Klõpsake nuppu Sirvi ja navigeerige varasemalt allalaaditud failini SampleIncomingMessage.txt.</span><span class="sxs-lookup"><span data-stu-id="66e9d-236">Click Browse and navigate to the SampleIncomingMessage.txt file that you previously downloaded.</span></span>  
2. <span data-ttu-id="66e9d-237">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="66e9d-237">Click OK.</span></span>
    * <span data-ttu-id="66e9d-238">Vaadake väljund üle XML-vormingus, mis tähistab valitud failist imporditud ja andmemudelisse porditud andmeid.</span><span class="sxs-lookup"><span data-stu-id="66e9d-238">Review the output in XML format that represents the data that has been imported from the selected file and ported to the data model.</span></span> <span data-ttu-id="66e9d-239">Pange tähele, et töödeldi imporditud TXT-faili ainult 3 rida.</span><span class="sxs-lookup"><span data-stu-id="66e9d-239">Note that only 3 lines of the imported TXT file were processed.</span></span> <span data-ttu-id="66e9d-240">4. real olev kehtetu IBAN-kood jäeti vahele ja teabelogisse lisatakse tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="66e9d-240">The IBAN code on line 4 that is not valid was skipped and an error message is provided in the Infolog.</span></span>  


