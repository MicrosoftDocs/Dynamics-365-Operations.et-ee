---
title: Konfiguratsioonide ülevaatamine aruannete loomiseks Office’i vormingus koos manuspiltidega
description: "Toimingute teostamiseks peab esmalt täitma juhendis „ER MS Office'i vormingutes manuspiltidega aruannete koostamine (1. osa: parameetrite häälestamine)” toodud toimingud."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c41ff1ba99411b97ea2b5d9f31bdee7c7701315
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684351"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="9a2b9-103">Konfiguratsioonide ülevaatamine aruannete loomiseks Office’i vormingus koos manuspiltidega</span><span class="sxs-lookup"><span data-stu-id="9a2b9-103">Review configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9a2b9-104">Toimingute teostamiseks peab esmalt täitma juhendis „ER MS Office'i vormingutes manuspiltidega aruannete koostamine (1. osa: parameetrite häälestamine)” toodud toimingud.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-104">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)" task guide.</span></span>

<span data-ttu-id="9a2b9-105">See toiming kirjeldab Microsoft Excelis ja Microsoft Wordis manuspilte sisaldavate elektrooniliste dokumentide loomiseks elektroonilise aruandluse (ER) konfiguratsioonide kujundamist.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-105">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="9a2b9-106">Selles näites vaatate üle näidisettevõtte Litware, Inc. jaoks loodud elektroonilise aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-106">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="9a2b9-107">Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="9a2b9-108">Need toimingud saab lõpule viia USMF-i andmekomplekti abil.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-108">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="9a2b9-109">Vaadake üle imporditud andmemudel</span><span class="sxs-lookup"><span data-stu-id="9a2b9-109">Review the imported data model</span></span>
1. <span data-ttu-id="9a2b9-110">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="9a2b9-111">Valige puus väärtus Tšekkide mudel.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-111">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="9a2b9-112">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-112">Click Designer.</span></span>
    * <span data-ttu-id="9a2b9-113">See mudel on ette nähtud maksetšekkide tähistamiseks ettevõtte seisukohast ja selle mudeli vastendamiseks rakenduse andmeallikatega.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-113">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application's data sources.</span></span> <span data-ttu-id="9a2b9-114">Vaadake see mudel üle ER-i operatsioonide kujundaja abil.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-114">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="9a2b9-115">Vaadake esitatud mudelielementide atribuute: struktuur, nimi, kirjeldus, andmetüüp jne.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-115">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="9a2b9-116">Laiendage puul valikut „root".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-116">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="9a2b9-117">Tehke puul valik „root\cheques".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-117">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="9a2b9-118">Laiendage puul valikut „root\cheques"</span><span class="sxs-lookup"><span data-stu-id="9a2b9-118">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="9a2b9-119">Laiendage puul valikut „root\cheques\attributes".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-119">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="9a2b9-120">Laiendage puul valikut „root\payer".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-120">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="9a2b9-121">Tehke puul valik „root\istestrun".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-121">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="9a2b9-122">Tehke puul valik „root\layout".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-122">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="9a2b9-123">Selle mudeli paigutuselement tähistab valitud pangakontoga seotud tšeki printimise vormi paigutuse üksikasju.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-123">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="9a2b9-124">See hõlmab piltide salvestamiseks ka kaht andmetüübi Konteiner sõlme.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-124">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="9a2b9-125">Laiendage puul valikut „root\layout".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-125">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="9a2b9-126">Tehke puul valik „root\layout\company logo".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-126">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="9a2b9-127">Laiendage puul valikut „root\layout\company logo".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-127">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="9a2b9-128">Tehke puul valik „root\layout\company logo\image".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-128">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="9a2b9-129">Tehke puul valik „root\layout\company logo\isprinted".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-129">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="9a2b9-130">Tehke puul valik „root\layout\signature"</span><span class="sxs-lookup"><span data-stu-id="9a2b9-130">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="9a2b9-131">Laiendage puul valikut „root\layout\signature".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-131">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="9a2b9-132">Tehke puul valik „root\layout\signature\image".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-132">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="9a2b9-133">Tehke puul valik „root\layout\signature\isprinted".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-133">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="9a2b9-134">Pange tähele, et kaks pildi andmemudeli elementi on seotud nende tabelite väljadega, mis sisaldavad binaarvormingus ettevõtte logo ja volitatud isiku allkirja.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-134">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person's signature in binary format.</span></span>  
