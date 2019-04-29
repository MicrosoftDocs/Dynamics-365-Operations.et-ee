---
title: Arvestuse jaotused ja alammooduli töölehe kirjed hankijaarvete puhul
description: Arvestuse jaotuste abil saate määratleda, kuidas summat arvestatakse, näiteks kulude, maksude või tasude arvestamisel hankija arvel. Igal summal, mida tuleb hankija arve töölehele kandmisel arvestada, on üks või mitu arvestuse jaotust.
author: abruer
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b75b1c8d98c15579909bd8816f2f7df8e6a5ba0
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/25/2019
ms.locfileid: "896737"
---
# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a><span data-ttu-id="db3fd-104">Arvestuse jaotused ja alammooduli töölehe kirjed hankijaarvete puhul</span><span class="sxs-lookup"><span data-stu-id="db3fd-104">Accounting distributions and subledger journal entries for vendor invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db3fd-105">Arvestuse jaotuste abil saate määratleda, kuidas summat arvestatakse, näiteks kulude, maksude või tasude arvestamisel hankija arvel.</span><span class="sxs-lookup"><span data-stu-id="db3fd-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="db3fd-106">Igal summal, mida tuleb hankija arve töölehele kandmisel arvestada, on üks või mitu arvestuse jaotust.</span><span class="sxs-lookup"><span data-stu-id="db3fd-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

<a name="accounting-distributions"></a><span data-ttu-id="db3fd-107">Arvestuse jaotused</span><span class="sxs-lookup"><span data-stu-id="db3fd-107">Accounting distributions</span></span> 
-------------------------

<span data-ttu-id="db3fd-108">Saate kasutada lehel Hankija arve iga hankija arve summa arvestuse jaotuse vaatamiseks ja võimaluse korral muutmiseks järgmisi nuppe.</span><span class="sxs-lookup"><span data-stu-id="db3fd-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="db3fd-109">**Summade jaotamine** – saate kuvada ja muuta arvestuse jaotusi üksiku rea ja alamüksuste ridade kohta (nt maksud või tasud).</span><span class="sxs-lookup"><span data-stu-id="db3fd-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="db3fd-110">Saate kuvada ja muuta ka alamrea arvestuse jaotusi otse lehelt Käibemaksukanded või Tasude kanded.</span><span class="sxs-lookup"><span data-stu-id="db3fd-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="db3fd-111">Hankija arve päise summad, nt tasud või valuuta ümardamissummad.</span><span class="sxs-lookup"><span data-stu-id="db3fd-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="db3fd-112">Hankija arve rea summade muutmine.</span><span class="sxs-lookup"><span data-stu-id="db3fd-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="db3fd-113">**Jaotuste kuvamine**– saate kuvada arvestuste jaotused kõigi dokumendi ridade kohta.</span><span class="sxs-lookup"><span data-stu-id="db3fd-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="db3fd-114">Selles vaates arvestuse jaotusi muuta ei saa.</span><span class="sxs-lookup"><span data-stu-id="db3fd-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="db3fd-115">Päise ja rea summade vaatamine.</span><span class="sxs-lookup"><span data-stu-id="db3fd-115">View header and line amounts.</span></span>

