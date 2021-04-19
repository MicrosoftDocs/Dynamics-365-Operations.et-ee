---
title: Veebimüügi ja -maksete sisestamine
description: See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist veebipoe kannete jaoks müügitellimuste ja maksete loomiseks.
author: psimolin
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2e482b0fb5f2cf67e687c2b278bc5b54ad09839
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802667"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="85798-103">Veebimüügi ja -maksete sisestamine</span><span class="sxs-lookup"><span data-stu-id="85798-103">Posting of online sales and payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85798-104">See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist veebipoe kannete jaoks müügitellimuste ja maksete loomiseks.</span><span class="sxs-lookup"><span data-stu-id="85798-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="85798-105">Internetimüügi ja maksete sisestamine on kaheosaline protsess.</span><span class="sxs-lookup"><span data-stu-id="85798-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="85798-106">Interneti kaubandustehingute toomine peakontorisse.</span><span class="sxs-lookup"><span data-stu-id="85798-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="85798-107">Tellimuste sünkroonimine müügitellimuse loomiseks peakontoris.</span><span class="sxs-lookup"><span data-stu-id="85798-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="85798-108">Internetitehingute andmete toomist võib teha kas käsitsi, käivitades P-töö või luues korduva pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="85798-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="85798-109">P-töö käivitamine käsitsi</span><span class="sxs-lookup"><span data-stu-id="85798-109">Manually running the P-job</span></span>

1. <span data-ttu-id="85798-110">Minge jaotisse Kõik tööruumid > Jaemüügi ja kaubanduse IT.</span><span class="sxs-lookup"><span data-stu-id="85798-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="85798-111">Klõpsake valikul Turustamisgraafik.</span><span class="sxs-lookup"><span data-stu-id="85798-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="85798-112">Valige P-0001.</span><span class="sxs-lookup"><span data-stu-id="85798-112">Select P-0001.</span></span>
4. <span data-ttu-id="85798-113">Reguleerige vajadusel kanali andmebaasi rühmasid.</span><span class="sxs-lookup"><span data-stu-id="85798-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="85798-114">Klõpsake valikut Käivita kohe.</span><span class="sxs-lookup"><span data-stu-id="85798-114">Click Run now.</span></span>
6. <span data-ttu-id="85798-115">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="85798-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="85798-116">Kordiva P-töö ajastamine</span><span class="sxs-lookup"><span data-stu-id="85798-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="85798-117">Minge jaotisse Kõik tööruumid > Jaemüügi ja kaubanduse IT.</span><span class="sxs-lookup"><span data-stu-id="85798-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="85798-118">Klõpsake valikul Turustamisgraafik.</span><span class="sxs-lookup"><span data-stu-id="85798-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="85798-119">Valige P-0001.</span><span class="sxs-lookup"><span data-stu-id="85798-119">Select P-0001.</span></span>
4. <span data-ttu-id="85798-120">Klõpsake käsku Pakett-töö loomine.</span><span class="sxs-lookup"><span data-stu-id="85798-120">Click Create batch job.</span></span>
5. <span data-ttu-id="85798-121">Klõpsake käsku Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="85798-121">Click Run in the background.</span></span>
5. <span data-ttu-id="85798-122">Luba Pakett-töötlus.</span><span class="sxs-lookup"><span data-stu-id="85798-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="85798-123">Klõpsake valikut Korduvus..</span><span class="sxs-lookup"><span data-stu-id="85798-123">Click Recurrence..</span></span>
7. <span data-ttu-id="85798-124">Valige suvand Lõppkuupäev puudub.</span><span class="sxs-lookup"><span data-stu-id="85798-124">Select the No end date option.</span></span>
8. <span data-ttu-id="85798-125">Sisestage väljale Loenda käitamistevaheline intervall minutites.</span><span class="sxs-lookup"><span data-stu-id="85798-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="85798-126">Tavaliselt peaks see olema 5-10.</span><span class="sxs-lookup"><span data-stu-id="85798-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="85798-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="85798-127">Click OK.</span></span>
10. <span data-ttu-id="85798-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="85798-128">Click OK.</span></span>

