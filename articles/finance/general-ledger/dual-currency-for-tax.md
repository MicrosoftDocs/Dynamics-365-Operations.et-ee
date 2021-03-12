---
title: Maksu topeltvaluuta tugi
description: Selles teemas selgitatakse, kuidas laiendada maksudomeenis topeltvaluuta arvestuse funktsiooni ja maksude arvutamise ja sisestamise mõju
author: EricWang
manager: Ann Beebe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 2e3e7ff93ca3c6a2266ba0f33c8eac7ceade0d4d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978592"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="906c4-103">Käibemaksu topeltvaluuta tugi</span><span class="sxs-lookup"><span data-stu-id="906c4-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="906c4-104">Selles teemas selgitatakse, kuidas laiendada käibemaksude topeltvaluuta arvestust ja käibemaksu arvutamise, sisestamise ja tasakaalustuste mõju.</span><span class="sxs-lookup"><span data-stu-id="906c4-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="906c4-105">Rakenduse Dynamics 365 Finance topeltvaluuta funktsioon lisati versioonis 8.1 (oktoober 2018).</span><span class="sxs-lookup"><span data-stu-id="906c4-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="906c4-106">See muudab raamatupidamise kirjete aruandevaluutas arvutamise viisi.</span><span class="sxs-lookup"><span data-stu-id="906c4-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="906c4-107">Varasemates versioonides teisendati kanded aruandlusvaluutasse järgmises järjestuses.</span><span class="sxs-lookup"><span data-stu-id="906c4-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="906c4-108">Kande kogusumma arvutati kande valuutas > kande summa teisendati arvestusvaluutaks > arvestusvaluuta summa teisendati aruandlusvaluutaks</span><span class="sxs-lookup"><span data-stu-id="906c4-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="906c4-109">Pärast topeltvaluuta funktsiooni lubamist teisendati kanded aruandlusvaluutasse järgmises järjestuses.</span><span class="sxs-lookup"><span data-stu-id="906c4-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="906c4-110">Kandevaluuta summa > Aruandlusvaluuta summa</span><span class="sxs-lookup"><span data-stu-id="906c4-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="906c4-111">Lisateavet topeltvaluuta kohta vt teemast [Topeltvaluuta](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="906c4-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="906c4-112">Topeltvaluuta toe tulemusena on funktsiooni halduses saadaval kaks uut funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="906c4-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="906c4-113">Käibemaksu konverteerimine (uus versioonis 10.0.13)</span><span class="sxs-lookup"><span data-stu-id="906c4-113">Sales tax conversion (new in version 10.0.13)</span></span>

<span data-ttu-id="906c4-114">Käibemaksu topeltvaluuta tugi tagab, et maksud arvutatakse maksu valuutas täpselt ja et käibemaksu tasakaalustuse saldo arvutatakse täpselt nii arvestusvaluutas kui ka aruandlusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="906c4-114">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="906c4-115">Käibemaksu teisendamine</span><span class="sxs-lookup"><span data-stu-id="906c4-115">Sales tax conversion</span></span>

<span data-ttu-id="906c4-116">Parameeter **Käibemaksu teisendamine** pakub maksusumma kandevaluutast maksuvaluutasse teisendamiseks kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="906c4-116">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="906c4-117">Arvestusvaluuta: teekond on „Summa kandevaluutas > Summa arvestusvaluutas > Summa maksuvaluutas”.</span><span class="sxs-lookup"><span data-stu-id="906c4-117">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="906c4-118">Valuuta konverteerimiseks kasutatakse arvestusvaluuta vahetuskursi tüüpi (konfigureeritud pearaamatu seadistuses).</span><span class="sxs-lookup"><span data-stu-id="906c4-118">The accounting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="906c4-119">Aruandlusvaluuta: teekond on „Summa kandevaluutas > Summa aruandlusvaluutas > Summa maksuvaluutas”.</span><span class="sxs-lookup"><span data-stu-id="906c4-119">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="906c4-120">Valuuta konverteerimiseks kasutatakse aruandlusvaluuta vahetuskursi tüüpi (konfigureeritud pearaamatu seadistuses).</span><span class="sxs-lookup"><span data-stu-id="906c4-120">The reporting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="906c4-121">Näide</span><span class="sxs-lookup"><span data-stu-id="906c4-121">Example</span></span>

