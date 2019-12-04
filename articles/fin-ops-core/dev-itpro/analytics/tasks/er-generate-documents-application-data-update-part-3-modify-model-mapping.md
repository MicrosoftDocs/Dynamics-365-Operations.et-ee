---
title: Mudelite ja vastenduste muutmine rakendusandmetega dokumentide loomiseks
description: Selle protseduuri toimingute lõpule viimiseks peate esmalt teostama protseduuri „ER Avalduse andmete värskendusega dokumentide genereerimine (2. osa – dokumentide genereerimine)“.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5df6128228b9ff620c606c550c5eb7a6039b915
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182297"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="244e8-103">Mudelite ja vastenduste muutmine rakendusandmetega dokumentide loomiseks</span><span class="sxs-lookup"><span data-stu-id="244e8-103">Modify models and mappings to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="244e8-104">Selle protseduuri toimingute lõpule viimiseks peate esmalt teostama protseduuri „ER Avalduse andmete värskendusega dokumentide genereerimine (2. osa: dokumentide genereerimine)“.</span><span class="sxs-lookup"><span data-stu-id="244e8-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 2: Generate documents)”.</span></span> 

<span data-ttu-id="244e8-105">Selles protseduuris demonstreeritakse, kuidas kujundada elektroonilise aruandluse (ER) konfiguratsioone elektroonilise dokumendi genereerimiseks ja avalduse andmete uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="244e8-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="244e8-106">Käesolevas näites muudate ER konfiguratsioone, et hakata neid kasutama elektrooniliste dokumentide loomiseks avalduse andmete uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="244e8-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="244e8-107">Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll.</span><span class="sxs-lookup"><span data-stu-id="244e8-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="244e8-108">Need toimingud saab lõpule viia DEMF-i andmekomplekti abil.</span><span class="sxs-lookup"><span data-stu-id="244e8-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="244e8-109">Andmemudeli muutmine</span><span class="sxs-lookup"><span data-stu-id="244e8-109">Modify data model</span></span>
1. <span data-ttu-id="244e8-110">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="244e8-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="244e8-111">Tehke puul valik „Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="244e8-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="244e8-112">Saate laiendada andmemudeli kasutamisviisi.</span><span class="sxs-lookup"><span data-stu-id="244e8-112">You will extend how you use the data model.</span></span> <span data-ttu-id="244e8-113">Lisaks selle kasutamisele andmeallikana Intrastat-aruande loomiseks, kasutatakse andmemudelit üksikasjade kogumiseks Intrastat-aruandluse protsessi kohta.</span><span class="sxs-lookup"><span data-stu-id="244e8-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="244e8-114">Üksikasju kasutatakse seejärel avalduse andmete uuendamiseks.</span><span class="sxs-lookup"><span data-stu-id="244e8-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="244e8-115">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="244e8-115">Click Designer.</span></span>
4. <span data-ttu-id="244e8-116">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="244e8-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="244e8-117">Väljale Uus sõlm kui sisestage „Mudeli juur”.</span><span class="sxs-lookup"><span data-stu-id="244e8-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="244e8-118">Tippige nime väljale tekst „For application data update".</span><span class="sxs-lookup"><span data-stu-id="244e8-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="244e8-119">Avalduse andmete uuendamiseks</span><span class="sxs-lookup"><span data-stu-id="244e8-119">For application data update</span></span>  
7. <span data-ttu-id="244e8-120">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="244e8-120">Click Add.</span></span>
8. <span data-ttu-id="244e8-121">Tehke puul valik „For application data update".</span><span class="sxs-lookup"><span data-stu-id="244e8-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="244e8-122">See uus juurkaup lisatakse andmevoo määramiseks andmete teisaldamise jaoks Intrastat-aruandest (kasutatakse andmeallikana) avalduse tabelitesse (uuenduse sihtkoht).</span><span class="sxs-lookup"><span data-stu-id="244e8-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="244e8-123">Pange tähele, et väljaminevasse dokumenti sisestatud andmete ja avalduse andmete uuendamiseks kasutatavast dokumendist andmete hankimiseks tuleb kasutada erinevaid juurkaupu.</span><span class="sxs-lookup"><span data-stu-id="244e8-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="244e8-124">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="244e8-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="244e8-125">Sisestage nimeväljale Arhiivi päis.</span><span class="sxs-lookup"><span data-stu-id="244e8-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="244e8-126">Arhiivi päis</span><span class="sxs-lookup"><span data-stu-id="244e8-126">Archive header</span></span>  
11. <span data-ttu-id="244e8-127">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="244e8-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="244e8-128">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="244e8-128">Click Add.</span></span>
    * <span data-ttu-id="244e8-129">Kuna te loote kirje iga genereeritud Intrastat-aruande jaoks, peate looma selleks uue kauba.</span><span class="sxs-lookup"><span data-stu-id="244e8-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="244e8-130">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="244e8-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="244e8-131">Tippige Faili nimi väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="244e8-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="244e8-132">Faili nimi</span><span class="sxs-lookup"><span data-stu-id="244e8-132">File name</span></span>  
