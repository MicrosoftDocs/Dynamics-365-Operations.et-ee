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
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d16ea19a6d3cfea325281f301e0502bb051381d9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "344060"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="251c9-103">Kogusumma ja intervalli arvutamise valikud käibemaksukoodide puhul</span><span class="sxs-lookup"><span data-stu-id="251c9-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="251c9-104">See artikkel selgitab käibemaksukoodide välja Arvutusmeetod ja seda, kuidas käibemaksu vahemike ja terviksummade puhul arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="251c9-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="251c9-105">Saate seadistada käibemaksukoodi arvutamise kogusumma või intervallisumma põhjal.</span><span class="sxs-lookup"><span data-stu-id="251c9-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="251c9-106">Valige käibemaksukoodi arvutamise viis lehe Käibemaksukoodid kiirkaardi Arvutamine väljal Arvutusmeetod.</span><span class="sxs-lookup"><span data-stu-id="251c9-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="251c9-107">Kogusumma – maksumäära rakendatakse kogu maksustatavale summale.</span><span class="sxs-lookup"><span data-stu-id="251c9-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="251c9-108">Intervall – maksustatav summa on jagatud osadeks, millest igaüks langeb kindla käibemaksumäärata vahemikku.</span><span class="sxs-lookup"><span data-stu-id="251c9-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="251c9-109">Osa summast, mis langeb antud intervalli, maksustatakse selle intervalli maksumäära järgi.</span><span class="sxs-lookup"><span data-stu-id="251c9-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="251c9-110">Käibemaks on iga summa intervalli kohta arvutatud maksusummade summa.</span><span class="sxs-lookup"><span data-stu-id="251c9-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="251c9-111">Suvand Intervall on saadaval ainult siis, kui valite lehel Pearaamatu parameetrid alal Käibemaks väljal Arvutusmeetod suvandi Rida.</span><span class="sxs-lookup"><span data-stu-id="251c9-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="251c9-112">Intervallid seadistatakse lehel Käibemaksukood, sisestades iga maksumäära kohta alampiiri ja ülempiiri summad.</span><span class="sxs-lookup"><span data-stu-id="251c9-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="251c9-113">Selleks et maksud arvutataks kõigi maksustatavate summade kohta olenemata valitud arvutusmeetodist, peavad intervallid järgima järgmisi reegleid.</span><span class="sxs-lookup"><span data-stu-id="251c9-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="251c9-114">Esimese intervalli alamlimiit peab olema null.</span><span class="sxs-lookup"><span data-stu-id="251c9-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="251c9-115">Viimase intervalli ülempiir peab olema null, mis tähistab lõpmatust.</span><span class="sxs-lookup"><span data-stu-id="251c9-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="251c9-116">Intervalli ülempiir peab olema järgmise intervalli alampiir.</span><span class="sxs-lookup"><span data-stu-id="251c9-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="251c9-117">Kui summa on eelmise intervalli ülempiir ja järgmise intervalli alampiir, rakendub summale esimese intervalli käibemaksumäär.</span><span class="sxs-lookup"><span data-stu-id="251c9-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="251c9-118">Kui summa jääb väljapoole intervalle, mis on määratletud ülem- ja alampiiriga, rakendatakse käibemaksumäära null.</span><span class="sxs-lookup"><span data-stu-id="251c9-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="251c9-119">Näide. Arvutamismeetod: kogusumma</span><span class="sxs-lookup"><span data-stu-id="251c9-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="251c9-120">Lehel Käibemaksukoodid seadistatakse käibemaksumäärad järgmiste intervallidega.</span><span class="sxs-lookup"><span data-stu-id="251c9-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="251c9-121">**Alampiir**</span><span class="sxs-lookup"><span data-stu-id="251c9-121">**Minimum limit**</span></span> | <span data-ttu-id="251c9-122">**Ülempiir**</span><span class="sxs-lookup"><span data-stu-id="251c9-122">**Maximum limit**</span></span> | <span data-ttu-id="251c9-123">**Maksumäär**</span><span class="sxs-lookup"><span data-stu-id="251c9-123">**Tax rate**</span></span> |
| <span data-ttu-id="251c9-124">0,00</span><span class="sxs-lookup"><span data-stu-id="251c9-124">0.00</span></span>              | <span data-ttu-id="251c9-125">50,00</span><span class="sxs-lookup"><span data-stu-id="251c9-125">50.00</span></span>             | <span data-ttu-id="251c9-126">30%</span><span class="sxs-lookup"><span data-stu-id="251c9-126">30%</span></span>          |
| <span data-ttu-id="251c9-127">50,00</span><span class="sxs-lookup"><span data-stu-id="251c9-127">50.00</span></span>             | <span data-ttu-id="251c9-128">100,00</span><span class="sxs-lookup"><span data-stu-id="251c9-128">100.00</span></span>            | <span data-ttu-id="251c9-129">20%</span><span class="sxs-lookup"><span data-stu-id="251c9-129">20%</span></span>          |
| <span data-ttu-id="251c9-130">100,00</span><span class="sxs-lookup"><span data-stu-id="251c9-130">100.00</span></span>            | <span data-ttu-id="251c9-131">0,00</span><span class="sxs-lookup"><span data-stu-id="251c9-131">0.00</span></span>              | <span data-ttu-id="251c9-132">10%</span><span class="sxs-lookup"><span data-stu-id="251c9-132">10%</span></span>          |

