---
title: Euroopa käibemaksuaruandlus
description: Selles teemas antakse üldine ülevaade käibemaksu (KM) aruande seadistamise ja koostamise kohta mõningates Euroopa riikides.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9d307ceae85773feb58d11e575df27e74b065cd3
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773445"
---
# <a name="vat-reporting-for-europe"></a><span data-ttu-id="8cd9c-103">Euroopa käibemaksuaruandlus</span><span class="sxs-lookup"><span data-stu-id="8cd9c-103">VAT reporting for Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8cd9c-104">Selles teemas antakse üldine ülevaade käibemaksu (KM) aruande seadistamise ja koostamise kohta mõningates Euroopa riikides.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="8cd9c-105">See teema käsitleb üldiselt KM-aruande seadistamist ja koostamist.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="8cd9c-106">See lähenemine on tavapärane kasutajate puhul järgmiste riikide/regioonide juriidiliste isikute puhul:</span><span class="sxs-lookup"><span data-stu-id="8cd9c-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="8cd9c-107">Austria</span><span class="sxs-lookup"><span data-stu-id="8cd9c-107">Austria</span></span>
-   <span data-ttu-id="8cd9c-108">Belgia</span><span class="sxs-lookup"><span data-stu-id="8cd9c-108">Belgium</span></span>
-   <span data-ttu-id="8cd9c-109">Tšehhi Vabariik</span><span class="sxs-lookup"><span data-stu-id="8cd9c-109">Czech Republic</span></span>
-   <span data-ttu-id="8cd9c-110">Eesti</span><span class="sxs-lookup"><span data-stu-id="8cd9c-110">Estonia</span></span>
-   <span data-ttu-id="8cd9c-111">Soome</span><span class="sxs-lookup"><span data-stu-id="8cd9c-111">Finland</span></span>
-   <span data-ttu-id="8cd9c-112">Saksamaa</span><span class="sxs-lookup"><span data-stu-id="8cd9c-112">Germany</span></span>
-   <span data-ttu-id="8cd9c-113">Läti</span><span class="sxs-lookup"><span data-stu-id="8cd9c-113">Latvia</span></span>
-   <span data-ttu-id="8cd9c-114">Leedu</span><span class="sxs-lookup"><span data-stu-id="8cd9c-114">Lithuania</span></span>
-   <span data-ttu-id="8cd9c-115">Holland</span><span class="sxs-lookup"><span data-stu-id="8cd9c-115">Netherlands</span></span>
-   <span data-ttu-id="8cd9c-116">Rootsi</span><span class="sxs-lookup"><span data-stu-id="8cd9c-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="8cd9c-117">KM-aruande ülevaade</span><span class="sxs-lookup"><span data-stu-id="8cd9c-117">VAT statement overview</span></span>
<span data-ttu-id="8cd9c-118">KM-aruanne põhineb maksukannete summadel.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="8cd9c-119">KM-aruande koostamise protsess kuulub käibemaksu tasumise protsessi juurde, mida rakendatakse funktsiooni Käibemaksu tasakaalustamine ja sisestamine kaudu.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="8cd9c-120">See funktsioon arvutab käibemaksu, mille tähtaeg jääb antud perioodi sisse.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="8cd9c-121">Tasakaalustuse arvutamine sisaldab maksukannete valitud tasakaalustusperioodil sisestatud käibemaksu.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="8cd9c-122">KM-aruande andmete arvutusprotsess põhineb käibemaksukoodide ja käibemaksuaruandluse koodide vahelisel seosel, mille alusel käibemaksuaruandluse koodid vastavad käibemaksuaruannete väljadele (või XML-i siltidele).</span><span class="sxs-lookup"><span data-stu-id="8cd9c-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="8cd9c-123">Iga käibemaksukoodi puhul tuleb seadistada igale kandetüübile (nt maksustatav müügikäive, maksustatavad ostud, maksustatav import) käibemaksuaruandluse koodid.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="8cd9c-124">Seda liiki kandeid on kirjeldatud selle teema edasises jaotises KM-koodid KM-aruandluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="8cd9c-125">Iga käibemaksuaruandluse koodi puhul tuleb määrata konkreetne aruande paigutus.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="8cd9c-126">Samal ajal on käibemaksukoodid seotud käibemaksu tasakaalustamise perioodide kaudu konkreetse käibemaksuasutusega.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="8cd9c-127">Iga käibemaksuasutuse puhul tuleb määrata aruande paigutus.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="8cd9c-128">Seega saab käibemaksukoodi aruande seadistuses valida ainult sama aruande paigutusega KM-aruandluse koode, mis on seadistatud käibemaksuasutuse jaoks käibemaksukoodi käibemaksu tasakaalustusperioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="8cd9c-129">Tellimuse või töölehe sisestamisel loodud käibemaksukanne sisaldab käibemaksukoodi, käibemaksu allikat, käibemaksu suunda ja kandesummasid (maksu põhisumma ja maksusumma arvestusvaluutas, käibemaksu valuuta ja kande valuuta).</span><span class="sxs-lookup"><span data-stu-id="8cd9c-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="8cd9c-130">Maksukannete atribuutide kombinatsiooni põhjal koostavad kandesummad käibemaksukoodidele määratud käibemaksuaruandluse koodide koondsummad.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="8cd9c-131">Järgmine illustratsioon näitab andmete seost.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-131">The following illustration shows the data relationship.</span></span>

