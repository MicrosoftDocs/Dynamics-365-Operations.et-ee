---
title: Elektrooniline aruandlus. Dokumendihalduse failide kasutamine vormingu väljundites (5. osa – vormingu muutmine ja käivitamine)
description: Selles teemas kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse (ER) vormingut kasutama ER-i väljundis dokumendihalduse faile (manused). (5. osa)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f96189163d5ecac47ade9f713b3fd689e41352d0
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092484"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="f2841-104">Elektrooniline aruandlus. Dokumendihalduse failide kasutamine vormingu väljundites (5. osa – vormingu muutmine ja käivitamine)</span><span class="sxs-lookup"><span data-stu-id="f2841-104">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2841-105">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.</span><span class="sxs-lookup"><span data-stu-id="f2841-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="f2841-106">Neid toiminguid saab teha DEMF ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="f2841-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="f2841-107">Nende etappide lõpule viimiseks peate esmalt viima lõpule etapid protseduuris „Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (4. osa: vormingu käivitamine)”.</span><span class="sxs-lookup"><span data-stu-id="f2841-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 4: Run format)" procedure.</span></span>

<span data-ttu-id="f2841-108">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="f2841-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="f2841-109">Muutke vormingut manuste lisamiseks, tekitades binaarvormingus sõnumid</span><span class="sxs-lookup"><span data-stu-id="f2841-109">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="f2841-110">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="f2841-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f2841-111">Laiendage puul valikut Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="f2841-111">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="f2841-112">Laiendage puul valikut Kliendiarve mudel \ Kliendiarve mudel (kohandatud).</span><span class="sxs-lookup"><span data-stu-id="f2841-112">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="f2841-113">Valige puult Kliendiarve mudel \ Kliendiarve mudel (kohandatud) \ Elektroonilise arve näidissõnum.</span><span class="sxs-lookup"><span data-stu-id="f2841-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="f2841-114">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="f2841-114">Click Designer.</span></span>
    * <span data-ttu-id="f2841-115">Arve sõnum lisatakse tekitatavasse väljundisse XML-failina, kasutades kodeeringut UNICODE.</span><span class="sxs-lookup"><span data-stu-id="f2841-115">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="f2841-116">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="f2841-116">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="f2841-117">Valige puul suvand Common\File.</span><span class="sxs-lookup"><span data-stu-id="f2841-117">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="f2841-118">Tippige väljale Nimi valik XML-sõnum.</span><span class="sxs-lookup"><span data-stu-id="f2841-118">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="f2841-119">XML-sõnum</span><span class="sxs-lookup"><span data-stu-id="f2841-119">Xml message</span></span>  
9. <span data-ttu-id="f2841-120">Sisestage väljale Kodeerimine suvand UTF-8.</span><span class="sxs-lookup"><span data-stu-id="f2841-120">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="f2841-121">UTF-8</span><span class="sxs-lookup"><span data-stu-id="f2841-121">UTF-8</span></span>  
10. <span data-ttu-id="f2841-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f2841-122">Click OK.</span></span>
    * <span data-ttu-id="f2841-123">Konfigureerige loodav väljund zip-failina.</span><span class="sxs-lookup"><span data-stu-id="f2841-123">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="f2841-124">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="f2841-124">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="f2841-125">Tehke puul valik Üldine \ Kaust.</span><span class="sxs-lookup"><span data-stu-id="f2841-125">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="f2841-126">Tippige väljale Nimi valik Zip-väljund.</span><span class="sxs-lookup"><span data-stu-id="f2841-126">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="f2841-127">Zip-väljund</span><span class="sxs-lookup"><span data-stu-id="f2841-127">Zip output</span></span>  
