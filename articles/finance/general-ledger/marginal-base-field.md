---
title: Käibemaksumäärad väljade Marginaali alus ja Arvutusmeetod põhjal
description: Selles teemas selgitatakse, kuidas väljade Marginaali alus ja Arvutamismeetod väärtused määravad müügi- ja ostukannete maksumäära(d).
author: ShylaThompson
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34e7e3f37d759953b7b4f70fe9eae78154da44d1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177300"
---
# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="70803-103">Käibemaksumäärad väljade Marginaali alus ja Arvutusmeetod põhjal</span><span class="sxs-lookup"><span data-stu-id="70803-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70803-104">Selles teemas selgitatakse, kuidas väljade Marginaali alus ja Arvutamismeetod väärtused määravad müügi- ja ostukannete maksumäära(d).</span><span class="sxs-lookup"><span data-stu-id="70803-104">This topic explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="70803-105">Lehe Käibemaksukoodid kiirkaardil Arvutus olev väli Marginaali alus määrab, millist summat kasutatakse sobiva(te) maksumäära(de) valimiseks lehel Käibemaksukoodi väärtused olevate määrade hulgast.</span><span class="sxs-lookup"><span data-stu-id="70803-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="70803-106">Väljal Marginaali alus olev summa tüüp koos meetodiga väljal Arvutusmeetod määrab kandele õige(te) maksumäära(de) leidmise loogika.</span><span class="sxs-lookup"><span data-stu-id="70803-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="70803-107">Erinevad väärtuste kombinatsioonid nendel väljadel annavad tulemuseks väga erinevad käibemaksu kalkulatsioonid, nagu näha järgmistes näidetes.</span><span class="sxs-lookup"><span data-stu-id="70803-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="70803-108">Näidetes kasutatakse samu maksu intervallväärtusi, mis on seadistatud iga maksukoodi jaoks lehel Käibemaksukoodide väärtused.</span><span class="sxs-lookup"><span data-stu-id="70803-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="70803-109">Selle lehe avamiseks klõpsake lehel Käibemaksukoodid valikuid Käibemaksukood &gt; Väärtused.</span><span class="sxs-lookup"><span data-stu-id="70803-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="70803-110">Kui Marginaali alus või mõni käibemaksukood põhineb reasummadel või ühikutel, tuleb lehel Pearaamatu parameetrid määrata välja Arvutusmeetod väärtuseks Rida.</span><span class="sxs-lookup"><span data-stu-id="70803-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="70803-111"> Netosumma rea kohta</span><span class="sxs-lookup"><span data-stu-id="70803-111">Net amount per line</span></span>
<span data-ttu-id="70803-112">Tehke see valik käibemaksumäärade arvutamiseks arve ridade netosumma alusel, välistades kõik muud maksud.</span><span class="sxs-lookup"><span data-stu-id="70803-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="70803-113">Näide</span><span class="sxs-lookup"><span data-stu-id="70803-113">Example</span></span>

<span data-ttu-id="70803-114">Käibemaksumäärad seadistatakse järgmiste intervallidega.</span><span class="sxs-lookup"><span data-stu-id="70803-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="70803-115">summa intervall</span><span class="sxs-lookup"><span data-stu-id="70803-115">Amount interval</span></span>    | <span data-ttu-id="70803-116">Maksumäär</span><span class="sxs-lookup"><span data-stu-id="70803-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="70803-117">0–50</span><span class="sxs-lookup"><span data-stu-id="70803-117">0 - 50</span></span>             | <span data-ttu-id="70803-118">30%</span><span class="sxs-lookup"><span data-stu-id="70803-118">30%</span></span>      |
| <span data-ttu-id="70803-119">50 – 100</span><span class="sxs-lookup"><span data-stu-id="70803-119">50 - 100</span></span>           | <span data-ttu-id="70803-120">20%</span><span class="sxs-lookup"><span data-stu-id="70803-120">20%</span></span>      |
| <span data-ttu-id="70803-121">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="70803-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="70803-122">10%</span><span class="sxs-lookup"><span data-stu-id="70803-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="70803-123">Viimase intervalli ülempiir null (0) tähendab, et kõik 100-st suuremad summad kaasatakse sellesse intervalli.</span><span class="sxs-lookup"><span data-stu-id="70803-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="70803-124">Marginaali alus: **Netosumma rea kohta**</span><span class="sxs-lookup"><span data-stu-id="70803-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="70803-125">Arvutamismeetod: **Intervall**</span><span class="sxs-lookup"><span data-stu-id="70803-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="70803-126">Ostate 8 lampi, mis maksavad 25.00 eurot tükk.</span><span class="sxs-lookup"><span data-stu-id="70803-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="70803-127">Arve rea netosumma on 200.00 eurot.</span><span class="sxs-lookup"><span data-stu-id="70803-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="70803-128">Käibemaks arvutatakse järgmiselt:</span><span class="sxs-lookup"><span data-stu-id="70803-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="70803-129">Käibemaksu kogusumma = 50 × 30% + 50 × 20% + 100 × 10% = 15 + 10 + 10 = 35.00.</span><span class="sxs-lookup"><span data-stu-id="70803-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="70803-130">Arve kogusumma = 200.00 + 35.00 = 235.00.</span><span class="sxs-lookup"><span data-stu-id="70803-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="70803-131">**Kõikumine**</span><span class="sxs-lookup"><span data-stu-id="70803-131">**Variation**</span></span> 

