---
title: "Skonto töötlemine ülemaksete korral"
description: "Selles artiklis on stsenaariumid, mis nöitavad, kuidas makset käsitletakse, kui klient võtab skonto, kuid maksab üle."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14171
ms.assetid: a94d0fd0-57ba-4054-93c8-519d01d50e19
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 5604f806eed81c60dfcae7cb7b1a22bba25aa454
ms.contentlocale: et-ee
ms.lasthandoff: 06/29/2017


---

# <a name="handling-cash-discounts-for-overpayments"></a><span data-ttu-id="87448-103">Skonto töötlemine ülemaksete korral</span><span class="sxs-lookup"><span data-stu-id="87448-103">Handling cash discounts for overpayments</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="87448-104">Selles artiklis on stsenaariumid, mis nöitavad, kuidas makset käsitletakse, kui klient võtab skonto, kuid maksab üle.</span><span class="sxs-lookup"><span data-stu-id="87448-104">This article provides scenarios that show how a payment is handled when the customer takes a cash discount but also overpays.</span></span> 

<span data-ttu-id="87448-105">Arve loetakse ülemakstuks, kui maksesumma on suurem kui arve summa, millest on maha arvestatud skonto.</span><span class="sxs-lookup"><span data-stu-id="87448-105">An invoice is considered overpaid when the payment amount is more than the invoice amount minus the cash discount.</span></span> <span data-ttu-id="87448-106">Määramaks, kuidas saadavat skonto erinevust ülemaksete korral käsitletakse, kasutage välju **Skonto haldamine** ja **Suurim üle- või alamakse** lehel **Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="87448-106">To specify how an obtainable cash discount difference is handled when an invoice is overpaid, use the **Cash discount administration** and **Maximum overpayment or underpayment** fields on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="87448-107">Järgmises näites on klient arve üle maksnud 0,50 võrra.</span><span class="sxs-lookup"><span data-stu-id="87448-107">In the following example, the customer has overpaid the invoice by 0.50.</span></span>

| <span data-ttu-id="87448-108">Arve summa</span><span class="sxs-lookup"><span data-stu-id="87448-108">Invoice total</span></span> | <span data-ttu-id="87448-109">Saadaolev skonto</span><span class="sxs-lookup"><span data-stu-id="87448-109">Cash discount available</span></span> | <span data-ttu-id="87448-110">Makstav summa, mis hõlmab skontot</span><span class="sxs-lookup"><span data-stu-id="87448-110">Amount to be paid, which includes the cash discount</span></span> | <span data-ttu-id="87448-111">Kliendi tegelikult makstav summa</span><span class="sxs-lookup"><span data-stu-id="87448-111">Amount the customer actually pays</span></span> |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| <span data-ttu-id="87448-112">105,00</span><span class="sxs-lookup"><span data-stu-id="87448-112">105.00</span></span>        | <span data-ttu-id="87448-113">10,50</span><span class="sxs-lookup"><span data-stu-id="87448-113">10.50</span></span>                   | <span data-ttu-id="87448-114">94,50</span><span class="sxs-lookup"><span data-stu-id="87448-114">94.50</span></span>                                               | <span data-ttu-id="87448-115">95,00</span><span class="sxs-lookup"><span data-stu-id="87448-115">95.00</span></span>                             |

## <a name="cash-discount-administration--specific"></a><span data-ttu-id="87448-116">Skonto haldamine = spetsiifiline</span><span class="sxs-lookup"><span data-stu-id="87448-116">Cash discount administration = Specific</span></span>
<span data-ttu-id="87448-117">Kui lehe **Automaatsete kannete kontod** väljal **Skonto haldamine** valitakse suvand **Spetsiifiline**, vetakse täielik skonto.</span><span class="sxs-lookup"><span data-stu-id="87448-117">When **Specific** is selected in the **Cash discount administration** field on the **Accounts for automatic transactions** page, the full cash discount is taken.</span></span> <span data-ttu-id="87448-118">Ülemakse summa sisestatakse skonto erinevuse pearaamatukontole või jäetakse saldona kliendi kontole.</span><span class="sxs-lookup"><span data-stu-id="87448-118">The overpayment amount either is posted to a cash discount difference ledger account or remains a balance on the customer’s account.</span></span> <span data-ttu-id="87448-119">Käitumine oleneb sellest, kas ülemakse summa on 0,00 ja väljale**Suurim üle- või alamakse** sisestatud summa vahel või kas ülemakse summa on suurem kui summa väljal **Suurim üle- või alamakse**.</span><span class="sxs-lookup"><span data-stu-id="87448-119">The behavior depends on whether the overpayment amount is between 0.00 and the amount that is entered in the **Maximum overpayment or underpayment** field, or whether the overpayment amount is more than the **Maximum overpayment or underpayment** amount.</span></span>

