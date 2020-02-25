---
title: Veebimüügi ja -maksete sisestamine
description: See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist veebipoe kannete jaoks müügitellimuste ja maksete loomiseks.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf7f72be22539271649aa7f5541735b3d24dab66
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022244"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="afdd4-103">Veebimüügi ja -maksete sisestamine</span><span class="sxs-lookup"><span data-stu-id="afdd4-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="afdd4-104">See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist veebipoe kannete jaoks müügitellimuste ja maksete loomiseks.</span><span class="sxs-lookup"><span data-stu-id="afdd4-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="afdd4-105">Internetimüügi ja maksete sisestamine on kaheosaline protsess.</span><span class="sxs-lookup"><span data-stu-id="afdd4-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="afdd4-106">Interneti kaubandustehingute toomine peakontorisse.</span><span class="sxs-lookup"><span data-stu-id="afdd4-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="afdd4-107">Tellimuste sünkroonimine müügitellimuse loomiseks peakontoris.</span><span class="sxs-lookup"><span data-stu-id="afdd4-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="afdd4-108">Internetitehingute andmete toomist võib teha kas käsitsi, käivitades P-töö või luues korduva pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="afdd4-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="afdd4-109">P-töö käivitamine käsitsi</span><span class="sxs-lookup"><span data-stu-id="afdd4-109">Manually running the P-job</span></span>

1. <span data-ttu-id="afdd4-110">Minge jaotisse Kõik tööruumid > Jaemüügi ja kaubanduse IT.</span><span class="sxs-lookup"><span data-stu-id="afdd4-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="afdd4-111">Klõpsake valikul Turustamisgraafik.</span><span class="sxs-lookup"><span data-stu-id="afdd4-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="afdd4-112">Valige P-0001.</span><span class="sxs-lookup"><span data-stu-id="afdd4-112">Select P-0001.</span></span>
4. <span data-ttu-id="afdd4-113">Reguleerige vajadusel kanali andmebaasi rühmasid.</span><span class="sxs-lookup"><span data-stu-id="afdd4-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="afdd4-114">Klõpsake valikut Käivita kohe.</span><span class="sxs-lookup"><span data-stu-id="afdd4-114">Click Run now.</span></span>
6. <span data-ttu-id="afdd4-115">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="afdd4-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="afdd4-116">Kordiva P-töö ajastamine</span><span class="sxs-lookup"><span data-stu-id="afdd4-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="afdd4-117">Minge jaotisse Kõik tööruumid > Jaemüügi ja kaubanduse IT.</span><span class="sxs-lookup"><span data-stu-id="afdd4-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="afdd4-118">Klõpsake valikul Turustamisgraafik.</span><span class="sxs-lookup"><span data-stu-id="afdd4-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="afdd4-119">Valige P-0001.</span><span class="sxs-lookup"><span data-stu-id="afdd4-119">Select P-0001.</span></span>
4. <span data-ttu-id="afdd4-120">Klõpsake käsku Pakett-töö loomine.</span><span class="sxs-lookup"><span data-stu-id="afdd4-120">Click Create batch job.</span></span>
5. <span data-ttu-id="afdd4-121">Klõpsake käsku Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="afdd4-121">Click Run in the background.</span></span>
5. <span data-ttu-id="afdd4-122">Luba Pakett-töötlus.</span><span class="sxs-lookup"><span data-stu-id="afdd4-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="afdd4-123">Klõpsake valikut Korduvus..</span><span class="sxs-lookup"><span data-stu-id="afdd4-123">Click Recurrence..</span></span>
7. <span data-ttu-id="afdd4-124">Valige suvand Lõppkuupäev puudub.</span><span class="sxs-lookup"><span data-stu-id="afdd4-124">Select the No end date option.</span></span>
8. <span data-ttu-id="afdd4-125">Sisestage väljale Loenda käitamistevaheline intervall minutites.</span><span class="sxs-lookup"><span data-stu-id="afdd4-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="afdd4-126">Tavaliselt peaks see olema 5-10.</span><span class="sxs-lookup"><span data-stu-id="afdd4-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="afdd4-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="afdd4-127">Click OK.</span></span>
10. <span data-ttu-id="afdd4-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="afdd4-128">Click OK.</span></span>

<span data-ttu-id="afdd4-129">Tellimusi saab sünkroonida kas käsitsi, käivitades töö "Sünkrooni tellimused" või luues korduva pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="afdd4-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="afdd4-130">Käsitsi tellimuste sünkroonimise käivitamine</span><span class="sxs-lookup"><span data-stu-id="afdd4-130">Manually running order synchronization</span></span> 