<span data-ttu-id="906c4-122">Lihtne näide selle funktsiooni demonstreerimiseks on järgmine.</span><span class="sxs-lookup"><span data-stu-id="906c4-122">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="906c4-123">Pearaamatu ja maksu valuuta seadistamine</span><span class="sxs-lookup"><span data-stu-id="906c4-123">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="906c4-124">Kande valuuta</span><span class="sxs-lookup"><span data-stu-id="906c4-124">Transaction currency</span></span> | <span data-ttu-id="906c4-125">Arvestusvaluuta</span><span class="sxs-lookup"><span data-stu-id="906c4-125">Accounting currency</span></span> | <span data-ttu-id="906c4-126">Aruandlusvaluuta</span><span class="sxs-lookup"><span data-stu-id="906c4-126">Reporting currency</span></span> | <span data-ttu-id="906c4-127">Maksuvaluuta</span><span class="sxs-lookup"><span data-stu-id="906c4-127">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="906c4-128"> eurot</span><span class="sxs-lookup"><span data-stu-id="906c4-128">EUR</span></span>                  | <span data-ttu-id="906c4-129">USA dollar</span><span class="sxs-lookup"><span data-stu-id="906c4-129">USD</span></span>                 | <span data-ttu-id="906c4-130">GBP</span><span class="sxs-lookup"><span data-stu-id="906c4-130">GBP</span></span>                | <span data-ttu-id="906c4-131">GBP</span><span class="sxs-lookup"><span data-stu-id="906c4-131">GBP</span></span>          |

<span data-ttu-id="906c4-132">Valuutakurss</span><span class="sxs-lookup"><span data-stu-id="906c4-132">Exchange rate</span></span>

| <span data-ttu-id="906c4-133">Valuutast</span><span class="sxs-lookup"><span data-stu-id="906c4-133">From currency</span></span> | <span data-ttu-id="906c4-134">Valuutaks</span><span class="sxs-lookup"><span data-stu-id="906c4-134">To currency</span></span> | <span data-ttu-id="906c4-135">Tegur</span><span class="sxs-lookup"><span data-stu-id="906c4-135">Factor</span></span> | <span data-ttu-id="906c4-136">Valuutakurss</span><span class="sxs-lookup"><span data-stu-id="906c4-136">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="906c4-137"> eurot</span><span class="sxs-lookup"><span data-stu-id="906c4-137">EUR</span></span>           | <span data-ttu-id="906c4-138">USA dollar</span><span class="sxs-lookup"><span data-stu-id="906c4-138">USD</span></span>         | <span data-ttu-id="906c4-139">1</span><span class="sxs-lookup"><span data-stu-id="906c4-139">1</span></span>      | <span data-ttu-id="906c4-140">1.11</span><span class="sxs-lookup"><span data-stu-id="906c4-140">1.11</span></span>          |
| <span data-ttu-id="906c4-141"> eurot</span><span class="sxs-lookup"><span data-stu-id="906c4-141">EUR</span></span>           | <span data-ttu-id="906c4-142">GBP</span><span class="sxs-lookup"><span data-stu-id="906c4-142">GBP</span></span>         | <span data-ttu-id="906c4-143">1</span><span class="sxs-lookup"><span data-stu-id="906c4-143">1</span></span>      | <span data-ttu-id="906c4-144">0.83</span><span class="sxs-lookup"><span data-stu-id="906c4-144">0.83</span></span>          |
| <span data-ttu-id="906c4-145">USA dollar</span><span class="sxs-lookup"><span data-stu-id="906c4-145">USD</span></span>           | <span data-ttu-id="906c4-146">GBP</span><span class="sxs-lookup"><span data-stu-id="906c4-146">GBP</span></span>         | <span data-ttu-id="906c4-147">1</span><span class="sxs-lookup"><span data-stu-id="906c4-147">1</span></span>      | <span data-ttu-id="906c4-148">0.75</span><span class="sxs-lookup"><span data-stu-id="906c4-148">0.75</span></span>          |

