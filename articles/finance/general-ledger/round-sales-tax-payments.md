---
title: Käibemaksu maksed ja ümardamisreeglid
description: See artikkel selgitab, kuidas toimib ümardamisreegli seadistus moodulis Käibemaksuhaldurid ja kuidas ümardada käibemaksusaldot töö Käibemaksu tasakaalustamine ja sisestamine käigus.
author: ShylaThompson
manager: AnnBe
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 998dbd01352d3fa5040187e81b564d14133464db
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4014955"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="4a318-103">Käibemaksu maksed ja ümardamisreeglid</span><span class="sxs-lookup"><span data-stu-id="4a318-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a318-104">See artikkel selgitab, kuidas toimib ümardamisreegli seadistus moodulis Käibemaksuhaldurid ja kuidas ümardada käibemaksusaldot töö Käibemaksu tasakaalustamine ja sisestamine käigus.</span><span class="sxs-lookup"><span data-stu-id="4a318-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="4a318-105">Käibemaksu kohta tuleb perioodiliselt maksuametile aruandeid esitada ja see tasuda.</span><span class="sxs-lookup"><span data-stu-id="4a318-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="4a318-106">Seda saab teha, käivitades tasakaalustamise ja sisestades käibemaksuprotsessi lehel Käibemaks.</span><span class="sxs-lookup"><span data-stu-id="4a318-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="4a318-107">Perioodi käibemaks tasakaalustatakse käibemaksukontodega ja käibemaksusaldo sisestatakse käibemaksu tasakaalustuskontole.</span><span class="sxs-lookup"><span data-stu-id="4a318-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="4a318-108">Käibemaksusaldo, mis sisestatakse käibemaksu tasakaalustuskontole, saab maksuameti nõude järgi ümardada, seadistades lehel Käibemaks ümardamisreegli.</span><span class="sxs-lookup"><span data-stu-id="4a318-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="4a318-109">Ümardamise erinevus sisestatakse käibemaksu ümardamise kontole, mis on valitud pearaamatus väljal Automaatsete kannete kontod.</span><span class="sxs-lookup"><span data-stu-id="4a318-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="4a318-110">Allolev näide selgitab lehel Käibemaksuhaldur ümardamisreegli toimimise põhimõtet.</span><span class="sxs-lookup"><span data-stu-id="4a318-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="4a318-111">Näited</span><span class="sxs-lookup"><span data-stu-id="4a318-111">Examples</span></span>

<span data-ttu-id="4a318-112">Perioodi kogu käibemaksu krediidisaldo on –98 765,43.</span><span class="sxs-lookup"><span data-stu-id="4a318-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="4a318-113">Juriidiline isik kogus rohkem käibemaksu kui ise tasus.</span><span class="sxs-lookup"><span data-stu-id="4a318-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="4a318-114">Seetõttu võlgneb juriidiline isik maksuametile raha.</span><span class="sxs-lookup"><span data-stu-id="4a318-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="4a318-115">Juriidiline isik soovib kasutada ümardamismeetodit, mis ümardab saldo lähima täisarvuni (1,00).</span><span class="sxs-lookup"><span data-stu-id="4a318-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="4a318-116">Käibemaksu arvestamise eest vastutav kasutaja peab tegema järgmist.</span><span class="sxs-lookup"><span data-stu-id="4a318-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1. <span data-ttu-id="4a318-117">Klõpsake suvandeid **Maks** > **Kaudsed maksud** > **Käibemaks** > **Käibemaksuhaldurid**.</span><span class="sxs-lookup"><span data-stu-id="4a318-117">Click **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
2. <span data-ttu-id="4a318-118">Valige kiirkaardi **Üldine** väljalt **Ümardamise vorm** suvand **Tavaline**.</span><span class="sxs-lookup"><span data-stu-id="4a318-118">On the **General** FastTab, in the **Rounding form** field, select **Normal**.</span></span>
3. <span data-ttu-id="4a318-119">Sisestage väljale **Ümardus** väärtus 1,00.</span><span class="sxs-lookup"><span data-stu-id="4a318-119">In the **Round-off** field, enter 1.00.</span></span>
4. <span data-ttu-id="4a318-120">Kui saabub aeg tasuda maksuametile käibemaks, avage **Maks** > **Deklaratsioonid** > **Käibemaks** > **Käibemaksu tasakaalustamine ja sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="4a318-120">When it is time to pay the sales taxes to the tax authority, go to **Tax** > **Declarations** > **Sales tax** > **Settle and post sale tax**.</span></span> <span data-ttu-id="4a318-121">Käibemaksu tasakaalustamise kontol näete, et maksukohustuse summa **98 765,43** ümardatakse summale **98 765**.</span><span class="sxs-lookup"><span data-stu-id="4a318-121">On the sales tax settlement account, you can see that the tax liability amount of **98,765.43** is rounded to **98,765**.</span></span>

