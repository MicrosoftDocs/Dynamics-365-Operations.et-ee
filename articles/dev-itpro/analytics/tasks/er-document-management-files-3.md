--- 
title: "Vormingute loomine dokumendihalduse failide kasutamiseks elektroonilise aruandluse väljundis"
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.openlocfilehash: 934775bbdda13238e16fba91dcb90d6d3249e812
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---
# <a name="create-formats-to-use-document-management-files-in-er-output"></a><span data-ttu-id="12faf-103">Vormingute loomine dokumendihalduse failide kasutamiseks elektroonilise aruandluse väljundis</span><span class="sxs-lookup"><span data-stu-id="12faf-103">Create formats to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="12faf-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.</span><span class="sxs-lookup"><span data-stu-id="12faf-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="12faf-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="12faf-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="12faf-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (2. osa: andmemudeli laiendamine).</span><span class="sxs-lookup"><span data-stu-id="12faf-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="12faf-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="12faf-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="12faf-108">Vormingu loomine arvete töötlemiseks</span><span class="sxs-lookup"><span data-stu-id="12faf-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="12faf-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="12faf-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="12faf-110">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="12faf-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="12faf-111">Laiendage puul valikut Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="12faf-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="12faf-112">Valige puult Kliendiarve mudel \ Kliendiarve mudel (kohandatud).</span><span class="sxs-lookup"><span data-stu-id="12faf-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="12faf-113">Saate luua vormi elektrooniliste sõnumite loomiseks teabega mis tahes failide kohta, mis on manustatud müügitellimusele, mis on seotud elektrooniliselt töödeldava arvega.</span><span class="sxs-lookup"><span data-stu-id="12faf-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="12faf-114">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="12faf-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="12faf-115">Sisestage väljale Uus valik Vorming põhineb andmemudelil Kliendiarve mudel (kohandatud).</span><span class="sxs-lookup"><span data-stu-id="12faf-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="12faf-116">Tippige väljale Nimi tekst Elektroonilise arve näidissõnum.</span><span class="sxs-lookup"><span data-stu-id="12faf-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="12faf-117">Elektroonilise arve näidissõnum</span><span class="sxs-lookup"><span data-stu-id="12faf-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="12faf-118">Sisestage või valige väärtus väljal Andmemudeli definitsioon.</span><span class="sxs-lookup"><span data-stu-id="12faf-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="12faf-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="12faf-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="12faf-120">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="12faf-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="12faf-121">Kujundage vorming manuste lisamiseks, tekitades MIME-vormingus sõnumi</span><span class="sxs-lookup"><span data-stu-id="12faf-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="12faf-122">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="12faf-122">Click Designer.</span></span>
2. <span data-ttu-id="12faf-123">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="12faf-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="12faf-124">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="12faf-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="12faf-125">Tippige Arve väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="12faf-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="12faf-126">Arve</span><span class="sxs-lookup"><span data-stu-id="12faf-126">Invoice</span></span>  
5. <span data-ttu-id="12faf-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="12faf-127">Click OK.</span></span>
6. <span data-ttu-id="12faf-128">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="12faf-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="12faf-129">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="12faf-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="12faf-130">Tippige SalesOrder väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="12faf-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="12faf-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="12faf-131">SalesOrder</span></span>  
9. <span data-ttu-id="12faf-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="12faf-132">Click OK.</span></span>
10. <span data-ttu-id="12faf-133">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="12faf-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="12faf-134">Tippige InvoiceNumber väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="12faf-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="12faf-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="12faf-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="12faf-136">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="12faf-136">Click OK.</span></span>
13. <span data-ttu-id="12faf-137">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="12faf-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="12faf-138">Tippige InvoiceAmount väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="12faf-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="12faf-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="12faf-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="12faf-140">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="12faf-140">Click OK.</span></span>
16. <span data-ttu-id="12faf-141">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="12faf-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="12faf-142">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="12faf-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="12faf-143">Tippige EnclosedDocs väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="12faf-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="12faf-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="12faf-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="12faf-145">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="12faf-145">Click OK.</span></span>
20. <span data-ttu-id="12faf-146">Valige puult Arve \ EnclosedDocs.</span><span class="sxs-lookup"><span data-stu-id="12faf-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="12faf-147">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="12faf-147">Click Add Element.</span></span>
22. <span data-ttu-id="12faf-148">Tippige Dokument väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="12faf-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="12faf-149">Dokument </span><span class="sxs-lookup"><span data-stu-id="12faf-149">Document</span></span>  
23. <span data-ttu-id="12faf-150">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="12faf-150">Click OK.</span></span>
24. <span data-ttu-id="12faf-151">Valige puult Arve \ EnclosedDocs \ Dokument.</span><span class="sxs-lookup"><span data-stu-id="12faf-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="12faf-152">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="12faf-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="12faf-153">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="12faf-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="12faf-154">Tippige FileName väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="12faf-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="12faf-155">FileName</span><span class="sxs-lookup"><span data-stu-id="12faf-155">FileName</span></span>  
28. <span data-ttu-id="12faf-156">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="12faf-156">Click OK.</span></span>
29. <span data-ttu-id="12faf-157">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="12faf-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="12faf-158">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="12faf-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="12faf-159">Tippige FileContent väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="12faf-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="12faf-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="12faf-160">FileContent</span></span>  
32. <span data-ttu-id="12faf-161">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="12faf-161">Click OK.</span></span>
33. <span data-ttu-id="12faf-162">Valige puult Arve \ EnclosedDocs \ Dokument \ FileContent.</span><span class="sxs-lookup"><span data-stu-id="12faf-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="12faf-163">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="12faf-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="12faf-164">Valige puul väärtus Tekst \ Base64.</span><span class="sxs-lookup"><span data-stu-id="12faf-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="12faf-165">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="12faf-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="12faf-166">Vorminguelementide vastendamine andmemudeliga andmeallikana</span><span class="sxs-lookup"><span data-stu-id="12faf-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="12faf-167">Valige puult Arve \ SalesOrder.</span><span class="sxs-lookup"><span data-stu-id="12faf-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="12faf-168">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="12faf-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="12faf-169">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="12faf-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="12faf-170">Valige puult mudel \ Müügitellimuse number (SalesId).</span><span class="sxs-lookup"><span data-stu-id="12faf-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="12faf-171">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="12faf-171">Click Bind.</span></span>
6. <span data-ttu-id="12faf-172">Valige puult Arve \ InvoiceNumber.</span><span class="sxs-lookup"><span data-stu-id="12faf-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="12faf-173">Laiendage puul valikut mudel \ Alusarve (InvoiceBase).</span><span class="sxs-lookup"><span data-stu-id="12faf-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="12faf-174">Valige puult mudel \ Alusarve (InvoiceBase) \ Arve number (Id).</span><span class="sxs-lookup"><span data-stu-id="12faf-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="12faf-175">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="12faf-175">Click Bind.</span></span>
10. <span data-ttu-id="12faf-176">Valige puult Arve \ InvoiceAmount.</span><span class="sxs-lookup"><span data-stu-id="12faf-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="12faf-177">Valige puult mudel \ Alusarve (InvoiceBase) \ Arve summa (summa).</span><span class="sxs-lookup"><span data-stu-id="12faf-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="12faf-178">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="12faf-178">Click Bind.</span></span>
13. <span data-ttu-id="12faf-179">Laiendage puul valikut mudel \ Arve manused.</span><span class="sxs-lookup"><span data-stu-id="12faf-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="12faf-180">Valige puult mudel \ Arve manused \ Faili sisu.</span><span class="sxs-lookup"><span data-stu-id="12faf-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="12faf-181">Valige puult Arve \ EnclosedDocs \ Dokument \ FileContent \Base64.</span><span class="sxs-lookup"><span data-stu-id="12faf-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="12faf-182">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="12faf-182">Click Bind.</span></span>
17. <span data-ttu-id="12faf-183">Valige puult mudel \ Arve manused \ Faili nimi.</span><span class="sxs-lookup"><span data-stu-id="12faf-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="12faf-184">Valige puult Arve \ EnclosedDocs \ Dokument \ FileName.</span><span class="sxs-lookup"><span data-stu-id="12faf-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="12faf-185">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="12faf-185">Click Bind.</span></span>
20. <span data-ttu-id="12faf-186">Valige puult mudel \ Arve manused.</span><span class="sxs-lookup"><span data-stu-id="12faf-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="12faf-187">Valige puult Arve \ EnclosedDocs \ Dokument.</span><span class="sxs-lookup"><span data-stu-id="12faf-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="12faf-188">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="12faf-188">Click Bind.</span></span>
23. <span data-ttu-id="12faf-189">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="12faf-189">Click Save.</span></span>
24. <span data-ttu-id="12faf-190">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="12faf-190">Close the page.</span></span>


