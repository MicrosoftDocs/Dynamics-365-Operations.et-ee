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
ms.openlocfilehash: 1d42b585a61214628980cd45a859215443ed55b5
ms.sourcegitcommit: c461758290d7ddc19f0b60701368937c35ef78b0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864149"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="f0021-103">Veebimüügi ja -maksete sisestamine</span><span class="sxs-lookup"><span data-stu-id="f0021-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f0021-104">See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist veebipoe kannete jaoks müügitellimuste ja maksete loomiseks.</span><span class="sxs-lookup"><span data-stu-id="f0021-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="f0021-105">Internetimüügi ja maksete sisestamine on kaheosaline protsess.</span><span class="sxs-lookup"><span data-stu-id="f0021-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="f0021-106">Interneti jaemüügitehingute toomine peakontorisse.</span><span class="sxs-lookup"><span data-stu-id="f0021-106">Pulling the online retail transaction data in HQ.</span></span>
- <span data-ttu-id="f0021-107">Tellimuste sünkroonimine müügitellimuse loomiseks peakontoris.</span><span class="sxs-lookup"><span data-stu-id="f0021-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="f0021-108">Interneti jaemüügitehingute andmete toomist võib teha kas käsitsi, käivitades P-töö, või luues korduva pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="f0021-108">Pulling the online retail transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="f0021-109">P-töö käivitamine käsitsi</span><span class="sxs-lookup"><span data-stu-id="f0021-109">Manually running the P-job</span></span>

1. <span data-ttu-id="f0021-110">Avage Kõik töökohad > Jaemüügi IT.</span><span class="sxs-lookup"><span data-stu-id="f0021-110">Go to All workspaces > Retail IT.</span></span>
2. <span data-ttu-id="f0021-111">Klõpsake valikul Turustamisgraafik.</span><span class="sxs-lookup"><span data-stu-id="f0021-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="f0021-112">Valige P-0001.</span><span class="sxs-lookup"><span data-stu-id="f0021-112">Select P-0001.</span></span>
4. <span data-ttu-id="f0021-113">Reguleerige vajadusel kanali andmebaasi rühmasid.</span><span class="sxs-lookup"><span data-stu-id="f0021-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="f0021-114">Klõpsake valikut Käivita kohe.</span><span class="sxs-lookup"><span data-stu-id="f0021-114">Click Run now.</span></span>
6. <span data-ttu-id="f0021-115">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="f0021-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="f0021-116">Kordiva P-töö ajastamine</span><span class="sxs-lookup"><span data-stu-id="f0021-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="f0021-117">Avage Kõik töökohad > Jaemüügi IT.</span><span class="sxs-lookup"><span data-stu-id="f0021-117">Go to All workspaces > Retail IT.</span></span>
2. <span data-ttu-id="f0021-118">Klõpsake valikul Turustamisgraafik.</span><span class="sxs-lookup"><span data-stu-id="f0021-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="f0021-119">Valige P-0001.</span><span class="sxs-lookup"><span data-stu-id="f0021-119">Select P-0001.</span></span>
4. <span data-ttu-id="f0021-120">Klõpsake käsku Pakett-töö loomine.</span><span class="sxs-lookup"><span data-stu-id="f0021-120">Click Create batch job.</span></span>
5. <span data-ttu-id="f0021-121">Klõpsake käsku Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="f0021-121">Click Run in the background.</span></span>
5. <span data-ttu-id="f0021-122">Luba Pakett-töötlus.</span><span class="sxs-lookup"><span data-stu-id="f0021-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="f0021-123">Klõpsake valikut Korduvus..</span><span class="sxs-lookup"><span data-stu-id="f0021-123">Click Recurrence..</span></span>
7. <span data-ttu-id="f0021-124">Valige suvand Lõppkuupäev puudub.</span><span class="sxs-lookup"><span data-stu-id="f0021-124">Select the No end date option.</span></span>
8. <span data-ttu-id="f0021-125">Sisestage väljale Loenda käitamistevaheline intervall minutites.</span><span class="sxs-lookup"><span data-stu-id="f0021-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="f0021-126">Tavaliselt peaks see olema 5-10.</span><span class="sxs-lookup"><span data-stu-id="f0021-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="f0021-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f0021-127">Click OK.</span></span>
10. <span data-ttu-id="f0021-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f0021-128">Click OK.</span></span>

