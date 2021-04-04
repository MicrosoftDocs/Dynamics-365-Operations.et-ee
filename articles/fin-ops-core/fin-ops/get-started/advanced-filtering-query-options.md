---
title: Täpsema filtreerimise ja päringu süntaks
description: See artikkel kirjeldab filtreerimis- ja päringuvalikuid, mis on saadaval, kui kasutate Filtripaanil või ruudustiku veerupäisefiltrites dialoogi Täpsem filter/sortimine või võrdusoperaatorit.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15805e24c46603afd34d40c5f94c1422b01cab4c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566062"
---
# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="a59b3-103">Täpsema filtreerimise ja päringu süntaks</span><span class="sxs-lookup"><span data-stu-id="a59b3-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a59b3-104">See artikkel kirjeldab filtreerimis- ja päringuvalikuid, mis on saadaval, kui kasutate Filtripaanil või ruudustiku veerupäisefiltrites dialoogi Täpsem filter/sortimine või **võrdusoperaatorit** .</span><span class="sxs-lookup"><span data-stu-id="a59b3-104">This topic describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="a59b3-105">Täpsem päringusüntaks</span><span class="sxs-lookup"><span data-stu-id="a59b3-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a59b3-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="a59b3-106">Syntax</span></span></th>
<th><span data-ttu-id="a59b3-107">Märgi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a59b3-107">Character description</span></span></th>
<th><span data-ttu-id="a59b3-108">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a59b3-108">Description</span></span></th>
<th><span data-ttu-id="a59b3-109">Näide</span><span class="sxs-lookup"><span data-stu-id="a59b3-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a59b3-110"><em>väärtus</em></span><span class="sxs-lookup"><span data-stu-id="a59b3-110"><em>value</em></span></span></td>
<td><span data-ttu-id="a59b3-111">Võrdub sisestatud väärtusega</span><span class="sxs-lookup"><span data-stu-id="a59b3-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="a59b3-112">Tippige väärtus, mille soovite leida.</span><span class="sxs-lookup"><span data-stu-id="a59b3-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="a59b3-113"><strong>Sepp</strong> leiab väärtuse &quot;Sepp&quot;.</span><span class="sxs-lookup"><span data-stu-id="a59b3-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-114">!<em>väärtus</em> (hüüumärk)</span><span class="sxs-lookup"><span data-stu-id="a59b3-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="a59b3-115">Ei võrdu sisestatud väärtusega</span><span class="sxs-lookup"><span data-stu-id="a59b3-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="a59b3-116">Tippige hüüumärk ja seejärel väärtus, mille soovite välistada.</span><span class="sxs-lookup"><span data-stu-id="a59b3-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="a59b3-117"><strong>!Sepp</strong> leiab kõik väärtused, välja arvatud &quot;Sepp&quot;.</span><span class="sxs-lookup"><span data-stu-id="a59b3-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-118"><em>algväärtus</em>..<em>lõppväärtus</em> (topeltpunkt)</span><span class="sxs-lookup"><span data-stu-id="a59b3-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="a59b3-119">Kahe teineteisest topeltpunktiga eraldatud sisestatud väärtuse vahel</span><span class="sxs-lookup"><span data-stu-id="a59b3-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="a59b3-120">Tippige algväärtus, seejärel kaks punkti ja siis lõppväärtus.</span><span class="sxs-lookup"><span data-stu-id="a59b3-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="a59b3-121"><strong>1..10</strong> leiab kõik väärtused vahemikus 1 kuni 10.</span><span class="sxs-lookup"><span data-stu-id="a59b3-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="a59b3-122">Kuid näiteks stringiväljal leiab <strong>A..C</strong> kõik tähtedega &quot;A&quot; ja &quot;B&quot; algavad väärtused ning väärtused, mis võrduvad täpselt tähega &quot;C&quot;.</span><span class="sxs-lookup"><span data-stu-id="a59b3-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="a59b3-123">Näiteks ei leia see päring stringi &quot;Ca&quot;.</span><span class="sxs-lookup"><span data-stu-id="a59b3-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="a59b3-124">Selleks et leida kõiki väärtusi vahemikus &quot;A<em>&quot; kuni &quot;C</em>&quot;, tippige <strong>A..D</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-125">..<em>väärtus</em> (topeltpunkt)</span><span class="sxs-lookup"><span data-stu-id="a59b3-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="a59b3-126">Sisestatud väärtusest väiksem või sellega võrdne</span><span class="sxs-lookup"><span data-stu-id="a59b3-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="a59b3-127">Tippige kaks punkti ja seejärel väärtus.</span><span class="sxs-lookup"><span data-stu-id="a59b3-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="a59b3-128"><strong>..1000</strong> leiab iga tuhandest väiksema või sellega võrdse arvu, näiteks &quot;100&quot;, &quot;999,95&quot; ja &quot;1000&quot;.</span><span class="sxs-lookup"><span data-stu-id="a59b3-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-129"><em>väärtus</em>..</span><span class="sxs-lookup"><span data-stu-id="a59b3-129"><em>value</em>..</span></span> <span data-ttu-id="a59b3-130">(topeltpunkt)</span><span class="sxs-lookup"><span data-stu-id="a59b3-130">(double period)</span></span></td>
<td><span data-ttu-id="a59b3-131">Sisestatud väärtusest suurem või sellega võrdne</span><span class="sxs-lookup"><span data-stu-id="a59b3-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="a59b3-132">Tippige väärtus ja seejärel kaks punkti.</span><span class="sxs-lookup"><span data-stu-id="a59b3-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="a59b3-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="a59b3-133"><strong>1000..</strong></span></span> <span data-ttu-id="a59b3-134">leiab iga tuhandest suurema või sellega võrdse arvu, näiteks &quot;1000&quot;, &quot;1000,01&quot; ja &quot;1 000 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="a59b3-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-135">&gt;<em>väärtus</em> (märk „suurem kui”)</span><span class="sxs-lookup"><span data-stu-id="a59b3-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="a59b3-136">Sisestatud väärtusest suurem</span><span class="sxs-lookup"><span data-stu-id="a59b3-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="a59b3-137">Tippige märk „suurem kui” (<strong>&gt;</strong>) ja seejärel väärtus.</span><span class="sxs-lookup"><span data-stu-id="a59b3-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="a59b3-138"><strong>&gt;1000</strong> leiab iga tuhandest suurema arvu, näiteks &quot;1000,01&quot;, &quot;20 000&quot; ja &quot;1 000 000&quot;.</span><span class="sxs-lookup"><span data-stu-id="a59b3-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-139">&lt;<em>väärtus</em> (märk „väiksem kui”)</span><span class="sxs-lookup"><span data-stu-id="a59b3-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="a59b3-140">Sisestatud väärtusest väiksem</span><span class="sxs-lookup"><span data-stu-id="a59b3-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="a59b3-141">Tippige märk „väiksem kui” (<strong>&lt;</strong>) ja seejärel väärtus.</span><span class="sxs-lookup"><span data-stu-id="a59b3-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="a59b3-142"><strong>&lt;1000</strong> leiab iga tuhandest väiksema arvu, näiteks &quot;999,99&quot;, &quot;1&quot; ja &quot;–200&quot;.</span><span class="sxs-lookup"><span data-stu-id="a59b3-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-143"><em>väärtus</em>\* (tärn)</span><span class="sxs-lookup"><span data-stu-id="a59b3-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="a59b3-144">Sisestatud väärtusega algav</span><span class="sxs-lookup"><span data-stu-id="a59b3-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="a59b3-145">Tippige lähteväärtus ja selle järele tärn (<strong>\*</strong>).</span><span class="sxs-lookup"><span data-stu-id="a59b3-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="a59b3-146"><strong>S\*</strong> leiab iga S-tähega algava stringi, näiteks &quot;S&quot;, nagu &quot;Stockholm&quot;, &quot;Sindi&quot; ja &quot;San Francisco&quot;.</span><span class="sxs-lookup"><span data-stu-id="a59b3-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-147">\*<em>väärtus</em> (tärn)</span><span class="sxs-lookup"><span data-stu-id="a59b3-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="a59b3-148">Sisestatud väärtusega lõppev</span><span class="sxs-lookup"><span data-stu-id="a59b3-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="a59b3-149">Tippige tärn ja selle järele lõppväärtus.</span><span class="sxs-lookup"><span data-stu-id="a59b3-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="a59b3-150"><strong>\*vere</strong> leiab iga &quot;vere&quot;-lõpulise stringi, näiteks &quot;Adavere&quot; ja &quot;Pandivere&quot;.</span><span class="sxs-lookup"><span data-stu-id="a59b3-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-151">*<em>väärtus</em>* (tärn)</span><span class="sxs-lookup"><span data-stu-id="a59b3-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="a59b3-152">Sisaldab sisestatud väärtust</span><span class="sxs-lookup"><span data-stu-id="a59b3-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="a59b3-153">Tippige tärn, otsitav väärtus ja selle järele veel üks tärn.</span><span class="sxs-lookup"><span data-stu-id="a59b3-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="a59b3-154"><strong>*rn*</strong> leiab iga stringi, milles sisaldub täheühend &quot;rn&quot;, näiteks &quot;Pärnu&quot; ja &quot;Kernu&quot;.</span><span class="sxs-lookup"><span data-stu-id="a59b3-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-155">?</span><span class="sxs-lookup"><span data-stu-id="a59b3-155">?</span></span> <span data-ttu-id="a59b3-156">(küsimärk)</span><span class="sxs-lookup"><span data-stu-id="a59b3-156">(question mark)</span></span></td>
<td><span data-ttu-id="a59b3-157">Ühte või mitut tundmatut märki sisaldav</span><span class="sxs-lookup"><span data-stu-id="a59b3-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="a59b3-158">Tippige väärtuses tundmatu märgi asemele küsimärk.</span><span class="sxs-lookup"><span data-stu-id="a59b3-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="a59b3-159"><strong>Ma?i</strong> leiab nii &quot;Mari&quot; kui ka &quot;Mati&quot;.</span><span class="sxs-lookup"><span data-stu-id="a59b3-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-160"><em>väärtus</em>,<em>väärtus</em> (koma)</span><span class="sxs-lookup"><span data-stu-id="a59b3-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="a59b3-161">Vastendab sobivad väärtused komadega eraldatult</span><span class="sxs-lookup"><span data-stu-id="a59b3-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="a59b3-162">Tippige kõik kriteeriumid, eraldades need komadega.</span><span class="sxs-lookup"><span data-stu-id="a59b3-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="a59b3-163"><strong>A, D, F, G</strong> leiab täpselt &quot;A&quot;, &quot;D&quot;, &quot;F&quot; ja &quot;G&quot;.</span><span class="sxs-lookup"><span data-stu-id="a59b3-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="a59b3-164"><strong>10, 20, 30, 100</strong> leiab täpselt &quot;10, 20, 30, 100&quot;.</span><span class="sxs-lookup"><span data-stu-id="a59b3-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-165">"" (kaks kahekordset jutumärki)</span><span class="sxs-lookup"><span data-stu-id="a59b3-165">"" (two double quotes)</span></span></td>
<td><span data-ttu-id="a59b3-166">Tühja väärtuse sobitamine</span><span class="sxs-lookup"><span data-stu-id="a59b3-166">Matching a blank value</span></span></td>
<td><span data-ttu-id="a59b3-167">Tippige kaks järjestikust kahekordset jutumärki, et filtreerida selle välja tühjad väärtused.</span><span class="sxs-lookup"><span data-stu-id="a59b3-167">Type two consecutive double quotes to filter for blank values in that field.</span></span></td>
<td><span data-ttu-id="a59b3-168">Kaks järjestikust kahekordset jutumärki (<strong>"</strong>") leiab ilma väärtuseta ridu käesoleva veeru jaoks.</span><span class="sxs-lookup"><span data-stu-id="a59b3-168">Two consecutive double quotes (<strong>""</strong>) finds rows with no value for the current column.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-169">(<span class="code">Finance and Operations päring</span>) (Finance and Operations päring sulgudes)</span><span class="sxs-lookup"><span data-stu-id="a59b3-169">(<span class="code">Finance and Operations query</span>) (Finance and Operations query between parentheses)</span></span></td>
<td><span data-ttu-id="a59b3-170">Kirjeldatud päringule vastav</span><span class="sxs-lookup"><span data-stu-id="a59b3-170">Matching a defined query</span></span></td>
<td><span data-ttu-id="a59b3-171">Sisestage päring sulgude vahele SQL-lausena, kasutades päringukeelt Finance and Operations .</span><span class="sxs-lookup"><span data-stu-id="a59b3-171">Type a query as an SQL statement between parentheses using the Finance and Operations query language.</span></span></td>
  <td><span data-ttu-id="a59b3-172"><strong><span class="code">((AccountNum NAGU "US *") & & (DirPartyTable.Name NAGU "CONT*"))</span></strong></span><span class="sxs-lookup"><span data-stu-id="a59b3-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span></span><br><br> 
       <span data-ttu-id="a59b3-173">filtritingimuse süntaksi näitena väljal juurandmeallikast, samuti väljal teisest andmeallikast (kõigi klientide lehel)</span><span class="sxs-lookup"><span data-stu-id="a59b3-173">as an example of syntax for a filter condition on a field from the root datasource as well as a field from a different datasource (for the All customers page)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-174">N</span><span class="sxs-lookup"><span data-stu-id="a59b3-174">T</span></span></td>