![diagramm](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="8cd9c-133">KM-aruande seadistus</span><span class="sxs-lookup"><span data-stu-id="8cd9c-133">VAT statement setup</span></span>
<span data-ttu-id="8cd9c-134">KM-aruande koostamiseks tuleb seadistada järgmine.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="8cd9c-135">KM-asutused KM-aruandluse jaoks</span><span class="sxs-lookup"><span data-stu-id="8cd9c-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="8cd9c-136">Enne käibemaksuaruandluse koodide seadistamist tuleb valida käibemaksuasutuse jaoks õige aruande paigutus.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="8cd9c-137">Tehke lehel **Käibemaksuasutused** jaotises **Üldine** valik **Aruande paigutus**.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="8cd9c-138">Seda paigutust kasutatakse käibemaksuaruandluse koodide seadistamisel.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="8cd9c-139">Käibemaksuaruandluse koodid</span><span class="sxs-lookup"><span data-stu-id="8cd9c-139">Sales tax reporting codes</span></span>

<span data-ttu-id="8cd9c-140">Käibemaksuaruandluse koodid on väljade koodid KM-aruandes või siltide nimed XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="8cd9c-141">Neid koode kasutatakse aruande summade liitmiseks ja ettevalmistamiseks.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="8cd9c-142">KM-aruande elektroonilise aruandluse vormingu konfigureerimisel kasutatakse saadud summade nimesid.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="8cd9c-143">Käibemaksuaruandluse koode saab luua ja hallata lehel **Käibemaksuaruandluse koodid**.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="8cd9c-144">Igale koodile tuleb määrata aruande paigutus.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-144">You must assign each code a report layout.</span></span> <span data-ttu-id="8cd9c-145">Pärast käibemaksuaruandluse koodide loomist saate valida koodid jaotisest **Aruande seadistus** lehel **Käibemaksukoodid**.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="8cd9c-146">Käibemaksukoodid KM-aruandluse jaoks</span><span class="sxs-lookup"><span data-stu-id="8cd9c-146">Sales tax codes for VAT reporting</span></span>

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> <span data-ttu-id="8cd9c-147"> Alussummad ja käibemaksukannete maksusummad saab KM-aruandes aruandluskoodide all summeerida (XML-sildid või deklaratsiooni väljad).</span><span class="sxs-lookup"><span data-stu-id="8cd9c-147">Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes).</span></span> <span data-ttu-id="8cd9c-148">Selle saab seadistada, seostades käibemaksukoodide erinevate kandetüüpide käibemaksuaruandluse koodid lehel <strong>Käibemaksukoodid</strong>.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-148">You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Sales tax codes</strong> page.</span></span> <span data-ttu-id="8cd9c-149">Järgmises tabelis kirjeldatakse kandetüüpe käibemaksukoodide aruande seadistuses.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-149">The following table describes the transaction types in the report setup for sales tax codes.</span></span> <span data-ttu-id="8cd9c-150">Arvutus sisaldab kandeid kõigi allikatüüpide kohta, v.a käibemaks.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-150">The calculation includes transactions for all types of sources except sales tax.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8cd9c-151"><strong>Kande tüüp</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-151"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="8cd9c-152"><strong>Kande tüübi all arvestatud kannete ja summade kirjeldus</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-152"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cd9c-153"><strong>Maksustatav müük</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-153"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="8cd9c-154">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-154">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-155">Kande kuupäev on valitud perioodil /</span><span class="sxs-lookup"><span data-stu-id="8cd9c-155">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="8cd9c-156">Müük on siseriiklik (<strong>Maksu suund</strong> on <strong>Tasumisele kuuluv käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="8cd9c-156">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="8cd9c-157">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-157">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8cd9c-158"><strong>Maksuvaba müük</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-158"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="8cd9c-159">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-159">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-160">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-160">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="8cd9c-161">Müük on eksport (<strong>Maksu suund</strong> on <strong>Maksuvaba müük</strong>).</span><span class="sxs-lookup"><span data-stu-id="8cd9c-161">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="8cd9c-162">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-162">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cd9c-163"><strong>Tasumisele kuuluv käibemaks</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-163"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="8cd9c-164">Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-164">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-165">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-165">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="8cd9c-166">Müük on siseriiklik (<strong>Maksu suund</strong> on <strong>Tasumisele kuuluv käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="8cd9c-166">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="8cd9c-167">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-167">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8cd9c-168"><strong>Maksustatava müügi kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-168"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="8cd9c-169">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-169">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-170">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-170">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="8cd9c-171">Müük on siseriiklik (<strong>Maksu suund</strong> on <strong>Tasumisele kuuluv käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="8cd9c-171">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="8cd9c-172">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-172">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cd9c-173"><strong>Maksuvaba müügi kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-173"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="8cd9c-174">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-174">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-175">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-175">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="8cd9c-176">Müük on eksport (<strong>Maksu suund</strong> on <strong>Maksuvaba müük</strong>).</span><span class="sxs-lookup"><span data-stu-id="8cd9c-176">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="8cd9c-177">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-177">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8cd9c-178"><strong>Käibemaks müügi kreeditarvel</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-178"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="8cd9c-179">Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-179">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-180">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-180">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="8cd9c-181">Müük on siseriiklik (<strong>Maksu suund</strong> on <strong>Tasumisele kuuluv käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="8cd9c-181">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="8cd9c-182">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-182">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cd9c-183"><strong>Maksustatavad ostud</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-183"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="8cd9c-184">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-184">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-185">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-185">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="8cd9c-186">Ost on siseriiklik (<strong>Maksu suund</strong> on <strong>Saadaolev käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="8cd9c-186">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="8cd9c-187">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-187">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8cd9c-188"><strong>Maksuvaba ost</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-188"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="8cd9c-189">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-189">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-190">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-190">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="8cd9c-191">Ost on import (<strong>Maksu suund</strong> on <strong>Maksuvaba ost</strong>).</span><span class="sxs-lookup"><span data-stu-id="8cd9c-191">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="8cd9c-192">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-192">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cd9c-193"><strong>Saadaolev käibemaks</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-193"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="8cd9c-194">Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-194">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-195">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-195">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="8cd9c-196">Ost on siseriiklik (<strong>Maksu suund</strong> on <strong>Saadaolev käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="8cd9c-196">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="8cd9c-197">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-197">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8cd9c-198"><strong>Maksustatav ostu kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-198"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="8cd9c-199">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-199">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-200">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-200">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="8cd9c-201">Ost on siseriiklik (<strong>Maksu suund</strong> on <strong>Saadaolev käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="8cd9c-201">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="8cd9c-202">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-202">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cd9c-203"><strong>Maksuvaba ostu kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-203"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="8cd9c-204">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-204">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-205">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-205">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="8cd9c-206">Ost on import (<strong>Maksu suund</strong> on <strong>Maksuvaba ost</strong>).</span><span class="sxs-lookup"><span data-stu-id="8cd9c-206">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="8cd9c-207">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-207">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8cd9c-208"><strong>Käibemaks ostu kreeditarvel</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-208"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="8cd9c-209">Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-209">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-210">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-210">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="8cd9c-211">Ost on siseriiklik (<strong>Maksu suund</strong> on <strong>Saadaolev käibemaks</strong>).</span><span class="sxs-lookup"><span data-stu-id="8cd9c-211">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="8cd9c-212">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-212">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cd9c-213"><strong>Maksustatav import</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-213"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="8cd9c-214">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-214">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-215">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-215">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="8cd9c-216"><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-216"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="8cd9c-217">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-217">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8cd9c-218"><strong>Tasakaalusta maksustatav import</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-218"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="8cd9c-219">Väärtuste <strong>Maksu baassummad</strong> pöördsumma kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-219">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-220">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-220">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="8cd9c-221"><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong>.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-221"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="8cd9c-222">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-222">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cd9c-223"><strong>Maksustatava impordi kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-223"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="8cd9c-224">Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-224">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-225">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-225">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="8cd9c-226">e</span><span class="sxs-lookup"><span data-stu-id="8cd9c-226">e</span></span><li><span data-ttu-id="8cd9c-227"><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong>.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-227"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="8cd9c-228">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-228">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8cd9c-229"><strong>Tasakaalusta maksustatav impordi kreeditarve</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-229"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="8cd9c-230">Väärtuste <strong>Maksu baassummad</strong> pöördsumma kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-230">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-231">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-231">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="8cd9c-232">Maksusuund on <strong>Kasutusmaks</strong>.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-232">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="8cd9c-233">d</span><span class="sxs-lookup"><span data-stu-id="8cd9c-233">d</span></span><li><span data-ttu-id="8cd9c-234">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-234">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8cd9c-235"><strong>Kasutusmaks</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-235"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="8cd9c-236">Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-236">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-237">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-237">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="8cd9c-238"><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong>.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-238"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="8cd9c-239">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-239">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8cd9c-240"><strong>Kasutusmaksu vastasmaks</strong></span><span class="sxs-lookup"><span data-stu-id="8cd9c-240"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="8cd9c-241">Väärtuste <strong>Maksusummad</strong> pöördsumma kannete puhul, mis vastavad järgmistele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-241">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="8cd9c-242">Kande kuupäev on valitud perioodil.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-242">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="8cd9c-243"><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong>.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-243"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="8cd9c-244">Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-244">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="8cd9c-245">Ülal antud tabeli puhul eeldatakse, et täidetud on järgmised tingimused.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-245">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="8cd9c-246">Maksu baassumma on kande summa väljalt **Päritolu arvestusvaluutas**.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-246">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="8cd9c-247">Maksu baassumma on üleviidav summa väljalt **Tegelik käibemaksusumma arvestusvaluutas**.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-247">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="8cd9c-248">ER-mudeli ja aruande vormingu konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="8cd9c-248">Configure the ER model and format for the report</span></span>

<span data-ttu-id="8cd9c-249">Elektroonilist aruandlust (ER) saab kasutada väljavõtete ja aruande konfigureerimiseks ning andmete eksportimiseks erinevates elektroonilistes vormingutes, X++ koodi muutmata.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-249">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="8cd9c-250">Lisateave:</span><span class="sxs-lookup"><span data-stu-id="8cd9c-250">For additional information:</span></span>

-   [<span data-ttu-id="8cd9c-251">Elektroonilise aruandluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="8cd9c-251">Electronic reporting overview</span></span>](../../dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="8cd9c-252">Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="8cd9c-252">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="8cd9c-253">Lokaliseerimisnõuded – GER-i konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="8cd9c-253">Localization requirements – Create a GER configuration</span></span>](../../dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="8cd9c-254">Riigipõhised ressursid KM-aruannete puhul</span><span class="sxs-lookup"><span data-stu-id="8cd9c-254">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="8cd9c-255">Iga riigi KM-aruanne peab vastama selle riigi seaduste nõuetele.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-255">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="8cd9c-256">Järgmises tabelis loetletud riikide puhul on olemas KM-aruannete eelmääratud üldised mudelid ja vormingud.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-256">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="8cd9c-257">Riik</span><span class="sxs-lookup"><span data-stu-id="8cd9c-257">Country</span></span>        | <span data-ttu-id="8cd9c-258">Lisateave</span><span class="sxs-lookup"><span data-stu-id="8cd9c-258">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8cd9c-259">Austria</span><span class="sxs-lookup"><span data-stu-id="8cd9c-259">Austria</span></span>        |  [<span data-ttu-id="8cd9c-260">KM-aruande üksikasjad Austria puhul</span><span class="sxs-lookup"><span data-stu-id="8cd9c-260">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="8cd9c-261">Belgia</span><span class="sxs-lookup"><span data-stu-id="8cd9c-261">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="8cd9c-262">Tšehhi Vabariik</span><span class="sxs-lookup"><span data-stu-id="8cd9c-262">Czech Republic</span></span> |  [<span data-ttu-id="8cd9c-263">KM-aruanne Tšehhi Vabariigis</span><span class="sxs-lookup"><span data-stu-id="8cd9c-263">VAT statement for the Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="8cd9c-264">Eesti</span><span class="sxs-lookup"><span data-stu-id="8cd9c-264">Estonia</span></span>        |  [<span data-ttu-id="8cd9c-265">KM-aruande üksikasjad Eesti puhul</span><span class="sxs-lookup"><span data-stu-id="8cd9c-265">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="8cd9c-266">Soome</span><span class="sxs-lookup"><span data-stu-id="8cd9c-266">Finland</span></span>        |                                                                                 |
| <span data-ttu-id="8cd9c-267">Saksamaa</span><span class="sxs-lookup"><span data-stu-id="8cd9c-267">Germany</span></span>        |                                                                                 |
| <span data-ttu-id="8cd9c-268">Itaalia</span><span class="sxs-lookup"><span data-stu-id="8cd9c-268">Italy</span></span>          | [<span data-ttu-id="8cd9c-269">KM-aruannete üksikasjad Itaalias</span><span class="sxs-lookup"><span data-stu-id="8cd9c-269">VAT statements details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="8cd9c-270">Läti</span><span class="sxs-lookup"><span data-stu-id="8cd9c-270">Latvia</span></span>         | [<span data-ttu-id="8cd9c-271">KM-aruande üksikasjad Läti puhul</span><span class="sxs-lookup"><span data-stu-id="8cd9c-271">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="8cd9c-272">Leedu</span><span class="sxs-lookup"><span data-stu-id="8cd9c-272">Lithuania</span></span>      | [<span data-ttu-id="8cd9c-273">KM-aruande üksikasjad Leedu puhul</span><span class="sxs-lookup"><span data-stu-id="8cd9c-273">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="8cd9c-274">Holland</span><span class="sxs-lookup"><span data-stu-id="8cd9c-274">Netherlands</span></span>    |                                                                                 |
| <span data-ttu-id="8cd9c-275">Rootsi</span><span class="sxs-lookup"><span data-stu-id="8cd9c-275">Sweden</span></span>         |                                                                                 |