<span data-ttu-id="70803-132">Kui arvel on kaks rida, millest igal real on neli kaupa, on iga rea netosumma 100.00 ja käibemaks arvutatakse järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="70803-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="70803-133">Käibemaksu rida 1 = 50 × 30% + 50 × 20% = 15 + 10 = 25.00</span><span class="sxs-lookup"><span data-stu-id="70803-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="70803-134">Käibemaksu rida 2 = 50 × 30% + 50 × 20% = 15 + 10 = 25.00.</span><span class="sxs-lookup"><span data-stu-id="70803-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="70803-135">Käibemaks kokku = 25.00 + 25.00 = 50.00</span><span class="sxs-lookup"><span data-stu-id="70803-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="70803-136">Arve kogusumma = 200.00 + 50.00 = 250.00</span><span class="sxs-lookup"><span data-stu-id="70803-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="70803-137"> Netosumma ühiku kohta</span><span class="sxs-lookup"><span data-stu-id="70803-137">Net amount per unit</span></span>
<span data-ttu-id="70803-138">Tehke see valik käibemaksumäärade määramiseks iga ühiku väärtuse alusel, jättes muud maksud välja.</span><span class="sxs-lookup"><span data-stu-id="70803-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="70803-139">Kui on valitud ühikupõhine marginaali alus, tuleb käibemaksukoodile määrata ka ühik.</span><span class="sxs-lookup"><span data-stu-id="70803-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="70803-140">Näide</span><span class="sxs-lookup"><span data-stu-id="70803-140">Example</span></span>

<span data-ttu-id="70803-141">Käibemaksumäärad seadistatakse järgmiste intervallidega.</span><span class="sxs-lookup"><span data-stu-id="70803-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="70803-142">Summa</span><span class="sxs-lookup"><span data-stu-id="70803-142">Amount</span></span>             | <span data-ttu-id="70803-143">Maksumäär</span><span class="sxs-lookup"><span data-stu-id="70803-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="70803-144">0–50</span><span class="sxs-lookup"><span data-stu-id="70803-144">0 - 50</span></span>             | <span data-ttu-id="70803-145">30%</span><span class="sxs-lookup"><span data-stu-id="70803-145">30%</span></span>      |
| <span data-ttu-id="70803-146">50 – 100</span><span class="sxs-lookup"><span data-stu-id="70803-146">50 - 100</span></span>           | <span data-ttu-id="70803-147">20%</span><span class="sxs-lookup"><span data-stu-id="70803-147">20%</span></span>      |
| <span data-ttu-id="70803-148">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="70803-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="70803-149">10%</span><span class="sxs-lookup"><span data-stu-id="70803-149">10%</span></span>      |

