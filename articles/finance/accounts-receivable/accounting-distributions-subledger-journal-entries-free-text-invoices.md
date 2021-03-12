---
title: Arvestuse jaotused ja töölehekirjed vabas vormis arvete puhul
description: Arvestuse jaotused määratlevad, kuidas summat arvestatakse, näiteks tulu, maksude või tasude arvestamisel vabas vormis arvel. Igal summal, mida tuleb vabas vormis arve töölehele kandmisel arvestada, on üks või mitu arvestuse jaotust.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f3ee26825ec48a8e8e32401ceaa8c80ecd679d2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993189"
---
# <a name="accounting-distributions-and-subledger-entries-for-free-text-invoices"></a><span data-ttu-id="b7bef-104">Arvestuse jaotused ja alammooduli kirjed vabas vormis arvete puhul</span><span class="sxs-lookup"><span data-stu-id="b7bef-104">Accounting distributions and subledger entries for free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7bef-105">Arvestuse jaotused määratlevad, kuidas summat arvestatakse, näiteks tulu, maksude või tasude arvestamisel vabas vormis arvel.</span><span class="sxs-lookup"><span data-stu-id="b7bef-105">Accounting distributions are used to define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span> <span data-ttu-id="b7bef-106">Igal summal, mida tuleb vabas vormis arve töölehele kandmisel arvestada, on üks või mitu arvestuse jaotust.</span><span class="sxs-lookup"><span data-stu-id="b7bef-106">Every amount that must be accounted for when the free text invoice is journalized will have one or more accounting distributions.</span></span>

<a name="accounting-distributions"></a><span data-ttu-id="b7bef-107">Arvestuse jaotused</span><span class="sxs-lookup"><span data-stu-id="b7bef-107">Accounting distributions</span></span>
------------------------

<span data-ttu-id="b7bef-108">Saate kasutada järgmisi nuppe lehel Vabas vormis arve iga vabas vormis arve summa arvestuse jaotuse vaatamiseks ja võimaluse korral muutmiseks.</span><span class="sxs-lookup"><span data-stu-id="b7bef-108">You can use the following buttons in the Free text invoice page to view, and possibly change, the accounting distributions for each amount on the free text invoice.</span></span>