<span data-ttu-id="4a318-122">Järgmine tabel näitab, kuidas ümardatakse summat 98 765,43, kasutades iga ümardusmeetodit, mis on saadaval lehe **Käibemaksuhaldurid** väljal **Ümardamise vorm**.</span><span class="sxs-lookup"><span data-stu-id="4a318-122">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the **Rounding form** field in the **Sales tax authorities** page.</span></span>

> [!NOTE]                                                                                  
> <span data-ttu-id="4a318-123">Kui ümardamisväärtuseks on seatud 0,00, siis kehtib järgmine.</span><span class="sxs-lookup"><span data-stu-id="4a318-123">If the round-off value is set as 0.00, then:</span></span>
>
> - <span data-ttu-id="4a318-124">Tavalise ümardamise puhul toimub ümardamine samamoodi nagu suvandi **Ümardus = 0,01** puhul.</span><span class="sxs-lookup"><span data-stu-id="4a318-124">For normal rounding, the rounding behavior is the same as for **Round-off = 0.01**.</span></span>
> - <span data-ttu-id="4a318-125">Suvandite **Ümardamise vormi suvandid** , **Allapoole** , **Ülespoole ümardamine** ja **Oma kasuks** puhul käitutakse samamoodi nagu suvandi **Ümardus = 1,00** puhul.</span><span class="sxs-lookup"><span data-stu-id="4a318-125">For the **Rounding form options** , **Downward** , **Rounding-up** , and **Own advantage** , the behavior is the same as for **Round-off = 1.00**.</span></span>

