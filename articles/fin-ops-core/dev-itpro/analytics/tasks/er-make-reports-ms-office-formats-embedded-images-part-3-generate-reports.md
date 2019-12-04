---
title: Manuspiltidega aruannete loomine Office’i vormingus
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua elektroonilise aruandluse (ER) konfiguratsioone manuspilte sisaldavate elektrooniliste dokumentide loomiseks MS Office'i vormingutes (Excel ja Word).
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.openlocfilehash: 64fade6578e9cd4f8a51c524e4f6ebbf63b93f20
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184757"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="f3a56-103">Manuspiltidega aruannete loomine Office’i vormingus</span><span class="sxs-lookup"><span data-stu-id="f3a56-103">Generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3a56-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua elektroonilise aruandluse (ER) konfiguratsioone manuspilte sisaldavate elektrooniliste dokumentide loomiseks MS Office'i vormingutes (Excel ja Word).</span><span class="sxs-lookup"><span data-stu-id="f3a56-104">The following steps explain how a user playing either ‘System administrator’ or ‘Electronic reporting developer’ role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="f3a56-105">Selles näites kasutate näidisettevõtte Litware, Inc. jaoks loodud elektroonilise aruandluse konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="f3a56-105">In this example, you will use created ER configurations for sample company, ‘Litware, Inc.’.</span></span>  <span data-ttu-id="f3a56-106">Toimingute teostamiseks peab esmalt täitma juhendis "ER MS Office'i vormingutes manuspiltidega aruannete koostamine (2. osa: konfiguratsioonide ülevaatamine)" toodud toimingud.</span><span class="sxs-lookup"><span data-stu-id="f3a56-106">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)” task guide.</span></span> <span data-ttu-id="f3a56-107">Neid toiminguid saab teha ettevõttes USMF</span><span class="sxs-lookup"><span data-stu-id="f3a56-107">These steps can be performed in ‘USMF’ company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="f3a56-108">Vormingu käivitamine algse mudelivastendusega</span><span class="sxs-lookup"><span data-stu-id="f3a56-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="f3a56-109">Avage Sularaha- ja pangahaldus > Pangakontod > Pangakontod.</span><span class="sxs-lookup"><span data-stu-id="f3a56-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="f3a56-110">Kasutage kiirfiltrit, et filtrida välja Pangakonto väärtusega USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="f3a56-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="f3a56-111">Klõpsake tegumiribal valikut Seadistus.</span><span class="sxs-lookup"><span data-stu-id="f3a56-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="f3a56-112">Klõpsake nuppu Kontrolli.</span><span class="sxs-lookup"><span data-stu-id="f3a56-112">Click Check.</span></span>
5. <span data-ttu-id="f3a56-113">Klõpsake valikut Prindi test.</span><span class="sxs-lookup"><span data-stu-id="f3a56-113">Click Print test.</span></span>
    * <span data-ttu-id="f3a56-114">Käivitage testimiseks vorming.</span><span class="sxs-lookup"><span data-stu-id="f3a56-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="f3a56-115">Valige väljal Käibiv tšekivorming väärtus Jah.</span><span class="sxs-lookup"><span data-stu-id="f3a56-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="f3a56-116">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f3a56-116">Click OK.</span></span>
    * <span data-ttu-id="f3a56-117">Vaadake loodud väljund üle.</span><span class="sxs-lookup"><span data-stu-id="f3a56-117">Review the created output.</span></span> <span data-ttu-id="f3a56-118">Võtke arvesse, et aruandes on esitatud nii ettevõtte logo kui ka volitatud isiku allkiri.</span><span class="sxs-lookup"><span data-stu-id="f3a56-118">Note that the company logo is presented in the report as well as the authorized person’s signature.</span></span> <span data-ttu-id="f3a56-119">Allkirja pilt võetakse valitud pangakontoga seotud tšeki paigutusekirje andmetüübi Konteiner väljalt.</span><span class="sxs-lookup"><span data-stu-id="f3a56-119">The signature image is taken from the field of the ‘Container’ data type of the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="f3a56-120">Laiendage jaotis Eksemplare.</span><span class="sxs-lookup"><span data-stu-id="f3a56-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="f3a56-121">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="f3a56-121">Click Edit.</span></span>