<span data-ttu-id="f0021-129">Tellimusi saab sünkroonida kas käsitsi, käivitades töö "Sünkrooni tellimused" või luues korduva pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="f0021-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="f0021-130">Käsitsi tellimuste sünkroonimise käivitamine</span><span class="sxs-lookup"><span data-stu-id="f0021-130">Manually running order synchronization</span></span> 

<span data-ttu-id="f0021-131">Toimige ühekordseks töö "Sünkrooni tellimused" käsitsi käivitamiseks järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="f0021-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="f0021-132">Avage Kõik tööruumid > Jaekaupluse rahandus.</span><span class="sxs-lookup"><span data-stu-id="f0021-132">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="f0021-133">Klõpsake suvandit Tellimuste sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="f0021-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="f0021-134">Valige väljal Organisatsiooni hierarhia suvand Jaekauplused piirkonniti.</span><span class="sxs-lookup"><span data-stu-id="f0021-134">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="f0021-135">Valige kindel veebipood või sõlm, kui soovite pakett-töö luua kaupluste grupi jaoks.</span><span class="sxs-lookup"><span data-stu-id="f0021-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="f0021-136">Klõpsake valiku lisamiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="f0021-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="f0021-137">Klõpsake vahekaarti Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="f0021-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="f0021-138">Keela Pakett-töötlus</span><span class="sxs-lookup"><span data-stu-id="f0021-138">Disable Batch processing</span></span>
6. <span data-ttu-id="f0021-139">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="f0021-139">Click Recurrence.</span></span>
7. <span data-ttu-id="f0021-140">Valige suvand Lõpeta pärast</span><span class="sxs-lookup"><span data-stu-id="f0021-140">Select End After option</span></span>
8. <span data-ttu-id="f0021-141">Sisestage väljale Lõpetage pärast väärtus 1.</span><span class="sxs-lookup"><span data-stu-id="f0021-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="f0021-142">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f0021-142">Click OK.</span></span>
10. <span data-ttu-id="f0021-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f0021-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="f0021-144">Korduva tellimuste sünkroonimise ajastamine</span><span class="sxs-lookup"><span data-stu-id="f0021-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="f0021-145">See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist veebipoe kannete jaoks müügitellimuste ja maksete loomiseks.</span><span class="sxs-lookup"><span data-stu-id="f0021-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="f0021-146">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="f0021-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="f0021-147">Avage Kõik tööruumid > Jaekaupluse rahandus.</span><span class="sxs-lookup"><span data-stu-id="f0021-147">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="f0021-148">Klõpsake suvandit Tellimuste sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="f0021-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="f0021-149">Valige väljal Organisatsiooni hierarhia suvand Jaekauplused piirkonniti.</span><span class="sxs-lookup"><span data-stu-id="f0021-149">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="f0021-150">Valige kindel veebipood või sõlm, kui soovite pakett-töö luua kaupluste grupi jaoks.</span><span class="sxs-lookup"><span data-stu-id="f0021-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="f0021-151">Klõpsake valiku lisamiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="f0021-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="f0021-152">Klõpsake vahekaarti Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="f0021-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="f0021-153">Luba Pakett-töötlus</span><span class="sxs-lookup"><span data-stu-id="f0021-153">Enable Batch processing</span></span>
6. <span data-ttu-id="f0021-154">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="f0021-154">Click Recurrence.</span></span>
7. <span data-ttu-id="f0021-155">Valige suvand Lõppkuupäev puudub.</span><span class="sxs-lookup"><span data-stu-id="f0021-155">Select the No end date option.</span></span>
8. <span data-ttu-id="f0021-156">Sisestage väljale Loenda käitamistevaheline intervall minutites.</span><span class="sxs-lookup"><span data-stu-id="f0021-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="f0021-157">Tavaliselt peaks see olema 2-20</span><span class="sxs-lookup"><span data-stu-id="f0021-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="f0021-158">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f0021-158">Click OK.</span></span>
10. <span data-ttu-id="f0021-159">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f0021-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="f0021-160">Protsessiga seotud andmeüksused</span><span class="sxs-lookup"><span data-stu-id="f0021-160">Data entities involved in the process</span></span>

- <span data-ttu-id="f0021-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="f0021-161">RetailTransactionTable</span></span>
- <span data-ttu-id="f0021-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="f0021-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="f0021-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="f0021-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="f0021-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="f0021-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="f0021-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="f0021-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="f0021-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="f0021-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="f0021-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="f0021-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="f0021-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="f0021-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="f0021-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="f0021-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="f0021-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="f0021-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="f0021-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="f0021-171">RetailTransactionAttributeTrans</span></span>
