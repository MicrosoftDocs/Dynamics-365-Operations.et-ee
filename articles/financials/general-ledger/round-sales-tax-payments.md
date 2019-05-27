---
title: Käibemaksu maksed ja ümardamisreeglid
description: See artikkel selgitab, kuidas toimib ümardamisreegli seadistus moodulis Käibemaksuhaldurid ja kuidas ümardada käibemaksusaldot töö Käibemaksu tasakaalustamine ja sisestamine käigus.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1c1bb1c792eb79888a1df209f2eebaf14a38dd
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1531853"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="a4522-103">Käibemaksu maksed ja ümardamisreeglid</span><span class="sxs-lookup"><span data-stu-id="a4522-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4522-104">See artikkel selgitab, kuidas toimib ümardamisreegli seadistus moodulis Käibemaksuhaldurid ja kuidas ümardada käibemaksusaldot töö Käibemaksu tasakaalustamine ja sisestamine käigus.</span><span class="sxs-lookup"><span data-stu-id="a4522-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="a4522-105">Käibemaksu kohta tuleb perioodiliselt maksuametile aruandeid esitada ja see tasuda.</span><span class="sxs-lookup"><span data-stu-id="a4522-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="a4522-106">Seda saab teha, käivitades tasakaalustamise ja sisestades käibemaksuprotsessi lehel Käibemaks.</span><span class="sxs-lookup"><span data-stu-id="a4522-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="a4522-107">Perioodi käibemaks tasakaalustatakse käibemaksukontodega ja käibemaksusaldo sisestatakse käibemaksu tasakaalustuskontole.</span><span class="sxs-lookup"><span data-stu-id="a4522-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="a4522-108">Käibemaksusaldo, mis sisestatakse käibemaksu tasakaalustuskontole, saab maksuameti nõude järgi ümardada, seadistades lehel Käibemaks ümardamisreegli.</span><span class="sxs-lookup"><span data-stu-id="a4522-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="a4522-109">Ümardamise erinevus sisestatakse käibemaksu ümardamise kontole, mis on valitud pearaamatus väljal Automaatsete kannete kontod.</span><span class="sxs-lookup"><span data-stu-id="a4522-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="a4522-110">Allolev näide selgitab lehel Käibemaksuhaldur ümardamisreegli toimimise põhimõtet.</span><span class="sxs-lookup"><span data-stu-id="a4522-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="a4522-111">Näited</span><span class="sxs-lookup"><span data-stu-id="a4522-111">Examples</span></span>

