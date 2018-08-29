--- 
title: Mudelite ja vastenduste muutmine rakendusandmetega dokumentide loomiseks
description: "Selle protseduuri toimingute lõpule viimiseks peate esmalt teostama protseduuri „ER Avalduse andmete värskendusega dokumentide genereerimine (2. osa – dokumentide genereerimine)“."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.openlocfilehash: 580f00faf6694dc2da476ffa75f995d9a24e0f8b
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="cd27b-103">Mudelite ja vastenduste muutmine rakendusandmetega dokumentide loomiseks</span><span class="sxs-lookup"><span data-stu-id="cd27b-103">Modify models and mappings to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd27b-104">Selle protseduuri toimingute lõpule viimiseks peate esmalt teostama protseduuri „ER Avalduse andmete värskendusega dokumentide genereerimine (2. osa: dokumentide genereerimine)“.</span><span class="sxs-lookup"><span data-stu-id="cd27b-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 2: Generate documents)”.</span></span> 

<span data-ttu-id="cd27b-105">Selles protseduuris demonstreeritakse, kuidas kujundada elektroonilise aruandluse (ER) konfiguratsioone elektroonilise dokumendi genereerimiseks ja avalduse andmete uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="cd27b-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="cd27b-106">Käesolevas näites muudate ER konfiguratsioone, et hakata neid kasutama elektrooniliste dokumentide loomiseks avalduse andmete uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="cd27b-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="cd27b-107">Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll.</span><span class="sxs-lookup"><span data-stu-id="cd27b-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="cd27b-108">Need toimingud saab lõpule viia DEMF-i andmekomplekti abil.</span><span class="sxs-lookup"><span data-stu-id="cd27b-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="cd27b-109">Andmemudeli muutmine</span><span class="sxs-lookup"><span data-stu-id="cd27b-109">Modify data model</span></span>
1. <span data-ttu-id="cd27b-110">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="cd27b-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="cd27b-111">Tehke puul valik „Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="cd27b-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="cd27b-112">Saate laiendada andmemudeli kasutamisviisi.</span><span class="sxs-lookup"><span data-stu-id="cd27b-112">You will extend how you use the data model.</span></span> <span data-ttu-id="cd27b-113">Lisaks selle kasutamisele andmeallikana Intrastat-aruande loomiseks, kasutatakse andmemudelit üksikasjade kogumiseks Intrastat-aruandluse protsessi kohta.</span><span class="sxs-lookup"><span data-stu-id="cd27b-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="cd27b-114">Üksikasju kasutatakse seejärel avalduse andmete uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="cd27b-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="cd27b-115">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="cd27b-115">Click Designer.</span></span>
4. <span data-ttu-id="cd27b-116">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cd27b-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="cd27b-117">Väljale Uus sõlm kui sisestage „Mudeli juur”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="cd27b-118">Tippige nime väljale tekst „For application data update".</span><span class="sxs-lookup"><span data-stu-id="cd27b-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="cd27b-119">Avalduse andmete uuendamiseks</span><span class="sxs-lookup"><span data-stu-id="cd27b-119">For application data update</span></span>  
7. <span data-ttu-id="cd27b-120">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="cd27b-120">Click Add.</span></span>
8. <span data-ttu-id="cd27b-121">Tehke puul valik „For application data update".</span><span class="sxs-lookup"><span data-stu-id="cd27b-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="cd27b-122">See uus juurkaup lisatakse andmevoo määramiseks andmete teisaldamise jaoks Intrastat-aruandest (kasutatakse andmeallikana) avalduse tabelitesse (uuenduse sihtkoht).</span><span class="sxs-lookup"><span data-stu-id="cd27b-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="cd27b-123">Pange tähele, et väljaminevasse dokumenti sisestatud andmete ja avalduse andmete uuendamiseks kasutatavast dokumendist andmete hankimiseks tuleb kasutada erinevaid juurkaupu.</span><span class="sxs-lookup"><span data-stu-id="cd27b-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="cd27b-124">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cd27b-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="cd27b-125">Sisestage nimeväljale Arhiivi päis.</span><span class="sxs-lookup"><span data-stu-id="cd27b-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="cd27b-126">Arhiivi päis</span><span class="sxs-lookup"><span data-stu-id="cd27b-126">Archive header</span></span>  
11. <span data-ttu-id="cd27b-127">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="cd27b-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="cd27b-128">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="cd27b-128">Click Add.</span></span>
    * <span data-ttu-id="cd27b-129">Kuna te loote kirje iga genereeritud Intrastat-aruande jaoks, peate looma selleks uue kauba.</span><span class="sxs-lookup"><span data-stu-id="cd27b-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="cd27b-130">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cd27b-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="cd27b-131">Tippige Faili nimi väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="cd27b-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="cd27b-132">Faili nimi</span><span class="sxs-lookup"><span data-stu-id="cd27b-132">File name</span></span>  