<span data-ttu-id="906c4-149">Maksusumma arvutamine erinevate parameetrite valikutega</span><span class="sxs-lookup"><span data-stu-id="906c4-149">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="906c4-150">Maksusumma = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="906c4-150">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="906c4-151">Käibemaksu teisendamise parameetrid</span><span class="sxs-lookup"><span data-stu-id="906c4-151">Sales tax conversion parameters</span></span> | <span data-ttu-id="906c4-152">Kande valuuta (EUR)</span><span class="sxs-lookup"><span data-stu-id="906c4-152">Transaction currency (EUR)</span></span> | <span data-ttu-id="906c4-153">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="906c4-153">Accounting currency (USD)</span></span> | <span data-ttu-id="906c4-154">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="906c4-154">Reporting currency (GBP)</span></span> | <span data-ttu-id="906c4-155">Maksuvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="906c4-155">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="906c4-156">Arvestusvaluuta</span><span class="sxs-lookup"><span data-stu-id="906c4-156">Accounting currency</span></span>             | <span data-ttu-id="906c4-157">100</span><span class="sxs-lookup"><span data-stu-id="906c4-157">100</span></span>                        | <span data-ttu-id="906c4-158">111</span><span class="sxs-lookup"><span data-stu-id="906c4-158">111</span></span>                       | <span data-ttu-id="906c4-159">83</span><span class="sxs-lookup"><span data-stu-id="906c4-159">83</span></span>                       | <span data-ttu-id="906c4-160">**83.25**</span><span class="sxs-lookup"><span data-stu-id="906c4-160">**83.25**</span></span>          |
| <span data-ttu-id="906c4-161">Aruandlusvaluuta</span><span class="sxs-lookup"><span data-stu-id="906c4-161">Reporting currency</span></span>              | <span data-ttu-id="906c4-162">100</span><span class="sxs-lookup"><span data-stu-id="906c4-162">100</span></span>                        | <span data-ttu-id="906c4-163">111</span><span class="sxs-lookup"><span data-stu-id="906c4-163">111</span></span>                       | <span data-ttu-id="906c4-164">83</span><span class="sxs-lookup"><span data-stu-id="906c4-164">83</span></span>                       | <span data-ttu-id="906c4-165">**83**</span><span class="sxs-lookup"><span data-stu-id="906c4-165">**83**</span></span>             |

<span data-ttu-id="906c4-166">Selle parameetri saab konfigureerida maksuhalduri nõuetelevastavuse nõude alusel.</span><span class="sxs-lookup"><span data-stu-id="906c4-166">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="906c4-167">Täienduse kaalutlus</span><span class="sxs-lookup"><span data-stu-id="906c4-167">Upgrade Consideration</span></span>

<span data-ttu-id="906c4-168">See funktsioon rakendub ainult uutele kannetele.</span><span class="sxs-lookup"><span data-stu-id="906c4-168">This feature will only apply for new transactions.</span></span> <span data-ttu-id="906c4-169">Tabelis TAXTRANS juba salvestatud, kuid veel mitte tasakaalustatud maksukannete puhul ei arvuta süsteem maksu summat maksu valuutas ümber, kuna maksu sisestamise hetke vahetuskurss on juba puudu.</span><span class="sxs-lookup"><span data-stu-id="906c4-169">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="906c4-170">Eelneva stsenaariumi vältimiseks soovitame muuta selle parameetri väärtust uues (puhtas) maksu tasakaalustusperioodil, mis ei sisalda ühtegi tasakaalustamata maksukannet.</span><span class="sxs-lookup"><span data-stu-id="906c4-170">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="906c4-171">Selle väärtuse muutmiseks maksu tasakaalustusperioodi keskel käivitage enne selle parameetri väärtuse muutmist programm „Käibemaksu tasakaalustamine ja sisestamine” praeguse maksu tasakaalustusperioodi jaoks.</span><span class="sxs-lookup"><span data-stu-id="906c4-171">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="906c4-172">Aruandlusvaluuta maksu summa jälgimine</span><span class="sxs-lookup"><span data-stu-id="906c4-172">Track reporting currency tax amount</span></span>