15. <span data-ttu-id="244e8-133">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="244e8-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="244e8-134">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="244e8-134">Click Add.</span></span>
17. <span data-ttu-id="244e8-135">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="244e8-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="244e8-136">Sisestage nimeväljale tekst „Ridade arv".</span><span class="sxs-lookup"><span data-stu-id="244e8-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="244e8-137">Ridade arv</span><span class="sxs-lookup"><span data-stu-id="244e8-137">Number of lines</span></span>  
19. <span data-ttu-id="244e8-138">Valige väljalt Kaubakood suvand DateTime.</span><span class="sxs-lookup"><span data-stu-id="244e8-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="244e8-139">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="244e8-139">Click Add.</span></span>
    * <span data-ttu-id="244e8-140">Lisage see kaup nende Intrastat-kannete arvu tähistamiseks, mis kinnitati praeguse aruandlusprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="244e8-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="244e8-141">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="244e8-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="244e8-142">Sisestage nimeväljale „Arhiiviread".</span><span class="sxs-lookup"><span data-stu-id="244e8-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="244e8-143">Arhiiviread</span><span class="sxs-lookup"><span data-stu-id="244e8-143">Archive lines</span></span>  
23. <span data-ttu-id="244e8-144">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="244e8-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="244e8-145">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="244e8-145">Click Add.</span></span>
    * <span data-ttu-id="244e8-146">Lisage see kaup selle Intrastat-kannete loendi tähistamiseks, mis kinnitati praeguse aruandlusprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="244e8-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="244e8-147">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="244e8-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="244e8-148">Sisestage väljale Nimi suvand Summa.</span><span class="sxs-lookup"><span data-stu-id="244e8-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="244e8-149">Summa</span><span class="sxs-lookup"><span data-stu-id="244e8-149">Amount</span></span>  
