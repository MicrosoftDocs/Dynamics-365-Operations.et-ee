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
ms.openlocfilehash: 1ba4d09240888f0c533fb07614e75ffecea0742c
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124089"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="a76e0-103">Käibemaksu topeltvaluuta tugi</span><span class="sxs-lookup"><span data-stu-id="a76e0-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="a76e0-104">Selles teemas selgitatakse, kuidas laiendada käibemaksude topeltvaluuta arvestust ja käibemaksu arvutamise, sisestamise ja tasakaalustuste mõju.</span><span class="sxs-lookup"><span data-stu-id="a76e0-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="a76e0-105">Rakenduse Dynamics 365 Finance topeltvaluuta funktsioon lisati versioonis 8.1 (oktoober 2018).</span><span class="sxs-lookup"><span data-stu-id="a76e0-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="a76e0-106">See muudab raamatupidamise kirjete aruandevaluutas arvutamise viisi.</span><span class="sxs-lookup"><span data-stu-id="a76e0-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="a76e0-107">Varasemates versioonides teisendati kanded aruandlusvaluutasse järgmises järjestuses.</span><span class="sxs-lookup"><span data-stu-id="a76e0-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

<span data-ttu-id="a76e0-108">Kande kogusumma arvutati kande valuutas > kande summa teisendati arvestusvaluutaks > arvestusvaluuta summa teisendati aruandlusvaluutaks</span><span class="sxs-lookup"><span data-stu-id="a76e0-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="a76e0-109">Pärast topeltvaluuta funktsiooni lubamist teisendati kanded aruandlusvaluutasse järgmises järjestuses.</span><span class="sxs-lookup"><span data-stu-id="a76e0-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="a76e0-110">Kandevaluuta summa > Aruandlusvaluuta summa</span><span class="sxs-lookup"><span data-stu-id="a76e0-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="a76e0-111">Lisateavet topeltvaluuta kohta vt teemast [Topeltvaluuta](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="a76e0-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="a76e0-112">Topeltvaluuta toe tulemusena on funktsiooni halduses saadaval kaks uut funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="a76e0-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="a76e0-113">Käibemaksu teisendamine (väljaanne versioonis 10.0.9)</span><span class="sxs-lookup"><span data-stu-id="a76e0-113">Sales tax conversion (Release in version 10.0.9)</span></span>
- <span data-ttu-id="a76e0-114">Aruandevaluuta maksu tasakaalustuse automaatne saldo (väljaanne versioonis 10.0.11)</span><span class="sxs-lookup"><span data-stu-id="a76e0-114">Tax settlement auto balance in reporting currency (Release in version 10.0.11)</span></span>

<span data-ttu-id="a76e0-115">Käibemaksu topeltvaluuta tugi tagab, et maksud arvutatakse maksu valuutas täpselt ja et käibemaksu tasakaalustuse saldo arvutatakse täpselt nii arvestusvaluutas kui ka aruandlusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="a76e0-115">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

<span data-ttu-id="a76e0-116">Uued funktsioonid on praegu lubatud privaatse eelvaate klientidele.</span><span class="sxs-lookup"><span data-stu-id="a76e0-116">The new features are currently enabled for private preview customers.</span></span> <span data-ttu-id="a76e0-117">Funktsioonide lubamiseks tõstatage vastavate kanalite kaudu Microsoftile hooldustaotlus.</span><span class="sxs-lookup"><span data-stu-id="a76e0-117">To enable the features, raise a service request through corresponding channels to Microsoft.</span></span>

## <a name="sales-tax-conversion"></a><span data-ttu-id="a76e0-118">Käibemaksu teisendamine</span><span class="sxs-lookup"><span data-stu-id="a76e0-118">Sales tax conversion</span></span>

