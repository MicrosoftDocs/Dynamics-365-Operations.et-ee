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
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 9e5db8e4bbd14aa30196e3be617cdfcb72c091fd
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977163"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="af33e-103">Käibemaksu topeltvaluuta tugi</span><span class="sxs-lookup"><span data-stu-id="af33e-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="af33e-104">Selles teemas selgitatakse, kuidas laiendada käibemaksude topeltvaluuta arvestust ja käibemaksu arvutamise, sisestamise ja tasakaalustuste mõju.</span><span class="sxs-lookup"><span data-stu-id="af33e-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="af33e-105">Rakenduse Dynamics 365 Finance topeltvaluuta funktsioon lisati versioonis 8.1 (oktoober 2018).</span><span class="sxs-lookup"><span data-stu-id="af33e-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="af33e-106">See muudab raamatupidamise kirjete aruandevaluutas arvutamise viisi.</span><span class="sxs-lookup"><span data-stu-id="af33e-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="af33e-107">Varasemates versioonides teisendati kanded aruandlusvaluutasse järgmises järjestuses.</span><span class="sxs-lookup"><span data-stu-id="af33e-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="af33e-108">Kande kogusumma arvutati kande valuutas > kande summa teisendati arvestusvaluutaks > arvestusvaluuta summa teisendati aruandlusvaluutaks</span><span class="sxs-lookup"><span data-stu-id="af33e-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="af33e-109">Pärast topeltvaluuta funktsiooni lubamist teisendati kanded aruandlusvaluutasse järgmises järjestuses.</span><span class="sxs-lookup"><span data-stu-id="af33e-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="af33e-110">Kandevaluuta summa > Aruandlusvaluuta summa</span><span class="sxs-lookup"><span data-stu-id="af33e-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="af33e-111">Lisateavet topeltvaluuta kohta vt teemast [Topeltvaluuta](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="af33e-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="af33e-112">Topeltvaluuta toe tulemusena on funktsiooni halduses saadaval kaks uut funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="af33e-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="af33e-113">Käibemaksu teisendamine (väljaanne versioonis 10.0.9)</span><span class="sxs-lookup"><span data-stu-id="af33e-113">Sales tax conversion (Release in version 10.0.9)</span></span>
- <span data-ttu-id="af33e-114">Aruandevaluuta maksu tasakaalustuse automaatne saldo (väljaanne versioonis 10.0.11)</span><span class="sxs-lookup"><span data-stu-id="af33e-114">Tax settlement auto balance in reporting currency (Release in version 10.0.11)</span></span>

<span data-ttu-id="af33e-115">Käibemaksu topeltvaluuta tugi tagab, et maksud arvutatakse maksu valuutas täpselt ja et käibemaksu tasakaalustuse saldo arvutatakse täpselt nii arvestusvaluutas kui ka aruandlusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="af33e-115">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="af33e-116">Käibemaksu teisendamine</span><span class="sxs-lookup"><span data-stu-id="af33e-116">Sales tax conversion</span></span>

<span data-ttu-id="af33e-117">Parameeter **Käibemaksu teisendamine** pakub maksusumma kandevaluutast maksuvaluutasse teisendamiseks kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="af33e-117">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="af33e-118">Arvestusvaluuta: teekond on „Summa kandevaluutas > Summa arvestusvaluutas > Summa maksuvaluutas”.</span><span class="sxs-lookup"><span data-stu-id="af33e-118">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="af33e-119">Valuuta teisendamiseks kasutatakse arvestusvaluuta vahetuskursi tüüpi (konfigureeritud pearaamatu seadistuses).</span><span class="sxs-lookup"><span data-stu-id="af33e-119">The accounting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="af33e-120">Aruandlusvaluuta: teekond on „Summa kandevaluutas > Summa aruandlusvaluutas > Summa maksuvaluutas”.</span><span class="sxs-lookup"><span data-stu-id="af33e-120">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="af33e-121">Valuuta teisendamiseks kasutatakse aruandlusvaluuta vahetuskursi tüüpi (konfigureeritud pearaamatu seadistuses).</span><span class="sxs-lookup"><span data-stu-id="af33e-121">The reporting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="af33e-122">Näide</span><span class="sxs-lookup"><span data-stu-id="af33e-122">Example</span></span>