### <a name="scenario-1"></a><span data-ttu-id="87448-120">1. stsenaarium</span><span class="sxs-lookup"><span data-stu-id="87448-120">Scenario 1</span></span>

<span data-ttu-id="87448-121">Selles stsenaariumis on ülemakse summa 0,00 ja maksimaalse üle- või alamakse vahemikus.</span><span class="sxs-lookup"><span data-stu-id="87448-121">In this scenario, the overpayment amount is between 0.00 and the maximum overpayment or underpayment.</span></span> <span data-ttu-id="87448-122">Arve on sisestatud summas 105,00 ja skonto on saadaval, kui arve makstakse seitsme päeva jooksul.</span><span class="sxs-lookup"><span data-stu-id="87448-122">An invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="87448-123">Arve summa</span><span class="sxs-lookup"><span data-stu-id="87448-123">Invoice total</span></span> | <span data-ttu-id="87448-124">Saadaolev skonto</span><span class="sxs-lookup"><span data-stu-id="87448-124">Cash discount available</span></span> | <span data-ttu-id="87448-125">Makstav summa, mis hõlmab skontot</span><span class="sxs-lookup"><span data-stu-id="87448-125">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="87448-126">105,00</span><span class="sxs-lookup"><span data-stu-id="87448-126">105.00</span></span>        | <span data-ttu-id="87448-127">10,50</span><span class="sxs-lookup"><span data-stu-id="87448-127">10.50</span></span>                   | <span data-ttu-id="87448-128">94,50</span><span class="sxs-lookup"><span data-stu-id="87448-128">94.50</span></span>                                               |

<span data-ttu-id="87448-129">Klient edastab makse 95,00 skontoperioodil.</span><span class="sxs-lookup"><span data-stu-id="87448-129">The customer submits a payment for 95.00 within the cash discount period.</span></span> <span data-ttu-id="87448-130">Makse tasakaalustatakse arve alusel, mille summa on 105,00.</span><span class="sxs-lookup"><span data-stu-id="87448-130">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="87448-131">Kui arve ja makse on tasakaalustatud, luuakse kliendi ostureskontrosse järgmised kanded.</span><span class="sxs-lookup"><span data-stu-id="87448-131">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="87448-132">Kanne</span><span class="sxs-lookup"><span data-stu-id="87448-132">Transaction</span></span>   | <span data-ttu-id="87448-133">Summa</span><span class="sxs-lookup"><span data-stu-id="87448-133">Amount</span></span> | <span data-ttu-id="87448-134">Saldo</span><span class="sxs-lookup"><span data-stu-id="87448-134">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="87448-135">Arve</span><span class="sxs-lookup"><span data-stu-id="87448-135">Invoice</span></span>       | <span data-ttu-id="87448-136">105,00</span><span class="sxs-lookup"><span data-stu-id="87448-136">105.00</span></span> | <span data-ttu-id="87448-137">0,00</span><span class="sxs-lookup"><span data-stu-id="87448-137">0.00</span></span>    |
| <span data-ttu-id="87448-138">Makse</span><span class="sxs-lookup"><span data-stu-id="87448-138">Payment</span></span>       | <span data-ttu-id="87448-139">-95,00</span><span class="sxs-lookup"><span data-stu-id="87448-139">-95.00</span></span> | <span data-ttu-id="87448-140">0,00</span><span class="sxs-lookup"><span data-stu-id="87448-140">0.00</span></span>    |
| <span data-ttu-id="87448-141">Skonto</span><span class="sxs-lookup"><span data-stu-id="87448-141">Cash discount</span></span> | <span data-ttu-id="87448-142">-10,50</span><span class="sxs-lookup"><span data-stu-id="87448-142">-10.50</span></span> | <span data-ttu-id="87448-143">0,00</span><span class="sxs-lookup"><span data-stu-id="87448-143">0.00</span></span>    |