<td><span data-ttu-id="a59b3-175">Tänane kuupäev</span><span class="sxs-lookup"><span data-stu-id="a59b3-175">Today's date</span></span></td>
<td><span data-ttu-id="a59b3-176">Tippige <strong>T</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-176">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="a59b3-177"><strong>T</strong> vastab tänasele kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="a59b3-177"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong>-meetod sulgudes)</span><span class="sxs-lookup"><span data-stu-id="a59b3-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="a59b3-179">Vastendab <strong>SysQueryRangeUtil</strong>-meetodi parameetritega määratud väärtuse või väärtusevahemiku</span><span class="sxs-lookup"><span data-stu-id="a59b3-179">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="a59b3-180">Tippige <strong>SysQueryRangeUtil</strong>-meetod, mille parameetrid määravad väärtuse või väärtusevahemiku.</span><span class="sxs-lookup"><span data-stu-id="a59b3-180">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="a59b3-181">Klõpsake valikuid <strong>Müügireskontro</strong> &gt; <strong>Arved</strong> &gt; <strong>Ava kliendiarved</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-181">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="a59b3-182">Vajutage klahvikombinatsiooni Ctrl + Shift + F3, et avada leht <strong>Päring</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-182">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="a59b3-183">Klõpsake vahekaardil <strong>Vahemik</strong> nuppu <strong>Lisa</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-183">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="a59b3-184">Valige väljal <strong>Tabel</strong> suvand <strong>Avatud kliendikanded</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-184">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="a59b3-185">Valige väljal <strong>Väli</strong> suvand <strong>Tähtaeg</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-185">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="a59b3-186">Sisestage väljale <strong>Kriteeriumid</strong> väärtus <strong>(yearRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-186">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="a59b3-187">Klõpsake nupul <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-187">Click <strong>OK</strong>.</span></span> <span data-ttu-id="a59b3-188">Loendilehte värskendatakse, et kuvada teie sisestatud kriteeriumitele vastavad arved.</span><span class="sxs-lookup"><span data-stu-id="a59b3-188">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="a59b3-189">Selle näite puhul loetletakse kahe eelmise aasta tasumata arved.</span><span class="sxs-lookup"><span data-stu-id="a59b3-189">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="a59b3-190">Lisateavet <strong>SysQueryRangeUtil</strong>-kuupäevameetodite kohta ja mõne näite leiate järgmises jaotises toodud tabelist.</span><span class="sxs-lookup"><span data-stu-id="a59b3-190">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="a59b3-191">Täpsemad kuupäevapäringud, mis kasutavad SysQueryRangeUtil-meetodeid</span><span class="sxs-lookup"><span data-stu-id="a59b3-191">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a59b3-192">Meetod</span><span class="sxs-lookup"><span data-stu-id="a59b3-192">Method</span></span></th>
<th><span data-ttu-id="a59b3-193">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a59b3-193">Description</span></span></th>
<th><span data-ttu-id="a59b3-194">Näide</span><span class="sxs-lookup"><span data-stu-id="a59b3-194">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a59b3-195">Day (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="a59b3-195">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="a59b3-196">Leidke seansi kuupäevaga seotud kuupäev.</span><span class="sxs-lookup"><span data-stu-id="a59b3-196">Find a date relative to the session date.</span></span> <span data-ttu-id="a59b3-197">Positiivsed väärtused näitavad tulevikukuupäevi ja negatiivsed väärtused näitavad minevikukuupäev.</span><span class="sxs-lookup"><span data-stu-id="a59b3-197">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a59b3-198"><strong>Homme</strong> – sisestage <strong>(Day(1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-198"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="a59b3-199"><strong>Täna</strong> – sisestage <strong>(Day(0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-199"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="a59b3-200"><strong>Eile</strong> – sisestage <strong>(Day(-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-200"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="a59b3-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="a59b3-202">Leidke seansi kuupäevaga seotud kuupäevavahemik.</span><span class="sxs-lookup"><span data-stu-id="a59b3-202">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="a59b3-203">Positiivsed väärtused näitavad tulevikukuupäevi ja negatiivsed väärtused näitavad minevikukuupäev.</span><span class="sxs-lookup"><span data-stu-id="a59b3-203">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a59b3-204"><strong>Viimased 30 päeva</strong> – sisestage <strong>(DayRange(-30,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-204"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="a59b3-205"><strong>Eelmised 30 päeva ja järgmised 30 päeva</strong> – sisestage <strong>(DayRange(-30,30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-205"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="a59b3-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="a59b3-207">Leidke kõik kuupäevad pärast määratud suhtelist kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="a59b3-207">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a59b3-208"><strong>Rohkem kui 30 päeva alates praegusest</strong> – sisestage <strong>(GreaterThanDate(30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-208"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-209">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="a59b3-209">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="a59b3-210">Leidke kõik kuupäeva-/kellaajakirjed pärast praegust aega.</span><span class="sxs-lookup"><span data-stu-id="a59b3-210">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a59b3-211"><strong>Kõik tuleviku kuupäevad/kellaajad</strong> – sisestage <strong>(GreaterThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-211"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="a59b3-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="a59b3-213">Leidke kõik kuupäevad enne määratud suhtelist kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="a59b3-213">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a59b3-214"><strong>Vähem kui seitse päeva alates praegusest</strong> – sisestage <strong>(LessThanDate(7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-214"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-215">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="a59b3-215">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="a59b3-216">Leidke kõik kuupäeva-/kellaajakirjed enne praegust aega.</span><span class="sxs-lookup"><span data-stu-id="a59b3-216">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a59b3-217"><strong>Kõik varasemad kuupäevad/kellaajad</strong> – sisestage <strong>(LessThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-217"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="a59b3-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="a59b3-219">Leidke kuupäevavahemik praeguse kuuga seotud kuude põhjal.</span><span class="sxs-lookup"><span data-stu-id="a59b3-219">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a59b3-220"><strong>Eelmised kaks kuud</strong> – sisestage <strong>(MonthRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-220"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="a59b3-221"><strong>Järgmised kolm kuud</strong> – sisestage <strong>(MonthRange(0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-221"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a59b3-222">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="a59b3-222">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="a59b3-223">Leidke kuupäevavahemik praeguse aastaga seotud aastate põhjal.</span><span class="sxs-lookup"><span data-stu-id="a59b3-223">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a59b3-224"><strong>Järgmine aasta</strong> – sisestage <strong>(YearRange(0, 1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-224"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="a59b3-225"><strong>Eelmine aasta</strong> – sisestage <strong>(YearRange(-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a59b3-225"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]