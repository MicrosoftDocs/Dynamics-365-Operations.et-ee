--- 
title: "EL-i kandesertifikaadi väljastamine"
description: "See protseduur selgitab EL-i kandesertifikaadi lubamist, kliendikonto konfigureerimist kandesertifikaatide kasutamiseks ja sertifikaadi väljastamist."
author: mrolecki
manager: AnnBe
ms.date: 02/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ff00ff0df3835ee2cbf21219ad6f07bfeba6e7ac
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="issue-an-eu-entry-certificate"></a><span data-ttu-id="9763b-103">EL-i kandesertifikaadi väljastamine</span><span class="sxs-lookup"><span data-stu-id="9763b-103">Issue an EU entry certificate</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9763b-104">See protseduur selgitab EL-i kandesertifikaadi lubamist, kliendikonto konfigureerimist kandesertifikaatide kasutamiseks ja sertifikaadi väljastamist.</span><span class="sxs-lookup"><span data-stu-id="9763b-104">This procedure walks you through enabling an EU entry certificate, configuring a customer account to use entry certificates and issue a certificate.</span></span> <span data-ttu-id="9763b-105">Protseduuri loomisel kasutati demoettevõtte DEMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="9763b-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="enable-entry-certificate-management"></a><span data-ttu-id="9763b-106">Luba kandesertifikaadi haldamine</span><span class="sxs-lookup"><span data-stu-id="9763b-106">Enable entry certificate management</span></span>
1. <span data-ttu-id="9763b-107">Minge jaotisse Müügireskontro > Seadistus > Müügireskontro parameetrid.</span><span class="sxs-lookup"><span data-stu-id="9763b-107">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="9763b-108">Klõpsake vahekaarti Saadetised.</span><span class="sxs-lookup"><span data-stu-id="9763b-108">Click the Shipments tab.</span></span>
3. <span data-ttu-id="9763b-109">Laiendage jaotist Kandesertifikaat.</span><span class="sxs-lookup"><span data-stu-id="9763b-109">Expand the Entry certificate section.</span></span>
4. <span data-ttu-id="9763b-110">Valige väljal Luba kandesertifikaadi haldus suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="9763b-110">Select Yes in the Enable entry certificate management field.</span></span>
5. <span data-ttu-id="9763b-111">Valige väljal Luba kandesertifikaadi väljastamine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="9763b-111">Select Yes in the Enable entry certificate issuing field.</span></span>
6. <span data-ttu-id="9763b-112">Klõpsake vahekaarti Numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="9763b-112">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="9763b-113">Leidke ja valige loendist rida Kandesertifikaat.</span><span class="sxs-lookup"><span data-stu-id="9763b-113">In the list, find and select Entry certificate row.</span></span>
8. <span data-ttu-id="9763b-114">Sisestage või valige väärtus väljal Numbriseeria kood.</span><span class="sxs-lookup"><span data-stu-id="9763b-114">In the Number sequence code field, enter or select a value.</span></span>

## <a name="set-up-a-customer"></a><span data-ttu-id="9763b-115">Kliendi seadistamine</span><span class="sxs-lookup"><span data-stu-id="9763b-115">Set up a customer</span></span>
1. <span data-ttu-id="9763b-116">Avage Müügireskontro > Kliendid > Kõik kliendid.</span><span class="sxs-lookup"><span data-stu-id="9763b-116">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="9763b-117">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="9763b-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9763b-118">Näiteks saate filtrida välja Konto väärtuse DE-015 järgi.</span><span class="sxs-lookup"><span data-stu-id="9763b-118">For example, filter on the Account field with a value of 'DE-015'.</span></span>
3. <span data-ttu-id="9763b-119">Avage kliendi konto üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="9763b-119">Open customer account details.</span></span>
4. <span data-ttu-id="9763b-120">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="9763b-120">Click Edit.</span></span>
5. <span data-ttu-id="9763b-121">Laiendage jaotist Arve ja tarne.</span><span class="sxs-lookup"><span data-stu-id="9763b-121">Expand the Invoice and delivery section.</span></span>
6. <span data-ttu-id="9763b-122">Valige väljal Kandesertifikaat on nõutav suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="9763b-122">Select Yes in the Entry certificate required field.</span></span>
7. <span data-ttu-id="9763b-123">Valige väljal Väljasta kandesertifikaat suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="9763b-123">Select Yes in the Issue entry certificate field.</span></span>
8. <span data-ttu-id="9763b-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9763b-124">Click Save.</span></span>