10. <span data-ttu-id="f3a56-122">Sisestage väljale Vesimärk tekst Prindi vesimärk kui Tühista.</span><span class="sxs-lookup"><span data-stu-id="f3a56-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="f3a56-123">Muutke vesimärgi paigutuse sätet, et kuvada vesimärgi tekst dokumendi genereerimisel Exceli kujunduselemendis.</span><span class="sxs-lookup"><span data-stu-id="f3a56-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="f3a56-124">Klõpsake valikut Prindi test.</span><span class="sxs-lookup"><span data-stu-id="f3a56-124">Click Print test.</span></span>
12. <span data-ttu-id="f3a56-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f3a56-125">Click OK.</span></span>
    * <span data-ttu-id="f3a56-126">Vaadake loodud väljund üle.</span><span class="sxs-lookup"><span data-stu-id="f3a56-126">Review the created output.</span></span> <span data-ttu-id="f3a56-127">Võtke arvesse, et vesimärk kuvatakse loodud aruandes vastavalt valitud suvandile.</span><span class="sxs-lookup"><span data-stu-id="f3a56-127">Note that the watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="f3a56-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f3a56-128">Close the page.</span></span>
14. <span data-ttu-id="f3a56-129">Klõpsake toimingupaanil valikut Maksete haldamine.</span><span class="sxs-lookup"><span data-stu-id="f3a56-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="f3a56-130">Klõpsake nuppu Kontrolli.</span><span class="sxs-lookup"><span data-stu-id="f3a56-130">Click Checks.</span></span>
16. <span data-ttu-id="f3a56-131">Klõpsake suvandit Näita filtreid.</span><span class="sxs-lookup"><span data-stu-id="f3a56-131">Click Show filters.</span></span>
17. <span data-ttu-id="f3a56-132">Rakendage järgmised filtrid: sisestage väljale Tšeki number filtriväärtus „381“, „385“, „389“, kasutades filtri tehtemärki „üks (mitmest)“.</span><span class="sxs-lookup"><span data-stu-id="f3a56-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="f3a56-133">Märkige loendis kõik read.</span><span class="sxs-lookup"><span data-stu-id="f3a56-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="f3a56-134">Klõpsake valikut Tšeki koopia printimine.</span><span class="sxs-lookup"><span data-stu-id="f3a56-134">Click Print check copy.</span></span>
    * <span data-ttu-id="f3a56-135">Käivitage vorming valitud tšekkide uuesti printimiseks.</span><span class="sxs-lookup"><span data-stu-id="f3a56-135">Run the format to re-print the selected cheques.</span></span>  
    * <span data-ttu-id="f3a56-136">Vaadake loodud väljund üle.</span><span class="sxs-lookup"><span data-stu-id="f3a56-136">Review the created output.</span></span> <span data-ttu-id="f3a56-137">Pange tähele, et valitud tšekid on uuesti prinditud.</span><span class="sxs-lookup"><span data-stu-id="f3a56-137">Note that the selected cheques have been re-printed.</span></span> <span data-ttu-id="f3a56-138">Ettevõtte logo ja silte ei prindita, kuna need on esitatakse eelprinditud vormil.</span><span class="sxs-lookup"><span data-stu-id="f3a56-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="f3a56-139">Imporditud andmemudeli vastenduse muutmine</span><span class="sxs-lookup"><span data-stu-id="f3a56-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="f3a56-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f3a56-140">Close the page.</span></span>