<span data-ttu-id="a76e0-119">Parameeter **Käibemaksu teisendamine** pakub maksusumma kandevaluutast maksuvaluutasse teisendamiseks kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="a76e0-119">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="a76e0-120">Arvestusvaluuta: teekond on „Summa kandevaluutas > Summa arvestusvaluutas > Summa maksuvaluutas”.</span><span class="sxs-lookup"><span data-stu-id="a76e0-120">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="a76e0-121">Valuuta teisendamiseks kasutatakse arvestusvaluuta vahetuskursi tüüpi (konfigureeritud pearaamatu seadistuses).</span><span class="sxs-lookup"><span data-stu-id="a76e0-121">The accounting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="a76e0-122">Aruandlusvaluuta: teekond on „Summa kandevaluutas > Summa aruandlusvaluutas > Summa maksuvaluutas”.</span><span class="sxs-lookup"><span data-stu-id="a76e0-122">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="a76e0-123">Valuuta teisendamiseks kasutatakse aruandlusvaluuta vahetuskursi tüüpi (konfigureeritud pearaamatu seadistuses).</span><span class="sxs-lookup"><span data-stu-id="a76e0-123">The reporting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="a76e0-124">Näide</span><span class="sxs-lookup"><span data-stu-id="a76e0-124">Example</span></span>

<span data-ttu-id="a76e0-125">Lihtne näide selle funktsiooni demonstreerimiseks on järgmine.</span><span class="sxs-lookup"><span data-stu-id="a76e0-125">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="a76e0-126">Pearaamatu ja maksu valuuta seadistamine</span><span class="sxs-lookup"><span data-stu-id="a76e0-126">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="a76e0-127">Kande valuuta</span><span class="sxs-lookup"><span data-stu-id="a76e0-127">Transaction currency</span></span> | <span data-ttu-id="a76e0-128">Arvestusvaluuta</span><span class="sxs-lookup"><span data-stu-id="a76e0-128">Accounting currency</span></span> | <span data-ttu-id="a76e0-129">Aruandlusvaluuta</span><span class="sxs-lookup"><span data-stu-id="a76e0-129">Reporting currency</span></span> | <span data-ttu-id="a76e0-130">Maksuvaluuta</span><span class="sxs-lookup"><span data-stu-id="a76e0-130">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="a76e0-131"> eurot</span><span class="sxs-lookup"><span data-stu-id="a76e0-131">EUR</span></span>                  | <span data-ttu-id="a76e0-132">USA dollar</span><span class="sxs-lookup"><span data-stu-id="a76e0-132">USD</span></span>                 | <span data-ttu-id="a76e0-133">GBP</span><span class="sxs-lookup"><span data-stu-id="a76e0-133">GBP</span></span>                | <span data-ttu-id="a76e0-134">GBP</span><span class="sxs-lookup"><span data-stu-id="a76e0-134">GBP</span></span>          |

<span data-ttu-id="a76e0-135">Valuutakurss</span><span class="sxs-lookup"><span data-stu-id="a76e0-135">Exchange rate</span></span>

| <span data-ttu-id="a76e0-136">Valuutast</span><span class="sxs-lookup"><span data-stu-id="a76e0-136">From currency</span></span> | <span data-ttu-id="a76e0-137">Valuutaks</span><span class="sxs-lookup"><span data-stu-id="a76e0-137">To currency</span></span> | <span data-ttu-id="a76e0-138">Tegur</span><span class="sxs-lookup"><span data-stu-id="a76e0-138">Factor</span></span> | <span data-ttu-id="a76e0-139">Valuutakurss</span><span class="sxs-lookup"><span data-stu-id="a76e0-139">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="a76e0-140"> eurot</span><span class="sxs-lookup"><span data-stu-id="a76e0-140">EUR</span></span>           | <span data-ttu-id="a76e0-141">USA dollar</span><span class="sxs-lookup"><span data-stu-id="a76e0-141">USD</span></span>         | <span data-ttu-id="a76e0-142">1</span><span class="sxs-lookup"><span data-stu-id="a76e0-142">1</span></span>      | <span data-ttu-id="a76e0-143">1.11</span><span class="sxs-lookup"><span data-stu-id="a76e0-143">1.11</span></span>          |
| <span data-ttu-id="a76e0-144"> eurot</span><span class="sxs-lookup"><span data-stu-id="a76e0-144">EUR</span></span>           | <span data-ttu-id="a76e0-145">GBP</span><span class="sxs-lookup"><span data-stu-id="a76e0-145">GBP</span></span>         | <span data-ttu-id="a76e0-146">1</span><span class="sxs-lookup"><span data-stu-id="a76e0-146">1</span></span>      | <span data-ttu-id="a76e0-147">0.83</span><span class="sxs-lookup"><span data-stu-id="a76e0-147">0.83</span></span>          |
| <span data-ttu-id="a76e0-148">USA dollar</span><span class="sxs-lookup"><span data-stu-id="a76e0-148">USD</span></span>           | <span data-ttu-id="a76e0-149">GBP</span><span class="sxs-lookup"><span data-stu-id="a76e0-149">GBP</span></span>         | <span data-ttu-id="a76e0-150">1</span><span class="sxs-lookup"><span data-stu-id="a76e0-150">1</span></span>      | <span data-ttu-id="a76e0-151">0.75</span><span class="sxs-lookup"><span data-stu-id="a76e0-151">0.75</span></span>          |

