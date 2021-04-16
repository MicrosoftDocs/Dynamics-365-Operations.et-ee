---
title: Mudelite ja vastenduste muutmine rakendusandmetega dokumentide loomiseks
description: Selles teemas kirjeldatakse, kuidas kujundada aruandluse konfiguratsioone elektroonilise dokumendi loomiseks ja värskendada rakenduse andmeid. (2. osa – dokumentide loomine).
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78b1771d0e01702162192ff20c03facbba4f3513
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751602"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="0c500-104">Mudelite ja vastenduste muutmine rakendusandmetega dokumentide loomiseks</span><span class="sxs-lookup"><span data-stu-id="0c500-104">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c500-105">Selle protseduuri toimingute lõpule viimiseks peate esmalt teostama protseduuri „ER Avalduse andmete värskendusega dokumentide genereerimine (2. osa: dokumentide genereerimine)“.</span><span class="sxs-lookup"><span data-stu-id="0c500-105">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="0c500-106">Selles protseduuris demonstreeritakse, kuidas kujundada elektroonilise aruandluse (ER) konfiguratsioone elektroonilise dokumendi genereerimiseks ja avalduse andmete uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="0c500-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="0c500-107">Käesolevas näites muudate ER konfiguratsioone, et hakata neid kasutama elektrooniliste dokumentide loomiseks avalduse andmete uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="0c500-107">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="0c500-108">Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll.</span><span class="sxs-lookup"><span data-stu-id="0c500-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="0c500-109">Need toimingud saab lõpule viia DEMF-i andmekomplekti abil.</span><span class="sxs-lookup"><span data-stu-id="0c500-109">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="0c500-110">Andmemudeli muutmine</span><span class="sxs-lookup"><span data-stu-id="0c500-110">Modify data model</span></span>
1. <span data-ttu-id="0c500-111">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="0c500-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="0c500-112">Tehke puul valik „Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="0c500-112">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="0c500-113">Saate laiendada andmemudeli kasutamisviisi.</span><span class="sxs-lookup"><span data-stu-id="0c500-113">You will extend how you use the data model.</span></span> <span data-ttu-id="0c500-114">Lisaks selle kasutamisele andmeallikana Intrastat-aruande loomiseks, kasutatakse andmemudelit üksikasjade kogumiseks Intrastat-aruandluse protsessi kohta.</span><span class="sxs-lookup"><span data-stu-id="0c500-114">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="0c500-115">Üksikasju kasutatakse seejärel avalduse andmete uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="0c500-115">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="0c500-116">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="0c500-116">Click Designer.</span></span>
4. <span data-ttu-id="0c500-117">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c500-117">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="0c500-118">Väljale Uus sõlm kui sisestage „Mudeli juur”.</span><span class="sxs-lookup"><span data-stu-id="0c500-118">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="0c500-119">Tippige nime väljale tekst „For application data update".</span><span class="sxs-lookup"><span data-stu-id="0c500-119">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="0c500-120">Avalduse andmete uuendamiseks</span><span class="sxs-lookup"><span data-stu-id="0c500-120">For application data update</span></span>  
7. <span data-ttu-id="0c500-121">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c500-121">Click Add.</span></span>
8. <span data-ttu-id="0c500-122">Tehke puul valik „For application data update".</span><span class="sxs-lookup"><span data-stu-id="0c500-122">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="0c500-123">See uus juurkaup lisatakse andmevoo määramiseks andmete teisaldamise jaoks Intrastat-aruandest (kasutatakse andmeallikana) avalduse tabelitesse (uuenduse sihtkoht).</span><span class="sxs-lookup"><span data-stu-id="0c500-123">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="0c500-124">Pange tähele, et väljaminevasse dokumenti sisestatud andmete ja avalduse andmete uuendamiseks kasutatavast dokumendist andmete hankimiseks tuleb kasutada erinevaid juurkaupu.</span><span class="sxs-lookup"><span data-stu-id="0c500-124">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="0c500-125">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c500-125">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="0c500-126">Sisestage nimeväljale Arhiivi päis.</span><span class="sxs-lookup"><span data-stu-id="0c500-126">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="0c500-127">Arhiivi päis</span><span class="sxs-lookup"><span data-stu-id="0c500-127">Archive header</span></span>  
11. <span data-ttu-id="0c500-128">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="0c500-128">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="0c500-129">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c500-129">Click Add.</span></span>
    * <span data-ttu-id="0c500-130">Kuna te loote kirje iga genereeritud Intrastat-aruande jaoks, peate looma selleks uue kauba.</span><span class="sxs-lookup"><span data-stu-id="0c500-130">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="0c500-131">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c500-131">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="0c500-132">Tippige Faili nimi väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="0c500-132">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="0c500-133">Faili nimi</span><span class="sxs-lookup"><span data-stu-id="0c500-133">File name</span></span>  
