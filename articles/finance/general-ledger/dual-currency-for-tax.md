---
title: Maksu topeltvaluuta tugi
description: Selles teemas selgitatakse, kuidas laiendada maksudomeenis topeltvaluuta arvestuse funktsiooni ja maksude arvutamise ja sisestamise mõju
author: EricWang
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0a3245febe31857181d17bba42e12b65f4ebb40f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832966"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="c5721-103">Käibemaksu topeltvaluuta tugi</span><span class="sxs-lookup"><span data-stu-id="c5721-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5721-104">Selles teemas selgitatakse, kuidas laiendada käibemaksude topeltvaluuta arvestust ja käibemaksu arvutamise, sisestamise ja tasakaalustuste mõju.</span><span class="sxs-lookup"><span data-stu-id="c5721-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="c5721-105">Rakenduse Dynamics 365 Finance topeltvaluuta funktsioon lisati versioonis 8.1 (oktoober 2018).</span><span class="sxs-lookup"><span data-stu-id="c5721-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="c5721-106">See muudab raamatupidamise kirjete aruandevaluutas arvutamise viisi.</span><span class="sxs-lookup"><span data-stu-id="c5721-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="c5721-107">Varasemates versioonides teisendati kanded aruandlusvaluutasse järgmises järjestuses.</span><span class="sxs-lookup"><span data-stu-id="c5721-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="c5721-108">Kande kogusumma arvutati kande valuutas > kande summa teisendati arvestusvaluutaks > arvestusvaluuta summa teisendati aruandlusvaluutaks</span><span class="sxs-lookup"><span data-stu-id="c5721-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="c5721-109">Pärast topeltvaluuta funktsiooni lubamist teisendati kanded aruandlusvaluutasse järgmises järjestuses.</span><span class="sxs-lookup"><span data-stu-id="c5721-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="c5721-110">Kandevaluuta summa > Aruandlusvaluuta summa</span><span class="sxs-lookup"><span data-stu-id="c5721-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="c5721-111">Lisateavet topeltvaluuta kohta vt teemast [Topeltvaluuta](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="c5721-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="c5721-112">Topeltvaluuta toe tulemusena on funktsiooni halduses saadaval kaks uut funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="c5721-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="c5721-113">Käibemaksu konverteerimine (uus versioonis 10.0.13)</span><span class="sxs-lookup"><span data-stu-id="c5721-113">Sales tax conversion (new in version 10.0.13)</span></span>

<span data-ttu-id="c5721-114">Käibemaksu topeltvaluuta tugi tagab, et maksud arvutatakse maksu valuutas täpselt ja et käibemaksu tasakaalustuse saldo arvutatakse täpselt nii arvestusvaluutas kui ka aruandlusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="c5721-114">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="c5721-115">Käibemaksu teisendamine</span><span class="sxs-lookup"><span data-stu-id="c5721-115">Sales tax conversion</span></span>

<span data-ttu-id="c5721-116">Parameeter **Käibemaksu teisendamine** pakub maksusumma kandevaluutast maksuvaluutasse teisendamiseks kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="c5721-116">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="c5721-117">Arvestusvaluuta: teekond on „Summa kandevaluutas > Summa arvestusvaluutas > Summa maksuvaluutas”.</span><span class="sxs-lookup"><span data-stu-id="c5721-117">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="c5721-118">Valuuta konverteerimiseks kasutatakse arvestusvaluuta vahetuskursi tüüpi (konfigureeritud pearaamatu seadistuses).</span><span class="sxs-lookup"><span data-stu-id="c5721-118">The accounting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="c5721-119">Aruandlusvaluuta: teekond on „Summa kandevaluutas > Summa aruandlusvaluutas > Summa maksuvaluutas”.</span><span class="sxs-lookup"><span data-stu-id="c5721-119">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="c5721-120">Valuuta konverteerimiseks kasutatakse aruandlusvaluuta vahetuskursi tüüpi (konfigureeritud pearaamatu seadistuses).</span><span class="sxs-lookup"><span data-stu-id="c5721-120">The reporting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="c5721-121">Näide</span><span class="sxs-lookup"><span data-stu-id="c5721-121">Example</span></span>

<span data-ttu-id="c5721-122">Lihtne näide selle funktsiooni demonstreerimiseks on järgmine.</span><span class="sxs-lookup"><span data-stu-id="c5721-122">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="c5721-123">Pearaamatu ja maksu valuuta seadistamine</span><span class="sxs-lookup"><span data-stu-id="c5721-123">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="c5721-124">Kande valuuta</span><span class="sxs-lookup"><span data-stu-id="c5721-124">Transaction currency</span></span> | <span data-ttu-id="c5721-125">Arvestusvaluuta</span><span class="sxs-lookup"><span data-stu-id="c5721-125">Accounting currency</span></span> | <span data-ttu-id="c5721-126">Aruandlusvaluuta</span><span class="sxs-lookup"><span data-stu-id="c5721-126">Reporting currency</span></span> | <span data-ttu-id="c5721-127">Maksuvaluuta</span><span class="sxs-lookup"><span data-stu-id="c5721-127">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="c5721-128"> eurot</span><span class="sxs-lookup"><span data-stu-id="c5721-128">EUR</span></span>                  | <span data-ttu-id="c5721-129">USA dollar</span><span class="sxs-lookup"><span data-stu-id="c5721-129">USD</span></span>                 | <span data-ttu-id="c5721-130">GBP</span><span class="sxs-lookup"><span data-stu-id="c5721-130">GBP</span></span>                | <span data-ttu-id="c5721-131">GBP</span><span class="sxs-lookup"><span data-stu-id="c5721-131">GBP</span></span>          |

<span data-ttu-id="c5721-132">Valuutakurss</span><span class="sxs-lookup"><span data-stu-id="c5721-132">Exchange rate</span></span>

| <span data-ttu-id="c5721-133">Valuutast</span><span class="sxs-lookup"><span data-stu-id="c5721-133">From currency</span></span> | <span data-ttu-id="c5721-134">Valuutaks</span><span class="sxs-lookup"><span data-stu-id="c5721-134">To currency</span></span> | <span data-ttu-id="c5721-135">Tegur</span><span class="sxs-lookup"><span data-stu-id="c5721-135">Factor</span></span> | <span data-ttu-id="c5721-136">Valuutakurss</span><span class="sxs-lookup"><span data-stu-id="c5721-136">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="c5721-137"> eurot</span><span class="sxs-lookup"><span data-stu-id="c5721-137">EUR</span></span>           | <span data-ttu-id="c5721-138">USA dollar</span><span class="sxs-lookup"><span data-stu-id="c5721-138">USD</span></span>         | <span data-ttu-id="c5721-139">1</span><span class="sxs-lookup"><span data-stu-id="c5721-139">1</span></span>      | <span data-ttu-id="c5721-140">1.11</span><span class="sxs-lookup"><span data-stu-id="c5721-140">1.11</span></span>          |
| <span data-ttu-id="c5721-141"> eurot</span><span class="sxs-lookup"><span data-stu-id="c5721-141">EUR</span></span>           | <span data-ttu-id="c5721-142">GBP</span><span class="sxs-lookup"><span data-stu-id="c5721-142">GBP</span></span>         | <span data-ttu-id="c5721-143">1</span><span class="sxs-lookup"><span data-stu-id="c5721-143">1</span></span>      | <span data-ttu-id="c5721-144">0.83</span><span class="sxs-lookup"><span data-stu-id="c5721-144">0.83</span></span>          |
| <span data-ttu-id="c5721-145">USA dollar</span><span class="sxs-lookup"><span data-stu-id="c5721-145">USD</span></span>           | <span data-ttu-id="c5721-146">GBP</span><span class="sxs-lookup"><span data-stu-id="c5721-146">GBP</span></span>         | <span data-ttu-id="c5721-147">1</span><span class="sxs-lookup"><span data-stu-id="c5721-147">1</span></span>      | <span data-ttu-id="c5721-148">0.75</span><span class="sxs-lookup"><span data-stu-id="c5721-148">0.75</span></span>          |

<span data-ttu-id="c5721-149">Maksusumma arvutamine erinevate parameetrite valikutega</span><span class="sxs-lookup"><span data-stu-id="c5721-149">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="c5721-150">Maksusumma = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="c5721-150">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="c5721-151">Käibemaksu teisendamise parameetrid</span><span class="sxs-lookup"><span data-stu-id="c5721-151">Sales tax conversion parameters</span></span> | <span data-ttu-id="c5721-152">Kande valuuta (EUR)</span><span class="sxs-lookup"><span data-stu-id="c5721-152">Transaction currency (EUR)</span></span> | <span data-ttu-id="c5721-153">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="c5721-153">Accounting currency (USD)</span></span> | <span data-ttu-id="c5721-154">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="c5721-154">Reporting currency (GBP)</span></span> | <span data-ttu-id="c5721-155">Maksuvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="c5721-155">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="c5721-156">Arvestusvaluuta</span><span class="sxs-lookup"><span data-stu-id="c5721-156">Accounting currency</span></span>             | <span data-ttu-id="c5721-157">100</span><span class="sxs-lookup"><span data-stu-id="c5721-157">100</span></span>                        | <span data-ttu-id="c5721-158">111</span><span class="sxs-lookup"><span data-stu-id="c5721-158">111</span></span>                       | <span data-ttu-id="c5721-159">83</span><span class="sxs-lookup"><span data-stu-id="c5721-159">83</span></span>                       | <span data-ttu-id="c5721-160">**83.25**</span><span class="sxs-lookup"><span data-stu-id="c5721-160">**83.25**</span></span>          |
| <span data-ttu-id="c5721-161">Aruandlusvaluuta</span><span class="sxs-lookup"><span data-stu-id="c5721-161">Reporting currency</span></span>              | <span data-ttu-id="c5721-162">100</span><span class="sxs-lookup"><span data-stu-id="c5721-162">100</span></span>                        | <span data-ttu-id="c5721-163">111</span><span class="sxs-lookup"><span data-stu-id="c5721-163">111</span></span>                       | <span data-ttu-id="c5721-164">83</span><span class="sxs-lookup"><span data-stu-id="c5721-164">83</span></span>                       | <span data-ttu-id="c5721-165">**83**</span><span class="sxs-lookup"><span data-stu-id="c5721-165">**83**</span></span>             |

<span data-ttu-id="c5721-166">Selle parameetri saab konfigureerida maksuhalduri nõuetelevastavuse nõude alusel.</span><span class="sxs-lookup"><span data-stu-id="c5721-166">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="c5721-167">Täienduse kaalutlus</span><span class="sxs-lookup"><span data-stu-id="c5721-167">Upgrade Consideration</span></span>

<span data-ttu-id="c5721-168">See funktsioon rakendub ainult uutele kannetele.</span><span class="sxs-lookup"><span data-stu-id="c5721-168">This feature will only apply for new transactions.</span></span> <span data-ttu-id="c5721-169">Tabelis TAXTRANS juba salvestatud, kuid veel mitte tasakaalustatud maksukannete puhul ei arvuta süsteem maksu summat maksu valuutas ümber, kuna maksu sisestamise hetke vahetuskurss on juba puudu.</span><span class="sxs-lookup"><span data-stu-id="c5721-169">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="c5721-170">Eelneva stsenaariumi vältimiseks soovitame muuta selle parameetri väärtust uues (puhtas) maksu tasakaalustusperioodil, mis ei sisalda ühtegi tasakaalustamata maksukannet.</span><span class="sxs-lookup"><span data-stu-id="c5721-170">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="c5721-171">Selle väärtuse muutmiseks maksu tasakaalustusperioodi keskel käivitage enne selle parameetri väärtuse muutmist programm „Käibemaksu tasakaalustamine ja sisestamine” praeguse maksu tasakaalustusperioodi jaoks.</span><span class="sxs-lookup"><span data-stu-id="c5721-171">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="c5721-172">Aruandlusvaluuta maksu summa jälgimine</span><span class="sxs-lookup"><span data-stu-id="c5721-172">Track reporting currency tax amount</span></span>

<span data-ttu-id="c5721-173">Aruandlusvaluuta summade jälgimiseks lisati maksudega seotud tabelitesse kolm uut välja.</span><span class="sxs-lookup"><span data-stu-id="c5721-173">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="c5721-174">Need väljad asuvad tabelites TAXUNCOMMITTED ja TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="c5721-174">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="c5721-175">TaxAmountRep: maksusumma aruandlusvaluutas</span><span class="sxs-lookup"><span data-stu-id="c5721-175">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="c5721-176">TaxBaseAmountRep: aruandlusvaluuta baassumma</span><span class="sxs-lookup"><span data-stu-id="c5721-176">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="c5721-177">TaxInCostPriceRep: mahaarvamatu summa aruandlusvaluutas</span><span class="sxs-lookup"><span data-stu-id="c5721-177">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="c5721-178">Ainult tabelis TAXUNCOMMITTED salvestatud maks, mis pole veel postitatud, arvutab süsteem maksu summa postitmise ajal aruandlusvaluutas ümber ja salvestab tabelis TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="c5721-178">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="c5721-179">See väljaanne ei sisalda muudatusi aruannetes ega vormides, mis näitavad maksu summat aruandlusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="c5721-179">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="c5721-180">Aruannete ja vormide muudatused edastatakse tulevases väljaannetes.</span><span class="sxs-lookup"><span data-stu-id="c5721-180">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="c5721-181">Maksu tasakaalustuse automaatne saldo aruandlusvaluutas</span><span class="sxs-lookup"><span data-stu-id="c5721-181">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="c5721-182">Kui maksu tasakaalustamine ei ole aruandlusvaluuta jaoks mingil põhjusel tasakaalus, näiteks müügimaksu teisendustee on „Arvestusvaluuta” või vahetuskurss muutub samal maksu tasakaalustamise perioodil, siis süsteem loob automaatselt raamatupidamise kirjed, et reguleerida maksu summa erinevust ja tasakaalustada seda realiseeritud vahetusega saadud tulu/kulu kontoga, mis on pearaamatu seadistuses konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="c5721-182">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, then the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="c5721-183">Kasutades selle funktsiooni demonstreerimiseks eelmist näidet, oletagem, et tabeli TAXTRANS andmed on sisestamise ajal järgmised.</span><span class="sxs-lookup"><span data-stu-id="c5721-183">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="c5721-184">Käibemaksu teisendamise parameetrid</span><span class="sxs-lookup"><span data-stu-id="c5721-184">Sales tax conversion parameters</span></span> | <span data-ttu-id="c5721-185">Kande valuuta (EUR)</span><span class="sxs-lookup"><span data-stu-id="c5721-185">Transaction currency (EUR)</span></span> | <span data-ttu-id="c5721-186">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="c5721-186">Accounting currency (USD)</span></span> | <span data-ttu-id="c5721-187">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="c5721-187">Reporting currency (GBP)</span></span> | <span data-ttu-id="c5721-188">Maksuvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="c5721-188">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="c5721-189">Arvestusvaluuta</span><span class="sxs-lookup"><span data-stu-id="c5721-189">Accounting currency</span></span>             | <span data-ttu-id="c5721-190">100</span><span class="sxs-lookup"><span data-stu-id="c5721-190">100</span></span>                        | <span data-ttu-id="c5721-191">111</span><span class="sxs-lookup"><span data-stu-id="c5721-191">111</span></span>                       | <span data-ttu-id="c5721-192">83</span><span class="sxs-lookup"><span data-stu-id="c5721-192">83</span></span>                       | <span data-ttu-id="c5721-193">**83.25**</span><span class="sxs-lookup"><span data-stu-id="c5721-193">**83.25**</span></span>          |
| <span data-ttu-id="c5721-194">Aruandlusvaluuta</span><span class="sxs-lookup"><span data-stu-id="c5721-194">Reporting currency</span></span>              | <span data-ttu-id="c5721-195">100</span><span class="sxs-lookup"><span data-stu-id="c5721-195">100</span></span>                        | <span data-ttu-id="c5721-196">111</span><span class="sxs-lookup"><span data-stu-id="c5721-196">111</span></span>                       | <span data-ttu-id="c5721-197">83</span><span class="sxs-lookup"><span data-stu-id="c5721-197">83</span></span>                       | <span data-ttu-id="c5721-198">**83**</span><span class="sxs-lookup"><span data-stu-id="c5721-198">**83**</span></span>             |

<span data-ttu-id="c5721-199">Kui käivitate käibemaksu tasakaalustuse programmi kuu lõpus, on raamatupidamise kirje järgmine.</span><span class="sxs-lookup"><span data-stu-id="c5721-199">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="c5721-200">Stsenaarium: müügimaksu teisendamine = „arvestusvaluuta”</span><span class="sxs-lookup"><span data-stu-id="c5721-200">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="c5721-201">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="c5721-201">Main account</span></span>           | <span data-ttu-id="c5721-202">Kande valuuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="c5721-202">Transaction currency (GBP)</span></span> | <span data-ttu-id="c5721-203">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="c5721-203">Accounting currency (USD)</span></span> | <span data-ttu-id="c5721-204">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="c5721-204">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="c5721-205">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="c5721-205">Tax Payable/Receivable</span></span> | <span data-ttu-id="c5721-206">–83,25</span><span class="sxs-lookup"><span data-stu-id="c5721-206">-83.25</span></span>                     | <span data-ttu-id="c5721-207">–111</span><span class="sxs-lookup"><span data-stu-id="c5721-207">-111</span></span>                      | <span data-ttu-id="c5721-208">–83,25</span><span class="sxs-lookup"><span data-stu-id="c5721-208">-83.25</span></span>                   |
| <span data-ttu-id="c5721-209">Maksu tasakaalustus</span><span class="sxs-lookup"><span data-stu-id="c5721-209">Tax Settlement</span></span>         | <span data-ttu-id="c5721-210">83.25</span><span class="sxs-lookup"><span data-stu-id="c5721-210">83.25</span></span>                      | <span data-ttu-id="c5721-211">111</span><span class="sxs-lookup"><span data-stu-id="c5721-211">111</span></span>                       | <span data-ttu-id="c5721-212">83.25</span><span class="sxs-lookup"><span data-stu-id="c5721-212">83.25</span></span>                    |
| <span data-ttu-id="c5721-213">Realiseeritud kasum/kahjum</span><span class="sxs-lookup"><span data-stu-id="c5721-213">Realized Gain/Loss</span></span>     | <span data-ttu-id="c5721-214">0</span><span class="sxs-lookup"><span data-stu-id="c5721-214">0</span></span>                          | <span data-ttu-id="c5721-215">0</span><span class="sxs-lookup"><span data-stu-id="c5721-215">0</span></span>                         | <span data-ttu-id="c5721-216">–0,25</span><span class="sxs-lookup"><span data-stu-id="c5721-216">-0.25</span></span>                    |
| <span data-ttu-id="c5721-217">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="c5721-217">Tax Payable/Receivable</span></span> | <span data-ttu-id="c5721-218">0</span><span class="sxs-lookup"><span data-stu-id="c5721-218">0</span></span>                          | <span data-ttu-id="c5721-219">0</span><span class="sxs-lookup"><span data-stu-id="c5721-219">0</span></span>                         | <span data-ttu-id="c5721-220">0.25</span><span class="sxs-lookup"><span data-stu-id="c5721-220">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="c5721-221">Stsenaarium: müügimaksu teisendamine = „aruandlusvaluuta”</span><span class="sxs-lookup"><span data-stu-id="c5721-221">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="c5721-222">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="c5721-222">Main account</span></span>           | <span data-ttu-id="c5721-223">Kande valuuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="c5721-223">Transaction currency (GBP)</span></span> | <span data-ttu-id="c5721-224">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="c5721-224">Accounting currency (USD)</span></span> | <span data-ttu-id="c5721-225">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="c5721-225">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="c5721-226">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="c5721-226">Tax Payable/Receivable</span></span> | <span data-ttu-id="c5721-227">–83</span><span class="sxs-lookup"><span data-stu-id="c5721-227">-83</span></span>                        | <span data-ttu-id="c5721-228">–110,67</span><span class="sxs-lookup"><span data-stu-id="c5721-228">-110.67</span></span>                   | <span data-ttu-id="c5721-229">–83</span><span class="sxs-lookup"><span data-stu-id="c5721-229">-83</span></span>                      |
| <span data-ttu-id="c5721-230">Maksu tasakaalustus</span><span class="sxs-lookup"><span data-stu-id="c5721-230">Tax Settlement</span></span>         | <span data-ttu-id="c5721-231">83</span><span class="sxs-lookup"><span data-stu-id="c5721-231">83</span></span>                         | <span data-ttu-id="c5721-232">110.67</span><span class="sxs-lookup"><span data-stu-id="c5721-232">110.67</span></span>                    | <span data-ttu-id="c5721-233">83</span><span class="sxs-lookup"><span data-stu-id="c5721-233">83</span></span>                       |
| <span data-ttu-id="c5721-234">Realiseeritud kasum/kahjum</span><span class="sxs-lookup"><span data-stu-id="c5721-234">Realized Gain/Loss</span></span>     | <span data-ttu-id="c5721-235">0</span><span class="sxs-lookup"><span data-stu-id="c5721-235">0</span></span>                          | <span data-ttu-id="c5721-236">0.33</span><span class="sxs-lookup"><span data-stu-id="c5721-236">0.33</span></span>                      | <span data-ttu-id="c5721-237">0</span><span class="sxs-lookup"><span data-stu-id="c5721-237">0</span></span>                        |
| <span data-ttu-id="c5721-238">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="c5721-238">Tax Payable/Receivable</span></span> | <span data-ttu-id="c5721-239">0</span><span class="sxs-lookup"><span data-stu-id="c5721-239">0</span></span>                          | <span data-ttu-id="c5721-240">–0,33</span><span class="sxs-lookup"><span data-stu-id="c5721-240">-0.33</span></span>                     | <span data-ttu-id="c5721-241">0</span><span class="sxs-lookup"><span data-stu-id="c5721-241">0</span></span>                        |



<span data-ttu-id="c5721-242">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="c5721-242">For more information, see the following topics:</span></span>

- [<span data-ttu-id="c5721-243">Topeltvaluuta</span><span class="sxs-lookup"><span data-stu-id="c5721-243">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="c5721-244">Käibemaksu ülevaade</span><span class="sxs-lookup"><span data-stu-id="c5721-244">Sales tax overview</span></span>](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]