---
title: Skonto võtmine väljaspool skonto perioodi
description: See artikkel pakub kaht stsenaariumi, mis näitavad, kuidas skontot saab arvestada, isegi kui makse on tehtud väljaspool skontoperioodi.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4a166e9a0d43da80986dd63d6739b104745b115
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189472"
---
# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a><span data-ttu-id="fc03f-103">Skonto võtmine väljaspool skonto perioodi</span><span class="sxs-lookup"><span data-stu-id="fc03f-103">Take a cash discount outside the cash discount period</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc03f-104">See artikkel pakub kaht stsenaariumi, mis näitavad, kuidas skontot saab arvestada, isegi kui makse on tehtud väljaspool skontoperioodi.</span><span class="sxs-lookup"><span data-stu-id="fc03f-104">This article provides two scenarios that show how a cash discount can be taken even if the payment is made outside the cash discount period.</span></span>

<span data-ttu-id="fc03f-105">28. juunil loob April arve hankijale 3052 summas 2000,00.</span><span class="sxs-lookup"><span data-stu-id="fc03f-105">On June 28, April creates an invoice for 2,000.00 for vendor 3052.</span></span> <span data-ttu-id="fc03f-106">Arvel on skonto 1 protsent, kui arve tasutakse 14 päeva jooksul.</span><span class="sxs-lookup"><span data-stu-id="fc03f-106">The invoice has a cash discount of 1 percent if the invoice is paid in 14 days.</span></span>

## <a name="use-cash-discount-option--always"></a><span data-ttu-id="fc03f-107">Suvand Kasuta skontot = Alati</span><span class="sxs-lookup"><span data-stu-id="fc03f-107">Use cash discount option = Always</span></span>
<span data-ttu-id="fc03f-108">April loob makse 1. juulil, mis on pärast skonto kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="fc03f-108">April creates a payment on July 1, which is after the discount date.</span></span> <span data-ttu-id="fc03f-109">April avab tasakaalustatavate arvete vaatamiseks lehekülje **Kannete tasakaalustamine**.</span><span class="sxs-lookup"><span data-stu-id="fc03f-109">April opens the **Settle transactions** page to view the transactions that can be settled.</span></span> 

<span data-ttu-id="fc03f-110">April märgib arve maksmiseks.</span><span class="sxs-lookup"><span data-stu-id="fc03f-110">April marks the invoice for payment.</span></span> <span data-ttu-id="fc03f-111">Skontot ei võeta, kuna makse toimub pärast skonto kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="fc03f-111">No cash discount is taken, because the payment is after the discount date.</span></span> <span data-ttu-id="fc03f-112">Siiski on andnud hankija Aprilile nõusoleku vaatamata sellele skontot võtta.</span><span class="sxs-lookup"><span data-stu-id="fc03f-112">However, the vendor has given April approval to take the cash discount anyway.</span></span> <span data-ttu-id="fc03f-113">Seega muudab April väljal **Kasuta skontot** väärtuseks **Alati**.</span><span class="sxs-lookup"><span data-stu-id="fc03f-113">Therefore, April changes the value in the **Use cash discount** field to **Always**.</span></span>