15. <span data-ttu-id="0c500-134">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="0c500-134">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="0c500-135">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c500-135">Click Add.</span></span>
17. <span data-ttu-id="0c500-136">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c500-136">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="0c500-137">Sisestage nimeväljale tekst „Ridade arv".</span><span class="sxs-lookup"><span data-stu-id="0c500-137">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="0c500-138">Ridade arv</span><span class="sxs-lookup"><span data-stu-id="0c500-138">Number of lines</span></span>  
19. <span data-ttu-id="0c500-139">Valige väljalt Kaubakood suvand DateTime.</span><span class="sxs-lookup"><span data-stu-id="0c500-139">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="0c500-140">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c500-140">Click Add.</span></span>
    * <span data-ttu-id="0c500-141">Lisage see kaup nende Intrastat-kannete arvu tähistamiseks, mis kinnitati praeguse aruandlusprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="0c500-141">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="0c500-142">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c500-142">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="0c500-143">Sisestage nimeväljale „Arhiiviread".</span><span class="sxs-lookup"><span data-stu-id="0c500-143">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="0c500-144">Arhiiviread</span><span class="sxs-lookup"><span data-stu-id="0c500-144">Archive lines</span></span>  
23. <span data-ttu-id="0c500-145">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="0c500-145">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="0c500-146">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c500-146">Click Add.</span></span>
    * <span data-ttu-id="0c500-147">Lisage see kaup selle Intrastat-kannete loendi tähistamiseks, mis kinnitati praeguse aruandlusprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="0c500-147">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="0c500-148">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c500-148">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="0c500-149">Sisestage väljale Nimi suvand Summa.</span><span class="sxs-lookup"><span data-stu-id="0c500-149">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="0c500-150">Summa</span><span class="sxs-lookup"><span data-stu-id="0c500-150">Amount</span></span>  
