---
title: Kogusumma ja intervalli arvutamise valikud käibemaksukoodide puhul
description: See artikkel selgitab käibemaksukoodide välja Arvutusmeetod ja seda, kuidas käibemaksu vahemike ja terviksummade puhul arvutatakse.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cc998ddc2f654afba778c8c3af85dce37d3c3427
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570167"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="02d67-103">Kogusumma ja intervalli arvutamise valikud käibemaksukoodide puhul</span><span class="sxs-lookup"><span data-stu-id="02d67-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02d67-104">See artikkel selgitab käibemaksukoodide välja Arvutusmeetod ja seda, kuidas käibemaksu vahemike ja terviksummade puhul arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="02d67-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="02d67-105">Saate seadistada käibemaksukoodi arvutamise kogusumma või intervallisumma põhjal.</span><span class="sxs-lookup"><span data-stu-id="02d67-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="02d67-106">Valige käibemaksukoodi arvutamise viis lehe Käibemaksukoodid kiirkaardi Arvutamine väljal Arvutusmeetod.</span><span class="sxs-lookup"><span data-stu-id="02d67-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="02d67-107">Kogusumma – maksumäära rakendatakse kogu maksustatavale summale.</span><span class="sxs-lookup"><span data-stu-id="02d67-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="02d67-108">Intervall – maksustatav summa on jagatud osadeks, millest igaüks langeb kindla käibemaksumäärata vahemikku.</span><span class="sxs-lookup"><span data-stu-id="02d67-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="02d67-109">Osa summast, mis langeb antud intervalli, maksustatakse selle intervalli maksumäära järgi.</span><span class="sxs-lookup"><span data-stu-id="02d67-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="02d67-110">Käibemaks on iga summa intervalli kohta arvutatud maksusummade summa.</span><span class="sxs-lookup"><span data-stu-id="02d67-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="02d67-111">Suvand Intervall on saadaval ainult siis, kui valite lehel Pearaamatu parameetrid alal Käibemaks väljal Arvutusmeetod suvandi Rida.</span><span class="sxs-lookup"><span data-stu-id="02d67-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="02d67-112">Intervallid seadistatakse lehel Käibemaksukood, sisestades iga maksumäära kohta alampiiri ja ülempiiri summad.</span><span class="sxs-lookup"><span data-stu-id="02d67-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="02d67-113">Selleks et maksud arvutataks kõigi maksustatavate summade kohta olenemata valitud arvutusmeetodist, peavad intervallid järgima järgmisi reegleid.</span><span class="sxs-lookup"><span data-stu-id="02d67-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="02d67-114">Esimese intervalli alamlimiit peab olema null.</span><span class="sxs-lookup"><span data-stu-id="02d67-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="02d67-115">Viimase intervalli ülempiir peab olema null, mis tähistab lõpmatust.</span><span class="sxs-lookup"><span data-stu-id="02d67-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="02d67-116">Intervalli ülempiir peab olema järgmise intervalli alampiir.</span><span class="sxs-lookup"><span data-stu-id="02d67-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="02d67-117">Kui summa on eelmise intervalli ülempiir ja järgmise intervalli alampiir, rakendub summale esimese intervalli käibemaksumäär.</span><span class="sxs-lookup"><span data-stu-id="02d67-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="02d67-118">Kui summa jääb väljapoole intervalle, mis on määratletud ülem- ja alampiiriga, rakendatakse käibemaksumäära null.</span><span class="sxs-lookup"><span data-stu-id="02d67-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="02d67-119">Näide. Arvutamismeetod: kogusumma</span><span class="sxs-lookup"><span data-stu-id="02d67-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="02d67-120">Lehel Käibemaksukoodid seadistatakse käibemaksumäärad järgmiste intervallidega.</span><span class="sxs-lookup"><span data-stu-id="02d67-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="02d67-121">**Alampiir**</span><span class="sxs-lookup"><span data-stu-id="02d67-121">**Minimum limit**</span></span> | <span data-ttu-id="02d67-122">**Ülempiir**</span><span class="sxs-lookup"><span data-stu-id="02d67-122">**Maximum limit**</span></span> | <span data-ttu-id="02d67-123">**Maksumäär**</span><span class="sxs-lookup"><span data-stu-id="02d67-123">**Tax rate**</span></span> |
| <span data-ttu-id="02d67-124">0,00</span><span class="sxs-lookup"><span data-stu-id="02d67-124">0.00</span></span>              | <span data-ttu-id="02d67-125">50,00</span><span class="sxs-lookup"><span data-stu-id="02d67-125">50.00</span></span>             | <span data-ttu-id="02d67-126">30%</span><span class="sxs-lookup"><span data-stu-id="02d67-126">30%</span></span>          |
| <span data-ttu-id="02d67-127">50,00</span><span class="sxs-lookup"><span data-stu-id="02d67-127">50.00</span></span>             | <span data-ttu-id="02d67-128">100,00</span><span class="sxs-lookup"><span data-stu-id="02d67-128">100.00</span></span>            | <span data-ttu-id="02d67-129">20%</span><span class="sxs-lookup"><span data-stu-id="02d67-129">20%</span></span>          |
| <span data-ttu-id="02d67-130">100,00</span><span class="sxs-lookup"><span data-stu-id="02d67-130">100.00</span></span>            | <span data-ttu-id="02d67-131">0,00</span><span class="sxs-lookup"><span data-stu-id="02d67-131">0.00</span></span>              | <span data-ttu-id="02d67-132">10%</span><span class="sxs-lookup"><span data-stu-id="02d67-132">10%</span></span>          |