<span data-ttu-id="a76e0-152">Maksusumma arvutamine erinevate parameetrite valikutega</span><span class="sxs-lookup"><span data-stu-id="a76e0-152">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="a76e0-153">Maksusumma = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="a76e0-153">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="a76e0-154">Käibemaksu teisendamise parameetrid</span><span class="sxs-lookup"><span data-stu-id="a76e0-154">Sales tax conversion parameters</span></span> | <span data-ttu-id="a76e0-155">Kande valuuta (EUR)</span><span class="sxs-lookup"><span data-stu-id="a76e0-155">Transaction currency (EUR)</span></span> | <span data-ttu-id="a76e0-156">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="a76e0-156">Accounting currency (USD)</span></span> | <span data-ttu-id="a76e0-157">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="a76e0-157">Reporting currency (GBP)</span></span> | <span data-ttu-id="a76e0-158">Maksuvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="a76e0-158">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="a76e0-159">Arvestusvaluuta</span><span class="sxs-lookup"><span data-stu-id="a76e0-159">Accounting currency</span></span>             | <span data-ttu-id="a76e0-160">100</span><span class="sxs-lookup"><span data-stu-id="a76e0-160">100</span></span>                        | <span data-ttu-id="a76e0-161">111</span><span class="sxs-lookup"><span data-stu-id="a76e0-161">111</span></span>                       | <span data-ttu-id="a76e0-162">83</span><span class="sxs-lookup"><span data-stu-id="a76e0-162">83</span></span>                       | <span data-ttu-id="a76e0-163">**83.25**</span><span class="sxs-lookup"><span data-stu-id="a76e0-163">**83.25**</span></span>          |
| <span data-ttu-id="a76e0-164">Aruandlusvaluuta</span><span class="sxs-lookup"><span data-stu-id="a76e0-164">Reporting currency</span></span>              | <span data-ttu-id="a76e0-165">100</span><span class="sxs-lookup"><span data-stu-id="a76e0-165">100</span></span>                        | <span data-ttu-id="a76e0-166">111</span><span class="sxs-lookup"><span data-stu-id="a76e0-166">111</span></span>                       | <span data-ttu-id="a76e0-167">83</span><span class="sxs-lookup"><span data-stu-id="a76e0-167">83</span></span>                       | <span data-ttu-id="a76e0-168">**83**</span><span class="sxs-lookup"><span data-stu-id="a76e0-168">**83**</span></span>             |

<span data-ttu-id="a76e0-169">Selle parameetri saab konfigureerida maksuhalduri nõuetelevastavuse nõude alusel.</span><span class="sxs-lookup"><span data-stu-id="a76e0-169">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="a76e0-170">Täienduse kaalutlus</span><span class="sxs-lookup"><span data-stu-id="a76e0-170">Upgrade Consideration</span></span>

