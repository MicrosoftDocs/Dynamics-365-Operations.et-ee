---
title: Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (3. osa – vormingu loomine)
description: Selles teemas kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse vormingut kasutama ER-i väljundis dokumendihalduse faile. (3. osa)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 432cf4c41a7a223ab07b02edf6da7eac9965cff0
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092612"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="c7596-104">Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (3. osa – vormingu loomine)</span><span class="sxs-lookup"><span data-stu-id="c7596-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c7596-105">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.</span><span class="sxs-lookup"><span data-stu-id="c7596-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="c7596-106">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="c7596-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="c7596-107">Nende etappide lõpule viimiseks peate esmalt viima lõpule etapid protseduuris „Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (2. osa: andmemudeli laiendamine)”.</span><span class="sxs-lookup"><span data-stu-id="c7596-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="c7596-108">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="c7596-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="c7596-109">Vormingu loomine arvete töötlemiseks</span><span class="sxs-lookup"><span data-stu-id="c7596-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="c7596-110">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="c7596-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c7596-111">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="c7596-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="c7596-112">Laiendage puul valikut Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="c7596-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="c7596-113">Valige puult Kliendiarve mudel \ Kliendiarve mudel (kohandatud).</span><span class="sxs-lookup"><span data-stu-id="c7596-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="c7596-114">Saate luua vormi elektrooniliste sõnumite loomiseks teabega mis tahes failide kohta, mis on manustatud müügitellimusele, mis on seotud elektrooniliselt töödeldava arvega.</span><span class="sxs-lookup"><span data-stu-id="c7596-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="c7596-115">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="c7596-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="c7596-116">Sisestage väljale Uus valik Vorming põhineb andmemudelil Kliendiarve mudel (kohandatud).</span><span class="sxs-lookup"><span data-stu-id="c7596-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="c7596-117">Tippige väljale Nimi tekst Elektroonilise arve näidissõnum.</span><span class="sxs-lookup"><span data-stu-id="c7596-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="c7596-118">Elektroonilise arve näidissõnum</span><span class="sxs-lookup"><span data-stu-id="c7596-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="c7596-119">Sisestage või valige väärtus väljal Andmemudeli definitsioon.</span><span class="sxs-lookup"><span data-stu-id="c7596-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="c7596-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="c7596-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="c7596-121">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="c7596-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="c7596-122">Kujundage vorming manuste lisamiseks, tekitades MIME-vormingus sõnumi</span><span class="sxs-lookup"><span data-stu-id="c7596-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="c7596-123">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="c7596-123">Click Designer.</span></span>
2. <span data-ttu-id="c7596-124">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="c7596-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="c7596-125">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="c7596-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="c7596-126">Tippige Arve väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="c7596-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="c7596-127">Arve</span><span class="sxs-lookup"><span data-stu-id="c7596-127">Invoice</span></span>  
5. <span data-ttu-id="c7596-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c7596-128">Click OK.</span></span>
6. <span data-ttu-id="c7596-129">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="c7596-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="c7596-130">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="c7596-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="c7596-131">Tippige SalesOrder väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="c7596-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="c7596-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="c7596-132">SalesOrder</span></span>  
9. <span data-ttu-id="c7596-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c7596-133">Click OK.</span></span>
10. <span data-ttu-id="c7596-134">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="c7596-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="c7596-135">Tippige InvoiceNumber väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="c7596-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="c7596-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="c7596-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="c7596-137">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c7596-137">Click OK.</span></span>
13. <span data-ttu-id="c7596-138">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="c7596-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="c7596-139">Tippige InvoiceAmount väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="c7596-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="c7596-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="c7596-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="c7596-141">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c7596-141">Click OK.</span></span>
16. <span data-ttu-id="c7596-142">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="c7596-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="c7596-143">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="c7596-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="c7596-144">Tippige EnclosedDocs väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="c7596-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="c7596-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="c7596-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="c7596-146">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c7596-146">Click OK.</span></span>
20. <span data-ttu-id="c7596-147">Valige puult Arve \ EnclosedDocs.</span><span class="sxs-lookup"><span data-stu-id="c7596-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="c7596-148">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="c7596-148">Click Add Element.</span></span>
22. <span data-ttu-id="c7596-149">Tippige Dokument väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="c7596-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="c7596-150">Dokument </span><span class="sxs-lookup"><span data-stu-id="c7596-150">Document</span></span>  
23. <span data-ttu-id="c7596-151">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c7596-151">Click OK.</span></span>
24. <span data-ttu-id="c7596-152">Valige puult Arve \ EnclosedDocs \ Dokument.</span><span class="sxs-lookup"><span data-stu-id="c7596-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="c7596-153">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="c7596-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="c7596-154">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="c7596-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="c7596-155">Tippige FileName väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="c7596-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="c7596-156">FileName</span><span class="sxs-lookup"><span data-stu-id="c7596-156">FileName</span></span>  
28. <span data-ttu-id="c7596-157">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c7596-157">Click OK.</span></span>
29. <span data-ttu-id="c7596-158">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="c7596-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="c7596-159">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="c7596-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="c7596-160">Tippige FileContent väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="c7596-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="c7596-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="c7596-161">FileContent</span></span>  
32. <span data-ttu-id="c7596-162">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c7596-162">Click OK.</span></span>
33. <span data-ttu-id="c7596-163">Valige puult Arve \ EnclosedDocs \ Dokument \ FileContent.</span><span class="sxs-lookup"><span data-stu-id="c7596-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="c7596-164">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="c7596-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="c7596-165">Valige puul väärtus Tekst \ Base64.</span><span class="sxs-lookup"><span data-stu-id="c7596-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="c7596-166">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c7596-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="c7596-167">Vorminguelementide vastendamine andmemudeliga andmeallikana</span><span class="sxs-lookup"><span data-stu-id="c7596-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="c7596-168">Valige puult Arve \ SalesOrder.</span><span class="sxs-lookup"><span data-stu-id="c7596-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="c7596-169">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="c7596-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="c7596-170">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="c7596-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="c7596-171">Valige puult mudel \ Müügitellimuse number (SalesId).</span><span class="sxs-lookup"><span data-stu-id="c7596-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="c7596-172">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="c7596-172">Click Bind.</span></span>
6. <span data-ttu-id="c7596-173">Valige puult Arve \ InvoiceNumber.</span><span class="sxs-lookup"><span data-stu-id="c7596-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="c7596-174">Laiendage puul valikut mudel \ Alusarve (InvoiceBase).</span><span class="sxs-lookup"><span data-stu-id="c7596-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="c7596-175">Valige puult mudel \ Alusarve (InvoiceBase) \ Arve number (Id).</span><span class="sxs-lookup"><span data-stu-id="c7596-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="c7596-176">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="c7596-176">Click Bind.</span></span>
10. <span data-ttu-id="c7596-177">Valige puult Arve \ InvoiceAmount.</span><span class="sxs-lookup"><span data-stu-id="c7596-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="c7596-178">Valige puult mudel \ Alusarve (InvoiceBase) \ Arve summa (summa).</span><span class="sxs-lookup"><span data-stu-id="c7596-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="c7596-179">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="c7596-179">Click Bind.</span></span>
13. <span data-ttu-id="c7596-180">Laiendage puul valikut mudel \ Arve manused.</span><span class="sxs-lookup"><span data-stu-id="c7596-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="c7596-181">Valige puult mudel \ Arve manused \ Faili sisu.</span><span class="sxs-lookup"><span data-stu-id="c7596-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="c7596-182">Valige puult Arve \ EnclosedDocs \ Dokument \ FileContent \Base64.</span><span class="sxs-lookup"><span data-stu-id="c7596-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="c7596-183">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="c7596-183">Click Bind.</span></span>
17. <span data-ttu-id="c7596-184">Valige puult mudel \ Arve manused \ Faili nimi.</span><span class="sxs-lookup"><span data-stu-id="c7596-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="c7596-185">Valige puult Arve \ EnclosedDocs \ Dokument \ FileName.</span><span class="sxs-lookup"><span data-stu-id="c7596-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="c7596-186">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="c7596-186">Click Bind.</span></span>
20. <span data-ttu-id="c7596-187">Valige puult mudel \ Arve manused.</span><span class="sxs-lookup"><span data-stu-id="c7596-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="c7596-188">Valige puult Arve \ EnclosedDocs \ Dokument.</span><span class="sxs-lookup"><span data-stu-id="c7596-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="c7596-189">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="c7596-189">Click Bind.</span></span>
23. <span data-ttu-id="c7596-190">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="c7596-190">Click Save.</span></span>
24. <span data-ttu-id="c7596-191">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c7596-191">Close the page.</span></span>

