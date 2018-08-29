--- 
title: "Andmemudelite laiendamine dokumendihalduse failide kasutamiseks elektroonilise aruandluse väljundis"
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
ms.openlocfilehash: 8363dd2af728577175a620d7b645d90cea84803a
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---
# <a name="extend-data-models-to-use-document-management-files-in-er-output"></a><span data-ttu-id="69939-103">Andmemudelite laiendamine dokumendihalduse failide kasutamiseks elektroonilise aruandluse väljundis</span><span class="sxs-lookup"><span data-stu-id="69939-103">Extend data models to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="69939-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.</span><span class="sxs-lookup"><span data-stu-id="69939-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="69939-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="69939-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="69939-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid tegevuse juhendis Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (1. osa: andmemudeli ettevalmistamine).</span><span class="sxs-lookup"><span data-stu-id="69939-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="69939-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="69939-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="69939-108">Laiendage andmemudelit, et esitada selles dokumendihalduse faile</span><span class="sxs-lookup"><span data-stu-id="69939-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="69939-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="69939-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="69939-110">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="69939-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="69939-111">Laiendage puul valikut Kliendiarve mudel.</span><span class="sxs-lookup"><span data-stu-id="69939-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="69939-112">Valige puult Kliendiarve mudel \ Kliendiarve mudel (kohandatud).</span><span class="sxs-lookup"><span data-stu-id="69939-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="69939-113">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="69939-113">Click Designer.</span></span>
6. <span data-ttu-id="69939-114">Valige puult Kliendiarve(InvoiceCustomer).</span><span class="sxs-lookup"><span data-stu-id="69939-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="69939-115">Laiendame seda andmemudelit, näidates seda mis tahes failides, mis on manustatud müügitellimusele, mis on seotud elektrooniliselt töödeldava arvega.</span><span class="sxs-lookup"><span data-stu-id="69939-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="69939-116">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="69939-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="69939-117">Tippige Arve manused väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="69939-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="69939-118">Arve manused</span><span class="sxs-lookup"><span data-stu-id="69939-118">Invoice attachments</span></span>  
9. <span data-ttu-id="69939-119">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="69939-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="69939-120">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="69939-120">Click Add.</span></span>
11. <span data-ttu-id="69939-121">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="69939-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="69939-122">Tippige Faili sisu väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="69939-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="69939-123">Faili sisu</span><span class="sxs-lookup"><span data-stu-id="69939-123">File content</span></span>  
13. <span data-ttu-id="69939-124">Valige väljalt Kauba tüüp väärtus Konteiner.</span><span class="sxs-lookup"><span data-stu-id="69939-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="69939-125">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="69939-125">Click Add.</span></span>
15. <span data-ttu-id="69939-126">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="69939-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="69939-127">Tippige Faili nimi väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="69939-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="69939-128">Faili nimi</span><span class="sxs-lookup"><span data-stu-id="69939-128">File name</span></span>  
17. <span data-ttu-id="69939-129">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="69939-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="69939-130">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="69939-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="69939-131">Uute andmemudeli elementide vastendamine rakenduse Dynamics 365 for Finance and Operations andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="69939-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="69939-132">Klõpsake suvandit Mudeli vastendamine andmeallikaga.</span><span class="sxs-lookup"><span data-stu-id="69939-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="69939-133">Kasutage kiirfiltrit, et filtreerida väljal Definitsioon väärtusega InvoiceCustomer.</span><span class="sxs-lookup"><span data-stu-id="69939-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="69939-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="69939-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="69939-135">Vastendame uued mudelielemendid sobivate andmeallikatega.</span><span class="sxs-lookup"><span data-stu-id="69939-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="69939-136">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="69939-136">Click Designer.</span></span>
4. <span data-ttu-id="69939-137">Valige puult Arve manused.</span><span class="sxs-lookup"><span data-stu-id="69939-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="69939-138">Laiendage puul valikut Arve manused.</span><span class="sxs-lookup"><span data-stu-id="69939-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="69939-139">Valige puult Arve manused \ Faili nimi.</span><span class="sxs-lookup"><span data-stu-id="69939-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="69939-140">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="69939-140">Click Edit.</span></span>
8. <span data-ttu-id="69939-141">Sisestage väljale Valem väärtus 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="69939-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="69939-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="69939-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="69939-143">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="69939-143">Click Save.</span></span>
10. <span data-ttu-id="69939-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="69939-144">Close the page.</span></span>
11. <span data-ttu-id="69939-145">Valige puult Arve manused \ Faili sisu.</span><span class="sxs-lookup"><span data-stu-id="69939-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="69939-146">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="69939-146">Click Edit.</span></span>
13. <span data-ttu-id="69939-147">Sisestage väljale Valem väärtus 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="69939-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="69939-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="69939-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="69939-149">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="69939-149">Click Save.</span></span>
15. <span data-ttu-id="69939-150">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="69939-150">Close the page.</span></span>
16. <span data-ttu-id="69939-151">Valige puult Arve manused.</span><span class="sxs-lookup"><span data-stu-id="69939-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="69939-152">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="69939-152">Click Edit.</span></span>
18. <span data-ttu-id="69939-153">Sisestage väljale Valem väärtus 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="69939-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="69939-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="69939-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="69939-155">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="69939-155">Click Save.</span></span>
20. <span data-ttu-id="69939-156">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="69939-156">Close the page.</span></span>
21. <span data-ttu-id="69939-157">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="69939-157">Click Save.</span></span>
22. <span data-ttu-id="69939-158">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="69939-158">Close the page.</span></span>
23. <span data-ttu-id="69939-159">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="69939-159">Close the page.</span></span>
24. <span data-ttu-id="69939-160">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="69939-160">Close the page.</span></span>
25. <span data-ttu-id="69939-161">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="69939-161">Click Change status.</span></span>
26. <span data-ttu-id="69939-162">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="69939-162">Click Complete.</span></span>
27. <span data-ttu-id="69939-163">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="69939-163">Click OK.</span></span>


