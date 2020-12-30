---
title: Rendi sisestamise tüübid
description: Selles teemas kirjeldatakse vara rentimise kannete jaoks kasutatavaid sisestamise tüüpe.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ceb4fbeb4dbf2f535e05a9d46c84169435d2803b
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442575"
---
# <a name="lease-posting-types"></a><span data-ttu-id="75d87-103">Rendi sisestamise tüübid</span><span class="sxs-lookup"><span data-stu-id="75d87-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75d87-104">Selles teemas kirjeldatakse vara rentimise kannete jaoks kasutatavaid sisestamise tüüpe.</span><span class="sxs-lookup"><span data-stu-id="75d87-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="75d87-105">Rendivara</span><span class="sxs-lookup"><span data-stu-id="75d87-105">Lease asset</span></span>

<span data-ttu-id="75d87-106">Konto on seostatud kasutamisõiguse esemeks oleva varaga.</span><span class="sxs-lookup"><span data-stu-id="75d87-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="75d87-107">Seda kontot debiteeritakse, kui rendikirje algselt tuvastatakse uue rendi raamatupidamise standardites, raamatupidamise standardite kodeerimise teemas 842 (ASC 842) ja rahvusvahelise finantsaruandluse standardis 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="75d87-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="75d87-108">Muudetud rendikirje puhul võidakse seda kontot kas debiteerida või krediteerida, sõltuvalt sellest, kas muudatus suurendab või vähendab rendikohustist.</span><span class="sxs-lookup"><span data-stu-id="75d87-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="75d87-109">**Töölehe kirjete näide:** esialgne tuvastamine</span><span class="sxs-lookup"><span data-stu-id="75d87-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="75d87-110">**Deebet:** renditav vara XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="75d87-111">**Kreedit:** rendikohustis XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="75d87-112">Rendikohustis</span><span class="sxs-lookup"><span data-stu-id="75d87-112">Lease liability</span></span>

<span data-ttu-id="75d87-113">Konto on seostatud rendikohustisega, mis tekib, kui maksed diskonteeritakse uute IFRS 16 ja ASC 842 standardite alusel.</span><span class="sxs-lookup"><span data-stu-id="75d87-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="75d87-114">See konto krediteeritakse, kui rendikirje uute standardite alusel esmakordselt tuvastatakse.</span><span class="sxs-lookup"><span data-stu-id="75d87-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="75d87-115">See debiteeritakse rendimaksete ja krediteeritakse intressi laekumiste suhtes.</span><span class="sxs-lookup"><span data-stu-id="75d87-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="75d87-116">**Töölehe kirjete näide:** esialgne tuvastamine</span><span class="sxs-lookup"><span data-stu-id="75d87-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="75d87-117">**Deebet:** renditav vara XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="75d87-118">**Kreedit:** rendikohustis XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="75d87-119">**Töölehe kirjete näide:** intressi laekumine</span><span class="sxs-lookup"><span data-stu-id="75d87-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="75d87-120">**Deebet:** intressikulu XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="75d87-121">**Kreedit:** rendikohustis XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="75d87-122">**Töölehe kirjete näide:** rendimakse</span><span class="sxs-lookup"><span data-stu-id="75d87-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="75d87-123">**Deebet:** rendikohustis XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="75d87-124">**Kreedit:** hankija reskontro / rendimakse XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="75d87-125">Lühiajalise rendilepingu kohustis</span><span class="sxs-lookup"><span data-stu-id="75d87-125">Short-term lease liability</span></span>

<span data-ttu-id="75d87-126">Konto on seostatud lühiajalise rendikohustisega, kui sisestatakse lühiajalise rendikohustise ümberklassifitseerimise töölehe kirje.</span><span class="sxs-lookup"><span data-stu-id="75d87-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="75d87-127">Seda kontot krediteeritakse kuu viimasel päeval lühiajalise kohustise amortiseerimise graafikuga.</span><span class="sxs-lookup"><span data-stu-id="75d87-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="75d87-128">Samas järgmise kuu esimesel päeval sama summa debiteeritakse.</span><span class="sxs-lookup"><span data-stu-id="75d87-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="75d87-129">**Töölehe kirjete näide:** lühiajalise rendikohustise ümberklassifitseerimine</span><span class="sxs-lookup"><span data-stu-id="75d87-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="75d87-130">**Deebet:** rendikohustis XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="75d87-131">**Kreedit:** lühiajaline rendikohustis XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="75d87-132">**Deebet:** lühiajaline rendikohustis XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="75d87-133">**Kreedit:** rendikohustis XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="75d87-134">Kulumi kulu</span><span class="sxs-lookup"><span data-stu-id="75d87-134">Depreciation expense</span></span>

