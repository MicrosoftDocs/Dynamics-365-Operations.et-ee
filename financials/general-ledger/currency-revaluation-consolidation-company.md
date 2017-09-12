---
title: "Valuuta ümberarvutamine konsolideeritavas ettevõttes"
description: 
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 643af8d771685fe8fd652b353d41f2679e0bef8b
ms.contentlocale: et-ee
ms.lasthandoff: 07/18/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="4fd74-102">Valuuta ümberarvutamine konsolideeritavas ettevõttes</span><span class="sxs-lookup"><span data-stu-id="4fd74-102">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="4fd74-103">Kui konsolodeerite andmeid ühelt arveldusvaluutalt teisele, peate siiski käivitama valuuta ümberarvestamise, kui vahetuskurssides on muutusi, et teie konto saldo arvestataks õigesti ümber.</span><span class="sxs-lookup"><span data-stu-id="4fd74-103">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="4fd74-104">Kasutage algsel andmete konsolideerimisel vahekaarti **Valuuta teisendamine**, et valida algsed vahetuskursid ümberarvestamiseks konsolideerimisprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="4fd74-104">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="4fd74-105">Pärast uue vahetuskursi sisestamist (näiteks järgmisel kuul) peate konto saldo ümber arvutama.</span><span class="sxs-lookup"><span data-stu-id="4fd74-105">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="4fd74-106">Realiseerimata kasumeid või kahjumeid värskendatakse vastavalt uue vahetuskursi ja kuupäeva alusel.</span><span class="sxs-lookup"><span data-stu-id="4fd74-106">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="4fd74-107">Järgnev näide illustreerib raamatupidamiskandeid, mis luuakse protsessi ajal.</span><span class="sxs-lookup"><span data-stu-id="4fd74-107">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="4fd74-108">Ettevõtte seadistus</span><span class="sxs-lookup"><span data-stu-id="4fd74-108">Company setup</span></span>
-   <span data-ttu-id="4fd74-109">**Lähte-/töötav ettevõte (USMF)** – USA dollareid (USD) kasutatakse arvestus- ja aruandlusvaluutana.</span><span class="sxs-lookup"><span data-stu-id="4fd74-109">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="4fd74-110">**Konsolideeritud ettevõte (CON)** – eurosid (EUR) kasutatakse arvestus- ja aruandlusvaluutana.</span><span class="sxs-lookup"><span data-stu-id="4fd74-110">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="4fd74-111">**Realiseeritud kasum** – pearaamatukonto 801500</span><span class="sxs-lookup"><span data-stu-id="4fd74-111">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="4fd74-112">**Realiseeritud kahjum** – pearaamatukonto 801600</span><span class="sxs-lookup"><span data-stu-id="4fd74-112">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="4fd74-113">**Realiseerimata kasum** – pearaamatukonto 801600</span><span class="sxs-lookup"><span data-stu-id="4fd74-113">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="4fd74-114">**Realiseerimata kahjum** – pearaamatukonto 801400</span><span class="sxs-lookup"><span data-stu-id="4fd74-114">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="4fd74-115">Algsed kanded</span><span class="sxs-lookup"><span data-stu-id="4fd74-115">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="4fd74-116">Kassaorderi kanded USMF-is</span><span class="sxs-lookup"><span data-stu-id="4fd74-116">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="4fd74-117">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="4fd74-117">Date</span></span>       | <span data-ttu-id="4fd74-118">Pearaamatu konto</span><span class="sxs-lookup"><span data-stu-id="4fd74-118">Ledger account</span></span>               | <span data-ttu-id="4fd74-119">Valuuta</span><span class="sxs-lookup"><span data-stu-id="4fd74-119">Currency</span></span> | <span data-ttu-id="4fd74-120">Summa</span><span class="sxs-lookup"><span data-stu-id="4fd74-120">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="4fd74-121">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="4fd74-121">10/11/2015</span></span> | <span data-ttu-id="4fd74-122">110110 – sularaha</span><span class="sxs-lookup"><span data-stu-id="4fd74-122">110110 – Cash</span></span>                | <span data-ttu-id="4fd74-123">USA dollar</span><span class="sxs-lookup"><span data-stu-id="4fd74-123">USD</span></span>      | <span data-ttu-id="4fd74-124">500</span><span class="sxs-lookup"><span data-stu-id="4fd74-124">500</span></span>    |
| <span data-ttu-id="4fd74-125">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="4fd74-125">10/11/2015</span></span> | <span data-ttu-id="4fd74-126">130100 – müügireskontro</span><span class="sxs-lookup"><span data-stu-id="4fd74-126">130100 – Accounts Receivable</span></span> | <span data-ttu-id="4fd74-127">USA dollar</span><span class="sxs-lookup"><span data-stu-id="4fd74-127">USD</span></span>      | <span data-ttu-id="4fd74-128">–500</span><span class="sxs-lookup"><span data-stu-id="4fd74-128">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="4fd74-129">Vahetuskursid</span><span class="sxs-lookup"><span data-stu-id="4fd74-129">Exchange rates</span></span>
| <span data-ttu-id="4fd74-130">Valuutast</span><span class="sxs-lookup"><span data-stu-id="4fd74-130">From currency</span></span> | <span data-ttu-id="4fd74-131">Valuutaks</span><span class="sxs-lookup"><span data-stu-id="4fd74-131">To currency</span></span> | <span data-ttu-id="4fd74-132">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="4fd74-132">Start date</span></span> | <span data-ttu-id="4fd74-133">Vahetuskurss</span><span class="sxs-lookup"><span data-stu-id="4fd74-133">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="4fd74-134"> eurot</span><span class="sxs-lookup"><span data-stu-id="4fd74-134">EUR</span></span>           | <span data-ttu-id="4fd74-135">USA dollar</span><span class="sxs-lookup"><span data-stu-id="4fd74-135">USD</span></span>         | <span data-ttu-id="4fd74-136">1.10.2015</span><span class="sxs-lookup"><span data-stu-id="4fd74-136">10/1/2015</span></span>  | <span data-ttu-id="4fd74-137">200</span><span class="sxs-lookup"><span data-stu-id="4fd74-137">200</span></span>           |
| <span data-ttu-id="4fd74-138"> eurot</span><span class="sxs-lookup"><span data-stu-id="4fd74-138">EUR</span></span>           | <span data-ttu-id="4fd74-139">USA dollar</span><span class="sxs-lookup"><span data-stu-id="4fd74-139">USD</span></span>         | <span data-ttu-id="4fd74-140">1.11.2015</span><span class="sxs-lookup"><span data-stu-id="4fd74-140">11/1/2015</span></span>  | <span data-ttu-id="4fd74-141">150</span><span class="sxs-lookup"><span data-stu-id="4fd74-141">150</span></span>           |
| <span data-ttu-id="4fd74-142"> eurot</span><span class="sxs-lookup"><span data-stu-id="4fd74-142">EUR</span></span>           | <span data-ttu-id="4fd74-143">USA dollar</span><span class="sxs-lookup"><span data-stu-id="4fd74-143">USD</span></span>         | <span data-ttu-id="4fd74-144">1.12.2012</span><span class="sxs-lookup"><span data-stu-id="4fd74-144">12/1/2012</span></span>  | <span data-ttu-id="4fd74-145">100</span><span class="sxs-lookup"><span data-stu-id="4fd74-145">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="4fd74-146">2015. aasta oktoobri konsolideerimine</span><span class="sxs-lookup"><span data-stu-id="4fd74-146">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="4fd74-147">Konsolideeritava ettevõtte saldod</span><span class="sxs-lookup"><span data-stu-id="4fd74-147">Balances in the consolidation company</span></span>