2. <span data-ttu-id="f3a56-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f3a56-141">Close the page.</span></span>
3. <span data-ttu-id="f3a56-142">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="f3a56-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="f3a56-143">Valige puus väärtus Tšekkide mudel.</span><span class="sxs-lookup"><span data-stu-id="f3a56-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="f3a56-144">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="f3a56-144">Click Designer.</span></span>
6. <span data-ttu-id="f3a56-145">Klõpsake suvandit Mudeli vastendamine andmeallikaga.</span><span class="sxs-lookup"><span data-stu-id="f3a56-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="f3a56-146">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="f3a56-146">Click Designer.</span></span>
    * <span data-ttu-id="f3a56-147">Muudame andmemudeli allkirjaüksuse sidumist, et tuua allkirja pilt failist, mis on manustatud valitud pangakontoga seostatud tšeki paigutusekirjele.</span><span class="sxs-lookup"><span data-stu-id="f3a56-147">We will change the binding of the data model’s signature item to get the signature image from the file that has been attached to the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="f3a56-148">Lülitage säte Näita üksikasju välja.</span><span class="sxs-lookup"><span data-stu-id="f3a56-148">Turn Show details off.</span></span>
9. <span data-ttu-id="f3a56-149">Laiendage puus valik layout.</span><span class="sxs-lookup"><span data-stu-id="f3a56-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="f3a56-150">Laiendage puus valik „layout\signature“.</span><span class="sxs-lookup"><span data-stu-id="f3a56-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="f3a56-151">Valige puus „layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp“.</span><span class="sxs-lookup"><span data-stu-id="f3a56-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="f3a56-152">Laiendage puus valik chequesaccount.</span><span class="sxs-lookup"><span data-stu-id="f3a56-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="f3a56-153">Laiendage puus valikut „chequesaccount\<Relations“.</span><span class="sxs-lookup"><span data-stu-id="f3a56-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="f3a56-154">Laiendage puus valikut „chequesaccount\<Relations\BankChequeLayout“.</span><span class="sxs-lookup"><span data-stu-id="f3a56-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="f3a56-155">Laiendage puus valik „chequesaccount\<Relations\BankChequeLayout\<Relations“.</span><span class="sxs-lookup"><span data-stu-id="f3a56-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="f3a56-156">Laiendage puus valik „chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents“.</span><span class="sxs-lookup"><span data-stu-id="f3a56-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="f3a56-157">Valige puus „chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()“.</span><span class="sxs-lookup"><span data-stu-id="f3a56-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="f3a56-158">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="f3a56-158">Click Bind.</span></span>
19. <span data-ttu-id="f3a56-159">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f3a56-159">Click Save.</span></span>
20. <span data-ttu-id="f3a56-160">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f3a56-160">Close the page.</span></span>
21. <span data-ttu-id="f3a56-161">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f3a56-161">Close the page.</span></span>
22. <span data-ttu-id="f3a56-162">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f3a56-162">Close the page.</span></span>
23. <span data-ttu-id="f3a56-163">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f3a56-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="f3a56-164">Vormingu käivitamine kohandatud mudelivastendusega</span><span class="sxs-lookup"><span data-stu-id="f3a56-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="f3a56-165">Avage Sularaha- ja pangahaldus > Pangakontod > Pangakontod.</span><span class="sxs-lookup"><span data-stu-id="f3a56-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="f3a56-166">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="f3a56-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f3a56-167">Näiteks saate välja Pangakonto filtreerida väärtuse USMF OPER alusel.</span><span class="sxs-lookup"><span data-stu-id="f3a56-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="f3a56-168">Klõpsake tegumiribal valikut Seadistus.</span><span class="sxs-lookup"><span data-stu-id="f3a56-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="f3a56-169">Klõpsake nuppu Kontrolli.</span><span class="sxs-lookup"><span data-stu-id="f3a56-169">Click Check.</span></span>
5. <span data-ttu-id="f3a56-170">Klõpsake valikut Prindi test.</span><span class="sxs-lookup"><span data-stu-id="f3a56-170">Click Print test.</span></span>
6. <span data-ttu-id="f3a56-171">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f3a56-171">Click OK.</span></span>
    * <span data-ttu-id="f3a56-172">Vaadake loodud väljund üle.</span><span class="sxs-lookup"><span data-stu-id="f3a56-172">Review the created output.</span></span> <span data-ttu-id="f3a56-173">Pange tähele, et dokumendihalduse manusest pärit pilt on esitatud volitatud isiku allkirjana.</span><span class="sxs-lookup"><span data-stu-id="f3a56-173">Note that the image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="f3a56-174">MS Wordi dokumendi kasutamine imporditud vormingus mallina</span><span class="sxs-lookup"><span data-stu-id="f3a56-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="f3a56-175">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f3a56-175">Close the page.</span></span>