<span data-ttu-id="af33e-123">Lihtne näide selle funktsiooni demonstreerimiseks on järgmine.</span><span class="sxs-lookup"><span data-stu-id="af33e-123">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="af33e-124">Pearaamatu ja maksu valuuta seadistamine</span><span class="sxs-lookup"><span data-stu-id="af33e-124">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="af33e-125">Kande valuuta</span><span class="sxs-lookup"><span data-stu-id="af33e-125">Transaction currency</span></span> | <span data-ttu-id="af33e-126">Arvestusvaluuta</span><span class="sxs-lookup"><span data-stu-id="af33e-126">Accounting currency</span></span> | <span data-ttu-id="af33e-127">Aruandlusvaluuta</span><span class="sxs-lookup"><span data-stu-id="af33e-127">Reporting currency</span></span> | <span data-ttu-id="af33e-128">Maksuvaluuta</span><span class="sxs-lookup"><span data-stu-id="af33e-128">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="af33e-129"> eurot</span><span class="sxs-lookup"><span data-stu-id="af33e-129">EUR</span></span>                  | <span data-ttu-id="af33e-130">USA dollar</span><span class="sxs-lookup"><span data-stu-id="af33e-130">USD</span></span>                 | <span data-ttu-id="af33e-131">GBP</span><span class="sxs-lookup"><span data-stu-id="af33e-131">GBP</span></span>                | <span data-ttu-id="af33e-132">GBP</span><span class="sxs-lookup"><span data-stu-id="af33e-132">GBP</span></span>          |

<span data-ttu-id="af33e-133">Valuutakurss</span><span class="sxs-lookup"><span data-stu-id="af33e-133">Exchange rate</span></span>

| <span data-ttu-id="af33e-134">Valuutast</span><span class="sxs-lookup"><span data-stu-id="af33e-134">From currency</span></span> | <span data-ttu-id="af33e-135">Valuutaks</span><span class="sxs-lookup"><span data-stu-id="af33e-135">To currency</span></span> | <span data-ttu-id="af33e-136">Tegur</span><span class="sxs-lookup"><span data-stu-id="af33e-136">Factor</span></span> | <span data-ttu-id="af33e-137">Valuutakurss</span><span class="sxs-lookup"><span data-stu-id="af33e-137">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="af33e-138"> eurot</span><span class="sxs-lookup"><span data-stu-id="af33e-138">EUR</span></span>           | <span data-ttu-id="af33e-139">USA dollar</span><span class="sxs-lookup"><span data-stu-id="af33e-139">USD</span></span>         | <span data-ttu-id="af33e-140">1</span><span class="sxs-lookup"><span data-stu-id="af33e-140">1</span></span>      | <span data-ttu-id="af33e-141">1.11</span><span class="sxs-lookup"><span data-stu-id="af33e-141">1.11</span></span>          |
| <span data-ttu-id="af33e-142"> eurot</span><span class="sxs-lookup"><span data-stu-id="af33e-142">EUR</span></span>           | <span data-ttu-id="af33e-143">GBP</span><span class="sxs-lookup"><span data-stu-id="af33e-143">GBP</span></span>         | <span data-ttu-id="af33e-144">1</span><span class="sxs-lookup"><span data-stu-id="af33e-144">1</span></span>      | <span data-ttu-id="af33e-145">0.83</span><span class="sxs-lookup"><span data-stu-id="af33e-145">0.83</span></span>          |
| <span data-ttu-id="af33e-146">USA dollar</span><span class="sxs-lookup"><span data-stu-id="af33e-146">USD</span></span>           | <span data-ttu-id="af33e-147">GBP</span><span class="sxs-lookup"><span data-stu-id="af33e-147">GBP</span></span>         | <span data-ttu-id="af33e-148">1</span><span class="sxs-lookup"><span data-stu-id="af33e-148">1</span></span>      | <span data-ttu-id="af33e-149">0.75</span><span class="sxs-lookup"><span data-stu-id="af33e-149">0.75</span></span>          |

