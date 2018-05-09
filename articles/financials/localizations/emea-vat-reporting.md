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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5c5cd61c45eb7cbc6f040f054a99d9a54e1ee854
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="vat-reporting-for-europe"></a><span data-ttu-id="f772a-103">Euroopa käibemaksuaruandlus</span><span class="sxs-lookup"><span data-stu-id="f772a-103">VAT reporting for Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f772a-104">Selles teemas antakse üldine ülevaade käibemaksu (KM) aruande seadistamise ja koostamise kohta mõningates Euroopa riikides.</span><span class="sxs-lookup"><span data-stu-id="f772a-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="f772a-105">See teema käsitleb üldiselt KM-aruande seadistamist ja koostamist.</span><span class="sxs-lookup"><span data-stu-id="f772a-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="f772a-106">See lähenemine on tavapärane kasutajate puhul järgmiste riikide/regioonide juriidiliste isikute puhul:</span><span class="sxs-lookup"><span data-stu-id="f772a-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="f772a-107">Austria</span><span class="sxs-lookup"><span data-stu-id="f772a-107">Austria</span></span>
-   <span data-ttu-id="f772a-108">Belgia</span><span class="sxs-lookup"><span data-stu-id="f772a-108">Belgium</span></span>
-   <span data-ttu-id="f772a-109">Tšehhi Vabariik</span><span class="sxs-lookup"><span data-stu-id="f772a-109">Czech Republic</span></span>
-   <span data-ttu-id="f772a-110">Eesti</span><span class="sxs-lookup"><span data-stu-id="f772a-110">Estonia</span></span>
-   <span data-ttu-id="f772a-111">Soome</span><span class="sxs-lookup"><span data-stu-id="f772a-111">Finland</span></span>
-   <span data-ttu-id="f772a-112">Saksamaa</span><span class="sxs-lookup"><span data-stu-id="f772a-112">Germany</span></span>
-   <span data-ttu-id="f772a-113">Läti</span><span class="sxs-lookup"><span data-stu-id="f772a-113">Latvia</span></span>
-   <span data-ttu-id="f772a-114">Leedu</span><span class="sxs-lookup"><span data-stu-id="f772a-114">Lithuania</span></span>
-   <span data-ttu-id="f772a-115">Holland</span><span class="sxs-lookup"><span data-stu-id="f772a-115">Netherlands</span></span>
-   <span data-ttu-id="f772a-116">Rootsi</span><span class="sxs-lookup"><span data-stu-id="f772a-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="f772a-117">KM-aruande ülevaade</span><span class="sxs-lookup"><span data-stu-id="f772a-117">VAT statement overview</span></span>
<span data-ttu-id="f772a-118">KM-aruanne põhineb maksukannete summadel.</span><span class="sxs-lookup"><span data-stu-id="f772a-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="f772a-119">KM-aruande koostamise protsess kuulub käibemaksu tasumise protsessi juurde, mida rakendatakse funktsiooni Käibemaksu tasakaalustamine ja sisestamine kaudu.</span><span class="sxs-lookup"><span data-stu-id="f772a-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="f772a-120">See funktsioon arvutab käibemaksu, mille tähtaeg jääb antud perioodi sisse.</span><span class="sxs-lookup"><span data-stu-id="f772a-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="f772a-121">Tasakaalustuse arvutamine sisaldab maksukannete valitud tasakaalustusperioodil sisestatud käibemaksu.</span><span class="sxs-lookup"><span data-stu-id="f772a-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="f772a-122">KM-aruande andmete arvutusprotsess põhineb käibemaksukoodide ja käibemaksuaruandluse koodide vahelisel seosel, mille alusel käibemaksuaruandluse koodid vastavad käibemaksuaruannete väljadele (või XML-i siltidele).</span><span class="sxs-lookup"><span data-stu-id="f772a-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="f772a-123">Iga käibemaksukoodi puhul tuleb seadistada igale kandetüübile (nt maksustatav müügikäive, maksustatavad ostud, maksustatav import) käibemaksuaruandluse koodid.</span><span class="sxs-lookup"><span data-stu-id="f772a-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="f772a-124">Seda liiki kandeid on kirjeldatud selle teema edasises jaotises KM-koodid KM-aruandluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="f772a-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="f772a-125">Iga käibemaksuaruandluse koodi puhul tuleb määrata konkreetne aruande paigutus.</span><span class="sxs-lookup"><span data-stu-id="f772a-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="f772a-126">Samal ajal on käibemaksukoodid seotud käibemaksu tasakaalustamise perioodide kaudu konkreetse käibemaksuasutusega.</span><span class="sxs-lookup"><span data-stu-id="f772a-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="f772a-127">Iga käibemaksuasutuse puhul tuleb määrata aruande paigutus.</span><span class="sxs-lookup"><span data-stu-id="f772a-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="f772a-128">Seega saab käibemaksukoodi aruande seadistuses valida ainult sama aruande paigutusega KM-aruandluse koode, mis on seadistatud käibemaksuasutuse jaoks käibemaksukoodi käibemaksu tasakaalustusperioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="f772a-129">Tellimuse või töölehe sisestamisel loodud käibemaksukanne sisaldab käibemaksukoodi, käibemaksu allikat, käibemaksu suunda ja kandesummasid (maksu põhisumma ja maksusumma arvestusvaluutas, käibemaksu valuuta ja kande valuuta).</span><span class="sxs-lookup"><span data-stu-id="f772a-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="f772a-130">Maksukannete atribuutide kombinatsiooni põhjal koostavad kandesummad käibemaksukoodidele määratud käibemaksuaruandluse koodide koondsummad.</span><span class="sxs-lookup"><span data-stu-id="f772a-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="f772a-131">Järgmine illustratsioon näitab andmete seost.</span><span class="sxs-lookup"><span data-stu-id="f772a-131">The following illustration shows the data relationship.</span></span>

