---
title: Elektrooniline aruandlus. Dokumendihalduse failide kasutamine vormingu väljundites (2. osa – andmemudeli laiendamine)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 032f9c5707294ee33cc848ecc6990c1ef5bbfdbb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185033"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2-extend-data-model"></a><span data-ttu-id="9789c-103">Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (2. osa: andmemudeli laiendamine)</span><span class="sxs-lookup"><span data-stu-id="9789c-103">ER Use Document Management files in format outputs (Part 2: Extend data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9789c-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.</span><span class="sxs-lookup"><span data-stu-id="9789c-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="9789c-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="9789c-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="9789c-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid tegevuse juhendis Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (1. osa: andmemudeli ettevalmistamine).</span><span class="sxs-lookup"><span data-stu-id="9789c-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="9789c-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="9789c-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="9789c-108">Laiendage andmemudelit, et esitada selles dokumendihalduse faile</span><span class="sxs-lookup"><span data-stu-id="9789c-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="9789c-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="9789c-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="9789c-110">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="9789c-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="9789c-111">Laiendage puul valikut Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="9789c-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="9789c-112">Valige puult Kliendiarve mudel \ Kliendiarve mudel (kohandatud).</span><span class="sxs-lookup"><span data-stu-id="9789c-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="9789c-113">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="9789c-113">Click Designer.</span></span>
6. <span data-ttu-id="9789c-114">Valige puult Kliendiarve(InvoiceCustomer).</span><span class="sxs-lookup"><span data-stu-id="9789c-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="9789c-115">Laiendame seda andmemudelit, näidates seda mis tahes failides, mis on manustatud müügitellimusele, mis on seotud elektrooniliselt töödeldava arvega.</span><span class="sxs-lookup"><span data-stu-id="9789c-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="9789c-116">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9789c-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="9789c-117">Tippige Arve manused väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="9789c-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="9789c-118">Arve manused</span><span class="sxs-lookup"><span data-stu-id="9789c-118">Invoice attachments</span></span>  
9. <span data-ttu-id="9789c-119">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="9789c-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="9789c-120">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="9789c-120">Click Add.</span></span>
11. <span data-ttu-id="9789c-121">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9789c-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="9789c-122">Tippige Faili sisu väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="9789c-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="9789c-123">Faili sisu</span><span class="sxs-lookup"><span data-stu-id="9789c-123">File content</span></span>  
13. <span data-ttu-id="9789c-124">Valige väljalt Kauba tüüp väärtus Konteiner.</span><span class="sxs-lookup"><span data-stu-id="9789c-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="9789c-125">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="9789c-125">Click Add.</span></span>
15. <span data-ttu-id="9789c-126">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9789c-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="9789c-127">Tippige Faili nimi väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="9789c-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="9789c-128">Faili nimi</span><span class="sxs-lookup"><span data-stu-id="9789c-128">File name</span></span>  
17. <span data-ttu-id="9789c-129">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="9789c-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="9789c-130">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="9789c-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="9789c-131">Uue andmemudeli elementide vastendamine andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="9789c-131">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="9789c-132">Klõpsake suvandit Mudeli vastendamine andmeallikaga.</span><span class="sxs-lookup"><span data-stu-id="9789c-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="9789c-133">Kasutage kiirfiltrit, et filtreerida väljal Definitsioon väärtusega InvoiceCustomer.</span><span class="sxs-lookup"><span data-stu-id="9789c-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="9789c-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="9789c-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="9789c-135">Vastendame uued mudelielemendid sobivate andmeallikatega.</span><span class="sxs-lookup"><span data-stu-id="9789c-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="9789c-136">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="9789c-136">Click Designer.</span></span>
4. <span data-ttu-id="9789c-137">Valige puult Arve manused.</span><span class="sxs-lookup"><span data-stu-id="9789c-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="9789c-138">Laiendage puul valikut Arve manused.</span><span class="sxs-lookup"><span data-stu-id="9789c-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="9789c-139">Valige puult Arve manused \ Faili nimi.</span><span class="sxs-lookup"><span data-stu-id="9789c-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="9789c-140">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="9789c-140">Click Edit.</span></span>
8. <span data-ttu-id="9789c-141">Sisestage väljale Valem väärtus 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="9789c-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="9789c-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="9789c-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="9789c-143">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9789c-143">Click Save.</span></span>
10. <span data-ttu-id="9789c-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9789c-144">Close the page.</span></span>
11. <span data-ttu-id="9789c-145">Valige puult Arve manused \ Faili sisu.</span><span class="sxs-lookup"><span data-stu-id="9789c-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="9789c-146">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="9789c-146">Click Edit.</span></span>
13. <span data-ttu-id="9789c-147">Sisestage väljale Valem väärtus 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="9789c-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="9789c-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="9789c-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="9789c-149">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9789c-149">Click Save.</span></span>
15. <span data-ttu-id="9789c-150">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9789c-150">Close the page.</span></span>
16. <span data-ttu-id="9789c-151">Valige puult Arve manused.</span><span class="sxs-lookup"><span data-stu-id="9789c-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="9789c-152">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="9789c-152">Click Edit.</span></span>
18. <span data-ttu-id="9789c-153">Sisestage väljale Valem väärtus 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="9789c-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="9789c-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="9789c-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="9789c-155">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9789c-155">Click Save.</span></span>
20. <span data-ttu-id="9789c-156">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9789c-156">Close the page.</span></span>
21. <span data-ttu-id="9789c-157">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9789c-157">Click Save.</span></span>
22. <span data-ttu-id="9789c-158">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9789c-158">Close the page.</span></span>
23. <span data-ttu-id="9789c-159">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9789c-159">Close the page.</span></span>
24. <span data-ttu-id="9789c-160">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9789c-160">Close the page.</span></span>
25. <span data-ttu-id="9789c-161">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="9789c-161">Click Change status.</span></span>
26. <span data-ttu-id="9789c-162">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="9789c-162">Click Complete.</span></span>
27. <span data-ttu-id="9789c-163">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9789c-163">Click OK.</span></span>