<span data-ttu-id="a76e0-171">See funktsioon rakendub ainult uutele kannetele.</span><span class="sxs-lookup"><span data-stu-id="a76e0-171">This feature will only apply for new transactions.</span></span> <span data-ttu-id="a76e0-172">Tabelis TAXTRANS juba salvestatud, kuid veel mitte tasakaalustatud maksukannete puhul ei arvuta süsteem maksu summat maksu valuutas ümber, kuna maksu sisestamise hetke vahetuskurss on juba puudu.</span><span class="sxs-lookup"><span data-stu-id="a76e0-172">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="a76e0-173">Eelneva stsenaariumi vältimiseks soovitame muuta selle parameetri väärtust uues (puhtas) maksu tasakaalustusperioodil, mis ei sisalda ühtegi tasakaalustamata maksukannet.</span><span class="sxs-lookup"><span data-stu-id="a76e0-173">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="a76e0-174">Selle väärtuse muutmiseks maksu tasakaalustusperioodi keskel käivitage enne selle parameetri väärtuse muutmist programm „Käibemaksu tasakaalustamine ja sisestamine” praeguse maksu tasakaalustusperioodi jaoks.</span><span class="sxs-lookup"><span data-stu-id="a76e0-174">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="a76e0-175">Aruandlusvaluuta maksu summa jälgimine</span><span class="sxs-lookup"><span data-stu-id="a76e0-175">Track reporting currency tax amount</span></span>

<span data-ttu-id="a76e0-176">Aruandlusvaluuta summade jälgimiseks lisati maksudega seotud tabelitesse kolm uut välja.</span><span class="sxs-lookup"><span data-stu-id="a76e0-176">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="a76e0-177">Need väljad asuvad tabelites TAXUNCOMMITTED ja TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="a76e0-177">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="a76e0-178">TaxAmountRep: maksusumma aruandlusvaluutas</span><span class="sxs-lookup"><span data-stu-id="a76e0-178">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="a76e0-179">TaxBaseAmountRep: aruandlusvaluuta baassumma</span><span class="sxs-lookup"><span data-stu-id="a76e0-179">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="a76e0-180">TaxInCostPriceRep: mahaarvamatu summa aruandlusvaluutas</span><span class="sxs-lookup"><span data-stu-id="a76e0-180">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="a76e0-181">Ainult tabelis TAXUNCOMMITTED salvestatud maks, mis pole veel postitatud, arvutab süsteem maksu summa postitmise ajal aruandlusvaluutas ümber ja salvestab tabelis TAXTRANS.</span><span class="sxs-lookup"><span data-stu-id="a76e0-181">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="a76e0-182">See väljaanne ei sisalda muudatusi aruannetes ega vormides, mis näitavad maksu summat aruandlusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="a76e0-182">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="a76e0-183">Aruannete ja vormide muudatused edastatakse tulevases väljaannetes.</span><span class="sxs-lookup"><span data-stu-id="a76e0-183">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="a76e0-184">Maksu tasakaalustuse automaatne saldo aruandlusvaluutas</span><span class="sxs-lookup"><span data-stu-id="a76e0-184">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="a76e0-185">Kui maksu tasakaalustamine ei ole aruandlusvaluuta jaoks mingil põhjusel tasakaalus, näiteks müügimaksu teisendustee on „Arvestusvaluuta” või vahetuskurss muutub samal maksu tasakaalustamise perioodil, siis süsteem loob automaatselt raamatupidamise kirjed, et reguleerida maksu summa erinevust ja tasakaalustada seda realiseeritud vahetusega saadud tulu/kulu kontoga, mis on pearaamatu seadistuses konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="a76e0-185">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, thebn the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="a76e0-186">Kasutades selle funktsiooni demonstreerimiseks eelmist näidet, oletagem, et tabeli TAXTRANS andmed on sisestamise ajal järgmised.</span><span class="sxs-lookup"><span data-stu-id="a76e0-186">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="a76e0-187">Käibemaksu teisendamise parameetrid</span><span class="sxs-lookup"><span data-stu-id="a76e0-187">Sales tax conversion parameters</span></span> | <span data-ttu-id="a76e0-188">Kande valuuta (EUR)</span><span class="sxs-lookup"><span data-stu-id="a76e0-188">Transaction currency (EUR)</span></span> | <span data-ttu-id="a76e0-189">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="a76e0-189">Accounting currency (USD)</span></span> | <span data-ttu-id="a76e0-190">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="a76e0-190">Reporting currency (GBP)</span></span> | <span data-ttu-id="a76e0-191">Maksuvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="a76e0-191">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="a76e0-192">Arvestusvaluuta</span><span class="sxs-lookup"><span data-stu-id="a76e0-192">Accounting currency</span></span>             | <span data-ttu-id="a76e0-193">100</span><span class="sxs-lookup"><span data-stu-id="a76e0-193">100</span></span>                        | <span data-ttu-id="a76e0-194">111</span><span class="sxs-lookup"><span data-stu-id="a76e0-194">111</span></span>                       | <span data-ttu-id="a76e0-195">83</span><span class="sxs-lookup"><span data-stu-id="a76e0-195">83</span></span>                       | <span data-ttu-id="a76e0-196">**83.25**</span><span class="sxs-lookup"><span data-stu-id="a76e0-196">**83.25**</span></span>          |
| <span data-ttu-id="a76e0-197">Aruandlusvaluuta</span><span class="sxs-lookup"><span data-stu-id="a76e0-197">Reporting currency</span></span>              | <span data-ttu-id="a76e0-198">100</span><span class="sxs-lookup"><span data-stu-id="a76e0-198">100</span></span>                        | <span data-ttu-id="a76e0-199">111</span><span class="sxs-lookup"><span data-stu-id="a76e0-199">111</span></span>                       | <span data-ttu-id="a76e0-200">83</span><span class="sxs-lookup"><span data-stu-id="a76e0-200">83</span></span>                       | <span data-ttu-id="a76e0-201">**83**</span><span class="sxs-lookup"><span data-stu-id="a76e0-201">**83**</span></span>             |