2. <span data-ttu-id="f3a56-176">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f3a56-176">Close the page.</span></span>
3. <span data-ttu-id="f3a56-177">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="f3a56-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="f3a56-178">Laiendage puus valik Tšekkide mudel.</span><span class="sxs-lookup"><span data-stu-id="f3a56-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="f3a56-179">Valige puus „Model for cheques\Cheques printing format“.</span><span class="sxs-lookup"><span data-stu-id="f3a56-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="f3a56-180">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="f3a56-180">Click Designer.</span></span>
7. <span data-ttu-id="f3a56-181">Klõpsake suvandit Manused.</span><span class="sxs-lookup"><span data-stu-id="f3a56-181">Click Attachments.</span></span>
8. <span data-ttu-id="f3a56-182">Klõpsake  Kustuta.</span><span class="sxs-lookup"><span data-stu-id="f3a56-182">Click Delete.</span></span>
9. <span data-ttu-id="f3a56-183">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="f3a56-183">Click Yes.</span></span>
10. <span data-ttu-id="f3a56-184">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f3a56-184">Click New.</span></span>
11. <span data-ttu-id="f3a56-185">Klõpsake suvandit Fail.</span><span class="sxs-lookup"><span data-stu-id="f3a56-185">Click File.</span></span>
    * <span data-ttu-id="f3a56-186">Klõpsake nuppu Sirvi ja valige eelnevalt allalaaditud fail „Cheque template Word.docx“.</span><span class="sxs-lookup"><span data-stu-id="f3a56-186">Click Browse and select the downloaded in advance ‘Cheque template Word.docx’ file.</span></span>  
12. <span data-ttu-id="f3a56-187">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f3a56-187">Close the page.</span></span>
13. <span data-ttu-id="f3a56-188">Sisestage või valige väärtus väljal Mall.</span><span class="sxs-lookup"><span data-stu-id="f3a56-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="f3a56-189">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f3a56-189">Click Save.</span></span>
15. <span data-ttu-id="f3a56-190">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f3a56-190">Close the page.</span></span>
16. <span data-ttu-id="f3a56-191">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="f3a56-191">Click Edit.</span></span>
17. <span data-ttu-id="f3a56-192">Tehke väljal Käivita mustand valik Jah.</span><span class="sxs-lookup"><span data-stu-id="f3a56-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="f3a56-193">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f3a56-193">Close the page.</span></span>
19. <span data-ttu-id="f3a56-194">Avage Sularaha- ja pangahaldus > Pangakontod > Pangakontod.</span><span class="sxs-lookup"><span data-stu-id="f3a56-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="f3a56-195">Kasutage kiirfiltrit, et filtrida välja Pangakonto väärtusega USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="f3a56-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="f3a56-196">Klõpsake nuppu Kontrolli.</span><span class="sxs-lookup"><span data-stu-id="f3a56-196">Click Check.</span></span>
22. <span data-ttu-id="f3a56-197">Klõpsake valikut Prindi test.</span><span class="sxs-lookup"><span data-stu-id="f3a56-197">Click Print test.</span></span>
23. <span data-ttu-id="f3a56-198">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f3a56-198">Click OK.</span></span>
    * <span data-ttu-id="f3a56-199">Vaadake loodud väljund üle.</span><span class="sxs-lookup"><span data-stu-id="f3a56-199">Review the created output.</span></span> <span data-ttu-id="f3a56-200">Võtke arvesse, et väljund on loodud manuspiltidega MS Wordi dokumendina, kus on ettevõtte logo, volitatud isiku allkiri ning vesimärgi jaoks valitud tekst.</span><span class="sxs-lookup"><span data-stu-id="f3a56-200">Note that the output has been generated as a MS Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  
