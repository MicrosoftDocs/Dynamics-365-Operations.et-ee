---
title: Arvutatud käibemaks üldise töölehe ridade kohta
description: Selles teemas selgitatakse, kuidas arvutatakse käibemaksu eri tüüpi kontode (hankija, klient, pearaamat ja projekt) kohta üldise töölehe ridadel.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
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
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 51d43c8e6d16201e1f8c392c13ead20287782dcc
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983593"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="3c819-103">Arvutatud käibemaks üldise töölehe ridade kohta</span><span class="sxs-lookup"><span data-stu-id="3c819-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c819-104">Selles teemas selgitatakse, kuidas arvutatakse käibemaksu eri tüüpi kontode (hankija, klient, pearaamat ja projekt) kohta üldise töölehe ridadel.</span><span class="sxs-lookup"><span data-stu-id="3c819-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="3c819-105">Protsessi saab jagada kolme etappi:</span><span class="sxs-lookup"><span data-stu-id="3c819-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="3c819-106">Määratlege käibemaksu suund.</span><span class="sxs-lookup"><span data-stu-id="3c819-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="3c819-107">Määratlege käibemaksu summa, mis talletatakse ajutise käibemaksu tabelis.</span><span class="sxs-lookup"><span data-stu-id="3c819-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="3c819-108">Määratleb käibemaksu summa ja konto kandel.</span><span class="sxs-lookup"><span data-stu-id="3c819-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="3c819-109">Määratlege käibemaksu suund.</span><span class="sxs-lookup"><span data-stu-id="3c819-109">Determine the sales tax direction</span></span>

<span data-ttu-id="3c819-110">Käibemaksu suuna määratlemise viis sõltub konto tüübist kandes.</span><span class="sxs-lookup"><span data-stu-id="3c819-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="3c819-111">Käibemaksu suund määratakse konto tüübi ja käibemaksukoodi kombinatsiooniga.</span><span class="sxs-lookup"><span data-stu-id="3c819-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="3c819-112">Järgmistes jaotistes on võimalused üksikasjalikumalt.</span><span class="sxs-lookup"><span data-stu-id="3c819-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="3c819-113">Kontotüüp on Projekt</span><span class="sxs-lookup"><span data-stu-id="3c819-113">Account type is Project</span></span>

<span data-ttu-id="3c819-114">Kui kandel on töölehe rida, kus konto tüüp on **Projekt**, rakendatakse kõigil kande tööleheridadel sama maksu suunda.</span><span class="sxs-lookup"><span data-stu-id="3c819-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="3c819-115">Järgmine illustratsioon näitab seda vormingut.</span><span class="sxs-lookup"><span data-stu-id="3c819-115">The following illustration shows the rule.</span></span> <span data-ttu-id="3c819-116">Järgmised punktid näitavad projekti kontode võimalikke maksu suundi.</span><span class="sxs-lookup"><span data-stu-id="3c819-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="3c819-117">•   Kui käibemaksukood on kasutusmaks, siis käibemaksu suund on kasutusmaks.</span><span class="sxs-lookup"><span data-stu-id="3c819-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="3c819-118">•   Kui käibemaksukood on maksuvaba, siis käibemaksu suund on maksuvaba ost.</span><span class="sxs-lookup"><span data-stu-id="3c819-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="3c819-119">•   Kui käibemaksukood on intracom km, siis käibemaksu suund on tasumisele kuuluv käibemaks.</span><span class="sxs-lookup"><span data-stu-id="3c819-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="3c819-120">• Kui käibemaksukood on pöördmaksustamine, siis käibemaksu suund on tasumisele kuuluv käibemaks.</span><span class="sxs-lookup"><span data-stu-id="3c819-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="3c819-121">Vastasel juhul on käibemaksu suund saadaolev käibemaks.</span><span class="sxs-lookup"><span data-stu-id="3c819-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="3c819-122">Järgmine diagramm illustreerib reeglit graafiliselt.</span><span class="sxs-lookup"><span data-stu-id="3c819-122">The following diagram illustrates the rule graphically.</span></span>