| <span data-ttu-id="4a318-126">Ümardamise vormi suvand</span><span class="sxs-lookup"><span data-stu-id="4a318-126">Rounding form option</span></span>                | <span data-ttu-id="4a318-127">Ümardamisväärtus = 0,01</span><span class="sxs-lookup"><span data-stu-id="4a318-127">Round-off value = 0.01</span></span> | <span data-ttu-id="4a318-128">Ümardamisväärtus = 0,10</span><span class="sxs-lookup"><span data-stu-id="4a318-128">Round-off value = 0.10</span></span> | <span data-ttu-id="4a318-129">Ümardamisväärtus = 1,00</span><span class="sxs-lookup"><span data-stu-id="4a318-129">Round-off value = 1.00</span></span> | <span data-ttu-id="4a318-130">Ümardamisväärtus = 100,00</span><span class="sxs-lookup"><span data-stu-id="4a318-130">Round-off value = 100.00</span></span> | <span data-ttu-id="4a318-131">Ümardamisväärtus = 0,00</span><span class="sxs-lookup"><span data-stu-id="4a318-131">Round-off value = 0.00</span></span>   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| <span data-ttu-id="4a318-132">Tavaline</span><span class="sxs-lookup"><span data-stu-id="4a318-132">Normal</span></span>                              | <span data-ttu-id="4a318-133">98,765.43</span><span class="sxs-lookup"><span data-stu-id="4a318-133">98,765.43</span></span>              | <span data-ttu-id="4a318-134">98,765.40</span><span class="sxs-lookup"><span data-stu-id="4a318-134">98,765.40</span></span>              | <span data-ttu-id="4a318-135">98,765.00</span><span class="sxs-lookup"><span data-stu-id="4a318-135">98,765.00</span></span>              | <span data-ttu-id="4a318-136">98,800.00</span><span class="sxs-lookup"><span data-stu-id="4a318-136">98,800.00</span></span>                | <span data-ttu-id="4a318-137">98,765.43</span><span class="sxs-lookup"><span data-stu-id="4a318-137">98,765.43</span></span>                |
| <span data-ttu-id="4a318-138">Allapoole</span><span class="sxs-lookup"><span data-stu-id="4a318-138">Downward</span></span>                            | <span data-ttu-id="4a318-139">98,765.43</span><span class="sxs-lookup"><span data-stu-id="4a318-139">98,765.43</span></span>              | <span data-ttu-id="4a318-140">98,765.40</span><span class="sxs-lookup"><span data-stu-id="4a318-140">98,765.40</span></span>              | <span data-ttu-id="4a318-141">98,765.00</span><span class="sxs-lookup"><span data-stu-id="4a318-141">98,765.00</span></span>              | <span data-ttu-id="4a318-142">98,700.00</span><span class="sxs-lookup"><span data-stu-id="4a318-142">98,700.00</span></span>                | <span data-ttu-id="4a318-143">98,765.00</span><span class="sxs-lookup"><span data-stu-id="4a318-143">98,765.00</span></span>                |
| <span data-ttu-id="4a318-144">Ümardamine</span><span class="sxs-lookup"><span data-stu-id="4a318-144">Rounding-up</span></span>                         | <span data-ttu-id="4a318-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="4a318-145">98,765.43</span></span>              | <span data-ttu-id="4a318-146">98,765.50</span><span class="sxs-lookup"><span data-stu-id="4a318-146">98,765.50</span></span>              | <span data-ttu-id="4a318-147">98,766.00</span><span class="sxs-lookup"><span data-stu-id="4a318-147">98,766.00</span></span>              | <span data-ttu-id="4a318-148">98,800.00</span><span class="sxs-lookup"><span data-stu-id="4a318-148">98,800.00</span></span>                | <span data-ttu-id="4a318-149">98,766.00</span><span class="sxs-lookup"><span data-stu-id="4a318-149">98,766.00</span></span>                |
| <span data-ttu-id="4a318-150">Oma eelis kreeditsaldo puhul</span><span class="sxs-lookup"><span data-stu-id="4a318-150">Own advantage, for a credit balance</span></span> | <span data-ttu-id="4a318-151">98,765.43</span><span class="sxs-lookup"><span data-stu-id="4a318-151">98,765.43</span></span>              | <span data-ttu-id="4a318-152">98,765.40</span><span class="sxs-lookup"><span data-stu-id="4a318-152">98,765.40</span></span>              | <span data-ttu-id="4a318-153">98,765.00</span><span class="sxs-lookup"><span data-stu-id="4a318-153">98,765.00</span></span>              | <span data-ttu-id="4a318-154">98,700.00</span><span class="sxs-lookup"><span data-stu-id="4a318-154">98,700.00</span></span>                | <span data-ttu-id="4a318-155">98,765.00</span><span class="sxs-lookup"><span data-stu-id="4a318-155">98,765.00</span></span>                |
| <span data-ttu-id="4a318-156">Oma eelis deebetsaldo puhul</span><span class="sxs-lookup"><span data-stu-id="4a318-156">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="4a318-157">98,765.43</span><span class="sxs-lookup"><span data-stu-id="4a318-157">98,765.43</span></span>              | <span data-ttu-id="4a318-158">98,765.50</span><span class="sxs-lookup"><span data-stu-id="4a318-158">98,765.50</span></span>              | <span data-ttu-id="4a318-159">98,766.00</span><span class="sxs-lookup"><span data-stu-id="4a318-159">98,766.00</span></span>              | <span data-ttu-id="4a318-160">98,800.00</span><span class="sxs-lookup"><span data-stu-id="4a318-160">98,800.00</span></span>                | <span data-ttu-id="4a318-161">98,766.00</span><span class="sxs-lookup"><span data-stu-id="4a318-161">98,766.00</span></span>                |

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="4a318-162">Tavaline ümardamine, ümardamistäpsus on 0,01</span><span class="sxs-lookup"><span data-stu-id="4a318-162">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="4a318-163">Ümardamine</span><span class="sxs-lookup"><span data-stu-id="4a318-163">Rounding</span></span>
    </td>
    <td><span data-ttu-id="4a318-164">Arvutamisprotsess</span><span class="sxs-lookup"><span data-stu-id="4a318-164">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="4a318-165">round(1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="4a318-165">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="4a318-166">round(1,015 / 0,01, 0) = round(101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="4a318-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="4a318-167">102 × 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="4a318-167">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="4a318-168">round(1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="4a318-168">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="4a318-169">round(1,014 / 0,01, 0) = round(101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="4a318-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="4a318-170">101 × 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="4a318-170">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="4a318-171">round(1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="4a318-171">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="4a318-172">round(1,011 / 0,02, 0) = round(50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="4a318-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="4a318-173">51 × 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="4a318-173">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="4a318-174">round(1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="4a318-174">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="4a318-175">round(1,009 / 0,02, 0) = round(50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="4a318-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="4a318-176">50 × 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="4a318-176">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="4a318-177">Kui valite suvandi Oma eelis, toimub ümardamine alati juriidilise isiku kasuks.</span><span class="sxs-lookup"><span data-stu-id="4a318-177">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="4a318-178">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="4a318-178">For more information, see the following topics:</span></span>
- [<span data-ttu-id="4a318-179">Käibemaksu ülevaade</span><span class="sxs-lookup"><span data-stu-id="4a318-179">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="4a318-180">Käibemaksumakse loomine</span><span class="sxs-lookup"><span data-stu-id="4a318-180">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="4a318-181">Käibemaksukannete loomine dokumentidel</span><span class="sxs-lookup"><span data-stu-id="4a318-181">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="4a318-182">Sisestatud käibemaksukannete kuvamine</span><span class="sxs-lookup"><span data-stu-id="4a318-182">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="4a318-183">Ümardamisfunktsioon</span><span class="sxs-lookup"><span data-stu-id="4a318-183">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