<span data-ttu-id="251c9-133">Käibemaks arvutatakse kogu maksustatava summa kohta.</span><span class="sxs-lookup"><span data-stu-id="251c9-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="251c9-134">Maksustatav summa (hind)</span><span class="sxs-lookup"><span data-stu-id="251c9-134">Taxable amount (price)</span></span> | <span data-ttu-id="251c9-135">Kalkulatsioon</span><span class="sxs-lookup"><span data-stu-id="251c9-135">Calculation</span></span>    | <span data-ttu-id="251c9-136">Käibemaks</span><span class="sxs-lookup"><span data-stu-id="251c9-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="251c9-137">35,00</span><span class="sxs-lookup"><span data-stu-id="251c9-137">35.00</span></span>                  | <span data-ttu-id="251c9-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="251c9-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="251c9-139">10,50</span><span class="sxs-lookup"><span data-stu-id="251c9-139">10.50</span></span>     |
| <span data-ttu-id="251c9-140">50,00</span><span class="sxs-lookup"><span data-stu-id="251c9-140">50.00</span></span>                  | <span data-ttu-id="251c9-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="251c9-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="251c9-142">15,00</span><span class="sxs-lookup"><span data-stu-id="251c9-142">15.00</span></span>     |
| <span data-ttu-id="251c9-143">85,00</span><span class="sxs-lookup"><span data-stu-id="251c9-143">85.00</span></span>                  | <span data-ttu-id="251c9-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="251c9-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="251c9-145">17,00</span><span class="sxs-lookup"><span data-stu-id="251c9-145">17.00</span></span>     |
| <span data-ttu-id="251c9-146">305,00</span><span class="sxs-lookup"><span data-stu-id="251c9-146">305.00</span></span>                 | <span data-ttu-id="251c9-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="251c9-147">305.00 \* 0.10</span></span> | <span data-ttu-id="251c9-148">30,50</span><span class="sxs-lookup"><span data-stu-id="251c9-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="251c9-149"> Näide. Arvutusmeetod: intervall</span><span class="sxs-lookup"><span data-stu-id="251c9-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="251c9-150">Lehel Väärtused seadistatakse käibemaksumäärad järgmiste intervallidega.</span><span class="sxs-lookup"><span data-stu-id="251c9-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="251c9-151">**Alampiir**</span><span class="sxs-lookup"><span data-stu-id="251c9-151">**Minimum limit**</span></span> | <span data-ttu-id="251c9-152">**Ülempiir**</span><span class="sxs-lookup"><span data-stu-id="251c9-152">**Maximum limit**</span></span> | <span data-ttu-id="251c9-153">**Maksumäär**</span><span class="sxs-lookup"><span data-stu-id="251c9-153">**Tax rate**</span></span> |
| <span data-ttu-id="251c9-154">0,00</span><span class="sxs-lookup"><span data-stu-id="251c9-154">0.00</span></span>              | <span data-ttu-id="251c9-155">50,00</span><span class="sxs-lookup"><span data-stu-id="251c9-155">50.00</span></span>             | <span data-ttu-id="251c9-156">30%</span><span class="sxs-lookup"><span data-stu-id="251c9-156">30%</span></span>          |
| <span data-ttu-id="251c9-157">50,00</span><span class="sxs-lookup"><span data-stu-id="251c9-157">50.00</span></span>             | <span data-ttu-id="251c9-158">100,00</span><span class="sxs-lookup"><span data-stu-id="251c9-158">100.00</span></span>            | <span data-ttu-id="251c9-159">20%</span><span class="sxs-lookup"><span data-stu-id="251c9-159">20%</span></span>          |
| <span data-ttu-id="251c9-160">100,00</span><span class="sxs-lookup"><span data-stu-id="251c9-160">100.00</span></span>            | <span data-ttu-id="251c9-161">0,00</span><span class="sxs-lookup"><span data-stu-id="251c9-161">0.00</span></span>              | <span data-ttu-id="251c9-162">10%</span><span class="sxs-lookup"><span data-stu-id="251c9-162">10%</span></span>          |