<span data-ttu-id="906c4-173">Aruandlusvaluuta summade jälgimiseks lisati maksudega seotud tabelitesse kolm uut välja.</span><span class="sxs-lookup"><span data-stu-id="906c4-173">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="906c4-174">Need väljad asuvad tabelites TAXUNCOMMITTED ja TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="906c4-174">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="906c4-175">TaxAmountRep: maksusumma aruandlusvaluutas</span><span class="sxs-lookup"><span data-stu-id="906c4-175">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="906c4-176">TaxBaseAmountRep: aruandlusvaluuta baassumma</span><span class="sxs-lookup"><span data-stu-id="906c4-176">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="906c4-177">TaxInCostPriceRep: mahaarvamatu summa aruandlusvaluutas</span><span class="sxs-lookup"><span data-stu-id="906c4-177">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="906c4-178">Ainult tabelis TAXUNCOMMITTED salvestatud maks, mis pole veel postitatud, arvutab süsteem maksu summa postitmise ajal aruandlusvaluutas ümber ja salvestab tabelis TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="906c4-178">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="906c4-179">See väljaanne ei sisalda muudatusi aruannetes ega vormides, mis näitavad maksu summat aruandlusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="906c4-179">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="906c4-180">Aruannete ja vormide muudatused edastatakse tulevases väljaannetes.</span><span class="sxs-lookup"><span data-stu-id="906c4-180">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="906c4-181">Maksu tasakaalustuse automaatne saldo aruandlusvaluutas</span><span class="sxs-lookup"><span data-stu-id="906c4-181">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="906c4-182">Kui maksu tasakaalustamine ei ole aruandlusvaluuta jaoks mingil põhjusel tasakaalus, näiteks müügimaksu teisendustee on „Arvestusvaluuta” või vahetuskurss muutub samal maksu tasakaalustamise perioodil, siis süsteem loob automaatselt raamatupidamise kirjed, et reguleerida maksu summa erinevust ja tasakaalustada seda realiseeritud vahetusega saadud tulu/kulu kontoga, mis on pearaamatu seadistuses konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="906c4-182">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, then the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="906c4-183">Kasutades selle funktsiooni demonstreerimiseks eelmist näidet, oletagem, et tabeli TAXTRANS andmed on sisestamise ajal järgmised.</span><span class="sxs-lookup"><span data-stu-id="906c4-183">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="906c4-184">Käibemaksu teisendamise parameetrid</span><span class="sxs-lookup"><span data-stu-id="906c4-184">Sales tax conversion parameters</span></span> | <span data-ttu-id="906c4-185">Kande valuuta (EUR)</span><span class="sxs-lookup"><span data-stu-id="906c4-185">Transaction currency (EUR)</span></span> | <span data-ttu-id="906c4-186">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="906c4-186">Accounting currency (USD)</span></span> | <span data-ttu-id="906c4-187">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="906c4-187">Reporting currency (GBP)</span></span> | <span data-ttu-id="906c4-188">Maksuvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="906c4-188">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="906c4-189">Arvestusvaluuta</span><span class="sxs-lookup"><span data-stu-id="906c4-189">Accounting currency</span></span>             | <span data-ttu-id="906c4-190">100</span><span class="sxs-lookup"><span data-stu-id="906c4-190">100</span></span>                        | <span data-ttu-id="906c4-191">111</span><span class="sxs-lookup"><span data-stu-id="906c4-191">111</span></span>                       | <span data-ttu-id="906c4-192">83</span><span class="sxs-lookup"><span data-stu-id="906c4-192">83</span></span>                       | <span data-ttu-id="906c4-193">**83.25**</span><span class="sxs-lookup"><span data-stu-id="906c4-193">**83.25**</span></span>          |
| <span data-ttu-id="906c4-194">Aruandlusvaluuta</span><span class="sxs-lookup"><span data-stu-id="906c4-194">Reporting currency</span></span>              | <span data-ttu-id="906c4-195">100</span><span class="sxs-lookup"><span data-stu-id="906c4-195">100</span></span>                        | <span data-ttu-id="906c4-196">111</span><span class="sxs-lookup"><span data-stu-id="906c4-196">111</span></span>                       | <span data-ttu-id="906c4-197">83</span><span class="sxs-lookup"><span data-stu-id="906c4-197">83</span></span>                       | <span data-ttu-id="906c4-198">**83**</span><span class="sxs-lookup"><span data-stu-id="906c4-198">**83**</span></span>             |