<span data-ttu-id="87448-144">Makse ja tasakaalustuse kohta luuakse järgmised raamatupidamiskirjed.</span><span class="sxs-lookup"><span data-stu-id="87448-144">The following accounting entries are generated for the payment and the settlement.</span></span> <span data-ttu-id="87448-145">**Makse**</span><span class="sxs-lookup"><span data-stu-id="87448-145">**Payment**</span></span>

| <span data-ttu-id="87448-146">Konto</span><span class="sxs-lookup"><span data-stu-id="87448-146">Account</span></span>             | <span data-ttu-id="87448-147">Deebetsumma</span><span class="sxs-lookup"><span data-stu-id="87448-147">Debit amount</span></span> | <span data-ttu-id="87448-148">Kreeditsumma</span><span class="sxs-lookup"><span data-stu-id="87448-148">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="87448-149">Sularaha</span><span class="sxs-lookup"><span data-stu-id="87448-149">Cash</span></span>                | <span data-ttu-id="87448-150">95,00</span><span class="sxs-lookup"><span data-stu-id="87448-150">95.00</span></span>        |               |
| <span data-ttu-id="87448-151">Müügireskontro</span><span class="sxs-lookup"><span data-stu-id="87448-151">Accounts receivable</span></span> |              | <span data-ttu-id="87448-152">95,00</span><span class="sxs-lookup"><span data-stu-id="87448-152">95.00</span></span>         |

<span data-ttu-id="87448-153">**Tasakaalustus**</span><span class="sxs-lookup"><span data-stu-id="87448-153">**Settlement**</span></span>

| <span data-ttu-id="87448-154">Konto</span><span class="sxs-lookup"><span data-stu-id="87448-154">Account</span></span>                                                                                                          | <span data-ttu-id="87448-155">Deebetsumma</span><span class="sxs-lookup"><span data-stu-id="87448-155">Debit amount</span></span> | <span data-ttu-id="87448-156">Kreeditsumma</span><span class="sxs-lookup"><span data-stu-id="87448-156">Credit amount</span></span> |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="87448-157">Skonto (väli **Kliendi allahindluste põhikonto** lehel **Skontod**)</span><span class="sxs-lookup"><span data-stu-id="87448-157">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span>                 | <span data-ttu-id="87448-158">10,50</span><span class="sxs-lookup"><span data-stu-id="87448-158">10.50</span></span>        |               |
| <span data-ttu-id="87448-159">Müügireskontro</span><span class="sxs-lookup"><span data-stu-id="87448-159">Accounts receivable</span></span>                                                                                              |              | <span data-ttu-id="87448-160">10,50</span><span class="sxs-lookup"><span data-stu-id="87448-160">10.50</span></span>         |
| <span data-ttu-id="87448-161">Kliendi skonto (väli **Kliendi skonto** lehel **Automaatsete kannete konto**)</span><span class="sxs-lookup"><span data-stu-id="87448-161">Customer cash discount (the **Customer cash discount** field on the **Account for automatic transactions** page)</span></span> |              | <span data-ttu-id="87448-162">0,50</span><span class="sxs-lookup"><span data-stu-id="87448-162">0.50</span></span>          |
| <span data-ttu-id="87448-163">Müügireskontro</span><span class="sxs-lookup"><span data-stu-id="87448-163">Accounts receivable</span></span>                                                                                              | <span data-ttu-id="87448-164">0,50</span><span class="sxs-lookup"><span data-stu-id="87448-164">0.50</span></span>         |               |

### <a name="scenario-2"></a><span data-ttu-id="87448-165">2. stsenaarium</span><span class="sxs-lookup"><span data-stu-id="87448-165">Scenario 2</span></span>

<span data-ttu-id="87448-166">Selles stsenaariumis on ülemakse summa suurem kui maksimaalne üle- või alamakse.</span><span class="sxs-lookup"><span data-stu-id="87448-166">In this scenario, the overpayment amount exceeds the maximum overpayment or underpayment amount.</span></span> <span data-ttu-id="87448-167">Arve on sisestatud summas 105,00 ja skonto on saadaval, kui arve makstakse seitsme päeva jooksul.</span><span class="sxs-lookup"><span data-stu-id="87448-167">An invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="87448-168">Arve summa</span><span class="sxs-lookup"><span data-stu-id="87448-168">Invoice total</span></span> | <span data-ttu-id="87448-169">Saadaolev skonto</span><span class="sxs-lookup"><span data-stu-id="87448-169">Cash discount available</span></span> | <span data-ttu-id="87448-170">Makstav summa, mis hõlmab skontot</span><span class="sxs-lookup"><span data-stu-id="87448-170">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="87448-171">105,00</span><span class="sxs-lookup"><span data-stu-id="87448-171">105.00</span></span>        | <span data-ttu-id="87448-172">10,50</span><span class="sxs-lookup"><span data-stu-id="87448-172">10.50</span></span>                   | <span data-ttu-id="87448-173">94,50</span><span class="sxs-lookup"><span data-stu-id="87448-173">94.50</span></span>                                               |