<span data-ttu-id="02d67-133">Käibemaks arvutatakse kogu maksustatava summa kohta.</span><span class="sxs-lookup"><span data-stu-id="02d67-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="02d67-134">Maksustatav summa (hind)</span><span class="sxs-lookup"><span data-stu-id="02d67-134">Taxable amount (price)</span></span> | <span data-ttu-id="02d67-135">Kalkulatsioon</span><span class="sxs-lookup"><span data-stu-id="02d67-135">Calculation</span></span>    | <span data-ttu-id="02d67-136">Käibemaks</span><span class="sxs-lookup"><span data-stu-id="02d67-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="02d67-137">35,00</span><span class="sxs-lookup"><span data-stu-id="02d67-137">35.00</span></span>                  | <span data-ttu-id="02d67-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="02d67-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="02d67-139">10,50</span><span class="sxs-lookup"><span data-stu-id="02d67-139">10.50</span></span>     |
| <span data-ttu-id="02d67-140">50,00</span><span class="sxs-lookup"><span data-stu-id="02d67-140">50.00</span></span>                  | <span data-ttu-id="02d67-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="02d67-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="02d67-142">15,00</span><span class="sxs-lookup"><span data-stu-id="02d67-142">15.00</span></span>     |
| <span data-ttu-id="02d67-143">85,00</span><span class="sxs-lookup"><span data-stu-id="02d67-143">85.00</span></span>                  | <span data-ttu-id="02d67-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="02d67-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="02d67-145">17,00</span><span class="sxs-lookup"><span data-stu-id="02d67-145">17.00</span></span>     |
| <span data-ttu-id="02d67-146">305,00</span><span class="sxs-lookup"><span data-stu-id="02d67-146">305.00</span></span>                 | <span data-ttu-id="02d67-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="02d67-147">305.00 \* 0.10</span></span> | <span data-ttu-id="02d67-148">30,50</span><span class="sxs-lookup"><span data-stu-id="02d67-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="02d67-149"> Näide. Arvutusmeetod: intervall</span><span class="sxs-lookup"><span data-stu-id="02d67-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="02d67-150">Lehel Väärtused seadistatakse käibemaksumäärad järgmiste intervallidega.</span><span class="sxs-lookup"><span data-stu-id="02d67-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="02d67-151">**Alampiir**</span><span class="sxs-lookup"><span data-stu-id="02d67-151">**Minimum limit**</span></span> | <span data-ttu-id="02d67-152">**Ülempiir**</span><span class="sxs-lookup"><span data-stu-id="02d67-152">**Maximum limit**</span></span> | <span data-ttu-id="02d67-153">**Maksumäär**</span><span class="sxs-lookup"><span data-stu-id="02d67-153">**Tax rate**</span></span> |
| <span data-ttu-id="02d67-154">0,00</span><span class="sxs-lookup"><span data-stu-id="02d67-154">0.00</span></span>              | <span data-ttu-id="02d67-155">50,00</span><span class="sxs-lookup"><span data-stu-id="02d67-155">50.00</span></span>             | <span data-ttu-id="02d67-156">30%</span><span class="sxs-lookup"><span data-stu-id="02d67-156">30%</span></span>          |
| <span data-ttu-id="02d67-157">50,00</span><span class="sxs-lookup"><span data-stu-id="02d67-157">50.00</span></span>             | <span data-ttu-id="02d67-158">100,00</span><span class="sxs-lookup"><span data-stu-id="02d67-158">100.00</span></span>            | <span data-ttu-id="02d67-159">20%</span><span class="sxs-lookup"><span data-stu-id="02d67-159">20%</span></span>          |
| <span data-ttu-id="02d67-160">100,00</span><span class="sxs-lookup"><span data-stu-id="02d67-160">100.00</span></span>            | <span data-ttu-id="02d67-161">0,00</span><span class="sxs-lookup"><span data-stu-id="02d67-161">0.00</span></span>              | <span data-ttu-id="02d67-162">10%</span><span class="sxs-lookup"><span data-stu-id="02d67-162">10%</span></span>          |

