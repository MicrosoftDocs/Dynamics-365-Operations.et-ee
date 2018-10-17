---
title: "Valuuta ümberarvutamine konsolideeritavas ettevõttes"
description: "Selles teemas kirjeldatakse valuuta ümberhindamist konsolideeritud ettevõttes."
author: ShylaThompson
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ad0083018d2734cb1e36cbf5f94105376c57cdf9
ms.openlocfilehash: 76290564037ab6f5c7a1cd4508a819bd603e8148
ms.contentlocale: et-ee
ms.lasthandoff: 10/02/2018

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="07219-103">Valuuta ümberarvutamine konsolideeritavas ettevõttes</span><span class="sxs-lookup"><span data-stu-id="07219-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07219-104">Kui konsolodeerite andmeid ühelt arveldusvaluutalt teisele, peate siiski käivitama valuuta ümberarvestamise, kui vahetuskurssides on muutusi, et teie konto saldo arvestataks õigesti ümber.</span><span class="sxs-lookup"><span data-stu-id="07219-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="07219-105">Kasutage algsel andmete konsolideerimisel vahekaarti **Valuuta teisendamine**, et valida algsed vahetuskursid ümberarvestamiseks konsolideerimisprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="07219-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="07219-106">Pärast uue vahetuskursi sisestamist (näiteks järgmisel kuul) peate konto saldo ümber arvutama.</span><span class="sxs-lookup"><span data-stu-id="07219-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="07219-107">Realiseerimata kasumeid või kahjumeid värskendatakse vastavalt uue vahetuskursi ja kuupäeva alusel.</span><span class="sxs-lookup"><span data-stu-id="07219-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="07219-108">Järgnev näide illustreerib raamatupidamiskandeid, mis luuakse protsessi ajal.</span><span class="sxs-lookup"><span data-stu-id="07219-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="07219-109">Ettevõtte seadistus</span><span class="sxs-lookup"><span data-stu-id="07219-109">Company setup</span></span>
-   <span data-ttu-id="07219-110">**Lähte-/töötav ettevõte (USMF)** – USA dollareid (USD) kasutatakse arvestus- ja aruandlusvaluutana.</span><span class="sxs-lookup"><span data-stu-id="07219-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="07219-111">**Konsolideeritud ettevõte (CON)** – eurosid (EUR) kasutatakse arvestus- ja aruandlusvaluutana.</span><span class="sxs-lookup"><span data-stu-id="07219-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="07219-112">**Realiseeritud kasum** – pearaamatukonto 801500</span><span class="sxs-lookup"><span data-stu-id="07219-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="07219-113">**Realiseeritud kahjum** – pearaamatukonto 801600</span><span class="sxs-lookup"><span data-stu-id="07219-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="07219-114">**Realiseerimata kasum** – pearaamatukonto 801600</span><span class="sxs-lookup"><span data-stu-id="07219-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="07219-115">**Realiseerimata kahjum** – pearaamatukonto 801400</span><span class="sxs-lookup"><span data-stu-id="07219-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="07219-116">Algsed kanded</span><span class="sxs-lookup"><span data-stu-id="07219-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="07219-117">Kassaorderi kanded USMF-is</span><span class="sxs-lookup"><span data-stu-id="07219-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="07219-118">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="07219-118">Date</span></span>       | <span data-ttu-id="07219-119">Pearaamatu konto</span><span class="sxs-lookup"><span data-stu-id="07219-119">Ledger account</span></span>               | <span data-ttu-id="07219-120">Valuuta</span><span class="sxs-lookup"><span data-stu-id="07219-120">Currency</span></span> | <span data-ttu-id="07219-121">Summa</span><span class="sxs-lookup"><span data-stu-id="07219-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="07219-122">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="07219-122">10/11/2015</span></span> | <span data-ttu-id="07219-123">110110 – sularaha</span><span class="sxs-lookup"><span data-stu-id="07219-123">110110 – Cash</span></span>                | <span data-ttu-id="07219-124">USA dollar</span><span class="sxs-lookup"><span data-stu-id="07219-124">USD</span></span>      | <span data-ttu-id="07219-125">500</span><span class="sxs-lookup"><span data-stu-id="07219-125">500</span></span>    |
| <span data-ttu-id="07219-126">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="07219-126">10/11/2015</span></span> | <span data-ttu-id="07219-127">130100 – müügireskontro</span><span class="sxs-lookup"><span data-stu-id="07219-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="07219-128">USA dollar</span><span class="sxs-lookup"><span data-stu-id="07219-128">USD</span></span>      | <span data-ttu-id="07219-129">–500</span><span class="sxs-lookup"><span data-stu-id="07219-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="07219-130">Vahetuskursid</span><span class="sxs-lookup"><span data-stu-id="07219-130">Exchange rates</span></span>