<span data-ttu-id="afdd4-131">Toimige ühekordseks töö "Sünkrooni tellimused" käsitsi käivitamiseks järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="afdd4-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="afdd4-132">Avage Kõik tööruumid > Kaupluse rahandus.</span><span class="sxs-lookup"><span data-stu-id="afdd4-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="afdd4-133">Klõpsake suvandit Tellimuste sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="afdd4-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="afdd4-134">Valige väljal Organisatsiooni hierarhia suvand Kauplused piirkonniti.</span><span class="sxs-lookup"><span data-stu-id="afdd4-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="afdd4-135">Valige kindel veebipood või sõlm, kui soovite pakett-töö luua kaupluste grupi jaoks.</span><span class="sxs-lookup"><span data-stu-id="afdd4-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="afdd4-136">Klõpsake valiku lisamiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="afdd4-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="afdd4-137">Klõpsake vahekaarti Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="afdd4-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="afdd4-138">Keela Pakett-töötlus</span><span class="sxs-lookup"><span data-stu-id="afdd4-138">Disable Batch processing</span></span>
6. <span data-ttu-id="afdd4-139">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="afdd4-139">Click Recurrence.</span></span>
7. <span data-ttu-id="afdd4-140">Valige suvand Lõpeta pärast</span><span class="sxs-lookup"><span data-stu-id="afdd4-140">Select End After option</span></span>
8. <span data-ttu-id="afdd4-141">Sisestage väljale Lõpetage pärast väärtus 1.</span><span class="sxs-lookup"><span data-stu-id="afdd4-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="afdd4-142">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="afdd4-142">Click OK.</span></span>
10. <span data-ttu-id="afdd4-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="afdd4-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="afdd4-144">Korduva tellimuste sünkroonimise ajastamine</span><span class="sxs-lookup"><span data-stu-id="afdd4-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="afdd4-145">See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist veebipoe kannete jaoks müügitellimuste ja maksete loomiseks.</span><span class="sxs-lookup"><span data-stu-id="afdd4-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="afdd4-146">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="afdd4-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="afdd4-147">Avage Kõik tööruumid > Kaupluse rahandus.</span><span class="sxs-lookup"><span data-stu-id="afdd4-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="afdd4-148">Klõpsake suvandit Tellimuste sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="afdd4-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="afdd4-149">Valige väljal Organisatsiooni hierarhia suvand Kauplused piirkonniti.</span><span class="sxs-lookup"><span data-stu-id="afdd4-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="afdd4-150">Valige kindel veebipood või sõlm, kui soovite pakett-töö luua kaupluste grupi jaoks.</span><span class="sxs-lookup"><span data-stu-id="afdd4-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="afdd4-151">Klõpsake valiku lisamiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="afdd4-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="afdd4-152">Klõpsake vahekaarti Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="afdd4-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="afdd4-153">Luba Pakett-töötlus</span><span class="sxs-lookup"><span data-stu-id="afdd4-153">Enable Batch processing</span></span>
6. <span data-ttu-id="afdd4-154">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="afdd4-154">Click Recurrence.</span></span>
7. <span data-ttu-id="afdd4-155">Valige suvand Lõppkuupäev puudub.</span><span class="sxs-lookup"><span data-stu-id="afdd4-155">Select the No end date option.</span></span>
8. <span data-ttu-id="afdd4-156">Sisestage väljale Loenda käitamistevaheline intervall minutites.</span><span class="sxs-lookup"><span data-stu-id="afdd4-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="afdd4-157">Tavaliselt peaks see olema 2-20</span><span class="sxs-lookup"><span data-stu-id="afdd4-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="afdd4-158">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="afdd4-158">Click OK.</span></span>
10. <span data-ttu-id="afdd4-159">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="afdd4-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="afdd4-160">Protsessiga seotud andmeüksused</span><span class="sxs-lookup"><span data-stu-id="afdd4-160">Data entities involved in the process</span></span>

- <span data-ttu-id="afdd4-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="afdd4-161">RetailTransactionTable</span></span>
- <span data-ttu-id="afdd4-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="afdd4-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="afdd4-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="afdd4-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="afdd4-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="afdd4-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="afdd4-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="afdd4-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="afdd4-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="afdd4-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="afdd4-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="afdd4-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="afdd4-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="afdd4-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="afdd4-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="afdd4-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="afdd4-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="afdd4-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="afdd4-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="afdd4-171">RetailTransactionAttributeTrans</span></span>