<span data-ttu-id="02d67-163">Käibemaks on iga summa intervalli kohta arvutatud maksusummade summa.</span><span class="sxs-lookup"><span data-stu-id="02d67-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="02d67-164">Maksustatav summa (hind)</span><span class="sxs-lookup"><span data-stu-id="02d67-164">Taxable amount (price)</span></span> | <span data-ttu-id="02d67-165">Kalkulatsioon</span><span class="sxs-lookup"><span data-stu-id="02d67-165">Calculation</span></span>                                                               | <span data-ttu-id="02d67-166">Käibemaks</span><span class="sxs-lookup"><span data-stu-id="02d67-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="02d67-167">35,00</span><span class="sxs-lookup"><span data-stu-id="02d67-167">35.00</span></span>                  | <span data-ttu-id="02d67-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="02d67-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="02d67-169">10,50</span><span class="sxs-lookup"><span data-stu-id="02d67-169">10.50</span></span>     |
| <span data-ttu-id="02d67-170">50,00</span><span class="sxs-lookup"><span data-stu-id="02d67-170">50.00</span></span>                  | <span data-ttu-id="02d67-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="02d67-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="02d67-172">15,00</span><span class="sxs-lookup"><span data-stu-id="02d67-172">15.00</span></span>     |
| <span data-ttu-id="02d67-173">85,00</span><span class="sxs-lookup"><span data-stu-id="02d67-173">85.00</span></span>                  | <span data-ttu-id="02d67-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="02d67-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="02d67-175">22,00</span><span class="sxs-lookup"><span data-stu-id="02d67-175">22.00</span></span>     |
| <span data-ttu-id="02d67-176">305,00</span><span class="sxs-lookup"><span data-stu-id="02d67-176">305.00</span></span>                 | <span data-ttu-id="02d67-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="02d67-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="02d67-178">45,50</span><span class="sxs-lookup"><span data-stu-id="02d67-178">45.50</span></span>     |



<span data-ttu-id="02d67-179">Lisateabe saamiseks vaadake teemat [Käibemaksumäärade määramine väljade Marginaali alus ja Arvutusmeetod põhjal](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="02d67-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>





