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
ms.openlocfilehash: 24eba0402caefb611a212db19cdb8feafa7c1fee
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550736"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="5decc-103">Elektrooniline aruandlus. Dokumendihalduse failide kasutamine vormingu väljundites (2. osa – andmemudeli laiendamine)</span><span class="sxs-lookup"><span data-stu-id="5decc-103">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5decc-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.</span><span class="sxs-lookup"><span data-stu-id="5decc-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="5decc-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="5decc-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="5decc-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid tegevuse juhendis Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (1. osa: andmemudeli ettevalmistamine).</span><span class="sxs-lookup"><span data-stu-id="5decc-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="5decc-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="5decc-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="5decc-108">Laiendage andmemudelit, et esitada selles dokumendihalduse faile</span><span class="sxs-lookup"><span data-stu-id="5decc-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="5decc-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="5decc-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="5decc-110">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="5decc-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="5decc-111">Laiendage puul valikut Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="5decc-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="5decc-112">Valige puult Kliendiarve mudel \ Kliendiarve mudel (kohandatud).</span><span class="sxs-lookup"><span data-stu-id="5decc-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="5decc-113">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="5decc-113">Click Designer.</span></span>
6. <span data-ttu-id="5decc-114">Valige puult Kliendiarve(InvoiceCustomer).</span><span class="sxs-lookup"><span data-stu-id="5decc-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="5decc-115">Laiendame seda andmemudelit, näidates seda mis tahes failides, mis on manustatud müügitellimusele, mis on seotud elektrooniliselt töödeldava arvega.</span><span class="sxs-lookup"><span data-stu-id="5decc-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="5decc-116">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="5decc-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="5decc-117">Tippige Arve manused väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="5decc-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="5decc-118">Arve manused</span><span class="sxs-lookup"><span data-stu-id="5decc-118">Invoice attachments</span></span>  
9. <span data-ttu-id="5decc-119">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="5decc-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="5decc-120">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="5decc-120">Click Add.</span></span>
11. <span data-ttu-id="5decc-121">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="5decc-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="5decc-122">Tippige Faili sisu väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="5decc-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="5decc-123">Faili sisu</span><span class="sxs-lookup"><span data-stu-id="5decc-123">File content</span></span>  
13. <span data-ttu-id="5decc-124">Valige väljalt Kauba tüüp väärtus Konteiner.</span><span class="sxs-lookup"><span data-stu-id="5decc-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="5decc-125">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="5decc-125">Click Add.</span></span>
15. <span data-ttu-id="5decc-126">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="5decc-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="5decc-127">Tippige Faili nimi väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="5decc-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="5decc-128">Faili nimi</span><span class="sxs-lookup"><span data-stu-id="5decc-128">File name</span></span>  
17. <span data-ttu-id="5decc-129">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="5decc-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="5decc-130">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="5decc-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="5decc-131">Uue andmemudeli elementide vastendamine andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="5decc-131">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="5decc-132">Klõpsake suvandit Mudeli vastendamine andmeallikaga.</span><span class="sxs-lookup"><span data-stu-id="5decc-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="5decc-133">Kasutage kiirfiltrit, et filtreerida väljal Definitsioon väärtusega InvoiceCustomer.</span><span class="sxs-lookup"><span data-stu-id="5decc-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="5decc-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="5decc-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="5decc-135">Vastendame uued mudelielemendid sobivate andmeallikatega.</span><span class="sxs-lookup"><span data-stu-id="5decc-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="5decc-136">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="5decc-136">Click Designer.</span></span>
4. <span data-ttu-id="5decc-137">Valige puult Arve manused.</span><span class="sxs-lookup"><span data-stu-id="5decc-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="5decc-138">Laiendage puul valikut Arve manused.</span><span class="sxs-lookup"><span data-stu-id="5decc-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="5decc-139">Valige puult Arve manused \ Faili nimi.</span><span class="sxs-lookup"><span data-stu-id="5decc-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="5decc-140">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="5decc-140">Click Edit.</span></span>
8. <span data-ttu-id="5decc-141">Sisestage väljale Valem väärtus 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="5decc-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="5decc-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="5decc-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="5decc-143">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5decc-143">Click Save.</span></span>
10. <span data-ttu-id="5decc-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5decc-144">Close the page.</span></span>
11. <span data-ttu-id="5decc-145">Valige puult Arve manused \ Faili sisu.</span><span class="sxs-lookup"><span data-stu-id="5decc-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="5decc-146">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="5decc-146">Click Edit.</span></span>
13. <span data-ttu-id="5decc-147">Sisestage väljale Valem väärtus 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="5decc-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="5decc-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="5decc-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="5decc-149">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5decc-149">Click Save.</span></span>
15. <span data-ttu-id="5decc-150">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5decc-150">Close the page.</span></span>
16. <span data-ttu-id="5decc-151">Valige puult Arve manused.</span><span class="sxs-lookup"><span data-stu-id="5decc-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="5decc-152">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="5decc-152">Click Edit.</span></span>
18. <span data-ttu-id="5decc-153">Sisestage väljale Valem väärtus 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="5decc-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="5decc-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="5decc-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="5decc-155">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5decc-155">Click Save.</span></span>
20. <span data-ttu-id="5decc-156">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5decc-156">Close the page.</span></span>
21. <span data-ttu-id="5decc-157">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5decc-157">Click Save.</span></span>
22. <span data-ttu-id="5decc-158">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5decc-158">Close the page.</span></span>
23. <span data-ttu-id="5decc-159">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5decc-159">Close the page.</span></span>
24. <span data-ttu-id="5decc-160">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5decc-160">Close the page.</span></span>
25. <span data-ttu-id="5decc-161">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="5decc-161">Click Change status.</span></span>
26. <span data-ttu-id="5decc-162">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="5decc-162">Click Complete.</span></span>
27. <span data-ttu-id="5decc-163">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5decc-163">Click OK.</span></span>
