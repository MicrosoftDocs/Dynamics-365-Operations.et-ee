---
title: Kliendi jaoks mahakandmise töölehe loomine
description: See ülesande juhend näitab, kuidas seadistada mahakandmiste parameetreid ja seejärel kandeid lehelt Sissenõuded, Kliendiarvete avamine ja Klient maha kanda.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44f36a12195a57e1b4cea524d2e4881f1fa7d0e9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842925"
---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="d3725-103">Kliendi jaoks mahakandmise töölehe loomine</span><span class="sxs-lookup"><span data-stu-id="d3725-103">Create a write-off journal for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d3725-104">See ülesande juhend näitab, kuidas seadistada mahakandmiste parameetreid ja seejärel kandeid lehelt Sissenõuded, Kliendiarvete avamine ja Klient maha kanda.</span><span class="sxs-lookup"><span data-stu-id="d3725-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="d3725-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="d3725-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="d3725-106">Mahakandmise parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="d3725-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="d3725-107">Tehke valik Krediit ja sissenõuded > Seadistus > Ostureskontro parameetrid.</span><span class="sxs-lookup"><span data-stu-id="d3725-107">Go to Credit and collections > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="d3725-108">Klõpsake vahekaarti Sissenõuded.</span><span class="sxs-lookup"><span data-stu-id="d3725-108">Click the Collections tab.</span></span>
3. <span data-ttu-id="d3725-109">Laiendage või ahendage jaotist Mahakandmine.</span><span class="sxs-lookup"><span data-stu-id="d3725-109">Expand or collapse the Write-off section.</span></span>
    * <span data-ttu-id="d3725-110">Mahakandmise tööleht on peažurnaal, millel on teie loodud mahakandmise kanded.</span><span class="sxs-lookup"><span data-stu-id="d3725-110">The Write-off journal is the general journal that will hold the write-off transactions that you create.</span></span>  
    * <span data-ttu-id="d3725-111">Saate lisada igale mahakandmisele põhjusekoodi.</span><span class="sxs-lookup"><span data-stu-id="d3725-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="d3725-112">Saate selle vaikeväärtuse mahakandmisel alistada.</span><span class="sxs-lookup"><span data-stu-id="d3725-112">You can override this default at the time of the write-off.</span></span>  
    * <span data-ttu-id="d3725-113">Kui soovite mahakandmisel käibemaksu algsest kandest eristada, määrake see suvandile Jah.</span><span class="sxs-lookup"><span data-stu-id="d3725-113">Set this to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="d3725-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d3725-114">Close the page.</span></span>
5. <span data-ttu-id="d3725-115">Avage Krediit ja sissenõuded > Seadistus > Kliendi sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="d3725-115">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
    * <span data-ttu-id="d3725-116">Mahakandmiskontot kasutatakse peažurnaalil kulu kontona või korrigeerimise reserveerimiseks</span><span class="sxs-lookup"><span data-stu-id="d3725-116">The write-off account will be used as the expense account or reserve adjustment in the general journal</span></span>   