| <span data-ttu-id="4fd74-148">Pearaamatu konto</span><span class="sxs-lookup"><span data-stu-id="4fd74-148">Ledger account</span></span> | <span data-ttu-id="4fd74-149">Valuuta</span><span class="sxs-lookup"><span data-stu-id="4fd74-149">Currency</span></span> | <span data-ttu-id="4fd74-150">Summa</span><span class="sxs-lookup"><span data-stu-id="4fd74-150">Amount</span></span> | <span data-ttu-id="4fd74-151">Arvutus</span><span class="sxs-lookup"><span data-stu-id="4fd74-151">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="4fd74-152">110110</span><span class="sxs-lookup"><span data-stu-id="4fd74-152">110110</span></span>         | <span data-ttu-id="4fd74-153"> eurot</span><span class="sxs-lookup"><span data-stu-id="4fd74-153">EUR</span></span>      | <span data-ttu-id="4fd74-154">250</span><span class="sxs-lookup"><span data-stu-id="4fd74-154">250</span></span>    | <span data-ttu-id="4fd74-155">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="4fd74-155">500 USD × 50%</span></span>  |
| <span data-ttu-id="4fd74-156">130100</span><span class="sxs-lookup"><span data-stu-id="4fd74-156">130100</span></span>         | <span data-ttu-id="4fd74-157"> eurot</span><span class="sxs-lookup"><span data-stu-id="4fd74-157">EUR</span></span>      | <span data-ttu-id="4fd74-158">–250</span><span class="sxs-lookup"><span data-stu-id="4fd74-158">-250</span></span>   | <span data-ttu-id="4fd74-159">–500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="4fd74-159">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="4fd74-160">Perioodi 1. oktoober 2015 kuni 30. november 2015 kontode valuuta ümberarvutamine</span><span class="sxs-lookup"><span data-stu-id="4fd74-160">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="4fd74-161">Konsolideeritava ettevõtte saldod</span><span class="sxs-lookup"><span data-stu-id="4fd74-161">Balances in the consolidation company</span></span>