<span data-ttu-id="906c4-199">Kui käivitate käibemaksu tasakaalustuse programmi kuu lõpus, on raamatupidamise kirje järgmine.</span><span class="sxs-lookup"><span data-stu-id="906c4-199">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="906c4-200">Stsenaarium: müügimaksu teisendamine = „arvestusvaluuta”</span><span class="sxs-lookup"><span data-stu-id="906c4-200">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="906c4-201">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="906c4-201">Main account</span></span>           | <span data-ttu-id="906c4-202">Kande valuuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="906c4-202">Transaction currency (GBP)</span></span> | <span data-ttu-id="906c4-203">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="906c4-203">Accounting currency (USD)</span></span> | <span data-ttu-id="906c4-204">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="906c4-204">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="906c4-205">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="906c4-205">Tax Payable/Receivable</span></span> | <span data-ttu-id="906c4-206">–83,25</span><span class="sxs-lookup"><span data-stu-id="906c4-206">-83.25</span></span>                     | <span data-ttu-id="906c4-207">–111</span><span class="sxs-lookup"><span data-stu-id="906c4-207">-111</span></span>                      | <span data-ttu-id="906c4-208">–83,25</span><span class="sxs-lookup"><span data-stu-id="906c4-208">-83.25</span></span>                   |
| <span data-ttu-id="906c4-209">Maksu tasakaalustus</span><span class="sxs-lookup"><span data-stu-id="906c4-209">Tax Settlement</span></span>         | <span data-ttu-id="906c4-210">83.25</span><span class="sxs-lookup"><span data-stu-id="906c4-210">83.25</span></span>                      | <span data-ttu-id="906c4-211">111</span><span class="sxs-lookup"><span data-stu-id="906c4-211">111</span></span>                       | <span data-ttu-id="906c4-212">83.25</span><span class="sxs-lookup"><span data-stu-id="906c4-212">83.25</span></span>                    |
| <span data-ttu-id="906c4-213">Realiseeritud kasum/kahjum</span><span class="sxs-lookup"><span data-stu-id="906c4-213">Realized Gain/Loss</span></span>     | <span data-ttu-id="906c4-214">0</span><span class="sxs-lookup"><span data-stu-id="906c4-214">0</span></span>                          | <span data-ttu-id="906c4-215">0</span><span class="sxs-lookup"><span data-stu-id="906c4-215">0</span></span>                         | <span data-ttu-id="906c4-216">–0,25</span><span class="sxs-lookup"><span data-stu-id="906c4-216">-0.25</span></span>                    |
| <span data-ttu-id="906c4-217">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="906c4-217">Tax Payable/Receivable</span></span> | <span data-ttu-id="906c4-218">0</span><span class="sxs-lookup"><span data-stu-id="906c4-218">0</span></span>                          | <span data-ttu-id="906c4-219">0</span><span class="sxs-lookup"><span data-stu-id="906c4-219">0</span></span>                         | <span data-ttu-id="906c4-220">0.25</span><span class="sxs-lookup"><span data-stu-id="906c4-220">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="906c4-221">Stsenaarium: müügimaksu teisendamine = „aruandlusvaluuta”</span><span class="sxs-lookup"><span data-stu-id="906c4-221">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="906c4-222">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="906c4-222">Main account</span></span>           | <span data-ttu-id="906c4-223">Kande valuuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="906c4-223">Transaction currency (GBP)</span></span> | <span data-ttu-id="906c4-224">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="906c4-224">Accounting currency (USD)</span></span> | <span data-ttu-id="906c4-225">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="906c4-225">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="906c4-226">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="906c4-226">Tax Payable/Receivable</span></span> | <span data-ttu-id="906c4-227">–83</span><span class="sxs-lookup"><span data-stu-id="906c4-227">-83</span></span>                        | <span data-ttu-id="906c4-228">–110,67</span><span class="sxs-lookup"><span data-stu-id="906c4-228">-110.67</span></span>                   | <span data-ttu-id="906c4-229">–83</span><span class="sxs-lookup"><span data-stu-id="906c4-229">-83</span></span>                      |
| <span data-ttu-id="906c4-230">Maksu tasakaalustus</span><span class="sxs-lookup"><span data-stu-id="906c4-230">Tax Settlement</span></span>         | <span data-ttu-id="906c4-231">83</span><span class="sxs-lookup"><span data-stu-id="906c4-231">83</span></span>                         | <span data-ttu-id="906c4-232">110.67</span><span class="sxs-lookup"><span data-stu-id="906c4-232">110.67</span></span>                    | <span data-ttu-id="906c4-233">83</span><span class="sxs-lookup"><span data-stu-id="906c4-233">83</span></span>                       |
| <span data-ttu-id="906c4-234">Realiseeritud kasum/kahjum</span><span class="sxs-lookup"><span data-stu-id="906c4-234">Realized Gain/Loss</span></span>     | <span data-ttu-id="906c4-235">0</span><span class="sxs-lookup"><span data-stu-id="906c4-235">0</span></span>                          | <span data-ttu-id="906c4-236">0.33</span><span class="sxs-lookup"><span data-stu-id="906c4-236">0.33</span></span>                      | <span data-ttu-id="906c4-237">0</span><span class="sxs-lookup"><span data-stu-id="906c4-237">0</span></span>                        |
| <span data-ttu-id="906c4-238">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="906c4-238">Tax Payable/Receivable</span></span> | <span data-ttu-id="906c4-239">0</span><span class="sxs-lookup"><span data-stu-id="906c4-239">0</span></span>                          | <span data-ttu-id="906c4-240">–0,33</span><span class="sxs-lookup"><span data-stu-id="906c4-240">-0.33</span></span>                     | <span data-ttu-id="906c4-241">0</span><span class="sxs-lookup"><span data-stu-id="906c4-241">0</span></span>                        |



<span data-ttu-id="906c4-242">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="906c4-242">For more information, see the following topics:</span></span>

- [<span data-ttu-id="906c4-243">Topeltvaluuta</span><span class="sxs-lookup"><span data-stu-id="906c4-243">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="906c4-244">Käibemaksu ülevaade</span><span class="sxs-lookup"><span data-stu-id="906c4-244">Sales tax overview</span></span>](indirect-taxes-overview.md)