![Maksu suuna võimalused projekti kontodele](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="3c819-124">Kontotüüp on Tarnija</span><span class="sxs-lookup"><span data-stu-id="3c819-124">Account type is Vendor</span></span>

<span data-ttu-id="3c819-125">Kui kandel on töölehe rida, kus konto tüüp on **Tarnija**, rakendavad kõik kande töölehe read sama maksu suuna.</span><span class="sxs-lookup"><span data-stu-id="3c819-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="3c819-126">Järgmised punktid näitavad tarnija kontode võimalikke maksustamise suundi.</span><span class="sxs-lookup"><span data-stu-id="3c819-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="3c819-127">•   Kui käibemaksukood on kasutusmaks, siis käibemaksu suund on kasutusmaks.</span><span class="sxs-lookup"><span data-stu-id="3c819-127">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="3c819-128">•   Kui käibemaksukood on maksuvaba, siis käibemaksu suund on maksuvaba ost.</span><span class="sxs-lookup"><span data-stu-id="3c819-128">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="3c819-129">•   Kui käibemaksukood on intracom km, siis käibemaksu suund on tasumisele kuuluv käibemaks.</span><span class="sxs-lookup"><span data-stu-id="3c819-129">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="3c819-130">• Kui käibemaksukood on pöördmaksustamine, siis käibemaksu suund on tasumisele kuuluv käibemaks.</span><span class="sxs-lookup"><span data-stu-id="3c819-130">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="3c819-131">Vastasel juhul on käibemaksu suund saadaolev käibemaks.</span><span class="sxs-lookup"><span data-stu-id="3c819-131">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="3c819-132">Järgmine diagramm illustreerib reeglit graafiliselt.</span><span class="sxs-lookup"><span data-stu-id="3c819-132">The following diagram illustrates the rule graphically.</span></span>

![Maksu suuna võimalused tarnija kontodele](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="3c819-134">Kontotüüp on Klient</span><span class="sxs-lookup"><span data-stu-id="3c819-134">Account type is Customer</span></span>

<span data-ttu-id="3c819-135">Kui kandel on töölehe rida, kus konto tüüp on **Klient**, rakendavad kõik kande töölehe read sama maksu suuna.</span><span class="sxs-lookup"><span data-stu-id="3c819-135">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="3c819-136">Järgmised punktid näitavad kliendi kontode võimalikke maksustamise suundi.</span><span class="sxs-lookup"><span data-stu-id="3c819-136">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="3c819-137">•   Kui käibemaksukood on maksuvaba, siis käibemaksu suund on maksuvaba ost.</span><span class="sxs-lookup"><span data-stu-id="3c819-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="3c819-138">• Kui käibemaksukood on intracom km, siis käibemaksu suund on saadaolev käibemaks.</span><span class="sxs-lookup"><span data-stu-id="3c819-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="3c819-139">• Kui käibemaksukood on pöördmaksustamine, siis käibemaksu suund on saadaolev käibemaks.</span><span class="sxs-lookup"><span data-stu-id="3c819-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="3c819-140">Muul juhul on käibemaksu suund tasumisele kuuluv käibemaks.</span><span class="sxs-lookup"><span data-stu-id="3c819-140">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="3c819-141">Järgmine diagramm illustreerib reeglit graafiliselt.</span><span class="sxs-lookup"><span data-stu-id="3c819-141">The following diagram illustrates the rule graphically.</span></span>

![Maksu suuna võimalused kliendi kontodele](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="3c819-143">Konto tüüp on Pearaamat</span><span class="sxs-lookup"><span data-stu-id="3c819-143">Account type is Ledger</span></span>

<span data-ttu-id="3c819-144">Järgmisel joonisel on näha reegel, mis rakendub siis, kui kandel on ainult töölehe read, kus konto tüüp on **Pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="3c819-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="3c819-145">Järgmised punktid näitavad pearaamatu kontode võimalikke maksustamise suundi.</span><span class="sxs-lookup"><span data-stu-id="3c819-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="3c819-146">•   Kui käibemaksukood on kasutusmaks, siis käibemaksu suund on kasutusmaks.</span><span class="sxs-lookup"><span data-stu-id="3c819-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="3c819-147">•   Kui käibemaksukood on maksuvaba, siis käibemaksu suund on maksuvaba ost.</span><span class="sxs-lookup"><span data-stu-id="3c819-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="3c819-148">Vastasel juhul, kui töölehe summa on deebet (positiivne), on käibemaksu suund saadaolev käibemaks. Kui töölehe summa on kreedit (negatiivne), on käibemaksu suund tasumisele kuuluv käibemaks.</span><span class="sxs-lookup"><span data-stu-id="3c819-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="3c819-149">Järgmine diagramm illustreerib reeglit graafiliselt.</span><span class="sxs-lookup"><span data-stu-id="3c819-149">The following diagram illustrates the rule graphically.</span></span>

![Maksu suuna võimalused pearaamatu kontodele](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="3c819-151">Käibemaksu suuna muutmine</span><span class="sxs-lookup"><span data-stu-id="3c819-151">Override the sales tax direction</span></span>

<span data-ttu-id="3c819-152">Käibemaksu suunda saate muuta siis, kui kanne sisaldab ainult ridu, mille konto tüüp on **Pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="3c819-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="3c819-153">Avage **Pearaamat \> Kontode tabel \> Kontod \> Põhikontod**, ja valige **juriidilise isiku muutmiste** kiirkaart</span><span class="sxs-lookup"><span data-stu-id="3c819-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="3c819-154">Käibemaksu summa määramine</span><span class="sxs-lookup"><span data-stu-id="3c819-154">Determine the sales tax amount</span></span>

<span data-ttu-id="3c819-155">Selles jaotises kirjeldatakse käibemaksu summa märgi arvutamist.</span><span class="sxs-lookup"><span data-stu-id="3c819-155">This section describes how the sales tax amount sign is calculated.</span></span>

![Käibemaksu kannete leht](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="3c819-157">Järgmine tabel näitab üldist käibemaksu summade märgi määramise reeglit ajutises käibemaksu tabelis.</span><span class="sxs-lookup"><span data-stu-id="3c819-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="3c819-158">Töölehe rea summa</span><span class="sxs-lookup"><span data-stu-id="3c819-158">Journal line amount</span></span> | <span data-ttu-id="3c819-159">Käibemaksu suund</span><span class="sxs-lookup"><span data-stu-id="3c819-159">Sales tax direction</span></span>  | <span data-ttu-id="3c819-160">Käibemaksu summa märk</span><span class="sxs-lookup"><span data-stu-id="3c819-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="3c819-161">Positiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-161">Positive</span></span>            | <span data-ttu-id="3c819-162">Saadaolev käibemaks</span><span class="sxs-lookup"><span data-stu-id="3c819-162">Sales Tax Receivable</span></span> | <span data-ttu-id="3c819-163">Positiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-163">Positive</span></span>              |
| <span data-ttu-id="3c819-164">Positiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-164">Positive</span></span>            | <span data-ttu-id="3c819-165">Tasumisele kuuluv käibemaks</span><span class="sxs-lookup"><span data-stu-id="3c819-165">Sales Tax Payable</span></span>    | <span data-ttu-id="3c819-166">Negatiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-166">Negative</span></span>              |
| <span data-ttu-id="3c819-167">Negatiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-167">Negative</span></span>            | <span data-ttu-id="3c819-168">Saadaolev käibemaks</span><span class="sxs-lookup"><span data-stu-id="3c819-168">Sales Tax Receivable</span></span> | <span data-ttu-id="3c819-169">Negatiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-169">Negative</span></span>              |
| <span data-ttu-id="3c819-170">Negatiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-170">Negative</span></span>            | <span data-ttu-id="3c819-171">Tasumisele kuuluv käibemaks</span><span class="sxs-lookup"><span data-stu-id="3c819-171">Sales Tax Payable</span></span>    | <span data-ttu-id="3c819-172">Positiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-172">Positive</span></span>              |

<span data-ttu-id="3c819-173">On olemas erireegel kannete jaoks, millel on ainult read **Projekt** või **Pearaamat**, kui real **Pearaamat** on valitud käibemaksugrupp või kauba käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="3c819-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="3c819-174">Seda reeglit juhib üldiste töölehtede puhul sõltumatu käibemaksu arvutamise lubamise funktsioon.</span><span class="sxs-lookup"><span data-stu-id="3c819-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="3c819-175">Kui see funktsioon on välja lülitatud, kasutab rea **Pearaamatu** maksusumma rea **Projekt** deebeti/kreediti suunda.</span><span class="sxs-lookup"><span data-stu-id="3c819-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="3c819-176">Kui see funktsioon on sisse lülitatud, kasutab rea **Pearaamat** maksusmma omaenda deebeti/kreediti suunda.</span><span class="sxs-lookup"><span data-stu-id="3c819-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="3c819-177">Järgmised tabelid näitavad iga stsenaariumi reeglit.</span><span class="sxs-lookup"><span data-stu-id="3c819-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="3c819-178">**Reegel sisse lülitatud funktsiooni korral**</span><span class="sxs-lookup"><span data-stu-id="3c819-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="3c819-179">Projekti töölehe rea summa</span><span class="sxs-lookup"><span data-stu-id="3c819-179">Journal line amount of project</span></span> | <span data-ttu-id="3c819-180">Käibemaksu suund</span><span class="sxs-lookup"><span data-stu-id="3c819-180">Sales tax direction</span></span>  | <span data-ttu-id="3c819-181">Käibemaksu summa märk</span><span class="sxs-lookup"><span data-stu-id="3c819-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="3c819-182">Positiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-182">Positive</span></span>                       | <span data-ttu-id="3c819-183">Saadaolev käibemaks</span><span class="sxs-lookup"><span data-stu-id="3c819-183">Sales Tax Receivable</span></span> | <span data-ttu-id="3c819-184">Positiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-184">Positive</span></span>              |
| <span data-ttu-id="3c819-185">Negatiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-185">Negative</span></span>                       | <span data-ttu-id="3c819-186">Saadaolev käibemaks</span><span class="sxs-lookup"><span data-stu-id="3c819-186">Sales Tax Receivable</span></span> | <span data-ttu-id="3c819-187">Negatiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-187">Negative</span></span>              |

<span data-ttu-id="3c819-188">**Reegel välja lülitatud funktsiooni korral**</span><span class="sxs-lookup"><span data-stu-id="3c819-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="3c819-189">Pearaamatu töölehe rea summa</span><span class="sxs-lookup"><span data-stu-id="3c819-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="3c819-190">Käibemaksu suund</span><span class="sxs-lookup"><span data-stu-id="3c819-190">Sales tax direction</span></span>  | <span data-ttu-id="3c819-191">Käibemaksu summa märk</span><span class="sxs-lookup"><span data-stu-id="3c819-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="3c819-192">Positiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-192">Positive</span></span>                       | <span data-ttu-id="3c819-193">Saadaolev käibemaks</span><span class="sxs-lookup"><span data-stu-id="3c819-193">Sales Tax Receivable</span></span> | <span data-ttu-id="3c819-194">Positiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-194">Positive</span></span>              |
| <span data-ttu-id="3c819-195">Negatiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-195">Negative</span></span>                       | <span data-ttu-id="3c819-196">Saadaolev käibemaks</span><span class="sxs-lookup"><span data-stu-id="3c819-196">Sales Tax Receivable</span></span> | <span data-ttu-id="3c819-197">Negatiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="3c819-198">Määratleb kande käibemaksu summa ja konto</span><span class="sxs-lookup"><span data-stu-id="3c819-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="3c819-199">Kui sisestate käibemaksu, tuuakse põhikonto pearaamatusse sisestatava grupi profiilist.</span><span class="sxs-lookup"><span data-stu-id="3c819-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="3c819-200">Kui käibemaks on saadaolev, kasutab süsteem profiilis määratletud saadaoleva käibemaksu kontot.</span><span class="sxs-lookup"><span data-stu-id="3c819-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="3c819-201">Kui käibemaks on tasumisele kuuluv, kasutab süsteem profiilis määratletud tasumisele kuuluva käibemaksu kontot.</span><span class="sxs-lookup"><span data-stu-id="3c819-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="3c819-202">Järgmine tabel näitab üldist reeglit.</span><span class="sxs-lookup"><span data-stu-id="3c819-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="3c819-203">Käibemaksu suund</span><span class="sxs-lookup"><span data-stu-id="3c819-203">Sales tax direction</span></span>  | <span data-ttu-id="3c819-204">Käibemaksu summa märk</span><span class="sxs-lookup"><span data-stu-id="3c819-204">Sales tax amount sign</span></span> | <span data-ttu-id="3c819-205">Käibemaksukonto</span><span class="sxs-lookup"><span data-stu-id="3c819-205">Sales tax account</span></span>      | <span data-ttu-id="3c819-206">Kandesumma</span><span class="sxs-lookup"><span data-stu-id="3c819-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="3c819-207">Saadaolev käibemaks</span><span class="sxs-lookup"><span data-stu-id="3c819-207">Sales Tax Receivable</span></span> | <span data-ttu-id="3c819-208">Positiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-208">Positive</span></span>              | <span data-ttu-id="3c819-209">Saadaoleva käibemaksu konto</span><span class="sxs-lookup"><span data-stu-id="3c819-209">Tax Receivable Account</span></span> | <span data-ttu-id="3c819-210">Positiivne (deebet)</span><span class="sxs-lookup"><span data-stu-id="3c819-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="3c819-211">Saadaolev käibemaks</span><span class="sxs-lookup"><span data-stu-id="3c819-211">Sales Tax Receivable</span></span> | <span data-ttu-id="3c819-212">Negatiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-212">Negative</span></span>              | <span data-ttu-id="3c819-213">Saadaoleva käibemaksu konto</span><span class="sxs-lookup"><span data-stu-id="3c819-213">Tax Receivable Account</span></span> | <span data-ttu-id="3c819-214">Negatiivne (kreedit)</span><span class="sxs-lookup"><span data-stu-id="3c819-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="3c819-215">Tasumisele kuuluv käibemaks</span><span class="sxs-lookup"><span data-stu-id="3c819-215">Sales Tax Payable</span></span>    | <span data-ttu-id="3c819-216">Positiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-216">Positive</span></span>              | <span data-ttu-id="3c819-217">Tasumisele kuuluva käibemaksu konto</span><span class="sxs-lookup"><span data-stu-id="3c819-217">Tax Payable Account</span></span>    | <span data-ttu-id="3c819-218">Negatiivne (kreedit)</span><span class="sxs-lookup"><span data-stu-id="3c819-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="3c819-219">Tasumisele kuuluv käibemaks</span><span class="sxs-lookup"><span data-stu-id="3c819-219">Sales Tax Payable</span></span>    | <span data-ttu-id="3c819-220">Negatiivne</span><span class="sxs-lookup"><span data-stu-id="3c819-220">Negative</span></span>              | <span data-ttu-id="3c819-221">Tasumisele kuuluva käibemaksu konto</span><span class="sxs-lookup"><span data-stu-id="3c819-221">Tax Payable Account</span></span>    | <span data-ttu-id="3c819-222">Positiivne (deebet)</span><span class="sxs-lookup"><span data-stu-id="3c819-222">Positive (Debit)</span></span>  |
