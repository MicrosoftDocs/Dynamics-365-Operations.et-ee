---
title: Kliendi jaoks mahakandmise töölehe loomine
description: See ülesande juhend näitab, kuidas seadistada mahakandmiste parameetreid ja seejärel kandeid lehelt Sissenõuded, Kliendiarvete avamine ja Klient maha kanda.
author: ShivamPandey-msft
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 857d3a224f35c4eeedbf4913aea14011091d5466
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823115"
---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="a698d-103">Kliendi jaoks mahakandmise töölehe loomine</span><span class="sxs-lookup"><span data-stu-id="a698d-103">Create a write-off journal for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a698d-104">See ülesande juhend näitab, kuidas seadistada mahakandmiste parameetreid ja seejärel kandeid lehelt Sissenõuded, Kliendiarvete avamine ja Klient maha kanda.</span><span class="sxs-lookup"><span data-stu-id="a698d-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="a698d-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="a698d-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="a698d-106">Mahakandmise parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="a698d-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="a698d-107">Avage **Navigeerimispaan > Moodulid > Krediidihaldus ja võlanõuded > Seadistus > Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="a698d-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="a698d-108">Klõpsake vahekaarti **Võlanõuded**.</span><span class="sxs-lookup"><span data-stu-id="a698d-108">Click the **Collections** tab.</span></span>
3. <span data-ttu-id="a698d-109">Laiendage või ahendage jaotis **Mahakandmine**.</span><span class="sxs-lookup"><span data-stu-id="a698d-109">Expand or collapse the **Write-off** section.</span></span>
    - <span data-ttu-id="a698d-110">**Mahakandmise tööleht** on päevaraamat, mis hoiustab teie loodud mahakandmiskandeid.</span><span class="sxs-lookup"><span data-stu-id="a698d-110">The **Write-off journal** is the general journal that will hold the write-off transactions that you create.</span></span>  
    - <span data-ttu-id="a698d-111">Saate lisada igale mahakandmisele põhjusekoodi.</span><span class="sxs-lookup"><span data-stu-id="a698d-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="a698d-112">Saate selle vaikeväärtuse mahakandmisel alistada.</span><span class="sxs-lookup"><span data-stu-id="a698d-112">You can override this default at the time of the write-off.</span></span>  
    - <span data-ttu-id="a698d-113">Seadke suvandi **Eralda käibemaks** väärtuseks Jah, kui soovite eraldada käibemaksu algsest kandest mahakandmisel.</span><span class="sxs-lookup"><span data-stu-id="a698d-113">Set the **Separate sales tax** to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="a698d-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a698d-114">Close the page.</span></span>