27. <span data-ttu-id="244e8-150">Valige väljalt Kaubakood suvand Tegelik.</span><span class="sxs-lookup"><span data-stu-id="244e8-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="244e8-151">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="244e8-151">Click Add.</span></span>
29. <span data-ttu-id="244e8-152">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="244e8-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="244e8-153">Sisestage nimeväljale valik „Commodity rec id”.</span><span class="sxs-lookup"><span data-stu-id="244e8-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="244e8-154">Kaubakirje ID</span><span class="sxs-lookup"><span data-stu-id="244e8-154">Commodity rec id</span></span>  
31. <span data-ttu-id="244e8-155">Valige väljalt Kaubatüüp suvand Int64.</span><span class="sxs-lookup"><span data-stu-id="244e8-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="244e8-156">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="244e8-156">Click Add.</span></span>
33. <span data-ttu-id="244e8-157">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="244e8-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="244e8-158">Sisestage nimeväljale tekst „Kaubakood”.</span><span class="sxs-lookup"><span data-stu-id="244e8-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="244e8-159">Kaubakood</span><span class="sxs-lookup"><span data-stu-id="244e8-159">Item number</span></span>  
35. <span data-ttu-id="244e8-160">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="244e8-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="244e8-161">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="244e8-161">Click Add.</span></span>
37. <span data-ttu-id="244e8-162">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="244e8-162">Click Save.</span></span>
38. <span data-ttu-id="244e8-163">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="244e8-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="244e8-164">Mudelivastenduse muutmine</span><span class="sxs-lookup"><span data-stu-id="244e8-164">Modify model mapping</span></span>
1. <span data-ttu-id="244e8-165">Laiendage puul valikut „Intrastat (model)".</span><span class="sxs-lookup"><span data-stu-id="244e8-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="244e8-166">Tehke puul valik „Intrastat (model)\Intrastat (mapping)".</span><span class="sxs-lookup"><span data-stu-id="244e8-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="244e8-167">Muutke olemasolevat mudelivastendust, et hakata seda kasutama avalduse andmete uuendamiseks ja Intrastat-aruande üksikasjade arhiivimiseks.</span><span class="sxs-lookup"><span data-stu-id="244e8-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="244e8-168">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="244e8-168">Click Designer.</span></span>
4. <span data-ttu-id="244e8-169">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="244e8-169">Click New.</span></span>
5. <span data-ttu-id="244e8-170">Sisestage nimeväljale „Uuenda arhiiv".</span><span class="sxs-lookup"><span data-stu-id="244e8-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="244e8-171">Arhiivi uuendamine</span><span class="sxs-lookup"><span data-stu-id="244e8-171">Update archive</span></span>  
6. <span data-ttu-id="244e8-172">Tehke suunaväljal valik „To destination".</span><span class="sxs-lookup"><span data-stu-id="244e8-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="244e8-173">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="244e8-173">Click Save.</span></span>
    * <span data-ttu-id="244e8-174">See uus vastendus määrab andmevoo andmete (Intrastat-aruande üksikasjad) teisaldamiseks andmemudelist avalduse tabelitesse (uuenduse sihtkoht).</span><span class="sxs-lookup"><span data-stu-id="244e8-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="244e8-175">Pange tähele, et aruandlusprotsessi jaoks avaldusest hangitavate andmete ja andmemudeli andmete kasutamiseks avalduse andmete uuenduse jaoks tuleb kasutada mudeli erinevaid juurkaupu.</span><span class="sxs-lookup"><span data-stu-id="244e8-175">Note that different model’s root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="244e8-176">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="244e8-176">Click Designer.</span></span>
9. <span data-ttu-id="244e8-177">Tehke puul valik „Data model\Data model“.</span><span class="sxs-lookup"><span data-stu-id="244e8-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="244e8-178">Lisage nõutav andmeallikas.</span><span class="sxs-lookup"><span data-stu-id="244e8-178">Add the required data source.</span></span> <span data-ttu-id="244e8-179">See on andmemudel, mis sisaldab arhiivitavate kinnitatud Antrastat-kannete üksikasju.</span><span class="sxs-lookup"><span data-stu-id="244e8-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="244e8-180">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="244e8-180">Click Add root.</span></span>
11. <span data-ttu-id="244e8-181">Sisestage nimeväljale „model”.</span><span class="sxs-lookup"><span data-stu-id="244e8-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="244e8-182">mudel</span><span class="sxs-lookup"><span data-stu-id="244e8-182">model</span></span>  
12. <span data-ttu-id="244e8-183">Sisestage või valige definitsiooni väljal väärtus „For application data update”.</span><span class="sxs-lookup"><span data-stu-id="244e8-183">In the Definition field, enter or select the value ‘For application data update’.</span></span>
    * <span data-ttu-id="244e8-184">Avalduse andmete uuendamiseks</span><span class="sxs-lookup"><span data-stu-id="244e8-184">For application data update</span></span>  
13. <span data-ttu-id="244e8-185">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="244e8-185">Click OK.</span></span>
14. <span data-ttu-id="244e8-186">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="244e8-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="244e8-187">Valige puul suvand Funktsioonid\arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="244e8-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="244e8-188">Tehke puul valik „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="244e8-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="244e8-189">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="244e8-189">Click Add.</span></span>
    * <span data-ttu-id="244e8-190">Kuna soovite nummerdada kinnitatud Intrastat-kandeid arhiivimiseks, peate lisama õige andmeallika.</span><span class="sxs-lookup"><span data-stu-id="244e8-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="244e8-191">Sisestage nimeväljale tekst „Enumerated lines".</span><span class="sxs-lookup"><span data-stu-id="244e8-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="244e8-192">Nummerdatud read</span><span class="sxs-lookup"><span data-stu-id="244e8-192">Enumerated lines</span></span>  