| <span data-ttu-id="fc03f-114">Märge</span><span class="sxs-lookup"><span data-stu-id="fc03f-114">Mark</span></span>     | <span data-ttu-id="fc03f-115">Kasuta skontot</span><span class="sxs-lookup"><span data-stu-id="fc03f-115">Use cash discount</span></span> | <span data-ttu-id="fc03f-116">Kanne</span><span class="sxs-lookup"><span data-stu-id="fc03f-116">Voucher</span></span>   | <span data-ttu-id="fc03f-117">Konto</span><span class="sxs-lookup"><span data-stu-id="fc03f-117">Account</span></span> | <span data-ttu-id="fc03f-118">Skonto kuupäev</span><span class="sxs-lookup"><span data-stu-id="fc03f-118">Cash discount date</span></span> | <span data-ttu-id="fc03f-119">Tähtaeg</span><span class="sxs-lookup"><span data-stu-id="fc03f-119">Due date</span></span>  | <span data-ttu-id="fc03f-120">Arve</span><span class="sxs-lookup"><span data-stu-id="fc03f-120">Invoice</span></span> | <span data-ttu-id="fc03f-121">Summa kandevaluutas</span><span class="sxs-lookup"><span data-stu-id="fc03f-121">Amount in transaction currency</span></span> | <span data-ttu-id="fc03f-122">Valuuta</span><span class="sxs-lookup"><span data-stu-id="fc03f-122">Currency</span></span> | <span data-ttu-id="fc03f-123">Tasakaalustatav summa</span><span class="sxs-lookup"><span data-stu-id="fc03f-123">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="fc03f-124">Valitud</span><span class="sxs-lookup"><span data-stu-id="fc03f-124">Selected</span></span> | <span data-ttu-id="fc03f-125">Alati</span><span class="sxs-lookup"><span data-stu-id="fc03f-125">Always</span></span>            | <span data-ttu-id="fc03f-126">Inv-10030</span><span class="sxs-lookup"><span data-stu-id="fc03f-126">Inv-10030</span></span> | <span data-ttu-id="fc03f-127">3052</span><span class="sxs-lookup"><span data-stu-id="fc03f-127">3052</span></span>    | <span data-ttu-id="fc03f-128">28.06.2015</span><span class="sxs-lookup"><span data-stu-id="fc03f-128">6/28/2015</span></span>          | <span data-ttu-id="fc03f-129">12.07.2015</span><span class="sxs-lookup"><span data-stu-id="fc03f-129">7/12/2015</span></span> | <span data-ttu-id="fc03f-130">10030</span><span class="sxs-lookup"><span data-stu-id="fc03f-130">10030</span></span>   | <span data-ttu-id="fc03f-131">‑2000,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-131">-2,000.00</span></span>                      | <span data-ttu-id="fc03f-132">USA dollar</span><span class="sxs-lookup"><span data-stu-id="fc03f-132">USD</span></span>      | <span data-ttu-id="fc03f-133">‑1980,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-133">-1,980.00</span></span>        |