## <a name="create-an-eu-entry-certificate-automatically"></a><span data-ttu-id="9763b-125">EL-i kandesertifikaadi automaatne loomine</span><span class="sxs-lookup"><span data-stu-id="9763b-125">Create an EU entry certificate automatically</span></span>
1. <span data-ttu-id="9763b-126">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="9763b-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="9763b-127">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9763b-127">Click New.</span></span>
3. <span data-ttu-id="9763b-128">Valige või sisestage väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="9763b-128">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="9763b-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9763b-129">Click OK.</span></span>
5. <span data-ttu-id="9763b-130">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="9763b-130">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="9763b-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9763b-131">Click Save.</span></span>
7. <span data-ttu-id="9763b-132">Klõpsake toimingupaanil valikut Komplekteerimine ja pakkimine.</span><span class="sxs-lookup"><span data-stu-id="9763b-132">On the Action Pane, click Pick and pack.</span></span>
8. <span data-ttu-id="9763b-133">Klõpsake valikut Saatelehe sisestamine.</span><span class="sxs-lookup"><span data-stu-id="9763b-133">Click Post packing slip.</span></span>
9. <span data-ttu-id="9763b-134">Laiendage jaotist Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="9763b-134">Expand the Parameters section.</span></span>
10. <span data-ttu-id="9763b-135">Valige väljal Kogus väärtus Kõik.</span><span class="sxs-lookup"><span data-stu-id="9763b-135">In the Quantity field, select 'All'.</span></span>
11. <span data-ttu-id="9763b-136">Tühjendage ruut Väljasta kandesertifikaat.</span><span class="sxs-lookup"><span data-stu-id="9763b-136">Clear the Issue entry certificate check box.</span></span>
    * <span data-ttu-id="9763b-137">Kandesertifikaadi saab väljastada saatelehe sisestamise või tellimuse arveldamise ajal.</span><span class="sxs-lookup"><span data-stu-id="9763b-137">An entry certificate can be issued during packing slip posting or during order invoicing.</span></span> <span data-ttu-id="9763b-138">Hiljem väljastamiseks jätke ruut Väljasta kandesertifikaat tühjaks.</span><span class="sxs-lookup"><span data-stu-id="9763b-138">Leave the Issue entry certificate checkbox unchecked to issue it later.</span></span>  
12. <span data-ttu-id="9763b-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9763b-139">Click OK.</span></span>
13. <span data-ttu-id="9763b-140">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9763b-140">Click OK.</span></span>
14. <span data-ttu-id="9763b-141">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="9763b-141">On the Action Pane, click Invoice.</span></span>
15. <span data-ttu-id="9763b-142">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="9763b-142">Click Invoice.</span></span>
    * <span data-ttu-id="9763b-143">Kontrollige, kas ruudud Kandesertifikaat on nõutav ja Väljasta kandesertifikaat jaotises Ülevaade on märgitud.</span><span class="sxs-lookup"><span data-stu-id="9763b-143">Verify that the Entry certificate required and Issue entry certificate checkboxes in the Overview section are marked.</span></span>  <span data-ttu-id="9763b-144">Saate valida ka ruudu Prindi kandesertifikaat, et lubada sertifikaadi printimine.</span><span class="sxs-lookup"><span data-stu-id="9763b-144">You can also select the Print entry certificate check box to allow printing of the certificate.</span></span>  
16. <span data-ttu-id="9763b-145">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9763b-145">Click OK.</span></span>
17. <span data-ttu-id="9763b-146">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9763b-146">Click OK.</span></span>
18. <span data-ttu-id="9763b-147">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="9763b-147">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="9763b-148">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="9763b-148">Click Invoice.</span></span>
20. <span data-ttu-id="9763b-149">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="9763b-149">On the Action Pane, click Invoice.</span></span>
21. <span data-ttu-id="9763b-150">Klõpsake suvandit Kuva väljastatud kandesertifikaadid.</span><span class="sxs-lookup"><span data-stu-id="9763b-150">Click View issued entry certificates.</span></span>
22. <span data-ttu-id="9763b-151">Klõpsake Prindi.</span><span class="sxs-lookup"><span data-stu-id="9763b-151">Click Print.</span></span>
23. <span data-ttu-id="9763b-152">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9763b-152">Close the page.</span></span>
24. <span data-ttu-id="9763b-153">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="9763b-153">Click Change status.</span></span>
25. <span data-ttu-id="9763b-154">Valige suvand väljal Uus olek.</span><span class="sxs-lookup"><span data-stu-id="9763b-154">In the New status field, select an option.</span></span>
26. <span data-ttu-id="9763b-155">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9763b-155">Click OK.</span></span>
27. <span data-ttu-id="9763b-156">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9763b-156">Close the page.</span></span>

## <a name="create-an-eu-entry-certificate-manually"></a><span data-ttu-id="9763b-157">EL-i kandesertifikaadi käsitsi loomine</span><span class="sxs-lookup"><span data-stu-id="9763b-157">Create an EU entry certificate manually</span></span>
1. <span data-ttu-id="9763b-158">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="9763b-158">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="9763b-159">Klõpsake suvandit Loo kandesertifikaat.</span><span class="sxs-lookup"><span data-stu-id="9763b-159">Click Create entry certificate.</span></span>
3. <span data-ttu-id="9763b-160">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9763b-160">Click OK.</span></span>
4. <span data-ttu-id="9763b-161">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="9763b-161">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="9763b-162">Klõpsake suvandit Kuva väljastatud kandesertifikaadid.</span><span class="sxs-lookup"><span data-stu-id="9763b-162">Click View issued entry certificates.</span></span>