| <span data-ttu-id="4fd74-162">Pearaamatu konto</span><span class="sxs-lookup"><span data-stu-id="4fd74-162">Ledger account</span></span> | <span data-ttu-id="4fd74-163">Valuuta</span><span class="sxs-lookup"><span data-stu-id="4fd74-163">Currency</span></span> | <span data-ttu-id="4fd74-164">Summa</span><span class="sxs-lookup"><span data-stu-id="4fd74-164">Amount</span></span>  | <span data-ttu-id="4fd74-165">Arvutus</span><span class="sxs-lookup"><span data-stu-id="4fd74-165">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="4fd74-166">110110</span><span class="sxs-lookup"><span data-stu-id="4fd74-166">110110</span></span>         | <span data-ttu-id="4fd74-167"> eurot</span><span class="sxs-lookup"><span data-stu-id="4fd74-167">EUR</span></span>      | <span data-ttu-id="4fd74-168">333,33</span><span class="sxs-lookup"><span data-stu-id="4fd74-168">333.33</span></span>  | <span data-ttu-id="4fd74-169">Algne summa 500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="4fd74-169">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="4fd74-170">130100</span><span class="sxs-lookup"><span data-stu-id="4fd74-170">130100</span></span>         | <span data-ttu-id="4fd74-171"> eurot</span><span class="sxs-lookup"><span data-stu-id="4fd74-171">EUR</span></span>      | <span data-ttu-id="4fd74-172">–333,33</span><span class="sxs-lookup"><span data-stu-id="4fd74-172">-333.33</span></span> | <span data-ttu-id="4fd74-173">Algne summa –500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="4fd74-173">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="4fd74-174">801400</span><span class="sxs-lookup"><span data-stu-id="4fd74-174">801400</span></span>         | <span data-ttu-id="4fd74-175"> eurot</span><span class="sxs-lookup"><span data-stu-id="4fd74-175">EUR</span></span>      | <span data-ttu-id="4fd74-176">83,33</span><span class="sxs-lookup"><span data-stu-id="4fd74-176">83.33</span></span>   | <span data-ttu-id="4fd74-177">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="4fd74-177">333.33 – 250</span></span>                       |
| <span data-ttu-id="4fd74-178">801600</span><span class="sxs-lookup"><span data-stu-id="4fd74-178">801600</span></span>         | <span data-ttu-id="4fd74-179"> eurot</span><span class="sxs-lookup"><span data-stu-id="4fd74-179">EUR</span></span>      | <span data-ttu-id="4fd74-180">–83,33</span><span class="sxs-lookup"><span data-stu-id="4fd74-180">-83.33</span></span>  | <span data-ttu-id="4fd74-181">–333,33 – (–250)</span><span class="sxs-lookup"><span data-stu-id="4fd74-181">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="4fd74-182">Näete aruandlusvaluuta summade puhul lisakandeid.</span><span class="sxs-lookup"><span data-stu-id="4fd74-182">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="4fd74-183">Perioodi 1. oktoober 2015 kuni 31. detsember 2015 kontode valuuta ümberarvutamine</span><span class="sxs-lookup"><span data-stu-id="4fd74-183">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="4fd74-184">Konsolideeritava ettevõtte saldod</span><span class="sxs-lookup"><span data-stu-id="4fd74-184">Balances in the consolidation company</span></span>