<span data-ttu-id="fc03f-134">Teave märgitud arve allahindluse kohta kuvatakse lehe **Kannete tasakaalustamine** allosas.</span><span class="sxs-lookup"><span data-stu-id="fc03f-134">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="fc03f-135">Skonto kuupäev</span><span class="sxs-lookup"><span data-stu-id="fc03f-135">Cash discount date</span></span>           | <span data-ttu-id="fc03f-136">12.07.2015</span><span class="sxs-lookup"><span data-stu-id="fc03f-136">7/12/2015</span></span> |
| <span data-ttu-id="fc03f-137">Skonto summa</span><span class="sxs-lookup"><span data-stu-id="fc03f-137">Cash discount amount</span></span>         | <span data-ttu-id="fc03f-138">‑20,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-138">-20.00</span></span>    |
| <span data-ttu-id="fc03f-139">Kasuta skontot</span><span class="sxs-lookup"><span data-stu-id="fc03f-139">Use cash discount</span></span>            | <span data-ttu-id="fc03f-140">Alati</span><span class="sxs-lookup"><span data-stu-id="fc03f-140">Always</span></span>    |
| <span data-ttu-id="fc03f-141">Võetud skonto</span><span class="sxs-lookup"><span data-stu-id="fc03f-141">Cash discount taken</span></span>          | <span data-ttu-id="fc03f-142">0,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-142">0.00</span></span>      |
| <span data-ttu-id="fc03f-143">Skonto summa võtmiseks</span><span class="sxs-lookup"><span data-stu-id="fc03f-143">Cash discount amount to take</span></span> | <span data-ttu-id="fc03f-144">‑20,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-144">-20.00</span></span>    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a><span data-ttu-id="fc03f-145">Kuupäev, mida kasutatakse allahindluste arvutamiseks = Valitud kuupäev</span><span class="sxs-lookup"><span data-stu-id="fc03f-145">Date to use for calculating discounts = Selected date</span></span>
<span data-ttu-id="fc03f-146">Kui mõlemad, nii arve kui ka makse on sisestatud, saab kannete tasakaalustamisel skontot võtta leheküljel **Kannete tasakaalustamine**.</span><span class="sxs-lookup"><span data-stu-id="fc03f-146">If both the invoice and the payment have been posted, the cash discount can still be taken when the transactions are settled on the **Settle transactions** page.</span></span> <span data-ttu-id="fc03f-147">April muudab välja **Kuupäev, mida kasutatakse allahindluste arvutamiseks** väärtuseks **Valitud kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="fc03f-147">April changes the value in the **Date to use for calculating discounts** field to **Selected date**.</span></span> <span data-ttu-id="fc03f-148">Seejärel sisestab ta kuupäevaks 28. juuni, mis jääb arvel olnud skonto perioodi.</span><span class="sxs-lookup"><span data-stu-id="fc03f-148">She then enters a date of June 28, which is in the cash discount period for the invoice.</span></span> <span data-ttu-id="fc03f-149">Kande skonto arvutamiseks kasutatakse seda kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="fc03f-149">That date is used to calculate a cash discount for the transaction.</span></span> <span data-ttu-id="fc03f-150">April näeb, et vaikimisi kuvatakse leheküljel **Avatud kannete tasakaalustamine** kogu skonto summas 20,00.</span><span class="sxs-lookup"><span data-stu-id="fc03f-150">On the **Settle open transactions** page, April sees that, by default, the full discount of 20.00 appears.</span></span> <span data-ttu-id="fc03f-151">Arve real kuvatakse tasakaalustatavaks summaks 1980,00.</span><span class="sxs-lookup"><span data-stu-id="fc03f-151">The invoice line shows that the amount to settle is 1,980.00.</span></span>