27. <span data-ttu-id="0c500-151">Valige väljalt Kaubakood suvand Tegelik.</span><span class="sxs-lookup"><span data-stu-id="0c500-151">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="0c500-152">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c500-152">Click Add.</span></span>
29. <span data-ttu-id="0c500-153">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c500-153">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="0c500-154">Sisestage nimeväljale valik „Commodity rec id”.</span><span class="sxs-lookup"><span data-stu-id="0c500-154">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="0c500-155">Kaubakirje ID</span><span class="sxs-lookup"><span data-stu-id="0c500-155">Commodity rec id</span></span>  
31. <span data-ttu-id="0c500-156">Valige väljalt Kaubatüüp suvand Int64.</span><span class="sxs-lookup"><span data-stu-id="0c500-156">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="0c500-157">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c500-157">Click Add.</span></span>
33. <span data-ttu-id="0c500-158">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c500-158">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="0c500-159">Sisestage nimeväljale tekst „Kaubakood”.</span><span class="sxs-lookup"><span data-stu-id="0c500-159">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="0c500-160">Kaubakood</span><span class="sxs-lookup"><span data-stu-id="0c500-160">Item number</span></span>  
35. <span data-ttu-id="0c500-161">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="0c500-161">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="0c500-162">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c500-162">Click Add.</span></span>
37. <span data-ttu-id="0c500-163">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="0c500-163">Click Save.</span></span>
38. <span data-ttu-id="0c500-164">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0c500-164">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="0c500-165">Mudelivastenduse muutmine</span><span class="sxs-lookup"><span data-stu-id="0c500-165">Modify model mapping</span></span>
1. <span data-ttu-id="0c500-166">Laiendage puul valikut „Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="0c500-166">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="0c500-167">Tehke puul valik „Intrastat (model)\Intrastat (mapping)".</span><span class="sxs-lookup"><span data-stu-id="0c500-167">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="0c500-168">Muutke olemasolevat mudelivastendust, et hakata seda kasutama avalduse andmete uuendamiseks ja Intrastat-aruande üksikasjade arhiivimiseks.</span><span class="sxs-lookup"><span data-stu-id="0c500-168">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="0c500-169">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="0c500-169">Click Designer.</span></span>
4. <span data-ttu-id="0c500-170">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c500-170">Click New.</span></span>
5. <span data-ttu-id="0c500-171">Sisestage nimeväljale „Uuenda arhiiv".</span><span class="sxs-lookup"><span data-stu-id="0c500-171">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="0c500-172">Arhiivi uuendamine</span><span class="sxs-lookup"><span data-stu-id="0c500-172">Update archive</span></span>  
6. <span data-ttu-id="0c500-173">Tehke suunaväljal valik „To destination".</span><span class="sxs-lookup"><span data-stu-id="0c500-173">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="0c500-174">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="0c500-174">Click Save.</span></span>
    * <span data-ttu-id="0c500-175">See uus vastendus määrab andmevoo andmete (Intrastat-aruande üksikasjad) teisaldamiseks andmemudelist avalduse tabelitesse (uuenduse sihtkoht).</span><span class="sxs-lookup"><span data-stu-id="0c500-175">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="0c500-176">Pange tähele, et aruandlusprotsessi jaoks avaldusest hangitavate andmete ja andmemudeli andmete kasutamiseks avalduse andmete uuenduse jaoks tuleb kasutada mudeli erinevaid juurkaupu.</span><span class="sxs-lookup"><span data-stu-id="0c500-176">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="0c500-177">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="0c500-177">Click Designer.</span></span>
9. <span data-ttu-id="0c500-178">Tehke puul valik „Data model\Data model“.</span><span class="sxs-lookup"><span data-stu-id="0c500-178">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="0c500-179">Lisage nõutav andmeallikas.</span><span class="sxs-lookup"><span data-stu-id="0c500-179">Add the required data source.</span></span> <span data-ttu-id="0c500-180">See on andmemudel, mis sisaldab arhiivitavate kinnitatud Antrastat-kannete üksikasju.</span><span class="sxs-lookup"><span data-stu-id="0c500-180">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="0c500-181">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="0c500-181">Click Add root.</span></span>
11. <span data-ttu-id="0c500-182">Sisestage nimeväljale „model”.</span><span class="sxs-lookup"><span data-stu-id="0c500-182">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="0c500-183">mudel</span><span class="sxs-lookup"><span data-stu-id="0c500-183">model</span></span>  
12. <span data-ttu-id="0c500-184">Sisestage või valige definitsiooni väljal väärtus „Avalduse andmete uuendamiseks”.</span><span class="sxs-lookup"><span data-stu-id="0c500-184">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="0c500-185">Avalduse andmete uuendamiseks</span><span class="sxs-lookup"><span data-stu-id="0c500-185">For application data update</span></span>  
13. <span data-ttu-id="0c500-186">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0c500-186">Click OK.</span></span>
14. <span data-ttu-id="0c500-187">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="0c500-187">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="0c500-188">Valige puul suvand Funktsioonid\arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="0c500-188">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="0c500-189">Tehke puul valik „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="0c500-189">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="0c500-190">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c500-190">Click Add.</span></span>
    * <span data-ttu-id="0c500-191">Kuna soovite nummerdada kinnitatud Intrastat-kandeid arhiivimiseks, peate lisama õige andmeallika.</span><span class="sxs-lookup"><span data-stu-id="0c500-191">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="0c500-192">Sisestage nimeväljale tekst „Enumerated lines".</span><span class="sxs-lookup"><span data-stu-id="0c500-192">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="0c500-193">Nummerdatud read</span><span class="sxs-lookup"><span data-stu-id="0c500-193">Enumerated lines</span></span>  