| <span data-ttu-id="4fd74-185">Pearaamatu konto</span><span class="sxs-lookup"><span data-stu-id="4fd74-185">Ledger account</span></span> | <span data-ttu-id="4fd74-186">Valuuta</span><span class="sxs-lookup"><span data-stu-id="4fd74-186">Currency</span></span> | <span data-ttu-id="4fd74-187">Summa</span><span class="sxs-lookup"><span data-stu-id="4fd74-187">Amount</span></span>  | <span data-ttu-id="4fd74-188">Arvutus</span><span class="sxs-lookup"><span data-stu-id="4fd74-188">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="4fd74-189">110110</span><span class="sxs-lookup"><span data-stu-id="4fd74-189">110110</span></span>         | <span data-ttu-id="4fd74-190"> eurot</span><span class="sxs-lookup"><span data-stu-id="4fd74-190">EUR</span></span>      | <span data-ttu-id="4fd74-191">500,00</span><span class="sxs-lookup"><span data-stu-id="4fd74-191">500.00</span></span>  | <span data-ttu-id="4fd74-192">Algne summa 500 × 1</span><span class="sxs-lookup"><span data-stu-id="4fd74-192">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="4fd74-193">130100</span><span class="sxs-lookup"><span data-stu-id="4fd74-193">130100</span></span>         | <span data-ttu-id="4fd74-194"> eurot</span><span class="sxs-lookup"><span data-stu-id="4fd74-194">EUR</span></span>      | <span data-ttu-id="4fd74-195">–500,00</span><span class="sxs-lookup"><span data-stu-id="4fd74-195">-500.00</span></span> | <span data-ttu-id="4fd74-196">Algne summa –500 × 1</span><span class="sxs-lookup"><span data-stu-id="4fd74-196">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="4fd74-197">801400</span><span class="sxs-lookup"><span data-stu-id="4fd74-197">801400</span></span>         | <span data-ttu-id="4fd74-198"> eurot</span><span class="sxs-lookup"><span data-stu-id="4fd74-198">EUR</span></span>      | <span data-ttu-id="4fd74-199">250</span><span class="sxs-lookup"><span data-stu-id="4fd74-199">250</span></span>     | <span data-ttu-id="4fd74-200">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="4fd74-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="4fd74-201">801600</span><span class="sxs-lookup"><span data-stu-id="4fd74-201">801600</span></span>         | <span data-ttu-id="4fd74-202"> eurot</span><span class="sxs-lookup"><span data-stu-id="4fd74-202">EUR</span></span>      | <span data-ttu-id="4fd74-203">–250</span><span class="sxs-lookup"><span data-stu-id="4fd74-203">-250</span></span>    | <span data-ttu-id="4fd74-204">–500 – (–333,33) = –166,67 –166,67 + (–83,33) = –250</span><span class="sxs-lookup"><span data-stu-id="4fd74-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