<span data-ttu-id="af33e-150">Maksusumma arvutamine erinevate parameetrite valikutega</span><span class="sxs-lookup"><span data-stu-id="af33e-150">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="af33e-151">Maksusumma = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="af33e-151">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="af33e-152">Käibemaksu teisendamise parameetrid</span><span class="sxs-lookup"><span data-stu-id="af33e-152">Sales tax conversion parameters</span></span> | <span data-ttu-id="af33e-153">Kande valuuta (EUR)</span><span class="sxs-lookup"><span data-stu-id="af33e-153">Transaction currency (EUR)</span></span> | <span data-ttu-id="af33e-154">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="af33e-154">Accounting currency (USD)</span></span> | <span data-ttu-id="af33e-155">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="af33e-155">Reporting currency (GBP)</span></span> | <span data-ttu-id="af33e-156">Maksuvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="af33e-156">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="af33e-157">Arvestusvaluuta</span><span class="sxs-lookup"><span data-stu-id="af33e-157">Accounting currency</span></span>             | <span data-ttu-id="af33e-158">100</span><span class="sxs-lookup"><span data-stu-id="af33e-158">100</span></span>                        | <span data-ttu-id="af33e-159">111</span><span class="sxs-lookup"><span data-stu-id="af33e-159">111</span></span>                       | <span data-ttu-id="af33e-160">83</span><span class="sxs-lookup"><span data-stu-id="af33e-160">83</span></span>                       | <span data-ttu-id="af33e-161">**83.25**</span><span class="sxs-lookup"><span data-stu-id="af33e-161">**83.25**</span></span>          |
| <span data-ttu-id="af33e-162">Aruandlusvaluuta</span><span class="sxs-lookup"><span data-stu-id="af33e-162">Reporting currency</span></span>              | <span data-ttu-id="af33e-163">100</span><span class="sxs-lookup"><span data-stu-id="af33e-163">100</span></span>                        | <span data-ttu-id="af33e-164">111</span><span class="sxs-lookup"><span data-stu-id="af33e-164">111</span></span>                       | <span data-ttu-id="af33e-165">83</span><span class="sxs-lookup"><span data-stu-id="af33e-165">83</span></span>                       | <span data-ttu-id="af33e-166">**83**</span><span class="sxs-lookup"><span data-stu-id="af33e-166">**83**</span></span>             |

<span data-ttu-id="af33e-167">Selle parameetri saab konfigureerida maksuhalduri nõuetelevastavuse nõude alusel.</span><span class="sxs-lookup"><span data-stu-id="af33e-167">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="af33e-168">Täienduse kaalutlus</span><span class="sxs-lookup"><span data-stu-id="af33e-168">Upgrade Consideration</span></span>

<span data-ttu-id="af33e-169">See funktsioon rakendub ainult uutele kannetele.</span><span class="sxs-lookup"><span data-stu-id="af33e-169">This feature will only apply for new transactions.</span></span> <span data-ttu-id="af33e-170">Tabelis TAXTRANS juba salvestatud, kuid veel mitte tasakaalustatud maksukannete puhul ei arvuta süsteem maksu summat maksu valuutas ümber, kuna maksu sisestamise hetke vahetuskurss on juba puudu.</span><span class="sxs-lookup"><span data-stu-id="af33e-170">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="af33e-171">Eelneva stsenaariumi vältimiseks soovitame muuta selle parameetri väärtust uues (puhtas) maksu tasakaalustusperioodil, mis ei sisalda ühtegi tasakaalustamata maksukannet.</span><span class="sxs-lookup"><span data-stu-id="af33e-171">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="af33e-172">Selle väärtuse muutmiseks maksu tasakaalustusperioodi keskel käivitage enne selle parameetri väärtuse muutmist programm „Käibemaksu tasakaalustamine ja sisestamine” praeguse maksu tasakaalustusperioodi jaoks.</span><span class="sxs-lookup"><span data-stu-id="af33e-172">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="af33e-173">Aruandlusvaluuta maksu summa jälgimine</span><span class="sxs-lookup"><span data-stu-id="af33e-173">Track reporting currency tax amount</span></span>

