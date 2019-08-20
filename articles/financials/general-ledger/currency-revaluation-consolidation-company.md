---
title: Valuuta ümberarvutamine konsolideeritavas ettevõttes
description: Selles teemas kirjeldatakse valuuta ümberhindamist konsolideeritud ettevõttes.
author: ShylaThompson
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b7f0a18910cbaed382971e47eb688c075e7e6a5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839420"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="a6f61-103">Valuuta ümberarvutamine konsolideeritavas ettevõttes</span><span class="sxs-lookup"><span data-stu-id="a6f61-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6f61-104">Kui konsolodeerite andmeid ühelt arveldusvaluutalt teisele, peate siiski käivitama valuuta ümberarvestamise, kui vahetuskurssides on muutusi, et teie konto saldo arvestataks õigesti ümber.</span><span class="sxs-lookup"><span data-stu-id="a6f61-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="a6f61-105">Kasutage algsel andmete konsolideerimisel vahekaarti **Valuuta teisendamine**, et valida algsed vahetuskursid ümberarvestamiseks konsolideerimisprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="a6f61-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="a6f61-106">Pärast uue vahetuskursi sisestamist (näiteks järgmisel kuul) peate konto saldo ümber arvutama.</span><span class="sxs-lookup"><span data-stu-id="a6f61-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="a6f61-107">Realiseerimata kasumeid või kahjumeid värskendatakse vastavalt uue vahetuskursi ja kuupäeva alusel.</span><span class="sxs-lookup"><span data-stu-id="a6f61-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="a6f61-108">Järgnev näide illustreerib raamatupidamiskandeid, mis luuakse protsessi ajal.</span><span class="sxs-lookup"><span data-stu-id="a6f61-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="a6f61-109">Ettevõtte seadistus</span><span class="sxs-lookup"><span data-stu-id="a6f61-109">Company setup</span></span>
-   <span data-ttu-id="a6f61-110">**Lähte-/töötav ettevõte (USMF)** – USA dollareid (USD) kasutatakse arvestus- ja aruandlusvaluutana.</span><span class="sxs-lookup"><span data-stu-id="a6f61-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="a6f61-111">**Konsolideeritud ettevõte (CON)** – eurosid (EUR) kasutatakse arvestus- ja aruandlusvaluutana.</span><span class="sxs-lookup"><span data-stu-id="a6f61-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="a6f61-112">**Realiseeritud kasum** – pearaamatukonto 801500</span><span class="sxs-lookup"><span data-stu-id="a6f61-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="a6f61-113">**Realiseeritud kahjum** – pearaamatukonto 801600</span><span class="sxs-lookup"><span data-stu-id="a6f61-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="a6f61-114">**Realiseerimata kasum** – pearaamatukonto 801600</span><span class="sxs-lookup"><span data-stu-id="a6f61-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="a6f61-115">**Realiseerimata kahjum** – pearaamatukonto 801400</span><span class="sxs-lookup"><span data-stu-id="a6f61-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="a6f61-116">Algsed kanded</span><span class="sxs-lookup"><span data-stu-id="a6f61-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="a6f61-117">Kassaorderi kanded USMF-is</span><span class="sxs-lookup"><span data-stu-id="a6f61-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="a6f61-118">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="a6f61-118">Date</span></span>       | <span data-ttu-id="a6f61-119">Pearaamatu konto</span><span class="sxs-lookup"><span data-stu-id="a6f61-119">Ledger account</span></span>               | <span data-ttu-id="a6f61-120">Valuuta</span><span class="sxs-lookup"><span data-stu-id="a6f61-120">Currency</span></span> | <span data-ttu-id="a6f61-121">Summa</span><span class="sxs-lookup"><span data-stu-id="a6f61-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="a6f61-122">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="a6f61-122">10/11/2015</span></span> | <span data-ttu-id="a6f61-123">110110 – sularaha</span><span class="sxs-lookup"><span data-stu-id="a6f61-123">110110 – Cash</span></span>                | <span data-ttu-id="a6f61-124">USA dollar</span><span class="sxs-lookup"><span data-stu-id="a6f61-124">USD</span></span>      | <span data-ttu-id="a6f61-125">500</span><span class="sxs-lookup"><span data-stu-id="a6f61-125">500</span></span>    |
| <span data-ttu-id="a6f61-126">11.10.2015</span><span class="sxs-lookup"><span data-stu-id="a6f61-126">10/11/2015</span></span> | <span data-ttu-id="a6f61-127">130100 – müügireskontro</span><span class="sxs-lookup"><span data-stu-id="a6f61-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="a6f61-128">USA dollar</span><span class="sxs-lookup"><span data-stu-id="a6f61-128">USD</span></span>      | <span data-ttu-id="a6f61-129">–500</span><span class="sxs-lookup"><span data-stu-id="a6f61-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="a6f61-130">Vahetuskursid</span><span class="sxs-lookup"><span data-stu-id="a6f61-130">Exchange rates</span></span>

