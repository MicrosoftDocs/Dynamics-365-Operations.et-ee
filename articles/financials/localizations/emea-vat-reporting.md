---
title: "Euroopa käibemaksuaruandlus"
description: "Selles teemas antakse üldine ülevaade käibemaksu (KM) aruande seadistamise ja koostamise kohta mõningates Euroopa riikides."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7ce3c0397986ba2281aae7b71d579f3fe5f488ae
ms.openlocfilehash: 415e23190c6d7d12e824a42dec3916a4c3f5bc92
ms.contentlocale: et-ee
ms.lasthandoff: 12/21/2017

---

# <a name="vat-reporting-for-europe"></a><span data-ttu-id="58578-103">Euroopa käibemaksuaruandlus</span><span class="sxs-lookup"><span data-stu-id="58578-103">VAT reporting for Europe</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="58578-104">Selles teemas antakse üldine ülevaade käibemaksu (KM) aruande seadistamise ja koostamise kohta mõningates Euroopa riikides.</span><span class="sxs-lookup"><span data-stu-id="58578-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="58578-105">See teema käsitleb üldiselt KM-aruande seadistamist ja koostamist.</span><span class="sxs-lookup"><span data-stu-id="58578-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="58578-106">See lähenemine on tavapärane kasutajate puhul järgmiste riikide/regioonide juriidiliste isikute puhul:</span><span class="sxs-lookup"><span data-stu-id="58578-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="58578-107">Austria</span><span class="sxs-lookup"><span data-stu-id="58578-107">Austria</span></span>
-   <span data-ttu-id="58578-108">Belgia</span><span class="sxs-lookup"><span data-stu-id="58578-108">Belgium</span></span>
-   <span data-ttu-id="58578-109">Tšehhi Vabariik</span><span class="sxs-lookup"><span data-stu-id="58578-109">Czech Republic</span></span>
-   <span data-ttu-id="58578-110">Eesti</span><span class="sxs-lookup"><span data-stu-id="58578-110">Estonia</span></span>
-   <span data-ttu-id="58578-111">Soome</span><span class="sxs-lookup"><span data-stu-id="58578-111">Finland</span></span>
-   <span data-ttu-id="58578-112">Saksamaa</span><span class="sxs-lookup"><span data-stu-id="58578-112">Germany</span></span>
-   <span data-ttu-id="58578-113">Läti</span><span class="sxs-lookup"><span data-stu-id="58578-113">Latvia</span></span>
-   <span data-ttu-id="58578-114">Leedu</span><span class="sxs-lookup"><span data-stu-id="58578-114">Lithuania</span></span>
-   <span data-ttu-id="58578-115">Holland</span><span class="sxs-lookup"><span data-stu-id="58578-115">Netherlands</span></span>
-   <span data-ttu-id="58578-116">Rootsi</span><span class="sxs-lookup"><span data-stu-id="58578-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="58578-117">KM-aruande ülevaade</span><span class="sxs-lookup"><span data-stu-id="58578-117">VAT statement overview</span></span>
<span data-ttu-id="58578-118">KM-aruanne põhineb maksukannete summadel.</span><span class="sxs-lookup"><span data-stu-id="58578-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="58578-119">KM-aruande koostamise protsess kuulub käibemaksu tasumise protsessi juurde, mida rakendatakse funktsiooni Käibemaksu tasakaalustamine ja sisestamine kaudu.</span><span class="sxs-lookup"><span data-stu-id="58578-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="58578-120">See funktsioon arvutab käibemaksu, mille tähtaeg jääb antud perioodi sisse.</span><span class="sxs-lookup"><span data-stu-id="58578-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="58578-121">Tasakaalustuse arvutamine sisaldab maksukannete valitud tasakaalustusperioodil sisestatud käibemaksu.</span><span class="sxs-lookup"><span data-stu-id="58578-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="58578-122">KM-aruande andmete arvutusprotsess põhineb käibemaksukoodide ja käibemaksuaruandluse koodide vahelisel seosel, mille alusel käibemaksuaruandluse koodid vastavad käibemaksuaruannete väljadele (või XML-i siltidele).</span><span class="sxs-lookup"><span data-stu-id="58578-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="58578-123">Iga käibemaksukoodi puhul tuleb seadistada igale kandetüübile (nt maksustatav müügikäive, maksustatavad ostud, maksustatav import) käibemaksuaruandluse koodid.</span><span class="sxs-lookup"><span data-stu-id="58578-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="58578-124">Seda liiki kandeid on kirjeldatud selle teema edasises jaotises KM-koodid KM-aruandluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="58578-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="58578-125">Iga käibemaksuaruandluse koodi puhul tuleb määrata konkreetne aruande paigutus.</span><span class="sxs-lookup"><span data-stu-id="58578-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="58578-126">Samal ajal on käibemaksukoodid seotud käibemaksu tasakaalustamise perioodide kaudu konkreetse käibemaksuasutusega.</span><span class="sxs-lookup"><span data-stu-id="58578-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="58578-127">Iga käibemaksuasutuse puhul tuleb määrata aruande paigutus.</span><span class="sxs-lookup"><span data-stu-id="58578-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="58578-128">Seega saab käibemaksukoodi aruande seadistuses valida ainult sama aruande paigutusega KM-aruandluse koode, mis on seadistatud käibemaksuasutuse jaoks käibemaksukoodi käibemaksu tasakaalustusperioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="58578-129">Tellimuse või töölehe sisestamisel loodud käibemaksukanne sisaldab käibemaksukoodi, käibemaksu allikat, käibemaksu suunda ja kandesummasid (maksu põhisumma ja maksusumma arvestusvaluutas, käibemaksu valuuta ja kande valuuta).</span><span class="sxs-lookup"><span data-stu-id="58578-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="58578-130">Maksukannete atribuutide kombinatsiooni põhjal koostavad kandesummad käibemaksukoodidele määratud käibemaksuaruandluse koodide koondsummad.</span><span class="sxs-lookup"><span data-stu-id="58578-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="58578-131">Järgmine illustratsioon näitab andmete seost.</span><span class="sxs-lookup"><span data-stu-id="58578-131">The following illustration shows the data relationship.</span></span>