| <span data-ttu-id="fc03f-152">Märge</span><span class="sxs-lookup"><span data-stu-id="fc03f-152">Mark</span></span>                     | <span data-ttu-id="fc03f-153">Kasuta skontot</span><span class="sxs-lookup"><span data-stu-id="fc03f-153">Use cash discount</span></span> | <span data-ttu-id="fc03f-154">Kanne</span><span class="sxs-lookup"><span data-stu-id="fc03f-154">Voucher</span></span>   | <span data-ttu-id="fc03f-155">Konto</span><span class="sxs-lookup"><span data-stu-id="fc03f-155">Account</span></span> | <span data-ttu-id="fc03f-156">Skonto kuupäev</span><span class="sxs-lookup"><span data-stu-id="fc03f-156">Cash discount date</span></span> | <span data-ttu-id="fc03f-157">Tähtaeg</span><span class="sxs-lookup"><span data-stu-id="fc03f-157">Due date</span></span>  | <span data-ttu-id="fc03f-158">Arve</span><span class="sxs-lookup"><span data-stu-id="fc03f-158">Invoice</span></span> | <span data-ttu-id="fc03f-159">Summa kandevaluutas</span><span class="sxs-lookup"><span data-stu-id="fc03f-159">Amount in transaction currency</span></span> | <span data-ttu-id="fc03f-160">Valuuta</span><span class="sxs-lookup"><span data-stu-id="fc03f-160">Currency</span></span> | <span data-ttu-id="fc03f-161">Tasakaalustatav summa</span><span class="sxs-lookup"><span data-stu-id="fc03f-161">Amount to settle</span></span> |
|--------------------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="fc03f-162">Valitud ja esile tõstetud</span><span class="sxs-lookup"><span data-stu-id="fc03f-162">Selected and highlighted</span></span> | <span data-ttu-id="fc03f-163">Tavaline</span><span class="sxs-lookup"><span data-stu-id="fc03f-163">Normal</span></span>            | <span data-ttu-id="fc03f-164">Inv-10030</span><span class="sxs-lookup"><span data-stu-id="fc03f-164">Inv-10030</span></span> | <span data-ttu-id="fc03f-165">3052</span><span class="sxs-lookup"><span data-stu-id="fc03f-165">3052</span></span>    | <span data-ttu-id="fc03f-166">28.06.2015</span><span class="sxs-lookup"><span data-stu-id="fc03f-166">6/28/2015</span></span>          | <span data-ttu-id="fc03f-167">12.07.2015</span><span class="sxs-lookup"><span data-stu-id="fc03f-167">7/12/2015</span></span> | <span data-ttu-id="fc03f-168">10030</span><span class="sxs-lookup"><span data-stu-id="fc03f-168">10030</span></span>   | <span data-ttu-id="fc03f-169">‑2000,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-169">-2,000.00</span></span>                      | <span data-ttu-id="fc03f-170">USA dollar</span><span class="sxs-lookup"><span data-stu-id="fc03f-170">USD</span></span>      | <span data-ttu-id="fc03f-171">‑1980,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-171">-1,980.00</span></span>        |
| <span data-ttu-id="fc03f-172">Valitud</span><span class="sxs-lookup"><span data-stu-id="fc03f-172">Selected</span></span>                 | <span data-ttu-id="fc03f-173">Tavaline</span><span class="sxs-lookup"><span data-stu-id="fc03f-173">Normal</span></span>            | <span data-ttu-id="fc03f-174">APP‑10030</span><span class="sxs-lookup"><span data-stu-id="fc03f-174">APP-10030</span></span> | <span data-ttu-id="fc03f-175">3052</span><span class="sxs-lookup"><span data-stu-id="fc03f-175">3052</span></span>    | <span data-ttu-id="fc03f-176">15.07.2015</span><span class="sxs-lookup"><span data-stu-id="fc03f-176">7/15/2015</span></span>          | <span data-ttu-id="fc03f-177">15.07.2015</span><span class="sxs-lookup"><span data-stu-id="fc03f-177">7/15/2015</span></span> |         | <span data-ttu-id="fc03f-178">500,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-178">500.00</span></span>                         | <span data-ttu-id="fc03f-179">USA dollar</span><span class="sxs-lookup"><span data-stu-id="fc03f-179">USD</span></span>      | <span data-ttu-id="fc03f-180">500,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-180">500.00</span></span>           |

<span data-ttu-id="fc03f-181">Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas.</span><span class="sxs-lookup"><span data-stu-id="fc03f-181">Discount information appears at the bottom of the **Settle open transactions** page.</span></span> <span data-ttu-id="fc03f-182">Võetakse skonto summas 20,00, kuna tasakaalustatav summa arvel on vaikesumma 1980,00.</span><span class="sxs-lookup"><span data-stu-id="fc03f-182">The discount amount that is taken is 20.00, because the amount to settle for the invoice is the default amount, 1,980.00.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="fc03f-183">Skonto kuupäev</span><span class="sxs-lookup"><span data-stu-id="fc03f-183">Cash discount date</span></span>           | <span data-ttu-id="fc03f-184">12.07.2015</span><span class="sxs-lookup"><span data-stu-id="fc03f-184">7/12/2015</span></span> |
| <span data-ttu-id="fc03f-185">Skonto summa</span><span class="sxs-lookup"><span data-stu-id="fc03f-185">Cash discount amount</span></span>         | <span data-ttu-id="fc03f-186">‑20,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-186">-20.00</span></span>    |
| <span data-ttu-id="fc03f-187">Kasuta skontot</span><span class="sxs-lookup"><span data-stu-id="fc03f-187">Use cash discount</span></span>            | <span data-ttu-id="fc03f-188">Tavaline</span><span class="sxs-lookup"><span data-stu-id="fc03f-188">Normal</span></span>    |
| <span data-ttu-id="fc03f-189">Võetud skonto</span><span class="sxs-lookup"><span data-stu-id="fc03f-189">Cash discount taken</span></span>          | <span data-ttu-id="fc03f-190">0,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-190">0.00</span></span>      |
| <span data-ttu-id="fc03f-191">Skonto summa võtmiseks</span><span class="sxs-lookup"><span data-stu-id="fc03f-191">Cash discount amount to take</span></span> | <span data-ttu-id="fc03f-192">‑20,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-192">-20.00</span></span>    |