<span data-ttu-id="87448-174">Klient edastab makse 95,00 skontoperioodil.</span><span class="sxs-lookup"><span data-stu-id="87448-174">The customer submits a payment for 95.00 within the cash discount period.</span></span> <span data-ttu-id="87448-175">Makse tasakaalustatakse arve alusel, mille summa on 105,00.</span><span class="sxs-lookup"><span data-stu-id="87448-175">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="87448-176">Kui arve ja makse on tasakaalustatud, luuakse kliendi ostureskontrosse järgmised kanded.</span><span class="sxs-lookup"><span data-stu-id="87448-176">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="87448-177">Kanne</span><span class="sxs-lookup"><span data-stu-id="87448-177">Transaction</span></span>   | <span data-ttu-id="87448-178">Summa</span><span class="sxs-lookup"><span data-stu-id="87448-178">Amount</span></span> | <span data-ttu-id="87448-179">Saldo</span><span class="sxs-lookup"><span data-stu-id="87448-179">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="87448-180">Arve</span><span class="sxs-lookup"><span data-stu-id="87448-180">Invoice</span></span>       | <span data-ttu-id="87448-181">105,00</span><span class="sxs-lookup"><span data-stu-id="87448-181">105.00</span></span> | <span data-ttu-id="87448-182">0,00</span><span class="sxs-lookup"><span data-stu-id="87448-182">0.00</span></span>    |
| <span data-ttu-id="87448-183">Makse</span><span class="sxs-lookup"><span data-stu-id="87448-183">Payment</span></span>       | <span data-ttu-id="87448-184">-95,00</span><span class="sxs-lookup"><span data-stu-id="87448-184">-95.00</span></span> | <span data-ttu-id="87448-185">-0,50</span><span class="sxs-lookup"><span data-stu-id="87448-185">-0.50</span></span>   |
| <span data-ttu-id="87448-186">Skonto</span><span class="sxs-lookup"><span data-stu-id="87448-186">Cash discount</span></span> | <span data-ttu-id="87448-187">-10,50</span><span class="sxs-lookup"><span data-stu-id="87448-187">-10.50</span></span> | <span data-ttu-id="87448-188">0,00</span><span class="sxs-lookup"><span data-stu-id="87448-188">0.00</span></span>    |

<span data-ttu-id="87448-189">Ülemakse summa 0,50 jääb makse avatud saldoks ning selle saab muu arvega tasakaalustada.</span><span class="sxs-lookup"><span data-stu-id="87448-189">The overpayment amount of 0.50 will remain as an open balance on the payment and can be settled against another invoice.</span></span> <span data-ttu-id="87448-190">Makse ja tasakaalustuse kohta luuakse järgmised raamatupidamiskirjed.</span><span class="sxs-lookup"><span data-stu-id="87448-190">The following accounting entries are generated for the payment and the settlement.</span></span> <span data-ttu-id="87448-191">**Makse**</span><span class="sxs-lookup"><span data-stu-id="87448-191">**Payment**</span></span>

| <span data-ttu-id="87448-192">Konto</span><span class="sxs-lookup"><span data-stu-id="87448-192">Account</span></span>             | <span data-ttu-id="87448-193">Deebetsumma</span><span class="sxs-lookup"><span data-stu-id="87448-193">Debit amount</span></span> | <span data-ttu-id="87448-194">Kreeditsumma</span><span class="sxs-lookup"><span data-stu-id="87448-194">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="87448-195">Sularaha</span><span class="sxs-lookup"><span data-stu-id="87448-195">Cash</span></span>                | <span data-ttu-id="87448-196">95,00</span><span class="sxs-lookup"><span data-stu-id="87448-196">95.00</span></span>        |               |
| <span data-ttu-id="87448-197">Müügireskontro</span><span class="sxs-lookup"><span data-stu-id="87448-197">Accounts receivable</span></span> |              | <span data-ttu-id="87448-198">95,00</span><span class="sxs-lookup"><span data-stu-id="87448-198">95.00</span></span>         |