19. <span data-ttu-id="0c500-194">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="0c500-194">Click Edit formula.</span></span>
20. <span data-ttu-id="0c500-195">Tehke puul valik „List\ENUMERATE“.</span><span class="sxs-lookup"><span data-stu-id="0c500-195">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="0c500-196">Klõpsake suvandit Funktsiooni lisamine.</span><span class="sxs-lookup"><span data-stu-id="0c500-196">Click Add function.</span></span>
22. <span data-ttu-id="0c500-197">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="0c500-197">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="0c500-198">Laiendage puul valikut „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="0c500-198">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="0c500-199">Tehke puul valik „model\Archive header\Archive lines”.</span><span class="sxs-lookup"><span data-stu-id="0c500-199">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="0c500-200">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="0c500-200">Click Add data source.</span></span>
26. <span data-ttu-id="0c500-201">Sisestage valemiväljale väärtus „ENUMERATE(model.'Archive header'.'Archive lines')”.</span><span class="sxs-lookup"><span data-stu-id="0c500-201">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="0c500-202">ENUMERATE(model.'Archive header'.'Archive lines')</span><span class="sxs-lookup"><span data-stu-id="0c500-202">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="0c500-203">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="0c500-203">Click Save.</span></span>
28. <span data-ttu-id="0c500-204">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0c500-204">Close the page.</span></span>
29. <span data-ttu-id="0c500-205">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0c500-205">Click OK.</span></span>
30. <span data-ttu-id="0c500-206">Klõpsake nuppu Lisa sihtkoht.</span><span class="sxs-lookup"><span data-stu-id="0c500-206">Click Add destination.</span></span>
    * <span data-ttu-id="0c500-207">Lisage avalduse tabelid nõutavate sihtkohtadena, mis nõuavad kinnitatud Intrastat-kannete arhiiviüksikasjade uuendusi.</span><span class="sxs-lookup"><span data-stu-id="0c500-207">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="0c500-208">Sisestage nimeväljale väärtus „Arhiiv”.</span><span class="sxs-lookup"><span data-stu-id="0c500-208">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="0c500-209">Arhiivi</span><span class="sxs-lookup"><span data-stu-id="0c500-209">Archive</span></span>  
32. <span data-ttu-id="0c500-210">Sisestage tabelinime väljale väärtus „IntrastatArchiveGeneral”.</span><span class="sxs-lookup"><span data-stu-id="0c500-210">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="0c500-211">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="0c500-211">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="0c500-212">Säilitage kirje toiming „Sisesta”, et saaksite kirjeid iga Intrastat-aruandluse protsessi üksikasjade arhiivimise ajal lisada.</span><span class="sxs-lookup"><span data-stu-id="0c500-212">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="0c500-213">Valige Jah väljal Teabelogi kirjendamine.</span><span class="sxs-lookup"><span data-stu-id="0c500-213">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="0c500-214">Teabe hankimiseks avalduse andmete uuendamise probleemide kohta valige Jah.</span><span class="sxs-lookup"><span data-stu-id="0c500-214">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="0c500-215">Valige Jah, kirjetegevuse kinnitamise vahelejätmine väljal.</span><span class="sxs-lookup"><span data-stu-id="0c500-215">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="0c500-216">Valige Jah, et tõkestada valideerimistõrkeid tühja välja „Intrastat-arhiivi ID” kohta.</span><span class="sxs-lookup"><span data-stu-id="0c500-216">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="0c500-217">Seda tehakse pärast kirjete lisamist nende järjekorranumbrite sätte põhjal, mis konfigureeriti selle tabeli jaoks väliskaubandusparameetrite vormil.</span><span class="sxs-lookup"><span data-stu-id="0c500-217">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="0c500-218">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0c500-218">Click OK.</span></span>
    * <span data-ttu-id="0c500-219">Siduge lisatud andmeallika (valitud juurkauba alusel filtreeritud mudel) elemendid lisatud sihtkoha elementidega.</span><span class="sxs-lookup"><span data-stu-id="0c500-219">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="0c500-220">Laiendage puul valikut „Archive”.</span><span class="sxs-lookup"><span data-stu-id="0c500-220">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="0c500-221">Laiendage puul valikut „Archive\<Relations“.</span><span class="sxs-lookup"><span data-stu-id="0c500-221">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="0c500-222">Laiendage puul valikut „Archive\<Relations\IntrastatArchiveDetail”.</span><span class="sxs-lookup"><span data-stu-id="0c500-222">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="0c500-223">Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)”.</span><span class="sxs-lookup"><span data-stu-id="0c500-223">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="0c500-224">Laiendage puul valikut „model\Archive header\Enumerated lines”.</span><span class="sxs-lookup"><span data-stu-id="0c500-224">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="0c500-225">Laiendage puul valikut „model\Archive header\Enumerated lines\Value”.</span><span class="sxs-lookup"><span data-stu-id="0c500-225">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="0c500-226">Tehke puul valik „model\Archive header\Enumerated lines\Value\Amount”.</span><span class="sxs-lookup"><span data-stu-id="0c500-226">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="0c500-227">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="0c500-227">Click Bind.</span></span>