<span data-ttu-id="af33e-174">Aruandlusvaluuta summade jälgimiseks lisati maksudega seotud tabelitesse kolm uut välja.</span><span class="sxs-lookup"><span data-stu-id="af33e-174">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="af33e-175">Need väljad asuvad tabelites TAXUNCOMMITTED ja TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="af33e-175">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="af33e-176">TaxAmountRep: maksusumma aruandlusvaluutas</span><span class="sxs-lookup"><span data-stu-id="af33e-176">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="af33e-177">TaxBaseAmountRep: aruandlusvaluuta baassumma</span><span class="sxs-lookup"><span data-stu-id="af33e-177">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="af33e-178">TaxInCostPriceRep: mahaarvamatu summa aruandlusvaluutas</span><span class="sxs-lookup"><span data-stu-id="af33e-178">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="af33e-179">Ainult tabelis TAXUNCOMMITTED salvestatud maks, mis pole veel postitatud, arvutab süsteem maksu summa postitmise ajal aruandlusvaluutas ümber ja salvestab tabelis TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="af33e-179">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="af33e-180">See väljaanne ei sisalda muudatusi aruannetes ega vormides, mis näitavad maksu summat aruandlusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="af33e-180">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="af33e-181">Aruannete ja vormide muudatused edastatakse tulevases väljaannetes.</span><span class="sxs-lookup"><span data-stu-id="af33e-181">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="af33e-182">Maksu tasakaalustuse automaatne saldo aruandlusvaluutas</span><span class="sxs-lookup"><span data-stu-id="af33e-182">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="af33e-183">Kui maksu tasakaalustamine ei ole aruandlusvaluuta jaoks mingil põhjusel tasakaalus, näiteks müügimaksu teisendustee on „Arvestusvaluuta” või vahetuskurss muutub samal maksu tasakaalustamise perioodil, siis süsteem loob automaatselt raamatupidamise kirjed, et reguleerida maksu summa erinevust ja tasakaalustada seda realiseeritud vahetusega saadud tulu/kulu kontoga, mis on pearaamatu seadistuses konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="af33e-183">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, thebn the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="af33e-184">Kasutades selle funktsiooni demonstreerimiseks eelmist näidet, oletagem, et tabeli TAXTRANS andmed on sisestamise ajal järgmised.</span><span class="sxs-lookup"><span data-stu-id="af33e-184">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="af33e-185">Käibemaksu teisendamise parameetrid</span><span class="sxs-lookup"><span data-stu-id="af33e-185">Sales tax conversion parameters</span></span> | <span data-ttu-id="af33e-186">Kande valuuta (EUR)</span><span class="sxs-lookup"><span data-stu-id="af33e-186">Transaction currency (EUR)</span></span> | <span data-ttu-id="af33e-187">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="af33e-187">Accounting currency (USD)</span></span> | <span data-ttu-id="af33e-188">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="af33e-188">Reporting currency (GBP)</span></span> | <span data-ttu-id="af33e-189">Maksuvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="af33e-189">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="af33e-190">Arvestusvaluuta</span><span class="sxs-lookup"><span data-stu-id="af33e-190">Accounting currency</span></span>             | <span data-ttu-id="af33e-191">100</span><span class="sxs-lookup"><span data-stu-id="af33e-191">100</span></span>                        | <span data-ttu-id="af33e-192">111</span><span class="sxs-lookup"><span data-stu-id="af33e-192">111</span></span>                       | <span data-ttu-id="af33e-193">83</span><span class="sxs-lookup"><span data-stu-id="af33e-193">83</span></span>                       | <span data-ttu-id="af33e-194">**83.25**</span><span class="sxs-lookup"><span data-stu-id="af33e-194">**83.25**</span></span>          |
| <span data-ttu-id="af33e-195">Aruandlusvaluuta</span><span class="sxs-lookup"><span data-stu-id="af33e-195">Reporting currency</span></span>              | <span data-ttu-id="af33e-196">100</span><span class="sxs-lookup"><span data-stu-id="af33e-196">100</span></span>                        | <span data-ttu-id="af33e-197">111</span><span class="sxs-lookup"><span data-stu-id="af33e-197">111</span></span>                       | <span data-ttu-id="af33e-198">83</span><span class="sxs-lookup"><span data-stu-id="af33e-198">83</span></span>                       | <span data-ttu-id="af33e-199">**83**</span><span class="sxs-lookup"><span data-stu-id="af33e-199">**83**</span></span>             |

