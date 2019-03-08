---
title: Käibemaksu maksed ja ümardamisreeglid
description: See artikkel selgitab, kuidas toimib ümardamisreegli seadistus moodulis Käibemaksuhaldurid ja kuidas ümardada käibemaksusaldot töö Käibemaksu tasakaalustamine ja sisestamine käigus.
author: ShylaThompson
manager: AnnBe
ms.date: 08/01/2017
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
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f03336c834e74cd12d039c7b9692874843811746
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "367842"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="b8ede-103">Käibemaksu maksed ja ümardamisreeglid</span><span class="sxs-lookup"><span data-stu-id="b8ede-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8ede-104">See artikkel selgitab, kuidas toimib ümardamisreegli seadistus moodulis Käibemaksuhaldurid ja kuidas ümardada käibemaksusaldot töö Käibemaksu tasakaalustamine ja sisestamine käigus.</span><span class="sxs-lookup"><span data-stu-id="b8ede-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="b8ede-105">Käibemaksu kohta tuleb perioodiliselt maksuametile aruandeid esitada ja see tasuda.</span><span class="sxs-lookup"><span data-stu-id="b8ede-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="b8ede-106">Seda saab teha, käivitades tasakaalustamise ja sisestades käibemaksuprotsessi lehel Käibemaks.</span><span class="sxs-lookup"><span data-stu-id="b8ede-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="b8ede-107">Perioodi käibemaks tasakaalustatakse käibemaksukontodega ja käibemaksusaldo sisestatakse käibemaksu tasakaalustuskontole.</span><span class="sxs-lookup"><span data-stu-id="b8ede-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="b8ede-108">Käibemaksusaldo, mis sisestatakse käibemaksu tasakaalustuskontole, saab maksuameti nõude järgi ümardada, seadistades lehel Käibemaks ümardamisreegli.</span><span class="sxs-lookup"><span data-stu-id="b8ede-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="b8ede-109">Ümardamise erinevus sisestatakse käibemaksu ümardamise kontole, mis on valitud pearaamatus väljal Automaatsete kannete kontod.</span><span class="sxs-lookup"><span data-stu-id="b8ede-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="b8ede-110">Allolev näide selgitab lehel Käibemaksuhaldur ümardamisreegli toimimise põhimõtet.</span><span class="sxs-lookup"><span data-stu-id="b8ede-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

### <a name="example"></a><span data-ttu-id="b8ede-111">Näide:</span><span class="sxs-lookup"><span data-stu-id="b8ede-111">Example:</span></span>