<span data-ttu-id="70803-150">Marginaali alus: **Netosumma ühiku kohta**</span><span class="sxs-lookup"><span data-stu-id="70803-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="70803-151">Arvutamismeetod = **terve summa**</span><span class="sxs-lookup"><span data-stu-id="70803-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="70803-152">Ostate 8 lampi, mis maksavad 25.00 eurot tükk.</span><span class="sxs-lookup"><span data-stu-id="70803-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="70803-153">Arve rea netosumma on 200.00 eurot.</span><span class="sxs-lookup"><span data-stu-id="70803-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="70803-154">Käibemaks arvutatakse järgmiselt: käibemaks ühiku kohta = 25.00 x 30% = 7.50 Käibemaks kokku = 7.50 x 8 ühikut = 60.00 Arve koondsumma = 200.00 + 60.00 = 260.00</span><span class="sxs-lookup"><span data-stu-id="70803-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="70803-155"> Arve saldo netosumma</span><span class="sxs-lookup"><span data-stu-id="70803-155">Net amount of invoice balance</span></span>

<span data-ttu-id="70803-156">Tehke see valik käibemaksumäärade arvutamiseks arve koondväärtuse alusel, välistades kõik muud maksud.</span><span class="sxs-lookup"><span data-stu-id="70803-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="70803-157">Näide</span><span class="sxs-lookup"><span data-stu-id="70803-157">Example</span></span>

<span data-ttu-id="70803-158">Käibemaksumäärad seadistatakse järgmiste intervallidega.</span><span class="sxs-lookup"><span data-stu-id="70803-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="70803-159">Summa</span><span class="sxs-lookup"><span data-stu-id="70803-159">Amount</span></span>            | <span data-ttu-id="70803-160">Maksumäär</span><span class="sxs-lookup"><span data-stu-id="70803-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="70803-161">0–50</span><span class="sxs-lookup"><span data-stu-id="70803-161">0 - 50</span></span>            | <span data-ttu-id="70803-162">30%</span><span class="sxs-lookup"><span data-stu-id="70803-162">30%</span></span>      |
| <span data-ttu-id="70803-163">50 – 100</span><span class="sxs-lookup"><span data-stu-id="70803-163">50 - 100</span></span>          | <span data-ttu-id="70803-164">20%</span><span class="sxs-lookup"><span data-stu-id="70803-164">20%</span></span>      |
| <span data-ttu-id="70803-165">100 -0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="70803-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="70803-166">10%</span><span class="sxs-lookup"><span data-stu-id="70803-166">10%</span></span>      |

<span data-ttu-id="70803-167">Marginaali alus: **arve saldo netosumma**</span><span class="sxs-lookup"><span data-stu-id="70803-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="70803-168">Arvutamismeetod: **intervall** Müügiarvel on 2 rida, millest igal real on 4 lampi hinnaga 25.00.</span><span class="sxs-lookup"><span data-stu-id="70803-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="70803-169">Arve saldo netosumma on 4 x 25.00 + 4 x 25.00 = 200.00.</span><span class="sxs-lookup"><span data-stu-id="70803-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="70803-170">Käibemaks arvutatakse järgmiselt: käibemaksu koondsumma = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Arve koondsumma = 200.00 + 35.00 = 235.00</span><span class="sxs-lookup"><span data-stu-id="70803-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="70803-171"> Brutosumma rea kohta</span><span class="sxs-lookup"><span data-stu-id="70803-171">Gross amount per line</span></span>

<span data-ttu-id="70803-172">Tehke see valik käibemaksumäärade arvutamiseks arve rea väärtuse alusel, kaasates kõik muud selle rea maksud.</span><span class="sxs-lookup"><span data-stu-id="70803-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="70803-173">Käibemaksugrupis saab teil selle valiku puhul olla ainult üks käibemaksukood väljal Marginaali alus.</span><span class="sxs-lookup"><span data-stu-id="70803-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="70803-174">Näide</span><span class="sxs-lookup"><span data-stu-id="70803-174">Example</span></span>

<span data-ttu-id="70803-175">Käibemaksumäärad seadistatakse järgmiste intervallidega.</span><span class="sxs-lookup"><span data-stu-id="70803-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="70803-176">Summa</span><span class="sxs-lookup"><span data-stu-id="70803-176">Amount</span></span>             | <span data-ttu-id="70803-177">Maksumäär</span><span class="sxs-lookup"><span data-stu-id="70803-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="70803-178">0–50</span><span class="sxs-lookup"><span data-stu-id="70803-178">0 - 50</span></span>             | <span data-ttu-id="70803-179">30%</span><span class="sxs-lookup"><span data-stu-id="70803-179">30%</span></span>      |
| <span data-ttu-id="70803-180">50 – 100</span><span class="sxs-lookup"><span data-stu-id="70803-180">50 - 100</span></span>           | <span data-ttu-id="70803-181">20%</span><span class="sxs-lookup"><span data-stu-id="70803-181">20%</span></span>      |
| <span data-ttu-id="70803-182">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="70803-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="70803-183">10%</span><span class="sxs-lookup"><span data-stu-id="70803-183">10%</span></span>      |