5. <span data-ttu-id="a698d-115">Avage **Krediit ja sissenõuded > Seadistus > Kliendi sisestusreeglid**.</span><span class="sxs-lookup"><span data-stu-id="a698d-115">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span> <span data-ttu-id="a698d-116">Mahakandmise kontot kasutatakse kulukontona või reservi kohandamiseks pearaamatus.</span><span class="sxs-lookup"><span data-stu-id="a698d-116">The write-off account will be used as the expense account or reserve adjustment in the general journal.</span></span>
6. <span data-ttu-id="a698d-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a698d-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="a698d-118">Kliendi saldo mahakandmine aegunud saldode lehelt</span><span class="sxs-lookup"><span data-stu-id="a698d-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="a698d-119">Avage **Krediit ja sissenõudmised > Sissenõudmised > Aegunud kliendisaldod**.</span><span class="sxs-lookup"><span data-stu-id="a698d-119">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="a698d-120">Märkige kliendi puhul rida, mille soovite maha kanda.</span><span class="sxs-lookup"><span data-stu-id="a698d-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="a698d-121">Näiteks märkige rida, millel on ettevõte Birch Company.</span><span class="sxs-lookup"><span data-stu-id="a698d-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="a698d-122">Paanil **Toimingupaan** klõpsake **Võta vastu**.</span><span class="sxs-lookup"><span data-stu-id="a698d-122">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="a698d-123">Klõpsake **Kanna maha**.</span><span class="sxs-lookup"><span data-stu-id="a698d-123">Click **Write off**.</span></span>
5. <span data-ttu-id="a698d-124">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="a698d-124">Click **OK**.</span></span>
6. <span data-ttu-id="a698d-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a698d-125">Close the page.</span></span>
7. <span data-ttu-id="a698d-126">Avage **Navigeerimispaan > Moodulid > Pearaamat > Töölehe kanded > Päevaraamatud**.</span><span class="sxs-lookup"><span data-stu-id="a698d-126">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
8. <span data-ttu-id="a698d-127">Valige töölehe partiinumber töölehe puhul, mis sisaldab teie mahakandmist.</span><span class="sxs-lookup"><span data-stu-id="a698d-127">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="a698d-128">Kliendi saldo tühistamiseks luuakse üks rida.</span><span class="sxs-lookup"><span data-stu-id="a698d-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="a698d-129">Üks või mitu rida luuakse mahakandmise sisestamiseks mahakandmiskontole.</span><span class="sxs-lookup"><span data-stu-id="a698d-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="a698d-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a698d-130">Close the page.</span></span>
10. <span data-ttu-id="a698d-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a698d-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="a698d-132">Kannete mahakandmine sissenõuete vormilt.</span><span class="sxs-lookup"><span data-stu-id="a698d-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="a698d-133">Avage **Krediit ja sissenõudmised > Sissenõudmised > Aegunud kliendisaldod**.</span><span class="sxs-lookup"><span data-stu-id="a698d-133">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="a698d-134">Valige kliendi nimi, kelle kandeid soovite maha kanda.</span><span class="sxs-lookup"><span data-stu-id="a698d-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="a698d-135">Näiteks valige Cave Wholesales (US-004).</span><span class="sxs-lookup"><span data-stu-id="a698d-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="a698d-136">Märkige esimese kande rida.</span><span class="sxs-lookup"><span data-stu-id="a698d-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="a698d-137">Märkige teise kande rida.</span><span class="sxs-lookup"><span data-stu-id="a698d-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="a698d-138">Klõpsake **Kanna maha**.</span><span class="sxs-lookup"><span data-stu-id="a698d-138">Click **Write off**.</span></span>
6. <span data-ttu-id="a698d-139">Väljale **Põhjuse kommentaar** sisestage "Halvad võlad".</span><span class="sxs-lookup"><span data-stu-id="a698d-139">In the **Reason comment** field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="a698d-140">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="a698d-140">Click **OK**.</span></span>
8. <span data-ttu-id="a698d-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a698d-141">Close the page.</span></span>
9. <span data-ttu-id="a698d-142">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a698d-142">Close the page.</span></span>
10. <span data-ttu-id="a698d-143">Avage **Pearaamat > Töölehe kanded > Päevaraamatud**.</span><span class="sxs-lookup"><span data-stu-id="a698d-143">Go to **General ledger > Journal entries > General journals**.</span></span>
11. <span data-ttu-id="a698d-144">Valige töölehe partiinumber töölehe puhul, mis sisaldab teie mahakandmist.</span><span class="sxs-lookup"><span data-stu-id="a698d-144">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="a698d-145">Kliendi saldo tühistamiseks luuakse üks rida.</span><span class="sxs-lookup"><span data-stu-id="a698d-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="a698d-146">Üks või mitu rida luuakse mahakandmise sisestamiseks mahakandmiskontole.</span><span class="sxs-lookup"><span data-stu-id="a698d-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="a698d-147">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a698d-147">Close the page.</span></span>
13. <span data-ttu-id="a698d-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a698d-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="a698d-149">Arve mahakandmine lehelt Klientide arvete avamine</span><span class="sxs-lookup"><span data-stu-id="a698d-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="a698d-150">Avage **Navigeerimispaan > Moodulid > Müügireskontro > Arved > Avatud kliendiarved**.</span><span class="sxs-lookup"><span data-stu-id="a698d-150">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Open customer invoices**.</span></span>
2. <span data-ttu-id="a698d-151">Märkige arve rida.</span><span class="sxs-lookup"><span data-stu-id="a698d-151">Mark the line for an invoice.</span></span> <span data-ttu-id="a698d-152">Näiteks, märkige rida CIV-000667 jaoks.</span><span class="sxs-lookup"><span data-stu-id="a698d-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="a698d-153">Paanil **Toimingupaan** klõpsake **Arve**.</span><span class="sxs-lookup"><span data-stu-id="a698d-153">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="a698d-154">Klõpsake **Kanna maha**.</span><span class="sxs-lookup"><span data-stu-id="a698d-154">Click **Write off**.</span></span>
5. <span data-ttu-id="a698d-155">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="a698d-155">Click **OK**.</span></span>
6. <span data-ttu-id="a698d-156">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a698d-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="a698d-157">Kliendi saldo mahakandmine kliendi lehelt</span><span class="sxs-lookup"><span data-stu-id="a698d-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="a698d-158">Avage **Müügireskontro > Kliendid > Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="a698d-158">Go to **Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="a698d-159">Valige kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="a698d-159">Select a customer account.</span></span> <span data-ttu-id="a698d-160">Näiteks valige US-001 (Contoso Retail San Diego).</span><span class="sxs-lookup"><span data-stu-id="a698d-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="a698d-161">Paanil **Toimingupaan** klõpsake **Võta vastu**.</span><span class="sxs-lookup"><span data-stu-id="a698d-161">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="a698d-162">Klõpsake **Kanna maha**.</span><span class="sxs-lookup"><span data-stu-id="a698d-162">Click **Write off**.</span></span>
5. <span data-ttu-id="a698d-163">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="a698d-163">Click **OK**.</span></span>
6. <span data-ttu-id="a698d-164">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a698d-164">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]