| <span data-ttu-id="a6f61-131">Valuutast</span><span class="sxs-lookup"><span data-stu-id="a6f61-131">From currency</span></span> | <span data-ttu-id="a6f61-132">Valuutaks</span><span class="sxs-lookup"><span data-stu-id="a6f61-132">To currency</span></span> | <span data-ttu-id="a6f61-133">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="a6f61-133">Start date</span></span> | <span data-ttu-id="a6f61-134">Vahetuskurss</span><span class="sxs-lookup"><span data-stu-id="a6f61-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="a6f61-135"> eurot</span><span class="sxs-lookup"><span data-stu-id="a6f61-135">EUR</span></span>           | <span data-ttu-id="a6f61-136">USA dollar</span><span class="sxs-lookup"><span data-stu-id="a6f61-136">USD</span></span>         | <span data-ttu-id="a6f61-137">1.10.2015</span><span class="sxs-lookup"><span data-stu-id="a6f61-137">10/1/2015</span></span>  | <span data-ttu-id="a6f61-138">200</span><span class="sxs-lookup"><span data-stu-id="a6f61-138">200</span></span>           |
| <span data-ttu-id="a6f61-139"> eurot</span><span class="sxs-lookup"><span data-stu-id="a6f61-139">EUR</span></span>           | <span data-ttu-id="a6f61-140">USA dollar</span><span class="sxs-lookup"><span data-stu-id="a6f61-140">USD</span></span>         | <span data-ttu-id="a6f61-141">1.11.2015</span><span class="sxs-lookup"><span data-stu-id="a6f61-141">11/1/2015</span></span>  | <span data-ttu-id="a6f61-142">150</span><span class="sxs-lookup"><span data-stu-id="a6f61-142">150</span></span>           |
| <span data-ttu-id="a6f61-143"> eurot</span><span class="sxs-lookup"><span data-stu-id="a6f61-143">EUR</span></span>           | <span data-ttu-id="a6f61-144">USA dollar</span><span class="sxs-lookup"><span data-stu-id="a6f61-144">USD</span></span>         | <span data-ttu-id="a6f61-145">1.12.2012</span><span class="sxs-lookup"><span data-stu-id="a6f61-145">12/1/2012</span></span>  | <span data-ttu-id="a6f61-146">100</span><span class="sxs-lookup"><span data-stu-id="a6f61-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="a6f61-147">2015. aasta oktoobri konsolideerimine</span><span class="sxs-lookup"><span data-stu-id="a6f61-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="a6f61-148">Konsolideeritava ettevõtte saldod</span><span class="sxs-lookup"><span data-stu-id="a6f61-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="a6f61-149">Pearaamatu konto</span><span class="sxs-lookup"><span data-stu-id="a6f61-149">Ledger account</span></span> | <span data-ttu-id="a6f61-150">Valuuta</span><span class="sxs-lookup"><span data-stu-id="a6f61-150">Currency</span></span> | <span data-ttu-id="a6f61-151">Summa</span><span class="sxs-lookup"><span data-stu-id="a6f61-151">Amount</span></span> | <span data-ttu-id="a6f61-152">Arvutus</span><span class="sxs-lookup"><span data-stu-id="a6f61-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="a6f61-153">110110</span><span class="sxs-lookup"><span data-stu-id="a6f61-153">110110</span></span>         | <span data-ttu-id="a6f61-154"> eurot</span><span class="sxs-lookup"><span data-stu-id="a6f61-154">EUR</span></span>      | <span data-ttu-id="a6f61-155">250</span><span class="sxs-lookup"><span data-stu-id="a6f61-155">250</span></span>    | <span data-ttu-id="a6f61-156">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="a6f61-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="a6f61-157">130100</span><span class="sxs-lookup"><span data-stu-id="a6f61-157">130100</span></span>         | <span data-ttu-id="a6f61-158"> eurot</span><span class="sxs-lookup"><span data-stu-id="a6f61-158">EUR</span></span>      | <span data-ttu-id="a6f61-159">–250</span><span class="sxs-lookup"><span data-stu-id="a6f61-159">-250</span></span>   | <span data-ttu-id="a6f61-160">–500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="a6f61-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="a6f61-161">Perioodi 1. oktoober 2015 kuni 30. november 2015 kontode valuuta ümberarvutamine</span><span class="sxs-lookup"><span data-stu-id="a6f61-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="a6f61-162">Konsolideeritava ettevõtte saldod</span><span class="sxs-lookup"><span data-stu-id="a6f61-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="a6f61-163">Pearaamatu konto</span><span class="sxs-lookup"><span data-stu-id="a6f61-163">Ledger account</span></span> | <span data-ttu-id="a6f61-164">Valuuta</span><span class="sxs-lookup"><span data-stu-id="a6f61-164">Currency</span></span> | <span data-ttu-id="a6f61-165">Summa</span><span class="sxs-lookup"><span data-stu-id="a6f61-165">Amount</span></span>  | <span data-ttu-id="a6f61-166">Arvutus</span><span class="sxs-lookup"><span data-stu-id="a6f61-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="a6f61-167">110110</span><span class="sxs-lookup"><span data-stu-id="a6f61-167">110110</span></span>         | <span data-ttu-id="a6f61-168"> eurot</span><span class="sxs-lookup"><span data-stu-id="a6f61-168">EUR</span></span>      | <span data-ttu-id="a6f61-169">333,33</span><span class="sxs-lookup"><span data-stu-id="a6f61-169">333.33</span></span>  | <span data-ttu-id="a6f61-170">Algne summa 500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="a6f61-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="a6f61-171">130100</span><span class="sxs-lookup"><span data-stu-id="a6f61-171">130100</span></span>         | <span data-ttu-id="a6f61-172"> eurot</span><span class="sxs-lookup"><span data-stu-id="a6f61-172">EUR</span></span>      | <span data-ttu-id="a6f61-173">–333,33</span><span class="sxs-lookup"><span data-stu-id="a6f61-173">-333.33</span></span> | <span data-ttu-id="a6f61-174">Algne summa –500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="a6f61-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="a6f61-175">801400</span><span class="sxs-lookup"><span data-stu-id="a6f61-175">801400</span></span>         | <span data-ttu-id="a6f61-176"> eurot</span><span class="sxs-lookup"><span data-stu-id="a6f61-176">EUR</span></span>      | <span data-ttu-id="a6f61-177">83,33</span><span class="sxs-lookup"><span data-stu-id="a6f61-177">83.33</span></span>   | <span data-ttu-id="a6f61-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="a6f61-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="a6f61-179">801600</span><span class="sxs-lookup"><span data-stu-id="a6f61-179">801600</span></span>         | <span data-ttu-id="a6f61-180"> eurot</span><span class="sxs-lookup"><span data-stu-id="a6f61-180">EUR</span></span>      | <span data-ttu-id="a6f61-181">–83,33</span><span class="sxs-lookup"><span data-stu-id="a6f61-181">-83.33</span></span>  | <span data-ttu-id="a6f61-182">–333,33 – (–250)</span><span class="sxs-lookup"><span data-stu-id="a6f61-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="a6f61-183">Näete aruandlusvaluuta summade puhul lisakandeid.</span><span class="sxs-lookup"><span data-stu-id="a6f61-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="a6f61-184">Perioodi 1. oktoober 2015 kuni 31. detsember 2015 kontode valuuta ümberarvutamine</span><span class="sxs-lookup"><span data-stu-id="a6f61-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="a6f61-185">Konsolideeritava ettevõtte saldod</span><span class="sxs-lookup"><span data-stu-id="a6f61-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="a6f61-186">Pearaamatu konto</span><span class="sxs-lookup"><span data-stu-id="a6f61-186">Ledger account</span></span> | <span data-ttu-id="a6f61-187">Valuuta</span><span class="sxs-lookup"><span data-stu-id="a6f61-187">Currency</span></span> | <span data-ttu-id="a6f61-188">Summa</span><span class="sxs-lookup"><span data-stu-id="a6f61-188">Amount</span></span>  | <span data-ttu-id="a6f61-189">Arvutus</span><span class="sxs-lookup"><span data-stu-id="a6f61-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="a6f61-190">110110</span><span class="sxs-lookup"><span data-stu-id="a6f61-190">110110</span></span>         | <span data-ttu-id="a6f61-191"> eurot</span><span class="sxs-lookup"><span data-stu-id="a6f61-191">EUR</span></span>      | <span data-ttu-id="a6f61-192">500,00</span><span class="sxs-lookup"><span data-stu-id="a6f61-192">500.00</span></span>  | <span data-ttu-id="a6f61-193">Algne summa 500 × 1</span><span class="sxs-lookup"><span data-stu-id="a6f61-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="a6f61-194">130100</span><span class="sxs-lookup"><span data-stu-id="a6f61-194">130100</span></span>         | <span data-ttu-id="a6f61-195"> eurot</span><span class="sxs-lookup"><span data-stu-id="a6f61-195">EUR</span></span>      | <span data-ttu-id="a6f61-196">–500,00</span><span class="sxs-lookup"><span data-stu-id="a6f61-196">-500.00</span></span> | <span data-ttu-id="a6f61-197">Algne summa –500 × 1</span><span class="sxs-lookup"><span data-stu-id="a6f61-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="a6f61-198">801400</span><span class="sxs-lookup"><span data-stu-id="a6f61-198">801400</span></span>         | <span data-ttu-id="a6f61-199"> eurot</span><span class="sxs-lookup"><span data-stu-id="a6f61-199">EUR</span></span>      | <span data-ttu-id="a6f61-200">250</span><span class="sxs-lookup"><span data-stu-id="a6f61-200">250</span></span>     | <span data-ttu-id="a6f61-201">500 – 333,33 = 166,67 166,67 + 83,33 = 250</span><span class="sxs-lookup"><span data-stu-id="a6f61-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="a6f61-202">801600</span><span class="sxs-lookup"><span data-stu-id="a6f61-202">801600</span></span>         | <span data-ttu-id="a6f61-203"> eurot</span><span class="sxs-lookup"><span data-stu-id="a6f61-203">EUR</span></span>      | <span data-ttu-id="a6f61-204">–250</span><span class="sxs-lookup"><span data-stu-id="a6f61-204">-250</span></span>    | <span data-ttu-id="a6f61-205">–500 – (–333,33) = –166,67 –166,67 + (–83,33) = –250</span><span class="sxs-lookup"><span data-stu-id="a6f61-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