<span data-ttu-id="75d87-135">Konto on seostatud kuluga, mis on seotud kasutamisõiguse esemeks oleva vara kulumiga vastavalt standardile IFRS 16, ASC 842 ja kapitalirendi tingimustel vastavalt standardile IAS 17 ja ASC 840.</span><span class="sxs-lookup"><span data-stu-id="75d87-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="75d87-136">Seda kontot debiteeritakse, kui kasutamisõiguse esemeks olev vara iga kuu kantakse kulumisse.</span><span class="sxs-lookup"><span data-stu-id="75d87-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="75d87-137">**Töölehe kirjete näide:** kulumi laekumine</span><span class="sxs-lookup"><span data-stu-id="75d87-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="75d87-138">**Deebet:** kulumi kulu XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="75d87-139">**Kreedit:** kogunenud kulum XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="75d87-140">Kasum/kahjum rendi muutmisel</span><span class="sxs-lookup"><span data-stu-id="75d87-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="75d87-141">Konto on seostatud mis tahes kasumi või kahjumiga, mis tulenevad rendi muudatustest.</span><span class="sxs-lookup"><span data-stu-id="75d87-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="75d87-142">Rendi muutumise ajal võib tekkida kasum, kui muudatus vähendab rendikohustist summa võrra, mis ületab kasutamisõiguse esemeks oleva vara bilansilist väärtust.</span><span class="sxs-lookup"><span data-stu-id="75d87-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="75d87-143">Näiteks on rendikirjel praegu rendikohustise bilansiline väärtus 150 000 eurot ja kasutamisõiguse esemeks oleva vara bilansiline väärtus 100 000 eurot.</span><span class="sxs-lookup"><span data-stu-id="75d87-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="75d87-144">Renti muudetakse ja see muudatus tekitab uue tulevaste minimaalsete rendimaksete praeguse väärtuse (PVFMLP) 40 000 eurot.</span><span class="sxs-lookup"><span data-stu-id="75d87-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="75d87-145">Seega rendikohustist debiteeritakse summas 110 000 eurot (150 000 – 40 000).</span><span class="sxs-lookup"><span data-stu-id="75d87-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="75d87-146">Kuna kasutamisõiguse esemeks oleva vara väärtus on ainult 100 000 eurot, vähendab see vara väärtuse alla nulli (0).</span><span class="sxs-lookup"><span data-stu-id="75d87-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="75d87-147">Seetõttu on raamatupidamise juhendis sätestatud, et ülejäänu tuleks kirjendada kasumi kontole.</span><span class="sxs-lookup"><span data-stu-id="75d87-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="75d87-148">Sellisel juhul on töölehe lõplikuks kirjeks rendikohustise deebet summas 110 000 eurot, rendi vara kreedit summas 100 000 eurot ja kasumi konto kreedit summas 10 000 eurot.</span><span class="sxs-lookup"><span data-stu-id="75d87-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="75d87-149">**Töölehe kirjete näide:** rendi muutmine</span><span class="sxs-lookup"><span data-stu-id="75d87-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="75d87-150">**Deebet:** rendikohustis XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="75d87-151">**Kreedit:** renditav vara XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="75d87-152">**Kreedit:** kasum XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="75d87-153">Akumuleeritud kulum</span><span class="sxs-lookup"><span data-stu-id="75d87-153">Accumulated depreciation</span></span>

<span data-ttu-id="75d87-154">Konto on seotud kasutamisõiguse esemeks oleva vara kontrakontoga.</span><span class="sxs-lookup"><span data-stu-id="75d87-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="75d87-155">Seda kontot krediteeritakse kulumi kulu sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="75d87-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="75d87-156">**Töölehe kirjete näide:** kulumi laekumine</span><span class="sxs-lookup"><span data-stu-id="75d87-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="75d87-157">**Deebet:** kulumi kulu XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="75d87-158">**Kreedit:** kogunenud kulum XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="retained-earnings"></a><span data-ttu-id="75d87-159">Jaotamata kasum</span><span class="sxs-lookup"><span data-stu-id="75d87-159">Retained earnings</span></span>