<span data-ttu-id="87448-199">**Tasakaalustus**</span><span class="sxs-lookup"><span data-stu-id="87448-199">**Settlement**</span></span>

| <span data-ttu-id="87448-200">Konto</span><span class="sxs-lookup"><span data-stu-id="87448-200">Account</span></span>                                                                                          | <span data-ttu-id="87448-201">Deebetsumma</span><span class="sxs-lookup"><span data-stu-id="87448-201">Debit amount</span></span> | <span data-ttu-id="87448-202">Kreeditsumma</span><span class="sxs-lookup"><span data-stu-id="87448-202">Credit amount</span></span> |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="87448-203">Skonto (väli **Kliendi allahindluste põhikonto** lehel **Skontod**)</span><span class="sxs-lookup"><span data-stu-id="87448-203">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span> | <span data-ttu-id="87448-204">10,50</span><span class="sxs-lookup"><span data-stu-id="87448-204">10.50</span></span>        |               |
| <span data-ttu-id="87448-205">Müügireskontro</span><span class="sxs-lookup"><span data-stu-id="87448-205">Accounts receivable</span></span>                                                                              |              | <span data-ttu-id="87448-206">10,50</span><span class="sxs-lookup"><span data-stu-id="87448-206">10.50</span></span>         |

## <a name="cash-discount-administration--unspecific"></a><span data-ttu-id="87448-207">Skonto haldamine = määramata</span><span class="sxs-lookup"><span data-stu-id="87448-207">Cash discount administration = Unspecific</span></span>
<span data-ttu-id="87448-208">Kui lehe **Automaatsete kannete kontod** väljal **Skonto haldamine** valitakse suvand **Määramata**, vähendatakse skonto summat ülemakse summa võrra.</span><span class="sxs-lookup"><span data-stu-id="87448-208">When **Unspecific** is selected in the **Cash discount administration** field on the **Accounts for automatic transactions** page, the cash discount amount is reduced by the overpayment amount.</span></span> <span data-ttu-id="87448-209">Seda kasutatakse alati, olenemata sellest, kas ülemakse summa on suurem või väiksem kui summa, mis on sisestatud väljale **Suurim üle- või alamakse**.</span><span class="sxs-lookup"><span data-stu-id="87448-209">This behavior always applies, regardless of whether the overpayment amount is over or under the amount that is entered in the **Maximum overpayment or underpayment** field.</span></span>

### <a name="scenario-3"></a><span data-ttu-id="87448-210">3. stsenaarium</span><span class="sxs-lookup"><span data-stu-id="87448-210">Scenario 3</span></span>

<span data-ttu-id="87448-211">Selles stsenaariumis on arve sisestatud summas 105,00 ja skonto on saadaval, kui arve makstakse seitsme päeva jooksul.</span><span class="sxs-lookup"><span data-stu-id="87448-211">In this scenario, an invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="87448-212">Arve summa</span><span class="sxs-lookup"><span data-stu-id="87448-212">Invoice total</span></span> | <span data-ttu-id="87448-213">Saadaolev skonto</span><span class="sxs-lookup"><span data-stu-id="87448-213">Cash discount available</span></span> | <span data-ttu-id="87448-214">Makstav summa, mis hõlmab skontot</span><span class="sxs-lookup"><span data-stu-id="87448-214">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="87448-215">105,00</span><span class="sxs-lookup"><span data-stu-id="87448-215">105.00</span></span>        | <span data-ttu-id="87448-216">10,50</span><span class="sxs-lookup"><span data-stu-id="87448-216">10.50</span></span>                   | <span data-ttu-id="87448-217">94,50</span><span class="sxs-lookup"><span data-stu-id="87448-217">94.50</span></span>                                               |