19. <span data-ttu-id="244e8-193">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="244e8-193">Click Edit formula.</span></span>
20. <span data-ttu-id="244e8-194">Tehke puul valik „List\ENUMERATE“.</span><span class="sxs-lookup"><span data-stu-id="244e8-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="244e8-195">Klõpsake suvandit Funktsiooni lisamine.</span><span class="sxs-lookup"><span data-stu-id="244e8-195">Click Add function.</span></span>
22. <span data-ttu-id="244e8-196">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="244e8-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="244e8-197">Laiendage puul valikut „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="244e8-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="244e8-198">Tehke puul valik „model\Archive header\Archive lines”.</span><span class="sxs-lookup"><span data-stu-id="244e8-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="244e8-199">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="244e8-199">Click Add data source.</span></span>
26. <span data-ttu-id="244e8-200">Sisestage valemiväljale väärtus „ENUMERATE(model.'Archive header'.'Archive lines')”.</span><span class="sxs-lookup"><span data-stu-id="244e8-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="244e8-201">ENUMERATE(model.'Archive header'.'Archive lines')</span><span class="sxs-lookup"><span data-stu-id="244e8-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="244e8-202">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="244e8-202">Click Save.</span></span>
28. <span data-ttu-id="244e8-203">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="244e8-203">Close the page.</span></span>
29. <span data-ttu-id="244e8-204">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="244e8-204">Click OK.</span></span>
30. <span data-ttu-id="244e8-205">Klõpsake nuppu Lisa sihtkoht.</span><span class="sxs-lookup"><span data-stu-id="244e8-205">Click Add destination.</span></span>
    * <span data-ttu-id="244e8-206">Lisage avalduse tabelid nõutavate sihtkohtadena, mis nõuavad kinnitatud Intrastat-kannete arhiiviüksikasjade uuendusi.</span><span class="sxs-lookup"><span data-stu-id="244e8-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="244e8-207">Sisestage nimeväljale väärtus „Arhiiv”.</span><span class="sxs-lookup"><span data-stu-id="244e8-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="244e8-208">Arhiivi</span><span class="sxs-lookup"><span data-stu-id="244e8-208">Archive</span></span>  
32. <span data-ttu-id="244e8-209">Sisestage tabelinime väljale väärtus „IntrastatArchiveGeneral”.</span><span class="sxs-lookup"><span data-stu-id="244e8-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="244e8-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="244e8-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="244e8-211">Säilitage kirje toiming Sisesta, et saaksite kirjeid iga Intrastat-aruandluse protsessi üksikasjade arhiivimise ajal lisada.</span><span class="sxs-lookup"><span data-stu-id="244e8-211">Keep the record action ‘Insert’ so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="244e8-212">Valige Jah väljal Teabelogi kirjendamine.</span><span class="sxs-lookup"><span data-stu-id="244e8-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="244e8-213">Teabe hankimiseks avalduse andmete uuendamise probleemide kohta valige Jah.</span><span class="sxs-lookup"><span data-stu-id="244e8-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="244e8-214">Valige Jah, kirjetegevuse kinnitamise vahelejätmine väljal.</span><span class="sxs-lookup"><span data-stu-id="244e8-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="244e8-215">Valige Jah, et tõkestada valideerimistõrkeid tühja "Intrastat-arhiivi ID" välja kohta.</span><span class="sxs-lookup"><span data-stu-id="244e8-215">Select Yes to suppress validation errors about the empty ‘Intrastat archive ID’ field.</span></span> <span data-ttu-id="244e8-216">Seda tehakse pärast kirjete lisamist nende järjekorranumbrite sätte põhjal, mis konfigureeriti selle tabeli jaoks väliskaubandusparameetrite vormil.</span><span class="sxs-lookup"><span data-stu-id="244e8-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="244e8-217">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="244e8-217">Click OK.</span></span>
    * <span data-ttu-id="244e8-218">Siduge lisatud andmeallika (valitud juurkauba alusel filtreeritud mudel) elemendid lisatud sihtkoha elementidega.</span><span class="sxs-lookup"><span data-stu-id="244e8-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="244e8-219">Laiendage puul valikut „Archive”.</span><span class="sxs-lookup"><span data-stu-id="244e8-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="244e8-220">Laiendage puul valikut „Archive\<Relations“.</span><span class="sxs-lookup"><span data-stu-id="244e8-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="244e8-221">Laiendage puul valikut „Archive\<Relations\IntrastatArchiveDetail”.</span><span class="sxs-lookup"><span data-stu-id="244e8-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="244e8-222">Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)”.</span><span class="sxs-lookup"><span data-stu-id="244e8-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="244e8-223">Laiendage puul valikut „model\Archive header\Enumerated lines”.</span><span class="sxs-lookup"><span data-stu-id="244e8-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="244e8-224">Laiendage puul valikut „model\Archive header\Enumerated lines\Value”.</span><span class="sxs-lookup"><span data-stu-id="244e8-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="244e8-225">Tehke puul valik „model\Archive header\Enumerated lines\Value\Amount”.</span><span class="sxs-lookup"><span data-stu-id="244e8-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="244e8-226">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="244e8-226">Click Bind.</span></span>