<span data-ttu-id="fc03f-193">April värskendab välja **Tasakaalustatav summa** väärtuseks **500,00**.</span><span class="sxs-lookup"><span data-stu-id="fc03f-193">April updates the value in the **Amount to settle** field to **500.00**.</span></span> <span data-ttu-id="fc03f-194">Välja **Skonto summa võtmiseks** väärtuseks arvutatakse **5,05**.</span><span class="sxs-lookup"><span data-stu-id="fc03f-194">The value in the **Cash discount amount to take** field is calculated as **5.05**.</span></span>

| <span data-ttu-id="fc03f-195">Märge</span><span class="sxs-lookup"><span data-stu-id="fc03f-195">Mark</span></span>                     | <span data-ttu-id="fc03f-196">Kasuta skontot</span><span class="sxs-lookup"><span data-stu-id="fc03f-196">Use cash discount</span></span> | <span data-ttu-id="fc03f-197">Kanne</span><span class="sxs-lookup"><span data-stu-id="fc03f-197">Voucher</span></span>   | <span data-ttu-id="fc03f-198">Konto</span><span class="sxs-lookup"><span data-stu-id="fc03f-198">Account</span></span> | <span data-ttu-id="fc03f-199">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="fc03f-199">Date</span></span>      | <span data-ttu-id="fc03f-200">Tähtaeg</span><span class="sxs-lookup"><span data-stu-id="fc03f-200">Due date</span></span>  | <span data-ttu-id="fc03f-201">Arve</span><span class="sxs-lookup"><span data-stu-id="fc03f-201">Invoice</span></span> | <span data-ttu-id="fc03f-202">Summa kandevaluutas</span><span class="sxs-lookup"><span data-stu-id="fc03f-202">Amount in transaction currency</span></span> | <span data-ttu-id="fc03f-203">Valuuta</span><span class="sxs-lookup"><span data-stu-id="fc03f-203">Currency</span></span> | <span data-ttu-id="fc03f-204">Tasakaalustatav summa</span><span class="sxs-lookup"><span data-stu-id="fc03f-204">Amount to settle</span></span> |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="fc03f-205">Valitud ja esile tõstetud</span><span class="sxs-lookup"><span data-stu-id="fc03f-205">Selected and highlighted</span></span> | <span data-ttu-id="fc03f-206">Tavaline</span><span class="sxs-lookup"><span data-stu-id="fc03f-206">Normal</span></span>            | <span data-ttu-id="fc03f-207">Inv-10030</span><span class="sxs-lookup"><span data-stu-id="fc03f-207">Inv-10030</span></span> | <span data-ttu-id="fc03f-208">3052</span><span class="sxs-lookup"><span data-stu-id="fc03f-208">3052</span></span>    | <span data-ttu-id="fc03f-209">28.06.2015</span><span class="sxs-lookup"><span data-stu-id="fc03f-209">6/28/2015</span></span> | <span data-ttu-id="fc03f-210">12.07.2015</span><span class="sxs-lookup"><span data-stu-id="fc03f-210">7/12/2015</span></span> | <span data-ttu-id="fc03f-211">10030</span><span class="sxs-lookup"><span data-stu-id="fc03f-211">10030</span></span>   | <span data-ttu-id="fc03f-212">2000,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-212">2,000.00</span></span>                       | <span data-ttu-id="fc03f-213">USA dollar</span><span class="sxs-lookup"><span data-stu-id="fc03f-213">USD</span></span>      | <span data-ttu-id="fc03f-214">‑500,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-214">-500.00</span></span>          |
| <span data-ttu-id="fc03f-215">Valitud</span><span class="sxs-lookup"><span data-stu-id="fc03f-215">Selected</span></span>                 | <span data-ttu-id="fc03f-216">Tavaline</span><span class="sxs-lookup"><span data-stu-id="fc03f-216">Normal</span></span>            | <span data-ttu-id="fc03f-217">APP‑10030</span><span class="sxs-lookup"><span data-stu-id="fc03f-217">APP-10030</span></span> | <span data-ttu-id="fc03f-218">3052</span><span class="sxs-lookup"><span data-stu-id="fc03f-218">3052</span></span>    | <span data-ttu-id="fc03f-219">15.07.2015</span><span class="sxs-lookup"><span data-stu-id="fc03f-219">7/15/2015</span></span> | <span data-ttu-id="fc03f-220">15.07.2015</span><span class="sxs-lookup"><span data-stu-id="fc03f-220">7/15/2015</span></span> |         | <span data-ttu-id="fc03f-221">500,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-221">500.00</span></span>                         | <span data-ttu-id="fc03f-222">USA dollar</span><span class="sxs-lookup"><span data-stu-id="fc03f-222">USD</span></span>      | <span data-ttu-id="fc03f-223">500,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-223">500.00</span></span>           |