<span data-ttu-id="87448-218">Klient edastab makse 95,00 skonto kuupäevaks.</span><span class="sxs-lookup"><span data-stu-id="87448-218">The customer submits a payment for 95.00 within the cash discount date.</span></span> <span data-ttu-id="87448-219">Makse tasakaalustatakse arve alusel, mille summa on 105,00.</span><span class="sxs-lookup"><span data-stu-id="87448-219">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="87448-220">Kui arve ja makse on tasakaalustatud, luuakse kliendi ostureskontrosse järgmised kanded.</span><span class="sxs-lookup"><span data-stu-id="87448-220">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="87448-221">Kanne</span><span class="sxs-lookup"><span data-stu-id="87448-221">Transaction</span></span>   | <span data-ttu-id="87448-222">Summa</span><span class="sxs-lookup"><span data-stu-id="87448-222">Amount</span></span> | <span data-ttu-id="87448-223">Saldo</span><span class="sxs-lookup"><span data-stu-id="87448-223">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="87448-224">Arve</span><span class="sxs-lookup"><span data-stu-id="87448-224">Invoice</span></span>       | <span data-ttu-id="87448-225">105,00</span><span class="sxs-lookup"><span data-stu-id="87448-225">105.00</span></span> | <span data-ttu-id="87448-226">0,00</span><span class="sxs-lookup"><span data-stu-id="87448-226">0.00</span></span>    |
| <span data-ttu-id="87448-227">Makse</span><span class="sxs-lookup"><span data-stu-id="87448-227">Payment</span></span>       | <span data-ttu-id="87448-228">-95,00</span><span class="sxs-lookup"><span data-stu-id="87448-228">-95.00</span></span> | <span data-ttu-id="87448-229">-0,00</span><span class="sxs-lookup"><span data-stu-id="87448-229">-0.00</span></span>   |
| <span data-ttu-id="87448-230">Skonto</span><span class="sxs-lookup"><span data-stu-id="87448-230">Cash discount</span></span> | <span data-ttu-id="87448-231">-10,00</span><span class="sxs-lookup"><span data-stu-id="87448-231">-10.00</span></span> | <span data-ttu-id="87448-232">0,00</span><span class="sxs-lookup"><span data-stu-id="87448-232">0.00</span></span>    |

<span data-ttu-id="87448-233">Skonto summat 10,50 vähendatakse 10,00-ni.</span><span class="sxs-lookup"><span data-stu-id="87448-233">The cash discount amount is reduced from 10.50 to 10.00.</span></span> <span data-ttu-id="87448-234">Makse ja arve loetakse tasakaalustatuks.</span><span class="sxs-lookup"><span data-stu-id="87448-234">The payment and invoice are considered settled.</span></span> <span data-ttu-id="87448-235">**Makse**</span><span class="sxs-lookup"><span data-stu-id="87448-235">**Payment**</span></span>

| <span data-ttu-id="87448-236">Konto</span><span class="sxs-lookup"><span data-stu-id="87448-236">Account</span></span>             | <span data-ttu-id="87448-237">Deebetsumma</span><span class="sxs-lookup"><span data-stu-id="87448-237">Debit amount</span></span> | <span data-ttu-id="87448-238">Kreeditsumma</span><span class="sxs-lookup"><span data-stu-id="87448-238">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="87448-239">Sularaha</span><span class="sxs-lookup"><span data-stu-id="87448-239">Cash</span></span>                | <span data-ttu-id="87448-240">95,00</span><span class="sxs-lookup"><span data-stu-id="87448-240">95.00</span></span>        |               |
| <span data-ttu-id="87448-241">Müügireskontro</span><span class="sxs-lookup"><span data-stu-id="87448-241">Accounts receivable</span></span> |              | <span data-ttu-id="87448-242">95,00</span><span class="sxs-lookup"><span data-stu-id="87448-242">95.00</span></span>         |

<span data-ttu-id="87448-243">**Tasakaalustus**</span><span class="sxs-lookup"><span data-stu-id="87448-243">**Settlement**</span></span>

| <span data-ttu-id="87448-244">Konto</span><span class="sxs-lookup"><span data-stu-id="87448-244">Account</span></span>                                                                                          | <span data-ttu-id="87448-245">Deebetsumma</span><span class="sxs-lookup"><span data-stu-id="87448-245">Debit amount</span></span> | <span data-ttu-id="87448-246">Kreeditsumma</span><span class="sxs-lookup"><span data-stu-id="87448-246">Credit amount</span></span> |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="87448-247">Skonto (väli **Kliendi allahindluste põhikonto** lehel **Skontod**)</span><span class="sxs-lookup"><span data-stu-id="87448-247">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span> | <span data-ttu-id="87448-248">10,50</span><span class="sxs-lookup"><span data-stu-id="87448-248">10.50</span></span>        |               |
| <span data-ttu-id="87448-249">Müügireskontro</span><span class="sxs-lookup"><span data-stu-id="87448-249">Accounts receivable</span></span>                                                                              |              | <span data-ttu-id="87448-250">10,50</span><span class="sxs-lookup"><span data-stu-id="87448-250">10.50</span></span>         |