<span data-ttu-id="db3fd-116">Kui hankija arve viitab ostutellimusele, saate tükeldada ja muuta arvestuse jaotusi ridade puhul, mis sisaldavad ladustamata kaupa.</span><span class="sxs-lookup"><span data-stu-id="db3fd-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="db3fd-117">Kui hankija arve rida ei viita ostutellimuse reale, saate ka arvestuse jaotuse kustutada.</span><span class="sxs-lookup"><span data-stu-id="db3fd-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="db3fd-118">Tasude, maksude ja rea allahindluste ridu ei saa tükeldada ega kustutada.</span><span class="sxs-lookup"><span data-stu-id="db3fd-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="db3fd-119">Saate pearaamatukontot muuta, kuid te ei saa muuta summasid ega protsente.</span><span class="sxs-lookup"><span data-stu-id="db3fd-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="db3fd-120">Kui peamine rida sisaldab üksust, mida pole ladustatud, ja arvestuse jaotused on tükeldatud, tükeldatakse alamüksuse read automaatselt nii, et need vastaksid peamise rea finantsdimensioonidele.</span><span class="sxs-lookup"><span data-stu-id="db3fd-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="db3fd-121">Alamüksuse rea arvestuse jaotusi ei saa täiendavalt tükeldada ega kustutada, kuid sõltuvalt alamüksuse seadistusest võib teil olla võimalik muuta alamüksuse rea arvestuse jaotuse pearaamatukontot.</span><span class="sxs-lookup"><span data-stu-id="db3fd-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="db3fd-122">Summade jaotamine</span><span class="sxs-lookup"><span data-stu-id="db3fd-122">Distributing amounts</span></span>
<span data-ttu-id="db3fd-123">Hankija arve sisestamisel jaotatakse iga summa järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="db3fd-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db3fd-124">Hankija arve rea tüüp</span><span class="sxs-lookup"><span data-stu-id="db3fd-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="db3fd-125">Prioriteetsusjärjestus, mis määrab, kust põhikonto kuvatakse</span><span class="sxs-lookup"><span data-stu-id="db3fd-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="db3fd-126">Prioriteetsusjärjestus, mis määrab, milline finantsdimensiooni vaikeväärtus kuvatakse</span><span class="sxs-lookup"><span data-stu-id="db3fd-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db3fd-127">Ladustatav toode</span><span class="sxs-lookup"><span data-stu-id="db3fd-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="db3fd-128">Ostutellimuse rea arvestuse jaotus.</span><span class="sxs-lookup"><span data-stu-id="db3fd-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-129">Põhikonto väli, kui lehel Sisestamine on valitud suvand Toote ostukulu.</span><span class="sxs-lookup"><span data-stu-id="db3fd-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="db3fd-130">Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</span><span class="sxs-lookup"><span data-stu-id="db3fd-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-131">Saate kasutada hankija arve finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db3fd-132">Hankekategooria või toode, mis pole ladustatud</span><span class="sxs-lookup"><span data-stu-id="db3fd-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="db3fd-133">Ostutellimuse rea arvestuse jaotus, kui hankija arve rida viitab ostutellimuse reale.</span><span class="sxs-lookup"><span data-stu-id="db3fd-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-134">Põhikonto väli, kui lehel Sisestamine on valitud suvand Kulu ostukulu.</span><span class="sxs-lookup"><span data-stu-id="db3fd-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="db3fd-135">Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</span><span class="sxs-lookup"><span data-stu-id="db3fd-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-136">Kui põhikonto on eraldamiskonto, kasutage eraldamiskonto määratluse vaikeväärtust.</span><span class="sxs-lookup"><span data-stu-id="db3fd-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="db3fd-137">Saate kasutada hankija arve finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="db3fd-138">Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="db3fd-139">Saate kasutada lehel Kontoplaan põhikonto finantsdimensiooni vaikeväärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db3fd-140">Põhivarad</span><span class="sxs-lookup"><span data-stu-id="db3fd-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="db3fd-141">Ostutellimuse rea arvestuse jaotus, kui hankija arve rida viitab ostutellimuse reale.</span><span class="sxs-lookup"><span data-stu-id="db3fd-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-142">Põhikonto väli, kui vormi Hankija arve väljal Kande tüüp on valitud suvand Soetus ja lehel Põhivara sisestusreeglid valitakse suvand Soetus.</span><span class="sxs-lookup"><span data-stu-id="db3fd-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="db3fd-143">Põhikonto väli, kui vormi Hankija arve väljal Kande tüüp on valitud suvand Soetuse korrigeerimine ja lehel Põhivara sisestusreeglid valitakse suvand Soetuse korrigeerimine.</span><span class="sxs-lookup"><span data-stu-id="db3fd-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="db3fd-144">Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</span><span class="sxs-lookup"><span data-stu-id="db3fd-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-145">Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="db3fd-146">Saate kasutada lehel Kontoplaan põhikonto finantsdimensiooni vaikeväärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db3fd-147">Hankija arve real määratletud projekt</span><span class="sxs-lookup"><span data-stu-id="db3fd-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="db3fd-148">Ostutellimuse rea arvestuse jaotus, kui arve rida viitab ostutellimuse reale.</span><span class="sxs-lookup"><span data-stu-id="db3fd-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-149">Põhikonto väli, kui lehe Projektigrupid väljal Sisesta kulud – kaup on valitud suvand Saldo ja lehel Pearaamatu sisestamise seadistus valitakse suvand Kulu.</span><span class="sxs-lookup"><span data-stu-id="db3fd-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="db3fd-150">Põhikonto väli, kui lehe Projektigrupid väljal Sisesta kulud – kaup on valitud suvand Kasub ja kahjum ning lehel Pearaamatu sisestamise seadistus valitakse suvand Kulu – kaup.</span><span class="sxs-lookup"><span data-stu-id="db3fd-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="db3fd-151">Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</span><span class="sxs-lookup"><span data-stu-id="db3fd-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db3fd-152">Rea allahindlus</span><span class="sxs-lookup"><span data-stu-id="db3fd-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="db3fd-153">Ostutellimuse rea arvestuse jaotus, kui arve rida viitab ostutellimuse reale.</span><span class="sxs-lookup"><span data-stu-id="db3fd-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-154">Põhikonto väli, kui lehel Sisestamine valitakse suvand Allahindlus.</span><span class="sxs-lookup"><span data-stu-id="db3fd-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="db3fd-155">Kui allahindluse põhikonto pole sisestusreeglites määratletud, siis laiendatud hinna arvestuse jaotus ostutellimuse real.</span><span class="sxs-lookup"><span data-stu-id="db3fd-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="db3fd-156">Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul arvestuse jaotust.</span><span class="sxs-lookup"><span data-stu-id="db3fd-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-157">Kasutage hankija arve rea laiendatud hinna puhul arvestuse jaotuste finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="db3fd-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="db3fd-158">Saate kasutada hankija arve real finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="db3fd-159">Saate kasutada lehel Kontoplaan põhikonto finantsdimensiooni vaikeväärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db3fd-160">Ostukulu, mis sisestatakse ostutellimuse rea vahekaardile Hind ja allahindlus</span><span class="sxs-lookup"><span data-stu-id="db3fd-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="db3fd-161">Ostutellimuse rea arvestuse jaotus, kui arve rida viitab ostutellimuse reale.</span><span class="sxs-lookup"><span data-stu-id="db3fd-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-162">Laiendatud hinna arvestuse jaotus ostutellimuse real.</span><span class="sxs-lookup"><span data-stu-id="db3fd-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="db3fd-163">Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</span><span class="sxs-lookup"><span data-stu-id="db3fd-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-164">Kasutage hankija arve rea laiendatud hinna puhul arvestuse jaotuste finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="db3fd-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db3fd-165">Reatasu</span><span class="sxs-lookup"><span data-stu-id="db3fd-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="db3fd-166">Ostutellimuse rea arvestuse jaotus, kui arve rida viitab ostutellimuse reale.</span><span class="sxs-lookup"><span data-stu-id="db3fd-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-167">Deebetkonto väli lehel Tasukood, kui vormi Tasukood väljal Deebeti tüüp on valitud suvand Pearaamatukonto.</span><span class="sxs-lookup"><span data-stu-id="db3fd-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="db3fd-168">Laiendatud hinna arvestuse jaotus ostutellimuse real, kui vormi Tasukood väljal Deebeti tüüp on valitud suvand Kaup.</span><span class="sxs-lookup"><span data-stu-id="db3fd-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-169">Kreeditkonto väli lehel Tasukood, kui vormi Tasukood väljal Deebeti tüüp on valitud suvand Klient/hankija.</span><span class="sxs-lookup"><span data-stu-id="db3fd-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="db3fd-170">Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</span><span class="sxs-lookup"><span data-stu-id="db3fd-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-171">Kasutage hankija arve rea laiendatud hinna puhul arvestuse jaotuste finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="db3fd-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="db3fd-172">Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="db3fd-173">Saate kasutada lehel Kontoplaan põhikonto finantsdimensiooni vaikeväärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db3fd-174">Maks, järgmise tingimusega.</span><span class="sxs-lookup"><span data-stu-id="db3fd-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="db3fd-175">Lehel Pearaamatu parameetrid on märgitud ruut Rakenda USA maksureeglid.</span><span class="sxs-lookup"><span data-stu-id="db3fd-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="db3fd-176">Ostutellimuse rea arvestuse jaotus, kui arve rida viitab ostutellimuse reale.</span><span class="sxs-lookup"><span data-stu-id="db3fd-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-177">Laiendatud hinna või tasu arvestuse jaotus.</span><span class="sxs-lookup"><span data-stu-id="db3fd-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="db3fd-178">Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</span><span class="sxs-lookup"><span data-stu-id="db3fd-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-179">Kasutage hankija arve rea laiendatud hinna puhul arvestuse jaotuste finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="db3fd-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="db3fd-180">Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db3fd-181">Maks, järgmiste tingimustega.</span><span class="sxs-lookup"><span data-stu-id="db3fd-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="db3fd-182">Lehel Pearaamatu parameetrid on tühjendatud ruut Rakenda USA maksureeglid.</span><span class="sxs-lookup"><span data-stu-id="db3fd-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="db3fd-183">Lehel Käibemaksugrupid on käibemaksugrupi puhul ruut Kasuta maksu tühjendatud.</span><span class="sxs-lookup"><span data-stu-id="db3fd-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="db3fd-184">Väli Saadaolev käibemaks lehel Pearaamatu sisestusgrupid, kui maksusumma on tagastatav.</span><span class="sxs-lookup"><span data-stu-id="db3fd-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="db3fd-185">Kui maksusumma pole tagastatav, siis laiendatud hind või tasu arvestuse jaotus.</span><span class="sxs-lookup"><span data-stu-id="db3fd-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="db3fd-186">Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</span><span class="sxs-lookup"><span data-stu-id="db3fd-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-187">Kasutage hankija arve rea tasu puhul laiendatud hinna või arvestuse jaotuste finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="db3fd-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="db3fd-188">Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="db3fd-189">Saate kasutada lehel Kontoplaan põhikonto finantsdimensiooni vaikeväärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db3fd-190">Maks, järgmiste tingimustega.</span><span class="sxs-lookup"><span data-stu-id="db3fd-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="db3fd-191">Lehel Pearaamatu parameetrid on tühjendatud ruut Rakenda USA maksureeglid.</span><span class="sxs-lookup"><span data-stu-id="db3fd-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="db3fd-192">Lehel Käibemaksugrupid on käibemaksugrupi puhul ruut Kasuta maksu märgitud.</span><span class="sxs-lookup"><span data-stu-id="db3fd-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="db3fd-193">Väli Saadaolev käibemaks lehel Pearaamatu sisestusgrupid, kui maksusumma on tagastatav.</span><span class="sxs-lookup"><span data-stu-id="db3fd-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="db3fd-194">Väli Kasutusmaksu kulu lehel Pearaamatu sisestusgrupid, kui maksusumma ei ole tagastatav.</span><span class="sxs-lookup"><span data-stu-id="db3fd-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="db3fd-195">Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</span><span class="sxs-lookup"><span data-stu-id="db3fd-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-196">Kasutage hankija arve rea tasu puhul laiendatud hinna või arvestuse jaotuste finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="db3fd-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="db3fd-197">Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="db3fd-198">Saate kasutada lehel Kontoplaan põhikonto finantsdimensiooni vaikeväärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db3fd-199">Päise tasu</span><span class="sxs-lookup"><span data-stu-id="db3fd-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="db3fd-200">Deebetkonto väli lehel Tasukood, kui vormi Tasukood väljal Deebeti tüüp on valitud suvand Pearaamatukonto.</span><span class="sxs-lookup"><span data-stu-id="db3fd-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="db3fd-201">Kreeditkonto väli lehel Tasukood, kui vormi Tasukood väljal Deebeti tüüp on valitud suvand Klient/hankija.</span><span class="sxs-lookup"><span data-stu-id="db3fd-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="db3fd-202">Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</span><span class="sxs-lookup"><span data-stu-id="db3fd-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-203">Kui põhikonto on eraldamiskonto, kasutage eraldamiskonto määratluse vaikeväärtust.</span><span class="sxs-lookup"><span data-stu-id="db3fd-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="db3fd-204">Saate kasutada hankija arve päise finantsdimensiooni vaikemalli väärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="db3fd-205">Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="db3fd-206">Saate kasutada lehel Kontoplaan põhikonto finantsdimensiooni vaikeväärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db3fd-207">Päise allahindlus</span><span class="sxs-lookup"><span data-stu-id="db3fd-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="db3fd-208">Põhikonto väli lehe Automaatsete kannete kontod sisestustüübi Hankija arve allahindlus puhul.</span><span class="sxs-lookup"><span data-stu-id="db3fd-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="db3fd-209">Kui arve rida viitab ostutellimuse reale, kasutage ostutellimuse rea puhul konto jaotust.</span><span class="sxs-lookup"><span data-stu-id="db3fd-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="db3fd-210">Kasutage hankija arve rea laiendatud hinna puhul arvestuse jaotuste finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="db3fd-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="db3fd-211">Saate kasutada hankija arve rea finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="db3fd-212">Saate kasutada lehel Kontoplaan põhikonto finantsdimensiooni vaikeväärtusi.</span><span class="sxs-lookup"><span data-stu-id="db3fd-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a><span data-ttu-id="db3fd-213">Maksude jaotamine</span><span class="sxs-lookup"><span data-stu-id="db3fd-213">Distributing taxes</span></span>
------------------