-   <span data-ttu-id="b7bef-109">**Summade jaotamine** –saate kuvada ja muuta arvestuse jaotusi üksiku rea ning alamridade kohta (nt maksud või tasud).</span><span class="sxs-lookup"><span data-stu-id="b7bef-109">**Distribute amounts**—View and change the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="b7bef-110">Saate kuvada ja muuta ka alamrea arvestuse jaotusi otse lehelt Käibemaksukanded või Tasude kanded.</span><span class="sxs-lookup"><span data-stu-id="b7bef-110">You can also view and change the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="b7bef-111">Saate vabas vormis arve päise summasid (nt tasusid või valuuta ümardamissummasid) muuta.</span><span class="sxs-lookup"><span data-stu-id="b7bef-111">Change free text invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="b7bef-112">Saate vabas vormis arve reasummasid muuta.</span><span class="sxs-lookup"><span data-stu-id="b7bef-112">Change free text invoice line amounts.</span></span>
-   <span data-ttu-id="b7bef-113">**Jaotuste kuvamine**–arvestuste jaotuste kuvamine kõigi dokumendi ridade kohta.</span><span class="sxs-lookup"><span data-stu-id="b7bef-113">**View distributions**—View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="b7bef-114">Selles vaates arvestuse jaotusi muuta ei saa.</span><span class="sxs-lookup"><span data-stu-id="b7bef-114">You can't change the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="b7bef-115">Päise ja rea summade vaatamine.</span><span class="sxs-lookup"><span data-stu-id="b7bef-115">View header and line amounts.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="b7bef-116">Summade jaotamine</span><span class="sxs-lookup"><span data-stu-id="b7bef-116">Distributing amounts</span></span>
<span data-ttu-id="b7bef-117">Vabas vormis arve sisestamisel jaotatakse iga summa järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b7bef-117">When you enter a free text invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7bef-118">Rahasumma tüüp</span><span class="sxs-lookup"><span data-stu-id="b7bef-118">Type of monetary amount</span></span></th>
<th><span data-ttu-id="b7bef-119">Põhikonto kuvamise koht</span><span class="sxs-lookup"><span data-stu-id="b7bef-119">Where the main account is displayed from</span></span></th>
<th><span data-ttu-id="b7bef-120">Prioriteetsusjärjestus, mis määrab, milline finantsdimensiooni vaikeväärtus kuvatakse</span><span class="sxs-lookup"><span data-stu-id="b7bef-120">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7bef-121">Vabas vormis arve rida</span><span class="sxs-lookup"><span data-stu-id="b7bef-121">Free text invoice line</span></span></td>
<td><span data-ttu-id="b7bef-122">Vabas vormis arve rea pearaamatukonto.</span><span class="sxs-lookup"><span data-stu-id="b7bef-122">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="b7bef-123">Kui põhikonto on eraldamiskonto, kasutage eraldamiskonto määratluse vaikeväärtust.</span><span class="sxs-lookup"><span data-stu-id="b7bef-123">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="b7bef-124">Kui põhikonto ei ole eraldamise konto, kasutage vabas vormis arve real finantsdimensiooni vaikemalli.</span><span class="sxs-lookup"><span data-stu-id="b7bef-124">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b7bef-125">Saate kasutada vabas vormis arve real finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="b7bef-125">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b7bef-126">Saate kasutada lehel Kontoplaan pearaamatukonto finantsdimensiooni vaikeväärtusi.</span><span class="sxs-lookup"><span data-stu-id="b7bef-126">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bef-127">Vabas vormis arve rida põhivara numbri ja väärtusmudeli kombinatsiooni jaoks</span><span class="sxs-lookup"><span data-stu-id="b7bef-127">Free text invoice line for a fixed asset number and value model combination</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b7bef-128"><strong>Märkus. </strong></span><span class="sxs-lookup"><span data-stu-id="b7bef-128"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7bef-129">Vabas vormis arve real olev põhikonto on põhivara likvideerimiskonto.</span><span class="sxs-lookup"><span data-stu-id="b7bef-129">The main account on the free text invoice line will be the fixed asset disposal account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
<td><span data-ttu-id="b7bef-130">Vabas vormis arve rea pearaamatukonto.</span><span class="sxs-lookup"><span data-stu-id="b7bef-130">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="b7bef-131">Saate kasutada vabas vormis arve real finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="b7bef-131">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b7bef-132">Saate kasutada lehel Kontoplaan pearaamatukonto finantsdimensiooni vaikeväärtusi.</span><span class="sxs-lookup"><span data-stu-id="b7bef-132">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bef-133">Vabas vormis arve allahindluse summa</span><span class="sxs-lookup"><span data-stu-id="b7bef-133">Free text invoice discount amount</span></span></td>
<td><span data-ttu-id="b7bef-134">Kliendi allahindluste välja põhikonto lehel Skontod.</span><span class="sxs-lookup"><span data-stu-id="b7bef-134">The Main account for customer discounts field in the Cash discounts page.</span></span></td>
<td><ol>
<li><span data-ttu-id="b7bef-135">Kui põhikonto on eraldamiskonto, kasutage eraldamiskonto määratluse vaikeväärtust.</span><span class="sxs-lookup"><span data-stu-id="b7bef-135">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="b7bef-136">Kui põhikonto ei ole eraldamise konto, kasutage vabas vormis arve real finantsdimensiooni vaikemalli.</span><span class="sxs-lookup"><span data-stu-id="b7bef-136">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b7bef-137">Saate kasutada vabas vormis arve real finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="b7bef-137">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b7bef-138">Saate kasutada lehel Kontoplaan pearaamatukonto finantsdimensiooni vaikeväärtusi.</span><span class="sxs-lookup"><span data-stu-id="b7bef-138">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bef-139">Vabas vormis arve käibemaksusumma</span><span class="sxs-lookup"><span data-stu-id="b7bef-139">Free text invoice sales tax amount</span></span></td>
<td><span data-ttu-id="b7bef-140">Tasumisele kuuluva käibemaksu väli lehel Pearaamatu sisestamisgrupid.</span><span class="sxs-lookup"><span data-stu-id="b7bef-140">The Sales tax payable field in the Ledger posting groups page.</span></span></td>
<td><ol>
<li><span data-ttu-id="b7bef-141">Kasutage vabas vormis arve rea summas või tasurea summa jaotustes määratud finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="b7bef-141">Use the financial dimensions that are defined on the free text invoice line amount or the distributions for the charge line amount.</span></span></li>
<li><span data-ttu-id="b7bef-142">Saate kasutada vabas vormis arve real finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="b7bef-142">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b7bef-143">Saate kasutada lehel Kontoplaan pearaamatukonto finantsdimensiooni vaikeväärtusi.</span><span class="sxs-lookup"><span data-stu-id="b7bef-143">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bef-144">Vabas vormis arve tasurea summa</span><span class="sxs-lookup"><span data-stu-id="b7bef-144">Free text invoice charge line amount</span></span></td>
<td><span data-ttu-id="b7bef-145">Väli Kreeditkonto lehel Tasukood.</span><span class="sxs-lookup"><span data-stu-id="b7bef-145">The Credit account field in the Charges code page.</span></span></td>
<td><ol>
<li><span data-ttu-id="b7bef-146">Kui põhikonto on eraldamiskonto, kasutage eraldamiskonto määratluse vaikeväärtust.</span><span class="sxs-lookup"><span data-stu-id="b7bef-146">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="b7bef-147">Kui põhikonto ei ole eraldamise konto, kasutage vabas vormis arve real finantsdimensiooni vaikemalli.</span><span class="sxs-lookup"><span data-stu-id="b7bef-147">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b7bef-148">Saate kasutada vabas vormis arve real finantsdimensiooni väärtusi.</span><span class="sxs-lookup"><span data-stu-id="b7bef-148">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="b7bef-149">Saate kasutada lehel Kontoplaan pearaamatukonto finantsdimensiooni vaikeväärtusi.</span><span class="sxs-lookup"><span data-stu-id="b7bef-149">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a><span data-ttu-id="b7bef-150">Maksude jaotamine</span><span class="sxs-lookup"><span data-stu-id="b7bef-150">Distributing taxes</span></span>
<span data-ttu-id="b7bef-151">Maksude arvestuse jaotusi ei saa luua, kuni makse arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="b7bef-151">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="b7bef-152">Käibemaksu arvutamiseks peate täitma ühe järgmise ülesande vabas vormis arve vormil.</span><span class="sxs-lookup"><span data-stu-id="b7bef-152">To calculate sales taxes, you must complete one of the following tasks in the Free text invoice form:</span></span>
-   <span data-ttu-id="b7bef-153">Käibemaksu kuvamine.</span><span class="sxs-lookup"><span data-stu-id="b7bef-153">View the sales tax.</span></span>
-   <span data-ttu-id="b7bef-154">Arve kogusumma kuvamine.</span><span class="sxs-lookup"><span data-stu-id="b7bef-154">View the invoice total.</span></span>
-   <span data-ttu-id="b7bef-155">Saate kuvada rahavoo.</span><span class="sxs-lookup"><span data-stu-id="b7bef-155">View the cash flow.</span></span>
-   <span data-ttu-id="b7bef-156">Saate kuvada kogu vabas vormis arve arvestuse jaotused.</span><span class="sxs-lookup"><span data-stu-id="b7bef-156">View accounting distributions for the whole free text invoice.</span></span>
-   <span data-ttu-id="b7bef-157">Alammooduli töölehe kuvamine.</span><span class="sxs-lookup"><span data-stu-id="b7bef-157">View the subledger journal.</span></span>