15. <span data-ttu-id="cd27b-133">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="cd27b-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="cd27b-134">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="cd27b-134">Click Add.</span></span>
17. <span data-ttu-id="cd27b-135">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cd27b-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="cd27b-136">Sisestage nimeväljale tekst „Ridade arv".</span><span class="sxs-lookup"><span data-stu-id="cd27b-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="cd27b-137">Ridade arv</span><span class="sxs-lookup"><span data-stu-id="cd27b-137">Number of lines</span></span>  
19. <span data-ttu-id="cd27b-138">Valige väljalt Kaubakood suvand DateTime.</span><span class="sxs-lookup"><span data-stu-id="cd27b-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="cd27b-139">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="cd27b-139">Click Add.</span></span>
    * <span data-ttu-id="cd27b-140">Lisage see kaup nende Intrastat-kannete arvu tähistamiseks, mis kinnitati praeguse aruandlusprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="cd27b-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="cd27b-141">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cd27b-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="cd27b-142">Sisestage nimeväljale „Arhiiviread".</span><span class="sxs-lookup"><span data-stu-id="cd27b-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="cd27b-143">Arhiiviread</span><span class="sxs-lookup"><span data-stu-id="cd27b-143">Archive lines</span></span>  
23. <span data-ttu-id="cd27b-144">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="cd27b-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="cd27b-145">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="cd27b-145">Click Add.</span></span>
    * <span data-ttu-id="cd27b-146">Lisage see kaup selle Intrastat-kannete loendi tähistamiseks, mis kinnitati praeguse aruandlusprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="cd27b-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="cd27b-147">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cd27b-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="cd27b-148">Sisestage väljale Nimi suvand Summa.</span><span class="sxs-lookup"><span data-stu-id="cd27b-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="cd27b-149">Summa</span><span class="sxs-lookup"><span data-stu-id="cd27b-149">Amount</span></span>  
27. <span data-ttu-id="cd27b-150">Valige väljalt Kaubakood suvand Tegelik.</span><span class="sxs-lookup"><span data-stu-id="cd27b-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="cd27b-151">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="cd27b-151">Click Add.</span></span>
29. <span data-ttu-id="cd27b-152">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cd27b-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="cd27b-153">Sisestage nimeväljale valik „Commodity rec id”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="cd27b-154">Kaubakirje ID</span><span class="sxs-lookup"><span data-stu-id="cd27b-154">Commodity rec id</span></span>  
31. <span data-ttu-id="cd27b-155">Valige väljalt Kaubatüüp suvand Int64.</span><span class="sxs-lookup"><span data-stu-id="cd27b-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="cd27b-156">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="cd27b-156">Click Add.</span></span>
33. <span data-ttu-id="cd27b-157">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cd27b-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="cd27b-158">Sisestage nimeväljale tekst „Kaubakood”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="cd27b-159">Kaubakood</span><span class="sxs-lookup"><span data-stu-id="cd27b-159">Item number</span></span>  
35. <span data-ttu-id="cd27b-160">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="cd27b-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="cd27b-161">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="cd27b-161">Click Add.</span></span>
37. <span data-ttu-id="cd27b-162">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="cd27b-162">Click Save.</span></span>
38. <span data-ttu-id="cd27b-163">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="cd27b-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="cd27b-164">Mudelivastenduse muutmine</span><span class="sxs-lookup"><span data-stu-id="cd27b-164">Modify model mapping</span></span>
1. <span data-ttu-id="cd27b-165">Laiendage puul valikut „Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="cd27b-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="cd27b-166">Tehke puul valik „Intrastat (model)\Intrastat (mapping)".</span><span class="sxs-lookup"><span data-stu-id="cd27b-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="cd27b-167">Muutke olemasolevat mudelivastendust, et hakata seda kasutama avalduse andmete uuendamiseks ja Intrastat-aruande üksikasjade arhiivimiseks.</span><span class="sxs-lookup"><span data-stu-id="cd27b-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="cd27b-168">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="cd27b-168">Click Designer.</span></span>
4. <span data-ttu-id="cd27b-169">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cd27b-169">Click New.</span></span>
5. <span data-ttu-id="cd27b-170">Sisestage nimeväljale „Uuenda arhiiv".</span><span class="sxs-lookup"><span data-stu-id="cd27b-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="cd27b-171">Arhiivi uuendamine</span><span class="sxs-lookup"><span data-stu-id="cd27b-171">Update archive</span></span>  
6. <span data-ttu-id="cd27b-172">Tehke suunaväljal valik „To destination".</span><span class="sxs-lookup"><span data-stu-id="cd27b-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="cd27b-173">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="cd27b-173">Click Save.</span></span>
    * <span data-ttu-id="cd27b-174">See uus vastendus määrab andmevoo andmete (Intrastat-aruande üksikasjad) teisaldamiseks andmemudelist avalduse tabelitesse (uuenduse sihtkoht).</span><span class="sxs-lookup"><span data-stu-id="cd27b-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="cd27b-175">Pange tähele, et aruandlusprotsessi jaoks avaldusest hangitavate andmete ja andmemudeli andmete kasutamiseks avalduse andmete uuenduse jaoks tuleb kasutada mudeli erinevaid juurkaupu.</span><span class="sxs-lookup"><span data-stu-id="cd27b-175">Note that different model’s root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="cd27b-176">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="cd27b-176">Click Designer.</span></span>
