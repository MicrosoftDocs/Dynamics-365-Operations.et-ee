---
title: EUR-00012 EL-i kandesertifikaadi väljastamine
description: See protseduur selgitab EL-i kandesertifikaadi lubamist, kliendikonto konfigureerimist kandesertifikaatide kasutamiseks ja sertifikaadi väljastamist.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustTable, SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CustEntryCertificateJour_W, SrsReportViewerForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee04632eee45aff1fe4b286c65024b0bc57bbb73
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537821"
---
# <a name="eur-00012-issue-an-eu-entry-certificate"></a><span data-ttu-id="9e931-103">EUR-00012 EL-i kandesertifikaadi väljastamine</span><span class="sxs-lookup"><span data-stu-id="9e931-103">EUR-00012 Issue an EU entry certificate</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e931-104">See protseduur selgitab EL-i kandesertifikaadi lubamist, kliendikonto konfigureerimist kandesertifikaatide kasutamiseks ja sertifikaadi väljastamist.</span><span class="sxs-lookup"><span data-stu-id="9e931-104">This procedure walks you through enabling an EU entry certificate, configuring a customer account to use entry certificates and issue a certificate.</span></span> <span data-ttu-id="9e931-105">Protseduuri loomisel kasutati demoettevõtte DEMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="9e931-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="enable-entry-certificate-management"></a><span data-ttu-id="9e931-106">Luba kandesertifikaadi haldamine</span><span class="sxs-lookup"><span data-stu-id="9e931-106">Enable entry certificate management</span></span>
1. <span data-ttu-id="9e931-107">Minge jaotisse Müügireskontro > Seadistus > Müügireskontro parameetrid.</span><span class="sxs-lookup"><span data-stu-id="9e931-107">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="9e931-108">Klõpsake vahekaarti Saadetised.</span><span class="sxs-lookup"><span data-stu-id="9e931-108">Click the Shipments tab.</span></span>
3. <span data-ttu-id="9e931-109">Laiendage jaotist Kandesertifikaat.</span><span class="sxs-lookup"><span data-stu-id="9e931-109">Expand the Entry certificate section.</span></span>
4. <span data-ttu-id="9e931-110">Valige väljal Luba kandesertifikaadi haldus suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="9e931-110">Select Yes in the Enable entry certificate management field.</span></span>
5. <span data-ttu-id="9e931-111">Valige väljal Luba kandesertifikaadi väljastamine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="9e931-111">Select Yes in the Enable entry certificate issuing field.</span></span>
6. <span data-ttu-id="9e931-112">Klõpsake vahekaarti Numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="9e931-112">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="9e931-113">Leidke ja valige loendist rida Kandesertifikaat.</span><span class="sxs-lookup"><span data-stu-id="9e931-113">In the list, find and select Entry certificate row.</span></span>
8. <span data-ttu-id="9e931-114">Sisestage või valige väärtus väljal Numbriseeria kood.</span><span class="sxs-lookup"><span data-stu-id="9e931-114">In the Number sequence code field, enter or select a value.</span></span>

## <a name="set-up-a-customer"></a><span data-ttu-id="9e931-115">Kliendi seadistamine</span><span class="sxs-lookup"><span data-stu-id="9e931-115">Set up a customer</span></span>
1. <span data-ttu-id="9e931-116">Avage Müügireskontro > Kliendid > Kõik kliendid.</span><span class="sxs-lookup"><span data-stu-id="9e931-116">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="9e931-117">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="9e931-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9e931-118">Näiteks saate filtrida välja Konto väärtuse DE-015 järgi.</span><span class="sxs-lookup"><span data-stu-id="9e931-118">For example, filter on the Account field with a value of 'DE-015'.</span></span>
3. <span data-ttu-id="9e931-119">Avage kliendi konto üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="9e931-119">Open customer account details.</span></span>
4. <span data-ttu-id="9e931-120">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="9e931-120">Click Edit.</span></span>
5. <span data-ttu-id="9e931-121">Laiendage jaotist Arve ja tarne.</span><span class="sxs-lookup"><span data-stu-id="9e931-121">Expand the Invoice and delivery section.</span></span>
6. <span data-ttu-id="9e931-122">Valige väljal Kandesertifikaat on nõutav suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="9e931-122">Select Yes in the Entry certificate required field.</span></span>
7. <span data-ttu-id="9e931-123">Valige väljal Väljasta kandesertifikaat suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="9e931-123">Select Yes in the Issue entry certificate field.</span></span>
8. <span data-ttu-id="9e931-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9e931-124">Click Save.</span></span>