44. <span data-ttu-id="0c500-228">Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)”.</span><span class="sxs-lookup"><span data-stu-id="0c500-228">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="0c500-229">Tehke puul valik „model\Archive header\Enumerated lines\Value\Commodity rec id”.</span><span class="sxs-lookup"><span data-stu-id="0c500-229">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="0c500-230">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="0c500-230">Click Bind.</span></span>
47. <span data-ttu-id="0c500-231">Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)”.</span><span class="sxs-lookup"><span data-stu-id="0c500-231">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="0c500-232">Tehke puul valik „model\Archive header\Enumerated lines\Value\Item number”.</span><span class="sxs-lookup"><span data-stu-id="0c500-232">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="0c500-233">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="0c500-233">Click Bind.</span></span>
50. <span data-ttu-id="0c500-234">Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)”.</span><span class="sxs-lookup"><span data-stu-id="0c500-234">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="0c500-235">Tehke puul valik „model\Archive header\Enumerated lines\Number”.</span><span class="sxs-lookup"><span data-stu-id="0c500-235">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="0c500-236">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="0c500-236">Click Bind.</span></span>
53. <span data-ttu-id="0c500-237">Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail”.</span><span class="sxs-lookup"><span data-stu-id="0c500-237">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="0c500-238">Tehke puul valik „model\Archive header\Enumerated lines”.</span><span class="sxs-lookup"><span data-stu-id="0c500-238">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="0c500-239">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="0c500-239">Click Bind.</span></span>
56. <span data-ttu-id="0c500-240">Tehke puul valik „Archive\File name(FileName)”.</span><span class="sxs-lookup"><span data-stu-id="0c500-240">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="0c500-241">Tehke puul valik „model\Archive header\File name”.</span><span class="sxs-lookup"><span data-stu-id="0c500-241">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="0c500-242">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="0c500-242">Click Bind.</span></span>
59. <span data-ttu-id="0c500-243">Tehke puul valik „Archive\Number of lines(NumberOfLines)”.</span><span class="sxs-lookup"><span data-stu-id="0c500-243">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="0c500-244">Tehke puul valik „model\Archive header\Number of lines”.</span><span class="sxs-lookup"><span data-stu-id="0c500-244">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="0c500-245">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="0c500-245">Click Bind.</span></span>
62. <span data-ttu-id="0c500-246">Valige puul väärtus „Archive”.</span><span class="sxs-lookup"><span data-stu-id="0c500-246">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="0c500-247">Tehke puul valik „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="0c500-247">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="0c500-248">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="0c500-248">Click Bind.</span></span>
65. <span data-ttu-id="0c500-249">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="0c500-249">Click Save.</span></span>
66. <span data-ttu-id="0c500-250">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0c500-250">Close the page.</span></span>
67. <span data-ttu-id="0c500-251">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0c500-251">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]