<span data-ttu-id="85798-129">Tellimusi saab sünkroonida kas käsitsi, käivitades töö "Sünkrooni tellimused" või luues korduva pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="85798-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="85798-130">Käsitsi tellimuste sünkroonimise käivitamine</span><span class="sxs-lookup"><span data-stu-id="85798-130">Manually running order synchronization</span></span> 

<span data-ttu-id="85798-131">Toimige ühekordseks töö "Sünkrooni tellimused" käsitsi käivitamiseks järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="85798-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="85798-132">Avage Kõik tööruumid > Kaupluse rahandus.</span><span class="sxs-lookup"><span data-stu-id="85798-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="85798-133">Klõpsake suvandit Tellimuste sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="85798-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="85798-134">Valige väljal Organisatsiooni hierarhia suvand Kauplused piirkonniti.</span><span class="sxs-lookup"><span data-stu-id="85798-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="85798-135">Valige kindel veebipood või sõlm, kui soovite pakett-töö luua kaupluste grupi jaoks.</span><span class="sxs-lookup"><span data-stu-id="85798-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="85798-136">Klõpsake valiku lisamiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="85798-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="85798-137">Klõpsake vahekaarti Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="85798-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="85798-138">Keela Pakett-töötlus</span><span class="sxs-lookup"><span data-stu-id="85798-138">Disable Batch processing</span></span>
6. <span data-ttu-id="85798-139">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="85798-139">Click Recurrence.</span></span>
7. <span data-ttu-id="85798-140">Valige suvand Lõpeta pärast</span><span class="sxs-lookup"><span data-stu-id="85798-140">Select End After option</span></span>
8. <span data-ttu-id="85798-141">Sisestage väljale Lõpetage pärast väärtus 1.</span><span class="sxs-lookup"><span data-stu-id="85798-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="85798-142">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="85798-142">Click OK.</span></span>
10. <span data-ttu-id="85798-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="85798-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="85798-144">Korduva tellimuste sünkroonimise ajastamine</span><span class="sxs-lookup"><span data-stu-id="85798-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="85798-145">See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist veebipoe kannete jaoks müügitellimuste ja maksete loomiseks.</span><span class="sxs-lookup"><span data-stu-id="85798-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="85798-146">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="85798-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="85798-147">Avage Kõik tööruumid > Kaupluse rahandus.</span><span class="sxs-lookup"><span data-stu-id="85798-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="85798-148">Klõpsake suvandit Tellimuste sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="85798-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="85798-149">Valige väljal Organisatsiooni hierarhia suvand Kauplused piirkonniti.</span><span class="sxs-lookup"><span data-stu-id="85798-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="85798-150">Valige kindel veebipood või sõlm, kui soovite pakett-töö luua kaupluste grupi jaoks.</span><span class="sxs-lookup"><span data-stu-id="85798-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="85798-151">Klõpsake valiku lisamiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="85798-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="85798-152">Klõpsake vahekaarti Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="85798-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="85798-153">Luba Pakett-töötlus</span><span class="sxs-lookup"><span data-stu-id="85798-153">Enable Batch processing</span></span>
6. <span data-ttu-id="85798-154">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="85798-154">Click Recurrence.</span></span>
7. <span data-ttu-id="85798-155">Valige suvand Lõppkuupäev puudub.</span><span class="sxs-lookup"><span data-stu-id="85798-155">Select the No end date option.</span></span>
8. <span data-ttu-id="85798-156">Sisestage väljale Loenda käitamistevaheline intervall minutites.</span><span class="sxs-lookup"><span data-stu-id="85798-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="85798-157">Tavaliselt peaks see olema 2-20</span><span class="sxs-lookup"><span data-stu-id="85798-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="85798-158">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="85798-158">Click OK.</span></span>
10. <span data-ttu-id="85798-159">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="85798-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="85798-160">Protsessiga seotud andmeüksused</span><span class="sxs-lookup"><span data-stu-id="85798-160">Data entities involved in the process</span></span>

- <span data-ttu-id="85798-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="85798-161">RetailTransactionTable</span></span>
- <span data-ttu-id="85798-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="85798-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="85798-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="85798-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="85798-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="85798-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="85798-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="85798-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="85798-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="85798-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="85798-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="85798-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="85798-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="85798-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="85798-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="85798-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="85798-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="85798-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="85798-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="85798-171">RetailTransactionAttributeTrans</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]