<span data-ttu-id="db3fd-214">Maksude arvestuse jaotusi ei saa luua, kuni makse arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="db3fd-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="db3fd-215">Käibemaksu arvutamiseks peate täitma lehel Hankija arve ühe järgmise ülesande.</span><span class="sxs-lookup"><span data-stu-id="db3fd-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="db3fd-216">Arve kogusumma kuvamine.</span><span class="sxs-lookup"><span data-stu-id="db3fd-216">View the invoice total.</span></span>
-   <span data-ttu-id="db3fd-217">Käibemaksu kuvamine.</span><span class="sxs-lookup"><span data-stu-id="db3fd-217">View the sales tax.</span></span>
-   <span data-ttu-id="db3fd-218">Alammooduli töölehe kuvamine.</span><span class="sxs-lookup"><span data-stu-id="db3fd-218">View the subledger journal.</span></span>
-   <span data-ttu-id="db3fd-219">Hankija koguarve arvestuse jaotuste kuvamine.</span><span class="sxs-lookup"><span data-stu-id="db3fd-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="db3fd-220">Hankija arve ootele panemine.</span><span class="sxs-lookup"><span data-stu-id="db3fd-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="db3fd-221">Hankija arve sisestamine.</span><span class="sxs-lookup"><span data-stu-id="db3fd-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="db3fd-222">Hankija arvete alammooduli töölehed</span><span class="sxs-lookup"><span data-stu-id="db3fd-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="db3fd-223">Enne hankija arve sisestamist saate vaadata arve täielikku raamatupidamiskirjet, mis sisaldab deebet- ja kreeditsummasid, kontrollimaks, et arve sisestatakse õigetele kontodele.</span><span class="sxs-lookup"><span data-stu-id="db3fd-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="db3fd-224">Selles vaates nimetatakse täielikku raamatupidamiskirjet alammooduli tööleheks.</span><span class="sxs-lookup"><span data-stu-id="db3fd-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="db3fd-225">Kui alammooduli töölehe kirje on enne hankija arve töölehele paigutamist vale, ei saa te alammooduli töölehe kirjet muuta.</span><span class="sxs-lookup"><span data-stu-id="db3fd-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="db3fd-226">Selle asemel peate muutma arvestuse jaotusi või sisestusreegleid.</span><span class="sxs-lookup"><span data-stu-id="db3fd-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="db3fd-227">Arvestuse jaotuste abil määratletakse raamatupidamiskirje üks pool, deebet- või kreeditsumma.</span><span class="sxs-lookup"><span data-stu-id="db3fd-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="db3fd-228">Alammooduli töölehe konto kirje vastaskonto luuakse sisestusreegleid kasutades, nt hankija konto või maksu põhjal.</span><span class="sxs-lookup"><span data-stu-id="db3fd-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>