<span data-ttu-id="70803-184">Marginaali alus: **brutosumma rea kohta** Arvutusmeetod: **intervall** Lisaks on veel üks maksukood, millega arvutatakse erilõiv 5.00 iga lambi kohta.</span><span class="sxs-lookup"><span data-stu-id="70803-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is another tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="70803-185">Lõiv lisatakse netosummale enne käibemaksu arvutamist.</span><span class="sxs-lookup"><span data-stu-id="70803-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="70803-186">Ostate 8 lampi, mis maksavad 25.00 eurot tükk.</span><span class="sxs-lookup"><span data-stu-id="70803-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="70803-187">Arve rea netosumma on 200.00 eurot.</span><span class="sxs-lookup"><span data-stu-id="70803-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="70803-188">Arverea brutosumma on 8 x 25.00 + 8 x 5.00 = 240.00 eurot.</span><span class="sxs-lookup"><span data-stu-id="70803-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="70803-189">Käibemaks arvutatakse järgmiselt: käibemaksu koondsumma = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Lõiv kokku = 5.00 x 8 = 40.00 Arve summa kokku = 200.00 + 39.00 + 40.00 = 279.00</span><span class="sxs-lookup"><span data-stu-id="70803-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="70803-190">**Kõikumine**</span><span class="sxs-lookup"><span data-stu-id="70803-190">**Variation**</span></span> 

<span data-ttu-id="70803-191">Kui arve koostatakse 2 arvereaga, millest igal real on 4 kaupa, on netosumma arve rea kohta 100.00.</span><span class="sxs-lookup"><span data-stu-id="70803-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="70803-192">Brutosumma (sh lõiv 4 x 5.00) arve rea kohta oleks 120.00 ja käibemaks luuakse järgmiselt 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Käibemaksuarve rida 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Käibemaks kokku = 27.00 + 27.00 = 54.00 Lõiv kokku = 5.00 x 8 = 40.00 Arve summa kokku = 200.00 + 54.00 + 40.00 = 294.00</span><span class="sxs-lookup"><span data-stu-id="70803-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="70803-193"> Brutosumma ühiku kohta</span><span class="sxs-lookup"><span data-stu-id="70803-193">Gross amount per unit</span></span>

<span data-ttu-id="70803-194">Tehke see valik käibemaksumäärade määramiseks iga ühiku väärtuse alusel, kaasates kõik muud maksud.</span><span class="sxs-lookup"><span data-stu-id="70803-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="70803-195">Käibemaksugrupis saab teil selle valiku puhul olla ainult üks käibemaksukood väljal Marginaali alus.</span><span class="sxs-lookup"><span data-stu-id="70803-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="70803-196">Näide</span><span class="sxs-lookup"><span data-stu-id="70803-196">Example</span></span>

<span data-ttu-id="70803-197">Käibemaksumäärad seadistatakse järgmiste intervallidega.</span><span class="sxs-lookup"><span data-stu-id="70803-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="70803-198">Summa</span><span class="sxs-lookup"><span data-stu-id="70803-198">Amount</span></span>             | <span data-ttu-id="70803-199">Maksumäär</span><span class="sxs-lookup"><span data-stu-id="70803-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="70803-200">0–50</span><span class="sxs-lookup"><span data-stu-id="70803-200">0 - 50</span></span>             | <span data-ttu-id="70803-201">30%</span><span class="sxs-lookup"><span data-stu-id="70803-201">30%</span></span>      |
| <span data-ttu-id="70803-202">50 – 100</span><span class="sxs-lookup"><span data-stu-id="70803-202">50 - 100</span></span>           | <span data-ttu-id="70803-203">20%</span><span class="sxs-lookup"><span data-stu-id="70803-203">20%</span></span>      |
| <span data-ttu-id="70803-204">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="70803-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="70803-205">10%</span><span class="sxs-lookup"><span data-stu-id="70803-205">10%</span></span>      |