14. <span data-ttu-id="f2841-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f2841-128">Click OK.</span></span>
15. <span data-ttu-id="f2841-129">Valige puult Zip-väljund.</span><span class="sxs-lookup"><span data-stu-id="f2841-129">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="f2841-130">Lisage manused loodavale zip-failile algsete nimede ja laienditega failidena.</span><span class="sxs-lookup"><span data-stu-id="f2841-130">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="f2841-131">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="f2841-131">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="f2841-132">Valige puul suvand Common\File.</span><span class="sxs-lookup"><span data-stu-id="f2841-132">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="f2841-133">Tippige Manustatud fail väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f2841-133">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="f2841-134">Manustatud fail</span><span class="sxs-lookup"><span data-stu-id="f2841-134">Attached file</span></span>  
19. <span data-ttu-id="f2841-135">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f2841-135">Click OK.</span></span>
20. <span data-ttu-id="f2841-136">Valige puult Zip-väljund \ Manustatud fail.</span><span class="sxs-lookup"><span data-stu-id="f2841-136">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="f2841-137">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="f2841-137">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="f2841-138">Valige puul väärtus Tekst \ Base64.</span><span class="sxs-lookup"><span data-stu-id="f2841-138">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="f2841-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f2841-139">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="f2841-140">Uute vorminguelementide vastendamine andmemudeliga</span><span class="sxs-lookup"><span data-stu-id="f2841-140">Map new format elements to data model</span></span>
1. <span data-ttu-id="f2841-141">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="f2841-141">Click the Mapping tab.</span></span>
2. <span data-ttu-id="f2841-142">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="f2841-142">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="f2841-143">Laiendage puul valikut mudel \ Arve manused.</span><span class="sxs-lookup"><span data-stu-id="f2841-143">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="f2841-144">Valige puult Zip-väljund \ Manustatud fail \ Base64.</span><span class="sxs-lookup"><span data-stu-id="f2841-144">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="f2841-145">Valige puult mudel \ Arve manused \ Faili sisu.</span><span class="sxs-lookup"><span data-stu-id="f2841-145">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="f2841-146">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="f2841-146">Click Bind.</span></span>
7. <span data-ttu-id="f2841-147">Valige puult Zip-väljund \ Manustatud fail.</span><span class="sxs-lookup"><span data-stu-id="f2841-147">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="f2841-148">Klõpsake valikut Failinime redigeerimine.</span><span class="sxs-lookup"><span data-stu-id="f2841-148">Click Edit filename.</span></span>
9. <span data-ttu-id="f2841-149">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="f2841-149">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="f2841-150">Laiendage puul valikut mudel \ Arve manused.</span><span class="sxs-lookup"><span data-stu-id="f2841-150">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="f2841-151">Valige puult mudel \ Arve manused \ Faili nimi.</span><span class="sxs-lookup"><span data-stu-id="f2841-151">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="f2841-152">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="f2841-152">Click Add data source.</span></span>
13. <span data-ttu-id="f2841-153">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f2841-153">Click Save.</span></span>
14. <span data-ttu-id="f2841-154">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f2841-154">Close the page.</span></span>
15. <span data-ttu-id="f2841-155">Valige puult mudel \ Arve manused.</span><span class="sxs-lookup"><span data-stu-id="f2841-155">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="f2841-156">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="f2841-156">Click Bind.</span></span>
17. <span data-ttu-id="f2841-157">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f2841-157">Click Save.</span></span>
18. <span data-ttu-id="f2841-158">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f2841-158">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="f2841-159">Käivitage valitud arvele koostatud aruanne</span><span class="sxs-lookup"><span data-stu-id="f2841-159">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="f2841-160">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="f2841-160">Click Run.</span></span>
2. <span data-ttu-id="f2841-161">Jaotise () kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="f2841-161">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="f2841-162">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="f2841-162">Click Filter.</span></span>
4. <span data-ttu-id="f2841-163">Valige töölehe Kliendiarve ja välja Müügitellimus rida.</span><span class="sxs-lookup"><span data-stu-id="f2841-163">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="f2841-164">Tippige väljal Kriteerium väljale „Müügitellimus” tellimuse number 000148.</span><span class="sxs-lookup"><span data-stu-id="f2841-164">In the Criteria field, In the criteria "Sales order" field, type the order number 000148.</span></span>
    * <span data-ttu-id="f2841-165">000148</span><span class="sxs-lookup"><span data-stu-id="f2841-165">000148</span></span>  
6. <span data-ttu-id="f2841-166">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f2841-166">Click OK.</span></span>
7. <span data-ttu-id="f2841-167">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f2841-167">Click OK.</span></span>
    * <span data-ttu-id="f2841-168">Vaadake loodud väljundit.</span><span class="sxs-lookup"><span data-stu-id="f2841-168">Review the generated output.</span></span> <span data-ttu-id="f2841-169">Pange tähele, et lisaks XML-vormingus arve sõnumile on igale manusele loodud üks fail.</span><span class="sxs-lookup"><span data-stu-id="f2841-169">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="f2841-170">Manuse failidele lisatakse zip-väljund binaarvormingus.</span><span class="sxs-lookup"><span data-stu-id="f2841-170">The attachment files are populated with the zipped output in binary format.</span></span>  

