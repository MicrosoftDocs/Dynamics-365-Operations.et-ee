---
title: Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (4. osa – vormingu käivitamine)
description: Selles teemas kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse vormingut kasutama ER-i väljundis dokumendihalduse faile. (4. osa)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7a7c9705d8b53ef13cd3faf13290f3f1b1d1c43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749113"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="da328-104">Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (4. osa – vormingu käivitamine)</span><span class="sxs-lookup"><span data-stu-id="da328-104">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da328-105">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.</span><span class="sxs-lookup"><span data-stu-id="da328-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="da328-106">Neid toiminguid saab teha DEMF ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="da328-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="da328-107">Nende etappide lõpule viimiseks peate esmalt viima lõule etapid protseduuris „Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (3. osa: vormingu loomine)”.</span><span class="sxs-lookup"><span data-stu-id="da328-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="da328-108">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="da328-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="da328-109">Vajalike manuste lisamine ühe arvega müügitellimusele</span><span class="sxs-lookup"><span data-stu-id="da328-109">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="da328-110">Avage Müügireskontro > Arved > Kliendiarvete avamine.</span><span class="sxs-lookup"><span data-stu-id="da328-110">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="da328-111">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="da328-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="da328-112">Näiteks saate filtrida välja Arve alusel väärtusega CIV-000148.</span><span class="sxs-lookup"><span data-stu-id="da328-112">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="da328-113">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="da328-113">CIV-000148</span></span>  
3. <span data-ttu-id="da328-114">Klõpsake valitud arve lingi järgimiseks.</span><span class="sxs-lookup"><span data-stu-id="da328-114">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="da328-115">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="da328-115">CIV-000148</span></span>  
4. <span data-ttu-id="da328-116">Klõpsake, et järgida linki väljal Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="da328-116">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="da328-117">000148</span><span class="sxs-lookup"><span data-stu-id="da328-117">000148</span></span>  
5. <span data-ttu-id="da328-118">Valige Päis väljalt Read või päis.</span><span class="sxs-lookup"><span data-stu-id="da328-118">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="da328-119">Valige Päis, näitamaks, et see on manuste lisamise eesmärk.</span><span class="sxs-lookup"><span data-stu-id="da328-119">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="da328-120">Klõpsake suvandit Manusta.</span><span class="sxs-lookup"><span data-stu-id="da328-120">Click Attach.</span></span>
    * <span data-ttu-id="da328-121">Lisage sellele müügitellimusele manusena mõned failid.</span><span class="sxs-lookup"><span data-stu-id="da328-121">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="da328-122">Kasutage faile, mille tüüpe dokumendihalduse moodul toetab (faililaiendid DOCX, DPF, XML, JPG jne).</span><span class="sxs-lookup"><span data-stu-id="da328-122">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="da328-123">Sirvige ja valige manustatavad failid, mida töödeldakse täiendavalt koos seotud arvega elektroonilise aruandluse elektroonilises sõnumis.</span><span class="sxs-lookup"><span data-stu-id="da328-123">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="da328-124">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="da328-124">Click New.</span></span>
8. <span data-ttu-id="da328-125">Klõpsake suvandit Fail.</span><span class="sxs-lookup"><span data-stu-id="da328-125">Click File.</span></span>
9. <span data-ttu-id="da328-126">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="da328-126">Click New.</span></span>
10. <span data-ttu-id="da328-127">Klõpsake suvandit Fail.</span><span class="sxs-lookup"><span data-stu-id="da328-127">Click File.</span></span>
11. <span data-ttu-id="da328-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da328-128">Close the page.</span></span>
12. <span data-ttu-id="da328-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da328-129">Close the page.</span></span>
13. <span data-ttu-id="da328-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da328-130">Close the page.</span></span>
14. <span data-ttu-id="da328-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da328-131">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="da328-132">Käivitage valitud arvele koostatud aruanne</span><span class="sxs-lookup"><span data-stu-id="da328-132">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="da328-133">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="da328-133">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="da328-134">Laiendage puul valikut Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="da328-134">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="da328-135">Laiendage puul valikut Kliendiarve mudel \ Kliendiarve mudel (kohandatud).</span><span class="sxs-lookup"><span data-stu-id="da328-135">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="da328-136">Valige puult Kliendiarve mudel \ Kliendiarve mudel (kohandatud) \ Elektroonilise arve näidissõnum.</span><span class="sxs-lookup"><span data-stu-id="da328-136">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="da328-137">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="da328-137">Click Run.</span></span>
6. <span data-ttu-id="da328-138">Jaotise () kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="da328-138">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="da328-139">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="da328-139">Click Filter.</span></span>
8. <span data-ttu-id="da328-140">Valige töölehe Kliendiarve ja välja Müügitellimus rida.</span><span class="sxs-lookup"><span data-stu-id="da328-140">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="da328-141">Tippige väärtus 000148 väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="da328-141">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="da328-142">Tippige kriteeriumiväljale „Müügitellimus” tellimuse number 000148.</span><span class="sxs-lookup"><span data-stu-id="da328-142">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="da328-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="da328-143">Click OK.</span></span>
11. <span data-ttu-id="da328-144">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="da328-144">Click OK.</span></span>
    * <span data-ttu-id="da328-145">Vaadake loodud väljundit.</span><span class="sxs-lookup"><span data-stu-id="da328-145">Review the generated output.</span></span> <span data-ttu-id="da328-146">Pange tähele, et igale manusele on loodud üks XML-sõlm.</span><span class="sxs-lookup"><span data-stu-id="da328-146">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="da328-147">Manuse sisu lisatakse XML-väljundile tekstivormingus MIME (base64).</span><span class="sxs-lookup"><span data-stu-id="da328-147">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]