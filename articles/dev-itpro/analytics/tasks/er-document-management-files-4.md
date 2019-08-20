---
title: Vormingute käitamine dokumendihalduse failide kasutamiseks elektroonilise aruandluse väljundis
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse vormingu dokumendihalduse failide kasutamiseks elektroonilise aruandluse väljundis.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8dc541af4d26b61ff9b90e08a8ca2c6a6bb8e70
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850251"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4-run-format"></a><span data-ttu-id="bc4d9-103">Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (4. osa: vormingu käivitamine)</span><span class="sxs-lookup"><span data-stu-id="bc4d9-103">ER Use Document Management files in format outputs (Part 4: Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bc4d9-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="bc4d9-105">Neid toiminguid saab teha DEMF ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="bc4d9-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (3. osa: vormingu loomine).</span><span class="sxs-lookup"><span data-stu-id="bc4d9-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 3: Create format)” procedure.</span></span>

<span data-ttu-id="bc4d9-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="bc4d9-108">Vajalike manuste lisamine ühe arvega müügitellimusele</span><span class="sxs-lookup"><span data-stu-id="bc4d9-108">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="bc4d9-109">Avage Müügireskontro > Arved > Kliendiarvete avamine.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-109">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="bc4d9-110">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="bc4d9-111">Näiteks saate filtrida välja Arve alusel väärtusega CIV-000148.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-111">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="bc4d9-112">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="bc4d9-112">CIV-000148</span></span>  
3. <span data-ttu-id="bc4d9-113">Klõpsake valitud arve lingi järgimiseks.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-113">Click to follow the selected invoice’s link.</span></span>
    * <span data-ttu-id="bc4d9-114">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="bc4d9-114">CIV-000148</span></span>  
4. <span data-ttu-id="bc4d9-115">Klõpsake, et järgida linki väljal Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-115">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="bc4d9-116">000148</span><span class="sxs-lookup"><span data-stu-id="bc4d9-116">000148</span></span>  
5. <span data-ttu-id="bc4d9-117">Valige Päis väljalt Read või päis.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-117">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="bc4d9-118">Valige Päis, näitamaks, et see on manuste lisamise eesmärk.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-118">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="bc4d9-119">Klõpsake suvandit Manusta.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-119">Click Attach.</span></span>
    * <span data-ttu-id="bc4d9-120">Lisage sellele müügitellimusele manusena mõned failid.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-120">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="bc4d9-121">Kasutage faile, mille tüüpe dokumendihalduse moodul toetab (faililaiendid DOCX, DPF, XML, JPG jne).</span><span class="sxs-lookup"><span data-stu-id="bc4d9-121">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="bc4d9-122">Sirvige ja valige manustatavad failid, mida töödeldakse täiendavalt koos seotud arvega elektroonilise aruandluse elektroonilises sõnumis.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-122">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="bc4d9-123">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-123">Click New.</span></span>
8. <span data-ttu-id="bc4d9-124">Klõpsake suvandit Fail.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-124">Click File.</span></span>
9. <span data-ttu-id="bc4d9-125">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-125">Click New.</span></span>
10. <span data-ttu-id="bc4d9-126">Klõpsake suvandit Fail.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-126">Click File.</span></span>
11. <span data-ttu-id="bc4d9-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-127">Close the page.</span></span>
12. <span data-ttu-id="bc4d9-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-128">Close the page.</span></span>
13. <span data-ttu-id="bc4d9-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-129">Close the page.</span></span>
14. <span data-ttu-id="bc4d9-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-130">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="bc4d9-131">Käivitage valitud arvele koostatud aruanne</span><span class="sxs-lookup"><span data-stu-id="bc4d9-131">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="bc4d9-132">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-132">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="bc4d9-133">Laiendage puul valikut Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-133">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="bc4d9-134">Laiendage puul valikut Kliendiarve mudel \ Kliendiarve mudel (kohandatud).</span><span class="sxs-lookup"><span data-stu-id="bc4d9-134">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="bc4d9-135">Valige puult Kliendiarve mudel \ Kliendiarve mudel (kohandatud) \ Elektroonilise arve näidissõnum.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-135">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="bc4d9-136">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-136">Click Run.</span></span>
6. <span data-ttu-id="bc4d9-137">Jaotise () kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-137">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="bc4d9-138">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-138">Click Filter.</span></span>
8. <span data-ttu-id="bc4d9-139">Valige töölehe Kliendiarve ja välja Müügitellimus rida.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-139">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="bc4d9-140">Tippige väärtus 000148 väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-140">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="bc4d9-141">Tippige kriteeriumiväljale Müügitellimus tellimuse number 000148.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-141">In the criteria “Sales order” field, type the order number 000148.</span></span>  
10. <span data-ttu-id="bc4d9-142">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-142">Click OK.</span></span>
11. <span data-ttu-id="bc4d9-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-143">Click OK.</span></span>
    * <span data-ttu-id="bc4d9-144">Vaadake loodud väljundit.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-144">Review the generated output.</span></span> <span data-ttu-id="bc4d9-145">Pange tähele, et igale manusele on loodud üks XML-sõlm.</span><span class="sxs-lookup"><span data-stu-id="bc4d9-145">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="bc4d9-146">Manuse sisu lisatakse XML-väljundile tekstivormingus MIME (base64).</span><span class="sxs-lookup"><span data-stu-id="bc4d9-146">The attachment’s content is populated to the XML output in MIME (base64) text format.</span></span>  