## <a name="subledger-journals-for-free-text-invoices"></a><span data-ttu-id="b7bef-158"> Vabas vormis arvete alammooduli töölehed</span><span class="sxs-lookup"><span data-stu-id="b7bef-158">Subledger journals for free text invoices</span></span>
<span data-ttu-id="b7bef-159">Enne vabas vormis arve sisestamist saate vaadata arve täielikku raamatupidamiskirjet, mis sisaldab deebet- ja kreeditsummasid, kontrollimaks, et arve sisestatakse õigetele kontodele.</span><span class="sxs-lookup"><span data-stu-id="b7bef-159">Before you post a free text invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="b7bef-160">Selles vaates nimetatakse täielikku raamatupidamiskirjet alammooduli tööleheks.</span><span class="sxs-lookup"><span data-stu-id="b7bef-160">This view of the full accounting entry is called a subledger journal.</span></span> <span data-ttu-id="b7bef-161">Kui alammooduli töölehe kirje on enne vabas vormis arve töölehele paigutamist vale, ei saa alammooduli töölehe kirjet muuta.</span><span class="sxs-lookup"><span data-stu-id="b7bef-161">If the subledger journal entry is incorrect when you preview it before you journalize the free text invoice, you can't change the subledger journal entry.</span></span> <span data-ttu-id="b7bef-162">Selle asemel peate muutma arvestuse jaotusi või sisestusreegleid.</span><span class="sxs-lookup"><span data-stu-id="b7bef-162">Instead, you must change the accounting distributions or the posting profile.</span></span> <span data-ttu-id="b7bef-163">Arvestuse jaotuste abil määratletakse raamatupidamiskirje üks pool, deebet- või kreeditsumma.</span><span class="sxs-lookup"><span data-stu-id="b7bef-163">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="b7bef-164">Alammooduli töölehe konto kirje vastaskonto luuakse sisestusreeglite abil, nt kliendi konto või maksu põhjal.</span><span class="sxs-lookup"><span data-stu-id="b7bef-164">The offsetting subledger journal account entry is created from the posting profiles, such as from the customer account or the tax.</span></span>