<span data-ttu-id="a76e0-202">Kui käivitate käibemaksu tasakaalustuse programmi kuu lõpus, on raamatupidamise kirje järgmine.</span><span class="sxs-lookup"><span data-stu-id="a76e0-202">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="a76e0-203">Stsenaarium: müügimaksu teisendamine = „arvestusvaluuta”</span><span class="sxs-lookup"><span data-stu-id="a76e0-203">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="a76e0-204">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="a76e0-204">Main account</span></span>           | <span data-ttu-id="a76e0-205">Kande valuuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="a76e0-205">Transaction currency (GBP)</span></span> | <span data-ttu-id="a76e0-206">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="a76e0-206">Accounting currency (USD)</span></span> | <span data-ttu-id="a76e0-207">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="a76e0-207">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="a76e0-208">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="a76e0-208">Tax Payable/Receivable</span></span> | <span data-ttu-id="a76e0-209">–83,25</span><span class="sxs-lookup"><span data-stu-id="a76e0-209">-83.25</span></span>                     | <span data-ttu-id="a76e0-210">–111</span><span class="sxs-lookup"><span data-stu-id="a76e0-210">-111</span></span>                      | <span data-ttu-id="a76e0-211">–83,25</span><span class="sxs-lookup"><span data-stu-id="a76e0-211">-83.25</span></span>                   |
| <span data-ttu-id="a76e0-212">Maksu tasakaalustus</span><span class="sxs-lookup"><span data-stu-id="a76e0-212">Tax Settlement</span></span>         | <span data-ttu-id="a76e0-213">83.25</span><span class="sxs-lookup"><span data-stu-id="a76e0-213">83.25</span></span>                      | <span data-ttu-id="a76e0-214">111</span><span class="sxs-lookup"><span data-stu-id="a76e0-214">111</span></span>                       | <span data-ttu-id="a76e0-215">83.25</span><span class="sxs-lookup"><span data-stu-id="a76e0-215">83.25</span></span>                    |
| <span data-ttu-id="a76e0-216">Realiseeritud kasum/kahjum</span><span class="sxs-lookup"><span data-stu-id="a76e0-216">Realized Gain/Loss</span></span>     | <span data-ttu-id="a76e0-217">0</span><span class="sxs-lookup"><span data-stu-id="a76e0-217">0</span></span>                          | <span data-ttu-id="a76e0-218">0</span><span class="sxs-lookup"><span data-stu-id="a76e0-218">0</span></span>                         | <span data-ttu-id="a76e0-219">–0,25</span><span class="sxs-lookup"><span data-stu-id="a76e0-219">-0.25</span></span>                    |
| <span data-ttu-id="a76e0-220">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="a76e0-220">Tax Payable/Receivable</span></span> | <span data-ttu-id="a76e0-221">0</span><span class="sxs-lookup"><span data-stu-id="a76e0-221">0</span></span>                          | <span data-ttu-id="a76e0-222">0</span><span class="sxs-lookup"><span data-stu-id="a76e0-222">0</span></span>                         | <span data-ttu-id="a76e0-223">0.25</span><span class="sxs-lookup"><span data-stu-id="a76e0-223">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="a76e0-224">Stsenaarium: müügimaksu teisendamine = „aruandlusvaluuta”</span><span class="sxs-lookup"><span data-stu-id="a76e0-224">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="a76e0-225">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="a76e0-225">Main account</span></span>           | <span data-ttu-id="a76e0-226">Kande valuuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="a76e0-226">Transaction currency (GBP)</span></span> | <span data-ttu-id="a76e0-227">Arvestusvaluuta (USD)</span><span class="sxs-lookup"><span data-stu-id="a76e0-227">Accounting currency (USD)</span></span> | <span data-ttu-id="a76e0-228">Aruandlusvaluuta (GBP)</span><span class="sxs-lookup"><span data-stu-id="a76e0-228">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="a76e0-229">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="a76e0-229">Tax Payable/Receivable</span></span> | <span data-ttu-id="a76e0-230">–83</span><span class="sxs-lookup"><span data-stu-id="a76e0-230">-83</span></span>                        | <span data-ttu-id="a76e0-231">–110,67</span><span class="sxs-lookup"><span data-stu-id="a76e0-231">-110.67</span></span>                   | <span data-ttu-id="a76e0-232">–83</span><span class="sxs-lookup"><span data-stu-id="a76e0-232">-83</span></span>                      |
| <span data-ttu-id="a76e0-233">Maksu tasakaalustus</span><span class="sxs-lookup"><span data-stu-id="a76e0-233">Tax Settlement</span></span>         | <span data-ttu-id="a76e0-234">83</span><span class="sxs-lookup"><span data-stu-id="a76e0-234">83</span></span>                         | <span data-ttu-id="a76e0-235">110.67</span><span class="sxs-lookup"><span data-stu-id="a76e0-235">110.67</span></span>                    | <span data-ttu-id="a76e0-236">83</span><span class="sxs-lookup"><span data-stu-id="a76e0-236">83</span></span>                       |
| <span data-ttu-id="a76e0-237">Realiseeritud kasum/kahjum</span><span class="sxs-lookup"><span data-stu-id="a76e0-237">Realized Gain/Loss</span></span>     | <span data-ttu-id="a76e0-238">0</span><span class="sxs-lookup"><span data-stu-id="a76e0-238">0</span></span>                          | <span data-ttu-id="a76e0-239">0.33</span><span class="sxs-lookup"><span data-stu-id="a76e0-239">0.33</span></span>                      | <span data-ttu-id="a76e0-240">0</span><span class="sxs-lookup"><span data-stu-id="a76e0-240">0</span></span>                        |
| <span data-ttu-id="a76e0-241">Makstav/saadav maks</span><span class="sxs-lookup"><span data-stu-id="a76e0-241">Tax Payable/Receivable</span></span> | <span data-ttu-id="a76e0-242">0</span><span class="sxs-lookup"><span data-stu-id="a76e0-242">0</span></span>                          | <span data-ttu-id="a76e0-243">–0,33</span><span class="sxs-lookup"><span data-stu-id="a76e0-243">-0.33</span></span>                     | <span data-ttu-id="a76e0-244">0</span><span class="sxs-lookup"><span data-stu-id="a76e0-244">0</span></span>                        |



<span data-ttu-id="a76e0-245">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="a76e0-245">For more information, see the following topics:</span></span>

- [<span data-ttu-id="a76e0-246">Topeltvaluuta</span><span class="sxs-lookup"><span data-stu-id="a76e0-246">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="a76e0-247">Käibemaksu ülevaade</span><span class="sxs-lookup"><span data-stu-id="a76e0-247">Sales tax overview</span></span>](indirect-taxes-overview.md)