<span data-ttu-id="70803-206">Marginaali alus: **ühiku brutosumma** Iga lambi kohta kehtib erilõiv 5.00.</span><span class="sxs-lookup"><span data-stu-id="70803-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="70803-207">Lõiv lisatakse netosummale enne käibemaksu arvutamist.</span><span class="sxs-lookup"><span data-stu-id="70803-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="70803-208">Ostate 8 lampi, mis maksavad 25.00 eurot tükk.</span><span class="sxs-lookup"><span data-stu-id="70803-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="70803-209">Ühiku brutosumma on 30.00.</span><span class="sxs-lookup"><span data-stu-id="70803-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="70803-210">Maks arvutatakse järgmiselt: käibemaks ühiku kohta = 30 x 30% = 9.00 Käibemaks kokku = 9.00 x 8 = 72.00 Lõiv kokku = 5.00 x 8 = 40.00 Arve koondsumma = 200.00 + 72.00 + 40.00 = 312.00</span><span class="sxs-lookup"><span data-stu-id="70803-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="70803-211"> Arve kokku, sh muud käibemaksusummad</span><span class="sxs-lookup"><span data-stu-id="70803-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="70803-212">Tehke see valik käibemaksumäärade arvutamiseks arve koondväärtuse alusel, kaasates kõik muud maksud.</span><span class="sxs-lookup"><span data-stu-id="70803-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="70803-213">Käibemaksugrupis saab teil selle valiku puhul olla ainult üks käibemaksukood väljal Marginaali alus</span><span class="sxs-lookup"><span data-stu-id="70803-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="70803-214">Näide</span><span class="sxs-lookup"><span data-stu-id="70803-214">Example</span></span>

<span data-ttu-id="70803-215">Käibemaksumäärad seadistatakse järgmiste intervallidega.</span><span class="sxs-lookup"><span data-stu-id="70803-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="70803-216">Summa</span><span class="sxs-lookup"><span data-stu-id="70803-216">Amount</span></span>             | <span data-ttu-id="70803-217">Maksumäär</span><span class="sxs-lookup"><span data-stu-id="70803-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="70803-218">0–50</span><span class="sxs-lookup"><span data-stu-id="70803-218">0 - 50</span></span>             | <span data-ttu-id="70803-219">30%</span><span class="sxs-lookup"><span data-stu-id="70803-219">30%</span></span>      |
| <span data-ttu-id="70803-220">50 – 100</span><span class="sxs-lookup"><span data-stu-id="70803-220">50 - 100</span></span>           | <span data-ttu-id="70803-221">20%</span><span class="sxs-lookup"><span data-stu-id="70803-221">20%</span></span>      |
| <span data-ttu-id="70803-222">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="70803-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="70803-223">10%</span><span class="sxs-lookup"><span data-stu-id="70803-223">10%</span></span>      |

<span data-ttu-id="70803-224">Marginaali alus: **arve koondsumma, sh muud käibemaksusummad** Arvutusmeetod: **intervall** </span><span class="sxs-lookup"><span data-stu-id="70803-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="70803-225">Iga lambi kohta kehtib erilõiv 5.00.</span><span class="sxs-lookup"><span data-stu-id="70803-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="70803-226">Lõiv lisatakse netosummale enne käibemaksu arvutamist.</span><span class="sxs-lookup"><span data-stu-id="70803-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="70803-227">Ostate 8 lampi, mis maksavad 25.00 eurot tükk.</span><span class="sxs-lookup"><span data-stu-id="70803-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="70803-228">Arve netosumma on 200.00 eurot.</span><span class="sxs-lookup"><span data-stu-id="70803-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="70803-229">Arve brutosumma on 200.00 + (8 x 5.00) = 240.00.</span><span class="sxs-lookup"><span data-stu-id="70803-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="70803-230">Käibemaks arvutatakse järgmiselt: käibemaksu koondsumma = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Lõiv kokku = 5.00 x 8 = 40.00 Arve summa kokku = 200.00 + 39.00 + 40.00 = 279.00</span><span class="sxs-lookup"><span data-stu-id="70803-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="70803-231">Lisateavet leiate jaotisest [Kogusumma ja intervalli arvutamise valikud käibemaksukoodide puhul](whole-amount-interval-options-sales-tax-codes.md) [Käibemaksu arvutusmeetodid väljal Päritolu](sales-tax-calculation-methods-origin-field.md).</span><span class="sxs-lookup"><span data-stu-id="70803-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>


