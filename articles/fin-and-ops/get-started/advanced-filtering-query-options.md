---
title: "Täpsem filtreerimis- ja päringusüntaks"
description: "See artikkel kirjeldab filtreerimis- ja päringuvalikuid, mis on saadaval, kui kasutate dialoogiboksis Täpsem filter / sortimine tehtemärki „vastab”."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fa9c962ffce161365d1a030cf9995cce3ff19934
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="ab2ef-103">Täpsem filtreerimis- ja päringusüntaks</span><span class="sxs-lookup"><span data-stu-id="ab2ef-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab2ef-104">See artikkel kirjeldab filtreerimis- ja päringuvalikuid, mis on saadaval, kui kasutate dialoogiboksis Täpsem filter / sortimine tehtemärki „vastab”.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-104">This article describes the filtering and query options that are available when you use the "matches" operator in the Advanced filter/sort dialog.</span></span>

<a name="advanced-query-syntax"></a><span data-ttu-id="ab2ef-105">Täpsem päringusüntaks</span><span class="sxs-lookup"><span data-stu-id="ab2ef-105">Advanced query syntax</span></span>
---------------------

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab2ef-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="ab2ef-106">Syntax</span></span></th>
<th><span data-ttu-id="ab2ef-107">Märgi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ab2ef-107">Character description</span></span></th>
<th><span data-ttu-id="ab2ef-108">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ab2ef-108">Description</span></span></th>
<th><span data-ttu-id="ab2ef-109">Näide</span><span class="sxs-lookup"><span data-stu-id="ab2ef-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ab2ef-110"><em>väärtus</em></span><span class="sxs-lookup"><span data-stu-id="ab2ef-110"><em>value</em></span></span></td>
<td><span data-ttu-id="ab2ef-111">Võrdub sisestatud väärtusega</span><span class="sxs-lookup"><span data-stu-id="ab2ef-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="ab2ef-112">Tippige väärtus, mille soovite leida.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="ab2ef-113"><strong>Sepp</strong> leiab väärtuse &quot;Sepp&quot;.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab2ef-114">!<em>väärtus</em> (hüüumärk)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="ab2ef-115">Ei võrdu sisestatud väärtusega</span><span class="sxs-lookup"><span data-stu-id="ab2ef-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="ab2ef-116">Tippige hüüumärk ja seejärel väärtus, mille soovite välistada.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="ab2ef-117"><strong>!Sepp</strong> leiab kõik väärtused, välja arvatud &quot;Sepp&quot;.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab2ef-118"><em>algväärtus</em>..<em>lõppväärtus</em> (topeltpunkt)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="ab2ef-119">Kahe teineteisest topeltpunktiga eraldatud sisestatud väärtuse vahel</span><span class="sxs-lookup"><span data-stu-id="ab2ef-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="ab2ef-120">Tippige algväärtus, seejärel kaks punkti ja siis lõppväärtus.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="ab2ef-121"><strong>1..10</strong> leiab kõik väärtused vahemikus 1 kuni 10.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="ab2ef-122">Kuid näiteks stringiväljal leiab <strong>A..C</strong> kõik tähtedega &quot;A&quot; ja &quot;B&quot; algavad väärtused ning väärtused, mis võrduvad täpselt tähega &quot;C&quot;.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="ab2ef-123">Näiteks ei leia see päring stringi &quot;Ca&quot;.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-123">For example, this query won&#39;t find &quot;Ca&quot;.</span></span> <span data-ttu-id="ab2ef-124">Selleks et leida kõiki väärtusi vahemikus &quot;A<em>&quot; kuni &quot;C</em>&quot;, tippige <strong>A..D</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab2ef-125">..<em>väärtus</em> (topeltpunkt)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="ab2ef-126">Sisestatud väärtusest väiksem või sellega võrdne</span><span class="sxs-lookup"><span data-stu-id="ab2ef-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="ab2ef-127">Tippige kaks punkti ja seejärel väärtus.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="ab2ef-128"><strong>..1000</strong> leiab iga tuhandest väiksema või sellega võrdse arvu, näiteks &quot;100&quot;, &quot;999,95&quot; ja &quot;1000&quot;.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab2ef-129"><em>väärtus</em>..</span><span class="sxs-lookup"><span data-stu-id="ab2ef-129"><em>value</em>..</span></span> <span data-ttu-id="ab2ef-130">(topeltpunkt)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-130">(double period)</span></span></td>
<td><span data-ttu-id="ab2ef-131">Sisestatud väärtusest suurem või sellega võrdne</span><span class="sxs-lookup"><span data-stu-id="ab2ef-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="ab2ef-132">Tippige väärtus ja seejärel kaks punkti.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="ab2ef-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="ab2ef-133"><strong>1000..</strong></span></span> <span data-ttu-id="ab2ef-134">leiab iga tuhandest suurema või sellega võrdse arvu, näiteks &quot;1000&quot;, &quot;1000,01&quot; ja &quot;1 000 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab2ef-135">&gt;<em>väärtus</em> (märk „suurem kui”)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="ab2ef-136">Sisestatud väärtusest suurem</span><span class="sxs-lookup"><span data-stu-id="ab2ef-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="ab2ef-137">Tippige märk „suurem kui” (<strong>&gt;</strong>) ja seejärel väärtus.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="ab2ef-138"><strong>&gt;1000</strong> leiab iga tuhandest suurema arvu, näiteks &quot;1000,01&quot;, &quot;20 000&quot; ja &quot;1 000 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab2ef-139">&lt;<em>väärtus</em> (märk „väiksem kui”)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="ab2ef-140">Sisestatud väärtusest väiksem</span><span class="sxs-lookup"><span data-stu-id="ab2ef-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="ab2ef-141">Tippige märk „väiksem kui” (<strong>&lt;</strong>) ja seejärel väärtus.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="ab2ef-142"><strong>&lt;1000</strong> leiab iga tuhandest väiksema arvu, näiteks &quot;999,99&quot;, &quot;1&quot; ja &quot;–200&quot;.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab2ef-143"><em>väärtus</em>\* (tärn)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="ab2ef-144">Sisestatud väärtusega algav</span><span class="sxs-lookup"><span data-stu-id="ab2ef-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="ab2ef-145">Tippige lähteväärtus ja selle järele tärn (<strong><em></strong>).</span><span class="sxs-lookup"><span data-stu-id="ab2ef-145">Type the starting value and then an asterisk (<strong><em></strong>).</span></span></td>
<td><span data-ttu-id="ab2ef-146"><strong>S</em></strong> leiab iga &quot;S&quot;-tähega algava stringi, näiteks &quot;Stockholm&quot;, &quot;Sydney&quot; ja &quot;San Francisco&quot;.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-146"><strong>S</em></strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab2ef-147"><em><em>väärtus</em> (tärn)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-147"><em><em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="ab2ef-148">Sisestatud väärtusega lõppev</span><span class="sxs-lookup"><span data-stu-id="ab2ef-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="ab2ef-149">Tippige tärn ja selle järele lõppväärtus.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="ab2ef-150"><strong></em>east</strong> leiab iga &quot;east&quot;-lõpulise stringi, näiteks &quot;Northeast&quot; ja &quot;Southeast&quot;.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-150"><strong></em>east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab2ef-151"><em><em>väärtus</em></em> (tärn)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-151"><em><em>value</em></em> (asterisk)</span></span></td>
<td><span data-ttu-id="ab2ef-152">Sisaldab sisestatud väärtust</span><span class="sxs-lookup"><span data-stu-id="ab2ef-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="ab2ef-153">Tippige tärn, otsitav väärtus ja selle järele veel üks tärn.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="ab2ef-154"><strong><em>rn</em></strong> leiab iga stringi, milles sisaldub täheühend &quot;rn&quot;, näiteks &quot;Pärnu&quot; ja &quot;Kernu&quot;.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-154"><strong><em>th</em></strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab2ef-155">?</span><span class="sxs-lookup"><span data-stu-id="ab2ef-155">?</span></span> <span data-ttu-id="ab2ef-156">(küsimärk)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-156">(question mark)</span></span></td>
<td><span data-ttu-id="ab2ef-157">Ühte või mitut tundmatut märki sisaldav</span><span class="sxs-lookup"><span data-stu-id="ab2ef-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="ab2ef-158">Tippige väärtuses tundmatu märgi asemele küsimärk.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="ab2ef-159"><strong>Ma?i</strong> leiab nii &quot;Mari&quot; kui ka &quot;Mati&quot;.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab2ef-160"><em>väärtus</em>,<em>väärtus</em> (koma)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="ab2ef-161">Vastendab sobivad väärtused komadega eraldatult</span><span class="sxs-lookup"><span data-stu-id="ab2ef-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="ab2ef-162">Tippige kõik kriteeriumid, eraldades need komadega.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="ab2ef-163"><strong>A, D, F, G</strong> leiab täpselt &quot;A&quot;, &quot;D&quot;, &quot;F&quot; ja &quot;G&quot;.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="ab2ef-164"><strong>10, 20, 30, 100</strong> leiab täpselt &quot;10, 20, 30, 100&quot;.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab2ef-165">(<span class="code">SQL-lause</span>) (sulgudes SQL-lause)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-165">(<span class="code">SQL statement</span>) (SQL statement between parentheses)</span></span></td>
<td><span data-ttu-id="ab2ef-166">Kirjeldatud päringule vastav</span><span class="sxs-lookup"><span data-stu-id="ab2ef-166">Matching a defined query</span></span></td>
<td><span data-ttu-id="ab2ef-167">Tippige sulgudesse päring SQL-lausena.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-167">Type a query as an SQL statement between parentheses.</span></span></td>
<td><span data-ttu-id="ab2ef-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span><span class="sxs-lookup"><span data-stu-id="ab2ef-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab2ef-169">T</span><span class="sxs-lookup"><span data-stu-id="ab2ef-169">T</span></span></td>
<td><span data-ttu-id="ab2ef-170">Tänane kuupäev</span><span class="sxs-lookup"><span data-stu-id="ab2ef-170">Today&#39;s date</span></span></td>
<td><span data-ttu-id="ab2ef-171">Tippige <strong>T</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-171">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="ab2ef-172"><strong>T</strong> vastab tänasele kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-172"><strong>T</strong> matches today&#39;s date.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab2ef-173">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong>-meetod sulgudes</span><span class="sxs-lookup"><span data-stu-id="ab2ef-173">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="ab2ef-174">Vastendab <strong>SysQueryRangeUtil</strong>-meetodi parameetritega määratud väärtuse või väärtusevahemiku</span><span class="sxs-lookup"><span data-stu-id="ab2ef-174">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="ab2ef-175">Tippige <strong>SysQueryRangeUtil</strong>-meetod, mille parameetrid määravad väärtuse või väärtusevahemiku.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-175">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td><ol>
<li><span data-ttu-id="ab2ef-176">Klõpsake valikuid <strong>Müügireskontro</strong> &gt; <strong>Arved</strong> &gt; <strong>Ava kliendiarved</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-176">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="ab2ef-177">Vajutage klahvikombinatsiooni Ctrl + Shift + F3, et avada leht <strong>Päring</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-177">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="ab2ef-178">Klõpsake vahekaardil <strong>Vahemik</strong> nuppu <strong>Lisa</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-178">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="ab2ef-179">Valige väljal <strong>Tabel</strong> suvand <strong>Avatud kliendikanded</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-179">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="ab2ef-180">Valige väljal <strong>Väli</strong> suvand <strong>Tähtaeg</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-180">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="ab2ef-181">Sisestage väljale <strong>Kriteeriumid</strong> väärtus <strong>(yearRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-181">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="ab2ef-182">Klõpsake nupul <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-182">Click <strong>OK</strong>.</span></span> <span data-ttu-id="ab2ef-183">Loendilehte värskendatakse, et kuvada teie sisestatud kriteeriumitele vastavad arved.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-183">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="ab2ef-184">Selle näite puhul loetletakse kahe eelmise aasta tasumata arved.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-184">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="ab2ef-185">Lisateavet <strong>SysQueryRangeUtil</strong>-kuupäevameetodite kohta ja mõne näite leiate järgmises jaotises toodud tabelist.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-185">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="ab2ef-186">Täpsemad kuupäevapäringud, mis kasutavad SysQueryRangeUtil-meetodeid</span><span class="sxs-lookup"><span data-stu-id="ab2ef-186">Advanced date queries that use SysQueryRangeUtil methods</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab2ef-187">Meetod</span><span class="sxs-lookup"><span data-stu-id="ab2ef-187">Method</span></span></th>
<th><span data-ttu-id="ab2ef-188">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ab2ef-188">Description</span></span></th>
<th><span data-ttu-id="ab2ef-189">Näide</span><span class="sxs-lookup"><span data-stu-id="ab2ef-189">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ab2ef-190">Day (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-190">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="ab2ef-191">Leidke seansi kuupäevaga seotud kuupäev.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-191">Find a date relative to the session date.</span></span> <span data-ttu-id="ab2ef-192">Positiivsed väärtused näitavad tulevikukuupäevi ja negatiivsed väärtused näitavad minevikukuupäev.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-192">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td><ul>
<li><span data-ttu-id="ab2ef-193"><strong>Homme</strong> – sisestage <strong>(Day(1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-193"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="ab2ef-194"><strong>Täna</strong> – sisestage <strong>(Day(0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-194"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="ab2ef-195"><strong>Eile</strong> – sisestage <strong>(Day(-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-195"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab2ef-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="ab2ef-197">Leidke seansi kuupäevaga seotud kuupäevavahemik.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-197">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="ab2ef-198">Positiivsed väärtused näitavad tulevikukuupäevi ja negatiivsed väärtused näitavad minevikukuupäev.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-198">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td><ul>
<li><span data-ttu-id="ab2ef-199"><strong>Viimased 30 päeva</strong> – sisestage <strong>(DayRange(-30,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-199"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="ab2ef-200"><strong>Eelmised 30 päeva ja järgmised 30 päeva</strong> – sisestage <strong>(DayRange(-30,30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-200"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab2ef-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="ab2ef-202">Leidke kõik kuupäevad pärast määratud suhtelist kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-202">Find all dates after the specified relative date.</span></span></td>
<td><ul>
<li><span data-ttu-id="ab2ef-203"><strong>Rohkem kui 30 päeva alates praegusest</strong> – sisestage <strong>(GreaterThanDate(30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-203"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab2ef-204">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="ab2ef-204">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="ab2ef-205">Leidke kõik kuupäeva-/kellaajakirjed pärast praegust aega.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-205">Find all date/time entries after the current time.</span></span></td>
<td><ul>
<li><span data-ttu-id="ab2ef-206"><strong>Kõik tuleviku kuupäevad/kellaajad</strong> – sisestage <strong>(GreaterThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-206"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab2ef-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="ab2ef-208">Leidke kõik kuupäevad enne määratud suhtelist kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-208">Find all dates before the specified relative date.</span></span></td>
<td><ul>
<li><span data-ttu-id="ab2ef-209"><strong>Vähem kui seitse päeva alates praegusest</strong> – sisestage <strong>(LessThanDate(7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-209"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab2ef-210">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="ab2ef-210">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="ab2ef-211">Leidke kõik kuupäeva-/kellaajakirjed enne praegust aega.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-211">Find all date/time entries before the current time.</span></span></td>
<td><ul>
<li><span data-ttu-id="ab2ef-212"><strong>Kõik varasemad kuupäevad/kellaajad</strong> – sisestage <strong>(LessThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-212"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab2ef-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="ab2ef-214">Leidke kuupäevavahemik praeguse kuuga seotud kuude põhjal.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-214">Find a range of dates, based on months relative to the current month.</span></span></td>
<td><ul>
<li><span data-ttu-id="ab2ef-215"><strong>Eelmised kaks kuud</strong> – sisestage <strong>(MonthRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-215"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="ab2ef-216"><strong>Järgmised kolm kuud</strong> – sisestage <strong>(MonthRange(0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-216"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab2ef-217">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-217">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="ab2ef-218">Leidke kuupäevavahemik praeguse aastaga seotud aastate põhjal.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-218">Find a range of dates, based on years relative to the current year.</span></span></td>
<td><ul>
<li><span data-ttu-id="ab2ef-219"><strong>Järgmine aasta</strong> – sisestage <strong>(YearRange(0, 1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-219"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="ab2ef-220"><strong>Eelmine aasta</strong> – sisestage <strong>(YearRange(-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-220"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