![diagramm](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="58578-133">KM-aruande seadistus</span><span class="sxs-lookup"><span data-stu-id="58578-133">VAT statement setup</span></span>
<span data-ttu-id="58578-134">KM-aruande koostamiseks tuleb seadistada järgmine.</span><span class="sxs-lookup"><span data-stu-id="58578-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="58578-135">KM-asutused KM-aruandluse jaoks</span><span class="sxs-lookup"><span data-stu-id="58578-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="58578-136">Enne käibemaksuaruandluse koodide seadistamist tuleb valida käibemaksuasutuse jaoks õige aruande paigutus.</span><span class="sxs-lookup"><span data-stu-id="58578-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="58578-137">Tehke lehel **Käibemaksuasutused** jaotises **Üldine** valik **Aruande paigutus**.</span><span class="sxs-lookup"><span data-stu-id="58578-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="58578-138">Seda paigutust kasutatakse käibemaksuaruandluse koodide seadistamisel.</span><span class="sxs-lookup"><span data-stu-id="58578-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="58578-139">Käibemaksuaruandluse koodid</span><span class="sxs-lookup"><span data-stu-id="58578-139">Sales tax reporting codes</span></span>

<span data-ttu-id="58578-140">Käibemaksuaruandluse koodid on väljade koodid KM-aruandes või siltide nimed XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="58578-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="58578-141">Neid koode kasutatakse aruande summade liitmiseks ja ettevalmistamiseks.</span><span class="sxs-lookup"><span data-stu-id="58578-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="58578-142">KM-aruande elektroonilise aruandluse vormingu konfigureerimisel kasutatakse saadud summade nimesid.</span><span class="sxs-lookup"><span data-stu-id="58578-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="58578-143">Käibemaksuaruandluse koode saab luua ja hallata lehel **Käibemaksuaruandluse koodid**.</span><span class="sxs-lookup"><span data-stu-id="58578-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="58578-144">Igale koodile tuleb määrata aruande paigutus.</span><span class="sxs-lookup"><span data-stu-id="58578-144">You must assign each code a report layout.</span></span> <span data-ttu-id="58578-145">Pärast käibemaksuaruandluse koodide loomist saate valida koodid jaotisest **Aruande seadistus** lehel **Käibemaksukoodid**.</span><span class="sxs-lookup"><span data-stu-id="58578-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="58578-146">Käibemaksukoodid KM-aruandluse jaoks</span><span class="sxs-lookup"><span data-stu-id="58578-146">Sales tax codes for VAT reporting</span></span>

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the **Sales tax codes** page. The following table describes the transaction types in the report setup for sales tax codes. The calculation includes transactions for all types of sources except sales tax.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="58578-147"><strong>Kande tüüp</strong></span><span class="sxs-lookup"><span data-stu-id="58578-147"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="58578-148"><strong>Kande tüübi all arvestatud kannete ja summade kirjeldus</strong></span><span class="sxs-lookup"><span data-stu-id="58578-148"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58578-149"><strong>Maksustatav müük</strong></span><span class="sxs-lookup"><span data-stu-id="58578-149"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="58578-150">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-150">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-151">Kande kuupäev on valitud perioodil /</span><span class="sxs-lookup"><span data-stu-id="58578-151">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="58578-152">Müük on siseriiklik (<strong>Maksu suund</strong> on <strong>Tasumisele kuuluv käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="58578-152">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="58578-153">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-153">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58578-154"><strong>Maksuvaba müük</strong></span><span class="sxs-lookup"><span data-stu-id="58578-154"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="58578-155">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-155">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-156">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-156">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="58578-157">Müük on eksport (<strong>Maksu suund</strong> on <strong>Maksuvaba müük</strong>).</span><span class="sxs-lookup"><span data-stu-id="58578-157">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="58578-158">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-158">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58578-159"><strong>Tasumisele kuuluv käibemaks</strong></span><span class="sxs-lookup"><span data-stu-id="58578-159"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="58578-160">Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-160">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-161">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-161">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="58578-162">Müük on siseriiklik (<strong>Maksu suund</strong> on <strong>Tasumisele kuuluv käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="58578-162">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="58578-163">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-163">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58578-164"><strong>Maksustatava müügi kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="58578-164"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="58578-165">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-165">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-166">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-166">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="58578-167">Müük on siseriiklik (<strong>Maksu suund</strong> on <strong>Tasumisele kuuluv käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="58578-167">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="58578-168">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-168">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58578-169"><strong>Maksuvaba müügi kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="58578-169"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="58578-170">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-170">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-171">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-171">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="58578-172">Müük on eksport (<strong>Maksu suund</strong> on <strong>Maksuvaba müük</strong>).</span><span class="sxs-lookup"><span data-stu-id="58578-172">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="58578-173">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-173">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58578-174"><strong>Käibemaks müügi kreeditarvel</strong></span><span class="sxs-lookup"><span data-stu-id="58578-174"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="58578-175">Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-175">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-176">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-176">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="58578-177">Müük on siseriiklik (<strong>Maksu suund</strong> on <strong>Tasumisele kuuluv käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="58578-177">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="58578-178">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-178">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58578-179"><strong>Maksustatavad ostud</strong></span><span class="sxs-lookup"><span data-stu-id="58578-179"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="58578-180">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-180">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-181">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-181">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="58578-182">Ost on siseriiklik (<strong>Maksu suund</strong> on <strong>Saadaolev käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="58578-182">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="58578-183">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-183">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58578-184"><strong>Maksuvaba ost</strong></span><span class="sxs-lookup"><span data-stu-id="58578-184"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="58578-185">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-185">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-186">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-186">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="58578-187">Ost on import (<strong>Maksu suund</strong> on <strong>Maksuvaba ost</strong>).</span><span class="sxs-lookup"><span data-stu-id="58578-187">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="58578-188">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-188">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58578-189"><strong>Saadaolev käibemaks</strong></span><span class="sxs-lookup"><span data-stu-id="58578-189"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="58578-190">Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-190">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-191">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-191">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="58578-192">Ost on siseriiklik (<strong>Maksu suund</strong> on <strong>Saadaolev käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="58578-192">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="58578-193">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-193">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58578-194"><strong>Maksustatav ostu kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="58578-194"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="58578-195">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-195">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-196">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-196">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="58578-197">Ost on siseriiklik (<strong>Maksu suund</strong> on <strong>Saadaolev käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="58578-197">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="58578-198">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-198">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58578-199"><strong>Maksuvaba ostu kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="58578-199"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="58578-200">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-200">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-201">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-201">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="58578-202">Ost on import (<strong>Maksu suund</strong> on <strong>Maksuvaba ost</strong>).</span><span class="sxs-lookup"><span data-stu-id="58578-202">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="58578-203">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-203">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58578-204"><strong>Käibemaks ostu kreeditarvel</strong></span><span class="sxs-lookup"><span data-stu-id="58578-204"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="58578-205">Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-205">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-206">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-206">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="58578-207">Ost on siseriiklik (<strong>Maksu suund</strong> on <strong>Saadaolev käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="58578-207">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="58578-208">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-208">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58578-209"><strong>Maksustatav import</strong></span><span class="sxs-lookup"><span data-stu-id="58578-209"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="58578-210">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-210">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-211">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-211">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="58578-212"><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong></span><span class="sxs-lookup"><span data-stu-id="58578-212"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="58578-213">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-213">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58578-214"><strong>Tasakaalusta maksustatav import</strong></span><span class="sxs-lookup"><span data-stu-id="58578-214"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="58578-215">Väärtuste <strong>Maksu baassummad</strong> pöördsumma kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-215">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-216">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-216">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="58578-217"><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong>.</span><span class="sxs-lookup"><span data-stu-id="58578-217"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="58578-218">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-218">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58578-219"><strong>Maksustatava impordi kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="58578-219"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="58578-220">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-220">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-221">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-221">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="58578-222">e</span><span class="sxs-lookup"><span data-stu-id="58578-222">e</span></span><li><span data-ttu-id="58578-223"><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong>.</span><span class="sxs-lookup"><span data-stu-id="58578-223"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="58578-224">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-224">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58578-225"><strong>Tasakaalusta maksustatav impordi kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="58578-225"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="58578-226">Väärtuste <strong>Maksu baassummad</strong> pöördsumma kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-226">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-227">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-227">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="58578-228">Maksusuund on <strong>Kasutusmaks</strong>.</span><span class="sxs-lookup"><span data-stu-id="58578-228">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="58578-229">d</span><span class="sxs-lookup"><span data-stu-id="58578-229">d</span></span><li><span data-ttu-id="58578-230">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-230">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58578-231"><strong>Kasutusmaks</strong></span><span class="sxs-lookup"><span data-stu-id="58578-231"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="58578-232">Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-232">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-233">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-233">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="58578-234"><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong>.</span><span class="sxs-lookup"><span data-stu-id="58578-234"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="58578-235">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-235">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58578-236"><strong>Kasutusmaksu vastasmaks</strong></span><span class="sxs-lookup"><span data-stu-id="58578-236"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="58578-237">Väärtuste <strong>Maksusummad</strong> pöördsumma kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="58578-237">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58578-238">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="58578-238">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="58578-239"><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong>.</span><span class="sxs-lookup"><span data-stu-id="58578-239"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="58578-240">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="58578-240">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="58578-241">Ülal antud tabeli puhul eeldatakse, et täidetud on järgmised tingimused.</span><span class="sxs-lookup"><span data-stu-id="58578-241">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="58578-242">Maksu baassumma on kande summa väljalt **Päritolu arvestusvaluutas**.</span><span class="sxs-lookup"><span data-stu-id="58578-242">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="58578-243">Maksu baassumma on üleviidav summa väljalt **Tegelik käibemaksusumma arvestusvaluutas**.</span><span class="sxs-lookup"><span data-stu-id="58578-243">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="58578-244">ER-mudeli ja aruande vormingu konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="58578-244">Configure the ER model and format for the report</span></span>

<span data-ttu-id="58578-245">Elektroonilist aruandlust (ER) saab kasutada väljavõtete ja aruande konfigureerimiseks ning andmete eksportimiseks erinevates elektroonilistes vormingutes, X++ koodi muutmata.</span><span class="sxs-lookup"><span data-stu-id="58578-245">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="58578-246">Lisateave:</span><span class="sxs-lookup"><span data-stu-id="58578-246">For additional information:</span></span>

-   [<span data-ttu-id="58578-247">Elektroonilise aruandluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="58578-247">Electronic reporting overview</span></span>](../../dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="58578-248">Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="58578-248">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="58578-249">Lokaliseerimisnõuded – GER-i konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="58578-249">Localization requirements – Create a GER configuration</span></span>](../../dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="58578-250">Riigipõhised ressursid KM-aruannete puhul</span><span class="sxs-lookup"><span data-stu-id="58578-250">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="58578-251">Iga riigi KM-aruanne peab vastama selle riigi seaduste nõuetele.</span><span class="sxs-lookup"><span data-stu-id="58578-251">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="58578-252">Järgmises tabelis loetletud riikide puhul on olemas KM-aruannete eelmääratud üldised mudelid ja vormingud.</span><span class="sxs-lookup"><span data-stu-id="58578-252">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="58578-253">Riik</span><span class="sxs-lookup"><span data-stu-id="58578-253">Country</span></span>        | <span data-ttu-id="58578-254">Lisateave</span><span class="sxs-lookup"><span data-stu-id="58578-254">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="58578-255">Austria</span><span class="sxs-lookup"><span data-stu-id="58578-255">Austria</span></span>        |  [<span data-ttu-id="58578-256">KM-aruande üksikasjad Austria puhul</span><span class="sxs-lookup"><span data-stu-id="58578-256">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="58578-257">Belgia</span><span class="sxs-lookup"><span data-stu-id="58578-257">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="58578-258">Tšehhi Vabariik</span><span class="sxs-lookup"><span data-stu-id="58578-258">Czech Republic</span></span> |  [<span data-ttu-id="58578-259">KM-aruande üksikasjad Tšehhi Vabariigi puhul</span><span class="sxs-lookup"><span data-stu-id="58578-259">VAT statement details for Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="58578-260">Eesti</span><span class="sxs-lookup"><span data-stu-id="58578-260">Estonia</span></span>        |  [<span data-ttu-id="58578-261">KM-aruande üksikasjad Eesti puhul</span><span class="sxs-lookup"><span data-stu-id="58578-261">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="58578-262">Soome</span><span class="sxs-lookup"><span data-stu-id="58578-262">Finland</span></span>        |                                                                                 |
| <span data-ttu-id="58578-263">Saksamaa</span><span class="sxs-lookup"><span data-stu-id="58578-263">Germany</span></span>        |                                                                                 |
| <span data-ttu-id="58578-264">Itaalia</span><span class="sxs-lookup"><span data-stu-id="58578-264">Italy</span></span>          | [<span data-ttu-id="58578-265">KM-aruande üksikasjad Itaalia puhul</span><span class="sxs-lookup"><span data-stu-id="58578-265">VAT statement details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="58578-266">Läti</span><span class="sxs-lookup"><span data-stu-id="58578-266">Latvia</span></span>         | [<span data-ttu-id="58578-267">KM-aruande üksikasjad Läti puhul</span><span class="sxs-lookup"><span data-stu-id="58578-267">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="58578-268">Leedu</span><span class="sxs-lookup"><span data-stu-id="58578-268">Lithuania</span></span>      | [<span data-ttu-id="58578-269">KM-aruande üksikasjad Leedu puhul</span><span class="sxs-lookup"><span data-stu-id="58578-269">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="58578-270">Holland</span><span class="sxs-lookup"><span data-stu-id="58578-270">Netherlands</span></span>    |                                                                                 |
| <span data-ttu-id="58578-271">Rootsi</span><span class="sxs-lookup"><span data-stu-id="58578-271">Sweden</span></span>         |                                                                                 |