44. <span data-ttu-id="244e8-227">Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)”.</span><span class="sxs-lookup"><span data-stu-id="244e8-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="244e8-228">Tehke puul valik „model\Archive header\Enumerated lines\Value\Commodity rec id”.</span><span class="sxs-lookup"><span data-stu-id="244e8-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="244e8-229">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="244e8-229">Click Bind.</span></span>
47. <span data-ttu-id="244e8-230">Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)”.</span><span class="sxs-lookup"><span data-stu-id="244e8-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="244e8-231">Tehke puul valik „model\Archive header\Enumerated lines\Value\Item number”.</span><span class="sxs-lookup"><span data-stu-id="244e8-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="244e8-232">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="244e8-232">Click Bind.</span></span>
50. <span data-ttu-id="244e8-233">Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)”.</span><span class="sxs-lookup"><span data-stu-id="244e8-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="244e8-234">Tehke puul valik „model\Archive header\Enumerated lines\Number”.</span><span class="sxs-lookup"><span data-stu-id="244e8-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="244e8-235">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="244e8-235">Click Bind.</span></span>
53. <span data-ttu-id="244e8-236">Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail”.</span><span class="sxs-lookup"><span data-stu-id="244e8-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="244e8-237">Tehke puul valik „model\Archive header\Enumerated lines”.</span><span class="sxs-lookup"><span data-stu-id="244e8-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="244e8-238">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="244e8-238">Click Bind.</span></span>
56. <span data-ttu-id="244e8-239">Tehke puul valik „Archive\File name(FileName)”.</span><span class="sxs-lookup"><span data-stu-id="244e8-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="244e8-240">Tehke puul valik „model\Archive header\File name”.</span><span class="sxs-lookup"><span data-stu-id="244e8-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="244e8-241">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="244e8-241">Click Bind.</span></span>
59. <span data-ttu-id="244e8-242">Tehke puul valik „Archive\Number of lines(NumberOfLines)”.</span><span class="sxs-lookup"><span data-stu-id="244e8-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="244e8-243">Tehke puul valik „model\Archive header\Number of lines”.</span><span class="sxs-lookup"><span data-stu-id="244e8-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="244e8-244">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="244e8-244">Click Bind.</span></span>
62. <span data-ttu-id="244e8-245">Valige puul väärtus „Archive”.</span><span class="sxs-lookup"><span data-stu-id="244e8-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="244e8-246">Tehke puul valik „model\Archive header“.</span><span class="sxs-lookup"><span data-stu-id="244e8-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="244e8-247">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="244e8-247">Click Bind.</span></span>
65. <span data-ttu-id="244e8-248">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="244e8-248">Click Save.</span></span>
66. <span data-ttu-id="244e8-249">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="244e8-249">Close the page.</span></span>
67. <span data-ttu-id="244e8-250">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="244e8-250">Close the page.</span></span>