| <span data-ttu-id="07219-131">Valuutast</span><span class="sxs-lookup"><span data-stu-id="07219-131">From currency</span></span> | <span data-ttu-id="07219-132">Valuutaks</span><span class="sxs-lookup"><span data-stu-id="07219-132">To currency</span></span> | <span data-ttu-id="07219-133">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="07219-133">Start date</span></span> | <span data-ttu-id="07219-134">Vahetuskurss</span><span class="sxs-lookup"><span data-stu-id="07219-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="07219-135"> eurot</span><span class="sxs-lookup"><span data-stu-id="07219-135">EUR</span></span>           | <span data-ttu-id="07219-136">USA dollar</span><span class="sxs-lookup"><span data-stu-id="07219-136">USD</span></span>         | <span data-ttu-id="07219-137">1.10.2015</span><span class="sxs-lookup"><span data-stu-id="07219-137">10/1/2015</span></span>  | <span data-ttu-id="07219-138">200</span><span class="sxs-lookup"><span data-stu-id="07219-138">200</span></span>           |
| <span data-ttu-id="07219-139"> eurot</span><span class="sxs-lookup"><span data-stu-id="07219-139">EUR</span></span>           | <span data-ttu-id="07219-140">USA dollar</span><span class="sxs-lookup"><span data-stu-id="07219-140">USD</span></span>         | <span data-ttu-id="07219-141">1.11.2015</span><span class="sxs-lookup"><span data-stu-id="07219-141">11/1/2015</span></span>  | <span data-ttu-id="07219-142">150</span><span class="sxs-lookup"><span data-stu-id="07219-142">150</span></span>           |
| <span data-ttu-id="07219-143"> eurot</span><span class="sxs-lookup"><span data-stu-id="07219-143">EUR</span></span>           | <span data-ttu-id="07219-144">USA dollar</span><span class="sxs-lookup"><span data-stu-id="07219-144">USD</span></span>         | <span data-ttu-id="07219-145">1.12.2012</span><span class="sxs-lookup"><span data-stu-id="07219-145">12/1/2012</span></span>  | <span data-ttu-id="07219-146">100</span><span class="sxs-lookup"><span data-stu-id="07219-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="07219-147">2015. aasta oktoobri konsolideerimine</span><span class="sxs-lookup"><span data-stu-id="07219-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="07219-148">Konsolideeritava ettevõtte saldod</span><span class="sxs-lookup"><span data-stu-id="07219-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="07219-149">Pearaamatu konto</span><span class="sxs-lookup"><span data-stu-id="07219-149">Ledger account</span></span> | <span data-ttu-id="07219-150">Valuuta</span><span class="sxs-lookup"><span data-stu-id="07219-150">Currency</span></span> | <span data-ttu-id="07219-151">Summa</span><span class="sxs-lookup"><span data-stu-id="07219-151">Amount</span></span> | <span data-ttu-id="07219-152">Arvutus</span><span class="sxs-lookup"><span data-stu-id="07219-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="07219-153">110110</span><span class="sxs-lookup"><span data-stu-id="07219-153">110110</span></span>         | <span data-ttu-id="07219-154"> eurot</span><span class="sxs-lookup"><span data-stu-id="07219-154">EUR</span></span>      | <span data-ttu-id="07219-155">250</span><span class="sxs-lookup"><span data-stu-id="07219-155">250</span></span>    | <span data-ttu-id="07219-156">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="07219-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="07219-157">130100</span><span class="sxs-lookup"><span data-stu-id="07219-157">130100</span></span>         | <span data-ttu-id="07219-158"> eurot</span><span class="sxs-lookup"><span data-stu-id="07219-158">EUR</span></span>      | <span data-ttu-id="07219-159">–250</span><span class="sxs-lookup"><span data-stu-id="07219-159">-250</span></span>   | <span data-ttu-id="07219-160">–500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="07219-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="07219-161">Perioodi 1. oktoober 2015 kuni 30. november 2015 kontode valuuta ümberarvutamine</span><span class="sxs-lookup"><span data-stu-id="07219-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="07219-162">Konsolideeritava ettevõtte saldod</span><span class="sxs-lookup"><span data-stu-id="07219-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="07219-163">Pearaamatu konto</span><span class="sxs-lookup"><span data-stu-id="07219-163">Ledger account</span></span> | <span data-ttu-id="07219-164">Valuuta</span><span class="sxs-lookup"><span data-stu-id="07219-164">Currency</span></span> | <span data-ttu-id="07219-165">Summa</span><span class="sxs-lookup"><span data-stu-id="07219-165">Amount</span></span>  | <span data-ttu-id="07219-166">Arvutus</span><span class="sxs-lookup"><span data-stu-id="07219-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="07219-167">110110</span><span class="sxs-lookup"><span data-stu-id="07219-167">110110</span></span>         | <span data-ttu-id="07219-168"> eurot</span><span class="sxs-lookup"><span data-stu-id="07219-168">EUR</span></span>      | <span data-ttu-id="07219-169">333,33</span><span class="sxs-lookup"><span data-stu-id="07219-169">333.33</span></span>  | <span data-ttu-id="07219-170">Algne summa 500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="07219-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="07219-171">130100</span><span class="sxs-lookup"><span data-stu-id="07219-171">130100</span></span>         | <span data-ttu-id="07219-172"> eurot</span><span class="sxs-lookup"><span data-stu-id="07219-172">EUR</span></span>      | <span data-ttu-id="07219-173">–333,33</span><span class="sxs-lookup"><span data-stu-id="07219-173">-333.33</span></span> | <span data-ttu-id="07219-174">Algne summa –500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="07219-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="07219-175">801400</span><span class="sxs-lookup"><span data-stu-id="07219-175">801400</span></span>         | <span data-ttu-id="07219-176"> eurot</span><span class="sxs-lookup"><span data-stu-id="07219-176">EUR</span></span>      | <span data-ttu-id="07219-177">83,33</span><span class="sxs-lookup"><span data-stu-id="07219-177">83.33</span></span>   | <span data-ttu-id="07219-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="07219-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="07219-179">801600</span><span class="sxs-lookup"><span data-stu-id="07219-179">801600</span></span>         | <span data-ttu-id="07219-180"> eurot</span><span class="sxs-lookup"><span data-stu-id="07219-180">EUR</span></span>      | <span data-ttu-id="07219-181">–83,33</span><span class="sxs-lookup"><span data-stu-id="07219-181">-83.33</span></span>  | <span data-ttu-id="07219-182">–333,33 – (–250)</span><span class="sxs-lookup"><span data-stu-id="07219-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="07219-183">Näete aruandlusvaluuta summade puhul lisakandeid.</span><span class="sxs-lookup"><span data-stu-id="07219-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="07219-184">Perioodi 1. oktoober 2015 kuni 31. detsember 2015 kontode valuuta ümberarvutamine</span><span class="sxs-lookup"><span data-stu-id="07219-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="07219-185">Konsolideeritava ettevõtte saldod</span><span class="sxs-lookup"><span data-stu-id="07219-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="07219-186">Pearaamatu konto</span><span class="sxs-lookup"><span data-stu-id="07219-186">Ledger account</span></span> | <span data-ttu-id="07219-187">Valuuta</span><span class="sxs-lookup"><span data-stu-id="07219-187">Currency</span></span> | <span data-ttu-id="07219-188">Summa</span><span class="sxs-lookup"><span data-stu-id="07219-188">Amount</span></span>  | <span data-ttu-id="07219-189">Arvutus</span><span class="sxs-lookup"><span data-stu-id="07219-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="07219-190">110110</span><span class="sxs-lookup"><span data-stu-id="07219-190">110110</span></span>         | <span data-ttu-id="07219-191"> eurot</span><span class="sxs-lookup"><span data-stu-id="07219-191">EUR</span></span>      | <span data-ttu-id="07219-192">500,00</span><span class="sxs-lookup"><span data-stu-id="07219-192">500.00</span></span>  | <span data-ttu-id="07219-193">Algne summa 500 × 1</span><span class="sxs-lookup"><span data-stu-id="07219-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="07219-194">130100</span><span class="sxs-lookup"><span data-stu-id="07219-194">130100</span></span>         | <span data-ttu-id="07219-195"> eurot</span><span class="sxs-lookup"><span data-stu-id="07219-195">EUR</span></span>      | <span data-ttu-id="07219-196">–500,00</span><span class="sxs-lookup"><span data-stu-id="07219-196">-500.00</span></span> | <span data-ttu-id="07219-197">Algne summa –500 × 1</span><span class="sxs-lookup"><span data-stu-id="07219-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="07219-198">801400</span><span class="sxs-lookup"><span data-stu-id="07219-198">801400</span></span>         | <span data-ttu-id="07219-199"> eurot</span><span class="sxs-lookup"><span data-stu-id="07219-199">EUR</span></span>      | <span data-ttu-id="07219-200">250</span><span class="sxs-lookup"><span data-stu-id="07219-200">250</span></span>     | <span data-ttu-id="07219-201">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="07219-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="07219-202">801600</span><span class="sxs-lookup"><span data-stu-id="07219-202">801600</span></span>         | <span data-ttu-id="07219-203"> eurot</span><span class="sxs-lookup"><span data-stu-id="07219-203">EUR</span></span>      | <span data-ttu-id="07219-204">–250</span><span class="sxs-lookup"><span data-stu-id="07219-204">-250</span></span>    | <span data-ttu-id="07219-205">–500 – (–333,33) = –166,67 –166,67 + (–83,33) = –250</span><span class="sxs-lookup"><span data-stu-id="07219-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