<span data-ttu-id="75d87-160">Konto on seostatud kinnipeetud tuludega.</span><span class="sxs-lookup"><span data-stu-id="75d87-160">The account is associated with retained earnings.</span></span> <span data-ttu-id="75d87-161">Seda kontot on võimalik kas debiteerida või krediteerida ülemineku korrigeerimise töölehe kirjel, kasutades täielikku tagasiulatuvat meetodit või kumulatiivset järelkulu valiku A meetodil.</span><span class="sxs-lookup"><span data-stu-id="75d87-161">This account might be either debited or credited in a transition adjustment journal entry by using the full retrospective method or the cumulative catch-up option A method.</span></span> <span data-ttu-id="75d87-162">Erinevus esialgse kasutamisõiguse esemeks oleva vara ja rendikohustise vahel kirjendatakse kinnipeetud tuludena.</span><span class="sxs-lookup"><span data-stu-id="75d87-162">The difference between the initial ROU asset and lease liability is booked to retained earnings.</span></span> <span data-ttu-id="75d87-163">Harvadel juhtudel võib jaotamata kasumit mõjutada ka rendi muutmine, kui rendi klassifikatsioon muutub finantseerimisest kasutusele, et hinnata kasutamisõiguse esemeks olev vara üles või alla, et see oleks kapitalirendiga võrdne.</span><span class="sxs-lookup"><span data-stu-id="75d87-163">In rare cases, the retained earnings might also be affected during lease modification, if the classification of a lease is changed from finance to operating to write the ROU asset up or down so that it equals the lease liability.</span></span>

<span data-ttu-id="75d87-164">**Töölehe kirjete näidis:** siirde korrigeerimine (täielikult tagasiulatuv või kumulatiivse järelkulu valiku A meetod)</span><span class="sxs-lookup"><span data-stu-id="75d87-164">**Example journal entries:** Transition adjustment (full retrospective or cumulative catch-up option A method)</span></span><br>
<span data-ttu-id="75d87-165">**Deebet:** rendikohustis XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-165">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="75d87-166">**Kreedit:** renditav vara XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-166">**Credit:** Lease asset XXX</span></span><br>
<span data-ttu-id="75d87-167">**Kreedit:** jaotamata kasum XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-167">**Credit:** Retained earnings XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="75d87-168">Muutuv makse</span><span class="sxs-lookup"><span data-stu-id="75d87-168">Variable payment</span></span>

<span data-ttu-id="75d87-169">Konto on seotud muutuvate rendimaksetega, mis luuakse indeksi ümberhindamise poolt vastavalt standardite ASC 842, ASC 840 ja IAS 17 liisingutele.</span><span class="sxs-lookup"><span data-stu-id="75d87-169">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="75d87-170">Rendi maksegraafikus on muutuvad maksed lisatud veergu **Muutuv makse**.</span><span class="sxs-lookup"><span data-stu-id="75d87-170">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="75d87-171">Seda konto debiteeritakse, kui arve luuakse maksegraafiku rea suhtes, mis sisaldab muutuvat makset.</span><span class="sxs-lookup"><span data-stu-id="75d87-171">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="75d87-172">**Töölehe kirjete näide:** rendimakse</span><span class="sxs-lookup"><span data-stu-id="75d87-172">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="75d87-173">**Deebet:** rendikohustis XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-173">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="75d87-174">**Deebet:** muutuv makse XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-174">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="75d87-175">**Kreedit:** hankija reskontro / rendimakse XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-175">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="75d87-176">Edasilükatud rendi vara (kohustis)</span><span class="sxs-lookup"><span data-stu-id="75d87-176">Deferred rent asset (liability)</span></span>

<span data-ttu-id="75d87-177">Konto on seostatud edasilükatud rendi varaga või kohustisega, mis on loodud edasilükatud rendi töötlemise rendi poolt.</span><span class="sxs-lookup"><span data-stu-id="75d87-177">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="75d87-178">Seda kontot debiteeritakse, kui arve sisestatakse edasilükatud üüri töötlemise rendikirjega, kui rendimakse summa on suurem kui perioodi lineaarse rendi kulu.</span><span class="sxs-lookup"><span data-stu-id="75d87-178">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="75d87-179">See krediteeritakse, kui rendimakse on väiksem kui perioodi lineaarse rendi kulu.</span><span class="sxs-lookup"><span data-stu-id="75d87-179">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="75d87-180">**Töölehe kirjete näide:** rendimakse (edasilükatud rendi töötlemise rent)</span><span class="sxs-lookup"><span data-stu-id="75d87-180">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="75d87-181">**Deebet:** rendikulu XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-181">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="75d87-182">**Kreedit:** edasilükatud rendi kohustis XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-182">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="75d87-183">**Kreedit:** hankija reskontro / rendimakse XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-183">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="75d87-184">Rendikulu</span><span class="sxs-lookup"><span data-stu-id="75d87-184">Lease expense</span></span>