<span data-ttu-id="251c9-163">Käibemaks on iga summa intervalli kohta arvutatud maksusummade summa.</span><span class="sxs-lookup"><span data-stu-id="251c9-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="251c9-164">Maksustatav summa (hind)</span><span class="sxs-lookup"><span data-stu-id="251c9-164">Taxable amount (price)</span></span> | <span data-ttu-id="251c9-165">Kalkulatsioon</span><span class="sxs-lookup"><span data-stu-id="251c9-165">Calculation</span></span>                                                               | <span data-ttu-id="251c9-166">Käibemaks</span><span class="sxs-lookup"><span data-stu-id="251c9-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="251c9-167">35,00</span><span class="sxs-lookup"><span data-stu-id="251c9-167">35.00</span></span>                  | <span data-ttu-id="251c9-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="251c9-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="251c9-169">10,50</span><span class="sxs-lookup"><span data-stu-id="251c9-169">10.50</span></span>     |
| <span data-ttu-id="251c9-170">50,00</span><span class="sxs-lookup"><span data-stu-id="251c9-170">50.00</span></span>                  | <span data-ttu-id="251c9-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="251c9-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="251c9-172">15,00</span><span class="sxs-lookup"><span data-stu-id="251c9-172">15.00</span></span>     |
| <span data-ttu-id="251c9-173">85,00</span><span class="sxs-lookup"><span data-stu-id="251c9-173">85.00</span></span>                  | <span data-ttu-id="251c9-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="251c9-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="251c9-175">22,00</span><span class="sxs-lookup"><span data-stu-id="251c9-175">22.00</span></span>     |
| <span data-ttu-id="251c9-176">305,00</span><span class="sxs-lookup"><span data-stu-id="251c9-176">305.00</span></span>                 | <span data-ttu-id="251c9-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="251c9-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="251c9-178">45,50</span><span class="sxs-lookup"><span data-stu-id="251c9-178">45.50</span></span>     |



<span data-ttu-id="251c9-179">Lisateabe saamiseks vaadake teemat [Käibemaksumäärade määramine väljade Marginaali alus ja Arvutusmeetod põhjal](marginal-base-field.md).</span><span class="sxs-lookup"><span data-stu-id="251c9-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>