6. <span data-ttu-id="d3725-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d3725-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="d3725-118">Kliendi saldo mahakandmine aegunud saldode lehelt</span><span class="sxs-lookup"><span data-stu-id="d3725-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="d3725-119">Tehke valik Krediit ja sissenõuded > Sissenõuded > Aegunud saldod.</span><span class="sxs-lookup"><span data-stu-id="d3725-119">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="d3725-120">Märkige kliendi puhul rida, mille soovite maha kanda.</span><span class="sxs-lookup"><span data-stu-id="d3725-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="d3725-121">Näiteks märkige rida, millel on ettevõte Birch Company.</span><span class="sxs-lookup"><span data-stu-id="d3725-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="d3725-122">Klõpsake toimingupaanil suvandit Sissenõudmine.</span><span class="sxs-lookup"><span data-stu-id="d3725-122">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="d3725-123">Klõpsake valikut Mahakandmine.</span><span class="sxs-lookup"><span data-stu-id="d3725-123">Click Write off.</span></span>
5. <span data-ttu-id="d3725-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d3725-124">Click OK.</span></span>
6. <span data-ttu-id="d3725-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d3725-125">Close the page.</span></span>
7. <span data-ttu-id="d3725-126">Avage Pearaamat > Töölehe sisestused > Päevaraamatud.</span><span class="sxs-lookup"><span data-stu-id="d3725-126">Go to General ledger > Journal entries > General journals.</span></span>
8. <span data-ttu-id="d3725-127">Valige töölehe partiinumber töölehe puhul, mis sisaldab teie mahakandmist.</span><span class="sxs-lookup"><span data-stu-id="d3725-127">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="d3725-128">Kliendi saldo tühistamiseks luuakse üks rida.</span><span class="sxs-lookup"><span data-stu-id="d3725-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="d3725-129">Üks või mitu rida luuakse mahakandmise sisestamiseks mahakandmiskontole.</span><span class="sxs-lookup"><span data-stu-id="d3725-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="d3725-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d3725-130">Close the page.</span></span>
10. <span data-ttu-id="d3725-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d3725-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="d3725-132">Kannete mahakandmine sissenõuete vormilt.</span><span class="sxs-lookup"><span data-stu-id="d3725-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="d3725-133">Tehke valik Krediit ja sissenõuded > Sissenõuded > Aegunud saldod.</span><span class="sxs-lookup"><span data-stu-id="d3725-133">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="d3725-134">Valige kliendi nimi, kelle kandeid soovite maha kanda.</span><span class="sxs-lookup"><span data-stu-id="d3725-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="d3725-135">Näiteks valige Cave Wholesales (US-004).</span><span class="sxs-lookup"><span data-stu-id="d3725-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="d3725-136">Märkige esimese kande rida.</span><span class="sxs-lookup"><span data-stu-id="d3725-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="d3725-137">Märkige teise kande rida.</span><span class="sxs-lookup"><span data-stu-id="d3725-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="d3725-138">Klõpsake valikut Mahakandmine.</span><span class="sxs-lookup"><span data-stu-id="d3725-138">Click Write off.</span></span>
6. <span data-ttu-id="d3725-139">Sisestage väljale Põhjuse kommentaar suvand Halvad võlad.</span><span class="sxs-lookup"><span data-stu-id="d3725-139">In the Reason comment field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="d3725-140">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d3725-140">Click OK.</span></span>
8. <span data-ttu-id="d3725-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d3725-141">Close the page.</span></span>
9. <span data-ttu-id="d3725-142">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d3725-142">Close the page.</span></span>
10. <span data-ttu-id="d3725-143">Avage Pearaamat > Töölehe sisestused > Päevaraamatud.</span><span class="sxs-lookup"><span data-stu-id="d3725-143">Go to General ledger > Journal entries > General journals.</span></span>
11. <span data-ttu-id="d3725-144">Valige töölehe partiinumber töölehe puhul, mis sisaldab teie mahakandmist.</span><span class="sxs-lookup"><span data-stu-id="d3725-144">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="d3725-145">Kliendi saldo tühistamiseks luuakse üks rida.</span><span class="sxs-lookup"><span data-stu-id="d3725-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="d3725-146">Üks või mitu rida luuakse mahakandmise sisestamiseks mahakandmiskontole.</span><span class="sxs-lookup"><span data-stu-id="d3725-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="d3725-147">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d3725-147">Close the page.</span></span>
13. <span data-ttu-id="d3725-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d3725-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="d3725-149">Arve mahakandmine lehelt Klientide arvete avamine</span><span class="sxs-lookup"><span data-stu-id="d3725-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="d3725-150">Avage Müügireskontro > Arved > Kliendiarvete avamine.</span><span class="sxs-lookup"><span data-stu-id="d3725-150">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="d3725-151">Märkige arve rida.</span><span class="sxs-lookup"><span data-stu-id="d3725-151">Mark the line for an invoice.</span></span> <span data-ttu-id="d3725-152">Näiteks, märkige rida CIV-000667 jaoks.</span><span class="sxs-lookup"><span data-stu-id="d3725-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="d3725-153">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="d3725-153">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="d3725-154">Klõpsake valikut Mahakandmine.</span><span class="sxs-lookup"><span data-stu-id="d3725-154">Click Write off.</span></span>
5. <span data-ttu-id="d3725-155">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d3725-155">Click OK.</span></span>
6. <span data-ttu-id="d3725-156">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d3725-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="d3725-157">Kliendi saldo mahakandmine kliendi lehelt</span><span class="sxs-lookup"><span data-stu-id="d3725-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="d3725-158">Avage Müügireskontro > Kliendid > Kõik kliendid.</span><span class="sxs-lookup"><span data-stu-id="d3725-158">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="d3725-159">Valige kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="d3725-159">Select a customer account.</span></span> <span data-ttu-id="d3725-160">Näiteks valige US-001 (Contoso Retail San Diego).</span><span class="sxs-lookup"><span data-stu-id="d3725-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="d3725-161">Klõpsake toimingupaanil suvandit Sissenõudmine.</span><span class="sxs-lookup"><span data-stu-id="d3725-161">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="d3725-162">Klõpsake valikut Mahakandmine.</span><span class="sxs-lookup"><span data-stu-id="d3725-162">Click Write off.</span></span>
5. <span data-ttu-id="d3725-163">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d3725-163">Click OK.</span></span>
6. <span data-ttu-id="d3725-164">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d3725-164">Close the page.</span></span>