<span data-ttu-id="75d87-185">Konto on seostatud rendi kuluga, kui rent on klassifitseeritud kui edasilükatud rent.</span><span class="sxs-lookup"><span data-stu-id="75d87-185">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="75d87-186">Seda kontot debiteeritakse, kui arve sisestatakse edasilükatud üüri töötlemise suhtes.</span><span class="sxs-lookup"><span data-stu-id="75d87-186">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="75d87-187">**Töölehe kirjete näide:** rendimakse (edasilükatud rendi töötlemise rent)</span><span class="sxs-lookup"><span data-stu-id="75d87-187">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="75d87-188">**Deebet:** rendikulu XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-188">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="75d87-189">**Kreedit:** edasilükatud rendi kohustis XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-189">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="75d87-190">**Kreedit:** hankija reskontro / rendimakse XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-190">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="75d87-191">Väärtuse languse kulu</span><span class="sxs-lookup"><span data-stu-id="75d87-191">Impairment expense</span></span>

<span data-ttu-id="75d87-192">Konto sisestatakse siis, kui rent on mõjutatud.</span><span class="sxs-lookup"><span data-stu-id="75d87-192">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="75d87-193">Seda kontot debiteeritakse, samas kui kasutamisõiguse esemeks oleva vara konto on otse krediteeritud.</span><span class="sxs-lookup"><span data-stu-id="75d87-193">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="75d87-194">**Töölehe kirjete näide:** rendimakse</span><span class="sxs-lookup"><span data-stu-id="75d87-194">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="75d87-195">**Deebet:** väärtuse languse kulu XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-195">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="75d87-196">**Kreedit:** kasutamisõiguse esemeks olev vara XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-196">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="75d87-197">Rendimakse</span><span class="sxs-lookup"><span data-stu-id="75d87-197">Lease payment</span></span>

<span data-ttu-id="75d87-198">Konto sisestatakse, kui **Hankijale maksmine** parameetrid on välja lülitatud.</span><span class="sxs-lookup"><span data-stu-id="75d87-198">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="75d87-199">Kui parameeter on välja lülitatud, krediteeritakse hankija tasutava asemel seda kontot.</span><span class="sxs-lookup"><span data-stu-id="75d87-199">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="75d87-200">**Töölehe kirjete näide:** rendimakse</span><span class="sxs-lookup"><span data-stu-id="75d87-200">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="75d87-201">**Deebet:** rendikohustis XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-201">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="75d87-202">**Krediteerimine:** rendimakse XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-202">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="75d87-203">Kulutüübi sisestused</span><span class="sxs-lookup"><span data-stu-id="75d87-203">Expense type postings</span></span>

<span data-ttu-id="75d87-204">Iga kulutüübi jaoks valitud konto debiteeritakse, kui selle kulu tüübi jaoks on loodud makse.</span><span class="sxs-lookup"><span data-stu-id="75d87-204">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="75d87-205">Näiteks debiteeritakse kulutüübi **Kindlustus** jaoks määratud kontot iga kord, kui kindlustuse täitekulu ajakavast loodud arve või makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="75d87-205">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="75d87-206">**Töölehe kirjete näide:** kindlustuse makse</span><span class="sxs-lookup"><span data-stu-id="75d87-206">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="75d87-207">**Deebet:** kindlustuse kulutüübi konto XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-207">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="75d87-208">**Kreedit:** nihkekonto XXX</span><span class="sxs-lookup"><span data-stu-id="75d87-208">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="75d87-209">Nihkekonto valitakse täitekulu maksegraafikule rendi tasemel.</span><span class="sxs-lookup"><span data-stu-id="75d87-209">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="75d87-210">Selle nihkekonto saab seostada hankija või pearaamatu konto.</span><span class="sxs-lookup"><span data-stu-id="75d87-210">This offset account can associated with the vendor, or with a ledger account.</span></span>