<span data-ttu-id="b8ede-112">Perioodi kogu käibemaksu krediidisaldo on –98 765,43.</span><span class="sxs-lookup"><span data-stu-id="b8ede-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="b8ede-113">Juriidiline isik kogus rohkem käibemaksu kui ise tasus.</span><span class="sxs-lookup"><span data-stu-id="b8ede-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="b8ede-114">Seetõttu võlgneb juriidiline isik maksuametile raha.</span><span class="sxs-lookup"><span data-stu-id="b8ede-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="b8ede-115">Juriidiline isik soovib kasutada ümardamismeetodit, mis ümardab saldo lähima täisarvuni (1,00).</span><span class="sxs-lookup"><span data-stu-id="b8ede-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="b8ede-116">Käibemaksu arvestamise eest vastutav kasutaja peab tegema järgmist.</span><span class="sxs-lookup"><span data-stu-id="b8ede-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="b8ede-117">Klõpsake valikuid Maks &gt; Kaudsed maksud &gt; Käibemaks &gt; Käibemaksuhaldurid</span><span class="sxs-lookup"><span data-stu-id="b8ede-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="b8ede-118">Valige kiirkaardi Üldine väljalt Ümardamise vorm suvand Tavaline.</span><span class="sxs-lookup"><span data-stu-id="b8ede-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="b8ede-119">Sisestage väljale Ümardus väärtus 1,00.</span><span class="sxs-lookup"><span data-stu-id="b8ede-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="b8ede-120">Kui saabub aeg tasuda maksuametile käibemaks, avage leht Käibemaksu tasakaalustamine ja sisestamine.</span><span class="sxs-lookup"><span data-stu-id="b8ede-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="b8ede-121">(Klõpsake valikuid Maks &gt; Deklaratsioonid &gt; Käibemaks &gt; Käibemaksu tasakaalustamine ja sisestamine.)</span><span class="sxs-lookup"><span data-stu-id="b8ede-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="b8ede-122">Käibemaksu tasakaalustamise kontol ümardatakse maksukohustuse summa 98 765,43 summale 98 765.</span><span class="sxs-lookup"><span data-stu-id="b8ede-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="b8ede-123">Järgmine tabel näitab, kuidas ümardatakse summat 98 765,43, kasutades iga ümardusmeetodit, mis on saadaval lehe Käibemaksuhaldurid väljal Ümardamise vorm.</span><span class="sxs-lookup"><span data-stu-id="b8ede-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="b8ede-124">Ümardamise vormi suvand</span><span class="sxs-lookup"><span data-stu-id="b8ede-124">Rounding form option</span></span>                | <span data-ttu-id="b8ede-125">Ümardamisväärtus = 0,01</span><span class="sxs-lookup"><span data-stu-id="b8ede-125">Round-off value = 0.01</span></span> | <span data-ttu-id="b8ede-126">Ümardamisväärtus = 0,10</span><span class="sxs-lookup"><span data-stu-id="b8ede-126">Round-off value = 0.10</span></span> | <span data-ttu-id="b8ede-127">Ümardamisväärtus = 1,00</span><span class="sxs-lookup"><span data-stu-id="b8ede-127">Round-off value = 1.00</span></span> | <span data-ttu-id="b8ede-128">Ümardamisväärtus = 100,00</span><span class="sxs-lookup"><span data-stu-id="b8ede-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="b8ede-129">Tavaline</span><span class="sxs-lookup"><span data-stu-id="b8ede-129">Normal</span></span>                              | <span data-ttu-id="b8ede-130">98,765.43</span><span class="sxs-lookup"><span data-stu-id="b8ede-130">98,765.43</span></span>              | <span data-ttu-id="b8ede-131">98,765.40</span><span class="sxs-lookup"><span data-stu-id="b8ede-131">98,765.40</span></span>              | <span data-ttu-id="b8ede-132">98,765.00</span><span class="sxs-lookup"><span data-stu-id="b8ede-132">98,765.00</span></span>              | <span data-ttu-id="b8ede-133">98,800.00</span><span class="sxs-lookup"><span data-stu-id="b8ede-133">98,800.00</span></span>                |
| <span data-ttu-id="b8ede-134">Allapoole</span><span class="sxs-lookup"><span data-stu-id="b8ede-134">Downward</span></span>                            | <span data-ttu-id="b8ede-135">98,765.43</span><span class="sxs-lookup"><span data-stu-id="b8ede-135">98,765.43</span></span>              | <span data-ttu-id="b8ede-136">98,765.40</span><span class="sxs-lookup"><span data-stu-id="b8ede-136">98,765.40</span></span>              | <span data-ttu-id="b8ede-137">98,765.00</span><span class="sxs-lookup"><span data-stu-id="b8ede-137">98,765.00</span></span>              | <span data-ttu-id="b8ede-138">98,700.00</span><span class="sxs-lookup"><span data-stu-id="b8ede-138">98,700.00</span></span>                |
| <span data-ttu-id="b8ede-139">Ümardamine</span><span class="sxs-lookup"><span data-stu-id="b8ede-139">Rounding-up</span></span>                         | <span data-ttu-id="b8ede-140">98,765.43</span><span class="sxs-lookup"><span data-stu-id="b8ede-140">98,765.43</span></span>              | <span data-ttu-id="b8ede-141">98,765.50</span><span class="sxs-lookup"><span data-stu-id="b8ede-141">98,765.50</span></span>              | <span data-ttu-id="b8ede-142">98,766.00</span><span class="sxs-lookup"><span data-stu-id="b8ede-142">98,766.00</span></span>              | <span data-ttu-id="b8ede-143">98,800.00</span><span class="sxs-lookup"><span data-stu-id="b8ede-143">98,800.00</span></span>                |
| <span data-ttu-id="b8ede-144">Oma eelis kreeditsaldo puhul</span><span class="sxs-lookup"><span data-stu-id="b8ede-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="b8ede-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="b8ede-145">98,765.43</span></span>              | <span data-ttu-id="b8ede-146">98,765.40</span><span class="sxs-lookup"><span data-stu-id="b8ede-146">98,765.40</span></span>              | <span data-ttu-id="b8ede-147">98,765.00</span><span class="sxs-lookup"><span data-stu-id="b8ede-147">98,765.00</span></span>              | <span data-ttu-id="b8ede-148">98,700.00</span><span class="sxs-lookup"><span data-stu-id="b8ede-148">98,700.00</span></span>                |
| <span data-ttu-id="b8ede-149">Oma eelis deebetsaldo puhul</span><span class="sxs-lookup"><span data-stu-id="b8ede-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="b8ede-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="b8ede-150">98,765.43</span></span>              | <span data-ttu-id="b8ede-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="b8ede-151">98,765.50</span></span>              | <span data-ttu-id="b8ede-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="b8ede-152">98,766.00</span></span>              | <span data-ttu-id="b8ede-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="b8ede-153">98,800.00</span></span>                |

> [!NOTE]                                                                                  
> <span data-ttu-id="b8ede-154">Kui valite suvandi Oma eelis, toimub ümardamine alati juriidilise isiku kasuks.</span><span class="sxs-lookup"><span data-stu-id="b8ede-154">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="b8ede-155">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="b8ede-155">For more information, see the following topics:</span></span>
- [<span data-ttu-id="b8ede-156">Käibemaksu ülevaade</span><span class="sxs-lookup"><span data-stu-id="b8ede-156">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="b8ede-157">Käibemaksumakse loomine</span><span class="sxs-lookup"><span data-stu-id="b8ede-157">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="b8ede-158">Müügikannete loomine dokumentidel</span><span class="sxs-lookup"><span data-stu-id="b8ede-158">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="b8ede-159">Sisestatud käibemaksukannete kuvamine</span><span class="sxs-lookup"><span data-stu-id="b8ede-159">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)