![diagramm](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="f772a-133">KM-aruande seadistus</span><span class="sxs-lookup"><span data-stu-id="f772a-133">VAT statement setup</span></span>
<span data-ttu-id="f772a-134">KM-aruande koostamiseks tuleb seadistada järgmine.</span><span class="sxs-lookup"><span data-stu-id="f772a-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="f772a-135">KM-asutused KM-aruandluse jaoks</span><span class="sxs-lookup"><span data-stu-id="f772a-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="f772a-136">Enne käibemaksuaruandluse koodide seadistamist tuleb valida käibemaksuasutuse jaoks õige aruande paigutus.</span><span class="sxs-lookup"><span data-stu-id="f772a-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="f772a-137">Tehke lehel **Käibemaksuasutused** jaotises **Üldine** valik **Aruande paigutus**.</span><span class="sxs-lookup"><span data-stu-id="f772a-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="f772a-138">Seda paigutust kasutatakse käibemaksuaruandluse koodide seadistamisel.</span><span class="sxs-lookup"><span data-stu-id="f772a-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="f772a-139">Käibemaksuaruandluse koodid</span><span class="sxs-lookup"><span data-stu-id="f772a-139">Sales tax reporting codes</span></span>

<span data-ttu-id="f772a-140">Käibemaksuaruandluse koodid on väljade koodid KM-aruandes või siltide nimed XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="f772a-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="f772a-141">Neid koode kasutatakse aruande summade liitmiseks ja ettevalmistamiseks.</span><span class="sxs-lookup"><span data-stu-id="f772a-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="f772a-142">KM-aruande elektroonilise aruandluse vormingu konfigureerimisel kasutatakse saadud summade nimesid.</span><span class="sxs-lookup"><span data-stu-id="f772a-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="f772a-143">Käibemaksuaruandluse koode saab luua ja hallata lehel **Käibemaksuaruandluse koodid**.</span><span class="sxs-lookup"><span data-stu-id="f772a-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="f772a-144">Igale koodile tuleb määrata aruande paigutus.</span><span class="sxs-lookup"><span data-stu-id="f772a-144">You must assign each code a report layout.</span></span> <span data-ttu-id="f772a-145">Pärast käibemaksuaruandluse koodide loomist saate valida koodid jaotisest **Aruande seadistus** lehel **Käibemaksukoodid**.</span><span class="sxs-lookup"><span data-stu-id="f772a-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="f772a-146">Käibemaksukoodid KM-aruandluse jaoks</span><span class="sxs-lookup"><span data-stu-id="f772a-146">Sales tax codes for VAT reporting</span></span>

<span data-ttu-id="f772a-147"><!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Käibemaksukoodide</strong> lehel.</span><span class="sxs-lookup"><span data-stu-id="f772a-147"><!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Sales tax codes</strong> page.</span></span> <span data-ttu-id="f772a-148">Järgmises tabelis kirjeldatakse kandetüüpe käibemaksukoodide aruande seadistuses.</span><span class="sxs-lookup"><span data-stu-id="f772a-148">The following table describes the transaction types in the report setup for sales tax codes.</span></span> <span data-ttu-id="f772a-149">Arvutus sisaldab kandeid kõigi allikatüüpide kohta, v.a käibemaks.</span><span class="sxs-lookup"><span data-stu-id="f772a-149">The calculation includes transactions for all types of sources except sales tax.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f772a-150"><strong>Kande tüüp</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-150"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="f772a-151"><strong>Kande tüübi all arvestatud kannete ja summade kirjeldus</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-151"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f772a-152"><strong>Maksustatav müük</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-152"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="f772a-153">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-153">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-154">Kande kuupäev on valitud perioodil /</span><span class="sxs-lookup"><span data-stu-id="f772a-154">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="f772a-155">Müük on siseriiklik (<strong>Maksu suund</strong> on <strong>Tasumisele kuuluv käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="f772a-155">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="f772a-156">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-156">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f772a-157"><strong>Maksuvaba müük</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-157"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="f772a-158">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-158">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-159">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-159">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f772a-160">Müük on eksport (<strong>Maksu suund</strong> on <strong>Maksuvaba müük</strong>).</span><span class="sxs-lookup"><span data-stu-id="f772a-160">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="f772a-161">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-161">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f772a-162"><strong>Tasumisele kuuluv käibemaks</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-162"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="f772a-163">Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-163">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-164">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-164">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f772a-165">Müük on siseriiklik (<strong>Maksu suund</strong> on <strong>Tasumisele kuuluv käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="f772a-165">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="f772a-166">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-166">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f772a-167"><strong>Maksustatava müügi kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-167"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="f772a-168">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-168">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-169">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-169">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f772a-170">Müük on siseriiklik (<strong>Maksu suund</strong> on <strong>Tasumisele kuuluv käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="f772a-170">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="f772a-171">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-171">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f772a-172"><strong>Maksuvaba müügi kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-172"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="f772a-173">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-173">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-174">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-174">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f772a-175">Müük on eksport (<strong>Maksu suund</strong> on <strong>Maksuvaba müük</strong>).</span><span class="sxs-lookup"><span data-stu-id="f772a-175">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="f772a-176">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-176">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f772a-177"><strong>Käibemaks müügi kreeditarvel</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-177"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="f772a-178">Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-178">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-179">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-179">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f772a-180">Müük on siseriiklik (<strong>Maksu suund</strong> on <strong>Tasumisele kuuluv käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="f772a-180">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="f772a-181">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-181">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f772a-182"><strong>Maksustatavad ostud</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-182"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="f772a-183">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-183">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-184">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-184">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f772a-185">Ost on siseriiklik (<strong>Maksu suund</strong> on <strong>Saadaolev käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="f772a-185">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="f772a-186">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-186">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f772a-187"><strong>Maksuvaba ost</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-187"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="f772a-188">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-188">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-189">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-189">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f772a-190">Ost on import (<strong>Maksu suund</strong> on <strong>Maksuvaba ost</strong>).</span><span class="sxs-lookup"><span data-stu-id="f772a-190">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="f772a-191">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-191">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f772a-192"><strong>Saadaolev käibemaks</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-192"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="f772a-193">Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-193">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-194">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-194">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f772a-195">Ost on siseriiklik (<strong>Maksu suund</strong> on <strong>Saadaolev käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="f772a-195">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="f772a-196">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-196">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f772a-197"><strong>Maksustatav ostu kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-197"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="f772a-198">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-198">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-199">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-199">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f772a-200">Ost on siseriiklik (<strong>Maksu suund</strong> on <strong>Saadaolev käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="f772a-200">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="f772a-201">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-201">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f772a-202"><strong>Maksuvaba ostu kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-202"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="f772a-203">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-203">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-204">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-204">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f772a-205">Ost on import (<strong>Maksu suund</strong> on <strong>Maksuvaba ost</strong>).</span><span class="sxs-lookup"><span data-stu-id="f772a-205">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="f772a-206">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-206">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f772a-207"><strong>Käibemaks ostu kreeditarvel</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-207"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="f772a-208">Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-208">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-209">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-209">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f772a-210">Ost on siseriiklik (<strong>Maksu suund</strong> on <strong>Saadaolev käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="f772a-210">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="f772a-211">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-211">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f772a-212"><strong>Maksustatav import</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-212"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="f772a-213">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-213">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-214">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-214">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f772a-215"><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-215"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="f772a-216">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-216">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f772a-217"><strong>Tasakaalusta maksustatav import</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-217"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="f772a-218">Väärtuste <strong>Maksu baassummad</strong> pöördsumma kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-218">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-219">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-219">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f772a-220"><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong>.</span><span class="sxs-lookup"><span data-stu-id="f772a-220"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="f772a-221">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-221">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f772a-222"><strong>Maksustatava impordi kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-222"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="f772a-223">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-223">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-224">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-224">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="f772a-225">e</span><span class="sxs-lookup"><span data-stu-id="f772a-225">e</span></span><li><span data-ttu-id="f772a-226"><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong>.</span><span class="sxs-lookup"><span data-stu-id="f772a-226"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="f772a-227">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-227">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f772a-228"><strong>Tasakaalusta maksustatav impordi kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-228"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="f772a-229">Väärtuste <strong>Maksu baassummad</strong> pöördsumma kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-229">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-230">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-230">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f772a-231">Maksusuund on <strong>Kasutusmaks</strong>.</span><span class="sxs-lookup"><span data-stu-id="f772a-231">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="f772a-232">d</span><span class="sxs-lookup"><span data-stu-id="f772a-232">d</span></span><li><span data-ttu-id="f772a-233">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-233">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f772a-234"><strong>Kasutusmaks</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-234"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="f772a-235">Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-235">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-236">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-236">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f772a-237"><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong>.</span><span class="sxs-lookup"><span data-stu-id="f772a-237"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="f772a-238">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-238">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f772a-239"><strong>Kasutusmaksu vastasmaks</strong></span><span class="sxs-lookup"><span data-stu-id="f772a-239"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="f772a-240">Väärtuste <strong>Maksusummad</strong> pöördsumma kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="f772a-240">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="f772a-241">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="f772a-241">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="f772a-242"><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong>.</span><span class="sxs-lookup"><span data-stu-id="f772a-242"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="f772a-243">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="f772a-243">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="f772a-244">Ülal antud tabeli puhul eeldatakse, et täidetud on järgmised tingimused.</span><span class="sxs-lookup"><span data-stu-id="f772a-244">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="f772a-245">Maksu baassumma on kande summa väljalt **Päritolu arvestusvaluutas**.</span><span class="sxs-lookup"><span data-stu-id="f772a-245">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="f772a-246">Maksu baassumma on üleviidav summa väljalt **Tegelik käibemaksusumma arvestusvaluutas**.</span><span class="sxs-lookup"><span data-stu-id="f772a-246">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="f772a-247">ER-mudeli ja aruande vormingu konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f772a-247">Configure the ER model and format for the report</span></span>

<span data-ttu-id="f772a-248">Elektroonilist aruandlust (ER) saab kasutada väljavõtete ja aruande konfigureerimiseks ning andmete eksportimiseks erinevates elektroonilistes vormingutes, X++ koodi muutmata.</span><span class="sxs-lookup"><span data-stu-id="f772a-248">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="f772a-249">Lisateave:</span><span class="sxs-lookup"><span data-stu-id="f772a-249">For additional information:</span></span>

-   [<span data-ttu-id="f772a-250">Elektroonilise aruandluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="f772a-250">Electronic reporting overview</span></span>](../../dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="f772a-251">Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="f772a-251">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="f772a-252">Lokaliseerimisnõuded – GER-i konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="f772a-252">Localization requirements – Create a GER configuration</span></span>](../../dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="f772a-253">Riigipõhised ressursid KM-aruannete puhul</span><span class="sxs-lookup"><span data-stu-id="f772a-253">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="f772a-254">Iga riigi KM-aruanne peab vastama selle riigi seaduste nõuetele.</span><span class="sxs-lookup"><span data-stu-id="f772a-254">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="f772a-255">Järgmises tabelis loetletud riikide puhul on olemas KM-aruannete eelmääratud üldised mudelid ja vormingud.</span><span class="sxs-lookup"><span data-stu-id="f772a-255">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="f772a-256">Riik</span><span class="sxs-lookup"><span data-stu-id="f772a-256">Country</span></span>        | <span data-ttu-id="f772a-257">Lisateave</span><span class="sxs-lookup"><span data-stu-id="f772a-257">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="f772a-258">Austria</span><span class="sxs-lookup"><span data-stu-id="f772a-258">Austria</span></span>        |  [<span data-ttu-id="f772a-259">KM-aruande üksikasjad Austria puhul</span><span class="sxs-lookup"><span data-stu-id="f772a-259">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="f772a-260">Belgia</span><span class="sxs-lookup"><span data-stu-id="f772a-260">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="f772a-261">Tšehhi Vabariik</span><span class="sxs-lookup"><span data-stu-id="f772a-261">Czech Republic</span></span> |  [<span data-ttu-id="f772a-262">KM-aruande üksikasjad Tšehhi Vabariigi puhul</span><span class="sxs-lookup"><span data-stu-id="f772a-262">VAT statement details for Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="f772a-263">Eesti</span><span class="sxs-lookup"><span data-stu-id="f772a-263">Estonia</span></span>        |  [<span data-ttu-id="f772a-264">KM-aruande üksikasjad Eesti puhul</span><span class="sxs-lookup"><span data-stu-id="f772a-264">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="f772a-265">Soome</span><span class="sxs-lookup"><span data-stu-id="f772a-265">Finland</span></span>        |                                                                                 |
| <span data-ttu-id="f772a-266">Saksamaa</span><span class="sxs-lookup"><span data-stu-id="f772a-266">Germany</span></span>        |                                                                                 |
| <span data-ttu-id="f772a-267">Itaalia</span><span class="sxs-lookup"><span data-stu-id="f772a-267">Italy</span></span>          | [<span data-ttu-id="f772a-268">KM-aruande üksikasjad Itaalia puhul</span><span class="sxs-lookup"><span data-stu-id="f772a-268">VAT statement details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="f772a-269">Läti</span><span class="sxs-lookup"><span data-stu-id="f772a-269">Latvia</span></span>         | [<span data-ttu-id="f772a-270">KM-aruande üksikasjad Läti puhul</span><span class="sxs-lookup"><span data-stu-id="f772a-270">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="f772a-271">Leedu</span><span class="sxs-lookup"><span data-stu-id="f772a-271">Lithuania</span></span>      | [<span data-ttu-id="f772a-272">KM-aruande üksikasjad Leedu puhul</span><span class="sxs-lookup"><span data-stu-id="f772a-272">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="f772a-273">Holland</span><span class="sxs-lookup"><span data-stu-id="f772a-273">Netherlands</span></span>    |                                                                                 |
| <span data-ttu-id="f772a-274">Rootsi</span><span class="sxs-lookup"><span data-stu-id="f772a-274">Sweden</span></span>         |                                                                                 |