<span data-ttu-id="fc03f-224">Teave märgitud arve allahindluse kohta kuvatakse lehe **Avatud kannete tasakaalustamine** allosas.</span><span class="sxs-lookup"><span data-stu-id="fc03f-224">Discount information appears at the bottom of the **Settle open transactions** page.</span></span> <span data-ttu-id="fc03f-225">Välja **Skonto summa võtmiseks** väärtus on **5,05**, kuna tasakaalustatav summa arvel muudeti maksesummaks 500,00.</span><span class="sxs-lookup"><span data-stu-id="fc03f-225">The value in the **Cash discount amount to take** field is **5.05**, because the amount to settle for the invoice was changed to the payment amount, 500.00.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="fc03f-226">Skonto kuupäev</span><span class="sxs-lookup"><span data-stu-id="fc03f-226">Cash discount date</span></span>           | <span data-ttu-id="fc03f-227">12.07.2015</span><span class="sxs-lookup"><span data-stu-id="fc03f-227">7/12/2015</span></span> |
| <span data-ttu-id="fc03f-228">Skonto summa</span><span class="sxs-lookup"><span data-stu-id="fc03f-228">Cash discount amount</span></span>         | <span data-ttu-id="fc03f-229">‑20,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-229">-20.00</span></span>    |
| <span data-ttu-id="fc03f-230">Kasuta skontot</span><span class="sxs-lookup"><span data-stu-id="fc03f-230">Use cash discount</span></span>            | <span data-ttu-id="fc03f-231">Tavaline</span><span class="sxs-lookup"><span data-stu-id="fc03f-231">Normal</span></span>    |
| <span data-ttu-id="fc03f-232">Võetud skonto</span><span class="sxs-lookup"><span data-stu-id="fc03f-232">Cash discount taken</span></span>          | <span data-ttu-id="fc03f-233">0,00</span><span class="sxs-lookup"><span data-stu-id="fc03f-233">0.00</span></span>      |
| <span data-ttu-id="fc03f-234">Skonto summa võtmiseks</span><span class="sxs-lookup"><span data-stu-id="fc03f-234">Cash discount amount to take</span></span> | <span data-ttu-id="fc03f-235">‑5,05</span><span class="sxs-lookup"><span data-stu-id="fc03f-235">-5.05</span></span>     |