<span data-ttu-id="a4522-112">Perioodi kogu käibemaksu krediidisaldo on –98 765,43.</span><span class="sxs-lookup"><span data-stu-id="a4522-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="a4522-113">Juriidiline isik kogus rohkem käibemaksu kui ise tasus.</span><span class="sxs-lookup"><span data-stu-id="a4522-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="a4522-114">Seetõttu võlgneb juriidiline isik maksuametile raha.</span><span class="sxs-lookup"><span data-stu-id="a4522-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="a4522-115">Juriidiline isik soovib kasutada ümardamismeetodit, mis ümardab saldo lähima täisarvuni (1,00).</span><span class="sxs-lookup"><span data-stu-id="a4522-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="a4522-116">Käibemaksu arvestamise eest vastutav kasutaja peab tegema järgmist.</span><span class="sxs-lookup"><span data-stu-id="a4522-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="a4522-117">Klõpsake valikuid Maks &gt; Kaudsed maksud &gt; Käibemaks &gt; Käibemaksuhaldurid</span><span class="sxs-lookup"><span data-stu-id="a4522-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="a4522-118">Valige kiirkaardi Üldine väljalt Ümardamise vorm suvand Tavaline.</span><span class="sxs-lookup"><span data-stu-id="a4522-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="a4522-119">Sisestage väljale Ümardus väärtus 1,00.</span><span class="sxs-lookup"><span data-stu-id="a4522-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="a4522-120">Kui saabub aeg tasuda maksuametile käibemaks, avage leht Käibemaksu tasakaalustamine ja sisestamine.</span><span class="sxs-lookup"><span data-stu-id="a4522-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="a4522-121">(Klõpsake valikuid Maks &gt; Deklaratsioonid &gt; Käibemaks &gt; Käibemaksu tasakaalustamine ja sisestamine.)</span><span class="sxs-lookup"><span data-stu-id="a4522-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="a4522-122">Käibemaksu tasakaalustamise kontol ümardatakse maksukohustuse summa 98 765,43 summale 98 765.</span><span class="sxs-lookup"><span data-stu-id="a4522-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="a4522-123">Järgmine tabel näitab, kuidas ümardatakse summat 98 765,43, kasutades iga ümardusmeetodit, mis on saadaval lehe Käibemaksuhaldurid väljal Ümardamise vorm.</span><span class="sxs-lookup"><span data-stu-id="a4522-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="a4522-124">Ümardamise vormi suvand</span><span class="sxs-lookup"><span data-stu-id="a4522-124">Rounding form option</span></span>                | <span data-ttu-id="a4522-125">Ümardamisväärtus = 0,01</span><span class="sxs-lookup"><span data-stu-id="a4522-125">Round-off value = 0.01</span></span> | <span data-ttu-id="a4522-126">Ümardamisväärtus = 0,10</span><span class="sxs-lookup"><span data-stu-id="a4522-126">Round-off value = 0.10</span></span> | <span data-ttu-id="a4522-127">Ümardamisväärtus = 1,00</span><span class="sxs-lookup"><span data-stu-id="a4522-127">Round-off value = 1.00</span></span> | <span data-ttu-id="a4522-128">Ümardamisväärtus = 100,00</span><span class="sxs-lookup"><span data-stu-id="a4522-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="a4522-129">Tavaline</span><span class="sxs-lookup"><span data-stu-id="a4522-129">Normal</span></span>                              | <span data-ttu-id="a4522-130">98 765,43</span><span class="sxs-lookup"><span data-stu-id="a4522-130">98,765.43</span></span>              | <span data-ttu-id="a4522-131">98 765,40</span><span class="sxs-lookup"><span data-stu-id="a4522-131">98,765.40</span></span>              | <span data-ttu-id="a4522-132">98 765,00</span><span class="sxs-lookup"><span data-stu-id="a4522-132">98,765.00</span></span>              | <span data-ttu-id="a4522-133">98 800,00</span><span class="sxs-lookup"><span data-stu-id="a4522-133">98,800.00</span></span>                |
| <span data-ttu-id="a4522-134">Allapoole</span><span class="sxs-lookup"><span data-stu-id="a4522-134">Downward</span></span>                            | <span data-ttu-id="a4522-135">98 765,43</span><span class="sxs-lookup"><span data-stu-id="a4522-135">98,765.43</span></span>              | <span data-ttu-id="a4522-136">98 765,40</span><span class="sxs-lookup"><span data-stu-id="a4522-136">98,765.40</span></span>              | <span data-ttu-id="a4522-137">98 765,00</span><span class="sxs-lookup"><span data-stu-id="a4522-137">98,765.00</span></span>              | <span data-ttu-id="a4522-138">98 700,00</span><span class="sxs-lookup"><span data-stu-id="a4522-138">98,700.00</span></span>                |
| <span data-ttu-id="a4522-139">Ümardamine</span><span class="sxs-lookup"><span data-stu-id="a4522-139">Rounding-up</span></span>                         | <span data-ttu-id="a4522-140">98 765,43</span><span class="sxs-lookup"><span data-stu-id="a4522-140">98,765.43</span></span>              | <span data-ttu-id="a4522-141">98 765,50</span><span class="sxs-lookup"><span data-stu-id="a4522-141">98,765.50</span></span>              | <span data-ttu-id="a4522-142">98 766,00</span><span class="sxs-lookup"><span data-stu-id="a4522-142">98,766.00</span></span>              | <span data-ttu-id="a4522-143">98 800,00</span><span class="sxs-lookup"><span data-stu-id="a4522-143">98,800.00</span></span>                |
| <span data-ttu-id="a4522-144">Oma eelis kreeditsaldo puhul</span><span class="sxs-lookup"><span data-stu-id="a4522-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="a4522-145">98 765,43</span><span class="sxs-lookup"><span data-stu-id="a4522-145">98,765.43</span></span>              | <span data-ttu-id="a4522-146">98 765,40</span><span class="sxs-lookup"><span data-stu-id="a4522-146">98,765.40</span></span>              | <span data-ttu-id="a4522-147">98 765,00</span><span class="sxs-lookup"><span data-stu-id="a4522-147">98,765.00</span></span>              | <span data-ttu-id="a4522-148">98 700,00</span><span class="sxs-lookup"><span data-stu-id="a4522-148">98,700.00</span></span>                |
| <span data-ttu-id="a4522-149">Oma eelis deebetsaldo puhul</span><span class="sxs-lookup"><span data-stu-id="a4522-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="a4522-150">98 765,43</span><span class="sxs-lookup"><span data-stu-id="a4522-150">98,765.43</span></span>              | <span data-ttu-id="a4522-151">98 765,50</span><span class="sxs-lookup"><span data-stu-id="a4522-151">98,765.50</span></span>              | <span data-ttu-id="a4522-152">98 766,00</span><span class="sxs-lookup"><span data-stu-id="a4522-152">98,766.00</span></span>              | <span data-ttu-id="a4522-153">98 800,00</span><span class="sxs-lookup"><span data-stu-id="a4522-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="a4522-154">Ümardamist pole, kui ümardamisväärtus on 0,00</span><span class="sxs-lookup"><span data-stu-id="a4522-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="a4522-155">round(1,0151, 0,00) = 1,0151 round(1,0149, 0,00) = 1,0149</span><span class="sxs-lookup"><span data-stu-id="a4522-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="a4522-156">Tavaline ümardamine, ümardamistäpsus on 0,01</span><span class="sxs-lookup"><span data-stu-id="a4522-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="a4522-157">Ümardamine</span><span class="sxs-lookup"><span data-stu-id="a4522-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="a4522-158">Arvutamisprotsess</span><span class="sxs-lookup"><span data-stu-id="a4522-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="a4522-159">round(1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="a4522-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="a4522-160">round(1,015 / 0,01, 0) = round(101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="a4522-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="a4522-161">102 × 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="a4522-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="a4522-162">round(1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="a4522-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="a4522-163">round(1,014 / 0,01, 0) = round(101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="a4522-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="a4522-164">101 × 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="a4522-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="a4522-165">round(1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="a4522-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="a4522-166">round(1,011 / 0,02, 0) = round(50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="a4522-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="a4522-167">51 × 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="a4522-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="a4522-168">round(1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="a4522-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="a4522-169">round(1,009 / 0,02, 0) = round(50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="a4522-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="a4522-170">50 × 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="a4522-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="a4522-171">Kui valite suvandi Oma eelis, toimub ümardamine alati juriidilise isiku kasuks.</span><span class="sxs-lookup"><span data-stu-id="a4522-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="a4522-172">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="a4522-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="a4522-173">Käibemaksu ülevaade</span><span class="sxs-lookup"><span data-stu-id="a4522-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="a4522-174">Käibemaksumakse loomine</span><span class="sxs-lookup"><span data-stu-id="a4522-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="a4522-175">Müügikannete loomine dokumentidel</span><span class="sxs-lookup"><span data-stu-id="a4522-175">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="a4522-176">Sisestatud käibemaksukannete kuvamine</span><span class="sxs-lookup"><span data-stu-id="a4522-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="a4522-177">Ümardamisfunktsioon</span><span class="sxs-lookup"><span data-stu-id="a4522-177">round Function</span></span>](https://msdn.microsoft.com/en-us/library/aa850656.aspx)


