--- 
title: "Vormingu muutmine ja käivitamine dokumendihalduse failide vormingu väljundites kasutamiseks"
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis."
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
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
ms.openlocfilehash: 1c8a71c76b81991e88097c6d043e6ac50b5a3ad9
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="modify-and-run-format-to-use-document-management-files-in-format-outputs"></a><span data-ttu-id="0ac0a-103">Vormingu muutmine ja käivitamine dokumendihalduse failide vormingu väljundites kasutamiseks</span><span class="sxs-lookup"><span data-stu-id="0ac0a-103">Modify and run format to use Document Management files in format outputs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0ac0a-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="0ac0a-105">Neid toiminguid saab teha DEMF ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="0ac0a-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (4. osa: vormingu käivitamine).</span><span class="sxs-lookup"><span data-stu-id="0ac0a-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4): Run format” procedure.</span></span>

<span data-ttu-id="0ac0a-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="0ac0a-108">Muutke vormingut manuste lisamiseks, tekitades binaarvormingus sõnumid</span><span class="sxs-lookup"><span data-stu-id="0ac0a-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="0ac0a-109">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="0ac0a-110">Laiendage puul valikut Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="0ac0a-111">Laiendage puul valikut Kliendiarve mudel \ Kliendiarve mudel (kohandatud).</span><span class="sxs-lookup"><span data-stu-id="0ac0a-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="0ac0a-112">Valige puult Kliendiarve mudel \ Kliendiarve mudel (kohandatud) \ Elektroonilise arve näidissõnum.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="0ac0a-113">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-113">Click Designer.</span></span>
    * <span data-ttu-id="0ac0a-114">Arve sõnum lisatakse tekitatavasse väljundisse XML-failina, kasutades kodeeringut UNICODE.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="0ac0a-115">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="0ac0a-116">Valige puul suvand Common\File.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="0ac0a-117">Tippige väljale Nimi valik XML-sõnum.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="0ac0a-118">XML-sõnum</span><span class="sxs-lookup"><span data-stu-id="0ac0a-118">Xml message</span></span>  
9. <span data-ttu-id="0ac0a-119">Sisestage väljale Kodeerimine suvand UTF-8.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="0ac0a-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="0ac0a-120">UTF-8</span></span>  
10. <span data-ttu-id="0ac0a-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-121">Click OK.</span></span>
    * <span data-ttu-id="0ac0a-122">Konfigureerige loodav väljund zip-failina.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="0ac0a-123">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="0ac0a-124">Tehke puul valik Üldine \ Kaust.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="0ac0a-125">Tippige väljale Nimi valik Zip-väljund.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="0ac0a-126">Zip-väljund</span><span class="sxs-lookup"><span data-stu-id="0ac0a-126">Zip output</span></span>  
14. <span data-ttu-id="0ac0a-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-127">Click OK.</span></span>
15. <span data-ttu-id="0ac0a-128">Valige puult Zip-väljund.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="0ac0a-129">Lisage manused loodavale zip-failile algsete nimede ja laienditega failidena.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="0ac0a-130">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="0ac0a-131">Valige puul suvand Common\File.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="0ac0a-132">Tippige Manustatud fail väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="0ac0a-133">Manustatud fail</span><span class="sxs-lookup"><span data-stu-id="0ac0a-133">Attached file</span></span>  
19. <span data-ttu-id="0ac0a-134">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-134">Click OK.</span></span>
20. <span data-ttu-id="0ac0a-135">Valige puult Zip-väljund \ Manustatud fail.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="0ac0a-136">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="0ac0a-137">Valige puul väärtus Tekst \ Base64.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="0ac0a-138">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="0ac0a-139">Uute vorminguelementide vastendamine andmemudeliga</span><span class="sxs-lookup"><span data-stu-id="0ac0a-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="0ac0a-140">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="0ac0a-141">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="0ac0a-142">Laiendage puul valikut mudel \ Arve manused.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="0ac0a-143">Valige puult Zip-väljund \ Manustatud fail \ Base64.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="0ac0a-144">Valige puult mudel \ Arve manused \ Faili sisu.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="0ac0a-145">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-145">Click Bind.</span></span>
7. <span data-ttu-id="0ac0a-146">Valige puult Zip-väljund \ Manustatud fail.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="0ac0a-147">Klõpsake valikut Failinime redigeerimine.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-147">Click Edit filename.</span></span>
9. <span data-ttu-id="0ac0a-148">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="0ac0a-149">Laiendage puul valikut mudel \ Arve manused.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="0ac0a-150">Valige puult mudel \ Arve manused \ Faili nimi.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="0ac0a-151">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-151">Click Add data source.</span></span>
13. <span data-ttu-id="0ac0a-152">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-152">Click Save.</span></span>
14. <span data-ttu-id="0ac0a-153">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-153">Close the page.</span></span>
15. <span data-ttu-id="0ac0a-154">Valige puult mudel \ Arve manused.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="0ac0a-155">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-155">Click Bind.</span></span>
17. <span data-ttu-id="0ac0a-156">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-156">Click Save.</span></span>
18. <span data-ttu-id="0ac0a-157">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="0ac0a-158">Käivitage valitud arvele koostatud aruanne</span><span class="sxs-lookup"><span data-stu-id="0ac0a-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="0ac0a-159">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-159">Click Run.</span></span>
2. <span data-ttu-id="0ac0a-160">Jaotise () kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="0ac0a-161">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-161">Click Filter.</span></span>
4. <span data-ttu-id="0ac0a-162">Valige töölehe Kliendiarve ja välja Müügitellimus rida.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="0ac0a-163">Tippige väljal Kriteerium väljale Müügitellimus tellimuse number 000148.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="0ac0a-164">000148</span><span class="sxs-lookup"><span data-stu-id="0ac0a-164">000148</span></span>  
6. <span data-ttu-id="0ac0a-165">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-165">Click OK.</span></span>
7. <span data-ttu-id="0ac0a-166">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-166">Click OK.</span></span>
    * <span data-ttu-id="0ac0a-167">Vaadake loodud väljundit.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-167">Review the generated output.</span></span> <span data-ttu-id="0ac0a-168">Pange tähele, et lisaks XML-vormingus arve sõnumile on igale manusele loodud üks fail.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-168">Note, in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="0ac0a-169">Manuse failidele lisatakse zip-väljund binaarvormingus.</span><span class="sxs-lookup"><span data-stu-id="0ac0a-169">The attachment files are populated with the zipped output in binary format.</span></span>  