<span data-ttu-id="af33e-200">Kui käivitate käibemaksu tasakaalustuse programmi kuu lõpus, on raamatupidamise kirje järgmine.</span><span class="sxs-lookup"><span data-stu-id="af33e-200">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="af33e-201">Stsenaarium: müügimaksu teisendamine = „arvestusvaluuta”</span><span class="sxs-lookup"><span data-stu-id="af33e-201">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="af33e-202">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="af33e-202">Main account</span></span>           | <span data-ttu-id="af33e-203">Kande valuuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="af33e-203">Transaction currency (GBP)</span></span> | <span data-ttu-id="af33e-204">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="af33e-204">Accounting currency (USD)</span></span> | <span data-ttu-id="af33e-205">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="af33e-205">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="af33e-206">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="af33e-206">Tax Payable/Receivable</span></span> | <span data-ttu-id="af33e-207">–83,25</span><span class="sxs-lookup"><span data-stu-id="af33e-207">-83.25</span></span>                     | <span data-ttu-id="af33e-208">–111</span><span class="sxs-lookup"><span data-stu-id="af33e-208">-111</span></span>                      | <span data-ttu-id="af33e-209">–83,25</span><span class="sxs-lookup"><span data-stu-id="af33e-209">-83.25</span></span>                   |
| <span data-ttu-id="af33e-210">Maksu tasakaalustus</span><span class="sxs-lookup"><span data-stu-id="af33e-210">Tax Settlement</span></span>         | <span data-ttu-id="af33e-211">83.25</span><span class="sxs-lookup"><span data-stu-id="af33e-211">83.25</span></span>                      | <span data-ttu-id="af33e-212">111</span><span class="sxs-lookup"><span data-stu-id="af33e-212">111</span></span>                       | <span data-ttu-id="af33e-213">83.25</span><span class="sxs-lookup"><span data-stu-id="af33e-213">83.25</span></span>                    |
| <span data-ttu-id="af33e-214">Realiseeritud kasum/kahjum</span><span class="sxs-lookup"><span data-stu-id="af33e-214">Realized Gain/Loss</span></span>     | <span data-ttu-id="af33e-215">0</span><span class="sxs-lookup"><span data-stu-id="af33e-215">0</span></span>                          | <span data-ttu-id="af33e-216">0</span><span class="sxs-lookup"><span data-stu-id="af33e-216">0</span></span>                         | <span data-ttu-id="af33e-217">–0,25</span><span class="sxs-lookup"><span data-stu-id="af33e-217">-0.25</span></span>                    |
| <span data-ttu-id="af33e-218">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="af33e-218">Tax Payable/Receivable</span></span> | <span data-ttu-id="af33e-219">0</span><span class="sxs-lookup"><span data-stu-id="af33e-219">0</span></span>                          | <span data-ttu-id="af33e-220">0</span><span class="sxs-lookup"><span data-stu-id="af33e-220">0</span></span>                         | <span data-ttu-id="af33e-221">0.25</span><span class="sxs-lookup"><span data-stu-id="af33e-221">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="af33e-222">Stsenaarium: müügimaksu teisendamine = „aruandlusvaluuta”</span><span class="sxs-lookup"><span data-stu-id="af33e-222">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="af33e-223">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="af33e-223">Main account</span></span>           | <span data-ttu-id="af33e-224">Kande valuuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="af33e-224">Transaction currency (GBP)</span></span> | <span data-ttu-id="af33e-225">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="af33e-225">Accounting currency (USD)</span></span> | <span data-ttu-id="af33e-226">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="af33e-226">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="af33e-227">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="af33e-227">Tax Payable/Receivable</span></span> | <span data-ttu-id="af33e-228">–83</span><span class="sxs-lookup"><span data-stu-id="af33e-228">-83</span></span>                        | <span data-ttu-id="af33e-229">–110,67</span><span class="sxs-lookup"><span data-stu-id="af33e-229">-110.67</span></span>                   | <span data-ttu-id="af33e-230">–83</span><span class="sxs-lookup"><span data-stu-id="af33e-230">-83</span></span>                      |
| <span data-ttu-id="af33e-231">Maksu tasakaalustus</span><span class="sxs-lookup"><span data-stu-id="af33e-231">Tax Settlement</span></span>         | <span data-ttu-id="af33e-232">83</span><span class="sxs-lookup"><span data-stu-id="af33e-232">83</span></span>                         | <span data-ttu-id="af33e-233">110.67</span><span class="sxs-lookup"><span data-stu-id="af33e-233">110.67</span></span>                    | <span data-ttu-id="af33e-234">83</span><span class="sxs-lookup"><span data-stu-id="af33e-234">83</span></span>                       |
| <span data-ttu-id="af33e-235">Realiseeritud kasum/kahjum</span><span class="sxs-lookup"><span data-stu-id="af33e-235">Realized Gain/Loss</span></span>     | <span data-ttu-id="af33e-236">0</span><span class="sxs-lookup"><span data-stu-id="af33e-236">0</span></span>                          | <span data-ttu-id="af33e-237">0.33</span><span class="sxs-lookup"><span data-stu-id="af33e-237">0.33</span></span>                      | <span data-ttu-id="af33e-238">0</span><span class="sxs-lookup"><span data-stu-id="af33e-238">0</span></span>                        |
| <span data-ttu-id="af33e-239">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="af33e-239">Tax Payable/Receivable</span></span> | <span data-ttu-id="af33e-240">0</span><span class="sxs-lookup"><span data-stu-id="af33e-240">0</span></span>                          | <span data-ttu-id="af33e-241">–0,33</span><span class="sxs-lookup"><span data-stu-id="af33e-241">-0.33</span></span>                     | <span data-ttu-id="af33e-242">0</span><span class="sxs-lookup"><span data-stu-id="af33e-242">0</span></span>                        |



<span data-ttu-id="af33e-243">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="af33e-243">For more information, see the following topics:</span></span>

- [<span data-ttu-id="af33e-244">Topeltvaluuta</span><span class="sxs-lookup"><span data-stu-id="af33e-244">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="af33e-245">Käibemaksu ülevaade</span><span class="sxs-lookup"><span data-stu-id="af33e-245">Sales tax overview</span></span>](indirect-taxes-overview.md)

