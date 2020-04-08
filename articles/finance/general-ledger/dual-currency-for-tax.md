---
title: Maksu topeltvaluuta tugi
description: Selles teemas selgitatakse, kuidas laiendada maksudomeenis topeltvaluuta arvestuse funktsiooni ja maksude arvutamise ja sisestamise mõju
author: EricWang
manager: Ann Beebe
ms.date: 12/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 863403dc3b2444f00f0cac27a494fc49d3d70de7
ms.sourcegitcommit: 34e543e807ac8790597f522fe3b4f0266cf4ee56
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/24/2020
ms.locfileid: "3161588"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="9cff6-103">Käibemaksu topeltvaluuta tugi</span><span class="sxs-lookup"><span data-stu-id="9cff6-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="9cff6-104">Selles teemas selgitatakse, kuidas laiendada käibemaksude topeltvaluuta arvestust ja käibemaksu arvutamise, sisestamise ja tasakaalustuste mõju.</span><span class="sxs-lookup"><span data-stu-id="9cff6-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="9cff6-105">Rakenduse Dynamics 365 Finance topeltvaluuta funktsioon lisati versioonis 8.1 (oktoober 2018).</span><span class="sxs-lookup"><span data-stu-id="9cff6-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="9cff6-106">See muudab raamatupidamise kirjete aruandevaluutas arvutamise viisi.</span><span class="sxs-lookup"><span data-stu-id="9cff6-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="9cff6-107">Varasemates versioonides teisendati kanded aruandlusvaluutasse järgmises järjestuses.</span><span class="sxs-lookup"><span data-stu-id="9cff6-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="9cff6-108">Kande kogusumma arvutati kande valuutas > kande summa teisendati arvestusvaluutaks > arvestusvaluuta summa teisendati aruandlusvaluutaks</span><span class="sxs-lookup"><span data-stu-id="9cff6-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="9cff6-109">Pärast topeltvaluuta funktsiooni lubamist teisendati kanded aruandlusvaluutasse järgmises järjestuses.</span><span class="sxs-lookup"><span data-stu-id="9cff6-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="9cff6-110">Kandevaluuta summa > Aruandlusvaluuta summa</span><span class="sxs-lookup"><span data-stu-id="9cff6-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="9cff6-111">Lisateavet topeltvaluuta kohta vt teemast [Topeltvaluuta](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="9cff6-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="9cff6-112">Topeltvaluuta toe tulemusena on funktsiooni halduses saadaval kaks uut funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="9cff6-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="9cff6-113">Käibemaksu teisendamine (väljaanne versioonis 10.0.9)</span><span class="sxs-lookup"><span data-stu-id="9cff6-113">Sales tax conversion (Release in version 10.0.9)</span></span>
- <span data-ttu-id="9cff6-114">Aruandevaluuta maksu tasakaalustuse automaatne saldo (väljaanne versioonis 10.0.11)</span><span class="sxs-lookup"><span data-stu-id="9cff6-114">Tax settlement auto balance in reporting currency (Release in version 10.0.11)</span></span>

<span data-ttu-id="9cff6-115">Käibemaksu topeltvaluuta tugi tagab, et maksud arvutatakse maksu valuutas täpselt ja et käibemaksu tasakaalustuse saldo arvutatakse täpselt nii arvestusvaluutas kui ka aruandlusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="9cff6-115">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="9cff6-116">Käibemaksu teisendamine</span><span class="sxs-lookup"><span data-stu-id="9cff6-116">Sales tax conversion</span></span>

<span data-ttu-id="9cff6-117">Parameeter **Käibemaksu teisendamine** pakub maksusumma kandevaluutast maksuvaluutasse teisendamiseks kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="9cff6-117">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="9cff6-118">Arvestusvaluuta: teekond on „Summa kandevaluutas > Summa arvestusvaluutas > Summa maksuvaluutas”.</span><span class="sxs-lookup"><span data-stu-id="9cff6-118">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="9cff6-119">Valuuta teisendamiseks kasutatakse arvestusvaluuta vahetuskursi tüüpi (konfigureeritud pearaamatu seadistuses).</span><span class="sxs-lookup"><span data-stu-id="9cff6-119">The accounting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="9cff6-120">Aruandlusvaluuta: teekond on „Summa kandevaluutas > Summa aruandlusvaluutas > Summa maksuvaluutas”.</span><span class="sxs-lookup"><span data-stu-id="9cff6-120">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="9cff6-121">Valuuta teisendamiseks kasutatakse aruandlusvaluuta vahetuskursi tüüpi (konfigureeritud pearaamatu seadistuses).</span><span class="sxs-lookup"><span data-stu-id="9cff6-121">The reporting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="9cff6-122">Näide</span><span class="sxs-lookup"><span data-stu-id="9cff6-122">Example</span></span>

<span data-ttu-id="9cff6-123">Lihtne näide selle funktsiooni demonstreerimiseks on järgmine.</span><span class="sxs-lookup"><span data-stu-id="9cff6-123">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="9cff6-124">Pearaamatu ja maksu valuuta seadistamine</span><span class="sxs-lookup"><span data-stu-id="9cff6-124">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="9cff6-125">Kande valuuta</span><span class="sxs-lookup"><span data-stu-id="9cff6-125">Transaction currency</span></span> | <span data-ttu-id="9cff6-126">Arvestusvaluuta</span><span class="sxs-lookup"><span data-stu-id="9cff6-126">Accounting currency</span></span> | <span data-ttu-id="9cff6-127">Aruandlusvaluuta</span><span class="sxs-lookup"><span data-stu-id="9cff6-127">Reporting currency</span></span> | <span data-ttu-id="9cff6-128">Maksuvaluuta</span><span class="sxs-lookup"><span data-stu-id="9cff6-128">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="9cff6-129"> eurot</span><span class="sxs-lookup"><span data-stu-id="9cff6-129">EUR</span></span>                  | <span data-ttu-id="9cff6-130">USA dollar</span><span class="sxs-lookup"><span data-stu-id="9cff6-130">USD</span></span>                 | <span data-ttu-id="9cff6-131">GBP</span><span class="sxs-lookup"><span data-stu-id="9cff6-131">GBP</span></span>                | <span data-ttu-id="9cff6-132">GBP</span><span class="sxs-lookup"><span data-stu-id="9cff6-132">GBP</span></span>          |

<span data-ttu-id="9cff6-133">Valuutakurss</span><span class="sxs-lookup"><span data-stu-id="9cff6-133">Exchange rate</span></span>

| <span data-ttu-id="9cff6-134">Valuutast</span><span class="sxs-lookup"><span data-stu-id="9cff6-134">From currency</span></span> | <span data-ttu-id="9cff6-135">Valuutaks</span><span class="sxs-lookup"><span data-stu-id="9cff6-135">To currency</span></span> | <span data-ttu-id="9cff6-136">Tegur</span><span class="sxs-lookup"><span data-stu-id="9cff6-136">Factor</span></span> | <span data-ttu-id="9cff6-137">Valuutakurss</span><span class="sxs-lookup"><span data-stu-id="9cff6-137">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="9cff6-138"> eurot</span><span class="sxs-lookup"><span data-stu-id="9cff6-138">EUR</span></span>           | <span data-ttu-id="9cff6-139">USA dollar</span><span class="sxs-lookup"><span data-stu-id="9cff6-139">USD</span></span>         | <span data-ttu-id="9cff6-140">1</span><span class="sxs-lookup"><span data-stu-id="9cff6-140">1</span></span>      | <span data-ttu-id="9cff6-141">1.11</span><span class="sxs-lookup"><span data-stu-id="9cff6-141">1.11</span></span>          |
| <span data-ttu-id="9cff6-142"> eurot</span><span class="sxs-lookup"><span data-stu-id="9cff6-142">EUR</span></span>           | <span data-ttu-id="9cff6-143">GBP</span><span class="sxs-lookup"><span data-stu-id="9cff6-143">GBP</span></span>         | <span data-ttu-id="9cff6-144">1</span><span class="sxs-lookup"><span data-stu-id="9cff6-144">1</span></span>      | <span data-ttu-id="9cff6-145">0.83</span><span class="sxs-lookup"><span data-stu-id="9cff6-145">0.83</span></span>          |
| <span data-ttu-id="9cff6-146">USA dollar</span><span class="sxs-lookup"><span data-stu-id="9cff6-146">USD</span></span>           | <span data-ttu-id="9cff6-147">GBP</span><span class="sxs-lookup"><span data-stu-id="9cff6-147">GBP</span></span>         | <span data-ttu-id="9cff6-148">1</span><span class="sxs-lookup"><span data-stu-id="9cff6-148">1</span></span>      | <span data-ttu-id="9cff6-149">0.75</span><span class="sxs-lookup"><span data-stu-id="9cff6-149">0.75</span></span>          |

<span data-ttu-id="9cff6-150">Maksusumma arvutamine erinevate parameetrite valikutega</span><span class="sxs-lookup"><span data-stu-id="9cff6-150">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="9cff6-151">Maksusumma = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="9cff6-151">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="9cff6-152">Käibemaksu teisendamise parameetrid</span><span class="sxs-lookup"><span data-stu-id="9cff6-152">Sales tax conversion parameters</span></span> | <span data-ttu-id="9cff6-153">Kande valuuta (EUR)</span><span class="sxs-lookup"><span data-stu-id="9cff6-153">Transaction currency (EUR)</span></span> | <span data-ttu-id="9cff6-154">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="9cff6-154">Accounting currency (USD)</span></span> | <span data-ttu-id="9cff6-155">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="9cff6-155">Reporting currency (GBP)</span></span> | <span data-ttu-id="9cff6-156">Maksuvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="9cff6-156">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="9cff6-157">Arvestusvaluuta</span><span class="sxs-lookup"><span data-stu-id="9cff6-157">Accounting currency</span></span>             | <span data-ttu-id="9cff6-158">100</span><span class="sxs-lookup"><span data-stu-id="9cff6-158">100</span></span>                        | <span data-ttu-id="9cff6-159">111</span><span class="sxs-lookup"><span data-stu-id="9cff6-159">111</span></span>                       | <span data-ttu-id="9cff6-160">83</span><span class="sxs-lookup"><span data-stu-id="9cff6-160">83</span></span>                       | <span data-ttu-id="9cff6-161">**83.25**</span><span class="sxs-lookup"><span data-stu-id="9cff6-161">**83.25**</span></span>          |
| <span data-ttu-id="9cff6-162">Aruandlusvaluuta</span><span class="sxs-lookup"><span data-stu-id="9cff6-162">Reporting currency</span></span>              | <span data-ttu-id="9cff6-163">100</span><span class="sxs-lookup"><span data-stu-id="9cff6-163">100</span></span>                        | <span data-ttu-id="9cff6-164">111</span><span class="sxs-lookup"><span data-stu-id="9cff6-164">111</span></span>                       | <span data-ttu-id="9cff6-165">83</span><span class="sxs-lookup"><span data-stu-id="9cff6-165">83</span></span>                       | <span data-ttu-id="9cff6-166">**83**</span><span class="sxs-lookup"><span data-stu-id="9cff6-166">**83**</span></span>             |

<span data-ttu-id="9cff6-167">Selle parameetri saab konfigureerida maksuhalduri nõuetelevastavuse nõude alusel.</span><span class="sxs-lookup"><span data-stu-id="9cff6-167">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="9cff6-168">Täienduse kaalutlus</span><span class="sxs-lookup"><span data-stu-id="9cff6-168">Upgrade Consideration</span></span>

<span data-ttu-id="9cff6-169">See funktsioon rakendub ainult uutele kannetele.</span><span class="sxs-lookup"><span data-stu-id="9cff6-169">This feature will only apply for new transactions.</span></span> <span data-ttu-id="9cff6-170">Tabelis TAXTRANS juba salvestatud, kuid veel mitte tasakaalustatud maksukannete puhul ei arvuta süsteem maksu summat maksu valuutas ümber, kuna maksu sisestamise hetke vahetuskurss on juba puudu.</span><span class="sxs-lookup"><span data-stu-id="9cff6-170">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="9cff6-171">Eelneva stsenaariumi vältimiseks soovitame muuta selle parameetri väärtust uues (puhtas) maksu tasakaalustusperioodil, mis ei sisalda ühtegi tasakaalustamata maksukannet.</span><span class="sxs-lookup"><span data-stu-id="9cff6-171">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="9cff6-172">Selle väärtuse muutmiseks maksu tasakaalustusperioodi keskel käivitage enne selle parameetri väärtuse muutmist programm „Käibemaksu tasakaalustamine ja sisestamine” praeguse maksu tasakaalustusperioodi jaoks.</span><span class="sxs-lookup"><span data-stu-id="9cff6-172">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="9cff6-173">Aruandlusvaluuta maksu summa jälgimine</span><span class="sxs-lookup"><span data-stu-id="9cff6-173">Track reporting currency tax amount</span></span>

<span data-ttu-id="9cff6-174">Aruandlusvaluuta summade jälgimiseks lisati maksudega seotud tabelitesse kolm uut välja.</span><span class="sxs-lookup"><span data-stu-id="9cff6-174">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="9cff6-175">Need väljad asuvad tabelites TAXUNCOMMITTED ja TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="9cff6-175">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="9cff6-176">TaxAmountRep: maksusumma aruandlusvaluutas</span><span class="sxs-lookup"><span data-stu-id="9cff6-176">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="9cff6-177">TaxBaseAmountRep: aruandlusvaluuta baassumma</span><span class="sxs-lookup"><span data-stu-id="9cff6-177">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="9cff6-178">TaxInCostPriceRep: mahaarvamatu summa aruandlusvaluutas</span><span class="sxs-lookup"><span data-stu-id="9cff6-178">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="9cff6-179">Ainult tabelis TAXUNCOMMITTED salvestatud maks, mis pole veel postitatud, arvutab süsteem maksu summa postitmise ajal aruandlusvaluutas ümber ja salvestab tabelis TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="9cff6-179">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="9cff6-180">See väljaanne ei sisalda muudatusi aruannetes ega vormides, mis näitavad maksu summat aruandlusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="9cff6-180">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="9cff6-181">Aruannete ja vormide muudatused edastatakse tulevases väljaannetes.</span><span class="sxs-lookup"><span data-stu-id="9cff6-181">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="9cff6-182">Maksu tasakaalustuse automaatne saldo aruandlusvaluutas</span><span class="sxs-lookup"><span data-stu-id="9cff6-182">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="9cff6-183">Kui maksu tasakaalustamine ei ole aruandlusvaluuta jaoks mingil põhjusel tasakaalus, näiteks müügimaksu teisendustee on „Arvestusvaluuta” või vahetuskurss muutub samal maksu tasakaalustamise perioodil, siis süsteem loob automaatselt raamatupidamise kirjed, et reguleerida maksu summa erinevust ja tasakaalustada seda realiseeritud vahetusega saadud tulu/kulu kontoga, mis on pearaamatu seadistuses konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="9cff6-183">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, thebn the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="9cff6-184">Kasutades selle funktsiooni demonstreerimiseks eelmist näidet, oletagem, et tabeli TAXTRANS andmed on sisestamise ajal järgmised.</span><span class="sxs-lookup"><span data-stu-id="9cff6-184">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="9cff6-185">Käibemaksu teisendamise parameetrid</span><span class="sxs-lookup"><span data-stu-id="9cff6-185">Sales tax conversion parameters</span></span> | <span data-ttu-id="9cff6-186">Kande valuuta (EUR)</span><span class="sxs-lookup"><span data-stu-id="9cff6-186">Transaction currency (EUR)</span></span> | <span data-ttu-id="9cff6-187">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="9cff6-187">Accounting currency (USD)</span></span> | <span data-ttu-id="9cff6-188">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="9cff6-188">Reporting currency (GBP)</span></span> | <span data-ttu-id="9cff6-189">Maksuvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="9cff6-189">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="9cff6-190">Arvestusvaluuta</span><span class="sxs-lookup"><span data-stu-id="9cff6-190">Accounting currency</span></span>             | <span data-ttu-id="9cff6-191">100</span><span class="sxs-lookup"><span data-stu-id="9cff6-191">100</span></span>                        | <span data-ttu-id="9cff6-192">111</span><span class="sxs-lookup"><span data-stu-id="9cff6-192">111</span></span>                       | <span data-ttu-id="9cff6-193">83</span><span class="sxs-lookup"><span data-stu-id="9cff6-193">83</span></span>                       | <span data-ttu-id="9cff6-194">**83.25**</span><span class="sxs-lookup"><span data-stu-id="9cff6-194">**83.25**</span></span>          |
| <span data-ttu-id="9cff6-195">Aruandlusvaluuta</span><span class="sxs-lookup"><span data-stu-id="9cff6-195">Reporting currency</span></span>              | <span data-ttu-id="9cff6-196">100</span><span class="sxs-lookup"><span data-stu-id="9cff6-196">100</span></span>                        | <span data-ttu-id="9cff6-197">111</span><span class="sxs-lookup"><span data-stu-id="9cff6-197">111</span></span>                       | <span data-ttu-id="9cff6-198">83</span><span class="sxs-lookup"><span data-stu-id="9cff6-198">83</span></span>                       | <span data-ttu-id="9cff6-199">**83**</span><span class="sxs-lookup"><span data-stu-id="9cff6-199">**83**</span></span>             |

<span data-ttu-id="9cff6-200">Kui käivitate käibemaksu tasakaalustuse programmi kuu lõpus, on raamatupidamise kirje järgmine.</span><span class="sxs-lookup"><span data-stu-id="9cff6-200">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="9cff6-201">Stsenaarium: müügimaksu teisendamine = „arvestusvaluuta”</span><span class="sxs-lookup"><span data-stu-id="9cff6-201">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="9cff6-202">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="9cff6-202">Main account</span></span>           | <span data-ttu-id="9cff6-203">Kande valuuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="9cff6-203">Transaction currency (GBP)</span></span> | <span data-ttu-id="9cff6-204">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="9cff6-204">Accounting currency (USD)</span></span> | <span data-ttu-id="9cff6-205">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="9cff6-205">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="9cff6-206">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="9cff6-206">Tax Payable/Receivable</span></span> | <span data-ttu-id="9cff6-207">–83,25</span><span class="sxs-lookup"><span data-stu-id="9cff6-207">-83.25</span></span>                     | <span data-ttu-id="9cff6-208">–111</span><span class="sxs-lookup"><span data-stu-id="9cff6-208">-111</span></span>                      | <span data-ttu-id="9cff6-209">–83,25</span><span class="sxs-lookup"><span data-stu-id="9cff6-209">-83.25</span></span>                   |
| <span data-ttu-id="9cff6-210">Maksu tasakaalustus</span><span class="sxs-lookup"><span data-stu-id="9cff6-210">Tax Settlement</span></span>         | <span data-ttu-id="9cff6-211">83.25</span><span class="sxs-lookup"><span data-stu-id="9cff6-211">83.25</span></span>                      | <span data-ttu-id="9cff6-212">111</span><span class="sxs-lookup"><span data-stu-id="9cff6-212">111</span></span>                       | <span data-ttu-id="9cff6-213">83.25</span><span class="sxs-lookup"><span data-stu-id="9cff6-213">83.25</span></span>                    |
| <span data-ttu-id="9cff6-214">Realiseeritud kasum/kahjum</span><span class="sxs-lookup"><span data-stu-id="9cff6-214">Realized Gain/Loss</span></span>     | <span data-ttu-id="9cff6-215">0</span><span class="sxs-lookup"><span data-stu-id="9cff6-215">0</span></span>                          | <span data-ttu-id="9cff6-216">0</span><span class="sxs-lookup"><span data-stu-id="9cff6-216">0</span></span>                         | <span data-ttu-id="9cff6-217">–0,25</span><span class="sxs-lookup"><span data-stu-id="9cff6-217">-0.25</span></span>                    |
| <span data-ttu-id="9cff6-218">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="9cff6-218">Tax Payable/Receivable</span></span> | <span data-ttu-id="9cff6-219">0</span><span class="sxs-lookup"><span data-stu-id="9cff6-219">0</span></span>                          | <span data-ttu-id="9cff6-220">0</span><span class="sxs-lookup"><span data-stu-id="9cff6-220">0</span></span>                         | <span data-ttu-id="9cff6-221">0.25</span><span class="sxs-lookup"><span data-stu-id="9cff6-221">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="9cff6-222">Stsenaarium: müügimaksu teisendamine = „aruandlusvaluuta”</span><span class="sxs-lookup"><span data-stu-id="9cff6-222">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="9cff6-223">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="9cff6-223">Main account</span></span>           | <span data-ttu-id="9cff6-224">Kande valuuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="9cff6-224">Transaction currency (GBP)</span></span> | <span data-ttu-id="9cff6-225">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="9cff6-225">Accounting currency (USD)</span></span> | <span data-ttu-id="9cff6-226">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="9cff6-226">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="9cff6-227">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="9cff6-227">Tax Payable/Receivable</span></span> | <span data-ttu-id="9cff6-228">–83</span><span class="sxs-lookup"><span data-stu-id="9cff6-228">-83</span></span>                        | <span data-ttu-id="9cff6-229">–110,67</span><span class="sxs-lookup"><span data-stu-id="9cff6-229">-110.67</span></span>                   | <span data-ttu-id="9cff6-230">–83</span><span class="sxs-lookup"><span data-stu-id="9cff6-230">-83</span></span>                      |
| <span data-ttu-id="9cff6-231">Maksu tasakaalustus</span><span class="sxs-lookup"><span data-stu-id="9cff6-231">Tax Settlement</span></span>         | <span data-ttu-id="9cff6-232">83</span><span class="sxs-lookup"><span data-stu-id="9cff6-232">83</span></span>                         | <span data-ttu-id="9cff6-233">110.67</span><span class="sxs-lookup"><span data-stu-id="9cff6-233">110.67</span></span>                    | <span data-ttu-id="9cff6-234">83</span><span class="sxs-lookup"><span data-stu-id="9cff6-234">83</span></span>                       |
| <span data-ttu-id="9cff6-235">Realiseeritud kasum/kahjum</span><span class="sxs-lookup"><span data-stu-id="9cff6-235">Realized Gain/Loss</span></span>     | <span data-ttu-id="9cff6-236">0</span><span class="sxs-lookup"><span data-stu-id="9cff6-236">0</span></span>                          | <span data-ttu-id="9cff6-237">0.33</span><span class="sxs-lookup"><span data-stu-id="9cff6-237">0.33</span></span>                      | <span data-ttu-id="9cff6-238">0</span><span class="sxs-lookup"><span data-stu-id="9cff6-238">0</span></span>                        |
| <span data-ttu-id="9cff6-239">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="9cff6-239">Tax Payable/Receivable</span></span> | <span data-ttu-id="9cff6-240">0</span><span class="sxs-lookup"><span data-stu-id="9cff6-240">0</span></span>                          | <span data-ttu-id="9cff6-241">–0,33</span><span class="sxs-lookup"><span data-stu-id="9cff6-241">-0.33</span></span>                     | <span data-ttu-id="9cff6-242">0</span><span class="sxs-lookup"><span data-stu-id="9cff6-242">0</span></span>                        |



<span data-ttu-id="9cff6-243">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="9cff6-243">For more information, see the following topics:</span></span>

- [<span data-ttu-id="9cff6-244">Topeltvaluuta</span><span class="sxs-lookup"><span data-stu-id="9cff6-244">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="9cff6-245">Käibemaksu ülevaade</span><span class="sxs-lookup"><span data-stu-id="9cff6-245">Sales tax overview</span></span>](indirect-taxes-overview.md)