9. <span data-ttu-id="cd27b-177">Tehke puul valik „Data model\Data model“.</span><span class="sxs-lookup"><span data-stu-id="cd27b-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="cd27b-178">Lisage nõutav andmeallikas.</span><span class="sxs-lookup"><span data-stu-id="cd27b-178">Add the required data source.</span></span> <span data-ttu-id="cd27b-179">See on andmemudel, mis sisaldab arhiivitavate kinnitatud Antrastat-kannete üksikasju.</span><span class="sxs-lookup"><span data-stu-id="cd27b-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="cd27b-180">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="cd27b-180">Click Add root.</span></span>
11. <span data-ttu-id="cd27b-181">Sisestage nimeväljale „model”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="cd27b-182">mudel</span><span class="sxs-lookup"><span data-stu-id="cd27b-182">model</span></span>  
12. <span data-ttu-id="cd27b-183">Sisestage või valige definitsiooni väljal väärtus „For application data update”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-183">In the Definition field, enter or select the value ‘For application data update’.</span></span>
    * <span data-ttu-id="cd27b-184">Avalduse andmete uuendamiseks</span><span class="sxs-lookup"><span data-stu-id="cd27b-184">For application data update</span></span>  
13. <span data-ttu-id="cd27b-185">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="cd27b-185">Click OK.</span></span>
14. <span data-ttu-id="cd27b-186">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="cd27b-187">Valige puul suvand Funktsioonid\arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="cd27b-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="cd27b-188">Tehke puul valik „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="cd27b-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="cd27b-189">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="cd27b-189">Click Add.</span></span>
    * <span data-ttu-id="cd27b-190">Kuna soovite nummerdada kinnitatud Intrastat-kandeid arhiivimiseks, peate lisama õige andmeallika.</span><span class="sxs-lookup"><span data-stu-id="cd27b-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="cd27b-191">Sisestage nimeväljale tekst „Enumerated lines".</span><span class="sxs-lookup"><span data-stu-id="cd27b-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="cd27b-192">Nummerdatud read</span><span class="sxs-lookup"><span data-stu-id="cd27b-192">Enumerated lines</span></span>  
19. <span data-ttu-id="cd27b-193">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="cd27b-193">Click Edit formula.</span></span>
20. <span data-ttu-id="cd27b-194">Tehke puul valik „List\ENUMERATE“.</span><span class="sxs-lookup"><span data-stu-id="cd27b-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="cd27b-195">Klõpsake suvandit Funktsiooni lisamine.</span><span class="sxs-lookup"><span data-stu-id="cd27b-195">Click Add function.</span></span>
22. <span data-ttu-id="cd27b-196">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="cd27b-197">Laiendage puul valikut „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="cd27b-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="cd27b-198">Tehke puul valik „model\Archive header\Archive lines”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="cd27b-199">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="cd27b-199">Click Add data source.</span></span>
26. <span data-ttu-id="cd27b-200">Sisestage valemiväljale väärtus „ENUMERATE(model.'Archive header'.'Archive lines')”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="cd27b-201">ENUMERATE(model.'Archive header'.'Archive lines')</span><span class="sxs-lookup"><span data-stu-id="cd27b-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="cd27b-202">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="cd27b-202">Click Save.</span></span>
28. <span data-ttu-id="cd27b-203">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="cd27b-203">Close the page.</span></span>
29. <span data-ttu-id="cd27b-204">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="cd27b-204">Click OK.</span></span>
30. <span data-ttu-id="cd27b-205">Klõpsake nuppu Lisa sihtkoht.</span><span class="sxs-lookup"><span data-stu-id="cd27b-205">Click Add destination.</span></span>
    * <span data-ttu-id="cd27b-206">Lisage avalduse tabelid nõutavate sihtkohtadena, mis nõuavad kinnitatud Intrastat-kannete arhiiviüksikasjade uuendusi.</span><span class="sxs-lookup"><span data-stu-id="cd27b-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="cd27b-207">Sisestage nimeväljale väärtus „Arhiiv”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="cd27b-208">Arhiivi</span><span class="sxs-lookup"><span data-stu-id="cd27b-208">Archive</span></span>  
