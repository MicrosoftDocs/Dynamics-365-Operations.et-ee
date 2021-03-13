---
title: Elektrooniline aruandlus. Dokumendihalduse failide kasutamine vormingu väljundites (2. osa – andmemudeli laiendamine)
description: Selles teemas kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse (ER) vormingut kasutama ER-i väljundis dokumendihalduse faile (manused). (2. osa)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd06cdfd9bae57577c2e3ec97848e319b197f41
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092586"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="884ac-104">Elektrooniline aruandlus. Dokumendihalduse failide kasutamine vormingu väljundites (2. osa – andmemudeli laiendamine)</span><span class="sxs-lookup"><span data-stu-id="884ac-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="884ac-105">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.</span><span class="sxs-lookup"><span data-stu-id="884ac-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="884ac-106">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="884ac-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="884ac-107">Nende etappide lõpule viimiseks peate esmalt lõpetama etapid tegevuse juhendis „Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (1. osa: andmemudeli ettevalmistamine)”.</span><span class="sxs-lookup"><span data-stu-id="884ac-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="884ac-108">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="884ac-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="884ac-109">Laiendage andmemudelit, et esitada selles dokumendihalduse faile</span><span class="sxs-lookup"><span data-stu-id="884ac-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="884ac-110">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="884ac-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="884ac-111">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="884ac-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="884ac-112">Laiendage puul valikut Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="884ac-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="884ac-113">Valige puult Kliendiarve mudel \ Kliendiarve mudel (kohandatud).</span><span class="sxs-lookup"><span data-stu-id="884ac-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="884ac-114">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="884ac-114">Click Designer.</span></span>
6. <span data-ttu-id="884ac-115">Valige puult Kliendiarve(InvoiceCustomer).</span><span class="sxs-lookup"><span data-stu-id="884ac-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="884ac-116">Laiendame seda andmemudelit, näidates seda mis tahes failides, mis on manustatud müügitellimusele, mis on seotud elektrooniliselt töödeldava arvega.</span><span class="sxs-lookup"><span data-stu-id="884ac-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="884ac-117">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="884ac-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="884ac-118">Tippige Arve manused väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="884ac-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="884ac-119">Arve manused</span><span class="sxs-lookup"><span data-stu-id="884ac-119">Invoice attachments</span></span>  
9. <span data-ttu-id="884ac-120">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="884ac-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="884ac-121">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="884ac-121">Click Add.</span></span>
11. <span data-ttu-id="884ac-122">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="884ac-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="884ac-123">Tippige Faili sisu väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="884ac-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="884ac-124">Faili sisu</span><span class="sxs-lookup"><span data-stu-id="884ac-124">File content</span></span>  
13. <span data-ttu-id="884ac-125">Valige väljalt Kauba tüüp väärtus Konteiner.</span><span class="sxs-lookup"><span data-stu-id="884ac-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="884ac-126">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="884ac-126">Click Add.</span></span>
15. <span data-ttu-id="884ac-127">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="884ac-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="884ac-128">Tippige Faili nimi väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="884ac-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="884ac-129">Faili nimi</span><span class="sxs-lookup"><span data-stu-id="884ac-129">File name</span></span>  
17. <span data-ttu-id="884ac-130">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="884ac-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="884ac-131">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="884ac-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="884ac-132">Uue andmemudeli elementide vastendamine andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="884ac-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="884ac-133">Klõpsake suvandit Mudeli vastendamine andmeallikaga.</span><span class="sxs-lookup"><span data-stu-id="884ac-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="884ac-134">Kasutage kiirfiltrit, et filtreerida väljal Definitsioon väärtusega InvoiceCustomer.</span><span class="sxs-lookup"><span data-stu-id="884ac-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="884ac-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="884ac-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="884ac-136">Vastendame uued mudelielemendid sobivate andmeallikatega.</span><span class="sxs-lookup"><span data-stu-id="884ac-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="884ac-137">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="884ac-137">Click Designer.</span></span>
4. <span data-ttu-id="884ac-138">Valige puult Arve manused.</span><span class="sxs-lookup"><span data-stu-id="884ac-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="884ac-139">Laiendage puul valikut Arve manused.</span><span class="sxs-lookup"><span data-stu-id="884ac-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="884ac-140">Valige puult Arve manused \ Faili nimi.</span><span class="sxs-lookup"><span data-stu-id="884ac-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="884ac-141">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="884ac-141">Click Edit.</span></span>
8. <span data-ttu-id="884ac-142">Sisestage väljale Valem väärtus 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="884ac-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="884ac-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="884ac-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="884ac-144">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="884ac-144">Click Save.</span></span>
10. <span data-ttu-id="884ac-145">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="884ac-145">Close the page.</span></span>
11. <span data-ttu-id="884ac-146">Valige puult Arve manused \ Faili sisu.</span><span class="sxs-lookup"><span data-stu-id="884ac-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="884ac-147">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="884ac-147">Click Edit.</span></span>
13. <span data-ttu-id="884ac-148">Sisestage väljale Valem väärtus 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="884ac-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="884ac-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="884ac-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="884ac-150">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="884ac-150">Click Save.</span></span>
15. <span data-ttu-id="884ac-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="884ac-151">Close the page.</span></span>
16. <span data-ttu-id="884ac-152">Valige puult Arve manused.</span><span class="sxs-lookup"><span data-stu-id="884ac-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="884ac-153">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="884ac-153">Click Edit.</span></span>
18. <span data-ttu-id="884ac-154">Sisestage väljale Valem väärtus 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="884ac-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="884ac-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="884ac-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="884ac-156">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="884ac-156">Click Save.</span></span>
20. <span data-ttu-id="884ac-157">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="884ac-157">Close the page.</span></span>
21. <span data-ttu-id="884ac-158">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="884ac-158">Click Save.</span></span>
22. <span data-ttu-id="884ac-159">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="884ac-159">Close the page.</span></span>
23. <span data-ttu-id="884ac-160">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="884ac-160">Close the page.</span></span>
24. <span data-ttu-id="884ac-161">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="884ac-161">Close the page.</span></span>
25. <span data-ttu-id="884ac-162">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="884ac-162">Click Change status.</span></span>
26. <span data-ttu-id="884ac-163">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="884ac-163">Click Complete.</span></span>
27. <span data-ttu-id="884ac-164">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="884ac-164">Click OK.</span></span>

