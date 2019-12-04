---
title: Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (3. osa – vormingu loomine)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse vormingu dokumendihalduse failide kasutamiseks elektroonilise aruandluse väljundis.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 618fabc96bdfeb0c2b577aa686702d9f1257ed70
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550713"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="5396a-103">Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (3. osa – vormingu loomine)</span><span class="sxs-lookup"><span data-stu-id="5396a-103">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5396a-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.</span><span class="sxs-lookup"><span data-stu-id="5396a-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="5396a-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="5396a-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="5396a-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (2. osa: andmemudeli laiendamine).</span><span class="sxs-lookup"><span data-stu-id="5396a-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="5396a-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="5396a-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="5396a-108">Vormingu loomine arvete töötlemiseks</span><span class="sxs-lookup"><span data-stu-id="5396a-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="5396a-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="5396a-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="5396a-110">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="5396a-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="5396a-111">Laiendage puul valikut Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="5396a-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="5396a-112">Valige puult Kliendiarve mudel \ Kliendiarve mudel (kohandatud).</span><span class="sxs-lookup"><span data-stu-id="5396a-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="5396a-113">Saate luua vormi elektrooniliste sõnumite loomiseks teabega mis tahes failide kohta, mis on manustatud müügitellimusele, mis on seotud elektrooniliselt töödeldava arvega.</span><span class="sxs-lookup"><span data-stu-id="5396a-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="5396a-114">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="5396a-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="5396a-115">Sisestage väljale Uus valik Vorming põhineb andmemudelil Kliendiarve mudel (kohandatud).</span><span class="sxs-lookup"><span data-stu-id="5396a-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="5396a-116">Tippige väljale Nimi tekst Elektroonilise arve näidissõnum.</span><span class="sxs-lookup"><span data-stu-id="5396a-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="5396a-117">Elektroonilise arve näidissõnum</span><span class="sxs-lookup"><span data-stu-id="5396a-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="5396a-118">Sisestage või valige väärtus väljal Andmemudeli definitsioon.</span><span class="sxs-lookup"><span data-stu-id="5396a-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="5396a-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="5396a-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="5396a-120">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="5396a-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="5396a-121">Kujundage vorming manuste lisamiseks, tekitades MIME-vormingus sõnumi</span><span class="sxs-lookup"><span data-stu-id="5396a-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="5396a-122">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="5396a-122">Click Designer.</span></span>
2. <span data-ttu-id="5396a-123">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="5396a-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="5396a-124">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="5396a-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="5396a-125">Tippige Arve väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="5396a-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="5396a-126">Arve</span><span class="sxs-lookup"><span data-stu-id="5396a-126">Invoice</span></span>  
5. <span data-ttu-id="5396a-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5396a-127">Click OK.</span></span>
6. <span data-ttu-id="5396a-128">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="5396a-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="5396a-129">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="5396a-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="5396a-130">Tippige SalesOrder väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="5396a-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="5396a-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="5396a-131">SalesOrder</span></span>  
9. <span data-ttu-id="5396a-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5396a-132">Click OK.</span></span>
10. <span data-ttu-id="5396a-133">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="5396a-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="5396a-134">Tippige InvoiceNumber väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="5396a-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="5396a-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="5396a-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="5396a-136">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5396a-136">Click OK.</span></span>
13. <span data-ttu-id="5396a-137">Klõpsake valikut Lisa atribuut.</span><span class="sxs-lookup"><span data-stu-id="5396a-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="5396a-138">Tippige InvoiceAmount väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="5396a-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="5396a-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="5396a-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="5396a-140">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5396a-140">Click OK.</span></span>
16. <span data-ttu-id="5396a-141">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="5396a-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="5396a-142">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="5396a-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="5396a-143">Tippige EnclosedDocs väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="5396a-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="5396a-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="5396a-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="5396a-145">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5396a-145">Click OK.</span></span>
20. <span data-ttu-id="5396a-146">Valige puult Arve \ EnclosedDocs.</span><span class="sxs-lookup"><span data-stu-id="5396a-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="5396a-147">Klõpsake käsku Lisa element.</span><span class="sxs-lookup"><span data-stu-id="5396a-147">Click Add Element.</span></span>
22. <span data-ttu-id="5396a-148">Tippige Dokument väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="5396a-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="5396a-149">Dokument </span><span class="sxs-lookup"><span data-stu-id="5396a-149">Document</span></span>  
23. <span data-ttu-id="5396a-150">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5396a-150">Click OK.</span></span>
24. <span data-ttu-id="5396a-151">Valige puult Arve \ EnclosedDocs \ Dokument.</span><span class="sxs-lookup"><span data-stu-id="5396a-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="5396a-152">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="5396a-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="5396a-153">Valige puul suvand XML\Attribute.</span><span class="sxs-lookup"><span data-stu-id="5396a-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="5396a-154">Tippige FileName väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="5396a-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="5396a-155">FileName</span><span class="sxs-lookup"><span data-stu-id="5396a-155">FileName</span></span>  
28. <span data-ttu-id="5396a-156">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5396a-156">Click OK.</span></span>
29. <span data-ttu-id="5396a-157">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="5396a-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="5396a-158">Valige puul suvand XML\Element.</span><span class="sxs-lookup"><span data-stu-id="5396a-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="5396a-159">Tippige FileContent väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="5396a-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="5396a-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="5396a-160">FileContent</span></span>  
32. <span data-ttu-id="5396a-161">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5396a-161">Click OK.</span></span>
33. <span data-ttu-id="5396a-162">Valige puult Arve \ EnclosedDocs \ Dokument \ FileContent.</span><span class="sxs-lookup"><span data-stu-id="5396a-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="5396a-163">Klõpsake valikut Lisa rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="5396a-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="5396a-164">Valige puul väärtus Tekst \ Base64.</span><span class="sxs-lookup"><span data-stu-id="5396a-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="5396a-165">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5396a-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="5396a-166">Vorminguelementide vastendamine andmemudeliga andmeallikana</span><span class="sxs-lookup"><span data-stu-id="5396a-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="5396a-167">Valige puult Arve \ SalesOrder.</span><span class="sxs-lookup"><span data-stu-id="5396a-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="5396a-168">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="5396a-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="5396a-169">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="5396a-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="5396a-170">Valige puult mudel \ Müügitellimuse number (SalesId).</span><span class="sxs-lookup"><span data-stu-id="5396a-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="5396a-171">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="5396a-171">Click Bind.</span></span>
6. <span data-ttu-id="5396a-172">Valige puult Arve \ InvoiceNumber.</span><span class="sxs-lookup"><span data-stu-id="5396a-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="5396a-173">Laiendage puul valikut mudel \ Alusarve (InvoiceBase).</span><span class="sxs-lookup"><span data-stu-id="5396a-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="5396a-174">Valige puult mudel \ Alusarve (InvoiceBase) \ Arve number (Id).</span><span class="sxs-lookup"><span data-stu-id="5396a-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="5396a-175">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="5396a-175">Click Bind.</span></span>
10. <span data-ttu-id="5396a-176">Valige puult Arve \ InvoiceAmount.</span><span class="sxs-lookup"><span data-stu-id="5396a-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="5396a-177">Valige puult mudel \ Alusarve (InvoiceBase) \ Arve summa (summa).</span><span class="sxs-lookup"><span data-stu-id="5396a-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="5396a-178">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="5396a-178">Click Bind.</span></span>
13. <span data-ttu-id="5396a-179">Laiendage puul valikut mudel \ Arve manused.</span><span class="sxs-lookup"><span data-stu-id="5396a-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="5396a-180">Valige puult mudel \ Arve manused \ Faili sisu.</span><span class="sxs-lookup"><span data-stu-id="5396a-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="5396a-181">Valige puult Arve \ EnclosedDocs \ Dokument \ FileContent \Base64.</span><span class="sxs-lookup"><span data-stu-id="5396a-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="5396a-182">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="5396a-182">Click Bind.</span></span>
17. <span data-ttu-id="5396a-183">Valige puult mudel \ Arve manused \ Faili nimi.</span><span class="sxs-lookup"><span data-stu-id="5396a-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="5396a-184">Valige puult Arve \ EnclosedDocs \ Dokument \ FileName.</span><span class="sxs-lookup"><span data-stu-id="5396a-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="5396a-185">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="5396a-185">Click Bind.</span></span>
20. <span data-ttu-id="5396a-186">Valige puult mudel \ Arve manused.</span><span class="sxs-lookup"><span data-stu-id="5396a-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="5396a-187">Valige puult Arve \ EnclosedDocs \ Dokument.</span><span class="sxs-lookup"><span data-stu-id="5396a-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="5396a-188">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="5396a-188">Click Bind.</span></span>
23. <span data-ttu-id="5396a-189">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5396a-189">Click Save.</span></span>
24. <span data-ttu-id="5396a-190">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5396a-190">Close the page.</span></span>