20. <span data-ttu-id="9a2b9-135">Laiendage puul valikut „root\layout\watermark".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-135">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="9a2b9-136">Klõpsake suvandit Mudeli vastendamine andmeallikaga.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-136">Click Map model to datasource.</span></span>
22. <span data-ttu-id="9a2b9-137">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-137">Click Designer.</span></span>
23. <span data-ttu-id="9a2b9-138">Laiendage puul valikut „chequesselected".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-138">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="9a2b9-139">Laiendage puus valik layout.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-139">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="9a2b9-140">Laiendage puul valikut „layout\company logo".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-140">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="9a2b9-141">Laiendage puus valik „layout\signature“.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-141">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="9a2b9-142">Laiendage puul valikut „layout\watermark".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-142">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="9a2b9-143">Lülitage nupp Kuva üksikasjad sisse.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-143">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="9a2b9-144">Pange tähele, et tšekkide andmemudeli element on seotud tabeliga TmpChequePrintout, mis sisaldab käitusajal nende tšekkide kirjeid, mille kasutaja on valinud printimiseks.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-144">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="9a2b9-145">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-145">Close the page.</span></span>
30. <span data-ttu-id="9a2b9-146">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-146">Close the page.</span></span>
31. <span data-ttu-id="9a2b9-147">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-147">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="9a2b9-148">Vaadake üle imporditud vorming</span><span class="sxs-lookup"><span data-stu-id="9a2b9-148">Review the imported format</span></span>
1. <span data-ttu-id="9a2b9-149">Laiendage puus valik Tšekkide mudel.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-149">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="9a2b9-150">Valige puus „Model for cheques\Cheques printing format“.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-150">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="9a2b9-151">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-151">Click Designer.</span></span>
4. <span data-ttu-id="9a2b9-152">Klõpsake suvandit Manused.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-152">Click Attachments.</span></span>
5. <span data-ttu-id="9a2b9-153">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-153">Click Open.</span></span>
    * <span data-ttu-id="9a2b9-154">Avage manustatud aruande mall Excelis.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-154">Open the attached report's template in Excel.</span></span>  
    * <span data-ttu-id="9a2b9-155">Vaadake läbi manustatud aruande Exceli mall, mida kasutatakse tšekkide printimiseks.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-155">Review the attached report's Excel template that will be used to print cheques.</span></span> <span data-ttu-id="9a2b9-156">Mall sisaldab kaht tšekki lehe kohta ja see on mõeldud tšekkide printimiseks eelprinditud vormile.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-156">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="9a2b9-157">Võtke arvesse, et kaks tühja pilti on manustatud.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-157">Note that two blank images are embedded.</span></span> <span data-ttu-id="9a2b9-158">Tühjad pildid on ette nähtud ettevõtte logo ja makse autoriseerija allkirja jaoks.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-158">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="9a2b9-159">Veenduge, et piltidel on Excelis vastavalt nimed CompLogo ja SignatureImage.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-159">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="9a2b9-160">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-160">Close the page.</span></span>
7. <span data-ttu-id="9a2b9-161">Laiendage puul valikut „Report".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-161">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="9a2b9-162">Laiendage puul valikut „Report\ChequeLines".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-162">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="9a2b9-163">Tehke puul valik „Report\ChequeLines\CompLogo".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-163">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="9a2b9-164">Lülitage nupp Kuva üksikasjad sisse.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-164">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="9a2b9-165">Pange tähele, et pildi „CompLogo” vormingu lahtrielement tähistab Exceli üksust, mille abil täidetakse aruandes ettevõtte logo pilt.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-165">Note that the 'CompLogo' format's cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="9a2b9-166">See vorming on seotud pildi andmemudeli elemendiga, mis sisaldab käitusajal ettevõtte logo binaarvormingus pilti.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-166">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="9a2b9-167">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-167">Click the Mapping tab.</span></span>
12. <span data-ttu-id="9a2b9-168">Klõpsake valikut Redigeerimine on lubatud.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-168">Click Edit enabled.</span></span>
    * <span data-ttu-id="9a2b9-169">Pange tähele, et saate luua „CompLogo" vormingu lahtrielemendi sel viisil, et see pole enam lubatud.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-169">Note that you can make the 'CompLogo' format's cell element so that it's no longer enabled.</span></span> <span data-ttu-id="9a2b9-170">Sel juhul peidab Exceli seotud pildielement loodud aruandes ettevõtte logo.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-170">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="9a2b9-171">Kui lubatud avaldis tagastab väärtuse TRUE ja määratletud seos ei kuva pilti, kuvab Exceli seotud pildielement Exceli malli salvestatud pilti.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-171">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="9a2b9-172">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-172">Close the page.</span></span>
14. <span data-ttu-id="9a2b9-173">Laiendage puul valikut „labels: Container".</span><span class="sxs-lookup"><span data-stu-id="9a2b9-173">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="9a2b9-174">Mõned eelprinditud tšekivormidel olevad sildid kaasatakse aruandesse selle testimise eesmärgil loomisel.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-174">Some labels that are presented in the preprinted cheque form will be included in the report when it's created for testing purposes.</span></span> <span data-ttu-id="9a2b9-175">Neid silte aga ei prindita reaalse printimise ajal, kuna eelprinditud vorm juba sisaldab neid.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-175">However, those labels won't be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="9a2b9-176">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9a2b9-176">Close the page.</span></span>