32. <span data-ttu-id="cd27b-209">Sisestage tabelinime väljale väärtus „IntrastatArchiveGeneral”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="cd27b-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="cd27b-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="cd27b-211">Säilitage kirje toiming Sisesta, et saaksite kirjeid iga Intrastat-aruandluse protsessi üksikasjade arhiivimise ajal lisada.</span><span class="sxs-lookup"><span data-stu-id="cd27b-211">Keep the record action ‘Insert’ so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="cd27b-212">Valige Jah väljal Teabelogi kirjendamine.</span><span class="sxs-lookup"><span data-stu-id="cd27b-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="cd27b-213">Teabe hankimiseks avalduse andmete uuendamise probleemide kohta valige Jah.</span><span class="sxs-lookup"><span data-stu-id="cd27b-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="cd27b-214">Valige Jah, kirjetegevuse kinnitamise vahelejätmine väljal.</span><span class="sxs-lookup"><span data-stu-id="cd27b-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="cd27b-215">Valige Jah, et tõkestada valideerimistõrkeid tühja "Intrastat-arhiivi ID" välja kohta.</span><span class="sxs-lookup"><span data-stu-id="cd27b-215">Select Yes to suppress validation errors about the empty ‘Intrastat archive ID’ field.</span></span> <span data-ttu-id="cd27b-216">Seda tehakse pärast kirjete lisamist nende järjekorranumbrite sätte põhjal, mis konfigureeriti selle tabeli jaoks väliskaubandusparameetrite vormil.</span><span class="sxs-lookup"><span data-stu-id="cd27b-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="cd27b-217">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="cd27b-217">Click OK.</span></span>
    * <span data-ttu-id="cd27b-218">Siduge lisatud andmeallika (valitud juurkauba alusel filtreeritud mudel) elemendid lisatud sihtkoha elementidega.</span><span class="sxs-lookup"><span data-stu-id="cd27b-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="cd27b-219">Laiendage puul valikut „Archive”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="cd27b-220">Laiendage puul valikut „Archive\<Relations“.</span><span class="sxs-lookup"><span data-stu-id="cd27b-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="cd27b-221">Laiendage puul valikut „Archive\<Relations\IntrastatArchiveDetail”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="cd27b-222">Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="cd27b-223">Laiendage puul valikut „model\Archive header\Enumerated lines”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="cd27b-224">Laiendage puul valikut „model\Archive header\Enumerated lines\Value”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="cd27b-225">Tehke puul valik „model\Archive header\Enumerated lines\Value\Amount”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="cd27b-226">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="cd27b-226">Click Bind.</span></span>
44. <span data-ttu-id="cd27b-227">Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="cd27b-228">Tehke puul valik „model\Archive header\Enumerated lines\Value\Commodity rec id”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="cd27b-229">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="cd27b-229">Click Bind.</span></span>
47. <span data-ttu-id="cd27b-230">Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="cd27b-231">Tehke puul valik „model\Archive header\Enumerated lines\Value\Item number”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="cd27b-232">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="cd27b-232">Click Bind.</span></span>
50. <span data-ttu-id="cd27b-233">Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="cd27b-234">Tehke puul valik „model\Archive header\Enumerated lines\Number”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="cd27b-235">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="cd27b-235">Click Bind.</span></span>
53. <span data-ttu-id="cd27b-236">Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="cd27b-237">Tehke puul valik „model\Archive header\Enumerated lines”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="cd27b-238">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="cd27b-238">Click Bind.</span></span>
56. <span data-ttu-id="cd27b-239">Tehke puul valik „Archive\File name(FileName)”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="cd27b-240">Tehke puul valik „model\Archive header\File name”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="cd27b-241">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="cd27b-241">Click Bind.</span></span>
59. <span data-ttu-id="cd27b-242">Tehke puul valik „Archive\Number of lines(NumberOfLines)”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="cd27b-243">Tehke puul valik „model\Archive header\Number of lines”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="cd27b-244">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="cd27b-244">Click Bind.</span></span>
62. <span data-ttu-id="cd27b-245">Valige puul väärtus „Archive”.</span><span class="sxs-lookup"><span data-stu-id="cd27b-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="cd27b-246">Tehke puul valik „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="cd27b-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="cd27b-247">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="cd27b-247">Click Bind.</span></span>
65. <span data-ttu-id="cd27b-248">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="cd27b-248">Click Save.</span></span>
66. <span data-ttu-id="cd27b-249">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="cd27b-249">Close the page.</span></span>
67. <span data-ttu-id="cd27b-250">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="cd27b-250">Close the page.</span></span>