## <a name="create-an-eu-entry-certificate-automatically"></a><span data-ttu-id="9e931-125">EL-i kandesertifikaadi automaatne loomine</span><span class="sxs-lookup"><span data-stu-id="9e931-125">Create an EU entry certificate automatically</span></span>
1. <span data-ttu-id="9e931-126">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="9e931-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="9e931-127">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9e931-127">Click New.</span></span>
3. <span data-ttu-id="9e931-128">Valige või sisestage väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="9e931-128">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="9e931-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9e931-129">Click OK.</span></span>
5. <span data-ttu-id="9e931-130">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="9e931-130">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="9e931-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9e931-131">Click Save.</span></span>
7. <span data-ttu-id="9e931-132">Klõpsake toimingupaanil valikut Komplekteerimine ja pakkimine.</span><span class="sxs-lookup"><span data-stu-id="9e931-132">On the Action Pane, click Pick and pack.</span></span>
8. <span data-ttu-id="9e931-133">Klõpsake valikut Saatelehe sisestamine.</span><span class="sxs-lookup"><span data-stu-id="9e931-133">Click Post packing slip.</span></span>
9. <span data-ttu-id="9e931-134">Laiendage jaotist Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="9e931-134">Expand the Parameters section.</span></span>
10. <span data-ttu-id="9e931-135">Valige väljal Kogus väärtus Kõik.</span><span class="sxs-lookup"><span data-stu-id="9e931-135">In the Quantity field, select 'All'.</span></span>
11. <span data-ttu-id="9e931-136">Tühjendage ruut Väljasta kandesertifikaat.</span><span class="sxs-lookup"><span data-stu-id="9e931-136">Clear the Issue entry certificate check box.</span></span>
    * <span data-ttu-id="9e931-137">Kandesertifikaadi saab väljastada saatelehe sisestamise või tellimuse arveldamise ajal.</span><span class="sxs-lookup"><span data-stu-id="9e931-137">An entry certificate can be issued during packing slip posting or during order invoicing.</span></span> <span data-ttu-id="9e931-138">Hiljem väljastamiseks jätke ruut Väljasta kandesertifikaat tühjaks.</span><span class="sxs-lookup"><span data-stu-id="9e931-138">Leave the Issue entry certificate checkbox unchecked to issue it later.</span></span>  
12. <span data-ttu-id="9e931-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9e931-139">Click OK.</span></span>
13. <span data-ttu-id="9e931-140">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9e931-140">Click OK.</span></span>
14. <span data-ttu-id="9e931-141">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="9e931-141">On the Action Pane, click Invoice.</span></span>
15. <span data-ttu-id="9e931-142">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="9e931-142">Click Invoice.</span></span>
    * <span data-ttu-id="9e931-143">Kontrollige, kas ruudud Kandesertifikaat on nõutav ja Väljasta kandesertifikaat jaotises Ülevaade on märgitud.</span><span class="sxs-lookup"><span data-stu-id="9e931-143">Verify that the Entry certificate required and Issue entry certificate checkboxes in the Overview section are marked.</span></span>  <span data-ttu-id="9e931-144">Saate valida ka ruudu Prindi kandesertifikaat, et lubada sertifikaadi printimine.</span><span class="sxs-lookup"><span data-stu-id="9e931-144">You can also select the Print entry certificate check box to allow printing of the certificate.</span></span>  
16. <span data-ttu-id="9e931-145">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9e931-145">Click OK.</span></span>
17. <span data-ttu-id="9e931-146">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9e931-146">Click OK.</span></span>
18. <span data-ttu-id="9e931-147">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="9e931-147">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="9e931-148">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="9e931-148">Click Invoice.</span></span>
20. <span data-ttu-id="9e931-149">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="9e931-149">On the Action Pane, click Invoice.</span></span>
21. <span data-ttu-id="9e931-150">Klõpsake suvandit Kuva väljastatud kandesertifikaadid.</span><span class="sxs-lookup"><span data-stu-id="9e931-150">Click View issued entry certificates.</span></span>
22. <span data-ttu-id="9e931-151">Klõpsake Prindi.</span><span class="sxs-lookup"><span data-stu-id="9e931-151">Click Print.</span></span>
23. <span data-ttu-id="9e931-152">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9e931-152">Close the page.</span></span>
24. <span data-ttu-id="9e931-153">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="9e931-153">Click Change status.</span></span>
25. <span data-ttu-id="9e931-154">Valige suvand väljal Uus olek.</span><span class="sxs-lookup"><span data-stu-id="9e931-154">In the New status field, select an option.</span></span>
26. <span data-ttu-id="9e931-155">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9e931-155">Click OK.</span></span>
27. <span data-ttu-id="9e931-156">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9e931-156">Close the page.</span></span>

## <a name="create-an-eu-entry-certificate-manually"></a><span data-ttu-id="9e931-157">EL-i kandesertifikaadi käsitsi loomine</span><span class="sxs-lookup"><span data-stu-id="9e931-157">Create an EU entry certificate manually</span></span>
1. <span data-ttu-id="9e931-158">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="9e931-158">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="9e931-159">Klõpsake suvandit Loo kandesertifikaat.</span><span class="sxs-lookup"><span data-stu-id="9e931-159">Click Create entry certificate.</span></span>
3. <span data-ttu-id="9e931-160">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9e931-160">Click OK.</span></span>
4. <span data-ttu-id="9e931-161">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="9e931-161">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="9e931-162">Klõpsake suvandit Kuva väljastatud kandesertifikaadid.</span><span class="sxs-lookup"><span data-stu-id="9e931-162">Click View issued entry certificates.</span></span>

